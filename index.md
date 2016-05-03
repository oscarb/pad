---
layout: default
title: oscarb pad
---

# pad
Guides, resources, notes, docs and knowledge for everything Oscar 

{% include tags-docs.md %}

{% for t in unique_tags %}
<h2>{{ t }}</h2>

<ul>
{% for doc in site.docs %}
{% if doc.tags contains t %}
<li><a href=".{{ doc.url }}">{{ doc.title }}</a></li>
{% endif %}
{% endfor %}
</ul>

{% endfor %}

{% gist oscarb/9227cca2064b38c697fc362e6bc61a0c %}
