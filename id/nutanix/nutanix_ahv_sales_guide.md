# Nutanix AHV Sales Enablement Guide
### For Net-New Customer Conversations | Competitive Context: VMware / vSphere

---

## How to Use This Document

This guide is designed to help you walk into a sales conversation feeling confident about Nutanix AHV — even if you have never managed a server in your life. Start at the top and read straight through. The first section gives you the foundation you need to understand what the product is and why customers care. The rest of the document builds on that base and gives you the language, stories, and questions you need to run a real conversation.

> **Reading time:** Approximately 25–30 minutes for the full document.

---

## Section 1: Start Here — The Basics Every Seller Must Know

### 1.1 What Is a Server (and Why Does It Matter)?

Before we talk about Nutanix, let us make sure we share the same starting point.

A **server** is a powerful computer that lives inside a company's data center (or a rented facility). It does not have a screen or a keyboard. Its only job is to run software — things like email systems, databases, financial applications, or the website a company uses to take orders from customers. When employees log in to work every morning, they are usually connecting to one of these servers.

Most companies do not run just one server. They run dozens, hundreds, or even thousands of them.

### 1.2 The Problem With Running Lots of Servers the Old Way

Imagine you need ten applications to run your business — one for email, one for your database, one for your website, and so on. In the old model, you might buy ten separate physical servers — one for each application. This creates real problems:

- Most of the time, each server sits mostly idle. You sized it for the busiest day of the year, but on a normal day it might only be using 10–20% of its power.
- Every server needs to be physically managed, patched, and eventually replaced.
- If one server breaks, the application running on it goes down.
- The data center fills up with hardware, cables, and cooling equipment.

This is expensive, wasteful, and hard to manage.

### 1.3 The Solution: Virtualization

**Virtualization** is the technology that solved this problem. Instead of dedicating one physical server to one application, virtualization software lets you run *many* applications on *one* physical server at the same time — each inside its own isolated, self-contained bubble called a **virtual machine (VM)**.

Think of it like this: instead of owning ten separate houses (servers), you build one large apartment building (one powerful server) and carve it into ten apartments (ten VMs). Each apartment is private and independent, but they all share the same building infrastructure — electricity, plumbing, and walls.

This is a huge deal for businesses. They can:
- Run more applications on fewer physical machines.
- Use their hardware investment more efficiently.
- Spin up new applications in minutes instead of ordering new hardware that takes weeks to arrive.

### 1.4 What Is a Hypervisor?

The software that creates and manages virtual machines is called a **hypervisor**. You can think of the hypervisor as the building manager of the apartment building. It decides how much computing power each apartment (VM) gets, makes sure the tenants do not interfere with each other, and handles the day-to-day operations.

For the past twenty years, the dominant hypervisor in enterprise data centers has been **VMware vSphere** (powered by a product called ESXi). If you are talking to an IT buyer today, there is a very good chance their data center runs on VMware.

### 1.5 Enter Nutanix AHV

**Nutanix AHV** (Acropolis Hypervisor) is Nutanix's own modern hypervisor. It is a direct competitor to VMware's ESXi, but it is built differently, managed differently, and sold differently.

AHV does not stand alone. It is the virtualization engine inside a larger platform called **Nutanix Cloud Infrastructure (NCI)**, which bundles compute (servers), storage (where data lives), and networking (how data moves) into a single, unified system. This type of architecture is called **hyperconverged infrastructure (HCI)** — hyper because everything is tightly integrated into one thing, rather than three separate things you have to connect and manage independently.

**The short version for a sales call:**
> *"Nutanix AHV is a modern hypervisor that comes built into the Nutanix platform. It lets companies run all their virtual machines without paying separately for virtualization software — and it is managed from one simple interface that controls everything."*

---

## Section 2: Why Customers Are Looking Right Now

### 2.1 The VMware / Broadcom Disruption

This is the single biggest market event creating urgency for your prospects. You need to understand this story cold.

