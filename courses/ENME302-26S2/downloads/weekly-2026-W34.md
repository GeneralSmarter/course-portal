<!-- week-id: 2026-W34 -->
<!-- generated-at: 2026-08-23T06:16:52.651029+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Lecture 21: Laplace’s equation, separation of variables, finite and semi-infinite rectangular domains, Fourier sine series, analytical-solution checking, and numerical plotting.
- Lecture 22: Fourier-series convergence, Quiz 1 guidance, COMSOL finite-element workflow, boundary conditions, meshes, Laplace-equation heat-transfer modelling, and heat flux.
- Lecture 23: Seven-element welded-frame assignment, stress and wind-loading calculations, Euler–Bernoulli versus Timoshenko elements, geometry simplification, and mesh generation.
- Lecture 24: Structured and unstructured meshes, mesh quality and convergence, grid-generation methods, finite-difference discretisation, and the axially loaded elastic rod.
- Source coverage is complete for the specified week. No lectures were identified as missing or incomplete.

## Main concepts

- Laplace’s equation describes a harmonic scalar field:
  \[
  \nabla^2 u=0
  \]
  Separation of variables produces solutions whose form must be selected according to domain geometry and boundary conditions.
- Homogeneous boundary conditions are useful because they eliminate coefficients and restrict separation constants to discrete eigenvalues such as \(n\pi\).
- A constant boundary value generally requires a Fourier sine-series superposition rather than a single separated mode. For the constant function on the unit interval, only odd modes have non-zero coefficients.
- Truncated Fourier series improve as more terms are included but may show oscillatory behaviour near the ends of the interval.
- A finite-element workflow consists broadly of pre-processing, solving, and post-processing:
  - Define geometry, materials, physics, boundary conditions, and mesh.
  - Assemble and solve the algebraic system.
  - Visualise and interpret fields and derived quantities.
- Boundary conditions are required to close a PDE problem. Dirichlet conditions prescribe the dependent variable, Neumann conditions prescribe a derivative or flux, and Robin conditions combine the variable and its derivative or flux.
- For heat transfer, Fourier’s law is:
  \[
  \mathbf q=-k\nabla T
  \]
  The negative sign makes heat flux point from hotter regions towards colder regions.
- Structured meshes provide simple indexing and low connectivity-storage requirements, but they are difficult to fit to complex geometries. Unstructured meshes fit arbitrary geometries more easily but require more complex connectivity handling.
- Mesh refinement should target regions with steep gradients, stress concentrations, or boundary layers. Mesh convergence is assessed by monitoring a quantity of interest as the mesh is refined.
- Accuracy can be improved through h-refinement, which reduces element size, or p-refinement, which increases interpolation order.
- Total numerical error involves both discretisation error and round-off error. A finer mesh does not automatically minimise total error.
- In the frame assignment, the model uses seven 2D frame elements, rigid welded connections, fixed supports, and a circular hollow-section member.
- The assignment’s simplified stress calculation combines the absolute axial and bending normal stresses while neglecting shear stress:
  \[
  \sigma_{\text{total}}
  =
  |\sigma_{\text{axial}}|
  +
  |\sigma_{\text{bending}}|
  \]
- Wind pressure varies with the square of wind speed. The Timoshenko formulation includes shear deformation and generally predicts larger deflections than Euler–Bernoulli elements.
- In a finite-difference method, derivatives are replaced by algebraic approximations at grid nodes. The second-order central-difference approximation produces an algebraic equation for each interior node.
- Geometry should be simplified only where removed details do not materially affect the physics. Removing important fillets or other stress-controlling features can create artificial stress concentrations.

## Equations and worked patterns

- Two-dimensional Laplace equation:
  \[
  \frac{\partial^2u}{\partial x^2}
  +
  \frac{\partial^2u}{\partial y^2}
  =0
  \]

- Separated solution structure:
  \[
  u(x,y)=X(x)Y(y)
  \]

- Discrete eigenvalues from zero sine boundaries:
  \[
  \sin(\mu)=0
  \quad\Rightarrow\quad
  \mu=n\pi,\qquad n=1,2,3,\ldots
  \]

- For a semi-infinite domain with zero values at \(y=0\) and \(y=1\), prescribed value \(u(0,y)=1\), and \(u\to0\) as \(x\to\infty\):
  \[
  u(x,y)
  =
  \sum_{n=1}^{\infty}
  C_n e^{-n\pi x}\sin(n\pi y)
  \]
  with
  \[
  C_n=
  \begin{cases}
  \dfrac{4}{n\pi}, & n\text{ odd}\\[4pt]
  0, & n\text{ even}
  \end{cases}
  \]
  The growing exponential is discarded because it violates the far-field decay condition.

