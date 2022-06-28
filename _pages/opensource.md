---
layout: page
title: open source
permalink: /open_source/
description: I like open source research software.
nav: true
nav_order: 1
# display_categories: [maintainer, core-developer, contibutor]
horizontal: false
---

My contributions are scattered all over GitHub. I usually contribute to research software written in Python and Julia, but I am exploring the C/C++ side as well. Here are some of my significant contributions.

## Maintainer

---

### [PyBaMM (Python Battery Mathematical Modeling)](https://github.com/pybamm-team/PyBaMM)

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">PyBaMM (Python Battery Mathematical Modelling) solves physics-based electrochemical DAE models by using state-of-the-art automatic differentiation and numerical solvers. <br> <br>
    I started working with PyBaMM's team during my time as a Google Summer of Code developer. The team was very welcoming and inclusive; hence, I decided to continue working with them after the program ended! I am not very well versed in the mathematical modeling of batteries; therefore my main contributions revolve around bug fixes, adding utility features, and maintaining the infrastructure. <br> <br>
    Over the past few months, my contributions have mostly shifted towards the packaging, infrastructure, and CI/CD pipeline side of PyBaMM. I do wish to continue contributing new features to the PyBaMM repository.
  </td>
    <td><img style="float: right; width:100%" src="../assets/img/pybamm-logo.png"></td>
    <td></td>
  </tr>
</table>


### [BattBot](https://github.com/pybamm-team/BattBot)

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">An automated Twitter Bot that Tweets random Battery Simulations and replies to requested Battery Simulations. <br> <br>
    BattBot was my Google Summer of Code project. The project started as a stand-alone repository and is still running on the same good old infrastructure! The bot's codebase is well documented but it can be a bit confusing sometimes. The bot is partially deployed on Heroku and partially on GitHub Actions (yes, confusing). You can find it tweeting battery simulations on Twitter twice a day! <br> <br>
    Everything in the bot was built from scratch by me, under the guidance of my mentors. I still maintain the bot, which includes fixing bugs, adding features, and fixing documentation.
  </td>
    <td><img style="float: right; width:100%" src="../assets/img/battbot-logo.jpeg"></td>
    <td></td>
  </tr>
</table>

### [Vector](https://github.com/scikit-hep/vector)

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">Vector is a Python 3.6+ library for 2D, 3D, and Lorentz vectors, especially arrays of vectors, to solve common physics problems in a NumPy-like way. <br> <br>
    In-progress.

  </td>
    <td><img style="float: right; width:100%" src="../assets/img/vector-logo.png"></td>
    <td></td>
  </tr>
</table>

## Core-contributor

---

### [liionpack](https://github.com/pybamm-team/liionpack)

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">liionpack takes a 1D PyBaMM model and makes it into a pack. You can either specify the configuration e.g. 16 cells in parallel and 2 in series (16p2s) or load a netlist. <br> <br>
    Before liionpack's initial release, I worked extensively on its documentation, infrastructure, and CI/CD pipeline. As a result, Liionpack's paper, published in the Journal of Open Source Software, now lists me as a co-author!!<br> <br>
    I still look after liionpack's documentation, infrastructure, and CI/CD pipeline!

  </td>
    <td><img style="float: right; width:100%" src="../assets/img/liionpack-logo.png"></td>
    <td></td>
  </tr>
</table>

### [FluxML](https://github.com/FluxML/Flux.jl)

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">Flux is an elegant approach to machine learning. It's a 100% pure-Julia stack, and provides lightweight abstractions on top of Julia's native GPU and AD support. Flux makes the easy things easy while remaining fully hackable. <br> <br>
    In-progress.

  </td>
    <td><img style="float: right; width:100%" src="../assets/img/flux-logo.png"></td>
    <td></td>
  </tr>
</table>

<!-- ## Contributor

---

### [FluxML](https://github.com/FluxML/Flux.jl)

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">Flux is an elegant approach to machine learning. It's a 100% pure-Julia stack, and provides lightweight abstractions on top of Julia's native GPU and AD support. Flux makes the easy things easy while remaining fully hackable. <br> <br>
    In-progress.

  </td>
    <td><img style="float: right; width:100%" src="../assets/img/flux-logo.png"></td>
    <td></td>
  </tr>
</table> -->


<!-- pages/projects.md -->
<!-- <div class="projects">
{%- if site.enable_project_categories and page.display_categories %} -->
  <!-- Display categorized projects -->
  <!-- {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %} -->
  <!-- Generate cards for each project -->
  <!-- {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%} -->
<!-- Display projects without categories -->
  <!-- {%- assign sorted_projects = site.projects | sort: "importance" -%} -->
  <!-- Generate cards for each project -->
  <!-- {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div> -->
