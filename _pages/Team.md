---
layout: page-center
permalink: /team/
title: Team
description: "Meet Our Team Member!"
nav: true
nav_order: 4
---

<section class="our-webcoderskull">
<div class="container">
  <!-- <div class="row heading heading-icon">
    <h2>Our Team</h2>
  </div> -->
  <ul class="row">
    {% for member in site.data.team %}
      <li class="col-12 col-md-6 col-lg-4">
        <div class="cnt-block equal-hight">
<a href="{{ member.link }}">
          <figure><img src="{{ member.image }}" class="img-responsive" alt="{{ member.name }}" /></figure>
</a>
<a href="{{ member.link }}">            
<h3><strong>{{ member.name }}</strong></h3>
</a>
          <h6>{{ member.role }}</h6>
        </div>
        
      </li>
    {% endfor %}
  </ul>
</div>

</section>

