# Context

Use this rule when you need to update the shared LLM rules to the latest version from the remote repository. This ensures you have access to the most recent rule improvements and additions.

# Process

1. **Navigate to project root**: Ensure you're in the main project directory (not inside the submodule)

2. **Update the submodule**: Run the following command to fetch and update to the latest version:

   ```bash
   git submodule update --remote llm/common-rules
   ```

3. **Review the changes**: Check what rules have been updated:

   ```bash
   git diff llm/common-rules
   ```

4. **Stage the submodule update**: Add the updated submodule reference:

   ```bash
   git add llm/common-rules
   ```

5. **Commit the update**: Commit with a descriptive message:

   ```bash
   git commit -m "deps: update shared LLM rules to latest version"
   ```

6. **Verify the update**: Confirm the rules are accessible:
   ```bash
   ls llm/common-rules/rules/
   ```

# Alternative: Update All Submodules

If you have multiple submodules and want to update all:

```bash
git submodule update --remote
git add .
git commit -m "deps: update all submodules to latest versions"
```

# Avoid

- Running the update command from inside the submodule directory
- Forgetting to commit the submodule update to the main project
- Updating submodules without reviewing the changes first
- Using `git pull` inside the submodule (this detaches from the tracked branch)

# Notes

- The submodule will be updated to the latest commit on the main branch
- This operation is safe and won't affect your project-specific rules
- Always commit the submodule update so your team gets the same rule versions
- If you encounter conflicts, resolve them in the main project, not the submodule
