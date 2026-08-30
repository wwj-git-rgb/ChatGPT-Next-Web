```markdown
# ChatGPT-Next-Web Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns, coding conventions, and common workflows for contributing to the ChatGPT-Next-Web project. The codebase is written in TypeScript with no specific framework, and emphasizes clear file organization, consistent code style, and robust testing using Jest. You'll learn how to add unit tests, document environment variables, and contribute features or documentation through pull requests.

## Coding Conventions

- **File Naming:** Use camelCase for file names.
  - Example: `chatUtils.ts`, `apiClient.ts`
- **Import Style:** Use relative imports.
  - Example:
    ```typescript
    import { fetchData } from './apiClient';
    ```
- **Export Style:** Use named exports.
  - Example:
    ```typescript
    // In chatUtils.ts
    export function formatMessage(msg: string): string { ... }
    ```
    ```typescript
    // In another file
    import { formatMessage } from './chatUtils';
    ```
- **Commit Messages:** Mixed types, often prefixed with `test` or `docs`, average length ~55 characters.
  - Example: `test: add coverage for string utilities`

## Workflows

### Add Unit Tests for Helper Functions
**Trigger:** When you want to increase test coverage for utility/helper functions.
**Command:** `/add-helper-tests`

1. Identify untested helper functions in `app/utils` or similar directories.
2. Write new unit tests for these helpers in a corresponding `test/*.test.ts` file.
    - Example:
      ```typescript
      // test/formatMessage.test.ts
      import { formatMessage } from '../app/utils/chatUtils';

      test('formats message correctly', () => {
        expect(formatMessage('hello')).toBe('Hello');
      });
      ```
3. Commit the new or updated test file with a message describing the helpers covered.
    - Example: `test: add unit tests for formatMessage helper`

### Document Env Variable in Env Template
**Trigger:** When you add or clarify an environment variable for configuration.
**Command:** `/document-env-var`

1. Identify an undocumented or new environment variable used in the codebase.
2. Add a descriptive comment for the variable in `.env.template`.
    - Example:
      ```
      # API_KEY: The key used for authenticating API requests
      API_KEY=
      ```
3. Commit the change with a message referencing the variable and its purpose.
    - Example: `docs: document API_KEY in .env.template`

### Merge Feature Branch via Pull Request
**Trigger:** When a new feature, test, or documentation change is ready to be merged.
**Command:** `/merge-pr`

1. Push feature or documentation changes to a branch.
2. Open a pull request with a descriptive title and summary.
3. Merge the pull request, resulting in a merge commit that references the feature branch and the original commit.

## Testing Patterns

- **Framework:** Jest
- **Test File Pattern:** `*.test.ts`
- **Test Example:**
  ```typescript
  // test/sum.test.ts
  import { sum } from '../app/utils/math';

  test('adds numbers correctly', () => {
    expect(sum(1, 2)).toBe(3);
  });
  ```
- Place tests in the `test/` directory, mirroring the structure of the code being tested.

## Commands

| Command            | Purpose                                                        |
|--------------------|----------------------------------------------------------------|
| /add-helper-tests  | Add unit tests for helper functions                            |
| /document-env-var  | Document or clarify an environment variable in .env.template   |
| /merge-pr          | Merge a feature or documentation branch via pull request       |
```