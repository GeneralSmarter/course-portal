<!-- week-id: 2026-W29 -->
<!-- generated-at: 2026-10-20T12:19:32.657906+13:00 -->
# ENME302-26S2 weekly summary

## Coverage

Rebuilt 20 October 2026 from the corrected source-backed lecture notes. Teaching-week numbering omits the mid-semester break; ISO week identifiers are calendar dates.

- Lecture 1: 2026-07-13. - Lecture 1 introduced the course structure and the purpose of the first four weeks: building a computational framework for finite element analysis (FEA) on top of mechanics and materials concepts from ENME202 or an equivalent course. - The course is fundamentally concerned with numerical techniques for solving engineering problems governed by differential equations, including partial differential equations (PDEs). - The first four weeks have a structural focus:   - Weeks 1–2: axial truss elements.   - Weeks 3–4: flexural beam elements. - The initial emphasis is on one-dimensional elements. These are simpler than two- or three-dimensional solid elements but can still be assembled into complex 2D and 3D structures. - The central idea of FEA is to divide a complex system into smaller, simple

- Lecture 2: 2026-07-15. Lecture 2 introduced the finite element method as a systematic way to approximate the behaviour of complex structures by discretising them into simple elements. The central relationship is the matrix form of Hooke’s law:  \[ \mathbf{F}=\mathbf{K}\mathbf{D} \]  where applied nodal loads are related to nodal deflections through a stiffness matrix.  The lecture then focused on the simplest structural finite element: a two-node axial bar element. Its assumptions, local coordinate system, degrees of freedom, static equilibrium, and governing differential equation were introduced. Shape functions were identified as the mechanism used to reconstruct displacement, strain, and stress within an element from a limited set of nodal values, although the shape functions themselves were not derived in th

- Lecture 3: 2026-07-16. Lecture 3 develops the two-node axial bar element and introduces shape functions as the central mechanism of the finite element method. The lecture:  - Formulates the static boundary-value problem for a homogeneous, prismatic axial bar. - Assumes zero distributed axial loading within the element. - Derives a linear displacement field from the two nodal displacements. - Defines the corresponding linear shape functions. - Derives constant element strain, stress, and normal force. - Constructs the axial bar element stiffness matrix. - Explains why the unconstrained element stiffness matrix is singular. - Connects singularity to rigid-body motion and insufficient boundary conditions. - Discusses approximating varying geometry with multiple smaller elements. - Briefly previews a Python refreshe

- Lecture 4: 2026-07-17. - Brief Python lab recap:   - Array transpose using `np.transpose(A)` or the shorthand `A.T`.   - Construction of larger matrices from submatrices using `np.block`.   - Matrix multiplication using `np.matmul` or `@`, as distinct from elementwise multiplication using `*`.   - LaTeX-style formatting in plot labels and legends.   - Use of Spyder’s Variable Explorer and readable matrix-output formatting for debugging. - Structural-analysis example:   - A two-member pin-jointed bar structure with one horizontal member and one member inclined at \(45^\circ\).   - A \(100\ \text{kN}\) upward load is applied at the free joint \(C\).   - Member forces, axial deformations, and the horizontal and vertical displacement of joint \(C\) are calculated. - Small-deflection linearisation:   - Exact compatib

## Main concepts

### Lecture 1

- **Finite element analysis:** A framework for representing a complex continuous system using a collection of simpler discrete elements.
- **Discretisation:** Breaking a continuous structure or domain into a finite number of elements connected at nodes.
- **Nodes:** Discrete points at which quantities such as displacement are solved.
- **Shape functions:** Mathematical functions used to interpolate quantities within an element from nodal values.
- **Element assembly:** Combining the behaviour of individual elements to model an entire structure.
- **Statically determinate structure:** A stable structure whose reactions and internal member forces can be found using equilibrium equations alone.
- **Statically indeterminate structure:** A structure with more constraints than the minimum needed for stability. Its internal force distribution depends on compatibility and relative member stiffness, not statics alone.
- **Structural redundancy:** Additional constraints or load paths beyond the minimum required for stability.
- **Relative stiffness:** In an indeterminate structure, the proportion of load carried by different members depends on their stiffnesses.
- **Axial truss element:** A pin-connected element carrying only axial tension or compression, with no bending moment or shear force.
- **Flexural beam element:** An element capable of representing bending, shear, rotations, and moments.
- **Degrees of freedom:** The independent translations and rotations used to describe nodal motion.
- **Boundary conditions:** Restrictions imposed on degrees of freedom, such as fixed, free, pinned, roller, knife-edge, or slotted conditions.
- **Mesh:** The collection of finite elements used to represent a geometry. Mesh refinement produces smaller and more numerous elements.
- **Model hierarchy:** Use a relatively simple global model to understand overall load paths, then apply more detailed models to critical components where necessary.
- **Research-informed modelling:** Experimental results can be used to calibrate and validate computational models, which can then be modified to study related structures and generalise findings.

- **Relationship to prior mechanics**
  - ENME202 or an equivalent mechanics and materials course provides the foundation for this course.
  - Prior topics such as stress, strain, equilibrium, axial loading, shear force, bending moment, beam deflection, compatibility, and stiffness remain relevant.
  - FEA does not replace classical mechanics. It provides a systematic computational framework for applying those mechanics to systems that are impractical to solve analytically or by hand.

- **Why computational methods are needed**
  - A simple pin-jointed truss loaded only at its nodes can often be solved using:
    - force equilibrium,
    - moment equilibrium,
    - support reactions,
    - method-of-joints or equivalent force resolution,
    - axial stress calculations.
  - Because ideal truss members are pin-connected and loaded only at nodes, they carry axial forces only.
  - Adding one redundant member can make the truss statically indeterminate.
  - Once a structure is indeterminate, equilibrium alone is insufficient. Member stiffness and displacement compatibility must be considered.
  - If joints are rigidly welded rather than pinned:
    - members can carry axial force, shear, and bending moment;
    - nodal rotations matter;
    - distributed loads may be applied along members;
    - the structure can become substantially more difficult to analyse by hand.
  - The complexity grows quickly as members, orientations, fixed supports, and redundant load paths are added.

- **Fundamental finite element strategy**
  - A complicated structure is divided into simpler elements.
  - The behaviour of each element is described mathematically.
  - Elements are connected at nodes.
  - The element equations are assembled into a global system representing the complete structure.
  - Boundary conditions and loads are applied.
  - The global system is solved for unknown nodal quantities.
  - Element-level quantities such as forces, stresses, strains, moments, or shears can then be recovered.
  - This makes it possible for simple elements to represent a system much more complicated than any individual element.

- **One-dimensional elements**
  - The course begins with elements whose geometry and primary behaviour are represented along one dimension.
  - Initially, these elements stretch or compress along their length.
  - Bending moment and shear will be introduced later.
  - A one-dimensional element is not restricted to a one-dimensional overall structure:
    - elements can be placed at different orientations;
    - multiple 1D elements can form a 2D truss or frame;
    - a collection of 1D elements can also represent a 3D structure.
  - One-dimensional models are useful in their own right because they are computationally efficient and can reveal global load paths and structural behaviour.
  - Modelling an entire building with detailed 3D solid elements may be computationally excessive and unnecessary for high-level structural analysis.
  - A practical workflow is:
    1. Model the complete structure using simpler line elements.
    2. Determine global forces, deformations, and load paths.
    3. Identify critical members or connections.
    4. Analyse those local components using a more detailed model.

- **Element progression in the first four weeks**
  - **Weeks 1–2: axial truss elements**
    - Pin-connected.
    - Loads applied at nodal points.
    - Carry axial tension or compression.
    - Do not carry shear force or bending moment.
  - **Weeks 3–4: flexural beam elements**
    - Introduce bending and shear.
    - Include nodal rotations and bending moments.
    - Extend the same computational framework developed for axial elements.

- **From discrete nodes to a continuous field**
  - FEA solves unknown quantities at a finite number of nodal points.
  - The physical object being modelled is continuous, so the nodal solution must provide a representation of behaviour between nodes.
  - Shape functions interpolate quantities such as displacement inside an element from known nodal values.
  - Derived quantities such as strain can then be determined from the interpolated displacement field.
  - Shape functions are therefore central to:
    - constructing element equations,
    - connecting nodal values to internal element behaviour,
    - interpreting the finite element solution.

- **Dimensions and element types**
  - **1D elements:** Primarily defined along a line, including truss and beam elements.
  - **2D elements:** Used to represent behaviour over an \(x\)-\(y\) domain; the lecturer referred to plate-type elements as an example.
  - **3D solid elements:** Used to represent volumetric behaviour in three dimensions.
  - The mathematical principles and problem setup developed for 1D elements extend to 2D and 3D formulations.

- **Loads, supports, and degrees of freedom**
  - Potential applied loads include:
    - point forces,
    - moments,
    - continuously distributed loads.
  - Boundary conditions discussed include:
    - **fixed:** relevant translations and rotations restrained;
    - **free:** corresponding degrees of freedom unrestrained;
    - **pin or knife-edge:** translations restrained while rotation remains free;
    - **roller:** restrained in one translational direction but free in another;
    - **slotted connection:** similar directional restraint to a roller.
  - Selecting the correct degrees of freedom and boundary conditions is an essential modelling decision.

- **Classical cantilever example**
  - A tip-loaded cantilever has:
    - a fixed support at \(x=0\),
    - total length \(L\),
    - a point load \(P\) at the free end,
    - a coordinate \(x\) measured from the fixed end.
  - Cutting the beam at position \(x\) gives a remaining lever arm of \(L-x\).
  - With the sign convention used in the lecture, the bending moment is:
    \[
    M(x)=-P(L-x)=-PL+Px
    \]
  - The bending moment varies linearly:
    - \(M(0)=-PL\) at the fixed end;
    - \(M(L)=0\) at the free end;
    - slope \(dM/dx=P\).
  - Integrating the moment-curvature relation and applying fixed-end boundary conditions gives the beam rotation and deflection.
  - This familiar analytical element behaviour becomes a building block for modelling more complicated frames.
  - In a rigid frame made from several welded members, total displacement may contain contributions from:
    - axial deformation,
    - bending of multiple members,
    - nodal rotation,
    - coupling between connected members.
  - Although each member may be individually straightforward, the assembled structure can be difficult to solve manually.

