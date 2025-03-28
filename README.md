# River Cleaning Robot Using GPS

## Introduction

The increasing pollution of water bodies threatens aquatic life and human health. Manual cleaning of rivers and lakes is time-consuming, expensive, and sometimes dangerous. This project proposes a **River Cleaning Robot** using GPS that efficiently removes floating and submerged debris from water bodies. Equipped with sensors and GPS technology, the robot navigates autonomously to locate and clean targeted areas. This innovative approach ensures cost-effective and efficient water cleaning while enhancing the safety of personnel.

---

## Objectives

- Collect non-living garbage from water bodies using a robot.
- Provide cost-effective solutions for surface cleaning and garbage collection.
- Improve aquatic waste management efficiency to align with **Smart City** and **Clean India Mission** goals.

---

## Problem Statement

- Water pollution poses a serious threat to human and aquatic life.
- Manual cleaning is inefficient, costly, and hazardous.
- There is a need for an autonomous and eco-friendly river-cleaning robot utilizing GPS.

---

## Hardware Requirements

1. **Arduino Uno(ATMEGA328PU)**: Microcontroller board based on ATmega328P.
2. **APM 2.8 flight controller+NEO GPS M8N(Ardupilot Mega) Module**:module typically includes both a gps receiver provides location, while the campass gives direction
3. **GPS Module(GT-U7)**: Provides accurate location and time information.
4. **Compass Module(HMC5883L)**: Measures magnetic field direction.
5. **Motor Driver(L293D)**: Controls the speed and direction of motors.
6. **DC Motors**: Converts electrical energy into mechanical motion.
7. **3800MAH [18650] Li-Ion Cell Reachargeble Battery**:to give power suppply

---

## Software Requirements

- **Operating System**: Windows (latest versions) or Linux.
- **IDE**: Arduino IDE (versions 1.x or 2.x).
- **serial blouetooth terminal app**:to run the robot

**Arduino IDE** allows users to write, compile, and upload code to Arduino boards, supporting various platforms like Windows, macOS, and Linux.

---

## Block Diagram

![Block Diagram](https://github.com/Aishwaryan172/River-Cleaning-Robot-Using-GPS/blob/main/Block%20Diagram%20of%20the%20River%20Cleaning%20Robot.png)

**Figure**: Block Diagram of the River Cleaning Robot

---

## Methodology

1. The user enters GPS waypoints defining the cleaning area.
2. The **GPS module** determines the robot's current position.
3. The **compass module** identifies the heading direction.
4. The robot calculates the distance and adjusts direction to reach the waypoint.
5. After completing one waypoint, the robot moves to the next, ensuring comprehensive cleaning of the water body.

---

## Architecture

![Architecture](https://github.com/Aishwaryan172/River-Cleaning-Robot-Using-GPS/blob/main/Architecture%20of%20the%20River%20Cleaning%20Robot.png)
---
**Figure**: Architecture of the River Cleaning Robot
---
![Pin Diagram](https://github.com/Aishwaryan172/River-Cleaning-Robot-Using-GPS/blob/main/Pin%20Diagram%20of%20the%20River%20Cleaning%20Robot.png)
---
**Figure**: Pin Diagram of the River Cleaning Robot

Circuit Connections:
1. APM Module (GPS & Compass) → Arduino Uno
    VCC & GND → Power connections to the Arduino.
    SCL & SDA → Connected to Arduino’s I2C pins (A5 & A4) for compass data.
    TX & RX → Communicates GPS data with Arduino’s Serial Pins (TX-RX).

2. Bluetooth Module → Arduino Uno
    VCC & GND → Power supply from Arduino.
    TX (Bluetooth) → RX (Arduino)
    RX (Bluetooth) → TX (Arduino)

Bluetooth allows users to control or monitor the robot via a mobile app or PC.

3. Motor Driver → Arduino Uno
    VCC & GND → Power connections from the power supply.
    IN1, IN2, IN3, IN4 → Connected to Arduino’s digital pins (for motor direction control).
    Motor Outputs → Connected to the DC motors of the robot.

4. Power Supply → All Components
    VCC & GND from battery/power source are distributed to Arduino, APM, Bluetooth module, and motor driver.
    Working of the Circuit:
    The APM module (GPS) tracks the robot’s location and movement.
    The compass (magnetometer in APM) helps maintain direction.
    The Bluetooth module allows remote monitoring and control.
    The Arduino Uno processes all data and controls the motor driver.
    The Motor driver moves the robot based on GPS navigation or user control.

