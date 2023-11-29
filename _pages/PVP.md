---
layout: research
permalink: /pvp/
title: "PVP: Learning from Active Human Involvement"
page_title: "Learning from Active Human Involvement through Proxy Value Propagation"
description: "NeurIPS 2023"
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

---


**TL;DR** Training a policy with a human expert in the loop providing interventions and demonstrations, our method achieves 50x improvement in learning efficiency and greatly boost the agent's training-time and test time safety performance.

<!--research-section-splitter-->

## Proxy Value Propagation


We consider a human-AI shared control framework during training:


<div class="img-container" style="width: 80%; margin: 0 auto;">
    <img src="../assets/img/pvp/Framework-H.png" class="my-image" alt="Image" />
</div>


<br>

The key insight of the paper is to borrow the value-based RL framework but plugging in a proxy value function:

\begin{equation}
    J^\text{PV}(\theta) = 
    \mathbb E_{(s, a_n, a_h)}  [| Q_\theta (s, a_h) - 1 |^2  + | Q_\theta (s, a_n) + 1 |^2 ] I(s, a_n),
\end{equation}

wherein $$I(s, a_n)$$ is an indicator of whether at current step the human is intervening and $$a_n$$, $$a_h$$ are the agent's action and human's action. $$s$$ is the state and $$Q_\theta$$ is the proxy value network.
The $$J^\text{PV}(\theta)$$ basically assigns $$+1$$ to human actions and $$-1$$ to the intervened agent actions.



<br>

Adding the TD loss, we have the objective to update the proxy value. As PVP is **reward-free** does not require the reward, there is no reward term in the TD loss.

\begin{equation}
    J^\text{TD}(\theta) = \mathbb E_{(s, a, s')} | Q_\theta(s, a) -  \gamma \max_{a'} Q_{\hat{\theta}}(s', a') |^2.
\end{equation}



\begin{equation}
J(\theta) = J^\text{PV}(\theta) + J^\text{TD}(\theta) 
\end{equation}


<!--research-section-splitter-->

## Experiment

Compared to the pure RL method, our method PVP achieves unprecedented learning efficiency:

<div class="img-container">
    <img src="../assets/img/pvp/MainExp.jpg" class="my-image" alt="Image" />
</div>


<br>

Our method PVP uses fewer demonstrations but achieves less training-time safety violation and better final performance in the MetaDrive environment.

<div class="img-container" style="width: 80%; margin: 0 auto;">
    <img src="../assets/img/pvp/Table.png" class="my-image" alt="Image" />
</div>


[//]: # (<!--research-section-splitter-->)

[//]: # (## Experiment Footage)

[//]: # (Coming soon!)

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