**What happened:** In late 2023, Broadcom — a semiconductor and software company — completed the acquisition of VMware. Almost immediately, Broadcom changed how VMware products are sold and supported in ways that alarmed a large portion of VMware's customer base.

**Why customers are upset:**

- Broadcom eliminated perpetual licenses. Customers who had bought VMware software outright must now move to subscription-only contracts. For many organizations, this was not budgeted.
- Broadcom consolidated VMware products into large bundles. Customers who only needed one or two features found themselves being forced to buy a much larger package to get what they previously had.
- Many organizations reported renewal quotes that were dramatically higher than their previous contracts — in some documented cases, three to ten times higher or more.
- Broadcom ended relationships with many smaller VMware channel partners and resellers, disrupting support relationships that customers had relied on for years.

**Real-world examples you can use in conversation:**

- Toshiba, a VMware customer for sixteen years, received a renewal quote reportedly at ten times its previous cost and decided to migrate to Nutanix.
- A financial services company was quoted a 300–400% price increase and migrated 1,000 to 2,000 virtual machines to Nutanix in a matter of months.
- Computershare, a global stock registry company, was quoted a price increase between ten and fifteen times its current cost for 24,000 VMs. The CTO said the Nutanix project would pay for itself in single-digit months.

**Why this matters for your sale:**
Your prospect is almost certainly either actively evaluating alternatives or has already had a painful conversation internally about their VMware renewal. You do not need to manufacture urgency — it exists in the market. Your job is to show up at the right time with the right answer.

### 2.2 The Broader Problem AHV Solves (Beyond VMware)

Even setting aside the Broadcom disruption, there are structural reasons why organizations look for alternatives to the traditional VMware model:

1. **Complexity.** VMware's full stack involves multiple separate products — ESXi for the hypervisor, vCenter for management, vSAN for storage, NSX for networking — each with its own licensing, its own upgrade process, and often its own specialized skillset. Managing all of this requires experienced (and expensive) IT staff.

2. **Cost stacking.** Historically, VMware charged separately for each layer of the stack. Every advanced feature was an add-on. This created situations where customers needed to buy several products to get the complete experience they expected.

3. **Rigid, slow infrastructure.** Traditional data center setups require weeks or months to provision new servers. IT teams spend enormous amounts of time on routine maintenance tasks. Organizations want infrastructure that behaves more like the cloud — fast, self-service, easy to scale.

4. **Security gaps.** Keeping virtual machines properly isolated from each other and protecting the network traffic that flows *between* them (called east-west traffic) has historically required separate security tools and products.

---

## Section 3: What AHV Is and How It Works

### 3.1 AHV as Part of the Nutanix Stack

It helps to understand that AHV does not live by itself. It is one piece of the Nutanix platform. Here is how the pieces connect:

| Layer | What It Does | Nutanix Component |
|---|---|---|
| Virtualization | Creates and runs virtual machines | **AHV** (the hypervisor) |
| Storage | Stores the data that VMs use | **AOS** (Acropolis Operating System) |
| Management | Controls everything through one interface | **Prism** (the management console) |
| Networking & Security | Controls how VMs talk to each other | **Nutanix Flow** |
| Migration | Moves VMs from VMware to AHV | **Nutanix Move** (free tool) |

All of these layers are part of the same platform. They are designed to work together, managed from one place, and updated together. This is fundamentally different from VMware, where each layer often requires separate management, separate licensing, and separate upgrade windows.

### 3.2 What AHV Does in Plain Language

Here is what AHV actually does, explained the way you would describe it to a prospect:

**It runs virtual machines.** AHV creates and manages VMs just like VMware does. It supports all major operating systems — Windows, Linux, and others. It is certified to run demanding enterprise applications from Microsoft (SQL Server, Exchange), Oracle, SAP, and many others.

**It runs directly on the hardware.** AHV is what's called a "bare-metal" or "Type 1" hypervisor — it installs directly on the physical server, not on top of another operating system. This is the same approach VMware uses, and it is the gold standard for performance and stability.

