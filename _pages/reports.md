---
layout: archive
title: "Reports"
permalink: /reports/
author_profile: true
#redirect_from: 
#  - "/informes/"
#  - "/reports.html"
---

These are some example reports that I have written.

Métodos Numéricos para la Ingeniería y Ciencias (FI3104)
======

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.reports reversed %}
  {% include archive-single.html %}
{% endfor %}


Heading 2
======
