---
layout:     post
title:      Lecture 25 (Linear Algebra)
subtitle:   
date:       2018-01-12
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 25

**1. Symmetric Matrices**

**2. Positive Definite Matrices**

---

### 1. Symmetric Matrices

**Eigenvalues and Eigenvectors**

If $$A={A}^{T}$$, then all eigenvalues of A is real and the eigenvectors of A can be chosen to be perpendicular.(**can be chosen**: in case one eigenvalue corresponds to multiple independent eigenvectors).

**Diagonolization**

For a symmetric matrix A, because it has perpendicular eigenvectors, it can be diagonolized by orthogonal matrix.

$$
A=S\Lambda { S }^{ -1 }=Q\Lambda { Q }^{ T }
$$

**Why Symmetric Matrices' Eigenvalues is Real?**

$$
Ax=\lambda x\overset { conjugate }{ \Longrightarrow  } A\overset {  }{ \overset { - }{ x } =\overset { - }{ \lambda  }  } \overset { - }{ x } \overset { transpose }{ \Longrightarrow  } { \overset { \quad - }{ (x } ) }^{ T }A={ \overset { \quad - }{ (x } ) }^{ T }\overset { - }{ \lambda  } \quad \quad \quad \overset { right\quad multiple\quad x }{ \Longrightarrow  } \quad { \overset { \quad - }{ (x } ) }^{ T }Ax={ \overset { \quad - }{ (x } ) }^{ T }\overset { - }{ \lambda  } x\quad ----\boxed { 1 } 
$$

$$
Ax=\lambda x\overset { left\quad multiple\quad { \overset { \quad - }{ (x } ) }^{ T } }{ \Longrightarrow  } \quad { \overset { \quad - }{ (x } ) }^{ T }Ax={ \overset { \quad - }{ (x } ) }^{ T }\overset {  }{ \lambda  } x\quad ----\boxed { 2 } 
$$

Combine $$\boxed {1}$$ and $$\boxed {2}$$, we have $$\lambda =\overset { - }{ \lambda  } $$, $$\lambda$$ is real.

**Inner Product of Complex Vector**

Notice that

$$
(a+ib)(a+ib)={ a }^{ 2 }-{ b }^{ 2 }\\ (a+ib)(a-ib)={ a }^{ 2 }+{ b }^{ 2 }
$$

Therefor the inner product of two complex vectors is $${ \bar { v }  }^{ T }w$$ instead of $${v}^{T}w$$.

**Symmetrical Complex Matrix**

Similar to vector, the symmetrical complex matrices should be defined as $${ \bar { A }  }^{ T }=A$$, instead of $${A}^{T}=A$$.

**Symmetrical Matrices and Projection**

$$
A=Q\Lambda { Q }^{ T }={ \lambda  }_{ 1 }{ q }_{ 1 }{ q }_{ 1 }^{ T }+{ \lambda  }_{ 2 }{ q }_{ 2 }{ q }_{ 2 }^{ T }+...
$$

Every symmetical matrix is a combination of perpendicular projection matrix. The projection matrix is $${ P }_{ 1 }={ q }_{ 1 }{ ({ q }_{ 1 }^{ T }{ q }_{ 1 }) }^{ -1 }{ q }_{ 1 }^{ T }={ q }_{ 1 }{ q }_{ 1 }^{ T }$$. 

What is perpendicular projection matrix? 

Prject vector b by projection matrix $${P}_{1}$$, $${P}_{2}$$, ...,$${P}_{n}$$. The projection outcomes is perpendicular to each other is the projection matrix is perpendicular.

**Fact: Eigenvalues and Pivots**

If A is a symmetrical matrix, then the number of its positive eigenvalues equals to the number of its positive pivots.

### 2. Positive Definite Matrices

A positive definite matrix is firstly a symmetrical matrix, and it satifsfier conditions below:

All pivots are positive $$\Leftrightarrow $$ All eigenvalues are positive $$\Leftrightarrow $$ All subdeterminants are positive.

Subdeterminant: for a matrix below

$$
\begin{bmatrix} 1 & 2 & 3 \\ 2 & 5 & 6 \\ 3 & 6 & 7 \end{bmatrix}
$$

the subdeterminant is:

$$
\begin{vmatrix} 1 \end{vmatrix},\quad \begin{vmatrix} 1 & 2 \\ 2 & 5 \end{vmatrix},\quad \begin{vmatrix} 1 & 2 & 3 \\ 2 & 5 & 6 \\ 3 & 6 & 7 \end{vmatrix}
$$



