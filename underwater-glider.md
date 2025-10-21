---
layout: page
title: "Underwater Gladiator AUV"
permalink: /projects/underwater-glider/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="{{ site.baseurl }}/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Affiliation:** Purdue University — MARS Lab (2025)  
**Advisor:** Prof. Yu She  
**Collaborators:** MARS Lab, Shiraz Team  
**Role:** Mechanical Design & ROS 2 Modeling  
**Keywords:** AUV, glider mechanics, buoyancy control, ROS 2 simulation, underwater robotics  

---

## Abstract / Overview
At Purdue’s **MARS Lab** under **Prof. Yu She**, I contributed to the **Underwater Gladiator** project — an autonomous underwater vehicle (**AUV**) designed to operate in two distinct modes:  
1. **Conventional propulsion (submarine mode)** for direct thrust and maneuvering, and  
2. **Energy-efficient gliding mode**, driven by **dynamic buoyancy and mass-distribution control**.

My work focused on **mechanical design and ROS 2 integration**, developing and validating a glider mechanism capable of adjusting its **pitch** and **submerged velocity** through coordinated **mass-shifting** and **water-tank regulation**.

---

## 1. Introduction
Underwater exploration vehicles face a trade-off between **endurance** and **maneuverability**.  
Traditional AUVs rely on thrusters for agility but consume significant energy.  
Gliders, conversely, achieve high endurance via buoyancy-driven motion yet lack rapid control authority.  

The **Underwater Gladiator** merges these paradigms by integrating **thruster-based propulsion** and **glider-based buoyancy control**, enabling adaptive operation across a range of underwater missions.

---

## 2. System Architecture

### 2.1 Mechanical Design
- **Dual-mode structure:** combines a primary thruster with a controllable buoyancy engine.  
- **Variable-mass subsystem:** internal movable weight for precise pitch and trim adjustment.  
- **Water-tank subsystem:** pumps regulate fluid volume to alter density and control ascent/descent rate.  
- Modular layout for easy maintenance and sensor integration.

### 2.2 Simulation & Control
- Modeled the full hydrodynamic dynamics in **ROS 2 / Gazebo**, including drag, ballast shift, and thrust forces.  
- Implemented two controllable DOFs:  
  1. **Linear propulsion (thrust)**,  
  2. **Buoyancy regulation (mass + tank control)**.  
- Verified the dynamic response using trajectory and velocity tracking logs.  
- Simulated both **propulsion** and **gliding** modes under realistic drag and water-density conditions.

---

## 3. Results
The following media demonstrate my core contributions to the project:

<div style="text-align:center; margin:10px 0 20px;">
  <img src="/portfolio/assets/images/glider/model.png" width="680px" alt="Underwater Gladiator model visualization">
  <p style="margin-top:6px;"><em>Figure 1 — ROS 2 / Gazebo visualization of the dual-mode AUV model.</em></p>
</div>

<div style="text-align:center; margin:20px 0;">
  <video width="720" controls>
    <source src="/portfolio/assets/images/glider/movable_mass.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <p style="margin-top:6px;"><em>Figure 2 — Demonstration of internal movable-mass control within the URDF framework.</em></p>
</div>

<div style="text-align:center; margin:20px 0;">
  <video width="720" controls>
    <source src="/portfolio/assets/images/glider/Storm_simulation.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <p style="margin-top:6px;"><em>Figure 3 — Storm-condition simulation showcasing wave-disturbance effects on the AUV environment.</em></p>
</div>

**Highlights**
- Verified glider-mode dynamics in ROS 2 using buoyancy-driven motion equations.  
- Demonstrated **smooth pitch transitions** between thrust and glide regimes.  
- Showed robust stability under external wave disturbances.  
- Confirmed feasibility of internal mass-shift and buoyancy control prior to prototyping.

---

## 4. Discussion
Integrating propulsion and buoyancy control introduced complex coupling between **mechanics** and **fluid dynamics**.  
The simulation framework allows testing of adaptive control laws and quantifying **energy-efficiency gains** before hardware implementation.  
This work deepened my expertise in **system-level modeling**, **underwater control design**, and **ROS-based modular development**.

---

## 5. Conclusion
The **Underwater Gladiator AUV** demonstrates a scalable approach to combining **endurance-oriented gliding** with **agile thrust control**.  
My contributions established the **mechanical framework**, **simulation environment**, and **dynamic validation** supporting future field deployments.  
Next, the system will transition toward **embedded buoyancy-actuator integration** and **in-tank validation**.

---

## Acknowledgments
Grateful thanks to **Prof. Yu She** and the **MARS Lab** for guidance and collaboration, and to **Shiraz** for joint work on mechanical modeling and simulation alignment.

---

<!-- MathJax (if any light equations are later added) -->
<script>
window.MathJax = {
  tex: { inlineMath: [['$','$'], ['\\(','\\)']] },
  svg: { fontCache: 'global' }
};
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js" async></script>
