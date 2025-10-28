# title
Component Selection — DC Motor

# DC Motor Subsystem

Provide the mechanical output source for the AutoCan system by selecting a brushed DC gearmotor compatible with the chosen H-bridge driver and system voltage.

---

## Requirements

- **Operating voltage:** 6 – 9 V (nominal system = 9 V)
- **Continuous current:** ≤ 0.6 A (for L293D) or ≤ 3 A (for DRV8876)
- **Peak current:** ≤ 1 A (L293D) or ≤ 4 A (DRV8251/DRV8876)
- **Direction control:** bidirectional (H-bridge)
- **Form factor:** geared output shaft suitable for wheel coupling
- **Torque and speed:** sufficient to move lightweight chassis at 0.2 – 0.5 m/s
- **Mounting:** standard N20 or 37D form factor preferred

---

## Options

### 1) **Pololu 6 V N20 Metal Gearmotor – 200 RPM**
![Image](https://github.com/user-attachments/assets/38d7421e-bded-48c6-aa15-32e4b55f6008)

**Link:** [Digi-Key Product Page](https://www.digikey.com/en/products/detail/pololu/1093/7398781)

| Spec | Value |
|------|-------|
| Rated Voltage | 6 V DC |
| No-Load Speed | ~200 RPM |
| Stall Current | ~0.36 A |
| Stall Torque | ~0.03 N·m |
| Shaft | 3 mm D-shaft |
| Body Size | 12 × 10 × 26 mm |
| Gear Ratio | 30 : 1 |
| Unit Cost | ≈ $8.95 |

**Pros**
- Compact and light — ideal for small mobile robots  
- Compatible with **L293D** current limit (< 600 mA typical)  
- Many gear ratios available for tuning torque/speed  
- Works well on 5 – 9 V with PWM control  

**Cons**
- Limited torque for heavier robots  
- Shaft diameter small (needs hub adapter)  
- May heat up under stall conditions  

---

### 2) **Pololu 12 V 37D Metal Gearmotor – 100 RPM**
![Image](https://github.com/user-attachments/assets/929337e2-214e-4181-be0c-331c29a8daed)

**Link:** [Digi-Key Product Page](https://www.digikey.com/en/products/detail/pololu/1103/7398787)

| Spec | Value |
|------|-------|
| Rated Voltage | 12 V DC |
| No-Load Speed | ~100 RPM |
| Stall Current | ~3.5 A |
| Stall Torque | ~1.1 N·m |
| Shaft | 6 mm D-shaft |
| Body Size | Ø 37 mm × 63 mm |
| Gear Ratio | 100 : 1 |
| Unit Cost | ≈ $24.95 |

**Pros**
- High torque output — suitable for heavier chassis  
- Robust all-metal gearbox and bearings  
- Compatible with **DRV8876 / DRV8251** drivers (3 – 4 A peak)  
- Long service life under PWM control  

**Cons**
- Too powerful for **L293D** (will exceed current rating)  
- Larger physical size and higher cost  
- Needs stronger mounting and wiring  

---

## Choice

| Use Case | Recommended Motor | Compatible Driver |
|-----------|-------------------|-------------------|
| Low-power, educational prototype | **Pololu N20 6 V (200 RPM)** | L293D |
| Higher-power or production build | **Pololu 37D 12 V (100 RPM)** | DRV8876 / DRV8251 |

**If using L293D:** Stay below 0.6 A stall — the N20 motor is ideal.  
**If upgrading driver:** Use the 37D motor for more torque and load capacity.

---

## Rationale

Both motors meet the system’s bidirectional drive requirement but serve different scales:

- The **6 V N20** is efficient and matches the current limits of the **L293D**, making it perfect for small prototypes or lightweight autonomous systems.  
- The **12 V 37D** pairs naturally with **modern MOSFET H-bridge drivers (DRV8876/DRV8251)**, providing several times more torque and mechanical robustness for larger builds.  

Selecting between them depends on driver capability, chassis mass, and desired acceleration.

---
