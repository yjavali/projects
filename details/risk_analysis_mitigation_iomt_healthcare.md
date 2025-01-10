# **Risk Analysis and Mitigation for IoMT Devices in Healthcare**

## **Introduction**

This project investigates the vulnerabilities and risks associated with Internet of Medical Things (IoMT) devices in healthcare delivery organisations (HDOs). The focus is on implementing robust **Governance, Risk, and Compliance (GRC)** frameworks and adhering to international standards for security and risk management. The project also proposes practical controls to mitigate risks while ensuring compliance with regulatory requirements.

The complete project is available at the following secure link: [Access Complete Project](https://drive.proton.me/urls/KWTEHB22NC#7DxwFHp3l5GE). The document is password-protected. To request access, please email the author, **Yashas Javali**, stating your purpose. A secure password will be shared upon approval.

---

## **Governance and Compliance Framework**

### **Key Standards for IoMT Devices**

1. **IEC 80001-1:2021**  
   - Focus: Lifecycle risk management for IT networks integrating medical devices.
   - Emphasises identifying hazards, evaluating associated risks, and implementing controls.
   - Designates a **Medical IT Network Risk Manager** responsible for stakeholder collaboration.

2. **ISO/IEC 27001:2022**  
   - Focus: Establishing and maintaining an Information Security Management System (ISMS).
   - Includes 93 controls across 14 domains, covering access management, cryptographic controls, and incident management.
   - Requires continuous monitoring and periodic audits.

3. **NIST Cybersecurity Framework (CSF)**  
   - Focus: Providing a flexible framework for managing cybersecurity risks.
   - Five core functions: Identify, Protect, Detect, Respond, Recover.
   - Encourages a risk-based approach tailored to IoMT-specific needs.

4. **GDPR and Data Protection Act (DPA)**  
   - Focus: Ensuring data privacy and security for personal health information (PHI).
   - Article 32 mandates encryption and pseudonymisation for data protection.

5. **OWASP Secure Medical Device Deployment Standard v2.0**  
   - Focus: Secure configuration and deployment of IoMT devices.
   - Recommends vulnerability scanning, segmentation, and encrypted communication.

---

## **Risk Analysis and Standards-Based Controls**

### **Risk Register**

| **Device**                                      | **Version**           | **CVE**         | **Vulnerability**               | **Impact**        | **Mitigation Strategies**                                                      |
|-------------------------------------------------|-----------------------|-----------------|---------------------------------|-------------------|---------------------------------------------------------------------------------|
| Welch Allyn Connex Central Station (CS)        | v1.1                 | CVE-2021-27410  | Out-of-bounds Write             | Critical (C-I-A) | Implement DEP, VLAN segmentation, VPN access, and proactive monitoring.       |
| MiniMed Paradigm Veo 554/754 Pumps             | v2.6A                | CVE-2019-10964  | Improper Authentication         | High (C-I-A)     | Apply physical controls, data obfuscation, and disconnect unused connections. |
| Medtronic MyCareLink (MCL) Smart Model 25000   | v2.0                 | CVE-2020-25187  | Heap Overflow                   | Critical (C-I-A) | Regular patching, physical security, and proactive monitoring.                |
| Natus EEG with NeuroWorks                     | v8                    | CVE-2017-2853   | Stack Buffer Overflow           | High (C-I-A)     | Limit network exposure, use segmentation, and ensure VPN-only connections.    |
| Dickinson BD Alaris Plus Medical Syringe Pumps | v2.3.6               | CVE-2018-14786  | Improper Authentication         | Critical (C-I-A) | VLAN segmentation, VPN access, and strict firewall controls.                  |

---

### **Controls Based on Standards**

#### **Governance Controls**
- **Policy Framework:**  
  Align organisational policies with IEC 80001-1 to manage risks across the IoMT device lifecycle.  
- **Audit and Compliance:**  
  Conduct regular audits to ensure adherence to GDPR, NIST CSF, and ISO/IEC 27001 standards.

#### **Access Management**
- **RBAC Implementation:**  
  Define roles based on device functionality and enforce least privilege access.
- **Authentication:**  
  Implement MFA for administrative access, with support for biometrics.

#### **Cryptographic Controls**
- **Data Encryption:**  
  - AES-256 for data at rest.  
  - TLS 1.3 for data in transit, ensuring protection against eavesdropping.  
- **Integrity Validation:**  
  Use HMAC-SHA256 to validate the integrity of critical communications.

#### **Device Configuration and Deployment**
- **Secure Boot:**  
  Verify device integrity during boot using cryptographic signatures.  
- **Firmware Updates:**  
  Ensure signed firmware updates to prevent tampering.  
- **Network Isolation:**  
  Use VLAN segmentation and firewalls to isolate devices from critical infrastructure.

#### **Monitoring and Detection**
- **Intrusion Detection Systems (IDS):**  
  Deploy IDS tailored to IoMT traffic for anomaly detection.  
- **SIEM Integration:**  
  Use SIEM tools for centralised monitoring and incident response.

#### **Incident Management**
- Develop a robust incident response plan (aligned with ISO/IEC 27035), including detection, containment, and recovery phases.  
- Conduct mock incident simulations to enhance preparedness.

---

## **Learning Outcomes**

1. Strengthened understanding of governance frameworks (IEC 80001, ISO/IEC 27001) and their practical application to IoMT devices.
2. Gained expertise in developing standards-based controls to address IoMT risks.
3. Enhanced skills in integrating monitoring, incident management, and regulatory compliance for healthcare environments.
4. Improved proficiency in cryptographic controls and secure device configuration.

---

## **Conclusion and Future Scope**

The project underscores the critical importance of standards-based governance and technical controls in mitigating IoMT device risks. Implementing compliance-driven frameworks ensures both security and operational efficiency.

### **Future Directions**
1. **AI-Driven Monitoring:**  
   Develop advanced anomaly detection systems using AI to enhance real-time threat detection.

2. **Post-Quantum Security:**  
   Prepare IoMT devices for quantum-resilient cryptographic standards.

3. **IoMT Device Certification Programs:**  
   Promote certification standards for IoMT devices, ensuring secure development and deployment practices.

---

