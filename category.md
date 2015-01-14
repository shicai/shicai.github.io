---
layout: default
title: Category
permalink: /category/
---
{% for category in site.categories %}
<h1>{{ category | first }}</h1>
<ul class="cat-list">
    {% for post in category.last %}
        <li>{{ post.date | date:"%Y/%m/%d"}}<a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
{% endfor %}