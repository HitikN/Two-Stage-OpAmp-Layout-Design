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


# 🛠️ Design Rule Check (DRC) Report

## 📌 Overview

During the layout development of the **two-stage CMOS Operational Amplifier (Op-Amp)**, multiple Design Rule Check (DRC) violations were encountered and resolved.  

DRC ensures that the layout follows all **fabrication technology rules**, which is essential before manufacturing the circuit.

All errors were carefully analyzed and corrected to achieve a **clean DRC result**.

---

# 🚨 Common Types of DRC Errors Observed

The following DRC violations were observed and corrected during the layout process.

---

## 1️⃣ Metal Spacing Violations

📖 **Description:**  
Metal spacing violations occur when the distance between two metal layers is smaller than the minimum spacing defined by the technology rules.

🔧 **Fix Applied:**  
- Increased spacing between metal routing lines  
- Repositioned metal paths to maintain safe separation  
- Ensured spacing follows technology design rules  

✅ **Status:** Resolved

---

## 2️⃣ Minimum Width Violations

📖 **Description:**  
Minimum width violations occur when the width of metal or polysilicon lines is smaller than the required minimum value.

🔧 **Fix Applied:**  
- Increased width of metal tracks  
- Adjusted polysilicon dimensions  
- Verified width using layout measurement tools  

✅ **Status:** Resolved

---

## 3️⃣ Contact Enclosure Violations

📖 **Description:**  
Contact enclosure violations occur when contacts (vias) are not fully covered by surrounding metal layers.

🔧 **Fix Applied:**  
- Extended metal layers around contacts  
- Ensured proper enclosure margins  
- Verified enclosure rules using DRC tool  

✅ **Status:** Resolved

---

## 4️⃣ Minimum Area Violations

📖 **Description:**  
Minimum area violations occur when the total area of a layout shape is smaller than the required minimum allowed area.

🔧 **Fix Applied:**  
- Increased metal patch size  
- Adjusted layout geometry  
- Verified area compliance  

✅ **Status:** Resolved

---

## 5️⃣ Well Tap Violations (NTAP / PTAP)

📖 **Description:**  
Well tap violations occur when proper substrate connections are missing.

NTAP connects **N-well → VDD**  
PTAP connects **P-substrate → GND**

🔧 **Fix Applied:**  
- Added NTAP and PTAP structures  
- Connected taps to supply rails  
- Ensured proper spacing between taps  

✅ **Status:** Resolved

---

# 🧪 Final DRC Status

After correcting all violations, the layout successfully passed DRC verification.

🎯 **DRC Result:** CLEAN  
❌ **Number of Errors:** 0  
⚠️ **Number of Warnings:** 0  

---

# 🏁 Conclusion

Passing DRC confirms that the layout satisfies all **fabrication design rules** and is ready for the next verification stage.

➡️ **Next Step:** Layout Versus Schematic (LVS) Verification
