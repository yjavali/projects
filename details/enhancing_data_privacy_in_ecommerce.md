# Dissertation: Enhancing Data Privacy in E-commerce Applications through Homomorphic Encryption in a Multi-Cloud Environment

## **Dissertation Duration and Access Details**
This dissertation was conducted over a duration from **October 2023 to September 2024**, reflecting an extensive effort in research and implementation.

The complete dissertation, along with supporting resources, can be accessed through the following secure link:
[Access Complete Work](https://drive.proton.me/urls/EVT9QXJE8R#sKNmKc0tVaR2). The file is password-protected. To request access, please email the author, Yashas Javali, stating your purpose. A secure password will be shared upon approval.

---

## **Chapter 1: Introduction**

### **Background**
The adoption of multi-cloud architectures in e-commerce has introduced unprecedented complexities in ensuring data privacy and security. Sensitive customer information is fragmented across multiple cloud service providers (CSPs), increasing exposure to risks such as breaches, unauthorised access, and misconfigurations. Homomorphic encryption offers a transformative solution, enabling operations on encrypted data without compromising its confidentiality, which directly addresses the critical need for secure analytics.

### **Problem Statement**
Existing privacy-preserving mechanisms often fall short in balancing data utility, regulatory compliance, and security in distributed systems. E-commerce platforms, reliant on cloud infrastructure, face challenges in protecting data while extracting meaningful insights. This research seeks to provide an innovative framework addressing these challenges.

### **Research Questions and Objectives**
- **Research Question:** How can homomorphic encryption be effectively utilised to enhance data privacy in multi-cloud e-commerce environments while maintaining analytical integrity?
- **Objectives:**
  1. Develop a distributed, privacy-preserving system leveraging homomorphic encryption.
  2. Evaluate the framework against GDPR compliance requirements.
  3. Assess scalability and efficiency in real-world datasets.

### **Significance of the Study**
This study fills a critical gap by proposing a comprehensive privacy-preserving analytical framework for e-commerce platforms. It bridges theoretical cryptographic advancements and practical applications, aligning with stringent regulatory standards while addressing real-world challenges.

---

## **Chapter 2: Literature Review**

### **Overview of Privacy-Preserving Techniques**
1. **Homomorphic Encryption:** Facilitates computations on encrypted data, preserving confidentiality throughout the analytical process.
2. **Secure Multi-Party Computation (SMPC):** Enables collaborative computation across parties without sharing raw data.
3. **Differential Privacy:** Protects data privacy by introducing statistical noise, though at the potential cost of analytical accuracy.

### **Comparative Analysis**
- Homomorphic encryption is unmatched in maintaining data confidentiality during analysis but has a higher computational cost.
- SMPC offers collaboration without data exposure but struggles with scalability in large-scale systems.
- Differential privacy ensures statistical protection but may introduce data distortion.

### **Research Gaps**
1. Limited integration of homomorphic encryption in distributed, multi-cloud environments.
2. Insufficient focus on regulatory alignment, particularly GDPR compliance.
3. A lack of practical demonstrations on large-scale, real-world datasets in e-commerce.

---

## **Chapter 3: Methodology**

### **Research Design**
The research adopts a hybrid experimental approach, combining theoretical cryptographic design with practical implementation. 

### **Philosophical Positioning**
Acknowledging the dynamic nature of cyber threats, the study assumes the position of an “honest-but-curious” adversary model, focusing on securing data against intentional and accidental breaches within CSPs.

### **Hypotheses Development**
1. **H1:** The framework ensures end-to-end data privacy across CSPs.
2. **H2:** Encrypted analytical outputs match plaintext results with an acceptable margin of error.
3. **H3:** The system complies with GDPR mandates under Articles 25, 32, and 35.

### **Data Collection and Dataset Description**
- **Dataset:** Online Shoppers Purchasing Intention Dataset, comprising 12,330 records with variables related to demographics, behaviours, and transactional intents.
- **Source:** Publicly available under a CC-BY-4.0 license.

### **Data Analysis Techniques**
1. Encryption using the Brakerski-Gentry-Vaikuntanathan (BGV) scheme.
2. Distributed encrypted computation using AWS, Azure, and GCP nodes.
3. Validation by cross-referencing encrypted outcomes with plaintext results.

---

## **Chapter 4: Results and Analysis**

### **System Architecture**

Below is the **Logical Architecture Diagram** illustrating the interactions between components across multiple cloud platforms:

![LogicalArchitectureDiagram1](https://github.com/user-attachments/assets/0db38887-1b49-41eb-808a-0312c000a22a)

#### Key Highlights:
1. **Data Processing on AWS:** Encrypted data from MariaDB is preprocessed and distributed securely to other cloud environments.
2. **Analytical Computations on Azure:** Linear regression is performed using encrypted datasets.
3. **Decryption and Interpretation on GCP:** Results are decrypted, and insights are generated using an integrated LLM for secure interpretation.

---

### **Key Management System**

![KeyGenerationDiagram](https://github.com/user-attachments/assets/fe9b84da-a225-4ff4-9ef9-5145e6ddc33b)


The **Key Management System (KMS)** ensures robust encryption key handling:
- **Public Key Distribution:** Securely shared across AWS and Azure for encryption.
- **Private Key Retention:** Stored securely on GCP for decryption.
- **Relinearisation Keys:** Distributed to support efficient polynomial computations.
- **Role-Based Access Controls:** Ensure that only authorised entities access key resources.

---

### **Data Handling Techniques**
#### **Base64 Encoding**
- Used to transform binary data into text format for secure transmission.
- Ensures compatibility across multiple cloud platforms.

#### **Data Serialisation**
- Encoded data into a JSON structure to facilitate interoperability.
- Enabled efficient parsing by cloud-based applications.

#### **Data Integrity Checks**
- Applied hashing algorithms (e.g., SHA-256) to validate data consistency.
- Prevented unauthorised modifications during transit.

#### **Transmission Security**
- Utilised HTTPS and TLS 1.3 protocols to secure communication between cloud nodes.
- Ensured end-to-end encryption for data in transit.

---

### **Threat Modelling and Attack Graphs**
#### Threat Modelling:
The STRIDE methodology was applied to identify vulnerabilities:
- **Spoofing:** Addressed via mutual authentication and secure API communication.
- **Tampering:** Mitigated through data integrity checks and encryption.
- **Repudiation:** Implemented logging and auditing mechanisms.
- **Information Disclosure:** Homomorphic encryption safeguards sensitive data.
- **Denial of Service (DoS):** Resilient architecture with redundancy.
- **Elevation of Privileges:** Enforced role-based access control for key management.

#### Attack Graphs:
Attack graphs were constructed to simulate potential adversarial paths:
- **Data Breach:** Simulated data leakage through compromised CSP nodes.
- **Man-in-the-Middle Attack:** Demonstrated the resilience of encrypted API calls.
- **Insider Threat:** Validated key access control policies.

---

### **MITRE ATT&CK Framework**
The system was evaluated against the MITRE ATT&CK framework to assess its resilience:
- **Initial Access:** Prevented unauthorised API access through token-based authentication.
- **Execution:** Securely isolated computational processes in sandboxed environments.
- **Persistence:** Implemented encryption keys with limited validity to reduce attack duration.
- **Exfiltration:** Utilised encrypted API communication to thwart data leakage attempts.

#### Mitigation Techniques:
1. **Credential Hardening:** Enforced strong, rotated passwords and multi-factor authentication.
2. **Privilege Management:** Ensured minimal privilege allocation using role-based access controls.
3. **Automated Monitoring:** Integrated intrusion detection systems to monitor anomalous behaviours.

---

### **GDPR Compliance**

#### Alignment with Articles:
1. **Article 25:** Privacy by design was implemented in all stages of the architecture.
2. **Article 32:** Strong encryption and access control ensured secure processing.
3. **Article 35:** DPIA was conducted to assess risks and mitigations.

---

### **Findings**
1. **Privacy Preservation:** Maintained confidentiality throughout the data lifecycle.
2. **Analytical Integrity:** Outputs from encrypted computations were within a 3% deviation of plaintext benchmarks.
3. **Regulatory Compliance:** Fully aligned with GDPR principles.
4. **Scalability:** Demonstrated high performance across datasets with over 12,000 records.
5. **Security:** Resilience against various cyber threats validated through attack graph simulations.

---

## **Chapter 5: Discussion**

### **Implications for Cyber Security**
1. Strengthened resilience against cyber threats, including data breaches, insider attacks, and advanced persistent threats.
2. Enhanced trustworthiness of multi-cloud systems through rigorous regulatory alignment.
3. Promoted the adoption of privacy-preserving frameworks in e-commerce, addressing industry-wide concerns.

### **Challenges and Limitations**
1. High computational cost of homomorphic encryption necessitates further optimisation.
2. Dependency on CSP infrastructure raises concerns about vendor lock-in and systemic vulnerabilities.
3. Rapidly evolving threat landscapes require continual updates and adaptation of the framework.

---

## **Chapter 6: Conclusion and Future Scope**

### **Summary of Key Findings**
1. Validated the feasibility of secure, privacy-preserving analytics in multi-cloud environments.
2. Delivered a scalable and GDPR-compliant framework for e-commerce data handling.
3. Bridged the gap between cryptographic theory and real-world application.
4. Demonstrated robust security and compliance through STRIDE, MITRE ATT&CK, and GDPR alignment.

### **Future Directions**
1. **Algorithm Optimisation:** Enhance efficiency to reduce the computational cost of encryption.
2. **Post-Quantum Cryptography:** Research cryptographic schemes resilient to quantum computing threats.
3. **Dynamic Threat Detection:** Develop AI-driven intrusion detection systems for proactive mitigation.
4. **Cross-Domain Applications:** Expand the framework to domains such as healthcare, finance, and government operations.
5. **Decentralised Systems:** Explore blockchain-based implementations for immutable data integrity.

---

**Author:** Yashas Javali  

**Statement of Contribution:** This dissertation represents a comprehensive effort to design, implement, and validate a privacy-preserving multi-cloud framework tailored to the stringent demands of e-commerce data privacy and regulatory compliance.


