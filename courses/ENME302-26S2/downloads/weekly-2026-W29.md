<!-- week-id: 2026-W29 -->
<!-- generated-at: 2026-07-15T10:40:43.389167+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Week: 2026-W29, from 13 July 2026 00:00 to 19 July 2026 08:30 NZ time.
- Covered source: Lecture 1 only.
- Lecture 1 introduced finite element analysis (FEA), discretisation, structural element types, degrees of freedom, boundary conditions, shape functions, and the course structure.
- Lectures 2–4 are not represented because their verified summaries are missing.

## Main concepts

- FEA divides a continuous engineering system into simpler elements connected at nodes, formulates each element’s behaviour, assembles a global system, applies loads and boundary conditions, solves for nodal quantities, and recovers element forces, stresses, strains, moments, or shears.
- FEA builds on classical mechanics rather than replacing it. Stress, strain, equilibrium, compatibility, stiffness, axial loading, bending, and beam deflection remain foundational.
- A statically determinate structure can be solved using equilibrium alone. A statically indeterminate structure also requires displacement compatibility and relative stiffness.
- Ideal axial truss elements are pin-connected, loaded at nodes, and carry only axial tension or compression.
- Flexural beam elements additionally represent bending, shear, nodal rotations, and moments.
- Shape functions interpolate behaviour inside an element from discrete nodal values.
- One-dimensional elements can be oriented and assembled into complex two- or three-dimensional structures.
- A practical modelling hierarchy is to use efficient line elements for global behaviour, identify critical regions, and then apply detailed local models.
- Mesh refinement replaces a geometry with smaller and more numerous elements. Coarse and fine meshes can be compared to assess solution sensitivity.
- FEA is applicable beyond structural analysis wherever suitable governing differential equations exist, including heat flow and magnetism.

## Equations and worked patterns

- Axial normal stress:
  \[
  \sigma=\frac{N}{A}
  \]
  where \(N\) is internal axial force and \(A\) is cross-sectional area.

- Hollow circular cross-sectional area:
  \[
  A=\frac{\pi}{4}\left(D_o^2-D_i^2\right),\qquad D_i=D_o-2t
  \]

- Planar static equilibrium:
  \[
  \sum F_x=0,\qquad \sum F_y=0,\qquad \sum M=0
  \]

- For a cantilever of length \(L\), fixed at \(x=0\), with tip load \(P\), the lecture’s sign convention gives:
  \[
  M(x)=-P(L-x)=-PL+Px
  \]
  Therefore:
  \[
  M(0)=-PL,\qquad M(L)=0,\qquad \frac{dM}{dx}=P
  \]

- Euler–Bernoulli moment-curvature relation:
  \[
  EI\frac{d^2v}{dx^2}=M(x)
  \]
  The sign can vary with the selected moment, curvature, and displacement conventions.

- Fixed-end cantilever boundary conditions:
  \[
  v(0)=0,\qquad \frac{dv}{dx}(0)=0
  \]

- Tip-loaded cantilever result magnitudes:
  \[
  \delta_{\text{tip}}=\frac{PL^3}{3EI},\qquad
  \theta_{\text{tip}}=\frac{PL^2}{2EI}
  \]

- General FEA workflow:
  1. Discretise the domain into elements and nodes.
  2. Define element behaviour and degrees of freedom.
  3. Assemble the element equations into a global system.
  4. Apply loads and boundary conditions.
  5. Solve for unknown nodal quantities.
  6. Recover element-level forces, stresses, strains, moments, or shears.

## Warnings and deadlines

- A computer-based test was stated to be scheduled for the evening of Tuesday 18 August 2026, early in week 6.
- Assignment 1 was described as due shortly after the term break.
- Five quizzes worth 1% each were expected to begin after the week-5 lecturer change.
- Assignment 2 was described as due in early October.
- A minimum final-examination mark of 40% was stated as necessary to pass the course overall.
- The assessment schedule remained provisional until the end of week 2.
- Exact test-resource rules were unclear. The summary indicates that laboratory code, and possibly a self-prepared reference page, may be permitted, but this must be confirmed using official course instructions.
- Eigenvalue buckling gives an idealised elastic critical load. Lecture 1 did not cover imperfections, residual stress, material nonlinearity, or nonlinear post-buckling effects.
- Boundary conditions and degrees of freedom must match the physical structure; incorrect restraints can invalidate the model.

## Recall questions

1. What are the main steps for converting a continuous structure into a finite element model?
2. Why is equilibrium sufficient for a statically determinate structure but insufficient for a statically indeterminate one?
3. Under what assumptions does an axial truss element carry no shear force or bending moment?
4. What additional actions and degrees of freedom are introduced by a flexural beam element?
5. What role do shape functions play between finite element nodes?
6. How can one-dimensional elements represent a two- or three-dimensional structure?
7. For the tip-loaded cantilever, how is \(M(x)=-P(L-x)\) obtained, and what are its values at \(x=0\) and \(x=L\)?
8. What boundary conditions must be applied when integrating the cantilever moment-curvature equation?
9. Why might a global line-element model be preferable to a complete 3D solid model?
10. Why should coarse- and fine-mesh results be compared?

## Practice priorities

1. Refresh Python matrix entry, matrix multiplication, linear-algebra manipulation, and plotting before later finite element laboratories.
2. Practise identifying whether a structure is statically determinate or indeterminate and explaining what additional equations are required.
3. Classify supports as fixed, free, pinned, roller, knife-edge, or slotted, then identify the restrained and unrestrained degrees of freedom.
4. Derive the bending-moment function for a tip-loaded cantilever and apply the fixed-end boundary conditions.
5. Review axial stress and hollow circular-section area calculations.
6. Rehearse the full discretise–assemble–constrain–solve–recover FEA workflow.
7. Compare axial truss and flexural beam elements by their connections, loads, degrees of freedom, and internal actions.
8. Participate actively in computer laboratories because the resulting code and skills are intended to support the week-6 test.

## Missing or incomplete

- Lecture 2: missing summary.
- Lecture 3: missing summary.
- Lecture 4: missing summary.
- No concepts, equations, examples, or deadlines from Lectures 2–4 can be included or inferred.
- Some Lecture 1 timetable details and test-resource rules were unclear in the underlying transcript and require confirmation from official course information.

## Source manifest

- Lecture 1 (echo-lecture-1-1): complete; summary `2c8ccdce8568cc671739a4c19a27d1ddba6cc99644f848e3d5e60ac2d811ec61`; transcript `5b5cc30b8aee1409c1a3e520c3d03c1ac22a04e1a6c4bbd4565867a041c05e4b`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_01_summary.md`
- Lecture 2 (echo-lecture-2-2): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
- Lecture 3 (echo-lecture-3-3): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
- Lecture 4 (echo-lecture-4-4): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
