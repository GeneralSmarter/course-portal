<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-29T09:34:14.694791+12:00 -->
# ENME302-26S2 weekly summary

## Coverage

- Week: 2026-W31, covering 2026-07-27T00:00:00+12:00 to 2026-07-29T09:33:02.031274+12:00.
- Source available: Lecture 9 summary.
- Lecture 9 introduced the finite-element formulation of a two-node Euler–Bernoulli beam element.
- The full beam stiffness-matrix derivation was not completed in the lecture summary.

## Main concepts

- Beam elements model transverse deformation, shear forces, and bending moments. The initial formulation excludes axial deformation.
- The two-node beam element has four local degrees of freedom:
  - Transverse displacement at node 1, \(D_1=v_1\)
  - Rotation at node 1, \(D_2=\theta_1\)
  - Transverse displacement at node 2, \(D_3=v_2\)
  - Rotation at node 2, \(D_4=\theta_2\)
- The local degree-of-freedom sequence is \(Y,Z,Y,Z\), with positive rotation about the local \(z\)-axis defined as counterclockwise.
- Euler–Bernoulli beam theory assumes:
  - Plane sections remain plane.
  - Shear deformation is neglected.
  - Deflections and rotations are small.
  - The beam is slender, prismatic, homogeneous, and has constant \(E\), \(I\), and \(L\).
- A slenderness guideline of approximately \(L/B\gtrsim5\text{–}10\) was given. The stated error from neglecting shear may be less than approximately 1% for suitable aspect ratios, but this is only an approximate rule of thumb.
- Timoshenko beam elements are the appropriate extension when shear deformation is significant, such as for short or squat beams.
- The beam weak-form derivation parallels the axial-bar derivation, but integration by parts is applied twice because the beam equation contains higher derivatives.
- Four cubic shape functions interpolate the transverse displacement from the four nodal degrees of freedom.
- One element represents only a restricted family of cubic deformation shapes. More complex deformation can be captured using multiple elements or higher-order elements.

## Equations and worked patterns

- Local displacement vector:
  \[
  \mathbf{D}
  =
  \begin{bmatrix}
  D_1\\D_2\\D_3\\D_4
  \end{bmatrix}
  =
  \begin{bmatrix}
  v_1\\\theta_1\\v_2\\\theta_2
  \end{bmatrix}
  \]

- Transverse displacement interpolation:
  \[
  v(x)=\mathbf{N}(x)\mathbf{D}
  \]
  where
  \[
  \mathbf{N}(x)=
  \begin{bmatrix}
  N_1(x)&N_2(x)&N_3(x)&N_4(x)
  \end{bmatrix}
  \]

- Expanded interpolation:
  \[
  v(x)=N_1(x)D_1+N_2(x)D_2+N_3(x)D_3+N_4(x)D_4
  \]

- General shape-function form:
  \[
  N_i(x)=A_i x^3+B_i x^2+C_i x+D_i
  \]

- Slope and curvature:
  \[
  \theta(x)=\frac{\mathrm{d}v}{\mathrm{d}x}
  \]
  \[
  \kappa(x)=\frac{\mathrm{d}^2v}{\mathrm{d}x^2}
  \]

- Moment–curvature relationship:
  \[
  M=EI\frac{\mathrm{d}^2v}{\mathrm{d}x^2}
  \]
  The sign depends on the selected bending-moment and displacement convention.

- Shear and distributed-load relationships were given only up to convention-dependent signs:
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
  This produces a homogeneous beam equation and a cubic displacement field.

- End displacement and slope conditions:
  \[
  v(0)=D_1,\qquad
  \frac{\mathrm{d}v}{\mathrm{d}x}(0)=D_2
  \]
  \[
  v(L)=D_3,\qquad
  \frac{\mathrm{d}v}{\mathrm{d}x}(L)=D_4
  \]

- Worked unit-rotation pattern for \(D_2=1\), with \(D_1=D_3=D_4=0\):
  \[
  N_2(0)=0,\qquad
  \frac{\mathrm{d}N_2}{\mathrm{d}x}(0)=1
  \]
  \[
  N_2(L)=0,\qquad
  \frac{\mathrm{d}N_2}{\mathrm{d}x}(L)=0
  \]
  The summary does not reliably preserve the final explicit expressions for all four shape functions.

## Warnings and deadlines

- No deadlines or assessment dates are stated in the available Lecture 9 source.
- Do not rely on the exact signs of the equilibrium, shear-force, or end-force equations without checking the lecture slides or course notes.
- The exact ordering and signs of the nodal force and moment vector \(F_1\)–\(F_4\) are not reliably recoverable from the summary.
- The explicit final forms of the four cubic beam shape functions were not reliably captured.
- The approximately 1% shear-deflection error guideline is not a universal guarantee.
- The initial derivation assumes \(w(x)=0\); the non-zero distributed-load case is deferred.
- The combined axial-and-bending formulation is not covered in this lecture.

## Recall questions

1. What four local degrees of freedom does the two-node beam element use?
2. Why are axial degrees of freedom omitted from the initial beam-element formulation?
3. What assumptions make Euler–Bernoulli beam theory appropriate?
4. Why does shear deformation become important in short or squat beams?
5. What beam element formulation is suitable when shear deformation cannot be neglected?
6. What do the first and second derivatives of \(v(x)\) represent?
7. Why does the beam formulation require integration by parts twice?
8. How are the four shape functions generated using unit nodal displacement or rotation cases?
9. What four boundary conditions define the \(D_2=1\) unit-rotation shape function?
10. Why might multiple simple beam elements be preferred over one higher-order element?

## Practice priorities

- Memorise the four local degrees of freedom and their physical meanings.
- Check the slender-beam and small-deflection assumptions, including when Timoshenko theory is needed.
- Re-derive the relationships between \(v(x)\), slope, curvature, bending moment, shear force, and distributed load while explicitly tracking the chosen sign convention.
- Practise applying the four end displacement and slope conditions.
- Work through the unit-rotation shape-function procedure for \(D_2=1\).
- Be able to explain \(v(x)=\mathbf{N}(x)\mathbf{D}\) physically and mathematically.
- Compare mesh refinement using multiple two-node elements with the use of higher-order elements.
- Verify the explicit shape functions and nodal force/moment signs against the lecture slides before using them in calculations.

## Missing or incomplete

- Lecture 10: missing_summary.
- Lecture 9 is incomplete for:
  - The full beam stiffness-matrix derivation.
  - The explicit final expressions for all four shape functions.
  - Reliable signs and ordering for some force and moment relationships.
  - The non-zero distributed-load formulation.
  - The combined axial-and-bending formulation.

## Source manifest

- Lecture 9 (echo-lecture-9-9): complete; summary `1e662d43de9e25ff51ec7f8e102f8b1a68ca85692c4feed1690d32778b2421e4`; transcript `81778e30d402b2b4cdde588f61d06ab037b24a16a59c6bff2a1206d68a4cc171`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENME302-26S2/summaries/lecture_09_summary.md`
- Lecture 10 (echo-lecture-10-10): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
