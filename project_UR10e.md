---
layout: page
title: "UR10e Wave-Mimic Testbed"
permalink: /projects/ur10e/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Affiliation:** KAUST RISC Lab (2024) — with Prof. Shinkyu Park  
**Role:** Lead Design & Integration  
**Keywords:** URScript, hardware-in-the-loop, adaptive control, experimental validation  

---

## Abstract / Overview
This project developed an **experimental testbed for time-varying 1D disturbances** using a **UR10e manipulator**.  
The system enables **controller validation for underwater vehicle dynamics** by reproducing wave-like motion profiles in the lab—reducing costly, time-consuming underwater tests.  
Seven periodic trajectories were generated with adjustable amplitude and speed (up to **0.5 m displacement** and **0.65 m/s velocity**), exported via URScript, and validated in **ROS2** and **URSim**.  
This platform bridges theoretical control design with real-world hardware evaluation, providing a **reusable benchmark** for disturbance testing.

---

## 1. Introduction
Ocean environments introduce nonlinear, time-varying disturbances that challenge the stability of underwater control systems.  
Repeated field testing is costly, risky, and provides limited accuracy due to noisy underwater sensing.  
This project aimed to replicate these conditions in a **controlled laboratory setting**, allowing validation of underwater controllers without submersion.

---

## 2. Methodology

### 2.1 System Overview
- **Hardware:** UR10e 6-DoF industrial manipulator acting as a programmable disturbance generator.  
- **Software:** ROS 2 for motion recording, URSim for offline verification, URScript for trajectory execution.  
- **Deliverable:** Modular trajectory generator producing configurable motion profiles for controller tests.

### 2.2 Trajectory Design
- Planned **velocity trajectories** (sinusoidal, triangular, and composite forms).  
- Integrated velocity to predict **position trajectories**.  
- Validated using recorded vs. planned position data.  
- Used the metric \( E = \tfrac{1}{N}\sum_{i=1}^{N}\|\hat{\mathbf{p}}_i - \mathbf{p}_i\|_2 \) to quantify error.

### 2.3 Implementation
- Generated URScript files executed directly on UR10e.  
- Recorded joint-space positions and end-effector paths using ROS topics.  
- Verified synchronization between commanded and measured motion.

---

## 3. Results
- Achieved high-fidelity wave reproduction with < 1 cm average tracking error.  
- Real-time loop latency remained below **10 ms**.  
- Validated multiple disturbance modes with **repeatable performance** across trials.  

<div style="text-align:center;">
  <img src="/assets/img/ur10e_setup.jpg" width="420px" alt="UR10e experimental setup">
  <p><em>Figure 1. Experimental setup for time-varying 1D disturbance generation.</em></p>
</div>

---

## 4. Discussion
The setup successfully provided a controllable, verifiable disturbance source for evaluating adaptive and robust controllers.  
Key challenges included maintaining safety at high-speed motion and handling velocity discontinuities.  
The platform’s modular design makes it extendable to 3D motion and other robotic arms.

---

## 5. Conclusion
The **UR10e Wave-Mimic Testbed** establishes a practical middle ground between simulation and full-scale field testing.  
It enables reproducible, safe, and quantitatively validated controller evaluation under realistic wave dynamics.  
Future work will automate trajectory generation for arbitrary disturbance spectra and extend the benchmark to multi-axis motion.

---

## 6. References / Documentation
- [Poster (PDF)](/assets/docs/Poster.pdf)  
- [URScript Control Repository](#)  
- [ROS 2 Dataset](#)  
- [Project Hub / Report](#)

---

## 7. Acknowledgments
Thanks to **Prof. Shinkyu Park**, **Ali Al Nasser**, and all **RISC Lab** members for their continuous support and feedback.

---

## 8. Additional Materials
- 🎥 [Demo Video — Wave Playback on UR10e](#)  
- 🎥 [Simulation Video (URSim Verification)](#)  
- 🖼️ [Image Gallery](#)  
- 📄 [Poster (PDF)](/assets/docs/Poster.pdf)

---

## Media
<div style="display:flex; flex-wrap:wrap; gap:12px; justify-content:center;">
  <img src="/assets/img/ur10e_wave_demo.gif" width="360px" alt="UR10e wave playback">
  <img src="/assets/img/ur10e_ros_capture.png" width="360px" alt="ROS2 position recording">
  <img src="/assets/img/ur10e_poster_preview.jpg" width="360px" alt="Poster preview">
</div>
