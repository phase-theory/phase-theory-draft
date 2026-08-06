# Relativity Geometry: Induced Geometry on Admissibility Orbit Spaces

## Abstract

Relativity Geometry is the final geometric derived theory of Relativity Mechanics. It is posed only after orbit ontology, invariant observables, observers, reference transformations, constraints, dynamics, information, quantum theory, and gauge admissibility have been established. Its primitive question is:

\[
\boxed{
\text{What geometry supports the orbit spaces of Relativity Mechanics?}
}
\]

The answer is that geometry is not primitive. Geometry is induced on the physical quotient

\[
Q=\Omega/G
\]

by invariant structures on the description space \(\Omega\). Metrics, affine connections, curvature, topology, fiber bundles, and symplectic structures are not assumed as background absolutes. They descend from admissibility-invariant structures on \(\Omega\), or arise through reduction of the quotient map

\[
I:\Omega\to\Omega/G.
\]

This paper develops Relativity Geometry as the systematic theory of geometric structures on admissibility orbit spaces. We construct quotient metrics from invariant metrics, quotient connections from invariant connections, curvature as obstruction to horizontal transport, symplectic structures by Hamiltonian reduction, topological sectors by characteristic classes, and fiber-bundle structures by principal admissibility bundles. We show that general relativity, gauge theory, quantum projective geometry, moduli spaces, and Frame Theory are all special realizations of this quotient geometry.

The central principle is:

\[
\boxed{
\text{Geometry is the invariant differential structure of orbit spaces.}
}
\]

Frame Theory is therefore not the foundation of Relativity Mechanics. It is one specific geometric realization obtained by choosing the local admissibility group to be \(\mathrm{Spin}(1,3)\).

---

## 1. Introduction

In Relativity Mechanics, the physical world is not described by bare configurations. It is described by equivalence classes of admissible descriptions. Orbit Theory establishes that physical objects are orbits

\[
[\omega]=G\cdot\omega.
\]

Invariant Theory establishes that measurable quantities are functions on the quotient

\[
Q=\Omega/G.
\]

Constraint Mechanics establishes that admissible states form quotient spaces of constraint surfaces. Relativistic Dynamics establishes that physical evolution is flow on those quotients. Relativistic Quantum Theory establishes that quantum states are projective admissibility orbits. Gauge Theory of Admissibility establishes that internal interactions are quotient theories of local internal frames.

Only after all of this do we ask:

\[
\boxed{
\text{What geometry supports these orbit spaces?}
}
\]

Relativity Geometry answers this question.

It studies metrics, connections, curvature, topology, bundles, and symplectic structures on

\[
\Omega/G.
\]

It does not assume geometry as a primitive background. Geometry is induced, descended, reduced, or quotiented from invariant structures on the description space.

Thus Relativity Geometry reverses the traditional order of physics. Instead of placing fields on a pre-given geometry, it derives physical geometry from admissibility structure.

---

## 2. The Geometric Problem of Orbit Spaces

A Relativity Mechanics schema is

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

where

\[
I:\Omega\to Q=\Omega/G
\]

is the invariant projection.

The central geometric problem is:

\[
\boxed{
\text{Construct geometric structures on }Q=\Omega/G.
}
\]

If the action of \(G\) on \(\Omega\) is free and proper, then

\[
\pi:=I:\Omega\to Q
\]

is a principal \(G\)-bundle. In that case, standard differential geometry applies to the quotient.

If the action is not free, the quotient may be singular. Then Relativity Geometry must use:

1. stratified manifolds,
2. orbifolds,
3. differentiable stacks,
4. groupoid geometry,
5. singular reduction.

Thus Relativity Geometry is not restricted to smooth manifolds. It is the geometry of physical equivalence classes, whatever their regularity.

---

## 3. Metrics on Quotient Spaces

Let \(\Omega\) carry a \(G\)-invariant metric tensor \(H\). The metric may be Riemannian, pseudo-Riemannian, or degenerate in constrained directions. For simplicity, assume first that \(H\) is nondegenerate and \(G\) acts by isometries.

The vertical bundle is

\[
V\Omega=\ker I_*.
\]

A horizontal distribution is a complement

\[
T\Omega=V\Omega\oplus H\Omega.
\]

