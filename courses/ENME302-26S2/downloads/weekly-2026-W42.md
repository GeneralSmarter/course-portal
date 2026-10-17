<!-- week-id: 2026-W42 -->
<!-- generated-at: 2026-10-18T08:36:59.265674+13:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Week 42 covers Lectures 45–48, from 2026-10-12 to 2026-10-18.
- Lecture 45: examination revision, finite differences, the Laplace equation, Liebmann iteration, over-relaxation, grid indexing, and numerical-error interpretation.
- Lecture 46: boundary element methods, Green’s functions, CFD limitations, potential flow, cavitation, and flow control.
- Lecture 47: non-dimensionalisation, the Reynolds number, numerical-model limitations, optimisation, and a one-dimensional finite-element heat-conduction setup.
- Lecture 48: examination preparation, finite-element assembly, transient heat and wave equations, stability and convergence, boundary conditions, and course-wide revision.
- No lectures were identified as missing or incomplete.

## Main concepts

- Numerical PDE methods convert continuous governing equations into algebraic systems. Finite differences use neighbouring grid values, finite elements use element shape functions, and BEM discretises the boundary rather than the domain interior.
- The two-dimensional steady temperature problem in Lecture 45 uses the Laplace equation with prescribed boundary temperatures. Interior nodes are unknowns; Dirichlet boundary nodes remain fixed.
- For non-square finite-difference grids, the x- and y-spacing terms must remain distinct.
- Iterative finite-difference solvers require correct interior-node loops, correct array indexing, independent copies of previous iterates, and correctly weighted relaxation updates.
- BEM is especially applicable to selected elliptic PDEs, including Laplace-type potential-flow and Stokes-flow problems. Its lower-dimensional boundary discretisation can be computationally efficient, but it cannot represent arbitrary physics.
- Green’s functions, the Dirac delta function, Green’s second identity, and the divergence theorem provide the conceptual basis for converting a domain problem into a boundary representation.
- CFD output must be checked against the geometry, mesh, boundary conditions, physical assumptions, and solver settings. A converged or visually attractive result is not automatically physically valid.
- For incompressible, inviscid, irrotational flow, velocity can be represented using a potential satisfying Laplace’s equation.
- Non-dimensionalisation reduces the number of independent parameters and enables comparison across scales. The Reynolds number represents the ratio of inertial to viscous effects.
- Finite-element assembly maps local element contributions into global rows and columns. Shared nodes create shared degrees of freedom, so adjacent contributions must be added.
- A positive internal heat source raises the interior temperature above the source-free linear interpolation between boundary temperatures.
- Consistency concerns truncation error tending to zero, stability concerns bounded numerical errors, and the course notes state that convergence requires both consistency and stability.
- Explicit and implicit heat-equation schemes were described as first-order accurate in time and second-order accurate in space. The explicit scheme is conditionally stable; the implicit scheme is unconditionally stable. Crank–Nicolson combines contributions from adjacent time levels.

## Equations and worked patterns

- Two-dimensional Laplace equation:
  
  \[
  \frac{\partial^2 T}{\partial x^2}
  +
  \frac{\partial^2 T}{\partial y^2}
  =0
  \]

- Second-order central finite differences:
  
  \[
  \frac{\partial^2 T}{\partial x^2}
  \approx
  \frac{T_{i+1,j}-2T_{i,j}+T_{i-1,j}}{\Delta x^2}
  \]
  
  \[
  \frac{\partial^2 T}{\partial y^2}
  \approx
  \frac{T_{i,j+1}-2T_{i,j}+T_{i,j-1}}{\Delta y^2}
  \]

- Rearranged finite-difference update for an interior node:
  
  \[
  T_{i,j}
  =
  \frac{
  \Delta y^2(T_{i+1,j}+T_{i-1,j})
  +
  \Delta x^2(T_{i,j+1}+T_{i,j-1})
  }{
  2(\Delta y^2+\Delta x^2)
  }
  \]

- For a domain of x-length 2 and y-length 1:
  
  \[
  \Delta x=\frac{2}{N_x-1},
  \qquad
  \Delta y=\frac{1}{N_y-1}
  \]
  
  The subtraction by one is required because grid-point counts define interval counts.

