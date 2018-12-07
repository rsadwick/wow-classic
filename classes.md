---
layout: page
title: Classes
permalink: /classes/
---

<ul>
{% for class in site.data.classes %}
  <li>
    <a href="/classes/{{ class.slug }}">
      {{ class.name }}
    </a>
  </li>
{% endfor %}
</ul>

