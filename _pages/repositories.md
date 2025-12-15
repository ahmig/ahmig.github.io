---
layout: page
permalink: /repositories/
title: repositories
description: 
nav: true
nav_order: 4
---

<div class="repositories">

{% if site.data.repositories.github_repos %}
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo platform="github" %}
  {% endfor %}
{% endif %}

{% if site.data.repositories.codeberg_repos %}
  {% for repo in site.data.repositories.codeberg_repos %}
    {% include repository/repo.liquid repository=repo platform="codeberg" %}
  {% endfor %}
{% endif %}

{% if site.data.repositories.tangled_repos %}
  {% for repo in site.data.repositories.tangled_repos %}
    {% include repository/repo.liquid repository=repo platform="tangled" %}
  {% endfor %}
{% endif %}

</div>
