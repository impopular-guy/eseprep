---
layout: default
title:  "Time-Varying Electromagnetic Field"
parent: Eletromagnetics
nav_order: 4
mathjax: true
---

# Time-Varying Electromagnetic Field
{: .no_toc}

1. TOC
{:toc}

## Maxwell's Equation for Static EM fields

$$\begin{array} {|c|c|c| }
\hline
 & \textbf{Differential or Point form} & \textbf{Integral form} \\
\hline
\text{Gauss's Law} & \nabla \cdot \vec{D} = \rho_v & \oint_s \vec{D}\cdot d\vec{S} = \int_v \rho_v dv \\
\hline
\text{Nonexistence of magnetic monopoles} & \nabla \cdot \vec{B} = 0 & \oint_s \vec{B}\cdot d\vec{S} = 0 \\
\hline
\text{Conservativeness of electrostatic field} & \nabla \times \vec{E} = 0 & \oint_L \vec{E}\cdot d\vec{l} = 0 \\
\hline
\text{Ampere's Law} & \nabla \times \vec{H} = \vec{J} & \oint_L \vec{H}\cdot d\vec{l} = \int_s \vec{J} \cdot d\vec{S} \\
\hline
\end{array}
$$

- a field can only be electric or magnetic of it can satisfy corresponding  maxwell's equation
- above eqns are for static field. The divergence equations remain same but the curl equations change for time-varying fields.

## Faraday's Law of Induction

- time-varying current was obtained in the closed wire loop while magnet was being moved toward it or away from it.
- It states that the line integral of electric field around a closed loop equal the rate of change of magnetic flux through the loop.
- **Right-hand thumb rule** if curling of fingers point in direction of traversal in the loop then thumb points in the direction of positive magnetic flux.
- For any loop, $$\fbox{$ V_{emf} = \oint_L \vec{E} \cdot d\vec{l} = -\frac{d\phi}{dt} = - \frac{d}{dt} \int_s \vec{B}\cdot d\vec{S} $}$$ \
  where EMF is *electromotive force*


## Transformer and Motional EMFs

- The variation in flux with time can be caused in three ways:

### 1. Stationary Loop in time-varying B-Field(Treansform EMF)

- This is referred to transformer emf in power analysis since it is due to transformer action.
- Using Stoke's theorem: \
  $$V_{emf} = \oint_L \vec{E} \cdot d\vec{l} = \int_s \nabla \times \vec{E} d\vec{S} = -\int_s \frac{\partial \vec{B}}{ \partial t}\cdot d\vec{S}$$
- hence, **Faraday's Law of induction in differential form:** \
  $$\fbox{$ \nabla \times \vec{E} = - \frac{\partial \vec{B}}{\partial t} $}$$
- time-varying E-field is not conservative $$ \nabla \times \vec{E} \neq 0$$

### 2. Moving loop in static B-Field (Motional EMF)

- emf is induced in conduction loop when moved in a static B-field. It is called motional becaused it is due to motion. Found in motors, generators and alternators.
- We define motional E-field as $$\vec{E}_m = \frac{\vec{F}_m}{Q} = \vec{v} \times \vec{B}$$ \
  i.e. $$\fbox{$ \nabla \times \vec{E} = \nabla \times (\vec{v} \times \vec{B}) $}$$

### 3. Moving loop in time-varying fiels

- this is the general case \
  i.e. $$\fbox{$ \nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t} + \nabla \times (\vec{v} \times \vec{B}) $}$$

## Displacement Current

- For static EM field, $$\nabla \times \vec{H} = \vec{J}$$ \
  And divergence of curl is zero. i.e. $$\nabla \cdot (\nabla \times \vec{H}) = \nabla \cdot \vec{J} = 0$$ 
- However, **continuity equation** is given by $$\fbox{$ \nabla \cdot \vec{J} = - \frac{\partial \rho_v}{\partial t} $}$$
- Displacement current cannot be zero, so to the static EM eqn compatible we add a term $$\vec{J}_d$$ which is determined by using the fact that divergence of curl of any vector is zero. \
  $$\begin{align*}
  \nabla \times \vec{H} &= \vec{J} + \vec{J}_d \\
  \nabla \cdot (\nabla \times \vec{H}) &= \nabla \cdot \vec{J} + \nabla \cdot\vec{J}_d = 0 \\
  \nabla \cdot \vec{J}_d &= -\nabla \cdot\vec{J} = \frac{\partial \rho_v}{\partial t} = \frac{\partial }{\partial t}(\nabla \cdot \vec{D}) = \nabla \cdot \frac{\partial \vec{D}}{\partial t} \\
  \vec{J}_d &= \frac{\partial \vec{D}}{\partial t}
  \end{align*}$$
- Finally we have $$\fbox{$ \nabla \times \vec{H} = \vec{J} +  \frac{\partial \vec{D}}{\partial t}$}$$ \
    where $$\vec{J}_d$$ is **displacement current density** \
    and $$\vec{J} = \sigma\vec{E}$$ is **conduction current density**

## Maxwell's Equation in final form
- for a field to be qualified as EM field, it must satisfy all four equations.


$$\begin{array} {|c|c|c| }
\hline
 & \textbf{Differential form} & \textbf{Integral form} \\
\hline
\text{Gauss's Law} & \nabla \cdot \vec{D} = \rho_v & \oint_s \vec{D}\cdot d\vec{S} = \int_v \rho_v dv \\
\hline
\text{Nonexistence of isolated} \\ \text{magnetic monopoles} & \nabla \cdot \vec{B} = 0 & \oint_s \vec{B}\cdot d\vec{S} = 0 \\
\hline
\text{Faraday's Law} & \nabla \times \vec{E} = - \frac{\partial \vec{B}}{\partial t} & \oint_L \vec{E}\cdot d\vec{l} = - \frac{\partial }{\partial t} \int_s \vec{B} \cdot d\vec{S} \\
\hline
\text{Ampere's Circuit Law} & \nabla \times \vec{H} = \vec{J} +  \frac{\partial \vec{D}}{\partial t}& \oint_L \vec{H}\cdot d\vec{l} = \int_s \left( \vec{J} +  \frac{\partial \vec{D}}{\partial t} \right) \cdot d\vec{S} \\
\hline
\end{array}
$$