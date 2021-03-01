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
      {{ post.title }}<br>
      <p> {{ post.date | date: '%B %d, %Y' }}- {{ post.excerpt }}<a href="{{ post.url }}">more...</a></p>
    </li>
  {% endfor %}
</ul>
