# title
Component Selection – DC Motor

# DC Motor Subsystem

Provide the mechanical output source for the AutoCan system by selecting a brushed DC gearmotor compatible with the chosen H-bridge driver and system voltage.

---

## Requirements
- **Operating voltage:** 6 – 12 V (nominal 12 V)
- **Continuous current:** ≤ 3 A (DRV8876 class driver)
- **Peak current:** ≤ 4 A (DRV8251/DRV8876)
- **Direction control:** bidirectional (H-bridge)
- **Torque and speed:** sufficient to open a ~2 lb trash-lid (~400 oz-in torque, 10–30 rpm)
- **Mounting:** geared output shaft or worm-gear drive recommended

---

## Options

### 1) **DFRobot FIT0492-A Micro DC Gearmotor – 12 V, 50 RPM**
![Image](https://github.com/user-attachments/assets/1115248f-c77d-4318-84ff-1bb2fac5dd24)

**Link:** [Digi-Key Product Page](https://www.digikey.com/en/products/detail/dfrobot/FIT0492-A/7087165)

| Spec | Value |
|------|-------|
| Rated Voltage | 12 V DC |
| No-Load Speed | ~50 RPM |
| Rated Torque | ~9 kg·cm (≈ 125 oz-in ≈ 0.88 N·m) |
| Stall Torque | ~50 kg·cm (≈ 695 oz-in ≈ 4.8 N·m) |
| Gear Ratio | 100 : 1 |
| Shaft | 6 mm D-shaft |
| Body Size | Ø 37 mm × 60 mm |
| Unit Cost | ≈ $14.95 |

**Pros**
- Compact all-metal gearbox  
- Sufficient stall torque for light–medium mechanical loads  
- Operates directly on 12 V, easy to drive with DRV887x H-bridges  

**Cons**
- Rated torque slightly below the 2 lb-lid requirement (stall torque barely sufficient)  
- Not self-locking – lid may back-drive without brake or spring assist  
- Continuous duty torque may overheat under heavy load  

---

### 2) **ISL Products MOT-KM-NJSC-12-A – 5 V, 106 RPM**
<img width="200" height="200" alt="Image" src="https://github.com/user-attachments/assets/25be54c0-38a7-4d61-a732-7a865e7240a5" />

**Link:** [Digi-Key Product Page](https://www.digikey.com/en/products/detail/isl-products-international/MOT-KM-NJSC-12-A/15283282)

| Spec | Value |
|------|-------|
| Rated Voltage | 5 V DC |
| No-Load Speed | ~106 RPM |
| Rated Torque | 3.47 oz-in (≈ 0.025 N·m) |
| Max (Momentary) Torque | 8.99 oz-in (≈ 0.064 N·m) |
| Shaft | 3 mm round |
| Body Size | Ø 12 mm × 25 mm |
| Gear Type | Spur gear |
| Unit Cost | ≈ $305.46 |

**Pros**
- Miniature, lightweight  
- Low-voltage operation (5 V logic-level friendly)  

**Cons**
- **Extremely low torque** — over 100× weaker than required  
- Not suitable for lifting or high-load mechanisms  
- High cost for its performance  

---

## Choice

| Use Case | Recommended Motor | Compatible Driver |
|-----------|------------------|-------------------|
| Prototype / Low torque demo | DFRobot FIT0492-A | DRV8876 / DRV8251 |
| Full-scale lid actuator (~2 lb lid) | Higher-torque 12 V worm-gear motor (≥ 400 oz-in, 10–30 rpm) | DRV8876 / DRV8251 |

---

## Rationale
- The **FIT0492-A** offers moderate torque and simplicity but lacks self-locking and continuous duty capacity.  
- The **MOT-KM-NJSC-12-A** is far too small for the load requirement.  
- A **12 V worm-gear drive** around **400–700 oz-in torque** remains the practical choice for a 2 lb lid.
