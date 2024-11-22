---
layout: about
title: Projects
permalink: /
subtitle: AI Research for Generalizable and Interpretable Machine Autonomy
display_categories:
news: true  # includes a list of news items
latest_posts: true  # includes a list of the newest posts
selected_papers: true # includes a list of papers marked as "selected={true}"
nav_order: 0

---

<!-- _pages/publications.md -->
<div class="publications">

<!-- To use years as categories, add 
years: [2023,2022,2021]
to header!
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[year={{y}}]* %}
{% endfor %}
-->


{% bibliography -f {{ site.scholar.bibliography }} %}


</div>
