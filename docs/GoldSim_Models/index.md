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

The pool element contains three tabs: 'Definition', 'Inflows', and 'Outflows'. Inflows and outflows specify the mechanisms by which the contents in the pool change
over time. Take, for instance, [Model 2](https://sergiocobolopez.github.io/Workshop_ESA/GoldSim_Models/Model_2.html). There is a pool named 'Bacteria' and a function
named 'Bacterial_growth'. You need to define the function as an inflow of the pool to observe actual growth.

![GoldSim elements](../figures/pool_elements_2.PNG "Courtesy of GoldSim")

**Functions**: GoldSim has many types of functions. In this workshop we are going to use the Expression, the Selector, and the Splitter.

![GoldSim elements](../figures/function_elements.PNG "Courtesy of GoldSim")

**Results**:

![GoldSim elements](../figures/function_elements.PNG "Courtesy of GoldSim")

**Containers**:

![GoldSim elements](../figures/function_elements.PNG "Courtesy of GoldSim")

**Events**:

**Delays**:





