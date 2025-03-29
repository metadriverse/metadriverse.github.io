---
layout: research
permalink: /metaurban/
title: "MetaUrban: An Embodied AI Simulation Platform for Urban Micromobility"
page_title: "MetaUrban: An Embodied AI Simulation Platform for Urban Micromobility"
description: "<h3 style='color:red'>ICLR 2025 Spotlight</h3>"
authors:

- {name: "Wayne Wu<sup>*</sup>", url: "https://wywu.github.io/"}
- {name: "Honglin He<sup>*</sup>", url: "https://scholar.google.com/citations?user=Y0Qrwg0AAAAJ&hl"}
- {name: "Jack He", url: "https://jackhe313.github.io/"}
- {name: "Yiran Wang", url: "https://www.linkedin.com/in/yrw3/"}
- {name: "Chenda Duan", url: "https://chendaduan.com/"}
- {name: "Zhizheng Liu", url: "https://scholar.google.com/citations?user=Asc7j9oAAAAJ&hl=en"}
- {name: "Quanyi Li", url: "https://quanyili.github.io/"}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io/"}

institutions:

- {name: "University of California, Los Angeles"}

nav: false
nav_order: 1
pdf_link: https://openreview.net/pdf?id=kFsWpSxkFz
code_link: https://github.com/metadriverse/metaurban

---
<div class="research-section">
    <div class="logo">
        <img src="/assets/img/metaurban/logo.png" alt="MetaUrban Logo">
    </div>
</div>

<div class="research-section">
    <h3 style="text-align: center">TL;DR</h3>
    <ul style="list-style-type: none; padding-left: 0;">
      <strong>MetaUrban</strong> is a <em>compositional</em> simulation platform for AI-driven urban micromobility research. It will be open-source to enable more research opportunities for the community, and foster <em>generalizable</em> and <em>safe</em> embodied AI and micromobility in cities.
    </ul>
</div>

<div class="research-section">


    <h3 style="text-align: center">Introducing MetaUrban</h3>

    <div id="video" style="overflow: hidden;">
    <iframe 
        width="100%" 
        height="100%" 
        style="width: 101.5%; height: 101.5%; left: -0.5%; top: -0.5%;" 
        src="https://www.youtube.com/embed/vHuAzNxmfKc?autoplay=1&mute=1&loop=1&playlist=vHuAzNxmfKc&controls=1&rel=0&showinfo=0" 
        frameborder="0" 
        allow="autoplay" 
        allowfullscreen="allowfullscreen">
    </iframe>
    </div>

    <div style="text-align: center; margin-top: 10px;">
    Download Video from
    <a href="https://drive.google.com/file/d/1_xYL7IXuHc0b8DvghVvzpKeBQTsTxeUe/view?usp=sharing" target="_blank">Google Drive</a> | 
    <a href="https://pan.baidu.com/s/1y1koBWpVHsJBEvLPGbXpbw?pwd=yac9" target="_blank">Baidu Netdisk</a>
</div>
</div>

<div class="research-section">
    <h3 style="text-align: center">Abstract</h3>

        <p>Public urban spaces like streetscapes and plazas serve residents and accommodate social life in all its vibrant variations.
        Recent advances in Robotics and Embodied AI make public urban spaces no longer exclusive to humans. Food delivery bots and electric wheelchairs have started sharing sidewalks with pedestrians, while robot dogs and humanoids have recently emerged in the street.
        <strong>Micromobility</strong> enabled by AI for short-distance travel in public urban spaces plays a crucial component in the future transportation system.
        Ensuring the generalizability and safety of AI models maneuvering mobile machines is essential.
        In this work, we present <strong>MetaUrban</strong>, a <em>compositional</em> simulation platform for AI-driven urban micromobility research.
        MetaUrban can construct an <em>infinite</em> number of interactive urban scenes from compositional elements, covering a vast array of ground plans, object placements, pedestrians, vulnerable road users, and other mobile agents' appearances and dynamics.
        We design point navigation and social navigation tasks as the pilot study using MetaUrban for urban micromobility research and establish various baselines of Reinforcement Learning and Imitation Learning.
        We conduct extensive evaluation across mobile machines, demonstrating that heterogeneous mechanical structures significantly influence the learning and execution of AI policies.
        We perform a thorough ablation study, showing that the compositional nature of the simulated environments can substantially improve the generalizability and safety of the trained mobile agents.
        MetaUrban will be made publicly available to provide research opportunities and foster safe and trustworthy embodied AI and micromobility in cities. The code and dataset are released.</p>

