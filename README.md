# SMART-HOME-USING-ESP82-SINRIC-CLOUD-INTREGRATED-WITH-GOOGLE-ASSISTANCE
Smart Home with Google Assistant &amp; Alexa using NodeMCU ESP8266  A voice-controlled smart home automation project using NodeMCU ESP8266, 4-channel relay module, and Sinric Pro. Control appliances via Google Assistant, Alexa, mobile app, or manual switches. Optional OLED display for real-time status.

-------------------------------------------------------------------------ASPHANTOM19-------------------------------------------------------------------------------

# 🏠 Smart Home with Google Assistant & Alexa using NodeMCU ESP8266 (Manual + Voice)

This IoT project demonstrates how to automate home appliances using **Google Assistant**, **Amazon Alexa**, and manual switches. Built with a **NodeMCU ESP8266**, it uses a **4-channel relay module** to control appliances and can include a **1.96" OLED** display for real-time status feedback.

---
![Screenshot 2025-06-11 180136](https://github.com/user-attachments/assets/6522d7d5-7378-4f8a-ba23-ac2f5d7f3823)


## ✨ Features

- ✅ Voice Control using **Google Assistant** & **Amazon Alexa**
- 📱 App-based control using **Sinric Pro**
- 🔘 Manual control with physical push-button switches
- 🌐 Remote access via Wi-Fi
- 📺 Optional 1.96" OLED display for real-time status
- 🔁 Real-time sync between app and device state

---

## 🧰 Components Required

| Component                      | Quantity |
|-------------------------------|----------|
| NodeMCU ESP8266                | 1        |
| **4-Channel 5V Relay Module**  | 1        |
| Manual Push Button Switches    | 4        |
| 1.96" OLED Display (Optional)  | 1        |
| Jumper Wires                   | Several  |
| Breadboard / PCB               | 1        |
| Power Supply (5V, >500mA)      | 1        |
| Smart Speaker (Alexa/Google)   | Optional |

---

## ⚡ Relay Wiring with NodeMCU

| Relay Channel | NodeMCU GPIO Pin | Appliance Example       |
|---------------|------------------|--------------------------|
| IN1           | D1 (GPIO5)       | Light 1                  |
| IN2           | D2 (GPIO4)       | Fan                      |
| IN3           | D5 (GPIO14)      | Plug Socket              |
| IN4           | D6 (GPIO12)      | Light 2 / Other device   |

> ⚠️ Relay inputs are **active LOW**: setting GPIO LOW will turn the appliance **ON**.

> 🔌 Ensure common **GND** between NodeMCU and relay power if using external 5V.

---

## 🖼️ Circuit Diagram

![NodeMCU-control-4-relays-circuit-02](https://github.com/user-attachments/assets/4a365451-bacc-4e27-a155-8cb0d2933d82)

*Includes NodeMCU, 4-Channel Relay, Push Buttons, and optional OLED display.*

---

## 📲 Platform Setup (Sinric Pro)

1. Create an account at [https://sinric.pro](https://sinric.pro)
2. Add a new device (type: Switch or Light)
3. Note your **Device ID** and **API Key**
4. Link Sinric Pro to Google Home or Alexa using their respective apps
5. In the Arduino code:
    - Add your **Wi-Fi credentials**
    - Paste your **API key** and **Device IDs**

---

## 🛠️ Arduino IDE Setup

### 🔧 Libraries Required:

Install these from Library Manager:
- `ESP8266WiFi`
- `WebSocketsClient`
- `ArduinoJson`
- `SinricPro`
- `Adafruit_GFX` (if using OLED)
- `Adafruit_SSD1306` (if using OLED)

### 🔌 Board Configuration:

- Board: **NodeMCU 1.0 (ESP-12E Module)**
- Flash Size: **4MB (FS:2MB OTA:~1019KB)**
- Upload Speed: **115200**

---

## 💡 OLED Display (Optional)

- Connect the 1.96" OLED display via I2C:
    - SDA → D2 (GPIO4)
    - SCL → D1 (GPIO5)
- Displays real-time appliance status or custom messages.

---

## 📁 Project Folder Structure