- **Example: variable geometry and discretisation**
  - A member with varying cross-section may not have a convenient analytical solution.
  - It can be divided into several simpler elements, each approximating part of the geometry.
  - This illustrates the core FEA principle: approximate a difficult continuous problem using a finite set of manageable pieces.

- **Example: damper-shaft buckling**
  - A damping device used in structural testing contained an exposed shaft with a strongly varying cross-section.
  - The end conditions could be approximated as pinned because spherical plain bearings were present at both ends.
  - Standard closed-form buckling formulas assume relatively idealised geometry, such as a constant cross-section, and were not directly suitable for this component.
  - A solid model was therefore meshed using either a coarse or fine mesh.
  - An Euler buckling or eigenvalue buckling analysis was then used to estimate the load at which buckling would occur.
  - This demonstrated where FEA can fill a gap left by simplified analytical equations.

- **Earthquake-engineering applications**
  - The lecturer described rocking-wall systems used as primary lateral-load-resisting systems.
  - In the Tūranga central library example:
    - concrete walls are held against the foundation by approximately \(10{,}000\ \text{kN}\) of hold-down force from pretensioned steel tendons;
    - under low demand, such as wind or a small earthquake, the wall remains clamped to the foundation;
    - under higher demand, the wall uplifts and rocks on its foundation;
    - damping devices between the wall and foundation dissipate energy during rocking;
    - one cited damper had a resisting force of approximately \(750\ \text{kN}\), described as roughly 75 tonnes-force.
  - Small uplift displacements make unwanted flexibility, connection slip, and mechanical take-up important because these effects can consume a significant fraction of the intended damper motion.
  - Shake tables reproduce recorded earthquake acceleration histories to evaluate:
    - structural response,
    - damping systems,
    - force-transfer mechanisms,
    - damage progression.
  - One described facility used twelve hydraulic pumps and a bank of accumulators:
    - the accumulators were charged for roughly half an hour;
    - the stored energy could be discharged over approximately 30 seconds during a large test;
    - one pump was stated to use three-phase \(380\ \text{V}\) power with a full-load current of \(656\ \text{A}\).
  - A scaled high-rise test structure was approximately \(16\ \text{m}\) tall and weighed approximately \(140\) tonnes.
  - Large experiments are expensive and time-consuming, so validated numerical models are used to:
    - reproduce measured behaviour,
    - study damage progression,
    - refine modelling strategies,
    - explore related structures without repeating every full-scale experiment.

- **Biomechanics application**
  - Passive ultrasonic receivers were positioned along the region adjacent to a hip-replacement implant, approximately from the iliac crest to the mid-femur.
  - The setup also included motion-tracking markers, inertial measurement units, and a force plate.
  - The force plate measured three-dimensional ground-reaction forces.
  - Motion measurements captured hip, knee, and ankle articulation during walking.
  - The purpose was to non-invasively detect vibrations emitted by the implant and relate them to internal implant behaviour.
  - Inverse kinematics and a lower-limb biomechanics model could be used to associate observed ultrasonic emissions with specific phases or events in the walking motion.
  - Vibration-mode analysis of the implant could help interpret what particular measured frequencies or emissions represent.

- **Broader mathematical scope**
  - The first four weeks focus mainly on structural systems.
  - The later part of the course, taught by James, will place greater emphasis on PDEs.
  - Similar numerical mathematics can be applied to different physical quantities, including:
    - structural displacement and deformation,
    - heat flow,
    - magnetism.
  - Once a governing differential equation and suitable numerical framework are available, related solution methods can be applied across multiple engineering domains.

- **Course organisation and assessment**
  - The first lecturer teaches weeks 1–4.
  - James takes over the lectures in week 5.
  - Week 5 computer labs still relate to the first four weeks of content.
  - A computer-based test is scheduled for early week 6, stated as the evening of Tuesday 18 August.
  - Code developed during the laboratory sessions is intended to be used to solve problems in the test.
  - The first laboratory is mainly a Python refresher covering:
    - matrix entry,
    - matrix multiplication,
    - linear-algebra manipulation,
    - plotting.
  - These exercises were selected because the same Python skills will be needed in subsequent finite element work.
  - The assessment schedule described:
    - a week 6 test;
    - Assignment 1 due shortly after the term break;
    - five quizzes worth 1% each, beginning after James takes over;
    - Assignment 2 due in early October;
    - a final examination.
  - A minimum mark of 40% in the final examination is required to pass the course overall.
  - The assessment schedule was described as provisional until the end of week 2.
  - Active participation in computer laboratories was strongly encouraged because the code and skills developed there support performance in the test, even if the laboratories do not carry a direct grade.

### Lecture 2

- A complicated structure can be approximated by dividing it into simple, discrete finite elements.
- Each element has a known or derivable relationship between nodal forces and nodal deflections.
- Element equations are transformed and assembled into a global structural system.
- Boundary conditions constrain fixed degrees of freedom and make the final system solvable.
- The solved nodal displacement vector can be used to recover:
  - support reactions;
  - axial forces;
  - shear forces;
  - bending moments;
  - displacement within elements;
  - strain and stress within elements.
- The fundamental finite element equation is a matrix generalisation of Hooke’s law.
- Bar or truss elements:
  - are pin-connected;
  - carry axial force only;
  - initially have loads applied only at nodes;
  - have one axial translational degree of freedom at each end.
- Beam elements can carry bending moments and shear forces and include lateral translations and rotations.
- Frame elements combine axial and bending behaviour.
- Every element has a local coordinate system aligned with that element.
- A global coordinate system is used to describe the complete structure.
- Element orientation angles permit transformations between local and global coordinates.
- Shape functions interpolate behaviour inside an element using its nodal values.
- The analysis in this part of the course is static, although the stiffness framework can be extended to dynamic problems.
- Understanding the formulation is necessary to use commercial finite element software critically rather than treating it as a black box.

- The finite element method addresses structures whose complete continuous behaviour would involve infinitely many possible evaluation points.
- Solving for displacement, stress, or strain at every point directly is generally impractical.
- The structure is therefore discretised into a finite number of elements connected at nodes.
- Only a finite number of nodal degrees of freedom are solved explicitly.
- Internal element behaviour is then approximated from those nodal values.

- A simple cantilever beam can be solved analytically when it has:
  - constant cross-section;
  - constant elastic modulus;
  - homogeneous material;
  - prismatic geometry;
  - simple loading.
- A complete structure assembled from many members can be much harder to solve directly.
- Finite element analysis retains the comparatively simple behaviour of each member and combines those members computationally.

- The intended finite element workflow is:
  1. Discretise the structure into elements and nodes.
  2. Form an individual stiffness equation for each element.
  3. Transform element quantities between local and global coordinate systems where required.
  4. Assemble the element equations into a larger global system.
  5. Apply supports and boundary conditions by constraining the appropriate degrees of freedom.
  6. Solve the resulting linear algebra problem for the unknown nodal deflections.
  7. Recover reaction forces and internal element actions.
  8. Use interpolation functions to estimate displacement, strain, and stress inside each element.
  9. Interpret the numerical results physically and check whether they are meaningful.

- The simple axial-extension relationship for a uniform bar is:

\[
\delta=\frac{PL}{AE}
\]

- Rearranging gives:

\[
P=\frac{AE}{L}\delta
\]

- Therefore, the axial stiffness of the bar is:

\[
k=\frac{AE}{L}
\]

- This has the same form as the spring relation:

\[
F=kx
\]

- Physical interpretation:
  - increasing \(P\) increases extension;
  - increasing \(L\) increases extension;
  - increasing \(A\) decreases extension;
  - increasing \(E\) decreases extension.

- In finite element form, scalar force and displacement are replaced by vectors, and scalar stiffness is replaced by a matrix.
- The element-level relationship was presented as:

\[
\mathbf{F}^{e}=\mathbf{K}^{e}\mathbf{D}^{e}
\]

- Individual element equations are transformed and combined into a global equation of the same general form:

\[
\mathbf{F}=\mathbf{K}\mathbf{D}
\]

- Here:
  - \(\mathbf{F}\) is the applied nodal load vector;
  - \(\mathbf{D}\) is the nodal deflection vector;
  - \(\mathbf{K}\) is the stiffness matrix.

- Although the mathematical displacement solution can be written formally as:

\[
\mathbf{D}=\mathbf{K}^{-1}\mathbf{F}
\]

  the lecturer indicated that the code should use a linear-system solver rather than explicitly focusing on matrix inversion. The automated transcript appears to refer to NumPy’s linear algebra solver, likely `np.linalg.solve`, but the function name is mistranscribed.

- After solving for \(\mathbf{D}\), the displacement vector can be used to determine:
  - reaction forces;
  - axial normal forces;
  - shear forces;
  - bending moments;
  - approximate motion at locations between nodes.

- The first element type studied is the axial bar or truss element.
- Its assumptions include:
  - adjacent elements are joined by pins;
  - supports and applied loads act at nodal points;
  - each member carries axial force only;
  - the cross-sectional area \(A\) is constant;
  - the elastic modulus \(E\) is constant;
  - the member length \(L\) is fixed in the undeformed configuration;
  - the material is homogeneous;
  - the member is prismatic;
  - the initial formulation neglects distributed axial loading, so the internal axial force is constant.

- Applying a transverse load partway along a nominal bar element introduces shear and bending moment.
- That violates the axial-only bar assumption.
- This is why the initial truss formulation restricts applied loads to nodal points.
- Later formulations will relax some of these assumptions and incorporate bending, shear, and distributed loading.

- Beam elements were described as carrying:
  - bending moment;
  - shear force;
  - lateral displacement;
  - rotation.
- Frame elements combine:
  - axial behaviour;
  - bending behaviour;
  - shear-related behaviour;
  - translations;
  - rotations.

- Nomenclature:
  - Circles around numbers denote node numbers.
  - Squares or boxes around numbers denote element numbers.
  - Each element has its own local node 1 and local node 2.
  - Different elements may therefore each possess a local node labelled 1 and a local node labelled 2, even though they occupy different positions in the global structure.

- For an individual element:
  - the local \(x_e\)-axis runs along the element from local node 1 toward local node 2;
  - the local \(y_e\)-axis is perpendicular to \(x_e\) in the plane;
  - the \(z\)-axis points out of the page;
  - the coordinate system follows the right-hand rule.
