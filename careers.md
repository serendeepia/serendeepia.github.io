---
layout: mylayout
title: Careers
navigation_weight: 6
---

<div class="slogan">
    <p>
        <cite>Be part of a team of world-class talent in Artificial Intelligence and enjoy every day learning and enhancing business through new innovations.</cite>
    </p>
</div>

<div class="careers-values">

	<h2>Our Core Values</h2>
	<p>We believe that a healthy culture is even more important than a smart culture. We live by our values to be a force for positive change in business.</p>

<div class="container-fluid-how">
<div class="row"> 

	<div class="how_col">
	<h3>Decisive Visionaries</h3>
	<p>We go beyond incremental thinking, push boundaries, and act quickl.</p>
	</div>
	
	<div class="how_col">
	<h3>Decisive Visionaries</h3>
	<p>We go beyond incremental thinking, push boundaries, and act quickl.</p>
	</div>

	<div class="how_col">
	<h3>Decisive Visionaries</h3>
	<p>We go beyond incremental thinking, push boundaries, and act quickl.</p>
	</div>
	
	<div class="how_col">
	<h3>Decisive Visionaries</h3>
	<p>We go beyond incremental thinking, push boundaries, and act quickl.</p>
	</div>

</div>
<div style="clear: both;"></div>
</div>	
</div>


## Job opportunities

{% assign counter = 0 %}
{% assign careers = site.careers | sort:"weight" %}
{% for position in careers %}
{% if position.open == true %}
{% assign counter=counter | plus:1 %}
<h3><a href="{{position.url}}">{{ position.title }}</a></h3>
{% assign num_words = position.content | number_of_words %}
{% if num_words > 120 %}
{% capture summary %}{{ position.content | truncatewords: 120 }} 
<em><a href="{{ position.url }}">Read more</a></em>{% endcapture %}
{{ summary | markdownify }} 
{% else %}
{{ position.content | markdownify }}
{% endif %}
{% endif %}
{% endfor %}


{% if counter == 0 %}
There are currently no open positions. However, we are always keen to meet energetic and talented professionals who would like to join our team. Please send your CV and project portfolio and tell us why you want to be part of Serendeepia:
<p style="text-align: center; margin-top: 40px;">
{% else %}
<h3>Other positions</h3>
<p>
We are always keen to meet energetic and talented professionals who would like to join our team. Please send your CV and project portfolio and tell us why you want to be part of Serendeepia:
</p>
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
