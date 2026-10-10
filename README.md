# iTest Bangladesh PCB Design Contest 2026

My PCB designs for the **iTest Bangladesh PCB Design Contest 2026**, made in **EasyEDA**.

**Author:** M. Shoyab Sadik – IUBAT (B.Sc. in EEE)
**EDA tool:** EasyEDA
**Rounds:** Round 1 (deadline 6 Oct 2026) and Round 2

## Contents

| Round | Problem | Design | Folder |
|-------|---------|--------|--------|
| 1 | P1 | SparkFun Artemis Development Kit | [Round1/P1_Artemis_Dev_Kit](Round1/P1_Artemis_Dev_Kit) |
| 1 | P2 | Circuit Playground Express inspired controller | [Round1/P2_Circuit_Playground_Express](Round1/P2_Circuit_Playground_Express) |
| 1 | P3 | ExpressLRS ESP32 RF development PCB | [Round1/P3_ExpressLRS_ESP32_RF](Round1/P3_ExpressLRS_ESP32_RF) |
| 1 | Bonus | 555 timer + logic gate circuit | [Round1/Bonus_555_Logic](Round1/Bonus_555_Logic) |
| 2 | P1 | SparkFun OpenLog Artemis Data Logger (110 marks) | [Round2/Round2_P1_OpenLog_Artemis](Round2/Round2_P1_OpenLog_Artemis) |
| 2 | P2 | Infineon REF-FRIDGE-C101T-6ED Motor/Inverter (70 marks) | [Round2/Round2_P2_Infineon_Motor_Inverter](Round2/Round2_P2_Infineon_Motor_Inverter) |
| 2 | P3 | STM32 Ethernet + CAN + RS-485 Gateway (120 marks) | [Round2/Round2_P3_STM32_Gateway](Round2/Round2_P3_STM32_Gateway) |

See [Round1](Round1/README.md) and [Round2](Round2/README.md) for the round overviews.

## What each design folder holds

```
<problem>/
├── README.md                      overview and design notes
├── ShoyabSadik_IUBAT.json         EasyEDA schematic + board files
├── ShoyabSadik_IUBAT.pdf          all layers, one layer per page
├── ShoyabSadik_IUBAT_report.docx  design report with 2D and 3D views
└── images/                        schematic, top, bottom and 3D screenshots
```

## Evaluation criteria (same in both rounds)

| Category | Weight |
|----------|--------|
| Schematic design | 15–20 % |
| Custom library creation | 5–10 % |
| PCB layout design | 25–30 % |
| DRC compliance (5 marks off per logical error) | 15–20 % |
| Creativity and design efficiency | 10–15 % |
| Aesthetics and documentation | 10–15 % |
| Bonus for innovative routing/aesthetics | up to 5 marks |

## Contest rules followed

- EasyEDA only, designed from the given schematic and component list.
- No pre-made full designs; reference libraries only.
- Separate files, no ZIP: schematic, board, layer PDF, report, named `name_uni.filetype`.

## How to open the designs

1. Open [EasyEDA](https://easyeda.com).
2. `File` → `Open` → `EasyEDA Source…` and choose the `.json` file.
3. Run `Design` → `Check DRC` to verify.

## Skills shown

Schematic capture, custom symbol and footprint creation, 2-layer PCB layout, USB and RF-aware placement, power and high-voltage layout, high-speed Ethernet routing, DRC and documentation.

## License

Shared for learning and portfolio use. Reference designs and library parts belong to their original owners (SparkFun, Adafruit, Espressif, Infineon, STMicroelectronics, Texas Instruments, etc.).
