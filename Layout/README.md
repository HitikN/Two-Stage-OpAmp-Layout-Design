# Layout Design of Two-Stage CMOS Op-Amp

## Overview

This folder contains the physical layout implementation of the two-stage CMOS operational amplifier designed using Cadence Virtuoso.

The layout was created based on the schematic design and optimized to satisfy design rule constraints, ensure proper matching, and minimize parasitic effects.

The layout verification includes DRC and LVS validation before performing parasitic extraction (PEX).

---

## Layout Objectives

The main objectives of the layout design are:

- Implement schematic at physical level
- Maintain transistor matching
- Reduce parasitic capacitance
- Ensure proper routing
- Satisfy technology design rules
- Achieve LVS matching with schematic

---

## Layout Structure

The layout consists of the following major blocks:

### Differential Input Stage

- Matched NMOS differential pair
- Symmetrical placement for improved matching
- Common centroid structure (if used)

### Current Mirror Load

- PMOS current mirror implemented with matched geometry
- Proper routing to maintain symmetry

### Second Gain Stage

- NMOS transistor used as common-source amplifier
- Proper output routing for load connection

### Compensation Capacitor

- Miller compensation capacitor placed close to amplifier stages
- Routing optimized to reduce parasitic resistance

### Bias Circuit

- Bias transistors placed with proper spacing
- Connected to reference nodes

---

## Layout Techniques Used

The following layout techniques were applied:

- Symmetrical placement of matched devices
- Common centroid placement (if applicable)
- Use of multi-finger transistors
- Short routing paths
- Proper metal layer usage
- Guard ring implementation (if used)
- Well tap placement (NTAP/PTAP)

---

## Design Rule Check (DRC)

DRC was performed to verify that the layout satisfies all fabrication design rules.

Status:

DRC Result: Clean  
Number of Errors: 0  

### File Included

- layout_drc_clean.png

---

## Layout Versus Schematic (LVS)

LVS was performed to ensure that the layout matches the schematic connectivity.

Status:

LVS Result: Matched  

### File Included

- layout_lvs_matched.png

---

## Layout Dimensions

(You can update this if known)

Layout Area: (enter value)  
Technology Node: 180 nm CMOS (or your node)

---

## Layout Screenshot

The layout image shows the full physical implementation of the operational amplifier including routing, transistor placement, and interconnects.

### File Included

- opamp_layout.png

---

## Tools Used

- Cadence Virtuoso Layout Editor
- Assura / Calibre (for DRC & LVS verification)

---

## Notes

The layout is designed to maintain matching between critical devices and minimize parasitic effects that may degrade performance.

After DRC and LVS verification, parasitic extraction (PEX) was performed for post-layout simulation.
