---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h2>Projects</h2>

{% include project_header.html %}

{% for project in site.data.projects.projects %}
{% assign project_page = site.projects | where: "title", project.name | first %}
<div class="project-item">
    <div class="project-item-subcontainer">
        <a class="project-title" id="{{ project.name }}" href="{{ project_page.url }}">{{ project.name }}</a>
        <p>{{ project.description }}</p>
        <a class="project-button-source" href="//github.com/{{ site.github_username }}/{{ project.name }}">
            <img src="https://github-stats-extended.vercel.app/api/pin?username={{ site.github_username }}&repo={{ project.name }}">
        </a>
    </div>
    <div class="project-item-images">
        <img src="{{ project_page.img }}">
    </div>
</div>
{% endfor %}


<h2>Publications</h2>
<ul>
    <li>Petty, T., Vu, T., Zhao, X., Hirsh, R. A., Murray, G., Haas, F. M., & Xue, W. (2020). Evaluating Deep Learning Algorithms for Real-Time Arrhythmia Detection. 2020 IEEE/ACM International Conference on Big Data Computing, Applications and Technologies (BDCAT), 19–26. doi:10.1109/BDCAT50828.2020.00022</li>
    <li>Vu, T. (2021). Real-Time Arrhythmia Detection using Convolutional Neural Network. 78. https://doi.org/10.7273/000001873</li>
</ul>