- Reversing the element’s node numbering also reverses its local \(x_e\)-direction and changes the corresponding local coordinate definition.
- Consistency between node ordering, coordinate direction, force signs, and matrix numbering is essential.

- Each element in a multi-element structure has its own local coordinate system.
- The global coordinate system, denoted using \(x_g\) and \(y_g\), describes the complete structure.
- Although the global axes may be chosen arbitrarily, the usual convention is:
  - \(x_g\): horizontal;
  - \(y_g\): vertical.

- The element orientation angle \(\alpha\) relates an element’s local axis to the global system.
- It is measured from \(x_g\) to \(x_e\).
- Counterclockwise rotation is positive.
- Clockwise rotation is negative.
- Equivalent angles differing by \(360^\circ\) produce the same sine and cosine values.
- The lecture example stated that:

\[
195^\circ \equiv -165^\circ
\]

- Both represent the same orientation.
- Positive \(165^\circ\), however, represents a different direction and would be incorrect for that example.

- Terminology used in the course:
  - A displacement or translation is the linear component of deflection and is measured in units of length.
  - A rotation is an angular component, measured in radians or milliradians.
  - Deflection is used as a general term encompassing both translations and rotations.
- Axial bar analysis initially involves translations only.
- Beam and frame analysis introduces rotational degrees of freedom.

- For a two-node axial bar:
  - node 1 is at \(x=0\);
  - node 2 is at \(x=L\);
  - the two axial nodal displacements are \(D_1\) and \(D_2\);
  - there is one axial degree of freedom at each node;
  - the unknown displacement field inside the element is \(u(x)\).

- The interpolation must satisfy the endpoint values:

\[
u(0)=D_1
\]

\[
u(L)=D_2
\]

- This was described as a boundary-value problem: values are known at the element boundaries, and internal behaviour is inferred from them.
- The interpolation equations are called shape functions.
- Shape functions connect the continuous internal displacement field to the discrete nodal solution.
- Once \(u(x)\) is known approximately, it can be differentiated to obtain strain and then used to obtain stress and internal force.

- For static equilibrium of an isolated bar element, the two end-force results must be equal in magnitude and opposite in sign when expressed using a consistent nodal sign convention.
- In the lecture’s convention, both nodal force components were drawn in the positive local \(x_e\)-direction.
- Consequently, equilibrium is represented by force components with opposite algebraic signs rather than by arrows initially drawn in opposite directions.

- For an infinitesimal bar segment of length \(dx\):
  - \(N(x)\) is the internal axial normal force;
  - \(dN\) is its change over \(dx\);
  - \(p(x)\) is the distributed axial load intensity.
- Force equilibrium produces a differential relationship between \(N(x)\) and \(p(x)\).
- The exact sign depends on the adopted load and force directions. The transcript contains inconsistent wording about this sign, but the later governing equation includes a leading negative derivative.

- The axial force is related to stress by:

\[
N=A\sigma
\]

- Linear elasticity gives:

\[
\sigma=E\varepsilon
\]

- For small axial deformation:

\[
\varepsilon=\frac{du}{dx}
\]

- Therefore:

\[
N=EA\frac{du}{dx}
\]

- Combining constitutive behaviour with equilibrium gives the axial-bar governing differential equation, presented in the lecture in the form:

\[
-\frac{d}{dx}\left(EA\frac{du}{dx}\right)=p(x)
\]

- Initially, the distributed axial load is set to zero:

\[
p(x)=0
\]

- Under constant \(E\) and \(A\), this implies a constant internal axial force and leads to a simple displacement field.
- Distributed axial loading will be introduced later.

- The general structural dynamics equation was recalled as:

\[
\mathbf{M}\ddot{\mathbf{x}}
+\mathbf{C}\dot{\mathbf{x}}
+\mathbf{K}\mathbf{x}
=
\mathbf{F}
\]

- For the static analysis covered here:

\[
\ddot{\mathbf{x}}=\mathbf{0},
\qquad
\dot{\mathbf{x}}=\mathbf{0}
\]

- The dynamic equation therefore reduces to the static stiffness equation:

\[
\mathbf{K}\mathbf{x}=\mathbf{F}
\]

- The same stiffness principles remain applicable in dynamic finite element models, but dynamics is outside the scope of this part of ENME302.

- The practical purpose of deriving these formulations is to understand what commercial finite element tools do internally.
- Packages mentioned in the transcript appear to include ANSYS, COMSOL, and Abaqus, although the automated transcription distorted some names.
- More advanced software may include:
  - three-dimensional solid elements;
  - nonlinear material or geometric behaviour;
  - large-deflection analysis.
- Despite greater complexity, these packages still use the same underlying ideas of discretisation, element formulation, assembly, constraints, solution, and result recovery.
- Results must always be interpreted physically. A numerical output is not automatically valid merely because software produced it.

- Course and assessment information stated in the lecture:
  - The first test is scheduled for Tuesday of Week 6, stated as 18 August.
  - It is expected to be an evening, computer-based test across computer laboratories.
  - The test is worth 25%.
  - Students will develop finite element code in the preceding laboratory sessions and bring that code into the test.
  - The laboratory work itself does not carry direct attendance or achievement marks, but it prepares the code and understanding required for the test.
  - Assignment 1 is worth 10%, is released near the end of the term, and is due shortly after the break or early in Week 7.
  - Online quizzes total 5%, apparently five quizzes worth 1% each.
  - Assignment 2 is stated as due on 13 October or in the final week of the semester.
  - Passing requires:
    - at least 40% in the final examination; and
    - at least 50% overall in the course.
  - The first part of the course covers structural finite elements.
  - The later part covers numerical solutions of partial differential equations, including elliptic PDEs.
  - The structural sequence is:
    - two-degree-of-freedom bar element;
    - four-degree-of-freedom beam element;
    - six-degree-of-freedom frame element.
  - The laboratory following this lecture was described as a Python and linear algebra refresher.

### Lecture 3

- Finite elements replace a continuous structure with simple elements connected at discrete nodes.
- Shape functions interpolate a continuous field inside an element from values calculated at its nodes.
- For the two-node axial bar, the nodal degrees of freedom are the axial displacements \(d_1\) and \(d_2\).
- The local coordinate runs consistently from node 1 to node 2:
  - \(x=0\) at node 1.
  - \(x=L\) at node 2.
- A linear displacement field is appropriate when:
  - The elastic modulus \(E\) is constant.
  - The cross-sectional area \(A\) is constant.
  - The distributed axial load \(p(x)\) is zero.
  - Consequently, the internal normal force, stress, and strain are constant within the element.
- The shape functions act as weighting or participation factors:
  - Near node 1, \(d_1\) has greater influence.
  - Near node 2, \(d_2\) has greater influence.
- Rigid-body translation occurs when \(d_1=d_2\). The element moves without changing length, so it develops no strain, stress, or internal force.
- The free axial bar stiffness matrix is singular because it permits rigid-body motion.
- A displacement boundary condition, such as fixing one node, removes the rigid-body mode and permits a unique solution.
- Element assumptions determine both the capabilities and limitations of the model.
- A continuously varying bar can be approximated using many short, piecewise-prismatic elements.

### Finite elements as building blocks

The finite element method begins with an element whose behaviour is simple, predictable, and repeatable. More complicated structures are assembled from these elements.

Although the course treats static equilibrium, the same general framework can be extended to dynamics by including mass, damping, acceleration, and velocity terms. The lecture did not develop the dynamic case further.

For a two-node axial element, both nodal forces and nodal displacements were defined as positive in the element’s positive \(x\)-direction. Static equilibrium therefore requires the two end forces to have equal magnitudes and opposite signs.

### Continuous behaviour from nodal values

The objective is to describe the continuous displacement field \(u(x)\), for \(0\leq x\leq L\), using only the nodal displacements \(d_1\) and \(d_2\).

This interpolation is fundamental to finite elements:

- The unknowns are solved at a finite number of discrete nodes.
- Shape functions make those nodal values representative of the continuous field within each element.
- Once nodal displacements are known, the same interpolation can be used to recover internal displacement, strain, stress, and force.

The assumptions embedded in the chosen interpolation also restrict which physical behaviour the element can represent.

### Axial equilibrium and the strong form

For an infinitesimal section of an axial bar, equilibrium relates the rate of change of internal normal force \(N(x)\) to the distributed axial load intensity \(p(x)\).

Using axial constitutive and kinematic relationships:

- \(N=EA\varepsilon\).
- \(\varepsilon=du/dx\).

The governing equation can therefore be expressed in terms of \(u(x)\). For the homogeneous problem studied in this lecture, the distributed load was set to zero:

\[
p(x)=0.
\]

With constant \(E\) and \(A\), this gives:

\[
\frac{d}{dx}\left(EA\frac{du}{dx}\right)=0,
\]

or equivalently:

\[
EA\frac{d^2u}{dx^2}=0.
\]

The displacement boundary conditions for the element are:

\[
u(0)=d_1,
\]

\[
u(L)=d_2.
\]

This differential equation together with its boundary conditions was described as the strong form of the boundary-value problem. The strong form is required to hold throughout the element.

### Linear displacement approximation

The displacement was assumed to have the straight-line form:

\[
u(x)=a_0+a_1x.
\]

This is analogous to \(y=mx+c\). Applying the nodal displacement conditions gives:

\[
u(0)=a_0=d_1,
\]

and:

\[
u(L)=a_0+a_1L=d_2.
\]

Therefore:

\[
a_1=\frac{d_2-d_1}{L}.
\]

Substitution gives:

\[
u(x)=d_1+\frac{d_2-d_1}{L}x.
\]

Grouping the nodal displacement terms:

\[
u(x)=\left(1-\frac{x}{L}\right)d_1+\frac{x}{L}d_2.
\]

The linear interpolation follows from the assumed constant material properties, constant cross-section, and zero distributed axial load. These assumptions imply constant axial force and therefore constant strain.

### Shape functions

Define the two shape functions:

\[
\psi_1(x)=1-\frac{x}{L},
\]

\[
\psi_2(x)=\frac{x}{L}.
\]

The displacement field is then:

\[
u(x)=\psi_1(x)d_1+\psi_2(x)d_2.
\]

In matrix form:

\[
u(x)=
\begin{bmatrix}
\psi_1(x) & \psi_2(x)
\end{bmatrix}
\begin{bmatrix}
d_1\\
d_2
\end{bmatrix}.
\]

