---
layout: default
title: How to build this model
parent: Model 1
grand_parent: Models
nav_order: 1
---

## Brief instructions on how to build this model

### Step 1 -  Introduce a pool element

Pools (and stock elements, in general) encode state variables in GoldSim. This type of variables are the most important ones.
Select a pool element, change its name, fix the units to liters (l) and flow units to liters per hour (l/hr). Selecting units is an important step, since GoldSim enforces unit consistency.

### Step 2 -  Set upper bound for tank

Introduce a data element and set the upper bound to 30000 liters. As in the previous case, remember to set the units and name the data element properly ('Tank_capacity').

Open the Tank element and set the upper bound to 'Tank_capacity', the name of the data element.

### Step 3 - Pour water into the tank

Now we model a hose that fills the tank with water. We do this in four steps:

   1. Define a hose flow rate: introduce a new data element that sets the rate at which water flows into the tank. Name it properly and be careful with the units (because it is a rate, the units have to be liters per hour ($$l/hr$$).
   2. Define the time at which the hose switches off: this is another data element that we will call 'Time_hose_off'. The units in this case are going to be days ($$d$$) and we will fix the time at 2 days.
   3. Define a function: introduce an expression element with units of liters per hour ($$l/hr$$). In general, the units of a function should match the flow units of stock elements. Introduce the expression shown below.


   The expression above has the following meaning: if the time of the simulation is smaller than two days, the flow rate is equal to $$30 l/hr$$. Otherwise, it is 0. 'ETime' represents the simulation time of GoldSim. As you can see, the parentheses contains three instances separated by commas. These are the rules of GoldSim and in programming this is called [syntax](https://en.wikipedia.org/wiki/Syntax_(programming_languages))

   4. Now we need to connect this function to the pool. This is a very important step. Go to the Tank element, select the 'inflow' tab. Click 'add' and select the function defined before.


### Step 4 - Leakage



### Step 5 - Model settings



