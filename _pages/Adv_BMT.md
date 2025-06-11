---
layout: research
permalink: /adv-bmt/
title: "Bidirectional Motion Transformer for Safety-Critical Traffic Scenario Generation"
page_title: "Adv-BMT: Bidirectional Motion Transformer for Safety-Critical Traffic Scenario Generation"
authors:

- {name: "Yuxin Liu<sup>*</sup>", institution: "1"}
- {name: "Zhenghao Peng<sup>*</sup>", url: "https://pengzhenghao.github.io", institution: "1"}
- {name: "Xuanhao Cui",  institution: "1"}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io", institution: "1"}

institutions:

- {name: "University of California, Los Angeles", institution: "1"}

nav: false
nav_order: 1
code_link: https://metadriverse.github.io/adv-bmt/
pdf_link: https://metadriverse.github.io/adv-bmt/

---



<style>
.video-container {
  position: relative;
  max-width: 100%; /* Adjust this value to control the maximum width of the video container */
  margin: 0px auto 0; /* Optional: center the video container horizontally */
}

.video-container video {
  display: block;
  margin: 0 auto;
  max-width: 100%;
  max-height: 100%;
}
</style>


<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/Adv-BMT/demo_1.mp4"></video>
</div>

<!--research-section-splitter-->


## TL; DR
:fire: **Adv-BMT** augments `diverse` and `realistic` collision interactions from a input real-world driving log.

:star2: **Adv-BMT** generates collision interactions through adversarial initializations + reverse motion predictions.

:blue_car: **Adv-BMT** can be leveraged as a closed-loop generator for reinforcement adversarial learnings.

<!--research-section-splitter-->



## Adv-BMT

<div class="img-container" style="width: 100%; margin: 0 auto;">
    <img src="../assets/img/Adv-BMT/Adv-BMT_teaser.png" class="my-image" alt="Image" />
</div>

Adv-BMT is a two-staged pipeline: first, it initializes diverse collision states between a new adversary agent and ego vehicle; then, it reconstructs the adversarial trajectories via BMT's reverse predictions. A rule-based rejection sampling mechanism is used to filter candidate trajectories from unsatisfactory adversarial initializations, and maintain realistic collision interactions. In the output, the new agent maintains realistic interactions with surrounding traffic.

<!--research-section-splitter-->



## BMT Architecture

<div class="img-container" style="width: 100%; margin: 0 auto;">
    <img src="../assets/img/Adv-BMT/BMT.png" class="my-image" alt="Image" />
</div>
BMT is a transformer-based motion prediction model, and is able to predict both future and history trajectories for vehicles, bicycles, and pedestrain agents.  
<!--research-section-splitter-->


## Diverse Adversarial Behaviors
<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/Adv-BMT/demo_2.mp4"></video>
</div>
<!--research-section-splitter-->


## Safer Agent via Adversarial Learnings
<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/Adv-BMT/Safer_Agent.mp4"></video>
</div>
<!--research-section-splitter-->



## Prior Works

**[CAT (CoRL 2022)](https://metadriverse.github.io/cat/)**:
Closed-loop adversarial training for safe end-to-end driving.

**[MetaDrive (TPAMI 2021)](https://metadriverse.github.io/metadrive/)**:
An open-source platform for large-scale traffic scenario simulation and modeling























