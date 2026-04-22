<img width="768" height="512" alt="ChatGPT Image Apr 22, 2026, 02_44_59 PM" src="https://github.com/user-attachments/assets/76efc2c8-4db1-4d24-9250-a208991bb5f0" />

# BioScale

An embedded body composition analysis system built on the **ESP32** and **FreeRTOS** that estimates key health metrics using **weight sensing**, **bioelectrical impedance analysis (BIA)**, and user-provided physiological inputs.

**BioScale** is designed to go beyond traditional weighing scales by providing deeper insight into body composition, enabling users to better understand their health and track fitness progress.

---

## Overview

Most consumer scales only report body weight, offering limited insight into overall health. **BioScale** addresses this limitation by integrating multiple sensing subsystems and embedded computation into a single real-time system capable of estimating body composition metrics.

The system combines:

- **Load cell + ADC** for weight measurement  
- **Bioelectrical impedance sensing (BIA)** using controlled AC excitation  
- **ESP32 + FreeRTOS** for concurrent sensing, processing, and communication  
- **Laptop-assisted user input** for parameters such as age, sex, and height  
- **Host display interface** for presenting computed metrics  

---

## Key Features

- Real-time embedded implementation on **ESP32**
- Task-based architecture using **FreeRTOS**
- Calibrated **weight acquisition pipeline**
- **Bioelectrical impedance measurement** for impedance extraction
- Embedded computation of **Body Fat Percentage**
- UART-based communication with a host interface
- Extensible architecture for advanced body composition metrics

---

## System Architecture

**BioScale** is organized into the following subsystems:

### 1. Weight Measurement
A load cell and ADC are used to acquire stable and repeatable weight measurements.

### 2. Bioelectrical Impedance Measurement
A controlled AC excitation signal is applied through electrodes, and the resulting voltage is measured using a differential sensing path and instrumentation amplifier to estimate body impedance.

### 3. User Input Interface
A laptop interface is used to provide static user parameters such as age, sex, and height.

### 4. Embedded Processing
The ESP32 runs multiple FreeRTOS tasks responsible for:

- sensor acquisition  
- signal processing  
- metric computation  
- UART communication  

### 5. Host Display
Computed results are transmitted to a host interface for visualization.

---

## Tech Stack

### Embedded / Firmware
- ESP32  
- FreeRTOS  
- Embedded C  

### Hardware / Sensing
- Load Cell  
- ADC-based weight acquisition  
- Instrumentation amplifier  
- Electrode-based BIA sensing  
- Ultrasonic sensor (planned extension)  

### Communication / Interface
- UART serial communication  
- Laptop-based display / GUI  

---

## Engineering Focus

BioScale demonstrates:

- Real-time embedded system design  
- Multi-tasking using FreeRTOS  
- Sensor integration and signal acquisition  
- Mixed hardware/software system architecture  
- Embedded computation using physiological models  
- Reliable microcontroller-to-host communication  

---

## How It Works

1. The user enters static inputs (age, sex, height) through the host interface  
2. The user stands on the scale for weight measurement  
3. The BIA module captures impedance-related signals  
4. The ESP32 processes sensor data in real time  
5. Body composition metrics are computed and sent to the host display  

---

## Current Scope

### Core Implementation
- Weight sensing subsystem  
- Impedance acquisition pipeline  
- Host-assisted input flow  
- FreeRTOS-based task separation  
- UART-based result transmission  

### Planned Extensions
- Automated height estimation using ultrasonic sensing  
- Additional metrics:
  - Total Body Water  
  - Skeletal Muscle Mass  
  - BMI  
- Enhanced UI with historical tracking and visualization  

---

## Why BioScale

BioScale is not just a measurement device — it is a complete embedded system that combines:

- real-time processing  
- sensor fusion  
- system-level design  
- user-centric health insights  

This project demonstrates the ability to design and implement an end-to-end embedded system integrating both hardware and software components.

---

## Repository Contents

- Embedded firmware for ESP32  
- System architecture and documentation  
- Host communication components  
- Supporting diagrams and media  

