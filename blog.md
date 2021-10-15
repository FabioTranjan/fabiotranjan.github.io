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
        <h5 class="date">{{ post.date | date: "%B, %Y" }}</h5>
      {% endif %}

      <li>
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        {{ post.excerpt }}
      </li>
    {% endfor %}
  </ul>
</div>