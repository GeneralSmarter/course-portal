<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-10-20T12:19:32.657906+13:00 -->
# ENME302-26S2 weekly summary

## Coverage

Rebuilt 20 October 2026 from the corrected source-backed lecture notes. Teaching-week numbering omits the mid-semester break; ISO week identifiers are calendar dates.

- Lecture 9: 2026-07-27. Lecture 9 introduces the finite-element formulation of a beam element capable of carrying transverse shear forces and bending moments.  The lecture builds on the previously derived axial bar element:  - Bar elements model axial deformation only. - Beam elements initially model bending deformation only, with axial deformation excluded. - The beam element is assumed to be slender, prismatic, homogeneous, and governed by Euler–Bernoulli beam theory. - Each two-node beam element has four local degrees of freedom:   - Transverse displacement at node 1   - Rotation at node 1   - Transverse displacement at node 2   - Rotation at node 2 - Cubic polynomial shape functions are derived using unit nodal displacement and rotation cases. - The transverse displacement anywhere within the element is repre

- Lecture 10: 2026-07-29. - The lecture completes the derivation of the beam-element stiffness matrix and then introduces the more general two-dimensional frame element. - Main progression:   1. Review transverse beam shape functions and their assumptions.   2. Derive beam-element stiffness terms using virtual work.   3. Assemble the beam-element stiffness matrix in local coordinates.   4. Apply boundary conditions and test the element using cantilever examples.   5. Extend the beam element to a six-degree-of-freedom frame element by combining axial and flexural behaviour through linear superposition.   6. Review local-to-global coordinate transformations, assembly matrices, and implementation checks. - The beam element models transverse bending and rotation but excludes axial deformation. - The frame element inclu

- Lecture 11: 2026-07-30. This is the 30 July 2026 structural-FEA lecture, not the opening lecture. It works through a supported planar frame, its global/local displacement and force vectors, equilibrium checks, and plotting with shape functions. This Weeks 1–4 material is not part of the 2026 final's Weeks 5–12 scope.

- Lecture 12: 2026-07-31. Lecture 12 completed several frame-element examples and consolidated the interpretation of finite-element results before moving to distributed loading.  The main topics were:  - Checking equilibrium for individual frame elements and the overall structure. - Understanding how applied moments and forces are distributed between connected elements. - The effect of relative stiffness and boundary conditions on load distribution. - Correct interpretation and hand-sketching of deformed shapes. - Mapping element degrees of freedom to global structural degrees of freedom. - Constructing assembly matrices and interpreting solved displacement vectors. - Recovering element forces and support reactions. - Verifying global equilibrium using force and moment balances. - Assigning degrees of freedom for a

## Main concepts

### Lecture 9

- Beam element
  - Carries transverse shear forces and bending moments.
  - Initially excludes axial deformation.
  - Connections are rigid, so bending moments can transfer through element and support connections.

- Bar element versus beam element
  - A bar element has axial displacement degrees of freedom only.
  - A beam element has transverse displacement and rotational degrees of freedom.
  - The matrix and vector dimensions increase, but the meanings of quantities such as element stiffness, transformation matrices, and global assembly remain conceptually unchanged.

- Local element coordinates
  - The local \(x\)-axis runs from node 1 to node 2.
  - The transverse direction is \(y\).
  - The rotational degree of freedom about the \(z\)-axis is positive counterclockwise according to the stated right-hand-rule convention.

- Slender-beam assumption
  - The beam length \(L\) should be approximately 5–10 times greater than the relevant cross-sectional dimension.
  - Under this assumption, bending deflection dominates shear deflection.
  - The lecturer states that neglecting shear deflection may produce less than approximately 1% error for aspect ratios of 5–10 or greater.
  - The exact error depends on the beam and loading, so the stated percentage should be treated as an approximate rule of thumb.

- Euler–Bernoulli beam theory
  - Plane sections remain plane during bending.
  - In pure bending, beam cross-sections remain approximately perpendicular to the beam’s centreline.
  - Shear deformation is neglected.
  - The theory is therefore unsuitable for short, deep, or squat beams where shear deformation is significant.

- Small-deflection assumption
  - Deflections and rotations are assumed sufficiently small that the original geometry remains a reasonable approximation to the deformed geometry.
  - Products of infinitesimal quantities and second-order terms are neglected during equilibrium derivations.

- Strong form and weak form
  - The strong form must hold at every point along the element.
  - The weak form is obtained by multiplying the governing equation by a virtual displacement and integrating over the element.
  - Integration by parts is used twice for the beam formulation because the governing equation contains higher derivatives than the axial bar formulation.

- Shape functions
  - Shape functions interpolate the transverse displacement between nodal degrees of freedom.
  - Four shape functions are required because the beam element has four local degrees of freedom.
  - Each shape function is obtained by setting one nodal degree of freedom to one while setting the other three to zero.
  - The resulting functions are cubic polynomials.

- Unit-displacement method
  - A unit displacement or unit rotation is imposed at one degree of freedom while all other nodal degrees of freedom are held at zero.
  - The force or moment required to create that unit deformation corresponds to a stiffness coefficient.
  - This provides a mathematical method for constructing the element stiffness relationships.

- Element discretisation
  - A single cubic beam element can only produce a weighted combination of its four basis deformation shapes.
  - More complex deformation profiles can be represented by dividing the beam into multiple elements.
  - There is a trade-off between:
    - A larger number of simple elements
    - A smaller number of more complex elements with more degrees of freedom
  - More complex elements require more computation per element, while multiple simple elements increase the number of elements and global assembly operations.

### Transition from axial bars to beams

The preceding two weeks considered bar elements that were:

- Purely axial.
- Pin-jointed.
- Loaded only at nodal points.
- Unable to carry shear forces or bending moments.

Lecture 9 introduces beam elements that carry transverse shear forces and bending moments. Axial deformation is temporarily set aside so that the bending formulation can be developed independently. The lecturer states that axial and bending effects will be combined later.

Although the matrices and vectors become larger, the fundamental finite-element workflow remains the same:

1. Define element degrees of freedom.
2. Derive the element relationships.
3. Transform between local and global coordinates where required.
4. Assemble the global system.
5. Apply boundary conditions and solve.

### Beam-element assumptions

The beam is assumed to have:

- Constant shear-force treatment within the local derivation.
- Constant elastic modulus \(E\).
- Constant cross-sectional properties.
- Constant length \(L\).
- Constant second moment of area \(I\).
- A prismatic cross-section.
- Homogeneous material.
- Slender geometry.

The cross-sectional dimensions are described using dimensions labelled \(A\) and \(B\) in the transcript. The lecturer states that \(L\) should generally be greater than approximately 5–10 times dimension \(B\), or larger.

### Beam degrees of freedom

Axial deformation in the local \(x\)-direction is ignored. The local beam degrees of freedom are therefore ordered as:

\[
\mathbf{D}
=
\begin{bmatrix}
D_1\\
D_2\\
D_3\\
D_4
\end{bmatrix}
=
\begin{bmatrix}
v_1\\
\theta_1\\
v_2\\
\theta_2
\end{bmatrix}
\]

where:

- \(D_1\): transverse displacement in the \(y\)-direction at node 1.
- \(D_2\): rotation about the \(z\)-axis at node 1.
- \(D_3\): transverse displacement in the \(y\)-direction at node 2.
- \(D_4\): rotation about the \(z\)-axis at node 2.

The transcript repeatedly identifies the sequence as \(Y,Z,Y,Z\). Counterclockwise rotation about the local \(z\)-axis is positive under the stated convention.

The element has:

- Two nodes.
- Four local degrees of freedom.
- Two transverse displacement degrees of freedom.
- Two rotational degrees of freedom.

### Bending and shear components of deflection

The lecture distinguishes two mechanisms contributing to transverse deflection:

1. Bending or curvature deflection
   - Cross-sections rotate as the beam curves.
   - This is the deformation represented by Euler–Bernoulli beam theory.

2. Shear deflection
   - Cross-sections remain approximately vertical rather than remaining perpendicular to the curved centreline.
   - Small beam segments form distorted parallelograms.
   - This contribution becomes more important for short, squat beams.

For slender beams, bending deflection dominates and shear deflection can be neglected. For an aspect ratio near 2, the neglected shear contribution may be significant. A Timoshenko beam element includes additional terms to model shear deformation and is stated to be covered in the following week.

### Differential equilibrium

A differential beam segment is considered with:

- Shear force \(V\) at one end.
- Shear force \(V+\mathrm{d}V\) at the other end.
- Bending moment \(M\) at one end.
- Bending moment \(M+\mathrm{d}M\) at the other end.
- Distributed transverse load \(w(x)\) over a length \(\mathrm{d}x\).

The distributed load over the small segment is represented by an equivalent force of approximately:

\[
w(x)\,\mathrm{d}x
\]

acting at the segment midpoint, a distance \(\mathrm{d}x/2\) from either end.

Vertical force equilibrium gives the relationship between distributed transverse loading and the rate of change of internal shear force. The exact sign depends on the direction convention used in the diagram. The transcript’s verbal description indicates the standard relationship in magnitude:

\[
\frac{\mathrm{d}V}{\mathrm{d}x} \sim w(x)
\]

with the sign convention to be taken from the lecture’s diagram.

Moment equilibrium gives the relationship between shear force and the rate of change of bending moment:

\[
\frac{\mathrm{d}M}{\mathrm{d}x} \sim V
\]

Again, the exact sign is convention-dependent and is not unambiguously recoverable from the automated transcript.

### Moment–curvature relationship

The lecture states the Euler–Bernoulli moment–curvature relationship as:

\[
M = EI\frac{\mathrm{d}^2v}{\mathrm{d}x^2}
\]

where:

- \(M\) is bending moment.
- \(E\) is elastic modulus.
- \(I\) is the second moment of area.
- \(v(x)\) is transverse deflection.
- \(\mathrm{d}^2v/\mathrm{d}x^2\) is beam curvature under the stated sign convention.

The first derivative of transverse deflection is the beam slope:

\[
\frac{\mathrm{d}v}{\mathrm{d}x}
\]

The second derivative is curvature:

\[
\frac{\mathrm{d}^2v}{\mathrm{d}x^2}
\]

