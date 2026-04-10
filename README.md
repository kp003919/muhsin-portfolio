# Mini Project Portfolio – Muhsin Atto  
**Embedded Software Engineer | Real‑Time Systems | ESP32 | ARM Cortex‑M | FreeRTOS**

This portfolio showcases a collection of embedded systems, real‑time firmware, and IoT engineering projects I have built using ESP32, STM32, and ARM Cortex‑M microcontrollers. Each project demonstrates practical engineering skills including driver development, interrupt handling, FreeRTOS task design, BLE communication,
control systems, and hardware‑in‑the‑loop testing.

## 🔧 1. ESP32 PID Temperature Control System  
**Tech:** C/C++, ESP32, FreeRTOS, PWM  
**Category:** Embedded Systems · Control Theory · Real‑Time Firmware  

A real‑time PID controller implemented on the ESP32 with a simulated thermal model.  
Includes FreeRTOS timing, PWM output, disturbance simulation, and serial‑based tuning.

**Highlights**
- Custom PID implementation  
- Real‑time loop with deterministic timing  
- Thermal simulation with noise/disturbances  
- Serial plotting for tuning and analysis  

**GitHub:** 
      https://github.com/kp003919/PID_Demo.git

## 🔧 2. GPIO Interrupt Engine + FreeRTOS Event Pipeline  
**Tech:** ESP‑IDF, C, FreeRTOS  
**Category:** Firmware · Interrupts · Real‑Time Systems  

Low‑latency ISR pipeline using IRAM‑safe interrupts and FreeRTOS task notifications.  
Demonstrates clean ISR/application separation and deterministic state‑machine behaviour.

**Highlights**
- IRAM‑safe ISRs  
- Multi‑stage event pipeline  
- FreeRTOS semaphores & notifications  
- State machine driven by ISR events  

**Github:** 
     https://github.com/kp003919/ISR_Demos.git

## 🔧 3. BLE Beacon Scanner & Real‑Time Monitoring System  
**Tech:** ESP32, C/C++, BLE GAP, Node‑RED, MQTT/WebSocket, ReactJS  
**Category:** Wireless Systems · Embedded Firmware · Real‑Time Data Pipelines  

ESP32 BLE scanner that discovers beacons, extracts metadata (MAC, RSSI, UUIDs), and streams results into a real‑time dashboard.

**Highlights**
- BLE GAP scanning (active/passive)  
- Advertisement parsing (MAC, RSSI, UUIDs)  
- Node‑RED pipeline for filtering & timestamping  
- ReactJS dashboard with live updates  

**Github:**
    - Server: https://github.com/kp003919/ESP32_GATT_SERVER_BLE.git
    - Client: https://github.com/kp003919/GATT_Client_BLE.git
    - Demo: https://github.com/kp003919/BLE_Server_Client-Demo.git

## 🔧 4. Real‑Time IoT Dashboard (ReactJS + ESP32 + Node‑RED)  
**Tech:** ReactJS, TypeScript, Node‑RED, MQTT, WebSockets, ESP32  
**Category:** IoT Systems · Frontend Engineering · Cloud Integration  

A multi‑page real‑time dashboard visualising live telemetry from ESP32 devices.  
Includes DHT sensor page, RTLS view, BLE beacon inspector, and actuator control panel.

**Highlights**
- Real‑time WebSocket/MQTT updates  
- Reusable React components  
- Multi‑page routing  
- Embedded protocol tester (UART/I²C/SPI/Modbus)  

**Github:** 
    https://github.com/kp003919/ReactJS_Dashboard.git

## 🔧 5. Hardware‑in‑the‑Loop CI Pipeline (GitHub Actions + GitLab CI)  
**Tech:** GitHub Actions, GitLab CI, ESP32, Python, Serial Automation  
**Category:** CI/CD · Embedded Testing · Automation  

A fully automated CI pipeline that builds firmware, flashes a real ESP32, runs hardware‑in‑the‑loop tests, and reports results directly in CI.

**Highlights**
- Automated build → flash → test → report  
- Python serial test harness  
- Functional tests for DHT, BLE, RTLS, UART/I²C/SPI  
- Reproducible builds and fast feedback  

**Github:**
   https://github.com/kp003919/ESP32_GITHUP_ACTION_CI.git     

## 🧰 Technical Strengths Demonstrated  
- **Embedded:** C/C++, FreeRTOS, interrupts, drivers, DMA, GPIO, timers  
- **MCUs:** ESP32, STM32, SAMV70  
- **Debugging:** SWD, logic analysers, oscilloscopes  
- **Wireless:** BLE, Wi‑Fi  
- **IoT:** MQTT, Node‑RED, ThingsBoard  
- **Automation:** CI/CD, Python test harnesses  
- **Frontend:** ReactJS, real‑time UI components

## 📌 About Me  
I build clean, reliable, and practical embedded systems — from low‑level firmware and real‑time control loops to IoT pipelines and automated testing.  
I enjoy working close to hardware, solving real engineering problems, and delivering polished solutions.

## 📫 Contact  
**LinkedIn:** https://www.linkedin.com/in/muhsin-atto  
**Email:** darenhaji@gmail.com  
