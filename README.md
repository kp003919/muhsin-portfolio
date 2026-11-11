# 💻 Muhsin Atto — Embedded & Full-Stack Software Engineer

PhD-qualified engineer with **15+ years experience** spanning embedded firmware, real-time systems, and modern full-stack web development. I build reliable, maintainable systems — from low-level device drivers to cloud-connected React dashboards.

📍 Sheffield, UK | 📧 darenhaji@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/muhsin-atto) | 💻 [GitHub](https://github.com/kp003919)

---

## 🚀 Featured Projects

### 🔄 Full-Stack Data Manager — Dual-Backend System
**Tech:** C# / ASP.NET Core • Node.js / Express • MySQL • React • REST APIs  
**Category:** Full-Stack Web Development · Database Integration · Clean Architecture

A complete end-to-end system featuring **two interchangeable backends** sharing one MySQL database, with a component-based React frontend that can switch between them in real time — demonstrating API design, data consistency, and service abstraction.

| Repository | Description |
|---|---|
| **[ASP.net Core](https://github.com/kp003919/FullStackWbApp)** | ASP.NET Core — REST API with EF Core, Swagger, full CRUD & search |
| **[nodejs-api](https://github.com/kp003919/nodejs-api)** | Node.js / Express — identical API contract, direct SQL, matching responses |
| **[react-frontend](https://github.com/kp003919/react-frontend)** | React 18 — multi-page routing, backend switcher, form validation, data table |

**Highlights:**
- ✅ Identical routes & JSON format across both backends → frontend switches without code changes
- ✅ Shared MySQL → data consistency across service implementations
- ✅ Component-based architecture → reusable UI, clean separation of concerns
- ✅ Search, Create, Edit, Delete → complete data lifecycle
- ✅ CORS, error handling, user feedback → production-ready behaviour

---

### 🔧 ESP32 PID Temperature Control System
**Tech:** C/C++ • ESP32 • FreeRTOS • PWM  
**Category:** Embedded Systems · Control Theory · Real-Time Firmware

A real-time PID controller with simulated thermal model — demonstrating deterministic timing, stable control behaviour, and tunable parameters.

**Highlights:**
- Custom PID implementation (Proportional / Integral / Derivative)
- FreeRTOS task scheduling → guaranteed loop frequency
- Sine-wave disturbance simulation → visualises controller response
- Serial plotting → real-time tuning & analysis
- **GitHub:** [PID_Demo](https://github.com/kp003919/PID_Demo)

---

### ⚡ GPIO Interrupt Engine + FreeRTOS Event Pipeline
**Tech:** ESP-IDF • C • FreeRTOS  
**Category:** Firmware · Interrupts · Real-Time Systems

Low-latency interrupt-driven design demonstrating clean ISR/application separation using IRAM-safe ISRs and four distinct synchronization mechanisms running in parallel.

**Highlights:**
- ✅ Queue Demo — ISR → Queue → Task
- ✅ Semaphore Demo — ISR → Binary Semaphore → Task
- ✅ Task Notification Demo — ISR → Direct Notification → Task (fastest)
- ✅ State Machine Demo — ISR → Queue → FSM Task
- Independent GPIOs, no interference between demos
- **GitHub:** [ISR_Demos](https://github.com/kp003919/ISR_Demos)

---

### 📡 BLE GATT Server + Client
**Tech:** ESP32 • C/C++ • BLE GAP/GATT  
**Category:** Wireless Systems · Embedded Communication

Complete BLE implementation — separate server and client repos demonstrating custom services, notification streams, and bidirectional characteristics.

| Repository | Description |
|---|---|
| **[ESP32_GATT_SERVER_BLE](https://github.com/kp003919/ESP32_GATT_SERVER_BLE)** | GATT server — notify + read/write characteristics |
| **[GATT_Client_BLE](https://github.com/kp003919/GATT_Client_BLE)** | GATT client — scanning, connecting, receiving notifications |
| **[BLE_Server_Client-Demo](https://github.com/kp003919/BLE_Server_Client-Demo)** | Combined demo — matching UUIDs, periodic data exchange |

**Highlights:** Custom service/characteristic UUIDs → notify + read/write streams → stable persistent connection

---

### 📶 LTE Modem State Machine — Fault-Tolerant AT-Command Connectivity
**Tech:** C • ESP32 • LTE modem • AT commands • MQTT • State machines
**Category:** Embedded Systems · Communications · Fault Recovery · Unit Testing

A layered LTE connectivity stack that takes a modem from power-on to a live MQTT connection (SIM check → network attach → data session → TCP socket → MQTT connect and subscribe), and recovers automatically when any step fails.

**Highlights:**
- ✅ **One command in flight at a time** — AT replies carry no ID, so the state machine never sends a second command before the first finishes
- ✅ **Bounded retries and timeouts** — every command has its own retry counter (max 3) and timeout, also checked on a periodic tick so a silent modem is detected
- ✅ **Escalation to a modem reboot** — when retries run out, the modem is reset and the boot sequence restarts, so the device never loops forever
- ✅ **Unsolicited messages handled** — registration reports (`+CEREG`) are processed in both URC and query forms, including network lost and registration denied
- ✅ **Strict layering** — state machine → driver → hardware layer; the state machine never touches hardware directly
- ✅ **30 host-side tests** — a simulated modem with a fake clock covers success paths, `ERROR` / `+CME ERROR` replies, timeouts, retry exhaustion, locked SIM, and network loss, with no hardware needed

**How it recovers:**

| Failure | Response |
|---|---|
| Command returns an error or times out | Retry (up to 3 times), then reboot the modem |
| Modem silent at boot | Resend `AT` every 2 s (up to 15 times), then reboot |
| SIM not ready | Boot waits and asks again |
| Network lost (`+CEREG: 0`) | Re-attach |
| Registration denied (`+CEREG: 3`) | Counts as a failure towards a reboot |

**GitHub:** [lte_esp_Interface](https://github.com/kp003919/lte_esp_Interface)

-------------

### 📊 Real-Time IoT Dashboard (React + ESP32)
**Tech:** ReactJS • TypeScript • MQTT • WebSockets • Node-RED • ESP32  
**Category:** IoT Systems · Frontend Engineering · Cloud Integration

Multi-page dashboard visualising telemetry from remote devices — from raw sensor values to historical trends and actuator control.

**Highlights:**
- Real-time WebSocket/MQTT streaming → live updates
- Reusable components → responsive design
- Device overview + detailed views → multi-page routing
- **GitHub:** [ReactJS_Dashboard](https://github.com/kp003919/ReactJS_Dashboard)

---

# 🤖 ESP32 Hardware-in-the-Loop CI Pipeline

**Tech Stack:** GitHub Actions · GitLab CI · FreeRTOS · Python · ESP32 · PlatformIO · TLS/MQTT  
**Category:** Embedded Systems · Firmware · CI/CD · Hardware-in-the-Loop Testing

> From a simple superloop to a secure, fully-automated embedded system — **build → flash → test → report**, running on physical hardware, not just simulation.

---

## 📂 Project Structure — Two Distinct Branches

This repository shows the evolution of an embedded design, with two clearly separated paths:

| Branch | Architecture | Key Features |
|---|---|---|
| **`main`** | Superloop (single-threaded) | Minimal foundation · No RTOS · Basic sensors & comms · Simple, easy to debug |
| **`freertos-tasks`** | FreeRTOS Multi-Tasking | Secure TLS/MQTT · decoupled task design · full CI/CD automation · Hardware-in-the-Loop testing |

---

## 🌿 Branch: `main` — Superloop Foundation

The starting baseline: a clean, straightforward firmware with no external OS dependency.

- **Superloop / main-loop architecture** — predictable, fully deterministic execution
- Sensor support: DHT temperature & humidity
- Peripherals: UART, I²C, SPI
- WiFi & basic MQTT connectivity
- Build: PlatformIO configuration
- Purpose: **baseline comparison** — reference for reliability and performance improvements

---

## 🚀 Branch: `freertos-tasks` — FreeRTOS + Secure Comms + HIL CI

The advanced production-grade implementation — fully automated and security-hardened.

### FreeRTOS Task Architecture
- Decoupled dedicated tasks: sensor acquisition, MQTT/TLS transmission, BLE advertising, system monitoring
- Priority-driven scheduling
- Non-blocking design — no single component stalls the system
- Clean separation between data collection, processing, and transmission

### Secure Communications
- **TLS 1.2+** encrypted MQTT over WiFi
- Secure credential handling — credentials generated at CI runtime, never committed to repo
- Persistent MQTT sessions & automatic reconnection logic
- JSON-formatted telemetry payloads

### Hardware-in-the-Loop (HIL) Test Framework
- **Python serial automation harness** — controls and validates the physical ESP32 over USB
- Tests execute on **real hardware**, not just emulation
- Coverage:
  - ✅ System boot & health
  - ✅ DHT sensor readings
  - ✅ WiFi connection stability
  - ✅ MQTT publish/receive under outage conditions
  - ✅ I²C / SPI bus diagnostics
  - ✅ BLE advertising
  - ✅ Reset & recovery behaviour
- **Quantified reliability gains** over 90‑second simulated broker outage:
  - Longest sensor gap: **6.99 s → 5.01 s**
  - Lost telemetry messages: **52 → 0**

### CI/CD Pipeline
- **Runners:** GitHub Actions self-hosted runner + GitLab CI / Jenkins configurations
- **Workflow:**
  1. Checkout code → inject secure credentials
  2. Build firmware via PlatformIO
  3. Flash directly to physical ESP32
  4. Run full HIL test suite
  5. Report pass/fail status
- Trigger: push, pull request, or manual dispatch
- Secrets managed via encrypted repository variables

---

## 🛠️ Problems Solved

| Challenge | Resolution |
|---|---|
| Self-hosted runner not picking up jobs | Corrected runner labels & dedicated hardware registration |
| Missing credentials at build time | On-the-fly header generation — no secrets committed |
| Windows serial encoding crashes | Output sanitisation & robust parsing |
| Board not ready after flashing | Tuned reset timing & port open delays |
| MQTT outage false failures | Matched actual board output, not idealised text |
| Intermittent BLE timeouts | Extended per-test timeouts to match real hardware latency |

---

## 📊 Current Status

| Item | Status |
|---|---|
| Firmware build | ✅ Stable — PlatformIO compiles cleanly |
| Automated flash | ✅ Operational — deploys to physical hardware |
| HIL test suite | ✅ 12/15 passing — remaining items being refined |
| CI/CD pipeline | ✅ Fully green — every push runs the pipeline |
| Reliability | ✅ Zero lost messages during broker outage testing |

---

## 🔗 Repository Links

- **Project Home:** [github.com/kp003919/ESP32_GITHUP_ACTION_CI](https://github.com/kp003919/ESP32_GITHUP_ACTION_CI)
- **`main` Branch:** Superloop baseline — simple, minimal, deterministic
- **`freertos-tasks` Branch:** FreeRTOS + TLS + HIL CI — production-grade automation

---

## 💡 Summary

> This project demonstrates the complete embedded engineering journey — from a simple polling loop through to a secure, multi-tasking RTOS design, fully validated by automated hardware testing. It applies software-development best practices to firmware: version control, repeatable builds, continuous integration, and regression testing — all running on real silicon.

---

## 🧰 Full Technical Profile

| Category | Skills & Technologies |
|---|---|
| **Languages** | C • C++ • C# • JavaScript / ES6+ • TypeScript • Python • SQL |
| **Embedded** | ESP32 • STM32 • ARM Cortex-M • FreeRTOS • ISR design • Drivers • DMA • PWM • UART/I²C/SPI |
| **Backend** | ASP.NET Core 8 • Entity Framework Core • Node.js • Express • REST APIs • MySQL |
| **Frontend** | React 18 • React Router • Hooks • Component Architecture • HTML5 • CSS3 |
| **Wireless/IoT** | BLE (GAP/GATT) • Wi-Fi • MQTT • WebSockets • Node-RED |
| **Tools & DevOps** | Git • GitHub Actions • GitLab CI • Visual Studio • VS Code • PlatformIO • npm • pytest |
| **Process** | Agile • Jira • Technical Documentation • Code Review • CI/CD |

---

## 🎓 Education

| Qualification | Institution | Year |
|---|---|---|
| PhD in Computer Science | University of Reading, UK | 2016 |
| MSc in Computer Science | Uppsala University, Sweden | 2009 |
| BSc in Computer Science | University of Zakho, Iraq | 2004 |

---

## 💡 About My Work

I build systems that are **clean, tested, and maintainable** — whether they run on a microcontroller or in a browser. I value:
- ✅ Clear separation between components
- ✅ Consistent naming & predictable interfaces
- ✅ Documentation that explains *why*, not just *what*
- ✅ Systems that are testable, debuggable, and extendable
- ✅ Continuous learning — from embedded fundamentals to modern web stacks

---

## 📫 Get In Touch

- **Email:** darenhaji@gmail.com
- **LinkedIn:** [linkedin.com/in/muhsin-atto](https://linkedin.com/in/muhsin-atto)
- **GitHub:** [github.com/kp003919](https://github.com/kp003919)

---

*Last updated: October 2026*
