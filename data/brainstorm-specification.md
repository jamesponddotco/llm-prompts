# Brainstorm Specification

This prompt turns a conversation you had with [Socratic
Coder](socratic-coder.md) into a developer-ready specification. The
specification it helps you write is quite helpful when coming up with a
development plan or when using LLMs to code.

The prompt should be used as the **user prompt** after a conversation
with [Socratic Coder](socratic-coder.md) has come to a natural
conclusion.

## Prompt

### System

See [Socratic Coder](socratic-coder.md) for the system prompt.

### User
```text
Now that we have wrapped up the brainstorming process, you are tasked with compiling our findings into a comprehensive, developer-ready specification, similar to an RFC (Request for Comments). Your goal is to create a document that a developer can use to immediately begin implementation.

First, carefully review the brainstorming session we had so far. Analyze the session thoroughly, identifying key requirements, architectural decisions, data handling approaches, and any other relevant information for the project.

Based on your analysis, create a structured specification document with the following sections:

1. Introduction
   - Briefly describe the project's purpose and goals
   - Provide any necessary context or background information

2. Requirements
   - List all functional and non-functional requirements
   - Prioritize requirements if possible (e.g., must-have, should-have, nice-to-have)

3. Architecture
   - Describe the overall system architecture
   - Include any diagrams or flowcharts if mentioned in the brainstorming notes
   - Explain key components and their interactions

4. Data Handling
   - Detail data models and structures
   - Explain data flow within the system
   - Address any data storage, retrieval, or processing considerations

5. API Design (if applicable)
   - Define API endpoints, request/response formats, and authentication methods

6. Error Handling
   - Outline strategies for handling various types of errors
   - Include error codes and messages where appropriate

7. Performance Considerations
   - Discuss any performance requirements or optimizations

8. Security Measures
   - Address security concerns and proposed solutions

9. Testing Plan
   - Outline a comprehensive testing strategy
   - Include unit testing, integration testing, and any specific test scenarios

10. Implementation Timeline (if available from the brainstorming notes)
    - Provide estimated timeframes for different phases of the project

11. Open Questions and Future Considerations
    - List any unresolved issues or areas that need further discussion

When creating this specification:
- Use clear, concise language suitable for technical readers
- Provide sufficient detail for developers to begin implementation
- Ensure consistency throughout the document
- Use numbered lists, bullet points, or tables where appropriate to improve readability
- Include any relevant code snippets, pseudocode, or examples mentioned in the brainstorming notes

Your final output should be a well-structured, comprehensive specification document. Begin your response with <specification> and end it with </specification>. The content within these tags should be the complete, developer-ready specification without any additional commentary or meta-discussion.
```
