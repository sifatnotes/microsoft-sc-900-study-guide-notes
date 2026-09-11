# microsoft-sc-900-study-guide-notes
Complete community study guide, revision notes, practice tips, and resources for the Microsoft SC-900: Security, Compliance, and Identity Fundamentals certification exam.
# Microsoft SC-900: Security, Compliance, and Identity (SCI) Fundamentals Study Guide

Welcome to the ultimate community-driven study guide for the **Microsoft Exam SC-900: Security, Compliance, and Identity Fundamentals**. 

Whether you are an aspiring IT administrator, cloud architect, business stakeholder, or security specialist, this repository is designed to give you a clear, practical, and highly detailed roadmap to passing the SC-900 exam on your first attempt.

---

## 📌 Exam Overview

The **SC-900** exam evaluates your fundamental knowledge of security, compliance, and identity (SCI) concepts across cloud-based and related Microsoft services.

* **Exam Name:** Microsoft Certified: Security, Compliance, and Identity Fundamentals
* **Exam Code:** SC-900
* **Question Count:** ~40–60 questions
* **Format:** Multiple choice, multiple response, drag-and-drop, build list
* **Passing Score:** 700 / 1000
* **Duration:** 45 minutes (exam length) / 60 minutes total seating time
* **Prerequisites:** None (entry-level certification)

---

## 🎯 Who Should Take This Exam?

- **Beginners in Cybersecurity:** Individuals looking to build a foundation in modern cloud security architecture.
- **IT Professionals & Admins:** System and network admins transitioning into security roles or looking to understand Microsoft Entra ID and Defender.
- **Business Stakeholders & Sales Engineers:** Professionals who handle software procurement, compliance auditing, or technology consulting and need to speak the language of cloud security.
- **Students & Career Changers:** Anyone preparing to enter the cloud ecosystem with a credential from Microsoft.

---

## 📊 Exam Objectives & Domain Breakdown

The SC-900 exam measures skills across four core domains:

| Domain | Weightage |
| :--- | :--- |
| **Describe the concepts of security, compliance, and identity** | 10–15% |
| **Describe the capabilities of Microsoft Entra** | 25–30% |
| **Describe the capabilities of Microsoft security solutions** | 25–30% |
| **Describe the capabilities of Microsoft compliance solutions** | 20–25% |

---

## 🧠 Detailed Study Notes & Important Concepts

### Domain 1: Concepts of Security, Compliance, and Identity (10–15%)

#### Core Concepts & Principles
* **Shared Responsibility Model:**
  * **On-Premises:** You manage everything (Physical datacenter, hardware, OS, network, data, apps, identity).
  * **IaaS (Infrastructure as a Service):** Microsoft manages physical facilities, host hardware, and network infrastructure. You manage OS, network configurations, applications, and data.
  * **PaaS (Platform as a Service):** Microsoft manages OS and runtime environments. You focus on application code and data.
  * **SaaS (Software as a Service):** Microsoft manages everything end-to-end except your **data, identities, devices, and access policies** (which always remain your responsibility).
* **Defense-in-Depth:**
  * A layered defense approach (Physical → Identity & Access → Perimeter → Network → Compute → Application → Data). If one layer fails, subsequent layers prevent exposure.
* **Zero Trust Model:**
  * Guiding mantra: *"Never trust, always verify."*
  * **Three Core Pillars:**
    1. *Verify explicitly:* Always authenticate and authorize based on all available data points (user location, device health, service, workload).
    2. *Use least privilege access:* Limit user access with Just-In-Time (JIT) and Just-Enough-Access (JEA), Risk-Based Adaptive Policies, and Data Protection.
    3. *Assume breach:* Minimize blast radius by segmenting access, encrypting end-to-end communications, and monitoring real-time diagnostics.
* **CIA Triad:**
  * **Confidentiality:** Keeping sensitive data private (Encryption, RBAC).
  * **Integrity:** Ensuring data is not altered or tampered with (Hashing, Digital Signatures).
  * **Availability:** Ensuring systems and data are accessible when needed (Redundancy, Backups, DDoS Protection).
* **Encryption & Hashing:**
  * **Symmetric Encryption:** Same key used for encryption and decryption (e.g., AES).
  * **Asymmetric Encryption:** Public key encrypts, Private key decrypts (e.g., RSA).
  * **Hashing:** One-way mathematical transformation (e.g., SHA-256). Used for verifying message integrity and storing password hashes.

---

### Domain 2: Microsoft Entra Capabilities (25–30%)

Microsoft Entra is Microsoft’s suite of identity and network access solutions (formerly Azure AD).

#### Key Components
* **Microsoft Entra ID:** Cloud-based identity and access management (IAM) service.
* **Identity Types:**
  * **User Identities:** Employee and guest accounts.
  * **Service Principals:** Application objects that require access to resources.
  * **Managed Identities:** Automatically managed credentials for Azure services to authenticate to other cloud resources without storing passwords in code.
  * **Workload Identities:** Non-human identities like applications, service principals, and managed identities.
* **Hybrid Identity:**
  * Synchronizing on-premises Active Directory Domain Services (AD DS) with Microsoft Entra ID using tools like **Microsoft Entra Connect Sync / Cloud Sync**.
