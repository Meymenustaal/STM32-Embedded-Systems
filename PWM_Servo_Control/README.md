# ⚙️ PWM Servo Motor Control

## 📌 Project Overview
This project focuses on the angular control of a servo motor using Pulse Width Modulation (PWM).
By manipulating the duty cycle of the timer output, precise positioning of the motor shaft is achieved.

## ⚙️ Hardware Configuration
* **Microcontroller:** STM32F-DISC1 (Discovery)
* **Actuator:** Servo Motor
* **Key Peripherals Used:** Timer (TIM2), PWM Channel 3

## 🛠️ How It Works
The STM32 timer is configured to generate a PWM signal. By varying the compare value using the `__HAL_TIM_SET_COMPARE` function, the pulse width is adjusted, which directly translates into the servo motor's angular position. The code iterates through predefined compare values to demonstrate smooth sweep motion.

## 📷 Media
*(Buraya PWM projesine ait breadboard bağlantı fotoğrafını ekle)*

## 📂 Source Code
The complete implementation of the PWM control logic is available in the [main.c](main.c) file.
