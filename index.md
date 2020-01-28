---
layout: post/index
guid: index
---


<div>
  <p>&nbsp;</p>
  <h3>近期文章</h3>
  <ul class="listing">
  {% for post in site.posts limit: 10 %}
      <li><a href="{{ post.url }}">· {{ post.title }}</a></li>
  {% endfor %}
  </ul>
  <a href="/archive.html">❈ 所有文章</a>


  {% assign tags = site.posts.first.tags %}
  {% for post in site.posts offset:1 %}
    {% assign tags = tags | concat: post.tags %}
  {% endfor %}
  {% assign tags = tags | uniq %}

  {% if tags %}
    <p>&nbsp;</p>
    <h3>标签</h3>
    <span class="tags">
      {% for tag in tags %}
      #<a href="/tags.html#{{ tag }}" title="{{ tag }}">{{ tag }}</a>&nbsp;
      {% endfor %}
    </span>
  {% endif %}

</div>
