<!-- week-id: 2026-W37 -->
<!-- generated-at: 2026-09-15T15:19:45.817146+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

Week 2026-W37 covered Lectures 25–28, focusing on analytical and numerical solutions of ordinary and partial differential equations.

Topics included:

- Classification of PDEs and separation of variables for Laplace problems. [Lecture 25]
- Finite-difference discretisation, ghost nodes, matrix assembly, and verification against analytical solutions. [Lectures 25–26]
- Finite-difference accuracy, truncation error, mesh convergence, and two-dimensional Laplace problems. [Lecture 26]
- Structured and unstructured finite-element meshes, Gauss–Seidel/Liebmann iteration, relaxation, heat flux, and non-uniform grids. [Lecture 27]
- Mixed Dirichlet and Neumann boundary conditions, COMSOL comparisons, constraint groups, solution datasets, and insulated heated-plate problems. [Lecture 28]
- Chapter 5, the heat equation, was introduced as the topic for the following week. [Lecture 28]

## Main concepts

- An ODE uses ordinary or total derivatives; a PDE uses partial derivatives. The order of a PDE is its highest derivative order. [Lecture 25]
- For a second-order PDE, the discriminant is:
  
  \[
  \Delta=B^2-4AC
  \]
  
  Negative, zero, and positive values correspond to elliptic, parabolic, and hyperbolic equations respectively. [Lecture 25]
- Separation of variables converts a PDE into separate ODEs. Boundary conditions then determine the allowable modes and constants. [Lecture 25]
- Dirichlet conditions prescribe the dependent variable directly. Neumann conditions prescribe a derivative or normal flux. [Lectures 25, 27–28]
- Numerical solutions require verification against analytical, benchmark, or known solutions. Validation or comparison with experimental data tests whether the model adequately represents the physical system. [Lecture 25]
- Mesh convergence tests whether the numerical result is sufficiently independent of mesh resolution. Disagreement may instead indicate inadequate mesh resolution, incorrect physics, boundary conditions, governing equations, or implementation. [Lecture 25]
- Structured meshes have organised connectivity; unstructured meshes do not. Mesh type and refinement should be assessed for the particular geometry and loading case rather than assumed to have a universally superior accuracy. [Lectures 25, 27]
- Large discretised PDE systems are sparse. Iterative methods can avoid the storage and direct solution of a full dense matrix. [Lectures 26–27]
- Gauss–Seidel/Liebmann iteration updates values in place using the most recent available estimates. Diagonal dominance supports convergence of the method discussed. [Lecture 27]
- Over-relaxation can accelerate convergence, but an excessive relaxation factor can cause oscillation, instability, or slower convergence. [Lectures 27–28]
- Isotherms show constant-temperature contours. Fourier’s law indicates that heat flux points in the direction of decreasing temperature. [Lecture 27]
- Ghost nodes enable central-difference treatment of derivative boundary conditions where a physical neighbour is absent. [Lectures 25, 27–28]
- For prescribed boundary values, boundary nodes are not unknowns in the linear system. Neumann boundaries generally leave boundary-node values unknown while imposing their gradients. [Lectures 26, 28]

## Equations and worked patterns

- Analytical uniform-rod solution:
  
  \[
  AE\frac{d^2u}{dx^2}=0,\qquad
  AE\left.\frac{du}{dx}\right|_{x=L}=F_0,\qquad
  u(0)=0
  \]
  
  Integrating twice and applying the boundary conditions gives:
  
  \[
  u(x)=\frac{F_0}{AE}x
  \]
  
  This linear solution is an effective verification case because the second-order central difference reproduces its zero second derivative at grid points, apart from numerical precision. [Lecture 26]

- One-dimensional central differences:
  
  \[
  \frac{du}{dx}\bigg|_i\approx
  \frac{u_{i+1}-u_{i-1}}{2\Delta x},
  \qquad O(\Delta x^2)
  \]
  
  \[
  \frac{d^2u}{dx^2}\bigg|_i\approx
  \frac{u_{i-1}-2u_i+u_{i+1}}{\Delta x^2},
  \qquad O(\Delta x^2)
  \]
  
  [Lecture 26]

- Four-point asymmetric first derivative:
  
  \[
  \frac{du}{dx}\bigg|_i\approx
  \frac{-2u_{i-1}-3u_i+6u_{i+1}-u_{i+2}}{6\Delta x},
  \qquad O(\Delta x^3)
  \]
  
  It uses four points and is third-order accurate, but is not a central-difference stencil because it is asymmetric. [Lecture 26]

