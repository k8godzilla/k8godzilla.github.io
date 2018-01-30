---
layout:     post
title:      Lecture Notes 02
subtitle:   Reinforcement Learning - David Silver's Course
date:       2018-01-21
author:     Sun Yin
header-img: img/rlsilver/fengmian.png
catalog: true
tags:
    - Reinforcement Learning
---
## Lecture 01

**1. Markov Process**

**2. Markov Reward Process**

**3. Markov Decision Process**

**4. Extension to MDPs**

---

### 1. Markov Process

* **Simple Introduction**

In Markov decision process, the environment is fully observable. And almost all RL problem can be formalised as MDPs.

* **Markov Property**

$$
P\left[ { S }_{ t+1 }|{ S }_{ t } \right] =P\left[ { S }_{ t+1 }|{ S }_{ 1 },...,{ S }_{ t } \right] 
$$

* **State Transition Matrix**

$$
P=\begin{bmatrix} { P }_{ 11 } & { P }_{ 12 } & ... & { P }_{ 1n } \\ { P }_{ 21 } & { P }_{ 22 } & ... & { P }_{ 2n } \\ ... & ... & ... & ... \\ { P }_{ n1 } & { P }_{ n2 } & ... & { P }_{ nn } \end{bmatrix}
$$

$$
{ P }_{ s{ s }^{ ' } }=P\left[ { S }_{ t+1 }={ s }^{ ' }|{ S }_{ t }=s \right] 
$$

* **Markov Process**

Markov process is tuple - $$<S, P>$$


### 2. Markov Reward Process

* **Definition**

Markov reward process is a tuple $$<S, P, R, \gamma>$$.

$$
{ R }_{ s }=E\left[ { R }_{ t+1 }|{ S }_{ t }=s \right] 
$$

$$\gamma$$ is a discount factor, $$\gamma \in \left[ 0,\quad 1 \right] $$.

* **Return**

$$
{ G }_{ t }={ R }_{ t+1 }+\gamma { R }_{ t+2 }+...=\sum _{ k=0 }^{ \infty  }{ { \gamma  }^{ k }{ R }_{ t+k+1 } } 
$$

* **Why discount?**

1. Avoid infinite.
2. Uncertainty. The future may not be fully represented by model.
3. Animal/human behabiour shows preference for immediate reward.

* **Value Function**

$$
v(s)=E\left[ { G }_{ t }|{ S }_{ t }=s \right] 
$$

* **Bellman Equation**

$$
v(s)=E\left[ { R }_{ t+1 }+\gamma v\left( { S }_{ t+1 } \right) |{ S }_{ t }=s \right] 
$$

![](/img/rlsilver/bellman.png)

$$
v(s)={ R }_{ s }+\gamma \sum _{ { s }^{ ' }\in S }^{  }{ { P }_{ s{ s }^{ ' } }v\left( { s }^{ ' } \right)  } 
$$

* **Bellman Equation in Matrix**


