<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-31T18:58:47.313955+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Week: 2026-W31, from 2026-07-27T00:00:00+12:00 to 2026-07-31T18:57:33.094939+12:00.
- Sources covered:
  - Lecture 9: Euler–Bernoulli beam-element formulation and cubic shape functions.
  - Lecture 10: beam stiffness matrix, cantilever verification, and two-dimensional frame elements.
  - Lecture 11: purpose and scope of FEA, discretisation, stiffness, nodes, degrees of freedom, and classical beam analysis.
  - Lecture 12: frame equilibrium, load distribution, deformed shapes, assembly, reactions, and the consequences of suppressing degrees of freedom.
- All four expected lectures were covered. No missing or incomplete lectures were identified.

## Main concepts

- Finite element analysis represents a continuous structure using discrete elements, nodes, degrees of freedom, shape functions, and assembled global equations.
- A two-node Euler–Bernoulli beam element has four local degrees of freedom:
  - Transverse displacement and rotation at node 1.
  - Transverse displacement and rotation at node 2.
- Euler–Bernoulli theory assumes small deflections, linear elastic behaviour, and negligible shear deformation. It is intended for long, slender beams. A Timoshenko beam element is more suitable when shear deformation is significant.
- Beam displacement is interpolated from nodal values using four cubic shape functions:
  \[
  v(x)=\mathbf{N}(x)\mathbf{D}
  \]
- The beam stiffness matrix is derived from the second derivatives of the shape functions and is symmetric.
- The unconstrained beam stiffness matrix is singular because rigid-body modes remain until boundary conditions are applied.
- A frame element combines axial bar behaviour with beam bending behaviour. Its six local degrees of freedom are ordered as:
  \[
  [X_1,Y_1,Z_1,X_2,Y_2,Z_2]
  \]
- In the linear small-displacement frame formulation, axial and flexural effects appear in one matrix but are not inherently coupled.
- Local element quantities must be transformed into global coordinates before structural assembly.
- Degree-of-freedom numbering must match the stiffness-matrix derivation and element connectivity.
- Load distribution depends on effective stiffness, including material properties, geometry, end conditions, constraints, and available deformation modes.
- The principle “load follows stiffness” means that a stiffer load path generally attracts a greater share of the applied load.
- Nodal displacements and rotations determine the interpolated deformed shape between nodes.
- Every element and the assembled structure must satisfy force and moment equilibrium.
- Suppressing degrees of freedom can remove physically important load paths. In the portal-frame example, omitting vertical or axial deformation prevented the model from representing the tension–compression couple in the columns.

## Equations and worked patterns

- Beam moment–curvature relationship:
  \[
  M=EI\frac{d^2v}{dx^2}
  \]
  The sign depends on the adopted convention.

- Beam shear and distributed-load relationships:
  \[
  V\sim EI\frac{d^3v}{dx^3}
  \]
  \[
  w(x)\sim EI\frac{d^4v}{dx^4}
  \]
  The source summaries caution that the exact signs are convention-dependent.

- Beam nodal displacement and slope conditions:
  \[
  v(0)=D_1,\qquad \frac{dv}{dx}(0)=D_2
  \]
  \[
  v(L)=D_3,\qquad \frac{dv}{dx}(L)=D_4
  \]

- Initial shape-function derivation:
  \[
  w(x)=0
  \]
  Each shape function is obtained by applying one unit nodal displacement or rotation while setting the other three nodal degrees of freedom to zero.

- Beam stiffness component:
  \[
  K_{ij}
  =
  EI\int_0^L
  \frac{d^2N_i}{dx^2}
  \frac{d^2N_j}{dx^2}\,dx
  \]
  for constant \(E\) and \(I\).

- Standard two-node beam stiffness matrix for the ordering \([D_1,D_2,D_3,D_4]^T\):
  \[
  K_E=\frac{EI}{L^3}
  \begin{bmatrix}
  12 & 6L & -12 & 6L\\
  6L & 4L^2 & -6L & 2L^2\\
  -12 & -6L & 12 & -6L\\
  6L & 2L^2 & -6L & 4L^2
  \end{bmatrix}
  \]

- Symmetry check:
  \[
  K_{ij}=K_{ji}
  \]
  \[
  K_E-K_E^T=0
  \]

- Cantilever with a transverse tip load:
  \[
  \delta_{\text{tip}}=-\frac{PL^3}{3EI}
  \]
  \[
  \theta_{\text{tip}}=-\frac{PL^2}{2EI}
  \]
  The negative signs follow the stated convention for a downward load and clockwise tip rotation.

- Cantilever bending moment:
  \[
  M(x)=-P(L-x)=-PL+Px
  \]
  Thus:
  \[
  M(0)=-PL,\qquad M(L)=0
  \]

- Frame-element equilibrium:
  \[
  F_E=K_ED
  \]
  with \(F_E\) and \(D\) as \(6\times1\) vectors and \(K_E\) as a \(6\times6\) matrix.

- Coordinate transformation definitions:
  \[
  C=\cos\alpha,\qquad S=\sin\alpha
  \]
  The full transformation matrix was not reproduced in the source summaries, so its exact entries should be taken from the course notes or laboratory implementation.

- Static equilibrium:
  \[
  \sum F_{X_G}=0,\qquad
  \sum F_{Y_G}=0,\qquad
  \sum M_A=0
  \]

- Moment of a force:
  \[
  M_A=Fd_\perp
  \]
  A force whose line of action passes through \(A\) has \(d_\perp=0\) and produces no moment about \(A\).

