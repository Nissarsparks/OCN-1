# Experimental-verification-of-various-Fiber-losses--Propagation-Loss-Bend-Loss
# Propagation and Bending Losses in Plastic Fiber

## AIM
To measure propagation loss & bending losses for two different wavelengths in plastic Fiber provided with the kit.

---

## EQUIPMENTS REQUIRED
- Link-B Kit with power supply  
- Patch chords  
- 20MHz Dual Channel Oscilloscope  
- 1 MHz Function Generator  
- 1 Meter Fiber Cable  

---

## THEORY
Optical Fibers are available in different varieties of materials. These materials are usually selected by taking into account their absorption characteristics for different wavelengths of light.  

Since the signal in Optical Fiber is transmitted in the form of light (different in nature from electrons), one has to consider the interaction of matter with radiation to study the losses in fiber.  

- **Propagation Loss:**  
  - As light propagates from one end of Fiber to another, part of it is absorbed in the material (absorption loss).  
  - Some light is reflected back or scattered due to impurity particles, contributing to signal loss.  
  - Plastic Fibers typically have higher loss (~180 dB/Km).  

- **Bending Loss:**  
  - Losses occur when the angle of incidence condition is violated, causing refraction.  
  - Smaller radius of curvature → higher loss.  
  - Other losses occur due to coupling at LED and photo detector ends.  

---

## PROCEDURE

1. Connect the power supply with proper polarity to the kit link-B and switch it on.  
2. Keep all Switch Faults in **OFF** position.  
3. Set switch **SW8 → TX position**.  
4. Set switch **SW9 → TX1 position**.  
5. Set Jumper **JP5 → +12V position**.  
6. Short Jumpers **JP6, JP9, JP10**.  
7. Set Jumper **JP8 → sine position**.  
8. Keep Intensity control pot **P2 → minimum position**.  
9. Feed ~2Vpp sinusoidal signal of 1 KHz from function generator to **IN post of Analog Buffer**.  

10. Connect **OUT of Analog Buffer → TX IN of Transmitter**.  
11. Loosen cap of **SFH756V (660nm)**, insert 1m fiber, then tighten.  
12. Connect other end of fiber to **SFH350V (Photo Transistor Detector)** carefully.  
13. Observe detected signal at **ANALOG OUT** on oscilloscope. Adjust **P2** so signal amplitude = 2Vpp.  

14. Measure peak value at ANALOG OUT = **V1**.  
15. Replace 1m fiber with 3m fiber (no other changes). Measure peak value = **V2**.  

**Formula:**  
<img width="758" height="50" alt="image" src="https://github.com/user-attachments/assets/3ec6183f-3031-4862-bb34-9f59c7e29fa3" />

Where:  
- \(a\) = attenuation (nepers/meter)  
- \(L1\) = fiber length for V1  
- \(L2\) = fiber length for V2  

This \(a\) is for **660nm wavelength**.  

---

## TABULATION

### Propagation Loss

| S. No. | Wavelength | Fiber Length (m) | Input Amplitude (Vpp) | Received Output Amplitude (Vpp) |
|--------|------------|------------------|------------------------|----------------------------------|
| 1 | 660 nm | 1 m | 2.0 | 64.8 mV |
| 2 | 660 nm | 3 m | 2.0 | 52.8 mV |
| 3 | 950 nm | 1 m | 2.0 | 63.2 mV |
| 4 | 950 nm | 3 m | 2.0 | 53.6 mV |

### Bending Loss

| S. No. | Bending Diameter (cm) | Input Amplitude (Vpp) | Received Output Amplitude (Vpp) |
|--------|------------------------|------------------------|----------------------------------|
| 1 | Straight Fiber | 2.0 | 64.8 mV |
| 2 | 10 cm | 2.0 | 63.2 mV |
| 3 | 8 cm | 2.0 | 60.0 mV |
| 4 | 6 cm | 2.0 | 58.0 mV |
| 5 | 4 cm | 2.0 | 56.0 mV |
| 6 | 3 cm | 2.0 | 54.0 mV |
| 7 | 2 cm | 2.0 | 52.8 mV |
### For 950nm Wavelength
1. Set switch **SW9 → TX2 position**.  
2. Set Jumper **JP7 → +12V position**.  
3. Remove fiber from SFH756V (660nm) & SFH350V.  
4. Insert 1m fiber between **SFH450V (950nm)** & **SFH350V**.  
5. Observe detected signal at ANALOG OUT.  
6. Measure peak value = **V1**.  
7. Replace 1m fiber with 3m fiber. Measure peak value = **V2**.  

