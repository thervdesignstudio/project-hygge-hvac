# Project Hygge: Firmware License & Architecture (HICC)

[![License: MIT](https://img.shields.io/badge/Firmware-MIT-yellow.svg)](../LICENSE)
[![Platform: ESP32-S3](https://img.shields.io/badge/Platform-ESP32--S3-blue.svg)](https://www.espressif.com)

This document governs the licensing, system specifications, and structural directory links for the embedded firmware within **Project Hygge / HICC (Hygge Integrated Climate Control)**, maintained by **The RV Design Studio**.

---

## ⚡ System Specifications & Scope

The firmware in this directory is engineered specifically to control native 24V off-grid thermal systems, including:
* **Controller Hardware**: ESP32-S3 microcontrollers communicating via TWAI / CANbus (500kbps).
* **Thermal Actuators**: HLN Aquano 5K Diesel Furnace (17,000 BTU), TKT-30UBDC 24V Under-bench A/C Compressor, and Topsflo TL-B10 Glycol Circulation Pumps.
* **Automation Platform**: ESPHome / Home Assistant native local telemetry and PID climate loops.

---

## ⚖️ MIT License (Firmware Module)

All C++, Python, YAML, and configuration files contained within the `/firmware/` directory are licensed under the **MIT License** reproduced below, unless explicitly noted otherwise in individual file headers.

```text
MIT License

Copyright (c) 2026 The RV Design Studio (Project Hygge)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
