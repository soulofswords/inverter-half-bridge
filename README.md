# Low-Power Automatic Battery Inverter

A student-built, low-power backup inverter concept designed for small aquarium and lighting loads during a mains outage. The project combines automatic grid/battery transfer, battery charging, DC-to-AC conversion, and basic protection in a compact architecture.

> **Safety:** This is an educational prototype, not a certified mains product. The design includes lethal voltages and lithium-ion cells. Do not reproduce or connect it to mains power without qualified supervision, appropriate isolation, fusing, enclosure, measurement equipment, and battery protection.

## What the report documents

- Nominal 12 V battery system with a reported 220 V AC output target
- 220/12 V center-tapped transformers used for the supply and output stages
- AC-to-DC rectification and smoothing with bridge-rectifier diodes and capacitors
- Relay-controlled transfer between grid-derived charging and battery operation
- TTC5200 transistor switching stage
- 12-cell 18650 battery pack described as 3S4P (three series groups of four parallel cells)
- Automatic battery charging / transfer behavior and charge-level indication goals

The report uses bridge-rectifier and inverter terminology in different sections; this repository intentionally avoids claiming a strict half-bridge topology where the supplied documentation is not unambiguous.

## Reported design targets and results

The report describes a CircuitLab simulation target of approximately **24 W at 220 V AC**, with low-power aquarium air pumps and lighting as intended loads. It reports an estimated backup duration of up to about **five hours**, dependent on cell condition, charge state, and load. The hardware section records a prepared PCB and heatsink, with further assembly work still remaining at the time of writing.

The output is not presented as a pure sine wave. The report also notes transistor heating and recommends improved thermal management. The prototype is not intended for high-power appliances such as refrigerators, kettles, irons, televisions, or laptops.

## High-level operation

1. A transformer and rectifier/filter stage provide a low-voltage DC charging path when grid power is available.
2. A relay detects the grid state and selects either the charging path or the battery-powered inverter path.
3. The battery supplies the TTC5200 switching stage.
4. The transformer output stage produces the reported AC output for small loads.
5. Protection and charging behavior are intended to prevent overcharge and excessive battery discharge.

The exact schematic, component ratings, switching waveform, and protection implementation must be independently reviewed before any physical build or connection to a load.

## Components reported in the project

- Two 12 V, 2 A transformers
- 12 V relay
- TTC5200 transistor
- 1 kΩ resistor
- 1 µF / 63 V capacitor
- 2200 µF / 16 V capacitor
- Two 1N5408 diodes and one 1N4007 diode
- 12-cell 18650 battery pack, described as 3S4P
- Junction box and heatsink

These entries reproduce the project report at a high level; verify every part number, polarity, voltage rating, current rating, and thermal limit against the final schematic and datasheets.

## Limitations

- Non-sinusoidal output may be unsuitable for sensitive or inductive equipment.
- The transistor stage can heat quickly and needs properly sized thermal management.
- Battery runtime varies significantly with recycled-cell health and actual load.
- Lithium-ion cells require a suitable BMS, cell matching, fusing, insulation, and controlled charging.
- Mains-referenced work requires isolation, safe probing, enclosure, and qualified supervision.

## Documentation

See [`TECHNICAL-SUMMARY.md`](TECHNICAL-SUMMARY.md) for a concise source-grounded summary of the report.