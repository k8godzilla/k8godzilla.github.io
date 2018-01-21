---
layout:     post
title:      Lecture Notes 01 
subtitle:   Reinforcement Learning - David Silver's Course
date:       2018-01-20
author:     Sun Yin
header-img: img/rlsilver/fengmian.png
catalog: true
tags:
    - Reinforcement Learning
---
## Lecture 01

**1. The RL Problem**

**2. Inside An RL Agent**

**3. Problems within RL**

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
* An information state (a.k.a Markov state) contains all uesful information from the history. The formal definition is:

 A state $${S}_{t]$$ is Markov if and only if

 $$
 P\left[ { S }_{ t+1 }|{ S }_{ t } \right] =P\left[ { S }_{ t+1 }|{ S }_{ 1 },...,{ S }_{ t } \right] 
 $$

* A process is a **Markov decision process** if it satisfies full ovservability condition: $${O}_{t}={S}_{t}^{a}={S}_{t}^{e}$$.
* A process is a **partially observable Markov decision process** if agent indirectly observes enviroment(such as Poker game).


### 2. Inside An RL Agent

An RL agent may consist of one or more of these three components: policy, value function and model.

* **Policy**

Polocy is a map from the state to action. 

Deterministic policy: $$a=\pi (s)$$. 

Stochastic policy: $$\pi(a|s)=P\left[ { A }_{ t }=a|{ S }_{ t }=s \right]$$.

* **Value funtion**

$$
{ v }_{ \pi  }(s)={ E }_{ \pi  }\left[ { R }_{ t+1 }+\gamma { R }_{ t+2 }+{ \gamma  }^{ 2 }{ R }_{ t+3 }+...|{ S }_{ t }=s \right] 
$$

* **Model** 

Model predicts next state and next(immediate) reward

$$
{ P }_{ s{ s }^{ ' } }^{ a }=P\left[ { S }_{ t+1 }={ s }^{ ' }|{ S }_{ t }=s,{ A }_{ t }=a \right] 
$$

$$
{ R }_{ s }^{ a }=E\left[ { R }_{ t+1 }|{ S }_{ t }=s,{ A }_{ t }=a \right] 
$$

### 3. Problems within RL

* **Learning and Planing**

If the enviroment is initially unknown, the problem is reinforcement learning. If the enviroment us known, the problem is planning. 

* **Exploration and Exploitation**

There is a tradeoff between exploration and exploitation in reinforcement learning. Exploration helps us to find more information about the enviroment(try a new restaurant), while exploition exploits knwon information to maximize reward(go to favourite restaurant).

* **Prediction and Control**

Given policy, evaluating the future, it's prediction.

Optimising the future, it's control.

