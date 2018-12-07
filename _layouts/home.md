---
layout: default
---

<div class="home">
<div><p>follow up</p></div>
  {%- if page.title -%}
    <h1 class="page-heading">{{ page.title }}</h1>
  {%- endif -%}

  {{ content }}


<div class="flex-grid">
    {% for guide in site.legendaries %}
        <div class="col">
            <h2>{{ guide.name }}</h2>
            <img src="{{guide.image}}">
            <p>{{guide.content}}</p>
            <a href="{{guide.slug}}">Read Now</a>
        </div>

    {% endfor %}
</div>

<div class="flex-grid-thirds">
  <div class="col">This little piggy went to market.</div>
  <div class="col">This little piggy stayed home.</div>
  <div class="col">This little piggy had roast beef.</div>
</div>


  {%- if site.posts.size > 0 -%}
    <h2 class="post-list-heading">{{ page.list_title | default: "Posts" }}</h2>
    <ul class="post-list">
      {%- for post in site.posts -%}
      <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
          <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
          </a>
        </h3>
        {%- if site.show_excerpts -%}
          {{ post.excerpt }}
        {%- endif -%}
      </li>
      {%- endfor -%}
    </ul>

    <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | relative_url }}">via RSS</a></p>
  {%- endif -%}

</div>
