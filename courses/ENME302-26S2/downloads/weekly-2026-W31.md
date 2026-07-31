<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-31T12:08:19.801318+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Lecture 9: Euler–Bernoulli two-node beam-element formulation, beam degrees of freedom, cubic interpolation, weak form, and shape-function construction.
- Lecture 10: Beam stiffness-matrix derivation, cantilever verification, frame elements, coordinate transformations, assembly, and implementation checks.
- Lecture 11: Purpose and scope of finite element analysis, determinate versus indeterminate structures, discretisation, nodes, degrees of freedom, shape functions, and classical cantilever analysis.
- The supplied Lecture 11 file contains caveats indicating a possible lecture-number or course-code mismatch and substantial automated-transcription errors. Interpret details against the verified source files and official course information where necessary.

## Main concepts

- A two-node Euler–Bernoulli beam element has four local degrees of freedom:
  - Transverse displacement and rotation at node 1.
  - Transverse displacement and rotation at node 2.
- The beam element excludes axial deformation and assumes:
  - Small deflections and rotations.
  - Linear elastic behaviour.
  - Constant \(E\), \(I\), and \(L\).
  - A slender beam where shear deformation is negligible.
- Euler–Bernoulli theory is less suitable for short or squat beams. A Timoshenko beam element is the stated extension for including shear deformation.
- Beam transverse displacement is interpolated from four cubic shape functions:
  \[
  v(x)=\mathbf{N}(x)\mathbf{D}
  \]
- Shape functions are constructed by applying unit displacement or unit rotation at one degree of freedom while setting the other nodal quantities to zero.
- The beam stiffness matrix is obtained from the second derivatives of the shape functions through virtual work.
- The unconstrained beam stiffness matrix is singular because rigid-body modes remain. Boundary conditions are required before obtaining a unique solution.
- A frame element combines axial bar behaviour with beam bending behaviour in one six-degree-of-freedom element.
- In the presented linear frame formulation, axial and flexural behaviour appear in one matrix but are not inherently coupled.
- Local element quantities must be transformed to global coordinates before assembly.
- Matrix dimensions alone do not establish correctness. A local and global frame stiffness matrix may both be \(6\times6\), even though they have different physical meanings.
- Finite element analysis replaces a continuous structure with nodes and elements, then assembles local element relationships into a global system.
- Statically indeterminate structures require compatibility and stiffness information in addition to equilibrium.
- One-dimensional elements provide a computationally efficient starting point for modelling larger two-dimensional or three-dimensional structures.

## Equations and worked patterns

- Local beam degree-of-freedom vector:
  \[
  \mathbf{D}
  =
  \begin{bmatrix}
  v_1\\
  \theta_1\\
  v_2\\
  \theta_2
  \end{bmatrix}
  \]
- Beam interpolation:
  \[
  v(x)=N_1(x)D_1+N_2(x)D_2+N_3(x)D_3+N_4(x)D_4
  \]
- General cubic shape-function form:
  \[
  N_i(x)=A_i x^3+B_i x^2+C_i x+D_i
  \]
- Euler–Bernoulli moment–curvature relation:
  \[
  M=EI\frac{d^2v}{dx^2}
  \]
  The exact sign depends on the adopted convention.
- For a beam element with constant \(E\) and \(I\), a stiffness component is:
  \[
  K_{ij}
  =
  EI\int_0^L
  \frac{d^2N_i}{dx^2}
  \frac{d^2N_j}{dx^2}\,dx
  \]
- Beam-element stiffness matrix for the ordering \([D_1,D_2,D_3,D_4]^T\):
  \[
  K_E=\frac{EI}{L^3}
  \begin{bmatrix}
  12 & 6L & -12 & 6L\\
  6L & 4L^2 & -6L & 2L^2\\
  -12 & -6L & 12 & -6L\\
  6L & 2L^2 & -6L & 4L^2
  \end{bmatrix}
  \]
- Example stiffness entry:
  \[
  K_{22}=\frac{4EI}{L}
  \]
- Symmetry check:
  \[
  K_{ij}=K_{ji},\qquad K_E-K_E^T=0
  \]
- Cantilever with a transverse tip load \(P\):
  \[
  \delta_{\text{tip}}=-\frac{PL^3}{3EI}
  \]
  \[
  \theta_{\text{tip}}=-\frac{PL^2}{2EI}
  \]
  The negative signs follow the stated convention for downward displacement and clockwise tip rotation.
- Cantilever bending moment, with \(x\) measured from the fixed support:
  \[
  M(x)=-P(L-x)=-PL+Px
  \]
  Therefore:
  \[
  M(0)=-PL,\qquad M(L)=0
  \]
- Frame-element local degrees of freedom:
  \[
  [D_1,D_2,D_3,D_4,D_5,D_6]
  =
  [X_1,Y_1,Z_1,X_2,Y_2,Z_2]
  \]
- Frame equilibrium relationship:
  \[
  F_E=K_E D
  \]
- For an element at angle \(\alpha\):
  \[
  C=\cos\alpha,\qquad S=\sin\alpha
  \]
  The complete transformation matrix was not fully stated in the supplied Lecture 10 summary, so it should not be reconstructed from this summary alone.
