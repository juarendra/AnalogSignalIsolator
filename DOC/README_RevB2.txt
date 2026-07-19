HCNR201 Selectable Output Analog Isolator - Engineering Package Rev B2
========================================================================

FINAL POWER-INPUT CONFIGURATION
-------------------------------
5V_IN -> Q1 AO3401A -> FB1 -> YLPTEC IF0505S-1WR3

Q1 connections:
- Pin 3 / Drain  -> 5V_IN
- Pin 2 / Source -> 5V_PMOS / protected rail
- Pin 1 / Gate   -> RG 100 kOhm -> GND_HOST

FB1:
- Murata BLM18AG601SN1D, LCSC C19330
- 600 Ohm at 100 MHz class, 500 mA
- Placed after Q1 and before PS1 input capacitors
- 0 Ohm substitution is for validation only

NOT FITTED IN REV B2
--------------------
- PPTC / resettable input fuse
- Input TVS diode

SYSTEM ASSUMPTION
-----------------
The upstream 5 V source is regulated and current-limited. Rev B2 is primarily
intended for short or internal 5 V wiring, or for systems that provide surge
and overcurrent protection elsewhere.

ANALOG CONFIGURATION
--------------------
Input:
- Conditioned analog signal, 0-5 V

Output selector:
- MODE 24: 0-2.4 V
- MODE 33: 0-3.0 V
- MODE 50: 0-4.5 V

Core parts:
- U1/U2: Texas Instruments OPA317IDBVR, LCSC C2058367
- U3: Broadcom HCNR201-500E, LCSC C27465
- PS1: YLPTEC IF0505S-1WR3, LCSC C5369637
- Q1: UMW AO3401A, LCSC C347476
- SW1: SHOU HAN SK13D07VG5, LCSC C393948

PACKAGE CONTENTS
----------------
00 Block diagram: PDF, PNG, SVG
01 Requirements: PDF
02 Power/isolation schematic: PDF, PNG, SVG
03 HCNR201 analog schematic: PDF, PNG, SVG
04 Output mode and ADC interface: PDF, PNG, SVG
05 Connector wiring: PDF, PNG, SVG
06 BOM and calculations with LCSC part numbers: XLSX
07 PCB layout rules: PDF
08 Test and calibration procedure: PDF

REVISION
--------
Rev B2: PMOS + ferrite bead only; PPTC and input TVS removed.
