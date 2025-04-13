---
layout: default
title: ""
---

<ul class="post-list">
  {% for post in site.posts %}
    <li style="margin-bottom: 2em;">
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <small>{{ post.date | date: "%B %d, %Y" }}</small><br/>

      {% if post.thumbnail %}
        <img src="{{ site.baseurl }}/assets/images/{{ post.thumbnail }}" alt="Thumbnail" width="300" style="margin-top: 0.5em;" />
      {% endif %}
    </li>
  {% endfor %}
</ul>

