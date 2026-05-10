# Security Policy

## Supported Versions

Currently supported versions of the Movie Recommender System:

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | ✅ Yes             |
| < 1.0   | ❌ No              |

## Reporting a Vulnerability

**DO NOT** create public issues/pull requests for security vulnerabilities. Instead, please report security vulnerabilities responsibly through GitHub's private vulnerability reporting.

### How to Report

1. Visit the repository's Security tab
2. Click "Report a vulnerability"
3. Complete the vulnerability report form with:
   - **Vulnerability Title**: Clear, descriptive title
   - **Vulnerability Description**: Detailed explanation of the vulnerability
   - **Severity**: Critical, High, Medium, Low
   - **Affected Component**: Which part of the system is affected
   - **Steps to Reproduce**: How to reproduce the vulnerability
   - **Proof of Concept**: Code or example demonstrating the issue
   - **Impact**: Potential impact of the vulnerability
   - **Proposed Fix**: Your suggested fix (if available)

### Response Timeline

- **Acknowledgment**: Within 48 hours
- **Initial Assessment**: Within 1 week
- **Fix Development**: Depends on severity
- **Public Disclosure**: After patch release

### Severity Levels

- **Critical**: Remote code execution, authentication bypass, data breach
- **High**: Unauthorized access, significant data exposure
- **Medium**: Denial of service, privilege escalation
- **Low**: Information disclosure, minor bypass

## Security Best Practices

### For Users

- Keep your Python environment up to date
- Update dependencies regularly: `pip install --upgrade -r requirements.txt`
- Never hardcode sensitive information (API keys, passwords)
- Use environment variables for configuration
- Review code before installation

### For Developers

- Always run security checks: `bandit -r src/`
- Use `safety` to check dependencies: `safety check`
- Keep dependencies updated
- Follow OWASP guidelines
- Review security advisories for dependencies
- Use type hints for better code security

## Dependency Management

### Checking for Vulnerabilities

```bash
# Install safety
pip install safety

# Check for known vulnerabilities
safety check --file requirements.txt
```

### Updating Dependencies Safely

```bash
# Check for updates
pip list --outdated

# Update specific package
pip install --upgrade package-name

# Verify functionality after updates
pytest tests/
```

## Secure Coding Guidelines

1. **Input Validation**: Validate all user inputs
2. **Error Handling**: Don't expose sensitive information in errors
3. **Logging**: Don't log sensitive data
4. **Dependencies**: Use well-maintained packages
5. **Testing**: Write security-focused tests
6. **Code Review**: All changes should be reviewed

## Contact

For security concerns not covered by this policy, contact the project maintainers:

- Open a private security advisory through GitHub
- Maintainers will respond within 48 hours

## Acknowledgments

We appreciate security researchers who responsibly disclose vulnerabilities to us.

---

**Last Updated**: May 10, 2026
