---
layout: post
author: Bohan
date: 2022-10-17
permalink: /2022/10/17/Robertson-Channel.html
image-slider: /assets/images/posts/Bohan_icefloe.gif
<!-- excerpt: Multi-marginal optimal transport for Sea Ice Dynamics Prediction -->
categories: [Research]
excerpt_separator: <!--end_excerpt-->
---


<h5><span style="color:grey">Use Multi-marginal Optimal Transport for Sea Ice Dynamics Prediction</span></h5>
<!--end_excerpt-->

<img class="img-fluid" src="{{page.image-slider | relative_url}}" alt="Robertson Channel">

Joint with M. Parno \[[1]\], we develop a multi-marginal optimal transport (MMOT) framework for constructing **continuous representations of discrete-in-time data**. One natural application is in **predicting the sea ice dynamics**. Given a sequence of observations (the “marginals” in the MMOT framework) recorded at different time points, our method produces a continuous-time interpolation that captures the evolving motion of sea ice. This provides a solution to one stage in the [Lagrangian Observation Mapping Challenges](https://simda-muri.github.io/challenges/source/descriptions/problem2.html). The accompanying Python package and documentation are available in \[[2]\].

Using the SAR data (collected every 6 days) from [Alaska Satellite Facility](https://asf.alaska.edu) on the Robertson Channel (thanks to our group member J. Park at Dartmouth), the animation demonstrates predicted sea ice motion at two-day intervals. Remarkably, even finer temporal predictions can be generated within minutes on a standard personal computer.

----
##### References:

1. [Zhou and Parno, Efficient and Exact Multimarginal Optimal Transport with Pairwise Costs, 2022.](https://arxiv.org/abs/2208.03025)
2. [Parno and Zhou, MMOT2D python package, 2022.](https://simda-muri.github.io/mmot/)


[1]: https://arxiv.org/abs/2208.03025
[2]: https://simda-muri.github.io/mmot/

