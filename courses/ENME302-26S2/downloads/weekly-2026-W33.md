<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-23T09:44:35.960825+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Covered verified summaries for Lectures 17–20 during 2026-W33.
- Lecture 17: numerical modelling, PDE applications, discretisation, verification, and validation.
- Lecture 18: finite element analysis, structural modelling, shape functions, trusses, beams, and statical determinacy.
- Lecture 19: classification of second-order PDEs, boundary and initial conditions, homogeneous equations, and superposition.
- Lecture 20: derivation of the steady two-dimensional heat equation, boundary conditions, and separation of variables.
- No lecture files were identified as missing or incomplete.

## Main concepts

- Numerical software must not be treated as a black box. Model credibility depends on the governing physics, assumptions, geometry, boundary and initial conditions, mesh, convergence, verification, and validation. (Lecture 17)
- Numerical modelling follows a progression from the real engineering problem through physical simplification, mathematical formulation, discretisation, solution, convergence checks, verification, post-processing, and validation. (Lecture 17)
- Verification checks whether the equations and numerical implementation have been solved correctly. Validation checks whether the model represents the real physical system adequately. (Lecture 17)
- Moving-boundary and fluid–solid coupling problems require the evolving interface to affect, and be affected by, the surrounding field solution. Examples included clay-cylinder erosion and melting ice. (Lecture 17)
- Reduced models, such as shallow-water models for tsunami propagation, can reduce computational cost when their assumptions are justified. Adaptive mesh refinement concentrates resolution where the solution changes rapidly or requires greater detail. (Lecture 17)
- Finite element analysis represents a continuous structure using a finite collection of simpler elements connected at nodes. Shape functions approximate field quantities between nodal values. (Lecture 18)
- Statically determinate structures can be solved using equilibrium equations alone. Statically indeterminate structures also require stiffness, deformation compatibility, and constitutive relationships. (Lecture 18)
- Ideal pin-connected truss elements carry axial tension or compression, but not shear force or bending moment. Rigidly connected beam or frame elements can also carry bending and shear. (Lecture 18)
- PDE classification uses the discriminant \(b^2-4ac\):
  - Elliptic: \(b^2-4ac<0\)
  - Parabolic: \(b^2-4ac=0\)
  - Hyperbolic: \(b^2-4ac>0\)
- Elliptic equations generally describe steady spatial fields, parabolic equations describe diffusive time-dependent processes, and hyperbolic equations describe finite-speed wave propagation. (Lecture 19)
- Homogeneous equations have zero source terms. A Laplace-type equation with a nonzero source term is a non-homogeneous Poisson equation. (Lecture 19)
- In steady two-dimensional heat conduction, conservation of energy combined with Fourier’s law produces Laplace’s equation when thermal conductivity is constant and there is no internal heat generation. (Lecture 20)
- Boundary conditions select a particular solution from the many functions that satisfy Laplace’s equation:
  - Dirichlet: prescribed temperature.
  - Neumann: prescribed temperature gradient or heat flux.
  - Robin: a combination of temperature and heat flux. (Lecture 20)
- Separation of variables assumes a product solution and converts Laplace’s PDE into two ordinary differential equations. The admissible separated solution depends on the sign of the separation constant and the boundary conditions. (Lecture 20)

## Equations and worked patterns

- Reynolds number in the clay-cylinder crossflow example:
  \[
  Re\approx 30{,}000
  \]
  The lecture connected Reynolds number with flow separation, wake formation, and vortex structures. The full definition was not reproduced in the summary. (Lecture 17)

- Axial normal stress:
  \[
  \sigma=\frac{N}{A}
  \]
  where \(N\) is axial member force and \(A\) is cross-sectional area. (Lecture 18)

- Tip-loaded cantilever bending moment, with \(x\) measured from the fixed end:
  \[
  M(x)=-P(L-x)=-PL+Px
  \]
  Therefore:
  \[
  M(0)=-PL,\qquad M(L)=0
  \]
  The moment diagram is linear. (Lecture 18)

