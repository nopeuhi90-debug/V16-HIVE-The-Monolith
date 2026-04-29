🔋 Adapter Standard: Power Injection & Filtering
This document establishes the rigid framework for feeding the V16-HIVE audio matrix without sonic compromise. In high-fidelity audio, power is the foundation of sound; therefore, any fluctuation or noise in the power delivery system is strictly prohibited.

1. Plane-to-Pin Topology
[Mandatory] Traditional thin traces for main power rails are forbidden. All adapters must utilize L5 Internal Power Planes to deliver current.

Low Impedance Path: Use oversized vias (0.4mm or larger) to connect the power plane directly to the chipset pins. This minimizes resistive bottlenecks and thermal noise.

Star-Point Connection: Power must enter the adapter through a single star-point at the BTB connector to prevent ground loops and unintended return paths.

2. Capacitance Hierarchy (Filtering Strategy)
To ensure absolute DC stability, a three-stage decoupling hierarchy must be implemented:

Bulk Filtering: 47uF to 100uF Low-ESR Tantalum or Polymer capacitors at the board entrance to absorb low-frequency transients.

Local Buffering: 10uF X7R Ceramic capacitors for each IC rail branch, placed within 5mm of the chipset power entry pins.

HF Decoupling: 0.1uF C0G/NP0 capacitors for high-frequency noise suppression, placed directly on the landing pads of the chipset.

3. IR Drop & Thermal Stability
Copper Weight: A minimum of 2oz (70µm) copper weight is required for Power and Ground planes to minimize IR Drop ($V=I \times R$).

Voltage Tolerance: Under full-scale operation, the voltage sagging at the DAC/Chipset core must not exceed 0.5% of the nominal voltage.

Via Stitching: Multiple parallel vias must be used to act as high-bandwidth conduits, ensuring current spikes do not cause momentary voltage dips.

4. Ground Return & Isolation
Solid Return Path: The L2 GND plane must remain solid and uninterrupted beneath all high-speed power rails to ensure a zero-current loop area.

Digital/Analog Separation: Analog power rails must be physically isolated from digital switching noise using Ferrite Beads or dedicated LDOs (Low-Dropout Regulators) with high PSRR.
