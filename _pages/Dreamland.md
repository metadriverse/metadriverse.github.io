---
layout: research
permalink: /dreamland/
title: "Dreamland: Controllable World Creation with Simulator and Generative Models"
page_title: "Dreamland: Controllable World Creation with Simulator and Generative Models"
authors:

- {name: "Sicheng Mo<sup>*</sup>", url: "https://sichengmo.github.io/"}
- {name: "Ziyang Leng<sup>*</sup>", url: "https://matthew-leng.github.io/"}
- {name: "Leon Liu", url: "#"}
- {name: "Weizhen Wang", url: "#"}
- {name: "Honglin He", url: "https://scholar.google.com/citations?user=Y0Qrwg0AAAAJ&hl"}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io/"}

institutions:

- {name: "<p>University of California, Los Angeles</p><sup>*</sup> Equal Contribution"}

nav: false
nav_order: 1
code_link: https://github.com/matthew-leng/Dreamland/
pdf_link: https://www.arxiv.org/abs/2506.08006

---

<style>
.video-container {
  position: relative;
  max-width: 100%; /* Adjust this value to control the maximum width of the video container */
   margin: 0 auto 0; /* Optional: center the video container horizontally */
}

.teaser {
  margin: 0 auto; /* Optional: center the video container horizontally */
}

.video-container video {
  display: block;
  margin: 0 auto;
  max-width: 100%;
  max-height: 100%;
}

/* .video-grid {
    margin-top: 18px;
    display: grid;
    grid-template-columns: 1fr 1fr; /* Creates two columns */
    grid-gap: 30px; /* Space between videos */
} */

.video-grid {
    margin-top: 18px;
    display: grid;
    grid-template-rows: 1fr 1fr 1fr; /* Two rows */
    grid-gap: 70px; /* Space between items */
    justify-items: center; /* Horizontally center items */
    align-items: center; /* Vertically center items */
}

.video-grid figure {
    display: flex;
    flex-direction: column; /* Stack video and caption */
    align-items: center; /* Center video and caption */
    justify-content: center; /* Center content */
    margin: 0; /* Reset default margin */
}

.video-grid video {
    display: block;
    width: 80%; /* Adjust as needed */
    height: auto; /* Maintain aspect ratio */
}

.video-section {
  margin-bottom: 60px;
}

video {
  width: 100%;
  /* max-width: 1000px; */
  height: auto;
  margin: 0 auto;
}

.dots {
  display: flex;
  justify-content: center;
  gap: 10px;
}

.dot {
  font-size: 24px;
  cursor: pointer;
  color: #aaa;
}

.dot.active {
  color: #333;
}

</style>

<div class="video-container">
  <video loop autoplay muted playsinline src="../assets/img/dreamland/control_sample_1.mp4"></video>
</div>


<!--research-section-splitter-->


## TL; DR

:national_park: **Dreamland** is a hybird generation pipeline that connects simulators and generative models to achieve controllable and configurable world creation.

:robot: **Dreamland** demonstrates great quality and controllability in scene generation, and improves the adaptation of embodied agents to the real world.


<!--research-section-splitter-->

<div style="display: grid; grid-template-columns: 1fr; gap: 0px; margin: 0 auto;">
  <figure style="display: flex; flex-direction: column; gap: 8px;">
    <figcaption style="text-align: center; font-size: 30px;">
        <strong>Simulator-Conditioned Generation</strong>
    </figcaption>
    <video id="videoPlayer1" style="display:block; width:100%; height:auto;" muted autoplay loop controls playsinline>
      <source src="../assets/img/dreamland/control_sample_2.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div class="dots" data-player="videoPlayer1">
      <span class="dot active" data-src="../assets/img/dreamland/control_sample_2.mp4">●</span>
      <span class="dot" data-src="../assets/img/dreamland/control_sample_1.mp4">●</span>
    </div>
  </figure>
  <figure style="display: flex; flex-direction: column; gap: 8px;">
  <figcaption style="text-align: center; font-size: 30px;">
        <strong>Diverse Scene Generation</strong>
    </figcaption>
    <video id="videoPlayer2" style="display:block; width:100%; height:auto;" muted autoplay loop controls playsinline>
      <source src="../assets/img/dreamland/text_sample_1.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div class="dots" data-player="videoPlayer2">
      <span class="dot active" data-src="../assets/img/dreamland/text_sample_1.mp4">●</span>
      <span class="dot" data-src="../assets/img/dreamland/text_sample_2.mp4">●</span>
      <span class="dot" data-src="../assets/img/dreamland/text_sample_3.mp4">●</span>
    </div>
  </figure>
  <figure style="display: flex; flex-direction: column; gap: 8px;">
  <figcaption style="text-align: center; font-size: 30px;">
        <strong>Safety-Critical Scene Generation</strong>
    </figcaption>
    <video id="videoPlayer3" style="display:block; width:100%; height:auto;" muted autoplay loop controls playsinline>
      <source src="../assets/img/dreamland/safe_sample_1.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div class="dots" data-player="videoPlayer3">
      <span class="dot active" data-src="../assets/img/dreamland/safe_sample_1.mp4">●</span>
      <span class="dot" data-src="../assets/img/dreamland/safe_sample_2.mp4">●</span>
    </div>
  </figure>
