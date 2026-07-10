# **AZ-104 - PRACTICE QUESTIONS**

This section contains a curated set of **100 practice questions** designed to simulate the style, scope, and difficulty of the **Azure Administrator Associate** exam.

These questions focus on:

- Concept clarity
- Mixture of scenario-based, PBQ-style, and recall that I used for my preparation.
- Understanding why an answer is correct (and why others are not)

The goal is not just memorization, but **reinforcing understanding**, which is key to passing Microsoft AZ-104 exam.

>Note: I personally used such questions to quiz myself, however my main source of practice was the Udemy courses linked [here](../docs/Resources.md)
---

## How to Use

- Attempt questions without looking at answers first  
- Review explanations carefully  
- Identify weak areas and revise those topics  
- Repeat until you can confidently recognize patterns  

### ⚠️ Disclaimer

- Questions are formed with the help of ChatGPT. Once you go through these, you can paste these into a prompt and ask any LLM to generate more of them.
- These questions do not represent the real exam questions. However, I have tried to cover each topic to reinforce the knowledge to the best of my ability.
- In the real exam there will be a combination of these questions in a situation involving multiple domains. And you should expect multiple sub-questions for a given scenario.
- The best would be to get the exam series from Udemy mentioned [here](../docs/Resources.md)

---

**Answer key is at the end.**

Read slowly. Treat each one like an exam moment. Do deep research on any question you attempt wrongly. Pay attention to why each option is correct or incorrect.

---

### Section 1 - Identity & Governance (1–25)

```
(Q1.) You need to grant a user permission to manage virtual machines in a resource group without allowing access to other resource groups.

What should you assign?

A. Microsoft Entra role

B. Azure Policy

C. Azure RBAC role at the resource group scope

D. Management Group role


(Q2.) Which Azure RBAC role provides full management access to resources while allowing the user to assign roles to others?

A. Contributor

B. Reader

C. Owner

D. User Access Administrator


(Q3.) Which Azure RBAC role allows a user to manage access to Azure resources without allowing them to modify the resources themselves?

A. Owner

B. Reader

C. User Access Administrator

D. Contributor


(Q4.) A user needs permission to view all resources in a subscription but must not make any changes.

Which role should you assign?

A. Contributor

B. Reader

C. Owner

D. Virtual Machine Contributor

Q5

RBAC permissions assigned at a subscription are inherited by:

A. Only resource groups

B. Only resources

C. Resource groups and resources

D. Management groups only

Q6

Which identity type is automatically managed by Azure and can authenticate to Azure services without storing credentials?

A. Service Principal

B. Managed Identity

C. Guest User

D. Shared Access Signature

Q7

What are the two types of Managed Identities?

A. Public and Private

B. Local and Domain

C. System-assigned and User-assigned

D. Single and Multiple

Q8

A system-assigned managed identity is deleted when:

A. The subscription is deleted

B. The virtual machine is deleted

C. Microsoft Entra ID is disabled

D. The resource group is locked

Q9

Which Azure service stores user identities and authentication information?

A. Azure Monitor

B. Azure Firewall

C. Microsoft Entra ID

D. Azure Policy

Q10

Which Microsoft Entra feature enables users to sign in once and access multiple applications?

A. Multi-Factor Authentication

B. Conditional Access

C. Single Sign-On

D. Privileged Identity Management

Q11

Which feature evaluates conditions such as location, device compliance, and risk before granting access?

A. Azure Policy

B. Conditional Access

C. Resource Locks

D. Azure Monitor

Q12

Which authentication method provides an additional verification step beyond a password?

A. RBAC

B. MFA

C. Managed Identity

D. SSO

Q13

Which Microsoft Entra feature allows administrators to receive eligible permissions only when needed?

A. Azure Monitor

B. PIM

C. Azure Advisor

D. Azure Policy


(Q14) .What is the primary purpose of Administrative Units?

A. Organize Azure subscriptions

B. Delegate administration for subsets of users and groups

C. Create resource groups

D. Manage storage accounts


(Q15). Which Microsoft Entra group type supports assigning Azure RBAC roles?

A. Distribution Group only

B. Microsoft 365 Group only

C. Security Group

D. Mail-enabled Contact


Q16

A user account synchronized from on-premises Active Directory has an incorrect surname.

Where should you modify the attribute?

A. Azure Portal

B. Microsoft Entra Admin Center

C. On-premises Active Directory

D. Azure CLI

Q17

Which synchronization tool is commonly used to synchronize identities between Active Directory and Microsoft Entra ID?

A. Azure Backup

B. Azure Arc

C. Microsoft Entra Connect Sync

D. Azure Site Recovery

Q18

What is the highest level in the Azure resource hierarchy?

A. Subscription

B. Resource Group

C. Management Group

D. Resource

Q19

A Management Group can contain:

A. Resource Groups only

B. Subscriptions

C. Virtual Machines only

D. Storage Accounts

Q20

Which Azure construct is primarily used for organizing related resources?

A. Subscription

B. Resource Group

C. Availability Zone

D. Region

Q21

Azure Policy is primarily used to:

A. Assign permissions

B. Enforce organizational standards

C. Replicate storage

D. Monitor virtual machines

Q22

Which Azure feature prevents accidental deletion of resources?

A. Azure Policy

B. Resource Lock

C. Tags

D. Azure Advisor

Q23

Which Resource Lock prevents authorized users from deleting a resource while still allowing modifications?

A. ReadOnly

B. Delete

C. Contributor

D. Owner

Q24

Tags are primarily used for:

A. Authentication

B. Cost management and organization

C. Backup

D. Networking


(Q25). A company wants to ensure that storage accounts can only be created in specific Azure regions. (only East US and West Europe)

Which Azure feature should be used?

A. Azure Monitor

B. Resource Locks

C. Azure Policy

D. Azure Backup
```

