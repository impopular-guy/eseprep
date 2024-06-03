---
layout: default
title:  "Vector Analysis"
parent: Electromagnetics
nav_order: 1
mathjax: true
---

# Vector Analysis
{: .no_toc}

> Assumed that person reading this already possess a decent knowledge about this topic. Only special things are noted down.

1. TOC
{:toc}

---

Scalar triple product:

$$\vec{A} \cdot (\vec{B} \times \vec{C}) = \vec{B} \cdot (\vec{C} \times \vec{A}) = \vec{C} \cdot (\vec{A} \times \vec{B}) = \begin{vmatrix}
A_x & A_y & A_z \\
B_x & B_y & B_z \\
C_x & C_y & C_z \\
\end{vmatrix}
$$

Vector triple product: (*bac-cab* rule)

$$\vec{A} \times (\vec{B} \times \vec{C}) = \vec{B}(\vec{A} \cdot \vec{C}) - \vec{C}(\vec{A} \cdot \vec{B})$$

---

### Cylindrical coordinates $$(x,y,z) \rightarrow (\rho, \phi, z)$$

- Ranges: $$ 0 \leq\rho\leq\infty, \quad 0\leq\phi\leq 2\pi, \quad -\infty\leq z \leq\infty $$
- $$\hat{a_\rho} \times \hat{a_{\phi}} = \hat{a_z}$$
- $$ \rho = \sqrt{x^2 + y^2}, \quad \phi = \tan^{-1}\frac{y}{x}, \quad z = z$$
- $$x = \rho \cos \phi, \quad y = \rho \sin \phi, \quad z=z$$
- Transformation: $$(A_x\hat{a_x} + A_y\hat{a_y} + A_z\hat{a_z}) \longleftrightarrow (A_\rho\hat{a_\rho} + A_\phi\hat{a_\phi} + A_z\hat{a_z})$$

$$
\begin{bmatrix}
A_\rho \\
A_\phi \\
A_z 
\end{bmatrix} = \begin{bmatrix}
\cos\phi & \sin\phi & 0 \\
-\sin\phi & \cos\phi & 0 \\
0 & 0 & 1
\end{bmatrix} \begin{bmatrix}
A_x \\
A_y \\
A_z
\end{bmatrix}
$$

$$
\begin{bmatrix}
A_x \\
A_y \\
A_z
\end{bmatrix}  = \begin{bmatrix}
\cos\phi & -\sin\phi & 0 \\
\sin\phi & \cos\phi & 0 \\
0 & 0 & 1
\end{bmatrix} \begin{bmatrix}
A_\rho \\
A_\phi \\
A_z 
\end{bmatrix}
$$

---

### Spherical coordinates $$(x,y,z) \rightarrow (r, \theta, \phi)$$

- Ranges: $$ 0 \leq r \leq\infty, \quad 0\leq\theta\leq \pi, \quad 0\leq \phi \leq 2\pi $$
- $$\hat{a_r} \times \hat{a_\theta} = \hat{a_\phi}$$
- $$ r = \sqrt{x^2 + y^2 + z^2}, \quad \theta = \tan^{-1}\frac{\sqrt{x^2+y^2}}{z}, \quad \phi = \tan^{-1}\frac{y}{x}$$
- $$x = r\sin\theta\cos\phi, \quad y = r\sin\theta\sin\phi, \quad z=r\cos\theta$$
- Transformation: $$(A_x\hat{a_x} + A_y\hat{a_y} + A_z\hat{a_z}) \longleftrightarrow (A_r\hat{a_r} + A_\theta\hat{a_\theta} + A_\phi\hat{a_\phi})$$

$$
\begin{bmatrix}
A_r \\
A_\theta \\
A_\phi 
\end{bmatrix} = \begin{bmatrix}
\sin\theta\cos\phi & \sin\theta\sin\phi & \cos\theta \\
\cos\theta\cos\phi & \cos\theta\sin\phi & -\sin\theta \\
-\sin\phi & \cos\phi & 0 \\
\end{bmatrix} \begin{bmatrix}
A_x \\
A_y \\
A_z
\end{bmatrix}
$$

$$
\begin{bmatrix}
A_x \\
A_y \\
A_z
\end{bmatrix}  = \begin{bmatrix}
\sin\theta\cos\phi & \cos\theta\cos\phi & -\sin\phi \\
\sin\theta\cos\phi & \cos\theta\sin\phi & \cos\phi \\
\cos\theta & -\sin\theta & 0 \\
\end{bmatrix} \begin{bmatrix}
A_r \\
A_\theta \\
A_\phi 
\end{bmatrix}
$$

---

### Differential length ($$\vec{dl}$$), surface ($$\vec{ds}$$), volume ($$dv$$)

- **Cartesian**: \
$$
\begin{align*}
\vec{dl} &= dx \space \vec{a_x} + dy \space \vec{a_y} + dx \space \vec{a_x} \\
\vec{ds} &= dy \space dz \space \vec{a_x} + dx \space dz \space \vec{a_y} + dx \space dy \space \vec{a_x} \\
dv &= dx \space dy \space dz
\end{align*}
$$

- **Cylindrical**: \
$$
\begin{align*}
\vec{dl} &= d\rho \space \vec{a_\rho} + \rho d\phi \space \vec{a_\phi} + dx \space \vec{a_x} \\
\vec{ds} &= \rho d\phi \space dz \space \vec{a_\phi} + d\rho \space dz \space \vec{a_\phi} + \rho d\rho \space d\phi \space \vec{a_z} \\
dv &= \rho d\rho \space d\phi \space dz
\end{align*}
$$