- Recommended worked pattern:
  1. Define the element degrees of freedom and ordering.
  2. Form the local element stiffness matrix.
  3. Transform it to global coordinates if required.
  4. Assemble the global stiffness matrix.
  5. Apply boundary conditions.
  6. Solve for unknown nodal displacements.
  7. Recover element displacements and forces.
- For a cantilever verification, constrain the two fixed-end beam degrees of freedom, reduce the system to the free-end displacement and rotation, and compare the solution with the analytical tip results above.

## Warnings and deadlines

- Euler–Bernoulli beam results should not be applied uncritically to short, deep, or squat beams because shear deformation may be significant.
- The beam stiffness matrix is singular before boundary conditions are applied. Do not attempt to solve the unconstrained system as though it had a unique displacement solution.
- Maintain the exact degree-of-freedom ordering used to derive the stiffness matrix. A wrong ordering can produce plausible but incorrect results.
- Check both matrix symmetry and matrix meaning. For frame elements, using a local matrix instead of a transformed global matrix may not trigger a dimension error.
- The basic small-displacement frame formulation does not automatically capture secondary moments caused by axial force acting through a laterally displaced member.
- The gravity-induced overturning example involving a displaced lumped mass was described as a first-order approximation. An iterative update would be needed for improved convergence.
- Lecture 11 mentions a computer-based test in Week 6 and an indicated test date of 18 August, along with assignments, quizzes, and a minimum final-exam mark. The source explicitly describes these assessment details as provisional, so they are not confirmed deadlines.

## Recall questions

1. What are the four local degrees of freedom of the two-node Euler–Bernoulli beam element?
2. Why are four shape functions required for this beam element?
3. What assumptions justify neglecting shear deformation in the Euler–Bernoulli model?
4. How are the beam shape functions generated using unit nodal displacement and rotation cases?
5. Why does the beam stiffness matrix use the second derivatives of the shape functions?
6. Why is the unconstrained beam stiffness matrix singular?
7. What are the standard tip displacement and tip rotation results for a tip-loaded cantilever?
8. What is the difference between a beam element and a frame element in the presented formulation?
9. Why must a frame-element stiffness matrix be transformed from local to global coordinates before structural assembly?
10. Why are equilibrium equations alone insufficient for a statically indeterminate structure?

## Practice priorities

- Reconstruct the four beam-element degrees of freedom and maintain their ordering throughout a calculation.
- Practise the unit-deformation method for deriving cubic beam shape functions, including the four boundary conditions for each case.
- Derive or verify the beam stiffness matrix from the shape-function second derivatives and the \(EI\) integral.
- Check stiffness matrices for symmetry and identify why rigid-body modes produce singularity before constraints are applied.
- Solve a one-element cantilever by applying fixed-end boundary conditions and compare the numerical result with:
  \[
  \delta_{\text{tip}}=-\frac{PL^3}{3EI},\qquad
  \theta_{\text{tip}}=-\frac{PL^2}{2EI}
  \]
- Practise distinguishing local and global coordinate systems, especially when the element angle is not zero.
- Review the assembly workflow from element degrees of freedom through global displacement and element-force recovery.
- Revisit the difference between statically determinate and indeterminate structures, focusing on the role of relative stiffness and compatibility.
- Review nodes, degrees of freedom, boundary conditions, shape functions, mesh refinement, and the purpose of one-dimensional elements in FEA.

## Missing or incomplete

- Lecture 12: missing_summary.
- Lecture 9 does not provide the final explicit expressions for all four cubic beam shape functions.
- Lecture 9 does not complete the full beam stiffness-matrix derivation.
- Lecture 10 does not provide the complete coordinate-transformation matrix expression in the supplied summary.
- The exact sign conventions for some shear-force, bending-moment, and distributed-load relationships are not unambiguously recoverable from Lecture 9.
- Lecture 11 does not derive the complete finite-element matrix formulation, element stiffness matrices, coordinate transformations, or assembly algorithms.
- The numerical truss stress calculation in Lecture 11 is incomplete because the supplied summary lacks enough clearly transcribed geometry, support, and loading information.

## Source manifest

- Lecture 9 (echo-lecture-9-9): complete; summary `1e662d43de9e25ff51ec7f8e102f8b1a68ca85692c4feed1690d32778b2421e4`; transcript `81778e30d402b2b4cdde588f61d06ab037b24a16a59c6bff2a1206d68a4cc171`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_09_summary.md`
- Lecture 10 (echo-lecture-10-10): complete; summary `066dd373548f8543925b0c0f0b63898943ee78bc0b42d82169ef70199baa28c6`; transcript `6d30a9e5c8c05b34b58b042b84d2bbad87bb609aee7735536695a67784b7a967`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_10_summary.md`
- Lecture 11 (echo-lecture-11-11): complete; summary `6dbbf8c7d90a49048c92b917bf832c4a6e8c97e8394336c3b16135bd09982abe`; transcript `431c162d0ac2fe965d54ff2b4ea671ae168d1c6dceea78a3304be709f0ca8fb8`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_11_summary.md`
- Lecture 12 (echo-lecture-12-12): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
