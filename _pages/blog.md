---
layout: page
permalink: /blog/
title: Notizblog
---

Manche dieser Beiträge sind extrem kurz und dienen mir zur Erinnerung und / oder späteren Referenzierung. Andere widerum sind sehr lang und sollen ein konkretes Thema gezielt transportieren. 

<ul>
{% for post in site.posts %}
<li>
    <a href="{{ post.url }}">{{ post.title }}</a>
</li>
{% endfor %}
</ul>