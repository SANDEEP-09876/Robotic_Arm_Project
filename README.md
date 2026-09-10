# SmartElex Motor Driver Connections

| SmartElex Pin | NodeMCU Pin | Function |
|----------------|-------------|----------|
| L_PWM yellow | D7 (GPIO13) | Left Motor Speed |
| L_DIR white | D3 (GPIO0) | Left Motor Direction |
| R_PWM | D8 (GPIO15) | Right Motor Speed |
| R_DIR | D4 (GPIO2) | Right Motor Direction |
| GND | G (GND) | Common Ground |

---

# PCA9685 Connections

| PCA9685 Pin | NodeMCU Pin | Description |
|--------------|-------------|-------------|
| VCC | VIN | Logic Power |
| GND | G (GND) | Common Ground |
| SDA | D2 (GPIO4) | I2C Data |
| SCL | D1 (GPIO5) | I2C Clock |


# Ultrasonic sensor 
NodeMCU Pin (Label),Sensor Pin,Function
D5,Trig,Trigger Pulse
D6,Echo,Distance Echo (Via Resistors)
Vin,VCC,5V Power for Sensor
G,GND,Sensor Ground



# Phase 2: ESP32 Autonomous Robotics Base

This document outlines the hardware pin mapping and wiring guide for the ESP32 (30-Pin) microcontroller used in Phase 2 of the autonomous robotics project.

## 🔌 ESP32 (30-Pin) Pin Mapping Table

| Component | Component Pin | ESP32 Pin | Description |
| :--- | :--- | :--- | :--- |
| **PCA9685 Servo Driver** | `SDA` | `GPIO 21` | $I^2C$ Serial Data |
| | `SCL` | `GPIO 22` | $I^2C$ Serial Clock |
| | `VCC` | `3V3` | Logic Power (3.3V) |
| | `GND` | `GND` | Common System Ground |
| **SmartElex L298N Motor Driver** | `L_PWM` | `GPIO 13` | Left Motor Speed (PWM) |
| | `L_DIR` | `GPIO 12` | Left Motor Direction |
| | `R_PWM` | `GPIO 14` | Right Motor Speed (PWM) |
| | `R_DIR` | `GPIO 27` | Right Motor Direction |
| | `GND` | `GND` | Shared System Ground |

## ⚠️ Critical Wiring & Safety Rules
1. **Common Ground:** You **must** connect the ESP32 `GND` pin directly to the L298N ground terminal. Without a shared common ground reference, control signals will float and motors will behave erratically.
2. **Power Isolation:** Never connect high-current motor battery packs (6V/12V) directly into the ESP32 pins. Keep motor power isolated to the L298N and PCA9685 screw terminal blocks.
3. **Strapping Pins:** Avoid using restricted flash memory pins (GPIO 6-11) for external peripherals to prevent boot-loop panics.
