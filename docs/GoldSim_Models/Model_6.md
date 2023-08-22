---
layout: default
title: Model 6
nav_order: 6
parent: Models
---

## Model 6 - The switch

[Download](https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/GoldSim_Models/Model6_eDAR_switch_model.gsm){: .btn }

If you find this model useful for your own research, please remember to [cite us](https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/CITATION.cff){: .btn .btn-purple }

This model simulates a mechanism for the lytic/lysogenic switch as a function of metabolism. Metabolism in this case is represented by the **e**lectron **D**onor to **A**cceptor 
**R**atio or eDAR. 

### eDAR and the switch

As a firs approximation, suppose that the only electron donors and acceptors in our system are glucose and oxygen and that the main metabolic pathway is cellular respiration.
 Then, we have:

$$
\begin{equation}
   eDAR=6\frac{C_{6}H_{12}O_6}{O_2} \, ,
\end{equation}
$$

where the factor 6 accounts for the stoichiometry of cellular respiration.