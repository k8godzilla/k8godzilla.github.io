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

**property 1**

det I = 1

**property 2**

Exchange row: reverse sign of det A.

$$
permutation\quad matrix\quad P=\begin{cases} 1\quad if\quad exchange\quad row\quad even\quad times \\ -1\quad if\quad exchange\quad row\quad odd\quad times \end{cases}
$$

**property 3**

a. 

$$
\begin{vmatrix} ta & tb \\ c & d \end{vmatrix}=t\begin{vmatrix} a & b \\ c & d \end{vmatrix}
$$

b.

$$
\begin{vmatrix} a+{ a }^{ ' } & b+{ b }^{ ' } \\ c & d \end{vmatrix}=\begin{vmatrix} a & b \\ c & d \end{vmatrix}+\begin{vmatrix} { a }^{ ' } & { b }^{ ' } \\ c & d \end{vmatrix}
$$

**property 4**

Two equal rows$$\rightarrow$$det A = 0.

$$
\begin{vmatrix} a & b \\ a & b \end{vmatrix}\overset { p2 }{ \Rightarrow  } -\begin{vmatrix} a & b \\ a & b \end{vmatrix}$$

$$
\begin{vmatrix} a & b \\ a & b \end{vmatrix}=-\begin{vmatrix} a & b \\ a & b \end{vmatrix}\Rightarrow \begin{vmatrix} a & b \\ a & b \end{vmatrix}=0
$$

**property 5**

Subtract/Add l*row j for row i, det A doesn't change.

$$
\begin{vmatrix} a+lc & b+ld \\ c & d \end{vmatrix}\overset { p3a }{ = } \begin{vmatrix} a & b \\ c & d \end{vmatrix}+l\begin{vmatrix} c & d \\ c & d \end{vmatrix}\overset { p4 }{ = } \begin{vmatrix} a & b \\ c & d \end{vmatrix}$$

**property 6**

Row of zeros$$\rightarraw$$det A = 0.

$$
\begin{vmatrix} 0 & 0 \\ a & b \end{vmatrix}\overset { p5 }{ = } \begin{vmatrix} a & b \\ a & b \end{vmatrix}\overset { p4 }{ = } 0
$$

**property 7**

The determinant of uppertriangular matrix equals to the product of element in diagnal.

$$
\begin{vmatrix} { d }_{ 1 } & * & * & * & * \\ 0 & { d }_{ 2 } & * & * & * \\ 0 & 0 & { d }_{ 3 } & ... & * \\ ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & { d }_{ n } \end{vmatrix}\overset { p5 }{ = } \begin{vmatrix} { d }_{ 1 } & 0 & 0 & 0 & 0 \\ 0 & { d }_{ 2 } & 0 & 0 & 0 \\ 0 & 0 & { d }_{ 3 } & ... & 0 \\ ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & { d }_{ n } \end{vmatrix}\overset { p3a }{ = } { d }_{ 1 }\begin{vmatrix} 1 & 0 & 0 & 0 & 0 \\ 0 & { d }_{ 2 } & 0 & 0 & 0 \\ 0 & 0 & { d }_{ 3 } & ... & 0 \\ ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & { d }_{ n } \end{vmatrix}=...=(\prod _{ i=1 }^{ n }{ { d }_{ i } } )\begin{vmatrix} 1 & 0 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 1 & ... & 0 \\ ... & ... & ... & ... & ... \\ 0 & 0 & 0 & ... & 1 \end{vmatrix}\overset { p1 }{ = } \prod _{ i=1 }^{ n }{ { d }_{ i } } 
$$

**property 8**

$$det A=0$$ when A is singular. Because singular matrix A can be converted to a form with zeros rows by elimination.

$$det\quad A\neq 0$$ when A is not singular.

**property 9**

$$
det(AB)=(detA)*(detB)
$$

$$
det({ A }^{ -1 })={ 1 }/{ (detA) }
$$

$$
det({ 2A })={ 2 }^{ n }*{ (detA) }
$$

**property 10**

$$det({A}^{T})=det(A)$$, this make sure all row related properties above are also available to column.











