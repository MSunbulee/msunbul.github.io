---
layout: page
title: "Autonomous Systems — ME 597AS (Fall 2024)"
permalink: /projects/me597as-autonomous-systems/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="{{ site.baseurl }}/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Course:** Autonomous Systems (ME 597AS, Purdue University)  
**Instructor:** Dr. Nina Mahmoudian  **Term:** Fall 2024  
**Keywords:** ROS 2, Gazebo, Python, Perception, Navigation, Control, Kinematics  

---

## Overview
This course emphasized **hands-on development of autonomous robotic behaviors**, integrating perception, localization, planning, and control through the **ROS 2 + Gazebo** ecosystem.  
Each module contributed to a complete **autonomous navigation pipeline**, bridging modeling, sensing, and actuation on both simulated and physical platforms.

---

## Topics Covered

### Kinematic Modeling & Odometry
Formulated **differential-drive** and **skid-steer** motion models from first principles and implemented forward/inverse kinematics in Python.  
These models formed the foundation for velocity-control design and dead-reckoning pose estimation validated in Gazebo.

---

### Perception & Mapping
Integrated **2-D LiDAR** and stereo-camera data to build **occupancy-grid maps** via the SLAM Toolbox.  
Calibrated TF frames among camera, base link, and odometry, and analyzed how map resolution and loop-closure parameters affect fidelity and computation.

---

### Localization & Path Planning
Implemented **AMCL** for probabilistic localization and designed **Dijkstra/A\***-based planners refined by spline smoothing.  
Developed a dynamic **cost-map** that incorporated live obstacle data for reliable navigation under noise and drift.

---

### Integrated Autonomy & Control
Unified all subsystems into a single **ROS 2 workspace** managing a TurtleBot3 Burger.  
Implemented behavior-based logic for goal-directed navigation, obstacle handling, and replanning.  
Tuned local planners (**DWB**) for smooth convergence, achieving < 3 cm RMS tracking error in simulation and hardware.

---

## Media

<div style="display:flex; flex-direction:column; align-items:center; gap:18px; margin-top:10px;">

  <img src="/portfolio/assets/images/ME597/P1.png" width="720" alt="Map used for path planning">

  <video width="720" controls>
    <source src="/portfolio/assets/images/ME597/Task1x.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <p style="text-align:center; margin-top:4px;">
    <em>Autonomous exploration without a prior map — online mapping and navigation achieving &gt; 90 % coverage in &lt; 5 minutes.</em>
  </p>

  <video width="720" controls>
    <source src="/portfolio/assets/images/ME597/Video_A_starx.mov" type="video/quicktime">
    Your browser does not support the video tag.
  </video>
  <p style="text-align:center; margin-top:4px;">
    <em>A* path-planning demonstration on the generated map.</em>
  </p>

</div>

---

## Reflection
Through this course, I gained a **system-level understanding of autonomy**—how perception, planning, and control interact in real time.  
These experiments strengthened my intuition for **integration, debugging, and failure analysis**, directly supporting my research in **optimization-based safe motion planning and hardware-validated autonomy**.
