---
layout: research
permalink: /urban-x/
title: "Urban-X: Towards Autonomous Micromobility through Scalable Urban Simulation"
page_title: "Urban-X: Towards Autonomous Micromobility through Scalable Urban Simulation"
description: "<h3>CVPR 2025 Submission #18</h3>"
authors:
  - {name: "Wayne Wu", url: "https://wywu.github.io/"}
  - {name: "Honglin He", url: "https://scholar.google.com/citations?user=Y0Qrwg0AAAAJ&hl"}
  - {name: "Chaoyuan Zhang", url: "#"}
  - {name: "Jack He", url: "https://jackhe313.github.io/"}
  - {name: "Seth Z. Zhao", url: "https://sethzhao506.github.io/"}
  - {name: "Ran Gong", url: "#"}
  - {name: "Quanyi Li", url: "https://quanyili.github.io/"}
  - {name: "Bolei Zhou", url: "https://boleizhou.github.io/"}
institutions:
  - {name: "University of California, Los Angeles"}
nav: false
nav_order: 1
pdf_link: "#"
code_link: "#"  # Add link when code is available
---

<!-- TL;DR Section -->
<div class="research-section">
    <h3 style="text-align: center">TL;DR</h3>
    <ul style="list-style-type: none; padding-left: 0;">
      <strong>Urban-X</strong> is a <em>scalable urban simulation</em> solution for advancing research in autonomous micromobility. It introduces a high-performance robot learning platform for AI-driven navigation in complex urban settings, alongside a comprehensive benchmark suite that measures crucial robotic capabilities like locomotion, navigation, and long-horizon traversal.
    </ul>
</div>

<!-- Introducing Urban-X -->
<div class="research-section">
    <h3 style="text-align: center">Introducing Urban-X</h3>
    <div id="video" style="overflow: hidden;">
    <!-- Sample embedded video; replace with your own link -->
    <iframe 
        width="100%" 
        height="100%" 
        style="width: 101.5%; height: 101.5%; left: -0.5%; top: -0.5%;" 
        src="https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1&mute=1&loop=1&playlist=dQw4w9WgXcQ&controls=1&rel=0&showinfo=0" 
        frameborder="0" 
        allow="autoplay" 
        allowfullscreen="allowfullscreen">
    </iframe>
    </div>
    <div style="text-align: center; margin-top: 10px;">
    Download Video from
    <a href="#" target="_blank">Google Drive</a> | 
    <a href="#" target="_blank">Baidu Netdisk</a>
</div>
</div>

<!-- Abstract -->
<div class="research-section">
    <h3 style="text-align: center">Abstract</h3>
    <p>
      Urban public spaces can be tricky for micromobility devices such as delivery robots, electric wheelchairs, or small autonomous vehicles. 
      <strong>Urban-X</strong> provides a scalable simulation solution featuring diverse and realistic urban environments, enabling training and evaluation of AI agents for short-distance travel. 
      Our approach has two main components: 
      (1) A high-performance robot learning platform that programmatically generates an <em>infinite</em> variety of interactive urban scenes, covering road networks, obstacles, dynamic agents (pedestrians, bikes), and varied terrains (stairs, slopes, rough ground). 
      (2) A suite of essential tasks—<em>urban locomotion</em> and <em>urban navigation</em>—plus a <em>long-horizon urban traverse</em> benchmark. 
      We evaluate multiple robot embodiments (wheeled, quadruped, wheeled-legged, humanoid) using standard metrics. 
      Our results reveal unique capabilities and failure modes for each platform. 
      We will open-source both the core simulation engine and the benchmark suite, fostering future research in safer and more efficient micromobility in cities.
    </p>
</div>

<!-- Procedural Generation Pipeline -->
<div class="research-section">
    <h3 style="text-align: center">Procedural Generation Pipeline</h3>
    <div class="white-background">
        <!-- Replace with any diagram or flowchart image -->
        <img src="/assets/img/urban_x/pipeline.png" alt="Urban-X Pipeline">
    </div>
    <p>
        Urban-X’s <em>Hierarchical Urban Generation</em> pipeline constructs diverse static scenes—from road networks to building placement and terrain creation. Combined with <em>Interactive Dynamics Generation</em>, it populates each scene with pedestrians, cyclists, and other mobile agents that interact in real-time with the robot. An <em>Asynchronous Scene Sampling</em> scheme then streamlines large-scale parallel training on a single GPU. 
        This combination ensures both <strong>scene diversity</strong> and <strong>high performance</strong> for efficient policy optimization.
    </p>
</div>

<!-- Task Gallery -->
<div class="research-section">
    <h3 style="text-align: center">Task Gallery</h3>
    <div class="gif">
        <!-- Example GIF demonstrating various tasks -->
        <img src="/assets/img/urban_x/task_gallery.gif" alt="Urban-X Task Gallery">
    </div>
</div>