- Tip-loaded cantilever magnitudes:
  \[
  \delta_{\mathrm{tip}}=\frac{PL^3}{3EI},
  \qquad
  \theta_{\mathrm{tip}}=\frac{PL^2}{2EI}
  \]
  Sign conventions depend on the selected coordinate and deflection directions. (Lecture 18)

- PDE classification:
  \[
  \Delta=b^2-4ac
  \]
  Apply the sign test to the coefficients of the principal part:
  \[
  au_{xx}+bu_{xy}+cu_{yy}
  \]

- Standard PDE examples:
  \[
  T_{xx}+T_{yy}=0
  \]
  is elliptic because \(\Delta=-4<0\).

  \[
  T_t=\kappa T_{xx}
  \]
  is parabolic because, after rearrangement, \(a=\kappa\), \(b=0\), and \(c=0\), giving \(\Delta=0\).

  \[
  u_{xx}-\frac{1}{c^2}u_{tt}=0
  \]
  is hyperbolic because:
  \[
  \Delta=\frac{4}{c^2}>0
  \]

- Fourier’s law:
  \[
  \mathbf q=-k\nabla T
  \]
  with components:
  \[
  q_x=-k\frac{\partial T}{\partial x},
  \qquad
  q_y=-k\frac{\partial T}{\partial y}
  \]
  The negative sign indicates heat flows down the temperature gradient. (Lecture 20)

- Steady conservation of energy:
  \[
  \frac{\partial q_x}{\partial x}
  +
  \frac{\partial q_y}{\partial y}=0
  \]

- General steady heat equation:
  \[
  \frac{\partial}{\partial x}
  \left(k\frac{\partial T}{\partial x}\right)
  +
  \frac{\partial}{\partial y}
  \left(k\frac{\partial T}{\partial y}\right)=0
  \]

  For constant \(k\):
  \[
  \frac{\partial^2T}{\partial x^2}
  +
  \frac{\partial^2T}{\partial y^2}=0
  \]

- Separation of variables for Laplace’s equation:
  \[
  u(x,y)=X(x)Y(y)
  \]
  Substitution gives:
  \[
  \frac{1}{X}\frac{d^2X}{dx^2}
  =
  -\frac{1}{Y}\frac{d^2Y}{dy^2}
  =\lambda
  \]
  Hence:
  \[
  \frac{d^2X}{dx^2}=\lambda X,
  \qquad
  \frac{d^2Y}{dy^2}=-\lambda Y
  \]

- For the rectangular-domain example, applying the boundary conditions rejected the \(\lambda=0\) and one nontrivial separated family. The remaining family produced the condition:
  \[
  \sin(\mu)=0
  \]
  and therefore:
  \[
  \mu=n\pi,\qquad n\in\mathbb Z
  \]
  The final coefficients and complete right-edge solution were not reached in Lecture 20.

## Warnings and deadlines

- The Lecture 18 summary records a computer-based test scheduled for Tuesday, 18 August, during the evening. The assessment schedule was described as provisional, so confirm the current official course information.
- The same summary states that students may bring code developed during the computer laboratories into the test. The laboratories cover Python matrix entry, multiplication, manipulation, and plotting.
- The summary records a requirement to achieve at least 40% in the final exam to pass the course overall. Confirm the current official assessment rules.
- Lecture 19 states that AI may assist with explaining or debugging code, but generated code and results must be checked. The summary states that AI should not be used to complete the quizzes themselves.
- Do not reproduce the incomplete final constants from the rectangular-domain example. Lecture 20 ends before the remaining boundary condition and coefficients are fully applied.
- Exact equations for the moving ice interface, lava viscosity, shallow-water tsunami model, and wave-speed relation were not captured clearly in the verified summaries. Do not rely on reconstructed forms without checking the course material.

