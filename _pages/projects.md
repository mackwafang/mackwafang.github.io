---
layout: page
title: Projects
nav: true
permalink: /projects/
---

{% include project_header.html %}

{% for project in site.data.projects.projects %}
{% assign project_page = site.projects | where: "title", project.name | first %}
<div class="project-item">
    <a href="{{ project_page.url }}">
        <div class="project-item-subcontainer">
            <p class="project-title" id="{{ project.name }}">{{ project.name }}</p>
            <p>{{ project.description }}</p>
        </div>
        <div class="project-item-images">
            <img src="{{ project_page.img }}">
        </div>
    </a>
</div>
{% endfor %}