---
layout:     post
title:      Lecture 29 (Linear Algebra)
subtitle:   
date:       2018-01-16
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 29

**1. Definition of SVD**

**2. From Row Space, Column Space To SVD**

---

### 1. Definition of SVD

Any m by n matrix A can be decomposed into form $$A=U{\Sigma}{V}^{T}$$, where $${\Sigma}$$ is a diagnol matrix and U, V are orthogonal matrices.

### 2. From Row Space, Column Space To SVD

*Row Space*

$${v}_{1}, {v}_{2}, ..., {v}_{r}$$ is orthogonal basis of row space of A.

*Column Space*

$${u}_{1}=A{v}_{1}, {u}_{2}=A{v}_{2}, ...{u}_{r}=A{v}_{r}$$ is corresponding basis of column space of A.

*sigma*

To make u be a unit length vector, we introduce stretch coef $${\sigma}$$:

$$
A{ v }_{ 1 }={ \sigma  }_{ 1 }{ u }_{ 1 },\quad A{ v }_{ 2 }={ \sigma  }_{ 2 }{ u }_{ 2 }\quad ,...,\quad A{ v }_{ r }={ \sigma  }_{ r }{ u }_{ r }
$$

*Matrix Form*

$$
A\begin{bmatrix} { v }_{ 1 } & { v }_{ 2 } & ... & { v }_{ r } & { v }_{ r+1 } & ... & { v }_{ n } \end{bmatrix}=\begin{bmatrix} { u }_{ 1 } & { u }_{ 2 } & ... & { u }_{ r } & { u }_{ r+1 } & ... & { u }_{ n } \end{bmatrix}\begin{bmatrix} { \sigma  }_{ 1 } &  &  &  \\  & { \sigma  }_{ 2 } &  &  \\  &  & ... &  \\  &  &  & ... \end{bmatrix}
$$

$$
\\ AV=U\Sigma \quad \Rightarrow \quad A=U\Sigma { V }^{ -1 }\quad \overset { \boxed { 1 }  }{ = } \quad U\Sigma { V }^{ T }\\ \\ \boxed { 1 } -V\quad is\quad orthogonol
$$

So the key is to find a set of orthogonal basis of A's rowspace that make sure $${u}_{i}=A{v}_{i}$$ is still orthogonal in column space.
