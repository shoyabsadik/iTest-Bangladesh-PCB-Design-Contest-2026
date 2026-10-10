# Problem 1 – SparkFun OpenLog Artemis Data Logger

Compact data-logging PCB based on the SparkFun OpenLog Artemis architecture. It records motion and sensor data to a microSD card and offers USB, serial and Qwiic/I²C connectivity.

## Features

- Artemis module (U8) with local decoupling
- ICM-20948 9-DoF IMU (U13)
- microSD socket (J6) with MOSFET power switch (Q2) and level shifting (Q1, Q3, Q7, Q9, Q10)
- USB Type-C (J5) with CH340E USB-to-serial bridge (U10)
- LiPo charger MCP73831 (U2), JST 2 mm battery connector (J2)
- 3.3 V LDOs AP2112K (U3, U4), 1.8 V LDO (U14), 3.0 V supervisor (U1)
- Qwiic connector (J11), Cortex SWD/JTAG header (J14), headers J1, J3, J4, J7
- 32.768 kHz crystal (Y3), RTC battery ML414H (BT1), reset switch (S3)
- Test points: GND, QWIIC_3.3V, SCL, SDA, TP1

## Key component list

| Ref | Part | Package |
|-----|------|---------|
| U8 | Artemis module | ARTEMIS_FP |
| U13 | ICM-20948 | QFN-24 |
| U10 | CH340E | MSOP-10 |
| U2 | MCP73831 | SOT-23-5 |
| U3, U4 | AP2112K-3.3 | SOT-23-5 |
| U14 | 1.8 V LDO (SP6214 equivalent) | SOT-23-5 |
| Q1, Q3, Q7, Q9, Q10 | 2N7002 | SOT-23 |
| Q2 | AO3401A | SOT-23 |
| J5 | HX TYPE-C 16P-CT | SMD |
| J11 | SM04B-SRSS-TB | SMD |
| J2 | S2B-PH-SM4-TB | SMD |

## Layout notes

- Artemis module and its decoupling capacitors are placed together.
- IMU is kept away from USB and the charger/power section.
- microSD socket and USB-C are at the board edge.
- LiPo connector, charger and LDOs form one power section.
- Qwiic connector on the perimeter with short SDA/SCL.
- GND pour on both layers with stitching vias.
- Silkscreen marks connector names, polarity and pin functions.

## Files

| File | Description |
|------|-------------|
| `ShoyabSadik_IUBAT.json` | EasyEDA schematic and board |
| `ShoyabSadik_IUBAT.pdf` | All layers, one per page |
| `ShoyabSadik_IUBAT_report.docx` | Design report |

## Status

- [ ] Placement complete
- [ ] Routing complete
- [ ] DRC: 0 errors
- [ ] Layer PDF exported

## Preview

| Schematic | Top | Bottom | 3D |
|-----------|-----|--------|----|
| ![](images/schematic.png) | ![](images/top.png) | ![](images/bottom.png) | ![](images/3d.png) |
