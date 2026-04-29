🛡️ Adapter Standard: Z-Axis & Mechanical Requirements
This document defines the physical interface and Z-axis precision standards between the V16-HIVE Mainboard and the Honeycomb Adapters. Failure to comply with these specifications will lead to contact issues or signal degradation. Any module violating these rules is not recognized as an official V16-HIVE component.

1. Connector Mounting & Orientation
[Mandatory] The 40-Pin Male (Plug) BTB connector must be mounted on the Bottom Side of the adapter PCB.

This ensures the chipset faces upward (Top Side) when stacked onto the mainboard, allowing for heat dissipation and accessibility.

Connector Specification: 0.5mm Pitch 40-Pin Plug (Selected height must be compatible with the 4.0mm stacking rule).

2. Stacking Height & Spacers
Standard Height: The vertical gap between the Mainboard PCB surface and the Adapter PCB bottom surface is fixed at 4.0mm.

Spacer Requirement: To ensure mechanical stability, 4.0mm precision standoffs (Nylon or Brass) must be installed at the designated mounting points.

Tolerance: The vertical deviation must be kept within ±0.1mm. Exceeding this tolerance may result in structural stress or damage to the BTB connector pins.

3. Component Height Constraints
Top Side: The total height of components (Chipsets, Capacitors, Heatsinks) mounted on the top side should not exceed 15.0mm to prevent interference with external enclosures.

Bottom Side: No components other than the BTB connector are allowed on the bottom side. This is to avoid physical collisions with the Mainboard's onboard components.

4. Alignment & Physical Dimensions
The center of the hexagonal adapter must align perfectly with the center of the 40-pin connector on the Mainboard.

Precision Cutting: CNC or Laser cutting is highly recommended for the PCB outline. The dimension tolerance for the hexagonal shape is ±0.2mm.
