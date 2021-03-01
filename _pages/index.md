---
layout: single
author_profile: true
read_time: true
comments: false
share: true
related: true
---

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% for page in pages.pages %}
    {% include archive-single.html type=entries_layout %}
  {% endfor %}
</div>


<div class="entries-{{ entries_layout }}">
{% for page in site.pages %}
  <h3><a href="{{ page.url }}">{{ page.title }}</a></h3>
  <p>{{ page.content }}</p>
{% endfor %}
</div>
