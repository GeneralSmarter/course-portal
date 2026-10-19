<!-- week-id: 2026-W32 -->
<!-- generated-at: 2026-10-20T12:19:32.657906+13:00 -->
# ENME302-26S2 weekly summary

## Coverage

Rebuilt 20 October 2026 from the corrected source-backed lecture notes. Teaching-week numbering omits the mid-semester break; ISO week identifiers are calendar dates.

- Lecture 13: 2026-08-03. This lecture extends the finite-element formulation to include distributed loads without deriving a separate element type for every possible load profile.  The main approach is equivalent nodal loading:  - A distributed load acting over an element is converted into an equivalent vector of nodal forces and moments. - The existing beam, bar, and frame element formulations can then be retained. - The equivalent element load vector is transformed from local to global coordinates and assembled into the structural load vector. - The stiffness matrix and structural connectivity are unchanged; only the load side of the system equation is extended.  The lecture considers:  - Distributed transverse shear loads. - Uniformly distributed loads (UDLs). - Linearly varying distributed loads. - Concentrate

- Lecture 14: 2026-08-05. The 5 August 2026 lecture continues distributed loading in frame elements. It applies equivalent nodal loads to a bridge-frame example, interprets the resulting displacement field, and checks the formulation against simple cantilever cases. It also discusses the then-upcoming structural-FEA test. That historical test is different from the final examination.

- Lecture 15: 2026-08-06. This lecture connected the finite-element procedures used in the laboratory with commercial finite-element packages, emphasising that commercial software performs the same underlying mathematical operations:  - Solve for nodal displacements. - Apply displacement magnification for visualisation. - Transform element quantities between local and global coordinates. - Assemble element matrices into a global system. - Apply support constraints through assembly and boundary-condition procedures. - Convert distributed loads into equivalent nodal loads. - Account for “lost loads” or “ghost loads” when equivalent nodal loads are applied at support nodes.  The main technical focus was how assembly matrices impose connectivity and boundary conditions, followed by the treatment of lost loads when calc

- Lecture 16: 2026-08-07. This lecture revisits finite-element assembly and explains how assembly matrices map element degrees of freedom into global degrees of freedom. It then examines how to model a pin-jointed member within a frame-element formulation by introducing independent rotational degrees of freedom.  The lecture also summarises the element types covered in the course and places them in the broader context of:  - Static and dynamic finite-element analysis. - Two-dimensional and three-dimensional frame elements. - Linear elastic modelling and its limitations. - Timoshenko beam elements, which include shear deformation. - Commercial structural-analysis software. - Nonlinear structural modelling, plastic hinges, seismic design, and real-time hybrid testing.

## Main concepts

### Lecture 13

- **Equivalent nodal loading:** Replacing a distributed load with nodal forces and moments that produce an equivalent finite-element loading effect.
- **Distributed transverse load intensity:** Denoted in the transcript by \(W(X)\), acting in the local transverse direction.
- **Distributed axial load intensity:** Denoted by \(P(X)\), acting in the local axial direction.
- **Virtual work formulation:** The distributed-load contribution is introduced through the external virtual-work term on the right-hand side of the governing equation.
- **Shape functions:** Used not only to interpolate displacement but also to convert distributed loads into equivalent nodal loads.
- **Local and global coordinates:** Equivalent loads are first obtained in element coordinates, then transformed to global coordinates.
- **Assembly:** Element-level equivalent load vectors are inserted into the structural load vector using the assembly matrix.
- **Beam-to-frame conversion:** A four-degree-of-freedom beam load vector is embedded in a six-degree-of-freedom frame vector by placing zeros in the axial-force locations.
- **Bar-to-frame conversion:** A two-degree-of-freedom axial load vector is embedded in a frame vector by placing zeros in the transverse-force and moment locations.
- **No axial-flexural coupling:** The simplified formulation independently solves axial and transverse/flexural behaviour.
- **Element orientation:** Usually arbitrary if used consistently, but important for linearly varying load profiles because the load intensity depends on which node is at \(X=0\) and which is at \(X=L\).
- **Sanity checks:** Equivalent nodal forces should reproduce the total applied force and should distribute load in a physically sensible way.

The earlier derivations assumed that the internal axial-load distribution in axial bars and the distributed shear-load intensity in beam elements were zero. This was a simplifying assumption. The lecture relaxes that assumption while retaining the previously derived element formulations.

Two possible approaches were identified:

1. Derive new element types containing distributed loading directly.
2. Keep the existing element types and convert distributed loads into equivalent nodal loads.

The second approach is preferred because deriving a separate element for every possible distributed-load profile would produce many element types and stiffness matrices. Equivalent nodal loading allows the existing element stiffness matrices to be reused.

For a beam element, the transverse deflection is represented using shape functions and the element degree-of-freedom vector. In the earlier derivation, the right-hand side of the governing equation was set to zero because no distributed load was present. With a distributed load, the right-hand side is non-zero and contains the external virtual-work contribution.

The derivation follows the same general process used previously:

- Introduce the distributed-load intensity.
- Express the virtual transverse displacement using the beam shape functions.
- Integrate the distributed-load contribution over the element length.
- Integrate by parts where required.
- Apply boundary conditions.
- Group the terms into the familiar stiffness contribution and a new equivalent-load contribution.

The resulting element equation has the same general structure as before, but with an additional equivalent nodal-force term on the load side. In generic form, the structure is of the form

\[
K D = Q + F_{\mathrm{eq}}
\]

where \(K\) is the assembled stiffness matrix, \(D\) is the displacement vector, \(Q\) represents other applied nodal loads, and \(F_{\mathrm{eq}}\) represents the assembled equivalent nodal loads associated with distributed loading. The transcript uses several upper- and lower-case versions of \(F\), \(f\), and \(Q\); the precise notation should be checked against the course notes.

At element level, the distributed load is first converted into a lower-case local equivalent load vector. The local vector is then transformed to global element coordinates using the transformation matrix. Finally, the global element vector is assembled into the structural load vector using the assembly matrix.

For multiple elements and multiple distributed loads, the equivalent element contributions are summed before or during assembly. The structure of the stiffness equation remains unchanged apart from the extra load contribution.

The lecture focuses on the simplified four-degree-of-freedom beam element rather than the full six-degree-of-freedom frame element. The four-degree-of-freedom beam vector contains transverse displacement/force and rotational/moment terms at the two nodes. To use the result in a frame element, axial components are added in the correct positions. Because the distributed transverse load affects flexural behaviour only, the axial entries are set to zero.

### Uniformly distributed transverse load

The first specific load profile is a constant transverse load:

\[
W(X) = \overline{W}
\]

This is called a uniformly distributed load (UDL).

The sign convention used in the lecture defines the UDL as acting in the positive local \(Y\)-direction. A downward load, such as gravity acting on a horizontal element, therefore has a negative value of \(\overline{W}\). A positive value could represent an upward load or wind pressure, depending on the element orientation and coordinate convention.

Since \(\overline{W}\) is constant, it can be taken outside the integration. The equivalent nodal vector is obtained by integrating the transpose of the beam shape-function vector over the element length:

\[
f_{\mathrm{eq}}^{(e)}
=
\int_0^L N^T(X)\,\overline{W}\,dX
\]

The resulting vector represents the equivalent nodal shear forces and end moments for the UDL in the four-degree-of-freedom beam formulation. The transcript does not clearly capture the displayed numerical coefficients of this vector.

The resulting four-degree-of-freedom vector must be embedded into the frame vector by adding zeros in the axial-force positions.

### Linearly varying transverse load

The next load profile is linearly varying, with zero intensity at node 1 and peak intensity \(\overline{W}\) at node 2:

\[
W(X) = \overline{W}\frac{X}{L}
\]

The load is again assumed to act in the positive local \(Y\)-direction. The element orientation matters in this case. If the element is reversed, the load profile must instead be expressed using \(1-X/L\).

The equivalent-load integration becomes

\[
f_{\mathrm{eq}}^{(e)}
=
\int_0^L N^T(X)\,\overline{W}\frac{X}{L}\,dX
\]

The lecture states that the resulting equivalent shear-force components are:

\[
\frac{3\overline{W}L}{20}
\quad\text{and}\quad
\frac{7\overline{W}L}{20}
\]

with the larger force associated with the node at the higher load intensity. Their sum is

\[
\frac{3\overline{W}L}{20}
+
\frac{7\overline{W}L}{20}
=
\frac{\overline{W}L}{2}
\]

This agrees with the total force obtained directly from the triangular load diagram, whose average intensity is \(\overline{W}/2\).

The moment components have different magnitudes at the two nodes and switch when the load profile is reversed. The transcript does not capture all displayed signs and coefficients unambiguously, so those values should be checked against the lecture slides or course notes.

For a load with peak intensity at node 1 and zero intensity at node 2:

\[
W(X) = \overline{W}\left(1-\frac{X}{L}\right)
\]

The equivalent nodal force associated with the higher intensity occurs at node 1. The lecture states that the corresponding force coefficients are reversed relative to the previous case, with \(7\overline{W}L/20\) associated with the high-intensity end and \(3\overline{W}L/20\) associated with the low-intensity end. The moment magnitudes also switch.

