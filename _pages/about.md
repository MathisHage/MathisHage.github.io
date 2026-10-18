---
permalink: /
title: ""
author_profile: true
fr_url: /fr/
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}

About Me
========
I am a Master's student in Computer Science (with a Minor in Mathematics) at [EPFL](https://www.epfl.ch/), Switzerland, where I also completed my B.Sc. in Computer Science. I am interested in about any subjects at the border between theoretical computer science and mathematics, such as optimization, computational complexity, or mathematical logic.

I am currently looking for a semester project in a field broadly related to mathematical optimization.

You can find my full [CV here]({{ base_path }}/cv/) ([PDF]({{ base_path }}/files/cv.pdf)).

Selected Work
=============

Here are a few of my past projects / experiences :


{% assign post = site.portfolio | where: "path", "_portfolio/zx_calculus.md" | first %}
{% include archive-single.html %}

{% assign post = site.portfolio | where: "path", "_portfolio/nooc.md" | first %}
{% include archive-single.html %}

{% assign post = site.portfolio | where: "path", "_portfolio/opti_ml.md" | first %}
{% include archive-single.html %}

<p style="margin-top: 0.5em;"><a href="{{ base_path }}/projects/">See all research &amp; projects &rarr;</a></p>

Teaching
========

I have worked as a Student Assistant at EPFL, helping undergraduate students during exercise sessions and participating in grading :
* **Stochastic Models in Communications** — Fall 2026 ;
* **Theory of Computation** — Spring 2026 ;
* **Advanced Information, Computation and Communication II** — Spring 2024.

