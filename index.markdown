---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h2>Projects</h2>

{% for project in site.data.projects.projects %}
{% assign project_page = site.projects | where: "title", project.name | first %}

<div class="project-item">
    <a class="project-button-source" href="//github.com/{{ site.github_username }}/{{ project.name }}">
        <img src="https://github-stats-extended.vercel.app/api/pin?username={{ site.github_username }}&repo={{ project.name }}">
    </a>
</div>
{% endfor %}


<h2>Publications</h2>