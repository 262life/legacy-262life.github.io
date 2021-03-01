---
layout: single
author_profile: false
read_time: true
comments: false
share: true
related: true
---

{{ content }}

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
  {% include documents-collection.html collection=page.collection sort_by=page.sort_by sort_order=page.sort_order type=entries_layout %}
</div>
