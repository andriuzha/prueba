---
layout: default
title: Temas
---

<section class="posts">
	<h1>{{ page.title }}</h1>
	<h2>Escribo sobre:</h2> 
	<br>
<ul> 
 {% assign tags = site.tags | sort %}
{% for tag in tags %}
 <li><a href="/tag/{{ tag | first | slugify }}/">{{ tag[0] | replace:'-', ' ' }} ({{ tag | last | size }}){% unless forloop.last %}, {% endunless %}</a></li>
{% endfor %}
</ul>

</section>
