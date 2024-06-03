---
layout: default
title:  "Electrostatics"
parent: Electromagnetics
nav_order: 2
mathjax: true
---

# Electrostatics
{: .no_toc}

1. TOC
{:toc}

## Gauss's Law - Maxwell's Equation
We have, total outward electric flux $$\psi$$, any closed surface $$S$$, total charge enclosed $$Q_{enc}$$, volume charge density $$\rho_v$$, electric flux density $$\vec{D}$$

$$\psi = \oint_S \vec{D} \cdot d\vec{S} = Q_{end} = \int_V \rho_v dV$$

Applying divergence theorem, we get $$\nabla \cdot \vec{D} = \rho_v$$

$$\vec{D} = \epsilon_r \epsilon_o \vec{E}$$, (units $$C/m^2$$)

- Permittivity of free space: $$\epsilon_o = 8.854 \times 10^{-12} \space \text{F/m}$$
- $$k = \frac{1}{4\pi \epsilon_o} \simeq 9 \times 10^9 \space \text{m/F}$$

### Application of Gauss's Law

- Choose Gaussian surface such that $$\vec{D}$$ is normal or tangential to the surface and some symmetry exhibited by the charge distribution.

|Charge Source|$$\vec{D}$$|Gaussian surface|
|:-|:-|:-|
|Point |$$\frac{Q}{4\pi r^2}\hat{a_r}$$|Sphere|
|Infinite line (z-axis)|$$\frac{\rho_L}{2\pi \rho}\hat{a_\rho}$$|Cylinder|
|Infinite sheet (xy-plane)|$$\frac{\rho_S}{2}\hat{a_z}$$|Box|
|Uniformly charged sphere (radius $$a$$)|$$\begin{cases}\frac{r}{3}\rho_v \hat{a_r} & 0 \lt r \le a \\ \frac{a^3}{3r^2}\rho_v \hat{a_r} & r \ge a \end{cases}$$|Sphere|

---

### Application of Coulomb's Law

|source|$$\vec{E}$$|
|:-|:-|
|On axis of charged ring (xy-plane, radius $$a$$)|$$\frac{Qz}{4\pi \epsilon (z^2+a^2)^{3/2}} \hat{a_z}$$|
|On axis of charged disc (xy-plane, radius $$a$$)|$$\frac{\rho_S}{2\epsilon} \left(1 - \frac{z}{\sqrt{z^2+a^2}} \right) \hat{a_z}$$|

---

## Electric Potential

- Work = (Force component along path) x Distance
- $$\vec{F}=Q\vec{E} \quad $$ and $$ \quad dW=-\vec{F}\cdot d\vec{l}$$
- $$V_{AB} = \frac{W}{Q} = - \int_A^B\vec{E}\cdot d\vec{l} = V_B - V_A$$
- For closed path where point A = B, $$\oint \vec{E}\cdot d\vec{l} = 0$$
- Equipotential surfaces are always $$\perp^r$$ to $$\vec{E}$$.
- Potential due to set of point charges, $$V = \frac{1}{4\pi \epsilon} \sum_{k=1}^{N}\frac{Q_k}{\text{abs}(R-R_k) }$$

---

## Electric field as Gradient of potential - Maxwell's Equation

$$V_{AB} + V_{BA} = 0 \implies \oint_L \vec{E} \cdot d\vec{l} = 0$$

Using Stoke's Theorem, we get $$\quad \nabla \times \vec{E} = 0$$

- defining potential $$V = - \int \vec{E} \cdot d\vec{l}$$
- $$\vec{E} = - \nabla V$$

### Electric Dipole
- potential at point P $$V = \frac{Q}{4\pi \epsilon}\left( \frac{1}{R_+} - \frac{1}{R_-}\right)$$
- *vector electric dipole moment:* $$\vec{p} = Q\vec{d}$$ (d from -Q to +Q)
- if point P is very far away (i.e. $$R_+ \approx R_- \approx R$$, $$R >> d$$), then $$V = \frac{Qd\cos \theta}{4 \pi\epsilon R^2} = \frac{\vec{p} \cdot \hat{a_R}}{4 \pi\epsilon R^2}$$
- Therefore $$\vec{E} = -\nabla V = \frac{p}{4 \pi\epsilon R^3}(2\cos\theta \hat{a_R} + \sin\theta \hat{a_\theta})$$ (V/m)

### Energy density in electrostatic field ($$J/m^3$$)

