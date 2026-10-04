---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

About Me
========
I am a masters student in Computer Science at [EPFL](https://www.epfl.ch/), Switzerland. I am interested in about any subjects at the border between theoretical computer science and mathematics, such as optimization, computational complexity, or mathematical logic.

Selected Work
=============

Here are a few of my past projects / experiences :

{% include base_path %}

{% assign post = site.portfolio | where: "Networks Out of Control (COM-512)", "Research Paper Analysis" | first %}
{% include archive-single.html %}
