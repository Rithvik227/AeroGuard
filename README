Project AeroGuard: Firmware & System Logic

SkillsUSA Engineering Technology-Design (2024-2026)
Institution: William Mason High School
Lead Electronics & Firmware: Rithvik Godishala
Mechanical Design: Abinav Valluri
Project Management: Sushil Kumaresan

System Overview:
This repository contains the C++ firmware for Project AeroGuard, a low-cost (<$50) wearable air quality monitoring system engineered for high-risk industrial environments. 
The system utilizes an ESP32-C3 microcontroller to actively sample Volatile Organic Compounds (VOCs) and triggers a haptic feedback mechanism to alert users in high-noise 
environments where traditional audible alarms are ineffective.

This hardware and software integration directly addresses UN Sustainable Development Goals 3 (Good Health and Well-being) and 11 (Sustainable Cities and Communities).

 Hardware Architecture
 Microcontroller: ESP32-C3 SuperMini (Selected for ultra-low power consumption and minimal Z-height footprint)
 Sensor Array: BME680 (Environmental telemetry including Temperature, Humidity, Pressure, and VOC Gas Resistance)
 Display: 0.96" I2C OLED Display
 Alert Mechanism: 3V Haptic Vibration Motor (Driven via NPN Transistor)
 Power Management: 3.7V LiPo Battery integrated with a TP4056 Charging Module

Pin Configuration:
Component: ESP32-C3 Pin, Interface, Function

BME680 SDA: GPIO 6, I2C Data
BME680 SCL: GPIO 7, I2C Clock
OLED SDA: GPIO 5, I2C Data
OLED SCL: GPIO 4, I2C Clock
Haptic Motor: GPIO 3, Digital Out (Alert Trigger)

 Software Dependencies
To compile this firmware in the Arduino IDE or PlatformIO, the following dependencies must be installed:
`Adafruit_BME680`
`Adafruit_Sensor`
`Adafruit_SSD1306`
`Adafruit_GFX`

Core Logic & Polling Algorithm
Upon initialization, the firmware runs a boot sequence to establish a clean-air VOC baseline. 
The main execution `loop()` polls the BME680 sensor continuously.

If the environmental gas resistance drops below the calculated baseline threshold—indicating a sudden concentration of VOCs (e.g., industrial solvents, dry-erase marker solvent,
or construction fumes)—the ESP32 asserts the haptic motor pin HIGH.

Instructions
1. Install the ESP32 Board Support Package within the Arduino IDE.
2. Select the  target environment.
3. Interface the ESP32-C3 to the host machine via USB-C.
4. Verify the I2C pin mappings align with the active hardware revision.
5. Compile and flash `AeroGuard_Main.ino` to the MCU.
