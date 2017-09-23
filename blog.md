---
layout: mylayout
title: News
---

{% assign sorted_posts = site.posts | sort: date | reverse %}
{% for post in sorted_posts %}

## [{{ post.title }}]({{ post.url }})

{{ post.summary }}... <a href="{{ post.url }}">continue reading</a>

{% endfor %}