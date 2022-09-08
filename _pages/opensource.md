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

Refer to [https://saransh-cpp.github.io/repositories/](https://saransh-cpp.github.io/repositories/) for a shorter version of this page!

My contributions are scattered all over GitHub. I usually contribute to research software written in Python and Julia, but I am exploring the C/C++ side as well. Here are some of my significant contributions.

## Maintainer and core-developer

---

### [PyBaMM (Python Battery Mathematical Modeling)](https://github.com/pybamm-team/PyBaMM){:target="_blank"}

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

<!-- <div class="flex-row" style="display: flex; flex-direction: row; justify-content: space-between;">
<img style="width:25%" src="../assets/img/pybamm-logo.png">
<a style="width:25%" href="https://github.com/pybamm-team/PyBaMM"><img align="center" src="https://github-readme-stats.vercel.app/api/pin/?username=pybamm-team&repo=PyBaMM" /></a>
</div> -->

<!-- <br> <br> -->

<!-- PyBaMM (Python Battery Mathematical Modelling) solves physics-based electrochemical DAE models by using state-of-the-art automatic differentiation and numerical solvers. <br> <br>
I started working with PyBaMM's team during my time as a Google Summer of Code developer. The team was very welcoming and inclusive; hence, I decided to continue working with them after the program ended! I am not very well versed in the mathematical modeling of batteries; therefore my main contributions revolve around bug fixes, adding utility features, and maintaining the infrastructure. <br> <br>
Over the past few months, my contributions have mostly shifted towards the packaging, infrastructure, and CI/CD pipeline side of PyBaMM. I do wish to continue contributing new features to the PyBaMM repository. -->


### [liionpack](https://github.com/pybamm-team/liionpack){:target="_blank"}

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

### [BattBot](https://github.com/pybamm-team/BattBot){:target="_blank"}

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

<!-- ## Collaborater and core-contributor

--- -->

### [Vector](https://github.com/scikit-hep/vector){:target="_blank"}

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">Vector is a Python 3.7+ library for 2D, 3D, and Lorentz vectors, especially arrays of vectors, to solve common physics problems in a NumPy-like way. <br> <br>
    My IRIS-HEP fellowship work was focused on developing vector. I Prepared Vector for the v0.9.0, v0.10.0, and v1.0.0 (first major release) releases by developing new public APIs, fixing bugs, writing documentation, and building new infrastructure. This work was carried out under the supervision of CERN and Princeton researchers. <br> <br> 
    The major release is currently being used by researchers at CERN, ATLAS, CMS, and Princeton University to construct 4D jagged (awkward) vectors and perform Just-In-Time compiled vector operations in Python. <br> <br>
    I still contribute to vector and the HEP ecosystem (scikit-hep/awkward, scikit-hep/cookie, scikit-hep/scikit-hep.github.io, ...) in various forms!

  </td>
    <td><img style="float: right; width:100%" src="../assets/img/vector-logo.png"></td>
    <td></td>
  </tr>
</table>

## Core-contributor

---

### [FluxML](https://github.com/FluxML/){:target="_blank"}

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">Flux is an elegant approach to machine learning. It's a 100% pure-Julia stack, and provides lightweight abstractions on top of Julia's native GPU and AD support. Flux makes the easy things easy while remaining fully hackable. <br> <br>
    I worked on the FluxML ecosystem in the summer of 2022. I was primarily hired as a technical writer under Julia Season of Contributions, but I soon started contributing to the code as well as the infrastructure of the ecosystem. <br> <br>
    My work included fixing bugs and developing the infrastructure of prominent Julia ML libraries such as Flux.jl, NNlib.jl (Neural Network primitives), Metalhead.jl (Computer vision models), and Functors.jl. I also spent a considerable amount of time writing original Machine Learning/Deep Learning tutorials, documentation, and API references for FluxML’s ecosystem. <br> <br>
    I still contribute to the ecosystem! You can find me reviewing PRs, fixing docs, debugging bugs, and improving the infrastructure!

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
