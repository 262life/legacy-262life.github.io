---
layout: single
author_profile: true
read_time: false
comments: false
share: true
related: false
---


<div class="entries-{{ entries_layout }}">
{% for page in site.pages %}
  {% if page.style != 'posts' %}  
    <h3><a href="{{ page.url }}">{{ page.title }}</a></h3>
  {% endif %}
{% endfor %}
</div>




<div class="entries-{{ entries_layout }}">
{% for page in site.pages %}
    <h3><a href="{{ page.url }}">{{ page.title }}</a></h3>
{% endfor %}
</div>
