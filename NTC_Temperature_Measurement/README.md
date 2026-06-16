# 🌡️ NTC Thermistor Temperature Measurement

## 📌 Project Overview
This project focuses on accurately measuring ambient room temperature using an NTC (Negative Temperature Coefficient) thermistor and an STM32 microcontroller. The system reads analog voltage values, converts them to resistance, and calculates the real temperature in Celsius using logarithmic mathematical modeling.

## ⚙️ Hardware Configuration
* **Microcontroller:** STM32F103C8T6 (Blue Pill)
* **Sensor:** 10k NTC Thermistor
* **Voltage Divider Circuit:** 10k Fixed Resistor
* **Main Peripherals Used:** Single-Channel ADC (Polling Mode)

## 🛠️ How it Works
The STM32 utilizes its internal Analog-to-Digital Converter (ADC) to read the voltage drop across the NTC thermistor in a voltage divider setup. 
1. The 12-bit ADC converts the analog signal into a digital value (0-4095).
2. The raw ADC value is mapped to an actual voltage (up to 3.3V).
3. The dynamic resistance of the NTC is calculated based on the voltage divider rule.
4. The exact temperature is derived using the mathematical model.

## 🧮 Mathematical Model (Beta Parameter Equation)
To convert the non-linear resistance of the NTC thermistor into an accurate temperature reading, the system implements the 
**Beta Parameter Equation** (derived from the Steinhart-Hart equation) inside the microcontroller:

**T(K) = 1 / ( (1/T0) + (1/B) * ln(R_NTC / R0) )**

* **T(K):** Temperature in Kelvin
* **T0:** Nominal temperature (298.15 K / 25°C)
* **B:** Beta parameter of the NTC (3950)
* **R_NTC:** Calculated resistance of the NTC
* **R0:** Nominal resistance at 25°C (10kΩ)

Once the temperature is calculated in Kelvin, it is dynamically converted to Celsius by subtracting 273.15.

## 🔥 Real-World Testing & Validation
To verify the dynamic response of the system and the accuracy of the mathematical model,
a heat source (a lighter) was temporarily brought close to the NTC thermistor.
The system successfully detected the rapid environmental change,
with the real-time calculated temperature quickly rising from standard room temperature (~25°C) to over 35°C, 
confirming the reliability of the ADC readings and the conversion algorithm.

## 📷 Media
<img width="187" height="368" alt="ntc" src="https://github.com/user-attachments/assets/9df286fb-6a23-473f-b44d-4790ba7a2f6f" />
