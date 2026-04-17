# Design Rule Check (DRC) Verification

## Overview

This folder contains the Design Rule Check (DRC) verification results for the layout of a two-stage CMOS operational amplifier designed using Cadence Virtuoso.

DRC verification ensures that the physical layout follows all fabrication technology design rules such as spacing, width, enclosure, and overlap constraints.

Passing DRC confirms that the layout is manufacturable according to the specified CMOS technology rules.

---

## Objective of DRC

The main objectives of performing DRC are:

- Verify layout rule compliance
- Check minimum spacing between devices
- Validate metal width and enclosure rules
- Ensure proper well and substrate connections
- Identify layout violations
- Prepare layout for LVS verification

---

## Tool Used

DRC verification was performed using:

- Cadence Virtuoso Layout Editor
- Assura / Calibre DRC Tool (based on technology)

---

## Initial DRC Errors (During Development)

During initial layout design, several DRC violations were observed due to:

- Metal spacing violations
- Incorrect enclosure rules
- Minimum width violations
- Missing well tap placement
- Overlapping layout layers

These errors were corrected by adjusting layout geometry, improving routing, and adding required substrate taps.

---

## Final DRC Status

DRC Result: CLEAN  
Number of Errors: 0  
Number of Warnings: (update if applicable)

This confirms that the layout satisfies all required fabrication rules.

---

## Files Included

The following files are included in this folder:

- drc_clean_report.png
- drc_error_fix_log.txt (optional)
- drc_summary.png

These files show the final DRC verification results.

---

## DRC Fixing Techniques Used

The following corrective actions were applied to resolve DRC violations:

- Adjusted metal spacing
- Modified transistor placement
- Increased metal widths where required
- Corrected enclosure violations
- Added well taps (NTAP/PTAP)
- Improved routing alignment

These steps ensured compliance with all layout design rules.

---

## Importance of DRC

DRC is the first verification step in physical layout design.

Without successful DRC:

- Layout cannot proceed to LVS
- Fabrication may fail
- Device performance may be unreliable

Therefore, DRC-clean layout is mandatory before performing LVS verification.

---

## Next Step After DRC

After achieving a DRC-clean layout, Layout Versus Schematic (LVS) verification was performed to ensure electrical equivalence between schematic and layout.
