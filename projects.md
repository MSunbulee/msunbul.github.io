---
layout: page
title: "Research / Projects"
permalink: /projects/
---

{% include top-nav.html %}

# Research / Projects
A selection of projects demonstrating my research in **optimization-based control, motion planning, and autonomy under uncertainty**—spanning simulation, bench, and hardware validation.

---

## UR10e Wave-Mimic Testbed for Disturbance Studies
**Affiliation:** KAUST RISC Lab (Summer 2025) — with Prof. Shinkyu Park  
**Focus:** Hardware-in-the-loop platform that reproduces wave-like 1-D disturbances using a UR10e.  
**Contribution:** Built a velocity-profile generator with seven periodic motion modes (sin, triangular, composite) and URScript export. Max displacement **0.5 m** and end-effector speed **0.65 m/s**; accuracy evaluated via an RMSE metric between commanded and recorded motion. :contentReference[oaicite:0]{index=0} :contentReference[oaicite:1]{index=1}  
**[→ View Project](/projects/ur10e/)**

---

## Palm-Canopy 3-D Meshing Benchmark
**Affiliation:** KAUST RISC Lab (Summer 2025)  
**Focus:** 3-D reconstruction for agricultural robotics.  
**Contribution:** End-to-end capture→preprocess→mesh pipeline comparing ZED-2 stereo vs. smartphone LiDAR; evaluated vertex density, coverage, and robustness. LiDAR produced ≈ **2.0 M** vertices vs. **0.7 M** from stereo. :contentReference[oaicite:2]{index=2} :contentReference[oaicite:3]{index=3}  
**[→ View Project](/projects/palm-canopy-mesh/)**

---

## Underwater Glider / AUV Modeling & Control
**Affiliation:** Purdue University / KAUST RISC Lab (2024)  
**Focus:** Dynamic modeling of an AUV with **two control degrees** (buoyancy regulation & linear propulsion) enabling glide and submerged modes—implemented in ROS 2 / Gazebo.  
**Contribution:** Vehicle model, mode logic, and validation runs; emphasis on switching between gliding and powered motion (no MPC in this work). :contentReference[oaicite:4]{index=4}  
**[→ View Project](/projects/underwater-glider/)**

---

## Autonomous Water-Quality Boat (Senior Project)
**Affiliation:** KFUPM (2023)  
**Focus:** Autonomous surface vehicle for real-time water-quality monitoring.  
**Contribution:** Led system design & control; integrated GPS, IMU, and pH sensors on a dual-thruster platform for manual and fixed-path missions.  
**Metrics:** **< 0.5 m** GPS tracking error and **> 95%** uptime in field trials. :contentReference[oaicite:5]{index=5}  
**[→ View Project](/projects/wq-boat/)**

---

## Manipulator Trajectory Planning & Control — ECE 569
**Affiliation:** Purdue University (Fall 2024)  
**Focus:** UR manipulator kinematics and trajectory tracking in ROS 2 / MoveIt.  
**Contribution:** DH + PoE modeling, analytical/iterative IK, Lissajous & trapezoidal trajectories, and joint-space PD control with logging/visualization.  
**[→ View Project](/projects/ece569-project/)**

---

## Industrial Robots — IE 574
**Affiliation:** Purdue University (Spring 2025) — Prof. Yu She  
**Focus:** Collaborative automation & mobile manipulation.  
**Contribution:**  
1) **Networked workflow:** two TM12 arms + Fetch AMR via Node-RED.  
2) **Vision-guided sorting:** UR5e + RealSense with live orientation correction.  
3) **Grocery-store automation:** UR5 on AMR in CoppeliaSim with perception-driven restocking.  
**[→ View Project](/projects/ie574-industrial-robots/)**

---

## Autonomous Systems — ME 597AS
**Affiliation:** Purdue University (Fall 2024) — Dr. Nina Mahmoudian  
**Focus:** End-to-end autonomy in ROS 2 / Gazebo.  
**Contribution:** Perception, mapping (occupancy grid / SLAM), AMCL localization, custom A* global planning, and closed-loop navigation on TurtleBot3.  
**[→ View Project](/projects/me597as-autonomous-systems/)**

---

## Consensus-Driven Adaptive Signal Control
**Affiliation:** Purdue University (2025)  
**Focus:** Distributed optimization for traffic networks via consensus + adaptive coordination.  
**Contribution:** Front-priority weighted **average-consensus** within an Extended-Chain topology; controller allocates phases from real-time queue/delay summaries.  
**Metrics:** **57.1%** average waiting-time reduction and **53.3%** worst-case delay reduction across **100** one-hour simulations. :contentReference[oaicite:6]{index=6}  
**[→ View Project](/projects/consensus-signal-control/)**

---

## Selected Coursework
- **Manipulator Trajectory Planning & Control — ECE 569 (Purdue, Fall 2024)**  
  Modeling (DH/PoE), IK, trajectory generation, and joint-space PD control in ROS 2 / MoveIt.  
  **[Course Project →](/projects/ece569-project/)**

- **Industrial Robots — IE 574 (Purdue, Spring 2025)**  
  Multi-robot coordination (TM12 + Fetch AMR), vision-guided sorting, and mobile manipulation in CoppeliaSim.  
  **[Course Projects →](/projects/ie574-industrial-robots/)**

- **Autonomous Systems — ME 597AS (Purdue, Fall 2024)**  
  Full autonomy stack: perception, SLAM, AMCL, A* planning, and closed-loop navigation on TurtleBot3.  
  **[Course Labs/Project →](/projects/me597as-autonomous-systems/)**