An alternative to deriving the reversed profile is to reverse the element orientation through \(180^\circ\), provided the sign conventions and transformations are handled consistently.

The physical response provides a useful sign check. An upward distributed load on a horizontal element produces a hogging deformation pattern under the stated sign convention. The equivalent end moments should produce the same qualitative deformation.

### Concentrated transverse load within an element

A concentrated transverse load applied away from a node can be handled in two ways:

- Add a node at the load location and split the original element into two elements.
- Retain the original element and convert the internal point load into equivalent nodal forces and moments.

The second approach is useful if the structure has already been assembled or if adding a node would be inconvenient.

The concentrated load is represented using the Dirac delta function, also called the impulse function:

\[
W(X) = \overline{W}\,\delta(X-A)
\]

where \(A\) is the distance from node 1 to the point-load location.

The delta function is zero everywhere except at \(X=A\), and its integral extracts the value of the remaining function at \(X=A\). Substitution into the equivalent-load integral gives a general element load vector for a concentrated transverse shear load at any position \(A\).

For a mid-span load:

\[
A=\frac{L}{2}
\]

Substitution into the general expression gives a special-case four-degree-of-freedom beam load vector. The exact displayed coefficients are not fully recoverable from the automated transcript and should be checked against the course material.

The four-degree-of-freedom vector is converted into the six-degree-of-freedom frame vector by setting the axial-force entries to zero.

### Distributed axial load

Distributed axial loads are treated using the same equivalent-nodal-load procedure, but with the axial shape functions rather than the transverse beam shape functions.

The notation changes from:

- \(N(X)\) for transverse shape functions to \(\psi(X)\) for axial shape functions.
- \(W(X)\) for transverse distributed-load intensity to \(P(X)\) for axial distributed-load intensity.

The equivalent axial-load vector has the same general structure:

\[
f_{\mathrm{eq,axial}}^{(e)}
=
\int_0^L \psi^T(X)\,P(X)\,dX
\]

The first case considered is a constant axial load:

\[
P(X)=\overline{P}
\]

The lecture assumes that this load acts in the positive local \(X\)-direction. A negative \(\overline{P}\) represents loading in the opposite direction.

For a two-degree-of-freedom bar element, the constant distributed axial load produces an equal distribution of equivalent force at the two ends. The exact vector is described in the transcript but the displayed coefficient notation is not captured reliably.

To embed this in a frame element:

- Place the two axial equivalent-force terms in the axial-force locations.
- Set the transverse-force locations to zero.
- Set the moment locations to zero.

This reflects the assumption that pure axial loading does not produce transverse or rotational loading in the uncoupled element formulation.

### Concentrated axial load within an element

A concentrated axial load at a distance \(A\) from node 1 can similarly be represented using a delta function. The equivalent axial forces depend on the position ratio \(A/L\).

The transcript refers to the resulting interpolation terms as involving:

\[
1-\frac{A}{L}
\quad\text{and}\quad
\frac{A}{L}
\]

The load distribution is consistent with the relative stiffness of the two portions of the bar:

- If the load is close to node 1, the short segment near node 1 is stiffer and node 1 carries a greater proportion of the load.
- If the load is close to node 2, the load distribution shifts toward node 2.
- At mid-span, the contributions are equal under the assumed uniform bar properties.

The lecturer describes this as a computational representation of the statics and relative-stiffness behaviour of an axially loaded bar. The equivalent frame vector contains non-zero axial terms only; the transverse and moment terms are zero.

### Bridge-deck example

The final section revisits a previously solved portal-frame structure. The structure itself is unchanged, so the element connectivity, assembly matrices, and global stiffness matrix are unchanged.

The new loading consists of:

- A distributed self-weight load on the horizontal bridge-deck element.
- A concentrated load representing an approximately \(5\)-tonne truck.

The distributed self-weight is specified as:

\[
10\ \mathrm{kN/m}
\]

The loaded element length is:

\[
L=4.5\ \mathrm{m}
\]

The lecturer uses a negative value because the load acts downward:

\[
\overline{W}=-10\ \mathrm{kN/m}
\]

or, in SI base units,

\[
\overline{W}=-10000\ \mathrm{N/m}
\]

The truck load is treated as a \(50\ \mathrm{kN}\) concentrated load. The lecturer notes that this corresponds approximately to a \(5\)-tonne mass multiplied by \(9.81\ \mathrm{m/s^2}\), with the problem apparently choosing the value to give exactly \(50\ \mathrm{kN}\).

The procedure is:

1. Use the UDL equivalent-load vector in local element coordinates.
2. Substitute the negative distributed-load intensity and the element length.
3. Apply the transpose of the transformation matrix to obtain the equivalent force vector in global element coordinates.
4. Apply the assembly matrix for the loaded element.
5. Add the resulting global equivalent-load vector to the existing nodal-load vector.
6. Solve using the same global stiffness matrix as for the original structure.

In this particular example, the loaded horizontal element has an orientation angle of \(0^\circ\). Therefore, its transformation matrix is the identity matrix. The assembly matrix for the selected element also happens to be an identity matrix. Consequently, the local, global element, and assembled vectors appear identical in this example. This is a special case, not a general shortcut. In a general problem, the transformation and assembly operations must still be performed.

The worked example is not completed in this lecture.

### Lecture 14

- Distributed and within-element point loads are represented by consistent equivalent nodal forces and moments (12:00–21:00).
- Changing only loading does not change the stiffness matrix of the otherwise unchanged linear structure (15:00–21:00).
- Convert an equivalent load from local element coordinates to global coordinates and then assemble into the full structural force vector (15:00–21:00).
- Linear superposition allows separately calculated responses to be combined, even when the total response has neither component's symmetry (27:00–39:00).
- Benchmark against known solutions. An internally consistent matrix calculation is not sufficient evidence of a correct implementation (39:00–48:00).

### 1. Historical test guidance — not the final exam
The opening portion discusses the August structural-FEA test, an intended Python virtual environment, bringing familiar prepared code and a backup, and interpreting/sketching the results. The lecturer was still awaiting some technical arrangements, so remarks about IDE availability were provisional. Do not use these remarks to infer that computers, code files, USB drives or personal notes are permitted in the October/November final. The current final instructions are closed book and no calculator/computer.

### 2. Consistent loading
For a uniform transverse load, the equivalent vector includes both transverse end forces and end moments, with signs defined by the local element convention. Check the total force against load intensity × length and the overall moment against the distributed resultant. The discussion also recalls linearly varying loads, axial loads and a concentrated load located within an element. Follow the appropriate shape functions and load location; do not simply split every arbitrary point load equally between end nodes.

### 3. Bridge-frame example
The example combines directly applied nodal loads, self-weight represented by a uniformly distributed load, and a within-element point load representing a truck. Build each equivalent local load for the element that actually carries it, use that element's coordinate transformation and assembly mapping, and add the resulting structural vectors to the directly applied nodal force vector. In the displayed special case, a zero orientation angle makes one transformation the identity and one assembly map is also the identity. This numerical coincidence is not a general permission to interchange local, global-element and full-structure load vectors.

### 4. Displacement interpretation
Interpret entries using the associated element free-body diagram and coordinate system. A common axial displacement at both ends represents rigid translation; their difference represents axial extension/compression. The axial strain estimate uses the local axial-displacement difference divided by that element's length. A superscript identifying an element is not an exponent. At a rigid corner, connected members rotate together, preserving their relative angle. For sketches, mark the nodal displacement direction and rotation first, then draw a smooth compatible curve. Explicit labels such as “upward”, “right” or “clockwise” remove ambiguity in a small-scale drawing.

### 5. Superposition and validation
The nodal-only and equivalent-load contributions have different symmetry properties. Adding their responses yields a combined response that need not be symmetric or antisymmetric. Do not force an answer to look symmetric merely because the unloaded geometry does. The lecturer compares cantilever finite-element results with analytical/textbook tip deflection and rotation. Integrating the beam equation and imposing fixed-end and free-end conditions provides an independent benchmark. The lecture also flags that assembling a load vector into retained freedoms can hide contributions at constrained freedoms: reaction recovery needs care, with further treatment deferred to the next lecture. A correct displacement result alone does not validate every reaction calculation.

### Lecture 15

- **Displacement magnification:** A visualisation factor applied to calculated displacements. It does not change the solved displacement; it only exaggerates the plotted deformation.
- **True scale:** A plot using the actual displacement magnitude. For most engineering structures, true-scale deformation is too small to see.
- **Commercial finite-element packages:** They use the same mathematical processes as the laboratory code, including nodal displacement solutions and graphical displacement scaling.
- **Local and global coordinates:** Element quantities are often derived in local coordinates and transformed into the global structural coordinate system.
- **Beam-element transformation matrix:** A reduced transformation matrix can be obtained from the frame-element transformation matrix by removing the rows associated with axial degrees of freedom.
- **Assembly matrix:** Encodes how an element’s local degrees of freedom correspond to the structure’s global degrees of freedom.
- **Boundary conditions through assembly:** Zero columns in an assembly matrix indicate element degrees of freedom that do not correspond to active global degrees of freedom, such as fixed support degrees of freedom.
- **Global stiffness matrix:**
  \[
  K_G = A\hat{K}A^T
  \]
  where \(A\) is the assembly matrix and \(\hat{K}\) is the element stiffness matrix in the relevant coordinate system.
