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

1. **Arduino Uno**: Microcontroller board based on ATmega328P.
2. **GPS Module**: Provides accurate location and time information.
3. **HMC5883L Compass Module**: Measures magnetic field direction.
4. **Motor Driver**: Controls the speed and direction of motors.
5. **DC Motors**: Converts electrical energy into mechanical motion.

---

## Software Requirements

- **Operating System**: Windows (latest versions) or Linux.
- **IDE**: Arduino IDE (versions 1.x or 2.x).

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

**Figure**: Pin Diagram of the River Cleaning Robot

### Key Pin Descriptions:
- **Arduino Uno Pins**:
  - Analog Pins: For environmental monitoring sensors.
  - Digital Pins: For motor control and LEDs.
  - Power Pins: Supplies power to connected components.
- **GPS Module**: Communicates with Arduino via TX/RX pins.
- **Motor Driver**: Controls motor movement (forward, backward, left, right).
- **External Sensors**: For additional data like water quality and temperature.

---

## Conclusion

The **River Cleaning Robot Using GPS** is an innovative solution addressing water pollution. With autonomous navigation, eco-friendly design, and efficient debris collection, this project provides a sustainable approach to water body cleaning. It significantly contributes to global sustainability goals, making aquatic environments safer for all.

---

## How to Use

1. Clone the repository:
   ```bash
   git clone <repository_url>