Equivalently, a principal connection one-form

\[
A\in\Omega^1(\Omega,\mathfrak g)
\]

defines

\[
H\Omega=\ker A.
\]

For each vector field \(X\) on \(Q\), let \(X^H\) denote its horizontal lift to \(\Omega\).

The quotient metric is defined by

\[
\boxed{
g_Q(X,Y)(q)
=
H_\omega(X^H_\omega,Y^H_\omega),
\qquad
q=I(\omega).
}
\]

Because \(H\) is \(G\)-invariant and the horizontal distribution is \(G\)-equivariant, this definition is independent of the representative \(\omega\in I^{-1}(q)\).

Thus:

\[
\boxed{
g_Q \text{ is the metric induced on } Q=\Omega/G.
}
\]

In local coordinates, if \(z^A\) are coordinates on \(\Omega\) and \(q^\alpha\) are coordinates on \(Q\), the horizontal lift basis is

\[
E_\alpha^A=\frac{\partial z^A}{\partial q^\alpha}\bigg|_{\rm horizontal}.
\]

Then

\[
\boxed{
g_{\alpha\beta}(q)
=
H_{AB}(\omega)
E_\alpha^A E_\beta^B.
}
\]

This is the general formula for a quotient metric.

---

## 4. Riemannian Submersions and Physical Distance

When \(\pi:\Omega\to Q\) is a Riemannian submersion, the metric \(g_Q\) is characterized by the condition that horizontal lengths are preserved:

\[
g_Q(I_*X^H,I_*Y^H)
=
H(X^H,Y^H).
\]

The physical distance between two orbits \(q_1,q_2\in Q\) is the infimum of lengths of horizontal paths connecting their fibers:

\[
\boxed{
d_Q(q_1,q_2)
=
\inf_{\gamma_H}
\int
\sqrt{
H(\dot\gamma_H,\dot\gamma_H)
}\,dt.
}
\]

Equivalently, one may minimize over all paths in \(\Omega\) modulo gauge:

\[
d_Q([\omega_1],[\omega_2])
=
\inf_{g\in G}
d_\Omega(\omega_1,g\cdot\omega_2),
\]

when the metric and group action permit.

Thus physical distance is distance between orbits, not between representatives.

---

## 5. Affine Connections on Quotient Spaces

A metric is not sufficient for parallel transport. One also needs affine connections.

Let \(\nabla^\Omega\) be a \(G\)-invariant affine connection on \(\Omega\). For \(\nabla^\Omega\) to descend to \(Q\), it must preserve the vertical-horizontal splitting. A sufficient condition is that \(\nabla^\Omega\) is compatible with a principal connection \(A\) and that horizontal lifts of vector fields remain horizontal under covariant differentiation.

Given vector fields \(X,Y\) on \(Q\), define the quotient connection by

\[
\boxed{
\nabla^Q_XY
=
I_*
\left[
\left(
\nabla^\Omega_{X^H}Y^H
\right)^H
\right].
}
\]

Here the superscript \(H\) denotes horizontal projection.

If \(\nabla^\Omega\) is torsion-free and preserves the horizontal distribution, then \(\nabla^Q\) is torsion-free. If \(\nabla^\Omega\) is compatible with \(H\), then \(\nabla^Q\) is compatible with \(g_Q\).

Thus affine geometry also descends from admissibility-invariant structures.

---

## 6. Principal Connections and Gauge Potentials

The most fundamental connection in Relativity Geometry is the principal connection on the admissibility bundle

\[
\pi:\Omega\to Q.
\]

A principal connection is a \(\mathfrak g\)-valued one-form \(A\) satisfying:

\[
A(\xi_\Omega)=\xi,
\]

\[
R_g^*A=\operatorname{Ad}_{g^{-1}}A,
\]

where \(\xi_\Omega\) is the fundamental vector field generated by \(\xi\in\mathfrak g\), and \(R_g\) is the right action of \(g\).

The horizontal subspace is

\[
H_\omega\Omega=\ker A_\omega.
\]

The curvature of \(A\) is

\[
\boxed{
F=dA+\frac12[A,A].
}
\]

It is horizontal and equivariant:

\[
R_g^*F=\operatorname{Ad}_{g^{-1}}F.
\]

