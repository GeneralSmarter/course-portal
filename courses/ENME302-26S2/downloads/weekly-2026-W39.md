<!-- week-id: 2026-W39 -->
<!-- generated-at: 2026-10-07T10:46:42.484209+13:00 -->
# ENME302-26S2 weekly summary

## Coverage

This week covered Lectures 33–36:

- Lecture 33: Quiz 3 review, heat-equation preparation, numerical error, consistency, and the FTCS scheme.
- Lecture 34: Assignment 2 heat-transfer modelling, FTCS stability, and Du Fort–Frankel consistency.
- Lecture 35: Von Neumann stability analysis, convergence, Lax equivalence, and optimisation fundamentals.
- Lecture 36: Explicit finite differences for Assignment 2, convexity tests, global and local optimisation, line searches, penalty functions, and simulation-driven design.

No lectures were identified as missing or incomplete.

## Main concepts

- Numerical simulation proceeds through preprocessing, solving, and post-processing.
- Numerical results contain model, discretisation, solution, and total error.
- Consistency concerns whether the discretised equations approach the governing PDE as the grid spacings tend to zero.
- Stability concerns whether numerical errors remain bounded during computation.
- Convergence means that the computed solution approaches the exact PDE solution as the spatial and temporal discretisations are refined.
- For a well-posed linear initial-value problem, the Lax equivalence theorem relates consistency and stability to convergence.
- The FTCS heat-equation scheme is explicit: all values on the update right-hand side come from the previous time level.
- FTCS stability requires the dimensionless parameter λ to satisfy λ ≤ 1/2 for the simplified one-dimensional heat equation.
- Assignment 2 models transient heating of a chicken patty with temperature-dependent thermal conductivity, making the heat equation nonlinear.
- Assignment 2 uses Dirichlet, Neumann, symmetry, and Robin or convection boundary conditions.
- Mesh convergence and time-step convergence should be checked before accepting numerical results.
- Non-uniform grids require local node spacings to be retained in spatial derivative approximations.
- When thermal conductivity appears inside a spatial derivative, it should be evaluated at the relevant midpoint.
- A ghost node can be used to impose a Neumann boundary condition while retaining a central-difference treatment.
- Convexity can be assessed using the epigraph, Jensen’s inequality, or the Hessian.
- Monte Carlo sampling and grid search are global exploration methods; steepest descent is a local method.
- A practical strategy for multimodal problems is to search globally first, then refine a promising region locally.
- Backtracking line search reduces the step size until sufficient objective-function decrease is obtained.
- Penalty functions convert constrained optimisation into a modified, usually softly constrained, objective.
- Parameter optimisation changes selected variables, shape optimisation changes boundaries, and topology optimisation permits more fundamental changes such as internal holes.

## Equations and worked patterns

One-dimensional heat equation:

∂T/∂t = α ∂²T/∂x²

Thermal diffusivity:

α = k/(ρc)

Forward-time, centred-space discretisation:

(Tᵢⁿ⁺¹ − Tᵢⁿ)/Δt − α(Tᵢ₊₁ⁿ − 2Tᵢⁿ + Tᵢ₋₁ⁿ)/(Δx)² = 0

Equivalent FTCS update:

Tᵢⁿ⁺¹ = Tᵢⁿ + λ(Tᵢ₊₁ⁿ − 2Tᵢⁿ + Tᵢ₋₁ⁿ)

where:

λ = αΔt/(Δx)²

For the simplified one-dimensional FTCS scheme:

λ ≤ 1/2

or equivalently:

Δt ≤ (Δx)²/(2α)

The FTCS truncation error is:

τ = O(Δt) + O((Δx)²)

Therefore, the scheme is first-order accurate in time and second-order accurate in space.

The von Neumann error mode is represented as:

εᵢⁿ = Eⁿ exp(ik i Δx)

The FTCS amplification factor is:

γ = 1 − 4λ sin²(kΔx/2)

Stability requires:

|γ| ≤ 1

For the Assignment 2 heat equation with temperature-dependent conductivity:

ρcₚ ∂T/∂t = ∇·(κ(T)∇T)

A general convective boundary condition is:

−κ ∂T/∂n = h(Tₛ − T∞)

For the assignment:

- Initial temperature: T(x, 0) = 3 °C.
- Simplified bottom boundary temperature: T = 210 °C.
- Surrounding-air temperature: T∞ = 20 °C.
- Convective coefficient: h = 25 W m⁻² K⁻¹.
- Cooking criterion: min T(x, t_cooked) ≥ 80 °C.

Steepest descent:

xₖ₊₁ = xₖ − hₖ∇f(xₖ)

A typical stopping condition is:

||∇f(xₖ)|| < ε

For a descent direction d, an ideal line-search step is:

h* = arg minₕ≥₀ f(x + hd)

A soft penalty formulation is:

