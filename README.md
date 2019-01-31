# Prey-predator Dynamics

## Introduction
This project is about the dynamics of prey-predator system simulation with several conditions and parameters. This system consists of only four different species, but surprisingly with certain conditions and parameters, this system shows chaos phenomena which are characteristic of complex systems.

The species of this system are **A, X, Y, and Z**. Species A is autotrophs, Species X prey on species A, species Y prey on species X, and species Z prey on species Y. 

## Method
The dynamics of this system will be simulated by the differential equation of numbers of species over time. There are four equations that describe each species.

We will see the changing of numbers of species over time affected by their own predator and parameters.

These parameters are an **environment, activities, and numbers of their prey**. But these parameters are *not independent*. Each parameter affected by another parameter. and changing over time. However, each species has a constant parameter that characterizes them.

Activities parameter consist of *eating and mating parameter*. Environment parameter depends on the probability distribution of rain. I assume higher probability means that it will more affect species A to growth. But this will decrease eating parameter of other species, conversely increasing mating parameter. There are two more parameters that are *birth and death parameter*. Each species has their own birth and death constant parameter. 

Furthermore, we know that eating parameter must be controlled. Because it can be so high even though there is no food and it is impossible. So we must add another parameter, I named it an **alpha** parameter. Alpha parameter is the ratio of predator over prey. If alpha so *high*, then eating parameter must be low. Conversely, if alpha so *low*, then eating parameter must be high, if alpha *stable*, then it will not affect eating parameter. But we must choose 'low', 'stable' and 'high' value carefully.

I called the sum of all parameter to be the beta parameter.

Differential equations and equations of parameters are written on image.
![mind map](https://pbs.twimg.com/media/DyN1S5JVYAA2Mf1.jpg:large)

## Result

![graph 1](https://pbs.twimg.com/media/DyN3Yq_V4AAYFDN.jpg:large)
![graph 2](https://pbs.twimg.com/media/DyN36QhUwAAqwLk.jpg:large)
![graph 3](https://pbs.twimg.com/media/DyN4GuAVYAAOQJi.jpg:large)

X species dynamics animation: https://twitter.com/i/status/1090848173696868352
