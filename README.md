# River Cleaning Robot Using GPS  

## Introduction  

The increasing pollution of water bodies threatens aquatic life and human health. Manual cleaning of rivers and lakes is **time-consuming, expensive, and sometimes dangerous**. This project proposes a **River Cleaning Robot using GPS** that efficiently removes floating and submerged debris from water bodies. Equipped with **sensors and GPS technology**, the robot navigates autonomously to locate and clean targeted areas. This innovative approach ensures **cost-effective and efficient** water cleaning while enhancing the safety of personnel.  

---

## Objectives  

- Collect non-living garbage from water bodies using a robot.  
- Provide cost-effective solutions for surface cleaning and garbage collection.  
- Improve aquatic waste management efficiency to align with **Smart City** and **Clean India Mission** goals.  

---

## Problem Statement  

- **Water pollution** poses a serious threat to human and aquatic life.  
- **Manual cleaning** is inefficient, costly, and hazardous.  
- There is a need for an **autonomous and eco-friendly** river-cleaning robot utilizing GPS.  

---

## Hardware Requirements  

- **Arduino Uno (ATMEGA328P)** – Microcontroller board based on ATmega328P.  
- **APM 2.8 Flight Controller + NEO GPS M8N (Ardupilot Mega) Module** – Includes a **GPS receiver** (for location tracking) and a **compass/magnetometer** (for orientation).  
- **GPS Module (Ublox NEO-M8N)** – Provides accurate location and time information.  
- **Compass Module (HMC5883L)** – Measures the Earth's magnetic field for direction sensing.  
- **Motor Driver (L293D)** – Controls the speed and direction of motors.  
- **DC Motors** – Converts electrical energy into mechanical motion for movement.  
- **3800mAh [18650] Li-Ion Rechargeable Battery** – Power supply for the entire system.  
- **Bluetooth Module (HC-05)** – Enables communication between the robot and a mobile app via Bluetooth.  

---

## Software Requirements  

- **Operating System** – Windows (latest versions) or Linux.  
- **IDE** – Arduino IDE (versions 1.x or 2.x) for programming and compiling the code.  
- **Serial Bluetooth Terminal App** – Used to send commands to the robot via Bluetooth.  

---

## Block Diagram  

![Block Diagram](https://github.com/Aishwaryan172/River-Cleaning-Robot-Using-GPS/blob/main/Block%20Diagram%20of%20the%20River%20Cleaning%20Robot.png)  

**Figure**: Block Diagram of the River Cleaning Robot  

---

## Methodology  

1. The user enters **GPS waypoints** defining the cleaning area.  
2. The **GPS module** determines the robot's current position.  
3. The **compass module** identifies the heading direction.  
4. The robot calculates the **distance and adjusts direction** to reach the waypoint.  
5. After completing one waypoint, the robot moves to the next, ensuring **comprehensive cleaning** of the water body.  

---

## Architecture  

![Architecture](https://github.com/Aishwaryan172/River-Cleaning-Robot-Using-GPS/blob/main/Architecture%20of%20the%20River%20Cleaning%20Robot.png)  

**Figure**: Architecture of the River Cleaning Robot  

---

## Pin Diagram & Circuit Connections  

![Pin Diagram](https://github.com/Aishwaryan172/River-Cleaning-Robot-Using-GPS/blob/main/Pin%20Diagram%20of%20the%20River%20Cleaning%20Robot.png)  

**Figure**: Pin Diagram of the River Cleaning Robot  

### 1. APM Module (GPS & Compass) → Arduino Uno  
- **VCC & GND** → Power connections to the Arduino.  
- **SCL & SDA** → Connected to Arduino’s I2C pins (**A5 & A4**) for compass data.  
- **TX & RX** → Communicates GPS data with Arduino’s Serial Pins (**TX-RX**).  

### 2. Bluetooth Module (HC-05) → Arduino Uno  
- **VCC & GND** → Power supply from Arduino.  
- **TX (Bluetooth) → RX (Arduino)**  
- **RX (Bluetooth) → TX (Arduino)**  

> **Bluetooth allows users to control or monitor the robot via a mobile app or PC.**  

### 3. Motor Driver (L293D) → Arduino Uno  
- **VCC & GND** → Power connections from the power supply.  
- **IN1, IN2, IN3, IN4** → Connected to Arduino’s digital pins (for motor direction control).  
- **Motor Outputs** → Connected to the DC motors of the robot.  

### 4. Power Supply → All Components  
- **VCC & GND** from the battery/power source are distributed to **Arduino, APM, Bluetooth module, and motor driver**.  

### 5. Connecting Motors to Motor Driver  
- Connect **one DC motor** to **OUT1 & OUT2** of the motor driver.  
- Connect **another DC motor** to **OUT3 & OUT4** of the motor driver.  

### 6. Uploading Code to Arduino  
- After completing the circuit connections, compile and upload the program to **Arduino Uno** using **Arduino IDE**.  
- Once uploaded, the robot will operate based on GPS navigation and Bluetooth commands.  

---

## Connecting HC-05 to Serial Bluetooth Terminal App  

### 1. Pairing HC-05 with Your Mobile Phone  
1. Power on the robot and ensure the **HC-05 Bluetooth module** is connected properly.  
2. Turn on **Bluetooth** on your mobile device.  
3. Open **Bluetooth settings** and search for available devices.  
4. Select **HC-05** (or HC-06 if applicable).  
5. Enter the default pairing PIN:  
   - **1234** or **0000** (if not changed).  
6. Once paired, the HC-05 module’s **LED will blink slower**, indicating a successful connection.  

### 2. Using the Serial Bluetooth Terminal App  
After pairing the Bluetooth module, follow these steps to control the robot:  

1. **Download and Install the App**  
   - Install the **Serial Bluetooth Terminal** app from the **Google Play Store**.  
2. **Connect to HC-05**  
   - Open the app and go to **Devices** → Select **HC-05**.  
   - Tap **Connect**. If successful, you’ll see **"Connected"** in the app.  
3. **Send Commands to the Robot**  
   - The app allows you to send commands via the **Serial Monitor**.  
   - The Arduino code will read these commands and control the motors accordingly.  

---

## Conclusion  

This **River Cleaning Robot** is a smart solution for cleaning water bodies. It can navigate using **GPS and a compass** while also supporting **manual control via Bluetooth and a mobile app**. This makes it both an **autonomous** and **remote-controlled** system for efficient river cleaning.  

---

## Future Enhancements  
- Add **autonomous navigation** using GPS waypoints.  
- Integrate **obstacle detection** using ultrasonic sensors.  
- Use a **WiFi module (ESP8266/ESP32)** for long-range control.  