Important properties include:

\[
\psi_1(0)=1,\qquad \psi_2(0)=0,
\]

\[
\psi_1(L)=0,\qquad \psi_2(L)=1,
\]

and:

\[
\psi_1(x)+\psi_2(x)=1.
\]

Thus:

- At node 1, the displacement is entirely determined by \(d_1\).
- At node 2, it is entirely determined by \(d_2\).
- Inside the element, displacement is a weighted combination of both nodal values.

At selected positions:

\[
u(0.5L)=0.5d_1+0.5d_2,
\]

\[
u(0.25L)=0.75d_1+0.25d_2,
\]

\[
u(0.75L)=0.25d_1+0.75d_2.
\]

The lecturer described shape functions as weighting factors or participation factors. For more complicated element types, the shape functions will not necessarily be linear.

### Numerical interpolation example

For an element with:

\[
L=1\ \text{m},\qquad d_1=0.1\ \text{m},\qquad d_2=0.2\ \text{m},
\]

the displacement field is:

\[
u(x)=\left(1-\frac{x}{L}\right)(0.1)+\frac{x}{L}(0.2).
\]

This gives:

\[
u(0.25L)=0.125\ \text{m},
\]

\[
u(0.5L)=0.150\ \text{m},
\]

\[
u(0.75L)=0.175\ \text{m}.
\]

The motion can be decomposed conceptually into:

- A rigid-body translation of \(0.1\ \text{m}\), because both ends move by at least that amount.
- An extension of \(0.1\ \text{m}\), because the relative nodal displacement is \(0.2-0.1=0.1\ \text{m}\).

Only the relative nodal displacement changes the element length and produces strain.

### Strain, stress, and normal force

Differentiating the displacement field gives the axial strain:

\[
\varepsilon(x)=\frac{du}{dx}
=\frac{d_2-d_1}{L}.
\]

The strain is constant throughout the element.

Using Hooke’s law:

\[
\sigma(x)=E\varepsilon
=E\frac{d_2-d_1}{L}.
\]

The axial normal force is:

\[
N(x)=A\sigma
=\frac{EA}{L}(d_2-d_1).
\]

This force is also constant throughout the element.

The change in element length is:

\[
\Delta L=d_2-d_1.
\]

Therefore:

\[
\varepsilon=\frac{\Delta L}{L},
\]

and:

\[
N=\frac{EA}{L}\Delta L.
\]

These results agree with the standard mechanics-of-materials description of axial deformation.

### Rigid-body motion versus deformation

The absolute nodal displacements do not by themselves determine strain. Strain depends on their difference:

\[
\varepsilon=\frac{d_2-d_1}{L}.
\]

If:

\[
d_1=d_2=c,
\]

then:

\[
\Delta L=0,\qquad \varepsilon=0,\qquad \sigma=0,\qquad N=0.
\]

The element may translate by any value \(c\), but it does not deform. This is rigid-body motion.

Examples given in the lecture included:

- \(d_1=d_2=1\ \text{m}\).
- \(d_1=d_2=5\ \text{m}\).

In both cases, the element changes position but does not stretch or compress.

### Element end forces

Using the lecture’s sign convention, the end forces are:

\[
F_1=\frac{EA}{L}(d_1-d_2),
\]

\[
F_2=\frac{EA}{L}(d_2-d_1).
\]

Hence:

\[
F_1=-F_2,
\]

as required by static equilibrium when there is no distributed axial load.

If \(d_1>d_2\), the element shortens. Under the stated force convention, the resulting end forces point inward and represent compression.

If \(d_2>d_1\), the element lengthens and the end forces represent tension.

### Axial bar stiffness matrix

The end-force equations can be written as:

\[
\begin{bmatrix}
F_1\\
F_2
\end{bmatrix}
=
\frac{EA}{L}
\begin{bmatrix}
1 & -1\\
-1 & 1
\end{bmatrix}
\begin{bmatrix}
d_1\\
d_2
\end{bmatrix}.
\]

Thus, the element stiffness matrix is:

\[
\mathbf{k}^{(e)}
=
\frac{EA}{L}
\begin{bmatrix}
1 & -1\\
-1 & 1
\end{bmatrix}.
\]

The stiffness relation is:

\[
\mathbf{f}^{(e)}=\mathbf{k}^{(e)}\mathbf{d}^{(e)}.
\]

This was described as Hooke’s law written in matrix form: the stiffness matrix relates applied nodal forces to corresponding nodal displacements.

### Singularity of the unconstrained element

The two scalar equations represented by the stiffness relation are not independent. The second row of the stiffness matrix is the negative of the first row.

Its determinant is:

\[
\det\left(\mathbf{k}^{(e)}\right)
=
\left(\frac{EA}{L}\right)^2
\det
\begin{bmatrix}
1 & -1\\
-1 & 1
\end{bmatrix}
=0.
\]

Therefore, the unconstrained element stiffness matrix is singular and cannot be inverted to obtain a unique displacement solution.

The rigid-body displacement vector:

\[
\begin{bmatrix}
d_1\\
d_2
\end{bmatrix}
=
c
\begin{bmatrix}
1\\
1
\end{bmatrix}
\]

produces:

\[
\mathbf{k}^{(e)}
c
\begin{bmatrix}
1\\
1
\end{bmatrix}
=
\begin{bmatrix}
0\\
0
\end{bmatrix}.
\]

There are infinitely many rigid-body translations, with \(c\) ranging over all real values. A support or prescribed displacement is therefore required to prevent free translation and obtain a unique solution.

This explains finite element software warnings such as:

- “Rigid body modes detected.”
- “Insufficient constraints.”
- “Weak springs added to constrain rigid-body motion.”

Weak springs may allow a solver to proceed numerically, but the underlying issue is that the model has not been adequately constrained.

### Element assumptions and mesh refinement

A single linear axial bar element is not generally appropriate when \(E\) or \(A\) varies substantially along its length.

For example, if a bar tapers:

- The normal force may remain constant.
- The stress varies because \(\sigma=N/A(x)\).
- The strain varies because \(\varepsilon=\sigma/E\).
- The displacement is therefore not linear in \(x\).

The lecturer identified two broad options:

1. Develop or choose a different element whose formulation represents the varying properties.
2. Approximate the varying bar using many smaller elements, each with approximately constant properties.

The second approach produces a piecewise-linear approximation. Increasing the number of elements allows the stepped finite element representation to better approximate the continuously varying geometry.

### Why formal shape functions are needed

Linear interpolation for an axial bar may be easy to perform mentally, but more complicated structural behaviour is not.

The lecture used a cantilever beam to illustrate that beam deflection is curved and generally requires higher-order interpolation. When multiple actions such as shear force and applied moment contribute to deformation, internal displacement cannot be inferred reliably using simple linear weighting.

The same finite element framework can accommodate both simple axial elements and more complicated beam or frame elements by changing the appropriate shape functions and element formulation.

### Two purposes of shape functions

The lecture summarised two main purposes:

1. **Constructing the finite element equations**
   - They permit a continuous field to be represented using values at selected discrete nodes.
   - They are part of the mathematical framework used to solve for nodal displacements.

2. **Recovering internal element behaviour**
   - Once the nodal displacements are known, shape functions interpolate the internal displacement field.
   - Derivatives and constitutive relationships then provide strain, stress, and internal force.

The lecturer described this as shape functions both “building up” the finite element model and “breaking down” the solved nodal results into internal element behaviour.

### Python lab preview

The associated lab was described as a Python refresher focused on tools needed for later finite element coding.

Topics included:

- Array and matrix entry.
- Variable assignment versus copying:
  - An assignment such as `B = A` may make both names refer to the same underlying array.
  - An explicit copy is needed when an independent array is required.
- Building larger matrices from smaller submatrices.
- Matrix multiplication:
  - Use `np.matmul(A, B)` or `A @ B`.
  - `A * B` performs element-by-element multiplication for NumPy arrays and is not the matrix operation intended in this part of the course.
- Solving systems of linear equations.
- Plotting lines and locating their intersection.
- Entering large or small values using scientific notation.
- Formatting printed output so variables and large matrices are easier to read and debug.
- Using an IDE variable explorer where appropriate.

Clear output formatting was emphasised because it helps both interpretation and debugging.

### Lecture 4

- A structural degree of freedom is assigned wherever a non-zero displacement is kinematically possible, even if that displacement happens to be zero under one particular load case.
- Lowercase \(q\) denotes allowable global displacements or degrees of freedom; uppercase \(Q\) denotes the corresponding applied global loads.
- Restrained support displacements are zero and therefore are not included among the allowable global degrees of freedom in this example.
- For a pin-jointed bar or truss member:
  - Positive axial force denotes tension.
  - Negative axial force denotes compression.
  - Axial deformation follows from force, length, area, and elastic modulus.
- Exact nodal compatibility requires the connected members to satisfy their deformed lengths simultaneously.
- Small-deflection analysis assumes that the initial geometry is a sufficiently accurate approximation to the displaced geometry.
- The work done by a constant force is \(W=P\delta\), but the work done by a force that increases linearly from zero to \(P\) is \(W=\tfrac12P\delta\).
- Under slow, static, conservative loading, external work is converted into internal strain energy.
- The single-load work-energy method can determine only the displacement:
  - At the location of the single applied load.
  - In the direction of that load.
- With multiple loads, one scalar energy equation contains multiple unknown displacement components, so the single-load method cannot determine them independently.
- Virtual work overcomes this limitation by introducing a separate virtual load system.
- The virtual load is normally assigned unit magnitude for convenience, but any magnitude can be used if the final result is divided by that magnitude.
- Real and virtual load systems are analysed independently:
  - Uppercase \(F_i\): internal member force caused by the real loads.
  - Lowercase \(f_i\): internal member force caused by the virtual load.
- Virtual internal forces can be interpreted as influence or weighting factors that determine how strongly each member’s real deformation contributes to the requested displacement.

- The annotated lab sheet was made available on the course Learn page alongside the original lab sheet.
- Useful NumPy operations reviewed:
  - `A.T` returns the transpose of array \(A\).
  - `np.block` assembles a larger array from smaller arrays or submatrices.
  - `np.matmul(A, B)` and `A @ B` perform matrix multiplication.
  - `A * B` performs element-by-element multiplication.
