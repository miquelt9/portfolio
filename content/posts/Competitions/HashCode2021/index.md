---
title: "Google Hash Code 2021"
date: 2021-02-25T06:00:23+06:00
description: Google Hash Code 2021
theme: Toha
menu:
  sidebar:
    name: Google Hash Code 2021
    identifier: hashcode2021
    parent: competitions
    weight: 500
draft: false
tags: ["Competition", "C++"]
---

[Google Hash Code](https://codingcompetitions.withgoogle.com/hashcode) is a team programming competition that lasts about 4 hours, in which a solution to multiple inputs of a problem must be given, points are given depending on how good it is.

## The problem
In 2021 a city road network was given and planned paths for all cars in it, we had to optimize the schedule of traffic lights to minimize the total amount of time spent and help as many cars as possible reach their destination.

The full problem statement is below:

<embed src="hashcode_2021_online_qualification_round.pdf" width="100%" height="700" type="application/pdf">

## Our submission
Together with [@BernatBC](https://github.com/BernatBC), [@alexland7219](https://github.com/alexland7219) and I, three friends that just started that year to learn CS we started thinking about a solution. We first thought about counting the potential number of cars for each starting point and destination, assigning a more time to the roads that had more traffic influx. However due to our lack of experience and all the compilation errors and bugs we were having we were running out of time. At that time, we wanted to get at least some points but nothing was working, therefore we decided to try submitting a solution where all traffic lights had the same duration. This was a simple solution, but it worked out well enough! (way better than nothing)

In the ended up obtaining 7,886,739 points, getting into the 4432 position out of 9004. Not bad at all for our first ever coding competition.

#### [Solution's code on Github <i class="fab fa-github"></i>](https://github.com/BernatBC/Coding-Competitions/tree/main/GoogleHashCode2021)