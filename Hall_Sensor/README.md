# 🧲 Hall Effect Sensor Integration

## 📌 Project Overview
This project demonstrates the integration of a Hall Effect sensor with an STM32 microcontroller to detect the presence of magnetic fields.
It serves as a foundation for proximity sensing, non-contact switching, and motor speed measurement applications.

## ⚙️ Hardware Configuration
* **Microcontroller:** STM32F103C8T6 (Blue Pill)
* **Sensor:** Hall Effect Sensor Module
* **Key Peripherals Used:** GPIO (Input Configuration)

## 🛠️ How It Works
The STM32 is configured to read the digital output of the Hall sensor.
When a magnet approaches the sensor, the magnetic field triggers a state change on the corresponding GPIO pin. 
This state change can be handled via polling or interrupts to execute specific hardware responses (e.g., toggling an LED).

## 📷 Media & Demonstration
<img width="680" height="363" alt="image" src="https://github.com/user-attachments/assets/8cf4fc11-f1e4-4b70-af29-ae33fd5585db" />



▶️ **https://youtube.com/shorts/zZUeIIyXlSQ?feature=share**
