---
layout:     post
title:      Lecture 16 (Linear Algebra)
subtitle:   
date:       2018-01-02
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 16

**1. Review of projection**

**2. What's the question?**

**3. Solve the question**

**4. Invertibility of $${A}^{T}A$$**

---

### 1. Review of projection


Projetion matrix: $$P=A{ ({ A }^{ T }A) }^{ -1 }{ A }^{ T }$$

If b is in column space of A, then Pb=b.
If b $$\bot $$ column space of A, then Pb=0.

### 2. What's the question?

**Find the line to fit the three points best.**

![](/img/linear_Algebra/graph_1.jpg)

![](/img/linear_Algebra/graph_2.jpg)

The eqation system is: 

$$
C+D=1\\ C+2D=2\\ C+3D=2
$$

Write it into a matrix form:

$$
\begin{bmatrix} 1 & 1 \\ 1 & 2 \\ 1 & 3 \end{bmatrix}\begin{bmatrix} C \\ D \end{bmatrix}=\begin{bmatrix} 1 \\ 2 \\ 2 \end{bmatrix}
$$

### 3. Solve the question

Solve the equation by projection:

$$
\begin{bmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \end{bmatrix}\begin{bmatrix} 1 & 1 \\ 1 & 2 \\ 1 & 3 \end{bmatrix}\begin{bmatrix} C \\ D \end{bmatrix}=\begin{bmatrix} 1 & 1 & 1 \\ 1 & 2 & 3 \end{bmatrix}\begin{bmatrix} 1 \\ 2 \\ 2 \end{bmatrix}
$$

$$
\begin{bmatrix} 3 & 6 \\ 6 & 14 \end{bmatrix}\begin{bmatrix} C \\ D \end{bmatrix}=\begin{bmatrix} 5 \\ 11 \end{bmatrix}
$$

$$
C={ 2 }/{ 3 },D={ 1 }/{ 2 }
$$

Substitute C,D into equations, we get the e vector:

$$
e=\begin{bmatrix} -{ 1 }/{ 6 } \\ { 2 }/{ 6 } \\ -{ 1 }/{ 6 } \end{bmatrix}
$$

We can check that the error vector is perpendicular to column space.

### 4. Invertibility of $${A}^{T}A$$

The prerequisite that $$({A}^{T}A)\hat{x}={A}^{T}b$$ can be solved is that $${A}^{T}A$$ is invertible.

If A has indepenence columns, then $${A}^{T}A$$ is invertible.

**Proof**

Suppose $${A}^{T}Ax=0$$, we need to prove that x must be 0.

$$
{ x }^{ T }{ A }^{ T }Ax=0\Rightarrow { (Ax) }^{ T }(Ax)=0\overset { square }{ \Rightarrow  } Ax=0\overset { indep\quad cols }{ \Rightarrow  } x=0
$$

