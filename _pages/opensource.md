---
layout: page
permalink: /opensource/
title: open-source
description: i like open source research software
nav: true
nav_order: 3
---

I primarily contribute (or contributed) to (and in some cases maintain) **[PyBaMM ecosystem](https://github.com/pybamm-team/){:target="_blank"}**, **[Scikit-HEP/vector](https://github.com/scikit-hep/vector){:target="_blank"}** (and **[some surrounding packages](https://github.com/scikit-hep){:target="_blank"}**), **[Flux.jl](https://github.com/FluxML/Flux.jl){:target="_blank"}** (and **[some surrounding packages](https://github.com/FluxML){:target="_blank"}**), **[agda-stdlib](https://github.com/agda/agda-stdlib){:target="_blank}**, **[removestar](https://github.com/asmeurer/removestar){:target="_blank}**, and **[osl-incubator/scicookie](https://github.com/osl-incubator/scicookie){:target="_blank}**. My minor (or semi-major?) contributions are scattered all across GitHub (from the **[Scikit-HEP](https://github.com/scikit-hep/){:target="_blank"}** and **[Scientific Python](https://github.com/scientific-python/){:target="_blank"}** ecosystems to **[Zarr](https://github.com/zarr-developers/zarr-python){:target="_blank"}** and **[DeepXDE](https://github.com/lululxvi/deepxde){:target="_blank"}**). I also voluntarily supervise students for programs like **[GSoC](https://summerofcode.withgoogle.com)**.

Below is a list of projects I am involved with (as a maintainer, member, core-developer, contributor). I do NOT maintain all of the projects listed below. In fact, I am not even a "collaborator" for some of the projects mentioned here, but all of these projects have some significant contributions from me.

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

The software I am (or was) involved with as a maintainer, core developer, core contributor, or was funded to work on.

{% if site.data.repositories.main_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.main_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

---

## Significant contributions

Significant voluntary contributions or spin-off projects (was not directly funded to work on them but my work expanded and encompassed some of them).

Organization logos = contributions to the entire ecosystem.

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
    <a href="https://github.com/scikit-hep/" target="_blank"><img src="/assets/img/scikit-hep-logo.png" style="width: 170px"/></a>
    <a href="https://github.com/FluxML/" target="_blank"><img src="/assets/img/flux-logo.png" style="width: 300px"/></a>
    <a href="https://github.com/pybamm-team/" target="_blank"><img src="/assets/img/pybamm-logo.png" style="width: 300px"/></a>
</div>

{% if site.data.repositories.significant_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.significant_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}

---

## Small but nice contributions

Small contributions (not a spam spelling fix in README) that I did spend some time on.

{% if site.data.repositories.small_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-around align-items-center">
  {% for repo in site.data.repositories.small_repos %}
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
