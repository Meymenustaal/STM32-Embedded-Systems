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
<img width="520" height="435" alt="hall" src="https://github.com/user-attachments/assets/fb6898de-9b0d-423a-9f47-77e9817c75ee" />


▶️ **[Click here to watch the project demonstration video](YOUTUBE_LINKIN_BURAYA_GELECEK)**