**It keeps VMs running even when hardware fails.** AHV includes built-in **High Availability (HA)**. If a physical server in the cluster fails unexpectedly, AHV automatically detects the failure and restarts the affected VMs on other healthy servers in the cluster — without anyone having to manually intervene. This happens in the background, with minimal disruption.

**It moves VMs without turning them off.** AHV supports **Live Migration**, which means a running VM can be picked up and moved from one physical server to another without pausing or restarting the application. This is essential for routine maintenance. If a server needs to be taken offline for an upgrade, its VMs are quietly moved elsewhere first, and users never notice.

**It automatically balances workloads.** The **Acropolis Dynamic Scheduler (ADS)** constantly watches how busy each server in the cluster is. If one server is getting overloaded, ADS automatically moves VMs to less-busy servers. IT teams do not have to monitor this manually or set complex rules — it just happens.

**It is managed from a single screen.** Nutanix **Prism** is the web-based management console that controls AHV and the entire Nutanix cluster. There is no separate vCenter equivalent to install and manage. Compute, storage, and networking are all visible and manageable in one place. Software upgrades — including the hypervisor itself — can be triggered with a single click and happen non-disruptively.

### 3.3 What "Hyperconverged" Really Means for a Customer

When Nutanix talks about hyperconverged infrastructure, here is how to explain it in a sales conversation:

> *"Traditional data centers have three separate silos — servers, storage arrays, and networking gear — all bought from different vendors, all managed with different tools. Nutanix collapses all of that into a single system. You buy Nutanix nodes, and they deliver compute, storage, and virtualization together. You manage everything through one interface. When you need more capacity, you add another node and it joins the cluster automatically. It is designed to make infrastructure feel more like a cloud service than a traditional data center."*

---

## Section 4: Key Capabilities — Deeper Dives for Informed Conversations

### 4.1 Built-in Security: Nutanix Flow

**The problem it solves:** In a traditional network, a firewall sits at the edge — it checks traffic coming *into* the data center and going *out* of it. But what about traffic flowing between virtual machines *inside* the data center? This "east-west" traffic is often unprotected. If ransomware or a bad actor gains access to one VM, they can potentially move freely between systems inside the data center — a technique called lateral movement.

**What Flow does:** Nutanix Flow is a security capability built directly into AHV. It creates a distributed, software-based firewall that controls exactly which VMs are allowed to communicate with each other. This concept is called **microsegmentation**.

Instead of thinking about IP addresses and firewall rules — which is complex and breaks when VMs move — Flow lets IT teams apply labels (called categories) to groups of VMs based on their function. For example: all "web tier" VMs, all "database" VMs, all "production" VMs. Then a policy is written saying which groups are allowed to talk to which. When a VM moves to a different server, its category label moves with it, and the policy follows automatically.

**Why this matters to a security-conscious buyer:**
- Limits the damage a ransomware attack can do by preventing lateral movement between VMs.
- Helps satisfy compliance requirements (like PCI-DSS or HIPAA) that require workload isolation.
- Replaces or reduces the need for separate, expensive firewall products for east-west traffic.
- No additional agents or software to install on VMs — it works at the hypervisor level.

**How to position it in a call:**
> *"AHV has built-in network security called Flow. Instead of relying only on the firewall at the edge of your network, Flow creates a security boundary around every workload — right inside the hypervisor. If one VM gets compromised, the damage can be contained. This is the kind of microsegmentation that VMware charges separately for with NSX."*

### 4.2 Simple, Unified Management: Nutanix Prism

Prism is the management experience that differentiates Nutanix AHV most visibly from VMware in a demo.

In a VMware environment, IT administrators typically use multiple separate tools: vCenter for managing VMs, separate storage management interfaces, separate networking tools, and often third-party tools for monitoring and capacity planning.

Prism is a single web-based console that manages everything — VMs, storage, networking, cluster health, performance analytics, and software upgrades — for all Nutanix clusters in an organization. It is browser-based, requires no separate client software, and is designed to be intuitive enough that new administrators can be productive quickly.

