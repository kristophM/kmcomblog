+++
date = '2025-05-29T08:16:40-04:00'
draft = false
title = "Everybody's Outsourcin': Manage IT supply chain risk"
tags = ["outsourcing", "supply chain risk management", "scrm", "security", "privacy"]
+++


In today’s reality, **outsourcing isn’t just a trend—it’s the norm**. From cloud services to code libraries, from hardware manufacturing to AI model training, organizations are increasingly relying on third parties to perform work, handle data, and provide services as fundamental as infrastructure and as high level as data analysis.

But here’s the kicker: **every link in your supply chain is a potential attack vector**. And with the rise of AI, automation, and globalized tech ecosystems, the risks are multiplying faster than ever.

So let’s talk about it. What’s the risk? What can go wrong? And how can you stay ahead of the curve?

---

## What’s the Risk?

Today, we're going to focus mostly on software supply chain risk. Yes, plenty of risks exist with supply chain attacks and geopolitics on electronic components, but we'll save hardware SCRM and silicon root of trust (RoT) for another day. Specifically, we're going to focus on how **security** and **privacy** can be impacted by outsourcing.

When you outsource, you extend your **trust boundary**. That means you're not just trusting your own security practices—you’re trusting your vendors’, their vendors’, and sometimes even *their* vendors’ (queue image of robot babushka dolls now!). This creates a sprawling, often opaque network of dependencies.

And attackers know it.

Supply chain attacks can be stealthy, scalable, and devastating, and sometimes not even malicious (i.e. unintentional)--which is why you need to plan ahead.

---

## Real-World Examples

- **SolarWinds (2020):** Attackers inserted malicious code into a software update, compromising thousands of organizations, including U.S. government agencies.
- **Log4Shell (2021):** A vulnerability in a widely used Java logging library exposed countless systems to remote code execution.
- **CCleaner (2017):** A trusted software tool was compromised at the source, distributing malware to millions of users.

These weren’t flukes. They were **strategic, supply chain-based attacks**—and they’re becoming more common.

---

## Software Supply Chains: The Hidden Maze

Software supply chains are notoriously complex. You’re probably using **open-source libraries**, **third-party APIs**, and **cloud-based services**—and each one is a potential risk.

### Enter: SBOM

A **Software Bill of Materials (SBOM)** is like a nutrition label for your code. It lists all the components, libraries, and dependencies in your software. With an SBOM, you can:

- Identify vulnerable components
- Track updates and patches
- Respond faster to zero-days

Think of it as **visibility meets accountability**. When working with new vendors, you can request an SBOM and use it to understand the risk profile of the software you're using, and even create one for your own IT systems. Creating an SBOM is valuable but can be a pain, so 3rd party tools such as [BlackDuck](https://www.blackduck.com/) exist to help automate this (not an endorsement and I'm not afiliated at the time of writing).

![SBOM](/images/posts/sbom-screenshot.png)
> An example of an SBOM in JSON format, following the SPDX standard

---

## Security: Give them the benefit of the doubt, but DYDD

Supply chain security means:

- **Vendor vetting**: Do they follow secure development practices?
- **Contractual controls**: Are SLAs and security requirements clearly defined?
- **Continuous monitoring**: Are you watching for changes in risk posture?

And don’t forget **incident response**. If a vendor gets breached, how fast can you isolate and recover?

Once you have identified your IT supply chain, which remember, is not only your vendors, but also your vendors' vendors, and so on, 
you'll want to establish minimum security requirements for each link in the chain. This minimum requirement should be based on their 
ability to meet your existing security policy. You should be also ensuring that they are in turn responsible and accountable
for the next link in the chain as well. Do this at regular intervals. 

Assuming that you have started to do this as early as possible when getting to know a new vendor, the first step would be to issue
your own SLR (Service Level Requirements), to clearly define what your requirements are, not just for security, but for data handling
(more on that below), and performance/business requirements as well. Once an agreement is reached, make sure this is documented
in the SLA (Service Level Agreement) that starts your relationship with them.

---

## Privacy: Who’s Handling Your Data?

Wait! We've been focused on security this whole time, but what about privacy? With GDPR, CCPA, and other privacy regulations becoming
really seriously enforced, you need to make sure that your vendors are compliant with your own privacy policy even if you are.

Outsourcing often means **data sharing**. That raises big questions:

- Where is the data stored?
- Who has access?
- Is it encrypted in transit and at rest?
- Are privacy laws (like GDPR or CCPA) being followed?

Privacy isn’t just a legal checkbox—it’s a trust issue. We'll get into GDPR controls for data sub contractors in a future post, but 
for now, no what your regulatory requirements and internal security policy are when it comes to data handling, and ensure that 
your vendors are at least on the same level. And then go down the chain. Most vendors will either publish relevant reports 
on their data subcontractors in their trust centre, or be able to provide such info upon request. 

---

## How to Analyze and Identify Risk

Here’s a quick-start checklist:

1. **Map your supply chain**: Know who your vendors are—and who *their* vendors are.
2. **Assess criticality**: What would happen if this vendor failed or was compromised?
3. **Evaluate controls**: What security measures are in place?
4. **Monitor continuously**: Risk isn’t static. Stay updated.
5. **Plan for failure**: Have a backup plan. Always. (We'll cover this in a future post)

---

## Final Thoughts

Outsourcing is here to stay. AI is accelerating it. And the supply chain is now a **frontline battlefield** in cybersecurity.

But with the right mindset, tools, and practices, you can turn your supply chain from a liability into a strength.
