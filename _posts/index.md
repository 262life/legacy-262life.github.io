---
layout: posts
read_time: true
comments: true
share: true
related: true
---

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% for post in posts %}
    {% if post.layout == 'medium' %}
        <li><a href="{{ post.medium_url }}"><em>{{ post.date | date_to_string }} - {{ post.title }}</em></a></li>
    {% else %}
        {% include archive-single.html type=entries_layout %}
    {% endif %}
  {% endfor %}
</div>
