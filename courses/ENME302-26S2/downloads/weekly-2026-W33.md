<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-11T11:13:05.822158+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Week: 2026-W33
- Period: 2026-08-10T00:00:00+12:00 to 2026-08-11T11:11:57.677012+12:00
- Source covered: Lecture 17 summary
- Focus: Partial differential equations, numerical simulation, modelling assumptions, verification, validation, and engineering applications.
- No lectures were identified as missing or incomplete for this period.

## Main concepts

- PDEs are used to model systems involving multiple independent variables, such as space and time.
- The remaining course material will cover elliptic, parabolic, and hyperbolic PDEs.
- Numerical simulation requires understanding the governing physics, modelling assumptions, geometry, boundary and initial conditions, discretisation, solution process, and limitations.
- Fluid–solid coupling occurs when the fluid affects a solid boundary and the changing boundary subsequently alters the fluid domain.
- Wall shear stress can cause non-uniform erosion of a body in crossflow.
- Moving-boundary problems involve domains whose boundaries change with time, such as melting ice or eroding clay.
- Lava-flow modelling can use reduced-dimensional models when the lava thickness is small relative to its horizontal extent and the simplifying assumptions are justified.
- Forward problems predict behaviour from known parameters. Inverse problems estimate unknown parameters from observed behaviour.
- Shallow-water or Saint-Venant models approximate tsunami propagation when the vertical water-depth scale is small relative to the horizontal wave length scale.
- Adaptive mesh refinement increases resolution locally where the solution changes rapidly or where error indicators show that more detail is needed.
- Spatial discretisation converts governing PDEs into a discrete numerical problem. The resulting algebraic system must then be solved using numerical algorithms.
- Verification checks whether the equations were implemented and solved correctly.
- Validation checks whether the model represents the real physical system adequately.
- Numerical models can support detailed field prediction, parameter sweeps, and parametric design, but they remain dependent on assumptions and require benchmark testing and validation.
- The general engineering approaches discussed were established standards, simplified analysis, physical experimentation, and numerical simulation.

## Equations and worked patterns

- Lava thickness was represented as:
  
  \[
  H = H(x,t)
  \]
  
  where \(H\) is lava thickness or height, \(x\) is spatial position, and \(t\) is time. The full governing PDE was not captured.

- The clay-cylinder crossflow example used approximately:
  
  \[
  Re \approx 30{,}000
  \]
  
  Reynolds number was linked to flow separation, wake formation, and vortex structures. The exact definition and notation were not stated in the source.

- The lava viscosity relationship was described only generically as:
  
  \[
  \mu = \mu(T;\text{unknown parameters})
  \]
  
  The exact temperature-dependent functional form was not available.

- The tsunami model used nonlinear shallow-water or Saint-Venant equations with unknowns including water height or free-surface elevation and horizontal velocity components \(u\) and \(v\). The full equations were not transcribed.

- Moving-interface pattern:
  1. Determine the temperature field.
  2. Evaluate the temperature gradient normal to the interface.
  3. Relate the interface velocity to that gradient and relevant thermal/material properties.
  4. Update the boundary and solve again on the changing domain.
  
  The exact Stefan-type equation was not captured.

- Numerical-modelling workflow:
  1. Identify the real engineering problem and dominant physics.
  2. Simplify the geometry where justified.
  3. Define the mathematical model.
  4. Select governing equations and boundary or initial conditions.
  5. Discretise the equations.
  6. Solve the resulting algebraic system.
  7. Check convergence and numerical properties.
  8. Verify against benchmarks or known solutions.
  9. Postprocess and visualise.
  10. Validate against measurements or trusted real-system data.
  11. Decide whether the model is adequate for the engineering question.

## Warnings and deadlines

- No specific deadlines were provided in the source summary.
- Do not reproduce the full Navier–Stokes equations, moving-interface equation, lava viscosity equation, or shallow-water equations from this summary: their exact forms were not captured reliably.
- Do not treat numerical software as a black box. Check the governing equations, assumptions, geometry, boundary and initial conditions, mesh resolution, convergence, physical plausibility, and validation evidence.
- A verified implementation may still be physically inaccurate if the model assumptions are unsuitable.
- Agreement with one measurement does not by itself establish that the implementation is correct.
- Course administration, assessment scope, software requirements, and exam coverage mentioned in the lecture summary should be confirmed against current official ENME302 course information.

## Recall questions

1. What distinguishes verification from validation in numerical modelling?
2. Why is the clay-cylinder erosion example a fluid–solid coupling problem?
3. How can Reynolds number influence separation and wake formation around a cylinder?
4. Why is melting ice a moving-boundary problem, and what determines the interface motion?
5. In the lava model, what are \(H\), \(x\), and \(t\)?
6. What makes lava-flow forecasting an inverse problem?
7. What physical assumption permits the use of shallow-water equations for tsunami modelling?
8. Why is adaptive mesh refinement useful in large tsunami simulations?
9. Why are boundary conditions required, and when is an initial condition additionally needed?
10. What is one example of a verification test and one example of a validation test?

## Practice priorities

1. Be able to distinguish forward problems from inverse problems using the lava-flow example.
2. Explain the difference between verification and validation and provide a suitable example of each.
3. Reconstruct the full numerical-modelling workflow from physical problem definition through validation.
4. Explain why model simplification is useful and identify when it may invalidate the result.
5. Review the roles of Reynolds number, wall shear stress, interface velocity, and normal temperature gradient.
6. Understand the shallow-water approximation and why it reduces computational cost relative to full Navier–Stokes modelling.
7. Practise explaining how adaptive mesh refinement allocates computational effort.
8. Review the distinctions between spatial discretisation, algebraic-system solution, convergence, and validation.
9. Check the course reader or official lecture material for the exact equations omitted from the summary before attempting algebraic derivations.

## Missing or incomplete

- None of the lectures in the specified week were identified as missing or incomplete.
- Within the available Lecture 17 source, several exact equations and some technical notation were incomplete or unclear.

## Source manifest

- Lecture 17 (echo-lecture-17-17): complete; summary `df2f7c87000f0e58f9efdb94f4ba26ae9d4da0617d1af3951756cc39277be865`; transcript `fc4ba008504f88530bbe5a13e36b3f93f4f3c622b028373b8d999225ee510f3d`; summary path `[local source path redacted]`
