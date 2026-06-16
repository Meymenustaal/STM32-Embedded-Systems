# 🎛️ Potentiometer and Buzzer Volume Control (ADC to PWM)

## 📌 Project Overview
This project demonstrates a basic Mixed Signal integration on an STM32 microcontroller. It continuously reads an analog voltage signal from a potentiometer and dynamically maps this value to a hardware timer, adjusting the Pulse Width Modulation (PWM) duty cycle. This change in duty cycle directly controls the volume (audio output level) of a connected buzzer.

## ⚙️ Hardware Configuration
* **Microcontroller:** STM32F103C8T6 (Blue Pill)
* **Input Device:** 10kΩ Rotary Potentiometer
* **Output Device:** Buzzer
* **Main Peripherals Used:**

* **ADC1 (Analog-to-Digital Converter):** Polling mode, 12-bit resolution (0 - 4095)

* **TIMx (Hardware Timer):** Generating a PWM signal on a specified channel

## 🧠 System Architecture (ADC-PWM Mapping)
The basic logic of this system is based on real-time signal scaling. The STM32's ADC has 12-bit resolution, meaning the analog voltage of the potentiometer is converted into a digital value between `0` and `4095`.

## 💻 Basic Logic Implementation
Below is a conceptual C code snippet representing the continuous ADC polling within the main loop and the mathematical mapping to the PWM register:

```c
// Assume Timer ARR (Auto Reload Register) is set to 1000
uint32_t adc_value = 0;

uint32_t pwm_duty = 0;

// I started PWM generation on the specific Timer Channel
HAL_TIM_PWM_Start(&htim2, TIM_CHANNEL_1);

while (1) {
// I started the 1st ADC conversion
HAL_ADC_Start(&hadc1);

HAL_ADC_PollForConversion(&hadc1, 10);

// 2. Get the 12-bit analog value (0 - 4095)

adc_value = HAL_ADC_GetValue(&hadc1);

// 3. I mapped the ADC value proportionally to the Timer's Duty Cycle limit.
pwm_duty = (adc_value * 1000) / 4095;

// 4. I dynamically updated the PWM output register
__HAL_TIM_SET_COMPARE(&htim2, TIM_CHANNEL_1, pwm_duty);

// I added minimum delay for system stability
HAL_Delay(10);

}
```

## 📷 Media

<img width="987" height="397" alt="buzzer" src="https://github.com/user-attachments/assets/15b6000e-03eb-4af4-9961-6f6a5d10cfdb" />


## ▶️ Click here to watch the hardware demonstration video : https://youtube.com/shorts/nM_dF6m9VJ8
