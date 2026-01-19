---
layout: page
permalink: /publications/
title: publications
description: publications, conference proceedings, selected reports, citeable scientific software, ...
years: [2022, 2023, 2024, 2025, 2026]
nav: true
nav_order: 4
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years reversed %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
