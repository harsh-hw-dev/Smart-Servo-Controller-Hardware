# Smart Servo Controller – Hardware Design

## Overview
This repository contains the complete hardware design of a smart servo controller built using an STM32 microcontroller and the DRV8801 motor driver. The board is designed for reliable PWM-based motor/servo control with fault monitoring, USB communication, and onboard power regulation.

---

## Key Features
- STM32-based control logic
- DRV8801 H-Bridge motor driver
- PWM, Direction, Enable, Sleep control
- Fault detection and current sensing
- USB to UART interface (FT232RL)
- Onboard 5V to 3.3V LDO regulation
- SWD programming and debugging support
- Modular headers for motor and control signals

---

## Major ICs Used
- **STM32L431CCT6** – Main microcontroller
- **DRV8801PWPR** – Motor / Servo driver
- **FT232RL** – USB to UART converter
- **AZ1117-3.3** – 3.3V voltage regulator

---

## Power Architecture
- Input Supply: **5V**
- Logic Supply: **3.3V**
- Motor Supply: **VBUS / VBB**
- Separate decoupling for analog and digital domains
- Bulk + ceramic capacitors placed close to ICs

---

## Motor Control Interface
- PWM input from STM32
- Direction control (PHASE)
- Enable and Sleep pins
- Current sensing via SENSE pin
- Fault output monitored by MCU
- Supports bidirectional motor/servo operation

---

## Communication & Debug
- USB interface via FT232RL
- UART TX/RX routed to MCU
- SWD interface:
  - SWDIO
  - SWCLK
  - NRST
- Onboard reset and boot configuration

---

## PCB Design Notes
- Proper ground stitching and decoupling
- Short high-current motor loops
- Separate analog and digital grounds
- USB differential pair routing (DP/DN)
- Thermal considerations for motor driver and LDO

 
---

## Applications
- Servo motor control
- Robotics
- Automation systems
- Embedded motor drivers
- Educational hardware projects

---

## Status
- ✔ Schematic completed
- ✔ Power and communication verified
- ⏳ PCB fabrication & bring-up pending
- ⏳ Firmware integration

---

## Disclaimer
This design is intended for educational and prototyping purposes. Review component ratings, thermal limits, and protection requirements before using in production or high-power applications.

---

## Author
Designed by **Harsh Saini**


