---
layout: archive
title: "Portfolio and projects"
permalink: /projects/
author_profile: true
---

A series of projects that i have realized - mostly about Machine Learning, NLP, Computer Vision, Data Engineering, MLOps best practices.
Push in progress... :smile:

<br>
<br>

# Computer Vision

<div class="grid__wrapper">
    {% for post in site.posts %}
        {% if post.categories contains 'Computer_vision' %}
            {% include archive-single.html type="grid" %}
        {% endif %}
    {% endfor %}
</div>

# Forecasting

<div class="grid__wrapper">
    {% for post in site.posts %}
        {% if post.categories contains 'Forecasting' %}
            {% include archive-single.html type="grid" %}
        {% endif %}
    {% endfor %}
</div>

# NLP

<div class="grid__wrapper">
    {% for post in site.posts %}
        {% if post.categories contains 'NLP' %}
            {% include archive-single.html type="grid" %}
        {% endif %}
    {% endfor %}
</div>


# MLOps / Data Engineering

<div class="grid__wrapper">
    {% for post in site.posts %}
        {% if post.categories contains 'MLOps' %}
            {% include archive-single.html type="grid" %}
        {% endif %}
    {% endfor %}
</div>