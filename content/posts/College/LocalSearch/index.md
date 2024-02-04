---
title: "Local Search"
date: 2022-10-24T06:00:23+06:00
description: Local search
theme: Toha
menu:
  sidebar:
    name: Local Search
    identifier: localsearch
    parent: college
    weight: 500
draft: false
tags: ["AI", "College", "Java"]
math: true
---

## The statement
Given a set of power plants and clients, we had to optimize the profit. Power gets drained depending on the distance it needs to travel, clients don't pay the same (not all of them are requiered to be served) and power plants costs depend on their size. 

To solve the problem, we were asked to use [Hill Climbing](https://en.wikipedia.org/wiki/Hill_climbing) and [Simulated Annealing](https://en.wikipedia.org/wiki/Simulated_annealing).

The full statement below (in Spanish).

<embed src="PracticaBusqueda-local.pdf" width="100%" height="700" type="application/pdf">

## Our solution
Together with [@JCasahuga](https://github.com/JCasahuga) and [@XBLOYT](https://github.com/XBLOYT), we used [AIMA](https://github.com/aimacode/aima-java) library and we determined the initial state, the operands as well as the heuristic function. 

During the projects we saw how the initial states and operands could effect the reached states and therefore the results of our program. Also creating a good heuristic function was important in order to improve the final earnings of our fictional company.

In the end starting with a lot of different initial states and applying bot Hill Climbing and Simulated Annealing with an heuristic function based on the profit (which needed to be optimally updated across the steps) was what gave us the best result.

<embed src="Informe_LS.pdf" width="100%" height="700" type="application/pdf">
<p style="text-align: center;">Final report (in Catalan).</p>

### [Project's code on Github <i class="fab fa-github"></i> ](https://github.com/JCasahuga/LocalSearch) 
