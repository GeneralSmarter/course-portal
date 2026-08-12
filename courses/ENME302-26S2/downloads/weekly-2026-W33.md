<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-12T11:59:45.785564+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Week: 2026-W33
- Time window: 2026-08-10T00:00:00+12:00 to 2026-08-12T11:58:40.039233+12:00
- Sources covered:
  - Lecture 17: PDEs, numerical simulation, modelling assumptions, verification, and validation.
  - Lecture 18: finite element analysis, structural modelling, shape functions, and statically indeterminate structures.
- No lectures were identified as missing or incomplete.

## Main concepts

- Numerical models must not be treated as black boxes. Governing physics, assumptions, discretisation, convergence, and validation all affect whether results are credible.
- A numerical-modelling workflow includes identifying dominant physics, simplifying geometry, selecting governing equations and conditions, discretising, solving, checking convergence, verifying against benchmarks, and validating against physical measurements.
- Verification checks whether the equations and numerical implementation have been solved correctly.
- Validation checks whether the model represents the real physical system adequately.
- PDE applications discussed included fluid mechanics, moving boundaries, fluid-solid coupling, heat transfer, lava flows, tsunami propagation, and biomedical mechanics.
- Reynolds number influences flow attachment, separation, wake formation, and vortex structures.
- Moving-boundary problems require the evolving interface and its interaction with the surrounding physics to be modelled.
- Lava-flow modelling can use reduced shallow or height-profile models when the flow geometry supports that simplification.
- Forward problems predict behaviour from known parameters; inverse problems adjust unknown parameters to match observations.
- Shallow-water or Saint-Venant models reduce the computational cost of tsunami simulations by assuming the vertical scale is small relative to the horizontal wave scale.
- Adaptive mesh refinement concentrates computational resolution where the solution changes rapidly or requires greater detail.
- FEA represents a complex continuous structure using simpler connected elements and discrete nodes.
- Statically determinate structures can be solved using equilibrium equations alone.
- Statically indeterminate structures require stiffness, deformation compatibility, and constitutive relationships in addition to equilibrium.
- Relative stiffness determines how load is distributed between members in an overconstrained structure.
- Ideal pin-connected truss elements carry axial tension or compression, but not shear force or bending moment.
- Rigidly connected beam or frame elements can carry axial force, shear force, and bending moment.
- Shape functions interpolate displacement, strain, or other field quantities between nodal points.
- The planned FEA progression begins with axial truss elements and then introduces flexural beam elements.
- Boundary conditions, loads, degrees of freedom, material properties, geometry, and element connectivity must be defined when constructing an FEA model.

## Equations and worked patterns

- Reynolds number was given for the clay-cylinder crossflow example as:
  
  \[
  Re \approx 30{,}000
  \]
  
  The exact definition and variable notation were not stated in the source.

- Lava thickness was represented as a dependent field:
  
  \[
  H=H(x,t)
  \]
  
  The full governing PDE was not reproduced in the source.

- For an axial member, normal stress is:
  
  \[
  \sigma=\frac{N}{A}
  \]
  
  where \(N\) is axial force and \(A\) is cross-sectional area.

- For a tip-loaded cantilever of length \(L\), with \(x\) measured from the fixed end:
  
  \[
  M(x)=-P(L-x)=-PL+Px
  \]
  
  Therefore:
  - \(M(0)=-PL\) at the fixed end.
  - \(M(L)=0\) at the free end.
  - The moment diagram is linear.

- For the same cantilever, the standard magnitudes are:
  
  \[
  \delta_{\text{tip}}=\frac{PL^3}{3EI}
  \]
  
  \[
  \theta_{\text{tip}}=\frac{PL^2}{2EI}
  \]
  
  where \(E\) is Young’s modulus and \(I\) is the second moment of area. The source does not fully specify the final sign convention.

- Worked FEA pattern:
  1. Select the element type.
  2. Divide the structure into elements.
  3. Identify nodes and connectivity.
  4. Define nodal degrees of freedom.
  5. Specify material and geometric properties.
  6. Apply boundary conditions and loads.
  7. Formulate element equations.
  8. Assemble the global system.
  9. Solve for unknown nodal quantities.
  10. Use shape functions to estimate behaviour between nodes.
  11. Interpret displacements, strains, stresses, and reactions.

- The exact moving-interface, lava-viscosity, shallow-water, Navier–Stokes, and continuity equations were not sufficiently reproduced in the source files and should not be reconstructed from them.

## Warnings and deadlines

- Lecture 18 states that a computer-based test was scheduled for Tuesday, 18 August, during the evening.
- The assessment schedule was described as provisional until the end of week 2. Confirm the current date, scope, requirements, and permitted materials using the official ENME302 course information.
- Lecture 18 states that students must achieve at least 40% in the final exam to pass the course overall. Confirm that this requirement remains current.
- The computer laboratories are intended to develop Python and matrix-operation code that can be used during the computer-based test.
- Lecture 17 cautions that numerical results require benchmark testing, convergence checks, and validation against trusted physical data.
- Several equations in Lecture 17 were not legible in the source summary. Do not rely on unstated forms for the moving-interface, lava-flow, viscosity, or shallow-water models.

## Recall questions

1. What is the difference between verification and validation in numerical modelling?
2. Why can a model be numerically verified but still physically inaccurate?
3. Why does a clay cylinder in crossflow experience non-uniform erosion?
4. What makes the clay-cylinder example a fluid-solid coupling problem?
5. What assumptions support the use of a shallow-water tsunami model?
6. Why is adaptive mesh refinement useful in large tsunami simulations?
7. What additional information is required to solve a statically indeterminate structure?
8. Why do ideal pin-connected truss elements carry axial force but not bending moment or shear force?
9. What role do shape functions play in finite element analysis?
10. For the tip-loaded cantilever, what are the bending moments at the fixed and free ends?

## Practice priorities

- Be able to distinguish governing-physics selection, discretisation, solving, verification, and validation in a complete numerical-modelling workflow.
- Practise explaining when a reduced model is justified and what physical detail may be lost through simplification.
- Review Reynolds-number effects on separation and wake formation without relying on an unstated formula.
- Practise identifying dependent and independent variables in moving-boundary, lava-flow, and shallow-water models.
- Review the differences between statically determinate and indeterminate structures, especially the roles of stiffness and compatibility.
- Practise classifying truss and beam elements by their supported loads, moments, rotations, and degrees of freedom.
- Work through the cantilever moment equation and apply the tip-deflection and tip-rotation expressions.
- Practise assembling an FEA model from element selection through global-system solution and interpretation.
- Review boundary-condition types and identify which translations and rotations they constrain.
- Prepare Python and matrix-manipulation skills for the computer laboratories and the stated computer-based test.

## Missing or incomplete

None.

## Source manifest

- Lecture 17 (echo-lecture-17-17): complete; summary `df2f7c87000f0e58f9efdb94f4ba26ae9d4da0617d1af3951756cc39277be865`; transcript `fc4ba008504f88530bbe5a13e36b3f93f4f3c622b028373b8d999225ee510f3d`; summary path `[local source path redacted]`
- Lecture 18 (echo-lecture-18-18): complete; summary `6d09a93051a8bf1a9c0a25fc15153a15f4919187929873d8f55f52a1bfb27e97`; transcript `e1fc4a0c062cf1d87702bf45fabe280fb795cda48cb2a6542c1d1af71031651f`; summary path `[local source path redacted]`
