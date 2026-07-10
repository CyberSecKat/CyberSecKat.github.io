---
layout: page
title: Projects
subtitle: Tools and research I've built, mostly around detection engineering.
permalink: /projects/
---

{% assign projects = site.projects | sort: 'date' | reverse %}
<div class="card-grid">
  {% for project in projects %}
  <a class="card" href="{{ project.url | relative_url }}">
    <span class="card__title">{{ project.title }}</span>
    <span class="card__summary">{{ project.summary }}</span>
    {% if project.tags and project.tags.size > 0 %}
    <ul class="card__tags">
      {% for tag in project.tags %}<li class="badge">{{ tag }}</li>{% endfor %}
    </ul>
    {% endif %}
  </a>
  {% endfor %}
</div>

<!-- To add a new project, drop a new markdown file in the _projects/
     folder — copy _projects/sysmon-parser.md as a starting template. -->
