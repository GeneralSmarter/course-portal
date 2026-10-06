<!-- week-id: 2026-W40 -->
<!-- generated-at: 2026-10-07T11:02:13.604381+13:00 -->
# ENME302-26S2 weekly summary

## Coverage

Week 2026-W40 covers lectures 37–40, within 2026-09-28T00:00:00+13:00 to 2026-10-04T23:59:00+13:00.

- Lecture 37: One-dimensional transient heat transfer, COMSOL model reduction, finite-element fundamentals, and linear one-dimensional shape functions.
- Lecture 38: Linear versus quadratic finite elements, local coordinates, quadratic shape functions, and thermal-diffusivity parameter estimation.
- Lecture 39: Debugging the thermal-diffusivity optimisation, adaptive time stepping, weighted residuals, Galerkin formulation, and integration by parts.
- Lecture 40: Assembly of four linear elements, global stiffness and forcing matrices, boundary conditions, and interpretation of discretisation error.

## Main concepts

- A three-dimensional heat-transfer problem can be reduced to one dimension when geometry, boundary conditions, heat sources, and symmetry imply variation only along one direction.
- A thermally insulated boundary is represented by zero normal heat flux, a homogeneous Neumann condition.
- Backward-in-time, central-in-space discretisation evaluates the spatial terms at the new time level.
- Finite elements approximate a continuous field using elements, nodes, and shape functions.
- Linear elements use two nodes; quadratic elements use three nodes, including a midpoint node.
- Four linear elements require five global nodes because adjacent elements share interface nodes.
- Quadratic interpolation can represent a quadratic field exactly when the nodal arrangement is appropriate. Linear interpolation produces piecewise-linear approximations and discretisation error between nodes.
- A normalised local coordinate maps an element to 0 ≤ ξ ≤ 1 and simplifies shape-function derivation.
- The finite-element governing equation is imposed in a weak or integrated sense rather than pointwise within each element.
- In the Galerkin method, the shape functions are used as the weighting functions.
- Integration by parts reduces the highest derivative in the weak formulation from second order to first order.
- Element equations are assembled into a global system. Contributions from adjacent elements accumulate at shared nodes.
- Internal gradient terms cancel during assembly because neighbouring elements contribute opposite signs.
- Mesh refinement generally reduces discretisation error, but numerical parameter estimates can also be affected by solver tolerances and evaluation-time handling.
- Inverse problems identify an unknown parameter by minimising the discrepancy between a model response and a measured or prescribed target.
- Solver output times and internal adaptive time steps are not necessarily the same. An objective must be evaluated at the intended physical time.

## Equations and worked patterns

Linear two-node interpolation over an element from x₁ to x₂:

u(x) = N₁(x)u₁ + N₂(x)u₂

N₁(x) = (x₂ − x)/(x₂ − x₁)

N₂(x) = (x − x₁)/(x₂ − x₁)

The shape functions satisfy the nodal conditions:

N₁(x₁) = 1, N₁(x₂) = 0

N₂(x₁) = 0, N₂(x₂) = 1

Their derivatives and the element gradient are:

dN₁/dx = −1/(x₂ − x₁)

dN₂/dx = 1/(x₂ − x₁)

du/dx = (u₂ − u₁)/(x₂ − x₁)

The element integral is:

∫ₓ₁ˣ² u(x) dx = ((x₂ − x₁)/2)(u₁ + u₂)

For a quadratic element, use:

ξ = (x − xᵢ)/(xᵢ₊₁ − xᵢ)

with nodes at ξ = 0, 1/2, and 1. The quadratic interpolation is:

u(ξ) = N₁(ξ)u₁ + N₂(ξ)u₂ + N₃(ξ)u₃

N₁(ξ) = 2ξ² − 3ξ + 1

N₂(ξ) = −4ξ² + 4ξ

N₃(ξ) = 2ξ² − ξ

For the transient heat-transfer parameter-identification example:

∂T/∂t = α ∂²T/∂x²

T(0,t) = 0

T(L,t) = 0

T(x,0) = 100 sin(πx/L)

The model targeted the midpoint condition:

T(L/2, 6.75 min) = 50 °C

The objective was:

J(α) = [T(L/2, t_f; α) − 50]²

The corrected identification gave approximately α = 1.11 cm²/s to three significant figures. The earlier approximately 1.25 result arose because the optimisation was effectively matching the temperature at 6 minutes rather than 6.75 minutes.

For a steady one-dimensional finite-element problem:

d²T/dx² + F(x) = 0

The residual is:

R(x) = d²T̃/dx² + F(x)

The weighted-residual statement is:

∫Ω WᵢR dx = 0

The Galerkin choice is Wᵢ = Nᵢ:

∫Ω NᵢR dx = 0

Integration by parts gives:

∫ₓ₁ˣ² Nᵢ d²T̃/dx² dx
= [Nᵢ dT̃/dx]ₓ₁ˣ²
− ∫ₓ₁ˣ² (dNᵢ/dx)(dT̃/dx) dx

For a linear element of length Δx, the displayed stiffness pattern is:

