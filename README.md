# Cloud Infrastructure Automation (IaC)
> **Automating Secure Azure Landing Zones with Terraform**

## 🎯 Purpose
This repository contains the Infrastructure-as-Code (IaC) templates used to deploy hardened, compliant environments. It focuses on reducing "Blast Radius" through automated network and identity boundaries.

## 🛡️ Governance Features
* **Compliance Guardrails:** Automated deployment of Azure Policies to enforce "No Public IP" on sensitive resources.
* **Modular VNet Design:** Terraform modules for Hub-and-Spoke topology with integrated Azure Firewall and WAF configurations.
* **Least-Privilege IAM:** Automated Service Principal creation with scoped RBAC roles.

## 🚀 DevOps Workflow
* **CI/CD:** GitHub Actions for automated Plan/Apply cycles.
* **State Management:** Remote state stored in encrypted Azure Blob Storage with state locking.
