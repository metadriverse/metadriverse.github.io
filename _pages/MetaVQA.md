---
layout: metavqa_nolink
permalink: /metaVQA/
title: MetaVQA
page_title: MetaVQA
description: "A Benchmark for Embodied Scene Understanding of Vision-Language Models"
nav: false
nav_order: 1
---


<img src="../assets/img/metavqa/metavqa_method_v1.jpg" class="my-image" alt="Image" />

<!-- Disable changing the color of a clicked link -->
<style>
a:link, a:visited, a:hover, a:active {
    color: var(--global-text-color);
    text-decoration: none;
}
</style>


<div class="research-section">
    <h3 style="text-align: center">What is MetaVQA?</h3>
    <p><b>MetaVQA</b> a visual question-answering benchmark for improving and evaluating the embodied scene understanding of VLMs.</p>
<li style="padding: 0.5rem 0.5rem;">
MetaVQA designs a scalable pipeline to generate visual question answer (VQA) pairs relating to traffic scenarios imported from various sources, including nuScenes dataset, Waymo Open Motion Dataset, and a synthetic dataset of safety-critical scenes.
</li><li style="padding: 0.5rem 0.5rem;">
MetaVQA provides a large-scale VQA dataset containing 2.7M questions for 291K frames related to spatial, visual, dynamic, and safety-critical counterfactual scene understandings.
</li><li style="padding: 0.5rem 0.5rem;">
MetaVQA establishes the baseline performance of VLMs on the dataset and show that the VLMs achieve remarkable embodied scene understanding capabilities through instruction tuning, especially when handling safety-critical situations.
</li>
</div>





<div class="research-section">
    <h3 style="text-align: center">MetaVQA's QA Generation Pipeline</h3>
    <div class="img-container">
        <img src="../assets/img/metavqa/metavqa_qa_gen.jpg" class="my-image" alt="Image" />
    </div>
    <div class="description" style="margin-top: 1em;">
 We first modify a question-type-dependent context-free grammar (CFG) according to the scene graph. Then, we randomly sample a CFG tree and instantiate the referral in the question template by traversing leaf nodes according to the tree.Meanwhile, we compile a set of functional programs for all &lt;o&gt; token bottom-up. Each program enforces constraints from child nodes and filters the objects in the scene into an object set that satisfies these constraints. Once a program finishes, its return value informs the next program's constraints. Once all programs are terminated, the final set contains all objects grounded by the referral, and this set is post-processed to retrieve the final answer.
    </div>
</div>

<div class="research-section">
    <h3 style="text-align: center">MetaVQA's Baseline</h3>
    <div class="description" style="margin-top: 1em;">
