---
title: "Chips-Chips"
date: 2022-11-13T06:00:23+06:00
description: Funcions Numerables
theme: Toha
menu:
  sidebar:
    name: Chips-Chips
    identifier: funcions_numerables
    parent: competitions
    weight: 500
draft: false
tags: ["Competition", "Python"]
---


## The challenge
The goal of this challenge was to minimize the average length of chains that connected pins in a chip, while also trying to minimize the standard deviation of the lengths of the different chains. This was a problem set by Qualcomm for the [FME Datathon 2022](https://datathon.cat/2022/) which had the aim of minimizing the power loss across a chip.    

## Our approach

Together with [Paula](https://github.com/paulaesquerra), [Ruth](https://github.com/ruthilberry), [Àlex](https://github.com/AlexRG03) and I, we decided to approach the problem by modelling it by considering a graph where the nodes are pins and the edges cables. We implemented 2 strategies:   

The first strategy was implemented to minimize the sum of the lengths of the chain. In each iteration the algorithm connects a node to the path by removing one edge and and adding 2 edges from the disconnected nodes to the new node, which is choosen to minimize the length. However even though this works well, because the algorithm takes O(n³) it takes too long for large cases (>1000 nodes).   

Our second stratregy is less accurate but has a time complecity of O(log(n)). It takes all the pins (nodes) and divides them into 32 different intervals depending on the Y-axis, then every pin on the interval is connected with the same cable from left to right and the n-th interval is connected with the n+16-th internval so we connect the input with the output driver.

{{< line_break >}}

{{< figure src="pins.png">}}
<p style="text-align: center;">One of our solutions.</p>


#### [View Project on Devpost ](https://devpost.com/software/chip-chips)

#### [Project's code on Github <i class="fab fa-github"></i> ](https://github.com/paulaesquerra/funcions_numerables_datathon)