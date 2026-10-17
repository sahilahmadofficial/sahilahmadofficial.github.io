---
title: "Stop Googling ISC vs Human Fabric. Read This Instead."
date: 2026-10-17 19:07:00 +0530
categories: [IAM, SailPoint]
tags: [sailpoint, isc, identityiq, human-fabric, agentic-fabric, atlas, identity-governance]
description: "IdentityNow, ISC, Human Fabric, Agentic Fabric, Atlas. What each one actually is, how they relate, and why the naming is so confusing."
image:
  path: /assets/img/posts/stop-googling-isc-vs-human-fabric/cover.jpg
  alt: "A confusing maze of product names resolving into a clear architecture diagram"
pin: false
---

I spent an hour trying to figure out what SailPoint Human Fabric was.

I had just started working with SailPoint Identity Security Cloud. I was getting comfortable with sources, aggregation, correlation, and provisioning. Things were starting to make sense.

Then someone mentioned Human Fabric in a meeting. Then Agentic Fabric. Then Atlas. Then IdentityIQ.

I closed my laptop and sat there thinking: *Wait. What am I actually working with?*

If you have ever Googled "ISC vs Human Fabric" or wondered why IdentityNow keeps appearing in old tutorials, this post is for you.

Let me break this down. No jargon. No guessing. Just what each thing is based on SailPoint's official documentation and announcements.

---

## The Problem With Product Names

SailPoint has been through several product name changes over the years. Each change made sense at the time. But the old names never fully disappeared.

You will still find IdentityNow in API documentation. You will still find ISC in older release notes. You will see Human Fabric in current developer docs. And you will see IdentityIQ in its own separate universe, completely unaffected by the cloud naming saga.

The result is a portfolio where five names refer to things that overlap but are not the same.

Here is the simplest way to understand it.

**IdentityIQ is a separate product. IdentityNow became ISC. ISC evolved into Human Fabric. Agentic Fabric is a new product for AI agents and non-human identities. Atlas is the platform underneath.**

Now let me explain each one.

---

## The Chronological Order

### IdentityIQ (IIQ): The Original Enterprise IGA Product

SailPoint IdentityIQ is the original identity governance and administration product. It is customer-managed. You install it. You run it on your own infrastructure. It handles lifecycle management, access requests, provisioning, certifications, policy enforcement, and compliance.

IdentityIQ is still actively developed. SailPoint announced IdentityIQ 9.0 in October 2026. It is not a legacy product being phased out. It is a separate product with its own architecture, its own release cycle, and its own customer base.

If you are working with on-premises IGA deployments, this is the product you learn.

### IdentityNow (IDN): The Original Cloud Product

IdentityNow was SailPoint's first cloud-delivered identity governance platform. It took the core ideas of IdentityIQ and made them available as a SaaS product.

IdentityNow is the name you will find in a lot of older documentation, API examples, and tutorials. The API hostnames still use IdentityNow-era naming in some places.

If you are learning SailPoint's cloud product, you will eventually come across IdentityNow references. Understand that these are historical, not a separate product.

### Identity Security Cloud (ISC): IdentityNow Renamed

In March 2024, SailPoint announced that IdentityNow would be renamed to Identity Security Cloud (ISC). This was a product name change, not a new product.

The underlying product stayed the same. The capabilities, architecture, and deployment model did not change. The name did.

Most of the documentation, training materials, and blog posts from 2024 onwards use ISC. This is the name I use in my work and in this blog.

### Human Fabric (SHF): The Evolution of ISC

In August 2026, SailPoint announced Human Fabric as the evolution of Identity Security Cloud. The naming shifted again.

Human Fabric is not a completely new product. It is the next identity of the same cloud product lineage. SailPoint's developer documentation explicitly states that the platform was previously IdentityNow, then Identity Security Cloud, and is now Human Fabric.

Human Fabric brings new capabilities. Continuous privilege discovery. Just-in-time provisioning. Zero Standing Privilege. Real-time security context.

But the underlying product is the same. If you know ISC, most of your knowledge transfers directly.

### Agentic Fabric (SAF): Identity Security for AI Agents

Agentic Fabric is a new product announced in May 2026 and made generally available in August 2026.

Agentic Fabric addresses a different problem. Human Fabric governs human identities. Agentic Fabric governs AI agents and non-human identities.

This matters because AI agents have credentials, permissions, execution environments, and human owners. They can query databases, invoke APIs, and access sensitive information. Traditional human-focused governance does not provide visibility into all of that.

Agentic Fabric does three things. It discovers AI agents. It maps them to owners and permissions. It protects them with adaptive controls and runtime monitoring.

Agentic Fabric is available as a standalone product and as part of SailPoint's unified Identity Security solution.

### Atlas: The Platform Foundation

Atlas is the shared platform underneath the cloud products. It is not a product you buy separately. It is the common foundation that provides identity data, connectivity, AI services, workflows, analytics, and extensibility.

Think of it this way. Human Fabric is the application for human identity governance. Agentic Fabric is the application for AI agent governance. Atlas is the platform both of them run on.

Atlas is not another name for ISC. It is the layer below ISC, Human Fabric, and Agentic Fabric.

---

## The Mental Model

Here is the simplest way to remember all of this.

