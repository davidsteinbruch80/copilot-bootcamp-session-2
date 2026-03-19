# Coding Guidelines

## Overview

This document outlines the coding standards and quality principles for the TODO application. Following these guidelines ensures consistency across the codebase, improves maintainability, and enhances developer collaboration.

## Code Formatting

We use consistent formatting rules to maintain code readability. All JavaScript and TypeScript files should be formatted using Prettier with the default configuration. Key formatting standards include:

- Use 2 spaces for indentation
- Maximum line length of 80 characters where practical
- Always use semicolons to terminate statements
- Use single quotes for strings unless escaping is required
- Include trailing commas in multi-line objects and arrays

## Import Organization

Organize imports in a clear, hierarchical structure to improve code readability:

1. External library imports first (React, Express, etc.)
2. Internal module imports second (utilities, components)
3. Relative imports last (./components, ../utils)
4. Group imports by type and separate groups with blank lines
5. Use absolute imports for shared utilities and components when possible

## Linting and Code Quality

We enforce code quality through ESLint configuration with the following principles:

- Use ESLint with recommended rules for JavaScript/TypeScript
- Enable React-specific linting rules for frontend code
- Configure ESLint to catch potential bugs and enforce consistent patterns
- All code must pass linting checks before commits
- Use `eslint-disable` comments sparingly and only with justification

## Best Practices

### DRY Principle (Don't Repeat Yourself)
Extract common functionality into reusable functions, components, and utilities. If you find yourself writing similar code in multiple places, consider refactoring into a shared module.

### Meaningful Names
Use descriptive variable, function, and component names that clearly express intent. Avoid abbreviations and single-letter variables except for loop counters and widely understood conventions.

### Function Design
Keep functions small and focused on a single responsibility. Functions should ideally do one thing well and have minimal side effects. Use pure functions where possible for better testability.

### Error Handling
Implement proper error handling throughout the application. Use try-catch blocks for asynchronous operations and provide meaningful error messages for debugging and user feedback.

### Comments and Documentation
Write comments that explain why something is done, not what is done. The code should be self-documenting through clear naming and structure. Use JSDoc comments for function documentation when the purpose isn't immediately obvious.

## File Organization

Structure files and directories logically to make the codebase easy to navigate:

- Group related files together in appropriate directories
- Use consistent naming conventions for files and folders
- Keep file sizes reasonable by splitting large components or modules
- Place test files adjacent to the code they test

## Performance Considerations

Write efficient code that considers performance implications:

- Avoid unnecessary re-renders in React components
- Use appropriate data structures for the task
- Implement lazy loading for large datasets or components
- Minimize bundle size by avoiding unnecessary dependencies