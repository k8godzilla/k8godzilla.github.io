---
layout:     post
title:      Lecture 28 (Linear Algebra)
subtitle:   
date:       2018-01-15
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 28

**1. $${A}^{T}A$$ is Positive Definite**

**2. Simliar Matrix**

---

### 1. $${A}^{T}A$$ is Positive Definite

Suppose A is a m by n matrix whick rank is n, then $${A}^{T}A$$ must be a positive definite matrix.

$$
{ x }^{ T }{ A }^{ T }Ax={ (xA) }^{ T }(xA)>0
$$

### 2. Simliar Matrix

**Definition**

A and B are similar matrix means: there is some matrix M s.t. $$B={M}^{-1}AM$$.

**Example**

A is similar to $$/Lambda$$ because $${S}^{-1}AS=/Lambda$$.

Let $$M=\begin{bmatrix} 1 & 4 \\ 0 & 1 \end{bmatrix}$$, then similar matrix B can be computed by $$B={M}^{-1}AM$$:

$$
B=\begin{bmatrix} 1 & -4 \\ 0 & 1 \end{bmatrix}\begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}\begin{bmatrix} 1 & 4 \\ 0 & 1 \end{bmatrix}=\begin{bmatrix} -2 & -15 \\ 1 & 6 \end{bmatrix}
$$

**Similar Matrices, Same Eigenvalues**

$$
{ M }^{ -1 }AM=B
$$

$$
Ax=\lambda x\Rightarrow AM{ M }^{ -1 }x=M{ M }^{ -1 }\lambda x\Rightarrow { M }^{ -1 }AM{ M }^{ -1 }x={ M }^{ -1 }\lambda x\Rightarrow B{ M }^{ -1 }x=\lambda { M }^{ -1 }x
$$

**Bad Case**

*$${\lambda}_{1}={\lambda}_{2}=4$$*

Small family with only one member: $${ M }^{ -1 }\begin{bmatrix} 4 & 0 \\ 0 & 4 \end{bmatrix}M=\begin{bmatrix} 4 & 0 \\ 0 & 4 \end{bmatrix}$$.

Big family: other 2 by 2 matrices with trace equals to 8 and det equals to 16.

$$
\begin{bmatrix} 4 & 1 \\ 0 & 4 \end{bmatrix},\quad \begin{bmatrix} 5 & 1 \\ -1 & 3 \end{bmatrix},\quad \begin{bmatrix} 4 & 0 \\ 17 & 4 \end{bmatrix},\quad ...
$$

**Jordan Form**

*Jordan Block*

$$
{ J }_{ i }=\begin{bmatrix} { \lambda  }_{ i } & 1 & 0 & 0 \\ 0 & { \lambda  }_{ i } & 1 & 0 \\ 0 & 0 & ... & 1 \\ 0 & 0 & 0 & { \lambda  }_{ i } \end{bmatrix}
$$

One Jordan Block corresponds to only one eigenvetor.

*Jordan Matrix and Similarity*

Every square matrix A is similiar to matrix J.

$$
J=\begin{bmatrix} { J }_{ 1 } & 0 & ... & 0 \\ 0 & { J }_{ 2 } & ... & 0 \\ ... & ... & ... & ... \\ 0 & 0 & ... & { J }_{ d } \end{bmatrix}
$$

Number of eigenvectors = Number of Jordan Blocks. Good Jordan matrix is $$\Lambda$$.

*Example*

$$
A=\begin{bmatrix} 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{bmatrix}
$$

$$
B=\begin{bmatrix} 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 0 \end{bmatrix}
$$

The Jordan matrices of A ad B are different. A is not similar with B, although they have same eigenvalues.  


