<!-- week-id: 2026-W29 -->
<!-- generated-at: 2026-07-19T12:30:31.245689+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Study period: 2026-07-13 to 2026-07-19 12:28 NZ time.
- Verified summaries covered: Lectures 1–3.
- Lecture 1 introduced finite element analysis, discretisation, nodes, degrees of freedom, boundary conditions, element assembly, and the progression from axial truss to flexural beam elements.
- Lecture 2 established the finite element workflow and formulated the two-node axial bar boundary-value problem.
- Lecture 3 derived the axial bar’s linear shape functions, constant strain and stress fields, element stiffness matrix, rigid-body mode, and singularity of an unconstrained element.
- Lecture 4 was not available.

## Main concepts

- FEA replaces a continuous system with discrete elements connected at nodes. Nodal quantities are solved first, then internal fields are reconstructed using shape functions.
- Standard workflow:
  1. Discretise the structure.
  2. Form each element stiffness equation.
  3. Transform local quantities to global coordinates where necessary.
  4. Assemble the global system.
  5. Apply loads and displacement boundary conditions.
  6. Solve for nodal displacements.
  7. Recover reactions, internal forces, strains, and stresses.
  8. Check whether the results are physically meaningful.
- The matrix stiffness relationship is the finite element form of Hooke’s law:
  \[
  \mathbf F=\mathbf K\mathbf D
  \]
- The initial two-node bar element is homogeneous and prismatic, has constant \(E\) and \(A\), carries axial force only, and has one axial displacement degree of freedom at each node.
- Loads are initially restricted to nodes. A transverse load applied within a bar element would introduce shear and bending, violating the axial-only formulation.
- Each element has a local axis running from local node 1 to local node 2. A global coordinate system describes the complete structure, with element orientation used to transform between the two systems.
- For \(p(x)=0\) with constant \(E\) and \(A\), the axial displacement is linear, while strain, stress, and normal force are constant within an element.
- Shape functions act as position-dependent weights. They both construct the element formulation and recover internal behaviour from solved nodal displacements.
- If \(d_1=d_2\), the element undergoes rigid-body translation without deformation. Consequently, strain, stress, and internal force are zero.
- The unconstrained bar stiffness matrix is singular because rigid-body translation remains possible. A suitable displacement boundary condition is required for a unique solution.
- A varying cross-section can be approximated using multiple short, piecewise-prismatic elements. Refinement improves the representation of continuously varying geometry.

## Equations and worked patterns

- Uniform axial bar:
  \[
  \delta=\frac{PL}{AE},
  \qquad
  P=\frac{AE}{L}\delta,
  \qquad
  k=\frac{AE}{L}
  \]

- Axial-bar governing equation:
  \[
  -\frac{d}{dx}\left(EA\frac{du}{dx}\right)=p(x)
  \]
  The precise distributed-load sign depends on the adopted convention. For the zero-load case used in Lecture 3:
  \[
  \frac{d}{dx}\left(EA\frac{du}{dx}\right)=0
  \]

- With constant \(E\), constant \(A\), and \(p(x)=0\):
  \[
  EA\frac{d^2u}{dx^2}=0
  \]

- Apply the nodal conditions:
  \[
  u(0)=d_1,
  \qquad
  u(L)=d_2
  \]

- Starting from \(u(x)=a_0+a_1x\):
  \[
  a_0=d_1,
  \qquad
  a_1=\frac{d_2-d_1}{L}
  \]

- Linear displacement interpolation:
  \[
  u(x)=\left(1-\frac{x}{L}\right)d_1+\frac{x}{L}d_2
  \]

- Shape functions:
  \[
  \psi_1(x)=1-\frac{x}{L},
  \qquad
  \psi_2(x)=\frac{x}{L}
  \]
  with:
  \[
  \psi_1+\psi_2=1
  \]

- Recover element behaviour:
  \[
  \Delta L=d_2-d_1
  \]
  \[
  \varepsilon=\frac{du}{dx}=\frac{d_2-d_1}{L}
  \]
  \[
  \sigma=E\varepsilon
  =E\frac{d_2-d_1}{L}
  \]
  \[
  N=A\sigma
  =\frac{EA}{L}(d_2-d_1)
  \]

- Element end forces:
  \[
  F_1=\frac{EA}{L}(d_1-d_2),
  \qquad
  F_2=\frac{EA}{L}(d_2-d_1)
  \]
  Therefore \(F_1=-F_2\) when no distributed axial load acts.

- Element stiffness matrix:
  \[
  \begin{bmatrix}
  F_1\\
  F_2
  \end{bmatrix}
  =
  \frac{EA}{L}
  \begin{bmatrix}
  1 & -1\\
  -1 & 1
  \end{bmatrix}
  \begin{bmatrix}
  d_1\\
  d_2
  \end{bmatrix}
  \]

