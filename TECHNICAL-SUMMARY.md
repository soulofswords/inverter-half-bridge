# Technical Summary

This summary is derived from the supplied project report and excludes student identifiers, contact details, signatures, home information, and other personal or administrative data.

## Purpose

The project is a portable, low-power backup inverter for aquarium aerators, aquarium lighting, and a small desk fan. It is described as a power inverter with automatic transfer between grid-derived charging and battery operation.

## Topology and power path

The report documents:

1. A 220/12 V center-tapped transformer arrangement.
2. Full-bridge rectification of the input AC.
3. Capacitor smoothing on the rectified low-voltage path.
4. A 12 V relay for switching between grid charging and the battery path.
5. A TTC5200 transistor stage driven from the battery.
6. A second transformer producing nominal 220 V AC.
7. A 12 × 18650 battery pack arranged as 3S4P.

The report contains half-bridge and bridge-related wording. Because the available description does not make the exact switching topology unambiguous, this summary avoids assigning a stricter topology name than the report supports.

## Listed components

- Two 12 V, 2 A transformers
- 12 V relay
- TTC5200 transistor
- 1 kΩ resistor
- 1 µF, 63 V capacitor
- 2200 µF, 16 V capacitor
- Two 1N5408 diodes
- One 1N4007 diode
- Junction box
- Twelve 18650 cells in a 3S4P arrangement

## Design decisions

The documented design choices are automatic grid/battery transfer, filtered rectification, and a battery charging approach intended to reduce overcharge risk. The project prioritizes portability and low-power backup use rather than general-purpose mains power.

## Simulation and reported results

The report references CircuitLab, Tinkercad, EasyEDA, and Proteus. Reported simulation and planning figures include:

- Approximately 24 W at 220 V AC
- Intended 5 W aquarium air-pump loads
- Intended 20–24 W lighting load
- 12.6 V, 8 A battery input
- Up to approximately five hours of runtime, depending on cell condition and load

The figures are report claims and should be reproduced with appropriate instrumentation before relying on the design.

## Limitations and prototype status

The report identifies a non-pure-sine output, TTC5200 heating, and thermal-performance concerns. It excludes televisions, refrigerators, irons, kettles, laptops, and other unsuitable loads. PCB and heatsink preparation are described, while drilling, mounting, and soldering remained to be completed at the time of the report.

## Safety

This is not a certified mains product. The output transformer and associated wiring may expose users to lethal voltage. Testing requires qualified supervision, guarded conductors, suitable fusing, insulation, an enclosed assembly, and correctly rated measurement equipment.

The 3S4P lithium-ion pack must use cells with compatible condition and specifications, suitable protection, and a charger designed for the pack configuration. Do not short, puncture, overcharge, reverse-connect, or operate damaged cells. Disconnect the battery before servicing the inverter.
