# Fundamentals of IoT – Laboratory Repository

## Overview

This repository collects the lab experiments and hands-on implementations completed for the **Fundamentals of Internet of Things (FIoT) Lab** course at **Shiv Nadar University, Chennai**.

Folders follow the CAT (Continuous Assessment Test) numbering used in the coursework, with each CAT's exercises grouped beneath it. The experiments target two microcontroller families: the **8051** and **STM32**.

## Repository Structure

```text
FIoT_LAB/
│
├── 8051/
│   ├── CAT2/
│   ├── CAT3/
│   ├── CAT4/
│   ├── CAT5/
│   ├── CAT6/
│   └── CAT7/
│
├── STM32/
│   ├── CAT8/
│   ├── CAT9/
│   ├── CAT10/
│   ├── CAT11/
│   ├── CAT12/
│   ├── CAT13/
│   ├── CAT14/
│   └── CAT15/
│
├── README.md
└── .gitignore
```

Every CAT folder holds its task sub-folders along with the associated implementation files.

## Tools and Technologies

The experiments draw on the following hardware, software and techniques:

- **8051 microcontroller**
- **STM32F103C8T6 Blue Pill** (CAT8 – CAT10)
- **STM32F401RE (Nucleo / STM32F4 board)** (CAT11 – CAT15)
- STM32CubeMX
- Keil MDK-ARM
- Embedded C
- STM32 HAL libraries
- Peripheral interfaces such as GPIO, UART and I2C
- ESP8266 Wi-Fi module
- MQTT messaging
- BME280 environmental sensor

## Documentation per Experiment

Where relevant, each experiment folder provides:

- Embedded C source code
- Microcontroller project and configuration files
- Circuit diagrams
- A dedicated README describing the experiment
- Observations and implementation notes

Experiments are ordered by CAT number, and the individual tasks sit inside their CAT folder.

## Purpose

The repository is a working record of the IoT lab: the microcontroller programs, peripheral communication protocols, sensor interfacing, wireless connectivity and IoT messaging techniques practised through hands-on experiments over the course.
