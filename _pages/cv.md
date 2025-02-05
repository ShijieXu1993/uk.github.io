---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D in Financial Mathematics, University of Liverpool, 2024
* M.S. in Financial Mathematics, University of Liverpool, 2019
* B.S. in Mathematical Economics, Fudan University, 2017


  
Skills
======
* Language: Chinese, English
* Coding language: Python, SQL(my SQL), Pandas, Matlab, R, LaTeX
  
Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  

