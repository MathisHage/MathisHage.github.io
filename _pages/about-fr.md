---
permalink: /fr/
title: ""
lang: fr
en_url: /
author_profile: true
---

{% include base_path %}

À propos
========
Je suis étudiant en Master d'informatique (avec un mineur en mathématiques) à l'[EPFL](https://www.epfl.ch/), en Suisse, où j'ai également obtenu mon Bachelor en informatique. Je m'intéresse à la plupart des sujets à la frontière entre l'informatique théorique et les mathématiques, tels que l'optimisation, la complexité algorithmique ou la logique mathématique.

Je suis actuellement à la recherche d'un projet de semestre dans un domaine lié au sens large à l'optimisation mathématique.

Vous pouvez consulter mon [CV complet ici]({{ base_path }}/fr/cv/) ([PDF]({{ base_path }}/files/cv.pdf)).

Travaux sélectionnés
====================

Voici quelques-uns de mes projets et expériences passés :

{% assign post = site.portfolio | where: "path", "_portfolio/zx_calculus.md" | first %}
{% include archive-single.html %}

{% assign post = site.portfolio | where: "path", "_portfolio/nooc.md" | first %}
{% include archive-single.html %}

{% assign post = site.portfolio | where: "path", "_portfolio/opti_ml.md" | first %}
{% include archive-single.html %}

<p style="margin-top: 0.5em;"><a href="{{ base_path }}/fr/projects/">Voir tous les projets &amp; travaux de recherche &rarr;</a></p>

Enseignement
============

J'ai travaillé comme assistant-étudiant à l'EPFL, où j'ai encadré des étudiants de Bachelor lors des séances d'exercices et participé aux corrections :
* **Modèles Stochastiques pour les Communications** — Automne 2026 ;
* **Theory of Computation** — Printemps 2026 ;
* **Advanced Information, Computation and Communication II** — Printemps 2024.
