# Context

Use this rule when you need to write a pull request description for work that's been completed on a feature branch. This helps create consistent, informative PR descriptions that reviewers can easily understand.

# Process

1. **Gather context about the work**:

   - Review commit history: `git log --oneline main..HEAD`
   - Check files changed: `git diff main --name-only`
   - Understand the scope and purpose of the changes

2. **Write a clear summary**: Start with a brief description of what was accomplished and why

3. **Structure the description**:

   - **Summary paragraph**: High-level description of the changes
   - **Key changes**: Bullet points highlighting the main modifications
   - **Benefits**: What this enables or improves
   - **Any deployment considerations**: If applicable

4. **Use conversational tone**: Write like you're explaining the changes to a colleague

5. **Include testing considerations**: Note any areas that need particular attention during review

6. **Add agentic label**: Include `{agentic: [MODEL_NAME]}` at the end if an AI assisted with the work

# Template Structure

```
### Changes

[Brief summary of what was accomplished and why]

**Key changes:**
- [Bullet point of main change]
- [Another key modification]
- [Additional important change]

**Benefits:**
- [What this enables]
- [What this improves]
- [Additional benefit]

[Any additional context sections as needed]

{agentic: [MODEL_NAME]}
```

# Avoid

- Writing overly technical descriptions that don't explain the "why"
- Including every minor detail - focus on what reviewers need to know
- Forgetting to explain the business value or problem being solved
- Using jargon without context
- Making assumptions about reviewer knowledge

# Notes

- Focus on the value delivered rather than just listing technical changes
- Help reviewers understand what to pay attention to during review
- Use Australian/NZ English spelling and terminology
- Keep the tone professional but friendly and conversational