- Fourier sine-series coefficients on \(0\le x\le L\):
  \[
  b_n=
  \frac{2}{L}
  \int_0^L
  f(x)\sin\left(\frac{n\pi x}{L}\right)\,dx
  \]

- For \(f(x)=1\) on \(0\le x\le L\):
  \[
  b_n=
  \frac{2}{n\pi}\left(1-(-1)^n\right)
  \]
  Hence:
  \[
  1=
  \frac{4}{\pi}
  \sum_{\substack{n=1\\n\ \mathrm{odd}}}^{\infty}
  \frac{1}{n}
  \sin\left(\frac{n\pi x}{L}\right)
  \]

- Finite rectangular-domain pattern for a right boundary proportional to \(\sin(2\pi y)\):
  \[
  u(x,y)
  =
  a\,
  \frac{\sinh(2\pi x)}{\sinh(4\pi)}
  \sin(2\pi y)
  \]
  This uses the domain and boundary interpretation recorded in Lecture 21; the source notes that the exact normalisation should be checked against official course material if required for assessment.

- Heat flux:
  \[
  \mathbf q=-k\nabla T
  \]
  A zero-gradient Neumann condition represents zero heat flux and an insulating boundary.

- Circular hollow-section area:
  \[
  A=
  \frac{\pi}{4}
  \left(D_o^2-D_i^2\right)
  \]
  with \(D_o=100\ \mathrm{mm}\), \(D_i=90\ \mathrm{mm}\).

- Outer-fibre distance:
  \[
  c=\frac{D_o}{2}=50\ \mathrm{mm}
  \]

- Axial and bending stresses:
  \[
  \sigma_{\text{axial}}=\frac{N}{A},
  \qquad
  \sigma_{\text{bending}}=\frac{Mc}{I}
  \]

- Point-load moment pattern:
  \[
  M=Fd
  \]
  For the example values \(F=2000\ \mathrm N\) and \(d=0.5\ \mathrm m\):
  \[
  M=1000\ \mathrm{N\,m}
  \]

- Wind pressure:
  \[
  p=0.6v^2
  \]
  The assignment gives a yield stress of \(350\ \mathrm{MPa}\) and a factor of safety of \(2.5\), giving:
  \[
  \sigma_{\text{allow}}
  =
  \frac{350}{2.5}
  =
  140\ \mathrm{MPa}
  \]

- Timoshenko shear-deformation factor:
  \[
  \frac{12EI}{GA_sL^2}
  \]
  The stated effective shear-area relation is:
  \[
  A_s=\frac{2A}{\pi}\approx0.64A
  \]

- Axially loaded rod:
  \[
  \frac{d}{dx}
  \left(
  AE\frac{du}{dx}
  \right)=0
  \]
  For constant \(A\) and \(E\):
  \[
  \frac{d^2u}{dx^2}=0
  \]
  with the recorded boundary conditions:
  \[
  u(0)=0,
  \qquad
  \left.AE\frac{du}{dx}\right|_{x=L}
  =
  F_{\text{prescribed}}
  \]

- Second-order central difference:
  \[
  \left.\frac{d^2u}{dx^2}\right|_i
  \approx
  \frac{u_{i+1}-2u_i+u_{i-1}}{\Delta x^2}
  +
  O(\Delta x^2)
  \]

- Discretised constant-\(A\), constant-\(E\) rod equation:
  \[
  AE
  \frac{u_{i+1}-2u_i+u_{i-1}}{\Delta x^2}
  =0
  \]
  Boundary-condition incorporation into the algebraic system was deferred to a later lecture.

## Warnings and deadlines

