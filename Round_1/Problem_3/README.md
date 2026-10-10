# 📡 Round 1, Problem 3 – ExpressLRS ESP32 RF Development PCB

## 📌 Project Overview

An ESP32-based RF development and control board designed for radio module interfacing, SPI communication, and embedded wireless experimentation. The PCB features an ESP32-PICO-KIT socket, dedicated radio module headers, control connectors, and a programming interface.

The design emphasizes **RF-aware component placement, signal integrity, effective grounding, and accessible connectivity** for radio-frequency development and embedded control applications.

## ⚙️ Features & Components

### 🧠 Microcontroller Interface
- **ESP32-PICO-KIT Socket** — Custom PCB footprint for mounting the ESP32 development module.
- **U10, U11** — 20-pin, 2.54 mm-pitch headers for microcontroller connections.
- **Programming Interface (H1)** — 1×5 header for programming and debugging connections.

### 📡 Radio Module Interfaces
- **U3–U6** — 10-pin headers for radio module connections.
- **U1, U2** — 10-pin control headers for external peripherals or control interfaces.
- **U7, U8, U9** — 3-pin connectors for auxiliary signals or external connections.
- **R1, R2 (150 Ω, 0402)** — Series resistors on the radio MISO signal paths, as specified in the design.

### 🔌 SPI Communication
Dedicated net labels organize the communication interfaces between the ESP32 and external radio modules:

- `radio_sck` — SPI clock.
- `radio_mosi` — Master Out, Slave In.
- `radio_miso` — Master In, Slave Out.
- **Test Points** — Added for convenient signal probing and debugging.

## 📐 PCB Layout & RF Design Considerations

### 📡 RF-Aware Placement
- Keep RF-related components and SPI signal paths compact to reduce unnecessary routing length.
- Place radio module connectors close to their associated circuitry where practical.
- Avoid routing noisy power lines and high-current traces through sensitive RF areas.
- Keep antenna-sensitive areas clear of unnecessary copper and routing, following the module's antenna keep-out requirements.

### 🌐 Grounding & Signal Integrity
- Use continuous ground copper pours on both PCB layers where appropriate.
- Add ground stitching vias to improve ground continuity and provide low-impedance return paths.
- Avoid splitting the reference ground beneath critical signal paths.
- Verify SPI routing, return paths, and trace clearances during layout review.

### 🔋 Power Distribution
- Keep power distribution organized and separate high-current paths from sensitive RF sections.
- Place suitable decoupling capacitors close to the relevant power pins.
- Verify connector pin assignments and power requirements against the selected module datasheets.

### 🏷️ Accessibility & Silkscreen
- Position the programming header and perimeter connectors for easy access.
- Keep connector labels and pin-1 indicators clearly visible.
- Provide accessible test points for essential SPI and control signals.
- Place the ESP32-PICO-KIT antenna end near the board edge, maintaining the required antenna clearance and copper keep-out.

## 📂 Project Files

| 📄 File | 📝 Description |
|---|---|
| `ShoyabSadik_IUBAT.json` | EasyEDA schematic and PCB design data. |
| `ShoyabSadik_IUBAT.pdf` | PCB documentation, with individual layers presented on separate pages. |
| `ShoyabSadik_IUBAT_report.docx` | Detailed design report. |

## 🖼️ Design Preview

Explore the schematic, copper layers, and 3D board representation below.

| 🔌 Schematic | 🔝 Top Layer |
|---|---|
| ![Schematic](images/schematic.png) | ![Top Layer](images/top.png) |

| 🔽 Bottom Layer | 🧊 3D PCB View |
|---|---|
| ![Bottom Layer](images/bottom.png) | ![3D PCB View](images/3d.png) |

## ✅ Design Verification Checklist

- [ ] Verify the ESP32-PICO-KIT socket footprint, orientation, and pin mapping.
- [ ] Confirm all radio and control header pin assignments.
- [ ] Check SPI connections and verify the MISO series resistor placement.
- [ ] Validate power input requirements and decoupling arrangements.
- [ ] Inspect the ground pours and stitching vias on both layers.
- [ ] Verify the antenna keep-out against the module manufacturer's recommendations.
- [ ] Check test points, silkscreen labels, and connector accessibility.
- [ ] Run EasyEDA Design Rule Check (DRC).
- [ ] Review Gerber and drill files before fabrication.

## ⚠️ Important Notes

- This board is an ESP32-based RF development design inspired by ExpressLRS-related hardware concepts; it should not be assumed to be an official or electrically identical ExpressLRS reference design.
- RF performance depends on the actual module, antenna arrangement, PCB stack-up, grounding, and surrounding components.
- The 150 Ω MISO series resistors should be checked against the original circuit requirements and the selected radio module's electrical specifications.
- Final functionality and RF performance require appropriate design verification and hardware testing.

---

## 👨‍💻 Author

**M. Shoyab Sadik**  
B.Sc. in Electrical and Electronic Engineering (EEE), IUBAT

- 🌐 Website: [shoyabsadik.github.io](https://shoyabsadik.github.io/)
- 💼 LinkedIn: [shoyabsadik](https://www.linkedin.com/in/shoyabsadik/)

**🚀 From Code to Creation — Learn • Build • Innovate.**