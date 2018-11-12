---
layout: mylayout
title: Success Stories
#navigation_weight: 0
---

# Success Stories

{% for story in site.success_stories reversed %}

## [{{ story.title }}]({{ story.url }})

{% if story.image %}
<img src="/assets/{{story.image}}" class="success_story_large"/>
{% endif %}
{% assign num_words = story.content | number_of_words %}
{% if num_words > 100 %}
{{ story.content | truncatewords: 100 | markdownify}}
_[Continue reading]({{ story.url }})_
{% else %}
{{ story.content | markdownify }}
{% endif %}

<div class='clear'></div>

{% endfor %}
