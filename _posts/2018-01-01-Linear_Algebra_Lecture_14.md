---
layout:     post
title:      Lecture 14 (Linear Algebra)
subtitle:   
date:       2018-01-01
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 14

**1. Orthognal vectors and subspaces**

**2. Nullspace$$\bot$$Rowspace**

**3. N($${A}^{T}$$A)=N(A)**

---

### 1. Orthognal vectors and subspaces

**From Phythagoras to orthognal vectors**

According to Phythagoras, in a right trianle:

$$
{ \left\| x \right\|  }^{ 2 }+{ \left\| y \right\|  }^{ 2 }={ \left\| x+y \right\|  }^{ 2 }\\ \\ { \left\| x \right\|  }^{ 2 }+{ \left\| y \right\|  }^{ 2 }={ \left\| x \right\|  }^{ 2 }+{ \left\| y \right\|  }^{ 2 }+{ x }^{ T }y+{ y }^{ T }x={ \left\| x \right\|  }^{ 2 }+{ \left\| y \right\|  }^{ 2 }+{ 2x }^{ T }y\\ \\ { x }^{ T }y=0\quad -\quad orthognal\quad condition
$$

**Orthognal subspaces**

Definition: S$$\bot$$U $$\Leftrightarrow $$ every vector in S is perpendicular to every vector in T.


### 2. Nullspace$$\bot$$Rowspace

Rowspace is orthognal to Nullspace. Why?

$$
Ax=0\quad \Rightarrow \quad \begin{bmatrix} { row }_{ 1 }\quad of\quad A \\ { row }_{ 2 }\quad of\quad A \\ ...... \\ { row }_{ m }\quad of\quad A \end{bmatrix}\begin{bmatrix} | \\ x \\ | \end{bmatrix}=0\quad \Rightarrow \quad { ({ c }_{ 1 }{ row }_{ 1 }+{ c }_{ 2 }{ row }_{ 2 }+...+{ c }_{ m }{ row }_{ m }) }^{ T }x=0
$$

Actually nullspace are not only the orthognal subspace of rowspace. It contains all vectors perpendicular to rowspace. So nullspace and rowspace are **orthognal complements** in $${R}^{N}$$.

### 3. N($${A}^{T}$$A)=N(A)

**Problem**

Considering equation system Ax=b，it might have no solution if m>n.

**How to solve?**

To tackle this problem, we can solve $${A}^{T}A\hat { x }={A}^{T}b$$ instead of Ax=b.

**Invertibility of $${A}^{T}A$$**

To solve  $${A}^{T}A\hat { x }={A}^{T}b$$, we need to make sure $${A}^{T}A$$ be invertible.

A is m by n matrix, and $${A}^{T}A$$ is n by n matrix.

Because $${ A }^{ T }Ax=0\quad \Leftrightarrow \quad Ax=0$$, N($${A}^{T}$$A)=N(A). And because A and $${A}^{T}$$ have same number of columns, they share rank.

$${A}^{T}A$$ is invertible $$\Leftrightarrow$$ rank of $${A}^{T}A$$ and A is n $$\Leftrightarrow$$ A has independent columns.

Invertible $${A}^{T}A$$:

$$
\begin{bmatrix} 1 & 1 & 1 \\ 1 & 2 & 5 \end{bmatrix}\begin{bmatrix} 1 & 1 \\ 1 & 2 \\ 1 & 5 \end{bmatrix}=\begin{bmatrix} 3 & 8 \\ 8 & 30 \end{bmatrix}
$$

Uninvertible $${A}^{T}A$$:

$$
\begin{bmatrix} 1 & 1 & 1 \\ 3 & 3 & 3 \end{bmatrix}\begin{bmatrix} 1 & 3 \\ 1 & 3 \\ 1 & 3 \end{bmatrix}=\begin{bmatrix} 3 & 9 \\ 9 & 27 \end{bmatrix}
$$


