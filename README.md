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


| Name | Quantity | Price | Supplier Part ID | Link |
| :--- | :--- | :--- | :--- | :--- |
| 10uF | 3 | | C105225 | [Link](https://item.szlcsc.com/15869.html) |
| 100nF | 5 | 0.003 | C1525 | [Link](https://item.szlcsc.com/15869.html) |
| 10nF | 1 | 0.004 | C15195 | [Link](https://item.szlcsc.com/15869.html) |
| 2.2uF | 1 | 0.022 | C2897300 | [Link](https://item.szlcsc.com/15869.html) |
| 10uF | 1 | 0.032 | C380314 | [Link](https://item.szlcsc.com/362304.html) |
| 100nF | 1 | 0.009 | C14663 | [Link](https://item.szlcsc.com/362304.html) |
| BM04B-GHS-TBT(LF)(SN) | 1 | 0.71 | C161692 | [Link](https://lcsc.com/product-detail/Wire-To-Board-Wire-To-Wire-Connector_JST-Sales-America_BM04B-GHS-TBT-LF-SN_JST-Sales-America_BM04B-GHS-TBT-LF-SN_C161692.html) |
| 5.1kΩ | 2 | 0.002 | C23186 | [Link](https://www.mouser.in/datasheet/2/447/PYu_RT_1_to_0_01_RoHS_L_11-1669912.pdf) |
| 4.7kΩ | 2 | 0.003 | C23162 | [Link](https://www.mouser.in/datasheet/2/447/PYu_RT_1_to_0_01_RoHS_L_11-1669912.pdf) |
| 330Ω | 1 | 0.002 | C23138 | [Link](https://www.mouser.in/datasheet/2/447/PYu_RT_1_to_0_01_RoHS_L_11-1669912.pdf) |
| 10kΩ | 2 | 0.002 | C25804 | [Link](https://www.mouser.in/datasheet/2/447/PYu_RT_1_to_0_01_RoHS_L_11-1669912.pdf) |
| B3U-1000P | 2 | 0.189 | C231329 | [Link](https://item.szlcsc.com/260788.html) |
| ESP32-C3-MINI-1-N4 | 1 | 3.067 | C2838502 | [Link](https://atta.szlcsc.com/upload/public/pdf/source/20210720/C2838502_820C448AE0C4DF1D4546A4A5DCA77C73.pdf) |
| BMP280 | 1 | 13.148 | C83291 | [Link](https://atta.szlcsc.com/upload/public/pdf/source/20200702/C83291_F39E84AB7DFC569A4C7554F8659640A1.pdf) |
| ICM-42688-P | 1 | 20.178 | C1850418 | [Link](https://lcsc.com/product-detail/Sensors_Bosch_BMG250_BMG250_C189521.html) |
| AP2112K-3.3TRG1 | 1 | 0.18 | C51118 | [Link](https://atta.szlcsc.com/upload/public/pdf/source/20180521/C216647_DB6DD3A958B257C676AC8B0A0A0AE735.pdf) |
| WS2812B-1313-V6 | 1 | 0.109 | C52941388 | [Link](https://atta.szlcsc.com/upload/public/pdf/source/20240229/B8051D75F82007E6B8E5AD9424D7210B.pdf) |
| TYPE-C-31-M-12 | 1 | 0.189 | C165948 | [Link](https://item.szlcsc.com/datasheet/TYPE-C-31-M-12/177331.html?spm=sc.gbn.xds.a___sc.gbn.hd.ss&lcsc_vid=RgMNUVYEQARbV1xTElVcVwIAFFBXVwBfEQdfX1UCRAcxVlNTQFBcUlFXT1hYVTsOAxUeFF5JWA0NAgAHWQIASA%3D%3D) |




