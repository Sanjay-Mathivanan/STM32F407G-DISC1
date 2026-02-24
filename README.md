# STM32F407 Embedded Systems Projects

## 📌 Repository Overview

This repository contains embedded firmware projects developed using the STM32F407G-DISC1 development board and STM32CubeIDE.

The purpose of this repository is to document practical hands-on learning of ARM Cortex-M4 microcontroller programming, peripheral configuration, and embedded system design.

---

## 🧠 Hardware Platform

- Board: STM32F407G-DISC1
- MCU: STM32F407VGT6
- Core: ARM Cortex-M4
- Architecture: 32-bit
- Clock: Up to 168 MHz

---

## 🛠 Development Environment

- IDE: STM32CubeIDE
- Debugger: ST-LINK
- Drivers: STM32 HAL
- Language: Embedded C

---

## 📂 Project Structure

```
Docs/                     → Detailed technical documentation
external_led_blink/       → GPIO-based external LED project
```

Each project folder contains:
- Core source files
- HAL drivers
- .ioc configuration file
- Linker scripts
- Project configuration files

---

## 📘 Documentation Included

The `Docs/` folder contains detailed explanations of:

- Microcontroller Overview
- ARM Cortex-M4 Architecture
- Memory Map
- Clock System
- GPIO Configuration
- Interrupt & NVIC
- HAL vs Register-Level Programming
- Development Setup
- Common Debugging Errors
- Learning Roadmap

This makes the repository both a project collection and a learning reference.

---

## 🚀 Current Projects

### 1️⃣ External LED Blinking

- GPIO Output configuration
- External hardware interfacing
- HAL-based implementation
- Register-level alternative included

Pin used: PA5  
Function: Toggle LED every 500ms

---

## 🎯 Learning Objectives

This repository helps develop understanding of:

- GPIO configuration
- Clock management
- Interrupt handling
- Embedded firmware structure
- HAL driver usage
- Register-level programming
- Debugging embedded systems
- Hardware interfacing

---

## 🔌 How to Use

1. Clone the repository
2. Open project folder in STM32CubeIDE
3. Build the project
4. Flash using ST-LINK
5. Test on hardware

---

## 🧪 Future Projects

- Button interrupt handling
- Timer-based LED blinking
- PWM LED dimming
- UART communication
- ADC sensor reading
- DMA-based communication
- FreeRTOS examples

---

## 📈 Goal

The long-term goal of this repository is to build industry-level embedded systems expertise using STM32 microcontrollers.

This repository will continuously evolve with more advanced firmware implementations and structured documentation.

---

## 👨‍💻 Author

Developed as part of structured embedded systems learning and project practice.
