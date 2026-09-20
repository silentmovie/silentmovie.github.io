---
layout: post
author: Bohan
date: 2020-07-20
permalink: /2020/07/20/RT.html
image-slider: /assets/images/posts/movie6.png
categories: [Research]
excerpt_separator: <!--end_excerpt-->
code: https://github.com/silentmovie/RTmodel
---


<h5><span style="color:grey">Mixing under Rayleigh-Taylor instability</span></h5>
<!--end_excerpt-->

<div class="row">
<img class="img-fluid" src="{{'assets/images/posts/zmodel.mov' | relative_url}}" alt="Zmodel">
</div>

This project continues the line of research initiated in [[1]], where the authors derived an asymptotic model for the motion of **multiphase incompressible Euler flows** in two dimensions, subject to **Rayleigh–Taylor (RT) instability** and capable of describing **turn-over phenomena**.

The Matlab simulations in [[2]] visualize the **mixing process** driven by RT instability — even in immiscible fluids where no diffusion is present. For a detailed discussion on how to quantify the degree of mixing without diffusion, see [[3]].

In the movie, the top panel simulates the "rocket rig" experiment (mixing of an NaI solution and pentane accelerated by rocket motors). It performs ensemble averaging over multiple runs. The second panel shows the occupied density within the zoom-in window, averaged across all realizations. The third panel tracks the evolution of mixedness in terms of $\dot{H}^{-1}$ norm. The fourth panel illustrates the influence of artificial viscosity on the dynamics.

Please refer to \[[4]\] for the recent refinement and development.

----
##### References:


1. [Granero-Belinchon and Shkoller, A model for Rayleigh-Taylor mixing and interface turn-over, 2017.](https://epubs.siam.org/doi/pdf/10.1137/16M1083463?casa_token=0dRxZ_jt06AAAAAA:T2Bgm0RnBw64UHFZygEuj4gScaPw01fnfWQU0APePKiajut4Bui_B03K4PeqUFfZ85MaITV9ow)
2. [Zhou, RTmodel, 2020.](https://github.com/silentmovie/RTmodel)
3. [Thiffeault, Using multiscale norms to quantify mixing and transport, 2011.](https://iopscience.iop.org/article/10.1088/0951-7715/25/2/R1/pdf?casa_token=kxRedMFYm1QAAAAA:jtsmOCS0mceHwfRLlOsfEvV5YVVmZj-HNqMCKgyXhoac7HOUkUaKnyfEQlOruM9SJ1dL54_R1Q)
4. [Pandya and Shkoller, 3D interface models for Rayleigh-Taylor Problems, 2022.](https://arxiv.org/abs/2201.04538)


[1]: https://epubs.siam.org/doi/pdf/10.1137/16M1083463?casa_token=0dRxZ_jt06AAAAAA:T2Bgm0RnBw64UHFZygEuj4gScaPw01fnfWQU0APePKiajut4Bui_B03K4PeqUFfZ85MaITV9ow
[2]: https://github.com/silentmovie/RTmodel
[3]: https://simda-muri.github.io/mmot/
[4]: https://arxiv.org/abs/2201.04538

