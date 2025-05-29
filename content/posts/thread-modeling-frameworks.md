+++
date = '2025-05-29T07:24:47-04:00'
draft = false
title = 'Threat Modelling: How to make PASTA in Stride'
tags = ["threat modelling"]
+++

# Threat Modelling: How to Make PASTA in STRIDE

## 🍝 What Is Threat Modelling (and Why Should You Care)?

Imagine you're building a castle. You’ve got walls, a moat, and maybe even a dragon. But how do you know where the weak spots are? That’s where **threat modelling** comes in.

In the world of secure software and IT systems, threat modelling is your blueprint for identifying potential threats *before* the bad guys do (or before good guys unintentionally create them). It’s a structured way to ask:  
- What are we building?  
- What could go wrong?  
- What are we doing about it?

It’s not just a checkbox for compliance—it’s your early warning system, your security strategy, and your best friend when things get complicated.

---

## ⏰ When Should You Do Threat Modelling?

Short answer: **early and (reasonably)often**.

Long answer: Ideally, you start during the design phase—before a single line of code is written. But it’s never too late. Whether you’re launching a new feature, integrating a third-party service, or just doing a security review (for many places this is done quarterly), threat modelling helps you stay ahead of the curve.

---

## 🧩 Frameworks Galore: PASTA, STRIDE, and DREAD

Okay, time to enter acronym hell, something that engineers and security professionals alike dread, yet somehow insist on continuing to use?! The good news is that you don't need to do all of these all the time. I'll show you how to be selective and use the right framework for the right job. Bear with me, it'll be over soon.

### 🥫 PASTA: Process for Attack Simulation and Threat Analysis

Think of PASTA as the gourmet, seven-layer lasagna of threat modelling. It’s a **risk-centric** framework that consists of the following steps:

1. Define business objectives  
2. Define the technical scope  
3. Decompose the application  
4. Analyze threats  
5. Analyze vulnerabilities  
6. Model attacks  
7. Assess risk and impact

**Use PASTA when**:  
You need a deep-dive, business-aligned threat model—especially for complex systems or high-risk environments.

---

### 🏃 STRIDE: Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege

STRIDE is your quick-and-dirty checklist for identifying threats based on system components. It’s **developer-friendly** (no surprise, coming from Microsoft) and maps well to data flow diagrams.

**Use STRIDE when**:  
You want a fast, structured way to brainstorm threats during design or code reviews. In a lot of my work, this has been the bread and butter (ok, too many food analogies here) of thread modelling.

---

### 😱 DREAD: Damage, Reproducibility, Exploitability, Affected Users, Discoverability

DREAD is a scoring system to **prioritize** threats based on risk. It’s like Yelp for vulnerabilities—except instead of stars, you’re rating how damaging a threat could be.

**Use DREAD when**:  
You’ve identified threats already and need to rank them to decide what to fix first.

---

## 🧪 Real-World Example: Enterprise Document Management System (DMS)

Let’s say your company is building an internal **Document Management System** for storing, sharing, and collaborating on sensitive documents—think contracts, financial reports, and HR files. It integrates with Active Directory, supports role-based access, includes audit logging, and strong encryption at rest (more on this some other day).

Here’s how each framework might come into play:

### 🏃 Using STRIDE

You create a data flow diagram:
- Users authenticate via SSO  
- Upload/download documents  
- Share documents with colleagues  
- Admins manage permissions

Now apply STRIDE:
- **Spoofing**: Can someone impersonate a user or admin?  
- **Tampering**: Can someone alter documents or audit logs?  
- **Repudiation**: Can users deny uploading or modifying a file?  
- **Information Disclosure**: Are confidential documents exposed to unauthorized users?  
- **Denial of Service**: Can someone flood the system with large uploads or requests?  
- **Elevation of Privilege**: Can a regular user gain admin access?

They shouldn't be able to do any of these.

---

### 🍝 Using PASTA

You go deeper:
- **Business objectives**: Ensure secure, compliant document storage and collaboration  
- **Technical scope**: Web app, backend API, cloud storage, SSO integration  
- **Threats**: Insider threats, unauthorized access, data leakage, ransomware  
- **Attack simulation**: A compromised user account uploads malware or exfiltrates sensitive files  
- **Risk assessment**: High impact on compliance, legal exposure, and operational continuity
PASTA helps you align security with business risk and simulate real-world attack paths.

---

### 🔥 Using DREAD

You’ve identified several threats:
- Insider data exfiltration  
- Compromised admin account  
- Misconfigured access controls

Now you score them:
- **Damage**: Could this lead to regulatory fines or data breaches?  
- **Reproducibility**: Can the attack be repeated easily?  
- **Exploitability**: How hard is it to pull off?  
- **Affected Users**: Is it one department or the whole company?  
- **Discoverability**: Would an attacker easily find this vulnerability

---

## 📝 Final Thoughts

Admittedly, I've painted a picture of successively applying each and all of these frameworks. That was more to show how they all fit together and not a signal to use all of these, all the time. Rather, you'll want to use the right tool for the right job. I've found teams that I've worked on to often use the simpler models for the "bread and butter" designs and features, and a more comprehensive approach like the above for more complex and high risk/complexity designs, especially when there's a lot at stake. 

Now go make some PASTA! (Don't ask me why such a delightful food should be the symbol of intense risk-focused thread modelling, but it is :).




