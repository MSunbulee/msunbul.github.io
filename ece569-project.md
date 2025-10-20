---
layout: page
title: "Manipulator Trajectory Planning and Control — ECE 569"
permalink: /projects/ece569-project/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="{{ site.baseurl }}/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Course:** Introduction to Robotics (ECE 569, Purdue University)  
**Instructor:** Prof. Patrick  
**Term:** Fall 2024  
**Role:** Design, Implementation, and Validation  
**Keywords:** ROS 2, UR manipulators, MoveIt simulation, kinematics, trajectory control  

---

## Overview
Developed a **complete manipulator-control pipeline** for a 6-DOF UR arm, covering kinematic modeling, trajectory generation, and closed-loop control in **ROS 2 / Python**.  
The project demonstrates my ability to integrate **analytical modeling**, **control design**, and **simulation validation** within a unified framework.

This work emphasizes:
- Translating mathematical models into functional ROS 2 systems,  
- Designing controllers for precise motion execution, and  
- Quantitatively evaluating trajectory accuracy and stability.

---

## Technical Scope

### 1. Modeling & Kinematics
- Formulated both **Denavit–Hartenberg** and **Product-of-Exponentials** models for the UR manipulator.  
- Implemented spatial algebra utilities (`VecTose3`, `MatrixExp6`, `Adjoint`, etc.) and verified **forward/inverse kinematics** consistency between spatial and body frames.  
- Validated convergence of inverse kinematics through numerical experiments and cross-checked analytical solutions.

### 2. Trajectory Planning & Control
- Generated **Lissajous** and **trapezoidal-velocity** trajectories ensuring smooth, jerk-limited motion and constant linear velocity.  
- Designed a **joint-space PD controller** with velocity feedforward for improved tracking accuracy.  
- Integrated trajectory execution with **ROS 2 publishers/subscribers** and visualized real-time motion in **RViz / MoveIt**.

### 3. Validation & Visualization
- Recorded trajectories to **CSV logs** for post-analysis and generated long-exposure “light-painting” renders for qualitative validation.  
- Demonstrated stable, repeatable motion under varying trajectory frequencies.

<div style="display:flex; flex-wrap:wrap; gap:15px; justify-content:center; margin-top:10px;">
  <img src="/portfolio/assets/images/ece569/figure41x.png" width="340" alt="Trajectory verification plot">
  <img src="/portfolio/assets/images/ece569/track%20a%20flyer%20robot%20(frams).png" width="340" alt="Tracking a flyer robot (frames)">
  <img src="/portfolio/assets/images/ece569/capture%203.png" width="340" alt="Light painting visualization">
</div>

<p style="text-align:center; margin-top:6px;"><em>Figures 1–3. Trajectory verification, motion tracking frames, and qualitative visualization.</em></p>

---

## Core Competencies
- **Robot Modeling & URDF Design** — structured multi-link systems with accurate collision and inertial models.  
- **Analytical Kinematics** — forward/inverse solvers based on exponential coordinates.  
- **Controller Design** — PD loops with velocity feedforward for trajectory tracking.  
- **ROS 2 Systems Engineering** — workspace organization, node communication, debugging, and motion validation.  
- **Quantitative Evaluation** — error logging, trajectory visualization, and reproducibility analysis.  

---

## Reflection
This project solidified my understanding of **manipulator control as a full-stack problem**—where geometric modeling, algorithmic design, and empirical validation must cohere.  
It reinforced my focus on **safe, model-based motion control**, which continues to guide my current research on **constraint-aware autonomy and hardware-validated safety guarantees**.