</div>

<script>
  document.querySelectorAll('.dots').forEach(dotContainer => {
    const videoId = dotContainer.getAttribute('data-player');
    const videoElement = document.getElementById(videoId);
    const dots = dotContainer.querySelectorAll('.dot');

    dots.forEach(dot => {
      dot.addEventListener('click', () => {
        const src = dot.getAttribute('data-src');
        videoElement.src = src;
        videoElement.play();
    
        dots.forEach(d => d.classList.remove('active'));
        dot.classList.add('active');
      });
    });
  });
</script>

<!-- <div style="border-top: 1px solid #ccc; margin: 30px 0;"></div> -->

<!--research-section-splitter-->
  
## Dreamland Architecture


<div class="img-container" style="width: 100%; margin: 5px auto;">
    <img src="../assets/img/dreamland/pipeline.png" class="my-image" alt="Image" />
</div>

Dreamland pipeline consists of three key stages: (1) *Stage-1 Simulation* : scene construction with physics-based simulator, (2) *Stage-2 LWA-Sim2Real* : transferring the Sim-LWA from simulation to Real-LWA with an instructional editing model and user instructions, (3) *Stage-3 Mixed-Condition Generation* : rendering an aesthetic and realistic scene with a large-scale pretrained image or video generation model

<!-- <div style="margin-bottom: 15px"></div> -->

<!--research-section-splitter-->

## Experiments

<figure style="display: flex; flex-direction: column; gap: 8px;">
  <img id="imageViewer4" src="../assets/img/dreamland/qual1.jpg" 
       style="display:block; width:100%; height:auto;" alt="Scene Image"/>

  <div class="dots" data-player="imageViewer4">
    <span class="dot active" data-src="../assets/img/dreamland/qual1.jpg">●</span>
    <span class="dot" data-src="../assets/img/dreamland/qual2.jpg">●</span>
    <span class="dot" data-src="../assets/img/dreamland/qual3.jpg">●</span>
    <span class="dot" data-src="../assets/img/dreamland/qual4.jpg">●</span>
  </div>
  </figure>

<script>
  document.querySelectorAll('.dots').forEach(dotContainer => {
    const imageId = dotContainer.getAttribute('data-player');
    const imageElement = document.getElementById(imageId);
    const dots = dotContainer.querySelectorAll('.dot');

    dots.forEach(dot => {
      dot.addEventListener('click', () => {
        const src = dot.getAttribute('data-src');
        imageElement.src = src;

        dots.forEach(d => d.classList.remove('active'));
        dot.classList.add('active');
      });
    });
  });
</script>


<div class="img-container" style="width: 60%; margin: 5px auto;">
    <img src="../assets/img/dreamland/experiments.png" class="my-image" alt="Image" />
</div>

Dreamland demonstrates great **quality** and **controllability**, with **scalability** that benefits from stronger pre-trained model deployed for *Stage-3*.

<!-- <div style="margin-bottom: 15px"></div> -->


<!--research-section-splitter-->


## Scene Editing
<div class="img-container" style="width: 90%; margin: 5px auto;">
    <img src="../assets/img/dreamland/editing.jpg" class="my-image" alt="Image" />
</div>

Dreamland supports editing a generated scene by adjusting the corresponding source scene.

<pre><code class="language-plain">@article{mo2025dreamland,
  title={Dreamland: Controllable World Creation with Simulator and Generative Models},
  author={Sicheng Mo and Ziyang Leng and Leon Liu and Weizhen Wang and Honglin He and Bolei Zhou},
  journal={Preprint},
  year={2025}
}
</code></pre>

<h3 style="margin-top: 30px">Acknowledgement</h3>
<a href="https://github.com/nvidia-cosmos/cosmos-predict1">Cosmos-Predict1</a> and <a href="https://github.com/nvidia-cosmos/cosmos-transfer1">Cosmos-Transfer1</a> were used as the base generation models for video results.


