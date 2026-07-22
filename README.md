# OpenBattery Hub

![OpenBattery Hub PCB](docs/screenshot/2D_PCB%201.9.3_2026-07-22.png)

OpenBattery Hub is a DIY-friendly, open-hardware ESP32-S3 IoT platform built
to work seamlessly with the open-source [OpenDTU-OnBattery](https://github.com/hoylabs/OpenDTU-OnBattery)
Project. It makes it easy to connect and monitor batteries, solar charge
controllers, and inverters — all in one compact device. Whether you're
building your own off-grid setup or just love tinkering with energy tech,
the Hub is designed to keep things simple, open, and fun to experiment with.

| Function | Specification |
|---|---|
| MCU | ESP32-S3 16MB |
| CAN Bus / RS-485 Interfaces | SN65HVD230DR / ISL3178EIBZ-T |
| VE.Direct Interfaces | 3x isolated, 4-PIN JST PH |
| Power & Programming | USB-C, onboard 5V-to-3.3V regulator, max. 1A |
| Dual Inverter Interface | Nordic NRF24L01+ (HM) / EByte CMT2300A (HMS/T) |

## What you can do with it

- Unlock the full potential of OpenDTU-OnBattery — all features fully supported
- Connect and control Hoymiles HM, HMS, and HMS-T inverters
- Connect and monitor up to 3 Victron MPPTs
- Interface with popular batteries like Pylontech (CAN bus), JK-BMS, and Victron SmartShunt
- Optionally add a compact OLED display for real-time stats right on the device

## Enclosure

A 3D-printable case is included (see [`hardware/case`](hardware/case)).

<p>
  <img src="docs/Case.jpeg" alt="OpenBattery Hub in its 3D-printed case" width="49%">
  <img src="docs/Case Open.jpeg" alt="OpenBattery Hub case opened, board visible" width="49%">
</p>

## Status

- Hardware revision: **1.9.3**
- Field-tested with approx. 50 units

## Getting started

1. Power the board via USB-C (5V / 2A recommended).
2. Wait for it to create its own Wi-Fi hotspot, `OpenDTU-xxxxxx` (default password `OpenDTU42`).
3. Connect and open `192.168.4.1` in a browser to run through the setup, selecting the configuration profile that matches your battery/MPPT/inverter setup.
4. Wire up your solar gear according to the selected profile.

Full specifications, port pinouts, wiring diagrams for common setups
(Pylontech CAN, JK-BMS RS485, Victron SmartShunt, multi-MPPT), and the
optional OLED/serial header pinout are documented in
[`docs/Openbattery Hub - Datasheet & Manual.pdf`](docs/Openbattery%20Hub%20-%20Datasheet%20%26%20Manual.pdf).

A more comprehensive overview of OpenDTU-OnBattery itself is available at
[opendtu-onbattery.net](https://opendtu-onbattery.net/).

## Repository layout

```
hardware/
  schematics/   schematic exports (PDF)
  pcb/          PCB layout exports (PDF/PNG)
  bom/          Bill of Materials
  fabrication/  Pick-and-Place data and other assembly files
  gerber/       Gerber/drill files for fabrication
  case/         3D-printable enclosure files
  source/       editable EasyEDA/Altium source files (Complete Source, see hardware/source/README.md)
docs/           datasheet/manual, photos, additional documentation
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
