---
layout: page
title: "Autonomous Systems — ME 597AS (Fall 2024)"
permalink: /projects/me597as-autonomous-systems/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Course:** Autonomous Systems (ME 597AS, Purdue University)  
**Instructor:** Dr. Nina Mahmoudian  **Term:** Fall 2024  
**Role:** Individual Lab & Project Implementation  
**Keywords:** ROS 2, Gazebo, Python, Perception, Navigation, Control, Kinematics  

---

## Overview
This course emphasized **hands-on development of autonomous robotic behaviors**, integrating perception, localization, planning, and control through the **ROS 2 + Gazebo** ecosystem.  
Each laboratory progressively built toward a full **autonomous navigation pipeline**, bridging modeling, sensing, and actuation on both simulated and physical platforms.

---

## Task 1 — Robot Kinematics and Odometry
- Modeled **differential-drive and skid-steer** platforms from first principles.  
- Implemented forward / inverse kinematics in Python to convert velocity commands ↔ wheel speeds.  
- Verified **dead-reckoning** accuracy in Gazebo by comparing estimated vs ground-truth poses.  
- Tuned PID velocity controllers for stable trajectory tracking.

**Outcome:** Established the mathematical basis for all later navigation and control layers.

---

## Task 2 — Perception and Mapping
- Integrated **2-D LIDAR** and **stereo camera** streams through ROS 2 topics.  
- Implemented **occupancy-grid mapping** using SLAM toolbox; validated map fidelity under noise.  
- Calibrated sensor transforms (camera ↔ base link ↔ odom) using TF2.  
- Analyzed map resolution vs loop-closure accuracy to tune computational load.

**Outcome:** Built an environment model supporting real-time localization and planning.

---

## Task 3 — Localization and Path Planning
- Employed **AMCL (Adaptive Monte Carlo Localization)** for probabilistic pose estimation.  
- Generated paths with **Dijkstra / A\*** planners, then smoothed using cubic splines.  
- Created a custom **cost-map** integrating dynamic obstacles detected from LIDAR range data.  
- Verified convergence under sensor dropout and map drift conditions.

**Outcome:** Achieved robust, repeatable navigation in cluttered indoor environments.

---

## Task 4 — Autonomous Navigation and Control Integration
- Combined all subsystems into a single **ROS 2 launch workspace** controlling a TurtleBot3 Burger.  
- Implemented **behavior-based mission logic**: navigate → detect obstacle → replan → reach goal.  
- Tuned **velocity controllers** and **local planners (DWB)** for smooth goal convergence.  
- Logged odometry vs waypoint tracking error (< 3 cm RMS) using rosbag and Python analysis scripts.  

**Outcome:** Completed a full autonomy loop —from perception to planning to actuation—validated both in Gazebo and on physical robots.

---

<div style="display:flex; flex-wrap:wrap; gap:15px; justify-content:center;">
  <img src="/assets/img/me597as_mapping.png" width="320px" alt="Occupancy grid mapping in Gazebo">
  <img src="/assets/img/me597as_nav.png" width="320px" alt="Path planning and AMCL localization visualization">
  <img src="/assets/img/me597as_robot.png" width="320px" alt="Autonomous navigation on TurtleBot3 hardware">
</div>

<p style="text-align:center; margin-top:6px;"><em>Mapping, localization, and autonomous navigation results in ROS 2 / Gazebo.</em></p>

---

## Core Skills Demonstrated
- **Kinematic Modeling & Control:** derived motion models and implemented low-level PID loops.  
- **Perception & SLAM:** sensor fusion for environment mapping and pose estimation.  
- **Planning & Navigation:** global/local path planning with real-time obstacle avoidance.  
- **ROS 2 System Engineering:** topic architecture, TF frames, launch configurations.  
- **Validation & Metrics:** trajectory error analysis, timing logs, and visual debugging.

---

## Reflection
By completing this course, I reinforced a **system-level perspective on autonomy**—how perception, planning, and control co-evolve in a robotic loop.  
These experiments deepened my intuition for **integration and failure diagnostics**, directly feeding into my research focus on **optimization-based safe motion planning and hardware-validated autonomy**.

---

## Media
<div style="text-align:center;">
  <video width="720" controls poster="/assets/img/me597as_nav.png">
    <source src="/assets/videos/me597as_demo.mp4" type="video/mp4">
    Your browser does not support HTML video.
  </video>
  <p><em>Final demonstration — Autonomous navigation loop (Perception → Localization → Planning → Control) executed on ROS 2 / Gazebo.</em></p>
</div>
