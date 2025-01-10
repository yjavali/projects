# **IoT-Based Monitoring and Management System for Lettuce Cultivation**

## **Introduction**

This project explores the use of **Internet of Things (IoT)** technology to develop a smart system for monitoring and managing lettuce cultivation. By integrating sensors, microcontrollers, and a mobile application, the system addresses critical parameters like soil moisture, temperature, and humidity. The solution is designed to be cost-effective, portable, and scalable, catering to use cases in restaurants, café shops, and homes.

**Duration:** July 2019 - January 2020

---

## **Objectives**

1. **Automation of Monitoring and Irrigation:**
   - Automatically measure and maintain optimal soil moisture levels.
2. **Real-Time Alerts:**
   - Provide real-time updates to users via a mobile application.
3. **Scalability:**
   - Support multiple plant units without compromising performance.
4. **User-Friendly Interface:**
   - Design an intuitive mobile application for seamless monitoring.
5. **Portability:**
   - Ensure the system is lightweight and compact.

---

## **System Architecture**

### **1. Functional Overview**

The system comprises the following key components:
- **Sensors:**
  - Soil moisture, temperature, and humidity sensors to collect environmental data.
- **Microcontroller:**
  - Node MCU to process sensor data and communicate with the mobile application.
- **Actuators:**
  - A relay and a DC water pump for automated irrigation.
- **Mobile App:**
  - Blynk-based app for remote monitoring of system parameters.
- **Display:**
  - A 16x2 LCD for localised real-time data representation.

### **2. Workflow**
1. Sensors measure environmental parameters (soil moisture, temperature, humidity).
2. The microcontroller processes sensor data and compares soil moisture against the threshold.
3. If soil moisture is below the threshold:
   - The relay activates the water pump.
   - Water is dispensed for a set duration (10 seconds).
4. Sensor data is transmitted to the mobile application via the internet.
5. Real-time data is displayed on the LCD and the mobile app.

---

## **Hardware Implementation**

### **1. Components Used**
| **Component**           | **Specification**        | **Purpose**                                   |
|--------------------------|--------------------------|-----------------------------------------------|
| **Node MCU**             | ESP8266 Wi-Fi module    | Microcontroller for data processing and communication. |
| **Soil Moisture Sensor** | FC-28                   | Measures soil moisture levels.                |
| **Temperature Sensor**   | DHT22                   | Captures temperature and humidity readings.   |
| **Relay Module**         | 5V Single Channel       | Controls the water pump operation.            |
| **Water Pump**           | 12V DC                  | Dispenses water for irrigation.               |
| **LCD Display**          | 16x2 I2C module         | Displays sensor data locally.                 |

### **2. Circuit Connections**
- **Node MCU Pins:**
  - Analog Pin (A0) for soil moisture sensor input.
  - Digital Pins (D1, D2) for DHT22 and relay control.
- **Relay and Pump:**
  - Relay output connected to the DC pump's power circuit.
- **LCD Display:**
  - I2C interface connected to Node MCU for displaying real-time data.

---

## **Software Implementation**

### **1. Programming Environment**
- **IDE Used:** Arduino IDE.
- **Libraries Integrated:**
  - `DHT.h` for handling temperature and humidity sensor data.
  - `LiquidCrystal_I2C.h` for LCD communication.
  - `BlynkSimpleEsp8266.h` for app integration and internet connectivity.

### **2. Control Logic**
```c
// Threshold and duration settings
int soilThreshold = 30; // Percentage
int pumpDuration = 10000; // Milliseconds

void loop() {
  int soilMoisture = analogRead(A0);
  int temperature = dht.readTemperature();
  int humidity = dht.readHumidity();

  // Trigger pump if soil moisture is below threshold
  if (soilMoisture < soilThreshold) {
    digitalWrite(pumpRelayPin, HIGH);
    delay(pumpDuration);
    digitalWrite(pumpRelayPin, LOW);
  }

  // Send data to Blynk and display locally
  Blynk.virtualWrite(V1, soilMoisture);
  Blynk.virtualWrite(V2, temperature);
  Blynk.virtualWrite(V3, humidity);
  lcd.print("Soil: " + String(soilMoisture));
  lcd.print("Temp: " + String(temperature));
}
```

### **3. Mobile App Integration**
- **Platform:** Blynk  
- **Features:**
  - Real-time display of soil moisture, temperature, and humidity.
  - **Widgets:** Gauges for live parameter updates and notification alerts for critical thresholds.

---

## **Testing and Results**

### **1. Functional Testing**
- Soil moisture sensor accuracy validated against a calibrated device.
- Relay and pump operations tested under varying soil conditions.

### **2. Mobile App Testing**
- Successfully received real-time updates on the Blynk app with minimal latency.
- Alerts generated when soil moisture dropped below the defined threshold.

### **3. System Performance**
- **Response Time:** Average latency of 1.2 seconds for sensor data to app update.
- **Irrigation Effectiveness:** Uniform water delivery within 10 seconds of pump activation.

---

## **Technical Insights**

### **Cost Analysis**
| **Component**           | **Cost (INR)** |
|--------------------------|----------------|
| Node MCU                | 330            |
| Soil Moisture Sensor     | 120            |
| DHT22 Sensor             | 200            |
| Relay                    | 180            |
| Water Pump               | 220            |
| 16x2 LCD Display         | 165            |
| Jumper Wires/Breadboard  | 185            |
| Power Supply             | 550            |
| **Total Cost**           | **2650**       |

### **Performance Metrics**
- **Data Accuracy:** ±2% for soil moisture; ±0.5°C for temperature readings.
- **Energy Consumption:** 12V DC pump consumes approximately 3W per operation cycle.
- **System Uptime:** Reliable performance tested for 48 hours of continuous operation.

---

## **Learning Outcomes**

1. **IoT Development:**
   - Learned to integrate sensors, microcontrollers, and cloud platforms for real-time data monitoring.
2. **Mobile Application Design:**
   - Gained proficiency in developing a Blynk-based app for IoT systems.
3. **Circuit Optimisation:**
   - Enhanced skills in designing compact and efficient circuits.
4. **Testing Methodologies:**
   - Developed expertise in functional and stress testing of IoT systems.

---

## **Conclusion**

The IoT-based system effectively demonstrated its ability to monitor and manage lettuce cultivation in real-time. By combining automation, mobility, and scalability, the project offers a promising solution for precision agriculture. The system's modular design ensures ease of expansion, making it adaptable for larger-scale deployments.

---

## **Future Scope**

1. **Integration with AI:**
   - Use machine learning models to predict irrigation needs based on historical data.
2. **Multi-Crop Support:**
   - Extend the system to support various crop types with customisable parameters.
3. **Battery Integration:**
   - Implement solar-powered solutions for sustainable energy use.
4. **Cross-Platform Compatibility:**
   - Develop a unified app compatible with iOS and Windows devices.

---

**Author:** Yashas Javali  
**Specialisation:** IoT and Smart Agriculture  
**Statement:** This project represents a practical implementation of IoT principles to address challenges in modern agriculture, enhancing productivity and resource efficiency.

