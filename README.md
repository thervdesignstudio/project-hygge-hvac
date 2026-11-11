# project-hygge-hvac
Open-source 24V hydronic HVAC and climate control architecture for custom RVs and travel trailers.

[![License: MIT](https://img.shields.io/badge/Firmware-MIT-yellow.svg)](LICENSE)
[![License: CERN-OHL-P v2](https://img.shields.io/badge/Hardware-CERN--OHL--P_v2-blue.svg)](HARDWARE_LICENSE)
[![License: CC BY 4.0](https://img.shields.io/badge/Docs-CC_BY_4.0-lightgrey.svg)](DOCS_LICENSE)
[![Build Status](https://img.shields.io/badge/Status-v1.0.0--alpha-green.svg)](#)
[![Community](https://img.shields.io/badge/Studio-The_RV_Design_Studio-copper?color=B87333)](https://thervdesignstudio.com)

Welcome to the official repository for **Project Hygge** / **HICC (Hygge Integrated Cooling & Climate)**—an open-source, high-efficiency climate control system engineered specifically for off-grid travel trailers, van conversions, and overland builds. 

Maintained by **The RV Design Studio**, this project provides production-ready firmware, schematics, 3D printable PETG/ASA components, and complete Bills of Materials (BOM) to build a native 24V hydronic heating and integrated cooling system.

> **⚠️ IMPORTANT SAFETY & EDUCATIONAL DISCLAIMER**  
> This repository documents an experimental personal build for educational and research purposes. 
> It is NOT a certified installation manual or professional engineering service. 
> Modifying vehicle HVAC, high-current 24V DC systems, or diesel fuel lines carries inherent 
> risks of fire, injury, or property damage. Use all code, CAD, and schematics at your own risk.
---

## 🛠️ System Overview & Specifications

Project Hygge replaces inefficient roof-top A/C units and standalone propane heaters with a unified 24V under-bench architecture featuring hydronic radiant floor heating, fresh-air reheat capability, and variable-capacity cooling.

| Component | Technical Specification |
| :--- | :--- |
| **System Architecture** | Hydronic Radiant Floor / Hydronic-to-Air / Under-bench AC w/ Dehumidification |
| **Nominal System Voltage** | 24V DC Native |
| **A/C Cooling Capacity** | TKT-30UBDC / 8,500 BTU / R134a / 430W–850W (10A–35A @ 24V) |
| **Heating Furnace** | HLN Aquano 5K Diesel / 17,000 BTU (5kW) |
| **Auxiliary Electric Heat** | 600W 24V Submerged Element |
| **Fluid Circulation** | Topsflo TL-B10-C24-1208 Brushless Circulation Pumps (2Gal Glycol Loop) |
| **Air Handler Coils** | PKSABB Universal Cross-Flow Bar & Plate Oil Coolers (-10AN Male) |
| **Control System** | ESP32-S3 Nodes via CANbus / Optocoupled MOSFET Relays / Home Assistant |

---

## 📂 Repository Structure

The codebase and hardware files are structured into four primary modules:

```text
├── firmware/         # ESP32 C++ / ESP-IDF source code, CANbus node logic, ESPHome / Home Assistant YAMLs / Software
├── cad/              # Step files, 3D printing models (PETG/ASA), and CNC router DXF profiles
├── schematics/       # KiCad schematics, 24V DC wiring diagrams, optocoupled relay layouts, PEX plumbing
└── docs/             # Bill of Materials (BOM), assembly guides, commissioning procedures, safety warnings
