# Cheat Sheet

This cheat sheet is made as a quick reference to read before the exam. 
I have tried to include sufficient information as bullets here to help understand how each service and function is different from the other and to serve as memory / logical points which can help you pick the right option / eliminate choices in the exam based on the described scenario in the questions.  

## 1. ☁️ STORAGE

### Blob Storage

#### Supports:
- Block Blob
- Append Blob
- Page Blob (used by unmanaged disks)

#### Stores **unstructured data**

 > Examples:

* Images
* Videos
* Documents
* Backups
* Logs

#### Storage tiers:

* Hot → frequent access
* Cool → infrequent
* Cold → long-term (if available)
* Archive → cheapest, highest retrieval latency

#### ✅ Exam Focus:
- Default storage for backups and application data
- Lifecycle Management only applies to Blob Storage
- Archive has the lowest cost but highest retrieval latency

---

### Azure Files

Fully managed SMB/NFS file shares.

#### Use when:

* Multiple VMs need shared files
* Replace Windows File Server
* Can sync on-prem using Azure File Sync

#### Mounted as:

```
\\storageaccount.file.core.windows.net\share
```

---

### Queue Storage

- Stores messages between applications.
- Maximum message size: 64 KB

#### Example:

App uploads image →
Queue stores message →
Worker VM processes image

Decouples applications.

---

### Table Storage

- NoSQL key-value database.

#### Uses:
- Partition Key
- Row Key

#### Good for:

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

- 3 copies
- Same datacenter 
- Cheapest

#### ✅ Exam Focus:
- Same datacenter but different racks
- Could be upgraded to ZRS, GRS, or G-ZRS

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
### Tabular Representation

| Type   | Copies | Region        | Read Secondary |
| ------ | ------ | ------------- | -------------- |
| LRS    | 3      | Same DataCentre | ❌           |
| ZRS    | 3      | Availability Zones | ❌        |
| GRS    | 6      | Paired Region | ❌             |
| G-ZRS  | 6      | 3 AZ Local + 3 in Paired | ❌  |
| RA-GRS | 6      | Paired Region | ✅             |


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

### Subnetting 

- 5 Addresses are unavailable in each Vnet/ Subnet

#### Example:

- /24 address gives 251 usable addresses.
- rest used by Azur


### NSG (Network Security Group)

#### Stateful Firewall for

* VM NIC
* Subnet

#### Rules

- Allow/Deny
- Inbound/Outbound

#### Priority

- Lower number = higher priority (100 is read first and approved, 4000 is overlooked)

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

#### ✅ Use when traffic must pass through:

- Firewall

- NVA

- VPN appliance

---

### Service Endpoint

Secure Azure service over Microsoft backbone.

Traffic stays inside Azure.

Storage account still has public endpoint.

Good but older solution.

#### ⚠️ Common Exam Confusion

Service Endpoint
✔ Public endpoint
✔ Traffic stays on Microsoft backbone

Private Endpoint
✔ Private IP inside your VNet
✔ No public endpoint exposure

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

- Encrypted tunnel
- Internet
- Connects

On-prem ↔ Azure 

or

VNet ↔ VNet

#### ✅ Common Exam Question-

- Site to Site - on prem Vnet to Cloud Vnet
- Point to Site - on prem endpoint to Cloud Vnet
- Traffic enters through Azure Backbone.

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

#### Supports:

- FQDN filtering

- Application rules

- Network rules

- DNAT

#### ✅ Choose When:

✔ Central firewall
✔ Many VNets
✔ Network inspection
✔ DNAT

---

### Bastion

-Secure browser based RDP/SSH.

-No Public IP required.

-Subnet Requirement /26 or higher

-Name: AzureBastionSubnet

-Access through Azure Portal

#### ✅ Very common exam answer

---

### Load Balancer

Layer 4

TCP/UDP

Balances traffic.

Internal

or

Public

No URL routing.

#### ✅Don't confuse:

Load Balancer
✔ Layer 4
✔ TCP/UDP

Application Gateway
✔ Layer 7
✔ HTTP/HTTPS
✔ URL Routing
✔ WAF

---

### Application Gateway

- Layer 7
- HTTP/HTTPS

#### Supports:

- SSL termination
- Cookie affinity
- URL routing
- WAF

#### ✅ Choose when:

✔ HTTP/HTTPS
✔ URL routing
✔ WAF
✔ SSL termination

---

### Traffic Manager

- DNS based.
- Routes users to different regions.

#### Methods:

- Priority
- Weighted
- Performance
- Geographic

#### ✅ Choose when:

✔ Multiple Azure regions
✔ DNS routing

---

### Front Door

- Global Layer 7.
- Entry point for web apps.

