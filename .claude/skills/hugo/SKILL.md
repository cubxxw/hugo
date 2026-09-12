```markdown
# hugo Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the development patterns and conventions used in the `hugo` repository, which is a Go codebase with no detected framework. You'll learn how to structure files, write imports and exports, follow commit message conventions, and understand the project's testing patterns. This guide also provides suggested commands for common workflows.

## Coding Conventions

### File Naming
- Use **snake_case** for file names.
  - Example: `my_module.go`, `image_utils.go`

### Imports
- Use **relative imports** within the codebase.
  - Example:
    ```go
    import "./utils"
    ```

### Exports
- Use **named exports** for functions, types, and variables.
  - Example:
    ```go
    // In utils.go
    package utils

    func ExportedFunction() {
        // ...
    }
    ```

### Commit Messages
- Commit messages are **freeform** but often use prefixes like `all`, `images`.
- Keep commit messages concise (average length: 56 characters).
  - Example:
    ```
    images: update image processing for new format
    all: refactor error handling across modules
    ```

## Workflows

### Code Contribution
**Trigger:** When you want to add or update code in the repository  
**Command:** `/contribute`

1. Create a new branch for your feature or fix.
2. Write code using snake_case file naming and relative imports.
3. Use named exports for all public functions/types.
4. Write a concise, prefixed commit message (e.g., `images: improve loader`).
5. Push your branch and open a pull request.

### Testing Code
**Trigger:** When you want to test your changes  
**Command:** `/test`

1. Locate or create test files following the `*.test.*` pattern.
2. Write tests for your new or updated code.
3. Run tests using the Go testing tool:
    ```sh
    go test ./...
    ```
4. Ensure all tests pass before submitting your changes.

### Reviewing Commits
**Trigger:** When reviewing code for consistency  
**Command:** `/review-commits`

1. Check that commit messages use appropriate prefixes (`all`, `images`, etc.).
2. Ensure messages are clear and concise.
3. Verify that code changes follow file naming, import, and export conventions.

## Testing Patterns

- Test files follow the `*.test.*` naming pattern (e.g., `utils.test.go`).
- The testing framework is not explicitly defined, but standard Go testing practices are assumed.
- Example test file:
    ```go
    // utils.test.go
    package utils

    import "testing"

    func TestExportedFunction(t *testing.T) {
        // Test logic here
    }
    ```

## Commands
| Command         | Purpose                                         |
|-----------------|-------------------------------------------------|
| /contribute     | Guide for contributing code                     |
| /test           | Instructions for running and writing tests       |
| /review-commits | Checklist for reviewing commit message patterns  |
```
