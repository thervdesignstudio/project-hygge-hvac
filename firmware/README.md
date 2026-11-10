# Project Hygge: Firmware & Embedded Architecture

[![License: MIT](https://img.shields.io/badge/Firmware-MIT-yellow.svg)](../LICENSE)
[![Platform: ESP32-S3](https://img.shields.io/badge/Hardware-ESP32--S3-blue.svg)](https://www.espressif.com/en/products/socs/esp32-s3)
[![Framework: ESPHome / ESP-IDF](https://img.shields.io/badge/Framework-ESPHome%20%7C%20ESP--IDF-red.svg)](#)

This directory contains the firmware, control logic, and bus communications for the **HICC (Hygge Integrated Cooling & Climate)** system. The platform is engineered around the **ESP32-S3** microcontroller, utilizing **TWAI (Two-Wire Automotive Interface / CANbus)** to orchestrate distributed sensors, relays, and HVAC actuators across the vehicle.

> **⚠️ IMPORTANT SAFETY & EDUCATIONAL DISCLAIMER**  
> This repository documents an experimental personal build for educational and research purposes. 
> It is NOT a certified installation manual or professional engineering service. 
> Modifying vehicle HVAC, high-current 24V DC systems, or diesel fuel lines carries inherent 
> risks of fire, injury, or property damage. Use all code, CAD, and schematics at your own risk.
---

## 🏗️ System Architecture

The firmware relies on a distributed node topology to separate real-time thermal management from cloud/local user interface layers:

```text
[ Home Assistant ] <--- WiFi / Native API ---> [ Main Node: ESP32-S3 ]
                                                    |
                                            (CANbus / TWAI 500kbps)
                                                    |
                         +--------------------------+--------------------------+
                         |                                                     |
             [ Node 1: HVAC Main ]                                [ Node 2: Sub-floor ]
             - TKT-30UBDC A/C Relay                               - Radiant Floor Valves
             - HLN Aquano Diesel Furnace                          - Topsflo Glycol Pumps
             - Reheat Air Coils                                   - Temp / Pressure Sensors
