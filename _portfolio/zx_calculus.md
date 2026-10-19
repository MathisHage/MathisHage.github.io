---
title: "Research Internship : On the Hardness of Proving a ZX-Diagram Equality"
title_fr: "Stage de recherche : Sur la difficulté de prouver l'égalité de deux diagrammes ZX"
excerpt: "Investigated proof complexity and computational complexity questions about the ZX-calculus language for quantum computing. <a href='https://github.com/MathisHage/zx_calculus_internship'>[GitHub]</a>"
excerpt_fr: "Étude de questions de complexité de preuve et de complexité algorithmique autour du langage ZX-calculus pour l'informatique quantique. <a href='https://github.com/MathisHage/zx_calculus_internship'>[GitHub]</a>"
collection: portfolio
date: 2026-08-15
fr_url: /fr/projects/
---

# On the Hardness of Proving a ZX-Diagram Equality

**Role** : Research Intern, Summer 2026  
**Lab / Institution** : ALGO Group, University of Geneva  
**Author** : Mathis Hage  
**Repository** : [github.com/MathisHage/zx_calculus_internship](https://github.com/MathisHage/zx_calculus_internship)

---

## Context

The ZX-calculus language is a graphical way to represent and reason about linear maps between qubits. It is similar to, but more expressive than, quantum circuits, in the sense that a ZX-diagram can represent any linear map between qubits (universality). It has a wide range of applications including in quantum circuit optimization (such as T-gate count reduction), circuit equivalence verification, quantum error correction, etc. Here is a [useful website](https://zxcalculus.com/) for more information.

After several years of studies, the ZX-calculus has finally seen emergence of rulesets ensuring completeness for all sorts of fragments of quantum mechanics. Even though we therefore know that we can always prove or disprove an equality between two ZX-diagrams using only the rules of ZX-calculus, an interesting question could be to ask what is the number of rules necessary to do so. My work exhibits the difficulty of this question, lying mostly in proof complexity theory.

## The Problem

Since the ZX-calculus is *complete*, any two equivalent diagrams can always be transformed into one another using a sequence of rewrite rules. A natural question from proof complexity is then : *what is the number of steps needed to prove an equality between two diagrams ?*

More specifically, we study the complexity class of the language :

$$\textsc{ZX-REWRITE} := \{ (D_1, D_2, k) \; | \; D_1, D_2 \text{ are ZX-diagrams s.t. } D_1 = D_2 \text{ can be proven in at most } k \text{ steps}\}.$$

## Results

In this work, I prove that $\textsc{ZX-REWRITE}$ is in NP for rational phases by constructing an explicit polynomial-time verifier. I then introduce a reduction from $\textsc{SUBSET-SUM}$ showing that the problem is NP-hard when restricted to the spider fusion rule, and argue that this hardness extends to the general ruleset. Finally, for real phases, I discuss how an analogous reduction could be framed in the linear Blum-Shub-Smale (BSS) model to argue for $\text{NP}^=_{\text{lin}}$-hardness.

## Deliverables & Links
* [Report (PDF)](https://github.com/MathisHage/zx_calculus_internship/blob/main/report/report.pdf)
* [Presentation Slides (PDF)](https://github.com/MathisHage/zx_calculus_internship/blob/main/presentation/slides.pdf)
* [Code and Notebooks on GitHub](https://github.com/MathisHage/zx_calculus_internship)
