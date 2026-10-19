<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-10-20T12:19:32.657906+13:00 -->
# ENME302-26S2 weekly summary

## Coverage

Rebuilt 20 October 2026 from the corrected source-backed lecture notes. Teaching-week numbering omits the mid-semester break; ISO week identifiers are calendar dates.

- Lecture 17: 2026-08-10. This lecture introduced the remainder of the ENME302 course, focusing on partial differential equations, numerical simulation, modelling assumptions, and the role of verification and validation.  Main themes:  - Applications of fluid mechanics, moving-boundary problems, fluid–solid coupling, heat transfer, lava-flow modelling, tsunami modelling, and biomedical mechanics. - The distinction between analytical engineering methods, experiments, numerical simulation, and established design guidelines. - The general workflow for developing and assessing a numerical model. - The forthcoming study of elliptic, parabolic, and hyperbolic PDEs. - Course logistics, assessment structure, and use of the course reader, Python, and COMSOL.  The lecturer emphasised that numerical software must not be treat

- Lecture 18: 2026-08-12. This is the 12 August 2026 lecture at the start of the Weeks 5–12 PDE block. It reviews modelling failures, compares numerical methods and meshes, then introduces PDE notation, solution methods, boundary/initial conditions, order, linearity and homogeneity. The previous portal copy was the opening structural-FEA lecture and has been replaced.

- Lecture 19: 2026-08-13. Lecture 19 introduced the classification of second-order linear partial differential equations (PDEs) as elliptic, parabolic, or hyperbolic. The classification is based on the coefficients of the second-order derivative terms and the sign of the discriminant \(b^2 - 4ac\).  The lecture used three standard examples:  - Laplace equation: elliptic - Heat equation: parabolic - Wave equation: hyperbolic  The physical behaviour of each class was discussed:  - Elliptic equations generally describe steady-state spatial fields. - Parabolic equations generally describe diffusive, time-dependent processes. - Hyperbolic equations generally describe wave propagation at finite speed.  The lecture also covered homogeneous versus non-homogeneous PDEs, boundary and initial conditions, engineering applicati

- Lecture 20: 2026-08-14. This lecture introduces the derivation and analytical solution of a two-dimensional steady heat-conduction problem using elliptic partial differential equations.  Main topics:  - Derivation of the two-dimensional steady heat equation from conservation of energy. - Use of Fourier’s law to relate heat flux to the temperature gradient. - Recovery of Laplace’s equation for a plate with uniform thermal conductivity and no internal heat generation. - Dirichlet, Neumann, and Robin boundary conditions. - Separation of variables for solving Laplace’s equation on simple rectangular domains. - Classification of separated solutions according to the sign of the separation constant. - Application of boundary conditions to identify admissible solutions. - Use of analytical solutions to validate numerical

## Main concepts

### Lecture 17

- Partial differential equation (PDE)
- Elliptic, parabolic, and hyperbolic PDEs
- Navier–Stokes equations
- Continuity equation
- Reynolds number
- Laminar separation and vortex wakes
- Moving-boundary problem
- Fluid–solid coupling
- Interface velocity
- Wall shear stress
- Heat-transfer-driven melting
- Thermal conductivity, density, and heat capacity
- Lava rheology and viscosity
- Inverse problem and optimisation
- Shallow-water approximation
- Saint-Venant equations
- Computational grid
- Adaptive mesh refinement
- Spatial discretisation
- Finite-difference, finite-volume, and finite-element methods
- Initial and boundary conditions
- Accuracy, consistency, stability, and convergence
- Verification versus validation
- Model assumptions and simplification
- Parametric design and parameter sweeps
- Numerical-model limitations and computational cost

### Course direction and modelling applications

Earlier parts of ENME302 considered finite elements for specific structural cases, including:

- Bars
- Beams
- Trusses

The remaining lectures move toward more general PDE models and numerical methods. The lecturer used examples from fluid mechanics and related fields to show why these methods are useful.

Applications mentioned included:

- Computational fluid dynamics (CFD)
- Moving interfaces and evolving boundaries
- Fluid–structure interaction
- Non-Newtonian fluids
- Melting ice and icebergs
- Silica-scale deposition in geothermal systems
- Lava flows
- Biofluids and blood clots
- Tsunami propagation
- Heat transfer
- Potential flow
- Transient flow
- Elastic bending
- Wave propagation

### Non-Newtonian fluids

Newtonian fluids, such as water, have a comparatively simple relationship between stress and shear rate. Non-Newtonian fluids can change their apparent viscosity depending on the shear rate or the rate at which they are deformed.

Examples mentioned:

- Toothpaste
- Quicksand

Toothpaste was described as behaving like a viscoplastic material: it remains stationary until sufficient stress is applied, then flows when squeezed or pushed.

The transcript uses “visco plastic” and “rheology.” Rheology concerns how materials deform and flow under applied stresses.

### Erosion of a clay cylinder in crossflow

One research example involved modelling the erosion of a clay cylinder exposed to crossflow.

The setup involved:

- Fluid flowing from left to right.
- A cylindrical clay body in the flow.
- Shear separation around the cylinder.
- A downstream wake containing vortical structures.
- A Reynolds number of approximately 30,000.

At sufficiently low flow speed, the flow would be expected to remain attached around the cylinder. At the stated Reynolds number, separation and a wake develop.

The clay erodes because of wall shear stress. The erosion is not spatially uniform:

- The initial body is approximately circular.
- Over time, the shape changes.
- The final shape becomes more triangular or otherwise non-circular.
- The model tracks the evolving solid boundary.

The lecturer described coupling the fluid equations to the velocity of the clay-cylinder interface. The fluid affects the wall shear stress and therefore the erosion rate; the changing solid boundary then alters the fluid domain.

The downstream wake can contain three-dimensional turbulent structures even when the original clay geometry is treated as two-dimensional. The wake structure depends strongly on the Reynolds number.

A related spherical case showed:

- Laminar shear separation.
- Two downstream vortices.
- A non-uniform melting rate.
- A shape that does not remain spherical during melting.

### Melting ice and moving boundaries

For a melting ice body, the interface moves according to the thermal conditions at the surface.

The model requires solving for:

- Temperature in the surrounding domain.
- Temperature gradients at the ice interface.
- The velocity of the moving interface.
- The evolving shape of the ice.

The interface velocity is related to the normal temperature gradient at the surface. The normal direction is perpendicular to the interface.

The transcript indicates that the relationship includes material and thermal parameters such as:

- Thermal conductivity.
- Density.
- Heat capacity.

The example showed ice remaining relatively spherical upstream while developing a flatter or straighter downstream region. The lecturer suggested that vortical flow downstream may transport energy in a way that increases the melting rate there.

This is a moving-boundary problem because the domain boundary changes with time.

### Lava-flow modelling

Lava-flow modelling was presented as an example where simplifying assumptions can greatly reduce the computational problem.

A lava field may have:

- A large horizontal extent.
- A thickness much smaller than its width.
- A complex three-dimensional flow in reality.

A full CFD treatment is possible, but a reduced model may be more practical if the geometry and physics justify the approximation.

The model described the lava thickness as a dependent variable:

- \(H\): lava thickness or height profile.
- \(x\): spatial coordinate.
- \(t\): time.

The model solves a PDE for the height profile \(H(x,t)\). An initial Gaussian-shaped distribution was used as an example of lava emerging from a volcanic opening. Gravity then drives the lava downhill over time.

Lava rheology is strongly dependent on composition. The effective viscosity can:

- Differ between volcanoes.
- Change at the same volcano over time.
- Depend on shear rate and temperature.

If the rheological properties can be estimated in real time, the resulting model could improve lava-flow forecasting.

### Inverse problems and optimisation

The lava example also introduced an inverse problem.

In a forward problem:

- Material parameters are known or specified.
- The model predicts the resulting behaviour.

In an inverse problem:

- Observed behaviour is available.
- Unknown model parameters are adjusted so that the model matches the observations.

The lecture described an unknown viscosity relationship involving:

- Viscosity as a function of temperature.
- An unknown viscosity-related coefficient.
- An exponential coefficient, denoted in the transcript as alpha.

The model error was plotted over possible parameter pairs:

- High error was represented by yellow.
- Low error was represented by purple.
- A low-error region indicated parameter combinations that produced a close match to observations.

The exact viscosity equation was not audible or visible in the transcript, so its detailed functional form cannot be reconstructed reliably.

### Tsunami modelling and shallow-water equations

Tsunami propagation was presented as another application of PDEs and numerical simulation.

Tsunami models can help estimate:

- Whether a tsunami may reach New Zealand.
- How quickly it may arrive after an earthquake.
- How the wave propagates across the ocean.
- The spatial distribution of wave height and velocity.

The lecture referred to an open-source package called Basilisk. The transcript also refers to the work of Stéphane Popinet, although the name is uncertain in the automated transcript.

The tsunami model uses a shallow-water or long-wave approximation. This assumes that the vertical water depth is small relative to the horizontal length scale of the wave.

Under this approximation, the full Navier–Stokes equations can be reduced to a smaller set of nonlinear equations, commonly associated with the shallow-water or Saint-Venant equations.

The unknown fields include:

- Water height or free-surface elevation.
- Horizontal velocity components, referred to as \(u\) and \(v\) in the transcript.

