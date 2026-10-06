<!-- week-id: 2026-W38 -->
<!-- generated-at: 2026-10-07T10:43:22.927900+13:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Study period: 2026-W38, from 2026-09-14T00:00:00+12:00 to 2026-09-20T23:59:00+12:00.
- Covered lectures:
  - Lecture 29: Quiz 2 review, Quiz 3 guidance, transient heat equation derivation, and separation of variables.
  - Lecture 30: Mesh convergence, non-dimensionalisation, similarity solutions, error-function diffusion, and mixed boundary conditions.
  - Lecture 31: Finite-difference methods, FTCS, BTCS, stability, convergence, and ghost nodes.
  - Lecture 32: Crank–Nicolson, numerical-method comparison, mass diffusion, and dimensionless diffusion.
- Coverage is complete for the four specified lectures.

## Main concepts

- Laplace’s equation is an elliptic, steady-state diffusion equation; the heat equation is a parabolic, time-dependent diffusion equation.
- The one-dimensional heat equation follows from conservation of energy and Fourier’s law under constant area, uniform material properties, and negligible lateral heat transfer.
- Separation of variables represents the temperature as a product of spatial and temporal functions. Boundary conditions determine eigenvalues and spatial modes; the initial condition determines their coefficients.
- Thermal diffusivity controls how quickly temperature differences spread.
- Non-dimensionalisation uses characteristic scales to reduce parameters, reveal dominant behaviour, improve numerical conditioning, and allow results to apply across physically similar systems.
- In a semi-infinite slab, the diffusion length grows approximately as \(\sqrt{\alpha t}\). Combining position and time into a similarity variable reduces the PDE to an ODE.
- Mesh convergence requires numerical results to approach stable values as the mesh is refined. Both the maximum value and its location may need to be monitored.
- FTCS is simple and computationally cheap but conditionally stable.
- BTCS is implicit, requires a coupled matrix solve, and is described in the lectures as unconditionally stable for the linear diffusion problem. Stability does not guarantee accuracy for large time steps.
- Crank–Nicolson averages the spatial diffusion term between two time levels. It is second-order accurate in both time and space.
- Heat diffusion and mass diffusion have the same mathematical structure after replacing temperature \(T\) with concentration \(C\), and thermal diffusivity \(\alpha\) with mass diffusivity \(D\).

## Equations and worked patterns

- One-dimensional heat equation:
  
  \[
  \frac{\partial T}{\partial t}
  =
  \alpha\frac{\partial^2T}{\partial x^2}
  \]

- Thermal diffusivity:
  
  \[
  \alpha=\frac{k}{\rho c}
  \]

- Characteristic diffusion time:
  
  \[
  t_0=\frac{L^2}{\alpha}
  \]

- Similarity variable for a semi-infinite slab:
  
  \[
  \eta=\frac{x}{2\sqrt{\alpha t}}
  \]

- Error-function solution:
  
  \[
  \frac{T-T_\infty}{T_1-T_\infty}
  =
  \operatorname{erf}
  \left(
  \frac{x}{2\sqrt{\alpha t}}
  \right)
  \]

- Copper-bar single-mode solution:
  
  \[
  T(x,t)
  =
  100\sin\left(\frac{\pi x}{L}\right)
  \exp\left[-\alpha\left(\frac{\pi}{L}\right)^2t\right]
  \]

- Maximum-temperature decay:
  
  \[
  T_{\max}(t)
  =
  100\exp\left[-\alpha\left(\frac{\pi}{L}\right)^2t\right]
  \]

- Time for the maximum temperature to reach a target value:
  
  \[
  t_f
  =
  \frac{-\ln(T_f/T_0)}
  {\alpha(\pi/L)^2}
  \]

- Central-difference spatial approximation:
  
  \[
  \frac{\partial^2T}{\partial x^2}
  \approx
  \frac{T_{i-1}-2T_i+T_{i+1}}{\Delta x^2}
  \]

- Forward-time approximation:
  
  \[
  \frac{\partial T}{\partial t}
  \approx
  \frac{T_i^{n+1}-T_i^n}{\Delta t}
  \]

- FTCS update:
  
  \[
  T_i^{n+1}
  =
  T_i^n
  +
  \lambda
  \left(
  T_{i-1}^n-2T_i^n+T_{i+1}^n
  \right)
  \]

  where

  \[
  \lambda=\frac{\alpha\Delta t}{\Delta x^2}
  \]

- FTCS stability requirement:
  
  \[
  \lambda\leq\frac{1}{2}
  \]

  equivalently,

  \[
  \Delta t\leq\frac{\Delta x^2}{2\alpha}
  \]

- BTCS equation:
  
  \[
  -\lambda T_{i-1}^{n+1}
  +(1+2\lambda)T_i^{n+1}
  -\lambda T_{i+1}^{n+1}
  =
  T_i^n
  \]

- Neumann boundary condition using a ghost node:
  
  \[
  \frac{T_1-T_{-1}}{2\Delta x}=\beta
  \]

  therefore,

  \[
  T_{-1}=T_1-2\beta\Delta x
  \]

