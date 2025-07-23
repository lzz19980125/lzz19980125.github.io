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

##  Design Principles of Underwater Gliders
