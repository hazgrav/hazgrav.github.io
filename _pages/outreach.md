---
layout: page
permalink: /outreach/
title: outreach
description: Overview of outreach activities ran by HazGrav in and around Corvallis, OR
nav: true
nav_order: 6
horizontal: false
display_categories: ["Workshops", "Public lectures", "K-12"]
---

<!-- pages/outreach.md -->
<div class="projects">
{% if site.enable_outreach_categories and page.display_categories %}
  <!-- Display categorized outreach -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_outreach = site.outreach | where: "category", category %}
  {% assign sorted_outreach = categorized_outreach | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_outreach %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_outreach %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display outreach without categories -->

{% assign sorted_outreach = site.outreach | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_outreach %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_outreach %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
