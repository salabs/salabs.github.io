---
layout: page
permalink: /projects/
title: projects
description: Our Projects
---

<ul class="project-list">
{% for project in site.projects reversed %}
  <div class="project-container">
    <div class="project-name">
        <a class="project-title" href="{{ project.github }}">{{ project.title }}</a>
    </div>
    <div class="project-description">
        {{ project.description }}
    </div>
  </div>
{% endfor %}