Differentiating the moment–curvature equation relates shear force to the third derivative of transverse displacement:

\[
V \sim EI\frac{\mathrm{d}^3v}{\mathrm{d}x^3}
\]

The transcript appears to use this relationship when defining the nodal shear-force boundary conditions.

Combining equilibrium and the moment–curvature relationship produces a fourth-order beam differential equation involving the distributed transverse load:

\[
w(x) \sim EI\frac{\mathrm{d}^4v}{\mathrm{d}x^4}
\]

The sign is convention-dependent and cannot be confirmed reliably from the automated transcript.

### Initial zero-distributed-load assumption

For the initial shape-function derivation, the externally distributed transverse load is set to zero:

\[
w(x)=0
\]

This simplifies the governing equation and allows the interpolation functions to be derived from nodal boundary conditions. The lecturer states that the non-zero distributed-load case will be revisited later.

With \(w(x)=0\), the beam’s internal shear force and bending moment vary according to the homogeneous beam equation, leading to a cubic displacement field.

### Boundary conditions

The four boundary conditions correspond to the two force quantities and two displacement quantities at the two nodes.

At each node, the beam has:

- A transverse displacement.
- A rotation.
- A shear-force-related condition.
- A bending-moment-related condition.

The transcript describes the following relationships, with signs dependent on the local convention:

\[
EI\frac{\mathrm{d}^3v}{\mathrm{d}x^3}
\]

evaluated at the ends gives the nodal shear-force quantities, while:

\[
EI\frac{\mathrm{d}^2v}{\mathrm{d}x^2}
\]

evaluated at the ends gives the nodal bending-moment quantities.

The displacement and slope conditions are:

\[
v(0)=D_1
\]

\[
\frac{\mathrm{d}v}{\mathrm{d}x}(0)=D_2
\]

\[
v(L)=D_3
\]

\[
\frac{\mathrm{d}v}{\mathrm{d}x}(L)=D_4
\]

The transcript uses \(F_1\) through \(F_4\) for nodal force and moment quantities, but the precise sign and ordering of the force vector are not fully clear because of transcription errors.

### Weak-form derivation

The beam governing equation is multiplied by a virtual displacement and integrated over the element. This introduces internal virtual work and leads to the weak form.

Compared with the bar derivation:

- The beam equation contains higher-order derivatives.
- Integration by parts is applied twice rather than once.
- Boundary terms appear that correspond to nodal shear forces and bending moments.
- The resulting expression contains the internal bending contribution and the nodal virtual work terms.

The lecturer emphasises that the procedure parallels the axial bar derivation, even though the beam formulation involves more derivatives and more degrees of freedom.

### Cubic polynomial interpolation

The transverse displacement is assumed to be expressible as:

\[
v(x)=\mathbf{N}(x)\mathbf{D}
\]

where:

\[
\mathbf{N}(x)
=
\begin{bmatrix}
N_1(x) & N_2(x) & N_3(x) & N_4(x)
\end{bmatrix}
\]

and:

\[
\mathbf{D}
=
\begin{bmatrix}
D_1\\
D_2\\
D_3\\
D_4
\end{bmatrix}
\]

Thus:

\[
v(x)
=
N_1(x)D_1
+
N_2(x)D_2
+
N_3(x)D_3
+
N_4(x)D_4
\]

Each shape function is a cubic polynomial of the general form:

\[
N_i(x)=A_i x^3+B_i x^2+C_i x+D_i
\]

The coefficients are determined separately for each shape function using four boundary conditions.

The transcript does not clearly capture the lecturer’s final explicit expressions for all four \(N_i(x)\). Their standard cubic Hermite form is therefore not reproduced here as if it had been explicitly present in the transcript.

### Unit shape-function cases

The four shape functions are generated systematically:

- \(D_1=1\), with \(D_2=D_3=D_4=0\)
  - Unit transverse displacement at node 1.

- \(D_2=1\), with \(D_1=D_3=D_4=0\)
  - Unit rotation at node 1.

- \(D_3=1\), with \(D_1=D_2=D_4=0\)
  - Unit transverse displacement at node 2.

- \(D_4=1\), with \(D_1=D_2=D_3=0\)
  - Unit rotation at node 2.

For the worked example involving \(D_2=1\), the boundary conditions stated in the transcript are:

\[
N_2(0)=0
\]

\[
\frac{\mathrm{d}N_2}{\mathrm{d}x}(0)=1
\]

\[
N_2(L)=0
\]

\[
\frac{\mathrm{d}N_2}{\mathrm{d}x}(L)=0
\]

These conditions ensure that the second shape function represents a unit rotation at node 1 while all other nodal displacement and rotation values remain zero.

The first two conditions directly determine two polynomial coefficients. The remaining two conditions, evaluated at \(x=L\), determine the other two coefficients.

### Meaning of the interpolation

Once the four shape functions have been determined, the displacement at any location \(x\) along the beam can be obtained from only the four nodal degrees of freedom:

\[
v(x)=\mathbf{N}(x)\mathbf{D}
\]

This is a major finite-element simplification: the continuous displacement field is reconstructed from a finite set of nodal values.

The possible deformation shapes of one element are restricted to weighted sums of the four basis functions. Consequently, one element cannot represent an arbitrary deformation profile.

### Mesh refinement and higher-order elements

If a beam has a deformation profile that cannot be represented by one cubic element, the beam can be divided into multiple elements. Each element then represents a simpler local portion of the overall shape.

The lecture also mentions a more complex element with:

- Three nodes.
- Six degrees of freedom.
- A fifth-order polynomial.
- Six constants determined from six boundary conditions.

Such an element can represent more complex local behaviour but is more computationally involved.

The alternative is to use two or more simple two-node beam elements. The lecturer presents this as a trade-off between:

- Higher-order, more complex elements.
- More numerous, lower-order elements.

The lecture does not derive the higher-order element.

### Lecture 10

- A unit displacement produces a corresponding force equal to the relevant stiffness.
- Beam transverse displacement is represented as a weighted combination of four shape functions:
  - \(v(x)=N(x)D\)
  - \(N(x)\) contains the four transverse shape functions.
  - \(D\) is the element deflection vector.
- The beam shape functions are derived from a cubic polynomial with four constants determined by four boundary conditions.
- Euler–Bernoulli beam theory:
  - Assumes small motions.
  - Neglects shear deformation.
  - Is appropriate for long, slender beams.
  - The stated aspect-ratio guideline is approximately greater than \(5{:}1\) to \(10{:}1\).
- A single simple finite element cannot represent arbitrary complex deformation exactly, but multiple elements can approximate more complex behaviour.
- Finite-element modelling involves a trade-off between:
  - A small number of more complex elements.
  - A larger number of simpler elements.
- The beam stiffness matrix is obtained from the second derivatives of the shape functions.
- For constant \(E\) and \(I\), the product \(EI\) can be taken outside the stiffness integral.
- Element stiffness matrices are symmetric:
  \[
  K_{ij}=K_{ji}
  \]
- The unconstrained beam-element stiffness matrix is singular because rigid-body motion has not been restrained.
- Boundary conditions and connectivity information are required to obtain a unique solution.
- A cantilever example reproduces the standard analytical tip-deflection and tip-rotation results.
- A displaced lumped mass can introduce an additional gravity-induced overturning moment that is not automatically captured by the basic small-displacement analysis.
- Frame elements combine:
  - Axial bar behaviour.
  - Beam bending behaviour.
- The frame formulation assumes:
  - Small deflections.
  - Linear elastic material behaviour.
  - Linear superposition.
- In the presented linear frame formulation, axial and flexural terms are contained in one matrix but are not inherently coupled.
- Local axes follow the element. Global axes describe the overall structure.
- For a two-dimensional element, the out-of-plane \(z\)-direction does not rotate with the in-plane element angle, which produces the \(1\) entries in the transformation matrix.
- Matrix dimensions may be identical even when matrices have different meanings. Using the wrong \(6\times6\) matrix may therefore produce an incorrect result without a Python dimension error.
- Consistent degree-of-freedom numbering is essential because the stiffness matrix is derived for a specific ordering.

### Beam shape functions and assumptions

- The previous lecture introduced four possible deflected beam shapes.
- Each shape is represented using a generic cubic polynomial. The four polynomial constants are found by applying four boundary conditions.
- The same procedure is applied to all four shapes; only the boundary conditions differ.
- The resulting four specific equations correspond to the four transverse shape functions shown in the course material.
- The transverse displacement field is written in matrix form as:
  \[
  v(x)=N(x)D
  \]
- The lecture distinguishes this transverse displacement from the axial displacement field previously written using \(u(x)\) and axial shape functions.

The derivation assumes small motions:

- Terms involving squared slopes or other second-order quantities are neglected.
- This is justified only when the relevant displacement and slope quantities are sufficiently small.
- The beam model uses Euler–Bernoulli theory and therefore neglects shear deformation.
- For a short, squat beam, shear deformation may be significant compared with bending deformation.
- A Timoshenko beam element includes additional terms to account for shear deformation. The lecturer stated that this would be covered before the end of the following week.

### Finite-element approximation

- One beam element with two nodes and four degrees of freedom can represent only the deformation shapes included by its interpolation functions.
- More complex deformation behaviour can be represented by dividing the structure into multiple elements.
- A possible three-node beam element would have six degrees of freedom and could use a fifth-order polynomial determined by six boundary conditions.
- Such an element could model more complex behaviour within one element but would be more computationally and procedurally complex.
- The lecturer described the standard finite-element trade-off:
  - Fewer, more complex elements.
  - More, simpler elements.
- The computational effort can be comparable, so the choice depends on the modelling problem and implementation.

### Deriving the beam stiffness matrix

- The virtual-work equation contains:
  - The second derivative of the virtual transverse displacement.
  - \(EI\).
  - The second derivative of the actual transverse displacement.
  - The incremental displacement vector.
  - The applied external-force vector.
- Substituting the shape-function representation into the virtual-work equation and cancelling the common virtual displacement increment gives a matrix equation of the form:
  \[
  [\text{bracketed terms}]D=F
  \]
