<p align="center">
  <img width="1024" height="292" alt="Terraform Hetzner Modules Banner" src="https://clouddrove.s3.ca-central-1.amazonaws.com/Logo/hetzner.png" />
</p>

<h1 align="center">Terraform Hetzner Modules</h1>
<p align="center"><em>Reusable, cost-efficient, and production-ready Terraform modules for Hetzner Cloud.</em></p>

<p align="center">

![Provider](https://img.shields.io/badge/Provider-Hetzner%20Cloud-orange)
![Checkov](https://img.shields.io/badge/Security-Checkov-green)
[![License: MPL-2.0](https://img.shields.io/badge/License-MPL--2.0-blue.svg)](https://opensource.org/licenses/MPL-2.0)
[![Terraform](https://img.shields.io/badge/Terraform-%3E%3D1.10-blueviolet)](https://www.terraform.io/)
[![OpenTofu](https://img.shields.io/badge/OpenTofu-Compatible-yellow)](https://opentofu.org/)

</p>

---

## ⚡ What We Do
- **Infrastructure as Code (IaC):** Modular Terraform for Hetzner Cloud
- **Cost-Optimized:** Designed for Hetzner’s pricing advantage
- **Secure by Default:** Built-in security guardrails
- **Standardized:** Naming, tagging, and structure consistency
- **CI/CD Ready:** GitHub Actions & GitOps friendly

---

## 🏆 Highlights
- ✔️ Checkov validated modules  
- ✔️ Example usage in every module  
- ✔️ Lightweight & high-performance  
- ✔️ Community-driven  

---

## 🔁 CI/CD & Security

Every module runs these checks on each pull request:

- `terraform fmt` and `terraform validate` on the module and every example
- `terraform test` with offline plans
- tflint
- terraform-docs drift check on every README
- Checkov security scanning

Merged pull requests are tagged and released automatically from their `major`, `minor` or `patch` label.

---

### Available Modules

| Module | Description | Version |
|--------|-------------|---------|
| [terraform-hcloud-labels](https://github.com/terraform-hc-modules/terraform-hcloud-labels) | Naming and labeling utility | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-labels?label=) |
| [terraform-hcloud-network](https://github.com/terraform-hc-modules/terraform-hcloud-network) | Network, Subnets, Routes, Firewall, Firewall Attachment, Load Balancer | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-network?label=) |
| [terraform-hcloud-compute](https://github.com/terraform-hc-modules/terraform-hcloud-compute) | Server, Volume, Volume Attachment, Snapshot, SSH Key, Placement Group, rDNS | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-compute?label=) |
| [terraform-hcloud-ip](https://github.com/terraform-hc-modules/terraform-hcloud-ip) | Primary IP, Floating IP, rDNS | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-ip?label=) |
| [terraform-hcloud-certificate](https://github.com/terraform-hc-modules/terraform-hcloud-certificate) | SSL/TLS Certificates (Managed and Uploaded) | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-certificate?label=) |
| [terraform-hcloud-dns](https://github.com/terraform-hc-modules/terraform-hcloud-dns) | DNS Zones, Records and RRSets | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-dns?label=) |
| [terraform-hcloud-storage-box](https://github.com/terraform-hc-modules/terraform-hcloud-storage-box) | Storage Box, Subaccounts, Snapshots | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-storage-box?label=) |
| [terraform-hcloud-object-storage](https://github.com/terraform-hc-modules/terraform-hcloud-object-storage) | Object Storage buckets (S3 compatible, MinIO provider) | ![](https://img.shields.io/github/v/release/terraform-hc-modules/terraform-hcloud-object-storage?label=) |

---

## 👐 Open Source Ecosystem

| Platform        | Modules |
|----------------|--------|
| **AWS**        | https://github.com/clouddrove?q=terraform-aws |
| **GCP**        | https://github.com/clouddrove?q=terraform-gcp |
| **DigitalOcean** | https://github.com/terraform-do-modules |
| **Azure**    | https://github.com/terraform-az-modules |

---

## 📚 Blogs

👉 https://blog.clouddrove.com/  


