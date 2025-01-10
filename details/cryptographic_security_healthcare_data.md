# **Cryptographic Security Implementation for Protected Healthcare Data**

## **Introduction**

This project, completed on **April 21, 2024**, aims to enhance the cryptographic security of sensitive data assets for a leading UK Clinic. By integrating robust encryption mechanisms, authentication frameworks, and key management strategies, the project secures systems such as Medical Records, Payment Service, Electronic Prescribing System and the Intellectual Property Sharing.

The cryptographic simulations were performed using **CrypTool**, a comprehensive platform for cryptographic learning and experimentation.

The complete project is available at the following secure link: [Access Complete Project](https://drive.proton.me/urls/AYTH0QN80R#WgadLSyy85NB). The document is password-protected. To request access, please email the author, **Yashas Javali**, stating your purpose. A secure password will be shared upon approval.

---

## **Key Cryptographic Features**

### **Authentication and Authorisation**
- **Password Authentication:**  
  Uses salted passwords hashed with SHA-512 to prevent rainbow table attacks. A 16-byte random salt ensures unique hashes even for identical passwords.
- **Multi-Factor Authentication (MFA):**  
  Implements HOTP (HMAC-based One-Time Password) using the HMAC-SHA1 algorithm.
  - The HOTP is refreshed every minute and derived from a 16-byte key and current UNIX timestamp.
  - Chosen over SMS-based OTP to avoid SIM swap vulnerabilities and improve usability.
- **Single Sign-On (SSO):**  
  Utilises OAuth 2.0 with short-lived JSON Web Tokens (JWTs) generated using HKDF-SHA256.
  - Ensures secure access to resources through Role-Based Access Control (RBAC) policies.
  - Tokens are encrypted in transit and protected against replay and tampering attacks using HMAC-SHA256.

---

### **Key Lifecycle Management**
- **Key Derivation:**
  - HKDF-SHA256 is used for generating AES-256 keys with high entropy.
  - PBKDF2 is employed for deriving encryption keys in data sharing scenarios, protecting against brute force and rainbow table attacks.
- **Storage:**
  - Keys are stored in a Hardware Security Module (HSM) for maximum security.
  - Encryption keys for services (e.g., MedRecords, FinCare) are stored in a secure database after AES-256 encryption with the master key.
- **Key Rotation:**
  - Keys are regularly rotated and retired, minimising the impact of key compromise.
  - Complies with FIPS 140-2 standards for cryptographic module validation.

---

## **Data Encryption and Integrity**

### **Encryption at Rest**
- **Algorithm:** AES-256 in Cipher Block Chaining (CBC) mode with PKCS#7 padding.
- **Applications:**
  - Field-level encryption for databases storing sensitive information like MedRecords and FinCare.
  - Disk-level encryption for files, ensuring confidentiality in scenarios such as invoice handling and intellectual property sharing.
- **Compliance:** Designed to align with GDPR and CCPA requirements.

### **Encryption in Transit**
- **Protocol:** TLS 1.2 is used for secure data transmission.
- **Key Exchange:** Combines RSA-2048 with Diffie-Hellman to ensure forward secrecy.
- **Integrity:** Uses HMAC-SHA256 and digital signatures for message integrity and non-repudiation.

---

## **Proposed Cryptographic Architecture**

The simulation was designed and implemented using CrypTool, highlighting cryptographic workflows for various healthcare services:
1. **Medical Records:**
   - Key Derivation: HKDF-SHA256.
   - Integrity: HMAC-SHA256.
   - Storage: Field-level encrypted database.
2. **Payment Service:**
   - Key Derivation: HKDF-SHA256.
   - Integrity: Digital Signature with RSA-2048.
   - Storage: Encrypted database.
3. **Electronic Prescribing System:**
   - Key Derivation: HKDF-SHA256.
   - Storage: Disk-level encryption enabled volumes.
4. **Intellectual Property Sharing:**
   - Key Derivation: PBKDF2.
   - Integrity: HMAC-SHA256.
   - Storage: Disk-level encryption enabled volumes.

---

## **Compliance with Regulations**

The cryptographic framework adheres to:
- **GDPR (Article 32):** Ensures encryption of data at rest and in transit.
- **CCPA:** Implements privacy measures for consumer data protection.
- **PSD2:** Supports Strong Customer Authentication (SCA) with MFA and secure access token policies.

---

## **Learning Outcomes**

1. Designed and implemented advanced cryptographic solutions, including HKDF, PBKDF2, AES-256, and RSA-2048.
2. Strengthened knowledge of TLS protocols and their role in securing data transmission.
3. Enhanced understanding of compliance frameworks such as GDPR, CCPA, and PSD2.

---

## **Conclusion and Future Scope**

This project showcases the integration of robust cryptographic solutions into healthcare systems, ensuring security and compliance. Future directions may include:
- **Post-Quantum Cryptography:** Preparing systems for quantum-resilient encryption standards.
- **Homomorphic Encryption:** Exploring secure computations on encrypted data.
- **Blockchain Integration:** Decentralising identity and access management for data sharing.

---

