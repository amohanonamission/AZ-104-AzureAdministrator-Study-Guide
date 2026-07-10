# **AZ-104 PRACTICE QUESTIONS**

This section contains a curated set of **100 practice questions** designed to simulate the style, scope, and difficulty of the **Azure Administrator Associate** exam.

These questions focus on:

- Concept clarity
- Mixture of scenario-based, PBQ-style, and recall that I used for my preparation.
- Understanding why an answer is correct (and why others are not)

The goal is not just memorization, but **reinforcing understanding**, which is key to passing Microsoft AZ-104 exam.

---

> Questions are formed with the help of ChatGPT. Once you go through these, you can paste these into a prompt and ask any LLM to generate more of them.

## Sample Prompts



---

## How to Use

- Attempt questions without looking at answers first  
- Review explanations carefully  
- Identify weak areas and revise those topics  
- Repeat until you can confidently recognize patterns  

**Answer key is at the end.**

Read slowly. Treat each one like an exam moment. Do deep research on any question you attempt wrongly. Pay attention to why each option is correct or incorrect.

---

### Identity & Governance (1–25)

```
Q1

You need to grant a user permission to manage virtual machines in a resource group without allowing access to other resource groups.

What should you assign?

A. Microsoft Entra role

B. Azure Policy

C. Azure RBAC role at the resource group scope

D. Management Group role

Q2

Which Azure RBAC role provides full management access to resources while allowing the user to assign roles to others?

A. Contributor

B. Reader

C. Owner

D. User Access Administrator

Q3

Which Azure RBAC role allows a user to manage access to Azure resources without allowing them to modify the resources themselves?

A. Owner

B. Reader

C. User Access Administrator

D. Contributor

Q4

A user needs permission to view all resources in a subscription but must not make any changes.

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

Q14

What is the primary purpose of Administrative Units?

A. Organize Azure subscriptions

B. Delegate administration for subsets of users and groups

C. Create resource groups

D. Manage storage accounts

Q15

Which Microsoft Entra group type supports assigning Azure RBAC roles?

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

Q25

A company wants to ensure that storage accounts can only be created in approved Azure regions.

Which Azure feature should be used?

A. Azure Monitor

B. Resource Locks

C. Azure Policy

D. Azure Backup
```

### Storage (26–50)


### Networking (51–75)


### Compute, Monitoring & Recovery (76–100)


---

## Answer Key

| Q | Ans | Q  | Ans | Q  | Ans |
| - | --- | -- | --- | -- | --- |
| 1 | C   | 10 | C   | 19 | B   |
| 2 | C   | 11 | B   | 20 | B   |
| 3 | C   | 12 | B   | 21 | B   |
| 4 | B   | 13 | B   | 22 | B   |
| 5 | C   | 14 | B   | 23 | B   |
| 6 | B   | 15 | C   | 24 | B   |
| 7 | C   | 16 | C   | 25 | C   |
| 8 | B   | 17 | C   |    |     |
| 9 | C   | 18 | C   |    |     |



Include:

Scenario-based questions
Multiple choice
Case studies
Answer key
Explanations
