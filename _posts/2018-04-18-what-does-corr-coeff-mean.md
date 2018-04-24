---
layout: post
title: Difference between $\beta$, $r$, $r^2$ in computing Pearson and Spearman correlation
category: ep
---

Recently, I was working on an exploratory analysis to identify environmental and socioeconomic variables that are most correlated with disease prevalences on a population scale across different US cities. Before blindly computing these values, I wanted to get a deeper understanding of the assumptions behind computing a [Pearson correlation](https://en.wikipedia.org/wiki/Pearson_correlation_coefficient) and also remind myself of the relationship between $\beta$, $r$ and $r^2$ in simple linear regression. Furthermore, I wanted to explore exactly what this means in the context of Spearman correlates as well.

First of all, what is a Pearson correlation ($r$)?

In simple terms, it is a metric between -1 and 1 to measure the **linear** correlation.

In mathematical terms, it's basically just the covariance of two random variables normalized by their standard deviations.

In particular, it is the covariance of the normalization of two random variables. A simple derivation is as follows:

$$
\begin{align*}
cov(X,Y) &= E[(X - \mu_x)(Y - \mu_y)] \\
cov(\frac{X - \mu_x}{\sigma_x}, \frac{Y - \mu_y}{\sigma_y}) &= E[(\frac{X - \mu_x}{\sigma_x} - E[\frac{X - \mu_x}{\sigma_x}]) (\frac{Y - \mu_y}{\sigma_y} - E[\frac{Y - \mu_y}{\sigma_y}])] \\
&= E[\frac{1}{\sigma_x} (X - \mu_x - E[X-\mu_x]) \frac{1}{\sigma_y} (Y - \mu_y - E[Y - \mu_y])] \\
&= \frac{1}{\sigma_x \sigma_y} E[(X - E[X])(Y - E[Y])] \\
&= \frac{1}{\sigma_x \sigma_y} E[(X - \mu_x)(Y - \mu_y)] \\
&= \frac{1}{\sigma_x \sigma_y} cov(X,Y) \\
&= cor(X,Y)

\end{align*}
$$

Thus, we see that correlation is a scaled version of covariance. Using the Cauchy-Schwarz inequality, we can easily prove that correlation must, in fact, be between -1 and 1 as follows. For a closer look at this, see the tangential post I wrote about this! I must confess that while writing this post, I had somewhat of a linear algebra crisis about what it really means to take a dot product and why the definitions are the way they are, so I wrote a post for that separately!

$$


$$

Ok, this seems to make sense. Basically, the idea is to scale the variables so if they are measured in different units, or their ranges are wildly different we can account for that and then take the resulting covariance.

Now, back to linear regression.


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
