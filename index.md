---
layout: default
title: oscarb pad
---

# pad
Guides, resources, notes, docs and knowledge for everything Oscar 

{{ site.baseurl }} {{ site.url }}

<!-- Create empty arrays -->
{% assign tags = '' | split: ',' %}
{% assign unique_tags = '' | split: ',' %}

<!-- Map and flatten -->
{% assign docs_tags =  site.docs | map: 'tags' | join: ',' | join: ',' | split: ',' %}


<!-- Push to tags -->
{% for tag in docs_tags '%}
  {% assign tags = tags | push: tag %}
{% endfor %}


<!-- Uniq -->
{% assign tags = tags | sort %}
{% for tag in tags %}

<!-- If not equal to previous then it must be unique as sorted -->
{% unless tag == previous %}

<!-- Push to unique_tags -->
{% assign unique_tags = unique_tags | push: tag %}
{% endunless %}

{% assign previous = tag %}
{% endfor %}

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
