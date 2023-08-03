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

This part of the model  simulates three simplified metabolic 
processes: respiration, fermentation, and photosynthesis. The central state variables are glucose
 (C6H12O6), oxygen (O2), CO2, H20, and Ethanol (C2H6O). As usual, they 
are encoded by pool elements.


![Metabolic_Machine](../figures/Metabolic_Machine_1.PNG "Courtesy of GoldSim")


Respiration and fermentation outflow glucose and oxygen into the CO2, H2O, and Ethanol pools through 
different functions. One of those functions controls the fraction of respiration and fermentation according
 to the ratio of glucose to oxygen (eDAR, for electron donor to acceptor ratio): when the ratio is low, 
respiration dominates (catabolic environment), and when it is high, fermentation dominates (anaerobic 
environment). The demand for glucose and oxygen is set by a population of bacteria.

![Metabolic_Machine](../figures/Metabolic_Machine_2.PNG "Courtesy of GoldSim")


Conversely, photosynthesis outflows CO2 and H20 into the glucose and oxygen tanks. 
The photosynthetically active radiation (PAR) limits the rate of photosynthesis. 
[PAR](https://en.wikipedia.org/wiki/Photosynthetically_active_radiation) is the range of wavelengths 
from solar radiation that photosynthetizers can process. It is typically measured in moles of photons 
per area and time. PAR data for this model was obtained from [Ge et al](https://doi.org/10.1007/s00704-010-0368-6).

The PAR modeling follows several steps:

1. Convert PAR Index from $$mole/m^2 h$$ to $$J/m^2 h$$ using Avogadro's number and the following equation 
to calculate the energy of a photon $$\nu$$: $$E_{nu}=\frac{h c}{\lambda}$$, where $$h$$ is planck's constant, $$c$$ is 
the speed of light, and $$\lambda$$ is the wavelength of the photon. In our case, we considered $$\lambda=550 nm$$.

2. Set the area of photosynthetic biomass to extract power. In our case it was $$1 m^2$$.

3. Integrate power over time to extract energy (not strictly necessary)

4. Estimate the maximum amount of $$CO_2$$ that can be metabolized in an hour. Divide power over an hour by
the activation energy for photosynthesis (this gives the number of cycles of photosynthesis)
 and multiply by the weight of six molecules of $$CO_2$$.

5. If the power supplied by PAR in an hour is less than the activation energy for photosynthesis, no $$CO_2$$ is metabolized.

6. If the power demanded by the photosynthetic biomass is higher than the power supplied by PAR, only metabolize the maximum
$$CO_2$$ allowed by PAR.

7. This determines the outflow of the pool of $$CO_2$$ and the outflow of the $$H_2O$$ pool by stoichiometry.

![Metabolic_Machine](../figures/Metabolic_Machine_3.PNG "Courtesy of GoldSim")


