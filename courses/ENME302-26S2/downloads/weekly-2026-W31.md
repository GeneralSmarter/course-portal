<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-30T10:46:05.203994+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- 2026-W31 coverage: 2026-07-27T00:00:00+12:00 to 2026-07-30T10:45:03.767182+12:00.
- Lectures covered:
  - Lecture 9: Euler–Bernoulli beam-element formulation, degrees of freedom, weak form, and cubic interpolation.
  - Lecture 10: Beam stiffness matrix, cantilever verification, frame elements, transformations, and assembly checks.
  - Lecture 11: FEA motivation, determinate versus indeterminate structures, discretisation, shape functions, and the broader course framework.

## Main concepts

- A two-node Euler–Bernoulli beam element has four local degrees of freedom:
  - Transverse displacement and rotation at node 1.
  - Transverse displacement and rotation at node 2.
- Euler–Bernoulli theory assumes small deflections and rotations, slender geometry, and negligible shear deformation.
- Shear deformation becomes important for short or squat beams; Timoshenko beam elements are the stated extension for this case.
- Beam transverse displacement is interpolated using four cubic shape functions derived from four unit nodal displacement or rotation cases.
- The beam stiffness matrix is obtained from the second derivatives of the shape functions through virtual work.
- The unconstrained beam stiffness matrix is singular because rigid-body modes remain.
- Boundary conditions and connectivity are required before obtaining a unique structural solution.
- A frame element combines axial bar behaviour with beam bending behaviour through linear superposition.
- A two-dimensional frame element has six local degrees of freedom: two translations and one rotation at each node.
- Local element quantities must be transformed into global coordinates before structural assembly.
- Matrix dimensions alone do not verify correctness: local and global frame stiffness matrices can both be \(6\times6\) while representing different coordinate systems.
- FEA extends classical mechanics by discretising complex structures into elements and assembling their local equations into a global system.
- Statically indeterminate structures require compatibility and stiffness information in addition to equilibrium.
- Shape functions interpolate field quantities between discrete nodal values.

## Equations and worked patterns

- Beam displacement interpolation:
  \[
  v(x)=\mathbf{N}(x)\mathbf{D}
  \]
  with
  \[
  \mathbf{D}=[v_1,\theta_1,v_2,\theta_2]^T.
  \]

- Euler–Bernoulli moment–curvature relation:
  \[
  M=EI\frac{d^2v}{dx^2}
  \]
  with the sign dependent on the adopted convention.

- Beam stiffness component:
  \[
  K_{ij}=\int_0^L
  \left(\frac{d^2N_i}{dx^2}\right)^T
  EI
  \left(\frac{d^2N_j}{dx^2}\right)\,dx.
  \]

- For constant \(E\) and \(I\):
  \[
  K_{ij}=EI\int_0^L
  \frac{d^2N_i}{dx^2}
  \frac{d^2N_j}{dx^2}\,dx.
  \]

- Two-node beam-element stiffness matrix:
  \[
  K_E=\frac{EI}{L^3}
  \begin{bmatrix}
  12 & 6L & -12 & 6L\\
  6L & 4L^2 & -6L & 2L^2\\
  -12 & -6L & 12 & -6L\\
  6L & 2L^2 & -6L & 4L^2
  \end{bmatrix}.
  \]

- Example stiffness entry:
  \[
  K_{22}=\frac{4EI}{L}.
  \]

- Symmetry check:
  \[
  K_{ij}=K_{ji},\qquad K_E-K_E^T=0.
  \]

- Cantilever with a transverse tip load:
  \[
  \delta_{\text{tip}}=-\frac{PL^3}{3EI},
  \qquad
  \theta_{\text{tip}}=-\frac{PL^2}{2EI}.
  \]
  The signs depend on the course displacement and rotation conventions.

- Cantilever bending moment, measured from the fixed end:
  \[
  M(x)=-P(L-x)=-PL+Px.
  \]
  Therefore:
  \[
  M(0)=-PL,\qquad M(L)=0.
  \]

- Gravity-induced overturning moment for a laterally displaced mass:
  \[
  M_{\text{gravity}}=MgD_3.
  \]
  This effect may require an iterative update because the moment depends on the displacement being calculated.

- Frame-element equilibrium:
  \[
  F_E=K_ED
  \]
  where \(F_E\) and \(D\) are \(6\times1\), and \(K_E\) is \(6\times6\).

