---
layout: research
permalink: /metadrive-simulator/
title: MetaDrive
page_title: MetaDrive
description: "MetaDrive: Composing Diverse Driving Scenarios for Generalizable Reinforcement Learning"
nav: true
nav_order: 1
code_link: https://github.com/metadriverse/metadrive
pdf_link: https://arxiv.org/pdf/2109.12674.pdf
doc_link: https://metadrive-simulator.readthedocs.io/en/latest/
video_link: https://www.youtube.com/embed/3ziJPqC_-T4
redirect_from:
    - /metadrive
    - /md
---

<video style="display:block; width:100%; height:auto;" autoplay="autoplay" muted loop="loop" controls playsinline><source src="https://raw.githubusercontent.com/decisionforce/archive/master/MetaDrive/metadrive_teaser.mp4" type="video/mp4"/></video>


<!--research-section-splitter-->


## MetaDrive Simulator

To facilitate the research of generalizable reinforcement learning, we develop an open-source, highly efficient and flexible driving simulator MetaDrive, which holds the following key features:

* Modular
* Lightweight
* Customizable
* Realistic

We construct a variety of RL tasks and baselines in both single-agent and multi-agent settings, including benchmarking
generalizability across unseen scenes, safe exploration, and modeling multi-agent behaviors.

Empowered by ***[ScenarioNet](../scenarionet)***, all features of MetaDrive can be applied to 
the virtual environments reconstructed from the open-source dataset, such as Waymo Open Dataset, nuPlan, and L5.


<!--research-section-splitter-->


## Reference

Please refer to the [technical report](https://arxiv.org/pdf/2109.12674.pdf) or 
the [code repo](https://github.com/metadriverse/metadrive) for more information.

```plain
@article{li2021metadrive,
  title={Metadrive: Composing diverse driving scenarios for generalizable reinforcement learning},
  author={Li, Quanyi and Peng, Zhenghao and Feng, Lan and Zhang, Qihang and Xue, Zhenghai and Zhou, Bolei},
  journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year={2022}
}
```
