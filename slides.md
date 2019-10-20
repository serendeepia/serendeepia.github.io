---
layout: mylayout
title: Slides
#navigation_weight: 0
---
{%- for slide in site.slides reversed -%}
{%- if slide.permalink -%}
[{{slide.title}}]({{slide.url}})
 <br>
{%- endif -%}
{%- endfor -%}
<br>

{%- for slide in site.slides reversed -%}
{%- unless slide.permalink -%}
_{{slide.date | date_to_string }}_ - [{{slide.title}}]({{slide.url}})
 <br>
{%- endunless -%}
{%- endfor -%}