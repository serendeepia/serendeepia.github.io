---
layout: mylayout
title: Slides
#navigation_weight: 0
---
{%- for slides in site.slides reversed -%}
_{{slides.date | date_to_string }}_ - [{{slides.title}}]({{slides.url}})
{%- endfor -%}