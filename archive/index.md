---
layout:  page
title: 归档
description: 归档
---
人生，最宝贵的莫过于光阴。人生，最璀璨的莫过于事业。人生，最快乐的莫过于奋斗。

<ul class="archive">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="year">{{ y }}</li>
  {% endif %}
  <li class="item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>