---
layout: archive
title: "Projects and studies"
permalink: /projects/
author_profile: true
---

A series of projects and studies, Data architecture but also about Machine Learning, NLP, Computer Vision, Data Engineering, MLOps best practices.

<br>
<br>

<div class="grid__wrapper">
    {% for post in site.posts %}
        {% if post.categories contains 'projects' %}
            {% include archive-single.html type="grid" %}
        {% endif %}
    {% endfor %}
</div>
