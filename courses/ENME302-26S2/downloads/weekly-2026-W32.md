<!-- week-id: 2026-W32 -->
<!-- generated-at: 2026-08-13T12:49:23.399954+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Lecture 13: Equivalent nodal loading for distributed, concentrated transverse, and axial loads; local-to-global transformation; assembly; bridge-deck loading example.
- Lecture 14: FEA foundations, determinate and indeterminate structures, element types, shape functions, supports, and the mechanics basis of beam and truss analysis.
- Lecture 15: Assembly matrices, boundary conditions, displacement magnification, lost loads, ghost loads, and support-reaction calculations.
- Lecture 16: Assembly for connected elements, modelling pin joints with independent rotations, element classifications, static and dynamic formulations, three-dimensional frames, linear-elastic limitations, Timoshenko beams, and nonlinear structural applications.

## Main concepts

- Equivalent nodal loading allows distributed or internal point loads to be represented by nodal forces and moments without deriving a new stiffness matrix for every load profile.
- Distributed loads are integrated using element shape functions, transformed from local to global coordinates, and assembled into the global load vector.
- The stiffness matrix and structural connectivity are unchanged when distributed loading is introduced; the load side of the system is extended.
- Assembly matrices encode element connectivity, active degrees of freedom, and support constraints.
- A global stiffness contribution is formed by extracting element terms and placing them in the correct global rows and columns.
- A statically determinate structure can be solved using equilibrium alone. A statically indeterminate structure also requires compatibility and stiffness information.
- Shape functions interpolate displacement or other field variables between discrete nodal values.
- Bar elements carry axial force only. Beam elements represent transverse shear and bending behaviour. Frame elements can represent axial force, shear force, and bending moment.
- A pin joint shares translations but permits independent rotations. This requires an additional rotational degree of freedom when represented within a frame-element model.
- Lost loads or ghost loads occur when equivalent nodal loads act at constrained support degrees of freedom and therefore disappear from the active global load vector.
- Support reactions must account for both elastic element forces and equivalent loads applied directly to constrained supports.
- Displacement magnification changes only the plotted deformation, not the solved displacement.
- The course formulation is linear elastic and does not automatically detect yielding, material failure, or buckling.
- Timoshenko beam elements include shear deformation, which is more significant in short or deep beams than in slender beams.
- The same assembly principles extend from static analysis to dynamic analysis and from two-dimensional to three-dimensional models.

## Equations and worked patterns

- Equivalent transverse nodal loading:

  \[
  f_{\mathrm{eq}}^{(e)}
  =
  \int_0^L N^T(X)W(X)\,dX
  \]

- Equivalent axial nodal loading:

  \[
  f_{\mathrm{eq,axial}}^{(e)}
  =
  \int_0^L \psi^T(X)P(X)\,dX
  \]

- Local-to-global transformation and assembly:

  \[
  F_{\mathrm{eq}}^{(e)}=T^T f_{\mathrm{eq}}^{(e)}
  \]

  \[
  Q_{\mathrm{eq}}^{(e)}=A^{(e)}F_{\mathrm{eq}}^{(e)}
  \]

- Extended structural equilibrium:

  \[
  KD=Q+Q_{\mathrm{eq}}
  \]

- Uniformly distributed load:

  \[
  W(X)=\overline{W}
  \]

  Total resultant:

  \[
  F_{\mathrm{total}}=\overline{W}L
  \]

- Linearly varying load, zero at node 1:

  \[
  W(X)=\overline{W}\frac{X}{L}
  \]

  The equivalent shear-force components are:

  \[
  \frac{3\overline{W}L}{20}
  \quad\text{and}\quad
  \frac{7\overline{W}L}{20}
  \]

  Their sum is:

  \[
  \frac{\overline{W}L}{2}
  \]

- Concentrated transverse load at position \(A\):

  \[
  W(X)=\overline{W}\delta(X-A)
  \]

- Concentrated axial loading uses position factors:

  \[
  1-\frac{A}{L}
  \quad\text{and}\quad
  \frac{A}{L}
  \]

- Global stiffness assembly for one element and the complete structure:

  \[
  K_G^{(e)}=A_e\hat{K}_eA_e^T
  \]

  \[
  K_G=\sum_e A_e\hat{K}_eA_e^T
  \]

- Static and dynamic equations:

  \[
  KQ=F
  \]

  \[
  M\ddot{Q}+C\dot{Q}+KQ=F
  \]

- Lost-load reaction correction:

  \[
  R_{\mathrm{total}}
  =
  R_{\mathrm{elastic}}-f_{\mathrm{support}}
  \]

  The exact signs depend on the adopted force and reaction convention.

- Uniform-load equilibrium pattern:

  \[
  W=\bar{w}L
  \]

  For a full-length uniform load, the resultant acts at \(L/2\). A support reaction and moment can then be checked using:

  \[
  R=W
  \]

  \[
  M_R=Wx
  \]

