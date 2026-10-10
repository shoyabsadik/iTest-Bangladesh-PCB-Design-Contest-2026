# iTest Bangladesh PCB Design Contest 2026 – Round 2

PCB designs made in **EasyEDA** for Round 2 of the iTest Bangladesh PCB Design Contest 2026.

**Author:** M. Shoyab Sadik – IUBAT (B.Sc. in EEE)

## Projects

| # | Project | Type | Marks | Folder |
|---|---------|------|-------|--------|
| 1 | SparkFun OpenLog Artemis Data Logger | Precision analog / data acquisition | 110 | [Round2_P1_OpenLog_Artemis](Round2_P1_OpenLog_Artemis) |
| 2 | Infineon REF-FRIDGE-C101T-6ED Motor/Inverter Controller | Motor control / power electronics | 70 | [Round2_P2_Infineon_Motor_Inverter](Round2_P2_Infineon_Motor_Inverter) |
| 3 | STM32 Ethernet + CAN + RS-485 Industrial Gateway | High-speed digital | 120 | [Round2_P3_STM32_Gateway](Round2_P3_STM32_Gateway) |

## Repository layout

Each project folder follows the same layout:

```
Round2_Px_<name>/
├── README.md                    project overview, design notes, how to open
├── ShoyabSadik_IUBAT.json       EasyEDA schematic + board files
├── ShoyabSadik_IUBAT.pdf        all layers, one layer per page
├── ShoyabSadik_IUBAT_report.docx  design report with 2D and 3D views
└── images/                      schematic, top, bottom and 3D screenshots
```

## How to open the designs

1. Open [EasyEDA](https://easyeda.com) (Standard or Pro, matching the file version).
2. `File` → `Open` → `EasyEDA Source…` and choose the `.json` file.
3. Use `Design` → `Check DRC` to re-run the design rule check.

## Tools

- EasyEDA (schematic, PCB layout, DRC, 3D preview)
- Component footprints from the EasyEDA/LCSC library; custom footprints built from datasheets where needed

## Contest rules followed

- Designed only with EasyEDA, from the schematic and component list in the question.
- No pre-made full designs were used; reference libraries only.
- Submitted as separate files (no ZIP): schematic, board, layer PDF, report.

## License

Shared for learning and portfolio use. Reference designs and library parts belong to their original owners (SparkFun, Infineon, STMicroelectronics, Texas Instruments, etc.).