**One-Click Operations:** Routine tasks that might require a maintenance window and hours of work in a VMware environment — such as upgrading the hypervisor itself — can be done non-disruptively in AHV through Prism. This includes firmware updates across the entire cluster.

**Prism Central:** For organizations running multiple Nutanix clusters across multiple locations, Prism Central provides a single view across all of them — including clusters running in public clouds like AWS or Azure.

**How to position it in a call:**
> *"One thing customers consistently say after migrating to Nutanix is that their IT team has more time back. Managing the infrastructure goes from being a full-time job for several people to something a smaller team handles easily. Prism was designed so that you do not need VMware-certified experts just to keep the lights on."*

### 4.3 Enterprise Reliability: High Availability and Data Protection

AHV is built for production workloads. These are the features that give IT decision-makers and CIOs confidence to put critical business applications on the platform:

**High Availability (HA):** Nutanix clusters are designed to tolerate hardware failures without losing data or taking applications offline. The storage layer maintains multiple copies of data across different physical nodes. If a node fails, VMs are restarted on surviving nodes automatically. The number of failures the cluster can tolerate is configurable.

**VM Live Migration:** Moving a running VM between servers is seamless and non-disruptive. This is critical for performing hardware maintenance without scheduling downtime.

**Snapshots and Clones:** AHV supports fast, space-efficient snapshots — point-in-time copies of a VM's state — that can be used to quickly recover from problems or to spin up test copies of production environments. Cloning a VM for testing takes seconds, not hours.

**Disaster Recovery with Nutanix Leap:** Nutanix includes built-in disaster recovery workflows that allow IT teams to replicate VMs to a remote site or a public cloud, and to execute a failover in an emergency without having to purchase separate DR software.

**Compatibility with Backup Tools:** AHV exposes standard APIs that major backup vendors (like Veeam, Commvault, and others) use to perform full, incremental, and differential backups — protecting existing investments in backup infrastructure.

### 4.4 Migration Made Easy: Nutanix Move

One of the biggest objections in a net-new sale is the fear of migration. Customers have hundreds or thousands of VMs running on VMware. The idea of moving them is scary.

**Nutanix Move** is a free migration tool provided by Nutanix specifically to address this fear. It automates the process of moving virtual machines from VMware ESXi (and other sources like Hyper-V, AWS, and Azure) to AHV.

Key things to know about Nutanix Move:

- It **pre-seeds data** before the cutover, meaning the bulk of the data transfer happens in the background while the VM is still running on VMware. The final cutover window is small, minimizing downtime.
- It supports **test migrations** — customers can try moving a VM in an isolated environment to verify that it works correctly before doing the real thing.
- It **does not require application refactoring.** The VMs move as-is. No code changes, no architectural redesign.
- It handles driver installation and compatibility adjustments automatically.

**How to position it in a call:**
> *"Migration is always the first concern we hear. Nutanix provides a free tool called Move that automates the migration of VMs from VMware. Most customers migrate in phases — they start with less critical workloads to build confidence, then move production systems. We have customers who have migrated thousands of VMs with minimal disruption."*

### 4.5 Hybrid Cloud: AHV Beyond the Data Center

AHV is not limited to on-premises data centers. Through **Nutanix Cloud Clusters (NC2)**, customers can run AHV — and the same Nutanix management experience — inside AWS, Azure, Google Cloud, and other public clouds.

This means:

- A customer can manage on-premises and cloud workloads from the same Prism interface.
- VMs can be moved between on-premises and cloud environments without refactoring.
- Licenses are portable — if a customer reduces their on-premises footprint and grows in the cloud, the same license follows them.

This is particularly powerful in conversations about disaster recovery (the cloud becomes the recovery site), cloud bursting (temporarily running extra capacity in the cloud during peak periods), and multi-cloud flexibility.

---

## Section 5: Competitive Positioning

### 5.1 AHV vs. VMware vSphere — The Core Comparison

