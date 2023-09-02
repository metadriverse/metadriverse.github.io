---
layout: page-center
permalink: /metadrive-simulator/
title: MetaDrive
description: "MetaDrive: Composing Diverse Driving Scenarios for Generalizable Reinforcement Learning"
nav: true
nav_order: 1
---

<div class="col-12 md-5"  align="center">
    <h6 style="text-align: center">
        <a href="https://github.com/metadriverse/metadrive" style="color: black;"><b>Code</b></a> |
        <a href="https://arxiv.org/pdf/2109.12674.pdf" style="color: black;"><b>Paper</b></a> |
        <a href="https://metadrive-simulator.readthedocs.io/en/latest/" style="color: black;"><b>Documentation</b></a> |
        <a href="https://www.youtube.com/embed/3ziJPqC_-T4" style="color: black;"><b>Demo Video</b></a>
    </h6>
</div>



<div class="news-container">
    <p><br>
            <h3>News</h3>
        <ul>
            <li>
                Sep 2, 2023: <a class="bar" href="../scenarionet/"><b>ScenarioNet</b></a>, a platform for large-scale scenario modeling, is released!
            </li>
            <li>
                Oct 22, 2022: Benchmark results of MARL environments are provided in <a class="bar" href="https://github.com/metadriverse/metadrive-benchmark"><b>metadrive-benchmark</b></a>!
            </li>
            <li>
                May 3, 2022: MetaDrive 0.2.5 was released!
            </li>
            <li>
                Mar 28, 2022: MetaDrive <a class="bar" href="https://arxiv.org/pdf/2109.12674.pdf"><b>white paper</b></a> was accepted to TPAMI!
            </li>
        </ul>
    </p>
</div>



<div class="metadrive">
  {% for post in site.metadrive %}
  <div class="container metadrive">
    <div class="text">
      <h2>{{ post.title }}</h2>
      <p>{{ post.content }}</p>
    </div>
    <div class="image">
      {% if post.img %}
        <img src="{{ post.img | relative_url }}" alt="{{ post.title }}" />
      {% else %}
        {% if post.video %}
        <video autoplay loop muted>
          <source src="{{ post.video | relative_url }}" type="video/mp4">
          Your browser does not support the video tag.
        </video>
        {% else %}
          {% if post.youtube_id %}
            <iframe width="560" height="315" src="https://www.youtube.com/embed/{{ post.youtube_id }}?autoplay=1&loop=1&mute=1&playlist={{ post.youtube_id }}" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          {% endif %}
        {% endif %}
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>




<div class="bibtex">
    <h3>Reference</h3>
    Please refer to the <a href="https://arxiv.org/pdf/2109.12674.pdf">technical report</a> or the <a href="https://github.com/metadriverse/metadrive">code repo</a> for more information.
    <pre>
@article{li2021metadrive,
title={Metadrive: Composing diverse driving scenarios for generalizable reinforcement learning},
author={Li, Quanyi and Peng, Zhenghao and Feng, Lan and Zhang, Qihang and Xue, Zhenghai and Zhou, Bolei},
journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
year={2022}
}
    </pre>
</div>