# STM32 Embedded Systems & Hardware Control

## 📌 Overview
This repository contains a collection of embedded system applications and hardware control algorithms developed using STM32 microcontrollers. 
The projects focus on real-world engineering problems, utilizing various communication protocols, peripheral integrations, and HAL (Hardware Abstraction Layer) libraries.

## ⚙️ Core Competencies & Projects

* **Sensor Reading and Control:** Designed autonomous fan and contactor control circuits by reading temperature data from an NTC thermistor using the ADC module.
* **Motor Control:** Configured Timer and PWM modules to provide precise angular control of servo motors and integrated system feedback.
* **Distance Detection and Warning:** Processed data from ultrasonic sensors (HC-SR04) to develop distance-based visual (LED/flasher) and auditory (buzzer) warning systems.

## 🗺️ System Architecture Diagram

+--------------------+    Input Sensors      +-----------------------+       +--------------------+
|   Input Sensors    |       |     STM32 MCU         |       | Output / Actuators |
|   (Data Logging)   |       |  (Data Processing)    |       | (System Response)  |
+--------------------+       +-----------------------+       +--------------------+
|                    |       |                       |       |                    |
| - NTC Thermistor   | ----> | - ADC Modules         | ----> | - Autonomous Fan   |
| - HC-SR04 Sonic    | ----> | - Timers & Interrupts | ----> | - LEDs & Buzzer    |
| - Potentiometer    | ----> | - PWM Generators      | ----> | - Servo Motor      |
|                    |       | - HAL Library         |       | - Contactor        |
+--------------------+       +-----------------------+       +--------------------+

## 📂 Project Structure
* `NTC_Temp_Control/` - ADC configuration and temperature-triggered fan system.
* `PWM_Servo_Control/` - Timer/PWM settings for motor angle manipulation.
* `Ultrasonic_Warning/` - HC-SR04 integration with visual/auditory feedback.
* `CAN_Bus_Tests/` - MCP2515 integration attempts and debugging notes.

## 🛠️ Tools & Technologies
* STM32CubeIDE
* STM32 HAL Library
* C Programming
* Oscilloscope & Breadboard Prototyping

## 📷 Hardware Setup & Media