* **Authentication & Access Management:**
  * **Multifactor Authentication (MFA):** Requires 2 or more factors: *Something you know* (password), *Something you have* (authenticator app/security key), *Something you are* (biometrics).
  * **Self-Service Password Reset (SSPR):** Enables users to reset their passwords without IT helpdesk intervention.
  * **Conditional Access:** The policy engine for Zero Trust. Evaluates signals (User, Location, Device, Application, Real-time Risk) to enforce controls (*Allow*, *Block*, or *Require MFA*).
* **Identity Protection & Governance:**
  * **Microsoft Entra ID Governance:** Manages access lifecycles using access packages, entitlement management, and periodic **Access Reviews**.
  * **Privileged Identity Management (PIM):** Provides time-bound, just-in-time (JIT) administrative access with approval workflows and audit logs to reduce standing privileges.
  * **Microsoft Entra Permissions Management:** A Cloud Infrastructure Entitlement Management (CIEM) solution that gives visibility into permissions across Azure, AWS, and GCP.

---

### Domain 3: Microsoft Security Solutions (25–30%)

#### Infrastructure & Network Security in Azure
* **Network Security Groups (NSGs):** Filter inbound and outbound traffic to Azure Virtual Network resources by IP, port, and protocol.
* **Azure Firewall:** A stateful, fully managed cloud-native firewall providing layer 3 to layer 7 network protection.
* **Azure Web Application Firewall (WAF):** Protects web apps from common exploits (e.g., SQL injection, cross-site scripting) at Layer 7.
* **Azure Bastion:** Provides secure, seamless RDP/SSH access to VMs directly through the Azure portal via TLS, without exposing public IP addresses.
* **Azure Key Vault:** Centralized secure store for keys, secrets, certificates, and passwords.

#### Microsoft Defender XDR & Defender for Cloud
* **Microsoft Defender XDR:** Integrated suite protecting enterprise environments across endpoints, identity, email, and cloud apps.
  * **Defender for Endpoint:** Endpoint Detection and Response (EDR) for client devices and servers.
  * **Defender for Identity:** Monitors on-premises Active Directory signals to identify compromised accounts and insider threats.
  * **Defender for Office 365:** Protects email and collaboration tools against advanced threats, phishing, and business email compromise (BEC).
  * **Defender for Cloud Apps:** Cloud Access Security Broker (CASB) offering shadow IT discovery, data protection, and threat prevention across cloud apps.
* **Microsoft Defender for Cloud:**
  * **Cloud Security Posture Management (CSPM):** Continuously assesses configuration vulnerabilities and measures posture via **Secure Score**.
  * **Cloud Workload Protection (CWP):** Provides threat protection for workloads across Azure, AWS, GCP, and hybrid environments.

#### Microsoft Sentinel
* **SIEM (Security Information and Event Management):** Collects, aggregates, and analyzes security log data across the enterprise.
* **SOAR (Security Orchestration, Automation, and Response):** Automates incident response playbooks to resolve threats rapidly.
* **Microsoft Sentinel:** Microsoft's cloud-native SIEM and SOAR solution for scalable, enterprise-wide security analytics.

---

### Domain 4: Microsoft Compliance Solutions (20–25%)

#### Microsoft Purview Ecosystem
* **Microsoft Purview Portal:** Unified portal for data governance, risk management, and compliance solutions.
* **Compliance Manager & Compliance Score:** Measures an organization’s compliance posture against regulatory frameworks (e.g., GDPR, ISO 27001, HIPAA) and offers actionable improvements.

#### Information Protection & Data Governance
* **Data Classification:** Categorizes data based on type (Sensitive info types, trainable classifiers).
* **Sensitivity Labels:** Applies protection controls (encryption, watermarking, access restrictions) directly to files and emails based on sensitivity level.
* **Data Loss Prevention (DLP):** Prevents unauthorized sharing or leakage of sensitive data (e.g., credit card numbers, SSNs) outside the organization.
* **Retention Policies & Retention Labels:** Manages the lifecycle of content by automatically retaining data for required compliance windows or deleting it when no longer needed.

#### Risk & Compliance Capabilities
* **Insider Risk Management:** Uses machine learning signals to identify suspicious internal user activity (e.g., data theft before resignation, policy violations).
* **eDiscovery:** Facilitates legal discovery by identifying, preserving, and exporting electronic data for litigation or investigations.
* **Audit (Standard & Premium):** Tracks user and administrator activity logs for regulatory and operational auditing.

---

## 🛠️ Practical Hands-on Exercises (Labs)

To truly retain these concepts, log into a free or developer Azure account and complete these 4 labs:

1. **Configure Microsoft Entra Conditional Access:**
   * Go to Microsoft Entra ID → *Protection* → *Conditional Access*.
   * Create a mock policy that requires MFA for all users attempting to access the Azure Portal from outside trusted locations.
2. **Review Secure Score in Defender for Cloud:**
   * Navigate to *Microsoft Defender for Cloud* in the Azure Portal.
   * Open the *Recommendations* tab, inspect your overall Secure Score, and analyze top security recommendations.
3. **Set Up a Sensitivity Label in Microsoft Purview:**
   * Access the *Microsoft Purview Portal*.
   * Create a Sensitivity Label named `Confidential - Finance`, enable encryption, and test applying it to a sample document.
4. **Deploy Microsoft Sentinel Workspace:**
   * Search for *Microsoft Sentinel* in Azure.
   * Create a Log Analytics workspace and connect a free data connector (such as Azure Activity logs or Entra ID diagnostic settings).

---

## 📅 30-Day Study Plan
