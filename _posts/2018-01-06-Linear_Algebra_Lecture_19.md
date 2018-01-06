---
layout:     post
title:      Lecture 19 (Linear Algebra)
subtitle:   
date:       2018-01-06
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 19

**1. Big formula for det A**

**2. Cofactor**

**3.Tridiagnal matrix** 

---

### 1. Big formula for det A

**Review: three basic properties**

1. det I = 1.
2. sign reverse with row exchange.
3. det is linear in each row seperately.

**3by3 matrix case**

$$
\begin{vmatrix} { a }_{ 11 } & { a }_{ 12 } & { a }_{ 13 } \\ { a }_{ 21 } & { a }_{ 22 } & { a }_{ 23 } \\ { a }_{ 31 } & { a }_{ 32 } & { a }_{ 33 } \end{vmatrix}=\begin{vmatrix} { a }_{ 11 } & 0 & 0 \\ 0 & { a }_{ 22 } & 0 \\ 0 & 0 & { a }_{ 33 } \end{vmatrix}+\begin{vmatrix} { a }_{ 11 } & 0 & 0 \\ 0 & 0 & { a }_{ 23 } \\ 0 & { a }_{ 32 } & 0 \end{vmatrix}+\begin{vmatrix} 0 & { a }_{ 12 } & 0 \\ 0 & 0 & { a }_{ 23 } \\ { a }_{ 31 } & 0 & 0 \end{vmatrix}+\begin{vmatrix} 0 & { a }_{ 12 } & 0 \\ { a }_{ 21 } & 0 & 0 \\ 0 & 0 & { a }_{ 33 } \end{vmatrix}+\begin{vmatrix} 0 & 0 & { a }_{ 13 } \\ { a }_{ 21 } & 0 & 0 \\ 0 & { a }_{ 32 } & 0 \end{vmatrix}+\begin{vmatrix} 0 & 0 & { a }_{ 13 } \\ 0 & { a }_{ 22 } & 0 \\ { a }_{ 31 } & 0 & 0 \end{vmatrix}
$$

$$
det\quad A={ a }_{ 11 }{ a }_{ 22 }{ a }_{ 33 }-{ a }_{ 11 }{ a }_{ 23 }{ a }_{ 32 }+{ a }_{ 12 }{ a }_{ 23 }{ a }_{ 31 }-{ a }_{ 12 }{ a }_{ 21 }{ a }_{ 33 }+{ a }_{ 13 }{ a }_{ 21 }{ a }_{ 32 }+{ -a }_{ 13 }{ a }_{ 22 }{ a }_{ 31 }
$$

**Big formula**

$$
det\quad A=\sum _{ n!\quad terms }^{  }{ { a }_{ 1\alpha  }{ a }_{ 2\beta  }{ a }_{ 3\gamma  }...{ a }_{ n\omega  } } 
$$

$$(\alpha ,\beta ,\gamma ...\omega )$$ is permutation of $$(1, 2, 3,...,n)$$

**A 4by4 example**

$$
\begin{vmatrix} 0 & 0 & 1 & 1 \\ 0 & 1 & 1 & 0 \\ 1 & 1 & 0 & 0 \\ 1 & 0 & 0 & 1 \end{vmatrix}=\begin{vmatrix} 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0 \\ 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1 \end{vmatrix}+\begin{vmatrix} 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \\ 0 & 1 & 0 & 0 \\ 1 & 0 & 0 & 0 \end{vmatrix}=-1+1=0
$$

The first matrix needs 1(odd) step column exchange to convert to identity matrix, therefor its determinant is -1.

The second matrix needs 2(even) steps column exchange to convert to identity matrix, therefor its determinant is +1.

### 2. Cofactor

**3by3 matrix case**

In the 3by3 matrix case, notice that

