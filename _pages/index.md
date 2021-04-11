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
    {% if page.layout == 'single' and page.collection == 'examples' %}  
      <a href="{{ page.url }}" style="text-decoration: none;">{{ page.title }}</a><br>
    {% endif %}
  {% endif %}
{% endfor %}
</div>

