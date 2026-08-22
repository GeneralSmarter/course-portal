<!-- week-id: 2026-W34 -->
<!-- generated-at: 2026-08-23T09:32:09.414738+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Covered Lectures 21–24, spanning separation of variables, Fourier sine series, COMSOL finite-element modelling, frame analysis, mesh generation, numerical error, and finite-difference discretisation.
- Lecture 21 continued Laplace-equation solutions for finite rectangular and semi-infinite domains, including numerical visualisation. [Lecture 21]
- Lecture 22 completed the Fourier-series material and introduced COMSOL workflows for a two-dimensional Laplace-equation heat-transfer model. [Lecture 22]
- Lecture 23 covered the finite-element frame-analysis assignment, Timoshenko elements, geometry construction, and mesh generation. [Lecture 23]
- Lecture 24 covered structured and unstructured meshes, mesh convergence and quality, grid-generation methods, and finite differences applied to an axially loaded rod. [Lecture 24]

## Main concepts

- Laplace’s equation describes a harmonic scalar field. Separation of variables produces admissible spatial modes determined by the domain geometry and boundary conditions.
- Homogeneous boundary conditions are useful because they eliminate coefficients or restrict the separation constant to discrete eigenvalues.
- In a semi-infinite domain, terms that grow as the coordinate tends to infinity must be discarded. A constant boundary condition generally requires a Fourier sine series and linear superposition rather than one separated mode.
- Truncated Fourier series approximate the target boundary condition. Increasing the number of terms improves convergence, although oscillatory behaviour can remain near boundaries or discontinuities.
- COMSOL uses a finite-element workflow: define parameters, geometry, materials, physics, boundary conditions, mesh, study and solver, then post-process the results.
- Dirichlet conditions prescribe the dependent variable; Neumann conditions prescribe a derivative or flux; Robin conditions combine the dependent variable with its derivative or flux.
- Heat flux follows the temperature gradient according to Fourier’s law and points from hotter regions towards colder regions.
- The frame-analysis assignment uses seven welded two-dimensional frame elements, fixed supports, a circular hollow-section member, reaction checks, stress calculations, wind loading, and comparison of Euler–Bernoulli and Timoshenko formulations.
- The Timoshenko formulation includes shear deformation and generally predicts larger deflections than Euler–Bernoulli, although individual local deflections may decrease because the force distribution changes.
- Geometry should be simplified enough to reduce computational cost while retaining features that influence stresses, boundary conditions, flow, heat transfer, or other relevant physics.
- Structured meshes have implicit, index-based connectivity and are efficient when the geometry permits them. Unstructured meshes fit complex geometries more easily but require more connectivity data.
- Mesh refinement reduces discretisation error but increases computational cost. Refinement should target strong gradients, stress concentrations, boundary layers, and the selected quantity of interest.
- Numerical accuracy depends on both discretisation error and round-off error. A finer mesh does not automatically minimise total error.
- Finite differences replace derivatives with algebraic approximations at grid nodes. The central-difference approximation for a second derivative is second-order accurate.

## Equations and worked patterns

- Two-dimensional Laplace equation:
  \[
  \nabla^2u
  =
  \frac{\partial^2u}{\partial x^2}
  +
  \frac{\partial^2u}{\partial y^2}
  =0
  \]

- Separated solution structure:
  \[
  u(x,y)=X(x)Y(y)
  \]

- Zero boundary conditions can produce:
  \[
  \sin(\mu)=0
  \quad\Rightarrow\quad
  \mu=n\pi,\qquad n=1,2,3,\ldots
  \]

- For a semi-infinite domain with zero conditions at \(y=0\) and \(y=1\), prescribed value \(u(0,y)=1\), and \(u\to0\) as \(x\to\infty\):
  \[
  u(x,y)
  =
  \sum_{n=1}^{\infty}
  C_n e^{-n\pi x}\sin(n\pi y)
  \]
  where
  \[
  C_n=
  \begin{cases}
  \dfrac{4}{n\pi}, & n\text{ odd}\\[4pt]
  0, & n\text{ even}
  \end{cases}
  \]

- Fourier sine-series coefficients on \(0\le x\le L\):
  \[
  b_n
  =
  \frac{2}{L}
  \int_0^L
  f(x)\sin\left(\frac{n\pi x}{L}\right)\,dx
  \]

- Fourier’s law for heat flux:
  \[
  \mathbf q=-k\nabla T
  \]

- Simplified frame-analysis stress calculation:
  \[
  \sigma_{\text{total}}
  =
  |\sigma_{\text{axial}}|
  +
  |\sigma_{\text{bending}}|
  \]

- Axial and bending normal stresses:
  \[
  \sigma_{\text{axial}}=\frac{N}{A},
  \qquad
  \sigma_{\text{bending}}=\frac{Mc}{I}
  \]

- Moment from a point load:
  \[
  M=Fd
  \]
  The lecture example used \(F=2000\,\mathrm N\) and \(d=0.5\,\mathrm m\), giving approximately \(1000\,\mathrm{N\,m}\). The associated load orientations and signs must be taken from the assignment diagram.

- Wind pressure:
  \[
  p=0.6v^2
  \]
  with \(p\) in pascals and \(v\) in metres per second.

- Allowable stress for the assignment:
  \[
  \sigma_{\text{allow}}
  =
  \frac{\sigma_y}{2.5}
  =
  \frac{350\,\mathrm{MPa}}{2.5}
  =
  140\,\mathrm{MPa}
  \]

- Timoshenko shear-deformation parameter:
  \[
  \frac{12EI}{GA_sL^2}
  \]

- Second-order central difference:
  \[
  \left.\frac{d^2u}{dx^2}\right|_i
  \approx
  \frac{u_{i+1}-2u_i+u_{i-1}}{\Delta x^2}
  +
  O(\Delta x^2)
  \]

