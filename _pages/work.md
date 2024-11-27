---
layout: page
title: XRWORK
permalink: /xrwork/
nav: true
nav_order: 2
display_categories: [Immersive Visualisation, Spatial Mapping]
---
<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
    <h2 class="category">{{ category }}</h2>
    {%- assign categorized_projects = site.projects | where: "category", category -%}
    {%- assign sorted_projects = categorized_projects | sort: "importance" %}
    <!-- Generate cards for each project -->
    <div class="row">
      {%- for project in sorted_projects %}
        <div class="col-12" style="width: 50vw; margin-bottom: 20px;">
          {% include projects.html %}
        </div>
      {%- endfor %}
    </div>
  {% endfor %}
{%- else -%}
  <!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  <div class="row">
    {%- for project in sorted_projects %}
      <div class="col-12" style="width: 50vw; margin-bottom: 20px;">
        {% include projects.html %}
      </div>
    {%- endfor %}
  </div>
{%- endif -%}
</div>