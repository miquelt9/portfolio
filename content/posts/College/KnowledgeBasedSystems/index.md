---
title: "Knowledge Based Systems"
date: 2022-12-19T06:00:23+06:00
description: KnowledgeBasedSystems
theme: Toha
menu:
  sidebar:
    name: Knowledge Based Systems
    identifier: knowledgebasedsystems
    parent: college
    weight: 500
draft: false
tags: ["College","AI", "Clips"]
math: true
---

## The statement
In order to keep the older population in shape we had to build a program that recommends exercises and activities that are appropiate taking into account all factors of the individual and how may effect on the performance and goals.

I.e.: given certain information about a person, we had to output an exercise plan suitable for him/her.

The full statement is in the document below. Note that the statement is in Spanish.

<embed src="PracticaSBC.pdf" width="100%" height="700" type="application/pdf">

## Our approach
Together with [@JCasahuga](https://github.com/JCasahuga) and [@XBLOYT](https://github.com/XBLOYT), we starting building an ontology using [Protégé](https://protege.stanford.edu/). We specified all items involved in the problem, such as the different illnesses, body parts, properties, activities... Then using [owl2else](https://pypi.org/project/owl2else/) to convert our .owl file to a [CLIPS](https://clipsrules.net/). It was tricky to understand how to make our [CLIPS](https://clipsrules.net/) script work, but after few hours of try/error, asking other teams and reading a tone of tutorial we manage to make it work.

{{< figure src="ontologia_protege.png">}}
<p style="text-align: center;">Parts of the ontology in Protégé.</p>

{{< line_break >}}

Knowing how [CLIPS](https://clipsrules.net/) works, all we did afterwards was receive the input from the user and use some custom formulas with a little bit of randomitzation (so not all inputs did give the same result) for advising the user which exercises to do as well as their intensity based on its needs.


<embed src="Informe_SBC.pdf" width="100%" height="700" type="application/pdf">
<p style="text-align: center;">Final report (in Catalan).</p>

#### [Project's code on Github <i class="fab fa-github"></i> ](https://github.com/miquelt9/SBC) 
