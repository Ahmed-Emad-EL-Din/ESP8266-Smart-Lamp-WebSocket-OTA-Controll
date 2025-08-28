

#  ESP8266 Smart Home Lamp Control (WebSocket + OTA)

## Project Overview

This project demonstrates how to control a **real 220V lamp** as part of a **Smart Home system** using the **ESP8266 microcontroller**.
It combines **IoT**, **Electrical Engineering**, and **Web Development** to build a reliable and scalable home automation solution.

With this project, you can control your lamp directly from a **smartphone or PC browser** using a simple and responsive web interface — no mobile app required.

---

## Features

* 🌐 **Wi-Fi Control** – Access the ESP8266 from any device on the same network.
* 🔄 **WebSocket Communication** – Provides **real-time**, two-way updates between the ESP8266 and the web interface (instant ON/OFF switching without page refresh).
* 📲 **Mobile-Friendly Interface** – Built with **HTML, CSS, and JavaScript**, designed for phones and tablets.
* ⚡ **ElegantOTA** – Update ESP8266 firmware **over-the-air (OTA)** without reconnecting USB cables.
* 💡 **Smart Home Ready** – Control real 220V devices (lamp, fan, etc.) with safe relay integration.
* 👨‍💻 **C++ Firmware** – Written in Arduino framework for ESP8266.

---

## Technologies Used

* **ESP8266 Wi-Fi Module** (NodeMCU)
* **C++ / Arduino IDE Framework**
* **HTML + CSS + JavaScript** (for the web interface)
* **AsyncWebServer & WebSocket libraries**
* **AsyncElegantOTA** for OTA updates

---

## 🚀 How It Works

1. ESP8266 connects to your **Wi-Fi network** using SSID and password.
2. It starts a **WebSocket server** at `/ws` and a **web server** on port 80.
3. You open the ESP8266’s IP address in your **smartphone browser**.
4. A **web dashboard** appears with a toggle button to switch the lamp ON/OFF.
5. The **WebSocket protocol** ensures changes are updated instantly.
6. The **ElegantOTA** system allows firmware upgrades directly through the browser.

---

## User Interface

* Displays current lamp state (**ON/OFF**) in real-time.
* **Toggle button** to control the lamp.
* Clean and mobile-friendly design.

---

## Code Explanation 

* `#include <ESP8266WiFi.h>` → Connects ESP8266 to Wi-Fi.
* `#include <ESPAsyncWebServer.h>` → Creates a web server.
* `#include <ESPAsyncTCP.h>` → Enables asynchronous TCP connections.
* `#include <AsyncElegantOTA.h>` → Enables OTA updates from the browser.
* **`AsyncWebSocket ws("/ws");`** → Creates a WebSocket endpoint at `/ws`.
* **`ledState` & `ledPin`** → Track and control lamp ON/OFF state.
* **HTML/JS Code** → Renders a webpage, connects to WebSocket, and sends `"toggle"` when the button is pressed.
* **`notifyClients()`** → Sends updated state (ON/OFF) to all connected clients.
* **`onEvent()`** → Handles WebSocket events (connect, disconnect, data received).
* **`ElegantOTA.begin(&server)`** → Enables OTA updates.
* **`loop()`** → Keeps updating lamp state and WebSocket connections.

---

## ⚡ Key Benefits

✅ Real-time control via **WebSocket**
✅ Remote firmware upgrades via **OTA**
✅ Practical for **IoT & Electrical Engineering** projects
✅ Can be expanded for full **Smart Home systems**

---

## 🎥 Project Demo Video
[![Watch the video](https://img.youtube.com/vi/https://youtu.be/jlRyVyKFLNQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=https://youtu.be/jlRyVyKFLNQ)


---

## 🔗 Installation & Setup

1. Install **Arduino IDE** with **ESP8266 board support**.
2. Install required libraries:

   * ESPAsyncTCP
   * ESPAsyncWebServer
   * AsyncElegantOTA
3. Flash the code to your ESP8266.
4. Connect your relay + lamp to GPIO2 (modify if needed).
5. Open Serial Monitor to find the ESP8266 IP.
6. Enter IP in browser → Control lamp instantly.

---

## 👨‍💻 Author

**Ahmed Emad**
*Electrical Engineer* ⚡ | *IoT & Smart Home Enthusiast* 🌐
