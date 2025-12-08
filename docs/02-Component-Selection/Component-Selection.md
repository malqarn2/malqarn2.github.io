# Component Selection – Speaker

## Speaker Subsystem

Provide the audible output source for the AutoCan system by selecting a miniature 8 Ω speaker compatible with the transistor amplifier and 5 V logic-level drive from the PIC18F57Q43.

---

### Requirements

- **Operating voltage:** driven from **5 V amplifier** supply  
- **Speaker impedance:** **8 Ω** (compatible with simple class-AB amplifier)  
- **Rated / max power:** **0.5 – 1 W**  
- **Frequency range:** at least **500 Hz – 5 kHz** (tone and alert signals clearly audible)  
- **Size / mounting:** small enough for enclosure, simple panel or PCB mounting  
- **Driver circuit:** discrete push-pull amplifier (Q1 = 2N3904, Q2 = 2N3906) with DC-blocking capacitor

These requirements come directly from the AutoCan product goals: a compact, low-power, clearly audible alert speaker that can be driven from a 5 V rail and simple transistor amplifier.

---

### Options

#### 1) FD3057 (Provided Kit Speaker) – 8 Ω, ~0.5 W

![Image](https://github.com/user-attachments/assets/62a0a08d-da1b-40d3-b357-e64e36efd5e0)

**Spec (from kit / typical values):**

| Spec                | Value                |
|---------------------|----------------------|
| Impedance           | 8 Ω                  |
| Rated Power         | 0.5 W                |
| Max Power           | ~1.0 W (short term)  |
| Resonant Frequency  | ~600 Hz              |
| SPL (0.5 W @ 0.2 m) | ~85 dB (estimated)   |
| Dimensions          | Ø36 mm × 10 mm       |
| Unit Cost           | Included in lab kit  |

**Pros**

- Already provided in the EGR 304 kit (zero extra cost)  
- Physically large cone → decent loudness for tones  
- Works directly with 5 V transistor amplifier (2N3904 / 2N3906)

**Cons**

- Limited datasheet information (approximate specs only)  
- Larger diameter requires more enclosure space  
- Unknown detailed frequency response

---

#### 2) CUI / Same Sky CDS-16098A – 8 Ω, 1 W Micro Speaker

![Image](https://github.com/user-attachments/assets/9f9d0cf8-ac5d-48bf-a0be-5eff4faa8c34) 


**Key Specs**

| Spec                | Value                      |
|---------------------|----------------------------|
| Rated / Max Power   | 0.7 W / 1.0 W              |
| Impedance           | 8 Ω                        |
| Resonant Frequency  | ~500 Hz                    |
| Frequency Range     | ~400 Hz – 20 kHz           |
| SPL                 | 86 dB (0.5 W @ 0.1 m)      |
| Dimensions          | 16 × 9 × 3 mm (rectangular)|
| Unit Cost           | ≈ \$2–3 (qty 1)            |

**Pros**

- Very small footprint – easy to fit in a compact AutoCan enclosure  
- Published, detailed datasheet and frequency response  
- 1 W power rating matches 5 V amplifier capability with headroom

**Cons**

- More difficult to prototype mechanically (needs enclosure / baffle)  
- Requires PCB or mechanical features for mounting  
- Slightly more expensive than lab-kit speaker

---

#### 3) PUI Audio AS02808MR-R – 8 Ω, 1 W Round Speaker

![Image](https://github.com/user-attachments/assets/8eebde07-e489-4ccf-99a1-5d67792779eb)


**Key Specs**

| Spec                | Value                        |
|---------------------|------------------------------|
| Rated / Max Power   | 1.0 W / 1.5 W                |
| Impedance           | 8 Ω                          |
| Resonant Frequency  | ~500 Hz                      |
| Frequency Range     | 500 Hz – 20 kHz              |
| SPL                 | 80 dB (1 W @ 1 m)            |
| Dimensions          | Ø28 mm round, low profile    |
| Unit Cost           | ≈ \$2–3 (qty 1)              |

**Pros**

- Round form factor similar to FD3057 → easy mechanical replacement  
- Fully specified datasheet (power, SPL, frequency response)  
- 1 W rating provides safe headroom for 5 V amplifier

**Cons**

- Slightly lower SPL than CDS-16098A at the test point  
- Requires purchase (not in the default lab kit)

---

### Other Major Components in the Speaker Subsystem

Although the **speaker** is the primary selected component, the subsystem also depends on several major parts that must be compatible with the chosen speaker:

| Component                    | Chosen Part      | Role in Subsystem                            |
|-----------------------------|------------------|----------------------------------------------|
| NPN transistor              | 2N3904           | High-side of push-pull amplifier             |
| PNP transistor              | 2N3906           | Low-side of push-pull amplifier              |
| Output coupling capacitor   | 10 µF electrolytic | Blocks DC, passes AC audio signal           |
| Series resistors / bias net | 220 Ω, 100 Ω etc.| Biases transistors, sets current & gain      |
| Voltage regulator           | LM7805           | Provides regulated 5 V rail for amplifier & MCU |

These parts are standard EGR 304 components and remain fixed across all three speaker options; the chosen speaker must therefore be compatible with:

- 5 V supply  
- 8 Ω load impedance  
- Approximately 0.5–1 W available output power from the amplifier

---

### Choice

| Use Case                            | Recommended Speaker      | Compatible Driver                       |
|-------------------------------------|--------------------------|-----------------------------------------|
| Prototype / low-volume demo        | **FD3057 (kit)**         | Discrete push-pull (2N3904 / 2N3906)    |
| Compact enclosure / improved fidelity | **CDS-16098A (CUI)**   | Same discrete push-pull amplifier       |
| Final production-style design with round cutout | **AS02808MR-R (PUI)** | Same discrete push-pull amplifier       |

For the **current AutoCan lab build**, the **FD3057 kit speaker** is used because it is already available, works with the existing PCB footprint, and meets the minimum power and audibility requirements. The **CDS-16098A** and **AS02808MR-R** are documented as viable alternatives for future compact or higher-fidelity versions.

---

### Decision-Making and How the Choice Meets Requirements

1. **Impedance and amplifier compatibility**  
   All three candidates are **8 Ω speakers**, which matches the design of the 5 V push-pull transistor amplifier (2N3904 / 2N3906). This avoids redesigning the bias network or risking excessive current through the devices.

2. **Power handling**  
   - FD3057 handles roughly **0.5–1 W**, which is adequate for the short-duration tones used in AutoCan.  
   - CDS-16098A and AS02808MR-R are specified for **0.7–1 W** and **1–1.5 W**, respectively, providing comfortable headroom when driven from the 5 V supply. 
3. **Frequency response / audibility**  
   The CDS-16098A and AS02808MR-R both cover approximately **500 Hz–20 kHz**, so they easily span the 1–5 kHz range where human hearing is most sensitive.  
   The FD3057, while less well-documented, has been verified in the lab to produce clearly audible tones in this range.

4. **Size and mechanical integration**  
   - FD3057 is physically larger but easy to mount on a simple panel or bracket and already matches the kit hardware.  
   - CDS-16098A is ultra-compact (16 × 9 × 3 mm) and ideal for a tight enclosure, at the cost of more complex mounting. 
   - AS02808MR-R offers an intermediate option: smaller than FD3057 but still round, making it straightforward to integrate in a future enclosure design. 

5. **Cost and availability**  
   - FD3057 is effectively **free** for the project because it is included in the lab kit.  
   - CDS-16098A and AS02808MR-R are both low-cost (~\$2–3), widely available parts from standard distributors, so they are realistic options for later iterations.

6. **Final justification**  
   Given the current course constraints, the **FD3057 kit speaker** is selected as the primary component for the AutoCan design. It satisfies the electrical requirements (8 Ω, ≈0.5–1 W), is loud enough for alerts in a lab/vehicle environment, and requires no additional cost or PCB changes.  
   At the same time, documenting **three fully-specified alternatives** demonstrates that the design could easily migrate to a compact micro-speaker (CDS-16098A) or a more standard 28 mm round speaker (AS02808MR-R) without redesigning the power or driver circuitry.

---

### Summary

- All major components for the **speaker subsystem** (speaker, driver transistors, coupling capacitor, and 5 V supply) are explicitly listed.  
- The **speaker component** itself has **three detailed options**, each with specs, pros/cons, and use cases.  
- The **decision-making process** connects the final choice directly to the subsystem requirements: impedance, power, frequency range, mechanical size, cost, and compatibility with the existing 5 V amplifier.




