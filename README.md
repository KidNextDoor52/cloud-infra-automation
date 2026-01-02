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

Note: This deployment enforces VNet encapsulation by default; ensure your runner has private network access.


---

### **2. Automation: `cloud-infra-automation` (Infrastructure Deployment)**
Add this section to your `cloud-infra-automation` README. This demonstrates your **Security-By-Design** approach to automated governance.

```markdown
## 🛠️ Deployment Lifecycle (Terraform Workflow)

### 1. Initialization & Backend Setup
Infrastructure state is stored in an encrypted Azure Blob Storage container with state locking enabled for team collaboration.
```bash
terraform init -backend-config="storage_account_name=<STORAGE_ACCOUNT>"
