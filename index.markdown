---
layout: default
title: Home
---

{% for post in site.posts %}
<div class="post-block">

  <h1 class="post-title">
    <a href="{{ post.url }}">{{ post.title }}</a>
  </h1>

  <div class="post-meta">
    {{ post.date | date: "%B %d, %Y" }}
  </div>

  {% if post.excerpt %}
  <div class="post-excerpt">
    {{ post.excerpt }}
  </div>
  {% endif %}

</div>
{% endfor %}