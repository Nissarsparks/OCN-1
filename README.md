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
| 1 | 660 nm | 1 m | 2.0 | 68.4 mV |
| 2 | 660 nm | 3 m | 2.0 | 56.1 mV |
| 3 | 950 nm | 1 m | 2.0 | 66.2 mV |
| 4 | 950 nm | 3 m | 2.0 | 57.4 mV |

### Bending Loss

| S. No. | Bending Diameter (cm) | Input Amplitude (Vpp) | Received Output Amplitude (Vpp) |
|--------|------------------------|------------------------|----------------------------------|
| 1 | Straight Fiber | 2.0 | 68.4 mV |
| 2 | 10 cm | 2.0 | 66.8 mV |
| 3 | 8 cm | 2.0 | 64.9 mV |
| 4 | 6 cm | 2.0 | 62.5 mV |
| 5 | 4 cm | 2.0 | 60.3 mV |
| 6 | 3 cm | 2.0 | 58.2 mV |
| 7 | 2 cm | 2.0 | 56.1 mV |
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

- V₁ = 68.4 mV
- V₂ = 56.1 mV
- L₁ = 1 m
- L₂ = 3 m

Formula:

α = ln(V₁/V₂) / (L₂ - L₁)

Substituting:

α = ln(68.4/56.1) / (3 - 1)

α = 0.0992 Np/m

Conversion to dB/m:

α(dB/m) = 8.686 × α

α = 8.686 × 0.0992

α = 0.862 dB/m

Therefore, attenuation at 660 nm = 0.0992 Np/m = 0.862 dB/m.

---

### Propagation Loss at 950 nm

Given:

- V₁ = 66.2 mV
- V₂ = 57.4 mV
- L₁ = 1 m
- L₂ = 3 m

Formula:

α = ln(V₁/V₂) / (L₂ - L₁)

Substituting:

α = ln(66.2/57.6) / (3 - 1)

α = 0.0711 Np/m

Conversion to dB/m:

α(dB/m) = 8.686 × α

α = 8.686 × 0.0711

α = 0.618 dB/m

Therefore, attenuation at 950 nm = 0.0824 Np/m = 0.716 dB/m.

---

### Comparison

| Wavelength | V₁ (1 m) | V₂ (3 m) | Attenuation (Np/m) | Attenuation (dB/m) |
|------------|----------|----------|--------------------|--------------------|
| 660 nm | 68.4 mV | 56.1 mV | 0.0992 | 0.862 |
| 950 nm | 66.2 mV | 57.4 mV | 0.0711 | 0.618 |

### Bending Loss

Formula:

Bending Loss (dB) = 20 log₁₀(Vstraight / Vbent)

For 2 cm bending diameter:

Vstraight = 68.4 mV
Vbent = 56.1 mV

Bending Loss = 20 log₁₀(68.4 / 56.1)

Bending Loss = 1.72 dB

---
OUTPUT 
<img width="1600" height="1200" alt="WhatsApp Image 2026-07-27 at 3 30 03 PM (2)" src="https://github.com/user-attachments/assets/e747f86c-4cb7-4b29-91ab-ffaa730fc68b" />
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/e8a65e6c-2145-4d28-9859-d5730bad0c73" />
<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/f9ff1d5a-f757-40d7-9081-69dab9844bc4" />


## RESULT
- Propagation loss and bending losses for **660nm** and **950nm** wavelengths were measured.  
- Attenuation values compared and bending loss characteristics plotted.  