<!-- Benchmark Examples -->
<div class="research-section">
    <h3 style="text-align: center">Urban-X Benchmarks</h3>
    <p>
        <strong>Urban Locomotion</strong>: Four tasks designed to test how well an agent traverses different terrain types: flat, slope, stairs, and rough ground. 
        <br><br>
        <strong>Urban Navigation</strong>: Three tasks measuring the ability to navigate unobstructed spaces, static obstacles, and dynamic obstacles. 
        <br><br>
        <strong>Urban Traverse</strong>: A long-horizon benchmark where the agent must traverse over one kilometer of diverse terrain. We offer a <em>human-AI shared autonomy</em> pilot approach to handle this very challenging setting.
    </p>

    <div class="white-background">
        <!-- Example figure or table of performance results -->
        <img src="/assets/img/urban_x/benchmark.png" alt="Urban-X Benchmark Results">
    </div>
    <p>
        Multiple robot embodiments (e.g. wheeled, quadruped, humanoid) are evaluated across success rate, route completion, collisions, and other metrics like stability or smoothness in locomotion tasks. Each unique mechanical structure demonstrates distinct benefits and limitations in complex cityscapes.
    </p>
</div>

<!-- Results: Videos or Gifs Section -->
<div class="research-section">    
    <h3 style="text-align: center">Example Results</h3>
    <p>
       Below are representative success and failure scenarios when training an AI agent in Urban-X environments:
    </p>

    <h4>Success Cases</h4>
    <div class="video-grid">
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
              <source src="/assets/videos/urban_x/success1.mp4" type="video/mp4"/>
            </video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
              <source src="/assets/videos/urban_x/success2.mp4" type="video/mp4"/>
            </video>
        </div>
    </div>

    <br><br>

    <h4>Failure Cases</h4>
    <div class="video-grid">
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
              <source src="/assets/videos/urban_x/fail1.mp4" type="video/mp4"/>
            </video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
              <source src="/assets/videos/urban_x/fail2.mp4" type="video/mp4"/>
            </video>
        </div>
    </div>
</div>

<!-- Terrains and Materials (Optional) -->
<div class="research-section">
    <h3 style="text-align: center">Terrains and Materials</h3>
    <p>
      Urban-X generates stairs, slopes, rough sidewalks, and more, each with adjustable parameters like step height or ramp angle. Combined with dynamic agents, the platform pushes robot policies to adapt in real-time to complex city environments.
    </p>
    <div class="video-grid">
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
                <source src="/assets/videos/urban_x/terrain1.mp4" type="video/mp4">
            </video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
                <source src="/assets/videos/urban_x/terrain2.mp4" type="video/mp4">
            </video>
        </div>
    </div>
</div>

<!-- Traffic Rules (Optional) -->
<div class="research-section">
    <h3 style="text-align: center">Traffic Rules</h3>
    <video style="display:block; width:100%; height:auto;" muted controls playsinline>
        <source src="/assets/videos/urban_x/traffic_rules.mp4" type="video/mp4">
    </video>
    <p>
      By incorporating multi-agent path planning, realistic pedestrian and cyclist behaviors, and reaction to the trained robot, the traffic flow in Urban-X helps measure how AI solutions cope with dense interactions.
    </p>
</div>

<!-- Human-in-the-loop / Demo Data Collection UI (Optional) -->
<div class="research-section">
    <h3 style="text-align: center">Human-in-the-loop Interfaces</h3>
    <p>
      Urban-X provides customizable interfaces for demonstration data collection and human intervention during policy training. This is especially useful for the <em>long-horizon Urban Traverse</em> task, where real-time user adjustments can prevent catastrophic failures.
    </p>
    <div class="video-grid">
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
                <source src="/assets/videos/urban_x/UI1.mp4" type="video/mp4">
            </video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
                <source src="/assets/videos/urban_x/UI2.mp4" type="video/mp4">
            </video>
        </div>
    </div>
</div>

<!-- Impacts Section -->
<div class="research-section">
    <h3 style="text-align: center">Impacts</h3>
    <p><strong>Embodied AI.</strong> Urban-X supports advanced research in real-time robot decision-making across challenging sidewalks, plazas, and other public areas.</p>
    <p><strong>Economy.</strong> Enhanced last-mile delivery, reduced reliance on vehicle-based transport for short trips, and potential new urban services (e.g., trash-cleaning robots, assistive wheelchairs) may lower costs and traffic congestion.</p>
    <p><strong>Society.</strong> More inclusive, safer sidewalks and plazas, better accessibility for mobility-challenged citizens, and improved AI-human interactions in public spaces.</p>
</div>

<!-- Acknowledgement -->
<div class="research-section">
    <h3 style="text-align: center">Acknowledgement</h3>
    <p>
      We thank collaborators and the broader community for valuable discussions. The platform is built upon open datasets (e.g., large 3D assets, robot models) and simulation frameworks (Omniverse, PhysX), ensuring realistic training conditions and encouraging reproducible research.
    </p>
</div>

<!-- Reference -->
<div class="research-section">
    <h3 style="text-align: center">Reference</h3>
<pre><code class="language-plain">
@misc{urbanx2025,
  title={Towards Autonomous Micromobility through Scalable Urban Simulation},
  author={Anonymous},
  howpublished={CVPR 2025 Submission #18},
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
</style>
