---
layout: page
title: ARTWORK
permalink: /artwork/
nav: true
nav_order: 3
years: [2024]
---
<!-- pages/projects.md -->
<div class="arts">
{%- if site.enable_art_categories and page.display_categories %}
  <!-- Display art pieces -->
  {%- for category in page.display_categories %}
    <h2 class="category">{{ category }}</h2>
    {%- assign categorized_arts = site.arts | where: "category", category -%}
    {%- assign sorted_arts = categorized_arts | sort: "importance" %}
    <!-- Generate cards for each project -->
    <div class="row">
      {%- for art in sorted_arts %}
        <div class="col-12" style="width: 50vw; margin-bottom: 20px;">
          {% include arts.html %}
        </div>
      {%- endfor %}
   </div>
  {% endfor %}
{%- else -%}
  <!-- Display art pieces -->
  {%- assign sorted_arts = site.arts | sort: "importance" -%}
  <!-- Generate cards for each project -->
  <div class="row">
    {%- for art in sorted_arts %}
      <div class="col-12" style="width: 50vw; margin-bottom: 20px;">
        {% include arts.html %}
      </div>
    {%- endfor %}
  </div>
{%- endif -%}
</div>


