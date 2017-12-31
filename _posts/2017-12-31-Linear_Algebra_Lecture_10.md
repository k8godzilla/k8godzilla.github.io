---
layout:     post
title:      Lecture 10 (Linear Algebra)
subtitle:   
date:       2017-12-31
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 10

**Four Subspaces**

---

**Example**

$$
A=\begin{bmatrix} 1 & 2 & 3 & 1 \\ 1 & 1 & 2 & 1 \\ 1 & 2 & 3 & 1 \end{bmatrix}\rightarrow \begin{bmatrix} 1 & 0 & 1 & 1 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}=R
$$

**Column space of A, C(A)**

The dimension of C(A) = rank of A = 2.

The basis of C(A) is two pivot columns:$$\begin{bmatrix} 1 \\ 1 \\ 1 \end{bmatrix},\begin{bmatrix} 2 \\ 1 \\ 2 \end{bmatrix}$$.

**Nullspace of A, N(A)**

The dimension of N(A) = n-rank of A = 4-2 = 2.

The basis of N(A) is special solution of Ax=0: $$\begin{bmatrix} -1 \\ -1 \\ 1 \\ 0 \end{bmatrix},\begin{bmatrix} -1 \\ 0 \\ 0 \\ 1 \end{bmatrix}$$.

**Row space of A, C($${A}^{T}$$)**

The dimension of C($${A}^{T}$$) = rank of A = 2.

The basis of C($${A}^{T}$$) is the first r=2 rows of rref: $$\begin{bmatrix} 1 \\ 0 \\ 1 \\ 1 \end{bmatrix},\begin{bmatrix} 0 \\ 1 \\ 1 \\ 0 \end{bmatrix}$$

**Nullspace of $${A}^{T}$$, N($${A}^{T}$$)**

The dimension of N($${A}^{T}$$) = m-rank of A = 1.

Notice that $${ A }^{ T }y=0\quad \Rightarrow \quad { y }^{ T }A=0$$. To find the basis of N($${A}^{T}$$), we just need to find the row combinations of A that gives zero.

To find the proper row combination, we can write the row exchange into matrix form:

$$
E\begin{bmatrix} { A }_{ m*n } & { I }_{ m*m } \end{bmatrix}\rightarrow \begin{bmatrix} { R }_{ m*n } & { E }_{ m*m } \end{bmatrix}\\ \\ EA\quad =\quad R
$$

$$
\quad E\quad \quad \quad \quad \quad \quad \quad A\quad \quad \quad \quad \quad \quad \quad \quad R\\ \begin{bmatrix} -1 & 2 & 0 \\ 1 & -1 & 0 \\ -1 & 0 & 1 \end{bmatrix}\begin{bmatrix} 1 & 2 & 3 & 1 \\ 1 & 1 & 2 & 1 \\ 1 & 2 & 3 & 1 \end{bmatrix}\rightarrow \begin{bmatrix} 1 & 0 & 1 & 1 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}
$$

The basis of N($${A}^{T}$$) is $$\begin{bmatrix} -1 \\ 0 \\ 1 \end{bmatrix}$$.





