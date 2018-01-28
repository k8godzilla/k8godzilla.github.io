---
layout:     post
title:      Lecture Notes 05
subtitle:   Reinforcement Learning - David Silver's Course
date:       2018-01-27
author:     Sun Yin
header-img: img/rlsilver/fengmian.png
catalog: true
tags:
    - Reinforcement Learning
---
## Lecture 05

**1. On-Policy Monte-Carlo Control**

**2. On-Policy Temporal-Difference Learning**

**3. Off-Policy Learning**

**4. Summary**

---

### 1. On-Policy Monte-Carlo Control

**1.1** In Monte-Carlo control, does policy evaluation base on state value or state-action value? Why?

**1.2** What is $$\epsilon-Greedy Exploration$$?

**1.3** Prove that $$\epsilon-greedy$$ ensures improvement on q value.

**1.4** What is *GLIE*? How to fulfill it?

**1.5** What is *GLIE Monte-Carlo Control*?

### 2. On-Policy Temporal-Difference Learning

**2.1** What is Sarsa algorithm?

**2.2** What is the condition that ensure *Sarsa's convergence*?

**2.3** What is *n-step Sarsa*?

**2.4** What is *forward view $$Sarsa(\lambda)$$*?

**2.5** What is *backward view $$Sarsa(\lambda)$$*?

**2.6** Explain the advantage of $$Sarsa(\lambda)$$ in gridworld example.

### 3. Off-Policy Learning

**3.1** What is *importance sampling*? Compared to *importance sampling for MC*, what's the advantage of *importance sampling for TD*?

**3.2** What is *Q-learning*? What is the *behaviour policy* of Q-learning? What is the *target policy* of Q-learning? 

### 4. Summary

**4.1** Summarize the learning method in 2-D tables. The column is *DP* and *TD*, the row is $${ v }_{ \pi  }(s)$$, $${ q }_{ \pi  }(s,a)$$ and $${ q }_{ * }(s,a)$$. 