| Topic | VMware vSphere (Broadcom) | Nutanix AHV |
|---|---|---|
| Hypervisor | ESXi (separate product) | AHV (included in the platform) |
| Management | vCenter (separate product) | Prism (unified, included) |
| Storage | vSAN (separate add-on) | AOS Distributed Storage (included) |
| Networking/Security | NSX (separate, expensive add-on) | Nutanix Flow (included or add-on depending on edition) |
| Migration Tool | N/A | Nutanix Move (free) |
| Licensing Model | Per-CPU core, subscription bundles | Capacity-based, modular |
| Upgrade Process | Complex, often disruptive | One-click, non-disruptive |
| Learning Curve | Steep, requires certified specialists | Designed for smaller, generalist IT teams |

### 5.2 Key Differentiators to Emphasize

**1. Simplicity as a competitive advantage.** VMware's power comes with complexity. Managing a full VMware stack requires dedicated expertise in multiple product domains. Nutanix AHV is built for IT teams that want infrastructure to require less hands-on management. Smaller teams accomplish more.

**2. Everything is in one place.** When something goes wrong in a VMware environment, IT staff might have to check vCenter, the vSAN management interface, and NSX separately to diagnose the problem. In Nutanix, all of that information is in Prism.

**3. Enterprise-grade security included.** VMware's microsegmentation story requires NSX — a complex, expensive, separately licensed product. Nutanix Flow provides microsegmentation built into the hypervisor, at a lower entry cost and with simpler management.

**4. Non-disruptive upgrades.** Upgrading a VMware environment often requires scheduling maintenance windows, careful sequencing of product versions, and significant IT staff time. Nutanix upgrades are orchestrated through Prism and happen while the environment continues running — without taking applications offline.

**5. A credible hybrid cloud story.** With NC2, Nutanix customers run the same stack on-premises and in the cloud. VMware's equivalent offering (VMware Cloud on AWS) was significantly disrupted by the Broadcom acquisition and changes to the AWS partnership.

### 5.3 Handling Common Objections

**"VMware has been around longer and has a bigger ecosystem."**
> *"That is true, and VMware is a mature platform. But maturity is different from being the best option going forward. The ecosystem concern is real, and Nutanix is not a fit for every workload — they are transparent about that. For roughly 95% of standard enterprise virtualization needs, AHV is a fully capable replacement. The question is whether the remaining 5% of niche integrations is worth the cost and complexity of staying with VMware in its current form. Most customers we talk to are finding it is not."*

**"We have invested heavily in VMware skills and certifications."**
> *"We hear this often. Here is what customers tell us after the switch: the learning curve for Nutanix is short. Prism is designed to be intuitive. Your team does not need to start over — they can apply their virtualization knowledge in a simpler environment. Nutanix also provides training and certification programs to bridge the gap."*

**"What about our existing backup tools and third-party integrations?"**
> *"Nutanix AHV supports standard backup APIs, and major vendors like Veeam and Commvault have full AHV support. Before migration, it is always worth doing a compatibility check — Nutanix has a hardware and software compatibility list for exactly this purpose. In the large majority of cases, existing tools work."*

**"A migration sounds risky and disruptive."**
> *"That is the number one concern we hear, and it is a fair one. That is why Nutanix built Move — a free, automated migration tool specifically for this. The migration can be done in phases. You can test individual VMs before committing. You can run VMware and AHV in parallel during a transition. Multiple customers have migrated thousands of VMs without business disruption."*

**"We are not sure about support quality from a smaller vendor."**
> *"Nutanix has a ten-year average Net Promoter Score above 90, which is an unusually strong indicator of customer satisfaction in enterprise IT. They also ranked as a Leader in the 2025 Gartner Magic Quadrant for Distributed Hybrid Infrastructure. Support is a legitimate evaluation point — we encourage customers to speak to references and trial the support experience."*

---

## Section 6: Who Buys This and Why

### 6.1 Ideal Customer Profile

Nutanix AHV tends to resonate most strongly with organizations that share these characteristics:

