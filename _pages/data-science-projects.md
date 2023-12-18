---
layout: archive
title: "Data Science Projects"
permalink: /data-science-projects/
---

{% for post in site.categories['Data Science'] %}
  <h2>
    <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
  </h2>
  <p>{{ post.excerpt | strip_html }}</p>
  <a href="{{ post.url | prepend: site.baseurl }}">Read More...</a>
{% endfor %}