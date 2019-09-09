---
layout: mylayout
title: Products
navigation_weight: 5
---

{%- for product in site.products reversed -%}
{%- capture content_text_pos -%}{%- cycle 'right', 'left' -%}{%- endcapture -%}
{%- capture content_reverse -%}{%- cycle '', 'content-row-reverse' -%}{%- endcapture -%}

<div class="content-wrapper">
<div class="wrapper">
<div class="content-block {{ content_reverse }}">
	<div class="content-block-section">
		<img class="success_story_small" src="/assets/{{product.image}}"/>
	</div>
	<div class="content-block-section ">
		<h3><a href="{{ product.url }}">{{ product.title }}</a></h3>
		<div class="content-block-text-{{ content_text_pos }} content-light ">
			{%- assign num_words = product.content | number_of_words -%}
			{%- if num_words > 100 -%}
				{%- capture summary -%}{{ product.content | truncatewords: 100 }}
				    <em><a href="{{ product.url }}">Discover</a></em>
				{%- endcapture -%}
				{{ summary | markdownify }}
			{%- else -%}
				{{ product.content | markdownify }}
			{%- endif -%}
		</div>
	</div>
</div></div></div>
{%- endfor -%}
