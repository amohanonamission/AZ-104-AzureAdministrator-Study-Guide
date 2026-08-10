# AZ-104 Study Guide

> A practical roadmap for preparing for the **Microsoft Certified: Azure Administrator Associate (AZ-104)** through self-study, hands-on practice, and scenario-based learning.

This guide is based on my own preparation and the approach I used to pass AZ-104 after approximately **5–6 weeks of focused study**.

The goal is not to memorize Azure services.

The goal is to understand how Azure works well enough to make the right administrative decisions in real-world scenarios.

---

# 1. Study Philosophy

AZ-104 has a very broad syllabus.

You will encounter a large number of services, features, configurations, and administrative concepts.

Trying to memorize everything is inefficient.

Instead, focus on understanding:

* **What** a service does
* **Why** it exists
* **When** to use it
* **When not** to use it
* How it compares with similar services
* How it interacts with other Azure services
* How it affects security, cost, availability, and administration

When learning a new service, ask:

> **What problem does this solve?**

> **When would I choose it?**

> **What would I use instead, and why?**

That mindset is much more useful than memorizing isolated definitions.

---

# 2. Understand the Major Areas

Start by building a mental map of Azure administration.

I grouped my preparation into six major areas:

### Identity

* Microsoft Entra ID
* Users and Groups
* RBAC
* Managed Identities
* Conditional Access
* PIM
* Administrative Units
* Hybrid Identity

### Compute

* Virtual Machines
* VM Scale Sets
* Availability Sets
* Availability Zones
* Managed Disks
* VM Extensions
* Azure Backup
* Azure Site Recovery

### Storage

* Storage Accounts
* Blob Storage
* Azure Files
* Queue Storage
* Table Storage
* Storage Replication
* SAS
* Stored Access Policies
* Lifecycle Management

### Networking

* VNets
* Subnets
* NSGs
* ASGs
* Route Tables / UDRs
* Service Endpoints
* Private Endpoints
* VNet Peering
* VPN Gateway
* ExpressRoute
* Azure Firewall
* Azure Bastion
* Load Balancer
* Application Gateway
* Azure Front Door
* Traffic Manager
* NAT Gateway

### Governance

* Azure Policy
* Resource Locks
* Tags
* Resource Groups
* Management Groups
* Azure Resource Manager
* ARM/Bicep concepts

### Monitoring

* Azure Monitor
* Metrics
* Logs
* Log Analytics
* Alerts
* Action Groups
* Azure Advisor
* Service Health

You don't need to master everything immediately.

Build the vocabulary first.

---

# 3. Phase 1 — Learn the Fundamentals

Start with structured video learning and Microsoft Learn.

I used **John Savill's AZ-104 material** as my primary video resource and Microsoft Learn to clarify concepts and fill gaps.

At this stage:

* Follow the course in order.
* Take lightweight notes.
* Don't stop for every small detail.
* Focus on understanding the architecture and purpose of each service.
* Mark confusing topics for later review.

### Don't try to memorize everything on the first pass.

Your first pass should answer:

> "What is Azure doing here, and why?"

---

# 4. Phase 2 — Get Into the Azure Portal

This is where the theory starts becoming real.

Create an Azure Free Trial subscription and start deploying resources yourself.

Practice creating and managing:

* Resource Groups
* Virtual Machines
* Storage Accounts
* VNets
* Subnets
* NSGs
* RBAC assignments
* Private Endpoints
* Load Balancers
* Azure Monitor
* Azure Backup
* Azure Policy

Don't just deploy them once.

Try changing configurations.

Observe what happens.

Delete resources and rebuild them.

A useful learning cycle is:

> **Deploy → Configure → Test → Break → Fix → Delete → Rebuild**

The goal is to become comfortable navigating Azure rather than simply recognizing screenshots or definitions.

---

# 5. Phase 3 — Learn Through Comparisons

One of the most important parts of AZ-104 preparation is understanding services that appear similar.

Make sure you can explain the difference between:

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

### Storage

* Blob Storage vs Azure Files
* Standard vs Premium
* LRS vs ZRS vs GRS vs RA-GRS
* SAS vs Access Keys

### Recovery

* Azure Backup vs Azure Site Recovery

Don't just memorize a table.

Ask:

> **What scenario would make me choose one over the other?**

---

# 6. Phase 4 — Practice Exams

Practice exams became one of the most valuable parts of my preparation.

I completed approximately **12 full-length practice exams** and worked through **1000+ practice questions** across my preparation.

But the important part wasn't the number of questions.

It was the review process.

For every question you get wrong, ask:

1. Why was my answer wrong?
2. Why is the correct answer correct?
3. Why are the other options wrong?
4. What Azure concept is being tested?
5. Could I recognize this concept in a different scenario?

Then research the topic if necessary.

Use:

* Microsoft Learn
* Azure documentation
* Your own notes
* The Azure Portal
* AI for additional explanations

### Don't memorize the practice-question answer.

Understand the underlying concept.

---

# 7. How to Use Practice Exams Effectively

Don't treat practice exams as a scoreboard.

A practice exam is useful when it exposes a knowledge gap.

For example:

> You get a Private Endpoint question wrong.

Don't simply memorize the correct answer.

Go back and understand:

* What a Private Endpoint actually creates
* How the private IP works
* What happens to public access
* How DNS resolution works
* How it differs from a Service Endpoint
* When Microsoft would recommend it

Now you've learned an entire concept instead of one answer.

---

# 8. Use Microsoft Learn to Fill Gaps

Microsoft Learn was one of my primary references.

Use it whenever:

* A practice question doesn't make sense
* Two answers seem correct
* You don't understand a service
* You need to verify a configuration
* You keep making the same mistake

