---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

A list of all the pages found on the site. 

{% for post in site.pages %}
  {% include archive-single.html %}
{% endfor %}
