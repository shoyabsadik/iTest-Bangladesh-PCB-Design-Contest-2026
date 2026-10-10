# 🟣 Round 1, Problem 2 – Circuit Playground Express Inspired Controller

## 📌 Project Overview

A compact, interactive embedded controller inspired by the **Circuit Playground Express**, integrating a microcontroller, USB connectivity, motion and environmental sensors, addressable RGB LEDs, audio components, infrared communication, and user input controls.

The design focuses on a visually balanced PCB layout, accessible peripherals, and efficient component placement for educational, prototyping, and embedded systems applications.

## ⚙️ Features & Components

### 🧠 Microcontroller & Memory
- **ATSAMD21G18 (U$5)** — 32-bit ARM Cortex-M0+ microcontroller.
- **GD25Q16C (U4)** — 2 MB SPI flash memory for external data storage.

### 🌡️ Sensors & Input
- **LIS3DH (IC4)** — 3-axis accelerometer for motion and orientation detection.
- **ALS-PT19 (U2)** — Ambient light sensor.
- **10K NTC Thermistor (THM1)** — Temperature sensing.
- **SW1 / SW2** — User input buttons.
- **KMR2 Reset Switch** — Microcontroller reset control.
- **EG1390 Slide Switch** — Power or mode selection.

### 💡 RGB LED System
- **10 × WS2812B NeoPixels** — Individually addressable RGB LEDs arranged around the board.
- **L LED** — Status indication.
- **PWR LED** — Power status indication.

### 🎤 Audio System
- **SPH0645LM4H (IC1)** — Digital I²S MEMS microphone for audio input.
- **PAM8301 (IC2)** — Class-D audio amplifier.
- **SP1 (8 Ω)** — Speaker output.

### 📡 Infrared Communication
- **VSOP383 (U1)** — Infrared receiver.
- **IR LED (D5)** — Infrared signal transmission.
- **Photodiode (D3)** — Optical signal detection.
- **MMBT2222 (Q1)** — NPN transistor for switching and driving the IR LED.

### 🔋 Power Management
- **AP2112K-3.3 (U3)** — 3.3 V low-dropout voltage regulator.
- **MBR120 (D1, D2)** — Schottky diodes for power-path or protection functions, according to the schematic.
- **F1 (500 mA Resettable Fuse)** — Overcurrent protection.
- **CN1 (Micro-B USB)** — USB connectivity and potential power input.
- **BATT (JST-PH)** — Battery connection.

## 📐 PCB Layout & Design Considerations

- 💡 **Balanced LED Arrangement:** Place the 10 NeoPixels evenly around the PCB perimeter for a visually consistent layout.
- 🔌 **USB & Programming Access:** Position the USB connector and programming-related connections near an accessible board edge.
- ⚡ **Power Integrity:** Place decoupling capacitors close to the supply pins of each IC and keep power traces appropriate for their expected current.
- 🎤 **Audio Isolation:** Keep the microphone away from the speaker, amplifier, and noisy power circuitry where practical.
- 🌞 **Sensor Placement:** Position the ambient light sensor where surrounding light can reach it without significant obstruction from other components.
- 📡 **IR Accessibility:** Ensure the IR receiver, transmitter, and photodiode have suitable optical exposure.
- 🏷️ **Clear Silkscreen:** Label buttons, switches, connectors, indicators, and important test points.
- 🛠️ **Routing & Clearance:** Verify trace widths, ground return paths, copper clearances, and design-rule checks before fabrication.

## 📂 Project Files

| 📄 File | 📝 Description |
|---|---|
| `ShoyabSadik_IUBAT.json` | EasyEDA schematic and PCB design data. |
| `ShoyabSadik_IUBAT.pdf` | PCB design documentation, with individual layers presented on separate pages. |
| `ShoyabSadik_IUBAT_report.docx` | Detailed design report. |

## 🖼️ Design Preview

The following images provide an overview of the schematic, PCB routing, board appearance, and 3D model.

| 🔌 Schematic | 🔝 Top Layer |
|---|---|
| ![Schematic](images/schematic.png) | ![Top Layer](images/top.png) |

| 🔽 Bottom Layer | 🧊 3D PCB View |
|---|---|
| ![Bottom Layer](images/bottom.png) | ![3D PCB View](images/3d.png) |

## ✅ Design Verification Checklist

- [ ] Verify all schematic connections and component pin assignments.
- [ ] Confirm component footprints against datasheets.
- [ ] Check power input, voltage regulation, and protection circuitry.
- [ ] Verify the NeoPixel data chain and power distribution.
- [ ] Check USB connections and programming interfaces.
- [ ] Review audio, sensor, and infrared signal routing.
- [ ] Run the EasyEDA Design Rule Check (DRC).
- [ ] Review Gerber and drill outputs before manufacturing.

## ⚠️ Important Note

This project is inspired by the Circuit Playground Express concept and is not necessarily electrically or mechanically identical to the original Adafruit board. Component functionality, pin assignments, and circuit behavior should be verified against the schematic, datasheets, and design requirements.

---

### 👨‍💻 Author

**M. Shoyab Sadik**  
B.Sc. in Electrical and Electronic Engineering (EEE), IUBAT

- 🌐 Website: [shoyabsadik.github.io](https://shoyabsadik.github.io/)
- 💼 LinkedIn: [shoyabsadik](https://www.linkedin.com/in/shoyabsadik/)

**🚀 From Code to Creation — Learn • Build • Innovate.**