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

## Why multiagent simulation?
Multiagent simulation is a visual technology assisting in understanding natural or systemic dynamics. 
The such simulation consists of action rules and agent strategies in a designed environment. 
The interactions of agent-environment and agent-agent as markovian processes provide observation or insight into system dynamics. 
The essence of the art of multiagent simulation is the abstraction and simplification of the real world.

## A preliminary survey for suitable methods of multiagent simulation

`My standards of *suitable*:`  
- Open source with detailed description
- Python 3.8+
- Reinforcement learning compatible
- PyTorch based method prefer

### [VMAS](https://github.com/oudeng/VectorizedMultiAgentSimulator){:target="_blank"}  

PyTorch based high ranked multiagent simulation tool with the latest updates.  

### [mesa](https://github.com/oudeng/mesa){:target="_blank"}  

<iframe width="871" height="490" src="https://www.youtube.com/embed/1wa9lysIaD8" title="Tutorial - Agent Based Modelling In Python" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

A recent youtube content.

### [pyNetlogo](https://github.com/oudeng/pyNetLogo){:target="_blank"}  

Not competible for Python 3.9, but 3.8 is fine.  
<iframe width="871" height="490" src="https://www.youtube.com/embed/qLBzT85Z-aM" title="Python + Netlogo = PyNetlogo Tutorial pt. 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Reference:  
[https://github.com/topics/multi-agent-simulation](https://github.com/topics/multi-agent-simulation){:target="_blank"}


