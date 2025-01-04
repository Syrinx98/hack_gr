# Exercise Solution Guide

This concise guide outlines the essential steps to solve the GR (General Relativity) exercises.

## 1. Metric Tensor Transformation

1. **Identify the Original Metric**
- Start with the metric tensor $g_{\mu\nu}$ in the initial coordinates.
- In Cartesian coordinates $(x, y)$:
- $g_{\mu\nu} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$

2. **Define the Transformation**
- Express the new coordinates in terms of the original ones.
- $u = \frac{x + y}{2}, \quad v = \frac{x - y}{2}.$

3. **Compute Partial Derivatives**
- Calculate $\frac{\partial x^\mu}{\partial x^{\mu'}}$ for all relevant indices:
- $\frac{\partial x}{\partial u} = 1, \quad
  \frac{\partial x}{\partial v} = 1, \quad
  \frac{\partial y}{\partial u} = 1, \quad
  \frac{\partial y}{\partial v} = -1.$

4. **Apply the Transformation Rule**
- Use the tensor transformation rule:
- $g_{\mu'\nu'} = \frac{\partial x^\mu}{\partial x^{\mu'}} \, \frac{\partial x^\nu}{\partial x^{\nu'}} \, g_{\mu\nu}.$

5. **Simplify the Results**
- Determine the new metric tensor components:
- $g_{\mu'\nu'} = \begin{pmatrix} 2 & 0 \\ 0 & 2 \end{pmatrix}$

---

## 2. Computing Christoffel Symbols

1. **Count the Independent Symbols**
- In 2D, there are $2 \times 3 = 6$ independent Christoffel symbols considering symmetry.

2. **Identify Non-Vanishing Symbols**
- **Condition 1**: Indices in partial derivatives must align with non-zero components of the metric.
- **Condition 2**: Only one partial derivative of the metric is non-zero at a time.

3. **Apply the Connection Formula**
- Compute using:
 $\Gamma^\mu_{\nu\lambda} = \frac{1}{2} \, g^{\mu\rho}
 \bigl(
 \partial_\nu g_{\lambda\rho} +
 \partial_\lambda g_{\nu\rho} -
 \partial_\rho g_{\nu\lambda}
 \bigr).$

4. **List the Non-Zero Symbols**
- In polar coordinates:

 $\Gamma^r_{\phi\phi} = -r, \quad
  \Gamma^\phi_{r\phi} = \Gamma^\phi_{\phi r} = \frac{1}{r}.$

---

## 3. Christoffel Symbols in a 2D Spacetime

1. **Identify the Metric**
    - $ds^2 = -(1+x)^2 dt^2 + dx^2$
    - $g_{\mu\nu} = \begin{pmatrix} -(1+x)^2 & 0 \\ 0 & 1 \end{pmatrix}$

2. **Compute Non-Vanishing Derivatives**
    - $\partial_x g_{tt} = -2(1+x)$

3. **Calculate Christoffel Symbols**
    - $\Gamma^t_{tx} = \Gamma^t_{xt} = \frac{1}{2} g^{tt} \partial_x g_{tt} = \frac{1}{1+x}$
    - $\Gamma^x_{tt} = \frac{1}{2} g^{xx} \partial_x g_{tt} = 1+x$

---

## 4. Christoffel Symbols with Coordinate-Dependent Metric

1. **Identify the Metric**
    - $ds^2 = (1+x^2)dx^2 + (1+y^2)dy^2$
    - $g_{\mu\nu} = \begin{pmatrix} 1+x^2 & 0 \\ 0 & 1+y^2 \end{pmatrix}$

2. **Compute Non-Vanishing Derivatives**
    - $\partial_x g_{xx} = 2x$
    - $\partial_y g_{yy} = 2y$

3. **Calculate Christoffel Symbols**
    - $\Gamma^x_{xx} = \frac{1}{2} g^{xx} \partial_x g_{xx} = \frac{x}{1+x^2}$
    - $\Gamma^x_{yy} = 0$ 