- Crank–Nicolson equation:
  
  \[
  -\lambda T_{i-1}^{n+1}
  +2(1+\lambda)T_i^{n+1}
  -\lambda T_{i+1}^{n+1}
  =
  \lambda T_{i-1}^{n}
  +2(1-\lambda)T_i^{n}
  +\lambda T_{i+1}^{n}
  \]

- Implicit and Crank–Nicolson schemes are written as:

  \[
  \mathbf{A}\mathbf{T}^{n+1}=\mathbf{B}^{n}
  \]

  The coefficient matrix remains unchanged when the grid, time step, and diffusivity remain constant; the right-hand side changes at each time step.

- Mass-diffusion equation:

  \[
  \frac{\partial C}{\partial t}
  =
  D\frac{\partial^2C}{\partial x^2}
  \]

- Dimensionless mass-diffusion variables:

  \[
  \tilde{x}=\frac{x}{L},
  \qquad
  \tilde{t}=\frac{Dt}{L^2},
  \qquad
  \tilde{C}=\frac{C-C_0}{C_s-C_0}
  \]

## Warnings and deadlines

- Quiz 3 was stated to be due on Friday of the lecture week.
- For numerical results, check physical shape, units, boundary conditions, mesh convergence, and sensitivity of both maxima and their locations.
- Use consistent units. In particular, do not combine a length in centimetres with thermal diffusivity in \(\mathrm{m^2/s}\) without conversion.
- The explicit heat-equation scheme becomes unstable when \(\lambda>1/2\). Instability may produce negative or excessively large temperatures outside the physical boundary range.
- An implicit method can be stable but inaccurate when the time step is too large.
- For the circular-domain problem, the location of maximum displacement may be more mesh-sensitive than the maximum value.
- Use the correct units when reporting quiz answers; a numerically correct value with an incorrect unit may be physically incorrect and lose marks.
- Some source notes contain uncertain numerical examples and reconstructed equations. The general methods and equations are clear, but garbled node-by-node values, material data, and benchmark coordinates should not be treated as authoritative without checking the original course material.

## Recall questions

1. What assumptions permit the three-dimensional rod to be represented by the one-dimensional heat equation?
2. Why is a negative separation constant used for the ordinary diffusion solution?
3. How does the initial condition determine the coefficients in a separation-of-variables series?
4. Why is \(t_0=L^2/\alpha\) a useful characteristic diffusion time?
5. Why does the semi-infinite slab use the similarity variable \(\eta=x/(2\sqrt{\alpha t})\)?
6. What is the difference between convergence and stability in a finite-difference calculation?
7. Derive the FTCS stability condition \(\lambda\leq 1/2\) from the coefficient \(1-2\lambda\).
8. Why does halving \(\Delta x\) require reducing the explicit time step by a factor of four?
9. Why does BTCS require a simultaneous matrix solve while FTCS does not?
10. What does Crank–Nicolson average between time levels \(n\) and \(n+1\)?

## Practice priorities

1. Derive the one-dimensional heat equation from the differential-element energy balance and Fourier’s law.
2. Work through separation of variables for fixed-temperature boundaries, including eigenvalues, temporal decay, and initial-condition coefficients.
3. Rework the copper-bar maximum-temperature calculation with all lengths and diffusivities expressed in consistent SI units.
4. Non-dimensionalise the heat equation and verify that choosing \(t_0=L^2/\alpha\) removes the dimensional coefficient.
5. Derive the semi-infinite-slab error-function solution and verify both surface and far-field boundary conditions.
6. Implement one FTCS time step by hand, then check \(\lambda\) before running multiple steps.
7. Compare FTCS, BTCS, and Crank–Nicolson in terms of stencil, matrix solve, stability, and temporal accuracy.
8. Practise ghost-node treatment of a Neumann boundary condition.
9. Form the tridiagonal BTCS and Crank–Nicolson matrix systems and identify which terms belong on the right-hand side.
10. Apply mesh and time-step refinement, recording both numerical values and convergence behaviour rather than checking only whether a calculation runs.

## Missing or incomplete

- None.

## Source manifest

- Lecture 29 (echo-lecture-29-29): complete; summary `f47f9c1941041437ff0d97942a1bc6b7a813a75cea8ea80f54fefe91af223e58`; transcript `351e3e2b13d0a5144a03cdceef92d843a87087c65f80924684c3550716a3c6b6`; summary path `[local source path redacted]`
- Lecture 30 (echo-lecture-30-30): complete; summary `036dd4148c5dcc36faefa7b9d3211918f2f54606feb39408bf43e9209d2be713`; transcript `800516da1dc94c6cc79946973cd310eeaf770c39e92152e868b83315f20ebc3b`; summary path `[local source path redacted]`
- Lecture 31 (echo-lecture-31-31): complete; summary `15f6cbf4dbbcfe29cd1eb83c22e1580ab496871ad28d5191c0f0f627f0fef0ae`; transcript `cbb9666ec4fa3fdf34469dfd1d671869996c05a35a090035a92cff953b059ba8`; summary path `[local source path redacted]`
- Lecture 32 (echo-lecture-32-32): complete; summary `db6b9951eca78f2196f02114803566364aa2f994d870526f22906d075719cd16`; transcript `0247fde48cc996c2f7898dd6d809c11b84352ccbf10de1ee20ee2a523eaa9960`; summary path `[local source path redacted]`