- Energy stored for N point charges $$W_E = \frac{1}{2}\sum_{k=1}^{N}Q_kV_k$$
- continuous charge distribution $$W_E = \frac{1}{2}\int_{vol.} \rho_v V dv$$
- $$W_E = \frac{1}{2}\int_{vol.} \vec{D}\cdot\vec{E} \space dv$$
- define energy density as $$w_E = \frac{dW_E}{dv} = \frac{1}{2}\vec{D}\cdot\vec{E} = \frac{1}{2}\epsilon E^2 = \frac{D^2}{@\epsilon}$$

## Current and Current density

- $$I = \frac{dQ}{dt}$$ and $$\Delta I = J \Delta S$$ i.e. total current through a surface $$S$$ is $$I = \int_S \vec{J}\cdot \Delta \vec{S}$$
- $$I$$ depends on these kinds of current densities:
    * Convection current density
    * Conduction current density, $$\vec{J} = \rho_v \vec{v_d}$$
    * Displacement current density

### Ohm's law
- $$\vec{J} = \rho_v \vec{v_d} = \frac{ne^2\tau}{m_e}\vec{E} = \sigma\vec{E}$$ \
    where $$\sigma = \frac{ne^2\tau}{m_e}$$ is conductivity, $$n$$ is number of electrons per unit volume, $$\tau$$ is avg. time interval between collisions.


- **A perfect conductor($$\sigma = \infty$$) cannot contain an electrostatic field inside it**
    * i.e. under static conditions $$E=0, \rho_v =0, V=0$$
    * Hence, also called *equipotential*
    * As external electric field is applied, both +ve and -ve charges accumulate on the surface to form *induced surface charge* and create *induced internal field* to negate the external field.
    * Resistance $$R = \frac{V}{I} = \frac{\int_v \vec{E}\cdot d\vec{l}}{\int_s \sigma\vec{E}\cdot d\vec{S}}$$
    * Power = rate of change of energy = force times velocity
    $$P = \int_v \rho_vdv\vec{E}\cdot \vec{v}_d = \int_v \vec{E}\cdot \vec{J}$$ \
    This is known as **Joule's Law**

## Continuity Equation

- derived using principle of conservation of charge
- states that there can be no accumulation of charge at a point
- $$\fbox{$\nabla \cdot \vec{J} = - \frac{\partial\rho_v}{\partial t}$}$$ is called **continuity of current equation**
- Derivation: $$I_{out} = -\frac{dQ_{in}}{dt} = \oint \vec{J}\cdot d\vec{S} = \int \nabla \cdot \vec{J} dv$$ \
i.e. $$\int \nabla \cdot \vec{J} dv = -\frac{dQ_{in}}{dt} = -\int \frac{\partial\rho_v}{\partial t} dv$$
- For steady current, $$\frac{\partial\rho_v}{\partial t} = 0$$, which proves Kirchhoff's current law
- *Relaxation time:* time taken for interior charge to drop to $$e_{-1}$$ (36.8%) of initial value. \
$$T_r = \frac{\epsilon}{\sigma}$$

## Boundary Conditions

To determine boundary conditions, we use maxwell equations \
$$ \oint \vec{E}\cdot d\vec{l} = 0 $$ and $$ \oint \vec{D} \cdot d\vec{S} = Q_{end} $$ \
Also $$\vec{E} = \vec{E}_t + \vec{E}_n$$ and $$\vec{D} = \epsilon \vec{E}$$

> NOTE: $$E_{n}, E_{t}, D_{n}, D_{t}$$ are components, hence scalar.

### Dielectric-Dielectric Boundary Condition

![bc]({{ site.baseurl }}/assets/boundary_conditions.svg)

- We have for the two regions $$\epsilon_1 = \epsilon_o \epsilon_{r1}$$ and $$\epsilon_2 = \epsilon_o \epsilon_{r2}$$ \
Applying $$ \oint \vec{E}\cdot d\vec{l} = 0 $$ to the closed path abcda, and with $$\Delta h \rightarrow 0 $$ we get \
$$E_{1t} \Delta w - E_{2t} \Delta w = 0$$ \
i.e. $$\fbox{$E_{1t} = E_{2t}$}$$ and $$\fbox{$ \frac{D_{1t}}{\epsilon_1} = \frac{D_{2t}}{\epsilon_2}$}$$

