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
          <figure><img src="{{ member.image }}" class="img-responsive" alt="{{ member.name }}" /></figure>
          <h3><strong>{{ member.name }}</strong></h3>
          <h5>{{ member.role }}</h5>
          <ul class="follow-us clearfix">
            <a class="btn btn-dark btn-floating m-1" href="#!" role="button">
              <i class="bi bi-envelope-fill"></i> 
            </a>
            <a class="btn btn-dark btn-floating m-1" href="#!" role="button">
              <i class="bi bi-github"></i>
            </a>
          </ul>
        </div>
      </li>
    {% endfor %}
  </ul>
</div>

</section>

