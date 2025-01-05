# Exercise Solution Guide

This concise guide outlines the essential steps to solve the GR (General Relativity) exercises.

## 1. Metric Tensor Transformation

1.  **Identify the Original Metric**

    *   Start with the metric tensor $g_{\mu\nu}$ in the initial coordinates.
    *   In Cartesian coordinates $(x, y)$:
        *   $g_{\mu\nu} = \left[ 1 \quad 0 \atop 0 \quad 1 \right]$

2.  **Define the Transformation**

    *   Express the new coordinates in terms of the original ones.
    *   $u = \frac{x + y}{2}, \quad v = \frac{x - y}{2}.$

3.  **Compute Partial Derivatives**

    *   Calculate $\frac{\partial x^\mu}{\partial x^{\mu'}}$ for all relevant indices:
        *   $\frac{\partial x}{\partial u} = 1, \quad
            \frac{\partial x}{\partial v} = 1, \quad
            \frac{\partial y}{\partial u} = 1, \quad
            \frac{\partial y}{\partial v} = -1.$

4.  **Apply the Transformation Rule**

    *   Use the tensor transformation rule:
        *   $g_{\mu'\nu'} = \frac{\partial x^\mu}{\partial x^{\mu'}} \, \frac{\partial x^\nu}{\partial x^{\nu'}} \, g_{\mu\nu}.$

5.  **Simplify the Results**

    *   Determine the new metric tensor components:
        *   $g_{\mu'\nu'} = \left[ 2 \quad 0 \atop 0 \quad 2 \right]$

---

## 2. Computing Christoffel Symbols

1.  **Count the Independent Symbols**

    *   In 2D, there are $2 \times 3 = 6$ independent Christoffel symbols considering symmetry.

2.  **Identify Non-Vanishing Symbols**

    *   **Condition 1**: Indices in partial derivatives must align with non-zero components of the metric.
    *   **Condition 2**: Only one partial derivative of the metric is non-zero at a time.

3.  **Apply the Connection Formula**

    *   Compute using:
        $\Gamma^\mu_{\nu\lambda} = \frac{1}{2} \, g^{\mu\rho}
        \bigl(
        \partial_\nu g_{\lambda\rho} +
        \partial_\lambda g_{\nu\rho} -
        \partial_\rho g_{\nu\lambda}
        \bigr).$

4.  **List the Non-Zero Symbols**

    *   In polar coordinates:

        $\Gamma^r_{\phi\phi} = -r, \quad
        \Gamma^\phi_{r\phi} = \Gamma^\phi_{\phi r} = \frac{1}{r}.$

---

## 3. Christoffel Symbols in a 2D Spacetime

1.  **Identify the Metric**
    *   $ds^2 = -(1+x)^2 dt^2 + dx^2$
    *   $g_{\mu\nu} = \left[ -(1+x)^2 \ \quad 0\ \atop 0 \quad \ \ \ \ \ 1 \right]$

2.  **Compute Non-Vanishing Derivatives**
    *   $\partial_x g_{tt} = -2(1+x)$

3.  **Calculate Christoffel Symbols**
    *   $\Gamma^t_{tx} = \Gamma^t_{xt} = \frac{1}{2} g^{tt} \partial_x g_{tt} = \frac{1}{1+x}$
    *   $\Gamma^x_{tt} = \frac{1}{2} g^{xx} \partial_x g_{tt} = 1+x$

---

## 4. Christoffel Symbols with Coordinate-Dependent Metric

1.  **Identify the Metric**
    *   $ds^2 = (1+x^2)dx^2 + (1+y^2)dy^2$
    *   $g_{\mu\nu} = \left[ 1+x^2 \quad 0 \atop 0 \quad 1+y^2 \right]$

2.  **Compute Non-Vanishing Derivatives**
    *   $\partial_x g_{xx} = 2x$
    *   $\partial_y g_{yy} = 2y$

3.  **Calculate Christoffel Symbols**
    *   $\Gamma^x_{xx} = \frac{1}{2} g^{xx} \partial_x g_{xx} = \frac{x}{1+x^2}$
    *   $\Gamma^x_{yy} = 0$

---

## 5. Gravitational Time Dilation

1.  **Metric Approximation:**
    *   $ds^2 = -\left(1+2\Phi\right)dt^2 + \left(1-2\Phi\right)dr^2 + r^2d\theta^2 + r^2\sin^2\theta d\phi^2$
    *   $\Phi = -\frac{GM_E}{r}$

2.  **Scenario:**
    *   Two clocks: one at $r = R_E$ and another at $r = R_E + h$.

3.  **Proper Time Calculation:**
    *   $d\tau = \sqrt{1 + 2\Phi(r)} dt$
    *   Clock 1: $\tau_1 = \sqrt{1 - \frac{2GM_E}{R_E}} \times t$
    *   Clock 2: $\tau_2 = \sqrt{1 - \frac{2GM_E}{R_E + h}} \times t$

4.  **Proper Time Ratio:**
    - $\frac{\tau_2}{\tau_1} = \frac{\sqrt{1 - \frac{2GM_E}{R_E + h}}}{\sqrt{1 - \frac{2GM_E}{R_E}}}$

5.  **Approximation for $h \ll R_E$:**
    *   Using binomial expansion and weak field approximation:
    *   $\frac{\tau_2}{\tau_1} \approx 1 + \frac{GM_E h}{R_E^2}$
    *   $\frac{\tau_2}{\tau_1} \approx 1 + \frac{gh}{c^2}$ (in SI units), where $g = \frac{GM_E}{R_E^2}$