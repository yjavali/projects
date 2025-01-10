# Dissertation: Enhancing Data Privacy in E-commerce Applications through Homomorphic Encryption in a Multi-Cloud Environment

## **Overview**

### **Objective:**  
To design and implement a multi-cloud system leveraging homomorphic encryption to enhance data privacy in e-commerce applications while ensuring compliance with GDPR principles and maintaining analytical accuracy.

**Specialist Field:** Cyber Security Engineering  
**Institution:** WMG, University of Warwick  
**Timeframe:** October 2023 to September 2024  

This dissertation explores a novel approach to preserving data privacy in e-commerce applications by integrating homomorphic encryption into a multi-cloud architecture. The project addresses critical privacy concerns associated with distributed systems while mitigating cyber threats and maintaining analytical capabilities.

---

## **Motivation**

The exponential growth of e-commerce platforms has intensified the need for secure handling of sensitive data. Multi-cloud architectures, while offering scalability and redundancy, introduce significant cyber security risks, such as data breaches, unauthorised access, and compliance failures. Homomorphic encryption emerges as a vital tool to address these issues, enabling computations on encrypted data and protecting it against malicious actors.

This research is motivated by:
1. The increasing sophistication of cyber threats in cloud ecosystems.
2. The critical balance between data utility and cyber security.
3. The need for regulatory compliance and innovative privacy-preserving solutions.

---

## **Key Features**

1. **Homomorphic Encryption:** Safeguards data integrity and confidentiality by allowing encrypted computations.
2. **Cyber Resilience in Multi-Clouds:** Reduces attack surfaces by leveraging distributed systems with secure encryption.
3. **GDPR Compliance:** Implements robust security controls to ensure data protection aligns with European regulations.
4. **Secure Analytics Pipeline:** Performs secure and accurate analysis without exposing sensitive data.
5. **Threat Mitigation:** Incorporates threat modelling and risk assessment frameworks to identify and mitigate cyber risks.

---

## **System Design and Methodology**

### **Cyber Security-Focused Architecture:**
- **Data Encryption Layer:** Protects sensitive e-commerce data using the Brakerski-Gentry-Vaikuntanathan (BGV) encryption scheme.
- **Distributed Cloud Nodes:** AWS, Azure, and GCP process encrypted data securely to minimise risks of single points of failure.
- **Incident Response Integration:** Monitors data integrity and anomalies during computations to prevent breaches.

### **Functional Workflow:**
1. **Threat Modelling:** Utilised STRIDE methodology to identify potential vulnerabilities in the architecture.
2. **Data Encryption:** Applied homomorphic encryption to all user and transaction data.
3. **Secure Data Distribution:** Divided encrypted datasets across multiple cloud nodes for parallel processing.
4. **Cyber Security Controls:** Enforced access controls and secure APIs for communication between nodes.
5. **Validation:** Cross-referenced encrypted results with plaintext outputs to ensure accuracy and resilience.

---

## **Technical Details**

### **Encryption Scheme:**
The BGV encryption scheme was selected for its:
- **Security Against Advanced Attacks:** Designed to withstand modern cryptographic challenges.
- **Scalable Computation Support:** Enables complex operations, such as linear regression, without decryption.
- **Interoperability:** Functions seamlessly across heterogeneous cloud platforms.

### **Cloud Security Measures:**
1. **AWS Security Groups:** Defined role-based access control policies for computation environments.
2. **Azure Defender:** Actively monitored threats to virtual machines and enforced encryption policies.
3. **Google Cloud IAM:** Controlled identity and access for secure API interactions.

### **Risk Mitigation Strategies:**
- **Data Integrity Checks:** Periodically validated encrypted data for tampering.
- **Multi-Layered Security:** Combined encryption with intrusion detection systems for enhanced protection.
- **Latency Reduction:** Optimised encryption parameters to maintain performance without compromising security.

### **Compliance and Standards:**
- Aligned with **GDPR Articles 25 (Data Protection by Design)** and **32 (Security of Processing).**
- Benchmarked against NIST cryptographic guidelines for encryption schemes.

---

## **Results and Outcomes**

1. Achieved robust encrypted analytics with <1% latency overhead in multi-cloud environments.
2. Demonstrated accurate privacy-preserving computations with a ±5% error margin.
3. Validated resilience against simulated cyber-attacks, including eavesdropping and tampering.
4. Scaled the framework to process real-world e-commerce datasets efficiently.
5. Ensured compliance with GDPR and cyber security standards while maintaining analytical fidelity.

---

## **Learning Outcomes**

### **Cyber Security Expertise:**
1. Advanced understanding of homomorphic encryption as a defence mechanism.
2. Proficiency in securing multi-cloud architectures against diverse threat vectors.
3. Skilled in regulatory compliance and implementing privacy-by-design frameworks.

### **Problem-Solving Skills:**
1. Addressed encryption-induced latency challenges without compromising system security.
2. Designed scalable solutions for secure distributed computing.
3. Enhanced system resilience through iterative security testing and optimisation.

### **Impact on Cyber Security:**
1. Established a comprehensive framework for privacy-preserving analytics in high-risk environments.
2. Contributed to the evolving field of secure multi-cloud architectures.
3. Provided actionable insights for organisations aiming to enhance their data protection strategies.

---

## **Future Scope**

1. **Advanced Cryptographic Protocols:** Research post-quantum encryption to future-proof the framework.
2. **Real-Time Threat Detection:** Integrate AI-driven anomaly detection to identify and neutralise cyber threats dynamically.
3. **Cross-Domain Applications:** Adapt the system for critical sectors, including healthcare and finance, with stringent privacy needs.
4. **Decentralised Security:** Explore blockchain-based approaches for immutable and transparent encrypted data handling.

---

**Author:** Yashas Javali  

**Statement of Contribution:** This research represents a comprehensive effort to address pressing data privacy and cyber security challenges in e-commerce through innovative cryptographic and cloud computing solutions.


