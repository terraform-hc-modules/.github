# Contributing to Terraform Hetzner Cloud Modules

Thank you for your interest in contributing! This document provides guidelines for contributing to any module in the terraform-hc-modules organization.

## Code of Conduct

By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md).

## How to Contribute

### Reporting Bugs

1. Check existing issues to avoid duplicates
2. Use the bug report template
3. Include Terraform/OpenTofu version
4. Provide minimal reproduction steps

### Suggesting Features

1. Open an issue with the feature request template
2. Describe the use case
3. Explain why it benefits the community

### Pull Requests

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/my-feature`
3. Make your changes following our style guide
4. Run all validations locally
5. Commit with conventional commits: `feat:`, `fix:`, `docs:`, etc.
6. Push and open a pull request

## Development Setup

### Prerequisites

- [Terraform](https://www.terraform.io/downloads) >= 1.5.0
- [TFLint](https://github.com/terraform-linters/tflint)
- [terraform-docs](https://terraform-docs.io/)
- [tfsec](https://aquasecurity.github.io/tfsec/)
- [checkov](https://www.checkov.io/)
- [gitleaks](https://github.com/gitleaks/gitleaks)

### Running Validations

```bash
# Format code
make fmt

# Validate configuration
make validate

# Run security scans
make security

# Generate documentation
make docs
```

## Style Guide

We follow the [HashiCorp Terraform Style Guide](https://developer.hashicorp.com/terraform/language/style):

### File Organization

| File | Purpose |
|------|---------|
| `terraform.tf` | Version constraints |
| `main.tf` | Primary resources |
| `variables.tf` | Input variables (alphabetical) |
| `outputs.tf` | Outputs (alphabetical) |

### Naming

- Use lowercase with underscores
- Use descriptive nouns
- Default to `main` for single resources

### Variables

- Always include `type` and `description`
- Add `validation` blocks where appropriate
- Use `sensitive = true` for secrets

### Outputs

- Always include `description`
- Use `sensitive = true` for sensitive values

## Testing

Before submitting a PR:

```bash
# All checks must pass
terraform fmt -check -recursive
terraform init -backend=false
terraform validate
tflint -f compact
tfsec . --minimum-severity MEDIUM
checkov -d . --quiet
```

## Documentation

- Update README.md with terraform-docs
- Include usage examples
- Document all variables and outputs

## Commit Messages

Use [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` - New feature
- `fix:` - Bug fix
- `docs:` - Documentation only
- `chore:` - Maintenance
- `refactor:` - Code refactoring
- `test:` - Adding tests

## Release Process

Releases are automated via GitHub Actions when tags are pushed:

```bash
git tag v1.0.0
git push origin v1.0.0
```

## Questions?

Open a discussion or issue in the relevant repository.

Thank you for contributing!
