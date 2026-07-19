<!-- week-id: 2026-W29 -->
<!-- generated-at: 2026-07-19T20:53:20.337693+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Week: 2026-W29, from 2026-07-13T00:00:00+12:00 to 2026-07-19T20:52:01.289027+12:00.
- Sources covered:
  - Lecture 1: course framework, discretisation, element types, boundary conditions, shape functions, and FEA applications.
  - Lecture 2: matrix stiffness formulation, two-node axial bars, local and global coordinates, and the axial-bar governing equation.
  - Lecture 3: linear shape functions, interpolation, strain, stress, axial force, element stiffness matrix, rigid-body modes, and mesh refinement.
  - Lecture 4: two-member truss analysis, small-deflection linearisation, strain energy, work-energy methods, and virtual work.
- Missing or incomplete lectures: None.

## Main concepts

- Finite element analysis discretises a continuous structure into connected elements and nodes.
- Element equations are transformed where necessary and assembled into a global stiffness system.
- The fundamental static relationship is:
  \[
  \mathbf{F}=\mathbf{K}\mathbf{D}
  \]
- A two-node axial bar element assumes:
  - pin-connected members;
  - nodal loading;
  - axial force only;
  - constant \(A\), \(E\), and \(L\);
  - homogeneous, prismatic behaviour;
  - no distributed axial loading in the initial formulation.
- The local element coordinate runs from local node 1 to local node 2. Element orientation must be transformed consistently into the global coordinate system.
- Axial bar elements have one axial translational degree of freedom at each node. Beam elements add lateral displacement and rotation; frame elements combine axial and bending behaviour.
- Shape functions interpolate the displacement field between nodal values and allow strain, stress, and internal force to be recovered.
- For a uniform, unloaded axial bar, displacement varies linearly and strain, stress, and axial force are constant.
- Equal nodal displacements produce rigid-body translation, not deformation.
- The unconstrained axial-bar stiffness matrix is singular because rigid-body translation is possible. Adequate displacement boundary conditions are required for a unique solution.
- A varying cross-section can be approximated using multiple smaller, piecewise-prismatic elements.
- Small-deflection linearisation uses the initial geometry as an approximation to the displaced geometry and neglects higher-order geometric terms.
- External work and internal strain energy can determine displacement under suitable loading conditions.
- The single-load work-energy method determines displacement only at the point and in the direction of the single applied load.
- Virtual work uses separate real and virtual load systems to determine displacements in arbitrary directions, including where no real load acts.
- Virtual internal forces act as weighting factors for the contribution of each member’s deformation to the requested displacement.
- Python priorities included array copying, transposition, block-matrix construction, matrix multiplication, solving linear systems, plotting, scientific notation, and readable output.

## Equations and worked patterns

- Uniform-bar extension:
  \[
  \delta=\frac{PL}{AE}
  \]
- Axial stiffness:
  \[
  k=\frac{AE}{L}
  \]
- Global finite element equation:
  \[
  \mathbf{F}=\mathbf{K}\mathbf{D}
  \]
- Axial-bar strain and stress:
  \[
  \varepsilon=\frac{du}{dx},\qquad \sigma=E\varepsilon
  \]
- Axial force:
  \[
  N=A\sigma=EA\frac{du}{dx}
  \]
- Homogeneous, unloaded axial-bar equation:
  \[
  \frac{d}{dx}\left(EA\frac{du}{dx}\right)=0
  \]
- Two-node linear displacement field:
  \[
  u(x)=\left(1-\frac{x}{L}\right)d_1+\frac{x}{L}d_2
  \]
- Linear shape functions:
  \[
  \psi_1(x)=1-\frac{x}{L},\qquad \psi_2(x)=\frac{x}{L}
  \]
  with:
  \[
  \psi_1(x)+\psi_2(x)=1
  \]
- Constant axial strain:
  \[
  \varepsilon=\frac{d_2-d_1}{L}
  \]
- Constant axial force:
  \[
  N=\frac{EA}{L}(d_2-d_1)
  \]
- Element end forces:
  \[
  F_1=\frac{EA}{L}(d_1-d_2),\qquad
  F_2=\frac{EA}{L}(d_2-d_1)
  \]
- Two-node axial-bar stiffness matrix:
  \[
  \mathbf{k}^{(e)}
  =
  \frac{EA}{L}
  \begin{bmatrix}
  1 & -1\\
  -1 & 1
  \end{bmatrix}
  \]
- Rigid-body mode:
  \[
  \mathbf{d}^{(e)}
  =
  c
  \begin{bmatrix}
  1\\
  1
  \end{bmatrix},
  \qquad
  \mathbf{k}^{(e)}\mathbf{d}^{(e)}=\mathbf{0}
  \]
- Axial member deformation:
  \[
  \delta_i=\frac{F_iL_i}{A_iE_i}
  \]
- Strain energy in one axial member:
  \[
  U_i=\frac{F_i^2L_i}{2A_iE_i}
  \]
- Total truss strain energy:
  \[
  U_{\text{total}}=\sum_i\frac{F_i^2L_i}{2A_iE_i}
  \]
- Work for a constant force:
  \[
  W=P\delta
  \]
- Work for a gradually applied linear-elastic force:
  \[
  W=\frac12P\delta
  \]
- Single-load work-energy condition:
  \[
  U_{\text{total}}=\frac12P\delta
  \]
- Virtual-work equation:
  \[
  P_v\Delta
  =
  \sum_i\frac{f_iF_iL_i}{A_iE_i}
  \]
  For a unit virtual load:
  \[
  \Delta
  =
  \sum_i\frac{f_iF_iL_i}{A_iE_i}
  \]
