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

here,$$Q:\text{quality, Q-table}, S:\text{state}, a:\text{action}, \alpha: \text{learning rate},r:\text{reward}, \lambda: \text{discount, for blancing the short-term reward and long-term reward.}$$

For more details, see [my GitHub](https://github.com/oudeng/Reinforcement_Learning){:target="_blank"}.

### Method-1
$$ f(x)=\left\{
\begin{aligned}
x & = & \cos(t) \\
y & = & \sin(t) \\
z & = & \frac xy
\end{aligned}
\right.
$$

### Method-2
$$ F^{HLLC}=\left\{
\begin{array}{rcl}
F_L       &      & {0      <      S_L}\\
F^*_L     &      & {S_L \leq 0 < S_M}\\
F^*_R     &      & {S_M \leq 0 < S_R}\\
F_R       &      & {S_R \leq 0}
\end{array} \right. $$


### Method-3
$$f(x)=
\begin{cases}
0& \text{x=0}\\
1& \text{x!=0}
\end{cases}$$

If not work, try http://feigeek.com/posts/b1bbb984.html



