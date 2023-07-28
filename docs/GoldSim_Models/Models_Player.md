---
layout: default
title: GoldSim Player Models
nav_order: 6
parent: Models
---

## GoldSim Player files
In the event that you cannot access or use GoldSim, I have provided three player files. GoldSim player files can be run with GoldSim player, but they cannot be edited.

### Model 1 - Logistic bacterial growth

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files/Bacterial_growth.gsp>

This file can be found in the [repository](https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files) under the name Bacterial_growth.gsp.
The model simulates the bacterial growth of three bacterial strains using values found in the literature. In the player file, you can select several parameters to play around.

### Model 2 - Stochastic bacterial growth

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files/Bacterial_growth_stochastic.gsp>

This file can be found under the name Bacterial_growth_stochastic.gsp.
In this model I introduced stochasticity to account for variables that cannot be controled in experimental settings: the bacterial growth rate is not a fixed number, but an average depending on different factors. The same applies to the carrying capacity.

### Model 3 - Lotka Volterra

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files/Lotka_Volterra_Dashboard.gsp>

This file can be found under the name Lotka_Volterra.gsp.

In this model, I simulate a predator-prey model for bacteria and virulent phage with Lotka-Volterra equations. The model comprises for ecological mechanisms: exponential bacterial growth, infection of bacteria by phages, phage growth by burst, and phage decay.

---