- Four-point fourth-order central first derivative:
  
  \[
  \frac{du}{dx}\bigg|_i\approx
  \frac{u_{i-2}-8u_{i-1}+8u_{i+1}-u_{i+2}}{12\Delta x},
  \qquad O(\Delta x^4)
  \]
  
  [Lecture 26]

- For an error relationship \(R\propto\Delta x^p\):
  
  \[
  \log R=p\log(\Delta x)+C
  \]
  
  Therefore, the slope of a log-log error plot gives the observed order of accuracy. The demonstrated second- and fourth-order schemes produced slopes of approximately 2 and 4. [Lecture 26]

- Two-dimensional Laplace equation:
  
  \[
  \frac{\partial^2T}{\partial x^2}
  +\frac{\partial^2T}{\partial y^2}=0
  \]
  
  On a uniform grid:
  
  \[
  T_{i+1,j}+T_{i-1,j}+T_{i,j+1}+T_{i,j-1}-4T_{i,j}=0
  \]
  
  or:
  
  \[
  T_{i,j}=
  \frac{T_{i+1,j}+T_{i-1,j}+T_{i,j+1}+T_{i,j-1}}{4}
  \]
  
  [Lectures 26–28]

- A \(5\times5\) nodal grid over a unit square has four intervals in each direction:
  
  \[
  h=\frac{1}{5-1}=0.25
  \]
  
  With all boundary values prescribed, there are \(3\times3=9\) interior unknowns. In the mixed-boundary example, three left-boundary nodes were also unknown, giving 12 unknowns and equations. [Lectures 26, 28]

- Gauss–Seidel/Liebmann iteration uses the latest available values immediately. A complete iteration updates all interior nodes once. The node-wise relative change was given as:
  
  \[
  \varepsilon_{i,j}=
  \left|
  \frac{T_{i,j,\mathrm{new}}-T_{i,j,\mathrm{old}}}
  {T_{i,j,\mathrm{new}}}
  \right|
  \]
  
  [Lecture 27]

- Over-relaxation update:
  
  \[
  T_{i,j,\mathrm{new}}
  =
  \lambda T_{i,j,\mathrm{new}^*}
  +(1-\lambda)T_{i,j,\mathrm{old}}
  \]
  
  with \(1<\lambda<2\) for over-relaxation and \(\lambda=1\) corresponding to ordinary Gauss–Seidel. [Lecture 27]

- Fourier’s law:
  
  \[
  \dot{\mathbf q}=-k\nabla T
  \]
  
  \[
  q_x=-k\frac{\partial T}{\partial x},
  \qquad
  q_y=-k\frac{\partial T}{\partial y}
  \]
  
  [Lecture 27]

- Ghost-node treatment for a left Neumann boundary:
  
  \[
  \frac{T_{2,j}-T_{0,j}}{2\Delta x}
  =
  \left.\frac{\partial T}{\partial x}\right|_{x=0}
  \]
  
  giving:
  
  \[
  T_{0,j}
  =
  T_{2,j}
  -2\Delta x
  \left.\frac{\partial T}{\partial x}\right|_{x=0}
  \]
  
  For an insulated boundary, the derivative is zero and \(T_{0,j}=T_{2,j}\). [Lecture 27]

- For both lower and left boundaries insulated, the modified stencils include doubled contributions from the neighbouring interior nodes. The lower-left corner equation was given as:
  
  \[
  2T_{i+1,j}+2T_{i,j+1}-4T_{i,j}=0
  \]
  
  [Lecture 28]

- Discretised systems are assembled in the form:
  
  \[
  A\mathbf U=\mathbf b
  \]
  
  and can be compared with finite-element results from COMSOL. The reported centre temperatures, approximately \(56.3^\circ\mathrm C\) from finite differences and \(56.1^\circ\mathrm C\) from COMSOL, indicated close agreement. [Lecture 28]

## Warnings and deadlines