- **Spherical**: \
$$
\begin{align*}
\vec{dl} &= dr \space \vec{a_r} + r d\phi \space \vec{a_\theta} + r \sin \theta d\phi \space \vec{a_\phi} \\
\vec{ds} &= r^2 \sin\theta \space d\theta \space d\phi \space \vec{a_r} + r\sin\theta \space dr \space d\phi \space \vec{a_\theta} + r dr \space d\theta \space \vec{a_\phi} \\
dv &= r^2 \sin\theta \space dr \space d\theta \space d\phi
\end{align*}
$$

---

### Del operator $$\nabla$$

Cartesian: $$\nabla = \frac{\partial}{\partial x}\hat{a_x} + \frac{\partial}{\partial y}\hat{a_y} + \frac{\partial}{\partial z}\hat{a_z}$$

Cylindrical: $$\nabla = \frac{\partial}{\partial \rho}\hat{a_\rho} + \frac{1}{\rho}\frac{\partial}{\partial \phi}\hat{a_\phi} + \frac{\partial}{\partial z}\hat{a_z}$$

Spherical: $$\nabla = \frac{\partial}{\partial r}\hat{a_r} + \frac{1}{r}\frac{\partial}{\partial \theta}\hat{a_\theta} + \frac{1}{r\sin\theta}\frac{\partial}{\partial \phi}\hat{a_\phi}$$

- gradient: $$\nabla V$$
- divergence: $$\nabla \cdot \vec{A}$$
- curl: $$\nabla \times \vec{A}$$
- Laplacian: $$\nabla^2V$$
- $$\nabla \cdot (\nabla \times \vec{A}) = 0$$
- $$\nabla \times (\nabla f) = 0$$
- $$\nabla \times (\nabla \times \vec{A}) = \nabla(\nabla \cdot \vec{A}) - \nabla^2 \vec{A}$$
- $$\nabla(UV) = V\nabla U + U \nabla V$$

### Divergence
How much a field diverges from a point

Cartesian: $$\nabla \cdot \vec{A} = \frac{\partial A_x}{\partial x} + \frac{\partial A_y}{\partial y} + \frac{\partial A_z}{\partial z}$$

Cylindrical: $$\nabla \cdot \vec{A}= \frac{1}{\rho}\frac{\partial (\rho A_\rho)}{\partial \rho} + \frac{1}{\rho}\frac{\partial A_\phi}{\partial \phi} + \frac{\partial A_z}{\partial z}$$

Spherical: $$\nabla \cdot \vec{A}= \frac{1}{r^2}\frac{\partial(r^2 A_r)}{\partial r} + \frac{1}{r\sin \theta}\frac{\partial(A_\theta \sin\theta)}{\partial \theta} + \frac{1}{r\sin\theta}\frac{\partial A_\phi}{\partial \phi}$$

**Divergence Theorem:** $$\oint_S \vec{A} \cdot d\vec{S} = \int_V \nabla \cdot \vec{A} dv$$

### Curl
whether there is a rotation associated with a vector field

Cartesian: $$\nabla \times \vec{A} = \begin{vmatrix}
\hat{a_x} & \hat{a_y} & \hat{a_z} \\
\frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
A_x & A_y & A_z 
\end{vmatrix}$$

Cylindrical: $$\nabla \times \vec{A} = \frac{1}{\rho}\begin{vmatrix}
\hat{a_\rho} & \rho \hat{a_\phi} & \hat{a_z} \\
\frac{\partial}{\partial \rho} & \frac{\partial}{\partial \phi} & \frac{\partial}{\partial z} \\
A_\rho & \rho A_\phi & A_z 
\end{vmatrix}$$

Spherical: $$\nabla \times \vec{A} = \frac{1}{r^2 \sin\theta}\begin{vmatrix}
\hat{a_r} & r\hat{a_\theta} & r \sin\theta \hat{a_\phi} \\
\frac{\partial}{\partial r} & \frac{\partial}{\partial \theta} & \frac{\partial}{\partial \phi} \\
A_r & rA_\theta & r \sin\theta A_\phi 
\end{vmatrix}$$

**Stokes' Theorem**: $$\oint_L \vec{A} \cdot d\vec{l} = \int_S (\nabla \times \vec{A}) \cdot d\vec{S}$$

### Laplacian of a Scalar

Cartesian: $$\nabla^2 V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} + \frac{\partial^2 V}{\partial z^2}$$

Cylindrical: $$\nabla^2 V = \frac{1}{\rho}\frac{\partial }{\partial \rho}\left(\rho \frac{\partial V}{\partial \rho} \right) + \frac{1}{\rho^2}\frac{\partial^2 V}{\partial \phi^2} + \frac{\partial^2 V}{\partial z^2}$$

Spherical: $$\nabla^2 V = \frac{1}{r^2}\frac{\partial}{\partial r}\left( r^2 \frac{\partial V}{\partial r}\right) + \frac{1}{r^2 \sin\theta}\frac{\partial}{\partial \theta}\left( \sin\theta \frac{\partial V}{\partial \theta} \right) + \frac{1}{r^2 \sin^2\theta}\frac{\partial^2 V}{\partial \phi^2}$$
