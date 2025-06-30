# ESP32 Two LEDs Blink using esp-32 in ESP-IDF

This project demonstrates how to blink two LEDs **alternately** using an ESP32 development board and the **ESP-IDF framework**.

## 🔧 Requirements

- ESP32 board (e.g., DevKit v1)
- Two LEDs
- Two resistors (220Ω recommended)
- Breadboard and jumper wires
- [ESP-IDF](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/) v5.x installed

## ⚙️ Connections

| LED | ESP32 GPIO |
|-----|------------|
| LED1 | GPIO2     |
| LED2 | GPIO4     |

> Connect resistors in series with LEDs to avoid damage.

## 🧠 Code Overview

- GPIO2 and GPIO4 are configured as output pins
- LEDs are toggled every 500ms
- The logic alternates the ON/OFF state between both LEDs

## 📂 Project Structure
two_led_blink/
├── main/
│ ├── blink.c // Main application code
│ └── CMakeLists.txt // Component CMake file
├── CMakeLists.txt // Root CMake file
├── sdkconfig // ESP-IDF config file
└── README.md // This file
