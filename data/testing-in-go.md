# Testing in Go

This prompt helps you write better black-box tests for your Go code.
Should be used as the **user prompt** in conjunction with [Coding in
Go](coding-in-go.md) as the **system prompt**.

```
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