- **Singular free-element stiffness matrix:** An unconstrained element has rigid-body modes and therefore cannot produce a unique displacement solution.
- **Reduction of the system:** Known zero displacements can be removed from the equations, leaving only the unknown active degrees of freedom.
- **Alternative boundary-condition method:** Instead of removing constrained rows and columns, the corresponding equations can be overwritten to enforce prescribed displacements directly.
- **Equivalent nodal loading:** A distributed load is represented by equivalent forces and moments at element nodes.
- **Lost loads / ghost loads:** Equivalent nodal loads applied at support nodes disappear from the active global forcing vector because the corresponding degrees of freedom are constrained.
- **Reaction-load compensation:** Support reactions must include both:
  1. Forces transmitted through the elastic elements.
  2. The reactions to equivalent nodal loads applied directly at the support.
- **Diagnostic red flag:** If an element load vector has more non-zero terms than the assembled global load vector, some loads may have been applied to constrained support degrees of freedom.
- **No lost-load correction needed:** If all equivalent nodal loads are applied at nodes with active degrees of freedom, the element forces transmitted through the structure capture the reactions normally.

### Relationship between laboratory code and commercial software

The lecturer demonstrated displacement visualisation using examples from previous laboratory exercises.

With a displacement magnification factor of 1, the calculated deformation was effectively invisible. A factor of approximately 100 produced a useful visualisation. Excessively large factors, such as 10,000 or 100,000, made the deformation physically misleading because the structure appeared to separate or deform unrealistically.

The same principle applies in commercial finite-element software:

1. The software solves for the displacements at the mesh nodes.
2. The solved displacements are multiplied by a display magnification factor.
3. The displaced geometry is plotted.

The magnified plot is therefore not the actual deformed shape at the displayed scale. It is a visual aid. Magnification must be chosen carefully because excessive exaggeration can make a valid numerical result appear physically unreasonable.

A commercial example involved a viscous fluid damper with two internal pistons, piston valving, and a slightly tapered cylinder. The taper changes the annular flow gap along the stroke, producing variable damping behaviour. The damper is a closed hydraulic system, so cycling dissipates energy as heat and can increase internal fluid pressure. The damping response depends primarily on differential pressure, while the absolute internal pressure also creates stresses in the damper components.

The lecturer used an equivalent-stress analysis of an end cap to show that the displayed stress/deformation result is treated similarly to the laboratory results. The software included automatic deformation scaling, a true-scale option, and adjustable scaling relative to the automatic value. True-scale deformation was generally not visible.

### Beam-element transformation matrix

Beam elements were described as mainly a stepping stone in the derivation rather than a major object of assessment.

The four-degree-of-freedom beam element has transverse displacement and rotation degrees of freedom at each end, without axial displacement degrees of freedom. In local coordinates, the element contains shear/transverse displacement and moment/rotation information at each end.

A corresponding frame element has three degrees of freedom at each node, including axial displacement. For a two-node frame element, the global displacement vector has six components. The beam-element transformation matrix can be formed by taking the frame-element transformation matrix and removing the rows corresponding to the axial degrees of freedom.

The transcript describes the resulting matrix as having four rows and six columns. The dimensions are inferred from the stated removal of two axial rows from a six-row frame transformation matrix; the displayed matrix itself was not available in the transcript.

The lecturer stated that students were not expected to code or be formally tested on this beam transformation matrix. It was discussed to resolve questions from the previous laboratory.

### Assembly matrices and connectivity

Assembly matrices introduce connectivity information into the finite-element system. They specify:

- Which element degrees of freedom correspond to which global degrees of freedom.
- How elements connect to one another.
- How element degrees of freedom connect to support points.
- Which degrees of freedom are active or constrained.

A simple zero-degree transformation-angle cantilever was used to show the process.

For a frame element, the unconstrained element stiffness matrix is \(6 \times 6\). Because the element is free-floating before boundary conditions are introduced, its stiffness matrix is singular. Rigid-body motion is possible, so there is no unique displacement solution.

For a cantilever fixed at the left end:

- The three degrees of freedom at the fixed end are known to be zero.
- The three degrees of freedom at the free end remain unknown.
- The assembly matrix maps the element degrees of freedom to the active global degrees of freedom.

For the zero-degree transformation case, the transcript states that:

\[
D_4 \leftrightarrow Q_1,\qquad
D_5 \leftrightarrow Q_2,\qquad
D_6 \leftrightarrow Q_3
\]

The first three element degrees of freedom correspond to fixed support degrees of freedom. Their associated assembly-matrix columns contain zeros, indicating that they do not map to permissible active degrees of freedom in the global system.

The assembly matrix therefore effectively extracts the unknown portion of the system. The number and locations of the non-zero entries determine which rows and columns of the element stiffness matrix contribute to the active global stiffness matrix.

For a simple fixed cantilever, the active submatrix is a \(3 \times 3\) block. This is not universally the case. A partially restrained support may leave non-contiguous degrees of freedom active. For example, if a support permits some translations and rotation but constrains another translation, the retained rows and columns may be distributed throughout the original matrix rather than forming one corner block.

### Assembly operation

The global stiffness matrix is formed using:

\[
K_G = A\hat{K}A^T
\]

The multiplication performs more than a coordinate relabelling. It selects and places the element stiffness terms into the appropriate global locations.

For the cantilever example:

- Rows and columns corresponding to known zero displacements are excluded from the active system.
- Rows associated with known support forces are not required when solving for the unknown displacement vector.
- The retained submatrix contains the relationships between the unknown active displacements and their corresponding loads.

The lecturer emphasised that the four apparent submatrices of the full matrix are generally not identical. The global stiffness matrix is symmetric about its main diagonal, but the individual submatrices may be unique. One submatrix may be the transpose of another, but this does not mean all four submatrices are the same.

### Alternative method for enforcing supports

Assembly matrices are not the only way to impose boundary conditions.

An alternative is to retain the full system and overwrite the equations associated with fixed degrees of freedom. For a prescribed zero displacement:

- Replace the relevant row with an identity-equation row.
- Set the diagonal coefficient to 1.
- Set the other coefficients in that row to zero.
- Set the corresponding forcing-vector entry to zero.

This produces equations such as:

\[
1D_1 = 0,\qquad
1D_2 = 0,\qquad
1D_3 = 0
\]

The lecturer described placing a diagonal term equal to the inverse of a stiffness-related coefficient so that the resulting diagonal product becomes 1. The transcript renders one expression unclearly as “\(L\) cubed over \(EI\),” so the exact implementation detail should be checked against the lecture notes or course materials.

This method solves the full \(6 \times 6\) system rather than reducing it to a \(3 \times 3\) system. Both methods produce the same physical solution if implemented correctly:

- **Reduced system:** Remove constrained rows and columns and solve only for unknown degrees of freedom.
- **Overwritten system:** Retain all degrees of freedom but explicitly replace constrained equations.

The lecturer noted that retaining all degrees of freedom and overwriting equations can be convenient in code, although the reduced assembly approach was used in the course.

### Equivalent nodal loads

Distributed loads are represented in the finite-element formulation by equivalent nodal forces and moments.

For a beam element, a distributed transverse load generally produces four non-zero local equivalent nodal-load components:

- Shear force at one end.
- Moment at one end.
- Shear force at the other end.
- Moment at the other end.

After multiplication by an assembly matrix, some of these components may disappear from the active global load vector if they act at constrained support degrees of freedom.

This loss does not mean the physical load has disappeared. It means the corresponding load component is applied directly to a support degree of freedom that is not part of the unknown active system.

### Lost loads and ghost loads

The lecturer identified “lost loads” or “ghost loads” as one of the most complicated and non-intuitive topics in this part of the course.

The issue occurs when both of the following conditions apply:

1. A distributed load is converted into equivalent nodal loads.
2. One of the element nodes is also a support node with constrained degrees of freedom.

In that situation, the equivalent nodal load vector may contain four non-zero entries at the element level, but the assembled global load vector may contain only two non-zero entries. The missing terms are the loads applied directly to the support.

The element solution still correctly determines the deformation and internal element forces. However, if support reactions are calculated only from the elastic element forces, the reaction calculation omits the loads applied directly to the support.

A simple conceptual example is a cantilever with a load applied at the fixed support node. The element itself may have:

- No stress.
- No strain.
- No curvature.
- No deflection.

Nevertheless, the support must react to the externally applied load. Since the load is applied at a constrained node, it is not transmitted through the deforming element in the usual way.

### Reaction calculation with lost loads

The total support reaction must combine:

- The forces transmitted through the elastic element.
- The reaction to the equivalent nodal loads applied directly to the support.

In sign-convention form, the lecturer described the calculation as:

\[
\mathbf{R}_{\text{total}}
=
\mathbf{F}_{\text{element}}
-
\mathbf{f}_{\text{equiv at support}}
\]

