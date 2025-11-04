---
layout: research
permalink: /adv-bmt/
title: "Bidirectional Motion Transformer for Safety-Critical Traffic Scenario Generation"
page_title: "Adv-BMT: Bidirectional Motion Transformer for Safety-Critical Traffic Scenario Generation"
description: "<h3>NeurIPS 2025</h3>"
authors:

- {name: "Yuxin Liu<sup>*</sup>", institution: "1"}
- {name: "Zhenghao Peng<sup>*</sup>", url: "https://pengzhenghao.github.io", institution: "1"}
- {name: "Xuanhao Cui",  institution: "1"}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io", institution: "1"}

institutions:
- {name: "University of California, Los Angeles", institution: "1"}

nav: false
nav_order: 1
code_link: https://github.com/Yuxin45/Adv-BMT
pdf_link: https://arxiv.org/pdf/2506.09485

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
  <video loop autoplay muted playsinline src="../assets/img/Adv-BMT/demo_1_new.mp4"></video>
</div>

<!--research-section-splitter-->

## TL; DR
:blue_car: Adv-BMT for **data augmentation**: augments real-world driving logs with `realistic` and `diverse`  collision interactions.

:hammer_and_wrench: Adv-BMT is a **two-stage generation pipeline**: adversarial initialization + reverse motion prediction to produce plausible collision scenarios.

:motorway: Adv-BMT is an **adversarial scenario generator for closed-loop learning**: continuously produces diverse, realistic, collision-seeking interactions that target the ego vehicle.

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
  <video loop autoplay muted playsinline src="../assets/img/Adv-BMT/demo_2_1.mp4"></video>
</div>
<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/Adv-BMT/demo_2_2.mp4"></video>
</div>
<!--research-section-splitter-->


## Safer Agent via Adversarial Learnings
<div class="video-container" style="width: 60%; ">
  <video loop autoplay muted playsinline src="../assets/img/Adv-BMT/safer_agent_demo.mp4"></video>
</div>
<!--research-section-splitter-->

## Adversarial RL Evaluations in Waymo Environments
<div class="img-container" style="width: 60%; height: 120%; margin: 0 auto;">
    <img src="../assets/img/Adv-BMT/adv-bmt_waymo_eval.jpg" class="my-image" alt="Image" />
</div>


## Adversarial RL Evaluated in Safety-critical Environments
<div class="img-container" style="width: 60%; height: 120% ;margin: 0 auto;">
    <img src="../assets/img/Adv-BMT/adv-bmt_safety_critical_eval.jpg" class="my-image" alt="Image" />
</div>

<!--research-section-splitter-->



## Prior Works

**[CAT (CoRL 2022)](https://metadriverse.github.io/cat/)**:
Closed-loop adversarial training for safe end-to-end driving.

**[MetaDrive (TPAMI 2021)](https://metadriverse.github.io/metadrive/)**:
An open-source platform for large-scale traffic scenario simulation and modeling























