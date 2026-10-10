# ⚡ Problem 2 — Infineon REF-FRIDGE-C101T-6ED Motor/Inverter Controller

🚀 A three-phase motor inverter and control PCB based on the **Infineon REF-FRIDGE-C101T-6ED reference architecture**, designed using **EasyEDA** for the iTest Bangladesh PCB Design Contest 2026 — Round 2.

The design focuses on power conversion, three-phase motor control, gate driving, current sensing, and PCB layout considerations for BLDC/PMSM motor applications.

## 👨‍💻 Author

**M. Shoyab Sadik**  
🎓 B.Sc. in Electrical and Electronic Engineering (EEE) — IUBAT  
🤖 Robotics & Embedded Systems Enthusiast | PCB Designer  
💼 Founder & CEO, Pico Robotics

- 🌐 **Website:** [shoyabsadik.github.io](https://shoyabsadik.github.io)
- 💻 **GitHub:** [@shoyabsadik](https://github.com/shoyabsadik)
- 🔗 **LinkedIn:** [M. Shoyab Sadik](https://www.linkedin.com/in/shoyabsadik/)

## ✨ Key Features

- 🔌 **AC Input Protection:** Fuse (F1), varistor (RV1), NTC resistor (R14), and common-mode choke (L1).
- ⚡ **Bridge Rectifier:** GBU806 bridge rectifier for AC-to-DC conversion.
- 🔋 **Auxiliary Power Supply:** LNK3204D offline switching controller with PC817 optocoupler.
- 🎛️ **Three-Phase Gate Driver:** 6EDL04I06PT driver (U4).
- ⚙️ **Power Switching Stage:** Six IKD04N60RC2 IGBTs (Q3–Q8).
- 📉 **Current Sensing:** 150 mΩ, 1%, 3/4 W shunt resistor (RS1).
- 🔍 **Testing & Debugging:** Connectors J1–J4 and test points TP5 and TP6.

## 🧩 Key Component List

| Reference | Component | Function |
|---|---|---|
| F1 | T3.15A Fuse | Input overcurrent protection |
| RV1 | Varistor | Surge protection |
| R14 | NTC Resistor | Inrush current limiting |
| L1 | Common-Mode Choke | Input EMI filtering |
| BR | GBU806 Bridge Rectifier | AC-to-DC rectification |
| U2 | LNK3204D* | Auxiliary offline power supply |
| U3 | PC817 | Optocoupler isolation |
| U4 | 6EDL04I06PT | Three-phase gate driver |
| Q3–Q8 | IKD04N60RC2 | IGBT switching stage |
| RS1 | 150 mΩ Shunt Resistor | Current sensing |

*Component references and ratings should be verified against the contest schematic, BOM, and manufacturer datasheets.*

## 📐 PCB Layout & Design Considerations

- ⚡ **Power Flow:** AC input → bridge rectifier → DC link → IGBT switching stage → motor output.
- 🎛️ **Gate-Drive Routing:** Short, direct connections between the gate driver and IGBT gates.
- 🔄 **DC-Link Loop:** Minimize high-current switching loop area to reduce parasitic inductance.
- 📡 **Signal Separation:** Keep switching nodes away from sensitive sensing and control signals.
- 🌡️ **Thermal Management:** Use appropriately sized copper areas and thermal vias where required.
- 📏 **High-Voltage Isolation:** Maintain suitable creepage and clearance distances between high-voltage and low-voltage circuits.
- 🔍 **Test Accessibility:** Provide suitable test points for DC bus, phase, gate-drive, and auxiliary supply measurements.

## 📁 Project Files

The design files are organized within the `Problem_2` directory.

| File | Description |
|---|---|
| 📐 `ShoyabSadik_IUBAT.json` | EasyEDA schematic and PCB source |
| 📄 `ShoyabSadik_IUBAT.pdf` | PCB layer documentation |
| 📝 `ShoyabSadik_IUBAT_report.docx` | Technical design report |

### 📂 Supporting Resources

- 📐 [EasyEDA PCB Source Files](PCB_Files_EasyEDA_2/)
- 🖼️ [PCB Pictures & Previews](PCB_Pictures_2/)
- 📄 [Gerber Files](Gerber_2/)
- 📝 [Design Report](Report_2/)

📌 *These folder links assume the corresponding directories exist inside `Problem_2`. Update them if your actual folder names differ.*

## 🖥️ PCB Preview

Add your schematic, PCB layout, and 3D screenshots to the `PCB_Pictures_2` folder.

| 📐 Schematic | 🟩 Top Layer |
|---|---|
| ![Schematic](PCB_Pictures_2/schematic.png) | ![Top Layer](PCB_Pictures_2/top.png) |

| 🔵 Bottom Layer | 🧊 3D PCB View |
|---|---|
| ![Bottom Layer](PCB_Pictures_2/bottom.png) | ![3D PCB](PCB_Pictures_2/3d.png) |

📌 Ensure the image filenames match the files uploaded to GitHub.

## 🚀 How to Open the Design

1. 🌐 Visit [EasyEDA](https://easyeda.com).
2. 🖥️ Open the appropriate EasyEDA editor version.
3. 📥 Navigate to **File → Open → EasyEDA Source…**.
4. 🗂️ Select `ShoyabSadik_IUBAT.json`.
5. 🔍 Inspect the schematic, footprints, component placement, and routing.
6. ✅ Run **Design → Check DRC** to review design-rule violations.

## 🛠️ Tools & Technologies

`EasyEDA` `PCB Design` `Power Electronics` `Three-Phase Inverter` `BLDC/PMSM` `IGBT` `Gate Driver` `Current Sensing` `EMI Filtering` `DRC`

## ⚠️ High-Voltage Safety Notice

**This design involves potentially lethal mains voltage and a high-voltage DC bus.**

- 🚫 Never energize the PCB without qualified supervision and appropriate safety precautions.
- 🔌 Disconnect all power sources and verify that DC-link capacitors are discharged before handling the board.
- 🛡️ Use appropriate isolation, current limiting, protective equipment, and safe measurement procedures.
- ⚡ Maintain the required creepage, clearance, insulation, and protective-earth arrangements for the intended application.

This project documentation is for educational and design-review purposes. A PCB layout or successful DRC check alone does not establish electrical safety.

## 📝 Design Notes

- 📌 The contest question lists U2 as **LNK3204D**, while the schematic text shows **LNK304DN**. The component list designation is recorded here; verify the intended part before finalizing the design.
- 🧩 Footprints unavailable in the library were created using manufacturer datasheets, where necessary.
- 🔍 Verify component ratings, footprint dimensions, pinouts, isolation requirements, and thermal limits before fabrication or testing.

## ✅ Design Verification Checklist

- [ ] 📐 Schematic reviewed
- [ ] 🧩 Footprints checked against datasheets
- [ ] 🟩 Component placement completed
- [ ] 🔀 PCB routing completed
- [ ] ⚡ High-voltage clearances reviewed
- [ ] 🌡️ Thermal and current paths reviewed
- [ ] 🔍 DRC verification completed
- [ ] 📄 Layer-wise PDF exported
- [ ] 📝 Technical report completed
- [ ] 🖼️ PCB preview images added

*Update the checklist to reflect the actual completion and verification status.*

## 📄 License & Attribution

This repository is shared for educational, learning, and portfolio purposes. The original reference architecture, trademarks, and third-party library assets remain the property of their respective owners, including Infineon Technologies and other component manufacturers.

Please follow the applicable licenses and attribution requirements when reusing third-party materials.

---

💡 **Think • Design • Build • Innovate**

**M. Shoyab Sadik**  
*B.Sc. in EEE | IUBAT | PCB Design & Embedded Systems*
