---
layout:     post
title:      Lecture 27 (Linear Algebra)
subtitle:   
date:       2018-01-14
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 27

**1. Positive Definite Matrix Test**

**2. Positive Definite Matrix and Minimun**

**3. Geometry of Symmetric Metrices**

---

### 1. Positive Definite Matrix Test

For a symmetric matrix $$A=\begin{bmatrix} a & b \\ b & c \end{bmatrix}$$, the 4 conditions below are equivalent ti check whether A is positive definite.

1. eigenvalues $${ \lambda  }_{ 1 }>0,\quad { \lambda  }_{ 2 }>0$$.
2. subdeterminants, $$a>0, ac-{b}^{2}>0$$.
3. pivots $$a>0,\quad \frac { ac-{ b }^{ 2 } }{ a } >0$$.
4. $${x}^{T}Ax>0$$.

### 2. Positive Definite Matrix and Minimun

**Not Positive Definite Case**

*Matrix A*

$$
A=\begin{bmatrix} 2 & 6 \\ 6 & 7 \end{bmatrix}
$$

*$${x}^{T}Ax$$*

$$
f({ x }_{ 1 },{ x }_{ 2 })={ x }^{ T }Ax=\begin{bmatrix} { x }_{ 1 } & { x }_{ 2 } \end{bmatrix}\begin{bmatrix} 2 & 6 \\ 6 & 7 \end{bmatrix}\begin{bmatrix} { x }_{ 1 } \\ { x }_{ 2 } \end{bmatrix}=2{ x }_{ 1 }^{ 2 }+2*6{ x }_{ 1 }{ x }_{ 2 }+14{ x }_{ 2 }^{ 2 }=2{ ({ x }_{ 1 }+3{ x }_{ 2 }) }^{ 2 }-4{ x }_{ 2 }^{ 2 }
$$

*Plot*

![](/img/linear_Algebra/npdm.001.jpg)

$$f({ x }_{ 1 },{ x }_{ 2 })$$ doesn't have a minimum point. The point that first order equals to 0 is actually a saddle point.

**Positive Definite Case**

*Matrix A*

$$
A=\begin{bmatrix} 2 & 6 \\ 6 & 20 \end{bmatrix}
$$

*$${x}^{T}Ax$$*

$$
f({ x }_{ 1 },{ x }_{ 2 })={ x }^{ T }Ax=\begin{bmatrix} { x }_{ 1 } & { x }_{ 2 } \end{bmatrix}\begin{bmatrix} 2 & 6 \\ 6 & 20 \end{bmatrix}\begin{bmatrix} { x }_{ 1 } \\ { x }_{ 2 } \end{bmatrix}=2{ x }_{ 1 }^{ 2 }+2*6{ x }_{ 1 }{ x }_{ 2 }+20{ x }_{ 2 }^{ 2 }=2{ ({ x }_{ 1 }+3{ x }_{ 2 }) }^{ 2 }+2{ x }_{ 2 }^{ 2 }
$$

*Plot*

![](/img/linear_Algebra/pdm.001.jpg)

$$f({ x }_{ 1 },{ x }_{ 2 })$$ does have a minimum point. The point that first order equals to 0 is actually the minimum point.

**Minimum of Caculus and Linear Algebra**

*Calulus*



$$f(x)$$ minimun $$\Rightarrow \quad \frac { { d }^{ 2 }f }{ d{ x }^{ 2 } } >0$$.

*Linear Algebra*

$$f({ x }_{ 1 },{ x }_{ 2 },...,{ x }_{ n })$$ minimum $$\Rightarrow$$ 2nd derivitive matrix is positive definite.

2nd derivitive matrix for f(x,y):

$$
\begin{bmatrix} { f }_{ xx } & { f }_{ xy } \\ { f }_{ yx } & { f }_{ yy } \end{bmatrix}
$$

### 3. Geometry of Symmetric Metrices

*Matrix A*

$$A=\begin{bmatrix} 2 & -1 & 0 \\ -1 & 2 & -1 \\ 0 & -1 & 2 \end{bmatrix}$$

*Dets, Pivots, Eigenvalues*

$$SubDets=2, 3, 4$$.

$$Pivots=2,\frac { 2 }{ 3 } ,\frac { 3 }{ 4 } \quad $$.

$$Eigenvalues=2-\sqrt { 2 } ,2,2+\sqrt { 2 } $$

*Geometry*

Because A positive definite, the graph of $${x}^{T}Ax=constant$$ is a closed ball. 

The axis of the ball is along the direction of eigenvectors, and the axis length is corresponding eigenvalues. That is to say, diagonolized form $$A=Q\Lambda { Q }^{ T }$$ indicates how matrix A distort the space.

![](/img/linear_Algebra/3d.001.jpg)






