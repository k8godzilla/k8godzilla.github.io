---
layout:     post
title:      Lecture 17 (Linear Algebra)
subtitle:   
date:       2018-01-04
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 17

**1. Orthogonal Basis**

**2. Orthogonal Martix**

**3. Gram-Schmidt $A\rightarrowQ$**

---

### 1. Orthogonal Basis

From wiki:

>In mathematics, particularly linear algebra, an orthogonal basis for an inner product space V is a basis for V whose vectors are mutually orthogonal,i.e. for $$\forall$$ basis $${q}_{i}$$ and $${q}_{j}$$ of space V, we have.

$$
{ q }_{ i }^{ T }{ q }_{ j }=\begin{cases} 0\quad if\quad i\neq j \\ 1\quad if\quad i=j \end{cases}
$$

### 2. Orthogonal Martix

**Definition**

From wiki:

>In linear algebra, an orthogonal matrix or real orthogonal matrix is a square matrix with real entries whose columns and rows are orthogonal unit vectors (i.e., orthonormal vectors), i.e.
>
>$${Q}^{T}Q=I$$

**Properties**

**Q doesn't have to be square matrix**, as long as its columns are orthogonal to each other and have unit length, it is orthogonal matrix.

If Q is a square and orthogonal matrix, we have $${Q}^{T}={Q}^{-1}$$.

**Example**

$$
Q=P=\begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix}\quad 
$$

$$
Q=\begin{bmatrix} cos\theta  & -sin\theta  \\ sin\theta  & cos\theta  \end{bmatrix}
$$

$$
Q={ 1 }/{ 2 }\begin{bmatrix} 1 & -1 \\ 1 & 1 \end{bmatrix}
$$

$$
Q={ 1 }/{ 2 }\begin{bmatrix} 1 & 1 & 1 & 1 \\ 1 & -1 & 1 & -1 \\ 1 & 1 & -1 & -1 \\ 1 & -1 & -1 & 1 \end{bmatrix}
$$

**Benefit**

If Q is a orthogonal matrix, its projection matrix can be written as  $$P=Q{ ({ Q }^{ T }Q) }^{ -1 }{ Q }^{ T }=Q{ Q }^{ T }$$.

And the solution form of x also be simplified:

$$
\hat { x } ={ ({ A }^{ T }A) }^{ -1 }{ A }^{ T }b\quad \Rightarrow \quad \hat { x } ={ ({ Q }^{ T }Q) }^{ -1 }{ Q }^{ T }b={ Q }^{ T }b
$$

### 3.Gram-Schmidt $A\rightarrowQ$

We have three independent but not orthogonal vectors a,b,c in $${R}^{N}$$, how to find their corresponding orthogonormal vectors?

**Schmidt-a**

Normalize a.

$${ q }_{ 1 }={ a }/{ \left\| a \right\|  }$$

**Gram-b**

Remove the part that perpendicular to a from b.

$$
b=b-{ { a }^{ T }ba }/{ { a }^{ T }a }
$$

**Schmidt-b**

Normalize b.

$$
{ q }_{ 2 }={ b }/{ \left\| b \right\|  }
$$

**Gram-c**

Remove the part that perpendicular to a and b from c.

$$
c=c-{ { a }^{ T }ca }/{ { a }^{ T }a }-{ { b }^{ T }cb }/{ { b }^{ T }b }
$$

**Schmidt-c**

Normalize c.

$$
{ q }_{ 3 }={ b }/{ \left\| b \right\|  }
$$

**Column Space**

Because the Gram-Schmidt method only involves in column manipulation, the column space of $${q}_{1},{q}_{2},{q}_{3}$$ is same with a,b,c. And the method can be represented in a matrix style A=QR.











