# 🎶 Acoustic Design and Noise Control for a Music Hall

This project addresses the professional acoustic design of a **college-level chamber music hall**. It includes **environmental noise assessment**, **internal noise control**, **reverberation tuning**, **building acoustic insulation**, and **prediction of music-induced sound levels**, ensuring optimal conditions for both performances and lectures.

---

## 📌 Project Overview

- 📍 **Location**: Urban site near railway and main road
- 🎯 **Goal**: Maintain internal noise ≤ NR25, even during external peak noise
- 🎶 **Use Case**: Lectures, orchestral, choir, solo, jazz, rock performances
- 📐 **Focus**: Internal comfort, external sound isolation, reverberation control

---

## 📊 Noise Rating and Internal Noise Limits

- Targeted **Noise Rating**: NR25 for the music hall
- NR curves plotted and assessed from ISO 1996
- Design implication: HVAC and lighting systems must remain under NR25

![Figure 2](images/figure2.png)  
📌 *Internal source noise meets NR25 target*

---

## 🌍 External Noise Break-in and L10 Design

- External environmental control based on **L10 percentile**
- Chosen L10 = 60 dBA → Requires 35 dB insulation to meet NR25

```math
∆NR = L10 - NR = 60 - 25 = 35 dB
```

- Mitigation by: insulation, layout adjustments, and acoustic facades

![Figure 4](images/figure4.png)

---

## 🏗️ Sound Insulation and Building Material Selection

- Required **Rw/STC rating**: 60 dB  
- STC formula used:  
```math
RW = STCext + ∆NR = 25 + 35 = 60 dB
```

- Sabine formula for RT and absorption:
```math
T60 = 55.26 × V / c₀(Sα̅ + 4mV)
```

- Acoustic simulation used to optimize wall/roof/window assemblies

---

## 🎼 Sound Level Estimation for Performances

| Performance Type       | LAeq Range (dB) |
|------------------------|----------------|
| Orchestra              | 85–95          |
| Choir                  | 75–85          |
| Solo / Ensemble        | 70–90          |
| Rock Band              | 90–100         |
| Jazz Band              | 80–90          |

🎵 *Sound levels vary depending on instrument mix, room size, and dynamics*

---

## 🏡 Resident Noise Impact and Propagation Modeling

- Propagation modeled using **inverse square law**:

```math
Lr = Ls - 20 × log₁₀(dr / ds)
```

- Nighttime and peak noise levels compared to local regulations
- Estimated residential exposure modeled and mitigated

---

## 🔊 Reverberation Time and Acoustic Optimization

| Function          | Target T60 (sec) |
|------------------|------------------|
| Classical Music   | 1.6 – 2.0        |
| Jazz / Pop        | 1.0 – 1.4        |
| Lectures          | 0.6 – 1.0        |

- Adjustments made via variable acoustic panels and curtain systems
- Final hall mean RT = **2.2 s** across 500–2000 Hz band

---

## 🧱 Additional Absorbers and Acoustic Treatments

- Required extra absorption: **452.28 m²**
- Deployed absorbers: ceiling baffles, wall panels, curtains
- Sabine-based estimate:

```math
A_add = 0.16 × V × |ΔT60| / α̅
```

---

## 🏟️ Balcony, Reflectors and Secondary Geometry

- Added balcony for seating + acoustic diffusion
- Designed with:
  - Overhead reflectors for forward sound projection
  - Sound scattering geometry for spatial richness
- Improves clarity, envelopment, and immersive listening

---

## 💻 Code and Graphs

Python was used to simulate and plot NR curves and internal/external source noise graphs.

Example:
```python
plt.plot(frequencies, NR_25_values, label='NR25')
plt.plot(frequencies, internal_source, label='Internal Source')
```

![Figure 3](images/figure3.png)

> 📂 All code is included in [Appendix A](#).

---
