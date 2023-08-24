---
layout: default
title: Population dynamics
parent: Model 6
grand_parent: Models
nav_order: 2
---

## Dynamical model

To model the lytic-lysogenic switch we add several mechanistic processes and two additional state variables: Lysogens ($$L$$) and Infected bacteria ($$I$$). Infected bacteria are those in the process of becoming either lysogens ($$L$$) or new phages via burst:

$$\begin{eqnarray*}                                                                                 
\frac{dB}{dt}&=& \underbrace{r_{max}H''_{eDAR}B}_{growth} - \underbrace{dBP}_{infection} \\         
\frac{dP}{dt}&=& \underbrace{c\big(1-P_L\big)\mu_pI}_{\text{lytic burst}} +\underbrace{c\mu_iL}_{\te
xt{induct growth}} - \underbrace{mP}_{decay} \\                                                     
\frac{dI}{dt}&=& \underbrace{dBP}_{infection} - \underbrace{P_LI}_{lysogenic} - \underbrace{\big(1-P
_L\big)L}_{lytic} \\                                                                                
\frac{dL}{dt}&=& \underbrace{r_{max}H''_{eDAR}L }_{growth} +                                        
\underbrace{P_LI}_{\text{new lysogens}} - \underbrace{\mu_iL}_{induction}
\frac{dN}{dt}&=& \underbrace{r_{max}H''_{eDAR}L }_{growth} +                                        
\underbrace{P_LI}_{\text{new lysogens}} - \underbrace{\mu_iL}_{induction}
\end{eqnarray*} $$




 
