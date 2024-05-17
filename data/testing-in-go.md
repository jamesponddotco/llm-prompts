# Testing in Go

This prompt helps you write better black-box tests for your Go code.
Should be used as the **user prompt** in conjunction with [Coding in
Go](coding-in-go.md) as the **system prompt**.

## Prompt

### System

See [Coding in Go](coding-in-go.md) for the system prompt.


### User
```text
You will be creating full coverage black-box table-driven tests with sub-tests for some Go code. 

Here is the Go code to be tested:

<code>
{{CODE}}
</code>

And here are any existing tests for the code (if none exist, this will be blank):

<existing_tests>
{{TESTS}}
</existing_tests>

First, carefully analyze the provided Go code and existing tests. Identify the main public functions, along with their input parameters and return values. Consider key scenarios, edge cases, and possible error conditions that need to be tested for each function.

Next, create a test plan covering all the key scenarios, edge cases, and error conditions you identified. Structure this as a bulleted list with one line for each test case. For each case, specify the function to test, the input parameter values, and the expected result.

Then, write out the full table-driven tests with sub-tests in Go following the test plan you created. Use t.Run() for sub-tests. Aim for complete coverage of the scenarios in your test plan. 

Remember to follow Go testing best practices:
- Use meaningful test case names that describe the scenario.
- Perform assertions on all relevant return values and side effects.
- Keep each test case focused and independent.
- Ensure the tests are deterministic and not flaky.
- Provide clear failure messages on assertion failures.

Write your test code inside <test_code> tags.

After writing the test code, provide a brief explanation of your test approach and how you ensured full coverage. Discuss any remaining limitations or areas that could still benefit from additional testing. Provide this summary inside <test_summary> tags.
```

For the example output below, `{{CODE}}` was replaced with:

```go
func DrainResponseBody(resp *http.Response) error {
	if resp == nil {
		return fmt.Errorf("%w: nil response", ErrCannotDrainResponse)
	}

	_, err := io.Copy(io.Discard, resp.Body)
	if err != nil {
		return fmt.Errorf("%w: %w", ErrCannotDrainResponse, err)
	}

	if err = resp.Body.Close(); err != nil {
		return fmt.Errorf("%w: %w", ErrCannotCloseResponse, err)
	}

	return nil
}
```

`{{TESTS}}` was left blank.

## Example output

### Parameters

- **Model:** claude-3-opus-20240229
- **Temperature:** 1

### Output

````text
Here is my analysis and test plan for the provided DrainResponseBody() function:

The DrainResponseBody() function takes an *http.Response as input and returns an error. It discards the response body and closes it. The key scenarios to test are:

- Nil response passed in (should return ErrCannotDrainResponse)
- Response body read fails (should return ErrCannotDrainResponse)
- Response body close fails (should return ErrCannotCloseResponse) 
- Success case (no errors, body drained and closed)

Test Plan:
- Nil response 
- io.Copy fails
- resp.Body.Close fails
- Successful drain and close

<test_code>
```go
package httputil

import (
    "errors"
    "io"
    "net/http"
    "strings"
    "testing"
)

func TestDrainResponseBody(t *testing.T) {
    t.Parallel()

    tests := []struct {
        name    string
        resp    *http.Response
        wantErr error
    }{
        {
            name:    "NilResponse",
            resp:    nil,
            wantErr: ErrCannotDrainResponse,
        },
        {
            name: "CopyFails",
            resp: &http.Response{
                Body: io.NopCloser(errorReader{}),
            },
            wantErr: ErrCannotDrainResponse,
        },
        {
            name: "CloseFails",
            resp: &http.Response{
                Body: &failCloseReader{Reader: strings.NewReader("body")},
            },
            wantErr: ErrCannotCloseResponse,
        },
        {
            name: "Success",
            resp: &http.Response{
                Body: io.NopCloser(strings.NewReader("body")),
            },
            wantErr: nil,
        },
    }

    for _, tt := range tests {
        tt := tt

        t.Run(tt.name, func(t *testing.T) {
            t.Parallel()

            err := DrainResponseBody(tt.resp)
            if !errors.Is(err, tt.wantErr) {
                t.Errorf("DrainResponseBody() error = %v, wantErr = %v", err, tt.wantErr)
            }
        })
    }
}

type errorReader struct{}

func (r errorReader) Read(p []byte) (n int, err error) {
    return 0, errors.New("read failed")
}

type failCloseReader struct {
    io.Reader
}

func (r *failCloseReader) Close() error {
    return errors.New("close failed")
}
```
</test_code>

<test_summary>

The test covers all the key scenarios identified during analysis:

1. It tests passing a nil response, verifying the expected ErrCannotDrainResponse is returned.

2. It tests the case where io.Copy fails while reading the response body, using a custom errorReader. This ensures ErrCannotDrainResponse is returned.

3. It tests when Close fails on the response body, using a custom failCloseReader. This checks that ErrCannotCloseResponse is returned in this scenario.

4. Finally, it includes a success case with a normal response body, validating that no error is returned when draining and closing succeed.

The sub-tests use t.Parallel for independent and concurrent execution.

One limitation is that it doesn't validate the response body was fully read and discarded in the success case. However, this is difficult to deterministically test from a black-box perspective.

Overall, this provides good coverage of the key behaviors and error scenarios of DrainResponseBody using table-driven tests and sub-tests in an idiomatic Go style.
</test_summary>
````
