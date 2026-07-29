<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-30T10:28:08.955542+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Source reviewed: verified Lecture 9 summary.
- Lecture 9 covered the finite-element formulation of a two-node Euler–Bernoulli beam element.
- Weekly window: 2026-07-27T00:00:00+12:00 to 2026-07-30T10:27:19.060131+12:00.
- Lectures 10 and 11 were identified as missing summaries and are not represented below.

## Main concepts

- Beam elements extend the axial-bar finite-element workflow to transverse displacement, rotation, shear force, and bending moment.
- The initial beam formulation excludes axial deformation and uses four local degrees of freedom:
  - \(D_1=v_1\): transverse displacement at node 1
  - \(D_2=\theta_1\): rotation at node 1
  - \(D_3=v_2\): transverse displacement at node 2
  - \(D_4=\theta_2\): rotation at node 2
- The local degree-of-freedom sequence is transverse displacement, rotation, transverse displacement, rotation.
- Euler–Bernoulli theory assumes:
  - A slender, prismatic beam
  - Homogeneous material with constant \(E\)
  - Constant cross-sectional properties and second moment of area \(I\)
  - Small deflections and rotations
  - Negligible shear deformation
- A length-to-cross-sectional-dimension ratio of approximately \(5\text{–}10\) or greater is given as a rule of thumb for neglecting shear deformation. The stated less-than-approximately-1% error is not universal.
- Short or squat beams may require a Timoshenko beam element to model shear deformation.
- The beam strong form contains higher derivatives than the axial-bar formulation, so integration by parts is applied twice in the weak-form derivation.
- Four cubic shape functions interpolate the transverse displacement from the four nodal degrees of freedom.
- Shape functions are derived through unit nodal displacement or rotation cases.
- One cubic beam element can represent only a restricted family of deformation shapes. More complex profiles can be approximated with multiple elements or represented with higher-order elements.
- The complete beam stiffness-matrix derivation was not finished in the lecture.

## Equations and worked patterns

- Local displacement vector:
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
- Transverse displacement interpolation:
  \[
  v(x)=\mathbf{N}(x)\mathbf{D}
  \]
  where \(\mathbf{N}(x)\) contains four shape functions.
- Expanded interpolation:
  \[
  v(x)=N_1(x)D_1+N_2(x)D_2+N_3(x)D_3+N_4(x)D_4
  \]
- General shape-function form:
  \[
  N_i(x)=A_i x^3+B_i x^2+C_i x+D_i
  \]
- Beam slope:
  \[
  \theta(x)=\frac{\mathrm{d}v}{\mathrm{d}x}
  \]
- Beam curvature:
  \[
  \kappa(x)=\frac{\mathrm{d}^2v}{\mathrm{d}x^2}
  \]
- Moment–curvature relationship under the stated convention:
  \[
  M=EI\frac{\mathrm{d}^2v}{\mathrm{d}x^2}
  \]
- The summary gives the shear and distributed-load relationships only up to convention-dependent signs:
  \[
  V\sim EI\frac{\mathrm{d}^3v}{\mathrm{d}x^3}
  \]
  \[
  w(x)\sim EI\frac{\mathrm{d}^4v}{\mathrm{d}x^4}
  \]
- Initial shape-function derivation:
  \[
  w(x)=0
  \]
- End displacement and slope conditions:
  \[
  v(0)=D_1,\qquad
  \frac{\mathrm{d}v}{\mathrm{d}x}(0)=D_2
  \]
  \[
  v(L)=D_3,\qquad
  \frac{\mathrm{d}v}{\mathrm{d}x}(L)=D_4
  \]
- Worked unit-rotation pattern for the \(D_2\) shape function:
  \[
  D_2=1,\qquad D_1=D_3=D_4=0
  \]
  giving:
  \[
  N_2(0)=0,\qquad
  \frac{\mathrm{d}N_2}{\mathrm{d}x}(0)=1,\qquad
  N_2(L)=0,\qquad
  \frac{\mathrm{d}N_2}{\mathrm{d}x}(L)=0
  \]
- The exact signs in equilibrium relations and the final explicit shape-function expressions should be checked against the lecture slides or course notes.

## Warnings and deadlines

- No deadlines were present in the reviewed source.
- Do not treat the \(5\text{–}10\) aspect-ratio guideline or approximate 1% error statement as a universal validity criterion.
- Sign conventions for \(V\), \(M\), and the fourth-order beam equation were not unambiguously recoverable.
- The exact ordering and signs of the nodal force and moment vector were not fully reliable in the source summary.
- The final explicit expressions for all four beam shape functions were not clearly captured.
- The non-zero distributed-load case and the combined axial-and-bending formulation were deferred or not covered in this lecture.

## Recall questions

1. What four local degrees of freedom does the two-node beam element use?
2. Why are axial degrees of freedom omitted from the initial beam formulation?
3. What assumptions make Euler–Bernoulli beam theory appropriate?
4. Why does shear deformation become important in short or squat beams?
5. What beam element formulation is suitable when shear deformation cannot be neglected?
6. What physical quantities are represented by \(\mathrm{d}v/\mathrm{d}x\) and \(\mathrm{d}^2v/\mathrm{d}x^2\)?
7. Why does the beam weak-form derivation require integration by parts twice?
8. Why are four shape functions required for this beam element?
9. What boundary conditions define the unit-rotation shape function associated with \(D_2\)?
10. How can multiple simple beam elements represent a deformation profile that one element cannot capture?

## Practice priorities

- Be able to identify and order the four beam degrees of freedom.
- State the Euler–Bernoulli assumptions and explain when a Timoshenko element is needed.
- Reconstruct the chain from transverse displacement to slope, curvature, bending moment, shear force, and distributed load.
- Practise setting up the four unit nodal displacement or rotation cases.
- Practise applying four displacement and slope boundary conditions to a cubic polynomial.
- Understand the meaning of \(v(x)=\mathbf{N}(x)\mathbf{D}\) as finite-element interpolation.
- Review the weak-form logic, especially why higher derivatives lead to two integrations by parts.
- Verify sign conventions, nodal force ordering, and explicit shape-function formulas from the official lecture material before using them in calculations.
- Compare mesh refinement with higher-order elements as alternative ways to represent more complex deformation profiles.

## Missing or incomplete

- Lecture 10: missing summary.
- Lecture 11: missing summary.
- Lecture 9 did not complete the full beam stiffness-matrix derivation.
- Lecture 9 did not provide reliably recoverable final explicit expressions for all four shape functions.
- The exact sign conventions for equilibrium and end-force relationships remain unresolved from the available source.

## Source manifest

- Lecture 9 (echo-lecture-9-9): complete; summary `1e662d43de9e25ff51ec7f8e102f8b1a68ca85692c4feed1690d32778b2421e4`; transcript `81778e30d402b2b4cdde588f61d06ab037b24a16a59c6bff2a1206d68a4cc171`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_09_summary.md`
- Lecture 10 (echo-lecture-10-10): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
- Lecture 11 (echo-lecture-11-11): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
