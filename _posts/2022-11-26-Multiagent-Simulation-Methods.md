---
layout: post
title: "Multiagent simulation methods: pyNetlogo+Netlogo or mesa or VMAS"
categories:
 - Python
 - Reinforcement learning
tags: [Netlogo, Python-Netlogo API, Multiagent simulation, Reinforcement learning]
---

Based on a specific NetLogo program, I plan to develop it further with reinforcement learning, 
consisting of a preliminary survey for suitable methods of multiagent simulation in a Python 3.8+ environment. 
Meanwhile, my plan includes continuing to update the experiments of the candidate methods.

<!--more-->

# 2022-12-2 Updated. 
I tested ```pyNetlogo``` and ```mesa``` in the last few days. Though the both worked. ```pyNetlogo``` is no GUI on my mac environment; ```mesa``` lacks rich examples to study. The recently found item, VMAS, is a SOTA tool developed by the Cambridge team.

# 2022-22-26 Original contents
## Why multiagent simulation?
Multiagent simulation is a visual technology assisting in understanding natural or systemic dynamics. 
The such simulation consists of action rules and agent strategies in a designed environment. 
The interactions of agent-environment and agent-agent as markovian processes provide observation or insight into system dynamics. 
The essence of the art of multiagent simulation is the abstraction and simplification of the real world.

## A preliminary survey for suitable methods of multiagent simulation

#### My standards of suitable methods:
- Open source with detailed description
- Python 3.8+
- Reinforcement learning compatible
- PyTorch based prefer

### [VMAS](https://github.com/oudeng/VectorizedMultiAgentSimulator){:target="_blank"}  

PyTorch based high ranked multiagent simulation tool with the latest updates.  

Points:  
- VMAS is a vectorized framework designed for efficient MARL benchmarking. 
- Vectorization in PyTorch allows VMAS to perform simulations in a batch, seamlessly scaling to tens of thousands of parallel environments on accelerated hardware.
- VMAS has an interface compatible with OpenAI Gym and with the RLlib library, enabling out-of-the-box integration with a wide range of RL algorithms.
- Paper: [https://arxiv.org/abs/2207.03530](https://arxiv.org/abs/2207.03530){:target="_blank"}

![VMAS](/assets/images/20221126_VMAS_1.png)

<iframe width="900" height="433" src="https://www.youtube.com/embed/aaDRYfiesAY" title="VMAS: A Vectorized Multi-Agent Simulator for Collective Robot Learning" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### [mesa](https://github.com/oudeng/mesa){:target="_blank"}  

<iframe width="871" height="490" src="https://www.youtube.com/embed/1wa9lysIaD8" title="Tutorial - Agent Based Modelling In Python" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

A recent youtube content. Try it later.

### [pyNetlogo](https://github.com/oudeng/pyNetLogo){:target="_blank"}  

The official site: [https://pynetlogo.readthedocs.io/en/latest/install.html](https://pynetlogo.readthedocs.io/en/latest/install.html){:target="_blank"}

#### Note:
- Not competible for Python 3.9, but 3.8 is fine, according to the following youtube contents.
- Need to install JDK. JDK 17 confirmed. Not the latest version of JDK 19.
- ```On a Mac, only headless mode (without GUI) is supported.```, the comment in its official document.

<iframe width="871" height="490" src="https://www.youtube.com/embed/qLBzT85Z-aM" title="Python + Netlogo = PyNetlogo Tutorial pt. 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Reference:  
[https://github.com/topics/multi-agent-simulation](https://github.com/topics/multi-agent-simulation){:target="_blank"}

