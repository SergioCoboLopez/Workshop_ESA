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