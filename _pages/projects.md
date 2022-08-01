---
permalink: /projects/
layout: default
title: Projects
---

# Project's I've collaborated on

<ul>
  {% assign filtered_posts = site.posts | where_exp: 'post', "post.category == 'project'" %}
  {% for post in filtered_posts.posts %}
    <li>
      <a href="{{ post.url }}">
        {{ post.title }}
      </a>
      - <time datetime="{{ post.date | date: "%Y-%m-%d" }}">{{ post.date | date_to_long_string }}</time>
    </li>
  {% endfor %}
</ul>