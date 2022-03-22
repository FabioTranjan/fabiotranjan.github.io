---
layout: default
title: About
permalink: /about/
---
<div class="hero-container">

  <div class="hero-content">

    {% if site.title != '' %}
    <h1 class="text-center">{{site.title}}</h1>
    {% endif %}

    <img src="https://avatars.githubusercontent.com/u/26252636?v=4" class="hero-image" />

    <div class="text-center">
     <p>I'm a <b>Software Engineer</b> from <i>Curitiba, Brazil</i>.</p>
     <p>I create <b>WebApps</b> and <b>SaaS</b> platforms using <span style="color: #cc373d;">RoR</span> and <span style="color: #61dafb">React</span>.</p>
     <p><b>Contact me</b> directly at <i>{{ site.email }}</i>.</p>
    </div>

    <div class="hero-buttons">

      {% if site.linkedin_username != '' %}
        <a href="https://linkedin.com/in/{{ site.linkedin_username }}"><button class="btn btn-default btn-lg"><i class="fa fa-linkedin fa-lg"></i>LinkedIn</button></a>
      {% endif %}

      {% if site.github_username != '' %}
        <a href="https://github.com/{{ site.github_username }}"><button class="btn btn-default btn-lg"><i class="fa fa-github fa-lg"></i>Github</button></a>
      {% endif %}

      {% if site.medium_username != '' %}
        <a href="https://medium.com/{{ site.medium_username }}"><button class="btn btn-default btn-lg"><i class="fa fa-medium fa-lg"></i>Medium</button></a>
      {% endif %}

    </div>

  </div>

</div>