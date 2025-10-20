---
layout: page
title: "Industrial Robots — IE 574 (Spring 2025)"
permalink: /projects/ie574-industrial-robots/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="{{ site.baseurl }}/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Course:** Industrial Robots (IE 574, Purdue University)  
**Instructor:** Prof. Yu She  **Term:** Spring 2025  
**Keywords:** TM Flow, FetchCore, CoppeliaSim, UR5/UR5e, ROS 2 Integration, Computer Vision, Mobile Manipulation  

---

<div style="display:flex; align-items:flex-start; gap:25px; flex-wrap:wrap; margin-bottom:20px;">
  <div style="flex:1; min-width:300px;">
    <h2 id="overview">Overview</h2>
    <p>
      Across three progressively complex projects, our team explored the <strong>integration of industrial manipulators, AMRs, and perception systems</strong> within simulated and physical environments.  
      The sequence—from collaborative robot networking to vision-guided manipulation and multi-robot grocery-store automation—developed my ability to 
      <strong>design, synchronize, and validate hybrid robotic systems</strong> combining manipulation, navigation, and perception.
    </p>
  </div>

  <div style="flex:0 0 auto;">
    <img src="/portfolio/assets/images/IE/top_right.jpg" width="300px" style="border-radius:10px;" alt="IE574 lab setup image">
  </div>
</div>

---

## Project 1 — Collaborative Robot Workflow with AMR and Node-RED
**Objective:** Coordinate two TM12 manipulators (“Daisey” & “Rosie”) with a Fetch AMR (“Jerry”) through Node-RED-based network control.

- Implemented pick-and-place routines in **TM Flow** with waypoint interpolation and vision markers for cup alignment.  
- Programmed **Fetch Core navigation** between multiple stations using sensors for alignment and cart docking.  
- Integrated all robots via **Node-RED webhooks** and Modbus triggers for synchronized execution.  
- Established event-driven communication (Play → AMR → Manipulator → Return) ensuring no premature task execution.  

---

## Project 2 — Vision-Guided Sorting and Pick-and-Place
**Objective:** Develop a **vision-based sorting system** using a UR5e + Robotiq 2F-140 gripper + Intel RealSense D415.  

- Implemented a **2-stage image-processing pipeline** (grayscale → Canny edge → contour → classification) to locate and classify objects by shape.  
- Converted 2-D pixel coordinates → 3-D camera coordinates using depth data for precise grasp poses.  
- Designed **trajectory waypoints** and pick-place sequences via inverse kinematics and gripper orientation alignment.  
- Added a **feedback loop** that adjusts end-effector orientation continuously from live camera data to maintain perpendicular alignment to object edges.  
- Validated full integration in both **real hardware and CoppeliaSim** environments.

**Core Skills:** Computer vision · Coordinate transformation · Grasp planning · End-effector control · IK solver tuning  

---

## Project 3 — Grocery Store Automation with Mobile Manipulation
**Objective:** Simulate an **autonomous robotic system** for grocery-store shelf replenishment and misplaced-item correction.  

- Modeled a full store environment in **CoppeliaSim**, including dynamic obstacles (customers, carts).  
- Integrated a **UR5 manipulator mounted on a Pioneer P3Dx AMR**, equipped with RGB-depth camera for vision-based grasping.  
- Designed **path planning and collision avoidance** with waypoint-based navigation and real-time collision sensors.  
- Developed **color-based machine vision** to identify misplaced items and trigger restocking actions.  
- Implemented **bidirectional event-based synchronization** between AMR and UR5 using signal triggers (Arrival / Completion).  
- Achieved autonomous execution of two tasks—**restocking red items** and **returning misplaced green items**—with consistent success.  

---

## Media

<div style="display:flex; flex-direction:column; align-items:center; gap:20px; margin-top:10px;">

  <video width="720" controls>
    <source src="/portfolio/assets/images/IE/Project_1x.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <p><em>Project 1 — Node-RED integration between TM robots and Fetch AMR.</em></p>

  <video width="720" controls>
    <source src="/portfolio/assets/images/IE/Project2_Labx.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <p><em>Project 2 — Classification and sorting on UR-Arm.</em></p>

  <video width="720" controls>
    <source src="/portfolio/assets/images/IE/project2_Sim.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <p><em>Project 2 — Simulation of the classification task.</em></p>

  <img src="/portfolio/assets/images/IE/project3.jpg" width="700px" style="border-radius:10px;" alt="Project 3 simulation environment">
  <p><em>Project 3 — CoppeliaSim grocery-store environment for mobile manipulation.</em></p>

</div>

---

## Reflection
Collectively, these projects advanced my capability to **bridge perception, motion, and system control**—transitioning from isolated robot tasks to coordinated, intelligent systems.  
This hands-on trajectory established a foundation for my research in **safe motion planning and constraint-aware autonomy**, emphasizing verifiable performance across simulation, bench, and field contexts.
