---
layout: research
permalink: /vid2sim/
title: "Vid2Sim: Realistic and Interactive Simulation from Video for Urban Navigation"
page_title: "Vid2Sim: Realistic and Interactive Simulation from Video for Urban Navigation"
authors:

- {name: "Ziyang Xie", url: "https://ziyangxie.site/", institution: "1,2"}
- {name: "Zhizheng Liu", url: "#", institution: "1"}
- {name: "Zhenghao Peng", url: "https://pengzhenghao.github.io", institution: "1"}
- {name: "Wayne Wu", url: "https://wywu.github.io/", institution: "1"}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io/", institution: "1"}

institutions:

- {name: "University of California, Los Angeles", institution: "1"}
- {name: "University of Illinois Urbana-Champaign", institution: "2"}


nav: false
nav_order: 1
# code_link: https://github.com/
# pdf_link: https://arxiv.org/abs/

---



<!---
<div class="img-container" style="width: 100%; margin: 0 auto;">
    <img src="../assets/img/simgen/teaser.png" class="my-image" alt="Image" />
</div>
slides_link: https://docs.google.com/presentation/d/1X1nB9umPlWtNfuUjZObO6UNyyBUbgHogVJA4bCaMiKQ/edit?usp=sharing
--->


<style>
.video-container {
  position: relative;
  max-width: 100%; /* Adjust this value to control the maximum width of the video container */
}

.teaser {
  margin: -20px auto -20px; /* Optional: center the video container horizontally */
}

.video-container video {
  display: block;
  margin: 0 auto;
  max-width: 100%;
  max-height: 100%;
}

.video-grid {
    margin-top: 20px;
    display: grid;
    grid-template-columns: 1fr 1fr; /* Creates two columns */
    grid-gap: 30px; /* Space between videos */
}

</style>

<div class="video-container teaser">
  <video loop controls autoplay muted playsinline src="../assets/img/vid2sim/Vid2Sim_long.mp4"></video>
</div>



<!---
<div class="embed-responsive embed-responsive-21by9">
    <video width="100%" max-width="800px" loop autoplay muted playsinline src="../assets/img/simgen/SimGenWide.mp4">
    </video>
</div>
--->


<!--research-section-splitter-->


## TL; DR

:selfie: **Vid2Sim** can convert real-world monocular videos into `realistic` and `interactive` digital-twin environments in simulation for urban navigation training.

:robot: **Vid2Sim** enables reinforcement learning agents to learn navigation policies in diverse realistic simulation scenarios, where the learned policies can be directly deployed on real-world robots with minimal `sim-to-real gap`.  

<div style="border-top: 1px solid #ccc; margin: 30px 0;"></div>

## Vid2Sim Architecture


<div class="img-container" style="width: 100%; margin: 5px auto;">
    <img src="../assets/img/vid2sim/pipeline.png" class="my-image" alt="Image" />
</div>

Vid2Sim framework consists of three key stages: (1) **Geometry-consistent reconstruction** for high-quality real-to-sim environment creation, (2) building a **realistic and interactive simulation** with hybrid scene representation and diverse obstacle and scene augmentation for urban navigation training, and (3) zero-shot **sim-to-real deployment** in the real world to verify our pipeline's effectiveness.

<div style="margin-bottom: 15px"></div>

## Interactive Scene Composition
<div class="img-container" style="width: 100%; margin: 5px auto;">
    <img src="../assets/img/vid2sim/scene_composition.png" class="my-image" alt="Image" />
</div>

Vid2Sim facilitates augmented real-to-sim environment creation through interactive scene composition, including varied **static obstacles** and other **dynamic agents**. This approach enables the generation of **diverse**, **controllable** and **safty critical** corner cases for safe urban navigation training.


<div style="border-top: 1px solid #ccc; margin: 30px 0;"></div>

