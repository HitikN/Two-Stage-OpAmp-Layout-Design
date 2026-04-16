# Layout Versus Schematic (LVS) Verification

## Overview

This folder contains the LVS (Layout Versus Schematic) verification results for the two-stage CMOS operational amplifier designed using Cadence Virtuoso.

LVS verification ensures that the physical layout implementation matches the schematic design in terms of device connectivity, device sizes, and net connections.

This step confirms that the fabricated layout will function identically to the schematic design.

---

## Objective of LVS

The main objectives of LVS verification are:

- Verify connectivity between layout and schematic
- Ensure correct transistor sizes (W/L)
- Confirm correct device count
- Validate net connections
- Identify missing or extra devices
- Detect incorrect pin connections

---

## LVS Tool Used

LVS verification was performed using:

- Cadence Virtuoso LVS Tool
- Assura / Calibre (based on technology setup)

---

## LVS Procedure

The following steps were performed during LVS verification:

1. Extracted netlist generated from layout
2. Schematic netlist used as reference
3. Device comparison performed
4. Net connectivity verified
5. Errors identified and corrected
6. LVS re-run until match achieved

---

## Initial LVS Errors (If Any)

During initial LVS runs, mismatches were observed due to:

- Missing well taps (NTAP/PTAP)
- Incorrect substrate connections
- Net mismatches between layout and schematic
- Improper device connections

These issues were corrected through layout modification.

---

## Final LVS Status

LVS Result: MATCHED  
Number of Errors: 0  
Number of Warnings: (update if needed)

This confirms that the layout is electrically equivalent to the schematic.

---

## Files Included

- lvs_report_matched.png
- lvs_log.txt
- lvs_summary.png

These files show the final LVS matched status.

---

## Key Observations

After correcting layout issues and adding required taps and connections, the LVS verification successfully matched the schematic netlist.

This confirms correct implementation of:

- Differential input stage
- Current mirror load
- Second gain stage
- Compensation network
- Bias circuitry

---

## Importance of LVS

LVS verification is a critical step before fabrication or post-layout simulation.

Without LVS verification:

- Circuit may not function correctly
- Layout errors may remain undetected
- Post-layout simulation may produce incorrect results

---

## Next Step After LVS

After successful LVS matching, parasitic extraction (PEX) was performed to evaluate layout parasitic effects on circuit performance.
