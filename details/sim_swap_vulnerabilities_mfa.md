# **Evaluating SIM Swap Vulnerabilities and Proposing a Usability-Security Investigation in MFA Systems**

## **Introduction**

This research project, investigates vulnerabilities in SIM-based Multi-Factor Authentication (MFA) systems. By combining empirical experimentation, threat modeling, and analysis of carrier-specific authentication practices, the project identifies systemic weaknesses and proposes countermeasures to enhance security while balancing usability in MFA implementations.

The complete project is available at the following secure link: [Access Complete Project](https://drive.proton.me/urls/QJ6PBSEK10#MJD1UBBH6xUf). The document is password-protected. To request access, please email the author, **Yashas Javali**, stating your purpose. A secure password will be shared upon approval.

---

## **Research Objectives**

1. **Investigate Authentication Weaknesses:**
   - Assess inconsistencies in wireless carrier authentication procedures.
   - Evaluate vulnerabilities in SMS-based MFA systems.

2. **Understand the Impact of SIM Swap Attacks:**
   - Analyse the effects on confidentiality, integrity, and availability of sensitive data.

3. **Develop Mitigation Strategies:**
   - Propose scalable solutions for enterprises and carriers to address identified risks.
   - Explore usability-security trade-offs in alternative MFA systems.

---

## **Methodology**

### **Research Design**
This research follows an empirical approach, combining data collection, reverse engineering, and controlled experiments:
- **Controlled Experiments:** Simulated weak attacker models to probe carrier-specific authentication challenges.
- **MFA Analysis:** Reviewed the effectiveness of SMS-based MFA across 145 websites.
- **Threat Modelling:** Applied STRIDE to evaluate weaknesses in existing carrier systems and MFA configurations.

### **Data Collection**
- **Sample Size:** 50 prepaid accounts across five major U.S. wireless carriers.
- **Parameters Analysed:** Authentication challenges based on personal, account, device, and usage information.
- **Tools Used:** Wireshark for network monitoring and Burp Suite for interaction with authentication APIs.

### **Key Research Questions**
1. How effective are current wireless carrier authentication mechanisms in preventing SIM swap attacks?
2. What alternative MFA implementations can mitigate the risks associated with SIM swaps while maintaining usability?

---

## **Findings and Analysis**

### **Authentication Weaknesses**
1. **Personal Data Exploitation:**
   - Static personal information (e.g., birthdates) frequently used for authentication.
   - Easy availability of such data on social media makes carriers vulnerable to impersonation.
2. **Process Inconsistencies:**
   - Varied procedures across carriers increase attack vectors for adversaries.
   - Absence of dynamic challenges weakens authentication robustness.

### **Impact of SIM Swap Attacks**
1. **Compromised Confidentiality:**
   - Interception of one-time passwords (OTPs) for online banking and social media.
2. **Data Integrity Risks:**
   - Fraudulent SIM swaps enable attackers to manipulate financial and personal data.
3. **Service Denial:**
   - Victims experience extended downtime while resolving attacks.

### **MFA Reverse Engineering**
- Identified major flaws in MFA systems like Duo and Okta:
  - Lack of MFA customisation for SMS fallback options.
  - Default configurations exposing systems to phishing and credential stuffing attacks.

---

## **Legal and Regulatory Considerations**

1. **Wireless Provider Accountability:**
   - Potential negligence in adopting secure authentication processes.
   - Recommendations to enforce stricter regulatory oversight through the FCC and FTC.
2. **FCC 2023 Rules:**
   - Mandates customer notifications for SIM swaps.
   - Advocates advanced authentication mechanisms for high-risk actions.

---

## **Proposed Mitigation Strategies**

### **Improved Authentication Mechanisms**
1. Transition from SMS-based MFA to app-based or hardware token-based solutions.
2. Introduce dynamic knowledge-based challenges that require context-specific answers.

### **Carrier-Level Recommendations**
1. Implement stricter SIM swap authorisation processes, including notification response windows.
2. Strengthen SS7 protocol security to minimise legacy vulnerabilities.

### **Enterprise-Level Solutions**
1. Employ hardware-based tokens (e.g., YubiKey) for authentication.
2. Adopt zero-trust principles, requiring multiple factors for system access.

---

## **Learning Outcomes**

1. Mastered the application of empirical research techniques in cybersecurity contexts.
2. Gained expertise in threat modeling (STRIDE) and risk evaluation.
3. Developed skills in reverse engineering authentication systems to identify weaknesses.
4. Strengthened understanding of usability-security trade-offs in MFA system design.

---

## **Conclusion and Future Scope**

This project illustrates how systemic weaknesses in SIM-based MFA systems expose users to significant cybersecurity threats. By adopting stronger authentication mechanisms and implementing regulatory reforms, carriers and enterprises can mitigate these risks while ensuring user adoption through usability considerations.

Future research directions include:
- **AI-Powered Anomaly Detection:** Using machine learning to identify fraudulent SIM swap attempts in real-time.
- **Quantum-Resistant Authentication:** Preparing authentication systems for post-quantum cryptography challenges.
- **Usability vs. Security Trade-offs:** Designing MFA solutions that balance user convenience and security.

---

