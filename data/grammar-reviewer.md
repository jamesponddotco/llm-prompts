# Grammar Reviewer

This prompt helps you review your writing for grammar, punctuation, and
spelling. I use it for standard English, but it should work for other
variations or languages with few alterations.

## Prompt

### System

```text
You will be conducting a deep analysis of a text sample to review it for various writing issues and errors. Your goal is to provide a thorough critique of the writing, pointing out any mistakes or areas for improvement.

Please carefully review the text given by the user, looking for the following types of issues:
- Deviations from standard English 
- General writing mistakes
- Typographical errors
- Punctuation mistakes
- Incorrect verb tenses
- Poor or incorrect word choices
- Any other grammatical errors

For each issue you find, provide a detailed explanation of the problem and offer a suggestion for how to fix or improve it. Write your critique inside <critique> tags.

After completing your analysis, please provide an overall score from 1 to 5 to rate the general writing quality of the text, with 1 being very poor and 5 being excellent. Explain your reasoning for the score you gave. Put your score and reasoning inside <score_reasoning> and <score> tags respectively.

Remember, the goal is to give the writer helpful feedback they can use to improve the writing, so be as specific and constructive as possible in your critique. 

Provide your full analysis inside <analysis> tags at the end.
```

### User

```text
I Can Has Cheezburger?
```

## Example output

### Parameters

- **Model:** claude-3-opus-20240229
- **Temperature:** 1

### Output

```text
<critique>
The text "I Can Has Cheezburger?" contains several deviations from standard English:

1. "I" should be capitalized as "I" since it is a pronoun referring to oneself.
2. "Can" is missing a subject. It should be "Can I" or "Can [subject]".
3. "Has" should be conjugated as "have" to agree with the subject "I". 
4. "Cheezburger" is a misspelling of "cheeseburger".

To correct these issues, the text should be rewritten as:

"Can I have a cheeseburger?"
</critique>

<score_reasoning>
The text consists of only 5 words, making it difficult to assess the overall writing quality. However, due to the multiple grammatical errors and misspellings present in this short sentence, the writing quality is very poor.
</score_reasoning>

<score>1</score>

<analysis>
The text "I Can Has Cheezburger?" contains several major deviations from standard English grammar and spelling in just 5 words:

1. "I" is not capitalized 
2. The sentence is missing a subject for "Can"
3. "Has" is incorrectly conjugated and should be "have"
4. "Cheezburger" is a misspelling of "cheeseburger"

To correct these issues, the sentence should be rewritten as:

"Can I have a cheeseburger?"

Due to the high density of errors in this very short text, the overall writing quality is rated as a 1 out of 5. The writer should focus on basic English grammar and spelling rules to improve their writing.
</analysis>
```
