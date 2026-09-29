---
permalink: /
title: "Introduction"
description: "Latest blog posts and research notes from Shijie Xu, PhD researcher in Financial Mathematics at the University of Liverpool."
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}
Shijie Xu is a mathematician at Marketcolor, UK.

His research interests are financial mathematics and stochastic analysis.

## Latest posts

{% assign recent_posts = site.posts | where_exp: "post", "post.hidden != true" %}
{% if recent_posts.size > 0 %}
  {% for post in recent_posts limit:10 %}
    {% include archive-single.html %}
  {% endfor %}
{% else %}
  New posts will appear here once they are published.
{% endif %}
