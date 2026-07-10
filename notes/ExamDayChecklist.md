## Exam Day Preparation - Memory and Mentality

Read this on the morning of the exam. (or on the day before)

---

### If you have the time before the exam:

- Watch this [AZ-104 Study Cram](https://youtu.be/0Knf9nub4-k?si=gcCdGrmFYzf4v5vf) by John Savill. It is an excellent refresher. (I watched it at 2x speed to save time.)

- Go through the [Cheat Sheet](../notes/CheatSheet.md) for a quick revision of the core concepts.

- Get a good night's sleep, take a relaxing shower, and spend a few minutes doing breathing exercises before leaving for the exam

---

### ⭐ Memory Nuggets

If you can explain each of these concepts in one or two sentences without looking at your notes, you're in a strong position for AZ-104.

#### Identity & Governance

- **RBAC** = Who can perform actions
- **Azure Policy** = What is allowed or denied
- **Resource Locks** = Protect resources from accidental changes or deletion

#### Networking

- **NSG** = Filters inbound and outbound network traffic
- **ASG** = Logically groups VMs for NSG rules
- **UDR** = Overrides Azure's default routing
- **Service Endpoint** = Secure access to Azure PaaS services over the Azure backbone while keeping public endpoints
- **Private Endpoint** = Private IP address for Azure PaaS services
- **Load Balancer** = Layer 4 (TCP/UDP) load balancing
- **Application Gateway** = Layer 7 (HTTP/HTTPS) load balancing with WAF support
- **Traffic Manager** = DNS-based global traffic routing
- **Front Door** = Global HTTP(S) load balancing, acceleration, and WAF
- **VPN Gateway** = Encrypted connection over the public Internet
- **ExpressRoute** = Private dedicated connection to Azure
- **NAT Gateway** = Provides outbound Internet connectivity for private resources

#### Storage

- **Blob Storage** = Object storage for unstructured data
- **Azure Files** = Managed SMB/NFS file shares
- **Queue Storage** = Message storage for asynchronous communication
- **Table Storage** = NoSQL key-value data store
- **SAS** = Delegated, time-limited access to storage resources
- **Lifecycle Management** = Automatically moves or deletes blobs based on rules

#### Compute

- **VM Scale Sets** = Automatically scale virtual machines
- **Availability Set** = Protects VMs from host failures and maintenance within a datacenter
- **Availability Zone** = Protects workloads across physically separate datacenters
- **Azure Backup** = Backup and recovery solution
- **Azure Site Recovery** = Disaster recovery and failover

#### Monitoring

- **Azure Monitor** = Collects metrics and logs
- **Log Analytics** = Query and analyze logs using KQL
- **Alerts** = Notify when conditions are met
- **Action Groups** = Define notification and automation actions
- **Azure Advisor** = Best-practice recommendations
- **Service Health** = Azure service outages and maintenance events

---

### Things to remember:

If you have been following everything outlined here in the [Study Guide](../docs/StudyGuide.md) over the past 5-6 weeks, I think you have a realistic chance of passing.

Not because you've memorized every Azure service **(you probably haven't).**

But, Because you've developed the **Azure Administrator way of thinking**. Which means:

- You understand why the services exist.
- You know when each service should be used.
- You recognize common patterns and architectures.
- You can reason through unfamiliar scenarios.

That's exactly what AZ-104 is trying to test.

---

### During the Exam

- Read every question carefully.
- Identify the actual requirement before looking at the answer choices.
- Don't panic if you encounter unfamiliar services or scenarios.
- Eliminate obviously incorrect options first.
- Trust the preparation you've already put in.
- Skip any question taking more than 2 minutes of your time.

---

### Final Message

Remember, it's a two-hour exam. **Stay calm, stay focused, and manage your time well.**

> Go ahead and slay the dragon! All the best - you've got this. ☁️
