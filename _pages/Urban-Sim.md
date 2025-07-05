---
layout: research
permalink: /urbansim/
title: "Towards Autonomous Micromobility through Scalable Urban Simulation"
page_title: "Towards Autonomous Micromobility through Scalable Urban Simulation"
description: "<h3 style='color:red'>CVPR 2025 Highlight</h3><h3 style='color:black'>RSS MoMa Workshop, 2025</h3>"
authors:
  - {name: "Wayne Wu<sup>*</sup>", url: "https://wywu.github.io/", institution: "1"}
  - {name: "Honglin He<sup>*</sup>", url: "https://scholar.google.com/citations?user=Y0Qrwg0AAAAJ&hl", institution: "1"}
  - {name: "Chaoyuan Zhang", url: "#", institution: "2"}
  - {name: "Jack He", url: "https://jackhe313.github.io/", institution: "1"}
  - {name: "Seth Z. Zhao", url: "https://sethzhao506.github.io/", institution: "1"}
  - {name: "Ran Gong", url: "https://nikepupu.github.io/", institution: "1"}
  - {name: "Quanyi Li", url: "https://quanyili.github.io/", institution: "1"}
  - {name: "Bolei Zhou", url: "https://boleizhou.github.io/", institution: "1"}
institutions:
- {name: "University of California, Los Angeles", institution: "1"}
- {name: "University of Washington", institution: "2"}
nav: false
nav_order: 1
pdf_link: "http://arxiv.org/abs/2505.00690"
code_link: "https://github.com/metadriverse/urban-sim"

---
<!-- TL;DR Section -->
<div class="research-section">
    <ol style="list-style-position: inside">
      <strong>TL;DR</strong>: A solution to support <u>scalable robot learning in urban spaces</u>. <br>
      It consists of two components:
    <li><strong><span class="special-font">URBAN-SIM</span></strong> -- a large-scale robot learning platform built upon NVIDIA's Omniverse for reinforcement learning.</li>
    <li><strong><span class="special-font">URBAN-BENCH</span></strong> -- a holistic benchmark for foundational tasks like urban locomotion and navigation and comprehensive tasks like urban traversal.</li>
    </ol>
</div>

<!-- Introducing Urban-X -->
<div class="research-section">

<div class="white-background">
    <video style="display:block; width:100%; height:auto;" autoplay loop muted controls playsinline>
        <source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/img/urbanSim/urbansim_teaser.mp4" type="video/mp4"/>
    </video>
</div>
    
</div>

<!-- Micromobility Definition -->
<div class="research-section">
  <h3 style="text-align: center"><strong>What is Micromobility?</strong></h3>
  <p>Micromobility is a promising urban transport way for <u>short-distance travel</u>. <br>
  The figure below shows different alternates to car ownership categorized by trip length, where we focus on the short distance trips with micro-mobility devices.</p>
  <div class="white-background">
    <img src="/assets/img/urbanSim/micromobility.png" alt="Trip length vs transportation mode">
  </div>
</div>

<div class="research-section">
  <h3 style="text-align: center"><strong>What is a Micromobility Device?</strong></h3>
  <p>Micromobility Device encompasses two forms of machines:</p>
  <ol>
    <li> <u>Mobile robots</u>: wheeled, quadruped, wheeled-legged, humanoid robots, etc.</li>
    <li><u>Assistive mobility devices</u>: electric wheelchairs, mobility scooters, intelligent scooter, autonomous bicycles, etc.</li>
  </ol>
  <div class="white-background">
    <img src="/assets/img/urbanSim/device.png" alt="Micromobility Devices">
  </div>
</div>

