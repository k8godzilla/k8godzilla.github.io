---
layout:     post
title:      Lecture 12 (Linear Algebra)
subtitle:   
date:       2017-12-31
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 12

**1. Graph a network**

**2. Incidence matrices, potential view**

**3. Kirchhoff Circuit Laws, current view**

**4. Eular's formula**

---

### 1. Graph a network

![](img/LA_10_01.jpg)

Nodes: n = 4
Edges: m = 5

### 2. Incidence matrices, potential view

$$
A=\begin{bmatrix} -1 & 1 & 0 & 0 \\ 0 & -1 & 1 & 0 \\ -1 & 0 & 1 & 0 \\ -1 & 0 & 0 & 1 \\ 0 & 0 & -1 & 1 \end{bmatrix}
$$

The columns of A represent the nodes and the rows represent the edges. Each row shows that a current flow from one node into another. And the sum of each row equals to 0 if there if no potential difference between nodes it connencts.

rank(A) = 3. dim(N(A)) = 4-3 =1.

Assume that every node has same potential, then Ax=0:

$$
Ax=\begin{bmatrix} { x }_{ 2 }-{ x }_{ 1 } \\ { x }_{ 3 }-{ x }_{ 2 } \\ { x }_{ 3 }-{ x }_{ 1 } \\ { x }_{ 4 }-{ x }_{ 1 } \\ { x }_{ 4 }-{ x }_{ 3 } \end{bmatrix}=\begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \\ 0 \end{bmatrix}\quad \quad \quad x=c\begin{bmatrix} 1 \\ 1 \\ 1 \\ 1 \\ 1 \end{bmatrix}
$$

If add some outer potential to this system, the incidence matrices would become Ax = f, where f is the new potential difference.

### 3. Kirchhoff Circuit Laws, current view

According to the Kirchhoff Circuit Laws, the principle of conservation of electric charge implies that:

>At any node (junction) in an electrical circuit, the sum of currents flowing into that node is equal to the sum of currents flowing out of that node
or equivalently

or equivently:

>The algebraic sum of currents in a network of conductors meeting at a point is zero.

$${A}^{T}$$y=0 is the linear algebra form of kirchhoff lows.


$$
\begin{bmatrix} -1 & 0 & -1 & -1 & 0 \\ 1 & -1 & 0 & 0 & 0 \\ 0 & 1 & 1 & 0 & -1 \\ 0 & 0 & 0 & 1 & 1 \end{bmatrix}\begin{bmatrix} { y }_{ 1 } \\ { y }_{ 2 } \\ { y }_{ 3 } \\ { y }_{ 4 } \\ { y }_{ 5 } \end{bmatrix}=\begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \end{bmatrix}
$$

The rows represent the current flow of node. The columns represent the nodes.

dim(N($${A}^{T}$$))=5-rank of ($${A}^{T}$$) = 5-3=2

The basis is:

$$
\begin{bmatrix} 1 \\ 1 \\ -1 \\ 0 \\ 0 \end{bmatrix},\begin{bmatrix} 0 \\ 0 \\ 1 \\ -1 \\ 1 \end{bmatrix}
$$

These two basis are the two loops of the network.

### 4. Eular's formula

In our network case:

Number of loops = the number of free variables of $${A}^{T}$$ = m - r.

m = number of edges.

r = number of nodes - 1.

So, number of loops = number of edges - number of nodes + 1.

This is Eular's formula and can be applied to any network.

Notice that the loop in our discussion should be dependent - none edge is inside the loop. 
 

