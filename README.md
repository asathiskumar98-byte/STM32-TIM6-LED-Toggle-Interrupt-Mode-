# STM32 TIM6 LED Toggle (Interrupt Mode)

This project demonstrates how to use **Timer 6 (TIM6)** on the **STM32F446RE Nucleo board** to toggle an LED (PA5) every fixed time interval using **interrupts (ISR)**.

---

## ⚙️ Project Overview

- TIM6 is configured to generate an **update interrupt** every 1 second.  
- Inside the `TIM6_DAC_IRQHandler()`, the **LED (PA5)** toggles.  
- The LED blinks continuously without using any delay functions — fully interrupt-driven.  
- Built using **STM32CubeIDE** and **HAL libraries**.

---

## 🧩 Hardware Setup

| Pin  | Function | Description |
|------|-----------|-------------|
| PA5  | Output | LED (active HIGH, toggles on each interrupt) |

---

## 🔧 Configuration Summary

| Parameter | Value |
|------------|--------|
| **Timer** | TIM6 |
| **Prescaler** | 15999 |
| **Period** | 1000 |
| **Clock Source** | Internal |
| **Interrupt Mode** | Enabled |
| **Core Clock** | 16 MHz (HSI) |
| **LED Pin** | GPIOA PIN 5 |

---

## 🧰 Tools Used
- **STM32CubeIDE 1.x**
- **STM32CubeMX**
- **HAL Library**
- **Nucleo-F446RE Board**

---

## 🚀 How to Run
1. Open the project in **STM32CubeIDE**.  
2. Build and flash it to your **Nucleo-F446RE**.  
3. Observe the **onboard LED (PA5)** blinking at a 1-second interval — all handled via **TIM6 interrupts**.
- Real-time applications  
- Interrupt-based timing for motor control or sensor polling
