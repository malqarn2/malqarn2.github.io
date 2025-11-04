# Component Selection – Speaker

## Speaker Subsystem

Provide the audible output source for the AutoCan system by selecting a miniature 8 Ω speaker compatible with the transistor amplifier and 5 V logic-level drive from the PIC18F57Q43.

---

### Requirements

- **Operating voltage:** 5 V amplifier supply  
- **Speaker impedance:** 8 Ω (compatible with simple class-AB amplifier)  
- **Rated power:** 0.5 – 1 W  
- **Frequency range:** 500 Hz – 5 kHz (tone and alert signals)  
- **Mounting:** panel-mounted or enclosure-integrated speaker  
- **Driver circuit:** discrete push-pull amplifier (Q1 = 2N3904, Q2 = 2N3906) with DC-blocking capacitor  

---

### Options

#### 1) FD3057 (Provided Kit Speaker) — 8 Ω, ~0.5 W

**Spec (from kit / typical values):**

| Spec | Value |
|------|-------|
| Impedance | 8 Ω |
| Rated Power | 0.5 W |
| Max Power | 1.0 W |
| Resonant Frequency | ~600 Hz |
| SPL (0.5 W @ 0.1 m) | ~85 dB |
| Dimensions | Ø36 mm × 10 mm |
| Unit Cost | — (Included in kit) |

**Pros**
- Provided in lab kit  
- Compact and easy to mount  
- Works directly with 5 V transistor amplifier  

**Cons**
- Limited bass response  
- No published datasheet values for exact tuning  

---

#### 2) CUI Devices CDS-16098A — 8 Ω, 1 W Micro Speaker
![Image](https://github.com/user-attachments/assets/c134d1e8-8bce-4b2f-993f-a5da47f0f7f8)

**[Link: Digi-Key Product Page](https://www.digikey.com/en/products/detail/cui-devices/CDS-16098A/)**  

| Spec | Value |
|------|-------|
| Rated / Max Power | 1.0 W / 1.0 W |
| Impedance | 8 Ω (6.8 – 9.2 Ω @ 2 kHz) |
| Resonant Frequency (Fo) | ~500 Hz |
| SPL | 86 dB (0.5 W @ 0.1 m) |
| Frequency Response | 500 Hz – 20 kHz |
| Dimensions | 16 × 9 × 3 mm |
| Weight | 1.4 g |
| Unit Cost | ~$2.50 |

**Pros**
- Small footprint, easy to embed  
- Known SPL and frequency range  
- 1 W rating suits 5 V amplifier outputs  

**Cons**
- Low bass output  
- Requires acoustic cavity for loudness boost  

---

### Choice

| Use Case | Recommended Speaker | Compatible Driver |
|-----------|---------------------|-------------------|
| Prototype / Low-volume demo | **FD3057 (Kit)** | Discrete push-pull (2N3904/2N3906) |
| Compact enclosure / improved fidelity | **CDS-16098A (CUI)** | Same discrete push-pull amplifier |

---

### Rationale

- Both speakers meet the **8 Ω, ≤ 1 W** requirement for the existing amplifier circuit.  
- The **FD3057** is ideal for initial lab builds since it’s already included.  
- The **CDS-16098A** is well-documented and easier to spec for enclosures or final designs.  
- The 5 V amplifier provides enough swing to drive 0.5–1 W into 8 Ω without clipping under moderate loads.  

---


