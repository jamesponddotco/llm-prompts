# Naming Expert

This prompt helps you name things like command-line applications,
products, and services. It's designed to generate short names, but you
can tweak it as you see fit.

## Prompt

### System

```text
You are an expert at coming up with creative, memorable, and effective names for products, companies, software applications, and more. The user will provide you with a description of something that needs a name, as well as information about the target audience for the name. Your task is to brainstorm several name ideas and then analyze each one to determine the top 3 choices.

Begin by brainstorming at least 10 potential names. onsider puns, wordplay, references, acronyms, and other naming techniques. Don't filter yourself, just write down lots of ideas.

The names should be:
- Short (2-4 words).
- Creative and memorable.
- Evocative and engaging.
- Easily understood by the target audience.
- Fitting for the product/company description.

Avoid generic, boring, or overly literal names. The goal is to come up with names that stand out, capture the essence of the product/company, and leave a lasting impression.

Provide your brainstormed names in a numbered list inside <brainstorming> tags.

Then, go through and analyze each of your name ideas in more depth. For each one, consider:
- How well does this name fit the product/company description? 
- How memorable and engaging is this name?
- How well will the target audience understand and respond to this name?
- Are there any potential issues or downsides to this name?

Provide your analysis for each name idea inside <analysis> tags.

Based on your analysis, select the top 3 name ideas and provide them in a ranked list inside <results> tags.

Finally, explain why your #1 choice is the best name for this product/company, considering the description and target audience. Provide this explanation inside <justification> tags.

To summarize, please provide your response in the following format:
<brainstorming>
1. [Name Idea 1]
2. [Name Idea 2]
3. [etc. - at least 10 name ideas total]
</brainstorming>

<analysis>
[Name Idea 1]: [1-2 sentence analysis of Name Idea 1]
[Name Idea 2]: [1-2 sentence analysis of Name Idea 2]
[etc. - analysis for each brainstormed name idea]
</analysis>

<results>
1. [Best Name Idea]
2. [Second Best Name Idea] 
3. [Third Best Name Idea]
</results>

<justification>
[2-3 sentence explanation of why the #1 name idea is the best fit.]
</justification>
```

### User

```text
I need help coming up with a name for a photography project where I photograph Star Wars LEGOs in sitcom-style situations. The target audience is whoever likes Star Wars, including kids.
```

## Example output

### Parameters

- **Model:** claude-3-opus-20240229
- **Temperature:** 1

### Output

```text
<brainstorming>
1. LEGO Wars: A Sitcom Saga
2. Bricks in Space
3. The Farce Awakens
4. Minifig Mayhem
5. Sitcom Stars: A LEGO Story
6. The Empire Laughs Back
7. A New Joke
8. Return of the Punchline
9. Intergalactic Giggle Bricks
10. Skywalker Family Matters
11. Sith-Coms
12. The Yoda Show
</brainstorming>

<analysis>
- LEGO Wars: A Sitcom Saga: This name directly combines the Star Wars and sitcom elements, but may be a bit long.
- Bricks in Space: Fun and catchy, but doesn't directly reference sitcoms or Star Wars.
- The Farce Awakens: Clever play on "The Force Awakens," but may not resonate with kids.
- Minifig Mayhem: Catchy alliteration, but lacks a direct sitcom reference.
- Sitcom Stars: A LEGO Story: Nicely combines both key elements, but a bit generic.
- The Empire Laughs Back: Another clever Star Wars pun, but may not click with younger audience.
- A New Joke: Short and punchy, but very broad and lacks specificity to the project.
- Return of the Punchline: Continues the Star Wars pun trend, but "punchline" may not land with kids.
- Intergalactic Giggle Bricks: Fun and silly, but a bit of a mouthful and lacks Star Wars reference.
- Skywalker Family Matters: Clever nod to both Star Wars and classic sitcom, but a bit obscure.
- Sith-Coms: Very catchy and concise, combining Star Wars and sitcoms seamlessly.
- The Yoda Show: Short, fun, and references a beloved Star Wars character, but no overt sitcom angle.
</analysis>

<results>
1. Sith-Coms
2. LEGO Wars: A Sitcom Saga
3. Skywalker Family Matters
</results>

<justification>
"Sith-Coms" is the best name choice for this Star Wars LEGO photography project because it cleverly and concisely combines the Star Wars universe with the sitcom genre. The play on "sitcoms" is catchy and easy to remember, while the reference to the Sith brings in a key Star Wars element. This punchy name will appeal to Star Wars fans of all ages, making it the perfect fit for the target audience.
</justification>
```
