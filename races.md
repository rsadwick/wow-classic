---
layout: page
title: Races
permalink: /races/
---

## Alliance
{% assign races = site.data.races | where:"isAlliance", true %}
{% for race in races %}  
[{{race.name}}]({{race.slug}})
{% endfor %}

## Horde
{% assign races = site.data.races | where:"isHorde", true %}
{% for race in races %}  
[{{race.name}}]({{race.slug}})
{% endfor %}


