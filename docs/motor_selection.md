# MTM Gimbal System Redevelopment Project

![MTM Tool Axis](resources/mtm_tool_axis.png)

## Gimbal Overview

The system consists of the following joints from the original MTM:
*   **Joint 4:** Setup Joint (Platform)
*   **Joint 5:** Wrist Pitch
*   **Joint 6:** Wrist Yaw
*   **Joint 7:** Wrist Roll
*   **Joint 8:** Finger Grips

---

## Current System Specification (Based on Original MTM)

Of course. Here is the data organized into a table with the requested calculated columns for " CPR" and "Max. Output Torque".

### Motor Specifications Table

| Axis | Motor Type | Max. Continuous Torque (Nm) | Torque Constant (Nm/A) | Gear Ratio | Encoder CPR (at Motor) |  CPR (at Output)¹ | Max. Output Torque (Nm)² |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Platform** | RE025-055-38 | 0.0403 | 0.043800 | 10.53 | 4000 | 42,120 | 0.424 |
| **Wrist Pitch** | RE013-032-06 | 0.0047 | 0.004950 | 33.16 | 64 | 2,122 | 0.156 |
| **Wrist Yaw** | RE013-032-06 | 0.0029 | 0.004950 | 33.16 | 64 | 2,122 | 0.096 |
| **Wrist Roll** | RE013-020-08 | 0.0014 | 0.003390 | 16.58 | 64 | 1,061 | 0.023 |

Of course. Here is the comprehensive table that combines all the previous information, directly comparing the original Maxon geared systems with the proposed CubeMars direct-drive replacements for each axis.

### Comprehensive Motor Comparison: Maxon (Geared) vs. CubeMars (Direct Drive)

Understood. I have revised the table to remove the "Key Characteristics" column and have researched and added the nominal voltage and peak/stall current specifications for each motor system.

### Comprehensive Motor Comparison: Maxon (Geared) vs. CubeMars (Direct Drive)

| Axis | System Type | Motor / Model | Nominal Voltage (V)⁴ | Peak/Stall Current (A)³ | Gear Ratio | Peak / Max. Output Torque (Nm)¹ | Est. Dimensions (mm)² | Encoder / Resolution |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Platform** | Maxon + Gearbox | RE025-055-38 | 24 | ~2.8 | **10.53 : 1** | 0.424 | Ø26 x 89 | 4000 CPR -> **42,120** effective CPR |
| **Wrist Pitch**| Maxon + Gearbox | RE013-032-06 | 9 | ~1.3 | **33.16 : 1** | 0.156 | Ø13 x 56.3 | 64 CPR -> **2,122** effective CPR |
| **Wrist Yaw** | Maxon + Gearbox | RE013-032-06 | 9 | ~1.3 | **33.16 : 1** | 0.096 | Ø13 x 56.3 | 64 CPR -> **2,122** effective CPR |
| **Wrist Roll** | Maxon + Gearbox | RE013-020-08 | 6 | ~0.9 | **16.58 : 1** | 0.023 | Ø13 x 40.1 | 64 CPR -> **1,061** effective CPR |
| | | | | | | | | |
| **Platform** | CubeMars Direct Drive | **GL40** | 12 - 24 | 2.1 | **1 : 1** | 0.450 | Ø46 x 20.5 | Integrated Hall Sensors |
| **Wrist Pitch**| CubeMars Direct Drive | **GL35** | 12 - 24 | 1.5 | **1 : 1** | 0.200 | Ø40.8 x 17.5 | Integrated Hall Sensors |
| **Wrist Yaw** | CubeMars Direct Drive | **GL28** | 12 | 1.1 | **1 : 1** | 0.100 | Ø33.6 x 15.8 | Integrated Hall Sensors |
| **Wrist Roll** | CubeMars Direct Drive | **GL25** | 8.4 (2S) | 0.9 | **1 : 1** | ~0.040 | Ø30 x 12.5 | Integrated Hall Sensors |

---
#### **Footnotes & Explanations:**

¹ **Peak / Max. Output Torque (Nm):**
*   **Maxon:** Value is a theoretical calculation (*Max. Continuous Torque x Gear Ratio*). It's an ideal figure that does not account for gearbox efficiency losses.
*   **CubeMars:** Value is the motor's specified **Peak Torque** from its datasheet, representing the maximum dynamic output.

² **Estimated Dimensions (mm):**
*   **Maxon:** Dimensions are estimated by combining the motor and a compatible planetary gearbox. The actual size may vary.
*   **CubeMars:** Dimensions are from official datasheets.

³ **Peak/Stall Current (A):**
*   **Maxon:** This is the **Stall Current**—the theoretical current drawn at zero speed and nominal voltage. It represents the absolute maximum current draw.
*   **CubeMars:** This is the **Peak Current** as specified by the manufacturer, which is the recommended maximum current for short-duration dynamic movements.

⁴ **Nominal Voltage (V):**
*   **Maxon:** The voltage listed is the **Nominal Voltage** for that specific motor winding.
*   **CubeMars:** The voltage listed is the typical or recommended **operating range** (e.g., compatible with 4S-6S LiPo batteries).
-----
### Prompts
give me consice answers to these questions for my application , i call it MTM master tool manupilator

we are creating robotic surgery application in which we need MTM with 7 joints with last 4 joints as gimbal and first 3 are  for axis



now for last three we are plannign to use geears but lets focus on gimbal system


confusion is for gimbal with bldc can we go without  gearss and have smooth experience for sugeon ,
features wen eed
 ( small to mediam size ) ,
- when moving it should be water smooth ,
- when left free it should be holding position
- when we turn on it should get to a specific intial position and hold state ,

surgeon experience is the most important thing

in this context


- simple english explanatino  for inertia , reflective enrtia , ggravity compensation , frictions for gear vs non geared motors

and simple features worflows , seprtate for each