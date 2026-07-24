<!-- week-id: 2026-W30 -->
<!-- generated-at: 2026-07-24T23:42:27.670568+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Week: 2026-W30, from 2026-07-20T00:00:00+12:00 to 2026-07-24T23:41:42.354928+12:00.
- Source coverage: Lecture 7 only.
- Lecture 7 focused on finite-element analysis of two-dimensional pin-jointed bar and truss structures, including assembly, coordinate transformations, solving, post-processing, and Python implementation.
- Lectures 5, 6, and 8 are known to be missing summaries.

## Main concepts

- A two-dimensional bar element has four global-coordinate displacement components: two translations at each node.
- The finite-element workflow is:
  1. Number the global degrees of freedom.
  2. Define local element stiffness matrices.
  3. Transform element matrices according to orientation.
  4. Assemble the element contributions into the global stiffness matrix.
  5. Apply loads and boundary conditions.
  6. Solve for global displacements.
  7. Extract element quantities and calculate forces, strains, reactions, and deformed geometry.
- The assembly matrix maps element degrees of freedom to global degrees of freedom. It is used both to assemble stiffness contributions and to extract element displacements.
- Local coordinates are aligned with an element; global coordinates are shared by the complete structure.
- Element orientation affects the transformation matrix. Element connectivity affects the assembled global contribution.
- Elements with identical material, area, and length can have identical local stiffness matrices but different assembled contributions because they connect to different global degrees of freedom.
- Horizontal and vertical elements may produce uncoupled equations in the selected coordinates, while inclined elements generally introduce coupling.
- Fixed or supported degrees of freedom have prescribed zero displacement.
- Numerical results must be interpreted using geometry, supports, coordinate directions, force directions, and free-body diagrams.
- For a two-node axial bar, equal-and-opposite end forces directed toward the element indicate compression; forces directed away from the element indicate tension.
- A non-zero calculated displacement at a fixed support indicates a likely error in assembly, transformation, degree-of-freedom numbering, boundary conditions, or sign conventions.
- In Python, trigonometric functions require angles in radians. Deformation plots may use a visual magnification factor, which does not alter the physical solution.

## Equations and worked patterns

- Global stiffness equation:
  
  `K_G q = Q`

  where `K_G` is the assembled global stiffness matrix, `q` is the global displacement vector, and `Q` is the global applied-force vector. The source warns that notation and capitalisation should be checked against the official course material.

- Local two-node axial-bar stiffness matrix:

  `K_e = (EA/L) [[1, -1], [-1, 1]]`

  where `E` is Young’s modulus, `A` is cross-sectional area, and `L` is element length.

- Two-dimensional element displacement vector:

  `d_e = [u_1, v_1, u_2, v_2]^T`

  or the equivalent course-specific ordering.

- Assembly and extraction relation:

  `d_e = A_e^T q`

  where `A_e` is the assembly matrix for element `e`.

- Local element force relation:

  `f_e = K_e d_e`

  The exact transformed-coordinate relation depends on the course definition of the transformation matrix.

- Diagonal length in the square-grid example:

  `L_diagonal = √(10² + 10²) = 10√2 ≈ 14.1 m`

- Axial strain:

  `ε = (D2 − D1) / L`

  The source indicates that `L` should represent the original element length for the small-deformation formulation, but advises checking the official course notes.

- Deformed node coordinates:

  `x' = x + q_x`

  `y' = y + q_y`

- Magnified plotting coordinates:

  `x'_plot = x + mag q_x`

  `y'_plot = y + mag q_y`

  The magnification factor is for visualisation only.

- Worked pattern for a multi-element truss:
  - Construct each local stiffness matrix from `E`, `A`, and `L`.
  - Apply the element orientation.
  - Define the element-to-global degree-of-freedom mapping.
  - Assemble the global stiffness matrix.
  - Apply loads and boundary conditions.
  - Solve the global system.
  - Extract element displacements.
  - Calculate element forces and strains.
  - Check reactions, support displacements, signs, and physical equilibrium.

## Warnings and deadlines

- No deadlines were identified in the available Lecture 7 summary.
- The source is based on a local ASR transcript and reports uncertainty in matrix notation, force units, element numbering, node labels, load directions, displacement values, and transformation-matrix definitions.
- Confirm the official notation and transformation matrices against the course slides or laboratory material before graded use.
- Confirm the structural diagram, support locations, element numbering, and load directions before relying on the worked problem.
- Interpret force signs relative to the local coordinate system and free-body diagram; signs alone are insufficient.
- Ensure angles are converted from degrees to radians before using Python trigonometric functions.
- Distinguish alternating coordinate labels from plotting arrays, where x-values and y-values must be grouped separately.
- Do not treat a magnified deformation plot as the actual physical deformation.

## Recall questions

1. What are the main stages of the finite-element workflow for a two-dimensional pin-jointed structure?
2. What does the assembly matrix map, and why can it be used both for assembly and extraction?
3. How many displacement degrees of freedom does a two-dimensional bar element have?
4. What information is included in the local stiffness matrix, and what additional information is added by transformation and assembly?
5. Why can elements with identical local stiffness matrices have different assembled global contributions?
6. How is the diagonal length calculated for a `10 m × 10 m` square grid?
7. How should equal-and-opposite element-end forces be interpreted as tension or compression?
8. What possible implementation errors could cause a non-zero displacement at a fixed support?
9. Why must element orientation angles be supplied in radians to Python trigonometric functions?
10. How is axial strain calculated from the relative local displacement of an element’s two nodes?

## Practice priorities

1. Recreate the finite-element workflow for a simple two-element bar structure.
2. Practise numbering global and element degrees of freedom and constructing the assembly matrix.
3. Separate the roles of local stiffness, coordinate transformation, assembly, and global summation.
4. Check how element orientation changes the transformed stiffness matrix, especially for inclined members.
5. Practise extracting element displacement vectors from a solved global displacement vector.
6. Calculate element forces and strains, then interpret their signs with a free-body diagram.
7. Perform physical checks: zero displacement at fixed supports, force equilibrium at nodes, and equal-and-opposite axial end forces.
8. Implement the workflow using reusable Python functions for local stiffness, transformations, assembly, solving, and post-processing.
9. Verify degree-to-radian conversion and distinguish plotting coordinate order from displayed coordinate labels.
10. Compare finite-element results with an independently solved simple example where the official course material provides reference values.

## Missing or incomplete

- Lecture 5: missing summary.
- Lecture 6: missing summary.
- Lecture 8: missing summary.
- Within Lecture 7, the following remain incomplete or uncertain in the source:
  - Exact transformation-matrix form and notation.
  - Exact global and element vector notation.
  - Structural diagrams, support locations, element numbering, and load directions.
  - Some numerical force and displacement values, including units and signs.
  - Exact Python function names and implementation details.

## Source manifest

- Lecture 5 (echo-lecture-5-5): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
- Lecture 6 (echo-lecture-6-6): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
- Lecture 7 (echo-lecture-7-7): complete; summary `fc511e7e302eb6e8bdc2a5512ad9ae81810f02bc6ea52fae7e47a289e08f78bb`; transcript `ef8be63a5e990258aa1b573f86b319c8435ffbfc59500f375684c2a7772ee5ea`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_07_summary.md`
- Lecture 8 (echo-lecture-8-8): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
