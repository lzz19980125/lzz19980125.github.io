---
title: 'Gliding Motion Modeling and Energy Consumption Analysis for Underwater Glider'
date: 2025-07-20
category: Autonomous marine systems
permalink: /posts/2025-7-20-Gliding Motion Modeling and Energy Consumption Analysis for Underwater Glider
layout: single
classes: wide
excerpt: "This article includes the modeling of underwater glider motion and the analysis of energy consumption. <br/><img src='../images/2025-7-20-Gliding Motion Modeling and Energy Consumption Analysis for Underwater Glider.jpg'>"
tags:
  - Autonomous marine systems
  - Kinematics and kinetics
  - Motion planning

---

This article includes the modeling of underwater glider motion and the analysis of energy consumption.

# Preliminaries

## **Archimedes' Principle**

As early as middle school, we learned to explain the origin of buoyancy using **Archimedes' principle**:

> **An object submerged in a fluid (such as seawater) experiences an upward buoyant force equal to the weight of the fluid it displaces.**

The corresponding equation is:
 **F<sub>buoy</sub> = ρ<sub>fluid</sub> × g × V<sub>disp</sub>**

Where:

- ρ<sub>fluid</sub> is the density of seawater,
- *g* is the gravitational acceleration,
- V<sub>disp</sub> is the volume of seawater displaced by the object.

The vertical motion of an object in water depends on the relationship between **buoyancy** and **gravity**:

- When **buoyancy > weight**, the object rises.
- When **buoyancy < weight**, the object sinks.
- When **buoyancy = weight**, the object remains suspended.

In physics, the term *static buoyancy* typically refers to the buoyant force *F<sub>buoy</sub>* itself. However, in engineering applications—especially when discussing underwater gliders—we focus more on a derived concept: **net buoyancy**. The **net buoyant force** (*F<sub>net</sub>*) is defined as:

**F<sub>net</sub> = F<sub>buoy</sub> - G<sub>object</sub>**

Net buoyancy represents the resultant vertical force that determines whether the underwater vehicle ascends, descends, or hovers. Specifically:

- **F<sub>net</sub> > 0**: The net buoyant force is positive → the vehicle rises.
- **F<sub>net</sub> < 0**: The net buoyant force is negative → the vehicle sinks.
- **F<sub>net</sub> = 0**: The net buoyant force is zero → the vehicle hovers (or maintains a constant vertical velocity).

## Working Principle and Mechanism of Underwater Gliders

Underwater gliders control their vertical movement—descending and ascending—by adjusting their **net buoyancy**. Equipped with fixed wings, they convert vertical motion into horizontal glide using **hydrodynamic lift**. This method is highly energy-efficient: gliders **do not rely on continuously spinning propellers**, and consume only minimal energy when adjusting buoyancy or attitude. As a result, they can operate autonomously in the ocean for several months or even over a year, covering distances of thousands of kilometers.

<br/><img src='../images/2025-07-23_192552.jpg'>

To adjust net buoyancy, there are two main approaches:

- **Changing the displaced fluid volume** while keeping the mass constant.
- **Changing the mass** while keeping the displaced fluid volume constant.

The former typically involves **oil bladder systems** to modulate buoyancy, while the latter involves **taking in or expelling seawater** to vary the overall mass.

------

### 1. Variable Volume / Variable Displacement

This is the most common approach used in long-endurance underwater gliders such as **Slocum**, **Seaglider**, **Spray**, and **Petrel-L**.

- **Operating Principle**:
  - The glider's **total mass (m)** remains approximately constant.
  - It contains a **rigid high-pressure internal oil reservoir** and a **flexible external bladder**.
  - A **low-power hydraulic pump** transfers oil from the internal reservoir into the external bladder, increasing the **overall volume (V)** of the vehicle.
  - According to Archimedes' principle (F<sub>buoy</sub> = ρ<sub>seawater</sub> × g × V<sub>disp</sub>), an increase in displaced volume leads to increased buoyant force. When buoyancy exceeds gravity, the glider rises.
  - Conversely, by pumping oil back into the internal reservoir, the overall volume decreases, reducing buoyancy. When buoyancy is less than gravity, the glider sinks.
- **Advantages**:
  - **Low energy consumption**: Only a small amount of energy is needed to move oil, which is significantly more efficient than directly displacing water—especially under high-pressure deep-sea conditions.
  - **High precision**: The volume of oil transferred can be finely controlled.
  - **High reliability**: The hydraulic system is a **closed loop**, making it resistant to seawater corrosion and biofouling.

------

### 2. Variable Mass / Variable Ballast

This approach is more commonly found in other types of underwater vehicles, such as certain AUVs, underwater robots, or submarines.

- **Operating Principle**:
  - The glider's **overall volume (V)** remains approximately constant.
  - A **water pump system** draws seawater into an internal ballast tank or expels it back into the ocean.
  - When seawater is drawn in, the glider’s **total mass (m)** increases, resulting in greater gravitational force (G = m × g). When gravity exceeds buoyancy, the glider sinks.
  - When seawater is expelled, the total mass decreases, reducing gravity. When gravity is less than buoyancy, the glider rises.
- **Advantages**:
  - Allows for **large changes in net buoyancy**, potentially enabling **faster vertical motion**.
  - The working medium (seawater) is **abundant and readily available**.
- **Disadvantages**:
  - **Higher energy consumption**: Especially at great depths, high-pressure pumps are required to expel seawater, leading to significant energy usage.
  - **Vulnerability to corrosion and clogging**: Seawater is corrosive, and marine microorganisms or particles may clog pipes or pumps, affecting system reliability.

[![IMAGE ALT TEXT HERE](../images/2025-07-23_194339.jpg)](https://www.youtube.com/watch?v=dlaiIqyl8MU)
