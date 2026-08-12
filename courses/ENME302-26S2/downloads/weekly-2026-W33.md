<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-13T10:10:08.342188+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Study window: 2026-W33, from 2026-08-10T00:00:00+12:00 to 2026-08-13T10:09:15.026453+12:00.
- Covered source files:
  - `lecture_17_summary.md`
  - `lecture_18_summary.md`
- Lecture 17 introduced PDE-based modelling, numerical simulation, modelling assumptions, and verification versus validation.
- Lecture 18 introduced finite element analysis, statically determinate and indeterminate structures, one-dimensional elements, shape functions, and the planned progression from axial trusses to flexural beams.

## Main concepts

- Numerical models must not be treated as black boxes. Their governing physics, assumptions, discretisation, boundary conditions, mesh, convergence, and physical validity must be assessed.
- A numerical-modelling workflow progresses from the real engineering problem through physical simplification, mathematical formulation, discretisation, solution, verification, visualisation, and validation.
- Verification checks whether the equations were implemented and solved correctly. Validation checks whether the model represents the real physical system adequately.
- Partial differential equations were classified as elliptic, parabolic, or hyperbolic. Appropriate boundary conditions are required for a unique solution, with initial conditions additionally required for time-dependent problems.
- Moving-boundary problems involve domains whose boundaries change with time. Examples included clay erosion and ice melting.
- Fluid-solid coupling occurs when the fluid affects the solid boundary and the changing boundary subsequently alters the fluid domain.
- Shallow-water modelling reduces the computational cost of tsunami simulation by assuming that the vertical water-depth scale is small relative to the horizontal wave-length scale.
- Adaptive mesh refinement locally increases resolution where gradients, velocities, or estimated errors indicate that additional detail is needed.
- Finite element analysis represents a complex continuous structure using a finite collection of simpler elements connected at nodes.
- Shape functions interpolate displacement, strain, or other field quantities between nodal values.
- Statically determinate structures can be solved using equilibrium equations alone. Statically indeterminate structures additionally require stiffness and compatibility information.
- Relative stiffness affects how load is distributed between members in an overconstrained structure.
- Ideal pin-jointed truss elements carry axial tension or compression, but not shear force or bending moment.
- Rigidly connected beam or frame elements can carry axial force, shear force, and bending moment, with compatible translations and rotations at connections.
- One-dimensional structural elements are computationally efficient and can be arranged to model two-dimensional or three-dimensional structures.

## Equations and worked patterns

- Reynolds number was used qualitatively to relate flow behaviour to attachment, separation, wake formation, and vortical structures. The clay-cylinder example used:
  
  \(Re \approx 30{,}000\)

- Lava thickness was represented as a dependent field:
  
  \(H=H(x,t)\)

  The full governing PDE was not provided clearly enough to reproduce.
- For an axial member, normal stress is:
  
  \(\sigma=\frac{N}{A}\)

  where \(N\) is axial force and \(A\) is cross-sectional area.
- For a tip-loaded cantilever of length \(L\), with a point load \(P\) at the free tip and \(x\) measured from the fixed end:
  
  \(M(x)=-P(L-x)=-PL+Px\)

  Therefore:
  - \(M(0)=-PL\)
  - \(M(L)=0\)
- For constant flexural rigidity \(EI\), the standard magnitudes for the same cantilever are:
  
  \(\delta_{\text{tip}}=\frac{PL^3}{3EI}\)

  \(\theta_{\text{tip}}=\frac{PL^2}{2EI}\)

- \(E\) is Young’s modulus, \(I\) is the second moment of area, and \(EI\) is flexural rigidity.
- FEA pattern:
  1. Select the element type.
  2. Define nodes and connectivity.
  3. Define nodal degrees of freedom.
  4. Specify material and geometric properties.
  5. Apply boundary conditions and loads.
  6. Form element equations.
  7. Assemble the global system.
  8. Solve for nodal quantities.
  9. Use shape functions to estimate behaviour between nodes.
  10. Interpret displacements, strains, stresses, and reactions.
