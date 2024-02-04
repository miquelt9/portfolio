---
title: "PDDL on Mars"
date: 2023-01-14T06:00:23+06:00
description: Planification project
theme: Toha
menu:
  sidebar:
    name: PDDL on Mars
    identifier: planification
    parent: college
    weight: 500
draft: false
tags: ["College", "AI", "PDDL"]
math: true
---

## The statement
In 2075, the first colonizers of Mars have established a network of bases throughout the geography of the planet. Moving between these bases is done by rovers that can move supplies and specialized personnel.

We are in charge of planning the movements of the rovers from the base where they are parked, to pick up the supplies and personnel, to bring them in the requested place. We've been told that there are always more requests for supplies and personnel of those that can be used (life on Mars is very hard).

In this project, they ask to write a [PDDL](https://planning.wiki/) script alongside with the [Metric-FF](https://fai.cs.uni-saarland.de/hoffmann/metric-ff.html) planning system to solve the problem. We had to make both the domain and problem files.

The full statement is in the document below (in Spanish).

<embed src="PracticaPlanificacion.pdf" width="100%" height="700" type="application/pdf">

## Our solution
Together with [@JCasahuga](https://github.com/JCasahuga) and [@XBLOYT](https://github.com/XBLOYT), we started creating a basic domain with its objects, predicates and actions to allow PDDL find a solution for the problems definitions.   
Multiple extensions of the domain were requiered and the final one included capacity and fuel of the rovers, plus priority for the supplies and we optimized it using a custom heuristic.

<embed src="Informe_PDDL.pdf" width="100%" height="700" type="application/pdf">
<p style="text-align: center;">Final report (in Catalan).</p>

### [Project's code on Github <i class="fab fa-github"></i> ](https://github.com/miquelt9/PDDL-MarsLogistics) 
