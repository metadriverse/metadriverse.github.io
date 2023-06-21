---
layout: page-notitle
permalink: /scenarionet/
title: ScenarioNet
nav: true
nav_order: 2
---

<div class="col-12 position-relative">
    <!-- Mobile layout -->
    <div class="d-block d-sm-none text-center mb-3">
        <h2 style="color: white; text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); font-weight: bold;">ScenarioNet</h2>
        <p style="color: white; text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); font-size: 1.2em; font-weight: bold;">Open-source platform for large-scale traffic scenario modeling and simulation</p>
    </div>
    <!-- Video embed -->
    <div class="embed-responsive embed-responsive-16by9">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/C3DwU7GHJe0?autoplay=1&mute=1&loop=1&playlist=C3DwU7GHJe0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <!-- Desktop layout -->
        <div class="position-absolute w-100 h-100 d-none d-sm-flex flex-column align-items-center justify-content-center text-center" style="top: 0; left: 0;">
            <h2 style="color: white; text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.7); font-weight: bold;">ScenarioNet</h2>
            <p style="color: white; text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); font-size: 1.2em; font-weight: bold;">Open-source platform for large-scale traffic scenario modeling and simulation</p>
        </div>
    </div>
</div>


<div class="col-12 md-5" style="margin-top: 100px; margin-bottom: 100px;">    
    <h3 style="text-align: center">Meet ScenarioNet</h3>
    <p><b>ScenarioNet</b> is an open-sourced platform for large-scale traffic scenario modeling and simulation:</p>
<li>  
It processes various sources of the input data, including procedurally generated scenarios, 
human-crafted safety-critical data, and more importantly real-world data. 
</li><li>
It provides a unified interface to easily import and convert the data from various driving dataset such as Waymo, nuScenes, Lyft L5, and nuPlan datasets.
</li><li>
These realistic data can be further replayed and interact in our simulation environment, MetaDrive.
</li>
</div>



<div class="col-12 md-5" style="margin-top: 100px; margin-bottom: 100px;">
<li>
    <b>ScenarioNet</b> reads from real world dataset such as Waymo, nuScenes, Lyft L5, and nuPlan datasets and creates
interactive environment for closed-loop simulation.
</li>
    <video width="100%" max-width="800px" loop autoplay muted playsinline
    src="../assets/scenarionet/sn_convert.mp4">
    </video>
</div>


<div class="col-12 md-5" style="margin-top: 100px; margin-bottom: 100px;">
<li>
    <b>ScenarioNet</b> bridges OpenPilot (Left) and ROS (Right) for autonomous driving testing.
</li>
<iframe width="47%" height="230px" src="https://www.youtube.com/embed/KjlPB0nCTvg?autoplay=1&loop=1&mute=1&playlist=KjlPB0nCTvg" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="47%" height="230px" src="https://www.youtube.com/embed/WWwdnURnOBM?t=10&loop=1&autoplay=1&mute=1&playlist=WWwdnURnOBM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>



<div class="col-12 md-5" style="margin-top: 100px; margin-bottom: 100px;">
<li>
    <b>ScenarioNet</b> leverages <a href="../metadrive">MetaDrive Simulator</a> for multi-modal observation simulation.
</li>
    <video width="100%" max-width="800px" loop autoplay muted playsinline
    src="../assets/scenarionet/sn_sensors.mp4">
    </video>
</div>




<div class="col-12" style="margin-top: 100px; margin-bottom: 100px;"> 
    <h3 style="text-align: center">ScenarioNet's System Design</h3>
<p><b>ScenarioNet</b> ... Some description here.
    </p>
    <div class="img-container">
        <img src="../assets/img/system.png" class="my-image" alt="Your Image" />
    </div>
</div>
