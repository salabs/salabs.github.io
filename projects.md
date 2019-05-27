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
{% for repository in site.github.public_repositories %}
  {% if repository.name contains 'github.io' %}
    {% continue  %}
  {% endif %}
  <div class="project-container">
    <div class="project-name">
        <a class="project-title" href="{{ repository.html_url }}">{{ repository.name }}</a>
    </div>
    <div class="project-description">
        {{ repository.description }}
    </div>
{% endfor %}