- Quiz 2 included separation-of-variables practice, an elastic-rod coding question, and simulation-software questions involving a tapered cantilever and a clamp model. [Lecture 25]
- The lecture warned that quiz or Moodle-server overload near a deadline could cause timeouts or initially incorrect grading. No exact quiz deadline was given in the permitted sources. [Lecture 25]
- For the COMSOL quiz case, the lecturer stated that only one load case was required and that gravity should not be included in the intended answer. [Lecture 28]
- Numerical answers were described as requiring approximately 2% tolerance, with three significant figures sufficient. [Lecture 28]
- Check units carefully. Entering newtons where meganewtons were intended can create a factor-of-\(10^6\) error. [Lecture 28]
- Several source equations, node indices, units, and software terms were reconstructed from automated transcripts. Confirm ambiguous notation against the course reader before relying on it in a submission. [Lectures 25–28]
- The relative-error norm and some convergence details were not unambiguously defined in the source material. [Lecture 27]
- Do not treat the reported example temperature values or relaxation-factor iteration counts as universal results; they depend on the specific problem and implementation. [Lecture 27]

## Recall questions

1. How does an ODE differ from a PDE, and how is PDE order determined? [Lecture 25]
2. How does the sign of \(B^2-4AC\) classify a second-order PDE? [Lecture 25]
3. Why does the separation-of-variables solution for the rectangular Laplace problem contain a sine term in \(y\)? [Lecture 25]
4. Derive \(u(x)=F_0x/(AE)\) for the uniform axial rod using the two boundary conditions. [Lecture 26]
5. Why does the finite-difference solution reproduce the analytical rod solution at the grid points? [Lecture 26]
6. What does the slope of a log-log error-versus-grid-spacing plot represent? [Lecture 26]
7. Why does Gauss–Seidel use the most recent estimates, and how does this differ from a direct matrix solve? [Lecture 27]
8. What is the purpose of the relaxation factor \(\lambda\), and what can happen when it is chosen too close to 2? [Lecture 27]
9. State Fourier’s law and explain the physical meaning of its negative sign. [Lecture 27]
10. For a \(5\times5\) grid with mixed Dirichlet and Neumann boundaries, why are there 12 unknowns rather than 9? [Lecture 28]

## Practice priorities

1. Derive and verify the analytical uniform-rod solution, then explain how it validates a finite-difference implementation. [Lecture 26]
2. Memorise and apply the second- and fourth-order first-derivative stencils and the second-order second-derivative stencil. [Lecture 26]
3. Practise deriving the two-dimensional five-point Laplace stencil for both equal and unequal \(\Delta x,\Delta y\). [Lectures 26, 28]
4. Count nodes, intervals, boundary values, and unknowns carefully for \(5\times5\) grids. [Lectures 26, 28]
5. Work through ghost-node elimination for non-zero Neumann, insulated, and corner boundaries. [Lectures 27–28]
6. Implement or trace one complete Gauss–Seidel iteration using in-place updates. [Lecture 27]
7. Compare relaxation factors conceptually and interpret convergence using a specified error tolerance. [Lecture 27]
8. Use physical checks after solving: temperatures should respect boundary values, insulated boundaries should have zero normal gradient, and heat flux should point from hot to cold. [Lectures 27–28]
9. Review COMSOL workflows for constraint groups, copied solution datasets, cut lines, and derived maximum values. [Lecture 28]
10. Recheck units, boundary-condition selection, and whether gravity belongs in the specified load case before reproducing a simulation result. [Lecture 28]

## Missing or incomplete

None. All four lectures specified for 2026-W37 were covered by the provided summary files.

## Source manifest

- Lecture 25 (echo-lecture-25-25): complete; summary `3d7314cef69988b34610816f77fe12d5b4086e59ca687a750c0f758a49c8e763`; transcript `ac23a0133b66df935590c286b6b7d1a0a1cb20104560f0211dd44525aeb58fab`; summary path `[local source path redacted]`
- Lecture 26 (echo-lecture-26-26): complete; summary `ca4e1729e9581ffdc0e845aa6e17ace4ec8d5a2b9e661ad82b0283f5604b7317`; transcript `d8036a95bdaf6330814df8729afc70bb38a636cf922a51900493ca99768a16a4`; summary path `[local source path redacted]`
- Lecture 27 (echo-lecture-27-27): complete; summary `4059e587663d4962a1fbbbc0d93c0c1c751d24b1f3bae019505cedac3202f71a`; transcript `0a695665197d1b8f0fa86b3109072d75cad38812e15c69da7316c50a92884721`; summary path `[local source path redacted]`
- Lecture 28 (echo-lecture-28-28): complete; summary `abe272649f12cdfeb5e6117cfc1c905e7340babdbdf06524d8072c67bf89e32c`; transcript `b8240974f2055421d92317a4bcf5966cf92f5be3554f8deb2e6eb798ceec1449`; summary path `[local source path redacted]`
