# Exercise Solution Guide

This concise guide outlines the essential steps to solve the GR exercises.

## **1. Metric Tensor Transformation**

1. **Identify Original Metric:**
   - Start with the metric tensor $g_{\mu\nu}$ in the initial coordinates.
   - *Example:* In Cartesian coordinates $(x, y)$:

   $
   g_{\mu\nu} = \begin{pmatrix}
     1 & 0 \\
     0 & 1
   \end{pmatrix}.
   $

2. **Define Transformation:**
   - Express new coordinates in terms of the original ones.
   - *Example:* \(u = \frac{x + y}{2}\), \(v = \frac{x - y}{2}\).

3. **Compute Partial Derivatives:**
   - Calculate \(\frac{\partial x^\mu}{\partial x^{\mu'}}\) for all relevant indices.
   - *Example:*

   $
   \frac{\partial x}{\partial u} = 1, \quad
   \frac{\partial x}{\partial v} = 1, \quad
   \frac{\partial y}{\partial u} = 1, \quad
   \frac{\partial y}{\partial v} = -1.
   $

4. **Apply Transformation Rule:**
   - Use the tensor transformation rule:

   $
   g_{\mu'\nu'} = \frac{\partial x^\mu}{\partial x^{\mu'}} \,
                  \frac{\partial x^\nu}{\partial x^{\nu'}} \,
                  g_{\mu\nu}.
   $

5. **Simplify Results:**
   - Determine the new metric tensor components.
   - *Example:*

   $
   g_{\mu'\nu'} = \begin{pmatrix}
     2 & 0 \\
     0 & 2
   \end{pmatrix}.
   $

## **2. Computing Christoffel Symbols**

1. **Count Independent Symbols:**
   - For 2D, there are \(2 \times 3 = 6\) independent Christoffel symbols considering symmetry.

2. **Identify Non-Vanishing Symbols:**
   - **Condition 1:** Indices in partial derivatives must align with metric components.
   - **Condition 2:** Only one partial derivative of the metric is non-zero.

3. **Apply Connection Formula:**
   - Compute using:

   $
   \Gamma^\mu_{\nu\lambda} = \frac{1}{2} \, g^{\mu\rho}
   \bigl(
     \partial_\nu g_{\lambda\rho}
     + \partial_\lambda g_{\nu\rho}
     - \partial_\rho g_{\nu\lambda}
   \bigr).
   $

4. **List Non-Zero Symbols:**
   - *Example:* In polar coordinates,

   $
   \Gamma^r_{\phi\phi} = -r, \quad
   \Gamma^\phi_{r\phi} = \Gamma^\phi_{\phi r} = \frac{1}{r}.
   $
