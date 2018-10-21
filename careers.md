---
layout: mylayout
title: Careers
navigation_weight: 6
---

## Working at Serendeepia 

Our mission is to enhance business through new innovations in Artificial Intelligence with the state of the art research. You will be part of a team of world-class talent in Machine Learning and Deep Learning. 

We are a remote team of talented enthusiastic and hard working innovators. You will have the chance to work with people all over the world from the place that best suits your needs and with flexible time.

Serendeepia is still a small company with a lot of challenges ahead. We aim to grow in a pace that allow us a good balance between personal and professional live. You will have a huge impact in future of the company. 

## Job opportunities

{% assign counter = 0 %}
{% for position in site.careers %}
{% if position.open == true %}
{% assign counter=counter | plus:1 %}
### [{{ position.title }}]({{position.url}})
{% assign num_words = position.content | number_of_words %}
{% if num_words > 100 %}
{{ position.content | truncatewords: 100 | markdownify}}  
_[Read more]({{ position.url }})_
{% else %}
{{ position.content | markdownify }}
{% endif %}
{% endif %}
{% endfor %}


{% if counter == 0 %}
There are currently no open positions. However, we are always keen to meet energetic and talented professionals who would like to join our team. Please send your CV or projects you have worked before and tell us why you want to be part of Serendeepia:
<p style="text-align: center; margin-top: 40px;">
{% else %}
### Other positions
We are always keen to meet energetic and talented professionals who would like to join our team. Please send your CV or projects you have worked before and tell us why you want to be part of Serendeepia:
<p style="text-align: center;">
{% endif %}
<span class="icon">
    <svg viewBox="0 4.801209 28.3499966 18.7475815">
    <path fill="#4a3a8b"
          d="M15.699194,17.7568531c-0.4572582,0.3048401-0.9145174,0.6096783-1.5241938,0.6096783 c-0.6096773,0-1.0669355-0.15242-1.5241938-0.6096783L0,6.7826605v16.1564522C0,23.2439518,0.3048387,23.54879,0.6096774,23.54879 h27.1306419c0.3048401,0,0.6096764-0.3048382,0.6096764-0.6096764V6.7826605L15.699194,17.7568531z"/>
    <path fill="#5945a6"
          d="M14.9370966,15.7754021L27.587904,4.801209H0.9145162l12.6508064,10.9741936 C13.870162,16.0802422,14.4798384,16.0802422,14.9370966,15.7754021z"/>
    </svg>
</span>
<a href="mailto:careers@serendeepia.com">careers@serendeepia.com</a>
</p>