- Worked interpolation pattern from Lecture 3:
  \[
  L=1\ \text{m},\qquad d_1=0.1\ \text{m},\qquad d_2=0.2\ \text{m}
  \]
  gives:
  \[
  u(0.25L)=0.125\ \text{m},\quad
  u(0.5L)=0.150\ \text{m},\quad
  u(0.75L)=0.175\ \text{m}
  \]
  This consists of \(0.1\ \text{m}\) rigid-body translation plus \(0.1\ \text{m}\) extension.

## Warnings and deadlines

- The first computer-based test was stated as Tuesday 18 August, in Week 6, and worth 25%.
- Laboratory code is intended to support the test. The laboratories carry no direct grade but are important preparation.
- Assignment 1 was stated as worth 10% and due shortly after the term break or early in Week 7.
- Online quizzes were stated to total 5%, but their exact timing was inconsistent in the source summary and must be confirmed officially.
- Assignment 2 was described as due on 13 October or in the final week of semester; confirm the official schedule.
- Passing requirements stated in Lecture 2 were at least 40% in the final examination and at least 50% overall.
- The assessment schedule was described in Lecture 1 as provisional until the end of Week 2.
- Permitted test materials were not captured reliably enough to confirm. Check the official assessment instructions.
- Do not explicitly invert \(\mathbf K\) in implementation merely because \(\mathbf D=\mathbf K^{-1}\mathbf F\) can be written formally. Use a linear-system solver.
- NumPy’s `A @ B` or `np.matmul(A, B)` performs matrix multiplication; `A * B` performs element-wise multiplication.
- A solver warning about rigid-body modes, insufficient constraints, or automatically added weak springs indicates a boundary-condition problem that should be investigated rather than ignored.

## Recall questions

1. What are the principal stages from structural discretisation to physical interpretation of an FEA result?
2. Which assumptions define the initial two-node axial bar element?
3. Why would a transverse load applied between the nodes violate the axial-bar assumptions?
4. How are the shape functions \(\psi_1=1-x/L\) and \(\psi_2=x/L\) derived from the nodal displacement conditions?
5. Why does a linear displacement field produce constant strain within the element?
6. How are strain, stress, and normal force recovered from \(d_1\) and \(d_2\)?
7. What physical behaviour occurs when \(d_1=d_2\), and why does it produce no internal force?
8. Why is the unconstrained axial-bar stiffness matrix singular, and what modelling action removes that singularity?
9. Why might several piecewise-prismatic elements represent a tapered bar better than one linear element?
10. Why must finite element results still be checked physically even when the numerical solver converges?

## Practice priorities

1. Derive the two linear shape functions from \(u(0)=d_1\) and \(u(L)=d_2\) without referring to notes.
2. Differentiate the interpolated displacement to recover strain, then derive stress, normal force, end forces, and the \(2\times2\) stiffness matrix.
3. Demonstrate algebraically that the rigid-body vector \(c[1\ \ 1]^T\) produces zero element force.
4. Practise identifying local node order, the positive local axis, nodal degrees of freedom, and signs of tension or compression.
5. Work small interpolation problems at \(x=0.25L\), \(0.5L\), and \(0.75L\).
6. Practise distinguishing rigid-body translation from deformation using the relative displacement \(d_2-d_1\).
7. Review NumPy array copying, matrix assembly, matrix multiplication, linear-system solution, scientific notation, and readable output formatting.
8. For any solved model, check equilibrium, support conditions, displacement direction, force signs, units, and whether the chosen element assumptions match the loading.

## Missing or incomplete

- Lecture 4: `missing_summary`.
- Consequently, no Lecture 4 concepts, equations, examples, warnings, or deadlines are included.
- The distributed-load sign convention differs between the Lecture 2 and Lecture 3 presentations; the zero-distributed-load formulation is unaffected.
- Exact quiz dates, Assignment 2 timing, laboratory timetable details, and test-material rules require confirmation from official course information.

## Source manifest

- Lecture 1 (echo-lecture-1-1): complete; summary `2c8ccdce8568cc671739a4c19a27d1ddba6cc99644f848e3d5e60ac2d811ec61`; transcript `5b5cc30b8aee1409c1a3e520c3d03c1ac22a04e1a6c4bbd4565867a041c05e4b`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_01_summary.md`
- Lecture 2 (echo-lecture-2-2): complete; summary `6c2d654a4ba5b49990a4c28a57876f57edde8ecf57dae071a262155ea8c50cf2`; transcript `5217ec0795bda3c3cccff1ec79a5b5450196ed96b82e1bea1bf1b277ec274ff5`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_02_summary.md`
- Lecture 3 (echo-lecture-3-3): complete; summary `b2cf529a2ee003c3fdef687770a09173305c8d9ecbe64db35453876692eff8d6`; transcript `f0f7245ffdffa2b8cdac1cc73a98b4a01078bdf7d1fcd84760fdb0b09e0b4d45`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_03_summary.md`
- Lecture 4 (echo-lecture-4-4): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