- Over-relaxation update:
  
  \[
  T_{i,j}^{\mathrm{new}}
  =
  (1-\lambda)T_{i,j}^{\mathrm{old}}
  +
  \lambda T_{i,j}^{*}
  \]
  
  The old and newly calculated values must not receive swapped coefficients.

- PDE classification uses:
  
  \[
  B^2-4AC
  \]
  
  to distinguish elliptic, parabolic, and hyperbolic forms. The exact classification convention should be checked against the course formula sheet if required.

- Green’s-function relation under the lecture’s stated convention:
  
  \[
  \nabla^2G(\mathbf{x},\mathbf{x}_0)
  +
  \delta(\mathbf{x}-\mathbf{x}_0)
  =0
  \]

- Boundary representation for a harmonic field:
  
  \[
  F(\mathbf{x}_0)
  =
  \int_{\Gamma}
  \left[
  G\frac{\partial F}{\partial n}
  -
  F\frac{\partial G}{\partial n}
  \right]\,d\Gamma
  \]
  
  The sign and additional factors depend on the normal-direction and BEM conventions.

- BEM discretisation follows the pattern: divide the boundary into elements, define control points, impose boundary conditions, assemble influence coefficients into
  
  \[
  \mathbf{A}\mathbf{x}=\mathbf{b},
  \]
  
  solve for source or dipole strengths, then evaluate interior or exterior field values.

- Potential-flow reduction:
  
  \[
  \mathbf{u}=\nabla\Phi,
  \qquad
  \nabla\cdot\mathbf{u}=0
  \quad\Longrightarrow\quad
  \nabla^2\Phi=0
  \]

- Reynolds number:
  
  \[
  \mathrm{Re}=\frac{\rho V_0D}{\mu}
  \]

- Linear finite-element interpolation:
  
  \[
  \tilde{T}(x)=T_1N_1(x)+T_2N_2(x)
  \]
  
  with
  
  \[
  N_1(x)=\frac{x_2-x}{x_2-x_1},
  \qquad
  N_2(x)=\frac{x-x_1}{x_2-x_1}.
  \]

- The corresponding constant element gradient is:
  
  \[
  \frac{d\tilde{T}}{dx}
  =
  \frac{T_2-T_1}{x_2-x_1}
  \]

- For the two-element rod example, the boundary temperatures were \(T_1=10\) and \(T_3=20\). With no source:
  
  \[
  \frac{d^2T}{dx^2}=0,
  \qquad
  T(1/2)=\frac{10+20}{2}=15.
  \]
  
  With the positive source used in the worked example, the shared-node temperature was reported as:
  
  \[
  T_2=\frac{135}{4}=33.75.
  \]

- Transient heat equation:
  
  \[
  \frac{\partial T}{\partial t}
  =
  \alpha\frac{\partial^2T}{\partial x^2}
  \]

- Consistency requires the truncation error to satisfy:
  
  \[
  \tau(\Delta x,\Delta t)\to0
  \quad\text{as}\quad
  \Delta x,\Delta t\to0.
  \]

## Warnings and deadlines

- The final examination was described as closed-book, three hours, and worth 50 marks. The stated examination pass barrier was 40%, equivalent to 20/50.
- No calculator, computer, electronic device, communication device, or student-prepared cheat sheet was permitted. A formula sheet was to be provided.
- Students were advised to attempt every question, show working, use supplied hints and equations, and check both sides of the examination paper.
- Lecture 48 described Friday 30 October as a draft or provisional examination date. Confirm the official timetable before relying on it.
- Study-help sessions were discussed for the Thursday and Friday afternoons before the examination, but exact times were not confirmed.
- A 20% per day late-submission penalty was reported as the department default. Confirm the official course policy if submitting late.
- Assignment submissions were described as a PDF report plus a ZIP containing code, discretisation files, and model files. Nested ZIP archives were discouraged.
- Remove unnecessary generated solution data before submission where it is not required. Large meshes and frequent time-step output can create very large archives.
- Do not trust CFD or numerical results solely because the solver converged or produced an attractive plot. Check the physical model, boundary conditions, mesh, and governing assumptions.
- The finite-element source-term sign convention and the exact assembled matrix should be checked against the course reader before using the worked example as a numerical template.
- The BEM boundary-integral signs depend on the chosen Green’s-function and normal-direction conventions.

