# Brainstorm Critique

After having a conversation with [Socratic Coder](socratic-coder.md) and
turning that conversation into [a developer-ready
specification](brainstorm-specification.md), you can use this prompt to
create a critique of the plan so you can improve on the specification.

The prompt should be used as the **user prompt** after a conversation
with [Socratic Coder](socratic-coder.md) has come to a natural
conclusion and a specification for the project has been written.

## Prompt

### System

See [Socratic Coder](socratic-coder.md) for the system prompt.

### User
```text
Now that we have wrapped up the brainstorming process, acting like a third-party software engineer tasked with critically analyzing a project idea that has just completed its brainstorming phase, poke holes in the idea. Your goal is to identify potential flaws, challenges, and areas of improvement in the project concept. Approach this task with a constructive yet critical mindset, drawing from your expertise as an experienced software engineer.

First, review the brainstorm session so far, then examine the results of our brainstorming session.

Your task is to critically analyze the project idea and brainstorming results. Consider the following aspects:

1. Technical feasibility: Are there any technical challenges or limitations that may have been overlooked?
2. Scalability: How well would this solution scale as user base or data volume grows?
3. Security and privacy: Are there potential vulnerabilities or data protection issues?
4. User experience: Could there be usability problems or friction points for the end-users?
5. Market fit: Is there a clear need for this solution? How does it compare to existing alternatives?
6. Resource requirements: Are the necessary skills, time, and budget realistically accounted for?
7. Regulatory compliance: Are there any legal or regulatory hurdles that might affect implementation?
8. Maintenance and support: What long-term challenges might arise in maintaining and supporting this solution?

Provide a thorough analysis, pointing out potential issues, risks, or oversights in the current project concept. For each point you raise, briefly explain why it's a concern and, if possible, suggest a potential mitigation strategy or area for further investigation.

Present your analysis in a clear, organized manner. Use bullet points or numbered lists where appropriate to enhance readability. Be specific in your critiques, referencing particular aspects of the project summary or brainstorming results where relevant.

Remember, your goal is to help improve the project by identifying potential weaknesses or oversights. Maintain a professional and constructive tone throughout your analysis.

Your final output should be structured as follows:

<critical_analysis>
[Your detailed analysis here, organized by the aspects mentioned above or other relevant categories]
</critical_analysis>

<recommendations>
[A concise list of key recommendations or areas for further exploration based on your analysis]
</recommendations>

Ensure that your final output contains only the <critical_analysis> and <recommendations> sections, without any additional commentary or explanation.
```