- Cable-force resolution from the worked pattern:

  \[
  T_x=500\left(\frac{3}{5}\right)=300\ \mathrm{N}
  \]

  \[
  T_y=500\left(\frac{4}{5}\right)=400\ \mathrm{N}
  \]

  The horizontal component contributes to axial loading; the vertical component contributes to shear and bending.

- Pin-jointed inclined-member example:

  \[
  F_{\mathrm{inclined\ member}}\approx333.3\ \mathrm{kN}
  \]

  in compression, with the stated vertical reaction:

  \[
  R_{Cy}=100\ \mathrm{kN}
  \]

## Warnings and deadlines

- No deadlines or assessment dates are stated in the four source summaries.
- Lecture 13 does not capture the complete UDL equivalent-load vector coefficients, and some linearly varying-load moment coefficients and signs are also unclear. Verify those values against the course material before using them.
- The bridge-deck worked example in Lecture 13 is explicitly unfinished in that lecture.
- Check local and global sign conventions carefully, especially when reversing element orientation or applying downward loads.
- A difference between the number of non-zero element-load terms and global-load terms may indicate lost loads at constrained supports.
- Do not interpret displacement-magnified plots as true-scale deformation.
- The basic linear-elastic model does not warn about yielding, excessive stress, or buckling.
- The detailed beam transformation matrix and exact degree-of-freedom ordering were not identified as major assessment targets, but the underlying connectivity principles remain important.

## Recall questions

1. Why is equivalent nodal loading preferred to deriving a new element formulation for every distributed-load profile?
2. How are local equivalent element loads transformed and assembled into the global structural load vector?
3. What is the difference between a statically determinate and a statically indeterminate structure?
4. What information does an assembly matrix encode?
5. Why is the stiffness matrix of a completely unconstrained frame element singular?
6. Under what conditions do lost loads or ghost loads arise?
7. Why must support reactions include loads applied directly to constrained support degrees of freedom?
8. How should a pin joint be represented when connected elements must share translations but rotate independently?
9. What are the principal behavioural differences between bar, beam, and frame elements?
10. What limitations follow from using a linear-elastic finite-element model?

## Practice priorities

1. Derive and assemble equivalent nodal loads for UDLs, triangular loads, and internal point loads.
2. Practise checking equivalent nodal forces against the total applied resultant and expected load distribution.
3. Build assembly matrices from element-to-global degree-of-freedom mappings.
4. Reduce a constrained system and compare it conceptually with enforcing supports by overwriting equations.
5. Work through a distributed-load example where one element node is fixed, identify the lost loads, and correct the support reactions.
6. Model a pin-connected member inside a frame structure by adding an independent rotational degree of freedom.
7. Check frame, beam, and bar load vectors for correct zero entries and degree-of-freedom placement.
8. Verify finite-element reactions against whole-structure equilibrium.
9. Review the distinction between static \(KQ=F\) and dynamic \(M\ddot{Q}+C\dot{Q}+KQ=F\) formulations.
10. Practise identifying when shear deformation, nonlinear material behaviour, or buckling would make the basic course model inadequate.

## Missing or incomplete

- No lectures are missing or incomplete for this weekly coverage.
- Some exact displayed coefficients, signs, matrix layouts, and degree-of-freedom orderings are not fully recoverable from the source summaries.

## Source manifest

- Lecture 13 (echo-lecture-13-13): complete; summary `13a70e407d95c729b30f20204250d9391cab4f88b8ea0077d9fd2f6d000a088f`; transcript `889bc88e0f9a5b20bc56139e9db9aaf33d5803aca1a490f87dbdbe8d711c5426`; summary path `[local source path redacted]`
- Lecture 14 (echo-lecture-14-14): complete; summary `10b1b39170ba508fe8dd6ec43cac293ecd9cddfb5fefa5a38e72c0271d49ad6a`; transcript `b82ab49cc20590cb76ca38685dc389816a824ac22387893c2b11f6e696e47e67`; summary path `[local source path redacted]`
- Lecture 15 (echo-lecture-15-15): complete; summary `05d04f8aa8b6c1cdc9511a075229febd8af9dc14583863c898f001b3ad08d381`; transcript `b1a16c7824db87cdc4aa8fe09fc2756695e1aba3ba636ae77487b1ac08ab1d6e`; summary path `[local source path redacted]`
- Lecture 16 (echo-lecture-16-16): complete; summary `fb14394fc6013e5c5a52f304023b6c15010c638223be11ec257c09a07a890f6b`; transcript `7a8d90ea543f2c50e56782ca8798c0634153a0f13c2b6767d00a1f43fdcd20f0`; summary path `[local source path redacted]`