- Plot labels can contain LaTeX-style expressions by enclosing mathematical text in dollar signs.
- Readable output is important when comparing large stiffness matrices against intermediate results in the notes. Printing a newline before an array can prevent its first row from being offset and make columns easier to inspect.

- The structural example contains:
  - Two pin-jointed axial members.
  - Member 1 horizontal.
  - Member 2 inclined at \(45^\circ\).
  - Fixed pin locations at the left side.
  - A movable joint \(C\) with horizontal and vertical displacement components.
  - External loads \(Q_1=0\) horizontally and \(Q_2=100\ \text{kN}\) upward.
- The movable joint has two global degrees of freedom:
  - \(q_1\): horizontal displacement.
  - \(q_2\): vertical displacement.
- Each displacement degree of freedom has a corresponding load component:
  - \(q_1\) pairs with \(Q_1\).
  - \(q_2\) pairs with \(Q_2\).
- A degree of freedom is retained because displacement is possible, not because the corresponding load is necessarily non-zero. Thus \(q_1\) exists even though \(Q_1=0\).

- A free-body diagram around joint \(C\) gives the member forces:
  - Vertical equilibrium gives member 2 in tension:
    \[
    F_2=141.42\ \text{kN}=100\sqrt{2}\ \text{kN}.
    \]
  - Horizontal equilibrium gives:
    \[
    F_1=-100\ \text{kN},
    \]
    so member 1 carries \(100\ \text{kN}\) in compression.
- Using the axial-deformation relation:
  - Member 1 contracts by approximately \(0.637\ \text{mm}\).
  - Member 2 extends by approximately \(1.27\ \text{mm}\).
- The transcript does not state the individual numerical values of \(L_i\), \(A_i\), or \(E_i\), so the deformation calculations cannot be independently reconstructed from the transcript alone.

- Exact geometric compatibility can be visualised as follows:
  - Draw an arc centred at the fixed support of member 1 with radius equal to member 1’s compressed length.
  - Draw another arc centred at the fixed support of member 2 with radius equal to member 2’s extended length.
  - The intersection of the two arcs gives the exact displaced position of joint \(C\).
- Solving the true arc intersection directly is cumbersome.
- The lecture therefore linearises the geometry:
  - Curved compatibility loci are replaced by local straight-line approximations.
  - Changes in member orientation are neglected to first order.
  - Second-order geometric terms are omitted.
  - The original \(45^\circ\) member angle is used as an approximation to the displaced angle.
- The linearised geometric construction gives:
  - Horizontal displacement of joint \(C\): approximately \(0.637\ \text{mm}\) to the left.
  - Vertical displacement of joint \(C\): \(2.432\ \text{mm}\) upward.
- This manual compatibility method requires diagrams and trigonometric reasoning even for a two-member structure. It becomes impractical when:
  - More members are added.
  - Intermediate joints also move.
  - The displacement datum for one member depends on the displacement of another joint.
- A more systematic method is therefore required for larger structures.

- In the work-energy method:
  - Applied loads do external work.
  - Internal member forces produce internal work, stored as strain energy.
  - For slow, gradually applied static loading, damping, heat generation, and dynamic effects are neglected.
  - External work is equated to internal strain energy.
- For a linear elastic axial bar loaded gradually from zero to \(P\):
  - The force-displacement curve is linear.
  - Work is the triangular area under that curve.
  - Therefore \(W=\tfrac12P\delta\), not \(P\delta\).
- The expression \(W=P\delta\) applies when the force remains constant throughout the displacement, such as:
  - Slowly lifting an object whose weight remains constant.
  - Sliding an object against an approximately constant friction force.
- For a prismatic linear-elastic axial member:
  \[
  U_i=\frac{F_i^2L_i}{2A_iE_i}.
  \]
- For multiple members, total strain energy is the sum of the member contributions:
  \[
  U_{\text{total}}=\sum_i U_i.
  \]

- Applying the single-load work-energy method to the two-member structure gives:
  - Member 1 strain energy:
    \[
    U_1=31.83\ \text{J}.
    \]
  - Member 2 strain energy:
    \[
    U_2=89.76\ \text{J}.
    \]
  - Total strain energy:
    \[
    U_{\text{total}}=121.59\ \text{J}.
    \]
- Equating this to the external work from the \(100\ \text{kN}\) vertical load:
  \[
  U_{\text{total}}=\frac12P\delta_y
  \]
  gives:
  \[
  \delta_y=2.432\ \text{mm}.
  \]
- This agrees with the earlier geometric compatibility result.
- The single-load method cannot determine the horizontal displacement because:
  - There is no horizontal applied load whose work contains \(\delta_x\).
  - The scalar energy equation therefore contains no term that isolates \(\delta_x\).
- If both horizontal and vertical loads were applied:
  \[
  U_{\text{total}}
  =
  \frac12P_1\delta_y+\frac12P_2\delta_x.
  \]
  Even if all member forces and \(U_{\text{total}}\) were known, this would be one equation containing two unknown displacements.

- The method of virtual work extends the energy approach to:
  - Multiply loaded structures.
  - Displacements at locations where no real load acts.
  - Displacements in directions different from those of the real loads.
- The lecture’s formal statement was that, for a body in equilibrium under a virtual force system and subjected to small compatible real displacements:
  - External virtual work equals internal virtual work.
  - Virtual external forces act through real external displacements.
  - Virtual internal forces act through real internal displacements.
- Procedural application to a truss:
  1. Analyse the structure under the real external loads only.
  2. Determine the real internal member forces \(F_i\).
  3. Remove or ignore the real loads for the virtual analysis.
  4. Apply a virtual load at the point where displacement is required.
  5. Orient the virtual load in the direction of the required displacement.
  6. Determine the virtual internal member forces \(f_i\).
  7. Substitute the real and virtual member forces into the virtual-work equation.
  8. Sum the contributions from all members.
- Superposition is central to the procedure:
  - Analyse the real system while ignoring the virtual system.
  - Analyse the virtual system while ignoring the real system.
  - Combine their effects only in the virtual-work summation.

- To find the horizontal displacement of joint \(C\):
  - Apply a unit virtual load horizontally at \(C\).
  - Ignore the real \(100\ \text{kN}\) vertical load while solving the virtual system.
  - Virtual vertical equilibrium gives:
    \[
    f_2=0,
    \]
    because no other virtual vertical force is available to balance a vertical component in member 2.
  - Virtual horizontal equilibrium gives:
    \[
    f_1=1
    \]
    in the sign convention used for the virtual analysis.
  - The virtual-work summation gives a horizontal displacement of approximately:
    \[
    \delta_x=-0.636\ \text{mm}.
    \]
  - The negative sign means the actual displacement is opposite to the assumed positive horizontal virtual-load direction, corresponding to motion to the left.
  - The earlier geometric result was reported as \(0.637\ \text{mm}\) left; the \(0.001\ \text{mm}\) difference appears to be rounding.

- To find the vertical displacement of joint \(C\):
  - Retain the same real-force solution because the real loading has not changed.
  - Replace the horizontal virtual load with a vertical unit virtual load at \(C\).
  - The virtual member forces are approximately:
    \[
    f_2=1.41
    \]
    in tension and
    \[
    f_1=-1
    \]
    in compression.
  - Recalculate only the virtual-force column and the resulting virtual-work terms.
  - The result is:
    \[
    \delta_y=2.432\ \text{mm}
    \]
    upward.
- Once the real member forces are known, they can be reused for different requested displacement components. Only the virtual load case and corresponding \(f_i\) values must be changed.

- The lecturer suggested interpreting the virtual internal forces as weighting factors:
  - A member with \(f_i=0\) contributes nothing to the requested displacement in the virtual-work sum.
  - A non-zero \(f_i\) indicates that the member’s real axial deformation influences that displacement.
  - Members outside the relevant load path may receive zero virtual weighting.
- The demonstrated structure is statically determinate, so both real and virtual member forces can be found directly using equilibrium.
- For statically indeterminate or overconstrained structures, determining those forces is more difficult and requires a more general method.
- Virtual work is introduced here because it is fundamental to deriving stiffness matrices and assembling larger structural systems.

## Equations and worked patterns

### Lecture 1

- **Normal stress in an axially loaded member**
  \[
  \sigma=\frac{N}{A}
  \]
  where:
  - \(\sigma\) is normal stress,
  - \(N\) is the internal axial force,
  - \(A\) is cross-sectional area.

- **Area of a hollow circular section**
  \[
  A=\frac{\pi}{4}\left(D_o^2-D_i^2\right)
  \]
  with:
  \[
  D_i=D_o-2t
  \]
  where:
  - \(D_o\) is outside diameter,
  - \(D_i\) is inside diameter,
  - \(t\) is wall thickness.
  
  The lecture’s example truss used aluminium pipes with \(D_o=42\ \text{mm}\) and \(t=3.5\ \text{mm}\), but no member-force or stress results were provided.

- **Static equilibrium in a planar problem**
  \[
  \sum F_x=0,\qquad \sum F_y=0,\qquad \sum M=0
  \]

- **Tip-loaded cantilever bending moment**
  \[
  M(x)=-P(L-x)=-PL+Px
  \]
  for the sign convention used in the lecture.

- **Euler–Bernoulli moment-curvature relation**
  \[
  EI\frac{d^2v}{dx^2}=M(x)
  \]
  where:
  - \(E\) is Young’s modulus,
  - \(I\) is the second moment of area,
  - \(v(x)\) is transverse deflection,
  - \(M(x)\) is bending moment.
  
  The exact sign may change with the chosen conventions for displacement, curvature, and moment.

- **Tip deflection magnitude for a tip-loaded cantilever**
  \[
  \delta_{\text{tip}}=\frac{PL^3}{3EI}
  \]

- **Tip rotation magnitude for a tip-loaded cantilever**
  \[
  \theta_{\text{tip}}=\frac{PL^2}{2EI}
  \]

- **Fixed-end boundary conditions for the cantilever**
  \[
  v(0)=0,\qquad \frac{dv}{dx}(0)=0
  \]

- **Interpolation using shape functions**
  \[
  u(x)\approx\sum_{i=1}^{n}N_i(x)u_i
  \]
  where:
  - \(u(x)\) is the approximated field value inside an element,
  - \(N_i(x)\) is the shape function associated with node \(i\),
  - \(u_i\) is the nodal value,
  - \(n\) is the number of element nodes.
  
  This general expression was not explicitly written in the transcript, but it accurately formalises the lecturer’s verbal definition of shape functions.

