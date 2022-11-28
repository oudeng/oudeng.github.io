---
layout: post
title: "Multiagent simulation: pyNetlogo+Netlogo or mesa or VMAS"
categories:
 - Python
 - Reinforce learning
tags: [Netlogo, Python-Netlogo API, Multiagent simulation]
---

Based on a specific NetLogo program, I plan to develop it further with reinforcement learning, 
consisting of a preliminary survey for suitable methods of multiagent simulation in a Python 3.8+ environment. 

<!--more-->

## Why multiagent simulation?
Multiagent simulation is a visual technology assisting in understanding natural or systemic dynamics. 
The such simulation consists of action rules and agent strategies in a designed environment. 
The interactions of agent-environment and agent-agent as markovian processes provide observation or insight into system dynamics. 
The essence of the art of multiagent simulation is the abstraction and simplification of the real world.

## A preliminary survey for suitable methods of multiagent simulation

> My standards of "suitable":
> - Open source with detailed description.
> - Python 3.8+
> - Reinforcement learning
> - If possible, PyTorch based.

### [VMAS](https://github.com/oudeng/VectorizedMultiAgentSimulator){:target="_blank"}  

PyTorch based with the latest updates.

### [mesa](https://github.com/oudeng/mesa){:target="_blank"}  

<iframe width="1000" height="400" src="https://www.youtube.com/embed/1wa9lysIaD8" title="Tutorial - Agent Based Modelling In Python" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

A recent youtube content.

### [pyNetlogo](https://github.com/oudeng/pyNetLogo){:target="_blank"}  

Not competible for Python 3.9, but 3.8 is fine.  
<iframe width="1000" height="400" src="https://www.youtube.com/embed/qLBzT85Z-aM" title="Python + Netlogo = PyNetlogo Tutorial pt. 1" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Reference:  
[https://github.com/topics/multi-agent-simulation](https://github.com/topics/multi-agent-simulation){:target="_blank"}


<!--
Reference:  
https://github.com/topics/multi-agent-simulation

One of the rewards of switching my website to [Jekyll](http://jekyllrb.com/) is the
ability to support **MathJax**, which means I can write LaTeX-like equations that get
nicely displayed in a web browser, like this one \\( \sqrt{\frac{n!}{k!(n-k)!}} \\) or
this one \\( x^2 + y^2 = r^2 \\).

[//]: # (哈哈我是注释，不会在浏览器中显示。)
[//]: ``` shift+@

![XXXXXXX](/assets/images/XXXXXX.png)

## heading line

{:target="_blank"}

 file is: ```markdown: redcarpet```
 
 {% highlight r %}
$$a^2 + b^2 = c^2$$
{% endhighlight %}


{% highlight r %}
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  tex2jax: {
    inlineMath: [['$','$'], ['\\(','\\)']],
    processEscapes: true
  }
});
</script>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
{% endhighlight %}
-->
