---
layout: default
title:  "Magnetostatics"
parent: Electromagnetics
nav_order: 3
mathjax: true
---

# Magnetostatics
{: .no_toc}

1. TOC
{:toc}

- Magnetostatic field is produced by a *constant current flow*.

$$
\begin{array} {|c|c|c| }
\hline
\textbf{Term} & \textbf{Electric} & \textbf{Magnetic} \\
\hline
\text{basic laws} & \vec{F} = \frac{Q_1Q_2}{4\pi\epsilon^2}\hat{a}_r & d\vec{B} = \frac{\mu I d\vec{l} \times \hat{a}_r}{4\pi R^2} \\
& \int \vec{D} \cdot d\vec{S} = Q_{enc} & \int \vec{H} \cdot d\vec{l} = I_{enc} \\
\hline
\text{Force law} & \vec{F} = Q\vec{E} & \vec{F} = Q(\vec{v} \times \vec{B}) \\
\hline
\text{Field intensity} & E = \frac{V}{l}\text{(V/m)} & H = \frac{I}{l}\text{(A/m)}\\
\hline
\text{Flux density} & D = \frac{\Psi}{S}(\text{C/m}^2) & B = \frac{\Psi}{S} (\text{Wb/m}^2)\\
& \vec{D} = \epsilon\vec{E} & \vec{B} = \mu\vec{H} \\
\hline
\text{Potentials} & \vec{E} = -\nabla V & \vec{H} = \nabla V_m \\
& V = \int\frac{\rho_l dl}{4\pi\epsilon} & \vec{A} = \int\frac{\mu I d\vec{l}}{4\pi R} \\
\hline
\text{Flux} & \Psi = \int\vec{D}\cdot d\vec{S}  & \Psi = \int\vec{B}\cdot d\vec{S}\\
& \Psi = Q = CV & \Psi = LI \\
& I = C\frac{dV}{dt} & V = L\frac{dI}{dt} \\
\hline
\text{Energy density} & W_E = \frac{1}{2}\vec{D}\cdot\vec{E} & w_m = \frac{1}{2}\vec{B}\cdot\vec{H}\\
\hline
\text{Poisson's eqn} & \nabla^2 V = -\frac{\rho_v}{\epsilon} & \nabla^2 A = -\mu \vec{J}\\
\hline
\end{array}
$$

## Biot-Savart's Law

- $$dH \propto \frac{Idl \sin \alpha}{R^2}$$ where
    1. $$dH$$ = magnetic field intensity at a point P
    1. $$Idl$$ = differential current element
    1. $$\alpha$$ = angle between current element and line joining it to point P
    1. $$R$$ distance between point P and current element

    i.e. $$\fbox{$ d\vec{H} = \frac{Id\vec{l} \times \hat{a}_R}{4\pi R^2} = \frac{Id\vec{l} \times \vec{R}}{4\pi R^3} $}$$
- direction of magnetic field determined using **right-hand screw rule** where thumb represents direction of current, rest of the fingers show direction of field.
- other source elements for surface current density and volume current density are:
$$Id\vec{l} \equiv \vec{K}dS \equiv \vec{J}dv$$

### H-field for finite length of I carrying wire

![hwire]({{ site.baseurl }}/assets/hfield_wire.svg)

- $$\vec{H} = \frac{I}{4\pi \rho}(\sin\alpha_1 + \sin\alpha_2) \hat{a}_\phi$$
- for semi-infinite wire, $$\alpha_1 = 90^\circ, \alpha_2 = 0^\circ, \vec{H} = \frac{I}{4\pi\rho} \hat{a}_\phi$$
- for infinite wire, $$\alpha_1 = 90^\circ, \alpha_2 = 90^\circ, \vec{H} = \frac{I}{2\pi\rho} \hat{a}_\phi$$

## Ampere's Circuit Law-Maxwell's Equation

- If $$I_{enc}$$ is current enclosed by a closed path, then $$\fbox{$ \oint \vec{H} \cdot d\vec{l} = I_{enc} $}$$
- We have $$\oint \vec{H} \cdot d\vec{l} =\int_s (\nabla \times \vec{H}) \cdot d\vec{S} = I_{enc} = \int_s \vec{J} \cdot d\vec{S}$$ \
i.e $$\fbox{$ \nabla \times \vec{H} = \vec{J} $}$$
- $$ \nabla \times \vec{H} = \vec{J} \neq 0 $$ then field is **not conservative**
- |**Infinite line current** $$I$$ along z-axis| $$\vec{H} = \frac{I}{2\pi\rho}\hat{a}_\phi$$|
|**Infinite sheet current** with uniform current density $$\vec{K} = K_y \hat{a}_y$$ | $$\vec{H} = \frac{1}{2}\vec{K} \times \hat{a}_n$$|

## Magnetic Flux Density - Maxwell's Equation

- magnetic flux density $$\vec{B}$$ similar to $$\vec{D}$$
- $$\fbox{$ \vec{B} = \mu_o \vec{H} $}$$ (Webers/square meter) or **Teslas**
- magnetic flux $$\psi = \int_s \vec{B} \cdot d\vec{S}$$ (Webers)
- isolated magnetic poles don't exist hence $$\fbox{$ \oint_s \vec{B}\cdot d\vec{S} = 0 $}$$ i.e. $$\fbox{$ \nabla \cdot \vec{B} = 0 $}$$

> 1. magnetostatic field is not conserved, but magnetic flux is conserved
> 2. magnetic field lines are always continuous
> 3. $$\nabla \cdot \vec{b} = 0 $$ then field is said to be **solenoidal**

## Magnetic Scalar and Vector Potentials

- **Magnetic Scalar Potential $$V_m$$ (Amperes)** only defined where $$\vec{J} = 0$$ \
$$\fbox{$ \vec{H} = -\nabla V_m $}$$
- **vector magnetic potential $$\vec{A}$$ (Wb/m)** $$\vec{B} = \nabla \times \vec{A}$$
- scalar potential only used in source-free region

## Forces due to magnetic fields
- **charged particle**: $$\vec{F} = Q(\vec{E} + \vec{v} \times \vec{B})$$
- **current element**: $$d\vec{F} = Id\vec{l} \times \vec{B}$$

> Force per unit length between two current carrying conductor is given by $$\fbox{$ \frac{F}{L} = \frac{\mu_o I_1 I_2}{2\pi R} $}$$

## Magnetic boundary conditions

- equations used to determine boundary conditions for magnetic field are:
$$\oint \vec{B} \cdot d\vec{S} = 0$$ and $$\oint \vec{H} \cdot d\vec{l} = I$$
- Given $$K$$ is surface current at the boundary, $$\theta_1, \theta_2$$ are angle to normal of $$\vec{B}_1, \vec{B}_2$$ respectively
- $$\fbox{$ \vec{B}_{1n} =  \vec{B}_{2n}$}$$ or $$\fbox{$ \mu_1 \vec{H}_{1n} =  \mu_2 \vec{H}_{2n}$}$$
- $$\fbox{$ \vec{H}_{1t} - \vec{H}_{2t} = K $}$$ or $$\fbox{$ \frac{\vec{B}_{1t}}{\mu_1} - \frac{\vec{B}_{2t}}{\mu_2}$} = K$$
- general case $$(\vec{H}_1 - \vec{H}_2) \times \hat{a}_{n12} = \vec{K}$$
- for current free boundary($$K = 0$$),  $$\fbox{$ \frac{\tan\theta_1}{\tan\theta_2} = \frac{\mu_1}{\mu_2} $}$$

## Permeability ($$\mu_r$$)

Here, external field H, magnetization M, magnetic susceptibility $$\chi$$

- $$B = \mu_o (H + M) $$ and $$B = \mu_r \mu_o H$$ i.e. $$M = (\mu_r - 1)H$$
- where $$\fbox{$ \chi = \mu_r - 1 $}$$