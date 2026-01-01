# TryHackMe – OWASP Top 10 2025: IAAA Failures

## 🧠 Room Overview
This room explains failures related to **Identity, Authentication,
Authorisation, and Accountability (IAAA)** as defined in the
OWASP Top 10:2025.

The following categories are covered:
- **A01: Broken Access Control**
- **A07: Authentication Failures**
- **A09: Logging & Alerting Failures**

This room is designed for beginners and requires no prior security knowledge.

---

## 🔐 What is IAAA?
IAAA stands for:
- **Identity** – Identifying a user (user ID, email)
- **Authentication** – Proving that identity (password, OTP)
- **Authorisation** – What the user is allowed to do
- **Accountability** – Logging and monitoring user actions

Failures in IAAA can lead to data leakage and privilege escalation.

---

## 🟥 A01: Broken Access Control

### 📌 Explanation
Broken Access Control occurs when the server does not properly enforce
authorization checks on every request.

A common example is **IDOR (Insecure Direct Object Reference)**, where
changing an ID in the URL allows access to another user's data.

### 🧪 Lab Result
- Privilege escalation type: **Horizontal**
- Flag:

THM{Found.the.Millionare!}


---

## 🟧 A07: Authentication Failures

### 📌 Explanation
Authentication failures occur when an application cannot reliably verify
a user's identity.

Common causes include:
- Username confusion
- Weak authentication logic
- Poor session handling

### 🧪 Lab Result
- Admin dashboard flag:

THM{Account.confusion.FTW!}


---

## 🟨 A09: Logging & Alerting Failures

### 📌 Explanation
When applications do not log or alert on security-relevant events,
it becomes difficult to detect or investigate attacks.

### 🧪 Investigation Findings
- Attacker IP address: `203.0.113.45`
- Compromised account: `admin`
- Accessed endpoint:

/supersecretadminstuff


---

## ✅ Key Takeaways
- Access control must be enforced on the server side
- Authentication systems must prevent user confusion
- Proper logging is essential for accountability and incident response

---

## 📅 Status
Completed ✔
