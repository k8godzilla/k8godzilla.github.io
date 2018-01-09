---
layout:     post
title:      Lecture 22 (Linear Algebra)
subtitle:   
date:       2018-01-09
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 22

**1. Diagonalizing a matrix $${ S }^{ -1 }AS=\Lambda$$**

**2. Powers of A**

**3. $${u}_{k+1}=A{u}_{k}$$** 

---

### 1. Diagonalizing a matrix $${ S }^{ -1 }AS=\Lambda$$

**Diagonalizing matrix**

Suppose n by n matrix A has n independent eigenvectors. Put them in columns of S.

$$
AS=A\begin{bmatrix} { x }_{ 1 } & { x }_{ 2 } & ... & { x }_{ n } \end{bmatrix}=\begin{bmatrix} \lambda { x }_{ 1 } & \lambda { x }_{ 2 } & ... & \lambda { x }_{ n } \end{bmatrix}=\begin{bmatrix} { x }_{ 1 } & { x }_{ 2 } & ... & { x }_{ n } \end{bmatrix}\begin{bmatrix} { \lambda  }_{ 1 } & 0 & ... & 0 \\ 0 & { \lambda  }_{ 2 } & ... & 0 \\ ... & ... & ... & ... \\ 0 & 0 & ... & { \lambda  }_{ n } \end{bmatrix}=S\Lambda 
$$

$$
AS=S\Lambda 
$$

$$
{ S }^{ -1 }AS=\Lambda 
$$

**Guarantee of independence eigenvectors**

n by n matrix A is sure to have n independent eigenvectors and can be diagnoalizable if it has n distinct eigenvalues.

If A has repeated eigenvalues, it might or might not have n independent eigenvectors.

### 2.Powers of A

$$
A=S\Lambda { S }^{ -1 }
$$

$$
{ A }^{ 2 }=S{ \Lambda  }^{ 2 }{ S }^{ -1 }
$$

$$
{ A }^{ k }=S{ \Lambda  }^{ k }{ S }^{ -1 }
$$

**Theorem**: $${ A }^{ k }\rightarrow 0\quad as\quad k\rightarrow \infty \quad if\quad all\begin{vmatrix} { \lambda  }_{ i } \end{vmatrix}<1$$

### 3. $${u}_{k+1}=A{u}_{k}$$

**Question**

A is a n by n diagonalizable matrix. Start with given vector $${u}_{0}$$,and then $${ u }_{ 1 }=A{ u }_{ 0 }$$, $${ u }_{ 2 }={ A }^{ 2 }{ u }_{ 0 }$$,...how to solve $${ u }_{ k }={ A }^{ k }{ u }_{ 0 }$$?

**Factorize $${u}_{0}$$**

Because A has n independent eigenvectors vectors, its eigenvectors is a basis of $${R}^{n}$$. $${u}_{0}$$ can be written as:

$$
{ u }_{ 0 }={ c }_{ 1 }{ x }_{ 1 }+{ c }_{ 2 }{ x }_{ 2 }+...+{ c }_{ n }{ x }_{ n }=Sc
$$

$$
{ u }_{ k }={ A }^{ k }{ u }_{ 0 }={ c }_{ 1 }{ \Lambda  }^{ k }{ x }_{ 1 }+{ c }_{ 2 }{ \Lambda  }^{ k }{ x }_{ 2 }+...+{ c }_{ n }{ { \Lambda  }^{ k }x }_{ n }={ \Lambda  }^{ k }Sc
$$

**Example**

Fibonacci Series: 0,1,1,2,3,5,8,... What is $${F}_{100}$$?

Trick:

$$
{ F }_{ k+2 }={ F }_{ k+1 }+{ F }_{ k }
$$

$$
{F}_{k+1}={F}_{k+1}
$$

$$
{ u }_{ k+1 }=\begin{bmatrix} { F }_{ k+1 } \\ { F }_{ k } \end{bmatrix}
$$

$$
{ u }_{ k+1 }=\begin{bmatrix} 1 & 1 \\ 1 & 0 \end{bmatrix}{ u }_{ k }
$$

$$
A=\begin{bmatrix} 1 & 1 \\ 1 & 0 \end{bmatrix}
$$

$$
\begin{vmatrix} A-\lambda I \end{vmatrix}=\begin{vmatrix} 1-\lambda  & 1 \\ 1 & -\lambda  \end{vmatrix}={ \lambda  }^{ 2 }-\lambda -1=0
$$

$$
{ \lambda  }_{ 1 }={ (1+\sqrt { 5 } ) }/{ 2 }\approx 1.618\\ { \lambda  }_{ 2 }={ (1-\sqrt { 5 } ) }/{ 2 }\approx -0.618
$$

$$
\because \quad { ({ \lambda  }_{ 2 }) }^{ 100 }\approx 0\\ \therefore { F }_{ 100 }\approx { c }_{ 1 }{ u }_{ 0 }{ ({ \lambda  }_{ 1 }) }^{ 100 }
$$

$$
\because \quad { ({ \lambda  }_{ 2 }) }^{ 100 }\approx 0\\ \therefore { F }_{ 100 }\approx { c }_{ 1 }{ u }_{ 0 }{ ({ \lambda  }_{ 1 }) }^{ 100 }
$$

$$
{ x }_{ 1 }=\begin{bmatrix} { \lambda  }_{ 1 } \\ 1 \end{bmatrix},\quad { x }_{ 2 }=\begin{bmatrix} { \lambda  }_{ 2 } \\ 1 \end{bmatrix}\\ { c }_{ 1 }\quad and\quad { c }_{ 2 }\quad can\quad be\quad computed\quad from\quad { x }_{ 1 }\quad and\quad { x }_{ 2 }.
$$
