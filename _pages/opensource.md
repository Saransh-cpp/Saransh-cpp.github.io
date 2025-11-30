---
layout: page
permalink: /opensource/
title: open-source
description: open-source scientific software, devtools, mobile applications, ...
nav: true
nav_order: 3
---

Below is a list of projects I am involved with (as a maintainer, member, core-developer, contributor). I do NOT maintain all of the projects listed below. In fact, I am not even a "collaborator" for some of the projects mentioned here, but all of these projects have some significant contributions from me. I also voluntarily supervise students for programs like **[Google Summer of Code](https://summerofcode.withgoogle.com)**.

Rest of my contributions on GitHub are scattered across Computational Mathematics, Machine Learning, and HPC (Scientific Python + PyData + NumFOCUS affiliated) libraries.

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

## Main scientific software

The software I am (or was) involved with as a maintainer, core developer, core contributor, or was funded to work on.

{% if site.data.repositories.main_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.main_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

<br>

and [several conda feedstocks](https://github.com/orgs/conda-forge/teams?query=@Saransh-cpp).

---

## Significant contributions

Significant voluntary contributions or spin-off projects (was not directly funded to work on them but my work expanded and encompassed some of them).

Organization logos = contributions to multiple libraries of the ecosystem.

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
    <a href="https://github.com/scikit-hep/" target="_blank"><img src="/assets/img/scikit-hep-logo.png" style="width: 170px"/></a>
    <a href="https://github.com/FluxML/" target="_blank"><img src="/assets/img/flux-logo.png" style="width: 200px"/></a>
    <a href="https://github.com/pybamm-team/" target="_blank"><img src="/assets/img/pybamm-logo.png" style="width: 300px"/></a>
    <a href="https://github.com/scientific-python/" target="_blank"><img src="/assets/img/scientific-python-logo.svg" style="width: 150px"/></a>
</div>

<!-- {% if site.data.repositories.significant_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.significant_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %} -->

---

<!-- ## Small but nice contributions

Small contributions (not a spam spelling fix in README) that I did spend some time on.

{% if site.data.repositories.small_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.small_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

---  -->

## Personal projects

Personal projects that have some significant number stars or downloads (or took a lot of time for me to develop).

{% if site.data.repositories.project_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.project_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

---

## Misc repositories

Talks, coding experiments, helper repositories that people might be interested in, ...

{% if site.data.repositories.main_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.talk_misc_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
