---
layout: default
title: Population dynamics
parent: 6 - The Switch
grand_parent: Models
nav_order: 2
---

## Dynamical model

To model the lytic-lysogenic switch we add several mechanistic processes and two additional state variables: Lysogens ($$L$$) and Infected bacteria ($$I$$). Infected bacteria are those in the process of becoming either lysogens ($$L$$) or new phages via burst:

$$\begin{eqnarray}                                                                                 
\frac{dB}{dt}&=& \underbrace{r_{max}H''_{eDAR}B}_{growth} - \underbrace{dBP}_{infection} \label{eq:sensitive} \\         
\frac{dP}{dt}&=& \underbrace{c\big(1-P_L\big)\mu_pI}_{\text{lytic burst}} +
\underbrace{c\mu_iL}_{\text{induct growth}} - \underbrace{mP}_{decay} \\                         
\frac{dI}{dt}&=& \underbrace{dBP}_{infection} - \underbrace{\mu_p P_LI}_{lysogenic} - \underbrace{\mu_p\big(1-P_L\big)I}_{lytic} \label{eq:infected} \\  
\frac{dL}{dt}&=& \underbrace{r_{max}H''_{eDAR}L }_{growth} +                                        
\underbrace{\mu_p P_LI}_{\text{new lysogens}} - \underbrace{\mu_iL}_{induction} \\
\frac{dN}{dt}&=& \underbrace{r_{max}H''_{eDAR}(L+ B)}_{growth} + \underbrace{\mu_p P_LI}_{\text{new lysogens}} - \underbrace{\mu_iL}_{induction} \, ,
\end{eqnarray} $$

where $$B$$, $$I$$, and $$L$$ represent the concentrations of sensitive bacteria, infected bacteria, and lysogens, respectively. $$N$$ is a virtual state variable representing the total bacterial population $$N=B+I+L$$ and $$P$$ is the concentration of phages.

### B: Sensitive bacteria

The rate of sensitive bacteria is subject to two processes: (exponential) growth and density-dependent infection by phages.

1. Growth: $$r_max H''_{eDAR}$$.
The bacterial growth is controlled by maximum growth rate $$r_max$$ that depends on the bacterial strain and the function $$H''_{eDAR}$$, a modified Hill Function. $$H''_{eDAR}$$ is also a function of eDAR and takes values between 1 (fully catabolic system) and 2 (fully anabolic system) (see [eDAR and switch](https://sergiocobolopez.github.io/Workshop_ESA/GoldSim_Models/Model_6_edar_switch.html) ).

2. Infection: $$dBP$$.
The infection is a function of the density of phages and bacteria (hence density-dependent) and the infection or adsorption rate $$d$$.

### P: Phages

Three processes control the rate of phage concentration: lytic burst, induction growth, and phage decay.

1. Lytic burst: $$c\big(1-P_L\big)\mu_pI$$
This term represents the reproduction of phages through lysis of infected bacteria $$I$$. Phages lyse infected bacteria $$I$$ with a probability $$1 - P_L$$ ($$P_L$$ is the probability of lysogeny). For every lysed bacteria, $$c$$ phages reproduce. This process occurs at a rate of $$\mu_p$$.

2. Induction growth: $$c\mu_iL$$
This term represents the phage reproduction via lysogenic induction, which occurs at a rate of $$\mu_i$$.

3. Phage decay: $$mP$$
Phages decay at a rate of $$m$$

### I: Infected bacteria

This is the equation where the switch really operates. The rate of infected bacteria is governed by three processes: infection, lysogenic decision, and lytic decision.

1. Infection: $$dBP$$
This term simply implies that the sensitive bacteria infected Eq. \ref{eq:sensitive} become infected.


 