- **Running VMware today** — especially those facing upcoming renewals or who have already received a Broadcom pricing proposal.
- **Mid-market to large enterprise** — organizations with meaningful VM footprints (100 to 10,000+ VMs) where virtualization costs are a real budget line item.
- **Lean IT teams** — organizations that want powerful infrastructure but do not have large teams of specialists dedicated to managing it.
- **Security-conscious industries** — healthcare, financial services, government, and other regulated industries where VM isolation and compliance matter.
- **Organizations with hybrid cloud ambitions** — companies that want to run workloads across on-premises and public cloud environments without managing two completely different stacks.
- **VDI (Virtual Desktop Infrastructure) environments** — Nutanix is particularly well known for VDI performance, especially in large-scale deployments.

### 6.2 The Buying Team

In a Nutanix AHV sale, you will typically engage with:

| Role | What They Care About | Your Message |
|---|---|---|
| **CIO / VP of IT** | Strategic direction, vendor risk, long-term cost | Vendor independence, lower TCO, hybrid cloud flexibility |
| **Infrastructure Manager** | Operational simplicity, team bandwidth, reliability | One management plane, non-disruptive operations, strong HA |
| **Systems Administrator** | Day-to-day usability, migration risk, tool familiarity | Prism ease of use, Nutanix Move, familiar VM concepts |
| **CISO / Security Team** | Workload isolation, compliance, attack surface | Flow microsegmentation, zero trust, built-in security |
| **CFO / Finance** | Total cost of ownership, budget predictability | Consolidated licensing, elimination of separate add-ons |

---

## Section 7: Discovery Questions

Use these questions to open up a conversation and surface pain. Listen for the cues that tell you which capabilities to emphasize.

### Opening Questions (Understanding Their Current State)
- "Can you walk me through your current virtualization environment? What are you running today?"
- "How many virtual machines does your team manage, roughly?"
- "How long have you been on VMware, and how is that relationship going?"
- "Have you had any conversations internally about your virtualization strategy since the Broadcom acquisition?"

### Pain-Surfacing Questions
- "When your renewal comes up, how much visibility do you have into what the new pricing might look like?"
- "How much of your team's time goes into managing and maintaining the virtualization stack vs. working on things that directly benefit the business?"
- "If a server failed tonight, how confident are you that your applications would come back up automatically?"
- "How are you currently protecting workloads from threats that get inside your network?"
- "How long does it take today to provision a new environment when a project team needs one?"

### Future-Looking Questions
- "If you could change one thing about how your current infrastructure works, what would it be?"
- "Are there workloads you want to run in the cloud but have not been able to move because of cost or complexity?"
- "What does your ideal IT operations model look like in three years?"

---

## Section 8: Proof Points and Customer Stories

### Real-World Outcomes
These are real examples from documented public sources that you can reference in conversations:

- **Toshiba** migrated from VMware after receiving a Broadcom renewal quote reportedly ten times their previous cost. They selected Nutanix as their hybrid cloud platform for both cost reduction and modernization.

- **Computershare** (global stock registry operator, 24,000 VMs) began migrating from VMware to Nutanix AHV after receiving a renewal quote estimated at ten to fifteen times their previous price. The CTO projected the project would pay for itself within single-digit months.

- **A financial services company** received a 300–400% price increase on their VMware renewal, migrated 1,000–2,000 VMs to Nutanix AHV over approximately six months, and completed the project on schedule.

- **MSIG Insurance Asia**, a VMware customer since 2007, was offered a renewal that would have increased costs by 300–400%. They began evaluating alternatives.

- **University of Reading** adopted Nutanix AHV for campus-wide VDI, reducing licensing costs and improving performance.

### Analyst Recognition
- Nutanix was named a **Leader in the 2025 Gartner Magic Quadrant for Distributed Hybrid Infrastructure**.
- Nutanix has maintained a **Net Promoter Score above 90** for ten consecutive years — one of the highest in enterprise IT.
- AHV adoption among Nutanix customers has reached approximately **89% of total cores**, reflecting strong organic growth.

---

## Section 9: Key Terms Glossary

