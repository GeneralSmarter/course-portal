<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-30T10:40:46.027613+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Study period: 2026-07-27T00:00:00+12:00 to 2026-07-30T10:39:28.387769+12:00.
- Covered verified summaries:
  - Lecture 9: introduction to the two-node Euler–Bernoulli beam element and cubic interpolation.
  - Lecture 10: beam stiffness matrix, cantilever verification, and extension to two-dimensional frame elements.
  - Lecture 11: purpose of FEA, determinate versus indeterminate structures, discretisation, nodes, degrees of freedom, and shape functions.
- The lecture sequence developed the progression from axial bars to beam elements and then to combined axial-flexural frame elements.

## Main concepts

- A two-node Euler–Bernoulli beam element has four local degrees of freedom:
  - Transverse displacement and rotation at node 1.
  - Transverse displacement and rotation at node 2.
- Euler–Bernoulli theory assumes small deflections, small rotations, and negligible shear deformation. It is intended for slender beams, with an approximate length-to-cross-section guideline of 5–10 or greater.
- Short or squat beams may require a Timoshenko beam element because shear deformation becomes significant.
- The beam displacement field is interpolated using four cubic shape functions. Each shape function corresponds to one unit nodal displacement or rotation while the other nodal degrees of freedom are zero.
- The weak-form beam derivation requires integration by parts twice because the governing equation contains higher derivatives than the axial bar formulation.
- The beam stiffness matrix is constructed from the second derivatives of the shape functions and the flexural rigidity \(EI\).
- An unconstrained beam stiffness matrix is singular because rigid-body modes remain. Boundary conditions are required for a unique solution.
- The standard cantilever solution can be recovered from the beam-element formulation.
- A frame element combines axial bar behaviour with beam bending behaviour using linear superposition. Its six local degrees of freedom include axial displacement, transverse displacement, and rotation at each node.
- Local element matrices must be transformed into global coordinates before structural assembly. Correct matrix dimensions do not guarantee that the correct matrix or coordinate system has been used.
- Finite element analysis replaces a continuous structure with a mesh of simpler elements connected at nodes. Relative stiffness, compatibility, loading, and boundary conditions determine the solution for statically indeterminate structures.
- Shape functions interpolate quantities between nodal values and provide the basis for constructing element equations and assembling a global system.

## Equations and worked patterns

- Beam-element displacement interpolation:
  \[
  v(x)=\mathbf{N}(x)\mathbf{D}
  \]
  where
  \[
  \mathbf{D}=
  \begin{bmatrix}
  v_1\\
  \theta_1\\
  v_2\\
  \theta_2
  \end{bmatrix}.
  \]

- Beam slope and curvature:
  \[
  \theta(x)=\frac{dv}{dx},
  \qquad
  \kappa(x)=\frac{d^2v}{dx^2}.
  \]

- Moment–curvature relationship:
  \[
  M=EI\frac{d^2v}{dx^2}.
  \]
  The sign depends on the adopted moment and displacement conventions.

- The lecture summaries relate shear force and distributed load to higher derivatives of displacement:
  \[
  V\sim EI\frac{d^3v}{dx^3},
  \qquad
  w(x)\sim EI\frac{d^4v}{dx^4}.
  \]
  The exact signs should be checked against the course convention.

- For the initial shape-function derivation:
  \[
  w(x)=0.
  \]
  The four nodal displacement and slope conditions determine each cubic shape function.

- Beam stiffness component for constant \(E\) and \(I\):
  \[
  K_{ij}
  =
  EI\int_0^L
  \frac{d^2N_i}{dx^2}
  \frac{d^2N_j}{dx^2}\,dx.
  \]

- Standard Euler–Bernoulli beam stiffness matrix for the ordering \([D_1,D_2,D_3,D_4]^T\):
  \[
  K_E=\frac{EI}{L^3}
  \begin{bmatrix}
  12 & 6L & -12 & 6L\\
  6L & 4L^2 & -6L & 2L^2\\
  -12 & -6L & 12 & -6L\\
  6L & 2L^2 & -6L & 4L^2
  \end{bmatrix}.
  \]

- Example matrix entry:
  \[
  K_{22}=\frac{4EI}{L}
  =\frac{EI}{L^3}(4L^2).
  \]

- Matrix verification:
  \[
  K_{ij}=K_{ji},
  \qquad
  K_E-K_E^T=0.
  \]

- Tip-loaded cantilever response:
  \[
  \delta_{\text{tip}}=-\frac{PL^3}{3EI},
  \qquad
  \theta_{\text{tip}}=-\frac{PL^2}{2EI}.
  \]
  The negative signs follow the stated convention for a downward load and clockwise tip rotation.

- Cantilever bending moment, with \(x\) measured from the fixed end:
  \[
  M(x)=-P(L-x)=-PL+Px.
  \]
  Therefore:
  \[
  M(0)=-PL,
  \qquad
  M(L)=0.
  \]

- Frame-element local degrees of freedom:
  \[
  [D_1,D_2,D_3,D_4,D_5,D_6]
  =
  [X_1,Y_1,Z_1,X_2,Y_2,Z_2].
  \]