Equivalently, the reaction to the directly applied support load is the negative of that applied load, with signs interpreted according to the chosen force and moment convention.

For a uniformly distributed load over a \(3\ \text{m}\) cantilever, the total load is:

\[
W = \bar{w}L
\]

It acts through the centroid of the uniform load, at:

\[
x = \frac{L}{2}
\]

from the relevant end. The transcript gives an illustrative equilibrium result of approximately \(30\ \text{kN}\) reaction force and \(45\ \text{kN}\cdot\text{m}\) reaction moment. Some intermediate numerical values in the transcript are poorly recognised by the automated transcription, so the exact load intensity and sign convention should be verified from the original lecture slides.

The important procedure is:

1. Calculate the element equivalent nodal-load vector.
2. Apply the assembly matrix.
3. Identify which load components remain in the active global vector.
4. Recognise any components that were applied directly to constrained support degrees of freedom.
5. Calculate the elastic element forces.
6. Add the reactions associated with the lost support-applied loads.
7. Check the total result against whole-structure equilibrium.

After the missing support-applied loads were included, the calculated reaction force and moment matched the values from direct equilibrium analysis.

### Cable and pulley example

The lecturer considered an overhead cantilever carrying a cable and pulley that lifted an \(800\ \text{N}\) engine.

The cable geometry formed a \(3\)-\(4\)-\(5\) triangle. The cable tension was stated as \(500\ \text{N}\), resolving into:

- \(300\ \text{N}\) horizontal components.
- \(400\ \text{N}\) vertical components.

The horizontal components produce axial loading in the beam. The vertical components produce shear and bending.

The key assembly observation was:

- Some loads are transmitted elastically through the element.
- Other equivalent nodal loads are applied directly to the fixed support and are therefore lost from the active global system.

The element-force calculation produced values including \(400\ \text{N}\), \(300\ \text{N}\), and a \(1200\ \text{N}\cdot\text{m}\) moment. The lecturer noted that an apparent \(300\ \text{N}\) support value could be an internal element reaction rather than an external wall reaction. Independent equilibrium still requires the wall to support the \(800\ \text{N}\) engine load.

For a \(3\ \text{m}\) beam with the \(800\ \text{N}\) resultant acting \(1.5\ \text{m}\) from the support:

\[
R_y = 800\ \text{N}
\]

\[
M_R = 800(1.5)
= 1200\ \text{N}\cdot\text{m}
\]

The corrected finite-element reaction must agree with these equilibrium values.

### Partial distributed loading over multiple elements

The final example was a \(6\ \text{m}\) cantilever divided into two \(3\ \text{m}\) elements:

- The first \(3\ \text{m}\) had no distributed load.
- The second \(3\ \text{m}\) carried a distributed transverse load.
- The intermediate node was not a support; its degrees of freedom were active.

Because both nodes receiving the equivalent nodal loads had active degrees of freedom, all equivalent nodal-load components remained in the assembled global forcing vector. No lost-load correction was required.

The transcript gives an illustrative distributed load of approximately \(10\ \text{kN/m}\), producing:

\[
W = \bar{w}L
= 10(3)
= 30\ \text{kN}
\]

The resultant acts at the centre of the loaded \(3\ \text{m}\) section. Measured from the fixed support, the line of action is \(4.5\ \text{m}\) away:

\[
M_R = 30(4.5)
= 135\ \text{kN}\cdot\text{m}
\]

The computed support reactions agreed with these equilibrium values because the applied loads were carried through active nodes and then transmitted through the first element to the support.

The lecturer also checked equilibrium at the internal node by summing the element-end forces and moments. The internal element reactions balanced the applied external nodal loads.

### Preview of the next lecture

The next lecture was stated to cover rotationally decoupling frame elements, including the case where two frame elements are pinned together. The lecturer indicated that a frame element can be made to behave like a bar by enforcing the appropriate rotational release or decoupling.

### Lecture 16

- Assembly matrices map local element degrees of freedom into the global system.
- The global stiffness matrix is formed by adding each element’s assembled stiffness contribution:
  \[
  K_G = \sum_e A_e \hat{K}_e A_e^T
  \]
- Matrix multiplication by an assembly matrix extracts relevant rows or columns and places them in the correct global locations.
- A degree of freedom with no direct connection to an element produces zero stiffness contribution from that element.
- A frame element normally assumes that connected members are rigidly connected, so translations and rotations are shared.
- A pin joint allows connected elements to share translations while rotating independently.
- Independent rotations at a pin joint require an additional global degree of freedom.
- A frame element can be configured to behave like a bar by preventing bending and shear-force transfer.
- Bar elements carry axial force only.
- Beam elements carry transverse shear force and bending moment, but not axial force in the simplified classification used in the lecture.
- Frame elements are the general two-dimensional element type and can represent axial force, shear force, and bending moment.
- The finite-element procedure generalises from static analysis to dynamic analysis.
- Standard course models are linear elastic and do not automatically check yielding or buckling.
- Timoshenko beam elements include shear deformation in addition to bending deformation.
- A three-dimensional frame element has six degrees of freedom at each node: three translations and three rotations.
- Structural models may combine linear-elastic members with nonlinear components such as plastic hinges.
- Seismic design commonly aims for ductile damage in beams while protecting columns: the “strong-column, weak-beam” approach.
- Real-time hybrid simulation can combine a computational structural model with physically tested components such as dampers.

### Assembly-matrix operation

The first part of the lecture revisits a two-element cantilever-type example with:

- A fully fixed support.
- A roller support allowing horizontal movement and rotation while constraining vertical movement.
- A pin joint allowing rotation but preventing translation.

The element stiffness matrices are initially expressed in local element degree-of-freedom coordinates. Connectivity information specifies how these local degrees of freedom correspond to global degrees of freedom.

For one element, the lecture gives mappings of the form:

- \(D_4^{(1)} \rightarrow Q_1\)
- \(D_6^{(1)} \rightarrow Q_2\)
- No direct connection between element 1 and \(Q_3\)

For the second element, the mappings include:

- \(D_1^{(2)} \rightarrow Q_1\)
- \(D_3^{(2)} \rightarrow Q_2\)
- \(D_6^{(2)} \rightarrow Q_3\)

The assembly operation is written in the form:

\[
K_G^{(e)} = A_e \hat{K}_e A_e^T
\]

where:

- \(A_e\) is the assembly matrix for element \(e\).
- \(\hat{K}_e\) is the element stiffness matrix in its element degree-of-freedom ordering.
- \(A_e^T\) is the transpose of the assembly matrix.
- \(K_G^{(e)}\) is the element’s contribution to the global stiffness matrix.

The example uses a \(3 \times 6\) assembly matrix, a \(6 \times 6\) element stiffness matrix, and a \(6 \times 1\) element vector. The matrices are conformable because adjacent inner dimensions match.

The assembly matrix contains mostly zeros and selected ones. A one indicates that a particular local degree of freedom corresponds to a particular global degree of freedom. During multiplication:

- A one in a row of \(A_e\) selects the corresponding row of \(\hat{K}_e\).
- Multiplication by \(A_e^T\) places the selected terms into the appropriate global columns.
- Zeros prevent unrelated local degrees of freedom from contributing to a given global degree of freedom.

For example, if the first row of the assembly matrix has a one in column 4, the fourth row of the element stiffness matrix is extracted and becomes the first row of the intermediate product. A one in another position similarly extracts the associated row.

If an assembly-matrix row consists entirely of zeros, the element has no direct connection to that global degree of freedom. Consequently, the element contributes a zero row and column for that degree of freedom. The lecture emphasises that this does not necessarily mean the global degree of freedom has no stiffness at all: another connected element may contribute stiffness indirectly.

After each element contribution is assembled, the contributions are added to form the overall global stiffness matrix:

\[
K_G = \sum_e K_G^{(e)}
\]

The lecturer describes this as a bookkeeping operation implemented through linear algebra rather than a mysterious special procedure.

### Pin-jointed member within a frame model

The second major example contains a continuous T-shaped member and an inclined member connected through a pin joint. The outer supports are also pinned.

The inclined member is pinned at both ends and has no applied loads along its length. Therefore, it should carry a purely axial force. A hand calculation based on equilibrium and geometry gives:

- A vertical reaction of approximately \(100\ \text{kN}\).
- A compressive force in the inclined member of approximately \(333.3\ \text{kN}\).

The lecture first models the structure using the usual frame-element assumptions. In that initial setup:

- Each frame-element node has three degrees of freedom in two dimensions:
  - Horizontal translation.
  - Vertical translation.
  - Rotation.
- The model has eight global degrees of freedom.
- Translations and rotations at the shared interface are linked between the connected elements.

For the central node, the initial assembly links the rotational degrees of freedom of all three members to the same global variable. This forces all three elements to have one common mathematical rotation at the joint.

That assumption is incorrect for the actual physical structure because the inclined member is pin-connected. A pin joint should:

- Enforce compatible translations in the global \(x\) and \(y\) directions.
- Allow the connected members to rotate independently.

The initial model therefore does not reproduce the physical behaviour. In particular, it produces force and moment results inconsistent with the intended pin-jointed configuration.

### Introducing independent rotations

