---
layout: mylayout
title: Products
navigation_weight: 5
---

{% for product in site.products reversed %}

## [{{ product.title }}]({{ product.url }})

{% if product.image %}
<img src="/assets/{{product.image}}" class="success_product_large"/>
{% endif %}
{% assign num_words = product.content | number_of_words %}
{% if num_words > 100 %}
{{ product.content | truncatewords: 100 | markdownify}}
_[Continue reading]({{ product.url }})_
{% else %}
{{ product.content | markdownify }}
{% endif %}

<div class='clear'></div>

{% endfor %}
