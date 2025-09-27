# Contributing to YieldForge Protocol

Thank you for your interest in contributing to YieldForge! We welcome contributions from the community to help improve and expand the protocol.

## Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct. We are committed to providing a welcoming and inclusive environment for all contributors.

## Getting Started

### Prerequisites

Before contributing, ensure you have:

- [Clarinet](https://github.com/hirosystems/clarinet) >= 2.0 installed
- [Node.js](https://nodejs.org/) >= 18
- Basic understanding of Clarity smart contract language
- Familiarity with Stacks blockchain concepts

### Development Setup

1. Fork the repository on GitHub
2. Clone your fork locally:

   ```bash
   git clone https://github.com/YOUR-USERNAME/yield-forge.git
   cd yield-forge
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Verify your setup:

   ```bash
   clarinet check
   npm test
   ```

## Contributing Guidelines

### Code Style

- **Clarity Formatting**: Use `clarinet fmt --in-place` to format all contract files
- **Comments**: Write clear, descriptive comments for all public functions
- **Naming**: Use descriptive function and variable names following Clarity conventions
- **Error Handling**: Define specific error constants for all failure cases

### Testing Requirements

All contributions must include appropriate tests:

- **Unit Tests**: Test individual functions in isolation
- **Integration Tests**: Test complete user workflows
- **Edge Cases**: Include tests for error conditions and boundary values
- **Coverage**: Maintain high test coverage for all new code

Run tests before submitting:

```bash
npm test
npm run test:report  # For coverage analysis
```

### Security Considerations

Given the financial nature of this protocol, security is paramount:

- **Input Validation**: Validate all parameters and user inputs
- **Authorization**: Ensure proper access controls for administrative functions
- **Integer Overflow**: Use safe arithmetic operations
- **External Calls**: Be cautious with external contract calls

### Documentation

- Update README.md if adding new features or changing existing functionality
- Add inline comments explaining complex logic
- Include usage examples for new public functions
- Update API documentation as needed

## Submission Process

### Pull Request Guidelines

1. **Branch Naming**: Use descriptive branch names:
   - `feature/add-compound-staking`
   - `fix/reward-calculation-bug`
   - `docs/update-api-examples`

2. **Commit Messages**: Write clear, descriptive commit messages:
   - Use imperative mood ("Add feature" not "Added feature")
   - Include context about why the change was made
   - Reference relevant issues when applicable

3. **Pull Request Description**:
   - Clearly describe the changes made
   - Include any breaking changes
   - Add screenshots for UI changes
   - List any new dependencies

### Code Review Process

1. All pull requests require review from maintainers
2. Ensure CI tests pass before requesting review
3. Address review feedback promptly
4. Keep pull requests focused and reasonably sized

### Deployment Checklist

Before merging to main:

- [ ] All tests pass
- [ ] Code has been reviewed
- [ ] Documentation is updated
- [ ] Security considerations addressed
- [ ] Breaking changes are documented

## Types of Contributions

### Bug Fixes

- Report bugs using GitHub Issues
- Include reproduction steps and expected behavior
- Submit fixes with appropriate tests

### Feature Enhancements

- Discuss major changes in GitHub Issues first
- Ensure new features align with protocol goals
- Include comprehensive tests and documentation

### Documentation Improvements

- Fix typos and clarify existing documentation
- Add examples and use cases
- Improve API documentation

### Testing

- Add missing test coverage
- Improve existing test quality
- Add performance benchmarks

## Security Reporting

For security vulnerabilities, please email: [security@yieldforge.io](mailto:security@yieldforge.io)

Do not create public issues for security vulnerabilities.

## Questions and Support

- **General Questions**: Open a GitHub Discussion
- **Bug Reports**: Create a GitHub Issue
- **Feature Requests**: Create a GitHub Issue with the "enhancement" label
- **Development Help**: Join our Discord channel

## Recognition

Contributors will be recognized in:

- Repository contributor list
- Release notes for significant contributions
- Special recognition for security improvements

## License

By contributing to YieldForge, you agree that your contributions will be licensed under the MIT License.

Thank you for contributing to YieldForge! 🚀
