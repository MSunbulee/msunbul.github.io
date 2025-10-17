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

**Affiliation:** KAUST RISC Lab (Summer 2025) — with Prof. Shinkyu Park  
**Role:** Lead Design & Integration  
**Collaboration:** Ali Al Nasser — joint experimental study and paper  
**Keywords:** URScript, hardware-in-the-loop, adaptive control, experimental validation  

---

## Abstract / Overview
This project built an **experimental testbed for time-varying 1D disturbances** using a **UR10e manipulator**, enabling **controller validation for underwater vehicles** under repeatable wave-like motion.  
Seven periodic velocity profiles (sinusoidal, triangular, composite) were implemented with adjustable amplitude and frequency, exported through URScript, and validated in **ROS 2** and **URSim**.  
The setup serves as a **hardware-in-the-loop benchmark**, bridging theoretical control design with quantitative real-world validation.

---

## 1. Introduction
Underwater robotics faces challenges from unpredictable wave disturbances and costly field trials.  
The goal was to reproduce these dynamics safely within a lab environment—allowing controllers to be tested, tuned, and verified before deployment.  
This platform provides a **scalable, low-cost, and accurate means of replicating ocean-like motion** on-demand.

---

## 2. Methodology

### 2.1 System Overview
- **Hardware:** UR10e 6-DoF robot arm as a programmable disturbance generator.  
- **Software:** ROS 2 for data logging, URSim for verification, URScript for trajectory execution.  
- **Deliverable:** Stand-alone, autonomous setup that requires **no ROS experience**—users can directly load motion profiles, generate new ones, and run tests without prior configuration.

### 2.2 Trajectory Generation
Velocity profiles \( v(t) \) were designed for multiple modes (sin, square, triangular).  
Positions \( p(t) \) were obtained by integrating \( v(t) \) over time.  
Planned and measured positions were compared using the root-mean-square error:

<div align="center">
\[
E = \sqrt{\frac{1}{N}\sum_{i=1}^{N}\|\hat{\mathbf{p}}_i - \mathbf{p}_i\|^2}
\]
</div>

where \( \hat{\mathbf{p}}_i \) is the commanded position and \( \mathbf{p}_i \) is the recorded one.  
This metric quantified trajectory fidelity and mechanical repeatability.

### 2.3 Implementation
- Trajectories exported as URScript files and executed on the UR10e controller.  
- ROS 2 used for synchronized motion capture and position logging.  
- Results cross-validated in URSim before running on hardware.

---

## 3. Results

<div style="display:flex; flex-wrap:wrap; gap:15px; justify-content:center;">
  <img src="/assets/img/ur10e_planned_position.png" width="340px" alt="Planned position profile">
  <img src="/assets/img/ur10e_planned_velocity.png" width="340px" alt="Planned velocity profile">
  <img src="/assets/img/ur10e_ros_recorded.png" width="340px" alt="ROS recorded position">
  <img src="/assets/img/ur10e_ros_vs_commanded.png" width="340px" alt="Comparison of planned vs recorded">
</div>

<p style="text-align:center; margin-top:8px;"><em>Figures 1–4. Planned position, planned velocity, recorded trajectories, and comparison results.</em></p>

---

## 4. Discussion
The setup reproduced time-varying disturbances with high positional accuracy and temporal consistency.  
Its **autonomous design** enables non-ROS users to run experiments directly, generate new profiles, and validate their controllers with minimal setup effort.  
This accessibility makes it an excellent educational and benchmarking tool for motion-control research.  

Key challenges included:
- Maintaining safety at high-speed oscillations  
- Synchronizing commanded and recorded signals  
- Automating setup to ensure ease of use without manual calibration

---

## 5. Conclusion
The **UR10e Wave-Mimic Testbed** provides a reliable and reusable experimental platform for validating control algorithms under dynamic wave-like disturbances.  
It eliminates the cost and complexity of underwater trials while preserving key motion characteristics.  
Future development will extend it to **multi-axis motion** and integrate **automated profile tuning**.

---

## 6. References / Documentation
- [Poster (PDF)](/assets/docs/Poster.pdf)  
- [URScript Generator Repository](#)  
- [ROS Dataset & Analysis Notebook](#)  
- [Joint Paper with Ali Al Nasser (under review)](#)

---

## 7. Acknowledgments
Grateful to **Prof. Shinkyu Park** for the opportunity to join the **RISC Lab** during Summer 2025,  
and to **Ali Al Nasser** for close collaboration throughout this project.  
Thanks also to all **RISC Lab members** and the **SSI team** for coordinating and supporting the summer research program.

---

## 8. Additional Materials
- 🎥 [Demo Video — Wave Playback on UR10e](#)  
- 🎥 [Simulation Video (URSim Verification)](#)  
- 🖼️ [Image Gallery](#)  
- 📄 [Full Poster (PDF)](/assets/docs/Poster.pdf)

---

## Media
<div style="text-align:center;">
  <img src="/assets/docs/Poster.jpg" width="700px" alt="Poster: Experimental setup for Time-Varying 1D Disturbance">
  <p><a href="/assets/docs/Poster.pdf" style="font-weight:600;">View full poster →</a></p>
</div>
