---
layout: page
title: Teaching
class: teaching
permalink: /teaching/
---


{:.hidden}

<!-- ## Current Teaching

Parental leave -->

## Teaching Practice

<section class="teaching-feedback" aria-labelledby="student-feedback">
  <div class="teaching-feedback-copy">
    <h3 id="student-feedback">Student Feedback</h3>
    <p>I welcome questions during lectures, breaks, and office hours. Students can return to an explanation and work through the step that has left them stuck. Their feedback helps me decide where an explanation needs more attention.</p>
  </div>
  <figure class="teaching-feedback-figure">
    <img src="{{ '/assets/teaching/student-feedback-word-cloud.png' | relative_url }}" width="515" height="268" alt="Word cloud of positive student feedback, with prominent phrases including office hour, outside class, very helpful, very patient, and explained concepts.">
    <figcaption>Frequent words in positive comments from course evaluations.</figcaption>
  </figure>
</section>

### Course Reflections

*“It is rare in a math course for students to speak,”* one of my students once remarked. I believe that encouraging reflections and discussions during lectures provides valuable opportunities to turn mistakes and misunderstandings into active learning experiences, helping students build confidence in their reasoning. Here are some sample presentations.

[[M117]({{site.baseurl}}/assets/teaching/XiHe_M117.pdf)]; [[M108A]({{site.baseurl}}/assets/teaching/JiQi_M108A.pdf)]; [[M108B]({{site.baseurl}}/assets/teaching/MariaSegall_M108B.pdf)];


### Teamworks

*"I enjoyed being able to work with groupmates on a presentation and broadening my understanding of numerical analysis as well as programming."* quoted from my course evalutions. Here are some sample presentations credits to my wonderful students.

[[DFT-FFT]({{site.baseurl}}/assets/teaching/DFT-FFT.pdf)] by Yilin, Minxi, Puyuan and Yixiao.\\
[[Numerical Differentiation Visualizer](https://github.com/InariHimeko/fft_visual)] by Yijia, Wenxuan, Peter and Leyang.\\
[[Gaussian Elimination and Error Estimations]({{site.baseurl}}/assets/teaching/GaussElimination.pptx)] by Joseph, Ryan, Xinwei and Joo Ho.\\
[[Gram-Schmidt Instability]({{site.baseurl}}/assets/teaching/GS-instability.pdf)] by Angelina, Ron and Param.


## Past Teaching

<section class="teaching-list">
  {% for inst in site.data.courses %}
    <article class="teaching-institution">
      <h3 id="y{{ forloop.index0 }}">{{ inst.location }}</h3>
      <ul>
        {% for course in inst.courses %}
          <li>{{ course.title }}</li>
        {% endfor %}
      </ul>
    </article>
  {% endfor %}
</section>

