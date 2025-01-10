# Vehicle-to-Pedestrian Adaptive Communication System Using Cloud-Based Architecture

## **Overview**

### **Objective:**  
To develop a centralised system that alerts pedestrians on their smartphones and drivers on an onboard unit (OBU) about potential collision risks. The system is designed to be cost-effective, accurate, robust, and quick to respond, reducing pedestrian fatalities and enhancing road safety.

**Specialist Field:** Embedded Systems and Vehicular Communication  
**Submission Date:** January 2019 - May 2019  

The project tackles the increasing pedestrian fatalities in India by introducing a communication system that proactively alerts both pedestrians and drivers, thereby enabling timely corrective action to prevent collisions.

---

## **Motivation**

Indian roads report alarming pedestrian death rates due to jaywalking and lack of effective safety measures. Current vehicle safety features focus on occupants rather than vulnerable road users like pedestrians. This project aims to fill this gap by developing a bifunctional alert system that protects pedestrians and provides critical alerts to drivers.

---

## **Key Features**

1. **Bidirectional Alert System:** Alerts both pedestrians (via smartphone) and drivers (via onboard unit).
2. **Cloud-Based Architecture:** Utilises GPS data to compute collision risks in real-time.
3. **Weather and Lighting Independence:** Functions effectively in adverse conditions unlike traditional systems.
4. **Cost-Effective Solution:** Relies on affordable components such as GPS modules and cloud computing.
5. **High Accuracy:** Detects and alerts within a 15-metre range with a 360-degree field of view.

---

## **System Design and Methodology**

### **Functional Block Diagram:**
The system comprises:
- **GPS Modules:** Collect location data from the pedestrian’s smartphone and the vehicle’s onboard unit.
- **Cloud Server:** Computes the distance and risk of collision between pedestrian and vehicle.
- **Alert System:** Sends notifications to pedestrian smartphones and onboard units in real-time.

### **Hardware Components:**
1. **Raspberry Pi 3B:** Serves as the onboard processing unit.
2. **GPS NEO-6MV2:** Tracks the location of the vehicle and pedestrian.
3. **Amazon Web Services (AWS):** Hosts cloud computation for risk assessment.
4. **Buzzer:** Alerts drivers via an onboard sound system.
5. **Smartphone Application:** Provides visual and audio alerts to pedestrians.

### **Proposed Workflow:**
1. The pedestrian’s smartphone and vehicle onboard unit send location data to the cloud server.
2. The server computes the distance and checks if it falls within a predefined collision range.
3. If a collision risk is detected, alerts are sent to both devices in real-time.

---

## **Technical Details**

### **Key Algorithms:**
- **Distance Computation:** Calculates real-time separation between pedestrian and vehicle using GPS coordinates.
- **Threshold Comparison:** Determines collision risks based on predefined safety margins.
- **Alert Mechanism:** Push notifications sent to connected devices upon risk detection.

### **Optimisation Techniques:**
- Reduced cloud latency to improve real-time response.
- Optimised GPS data handling for efficient computation.
- Minimised power consumption for prolonged device operation.

---

## **Results and Outcomes**

1. Successfully achieved real-time bidirectional alerts for pedestrians and drivers.
2. Independent of weather and lighting conditions, ensuring robust operation.
3. Maintained high accuracy in collision detection with a 360-degree field of view.
4. Demonstrated low-cost implementation compared to LiDAR or RADAR-based solutions.

---

## **Learning Outcomes**

1. **Technical Proficiency:**
   - Acquired expertise in GPS-based tracking, cloud computing, and embedded systems.
   - Enhanced skills in developing efficient communication protocols.

2. **Problem-Solving:**
   - Overcame challenges in achieving low-latency alerts using cloud-based architecture.
   - Improved system reliability through iterative testing and optimisation.

3. **Impact:**
   - Contributed a scalable and economical solution to reduce pedestrian fatalities.
   - Established a foundation for expanding vehicle-to-everything (V2X) communication systems.

---

## **Future Scope**

1. **Distributed System:** Transition to a decentralised architecture to reduce cloud dependency.
2. **Multi-Platform Support:** Expand compatibility to iOS devices and additional onboard units.
3. **Enhanced Features:** Integrate advanced sensors and predictive analytics for proactive collision prevention.
4. **Extension to V2X Systems:** Broaden scope to include communication with infrastructure, motorcycles, and other road elements.

---

**Author:** Yashas Javali  

---

**Statement of Contribution:** This project represents a collaborative effort to design a reliable and efficient communication system aimed at improving road safety and reducing pedestrian fatalities.