We conduct benchmark experiments on VQA tasks. The model receives questions and corresponding visual data, which may consist of either a single frame (Static) or five frames (Dynamic and Safety) captured from six different views. The model is trained to predict the correct answer using token strings, and it is evaluated with questions from all three supertypes. For detailed explainations, please refer to the paper. Note that we are continue to expand this baseline to more models and more tasks.
    </div>
    <table>
  <caption><strong>Benchmarks with different data composition.</strong> All metrics are evaluated on a held-out test set with all supertypes. <strong>S:</strong> spatial; <strong>T:</strong> trajectory; <strong>A:</strong> attributes; <strong>N:</strong> numerical; <strong>L:</strong> logical. <span style="background-color: #f5f5f5;">Overall:</span> main metric.</caption>
  <thead>
    <tr>
      <th></th>
      <th colspan="3">Data Composition</th>
      <th></th>
      <th colspan="6">Averaged</th>
      <th colspan="4">Static</th>
      <th colspan="5">Dynamic</th>
    </tr>
    <tr>
      <th>Model</th>
      <th>Static</th>
      <th>Dynamic</th>
      <th>Safety</th>
      <th style="background-color: #f5f5f5;">Overall</th>
      <th>S&#8593;</th>
      <th>T&#8595;</th>
      <th>A&#8593;</th>
      <th>N&#8593;</th>
      <th>L&#8593;</th>
      <th>Safe&#8593;</th>
      <th>S&#8593;</th>
      <th>A&#8593;</th>
      <th>N&#8593;</th>
      <th>L&#8593;</th>
      <th>S&#8593;</th>
      <th>T&#8595;</th>
      <th>A&#8593;</th>
      <th>N&#8593;</th>
      <th>L&#8593;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>BLIP-2</td>
      <td>&#10003;</td>
      <td></td>
      <td></td>
      <td style="background-color: #f5f5f5;">0.093</td>
      <td>0.160</td>
      <td>N/A</td>
      <td>0.431</td>
      <td>0.359</td>
      <td>0.109</td>
      <td>0.164</td>
      <td><strong>0.249</strong></td>
      <td>0.499</td>
      <td>0.565</td>
      <td>0.103</td>
      <td>0.070</td>
      <td>N/A</td>
      <td>0.363</td>
      <td>0.152</td>
      <td>0.116</td>
    </tr>
    <tr>
      <td></td>
      <td>&#10003;</td>
      <td>&#10003;</td>
      <td></td>
      <td style="background-color: #f5f5f5;">0.385</td>
      <td><strong>0.280</strong></td>
      <td><strong>1.423</strong></td>
      <td>0.454</td>
      <td>0.501</td>
      <td>0.129</td>
      <td>0.000</td>
      <td>0.221</td>
      <td>0.463</td>
      <td>0.545</td>
      <td>0.173</td>
      <td><strong>0.338</strong></td>
      <td><strong>1.423</strong></td>
      <td>0.446</td>
      <td>0.457</td>
      <td>0.085</td>
    </tr>
    <tr>
      <td></td>
      <td>&#10003;</td>
      <td>&#10003;</td>
      <td>&#10003;</td>
      <td style="background-color: #f5f5f5;">0.489</td>
      <td>0.204</td>
      <td>4.563</td>
      <td>0.420</td>
      <td>0.486</td>
      <td>0.005</td>
      <td>0.822</td>
      <td>0.182</td>
      <td>0.419</td>
      <td>0.557</td>
      <td>0.000</td>
      <td>0.225</td>
      <td>4.563</td>
      <td>0.422</td>
      <td>0.415</td>
      <td>0.010</td>
    </tr>
    <tr>
      <td>ELM</td>
      <td>&#10003;</td>
      <td></td>
      <td></td>
      <td style="background-color: #f5f5f5;">0.385</td>
      <td>0.184</td>
      <td>N/A</td>
      <td>0.483</td>
      <td>0.400</td>
      <td>0.395</td>
      <td>0.108</td>
      <td>0.190</td>
      <td>0.499</td>
      <td>0.564</td>
      <td>0.598</td>
      <td>0.178</td>
      <td>N/A</td>
      <td>0.466</td>
      <td>0.235</td>
      <td>0.193</td>
    </tr>
    <tr>
      <td></td>
      <td>&#10003;</td>
      <td>&#10003;</td>
      <td></td>
      <td style="background-color: #f5f5f5;">0.710</td>
      <td>0.208</td>
      <td>1.710</td>
      <td>0.485</td>
      <td>0.515</td>
      <td>0.412</td>
      <td>0.150</td>
      <td>0.183</td>
      <td>0.502</td>
      <td><strong>0.576</strong></td>
      <td>0.514</td>
      <td>0.232</td>
      <td>1.710</td>
      <td>0.469</td>
      <td>0.454</td>
      <td><strong>0.310</strong></td>
    </tr>
    <tr>
      <td></td>
      <td>&#10003;</td>
      <td>&#10003;</td>
      <td>&#10003;</td>
      <td style="background-color: #f5f5f5;"><strong>0.897</strong></td>
      <td>0.206</td>
      <td>1.662</td>
      <td><strong>0.495</strong></td>
      <td><strong>0.516</strong></td>
      <td><strong>0.419</strong></td>
      <td><strong>0.825</strong></td>
      <td>0.179</td>
      <td><strong>0.515</strong></td>
      <td>0.574</td>
      <td><strong>0.538</strong></td>
      <td>0.232</td>
      <td>1.662</td>
      <td><strong>0.476</strong></td>
      <td><strong>0.459</strong></td>
      <td>0.301</td>
    </tr>
  </tbody>
</table>


</div>