---
layout: archive
title: "Reports"
permalink: /reports/
author_profile: true
---

These are some example reports that I have written.

Heading
======

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.reports reversed %}
  {% include archive-single.html %}
{% endfor %}
