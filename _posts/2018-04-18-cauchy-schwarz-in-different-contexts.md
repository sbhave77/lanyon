---
layout: post
title: Musings about dot products, cauchy-schwarz inequality and inner product spaces
category: ep
---

I was just recently working on understanding the relationship between $\beta$, $r$ and $r^2$ and this led me to get into the weeds of linear algebra including dot products, inner product spaces and the Cauchy-Schwarz inequality. This post outlines my review and renewed understanding of these topics.

First of, what exactly is a dot product both mathematically and intuitively?

It's defined as follows in two different ways:
$$
\begin{align*}
a \cdot b &= \sum_{i=1}^{n} a_i b_i \text{   (algebraic definition)}\\
&= ||a|| ||b|| cos(\theta) \text{   (geometric definition)}
\end{align*}
$$

Intuitively, the dot product is essentially a scalar measure of how much two vectors are in the same direction.

![Geometric Dot Product Interpetation](images/dot_product.svg)