- **Statically determinate**
  - Stable with only the minimum required constraints.
  - Internal forces and reactions can be obtained from equilibrium alone.
  - Member stiffness is not required to determine the force distribution.

- **Statically indeterminate**
  - Contains constraints or members beyond the minimum required for stability.
  - Equilibrium equations alone do not provide enough information.
  - Compatibility, deformation, and relative stiffness are required to determine the force distribution.

- **Axial truss element**
  - Carries tension or compression only.
  - Has no shear force or bending moment under the ideal truss assumptions.
  - Is connected by ideal pins and loaded at nodes.

- **Shape function**
  - A function that interpolates a field inside an element from nodal values.

- **Degree of freedom**
  - An independent nodal translation or rotation included in the model.

- **Mesh**
  - A discretised representation of a domain consisting of elements and nodes.

- **Eigenvalue buckling analysis**
  - A numerical analysis used to estimate idealised critical buckling loads and corresponding buckling modes.

### Lecture 2

- Axial extension of a uniform bar:

\[
\delta=\frac{PL}{AE}
\]

- Axial force–deflection form:

\[
P=\frac{AE}{L}\delta
\]

- Axial stiffness:

\[
k=\frac{AE}{L}
\]

- Scalar Hooke’s law:

\[
F=kx
\]

- Element finite element equation:

\[
\mathbf{F}^{e}=\mathbf{K}^{e}\mathbf{D}^{e}
\]

- Global finite element equation:

\[
\mathbf{F}=\mathbf{K}\mathbf{D}
\]

- Formal displacement solution:

\[
\mathbf{D}=\mathbf{K}^{-1}\mathbf{F}
\]

- Axial strain:

\[
\varepsilon=\frac{du}{dx}
\]

- Linear elastic stress–strain relation:

\[
\sigma=E\varepsilon
\]

- Internal normal force:

\[
N=A\sigma
\]

- Combined force–displacement relation:

\[
N=EA\frac{du}{dx}
\]

- Governing equation for an axially loaded bar:

\[
-\frac{d}{dx}\left(EA\frac{du}{dx}\right)=p(x)
\]

- Initial no-distributed-load assumption:

\[
p(x)=0
\]

- Axial displacement boundary values:

\[
u(0)=D_1,
\qquad
u(L)=D_2
\]

- General dynamic structural equation:

\[
\mathbf{M}\ddot{\mathbf{x}}
+\mathbf{C}\dot{\mathbf{x}}
+\mathbf{K}\mathbf{x}
=
\mathbf{F}
\]

- Static assumptions:

\[
\ddot{\mathbf{x}}=\mathbf{0},
\qquad
\dot{\mathbf{x}}=\mathbf{0}
\]

- \(A\): cross-sectional area.
- \(E\): elastic modulus.
- \(L\): original element length.
- \(P\): applied axial point load.
- \(\delta\): total axial extension.
- \(k\): scalar axial stiffness.
- \(\mathbf{K}^{e}\): element stiffness matrix.
- \(\mathbf{K}\): assembled global stiffness matrix.
- \(\mathbf{F}^{e}\): element nodal force vector.
- \(\mathbf{F}\): global applied nodal load vector.
- \(\mathbf{D}^{e}\): element nodal deflection vector.
- \(\mathbf{D}\): global nodal deflection vector.
- \(u(x)\): approximate axial displacement field within an element.
- \(D_1,D_2\): axial displacements at local nodes 1 and 2.
- \(N(x)\): internal axial normal force.
- \(p(x)\): distributed axial load intensity.
- \(\sigma\): axial normal stress.
- \(\varepsilon\): axial strain.
- \(x_e,y_e\): local element coordinates.
- \(x_g,y_g\): global structural coordinates.
- \(\alpha\): counterclockwise orientation angle from \(x_g\) to \(x_e\).
- Node: a discrete connection, support, or loading point at which degrees of freedom are defined.
- Degree of freedom: an independent displacement or rotation used to describe structural motion.
- Prismatic bar: a bar with constant cross-sectional area along its length.
- Homogeneous bar: a bar with constant material properties, including \(E\), along its length.
- Shape function: an interpolation function that expresses behaviour inside an element in terms of nodal values.
- Discretisation: replacement of a continuous structure with a finite collection of connected elements.
- Boundary condition: a prescribed displacement, rotation, force, or other condition at a boundary or node.
- Translation: a linear displacement measured in units of length.
- Rotation: an angular displacement measured in radians.
- Deflection: the general term used for translations and rotations.

### Lecture 3

- **Local element coordinate**
  \[
  0\leq x\leq L,
  \]
  with \(x=0\) at node 1 and \(x=L\) at node 2.

- **Nodal displacement conditions**
  \[
  u(0)=d_1,\qquad u(L)=d_2.
  \]

- **Homogeneous axial equilibrium equation**
  \[
  \frac{d}{dx}\left(EA\frac{du}{dx}\right)=0.
  \]

- **Linear displacement assumption**
  \[
  u(x)=a_0+a_1x.
  \]

- **Interpolation constants**
  \[
  a_0=d_1,\qquad a_1=\frac{d_2-d_1}{L}.
  \]

- **Axial displacement field**
  \[
  u(x)=\left(1-\frac{x}{L}\right)d_1+\frac{x}{L}d_2.
  \]

- **Shape functions**
  \[
  \psi_1(x)=1-\frac{x}{L},\qquad
  \psi_2(x)=\frac{x}{L}.
  \]

- **Partition of unity**
  \[
  \psi_1(x)+\psi_2(x)=1.
  \]

- **Shape-function interpolation**
  \[
  u(x)=\psi_1(x)d_1+\psi_2(x)d_2.
  \]

- **Axial strain**
  \[
  \varepsilon=\frac{du}{dx}=\frac{d_2-d_1}{L}.
  \]

- **Change in length**
  \[
  \Delta L=d_2-d_1.
  \]

- **Engineering strain**
  \[
  \varepsilon=\frac{\Delta L}{L}.
  \]

- **Normal stress**
  \[
  \sigma=E\varepsilon
  =E\frac{d_2-d_1}{L}.
  \]

- **Normal force**
  \[
  N=A\sigma
  =\frac{EA}{L}(d_2-d_1).
  \]

- **Element end forces**
  \[
  F_1=\frac{EA}{L}(d_1-d_2),
  \qquad
  F_2=\frac{EA}{L}(d_2-d_1).
  \]

- **Element stiffness equation**
  \[
  \mathbf{f}^{(e)}=\mathbf{k}^{(e)}\mathbf{d}^{(e)}.
  \]

- **Element stiffness matrix**
  \[
  \mathbf{k}^{(e)}
  =
  \frac{EA}{L}
  \begin{bmatrix}
  1 & -1\\
  -1 & 1
  \end{bmatrix}.
  \]

- **Rigid-body mode**
  \[
  \mathbf{d}^{(e)}
  =
  c
  \begin{bmatrix}
  1\\
  1
  \end{bmatrix},
  \qquad
  \mathbf{k}^{(e)}\mathbf{d}^{(e)}=\mathbf{0}.
  \]

- **Singular matrix**
  
  A matrix with zero determinant and no inverse. The unconstrained axial element stiffness matrix is singular because it permits rigid-body translation.

- **Shape function**
  
  A function that interpolates a field inside an element from its nodal values. It can be interpreted as a position-dependent weighting or participation factor.

- **Strong form**
  
  The governing differential equation and boundary conditions that must be satisfied pointwise throughout the domain.

- **Rigid-body motion**
  
  Motion that changes the position or orientation of an element without producing deformation, strain, stress, or internal force.

- **Prismatic element**
  
  An element with constant cross-sectional area along its length.

- **Homogeneous material**
  
  A material whose relevant properties, here particularly \(E\), are constant throughout the element.

### Lecture 4

- Global displacement and load vectors:
  \[
  \mathbf q=
  \begin{bmatrix}
  q_1\\
  q_2
  \end{bmatrix},
  \qquad
  \mathbf Q=
  \begin{bmatrix}
  Q_1\\
  Q_2
  \end{bmatrix}.
  \]
  - \(q_i\): allowable global displacement or degree of freedom.
  - \(Q_i\): applied global load corresponding to \(q_i\).

- Axial deformation of a prismatic, linear-elastic bar:
  \[
  \delta_i=\frac{F_iL_i}{A_iE_i}.
  \]
  - \(F_i\): axial member force.
  - \(L_i\): member length.
  - \(A_i\): cross-sectional area.
  - \(E_i\): Young’s modulus.
  - The sign of \(F_i\) determines extension or contraction under the adopted convention.

- Work under a general force-displacement relation:
  \[
  W=\int_0^\delta P\,d\delta.
  \]

- Constant force:
  \[
  W=P\delta.
  \]

- Linearly increasing force from zero to \(P\):
  \[
  W=\frac12P\delta.
  \]

- Strain energy in one prismatic axial member:
  \[
  U_i=\frac{F_i^2L_i}{2A_iE_i}.
  \]

- Total strain energy:
  \[
  U_{\text{total}}
  =
  \sum_i\frac{F_i^2L_i}{2A_iE_i}.
  \]

- Single-load work-energy condition:
  \[
  U_{\text{total}}=W_{\text{external}}
  =\frac12P\delta.
  \]

- Multiple-load external work for independently and proportionally increased linear loads:
  \[
  W_{\text{external}}
  =
  \frac12P_1\delta_1+\frac12P_2\delta_2+\cdots.
  \]
  In the lecture’s illustrative two-load case:
  \[
  U_{\text{total}}
  =
  \frac12P_1\delta_y+\frac12P_2\delta_x.
  \]

- Virtual-work equation for a truss:
  \[
  P_v\Delta
  =
  \sum_i\frac{f_iF_iL_i}{A_iE_i}.
  \]
  For a unit virtual load, \(P_v=1\):
  \[
  \Delta
  =
  \sum_i\frac{f_iF_iL_i}{A_iE_i}.
  \]

- Definitions in the virtual-work equation:
  - \(P_v\): virtual external load applied at the point and in the direction of the requested displacement.
  - \(\Delta\): real displacement caused by the real loading, measured at the virtual load’s point and in its direction.
  - \(F_i\): real internal axial force in member \(i\), produced by the real external loads.
  - \(f_i\): virtual internal axial force in member \(i\), produced by the virtual external load alone.
  - \(L_i\): length of member \(i\).
  - \(A_i\): cross-sectional area of member \(i\).
  - \(E_i\): Young’s modulus of member \(i\).
  - Positive and negative results indicate whether the real displacement is in the same or opposite direction to the chosen virtual load.

