---
layout: default
title: oscarb pad
---

# pad
Guides, resources, notes, docs and knowledge for everything Oscar 

{{ site.docs | group_by: "tags" }} Hello?

<ul>
{% for doc in site.docs %}
<li><a href=".{{ doc.url }}">{{ doc.title }}</a> {{ doc.categories }} {{ doc.tags }}
</li>
{% endfor %}
</ul>