The curvature measures the failure of horizontal lifts to close under Lie bracket:

\[
\boxed{
[X^H,Y^H]^V
=
-F(X^H,Y^H)_\Omega.
}
\]

Thus curvature is the obstruction to path-independent horizontal transport across orbit space.

In gauge theory, this curvature is the field strength. In Frame Theory, it becomes spacetime curvature. In quantum geometry, it appears as Berry curvature or Fubini–Study curvature.

---

## 7. Curvature on Quotient Manifolds

Given a quotient metric \(g_Q\) and connection \(\nabla^Q\), the Riemann curvature tensor is

\[
R^Q(X,Y)Z
=
\nabla^Q_X\nabla^Q_YZ
-
\nabla^Q_Y\nabla^Q_XZ
-
\nabla^Q_{[X,Y]}Z.
\]

In components,

\[
R^\alpha{}_{\beta\gamma\delta}
\]

encodes the intrinsic curvature of the physical orbit space.

For a Riemannian submersion, the curvature of \(Q\) is related to the curvature of \(\Omega\) and the curvature of the principal connection. Schematically,

\[
\boxed{
R^Q
=
\pi_*R^\Omega|_{H}
+
\text{gauge-curvature terms}
+
\text{second-fundamental-form terms}.
}
\]

Thus physical curvature receives contributions from:

1. intrinsic curvature of the description space,
2. curvature of the admissibility connection,
3. geometry of the fibers.

This is a central result of Relativity Geometry: physical curvature is not merely background curvature. It is quotient curvature.

---

## 8. Fiber Bundles and Associated Geometry

When the action is free and proper, the quotient map

\[
\pi:\Omega\to Q
\]

is a principal \(G\)-bundle. Associated vector bundles are constructed by representations

\[
\rho:G\to GL(V).
\]

The associated bundle is

\[
E=\Omega\times_G V.
\]

Sections of \(E\) correspond to equivariant functions

\[
\phi:\Omega\to V
\]

satisfying

\[
\phi(g\cdot\omega)=\rho(g^{-1})\phi(\omega).
\]

The principal connection \(A\) induces a covariant derivative on \(E\):

\[
\boxed{
D\phi=d\phi+\rho_*(A)\phi.
}
\]

Its curvature is

\[
\boxed{
D^2\phi=\rho_*(F)\phi.
}
\]

Thus matter fields, spinors, tensors, and frame fields are all sections of bundles associated to the admissibility bundle.

Geometry is therefore organized by the principal admissibility group \(G\).

---

## 9. Topology of Orbit Spaces

Topology in Relativity Geometry is the topology of the quotient \(Q=\Omega/G\).

Even if \(\Omega\) is topologically simple, the quotient may possess nontrivial topology. This topology can encode physical sectors.

### 9.1 Orbit-type stratification

For non-free actions, the quotient decomposes into strata labeled by stabilizer conjugacy classes:

\[
Q
=
\bigsqcup_{(H)}
Q_{(H)}.
\]

Each stratum corresponds to objects with a given residual symmetry type.

### 9.2 Large admissibility transformations

The group \(G\) may have disconnected components. These produce large gauge transformations or large diffeomorphisms. The quotient may therefore have nontrivial fundamental group:

\[
\pi_1(Q).
\]

Such topology can produce theta sectors, anyonic statistics, or mapping-class-group phases.

### 9.3 Characteristic classes

Principal bundles possess topological invariants constructed from curvature. For invariant polynomials \(P(F)\), the Chern–Weil forms

\[
P(F)
\]

are closed, and their cohomology classes are independent of connection.

Examples include Chern classes,

\[
c_k(P)
=
\left[
\left(\frac{i}{2\pi}\right)^k
\operatorname{tr}(F^k)
\right],
\]

Pontryagin classes,

\[
p_k(P)
=
\left[
\operatorname{tr}(F^{2k})
\right],
\]

and Euler classes.

In gauge theory, the instanton number is

\[
\boxed{
k
=
\frac{1}{8\pi^2}
\int_M \operatorname{tr}(F\wedge F).
}
\]

Such topological invariants are physical orbit data.

Thus:

\[
\boxed{
\text{Topology is global orbit structure.}
}
\]

---

## 10. Symplectic Structures on Quotient Spaces

