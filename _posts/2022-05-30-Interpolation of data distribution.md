---
layout: post
author: Bohan and Tyler 
permalink: /2022/05/30/Understand-interpolation.html
image-slider: /assets/images/posts/Wass-dough.gif
categories: [Mentor]
excerpt_separator: <!--end_excerpt-->
---


<h5><span style="color:#00703C">Interpolate between Point Clouds in the Wasserstein space</span></h5>
<!--end_excerpt-->
<div class="row">
	<div class="column">
	<img class="img-fluid" src="{{'/assets/images/posts/Wass-dough.gif' | relative_url}}" alt="Wasserstein dough">
	</div>
		<div class="column">
	<img class="img-fluid" src="{{'/assets/images/posts/Wass-rotation.gif' | relative_url}}" alt="Wasserstein rotation">
	</div>
</div>

Tyler, an undergraduate at Dartmouth College, set out to truly grasp the concept of **Wasserstein interpolation**. Although this idea is far from new, it remains a fascinating and subtle phenomenon.

Given two measures $\mu_1$ and $\mu_2$, one may define the Wasserstein interpolation through either a given optimal transport map $T$:

\begin{equation}
\label{eq:Wass_int_map}
\mu_t = ((1-t)x+tT(x))_{\sharp}\mu_1;
\end{equation}

or a given optimal transport plan $P$:

\begin{equation}
\label{eq:Wass_int_plan}
\mu_t = ((1-t)x+ty)_{\sharp} P.
\end{equation}

As the animations above illustrate, it can behave in surprisingly unstable ways, at least in numerical experiments.

Consider two pairs of point clouds — blue at time 0 and red at time 1. In the top figure, the two clouds meet at a perfect right angle (90°), while in the bottom figure, the angle is slightly perturbed to 84.55°. Despite the small geometric difference, their Wasserstein interpolations diverge dramatically: the left one deforms smoothly, like kneading soft dough, whereas the right one almost performs a rigid rotation — more like a spinning baguette than a loaf being reshaped.

This contrast reveals both the beauty and the complexity of the Wasserstein interpolation. Optimal transport theory provides a partial explanation, yet a full understanding remains elusive — especially when we aim for predictable and controllable interpolations in practical applications.

Our current implementation owes much to Prof. Peyré’s excellent open-source experiments [[1]], particularly his formulation of optimal transport via linear programming. Moving forward, we plan to experiment with faster modern solvers [[2]] and explore more general multi-marginal OT (MMOT) frameworks [[3]] to push these ideas further.

----
##### References:


1. [Peyre, Numerical Tours.](https://www.numerical-tours.com/python/)
2. [Jacobs and Leger, The Back-and-Forth Method, 2020.](https://back-and-forth.netlify.app)
3. [Parno and Zhou, MMOT2D python package, 2022.](https://simda-muri.github.io/mmot/)

[1]: https://www.numerical-tours.com/python/
[2]: https://back-and-forth.netlify.app
[3]: https://simda-muri.github.io/mmot/

