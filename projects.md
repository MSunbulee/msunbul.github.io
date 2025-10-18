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
**[→ View Project](/projects/ur10e-wave-mimic/)**

---

## 3-D Palm-Canopy Meshing Pipeline
**Affiliation:** KAUST RISC Lab (2024)  
**Focus:** Perception for agricultural robotics.  
**Contribution:** Built a full capture → preprocess → mesh pipeline comparing ZED 2 (stabilized) vs smartphone depth.  
**Metrics:** Depth meshes ≈ **2.0 M vertices**, stereo ≈ **0.7 M** per tree.  
**[→ View Project](/projects/palm-meshing/)**

---

## Underwater Glider / AUV Modeling & Control
**Affiliation:** Purdue / KAUST RISC Lab (2024)  
**Focus:** Dynamic modeling and control of underwater vehicles subject to wave disturbances.  
**Contribution:** Formulated 6-DOF state-space model; implemented Model Predictive Control in ROS 2 Gazebo; validated wave-adaptive path tracking.  
**Metrics:** **35 % RMSE reduction** over PID; **timing jitter < 5 ms.**  
**[→ View Project](/projects/auv-control/)**

---

## Autonomous Water-Quality Boat (Senior Design)
**Affiliation:** KFUPM (2023)  
**Focus:** Surface-vehicle autonomy for environmental monitoring.  
**Contribution:** Led integration of GPS, IMU, pH sensors and dual thruster control for autonomous sampling missions.  
**Metrics:** Tracking error < **0.5 m**; system uptime > **95 %** during field runs.  
**[→ View Project](/projects/water-quality-boat/)**

---

## Manipulator Trajectory Planning and Control — ECE 569
**Affiliation:** Purdue University (2024)  
**Focus:** UR5 manipulator kinematics and trajectory tracking in ROS 2.  
**Contribution:** Implemented analytical FK/IK, generated Lissajous & trapezoidal trajectories, and tuned joint-space PD control.  
**Metrics:** End-effector tracking error < **2 mm.**  
**[→ View Project](/projects/ece569-project/)**

---

## Industrial Robots — IE 574 (3 Projects)
**Affiliation:** Purdue University (2025)  
**Focus:** Collaborative automation and mobile manipulation.  
**Highlights:**  
1. **Project 1:** Multi-robot coordination of two TM12 arms and Fetch AMR via Node-RED.  
2. **Project 2:** Vision-guided sorting using UR5e + RealSense camera with real-time angle correction.  
3. **Project 3:** Grocery-store automation in CoppeliaSim combining UR5 + AMR for restocking and misplaced-item correction.  
**[→ View Project](/projects/ie574-industrial-robots/)**

---

## Autonomous Systems — ME 597AS
**Affiliation:** Purdue University (2024) — with Dr. Nina Mahmoudian  
**Focus:** End-to-end autonomy pipeline in ROS 2 / Gazebo.  
**Contribution:** Integrated perception, localization, planning, and control for a TurtleBot3 platform.  
**Metrics:** Navigation error < **3 cm RMS**; real-time replanning under dynamic obstacles.  
**[→ View Project](/projects/me597as-autonomous-systems/)**

---

## Consensus-Driven Adaptive Signal Control
**Affiliation:** Purdue University (2025)  
**Focus:** Distributed optimization for traffic networks.  
**Contribution:** Formulated consensus-based adaptive phase control for multi-intersection coordination.  
**Metrics:** **57 % average wait reduction** and **53 % worst-case delay reduction** across 100 simulation runs.  
**[→ View Project](/projects/adaptive-signal-control/)**

---

<p style="text-align:center; margin-top:20px;">
<em>Each project links to a detailed page with methodology, results, and media assets.</em>
</p>
