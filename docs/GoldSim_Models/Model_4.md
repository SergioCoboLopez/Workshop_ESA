---
layout: default
title: Model 4
nav_order: 4
parent: Models
---

## Model 4 - Lotka-Volterra

[Download](https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/GoldSim_Models/Lotka_Volterra.gsm){: .btn }

The next model is a [Lotka-Volterra](https://en.wikipedia.org/wiki/Lotka%E2%80%93Volterra_equations) predator-prey model for bacteria and bacteriophage.
In this case we have two pools: one for the bacteria and another one for the phage.
Bacteria have an inflow corresponding to exponential growth and an outflow corresponding to phage predation. This outflow becomes an inflow to phage: the concentration of phage
increases via burst. Phage have an outflow that corresponds to their decay.

![Lotka-Volterra](../figures/Lotka_Volterra_Diaram.png "Courtesy of GoldSim")


The equations for Lotka-Volterra model are shown below:

$$\begin{eqnarray*}
\frac{dB}{dt}&=&rB - aBP \\
\frac{dP}{dt}&=&caBP - mP
\end{eqnarray*}$$


|Letter|Element     |Units  |
|----|----------|-------|
|    B|Bacteria    |items/ml|
|    P|Phage    |items/ml  |
|r    |Growth rate |1/h    |
|a    |Adsorption rate |ml/h|
|c    |Burst size |items    |
|m    |Decay rate |1/h|