- For the constant-\(A\), constant-\(E\) elastic rod, the interior finite-difference equation is:
  \[
  AE
  \frac{u_{i+1}-2u_i+u_{i-1}}{\Delta x^2}
  =0
  \]
  Boundary-condition discretisation was deferred to a later lecture.

## Warnings and deadlines

- Lecture 21 gave test-environment guidance: the test was scheduled for the following evening from 6:30 pm to 8:30 pm, with 110 minutes for the assessment and approximately 10 minutes for uploading code to Learn. Students were advised to test the virtual environment, use student OneDrive, prepare code skeletons, keep backups, and arrive early. [Lecture 21]
- The test environment could require two-factor authentication, and USB storage and non-whitelisted cloud services would not be available. [Lecture 21]
- Stiffness matrices were not required to be written out in the test unless specifically requested. Correct final answers were generally sufficient, but intermediate working could support partial credit. [Lecture 21]
- Quiz 1 covers PDE classification, separation of variables, boundary-condition selection, structured and unstructured grids, numerical methods, and an introductory software question. It allows one attempt and is due at the end of Friday of the relevant week. Numerical answers require units and three significant figures where specified. [Lecture 22]
- Check unit formatting carefully in quiz answers, particularly milli- and kilo-prefixes. Incorrect unit entry may cause an otherwise correct numerical result to be marked wrong. [Lecture 22]
- The frame-analysis assignment report and code were stated to be due digitally at 6:00 p.m. on Monday, 7 September. The report maximum is eight pages excluding appendices. [Lecture 23]
- The assignment requires interpretation of numerical results, not numerical tables alone. The open-ended structural-modification component is approximately 10% of the assignment, so excessive optimisation effort was discouraged. [Lecture 23]
- The simplified assignment stress calculation intentionally neglects shear stress. Do not treat it as a complete combined-stress or von Mises analysis. [Lecture 23]
- The exact finite-domain Laplace-example normalisation and some assignment degree-of-freedom numbering should be checked against the course materials before assessment use. [Lecture 21; Lecture 23]
- Mesh convergence should be assessed using changes between successive meshes and then validated against analytical or experimental expectations where possible. [Lecture 24]

## Recall questions

1. Why does the condition \(u\to0\) as \(x\to\infty\) eliminate the growing exponential term in a separated solution?
2. Why is a Fourier sine series required to represent the constant boundary value \(u(0,y)=1\)?
3. Why are the even Fourier sine coefficients zero for the constant function on the interval used in the lectures?
4. What is the difference between Dirichlet, Neumann, and Robin boundary conditions?
5. What does the negative sign in \(\mathbf q=-k\nabla T\) indicate about heat-flux direction?
6. Why can a Timoshenko frame element generally produce larger deflections than an Euler–Bernoulli element?
7. What should be checked when simplifying geometry before creating a mesh?
8. What are the principal advantages and disadvantages of structured and unstructured meshes?
9. What is the difference between h-refinement and p-refinement?
10. Why is the second-order central-difference approximation called second-order accurate?

## Practice priorities

1. Derive the semi-infinite Laplace solution from the boundary conditions, including the removal of the growing exponential and determination of the Fourier coefficients.
2. Practise checking an analytical solution by substitution into Laplace’s equation and every boundary condition.
3. Reproduce the finite-element modelling workflow in COMSOL: parameters, geometry, physics, boundary conditions, mesh, stationary study, solve, and post-processing.
4. Review structured versus unstructured meshes, O–H grids, geometry partitioning, advancing-front generation, and Delaunay triangulation.
5. Perform a mesh-convergence study using a clearly defined quantity of interest, recording changes between successive mesh resolutions.
6. Review frame-assignment calculations: reaction equilibrium, axial stress, bending stress, maximum total normal stress, wind-pressure scaling, and allowable stress.
7. Modify the local frame-element stiffness matrix for Timoshenko behaviour while keeping the transformation and global assembly procedures unchanged.
8. Derive the central-difference approximation from Taylor expansions and apply it to the interior nodes of the elastic-rod equation.
9. Practise dimensional checking and unit entry for numerical quiz answers.
10. Prepare concise assignment reporting: method, results, interpretation, comparison of modelling methods, design implications, and conclusions.

## Missing or incomplete

- No lectures were identified as missing or incomplete for the requested 2026-W34 coverage.

## Source manifest

- Lecture 21 (echo-lecture-21-21): complete; summary `98ad658c93618500819a21b5dcbe680fbdb235e19f9f5259cc8794e4ad6bc1f3`; transcript `086292bafc117577969ee94a9b8fb4d9e9480795611e498369c4cd8866c10e28`; summary path `[local source path redacted]`
- Lecture 22 (echo-lecture-22-22): complete; summary `57f6aa190bdf3a2489283d83cda6e46b499245a782a40cdf6aead9b2eb338ffc`; transcript `05225a27eaedd22be998155e74ed25875fe3b38e52d74f21b134cab689ae16ca`; summary path `[local source path redacted]`
- Lecture 23 (echo-lecture-23-23): complete; summary `118ba3cb1867a30555e65c1ed91a15020ee9453db82855f86758674a889c1210`; transcript `40950df341510389b1ab1d93fa722fe6668661250333f56712c8826c04892553`; summary path `[local source path redacted]`
- Lecture 24 (echo-lecture-24-24): complete; summary `d5ef6fb6b062e109e7ff5d2247deedf84d2c949bb739feb2ea6f6d594a289f4b`; transcript `e7abd837b20d0cb815fd56576ab177afd76ccbaa872efea6d697310c3b4edae3`; summary path `[local source path redacted]`
