---
layout: research
permalink: /pvp4real/
title: "Data-Efficient Learning from Human Interventions for Mobile Robots"
page_title: "Data-Efficient Learning from Human Interventions for Mobile Robots" 
authors:

- {name: "Zhenghao Peng", url: "https://pengzhenghao.github.io", institution: ""}
- {name: "Zhizheng Liu", url: "#", institution: ""}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io", institution: ""}

institutions:

- {name: "University of California, Los Angeles", institution: ""}


description: "<h3>ICRA 2025</h3>"
pdf_link: https://arxiv.org/pdf/2503.04969
code_link: https://github.com/metadriverse/pvp4real
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


## TL; DR


We train two mobile robots in real world in real time :robot: via human-in-the-loop learning! Our method:

:star2: Learns from online human intervention and demonstration!

:star2: Trains from scratch, without reward!


<!--research-section-splitter-->


## Safe Navigation


A delivery robot (Unitree Go2) learns to navigate safely in a real-world environment, avoiding collisions with static or dynamic obstacles.
Even though the observation is RGB-D image, training can be done in 20 minutes and the robot can generalize to unseen environments.

<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/pvprobot/Compare_BC_Nav_Compressed.mp4"></video>
</div>


<!--research-section-splitter-->

## Human Following


We train a quadruped robot (Unitree Go2) to follow a human subject in a real-world environment.
Training is completed within 10 minutes.

<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/pvprobot/Compare_BC_Compressed.mp4"></video>
</div>


<!--research-section-splitter-->


## Zero-shot Deployment

We have successfully deployed the learned policies to unseen environments.

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



<div class="research-section">
<h3 style="text-align: center">Reference</h3>

<pre><code class="language-plain">@article{peng2025data,
  title={Data-Efficient Learning from Human Interventions for Mobile Robots},
  author={Peng, Zhenghao and Liu, Zhizheng and Zhou, Bolei},
  journal={arXiv preprint arXiv:2503.04969},
  year={2025}
}
</code></pre>
</div>