The equations remain nonlinear, but are less computationally expensive than solving the full Navier–Stokes equations.

The lecture animation showed wave propagation from the region of Japan. The wave was described as diffracting or reflecting around objects and boundaries.

### Adaptive mesh refinement

A tsunami does not need uniformly high spatial resolution throughout the entire ocean. High resolution is most useful where the solution has important or rapidly changing behaviour.

Adaptive mesh refinement:

- Starts with a coarse computational grid.
- Refines the grid locally in regions requiring more detail.
- Can use local error estimates.
- Can use local velocity gradients or other indicators.
- Avoids unnecessary computation in regions with relatively smooth behaviour.

The example showed coarse cells away from the main wave region and finer cells near regions of stronger activity.

Even with adaptive refinement, large two-dimensional simulations can require days or weeks. Three-dimensional simulations would generally be more computationally demanding.

### PDE categories and future course content

The remainder of the course will examine three broad PDE classifications:

- Elliptic PDEs
- Parabolic PDEs
- Hyperbolic PDEs

These classes have different mathematical characteristics and require different solution strategies.

The lecture identified future topics including:

- Boundary conditions.
- Initial conditions for time-dependent problems.
- Separation of variables.
- Laplace transforms.
- Analytical solutions for wave equations.
- Steady and transient heat transfer.
- Potential flow.
- Transient flow.
- Elastic bending.
- Wave equations.
- Spatial discretisation.
- Finite differences.
- Finite elements.
- Finite volumes.
- Numerical accuracy.
- Consistency.
- Stability.
- Convergence.
- Optimisation methods.
- Grid generation and geometry modelling.

A unique solution generally requires appropriate boundary conditions. For an unsteady or time-dependent problem, an initial condition is also required.

Without sufficient boundary conditions, the governing PDE may admit infinitely many possible solutions.

### Software and numerical methods

The course will use Python for problems that can be handled directly and COMSOL for more difficult numerical models. The transcript also refers to Basilisk as an open-source package for solving certain fluid and free-surface problems.

The lecturer stressed that software should not be used blindly. A numerical model must be understood sufficiently to assess:

- Whether the governing equations are appropriate.
- Whether the assumptions are justified.
- Whether the geometry has been represented adequately.
- Whether the boundary and initial conditions are correct.
- Whether the mesh is sufficiently refined.
- Whether the numerical solution has converged.
- Whether the result agrees with physical expectations.
- Whether the model has been validated against measurements or other trusted data.

### General numerical-simulation workflow

The numerical-modelling workflow presented was:

1. Begin with a real engineering problem involving potentially complex physics and geometry.
2. Identify the dominant physics.
3. Simplify the geometry where appropriate.
4. Define a mathematical model.
5. Select suitable governing equations and boundary or initial conditions.
6. Discretise the equations using an appropriate numerical method.
7. Solve the resulting algebraic system using linear algebra and numerical algorithms.
8. Check convergence and other numerical properties.
9. Verify the implementation against a benchmark or known solution.
10. Postprocess and visualise the results.
11. Validate the model against measured data or the behaviour of the real system.
12. Decide whether the model is an adequate approximation for the engineering problem.

### Verification and validation

Verification and validation are distinct.

Verification asks whether the equations have been solved correctly. Examples include:

- Checking that the discretised equations were implemented correctly.
- Checking that the algebraic system was solved.
- Checking convergence.
- Comparing with a simple benchmark solution.
- Checking whether numerical errors decrease as expected with refinement.

Validation asks whether the model represents the real physical system adequately. Examples include:

- Comparing predicted room temperatures with temperature-probe measurements.
- Comparing a simulated flow with experimental observations.
- Checking whether the simplified physical assumptions are acceptable for the intended application.

A model may be verified numerically but still fail to represent the real physics accurately. Conversely, agreement with one measurement does not by itself prove that the implementation is correct.

### Engineering design approaches

Four broad approaches to engineering design and analysis were discussed:

1. Established guidelines and standards.
2. Simplified engineering analysis.
3. Physical experimentation.
4. Numerical simulation.

#### Established guidelines and standards

Standards and industry guidelines encode accepted practice for particular design classes. When they cover the design adequately, they are often the most efficient option.

#### Simplified engineering analysis

Engineers may make justified assumptions and use basic methods such as:

- Free-body diagrams.
- Simple analytical models.
- Spreadsheet calculations.
- Python calculations.
- Approximate geometric models.

The validity of the result depends on whether the simplifications preserve the important physics.

#### Physical experiments

Experiments can:

- Improve existing data.
- Generate new data.
- Investigate effects that are difficult to model.
- Test designs over a range of conditions.

An aerofoil experiment was mentioned as an example. Variables could include:

- Angle of attack.
- The onset of stall.
- Wingtip or winglet geometry.

Experiments can be expensive, difficult to scale, or impossible for processes that are too large, too small, too slow, too dangerous, or too difficult to schedule.

#### Numerical simulation

Numerical models are useful when:

- Existing guidelines do not cover the design.
- Existing data does not cover the required operating range.
- Geometry or physics cannot be simplified sufficiently.
- High confidence or high accuracy is required.
- Many design variations need to be explored.
- Measurements throughout a volume are required.
- Experiments would be excessively expensive or impractical.

Numerical simulations can provide detailed fields such as:

- Pressure.
- Velocity.
- Temperature.
- Streamlines.
- Flow variables throughout a volume rather than only at discrete measurement points.

### Advantages and disadvantages of numerical models

Advantages include:

- Prediction across many points in space and time.
- Detailed visualisation of fields.
- Efficient parameter sweeps.
- Reduced need for manufacturing multiple physical prototypes.
- Support for lightweight or optimised designs.
- Exploration of many geometries and operating conditions.
- Support for parametric design.

A simulation can explore many car lengths or other geometric parameters before a smaller number of physical prototypes are built for validation.

Disadvantages include:

- High computational cost.
- Long training time for unfamiliar software.
- Difficult grid and model generation for complex systems.
- Limited documentation for some open-source packages.
- Licensing costs for commercial packages.
- Dependence on modelling assumptions.
- Risk of obtaining a numerical result that is not physically correct.
- Limited transparency in closed commercial software.
- Need for benchmark testing and independent validation.

The lecturer compared closed software to other black-box tools: a result is produced, but the user must still establish whether it is correct.

### Model complexity and simplification

The example of modelling the HVAC behaviour of the lecture room illustrated the modelling process.

The real room has:

- Tiered seating.
- Intricate architectural details.
- People who act as local heat sources.
- Fans or HVAC airflow.
- Natural convection.
- Spatially varying temperature.
- Fluid flow and temperature as coupled dependent variables.

A simplified model might:

- Represent the room geometry as a polygon.
- Approximate tiered seating with straight boundaries.
- Represent people or seating as distributed heat fluxes rather than individual bodies.
- Retain only the dominant fluid-flow and heat-transfer physics.

The aim is not necessarily to reproduce every detail. The aim is to create a model that is sufficiently accurate for the engineering question being asked.

### Numerical simulation history and computing

The lecturer described numerical simulation as a relatively recent engineering capability, with major development beginning around the 1960s.

Progress has resulted from advances in:

- Central processing units (CPUs).
- Graphics processing units (GPUs).
- Computer hardware.
- Numerical algorithms.
- Software implementation.

Numerical simulation is now used across many fields, including:

- Fluid mechanics.
- Aerospace.
- Biomedical engineering.
- Product design.
- Industrial systems.

### Lecture 18

- A model, numerical method and implementation can fail for different reasons; diagnose the layer before changing it (00:00–04:00).
- Verification asks whether the equations/method are being solved correctly; validation concerns agreement of the physical model with measurements (02:00–04:00).
- Finite element, finite difference and finite volume methods represent/discretise the governing equations differently (04:00–16:00).
- PDEs describe an unknown dependent variable over multiple independent variables; partial differentiation varies one coordinate while holding others fixed (30:00–40:00).
- A PDE can admit many solutions; the appropriate boundary and initial conditions select the physical problem (44:00–50:00).

### 1. Diagnose modelling and numerical failures
A computationally expensive model may need further physical simplification, such as modelling an appropriate 2D cross-section rather than an entire 3D system. Insufficient time or memory may instead call for a more efficient solver or implementation; additional CPU cores do not guarantee proportional speedup because partitioning and combining work have overheads. Failure to match a known numerical/analytical benchmark suggests checking discretisation, time resolution, setup and method. Failure to match measurements may indicate that physical assumptions themselves are wrong. The lecturer's deliberately poor heat-transfer example assumes isothermal behaviour for a problem whose purpose is predicting temperature changes.

### 2. Methods and meshes
Finite elements use nodal unknowns and interpolation within elements, enforcing physics in an integrated/weak form. They support structural and field problems and can be used for steady or transient solutions. Finite differences approximate derivatives at grid points, commonly via Taylor expansions; the course's introductory formulation uses a structured grid with identifiable neighbours. Finer spacing changes approximation error and the size/cost of the algebraic system. Finite volumes integrate balances over control volumes and track fluxes, providing a natural conservation framework widely used for CFD. The lecturer presents finite volumes as context, not as this course's detailed teaching focus.

