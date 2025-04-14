---
layout: default
title: ""
---
<style>
  .post-item {
    display: flex;
    align-items: center;
    margin-bottom: 2rem;
    gap: 1rem;
  }

  .post-thumbnail {
    width: 80px;
    height: 80px;
    object-fit: cover;
    border-radius: 6px;
  }

  .post-text {
    flex: 1;
  }

  .post-title {
    margin: 0;
    font-size: 1.25rem;
    font-weight: 600;
  }

  .post-title a {
    text-decoration: none;
    color: #0366d6;
  }

  .post-title a:hover {
    text-decoration: underline;
  }

  .post-date {
    font-size: 0.9rem;
    color: #666;
    margin-top: 0.25rem;
  }
</style>

<ul class="post-list">
  {% for post in site.posts %}
    <li style="margin-bottom: 2em;">
      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
      <small>{{ post.date | date: "%B %d, %Y" }}</small><br/>

      {% if post.thumbnail %}
        <img src="{{ site.baseurl }}/assets/images/{{ post.thumbnail }}" alt="Thumbnail" width="300" style="margin-top: 0.5em;" />
      {% endif %}
    </li>
  {% endfor %}
</ul>

