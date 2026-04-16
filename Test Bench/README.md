# Testbench Design for Two-Stage CMOS Op-Amp

## Overview

This folder contains the testbench configurations used to evaluate the performance of the two-stage CMOS operational amplifier designed using Cadence Virtuoso.

The testbench is used to verify the functionality and performance of the Op-Amp at both schematic (pre-layout) and extracted (post-layout) levels.

---

## Testbench Objectives

The main objectives of the testbench are:

- Verify correct circuit biasing
- Measure open-loop gain
- Evaluate frequency response
- Determine phase margin
- Analyze the effect of layout parasitics
- Compare pre-layout and post-layout performance

---

## Testbench Configuration

The Op-Amp is tested using a differential input configuration.

### Components Used

The testbench includes:

- Differential AC input source
- DC supply voltage (VDD)
- Ground reference (GND)
- Load capacitance (CL)
- Output measurement node
- Bias connections

### Supply Conditions

Supply Voltage (VDD): 1.8 V  
Ground: 0 V  

### Load Conditions

Load Capacitance (CL): 1 pF (or your value)

---

## Pre-Layout Testbench

The pre-layout testbench uses the schematic view of the operational amplifier.

### Purpose

- Verify schematic-level performance
- Measure initial gain and frequency response
- Validate circuit functionality before layout design

### Expected Performance

Open-loop Gain ≈ 55 dB (Pre-layout)

### File Included

- testbench_pre_layout.png

---

## Post-Layout Testbench

The post-layout testbench uses the extracted (PEX) view of the operational amplifier.

### Purpose

- Analyze the effect of parasitic resistance and capacitance
- Evaluate real layout performance
- Compare results with schematic simulation

### Observed Performance

Open-loop Gain ≈ 25 dB (Post-layout)

The reduction in gain is mainly due to parasitic effects introduced during layout.

### File Included

- testbench_post_layout.png

---

## AC Analysis Setup

AC sweep analysis is performed to obtain the frequency response of the Op-Amp.

### Parameters

AC Input Magnitude: 1 V  
Frequency Sweep Range: (e.g., 1 Hz to 1 GHz — update if needed)

### Outputs Measured

- Open-loop gain
- Phase response
- Unity gain bandwidth
- Phase margin

---

## DC Operating Point Analysis

DC analysis is used to verify:

- Bias currents
- Node voltages
- Transistor operating regions

This ensures proper circuit operation before AC analysis.

---

## Transient Analysis (Optional)

If transient analysis is performed:

- Step input signal applied
- Output response observed
- Slew rate measured

---

## Tools Used

- Cadence Virtuoso
- Spectre Simulator

---

## Notes

The same testbench structure is used for both schematic and post-layout simulations to ensure accurate performance comparison.
