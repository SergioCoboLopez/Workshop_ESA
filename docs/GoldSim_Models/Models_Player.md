---
layout: default
title: Models
nav_order: 4
has_children: true
permalink: docs/GoldSim_Models
---

Remember that GoldSim offers two very good [free courses](https://www.goldsim.com/Web/Customers/Education/Overview/) and other [learning resources](https://www.goldsim.com/Web/Customers/). There is also an active [community of users](https://www.goldsim.com/Web/Customers/Community/)

# Models

This section covers a series of models specific for the workshop at the [ESA Annual Meeting](https://esa.org/portland2023/) of 2023. 
---

## Model 1 - Example

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/GoldSim_Models/Model1_Example.gsm> 

Video: <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/data/videos>

Link to video: <https://www.youtube.com/watch?v=htNLMYaaiCE>

This model is a simple example provided by GoldSim in their basic course and can be found [here](https://www.goldsim.com/Courses/BasicGoldSim/Unit3/Lesson2/). The model exploits the analogy of a water management system to describe
a simple scenario and show the basic elements used in GoldSim. 

## Model 2 - Example ecology. 

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/GoldSim_Models/Model2_Example_Ecology.gsm>

Video: <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/data/videos>

Link to video: <https://www.youtube.com/watch?v=imbY64YM3fE>

You might be asking yourself how water management systems can help describe ecological models. This model gives you a basic answer. Model 2 is a modified version of Model 1 that describes a simulated experiment with bacterial
exponential growth (inflow) and bacterial sampling (outflow).

1. The tank of water becomes now the concentration of bacteria. This is the [state variable](https://en.wikipedia.org/wiki/State_variable) that describes the overall state of our system. Because bacteria are usually measured in concentrations, the 'bacterial tank' units are now 'items/ml' (usually, density is measured in 'cells/ml,' but GoldSim does not provide 'cell' as a standard unit). Remember that GoldSim is very consistent with units.

2. The tank capacity becomes the carrying capacity, the maximum concentration of bacteria in a system.

3. The 'inflow' of bacteria comes from bacterial exponential or Malthusian growth. That is, the bacterial growth is proportional to the actual concentration of bacteria. The time at which the hose switches off is the experiment time.

4. The outflow is reinterpreted as a sampling rate: an extraction of 15% of the total bacterial concentration every hour.

5. This model has a smaller timescale and simulation time.

## Model 3 - Bacterial growth

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/GoldSim_Models/Bacterial_growth.gsm>

This model is a refinement of the previous model. 
The first thing that you will notice when you open it is the existence of a new element that we have not discussed yet:
![Containers1](../figures/Containers_1.png "Courtesy of GoldSim")
Image courtesy of GoldSim

The three yellow elements are called [containers](https://www.goldsim.com/Courses/BasicGoldSim/Unit9/Lesson2/). Containers are used to store small parts of the models for esthetical reasons (not having lots of elements scattered around your workspace) or because you want to build a modular model, where each part of the model is as independent as possible from the rest. 

Notice the red marker on the top left corner of the containers:
![Containers2](../figures/Containers_2.png "Courtesy of GoldSim")
Image courtesy of GoldSim

These indicate that containers are localized. When a container is localized, the elements inside are hidden from the elements of the rest of the model. In this case, each container contains a different version of a model for bacterial growth:

### Exponential Model

If you go to the 'Exponential_Growth' container, you will see this model:

![Growth model 1](../figures/Bacterial_growth_exponential.png "Courtesy of GoldSim")
Image courtesy of GoldSim

This model is not very different from Model 2. In this case, there is no carrying capacity. The bacterial pool includes an upper bound of $1e20$ items/ml to prevent GoldSim from reaching
 very high concentrations and using too much memory. There is also a link to the paper that has the growth rate of *E. Coli*.

Remember GoldSim implicitly models differential equations. This is the equation for the exponential growth in this model:

$$\begin{equation*}
\frac{dB}{dt}=rB
\end{equation*}$$

|Letter|Element|Units  |
|----|----------|-------|
|    B|Bacteria    |items/ml  |
|dB/dt|Growth      |items/ml h|
|r    |Growth rate |1/h       |

### Logistic Model

If you go to the 'Exponential_Growth' container, you will see this model:

![Growth Model 2](../figures/Bacterial_growth_logistic.png "Courtesy of GoldSim")
Image courtesy of GoldSim

You will probably notice a new element that we had not discussed before:

![Growth Model 2](../figures/Dashboard.png "Courtesy of GoldSim")
Image courtesy of GoldSim

This a 'DashBoard'. DashBoards are extensively discussed in [Unit 16](https://www.goldsim.com/Courses/BasicGoldSim/Unit16/Lesson1/) 
of the [GoldSim Introduction Course](https://www.goldsim.com/Courses/BasicGoldSim/), but shortly speaking, a DashBoard is a special type of container that allows you to generate 
[GoldSim Player files](https://www.goldsim.com/Courses/BasicGoldSim/Unit16/Lesson4/), like the ones discussed below. You can open and run GoldSim Player files without a license.

Back to the model, this is a reformulation of Model 2, where the carrying capacity is explicitly implemented in the 'Logistic_growth' function, as shown below:

![Growth Model 3](../figures/growth_function.png "Courtesy of GoldSim")
Image courtesy of GoldSim

This simply makes the model closer to its mathematical formulation, and does not imply the previous model was wrong.
Another difference respect to the previous model is that there is no data element for finishing the experiment. This is not strictly necessary, as it is possible to stop the simulation at any time you wish in 
the Simulations settings.

This is the equation for the exponential growth in this model:

$$\begin{equation*}
\frac{dB}{dt}=r(1-B/K)B
\end{equation*}$$


|Letter|Element     |Units     |
|----|----------|-------|
|    B|Bacteria    |items/ml  |
|dB/dt|Growth      |items/ml h|
|r    |Growth rate |1/h       |
|K    |Carrying capacity |items/ml|


### Logistic Model Stochastic

Finally, we model a bacterial growth with stochastic bacterial growth rate, carrying capacity and initial bacterial concentration are stochastic variables. Stochastic processes are very commont in ecology; think about it: Is the
 initial concentration of bacteria in an experiment fixed or is there some uncertainty due to measurements errors? The same is probably true for the growth rate and the carrying capacity: 
are these unique and fixed rates? Or do they vary between minimum and maximum values depending on environmental or genetic conditions? For instance, some bacterial cells might have been selected to grow faster than others. Or 
maybe a rich media provides resources for a higher carrying capacity. GoldSim allows us to explore these scenarios and this model provides a simple example of it. 

![Growth Model 4](../figures/Bacterial_growth_logistic_stochastic.png "Courtesy of GoldSim")
Image courtesy of GoldSim

Here we find a new element, which is crucial to stochastic modeling: the 'Stochastic':

![Growth Model 5](../figures/Stochastic_1.PNG "Courtesy of GoldSim")
Image courtesy of GoldSim

If you click on the 'Edit' button, you can see how to define the stochastic element:

![Growth Model 6](../figures/Stochastic_2.PNG "Courtesy of GoldSim")
Image courtesy of GoldSim

In particular, there are many probability distributions that the parameter can take. In this case, we considered the [normal distribution](https://en.wikipedia.org/wiki/Normal_distribution). Normal or Gaussian distributions have a 
mean or expectation value $$\mu$$ that represents the most common outcome. As you move away from the mean, the likelihood of values occurring decreases. The standard deviation $$\sigma$$ represents how spread the distribution is.
The height distribution of adults follows a [normal distribution](https://ourworldindata.org/human-height#distribution-of-adult-heights).


## Model 4 - Lotka-Volterra

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/blob/main/GoldSim_Models/Lotka_Volterra.gsm>

The next model is a Lotka-Volterra predator-prey model for bacteria and bacteriophage.

The equations for Lotka-Volterra model are shown below:

$$\begin{eqnarray*}
\frac{dB}{dt}&=&rB - aBP \\
\frac{dP}{dt}&=&caBP - mP
\end{eqnarray*}$$


|Letter|Element     |Units  |
|----|----------|-------|
|    B|Bacteria    |items/ml|
|    P|Phage    |items/ml  |
|r    |Growth rate |1/h    |
|a    |Adsorption rate |ml/h|
|c    |Burst size |items    |
|m    |Decay rate |1/h|

## Model 5 - Lysogeny model



## GoldSim Player files
In the event that you cannot access or use GoldSim, I have provided three player files. GoldSim player files can be run with GoldSim player, but they cannot be edited.

### Model 1 - Logistic bacterial growth

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files/Bacterial_growth.gsp>

This file can be found in the [repository](https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files) under the name Bacterial_growth.gsp.
The model simulates the bacterial growth of three bacterial strains using values found in the literature. In the player file, you can select several parameters to play around.

### Model 2 - Stochastic bacterial growth

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files/Bacterial_growth_stochastic.gsp>

This file can be found under the name Bacterial_growth_stochastic.gsp.
In this model I introduced stochasticity to account for variables that cannot be controled in experimental settings: the bacterial growth rate is not a fixed number, but an average depending on different factors. The same applies to the carrying capacity.

### Model 3 - Lotka Volterra

Model: <https://github.com/SergioCoboLopez/Workshop_ESA/tree/main/GoldSim_Models/Player_Files/Lotka_Volterra_Dashboard.gsp>

This file can be found under the name Lotka_Volterra.gsp.

In this model, I simulate a predator-prey model for bacteria and virulent phage with Lotka-Volterra equations. The model comprises for ecological mechanisms: exponential bacterial growth, infection of bacteria by phages, phage growth by burst, and phage decay.

---
