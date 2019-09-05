---
layout: news
title: News
#navigation_weight: 0
---
{%- for post in site.posts -%}

## [{{ post.title }}]({{ post.url }})
<p class="date"><em>{{post.date | date_to_string }}</em></p>

{%- assign num_words = post.content | number_of_words -%}
{%- if num_words > 100 -%}
{{ post.content | truncatewords: 100 | markdownify}}
_[Continue reading]({{ post.url }})_
{%- else -%}
{{ post.content | markdownify }}
{%- endif -%}

{%- endfor -%}