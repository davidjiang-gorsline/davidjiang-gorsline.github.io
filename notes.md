---
layout: page
title: Notes
---

Short technical notes on evaluation, temporal alignment, retrieval/memory, and contextualised forecasting.

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>({{ post.date | date: site.date_format }})</small>
      {% if post.tags %}
        <div class="post-tags">{{ post.tags | join: ", " }}</div>
      {% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p>No notes yet. Check back soon.</p>
{% endif %}
