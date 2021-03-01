---
layout: single
author_profile: true
read_time: true
comments: false
share: true
related: true
---


<div class="entries-{{ entries_layout }}">
{% for page in site.pages %}
  <h3><a href="{{ page.url }}">{{ page.title }}</a></h3>
  <p>{{ xpage.content }}</p>
{% endfor %}
</div>
