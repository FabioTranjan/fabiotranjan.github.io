---
layout: inner
title: Blog
permalink: /blog/
---
<div class="blog">
  <ul class="posts">
    {% for post in site.posts %}
      {% capture day %}{{ post.date | date: '%m%Y' }}{% endcapture %}
      {% capture nextday %}{{ post.next.date | date: '%m%Y' }}{% endcapture %}

      {% if day != nextday %}
        <h2 class="date">{{ post.date | date: "%B, %Y" }}</h2>
      {% endif %}

      <li>
        <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
        {{ post.excerpt }}
        <div class="mini-break"></div>
      </li>
    {% endfor %}
  </ul>
</div>