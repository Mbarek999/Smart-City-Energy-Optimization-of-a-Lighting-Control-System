# Smart-City-Energy-Optimization-of-a-Lighting-Control-System

This repository contains the implementation of an energy-efficient autonomous lighting control system for smart cities, combining embedded systems programming with IoT capabilities.

Project Overview
The system optimizes public lighting energy consumption through:

Real-time ambient light measurement

Adaptive PWM-based dimming control

Autonomous operation with manual override capability

Energy consumption monitoring and reporting

Key Features
Hardware Implementation
STM32 Microcontroller for real-time control:

Analog light sensor input via A/D converter

PWM generation for LED dimming

Analog comparator for energy-saving mode triggering

UART communication with Raspberry Pi

Raspberry Pi for system monitoring:

Data logging and visualization

Remote control interface

Energy consumption analytics

Software Architecture
STM32CubeIDE firmware featuring:

Interrupt-driven sensor reading

Timer-based PWM generation

Analog comparator for low-power mode

UART communication protocol

Python backend (Raspberry Pi):

Real-time data visualization

Historical energy consumption tracking

Threshold configuration interface
