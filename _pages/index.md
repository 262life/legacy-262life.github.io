---
layout: single
author_profile: true
read_time: false
comments: false
share: false
related: false
---

<div class="entries-{{ entries_layout }}">
{% for page in site.pages %}
  {% if page.layout != 'post' %}  
    {% if page.layout != 'collection' %}  
      <h3><a href="{{ page.url }}">{{ page.title }}</a></h3>
    {% endif %}
  {% endif %}
{% endfor %}
</div>

