---
layout: mylayout
title: Home
---

<div class="slogan">
    <p>
        <cite>We help startups to create their first machine learning product with state of the art research.</cite>
    </p>
    <p style="text-align: center">
        <br>
        <a href="/contact.html" type="button" class="btn btn-primary">
            Get in touch
        </a>
    </p>
</div>

## Who

Serendeepia is a group of experts in Artificial Intelligence and Deep Learning with passion for startups. We build custom solutions for startups with state of the art research and help them to develop their own capability to use Artificial Intelligence.

We are a very multidisciplinar team. We all have been doing research in Artificial Intelligence for more than 5 years in the academia. We went beyond the PhD and we also hold MBAs and degree in Psychology. We have been leading Machine Learning projects in big consultancy companies and also worked for several years for startups around the world (London, San Francisco, Madrid, ...).

## What


We basically do consulting+research+mvp

### Research

### MVP

### Rinse and repeat

### Deploy when ready

## Technology

<div class="container-fluid">
<div class="row"> 

<div class="logo_col center-block"> 
<img src="assets/logo_tensorflow.svg" alt="tensorflow" class="logo">
    
TensorFlow is one of the most used libraries used by researchers to create deep learning models. It was also designed by Google to be used for running models in production. Once the model has been trained we can deploy it to <a href="https://cloud.google.com/products/machine-learning/">Cloud Machine Learning</a>, an <a href="https://aws.amazon.com/">AWS</a> instance using <a href="https://www.tensorflow.org/serving/">TensorFlow Serving</a> or to your Android/iOs mobile app as an optimized graph.

</div> 

<div class="logo_col center-block"> 
<img src="assets/logo_github.svg" alt="cloud" class="logo">
    
We use common tools of fast paced startups. 
    
</div> 

<div class="logo_col"> 
<img alt="python" src="assets/logo_python.svg" class="logo"> 

bla bla bla

</div>

<div style="clear: both;"></div>
</div>
</div>

## Life after us

Once we select a project where we want to collaborate we do it until the end. We would continue helping your startup beyond the product. We can prepare of ad-hoc courses for your company in order to train your team to keep developing the product or help you to to hire the best professionals in Machine Learning.

## Latest news

{% assign sorted_posts = site.posts | sort: date | reverse %}
{% for post in sorted_posts %}

<h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
<p>{{ post.summary }}... <a href="{{ post.url }}">continue reading</a></p>

{% endfor %}