**Formula:**  
<img width="758" height="50" alt="image" src="https://github.com/user-attachments/assets/56fbe9d6-9bff-460b-b04b-d2a73d0c3cd1" />


This \(a\) is for **950nm wavelength**.  
8. Compare attenuation values for 660nm and 950nm.  

---

## MEASUREMENT OF BENDING LOSSES
1. Remove fiber from SFH450V (950nm) & SFH350V.  
2. Insert 1m fiber between **SFH756V (660nm)** & **SFH350V**.  
3. Bend fiber in a loop and measure amplitude of received signal.  
4. Reduce loop diameter gradually to ~2 cm (not less than 1 cm).  
5. Record output voltage readings.  
6. Plot graph: **Received signal amplitude vs. Loop diameter**.  

---

## CALCULATIONS

### Propagation Loss at 660 nm

Given:

- V₁ = 64.8 mV
- V₂ = 52.8 mV
- L₁ = 1 m
- L₂ = 3 m

Formula:

α = ln(V₁/V₂) / (L₂ - L₁)

Substituting:

α = ln(64.8/52.8) / (3 - 1)

α = 0.1025 Np/m

Conversion to dB/m:

α(dB/m) = 8.686 × α

α = 8.686 × 0.1025

α = 0.890 dB/m

Therefore, attenuation at 660 nm = 0.1025 Np/m = 0.890 dB/m.

---

### Propagation Loss at 950 nm

Given:

- V₁ = 63.2 mV
- V₂ = 53.6 mV
- L₁ = 1 m
- L₂ = 3 m

Formula:

α = ln(V₁/V₂) / (L₂ - L₁)

Substituting:

α = ln(63.2/53.6) / (3 - 1)

α = 0.0824 Np/m

Conversion to dB/m:

α(dB/m) = 8.686 × α

α = 8.686 × 0.0824

α = 0.716 dB/m

Therefore, attenuation at 950 nm = 0.0824 Np/m = 0.716 dB/m.

---

### Comparison

| Wavelength | V₁ (1 m) | V₂ (3 m) | Attenuation (Np/m) | Attenuation (dB/m) |
|------------|----------|----------|--------------------|--------------------|
| 660 nm | 64.8 mV | 52.8 mV | 0.1025 | 0.890 |
| 950 nm | 63.2 mV | 53.6 mV | 0.0824 | 0.716 |

### Bending Loss

Formula:

Bending Loss (dB) = 20 log₁₀(Vstraight / Vbent)

For 2 cm bending diameter:

Vstraight = 64.8 mV
Vbent = 52.8 mV

Bending Loss = 20 log₁₀(64.8 / 52.8)

Bending Loss = 1.78 dB

---
OUTPUT 
<img width="1600" height="1200" alt="WhatsApp Image 2026-07-27 at 3 30 03 PM (2)" src="https://github.com/user-attachments/assets/e747f86c-4cb7-4b29-91ab-ffaa730fc68b" />
<img width="1600" height="1200" alt="WhatsApp Image 2026-07-27 at 3 30 04 PM (2)" src="https://github.com/user-attachments/assets/6fbf730d-4da3-4abf-8a34-4c19a0030c67" />
<img width="1600" height="1200" alt="WhatsApp Image 2026-07-27 at 3 30 05 PM (1)" src="https://github.com/user-attachments/assets/6fcae461-c5cf-4719-a5f6-6eb157dfe41f" />



## RESULT
- Propagation loss and bending losses for **660nm** and **950nm** wavelengths were measured.  
- Attenuation values compared and bending loss characteristics plotted.  
