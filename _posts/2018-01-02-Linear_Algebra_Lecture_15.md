---
layout:     post
title:      Lecture 15 (Linear Algebra)
subtitle:   
date:       2018-01-02
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 15

**1. Why project?**

**2. Projections to line**

**3. Projections to plane**

---

### 1. Why project?

Because Ax=b may have no solution, we solve $$A\hat{x}=p$$ instead, where p is the projection of b onto the column space of A.

### 2. Projections to line

![](/img/linear_Algebra/projecction_to_line.001.jpg)

Because the projection point is on line a, we can write as xa. The line that goes through b and projection point is orthognal to a, we apply this condition to derive projection matrix and projection point:

$$
{a}^{T}(b-ax)=0
$$

$$
{a}^{T}ax={a}^{T}b
$$

$$
x=\frac { { a }^{ T }b }{ { a }^{ T }a } 
$$

$$
projection\quad point\quad p=ax=\frac { a{ a }^{ T }b }{ { a }^{ T }a } 
$$

$$
projection\quad matrix\quad P\quad =\quad \frac { { a }{ a }^{ T } }{ { a }^{ T }a } 
$$

Projection point can be wriiten as p = Pb. As projection matrix P can and only can project to any point on a, P share column space with a. And rank(P) = rank(a) = 1.

Projection matrix has two important properties:

* $${P}^{T}=P$$ **symmetrical**
* $${P}^{2}=P$$ **projecting twice is equivlant to once**

### 3. Projections to plane

![](/img/linear_Algebra/projecction_to_plane.001.jpg)

The plane is the column space of $${a}_{1}$$ and $${a}_{2}$$, So any point on the plane can be written as $$A\hat { x }$$ where $$A=\begin{bmatrix} { a }_{ 1 } & { a }_{ 2 } \end{bmatrix}$$.

The problem is to find $$\hat{x}$$, s.t. $$e=b-a\hat{x}$$ is perpendicular to plane.

$$
{ a }_{ 1 }^{ T }(b-A\hat { x } )=0\quad { a }_{ 2 }^{ T }(b-A\hat { x } )=0\quad 
$$

Combine the two equations into a unified matrix form.

$$
\begin{bmatrix} { a }_{ 1 }^{ T } \\ { a }_{ 2 }^{ T } \end{bmatrix}(b-A\hat { x } )=\begin{bmatrix} 0 \\ 0 \end{bmatrix}
$$

$$
{ A }^{ T }(b-A\hat { x } )=0
$$

Then we find that $$e=b-A\hat { x } $$ is in $$N({A}^{T})$$. Because space of $$N({A}^{T})$$ is orthognal to C(A), e is perpendicular to C(A). That's just what we want to ensure.

$$
\hat { x } ={ ({ A }^{ T }A) }^{ -1 }{ A }^{ T }b
$$

$$
projection\quad point\quad p=A\hat { x } =A{ ({ A }^{ T }A) }^{ -1 }{ A }^{ T }b
$$

$$
projection\quad matrix\quad P=A{ ({ A }^{ T }A) }^{ -1 }{ A }^{ T }
$$



