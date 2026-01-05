OWASP Top 10 2025 – Insecure Data Handling
Overview

This repository documents my learning progress from the TryHackMe – Cyber Security 101 learning path, specifically covering OWASP Top 10 (2025): Insecure Data Handling.

In this room, I explored vulnerabilities related to application behaviour, user input handling, and data protection, including hands-on exploitation scenarios.

Covered OWASP Categories

A04: Cryptographic Failures

A05: Injection

A08: Software or Data Integrity Failures

Task 1 – Introduction

This room introduces three OWASP Top 10 (2025) categories related to insecure data handling.
Each section includes:

Concept explanation

Mitigation strategies

Practical exploitation using a vulnerable web application

Environment setup was performed using:

TryHackMe AttackBox

Deployed target virtual machines

Task 2 – A04: Cryptographic Failures
Description

Cryptographic failures occur when sensitive data is improperly protected due to:

Weak or outdated cryptographic algorithms (e.g. MD5, SHA1, DES)

Plaintext or poorly hashed password storage

Exposed encryption keys

Custom or home-grown cryptography implementations

Mitigation Techniques

Use strong, modern algorithms (AES, RSA with proper key sizes)

Hash passwords with slow hashing algorithms such as:

bcrypt

scrypt

Argon2

Never hardcode secrets or credentials in source code

Use secure key management solutions and environment variables

Practical Exploitation

The practical demonstrated a note-sharing application that used a weak shared cryptographic key to protect encrypted notes.

By exploiting the weak cryptographic implementation, all notes were decrypted successfully.

Flag obtained:

THM{WEAK_CRYPTO_FLAG}

Task 3 – A05: Injection
Description

Injection vulnerabilities occur when user input is improperly handled and passed directly into:

Databases

Operating system commands

Template engines

APIs or interpreters

Common injection types include:

SQL Injection

Command Injection

Server-Side Template Injection (SSTI)

AI Prompt Injection

Despite being a well-known vulnerability, injection remains a high-severity issue in 2025.

Mitigation Techniques

Treat all user input as untrusted

Use prepared statements and parameterized queries

Avoid passing user input directly to system shells

Apply strict input validation and sanitization

Enforce data types and escape dangerous characters

Practical Exploitation

This task demonstrated a Server-Side Template Injection (SSTI) vulnerability.

By abusing the template rendering mechanism, I was able to read sensitive files from the server, including flag.txt.

Flag obtained:

THM{SSTI_FLAG_OBTAINED}

Task 4 – A08: Software or Data Integrity Failures
Description

Software or Data Integrity Failures occur when applications trust data, updates, or code without verifying:

Authenticity

Integrity

Source

Examples include:

Insecure deserialization

Unverified software updates

Trusting external scripts or configuration files

Weak CI/CD pipeline security

Mitigation Techniques

Verify integrity using cryptographic hashes and signatures

Enforce strict trust boundaries

Secure CI/CD pipelines

Avoid unsafe deserialization of untrusted data

Practical Exploitation

This task focused on a Python insecure deserialization (pickle) vulnerability.

By crafting a malicious serialized payload, I was able to execute unintended behavior and read the contents of flag.txt.

Flag obtained:

THM{INSECURE_DESERIALIZATION}

Key Takeaways

OWASP Top 10 vulnerabilities remain highly relevant in modern applications

Weak cryptography, injection flaws, and insecure data handling are still common

Secure coding practices and proper validation are critical

Hands-on exploitation greatly improves understanding of real-world risks

Learning Platform

TryHackMe

Learning Path: Cyber Security 101

Room: OWASP Top 10 2025 – Insecure Data Handling
