# SkySense V1
### A Compact Drone Sensor Expansion Module

## Features

- **ESP32-C3 Microcontroller** — Processing, communication, and programmable functionality.
- **BMP280 Barometric Sensor** — Atmospheric pressure and temperature measurements, with estimated altitude calculations.
- **ICM-42688-P IMU** — 3-axis acceleration and 3-axis angular velocity measurements.
- **USB-C Interface** — Native USB programming and debugging, with external board power.
- **UART Interface** — 4-pin JST-GH connector for communication with a compatible flight controller.
- **RGB Status LED** — Programmable visual status indication.
- **BOOT and RESET Buttons** — Manual firmware download and reset control.
- **Mounting Holes** — Designed for secure installation.

## Hardware Specifications

| Component | Model / Specification |
|---|---|
| Microcontroller | ESP32-C3-MINI-1-N4 |
| Barometric Sensor | BMP280 |
| Motion Sensor | ICM-42688-P |
| Voltage Regulator | AP2112K-3.3 |
| RGB LED | WS2812B-1313-V6 |
| USB | USB Type-C |
| Drone Interface | 4-pin JST-GH |
| Input Power | Regulated 5V via JST |
| Logic Voltage | 3.3V |
| PCB | 2-layer |

## Flight Controller Connection

SkySense uses a 4-pin JST-GH connector for power and UART communication.

| Signal | Description |
|---|---|
| +5V | Regulated power input |
| GND | Common ground |
| TXD0 | SkySense UART transmit |
| RXD0 | SkySense UART receive |

**Important:** TXD0 connects to the flight controller's RX, and RXD0 connects to its TX. Compatible voltage levels and firmware protocols are required.

USB-C is intended for data/programming, not for independently powering the board.

## How SkySense Works

1. The flight controller supplies regulated 5V power.
2. The AP2112K regulator generates 3.3V for the electronics.
3. The BMP280 measures atmospheric pressure and temperature.
4. The ICM-42688-P measures acceleration and angular velocity.
5. The ESP32-C3 processes the sensor readings.
6. Firmware can transmit measurements over UART to a compatible flight controller or other host.

The communication protocol and sensor-processing firmware are still under development.

### PCB Preview

<img width="810" height="685" alt="image" src="https://github.com/user-attachments/assets/6b5b6afb-c084-4c05-b131-436e79068d13" />

<img width="882" height="664" alt="image" src="https://github.com/user-attachments/assets/b66a3b77-ac4d-425e-81e5-f77b707d0137" />

### Schematic

<img width="1169" height="828" alt="image" src="https://github.com/user-attachments/assets/22e870ae-29d1-40ab-94aa-51ded36474b3" />

### PCB Layout

<img width="787" height="682" alt="image" src="https://github.com/user-attachments/assets/76826687-0f06-4cd0-99a1-a68d2784eb0f" />

#### Top Layer 

<img width="897" height="747" alt="image" src="https://github.com/user-attachments/assets/e1fbeb42-2df2-45ef-9484-8a400404e266" />

#### Bottom Layer

<img width="907" height="750" alt="image" src="https://github.com/user-attachments/assets/7ef63150-5388-47d6-a5fc-7c09bd838bb7" />



