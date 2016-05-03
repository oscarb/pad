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
