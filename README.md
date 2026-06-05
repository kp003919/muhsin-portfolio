# Embedded Software Engineer | Real‑Time Systems | ESP32 | ARM Cortex‑M | FreeRTOS

This portfolio showcases a collection of embedded systems, real‑time firmware, and IoT engineering projects built using ESP32, STM32, and ARM Cortex‑M microcontrollers.

My work focuses on:

- Low‑level driver development  
- Interrupt‑driven design  
- FreeRTOS task scheduling  
- BLE communication  
- Real‑time control loops  
- IoT data pipelines  
- Hardware‑in‑the‑loop testing  
- Automated CI workflows  

---

## ⭐ Top Projects (Quick Links)
- **ESP32 PID Temperature Control System** — Real‑time control loop + FreeRTOS  
- **GPIO Interrupt Engine** — ISR pipeline + deterministic event handling  
- **BLE Beacon Scanner** — Wireless scanning + real‑time dashboard  
- **IoT Dashboard** — ReactJS + MQTT + multi‑device telemetry  
- **Hardware‑in‑the‑Loop CI** — Automated build/flash/test pipeline  

---

## 🔧 1. ESP32 PID Temperature Control System  
**Tech:** C/C++, ESP32, FreeRTOS, PWM  
**Category:** Embedded Systems · Control Theory · Real‑Time Firmware  

A real‑time PID controller implemented on the ESP32 with a simulated thermal model.  
Designed to demonstrate deterministic timing, stable control behaviour, and tunable PID parameters.

### Highlights
- Custom PID controller with tunable gains  
- Deterministic FreeRTOS control loop  
- Thermal simulation with noise/disturbance modelling  
- Serial plotting for real‑time tuning and analysis  

**Why it matters:** Shows real‑time control behaviour and FreeRTOS timing guarantees.  
**Skills demonstrated:** PID tuning, timing analysis, FreeRTOS scheduling.

**GitHub:**  
https://github.com/kp003919/PID_Demo.git

---

## 🔧 2. GPIO Interrupt Engine + FreeRTOS Event Pipeline  
**Tech:** ESP‑IDF, C, FreeRTOS  
**Category:** Firmware · Interrupts · Real‑Time Systems  

A low‑latency interrupt engine demonstrating clean ISR/application separation using IRAM‑safe ISRs and FreeRTOS task notifications.  
Implements a deterministic event pipeline suitable for real‑time embedded applications.

### Highlights
- IRAM‑safe interrupt service routines  
- Multi‑stage event pipeline  
- FreeRTOS semaphores, queues, and notifications  
- State‑machine execution triggered by ISR events  

**Why it matters:** Demonstrates interrupt‑driven design and deterministic event handling.  
**Skills demonstrated:** ISR design, concurrency, FreeRTOS primitives.

**GitHub:**  
https://github.com/kp003919/ISR_Demos.git

---

## 🔧 3. BLE Beacon Scanner & Real‑Time Monitoring System  
**Tech:** ESP32, C/C++, BLE GAP, Node‑RED, MQTT/WebSocket, ReactJS  
**Category:** Wireless Systems · Embedded Firmware · Real‑Time Data Pipelines  

An ESP32‑based BLE scanner that discovers nearby beacons, extracts metadata (MAC, RSSI, UUIDs), and streams results into a real‑time dashboard via MQTT/WebSockets.

### Highlights
- Active & passive BLE GAP scanning  
- Advertisement parsing (MAC, RSSI, UUIDs)  
- Node‑RED pipeline for filtering, timestamping, and routing  
- ReactJS dashboard with live updates and device diagnostics  

**Why it matters:** Shows wireless communication, data parsing, and real‑time telemetry.  
**Skills demonstrated:** BLE GAP, MQTT pipelines, dashboard integration.

**GitHub:**  
- Server: https://github.com/kp003919/ESP32_GATT_SERVER_BLE.git  
- Client: https://github.com/kp003919/GATT_Client_BLE.git  
- Demo: https://github.com/kp003919/BLE_Server_Client-Demo.git

---

## 🔧 4. Real‑Time IoT Dashboard (ReactJS + ESP32 + Node‑RED)  
**Tech:** ReactJS, TypeScript, Node‑RED, MQTT, WebSockets, ESP32  
**Category:** IoT Systems · Frontend Engineering · Cloud Integration  

A multi‑page real‑time dashboard visualising telemetry from ESP32 devices.  
Includes DHT sensor monitoring, RTLS visualisation, BLE beacon inspection, and actuator control.

### Highlights
- Real‑time WebSocket/MQTT data streaming  
- Reusable React components and modular UI design  
- Multi‑page routing with dynamic device views  
- Embedded protocol tester (UART/I²C/SPI/Modbus)  

**Why it matters:** Demonstrates full IoT pipeline from device → cloud → UI.  
**Skills demonstrated:** MQTT/WebSockets, UI engineering, multi‑device telemetry.

**GitHub:**  
https://github.com/kp003919/ReactJS_Dashboard.git

---

## 🔧 5. Hardware‑in‑the‑Loop CI Pipeline (GitHub Actions + GitLab CI)  
**Tech:** GitHub Actions, GitLab CI, ESP32, Python, Serial Automation  
**Category:** CI/CD · Embedded Testing · Automation  

A fully automated hardware‑in‑the‑loop (HIL) pipeline that builds firmware, flashes a real ESP32, executes functional tests, and reports results directly in CI.

### Highlights
- Automated build → flash → test → report workflow  
- Python‑based serial test harness  
- Functional tests for DHT, BLE, RTLS, UART/I²C/SPI  
- Reproducible builds and rapid feedback cycles  

**Why it matters:** Shows ability to automate embedded testing — rare and valuable.  
**Skills demonstrated:** CI/CD, Python automation, hardware testing.

**GitHub:**  
https://github.com/kp003919/ESP32_GITHUP_ACTION_CI.git

---

## 🧰 Technical Strengths Demonstrated  
- **Embedded:** C/C++, FreeRTOS, interrupts, drivers, DMA, GPIO, timers  
- **MCUs:** ESP32, STM32, SAMV70  
- **Debugging:** SWD, logic analysers, oscilloscopes  
- **Wireless:** BLE, Wi‑Fi  
- **IoT:** MQTT, Node‑RED, ThingsBoard  
- **Automation:** CI/CD, Python test harnesses  
- **Frontend:** ReactJS, real‑time UI components  

---

## 📌 About Me  
I build clean, reliable, and practical embedded systems — from low‑level firmware and real‑time control loops to IoT pipelines and automated testing.  
I enjoy working close to hardware, solving real engineering problems, and delivering polished, production‑ready solutions.

---

## 📫 Contact  
**LinkedIn:** https://www.linkedin.com/in/muhsin-atto  
**Email:** darenhaji@gmail.com
