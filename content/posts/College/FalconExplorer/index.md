---
title: "Falcon Explorer"
date: 2023-01-22T06:00:14+02:00
description: Falcon Explorer Document Manager
theme: Toha
menu:
  sidebar:
    name: Falcon Explorer
    identifier: falconexplorer
    parent: college
    weight: 500
draft: false
tags: ["College", "Java"]
math: true
---

## The statement
The [PROP](https://www.fib.upc.edu/en/studies/bachelors-degrees/bachelor-degree-informatics-engineering/curriculum/syllabus/PROP) college subject asked us to create an application to manage documents using Java. The app must allow the user to create, read, write, modify, delete, import and export files in various formats. One of the key features of the app is the queries to allow the user to find documents based on multiple arguments.

The full statement is in the document below (in Catalan). 

<embed src="enunciatProp.pdf" width="100%" height="700" type="application/pdf">

## Our approach
Together with [@AleexHrB](https://github.com/AleexHrB), [@LlucCC](https://github.com/LlucCC) and [@eZWALT](https://github.com/eZWALT), we made a case diagram to list all the features and functionalities our app had to have. One of the most important parts of it was the algorithms and a data structure we used. We ended up using the [Ternary Search Tree](https://en.wikipedia.org/wiki/Ternary_search_tree) data structure to index all words contained in the documents and the [term frequency–inverse document frequency](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) algorithm also known as tf-idf to rank the importance of each word across the documents.

{{< line_break >}}

## Documentation

<embed src="UserManual.pdf" width="100%" height="700" type="application/pdf">
<p style="text-align: center;">Falcon explorer user's manual.</p>

{{< line_break >}}
{{< line_break >}}

<embed src="documentation3.pdf" width="100%" height="700" type="application/pdf">
<p style="text-align: center;">Final report (in Catalan).</p>

{{< line_break >}}
{{< line_break >}}

#### [Project's code on Github <i class="fab fa-github"></i> ](https://github.com/miquelt9/PROP-FIB) 
