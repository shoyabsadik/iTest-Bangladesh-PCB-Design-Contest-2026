# 📊 Problem 1 — SparkFun OpenLog Artemis Data Logger

🚀 A compact data-logging PCB inspired by the **SparkFun OpenLog Artemis architecture**, designed using **EasyEDA** for the iTest Bangladesh PCB Design Contest 2026 — Round 2.

The design integrates an Artemis module, a 9-DoF IMU, microSD storage, USB-to-serial communication, battery charging, and multiple power-management circuits for sensor data acquisition and logging.

## 👨‍💻 Author

**M. Shoyab Sadik**  
🎓 B.Sc. in Electrical and Electronic Engineering (EEE) — IUBAT  
🤖 Robotics & Embedded Systems Enthusiast | PCB Designer  
💼 Founder & CEO, Pico Robotics  

- 🌐 **Website:** [shoyabsadik.github.io](https://shoyabsadik.github.io)
- 💻 **GitHub:** [@shoyabsadik](https://github.com/shoyabsadik)
- 🔗 **LinkedIn:** [M. Shoyab Sadik](https://www.linkedin.com/in/shoyabsadik/)

## ✨ Features

- 🧠 **Artemis Module (U8):** Main processing module with local decoupling capacitors.
- 🧭 **ICM-20948 IMU (U13):** 9-axis motion sensing.
- 💾 **microSD Interface (J6):** Data storage with MOSFET power switching and level-shifting circuitry.
- 🔌 **USB Type-C (J5):** USB connectivity with CH340E USB-to-serial bridge.
- 🔋 **LiPo Battery Charging:** MCP73831 charger and JST battery connector.
- ⚡ **Power Management:** 3.3 V LDOs, a 1.8 V regulator, and a 3.0 V supervisor.
- 🔗 **Qwiic / I²C Interface (J11):** External sensor connectivity through SDA and SCL.
- 🛠️ **Debugging Interface:** Cortex SWD/JTAG header.
- ⏱️ **RTC Support:** 32.768 kHz crystal and ML414H backup battery.
- 🔍 **Testing & Debugging:** Test points for GND, QWIIC_3.3V, SCL, SDA, and TP1.

## 🧩 Key Component List

| Reference | Component | Package |
|---|---|---|
| U8 | Artemis Module | `ARTEMIS_FP` |
| U13 | ICM-20948 9-DoF IMU | QFN-24 |
| U10 | CH340E USB-to-Serial Bridge | MSOP-10 |
| U2 | MCP73831 LiPo Charger | SOT-23-5 |
| U3, U4 | AP2112K-3.3 V LDO | SOT-23-5 |
| U14 | 1.8 V LDO (SP6214 equivalent) | SOT-23-5 |
| Q1, Q3, Q7, Q9, Q10 | 2N7002 MOSFET | SOT-23 |
| Q2 | AO3401A MOSFET | SOT-23 |
| J5 | HX TYPE-C 16P-CT USB-C Connector | SMD |
| J11 | SM04B-SRSS-TB Qwiic Connector | SMD |
| J2 | S2B-PH-SM4-TB Battery Connector | SMD |

📌 *Refer to the schematic and component datasheets to verify pin assignments, footprints, and electrical compatibility.*

## 📐 PCB Layout & Design Considerations

- 🧠 **Processor Section:** The Artemis module and its decoupling capacitors are placed close together.
- 🧭 **IMU Placement:** The motion sensor is positioned away from USB and charger circuitry to help reduce interference.
- 💾 **Board-Edge Interfaces:** The microSD socket and USB-C connector are placed near the board edge for accessibility.
- ⚡ **Power Section:** Battery connector, charger, and voltage regulators are grouped together.
- 🔗 **I²C Routing:** The Qwiic connector is positioned along the board perimeter, with short SDA/SCL connections where practical.
- 🌍 **Ground Plane:** GND copper pours and stitching vias are used on both PCB layers.
- 🏷️ **Silkscreen:** Connector names, polarity indicators, and pin functions are labeled for easier assembly and debugging.

## 📁 Project Files

The project files are organized in the `Problem_1` directory.

| File | Description |
|---|---|
| 📐 `ShoyabSadik_IUBAT.json` | EasyEDA schematic and PCB source |
| 📄 `ShoyabSadik_IUBAT.pdf` | PCB layer documentation, one layer per page |
| 📝 `ShoyabSadik_IUBAT_report.docx` | Technical report with design documentation |

### 📂 Supporting Resources

- 🖼️ [Schematic & PCB Images](PCB_Pictures_1/)
- 📐 [EasyEDA PCB Source Files](PCB_Files_EasyEDA_1/)
- 📄 [Gerber Files](Gerber_1/)
- 📝 [Design Report](Report_1/)

*These links assume the folder names match the repository structure shown in GitHub.*

## 🖥️ PCB Preview

The following images can be placed in the `PCB_Pictures_1` directory.

| 📐 Schematic | 🟩 Top Layer |
|---|---|
| ![Schematic](PCB_Pictures_1/schematic.png) | ![Top Layer](PCB_Pictures_1/top.png) |

| 🔵 Bottom Layer | 🧊 3D PCB View |
|---|---|
| ![Bottom Layer](PCB_Pictures_1/bottom.png) | ![3D PCB](PCB_Pictures_1/3d.png) |

📌 *Ensure the image filenames and folder paths match the actual files uploaded to GitHub.*

## 🔧 How to Open the Design

1. 🌐 Open [EasyEDA](https://easyeda.com).
2. 📥 Open the appropriate EasyEDA editor version.
3. 🗂️ Navigate to **File → Open → EasyEDA Source…**.
4. 📐 Select `ShoyabSadik_IUBAT.json`.
5. 🔍 Inspect the schematic, footprints, PCB placement, and routing.
6. ✅ Run **Design → Check DRC** to review design-rule violations.

## ✅ Design Verification Checklist

- [ ] 📐 Schematic reviewed
- [ ] 🧩 Component footprints verified against datasheets
- [ ] 🟩 Component placement completed
- [ ] 🔀 PCB routing completed
- [ ] ⚡ Power and ground connections reviewed
- [ ] 🔍 DRC check completed
- [ ] 📄 Layer-wise PDF exported
- [ ] 📝 Technical report completed
- [ ] 🖼️ Schematic, PCB, and 3D preview images added

⚠️ Update the checklist according to the actual completion and verification status of your design.

## 🛠️ Tools & Technologies

`EasyEDA` `PCB Design` `Schematic Capture` `Artemis` `ICM-20948` `USB Type-C` `microSD` `I²C` `LiPo Charging` `Power Management` `DRC`

## 📄 License & Attribution

This repository is shared for educational, learning, and portfolio purposes. The original SparkFun OpenLog Artemis design, third-party components, library assets, trademarks, and related reference materials remain the property of their respective owners.

Please follow the original licensing and attribution requirements when reusing third-party designs or assets.

---

💡 **Think • Design • Build • Innovate**

*Designed with curiosity. Documented for learning. Driven by innovation.*

**M. Shoyab Sadik | IUBAT | PCB Design & Embedded Systems**
