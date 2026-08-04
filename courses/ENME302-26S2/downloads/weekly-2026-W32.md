<!-- week-id: 2026-W32 -->
<!-- generated-at: 2026-08-05T11:14:32.005130+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Study window: 2026-08-03T00:00:00+12:00 to 2026-08-05T11:13:38.617864+12:00.
- Sources covered:
  - Lecture 13: equivalent nodal loading for distributed and concentrated loads.
  - Lecture 14: course framework, structural determinacy, finite-element modelling, element types, shape functions, and foundational beam/truss mechanics.
- No lectures were identified as missing or incomplete.

## Main concepts

- Equivalent nodal loading converts distributed loads into element nodal forces and moments, allowing existing stiffness formulations to be reused.
- Distributed loads are introduced on the load side of the finite-element equation. The stiffness matrix and structural connectivity remain unchanged.
- Equivalent loads are calculated in local element coordinates, transformed to global coordinates, and assembled into the global structural load vector.
- Uniformly distributed, linearly varying, concentrated transverse, distributed axial, and concentrated axial loads can all be represented using shape functions.
- Linearly varying loads require careful attention to element orientation because the load intensity depends on which node corresponds to \(X=0\) and \(X=L\).
- Transverse beam load vectors are embedded into frame vectors by inserting zeros in the axial-force positions.
- Axial bar load vectors are embedded into frame vectors by inserting zeros in the transverse-force and moment positions.
- The simplified formulation treats axial and flexural behaviour independently, with no axial-flexural coupling.
- Statically determinate structures can be solved using equilibrium alone.
- Statically indeterminate structures require equilibrium, compatibility, constitutive relationships, and member stiffness.
- Ideal pin-jointed truss members carry axial tension or compression only. Rigidly connected members can also carry shear and bending moment.
- Finite element analysis represents a complex continuous structure using simpler elements connected at nodes.
- Shape functions interpolate displacement or other field variables between discrete nodal points.
- Element choice should match the physical behaviour being modelled. Greater model dimensionality is not automatically better.
- The general FEA workflow is to define nodes and degrees of freedom, formulate elements, orient and assemble them, apply supports and loads, solve for nodal quantities, and recover element responses.

## Equations and worked patterns

- Distributed transverse load:
  \[
  f_{\mathrm{eq}}^{(e)}=\int_0^L N^T(X)W(X)\,dX
  \]

- Distributed axial load:
  \[
  f_{\mathrm{eq,axial}}^{(e)}=\int_0^L \psi^T(X)P(X)\,dX
  \]

- Conceptual transformation and assembly:
  \[
  F_{\mathrm{eq}}^{(e)}=T^T f_{\mathrm{eq}}^{(e)}
  \]
  followed by
  \[
  Q_{\mathrm{eq}}^{(e)}=A^{(e)}F_{\mathrm{eq}}^{(e)}
  \]

- Global equilibrium with equivalent loads:
  \[
  KD=Q+Q_{\mathrm{eq}}
  \]

- Uniformly distributed transverse load:
  \[
  W(X)=\overline{W}
  \]
  with total resultant:
  \[
  F_{\mathrm{total}}=\overline{W}L
  \]

- Linearly varying load with zero intensity at node 1:
  \[
  W(X)=\overline{W}\frac{X}{L}
  \]
  Its total resultant is:
  \[
  F_{\mathrm{total}}=\frac{\overline{W}L}{2}
  \]
  and the equivalent nodal shear-force components identified in Lecture 13 are:
  \[
  \frac{3\overline{W}L}{20},\qquad
  \frac{7\overline{W}L}{20}
  \]

- Reversed linearly varying load:
  \[
  W(X)=\overline{W}\left(1-\frac{X}{L}\right)
  \]
  The larger equivalent nodal shear force is associated with node 1.

- Concentrated transverse load at \(X=A\):
  \[
  W(X)=\overline{W}\delta(X-A)
  \]

- Concentrated axial load position factors:
  \[
  1-\frac{A}{L},\qquad \frac{A}{L}
  \]

