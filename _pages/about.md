---
permalink: /
title: "Introduction"
description: "Latest blog posts and research notes from Shijie Xu, PhD researcher in Financial Mathematics at the University of Liverpool."
author_profile: false
mathjax: true
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
      <p>I am a PhD in financial mathematics at University of Liverpool, supervised by Prof. Paul Eisenberg.</p>
      <p>I am a mathematician at Marketcolor, UK.</p>
      <p>My research interests are financial mathematics and stochastic analysis.</p>
    </div>
  </header>

  <div class="tile tile--red" aria-hidden="true"></div>
  <div class="tile tile--yellow tile--contactinfo">
    <ul class="contact-links">
      <li><a href="mailto:{{ site.author.email }}" aria-label="Email" title="Email"><i class="fas fa-envelope" aria-hidden="true"></i></a></li>
      <li><a href="https://www.linkedin.com/in/{{ site.author.linkedin }}" target="_blank" rel="noopener" aria-label="LinkedIn" title="LinkedIn"><i class="fab fa-linkedin-in" aria-hidden="true"></i></a></li>
      <li><a href="https://github.com/{{ site.author.github }}" target="_blank" rel="noopener" aria-label="GitHub" title="GitHub"><i class="fab fa-github" aria-hidden="true"></i></a></li>
      <li><a href="{{ site.author.orcid }}" target="_blank" rel="noopener" aria-label="ORCID" title="ORCID"><i class="ai ai-orcid" aria-hidden="true"></i></a></li>
    </ul>
  </div>
  <a class="tile nav-tile tile--blue2" href="{{ base_path }}/portfolio/">
    <span class="nav-label">Gallery</span>
    <span class="nav-sub">Photos <span class="arrow" aria-hidden="true">&rarr;</span></span>
  </a>

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

  <a class="tile nav-tile tile--blue" href="{{ base_path }}/teaching/">
    <span class="nav-label">Teaching</span>
    <span class="nav-sub">Courses <span class="arrow" aria-hidden="true">&rarr;</span></span>
  </a>

  <a class="tile nav-tile tile--teaching" href="{{ base_path }}/publications/">
    <span class="nav-label">Papers</span>
    <span class="nav-sub">Publications <span class="arrow" aria-hidden="true">&rarr;</span></span>
  </a>

  <a class="tile nav-tile tile--contact" href="{{ base_path }}/talks/">
    <span class="nav-label">Talks</span>
    <span class="nav-sub">Presentations <span class="arrow" aria-hidden="true">&rarr;</span></span>
  </a>

  <div class="tile tile--misc" aria-hidden="true"></div>

  <div class="tile tile--extra" aria-hidden="true"></div>

</div>

<section class="home-posts">
  <h2>Latest post</h2>

{% assign recent_posts = site.posts | where_exp: "post", "post.hidden != true" %}
{% if recent_posts.size > 0 %}
{% assign post = recent_posts.first %}
<article class="home-post">
<h3 class="home-post__title"><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a></h3>
<p class="home-post__date">{{ post.date | date: "%B %-d, %Y" }}</p>
<div class="home-post__body" id="home-post-body">
{{ post.content }}
</div>
<button type="button" class="home-post__toggle" id="home-post-toggle" aria-expanded="false" aria-controls="home-post-body" hidden>Read more</button>
</article>
<script>
(function () {
  var body = document.getElementById('home-post-body');
  var btn = document.getElementById('home-post-toggle');
  if (!body || !btn) { return; }

  // only offer "Read more" when the post is longer than the collapsed height
  function check() {
    if (body.classList.contains('is-open')) { return; }
    btn.hidden = body.scrollHeight <= body.clientHeight + 2;
    body.classList.toggle('is-short', btn.hidden);
  }

  btn.addEventListener('click', function () {
    var open = body.classList.toggle('is-open');
    btn.setAttribute('aria-expanded', open ? 'true' : 'false');
    btn.textContent = open ? 'Show less' : 'Read more';
    if (!open) { body.parentNode.scrollIntoView({ block: 'start' }); }
  });

  check();
  window.addEventListener('load', check);
  window.addEventListener('resize', check);
  // maths is typeset after load and changes the height
  if (window.MathJax && MathJax.startup && MathJax.startup.promise) {
    MathJax.startup.promise.then(check);
  }
  setTimeout(check, 1500);
})();
</script>
{% else %}
New posts will appear here once they are published.
{% endif %}
</section>
