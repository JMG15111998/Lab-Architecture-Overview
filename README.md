# Lab-Architecture-Overview
Shared cyber-range lab: Azure VMs + Tenable vulnerability scanning + Defender EDR. Hands-on threat hunting and remediation practice.
# cyber-range-lab

In this project, we explore a **shared cyber range lab** built on Microsoft Azure, Tenable Vulnerability Management, and Microsoft Defender for Endpoint (EDR). It’s designed to simulate **real-world attacks** (plus internal simulated ones), so students can practice threat hunting, vulnerability scanning, and incident response — in an environment that actually feels like a real network.

---

## 🧱 Architecture Overview

Unlike older courses where everyone had their own isolated Azure tenant, this lab drops all students into a **shared virtual environment**:

- One Azure subscription/tenant (managed centrally)  
- Shared vNet for all student VMs  
- Tenable scan engine deployed inside the vNet  
- Microsoft Defender for Endpoint for EDR and telemetry  
- Azure Portal access so students can manage their VMs directly

Because of this setup:

- Student VMs can technically **see and talk to each other**  
- They’re **exposed to the internet**, so real attackers will hit them  
- Logs include both **real** and **simulated** attacks

---

## 🔧 Key Components

### 💻 Student Virtual Machines

- Deployed in the shared vNet  
- Run Windows or Linux  
- Students have full **admin rights** to experiment freely

### 🛡️ Tenable Vulnerability Management

- Enterprise scan engine lives inside the lab network  
- Students run **authenticated scans** on their own VMs  
- Produces real vulnerability data for remediation practice

### 🔍 Microsoft Defender for Endpoint (EDR)

- Collects and analyzes endpoint logs  
- Supports **threat hunting via KQL** queries  
- Detects both simulated and live attack activity

### ⚠️ Attack Surfaces

- **External threats**: Real-world attackers hitting open ports  
- **Always-on targets**: VMs designed to attract and log attacks  
- **Internal attack simulator**: Deploys periodic test scenarios, including:

  - Malware  
  - Ransomware  
  - Data exfiltration  
  - Privilege escalation  

---

## 🛠️ Technology Utilized

- Azure VMs  
- Tenable Cloud Console + scan engine  
- Microsoft Defender for Endpoint (EDR)  
- PowerShell & Bash for remediation and simulation  

---

## 📚 Table of Contents

1. [Lab Architecture Explanation](#lab-architecture-explanation)  
2. [Requesting Access](#requesting-access)  
3. [Working with Tenable](#working-with-tenable)  
4. [Working with Microsoft Defender for Endpoint](#working-with-microsoft-defender-for-endpoint)  
5. [Attack Simulation](#attack-simulation)  
6. [Threat Hunting Scenarios](#threat-hunting-scenarios)  
7. [Community and Collaboration](#community-and-collaboration)  
8. [Going Beyond the Curriculum](#going-beyond-the-curriculum)

---

## 🏗️ Lab Architecture Explanation

Your VM launches inside the shared network, right alongside other students’ machines. That means:

- You’re working in a **corporate-style environment**  
- Logs and alerts feel more realistic  
- You’ll need to think about **network visibility**, not just endpoint data

This is a big step up from traditional labs where every student was isolated. It’s a more chaotic — but also more real — learning experience.

---

## 📝 Requesting Access

Before jumping in, you’ll need to:

- Accept the **EULA**  
- Request access to the Azure tenant  
- Request access to Tenable Cloud

Once onboarded, you’ll have:

- Elevated access in Azure  
- Ability to create/manage your own VMs  
- Full use of Tenable and Defender for Endpoint

---

## 🔎 Working with Tenable

You’ll get nearly full control here — just like an enterprise environment:

- Run authenticated scans  
- Download results  
- Dive into advanced features outside the core curriculum

Treat Tenable as your personal **vulnerability lab** — test, break, fix, repeat.

---

## 🧠 Working with Microsoft Defender for Endpoint

EDR is your main tool for detection and response:

- Query logs using **KQL**  
- Investigate attack timelines  
- Practice real-world threat hunting

Once you get the hang of Defender, transitioning to other tools (CrowdStrike, SentinelOne, etc.) is way easier — they all follow similar logic.

---

Attack Simulation

The lab includes an **attack simulator service** that runs regularly to keep logs flowing:

- Malware drops  
- Ransomware triggers  
- Data exfiltration tests  
- Privilege escalation attempts

Combined with **real-world attackers** scanning your public IPs, this gives you a rich stream of data to work with.

---

Threat Hunting Scenarios

- Both simulated and real attacks are in play  
- Students create and contribute **custom threat hunting challenges**  
- These are added to the simulator over time — so it gets smarter as the course evolves

---

Community and Collaboration

To qualify for the **Internship portion**, students must:

- Reach **Level 3** in the lab’s community forum  
- Help others, share discoveries, and stay active

This encourages the kind of collaboration you’d see in a real SOC — where junior analysts help each other grow.

---

Going Beyond the Curriculum

Once you’ve mastered the basics, push further:

- Build your own simulated attacks  
- Experiment with different OS versions and setups  
- Share what you’ve learned

This is more than a lab — it’s your **sandbox** to explore cybersecurity creatively.

---

Why This Matters

After completing this lab, you’ll have:

- Hands-on Azure cloud admin skills  
- Enterprise-level vulnerability management experience  
- Confidence working with an EDR platform  
- A foundation for tools like CrowdStrike, Rapid7, or AWS-native security tools