$$
\begin{vmatrix} { a }_{ 11 } & 0 & 0 \\ 0 & { a }_{ 22 } & 0 \\ 0 & 0 & { a }_{ 33 } \end{vmatrix}+\begin{vmatrix} { a }_{ 11 } & 0 & 0 \\ 0 & 0 & { a }_{ 23 } \\ 0 & { a }_{ 32 } & 0 \end{vmatrix}=\begin{vmatrix} { a }_{ 11 } & 0 & 0 \\ 0 & { a }_{ 22 } & { a }_{ 23 } \\ 0 & { a }_{ 32 } & { a }_{ 33 } \end{vmatrix}=\begin{vmatrix} { a }_{ 11 } & 0 \\ 0 & { A }_{ 23 } \end{vmatrix}={ a }_{ 11 }({ a }_{ 22 }{ a }_{ 33 }-{ a }_{ 23 }{ a }_{ 32 })={ a }_{ 11 }\left| { A }_{ 23 } \right| \quad ,\quad { A }_{ 23 }=\begin{vmatrix} { a }_{ 22 } & { a }_{ 23 } \\ { a }_{ 32 } & { a }_{ 33 } \end{vmatrix}
$$

and

$$
\begin{vmatrix} 0 & { a }_{ 12 } & 0 \\ { a }_{ 21 } & 0 & 0 \\ 0 & 0 & { a }_{ 33 } \end{vmatrix}+\begin{vmatrix} 0 & { a }_{ 12 } & 0 \\ 0 & 0 & { a }_{ 23 } \\ { a }_{ 31 } & 0 & 0 \end{vmatrix}=\begin{vmatrix} 0 & { a }_{ 12 } & 0 \\ { a }_{ 21 } & 0 & { a }_{ 23 } \\ { a }_{ 31 } & 0 & { a }_{ 33 } \end{vmatrix}=-\begin{vmatrix} { a }_{ 12 } & 0 \\ 0 & { A }_{ 13 } \end{vmatrix}={ a }_{ 12 }({ a }_{ 23 }{ a }_{ 31 }-{ a }_{ 21 }{ a }_{ 33 })={ a }_{ 12 }\left| { A }_{ 13 } \right| \quad ,\quad { A }_{ 13 }=\begin{vmatrix} { a }_{ 21 } & { a }_{ 23 } \\ { a }_{ 31 } & { a }_{ 33 } \end{vmatrix}\\
$$

**Definition**


Then we can generate the difinition of cofactor

$$
cofactor\quad of\quad { a }_{ ij }={ C }_{ ij }=det(matrix\quad with\quad row\quad i\quad and\quad column\quad j\quad erased)\quad *\quad \begin{cases} +1\quad (i+j)\quad is\quad even \\ -1\quad (i+j)\quad is\quad odd \end{cases}
$$

i + j is odd means $${a}_{ij}$$ needs odd step row and column exchange to move to (1,1), vice versa.

**Cofactor formula**

The cofactor formula along row 1 is:

$$
det(A)={ a }_{ 11 }{ C }_{ 11 }+{ a }_{ 12 }{ C }_{ 12 }+...+{ a }_{ 1n }{ C }_{ 1n }
$$

### 3.Tridiagnal matrix

$$
{ A }_{ 4 }=\begin{vmatrix} 1 & 1 & 0 & 0 \\ 1 & 1 & 1 & 0 \\ 0 & 1 & 1 & 1 \\ 0 & 0 & 1 & 1 \end{vmatrix}\quad 
$$

$$
\begin{vmatrix} { A }_{ 1 } \end{vmatrix}=1,\quad \begin{vmatrix} { A }_{ 2 } \end{vmatrix}=0,\quad \begin{vmatrix} { A }_{ 3 } \end{vmatrix}=-1\quad 
$$

$$
\begin{vmatrix} { A }_{ 4 } \end{vmatrix}=1*\begin{vmatrix} { A }_{ 3 } \end{vmatrix}-\begin{vmatrix} { A }_{ 2 } \end{vmatrix}\\ 
$$

$$
\begin{vmatrix} { A }_{ n } \end{vmatrix}=1*\begin{vmatrix} { A }_{ n-1 } \end{vmatrix}-\begin{vmatrix} { A }_{ n-2 } \end{vmatrix}\\ 
$$

$$
\begin{vmatrix} { A }_{ 5 } \end{vmatrix}=0,\quad \begin{vmatrix} { A }_{ 6 } \end{vmatrix}=1,\quad \begin{vmatrix} { A }_{ 7 } \end{vmatrix}=1\quad 
$$

The determinants of tridiagnal matrix familiy is a loop with 6 as the period.


