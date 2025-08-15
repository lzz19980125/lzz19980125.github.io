---
title: 'Hydrodynamic Analysis of Underwater Gliders'
date: 2025-08-16
category: Autonomous marine systems
permalink: /posts/2025-8-16-Hydrodynamic Analysis of Underwater Gliders
layout: single
classes: wide
excerpt: "This article presents a fundamental hydrodynamic analysis of underwater gliders. <br/><img src='../images/Archimedes.jpg'>"
tags:
  - Autonomous marine systems
  - Kinematics and kinetics
  - Motion planning

---



## Introduction

In our [previous post on Kinetics](https://lzz19980125.github.io/posts/2025-8-2-Kinetics%20Analysis%20of%20Underwater%20Gliders), we derived the rigid-body equations of motion, which describe how a vehicle's inertia resists acceleration. The result was the foundational equation: 

$$M_{RB} \dot{\nu} + C_{RB}(\nu) \nu = \tau$$

The term on the right, $$\tau$$, represents the sum of *all* external forces and moments acting on the vehicle. This is where the real-world physics of the marine environment comes into play. To build a complete and useful dynamic model, we must systematically define each component of $$\tau$$.

This article tackles the first and most fundamental of these external forces: **hydrostatics**. We will derive the 6-DOF generalized restoring force vector, denoted as $$g(\eta)$$, which arises from the interplay between gravity and buoyancy. This vector is a cornerstone of marine vehicle simulation, stability analysis, and control design. 

## 1. The Two Pillars of Hydrostatics: Gravity and Buoyancy

For any vehicle submerged in a fluid, two constant, opposing forces are always at play:

*   **Gravitational Force (W):** The force exerted by gravity on the vehicle's total mass ($$m$$). It always acts vertically downwards through a single point.
    *   **Magnitude:** $$W = mg$$
    *   **Point of Action:** The **Center of Gravity (CG)**, the mass-weighted average position of the vehicle.

*   **Buoyancy Force (B):** The upward force exerted by the fluid, equal to the weight of the fluid displaced by the vehicle's volume ($$\nabla$$). According to Archimedes' principle, it always acts vertically upwards through a single point.
    *   **Magnitude:** $$B = \rho g \nabla$$, where $$\rho$$ is the fluid density.
    *   **Point of Action:** The **Center of Buoyancy (CB)**, the geometric centroid of the vehicle's submerged volume.

<br/><img src='../images/Hydrostatics of Submerged Vehicles.jpg' alt='Forces on a Submarine'>
*Figure 1: The fundamental forces of gravity (acting at CG) and buoyancy (acting at CB) on a submerged vehicle.*

When a vehicle is in a stable, upright position, these two forces are perfectly aligned along the same vertical axis. However, if the vehicle tilts (rolls or pitches), the CG (fixed to the rigid body) stays put, but the CB (the center of the displaced volume) can move. This misalignment creates a **moment** that attempts to "restore" the vehicle to its upright position. It is this behavior that earns gravity and buoyancy the collective title of **restoring forces**.

Our goal is to mathematically capture the combined effect of these two forces as a single 6-DOF vector $$g(\eta)$$ that depends on the vehicle's orientation.

## 2. Step 1: Defining Forces in the World (NED Frame)

To begin our derivation, we first express the forces in the simplest possible reference frame: the non-accelerating, inertial **North-East-Down (NED) frame `{n}`**. In this frame, "down" is aligned with the direction of gravity.

*   The gravity vector $$f_g^n$$ acts purely in the positive z-direction (Down).
    $$
    f_g^n = \begin{bmatrix} 0 \\ 0 \\ W \end{bmatrix}
    $$

*   The buoyancy vector $$f_b^n$$ acts purely in the negative z-direction (Up).
    $$
    f_b^n = \begin{bmatrix} 0 \\ 0 \\ -B \end{bmatrix}
    $$

This representation is physically intuitive but not directly usable in our vehicle's equations of motion, which are formulated in the moving **BODY frame `{b}`**.

## 3. Step 2: Transforming Forces into the Vehicle's Perspective (BODY Frame)

To use these forces in our dynamic model, we must transform them from the NED frame `{n}` into the BODY frame `{b}`. This transformation is achieved using the **rotation matrix** $$R(\Theta_{nb})$$, which describes the orientation (roll $$\phi$$, pitch $$\theta$$, yaw $$\psi$$) of the body relative to the NED frame. The transformation from NED to BODY is given by the transpose of this matrix, $$R^T(\Theta_{nb})$$.

The transformation rule is: $$ f^b = R^T(\Theta_{nb}) f^n $$.

Applying this to our forces:

*   **Gravity in the BODY frame:**
    $$
    f_g^b = R^T(\Theta_{nb}) f_g^n = W \begin{bmatrix} -\sin(\theta) \\ \cos(\theta)\sin(\phi) \\ \cos(\theta)\cos(\phi) \end{bmatrix}
    $$

*   **Buoyancy in the BODY frame:**
    $$
    f_b^b = R^T(\Theta_{nb}) f_b^n = -B \begin{bmatrix} -\sin(\theta) \\ \cos(\theta)\sin(\phi) \\ \cos(\theta)\cos(\phi) \end{bmatrix}
    $$

The total hydrostatic force acting on the body is the sum of these two vectors:

$$
f_{total}^b = f_g^b + f_b^b = (W-B) \begin{bmatrix} -\sin(\theta) \\ \cos(\theta)\sin(\phi) \\ \cos(\theta)\cos(\phi) \end{bmatrix}
$$

This vector represents the first three components of our final restoring force model.

## 4. Step 3: Calculating the Restoring Moments

The forces $$f_g^b$$ and $$f_b^b$$ do not, in general, act at the origin of the BODY frame (the Coordinate Origin, CO). Therefore, they produce moments. The moment generated by a force $$F$$ acting at a point located by vector $$r$$ from the origin is given by the cross product $$ \tau = r \times F $$.

Let's define the position vectors for the CG and CB relative to the CO in the BODY frame:

*   **Vector to Center of Gravity:** $$r_{bg}^b = [x_g, y_g, z_g]^T$$
*   **Vector to Center of Buoyancy:** $$r_{bb}^b = [x_b, y_b, z_b]^T$$

The total restoring moment about the CO is the sum of the moments from gravity and buoyancy:

$$
m_{total}^b = (r_{bg}^b \times f_g^b) + (r_{bb}^b \times f_b^b)
$$

This expression is the source of the most complex terms in our hydrostatic model.

## 5. The Grand Finale: The 6-DOF Restoring Force Vector $$g(\eta)$$

In the standard formulation of the marine craft equations of motion, hydrostatic effects are moved to the left-hand side and represented by the vector $$g(\eta)$$. This means we must take the negative of the total forces and moments we just derived.

$$
g(\eta) = - \begin{bmatrix} f_{total}^b \\ m_{total}^b \end{bmatrix} = - \begin{bmatrix} f_g^b + f_b^b \\ (r_{bg}^b \times f_g^b) + (r_{bb}^b \times f_b^b) \end{bmatrix}
$$

By substituting our expressions for the forces and meticulously calculating the cross products for the moments, we arrive at the complete 6-DOF generalized restoring force vector:

$$
g(\eta) =
\begin{bmatrix}
(W-B)\sin(\theta) \\
-(W-B)\cos(\theta)\sin(\phi) \\
-(W-B)\cos(\theta)\cos(\phi) \\
-(y_g W - y_b B)\cos(\theta)\cos(\phi) + (z_g W - z_b B)\cos(\theta)\sin(\phi) \\
(z_g W - z_b B)\sin(\theta) + (x_g W - x_b B)\cos(\theta)\cos(\phi) \\
-(x_g W - x_b B)\cos(\theta)\sin(\phi) - (y_g W - y_b B)\sin(\theta)
\end{bmatrix}
$$

This equation is the primary result of our analysis. It provides a complete description of the hydrostatic forces and moments on any underwater vehicle, given its weight, buoyancy, CG/CB locations, and its orientation in the water.

## 6. Simplification and Physical Insight

The full equation is complex, but it simplifies beautifully under common assumptions, revealing deep physical truths about vehicle stability.

#### Case 1: Neutrally Buoyant Vehicles ($$W=B$$)

For most AUVs and ROVs, the design goal is neutral buoyancy. In this case, $$W-B=0$$.

*   **Forces:** The first three rows of $$g(\eta)$$ become zero. This makes perfect sense: a neutrally buoyant object experiences no net hydrostatic force and will not sink or rise on its own.
*   **Moments:** The moment equations simplify. For example, the term $$(y_g W - y_b B)$$ becomes $$W(y_g - y_b)$$. We can define a vector from the CB to the CG, $$r_{bg} = [BG_x, BG_y, BG_z]^T = [x_g-x_b, y_g-y_b, z_g-z_b]^T$$. The moment equations become functions of this single vector and the vehicle's weight.

#### Case 2: Symmetric Vehicles (CG and CB on the Same Vertical Axis)

Many underwater vehicles are designed with a high degree of symmetry, such that the CG and CB lie on the same vertical line when the vehicle is upright. In the BODY frame, this means $$x_g = x_b$$ and $$y_g = y_b$$, or $$BG_x = 0$$ and $$BG_y = 0$$.

Applying this to the neutrally buoyant case, the $$g(\eta)$$ vector collapses dramatically:

$$
g(\eta) = \begin{bmatrix} 0 \\ 0 \\ 0 \\ (W \cdot BG_z) \cos(\theta)\sin(\phi) \\ (W \cdot BG_z) \sin(\theta) \\ 0 \end{bmatrix}
$$

This simplified form provides a powerful insight:

> For a symmetric, neutrally buoyant vehicle, its static roll and pitch stability is determined *entirely* by the vertical separation between the Center of Gravity and the Center of Buoyancy ($$BG_z = z_g - z_b$$).

For the vehicle to be passively stable (i.e., to right itself after being disturbed), the restoring moments must oppose the roll and pitch angles. This requires the term $$W \cdot BG_z$$ to be positive. Since $$W$$ is positive, we must have **$$BG_z > 0$$, which means the CG must be located *below* the CB**. This fundamental design principle is the reason heavy components like batteries are placed at the bottom of underwater vehicles.

## Conclusion and What's Next

We have journeyed from the first principles of gravity and buoyancy to a complete 6-DOF hydrostatic model, $$g(\eta)$$. This vector is an essential component of any high-fidelity marine vehicle simulation. Through simplification, we also uncovered the critical design rule for passive stability: keep the center of gravity below the center of buoyancy.

However, relying solely on passive stability is often not enough, especially for vehicles that undergo significant changes in payload or need to maintain a specific trim angle. To achieve this, vehicles are equipped with systems to *actively* manage their weight and buoyancy distribution.

In the next part of this series, we will explore the dynamics and control of **Ballast Systems**. We will model the $$g_0$$ term in the equation of motion, which represents the forces and moments generated by actively pumping water between internal tanks. This will bridge the gap from static analysis to the practical engineering of trim and buoyancy control.



## References

[1] T. I. Fossen, *Handbook of Marine Craft Hydrodynamics and Motion Control*. Hoboken, NJ, USA: John Wiley & Sons, 2011.

[2] *Nomenclature for Treating the Motion of a Submerged Body Through a Fluid*. The Society of Naval Architects and Marine Engineers (SNAME), Technical and Research Bulletin No. 1-5, April 1950.

[3] S. I. Sagatun and T. I. Fossen, "Lagrangian formulation of underwater vehicles' dynamics," Conference Proceedings 1991 IEEE International Conference on Systems, Man, and Cybernetics, Charlottesville, VA, USA, 1991, pp. 1029-1034 vol.2, doi: 10.1109/ICSMC.1991.169823.







































