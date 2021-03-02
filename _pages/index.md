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
      <a href="{{ page.url }}">{{ page.summary }}</a><br>
    {% endif %}
  {% endif %}
{% endfor %}
</div>

