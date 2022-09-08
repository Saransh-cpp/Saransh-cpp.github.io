---
layout: page
permalink: /repositories/
title: repositories
description: Again, I like open source research software.
nav: true
nav_order: 2
---

Refer to [https://saransh-cpp.github.io/open_source/](https://saransh-cpp.github.io/open_source/) for a longer version of this page!

Below is a list of projects I am involved with. I am not a maintainer or even a collaborator of some of the projects listed here, but these projects have some significant contributions from me!

This list is somewhat incomplete. I contribute to a ton of OSS research software, but these are the ones where I spend most of the time.

## GitHub users

{% if site.data.repositories.github_users %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-center align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.html username=user %}
  {% endfor %}
</div>
{% endif %}

---

## GitHub Repositories

{% if site.data.repositories.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
