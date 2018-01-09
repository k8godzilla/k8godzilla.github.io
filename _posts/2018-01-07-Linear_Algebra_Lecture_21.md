---
layout:     post
title:      Lecture 21 (Linear Algebra)
subtitle:   
date:       2018-01-07
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 21

**1. Definition of eigenvalues and eigenvectors**

**2. How to solve eigenvalues and eigenvectors**

**3. Abnormal Case** 

---

### 1. Definition of eigenvalues and eigenvectors

**Definition**

For a matrix A, if vector x satisfies that $$Ax=\lambda x$$, then x is A's eignenvector and $$\lambda$$ is x's eigenvalue to A.

If A is singular, then $$\lambda=0$$ is one of the eigenvalues, because $$Ax=0$$.

**Projection matrix case**

What is the eigenvalue and eigenvector of projection matrix $$P=A({A}^{T}A){A}^{T}$$?

Any x in A: $$Px=x, \lambda=1$$.
Any x $$\bot$$ A: $$Px=0, \lambda=0$$.

### 2. How to solve eigenvalues and eigenvectors


**Solve method**

$$
Ax=\lambda x
$$

$$
(A-\lambda I)x=0
$$

$$
\begin{vmatrix} A-\lambda I \end{vmatrix}=0
$$

Find eigenvalues firstly by determinant.

**Case 1**

$$
A=\begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}
$$

$$
\begin{vmatrix} -\lambda  & 1 \\ 1 & -\lambda  \end{vmatrix}=0,\quad { \quad \lambda  }^{ 2 }-1=0,\quad \quad \lambda =\pm 1
$$

**Case 2**

$$
A=\begin{bmatrix} 3 & 1 \\ 1 & 3 \end{bmatrix}
$$

$$
\begin{vmatrix} 3-\lambda  & 1 \\ 1 & 3-\lambda  \end{vmatrix}=0,\quad { \quad \lambda  }^{ 2 }-6\lambda +8=0,\quad \quad \quad { \lambda  }_{ 1 }=2,{ \lambda  }_{ 2 }=4
$$

**Trace and eigenvalues**

Fact: Sum of eigenvalues of A = trace of A = $${a}_{11}+{a}_{22}+...+{a}_{nn}$$

We can verify this fact in case 1 and case 2.

The cause of the fact is the first order item of $$\begin{vmatrix} A-\lambda I \end{vmatrix}=0$$.

### 3.Abnormal Case

**Eigenvector of combination of matrices**

$$
\begin{matrix} Ax=\lambda x \\ B\quad has\quad eigenvalues\quad \alpha  \end{matrix}\Rightarrow (A+B)x=(\lambda +\alpha )x\quad \quad False!!!
$$

Because A and B might have different eigenvectors.

**Complex eigenvalues**

$$
Rotation\quad Matrix:\quad Q=\begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}
$$

$$
det(Q-\lambda I)=\begin{vmatrix} -\lambda  & 1 \\ -1 & -\lambda  \end{vmatrix}=0
$$

$$
{ \lambda  }_{ 1 }=i,\quad { \lambda  }_{ 2 }=-i
$$

The more close to symmetric is the matrix A, the more likely it has real value eigenvalues, and vice versa.

**Lack of eigenvectors**

$$
A=\begin{bmatrix} 3 & 1 \\ 0 & 3 \end{bmatrix}
$$

$$
det(A-\lambda I)=\begin{vmatrix} 3-\lambda  & 1 \\ 0 & 3-\lambda  \end{vmatrix}=(3-\lambda )(3-\lambda )=0
$$

$$
{ \lambda  }_{ 1 }={ \lambda  }_{ 2 }=3
$$

substitute $$\lambda=3$$ into formula:

$$
(A-\lambda I)x=\begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix}x=0
$$

$$
{ x }_{ 1 }=\begin{bmatrix} 1 \\ 0 \end{bmatrix},\quad { x }_{ 2 }=Null
$$

There is only one special solution of eigenvector while there are two equal eigenvalues.








