# Exercise Solution Guide

This concise guide outlines the essential steps to solve the GR (General Relativity) exercises.

Thank for all the contibutors in the telegram group (year 2024/2025):

* Jean-Pierre
* Belli Luigi
* Fulterz
* Margherita
* Sergio Lucci
* NikoG

## 1. Metric Tensor Transformation

1. **Identify the Original Metric**

    * Start with the metric tensor $g_{\mu\nu}$ in the initial coordinates.
    * In Cartesian coordinates $(x, y)$:
        * $g_{\mu\nu} = \left[ 1 \quad 0 \atop 0 \quad 1 \right]$

2. **Define the Transformation**

    * Express the new coordinates in terms of the original ones.
    * $u = \frac{x + y}{2}, \quad v = \frac{x - y}{2}.$

3. **Compute Partial Derivatives**

    * Calculate $\frac{\partial x^\mu}{\partial x^{\mu'}}$ for all relevant indices:
        * $\frac{\partial x}{\partial u} = 1, \quad
          \frac{\partial x}{\partial v} = 1, \quad
          \frac{\partial y}{\partial u} = 1, \quad
          \frac{\partial y}{\partial v} = -1.$

4. **Apply the Transformation Rule**

    * Use the tensor transformation rule:
        * $g_{\mu'\nu'} = \frac{\partial x^\mu}{\partial x^{\mu'}} \, \frac{\partial x^\nu}{\partial x^{\nu'}} \, g_{\mu\nu}.$

5. **Simplify the Results**

    * Determine the new metric tensor components:
        * $g_{\mu'\nu'} = \left[ 2 \quad 0 \atop 0 \quad 2 \right]$

---

## 2. Computing Christoffel Symbols

1. **Count the Independent Symbols**

    * In 2D, there are $2 \times 3 = 6$ independent Christoffel symbols considering symmetry.

2. **Identify Non-Vanishing Symbols**

    * **Condition 1**: Indices in partial derivatives must align with non-zero components of the metric.
    * **Condition 2**: Only one partial derivative of the metric is non-zero at a time.

3. **Apply the Connection Formula**

    * Compute using:
      $\Gamma^\mu_{\nu\lambda} = \frac{1}{2} \, g^{\mu\rho}
      \bigl(
      \partial_\nu g_{\lambda\rho} +
      \partial_\lambda g_{\nu\rho} -
      \partial_\rho g_{\nu\lambda}
      \bigr).$

4. **List the Non-Zero Symbols**

    * In polar coordinates:

      $\Gamma^r_{\phi\phi} = -r, \quad
      \Gamma^\phi_{r\phi} = \Gamma^\phi_{\phi r} = \frac{1}{r}.$

---

## 3. Christoffel Symbols in a 2D Spacetime

1. **Identify the Metric**
    * $ds^2 = -(1+x)^2 dt^2 + dx^2$
    * $g_{\mu\nu} = \left[ -(1+x)^2 \ \quad 0\ \atop 0 \quad \ \ \ \ \ 1 \right]$

2. **Compute Non-Vanishing Derivatives**
    * $\partial_x g_{tt} = -2(1+x)$

3. **Calculate Christoffel Symbols**
    * $\Gamma^t_{tx} = \Gamma^t_{xt} = \frac{1}{2} g^{tt} \partial_x g_{tt} = \frac{1}{1+x}$
    * $\Gamma^x_{tt} = \frac{1}{2} g^{xx} \partial_x g_{tt} = 1+x$

---

## 4. Christoffel Symbols with Coordinate-Dependent Metric

1. **Identify the Metric**
    * $ds^2 = (1+x^2)dx^2 + (1+y^2)dy^2$
    * $g_{\mu\nu} = \left[ 1+x^2 \quad 0 \atop 0 \quad 1+y^2 \right]$

2. **Compute Non-Vanishing Derivatives**
    * $\partial_x g_{xx} = 2x$
    * $\partial_y g_{yy} = 2y$

3. **Calculate Christoffel Symbols**
    * $\Gamma^x_{xx} = \frac{1}{2} g^{xx} \partial_x g_{xx} = \frac{x}{1+x^2}$
    * $\Gamma^x_{yy} = 0$

---

## 5. Gravitational Time Dilation

1. **Metric Approximation:**
    * $ds^2 = -\left(1+2\Phi\right)dt^2 + \left(1-2\Phi\right)dr^2 + r^2d\theta^2 + r^2\sin^2\theta d\phi^2$
    * $\Phi = -\frac{GM_E}{r}$

2. **Scenario:**
    * Two clocks: one at $r = R_E$ and another at $r = R_E + h$.

3. **Proper Time Calculation:**
    * $d\tau = \sqrt{1 + 2\Phi(r)} dt$
    * Clock 1: $\tau_1 = \sqrt{1 - \frac{2GM_E}{R_E}} \times t$
    * Clock 2: $\tau_2 = \sqrt{1 - \frac{2GM_E}{R_E + h}} \times t$

4. **Proper Time Ratio:**
    * $\frac{\tau_2}{\tau_1} = \frac{\sqrt{1 - \frac{2GM_E}{R_E + h}}}{\sqrt{1 - \frac{2GM_E}{R_E}}}$

5. **Approximation for $h \ll R_E$:**
    * Using binomial expansion and weak field approximation:
    * $\frac{\tau_2}{\tau_1} \approx 1 + \frac{GM_E h}{R_E^2}$
    * $\frac{\tau_2}{\tau_1} \approx 1 + \frac{gh}{c^2}$ (in SI units), where $g = \frac{GM_E}{R_E^2}$

---

## 6. Geodesics on a Sphere

1. **Identify the Metric**
    * $ds^2 = d\theta^2 + \sin^2\theta \, d\phi^2$

2. **Identify Non-Vanishing Christoffel Symbols**
    * $\Gamma^\theta_{\phi\phi} = -\sin\theta \cos\theta$
    * $\Gamma^\phi_{\theta\phi} = \Gamma^\phi_{\phi\theta} = \cot\theta$

3. **Write Down the Geodesic Equations**
    * $\frac{d^2 \theta}{d\lambda^2} - \sin\theta \cos\theta \left(\frac{d\phi}{d\lambda}\right)^2 = 0$
    * $\frac{d^2 \phi}{d\lambda^2} + 2 \cot\theta \frac{d\theta}{d\lambda} \frac{d\phi}{d\lambda} = 0$

4. **Lines of Constant Longitude ($\phi = \text{const.}$)**
    * Substitute $\frac{d\phi}{d\lambda} = 0$ and $\frac{d^2\phi}{d\lambda^2} = 0$ into the geodesic equations.
    * The equations are satisfied, confirming that lines of constant longitude are geodesics.

5. **Lines of Constant Latitude ($\theta = \text{const.}$)**
    * Substitute $\frac{d\theta}{d\lambda} = 0$ and $\frac{d^2\theta}{d\lambda^2} = 0$ into the geodesic equations.
    * The first equation reduces to $\sin\theta \cos\theta \left(\frac{d\phi}{d\lambda}\right)^2 = 0$.
    * This is satisfied if $\theta = \frac{\pi}{2}$ (equator) or if $\frac{d\phi}{d\lambda} = 0$ (meridian).
    * The second equation is satisfied, indicating that $\phi$ changes linearly with $\lambda$.
    * Therefore, the only line of constant latitude that is a geodesic is the equator.

---

## 7. Covariant Derivatives on a Sphere

1. **Identify the Metric and Coordinates**
    * $ds^2 = d\theta^2 + \sin^2\theta \, d\phi^2$
    * $x^\mu = (\theta, \phi)$

2. **Recall Non-Vanishing Christoffel Symbols**
    * $\Gamma^\theta_{\phi\phi} = -\sin\theta \cos\theta$
    * $\Gamma^\phi_{\theta\phi} = \Gamma^\phi_{\phi\theta} = \cot\theta$

3. **Compute Covariant Derivative of a Contravariant Vector**
    * $\nabla_\mu V^\nu = \partial_\mu V^\nu + \Gamma^\nu_{\mu\lambda} V^\lambda$
    * $\nabla_\theta V^\theta = \partial_\theta V^\theta$
    * $\nabla_\theta V^\phi = \partial_\theta V^\phi + \cot\theta V^\phi$
    * $\nabla_\phi V^\theta = \partial_\phi V^\theta - \sin\theta \cos\theta V^\phi$
    * $\nabla_\phi V^\phi = \partial_\phi V^\phi + \cot\theta V^\theta$

4. **Compute Covariant Derivative of a Covariant Vector**
    * $\nabla_\mu V_\nu = \partial_\mu V_\nu - \Gamma^\lambda_{\mu\nu} V_\lambda$
    * $\nabla_\theta V_\theta = \partial_\theta V_\theta$
    * $\nabla_\theta V_\phi = \partial_\theta V_\phi - \cot\theta V_\phi$
    * $\nabla_\phi V_\theta = \partial_\phi V_\theta - \cot\theta V_\phi$
    * $\nabla_\phi V_\phi = \partial_\phi V_\phi + \sin\theta \cos\theta V_\theta$

5. **Show $\nabla_\mu (V^\nu V_\nu) = \partial_\mu (V^\nu V_\nu)$**
    * Use the product rule: $\nabla_\mu (V^\nu V_\nu) = V^\nu \nabla_\mu V_\nu + V_\nu \nabla_\mu V^\nu$
    * Substitute the expressions for $\nabla_\mu V^\nu$ and $\nabla_\mu V_\nu$.
    * Show that the terms involving Christoffel symbols cancel out after renaming dummy indices.
    * The result follows: $\nabla_\mu (V^\nu V_\nu) = \partial_\mu (V^\nu V_\nu)$.

---

## 8. Commutator of Covariant Derivatives on a (2,0) Tensor

1. **General Commutator Formula**

   For a $(2,0)$ tensor $W^{\mu\nu}$,
   $[\nabla_\alpha, \nabla_\beta]\ W^{\mu\nu} \ =\ R^\mu_{\ \ \sigma\alpha\beta}\,W^{\sigma\nu} \ +\ R^\nu_{\ \ \sigma\alpha\beta}\,W^{\mu\sigma}.$

2. **Contraction and Conditions**

   After contracting suitable indices (so that we look at $[\nabla_{\mu}, \nabla_{\nu}]\,W^{\mu\nu}$), one obtains
   $[\nabla_{\mu}, \nabla_{\nu}]\,W^{\mu\nu} \ =\ R_{\sigma\nu}\,\bigl(W^{\sigma\nu} \ -\ W^{\nu\sigma}\bigr).$
   This expression vanishes under either of these conditions:
    * $W^{\mu\nu}$ is symmetric, i.e.\ $W^{\mu\nu} = W^{\nu\mu}$.
    * The spacetime is Ricci-flat, $R_{\mu\nu} = 0$.

3. **Different approach**

    Note: also a different approach is possible, if we assume zero torsion, then the commutator of covariant derivatives is always zero. (see box)

---

## 9. Photon Geodesics in 2D Spacetime

1. **Metric and Null Condition**

    * The 2D metric is:
      $ds^2 = -\Bigl(1 + \frac{x^2}{\ell^2}\Bigr)\,dt^2 \ +\ dx^2.$
    * A photon satisfies $ds^2 = 0$ (null geodesic).

2. **Conserved Quantity**

    * The metric does not depend on $t$, so $p_t = g_{t\alpha} \, p^\alpha$ is conserved.
    * Define $p_t = -\,E$, leading to
      $\Bigl(1 + \frac{x^2}{\ell^2}\Bigr)\,\frac{dt}{d\lambda} = E.$

3. **Solve for \(\frac{dx}{d\lambda}\)**

    * From the null condition:
      $0 = -\Bigl(1 + \frac{x^2}{\ell^2}\Bigr)\,\Bigl(\frac{dt}{d\lambda}\Bigr)^2 \ +\ \Bigl(\frac{dx}{d\lambda}\Bigr)^2.$
    * Substitute $\tfrac{dt}{d\lambda} = \tfrac{E}{1 + x^2/\ell^2}$ to get
      $\Bigl(\frac{dx}{d\lambda}\Bigr)^2 = \frac{E^2}{\,1 + \frac{x^2}{\ell^2}\,}.$
    * Therefore,
      $\frac{dx}{d\lambda} = \pm\ \frac{E}{\sqrt{\,1 + \frac{x^2}{\ell^2}\,}}.$

---

## 10. Christoffel Symbols in Schwarzschild Coordinates

1. **Schwarzschild Metric**

    * $ds^2 = -\left(1 - \frac{2GM}{r}\right)dt^2 + \left(1 - \frac{2GM}{r}\right)^{-1}dr^2 + r^2d\theta^2 + r^2\sin^2\theta d\phi^2.$

2. **Compute \(\Gamma^r_{rr}\)**

    * Recall
    * $\Gamma^r_{rr} = \frac{1}{2}g^{rr}\partial_r g_{rr}, \quad g_{rr} = \left(1 - \frac{2GM}{r}\right)^{-1}, \quad g^{rr} = \left(1 - \frac{2GM}{r}\right).$
    * One finds
    * $\Gamma^r_{rr} = -\frac{GM}{r^2}\left(1 - \frac{2GM}{r}\right)^{-1}.$

3. **Compute \(\Gamma^\phi_{r\phi}\)**

    * Recall
    * $\Gamma^\phi_{r\phi} = \frac{1}{2}g^{\phi\phi}\partial_r g_{\phi\phi},\quad g_{\phi\phi} = r^2\sin^2\theta, \quad g^{\phi\phi} = \frac{1}{r^2\sin^2\theta}.$
    * Hence
    * $\Gamma^\phi_{r\phi} = \frac{1}{r}.$

---

## 11. Stable Circular Orbits in Schwarzschild Geometry

1. **Schwarzschild Metric and Conserved Quantities**
    * The Schwarzschild metric is:
      $ds^2 = - \left(1 - \frac{2GM}{r}\right)dt^2 + \left(1 - \frac{2GM}{r}\right)^{-1}dr^2 + r^2 d\theta^2 + r^2 \sin^2\theta d\phi^2.$
    * Conserved quantities for geodesic motion are:
      $E = \left(1 - \frac{2GM}{r}\right) \frac{dt}{d\tau}$ (energy per unit mass)
      $L = r^2 \frac{d\phi}{d\tau}$ (angular momentum per unit mass)

2. **Normalization Condition and Effective Potential**
    * For a massive particle, the four-velocity normalization is:
      $g_{\mu\nu} \frac{dx^\mu}{d\tau} \frac{dx^\nu}{d\tau} = -1$
    * Restricting motion to the equatorial plane ($\theta = \frac{\pi}{2}$), the normalization condition becomes:
      $-\left(1 - \frac{2GM}{r}\right)\left(\frac{dt}{d\tau}\right)^2 + \left(1 - \frac{2GM}{r}\right)^{-1} \left(\frac{dr}{d\tau}\right)^2 + r^2 \left(\frac{d\phi}{d\tau}\right)^2 = -1$
    * Substituting $E$ and $L$ and rearranging, we get:
      $\frac{1}{2}\left(\frac{dr}{d\tau}\right)^2 + V_{\mathrm{eff}}(r) = \frac{E^2}{2}$
    * The effective potential $V_{\mathrm{eff}}(r)$ is:
      $V_{\mathrm{eff}}(r) = -\frac{GM}{r} + \frac{L^2}{2r^2} - \frac{GML^2}{r^3} + \frac{1}{2} = \left(1-\frac{2GM}{r}\right)\left(\frac{L^2}{2r^2}+\frac{1}{2}\right)$

3. **Circular Orbits**
    * For circular orbits, $\frac{dr}{d\tau} = 0$, implying an extremum of the effective potential:
      $\frac{dV_{\mathrm{eff}}}{dr} = 0$
    * This condition leads to the equation:
      $\frac{GM}{r^2} - \frac{L^2}{r^3} + \frac{3 G M L^2}{r^4} = 0$
    * Multiplying by $r^4$ gives a quadratic equation in $r$:
      $GMr^2 - L^2r + 3GML^2 = 0$

4. **Smallest Stable Radius (ISCO)**
    * The quadratic equation has solutions:
      $r = \frac{L^2 \pm \sqrt{L^4 - 12 G^2 M^2 L^2}}{2 G M}$
    * Real solutions exist only if $L^2 \ge 12 G^2 M^2$.
    * At the threshold $L^2 = 12 G^2 M^2$, the two solutions coincide, giving the innermost stable circular orbit (
      ISCO):
      $r_{\text{ISCO}} = 6GM$

## 12. Stable Circular Orbits in Schwarzschild Geometry (Continued)

1. **Effective Potential**
    * The effective potential $V_{\mathrm{eff}}(r)$ is:
      $V_{\mathrm{eff}}(r) = -\frac{GM}{r} + \frac{L^2}{2r^2} - \frac{GML^2}{r^3} + \frac{1}{2} = \left(1-\frac{2GM}{r}\right)\left(\frac{L^2}{2r^2}+\frac{1}{2}\right)$

2. **Circular Orbits**
    * For circular orbits, $\frac{dr}{d\tau} = 0$, implying an extremum of the effective potential:
      $\frac{dV_{\mathrm{eff}}}{dr} = 0$
    * This condition leads to the equation:
      $\frac{GM}{r^2} - \frac{L^2}{r^3} + \frac{3 G M L^2}{r^4} = 0$
    * Multiplying by $r^4$ gives a quadratic equation in $r$:
      $GMr^2 - L^2r + 3GML^2 = 0$

3. **Smallest Stable Radius (ISCO)**
    * The quadratic equation has solutions:
      $r = \frac{L^2 \pm \sqrt{L^4 - 12 G^2 M^2 L^2}}{2 G M}$
    * Real solutions exist only if $L^2 \ge 12 G^2 M^2$.
    * At the threshold $L^2 = 12 G^2 M^2$, the two solutions coincide, giving the innermost stable circular orbit (
      ISCO):
      $r_{\text{ISCO}} = 6GM$

4. **Stable Orbit in the \(L \to \infty\) Limit**
    * For large \(L\), the stable orbit radius is approximately:
      $r \approx \frac{L^2}{GM}$
    * This matches the Newtonian result in the same limit.

## 13. Circular Orbits for Massless Objects in Schwarzschild Geometry

1. **Schwarzschild Metric and Conserved Quantities**
    * The Schwarzschild metric is:
      $ds^2 = - \left(1 - \frac{2GM}{r}\right)dt^2 + \left(1 - \frac{2GM}{r}\right)^{-1}dr^2 + r^2 d\theta^2 + r^2 \sin^2\theta d\phi^2.$
    * Conserved quantities for geodesic motion are:
      $E = \left(1 - \frac{2GM}{r}\right) \frac{dt}{d\lambda}$ (energy)
      $L = r^2 \frac{d\phi}{d\lambda}$ (angular momentum)

2. **Normalization Condition and Effective Potential**
    * For a massless particle, the four-momentum normalization is:
      $g_{\mu\nu} \frac{dx^\mu}{d\lambda} \frac{dx^\nu}{d\lambda} = 0$
    * Restricting motion to the equatorial plane ($\theta = \frac{\pi}{2}$), the normalization condition becomes:
      $-\left(1 - \frac{2GM}{r}\right)\left(\frac{dt}{d\lambda}\right)^2 + \left(1 - \frac{2GM}{r}\right)^{-1} \left(\frac{dr}{d\lambda}\right)^2 + r^2 \left(\frac{d\phi}{d\lambda}\right)^2 = 0$
    * Substituting $E$ and $L$ and rearranging, we get:
      $\frac{1}{2}\left(\frac{dr}{d\lambda}\right)^2 + V_{\mathrm{eff}}(r) = \frac{E^2}{2}$
    * The effective potential $V_{\mathrm{eff}}(r)$ is:
      $V_{\mathrm{eff}}(r) = \frac{L^2}{2r^2}\left(1-\frac{2GM}{r}\right)$

3. **Circular Orbits**
    * For circular orbits, $\frac{dr}{d\lambda} = 0$, implying an extremum of the effective potential:
      $\frac{dV_{\mathrm{eff}}}{dr} = 0$
    * Setting $GM=1$ and $L=10$, this condition leads to the equation:
      $-\frac{100}{r^3} + \frac{300}{r^4} = 0$, that is solved for $r = 3GM$.

* Thus, the radius of the circular orbit for a massless particle is:
  $r = 3GM$

4. **Stability of the Circular Orbit**
    * To check stability, we compute the second derivative of the effective potential:
      $\frac{d^2 V_{\text{eff}}}{dr^2} = \frac{3L^2}{r^4} - \frac{12GML^2}{r^5}$
    * Evaluating at $r = 3GM$, we get:
      $\frac{d^2 V_{\text{eff}}}{dr^2}\Big|_{r=3GM} = -\frac{L^2}{81(GM)^4} < 0$
    * Since the second derivative is negative, the circular orbit at $r = 3GM$ is unstable.

---

## 14. Minimum Energy for Photon to Reach Singularity in Schwarzschild Geometry

1. **Schwarzschild Metric and Conserved Quantities**
    * The Schwarzschild metric is:
      $ds^2 = - \left(1 - \frac{2GM}{r}\right)dt^2 + \left(1 - \frac{2GM}{r}\right)^{-1}dr^2 + r^2 d\theta^2 + r^2 \sin^2\theta d\phi^2.$
    * Conserved quantities for geodesic motion are:
      $E = \left(1 - \frac{2GM}{r}\right) \frac{dt}{d\lambda}$ (energy)
      $L = r^2 \frac{d\phi}{d\lambda}$ (angular momentum)

2. **Normalization Condition and Effective Potential**
    * For a massless particle (photon), the four-momentum normalization is:
      $g_{\mu\nu} \frac{dx^\mu}{d\lambda} \frac{dx^\nu}{d\lambda} = 0$
    * Restricting motion to the equatorial plane ($\theta = \frac{\pi}{2}$), the normalization condition becomes:
      $-\left(1 - \frac{2GM}{r}\right)\left(\frac{dt}{d\lambda}\right)^2 + \left(1 - \frac{2GM}{r}\right)^{-1} \left(\frac{dr}{d\lambda}\right)^2 + r^2 \left(\frac{d\phi}{d\lambda}\right)^2 = 0$
    * Substituting $E$ and $L$ and rearranging, we get:
      $\frac{1}{2}\left(\frac{dr}{d\lambda}\right)^2 + V_{\mathrm{eff}}(r) = \frac{E^2}{2}$
    * The effective potential $V_{\mathrm{eff}}(r)$ is:
      $V_{\mathrm{eff}}(r) = \frac{L^2}{2r^2}\left(1-\frac{2GM}{r}\right)$

3. **Conditions for Reaching the Singularity**
    * Setting $GM=1$ and $L=10$, the effective potential becomes:
      $V_{\mathrm{eff}}(r) = \frac{50}{r^2} - \frac{100}{r^3}$
    * To reach the singularity at $r=0$, the photon's energy must be greater than or equal to the maximum value of the
      effective potential.
    * The maximum of $V_{\mathrm{eff}}$ occurs at $r_{\text{max}} = 3GM = 3$ (in units where $GM=1$).
    * The value of the effective potential at this maximum is:
      $V_{\mathrm{eff}}(3) = \frac{50}{27}$

4. **Minimum Energy**
    * The photon can reach the singularity if $\frac{E^2}{2} \ge V_{\mathrm{eff}}(3)$.
    * Therefore, the minimum energy required is:
      $E_{\min} = \sqrt{2 V_{\mathrm{eff}}(3)} = \frac{10}{3\sqrt{3}}$

---

## 15. Gauge Transformations in Linearized Gravity

1.  **Definition of $V_\mu$**

    *   Define the vector $V_\mu$ as:
        * $V_\mu = \partial_\nu h^\nu_\mu - \frac{1}{2} \partial_\mu h^\nu_\nu$
    *   $h^\nu_\mu = \eta^{\nu\alpha}h_{\mu\alpha}$ and $h^\nu_\nu = \eta^{\nu\alpha}h_{\nu\alpha}$ is the trace of $h_{\mu\nu}$.

2.  **Infinitesimal Gauge Transformation**

    *   Consider a small coordinate transformation:
        * $x^\mu \to x^\mu + \xi^\mu$
    *   The metric perturbation $h_{\mu\nu}$ transforms as:
        * $h_{\mu\nu} \to h_{\mu\nu} + \partial_\mu \xi_\nu + \partial_\nu \xi_\mu$
    *   $\xi_\mu = \eta_{\mu\alpha} \xi^\alpha$

3.  **Transformation of $V_\mu$**

    *   Under the gauge transformation, $V_\mu$ transforms as:
        * $V_\mu \to V_\mu + \Box \xi_\mu$
    *   $\Box = \partial^\alpha \partial_\alpha$ is the d'Alembert operator.

4.  **Existence of Lorenz Gauge**

    *   It is always possible to find a gauge where $V_\mu = 0$ (Lorenz gauge).
    *   This is achieved by choosing $\xi_\mu$ such that:
        * $\Box \xi_\mu = -V_\mu$
    *   The existence of a solution to this inhomogeneous wave equation guarantees that the Lorenz gauge can always be reached.

---

## 16. Gravitational Wave Polarization and Gauge Transformations

1.  **Plane Wave in TT Gauge**

    *   Consider a plane wave propagating in the positive z-direction:
        * $h_{\mu\nu}^{TT} = Re(C_{\mu\nu} e^{ik_\sigma x^\sigma})$
    *   $k^\mu = (\omega, 0, 0, \omega)$ for a wave propagating along the positive z-axis.

2.  **Polarization Tensor  $C_{\mu\nu}$ for '+' Polarization**

    *   $C_{\mu\nu}$ is symmetric: $C_{\mu\nu} = C_{\nu\mu}$.
    *   Transversality: $k^\mu C_{\mu\nu} = 0 \implies C_{0\nu} = -C_{3\nu}$
    *   Tracelessness: $C^\mu_\mu = 0 \implies C_{00} = C_{33}, C_{11} = -C_{22}$.
    *   For '+' polarization in standard TT gauge: $C_{11} = -C_{22} = C_+$ and $C_{12} = C_{21} = 0$, $C_{0\nu} = C_{3\nu} = 0$.
    *   Explicitly:
        * $C_{\mu\nu} = \begin{pmatrix}
        0 & 0 & 0 & 0 \\
        0 & C_+ & 0 & 0 \\
        0 & 0 & -C_+ & 0 \\
        0 & 0 & 0 & 0
        \end{pmatrix}$

3.  **Gauge Transformation**

    *   Consider a gauge transformation:
        * $\xi^\mu = (\alpha(x^\mu), \beta(x^\mu), 0, 0)$
    *   The metric perturbation transforms as:
        * $h_{\mu\nu} \to h'_{\mu\nu} = h_{\mu\nu} + \partial_\mu \xi_\nu + \partial_\nu \xi_\mu$
    *   Compute $\partial_\mu \xi_\nu + \partial_\nu \xi_\mu$, where $\xi_\nu = (-\alpha, \beta, 0, 0)$, by explicitly calculating all the partial derivatives.
    *   The transformed metric perturbation is:
        * $h'_{\mu\nu} = \begin{pmatrix}
        -2\partial_0 \alpha & \partial_0 \beta - \partial_1 \alpha & -\partial_2 \alpha & -\partial_3 \alpha \\
        \partial_0 \beta - \partial_1 \alpha & C_{+} \cos(\omega(t-z)) + 2\partial_1 \beta & \partial_2 \beta & \partial_3 \beta \\
        -\partial_2 \alpha & \partial_2 \beta & -C_{+} \cos(\omega(t-z)) & 0 \\
        -\partial_3 \alpha & \partial_3 \beta & 0 & 0
        \end{pmatrix}$