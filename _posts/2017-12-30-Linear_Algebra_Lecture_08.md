---
layout:     post
title:      Lecture 08 (Linear Algebra)
subtitle:   
date:       2017-12-30
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 08

**1. Solvability of Ax=b**

**2. Full Solution of Ax=b**

**3. Row, Column, Rank and Solution**

---
### 1.Solvability of Ax=b
There are two statements about solvability condition on b

* Ax=b solvable when b is in C(A)
* If a combinition of rows of A gives zero row, then same combination of entries of b must give zero.

**Example**
The equation system is below

$$
{ x }_{ 1 }+2{ x }_{ 2 }+2{ x }_{ 3 }+2{ x }_{ 4 }\quad ={ b }_{ 1 }\\ 2{ x }_{ 1 }+4{ x }_{ 2 }+6{ x }_{ 3 }+8{ x }_{ 4 }\quad ={ b }_{ 2 }\\ 3{ x }_{ 1 }+6{ x }_{ 2 }+8{ x }_{ 3 }+10{ x }_{ 4 }={ b }_{ 3 }
$$

The augmented matrix is below


$$
\begin{bmatrix} 1 & 2 & 2 & 2 & { b }_{ 1 } \\ 2 & 4 & 6 & 8 & { b }_{ 2 } \\ 3 & 6 & 8 & 10 & { b }_{ 3 } \end{bmatrix}\Rightarrow \begin{bmatrix} 1 & 2 & 2 & 2 & { b }_{ 1 } \\ 0 & 0 & 2 & 4 & { b }_{ 2 }-2{ b }_{ 1 } \\ 0 & 0 & 2 & 4 & { b }_{ 3 }-3{ b }_{ 1 } \end{bmatrix}\Rightarrow \begin{bmatrix} 1 & 2 & 2 & 2 & { b }_{ 1 } \\ 0 & 0 & 2 & 4 & { b }_{ 2 }-2{ b }_{ 1 } \\ 0 & 0 & 0 & 0 & { b }_{ 3 }-{ b }_{ 1 }-{ b }_{ 2 } \end{bmatrix}
$$

In the example above the condition on b to ensure Ax=b solvable is :$${ b }_{ 3 }-{ b }_{ 1 }-{ b }_{ 2 }$$.



### 2. Complete Solution of Ax=b
Let $${ b }_{ 1 }=1,{ b }_{ 2 }=5\quad and\quad { b }_{ 3 }=6$$. 

**Transform into rref form**
$$
\begin{bmatrix} 1 & 2 & 2 & 2 & { b }_{ 1 } \\ 0 & 0 & 2 & 4 & { b }_{ 2 }-2{ b }_{ 1 } \\ 0 & 0 & 0 & 0 & { b }_{ 3 }-{ b }_{ 1 }-{ b }_{ 2 } \end{bmatrix}=\begin{bmatrix} \boxed { 1 }  & 2 & 2 & 2 & 1 \\ 0 & 0 & \boxed { 2 }  & 4 & 3 \\ 0 & 0 & 0 & 0 & 0 \end{bmatrix}\Rightarrow \begin{bmatrix} \boxed { 1 }  & 2 & 0 & -2 & -2 \\ 0 & 0 & \boxed { 1 }  & 2 & { 3 }/{ 2 } \\ 0 & 0 & 0 & 0 & 0 \end{bmatrix}
$$

**Set the free variables to zero, get particular solution**
$$
 { X }_{ p }=\begin{bmatrix} 2 \\ 0 \\ -{ 3 }/{ 2 } \\ 0 \end{bmatrix}
$$

**Add nullspace to particular solution to get complete solution**

$$
 \begin{matrix} A{ X }_{ p }=b \\ AX_{ n }=0 \end{matrix}\Rightarrow A({ X }_{ p }+{ X }_{ n })=b 
$$

$$
{ X }_{ complete }=\begin{bmatrix} -2 \\ 0 \\ { 3 }/{ 2 } \\ 0 \end{bmatrix}+{ c }_{ 1 }\begin{bmatrix} -2 \\ 1 \\ 0 \\ 0 \end{bmatrix}+{ c }_{ 2 }\begin{bmatrix} 2 \\ 0 \\ -2 \\ 1 \end{bmatrix}
$$

### 3. Row, Column, Rank and Solution
Matrix A is a m by n matrix with rank r (then we know r <= m, r <= n).

**Full column rank(r=n)**

$$
A=\begin{bmatrix} 1 & 3 \\ 2 & 1 \\ 6 & 1 \\ 5 & 1 \end{bmatrix}\quad R=\begin{bmatrix} 1 & 0 \\ 0 & 1 \\ 0 & 0 \\ 0 & 0 \end{bmatrix}
$$

There is no free variables, so N(A) = {zero vector}. The solution to Ax=b is none or one particular solution.

**Full column rank(r=m)**

$$
A=\begin{bmatrix} 1 & 2 & 6 & 5 \\ 3 & 1 & 1 & 1 \end{bmatrix}\quad R=\begin{bmatrix} 1 & 0 & - & - \\ 0 & 1 & - & - \end{bmatrix}
$$

rref(A) has no all zero rows, so Ax=b can be solved for every b.

**All four situations**

$$
1.\quad r=m=n\\ \quad \quad R=I\quad \\ \quad 1\quad solution\\ \\ 2.\quad r=n<m\quad \\ \quad R=\begin{bmatrix} I \\ 0 \end{bmatrix}\\ \quad (0\quad or\quad 1\quad solution)\\ \\ 3.\quad r=m<n\\ \quad \quad R=\begin{bmatrix} I & F \end{bmatrix}\\ \quad \quad (\infty \quad solution)\\ \\ 4.\quad r<m,\quad r<n\\ \quad \quad R=\begin{bmatrix} I & F \\ 0 & 0 \end{bmatrix}\\ \quad \quad (0\quad or\quad \infty \quad solution)
$$

Notice that I and F might be column-mixed.
   

