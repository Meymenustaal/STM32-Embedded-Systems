# STM32 Embedded Systems & Hardware Control

## 📌 Overview
This repository contains a collection of embedded system applications and hardware control algorithms developed using STM32 microcontrollers. The projects focus on real-world engineering problems, utilizing various communication protocols, peripheral integrations, and HAL (Hardware Abstraction Layer) libraries. 

*Development and testing were conducted on multiple microcontroller families to ensure platform adaptability.*

## ⚙️ Core Competencies & Projects
* **Sensor Reading and Control:** Designed an autonomous fan control circuit by reading temperature data from an NTC thermistor using the ADC module.
* **Motor Control:** Configured Timer and PWM modules to provide precise angular control of servo motors and integrated system feedback.
* **Distance Detection and Warning:** Processed data from ultrasonic sensors (HC-SR04) to develop distance-based visual (LED) and auditory (buzzer) warning systems.
* **Magnetic Field Sensing:** Integrated a Hall Effect sensor to detect magnetic fields and process proximity-based hardware triggers.
* **Inter-Board Communication (CAN Bus):** Conducted communication and debugging tests between microcontrollers of the same family (two STM32F4 Discovery boards, and separately two STM32F103 "Blue Pill" boards) using the CAN Bus protocol and MCP2515 transceivers.

## 🗺️ System Architecture Diagram
<img width="1233" height="460" alt="Ekran görüntüsü 2026-06-15 230757" src="https://github.com/user-attachments/assets/a5b2e9f5-84a1-4ed7-a407-4496b3d6b28e" />


## 📂 Project Structure
* `Timer_Traffic_Light/` - Traffic light sequence implementation using hardware timers.
* `Potentiometer_Buzzer/` - Analog voltage reading via ADC to control buzzer frequency/volume.
* `Ultrasonic_Warning/` - HC-SR04 integration for distance measurement with visual/auditory feedback.
* `NTC_Fan_Control/` - ADC configuration and temperature-triggered autonomous fan system.
* `Hall_Sensor/` - Magnetic field detection and proximity-based hardware triggering.
* `PWM_Motor_Control/` - Timer/PWM settings for motor speed and precise angle manipulation.
* `CAN_Bus_Tests/` - CAN bus communication attempts between identical microcontroller pairs (F4 to F4, F1 to F1).

## 🛠️ Tools & Technologies
* **Software:** STM32CubeIDE, STM32 HAL Library, C Programming
* **Hardware:** STM32F407G-DISC1 (Discovery), STM32F103C8T6 (Blue Pill), Oscilloscope & Breadboard Prototyping
## 📷 Hardware Setup & Media
<img width="962" height="444" alt="potentiometer_readme" src="https://github.com/user-attachments/assets/45360071-6a22-419d-a0e1-445621ed85bc" />



## 👨‍💻 Muhammed Eymen Ustaal /Electrical and Electronics Engineering Student

