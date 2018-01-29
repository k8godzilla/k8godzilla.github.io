---
layout:     post
title:      Lecture Notes 07
subtitle:   Reinforcement Learning - David Silver's Course
date:       2018-01-29
author:     Sun Yin
header-img: img/rlsilver/fengmian.png
catalog: true
tags:
    - Reinforcement Learning
---
## Lecture 07

**1. Introduction**

**2. Finite Difference Policy Gradient**

**3. Monte-Carlo Policy Gradient**

**4. Actor-Critic Policy Gradient**

---

### 1. Introduction

**1.1** What is the advantage of policy gradient campared to value based algorithm?

**1.2** How to compute $$J(\theta)$$ in episodic and continuing enviroments.

### 2. Finite Difference Policy Gradient

**2.1** What is policy gradient like?

### 3. Monte-Carlo Policy Gradient

**3.1** What is *score function*? How to derive it?

**3.2** What is *softmax policy*? What is its score function?

**3.3** What is *gaussian policy*? What is its score function?

**3.4** How to use score function to compute policy gradient $${ \triangledown  }_{ \theta  }J\left( \theta  \right) $$?

**3.5** What is *policy gradient theorem*?

**3.6** Write down the pseudocode of *Monte-Carlo policy gradient Algorithm*.

### 4. Actor-Critic Policy Gradient

**4.1** Write down the pseudocode of *Actor-Critic policy gradient algorithm* with TD(0) as update method of critic.

**4.2** what is compatoble function approximation theorem? How to prove?

**4.3** How to reduce varience in policy gradient?

**4.4** How to estimate *advantage function*? 

**4.5** Show the update of critic value function at different time scale.

**4.6** Show the estimation of gradient policy at different time scale(Monte-Carlo, TD(0), forward-view $$TD(\lambda)$$ and backward-view $$TD(\lambda)$$).

**4.7** Summarize all the policy gradient forms.





