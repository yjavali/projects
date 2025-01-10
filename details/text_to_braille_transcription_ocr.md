# Project: Transcriber for Visually Impaired

## **Overview**

### **Objective:**  
To design and implement a device that captures printed text and converts it into Braille script, enabling visually impaired individuals to access information more effectively.

**Specialist Field:** Assistive Technologies  
**Submission Date:** Academic Year 2018-2019  

The project was conceived to address the challenges faced by visually impaired individuals in accessing printed text. The Transcriber device bridges the gap by enabling real-time conversion of printed material into Braille, using advanced image processing and embedded systems.

---

## **Motivation**

The inspiration for this project emerged from a survey conducted at the School for the Blind, Navanagar, Hubballi. The survey revealed the scarcity of Braille-based resources and the dependency on human translators for visually impaired individuals to access knowledge. This highlighted the need for an affordable, standalone device to enhance their learning and communication capabilities.

---

## **Key Features**

1. **Real-Time Text-to-Braille Conversion:** Converts captured images into Braille script.
2. **Standalone Functionality:** Operates independently without requiring external devices.
3. **User-Friendly Interface:** Simple and intuitive operation for visually impaired users.
4. **Cost-Effective Solution:** Designed with affordability in mind, using off-the-shelf components.

---

## **System Design and Methodology**

### **Functional Block Diagram:**
The system consists of the following major components:
- **Camera Module:** Captures the image of the printed text.
- **Optical Character Recognition (OCR):** Processes the captured image to extract text.
- **Microcontroller:** Converts ASCII characters into Braille script.
- **Braille Display:** Outputs the converted Braille script in real-time.

### **Hardware Components:**
1. **Raspberry Pi:** Central processing unit for image processing and Braille conversion.
2. **MAGPI Camera Module:** High-resolution camera for image capture.
3. **Tesseract OCR Engine:** Used for extracting text from images.
4. **Braille Display Unit:** Converts text into raised Braille characters using actuators.
5. **Power Supply:** 5.1V @ 2.5A for Raspberry Pi and connected peripherals.

### **Software Workflow:**
1. Capture an image using the camera module.
2. Process the image with Tesseract OCR to extract text.
3. Convert extracted text into ASCII format.
4. Map ASCII characters to corresponding Braille patterns.
5. Display the Braille patterns on the Braille display unit.

---

## **Technical Details**

### **Key Algorithms:**
- **OCR Preprocessing:** Used to clean up images and optimise text recognition.
- **ASCII-to-Braille Mapping:** Efficient conversion algorithm for real-time performance.
- **Modular Programming:** Ensured code maintainability and optimisation.

### **Optimisation Techniques:**
- Reduced loop redundancies and utilised library functions for better memory management.
- Eliminated dead code and optimised algorithm performance.
- Improved execution speed, reducing runtime by approximately 3.5%.

---

## **Results and Outcomes**

1. Successfully captured images were processed and converted to Braille script in real-time.
2. Achieved high accuracy in text-to-Braille conversion with minimal errors.
3. Developed a user-friendly interface for standalone operation.
4. The project met its goals of affordability and accessibility, with an estimated device cost of ₹6000.

---

## **Learning Outcomes**

1. **Technical Expertise:**
   - Gained hands-on experience with Raspberry Pi, OCR engines, and hardware interfacing.
   - Enhanced skills in algorithm design, optimisation, and modular programming.

2. **Problem-Solving:**
   - Addressed challenges in text recognition under varying lighting conditions.
   - Improved Braille conversion accuracy through iterative testing and optimisation.

3. **Impact:**
   - Contributed a potential solution to improve literacy and communication for the visually impaired.
   - Highlighted the importance of affordable assistive technologies.

---

## **Future Scope**

1. **Handwriting Recognition:** Enhance the system to recognise handwritten text.
2. **Multi-Language Support:** Extend OCR capabilities to include multiple languages.
3. **Portable Design:** Miniaturise the device for greater portability.
4. **Integration with Smart Devices:** Enable wireless connectivity for enhanced functionality.

---

**Author:** Yashas Javali  

---

**Statement of Contribution:** This project was an effort to design and develop an assistive technology device that has the potential to significantly impact the lives of visually impaired individuals.


