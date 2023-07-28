---
layout: default
title: Model 4
nav_order: 4
parent: GoldSim_Models
---

## Model 4 - Lotka-Volterra

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/GoldSim_Models/Lotka_Volterra.gsm>

The next model is a Lotka-Volterra predator-prey model for bacteria and bacteriophage.

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
