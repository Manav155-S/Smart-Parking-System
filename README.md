# 🅿️ IoT Smart Parking System

### [🎬 Watch the Video Demo](https://drive.google.com/drive/folders/1BNYem31uBJkF8tFde_yx2hmmL75IWGpo?usp=drive_link)

A real-time, IoT-based solution designed to monitor and manage parking space availability. This project uses ultrasonic sensors to detect vehicles and a Firebase backend to display live status on a mobile dashboard.

---

## 🛠️ Technology & Hardware Stack

* **Hardware:** NodeMCU (ESP8266), Ultrasonic Sensors (HC-SR04) 
* **Cloud & Backend:** Google Firebase (Realtime Database) 
* **Mobile App:** React Native 
* **Firmware Language:** C/C++ (for NodeMCU)

---

## 🏛️ System Architecture

The system operates on a simple, 4-layer architecture to provide real-time updates:

1.  **Sensor Layer:** An **HC-SR04 Ultrasonic Sensor** is placed at each parking spot. It continuously measures the distance to detect if a vehicle is present.

2.  **Microcontroller Layer:** The sensor is connected to a **NodeMCU (ESP8266) board**. This microcontroller reads the distance data from the sensor, determines if the slot is "Occupied" or "Available," and connects to the local Wi-Fi network.

3.  **Cloud Layer:** The NodeMCU sends the status of its assigned parking slot to a **Google Firebase Realtime Database**. This acts as our central, live backend, ensuring data is synchronized instantly.

4.  **Application Layer:** A mobile application built with **React Native** subscribes to the Firebase database. It listens for changes and updates the UI in real-time to show users the live status of all parking slots, without needing to refresh the page.

---
## 📂 Source Code

* [**NodeMCU Firmware Code**](./nodemcu-code/) - C/C++ code flashed onto the ESP8266 boards.
* [**React Native App Code**](./react-native-app/) - Code for the mobile dashboard.
