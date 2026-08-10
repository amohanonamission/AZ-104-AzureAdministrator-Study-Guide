# AZ-104 Exam Tips & Lessons Learned

> The advice I wish someone had given me before taking the AZ-104 exam.

These are the lessons I learned while preparing for and taking the **Microsoft Azure Administrator Associate (AZ-104)** exam.

The goal isn't to memorize hundreds of Azure services. It's to develop enough understanding and Azure-specific reasoning to choose the right solution when Microsoft gives you a real-world scenario.

---

## 1. Understand — Don't Memorize

AZ-104 covers a huge amount of material.

You will not remember every setting, SKU, command, or service.

Instead, understand:

* Why a service exists
* What problem it solves
* When you would use it
* When you would **not** use it
* How it compares with similar services
* How it interacts with other Azure services

For every service, ask:

> **What problem does this solve?**

> **When would I recommend it?**

> **Why wouldn't I use the alternatives?**

---

## 2. Think Like an Azure Administrator

Many AZ-104 questions aren't simply testing whether you recognize a service.

They're testing whether you can make the **best administrative decision**.

Think about:

* Security
* Cost
* Availability
* Scalability
* Performance
* Administrative effort
* Business requirements
* Existing infrastructure

Don't just ask:

> "Can this solution work?"

Ask:

> "Is this the best solution for the requirements?"

---

## 3. Learn Azure's Vocabulary

AZ-104 is broad.

One of the biggest challenges is becoming comfortable with Azure terminology.

You should eventually be able to immediately recognize concepts such as:

* NSG
* ASG
* RBAC
* Azure Policy
* Managed Identity
* Private Endpoint
* VNet Peering
* VM Scale Sets
* Recovery Services Vault
* Application Gateway
* Azure Front Door
* Azure Monitor
* Log Analytics

Once the vocabulary becomes familiar, questions become much easier to reason through.

---

## 4. Build Mental Connections

Don't study every Azure service in isolation.

Understand how services work together.

For example:

```text
User
  ↓
Front Door / Application Gateway
  ↓
Load Balancer
  ↓
VM / VMSS
  ↓
Storage
  ↓
Azure Monitor
```

Then think about the security and governance around that architecture:

```text
Microsoft Entra ID
        ↓
       RBAC
        ↓
Azure Policy + Locks
        ↓
Azure Resources
```

The more connections you make, the easier unfamiliar scenarios become.

---

## 5. Spend Time in the Azure Portal

Hands-on experience makes the concepts stick.

Deploy resources yourself.

Try things.

Break things.

Fix them.

Delete them.

Build them again.

Useful resources to practice include:

* Virtual Machines
* Storage Accounts
* VNets
* Subnets
* NSGs
* Private Endpoints
* RBAC
* Azure Policy
* Azure Monitor
* Azure Backup

A useful cycle is:

> **Deploy → Configure → Test → Break → Fix → Delete → Rebuild**

---

## 6. Practice Exams Are for Learning

Don't use practice exams only to measure your score.

Use them to discover what you don't understand.

For every incorrect answer, ask:

1. Why was my answer wrong?
2. Why is the correct answer correct?
3. Why are the other options wrong?
4. What concept is Microsoft actually testing?
5. Could the same concept appear in a different scenario?

This is where a large amount of exam preparation happens.

---

## 7. Don't Ignore Questions You Got Right

Getting the correct answer isn't always evidence that you understand the concept.

If you guessed correctly, review it.

If you knew the answer but couldn't explain why the other options were wrong, review it.

Your goal should be:

> **"I understand why this is correct."**

Not:

> **"I happened to select the correct option."**

---

## 8. Microsoft Learn Is Your Best Friend

Practice exams are useful, but don't treat their explanations as the final authority.

When something doesn't make sense:

* Search Microsoft Learn
* Read the relevant documentation
* Check Microsoft's terminology
* Understand the service
* Return to the question

Use practice questions to **find gaps**.

Use Microsoft Learn to **close them**.

---

## 9. Watch for the Actual Requirement

Many questions contain a lot of information that isn't equally important.

Before choosing an answer, identify:

* What is actually being requested?
* What constraints exist?
* What is the priority?
* What must be avoided?
* What does the question explicitly require?

Pay particular attention to phrases such as:

* Lowest cost
* Least administrative effort
* Most secure
* Highest availability
* Minimize downtime
* Least privilege
* Automatically scale
* Azure-native
* No public internet access
* Minimize management overhead

These aren't automatic answer keys, but they can dramatically narrow your choices.

