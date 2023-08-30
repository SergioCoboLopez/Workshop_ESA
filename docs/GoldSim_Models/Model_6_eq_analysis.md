---
layout: default
title: Equilibrium Analysis
parent: Model 6
grand_parent: Models
nav_order: 3
---

## Equilibrium analysis

Let us for the sake of simplicity rearrange the equation shown in the previous section:

$$\begin{eqnarray}  
\frac{dB}{dt}&=& \underbrace{r_{max}H''_{eDAR}B}_{growth} - \underbrace{dBP}_{infection} \\         
\frac{dP}{dt}&=& \underbrace{c\big(1-P_L\big)\mu_pI}_{\text{lytic burst}} +
\underbrace{c\mu_iL}_{\text{induct growth}} - \underbrace{mP}_{decay} -\underbrace{dBP}_{infection} \\                         
\frac{dI}{dt}&=& \underbrace{dBP}_{infection} - \underbrace{\mu_p I}_{lysogenic+burst} \\  
\frac{dL}{dt}&=& \underbrace{(r_{max}H''_{eDAR} - \mu_i)L }_{\text{effective growth}} +  \underbrace{\mu_p P_LI}_{\text{new lysogens}} 
\end{eqnarray} $$

We set all equations equal to zero to obtain the equilibrium conditions. The equilibrium concentrations are:

$$\begin{eqnarray}
B^{*}&=&\frac{\mu_p}{r H''} I^{*} \\
P^{*}&=&\frac{r H''(eDAR)}{d} \\
I^{*}&=&\frac{\mu_i - r H''}{\mu_p P_L} L^*\\
L^{*}&=&\frac{m \mu_p P_L r H''}{d[c(\mu_i - r H'' (1 - \mu_p P_L) + \mu_p (r H'' - \mu_i)]}
\end{eqnarray}$$


The derivations section provides more detain on how to obtain these concentrations.




 
