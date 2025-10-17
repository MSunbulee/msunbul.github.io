---
title: "UR10e Wave-Mimic Testbed"
order: 10                     # used for sorting on the listing page
year: 2024
affiliation: "KAUST RISC Lab"
role: "Lead design & integration"
tags: [hardware-in-the-loop, URScript, MPC, CBF, ROS2]
summary: "Hardware-in-the-loop platform that reproduces ocean-like disturbances on a UR10e for controller evaluation."
# If you have a cover image:
cover: /portfolio/assets/images/ur10e/cover.jpg
# permalink is auto from _config.yml: /portfolio/projects/ur10e/
---

**Affiliation:** KAUST RISC Lab (2024) — with Prof. Shinkyu Park  
**Role:** Lead design & integration  
**Keywords:** hardware-in-the-loop, URScript, MPC/CBF, validation

## Problem
Robots operating in wave-disturbed environments need controllers validated against realistic, repeatable disturbances. Sim-only tests miss actuation limits, timing jitter, and sensing noise.

## Approach
- Built a **velocity-profile generator** implementing seven periodic profiles (sine, square, triangle, chirp, etc.) with adjustable amplitude/speed/shape.  
- **URScript export** for on-robot execution; **ROS 2 logging** for ground truth.  
- Bench harness for **repeatable runs** and quick profile swapping.  
- Error metric for fidelity: \( E = \tfrac{1}{N}\sum_{i=1}^{N}\lVert \hat{\mathbf p}_i - \mathbf p_i \rVert_2 \).

## My Contribution
Architecture, trajectory generator, timing/jitter mitigation, URScript integration, ROS 2 logging, experiment design, and analysis.

## Results (key metrics)
- End-effector displacement up to **0.5 m**; peak velocity **0.65 m/s**.  
- Timing jitter **\< 5 ms** (controller loop).  
- High motion fidelity by \(E\) across profiles; reproducible across ≥10 runs/profile.

## Media
- Demo clip: (add link or embed)
- Figure: time-series trajectory vs. playback  
![UR10e profiles](/portfolio/assets/images/ur10e/profile-overlay.png)

## Tech Stack
UR10e, URScript, ROS 2 (rclcpp, rosbag2), Python tooling, NumPy, Matplotlib, GitHub Actions (optional CI for docs/plots).

## Links
- Dataset / logs (optional)  
- Source (private/public): (link)  
- Related write-up / poster: (link)
