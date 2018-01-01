---
layout:     post
title:      Lecture 11 (Linear Algebra)
subtitle:   
date:       2017-12-31
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 11

**1. Basis of new vector spaces**

**2. Analogy of differential equation**

**3. Rank one matrix**

**4. Simple case about four spaces**

---

### 1. Basis of new vector spaces

Like vector, matrix also has vector space and subspace. We take 3 by 3 matrix as example. Notice that all basis written below is not unique.

**M = all 3 by 3 matrix**

dimsion: 9

basis: 

$$
\begin{bmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix},......,\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix}
$$

**Symmetrical matrix**

dimension: 6

basis:

$$
\begin{bmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix},\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 1 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 & 1 \\ 0 & 0 & 0 \\ 1 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}
$$

**Upper triangular matrix**

dimension: 6

basis:

$$
\begin{bmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix},\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 1 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 1 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}
$$

**S$$\bigcup$$U = diagnal matrix**

dimension: 3

basis:

$$
\begin{bmatrix} 1 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{bmatrix},\begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 1 \end{bmatrix}
$$

**S+U**

S$$\bigcap$$U is not a subspace. S+U is a subspace which is exatly M.
Then we have the dimension relationship: dim(S) + dim(U) = dim(S+U) + dim(S$$\bigcup$$U)

### 2. Analogy of differential equation

equation: $${ { d }^{ 2 }y }/{ d{ x }^{ 2 } }+y=0$$

dimension of solution space: 2. Because this second-order differential equation.

solution basis: cos(x), sin(x).

complete solution: y = $${c}_{1}$$cos(x) + $${c}_{2}$$sin(x)


### 3.Rank one matrix

All rank one matrix can be written as $$u{v}^{T}$$, where u and v are vectors.The example is below: 

$$
A=\begin{bmatrix} 1 & 4 & 5 \\ 2 & 8 & 10 \end{bmatrix}=\begin{bmatrix} 1 \\ 2 \end{bmatrix}\begin{bmatrix} 1 & 4 & 5 \end{bmatrix}
$$

### 4. Simple case about four spaces

S = all vectors in $${R}^{4}$$ with $${v}_{1}+{v}_{2}+{v}_{3}+{v}_{4}=0$$.

S is the solution space of Ax = 0, where A = [1,1,1,1].So S is also the nullspace of A.

**N(A)**

Dimension of N(A) is 3.

Basis of N(A) is:

$$
\begin{bmatrix} -1 \\ 1 \\ 0 \\ 0 \end{bmatrix},\begin{bmatrix} -1 \\ 0 \\ 1 \\ 0 \end{bmatrix},\begin{bmatrix} -1 \\ 0 \\ 0 \\ 1 \end{bmatrix}
$$

**C($${A}^{T}$$)**

Dimension of C($${A}^{T}$$) is 1.

Basis of C($${A}^{T}$$) is:

$$
\begin{bmatrix} 1 \\ 1 \\ 1 \\ 1 \end{bmatrix}
$$

Basis of N(A) and C($${A}^{T}$$) lie in $${R}^{4}$$. And sum of dimension of them equals to 4, whis is column number of A.

**N($${A}^{T}$$)**

$${A}^{T}$$ has no free variable, so the dimension of N($${A}^{T}$$) is 0, and basis is {zero vector}.

**C(A)**

C(A) is the $${R}^{1}$$ space. The dimension is 1, and basis is 1.

Sum of dimension of C(A) and N($${A}^{T}$$) equals to 1, which is the row number of A.




 




