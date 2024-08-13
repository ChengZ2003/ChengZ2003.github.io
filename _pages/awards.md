---
layout: page
title: Awards
permalink: /awards/
description: Display of some big and small awards.
nav: true
nav_order: 2
horizontal: false
---

<!-- pages/awards.md -->
<div class="awards">
  {% if site.enable_awards %}
    {% assign awards = site[site.awards_dir] | sort: "importance" %}
    {% for award in awards %}
      <div class="award">
        <h2>{{ award.title }}</h2>
        <p>{{ award.description }}</p>
        <p><em>{{ award.year }}</em></p>
      </div>
    {% endfor %}
  {% else %}
    <p>No awards to display.</p>
  {% endif %}
</div>