---
layout: home
title: Home
---

## Blog Posts

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <small>{{ post.date | date: "%B %d, %Y" }}</small><br/>
      <p>{{ post.excerpt }}</p>
    </li>
    <hr />
  {% endfor %}
</ul>