- Exact full forms of the Navier–Stokes, continuity, shallow-water, lava-flow, and moving-interface equations were not reliably available in the source summaries and should not be reconstructed from these notes.

## Warnings and deadlines

- Lecture 18 states that a computer-based test was scheduled for Tuesday, 18 August, during the evening. The assessment schedule was described as provisional and must be checked against current official ENME302 course information.
- The lecture states that students must achieve at least 40% in the final exam to pass the course overall. Confirm this requirement against the official course information.
- Computer laboratories develop Python and matrix-operation skills intended for use in the computer-based test. The first laboratory includes matrix entry, multiplication, manipulation, and plotting.
- Do not rely on the lecture summaries for exact assessment scope, permitted materials, current dates, or updated requirements.
- Several equations in Lecture 17 were described but not captured in full. Do not infer the missing lava-viscosity, moving-interface, Navier–Stokes, continuity, or shallow-water equations from these summaries alone.
- The numerical values given for research examples, such as damping forces and shake-table equipment, are lecture statements rather than independently verified specifications.

## Recall questions

1. What is the difference between verification and validation of a numerical model?
2. Why are both boundary conditions and, for an unsteady problem, an initial condition required?
3. Why is the clay-cylinder erosion example a fluid-solid coupling and moving-boundary problem?
4. What physical assumption makes the shallow-water approximation computationally cheaper than solving the full Navier–Stokes equations?
5. What is adaptive mesh refinement, and why is it useful in tsunami simulations?
6. Why are equilibrium equations alone insufficient for a statically indeterminate structure?
7. What role do nodes and shape functions play in finite element analysis?
8. What forces and moments can an ideal pin-jointed truss element carry?
9. For the tip-loaded cantilever, what are the bending moments at the fixed end and free end?
10. How do relative stiffness and deformation compatibility affect load sharing in an overconstrained structure?

## Practice priorities

- Explain the numerical-modelling workflow from the physical problem to verification and validation.
- Practise distinguishing model verification errors from model-validation errors.
- Review PDE classifications, boundary conditions, initial conditions, shallow-water assumptions, and adaptive mesh refinement.
- Re-derive the cantilever bending-moment relation and check its endpoint values.
- Memorise and apply the cantilever tip-deflection and tip-rotation patterns, including the meaning of \(EI\).
- Practise identifying whether a structural problem is statically determinate or indeterminate and state what additional information is needed.
- Draw the modelling workflow for a finite element structure: elements, nodes, degrees of freedom, supports, loads, assembly, solution, and interpolation.
- Review the idealisations and limitations of axial truss elements versus flexural beam elements.
- Use Python to practise matrix entry, matrix multiplication, matrix manipulation, and plotting in preparation for the computer-based test, subject to confirmation of current assessment requirements.
- Consult the official course material before studying any equation whose full form was not captured in the summaries.

## Missing or incomplete

- Lecture 19: `missing_summary`.
- The source coverage does not support conclusions about Lecture 19 content, equations, examples, warnings, or deadlines.

## Source manifest

- Lecture 17 (echo-lecture-17-17): complete; summary `df2f7c87000f0e58f9efdb94f4ba26ae9d4da0617d1af3951756cc39277be865`; transcript `fc4ba008504f88530bbe5a13e36b3f93f4f3c622b028373b8d999225ee510f3d`; summary path `[local source path redacted]`
- Lecture 18 (echo-lecture-18-18): complete; summary `6d09a93051a8bf1a9c0a25fc15153a15f4919187929873d8f55f52a1bfb27e97`; transcript `e1fc4a0c062cf1d87702bf45fabe280fb795cda48cb2a6542c1d1af71031651f`; summary path `[local source path redacted]`
- Lecture 19 (echo-lecture-19-19): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
