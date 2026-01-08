# Contributing to PearPass

Thank you for your interest in contributing to PearPass! We welcome contributions from the community and are grateful for your support. This document provides guidelines and best practices to help you contribute effectively.

The source is open to use as per the [LICENSE](./LICENSE).

> **Note:** Any pull-request or issue may be closed without explanation.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Issues](#issues)
- [Pull Requests](#pull-requests)
- [Development Guidelines](#development-guidelines)
- [Testing Requirements](#testing-requirements)
- [Cross-Platform Development](#cross-platform-development)
- [Review Process](#review-process)
- [Community](#community)
- [License](#license)

## Code of Conduct

By participating in this project, you agree to maintain a respectful and inclusive environment for everyone. Please:

- Be respectful and considerate in your communications
- Provide constructive feedback
- Focus on what is best for the community and the project
- Show empathy towards other community members

## Getting Started

1. **Fork the repository** and clone it locally
2. **Set up your development environment** following the [README](./README.md)
3. **Create a new branch** from `dev` for your changes
4. **Make your changes** following our development guidelines
5. **Submit a pull request** to the `dev` branch

## Issues

### Reporting Bugs

When reporting bugs, please include:

- A clear and descriptive title
- Steps to reproduce the issue
- Expected behavior vs. actual behavior
- Screenshots or recordings if applicable
- Your environment details (OS, Node.js version, etc.)
- A failing test case (if possible)

### Feature Requests

Feature requests are welcome! Please provide:

- A clear description of the feature
- The problem it solves or the value it adds
- Any relevant use cases or examples
- Consideration for how it might impact other platforms (mobile, browser extension)

## Pull Requests

### Branch Strategy

- **All PRs must target the `dev` branch** - PRs to `main` will not be accepted
- Create feature branches from `dev` with descriptive names (e.g., `feature/password-export`, `fix/login-validation`)

### PR Requirements

Before submitting a PR, ensure:

1. **Use the PR Template** - All PRs must follow our [PR template](./.github/pull_request_template.md)
2. **CI Checks Pass** - All CI checks must pass before a PR can be reviewed
3. **Code Review** - PRs require approval from **at least 2 core team members**
4. **Tests** - All new code must be covered with tests
5. **Linting** - Code must pass linting: `npm run lint`
6. **Tests Passing** - All tests must pass: `npm test`

### PR Best Practices

- Keep PRs focused on a single feature or bug fix
- Provide a clear and detailed description of changes
- Link to related issues using keywords (e.g., "Fixes #123", "Closes #456")
- Keep commits atomic and well-documented
- Respond promptly to review feedback
- Rebase your branch on `dev` before submitting if needed

### What NOT to Include

- **Do NOT bump package versions** - Project versions are automatically bumped when changes are merged to `main`
- Do NOT include unrelated changes or refactoring
- Do NOT include generated files unless absolutely necessary

## Development Guidelines

### Code Quality Standards

We follow industry best practices and principles:

#### Clean Code

- Write readable, self-documenting code
- Use meaningful variable and function names
- Keep functions small and focused
- Avoid deep nesting and complex conditionals
- Add comments only when necessary to explain "why", not "what"

#### Clean Architecture

- Separate concerns into appropriate layers
- Keep business logic independent of frameworks and UI
- Use dependency injection where appropriate
- Follow the project's established folder structure

#### KISS (Keep It Simple, Stupid)

- Prefer simple solutions over complex ones
- Avoid over-engineering
- Write code that is easy to understand and maintain

#### SOLID Principles

- **S**ingle Responsibility: Each module/class should have one reason to change
- **O**pen/Closed: Open for extension, closed for modification
- **L**iskov Substitution: Subtypes must be substitutable for their base types
- **I**nterface Segregation: Prefer specific interfaces over general ones
- **D**ependency Inversion: Depend on abstractions, not concretions

#### Additional Standards

- Follow existing code style and patterns in the codebase
- Handle errors appropriately
- Write performant code - be mindful of memory and CPU usage

## Testing Requirements

### Test Requirements

- **All new code must be covered with tests**
- Tests should cover happy paths, edge cases, and error scenarios
- Both unit tests and integration tests are encouraged

### Running Tests

```bash
# Run unit tests
npm test

# Run linting
npm run lint
```

### Test Best Practices

- Write tests that are independent and isolated
- Use descriptive test names that explain what is being tested
- Follow the AAA pattern (Arrange, Act, Assert)
- Mock external dependencies appropriately
- Keep tests fast and reliable

## Cross-Platform Development

PearPass is a multi-platform ecosystem. To maintain consistency across all platforms:

> **Important:** Any new feature or functionality implemented in this desktop application must also be implemented in the other PearPass applications:
>
> - [pearpass-app-mobile](https://github.com/tetherto/pearpass-app-mobile) - Mobile application
> - [pearpass-app-browser-extension](https://github.com/tetherto/pearpass-app-browser-extension) - Browser extension

### Cross-Platform Guidelines

- Consider how your feature will work on all platforms
- Use shared libraries when possible (e.g., `pearpass-lib-vault`)
- Document any platform-specific behavior
- Coordinate with other platform maintainers when needed
- Ensure UI/UX consistency across platforms

## Review Process

### How Reviews Work

1. Submit your PR targeting the `dev` branch
2. Automated CI checks will run
3. If CI passes, core team members will review your code
4. Address any feedback and push updates
5. Once **2 core team members approve**, the PR can be merged

### What Reviewers Look For

- Code quality and adherence to guidelines
- Tests for new code
- Security considerations
- Performance implications
- Documentation updates if needed
- Cross-platform impact

### Response Times

- We aim to provide initial feedback within 3-5 business days
- Complex PRs may take longer to review
- Be patient and responsive to feedback

## Community

### Communication Channels

- **GitHub Issues** - For bug reports and feature requests
- **GitHub Discussions** - For questions and general discussions
- **Pull Requests** - For code contributions

### Getting Help

- Check existing issues and documentation first
- Provide context and details when asking questions
- Be patient and respectful when seeking help

### Recognition

We value all contributions! Contributors may be:

- Listed in project acknowledgments
- Mentioned in release notes for significant contributions

## Security

If you discover a security vulnerability, please **do NOT** open a public issue. Instead, please report it responsibly by contacting the maintainers directly.

## License

By contributing, you agree that your contributions will be licensed under the project [LICENSE](./LICENSE).

---

Thank you for contributing to PearPass! Your efforts help make password management more secure and accessible for everyone.
