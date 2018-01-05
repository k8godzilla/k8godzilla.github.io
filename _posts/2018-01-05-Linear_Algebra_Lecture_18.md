---
layout:     post
title:      Lecture 18 (Linear Algebra)
subtitle:   
date:       2018-01-05
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 18

**Determinants det A - 10 properties**

---

**1**

det I = 1

**2**

Exchange row: reverse sign of det A.

$$
permutation\quad matrix\quad P=\begin{cases} 1\quad if\quad exchange\quad row\quad even\quad times \\ -1\quad if\quad exchange\quad row\quad odd\quad times \end{cases}
$$

**3**

a. 

$$
\begin{vmatrix} ta & tb \\ c & d \end{vmatrix}=t\begin{vmatrix} a & b \\ c & d \end{vmatrix}
$$

b.

$$
\begin{vmatrix} a+{ a }^{ ' } & b+{ b }^{ ' } \\ c & d \end{vmatrix}=\begin{vmatrix} a & b \\ c & d \end{vmatrix}+\begin{vmatrix} { a }^{ ' } & { b }^{ ' } \\ c & d \end{vmatrix}
$$

**4**

Two equal rows$$\rightarrow$$det A = 0.

$$
\begin{vmatrix} a & b \\ a & b \end{vmatrix}\overset { exchange\quad row }{ \Rightarrow  } -\begin{vmatrix} a & b \\ a & b \end{vmatrix}
$$

$$
\begin{vmatrix} a & b \\ a & b \end{vmatrix}=-\begin{vmatrix} a & b \\ a & b \end{vmatrix}\Rightarrow \begin{vmatrix} a & b \\ a & b \end{vmatrix}=0
$$

**5**

Subtract/Add l*row j for row i, det A doesn't change.

$$
\begin{vmatrix} a+lc & b+ld \\ c & d \end{vmatrix}=\begin{vmatrix} a & b \\ c & d \end{vmatrix}+l\begin{vmatrix} c & d \\ c & d \end{vmatrix}=\begin{vmatrix} a & b \\ c & d \end{vmatrix}
$$

**6**

Row of zeros$$\rightarraw$$det A = 0.

$$
\begin{vmatrix} 0 & 0 \\ a & b \end{vmatrix}\overset { p5 }{ = } \begin{vmatrix} a & b \\ a & b \end{vmatrix}\overset { p4 }{ = } 0
$$












