---
layout: page
permalink: /articles/
title: articles
description: from my 2024 new years resolutions - to write at least one article per quarter
nav: true
nav_order: 3
---

this is a hobby

<div class="articles">
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.articles | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
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
</div>