A useful workflow is:

```text
Practice Question
       ↓
Identify Knowledge Gap
       ↓
Microsoft Learn / Documentation
       ↓
Understand the Concept
       ↓
Return to Practice
       ↓
Apply the Concept Again
```

This is much more effective than repeatedly memorizing practice questions.

---

# 9. Use AI as a Learning Tool

AI can be extremely useful during certification preparation, but I found it most useful when using it to **reason through concepts rather than simply provide answers**.

I regularly used AI to:

* Explain difficult concepts
* Compare Azure services
* Explain why answers were wrong
* Generate additional scenario questions
* Create mini case studies
* Simplify Microsoft Learn material
* Quiz me on weak topics
* Reinforce concepts through repetition

Examples of useful prompts:

> "Explain Service Endpoints vs Private Endpoints from an Azure Administrator perspective."

> "Give me an AZ-104 scenario where both answers seem correct and explain how to choose the best one."

> "Quiz me on Azure Storage. Don't reveal the answer until I respond."

> "Explain why each of these four options is correct or incorrect."

The objective is to make AI help you **think**, not replace the learning process.

---

# 10. Track Your Weak Areas

Keep a simple list of topics you repeatedly get wrong.

For example:

```text
Weak Areas

□ Private Endpoint DNS
□ Storage replication
□ RBAC scopes
□ VMSS scaling
□ Azure Policy effects
□ Log Analytics / KQL
```

Review this list regularly.

Your weakest topics should receive more attention than topics you already understand.

---

# 11. Build Scenario Thinking

As you progress, stop thinking only in definitions.

Instead, create scenarios.

For example:

> A company has multiple web servers across Azure regions and needs global HTTP routing, TLS termination, and WAF protection.

Now ask yourself:

* What service fits?
* Why?
* What alternatives exist?
* What requirement eliminates those alternatives?

This is the type of thinking you want to develop.

---

# 12. Learn to Read Azure Questions

Long scenario questions can look intimidating.

Don't let the amount of text overwhelm you.

First identify:

* What is being requested?
* What are the constraints?
* What is the priority?
* What must be avoided?
* What services are already deployed?

Useful requirement phrases include:

* Lowest cost
* Least administrative effort
* Most secure
* High availability
* Minimize downtime
* Least privilege
* No public internet access
* Automatic scaling
* Azure-native solution

These phrases aren't automatic answer keys.

They are clues about what the question is actually asking you to optimize.

---

# 13. Final Week

During the final days, shift away from learning completely new material.

Focus on:

### 1. Practice questions

Review incorrect answers and recurring mistakes.

### 2. Service comparisons

Revisit the major "A vs B" concepts.

### 3. Hands-on practice

Spend time in the Azure Portal.

### 4. Microsoft Learn

Use documentation to clarify persistent weak areas.

### 5. Study Cram

Use John Savill's Study Cram as a high-level final review.

### 6. Cheat Sheet

Review your condensed notes and memory aids.

The final stage should reinforce the mental model you've already built.

---

# 14. Don't Chase Perfect Practice Scores

Practice-exam scores are useful indicators, but they aren't the objective.

A high score achieved through memorization isn't necessarily strong preparation.

Ask yourself:

> Can I explain why the answer is correct?

> Can I explain why the other answers are wrong?

> Can I solve a similar question with different wording?

If yes, you're learning the concept.

---

# 15. Exam Day

Don't spend the final hours trying to learn the entire Azure platform.

Instead:

* Review your cheat sheet
* Review your weakest topics
* Revisit important comparisons
* Get enough sleep
* Eat appropriately
* Arrive early
* Read questions carefully
* Flag difficult questions when appropriate
* Don't let one difficult question affect the rest of the exam

Most importantly:

> **Trust the preparation you've already done.**

You aren't expected to know every Azure service.

You're expected to make reasonable administrative decisions based on the scenario.

---

# 16. The Final Mental Model

By the time you take AZ-104, try to think of Azure as a connected platform rather than a list of services.

For example:

```text
Identity
   ↓
RBAC / Policy
   ↓
Resources
   ↓
Networking
   ↓
Compute / Storage
   ↓
Monitoring
   ↓
Backup / Recovery
```

Then ask:

* Who can access it?
* What is allowed?
* Where does the traffic go?
* How is the workload deployed?
* How does it scale?
* How is it monitored?
* How is it protected?
* How is it recovered?
* How much does it cost?
* How much administration does it require?

That is the mindset of an Azure Administrator.

---

# 17. Recommended Repository Resources

Use the other files in this repository alongside this guide:

* **[Cheat Sheet](../notes/CheatSheet.md)** — condensed concepts and service comparisons
* **[Practice Questions](../practice/PracticeQuestions.md)** — AZ-104-style practice
* **[Exam Tips](../docs/ExamTips.md)** — exam strategy and lessons learned
* **[Home Labs](../practice/HomeLabs.md)** — hands-on exercises
* **[Resources](../docs/Resources.md)** — videos, documentation, and external resources
* **[Final Revision](../notes/ExamDayChecklist.md)** — final review before the exam

The idea is to use the repository as a complete study system rather than reading every file from beginning to end.

---

# Final Advice

You don't need to become an Azure expert before taking AZ-104.

You need a **broad foundation**, enough hands-on experience to understand how Azure behaves, and enough scenario practice to make good administrative decisions.

Learn the fundamentals.

Build things.

Break things.

Research your mistakes.

Understand the comparisons.

Repeat.

> **Don't memorize Azure. Learn to think in Azure.**

Good luck on your AZ-104 journey. ☁️

