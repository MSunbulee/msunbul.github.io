---
layout: page
title: "Research / Projects"
permalink: /projects/
---

{% include top-nav.html %}

A selection of projects demonstrating my research in **optimization-based control, motion planning, and autonomy under uncertainty** — spanning simulation, bench, and hardware validation.

---

## Research

---

## Consensus-Driven Adaptive Signal Control
**Affiliation:** Purdue University (2025)  
**Keywords:** Distributed Optimization, Consensus Control, Traffic Networks  
**Summary:** Designed a consensus-based adaptive phase coordination system for multi-intersection traffic control. The method prioritizes near-intersection vehicles while maintaining fairness and scalability.  
**Results:** Achieved **57.1%** average waiting-time reduction and **53.3%** worst-case delay reduction across **100** one-hour simulations.  
**[→ View Paper](/portfolio/projects/consensus-signal-control/)**

---

## UR10e Wave-Mimic Testbed for Disturbance Studies
**Affiliation:** KAUST RISC Lab (Summer 2025) — with Prof. Shinkyu Park  
**Keywords:** Hardware-in-the-loop, URScript, Experimental Validation  
**Summary:** Built an experimental setup using a UR10e manipulator to reproduce programmable 1D wave-like disturbances. Implemented seven periodic motion modes with amplitude up to **0.5 m** and velocity up to **0.65 m/s**. Validated tracking fidelity via RMSE comparison between commanded and recorded trajectories.  
**[→ View Project](/portfolio/projects/ur10e/)**

---

## Projects

---


## Palm-Canopy 3-D Meshing Benchmark
**Affiliation:** KAUST RISC Lab (Summer 2025)  
**Keywords:** 3-D Reconstruction, Stereo Vision, LiDAR Scanning, Agricultural Robotics  
**Summary:** Developed a full pipeline for 3-D palm-tree canopy reconstruction using ZED 2 stereo and smartphone LiDAR data. Evaluated vertex density, coverage, and ease of deployment under outdoor conditions. LiDAR models achieved ≈ **2.0 M** vertices vs. **0.7 M** from stereo captures.  
**[→ View Project](/portfolio/projects/palm-canopy-mesh/)**

---

## Underwater Glider / AUV Modeling & Control
**Affiliation:** Purdue University / KAUST RISC Lab (2024)  
**Keywords:** Vehicle Dynamics, Glider Mode Transition, ROS 2 Simulation  
**Summary:** Modeled and simulated an underwater glider with dual control inputs for buoyancy and thrust. Implemented dynamic switching between gliding and powered motion in ROS 2 / Gazebo and verified stable path tracking under varying hydrodynamic conditions.  
**[→ View Project](/portfolio/projects/underwater-glider/)**

---

## Autonomous Water-Quality Boat (Senior Project)
**Affiliation:** KFUPM (2023)  
**Keywords:** Autonomous Surface Vehicle, GPS/IMU Fusion, Environmental Robotics  
**Summary:** Led a team to design and build an autonomous water-quality-monitoring boat integrating GPS, IMU, and pH sensors on a dual-thruster platform. Supported manual and fixed-path modes.  
**Results:** Achieved **< 0.5 m** RMS GPS tracking error and **> 95 %** uptime across multiple field missions.  
**[→ View Project](/portfolio/projects/wq-boat/)**

---

## Selected Class Projects

---

## Industrial Robots — IE 574
**Instructor:** Prof. Yu She **Term:** Spring 2025  
**Keywords:** Collaborative Robots, Computer Vision, AMR Coordination  
**Tasks:**  
- Programmed two TM12 arms and a Fetch AMR for synchronized pick-and-place tasks using Node-RED and TM Flow.  
- Implemented vision-based object classification and real-time pose correction with UR5e + RealSense.  
- Built a grocery-store automation simulation (UR5 + AMR) for shelf restocking and misplaced-item correction.  
**[→ View Project](/portfolio/projects/ie574-industrial-robots/)**

---

## Manipulator Trajectory Planning & Control — ECE 569
**Instructor:** Prof. Patrick **Term:** Fall 2024  
**Keywords:** UR Manipulators, ROS 2 / MoveIt, Trajectory Generation  
**Tasks:**  
- Derived and implemented DH + PoE kinematic models for a 6-DOF UR5.  
- Generated smooth Lissajous and trapezoidal trajectories in ROS 2.  
- Designed and tuned a joint-space PD controller with velocity feed-forward.  
**[→ View Project](/portfolio/projects/ece569-project/)**

---

## Autonomous Systems — ME 597AS
**Instructor:** Dr. Nina Mahmoudian **Term:** Fall 2024  
**Keywords:** Perception, Mapping, Navigation, ROS 2 / Gazebo  
**Tasks:**  
- Integrated LIDAR and camera data for occupancy-grid mapping (SLAM).  
- Implemented AMCL localization and global path planning (A*).  
- Combined all modules into a unified autonomy stack for TurtleBot 3 navigation.  
**[→ View Project](/portfolio/projects/me597as-autonomous-systems/)**
