---
layout: archive
title: "Data Science Projects"
permalink: /data-science-projects/
---

{% for post in site.categories['Data Science'] %}
  <div class="post-summary">
    <h2>
      <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    </h2>

    <!-- Extract and display the first image from the post content -->
    {% if post.content contains "<img" %}
      {% assign img_parts = post.content | split: '<img ' %}
      {% for part in img_parts %}
        {% if part contains 'src="' %}
          {% assign img_tag = '<img ' | append: part | split: '>' | first %}
          {% assign img_src = img_tag | split: 'src="' | last | split: '"' | first %}
          <img src="{{ img_src | prepend: site.baseurl }}" alt="Post image" style="max-width: 100%; height: auto;">
          {% break %}
        {% endif %}
      {% endfor %}
    {% endif %}

    <p>{{ post.excerpt | strip_html }}</p>
    <a href="{{ post.url | prepend: site.baseurl }}">Read More...</a>
  </div>
{% endfor %}
