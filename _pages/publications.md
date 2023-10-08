---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u>my Google Scholar profile.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
  {% assign has_date = post.date | default: nil %}
  {% if has_date == nil and post.circumstance and post.venue %}
    <p>......</p >
  {% endif %}
{% endfor %}