## Real2Sim Navigation Training
We train and test our agents in diverse realistic real2sim environments with augmented static obstacles and dynamic agents. (Bottom-right is the agent's view)
<div class="video-grid">
    <div>
        <video style="display:block; width:100%; height:auto;" muted controls playsinline>
        <source src="../assets/img/vid2sim/simulation/sim_nav1.mp4" type="video/mp4">
        </video>
    </div>
    <div>
        <video style="display:block; width:100%; height:auto;" muted controls playsinline>
        <source src="../assets/img/vid2sim/simulation/sim_nav2.mp4" type="video/mp4">
        </video>
    </div>
</div>

<br>

## Zero-shot Sim2Real Deployment
After training in real2sim environments, we deploy our agents to the real world in a zero-shot manner. This demonstrates the effectiveness of our Vid2Sim pipeline in bridging the sim-to-real gap.  

* *Note: Our policies only take `RGB` images as visual observation and deployed in the real world without any fine-tuning*
<div class="video-grid">
    <div>
        <figure>
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
                <source src="../assets/img/vid2sim/realworld/realworld_nav1.mp4" type="video/mp4">
            </video>
            <figcaption style="text-align:center; margin-top:8px; font-size:14px;">
                Static & Dynamic Obstacles Avoidance
            </figcaption>
        </figure>
    </div>

    <div>
        <figure>
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
                <source src="../assets/img/vid2sim/realworld/realworld_nav2.mp4" type="video/mp4">
            </video>
            <figcaption style="text-align:center; margin-top:8px; font-size:14px;">
                Sudden Pedestrian Cut-in
            </figcaption>
        </figure>
    </div>
</div>

## Real2Sim Digital-Twin 
We show our Vid2Sim pipeline could generate realistic digital-twin environments for realworld scenes. The digital-twin environment is controllable as well as interactive and can be used for both policy training and evaluation navigation policies. 
<div class="img-container" style="width: 85%; margin: 5px auto;">
    <img src="../assets/img/vid2sim/digital-twin.png" class="my-image" alt="Image" />
</div>

<div style="border-top: 1px solid #ccc; margin: 30px 0;"></div>

## Diverse Environment Augmentation
Vid2Sim can further support controllable scene editing and advanced weather simulation through 3D scene editing and particle system simulation. This enables more robust and generalizable policy training under different lighting and weather conditions.

<h4 style="text-align: center; margin-bottom: 0px">Global 3D Scene Editing</h4>
<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/vid2sim/editing/augment.m4v"></video>
</div>


<h4 style="text-align: center; margin-bottom: 10px">Weather Simulation</h4>
<div class="video-grid">
    <div>
        <figure>
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
                <source src="../assets/img/vid2sim/editing/rain.mp4" type="video/mp4">
            </video>
            <figcaption style="text-align:center; margin-top:8px; font-size:14px;">
                Rain Simulation
            </figcaption>
        </figure>
    </div>

    <div>
        <figure>
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
                <source src="../assets/img/vid2sim/editing/fog.mp4" type="video/mp4">
            </video>
            <figcaption style="text-align:center; margin-top:8px; font-size:14px;">
                Fog Simulation
            </figcaption>
        </figure>
    </div>
</div>

<div style="border-top: 1px solid #ccc; margin: 30px 0;"></div>

## Scalable Real2Sim Environments

We curate a dataset of 30 diverse real-to-sim (real2sim) environments from web sourced videos for urban navigation training. We further evaluate the generalizability improvement of our agents as the number of the training environment increase.

<h4 style="text-align: center; margin-bottom: 15px">Environments Gallery</h4>
<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/vid2sim/gallery.mp4"></video>
</div>

<br>

<h4 style="text-align: center; margin-bottom: 15px">Generalizability Results</h4>
<div class="img-container" style="width: 80%; margin: 0 auto;">
    <img src="../assets/img/vid2sim/generalize.png" class="my-image" alt="Image" />
</div>

This table compares (a) the success rate (SR) and (b) success rate weighted by path length (SPL) across varying numbers of training environments. Increasing the number of training environments leads to a higher test success rate and SPL, which indicates improved agents generalizability.

<br>

<div style="border-top: 1px solid #ccc; margin: 20px 0;"></div>

<h3 style="text-align: center">Reference</h3>

<pre><code class="language-plain">@article{xie2024vid2sim,
  title={Vid2Sim: Realistic and Interactive Simulation from Video for Urban Navigation},
  author={Ziyang Xie and Zhizheng Liu and Zhenghao Peng and Wayne Wu and Bolei Zhou},
  journal={Preprint},
  year={2024}
}
</code></pre>