## ☁️ STORAGE

### Blob Storage

Stores **unstructured data**

Examples:

* Images
* Videos
* PDFs
* Backups
* VM diagnostics

Storage tiers:

* Hot → frequent access
* Cool → infrequent
* Cold → long-term (if available)
* Archive → cheapest, highest retrieval latency

---

### Azure Files

Fully managed SMB/NFS file shares.

Use when:

* Multiple VMs need shared files
* Replace Windows File Server
* Can sync on-prem using Azure File Sync

Mounted as:

```
\\storageaccount.file.core.windows.net\share
```

---

### Queue Storage

Stores messages between applications.

Example:

App uploads image →
Queue stores message →
Worker VM processes image

Decouples applications.

---

### Table Storage

NoSQL key-value database.

Good for:

* Large amounts of structured data
* Low cost
* Massive scale

NOT relational.

---

### Premium vs Standard Storage

#### Standard

HDD backed

✔ Cheap

✔ Most workloads

#### Premium

SSD backed

✔ High IOPS

✔ Low latency

Use for:

* Databases
* Production VMs
* Heavy workloads

---

### LRS (Locally Redundant Storage)

3 copies

Same datacenter

Cheapest

---

### ZRS (Zone Redundant)

3 copies

Across Availability Zones

Protects against datacenter failure.

---

### GRS (Geo-Redundant)

3 copies locally

*

3 copies in paired region

Protects regional outage.

Secondary NOT readable.

---

### RA-GRS

Same as GRS

BUT

Secondary region can be read.

(Read Access)

---

### SAS (Shared Access Signature)

Temporary access

No account keys shared.

Can limit:

✔ Time

✔ Permissions

✔ IP

✔ Protocol

Very common exam topic.

---

### Stored Access Policy

Stored on container/share.

Allows management of many SAS tokens.

Instead of changing each SAS individually,
change the Stored Access Policy.

---

### Lifecycle Management

Automatically move blobs:

Hot

↓

Cool

↓

Archive

↓

Delete

Used for cost optimization.

---

## 🌐 NETWORKING

### NSG (Network Security Group)

Firewall for

* VM NIC
* Subnet

Rules

Allow/Deny

Inbound/Outbound

Priority

Lower number = higher priority

---

### ASG (Application Security Group)

Groups VMs logically.

Instead of:

Allow VM1

Allow VM2

Allow VM3

Use:

Allow WebServers ASG

Much easier.

---

### UDR (User Defined Route)

Overrides Azure routing.

Use when traffic must pass through:

Firewall

NVA

VPN appliance

---

### Service Endpoint

Secure Azure service over Microsoft backbone.

Traffic stays inside Azure.

Storage account still has public endpoint.

Good but older solution.

---

### Private Endpoint

Private IP inside VNet.

Azure service completely private.

No public internet.

Preferred over Service Endpoints.

---

### VNet Peering

Connects two VNets.

High speed

Private

Microsoft backbone

No VPN required.

---

### VPN Gateway

Encrypted tunnel

Internet

Connects

On-prem ↔ Azure

or

VNet ↔ VNet

---

### ExpressRoute

Private dedicated connection.

NOT Internet.

Higher reliability.

Lower latency.

Enterprise solution.

---

### Azure Firewall

Managed Layer 3-7 firewall.

Centralized.

Supports:

FQDN filtering

Application rules

Network rules

DNAT

---

### Bastion

Secure RDP/SSH.

No Public IP required.

Access through Azure Portal.

Very common exam answer.

---

### Load Balancer

Layer 4

TCP/UDP

Balances traffic.

Internal

or

Public

No URL routing.

---

### Application Gateway

Layer 7

HTTP/HTTPS

Supports:

SSL termination

Cookie affinity

URL routing

WAF

---

### Traffic Manager

DNS based.

Routes users to different regions.

Methods:

Priority

Weighted

Performance

Geographic

---

### Front Door

Global Layer 7.

Entry point for web apps.

Supports

WAF

SSL

Caching

Acceleration

Global load balancing.

---

### NAT Gateway

Outbound internet.

Many private VMs

↓

One public IP

Does NOT accept inbound traffic.

---

## 🔐 IDENTITY

### RBAC

Role Based Access Control.

Who can do what.

Examples

Reader

Contributor

Owner

User Access Administrator

---

### PIM

Privileged Identity Management.

Just-in-time admin access.

User activates role only when needed.

