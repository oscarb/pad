---
layout: default
title: oscarb pad
---

# pad
Guides, resources, notes, docs and knowledge for everything Oscar

<ul>
{% for page in site.category.guides %}
<li><a href="{{ page.url }}">{{ page.title }}</a>
</li>
{% endfor %}
</ul>
