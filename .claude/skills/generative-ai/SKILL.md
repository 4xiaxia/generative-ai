```markdown
# generative-ai Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill introduces the core development patterns and conventions used in the `generative-ai` TypeScript codebase. It covers file organization, code style, commit practices, and testing approaches. By following these guidelines, contributors can maintain consistency and quality across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for filenames.
  - Example: `textGenerator.ts`, `apiClient.ts`

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { generateText } from './textGenerator';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In textGenerator.ts
    export function generateText(prompt: string): string { ... }
    ```

### Commit Messages
- Follow **Conventional Commits** with the `chore` prefix for maintenance tasks.
  - Example:  
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Code Contribution
**Trigger:** When adding new features or fixing bugs  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Implement your changes following the coding conventions.
3. Write or update tests as needed.
4. Commit using the conventional commit format (e.g., `chore: add new feature X`).
5. Push your branch and open a pull request.

### Dependency Update
**Trigger:** When dependencies need to be updated  
**Command:** `/update-deps`

1. Run the package manager to update dependencies.
   - Example: `npm update`
2. Test the application to ensure compatibility.
3. Commit changes with a message like `chore: update dependencies`.
4. Push and create a pull request.

## Testing Patterns

- Test files use the pattern `*.test.*` (e.g., `textGenerator.test.ts`).
- The specific testing framework is not detected; ensure your tests are self-contained and follow the project's import/export conventions.
- Example test file:
  ```typescript
  import { generateText } from './textGenerator';

  test('generateText returns expected output', () => {
    expect(generateText('hello')).toBe('Hello, world!');
  });
  ```

## Commands
| Command         | Purpose                                 |
|-----------------|-----------------------------------------|
| /contribute     | Start the code contribution workflow    |
| /update-deps    | Update project dependencies             |
```
