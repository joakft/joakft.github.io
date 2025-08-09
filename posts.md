---
layout: page
title: "All Posts"
permalink: /posts/
---

<ul>
  {% raw %}{% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <span> — {{ post.date | date: "%Y-%m-%d" }}</span>
    </li>
  {% endfor %}{% endraw %}
</ul>
