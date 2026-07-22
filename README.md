# OpenBattery Hub

An open-hardware ESP32-S3 board for the [OpenDTU-OnBattery](https://github.com/hoylabs/OpenDTU-OnBattery)
ecosystem.

- **3x isolated VE.Direct** for Victron MPPT charge controllers
- **CAN + RS485** for BMS communication (Pylontech, JK, and compatible protocols)
- **2.4 GHz NRF24** and **868 MHz CMT2300A** radios for Hoymiles microinverters
- ESP32-S3 based

## Status

- Hardware revision: **1.9.3**
- Field-tested small series (JLCPCB manufacturing)

## Repository layout

```
hardware/
  schematics/   schematic exports (PDF)
  pcb/          PCB layout exports (PDF/PNG)
  bom/          Bill of Materials
  fabrication/  Pick-and-Place data and other assembly files
  gerber/       Gerber/drill files for fabrication
  source/       editable EasyEDA source files (Complete Source, TODO — see hardware/source/README.md)
docs/           additional documentation
```

## License

The hardware design files in this repository are licensed under the
**CERN Open Hardware Licence Version 2 - Strongly Reciprocal (CERN-OHL-S v2)**.

See [LICENSE](LICENSE) for the full licence text and [NOTICE.md](NOTICE.md)
for the required notice, source location, and scope (including what is
*not* covered — e.g. firmware and the project name/logo).

Firmware is **not** part of this repository. This board is designed to run
[OpenDTU-OnBattery](https://github.com/hoylabs/OpenDTU-OnBattery), an
independent open-source project licensed under GPL-3.0.
