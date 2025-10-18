---
layout: page
title: "Manipulator Trajectory Planning and Control — ECE 569"
permalink: /projects/ece569-project/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
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
- Achieved end-effector tracking error below **2 mm** across multi-axis motions.  
- Recorded trajectories to **CSV logs** for post-analysis and generated long-exposure “light-painting” renders for qualitative validation.  
- Demonstrated stable, repeatable motion under varying trajectory frequencies.

---

<div style="display:flex; flex-wrap:wrap; gap:15px; justify-content:center;">
  <img src="/assets/img/lab1_table.png" width="320px" alt="URDF table and robot model">
  <img src="/assets/img/step6_step2.png" width="320px" alt="UR5 model loaded in RViz">
  <img src="/assets/img/figure41x.png" width="320px" alt="Trajectory verification plot">
  <img src="/assets/img/capture3.png" width="320px" alt="Light painting visualization">
</div>

<p style="text-align:center; margin-top:6px;"><em>Pipeline snapshots — from URDF modeling and RViz visualization to trajectory tracking and light-painting validation.</em></p>

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

---

## Media
<div style="text-align:center;">
  <video width="720" controls poster="/assets/img/figure41x.png">
    <source src="/assets/videos/ece569_demo.mp4" type="video/mp4">
    Your browser does not support HTML video.
  </video>
  <p><em>Final demonstration — UR arm tracing a smooth 3-D trajectory using PD control and trapezoidal velocity profiles.</em></p>
</div>