- Frame-element equilibrium relationship:
  \[
  F_E=K_E D.
  \]

- Coordinate transformation quantities:
  \[
  C=\cos\alpha,
  \qquad
  S=\sin\alpha.
  \]
  The complete transformation matrix was not recoverable from the summary, so its entries should be taken from the official course material.

- Recommended implementation pattern:
  1. Define element degrees of freedom consistently with the derived matrix.
  2. Form the local element stiffness matrix.
  3. Transform it to global coordinates when required.
  4. Assemble the global stiffness matrix.
  5. Apply boundary conditions.
  6. Solve for unknown nodal displacements.
  7. Recover element displacements and forces.
  8. Check symmetry, rank, dimensions, coordinate systems, and physical signs.

## Warnings and deadlines

- The Euler–Bernoulli beam formulation should not be applied uncritically to short, squat beams because it neglects shear deformation.
- The approximate “less than 1% error” guideline for aspect ratios of roughly 5–10 or greater is not a universal guarantee.
- Signs in the beam equilibrium, shear-force, and end-force relationships are convention-dependent. Verify them against the official diagrams or notes.
- The final explicit forms of all four Lecture 9 shape functions were not reliably recoverable from the summary.
- The complete frame transformation matrix was discussed but not fully recoverable from the Lecture 10 summary.
- A \(6\times6\) matrix can be dimensionally valid while still being the wrong matrix or expressed in the wrong coordinate system. Check matrix meaning, not only dimensions.
- The displaced-lumped-mass example involves a gravity-induced overturning moment that depends on displacement. A more accurate solution requires iteration.
- Lecture 11 described a computer-based test in Week 6, an indicated test date of 18 August, assignments, quizzes, and a minimum final-exam mark. The schedule was explicitly described as provisional, so current dates and requirements must be checked against the official course page.
- Student-developed code was described as intended to be available for the computer-based test, subject to the course’s current rules.

## Recall questions

1. What are the four local degrees of freedom of the two-node Euler–Bernoulli beam element?
2. Why is Euler–Bernoulli theory unsuitable for short or squat beams?
3. Why are four cubic shape functions required for the basic beam element?
4. What boundary conditions define the shape function associated with a unit rotation at node 1?
5. Why is integration by parts performed twice in the beam weak-form derivation?
6. Why is the unconstrained beam stiffness matrix singular?
7. How can the symmetry of a beam stiffness matrix be checked computationally?
8. What cantilever tip-deflection and tip-rotation relationships should the beam formulation reproduce?
9. How is a six-degree-of-freedom frame element constructed from axial and flexural behaviour?
10. Why can using the wrong \(6\times6\) frame matrix fail without producing a programming dimension error?

## Practice priorities

- Re-derive the four beam shape functions from the cubic polynomial and the four nodal displacement/slope conditions.
- Reproduce the beam stiffness integral using the second derivatives of the shape functions.
- Verify the standard \(4\times4\) beam stiffness matrix, including symmetry and the \(K_{22}\) entry.
- Apply boundary conditions to a one-element cantilever and recover tip displacement and rotation.
- Practise identifying rigid-body modes and explaining why constraints are required before solving.
- Draw the distinction between bar, beam, and frame elements, including their degrees of freedom and load-carrying behaviour.
- Practise transforming a frame element from local to global coordinates using \(C=\cos\alpha\) and \(S=\sin\alpha\).
- Check element numbering, matrix dimensions, coordinate systems, and sign conventions before coding or assembling a structure.
- Explain how mesh refinement and shape functions allow a finite element model to approximate a continuous structure.
- Review statically indeterminate load sharing in terms of relative stiffness, compatibility, material properties, geometry, and boundary conditions.

## Missing or incomplete

- No lectures were identified as missing or incomplete for this week.
- Source limitations remain within the supplied summaries:
  - Lecture 9 does not reliably preserve every explicit shape-function expression or sign convention.
  - Lecture 10 does not fully provide the frame transformation matrix or the detailed algebra for the iterative displaced-mass example.
  - Lecture 11 does not derive the complete finite-element matrix formulation.

## Source manifest

- Lecture 9 (echo-lecture-9-9): complete; summary `1e662d43de9e25ff51ec7f8e102f8b1a68ca85692c4feed1690d32778b2421e4`; transcript `81778e30d402b2b4cdde588f61d06ab037b24a16a59c6bff2a1206d68a4cc171`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_09_summary.md`
- Lecture 10 (echo-lecture-10-10): complete; summary `066dd373548f8543925b0c0f0b63898943ee78bc0b42d82169ef70199baa28c6`; transcript `6d30a9e5c8c05b34b58b042b84d2bbad87bb609aee7735536695a67784b7a967`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_10_summary.md`
- Lecture 11 (echo-lecture-11-11): complete; summary `6dbbf8c7d90a49048c92b917bf832c4a6e8c97e8394336c3b16135bd09982abe`; transcript `431c162d0ac2fe965d54ff2b4ea671ae168d1c6dceea78a3304be709f0ca8fb8`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_11_summary.md`
