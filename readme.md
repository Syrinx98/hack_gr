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
    *   $\frac{\tau_2}{\tau_1} = \frac{\sqrt{1 - \frac{2GM_E}{R_E + h}}}{\sqrt{1 - \frac{2GM_E}{R_E}}}$

5.  **Approximation for $h \ll R_E$:**
    *   Using binomial expansion and weak field approximation:
    *   $\frac{\tau_2}{\tau_1} \approx 1 + \frac{GM_E h}{R_E^2}$
    *   $\frac{\tau_2}{\tau_1} \approx 1 + \frac{gh}{c^2}$ (in SI units), where $g = \frac{GM_E}{R_E^2}$

---

## 6. Geodesics on a Sphere

1.  **Identify the Metric**
    *   $ds^2 = d\theta^2 + \sin^2\theta \, d\phi^2$

2.  **Identify Non-Vanishing Christoffel Symbols**
    *   $\Gamma^\theta_{\phi\phi} = -\sin\theta \cos\theta$
    *   $\Gamma^\phi_{\theta\phi} = \Gamma^\phi_{\phi\theta} = \cot\theta$

3.  **Write Down the Geodesic Equations**
    *   $\frac{d^2 \theta}{d\lambda^2} - \sin\theta \cos\theta \left(\frac{d\phi}{d\lambda}\right)^2 = 0$
    *   $\frac{d^2 \phi}{d\lambda^2} + 2 \cot\theta \frac{d\theta}{d\lambda} \frac{d\phi}{d\lambda} = 0$

4.  **Lines of Constant Longitude ($\phi = \text{const.}$)**
    *   Substitute $\frac{d\phi}{d\lambda} = 0$ and $\frac{d^2\phi}{d\lambda^2} = 0$ into the geodesic equations.
    *   The equations are satisfied, confirming that lines of constant longitude are geodesics.

5.  **Lines of Constant Latitude ($\theta = \text{const.}$)**
    *   Substitute $\frac{d\theta}{d\lambda} = 0$ and $\frac{d^2\theta}{d\lambda^2} = 0$ into the geodesic equations.
    *   The first equation reduces to $\sin\theta \cos\theta \left(\frac{d\phi}{d\lambda}\right)^2 = 0$.
    *   This is satisfied if $\theta = \frac{\pi}{2}$ (equator) or if $\frac{d\phi}{d\lambda} = 0$ (meridian).
    *   The second equation is satisfied, indicating that $\phi$ changes linearly with $\lambda$.
    *   Therefore, the only line of constant latitude that is a geodesic is the equator.

---

## 7. Covariant Derivatives on a Sphere

1.  **Identify the Metric and Coordinates**
    *   $ds^2 = d\theta^2 + \sin^2\theta \, d\phi^2$
    *   $x^\mu = (\theta, \phi)$

2.  **Recall Non-Vanishing Christoffel Symbols**
    *   $\Gamma^\theta_{\phi\phi} = -\sin\theta \cos\theta$
    *   $\Gamma^\phi_{\theta\phi} = \Gamma^\phi_{\phi\theta} = \cot\theta$

3.  **Compute Covariant Derivative of a Contravariant Vector**
    *   $\nabla_\mu V^\nu = \partial_\mu V^\nu + \Gamma^\nu_{\mu\lambda} V^\lambda$
    *   $\nabla_\theta V^\theta = \partial_\theta V^\theta$
    *   $\nabla_\theta V^\phi = \partial_\theta V^\phi + \cot\theta V^\phi$
    *   $\nabla_\phi V^\theta = \partial_\phi V^\theta - \sin\theta \cos\theta V^\phi$
    *   $\nabla_\phi V^\phi = \partial_\phi V^\phi + \cot\theta V^\theta$

4.  **Compute Covariant Derivative of a Covariant Vector**
    *   $\nabla_\mu V_\nu = \partial_\mu V_\nu - \Gamma^\lambda_{\mu\nu} V_\lambda$
    *   $\nabla_\theta V_\theta = \partial_\theta V_\theta$
    *   $\nabla_\theta V_\phi = \partial_\theta V_\phi - \cot\theta V_\phi$
    *   $\nabla_\phi V_\theta = \partial_\phi V_\theta - \cot\theta V_\phi$
    *   $\nabla_\phi V_\phi = \partial_\phi V_\phi + \sin\theta \cos\theta V_\theta$