#### Supports:

- WAF
- SSL
- Caching
- Acceleration
- Global load balancing.

---
### Simple Comparison - Load Balancing

| Service             | Layer | Scope    |
| ------------------- | ----- | -------- |
| Load Balancer       | L4    | Regional |
| Application Gateway | L7    | Regional |
| Front Door          | L7    | Global   |
| Traffic Manager     | DNS   | Global   |


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
```
VM
↓
Access Storage
↓
No passwords.
```

#### ⚠️ Common exam question:

#### System Assigned -

• One identity per resource
• Deleted with resource (linked lifecycle)

#### User Assigned -

• Standalone identity
• Can be shared (one identity many resources and vice versa)

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

- Fault Domains - max 3  - unplanned downtime - disaster - failure.

- Update Domains - max 20 - planned downtime - updates - upgrades.

Protect against maintenance and hardware failure.

#### ✅ Common Question - 

- Update happens 1 domain at a time. 
- Resources are split evenly.

#### Example:

- 20 vms split as 5 each on 4 update domains.
- at a given time, max 5 VMs are down.

---

### Availability Zones

Separate datacenters.

Higher availability.

Recommended for production.

---

### Managed Disks

- Azure-managed virtual hard disks
- Azure manages storage.
- Recommended. (least amount of admin work)
- No storage account management.


#### ✅ Recommended by Microsoft

Benefits

- Simpler management
- Better scalability
- Higher availability

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

-Managed backup.
-Recovery Services Vault.

#### Supports

-VMs
-SQL
-Files
-Policies


### 🔑 Keywords:

- Recovery Services Vault
- Backup Policy
- Restore Point
- Vault
- Retention

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

#### Example:

- Only East US
- Require tags
- Require encryption

#### ✅ Exam Focus:

#### Can:

- Audit
- Deny
- Modify
- DeployIfNotExists

---

### Locks

#### Delete lock

- Cannot delete.
- Can modify.
- Can move in

#### Read-only

- Cannot modify.
- Cannot delete.
- Cannot move.

#### ✅ Exam favorite.

- Locks override RBAC permissions.
- Get inherited.
- Cannot be applied to Management groups.

---

### Tags

- Metadata.

#### Examples

- Environment=Prod
- Owner=IT
- Department=Finance

#### Useful for:

- Billing
- Automation
- Organization

#### ✅ Exam favorite.

- NOT inherited.
- Cannot be applied to Management groups.

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

Examples:

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

Recommendations only.

Does not automatically fix resources.

#### Five pillars:

- Cost

- Security

- Reliability

- Performance

- Operational Excellence

---

### Service Health

- Shows Azure outages.

- Planned maintenance.

- Health advisories.

- Personalized for YOUR resources.

---

## AZ-104 Decision Tree:

- Need authentication?
#### → Entra ID

- Need permissions?
#### → RBAC

- Need compliance?
#### → Policy

- Need protection?
#### → Locks

- Need VM scaling?
#### → VMSS

- Need backup?
#### → Recovery Services Vault

- Need DR?
#### → Site Recovery

- Need HTTP load balancing?
#### → Application Gateway

- Need TCP balancing?
#### → Load Balancer

- Need Global HTTP?
#### → Front Door

- Need Global DNS routing?
#### → Traffic Manager

- Need Private Azure service?
#### → Private Endpoint

- Need Azure backbone only?
#### → Service Endpoint

- Need storage lifecycle?
#### → Blob Storage

- Need SMB shares?
#### → Azure Files

- Need messaging?
#### → Queue

- Need NoSQL?
#### → Table


##  AZ-104 Memory Nuggets

* **RBAC** = Who
* **Policy** = What is allowed
* **Lock**s = Protect resources
* **NSG** = Filter traffic
* **ASG** = Group VMs
* **UDR** = Change routing
* **Service Endpoint** = Public endpoint over Azure backbone
* **Private Endpoint** = Private IP
* **Load Balancer** = L4
* **Application Gateway** = L7
* **Traffic Manager** = DNS routing
* **Front Door** = Global HTTP(S) entry point
* **VPN** = Internet
* **ExpressRoute** = Private circuit
* **Blob** = Objects
* **Files** = SMB/NFS shares
* **Queue** = Messages
* **Table** = NoSQL
* **VMSS** = Scale automatically
* **Availability Set** = Protect within one datacenter
* **Availability Zone** = Separate datacenters
* **Backup** = Recovery
* **Site Recovery** = Disaster recovery
* **Monitor** = Metrics + Logs
* **Advisor** = Recommendations
* **Service Health** = Azure outages

If you can explain each of these concepts in one or two sentences without looking at your notes, you're in a strong position for AZ-104.

