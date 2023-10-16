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
---


### News

* Sep 2, 2023: <a class="bar" href="../scenarionet/"><b>ScenarioNet</b></a>, a platform for large-scale scenario modeling, is released!
* Oct 22, 2022: Benchmark results of MARL environments are provided in <a class="bar" href="https://github.com/metadriverse/metadrive-benchmark"><b>metadrive-benchmark</b></a>!
* Mar 28, 2022: MetaDrive <a class="bar" href="https://arxiv.org/pdf/2109.12674.pdf"><b>white paper</b></a> was accepted to TPAMI!


### MetaDrive Simulator

To facilitate the research of generalizable reinforcement learning, we develop an open-source, highly efficient and flexible driving simulator MetaDrive, which holds the following key features:

* Modular
* Lightweight
* Customizable
* Realistic

We construct a variety of RL tasks and baselines in both single-agent and multi-agent settings, including benchmarking
generalizability across unseen scenes, safe exploration, and modeling multi-agent behaviors.

Empowered by ***[ScenarioNet](../scenarionet)***, all features of MetaDrive can be applied to 
the virtual environments reconstructed from the open-source dataset, such as Waymo Open Dataset, nuPlan, and L5.


### Reference

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