- Coordinate direction shorthand:
  \[
  C=\cos\alpha,\qquad S=\sin\alpha.
  \]

- Axial stress for an axial member:
  \[
  \sigma=\frac{N}{A}.
  \]

- Hollow circular tube geometry:
  \[
  D_i=D_o-2t,
  \qquad
  A=\frac{\pi}{4}(D_o^2-D_i^2).
  \]

- General FEA solution pattern:
  1. Divide the structure into elements.
  2. Define nodal degrees of freedom.
  3. Derive or select local element equations.
  4. Transform element quantities where required.
  5. Assemble the global system.
  6. Apply loads and boundary conditions.
  7. Solve for unknown nodal displacements and reactions.
  8. Recover element forces, strains, and stresses.

## Warnings and deadlines

- Check beam slenderness before applying Euler–Bernoulli theory. The lectures give an approximate length-to-cross-section guideline of \(5{:}1\) to \(10{:}1\) or greater.
- Do not assume shear deformation is negligible for short or squat beams.
- Do not solve the unconstrained beam stiffness matrix as though it were nonsingular; rigid-body modes must be restrained.
- Preserve the exact degree-of-freedom ordering used to derive the stiffness matrix.
- For frame elements, verify whether a matrix is expressed in local or global coordinates even when its dimensions are correct.
- The Lecture 11 summary mentions a provisional computer-based test date of 18 August and other assessment requirements. The schedule was stated to be provisional, so current information must be checked against the official course page.
- No other verified deadlines or warnings are provided in the supplied lecture summaries.

## Recall questions

1. What are the four local degrees of freedom of the two-node Euler–Bernoulli beam element?
2. Why does the beam interpolation use four shape functions?
3. What assumptions distinguish Euler–Bernoulli beam theory from a model that includes shear deformation?
4. Why is the unconstrained beam-element stiffness matrix singular?
5. How is the beam stiffness component \(K_{ij}\) obtained from the shape functions?
6. Why must the beam stiffness matrix be symmetric?
7. How do the beam-element cantilever results relate to the analytical tip displacement and rotation?
8. How is a six-degree-of-freedom frame element constructed from axial and flexural behaviour?
9. Why can using the wrong \(6\times6\) frame matrix produce a physically incorrect result without a Python dimension error?
10. Why do statically indeterminate structures require relative stiffness and compatibility information in addition to equilibrium?

## Practice priorities

- Re-derive the beam stiffness matrix from the second derivatives of the cubic shape functions, paying particular attention to degree-of-freedom ordering and signs.
- Verify matrix symmetry and identify the rigid-body modes of the unconstrained beam matrix.
- Reduce the beam stiffness system for a fixed-free cantilever and reproduce the tip displacement and rotation relationships.
- Practise distinguishing axial truss, beam, and frame element degrees of freedom.
- Work through local-to-global transformation logic for frame elements at non-zero orientations.
- Build a complete FEA workflow from local element equations through global assembly, boundary conditions, solution, and recovery of element forces.
- Review when Euler–Bernoulli theory is appropriate and when shear deformation requires a Timoshenko formulation.
- Connect classical bending-moment diagrams to finite-element interpolation and stiffness formulations.
- Review statically determinate versus indeterminate structures, focusing on why stiffness controls load sharing in the indeterminate case.
- Practise implementation checks that detect transposition, sign, numbering, coordinate-system, and matrix-entry errors.

## Missing or incomplete

- None.

## Source manifest

- Lecture 9 (echo-lecture-9-9): complete; summary `1e662d43de9e25ff51ec7f8e102f8b1a68ca85692c4feed1690d32778b2421e4`; transcript `81778e30d402b2b4cdde588f61d06ab037b24a16a59c6bff2a1206d68a4cc171`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_09_summary.md`
- Lecture 10 (echo-lecture-10-10): complete; summary `066dd373548f8543925b0c0f0b63898943ee78bc0b42d82169ef70199baa28c6`; transcript `6d30a9e5c8c05b34b58b042b84d2bbad87bb609aee7735536695a67784b7a967`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_10_summary.md`
- Lecture 11 (echo-lecture-11-11): complete; summary `6dbbf8c7d90a49048c92b917bf832c4a6e8c97e8394336c3b16135bd09982abe`; transcript `431c162d0ac2fe965d54ff2b4ea671ae168d1c6dceea78a3304be709f0ca8fb8`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_11_summary.md`
