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

![Lotka-Volterra](../figures/Lotka_Volterra_Diagram.PNG "Courtesy of GoldSim")


The equations for Lotka-Volterra model are shown below:

$$\begin{eqnarray*}
\frac{dB}{dt}&=&\underbrace{rB}_{Growth} - \underbrace{aBP}_{Predation} \\
\frac{dP}{dt}&=&\underbrace{caBP}_{Burst} - \underbrace{mP}_{Decay}
\end{eqnarray*}$$


|Letter|Element       |Units    | Value  |
|----:|--------------:|--------:|-------:|
|    B|Bacteria       |items/ml |   55600|
|    P|Phage          |items/ml | 3330000|
|r    |Growth rate    |1/h      |     0.1|
|a    |Adsorption rate|ml/h     |    3e-8|
|c    |Burst size     |         |     150|
|m    |Decay rate     |      1/h|     0.1|
