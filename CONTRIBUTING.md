# Contributing to AI Coding Toolkit for Plaid

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to the project.

## Code of Conduct

Be respectful and constructive in all interactions. We are committed to providing a welcoming environment for all contributors.

## Getting Started

### Prerequisites
- Python 3.9 or higher
- pip or UV package manager
- Git

### Local Development Setup

1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/ai-coding-toolkit.git
   cd ai-coding-toolkit
   ```

3. Install development dependencies:
   ```bash
   pip install -e ".[dev]"
   ```

4. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## Development Workflow

### Before Submitting a PR

1. **Code Style**: Run formatters and linters
   ```bash
   black .
   ruff check --fix .
   ```

2. **Type Checking**: Run mypy
   ```bash
   mypy sandbox/
   ```

3. **Tests**: Ensure all tests pass
   ```bash
   pytest
   ```

4. **Commit Messages**: Use clear, descriptive commit messages
   ```
   fix: correct webhook simulation timeout
   feat: add support for new Plaid endpoint
   docs: update configuration examples
   ```

## Submitting Changes

1. Push to your fork
2. Create a Pull Request with:
   - Clear description of changes
   - Reference to related issues (if any)
   - Screenshot/video if UI-related
   - Tests for new functionality

3. Respond to review feedback promptly

## Reporting Issues

Please include:
- Clear title and description
- Steps to reproduce (if bug)
- Expected vs actual behavior
- Python version and environment details
- Relevant error messages or logs

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Questions?

Feel free to open an issue or discussion for questions about contributing.
