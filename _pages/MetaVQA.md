---
layout: research
permalink: /metavqa/
title: "Embodied Scene Understanding for Vision Language Models via MetaVQA"
page_title: "Embodied Scene Understanding for Vision Language Models via MetaVQA"
description: "<h3>CVPR 2025</h3>"
authors:

- {name: "Weizhen Wang"}
- {name: "Chenda Duan", url: "https://chendaduan.com"}
- {name: "Zhenghao Peng", url: "https://pengzhenghao.github.io/"}
- {name: "Yuxin Liu", url: "https://scholar.google.com/citations?user=ZQoOjaIAAAAJ&hl=en"}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io/"}

institutions:

- {name: "University of California, Los Angeles"}

nav: false
nav_order: 1
pdf_link: https://arxiv.org/abs/2501.09167
code_link: https://github.com/WeizhenWang-1210/MetaVQA


---
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
    padding: 5px;
}
.white-background img {
    width: 100%; /* Makes the image responsive */
    height: auto; /* Keeps the image's aspect ratio intact */
}
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
.gif img {
    width: 100%; /* Ensures the GIFs fill the cells */
    height: auto; /* Maintains the aspect ratio */
}
.button {
    text-decoration: none;
    border: 2px solid #d9d9d9;
    border-radius: 50px;
    padding: 10px 20px;
    font-size: 16px;
    color: #333;
    background-color: white;
    transition: all 0.3s ease;
}
.button:hover {
    background-color: #f0f0f0;
    border-color: #333;
    color: #007bff;
}
table th, 
table td {
    padding: 4px 8px !important;  /* Force smaller padding */
    line-height: 1.2 !important;  /* Control line height */
}

table tr.group-row td {
    padding: 0 !important;
    height: 8px !important;  /* Force smaller divider height */
    line-height: 1 !important;
}

/* Make all table text slightly smaller */
table, 
table th, 
table td {
    font-size: 14px !important;
}

/* Keep other styles but make them more specific */
table {
    width: 100%;
    border-collapse: collapse;
    margin: 20px 0;
}

table th {
    background-color: #f2f2f2;
    font-weight: bold;
}

table tr:not(.group-row):hover {
    background-color: #f8f9fa;
}
</style>
<!-- <div class="buttons" style="display: flex; justify-content: center; gap: 20px; margin-top: 20px;">
    <a href="#" class="button">PDF (TBD)</a>
    <a href="#" class="button">Arxiv (TBD)</a>
    <a href="#" class="button">GitHub (TBD)</a>
    <a href="#" class="button">Huggingface (TBD)</a>
    <a href="#" class="button">Inspect Dataset (TBD)</a>
</div> -->
<div class="research-section">
    <div class="white-background">
        <img src="../assets/img/metavqa/teaser.png">
    </div>
</div>
<div class="research-section">
    <ul style="list-style-type: none; padding-left: 0;">
      <strong>TL,DR: </strong> MetaVQA is a holistic benchmark for evaluating and enhancing <strong>general-purpose VLM as embodied agent</strong>.
    </ul>
</div>

<div class="research-section">
    <h3 style="text-align: center">Design Choice</h3>
    <div class="white-background">
        <img src="../assets/img/metavqa/som.png">
    </div>
   <strong>Multiple-Choice with Set-of-Marks (SoM)</strong> To effectively communicate with general-purpose vision-language models (VLMs) in visual question answering (VQA) tasks, we draw an analogy to students taking standardized tests, where clear and intuitive instructions ensure fair evaluation. Existing works rely on heterogeneous conventions, like associating pixel coordinates with image regions or using continuous versus discretized spatial information. These conventions, however, are rare in pre-training corpora dominated by human-created Internet data, making it difficult to distinguish whether poor zero-shot performance arises from a lack of scene understanding or unfamiliarity with these conventions. To address these challenges, we adopt the SoM prompting technique, which enhances visual grounding and provides unambiguous, labeled references. By formulating questions in a multiple-choice format with discretized spatial and dynamic information, we ensure fair, intuitive, and zero-shot evaluations. Our benchmark includes 30 question types that comprehensively assess spatial reasoning and embodied understanding through diverse real-world and simulated scenarios, validated further via closed-loop driving simulations.