### Section 2 - Storage (26–50)

```
Q26

You need to store millions of images and videos that will be accessed over HTTPS.

Which Azure storage service should you use?

A. Azure Files

B. Azure Queue Storage

C. Azure Blob Storage

D. Azure Table Storage

Q27

Which Azure storage service provides SMB file shares that can be mounted by Windows and Linux virtual machines?

A. Azure Blob Storage

B. Azure Files

C. Azure Queue Storage

D. Azure Table Storage

Q28

Which Azure storage service is designed to store large amounts of semi-structured NoSQL data?

A. Blob Storage

B. Azure Files

C. Azure Queue Storage

D. Azure Table Storage

Q29

Which Azure storage service is primarily used to decouple application components by storing messages?

A. Blob Storage

B. Queue Storage

C. Azure Files

D. Table Storage

Q30

Which storage redundancy option stores three copies of data within a single Azure datacenter?

A. ZRS

B. GRS

C. LRS

D. RA-GRS

Q31

Which redundancy option replicates data synchronously across multiple Availability Zones in the same region?

A. LRS

B. ZRS

C. GRS

D. RA-GRS

Q32

Which redundancy option provides asynchronous replication to a paired Azure region?

A. LRS

B. ZRS

C. GRS

D. Premium SSD

Q33

Which redundancy option provides read access to the secondary replicated region?

A. LRS

B. ZRS

C. RA-GRS

D. Locally Redundant Storage

Q34

Which storage access tier is intended for data accessed most frequently?

A. Archive

B. Cool

C. Hot

D. Premium

Q35

Which storage tier has the lowest storage cost but the highest retrieval latency?

A. Hot

B. Cool

C. Archive

D. Premium

Q36

A company wants blobs to automatically move to the Cool tier after 30 days and Archive after 180 days.

Which Azure feature should be used?

A. Azure Backup

B. Lifecycle Management

C. Azure Policy

D. Azure Monitor

Q37

You need to provide temporary access to specific blobs without exposing the storage account key.

What should you use?

A. Shared Access Signature (SAS)

B. Azure Policy

C. Resource Lock

D. Azure RBAC

Q38

What is the primary purpose of a Stored Access Policy?

A. Encrypt storage accounts

B. Provides centralized management of service SAS, including expiration and revocation

C. Replicate data

D. Configure storage redundancy


Q39

Which authentication method grants the highest level of access to a storage account?

A. SAS Token

B. Storage Account Key

C. Azure AD Group

D. Lifecycle Policy

Q40

Which Azure service can allow transfer of files over the public internet using AzCopy?

A. Azure Backup

B. Azure Files

C. Azure Storage

D. Azure Site Recovery

Q41

You need to migrate several terabytes of data over the internet as quickly as possible.

Which tool should you use?

A. Azure Storage Explorer

B. AzCopy

C. Azure Data Box

D. Azure Backup

Q42

Which Azure service is most appropriate for transferring petabytes of data when network bandwidth is limited?

A. AzCopy

B. Azure Files

C. Azure Data Box

D. Storage Explorer

Q43

Which storage account type supports Azure Blob, Azure Files, Queues, and Tables?

A. BlobStorage

B. FileStorage

C. StorageV2 (General-purpose v2)

D. Premium BlockBlobStorage

Q44

Premium storage is primarily recommended for workloads requiring:

A. Lowest storage cost

B. High IOPS and low latency

C. Archive storage

D. Long-term backup

Q45

A virtual machine uses managed disks.

Who manages the storage account for those disks?

A. Customer

B. Microsoft

C. Microsoft Entra ID

D. Azure Backup

Q46

Which Azure feature provides soft delete protection for Blob Storage?

A. Lifecycle Management

B. Blob Soft Delete

C. Azure Backup

D. Site Recovery

Q47

Which feature allows recovery of previous versions of a blob after it has been modified?

A. Blob Versioning

B. Archive Tier

C. Queue Storage

D. ZRS

Q48

You need to ensure deleted blobs can be recovered for 30 days.

Which feature should you enable?

A. Blob Soft Delete

B. Lifecycle Management

C. Azure Backup

D. Geo-replication

Q49

A company wants users to authenticate to Azure Storage using Microsoft Entra credentials instead of storage account keys whenever possible.

Which authorization method should be recommended?

A. Shared Key authorization

B. Microsoft Entra ID authentication with Azure RBAC

C. SAS Token only

D. Connection String authentication

Q50

A company needs to prevent accidental deletion of a storage account while still allowing administrators to modify its configuration.

Which feature should be used?

A. Read-only Lock

B. Delete Lock

C. Azure Policy

D. Lifecycle Management
```

