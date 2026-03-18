# 🔥 Forest Fire Detection System

An IoT-based wildfire detection and monitoring system designed to identify early signs of forest fires using distributed sensor nodes, cellular telemetry, and cloud-based alerting.

## 📌 Overview

The Forest Fire Detection System is a distributed embedded solution that monitors environmental conditions in fire-prone areas. Each node collects sensor data (smoke, temperature, wind, etc.) and transmits it to a cloud backend for analysis, visualization, and alerting.

The system is designed to:
- Detect early signs of wildfires
- Provide real-time monitoring through a web dashboard
- Send alerts to users via cellular networks
- Support multi-node deployments for improved detection accuracy

---

## 🧠 Key Features

- 🔍 **Multi-Sensor Fire Detection**
  - Ionization smoke detection (fast flame detection)
  - Photoelectric smoke detection (smoldering fires)
  - Temperature monitoring with threshold alerts

- 📡 **Cellular Telemetry**
  - Data transmission via GSM module
  - MQTT/HTTP communication to cloud services

- ☁️ **Cloud Integration**
  - AWS IoT for device communication
  - DynamoDB for data storage
  - Lambda for event-driven processing
  - SNS for push notifications

- 🌐 **Web Dashboard**
  - Real-time sensor data visualization
  - Device status monitoring
  - Alert notifications

- 📷 **Event-Based Video Capture**
  - Camera activates when fire conditions are detected
  - Stores and uploads footage to the cloud

- 🌬️ **Environmental Monitoring**
  - Wind speed and direction tracking
  - Humidity sensing

- 🔋 **Solar Powered**
  - автономous operation using solar panel + Li-Po battery
  - Designed for remote deployment

---

## 🏗️ System Architecture

```

[ Sensors ]
↓
[ Microcontroller (Arduino MKRGSM 1400) ]
↓
[ GSM Network ]
↓
[ AWS IoT Core ]
↓
[ Lambda Functions ]
↓
[ DynamoDB + S3 ]
↓
[ Web Dashboard / Notifications ]

```

---

## 🔧 Hardware Components

- Arduino MKRGSM 1400 (microcontroller + GSM)
- Ionization smoke sensor
- Photoelectric smoke sensor
- NEO-6M GPS module
- ArduCam camera module
- Temperature & humidity sensors
- Anemometer + wind vane
- Solar panel (6V, 9W)
- Li-Po battery (2000 mAh)
- Cooling fan + enclosure (IP67 target)

---

## 💻 Software Stack

- **Embedded**
  - Arduino IDE (C/C++)

- **Cloud**
  - AWS IoT Core
  - AWS Lambda
  - AWS DynamoDB
  - AWS S3
  - AWS SNS

- **Frontend**
  - Next.js (React + TypeScript)

---

## 🚀 How It Works

1. Sensors continuously monitor environmental conditions.
2. If abnormal conditions are detected (e.g., smoke or high temperature):
   - Device enters alert state
   - Data is sent to AWS via GSM
3. Cloud services process incoming data:
   - Store readings in database
   - Trigger alerts via SNS
4. Users view:
   - Real-time data on dashboard
   - Notifications on mobile devices
5. Camera activates and uploads footage when fire is detected.

---

## 📊 Functional Highlights

- Real-time sensor data streaming
- Threshold-based alert system
- Multi-node deployment for improved coverage
- Remote diagnostics and sensor validation
- Event-driven cloud architecture

---

## ⚠️ Limitations & Future Improvements

### Current Limitations
- Cellular triangulation accuracy is limited
- Power consumption is high under continuous operation
- Video streaming depends on network availability

### Planned Improvements
- Implement low-power sleep cycles
- Enhance detection using sensor fusion logic
- Replace continuous streaming with event-based snapshots
- Improve location accuracy using multi-node correlation
- Add CO / air quality sensors
- Explore edge-based machine learning for fire detection

---

## 👥 Team

**Quad Core Crew**
- Matthew Wilson (Team Lead)
- Edwin Hernandez (Software Lead)
- Luis Guevara (Hardware Lead)
- Lluviana Vasquez (Reporter)

---

## 📅 Timeline

- Project Duration: Aug 2022 – Apr 2023
- Built as part of a senior engineering project

---

## 📜 License

This project is for educational and portfolio purposes.

---

## 💡 Why This Project Matters

Wildfires cause massive environmental and economic damage every year. Early detection is critical.

This system demonstrates how IoT, cloud computing, and embedded systems can work together to create scalable, real-world solutions for environmental monitoring.

---

## 📬 Contact

For questions or collaboration:
- teamquadcorecrew@groups.com
