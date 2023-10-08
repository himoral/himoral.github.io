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
    {% assign publication_date = post.date | date: "%B %d, %Y" %}
  {% endif %}
  {% if post.circumstance and post.venue %}
    <p>Target in <i>{{ post.venue }}</i>, <strong>{{ post.circumstance }}</strong></p >
  {% elsif publication_date %}
    <p class="page__date"><strong><i class="fa fa-fw fa-calendar" aria-hidden="true"></i> {{ site.data.ui-text[site.locale].date_label | default: "Published:" }}</strong> <time datetime="{{ publication_date }}">{{ publication_date }}</time></p >
  {% endif %}
{% endfor %}