f̃(x) = f(x) + αP(x)

For the constraint x₁ ≤ 5, one stated penalty is:

P(x₁) = max(0, x₁ − 5)

Jensen’s inequality for convexity is:

f((1 − θ)x_A + θx_B) ≤ (1 − θ)f(x_A) + θf(x_B)

for 0 ≤ θ ≤ 1.

For a twice-differentiable multivariable function, convexity is associated with a positive semi-definite Hessian.

## Warnings and deadlines

- Assignment 2 is an individual digital submission through the course page.
- The assignment is due on a Tuesday in Week 12. An exact calendar date was not stated in the summaries.
- The assignment is worth 10% of the course grade.
- The report is limited to five pages.
- The submission archive has a 20 MB size limit.
- COMSOL solution data can make the archive unnecessarily large because temperatures may be stored at every node and saved time step. Delete unneeded solution data before submission if it can be recreated.
- Check the uploaded files after submission to confirm that the correct files were submitted and are not corrupted.
- Send questions or concerns by email rather than relying on submission comments, because teaching staff may not receive notifications for comments.
- The report should include discretisation, boundary conditions, temperature plots, mesh-convergence results, heat fluxes, Python and COMSOL comparisons, 2D and 3D comparisons, the circular axisymmetric model, flipping-time optimisation, and the improved model.
- The exact temperature-dependent conductivity correlation from Murphy and Marks (1999) was not given in the lecture summary; use the assignment brief or referenced source rather than reconstructing it.
- The exact Assignment 2 finite-difference formula and some Du Fort–Frankel indexing should be checked against the assignment or course notes before implementation.
- The FTCS condition λ ≤ 1/2 is stated for the simplified one-dimensional discussion. Do not automatically apply it to a multidimensional discretisation without checking the relevant scheme.

## Recall questions

1. What are the differences between model error, discretisation error, solution error, and total error?
2. Why is the FTCS heat-equation scheme explicit?
3. Derive the FTCS stability condition λ ≤ 1/2 using the amplification factor.
4. What does the Lax equivalence theorem require, and what does it relate?
5. Why does temperature-dependent thermal conductivity make the Assignment 2 heat equation nonlinear?
6. How do symmetry, Neumann, Dirichlet, and Robin boundary conditions differ in the Assignment 2 model?
7. Why should thermal conductivity be evaluated at a midpoint when it appears inside a spatial derivative on a non-uniform grid?
8. State Jensen’s inequality and explain its geometric interpretation.
9. What is the difference between global search methods and steepest descent?
10. Why can a penalty method fail to enforce a constraint exactly?

## Practice priorities

1. Re-derive the FTCS update and the λ ≤ 1/2 stability restriction.
2. Practise explaining consistency, stability, convergence, and their relationship under the Lax equivalence theorem.
3. Implement or work through a small explicit heat-equation example using previous-time-level values.
4. Practise handling non-uniform spatial spacing and midpoint conductivity values.
5. Review how ghost nodes impose Neumann boundary conditions.
6. Check mesh and time-step convergence for a heat-transfer calculation.
7. Map the Assignment 2 model requirements: geometry, initial condition, boundary conditions, cooking criterion, heat fluxes, and dimensional comparisons.
8. Work through Jensen’s inequality for convex and non-convex functions.
9. Practise one or two steepest-descent iterations and examine the effect of large and small step sizes.
10. Compare Monte Carlo search, grid search, steepest descent, and backtracking line search on a multimodal objective.

## Missing or incomplete

None. All four specified lecture summaries were available.

## Source manifest

- Lecture 33 (echo-lecture-33-33): complete; summary `b1378a82c097d47eabd1668578e7de5a686dd094ac04d6af647efc9f8570a3fc`; transcript `d7348a6d536d540368287af36244995dd56172fe95e30d64ff8bf6507540c5a2`; summary path `[local source path redacted]`
- Lecture 34 (echo-lecture-34-34): complete; summary `f84c6095fb98dc7a430c0aeb29cb3232cad299d7beb974fa3efa2416995f0f27`; transcript `ace06eacbafa682b5cbf7ca16bb62a4e678504695b1a893200984ce96ebb1fd9`; summary path `[local source path redacted]`
- Lecture 35 (echo-lecture-35-35): complete; summary `f70867e12847aae677dd4f2f9a0dde418fa3b6a30640ad540af7cedc278cac49`; transcript `8f5fac49e40679eb065591e42cdb81b36708892835bf39f1b5285d317f1b5dc2`; summary path `[local source path redacted]`
- Lecture 36 (echo-lecture-36-36): complete; summary `68feea67bfcd6408e9ab497c940b6f2ce026f2732c42112a7021f5748fca4a85`; transcript `6660b823bac34fb1669dd2e3b813a8f95d39d6422b9d3dd9934525ddcfc3572d`; summary path `[local source path redacted]`
