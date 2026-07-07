# IoT Assignment 3

Submission for IoT Assignment 3, covering REST APIs, protocol theory, and applied IoT design projects using ESP32/ESP8266.

## Repository Structure

```
/
├── Q35_Weather_API.md
├── Q36_MQTT_vs_HTTP.md
├── Q37_WiFi_Security.md
├── Q38_LoRa_LPWAN.md
├── Q39_IoT_Gateway.md
├── Q40_MQTT_QoS.md
├── Q41_Air_Quality_Monitor.md
├── Q42_Plant_Watering.md
├── Q43_Smart_Door_Lock.md
├── Q44_PIR_Security.md
├── Q45_Greenhouse.md
├── Q46_Flood_Detection.md
├── Q47_Health_Monitor.md
├── /final_project/smart_city_proposal.md   (Q48)
├── Q49_Security_Analysis.md
├── Q50_Reflection.md
└── config.h   (gitignored, not included in repo)
```

## Module Overview

**Module 3 — REST APIs (Q35)**
ESP32 fetches live weather data from OpenWeatherMap and compares it against a local DHT11 reading.

**Module 4 — Protocol Theory (Q36–Q40)**
MQTT vs HTTP, Wi-Fi security practices, LoRa/LPWAN, IoT gateway architecture, and MQTT QoS levels.

**Module 5 — Advanced IoT Projects (Q41–Q50)**
Ten open-ended design challenges spanning smart home, security/access control, agriculture, and healthcare, plus a smart city design proposal, a security vulnerability analysis, and a reflection.

| # | Project | Board | Key Components |
|---|---------|-------|-----------------|
| Q41 | Smart Home Air Quality Monitor | ESP32 | MQ-2, DHT11, RGB LED, buzzer, HC-05 |
| Q42 | Automated Plant Watering System | ESP8266 | Soil moisture sensor, LDR, relay, LCD |
| Q43 | Smart Door Lock with OTP | ESP32 | 4x4 keypad, LCD, HC-05, servo |
| Q44 | PIR-Based Security Camera Trigger | ESP32 | PIR, potentiometer, LEDs, buzzer, Telegram bot |
| Q45 | Smart Greenhouse Controller | ESP32 | DHT11, LDR, 3x relay, LCD, MQTT |
| Q46 | River Water Level Alert | ESP32 | HC-SR04, LEDs, buzzer, web dashboard (Chart.js) |
| Q47 | Heart Rate & SpO2 Monitor | ESP32 | MAX30102 (or LDR simulation) |
| Q48 | Smart City Proposal — Jammu | — | Street lighting, air quality, waste bins |
| Q49 | Security Vulnerability Analysis | ESP8266 | MQTT/Wi-Fi security review |
| Q50 | Reflection & Learning Portfolio | — | Personal write-up |

## Hardware & Tools Used

- **Microcontrollers:** ESP32, ESP8266 (NodeMCU)
- **Sensors:** DHT11, MQ-2, MQ-135, HC-SR04, PIR, LDR, soil moisture sensor, MAX30102
- **Actuators/Outputs:** Servo motor, relays, RGB LEDs, buzzer, 16x2 LCD (I2C)
- **Connectivity:** Wi-Fi, HC-05 Bluetooth, MQTT (HiveMQ), Telegram Bot API
- **Simulation:** Wokwi
- **Cloud/Logging:** Google Sheets (via Apps Script), Firebase, AWS IoT / Azure IoT (proposal-level)

## Setup Notes

- Each `.ino` project expects a companion `config.h` file containing Wi-Fi credentials and any API keys/tokens. This file is **not committed** — see `.gitignore`.
- Circuit/wiring tables are included at the top of each project file.
- Where relevant, Serial Monitor CSV log formats and expected output samples are documented alongside the code.
- Simulations were built and tested in Wokwi before physical assembly where applicable.

## Security Practices Followed

Per the findings in Q49, all working code in this repo avoids hardcoded credentials (moved to gitignored `config.h`), uses authenticated/encrypted MQTT where cloud connectivity is involved, and avoids executing unvalidated remote commands.

## Author's Note

This repository represents applied coursework in sensor interfacing, wireless protocol selection, and system reliability design for embedded IoT systems, with a personal focus on real-world applications relevant to J&K (agriculture, disaster management, and urban infrastructure). See Q50 for the full reflection and a proposed next project (Tawi River water quality monitoring network).