Many physical orbit spaces are not metric but symplectic. Relativity Geometry therefore includes symplectic reduction.

Let \((\Omega,\omega)\) be a symplectic manifold. Let \(G\) act symplectically and Hamiltonianly with moment map

\[
\mu:\Omega\to\mathfrak g^*.
\]

The moment map satisfies

\[
\iota_{\xi_\Omega}\omega=d\mu_\xi.
\]

The reduced phase space is

\[
\boxed{
Q_{\rm red}
=
\mu^{-1}(0)/G.
}
\]

Under appropriate regularity conditions, \(Q_{\rm red}\) carries a unique symplectic form \(\omega_{\rm red}\) such that

\[
\boxed{
i^*\omega=\pi^*\omega_{\rm red},
}
\]

where

\[
i:\mu^{-1}(0)\hookrightarrow\Omega,
\]

\[
\pi:\mu^{-1}(0)\to Q_{\rm red}.
\]

This is the Marsden–Weinstein reduction theorem.

Thus symplectic geometry on physical phase spaces is quotient geometry.

---

## 11. Poisson Reduction

If the quotient is singular, one may use Poisson reduction.

The algebra of physical observables is

\[
C^\infty(Q_{\rm red})
\cong
C^\infty(\Omega)^G
\]

restricted to the constraint surface.

The Poisson bracket descends to the invariant algebra:

\[
\{f,g\}_{\rm red}
=
\{f,g\}\big|_{\mu^{-1}(0)}.
\]

For second-class constraints, one uses the Dirac bracket:

\[
\boxed{
\{f,g\}_D
=
\{f,g\}
-
\{f,\chi_\alpha\}
\Delta^{\alpha\beta}
\{\chi_\beta,g\}.
}
\]

Thus constrained Hamiltonian mechanics is a special case of Relativity Geometry.

---

## 12. Kähler and Quantum Geometry

Quantum state spaces often carry Kähler geometry.

Let \(\mathcal H\) be a Hilbert space. The projective Hilbert space

\[
\mathbb P(\mathcal H)
\]

is obtained by quotienting by phase:

\[
\mathbb P(\mathcal H)
=
(\mathcal H\setminus\{0\})/\mathbb C^*.
\]

It carries the Fubini–Study metric:

\[
\boxed{
ds^2_{\rm FS}
=
\frac{
\langle d\psi|d\psi\rangle\langle\psi|\psi\rangle
-
|\langle\psi|d\psi\rangle|^2
}{
\langle\psi|\psi\rangle^2
}.
}
\]

It also carries the Fubini–Study symplectic form:

\[
\omega_{\rm FS}
=
\frac{i\hbar}{2}
\frac{
\langle d\psi|d\psi\rangle\langle\psi|\psi\rangle
-
\langle\psi|d\psi\rangle\langle d\psi|\psi\rangle
}{
\langle\psi|\psi\rangle^2
}.
\]

If an admissibility group \(G\) acts on \(\mathcal H\), the physical quantum state space is

\[
\mathbb P(\mathcal H)/G.
\]

The quotient inherits metric, symplectic, and complex structures when the action is compatible.

Thus quantum geometry is also quotient geometry.

---

## 13. Geometry of Gauge Orbit Spaces

In gauge theory, the description space is the affine space of connections

\[
\mathcal A.
\]

The admissibility group is the gauge group

\[
\mathcal G.
\]

The physical configuration space is

\[
\boxed{
\mathcal A/\mathcal G.
}
\]

A natural formal metric on \(\mathcal A\) is the \(L^2\) metric:

\[
\|\delta A\|^2
=
\int_M \operatorname{tr}(\delta A\wedge *\delta A).
\]

The quotient metric is defined on directions transverse to gauge orbits. A tangent vector \(\delta A\) is transverse if

\[
D_A^*\delta A=0.
\]

The curvature of the gauge connection is

\[
F=dA+A\wedge A.
\]

The gauge orbit space has rich topology, including instanton sectors labeled by

\[
k=\frac{1}{8\pi^2}\int_M\operatorname{tr}(F\wedge F).
\]

Thus Yang–Mills geometry is Relativity Geometry for internal admissibility groups.

---

## 14. Geometry of General Relativity Superspace