- Euler buckling:
  \[
  P_{\mathrm{cr}}=\frac{\pi^2EI}{(KL)^2}
  \]
  with \(K=1.0\) for a pin-pinned member and \(K=2.0\) for a fixed-free member, as stated in Lecture 12.

- Worked modelling pattern:
  1. Define element and global degrees of freedom.
  2. Establish local-to-global mappings.
  3. Construct transformation and assembly matrices.
  4. Assemble the global stiffness system.
  5. Apply loads and boundary conditions.
  6. Solve for global displacements.
  7. Recover element forces and support reactions.
  8. Check element, nodal, and global equilibrium.
  9. Interpret signs, directions, units, and physical locations before sketching the deformation.

## Warnings and deadlines

- Euler–Bernoulli beam theory should not be applied uncritically to short or squat beams because shear deformation may be significant.
- The beam and frame formulations use small-deflection assumptions. Secondary effects from displaced axial loads are not automatically captured by the basic uncoupled linear frame formulation.
- A numerically valid result can still be physically wrong if the wrong \(6\times6\) local or global matrix is used. Matrix dimensions alone will not necessarily expose the error.
- Stiffness-matrix entries, transformation matrices, assembly matrices, and degree-of-freedom ordering must be checked against the course notes and laboratory implementation where the summaries identify transcription limitations.
- The source summaries do not provide a confirmed current assessment deadline. Lecture 11 mentioned an indicated test date of 18 August, but described the assessment schedule as provisional and directed students to check the official course information.
- Lecture 12 stated that test preparation should include assigning degrees of freedom, drawing free-body diagrams, interpreting displacement results, sketching deformed shapes, and identifying reaction loads. A computer may be used as a calculator or computational tool; full marks should not require plotting code.
- Do not rely on the withdrawn explanation of differing load shares in Lecture 12. The corrected explanation is based on effective stiffness, boundary conditions, curvature, and deformation energy.

## Recall questions

1. What are the four local degrees of freedom of the two-node Euler–Bernoulli beam element?
2. Why are cubic shape functions used for this four-degree-of-freedom beam element?
3. Why is shear deformation neglected in Euler–Bernoulli theory, and when would a Timoshenko beam element be more appropriate?
4. Why is the unconstrained beam stiffness matrix singular?
5. What does the symmetry condition \(K_{ij}=K_{ji}\) imply, and how can it be checked computationally?
6. How is the six-degree-of-freedom frame element constructed from axial bar and beam formulations?
7. Why can two elements with identical \(E\), \(I\), and \(L\) attract different load shares?
8. What does “load follows stiffness” mean in the context of structural design?
9. Why must connected element degrees of freedom representing the same physical motion map to the same global degree of freedom?
10. What physical load path was lost when vertical or axial degrees of freedom were suppressed in the portal-frame example?

## Practice priorities

- Re-derive the four beam nodal boundary conditions and the unit-rotation shape-function case.
- Memorise the beam stiffness-matrix ordering and verify the matrix symmetry.
- Practise reducing the beam stiffness system for a cantilever and checking the analytical tip displacement and rotation.
- Distinguish clearly between bar, beam, and frame element degrees of freedom and load-carrying mechanisms.
- Practise local-to-global degree-of-freedom mapping for inclined frame elements.
- Build assembly matrices from connectivity rather than relying on memorised patterns.
- Interpret every solved displacement entry by its degree-of-freedom number, direction, sign, unit, and structural location.
- Sketch deformed shapes from nodal translations and rotations while enforcing fixed and pin-support constraints.
- Recover element-end forces and verify nodal and global equilibrium.
- Test any modelling simplification by checking whether it removes axial, bending, shear, rotational, or reaction load paths.
- Practise identifying when stiffness differences arise from \(E\), \(I\), \(L\), orientation, connectivity, or boundary conditions.
- Review Euler buckling effective-length factors and how support conditions affect effective stiffness.

## Missing or incomplete

- No lectures were missing or identified as incomplete for this weekly summary.
- The following source details remain incomplete or transcription-limited:
  - Lecture 9 does not reliably preserve all four explicit final beam shape-function expressions.
  - Lecture 10 does not fully reproduce the frame transformation matrix.
  - Lecture 10 does not fully recover the additional-displacement equation for the displaced lumped-mass example.
  - Lecture 12 does not fully reproduce some frame stiffness, transformation, shape-function, and assembly matrices.
  - Some Lecture 12 numerical values and degree-of-freedom labels depend on diagrams not included in the source text.

## Source manifest

- Lecture 9 (echo-lecture-9-9): complete; summary `1e662d43de9e25ff51ec7f8e102f8b1a68ca85692c4feed1690d32778b2421e4`; transcript `81778e30d402b2b4cdde588f61d06ab037b24a16a59c6bff2a1206d68a4cc171`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_09_summary.md`
- Lecture 10 (echo-lecture-10-10): complete; summary `066dd373548f8543925b0c0f0b63898943ee78bc0b42d82169ef70199baa28c6`; transcript `6d30a9e5c8c05b34b58b042b84d2bbad87bb609aee7735536695a67784b7a967`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_10_summary.md`
- Lecture 11 (echo-lecture-11-11): complete; summary `6dbbf8c7d90a49048c92b917bf832c4a6e8c97e8394336c3b16135bd09982abe`; transcript `431c162d0ac2fe965d54ff2b4ea671ae168d1c6dceea78a3304be709f0ca8fb8`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_11_summary.md`
- Lecture 12 (echo-lecture-12-12): complete; summary `941e2377bd4b9fc7884d7701752fa43a736b110a3b3fe8bb4cd28aa0d6bb86ed`; transcript `5eb2e9f2977101bb512f33d4d99074869e98372f9d557b3fddd5e3a74440ba18`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_12_summary.md`
