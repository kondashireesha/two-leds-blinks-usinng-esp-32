# ESP32 Two LEDs Blink using ESP-IDF

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
Two_led_blink/
├── main/
│ ├── blink.c // Main application file
│ └── CMakeLists.txt // Source CMake file
├── CMakeLists.txt // Root CMake file
├── .gitignore // Ignored build files
└── README.md // Project details
