> 🇬🇷 Ελληνική έκδοση: [README_GR.md](./README_GR.md)

# Embedded Systems – Head-Up Display (HUD)
### Course: Embedded Systems
### 4th Year – 7th Semester

This repository contains my final project for the elective course
**Embedded Systems**, focusing on the **system-level design and analysis**
of an automotive **Head-Up Display (HUD)** embedded system.

The work is presented as a **technical and architectural study**, covering
requirements, hardware and software architecture, subsystem design, and
performance considerations.  
No source code is included at this stage.

---

## 🧠 Project Overview

The proposed embedded system is an automotive **Head-Up Display (HUD)** that
provides real-time information to the driver, including:

- vehicle speed and engine RPM
- fuel consumption (instantaneous & average)
- coolant temperature and battery voltage
- tire pressure and temperature (via external sensors)
- engine fault and safety warnings
- smartphone-based navigation display (via Bluetooth)

All information is projected onto a transparent display on the windshield,
allowing the driver to remain focused on the road.

---

## ⚙️ System Requirements & Constraints

The system is designed to operate under real-time constraints and meet:

- real-time data updates (≤ 100 ms refresh rate)
- low power consumption (automotive 12V supply)
- compact physical size (dashboard-mounted)
- low production cost (target: ~50–60 € hardware cost)
- safe and non-distracting user interaction

---

## 🧩 Hardware Architecture

The proposed hardware architecture includes:

- **32-bit Microcontroller (MCU)**  
  - ~100 MHz clock frequency  
  - Integrated Flash & SRAM  
  - ADC channels for sensor input  
  - Timers and external interrupts  

- **Memory**
  - SRAM for temporary data storage
  - NAND Flash for firmware and configuration storage

- **Peripherals & Interfaces**
  - CAN transceiver (OBD interface)
  - Bluetooth module (smartphone connectivity)
  - GPS module
  - Display controller
  - Audio codec & speaker
  - External pressure & temperature sensors

- **Power Management**
  - PMIC
  - Battery management circuitry

---

## 🧠 Software Architecture

The software architecture is designed around:

- real-time data acquisition from vehicle and sensors
- periodic task execution using timers
- user interface management via physical buttons
- warning and alert generation based on thresholds
- resource-aware task scheduling

The system is designed to operate **without a general-purpose OS**,
following a bare-metal or lightweight embedded runtime approach.

---

## 🔬 Sensor Subsystem Analysis

A detailed theoretical implementation of the sensor subsystem is provided,
including:

- signal conditioning and amplification
- anti-aliasing filtering
- sampling theory and Nyquist criteria
- 16-bit ADC quantization
- multiplexing of multiple sensor inputs
- data encoding and register storage

Estimated measurements and error analysis are derived using datasheet-based
equations.

---

## 🚀 Future Work

This project currently focuses on **theoretical design and system architecture**.

As future work, the system is intended to be **implemented in practice** using:

- **Embedded C**
- a **low-cost, commercially available SoC or MCU development board**
- real sensors and peripherals

The goal is personal learning and experimentation, targeting an affordable,
hobby-friendly platform suitable for hands-on embedded development.

---

## 📁 Repository Contents

- Technical report (PDF)
- Project presentation slides
- System diagrams and architectural analysis

---

## 🔐 License

This repository contains personal academic work.
It is shared for **educational and reference purposes only**.

**All Rights Reserved.**
