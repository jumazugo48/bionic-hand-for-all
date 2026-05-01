# Hardware

This folder contains all electronic design files for the
Bionic Hand For All project.

## Contents

- Schematics (KiCad)
- PCB layouts (KiCad)
- Gerber files for fabrication
- Bill of materials for each board

## Main Boards

- **EMG Signal Capture Board** — Custom AD620-based circuit
  for electromyographic signal acquisition and amplification
- **Main Control Board** — ESP32-based processing and
  servo control unit

## Software Required

| File type | Software |
|---|---|
| `.kicad_sch` | KiCad 7 (free) |
| `.kicad_pcb` | KiCad 7 (free) |
| `.gbr` / Gerber | KiCad 7 or any Gerber viewer |

## References

The EMG signal conditioning stage is based on standard
instrumentation amplifier topology for biopotential acquisition,
implemented with the AD620. Circuit design by Juan Manuel Zumel González.

## License

All files in this folder are licensed under
[CC BY-NC-SA 4.0](../LICENSE-HARDWARE).