| Name | What It Actually Is |
|---|---|
| **IdentityIQ** | Separate, customer-managed IGA product |
| **IdentityNow** | Original name of the cloud product |
| **ISC** | IdentityNow renamed |
| **Human Fabric** | ISC evolved, current name for the cloud product |
| **Agentic Fabric** | New product for AI agents and non-human identities |
| **Atlas** | The platform foundation underneath the cloud products |

And the product lineage for the cloud side:

```text
IdentityNow → Identity Security Cloud → Human Fabric
```

Same product. Different names. Evolving capabilities.

![SailPoint Architecture showing Human Fabric, Agentic Fabric, and Atlas](/assets/img/posts/stop-googling-isc-vs-human-fabric/sailpoint-architecture.png)
*SailPoint's official architecture. Human Fabric and Agentic Fabric sit side by side in the Control Plane, both built on top of the Atlas platform foundation.*

When you look at the official architecture, the confusion finally goes away. You can see that Human Governance and Agentic Governance are two sides of the same Control Plane, and Atlas is the engine room underneath both of them.

---

## Why This Confusion Exists

SailPoint did not do anything wrong here. Product names change as products evolve. This happens everywhere.

But the confusion exists for three reasons.

First, old names never fully disappear. API documentation still uses IdentityNow in some places. Tutorials written in 2022 still refer to ISC. The internet does not update itself.

Second, the changes happened gradually. IdentityNow became ISC in 2024. ISC became Human Fabric in 2026. If you were not paying attention during those windows, you missed the announcements.

Third, the portfolio got more complex. It used to be two products. Now it is two products, a new product for AI agents, and a platform underneath everything. That is harder to keep straight.

This is not a SailPoint-specific problem. It happens in every mature technology company.

---

## What This Means for You

If you are learning SailPoint, here is what I would recommend.

**Start with IGA fundamentals.** Identity lifecycle, authoritative sources, correlation, provisioning, access requests, certifications, roles, separation of duties. These concepts apply across all products.

**Then go deep on Human Fabric or ISC.** The cloud product is where most of the industry is heading. Learn the architecture, connectors, identity profiles, workflows, access profiles, APIs, and troubleshooting. Old ISC-era material remains useful.

**Learn IdentityIQ separately if your job requires it.** IdentityIQ has a different architecture, different customization patterns, and a different deployment model. Do not assume ISC knowledge translates directly.

**Understand Atlas conceptually.** You do not need to configure Atlas directly. You need to understand that it provides the shared services underneath Human Fabric and Agentic Fabric.

**Explore Agentic Fabric as a specialization.** AI agent governance is where the industry is going. Understanding how to discover, govern, and protect non-human identities is a valuable skill.

---

## One Thing I Got Wrong

When I first heard "Human Fabric," I assumed it was a completely new product that replaced ISC.

It is not.

It is ISC, renamed and expanded. The concepts I learned in ISC still apply. The architecture is the same. The connectors, the identity profiles, the transforms, the rules. All of it carries forward.

That was a relief.

And when I heard "Agentic Fabric," I assumed it was a feature within Human Fabric.

It is not.

It is a separate product for a separate problem. Human identities and AI agents are different kinds of identities with different governance needs. Agentic Fabric handles the AI agent side.

Understanding this distinction saved me from a lot of confusion.

---

## The Final Mental Model

If you remember only one thing from this post, remember this.

**IdentityIQ is a separate product. IdentityNow became ISC. ISC evolved into Human Fabric. Agentic Fabric is for AI agents. Atlas is the platform underneath.**

Everything else is detail.

---

## Official References

If you want to verify any of this or go deeper, here are the sources I used.

- **SailPoint Platform and Atlas:** [sailpoint.com/products/platform](https://www.sailpoint.com/products/platform)
- **Human Fabric / ISC / IdentityNow developer documentation:** [developer.sailpoint.com/docs/](https://developer.sailpoint.com/docs/)
- **Agentic Fabric documentation:** [documentation.sailpoint.com/saas/help/agentic_fabric/index.html](https://documentation.sailpoint.com/saas/help/agentic_fabric/index.html)
- **Unified Identity Security announcement (August 2026):** [sailpoint.com/press-releases/sailpoint-identity-security-solution](https://www.sailpoint.com/press-releases/sailpoint-identity-security-solution)
- **IdentityIQ official documentation:** [documentation.sailpoint.com/identityiq/help/](https://documentation.sailpoint.com/identityiq/help/)
- **SailPoint official product documentation portal:** [documentation.sailpoint.com/](https://documentation.sailpoint.com/)

---

## What's Next

I will be writing more about identity security, IAM, and IGA as I go deeper into this field. Technical deep dives, implementation patterns, and real-world challenges from working with SailPoint ISC.

I also maintain a public GitHub repository where I store transforms, rules, workflows, API examples, and configuration templates.

[https://github.com/sahilahmadofficial/sailpoint-isc-lab](https://github.com/sahilahmadofficial/sailpoint-isc-lab)

If you are also learning SailPoint or entering the IAM space, follow along.

---

📧 [hello.sahilahmad@gmail.com](mailto:hello.sahilahmad@gmail.com)  
🐙 [github.com/sahilahmadofficial](https://github.com/sahilahmadofficial)  
💼 [linkedin.com/in/sahilahmadofficial](https://linkedin.com/in/sahilahmadofficial)  

---

— Sahil Ahmad

*Identity Security &middot; IAM &middot; IGA &middot; SailPoint ISC*