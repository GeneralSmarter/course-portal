<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-12T09:54:16.393355+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Week: 2026-W33, covering 2026-08-10T00:00:00+12:00 to 2026-08-12T09:53:08.362431+12:00.
- Source covered: Lecture 17 summary, generated 2026-08-10.
- Focus: partial differential equations, numerical simulation, modelling assumptions, discretisation, verification, validation, and engineering applications.
- Coverage status: complete. No lectures were identified as missing or incomplete.

## Main concepts

- PDE applications include fluid mechanics, moving boundaries, fluid-solid coupling, heat transfer, lava flows, tsunami propagation, and biomedical mechanics.
- Numerical models should not be treated as black boxes. Their governing physics, assumptions, geometry, conditions, discretisation, convergence, and physical credibility must be assessed.
- A moving-boundary problem involves a domain boundary that changes with time. Examples included clay erosion and melting ice.
- Fluid-solid coupling occurs when fluid behaviour changes the solid boundary and the evolving boundary changes the fluid domain.
- Reynolds number was connected to flow attachment, separation, wakes, and vortex formation. The clay-cylinder example used approximately \(Re \approx 30{,}000\).
- Lava-flow modelling can use a reduced model when the flow is much thinner horizontally than its overall extent and the simplifying assumptions are justified.
- Forward problems predict behaviour from known parameters. Inverse problems adjust unknown parameters so model predictions match observations.
- Shallow-water or Saint-Venant models reduce the computational cost of tsunami simulation by assuming the vertical water-depth scale is small relative to the horizontal wave-length scale.
- Adaptive mesh refinement begins with a coarse grid and locally increases resolution where gradients, velocities, error estimates, or other indicators show that more detail is needed.
- Elliptic, parabolic, and hyperbolic PDEs have different mathematical characteristics and solution strategies.
- Boundary conditions are required to constrain the solution. Time-dependent problems also require initial conditions.
- Numerical methods discussed include finite differences, finite volumes, and finite elements.
- Accuracy, consistency, stability, and convergence are separate numerical properties that must be assessed.
- Verification checks whether the equations were implemented and solved correctly. Validation checks whether the model represents the real physical system adequately.
- Engineering analysis may use established standards, simplified analytical methods, physical experiments, numerical simulation, or a combination of these.

## Equations and worked patterns

- Reynolds number:
  \[
  Re \approx 30{,}000
  \]
  This was the approximate value used for the clay-cylinder crossflow example. The full definition was not stated in the source.
- Lava thickness:
  \[
  H = H(x,t)
  \]
  Here, \(H\) is the dependent variable, while \(x\) and \(t\) are the spatial and temporal independent variables. The full governing PDE was not provided.
- Temperature-dependent lava viscosity:
  \[
  \mu = \mu(T;\text{unknown parameters})
  \]
  The source supports temperature dependence and unknown parameters, including an exponential coefficient denoted \(\alpha\), but does not provide a reliable exact functional form.
- Moving-interface pattern: the melting interface velocity depends on the normal temperature gradient and material or thermal properties including thermal conductivity, density, and heat capacity. The exact Stefan-type equation was not captured.
- Shallow-water modelling pattern:
  - Start from the full fluid description.
  - Apply the long-wave or shallow-water assumption.
  - Solve for water height or free-surface elevation and horizontal velocity components \(u\) and \(v\).
  - Use local mesh refinement where the wave solution requires greater resolution.
- Numerical-modelling workflow:
  - Identify dominant physics.
  - Simplify geometry where justified.
  - Define governing equations and initial or boundary conditions.
  - Discretise the equations.
  - Solve the resulting algebraic system.
  - Check numerical properties and convergence.
  - Verify against a benchmark or known solution.
  - Postprocess and visualise.
  - Validate against measurements or trusted real-system behaviour.
  - Decide whether the model is adequate for the engineering purpose.

## Warnings and deadlines

- No specific deadlines were stated in the source summary.
- Exact forms of the Navier-Stokes, continuity, moving-interface, lava-flow, and shallow-water equations were not captured reliably. Do not reconstruct them from this summary alone.
- Administrative details such as assessment percentages, quiz timing, exam scope, and software requirements may change. The source advises confirming current information on the ENME302 course page.
- The source notes that the final exam was stated to cover the lecturer’s content rather than the first four weeks, but this scope requires confirmation against official course information.
- Numerical results require independent checks. A verified implementation can still use an inadequate physical model, while agreement with one measurement does not by itself prove correct implementation.

## Recall questions

1. What distinguishes verification from validation in numerical modelling?
2. Why is the clay-cylinder erosion example a fluid-solid coupling problem?
3. How does Reynolds number affect separation and wake formation around the cylinder?
4. Why does a moving-boundary model need to track the interface velocity?
5. Which thermal and material properties influence the melting-interface model?
6. What is the difference between a forward problem and an inverse problem in the lava-flow example?
7. What physical scale assumption underlies the shallow-water or Saint-Venant approximation?
8. Why is adaptive mesh refinement useful in tsunami simulations?
9. Why are boundary conditions required, and what additional information is needed for an unsteady problem?
10. What is the difference between spatial discretisation and solving the resulting algebraic system?

## Practice priorities

- Be able to explain the complete numerical-modelling workflow from the engineering problem through verification and validation.
- Practise distinguishing modelling assumptions from numerical-method choices.
- Review the physical meaning and limitations of Reynolds number in the cylinder crossflow example.
- Explain how wall shear stress, interface motion, and changing geometry interact in erosion and melting problems.
- Compare full CFD with reduced lava-flow and shallow-water models, including the assumptions that make reduction reasonable.
- Practise identifying whether a task is a forward problem, inverse problem, verification test, or validation test.
- Review the roles of initial conditions, boundary conditions, mesh refinement, discretisation, convergence, and computational cost.
- Compare finite-difference, finite-volume, and finite-element approaches at the conceptual level.
- Assess when standards, simplified analysis, experiments, or numerical simulation are the most appropriate engineering design approach.

## Missing or incomplete

- No lectures were identified as missing or incomplete for this week.
- Within Lecture 17, several exact equations and some notation were incomplete in the source summary, including:
  - Navier-Stokes equations.
  - Continuity equation.
  - Moving-interface relation for melting ice.
  - Full lava-thickness PDE.
  - Exact temperature-dependent viscosity relation.
  - Shallow-water or Saint-Venant equations.

## Source manifest

- Lecture 17 (echo-lecture-17-17): complete; summary `df2f7c87000f0e58f9efdb94f4ba26ae9d4da0617d1af3951756cc39277be865`; transcript `fc4ba008504f88530bbe5a13e36b3f93f4f3c622b028373b8d999225ee510f3d`; summary path `[local source path redacted]`
