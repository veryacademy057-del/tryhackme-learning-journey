# OWASP Top 10 2025 – Insecure Data Handling  
## TryHackMe Learning Journey

This repository documents my learning progress on **TryHackMe** through the room  
**OWASP Top 10 2025: Insecure Data Handling**.

This room focuses on vulnerabilities related to **application behavior and how applications process user input and data**, including design and implementation flaws that can lead to data leakage, unauthorized command execution, and system manipulation.

---

## 🎯 Room Overview

- **Platform**: TryHackMe  
- **Room Name**: OWASP Top 10 2025 – Insecure Data Handling  
- **Level**: Beginner  
- **Module**: Cyber Security 101  

### OWASP Top 10 Categories Covered:
- **A04** – Cryptographic Failures  
- **A05** – Injection  
- **A08** – Software or Data Integrity Failures  

---

## 🧠 Learning Objectives

After completing this room, I learned about:

- What **Insecure Data Handling** is and its impact on application security
- Cryptographic failures caused by weak algorithms or improper implementations
- How **Injection attacks** work, especially **Server Side Template Injection (SSTI)**
- Risks related to **Software & Data Integrity Failures**, including **Insecure Deserialization**
- The importance of input validation, trust boundaries, and data integrity in applications

---

## 🧪 Task Summary & Flags

### 🔐 Task 2 – A04: Cryptographic Failures
**Description:**  
The application stores sensitive data using weak cryptographic mechanisms and a shared key.

**Practical:**
- Accessing a note-sharing application
- Decrypting encrypted notes
- Retrieving a hidden flag

**Flag:**

THM{WEAK_CRYPTO_FLAG}


---

### 💉 Task 3 – A05: Injection (SSTI)
**Description:**  
The application fails to properly validate user input and is vulnerable to **Server Side Template Injection**.

**Practical:**
- Exploiting an SSTI vulnerability
- Reading the `flag.txt` file on the server

**Flag:**

THM{SSTI_FLAG_OBTAINED}


---

### 📦 Task 4 – A08: Software or Data Integrity Failures
**Description:**  
The application processes serialized data without validation, leading to **Insecure Deserialization**.

**Practical:**
- Creating a malicious Python pickle payload
- Executing the payload to read a sensitive file

**Flag:**

THM{INSECURE_DESERIALIZATION}


---

## 🛡️ Mitigation & Prevention

### A04 – Cryptographic Failures
- Use modern and secure algorithms (bcrypt, Argon2, AES)
- Avoid implementing custom cryptographic algorithms
- Never store credentials in source code or repositories

### A05 – Injection
- Use prepared statements and parameterized queries
- Perform proper input validation and sanitization
- Avoid passing user input directly to shells or template engines

### A08 – Software or Data Integrity Failures
- Verify the integrity of updates and data (checksums, signatures)
- Never process serialized data from untrusted sources
- Apply security controls within CI/CD pipelines

---

## 📚 Recommended TryHackMe Rooms

- Cryptographic Failures Module  
- Injection Attacks Module  
- Command Injection  
- Insecure Deserialization  
- Supply Chain Attack: Lottie  

---

## 🧭 Learning Progress

This repository is part of my **cybersecurity learning journey** and will be continuously updated as I complete more TryHackMe rooms.

> All write-ups are created **for educational and personal learning purposes only**.

---