</div>

<div class="research-section">
    <h3 style="text-align: center">Procedural Generation Pipeline</h3>

    <div class="white-background">
        <img src="/assets/img/metaurban/procedural_generation.png">
    </div>

    MetaUrban can automatically generate complex urban scenes with its compositional nature. MetaUrban uses a structured description script to create urban scenes. Based on the provided information about street blocks, sidewalks, objects, agents, and more, it starts with the street block map, then plans the ground layout by dividing different function zones, then places static objects, and finally populates dynamic agents. In the Figure, the first column is the structured description script. From the second to the fourth column, the top rows show the 2D road maps, and the bottom rows show the bird-eye view of 3D scenes in the simulator.
</div>

<div class="research-section">
    <h3 style="text-align: center">Urban Scene Gallery</h3>
    <div class="gif">
        <img src="/assets/img/metaurban/urbanscene_gallery.gif">
    </div>
</div>

<div class="research-section">
    <h3 style="text-align: center">Parade of Dynamic Agents</h3>

    <video style="display:block; width:100%; height:auto;" autoplay="autoplay" muted loop="loop" controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/crossroad.mp4" type="video/mp4"/></video>
</div>

<div class="research-section">
    <h3 style="text-align: center">Sensors</h3>
    <div class="gif"><img src="/assets/img/metaurban/sensors_grid.gif"></div>
</div>

<div class="research-section">
    <h3 style="text-align: center">Benchmarks</h3>

    <div class="white-background">
        <img src="/assets/img/metaurban/benchmark.png">
    </div>

    We design two common tasks in urban scenes as the pilot study: Point Navigation (PointNav) and Social Navigation (Saccess to a pre-built environment map. In SocialNav, the agent is required to reach a point goal in dynamic environments that contain moving environmental agents. The agent shall avoid collisions or proximity to environmental agents beyond thresholds to avoid penalization (distance <0.2 meters).
    The agent is evaluated using the Success Rate (SR) and Success weighted by Path Length (SPL) metrics, which measure the success and efficiency of the path taken by the agent. For SocialNav, except Success Rate (SR), the Social Navigation Score (SNS), is also used to evaluate the social complicity of the agent. For both tasks, we further report the Cumulative Cost (CC) to evaluate the safety properties of the agent. It records the crash frequency to obstacles or environmental agents.
    We evaluate 7 typical baseline models to build comprehensive benchmarks on MetaUrban, across Reinforcement Learning (PPO), Safe Reinforcement Learning (PPO-LagocialNav). In PointNav, the agent’s goal is to navigate to the target coordinates in static environments without, and PPO-ET), Offline Reinforcement Learning (IQL and TD3+BC), and Imitation Learning (BC and GAIL).
</div>

<div class="research-section">    
    <h3 style="text-align: center">Results</h3>

    The results of a PPO policy trained in MetaUrban environments on the social navigation task. We demonstrate success cases that can avoid collision with objects and other agents. However, there are still many interesting failure cases, which indicate the complexity of MetaUrban environments and the significant room for improvement of embodied agents in urban spaces.

    <br><br>

    <h4>Success Cases</h4>
    <div class="video-grid">
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/success1.mp4" type="video/mp4"/></video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/success2.mp4" type="video/mp4"/></video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/success3.mp4" type="video/mp4"/></video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/success4.mp4" type="video/mp4"/></video>
        </div>
    </div>

    <br><br>

    <h4>Failure Cases</h4>
    <div class="video-grid">
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/fail1.mp4" type="video/mp4"/></video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/fail2.mp4" type="video/mp4"/></video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/fail3.mp4" type="video/mp4"/></video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline><source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/fail4.mp4" type="video/mp4"/></video>
        </div>
    </div>

</div>