- Lecture 21 stated that the upcoming test would run from 6:30 pm to 8:30 pm, with 110 minutes for the assessment and approximately 10 minutes for code upload. The source does not explicitly identify the calendar date in the summary.
- Test preparation guidance included verifying the virtual environment, OneDrive synchronisation, Anaconda/Spider access, two-factor-authentication requirements, and backup copies of code before the test.
- The test would not require students to write out stiffness matrices unless intermediate working was specifically requested. Correct final answers were generally sufficient for full marks.
- Quiz 1 covers PDE classification, separation of variables, boundary-condition selection, structured and unstructured grids, numerical methods, and an introductory software question.
- Quiz 1 allows one attempt and is due at the end of Friday of the relevant week. Numerical answers require units and three significant figures where specified. Unit formatting and metric-prefix conversions were specifically highlighted as possible sources of marking errors.
- The frame-analysis assignment deadline was stated as 6:00 pm on Monday, 7 September, submitted digitally. The report and code are required; the report is the primary assessed output.
- The assignment report has a maximum length of eight pages excluding appendices. The source states that the report may be submitted individually or in pairs, subject to the stated authorship requirements.
- The assignment’s open-ended structural-modification component is approximately 10% of the assignment. The lecturer cautioned against spending excessive time trying to optimise it.
- Lecture summaries contain transcript-reconstruction caveats. In particular, exact frame geometry, load orientations, some software command names, the finite-grid-generation equations, and certain numerical conventions should be checked against official course material before assessment use.

## Recall questions

1. Why must the growing exponential be removed from a semi-infinite-domain solution when the field must decay as \(x\to\infty\)?
2. Why does the constant boundary condition \(u(0,y)=1\) require a Fourier sine-series superposition?
3. Why do the even Fourier coefficients vanish when representing the constant function on the interval used in the lectures?
4. What is the difference between Dirichlet, Neumann, and Robin boundary conditions?
5. Why does the negative sign appear in Fourier’s law, \(\mathbf q=-k\nabla T\)?
6. What are the main advantages and disadvantages of structured and unstructured meshes?
7. How should a mesh-convergence study be performed, and why is the change between successive meshes important?
8. What is the difference between Euler–Bernoulli and Timoshenko frame elements?
9. Why is the assignment’s simplified total normal stress calculated using the sum of the absolute axial and bending stresses?
10. How are the Taylor expansions about \(u_{i+1}\) and \(u_{i-1}\) combined to obtain the second-order central-difference approximation?

## Practice priorities

1. Derive the Fourier sine coefficients for a constant boundary value and explain why only odd modes remain.
2. Reconstruct the semi-infinite Laplace solution, including the decay condition, eigenvalue restriction, superposition, and coefficient pattern.
3. Practise checking an analytical solution against the PDE and every boundary condition.
4. Review finite-element modelling workflow and classify example boundaries as Dirichlet, Neumann, or Robin.
5. Explain structured versus unstructured meshes, O–H grids, mesh refinement, element quality, and convergence studies.
6. Practise the frame-assignment stress workflow:
   - Calculate cross-sectional properties.
   - Determine axial and bending stresses.
   - Combine them using the assignment’s simplified rule.
   - Identify the critical element and location.
7. Practise wind-loading calculations using \(p=0.6v^2\), the allowable stress of \(140\ \mathrm{MPa}\), and the assignment’s load and equilibrium checks.
8. Compare Euler–Bernoulli and Timoshenko implementations, focusing on the local stiffness matrix, shear deformation, deflections, rotations, and unchanged transformation/assembly steps.
9. Derive the central-difference formula from forward and backward Taylor expansions.
10. Practise assembling the interior finite-difference equation for the axially loaded rod, while noting that boundary-condition discretisation was not completed in Lecture 24.

## Missing or incomplete

- None. All four specified lecture summary files were available and read.

## Source manifest

- Lecture 21 (echo-lecture-21-21): complete; summary `98ad658c93618500819a21b5dcbe680fbdb235e19f9f5259cc8794e4ad6bc1f3`; transcript `086292bafc117577969ee94a9b8fb4d9e9480795611e498369c4cd8866c10e28`; summary path `[local source path redacted]`
- Lecture 22 (echo-lecture-22-22): complete; summary `57f6aa190bdf3a2489283d83cda6e46b499245a782a40cdf6aead9b2eb338ffc`; transcript `05225a27eaedd22be998155e74ed25875fe3b38e52d74f21b134cab689ae16ca`; summary path `[local source path redacted]`
- Lecture 23 (echo-lecture-23-23): complete; summary `118ba3cb1867a30555e65c1ed91a15020ee9453db82855f86758674a889c1210`; transcript `40950df341510389b1ab1d93fa722fe6668661250333f56712c8826c04892553`; summary path `[local source path redacted]`
- Lecture 24 (echo-lecture-24-24): complete; summary `d5ef6fb6b062e109e7ff5d2247deedf84d2c949bb739feb2ea6f6d594a289f4b`; transcript `e7abd837b20d0cb815fd56576ab177afd76ccbaa872efea6d697310c3b4edae3`; summary path `[local source path redacted]`
