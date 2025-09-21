---
layout: research
permalink: /s2e/
title: "From Seeing to Experiencing: Scaling Navigation Foundation Models with Reinforcement Learning"
page_title: "From Seeing to Experiencing: Scaling Navigation Foundation Models with Reinforcement Learning"
authors:
- {name: "Honglin He<sup>*</sup>", url: "https://wywu.github.io/"}
- {name: "Yukai Ma<sup>*</sup>", url: "https://yukai-ma.github.io/"}
- {name: "Wayne Wu", url: "https://wywu.github.io/"}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io/"}

institutions:
- {name: "University of California, Los Angeles"}

nav: false
nav_order: 1
code_link: https://github.com/metadriverse/S2E
pdf_link: https://arxiv.org/pdf/2507.22028

---
<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/s2e/s2e.mp4"></video>
</div>

<div class="research-section">
    <h3 style="text-align: center">TL;DR</h3>
    <ul style="list-style-type: none; padding-left: 0;">
      <strong>S2E</strong> is a <em>unified</em> learning framework that scales navigation foundation models from passive offline video to interactive decision-making through reinforcement learning.<br><br>
    1. 📦 Provides a general framework for learning navigation from both offline data and online interaction.<br>
    2. 🔌 Introduces a plug-and-play <strong>Residual-Attention Module</strong> for efficient adaptation and scaling in RL.<br>
    3. 🧭 Releases <strong>NavBench-GS</strong>, a realistic 3D Gaussian Splatting benchmark for evaluating navigation performance in closed-loop, interactive, and physically grounded environments.
  </ul>
</div>


<div class="research-section">
    <h3 style="text-align: center">S2E Model Architecture</h3>
  
    <img src="../assets/img/s2e/s2e_model.png" alt="navbench-gs" style="display: block; margin: 10px auto; width: 100%; height: auto;" />
    
    <p style="margin-top: 5px;">
    S2E pipeline consists of two key components:<br>
    (1) Anchor-Guided Distribution Matching (AGDM): A framework that uses anchor-conditioned architecture to learn multi-modal trajectory distributions from offline real-world videos, improving model capability from the side of representation.<br>
    (2) Residual Attention Module (RAM): A lightweight residual design that fine-tunes pretrained attention blocks via reinforcement learning in simulation, enabling new behaviors (e.g., obstacle avoidance) while preserving general visual-motor priors.
     </p>
</div>

<div class="research-section">
    <h3 style="text-align: center">Environments for Pretraining and Finetuning</h3>

    <h4 style="text-align: center">Pretraining on Video Datasets</h4>
    <video style="display:block; width:100%; height:auto;" autoplay="autoplay" muted loop="loop" controls playsinline><source src="../assets/img/s2e/pretrain.mp4" type="video/mp4"/> </video>

    <h4 style="text-align: center">Finetuning on URBAN-SIM Simulator</h4>
    <video style="display:block; width:100%; height:auto;" autoplay="autoplay" muted loop="loop" controls playsinline><source src="../assets/img/s2e/finetune.mp4" type="video/mp4"/> </video>
    
</div>


<div class="research-section">
    <h3 style="text-align: center">NavBench-GS: Closed-Loop 3DGS Navigation Benchmark</h3>
    
    <video style="display:block; width:100%; height:auto;" autoplay="autoplay" muted loop="loop" controls playsinline><source src="../assets/img/s2e/navbench_gs.mp4" type="video/mp4"/> </video>

    <img src="../assets/img/s2e/navben_gs.png" alt="navbench-gs" style="display: block; margin: 10px auto; width: 100%; height: auto;" />

    <p style="margin-top: 5px;">
        We build NavBench-GS, a 3D Gaussian Splatting-based benchmark for evaluating navigation policies in closed-loop, visually reconstructed urban environments with simulated objects and pedestrians.
    </p>
    
</div>

<div class="research-section">
    <h3 style="text-align: center">Real World Deployment</h3>

    <video style="display:block; width:100%; height:auto;" autoplay="autoplay" muted loop="loop" controls playsinline><source src="../assets/img/s2e/obstacles.mp4" type="video/mp4"/> </video>
    <p style="text-align: center; margin-top: 5px;">
    Scenarios with Static Obstacles
    </p>
    
    <video style="display:block; width:100%; height:auto;" autoplay="autoplay" muted loop="loop" controls playsinline><source src="../assets/img/s2e/pedestrians.mp4" type="video/mp4"/> </video>
    <p style="text-align: center; margin-top: 5px;">
    Scenarios with Dynamic Pedestrians
    </p>

    <video style="display:block; width:100%; height:auto;" autoplay="autoplay" muted loop="loop" controls playsinline><source src="../assets/img/s2e/longnav.mp4" type="video/mp4"/> </video>
    <p style="text-align: center; margin-top: 5px;">
    Long-Horizon Navigation
    </p>

    <video style="display:block; width:100%; height:auto;" autoplay="autoplay" muted loop="loop" controls playsinline><source src="../assets/img/s2e/comparisons.mp4" type="video/mp4"/> </video>
    <p style="text-align: center; margin-top: 5px;">
    Comparison with SOTAs
    </p>
    
</div>



<div class="research-section">
<h3 style="text-align: center">Acknowledgement</h3>
<p>
We extend our gratitude for the excellent assets, including 3D objects from Objaverse-XL, 3D humans from SynBody, and robots from IsaacLab. Thank <a href="https://www.cocodelivery.com/" target="_blank">COCO Robot</a> for donating virtual and physical robots.
</p>
</div>


<div class="research-section">
<h3 style="text-align: center">Reference</h3>

<pre><code class="language-plain">@article{he2025from,
  title={From Seeing to Experiencing: Scaling Navigation Foundation Models with Reinforcement Learning},
  author={He, Honglin and Ma, Yukai and Wu, Wayne and Zhou, Bolei},
  journal={arXiv preprint arXiv:2507.22028},
  year={2025}
}
</code></pre>
</div>


<style>
.custom-heading {
  font-size: 1.5em;
  font-weight: bold;
  margin-bottom: 10px; /* Adjust this value as needed */
}
.white-background {
    background-color: white;
    display: block; /* Changed from inline-block if you want it to take the full width available */
    width: 100%; /* Ensures it takes the full width of its parent container */
    overflow: hidden; /* This will prevent any overflow outside this div */
    padding: 10px;
}
.white-background img {
    width: 100%; /* Makes the image responsive */
    height: auto; /* Keeps the image's aspect ratio intact */
}
.logo {
    display: inline; /* Changed from inline-block if you want it to take the full width available */
    width: 100%; /* Ensures it takes the full width of its parent container */
    overflow: hidden; /* This will prevent any overflow outside this div */
    padding: 10px;
}
.logo img {
    width: 100%; /* Makes the image responsive */
    height: auto; /* Keeps the image's aspect ratio intact */
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

@media (max-width: 600px) {
    .video-grid {
        grid-template-columns: 1fr; /* Stacks videos into a single column on small screens */
    }
}
.gif img {
    width: 100%; /* Ensures the GIFs fill the cells */
    height: auto; /* Maintains the aspect ratio */
}
</style>



