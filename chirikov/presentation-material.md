# Standard Map – Phase Space and K-Sweep Diagnostics

The Standard (Chirikov) Map is the iterated map:

> <p align="center">
> $I_{n+1} = I_n + K\sin(\theta_n)$
> </p>
> <p align="center">
> $\theta_{n+1} = \theta_n + I_{n+1} \; (\bmod\, 2\pi)$
> </p>

It is an **area-preserving**, discrete-time dynamical system defined on a **2D torus** $(\theta, I)$.  
Unlike dissipative maps (e.g., the logistic map), the Standard Map has **no attractors**.

This document contains the figures used to illustrate how phase-space structure evolves as the kick parameter $K$ varies.

---

## 1. Phase-Space Portraits

These plots show trajectories in $(\theta, I)$ for a set of initial conditions and illustrate how the geometry of phase space changes with $K$.

---

### K = 0.2 — Completely Regular Motion

![phase_K_0.2](plots/figures/K0.2.png)

**Key features (as seen in this plot):**
- All trajectories lie on smooth, intact **invariant curves (KAM tori)**
- No visible chaotic layers or resonance islands
- Motion is entirely **quasi-periodic**
- The system is close to the **integrable** limit

This is the expected behavior of the Standard Map for small $K$: essentially no chaos.

---

### K = 0.7 — Mostly Regular with Emerging Chaotic Regions

![phase_K_0.7](plots/figures/K0.7.png)

**Key features (as seen in this plot):**
- Many invariant curves still survive as smooth closed tori
- A thin **chaotic layer** appears near $I \approx 1$, where some tori have broken
- Trajectories in that band no longer lie on smooth curves, indicating **incipient stochastic behavior**
- No clearly visible resonance island chains in this particular sampling
- Phase space is beginning to show **mixed** behavior, but regular motion still dominates

This is typical for intermediate $K$: small pockets of chaos appear, but the overall structure remains mostly ordered.

---

### K = 2.0 — Dominantly Chaotic Phase Space

![phase_K_2.0](plots/figures/K2.0.png)

**Key features (as seen in this plot):**
- A large **chaotic sea** fills most of the phase space (the diffuse background)
- Only a few **resonance islands** and smooth tori persist; most have been destroyed
- The chaotic region spans a wide range in $I$, enabling significant **transport**
- Motion in chaotic areas is diffusive and unpredictable, while small regular islands remain embedded within the chaos

At this value of $K$, global chaos is well developed.

---

## 2. I–K Diagnostic Plots  
*(Illustrate structure breakdown; not true bifurcation diagrams)*

These plots show, for each value of $K$, the distribution of **late-time values** of $I_n$ across many initial conditions. They visualize how invariant structures break apart as $K$ increases.

---

### Cleaner I–K Diagnostic (Subsampled)

![IK_diagnostic_clean](plots/figures/IK-diagnostic-clean.png)

**Interpretation:**
- Low $K$: horizontal bands correspond to intact **KAM tori**
- Intermediate $K$: bands begin to bend and split
- High $K$: values fill a broad region, indicating **global chaos**

This plot emphasizes structure by subsampling for clarity.

---

### Dense I–K Diagnostic (Full Data)

![IK_diagnostic_dense](plots/figures/IK-diagnostic-dense.png)

**Interpretation:**
- Shows the full texture of area-preserving chaotic dynamics
- Fine resonance structures and stochastic layers appear at moderate $K$
- At high $K$, the phase space becomes densely chaotic

---

## 3. Why This Is Not a Logistic Bifurcation Diagram

The logistic map is a **dissipative** system: trajectories collapse onto **attractors**, producing a clean branching structure described by

> <p align="center">
> $x_{n+1} = r x_n (1 - x_n)$
> </p>

The Standard Map is fundamentally different. Being **area-preserving**, it evolves via

> <p align="center">
> $I_{n+1} = I_n + K\sin(\theta_n)$
> </p>
> <p align="center">
> $\theta_{n+1} = \theta_n + I_{n+1}$
> </p>

and **never collapses** trajectories onto attractors.

Therefore:

- No fixed-point or periodic attractors  
- No dissipative branching  
- No classical bifurcation diagram  
- Instead, we visualize **the breakdown of invariant curves**, not bifurcations

The I–K sweep is a **diagnostic tool**, not a true bifurcation diagram.

---

## 4. Key Concepts

These are the essential ideas needed to interpret the figures:

- **Torus:** Phase space wraps around in both $\theta$ and $I$
- **Orbit / trajectory:** Sequence $(\theta_n, I_n)$
- **Area-preserving map:** No contraction or expansion; no attractors
- **Invariant curves (KAM tori):** Smooth curves supporting quasi-periodic motion
- **Contractible / non-contractible tori:** Whether an invariant curve winds fully around the torus
- **Resonance islands:** Small regions of stable periodic motion (only clearly visible at larger $K$)
- **Stochastic layer:** Thin chaotic region where invariant curves have broken
- **Chaotic sea:** Large region of fully chaotic motion
- **Transport:** Drift in the momentum-like coordinate $I$
- **Rotation number:** Measures average angular change per iteration; distinguishes resonances
- **Mixed phase space:** Coexistence of ordered and chaotic dynamics

---

## Appendix A — Glossary

This appendix lists all terminology identified while studying the Standard Map.  
Definitions are not included here; this section serves purely as a reference.

- area-preserving map  
- continuous map  
- discrete-time system  
- chaotic system  
- torus  
- orbit  
- trajectory  
- stroboscopic  
- invariant curves  
- KAM tori  
    - contractible tori  
    - non-contractible tori  
- separatrices  
- rotation number  
    - rational rotation number  
    - irrational rotation number  
- Devil’s staircase  
- resonance islands  
- periodic point  
- inner foliation  
- stochastic layer  
- chaotic layers  
- island chains  
- chaotic sea  
- cantorus  
- Cantor set  
- periodic orbit  
- quasi-periodic orbits  
- chaotic orbits  
- transport  
- dissipative map  
- attractor  
- fixed point  
- Feigenbaum cascade  

---