K⁽ᵉ⁾ = (1/Δx)
[[1, −1],
 [−1, 1]]

For a uniform source F:

f⁽ᵉ⁾ = (FΔx/2)
[1,
 1]

Worked numerical pattern for F = 10 and Δx = 2.5:

f⁽ᵉ⁾ =
[12.5,
 12.5]

K⁽ᵉ⁾ =
[[0.4, −0.4],
 [−0.4, 0.4]]

For four equal elements, the displayed global stiffness matrix is:

Kᴳ =
[[0.4, −0.4, 0, 0, 0],
 [−0.4, 0.8, −0.4, 0, 0],
 [0, −0.4, 0.8, −0.4, 0],
 [0, 0, −0.4, 0.8, −0.4],
 [0, 0, 0, −0.4, 0.4]]

The assembled source contributions are 12.5 at each end node and 25 at each interior node, before applying boundary terms.

## Warnings and deadlines

- No verified deadlines are stated in the supplied lecture summaries.
- Lecture 37 mentions Quiz 5 topics and an assignment, but the summaries explicitly caution that assessment timing and related instructions should be checked against official course material.
- The thermal-diffusivity optimisation is highly sensitive to evaluating the objective at the correct time. Confirm the actual solver output times rather than relying only on the requested range.
- The summaries contain transcript-derived uncertainties concerning some equation conventions, conductivity factors, boundary-gradient signs, software details, and intermediate numerical values.
- The finite-element derivation is described as examinable. Assessment may use a variable source term or a different differential equation, so showing the derivation is more reliable than memorising only the displayed numerical matrices.
- The exact physical units of the displayed 0.4, −0.4, and 12.5 coefficients are not established in the summaries.
- Do not rely on the uncertain intermediate temperature values near 245–254 without checking the lecture code or course material.

## Recall questions

1. What assumptions allow the copper-cube heat-transfer problem to be reduced to one spatial dimension?
2. What is the difference between a Dirichlet temperature condition and a homogeneous Neumann no-flux condition?
3. Why do four linear finite elements require five global nodes?
4. What is the purpose of the local coordinate ξ, and where do the three quadratic-element nodes lie?
5. Derive the two linear shape functions for an element from x₁ to x₂ and verify their nodal values.
6. Why can a quadratic element represent a quadratic field exactly while a linear element generally cannot?
7. Why did matching the midpoint temperature at 6 minutes produce a larger estimated diffusivity than matching it at 6.75 minutes?
8. What is the purpose of the residual in the weighted-residual method?
9. Why is integration by parts required when using piecewise-linear finite elements?
10. Why do interior gradient terms cancel during global assembly, while external boundary-gradient terms remain?

## Practice priorities

1. Derive the linear shape functions, their derivatives, the constant element gradient, and the shape-function integrals.
2. Derive the quadratic shape functions from the nodal conditions at ξ = 0, 1/2, and 1.
3. Practise forming the residual, applying Galerkin weighting, integrating by parts, and identifying the stiffness and source contributions.
4. Assemble the four-element global stiffness matrix from the two-node element matrix.
5. Assemble the global forcing vector and explain why interior nodes receive two source contributions.
6. Apply no-flux and prescribed-temperature boundary conditions, including substitution and right-hand-side rearrangement.
7. Reproduce the source-vector and stiffness-matrix calculations for F = 10 and Δx = 2.5.
8. Explain how mesh refinement and interpolation order affect discretisation error.
9. Rework the thermal-diffusivity identification workflow, ensuring that the objective is evaluated at 6.75 minutes.
10. Validate numerical results against physical expectations, analytical solutions, actual solver times, and units.

## Missing or incomplete

None.

## Source manifest

- Lecture 37 (echo-lecture-37-37): complete; summary `4b5fe736a5b46192f2f42d072833d21abeccecdae0fa1177dba83f772de04f36`; transcript `7a7d0fa54cf93d06ebaf956cc66f6cee8b351a08da09123ac69fa2e9cc0cc7ca`; summary path `[local source path redacted]`
- Lecture 38 (echo-lecture-38-38): complete; summary `19055b60299ec56f81fe7fe3ec3086998c1c25a22e72d3a60e68570940acc20c`; transcript `e5864317cb88bd71e8eff998a75e0460f4cad61bae28976a87036d6e89ce02f5`; summary path `[local source path redacted]`
- Lecture 39 (echo-lecture-39-39): complete; summary `70626a904ff7005d5b1401958b13dfdf263e7d7f3aacf8863c6de0da56294d0e`; transcript `e0a0348851939ba9f69f1e273548368f7c7df0c3d0de9c1484d5a87c5dde2c10`; summary path `[local source path redacted]`
- Lecture 40 (echo-lecture-40-40): complete; summary `9f432965fcc649e8739d209f26452979eeea7bb04f3a9e85650c8378c8cbb8fb`; transcript `b2faa6cc7af00701aa65478b35bc86e02f83f3a9599341b6fb11173da0fa0602`; summary path `[local source path redacted]`
