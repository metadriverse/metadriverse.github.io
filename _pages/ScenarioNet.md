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



<div class="col-12 md-5" style="margin-top: 100px; margin-bottom: 100px">    
    <h3 style="text-align: center">Meet ScenarioNet</h3>
    <p><b>ScenarioNet</b> is an open-sourced platform for large-scale traffic scenario modeling and simulation.</p>
<li style="padding: 0.5rem 0.5rem;">
Large-scale driving datasets contain HD maps and detailed annotations which accurately reflect the real-world complexity of traffic behaviors, substantially accelerating autonomous driving research.
</li><li style="padding: 0.5rem 0.5rem;">
We can harvest a massive number of complex traffic scenarios and recreate their digital twins in simulation, for facilitating many research opportunities in machine learning and autonomous driving. 
</li><li style="padding: 0.5rem 0.5rem;">
ScenarioNet defines a unified scenario description format and collects a large-scale 
repository of real-world traffic scenarios from the heterogeneous data in various driving datasets including Waymo, nuScenes, Lyft L5, and nuPlan datasets. 
</li><li style="padding: 0.5rem 0.5rem;">
ScenarioNet pipelines those scenarios and creates log-replayed or interactive environments
with in multiple views from Bird-Eye-View layout to realistic 3D rendering in MetaDrive simulator,
providing a benchmark for evaluating the safety of autonomous driving stacks in simulation before their real-world 
deployment.
</li><li style="padding: 0.5rem 0.5rem;">
We demonstrate the strengths of ScenarioNet on large-scale scenario generation, AD testing, imitation learning, and reinforcement learning in both single-agent and multi-agent settings. 
</li>
</div>



<div class="col-12 md-5" style="margin-top: 100px; margin-bottom: 100px;">
    <video width="100%" max-width="800px" loop autoplay muted playsinline
    src="../assets/scenarionet/sn_convert.mp4">
    </video>
    <div class="description">
    <b>ScenarioNet</b> reads from real world dataset such as Waymo, nuScenes, Lyft L5, and nuPlan datasets and creates
interactive environment for closed-loop simulation.
    </div>
</div>


<div class="col-12 md-5" style="margin-top: 100px; margin-bottom: 100px;">
<iframe width="47%" height="230px" src="https://www.youtube.com/embed/KjlPB0nCTvg?autoplay=1&loop=1&mute=1&playlist=KjlPB0nCTvg" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="47%" height="230px" src="https://www.youtube.com/embed/WWwdnURnOBM?t=10&loop=1&autoplay=1&mute=1&playlist=WWwdnURnOBM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    <div class="description">
        <b>ScenarioNet</b> bridges OpenPilot (Left) and ROS (Right) for autonomous driving testing.
    </div>
</div>



<div class="col-12 md-5" style="margin-top: 100px; margin-bottom: 100px;">
    <video width="100%" max-width="800px" loop autoplay muted playsinline
    src="../assets/scenarionet/sn_sensors.mp4">
    </video>
    <div class="description">
        <b>ScenarioNet</b> leverages <a href="../metadrive">MetaDrive Simulator</a> for multi-modal observation simulation.
    </div>
</div>




<div class="col-12" style="margin-top: 100px; margin-bottom: 100px;"> 
    <h3 style="text-align: center">ScenarioNet's System Design</h3>
    <div class="img-container">
        <img src="../assets/img/system.jpg" class="my-image" alt="Your Image" />
    </div>
    <div class="description" style="margin-top: 1em;">
From bottom to top, <b>ScenarioNet</b>  consists of the data layer, system layer, and application layer which are connected by two critical data flows, 
<span style="color: #F07C8D">data conversion</span>
and 
<span style="color: #32A06E">simulation</span>
.
Data conversing unifies various data formats and stored them in an internal scenario description.
The system layer then provides a set of tools to operate converted data efficiently, such as
<span style="color: #FFAA2D">filtering</span>
, merging, sanity-check, 
<span style="color: #7A24AB">splitting</span>
 and so on.
Once the database is ready, it can be loaded into MetaDrive for large-scale simulation and supports applications. 
    </div>
</div>
