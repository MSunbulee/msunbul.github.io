---
layout: page
title: "Palm-Canopy 3-D Meshing Benchmark"
permalink: /projects/palm-canopy-mesh/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Affiliation:** KAUST RISC Lab (Summer 2025)  
**Keywords:** 3-D reconstruction, stereo vision, LiDAR scanning, agricultural robotics  

---

## Abstract / Overview
At the RISC Lab, I benchmarked two 3-D palm-canopy meshing approaches: a **ZED 2 stereo rig** and an **RGB camera paired with a LiDAR sensor**.  
Both followed a pipeline of data acquisition, pre-processing, structure-from-motion, multi-view stereo reconstruction, and meshing.  
Prior to this project I had minimal exposure to 3-D geometry, so it was a deep hands-on learning experience in modeling and evaluation.  
The benchmark quantified vertex density, area coverage, completeness, manipulator integrability, and deployment effort under varied conditions.  
Depth-camera captures achieved ≈ **2.0 M vertices** vs. **0.7 M from the ZED 2**, offering higher geometric fidelity but lower robustness and field convenience.

---

## 1. Introduction
Accurate 3-D reconstruction of vegetation canopies is critical for **harvest path planning, tree health monitoring,** and **pest detection**.  
Field conditions pose challenges—illumination variance, wind motion, and sensor drift—necessitating a systematic benchmark of capture methods.  
This work establishes a comparative study for palm trees, creating a foundation for future agricultural datasets and robotic inspection pipelines.

---

## 2. Methodology

### 2.1 Data Capture Setup
Two devices were used:  
- **ZED 2 Stereo Camera:** mounted on a mobile platform for programmable capture at ≈ 2 m radius.  
- **Smartphone LiDAR (iPhone Pro Max / Google Pixel):** handheld capture under outdoor lighting conditions.  

Each produced two samples, with careful control of exposure, distance, and motion speed to minimize vibration.  

### 2.2 Processing Pipeline
Captured frames were processed through these stages:  

1. Pre-processing and depth alignment  
2. Structure-from-Motion (SfM)  
3. Multi-View Stereo (MVS) reconstruction  
4. Mesh generation and refinement (Open3D, MeshLab)  

### 2.3 Evaluation Metrics
The comparison criteria included:  
- Vertex density and triangle count  
- Surface completeness and coverage area  
- Texture quality and noise robustness  
- Integration readiness with robotic manipulators  
- Ease of setup and field deployment  

---

## 3. Results

<div style="display:flex; flex-wrap:wrap; gap:15px; justify-content:center;">
  <img src="/portfolio/assets/images/mesh/ZED_Result.png" width="340px" alt="ZED 2 mesh reconstruction result">
  <img src="/portfolio/assets/images/mesh/LiDar_Result.png" width="340px" alt="LiDAR mesh reconstruction result">
</div>

<p style="text-align:center; margin-top:8px;"><em>Figures 1–2. Comparative reconstruction results from ZED 2 and LiDAR captures.</em></p>

Quantitatively, LiDAR meshes reached ~2.0 million vertices and ~2.1 million triangles, compared to 0.7 million vertices from the ZED 2 rig.  
Visually, LiDAR offered finer surface details and lower background clutter, while ZED maintained greater stability and reproducibility in motion.

---

## 4. Discussion & Conclusion
The study demonstrated that consumer LiDAR devices can generate high-quality meshes with minimal setup time, though they struggle under bright sunlight and thin leaf structures.  
The ZED rig is better for robotic integration and repeatable calibration, but requires careful motion control and post-filtering to achieve smooth geometry.  

This benchmark informed my later projects on perception-driven control and data-driven evaluation, highlighting how field efficiency and fidelity must be balanced in robotic datasets.  

---

## Poster & Documentation

<div style="text-align:center; margin-top:20px;">
  <img src="/portfolio/assets/images/mesh/Poster_2.png" width="700px" alt="Poster: Palm-Canopy 3-D Meshing Benchmark">
  <div style="margin-top:10px;">
    <a href="/portfolio/assets/images/mesh/Poster_2.pdf" style="font-weight:600; text-decoration:none; margin-right:25px;">🖼️ View full poster →</a>
    <a href="/portfolio/assets/images/mesh/Palme_tree_mesh_Report.pdf" style="font-weight:600; text-decoration:none;">📄 View detailed documentation →</a>
  </div>
</div>

---

## Media

<div style="display:flex; flex-wrap:wrap; gap:20px; justify-content:center;">
  <img src="/portfolio/assets/images/mesh/1.jpg" width="330px" alt="Mahmoud presenting the poster">
  <img src="/portfolio/assets/images/mesh/2.jpg" width="330px" alt="Palm tree used in experiments">
</div>

<p style="text-align:center; margin-top:8px;"><em>Figures 3–4. Project poster presentation and experimental palm-tree setup.</em></p>