<!-- URBAN-SIM -->
<div class="research-section">
  <h3 style="text-align: center"><strong>Why <span class="special-font">URBAN-SIM</span>?</strong></h3>
  <p>Previous simulation platforms can be categorized into two classes:</p>
  <ul>
    <li>Robot learning platforms (e.g., IsaacGym and IsaacLab):   ✅ High Performance ❌ Rich Scene Context</li>
    <li>Autonomous driving platforms (e.g., CARLA and MetaDrive): ❌ High Performance ✅ Rich Scene Context</li>
  </ul>
  <p><span class="special-font">URBAN-SIM</span> can achieve both two characteristics that are critical for robot learning in urban spaces:</p>
  <ul>
    <li>✅ High Performance: up to 2,600 fps on a single GPU - > support <u>high-efficient RL training</u>.</li>
    <li>✅ Rich Scene Context: infinite urban scene generation - > support <u>scene-aware tasks</u> such as visual locomotion, navigation and Vision-Language Action (VLA) model training, and broad  interaction tasks between robot, human and scene.</li>
  </ul>
  <p><strong>In a nutshell, <span class="special-font">URBAN-SIM</span> can make robot learning <u>scalable</u>: robots can be trained on an infinite number of diverse scenes with any number of GPUs.</strong></p>
</div>

<div class="research-section">
  <h3 style="text-align: center"><strong>What is <span class="special-font">URBAN-SIM</span>?</strong></h3>
  <p><span class="special-font">URBAN-SIM</span> is a high-performance robot learning platform for autonomous micromobility.  It can automatically construct infinite <i>diverse</i> and <i>realistic</i> interactive urban scenes for large-scale robot learning while providing up to 2,600 fps high simulation performance with large-scale parallelization in a single Nvidia L40S GPU.</p>

  <div class="video">
            <video style="display:block; width:100%; height:auto;" autoplay loop muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/img/urbanSim/training.mp4" type="video/mp4"/></video>
  </div>
  <br>
  <h6 style="text-align: center">Robot Training on Different Scales of Generated Scenes</h6>

</div>

<div class="research-section">
  <h3 style="text-align: center"><strong>Evaluation in Simulator</strong></h3>
  <p>With large-scale training on <span class="special-font">URBAN-SIM</span>, robots with different embodiments emerge different behaviors in same test environments.</p>

  <div class="video">
            <video style="display:block; width:100%; height:auto;" autoplay loop muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/img/urbanSim/evaluation_1.mp4" type="video/mp4"/></video>
  </div>
  <br>
</div>

<div class="research-section">
  <h3 style="text-align: center"><strong>Evaluation in Real World</strong></h3>
  <p>With large-scale training on <span class="special-font">URBAN-SIM</span>, policies can be deployed in unseen real-world environments.</p>

  <div class="video">
            <video style="display:block; width:100%; height:auto;" autoplay loop muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/img/urbanSim/real_world.mp4" type="video/mp4"/></video>
  </div>
  <br>
</div>

<div class="research-section">
  <h3 style="text-align: center"><strong>VR Interface</strong></h3>
  <p>In <span class="special-font">URBAN-SIM</span>, we provide VR interface for 1) demonstration data collection for imitation learning, and 2) flexible scene editing.</p>

  <div class="video">
            <video style="display:block; width:100%; height:auto;" autoplay loop muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/img/urbanSim/data_collect.mp4" type="video/mp4"/></video>
  </div>
  <br>
  <h6 style="text-align: center">Immersive Data Collection in Urban Scenes</h6>

  <br>

  <div class="video">
            <video style="display:block; width:100%; height:auto;" autoplay loop muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/img/urbanSim/customization.mp4" type="video/mp4"/></video>
  </div>
  <br>
  <h6 style="text-align: center">Immersive Urban Scene Customization</h6>


</div>

<!-- URBAN-BENCH -->
<div class="research-section">
  <h3 style="text-align: center"><strong>Why <span class="special-font">URBAN-BENCH</span>?</strong></h3>
  <p>Existing AI solutions often focus on isolated robot skills — like obstacle avoidance, goal reaching, or parkour. However, real-world urban tasks demand <b>versatile and integrated capabilities</b> for end-to-end operation.
  <br>
  <br>
  
  Take, for example, a robot dog navigating from a coffee shop to a campus building. It must climb up and down curbs and stairs, avoid collisions with pedestrians and sidewalk clutter, and traverse narrow or crowded spaces — sometimes requiring human teleoperation in risky scenarios. All these skills must work together to ensure one successful journey.
  <br>
  <br>
  
  To support research in this emerging domain of autonomous micromobility, and to standardize evaluation practices, we introduce <span class="special-font">URBAN-BENCH</span>. It spans both foundational tasks -- urban locomotion and navigation, and the comprehensive challenge of kilometer-scale urban traversal, all set in diverse and realistic city environments.
  </p>
