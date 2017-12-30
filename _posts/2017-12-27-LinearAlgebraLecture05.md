---
layout:     post
title:      Lecture 05 (Linear Algebra)
subtitle:   
date:       2017-12-27
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: false
tags:
    - Linear Algebra
---

## Lecture 05
1. PA = LU

2. Symmetrical Matrix

3. Vector Space, Subspaces

---
### 1. PA = LU

All invertible matrix can be transformed into PA = LU, where P is permutation matrix.

###  2. Symmetrical Matrix
\\({ R }^{ T }R\\)must be symmetrical metrix. Proof is below
$$
{ ({ R }^{ T }R) }^{ T }={ R }^{ T }{ ({ R }^{ T }) }^{ T }={ R }^{ T }R
$$
### 3. Vector Space and Subspace
#### What is Vector Space
A vector space (also called a linear space) is a collection of objects called vectors, which may be added together and multiplied ("scaled") by numbers, called scalars. 
#### Vector Space Example
\\({ R }^{ 2 }\\) - all 2-dim real vectors.

\\({ R }^{ 3 }\\) - all vectors with 3 components.
  
#### Non Vector Space Example
![](/img/01.jpg)
The graph above is not a vector space, because the product between a vector in this space and a negative scalar will be outside of this space.

#### Subspace
Subspace is a vector space that is included by another vector space.

**Example:** 

Subspace of \\({R}^{2}\\)

1. all of \\({R}^{2}\\)
2. any line that through origin point
3. zero vector itself

Subspace of \\({R}^{3}\\)

1. all of \\({R}^{3}\\)
2. any plane through origin point
3. any line through origin point
4. zero vector itself

#### What is Column Space?
In linear algebra, the column space of a matrix A is the span (set of all possible linear combinations) of its column vectors. 

**Example**

The column space of matrix below is all linear combinations of its two column vectors.
$$
A=\begin{bmatrix} 1 & 3 \\ 2 & 3 \\ 4 & 1 \end{bmatrix}
$$







