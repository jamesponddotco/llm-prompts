# CLI UX Improver

This prompt helps you improve the UX of your command-line application by
following the [Command Line Interface Guidelines](https://clig.dev/).

## Prompt

### System

```text
You will be acting as an expert code reviewer to analyze the UX of a command-line application and provide recommendations for improvement. The user will provide the code for a command-line application inside backticks.

Your task is to carefully review this code and identify ways the UX could be improved to better align with the Command Line Interface Guidelines found at clig.dev. 

First, thoroughly analyze the code, taking notes on any UX issues you notice or areas that deviate from the Command Line Interface Guidelines. Consider things like command naming, argument syntax, help documentation, output formatting, and error handling.

Then, write up your analysis inside <analysis> tags. Go through each UX issue or area for improvement you identified, citing specific examples from the code. Explain what the current issue is and provide clear recommendations on how it could be improved based on the Command Line Interface Guidelines. Be as specific as possible.

After your detailed analysis, provide a summary inside <summary> tags of the top 3-5 most important UX improvements you recommend, in order of priority. Keep these brief, referencing your earlier analysis.

Remember, the goal is to help improve the UX of the command-line application to make it as user-friendly and intuitive as possible for its users. Closely reference the Command Line Interface Guidelines in your review.
```

### User

```text
How can I improve the UX of this command-line application?

<code>
{{CODE}}
</code>
```

The content of `{{CODE}}` is omitted for brevity, but it's basically the
entire output of the [bonk
repository](https://sr.ht/~jamesponddotco/bonk/) processed through
[llmctx](https://sr.ht/~jamesponddotco/llmctx).

## Example output

### Parameters

- **Model:** claude-3-opus-20240229
- **Temperature:** 1

### Output

```text
Here is my analysis of the UX of the provided command-line application:

<analysis>

1. Command naming:
   - The command name "bonk" is quirky and memorable, tying into the "Go to horny jail" meme as explained in the README. However, it doesn't clearly convey the purpose of the tool, which is to detect nudity in images. A more descriptive name like "nudity-detector" or "image-nudity-scan" would be clearer to users unfamiliar with the meme reference.

2. Argument syntax:
   - Using a positional argument for the image/directory path is intuitive. However, the README and manpage should clarify that this argument is required, as that's not obvious from the usage help.
   - The `-t` and `-p` short options for `--threshold` and `--parallel` are not mnemonic. More intuitive short options could be used, like `-T` for threshold and `-j` for parallel (common for specifying concurrency).

3. Help documentation:
   - The `-h/--help` option is properly implemented to print usage information.
   - The README provides good background on the tool's purpose, installation, usage examples, and project details. However, it could benefit from a "Quick Start" section showing the most common usage at the top.
   - Having a manpage is great for CLI discoverability. The EXAMPLES section is helpful. Consider adding more details in the OPTIONS section to explain the threshold range and parallel default more clearly.

4. Output formatting:
   - Using JSON output is a good choice for easy parsing. However, as mentioned in the "Todo" section of the README, human-readable tabular output would be more friendly for interactive use. 
   - When switching the default output to a table, keep the JSON output available through an option for scripting use cases.
   - Consider supporting an output option to just get the list of paths of images exceeding the nudity threshold, for easier piping to other tools.

5. Error handling:
   - The error handling could be improved to provide clearer, more actionable error messages to users. For example, instead of "Permission denied when opening image file", suggest what permissions are needed.
   - Prefix error messages with "Error:" to distinguish them from normal output.

</analysis>

<summary>

In summary, the top UX improvements I recommend are:

1. Choose a command name more clearly tied to the purpose of detecting image nudity.
2. Improve usage help with argument requirement details and default option values. 
3. Add a "Quick Start" section to the README for the most common usage.
4. Support human-readable table output by default, with JSON output available via an option.
5. Polish error messages to be clearer and more actionable.

</summary>
```
