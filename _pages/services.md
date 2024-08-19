---
layout: page
title: services
permalink: /services/
description: Showcasing our main services.
nav: true
nav_order: 2
display_categories: [self-development, analytics, writing, workshops]
horizontal: false
---

<!-- pages/services.md -->
<div class="services">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized services -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_services = site.services | where: "category", category %}
  {% assign sorted_services = categorized_services | sort: "importance" %}
  <!-- Generate cards for each service -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for service in sorted_services %}
      {% include services_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for service in sorted_services %}
      {% include services.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display services without categories -->

{% assign sorted_services = site.services | sort: "importance" %}

  <!-- Generate cards for each service -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for service in sorted_services %}
      {% include services_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for service in sorted_services %}
      {% include services.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