### Section 3 - Networking (51–75)

```
Q51

You need to allow HTTP traffic from the internet to a virtual machine while blocking all other inbound traffic.

Which Azure resource should you configure?

A. Azure Firewall

B. Network Security Group (NSG)

C. Route Table

D. Traffic Manager

Q52

At which scope can a Network Security Group (NSG) be associated?

A. Resource Group only

B. Virtual Network only

C. Subnet and Network Interface

D. Subscription only

Q53

What is the primary purpose of an Application Security Group (ASG)?

A. Encrypt network traffic

B. Group virtual machines logically for NSG rules

C. Connect virtual networks

D. Provide internet access

Q54

You need to route all outbound internet traffic from a subnet through a network virtual appliance (NVA).

Which Azure feature should you configure?

A. NSG

B. User-Defined Route (UDR)

C. Application Gateway

D. Azure DNS

Q55

What is the primary purpose of a User-Defined Route (UDR)?

A. Filter traffic

B. Customize packet routing

C. Resolve DNS names

D. Encrypt traffic

(Q56). Which Azure feature allows Azure resources in a VNet to securely access an Azure PaaS service over the Azure backbone while the service continues to use its public endpoint?

A. Private Endpoint

B. Service Endpoint

C. VPN Gateway

D. Azure Bastion

Q57

Which Azure feature assigns a private IP address from your VNet to an Azure PaaS resource?

A. Service Endpoint

B. Private Endpoint

C. Azure Firewall

D. NAT Gateway

Q58

What is one advantage of a Private Endpoint over a Service Endpoint?

A. Lower storage costs

B. Private IP connectivity to the service

C. Automatic backups

D. Public internet access

Q59

You need to connect two Azure virtual networks with low latency over Microsoft's backbone network.

Which feature should you use?

A. VPN Gateway

B. VNet Peering

C. ExpressRoute

D. Azure Firewall

Q60

VNet Peering allows communication between:

A. Two VNets

B. Two Subnets only

C. Two Regions only

D. Two Resource Groups

Q61

Which Azure service provides encrypted connectivity between an on-premises network and Azure over the public internet?

A. ExpressRoute

B. VPN Gateway

C. Azure Bastion

D. NAT Gateway

Q62

Which Azure networking service provides a dedicated private connection from an on-premises datacenter to Azure?

A. VPN Gateway

B. ExpressRoute

C. VNet Peering

D. Service Endpoint

Q63

Which Azure service allows secure RDP and SSH access to virtual machines without exposing public IP addresses?

A. Azure Firewall

B. Azure Bastion

C. VPN Gateway

D. Traffic Manager

Q64

Azure Bastion requires deployment into which dedicated subnet?

A. AzureSubnet

B. BastionSubnet

C. AzureBastionSubnet

D. GatewaySubnet

Q65

Which Azure load balancing solution operates at Layer 4 (TCP/UDP)?

A. Azure Application Gateway

B. Azure Front Door

C. Azure Load Balancer

D. Traffic Manager

Q66

Which Azure service provides Layer 7 load balancing and Web Application Firewall (WAF) support?

A. Azure Firewall

B. Application Gateway

C. Azure Load Balancer

D. NAT Gateway

Q67

Which Azure networking service routes users to the closest endpoint based primarily on DNS routing methods?

A. Azure Front Door

B. Traffic Manager

C. Azure Firewall

D. VPN Gateway

Q68

Which Azure service provides global HTTP/HTTPS load balancing with application acceleration?

A. Azure Front Door

B. Traffic Manager

C. Azure Load Balancer

D. Application Gateway

Q69

What is the primary purpose of an Azure NAT Gateway?

A. Filter inbound traffic

B. Provide outbound internet connectivity for private resources

C. Route traffic between VNets

D. Host virtual machines

Q70

Which Azure networking component provides stateful network filtering across multiple virtual networks?

A. Azure Firewall

B. NSG

C. ASG

D. Route Table

(Q71). Which Azure service provides centralized, stateful network filtering for traffic between Azure virtual networks, on-premises networks, and the Internet?

A. NSG

B. Azure Firewall

C. Traffic Manager

D. Azure DNS

Q72

Which Azure DNS zone type allows name resolution only within Azure virtual networks?

A. Public DNS Zone

B. Private DNS Zone

C. Azure DNS Resolver

D. Route Table

Q73

A company wants virtual machines in one subnet to communicate with Azure SQL Database without traversing the public internet while keeping the SQL service on its public endpoint.

Which feature should be configured?

A. Private Endpoint

B. Service Endpoint

C. VPN Gateway

D. ExpressRoute

Q74

You need to ensure that inbound HTTPS traffic is inspected by a Web Application Firewall before reaching your web application.

Which Azure service should you deploy?

A. Azure Load Balancer

B. Azure Firewall

C. Application Gateway with WAF

D. Traffic Manager

Q75

A virtual machine in Azure requires outbound internet connectivity but should not have a public IP address.

Which Azure service is the best solution?

A. NAT Gateway

B. Azure Bastion

C. ExpressRoute

D. VPN Gateway
```

