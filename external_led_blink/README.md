# External LED Blinking – STM32F407

## 📌 Project Overview

This project demonstrates how to control an external LED using GPIO on the STM32F407G-DISC1 development board.

The LED is connected to GPIO pin PA5 and toggled every 500 milliseconds using STM32 HAL drivers.

This project verifies:

- GPIO configuration
- Clock initialization
- External hardware interfacing
- Basic embedded firmware structure
- HAL-based peripheral control

---

## 🧠 Microcontroller Used

- Board: STM32F407G-DISC1
- MCU: STM32F407VGT6
- Core: ARM Cortex-M4
- Default Clock: 16 MHz (HSI)

---

## 🔌 Hardware Requirements

- STM32F407G-DISC1 board
- 1 × LED
- 1 × 220Ω–330Ω resistor
- Jumper wires

---

## 🔗 External LED Connection

### Wiring Diagram

PA5  ----  330Ω Resistor  ----  LED (Anode/Long leg)  
LED (Cathode/Short leg)  ----  GND

### Connection Table

| STM32 Pin | Connect To |
|-----------|------------|
| PA5       | One side of resistor |
| Resistor  | LED Anode (long leg) |
| LED Cathode | GND |

Important Notes:

- Always use a resistor to limit current.
- Do NOT connect LED directly to GPIO pin.
- STM32 GPIO works at 3.3V.
- Ensure LED GND is connected to board GND.

---

## ⚙ GPIO Configuration (STM32CubeIDE)

Inside `.ioc` file:

- Select PA5
- Set Mode: GPIO_Output
- Output Type: Push-Pull
- Pull: No Pull
- Speed: Low

Generate code after configuration.

---
Code Explanation

HAL_GPIO_TogglePin() → Toggles LED state (ON ↔ OFF)

HAL_Delay(500) → Waits 500 milliseconds

while(1) → Infinite loop

Result:
The external LED blinks every 0.5 seconds.

🔬 Register-Level Alternative (Advanced)

Clock enable:

RCC->AHB1ENR |= (1 << 0);

Configure PA5 as output:

GPIOA->MODER |= (1 << 10);

Toggle LED:

GPIOA->ODR ^= (1 << 5);

This method provides faster execution and deeper hardware control.

🛠 Build & Flash Instructions

Open project in STM32CubeIDE

Connect USB to ST-LINK port

Click Build

Click Run (▶)

Observe LED blinking

🧪 Troubleshooting

If LED does not blink:

Check LED polarity

Verify resistor connection

Confirm PA5 configured correctly

Ensure GPIOA clock is enabled

Check board power LED

Verify correct GND connection

📚 Learning Outcomes

After completing this project, you understand:

GPIO configuration in STM32

Clock enable requirement

HAL driver usage

External hardware interfacing

Basic embedded debugging

