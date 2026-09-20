---
layout: post
author: Bohan 
permalink: /2020/08/31/Sea-Ice-Dynamics-via-regularized-optimal-transport.html
image-slider: /assets/images/posts/parno-GRL2019.png
<!-- excerpt: Measuring Ice Motion with Optimal Transport -->
categories: [Learning]
---

<h5><span style="color:#F58025">Measure Ice Motion with Regularized Optimal Transport</span></h5>


<img class="img-fluid" src="{{page.image-slider | relative_url}}" alt="OT">

In [[1]], the authors introduced an innovative approach to **estimating ice motion** from satellite imagery through the lens of optimal transport. The key idea is to view each image as a probability distribution and to compute an efficient, regularized optimal transport map that minimizes the “distance” between images captured on consecutive days. From this optimal transformation, one can infer displacement fields, velocities, and even strain patterns in the ice flow.

While elegant and computationally tractable, this framework has two main limitations. First, it is restricted to *two marginals*, meaning it can only compare images pairwise in time. Second, the entropic regularization that enables fast computation also introduces *blurring artifacts*, which can obscure fine-scale motion features.

These limitations motivated our project, which aims to develop an **exact, multi-marginal optimal transport (MMOT)**, which is capable of handling multiple time steps simultaneously while preserving sharper and more physically meaningful motion estimates.


----
##### References:


1. [Parno et al., Remote measurement of sea ice dynamics with regularized optimal transport, 2019](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/2019GL083037)

[1]: https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/2019GL083037
