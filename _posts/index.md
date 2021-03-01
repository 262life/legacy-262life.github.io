---
layout: posts
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
      <p> {{ post.date | date: '%B %d, %Y' }}- {{ post.content | strip_html | truncatewords:75 }}<a href="{{ post.url }}"> - more...</a></p>
    </li>
  {% endfor %}
</ul>


{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% for post in posts %}
    {% include archive-single.html type=entries_layout %}
  {% endfor %}
</div>