- Applying $$ \oint \vec{D} \cdot d\vec{S} = Q_{end} $$ to the cylindrical gaussian surface, we get \
$$D_{1n} \Delta S - D_{2n} \Delta S = \Delta Q = \rho_s \Delta S$$ \
i.e. $$\fbox{$ D_{1n} - D_{2n} = \rho_s $}$$ where $$\rho_s$$ is free density placed at the boundary.

- If no free charge exist in the boundary then we get \
$$\fbox{$D_{1n} = D_{2n}$}$$ and $$\fbox{$ \epsilon_1 E_{1n} = \epsilon_2 E_{2n} $}$$

- If the electric fields make angles $$\theta_1$$ and $$\theta_2$$ with the normal to the interface then $$\fbox{$\frac{\tan \theta_1}{\tan \theta_2} = \frac{\epsilon_{r1}}  {\epsilon_{r2}} $}$$

### Conductor-Dielectric Boundary Condition

- Inside a conductor $$\vec{E} = 0$$ 
- Therefore, $$\fbox{$ E_t = 0, D_t = 0$}$$ and $$\fbox{$ D_n = \rho_s, E_n = \frac{\rho_s}{\epsilon} $}$$

## Poisson's and Laplace's Equations

- Using Gauss's Law $$\nabla \cdot \vec{D} = \nabla \cdot \epsilon \vec{E} = \rho_v$$ and $$\vec{E} = - \nabla V$$

    **Poisson's Equation**: $$\fbox{$ \nabla^2 V = - \frac{\rho_v}{\epsilon} $}$$ \
    In charge free region **Laplace's Equation**: $$\fbox{$ \nabla^2 V = 0 $} $$ 

- Above is *valid for homogeneous medium*, i.e. $$\epsilon$$ is constant. For non-homogeneous medium we have $$\nabla \cdot (-\epsilon \nabla V) = \rho_v$$

- **Uniqueness Theorem**: if a solution to Laplace's equation can be found that satisfies the boundary conditions, then the *solution is unique*.

## Capacitance

- must have two (or more) conductors carrying equal but opposite charges
- flux lines leaving one conductor must necessarily terminate at the surface of other
- pot. diff. between the plates $$V = V_1 - V_2 = - \int^{1}_{2} \vec{E} \cdot d\vec{l}$$

- Define capacitance as $$C = \frac{Q}{V} = \frac{ \epsilon \oint \vec{E} \cdot d\vec{l} }{ \int \vec{E} \cdot d\vec{l}}$$ farads(F)

|Type|$$\vec{E}$$| $$V$$ | $$C$$ |
|:-|:-|:-|:-|
|**Parallel-plate** (plate area = A, plate separation = d)| $$-\frac{Q}{\epsilon A} \hat{a}_x$$| $$\frac{Qd}{ \epsilon A}$$ | $$\frac{\epsilon A}{d}$$ |
|**Coaxial** (inner radius = a, outer radius = b, length = L)| $$\frac{Q}{2\pi \epsilon \rho L} \hat{a}_\rho$$| $$ \frac{Q}{2\pi \epsilon \rho L} \ln \frac{b}{a}$$| $$ \frac{2\pi \epsilon \rho L}{\ln\frac{b}{a}} $$|
|**Spherical** (inner radius = a, outer radius = b)| $$\frac{Q}{4\pi \epsilon r^2} \hat{a}_r$$| $$\frac{Q}{4\pi \epsilon}\left( \frac{1}{a} - \frac{1}{b} \right)$$| $$\frac{4\pi \epsilon}{\frac{1}{a} - \frac{1}{b} }$$|

> - For isolated sphere $$(b \rightarrow \infty), C = 4\pi\epsilon a$$
> - For series capacitors, $$C = \frac{C_1 C_2}{C_1 + C_2}$$
> - For parallel capacitors, $$C = C_1 + C_2$$

## Extras

- dipole moment $$\vec{p} = Q\vec{d}$$
- for n dipole moments per unit volume, then $$\vec{p}_{total} = \sum^{n \Delta v}_{i=1}\vec{p}_i$$
- Polarization $$P = \lim_{\Delta v \rightarrow 0} \frac{1}{\Delta v} \vec{p}_{total}$$
- Also $$\fbox{$D = \epsilon_o E + P $}$$, $$ \fbox{$ P = \chi_e \epsilon_o E $}$$ and $$D = \epsilon_r \epsilon_o E$$
- $$\fbox{$ \epsilon_r = \chi_e + 1 $}$$, where $$\chi_e$$ is electric susceptibility of material.