---
layout: page
permalink: /publications/
title: publications
years: [2020, 2016, 2015]
nav: true
---

<!-- Coming Soon... -->
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
