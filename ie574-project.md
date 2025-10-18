---
layout: page
title: "Industrial Robots — IE 574 (Spring 2025)"
permalink: /projects/ie574-industrial-robots/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Course:** Industrial Robots (IE 574, Purdue University)  
**Instructor:** Prof. Yu She  **Term:** Spring 2025  
**Keywords:** TM Flow, FetchCore, CoppeliaSim, UR5/UR5e, ROS 2 Integration, Computer Vision, Mobile Manipulation  

---

## Overview
Across three progressively complex projects, our team explored the **integration of industrial manipulators, AMRs, and perception systems** within simulated and physical environments.  
The sequence—from collaborative robot networking to vision-guided manipulation and multi-robot grocery-store automation—developed my ability to **design, synchronize, and validate hybrid robotic systems** combining manipulation, navigation, and perception.

---

## Project 1 — Collaborative Robot Workflow with AMR and Node-RED
**Objective:** Coordinate two TM12 manipulators (“Daisey” & “Rosie”) with a Fetch AMR (“Jerry”) through Node-RED-based network control.

- Implemented pick-and-place routines in **TM Flow** with waypoint interpolation and vision markers for cup alignment.  
- Programmed **Fetch Core navigation** between multiple stations, using sensors for alignment and cart docking.  
- Integrated all robots via **Node-RED webhooks** and Modbus triggers for synchronized execution.  
- Established event-driven communication (Play → AMR → Manipulator → Return) ensuring no premature task execution.  
- Reflected on grasp strategy failures (top-grasp pivoting) → evaluated side-approach solutions:contentReference[oaicite:0]{index=0}.

**Skills:** Multi-robot coordination | Networked control | Event trigger design | Human-robot workflow debugging  

---

## Project 2 — Vision-Guided Sorting and Pick-and-Place
**Objective:** Develop a **vision-based sorting system** using a UR5e + Robotiq 2F-140 gripper + Intel RealSense D415.  

- Implemented a **2-stage image-processing pipeline** (grayscale → Canny edge → contour → classification) to locate and classify objects by shape.  
- Converted 2-D pixel coordinates → 3-D camera coordinates using depth data for precise grasp poses.  
- Designed **trajectory waypoints** and pick-place sequences via inverse kinematics and gripper orientation alignment.  
- Added a **feedback loop** that adjusts end-effector orientation continuously from live camera data to maintain perpendicular alignment to object edges.  
- Validated full integration in both **real-hardware and CoppeliaSim** environments:contentReference[oaicite:1]{index=1}.

**Skills:** Computer vision | Coordinate transformation | Grasp planning | End-effector control | IK solver tuning  

---

## Project 3 — Grocery Store Automation with Mobile Manipulation
**Objective:** Simulate an **autonomous robotic system** for grocery-store shelf replenishment and misplaced-item correction.  

- Modeled a full store environment in **CoppeliaSim**, including dynamic obstacles (customers, carts).  
- Integrated a **UR5 manipulator mounted on a Pioneer P3Dx AMR**, equipped with RGB-depth camera for vision-based grasping.  
- Designed **path planning and collision avoidance** with waypoint-based navigation and real-time collision sensors.  
- Developed **color-based machine vision** to identify misplaced items and trigger restocking actions.  
- Implemented **bidirectional event-based synchronization** between AMR and UR5 using signal triggers (Arrival / Completion).  
- Achieved autonomous execution of two tasks—**restocking red items** and **returning misplaced green items**—with consistent success:contentReference[oaicite:2]{index=2}:contentReference[oaicite:3]{index=3}.  

**Skills:** Mobile manipulation | Path planning | Collision avoidance | Perception integration | Distributed control architecture  

---

<div style="display:flex; flex-wrap:wrap; gap:15px; justify-content:center;">
  <img src="/assets/img/ie574_proj1.png" width="310px" alt="Node-RED integration between TM robots and Fetch AMR">
  <img src="/assets/img/ie574_proj2.png" width="310px" alt="Vision-guided sorting with UR5e and RealSense D415">
  <img src="/assets/img/ie574_proj3.png" width="310px" alt="CoppeliaSim grocery store simulation environment">
</div>

<p style="text-align:center; margin-top:6px;"><em>Progression from multi-robot coordination to vision-guided manipulation and large-scale mobile manipulation simulation.</em></p>

---

## Core Competencies Demonstrated
- **Robotic Systems Integration** — Coordinating heterogeneous platforms (AMRs, collaborative arms, sensors) through networked communication.  
- **Motion Planning & IK** — Generating collision-free joint-space trajectories with real-time feedback adjustment.  
- **Perception & Machine Vision** — Applying image processing for object detection, classification, and pose estimation.  
- **Human-Robot Interaction Safety** — Designing fail-safe coordination through triggered communication and collision sensing.  
- **Simulation Validation & Data Analysis** — Testing scenarios under dynamic environments and evaluating task success quantitatively.  

---

## Reflection
Collectively, these projects advanced my capability to **bridge perception, motion, and system control**—transitioning from isolated robot tasks to coordinated, intelligent systems.  
This hands-on trajectory established a foundation for my research in **safe motion planning and constraint-aware autonomy**, emphasizing verifiable performance across simulation, bench, and field contexts.

---

## Media
<div style="text-align:center;">
  <video width="720" controls poster="/assets/img/ie574_proj3.png">
    <source src="/assets/videos/ie574_demo.mp4" type="video/mp4">
  </video>
  <p><em>Integrated simulation — autonomous AMR–UR5 system restocking and correcting shelf items within a dynamic grocery environment.</em></p>
</div>
