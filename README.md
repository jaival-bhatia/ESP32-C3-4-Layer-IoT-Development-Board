# ESP32-C3-4-Layer-IoT-Development-Board
A custom-designed 4-layer ESP32-C3 IoT development board featuring USB Type-C, Li-ion battery management, environmental sensing, OLED display, and expandable peripheral interfaces.


<div align="center">

![PCB Render](Images/3D_Top.png)

**A Custom 4-Layer ESP32-C3 Development Board for Battery-Powered IoT Applications**

[![KiCad](https://img.shields.io/badge/KiCad-PCB%20Design-blue)]()
[![ESP32-C3](https://img.shields.io/badge/ESP32-C3-red)]()
[![4-Layer PCB](https://img.shields.io/badge/PCB-4%20Layers-success)]()
[![USB Type-C](https://img.shields.io/badge/USB-Type--C-orange)]()
[![IoT](https://img.shields.io/badge/IoT-Embedded-green)]()
[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)]()

</div>

---

# Overview

This project presents a **custom-designed 4-layer ESP32-C3 IoT Development Board** built for low-power, battery-operated embedded applications. The board combines wireless connectivity, intelligent power management, onboard environmental sensing, expandable storage, and a compact PCB layout into a single development platform.

The primary objective of this project was to design a production-ready embedded hardware platform capable of supporting rapid IoT prototyping while following professional PCB design practices such as dedicated power and ground planes, optimized signal routing, proper decoupling, and manufacturing-ready documentation.

Designed entirely in **KiCad**, the board integrates battery charging, USB Type-C connectivity, environmental sensing, local data storage, and display capabilities, making it suitable for a wide range of embedded applications.

---

# Key Features

- 4-Layer PCB designed using KiCad
- ESP32-C3 Wi-Fi + Bluetooth Low Energy (BLE) SoC
- USB Type-C interface for programming and charging
- TP4056 Li-ion battery charging circuit
- Single-cell Li-ion battery support
- Onboard BME280 environmental sensor
- Ambient Light Sensor
- Sound Sensor Interface
- I²C OLED Display Connector
- SPI Flash Memory
- MicroSD Card Storage
- Battery Status LEDs
- Low-Power Embedded Design
- Expandable GPIO Header
- Manufacturing Ready (ERC/DRC Verified)

---

# Hardware Specifications

| Parameter | Description |
|------------|-------------|
| Microcontroller | ESP32-C3 |
| PCB Layers | 4 |
| Power Input | USB Type-C |
| Battery | 3.7V Li-ion |
| Charging IC | TP4056 |
| Connectivity | Wi-Fi + BLE |
| Display | OLED (I²C) |
| Sensors | BME280, Ambient Light, Sound |
| Storage | SPI Flash + microSD |
| Design Software | KiCad |

---

# System Architecture

```
                  USB Type-C
                       │
                       ▼
                TP4056 Charger
                       │
         ┌─────────────┴─────────────┐
         │                           │
         ▼                           ▼
   Li-ion Battery              USB Power
         │                           │
         └─────────────┬─────────────┘
                       ▼
                 3.3V Regulation
                       │
                       ▼
                  ESP32-C3 MCU
      ┌────────┬────────┬────────┬────────┐
      │        │        │        │
      ▼        ▼        ▼        ▼
   OLED     BME280   Flash    microSD
      │
      ▼
 Additional Sensors & GPIO Expansion
```

---

# Power Architecture

The board supports dual power operation through USB Type-C and a rechargeable Li-ion battery.

Power flow:

```
USB Type-C
      │
      ▼
TP4056 Charger
      │
      ▼
Li-ion Battery
      │
      ▼
Voltage Regulation
      │
      ▼
ESP32-C3 + Peripherals
```

The TP4056 charging IC provides:

- Constant Current Charging
- Constant Voltage Charging
- Automatic Charge Termination
- Thermal Protection
- Battery Status Indication

This enables safe battery charging while simultaneously powering the embedded system.

---

# Major Components

| Component | Function |
|-----------|----------|
| ESP32-C3 | Main Microcontroller |
| TP4056 | Li-ion Battery Charger |
| USB Type-C | Power & Programming |
| BME280 | Temperature, Humidity & Pressure |
| OLED Display | Real-time Visualization |
| Flash Memory | Firmware/Data Storage |
| microSD | External Data Logging |

---

# PCB Design Highlights

Highlights include:

- 4-Layer PCB Stack-up
- Dedicated Ground Plane
- Dedicated Power Plane
- Optimized Component Placement
- Short High-Speed Signal Routing
- Proper Decoupling Capacitor Placement
- Optimized Power Distribution
- Low-Noise Analog Routing
- Manufacturing Ready Layout
- ERC & DRC Verified




## Schematics

| Sheet | Description |
|--------|-------------|
| Sheet 1 | USB Type-C & Power Input |
| Sheet 2 | ESP32-C3 Core Circuit |
| Sheet 3 | Sensors & Interfaces |
| Sheet 4 | Battery Charging & Peripheral Connections |

<img width="1253" height="848" alt="Screenshot 2026-07-09 132526" src="https://github.com/user-attachments/assets/e30d0ebe-9a98-4f21-9a3d-ced49805c8c0" />
<img width="1188" height="818" alt="Screenshot 2026-07-09 132548" src="https://github.com/user-attachments/assets/7c92fd54-9b70-43f7-ae3c-dd6bdc3c5e46" />
<img width="1276" height="688" alt="Screenshot 2026-07-09 132630" src="https://github.com/user-attachments/assets/f6868cb6-d304-4a81-9897-d683def44e77" />
<img width="1427" height="833" alt="Screenshot 2026-07-09 132616" src="https://github.com/user-attachments/assets/3de380b3-b73c-4e9f-adf9-44a51eb5b90e" />



PCB 1st Layer
<img width="978" height="618" alt="image" src="https://github.com/user-attachments/assets/d88b1396-10a7-4f26-a1d7-b6973fe32ae0" />

PCB 2nd Layer
<img width="1005" height="605" alt="image" src="https://github.com/user-attachments/assets/533479ab-8f20-454b-8952-cf012f62b293" />

PCB 3rd Layer
<img width="913" height="582" alt="image" src="https://github.com/user-attachments/assets/17b969ca-8939-45ad-90f2-c8e324ed55eb" />

PCB 4th Layer
<img width="915" height="568" alt="image" src="https://github.com/user-attachments/assets/633571c4-8305-48a7-96d9-d0ce9d0f7a2a" />


