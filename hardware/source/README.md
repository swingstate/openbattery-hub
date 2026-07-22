# Source (editable design files)

This directory contains:

- `Netlist_Schematics_*.enet` — schematic netlist (components, footprints,
  supplier/manufacturer part references, connectivity)
- `Netlist_PCB_*.enet` — PCB netlist (component-to-net mapping as placed
  on the board)

**TODO: these netlists are not the "Complete Source" required by
CERN-OHL-S v2 section 1.9.** They record connectivity and part data, but
not the schematic sheet layout or PCB component placement/routing —
recipients cannot recreate or fully re-edit the design from a netlist
alone. Still needed here: the actual editable EasyEDA project export
(schematic + PCB, e.g. via EasyEDA's "Export → EasyEDA Source Files")
that preserves layout, routing, and drawing data.

Until that is added, recipients cannot fully exercise the rights this
licence is meant to guarantee (study and modify the design). If you are
looking to fork or modify the board before the full source files are
added, open an issue or get in touch.
