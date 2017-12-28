---
layout:     post
title:      Lecture 06 (Linear Algebra)
subtitle:   Vector Space and Subspace, Column Space of A, Nullspace of A
date:       2017-12-28
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 06

1. Vector Space and Subspace
2. Column Space of A
3. Nullspace of A

----
### 1. Vector Space and Subspace
#### Definition

Vector space requires 

*  All v + w and cv are in this space.
*  All cv + dw are in this space.

#### Intersection and Union

If Both P and L are subspaces, then \\(P\bigcup C\\)is not a subspace (unless P or C is included by the other one).

If Both P and L are subspaces, then \\(P\bigcap C\\) is a subspace.

### 2. Columns Space of A
$$
Ax=\begin{bmatrix} 1 & 1 & 2 \\ 2 & 1 & 3 \\ 3 & 1 & 4 \\ 4 & 1 & 5 \end{bmatrix}\begin{bmatrix} x_{ 1 } \\ { x }_{ 2 } \\ { x }_{ 3 } \end{bmatrix}=b
$$
The equation system above has three unknowns and four equations, so the equations may have no solution. Only when b is in C(A), the equation system can be solved.

### 3. Nullspace of A
#### Definition
Nullspace of A is the solution set of Ax = 0. In our case, the nullspace of A is a subspace of \\({R}^{3}\)), while C(A) is a subspace of \\({R}^{4}\)).

#### Solution of Ax = 0
$$
Ax=\begin{bmatrix} 1 & 1 & 2 \\ 2 & 1 & 3 \\ 3 & 1 & 4 \\ 4 & 1 & 5 \end{bmatrix}\begin{bmatrix} x_{ 1 } \\ { x }_{ 2 } \\ { x }_{ 3 } \end{bmatrix}=\begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \end{bmatrix}\quad \quad \quad x=c\begin{bmatrix} 1 \\ 1 \\ -1 \end{bmatrix}
$$

#### Nullspace is a Vector Space
Statement Check:

If Av = 0 and Aw = 0, then A(cv + wd) = 0 for any real scalar c and d.

