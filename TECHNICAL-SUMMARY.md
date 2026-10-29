# Technical summary

## Topology and operating principle

The project report describes a low-power automatic inverter using 220/12 V center-tapped transformers, a rectifier-and-capacitor filtering stage, a relay for grid/battery transfer, a TTC5200 transistor switching stage, and a nominal 220 V AC output. The report refers to bridge rectification and inverter switching in several sections; it does not provide enough unambiguous evidence here to label the design a strict half-bridge.

When grid power is present, the low-voltage path is rectified and filtered for battery charging. When the grid is unavailable, the relay changes state and the battery supplies the transistor stage, with the transformer used to produce AC for small loads.

## Reported components

Two 12 V 2 A transformers; 12 V relay; TTC5200; 1 kΩ resistor; 1 µF/63 V and 2200 µF/16 V capacitors; two 1N5408 diodes; one 1N4007 diode; junction box; and a 12-cell 18650 pack described as 3S4P.

## Simulation and expected performance

The report mentions CircuitLab, Tinkercad, EasyEDA, and Proteus. It reports approximately 24 W at 220 V AC in simulation, with aquarium air pumps and lighting as intended low-power loads. It estimates up to approximately five hours of backup under stated conditions, but runtime depends on cell health, state of charge, conversion losses, and load.

## Limitations and safety

The report notes a non-pure-sine output, fast heating in the TTC5200 stage, and inability to power high-power appliances. The prototype should not be treated as a certified product. High-voltage AC and lithium-ion batteries can cause fatal shock, fire, or explosion. Any reproduction requires qualified supervision, isolation, fusing, a suitable BMS, cell matching, enclosure, thermal design, and verified measurements.

## Omitted information

Personal addresses, student IDs, signatures, administrative details, and other personal information from the source report are intentionally omitted from this public repository.