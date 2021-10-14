---
layout: inner
title: Blog
permalink: /blog/
---
<div class="blog">
  <h1>Posts</h1>
  
  <ul class="posts">
    {% for post in site.posts %}
      <li>
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        {{ post.excerpt }}
      </li>
    {% endfor %}
  </ul>
</div>