- The bracketed term is identified as the element stiffness matrix because it relates element forces to element deflections.
- The second derivatives of the four shape functions are substituted into the stiffness expression.
- A typical stiffness component is obtained from:
  \[
  K_{ij}=\int_0^L \left(\frac{d^2N_i}{dx^2}\right)^T EI
  \left(\frac{d^2N_j}{dx^2}\right)\,dx
  \]
- For constant material and geometric properties, \(E\) and \(I\) are taken outside the integral:
  \[
  K_{ij}=EI\int_0^L
  \frac{d^2N_i}{dx^2}
  \frac{d^2N_j}{dx^2}\,dx
  \]
- If the cross-section varies along the element, \(I\) could be retained inside the integral as \(I(x)\).
- If the material is non-homogeneous, \(E\) could similarly be represented as \(E(x)\).
- Such an element would be more specific to the chosen profile and would be less generally reusable.

### Symmetry and implementation checks

- Reversing the two factors in the scalar integrand does not change the result.
- Therefore:
  \[
  K_{ij}=K_{ji}
  \]
- The beam stiffness matrix must be symmetric about its main diagonal.
- For implementation, subtracting the transpose from the matrix should produce a zero matrix:
  \[
  K-K^T=0
  \]
- This is a useful check for:
  - Incorrect signs.
  - Incorrect matrix entries.
  - Incorrect degree-of-freedom ordering.
- The lecturer noted that a \(6\times6\) matrix contains 36 entries, making manual entry errors possible.
- Because of symmetry, only 10 values are unique in a symmetric \(4\times4\) beam matrix:
  - Four diagonal entries.
  - Six entries on one side of the diagonal.

### Beam-element local coordinates and numbering

The beam element uses four degrees of freedom:

- \(D_1\): local transverse displacement at node 1.
- \(D_2\): local rotation at node 1.
- \(D_3\): local transverse displacement at node 2.
- \(D_4\): local rotation at node 2.

The lecturer described the local transverse direction and rotation using the course’s local \(Y\) and \(Z\) notation. In the two-dimensional setting, the out-of-plane rotational direction remains aligned with the corresponding global direction.

The numbering sequence must remain consistent with the derivation. Other textbooks may use a different ordering, but their matrix entries are then rearranged accordingly.

### Beam-element stiffness matrix

With the stated ordering \([D_1,D_2,D_3,D_4]^T\), the standard Euler–Bernoulli beam stiffness matrix is represented in the factored form:

\[
K_E=\frac{EI}{L^3}
\begin{bmatrix}
12 & 6L & -12 & 6L\\
6L & 4L^2 & -6L & 2L^2\\
-12 & -6L & 12 & -6L\\
6L & 2L^2 & -6L & 4L^2
\end{bmatrix}
\]

The lecture explicitly worked through one entry:

\[
K_{22}=\frac{4EI}{L}
=\frac{EI}{L^3}(4L^2)
\]

Important properties stated in the lecture:

- The matrix is in element coordinates.
- \(E\) and \(I\) are assumed constant along the element.
- The beam is assumed long and slender.
- The deformation is predominantly flexural.
- Small-motion assumptions are used.
- Axial deformation is not included.
- The unconstrained matrix is singular because rigid-body modes remain.

For a \(4\times4\) matrix, full rank would mean rank \(4\). The unconstrained beam matrix does not have full rank. In Python, the lecturer referred to checking this with:

\[
\texttt{np.linalg.matrix\_rank(KE)}
\]

The exact automated transcript renders this command imperfectly, but the intended operation is a NumPy matrix-rank calculation.

### Cantilever beam example

- The first beam example is a cantilever fixed at the left end with a transverse tip load.
- The two degrees of freedom at the fixed end are constrained to zero.
- The two unknown degrees of freedom at the free end are:
  - A transverse tip displacement.
  - A tip rotation.
- An assembly matrix maps the element degrees of freedom to the global unknown vector.
- With one element, the element stiffness matrix is also the global stiffness matrix before reduction.
- Applying the assembly/reduction process removes the constrained rows and columns, leaving the reduced system associated with the unknown free-end degrees of freedom.
- Solving this system reproduces the standard cantilever results:

\[
\delta_{\text{tip}}=-\frac{PL^3}{3EI}
\]

\[
\theta_{\text{tip}}=-\frac{PL^2}{2EI}
\]

- The negative signs result from the sign convention:
  - Downward transverse displacement is negative.
  - Counterclockwise rotation is positive.
  - The cantilever tip rotates clockwise under the downward load.

### Cantilever with a displaced lumped mass

- The second example considers a vertical cantilever with a concentrated mass at the top.
- A lateral force \(P\) causes a lateral displacement.
- Once the mass moves outside the original footing or support line, gravity creates an overturning moment.
- This additional moment is not automatically included in the basic small-displacement beam solution.
- The lecturer described manually adding the gravity-induced contribution.
- The gravitational term depends on the weight and the lateral displacement, conceptually:
  \[
  M_{\text{gravity}}=Mg\,D_3
  \]
  where \(D_3\) is the relevant lateral tip displacement under the course’s degree-of-freedom convention.
- The resulting extra displacement contribution was described using the cantilever relationship:
  \[
  \delta_{\text{additional}}
  \sim \frac{M_{\text{gravity}}L^2}{2EI}
  \]
  The exact presentation of this term is difficult to recover from the automated transcript.
- In the numerical illustration:
  - The standard displacement was approximately \(0.18\ \text{m}\).
  - Including the additional overturning effect increased it to approximately \(0.212\ \text{m}\).
  - The lecturer described this as an increase of approximately \(18\%\).
- This calculation is only a first-order approximation because the overturning moment depends on the displacement being calculated.
- A more accurate procedure would:
  1. Calculate the displacement.
  2. Update the overturning moment using that displacement.
  3. Recalculate the displacement.
  4. Iterate until the result converges.

### From beams to frames

The lecturer defined the element types as follows:

- Bars:
  - Axial loads only.
  - No shear or bending-moment behaviour.
- Beams:
  - Transverse shear-force and bending-moment behaviour.
  - No axial deformation in the presented beam element.
- Frames:
  - Axial, transverse, and bending behaviour together.

The frame element is created using linear superposition:

- The axial bar formulation and beam bending formulation are combined.
- No new shape-function derivation is required because the required reaction mechanisms have already been derived.
- The resulting frame element has six degrees of freedom.

### Frame-element degrees of freedom

The local frame-element degrees of freedom are numbered:

- Node 1:
  - \(D_1\): local \(X\)-direction displacement.
  - \(D_2\): local \(Y\)-direction displacement.
  - \(D_3\): local \(Z\)-direction rotational degree of freedom.
- Node 2:
  - \(D_4\): local \(X\)-direction displacement.
  - \(D_5\): local \(Y\)-direction displacement.
  - \(D_6\): local \(Z\)-direction rotational degree of freedom.

The element axis \(x\) runs from node 1 toward node 2.

The frame element therefore has:

- A \(6\times1\) element force vector.
- A \(6\times6\) element stiffness matrix.
- A \(6\times1\) element displacement vector.

### Local frame stiffness matrix

- The frame stiffness matrix in local coordinates combines:
  - Axial stiffness terms involving \(EA/L\).
  - Bending stiffness terms involving \(EI/L^3\).
- The matrix contains zeros in positions representing the absence of direct coupling between axial and transverse/flexural degrees of freedom.
- Thus, the matrix is treated as one \(6\times6\) system, but it contains two independent subsystems:
  - Axial behaviour.
  - Flexural behaviour.
- In the stated linear formulation, axial and flexural terms are solved simultaneously but independently.

A limitation was highlighted:

- If a member deflects transversely while carrying an axial force, the line of action of that axial force may produce a secondary moment.
- This geometric effect is not captured by the basic uncoupled small-displacement frame formulation.
- It should not be assumed that this additional moment is automatically included in the frame stiffness matrix.

### Local-to-global transformation

- The local frame stiffness matrix must be transformed into global coordinates before structural assembly.
- The transformation uses the element angle \(\alpha\).
- The shorthand is:
  \[
  C=\cos\alpha,\qquad S=\sin\alpha
  \]
- The transformation matrix is built from smaller submatrices.
- The lecturer connected this to NumPy’s `block` operation, which constructs a larger matrix from smaller matrices.
- For the two-dimensional frame:
  - The in-plane local \(X\) and \(Y\) directions transform using sine and cosine terms.
  - The out-of-plane \(Z\) direction remains unchanged.
  - The unchanged \(Z\) directions produce \(1\) entries in the transformation matrix.
- The transformation matrix has a block structure containing:
  - Two identical or related \(3\times3\) submatrices.
  - Zero off-diagonal submatrices.
- The local and global coordinate systems coincide when \(\alpha=0^\circ\).
- Examples of element orientations included:
  - \(\alpha=0^\circ\).
  - \(\alpha=30^\circ\).
  - \(\alpha=340^\circ\), equivalently \(-20^\circ\).
  - \(\alpha=160^\circ\).
- Local axes remain aligned with the element, whereas global axes remain aligned with the structure.

### Matrix-dimension warnings

- In the earlier bar-element laboratory, the local matrix and transformed matrix had different dimensions, so using the wrong matrix could produce a Python dimension error.
- For the frame element, both the local stiffness matrix and transformed stiffness matrix are \(6\times6\).
- Consequently, using the wrong one may not produce a Python error.
- The code can execute and produce a numerically valid-looking but physically incorrect result.
- A zero-degree element may conceal this error because local and global coordinates coincide.
- The matrix meaning and coordinate system must therefore be checked explicitly, not inferred from dimensions alone.

### Assembly and structural solution

- The symbolic equations used for frame elements are the same general equations used for bars and beams.
- What changes is the size of the vectors and matrices and the number of reaction mechanisms represented.
- The assembly matrix:
  - Has six columns for a frame element because the element has six degrees of freedom.
  - Has a number of rows determined by the total number of global degrees of freedom in the structural problem.
- After solving for the global displacement vector \(q\), the transpose of the assembly matrix can be used to extract the corresponding element displacement vector \(D\).
- Element forces can then be calculated and assembled across multiple elements.
- The frame element supersedes the beam element for general modelling because axial, transverse, and rotational behaviour are all included.
- The beam element is primarily a stepping stone for understanding the derivation.

