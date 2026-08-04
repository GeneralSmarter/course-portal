<!-- week-id: 2026-W30 -->
<!-- generated-at: 2026-07-25T00:18:28.778152+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

Week 2026-W30 covered Lectures 5–8, from 2026-07-20T00:00:00+12:00 to 2026-07-25T00:17:32.686121+12:00.

The lectures developed the finite-element method for two-dimensional axial bar and pin-jointed truss structures:

- Weak-form derivation of the two-node axial bar element.
- Shape functions and displacement interpolation.
- Local element stiffness matrices.
- Local and global coordinate systems.
- Coordinate transformation of element matrices.
- Assembly matrices and structural connectivity.
- Assembly and solution of the global stiffness system.
- Recovery of element forces, strains, stresses, and support reactions.
- Physical interpretation and verification using free-body diagrams.
- Computational implementation and plotting of deformed structures.
- Preview of extensions to bending and shear elements.

## Main concepts

- A two-node bar element represents axial deformation only. It has no bending or rotational degrees of freedom.
- The weak form requires the governing equation to hold in an integrated sense over the element.
- Integration by parts reduces derivative order and produces boundary terms associated with nodal forces.
- Shape functions interpolate the continuous displacement field from nodal displacement values.
- For a uniform bar, stiffness depends on \(E\), \(A\), and \(L\), principally through \(EA/L\).
- Local coordinates follow the element axis. Global coordinates are fixed to the overall structure.
- The transformation matrix accounts for element orientation using sine and cosine terms.
- The assembly matrix is separate from the transformation matrix:
  - Transformation changes coordinate representation.
  - Assembly maps element quantities into structural degree-of-freedom locations.
- Assembly matrices contain zeros and ones. Their non-zero positions encode connectivity.
- An all-zero assembly-matrix column indicates an element degree of freedom associated with a constrained structural direction.
- An all-zero row indicates that the element has no direct connection to that global degree of freedom.
- The global stiffness matrix includes element properties, geometry, orientations, connectivity, and supports.
- Solving the global system gives the unknown structural displacements. Element forces, strains, stresses, and reactions are obtained during post-processing.
- Free-body diagrams are required to interpret force signs and check whether results are physically plausible.
- Reversing an element’s node order changes intermediate matrices and local quantities, but not the final physical response if all mappings and signs are updated consistently.
- Global force components are useful for combining reactions from differently oriented elements. Local axial forces are useful for calculating bar stress and sizing.
- Pin supports constrain both planar translations. A roller constrains one direction while allowing movement in the other, according to the support orientation.
- Linear shape functions give a linearly varying internal displacement for the bar element.
- The finite-element workflow remains applicable when extending to elements with bending moments and shear, although the degrees of freedom and matrices become more complex.

## Equations and worked patterns

For a two-node bar element with local coordinate \(x\) measured from node 1 to node 2:

\[
N_1(x)=1-\frac{x}{L},\qquad
N_2(x)=\frac{x}{L}
\]

The interpolated axial displacement is:

\[
u(x)=N_1(x)d_1+N_2(x)d_2
\]

At the midpoint:

\[
u\left(\frac{L}{2}\right)=\frac{d_1+d_2}{2}
\]

The axial strain is:

\[
\varepsilon=\frac{du}{dx}
=\frac{d_2-d_1}{L}
\]

Equivalently:

\[
\varepsilon=\frac{\Delta L}{L}
\]

Positive strain represents extension or tension. Negative strain represents shortening or compression.

For a linearly elastic bar:

\[
\sigma=E\varepsilon
\]

The local element stiffness matrix is:

\[
\mathbf{k}^{(e)}
=
\frac{EA}{L}
\begin{bmatrix}
1 & -1\\
-1 & 1
\end{bmatrix}
\]

The local element equation is:

\[
\mathbf{f}^{(e)}
=
\mathbf{k}^{(e)}\mathbf{d}^{(e)}
\]

For an inclined two-dimensional element, the global stiffness matrix is formed from the transformation matrix:

\[
\mathbf{K}^{(e)}
=
\boldsymbol{\Lambda}^{T}
\mathbf{k}^{(e)}
\boldsymbol{\Lambda}
\]

The assembly process is:

\[
\mathbf{K}_{g,e}
=
\mathbf{A}_e
\widehat{\mathbf{k}}_e
\mathbf{A}_e^T
\]

\[
\mathbf{K}_g
=
\sum_e
\mathbf{A}_e
\widehat{\mathbf{k}}_e
\mathbf{A}_e^T
\]

The global force vector is assembled as:

\[
\mathbf{Q}
=
\sum_e
\mathbf{A}_e\widehat{\mathbf{f}}_e
\]

The structural system has the form:

\[
\mathbf{K}_g\mathbf{q}
=
\mathbf{Q}
\]

Element displacement extraction follows the assembly mapping:

\[
\mathbf{d}_e
=
\mathbf{A}_e^T\mathbf{q}
\]

Element forces can then be recovered using:

\[
\widehat{\mathbf{f}}_e
=
\widehat{\mathbf{k}}_e
\mathbf{A}_e^T\mathbf{q}
\]

