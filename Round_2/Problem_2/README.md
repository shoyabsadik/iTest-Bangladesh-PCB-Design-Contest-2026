# Problem 2 – Infineon REF-FRIDGE-C101T-6ED Motor/Inverter Controller

Three-phase inverter and control PCB for a BLDC/PMSM motor, based on the Infineon REF-FRIDGE-C101T-6ED reference architecture.

## Features

- AC input stage: fuse F1 (T3.15A), varistor RV1, NTC R14, common-mode choke L1, bridge rectifier BR (GBU806)
- Off-line switcher U2 (LNK3204D) with optocoupler U3 (PC817) for the control supply
- 3-phase gate driver U4 (6EDL04I06PT)
- Six IGBTs Q3–Q8 (IKD04N60RC2)
- Shunt resistor RS1 (150 mΩ, 1 %, 3/4 W) for current sensing
- Connectors J1–J4 and test points TP5, TP6

## Design focus

- Logical power flow: AC in → rectifier → DC link → IGBT stage → motor.
- Short, direct gate-drive traces from U4 to the IGBTs.
- Small DC-link loop area.
- Switching nodes kept away from sensing and control signals.
- Wide copper for current paths, thermal copper and vias around power parts.
- Creepage and clearance between high-voltage and low-voltage areas.
- Test points for DC bus, phase, drive and control supply.

> **High voltage:** this design carries mains-level voltage. Do not power it without proper isolation and safety checks.

## Files

| File | Description |
|------|-------------|
| `ShoyabSadik_IUBAT.json` | EasyEDA schematic and board |
| `ShoyabSadik_IUBAT.pdf` | All layers, one per page |
| `ShoyabSadik_IUBAT_report.docx` | Design report |

## Notes

- The question lists U2 as LNK3204D, while the schematic text shows LNK304DN. The component list name is used.
- Footprints missing from the library were built from the datasheets.

## Status

- [ ] Placement complete
- [ ] Routing complete
- [ ] DRC: 0 errors
- [ ] Layer PDF exported

## Preview

| Schematic | Top | Bottom | 3D |
|-----------|-----|--------|----|
| ![](images/schematic.png) | ![](images/top.png) | ![](images/bottom.png) | ![](images/3d.png) |
