---
layout:     post
title:      Lecture 26 (Linear Algebra)
subtitle:   
date:       2018-01-13
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 26

**1. Inner Product of Complex Vectors and Matrices**

**2. Discrete Fourier**

**3. FFT**

---

### 1. Inner Product of Complex Vectors and Matrices

**Vector**

Considering a complex vector $$z={ \begin{bmatrix} { z }_{ 1 } & { z }_{ 2 } & ... & { z }_{ n } \end{bmatrix} }^{ T }$$, the inner prodect of it is $${ \bar { z }  }^{ T }z$$ instead of $${z}^{T}z$$. We use $${z}^{H}z$$ to represent $${ \bar { z }  }^{ T }$$, H stands for Hermition.

**Matrix**

Similar with vector situation, the proper formular of inner product of complex matrice is $${ \bar { A }  }^{ T }A$$. And a complex matrix is orthogonal if it satisfies $${ Q }^{ H }Q={ \bar { Q }  }^{ T }Q=I$$.

### 2. Discrete Fourier

**Fourier Matrix**

$$
{ F }_{ n }=\begin{bmatrix} 1 & 1 & 1 & ... & 1 \\ 1 & { w }^{ 1 } & { w }^{ 2 } & ... & { w }^{ n-1 } \\ 1 & { w }^{ 2 } & { w }^{ 4 } & ... & { w }^{ 2(n-1) } \\ ... & ... & ... & ... & ... \\ 1 & w^{ n-1 } & { w }^{ 2(n-1) } & ... & { w }^{ { (n-1) }^{ 2 } } \end{bmatrix}
$$

**What is w?**

$$
w={ e }^{ { 2\pi i }/{ n } }=\cos { \frac { 2\pi  }{ n }  } +i\sin { \frac { 2\pi  }{ n }  } 
$$

*n = 6*

![](/img/linear_Algebra/6w.001.jpg)

*n = 4*

![](/img/linear_Algebra/4w.001.jpg)

$$
{ w }^{ 4 }=1,\quad w={ e }^{ \cfrac { 2\pi i }{ 4 }  }=i,\quad { w }^{ 2 }=-1,\quad { w }^{ 3 }=-i
$$

$$
{ F }_{ 4 }=\frac { 1 }{ 2 } \begin{bmatrix} 1 & 1 & 1 & 1 \\ 1 & i & { i }^{ 2 } & { i }^{ 3 } \\ 1 & { i }^{ 2 } & { i }^{ 4 } & { i }^{ 6 } \\ 1 & { i }^{ 3 } & { i }^{ 6 } & { i }^{ 9 } \end{bmatrix}＝\frac { 1 }{ 2 } \begin{bmatrix} 1 & 1 & 1 & 1 \\ 1 & i\quad  & -1 & -i \\ 1 & -1 & 1 & -1 \\ 1 & -i & -1 & i \end{bmatrix}
$$

It's easy to verify that $${ F }_{ 4 }^{ H }{ F }_{ 4 }=I$$.

### 3. FFT

The fast fourier tranform applies the relation that $${ ({ W }_{ 64 }) }^{ 2 }={ W }_{ 32 }$$.

$$
\begin{bmatrix} { F }_{ 64 } \end{bmatrix}=\begin{bmatrix} I & D \\ I & -D \end{bmatrix}\begin{bmatrix} { F }_{ 32 } & 0 \\ 0 & { F }_{ 32 } \end{bmatrix}\begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \end{bmatrix},\quad D=\begin{bmatrix} 1 &  &  &  &  \\  & { W }^{ 1 } &  &  &  \\  &  & { W }^{ 2 } &  &  \\  &  &  & ... &  \\  &  &  &  & { W }^{ 31 } \end{bmatrix}
$$

*Computation Save*

$$
{ 64 }^{ 2 }\rightarrow 2{ (32) }^{ 2 }+32\rightarrow 2[2{ (16) }^{ 2 }+16]+32\rightarrow 6*32\\ 
$$

##
{ n }^{ 2 }\rightarrow \frac { 1 }{ 2 } n\log _{ 2 }{ n } 
$$