To model the pin joint correctly, the central node is assigned two rotational degrees of freedom instead of one. The system therefore has nine global degrees of freedom rather than eight.

The translations remain common to all connected elements. The rotations are separated as follows:

- The two portions of the continuous beam remain linked and share one rotational degree of freedom.
- The inclined member receives a separate rotational degree of freedom.
- The inclined member can therefore rotate independently of the continuous beam.

In terms of the local-to-global mapping, the lecture gives the essential relationships:

- The rotational degree of freedom of element 1 at the interface is linked to the corresponding rotational degree of freedom of element 2.
- Both map to one global rotational variable, identified in the lecture as \(Q_6\).
- The corresponding rotation of element 3 maps to a different global variable, identified as \(Q_7\).
- Other element degrees of freedom are shifted because the additional global rotational degree of freedom has been introduced.

The updated assembly matrices contain different rows for the independent rotations. Previously, the three local rotations occupied the same global row. After the modification:

- The rotations of elements 1 and 2 remain in the same global row.
- The rotation of element 3 occupies a separate global row.

This is a mathematical decoupling of the rotations while preserving translational compatibility.

After solving the corrected system and transforming the global forces back into local coordinates, the inclined member exhibits:

- Axial force.
- Zero shear force.
- Zero bending moment.

This agrees with the physical problem setup. The frame element has effectively been forced to behave like a bar by the choice of connectivity and degrees of freedom.

### Bar, beam, and frame elements

The lecture summarises the simplified element classifications:

- Bar element:
  - Carries axial force only.
  - Does not carry transverse shear force or bending moment.
- Beam element:
  - Carries transverse shear force and bending moment.
  - The transcript’s wording regarding axial force is unclear, but the intended simplified classification appears to exclude axial-force behaviour from the beam-only model.
- Frame element:
  - The general one-dimensional structural element in the course.
  - Can represent axial force, shear force, and bending moment.
  - Can also reproduce bar-like behaviour when the connectivity and constraints remove bending and shear-force transfer.

The course deals primarily with one-dimensional elements, but the same derivation and assembly principles extend to more complex multidimensional elements.

### Static and dynamic finite-element equations

The lecture places the static formulation within the more general equation of motion:

\[
M\ddot{Q} + C\dot{Q} + KQ = F
\]

where:

- \(M\) is the mass matrix.
- \(C\) is the damping matrix.
- \(K\) is the stiffness matrix.
- \(Q\) is the vector of global displacements or generalised coordinates.
- \(\dot{Q}\) is the velocity vector.
- \(\ddot{Q}\) is the acceleration vector.
- \(F\) is the global forcing vector.

For the static problems in this part of the course:

\[
\ddot{Q}=0
\]

and

\[
\dot{Q}=0
\]

so the equation reduces to:

\[
KQ=F
\]

The lecturer notes that the same matrix and assembly concepts generalise to dynamic problems. Mass matrices can be generated using procedures similar to those used for distributed loads. Damping matrices may be defined using combinations of mass and stiffness matrices.

### Three-dimensional frame elements

A three-dimensional frame element has six degrees of freedom at each node:

- Three translations:
  - \(u\)
  - \(v\)
  - \(w\)
- Three rotations:
  - \(\theta_x\)
  - \(\theta_y\)
  - \(\theta_z\)

With two nodes per element, this gives:

\[
6+6=12
\]

degrees of freedom per element. The element stiffness matrix is therefore:

\[
12 \times 12
\]

with:

\[
12 \times 12 = 144
\]

individual entries.

The matrix is sparse, meaning many entries are zero, but it still contains substantially more bookkeeping than the two-dimensional formulation. The conceptual process remains the same:

1. Define local element degrees of freedom.
2. Construct the local stiffness matrix.
3. Transform between local and global coordinates.
4. Assemble into the global system.
5. Apply constraints and solve.

### Linear-elastic limitations

The analysis developed in the course is linear elastic. It assumes a linear relationship between applied loads and calculated displacements and stresses.

The lecturer gives the example that if a load produces a stress of \(100\ \text{MPa}\), multiplying the load by ten would produce a calculated stress of approximately:

\[
10(100\ \text{MPa}) = 1000\ \text{MPa}
\]

and ten times the displacement, provided the same linear model is used.

The code does not automatically determine whether:

- The material has yielded.
- The calculated stress exceeds a permissible value.
- The member has undergone material failure.
- The model should switch to a nonlinear constitutive response.

Additional strength and material checks are therefore required.

Buckling is also not included in the basic analysis. A member may carry an axial load greater than its critical buckling load, making the physical structure unstable, while the basic code continues to return numerical results without warning.

The lecturer notes that buckling can be incorporated through an eigenvalue analysis. This would identify stability limits or critical load factors.

### Timoshenko beam elements

The lecture briefly contrasts the beam formulation used in the course with Timoshenko beam theory.

In a slender beam, total transverse deformation is dominated by bending deformation. Shear deformation is relatively small and may be neglected, as in the Euler–Bernoulli beam formulation used in the course.

For a short or squat beam, shear deformation may be significant. The total deformation can be considered as a superposition of:

- Bending deformation caused by curvature.
- Shear deformation, in which the element distorts toward a parallelogram-like shape.

Timoshenko beam elements include the shear-deformation contribution. Their stiffness matrices contain modification or correction factors associated with shear flexibility.

Including shear deformation generally:

- Reduces the effective stiffness compared with a pure bending model.
- Produces larger predicted deflections.
- Has a greater effect for short, deep, or squat beams than for slender beams.

The transformation and assembly procedures do not fundamentally change. The element stiffness matrix is modified, but the same matrix operations and coordinate transformations are used.

### Structural-analysis software and nonlinear modelling

Commercial structural-analysis packages use the same fundamental concepts but may include:

- Two-dimensional and three-dimensional elements.
- Plate and shell elements.
- Nonlinear material and geometric behaviour.
- Diaphragm action in floors.
- Plastic hinges.
- Soil–structure interaction.
- Dynamic and seismic analysis.

In building models, floor slabs may be represented using two-dimensional plate elements. Diaphragm action ties parts of a floor together and can force compatible movement across the floor system.

A lumped-plasticity model may represent a member as:

- A central linear-elastic element.
- Rotational plastic-hinge springs at one or both ends.

The plastic hinge is an additional rotational component that introduces nonlinear behaviour in a concentrated region rather than modelling plasticity throughout the entire member.

### Strong-column, weak-beam design

The lecture uses earthquake-resistant building design to illustrate why controlled nonlinear behaviour can be desirable.

A beam may be deliberately detailed so that it yields before a column. This allows the beam to absorb energy and undergo damage while limiting the moment transferred into the column.

The design principle is commonly referred to as:

- Strong column, weak beam.

The rationale is that damage to a beam may be repairable while the loss of a column can threaten the stability of the entire building.

The lecturer describes beam-end “dog-boning” or scalloping of an I-beam flange as a way of selectively weakening the beam near the column. This reduces the beam’s moment capacity near the column while retaining greater capacity near mid-span.

Using a smaller beam everywhere would not provide the same distribution of capacity. For gravity loading, the peak bending moment may occur near mid-span, while lower moment demands occur near the supports. Selective weakening can therefore preserve capacity where it is needed while protecting the column connection.

### Hybrid simulation and seismic dampers

The final section introduces real-time hybrid simulation.

A structural model is run computationally while a physical component, such as a viscous damper, is tested in real time. The process is:

1. The computational model calculates a required displacement or motion.
2. The physical actuator applies that motion to the damper specimen.
3. The measured restoring force is returned to the computational model.
4. The structural state is updated.
5. The process repeats within a strict real-time interval.

The damper discussed has a non-Newtonian fluid and a nonlinear force–velocity response, so physical testing is important.

The lecture states that a control cycle may be approximately \(1\ \text{ms}\), requiring all computation and communication for that step to complete within the available time.

Real-time simulation requires:

- Rapid numerical algorithms.
- Adequate computational capability.
- Numerical stability.
- Interlocks and protection systems.
- Careful handling of actuator commands and measured forces.

The lecture also mentions models involving:

- Multi-storey structural frames.
- Structural damping behaviour.
- Soil–structure interaction.
- Different damper configurations.
- Physical damper specimens combined with computational models.

## Equations and worked patterns

### Lecture 13

### Generic equivalent nodal-load expression

For a distributed transverse load:

\[
f_{\mathrm{eq}}^{(e)}
=
\int_0^L N^T(X)\,W(X)\,dX
\]

where:

- \(f_{\mathrm{eq}}^{(e)}\) is the local equivalent element load vector.
- \(N(X)\) is the vector of transverse beam shape functions.
- \(W(X)\) is the distributed transverse-load intensity.
- \(L\) is the element length.

For a distributed axial load:

\[
f_{\mathrm{eq,axial}}^{(e)}
=
\int_0^L \psi^T(X)\,P(X)\,dX
\]

where:

- \(\psi(X)\) is the vector of axial shape functions.
- \(P(X)\) is the distributed axial-load intensity.

### Structural load transformation and assembly

The local equivalent element vector is transformed and assembled into the global structural vector. In conceptual form:

