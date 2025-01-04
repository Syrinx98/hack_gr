# Exercise Solution Guide

This concise guide outlines the essential steps to solve the GR (General Relativity) exercises.

## 1. Metric Tensor Transformation

1. **Identify the Original Metric**  
   - Start with the metric tensor $g_{\mu\nu}$ in the initial coordinates.  
   - In Cartesian coordinates $(x, y)$:  
     
     $g_{\mu\nu} = \begin{pmatrix} 1 & 0 \\\ 0 & 1 \end{pmatrix}.$

2. **Define the Transformation**  
   - Express the new coordinates in terms of the original ones.  
   - 

     $u = \frac{x + y}{2}, \quad v = \frac{x - y}{2}.$

3. **Compute Partial Derivatives**  
   - Calculate $\frac{\partial x^\mu}{\partial x^{\mu'}}$ for all relevant indices.  
   - 

     $\frac{\partial x}{\partial u} = 1, \quad
      \frac{\partial x}{\partial v} = 1, \quad
      \frac{\partial y}{\partial u} = 1, \quad
      \frac{\partial y}{\partial v} = -1.$

4. **Apply the Transformation Rule**  
   - Use the tensor transformation rule:

     $g_{\mu'\nu'} = \frac{\partial x^\mu}{\partial x^{\mu'}} \, \frac{\partial x^\nu}{\partial x^{\nu'}} \, g_{\mu\nu}.$

5. **Simplify the Results**  
   - Determine the new metric tensor components.  
   - 

     $g_{\mu'\nu'} = \begin{pmatrix} 2 & 0 \\\ 0 & 2 \end{pmatrix}.$

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