Reduces standing privileges.

---

### Conditional Access

IF

User outside company

AND

Risk High

THEN

Require MFA

Very common.

---

### Microsoft Entra ID

Cloud identity service.

Authentication

Authorization

SSO

Groups

Applications

Devices

---

### Managed Identity

Azure automatically manages credentials.

VM

↓

Access Storage

↓

No passwords.

System Assigned

User Assigned

---

### Groups

Assign permissions once.

Users inherit permissions.

Security Group

Microsoft 365 Group

---

### Administrative Units

Delegate administration to part of organization.

Example

Delhi Admin

Only manages Delhi users.

---

### Hybrid Sync

Azure AD Connect.

Synchronizes

On-prem AD

↓

Entra ID

Changes should usually be made on-prem for synced objects.

---

## 💻 COMPUTE

### VM Scale Sets (VMSS)

Automatically scales VMs.

Load balanced.

Ideal for web apps.

---

### Availability Sets

Protect VMs inside one datacenter.

Fault Domains

Update Domains

Protect against maintenance and hardware failure.

---

### Availability Zones

Separate datacenters.

Higher availability.

Recommended for production.

---

### Managed Disks

Azure manages storage.

Recommended.

No storage account management.

---

### Extensions

Extra functionality for VMs.

Examples

Monitoring

Custom Script

Antimalware

DSC

---

### Custom Script Extension

Runs PowerShell/Bash after deployment.

Example

Install IIS

Download files

Configure VM

---

### Azure Backup

Managed backup.

Recovery Services Vault.

Supports

VMs

SQL

Files

Policies

---

### Azure Site Recovery

Disaster Recovery.

Replicates VMs

Failover

Failback

Business Continuity.

---

## 📋 GOVERNANCE

### Azure Policy

Enforces compliance.

Example

Only East US

Require tags

Require encryption

Can deny deployments.

---

### Locks

Delete lock

Cannot delete.

Can modify.

Read-only

Cannot modify.

Cannot delete.

Exam favorite.

---

### Tags

Metadata.

Examples

Environment=Prod

Owner=IT

Department=Finance

Useful for

Billing

Automation

Organization

---

### Management Groups

Above subscriptions.

Apply Policy/RBAC once.

Inherited by subscriptions.

---

### Resource Groups

Container for Azure resources.

Resources usually share:

Lifecycle

Permissions

Location

---

### Subscription Hierarchy

```
Management Group

↓

Subscription

↓

Resource Group

↓

Resource
```

RBAC and Policy inherit downward.

---

## 📊 MONITORING

### Azure Monitor

Main monitoring platform.

Collects

Metrics

Logs

Alerts

Insights

---

### Log Analytics

Stores logs.

Uses KQL.

Query data.

Usually connected to Monitor.

---

### Alerts

Notify when condition met.

Examples

CPU > 80%

VM stopped

Storage deleted

---

### Action Groups

What happens after alert?

Email

SMS

Webhook

Logic App

Automation Runbook

One Action Group

Many Alerts.

---

### Azure Advisor

Recommendations.

Five pillars

Cost

Security

Reliability

Performance

Operational Excellence

---

### Service Health

Shows Azure outages.

Planned maintenance.

Health advisories.

Personalized for YOUR resources.

---

## ⭐ Final AZ-104 Memory Nuggets

* **RBAC = Who**
* **Policy = What is allowed**
* **Locks = Protect resources**
* **NSG = Filter traffic**
* **ASG = Group VMs**
* **UDR = Change routing**
* **Service Endpoint = Public endpoint over Azure backbone**
* **Private Endpoint = Private IP**
* **Load Balancer = L4**
* **Application Gateway = L7**
* **Traffic Manager = DNS routing**
* **Front Door = Global HTTP(S) entry point**
* **VPN = Internet**
* **ExpressRoute = Private circuit**
* **Blob = Objects**
* **Files = SMB/NFS shares**
* **Queue = Messages**
* **Table = NoSQL**
* **VMSS = Scale automatically**
* **Availability Set = Protect within one datacenter**
* **Availability Zone = Separate datacenters**
* **Backup = Recovery**
* **Site Recovery = Disaster recovery**
* **Monitor = Metrics + Logs**
* **Advisor = Recommendations**
* **Service Health = Azure outages**

If you can explain each of these concepts in one or two sentences without looking at your notes, you're in a strong position for AZ-104.

