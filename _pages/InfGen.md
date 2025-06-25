---
layout: research
permalink: /infgen/
title:  "InfGen: Scenario Generation as Next-Token-Group Prediction"
page_title: "InfGen: Scenario Generation as Next-Token-Group Prediction"
authors:
  - {name: "Zhenghao Peng<sup>*</sup>", url: "https://pengzhenghao.github.io/"}
  - {name: "Yuxin Liu<sup>*</sup>",  url: "#"}
  - {name: "Bolei Zhou",            url: "https://boleizhou.github.io/"}
institutions:
    - {name: "<p>University of California, Los Angeles</p>"}
nav: false
nav_order: 1
code_link: https://github.com/metadriverse/infgen
pdf_link:  https://arxiv.org/abs/2506.XXXX   # ← update when live
---

<!-- ----------  GLOBAL VIDEO / IMAGE STYLE  ---------- -->
<style>
.video-container{position:relative;max-width:100%;margin:0 auto;}
.video-container video{display:block;margin:0 auto;max-width:100%;height:auto;}
.video-grid{margin-top:18px;display:grid;grid-template-rows:1fr 1fr 1fr;grid-gap:70px;
            justify-items:center;align-items:center;}
.video-grid figure{display:flex;flex-direction:column;align-items:center;justify-content:center;margin:0;}
.video-grid video{display:block;width:80%;height:auto;}
.dots{display:flex;justify-content:center;gap:10px;}
.dot{font-size:24px;cursor:pointer;color:#aaa;}
.dot.active{color:#333;}
</style>

<!-- ---------------- TEASER ---------------- -->
<div class="video-container">
  <!-- Replace with a short 8-10 s teaser clip that shows InfGen rolling out agents -->
  <video loop autoplay muted playsinline src="../assets/img/infgen/teaser.mp4"></video>
</div>

TODO: TEASER VIDEO PENDING...

<!--research-section-splitter-->

## TL;DR  
 **InfGen** is a unified transformer that treats the entire driving scene—map, lights, agent states and motions—as one long token stream and rolls it out autoregressively.  


&nbsp;
&nbsp;
:traffic_light:
Generates both initial states and trajectories in a single model, eliminating two-stage pipelines.

&nbsp;
&nbsp;
:mag: Supports *dynamic agent injection* for open-world, long-horizon simulation 

&nbsp;
&nbsp;
:rocket: RL planners trained in InfGen scenes show ↑ robustness & generalization over log-replay baselines

<!--research-section-splitter-->

<div style="display:grid;grid-template-columns:1fr;gap:0px;margin:0 auto;">
  <figure>
    <figcaption style="text-align:center;font-size:30px;"><strong>
Scenario Generation
</strong>
</figcaption>
    <video id="videoPlayer1" muted autoplay loop controls playsinline>
      <source src="../assets/img/infgen/rollout_0.mp4" type="video/mp4">
    </video>
  </figure>
</div>

TODO: VIDEO PENDING...


<div style="display:grid;grid-template-columns:1fr;gap:0px;margin:0 auto;">
  <figure>
    <figcaption style="text-align:center;font-size:30px;"><strong>
Scenario Densification
</strong>
</figcaption>
    <video id="videoPlayer1" muted autoplay loop controls playsinline>
      <source src="../assets/img/infgen/rollout_0.mp4" type="video/mp4">
    </video>
  </figure>
</div>

TODO: VIDEO PENDING...

<!--research-section-splitter-->

## InfGen Architecture

TODO: IMAGE PENDING...

InfGen encodes up to 3 000 lane-segment *map tokens* with a lightweight encoder, then autoregressively decodes traffic-light, agent-state, and motion tokens with group-causal attention :contentReference[oaicite:3]{index=3}.  
The single model thus produces **where** each agent appears *and* **how** it moves, while allowing new agents to enter at any timestep.

<!--research-section-splitter-->

## Experiments


TODO: Table pending... Text revision...



InfGen achieves the lowest initial-state MMD and dynamic-collision rate on WOMD, and planners trained in InfGen scenes sustain performance under 4× traffic density.


RL Exp results..




<!--


<!--research-section-splitter-->


## BibTeX
<pre><code class="language-plain">@article{peng2025infgen,
  title   = {InfGen: Scenario Generation as Next Token Group Prediction},
  author  = {Zhenghao Peng and Yuxin Liu and Bolei Zhou},
  journal = {NeurIPS},
  year    = {2025},
  url     = {https://metadriverse.github.io/infgen}
}
</code></pre>
-->