Structured grids provide systematic indexing and known neighbours; a geometrically curved O-grid can still be structured in computational indexing. An unstructured mesh needs explicit connectivity information; “unstructured” does not mean random or disconnected. Geometry, mesh type, approximation and solver choice are related but not interchangeable decisions. The package names in the speech transcript are sometimes misspelled; check the overview slides rather than treating the ASR spelling as authoritative.

### 3. PDE language and derivative meaning
Examples of dependent fields include temperature, displacement and fluid velocity; independent variables include space coordinates and time. The partial x derivative holds the other coordinates fixed while measuring the local x-direction change. Contour lines help visualise a two-variable field. A finite secant slope approximates the derivative; its limiting value as spacing approaches zero defines the derivative. Subscripts such as u_x, u_xx and u_xy are compact derivative notation, not extra independent unknowns.

### 4. Analytical and numerical solution routes
Separation of variables reduces a suitable PDE into ODEs; integral transforms and coordinate/dependent-variable changes may simplify appropriate problems. Choose coordinates to fit geometry, for example polar/cylindrical coordinates for circular domains. Analytical solutions are powerful but typically rely on restricted geometry and assumptions. Numerical methods replace the continuous problem by discrete unknowns and equations, usually at greater computational cost but with broader applicability. Comparing numerical output against an available analytical solution is a verification benchmark; agreement alone does not validate all physical assumptions against experiment.

### 5. Solutions and classification
A candidate function must have the required derivatives in the relevant domain and satisfy the PDE when substituted. For example, u=x²−y² satisfies the two-dimensional Laplace equation because u_xx=2 and u_yy=−2. This is not the unique solution to an unspecified physical problem: boundary conditions, and initial conditions for time-dependent problems, constrain which solution is relevant. PDE order is the highest derivative order. A PDE is linear in u if u and its derivatives occur linearly and coefficients depend only on independent variables; products such as u·u_y or powers of a derivative make it nonlinear. For a linear PDE, homogeneity means no independent forcing/source term: L[u]=0 rather than L[u]=f.

### 6. Course/exam remarks
Around 18:00 the lecturer states the final is worth 50% and requires at least 40% to pass the course. Around 24:00 the lecturer says a supplied formula sheet replaces a personal cheat sheet and that students should be able to integrate and use separation of variables. Treat the current published exam section and formula sheet as authoritative. The survey/IDE discussion is background, not an extra examinable topic. Later personal conversations are not reproduced in these notes.

### Lecture 19

- A PDE is linear when the dependent variable and its derivatives do not appear multiplied together, raised to powers, or inside nonlinear functions.
- A term such as \(u_{xx}\) is still linear. The squared notation refers to the order of differentiation, not to \(u\) being squared.
- A term such as \(u^2\) or \(u^3\) is nonlinear.
- A general second-order PDE in two independent variables can be classified using the coefficients \(a\), \(b\), and \(c\) of the second-order derivative terms.
- The discriminant is
  \[
  \Delta = b^2 - 4ac.
  \]
- Classification:
  - \(\Delta < 0\): elliptic
  - \(\Delta = 0\): parabolic
  - \(\Delta > 0\): hyperbolic
- Laplace equation:
  \[
  T_{xx} + T_{yy} = 0
  \]
  It represents a typical elliptic PDE.
- One-dimensional heat equation:
  \[
  T_t = \kappa T_{xx}
  \]
  It represents a typical parabolic PDE.
- One-dimensional wave equation:
  \[
  u_{xx} = \frac{1}{c^2}u_{tt}
  \]
  or, equivalently,
  \[
  u_{xx} - \frac{1}{c^2}u_{tt}=0.
  \]
  It represents a typical hyperbolic PDE.
- Homogeneous means that the source term on the right-hand side is zero.
- A source term makes the PDE non-homogeneous. For Laplace-type equations, a nonzero source term gives a Poisson equation.
- Elliptic problems generally require boundary conditions around the spatial domain.
- Parabolic problems require an initial condition in time and boundary conditions in space.
- Hyperbolic problems involve propagation of information or disturbances at finite speed.
- Linear combinations of solutions to a homogeneous linear PDE are also solutions.
- The superposition principle does not generally apply in the same way to a non-homogeneous equation with a source term.

### Linear and nonlinear PDEs

The lecture began by revisiting partial derivatives and PDE terminology.

A second derivative such as

\[
\frac{\partial^2 u}{\partial x^2}
\]

is linear with respect to \(u\). Although the derivative notation contains a square, this means that differentiation is performed twice. It does not mean that the dependent variable is squared.

Examples of nonlinear terms include:

\[
u^2
\]

and

\[
u^3.
\]

The lecture stated that the course would focus mainly on linear equations because they are more tractable analytically and numerically.

### General second-order PDE form

The lecture referred to a general second-order PDE containing second derivatives in two independent variables, described in the transcript as \(x\) and \(y\). The exact displayed form was not captured reliably by the local ASR, but the classification uses the coefficients of

\[
u_{xx}, \qquad u_{xy}, \qquad u_{yy}.
\]

These coefficients were referred to as \(a\), \(b\), and \(c\), respectively. Lower-order derivative terms and a source term may also be present.

The classification is determined by

\[
b^2 - 4ac.
\]

The independent variables do not have to be \(x\) and \(y\). They may instead be \(x\) and \(t\), as in the heat and wave equations.

### Elliptic equations: Laplace equation

The two-dimensional Laplace equation was given as

\[
\frac{\partial^2 T}{\partial x^2}
+
\frac{\partial^2 T}{\partial y^2}
=0.
\]

This can describe the steady-state temperature distribution in a thin plate.

For the classification:

\[
a=1,\qquad b=0,\qquad c=1.
\]

Therefore,

\[
b^2-4ac
=
0^2-4(1)(1)
=
-4<0.
\]

The equation is therefore elliptic.

The lecture emphasised that the solution at one point is influenced by the values throughout the domain. A membrane fixed around its perimeter and subjected to a pressure difference was used as a physical analogy. The membrane may form a peak near the centre while remaining in a steady state.

For an elliptic problem, boundary conditions around the closed boundary are needed to obtain a unique solution. Without sufficient boundary information, there may be infinitely many solutions.

The lecture also identified other possible engineering applications of elliptic equations:

- Steady-state heat transfer through a plate
- Hydraulic head distribution in groundwater flow through an aquifer
- Electric potential distributions

### Parabolic equations: heat equation

The one-dimensional heat equation was given in the form

\[
\frac{\partial T}{\partial t}
=
\kappa
\frac{\partial^2 T}{\partial x^2},
\]

where \(\kappa\) was described as a diffusion coefficient or thermal diffusivity.

Rearranging into a form suitable for classification gives

\[
\kappa T_{xx}-T_t=0.
\]

There is no mixed derivative and no second-order derivative in time. Thus, using the coefficients associated with \(T_{xx}\), \(T_{xt}\), and \(T_{tt}\),

\[
a=\kappa,\qquad b=0,\qquad c=0.
\]

The discriminant is

\[
b^2-4ac
=
0^2-4(\kappa)(0)
=
0.
\]

The equation is therefore parabolic.

Parabolic equations are diffusive and time-dependent. The solution is advanced or “marched” forward in time. The temperature distribution depends on the initial temperature field as well as the boundary conditions.

The lecture used heating a spoon in hot liquid as an intuitive example. The spoon begins heating immediately, but its temperature does not instantly become equal to the liquid temperature.

For a one-dimensional equation that is first order in time and second order in space:

- One initial condition is generally required.
- Two spatial boundary conditions are generally required.

The lecture also mentioned transient heat conduction in a long, thin rod. Possible conditions include fixed-temperature boundaries, convective heat transfer, and source terms. The exact wording of one term was unclear in the ASR and may have been “convective heat transfer.”

### Hyperbolic equations: wave equation

The one-dimensional wave equation was given approximately as

\[
\frac{\partial^2 u}{\partial x^2}
=
\frac{1}{c^2}
\frac{\partial^2 u}{\partial t^2},
\]

where \(u\) is displacement and \(c\) is the wave propagation speed.

Putting all terms on one side gives

\[
u_{xx}
-
\frac{1}{c^2}u_{tt}
=0.
\]

The coefficients are therefore

\[
a=1,\qquad b=0,\qquad c=-\frac{1}{c^2}.
\]

The use of \(c\) both as a PDE coefficient label and as wave speed can be confusing. The lecture appeared to distinguish these by context and possibly by capitalisation.

The discriminant is

\[
b^2-4ac
=
0^2
-
4(1)\left(-\frac{1}{c^2}\right)
=
\frac{4}{c^2}>0.
\]

The equation is therefore hyperbolic.

Hyperbolic equations are wave-like or propagative. Examples discussed included:

- A plucked guitar string
- Waves on a string
- Ocean waves
- Tsunami propagation
- Acoustic or sound propagation

The lecture emphasised that information propagates at finite speed in hyperbolic problems. In contrast, diffusion models are not described as finite-speed wave propagation.

Hyperbolic equations can be numerically difficult because they may be unstable if discretised or time-stepped incorrectly. Without damping, an idealised wave may continue propagating indefinitely. Physical damping causes the amplitude to decrease.

The wave speed may depend on physical properties such as tension and density. The transcript suggested a relation involving tension and density, but the exact equation was not stated clearly enough to reproduce confidently. The lecturer also mentioned sound propagation, where \(c\) represents the speed of sound and \(u\) may represent a pressure-related quantity; this part should be checked against the lecture slides.

