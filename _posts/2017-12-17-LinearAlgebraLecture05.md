---
layout:     post
title:      Lecture 05
subtitle:   PA = LU, Vector Space and Subspace
date:       2017-12-27
author:     Sun Yin
header-img: img/tags_linearAlgebra.jpg
catalog: true
tags:
    - Linear Algebra
---

#Lecture 05
**1. PA = LU**
**2. Symmetrical Matrix**
**3. Vector Space, Subspaces**

---
###01. PA = LU
All invertible matrix can be transformed into PA = LU, where P is permutation matrix.

###02. Symmetrical Matrix
![](/Users/sunyin/k8godzilla.github.io/img/linear_Algebra/lecture05_symmeric_transpose.png)
###03. Vector Space and Subspace
#####a. What is vector space
A vector space (also called a linear space) is a collection of objects called vectors, which may be added together and multiplied ("scaled") by numbers, called scalars. 
#####b. Vector Space Example
<math><mrow>
    <msup>
      <mi>R</mi>
      <mn>2</mn>
    </msup>
  </mrow></math> - all 2-dim real vectors.
  
  <math><mrow>
    <msup>
      <mi>R</mi>
      <mn>3</mn>
    </msup>
  </mrow></math> - all vectors with 3 components.
  
#####c. Non Vector Space Example
you can use an inline formula $$\forall x \in R$$ like this one  

Here is an example MathJax inline rendering \\( 1/x^{2} \\), and here is a block rendering: 
\\[ \frac{1}{n^{2}} \\]

$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$