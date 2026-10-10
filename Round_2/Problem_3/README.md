# 🌐 Problem 3 — STM32 Ethernet + CAN + RS-485 Industrial Gateway

🚀 A compact industrial communication gateway designed using **EasyEDA** for the iTest Bangladesh PCB Design Contest 2026 — Round 2.

The design integrates Ethernet, CAN, RS-485, and RS-232 interfaces with an STM32F407VET6 microcontroller, making it suitable as a foundation for industrial communication, automation, and robotics applications.

## 👨‍💻 Author

**M. Shoyab Sadik**  
🎓 B.Sc. in Electrical and Electronic Engineering (EEE) — IUBAT  
🤖 Robotics & Embedded Systems Enthusiast | PCB Designer  
💼 Founder & CEO, Pico Robotics

- 🌐 **Website:** [shoyabsadik.github.io](https://shoyabsadik.github.io)
- 💻 **GitHub:** [@shoyabsadik](https://github.com/shoyabsadik)
- 🔗 **LinkedIn:** [M. Shoyab Sadik](https://www.linkedin.com/in/shoyabsadik/)

## ✨ Key Features

- 🧠 **Main Controller:** STM32F407VET6 microcontroller (LQFP-100).
- 🌐 **Ethernet Interface:** DP83848IVV PHY with RMII connectivity and RJ45 magnetics.
- 🔗 **CAN Communication:** SN65HVD230 transceiver.
- 🏭 **RS-485 Communication:** ST3485 transceiver for industrial serial communication.
- 🔌 **RS-232 Interface:** ADM3202 transceiver with DB9 connectors.
- 💻 **USB Connectivity:** FT230XS-U USB-to-UART bridge and Mini-B connector.
- 💾 **Memory & Storage:** AT45DB161E SPI flash, M95256 EEPROM, and microSD interface.
- ⚡ **Power Management:** 24 V input, protection circuitry, LM2596S-5.0 buck converter, and LM1117-3.3 LDO.
- 🔔 **Indicators & Alerts:** Buzzer, status LEDs, and debugging test points.
- 🔧 **Expansion Interfaces:** JST 2×8 connector and multiple external communication connectors.

## 🧩 Key Component List

| Reference | Component | Function |
|---|---|---|
| D8 | STM32F407VET6 | Main microcontroller |
| D10 | DP83848IVV | Ethernet PHY |
| X12 | TRJ0011TBNL | RJ45 connector with magnetics |
| D3 | SN65HVD230 | CAN transceiver |
| D6 | ST3485 | RS-485 transceiver |
| D9 | ADM3202 | RS-232 transceiver |
| D4 | FT230XS-U | USB-to-UART bridge |
| X1 | USB Mini-B | USB interface |
| D1 | AT45DB161E | SPI flash memory |
| D2 | M95256 | EEPROM |
| X4 | microSD interface | Removable storage |
| X2 | 24 V input | Power input |
| D5 | LM2596S-5.0 | Step-down converter |
| D7 | LM1117-3.3 | 3.3 V voltage regulator |
| X5, X7 | DB9 connectors | Serial interfaces |

📌 *Verify component reference designators, package variants, and pin assignments against the original schematic and manufacturer datasheets.*

## 📐 PCB Layout & Design Considerations

- 🌐 **Ethernet Routing:** Route TX/RX differential pairs with controlled impedance appropriate to the PHY and magnetics design, minimizing unnecessary vias and stubs.
- 🔌 **PHY Placement:** Position the Ethernet PHY between the MCU and RJ45 interface to support a clean signal path.
- 🛡️ **ESD Protection:** Place suitable protection components near external connectors, with low-inductance paths to the appropriate return.
- 🔗 **CAN & RS-485:** Provide appropriate termination and protection according to the intended bus topology.
- ⚡ **Power Management:** Keep the buck-converter switching loop compact and separate from sensitive clock and communication circuitry.
- 🧠 **MCU Decoupling:** Place suitable decoupling capacitors close to the microcontroller supply pins.
- 🌍 **Grounding:** Plan return-current paths carefully across power, digital, and interface sections rather than splitting ground indiscriminately.
- 📍 **Connector Placement:** Position external connectors along board edges for accessibility.
- 🏷️ **Silkscreen & Testing:** Label connectors, signal names, polarity, and test points for easier assembly and debugging.

## 📁 Project Files

The project files are organized within the `Problem_3` directory.

| File | Description |
|---|---|
| 📐 `ShoyabSadik_IUBAT.json` | EasyEDA schematic and PCB source |
| 📄 `ShoyabSadik_IUBAT.pdf` | PCB layer documentation, one layer per page |
| 📝 `ShoyabSadik_IUBAT_report.docx` | Technical design report |

### 📂 Supporting Resources

- 📐 [EasyEDA PCB Source Files](PCB_Files_EasyEDA_3/)
- 🖼️ [PCB Pictures & Previews](PCB_Pictures_3/)
- 📄 [Gerber Files](Gerber_3/)
- 📝 [Design Report](Report_3/)

📌 *These links assume the listed folders exist inside `Problem_3`. Update the paths if your actual folder names differ.*

## 🖥️ PCB Preview

Add the following images to the `PCB_Pictures_3` directory.

| 📐 Schematic | 🟩 Top Layer |
|---|---|
| ![Schematic](PCB_Pictures_3/schematic.png) | ![Top Layer](PCB_Pictures_3/top.png) |

| 🔵 Bottom Layer | 🧊 3D PCB View |
|---|---|
| ![Bottom Layer](PCB_Pictures_3/bottom.png) | ![3D PCB](PCB_Pictures_3/3d.png) |

📌 Ensure the image filenames match the actual files uploaded to GitHub.

## 🚀 How to Open the Design

1. 🌐 Visit [EasyEDA](https://easyeda.com).
2. 🖥️ Open the appropriate EasyEDA editor version.
3. 📥 Navigate to **File → Open → EasyEDA Source…**.
4. 🗂️ Select `ShoyabSadik_IUBAT.json`.
5. 🔍 Review the schematic, footprints, PCB placement, and routing.
6. ✅ Run **Design → Check DRC** to inspect design-rule violations.

## 🛠️ Tools & Technologies

`EasyEDA` `STM32` `Ethernet` `RMII` `CAN Bus` `RS-485` `RS-232` `USB-UART` `SPI Flash` `EEPROM` `microSD` `Power Management` `PCB Layout` `DRC`

## 📝 Design Notes

- ⚡ **Power Converter:** The LM2596S-5.0 regulator (D5) appears in the schematic but is missing from the supplied component list; it has been included in the design according to the project notes.
- 🔌 **Connector Assignment:** DB9 connectors X5 and X7 are used for the serial interfaces to avoid a reference-designator conflict with USB Mini-B connector X1.
- 🧩 **Custom Footprints:** Footprints not available in the component library, including the RJ45 connector, JST 2×8 connector, selected TVS components, and crystals, were created using manufacturer datasheets where necessary.
- 🔍 **Design Verification:** Verify the power-input ratings, Ethernet differential impedance, transceiver termination, connector pinouts, and protection circuits before fabrication.

## ✅ Design Verification Checklist

- [ ] 📐 Schematic reviewed
- [ ] 🧩 Component footprints verified
- [ ] 🟩 PCB placement completed
- [ ] 🔀 PCB routing completed
- [ ] 🌐 Ethernet routing reviewed
- [ ] 🛡️ Interface protection and termination reviewed
- [ ] ⚡ Power circuitry checked
- [ ] 🔍 DRC verification completed
- [ ] 📄 Layer-wise PDF exported
- [ ] 📝 Technical report completed
- [ ] 🖼️ PCB preview images added

*Update this checklist to reflect the actual completion and verification status of the design.*

## 📄 License & Attribution

This repository is shared for educational, learning, and portfolio purposes. Third-party component designs, trademarks, reference materials, and library assets remain the property of their respective owners, including STMicroelectronics, Texas Instruments, Texas Instruments' interface-component suppliers, and other relevant manufacturers.

Please follow the original licensing and attribution requirements when reusing third-party materials.

---

💡 **Think • Design • Build • Innovate**

**M. Shoyab Sadik**  
*B.Sc. in EEE | IUBAT | PCB Design & Embedded Systems*
