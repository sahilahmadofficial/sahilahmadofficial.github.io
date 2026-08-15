---
title: "What Is Identity Security, IAM, and IGA (And Why I'm Learning It)"
date: 2026-08-15 10:00:00 +0530
categories: [IAM, SailPoint]
tags: [identity-governance, iam, iga, sailpoint, cybersecurity, learning]
description: "What Identity Security, IAM, and IGA are, why they matter, and why I'm learning it."
image:
  path: /assets/img/posts/what-is-identity-security-iam-iga/cover.jpg
  alt: "A complex network of interconnected identities and access flows"
pin: false
---

Identity is the new perimeter.

That phrase gets repeated so often it's almost lost its meaning. But it's true.

The old model of securing the network boundary doesn't work anymore. Everything is in the cloud. Employees work from anywhere. Contractors come and go. Applications live across multiple environments.

In this world, the only thing that matters is who has access to what.

That's where Identity Security comes in.

Six months ago, I had no idea what any of this meant. I barely knew what IAM stood for. If someone had asked me about access certifications, I would have stared at them blankly.

Now I spend my days in SailPoint Identity Security Cloud. I work with provisioning, access reviews, role-based access control, and separation of duties.

But I remember what it felt like to not understand any of this. So here's what I've learned. No jargon. No fluff. Just the problem, the solution, and why I'm in this space.

---

## What Is Identity Security?

Identity Security is the practice of ensuring that the right people have access to the right things at the right time, and that they lose that access when they no longer need it.

It sounds simple. It's not.

In a modern enterprise, there are thousands of employees. Each employee needs access to dozens of systems. Email, databases, HR portals, finance applications, cloud services. The list never ends.

Managing who has access to what, why they have it, and whether they should still have it is one of the most underestimated problems in enterprise security.

Get it wrong and you get breaches like the MGM Casino attack in 2023. Attackers exploited identity and access management failures to take down a billion-dollar operation. Not sophisticated hacking. Not zero-day exploits. Just poor identity governance.

Get it right and you have a provable, auditable, compliant identity programme. Auditors are happy. Attackers are out. The business keeps running.

---

## What Is IAM and IGA?

This confused me for a long time.

**Identity and Access Management (IAM)** is the foundation. It handles authentication (who you are) and authorization (what you can do). It's the plumbing.

**Identity Governance and Administration (IGA)** is the discipline built on top of it. It adds policies, compliance, audit trails, and lifecycle automation.

Think of it this way.

IAM says: "Yes, you can log in."

IGA says: "You should only have access to exactly what you need, no more, and here's the proof."

IAM is the engine. IGA is the steering wheel, the brakes, and the dashboard. You need both.

Together, they form Identity Security.

---

## The Three Problems IGA Solves

### The Joiner Problem

A new employee joins the company. They need access to fifteen systems before their first day.

Without IGA, IT manually creates accounts across every system. It takes days. Some systems get missed. The new employee sits idle waiting for access.

With SailPoint, the moment HR creates the employee record, SailPoint detects the new identity, evaluates their role and department, and automatically provisions the correct access across all connected systems. Done before they walk in the door.

### The Mover Problem

An employee moves from Finance to Marketing. Their Finance access should be removed. Their Marketing access should be granted.

Without IGA, this rarely happens cleanly. Old access accumulates over time. This is called privilege creep. It's a massive security risk.

With SailPoint, the role change triggers the removal of old access and provisioning of new access. Everything is adjusted automatically.

### The Leaver Problem

An employee resigns or is terminated. Every account across every system must be disabled immediately.

Without IGA, IT tries to remember every system the person had access to. Accounts get missed. Orphaned accounts sit active for months.

With SailPoint, the termination triggers immediate revocation of all access across all systems. Complete in seconds. Provable to auditors.

These three problems, joiner, mover, and leaver, are the core of identity lifecycle management. Solve them well and most of your identity governance problems disappear.

---

## What Is SailPoint?

SailPoint is the market leader in enterprise Identity Governance and Administration. Founded in 2005, it is used by Fortune 500 companies, banks, hospitals, and government agencies globally.

Two main products:

**SailPoint Identity Security Cloud (ISC)** is cloud-based SaaS. API-first architecture. This is what I work with.

**SailPoint IdentityIQ (IIQ)** is on-premise. Highly customisable. Still widely deployed in large enterprises.

I focus on ISC. It's modern, cloud-native, and where the industry is headed.

---

## Why I'm Learning This

Identity security is where automation, security, cloud, and business processes converge. That convergence is exactly what interests me.

I've earned my SailPoint Identity Security Leader certification and completed Introduction to Identity Security Cloud.

The IAM/IGA space is undersupplied with skilled professionals. Companies like Deloitte, Accenture, IBM Security, and TCS Digital Security actively hire SailPoint engineers. The demand is global and growing.

More than that, it's genuinely interesting. It's complex. It matters. And I enjoy it.

---

## What's Next

This is just the beginning.

I'll be writing more as I go deeper into identity security. Technical deep dives. Implementation patterns. Real-world challenges. Things I learn while working with SailPoint ISC.

I also maintain a public GitHub repository, `sailpoint-isc-lab`, where I store transforms, rules, workflows, API examples, and configuration templates. Everything I learn goes there.

If you're also learning SailPoint or entering the IAM space, follow along.

---

## Resources to Start Learning

- **SailPoint University** — [university.sailpoint.com](https://university.sailpoint.com) — free official courses
- **SailPoint Developer Portal** — [developer.sailpoint.com](https://developer.sailpoint.com) — API docs + free tenant
- **SailPoint Compass Community** — [community.sailpoint.com](https://community.sailpoint.com)
- **My GitHub** — [github.com/sahilahmadofficial/sailpoint-isc-lab](https://github.com/sahilahmadofficial/sailpoint-isc-lab)

---

📧 [hello.sahilahmad@gmail.com](mailto:hello.sahilahmad@gmail.com)  
🐙 [github.com/sahilahmadofficial](https://github.com/sahilahmadofficial)  
💼 [linkedin.com/in/sahilahmadofficial](https://linkedin.com/in/sahilahmadofficial)  

---

— Sahil Ahmad

*Identity & Access Management | SailPoint ISC | Linux · Python · Automation*