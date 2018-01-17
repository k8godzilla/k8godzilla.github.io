---
layout:     post
title:      Lecture 30 (Linear Algebra)
subtitle:   
date:       2018-01-17
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 30

**1. Linear Transform Examples**

**2. Build Matrix A for Linear Transform**

---

### 1. Linear Transform Examples

**Properties**

1. $$T(v+w)=T(v)+T(w)$$.
2. $$T(cv)=cT(v)$$.

Combine property 1 and 2:

$$T(cv+dw)=cT(v)+dT(w)$$.

**Example 1: Projection is a linear transform**

![](/img/linear_Algebra/projection.001.jpg)

**Example 2: Add a vector to the whole plane is not a linear transform**

![](/img/linear_Algebra/add_vector.001.jpg)

**Example 3: $$T(v)=\begin{Vmatrix} v \end{Vmatrix}$$ is not a linear transform**

Because $$T(cv)\neq cT(v)$$ when c is negative.

**Example 4: Rotate by 45 degrees is a linear transform**

![](/img/linear_Algebra/rotate.001.jpg)

**Example 5: $$T(v) = Av$$ is a linear transform**

Because $$A(v+w)=Av+Aw$$ and $$A(cv)=cAv$$.

### 2. Build Maxix A for Linear Transform

**Infomation Needed to Build T(v)**

Because T(v) is linear, we only need to know linear transform for all basis $$T({v}_{1}), T({v}_{2}),...,T({v}_{n})$$. Then for every $$v={ c }_{ 1 }{ v }_{ 1 }+{ c }_{ 2 }{ v }_{ 2 }+...+{ c }_{ n }{ v }_{ n }$$, its linear transorm is $$T(v)={ c }_{ 1 }T({ v }_{ 1 })+{ c }_{ 2 }T({ v }_{ 2 })+...+{ c }_{ n }T({ v }_{ n })$$.

**Projection Case**

For 2-D plane, if we take the direction of the line we want to project on as the first basis $${v}_{1}$$ and its orthogonal vector as the second basis $${v}_{2}$$, the projection problem would become:

$$
v={ c }_{ 1 }{ v }_{ 1 }+{ c }_{ 2 }{ v }_{ 2 }\Rightarrow T(v)={ c }_{ 1 }{ v }_{ 1 }
$$

Then we can infer that matrix A is $$\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$$.

$$
\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}\begin{bmatrix} { c }_{ 1 } \\ { c }_{ 2 } \end{bmatrix}=\begin{bmatrix} { c }_{ 1 } \\ 0 \end{bmatrix}
$$

Matrix A is diagonal because the basis $${v}_{1}$$ and $${v}_{2}$$ is the eigenvectors.

**Project to $${45}^{。}$$ line**

Use the standard basis $${ v }_{ 1 }=\begin{bmatrix} 1 \\ 0 \end{bmatrix}$$ and { v }_{ 2 }=\begin{bmatrix} 0 \\ 1 \end{bmatrix}, the projection matrix P is $$P=\frac { a{ a }^{ T } }{ { a }^{ T }a } =\begin{bmatrix} \frac { 1 }{ 2 }  & \frac { 1 }{ 2 }  \\ \frac { 1 }{ 2 }  & \frac { 1 }{ 2 }  \end{bmatrix}$$.

P is not diagonal becuase we didn't choose eigenvector basis.

**First Derivitive and Linear Transform**

First Derivitive is also a linear transform.

Input: $${ c }_{ 1 }+{ c }_{ 2 }x+{ c }_{ 3 }{ x }^{ 2 }$$ Basis: $$1, x, {x}^{2}$$

Output: $${ c }_{ 2 }+2{ c }_{ 3 }{ x }$$ Basis: $$1, x$$

The matrix form of linear transformation is:

$$
\begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 2 \end{bmatrix}\begin{bmatrix} { c }_{ 1 } \\ { c }_{ 2 } \\ { c }_{ 3 } \end{bmatrix}=\begin{bmatrix} { c }_{ 2 } \\ 2{ c }_{ 3 } \end{bmatrix}
$$.