- Two-member truss example:
  - Real member forces:
    \[
    F_1=-100\ \text{kN},\qquad F_2=141.42\ \text{kN}
    \]
    Member 1 is in compression and member 2 is in tension.
  - Reported displacements:
    \[
    \delta_x\approx-0.636\text{ to }-0.637\ \text{mm},
    \qquad
    \delta_y=2.432\ \text{mm}
    \]
  - Reported strain energies:
    \[
    U_1=31.83\ \text{J},\qquad
    U_2=89.76\ \text{J},\qquad
    U_{\text{total}}=121.59\ \text{J}
    \]
- Worked pattern for virtual work:
  1. Solve the real structure and obtain \(F_i\).
  2. Apply a unit virtual load at the point and in the direction of the desired displacement.
  3. Solve the virtual structure independently and obtain \(f_i\).
  4. Substitute \(F_i\) and \(f_i\) into the virtual-work sum.
  5. Interpret the sign of the result relative to the virtual-load direction.

## Warnings and deadlines

- The week 6 computer-based test was stated as Tuesday 18 August and worth 25%. The assessment schedule was described as provisional in the early lectures, so confirm the official course information.
- Laboratory work was described as preparation for the test and code developed in the labs was intended to be used during it. Exact permitted test resources were not reliable in the source and should be confirmed officially.
- Assignment 1 was described as due shortly after the term break or early in Week 7. Confirm the official date.
- Assignment 2 was described inconsistently as due on 13 October or during the final week of the semester. Confirm the official date.
- Five online quizzes were described as worth 1% each, but the timing was inconsistent in the source. Confirm the official schedule.
- The course was stated to require at least 40% in the final examination and at least 50% overall.
- Do not treat a solver’s convergence as proof that a model is physically valid. Check constraints, signs, units, load paths, displacement magnitudes, and expected deformation behaviour.
- A free axial element has a rigid-body mode. Warnings about rigid-body motion, insufficient constraints, or automatically added weak springs indicate a modelling problem that should be investigated.
- Keep local and global coordinate conventions, node ordering, force signs, and matrix numbering consistent.
- The numerical two-member example depends on member properties that were not fully stated in the source. Its reported numerical results should not be independently recomputed using guessed values.
- The demonstrated methods assume small displacement, linear elasticity, compatible deformation, static equilibrium, and valid superposition.

## Recall questions

1. What are the main stages of converting a continuous structure into a finite element model?
2. Why does the initial axial-bar formulation restrict loads to nodal points?
3. How does \(\mathbf{F}=\mathbf{K}\mathbf{D}\) generalise the scalar relation \(F=kx\)?
4. What assumptions justify the linear displacement field for the two-node axial bar?
5. Derive the two axial-bar shape functions and state their values at each node.
6. Why does \(d_1=d_2\) produce rigid-body translation rather than strain?
7. Why is the unconstrained axial-bar stiffness matrix singular, and what removes the singularity?
8. Why is the work for a gradually applied force \(\frac12P\delta\) rather than \(P\delta\)?
9. Why can the single-load work-energy method determine the vertical displacement in Lecture 4 but not the horizontal displacement?
10. In virtual work, what do the real member forces \(F_i\) and virtual member forces \(f_i\) represent?

## Practice priorities

1. Derive the two-node axial-bar interpolation from \(u(x)=a_0+a_1x\).
2. Practise evaluating \(u(x)\), \(\varepsilon\), \(\sigma\), \(N\), and end forces from \(d_1\), \(d_2\), \(A\), \(E\), and \(L\).
3. Assemble and interpret the \(2\times2\) axial-bar stiffness matrix.
4. Identify rigid-body modes and apply boundary conditions that produce a unique solution.
5. Check whether a bar problem satisfies the assumptions of constant \(A\), constant \(E\), and zero distributed axial loading.
6. Practise local-to-global coordinate reasoning, including element orientation and node ordering.
7. Rework the two-member truss equilibrium example and distinguish tension from compression using signs.
8. Compare exact geometric compatibility with the small-deflection linearisation.
9. Calculate member strain energies and use the single-load work-energy method for the displacement aligned with the applied load.
10. Practise the virtual-work workflow for horizontal and vertical displacement requests, keeping real and virtual analyses separate.
11. Consolidate Python operations used for finite element coding: transpose, block assembly, matrix multiplication, array copying, linear-system solving, and readable matrix output.

## Missing or incomplete

- None.

## Source manifest

- Lecture 1 (echo-lecture-1-1): complete; summary `2c8ccdce8568cc671739a4c19a27d1ddba6cc99644f848e3d5e60ac2d811ec61`; transcript `5b5cc30b8aee1409c1a3e520c3d03c1ac22a04e1a6c4bbd4565867a041c05e4b`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_01_summary.md`
- Lecture 2 (echo-lecture-2-2): complete; summary `6c2d654a4ba5b49990a4c28a57876f57edde8ecf57dae071a262155ea8c50cf2`; transcript `5217ec0795bda3c3cccff1ec79a5b5450196ed96b82e1bea1bf1b277ec274ff5`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_02_summary.md`
- Lecture 3 (echo-lecture-3-3): complete; summary `b2cf529a2ee003c3fdef687770a09173305c8d9ecbe64db35453876692eff8d6`; transcript `f0f7245ffdffa2b8cdac1cc73a98b4a01078bdf7d1fcd84760fdb0b09e0b4d45`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_03_summary.md`
- Lecture 4 (echo-lecture-4-4): complete; summary `2a124226ed35859dcbaf8e8e4515232db14da64eec5330c7db58cc5e9b185570`; transcript `2f760e9fbd881996fae0455608e3b5fbfbdaa88551503d9679e550ceffd75d10`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_04_summary.md`