### Physical comparison of the three PDE classes

The lecture’s physical interpretation can be summarised as follows:

Elliptic:

- Usually steady-state.
- The solution is determined throughout a spatial domain.
- Boundary conditions are central.
- Example: temperature in a plate at steady state.

Parabolic:

- Time-dependent and diffusive.
- The solution evolves from an initial condition.
- Boundary conditions are also needed.
- Example: heating or cooling of a rod.

Hyperbolic:

- Time-dependent and propagative.
- Disturbances travel through the domain at finite speed.
- Initial conditions determine the disturbance evolution.
- Example: waves on a string or in the ocean.

### Homogeneous and non-homogeneous equations

A PDE was described as homogeneous when the source term on the right-hand side is zero.

For a general equation represented schematically as

\[
\mathcal{L}[u]=g,
\]

where \(\mathcal{L}\) is a differential operator:

- \(g=0\): homogeneous equation
- \(g\neq 0\): non-homogeneous equation

The source term was described as independent of the dependent variable in the relevant discussion.

A Laplace-type equation with a source term,

\[
T_{xx}+T_{yy}=f(x,y),
\]

is commonly called the Poisson equation. The lecture stated that the Poisson equation is not homogeneous because of the nonzero source term.

### Boundary and initial conditions

The lecture gave a rule of thumb based on derivative order:

- A first-order derivative in time generally requires one initial condition.
- A second-order derivative in one spatial coordinate generally requires two boundary conditions.
- A second-order equation in both \(x\) and \(y\) requires boundary information around the domain; the lecture referred to four boundary conditions in a simple rectangular-domain interpretation.

These requirements depend on the exact PDE, domain, and boundary type. The rule is useful for the examples discussed but should not be applied mechanically to every PDE.

### Diffusion and species transport

The lecture extended the diffusion idea beyond heat transfer to species diffusion.

If \(\phi\) represents concentration, a diffusion equation may contain a term of the form

\[
D\frac{\partial^2\phi}{\partial x^2},
\]

where \(D\) is a diffusion coefficient.

A beaker containing dye was used as an example. If the liquid is not mixed, the dye spreads through diffusion alone. A larger diffusion coefficient corresponds to faster diffusion, all else being equal.

The ASR rendered some notation around this example unreliably. The symbol for concentration was heard as “phi,” and the coefficient was heard as \(D\), but these should be confirmed from the slides.

### Superposition principle for Laplace’s equation

The lecture considered two functions \(T_1\) and \(T_2\) satisfying Laplace’s equation:

\[
T_{1,xx}+T_{1,yy}=0,
\]

\[
T_{2,xx}+T_{2,yy}=0.
\]

It then defined

\[
T=\alpha T_1+\beta T_2,
\]

where \(\alpha\) and \(\beta\) are constants.

Substituting into Laplace’s equation gives

\[
T_{xx}+T_{yy}
=
\frac{\partial^2}{\partial x^2}
(\alpha T_1+\beta T_2)
+
\frac{\partial^2}{\partial y^2}
(\alpha T_1+\beta T_2).
\]

Because \(\alpha\) and \(\beta\) are constants,

\[
T_{xx}+T_{yy}
=
\alpha(T_{1,xx}+T_{1,yy})
+
\beta(T_{2,xx}+T_{2,yy}).
\]

Each bracketed expression is zero, so

\[
T_{xx}+T_{yy}=0.
\]

Therefore, any linear combination of solutions is also a solution. This is the superposition principle for a linear homogeneous PDE.

The result extends to sums of multiple solutions, subject to the same linearity and homogeneity conditions.

### Example harmonic function

The lecture checked whether

\[
T(x,y)=x^3-3xy^2
\]

satisfies Laplace’s equation.

First derivatives:

\[
T_x=3x^2-3y^2,
\]

\[
T_y=-6xy.
\]

Second derivatives:

\[
T_{xx}=6x,
\]

\[
T_{yy}=-6x.
\]

Therefore,

\[
T_{xx}+T_{yy}
=
6x-6x
=
0.
\]

Thus, the function satisfies Laplace’s equation.

### PDE with zero \(x\)-derivative

The lecture briefly considered

\[
\frac{\partial u}{\partial x}=0.
\]

Any function depending only on \(y\), such as

\[
u=f(y),
\]

satisfies this equation because its derivative with respect to \(x\) is zero.

The lecture connected this type of result with a method mentioned earlier in the week. The exact method name was not captured reliably by the ASR.

### Numerical methods and coding discussion

The lecturer connected the course material to numerical methods, particularly discretisation, consistency, and convergence. The stated purpose was to understand the mechanics and algorithms behind numerical methods rather than use commercial software or AI tools blindly.

The lecturer’s main points were:

- Students should understand how numerical methods work.
- AI can assist with explaining or debugging code, but generated results must be checked.
- If a student does not understand the expected method or result, they cannot reliably verify AI-generated code.
- Short course code should be manageable without outsourcing the learning process.
- Debugging is a useful skill and may be assessed directly.
- The quizzes were described as having short coding and algebraic questions.
- The transcript stated that AI should not be used to complete the quizzes themselves.
- Exercises and model solutions were presented as appropriate places to practise and seek help.

The lecture also described quiz mechanics, but some administrative details may depend on the current course configuration and should be checked in the official course site.

### Lecture 20

- Elliptic PDEs can be derived from integral statements of physical principles, such as conservation of mass or energy.
- For a steady-state heat problem without internal heat generation, heat entering a differential element must equal heat leaving it.
- In a two-dimensional thin plate, insulated front and back faces imply that temperature varies only with \(x\) and \(y\).
- Heat flux is a vector field with units of \(\mathrm{W/m^2}\).
- Fourier’s law is
  \[
  \mathbf{q}=-k\nabla T,
  \]
  where \(k\) is thermal conductivity.
- The negative sign in Fourier’s law indicates that heat flows down the temperature gradient, from hotter regions toward colder regions.
- Combining conservation of energy with Fourier’s law gives
  \[
  \frac{\partial}{\partial x}\left(k\frac{\partial T}{\partial x}\right)
  +
  \frac{\partial}{\partial y}\left(k\frac{\partial T}{\partial y}\right)=0.
  \]
- For constant thermal conductivity, this reduces to Laplace’s equation:
  \[
  \frac{\partial^2T}{\partial x^2}
  +
  \frac{\partial^2T}{\partial y^2}=0.
  \]
- Boundary conditions are required to select a unique solution from the infinitely many functions satisfying Laplace’s equation.
- The three boundary-condition types discussed are:
  - Dirichlet: prescribed temperature.
  - Neumann: prescribed temperature gradient or heat flux.
  - Robin: a combination of temperature and heat flux.
- Separation of variables assumes a product-form solution:
  \[
  u(x,y)=X(x)Y(y).
  \]
- Substitution into Laplace’s equation converts one PDE into two ODEs.
- The resulting ODE forms depend on the sign of the separation constant \(\lambda\).
- Analytical PDE solutions are often difficult or unavailable for realistic geometries, but simple analytical cases are valuable for validating numerical methods.

### Deriving the steady two-dimensional heat equation

The lecture considers a thin rectangular plate with thickness \(\Delta z\). The front and back faces are insulated, so no heat crosses those faces. Consequently, the temperature is assumed to vary only in the \(x\) and \(y\) directions.

Consider a small rectangular differential element with dimensions:

- \(\Delta x\) in the \(x\)-direction.
- \(\Delta y\) in the \(y\)-direction.
- \(\Delta z\) through the thickness.

Heat enters and leaves through the four faces normal to the \(x\)- and \(y\)-directions.

For the \(x\)-direction:

- Heat enters through the left face with heat-flux component \(q_x(x)\).
- Heat leaves through the right face with heat-flux component \(q_x(x+\Delta x)\).
- The area of each \(x\)-normal face is \(\Delta y\,\Delta z\).

For the \(y\)-direction:

- Heat enters through the lower face with heat-flux component \(q_y(y)\).
- Heat leaves through the upper face with heat-flux component \(q_y(y+\Delta y)\).
- The area of each \(y\)-normal face is \(\Delta x\,\Delta z\).

A heat flux has units of \(\mathrm{W/m^2}\), or equivalently \(\mathrm{J/(s\,m^2)}\). Multiplying heat flux by face area gives a rate of energy transfer in watts. Multiplying by a time interval \(\Delta t\) gives an amount of energy.

At steady state, with no internal heat generation or storage, the energy entering the element equals the energy leaving it. After cancelling the common factors and dividing by \(\Delta x\Delta y\Delta z\), the finite-difference balance becomes

\[
\frac{q_x(x)-q_x(x+\Delta x)}{\Delta x}
+
\frac{q_y(y)-q_y(y+\Delta y)}{\Delta y}
=0.
\]

Taking the limit as \(\Delta x,\Delta y\to 0\) gives

\[
-\frac{\partial q_x}{\partial x}
-\frac{\partial q_y}{\partial y}=0.
\]

Equivalently,

\[
\frac{\partial q_x}{\partial x}
+
\frac{\partial q_y}{\partial y}=0,
\]

