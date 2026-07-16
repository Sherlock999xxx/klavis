```markdown
# klavis Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `klavis` TypeScript codebase. It covers file organization, import/export styles, commit message habits, and testing patterns. By following these guidelines, contributors can write consistent, maintainable code that fits seamlessly into the project.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `dataFetcher.ts`

### Import Style
- Use **relative imports** for referencing modules within the codebase.
  - Example:
    ```typescript
    import { fetchData } from './dataFetcher';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In dataFetcher.ts
    export function fetchData() { ... }
    ```

### Commit Patterns
- Commit messages are **freeform** (no strict prefixes).
- Average commit message length: ~58 characters.
  - Example:
    ```
    Add user profile fetch logic and update error handling
    ```

## Workflows

### Adding a New Module
**Trigger:** When you need to add a new feature or utility.
**Command:** `/add-module`

1. Create a new file using camelCase (e.g., `newFeature.ts`).
2. Implement your functionality using TypeScript.
3. Use relative imports to bring in dependencies.
4. Export your functions or constants as named exports.
5. Write a corresponding test file (e.g., `newFeature.test.ts`).
6. Commit your changes with a clear, descriptive message.

### Refactoring Existing Code
**Trigger:** When improving or restructuring code.
**Command:** `/refactor`

1. Identify the module(s) to refactor.
2. Update file names to camelCase if necessary.
3. Ensure all imports are relative and exports are named.
4. Update any affected imports in other files.
5. Run tests to verify nothing is broken.
6. Commit with a message describing the refactor.

### Writing and Running Tests
**Trigger:** When adding new code or updating existing logic.
**Command:** `/test`

1. Create or update a test file matching the pattern `*.test.ts`.
2. Write tests for all exported functions.
3. Use the project's test runner (framework unknown; check project scripts).
4. Run tests and ensure all pass before committing.

## Testing Patterns

- Test files follow the `*.test.ts` naming convention.
- The testing framework is not specified; check for scripts or documentation.
- Tests should cover all named exports and edge cases.
- Example test file:
  ```typescript
  // dataFetcher.test.ts
  import { fetchData } from './dataFetcher';

  test('fetchData returns expected result', () => {
    // test implementation
  });
  ```

## Commands
| Command       | Purpose                                   |
|---------------|-------------------------------------------|
| /add-module   | Scaffold a new module with tests          |
| /refactor     | Refactor code to match conventions        |
| /test         | Run or write tests for your code          |
```