### Section 4 - Compute, Monitoring & Recovery (76–100)

```
Q76

Which Azure compute service automatically increases or decreases the number of virtual machines based on demand?

A. Availability Set

B. Virtual Machine Scale Set (VMSS)

C. Availability Zone

D. Azure Backup

Q77

What is the primary purpose of an Availability Set?

A. Backup VMs

B. Protect VMs from hardware and planned maintenance failures

C. Increase storage performance

D. Encrypt virtual machines

Q78

Availability Zones protect Azure resources against:

A. User errors

B. Datacenter failures within a region

C. Subscription deletion

D. Malware attacks

Q79

Which Azure disk type provides the highest performance for production workloads?

A. Standard HDD

B. Standard SSD

C. Premium SSD

D. Blob Storage

Q80

Which Azure feature allows you to automatically install software or configure a virtual machine after deployment?

A. Azure Policy

B. VM Extension

C. Azure Monitor

D. Azure Backup

Q81

Which VM extension is commonly used to execute PowerShell or Bash scripts after deployment?

A. Azure Monitor Agent

B. Custom Script Extension

C. Dependency Agent

D. DSC Extension

(Q82). You need to create scheduled backups of Azure virtual machines so they can be restored after accidental deletion or corruption.

Which service should you configure first?

A. Azure Site Recovery

B. Azure Backup

C. Azure Monitor

D. Log Analytics

Q83

Azure Backup stores recovery points inside a:

A. Recovery Services Vault

B. Storage Account

C. Resource Group

D. Managed Disk

Q84

Azure Site Recovery is primarily used for:

A. Monitoring

B. Disaster recovery

C. Identity synchronization

D. Cost optimization

Q85

Which Azure service continuously replicates virtual machines to another Azure region?

A. Azure Backup

B. Azure Site Recovery

C. Azure Monitor

D. Azure Advisor

Q86

Which Azure service collects metrics and logs from Azure resources?

A. Azure Advisor

B. Azure Monitor

C. Azure Policy

D. Azure Backup

Q87

Where are Azure Monitor logs typically stored for querying?

A. Blob Storage

B. Log Analytics Workspace

C. Azure SQL Database

D. Recovery Services Vault

Q88

Which Kusto Query Language (KQL)-enabled service allows you to analyze Azure logs?

A. Azure Monitor

B. Log Analytics

C. Service Health

D. Advisor

Q89

Which Azure feature sends notifications when specific conditions are met?

A. Azure Advisor

B. Alerts

C. Tags

D. Azure Firewall

Q90

What is an Action Group used for?

A. Group virtual machines

B. Define notification actions for alerts

C. Assign RBAC permissions

D. Create Resource Groups

Q91

Which Azure service provides personalized recommendations to improve performance, reliability, security, and cost?

A. Service Health

B. Azure Advisor

C. Azure Policy

D. Azure Backup

Q92

Which Azure service informs you about outages affecting Azure services in your region?

A. Azure Monitor

B. Azure Advisor

C. Service Health

D. Log Analytics

Q93

Which Azure service helps monitor the health and performance of applications?

A. Azure Backup

B. Application Insights

C. Azure Firewall

D. Recovery Services Vault

Q94

A virtual machine unexpectedly becomes unavailable because the physical host fails.

Which Azure feature minimizes downtime in this scenario?

A. Availability Set

B. Azure Backup

C. Resource Lock

D. Azure Policy

Q95

Which feature distributes virtual machines across separate physical datacenters within a region?

A. Availability Zones

B. Availability Sets

C. VM Extensions

D. Resource Groups

Q96

Which Azure monitoring data type records numerical performance values over time?

A. Logs

B. Metrics

C. Alerts

D. Events

Q97

Which Azure service should you use to restore a deleted Azure virtual machine?

A. Azure Site Recovery

B. Azure Backup

C. Azure Monitor

D. Azure Advisor

Q98

You need to receive an email whenever CPU utilization exceeds 80% on a virtual machine.

What should you configure?

A. Azure Advisor

B. Azure Monitor Alert with an Action Group

C. Azure Policy

D. Service Health

Q99

Which Azure service allows disaster recovery from an on-premises VMware environment to Azure?

A. Azure Backup

B. Azure Site Recovery

C. Azure Files

D. Azure Monitor

Q100

A company wants both automated backups and the ability to fail over workloads to another Azure region.

Which two Azure services should be implemented?

A. Azure Monitor + Advisor

B. Azure Backup + Azure Site Recovery

C. Azure Policy + Azure Monitor

D. VM Extensions + Availability Sets
```