### Lecture 11

- Each 2D frame node starts with two translational freedoms and one rotation; supports remove the constrained freedoms (03:00–09:00).
- A shared global displacement/rotation enforces compatibility at a rigid joint. Being free to rotate relative to a support does not imply an internal hinge between members (12:00; 42:00).
- Assembly and coordinate transformation are separate operations. Element stiffness can be identical in local coordinates yet differ globally when orientation changes (15:00).
- A plausible answer must satisfy constraints, force equilibrium and moment equilibrium, not merely return numbers from a matrix solve (18:00–36:00).
- A straight segment between displaced nodes omits bending curvature; shape functions recover the interior deflected curve (39:00–48:00).

### 1. Supports and global degrees of freedom
A clamp removes both translations and rotation. The illustrated horizontal roller constrains vertical translation but permits horizontal motion and rotation; a pin constrains translations while permitting rotation. The ideal roller model may support either sign of vertical reaction; physical lift-off would need a different model. Choose and label the global q values before assembly. A singular matrix can indicate an unconstrained rigid mode, an incorrect assembly mapping, or a missing element-stiffness contribution. Adding arbitrary constraints is not a substitute for checking the physical support model.

### 2. Assembly and solution
Draw each element's local and global degrees of freedom. Map its global element vector D to the full-structure q vector using the course assembly matrix, then transform between D and local d using the course convention. Consistent numbering is essential: renumbering q is permitted if the force vector and assembly matrices are changed consistently. Assemble every element contribution before solving. Use SI units consistently: E in Pa, area in m², second moment in m⁴, forces in N, moments in N·m; deflections emerge in metres and rotations in radians.

### 3. Physical checks
Recover displacement and end-force vectors, sketch their directions, and check known zeros at supports. A 90-degree transformation can exchange locations/signs of familiar numbers; an arbitrary angle generally creates different components. A pin with only one attached member cannot supply a reaction moment, but multiple rigidly connected members at an unrestrained rotational node may have nonzero member-end moments whose sum balances. At the illustrated roller, horizontal member forces sum to zero because there is no horizontal support reaction. Check the equilibrium of each element as well as the assembled structure. End moments need not be equal/opposite: the shear forces form a couple that must also be included in the moment balance. Small residuals from rounded printed values are not automatically modelling errors.

### 4. Plotting implementation
Build and test the local 6×6 frame stiffness function once. Checking K−Kᵀ detects asymmetric entry mistakes, although symmetry alone does not prove correctness. Recover local displacement vectors, evaluate axial and transverse shape functions at multiple positions, rotate the displacements back to global coordinates, and add the original nodal coordinates with a stated visual scale. A rigid connection preserves the relative angle between connected members. Use the four-quadrant angle function: numpy.arctan2(Δy, Δx), not arctan(Δy/Δx). Opposite quadrants share the same ratio and a vertical member can make the ratio undefined. Eleven plotting points correspond to ten intervals, not eleven intervals.

### Lecture 12

- **Local and global equilibrium:** Every element must satisfy equilibrium, and the assembled structure must also satisfy global static equilibrium.
- **Global coordinates:** Forces from multiple elements meeting at a node can be summed in the global \(X_G\), \(Y_G\), and \(Z_G\) directions.
- **Moment equilibrium:** Moments must be checked about a defined point using a consistent sign convention. Counterclockwise was taken as positive in the examples.
- **Moment distribution:** An externally applied moment can be distributed between connected elements according to their effective stiffness.
- **Load follows stiffness:** Increasing an element’s stiffness can cause it to attract a greater share of the applied load.
- **Boundary conditions affect stiffness:** Elements with the same \(E\), \(I\), and \(L\) can have different effective stiffnesses because their end conditions differ.
- **Static indeterminacy:** Equilibrium alone is insufficient for statically indeterminate systems. Constitutive relationships and relative stiffness are required.
- **Effective length and end conditions:** The Euler buckling effective-length factor changes with support conditions.
- **Nodal displacements control the deformed shape:** Element shape functions interpolate the continuous displacement field between nodal values.
- **Continuity at connected nodes:** Shared degrees of freedom enforce compatible translation and rotation between connected elements.
- **Support constraints:** A fixed support has zero translation and zero rotation. A pin support constrains translations but permits rotation. The precise translational constraints depend on the support orientation.
- **Degree-of-freedom numbering:** A logical numbering sequence is not mathematically mandatory, but it can produce simpler assembly matrices.
- **Element force recovery:** Element end-force vectors can be transformed and assembled to identify nodal reactions and internal force resultants.
- **Simplification risk:** Suppressing degrees of freedom can remove physically important load paths from the mathematical model.
- **Axial force couples:** In a laterally loaded portal frame, horizontal shear can be transferred into tension and compression in the columns, contributing to overturning resistance.
- **Equilibrium verification:** Recovered reactions should reproduce the applied external loads and satisfy force and moment equilibrium.

### 1. Equilibrium of the worked frame example

The lecture began by revisiting a two-element frame structure with a concentrated moment applied at the left-hand corner. The element reaction forces had already been calculated in the previous lecture and laboratory.

Important points:

- Each individual element must be in static equilibrium.
- The overall assembled structure must also be in static equilibrium.
- Element end moments do not necessarily need to be equal and opposite at a connection when a shear force is present.
- If an element carries no shear force, the corresponding moment terms may need to balance directly, depending on the element free-body diagram and sign convention.
- Global equilibrium is checked by summing force components in the global coordinate directions and summing moments about a convenient point.

For the example, the lecturer used:

- Rightward as positive in the global \(X_G\) direction.
- Upward as positive in the global \(Y_G\) direction.
- Counterclockwise as positive for moments.

The horizontal forces included approximately \(+2.7097\ \text{kN}\), internal contributions summing to zero at one node, and \(-2.7097\ \text{kN}\) elsewhere. These gave a net horizontal force of zero.

The vertical terms included approximately \(+9.4839\ \text{kN}\) and \(-9.4839\ \text{kN}\), again giving a net vertical force of zero.

When moments were summed about the bottom-left point \(A\):

- A horizontal force acting \(10\ \text{m}\) from \(A\) contributed a clockwise moment.
- Forces whose lines of action passed through \(A\) contributed no moment.
- A concentrated clockwise moment was included with a negative sign.
- A concentrated counterclockwise moment was included with a positive sign.
- The calculated residual was approximately \(0.0175\ \text{kN}\cdot\text{m}\), identified as a rounding error. Using unrounded values in Python would give a result much closer to zero.

The conclusion was that both the individual elements and the assembled structure satisfied equilibrium.

### 2. Distribution of an applied moment

A concentrated external moment was distributed between connected elements. The transcript gives values including approximately \(114.45\), \(45.16\), and \(94.83\), but the exact association of each value with a particular element is unclear because the transcript refers to an omitted diagram.

The central principle was clear:

- Load distribution depends on relative stiffness.
- Relative stiffness depends not only on material and geometric properties such as \(E\), \(I\), and \(L\), but also on boundary conditions and constraints.
- Two elements with identical lengths, elastic moduli, and second moments of area can still attract different loads if their end conditions differ.

In the example:

- One element was described as fully clamped at one end.
- Another was described as pinned at an end.
- The more strongly constrained element had greater effective stiffness and attracted a larger share of the applied moment.

Changing the second moment of area \(I\) of one element in the code was suggested as an experiment. Reducing the \(I\)-value of element 2 to approximately one quarter of its nominal value should cause that element to attract less moment, with more load redistributed to the other element. Increasing the \(I\)-value of element 1 should similarly alter the distribution.

### 3. Static indeterminacy and stiffness

The lecturer related the example to statically indeterminate systems:

- A statically indeterminate system cannot be solved using equilibrium equations alone.
- Compatibility conditions and constitutive relationships are also required.
- Relative member stiffness determines how the load is shared.
- The finite-element method incorporates these relationships automatically through the element stiffness matrices and global assembly.

The structure was described as overconstrained or overdefined relative to the minimum restraint required for stability. The finite-element system solves the resulting indeterminate problem without manual force-distribution intervention.

### 4. Correction to the explanation of stiffness

The lecturer explicitly corrected an earlier explanation of why one element attracted more load. The initial explanation was withdrawn and replaced with an explanation based on effective length, curvature, and boundary conditions.

The comparison was related to Euler buckling:

- A pin-ended column has an effective-length factor of approximately \(K=1.0\).
- A fixed-free column has an effective-length factor of approximately \(K=2.0\).
- The fixed-free member has a longer effective buckling length and therefore a lower critical buckling load for the same \(E\), \(I\), and physical length.

The lecturer used the deformed shapes to explain stiffness:

- One member was constrained against transverse displacement at one end.
- Another member was free to translate transversely.
- The more constrained member developed a tighter, higher-intensity curvature.
- A tighter curvature requires more bending energy to produce.
- Therefore, the member with the combined constraints was effectively stiffer and attracted a larger share of the bending load.

This was presented as the correct explanation for the differing load shares in the example. The earlier explanation should not be relied upon.

### 5. Design implication: strengthening can attract more load

The lecture emphasised the design principle that “load follows stiffness.”

If one element is highly stressed, strengthening it may not always solve the overall problem:

- Strengthening generally increases both strength and stiffness.
- The stiffer element may attract an even larger share of the applied load.
- The resulting load redistribution may increase demand at the strengthened location or elsewhere.
- Adjusting the relative stiffness of several members may be a more effective way to redistribute load through the structure.

A guest-lecture case study was mentioned in which a piece of mechanical equipment repeatedly failed at a location. The location was repeatedly strengthened, but the equipment continued to fail. The stated lesson was that strengthening one region can attract additional load to that region.

### 6. Interpreting and sketching the deformed shape

The lecturer explained how to sketch a frame’s deformed shape by hand from a small number of solved nodal values.

The procedure is:

1. Identify the displacement and rotation associated with each global degree of freedom.
2. Apply the correct sign convention:
   - Positive rotation corresponds to counterclockwise rotation.
   - Negative rotation corresponds to clockwise rotation.
3. Enforce the support constraints:
   - A fixed support has zero displacement and zero rotation.
   - A pin support has zero constrained translations but permits rotation.
