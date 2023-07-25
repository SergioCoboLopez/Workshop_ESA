---
layout: default
title: Models
nav_order: 4
---

Remember that GoldSim offers two very good [free courses](https://www.goldsim.com/Web/Customers/Education/Overview/) and other [learning resources](https://www.goldsim.com/Web/Customers/). There is also an active [community of users](https://www.goldsim.com/Web/Customers/Community/)

# Models

This section covers a series of models specific for the workshop at the [ESA Annual Meeting](https://esa.org/portland2023/) of 2023. 
---

## Model 1
This model is an example provided by GoldSim in their basic course and can be found [here](https://www.goldsim.com/Courses/BasicGoldSim/Unit3/Lesson2/). You can find a video of how to build my own version of the model in the repository <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/data/videos>

has not been built by me. It is an example provided by GoldSim and can be found [here](https://www.goldsim.com/Courses/BasicGoldSim/Unit3/Lesson2/). However, it is a very good example to familiarize ourselves with GoldSim and how it works.

## Model 2
This is our version of a Lotka-Volterra system.

You can find and download this model in the repository at <https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/GoldSim_Models/Bacterial_growth.gsm>

## Model 3
This one is our model for Lytic-Lysogenic interactions

You can find and download this model in the repository at <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models>

### GoldSim player files
In the event that you cannot access or use GoldSim, I have provided three player files. GoldSim player files can be run with GoldSim player, but they cannot be edited.

## GoldSim player 1

This file can be found in the [repository](https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files) under the name Bacterial_growth.gsp.
The model simulates the bacterial growth of three bacterial strains using values found in the literature. In the player file, you can select several parameters to play around.

## GoldSim player 2
This file can be found under the name Bacterial_growth_stochastic.gsp.
In this model I introduced stochasticity to account for variables that cannot be controled in experimental settings: the bacterial growth rate is not a fixed number, but an average depending on different factors. The same applies to the carrying capacity.

## GoldSim player 3
This file can be found under the name Lotka_Volterra.gsp.

In this model, I simulate a predator-prey model for bacteria and virulent phage with Lotka-Volterra equations. The model comprises for ecological mechanisms: exponential bacterial growth, infection of bacteria by phages, phage growth by burst, and phage decay.

---
