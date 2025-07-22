# LLM Rules

This repository contains generic LLM agent rules that can be shared across multiple projects.

## Structure

- `rules/` - Contains all shared LLM rules
  - `onboard-agent.md` - Standardized agent onboarding process
  - `commit.md`, `create-branch.md`, `rebase-branch.md` - Git workflows
  - `write-docs.md`, `write-card-description.md`, `create-rule.md` - Documentation creation
  - `update-submodule.md`, `get-latest-rules.md` - Submodule management

## Usage

These rules are designed to be used as a git submodule in project repositories:

```bash
git submodule add https://github.com/beyondessential/llm-rules.git llm/common-rules
```

LLM agents should reference rules using the path: `llm/common-rules/rules/[rule-name].md`

## Contributing

When adding or updating rules:

1. Keep rules generic and project-agnostic
2. Use Australian/NZ English spelling and terminology
3. Test rules across different project contexts
4. Follow the established rule structure (Context, Process, Avoid, Notes)

## Projects Using These Rules

- [Tamanu](https://github.com/beyondessential/tamanu) - Healthcare platform
- [Tupaia](https://github.com/beyondessential/tupaia) - Data visualization platform
