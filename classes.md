---
layout: page
title: Classes
permalink: /classes/
---
[cool item](https://www.wowhead.com/item=31015)

List of classes here!

<ul>
{% for class in site.data.classes %}
  <li>
    <a href="/classes/{{ class.slug }}">
      {{ class.name }}
    </a>
  </li>
{% endfor %}
</ul>

