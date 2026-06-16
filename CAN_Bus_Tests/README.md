# CAN Bus Node-to-Node Communication

## Project Overview
This project implements a basic CAN bus communication system between two STM32F4 Discovery boards. One node acts as a transmitter, reading analog sensor data, while the other acts as a receiver, triggering an output based on incoming CAN frames.

## Hardware Configuration
* **Microcontrollers:** 2x STM32F407G-DISC1
* **Transceivers:** 2x MCP2551 High-Speed ​​CAN Transceivers
* **Network Setup:** Two-wire differential bus with 120Ω termination resistors at both ends
* **I/O Components:** Potentiometer for input, LED for output indication

## System Architecture
The system uses the MCP2551 to interface the STM32 CAN controllers with the physical differential bus.

* **Transmitter Node (TX):** Reads a variable analog voltage from a potentiometer using an ADC. The data is packaged into a CAN frame with a standard ID and broadcast to the network.

* **Receiver Node (RX):** Uses CAN hardware filters to accept only messages with a specified ID. Reception is performed via FIFO0 interrupts. When a valid frame is received, the load is removed to check the status of an LED.

## Media
<img width="558" height="436" alt="image" src="https://github.com/user-attachments/assets/d4a74ace-cc82-4f54-a856-81fb1ced5255" />