4. Use the nodal translations and rotations to infer the local orientation of each element at its ends.
5. Join the element end conditions using a smooth, physically plausible curve.
6. Avoid introducing additional curvature modes unless the nodal information or loading requires them.

In the example, the lecturer described three relevant values:

- \(Q_1\): positive translation.
- \(Q_2\): positive rotation.
- \(Q_3\): negative rotation.

The positive and negative rotation values indicated opposite end rotations. The element therefore had a smooth curve joining a counterclockwise rotation at one end to a clockwise rotation at the other.

If a sufficiently large concentrated moment caused both ends to rotate in orientations requiring a reversal of curvature, the appropriate deformed shape could be a double-curvature shape. Otherwise, the simplest smooth curve consistent with the nodal values should be used.

The key hand-sketching principle was to focus on the nodal points, because that is where the finite-element solution directly provides information. The behaviour between nodes is inferred using the element interpolation functions and physical continuity.

### 7. Degree-of-freedom coupling and compatibility

The lecture revisited how degrees of freedom were coupled during matrix assembly.

In the earlier example:

- A global degree of freedom associated with the \(Z_G\) translation at one element end was connected to the corresponding rotational or nodal degree of freedom of another element according to the problem’s defined degree-of-freedom mapping.
- The transcript’s terminology and labels are unclear at this point, but the underlying principle is that shared physical nodal motions must be represented by shared entries in the global displacement vector.

When two element degrees of freedom are mapped to the same global degree of freedom:

- The elements share the same physical translation or rotation.
- The elements translate and rotate together at the common node.
- The elements cannot move independently at that connection.
- The support condition does not necessarily permit the connected elements to move independently of one another.

The lecturer stated that the method for breaking such coupling would be covered the following week.

### 8. Shape functions and plotting the continuous deformation

The frame-element shape functions were described as including:

- Axial shape functions for \(U(x)\).
- Transverse shape functions for \(V(x)\).

At a point such as \(x=0.2L\):

- \(U(x)\) is the axial displacement at that internal point.
- \(V(x)\) is the transverse displacement relative to the element’s longitudinal axis.

To plot the deformed element in Python:

- The local displacements \(U(x)\) and \(V(x)\) must be converted into global \(X\)- and \(Y\)-coordinates.
- The undeformed element position is combined with the local displacement vector.
- Sine and cosine components are used to account for element orientation.
- The resulting deflected global coordinates are plotted.

The lecturer described using 11 points within each element. Three points would produce a coarse curve, whereas approximately 10–20 points generally give a sufficiently smooth plot. Beyond this range, the visual improvement becomes subject to diminishing returns.

The complete deformed curve was described as being generated from:

- The physical positions of the nodes.
- The element shape functions.
- A small number of solved nodal displacement and rotation values.

This illustrates the finite-element principle that a continuous structural response can be represented using discrete nodal degrees of freedom and interpolation functions.

### 9. Assignment of degrees of freedom for a three-element frame

A new structure was introduced with:

- A pin or knife-edge support at the left.
- Two fixed supports at the other support locations.
- A central node connected to three elements.
- A \(100\ \text{kN}\) applied load at the central node.

The lecturer first identified the permissible degrees of freedom.

At the pin or knife-edge support:

- The global \(X_G\) and \(Y_G\) translations were constrained.
- The global \(Z_G\) rotation was permitted.
- One unknown degree of freedom was therefore assigned at that node, denoted \(Q_1\).
- The permitted rotation was taken as counterclockwise positive.

At each fixed support:

- Translation in the global \(X_G\) direction was constrained.
- Translation in the global \(Y_G\) direction was constrained.
- Rotation about the global \(Z_G\) axis was constrained.
- No unknown \(Q\)-values were assigned at those nodes.

At the central node:

- \(X_G\) translation was potentially non-zero.
- \(Y_G\) translation was potentially non-zero.
- \(Z_G\) rotation was potentially non-zero.
- These were assigned as \(Q_2\), \(Q_3\), and \(Q_4\), respectively.

The exact visual numbering order was not essential. A different numbering sequence would be valid provided that the same physical degrees of freedom were represented consistently. However, logical numbering can make the assembly matrices easier to form and interpret.

### 10. Element-to-global degree-of-freedom mapping

The lecturer then mapped local element degrees of freedom \(D_i\) to the global structural degrees of freedom \(Q_i\).

The transcript gives examples including:

- A local rotational degree of freedom for element 1 mapped to \(Q_1\).
- Several element degrees of freedom at the central node mapped to \(Q_2\), \(Q_3\), and \(Q_4\).
- Shared translations at the central node were assigned the same global degree-of-freedom numbers for all connected elements.

Although some local labels are unclear in the automated transcript, the general assembly rule is:

- Local degrees of freedom that represent the same physical nodal displacement or rotation are mapped to the same global degree of freedom.
- Local degrees of freedom at fixed supports are omitted or mapped to constrained entries.
- The mapping determines the assembly matrices.
- Once connectivity and degree-of-freedom mapping are known, the remaining calculation follows the same procedure used in the laboratory.

The element transformation matrices were calculated from the element orientation angles. The same transformation-matrix equation used in the laboratory applies here.

Because the elements had the same length and material properties, their local stiffness matrices were initially the same. After accounting for their different orientations, their global stiffness matrices were not necessarily identical.

### 11. Assembly matrices and force vector

The assembly matrices contained zero rows or columns associated with constrained or unconnected degrees of freedom.

Interpretation of the zero entries:

- An all-zero column can indicate that a local element degree of freedom is constrained at a support.
- An all-zero row can indicate that a global degree of freedom has no direct connection to a particular element.
- Repeated or identical assembly matrices can occur when two elements have the same connectivity pattern relative to the global degrees of freedom.

The global displacement vector \(Q\) was formed according to the chosen numbering sequence. The applied load vector was then constructed using the physical loading information:

- The applied \(100\ \text{kN}\) load was placed in the entry corresponding to the central-node vertical degree of freedom.
- Other entries were zero unless a force or moment was directly applied there.
- Rotational degrees of freedom require moment units, such as \(\text{N}\cdot\text{m}\) or \(\text{kN}\cdot\text{m}\).
- Translational degrees of freedom require force units, such as \(\text{N}\) or \(\text{kN}\).

The lecturer stressed that a solved vector of numbers is not sufficient. Each entry must be interpreted according to:

- Its degree-of-freedom number.
- Its physical direction.
- Its sign.
- Its units.
- Its location in the structure.

### 12. Interpretation of displacement results

For the three-element frame, the lecturer gave illustrative displacement values including:

- A rotation of approximately \(1.90\ \text{mrad}\), counterclockwise because it was positive.
- A horizontal displacement of approximately \(0.786\ \text{mm}\).
- A vertical displacement of approximately \(4.50\ \text{mm}\).
- A rotation of approximately \(0.414\) mrad or radians according to the transcript; the exact unit is uncertain because the automated transcript alternates between “milliradians” and “radians.”

The correct interpretation process is:

- Positive translation: displacement in the positive global coordinate direction.
- Negative translation: displacement in the negative global coordinate direction.
- Positive rotation: counterclockwise rotation.
- Negative rotation: clockwise rotation.
- Fixed support: zero displacement and zero rotation.
- Pin support: zero constrained translations but permitted rotation.

When sketching the shape by hand:

- Place the supports in their undeformed positions.
- Apply zero displacement and slope where required.
- Translate the central node according to \(Q_2\) and \(Q_3\).
- Rotate the central node according to \(Q_4\).
- Connect the element ends using smooth curves consistent with the end slopes.

### 13. Element reactions and nodal equilibrium

After solving the global system, the element force vectors were recovered and drawn on separate element free-body diagrams.

The support reactions were interpreted as follows:

- At a fixed support connected to only one element, the element end forces at that support correspond directly to the support reaction components.
- At a pin support, there is no reaction moment.
- Multiple element forces meeting at a node must be summed to determine nodal equilibrium.
- If no external horizontal load is applied at a node, the horizontal internal forces meeting there should sum to zero.
- If no external concentrated moment is applied at a node, the nodal moments should sum to zero.
- The vertical element forces at the loaded node should sum to the applied \(100\ \text{kN}\) load.

The lecture gave approximate vertical force contributions of:

- \(28.8692\ \text{kN}\)
- \(68.8798\ \text{kN}\)
- \(2.2510\ \text{kN}\)

These sum to approximately \(100\ \text{kN}\), matching the applied vertical load.

### 14. Global equilibrium check for the three-element frame

The complete structure was also checked using global equilibrium.

For the global \(X_G\) direction, the transcript gives approximate terms including:

- \(-0.3932\)
- \(-0.3932\)
- \(+0.7864\)

These sum to zero, subject to rounding.

For the global \(Y_G\) direction, the terms included:

- \(-28.8692\)
- \(+100\)
- \(-68.8798\)
- \(-2.2510\)

These sum to approximately zero.

Moments were summed about point \(A\), with counterclockwise positive. The lecturer used the appropriate perpendicular distances, including \(4\ \text{m}\) and \(8\ \text{m}\) distances from the diagram. The resulting moment balance was approximately zero.

The equilibrium checks demonstrate that:

- Element force recovery is consistent with nodal equilibrium.
- Nodal equilibrium is consistent with global equilibrium.
- The recovered reaction forces correctly balance the external loads.

### 15. Portal-frame example and omission of degrees of freedom

A portal frame was introduced with:

- Vertical members approximately \(3\ \text{m}\) high.
- A horizontal member approximately \(4.5\ \text{m}\) wide.
- A \(210\ \text{kN}\) horizontal loading arrangement.
- Given \(EI\)-type stiffness properties.

Initially, the lecturer simplified the model by omitting vertical degrees of freedom. The stated reasoning was:

- No vertical loads were directly applied.
- The vertical members were initially treated as rigid in that direction.
- The model was intended to behave more like a beam or bending-only system.
- Axial components were removed from the solution.

The normal finite-element procedure was then applied:

1. Identify the free-body diagrams.
2. Define the local-to-global degree-of-freedom relationships.
3. Construct the assembly matrices.
4. Insert the external loading vector.
5. Solve for the displacements.
6. Recover element force vectors.
7. Draw the reactions on the structure.

