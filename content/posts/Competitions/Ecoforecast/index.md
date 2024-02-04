---
title: "Ecoforecast"
date: 2023-11-21T06:00:23+06:00
description: Ecoforecast
theme: Toha
menu:
  sidebar:
    name: Ecoforecast 
    identifier: ecoforecast
    parent: competitions
    weight: 500
draft: false
tags: ["AI", "Competition", "Python", "Numpy", "Pandas", "scikit-learn"]
---


## The challenge

With increasing digitalisation and the growing on data servers, the significance of sustainable computing is on the rise. That's why the task is to predict which will be the European contry that will have the highest surplus of green energy in the following hour. Knowing this information can be critical to make important decisions in order to reduce CO2 emissions.
This [challenge](https://nuwe.io/dev/competitions/schneider-electric-european-2023/ecoforecast-revolutionizing-green-energy-surplus-prediction-in-europe) was the problem of a Nuwe competition.
  
## The approach

Given that no data for the training was given, I had to directly retrieve it using [entos-e api](https://transparency.entsoe.eu/content/static_content/Static%20content/web%20api/Guide.html), my lack of experience in APIs made me spend more time than I wanted in just obtaining the data. But after successfully getting it I needed to treat it, since intervals were not the same and there was some missing data.   

It was unfortunate to see how the data looked like in a chart, it was more than clear that during the last year, >99% of the hours, the country with the most surplus was the same. Nothing spectacular I could expect from my model, which it was trained to predict the MW of each country and from there extract which was the country with the highest surplus.    

{{< line_break >}}


{{< figure src="surplus_x_day.png">}}
<p style="text-align: center;">Surplus of green energy per day by country.</p>

{{< line_break >}}

The predictions reached a (not) stunning 0.9994295 accuracy and 0.9977298 precision, which was nice but not.   


{{< line_break >}}

#### [Project's code on Github <i class="fab fa-github"></i> ](https://github.com/miquelt9/ecoforecast_2023)

#### [Google Colab ](https://colab.research.google.com/drive/1ROKeqyYTzW2muFEA1-dAsgBHwFxoVSh8?usp=sharing)
