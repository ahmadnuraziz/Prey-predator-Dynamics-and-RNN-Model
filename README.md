# Prey-predator Dynamics

## Introduction
This project is about the dynamics of prey-predator system simulation with several conditions and parameters. This system consists of only four different species, but it shows chaos and nonlinear phenomena which are characteristic of complex systems and tuning parameters is important in this case.

The species of this system are **A, X, Y, and Z**. Species A is autotrophs, Species X prey on species A, species Y prey on species X, and species Z prey on species Y. 

## Method
### 1. Simulation
The dynamics of this system will be simulated by the differential equation of numbers of species over time. There are four equations that describe each species.

We will see the changing of numbers of species over time affected by their own predator and parameters.

These parameters are an **environment, activities, and numbers of their prey**. But these parameters are *not independent*. Each parameter affected by another parameter. and changing over time. However, each species has a constant parameter that characterizes them.

Activities parameter consists of *eating and mating parameter*. Environment parameter depends on the probability distribution of rain. I assume higher probability means that it will more affect species A to growth. But this will decrease eating parameter of other species, conversely increasing mating parameter. There are two more parameters that are *birth and death parameter*. Each species has their own birth and death constant parameter. 

Furthermore, we know that eating parameter must be controlled. Because it can be so high even though there is no food and it is impossible. So we must add another parameter, I named it an **alpha** parameter. The alpha parameter is the ratio of predator over prey. If alpha so *high*, then eating parameter must be low. Conversely, if alpha so *low*, then eating parameter must be high, if alpha *stable*, then it will not affect eating parameter. But we must choose 'low', 'stable' and 'high' value carefully.

I called the sum of all parameter to be the beta parameter.

Differential equations and equations of parameters are written on image.
![mind map](https://pbs.twimg.com/media/DyN1S5JVYAAnJXP.jpg:large)

### 2. RNN Model
Results of the simulation are used to train the model of Recurrent Neural Network (RNN) with Long-Short Term Memory (LSTM) layer. The model is built with four layers and each layer has 50 units. Then I use Adam optimizer for this model.

## Result

This model simulation shows chaos and nonlinear phenomena. Nonlinear characteristics are indicated by fluctuations in the number of each species while chaos characteristics are indicated by small parameter differences that are very significant in the simulation results.

Graph 1 shows the results of the simulation of the number of species to time for all species while graph 2 is the simulation result for each species. Graph 3 shows the interaction between species, namely the number of one species increases while another species decreases. Graphs 1 and 2 show fluctuations in the number of species over time but these fluctuations do not indicate that one species has increased without control, meaning that the condition of the system is balanced. Even though it looks random, these fluctuations indicate repetitions or oscillations when viewed in detail.

The simulation results are very dependent on parameter selection. The parameters used in this simulation must be carefully chosen to produce system equilibrium, different parameters can produce very different phenomena, for example the number of one species is too high while the other species is too low means that the balance of the system is not reached. Physically in nature, these parameters indicate conditions that we do not know so as to create a balance in nature and no extinction occurs. Extinction can occur if there is a condition that significantly changes the system itself, if associated with this simulation it means that the system parameters change. For example, suddenly there is a terrible natural disaster or uncontrolled exploitation by humans towards nature. Further analysis related to these parameters is an interesting thing that can be investigated.

Furthermore, this simulation data is used to make the RNN model. RNN can be used to predict trends from time-dependent data. Graphs 4 and 5 show the simulation results of the RNN model, from the graph it can be seen that the RNN model can predict the number of one species well against time.

### Results of Simulation
![graph 1](https://pbs.twimg.com/media/DyN3Yq_V4AA1SwU.jpg:large)
![graph 2](https://pbs.twimg.com/media/DyN36QhUwAAubXc.jpg:large)
![graph 3](https://pbs.twimg.com/media/DyN4GuAVYAAIFZY.jpg:large)

X species dynamics animation: https://twitter.com/i/status/1090848173696868352

### Results of RNN Model
![graph 4](https://pbs.twimg.com/media/DzqetVXU8AAHd2X.jpg:large)
![graph 5](https://pbs.twimg.com/media/DzqggWdVsAAlYSh.jpg:large)
