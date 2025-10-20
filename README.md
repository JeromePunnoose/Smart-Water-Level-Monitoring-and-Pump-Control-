# 💧 Smart Water Level Monitoring and Pump Control

### 📘 Overview  
This project monitors the water level in a tank using an **HC-SR04 ultrasonic sensor** and automatically controls a **12 V DC pump** through a **relay module**. The system runs on a **NodeMCU ESP8266** with the **Blynk IoT platform**, enabling real-time monitoring and remote control via smartphone.

---

### ⚙️ Components Used  
- NodeMCU ESP8266  
- HC-SR04 Ultrasonic Sensor  
- 5 V Dual-Channel Relay Module (with Optocoupler)  
- 12 V DC Water Pump  
- 12 V Power Supply  
- Jumper Wires and Breadboard

---

### 🧠 Working Principle  
1. The HC-SR04 emits an ultrasonic pulse via TRIG from the NodeMCU.  
2. The echo is received and the NodeMCU measures the time duration → converts to distance in cm.  
3. The distance is mapped to a percentage level (0 % = empty, 100 % = full) based on the calibrated min/max distances.  
4. In **Auto mode**, if water level falls below a threshold (e.g., 20 %), the pump is turned ON; when it rises above a higher threshold (e.g., 80 %), the pump is turned OFF.  
5. In **Manual mode**, the user can control the pump via the Blynk button. The pump status LED reflects whether the pump is running.

---

### 📱 Blynk Setup (Virtual Pins)  
| Virtual Pin | Widget       | Function                        |
|-------------|--------------|----------------------------------|
| V0          | Gauge        | Displays water level (%)         |
| V1          | Button       | Manual pump ON/OFF control       |
| V2          | LED          | Shows pump status (ON = lit)     |
| V3          | Switch       | Toggle Auto / Manual mode        |


---

### 📂 Circuit Diagram & Block Diagram  
([Circuit Diagram.jprg]([https://github.com/JeromePunnoose/Smart-Water-Level-Monitoring-and-Pump-Control-/blob/f839f9eca70d657e0669b6e009f69a8d3affdd94/Circuit%20Diagram.jpeg](https://github.com/JeromePunnoose/Smart-Water-Level-Monitoring-and-Pump-Control-/blob/f839f9eca70d657e0669b6e009f69a8d3affdd94/Circuit%20Diagram.jpeg)))  
([Block Diagram.png](https://github.com/JeromePunnoose/Smart-Water-Level-Monitoring-and-Pump-Control-/blob/fe7aee960c46aa4045717afc9d49d9a96d570527/Block%20Diagram.png))

---

### 🎥 Project Demonstration  
[![Watch the Demo Video]([https://img.youtube.com/vi/1mVJVF7FysNmHoguVx9TnmTg_7pHMOXsj/0.jpg)](https://drive.google.com/file/d/1mVJVF7FysNmHoguVx9TnmTg_7pHMOXsj/view?usp=drive_link](https://drive.google.com/file/d/1mVJVF7FysNmHoguVx9TnmTg_7pHMOXsj/view?usp=drive_link))

---

### 🧑‍💻 Source Code  
The Arduino sketch is available in `code/water_level_control.ino`.

---

### 🧾 Report  
A detailed project report (PDF) is available in `documentation/project_report.pdf`.

---


---

### 🎉 Developer  
**Name:** Jerome Punnoose  
**Platform:** Arduino IDE + NodeMCU + Blynk  
**Year:** 2025

---

Thank you for visiting! Feel free to explore the code, diagrams, and live demo.  

