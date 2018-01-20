---
layout:     post
title:      Lecture Notes 01 (Reinforcement Learning - David Silver's Course)
subtitle:   
date:       2018-01-20
author:     Sun Yin
header-img: img/rlsilver/fengmian.png
catalog: true
tags:
    - Reinforcement Learning
---
## Lecture 01

**1. The RL Problem**

**2. Basis Change and Linear Transform**

---

### 1. The RL Problem

**Reward**

* A *reward* $${R}_{t}$$ is a scalar feedback signal which indicates how well agent is doing at time t.
* The goal of agent is to select actions to maximize total future reward so actions may have long term consequences and sometimes sacrificing immediate reward to gain long-term reward is preferable.
* Reinforcement learning is based on the reward hypothesis:

> All goals can be described by the maximization of expected cumulative reward.

**Enviroment**

![](/img/rlsilver/l1_env.png)

**State**

* The history is the sequence of observations, actions, rewards $${ H }_{ t }={ O }_{ 1 },{ R }_{ 1 }.{ A }_{ 1 },...,{ A }_{ t-1 },{ O }_{ t },{ R }_{ t }$$
* State is the infomation uesd to determine what happens next. It is the function of history: $${S}_{t}=f({H}_{t})$$.
* $${ S }_{ t }^{ e }$$ is the representation of enviroment and ususally not visible to agents.
* $${ S }_{ t }^{ a }$$ is the infomation used by reinforcemnt learning algorithms and can be function of history: $${S}_{t}^{a}=f({H}_{t})$$.
