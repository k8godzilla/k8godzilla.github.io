---
layout:     post
title:      Lecture 31 (Linear Algebra)
subtitle:   
date:       2018-01-18
author:     Sun Yin
header-img: img/tags_linearAlgebra.png
catalog: true
tags:
    - Linear Algebra
---
## Lecture 31

**1. Basis Change and Image Compression**

**2. Basis Change and Linear Transform**

---

### 1. Basis Change and Image Compression

The image data usually have a very high dimension. For example a 256 * 256 image has a dimension over 60000. One way to compress the data size is to apply a new set of basis to represent data, and set the coefs of some unimportant basis to 0.

Let $${x}_{old}$$ be the coefs of old basis, $${x}_{new}$$ be the new basis and $$W$$ be the new basis, then 

$$
{ x }_{ old }=W{ x }_{ new }
$$

$$
{ x }_{ new }={ W }^{ -1 }{ x }_{ old }
$$

So the key to choose a good basis is 

1. Inversion computation is fast.
2. Set some coefs to 0 would not lose much infomation.

One common used basis is Fourier Basis which we have seen in lecture before. Another is Wavelt basis. The 8*8 Wavelt basis is shown below:

$$
\begin{bmatrix} 1 \\ 1 \\ 1 \\ 1 \\ 1 \\ 1 \\ 1 \\ 1 \end{bmatrix},\begin{bmatrix} 1 \\ 1 \\ 1 \\ 1 \\ -1 \\ -1 \\ -1 \\ -1 \end{bmatrix},\begin{bmatrix} 1 \\ 1 \\ -1 \\ -1 \\ 0 \\ 0 \\ 0 \\ 0 \end{bmatrix},\begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \\ 1 \\ 1 \\ -1 \\ -1 \end{bmatrix},\begin{bmatrix} 1 \\ -1 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \end{bmatrix},...,\begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 1 \\ -1 \end{bmatrix}
$$

### 2. Basis Change and Linear Transform*

T is a linear transformation. And A is the corresponding matrix of T with respect to basis set V and B is the corresponding matrix of T with respect to basis set W. Then we have B is similar to A. That is to say, $$B={M}^{-1}AM$$.