## Recall questions

1. Why is the two-dimensional Laplace equation linear and homogeneous?
2. Why must \(\Delta x\) and \(\Delta y\) be retained separately on a non-square grid?
3. Which nodes are updated in an interior finite-difference iteration, and why must boundary nodes be excluded?
4. What is the difference between assigning an array reference and making an independent copy of the previous iteration?
5. What is the purpose of the old-value and newly calculated-value coefficients in the over-relaxation update?
6. Why can a BEM solution avoid meshing the domain interior?
7. What do the Dirac delta function and Green’s function contribute to the BEM formulation?
8. Under what flow assumptions does the velocity potential satisfy Laplace’s equation?
9. Why is the Reynolds number dimensionless, and what physical effects does it compare?
10. How are local finite-element matrices assembled into a global system at a shared node?
11. What is the source-free midpoint temperature for endpoint temperatures of 10 and 20, and why can a positive source raise it above this value?
12. What are the differences between consistency, stability, and convergence?

## Practice priorities

1. Re-derive the non-square-grid finite-difference stencil and practise applying it without incorrectly setting \(\Delta x=\Delta y\).
2. Trace a Liebmann or over-relaxed iteration by hand, including correct interior indices, boundary preservation, and independent old/new arrays.
3. Practise classifying PDEs using \(B^2-4AC\), while checking the exact sign convention on the provided formula sheet.
4. Write the BEM workflow from boundary discretisation through assembly of \(\mathbf{A}\mathbf{x}=\mathbf{b}\) and post-solution field evaluation.
5. Explain why a CFD result may be numerically converged but physically invalid.
6. Derive the Reynolds number by non-dimensionalising the governing flow equation and verify its units.
7. Complete the two-element finite-element rod assembly, apply \(T_1=10\) and \(T_3=20\), and verify the reported midpoint value \(T_2=33.75\) against the course sign convention.
8. Practise linear shape functions, their derivatives, the weighted residual equation, integration by parts, and source-term integrals.
9. Review explicit, implicit, and Crank–Nicolson heat-equation schemes, including accuracy and stability properties.
10. Practise consistency and von Neumann stability arguments using the supplied formulae and chapter exercises before attempting past examinations.
11. Review separation of variables, Fourier-series boundary-condition treatment, the wave equation, and initial displacement versus initial velocity conditions.
12. Revise optimisation methods by comparing grid search, Monte Carlo sampling, and gradient or steepest-descent methods.

## Missing or incomplete

- None of the specified lectures were identified as missing or incomplete.
- Some source summaries contain transcript uncertainty: exact BEM sign conventions, finite-element matrix entries, certain method names, the provisional examination date, and some assignment-policy details should be verified against official course materials before being used as authoritative.

## Source manifest

- Lecture 45 (echo-lecture-45-45): complete; summary `d1faade27007852480d1d37ab0eb2de0804449cdb055ad474e2cc104885c68e5`; transcript `b178253961ff591645772a235c3a1dae416cede2ffc6f6d66230f528bccaca7c`; summary path `[local source path redacted]`
- Lecture 46 (echo-lecture-46-46): complete; summary `465481bcbe67217e86319b79cb354804a4c07d8aa4d1a80d2ed2aff994c34971`; transcript `e33ad03a9d659519346c8deebd52e8f0c88013fd64c9e96ad82e150f2a112dcf`; summary path `[local source path redacted]`
- Lecture 47 (echo-lecture-47-47): complete; summary `10872cde453825c3b78a43af97dda4314324da6f1afc4ade254d37a827ec31f7`; transcript `9aa33d41b16848f23ff1ced367a13dfa95966f3dcb44b394d729afdf3d8a7c5d`; summary path `[local source path redacted]`
- Lecture 48 (echo-lecture-48-48): complete; summary `4bbb37c73a074e3e665f42363a2840c3506377131f72244f8123472c668f3873`; transcript `a34f65a9cbcb6a037a867f0908e03c1bccfe2c77fe251c1c5346bcf13f63bf62`; summary path `[local source path redacted]`
