---
layout: default                                                                                     
title: Derivations                                                                              
parent: 6 - The Switch                                                                                    
grand_parent: Models                                                                                
nav_order: 7
header-includes:
    - \usepackage[colorlinks=false, allcolors=blue]{hyperref}
---

### Maximum value of modified Hill functions

The modified Hill function reads:

$$\begin{equation*}
 H'(eDAR)=\frac{(eDAR - eDAR_{min})^{n}}{K^n + \alpha (eDAR - eDAR_{min})^{n}} \, .
\end{equation*} $$

With

$$\begin{equation*}
\alpha=\frac{(eDAR_{max} - eDAR_{min})^{n} - 2(1 - eDAR_{min})^{n}}{(eDAR_{max}- eDAR_{min})\
^{n} - (1 - eDAR_{min})^{n}}
\end{equation*}$$

and

$$\begin{equation*}
K=(2-\alpha)^{1/n}(1-eDAR_{min})
\end{equation*}$$

Here, we prove that $$H'(eDAR=eDAR_{max})=1$$. For the sake of simplicity let us introduce some compact notation:

$$\begin{eqnarray*}
eDAR - eDAR_{min}&=&\Delta \\
eDAR_{max} - eDAR_{min}&=&\Delta_{tot} \\
1 - eDAR_{min}&=&\Delta_{1}
\end{eqnarray*}$$

Then we have that:

$$\begin{equation*}
K^n=\frac{\Delta^n_{tot} \Delta^n_{1} }{\Delta^n_{tot} - \Delta^n_{1}}
\end{equation*}$$

And the modified Hill function reads now:

$$\begin{equation*}                                                                                 
H'(eDAR)=\frac{\Delta^n}{\frac{\Delta^n_{tot} \Delta^n_1 + (\Delta^n_{tot} - 2
\Delta^n_1) \Delta^n}{\Delta^n_{tot} - \Delta^n_1}}= \frac{(\Delta^n_{tot} - \Delta^n_1)\Delta^n}{\Delta^n_{tot} \Delta^n_1 + (\Delta^n_{tot} - 2 \Delta^n_1) \Delta^n}
\end{equation*}$$

If $$eDAR=eDAR_{max}$$, then $$\Delta=\Delta_{tot}$$ which gives $$H'(eDAR=eDAR_{max})=1$$.

Alternatively, if $$eDAR=1$$, then $$\Delta=Delta_1$$, which gives $$H'(eDAR=1)=0.5$$. 

### Equilibrium analysis

The equilibrium analysis is done by taking the ODEs and setting them to zero:

$$\begin{eqnarray}  
\frac{dB}{dt}&=&0; \underbrace{r_{max}H''_{eDAR}B}_{growth} - \underbrace{dBP}_{infection}& = &0 \\
\frac{dP}{dt}&=&0; \underbrace{c\big(1-P_L\big)\mu_pI}_{\text{lytic burst}} +
\underbrace{c\mu_iL}_{\text{induct growth}} - \underbrace{mP}_{decay} - \underbrace{dBP}_{infection} &=& 0 \\                         
\frac{dI}{dt}&=&0;  \underbrace{dBP}_{infection} - \underbrace{\mu_p I}_{lysogenic+burst}& =& 0 \\  
\frac{dL}{dt}&=&0; \underbrace{(r_{max}H''_{eDAR} - \mu_i)L }_{\text{effective growth}} +  \underbrace{\mu_p P_LI}_{\text{new lysogens}} &=&0
\label{eq:equilibrium} \end{eqnarray}$$

From Eq. \ref{eq:equilibrium} .(1) we get:

$$\begin{equation}
P^{*}=\frac{rH''}{d}
\label{eq:phage_eq} \end{equation}$$

From Eq. \ref{eq:equilibrium} .(3) we have:

$$\begin{equation}
dBP=\mu_p I
\label{eq:infected_sensitive} \end{equation}$$

Substituting Eq. \ref{eq:infected_sensitive} in Eq. \ref{eq:equilibrium} .(2):

$$\begin{equation}
I^{*}=\frac{1}{c(1 - \mu_p P_L) - \mu_p} \big[ m P^{*} - c \mu_i L^*\big]
\label{eq:lysogens_1} \end{equation}$$

From Eq. \ref{eq:equilibrium} .(4):

$$\begin{equation}
I^{*}=\frac{\mu_i - rH''}{\mu_p P_L} L^*
\label{eq:lysogens_2} \end{equation}$$

Putting Eq. \ref{eq:lysogens_1} and Eq. \ref{eq:lysogens_2} together and rearranging terms, we get the equilibrium concentration of lysogens:

$$\begin{equation}
L^{*}=\frac{m \mu_p P_L r H''}{d[c(\mu_i - r H'' (1 - \mu_p P_L) + \mu_p (r H'' - \mu_i)]}
\label{eq:lysogens_eq} \end{equation}$$

Getting the equilibrium concentration of infected bacteria $$I^*$$ from Eq. \ref{eq:lysogens_eq} is straightforward:

$$\begin{equation}
I^{*}=\frac{\mu_i - r H''}{\mu_p P_L} L^* .
\label{eq:infected_eq} \end{equation}$$

Similarly, for the equilibrium concentration of sensitive bacteria $$B^*$$:

$$\begin{equation}
B^{*}=\frac{\mu_p}{r H''} I^* .
\end{equation} \label{eq:sensitive_eq}$$