---

## Answer Key

### Section 1 - Identity & Governance (1–25)

| Q | Ans | Q  | Ans | Q  | Ans |
| - | --- | -- | --- | -- | --- |
| **1** | C   | **10** | C   | **19** | B   |
| **2** | C   | **11** | B   | **20** | B   |
| **3** | C   | **12** | B   | **21** | B   |
| **4** | B   | **13** | B   | **22** | B   |
| **5** | C   | **14** | B   | **23** | B   |
| **6** | B   | **15** | C   | **24** | B   |
| **7** | C   | **16** | C   | **25** | C   |
| **8** | B   | **17** | C   |    |     |
| **9** | C   | **18** | C   |    |     |

### Section 2 - Storage (26–50)

| Q  | Ans | Q  | Ans | Q  | Ans |
| -- | --- | -- | --- | -- | --- |
| **26** | C   | **35** | C   | **44** | B   |
| **27** | B   | **36** | B   | **45** | B   |
| **28** | D   | **37** | A   | **46** | B   |
| **29** | B   | **38** | B   | **47** | A   |
| **30** | C   | **39** | B   | **48** | A   |
| **31** | B   | **40** | C   | **49** | B   |
| **32** | C   | **41** | B   | **50** | B   |
| **33** | C   | **42** | C   |    |     |
| **34** | C   | **43** | C   |    |     |


