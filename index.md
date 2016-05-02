---
layout: default
title: oscarb pad
---

# pad
Guides, resources, notes, docs and knowledge for everything Oscar

<ul>
{% for page in site.pages %}
<li><a href="{{ page.url }}">{{ page.title }}</a> {{ page.categories }} {{ page.tags }}
</li>
{% endfor %}
</ul>
