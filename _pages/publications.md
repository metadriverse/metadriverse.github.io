---
layout: page
permalink: /publications/
title: publications
description: publications by categories in reversed chronological order.
years: [2023,2022,2021]
nav: true
nav_order: 2
hide_from_nav: true
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}

</div>
