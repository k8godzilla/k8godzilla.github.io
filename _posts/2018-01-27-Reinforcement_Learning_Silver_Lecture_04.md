---
layout:     post
title:      Lecture Notes 04
subtitle:   Reinforcement Learning - David Silver's Course
date:       2018-01-27
author:     Sun Yin
header-img: img/rlsilver/fengmian.png
catalog: true
tags:
    - Reinforcement Learning
---
## Lecture 04

**1. Monte-Carlo Learning**

**2. Temporal-Difference Learning**

**3. $$TD(\lambda)$$**

---

### 1. Monte-Carlo Learning

**1.1** Describe First-Visit and Every-Visit Monte-Carlo policy evaluation.

**1.2** What's the two updates method in incremental Monte-Carlo updates?

### 2. Temporal-Difference Learning

**2.1** How $$V({S}_{t})$$ is updated in the situation of $$TD(0)$$? What is *TD target* and *TD error*?

**2.2** What is the advantages and disadvantages of *TD method* comapared to *Monte-Carlo method*?

**2.3** What is the bias/varience tradeoff of *TD method* and *Monte-Carlo Method*?

**2.4** In the AB example, what is $$V(A)$$?

**2.5** What is the convergence direction of *MC method* and *TD method*?

**2.6** What is the tree graph of *MC method*, *TD method* and *Dynmamic Programming*?

**2.7** What is the *sampling* and *bootstrappint* overview of reinforcement learning? 

### 3. $$TD(\lambda)$$

**3.1** What is *n-Step TD*?

**3.2** What is *forward view of $$TD(\lambda)$$*?

**3.3** What is *backward view of $$TD(\lambda)$$*?

**3.4** Prove that backward view of $$TD(\lambda)$$ is equivalent to $$TD(0)$$ when $${\lambda}=0$$.

**3.5** Prove that backward view of *$$TD(\lambda)$$* is equivalent to *MC method* when $${\lambda}=1$$.

**3.6** In offline updates, what is the relation between forward view and backward view of $$TD(\lambda)$$?

**3.7** Prove that in offline situation for general $$\lambda$$, the forward and backward view of $$TD(\lambda)$$ is equivalent.

**3.8** Summarize the equivalence of forward and backward view of $$TD(\lambda)$$ in offline and online updates.






