# ⚙️ PWM Servo Motor Control

## 📌 Project Overview
This project focuses on the angular control of a servo motor using Pulse Width Modulation (PWM).

By manipulating the duty cycle of the timer output, I achieved precise positioning of the motor shaft.

## ⚙️ Hardware Configuration
* **Microcontroller:** STM32F103C8T6 (Blue Pill)
* **Actuator:** Servo Motor
* **Main Peripherals Used:** Timer (TIM2), PWM Channel 3

## 🛠️ How it Works
The STM32 timer is configured to generate a PWM signal. By changing the comparison value using the `__HAL_TIM_SET_COMPARE` function, the pulse width is adjusted, which directly reflects on the angular position of the servo motor. The code loops between predefined comparison values ​​to demonstrate smooth sweep motion.

## 📷 Media
<img width="272" height="403" alt="pwm_mission" src="https://github.com/user-attachments/assets/982af40b-f215-4da8-8383-67159fe746d9" />