In general relativity, the configuration space is the space of Riemannian or Lorentzian metrics:

\[
\operatorname{Met}(M).
\]

The admissibility group is

\[
\operatorname{Diff}(M).
\]

The physical configuration space is superspace:

\[
\boxed{
\mathcal S
=
\operatorname{Met}(M)/\operatorname{Diff}(M).
}
\]

Superspace carries the DeWitt supermetric:

\[
\boxed{
G^{ijkl}
=
\frac{1}{2\sqrt{h}}
\left(
h^{ik}h^{jl}
+
h^{il}h^{jk}
-
h^{ij}h^{kl}
\right).
}
\]

For variations \(\delta h_{ij}\), the formal line element is

\[
ds^2
=
\int_\Sigma d^3x\,
G^{ijkl}
\delta h_{ij}\delta h_{kl}.
\]

This metric is indefinite. Its quotient geometry encodes canonical gravitational dynamics.

The strata of superspace correspond to metrics with different isometry groups. Highly symmetric geometries lie on singular strata.

Thus general relativity is a quotient geometry of metrics modulo diffeomorphisms.

---

## 15. Geometry of String Moduli Spaces

In string theory, the worldsheet description space includes metrics \(h_{ab}\) on a genus-\(g\) surface \(\Sigma_g\). The admissibility group is

\[
\operatorname{Diff}(\Sigma_g)\ltimes\operatorname{Weyl}(\Sigma_g).
\]

The quotient

\[
\mathcal M_g
=
\operatorname{Met}(\Sigma_g)/
\bigl(
\operatorname{Diff}(\Sigma_g)\ltimes\operatorname{Weyl}(\Sigma_g)
\bigr)
\]

is the moduli space of Riemann surfaces.

It carries natural geometric structures, including the Weil–Petersson metric. String amplitudes integrate over this quotient space.

Thus string geometry is also Relativity Geometry.

---

## 16. Stacky Geometry and Singular Quotients

When the admissibility action has stabilizers, the naive quotient loses automorphism data. Relativity Geometry then uses the quotient stack

\[
\boxed{
[\Omega/G].
}
\]

The stack remembers:

1. orbits,
2. stabilizers,
3. orbifold singularities,
4. residual gauge automorphisms.

In stacky language, geometry is not merely the space \(Q=\Omega/G\), but the groupoid

\[
\Omega//G.
\]

This is especially important in:

1. gauge theory with reducible connections,
2. general relativity with symmetric metrics,
3. orbifold string backgrounds,
4. moduli spaces with automorphisms.

Thus Relativity Geometry includes ordinary quotient geometry as a special case.

---

## 17. Frame Theory as a Specific Realization

Frame Theory is obtained by choosing:

\[
\Omega_{\rm FT}
=
\{e^I_\mu\},
\]

\[
G_{\rm FT}
=
C^\infty(M,\mathrm{Spin}(1,3)).
\]

The invariant projection gives the metric:

\[
\boxed{
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
}
\]

Thus the quotient by local spin transformations gives Lorentzian metric geometry:

\[
\Omega_{\rm FT}/G_{\rm FT}
\cong
\operatorname{Met}_{1,3}(M).
\]

Including diffeomorphisms gives the full gravitational quotient:

\[
\operatorname{Met}_{1,3}(M)/\operatorname{Diff}(M).
\]

The spin connection

\[
\omega^{IJ}
\]

is the principal connection of the local spin admissibility bundle. Its curvature is

\[
R^{IJ}
=
d\omega^{IJ}
+
\omega^I{}_K\wedge\omega^{KJ}.
\]

The torsion is

\[
T^I
=
de^I+\omega^I{}_J\wedge e^J.
\]

The Palatini action,

\[
S[e,\omega]
=
\frac{1}{2\kappa}
\int
\epsilon_{IJKL}
e^I\wedge e^J\wedge R^{KL},
\]

is an invariant functional on the frame quotient geometry.

Thus Frame Theory is not the foundation of Relativity Mechanics. It is a specific realization of Relativity Geometry obtained by choosing the local admissibility group to be \(\mathrm{Spin}(1,3)\).

\[
\boxed{
\text{Frame Theory is Relativity Geometry with spin-frame admissibility.}
}
\]

