---
layout:     post
title:      Lecture 23 (Linear Algebra)
subtitle:   
date:       2018-01-10
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 23

**1. Differential equations: particular case**

**2. Differential equations: general form**

**3. Exponential of a matrix $${e}^{At}$$**

**4. High order differential equations**

---

### 1. Differential equations: particular case

**Question**

*Diffrential Equation*

$$
\frac { d{ u }_{ 1 } }{ dt } =-{ u }_{ 1 }+2{ u }_{ 2 }\\ \frac { d{ u }_{ 2 } }{ dt } ={ u }_{ 1 }-2{ u }_{ 2 }
$$

*Initial State*

$$
u(0)=\begin{bmatrix} 1 \\ 0 \end{bmatrix}
$$

**Solve Equation**

*Coef Matrix*

$$
A=\begin{bmatrix} -1 & 2 \\ 1 & -2 \end{bmatrix}
$$

*Solve eigenvalues and eigenvectors*

$$
{ \lambda  }_{ 1 }=0,\quad { x }_{ 1 }=\begin{bmatrix} 2 \\ 1 \end{bmatrix}\\ { \lambda  }_{ 2 }=-3,\quad { x }_{ 2 }=\begin{bmatrix} 1 \\ -1 \end{bmatrix}
$$

*Solution*

$$
{ u }_{ t }={ c }_{ 1 }{ e }^{ { \lambda  }_{ 1 }t }{ x }_{ 1 }+{ c }_{ 2 }{ e }^{ { \lambda  }_{ 2 }t }{ x }_{ 2 }
$$

set t=0, and $${c}_{1}$$ and $${c}_{2}$$ can be computed from $$u(0)$$.

**Stability Discussion**

*General Rule*

1. Stable: $${ u }_{ t }\rightarrow 0\quad \Rightarrow \quad all\quad { e }^{ \lambda t }\rightarrow 0\quad \Rightarrow \quad all\quad Re(\lambda )<0$$.
2. Steady state: $${\lambda}_{1}=0$$ and other $$Re(\lambda)<0$$.
3. Blow up: if any $$Re(\lambda)>0$$.

*2 by 2 Case*

To ensure differential equation with 2 by 2 matrix A as coef matrix, two conditions below need to be staified.
1. trace(A) < 0
2. det(A) > 0


### 2. Differential equations: general form

*Original Question*

$$
\frac { du }{ dt } =A
$$

*Eigenvector Form*

Set $$u=Sv$$, where S is matrix consists of eigenvectors.

$$
\frac { dv }{ dt } ={ S }^{ -1 }ASv=\Lambda v
$$

*Solution*

$$
v(t)={ e }^{ \Lambda t }v(0)\\ \\ u(t)=S{ e }^{ \Lambda t }{ S }^{ -1 }u(0)={ e }^{ At }u(0)
$$

### 3. Exponential of a matrix $${e}^{At}$$

*$${e}^{At}$$*

How to interpret the exponental of a matrix?

Using **taylor series**:

$$
{ e }^{ At }=I+At+\frac { { (At) }^{ 2 } }{ 2! } +\frac { { (At) }^{ 3 } }{ 3! } +...+\frac { { (At) }^{ n } }{ n! } +...=\sum _{ 0 }^{ \infty  }{ \frac { { x }^{ n } }{ n! }  } 
$$

*Prove $${e}^{At}=S{e}^{\Lambda t}{S}^{-1}$$*

$$
{ e }^{ At }=S{ S }^{ -1 }+S\Lambda { S }^{ -1 }t+S\frac { { \Lambda  }^{ 2 } }{ 2! } { S }^{ -1 }{ t }^{ 2 }+S\frac { { \Lambda  }^{ 3 } }{ 3! } { S }^{ -1 }{ t }^{ 3 }+...+S\frac { { \Lambda  }^{ n } }{ n! } { S }^{ -1 }{ t }^{ n }+...=S{ e }^{ \Lambda t }{ S }^{ -1 }
$$

### 4. High order differential equations

*Equation*

$$
{ y }^{ '' }+b{ y }^{ ' }+k=0
$$

*Conversion*

$$
u=\begin{bmatrix} { y }^{ ' } \\ y \end{bmatrix}
$$

$$
{ u }^{ ' }=\begin{bmatrix} { y }^{ '' } \\ { y }^{ ' } \end{bmatrix}=\begin{bmatrix} -b & -k \\ 1 & 0 \end{bmatrix}\begin{bmatrix} { y }^{ ' } \\ y \end{bmatrix}=\begin{bmatrix} -b & -k \\ 1 & 0 \end{bmatrix}u
$$

*Higher Order*

Higher order differential equations can also use same method to convert equation into form below:

$$
\begin{bmatrix} * & * & * & * & * \\ 1 & 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 & 0 \end{bmatrix}
$$