- Numerical results for the lecture example:
  \[
  F_1=-100\ \text{kN},
  \qquad
  F_2=141.42\ \text{kN}.
  \]
  \[
  \Delta L_1\approx-0.637\ \text{mm},
  \qquad
  \Delta L_2\approx+1.27\ \text{mm}.
  \]
  \[
  U_1=31.83\ \text{J},
  \qquad
  U_2=89.76\ \text{J},
  \qquad
  U_{\text{total}}=121.59\ \text{J}.
  \]
  \[
  \delta_x\approx-0.636\text{ to }-0.637\ \text{mm},
  \qquad
  \delta_y=+2.432\ \text{mm}.
  \]

## Warnings and deadlines

### Lecture 1 — historical source caveats

- These notes are based on a native Echo automated transcript, so names, Māori text, room identifiers, and some technical terms were transcribed unreliably.
- The course was repeatedly transcribed as “NMA 302” rather than ENME302.
- “Finite element analysis” was sometimes transcribed as “find element analysis,” “final solution,” or “fun elements.” These have been interpreted as finite element analysis where the context is clear.
- “Shear” was repeatedly transcribed as “sheer.”
- “PDEs” appears to have been transcribed once as “PDAs.”
- “Euler buckling analysis” appears to have been transcribed as “oiler buckling analysis.”
- “Spherical plain bearing” appears to have been transcribed as “spherical plane bearing.”
- The transcript says “390-minute sessions” for Thursday computer labs. This may mean “three 90-minute sessions,” but the exact timetable should be checked against the official course-information system.
- The Monday and Wednesday–Friday room descriptions are unclear in the transcript. The lecturer identified the central timetabling system as the source of truth.
- A post-lecture exchange suggests students may be allowed to bring code into the week 6 test and possibly a self-prepared page of material. The recording is fragmented, so the exact test-resource rules should be confirmed from official course instructions.
- The transcript clearly states the test date as Tuesday 18 August and the final-exam hurdle as 40%, but the lecturer also stated that the assessment schedule remained provisional until the end of week 2.
- The cantilever deflection phrase was poorly transcribed as something resembling “PLQ 3 I.” It has been interpreted as the standard result \(PL^3/(3EI)\), consistent with the surrounding beam discussion.
- The general shape-function interpolation equation was included to formalise the lecturer’s verbal explanation. It was not explicitly presented in symbolic form during this transcript.
- The lecturer described greater structural restraint and redundancy as generally improving safety. This is a broad introductory statement, not a universal design rule; redundancy, stiffness, ductility, failure modes, and load redistribution must all be assessed.
- Eigenvalue buckling predicts an idealised elastic critical load. The lecture did not discuss imperfections, material nonlinearity, residual stresses, or nonlinear post-buckling behaviour, all of which may reduce real buckling capacity.

### Lecture 2 — historical source caveats

- These notes are based on a native Echo automated transcript, which contains substantial recognition errors.
- Terms transcribed as “fire element,” “final element,” and similar variants have been interpreted as “finite element.”
- “To fictions” and “dyslexion” have been interpreted from context as “deflections.”
- “Actual force” has generally been interpreted as “axial force.”
- The commercial package names appear to be ANSYS, COMSOL, and Abaqus, but the transcript records distorted versions.
- The numerical solver reference appears to be `np.linalg.solve`, but the audio was transcribed as “NP dot Glenelg”; this identification is probable rather than certain.
- The transcript gives inconsistent spoken signs for the differential equilibrium equation. It first appears to state \(dN/dx=p\), while the later displayed governing equation is described with a leading negative derivative. The notes preserve the later form:

\[
-\frac{d}{dx}\left(EA\frac{du}{dx}\right)=p(x)
\]

  The exact sign must be checked against the lecturer’s written notes and adopted force convention.
- The transcript does not provide the explicit two-node bar shape functions or element stiffness matrix, so they have not been added.
- The quiz timing is inconsistent: one passage says quizzes begin in Week 6, while another appears to say Week 10 and then mentions Weeks 6 to 10. Confirm the official schedule on the course page.
- Assignment 2 is described both as due on 13 October and as due in the final week of the semester; these may be consistent, but the official course schedule should be checked.
- The post-lecture discussion appears to state that one side of an A4 sheet may be permitted in the test and that full books are not permitted. The audio is fragmented, so this test-material rule should be confirmed from the official assessment instructions.
- A private post-lecture student discussion was poorly captured and is unrelated to the technical lecture content; it has not been incorporated.

### Lecture 3 — historical source caveats

- The source is a native Echo automated transcript and contains numerous recognition errors. Examples include “stamping matrix” for damping matrix, “electric modules” for elastic modulus, and “final element method” for finite element method.
- Some equations were being displayed or handwritten rather than spoken completely. The notes reconstruct equations only where the surrounding statements make the intended form sufficiently clear.
- The transcript’s spoken sign description for distributed loading is ambiguous. Depending on the chosen force convention, axial equilibrium may be written as \(dN/dx+p=0\) or with the opposite sign for \(p\). The zero-load result used in this lecture is unaffected:
  \[
  \frac{d}{dx}\left(EA\frac{du}{dx}\right)=0.
  \]
- The lecturer stated that a tapered bar would require a “parabolic equation.” This should be treated as a qualitative indication that linear interpolation may no longer be adequate, not as a general rule that every varying-area bar has a parabolic displacement field.
- The cantilever-beam example is unclear and appears internally questionable in the automated transcript. The lecturer stated a tip deflection of \(PL^3/(3EI)\), described the displacement as cubic, and then used the cube of \(0.5\) to infer a halfway value of \(0.0125\ \text{m}\) for a \(0.1\ \text{m}\) tip displacement. The exact cantilever deflection field was not captured clearly enough to endorse that interpolation. The transcript later confirms that the intended unit was metres rather than millimetres.
- The post-lecture discussion about lab session times is heavily corrupted and was not included as reliable course content.

### Lecture 4 — historical source caveats

- The source is an automated Echo transcript and contains transcription errors, fragmented sentences, and ambiguous references to diagrams that are not embedded in the transcript.
- The transcript sometimes renders “truss” as “trust,” “strain energy” incorrectly, and `np.matmul` as “NP mat mole.” These have been normalised in the notes.
- The transcript verbally refers to lowercase and uppercase “Q” in places where the intended notation is evidently lowercase \(q\) for displacement and uppercase \(Q\) for load.
- Several derivations depend on diagrams from the lecture notes, especially the member geometry, arc construction, quadrilateral construction, and virtual-work tables. Their full layout cannot be recovered from the transcript alone.
- The member lengths, cross-sectional areas, and elastic moduli used to obtain the numerical deformations and strain energies are not stated clearly in the transcript.
- The claim around 18 minutes that a constructed triangle is “equilateral” may be a transcription error or may depend on the unseen diagram. The reliable stated result is a vertical displacement of \(2.432\ \text{mm}\).
- The horizontal displacement is reported as both \(0.637\ \text{mm}\) left and \(-0.636\ \text{mm}\). This is most likely rounding.
- The transcript inconsistently refers to virtual-load units as newtons or kilonewtons. A consistent unit system must be used throughout any calculation.
- The lecture’s post-class discussion after approximately 50 minutes is largely unintelligible. It appears to confirm that virtual-work results still rely on a linear or small-deflection approximation, but the details cannot be recovered reliably.
- All demonstrated structural calculations assume small displacement, linear elasticity, compatible deformation, static equilibrium, and applicability of superposition. Large geometric changes would require additional nonlinear analysis steps.

## Recall questions

1. Lecture 1: What is the fundamental principle of finite element analysis?

2. Lecture 1: Why does FEA build on classical mechanics rather than replace it?

3. Lecture 1: Under what assumptions does a truss member carry only axial force?

4. Lecture 1: Why can a statically determinate truss be solved using equilibrium alone?

5. Lecture 1: What changes mathematically when an extra redundant member is added to a truss?

6. Lecture 1: Why does the force distribution in a statically indeterminate structure depend on relative member stiffness?

7. Lecture 1: How does replacing pin joints with rigid welded joints change the forces and degrees of freedom that must be modelled?

8. Lecture 1: Why can a structure assembled from individually simple members still be difficult to solve by hand?

9. Lecture 1: Describe the main steps for converting a continuous structure into a finite element model.

10. Lecture 1: What information is normally solved at nodes, and how is behaviour between nodes estimated?

11. Lecture 1: What is a shape function, and why is it central to finite element analysis?

12. Lecture 1: How can one-dimensional elements be used to model a two- or three-dimensional structure?

13. Lecture 1: Why might a global line-element model be preferable to modelling an entire building with 3D solid elements?

14. Lecture 1: What is the difference between an axial truss element and a flexural beam element?

15. Lecture 1: Which loads and internal actions can an ideal axial truss element carry?

16. Lecture 1: What additional quantities must be introduced when moving from truss elements to beam elements?

17. Lecture 1: What translations and rotations are restrained by fixed, pinned, and roller supports?

18. Lecture 1: For the lecture’s tip-loaded cantilever, derive:

19. Lecture 1: What are the fixed-end boundary conditions for a cantilever beam?

20. Lecture 1: How are the tip deflection and tip rotation of a tip-loaded cantilever related to \(P\), \(L\), \(E\), and \(I\)?

21. Lecture 1: Why was a standard closed-form buckling equation unsuitable for the damper shaft described in the lecture?

22. Lecture 1: What is the purpose of comparing coarse and fine meshes?

23. Lecture 1: How can shake-table experiments and FEA models complement one another?

24. Lecture 1: Why are connection flexibility, slip, and take-up especially important when the intended damper displacement is small?

25. Lecture 1: How were ultrasound, motion tracking, inertial measurements, and force-plate data combined in the hip-implant research?

26. Lecture 1: Why can similar numerical methods be applied to structural deformation, heat flow, and magnetism?

27. Lecture 1: What Python and linear-algebra skills are expected to support the first finite element laboratories?

28. Lecture 1: Why do the computer laboratories matter even if they have no direct grade?

