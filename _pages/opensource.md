---
layout: page
permalink: /opensource/
title: open-source
description: I like open source research software.
nav: true
nav_order: 2
---

<!-- Refer to [https://saransh-cpp.github.io/open_source/](https://saransh-cpp.github.io/open_source/) for a longer version of this page! -->

Below is a list of projects I am involved with (as a maintainer, member, core-developer, contributor). I do NOT maintain all of the projects listed below. In fact, I am not even a "collaborator" for some of the projects mentioned here, but all of these projects have some significant contributions from me.

This list is somewhat incomplete. I contribute to a ton of Open Source Research Software, but these are the ones where you will usually find me.

---

## GitHub user

{% if site.data.repositories.github_users %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-center align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.html username=user %}
  {% endfor %}
</div>
{% endif %}

---

## Main research software

The software I am involved with as a maintainer, core-developer, core-contributor, etc.

{% if site.data.repositories.main_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.main_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

---

## Significant contributions

The software I have some good contributions in, in the form of code, docs, build and packaging infrastructure, etc.

"some good contributions": Contributions where I spent a signifcant amount of time researching, writing code, debugging, documenting, etc.

{% if site.data.repositories.significant_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.significant_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

---

## Personal projects

Personal projects that have some significant number stars or downloads (or took a lot of time for me to develop).

{% if site.data.repositories.project_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.project_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