<div class="research-section">
    <h3 style="text-align: center">Terrains and Materials</h3>
    <div class="video-grid">
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
            <source src="https://raw.githubusercontent.com/metaurban-iclr-2025/metaurban-iclr-2025.github.io/main/assets/teaser/Index_0001.mp4" type="video/mp4">
        </video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
            <source src="https://raw.githubusercontent.com/metaurban-iclr-2025/metaurban-iclr-2025.github.io/main/assets/teaser/Index_0002.mp4" type="video/mp4">
            </video>
        </div>
    </div>
</div>

<div class="research-section">
    <h3 style="text-align: center">Traffic Rules</h3>
        <video style="display:block; width:100%; height:auto;" muted controls playsinline>
        <source src="https://raw.githubusercontent.com/metaurban-iclr-2025/metaurban-iclr-2025.github.io/main/assets/teaser/Index_0000.mp4" type="video/mp4">
        </video>
</div>

<!-- Interface for Demonstration Data Collection -->
<div class="research-section">
    <h3 style="text-align: center">Interface for Demonstration Data Collection</h3>
    <div class="video-grid">
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
            <source src="https://raw.githubusercontent.com/metaurban-iclr-2025/metaurban-iclr-2025.github.io/main/assets/teaser/UI1.mp4" type="video/mp4">
            </video>
        </div>
        <div class="video">
            <video style="display:block; width:100%; height:auto;" muted controls playsinline>
            <source src="https://raw.githubusercontent.com/metaurban-iclr-2025/metaurban-iclr-2025.github.io/main/assets/teaser/UI2.mp4" type="video/mp4">
            </video>
        </div>
    </div>
</div>

<div class="research-section">
    <h3 style="text-align: center">Interface for Human-in-the-loop Learning</h3>
        <video style="display:block; width:100%; height:auto;" muted controls playsinline>
        <source src="https://raw.githubusercontent.com/metaurban-iclr-2025/metaurban-iclr-2025.github.io/main/assets/teaser/Index_0009.mp4" type="video/mp4">
        </video>
</div>

<div class="research-section">
    <h3 style="text-align: center">Impacts</h3>

    <strong>Embodied AI</strong>. MetaUrban contributes to advancing areas such as robot navigation, social robotics, and interactive systems. It could facilitate the development of robust AI systems capable of understanding and navigating complex urban environments.
    <br>

    <strong>Economy</strong>. MetaUrban could be used in businesses and services operating in urban environments, such as last-mile food delivery, assistive wheelchairs, and trash-cleaning robots. It could also drive innovation in urban planning and infrastructure development by providing simulation tools and insights into how spaces are utilized, thereby enhancing the economic and societal efficiency of public urban spaces like sidewalks and parks.
    <br>

    <strong>Society</strong>. By enabling the safe integration of robots and AI systems in public spaces, MetaUrban could support the development of assistive technologies that can aid in accessibility and public services. Using AI in public spaces might foster new forms of social interaction and community services, making urban spaces more livable and joyful.
    
</div>

<div class="research-section">
<h3 style="text-align: center">Acknowledgement</h3>
<p>
The project was supported by the NSF Grants CNS-2235012, IIS-2339769, and TI-2346267, and the Intel Rising Star Faculty Award. We extend our gratitude for the excellent datasets, including 3D objects from <a href="https://github.com/allenai/objaverse-xl" target="_blank">Objaverse-XL</a> and <a href="https://omniobject3d.github.io/" target="_blank">OmniObject3D</a>, 3D humans from <a href="https://synbody.github.io/" target="_blank">SynBody</a>, and human motions from <a href="https://bedlam.is.tue.mpg.de/" target="_blank">BEDLAM</a>. Special thanks to Hao Zhu, Haiyi Mei, Jianglin Fu, Rongzhang Gu, Lei Yang, and Zhenghao Peng for their assistance and insightful discussions. Thank <a href="https://www.cocodelivery.com/" target="_blank">COCO Robot</a> for donating virtual and physical robots.
</p>
</div>


<div class="research-section">
<h3 style="text-align: center">Reference</h3>

<pre><code class="language-plain">@article{wu2025metaurban,
  title={MetaUrban: An Embodied AI Simulation Platform for Urban Micromobility},
  author={Wu, Wayne and He, Honglin and He, Jack and Wang, Yiran and Duan, Chenda and Liu, Zhizheng and Li, Quanyi and Zhou, Bolei},
  journal={International Conference on Learning Representation},
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



