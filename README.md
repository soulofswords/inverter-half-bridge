# 12 V Battery Backup Inverter

This repository documents a low-power, battery-backed inverter project intended for portable backup loads such as aquarium aerators, aquarium lighting, and a small desk fan. The design combines automatic grid/battery transfer, a filtered charging path, and a transistor-driven transformer output stage.

> **Safety warning:** This is an experimental, non-certified power-electronics project. The output and transformer wiring can present lethal mains-level voltage. Use an enclosure, fusing, insulation, strain relief, earthing where applicable, and appropriate test equipment. Never work on the circuit while energized. The lithium-ion battery pack requires a suitable battery-management and charging strategy; damaged or mismatched 18650 cells can cause fire or explosion.

## Verified design

- Two nominal 12 V, 2 A transformers are used in the documented power path.
- Input AC is converted through a full-bridge rectifier and smoothed with capacitors.
- A 12 V relay selects between the grid-derived charging path and the battery path.
- The battery pack drives a TTC5200 transistor stage; the second transformer produces nominal 220 V AC.
- The battery pack is documented as 12 × 18650 cells in a 3S4P arrangement.
- Listed components include a 1 kΩ resistor, 1 µF/63 V and 2200 µF/16 V capacitors, two 1N5408 diodes, one 1N4007 diode, a relay, and a junction box.

The source report uses both “half-bridge” and broader bridge-related terminology. This README intentionally does not claim a strict half-bridge topology where the available documentation is not unambiguous.

## Operating principle

During grid operation, the rectifier and capacitor stage provide a filtered low-voltage charging path. When grid power is unavailable, the relay transfers the load to the 12 V battery system. The transistor stage switches the battery-side transformer so the output transformer can provide nominal 220 V AC for the intended low-power loads.

## Testing and reported results

The report references CircuitLab, Tinkercad, EasyEDA, and Proteus for design and simulation work. It reports a simulated output of approximately 24 W at 220 V AC, with intended loads including 5 W aquarium air pumps and 20–24 W lighting. It also documents a 12.6 V, 8 A battery input and an estimated runtime of up to about five hours, dependent on cell condition and load.

The documented output is not pure sine wave. The report notes TTC5200 heating and thermal-performance concerns. It also states that the inverter is not intended for televisions, refrigerators, irons, kettles, laptops, or other unsuitable loads. The hardware preparation described includes a PCB and heatsink, while drilling, mounting, and soldering were still outstanding in the report.

These are reported project results, not independent certification or a guarantee of safe continuous operation.

## Documentation

- [`TECHNICAL-SUMMARY.md`](TECHNICAL-SUMMARY.md) — sanitized source-based summary of the report, including scope and limitations.

## Project status

The repository is documentation-first. The source report describes an experimental prototype and identifies remaining mechanical and assembly work; no claim is made here that a finished, safety-certified product exists.