For a hollow circular section:

\[
A=\frac{\pi}{4}\left(D_o^2-D_i^2\right),
\qquad
D_i=D_o-2t
\]

A reliable worked pattern is:

1. Define geometry, material, and cross-sectional properties.
2. Assign allowable structural degrees of freedom from the supports.
3. Define each element’s local stiffness matrix.
4. Define element orientations and transformation matrices.
5. Transform element matrices into global coordinates.
6. Construct assembly matrices from connectivity.
7. Assemble the global stiffness and force vectors.
8. Solve for global nodal displacements.
9. Extract element displacements.
10. Calculate element forces, strains, stresses, and support reactions.
11. Check equilibrium, support constraints, signs, and the deformed shape.

For a square-grid diagonal with equal horizontal and vertical dimensions \(a\):

\[
L_{\text{diagonal}}
=
\sqrt{a^2+a^2}
=
a\sqrt{2}
\]

## Warnings and deadlines

- No deadlines or assessment dates were stated in the four source summaries.
- Degree-of-freedom numbering must be based on possible structural motion and support constraints, not only on the particular load case.
- A free or insufficiently constrained structure can produce a singular global stiffness system.
- Transformation and assembly matrices must use consistent element orientation, node ordering, global numbering, and sign conventions.
- A non-zero displacement at a fixed support indicates an error in the boundary conditions, degree-of-freedom numbering, transformation, assembly, or vector extraction.
- A reaction in a direction that a support cannot resist is a major warning sign.
- Element-force signs must be interpreted using the local coordinate system and a free-body diagram; the sign alone is not sufficient.
- Angles supplied in degrees must be converted to radians before use with Python trigonometric functions.
- Use one consistent magnification factor for all nodes and directions when plotting deformation. Magnification changes only the visualisation.
- Matrix dimensions alone may not detect errors when different matrices happen to be dimensionally compatible. Check the physical meaning of the entries and the resulting equilibrium.
- The summaries contain inconsistent notation in places for local/global displacement and force vectors. Confirm the course’s exact symbols and ordering before assessed calculations or coding.
- Numerical values from illustrative worked examples should be checked against the corresponding course diagrams and notes before reuse.

## Recall questions

1. What limitations of the work-energy method motivated the use of virtual displacement?
2. How does the weak form differ from the strong form of the governing equation?
3. Why is integration by parts used in the bar-element derivation?
4. What physical deformation can a two-node axial bar element represent, and which degrees of freedom does it omit?
5. Write the two linear shape functions and explain their values at the two nodes.
6. How is the global element stiffness matrix obtained from the local stiffness matrix?
7. What is the difference between a transformation matrix and an assembly matrix?
8. What do the zero and non-zero entries of an assembly matrix represent?
9. Why can the global stiffness matrix be singular?
10. How are element forces, strains, stresses, and support reactions obtained after solving the global displacement system?

## Practice priorities

1. Derive the local \(2\times2\) bar stiffness matrix from the linear shape functions.
2. Practise assigning structural degrees of freedom from pin and roller support conditions.
3. Construct transformation matrices for horizontal, vertical, reversed, and inclined elements.
4. Assemble a multi-element global stiffness matrix using element connectivity.
5. Solve the global system and extract each element’s displacement vector.
6. Calculate local axial strain and stress from the relative displacement of the element ends.
7. Interpret equal-and-opposite element-end forces as tension or compression using free-body diagrams.
8. Check support reactions and nodal force equilibrium in global coordinates.
9. Verify midpoint displacement using the shape-function interpolation.
10. Implement the workflow with reusable element functions, consistent radian angles, matrix operations, and a single deformation magnification factor.

## Missing or incomplete

None. All lectures identified for 2026-W30, Lectures 5–8, were covered.

## Source manifest

- Lecture 5 (echo-lecture-5-5): complete; summary `2f0a220270f6cf76c5f2ea3122454396a280ef423504965cd8c66cb0986fc13a`; transcript `f74ea90f63fd7e849c70c44aec0f7cbbe8576f5dea8e49127cdaa530b8df2c31`; summary path `[local source path redacted]`
- Lecture 6 (echo-lecture-6-6): complete; summary `f6914586bd08ced9c04f3e32074af53d49b1c9cfd968afccf03eeae363a358ba`; transcript `5c1cc5d0fd40e9f4584f93f789913f7fe4560b57bae0b845e1fd18f1360d8ab4`; summary path `[local source path redacted]`
- Lecture 7 (echo-lecture-7-7): complete; summary `fc511e7e302eb6e8bdc2a5512ad9ae81810f02bc6ea52fae7e47a289e08f78bb`; transcript `ef8be63a5e990258aa1b573f86b319c8435ffbfc59500f375684c2a7772ee5ea`; summary path `[local source path redacted]`
- Lecture 8 (echo-lecture-8-8): complete; summary `b52bda88ff7e7e1ecd67ed990ad5ba97323bb31aa9bdc9fdb870ae788b2ca0f2`; transcript `0625f492958f4f7cdfbf41fe3ec5b3a6e511503c48bef10fdc1af8a9cb670f5f`; summary path `[local source path redacted]`
