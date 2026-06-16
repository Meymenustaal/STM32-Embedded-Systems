# 🚦 STM32 Traffic Light Controller (State Machine & Timers)

## 📌 Project Overview
This project demonstrates the implementation of a classic Traffic Light control system using an STM32 microcontroller. Instead of relying on inefficient blocking functions like `HAL_Delay()`, the system is designed around a **Finite State Machine (FSM)** and **Hardware Timers** to ensure precise, non-blocking execution.

## ⚙️ Hardware Configuration
* **Microcontroller:** STM32F103C8T6 (Blue Pill)
* **Actuators:** 3x LEDs (Red, Yellow, Green)
* **Current Limiting:** 3x 330Ω Resistors
* **Main Peripherals Used:** General Purpose Output (GPIO), Hardware Timer (TIMx)

## 🧠 System Architecture (State Machine Logic)
The system operates on a 4-state sequence mimicking standard traffic light regulations:
1. **State 0 (STOP):** Red LED is ON.
2. **State 1 (GET READY):** Red and Yellow LEDs are ON.
3. **State 2 (GO):** Green LED is ON.
4. **State 3 (WAIT):** Yellow LED is ON.

Transitions between these states are strictly governed by hardware timer interrupts, ensuring the main loop remains free for other potential tasks.

## 💻 Core Logic Implementation
Below is the conceptual C-code snippet representing the Finite State Machine (FSM) implemented in the timer callback:

```c
typedef enum {
    STATE_RED,
    STATE_RED_YELLOW,
    STATE_GREEN,
    STATE_YELLOW
} TrafficState_t;

TrafficState_t currentState = STATE_RED;

void HAL_TIM_PeriodElapsedCallback(TIM_HandleTypeDef *htim) {
    if(htim->Instance == TIM2) {
        switch(currentState) {
            case STATE_RED:    // Turn on RED, Turn off others

                currentState = STATE_RED_YELLOW; // Next state
                break;

            case STATE_RED_YELLOW:    // Turn on RED and YELLOW
               
                currentState = STATE_GREEN; // Next state
                break;

            case STATE_GREEN:    // Turn on GREEN, Turn off others
                
                currentState = STATE_YELLOW; // Next state
                break;

            case STATE_YELLOW:    // Turn on YELLOW, Turn off others
                
                currentState = STATE_RED; // Next state
                break;
        }
    }
}
```

## 📷 Media
<img width="397" height="207" alt="traffic_lamb" src="https://github.com/user-attachments/assets/de4324c2-771a-4d0e-bcf2-4eacf314875d" />


## ▶️ [Click here to watch a video of the hardware: https://youtube.com/shorts/5xPPrxuDroI?feature=share]