</div>

<div class="research-section">
  <h3 style="text-align: center"><strong>What is <span class="special-font">URBAN-BENCH</span>?</strong></h3>
  <p><span class="special-font">URBAN-BENCH</span> is a suite of essential tasks and benchmarks to train and evaluate different capabilities of robots. We propose three tasks across eight scenarios on four robots - including wheeled robot (COCO Robotics' delivery robot), a quadruped robot (Unitree Go2), a wheeled-legged robot (Unitree B2-W), and a humanoid robot (Unitree G1).</p>

  <div class="white-background">
    <img src="/assets/img/urbanSim/urban_bench.png" alt="Urban Bench">
  </div>
</div>

<!-- Scalability Experiments -->
<div class="research-section">
  <h3 style="text-align: center"><strong>How is the Scalability?</strong></h3>
  <p>Experiments demonstrates <span class="special-font">URBAN-SIM</span> has strong scalability.</p>
  <ul>
    <li>Left: as the number of environments increases from 1 to 256, FPS scales significantly from 100 to 2,620 fps. GPU memory usage grows only slightly, with 256 environments occupying just 11.2 GB of the available 46 GB memory.</li>
    <li>Right: As the number of training scenes increases from 1 to 1,024, the performance remarkably improves from 5.1% to 83.2% in success rate.</li>
  </ul>

  <div class="white-background">
    <img src="/assets/img/urbanSim/Scalability.png" alt="Scalability Experiments">
  </div>
</div>

<!-- Acknowledgement -->
<div class="research-section">
  <h3 style="text-align: center"><b>Acknowledgement</b></h3>
  <p>The project was supported by the NSF grants CNS-2235012 and IIS-2339769, and ONR grant N000142512166. We extend our gratitude for the excellent assets, including 3D objects from Objaverse-XL, 3D humans from SynBody, and robots from IsaacLab. Thank <a href="https://www.cocodelivery.com/">COCO Robotics</a> for donating virtual and physical robots.</p>
</div>

<!-- Citation -->
<div class="research-section">
  <h3 style="text-align: center">Citation</h3>
  <pre><code class="language-plain">
@ inproceedings{wu2025urbansim,
title={Towards Autonomous Micromobility through Scalable Urban Simulation},
author={Wu, Wayne and He, Honglin and Zhang, Chaoyuan and He, Jack and Zhao, Seth Z. and Gong, Ran and Li, Quanyi and Zhou, Bolei},
booktitle ={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
year={2025}
}
</code></pre>
</div>

<style>
.custom-heading {
  font-size: 1.5em;
  font-weight: bold;
  margin-bottom: 10px; 
}
.white-background {
    background-color: white;
    display: block;
    width: 100%; 
    overflow: hidden; 
    padding: 10px;
}
.white-background img {
    width: 100%; 
    height: auto; 
}
.logo {
    display: block; 
    width: 100%; 
    overflow: hidden;
    padding: 10px;
}
.logo img {
    width: 100%; 
    height: auto; 
}
.video-grid {
    display: grid;
    grid-template-columns: 1fr 1fr; 
    grid-gap: 20px; 
}
.video iframe {
    width: 100%; 
    height: 250px; 
}
@media (max-width: 600px) {
    .video-grid {
        grid-template-columns: 1fr; 
    }
}
.gif img {
    width: 100%; 
    height: auto; 
}

/* Special monospace font for URBAN-SIM & URBAN-BENCH */
.special-font {
    font-family: 'Andale Mono', monospace;
}

</style>