\[
F_{\mathrm{eq}}^{(e)}
=
T^T f_{\mathrm{eq}}^{(e)}
\]

followed by assembly:

\[
Q_{\mathrm{eq}}^{(e)}
=
A^{(e)}F_{\mathrm{eq}}^{(e)}
\]

For several loaded elements:

\[
Q_{\mathrm{eq}}
=
\sum_e Q_{\mathrm{eq}}^{(e)}
\]

The exact placement and notation of the transformation and assembly matrices should be checked against the course convention.

### Structural equilibrium equation

The extended structural equation is conceptually:

\[
K D = Q + Q_{\mathrm{eq}}
\]

where:

- \(K\) is the global stiffness matrix.
- \(D\) is the global displacement vector.
- \(Q\) is the existing applied nodal-load vector.
- \(Q_{\mathrm{eq}}\) is the assembled equivalent-load contribution.

### Uniformly distributed transverse load

\[
W(X)=\overline{W}
\]

The total resultant force over the element is:

\[
F_{\mathrm{total}}=\overline{W}L
\]

The sign convention in the lecture defines positive \(\overline{W}\) as acting in the positive local \(Y\)-direction.

### Linearly varying transverse load, zero at node 1

\[
W(X)=\overline{W}\frac{X}{L}
\]

with:

\[
W(0)=0,
\qquad
W(L)=\overline{W}
\]

The average intensity is:

\[
W_{\mathrm{avg}}=\frac{\overline{W}}{2}
\]

The total resultant force is:

\[
F_{\mathrm{total}}
=
W_{\mathrm{avg}}L
=
\frac{\overline{W}L}{2}
\]

The lecture identifies the equivalent nodal shear-force components as:

\[
\frac{3\overline{W}L}{20}
\quad\text{and}\quad
\frac{7\overline{W}L}{20}
\]

Their sum is:

\[
\frac{3\overline{W}L}{20}
+
\frac{7\overline{W}L}{20}
=
\frac{\overline{W}L}{2}
\]

### Linearly varying transverse load, zero at node 2

\[
W(X)=\overline{W}\left(1-\frac{X}{L}\right)
\]

with:

\[
W(0)=\overline{W},
\qquad
W(L)=0
\]

The higher equivalent nodal shear force is associated with node 1. The force coefficients are reversed relative to the previous orientation.

### Concentrated transverse load

\[
W(X)=\overline{W}\,\delta(X-A)
\]

where:

- \(\delta(X-A)\) is the Dirac delta function.
- \(A\) is the load location measured from node 1.

For a mid-span load:

\[
A=\frac{L}{2}
\]

### Constant distributed axial load

\[
P(X)=\overline{P}
\]

The load is assumed positive in the local \(X\)-direction. For a two-degree-of-freedom bar element, the resulting equivalent axial load is distributed equally between the two ends according to the lecture discussion.

### Concentrated axial load

A concentrated axial load at distance \(A\) from node 1 is represented using a delta-function formulation. The equivalent axial contributions contain the position-dependent factors:

\[
1-\frac{A}{L}
\quad\text{and}\quad
\frac{A}{L}
\]

The transverse-force and moment entries are zero when the axial and flexural systems are treated independently.

### Beam-to-frame and bar-to-frame vectors

For the six-degree-of-freedom frame ordering described in the lecture:

- Axial terms occupy the axial-force locations.
- Transverse terms occupy the transverse-force locations.
- Rotational terms correspond to nodal moments.
- A transverse beam load vector is expanded by inserting zeros into the axial locations.
- An axial bar load vector is expanded by inserting zeros into the transverse-force and moment locations.

The exact degree-of-freedom numbering should be checked against the course’s frame-element convention.

### Lecture 14

- Total assembled load: Q_total = Q_direct + Q_equiv,UDL + Q_equiv,point, using the course's transformation/assembly conventions.
- Unchanged linear structure: K_global q = Q_total.
- Local axial strain: ε_axial = (d_axial,2 − d_axial,1)/L for the same element. Bending produces additional normal-strain variation through the section.
- Uniform load resultant: w̄L; the illustrated symmetric consistent transverse-force components are w̄L/2 at each end, accompanied by end moments. Check their exact signs against the reader.
- Linear superposition: the displacement response to a sum of loads is the sum of individual displacement responses when the same linear stiffness model applies.

### Lecture 15

### Displacement magnification

A plotted displacement can be represented conceptually as:

\[
\mathbf{u}_{\text{plot}}
=
m\mathbf{u}_{\text{solved}}
\]

where:

- \(\mathbf{u}_{\text{solved}}\) is the actual calculated displacement.
- \(m\) is the display magnification factor.
- \(\mathbf{u}_{\text{plot}}\) is the displayed deformation.

The factor \(m\) affects visualisation only, not the solution.

### Global stiffness assembly

\[
K_G = A\hat{K}A^T
\]

where:

- \(K_G\) is the assembled global stiffness matrix.
- \(A\) is the assembly matrix.
- \(\hat{K}\) is the element stiffness matrix after any required coordinate transformation.
- \(A^T\) is the transpose of the assembly matrix.

### Uniformly distributed load resultant

For a uniform distributed load \(\bar{w}\) acting over length \(L\):

\[
W = \bar{w}L
\]

The resultant acts at the centroid of the loaded length. For a uniform load over the full element:

\[
x_{\text{resultant}} = \frac{L}{2}
\]

### Cantilever reaction from a point resultant

For a resultant force \(W\) acting at perpendicular distance \(x\) from the support:

\[
R = W
\]

\[
M_R = Wx
\]

with signs determined by the selected equilibrium convention.

### Total reaction with lost loads

Conceptually:

\[
\mathbf{R}_{\text{total}}
=
\mathbf{R}_{\text{elastic}}
+
\mathbf{R}_{\text{direct support load}}
\]

If \(\mathbf{f}_{\text{support}}\) is the equivalent nodal load applied directly to a constrained support degree of freedom, then:

\[
\mathbf{R}_{\text{direct support load}}
=
-\mathbf{f}_{\text{support}}
\]

Therefore:

\[
\mathbf{R}_{\text{total}}
=
\mathbf{R}_{\text{elastic}}
-
\mathbf{f}_{\text{support}}
\]

The exact signs depend on whether the reported quantities are element-end forces, externally applied loads, or support reactions.

### \(3\)-\(4\)-\(5\) cable-force resolution

For a cable tension of \(500\ \text{N}\) aligned with a \(3\)-\(4\)-\(5\) triangle:

\[
T_x = 500\left(\frac{3}{5}\right)=300\ \text{N}
\]

\[
T_y = 500\left(\frac{4}{5}\right)=400\ \text{N}
\]

The horizontal component contributes to axial loading; the vertical component contributes to shear and bending.

### Terminology

- **Active degree of freedom:** An unknown displacement included in the solved global system.
- **Constrained degree of freedom:** A prescribed displacement, usually zero at a fixed support.
- **Element forcing vector:** The load vector associated with an individual element, including equivalent nodal loads.
- **Global forcing vector:** The assembled load vector for the whole structure.
- **Equivalent nodal load:** A set of nodal forces and moments that represents the effect of a distributed or non-nodal load within the finite-element formulation.
- **Lost load / ghost load:** An equivalent nodal-load component applied at a constrained degree of freedom and therefore omitted from the active assembled forcing vector.
- **Assembly matrix:** A mapping matrix that places element degrees of freedom and loads into their corresponding global positions and implicitly eliminates constrained degrees of freedom in the reduced system.

### Lecture 16

### Global stiffness assembly

For an element \(e\):

\[
K_G^{(e)} = A_e \hat{K}_e A_e^T
\]

where:

- \(A_e\): assembly matrix.
- \(\hat{K}_e\): element stiffness matrix.
- \(A_e^T\): transpose of the assembly matrix.
- \(K_G^{(e)}\): contribution of the element to the global stiffness matrix.

The total global stiffness matrix is:

\[
K_G = \sum_e K_G^{(e)}
\]

### Static equilibrium

\[
KQ=F
\]

where:

- \(K\): global stiffness matrix.
- \(Q\): global displacement/generalised-coordinate vector.
- \(F\): global force vector.

### General dynamic equation

\[
M\ddot{Q}+C\dot{Q}+KQ=F
\]

For static analysis:

\[
\dot{Q}=0,\qquad \ddot{Q}=0
\]

so:

\[
KQ=F
\]

### Two-dimensional frame-element degrees of freedom

A typical two-dimensional frame node has:

\[
\{u,\ v,\ \theta\}
\]

where:

- \(u\): horizontal translation.
- \(v\): vertical translation.
- \(\theta\): in-plane rotation.

### Three-dimensional frame-element degrees of freedom

A three-dimensional frame node has:

\[
\{u,\ v,\ w,\ \theta_x,\ \theta_y,\ \theta_z\}
\]

With two nodes per element:

\[
n_{\text{DOF}}=12
\]

and the element stiffness matrix is:

\[
K_e \in \mathbb{R}^{12\times 12}
\]

### Axial member result from the lecture example

The hand calculation for the inclined, pin-ended member gives approximately:

\[
F_{\text{inclined member}}=333.3\ \text{kN}
\]

in compression.

The corresponding vertical reaction is stated as:

\[
R_{Cy}=100\ \text{kN}
\]

### Linear scaling assumption

Under linear elasticity:

\[
F \propto Q
\]

and, for a fixed linear material model:

\[
\sigma \propto F
\]

Thus, multiplying the load by a factor of ten multiplies the predicted displacement and stress by ten, provided no nonlinear behaviour is included.

### Buckling

Buckling is described as an instability associated with an axial load causing loss of lateral stiffness. The basic course code does not calculate or flag the critical buckling load. The lecturer identifies eigenvalue analysis as one possible method for adding buckling assessment.

### Timoshenko beam behaviour

The total beam deformation may be viewed conceptually as:

\[
\delta_{\text{total}}
=
\delta_{\text{bending}}
+
\delta_{\text{shear}}
\]

The Euler–Bernoulli formulation neglects the shear contribution. Timoshenko beam theory includes it.

## Warnings and deadlines

### Lecture 13 — historical source caveats

- This source is a native Echo automated transcript with substantial recognition errors, especially in mathematical notation, variable names, degree-of-freedom labels, and displayed vectors.
- The transcript alternates between potentially different cases of \(F\), \(f\), \(Q\), and \(q\). The exact course notation should be checked against the lecture slides and prior notes.
- Several displayed equivalent-load vectors were spoken while the lecturer referred to a slide, but their complete coefficients and signs are not recoverable reliably from the transcript. In particular, verify:
  - The complete UDL beam-element vector.
  - The moment components for the linearly varying load.
  - The complete concentrated transverse-load vector.
  - The complete constant distributed axial-load vector.
  - The exact degree-of-freedom ordering for the frame vector.
- The transcript sometimes renders “shear” as “share,” “beam” as “be,” “node” as “note,” and mathematical symbols as unrelated words.
- The lecturer states that the simplified beam formulation uses four degrees of freedom and that the full frame element uses six degrees of freedom. The exact ordering of these degrees of freedom should be confirmed from the course’s established convention.
- The bridge example is incomplete. The transcript ends after the equivalent UDL vector has been transformed and assembled; the structural solution and the combined truck-load calculation are deferred to the next lecture.
- The lecturer describes the approximately \(5\)-tonne truck load as being selected to produce exactly \(50\ \mathrm{kN}\). Treat \(50\ \mathrm{kN}\) as the problem input rather than independently recomputing it from an unspecified exact mass.
- The transcript contains unrelated post-lecture conversation after the formal lecture ends. It has not been included in the study notes.

### Lecture 14 — historical source caveats

Rebuilt on 20 October 2026 from the recording-identity-verified native Echo transcript. This is Weeks 1–4 structural FEA, outside the final's Weeks 5–12 scope. The transcript contains garbled variable names, self-corrections and diagram-dependent numerical statements; the exact element matrices, equivalent-load signs and printed values remain authoritative in the reader. These notes are selective rather than exhaustive. Historical test logistics are not current permissions. No new audio ASR was performed.

### Lecture 15 — historical source caveats

- This document is based only on the native Echo automated transcript. No slides, diagrams, handwritten matrix layouts, or source code were available for cross-checking.
- Several technical terms were mistranscribed. Examples include “beam” or “bean,” “shear” or “she,” “kilonewton,” “equivalent,” and other matrix-related phrases. The notes use the technically consistent interpretation where the intended meaning is clear.
- The transcript states that the beam transformation matrix has “66 columns,” which is almost certainly an automated-transcription error. The explanation indicates a \(4 \times 6\) matrix obtained by removing two axial rows from a \(6 \times 6\) frame transformation matrix.
- The exact beam-element displacement and force ordering was not fully audible. The stated correspondences between \(D_4,D_5,D_6\) and \(Q_1,Q_2,Q_3\) are retained from the transcript, but notation should be checked against course notes.
- Some numerical values in the lost-load examples were unclear or internally inconsistent in the transcript. The robust results explicitly stated by the lecturer include:
  - \(800\ \text{N}\) engine load.
  - \(500\ \text{N}\) cable tension.
  - \(300\ \text{N}\) and \(400\ \text{N}\) cable-force components.
  - \(1200\ \text{N}\cdot\text{m}\) moment for an \(800\ \text{N}\) load acting \(1.5\ \text{m}\) from the support.
  - Approximately \(30\ \text{kN}\) resultant and \(135\ \text{kN}\cdot\text{m}\) moment for the partially distributed \(6\ \text{m}\) cantilever example, based on the stated \(10\ \text{kN/m}\) load over \(3\ \text{m}\).
- The exact expression described for overwriting the stiffness-matrix diagonal was unclear in the transcript. It was rendered approximately as \(L^3/EI\); this should be verified against the lecture material before using it in code.
- The lecture explicitly indicated that the detailed beam transformation derivation and handwritten assembly-matrix manipulation were not expected to be major assessment targets, although understanding the principles remains useful.
- The transcript contains substantial pre-lecture, post-lecture, microphone, and informal conversation material. These have been excluded from the study notes except where they affected technical interpretation.

### Lecture 16 — historical source caveats

- This is a native Echo automated transcript and contains substantial transcription errors, missing words, speaker-attribution errors, and occasional unclear terminology.
- Several matrix entries and degree-of-freedom mappings were described while referring to displayed slides that are not present in the transcript. The notes preserve only mappings that can be interpreted with reasonable confidence.
- The notation around local and global force vectors is inconsistent in the transcript. The general dynamic equation is written here using the conventional form \(M\ddot{Q}+C\dot{Q}+KQ=F\).
- The transcript sometimes says “assembly matrix” where the surrounding explanation appears to refer to a transposed assembly matrix or to the intermediate matrix product. The underlying operation is summarised using the standard expression \(A_e\hat{K}_eA_e^T\).
- The transcript contains garbled terms such as “sheer” for “shear,” “Tymoshenko” for “Timoshenko,” and distorted names for Euler–Bernoulli beam theory. These have been corrected where the intended technical meaning is clear.
- The statement describing beam elements as carrying only shear and moments is simplified and potentially incomplete. The notes retain the lecture’s intended bar/beam/frame classification without extending it beyond what was explicitly explained.
- The \(333.3\ \text{kN}\) compressive force and \(100\ \text{kN}\) reaction are reported as lecture results. The transcript does not provide enough geometry and loading information to independently reproduce the calculation.
- The lecture mentions that commercial software may include nonlinear element actions, plate elements, diaphragm action, plastic hinges, and soil–structure interaction, but does not derive those formulations.
- The buckling discussion distinguishes transverse bending deflection from buckling due to a sufficiently large axial load. These are different phenomena: ordinary lateral deflection under transverse loading is not itself a buckling calculation.
- The real-time hybrid-simulation discussion includes project-specific examples and approximate facility specifications. Those details are contextual rather than core ENME302 derivations and should not be treated as independently verified technical data from this transcript alone.

## Recall questions

1. Lecture 13: Why is equivalent nodal loading preferred over deriving a new finite element for every distributed-load profile?

2. Lecture 13: What simplifying assumption about distributed loading was made in the earlier beam and bar derivations?

3. Lecture 13: How does introducing a distributed load change the right-hand side of the finite-element equilibrium equation?

4. Lecture 13: Write the general equivalent nodal-load integral for a distributed transverse load.

5. Lecture 13: What is the role of the beam shape functions in converting a distributed load into nodal forces and moments?

6. Lecture 13: Why can a constant UDL intensity be taken outside the equivalent-load integral?

7. Lecture 13: For \(W(X)=\overline{W}X/L\), what are the load intensities at node 1 and node 2?

8. Lecture 13: For the linearly varying load \(W(X)=\overline{W}X/L\), verify that the equivalent shear-force components stated in the lecture sum to the total triangular-load resultant.

9. Lecture 13: Why is the larger equivalent nodal shear force associated with the node at the higher load intensity?

10. Lecture 13: How does reversing the element orientation change the expression for a linearly varying load?

11. Lecture 13: Why does element orientation matter for a linearly varying distributed load but not in the same way for a constant UDL?

12. Lecture 13: What physical deformation pattern is expected from an upward UDL under the sign convention used in the lecture?

13. Lecture 13: How can a concentrated load applied within an element be handled without using a Dirac delta function?

14. Lecture 13: What is the purpose of using \(\delta(X-A)\) to represent an internal point load?

15. Lecture 13: What does the Dirac delta function do when it appears inside the equivalent-load integral?

16. Lecture 13: What is the special value of \(A\) for a mid-span point load?

17. Lecture 13: How does the equivalent-load formulation for a distributed axial load differ from the transverse-load formulation?

18. Lecture 13: Which shape functions are used for distributed axial loading?

19. Lecture 13: Why does a constant distributed axial load produce equal end contributions in the simple bar-element formulation?

20. Lecture 13: How should a transverse beam load vector be embedded into a six-degree-of-freedom frame load vector?

21. Lecture 13: How should an axial bar load vector be embedded into a six-degree-of-freedom frame load vector?

22. Lecture 13: What assumption justifies setting the axial entries to zero for a pure transverse load?

