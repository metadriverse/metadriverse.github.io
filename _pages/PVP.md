---
layout: research
permalink: /pvp/
title: "PVP: Learning from Active Human Involvement"
page_title: "Learning from Active Human Involvement through Proxy Value Propagation"
description: "<h3>NeurIPS 2023 <b>Spotlight</b></h3>"
authors:

- {name: "Zhenghao Peng", url: "https://pengzhenghao.github.io", institution: "1"}
- {name: "Wenjie Mo", url: "https://wenjie-mo.github.io/", institution: "1"}
- {name: "Chenda Duan", url: "https://chendaduan.com/", institution: "1"}
- {name: "Quanyi Li", url: "https://quanyili.github.io", institution: "2"}
- {name: "Bolei Zhou", url: "https://boleizhou.github.io", institution: "1"}

institutions:

- {name: "University of California, Los Angeles", institution: "1"}
- {name: "University of Edinburgh", institution: "2"}

nav: false
nav_order: 1
code_link: https://github.com/metadriverse/PVP
pdf_link: https://openreview.net/pdf?id=q8SukwaEBy
poster_link: ../assets/img/pvp/PVP-Poster.pdf
---


<div class="embed-responsive embed-responsive-16by9">
    <video width="100%" max-width="800px" loop autoplay muted playsinline src="../assets/img/pvp/Teaser-Video-Compressed2.mp4">
    </video>
</div>


<!--research-section-splitter-->

## Summary

**Proxy value propagation (PVP)** is a human-in-the-loop policy learning method.

* PVP is reward-free, avoiding sophisticated reward engineering.
* PVP learns from online human interventions and demonstrations, 
ensuring the training-time safety and benefited from corrective feedback.

In real-human experiments on various tasks and various control devices,

* PVP achieves 10x improvement in learning efficiency;
* PVP greatly boosts the agent's training-time and test time safety performance;
* PVP makes human subjects feel better according to an user study.

<!--research-section-splitter-->

## Human-AI Shared Control


<div class="img-container" style="width: 100%; margin: 0 auto;">
    <img src="../assets/img/pvp/comparison.png" class="my-image" alt="Image" />
</div>

<br>

Among different forms of human-in-the-loop approaches, we focus on the **active human involvement**, 
where human experts oversee the exploration processes of the learning agent so that the safety of human-AI system
is ensured.


As shown in the teaser videos, in training-time, the human experts can intervene and provide corrective demonstrations. 
We will discuss how to learn performant and human-aligned policies with the data from human-AI shared control
**without reward function** in the following section.

<!--research-section-splitter-->

## Proxy Value Propagation

We learn a **proxy value function** along with the policy during human-AI shared control.

---

<div class="img-container" style="width: 100%; margin: 0 auto;">
    <img src="../assets/img/pvp/trajectory.png" class="my-image" alt="Image" />
</div>

As illustrated in the figure above, we categorize the data into two partitions:

1. The agent's exploratory trajectories;
2. The human-involved trajectories.

**The agent's exploratory trajectories**: The state transitions $$(s, a, s')$$ during agent's exploration will be stored in the Novice Buffer $$\mathcal B_n$$. Note that our method is **reward-free** so no reward is available.


**The human-involved trajectories**: The actions $$a_h$$ provided by the human are applied to the environment, 
while the agent's actions $$a_n$$ are concurrently recorded. 
The state transitions $$(s, a_h, a_n, s')$$ will be stored in the Human Buffer $$\mathcal B_h$$. Again, no reward is stored.

---


<div class="img-container" style="width: 50%; margin: 0 auto;">
    <img src="../assets/img/pvp/method-1.png" class="my-image" alt="Image" />
</div>


The key insight of this paper is to build a proxy value function that induces human-aligned actions and
integrate the proxy value function into a value-based RL framework.

During these human-involved transitions, we optimize the proxy values to ensure the human action approximates a value close to 1, 
while the intervened agent actions approximate a value close to -1:
<div class="img-container" style="width: 60%;">
    <img src="../assets/img/pvp/method-2-pv.png" class="my-image" alt="Image" />
</div>

<br>

The proxy value network $$Q_\theta$$ is updated with both the proxy value objective and the TD objective so that
the proxy value is propagated:
<div class="img-container" style="width: 60%;">
    <img src="../assets/img/pvp/method-3-td.png" class="my-image" alt="Image" />
</div>
<div class="img-container" style="width: 33%;">
    <img src="../assets/img/pvp/method-4-total.png" class="my-image" alt="Image" />
</div>


<br>

We then use value-based RL method like TD3 or DQN to optimize the policy with the proxy value function.



<!--research-section-splitter-->

## Experiment

Compared to the RL baselines, our method PVP achieves unprecedented learning efficiency:

<div class="img-container">
    <img src="../assets/img/pvp/MainExp.jpg" class="my-image" alt="Image" />
</div>


<br>

Our method PVP uses fewer demonstrations but achieves less training-time safety violation and better final performance in the MetaDrive environment.

<div class="img-container" style="width: 80%; margin: 0 auto;">
    <img src="../assets/img/pvp/Table.png" class="my-image" alt="Image" />
</div>


<!--research-section-splitter-->



## Reference

```plain
@article{peng2023learning,
  title={Learning from Active Human Involvement through Proxy Value Propagation},
  author={Peng, Zhenghao and Mo, Wenjie and Duan, Chenda and Li, Quanyi and Zhou, Bolei},
  journal={Advances in Neural Information Processing Systems},
  year={2023}
}   
```

<br>

## Acknowledgement

This work was supported by the National Science Foundation under Grant No. 2235012. The human experiment in this study is approved through the IRB#23-000116 at UCLA.