provided the sign convention is written consistently. The transcript describes the expression using heat flux entering minus heat flux leaving, so the negative signs arise from that orientation.

### Fourier’s law

The heat-flux vector is related to the temperature gradient by Fourier’s law:

\[
\mathbf{q}=-k\nabla T.
\]

For a two-dimensional field,

\[
\nabla T
=
\frac{\partial T}{\partial x}\mathbf{i}
+
\frac{\partial T}{\partial y}\mathbf{j},
\]

so

\[
q_x=-k\frac{\partial T}{\partial x},
\qquad
q_y=-k\frac{\partial T}{\partial y}.
\]

Here:

- \(\mathbf{q}\) is the heat-flux vector.
- \(q_x\) and \(q_y\) are its Cartesian components.
- \(k\) is thermal conductivity.
- \(T\) is temperature.
- \(\mathbf{i}\) and \(\mathbf{j}\) are unit vectors in the \(x\)- and \(y\)-directions.

The thermal conductivity depends on the material. The lecturer contrasts materials such as steel and wood: steel generally conducts heat more rapidly than wood.

Substituting Fourier’s law into the conservation equation gives

\[
-\frac{\partial}{\partial x}
\left(-k\frac{\partial T}{\partial x}\right)
-
\frac{\partial}{\partial y}
\left(-k\frac{\partial T}{\partial y}\right)
=0,
\]

which simplifies to

\[
\frac{\partial}{\partial x}
\left(k\frac{\partial T}{\partial x}\right)
+
\frac{\partial}{\partial y}
\left(k\frac{\partial T}{\partial y}\right)
=0.
\]

For a uniform material with constant \(k\), the conductivity can be taken outside the derivatives and cancelled:

\[
\frac{\partial^2T}{\partial x^2}
+
\frac{\partial^2T}{\partial y^2}
=0.
\]

This is Laplace’s equation for the steady two-dimensional temperature field.

### Why the flux relation is needed

The conservation equation alone contains two unknown fields, \(q_x\) and \(q_y\), but only one equation. It is therefore underdetermined or not well posed in that form.

Fourier’s law supplies the constitutive relation between heat flux and temperature. After substituting it into the conservation equation, the problem has one dependent variable, \(T(x,y)\), rather than the two unknown heat-flux components.

### Boundary conditions

Laplace’s equation has infinitely many solutions. Boundary conditions are required to select a unique solution.

#### Dirichlet boundary condition

A Dirichlet boundary condition specifies the dependent variable itself, here the temperature:

\[
T(0,y)=f(y).
\]

The prescribed temperature may be constant or may vary along the boundary.

An example discussed is a melting interface fixed at \(0^\circ\mathrm{C}\). Additional heat supplied to the interface can be used in the phase change rather than raising the interface temperature, so the temperature remains fixed at the melting point.

#### Neumann boundary condition

A Neumann boundary condition specifies a derivative of the dependent variable, often expressed as a heat flux:

\[
q_x(0,y)=g(y).
\]

Using Fourier’s law, this can also be written as

\[
-k\frac{\partial T}{\partial x}(0,y)=g(y).
\]

Examples include:

- A prescribed heat flux from a blowtorch.
- A specified heat flux on a boundary.
- An insulated boundary.

For a fully insulated boundary, the normal heat flux is zero. In the relevant direction this may be written as

\[
q_x=0,
\]

or, for nonzero constant \(k\),

\[
\frac{\partial T}{\partial x}=0.
\]

The transcript refers to the front and back faces being insulated during the derivation.

#### Robin boundary condition

A Robin boundary condition combines temperature and its gradient or heat flux. The lecture gives a convective form:

\[
q_x=h(T-T_{\mathrm{ref}}),
\]

or, after substituting Fourier’s law,

\[
-k\frac{\partial T}{\partial x}
=
h(T-T_{\mathrm{ref}}).
\]

Here:

- \(h\) is the convective heat-transfer coefficient.
- \(T_{\mathrm{ref}}\) is a reference or surrounding temperature.
- \(T\) is the temperature at the boundary.

Physically, the heat flux depends on the temperature difference between the surface and its surroundings. The coefficient \(h\) determines how strongly the heat-transfer rate responds to that difference.

The lecturer describes Robin conditions as a combination of:

- Fixing the dependent variable, \(T\).
- Fixing the gradient or heat flux.

### Analytical solution methods

Analytical solutions for PDEs are generally uncommon and difficult, particularly for complex domains or boundary conditions. However, they are useful for validating numerical solutions.

Separation of variables can sometimes be applied when:

- The PDE is linear.
- The equation is homogeneous, with no source term.
- The domain has a simple geometry, such as a rectangle or square.
- The boundary conditions are compatible with separated solutions.

Simple analytical cases can be used to check a numerical model before applying it to more complicated geometries.

### Separation of variables

Starting with Laplace’s equation for a generic field \(u(x,y)\),

\[
\frac{\partial^2u}{\partial x^2}
+
\frac{\partial^2u}{\partial y^2}
=0,
\]

assume a product solution

\[
u(x,y)=X(x)Y(y),
\]

where:

- \(X\) depends only on \(x\).
- \(Y\) depends only on \(y\).

Because \(Y\) is constant with respect to \(x\),

\[
\frac{\partial^2u}{\partial x^2}
=
Y\frac{d^2X}{dx^2}.
\]

Similarly, because \(X\) is constant with respect to \(y\),

\[
\frac{\partial^2u}{\partial y^2}
=
X\frac{d^2Y}{dy^2}.
\]

Substitution gives

\[
Y\frac{d^2X}{dx^2}
+
X\frac{d^2Y}{dy^2}
=0.
\]

Dividing through by \(XY\), assuming \(X\) and \(Y\) are nonzero in the region of interest,

\[
\frac{1}{X}\frac{d^2X}{dx^2}
=
-\frac{1}{Y}\frac{d^2Y}{dy^2}.
\]

The left-hand side depends only on \(x\), while the right-hand side depends only on \(y\). For equality to hold for all \(x\) and \(y\), both sides must equal a constant, denoted \(\lambda\):

\[
\frac{1}{X}\frac{d^2X}{dx^2}=\lambda,
\qquad
-\frac{1}{Y}\frac{d^2Y}{dy^2}=\lambda.
\]

Therefore,

\[
\frac{d^2X}{dx^2}=\lambda X,
\]

and

\[
\frac{d^2Y}{dy^2}=-\lambda Y.
\]

The original PDE has been reduced to two ODEs.

### Cases based on the separation constant

#### Case 1: \(\lambda=0\)

The ODEs become

\[
\frac{d^2X}{dx^2}=0,
\qquad
\frac{d^2Y}{dy^2}=0.
\]

Integrating twice gives

\[
X(x)=Ax+B,
\]

\[
Y(y)=Cy+D.
\]

The corresponding product solution is

\[
u(x,y)=(Ax+B)(Cy+D).
\]

This is the linear-product solution associated with \(\lambda=0\).

#### Case 2: \(\lambda<0\)

Write

\[
\lambda=-\mu^2,
\]

where \(\mu\neq 0\) and \(\mu^2>0\). The ODEs become

\[
\frac{d^2X}{dx^2}=-\mu^2X,
\]

\[
\frac{d^2Y}{dy^2}=\mu^2Y.
\]

The general forms are

\[
X(x)=A\sin(\mu x)+B\cos(\mu x),
\]

and

\[
Y(y)=Ce^{\mu y}+De^{-\mu y}.
\]

The \(Y\)-solution may alternatively be expressed using hyperbolic functions:

\[
Y(y)=C_1\cosh(\mu y)+C_2\sinh(\mu y).
\]

The corresponding separated product contains trigonometric functions in \(x\) and exponential or hyperbolic functions in \(y\).

#### Case 3: \(\lambda>0\)

Write

\[
\lambda=\mu^2,
\]

where \(\mu^2>0\). The ODEs become

\[
\frac{d^2X}{dx^2}=\mu^2X,
\]

\[
\frac{d^2Y}{dy^2}=-\mu^2Y.
\]

The general forms are

\[
X(x)=Ae^{\mu x}+Be^{-\mu x},
\]

and

\[
Y(y)=C\sin(\mu y)+D\cos(\mu y).
\]

The corresponding separated product contains exponential functions in \(x\) and trigonometric functions in \(y\).

The lecture notes that the three separated solution types are all solutions of Laplace’s equation before boundary conditions are applied. Boundary conditions determine which type and which parameter values are admissible.

### Rectangular-domain example

The example considers a rectangular domain approximately described by

\[
0\leq x\leq 2,
\qquad
0\leq y\leq 1.
\]

There is one boundary condition on each of the four edges. The transcript indicates that three edges have zero displacement or temperature, while the remaining edge has a prescribed sine profile. The exact right-edge expression is not fully clear in the automated transcript.

The lecturer tests the three separated-solution families.

#### Testing the \(\lambda=0\) solution

The proposed solution is

\[
u(x,y)=(Ax+B)(Cy+D).
\]

Applying the zero condition at \(y=0\) gives

\[
(Ax+B)D=0
\]

for all \(x\). To avoid the entirely trivial solution, the lecturer sets

\[
D=0.
\]

Applying the zero condition at \(x=0\) then gives

\[
B(Cy+D)=0.
\]

With \(D=0\), this leads to