5.  **Show $\nabla_\mu (V^\nu V_\nu) = \partial_\mu (V^\nu V_\nu)$**
    *   Use the product rule: $\nabla_\mu (V^\nu V_\nu) = V^\nu \nabla_\mu V_\nu + V_\nu \nabla_\mu V^\nu$
    *   Substitute the expressions for $\nabla_\mu V^\nu$ and $\nabla_\mu V_\nu$.
    *   Show that the terms involving Christoffel symbols cancel out after renaming dummy indices.
    *   The result follows: $\nabla_\mu (V^\nu V_\nu) = \partial_\mu (V^\nu V_\nu)$.

---

## 8. Commutator of Covariant Derivatives on a (2,0) Tensor

1. **General Commutator Formula**

   For a $(2,0)$ tensor $W^{\mu\nu}$,
   $[\nabla_\alpha, \nabla_\beta]\ W^{\mu\nu} \ =\  R^\mu_{\ \ \sigma\alpha\beta}\,W^{\sigma\nu} \ +\  R^\nu_{\ \ \sigma\alpha\beta}\,W^{\mu\sigma}.$

2. **Contraction and Conditions**

   After contracting suitable indices (so that we look at $[\nabla_{\mu}, \nabla_{\nu}]\,W^{\mu\nu}$), one obtains
   $[\nabla_{\mu}, \nabla_{\nu}]\,W^{\mu\nu} \ =\ R_{\sigma\nu}\,\bigl(W^{\sigma\nu} \ -\  W^{\nu\sigma}\bigr).$
   This expression vanishes under either of these conditions:
   *   $W^{\mu\nu}$ is symmetric, i.e.\ $W^{\mu\nu} = W^{\nu\mu}$.
   *   The spacetime is Ricci-flat, $R_{\mu\nu} = 0$.

---

## 9. Photon Geodesics in 2D Spacetime

1. **Metric and Null Condition**

   *   The 2D metric is:
     $ds^2 = -\Bigl(1 + \frac{x^2}{\ell^2}\Bigr)\,dt^2 \ +\ dx^2.$
   *   A photon satisfies $ds^2 = 0$ (null geodesic).

2. **Conserved Quantity**

   *   The metric does not depend on $t$, so $p_t = g_{t\alpha} \, p^\alpha$ is conserved.
   *   Define $p_t = -\,E$, leading to
     $\Bigl(1 + \frac{x^2}{\ell^2}\Bigr)\,\frac{dt}{d\lambda} = E.$

3. **Solve for \(\frac{dx}{d\lambda}\)**

   *   From the null condition:
     $0 = -\Bigl(1 + \frac{x^2}{\ell^2}\Bigr)\,\Bigl(\frac{dt}{d\lambda}\Bigr)^2 \ +\ \Bigl(\frac{dx}{d\lambda}\Bigr)^2.$
   *   Substitute $\tfrac{dt}{d\lambda} = \tfrac{E}{1 + x^2/\ell^2}$ to get
     $\Bigl(\frac{dx}{d\lambda}\Bigr)^2 = \frac{E^2}{\,1 + \frac{x^2}{\ell^2}\,}.$
   *   Therefore,
     $\frac{dx}{d\lambda} = \pm\ \frac{E}{\sqrt{\,1 + \frac{x^2}{\ell^2}\,}}.$

---

## 10. Christoffel Symbols in Schwarzschild Coordinates

1. **Schwarzschild Metric**

   * $ ds^2 = -\Bigl(1 - \tfrac{2GM}{r}\Bigr)\,dt^2 \ +\ \Bigl(1 - \tfrac{2GM}{r}\Bigr)^{-1}\,dr^2 \ +\ r^2\,d\theta^2 \ +\ r^2\,\sin^2\theta\,d\phi^2.$

2. **Compute \(\Gamma^r_{rr}\)**

   *   Recall
     * $\Gamma^r_{rr} = \tfrac12\,g^{rr}\,\partial_r g_{rr}, \quad g_{rr} = \Bigl(1 - \tfrac{2GM}{r}\Bigr)^{-1}, \quad g^{rr} = \Bigl(1 - \tfrac{2GM}{r}\Bigr).$
   *   One finds
     * $\Gamma^r_{rr} = -\,\frac{GM}{r^2}\,\Bigl(1 - \tfrac{2GM}{r}\Bigr)^{-1}.$

3. **Compute \(\Gamma^\phi_{r\phi}\)**

   *   Recall
     * $ \Gamma^\phi_{r\phi}=\tfrac12\,g^{\phi\phi}\,\partial_r g_{\phi\phi},\quad g_{\phi\phi} = r^2\,\sin^2\theta, \quad g^{\phi\phi} = \frac{1}{\,r^2\,\sin^2\theta\,}.$
   *   Hence
     * $ \Gamma^\phi_{r\phi} = \frac{1}{r}.$
