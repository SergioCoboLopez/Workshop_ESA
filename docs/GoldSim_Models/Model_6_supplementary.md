---                   
layout: default                                                                                     
title: Derivations                                                                              
parent: Model 6                                                                                     
grand_parent: Models                                                                                
nav_order: 7                                                      
---

### Maximum value of modified Hill functions

The modified Hill function reads:

$$\begin{equation*}
 H'(eDAR)=\frac{(eDAR - eDAR_{min})^{n}}{K^n + \alpha (eDAR - eDAR_{min})^{n}} \,
\end{equation*} $$
with

$$\begin{equation*}
\alpha=\frac{(eDAR_{max} - eDAR_{min})^{n} - 2(1 - eDAR_{min})^{n}}{(eDAR_{max}- eDAR_{min})\
^{n} - (1 - eDAR_{min})^{n}}
\end{equation*}$$

and

$$\begin{equation*}
K=(2-\alpha)^{1/n}(1-eDAR_{min})
\end{equation*}$$

Here, we prove that $$H'(eDAR=eDAR_{max})=1$$