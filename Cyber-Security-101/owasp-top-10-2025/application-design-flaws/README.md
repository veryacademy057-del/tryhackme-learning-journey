# TryHackMe – OWASP Top 10 2025: Application Design Flaws

## 🧠 Room Overview
This room focuses on **application design and architecture failures**
as defined in the **OWASP Top 10:2025**.

Rather than code-level bugs, these vulnerabilities arise from
**poor design decisions, unsafe defaults, weak assumptions, and flawed system architecture**.
The room combines theory with hands-on challenges.

### Categories Covered
- **AS02: Security Misconfigurations**
- **AS03: Software Supply Chain Failures**
- **AS04: Cryptographic Failures**
- **AS06: Insecure Design**

---

## 🟥 AS02: Security Misconfigurations

### 📌 Description
Security misconfigurations occur when systems are deployed with:
- Unsafe default settings
- Exposed services or APIs
- Verbose error messages
- Misconfigured permissions

These are environment or configuration mistakes rather than code flaws.

### 🌍 Real-World Example
In 2017, Uber exposed sensitive user data due to a publicly accessible
AWS S3 bucket, demonstrating how a single misconfiguration can cause a major breach.

### 🧪 Lab Result
- Issue: **Verbose error messages leaking internal API details**
- Flag:

THM{V3RB0S3_3RR0R_L34K}


### 🛡️ Prevention
- Harden default configurations
- Restrict exposed services
- Hide stack traces
- Regularly audit cloud permissions

---

## 🟧 AS03: Software Supply Chain Failures

### 📌 Description
Supply chain failures occur when applications depend on:
- Outdated libraries
- Unverified third-party components
- Compromised build or update pipelines

Attackers exploit trusted dependencies rather than the application itself.

### 🌍 Real-World Example
The **SolarWinds (2021)** attack demonstrated how malicious code embedded
into trusted updates can compromise thousands of organizations.

### 🧪 Lab Result
- Vulnerable component: outdated `vulnerable_utils.py`
- Flag:

THM{SUPPLY_CH41N_VULN3R4B1L1TY}


### 🛡️ Prevention
- Verify and monitor dependencies
- Secure CI/CD pipelines
- Sign and audit software updates
- Track component provenance

---

## 🟨 AS04: Cryptographic Failures

### 📌 Description
Cryptographic failures occur when encryption is:
- Weak
- Misused
- Hard-coded
- Missing entirely

These failures can expose sensitive data such as passwords, keys, or tokens.

### 🧪 Lab Result
- Issue: **Hard-coded cryptographic key**
- Flag:

THM{CRYPTO_FAILURE_H4RDCOD3D_K3Y}


### 🛡️ Prevention
- Use modern encryption standards (AES-GCM, TLS 1.3)
- Implement proper key management
- Rotate secrets regularly
- Avoid hard-coded credentials

---

## 🟦 AS06: Insecure Design

### 📌 Description
Insecure design refers to **fundamental architectural flaws**
that cannot be fixed with patches.

These often result from:
- Missing threat modeling
- Weak business logic assumptions
- Blind trust in AI or automation systems

### 🧠 Insecure Design in the AI Era
Modern systems increasingly rely on AI, introducing new risks such as:
- Prompt injection
- Poisoned models
- Unvalidated AI decisions

### 🧪 Lab Result
- Flawed assumption: only mobile devices could access the system
- Flag:

THM{1NS3CUR3_D35IGN_4SSUMPT10N}


### 🛡️ Secure Design Principles
- Perform threat modeling early
- Apply least privilege
- Validate all inputs and outputs
- Require human review for high-risk actions
- Treat AI systems as untrusted by default

---

## ✅ Key Takeaways
- Security must be designed from the start, not added later
- Defaults, dependencies, and design assumptions are common attack vectors
- Strong foundations reduce long-term security risk

---

## 📅 Status
Room completed ✔
