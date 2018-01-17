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

**Row Space**

$${v}_{1}, {v}_{2}, ..., {v}_{r}$$ is orthogonal basis of row space of A.

**Column Space**

$${u}_{1}=A{v}_{1}, {u}_{2}=A{v}_{2}, ...{u}_{r}=A{v}_{r}$$ is corresponding basis of column space of A.

**sigma**

To make u be a unit length vector, we introduce stretch coef $${\sigma}$$:

$$
A{ v }_{ 1 }={ \sigma  }_{ 1 }{ u }_{ 1 },\quad A{ v }_{ 2 }={ \sigma  }_{ 2 }{ u }_{ 2 }\quad ,...,\quad A{ v }_{ r }={ \sigma  }_{ r }{ u }_{ r }
$$

**Matrix Form**

$$
A\begin{bmatrix} { v }_{ 1 } & { v }_{ 2 } & ... & { v }_{ r } & { v }_{ r+1 } & ... & { v }_{ n } \end{bmatrix}=\begin{bmatrix} { u }_{ 1 } & { u }_{ 2 } & ... & { u }_{ r } & { u }_{ r+1 } & ... & { u }_{ n } \end{bmatrix}\begin{bmatrix} { \sigma  }_{ 1 } &  &  &  \\  & { \sigma  }_{ 2 } &  &  \\  &  & ... &  \\  &  &  & ... \end{bmatrix}
$$

$$
\\ AV=U\Sigma \quad \Rightarrow \quad A=U\Sigma { V }^{ -1 }\quad \overset { \boxed { 1 }  }{ = } \quad U\Sigma { V }^{ T }\\ \\ \boxed { 1 } -V\quad is\quad orthogonol
$$

So the key is to find a set of orthogonal basis of A's rowspace that make sure $${u}_{i}=A{v}_{i}$$ is still orthogonal in column space.

**How to find V And U**

$$
A{ A }^{ T }=U\Sigma { V }^{ T }V{ \Sigma  }^{ T }{ U }^{ T }=V{ \Sigma  }^{ T }\Sigma { V }^{ T }=V\begin{bmatrix} { \sigma  }_{ 1 }^{ 2 } &  &  &  \\  & { \sigma  }_{ 2 }^{ 2 } &  &  \\  &  & ... &  \\  &  &  & ... \end{bmatrix}{ V }^{ T }
$$

V is the eigenvectors of $${A}^{T}A$$.

$$
A{ A }^{ T }=U\Sigma { V }^{ T }V{ \Sigma  }^{ T }{ U }^{ T }=V{ \Sigma  }^{ T }\Sigma { V }^{ T }=U\begin{bmatrix} { \sigma  }_{ 1 }^{ 2 } &  &  &  \\  & { \sigma  }_{ 2 }^{ 2 } &  &  \\  &  & ... &  \\  &  &  & ... \end{bmatrix}U^{ T }
$$

U is the eigenvectors of $$A{A}^{T}$$. And $$\Sigma$$ is the sqaured root of $$A{A}^{T}$$ and $${A}^{T}A$$.

**Example**

$$
A=\begin{bmatrix} 4 & 4 \\ -3 & 3 \end{bmatrix}
$$

Eigendecompose of $${A}^{T}A$$

$$
{ A }^{ T }A=\begin{bmatrix} 25 & 7 \\ 7 & 25 \end{bmatrix},\quad { s }_{ 1 }=32,\quad { x }_{ 1 }=\frac { 1 }{ \sqrt { 2 }  } \begin{bmatrix} 1 \\ 1 \end{bmatrix},\quad { s }_{ 2 }=18,\quad { x }_{ 1 }=\frac { 1 }{ \sqrt { 2 }  } \begin{bmatrix} 1 \\ -1 \end{bmatrix}
$$

Eigendecompose of $$A{A}^{T}$$

$$
A{ A }^{ T }=\begin{bmatrix} 32 & 0 \\ 0 & 18 \end{bmatrix},\quad { s }_{ 1 }=32,\quad { x }_{ 1 }=\begin{bmatrix} 1 \\ 0 \end{bmatrix},\quad { s }_{ 2 }=18,\quad { x }_{ 1 }=\begin{bmatrix} 0 \\ 1 \end{bmatrix}
$$

The SVD result is 

$$
A=\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}\begin{bmatrix} 32 & 0 \\ 0 & 18 \end{bmatrix}\begin{bmatrix} { 1 }/{ \sqrt { 2 }  } & { 1 }/{ \sqrt { 2 }  } \\ { 1 }/{ \sqrt { 2 }  } & { -1 }/{ \sqrt { 2 }  } \end{bmatrix}
$$

**SVD and Four Subspaces**

* $${v}_{1}$$, $${v}_{2}$$, ...,$${v}_{r}$$ is the orthogonal basis for rowspace.
* $${u}_{1}$$, $${u}_{2}$$, ...,$${u}_{r}$$ is the orthogonal basis for columnspace.
* $${v}_{r+1}$$, $${v}_{r+2}$$, ...,$${v}_{n}$$ is the orthogonal basis for $$N(A)$$.
* $${u}_{r+1}$$, $${u}_{r+2}$$, ...,$${u}_{m}$$ is the orthogonal basis for $$N({A}^{T})$$.




