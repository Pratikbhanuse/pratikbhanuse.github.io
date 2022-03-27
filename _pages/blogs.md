---
layout: page
title: blogs
permalink: /blogs/
description: A growing collection of cool blog. Please leave your comments and feedback on the comment section n each blog.
nav: true
display_categories: [science, money, random]
horizontal: false
---

<!-- pages/blogs.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_blogs = site.blogs | where: "category", category -%}
  {%- assign sorted_blogs = categorized_blogs | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for blog in sorted_blogs -%}
      {% include blogs_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_blogs -%}
      {% include blogs.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display blogs without categories -->
  {%- assign sorted_blogs = site.blogs | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_blogs -%}
      {% include blogs_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_blogs -%}
      {% include blogs.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