However, the simplified model produced unexpected vertical forces at locations where no vertical external loads had been specified. This showed that suppressing the vertical degrees of freedom had changed the physical behaviour of the model.

### 16. Axial force couple in the portal frame

The portal-frame problem was antisymmetric, so the base reactions should reflect the corresponding symmetry.

Under a horizontal load:

- One column develops tension.
- The opposite column develops compression.
- These axial forces form a couple.
- The couple contributes to resistance against the applied overturning moment.
- The horizontal shear in the top member is transmitted into axial forces in the two columns.

By omitting the vertical or axial degrees of freedom, the mathematical system was deprived of the ability to represent this axial force couple. The simplification therefore removed an important load-carrying mechanism.

The problem was re-solved with the omitted degrees of freedom reintroduced:

- Each of the two relevant nodes had three translational or rotational degrees of freedom.
- There were six global degrees of freedom in total for the reduced structural model.
- The resulting assembly matrices were \(6\times6\), with useful zero and identity submatrices due to the logical numbering sequence.
- The solution produced approximately \(10\ \text{kN}\) vertical reactions at each support according to the transcript.
- Non-zero axial forces appeared in the columns.
- The shear force in the horizontal member was transmitted into axial forces in the columns.
- The recovered forces were consistent with the original physical problem.

The lesson was not that simplification is prohibited, but that every suppressed degree of freedom must be checked against the physical load paths. A simplification is acceptable only if it cannot remove a relevant deformation or reaction mechanism.

### 17. Preview of distributed loading and flexible supports

The final discussion briefly considered a support or foundation that is not perfectly rigid.

Possible modelling approaches mentioned were:

- Simplifying the system as a cantilever beam.
- Representing the support using springs with different spring constants.
- Using a fixed support together with distributed or discrete foundation springs.
- Allowing force to distribute across the support rather than concentrating at one idealised point.

The spring stiffnesses would be approximate and depend on the physical support or soil conditions. This topic was only discussed informally and was not developed into a complete derivation in the lecture.

Distributed loading was scheduled for the following lecture.

## Equations and worked patterns

### Lecture 9

### Local beam degrees of freedom

\[
\mathbf{D}
=
\begin{bmatrix}
D_1\\
D_2\\
D_3\\
D_4
\end{bmatrix}
=
\begin{bmatrix}
v_1\\
\theta_1\\
v_2\\
\theta_2
\end{bmatrix}
\]

- \(D_1=v_1\): transverse displacement at node 1.
- \(D_2=\theta_1\): rotation at node 1.
- \(D_3=v_2\): transverse displacement at node 2.
- \(D_4=\theta_2\): rotation at node 2.

### Transverse displacement interpolation

\[
v(x)=\mathbf{N}(x)\mathbf{D}
\]

or:

\[
v(x)
=
N_1(x)D_1
+
N_2(x)D_2
+
N_3(x)D_3
+
N_4(x)D_4
\]

### General cubic shape-function form

\[
N_i(x)=A_i x^3+B_i x^2+C_i x+D_i
\]

The coefficients are determined by the four nodal displacement and slope conditions for each unit deformation case.

### Beam slope

\[
\theta(x)=\frac{\mathrm{d}v}{\mathrm{d}x}
\]

### Beam curvature

\[
\kappa(x)=\frac{\mathrm{d}^2v}{\mathrm{d}x^2}
\]

### Moment–curvature relationship

\[
M=EI\frac{\mathrm{d}^2v}{\mathrm{d}x^2}
\]

The sign may change under a different bending-moment and displacement convention.

### Shear-force relationship

The transcript gives the shear relationship in terms of the derivative of bending moment:

\[
V\sim \frac{\mathrm{d}M}{\mathrm{d}x}
\]

Using the moment–curvature relation:

\[
V\sim EI\frac{\mathrm{d}^3v}{\mathrm{d}x^3}
\]

The exact sign is uncertain in the automated transcript.

### Distributed-load relationship

The distributed transverse load is related to the rate of change of shear force:

\[
w(x)\sim \frac{\mathrm{d}V}{\mathrm{d}x}
\]

Combining the relationships gives:

\[
w(x)\sim EI\frac{\mathrm{d}^4v}{\mathrm{d}x^4}
\]

The sign is convention-dependent and should be checked against the lecture slides or notes.

### Beam end displacement and slope conditions

\[
v(0)=D_1
\]

\[
\frac{\mathrm{d}v}{\mathrm{d}x}(0)=D_2
\]

\[
v(L)=D_3
\]

\[
\frac{\mathrm{d}v}{\mathrm{d}x}(L)=D_4
\]

### Worked \(D_2\) unit-rotation shape-function conditions

For \(D_2=1\) and \(D_1=D_3=D_4=0\):

\[
N_2(0)=0
\]

\[
\frac{\mathrm{d}N_2}{\mathrm{d}x}(0)=1
\]

\[
N_2(L)=0
\]

\[
\frac{\mathrm{d}N_2}{\mathrm{d}x}(L)=0
\]

### Distributed load assumption used in the initial derivation

\[
w(x)=0
\]

### Geometric assumptions

- Slender beam:

\[
\frac{L}{B}\gtrsim 5\text{–}10
\]

- Small deflection:
  - Deflections and rotations are sufficiently small.
  - Second-order products are neglected.
  - The original geometry is used as an adequate approximation to the deformed geometry.

- Prismatic beam:
  - Constant cross-section.
  - Constant \(I\).

- Homogeneous beam:
  - Constant \(E\).

### Lecture 10

### Beam displacement interpolation

\[
v(x)=N(x)D
\]

- \(v(x)\): transverse displacement at position \(x\).
- \(N(x)\): row vector of transverse beam shape functions.
- \(D\): beam-element displacement vector.
- \(x\): local coordinate along the element.
- \(L\): element length.

### Beam stiffness component

\[
K_{ij}
=
\int_0^L
\left(\frac{d^2N_i}{dx^2}\right)^T
EI
\left(\frac{d^2N_j}{dx^2}\right)\,dx
\]

For constant \(E\) and \(I\):

\[
K_{ij}
=
EI\int_0^L
\frac{d^2N_i}{dx^2}
\frac{d^2N_j}{dx^2}\,dx
\]

- \(K_{ij}\): stiffness contribution in row \(i\), column \(j\).
- \(E\): Young’s modulus.
- \(I\): second moment of area.
- \(EI\): flexural rigidity.

### Beam-element stiffness matrix

For the ordering \([D_1,D_2,D_3,D_4]^T\):

\[
K_E=\frac{EI}{L^3}
\begin{bmatrix}
12 & 6L & -12 & 6L\\
6L & 4L^2 & -6L & 2L^2\\
-12 & -6L & 12 & -6L\\
6L & 2L^2 & -6L & 4L^2
\end{bmatrix}
\]

Example entry:

\[
K_{22}=\frac{4EI}{L}
=\frac{EI}{L^3}(4L^2)
\]

Symmetry condition:

\[
K_{ij}=K_{ji}
\]

Matrix check:

\[
K_E-K_E^T=0
\]

### Cantilever response

For a cantilever with a transverse tip load \(P\):

\[
\delta_{\text{tip}}=-\frac{PL^3}{3EI}
\]

\[
\theta_{\text{tip}}=-\frac{PL^2}{2EI}
\]

- \(\delta_{\text{tip}}\): vertical or transverse tip displacement.
- \(\theta_{\text{tip}}\): tip rotation.
- The sign depends on the course’s displacement and rotation conventions.

### Gravity-induced overturning moment

For a mass \(M\) displaced laterally by \(D_3\):

\[
M_{\text{gravity}}=MgD_3
\]

- \(Mg\): weight of the mass.
- \(D_3\): relevant lateral displacement according to the example’s degree-of-freedom numbering.
- The exact additional-displacement equation was not fully recoverable from the automated transcript.

### Frame degrees of freedom

\[
D=
\begin{bmatrix}
D_1\\D_2\\D_3\\D_4\\D_5\\D_6
\end{bmatrix}
\]

Ordering:

\[
[D_1,D_2,D_3,D_4,D_5,D_6]
=
[X_1,Y_1,Z_1,X_2,Y_2,Z_2]
\]

where the \(Z\) entries represent the in-plane rotational degree of freedom under the course’s two-dimensional notation.

### Frame equilibrium equation

\[
F_E=K_E D
\]

For a frame element:

- \(F_E\) is \(6\times1\).
- \(K_E\) is \(6\times6\).
- \(D\) is \(6\times1\).

### Coordinate transformation

\[
C=\cos\alpha,\qquad S=\sin\alpha
\]

The global stiffness matrix is obtained by transforming the local element stiffness matrix using the element transformation matrix. The transcript clearly refers to the standard transformation process, but the complete matrix expression was not fully spoken in the recording.

### Rank

- A \(4\times4\) matrix has full rank if its rank is \(4\).
- The unconstrained beam stiffness matrix is singular because rigid-body modes remain.
- Boundary conditions are required before solving for a unique displacement field.

### Lecture 11

- q: retained global structural degrees of freedom; D: global-coordinate element displacement vector; d: local-coordinate element displacement vector. Consult the reader for the exact transformation-matrix direction.
- Static system: K_global q = Q, with each correctly transformed/assembled element contributing to K_global.
- Length: L = sqrt((x₂−x₁)² + (y₂−y₁)²).
- Orientation: α = atan2(y₂−y₁, x₂−x₁).
- Interior axial/transverse displacement is obtained by multiplying the corresponding shape-function row by the element displacement vector.
- Equilibrium requires both sum of forces = 0 and sum of moments = 0, including force couples.

### Lecture 12

### Static equilibrium

For a structure in static equilibrium:

\[
\sum F_{X_G}=0
\]

\[
\sum F_{Y_G}=0
\]

\[
\sum M_A=0
\]

The exact set of equations depends on the problem’s dimensionality and coordinate system.

### Moment from a force

The magnitude of a moment about point \(A\) is:

\[
M_A = Fd_\perp
\]

where:

- \(F\) is the force magnitude.
- \(d_\perp\) is the perpendicular distance from \(A\) to the force’s line of action.

Using the lecture sign convention:

- Counterclockwise moment: positive.
- Clockwise moment: negative.

