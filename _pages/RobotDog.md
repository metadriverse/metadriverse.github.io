---
layout: research
permalink: /pvprobot/
title: "Human-in-the-loop Learning for Mobile Robots"
page_title: "Data-Efficient Learning from Human Interventions for Mobile Robots" 
authors:

- {name: "Zhenghao Peng", url: "https://pengzhenghao.github.io", institution: ""}
- {name: "Zhizheng Liu", url: "#", institution: ""}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io", institution: ""}

institutions:

- {name: "University of California, Los Angeles", institution: ""}


code_link: ""
nav: false
nav_order: 1
---

<style>
.video-container {
  position: relative;
  max-width: 100%; /* Adjust this value to control the maximum width of the video container */
  margin: 0 auto 0; /* Optional: center the video container horizontally */
}

.video-container video {
  display: block;
  margin: 0 auto;
  max-width: 100%;
  max-height: 100%;
}


.video-grid {
    display: grid;
    grid-template-columns: 1fr 1fr; /* Creates two columns */
    grid-gap: 20px; /* Space between videos */
}
.video iframe {
    width: 100%; /* Ensures iframe takes the full width of the container */
    height: 250px; /* Fixed height for all videos */
}

@media (max-width: 600px) {
    .video-grid {
        grid-template-columns: 1fr; /* Stacks videos into a single column on small screens */
    }
}
</style>




<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/pvprobot/TeaserVideoCompressed.mp4"></video>
</div>




<!--research-section-splitter-->



## Summary


:robot: We train two mobile robots with human-in-the-loop learning! Our method:

:star2: Learns from online human intervention and demonstration!

:star2: Trains from scratch in real world, without reward!


<!--research-section-splitter-->

## Human Following


We use a quadruped robot (Unitree Go2) to follow a human subject in a real-world environment.




<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/pvprobot/Compare_BC_Compressed.mp4"></video>
</div>







<!--research-section-splitter-->


## Safe Navigation


<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/pvprobot/Compare_BC_Nav_Compressed.mp4"></video>
</div>




<!--research-section-splitter-->


## Zero-shot Deployment

We have successfully deployed the learned policy to an unseen environment.

Safe Navigation:

<div class="video-container">
  <video style="width:80%;" loop controls muted playsinline src="../assets/img/pvprobot/Zeroshot_Nav_Compressed.mp4"></video>
</div>

<br>

Human Following:

<div class="video-container">
  <video style="width:80%;" loop controls muted playsinline src="../assets/img/pvprobot/Zeroshot_Dog_Following_Compressed.mp4"></video>
</div>




<!--research-section-splitter-->

## Full Training Footage


<div class="video-grid">
    <div class="video">
        <div id="video" style="overflow: hidden;">
          <iframe width="100%" height="100%" style="width: 101.5%; height: 101.5%; left: -0.5%; top: -0.5%;" src="https://www.youtube.com/embed/gRwfaxRFazM?autoplay=0&loop=1&mute=1&controls=1&rel=0&showinfo=0" frameborder="0" allowfullscreen="allowfullscreen"></iframe>
        </div>
    </div>
    <div class="video">
        <div id="video" style="overflow: hidden;">
          <iframe width="100%" height="100%" style="width: 101.5%; height: 101.5%; left: -0.5%; top: -0.5%;" src="https://www.youtube.com/embed/gUXpKF4wZrg?autoplay=0&loop=1&mute=1&controls=1&rel=0&showinfo=0" frameborder="0" allowfullscreen="allowfullscreen"></iframe>
        </div>
    </div>
</div>


<!--


<!--research-section-splitter-->


## Reference

**Proxy Value Propagation (NeurIPS 2023 Spotlight)**:
```plain
@article{peng2023learning,
  title={Learning from Active Human Involvement through Proxy Value Propagation},
  author={Peng, Zhenghao and Mo, Wenjie and Duan, Chenda and Li, Quanyi and Zhou, Bolei},
  journal={Advances in Neural Information Processing Systems},
  year={2023}
}   
```


<br>

**Acknowledgement**: TODOTODOTODOTODOTODOTODOTODOTODOTODOTODOTODOTODOTODOTODO 
This work was supported by the National Science Foundation under Grant No. 2235012. The human experiment in this study is approved through the IRB#23-000116 



<!--research-section-splitter-->


## Prior Works


**Expert Guided Policy Optimization (CoRL 2021)**:
Our research on human-in-the-loop policy learning began in 2021.
The first published work is [Expert Guided Policy Optimization (EGPO)](https://decisionforce.github.io/EGPO/).
In this work, we explored how an RL agent can benefit from the intervention of a PPO expert.


**Human-AI Copilot Optimization (ICLR 2022)**:
Building upon the methodology of EGPO, and substituting the PPO expert with a real human subject, we proposed [Human-AI Copilot Optimization (HACO)](https://decisionforce.github.io/HACO/) and it demonstrated significant improvements in learning efficiency over traditional RL baselines.


**Teacher-Student Shared Control (ICLR 2023)**:
In [Teacher-Student Shared Control (TS2C)](https://metadriverse.github.io/TS2C/), we examined the impact of using the value function as a criterion for determining when the PPO expert should intervene. The value function-based intervention makes it possible for the student agent to learn from a suboptimal teacher.


**Proxy Value Propagation (NeurIPS 2023 Spotlight)**: Considering the reward-free setting, we proposed several improvements to enhance learning from active human involvement.
These improvements address issues observed in HACO, including the jittering and oscillation of the learning agent, catastrophic forgetting, and challenges in learning sparse yet crucial behaviors.


-->