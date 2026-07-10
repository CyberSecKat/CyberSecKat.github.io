---
layout: page
title: Writings
subtitle: Essays and notes on detection engineering, security research, and whatever else I'm digging into.
permalink: /writings/
---

<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <a class="post-list__title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-list__date">{{ post.date | date: '%B %-d, %Y' }}</span>
    <p class="post-list__excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
  </li>
  {% else %}
  <li>No writings yet — check back soon.</li>
  {% endfor %}
</ul>

<!-- New posts go in _posts/ as YYYY-MM-DD-title.md — copy the seeded post
     as a starting template. -->