A force whose line of action passes through \(A\) has:

\[
d_\perp=0
\]

and therefore produces no moment about \(A\).

### Euler buckling equation

The lecture gave the Euler critical buckling load as:

\[
P_{\mathrm{cr}}=\frac{\pi^2EI}{(KL)^2}
\]

where:

- \(P_{\mathrm{cr}}\) is the critical buckling load.
- \(E\) is Young’s modulus.
- \(I\) is the second moment of area.
- \(L\) is the physical member length.
- \(K\) is the effective-length factor.

Values explicitly mentioned:

- Pin-pinned member: \(K=1.0\).
- Fixed-free member: \(K=2.0\).

The effective buckling length is:

\[
L_{\mathrm{eff}}=KL
\]

### Bending stiffness

The lecture repeatedly referred to bending stiffness through the product:

\[
EI
\]

A larger \(EI\) generally corresponds to greater resistance to bending deformation, but the effective structural stiffness also depends on:

- Boundary conditions.
- Element orientation.
- Connectivity.
- Constraints.
- The available deformation mode.

### Local displacement interpolation

The local element displacement field was represented using shape functions:

\[
U(x) = \text{axial displacement field}
\]

\[
V(x) = \text{transverse displacement field}
\]

The exact shape-function equations were not spoken explicitly in the transcript. The stated process was that axial shape functions interpolate \(U(x)\), while transverse frame-element shape functions interpolate \(V(x)\) and the associated rotations.

### Local-to-global plotting transformation

The lecture described converting local axial and transverse displacements into global coordinates using sine and cosine components. The exact equations were not reproduced in the transcript, but the process is conceptually:

\[
\mathbf{x}_{\mathrm{deflected}}
=
\mathbf{x}_{\mathrm{undeformed}}
+
\mathbf{R}(\theta)
\begin{bmatrix}
U(x)\\
V(x)
\end{bmatrix}
\]

where \(\mathbf{R}(\theta)\) is the rotation transformation associated with the element orientation. The exact sign convention and matrix form should be taken from the course notes or laboratory code.

### Global displacement vector

The global displacement vector was denoted by \(Q\) or \(Q_G\). Its entries represent the unknown global nodal translations and rotations in the chosen numbering sequence.

For a three-degree-of-freedom frame node, the entries generally correspond to:

\[
Q_i =
\begin{bmatrix}
u_{X_G}\\
u_{Y_G}\\
\theta_{Z_G}
\end{bmatrix}
\]

The ordering used in the lecture depends on the chosen global numbering sequence.

### Finite-element system

The general assembled finite-element equation is:

\[
K_G Q_G = F_G
\]

where:

- \(K_G\) is the global stiffness matrix.
- \(Q_G\) is the global displacement vector.
- \(F_G\) is the global applied force and moment vector.

The transcript did not explicitly write this equation during the lecture, but the described procedure was to assemble the stiffness system, insert the forcing vector, solve for displacements, and recover element forces.

### Units

- Translational degrees of freedom are associated with displacement units, such as metres or millimetres.
- Rotational degrees of freedom are associated with radians or milliradians.
- Translational force components are measured in newtons or kilonewtons.
- Rotational force components are moments measured in newton-metres or kilonewton-metres.

A force vector must be ordered consistently with the displacement vector so that force components correspond to the correct translation or rotation degrees of freedom.

### Definitions

- **Global degree of freedom:** A structural displacement or rotation defined in the global coordinate system.
- **Local degree of freedom:** A displacement or rotation associated with an individual element’s local coordinate system.
- **Assembly matrix:** A matrix mapping local element degrees of freedom into global structural degrees of freedom.
- **Static indeterminacy:** A condition in which equilibrium equations alone do not uniquely determine all reactions or internal forces.
- **Effective stiffness:** The resistance of an element or structural system to a particular deformation mode, including the effects of \(E\), \(I\), length, orientation, connectivity, and boundary conditions.
- **Compatibility:** The requirement that connected elements share compatible nodal translations and rotations.
- **Reaction force:** A support force or moment required to enforce a support constraint.
- **Load follows stiffness:** A qualitative design principle stating that stiffer load paths generally attract a larger share of the applied load.
- **Axial force couple:** A pair of opposing axial forces, such as tension in one column and compression in another, that produces a resisting moment.

## Warnings and deadlines

### Lecture 9 — historical source caveats

- This is based on a native Echo automated transcript with substantial recognition errors.
- Several technical terms are transcribed incorrectly, including “shear,” “deflection,” “Euler–Bernoulli,” and “Timoshenko.”
- The transcript does not reliably preserve the displayed equations, matrix entries, or the final explicit expressions for all four shape functions.
- Signs in the equilibrium equations and end-force relationships are convention-dependent and are not unambiguously recoverable from the spoken transcript.
- The transcript appears to contain inconsistent or corrupted labels for some nodal forces and moments, particularly \(F_1\)–\(F_4\). Verify their exact ordering from the lecture slides.
- The transcript mentions equations and diagrams displayed on pages 67 and 69, but their visual contents are not included in the text.
- The stated “less than 1% error” for aspect ratios of approximately 5–10 or greater is an approximate lecture guideline, not a universal guarantee.
- The transcript says the beam initially has no axial components and is treated as axially rigid. The later combined axial-and-bending formulation is not covered in this lecture.
- The derivation assumes zero distributed transverse load initially. The non-zero distributed-load case is deferred to a later lecture.
- The post-lecture student conversation is unintelligible and contains no usable technical content.

### Lecture 10 — historical source caveats

- This is a native Echo automated transcript and contains substantial recognition errors, including:
  - “beam” rendered as “bean”.
  - “shear” rendered as “sheer”.
  - “Timoshenko” rendered approximately as “Tymoshenko”.
  - “finite-element analysis” rendered with several incorrect words.
  - Mathematical symbols, subscripts, superscripts, and matrix notation rendered inconsistently.
- The transcript does not clearly verbalise every entry of the beam or frame stiffness matrices. The standard beam matrix is included using the degree-of-freedom ordering and values referenced during the lecture.
- The complete frame transformation matrix was discussed visually but not fully recoverable from the spoken transcript.
- The exact additional-displacement equation for the displaced lumped mass is unclear in the automated transcript. The physical relationship \(M_{\text{gravity}}=MgD_3\) and the need for iterative updating are clear, but the detailed algebra should be checked against the lecture slides.
- The transcript refers to course-material pages 67, 70, 76, 77, and 79. Those page references are retained where they clarify the lecture sequence, but the slide contents were not independently inspected.
- Several lines after approximately 49 minutes consist of informal conversation, equipment troubleshooting, and unrelated post-lecture discussion. They were excluded from the study notes.
- The lecture assumes the course’s established sign conventions and degree-of-freedom notation. Verify these against the official notes before implementing the matrices.

### Lecture 11 — historical source caveats

Rebuilt on 20 October 2026 from the correctly identified native Echo transcript. Automated speech text has garbled variable names and occasional spoken corrections; exact diagram labels, matrix entries, signs and numerical results should be checked against the course reader/recording. These are selective source-backed notes, not a verbatim or exhaustive replacement for the lecture. Historical test/lab remarks are not final-exam rules. No audio re-transcription was performed.

### Lecture 12 — historical source caveats

- This was a native Echo automated transcript. Numerous words were misrecognised, including “shear” as “share,” “deformed” as “defective,” “kilonewton” as “kilometre” or similar, and “radians” or “milliradians” inconsistently.
- Several numerical values were spoken while referring to diagrams that are not present in the transcript. Their association with particular elements or force components is therefore uncertain.
- The exact geometry and labels of some examples cannot be reconstructed reliably from text alone.
- The transcript gives an approximate residual of \(0.0175\ \text{kN}\cdot\text{m}\) for one moment balance and describes it as a rounding error. The unrounded computational result was said to be closer to zero.
- The transcript’s discussion of the degree-of-freedom mapping around lines corresponding to the bottom-left connection contains corrupted local labels. The reliable principle is that physically compatible connected nodal degrees of freedom must map to the same global degree of freedom.
- The transcript alternates between “rotation,” “radians,” and “milliradians” for one displacement result. The magnitude and sign interpretation are retained, but the unit should be checked against the lecture notes or laboratory code.
- The exact frame stiffness matrix, transformation matrix, shape-function equations, and assembly matrices were referred to but not transcribed explicitly. These should be taken from the course notes and laboratory implementation.
- The final discussion about flexible supports, springs, and simplified cantilever representations was informal and incomplete. It should be treated as a conceptual preview rather than a complete modelling procedure.
- The lecturer explicitly corrected an earlier explanation of why one element attracted more load. The corrected explanation is based on boundary conditions, effective stiffness, curvature, and deformation energy; the withdrawn explanation should not be used.
- The transcript refers to “page 89” and “page 104” of the course notes, but the corresponding diagrams and tables were not included in the source text.

## Recall questions

1. Lecture 9: What types of loading can the beam element carry that the previously studied bar element could not?

2. Lecture 9: Why are axial degrees of freedom omitted in the initial beam-element derivation?

3. Lecture 9: What are the four local degrees of freedom of the two-node beam element?

4. Lecture 9: Why is the local degree-of-freedom sequence described as \(Y,Z,Y,Z\)?

5. Lecture 9: What does the positive \(Z\)-rotation convention represent?

6. Lecture 9: What assumptions are required for Euler–Bernoulli beam theory to be appropriate?

7. Lecture 9: Why must the beam be slender for shear deformation to be neglected?

8. Lecture 9: What is the approximate aspect-ratio guideline given in the lecture for using the Euler–Bernoulli formulation?

9. Lecture 9: Why can shear deflection become important in a short, squat beam?

10. Lecture 9: What beam theory or element type was identified as suitable for modelling significant shear deformation?

11. Lecture 9: What is the physical meaning of the moment–curvature relationship?

12. Lecture 9: What does the first derivative of transverse deflection represent?

13. Lecture 9: What does the second derivative of transverse deflection represent?

14. Lecture 9: How is the shear force related to the derivative of bending moment?

15. Lecture 9: Why does the beam governing equation contain a fourth derivative of transverse displacement?

16. Lecture 9: What simplification results from setting the distributed transverse load \(w(x)\) to zero?

