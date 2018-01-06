---
layout:     post
title:      Lecture 20 (Linear Algebra)
subtitle:   
date:       2018-01-06
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 20

**1. Formula for $${A}^{-1}$$**

**2. Cramer's rule for $$x={A}^{-1}b$$**

**3.$$\begin{vmatrix} Det\quad A \end{vmatrix}$$= volume of box** 

---

### 1. Formula for $${A}^{-1}$$

$$
{ A }^{ -1 }=({ 1 }/{ det\quad A }){ C }^{ T }
$$

Check

$$
A{ C }^{ T }=(det\quad A)I
$$

$$
\begin{bmatrix} { a }_{ 11 } & { a }_{ 12 } & ... & { a }_{ 1n } \\ { a }_{ 21 } & { a }_{ 22 } & ... & { a }_{ 2n } \\ ... & ... & ... & ... \\ { a }_{ n1 } & { a }_{ n2 } & ... & { a }_{ nn } \end{bmatrix}\begin{bmatrix} { c }_{ 11 } & { c }_{ 21 } & ... & { c }_{ n1 } \\ { c }_{ 12 } & { c }_{ 22 } & ... & { c }_{ n2 } \\ ... & ... & ... & ... \\ { c }_{ 1n } & { c }_{ 2n } & ... & { c }_{ nn } \end{bmatrix}=\begin{bmatrix} det\quad A & 0 & ... & 0 \\ 0 & det\quad A & ... & 0 \\ ... & ... & ... & ... \\ 0 & 0 & ... & det\quad A \end{bmatrix}
$$

Checked.

### 2. Cramer's rule for $$x={A}^{-1}b$$

$$
Ax=b
$$

$$
x={ A }^{ -1 }b=({ 1 }/{ det\quad A }){ C }^{ T }b=({ 1 }/{ det\quad A })\begin{bmatrix} { c }_{ 11 } & { c }_{ 21 } & ... & { c }_{ n1 } \\ { c }_{ 12 } & { c }_{ 22 } & ... & { c }_{ n2 } \\ ... & ... & ... & ... \\ { c }_{ 1n } & { c }_{ 2n } & ... & { c }_{ nn } \end{bmatrix}\begin{bmatrix} { b }_{ 1 } \\ { b }_{ 2 } \\ ... \\ { b }_{ n } \end{bmatrix}
$$

$$
{ x }_{ 1 }=({ 1 }/{ det\quad A })({ c }_{ 11 }{ b }_{ 1 }+{ c }_{ 21 }{ b }_{ 2 }+...+{ c }_{ n1 }{ b }_{ n })={ (det\quad { B }_{ 1 }) }/{ (det\quad A) }
$$

$$
{ B }_{ 1 }=\begin{bmatrix} { b }_{ 1 } & { a }_{ 12 } & ... & { a }_{ 1n } \\ { b }_{ 2 } & { a }_{ 22 } & ... & { a }_{ 2n } \\ ... & ... & ... & ... \\ { b }_{ n } & { a }_{ n2 } & ... & { a }_{ nn } \end{bmatrix}
$$

$${B}_{j}$$=A with column j replaced by b.
