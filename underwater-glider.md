---
layout: page
title: "Underwater Gladiator AUV"
permalink: /projects/underwater-glider/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Affiliation:** Purdue University — MARS Lab (2025)  
**Advisor:** Prof. Yu She  
**Collaborators:** Shiraz A., MARS Lab Team  
**Role:** Mechanical Design & ROS 2 Modeling Lead  
**Keywords:** AUV, glider mechanics, buoyancy control, Gazebo simulation, underwater robotics  

---

## Abstract / Overview
At Purdue’s **MARS Lab** under **Prof. Yu She**, I contributed to the **Underwater Gladiator** project—an autonomous underwater vehicle (AUV) designed to operate in two distinct modes:  
1. **Conventional propulsion (submarine mode)** for direct thrust and maneuvering, and  
2. **Energy-efficient gliding mode**, driven by **dynamic buoyancy and mass-distribution control**.

My primary contribution focused on **mechanical design and ROS 2 integration**, developing and validating a glider mechanism capable of adjusting its pitch and submerged velocity through coordinated mass-shifting and water-tank regulation.

---

## 1. Introduction
Underwater exploration platforms face a persistent trade-off between endurance and maneuverability.  
Traditional AUVs rely on continuous thruster use, limiting mission time. In contrast, gliders exploit buoyancy-driven motion to achieve high endurance but offer limited agility.  
The Underwater Gladiator seeks to merge both paradigms—**combining thruster-based actuation with buoyancy-driven motion**—to enable adaptable underwater operation with minimal energy loss.

---

## 2. System Architecture

### 2.1 Mechanical Design
- **Dual-mode frame** integrating a primary thruster and a buoyancy engine.  
- **Variable-mass system:** movable internal weights for fine pitch and angle adjustment.  
- **Water-tank subsystem:** pumps regulate fluid volume, altering the overall density to control descent rate.  
- Designed modularly for maintainability and sensor integration.

### 2.2 Simulation & Control
- Modeled complete vehicle dynamics in **ROS 2 / Gazebo**, including hydrodynamic drag, ballast shifts, and thrust.  
- Implemented **two controllable degrees of freedom**:  
  1. **Linear propulsion (thrust)**,  
  2. **Buoyancy regulation (mass + tank control)**.  
- Developed and verified the dynamic model using recorded trajectory and velocity profiles.  
- Simulated both operational regimes—continuous propulsion and buoyancy-driven glide—under realistic water-density and drag parameters.

---

## 3. Results
- Verified the **glider dynamics** within ROS 2 using differential equations for motion under variable buoyancy.  
- Demonstrated stable transitions between propulsion and glide modes.  
- Achieved smooth submergence control through combined angle–mass modulation, confirming mechanical feasibility before physical prototyping.

<div style="display:flex; flex-wrap:wrap; gap:15px; justify-content:center;">
  <img src="/assets/img/gladiator_model.png" width="340px" alt="Underwater Gladiator ROS2 model">
  <img src="/assets/img/gladiator_mechanics.png" width="340px" alt="Mechanical glider layout">
  <img src="/assets/img/gladiator_simulation.png" width="340px" alt="Simulation results in Gazebo">
</div>

<p style="text-align:center; margin-top:8px;"><em>Figures 1–3. Mechanical concept, ROS 2 model, and Gazebo simulation of dual-mode glider.</em></p>

---

## 4. Discussion
Integrating propulsion and buoyancy control presented mechanical and modeling challenges—particularly in achieving stable transition dynamics and realistic hydrodynamic coupling.  
The simulation framework now enables testing of control strategies and validating **glider-based energy efficiency** prior to full-scale manufacturing.  
This work deepened my understanding of **system modeling, underwater vehicle control, and ROS-based modular architectures** for autonomous platforms.

---

## 5. Conclusion
The Underwater Gladiator establishes a **dual-mode AUV framework** uniting high-endurance gliding with agile maneuvering.  
My work contributed the **mechanical design**, **ROS 2 simulation**, and **control-mode validation** supporting future field trials.  
Building on this, our next phase will integrate embedded buoyancy-actuator hardware for in-water experiments and controller tuning.

---

## 6. References / Documentation
- [Project Report (PDF)](#)  
- [ROS 2 Simulation Repository](#)  
- [Mechanical Design Files (CAD)](#)

---

## 7. Acknowledgments
Thanks to **Prof. Yu She** for the opportunity to join the **MARS Lab** and contribute to the Underwater Gladiator initiative, and to **Shiraz A.** and all **MARS team members** for collaboration on the mechanical design and modeling workflow.

---

## Media
<div style="text-align:center;">
  <img src="/assets/img/gladiator_poster_preview.jpg" width="700px" alt="Poster preview: Underwater Gladiator AUV">
  <p><a href="/assets/docs/Underwater_Gladiator.pdf" style="font-weight:600;">View full poster →</a></p>
</div>
