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

<div class="grid__wrapper">
    {% for post in site.posts %}
        {% if post.categories contains 'projects' %}
            {% include archive-single.html type="grid" %}
        {% endif %}
    {% endfor %}
</div>
