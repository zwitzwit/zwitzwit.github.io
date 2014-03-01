---
layout:  page
title: 文章归档
stitle: Archive
---
人生，最宝贵的莫过于光阴。人生，最璀璨的莫过于事业。人生，最快乐的莫过于奋斗。

<ul class="gamelists">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="year">{{ y }}</li>
  {% endif %}
    <li>
        <h4><a href="{{ post.url }}">{{ post.title }}</a></h4><span>{{ post.date | date:"%Y-%m-%d"}} 发布 | 分类：{{ post.category }}</span>
        <p>{{ post.description }}</p>
    </li>
{% endfor %}
</ul>