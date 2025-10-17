---
layout: page
title: ""
---

<div style="display:flex; align-items:flex-start; justify-content:space-between; flex-wrap:wrap;">
  <div style="flex:1; min-width:280px;">

  <h1 style="font-size:2.1rem; font-weight:700; margin:0;">Mahmoud Sunbul</h1>

  <div style="font-size:0.95rem; line-height:1.4; margin-top:4px; display:block;">
    <p style="margin:0; display:block;">Faculty Member (on leave), KFUPM — Electrical Engineering Department</p>
    <p style="margin:0; display:block;">M.S. Robotics, Purdue University (’26 expected)</p>
    <p style="margin:0; display:block;">B.S. Electrical Engineering, KFUPM (’24)</p>
  </div>



  <div style="margin:10px 0; font-size:0.95rem;">
    <a href="https://msunbulee.github.io/portfolio/contact/" target="_blank">Contact</a> ·
    <a href="/portfolio/assets/cv/msunbul_Resume.pdf" target="_blank">CV</a> ·
    <a href="https://www.linkedin.com/in/msunbul/" target="_blank">LinkedIn</a> ·
    <a href="https://github.com/MSunbulee" target="_blank">GitHub</a>
    <br>
    <strong>Email:</strong> mahmoud.sunbul@kfupm.edu.sa <span style="color:#777;"></span>
  </div>


  </div>

  <div style="flex:0 0 auto; margin-left:20px;">
    <img src="/portfolio/assets/images/mahmoud.PNG" alt="Mahmoud Sunbul" width="180" style="border-radius:12px; margin-top:5px;">
  </div>
</div>


## Research focus
I develop optimization-based control and state-estimation methods—MPC with control-barrier guarantees and adaptive disturbance modeling—to keep robots safe and effective in uncertain, human environments. My work integrates planning, control, and perception through reproducible pipelines from simulation → bench → hardware.

## Projects
- **UR10e Wave-Mimic Testbed** — Hardware-in-the-loop disturbance profiles for controller evaluation.  
  <a href="/portfolio/projects/ur10e/" target="_blank">Project page →</a>


- **3-D Palm-Canopy Meshing** — Stereo vs. depth capture; pipeline from capture → preprocess → mesh.  
  <a href="/projects/palm-mesh/">Project page →</a>

- **Consensus-Driven Adaptive Signal Control** — Reduces average wait and worst-case delay in simulation.  
  <a href="/projects/traffic-consensus/">Project page →</a>

<div style="clear:both;"></div>

{% for p in site.projects %}
- **{{ p.title }}** — {{ p.blurb }}  
  <a href="{{ p.url | relative_url }}" target="_blank">Project page →</a>
{% endfor %}