23. Lecture 13: What assumption justifies setting the transverse-force and moment entries to zero for a pure axial load?

24. Lecture 13: What is the purpose of the transformation matrix in the equivalent-load procedure?

25. Lecture 13: What is the purpose of the assembly matrix?

26. Lecture 13: Why did the transformation and assembly matrices appear to have no effect in the bridge example?

27. Lecture 13: Why would it be incorrect to omit the transformation and assembly steps in a general problem?

28. Lecture 13: For the bridge-deck example, why is the self-weight input as a negative \(10\ \mathrm{kN/m}\) load?

29. Lecture 13: What parts of the finite-element model remain unchanged when additional distributed loads are introduced?

30. Lecture 13: What physical and dimensional sanity checks should be applied to an equivalent nodal-load vector?

31. Lecture 14: Why must a consistent distributed-load vector include end moments as well as end forces?

32. Lecture 14: Which matrices change when only load intensity changes on the same linear frame?

33. Lecture 14: Why can an identity transformation in one example hide an error that fails for a rotated element?

34. Lecture 14: How do you distinguish rigid axial translation from axial strain?

35. Lecture 14: How can a symmetric geometry have a nonsymmetric deflected shape?

36. Lecture 14: What benchmark and boundary conditions would you use to validate a cantilever implementation?

37. Lecture 14: Why does a correct displacement solution not automatically prove correct support reactions?

38. Lecture 15: What is the purpose of displacement magnification in a finite-element plot?

39. Lecture 15: Why is a true-scale deformation plot often not useful for engineering structures?

40. Lecture 15: What mathematical operations does a commercial finite-element package perform when displaying a deformed mesh?

41. Lecture 15: Why can excessive displacement magnification produce a physically misleading plot?

42. Lecture 15: What degrees of freedom are present in the four-degree-of-freedom beam element discussed in the lecture?

43. Lecture 15: How can the beam-element transformation matrix be obtained from the frame-element transformation matrix?

44. Lecture 15: Why is the stiffness matrix of a completely unconstrained frame element singular?

45. Lecture 15: What information is encoded by an assembly matrix?

46. Lecture 15: For a zero-degree cantilever with the left end fixed, which global degrees of freedom remain unknown?

47. Lecture 15: Explain why zero columns appear in the assembly matrix for constrained support degrees of freedom.

48. Lecture 15: State the global stiffness assembly equation and identify each matrix.

49. Lecture 15: Why are the submatrices of the assembled stiffness matrix not necessarily identical?

50. Lecture 15: How does the location of the 1s and 0s in an assembly matrix determine which stiffness-matrix rows and columns are retained?

51. Lecture 15: Why might the retained active submatrix not form a simple corner block for a partially restrained support?

52. Lecture 15: Describe the alternative method of enforcing fixed displacements by overwriting equations in the full stiffness matrix.

53. Lecture 15: Compare solving a reduced \(3 \times 3\) system with solving an overwritten \(6 \times 6\) system.

54. Lecture 15: What are equivalent nodal loads, and why are they used for distributed loading?

55. Lecture 15: Under what two conditions do lost loads or ghost loads arise?

56. Lecture 15: Why can an element load vector have four non-zero terms while the assembled global load vector has only two?

57. Lecture 15: Does a load disappear physically when it is lost from the active global load vector? Explain.

58. Lecture 15: Why can calculating reactions only from elastic element forces produce an incorrect answer?

59. Lecture 15: How should the reaction to an equivalent nodal load applied directly to a support be included?

60. Lecture 15: What red flag in the number of non-zero load-vector components may indicate lost loads?

61. Lecture 15: For a uniform load over a length \(L\), where does the equivalent resultant act for a simple equilibrium calculation?

62. Lecture 15: For a \(3\ \text{m}\) cantilever carrying a uniform load, how would you calculate the total vertical reaction and support moment?

63. Lecture 15: In the cable example, how are a \(500\ \text{N}\) cable tension and a \(3\)-\(4\)-\(5\) geometry resolved into horizontal and vertical components?

64. Lecture 15: Which cable-force components contribute to axial loading, and which contribute to bending?

65. Lecture 15: Why was no lost-load compensation required in the two-element example with the load applied only to the second element?

66. Lecture 15: How can equilibrium at an internal node be checked using the element-end forces?

67. Lecture 15: What is the difference between a load transmitted through an elastic element and a load applied directly to a constrained support node?

68. Lecture 16: What physical information is represented by an assembly matrix?

69. Lecture 16: Why must the inner dimensions of matrices match for the assembly multiplication to be valid?

70. Lecture 16: In the expression

71. Lecture 16: How does a one in an assembly matrix select a row or column of the element stiffness matrix?

72. Lecture 16: What does an all-zero row in an assembly matrix indicate about the element’s direct contribution to a global degree of freedom?

73. Lecture 16: Why can an element have no direct stiffness contribution to a global degree of freedom while the global structure still has stiffness associated with that degree of freedom?

74. Lecture 16: What assumptions about connected rotations are made by the standard frame-element formulation?

75. Lecture 16: Why does directly connecting the rotations of all three members at the central joint incorrectly model the pin-jointed inclined member?

76. Lecture 16: What compatibility conditions should a pin joint impose on translations?

77. Lecture 16: What compatibility condition should a pin joint not impose on the rotations of independently pinned members?

78. Lecture 16: Why was an additional global degree of freedom required in the corrected pin-joint model?

79. Lecture 16: Which rotations remained linked after the additional degree of freedom was introduced, and which rotation was decoupled?

80. Lecture 16: Why should a member pinned at both ends, with no distributed load along its length, carry only axial force?

81. Lecture 16: How does the corrected frame model force the inclined member to behave like a bar?

82. Lecture 16: What are the principal differences between bar, beam, and frame elements in the simplified classification used in the lecture?

83. Lecture 16: Starting from

84. Lecture 16: How many degrees of freedom does a two-dimensional frame node have?

85. Lecture 16: How many degrees of freedom does a three-dimensional frame element with two nodes have?

86. Lecture 16: Why does a three-dimensional frame element require a \(12\times12\) stiffness matrix?

87. Lecture 16: What does it mean for the element stiffness matrix to be sparse?

88. Lecture 16: Why is the course analysis unable to identify yielding automatically?

89. Lecture 16: What could happen if a load is increased tenfold in a linear-elastic model beyond the material’s actual capacity?

90. Lecture 16: Why is a structure that exceeds its critical buckling load not necessarily identified as unsafe by the basic code?

91. Lecture 16: What type of analysis can be added to assess buckling?

92. Lecture 16: Why is shear deformation often neglected for slender beams?

93. Lecture 16: Why is shear deformation more important for short or squat beams?

94. Lecture 16: How does including shear deformation affect the predicted stiffness and deflection?

95. Lecture 16: What aspects of the finite-element procedure remain unchanged when switching from an Euler–Bernoulli beam element to a Timoshenko beam element?

96. Lecture 16: What is the purpose of a plastic-hinge spring in a lumped-plasticity model?

97. Lecture 16: Explain the structural rationale behind the strong-column, weak-beam design approach.

98. Lecture 16: Why might a beam be selectively weakened near a column rather than simply replaced with a smaller beam throughout its length?

99. Lecture 16: Describe the information flow between a computational structural model and a physical damper in real-time hybrid simulation.

100. Lecture 16: Why are numerical stability and interlocks particularly important in real-time structural testing?

## Practice priorities

1. Tutor strategy for Lecture 13: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

2. Tutor strategy for Lecture 14: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

3. Tutor strategy for Lecture 15: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

4. Tutor strategy for Lecture 16: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

## Missing or incomplete

No missing source-backed lectures in this window. Equations/diagrams remain subject to the per-lecture caveats. The wrong duplicate transcript(s) have been replaced, not guessed from their titles.

## Source manifest

- Lecture 13 (echo-lecture-13-13): complete; summary `13a70e407d95c729b30f20204250d9391cab4f88b8ea0077d9fd2f6d000a088f`; transcript `889bc88e0f9a5b20bc56139e9db9aaf33d5803aca1a490f87dbdbe8d711c5426`; summary path `[local source path redacted]`
- Lecture 14 (echo-lecture-14-14): complete; summary `5a66137fac0ddd51e8dcf2460f8c2fe11d060dd9e320f1eb64dd6102e482b2e4`; transcript `5a8767017afdde9831cde92941429f887a1b22154729f072a975bcf67e005820`; summary path `[local source path redacted]`
- Lecture 15 (echo-lecture-15-15): complete; summary `05d04f8aa8b6c1cdc9511a075229febd8af9dc14583863c898f001b3ad08d381`; transcript `b1a16c7824db87cdc4aa8fe09fc2756695e1aba3ba636ae77487b1ac08ab1d6e`; summary path `[local source path redacted]`
- Lecture 16 (echo-lecture-16-16): complete; summary `fb14394fc6013e5c5a52f304023b6c15010c638223be11ec257c09a07a890f6b`; transcript `7a8d90ea543f2c50e56782ca8798c0634153a0f13c2b6767d00a1f43fdcd20f0`; summary path `[local source path redacted]`
