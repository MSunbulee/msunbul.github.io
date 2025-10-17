---
title: "UR10e Wave-Mimic Testbed"
year: 2024
affiliation: "KAUST RISC Lab"
role: "Lead design & integration"
tags: [hardware-in-the-loop, URScript, MPC, CBF, ROS2]
summary: "Hardware-in-the-loop platform that reproduces ocean-like disturbances on a UR10e for controller evaluation."
# layout is inherited; permalink comes from the collection rule
---

**Affiliation:** KAUST RISC Lab (2024) — with Prof. Shinkyu Park  
**Role:** Lead design & integration  
**Keywords:** hardware-in-the-loop, URScript, MPC/CBF, validation

## Problem
Robots in wave-disturbed environments need controllers validated against realistic, repeatable disturbances; sim-only tests miss actuation limits, timing jitter, and sensing noise.

## Approach
- Velocity-profile generator with seven periodic profiles (sine, square, triangle, chirp, …) and adjustable amplitude/speed/shape  
- URScript export for on-robot execution; ROS 2 logging for ground truth  
- Bench harness for repeatable runs; fidelity metric \(E=\tfrac{1}{N}\sum_{i=1}^{N}\lVert \hat{\mathbf p}_i-\mathbf p_i\rVert_2\)

## My Contribution
Architecture, generator, timing/jitter mitigation, URScript integration, ROS 2 logging, experiment design, and analysis.

## Results (key metrics)
- Displacement **0.5 m**; peak velocity **0.65 m/s**  
- Timing jitter **\< 5 ms**  
- High fidelity across ≥10 runs/profile

## Media
![UR10e profiles](/portfolio/assets/images/ur10e/profile-overlay.png)

## Tech Stack
UR10e, URScript, ROS 2 (rclcpp/rosbag2), Python, NumPy, Matplotlib.
