<!-- week-id: 2026-W29 -->
<!-- generated-at: 2026-07-19T20:33:25.107034+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Covered Lectures 1–4 during 2026-W29, from 2026-07-13T00:00:00+12:00 to 2026-07-19T20:32:17.458653+12:00.
- Main progression:
  - Finite element analysis fundamentals and modelling decisions.
  - Matrix stiffness formulation.
  - Two-node axial bar element.
  - Shape functions, strain, stress, element forces, and stiffness matrix.
  - Rigid-body modes and insufficient constraints.
  - Small-deflection truss analysis.
  - Work-energy and virtual-work methods.
  - Python and NumPy operations supporting finite element implementation.

## Main concepts

- Finite element analysis discretises a continuous structure into elements connected at nodes.
- Element equations are transformed where necessary and assembled into a global system.
- The central static relationship is the matrix form of Hooke’s law:
  \[
  \mathbf{F}=\mathbf{K}\mathbf{D}
  \]
- A two-node axial bar element:
  - Has one axial displacement degree of freedom at each node.
  - Assumes pin connections, nodal loading, constant \(A\), constant \(E\), homogeneous material, and prismatic geometry.
  - Carries axial force only.
- Shape functions interpolate the continuous displacement field from nodal displacements.
- For the homogeneous, unloaded axial bar, displacement is linear and strain, stress, and axial force are constant.
- Rigid-body translation occurs when both nodal displacements are equal. It produces no extension, strain, stress, or internal force.
- The unconstrained axial-bar stiffness matrix is singular because rigid-body translation is possible.
- Boundary conditions remove rigid-body modes and permit a unique solution.
- Local element coordinates describe individual members; global coordinates describe the complete structure. Orientation angles connect the two systems.
- Beam elements add lateral displacement, rotation, bending moment, and shear force. Frame elements combine axial and bending behaviour.
- Small-deflection analysis uses the initial geometry as an approximation to the deformed geometry and neglects higher-order geometric terms.
- Work-energy determines displacement in the direction of a single applied load but cannot generally resolve multiple independent displacement components.
- Virtual work uses a separate virtual load system to calculate a requested displacement at any point and in any direction.
- Virtual internal forces act as weighting factors for the contributions of real member deformations.
- Mesh refinement approximates varying geometry using multiple smaller elements.
- Numerical results must be checked against physical expectations rather than accepted solely because a solver converges.

## Equations and worked patterns

- Uniform axial-bar extension:
  \[
  \delta=\frac{PL}{AE}
  \]
  Therefore:
  \[
  P=\frac{AE}{L}\delta,\qquad k=\frac{AE}{L}
  \]

- Two-node axial-bar displacement interpolation:
  \[
  u(x)=\left(1-\frac{x}{L}\right)d_1+\frac{x}{L}d_2
  \]

- Linear shape functions:
  \[
  \psi_1(x)=1-\frac{x}{L},\qquad
  \psi_2(x)=\frac{x}{L}
  \]
  with:
  \[
  \psi_1(x)+\psi_2(x)=1
  \]

