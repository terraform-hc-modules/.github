<img src="https://raw.githubusercontent.com/hetznercloud/hcloud-cloud-controller-manager/main/.github/images/hetzner-cloud-logo.svg" width="80" align="left" alt="Hetzner Cloud">

## Terraform Hetzner Cloud Modules

Unofficial community maintained Terraform modules for Hetzner Cloud

---

[![License: MPL-2.0](https://img.shields.io/badge/License-MPL--2.0-blue.svg)](https://opensource.org/licenses/MPL-2.0)
[![Terraform](https://img.shields.io/badge/Terraform-%3E%3D1.0-blueviolet)](https://www.terraform.io/)
[![OpenTofu](https://img.shields.io/badge/OpenTofu-Compatible-yellow)](https://opentofu.org/)

### Available Modules

| Module | Description | Version |
|--------|-------------|---------|
| [terraform-hcloud-labels](https://github.com/terraform-hc-modules/terraform-hcloud-labels) | Naming and labeling utility | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-labels?label=) |
| [terraform-hcloud-network](https://github.com/terraform-hc-modules/terraform-hcloud-network) | VPC, Firewall, Load Balancer | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-network?label=) |
| [terraform-hcloud-compute](https://github.com/terraform-hc-modules/terraform-hcloud-compute) | Server, Volume, SSH Key, Placement Group | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-compute?label=) |
| [terraform-hcloud-ip](https://github.com/terraform-hc-modules/terraform-hcloud-ip) | Primary IP, Floating IP, rDNS | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-ip?label=) |
| [terraform-hcloud-certificate](https://github.com/terraform-hc-modules/terraform-hcloud-certificate) | SSL/TLS Certificates (Managed & Uploaded) | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-certificate?label=) |
| [terraform-hcloud-dns](https://github.com/terraform-hc-modules/terraform-hcloud-dns) | DNS Zones and Records | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-dns?label=) |
| [terraform-hcloud-storage-box](https://github.com/terraform-hc-modules/terraform-hcloud-storage-box) | Storage Box (Beta) | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-storage-box?label=&include_prereleases) |

### Quick Start

```hcl
module "network" {
  source  = "terraform-hc-modules/network/hcloud"
  version = "0.1.0"

  name     = "my-vpc"
  ip_range = "10.0.0.0/16"

  subnets = [{
    ip_range     = "10.0.1.0/24"
    network_zone = "eu-central"
  }]
}

module "compute" {
  source  = "terraform-hc-modules/compute/hcloud"
  version = "0.1.0"

  name        = "my-server"
  server_type = "cx22"
  image       = "ubuntu-24.04"
  location    = "fsn1"
}
```

### Contributing

We welcome contributions! See our [Contributing Guide](https://github.com/terraform-hc-modules/.github/blob/main/CONTRIBUTING.md).

### Resources

- [Hetzner Cloud Provider Docs](https://registry.terraform.io/providers/hetznercloud/hcloud/latest/docs)
- [Hetzner Cloud API](https://docs.hetzner.cloud/)
