# Context

Use this rule when you need to make improvements to the shared LLM rules that should be available across all projects. This covers adding new rules, updating existing ones, or fixing issues in the shared repository.

# Process

1. **Navigate to the submodule**: Enter the common rules directory:

   ```bash
   cd llm/common-rules
   ```

2. **Ensure you're on main branch**: Check and switch if needed:

   ```bash
   git branch
   git checkout main
   ```

3. **Pull latest changes**: Get the most recent version before making changes:

   ```bash
   git pull origin main
   ```

4. **Make your changes**: Edit rule files in the root directory or update the README

5. **Stage your changes**: Add the modified files:

   ```bash
   git add .
   ```

6. **Commit with conventional format**: Use a descriptive commit message:

   ```bash
   git commit -m "feat: add new rule for X"
   # or
   git commit -m "fix: improve clarity in Y rule"
   # or
   git commit -m "docs: update README with usage examples"
   ```

7. **Push to remote**: Send changes to the shared repository:

   ```bash
   git push origin main
   ```

8. **Return to project root**: Navigate back to the main project:

   ```bash
   cd ../../
   ```

9. **Update main project**: Update the submodule reference in the main project:
   ```bash
   git add llm/common-rules
   git commit -m "deps: update shared LLM rules with latest changes"
   ```

# Common Update Types

**Adding a new rule:**

```bash
# Create new rule file
echo "# New Rule" > new-rule.md
git add new-rule.md
git commit -m "feat: add rule for handling X scenarios"
```

**Updating existing rule:**

```bash
# Edit existing rule
git add existing-rule.md
git commit -m "fix: clarify process steps in existing-rule"
```

**Updating documentation:**

```bash
git add README.md
git commit -m "docs: add contributing guidelines"
```

# Avoid

- Making changes without pulling latest first
- Forgetting to update the main project's submodule reference
- Using unclear commit messages
- Making project-specific changes to shared rules
- Committing directly to main without testing the rule first

# Notes

- Always test rule changes in at least one project before pushing
- Keep rules generic and project-agnostic
- Use Australian/NZ English spelling and terminology
- Follow conventional commit format for consistency
- Consider the impact on all projects using these rules