\[
B=0.
\]

The solution reduces to a multiple of \(xy\). Applying the zero condition at the upper boundary then forces the remaining product coefficient to vanish, resulting in

\[
u(x,y)=0.
\]

This is a trivial solution of Laplace’s equation, but it does not satisfy the nonzero sine-profile condition on the remaining boundary. Therefore, the \(\lambda=0\) family is rejected for this boundary-value problem.

#### Testing the trigonometric-in-\(x\), exponential-in-\(y\) solution

The second proposed family has the form

\[
u(x,y)
=
\left[A\sin(\mu x)+B\cos(\mu x)\right]
\left[Ce^{\mu y}+De^{-\mu y}\right].
\]

Applying the zero condition at \(y=0\) gives

\[
C+D=0,
\]

so

\[
D=-C.
\]

The \(y\)-dependent factor can therefore be written in the form

\[
C\left(e^{\mu y}-e^{-\mu y}\right).
\]

The constants can be regrouped into new coefficients, leaving a simplified expression involving

\[
\left[A\sin(\mu x)+B\cos(\mu x)\right]
\left(e^{\mu y}-e^{-\mu y}\right).
\]

Applying the zero condition at \(x=0\):

- \(\sin(0)=0\).
- \(\cos(0)=1\).

The expression therefore depends on the coefficient multiplying the cosine term. Since the exponential factor cannot generally vanish for \(\mu\neq 0\), the boundary condition requires

\[
B=0.
\]

Applying the zero condition at \(y=1\) then leads to a factor involving

\[
e^\mu-e^{-\mu}.
\]

For \(\mu\neq 0\), this factor is nonzero. Consequently, the remaining coefficient must also vanish, giving only the trivial solution. This family therefore cannot satisfy the full set of boundary conditions in a useful nontrivial way.

#### Testing the exponential-in-\(x\), trigonometric-in-\(y\) solution

The third proposed family has the form

\[
u(x,y)
=
\left[Ae^{\mu x}+Be^{-\mu x}\right]
\left[C\sin(\mu y)+D\cos(\mu y)\right].
\]

Applying the zero condition at \(y=0\):

- \(\sin(0)=0\).
- \(\cos(0)=1\).

This forces

\[
D=0.
\]

The solution becomes

\[
u(x,y)
=
\left[Ae^{\mu x}+Be^{-\mu x}\right]
C\sin(\mu y),
\]

with constants regrouped into new coefficients if desired.

Applying the zero condition at \(y=1\) gives a factor of

\[
\sin(\mu).
\]

For the boundary condition to hold for all \(x\), the lecturer concludes that

\[
\sin(\mu)=0.
\]

Thus the admissible values of \(\mu\) are integer multiples of \(\pi\):

\[
\mu=n\pi,
\qquad n\in\mathbb{Z},
\]

subject to the remaining boundary conditions and the nontriviality requirement.

The lecture ends before the right-edge boundary condition is fully applied and before the final coefficients are determined.

## Equations and worked patterns

### Lecture 17

The transcript refers to several governing equations but does not reproduce their full mathematical forms clearly. The following definitions are therefore limited to what can be established from the spoken content.

### Reynolds number

The Reynolds number is a dimensionless quantity used to characterise the relative importance of inertial and viscous effects in a flow.

The lecture used a value of approximately:

\[
Re \approx 30{,}000
\]

for the clay-cylinder crossflow example.

The lecturer connected Reynolds number with:

- Whether flow remains attached.
- Shear separation.
- Wake and vortex formation.
- The character of the flow field.

The exact definition and variable notation were not stated in this transcript.

### Navier–Stokes equations

The Navier–Stokes equations govern fluid motion. The lecture described using them to analyse fluid flow around evolving bodies such as clay cylinders and melting ice.

The transcript does not contain a legible full form of the equations.

### Continuity equation

The continuity equation expresses conservation of mass. It was mentioned alongside the Navier–Stokes equations.

The full equation and assumptions used in the lecture were not transcribed.

### Interface velocity

A velocity variable was introduced for the moving interface around the clay cylinder. This velocity describes how the fluid–solid boundary changes with time.

For melting ice, the interface velocity is related to the temperature gradient normal to the interface.

### Normal temperature gradient

The normal direction is perpendicular to the surface. The melting interface responds to the temperature gradient in this direction.

The transcript indicates that the interface motion depends on this normal gradient and on thermal/material properties including:

- Thermal conductivity.
- Density.
- Heat capacity.

The exact Stefan-type relation was not audible in the transcript.

### Lava-thickness PDE

The lava thickness was denoted by \(H\), with:

- \(H\) as the dependent variable.
- \(x\) and \(t\) as independent variables.

The model solves for the height or thickness profile:

\[
H = H(x,t)
\]

The full PDE was not transcribed. The described model represents lava spreading under gravity from an initial distribution.

### Viscosity relation for lava

The lecture described viscosity as a temperature-dependent function involving unknown parameters, including a coefficient and an exponential coefficient \(\alpha\).

The general structure can be stated only as:

\[
\mu = \mu(T;\text{unknown parameters})
\]

The exact functional form was not provided clearly enough by the transcript to reproduce accurately.

### Shallow-water or Saint-Venant equations

The tsunami model uses three nonlinear equations derived from the Navier–Stokes equations under a long-wave or shallow-water approximation.

The main unknowns include:

- Water height or free-surface elevation.
- Horizontal velocity components \(u\) and \(v\).

The approximation assumes that the vertical water-depth scale is much smaller than the horizontal length scale of the wave. The exact equations were not transcribed.

### Initial and boundary conditions

Boundary conditions specify the behaviour of the solution at the boundaries of the domain.

Initial conditions specify the state of a time-dependent problem at the starting time.

A unique solution generally requires sufficient boundary conditions. An unsteady problem additionally requires an initial condition.

### Lecture 18

- ∂u/∂x = lim(h→0) [u(x+h,y)−u(x,y)]/h; y is held fixed.
- ∂u/∂y = lim(h→0) [u(x,y+h)−u(x,y)]/h; x is held fixed.
- u_x = ∂u/∂x; u_xx = ∂²u/∂x²; u_xy is a mixed partial derivative.
- Two-dimensional Laplace equation: u_xx + u_yy = 0.
- Example check: u=x²−y² gives 2+(−2)=0.
- PDE order: largest derivative order appearing in the equation, not the number of independent variables.
- For linear L: homogeneous problem L[u]=0; nonhomogeneous problem L[u]=f with an independent nonzero source.

### Lecture 19

### Linearity

A PDE is linear with respect to \(u\) if \(u\) and its derivatives appear only to the first power and are not multiplied together or placed inside nonlinear functions.

Linear derivative term:

\[
u_{xx}.
\]

Nonlinear dependent-variable terms:

\[
u^2,\qquad u^3,\qquad uu_x.
\]

### General second-order classification

For a two-variable second-order PDE whose principal part is

\[
a u_{xx}+b u_{xy}+c u_{yy},
\]

define

\[
\Delta=b^2-4ac.
\]

Classification:

\[
\Delta<0
\quad\Rightarrow\quad
\text{elliptic},
\]

\[
\Delta=0
\quad\Rightarrow\quad
\text{parabolic},
\]

\[
\Delta>0
\quad\Rightarrow\quad
\text{hyperbolic}.
\]

The transcript referred to the general PDE as an equation numbered approximately “1.9.” The precise complete general form was not captured reliably.

### Laplace equation

\[
T_{xx}+T_{yy}=0.
\]

For this equation:

\[
a=1,\qquad b=0,\qquad c=1,
\]

so

\[
\Delta=-4<0.
\]

Therefore it is elliptic.

### Heat equation

\[
T_t=\kappa T_{xx}.
\]

Equivalent zero-right-hand-side form:

\[
\kappa T_{xx}-T_t=0.
\]

For classification:

\[
a=\kappa,\qquad b=0,\qquad c=0,
\]

so

\[
\Delta=0.
\]

Therefore it is parabolic.

### Wave equation

\[
u_{xx}=\frac{1}{c^2}u_{tt}.
\]

Equivalent form:

\[
u_{xx}-\frac{1}{c^2}u_{tt}=0.
\]

For classification:

\[
a=1,\qquad b=0,\qquad c=-\frac{1}{c^2},
\]

so

\[
\Delta=\frac{4}{c^2}>0.
\]

Therefore it is hyperbolic.

### Homogeneous equation

For

\[
\mathcal{L}[u]=g,
\]

the equation is homogeneous if

\[
g=0.
\]

### Poisson equation

A Laplace-type equation with a source term can be written as

\[
T_{xx}+T_{yy}=f(x,y).
\]

This is commonly called Poisson’s equation. It is non-homogeneous when \(f(x,y)\neq 0\).

### Superposition

If

\[
\mathcal{L}[T_1]=0
\]

and

\[
\mathcal{L}[T_2]=0,
\]

for a linear differential operator \(\mathcal{L}\), then

\[
\mathcal{L}[\alpha T_1+\beta T_2]=0
\]

for constants \(\alpha\) and \(\beta\).

### Example harmonic function

\[
T=x^3-3xy^2.
\]

Its second derivatives are

\[
T_{xx}=6x,\qquad T_{yy}=-6x,
\]

therefore