### Section 3 - Networking (51–75)

| Q  | Ans | Q  | Ans | Q  | Ans |
| -- | --- | -- | --- | -- | --- |
| **51** | B   | **60** | A   | **69** | B   |
| **52** | C   | **61** | B   | **70** | A   |
| **53** | B   | **62** | B   | **71** | B   |
| **54** | B   | **63** | B   | **72** | B   |
| **55** | B   | **64** | C   | **73** | B   |
| **56** | B   | **65** | C   | **74** | C   |
| **57** | B   | **66** | B   | **75** | A   |
| **58** | B   | **67** | B   |    |     |
| **59** | B   | **68** | A   |    |     |


### Section 4 - Compute, Monitoring & Recovery (76–100)



| Q  | Ans | Q  | Ans | Q  | Ans | Q  | Ans |
| -- | --- | -- | --- | -- | --- | -- | --- |
| **76** | B   | **82** | B   | **88** | B   | **94** | A   |
| **77** | B   | **83** | A   | **89** | B   | **95** | A   |
| **78** | B   | **84** | B   | **90** | B   | **96** | B   |
| **79** | C   | **85** | B   | **91** | B   | **97** | B   |
| **80** | B   | **86** | B   | **92** | C   | **98** | B   |
| **81** | B   | **87** | B   | **93** | B   | **99** | B   |
|    |     |    |     |    |     |  **100**  | B |


---


## Future Work and Improvements - 

I would intentionally make the questions slightly harder than average.

Right now these are around 6.5–7/10 difficulty.

The real AZ-104 has many scenario-based questions like:

Your company has three subscriptions...

You need to minimize administrative effort...

Which two actions should you perform?

Those force candidates to think instead of simply recalling facts.

My recommendation for the remaining 75 questions is:

30% straightforward knowledge checks (like the ones above).
70% scenario-based questions modeled after the actual exam.

That mix will make your repository stand out because it will prepare people for the style of the real exam, not just the content.


--- 

Things I'd add

Your Storage section is already good.

But the real AZ-104 asks about these topics surprisingly often.

I'd include one or two of these.

Storage Explorer

Example

Which tool provides a graphical interface to upload and manage Azure Storage?

Azure Storage Explorer

Immutable Blob Storage

Example

Which feature prevents blobs from being modified or deleted for a specified retention period?

Immutable Storage

File Sync

Example

Which service synchronizes Azure Files with on-premises Windows Servers?

Azure File Sync

Very common.

Premium File Shares

They like asking

Premium File Share

vs

Standard File Share

Managed Disk Types

Standard HDD

Standard SSD

Premium SSD

Ultra Disk

These appear on AZ-104 more often than people expect.

---

If you ever expand this to 150–200 questions, I'd include these networking topics because they appear in AZ-104 more often than many people realize:

Azure DNS

Forward lookup zones

Reverse lookup

Alias records

Private DNS linking

Effective Security Rules

Microsoft loves asking:

Which NSG rule is actually applied?

Effective Routes

Very common.

Given

System Route

UDR

BGP

Which route wins?

Route Priority

Longest Prefix Match

User Defined

BGP

System

This catches many candidates.

Accelerated Networking

Appears occasionally.

IP Addressing

Static

Dynamic

Reserved IPs

Private/Public

Gateway Transit

Used with VNet Peering.

Surprisingly common.

---

Things I'd Add (Optional)

If you ever expand this repository to 150–200 questions, I'd include more questions on:

Managed Disks
Disk encryption
Snapshots
Disk types
Shared disks
Azure Compute Gallery

Formerly Shared Image Gallery.

Frequently appears.

Run Command

Microsoft likes asking:

Run Command

vs

Custom Script Extension

Boot Diagnostics

Surprisingly common.

Serial Console

VM troubleshooting.

Resource Health

Different from Service Health.

Common confusion.

Azure Monitor Agent (AMA)

Replacing Log Analytics Agent.

Recovery Services Vault vs Backup Vault

Worth one question if updating for newer Azure features.
