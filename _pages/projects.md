---
layout: page
title: projects
permalink: /projects/
description: Fun experiments. (page under construction)
nav: true
nav_order: 1
# display_categories: [work, fun]
horizontal: false
---

### ChaoticEncryption.jl 
Julia Package, ODEs, Pseudo-Random Number Generators, Encryption-Decryption

---

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">Encrypt and decrypt image files using Pseudo-Random Number Generators and various encryption techniques! ChaoticEncryption.jl is a Julia package that comes loaded with Pseudo-Random Number Generators and various encryption techniques, which can be used to encrypt and decrypt any image file. The package is under active development, but the existing API is stable and might not change significantly. <br> <br>
    The algorithms, with the help of Julia's optimisation techniques and multiple dispatch, have been vectorised to run 5-10 times faster than ordinary nested-for implementations. The package can be installed using Julia's package manager Pkg.jl - <br>
    <code> julia> ] add ChaoticEncryption </code> <br> <br>
    The complete infrastructure, documentation, code, and CI/CD pipeline of the package have been built/written by me. The package has been starred 23 times on <a href="https://github.com/Saransh-cpp/ChaoticEncryption.jl">GitHub</a> and is available on JuliaHub <a href="https://juliahub.com/ui/Packages/ChaoticEncryption/dtMkN">here</a> (11 downloads). The documentation for the package is hosted by GitHub Pages and is available <a href="https://saransh-cpp.github.io/ChaoticEncryption.jl/stable">here</a> (stable/latest tagged version).
  </td>
    <td><img style="float: right; width:100%" src="../assets/img/chaoticencryption-logo.png"></td>
    <td></td>
  </tr>
</table>

<br>

### SceneNet
Transfer Learning, VGG19, Python, Flutter, Dart, FastAPI, Heroku

---

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">User-facing scenery detection using transfer learning. <br> <br>
  </td>
    <td><img style="float: right; width:100%" src="" alt="Under construction"></td>
    <td></td>
  </tr>
</table>

<br>

### PopItUp
Android, Kotlin, Firebase, Firestore, Google Sceneform SDK, Google ARCore SDK

---

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">An Augmented Reality shooting game, built with Google ARCore SDK and Google Sceneform SDK. <br> <br>
  </td>
    <td><img style="float: right; width:100%" src="../assets/img/popitup-logo-not-transparent.png"></td>
    <td></td>
  </tr>
</table>

<br>

### MemeTastic
Flutter, Dart, NodeJS, Elasticsearch, Kibana, CI/CD, Google Cloud, Reddit API, Ngram Analyser

---

<table>
  <colgroup>
       <col span="1" style="width: 65%;">
       <col span="1" style="width: 35%;">
  </colgroup>
  <tr>
    <td style="text-align:justify; padding-bottom: 20px; padding-right: 30px">Summon and search Reddit memes from anywhere and at anytime!<br> <br>
  </td>
    <td><img style="float: right; width:100%" src="" alt="Under construction"></td>
    <td></td>
  </tr>
</table>

<br>


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
