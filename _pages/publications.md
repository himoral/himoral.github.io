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
  {% if post.date %}
    {% assign has_date = true %}
  {% endif %}
  {% if post.circumstance and post.venue and !post.date %}
    {% if has_date %}
      <p>......</p >
    {% else %}
      <p>......</p >
    {% endif %}
  {% endif %}
{% endfor %}
