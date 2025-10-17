---
layout: page
title: "UR10e Wave-Mimic Testbed"
permalink: /projects/ur10e/
---

**Affiliation:** KAUST RISC Lab (2024) — with Prof. Shinkyu Park

**Summary:** A velocity-profile generator for the UR10e that reproduces time-varying ocean-wave disturbances to evaluate controllers on hardware.

**Your contribution:** Implemented 7 periodic motion profiles (adjustable amplitude, speed, shape) exporting URScript; integrated logging for validation.

**Key metrics:**
- Amplitude up to **0.5 m**
- End-effector speed **0.65 m/s**
- Jitter **< 5 ms**
- Fidelity validated via \(E=\tfrac{1}{N}\sum_{i=1}^N \lVert \hat{\mathbf p}_i - \mathbf p_i \rVert_2\)

**Artifacts:** [Code](#) · [Dataset](#) · [Video](#) · [Poster](#)

**Gallery**
![UR10e setup](/assets/img/ur10e.jpg){: style="max-width:720px; border-radius:12px;" }

**Reflection:** Reinforced the sim→bench→hardware approach to maintain safety guarantees under realistic disturbances.
