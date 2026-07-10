
# Home Labs (AZ-104)

These are the hands-on labs I recommend completing while studying for AZ-104.

> The goal isn't to memorize Azure services—it's to build them, configure them, break them, and understand how they work together. 

---
## What to expect

These labs are designed to reinforce the concepts covered in AZ-104 through hands-on experience.

More importantly, they'll help you start thinking like an Azure Administrator—not just someone preparing for an exam.

| Difficulty | Lab                             |
| ---------- | ------------------------------- |
| ⭐          | Users, Groups, RBAC             |
| ⭐          | Storage Account                 |
| ⭐⭐         | Virtual Machines                |
| ⭐⭐         | NSGs                            |
| ⭐⭐⭐        | Private Endpoint                |
| ⭐⭐⭐        | Azure Backup                    |
| ⭐⭐⭐⭐       | Load Balancer                   |
| ⭐⭐⭐⭐       | Azure Monitor                   |
| ⭐⭐⭐⭐⭐      | Complete Production Environment |

---

## Identity

### Lab 1 — Create Users and Groups

**Objectives:**

- Create Microsoft Entra users
- Create Security Groups
- Assign users to groups
- Explore Microsoft 365 Groups

**Concepts:**

- Entra ID
- Groups
- Identity Management

---

### Lab 2 — RBAC

**Objectives:**

- Create a Resource Group
- Assign Reader
- Assign Contributor
- Remove assignments
- Verify inherited permissions

**Concepts:**

- RBAC
- Scope
- Least Privilege

---

## Compute

### Lab 3 — Deploy a Virtual Machine

**Objectives:**

- Deploy Windows/Linux VM
- Connect using Bastion or RDP
- Stop
- Start
- Resize
- Restart
- Redeploy
- Delete

**Concepts:**

- VM
- Managed Disks
- Public IP
- NIC

---

### Lab 4 — VM Extensions

**Objectives:**

- Install Custom Script Extension
- Install Monitoring Agent

**Concepts:**

- VM Extensions
- Automation

---

### Lab 5 — Azure Backup

**Objectives:**

- Create Recovery Services Vault
- Configure Backup
- Trigger Backup
- Restore VM

**Concepts:**

- Backup
- Recovery
- Vaults

---

## Storage

### Lab 6 — Storage Accounts

**Create:**

- Standard Storage
- Blob Container
- File Share
- Queue
- Table
- Configure Lifecycle Management

**Explore:**

- Access Keys
- SAS
- Lifecycle Management
- Replication Options

---

### Lab 7 — Azure Files

**Objectives:**

- Create File Share
- Mount on Windows VM
- Upload files

---

## Networking

### Lab 8 — Virtual Networking

**Create:**

- VNet
- Multiple Subnets
- NSGs
- Create Route Table (UDR)
- Associate NSGs with subnets and NICs

**Experiment with:**

- Allow Rules
- Deny Rules
- Priorities

---

### Lab 9 — Private Endpoint

**Objectives:**

- Create Storage Account
- Configure Private Endpoint
- Disable Public Access
- Verify connectivity
- Compare Private Endpoint with Service Endpoint

---

### Lab 10 — Load Balancer

**Objectives:**

- Deploy two VMs
- Create Load Balancer
- Configure Health Probe
- Configure Load Balancing Rule

---

## Governance

### Lab 11 — Azure Policy

**Create policies that:**

- Require Tags
- Restrict Regions
- Restrict VM SKUs

Observe what happens during deployment.

---

### Lab 12 — Resource Locks

**Create:**

- Delete Lock
- Read-only Lock

**Attempt:**

- Delete Resource
- Modify Resource

Observe the behavior.

---

## Monitoring

### Lab 13 — Azure Monitor

**Objectives:**

- View Metrics
- Explore Activity Log
- Create an Alert Rule
- Create an Action Group

---

### Lab 14 — Log Analytics

**Objectives:**

- Create Workspace
- Connect VM
- Run KQL Queries

---

## Bonus Challenge

**Final Challenge — Build a Small Production Environment**

- Resource Group
- Virtual Network
- Subnets
- NSGs
- Two Web VMs
- Azure Load Balancer
- Storage Account
- Recovery Services Vault
- Azure Monitor
- RBAC Assignments

This single lab touches most of the major AZ-104 objectives.

**Double Bonus**: Recreate the same environment using Infrastructure as Code (Bicep or ARM Templates).

Organizations deploy Azure resources through IaC rather than manually through the portal, and basic Bicep concepts may also appear on the AZ-104 exam.

---

### My Recommendation

- Don't just deploy resources once.

- Repeat the process until you can build them from memory.

- Deploy → Configure → Test → Break → Delete → Rebuild.

- That's where the learning happens.

## Final Thoughts

The Azure Portal is one of your best teachers.

The more comfortable you become navigating Azure, the easier both the exam and real-world administration will feel.

> No amount of reading can supplement actual hands on practice. Reading builds knowledge. Hands-on practice builds confidence.
