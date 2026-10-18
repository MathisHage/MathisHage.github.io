---
title: "Research Internship : On the Hardness of Proving a ZX-Diagram Equality"
excerpt: "Investigated proof complexity and computational complexity questions about the ZX-calculus language for quantum computing. <a href='https://github.com/MathisHage/zx_calculus_internship'>[GitHub]</a>"
collection: portfolio
date: 2026-08-15
---

# On the Hardness of Proving a ZX-Diagram Equality

**Role** : Research Intern, Summer 2026  
**Lab / Institution** : ALGO Group, University of Geneva  
**Author** : Mathis Hage  
**Repository** : [github.com/MathisHage/zx_calculus_internship](https://github.com/MathisHage/zx_calculus_internship)

---

## Abstract

After several years of studies, the ZX-calculus language for diagrammatic reasoning on qubits has finally seen emergence of rulesets ensuring completeness for all sorts of fragments of quantum mechanics. Even though we therefore know that we can always prove or disprove an equality between two ZX-diagrams using only the rules of ZX-calculus, an interesting question could be to ask what is the number of rules necessary to do so. This paper exhibits the difficulty of this question, lying mostly in proof complexity theory. Despite this, after some work to prove NP-membership, I still present serious arguments for NP-hardness of the problem when constrained to rational phases. An extension is then made to the real phases case in the context of the Blum-Shub-Smale Model, before ending by a hypothesis regarding the difficulty of the problem constrained to the Clifford fragment.

## The Problem

In this case study, we look at another aspect of the ZX-Calculus. We know that this language is *complete* : this means that two diagrams are equal if and only if there is a sequence of rules (allowed by the language) transforming one diagram into the other. Therefore it is always possible to go from one diagram to another if they represent the same linear map on qubits. An interesting question can now be asked : what is the *number of steps* needed to prove an equality between two diagrams ? More specifically, let the language :

$$\textsc{ZX-REWRITE} := \{ (D_1, D_2, k) \; | \; D_1, D_2 \text{ are ZX-diagrams s.t. the equality } D_1=D_2 \text{ can be proven true in at most } k \text{ steps}\}.$$

What is its complexity class ? This problem not only stems from ZX-calculus theory, but also from a general proof complexity setting.

## Deliverables & Links
* [Report (PDF)](https://github.com/MathisHage/zx_calculus_internship/blob/main/report/report.pdf)
* [Presentation Slides (PDF)](https://github.com/MathisHage/zx_calculus_internship/blob/main/presentation/slides.pdf)
* [Code and Notebooks on GitHub](https://github.com/MathisHage/zx_calculus_internship)
