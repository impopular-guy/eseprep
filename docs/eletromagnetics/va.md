---
layout: default
title:  "Vector Analysis"
parent: Eletromagnetics
nav_order: 1
mathjax: true
---

# Vector Analysis

> Assumed that person reading this already possess a decent knowledge about this topic. Only special things are noted down.

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

Catesian: $$\nabla = \frac{\partial}{\partial x}\hat{a_x} + \frac{\partial}{\partial y}\hat{a_y} + \frac{\partial}{\partial z}\hat{a_z}$$

Cylindrical: $$\nabla = \frac{\partial}{\partial \rho}\hat{a_\rho} + \frac{1}{\rho}\frac{\partial}{\partial \phi}\hat{a_\phi} + \frac{\partial}{\partial z}\hat{a_z}$$

Spherical: $$\nabla = \frac{\partial}{\partial r}\hat{a_r} + \frac{1}{r}\frac{\partial}{\partial \theta}\hat{a_\theta} + \frac{1}{r\sin\theta}\frac{\partial}{\partial \phi}\hat{a_\phi}$$