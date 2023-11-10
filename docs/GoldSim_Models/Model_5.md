---
layout: default
title: Model 5 - The Metabolic Machine
nav_order: 5
parent: Models
has_children: true
---

## The Metabolic Machine

[Download](https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/GoldSim_Models/Model5_Metabolic_Machine.gsm){: .btn }


If you find this model useful for your own research, please remember to [cite us](https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/CITATION.cff){: .btn .btn-purple }

This model simulates bacterial growth based on metabolism and energy production. The model consists of three parts stored in their corresponding containers: Metabolism, Energy production, and Bacterial growth.

### Metabolism

The Metabolic container simulates three simplified metabolic processes: respiration, fermentation, and photosynthesis. The state variables of this part of the model are: glucose
 (C6H12O6), oxygen (O2), CO2, H20, and Ethanol (C2H6O). 
Bacteria perform respiration and fermentation and photosynthesis is carried out by a generic non-explicitly modeled primary producer (algae). The function eDAR (the ratio of glucose to O$$_2$$) controls the ratio of respiration and fermentation
carried out by bacteria.

The technical details of this part of the model are discussed in the corresponding section: 

[Metabolism](https://sergiocobolopez.github.io/Workshop_ESA/GoldSim_Models/Model_5%20-%20Metabolism.html){: .btn }

