---
name: document-env-variable-in-env-template
description: Workflow command scaffold for document-env-variable-in-env-template in ChatGPT-Next-Web.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /document-env-variable-in-env-template

Use this workflow when working on **document-env-variable-in-env-template** in `ChatGPT-Next-Web`.

## Goal

Documents or describes a new or existing environment variable in the .env.template file.

## Common Files

- `.env.template`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify an undocumented or new environment variable used in the codebase.
- Add a descriptive comment for the variable in .env.template.
- Commit the change with a message referencing the variable and its purpose.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.