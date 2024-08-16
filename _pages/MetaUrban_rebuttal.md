---
layout: research
permalink: /metaurban/rebuttal/
title: "MetaUrban: Rebuttal Video Demonstrations"
page_title: "MetaUrban: Rebuttal Video Demonstrations"
nav: false
nav_order: 2
---

<div class="research-section">
    <h3 style="text-align: center">Rebuttal Video Demonstrations</h3>
    <p style="text-align: center">This page showcases various video demonstrations in response to reviewer feedback. Click on any video to play.</p>

    <div class="video-grid">
        <div class="video">
            <h4 style="text-align: center;">Video Index_0000 <br> (To Reviewer FiPy and R6rL)</h4>
            <video style="display:block; width:100%; height:auto;" controls playsinline>
                <source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/Index_0000.mp4" type="video/mp4"/>
            </video>
            <p style="text-align: center;">Traffic light rules.</p>
        </div>

        <div class="video">
            <h4 style="text-align: center;">Video Index_0001 <br> (To Reviewer FiPy)</h4>
            <video style="display:block; width:100%; height:auto;" controls playsinline>
                <source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/Index_0000.mp4" type="video/mp4"/>
            </video>
            <p style="text-align: center;">Simulation of a delivery bot moving on different terrains.</p>
        </div>

        <div class="video">
            <h4 style="text-align: center;">Video Index_0002 <br> (To Reviewer FiPy)</h4>
            <video style="display:block; width:100%; height:auto;" controls playsinline>
                <source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/Index_0002.mp4" type="video/mp4"/>
            </video>
            <p style="text-align: center;">Simulation of a delivery bot moving on different materials.</p>
        </div>

        <div class="video">
            <h4 style="text-align: center;">Video Index_0003 <br> (To Reviewer FiPy)</h4>
            <video style="display:block; width:100%; height:auto;" controls playsinline>
                <source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/Index_0002.mp4" type="video/mp4"/>
            </video>
            <p style="text-align: center;">Simulation of lane merging and diverging scenarios.</p>
        </div>

        <div class="video">
            <h4 style="text-align: center;">Video Index_0004 <br> (To Reviewer R6rL)</h4>
            <video style="display:block; width:100%; height:auto;" controls playsinline>
                <source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/Index_0002.mp4" type="video/mp4"/>
            </video>
            <p style="text-align: center;">Collaboration with <a href="https://www.cocodelivery.com/" target="_blank">COCO Robotics</a> for real-world food delivery.</p>
        </div>

        <div class="video">
            <h4 style="text-align: center;">Video Index_0005 <br> (To Reviewer R6rL and qkEE)</h4>
            <video style="display:block; width:100%; height:auto;" controls playsinline>
                <source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/Index_0002.mp4" type="video/mp4"/>
            </video>
            <p style="text-align: center;">Integration of OmniVerse as the renderer to improve visual realism and PhysX as the physical engine to improve interactive realism.</p>
        </div>

        <div class="video">
            <h4 style="text-align: center;">Video Index_0006 <br> (To Reviewer R6rL and yJjR)</h4>
            <video style="display:block; width:100%; height:auto;" controls playsinline>
                <source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/Index_0000.mp4" type="video/mp4"/>
            </video>
            <p style="text-align: center;">Preliminary results of harnessing Diffusion Model to improve the visual quality of MetaUrban in 2D space. Input: RGB image, depth map, semantic map and provided by MetaUrban; output: photo-realistic image. (It is an extension of our previous work <a href="https://metadriverse.github.io/simgen/" target="_blank">SimGen</a>)
</p>
        </div>

        <div class="video">
            <h4 style="text-align: center;">Video Index_0007 <br> (To Reviewer R6rL and yJjR)</h4>
            <video style="display:block; width:100%; height:auto;" controls playsinline>
                <source src="https://raw.githubusercontent.com/metadriverse/metadriverse.github.io/main/assets/teaser/Index_0000.mp4" type="video/mp4"/>
            </video>
            <p style="text-align: center;">Preliminary results of harnessing Gaussian Splatting to improve the visual quality of MetaUrban in 3D space. Input: monocular videos; output: 3D scene represented by Gaussian Splatting. Integrated within the simulator, it enables training agents with photo-realistic RGB images.</p>
        </div>
    </div>
</div>

<style>
.video-grid {
    display: grid;
    grid-template-columns: 1fr 1fr; /* Creates two columns */
    grid-gap: 20px; /* Space between videos */
}
.video iframe {
    width: 100%; /* Ensures iframe takes the full width of the container */
    height: 250px; /* Fixed height for all videos */
}
.video h4, .video p {
    margin: 10px 0; /* Space around the titles and captions */
}

@media (max-width: 600px) {
    .video-grid {
        grid-template-columns: 1fr; /* Stacks videos into a single column on small screens */
    }
}

/* Hide the "Code" link specifically on this page */
.col-12.md-5 h6 a[href="{{ page.code_link }}"] {
    display: none;
}
</style>
