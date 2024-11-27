---
layout: page
permalink: /publications/
title: PUBLICATIONS
nav: true
nav_order: 4
years: [2024, 2023,2022,2021]
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>