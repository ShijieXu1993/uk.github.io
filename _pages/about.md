---
permalink: /
title: "Introduction"
description: "Latest blog posts and research notes from Shijie Xu, PhD researcher in Financial Mathematics at the University of Liverpool."
author_profile: false
layout: single
classes: wide
mondrian_home: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

<div class="home-grid">

  <header class="tile tile--name">
    <p class="eyebrow">Mathematician · Marketcolor, UK</p>
    <h1>Shijie Xu</h1>
    <div class="bio">
      <p>I am a PhD researcher in Financial Mathematics at the University of Liverpool, and a mathematician at Marketcolor, UK.</p>
      <p>My research interests are financial mathematics and stochastic analysis. I use this site to collect research notes, implementation write-ups, and updates on my academic work.</p>
    </div>
  </header>

  <div class="tile tile--photo">
    <img src="{{ base_path }}/images/profile.png" alt="Shijie Xu">
  </div>

  <a class="tile nav-tile tile--research" href="{{ base_path }}/year-archive/">
    <p class="eyebrow">Explore</p>
    <span class="nav-label">Blog</span>
    <span class="nav-sub">Research notes &amp; write-ups <span class="arrow" aria-hidden="true">&rarr;</span></span>
  </a>

  <a class="tile nav-tile tile--cv" href="{{ base_path }}/cv/">
    <span class="nav-label">CV</span>
    <span class="nav-sub">Background <span class="arrow" aria-hidden="true">&rarr;</span></span>
  </a>

  <div class="tile tile--blue" aria-hidden="true"></div>

  <a class="tile nav-tile tile--teaching" href="{{ base_path }}/publications/">
    <span class="nav-label">Papers</span>
    <span class="nav-sub">Publications <span class="arrow" aria-hidden="true">&rarr;</span></span>
  </a>

  <a class="tile nav-tile tile--contact" href="{{ base_path }}/talks/">
    <span class="nav-label">Talks</span>
    <span class="nav-sub">Presentations <span class="arrow" aria-hidden="true">&rarr;</span></span>
  </a>

  <a class="tile nav-tile tile--misc" href="{{ base_path }}/teaching/">
    <span class="nav-label">Teaching</span>
    <span class="nav-sub">Courses &amp; supervision <span class="arrow" aria-hidden="true">&rarr;</span></span>
  </a>

  <div class="tile tile--extra" aria-hidden="true"></div>

</div>

<section class="home-posts">
  <h2>Latest posts</h2>

{% assign recent_posts = site.posts | where_exp: "post", "post.hidden != true" %}
{% if recent_posts.size > 0 %}
  {% for post in recent_posts limit:10 %}
    {% include archive-single.html %}
  {% endfor %}
{% else %}
  New posts will appear here once they are published.
{% endif %}
</section>
