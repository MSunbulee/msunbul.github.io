---
layout: page
title: "Consensus-Driven Adaptive Signal Control"
permalink: /projects/consensus-signal-control/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="{{ site.baseurl }}/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

**Keywords:** consensus control, adaptive signal coordination, traffic optimization, scalability

---

## Abstract
We propose a hybrid **two-layer traffic signal controller** that fuses a **distributed vehicle consensus layer** with a **central adaptive phase selector**. A **front-priority weighted average consensus** emphasizes vehicles nearest the stop line, and an **Extended Chain** topology provides low-latency cross-approach communication without full connectivity. Across 100 one-hour runs, the best configuration (Average Consensus + Extended Chain) reduces **average waiting time by 57.1%** and **worst-case delay by 53.3%** relative to a global-information baseline, while maintaining competitive throughput and fairness.

<div style="text-align:center; margin:12px 0 6px;">
  <img src="/portfolio/assets/images/consensus-signal-control/First_page.png" width="720" alt="Paper first page preview">
</div>

<p style="text-align:center; margin:8px 0 18px;">
  <a href="/assets/docs/Consensus_Driven.pdf" style="font-weight:700; text-decoration:none; border:1px solid #ccc; padding:8px 14px; border-radius:8px; display:inline-block;">📄 View full paper →</a>
</p>

---

## 1. Main Results

### 1.1 One-Table Summary (100 × 1-hour episodes)

<table style="width:100%; border-collapse:collapse; font-size:0.98rem;">
  <thead>
    <tr>
      <th style="border-bottom:1px solid #ccc; text-align:left;">Configuration</th>
      <th style="border-bottom:1px solid #ccc; text-align:right;">Avg. Wait (s)</th>
      <th style="border-bottom:1px solid #ccc; text-align:right;">Max Wait (s)</th>
      <th style="border-bottom:1px solid #ccc; text-align:right;">Throughput (veh/hr)</th>
      <th style="border-bottom:1px solid #ccc; text-align:right;">Fairness (J)</th>
      <th style="border-bottom:1px solid #ccc; text-align:right;">Δ Avg Wait vs Baseline</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Baseline — Global Info (Centralized)</td>
      <td style="text-align:right;">13.90 ± 0.64</td>
      <td style="text-align:right;">118.25 ± 21.11</td>
      <td style="text-align:right;">3332 ± 479</td>
      <td style="text-align:right;">0.519 ± 0.146</td>
      <td style="text-align:right;">—</td>
    </tr>
    <tr>
      <td><strong>Average Consensus — Extended Chain</strong></td>
      <td style="text-align:right;"><strong>5.96 ± 0.19</strong></td>
      <td style="text-align:right;"><strong>55.22 ± 6.95</strong></td>
      <td style="text-align:right;">3191 ± 325</td>
      <td style="text-align:right;">0.482 ± 0.170</td>
      <td style="text-align:right;"><strong>−57.1 %</strong></td>
    </tr>
    <tr>
      <td>Max-Consensus — Centralized</td>
      <td style="text-align:right;">22.10 ± 1.09</td>
      <td style="text-align:right;">186.39 ± 30.10</td>
      <td style="text-align:right;"><strong>3627 ± 703</strong></td>
      <td style="text-align:right;"><strong>0.547 ± 0.116</strong></td>
      <td style="text-align:right;">+58.9 %</td>
    </tr>
  </tbody>
</table>

<p style="margin-top:6px; font-size:0.95rem;">
<strong>Interpretation.</strong> The proposed <em>Average Consensus + Extended Chain</em> achieves the lowest mean and worst-case delays with small variance, while the centralized Max-Consensus trades significantly higher delay for slightly higher throughput/fairness.
</p>

<div style="display:flex; flex-wrap:wrap; gap:15px; justify-content:center; margin-top:10px;">
  <img src="/portfolio/assets/images/consensus-signal-control/consensus_topology_avg_heatmap_100_runs.png" width="360" alt="Distribution of average waiting times across configurations">
  <img src="/portfolio/assets/images/consensus-signal-control/consensus_topology_comparison_heatmap_100_runs.png" width="360" alt="Heatmap of cross-metric performance across configurations">
</div>

<p style="text-align:center; margin-top:6px;">
  <em>Figures — Left: distribution of average waiting times. Right: cross-metric heatmap across consensus–topology pairs.</em>
</p>

---

## 2. Formulation (Key Equations)

**Per-vehicle and average waiting time**
\[
W_i = t_i^{\mathrm{dep}} - t_i^{\mathrm{arr}}, \qquad
\overline{W} = \frac{1}{N}\sum_{i=1}^{N} W_i.
\]

**Maximum waiting time**
\[
W^{\max} = \max_{i} W_i.
\]

**Jain’s fairness index** (queues per approach \(q_d\), directions set \(D\))
\[
J = \frac{\left(\sum_{d\in D} q_d\right)^2}{|D|\sum_{d\in D} q_d^2}, \quad J\in[0,1].
\]

**Priority score for movement \((d,m)\)**
\[
S_{d,m} = \alpha\,n_{d,m} \;+\; \beta\,w_d^{\max} \;+\; \gamma\,\bar{w}_d,
\]
with \(n_{d,m}\) (queue), \(\bar{w}_d\) (avg wait), \(w_d^{\max}\) (max wait), and tuned \(\alpha,\beta,\gamma\).

**Adaptive green time (selected non-conflicting set \(\mathcal{M}\))**
\[
Q=\sum_{(d,m)\in\mathcal{M}} n_{d,m},\qquad
\bar{w}=\frac{\sum_{(d,m)\in\mathcal{M}} \bar{w}_d\,n_{d,m}}{\max(Q,1)},
\]
\[
r=\min\!\Bigl(1,\tfrac{Q/|\mathcal{M}|}{10}\Bigr),\quad
u=\min\!\Bigl(1,\tfrac{\bar{w}}{30}\Bigr),\quad
\phi=0.7\,r+0.3\,u,
\]
\[
T_{\mathrm{green}} = T_{\min} + \phi\,(T_{\max}-T_{\min}).
\]

---

## 3. Architecture (Concise)
- **Distributed Consensus Layer:** vehicles exchange queue/wait data under a specified topology; we study **Centralized**, **Chain**, **Chain + Front-Priority**, and **Extended Chain**.
- **Adaptive Controller:** consumes the aggregated (consensus) summary and selects phases/green durations via the scores above.

<div style="text-align:center; margin:10px 0 0;">
  <img src="/portfolio/assets/images/consensus-signal-control/vehicle_topology_mode_1_fully_connected.png" width="650" alt="Fully connected / centralized topology schematic">
  <p style="margin-top:6px;"><em>Fully connected (ideal) topology, used as a performance reference.</em></p>
</div>

---

## 4. Discussion (Concise)
**Structured partial connectivity > full observability.** The Extended Chain’s front-vehicle cross-links deliver the most informative, low-latency signals to the controller without flooding.  
**Delay vs throughput trade-off.** Max-Consensus (Centralized) pushes capacity but inflates delay; our method prioritizes delay reduction with stable throughput/fairness.  
**Bandwidth efficiency.** Event-Triggered + Chain (not shown) offers strong message efficiency (≈159 msgs/hr) for constrained deployments.

---

## References / Documentation
- [Full Paper (PDF)](/assets/docs/Consensus_Driven.pdf)

<!-- MathJax (inline $...$ and display \[...\]) -->
<script>
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['\\[', '\\]'], ['$$','$$']]
    },
    svg: { fontCache: 'global' }
  };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js" async></script>
