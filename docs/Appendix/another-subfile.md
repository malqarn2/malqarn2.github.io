---
title: Appendix - Another Subfile
---

# Appendix – Supporting Calculations

## A. Power Budget Summary

### 5V Power Rail

| Component | Max Current (mA) | Voltage (V) | Power (mW) |
|----------|------------------|-------------|------------|
| PIC18F57Q43 Curiosity Nano | 120 | 5 | 600 |
| Push-Pull Amplifier (2N3904/2N3906) | 200 | 5 | 1000 |
| Status LED + Resistor | 15 | 5 | 75 |
| Subtotal | **335 mA** |  | **1675 mW** |
| Safety Margin (25%) | **83.75 mA** |  |  |
| **Total Required** | **418.75 mA** |  |  |

### External Supply
- Wall Adapter: **9V, 800 mA**
- Required Current: **418.75 mA**
- Remaining Capacity: **381 mA**

✅ Supply is sufficient.

---

## B. Regulator Verification

- Regulator: **LM7805**
- Rated Output: **1A**
- Required Output: **418.75 mA**

✅ Regulator operates safely within limits.

---

## C. Design Assumptions

1. Speaker is driven from a 5V AC-coupled amplifier.
2. MCU maximum operating current is 120 mA.
3. LED is limited to 15 mA with a 100Ω resistor.
4. Safety margin of 25% is applied to all rails.


