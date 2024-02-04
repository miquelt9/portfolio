---
title: "Royal Hackaway v6"
date: 2022-02-07T06:00:23+06:00
description: Royal Hackaway v6
theme: Toha
menu:
  sidebar:
    name: Royal Hackaway v6
    identifier: royalhackawayv6
    parent: competitions
    weight: 500
draft: false
tags: ["AI", "Competition", "C#", "PDDL", "Unity"]
---


## Our project
When [@BernatBC](https://github.com/BernatBC), [@alexland7219](https://github.com/alexland7219), [@Loparc](https://github.com/Loparc), and I discovered that a shark plushies were one of the prizes of an clearly underated challenge, we realized that 
the UK's hackathons needed a way to optimally distribute the shark flushies across the country.

Therefore, we develop a simulator that allows them to place the distribution centers and hackathons (and link them), as well as how many plushie vans you want and its capacity, and it will find a optimal route at the same time it satisfies the demand.

To build it we use Unity for the user interface side of the project, and for the algrithms we used PDDL, which uses A* to guide himself to the optimal solution. In case it's detected that optimal solution might be too expensive to find, a optimized solution will be looked for so the solution is given in a reasonable amount of time.

{{< line_break >}}

{{< youtube -YuJQaDd6i0 >}}

{{< line_break >}}

#### [View Project on Devpost ](https://devpost.com/software/plushistics)

#### [Project's code on Github <i class="fab fa-github"></i> ](https://github.com/Loparc/Plushistics-Royal_Hackaway_v6 )

#### [<i class="fa-solid fa-cloud-arrow-down"></i> for <i class="fa-brands fa-windows"></i>Windows 64bit ](https://github.com/Loparc/Plushistics/releases/download/release-1.1/Plushistics.zip)