---
layout: default
title: Models
nav_order: 4
has_children: true
permalink: docs/GoldSim_Models
---

This section covers a series of models specific for the workshop at the [ESA Annual Meeting](https://esa.org/portland2023/) of 2023. 
Don't forget that GoldSim provides two excellent [free courses](https://www.goldsim.com/Web/Customers/Education/Overview/) and other 
valuable [learning materials](https://www.goldsim.com/Web/Customers/). Additionally, there is a thriving 
[community of users](https://www.goldsim.com/Web/Customers/Community/) who can provide help.

## Modeling elements in GoldSim

For a more detailed description, see the [Unit 2](https://www.goldsim.com/Courses/BasicGoldSim/Unit2/Lesson1/) of the GoldSim 
Introduction Course.

There are seven types of elements or building blocks in GoldSim:

**Inputs**: values you provide GoldSim to run a simulation. They can be just numbers (data elements), datasets, or probability 
distribution (stochastic elements). For example, the growth rate of a population. In this workshop we are going to deal 
primarily with data elements and stochastics.

![GoldSim elements](../figures/input_elements.PNG "Courtesy of GoldSim")

**Stocks**: These are the state variables or outputs of your model. For example, the population of animals in an ecosystem
or the volume of water in a tank. In this workshop we are going to use the pool element, but the reservoir and integrator are other stock elements.


![GoldSim elements](../figures/pool_elements.PNG "Courtesy of GoldSim")


The main elements that we are going to use in the next models are:

1. The pool

2. The input data element

3. The expression function element

4. The time history result

5. The container

6. The stochastic element

7. The dashboard




