---
layout: splash
author_profile: true
read_time: true
comments: true
share: true
related: true
---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a><br>
      {{ post.date | date: '%B %d, %Y' }}
    </li>
  {% endfor %}
</ul>
