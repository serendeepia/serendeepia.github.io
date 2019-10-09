---
layout: mylayout
title: Products
navigation_weight: 5
---

{%- for product in site.products reversed -%}
{%- if product.date < site.time -%}
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
			{{ product.description }}
		</div>
	</div>
</div></div></div>
{%- endif -%}
{%- endfor -%}