---

## 10. Read the Question Carefully

One strategy that helped me was reading the **final sentence first** when a question contained a long scenario.

This can help you understand what you're actually being asked before processing all the details.

For example:

> "Which solution should you recommend?"

Then read the scenario looking specifically for the requirements that determine that recommendation.

Don't blindly apply this to every question, though. If the scenario is short, simply read it normally.

---

## 11. Eliminate Before You Choose

You don't always need to immediately know the answer.

Sometimes you can eliminate three wrong answers.

Ask:

* Does this actually satisfy the requirement?
* Is this service designed for this use case?
* Does it introduce unnecessary administration?
* Does it violate a security requirement?
* Is it solving a different problem?

Then choose from the remaining options.

---

## 12. If Two Answers Look Correct

This is where many scenario questions become difficult.

If two options technically work, compare them against **all** the requirements.

Ask:

* Which requires less administration?
* Which is more secure?
* Which is more appropriate for the stated architecture?
* Which better satisfies the business requirement?
* Which avoids unnecessary components?
* Which is the Azure service designed specifically for this scenario?

The answer isn't necessarily the most sophisticated solution.

It's the one that best satisfies the question.

---

## 13. Know the Common Comparisons

Be able to explain these without looking at your notes:

### Identity & Governance

* RBAC vs Azure Policy
* Azure Policy vs Resource Locks
* RBAC vs Managed Identity
* PIM vs permanent role assignment

### Networking

* Service Endpoint vs Private Endpoint
* VPN Gateway vs ExpressRoute
* NSG vs Azure Firewall
* Load Balancer vs Application Gateway
* Traffic Manager vs Azure Front Door
* VNet Peering vs VPN Gateway

### Compute

* VMSS vs individual VMs
* Availability Sets vs Availability Zones
* VM Extensions vs Custom Script Extension

### Storage

* Blob Storage vs Azure Files
* Standard vs Premium
* LRS vs ZRS vs GRS vs RA-GRS
* SAS vs Access Keys
* Lifecycle Management vs manual tiering

### Recovery

* Azure Backup vs Azure Site Recovery

If you can explain **why** you would choose one over the other, you're in a much stronger position.

---

## 14. Don't Underestimate Networking

Networking appears throughout AZ-104.

Make sure you understand:

* VNets
* Subnets
* NSGs
* ASGs
* Route Tables / UDRs
* Private Endpoints
* Service Endpoints
* VNet Peering
* VPN Gateway
* ExpressRoute
* Azure Firewall
* Load Balancer
* Application Gateway
* Front Door
* Traffic Manager
* NAT Gateway

Don't memorize definitions alone.

Understand **where traffic goes**.

---

## 15. Don't Underestimate Identity

Identity is another area that connects to almost everything.

Understand:

* Microsoft Entra ID
* Users
* Groups
* RBAC
* Managed Identities
* Conditional Access
* PIM
* Administrative Units
* Hybrid Identity

Especially understand the difference between:

> **Authentication**

and

> **Authorization**

and then understand how Azure uses identity to control access to resources.

---

## 16. Know Azure's Hierarchy

Understand this structure:

```text
Management Group
        ↓
Subscription
        ↓
Resource Group
        ↓
Resource
```

And understand how things such as:

* RBAC
* Azure Policy
* Locks
* Tags

fit into this hierarchy.

---

## 17. Understand Scope and Inheritance

A recurring Azure administration concept is:

> **Where is this configuration applied?**

Understand scopes.

For example, an RBAC assignment or Azure Policy can exist at different levels of the Azure hierarchy and may be inherited by child resources.

When a question asks why a user has access, don't only look at the resource itself.

Think about inherited permissions.

---

## 18. Know the Difference Between Monitoring Tools

Don't treat Azure Monitor, Log Analytics, Advisor and Service Health as interchangeable.

Understand:

* **Azure Monitor** → monitoring platform
* **Log Analytics** → log storage and KQL analysis
* **Alerts** → detect conditions
* **Action Groups** → define notification/action responses
* **Advisor** → recommendations
* **Service Health** → Azure service issues affecting you

---

## 19. Understand Backup vs Disaster Recovery

These are not the same thing.

### Azure Backup

Think:

> **Recover deleted/corrupted/lost data or resources.**

### Azure Site Recovery

Think:

> **Keep workloads available during a major outage by replicating and failing over.**

If a question involves **replication, failover or failback**, think Site Recovery.

If it involves **backup and restore**, think Azure Backup.

---

## 20. Don't Panic When You See Something Unfamiliar

