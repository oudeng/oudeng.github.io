---
layout: post
title: "Q-learning and Bellman Equation"
categories:
 - Reinforcement learning
 - Python
tags: [Q-learning, Bellman equation]
---

The fundamental reinforcement algorithm: Q learning and Bellman equation. Experiment on a simple Atari game: Frozen Lake.  
Done of 4x4, 5x5 and 8x8 map(s).

<!--more-->

## Bellman equation
$$Q(S_t, a_t) \leftarrow Q(S_t, a_t)+\alpha [r_{t+1}+\lambda \sideset{}{}{max}_a (S_t,a)-Q(S_t, a_t))]$$  

$$
begin{aligned}
x &= v_0costheta t 
y &= v_0sintheta t - frac{1}{2}gt^2 
end{aligned}
$$

here,$$Q:\text{quality, Q-table}, S:\text{state}, a:\text{action}, \alpha: \text{learning rate},r:\text{reward}, \lambda: \text{discount, for blancing the short-term reward and long-term reward.}$$

For more details, see [my GitHub](https://github.com/oudeng/Reinforcement_Learning){:target="_blank"}.