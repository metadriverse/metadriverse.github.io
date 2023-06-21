---
layout: page-center
permalink: /metadrive/
title: MetaDrive
description: "MetaDrive: Composing Diverse Driving Scenarios for Generalizable Reinforcement Learning"
nav: true
nav_order: 1
---



<div class="metadrive">
  {% for post in site.metadrive %}
  <div class="container metadrive">
    <div class="text">
      <h2>{{ post.title }}</h2>
      <p>{{ post.content }}</p>
    </div>
    <div class="image">
      {% if post.img %}
        <img src="{{ post.img | relative_url }}" alt="{{ post.title }}" />
      {% else %}
        {% if post.video %}
        <video autoplay loop muted>
          <source src="{{ post.video | relative_url }}" type="video/mp4">
          Your browser does not support the video tag.
        </video>
        {% else %}
          {% if post.youtube_id %}
            <iframe width="560" height="315" src="https://www.youtube.com/embed/{{ post.youtube_id }}?autoplay=1&loop=1&mute=1&playlist={{ post.youtube_id }}" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          {% endif %}
        {% endif %}
      {% endif %}
    </div>
  </div>
  {% endfor %}
</div>

