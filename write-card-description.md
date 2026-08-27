# Context

Use this rule when creating card descriptions for Linear or similar project management tools, especially when documenting changes that have already been made but need a retrospective card description.

Focus on concise, problem-first card descriptions that explain the "why" rather than listing detailed technical changes. Use gentle, non-directive language appropriate for NZ/Australian culture.

# Process

- Start by identifying the core problem or pain point that motivated the changes
- Only assert a problem you actually have evidence for. If you don't know how
  things currently work, describe what the change gives rather than asserting
  what's wrong today — "a command that reports X" instead of "there's no way to
  see X"
- Present the problem first in a conversational tone that explains what was going wrong or missing
- Follow with a broad outline of the solution approach, not detailed implementation steps
- Structure as 2-3 sentences total, but sentences can be longer and more conversational
- Use line breaks to separate the problem statement from the solution outline
- Write in present tense as if planning the work (even if retrospective)
- Focus on the business/development impact rather than technical specifics
- Use gentle language: "we could", "we can", "might", "tends to" rather than directive commands
- Avoid overly strong or prescriptive wording

Example structure:

```
[Problem statement explaining what's wrong or missing, using gentle language]

[Solution approach at a high level, suggesting rather than commanding]
```

# Avoid

- Inventing a problem statement to fill the structure. The problem-first shape
  invites a confident opening line, which is exactly where a guess slips in.
  A fabricated claim about the current state of a codebase, team, or deployment
  reads as criticism of someone else's work, and it gets the whole card
  dismissed for cause — including the parts that were well founded. This matters
  most when filing into another team's project, where you are least likely to
  have read the code you are describing
- Writing in past tense when creating cards (use present tense as if planning)
- Leading with the solution instead of the problem
- Using overly directive language - prefer gentle suggestions like "we could" or "we can"
- Using bold formatting - keep all text plain

# Notes

- Use Australian/NZ English spelling and terminology in card descriptions
- Adapt language style to match team culture and communication norms (casual, friendly, competent)