\[
T_{xx}+T_{yy}=0.
\]

### Lecture 20

### Heat flux and conservation

Heat flux:

\[
\mathbf{q}=
q_x\mathbf{i}+q_y\mathbf{j}
\]

Units:

\[
[\mathbf{q}]=\mathrm{W/m^2}.
\]

Steady two-dimensional conservation of energy without internal generation:

\[
\frac{\partial q_x}{\partial x}
+
\frac{\partial q_y}{\partial y}
=0.
\]

Equivalent divergence form:

\[
\nabla\cdot\mathbf{q}=0.
\]

### Fourier’s law

\[
\mathbf{q}=-k\nabla T.
\]

Components:

\[
q_x=-k\frac{\partial T}{\partial x},
\qquad
q_y=-k\frac{\partial T}{\partial y}.
\]

Temperature gradient:

\[
\nabla T
=
\frac{\partial T}{\partial x}\mathbf{i}
+
\frac{\partial T}{\partial y}\mathbf{j}.
\]

### General steady heat equation

For variable thermal conductivity:

\[
\frac{\partial}{\partial x}
\left(k\frac{\partial T}{\partial x}\right)
+
\frac{\partial}{\partial y}
\left(k\frac{\partial T}{\partial y}\right)
=0.
\]

For constant thermal conductivity:

\[
\frac{\partial^2T}{\partial x^2}
+
\frac{\partial^2T}{\partial y^2}
=0.
\]

This is Laplace’s equation.

### Boundary conditions

Dirichlet:

\[
T|_{\partial\Omega}=f.
\]

Neumann:

\[
\frac{\partial T}{\partial n}=g
\]

or, in heat-flux form,

\[
q_n=g.
\]

Insulated boundary:

\[
q_n=0.
\]

For constant nonzero \(k\), this is equivalent to

\[
\frac{\partial T}{\partial n}=0.
\]

Robin:

\[
q_n=h(T-T_{\mathrm{ref}})
\]

or, using Fourier’s law,

\[
-k\frac{\partial T}{\partial n}
=
h(T-T_{\mathrm{ref}}).
\]

### Separation of variables

Assumed solution:

\[
u(x,y)=X(x)Y(y).
\]

Substitution into Laplace’s equation:

\[
Y\frac{d^2X}{dx^2}
+
X\frac{d^2Y}{dy^2}
=0.
\]

After division by \(XY\):

\[
\frac{1}{X}\frac{d^2X}{dx^2}
=
-\frac{1}{Y}\frac{d^2Y}{dy^2}
=\lambda.
\]

Separated ODEs:

\[
\frac{d^2X}{dx^2}=\lambda X,
\qquad
\frac{d^2Y}{dy^2}=-\lambda Y.
\]

### Separated solution families

For \(\lambda=0\):

\[
X=Ax+B,
\qquad
Y=Cy+D.
\]

For \(\lambda=-\mu^2<0\):

\[
X=A\sin(\mu x)+B\cos(\mu x),
\]

\[
Y=Ce^{\mu y}+De^{-\mu y}.
\]

For \(\lambda=\mu^2>0\):

\[
X=Ae^{\mu x}+Be^{-\mu x},
\]

\[
Y=C\sin(\mu y)+D\cos(\mu y).
\]

Equivalent hyperbolic representation for exponential solutions:

\[
Ce^{\mu y}+De^{-\mu y}
=
C_1\cosh(\mu y)+C_2\sinh(\mu y).
\]

Quantisation condition arising from the lecture’s upper-boundary calculation:

\[
\sin(\mu)=0
\quad\Rightarrow\quad
\mu=n\pi,
\]

provided the remaining boundary conditions support this family.

## Warnings and deadlines

### Lecture 17 — historical source caveats

- This is a native Echo automated transcript with substantial recognition errors. Technical terms were sometimes transcribed incorrectly, including “CFT” for what is likely “CFD,” “Renal’s number” for Reynolds number, “thermal connectivity” for thermal conductivity, and “Saint Berne” for Saint-Venant.
- Several equations were referred to on slides but were not captured in readable form. Their exact algebraic expressions, coefficients, signs, and assumptions should be checked against the course reader or lecture slides.
- The viscosity equation for lava was not transcribed clearly enough to reproduce. Only its temperature dependence and unknown coefficient parameters can be stated confidently.
- The moving-interface equation for melting ice was described verbally but not captured fully. The precise normal-direction convention and thermal parameters should be confirmed from the course material.
- The transcript identifies the tsunami equations as shallow-water or Saint-Venant equations, but the exact notation and variable definitions are incomplete.
- The name of the researcher associated with Basilisk and shallow-water modelling is uncertain in the automated transcript. It appears to be Stéphane Popinet, but this should be verified independently.
- Some statements about the course schedule, assessment percentages, quiz timing, exam scope, and software may be administrative or subject to later updates. Confirm current details on the ENME302 course page.
- The lecturer stated that the final exam would cover the lecturer’s content rather than the first four weeks, but the exact assessment scope should be confirmed against official course information.
- The final section of the transcript contains mostly unintelligible background speech and has not been used to infer additional content.

### Lecture 18 — historical source caveats

Rebuilt on 20 October 2026 from the native transcript endpoint whose recording identity matches the 12 August Echo card and active player. Automated speech transcription remains imperfect; diagrams, package names and exact mathematical notation should be checked against the reader/overview slides. No wording has been reconstructed from imagined audio. Survey answers and post-lecture private conversations are intentionally omitted. These are source-backed study notes, not a full verbatim replacement for the recording.

### Lecture 19 — historical source caveats

- This document is based entirely on Hermes local ASR using faster-whisper tiny.en, not a native Echo360 transcript.
- The transcript itself warns that technical terms, equations, names, and Māori words require checking against the slides or audio.
- The complete general second-order PDE form was not captured clearly. The classification form
  \[
  au_{xx}+bu_{xy}+cu_{yy}
  \]
  is used because the lecture clearly identified \(a\), \(b\), and \(c\) as the coefficients needed for \(b^2-4ac\).
- Several ASR substitutions were obvious, including “rebels” for “variables,” “lip pick” for “elliptic,” “high-volic” for “hyperbolic,” and “past equation” for “Laplace equation.” These have been corrected only where the surrounding mathematics made the intended meaning clear.
- The notation \(c\) is potentially ambiguous because it was used both as the coefficient in the PDE classification and as the wave speed. The coefficient label and wave-speed symbol should be distinguished when consulting the original slides.
- The exact wave-speed relation involving tension and density was not reproduced because the ASR was unclear.
- The species-diffusion notation, including the concentration symbol and diffusion coefficient, should be checked against the original material.
- The exact name of the method associated with the equation \(u_x=0\) was not captured reliably.
- Some engineering examples and administrative statements near the end of the lecture were affected by poor ASR quality. Confirm current quiz dates, weighting, attempt rules, and AI restrictions using the official course information.
- No Māori words were confidently identified in the transcript.

### Lecture 20 — historical source caveats

- This is a native Echo automated transcript and contains substantial speech-recognition errors in mathematical notation, including confusion between \(x\), \(X\), \(y\), \(Y\), \(q\), \(k\), \(\mu\), and \(\lambda\).
- Some phrases such as “FOIA’s law” clearly refer to Fourier’s law.
- The transcript inconsistently describes signs while converting the finite-volume heat balance into differential form. The physically consistent conservation statement is \(\nabla\cdot\mathbf{q}=0\), with sign conventions determined by the chosen inward/outward face orientations.
- The lecture’s notation uses uppercase \(X\) and \(Y\) for separated functions, while lowercase \(x\) and \(y\) denote spatial coordinates. The transcript sometimes merges these visually.
- The right-edge boundary condition in the worked rectangle example is not transcribed clearly. It appears to be a prescribed sine profile, possibly involving a factor such as \(2\pi y\), but the exact expression should be checked against the lecture slides or the next lecture.
- The transcript appears to use \(u(x,y)\) as a generic displacement or field variable in the worked example, although the earlier derivation concerns temperature \(T(x,y)\).
- The final application of the right-edge boundary condition, the complete determination of coefficients, and the final closed-form solution are not included because the lecture ends before the example is completed.
- The statement that there are “four boundary conditions” for a second-order PDE is a practical description of prescribing data around the four edges of the rectangle; uniqueness depends on the compatibility and mathematical form of the complete boundary-value problem, not simply on counting conditions.

## Recall questions

1. Lecture 17: What finite-element cases had been covered earlier in ENME302 before the material introduced in this lecture?

2. Lecture 17: What distinguishes a Newtonian fluid from a non-Newtonian fluid?

3. Lecture 17: Why was toothpaste used as an example of viscoplastic behaviour?

4. Lecture 17: What effect does Reynolds number have on the flow around a cylinder?

5. Lecture 17: Why does a clay cylinder subjected to crossflow not necessarily erode uniformly?

6. Lecture 17: How does wall shear stress contribute to erosion?

7. Lecture 17: Why is the clay-cylinder example a fluid–solid coupling problem?

8. Lecture 17: How can a two-dimensional body produce three-dimensional flow structures downstream?

9. Lecture 17: Why does the melting rate of an ice body depend on the temperature gradient at the interface?

10. Lecture 17: What is meant by the normal component of interface velocity?