You will probably encounter questions where you don't immediately know the answer.

That's normal.

Don't let one unfamiliar service destroy your confidence.

Break the question down:

1. What is the business requirement?
2. What Azure area is being tested?
3. What constraints are given?
4. Which options can I eliminate?
5. What service best fits the remaining requirement?

You can often reason your way to the answer without knowing every detail.

---

## 21. The Exam Is Broad

AZ-104 isn't necessarily difficult because every individual concept is complicated.

It's difficult because the syllabus is **wide**.

You are expected to understand administration across:

* Identity
* Governance
* Compute
* Storage
* Networking
* Monitoring
* Backup
* Disaster Recovery

Accept that you won't know everything.

Aim for **broad understanding + strong fundamentals + scenario reasoning**.

---

## 22. Don't Chase Perfect Practice Scores

Practice exams are indicators, not guarantees.

A score is much more useful when you understand:

* Why you got questions wrong
* Which domains you're weak in
* Whether you're improving
* Whether you can reason through unfamiliar scenarios

A 90% score achieved through memorizing a question bank isn't necessarily better preparation than a 75% score where you deeply understand every mistake.

---

## 23. Build Exam Stamina

AZ-104 requires sustained concentration.

Practice sitting through longer blocks of scenario-based questions.

Get comfortable with:

* Reading carefully
* Making decisions
* Flagging difficult questions
* Moving forward
* Returning to difficult questions
* Maintaining concentration

Don't let one difficult question consume excessive time.

---

## 24. Don't Cram Random Information

In the final days, prioritize:

1. Your mistakes
2. Weak domains
3. Service comparisons
4. Your cheat sheet
5. Microsoft Learn clarification
6. Hands-on experience
7. Final revision

Don't suddenly try to memorize hundreds of unrelated facts.

Strengthen the mental model you've already built.

---

## 25. Trust Your Preparation

By exam day, you probably won't feel like you know everything.

That's normal.

If you've:

* Studied consistently
* Used Microsoft Learn
* Practiced questions
* Reviewed your mistakes
* Built Azure resources
* Learned the major service comparisons
* Practiced scenario-based reasoning

then you've done the work.

You don't need to know everything.

You need to know enough to make good decisions.

---

# ⭐ Final AZ-104 Memory Nuggets

Keep these mental shortcuts in your head:

| Concept                 | Think                                                    |
| ----------------------- | -------------------------------------------------------- |
| **RBAC**                | Who can do what?                                         |
| **Azure Policy**        | What configurations/actions are allowed?                 |
| **Locks**               | Protect resources from modification/deletion             |
| **NSG**                 | Filter network traffic                                   |
| **ASG**                 | Group VMs for NSG rules                                  |
| **UDR**                 | Control/change routing                                   |
| **Service Endpoint**    | Secure access to Azure service using its public endpoint |
| **Private Endpoint**    | Private IP for Azure service                             |
| **Load Balancer**       | Layer 4                                                  |
| **Application Gateway** | Layer 7                                                  |
| **Traffic Manager**     | DNS-based routing                                        |
| **Front Door**          | Global HTTP(S) entry point                               |
| **VPN Gateway**         | Encrypted connection over the internet                   |
| **ExpressRoute**        | Private dedicated connectivity                           |
| **Blob**                | Object storage                                           |
| **Files**               | Managed file shares                                      |
| **Queue**               | Messages                                                 |
| **Table**               | NoSQL key-value data                                     |
| **VMSS**                | Manage and scale groups of VMs                           |
| **Availability Set**    | Fault/update domains within a datacenter                 |
| **Availability Zone**   | Separate physical datacenter locations within a region   |
| **Azure Backup**        | Backup and restore                                       |
| **Site Recovery**       | Replication and disaster recovery                        |
| **Monitor**             | Monitoring platform                                      |
| **Log Analytics**       | Logs + KQL                                               |
| **Advisor**             | Recommendations                                          |
| **Service Health**      | Personalized Azure service health information            |

> **If you can explain each of these concepts in your own words—and explain when you'd choose one over its closest alternative—you're in a much stronger position for AZ-104.**

---

# Final Thought

Azure administration isn't about memorizing every service or configuration option.

It's about understanding how Azure works, selecting the right solution for the scenario, managing resources securely and efficiently, and continuously building practical experience.

Every deployment, mistake, troubleshooting session, and practice question adds to that mental model.

**Learn. Deploy. Break. Fix. Repeat.**

Good luck with your AZ-104 journey. ☁️