Use this section as a quick reference when you encounter technical language in a customer meeting.

| Term | Plain-English Definition |
|---|---|
| **Hypervisor** | Software that creates and manages virtual machines on a physical server. AHV is Nutanix's hypervisor. ESXi is VMware's. |
| **Virtual Machine (VM)** | A software-based computer that runs inside a physical server. Each VM runs its own operating system and applications. |
| **Hyperconverged Infrastructure (HCI)** | An architecture that combines compute, storage, and networking into a single, unified system managed by one platform. |
| **Cluster** | A group of physical servers (nodes) that work together as a single pool of resources under AHV. |
| **Prism** | Nutanix's web-based management console. Controls VMs, storage, networking, and cluster health in one place. |
| **Live Migration** | Moving a running virtual machine from one physical server to another without interrupting the application. |
| **High Availability (HA)** | Automatic restart of VMs on healthy servers if a physical server fails unexpectedly. |
| **Acropolis Dynamic Scheduler (ADS)** | AHV's built-in workload balancer. Automatically moves VMs to prevent any single server from being overloaded. |
| **Microsegmentation** | A security technique that controls which VMs are allowed to communicate with each other, limiting how far an attack can spread. |
| **Nutanix Flow** | Nutanix's built-in networking and security product. Provides microsegmentation for AHV workloads. |
| **East-West Traffic** | Network traffic that travels *between* VMs inside the data center (as opposed to traffic coming from the internet, which is north-south). |
| **vSphere** | VMware's virtualization platform. Includes ESXi (hypervisor) and vCenter (management). |
| **NSX** | VMware's networking and security add-on product. Provides microsegmentation and software-defined networking. Sold separately. |
| **AOS (Acropolis Operating System)** | The distributed operating system that runs on all Nutanix nodes and powers storage, replication, and cluster management. |
| **Nutanix Move** | A free Nutanix tool that automates the migration of VMs from VMware (and other sources) to AHV. |
| **NC2 (Nutanix Cloud Clusters)** | A product that allows customers to run the Nutanix AHV stack in public clouds like AWS and Azure. |
| **Bare-Metal Hypervisor** | A hypervisor that installs directly on the physical hardware, not on top of another operating system. Both AHV and ESXi are bare-metal. |
| **TCO (Total Cost of Ownership)** | The full cost of owning and operating a system over time, including licensing, hardware, staffing, and maintenance. |
| **VDI (Virtual Desktop Infrastructure)** | Technology that hosts desktop environments (like Windows) on a central server, allowing employees to access their desktop from any device. |

---

## Section 10: Quick-Reference Summary

> **What is AHV?**
> A modern, enterprise-grade hypervisor built into the Nutanix platform. It creates and manages virtual machines, is managed through a single interface called Prism, and includes built-in capabilities for high availability, live migration, workload balancing, and security.

> **Who should buy it?**
> Organizations currently running VMware who face renewal pain, want simpler operations, want to reduce the complexity of their infrastructure stack, or want a credible hybrid cloud path.

> **What makes it different from VMware?**
> Simpler management, unified platform (no separate products for storage, networking, and security), non-disruptive upgrades, built-in migration tooling, and a licensing model that does not require purchasing multiple layers separately.

> **What is the market moment?**
> The Broadcom acquisition of VMware has caused widespread pricing disruption. Many organizations are actively evaluating alternatives. Nutanix AHV is the most direct like-for-like replacement available.

> **What should I do after a discovery call?**
> Involve a Nutanix Systems Engineer (SE) for a technical deep-dive. Request a reference customer from a similar industry. Offer a test drive (Nutanix has a hosted environment available at nutanix.com/one-platform). Ask the customer when their VMware renewal is due — that date is your target.

---

*Sources: Nutanix.com, Nutanix Bible (nutanixbible.com), TechTarget, The Register, Computer Weekly, Veeam Blog, Gartner (2025 Magic Quadrant for Distributed Hybrid Infrastructure), SDxCentral. This document is intended for internal sales enablement purposes only.*