17. Lecture 9: Why are second-order differential terms neglected in the differential equilibrium derivation?

18. Lecture 9: How is the small-deflection assumption connected to the neglect of second-order terms?

19. Lecture 9: Why is integration by parts applied twice in the beam weak-form derivation?

20. Lecture 9: What is the difference between the strong form and weak form of the beam equation?

21. Lecture 9: Why are four shape functions needed for the two-node beam element?

22. Lecture 9: What does the unit-displacement method do?

23. Lecture 9: For the \(D_2=1\) shape function, what values are imposed on \(D_1\), \(D_3\), and \(D_4\)?

24. Lecture 9: What four boundary conditions determine the shape function associated with a unit rotation at node 1?

25. Lecture 9: Why are cubic polynomials used for the two-node beam element?

26. Lecture 9: Why would a fifth- or sixth-order polynomial not be directly justified for the basic four-degree-of-freedom element?

27. Lecture 9: What does the expression \(v(x)=\mathbf{N}(x)\mathbf{D}\) mean physically?

28. Lecture 9: Why can one beam element represent only a restricted family of deformation shapes?

29. Lecture 9: How can multiple simple elements represent a deformation profile that one element cannot capture?

30. Lecture 9: What is the trade-off between using more simple elements and fewer higher-order elements?

31. Lecture 9: How many nodes and degrees of freedom were associated with the more complex element mentioned near the end of the lecture?

32. Lecture 9: Why would the more complex element be computationally more expensive?

33. Lecture 9: Which quantities in the beam formulation retain the same conceptual meaning as in the axial bar formulation, despite the larger matrices?

34. Lecture 9: Which details of the final four explicit beam shape-function equations should be checked against the lecture slides or course notes because they are not fully recoverable from the transcript?

35. Lecture 10: Why are four shape functions required for the two-node Euler–Bernoulli beam element?

36. Lecture 10: How are the constants in the generic cubic beam polynomial determined?

37. Lecture 10: What physical assumptions are made when second-order displacement and slope terms are neglected?

38. Lecture 10: Why is the Euler–Bernoulli beam element unsuitable for short, squat beams?

39. Lecture 10: What additional deformation mechanism is included by a Timoshenko beam element?

40. Lecture 10: Explain why several simple finite elements can model deformation that one element cannot represent.

41. Lecture 10: What is the physical meaning of the bracketed term obtained after substituting the shape functions into the virtual-work equation?

42. Lecture 10: Why can \(E\) and \(I\) be taken outside the beam stiffness integral in the standard formulation?

43. Lecture 10: How would the stiffness integral change if \(E\) or \(I\) varied along the element?

44. Lecture 10: Why must the beam stiffness matrix be symmetric?

45. Lecture 10: What coding check can be used to test the symmetry of a stiffness matrix?

46. Lecture 10: Using the beam matrix ordering in the lecture, what physical degree of freedom corresponds to \(D_2\)?

47. Lecture 10: Why is the unconstrained beam-element stiffness matrix singular?

48. Lecture 10: What boundary conditions are applied to the fixed end of the cantilever example?

49. Lecture 10: Derive or verify the cantilever tip-deflection expression:

50. Lecture 10: Why is the cantilever tip rotation negative under a downward tip load in the stated sign convention?

51. Lecture 10: Why is the gravity-induced overturning moment not automatically captured in the simple lateral-displacement solution for the lumped-mass example?

52. Lecture 10: Why would the lumped-mass example require iteration for a more accurate solution?

53. Lecture 10: What are the differences between bar, beam, and frame elements?

54. Lecture 10: What assumptions are required for linear superposition in the frame formulation?

55. Lecture 10: How is the six-degree-of-freedom frame element constructed from the bar and beam elements?

56. Lecture 10: Why do the local frame stiffness matrix and the global frame stiffness matrix contain zero terms between axial and flexural degrees of freedom?

57. Lecture 10: Does the absence of axial-flexural coupling mean that a laterally displaced axially loaded member has no secondary moment? Explain the limitation stated in the lecture.

58. Lecture 10: What is the frame-element degree-of-freedom ordering from node 1 to node 2?

59. Lecture 10: What is the purpose of the local-to-global transformation matrix?

60. Lecture 10: Why do the \(Z\)-direction entries in the two-dimensional transformation matrix remain equal to \(1\)?

61. Lecture 10: What do \(C=\cos\alpha\) and \(S=\sin\alpha\) represent?

62. Lecture 10: Why can using the wrong \(6\times6\) matrix fail silently in Python?

63. Lecture 10: What dimensions should the local frame stiffness matrix, element displacement vector, and element force vector have?

64. Lecture 10: Why must the numbering sequence used in the code match the numbering sequence used to derive the stiffness matrix?

65. Lecture 11: Which global freedoms remain for a clamp, a horizontal roller and a pin?

66. Lecture 11: Why can a roller-supported rigid joint have nonzero member-end moments?

67. Lecture 11: List three causes of a singular global stiffness matrix and a physical check for each.

68. Lecture 11: Why do unequal end moments not necessarily violate element equilibrium?

69. Lecture 11: What information is lost if the deformed frame is plotted as straight lines between displaced nodes?

70. Lecture 11: Give an orientation where arctan(Δy/Δx) selects the wrong direction, and explain why atan2 resolves it.

71. Lecture 12: Why must both each individual frame element and the overall assembled structure satisfy static equilibrium?

72. Lecture 12: Under what circumstances do element end moments not need to be equal and opposite?

73. Lecture 12: What sign convention was used for horizontal force, vertical force, and moment in the worked equilibrium checks?

74. Lecture 12: Why does a force whose line of action passes through the point about which moments are being summed produce no moment?

75. Lecture 12: What was the approximate residual moment obtained in one global equilibrium check, and why was it considered acceptable?

76. Lecture 12: Why can two elements with identical \(E\), \(I\), and \(L\) attract different shares of an applied moment?

77. Lecture 12: How do different end conditions change an element’s effective stiffness?

78. Lecture 12: Explain the connection between the Euler buckling effective-length factor and support conditions for pin-pinned and fixed-free columns.

79. Lecture 12: Why can a tighter curvature indicate a stiffer deformation mode?

80. Lecture 12: Explain the design meaning of the phrase “load follows stiffness.”

81. Lecture 12: Why might strengthening the most highly stressed element fail to solve the overall structural problem?

82. Lecture 12: What information is needed to sketch a frame’s deformed shape by hand?

83. Lecture 12: How does the sign of a rotational degree of freedom affect the direction of rotation in a sketch?

84. Lecture 12: What displacement and rotation constraints must be shown at a fixed support?

85. Lecture 12: What displacement constraints and permitted rotation apply at a pin or knife-edge support in the example?

86. Lecture 12: Why should the deformed shape be smooth and continuous between nodal points?

87. Lecture 12: Under what circumstances might a double-curvature deformed shape be appropriate?

88. Lecture 12: What is the purpose of assigning the same global degree-of-freedom number to local degrees of freedom belonging to connected elements?

89. Lecture 12: Why is a logical global degree-of-freedom numbering sequence useful even though alternative numbering sequences are mathematically valid?

90. Lecture 12: What can an all-zero row or column in an assembly matrix indicate?

91. Lecture 12: Why can two elements with identical local stiffness matrices have different global stiffness matrices?

92. Lecture 12: How should a solved displacement-vector entry be interpreted beyond simply reporting its numerical value?

93. Lecture 12: Why must a rotational entry in the force vector have moment units rather than force units?

94. Lecture 12: How can element end-force vectors be used to determine support reactions?

95. Lecture 12: How can nodal equilibrium be checked using the forces from several connected elements?

96. Lecture 12: In the three-element frame, why should the vertical force contributions at the loaded node sum to the applied \(100\ \text{kN}\) load?

97. Lecture 12: What physical load path was removed when the vertical degrees of freedom were suppressed in the portal-frame example?

98. Lecture 12: How does a horizontal shear force in a portal frame produce tension and compression in the columns?

99. Lecture 12: Why did omitting axial degrees of freedom generate unexpected vertical reaction forces in the simplified model?

100. Lecture 12: What changed when the omitted vertical degrees of freedom were reintroduced?

101. Lecture 12: When is it safe to suppress degrees of freedom in a finite-element model?

102. Lecture 12: How could flexible soil or foundation support be represented using springs?

103. Lecture 12: What are the main tasks expected in the written test according to the lecture?

104. Lecture 12: Why is plotting code useful for the test but not necessarily required for full marks?

## Practice priorities

1. Tutor strategy for Lecture 9: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

2. Tutor strategy for Lecture 10: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

3. Tutor strategy for Lecture 11: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

4. Tutor strategy for Lecture 12: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

## Missing or incomplete

No missing source-backed lectures in this window. Equations/diagrams remain subject to the per-lecture caveats. The wrong duplicate transcript(s) have been replaced, not guessed from their titles.

## Source manifest

- Lecture 9 (echo-lecture-9-9): complete; summary `1e662d43de9e25ff51ec7f8e102f8b1a68ca85692c4feed1690d32778b2421e4`; transcript `81778e30d402b2b4cdde588f61d06ab037b24a16a59c6bff2a1206d68a4cc171`; summary path `[local source path redacted]`
- Lecture 10 (echo-lecture-10-10): complete; summary `066dd373548f8543925b0c0f0b63898943ee78bc0b42d82169ef70199baa28c6`; transcript `6d30a9e5c8c05b34b58b042b84d2bbad87bb609aee7735536695a67784b7a967`; summary path `[local source path redacted]`
- Lecture 11 (echo-lecture-11-11): complete; summary `9fc3ad10d463706bc5d51cf5e697ec07c0ca432a22d8000795ab95246e958894`; transcript `603576dfddedfff7d1ecca96580509e6a05d8cbff3e656deedc693d6f240c9cb`; summary path `[local source path redacted]`
- Lecture 12 (echo-lecture-12-12): complete; summary `941e2377bd4b9fc7884d7701752fa43a736b110a3b3fe8bb4cd28aa0d6bb86ed`; transcript `5eb2e9f2977101bb512f33d4d99074869e98372f9d557b3fddd5e3a74440ba18`; summary path `[local source path redacted]`
