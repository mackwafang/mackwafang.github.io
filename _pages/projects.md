---
layout: page
title: Projects
nav: true
permalink: /projects/
---

{% include project_header.html %}

{% for project in site.projects %}
<div class="project-item">
    <a href="{{ project.url }}">
        <div class="project-item-subcontainer">
            <p class="project-title" id="{{ project.title }}">{{ project.title }}</p>
            <p>{{ project.description }}</p>
        </div>
        <div class="project-item-images">
            <img src="{{ project.img }}">
        </div>
    </a>
</div>
{% endfor %}