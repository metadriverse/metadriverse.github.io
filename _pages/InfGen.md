---
layout: research
permalink: /infgen/
title:  "InfGen: Scenario Generation as Next-Token-Group Prediction"
page_title: "InfGen: Scenario Generation as Next-Token-Group Prediction"
authors:
  - {name: "Zhenghao Peng", url: "https://pengzhenghao.github.io/"}
  - {name: "Yuxin Liu",  url: "#"}
  - {name: "Bolei Zhou",            url: "https://boleizhou.github.io/"}
institutions:
    - {name: "<p>University of California, Los Angeles</p>"}
nav: false
nav_order: 1
code_link: https://github.com/metadriverse/infgen
pdf_link: https://arxiv.org/pdf/2506.23316
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




<div class="img-container" style="width: 60%; margin: auto auto;">
    <img src="../assets/img/infgen/teaser.png" class="my-image" alt="Image" />
</div>


 **InfGen** is a unified transformer that treats the entire driving scene—map, lights, agent states and motions—as one long token stream and rolls it out autoregressively.  


&nbsp;
&nbsp;
:traffic_light:
Generates both initial states, traffic light signals, and traffic participant trajectories in a single model.

&nbsp;
&nbsp;
:mag: Supports dynamic agent injection for open-world, long-horizon simulation.

&nbsp;
&nbsp;
:rocket: Autonomous driving planners trained in InfGen scenarios show ↑ robustness & generalization over log-replay baselines.


<!--research-section-splitter-->

<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/infgen/infgen_generated_scenario.mp4"></video>
</div>


<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/infgen/infgen_densified_scenario.mp4"></video>
</div>


<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/infgen/infgen_densified_and_extended_scenario.mp4"></video>
</div>


<!--research-section-splitter-->

<pre><code class="language-plain">@article{peng2025infgen,
  title={InfGen: Scenario Generation as Next Token Group Prediction},
  author={Peng, Zhenghao and Liu, Yuxin and Zhou, Bolei},
  journal={arXiv preprint arXiv:2506.23316},
  year={2025}
}
</code></pre>