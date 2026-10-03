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
* M.Sc. in Computer Science, Minor in Mathematics, EPFL, 2026 - Current
* B.Sc. in Computer Science, EPFL, 2022 - 2025

Work experience
======
* Summer 2025: Research Intern
  * Geneva University
  * Studied properties of the ZX-calculus language for quantum computing from a complexity theory perspective
  * Supervisors: Matteo De Francesco, Prof. Arnaud Casteigts

* 2022-2026: Student Assistant at EPFL
  * Advanced Information, Computation, Communication II, Theory of Computation, Stochastic Models in Communication
  * Provided guidance to undergraduate students during exercise sessions, and participated in exam corrections
  
Skills
======
* Proficient in LateX, Git
* Proficient in declarative, imperative, functional and object-oriented programming. Languages include:
  * Python
  * Scala
  * C
  * C++
  * Java
  * Kotlin

Projects
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
