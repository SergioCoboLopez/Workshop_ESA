---
layout: default
title: Model 5
nav_order: 5
parent: Models
---

## Model 5 - The Metabolic Machine

This model simulates bacterial growth based on metabolism and energy production. The model comprises
three parts stored in containers: Metabolism, Energy production, and Bacterial growth.

### Metabolism

This part of the model is stored in a container, and it simulates three simplified metabolic 
processes: respiration, fermentation, and photosynthesis. The central state variables in this
 container are glucose (C6H12O6), oxygen (O2), CO2, H20, and Ethanol (C2H6O). As usual, they 
are encoded by pool elements.


![Metabolic_Machine](../figures/Metabolic_Machine_1.PNG "Courtesy of GoldSim")


Respiration and fermentation outflow glucose and oxygen into the CO2, H2O, and Ethanol pools. 
A function controls the fraction of respiration and fermentation according to the ratio of glucose
 to oxygen (eDAR, for electron donor to acceptor ratio): when the ratio is low, respiration 
dominates (catabolic environment), and when it is high, fermentation dominates (anaerobic 
environment). Conversely, photosynthesis outflows CO2 and H20 into the glucose and oxygen tanks. 
The photosynthetic active radiation (PAR) controls the rate of photosynthesis.

The limiting factors for this model are the demand of oxygen and the 



