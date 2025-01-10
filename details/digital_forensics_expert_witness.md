# **Project: Digital Forensics Investigation and Analysis**

## **Disclaimer:**  

The case details and all characters mentioned in this document are fictional and anonymised wherever possible for educational and illustrative purposes. Specific names and identifiable details have been replaced with generic terms. 

---

## **Introduction**

This project involves a comprehensive digital forensics investigation conducted for the court case **Rex v. Djanko**, focusing on allegations of assault and narcotics distribution. The investigation adhered to strict forensic principles, ensuring evidence integrity, chain of custody, and admissibility in court. The analysis utilised industry-standard tools to extract, process, and interpret data from seized digital devices.

The complete report is available at the following secure link: [Access Complete Report](https://drive.proton.me/urls/RKN17SHN4W#NmZWLcfasG5a). The document is password-protected. To request access, please email the author, **Yashas Javali**, stating your purpose. A secure password will be shared upon approval.

---

## **Objectives**

1. **Evidence Acquisition and Integrity Validation:**
   - Ensure forensically sound acquisition of data from all devices.
   - Validate evidence authenticity using cryptographic hash functions.

2. **Detailed Analysis:**
   - Extract and interpret digital artifacts to establish a timeline of events.
   - Cross-validate findings from multiple devices.

3. **Technical Correlation:**
   - Use metadata, geospatial data, and user activity logs to connect the suspect to the crime scene and narcotics distribution.

4. **Expert Witness Reporting:**
   - Present findings in a clear, unbiased, and legally compliant manner.

---

## **Forensic Process and Methodology**

### **1. Evidence Acquisition**
- **Devices Seized:**
  - **Laptop (MMX-Djanko-PC.E01):** Acquired from the suspect’s residence.
  - **Dashcam (MMX-1-Dashcam.E01):** Retrieved from the suspect's vehicle.
- **Tools Used:**  
  - **FTK Imager v3.4.2.6:** Created forensic disk images in `.E01` format.  
  - **Hash Validation:** MD5 and SHA1 hashes verified during acquisition to ensure no tampering.
- **Chain of Custody:**  
  A strict chain of custody was maintained, with all handling logged in compliance with ISO/IEC 27037 standards.

### **2. Evidence Processing**
- **Primary Tool:**  
  - **Autopsy v4.19.3:** Automated artifact extraction, registry analysis, and timeline generation.
- **Supplementary Tools:**  
  - **ExifTool v12.57:** Extracted GPS metadata from dashcam videos.
  - **RegRipper:** Parsed Windows Registry hives for user activity.
  - **Bulk Extractor:** Identified patterns, including email addresses, URLs, and credit card data.

### **3. Analysis and Interpretation**
#### **Laptop Analysis**
- **User Accounts:**
  - Identified two active user profiles: `djanko` and `PaulD`.
  - `djanko` had administrative privileges, allowing unrestricted system access.
- **Registry Analysis:**
  - Recent activity logs showed file access patterns related to encrypted files (`SensitiveData.pdf` and `DropLocations.pdf`).
  - Installed software included a dark web browser and VPN applications.
- **Browser History:**
  - Frequent visits to forums discussing narcotics sourcing and distribution.

#### **Dashcam Analysis**
- **GPS Metadata:**
  - Extracted GPS coordinates from 22 video files using ExifTool.
  - Cross-referenced data with Google Maps to create a travel timeline.
  - Confirmed suspect’s proximity to the crime scene near the **Degree Apprenticeship Centre, University of Warwick** on the incident date.
- **Video Frame Analysis:**
  - Applied frame extraction tools to identify objects of interest but faced clarity challenges due to low resolution.

#### **Network Traffic and Emails**
- **Emails Recovered:**
  - Communications between `PaulD` and `Stuart Tchaikomsiva` discussed logistics for drug drops.
- **Network Logs:**
  - VPN traffic correlated with timestamps of sensitive email exchanges, indicating secure communication channels.

---

## **Key Findings**

1. **Connection Between Suspect and Victim:**
   - Recovered emails established direct communication between the suspect and the victim, including plans for narcotics distribution.

2. **Proximity to Crime Scene:**
   - GPS metadata from the dashcam confirmed the suspect’s vehicle was at the crime scene during the alleged assault.

3. **Evidence of Narcotics Distribution:**
   - Email content and search history indicated systematic drug sourcing and delivery methods.
   - Metadata revealed encrypted documents likely containing critical evidence.

4. **Attempts to Obfuscate Data:**
   - The presence of encrypted files (`SensitiveData.pdf`) and data deletion attempts suggested deliberate obfuscation.

---

## **Technical Insights**

### **Tools and Techniques Used**
| **Tool**             | **Purpose**                                                             |
|-----------------------|-------------------------------------------------------------------------|
| FTK Imager            | Forensic imaging and hash validation of digital evidence.              |
| Autopsy               | Disk analysis, artifact extraction, and timeline reconstruction.       |
| ExifTool              | GPS metadata extraction from dashcam video files.                     |
| RegRipper             | Windows Registry analysis for user activity and software artifacts.   |
| Bulk Extractor        | Pattern-based search for email addresses, URLs, and sensitive data.   |
| Google Earth Pro      | Visualisation of geospatial data for route reconstruction.            |

### **Validation and Correlation**
- **Hash Validation:** Ensured integrity of forensic images using MD5 and SHA1 hashes.
- **Metadata Correlation:** Cross-referenced GPS data from dashcam with timestamps of emails and file access.

---

## **Legal and Admissibility Aspects**

1. **Chain of Custody:**
   - Strictly followed throughout the investigation to ensure admissibility under legal frameworks like **ACPO (Association of Chief Police Officers) Guidelines** and **ISO/IEC 27037**.

2. **Evidence Authenticity:**
   - Hash values (MD5 and SHA1) verified for forensic images, demonstrating evidence integrity.
   - Processes adhered to **Daubert Standards**, ensuring reliability in methodology and analysis.

3. **Rights of the Accused:**
   - Privacy rights of the suspect were respected during the acquisition and handling of personal data.
   - Evidence collection remained within the scope of the search warrant.

4. **Limitations in Decryption:**
   - Encrypted files remain inaccessible due to advanced password protection, but their existence corroborates other findings.

---

## **Challenges and Resolutions**

1. **Encrypted Files:**
   - Encountered strong encryption on PDFs. Resolution required further decryption efforts, potentially involving brute force or key recovery methods but the files remained inaccessible.
   
2. **Low-Quality Dashcam Footage:**
   - Attempted enhancing frames using OpenCV-based video processing, though clarity remained limited.

3. **Cross-Validation:**
   - Used redundant tools like ExifTool and Google Earth Pro to ensure accuracy of GPS metadata analysis.

---

## **Learning Outcomes**

1. **Forensic Tool Proficiency:**
   - Gained expertise in FTK Imager, Autopsy, and ExifTool for forensic imaging, analysis, and metadata extraction.
2. **Geospatial Analysis:**
   - Developed advanced skills in GPS metadata processing and route visualisation.
3. **Chain of Custody Best Practices:**
   - Strengthened understanding of ISO/IEC 27037 guidelines for evidence handling.
4. **Legal Admissibility:**
   - Strengthened understanding of evidence admissibility through adherence to ACPO Guidelines and ISO/IEC standards.

---

## **Conclusion and Recommendations**

### **Conclusion**
The investigation successfully uncovered:
1. A direct connection between the suspect and the victim.
2. Evidence of the suspect’s presence at the crime scene.
3. Substantial indications of narcotics distribution activities.
4. Attempts to conceal critical evidence through encryption and deletion.

### **Recommendations**
1. **Advanced Decryption Efforts:**  
   Leverage cloud computing resources for password recovery on encrypted files.
2. **Automation in Metadata Processing:**  
   Deploy AI-based tools for faster and more accurate artifact analysis.
3. **Operational Guidelines:**  
   Establish a centralised digital evidence repository with role-based access controls for efficient case management.

---

**Author:** Yashas Javali  
**Specialisation:** Digital Forensics  
**Statement:** This report was prepared as an expert witness account for **West Midshires Police** to assist in the court case **Rex v. Djanko**.

---

