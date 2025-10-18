---
layout: page
title: "Consensus-Driven Adaptive Signal Control"
permalink: /projects/consensus-signal-control/
---

<div style="display:flex; justify-content:flex-end; gap:15px; margin-bottom:10px;">
  <a href="/portfolio/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">🏠 Home / Portfolio</a>
  <a href="/projects/" style="font-weight:600; text-decoration:none; border:1px solid #ccc; padding:6px 12px; border-radius:6px;">📂 All Projects</a>
</div>

---

**Keywords:** consensus control, adaptive signal coordination, traffic optimization, scalability  

---

## Abstract / Overview
This study introduces a **hybrid two-layer signal control architecture** that integrates **localized consensus-based communication** with **centralized adaptive phase selection** to manage intersections efficiently under mixed traffic conditions.  
The approach employs a **front-priority weighted average consensus algorithm**, emphasizing vehicles nearest to intersections to enhance responsiveness. Structured through an **Extended Chain topology**, it eliminates communication bottlenecks while maintaining constant message load regardless of traffic density.  
Simulations demonstrate a **57.1% reduction in average waiting time** and a **53.3% reduction in worst-case delay**, validating the method’s scalability and robustness across 100 one-hour runs.

---

## 1. Introduction
Urban intersections suffer from inefficiencies in traditional centralized signal systems that rely on static timing and global observability. As cities transition to **mixed traffic**—combining human-driven, connected, and automated vehicles—signal control must adapt to uncertainty and limited connectivity.  
This work addresses these challenges through a **decentralized, scalable coordination framework**, bridging data-driven consensus algorithms with adaptive traffic control logic.

---

## 2. Methodology

### 2.1 Architecture
The proposed system features two cooperative layers:
1. **Distributed Consensus Layer:** Connected vehicles share queue and delay data through neighbor-to-neighbor communication governed by topology.  
2. **Adaptive Control Layer:** A central controller uses the aggregated consensus information to determine signal phases and green durations based on real-time demand.

This design achieves near-optimal control with constant computational and communication cost, even as vehicle count scales.

### 2.2 Consensus Algorithms
Four algorithmic families were evaluated:
- **Average Consensus** — smooth convergence and delay minimization.  
- **Max-Consensus (FloodMax)** — high throughput but fairness trade-offs.  
- **Event-Triggered Consensus** — efficient under bandwidth limits.  
- **Front-Priority Weighted Consensus** — prioritizes front vehicles to improve responsiveness.  

### 2.3 Communication Topologies
Four topologies were tested:
- **Centralized (Global Info)** — ideal reference model.  
- **Chain** — local V2V communication within each lane.  
- **Chain + Front Priority** — adds weighted messaging from front vehicles.  
- **Extended Chain** — introduces cross-links among leading vehicles, enabling rapid, low-latency updates across directions.

---

## 3. Results

<div style="display:flex; flex-wrap:wrap; gap:15px; justify-content:center;">
  <img src="/assets/img/consensus_topologies.png" width="340px" alt="Consensus communication topologies">
  <img src="/assets/img/consensus_metrics_radar.png" width="340px" alt="Performance metrics radar chart">
  <img src="/assets/img/consensus_boxplot.png" width="340px" alt="Box plot of average waiting times">
  <img src="/assets/img/consensus_heatmap.png" width="340px" alt="Heatmap of consensus-topology performance">
</div>

<p style="text-align:center; margin-top:8px;"><em>Figures 1–4. Comparison of topologies and consensus variants across performance metrics.</em></p>

**Quantitative Highlights:**
- **Average Consensus + Extended Chain:**  
  - ↓ 57.1 % average waiting time  
  - ↓ 53.3 % maximum waiting time  
  - Constant controller message load (independent of vehicle count)  
- **Max-Consensus + Centralized:** +8.9 % throughput, but +58.9 % waiting time (delay-throughput trade-off)  
- **Event-Triggered + Chain:** Balanced performance with minimal communication (≈ 159 msgs/hr)  

The Extended Chain topology consistently achieved the best mean and variance—**5.96 ± 0.19 s** average delay vs. **13.9 ± 0.64 s** baseline.

---

## 4. Discussion
This work demonstrates that **structured partial connectivity** can outperform full observability by filtering only spatially relevant information.  
The Extended Chain topology leverages **front-vehicle awareness**, providing real-time responsiveness with bounded message complexity.  
Event-triggered strategies, though less optimal in absolute delay, offer **superior bandwidth efficiency**, making them ideal for low-infrastructure deployments.  
These insights support a scalable migration path toward **decentralized, communication-efficient smart intersections**.

---

## 5. Conclusion
The **Consensus-Driven Adaptive Signal Control** framework merges distributed intelligence with centralized adaptivity to address scalability, fairness, and responsiveness.  
By combining **Average Consensus** algorithms with **spatially structured topologies**, it achieves superior delay reduction and stable operation under realistic communication constraints.  
This architecture provides a practical blueprint for the next generation of **connected-vehicle traffic management systems**.

---

## References / Documentation
- [Full Paper (PDF)](/assets/docs/Consensus_Driven.pdf)  
- [Simulation Repository](#)  
- [Dataset & Plots (Extended Results)](#)

---

## Acknowledgments
This research was conducted in collaboration with **KFUPM** and **Purdue University**, under faculty guidance and peer review.  
Special thanks to the **RISC Lab (KAUST)** for simulation discussions and the reviewers who supported early validation.

---

## Media
<div style="text-align:center;">
  <img src="/assets/img/consensus_poster_preview.jpg" width="700px" alt="Poster preview: Consensus-Driven Adaptive Signal Control">
  <p><a href="/assets/docs/Consensus_Driven.pdf" style="font-weight:600;">View full paper →</a></p>
</div>
