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

<!-- Create empty arrays -->
{% assign tags = '' | split: ',' %}
{% assign unique_tags = '' | split: ',' %}

<!-- Map and flatten -->
{% assign docs_tags =  site.docs | map: 'tags' | join: ',' | join: ',' | split: ',' %}
{{ docs_tags }}<br/>

<!-- Push to tags -->
{% for tag in docs_tags '%}
  {% assign tags = tags | push: tag %}
{% endfor %}
{{ tags }}<br/>

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
{{ unique_tags }}<br/>
{{ tags }}<br/>

{% for tag in tags '%}
  {{ tag }}<br/>
{% endfor %}
