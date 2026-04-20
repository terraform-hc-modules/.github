# Security Policy

## Supported Versions

We release patches for security vulnerabilities in the following versions:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | :white_check_mark: |
| < Latest | :x:               |

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report them via GitHub's private vulnerability reporting feature:

1. Go to the repository's Security tab
2. Click "Report a vulnerability"
3. Fill out the form with details

### What to Include

- Type of issue (e.g., credential exposure, insecure defaults)
- Full paths of source file(s) related to the issue
- Location of the affected source code (tag/branch/commit or direct URL)
- Step-by-step instructions to reproduce the issue
- Proof-of-concept or exploit code (if possible)
- Impact of the issue

### Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 7 days
- **Resolution**: Depends on severity and complexity

## Security Best Practices

When using our modules:

1. **Never commit secrets** - Use environment variables or secret managers
2. **Pin versions** - Always specify module versions
3. **Review changes** - Check `terraform plan` output before applying
4. **Use remote state** - With encryption and access controls
5. **Enable logging** - For audit trails

## Security Scanning

All our modules are scanned with:

- [gitleaks](https://github.com/gitleaks/gitleaks) - Secret detection
- [tfsec](https://aquasecurity.github.io/tfsec/) - Security scanner
- [checkov](https://www.checkov.io/) - Policy-as-code

## Acknowledgments

We appreciate responsible disclosure and will acknowledge security researchers who help improve our modules.