11. Lecture 17: Which thermal and material properties were identified as relevant to the melting-interface model?

12. Lecture 17: In the lava-flow example, what is the dependent variable and what are the independent variables?

13. Lecture 17: Why might a reduced lava-flow model be preferable to a full three-dimensional CFD model?

14. Lecture 17: Why can lava viscosity vary between volcanoes and over time at the same volcano?

15. Lecture 17: What makes lava-flow forecasting an inverse problem?

16. Lecture 17: What role do the unknown viscosity parameters play in matching a model to observations?

17. Lecture 17: What is the purpose of plotting model error over possible parameter values?

18. Lecture 17: What physical assumptions underlie a shallow-water or long-wave tsunami model?

19. Lecture 17: Why are the shallow-water equations computationally cheaper than the full Navier–Stokes equations?

20. Lecture 17: What are the main unknown quantities in the tsunami model described in the lecture?

21. Lecture 17: What is adaptive mesh refinement, and why is it useful for tsunami simulations?

22. Lecture 17: What criteria could be used to decide where a computational mesh should be refined?

23. Lecture 17: What are the three broad classifications of PDE discussed for the remainder of the course?

24. Lecture 17: Why are boundary conditions required for a unique PDE solution?

25. Lecture 17: Why is an initial condition required for an unsteady problem?

26. Lecture 17: What is the difference between spatial discretisation and solving the resulting algebraic system?

27. Lecture 17: What are accuracy, consistency, stability, and convergence in the context of numerical methods?

28. Lecture 17: What is the difference between verification and validation?

29. Lecture 17: Give an example of a verification test for a numerical model.

30. Lecture 17: Give an example of validating an HVAC model of the lecture room.

31. Lecture 17: What are the four broad engineering design approaches discussed in the lecture?

32. Lecture 17: When might established standards or guidelines be preferable to numerical simulation?

33. Lecture 17: When might physical experiments be impractical or impossible?

34. Lecture 17: Why are numerical models useful for parameter sweeps and parametric design?

35. Lecture 17: What are the main risks of treating commercial or open-source simulation software as a black box?

36. Lecture 17: Outline the complete workflow from defining a real engineering problem to validating a numerical model.

37. Lecture 17: In the lecture-room HVAC example, what geometry and physics could be simplified while retaining the dominant behaviour?

38. Lecture 17: Why can a verified model still fail to predict the real system accurately?

39. Lecture 18: A simulation agrees with an analytical benchmark but not measurements. What has been checked, and what remains questionable?

40. Lecture 18: When would reducing 3D to 2D be a valid simplification, and what assumption must be justified?

41. Lecture 18: Compare finite difference, element and volume methods without confusing mesh type with governing physics.

42. Lecture 18: Why can an O-grid be structured despite looking curved?

43. Lecture 18: Verify u=x²−y² against Laplace's equation, then explain why more information is needed to define a physical solution.

44. Lecture 18: Classify a PDE by order, linearity and homogeneity. Why is u·u_y nonlinear?

45. Lecture 18: Why is numerical agreement with an analytical solution a verification step rather than complete physical validation?

46. Lecture 19: Why is \(u_{xx}\) a linear term even though the derivative notation contains a square?

47. Lecture 19: Give two examples of nonlinear terms involving a dependent variable \(u\).

48. Lecture 19: For the principal part

49. Lecture 19: State the conditions on \(b^2-4ac\) for elliptic, parabolic, and hyperbolic equations.

50. Lecture 19: Classify the Laplace equation

51. Lecture 19: Why is the one-dimensional heat equation parabolic?

52. Lecture 19: Rewrite

53. Lecture 19: What is the physical meaning of the diffusion coefficient \(\kappa\) in the heat equation?

54. Lecture 19: What type of physical behaviour is associated with elliptic, parabolic, and hyperbolic PDEs?

55. Lecture 19: Why are boundary conditions especially important for an elliptic steady-state problem?

56. Lecture 19: For a one-dimensional heat equation that is first order in time and second order in space, how many initial and spatial boundary conditions are generally required?

57. Lecture 19: What does it mean for a PDE to be homogeneous?

58. Lecture 19: Why is a Poisson equation with a nonzero source term non-homogeneous?

59. Lecture 19: Show algebraically that if \(T_1\) and \(T_2\) satisfy Laplace’s equation, then \(\alpha T_1+\beta T_2\) also satisfies Laplace’s equation.

60. Lecture 19: Does the same homogeneous superposition argument apply unchanged when a nonzero source term is present? Explain.

61. Lecture 19: Verify whether

62. Lecture 19: What kind of transport process can be modelled by a diffusion equation for a concentration \(\phi\)?

63. Lecture 19: What does the wave speed \(c\) represent in the one-dimensional wave equation?

64. Lecture 19: Why can hyperbolic equations be challenging to solve numerically?

65. Lecture 19: Find the general type of function that satisfies

66. Lecture 19: Explain why understanding convergence and consistency is important when using numerical software or AI-generated code.

67. Lecture 19: According to the lecture, what is an appropriate and inappropriate use of AI in relation to the ENME302 quizzes?

68. Lecture 20: What physical conservation principle is used to derive the steady heat equation?

69. Lecture 20: Why can the temperature be treated as a function of only \(x\) and \(y\) in the thin-plate example?

70. Lecture 20: What are the dimensions of heat flux, and why must heat flux be multiplied by an area and a time interval to obtain an amount of energy?

71. Lecture 20: Starting from a differential energy balance, derive the two-dimensional steady conservation equation for \(q_x\) and \(q_y\).

72. Lecture 20: State Fourier’s law in vector and component form.

73. Lecture 20: What is the physical meaning of the negative sign in Fourier’s law?

74. Lecture 20: Why is the conservation equation alone insufficient to determine the temperature field?

75. Lecture 20: Derive Laplace’s equation from conservation of energy and Fourier’s law for constant thermal conductivity.

76. Lecture 20: How would the governing equation differ if thermal conductivity varied spatially?

77. Lecture 20: Distinguish between Dirichlet, Neumann, and Robin boundary conditions.

78. Lecture 20: Write a mathematical expression for a fully insulated boundary.

79. Lecture 20: Explain the physical meaning of

80. Lecture 20: Under what conditions is separation of variables likely to be useful for a PDE?

81. Lecture 20: Starting with \(u(x,y)=X(x)Y(y)\), derive the two ODEs obtained from Laplace’s equation.

82. Lecture 20: Why must the separated \(x\)- and \(y\)-dependent expressions equal a constant?

83. Lecture 20: What are the solution forms for \(X\) and \(Y\) when \(\lambda=0\)?

84. Lecture 20: For \(\lambda=-\mu^2\), which coordinate has trigonometric solutions and which has exponential or hyperbolic solutions?

85. Lecture 20: For \(\lambda=\mu^2\), which coordinate has exponential solutions and which has trigonometric solutions?

86. Lecture 20: Why do boundary conditions determine allowable values of \(\mu\)?

87. Lecture 20: In the rectangular example, why is the \(\lambda=0\) solution rejected?

88. Lecture 20: For the trigonometric-in-\(x\), exponential-in-\(y\) family, why does applying the condition at \(x=0\) eliminate the cosine coefficient?

89. Lecture 20: Why does the upper boundary condition lead to a condition involving \(\sin(\mu)\) for the exponential-in-\(x\), trigonometric-in-\(y\) family?

90. Lecture 20: Why are analytical solutions useful even when the ultimate engineering problem will be solved numerically?

91. Lecture 20: What part of the rectangular-domain example remains unfinished at the end of the lecture?

## Practice priorities

1. Tutor strategy for Lecture 17: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

2. Tutor strategy for Lecture 18: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

3. Tutor strategy for Lecture 19: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

4. Tutor strategy for Lecture 20: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

## Missing or incomplete

No missing source-backed lectures in this window. Equations/diagrams remain subject to the per-lecture caveats. The wrong duplicate transcript(s) have been replaced, not guessed from their titles.

## Source manifest

- Lecture 17 (echo-lecture-17-17): complete; summary `df2f7c87000f0e58f9efdb94f4ba26ae9d4da0617d1af3951756cc39277be865`; transcript `fc4ba008504f88530bbe5a13e36b3f93f4f3c622b028373b8d999225ee510f3d`; summary path `[local source path redacted]`
- Lecture 18 (echo-lecture-18-18): complete; summary `eec6b949f3b4bc5ade2a82d9f5b79eaa306e44ee45691b33fa54b16b4cb5f2ed`; transcript `b25b452c6a0484539dbf1388eaecc640fe83d73ccd7185d8515f923d8bc78cbc`; summary path `[local source path redacted]`
- Lecture 19 (echo-lecture-19-19): complete; summary `b75b9d8a07b0ddc0789bba31659608dd57dfca6f4c3a01348a7d68b2279e4a6a`; transcript `211bea4a8e6c20782c17081483b60239faecac9d7b9158533d8d9178d165cedb`; summary path `[local source path redacted]`
- Lecture 20 (echo-lecture-20-20): complete; summary `9d7a9599da73ee0da57fda0a7c9ba62eb2885e167964e71fa6f9f4d709e09562`; transcript `ce5240c7cc9f1d3ca3ada583444382cab0b9cccbf6e68707fa62ee83fee697c4`; summary path `[local source path redacted]`
