---
layout: page
title: "Research / Projects"
permalink: /projects/
---

{% include top-nav.html %}

# Research / Projects
A selection of eight projects demonstrating my research focus on **optimization-based control, motion planning, and autonomy under uncertainty** — spanning simulation, bench, and hardware validation.

---

## UR10e Wave-Mimic Testbed for Disturbance Studies
**Affiliation:** KAUST RISC Lab (2024) — with Prof. Shinkyu Park  
**Focus:** Hardware-in-the-loop evaluation of controllers under ocean-like disturbances.  
**Contribution:** Developed a UR10e velocity-profile generator implementing seven periodic motion patterns; amplitude ≤ 0.5 m, velocity ≤ 0.65 m/s.  
**Metrics:** < 5 ms loop jitter; trajectory fidelity validated by \(E=\tfrac{1}{N}\sum\lVert\hat{\mathbf p}_i-\mathbf p_i\rVert\).  
**[→ View Project](/portfolio/projects/ur10e/)**

---

## 3-D Palm-Canopy Meshing Pipeline
**Affiliation:** KAUST RISC Lab (2024)  
**Focus:** Perception for agricultural robotics.  
**Contribution:** Built a full capture → preprocess → mesh pipeline comparing ZED 2 (stabilized) vs smartphone depth.  
**Metrics:** Depth meshes ≈ **2.0 M vertices**, stereo ≈ **0.7 M** per tree.  
**[→ View Project](/portfolio/projects/palm-canopy-mesh/)**

---

## Underwater Glider / AUV Modeling & Control
**Affiliation:** Purdue / KAUST RISC Lab (2024)  
**Focus:** Dynamic modeling and control of underwater vehicles subject to wave disturbances.  
**Contribution:** 6-DOF modeling + MPC in ROS 2/Gazebo; wave-adaptive path tracking.  
**Metrics:** **35% RMSE reduction** over PID; **< 5 ms** timing jitter.  
**[→ View Project](portfolio/projects/underwater-gladiator/)**

---

## Autonomous Water-Quality Boat (Senior Design)
**Affiliation:** KFUPM (2023)  
**Focus:** Surface-vehicle autonomy for environmental monitoring.  
**Contribution:** Integrated GPS, IMU, pH sensors; dual-thruster control for autonomous sampling missions.  
**Metrics:** Tracking error < **0.5 m**; uptime > **95%** during field runs.  
**[→ View Project](/portfolio/projects/wq-boat/)**

---

## Manipulator Trajectory Planning and Control — ECE 569
**Affiliation:** Purdue University (2024)  
**Focus:** UR5 manipulator kinematics and trajectory tracking in ROS 2.  
**Contribution:** Analytical FK/IK; Lissajous & trapezoidal trajectories; joint-space PD control.  
**Metrics:** End-effector tracking error < **2 mm**.  
**[→ View Project](/portfolio/projects/ece569-project/)**

---

## Industrial Robots — IE 574 (3 Projects)
**Affiliation:** Purdue University (2025)  
**Focus:** Collaborative automation and mobile manipulation.  
**Highlights:**  
1) Multi-robot coordination of two TM12 arms + Fetch AMR via Node-RED.  
2) Vision-guided sorting (UR5e + RealSense) with real-time angle correction.  
3) Grocery-store automation in CoppeliaSim (UR5 + AMR) for restocking & misplaced-item return.  
**[→ View Project](/portfolio/projects/ie574-industrial-robots/)**

---

## Autonomous Systems — ME 597AS
**Affiliation:** Purdue University (2024) — with Dr. Nina Mahmoudian  
**Focus:** End-to-end autonomy pipeline in ROS 2 / Gazebo.  
**Contribution:** Integrated perception, localization, planning, and control for TurtleBot3.  
**Metrics:** Navigation error < **3 cm RMS**; real-time replanning with dynamic obstacles.  
**[→ View Project](/portfolio/projects/me597as-autonomous-systems/)**

---

## Consensus-Driven Adaptive Signal Control
**Affiliation:** Purdue University (2025)  
**Focus:** Distributed optimization for traffic networks.  
**Contribution:** Consensus-based adaptive phase control for multi-intersection coordination.  
**Metrics:** **57%** avg wait ↓ and **53%** worst-case delay ↓ across 100 sims.  
**[→ View Project](/portfolio/projects/consensus-signal-control/)**
