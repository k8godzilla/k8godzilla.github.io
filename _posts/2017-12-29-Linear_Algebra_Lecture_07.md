---
layout:     post
title:      Lecture 07 (Linear Algebra)
subtitle:   
date:       2017-12-29
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 07

**Computing the Nullspace (Ax = 0)**

* Pivot Variables and Free Variables
* Special Solution, rref(A)

---
### Case 1
$$
\quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad \quad U\\ A=\begin{bmatrix} 1 & 2 & 2 & 2 \\ 2 & 4 & 6 & 8 \\ 3 & 6 & 8 & 10 \end{bmatrix}\Rightarrow \begin{bmatrix} 1 & 2 & 2 & 2 \\ 0 & 0 & 2 & 4 \\ 0 & 0 & 2 & 4 \end{bmatrix}\Rightarrow \begin{bmatrix} \boxed { 1 }  & 2 & 2 & 2 \\ 0 & 0 & \boxed { 2 }  & 4 \\ 0 & 0 & 0 & 0 \end{bmatrix}
$$
The first and third column are *pivot column*. The second and fourth column are *free variable*.

*The rank of Matrix A* is the number of pivot columns, which is 2 in this case.

Number of pivot variable is r = 2. Number of free variavle is n-r=4-2=2.

$$
\quad U=\begin{bmatrix} 1 & 2 & 2 & 2 \\ 0 & 0 & 2 & 4 \\ 0 & 0 & 0 & 0 \end{bmatrix}\Rightarrow \begin{bmatrix} 1 & 2 & 0 & -2 \\ 0 & 0 & 2 & 4 \\ 0 & 0 & 0 & 0 \end{bmatrix}\Rightarrow \begin{bmatrix} 1 & 2 & 0 & -2 \\ 0 & 0 & 1 & 2 \\ 0 & 0 & 0 & 0 \end{bmatrix}=R
$$

R is **reduced row echelon form** which has two properties:

* All pivots are one.
* All elements below and above pivots are zero.

Exchange the columns of R to make all pivot columns prior to free columns.
The rref would be transformed as below:
$$
R=\begin{bmatrix} I & F \\ 0 & 0 \end{bmatrix}\\ \quad \quad \quad \quad \\ Rx=0\quad \Rightarrow \quad \begin{bmatrix} I & F \\ 0 & 0 \end{bmatrix}\begin{bmatrix} { X }_{ pivot } \\ { X }_{ free } \end{bmatrix}\quad \Rightarrow \quad { X }_{ pivot }=-F{ X }_{ free }
$$

So the solution is:
$$
x=c\begin{bmatrix} -2 \\ 1 \\ 0 \\ 0 \end{bmatrix}+d\begin{bmatrix} 2 \\ 0 \\ -2 \\ 1 \end{bmatrix}
$$

### Case 2
$$
\quad \quad \quad A\quad \quad \quad \quad \quad \quad \quad \quad \quad U\quad \quad \quad \quad \quad \quad \quad \quad R\\ \begin{bmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 2 & 6 & 8 \\ 2 & 8 & 10 \end{bmatrix}\Rightarrow \begin{bmatrix} \boxed { 1 }  & 2 & 3 \\ 0 & \boxed { 2 }  & 2 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}\Rightarrow \begin{bmatrix} \boxed { 1 }  & 0 & 1 \\ 0 & \boxed { 1 }  & 1 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix}
$$

There is only one free column.

The solution is: 
$$
x=c\begin{bmatrix} -1 \\ -1 \\ 1 \end{bmatrix}
$$


