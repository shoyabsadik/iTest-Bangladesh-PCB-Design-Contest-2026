# Problem 3 – STM32 Ethernet + CAN + RS-485 Industrial Gateway

Compact industrial gateway that bridges Ethernet, CAN and RS-485 for factory and robotics use.

## Features

- MCU STM32F407VET6 (D8, LQFP-100)
- Ethernet PHY DP83848IVV (D10) with RJ45 magnetics TRJ0011TBNL (X12), RMII interface
- CAN transceiver SN65HVD230 (D3), RS-485 transceiver ST3485 (D6), RS-232 transceiver ADM3202 (D9)
- USB-UART bridge FT230XS-U (D4), USB Mini-B (X1)
- SPI flash AT45DB161E (D1), EEPROM M95256 (D2), microSD (X4)
- 24 V input (X2) with fuses, TVS, LM2596S-5.0 buck (D5) and LM1117-3.3 LDO (D7)
- Crystals BQ1–BQ3, buzzer G1, LEDs HL1–HL6, DB9 connectors X5, X7, JST 2×8 connector X11

## Design focus

- Ethernet TX/RX as 100 Ω differential pairs, short and without vias.
- PHY placed between the MCU and the RJ45.
- TVS/ESD protection and termination resistors on CAN and RS-485.
- Ground partitioning between power, digital and interface sections.
- Compact buck stage kept away from Ethernet and crystals.
- Decoupling capacitor at every MCU supply pin.
- Connectors on the board edges, test points and clean silkscreen.

## Files

| File | Description |
|------|-------------|
| `ShoyabSadik_IUBAT.json` | EasyEDA schematic and board |
| `ShoyabSadik_IUBAT.pdf` | All layers, one per page |
| `ShoyabSadik_IUBAT_report.docx` | Design report |

## Notes

- D5 (LM2596S-5.0) is in the schematic but missing from the component list; it is included in the design.
- The RS-232 DB9 connectors are X5 and X7 to avoid a clash with the USB Mini-B (X1).
- Footprints missing from the library (RJ45, JST 2×8, some TVS and crystals) were built from datasheets.

## Status

- [ ] Placement complete
- [ ] Routing complete
- [ ] DRC: 0 errors
- [ ] Layer PDF exported

## Preview

| Schematic | Top | Bottom | 3D |
|-----------|-----|--------|----|
| ![](images/schematic.png) | ![](images/top.png) | ![](images/bottom.png) | ![](images/3d.png) |
