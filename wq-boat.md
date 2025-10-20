---
layout: page
title: "Autonomous Water-Quality Boat (Senior Project)"
permalink: /projects/wq-boat/
---

{% include top-nav.html %}

**Affiliation:** King Fahd University of Petroleum and Minerals (KFUPM) — Senior Design 2023  
**Role:** Team Lead (System Design & Control Integration)  
**Keywords:** autonomous surface vehicle, GPS/IMU fusion, environmental monitoring  

---

<div style="display:flex; justify-content:space-between; align-items:flex-start; flex-wrap:wrap;">
  <div style="flex:1; min-width:300px;">

  ## Overview
  This project developed a fully autonomous surface vehicle (ASV) for real-time **water-quality monitoring** in industrial and environmental settings.  
  The system integrates **GPS**, **IMU**, and **pH sensors** for both **manual** and **pre-programmed fixed-path** operation.  
  Powered by dual **900 W thrusters**, the platform supports submerged payloads up to **1 kg** for multi-depth sampling missions.

  Designed for robustness and simplicity, the boat achieved:
  - **< 0.5 m** RMS GPS tracking error  
  - **> 95 %** operational uptime  
  - Reliable pH readings across repeated trials  
  - Real-time telemetry and mission replay via onboard logging  

  </div>

  <div style="flex:0 0 auto; margin-left:24px;">
    <img src="/portfolio/assets/images/Senior/Right_top.jpg" width="280" alt="Poster day highlight" style="border-radius:10px;">
  </div>
</div>

---

## System Architecture

### Hardware Integration
Fiberglass hull with watertight electronics bay; dual-thruster differential propulsion; embedded control unit (Raspberry Pi + Arduino); GPS/IMU fusion for localization; pH sensor with submerged probe interface.

### Navigation & Control
Waypoint tracking via PID velocity control with geofencing and manual override.  
Mission logic implemented in Python with data logging and automatic mission-resume on restart.

### Communication & Power
Wi-Fi telemetry link for status updates and parameter tuning; 12 V Li-ion battery pack delivering ~30 min endurance at 600 m range.

---

## Experimental Results

Field validation in calm-water basins confirmed consistent autonomous navigation and stable sensor measurements.  
The boat completed repeated loops within **< 0.5 m** deviation from the reference path and maintained continuous logging for > 95 % of runtime.

<div style="display:flex; flex-wrap:wrap; gap:16px; justify-content:center; margin-top:10px;">
  <img src="/portfolio/assets/images/Senior/Our_boat.jpg" width="360" alt="Autonomous water-quality boat" style="border-radius:10px;">
  <img src="/portfolio/assets/images/Senior/Poster.jpg" width="360" alt="KFUPM Design Expo project poster" style="border-radius:10px;">
</div>

<p style="text-align:center; margin-top:6px;"><em>Prototype and design-expo poster showcasing system integration and field testing.</em></p>

---

## Discussion & Future Work
The project demonstrated that compact ASVs can deliver precise, repeatable water-quality measurements at low cost.  
Next steps include:
- **Adaptive sampling** based on sensor variance  
- **Solar-assisted endurance** for extended missions  
- Integration of **EC, DO, and turbidity sensors** for full water-profile analytics  

---

## Team
| Member | Discipline | Role |
|:--|:--|:--|
| **Mahmoud Sunbul** | EE | System lead — control & integration |
| **Mohammed Al Yusuf** | ME | Hull design & fabrication |
| **Abdullah Alabbad** | ME | Mechanical assembly |
| **Ali Alahmed** | EE | Electronics integration |
| **Ahmed Baabdullah** | CS | Software interface & ML data analysis |

---

## Media

<div style="text-align:center; margin-top:10px;">
  <img src="/portfolio/assets/images/Senior/Near_the_end_group_pic.jpg" width="700" alt="Team photo near final testing" style="border-radius:12px;">
  <p><em>Final prototype testing during KFUPM Design Expo 2023.</em></p>
</div>
