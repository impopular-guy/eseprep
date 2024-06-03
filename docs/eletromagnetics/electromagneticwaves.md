---
layout: default
title:  "Electromagnetic Waves"
parent: Electromagnetics
nav_order: 5
mathjax: true
---

# Electromagnetic Waves
{: .no_toc}

1. TOC
{:toc}

- EM waves composed of undulating electrical and magnetic fields. Means of transporting energy or information.

## Intrinsic Wave Impedance

- ratio of electric and magnetic field phasors (complex amplitudes)
- $$ \eta = \frac{E_{zs}}{H_{xs}} = \frac{ E_o e^{-\gamma y} }{ \frac{\gamma}{j \omega \mu} E_o e^{-\gamma y}} = \frac{j \omega \mu}{\gamma}$$
- $$\gamma = \sqrt{j\omega\mu (\sigma + j\omega \epsilon)} = \alpha + j\beta$$ \
  where $$\fbox{$ \alpha = \omega \sqrt{\frac{\mu\epsilon}{2} \left[ \sqrt{1+ \left( \frac{\sigma}{\omega\epsilon} \right)^2} - 1 \right] } $}$$ \
  where $$\fbox{$ \beta = \omega \sqrt{\frac{\mu\epsilon}{2} \left[ \sqrt{1+ \left( \frac{\sigma}{\omega\epsilon} \right)^2} + 1 \right] } $}$$ and $$\fbox{$ v = \frac{\omega}{\beta}, \lambda = \frac{2\pi}{\beta} $}$$
- $$\fbox{$ \eta = |\eta|e^{j\theta_\eta} = \sqrt{\frac{j\omega \mu}{\sigma + j\omega \epsilon}}$}$$ \
  where $$|\eta| = \frac{ \sqrt{\mu/\epsilon} }{\left[1 + \left( \frac{\sigma}{\omega\epsilon} \right)^2 \right]^{1/4}}$$ \
  and $$\tan\theta_\eta = \frac{\sigma}{\omega\epsilon}, 0 \le \theta_\eta \le 45^o$$
- lossy dielectric: $$\sigma > 0$$

## Wave Propagation in Materials

- Consider linear, homogeneous, isotropic media in a **source-free region($$\vec{J} = 0, \rho_v = 0$$)**. Now Maxwell's equation in phasor form:
  $$\begin{align*}
  \nabla \times \vec{E}_s &= -j\omega\mu\vec{H}_s \\
  \nabla \times \vec{H}_s &= \sigma \vec{E}_s + j\omega\mu\vec{H}_s\\
  \nabla \cdot \vec{E}_s &= 0 \\
  \nabla \cdot \vec{H}_s &= 0 \\
  \end{align*}$$

- Taking curl on the curl equations, substituting and using the vector identity $$\fbox{$ \nabla\times\nabla\times \vec{F} = \nabla(\nabla\cdot \vec{F}) - \nabla^2 \vec{F} $}$$, we get:
  $$\begin{align*}
  \nabla^2 \vec{E}_s - \gamma^2 \vec{E}_s &= 0 \\
  \nabla^2 \vec{H}_s - \gamma^2 \vec{H}_s &= 0 \\
  \end{align*}$$ where $$\gamma^2 = j\omega\mu (\sigma + j\omega \epsilon)$$ \
  These equations are called phasor vector wave equations or *Helmnoltz* equations.
- Here $$\nabla^2$$ is the **vector Laplacian operator**.

### propagation Constant
- The complex constant $$\gamma = \sqrt{j\omega\mu (\sigma + j\omega \epsilon)} = \alpha + j\beta$$ is defined as **propagation constant**.
- The real part($$\alpha$$) is called **attenuation constant**. It defines the rate at which the fields of the wave are attenuated as the wave propagates. For lossless media $$\alpha = 0$$
- The img part($$\beta$$) is called **phase constant**. Defines rate at which phase changes as wave propagates.
- |Constants| Units|
  |:-|:-|
  |$$\gamma$$|$$\text{m}^{-1}$$|
  |$$\alpha$$|Np/m or dB/m **(1Np = 8.686dB)**|
  |$$\beta$$|rad/m|

### Properties of EM Waves

- The vector laplacian operator in terms of scalar Laplacian: \
  $$\nabla^2 \vec{F} = (\nabla^2 F_x)\hat{x} + (\nabla^2 F_y)\hat{y} + (\nabla^2 F_z)\hat{z}$$ \
  where $$\nabla^2 f = \frac{\partial^2 f}{\partial x^2} +\frac{\partial^2 f}{\partial y^2} +\frac{\partial^2 f}{\partial z^2} $$
- Use this in the phasor vector wave equations: $$\nabla^2 \vec{E}_s = \gamma^2 \vec{E}_s$$ and $$\nabla^2 \vec{H}_s = \gamma^2 \vec{H}_s$$ \
  We get, six partial differential equation one for each scalar components($$E_{xs}, E_{ys}, E_{zs}, H_{xs}, H_{ys}, H_{zs}$$). And EM wave must satisfy all six of these PDEs. A EM wave may not have all six of the components and based on this various types of waves are defined.

#### Plane Wave
- $$\vec{E}$$ and $$\vec{H}$$ lie in a place perpendicular to the direction of propagation
- $$\vec{E}$$ and $$\vec{H}$$ are perpendicular to each other.

#### Uniform Plane Wave
- A plane wave is called uniform if $$\vec{E}$$ and $$\vec{H}$$ in the plane perpendicular to the direction of propagation i.e. they vary only in direction of the propagation.