## Recall questions

1. What is the difference between verification and validation of a numerical model?
2. Why can a statically indeterminate structure not be solved using equilibrium equations alone?
3. What quantities do shape functions interpolate within a finite element?
4. For \(au_{xx}+bu_{xy}+cu_{yy}\), how does the sign of \(b^2-4ac\) determine the PDE classification?
5. Why is the heat equation parabolic, while Laplace’s equation is elliptic?
6. What is the physical meaning of the negative sign in Fourier’s law?
7. Distinguish Dirichlet, Neumann, and Robin boundary conditions for a heat-conduction problem.
8. Why are boundary conditions required when solving Laplace’s equation?
9. What product-form assumption is used in separation of variables, and what two ODEs result?
10. Why are analytical solutions useful even when realistic engineering geometries generally require numerical methods?

## Practice priorities

1. Practise classifying PDEs from their second-order coefficients using \(b^2-4ac\), including the Laplace, heat, and wave equations.
2. Derive the steady two-dimensional heat equation from conservation of energy and Fourier’s law.
3. Identify whether a thermal boundary condition is Dirichlet, Neumann, or Robin, and translate between heat-flux and temperature-gradient forms.
4. Work through separation of variables for Laplace’s equation, including the \(\lambda=0\), \(\lambda<0\), and \(\lambda>0\) cases.
5. Continue the rectangular-domain example from Lecture 20 using the remaining boundary condition, without assuming constants or expressions not provided in the source.
6. Review the finite element workflow: element selection, nodes, connectivity, degrees of freedom, properties, boundary conditions, loading, assembly, solution, and interpolation.
7. Rework the cantilever patterns for \(M(x)\), tip deflection, and tip rotation, carefully tracking sign conventions and flexural rigidity \(EI\).
8. Practise explaining why a numerical result can be mathematically verified yet physically invalid.
9. Review the assumptions behind reduced models, particularly shallow-water tsunami modelling and adaptive mesh refinement.
10. Prepare the Python matrix and plotting skills identified as relevant to the upcoming computer-based test, subject to confirmation of the current assessment information.

## Missing or incomplete

- No lecture files are missing from the requested coverage.
- Lecture 20 ends partway through the rectangular-domain separation-of-variables example; its final constants and complete solution are deferred to the following lecture.
- The verified summaries explicitly mark several detailed equations as unavailable or unclear, including the moving-interface relation for melting ice, the lava viscosity relation, the shallow-water equations, and the wave-speed relation involving material properties.

## Source manifest

- Lecture 17 (echo-lecture-17-17): complete; summary `df2f7c87000f0e58f9efdb94f4ba26ae9d4da0617d1af3951756cc39277be865`; transcript `fc4ba008504f88530bbe5a13e36b3f93f4f3c622b028373b8d999225ee510f3d`; summary path `[local source path redacted]`
- Lecture 18 (echo-lecture-18-18): complete; summary `6d09a93051a8bf1a9c0a25fc15153a15f4919187929873d8f55f52a1bfb27e97`; transcript `e1fc4a0c062cf1d87702bf45fabe280fb795cda48cb2a6542c1d1af71031651f`; summary path `[local source path redacted]`
- Lecture 19 (echo-lecture-19-19): complete; summary `b75b9d8a07b0ddc0789bba31659608dd57dfca6f4c3a01348a7d68b2279e4a6a`; transcript `211bea4a8e6c20782c17081483b60239faecac9d7b9158533d8d9178d165cedb`; summary path `[local source path redacted]`
- Lecture 20 (echo-lecture-20-20): complete; summary `9d7a9599da73ee0da57fda0a7c9ba62eb2885e167964e71fa6f9f4d709e09562`; transcript `ce5240c7cc9f1d3ca3ada583444382cab0b9cccbf6e68707fa62ee83fee697c4`; summary path `[local source path redacted]`
