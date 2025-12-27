# 🤖 Autonomous Line Following & Obstacle Avoiding Robot

![Project Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Language](https://img.shields.io/badge/Language-C%2B%2B%20%2F%20Arduino-blue?style=for-the-badge)
![Hardware](https://img.shields.io/badge/Hardware-Arduino%20Uno%20%2B%20L293D-orange?style=for-the-badge)

## 📖 Introduction
This project is a **2WD Autonomous Mobile Robot** developed as a Freshman Capstone Project at **HCMUTE**. The robot operates in two modes:
1.  **Line Following:** Tracks a black line on a white surface using 3 IR sensors (TCRT5000).
2.  **Obstacle Avoidance:** Detects obstacles using an Ultrasonic Sensor (HC-SR04) and scans the path using a Servo motor.

<div align="center">
  <img src="images/xedoline.jpg" width="45%" alt="Robot View 1" style="border-radius: 10px;">
  &nbsp;
  <img src="images/xedoline1.jpg" width="45%" alt="Robot View 2" style="border-radius: 10px;">
  <br><br>
  <img src="images/xedoline2.jpg" width="60%" alt="Robot View 3" style="border-radius: 10px;">
</div>

---

## 🛠️ Hardware Requirements

| Component | Specification | Quantity |
| :--- | :--- | :---: |
| **MCU** | Arduino Uno R3 | 1 |
| **Driver** | L293D Motor Shield | 1 |
| **Motors** | DC Gear Motors (Yellow, 1:48) | 2 |
| **Line Sensors** | TCRT5000 IR Sensor (3-Channel) | 1 |
| **Distance Sensor** | HC-SR04 Ultrasonic | 1 |
| **Servo** | SG90 Micro Servo | 1 |
| **Power** | 18650 Li-ion Batteries (3.7V x 2) | 2 |
| **Regulator**| LM2596 Buck Converter (5V Out) | 1 |
| **Chassis** | Acrylic 2WD Smart Car | 1 |

---

## 🔌 Wiring & Pinout
Based on the firmware configuration:

### 1. Line Tracking Sensors (TCRT5000)
| Position | Arduino Pin |
| :--- | :---: |
| Left Sensor (SL) | **A5** |
| Middle Sensor (SM) | **A4** |
| Right Sensor (SR) | **A3** |

### 2. Obstacle Avoidance Modules
| Component | Pin | Connected To |
| :--- | :---: | :---: |
| **HC-SR04** | Trig | **A1** |
| | Echo | **A0** |
| **Servo SG90** | Signal | **Pin 9** (Servo 2 on Shield) |

---

## 💻 How It Works
* **Line Following:** Uses a simple PID-like logic. If `Middle` sees line -> Forward. If `Left` sees line -> Turn Left. If `Right` sees line -> Turn Right.
* **Obstacle Avoidance:** If `Distance < 24cm` -> Stop -> Back up -> Scan Left/Right -> Turn to the clearer path.

---

## 👤 Author
* **Nguyen Phu Huu** (ID: 24161090)
* **Major:** Electronics & Telecommunications Technology - HCMUTE

### 🎓 Acknowledgments
Special thanks to **Lecturer Phan Van Ca** for his guidance in the *Introduction to ECET* course.

---
### 📝 License
This project is open-source and available under the [MIT License](LICENSE).
