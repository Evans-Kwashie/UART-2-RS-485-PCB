# UART to RS-485 Converter Board

A 2-layer PCB that converts UART (TTL logic level) to RS-485 differential 
signaling, designed and routed from scratch in KiCad as a self-directed 
learning project focused on differential pair fundamentals.

## Overview

RS-485 is widely used in industrial automation, building automation, and 
long-distance serial communication where noise immunity and cable length 
matter more than raw speed. This board bridges a standard UART interface 
(TX/RX) to an RS-485 A/B differential bus using the STR485 transceiver.

## Key Design Features

- **STR485 transceiver** with DE/RE tied together and driven from a single 
  control pin for half-duplex direction switching
- **120Ω termination resistor** on the A/B bus, placed at the board's output
- **TVS diode protection** on the bus lines for ESD/surge resistance
- **Differential pair routing** for the A/B signal traces
- Standard decoupling (100nF) on the transceiver's VCC pin

## Design Challenges Solved

- Diagnosed and resolved a **thermal relief spoke count DRC error** on 
  fine-pitch pads by adjusting zone connection settings
- Worked through a **hole clearance violation** on the connector's 
  mechanical mounting holes, evaluating fab tolerance vs. board rules
- Learned and applied **differential pair routing concepts**: controlled 
  spacing, length matching, and why they matter for signal integrity at 
  higher speeds

## Files

- `.kicad_sch` / `.kicad_pcb` — full KiCad source project
- `RS 485.pdf` — schematic export
- `board_3d_render.png` — 3D rendered preview

## Tools

Designed entirely in KiCad 10.

## Status

Schematic and layout complete, DRC clean. Not yet fabricated/assembled.
