# Terraform Hetzner Cloud Modules

[![License: MPL-2.0](https://img.shields.io/badge/License-MPL--2.0-blue.svg)](https://opensource.org/licenses/MPL-2.0)
[![Terraform](https://img.shields.io/badge/Terraform-%3E%3D1.5.0-blueviolet)](https://www.terraform.io/)
[![OpenTofu](https://img.shields.io/badge/OpenTofu-Compatible-yellow)](https://opentofu.org/)

**Community-maintained Terraform modules for [Hetzner Cloud](https://www.hetzner.com/cloud).**

## About

This organization provides high-quality, well-tested Terraform modules for Hetzner Cloud infrastructure. All modules are:

- **Open Source** - Licensed under MPL-2.0
- **Well Tested** - CI/CD with Terraform, OpenTofu, and Terragrunt
- **Security Scanned** - Using tfsec, checkov, and gitleaks
- **HashiCorp Style** - Following official Terraform best practices

## Available Modules

| Module | Description | Registry |
|--------|-------------|----------|
| [terraform-module-template](https://github.com/terraform-hc-modules/terraform-module-template) | Template for creating new modules | - |

*More modules coming soon!*

## Quick Start

```hcl
module "server" {
  source  = "terraform-hc-modules/server/hcloud"
  version = "~> 1.0"

  name        = "web-server"
  server_type = "cx21"
  image       = "ubuntu-24.04"
}
```

## Contributing

We welcome contributions! Please see our [Contributing Guide](https://github.com/terraform-hc-modules/.github/blob/main/CONTRIBUTING.md) for details.

### Creating a New Module

1. Use the [terraform-module-template](https://github.com/terraform-hc-modules/terraform-module-template) as a GitHub template
2. Replace placeholders with your module details
3. Implement your module
4. Submit for review

## Resources

- [Hetzner Cloud](https://www.hetzner.com/cloud)
- [Hetzner Cloud Provider](https://registry.terraform.io/providers/hetznercloud/hcloud/latest/docs)
- [Terraform Documentation](https://developer.hashicorp.com/terraform)
- [OpenTofu Documentation](https://opentofu.org/docs)

## License

All modules in this organization are licensed under the [Mozilla Public License 2.0](https://opensource.org/licenses/MPL-2.0).