---

## 18. Gauge Theory as Another Specific Realization

Gauge Theory of Admissibility is obtained by choosing an arbitrary internal group \(G\) and taking the description space to be connections:

\[
\Omega=\mathcal A.
\]

The quotient is

\[
\mathcal A/\mathcal G.
\]

The principal connection is the gauge potential \(A\). Its curvature is the field strength \(F\). The quotient geometry carries Yang–Mills metric structures, symplectic phase spaces, characteristic classes, and moduli spaces.

Thus gauge theory and Frame Theory are parallel realizations of Relativity Geometry, differing only in the choice of admissibility group and representation content.

---

## 19. Information Geometry as Quotient Geometry

Relativistic Information Theory also induces geometry.

Given a family of probability measures \(p(q|\theta)\) on an orbit space \(Q\), the Fisher information metric is

\[
\boxed{
F_{ab}
=
\int_Q
p(q|\theta)
\partial_a\log p(q|\theta)
\partial_b\log p(q|\theta)
\,dq.
}
\]

This is a Riemannian metric on the physical parameter space. It measures infinitesimal distinguishability of physical information states.

Thus statistical geometry is another quotient geometry within Relativity Mechanics.

---

## 20. Axioms of Relativity Geometry

Relativity Geometry is governed by the following axioms.

### Axiom I: Geometry is induced on orbit spaces

Physical geometry is geometry on

\[
Q=\Omega/G.
\]

It is not imposed prior to admissibility.

### Axiom II: Geometric structures descend from invariant structures

Metrics, connections, symplectic forms, and topological classes must be \(G\)-invariant or arise through reduction.

### Axiom III: Singular quotients are geometric

Stratification, orbifold points, and stacky stabilizers are not defects. They are part of physical geometry.

### Axiom IV: Curvature is quotient obstruction

Curvature measures failure of horizontal transport, gauge trivialization, or relational parallelism on orbit space.

### Axiom V: Topology is global orbit structure

Topological sectors are global features of admissibility quotients.

### Axiom VI: Frame geometry is a special case

Spacetime frame geometry is one realization of quotient geometry, not the general foundation.

---

## 21. The Complete Geometric Hierarchy

The geometric hierarchy of Relativity Mechanics is:

\[
\boxed{
\Omega
}
\]

\[
\downarrow
\]

\[
\boxed{
G\text{-invariant structures on }\Omega
}
\]

\[
\downarrow
\]

\[
\boxed{
I:\Omega\to Q=\Omega/G
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Induced geometry on }Q
}
\]

\[
\downarrow
\]

\[
\boxed{
\text{Physical geometry}
}
\]

The induced geometry may include:

\[
\begin{aligned}
&\text{metrics }g_Q,\\
&\text{connections }\nabla^Q,\\
&\text{curvature }R^Q,\\
&\text{symplectic forms }\omega_{\rm red},\\
&\text{Poisson brackets }\{\cdot,\cdot\}_{\rm red},\\
&\text{topological sectors},\\
&\text{characteristic classes},\\
&\text{moduli spaces},\\
&\text{stacky automorphism data}.
\end{aligned}
\]

Thus geometry is the final differential expression of admissibility.

---

## 22. Conclusion

Relativity Geometry answers the final geometric question of Relativity Mechanics:

\[
\boxed{
\text{What geometry supports the orbit spaces?}
}
\]

The answer is:

\[
\boxed{
\text{Geometry is induced on } \Omega/G.
}
\]

Metrics arise from invariant metrics and Riemannian submersions. Connections arise from principal admissibility bundles. Curvature measures obstruction to horizontal transport. Symplectic structures arise by Hamiltonian reduction. Topology arises from global orbit structure. Fiber bundles arise from the principal admissibility action.

General relativity, gauge theory, quantum projective geometry, string moduli spaces, and Frame Theory are all special cases of this principle.

Frame Theory, in particular, is not foundational. It is the specific realization obtained by choosing the local admissibility group to be

\[
\mathrm{Spin}(1,3).
\]

Thus Relativity Geometry completes the geometric layer of Relativity Mechanics:

\[
\boxed{
\text{Geometry is not the stage on which admissibility acts. Geometry is the invariant structure left when admissibility has acted.}
}
\]