29. Lecture 1: What minimum final-examination mark was stated as necessary to pass the course?

30. Lecture 1: Which parts of the announced assessment schedule were still provisional at the time of this lecture?

31. Lecture 2: Why is a complicated structure easier to analyse after it has been discretised into finite elements?

32. Lecture 2: What continuous information is lost when a structure is reduced to a finite set of nodal degrees of freedom, and how is that information approximately recovered?

33. Lecture 2: Explain how \(\mathbf{F}=\mathbf{K}\mathbf{D}\) is a matrix generalisation of \(F=kx\).

34. Lecture 2: Derive \(P=(AE/L)\delta\) from the axial-extension equation.

35. Lecture 2: How do \(A\), \(E\), and \(L\) affect the axial stiffness of a bar?

36. Lecture 2: What assumptions define the initial two-node axial bar element?

37. Lecture 2: Why must loads on the initial truss model be applied only at nodal points?

38. Lecture 2: What behaviour would be introduced by placing a transverse load halfway along a bar element?

39. Lecture 2: How do bar, beam, and frame elements differ in the forces and motions they represent?

40. Lecture 2: What are the two degrees of freedom of the local axial bar element?

41. Lecture 2: Why must the two element end-force results be equal in magnitude and opposite in sign under static equilibrium?

42. Lecture 2: What is the difference between a node number and an element number?

43. Lecture 2: How is the positive local \(x_e\)-direction defined?

44. Lecture 2: What must change if local node 1 and local node 2 are exchanged?

45. Lecture 2: How does the right-hand rule determine the local \(y_e\)-axis and positive rotational direction?

46. Lecture 2: Define the element orientation angle \(\alpha\).

47. Lecture 2: Why do \(195^\circ\) and \(-165^\circ\) describe the same orientation, while \(+165^\circ\) does not?

48. Lecture 2: Why are both local and global coordinate systems required?

49. Lecture 2: Distinguish displacement, rotation, and deflection as used in this course.

50. Lecture 2: What endpoint conditions must \(u(x)\) satisfy for a two-node bar?

51. Lecture 2: What is a shape function, and why is it central to the finite element method?

52. Lecture 2: How can strain, stress, and internal axial force be recovered from \(u(x)\)?

53. Lecture 2: Starting from \(N=A\sigma\), \(\sigma=E\varepsilon\), and \(\varepsilon=du/dx\), derive:

54. Lecture 2: What does \(p(x)\) physically represent?

55. Lecture 2: What does setting \(p(x)=0\) imply about the internal axial force?

56. Lecture 2: How does the general dynamic equation reduce to the static stiffness equation?

57. Lecture 2: Why should a linear-system solver generally be used instead of explicitly calculating \(\mathbf{K}^{-1}\)?

58. Lecture 2: List the main stages from element formulation to interpretation of finite element results.

59. Lecture 2: Why can a commercial finite element solution be physically meaningless even if the software successfully converges?

60. Lecture 2: What physical checks could be applied to nodal displacements and element forces before accepting an analysis?

61. Lecture 3: Why are shape functions fundamental to the finite element method?

62. Lecture 3: What are the nodal degrees of freedom of a two-node axial bar element?

63. Lecture 3: Why is the local coordinate convention \(x=0\) at node 1 and \(x=L\) at node 2 important?

64. Lecture 3: Which assumptions justify using a linear displacement field for the axial bar element?

65. Lecture 3: Starting from \(u(x)=a_0+a_1x\), derive \(a_0\) and \(a_1\) using the nodal boundary conditions.

66. Lecture 3: Derive the axial bar shape functions \(\psi_1(x)\) and \(\psi_2(x)\).

67. Lecture 3: What values do the two shape functions take at node 1 and node 2?

68. Lecture 3: Why must \(\psi_1(x)+\psi_2(x)=1\)?

69. Lecture 3: Explain physically why the nodal displacement closer to a point has greater influence on the interpolated displacement there.

70. Lecture 3: If \(d_1=3\ \text{mm}\) and \(d_2=7\ \text{mm}\), express \(u(x)\) in terms of \(x/L\).

71. Lecture 3: For the same element, calculate the interpolated displacement at \(x=0.25L\), \(0.5L\), and \(0.75L\).

72. Lecture 3: Derive the constant strain \(\varepsilon=(d_2-d_1)/L\) from the displacement interpolation.

73. Lecture 3: How are strain, stress, and normal force recovered from the nodal displacements?

74. Lecture 3: Why does a linear displacement field produce constant strain?

75. Lecture 3: What is the physical significance of \(d_2-d_1\)?

76. Lecture 3: What happens to strain, stress, and normal force when \(d_1=d_2\)?

77. Lecture 3: Distinguish rigid-body translation from axial deformation.

78. Lecture 3: Derive the two element end-force equations from the normal-force relationship.

79. Lecture 3: Assemble the end-force equations into the \(2\times2\) element stiffness matrix.

80. Lecture 3: Why are the two equations represented by the free-element stiffness matrix not independent?

81. Lecture 3: Show that the determinant of the unconstrained element stiffness matrix is zero.

82. Lecture 3: Identify the rigid-body mode of the two-node axial bar.

83. Lecture 3: What boundary condition could be applied to eliminate the rigid-body mode?

84. Lecture 3: Why might commercial finite element software report “rigid body modes detected”?

85. Lecture 3: What does it mean if a solver automatically adds weak springs?

86. Lecture 3: Why is a single linear element unsuitable for a strongly tapered bar?

87. Lecture 3: How can many piecewise-prismatic elements approximate a bar with continuously varying cross-section?

88. Lecture 3: Why might beam elements require higher-order shape functions than axial bar elements?

89. Lecture 3: In NumPy, what is the difference between `A @ B` and `A * B`?

90. Lecture 3: Why can `B = A` behave differently from creating an explicit copy of array `A`?

91. Lecture 4: What is the distinction between `A.T`, `np.matmul(A, B)`, `A @ B`, and `A * B` in NumPy?

92. Lecture 4: Why is a horizontal degree of freedom defined at joint \(C\) even though the applied horizontal load is zero?

93. Lecture 4: Why are no allowable global displacement degrees of freedom assigned at the pinned supports in this example?

94. Lecture 4: Using joint equilibrium, explain why member 2 carries \(141.42\ \text{kN}\) in tension and member 1 carries \(100\ \text{kN}\) in compression.

95. Lecture 4: What physical information is provided by \(\delta=FL/(AE)\)?

96. Lecture 4: How can intersecting arcs be used to identify the exact displaced location of a pin-jointed node?

97. Lecture 4: What assumptions allow the arc construction to be replaced by a linearised geometric construction?

98. Lecture 4: What does it mean to say that the initial geometry approximates the final geometry?

99. Lecture 4: Why does the manual geometric compatibility method become difficult for a larger truss?

100. Lecture 4: Under what conditions is \(W=P\delta\) valid?

101. Lecture 4: Why is the external work for a gradually applied linear-elastic load equal to \(\tfrac12P\delta\)?

102. Lecture 4: What assumptions are required to equate external work with internal strain energy?

103. Lecture 4: Derive the total strain energy of a truss as a sum of member strain energies.

104. Lecture 4: Why can the single-load work-energy method determine the vertical displacement in the example but not the horizontal displacement?

105. Lecture 4: Why does one work-energy equation fail when two independent displacement components are unknown?

106. Lecture 4: What is the difference between a real load system and a virtual load system?

107. Lecture 4: Where and in what direction should a virtual load be applied?

108. Lecture 4: Why is a unit virtual load normally chosen?

109. Lecture 4: What do uppercase \(F_i\) and lowercase \(f_i\) represent?

110. Lecture 4: Why must the real and virtual systems be analysed separately before their results are combined?

111. Lecture 4: Write the truss virtual-work equation and identify every term.

112. Lecture 4: Why does member 2 have zero virtual internal force when a horizontal unit virtual load is applied at joint \(C\)?

113. Lecture 4: What does the negative horizontal displacement from the virtual-work calculation mean physically?

114. Lecture 4: When changing from a requested horizontal displacement to a requested vertical displacement, which quantities can be reused and which must be recalculated?

115. Lecture 4: How can virtual internal forces be interpreted as weighting or influence factors?

116. Lecture 4: What does a value \(f_i=0\) imply about member \(i\)’s contribution to the requested displacement?

117. Lecture 4: Why is the demonstrated virtual-work procedure straightforward for a statically determinate truss but harder for a statically indeterminate structure?

118. Lecture 4: How does the principle of virtual work support the later derivation of structural stiffness matrices?

## Practice priorities

1. Tutor strategy for Lecture 1: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

2. Tutor strategy for Lecture 2: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

3. Tutor strategy for Lecture 3: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

4. Tutor strategy for Lecture 4: attempt the associated course-reader examples, check the method against the notes and record your first error. These are study suggestions, not extra assessment requirements.

## Missing or incomplete

No missing source-backed lectures in this window. Equations/diagrams remain subject to the per-lecture caveats. The wrong duplicate transcript(s) have been replaced, not guessed from their titles.

## Source manifest

- Lecture 1 (echo-lecture-1-1): complete; summary `9571f2c0cd7917917eed393739bf65b46c43f5ac7e3ea30195475b96d92f2f8b`; transcript `ec99fc9defb482191133ecf0135f407fb55ee4b2d1ca96f50100859065c34197`; summary path `[local source path redacted]`
- Lecture 2 (echo-lecture-2-2): complete; summary `6c2d654a4ba5b49990a4c28a57876f57edde8ecf57dae071a262155ea8c50cf2`; transcript `5217ec0795bda3c3cccff1ec79a5b5450196ed96b82e1bea1bf1b277ec274ff5`; summary path `[local source path redacted]`
- Lecture 3 (echo-lecture-3-3): complete; summary `b2cf529a2ee003c3fdef687770a09173305c8d9ecbe64db35453876692eff8d6`; transcript `f0f7245ffdffa2b8cdac1cc73a98b4a01078bdf7d1fcd84760fdb0b09e0b4d45`; summary path `[local source path redacted]`
- Lecture 4 (echo-lecture-4-4): complete; summary `2a124226ed35859dcbaf8e8e4515232db14da64eec5330c7db58cc5e9b185570`; transcript `2f760e9fbd881996fae0455608e3b5fbfbdaa88551503d9679e550ceffd75d10`; summary path `[local source path redacted]`