- Normal stress:
  \[
  \sigma=\frac{N}{A}
  \]

- Circular hollow-section area:
  \[
  A=\frac{\pi}{4}(D^2-d^2),\qquad d=D-2t
  \]

- Tip-loaded cantilever moment:
  \[
  M(x)=-P(L-x)
  \]

- Tip-loaded cantilever magnitudes:
  \[
  \delta_{\mathrm{tip}}=\frac{PL^3}{3EI}
  \]
  \[
  \theta_{\mathrm{tip}}=\frac{PL^2}{2EI}
  \]

- Bridge-deck worked pattern from Lecture 13:
  - Apply the UDL equivalent-load vector in local coordinates.
  - Use \(\overline{W}=-10\ \mathrm{kN/m}\) for the downward self-weight.
  - Use \(L=4.5\ \mathrm{m}\).
  - Transform to global coordinates.
  - Assemble into the structural load vector.
  - Add the \(50\ \mathrm{kN}\) concentrated truck load.
  - Solve using the unchanged global stiffness matrix.
  - In the stated \(0^\circ\) orientation and selected assembly, the transformation and assembly matrices are identities.

## Warnings and deadlines

- No deadlines or assessment dates were stated in the two source files.
- Do not use the equivalent-load coefficients for a linearly varying load without first checking which node has the higher load intensity.
- Downward loading may require a negative \(\overline{W}\), depending on the local-coordinate sign convention.
- The transformation and assembly steps are still required in general, even though they reduce to identity operations in the bridge-deck example.
- The automated transcript does not reliably capture all signs and moment coefficients for the linearly varying transverse-load vectors. Verify those values against the course lecture material before using them in assessed work.
- Lecture 13 states that the bridge-deck example was not completed within that lecture.

## Recall questions

1. Why is equivalent nodal loading preferred to deriving a new finite element for every distributed-load profile?
2. What changes in the global finite-element equation when distributed loading is introduced?
3. What is the general equivalent-load integral for a distributed transverse load?
4. Why does element orientation matter for a linearly varying distributed load?
5. How can a concentrated transverse load inside an element be represented without adding a node?
6. What is the difference between a statically determinate and a statically indeterminate structure?
7. Why does relative stiffness affect load distribution in a statically indeterminate structure?
8. What physical behaviours can an ideal pin-jointed truss member carry, and which does it exclude?
9. What role do shape functions play between finite-element nodes?
10. What sequence of local-load transformation and assembly operations is used before solving the global system?

## Practice priorities

1. Derive and apply equivalent nodal loads for uniform transverse loading.
2. Check that equivalent nodal forces reproduce the total resultant load.
3. Practise both orientations of a linearly varying load and track the sign convention.
4. Formulate a concentrated transverse load using the Dirac delta representation.
5. Embed beam and bar load vectors correctly into six-degree-of-freedom frame vectors.
6. Practise local-to-global transformation and global assembly for an element that is not aligned with the global axes.
7. Distinguish determinate and indeterminate structures, identifying when stiffness and compatibility are required.
8. Review the FEA workflow from element definition through global solution and element-force recovery.
9. Rework the cantilever relationships for moment, tip deflection, and tip rotation.
10. Review axial stress and hollow-section area calculations using consistent units.

## Missing or incomplete

None identified for the requested weekly coverage.

## Source manifest

- Lecture 13 (echo-lecture-13-13): complete; summary `13a70e407d95c729b30f20204250d9391cab4f88b8ea0077d9fd2f6d000a088f`; transcript `889bc88e0f9a5b20bc56139e9db9aaf33d5803aca1a490f87dbdbe8d711c5426`; summary path `[local source path redacted]`
- Lecture 14 (echo-lecture-14-14): complete; summary `10b1b39170ba508fe8dd6ec43cac293ecd9cddfb5fefa5a38e72c0271d49ad6a`; transcript `b82ab49cc20590cb76ca38685dc389816a824ac22387893c2b11f6e696e47e67`; summary path `[local source path redacted]`
