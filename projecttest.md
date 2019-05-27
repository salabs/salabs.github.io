---
layout: page
permalink: /projecttest/
title: test projects
description: Our Projects
---

<ul class="project-list">
{% for repository in site.github.public_repositories %}
  <div class="project-container">
    <div class="project-name">
        <a class="project-title" href="{{ repository.html_url }}">{{ repository.name }}</a>
    </div>
    <div class="project-description">
        {{ repository.description }}
    </div>
{% endfor %}