- Axial strain, stress, and normal force:
  \[
  \varepsilon=\frac{du}{dx}=\frac{d_2-d_1}{L}
  \]
  \[
  \sigma=E\varepsilon
  \]
  \[
  N=A\sigma=\frac{EA}{L}(d_2-d_1)
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
  and:
  \[
  \mathbf{f}^{(e)}=\mathbf{k}^{(e)}\mathbf{d}^{(e)}
  \]

- Rigid-body mode:
  \[
  \mathbf{d}^{(e)}
  =
  c
  \begin{bmatrix}
  1\\
  1
  \end{bmatrix}
  \]
  gives:
  \[
  \mathbf{k}^{(e)}\mathbf{d}^{(e)}=\mathbf{0}
  \]

- Axial-bar governing equation for zero distributed load:
  \[
  \frac{d}{dx}\left(EA\frac{du}{dx}\right)=0
  \]
  with:
  \[
  u(0)=d_1,\qquad u(L)=d_2
  \]

- Axial deformation of member \(i\):
  \[
  \delta_i=\frac{F_iL_i}{A_iE_i}
  \]

- Strain energy in a prismatic linear-elastic member:
  \[
  U_i=\frac{F_i^2L_i}{2A_iE_i}
  \]
  For multiple members:
  \[
  U_{\text{total}}=\sum_i\frac{F_i^2L_i}{2A_iE_i}
  \]

- Gradually applied linear-elastic load:
  \[
  W_{\text{external}}=\frac12P\delta
  \]
  A constant force acting throughout the displacement instead gives:
  \[
  W=P\delta
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
  - Reported joint displacements:
    \[
    \delta_x\approx-0.636\text{ to }-0.637\ \text{mm}
    \]
    \[
    \delta_y=2.432\ \text{mm}
    \]
  - The vertical displacement was obtained using total strain energy and the \(100\ \text{kN}\) applied load. The horizontal displacement required a horizontal unit virtual load.

## Warnings and deadlines

- The first computer-based test was stated as Tuesday 18 August in Week 6 and was described as worth 25%.
- The test is expected to use finite element code developed during the preceding laboratories.
- Assignment 1 was described as worth 10% and due shortly after the term break or early in Week 7.
- Online quizzes were described as totalling 5%, apparently five quizzes worth 1% each.
- Assignment 2 was described as due on 13 October, also described as being in the final week of the semester. Confirm the official course schedule.
- Passing requirements stated in Lecture 2:
  - At least 40% in the final examination.
  - At least 50% overall in the course.
- The assessment schedule was described as provisional until the end of Week 2.
- Quiz timing and test-resource rules were inconsistent or unclear in the source summaries. Confirm them using official course instructions.
- A singular stiffness matrix or warnings about rigid-body modes indicate insufficient constraints, not a problem that should simply be hidden with weak springs.
- The Lecture 4 numerical deformation calculations cannot be independently reconstructed from the summaries because the member lengths, areas, and elastic moduli were not stated.
- Use consistent signs and units when applying real and virtual member forces.

## Recall questions

1. What are the main stages from discretising a structure to interpreting recovered finite element results?
2. What assumptions define the initial two-node axial bar element?
3. Why must the initial truss loads be applied at nodes rather than partway along a bar?
4. Derive the two-node axial-bar shape functions from \(u(0)=d_1\) and \(u(L)=d_2\).
5. Why does the linear axial-bar interpolation produce constant strain, stress, and normal force?
6. What happens when \(d_1=d_2\), and why does this make the unconstrained stiffness matrix singular?
7. How do local and global coordinate systems work together for an inclined element?
8. Why can the single-load work-energy method determine the vertical displacement in Lecture 4 but not the horizontal displacement?
9. What is the difference between real internal forces \(F_i\) and virtual internal forces \(f_i\)?
10. How should a horizontal or vertical virtual load be selected when calculating the corresponding displacement?

## Practice priorities

1. Re-derive the axial-bar interpolation, shape functions, strain, stress, normal force, and stiffness matrix without referring to the notes.
2. Practise identifying rigid-body modes and applying sufficient displacement boundary conditions.
3. Implement and test the \(2\times2\) axial-bar stiffness matrix and the global relation \(\mathbf{F}=\mathbf{K}\mathbf{D}\).
4. Review NumPy operations:
   - `A.T` or `np.transpose(A)` for transpose.
   - `np.block` for assembling matrices.
   - `A @ B` or `np.matmul(A, B)` for matrix multiplication.
   - `A * B` for elementwise multiplication.
5. Practise sign conventions for tension, compression, local axes, orientation angles, and element end forces.
6. Work through the Lecture 4 two-member truss using equilibrium and verify the stated member-force signs.
7. Compare the single-load work-energy method with virtual work, including when each method can determine a displacement.
8. Practise calculating member strain energy and summing contributions across a truss.
9. Apply the virtual-work equation for both horizontal and vertical displacements, keeping the real and virtual load cases separate.
10. Check all numerical outputs for equilibrium, plausible deformation directions, compatible units, and physically sensible magnitudes.

## Missing or incomplete

- No lectures were identified as missing or incomplete for this week.
- Some source limitations remain:
  - Several Lecture 4 calculations depend on diagram geometry and material/property data not fully stated in the summary.
  - Official assessment details should be confirmed where the lecture summaries record provisional or conflicting information.
  - The sign convention for the distributed-load differential equation should be checked against the official written notes if used in calculations.

## Source manifest

- Lecture 1 (echo-lecture-1-1): complete; summary `2c8ccdce8568cc671739a4c19a27d1ddba6cc99644f848e3d5e60ac2d811ec61`; transcript `5b5cc30b8aee1409c1a3e520c3d03c1ac22a04e1a6c4bbd4565867a041c05e4b`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_01_summary.md`
- Lecture 2 (echo-lecture-2-2): complete; summary `6c2d654a4ba5b49990a4c28a57876f57edde8ecf57dae071a262155ea8c50cf2`; transcript `5217ec0795bda3c3cccff1ec79a5b5450196ed96b82e1bea1bf1b277ec274ff5`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_02_summary.md`
- Lecture 3 (echo-lecture-3-3): complete; summary `b2cf529a2ee003c3fdef687770a09173305c8d9ecbe64db35453876692eff8d6`; transcript `f0f7245ffdffa2b8cdac1cc73a98b4a01078bdf7d1fcd84760fdb0b09e0b4d45`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_03_summary.md`
- Lecture 4 (echo-lecture-4-4): complete; summary `2a124226ed35859dcbaf8e8e4515232db14da64eec5330c7db58cc5e9b185570`; transcript `2f760e9fbd881996fae0455608e3b5fbfbdaa88551503d9679e550ceffd75d10`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_04_summary.md`
