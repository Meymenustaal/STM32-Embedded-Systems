# 📏 HC-SR04 Ultrasonic Distance Measurement & Warning System

## 📌 Project Overview
This project implements a non-contact distance measurement system using an HC-SR04 ultrasonic sensor and an STM32 microcontroller. 

A threshold-based visual warning mechanism is integrated into the system, demonstrating real-time data processing and hardware decision-making capabilities.

## ⚙️ Hardware Configuration
* **Microcontroller:** STM32F103C8T6 (Blue Pill)
* **Sensor:** HC-SR04 Ultrasonic Sensor
* **Output:** LED (Visual Warning Indicator)
* **Main Peripherals Used:** GPIO (Trigger and LED), Timer (Echo pulse duration measurement)

## 🛠️ How it Works
The STM32 generates a 10µs pulse on the sensor's Trigger pin to emit an ultrasonic wave. The microcontroller then measures the duration of the high state on the Echo pin using a hardware Timer. The distance is calculated based on the speed of sound. 

A specific software threshold is implemented: 
**If the measured distance falls below 12 cm, the microcontroller immediately activates the green LED** to provide a visual proximity warning.

## 📷 Media
<img width="357" height="405" alt="image" src="https://github.com/user-attachments/assets/ec8507b6-9eed-4ee6-8c98-944a89d43986" />


▶️ ** https://youtube.com/shorts/H6jMKykle88?feature=share **
