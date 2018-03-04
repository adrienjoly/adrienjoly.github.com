---
layout: projects
title: Projects
---

## Recent projects

<ul class="items">

  <!-- listed from _data/projects.yaml -->

  {% for proj in site.data.projects %}
    <li class="project">
      <a class="screenshot" href="{{ proj.url }}" target="_blank">
        <img src="{{ proj.img }}" alt="{{ proj.title }} screenshot">
      </a>
      <h2><a href="{{ proj.url }}" target="_blank">{{ proj.title }}</a><small>{{ proj.date }}</small></h2>
      <p>{{ proj.desc | markdownify }}</p>
      {% for link in proj.links %}
        <p><a href="{{ link.url }}" target="_blank">
          <span class="{{ link.className }}">{{ link.title }}</span></a>
        </p>
      {% endfor %}
    </li>
  {% endfor %}

</ul>