---
layout: post
author: Bohan 
date: 2022-11-05
permalink: /2022/11/05/Shape-Interpolation.html
image-slider: /assets/images/posts/barycenter-comp.png
<!-- excerpt: Multi-marginal optimal transport for the Wasserstein barycenter -->
categories: [Research]
excerpt_separator: <!--end_excerpt-->
paper: https://doi.org/10.1007/s10915-024-02572-8
code: https://simda-muri.github.io/mmot/
---


<h5><span style="color:grey">Use Multi-marginal optimal transport to compute exact Wasserstein barycenter</span></h5>
<!--end_excerpt-->

<div><img class="img-fluid" src="{{page.image-slider | relative_url}}" alt="Wasserstein Barycenter" /></div>

A barycenter-type problem asks the following: given a set of objects $(\mu_i)_{i=1}^m$,  we are looking for another object in the same space (or more formally, within the same category), that is close as possible to all of them with respect to a chosen metric or divergence.

\begin{equation}
\label{eq:bary}
\mu= \textrm{argmin}\sum_{i=1}^m \lambda_i \textrm{dis}(\mu_i,\mu).
\end{equation}

Depending on the metric, the barycenter contains "averaged" information from input objects.

In our problem, we are particularly interested in the space of probability measures equipped with the Wasserstein distance, which was introduced by Agueh and Carlier \[[1]\].

\begin{equation}
\label{eq:Wass_bary}
\mu= \textrm{argmin}\sum_{i=1}^m \frac{\lambda_i}{2} W_2^2(\mu_i,\mu).
\end{equation}

They showed it is equivalent to the MMOT under the cost 
\begin{equation}
c(x_1,\ldots,x_m)=\sum_{i<j}\frac{\lambda_i \lambda_j}{2} \|x_i-x_j\|^2.
\end{equation}

Out method \[[2]\] provides an exact and efficient way to solve the dual problem to the MMOT problem, 
$$
\begin{eqnarray}
&\sup& \sum_{i=1}^m \int f_i(x_i) \mathrm{d}\mu_i;\\
&\textrm{s.t.}& \sum_{i=1}^m f_i(x_i)\leqslant c(x_1,\ldots,x_m).
\end{eqnarray}
$$
and the dual variables $(f_i)$, as one of outputs, can induce the Wasserstein barycenter by
\begin{equation}
\label{eq:pushforward}
\mu= (\textrm{id} - \frac{\nabla f_i}{\lambda_i})_{\sharp} \mu_i.
\end{equation}

----
##### References:


1. [Agueh and Carlier, Barycenter in the Wasserstein space, 2011.](http://doi.org/10.1137/100805741)
2. [Zhou and Parno, Efficient and Exact Multimarginal Optimal Transport with Pairwise Costs, 2022.](https://arxiv.org/abs/2208.03025)


[1]: http://doi.org/10.1137/100805741
[2]: https://arxiv.org/abs/2208.03025



