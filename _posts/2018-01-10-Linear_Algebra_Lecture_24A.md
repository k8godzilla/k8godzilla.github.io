---
layout:     post
title:      Lecture 24A (Linear Algebra)
subtitle:   
date:       2018-01-10
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 24A

**1. Markov Matrices**

**2. Fourier Series and Orthogonal Projection**

---

### 1. Markov Matrices

**Example Matrices**

$$
A=\begin{bmatrix} 0.1 & 0.01 & 0.3 \\ 0.2 & 0.99 & 0.3 \\ 0.7 & 0 & 0.4 \end{bmatrix}
$$

**What is Markov Matrices**

1. All entries $$\ge 0$$.
2. All columns add to 1

**Eigenvalues and Eigenvectors of Markov Matrices**

1. $$\lambda = 1$$ is a eigenvalue, let it be $${\lambda}_{1}$$.
2. All other $$\begin{vmatrix} { \lambda  }_{ i } \end{vmatrix}<1$$.
3. all entries of $${x}+{1}$$ >0.
4. $${u}_{k}={c}_{1}{]lambda}_{1}{x}_{1}+{c}_{2}{]lambda}_{2}{x}_{2}+{c}_{3}{]lambda}_{3}{x}_{3}+...={c}_{1}{x}_{1}$$

**Solve Markov Matrices**

$$
{ \lambda  }_{ 1 }=1,\quad { x }_{ 1 }=\begin{bmatrix} 0.6 \\ 33 \\ 0.7 \end{bmatrix}
$$

$${c}_{1}$$ is decided by initial state.

**Example: California and massachusetts**

*Equation*

$$
\begin{bmatrix} { u }_{ cal } \\ { u }_{ mass } \end{bmatrix}=\begin{bmatrix} 0.9 & 0.2 \\ 0.1 & 0.8 \end{bmatrix}\begin{bmatrix} { u }_{ cal } \\ { u }_{ mass } \end{bmatrix}
$$

$$
{ u }_{ 0 }=\begin{bmatrix} 0 \\ 1000 \end{bmatrix}
$$

*Solve eigenvalue and eigenvectors*

$$
{ \lambda  }_{ 1 }=1,\quad { x }_{ 1 }=\begin{bmatrix} 2 \\ 1 \end{bmatrix}\\ { \lambda  }_{ 2 }=0.7,\quad { x }_{ 2 }=\begin{bmatrix} -1 \\ 1 \end{bmatrix}
$$

*Solution*

$$
{ u }_{ k }=\frac { 1000 }{ 3 } { 1 }^{ k }\begin{bmatrix} 2 \\ 1 \end{bmatrix}+\frac { 2000 }{ 3 } { (0.7) }^{ k }\begin{bmatrix} -1 \\ 1 \end{bmatrix}
$$

### 2. Fourier Series and Orthogonal Projection

**Orthogonal Projection**

$${q}_{1}$$,$${q}_{2}$$,...,$${q}_{n}$$ are orthogonal basis.

$$
v={ q }_{ 1 }{ x }_{ 1 }+{ q }_{ 2 }{ x }_{ 2 }+...+{ q }_{ n }{ x }_{ n }
$$

Because of orthhogonality:

$$
{ q }_{ 1 }^{ T }v={ { x }_{ 1 } }
$$

**Fourier Series**

*The Series*

$$
f(x)={ a }_{ 0 }1+{ a }_{ 1 }\cos { x } +{ b }_{ 1 }\sin { x } +{ a }_{ 2 }\cos { 2x } +{ b }_{ 2 }\sin { 2x } +...
$$

*Vectors Product*

$$
{ v }^{ T }w={ v }_{ 1 }{ w }_{ 1 }+{ v }_{ 2 }{ w }_{ 2 }+...+{ v }_{ n }{ w }_{ n }
$$

*Function Product Analogy*

$$
{ f }^{ T }g=\int _{ 0 }^{ 2\pi  }{ f(x)g(x)dx } 
$$

*Orthogonality of Fourier Series*

Fact: All basis of fourier series is orthogonal with each other.

Therefore the fourier series can have this kind of manipulation:

$$
{ f }(x)\cos { (x) } =\int _{ 0 }^{ 2\pi  }{ { (\cos { x } ) }^{ 2 }dx } 
$$