</div>
<div class="research-section">
    <h3 style="text-align: center">Dataset Compositions</h3>
    <div class="white-background">
        <img src="../assets/img/metavqa/metavqa_distribution.png">
    </div>
   <p><strong>Left</strong>: Distribution of the question types. <strong>Right</strong>: Example for each question supertype.</p>

   <p>MetaVQA Dataset consists of a large corpus of multiple-choice questions, which contains 4,305,450 questions using 442,102 annotated frames extracted from 400 nuScenes scenarios and 6,900 Waymo scenarios covering 59,682 seconds (16.5 hours) of driving log. The questions can be categorized into three supercategories: <strong>spatial</strong> questions, <strong>embodied</strong> questions, and <strong>grounding</strong> questions. The former two supercategories cover the two facets of embodied scene understanding: spatial awareness and embodied understanding,  and the latter one diagnoses VLMs' capabilities to associate marked objects in the observation with textual referral.</p>
</div>
<div class="research-section">
    <h3 style="text-align: center">Learned Embodied Scene Understanding</h3>
    <div class="white-background">
        <img src="/assets/img/metavqa/closed_loop-demo_5.png">
    </div>
    <div class="video-container">
        <video loop autoplay muted playsinline controls>
            <source src="/assets/img/metavqa/closed_1.mp4" type="video/mp4">
        </video>
    </div>
    <div class="video-container">
        <video loop autoplay muted playsinline controls>
            <source src="/assets/img/metavqa/closed_2.mp4" type="video/mp4">
        </video>
    </div>
    <strong>Qualitative result of closed-loop evaluation.</strong> We evaluated the performance of vision-language models in a closed-loop driving set up. Case 1 compares the performance of fine-tuned Llama3.2 (left) versus its zero-shot counterpart (right) in the same scenario. Case 2 compares the performance of fine-tuned Llama3.2 (left) versus fine-tuned Qwen2 (right). As shown, fine-tuned Llama3.2 gains elevated situational awareness and can avoid collision. It also demonstrates superior safety capability compared to its trained peers.
    <div class="white-background">
        <img src="../assets/img/metavqa/learned-DEMO_2.png">
    </div>
    <strong>Improved embodied scene understanding after fine-tuning</strong> of InternVL2-8B on the withheld training set. The VLM demonstrates improved spatial understanding and embodied knowledge after learning the MetaVQA Dataset. In addition, the model attains better grounding capability.
</div>



<div class="research-section">
    <h3 style="text-align: center">VQA Benchmarks</h3>
    <div class="white-background">
        <img src="../assets/img/metavqa/radar-figure-0106.png">
    </div>
    <div class="white-background">
        <img src="../assets/img/metavqa/vqabenchmark.png">
    </div>
    <strong>Visual question answering benchmark</strong>. Performance comparison of different models on overall, simulation-only-part, and real-only-part of the withheld test sets. The parsing failure rate is also provided. Models report consistent improvements after fine-tuning, with InternVL2-8B achieving the best performance.
    
</div>
<div class="research-section">
    <h3 style="text-align: center">Close-Loop Evaluation</h3>
    <div class="white-background">
        <img src="../assets/img/metavqa/closed_loop_pipeline.png">
    </div>
    <strong>Formulation of closed-loop evaluation</strong>. At every five simulation steps (0.5 seconds wall time), the evaluated VLM is provided with annotated observations and current navigation command. The chosen action will be fed into the simulation.
    <div class="white-background">
        <img src="../assets/img/metavqa/closeloop.png">
    </div>
    <strong>Quantitative result of closed-loop evaluation</strong>. Despite not being directly trained on the driving task, VLMs report improvements in closed-loop metrics after learning the MetaVQA Dataset, in addition to better VQA accuracy. This correlation suggests that the MetaVQA Dataset contains generalizable embodied knowledge that could be easily learned and transferred to the downstream application domain (in this case, self-driving).
</div>

<div class="research-section">
    <h3 style="text-align: center">Reference</h3>
<pre><code class="language-plain">@article{wang2025metavqa,
  title={Embodied Scene Understanding for Vision Language Models via MetaVQA},
  author={Wang, Weizhen and Duan, Chenda and Peng, Zhenghao and Liu, Yuxin and Zhou, Bolei},
  journal={arXiv preprint arXiv:2501.09167},
  year={2025}
}</code></pre></div>





