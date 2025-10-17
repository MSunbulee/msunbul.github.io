---
layout: page
title: "Research / Projects"
permalink: /projects/
---

## UR10e Wave-Mimic Testbed for Disturbance Studies
**Affiliation:** KAUST RISC Lab, 2024 — with Prof. Shinkyu Park  
**Problem:** Evaluating controllers under realistic, time-varying ocean disturbances is hard without repeatable hardware profiles.  
**Contribution:** Built a velocity-profile generator (7 periodic motions) exporting URScript; amplitude up to **0.5 m**, end-effector **0.65 m/s**.  
**Metrics:** < 5 ms jitter; trajectory fidelity validated by planned vs recorded \(E=\tfrac{1}{N}\sum\lVert \hat{\mathbf p}_i - \mathbf p_i\rVert\).  
**Artifacts:** [Code](), [Dataset](), [Video]().  
**Reflection:** Reinforced sim→bench→hardware discipline for safety guarantees.

---

## 3-D Palm-Canopy Meshing Pipeline
**Affiliation:** KAUST RISC Lab, 2024  
**Problem:** Accurate canopy meshes for agricultural perception are limited by capture stability and sensor modality.  
**Contribution:** Captured with ZED 2 (stabilized) and smartphone+depth; pipeline: capture → preprocess → mesh.  
**Metrics:** Depth meshes **≈2.0M vertices** vs stereo **≈0.7M** (per tree/area).  
**Artifacts:** [Code](), [Sample Mesh](), [Video]().  
**Reflection:** Showed how sensor choice impacts geometric fidelity and downstream planning.

---

## Consensus-Driven Adaptive Signal Control
**Affiliation:** Purdue, 2025  
**Problem:** Urban intersections suffer long waits under non-stationary traffic.  
**Contribution:** Designed consensus-based control with adaptive phases.  
**Metrics:** **57%** avg wait ↓; **53%** worst-case delay ↓ across 100 one-hour sims.  
**Artifacts:** [Paper](), [Code](), [Poster]().  
**Reflection:** Validated robust performance under distribution shift.
