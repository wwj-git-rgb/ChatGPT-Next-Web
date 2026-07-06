---
name: add-unit-tests-for-helper-functions
description: Workflow command scaffold for add-unit-tests-for-helper-functions in ChatGPT-Next-Web.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-unit-tests-for-helper-functions

Use this workflow when working on **add-unit-tests-for-helper-functions** in `ChatGPT-Next-Web`.

## Goal

Adds new unit test files to cover previously untested pure helper functions in the codebase.

## Common Files

- `test/*.test.ts`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify untested helper functions in app/utils or similar directories.
- Write new unit tests for these helpers in a corresponding test/*.test.ts file.
- Commit the new or updated test file with a message describing the helpers covered.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.