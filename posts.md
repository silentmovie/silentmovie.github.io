---
layout: page
title: Posts
class: projects
permalink: /posts/
---

<!-- {:.hidden}
# Projects -->

<!-- {:.lead}
Here are some projects I have worked on for school, work, or fun. You can find the code for most of them on [GitHub](https://github.com/domoritz). -->

<div class="post-filters" role="group" aria-label="Filter posts by category">
  <button type="button" class="post-filter is-active" data-category="all" aria-pressed="true">All Posts</button>
  <button type="button" class="post-filter category-research" data-category="research" aria-pressed="false">Research</button>
  <button type="button" class="post-filter category-learning" data-category="learning" aria-pressed="false">Learning</button>
  <button type="button" class="post-filter category-mentor" data-category="mentor" aria-pressed="false">Mentor</button>
</div>

<div class="grid post-grid">
  {% for post in site.posts %}
    {% include post.html post=post %}
  {% endfor %}
</div>

<script>
  (function() {
    var filters = document.querySelectorAll(".post-filter");
    var posts = document.querySelectorAll(".post-card");

    filters.forEach(function(filter) {
      filter.addEventListener("click", function() {
        var category = filter.dataset.category;

        filters.forEach(function(button) {
          var isActive = button === filter;
          button.classList.toggle("is-active", isActive);
          button.setAttribute("aria-pressed", isActive ? "true" : "false");
        });

        posts.forEach(function(post) {
          var isVisible = category === "all" || post.dataset.category === category;
          post.classList.toggle("is-hidden", !isVisible);
        });
      });
    });
  })();
</script>
