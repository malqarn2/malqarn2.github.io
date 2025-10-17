---
title: Component Selection – H-Bridge Drivers
---

# H-Bridge Motor Driver Subsystem

> Provide a bidirectional driver for a brushed DC motor with integrated protection and simple MCU control.

## Requirements
- Motor supply: 4.5–48 V acceptable, target ~12–24 V
- Peak motor current: ≥ 3 A
- Built-in protections (OCP/OTP/UVLO)
- Simple MCU control (PH/EN or IN/IN PWM)
- Small SMT package preferred

---

## Options

### 1) Texas Instruments **DRV8876** – 40 V, 3.5 A H-bridge motor driver
![DRV8876](<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/d799f996-9aaf-4787-9717-c21b7f43603b" />
)
- **Unit cost:** \$1.90
- **Link to product:** [Digi-Key highlight page](https://www.digikey.com/en/product-highlight/t/texas-instruments/drv8876-h-bridge-motor-driver)  
  [Digi-Key part page (DRV8876PWPR)](https://www.digikey.com/en/products/detail/texas-instruments/DRV8876PWPR/10270191)
- **Key specs:**
  - Operating VSUP: **4.5–37 V**
  - Peak output current: **up to ~3.5 A**
  - Integrated current sensing/regulation, proportional current output (IPROPI)
  - Protections: overcurrent, thermal, undervoltage

| Pros | Cons |
|---|---|
| Wide supply range for many motors | 16-pin HTSSOP package is larger than 8-pin options |
| Built-in current sense/regulation reduces external parts | ~3.5 A peak: check thermal/electrical headroom for your load |
| Multiple input modes (PH/EN, IN/IN, half-bridge) | Layout care still needed for heat/current paths |

---

### 2) Texas Instruments **DRV8251 / DRV8251A** – 48–50 V, 4.1 A H-bridge motor driver
![DRV8251](./assets/ctx936tr_nd_oscillator.png)
- **Unit cost:** \$2.09 
- **Link to product:** [Digi-Key highlight page](https://www.digikey.com/en/product-highlight/t/texas-instruments/drv8251-a-48v-h-bridge-motor-drivers)
- **Key specs:**
  - Operating VSUP: **4.5–48 V** (family up to 50 V per TI datasheet)
  - Peak output current: **~4.1 A**
  - Charge pump for N-MOS H-bridge, **current regulation**; **A-variant** adds current-sense feedback
  - Protections: overcurrent, thermal; low-power sleep

| Pros | Cons |
|---|---|
| Higher voltage headroom (good for 24–48 V systems) | Slightly more complex configuration (IPROPI/ISEN, current regulation) |
| Strong protection features and stall/load feedback | Cost may be higher vs simpler drivers |
| 8-pin option available in the family for compact designs | Careful layout/thermal vias recommended for higher currents |

---

## Choice
**DRV8251A** (if your system voltage is ≥ 24 V or you want current-sense feedback)  
**DRV8876** (if your system is ≤ 24–36 V and you want a proven, flexible driver with integrated current regulation)

## Rationale
Both devices meet the bidirectional control requirement and integrate protections. **DRV8251A** offers higher voltage capability and built-in current feedback for diagnostics/stall detection, making it better for **24–48 V** systems. **DRV8876** is ideal for **4.5–37 V** designs where an integrated current regulation loop and flexible control modes simplify firmware and reduce external parts.
