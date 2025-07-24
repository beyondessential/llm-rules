# LLM Rules

This repository contains generic LLM agent rules that can be shared across multiple projects.

## Structure

All shared LLM rules are located directly in the root directory:

- `onboard-agent.md` - Standardized agent onboarding process
- `commit.md`, `create-branch.md`, `rebase-branch.md` - Git workflows
- `write-docs.md`, `write-card-description.md`, `create-rule.md` - Documentation creation
- `update-submodule.md`, `get-latest-rules.md` - Submodule management

## Usage

These rules are designed to be used as a git submodule in project repositories:

```bash
git submodule add https://github.com/beyondessential/llm-rules.git llm/common-rules
```

LLM agents should reference rules using the path: `llm/common-rules/[rule-name].md`

### First Time Setup

If you see an empty `llm/common-rules/` folder after pulling:

```bash
# Run this in your main repo directory
git submodule update --init --recursive
```

### Keeping Rules Updated

**Manual updates (run occasionally):**

```bash
git pull --recurse-submodules
```

**Make it completely automatic (optional):**

```bash
# Set up a post-merge hook to auto-update submodules after every pull
echo "git submodule update --remote --merge" > .git/hooks/post-merge
chmod +x .git/hooks/post-merge
```

After setting up the hook, submodules will update automatically whenever you `git pull`.

### Updating Shared Rules

**To update a rule and sync it everywhere:**
Tell the AI: "use the `update-submodule.md` rule to update [rule name]" - it will handle the submodule workflow for you.

**Manual process:**

```bash
# Make changes in the submodule
cd llm/common-rules
# ... make changes ...
git add . && git commit -m "feat: improve rule X"
git push

# Update main project to use the latest
cd ../../
git submodule update --remote llm/common-rules
git add llm/common-rules
git commit -m "deps: update shared LLM rules"
```

## Contributing

When adding or updating rules:

1. Keep rules generic and project-agnostic
2. Use Australian/NZ English spelling and terminology
3. Test rules across different project contexts
4. Follow the established rule structure (Context, Process, Avoid, Notes)

## Projects Using These Rules

- [Tamanu](https://github.com/beyondessential/tamanu) - Healthcare platform
- [Tupaia](https://github.com/beyondessential/tupaia) - Data visualization platform
