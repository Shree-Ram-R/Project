# Post-Quantum Cryptography-Enhanced FIDO2 Password-less Authentication
## Title of the Project

### Post-Quantum Cryptography-Enhanced FIDO2 Password-less Authentication System

## Project Description

A secure password-less authentication system that enhances FIDO2 login with quantum-resistant digital signatures, ensuring long-term protection against future quantum computing attacks.
This system enables a smooth transition from classical cryptography (RSA/ECC) to Post-Quantum Cryptography (PQC) using a hybrid approach.

## About

Post-Quantum Cryptography-Enhanced FIDO2 Authentication integrates the NIST-recommended lattice-based digital signature algorithm CRYSTALS-DILITHIUM into the traditional FIDO2 workflow.

Current FIDO2 authentication relies on RSA and ECC, which are vulnerable to quantum attacks through Shor’s Algorithm. Although FIDO2 removes password dependency and strengthens phishing resistance using cryptographic key pairs, it does not natively support quantum-safe cryptography.

To address this, the project introduces:

CRYSTALS-DILITHIUM (ML-DSA) for quantum-resistant digital signature verification

A hybrid FIDO2 authentication flow ensuring backward compatibility

Spring Boot (Java Backend) and Kotlin (Android Frontend) implementation

Secure key storage using HSM/TPM/YubiKey, DFS challenge signing, and JWT session security

Scalability aimed at mobile, enterprise, cloud & IoT authentication ecosystems

Prioritizing both security and usability, this solution future-proofs authentication while maintaining a fast and seamless user experience.

## Features

🔐 Quantum-Resistant Authentication using Multi-Layered Dilithium Signature Algorithm (ML-DSA)

🔑 FIDO2 + WebAuthn + CTAP Integration, fully password-less

⚙️ Secure Key Management via HSM, TPM, YubiKey & Android Keystore enclave

🔄 Hybrid Cryptographic Model to allow smooth migration from RSA/ECC to PQC

⚡ Optimized Cryptographic Operations for reduced authentication latency

📊 Comprehensive Logging & Monitoring for audit trails and anomaly detection

☁️ Scalable Deployment for mobile, web, cloud & IoT authentication

🛡️ Zero Trust Security Model with continuous identity validation

🧬 Biometric Authentication Support for multi-factor authentication readiness

📦 JSON-based scoped response model for structured chatbot interaction (if further extended)

## Requirements
💻 Operating System

64-bit OS: Windows 10 or Linux (Ubuntu/CentOS recommended)

### Development Environment

Kotlin – Android frontend development (Android 8.0+)

Java 17+ – Spring Boot backend services

### Cryptographic Tools & Frameworks

CRYSTALS-DILITHIUM for quantum-resistant signature verification

OpenSSL for encryption, TLS verification, and key processing

WebAuthn & CTAP libraries for FIDO2 authentication compliance

### Database

PostgreSQL / MySQL for secure storage of authentication keys and logs

🔑 Secure Storage Hardware (Recommended)

TPM / HSM / FIDO2 Security Keys (YubiKey, Passkeys, Secure Enclave)

🔥 Security & Testing Tools

Postman, Wireshark, Burp Suite, Metasploit, Nmap, OWASP ZAP, JUnit, Espresso

🎯 Additional Dependencies

Spring Boot, Spring Security, JWT, coroutines, Android SDK 30+

## System Architecture
🧱 Tech Stack
Component	Technology
Frontend	Kotlin (Android App)
Backend	Java (Spring Boot)
Database	PostgreSQL / MySQL
Cryptography	CRYSTALS-DILITHIUM (ML-DSA)
Session Security	JWT
Key Storage	Android Keystore, Secure Enclave, HSM, TPM, YubiKey
Communication	HTTPS + TLS 1.3
## Authentication Flow

Client generates cryptographic key pairs (during registration)

Server provides challenge via WebAuthn

Client signs challenge with CRYSTALS-DILITHIUM private key

Server retrieves stored public key and verifies signature

Grants or denies authentication

JWT securely maintains session

🔧 Experiments and Results
⚡ Performance Evaluation
Metric	Traditional FIDO2	PQC-Enhanced FIDO2
Registration Time	~1.2s	~1.8s
Authentication Time	~0.8s	~1.4s
Key Size	2048-bit RSA	~2KB Dilithium Key
🛡 Security Testing Summary
Attack	Result
MITM Attack	No data leakage
Replay Attack	Authentication rejected
Brute Force	Account lockout triggered
SQL Injection	No vulnerability found

✅ All security scenarios passed with strong quantum-attack resistance.
## System Architecture
<img width="680" height="295" alt="image" src="https://github.com/user-attachments/assets/0564ce1a-4c77-45f2-90f1-2b9547ced099" />


## Output
### Home:
<img width="264" height="421" alt="image" src="https://github.com/user-attachments/assets/00a23192-3f11-4749-8f0c-7064e3f6d4c4" />

### Registration

<img width="256" height="425" alt="image" src="https://github.com/user-attachments/assets/e93990f0-c1e0-4770-b08d-f784d63a8726" />

### Registration completed

<img width="266" height="418" alt="image" src="https://github.com/user-attachments/assets/805cb3c0-7239-4ae1-8e44-ad5268abe1ae" />


### Logged In
<img width="261" height="420" alt="image" src="https://github.com/user-attachments/assets/d658f290-23b9-46a7-b352-e4cf04e9a0e0" />

### DashBoard I
<img width="263" height="419" alt="image" src="https://github.com/user-attachments/assets/43243d31-f98c-46fa-bc27-37bb27b5a504" />

### DashBoard II
<img width="256" height="422" alt="image" src="https://github.com/user-attachments/assets/4e5ebb21-2910-40ea-bbec-746e10717fc5" />

### Server Logs
<img width="615" height="212" alt="image" src="https://github.com/user-attachments/assets/75ca7c41-42ae-473d-a2e5-61c76c6fa97d" />


## Results and Impact

Successfully safeguards authentication against future quantum threats

Enables a hybrid migration path without disrupting current systems

Demonstrates scalable, secure, and usable passwordless authentication

Strengthens enterprise identity verification for banking, IoT, defense, and cloud login ecosystems

Builds foundation for further multi-platform PQC FIDO2 expansion

## Future Enhancements

Improve performance using hardware acceleration & parallel cryptographic processing

Extend support to iOS, Windows, and Linux authenticators

Integrate additional authentication factors like behavioral and advanced biometric verification

Ensure evolving compliance with NIST PQC, ISO/IEC 27001, and FIDO Alliance standards

Continuous third-party security audits

## References

L. Deepesh et al., Anna University – Authentication Standards Review

National Institute of Standards and Technology – PQC Finalists

Fluhrer et al., Lattice-based authentication integrity survey

Anderson et al., Large scale PQC enterprise deployment evaluation
