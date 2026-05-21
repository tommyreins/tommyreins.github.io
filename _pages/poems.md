---
layout: page
permalink: /poems/
title: poems
description: hopefully they rhyme
nav: true
nav_order: 4
horizontal: false
---

this is a hobby

---

<div class="projects">
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.liquid %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {%- for project in sorted_projects -%}
      {% include projects.liquid %}
    {%- endfor %}
    </div>
  </div>
  {%- endif -%}
</div>
