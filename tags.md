---
layout: default
title: Tags
permalink: /tags/
---
<div>
{% for tag in site.tags %} 
	<a name="{{ tag[0] }}"></a><h3>{{ tag[0] }}({{ tag[1].size }})</h3>
	<ul class="cat-list">
	{% for post in tag[1] %}
		<li>{{ post.date | date:"%Y/%m/%d" }}<a href="{{ post.url }}">{{ post.title }}</a></li>
	{% endfor %}
	</ul>
{% endfor %}
</div>
