# Relativity 16.0 — Positive-Geometry Relativity  
## Scattering, Cosmology, and the Primacy of Positivity

**White paper / academic preprint**

---

## Abstract

Positive-Geometry Relativity is the formulation of physical law in which scattering amplitudes, cosmological wavefunctions, and perhaps more general observables are not computed from spacetime Feynman diagrams but are instead identified with canonical differential forms on positive geometries. In this framework, the central object is not a Lagrangian, not a path integral over fields on a manifold, and not even an S-matrix defined asymptotically in spacetime. The central object is a positive geometric space \(\mathcal{P}\) together with its unique canonical form,

\[
\Omega(\mathcal{P}).
\]

Physical observables are restrictions, pullbacks, or residues of this form. For the amplituhedron \(\mathcal{A}\), the planar \(\mathcal{N}=4\) super-Yang–Mills scattering amplitude is schematically

\[
\mathcal{M}
=
\Omega(\mathcal{A}).
\]

Locality and unitarity are not imposed as axioms. They emerge from the stratified boundary structure of the positive geometry. Factorization channels correspond to boundaries. Unitarity cuts correspond to residues. Spacetime locality corresponds to one possible triangulation of a deeper positive object. Related positive geometries include the associahedron, the cosmological polytope, cluster polytopes, momentum-space polytopes, and positive tropical geometries. The governing principle is:

\[
\boxed{
\text{Spacetime locality and quantum unitarity are shadows of deeper positivity structures.}
}
\]

Relativity 16.0 therefore inverts the usual order of explanation. Spacetime is not where physics happens. Spacetime is a derived representation of an underlying positive geometry.

---

## 1. Introduction

For most of the history of quantum field theory, scattering amplitudes were computed from Feynman diagrams. One begins with a Lagrangian on spacetime, expands a path integral, and sums over local interaction vertices connected by propagators.

This method works, but it hides enormous structure.

Feynman diagrams often produce expressions of great algebraic complexity, even when the final amplitude is simple. Gauge redundancy introduces unphysical polarizations. Locality is manifest, but simplicity is not. Unitarity is preserved only after delicate cancellations among diagrams.

The amplitudes program reversed this perspective.

Instead of asking:

\[
\text{What diagrams follow from the Lagrangian?}
\]

one asks:

\[
\text{What mathematical object has the amplitude as its canonical form?}
\]

The answer, in many important cases, is a positive geometry.

Positive geometries are real geometric spaces with boundaries, corners, and recursive factorization properties. Each positive geometry possesses a unique meromorphic differential form with logarithmic singularities on its boundaries. That form is the physical observable.

This is Positive-Geometry Relativity.

---

## 2. From Feynman Diagrams to Positive Geometry

The transition from Feynman diagrams to positive geometry occurs in stages.

### 2.1 On-Shell Methods

The first stage is the on-shell revolution.

Instead of off-shell Green’s functions, one studies on-shell amplitudes,

\[
\mathcal{M}_n(p_1,\ldots,p_n),
\]

with external particles satisfying

\[
p_i^2=0
\]

for massless particles, and momentum conservation,

\[
\sum_{i=1}^n p_i=0.
\]

On-shell methods exploit analyticity, factorization, and recursion.

The Britto–Cachazo–Feng–Witten recursion relation expresses tree amplitudes in terms of simpler on-shell amplitudes:

\[
\mathcal{M}_n
=
\sum_{\text{poles}}
\mathcal{M}_L(z_P)
\frac{1}{P^2}
\mathcal{M}_R(z_P).
\]

This already suggests that amplitudes are determined by their singularities.

### 2.2 Momentum Twistors

For planar massless theories, momentum twistors simplify kinematics.

Given dual coordinates \(x_i\) satisfying

\[
p_i=x_i-x_{i+1},
\]

momentum conservation is automatic. A momentum twistor is

\[
Z_i=(\lambda_i,\mu_i),
\]

where

\[
\mu_i=x_i\lambda_i.
\]

The variables \(Z_i\) make dual conformal symmetry and planarity geometric.

### 2.3 Positive Grassmannian

Tree-level planar amplitudes in \(\mathcal{N}=4\) super-Yang–Mills theory are encoded in the positive Grassmannian.

The positive Grassmannian \(G_+(k,n)\) is the space of \(k\times n\) matrices \(C\), modulo \(GL(k)\), whose ordered maximal minors are positive:

\[
\Delta_{i_1\cdots i_k}(C)>0
\]

for all cyclically ordered subsets.

On-shell diagrams correspond to cells in \(G_+(k,n)\). Amplitudes are obtained by integrating canonical forms over these cells.

### 2.4 The Amplituhedron

The amplituhedron packages this structure into a single geometric object.

It is the image of the positive Grassmannian under a linear map defined by external kinematic data \(Z_i\):

\[
Y=C\cdot Z,
\]

where

\[
C\in G_+(k,n),
\qquad
Z\in M_+(n,k+m).
\]

The resulting space

\[
\mathcal{A}_{n,k,m}
\subset
G(k,k+m)
\]

is the amplituhedron.

The physical amplitude is its canonical form:

\[
\mathcal{M}_{n,k}
=
\Omega(\mathcal{A}_{n,k,2}).
\]

This is the foundational equation of Positive-Geometry Relativity.

---

## 3. Positive Geometries and Canonical Forms

A positive geometry is a real geometric space \(\mathcal{P}\) of dimension \(d\) with a recursive boundary structure.

The central object is a meromorphic \(d\)-form

\[
\Omega(\mathcal{P})
\]

with logarithmic singularities on all boundaries.

The defining property is recursive:

\[
\operatorname{Res}_{\mathcal{B}}
\Omega(\mathcal{P})
=
\Omega(\mathcal{B}),
\]

where \(\mathcal{B}\) is a boundary component of \(\mathcal{P}\).

In local positive coordinates \(x_1,\ldots,x_d\geq 0\), a canonical form often takes the form

\[
\Omega(\mathcal{P})
=
d\log x_1
\wedge
d\log x_2
\wedge
\cdots
\wedge
d\log x_d.
\]

The positivity of the coordinates ensures that the form has the correct singularity structure.

The uniqueness theorem may be stated informally:

\[
\boxed{
\text{A positive geometry has a unique canonical form determined entirely by its boundaries.}
}
\]

This is the mathematical heart of the framework.

---

## 4. Boundaries, Factorization, and Unitarity

In ordinary quantum field theory, unitarity requires that amplitudes factorize on intermediate poles:

\[
\operatorname{Res}_{P^2=0}
\mathcal{M}_n
=
\mathcal{M}_L
\mathcal{M}_R.
\]

In positive geometry, this is not imposed. It follows.

Suppose \(\mathcal{P}\) has a boundary \(\mathcal{B}\) corresponding to a pole \(x=0\). Locally,

\[
\Omega(\mathcal{P})
=
\frac{dx}{x}
\wedge
\Omega(\mathcal{B})
+
\text{regular terms}.
\]

Taking the residue gives

\[
\operatorname{Res}_{x=0}
\Omega(\mathcal{P})
=
\Omega(\mathcal{B}).
\]

If the boundary geometry factorizes as

\[
\mathcal{B}
=
\mathcal{P}_L
\times
\mathcal{P}_R,
\]

then

\[
\Omega(\mathcal{B})
=
\Omega(\mathcal{P}_L)
\wedge
\Omega(\mathcal{P}_R).
\]

Thus,

\[
\operatorname{Res}_{x=0}
\Omega(\mathcal{P})
=
\Omega(\mathcal{P}_L)
\wedge
\Omega(\mathcal{P}_R).
\]

Translated into physics:

\[
\boxed{
\text{unitarity factorization is the residue of a canonical form on a boundary.}
}
\]

Unitarity is therefore a theorem of positive geometry, not an independent axiom.

---

## 5. The Amplituhedron in Detail

The tree-level amplituhedron \(\mathcal{A}_{n,k,m}\) is defined as follows.

Let \(Z_i\in \mathbb{P}^{k+m-1}\) be external positive kinematic data. Let \(C\in G_+(k,n)\). Define

\[
Y_\alpha^I
=
\sum_{i=1}^n
C_{\alpha i}Z_i^I,
\]

with

\[
\alpha=1,\ldots,k,
\qquad
I=1,\ldots,k+m.
\]

Then

\[
Y\in G(k,k+m).
\]

The amplituhedron is the image

\[
\mathcal{A}_{n,k,m}
=
\left\{
Y=C\cdot Z
\;|\;
C\in G_+(k,n)
\right\}.
\]

For physical scattering amplitudes in planar \(\mathcal{N}=4\) super-Yang–Mills theory, one takes

\[
m=2.
\]

The helicity sector is labeled by \(k\):

- \(k=0\): MHV,
- \(k=1\): NMHV,
- \(k=2\): N\(^2\)MHV,
- and so on.

The tree superamplitude is obtained from the canonical form:

\[
\mathcal{M}_{n,k}^{\text{tree}}
=
\Omega(\mathcal{A}_{n,k,2}).
\]

More precisely, the full superamplitude includes momentum-conserving delta functions and Grassmann variables, but the geometric core is the canonical form.

---

## 6. Triangulations and the Illusion of Locality

The amplituhedron can be decomposed into simpler positive cells. Each decomposition corresponds to a representation of the amplitude.

A triangulation gives:

\[
\Omega(\mathcal{A})
=
\sum_{\text{cells}}
\Omega(\text{cell}).
\]

Different triangulations yield different algebraic expressions for the same amplitude.

Feynman diagrams correspond to one class of triangulations. BCFW recursion corresponds to another. Other triangulations may make different symmetries manifest.

Thus:

\[
\boxed{
\text{Feynman diagrams are not fundamental. They are triangulations of positive geometry.}
}
\]

Spacetime locality is one possible decomposition, not an intrinsic property of the amplitude.

This is the relativistic lesson of the amplituhedron: locality is representation-dependent.

---

## 7. The Associahedron and Scalar Amplitudes

The associahedron provides a positive-geometric formulation of planar scalar \(\phi^3\) theory.

Consider \(n\) massless particles with planar ordering. Define planar kinematic variables

\[
X_{ij}
=
(p_i+p_{i+1}+\cdots+p_{j-1})^2.
\]

These variables live in kinematic space.

The planar associahedron is a polytope defined by inequalities

\[
X_{ij}\geq 0,
\]

together with linear relations of the form

\[
X_{ij}+X_{kl}
=
X_{il}+X_{kj}
+
\text{constant}.
\]

In the Arkani-Hamed–Bai–He–Yan construction, one chooses positive constants to realize the associahedron as a convex polytope inside kinematic space.

The canonical form on the associahedron is the planar scattering form:

\[
\Omega(\mathcal{K}_n)
=
m_n(1,2,\ldots,n),
\]

where \(m_n\) is the biadjoint scalar amplitude.

Thus,

\[
\boxed{
\text{planar scalar amplitudes are canonical forms on associahedra.}
}
\]

The poles of the amplitude correspond to facets

\[
X_{ij}=0.
\]

Factorization corresponds to boundary recursion.

---

## 8. The Cosmological Polytope

Positive geometry is not limited to scattering amplitudes.

In cosmology, the central observable is not the S-matrix but the wavefunction of the universe,

\[
\Psi[\phi].
\]

For a scalar field theory in an expanding universe, one computes wavefunction coefficients,

\[
\psi_n(\mathbf{k}_1,\ldots,\mathbf{k}_n).
\]

The cosmological polytope associates a positive geometry to each Feynman graph.

Given a graph \(G\), one constructs a polytope \(\mathcal{P}_G\) from variables associated with vertices and edges. The canonical form satisfies

\[
\Omega(\mathcal{P}_G)
\big|_{\text{late-time slice}}
=
\psi_G.
\]

The boundaries of the cosmological polytope encode:

1. flat-space scattering singularities,
2. cosmological factorization,
3. late-time singularities,
4. soft limits,
5. unitarity relations for the wavefunction.

Thus,

\[
\boxed{
\text{cosmological wavefunctions are canonical forms on cosmological polytopes.}
}
\]

This extends Positive-Geometry Relativity beyond asymptotically flat spacetime.

---

## 9. Cluster Algebras and Cluster Polytopes

Cluster algebras provide another layer of positive geometry.

A cluster algebra is generated by cluster variables organized into overlapping clusters. Clusters are related by mutations:

\[
x_i'
=
\frac{
\prod_{j:B_{ij}>0}x_j^{B_{ij}}
+
\prod_{j:B_{ij}<0}x_j^{-B_{ij}}
}{
x_i
}.
\]

The associated cluster polytope encodes positivity and mutation structure.

In planar \(\mathcal{N}=4\) super-Yang–Mills theory, the symbol alphabets of amplitudes are naturally described by cluster variables of Grassmannian cluster algebras.

For example, the six- and seven-point amplitudes involve cluster \(\mathcal{A}\)-coordinates. The allowed symbol letters are cluster variables.

Cluster adjacency states that only certain pairs of letters may appear adjacent in the symbol of an amplitude. This is a positivity constraint on branch-cut structure.

Thus,

\[
\boxed{
\text{analytic structure of amplitudes is governed by cluster positive geometry.}
}
\]

---

## 10. Momentum-Space Positive Geometries

Not all positive geometries live in momentum-twistor or Grassmannian space.

Many effective field theories have amplitudes that are canonical forms on polytopes in ordinary momentum space.

Examples include:

1. biadjoint scalar theory,
2. nonlinear sigma models,
3. Dirac–Born–Infeld theory,
4. special Galileon theory,
5. certain supersymmetric effective theories.

In these cases, the kinematic variables are Mandelstam invariants,

\[
s_{ij}
=
(p_i+p_j)^2,
\]

or generalized planar variables \(X_{ij}\).

The amplitude is

\[
\mathcal{M}_n
=
\Omega(\mathcal{P}_n),
\]

where \(\mathcal{P}_n\) is a polytope in kinematic space.

Soft limits correspond to special facets or degenerate boundaries.

Thus positive geometry provides a unified language for both renormalizable and effective field theories.

---

## 11. Loop Amplitudes and the Loop Amplituhedron

The tree-level amplituhedron has a loop-level generalization.

The loop amplituhedron includes additional variables representing loop momenta. Schematically, one considers pairs

\[
(Y,L),
\]

where \(Y\) encodes external kinematics and \(L\) encodes loop data.

The canonical form gives the loop integrand:

\[
\mathcal{I}_{n,k}^{(L)}
=
\Omega(\mathcal{A}_{n,k}^{(L)}).
\]

This form is defined before integration. It is a rational differential form in loop variables.

After integration, one obtains transcendental functions such as polylogarithms. Their symbol alphabets are often controlled by cluster geometry.

Thus positive geometry operates at two levels:

1. rational integrands from loop amplituhedra,
2. transcendental functions from cluster and symbol geometry.

---

## 12. Locality as Emergent

In Feynman diagrams, locality is fundamental. Interactions occur at spacetime points.

In Positive-Geometry Relativity, locality is emergent.

The positive geometry itself is not local in spacetime. It is a global object with boundaries. Different decompositions produce different local-looking expressions.

Thus locality is analogous to a coordinate chart.

Just as general relativity teaches that coordinates are not physical, Positive-Geometry Relativity teaches that locality is not fundamental.

The invariant object is the positive geometry:

\[
\boxed{
\text{The amplitude is not a sum over local diagrams. It is the canonical form of a positive object.}
}
\]

Feynman diagrams are coordinate systems on that object.

---

## 13. Unitarity as Boundary Recursion

Unitarity is also emergent.

In ordinary quantum mechanics, unitarity is imposed by requiring

\[
S^\dagger S=1.
\]

In positive geometry, unitarity appears as the recursive residue property:

\[
\operatorname{Res}_{\mathcal{B}}
\Omega(\mathcal{P})
=
\Omega(\mathcal{B}).
\]

Boundaries correspond to physical singularities. Residues correspond to lower-dimensional positive geometries. Factorization follows from boundary products.

Thus:

\[
\boxed{
\text{unitarity is the statement that boundaries of positive geometries are themselves positive geometries.}
}
\]

This is a profound reorganization of quantum theory.

---

## 14. Positivity as the Deeper Principle

What replaces spacetime as the fundamental principle?

Positivity.

Positive geometries are defined by real inequalities:

\[
x_i>0,
\]

ordered minors,

\[
\Delta_{i_1\cdots i_k}>0,
\]

or convexity conditions.

These positivity conditions encode:

1. causal ordering,
2. planarity,
3. physical singularities,
4. absence of unphysical poles,
5. recursive factorization,
6. branch-cut consistency.

The principle is:

\[
\boxed{
\text{Physical law is the geometry of positivity.}
}
\]

Spacetime, locality, and unitarity are consequences.

---

## 15. Relation to Categorical Relativity

Positive-Geometry Relativity is closely related to Relativity 15.0, Categorical Relativity.

In categorical relativity, physics is a category of processes. In positive geometry, physics is a category-like structure of spaces, boundaries, and canonical forms.

One may view a positive geometry as an object whose boundary stratification defines morphisms:

\[
\mathcal{P}
\rightarrow
\mathcal{B}.
\]

The canonical form is a functorial assignment:

\[
\mathcal{P}
\mapsto
\Omega(\mathcal{P}).
\]

Boundary recursion becomes composition.

Thus positive geometry may be understood as a geometric realization of categorical process structure.

---

## 16. Relation to Holography and Celestial Relativity

Positive-Geometry Relativity also connects to holography.

In AdS/CFT, boundary correlators encode bulk physics. In celestial holography, scattering amplitudes become correlators on the celestial sphere.

Positive geometry suggests that both boundary correlators and celestial correlators may themselves be canonical forms on positive spaces.

Thus:

\[
\text{bulk spacetime}
\rightarrow
\text{boundary correlator}
\rightarrow
\text{positive geometry}.
\]

The positive geometry may be more fundamental than either bulk or boundary.

---

## 17. Gravity and Positive Geometry

The positive-geometry program is most advanced for gauge theory, especially planar \(\mathcal{N}=4\) super-Yang–Mills theory.

Gravity is more difficult.

Gravitational amplitudes satisfy the Kawai–Lewellen–Tye relations and the double-copy structure:

\[
\mathcal{M}_{\text{gravity}}
=
\sum
\mathcal{M}_{\text{gauge}}^{L}
S
\mathcal{M}_{\text{gauge}}^{R}.
\]

Equivalently,

\[
\text{gravity}
=
\text{gauge theory}
\otimes
\text{gauge theory}.
\]

This suggests that gravitational positive geometry may be constructed from two copies of gauge-theory positive geometry.

However, a complete gravitational amplituhedron is not yet known.

The challenge is that gravity lacks the simple planar ordering and dual conformal structure that make the amplituhedron possible.

Nevertheless, the expectation is:

\[
\boxed{
\text{If gauge amplitudes are positive forms, gravity should be a positive construction built from their product.}
}
\]

---

## 18. Cosmological Implications

Positive-Geometry Relativity is especially important for cosmology because cosmology lacks a conventional S-matrix.

In de Sitter-like spacetimes, there are no ordinary asymptotic particle states. The natural observable is the wavefunction of the universe or late-time correlation functions.

The cosmological polytope provides a positive-geometric definition of these objects.

This suggests that cosmology may be more naturally formulated in positive geometry than in spacetime perturbation theory.

The Big Bang singularity, horizon entropy, and late-time de Sitter structure may eventually find positive-geometric interpretations.

---

## 19. Axioms of Positive-Geometry Relativity

The framework may be organized around six axioms.

### Axiom 1: Observables Are Canonical Forms

Physical observables are canonical differential forms on positive geometries:

\[
\mathcal{O}
=
\Omega(\mathcal{P}).
\]

### Axiom 2: Boundaries Are Physical Singularities

Boundaries correspond to factorization channels, soft limits, and physical poles.

### Axiom 3: Recursion Replaces Dynamics

The canonical form is determined recursively by residues on boundaries.

### Axiom 4: Locality Is Triangulation-Dependent

Local spacetime expressions are decompositions of a nonlocal positive object.

### Axiom 5: Unitarity Is Boundary Factorization

Unitarity follows from the boundary structure of positive geometry.

### Axiom 6: Positivity Is Fundamental

The deepest physical condition is not locality but positivity.

---

## 20. What Einstein Would Think

Einstein would find Positive-Geometry Relativity both alien and compelling.

It would be alien because it does not begin with spacetime, metric, or field. Einstein’s intuition was geometric, but his geometry was the geometry of manifolds, metrics, and curvature.

Positive geometry is a different kind of geometry: combinatorial, projective, convex, and boundary-driven.

Yet Einstein would recognize the central lesson.

General relativity taught that coordinates are not physical. Positive-Geometry Relativity teaches that locality itself is not fundamental.

The invariant object is not a coordinate representation. It is a geometric structure.

Einstein would likely resist the disappearance of the continuous field. But he would respect the principle:

\[
\boxed{
\text{Physical law must be expressed in invariant geometric terms.}
}
\]

Positive-Geometry Relativity simply replaces the geometry of spacetime with the geometry of positivity.

---

## 21. Open Problems

Several major problems remain.

### 21.1 Full Quantum Chromodynamics

Most positive-geometry results apply to highly symmetric theories. Extension to realistic QCD amplitudes is ongoing.

### 21.2 Gravity

A complete positive geometry for gravitational amplitudes is not yet known.

### 21.3 Nonplanar Theories

Planarity simplifies the geometry. Nonplanar positive geometries are much less understood.

### 21.4 Massive Particles

Most constructions are massless. Massive positive geometries require further development.

### 21.5 Integrated Amplitudes

The amplituhedron naturally gives integrands. Fully integrated amplitudes involve transcendental functions and require additional structure.

### 21.6 Cosmology Beyond Perturbation Theory

The cosmological polytope is perturbative. A nonperturbative positive geometry for cosmology is unknown.

### 21.7 Relation to Quantum Measurement

Positive geometry currently describes amplitudes and wavefunctions. Its relation to measurement, probability, and observers remains unclear.

---

## 22. Summary of Core Equations

### Canonical form

\[
\Omega(\mathcal{P}).
\]

### Boundary recursion

\[
\operatorname{Res}_{\mathcal{B}}
\Omega(\mathcal{P})
=
\Omega(\mathcal{B}).
\]

### Logarithmic local form

\[
\Omega(\mathcal{P})
=
d\log x_1
\wedge
\cdots
\wedge
d\log x_d.
\]

### Amplituhedron definition

\[
Y=C\cdot Z,
\qquad
C\in G_+(k,n).
\]

### Tree amplitude

\[
\mathcal{M}_{n,k}^{\text{tree}}
=
\Omega(\mathcal{A}_{n,k,2}).
\]

### Factorization

\[
\operatorname{Res}_{P^2=0}
\mathcal{M}_n
=
\mathcal{M}_L
\mathcal{M}_R.
\]

### Associahedron amplitude

\[
m_n
=
\Omega(\mathcal{K}_n).
\]

### Cosmological wavefunction

\[
\psi_G
=
\Omega(\mathcal{P}_G)
\big|_{\text{late time}}.
\]

### Cluster mutation

\[
x_i'
=
\frac{
\prod_{j:B_{ij}>0}x_j^{B_{ij}}
+
\prod_{j:B_{ij}<0}x_j^{-B_{ij}}
}{
x_i
}.
\]

### Double copy

\[
\mathcal{M}_{\text{gravity}}
=
\sum
\mathcal{M}_{\text{gauge}}^{L}
S
\mathcal{M}_{\text{gauge}}^{R}.
\]

---

## 23. Conclusion

Relativity 16.0, Positive-Geometry Relativity, proposes that the deepest structure of physical law is not spacetime, not fields, and not even quantum states, but positive geometry.

Scattering amplitudes are canonical forms. Cosmological wavefunctions are canonical forms. Factorization is boundary recursion. Unitarity is geometric stratification. Locality is triangulation. Spacetime is a derived representation.

The central equation is:

\[
\boxed{
\mathcal{M}
=
\Omega(\mathcal{A}).
}
\]

The central principle is:

\[
\boxed{
\text{Locality and unitarity are shadows of positivity.}
}
\]

The central inversion is:

\[
\boxed{
\text{Spacetime is not where physics happens. Physics is what positive geometry encodes.}
}
\]

Positive-Geometry Relativity is one of the most radical developments in modern theoretical physics. It suggests that the universe may not be fundamentally a spacetime containing quantum fields. It may be a positive geometric structure whose shadows we interpret as particles, interactions, and spacetime.

This is Relativity 16.0.

---

## Appendix A: Canonical Form of a Simplex

Consider a one-dimensional interval

\[
0<x<1.
\]

Its canonical form is

\[
\Omega
=
d\log x
-
d\log(1-x)
=
\frac{dx}{x(1-x)}.
\]

The residues are:

\[
\operatorname{Res}_{x=0}\Omega=1,
\]

\[
\operatorname{Res}_{x=1}\Omega=-1.
\]

For a \(d\)-dimensional simplex with positive coordinates

\[
x_i>0,
\qquad
\sum_{i=1}^d x_i<1,
\]

the canonical form is

\[
\Omega
=
d\log x_1
\wedge
\cdots
\wedge
d\log x_d
\wedge
d\log\left(1-\sum_i x_i\right).
\]

This illustrates the general principle: boundaries determine the form.

---

## Appendix B: Positive Grassmannian

The Grassmannian \(G(k,n)\) is the space of \(k\)-planes in \(n\)-dimensional space.

A point may be represented by a \(k\times n\) matrix \(C\), modulo \(GL(k)\).

Maximal minors are

\[
\Delta_{i_1\cdots i_k}
=
\det
\left(
C_{\alpha,i_a}
\right).
\]

The positive Grassmannian \(G_+(k,n)\) is the subset where all ordered minors are positive:

\[
\Delta_{i_1<\cdots<i_k}>0.
\]

This positivity is the foundation of on-shell diagrams and the amplituhedron.

---

## Appendix C: Momentum Twistors

For planar massless momenta,

\[
p_i=\lambda_i\tilde\lambda_i,
\]

define dual coordinates \(x_i\) by

\[
p_i=x_i-x_{i+1}.
\]

Momentum twistors are

\[
Z_i=(\lambda_i,\mu_i),
\]

with

\[
\mu_i=x_i\lambda_i.
\]

The four-bracket is

\[
\langle i j k l\rangle
=
\epsilon_{IJKL}
Z_i^I Z_j^J Z_k^K Z_l^L.
\]

These brackets are the basic conformally invariant variables of the amplituhedron.

---

## Appendix D: BCFW Recursion

A BCFW shift deforms two spinors:

\[
\hat\lambda_i
=
\lambda_i
+
z\lambda_j,
\]

\[
\hat{\tilde\lambda}_j
=
\tilde\lambda_j
-
z\tilde\lambda_i.
\]

The amplitude becomes a rational function of \(z\):

\[
\mathcal{M}(z).
\]

If \(\mathcal{M}(z)\to 0\) as \(z\to\infty\), Cauchy’s theorem gives

\[
\mathcal{M}(0)
=
\sum_{\text{poles }z_P}
\operatorname{Res}_{z=z_P}
\frac{\mathcal{M}(z)}{z}.
\]

This yields

\[
\mathcal{M}
=
\sum_P
\mathcal{M}_L(z_P)
\frac{1}{P^2}
\mathcal{M}_R(z_P).
\]

Geometrically, BCFW recursion triangulates the amplituhedron.

---

## Appendix E: Associahedron Variables

For planar \(n\)-point kinematics, define

\[
X_{ij}
=
(p_i+p_{i+1}+\cdots+p_{j-1})^2.
\]

The planar associahedron is cut out by

\[
X_{ij}\geq 0,
\]

and linear relations such as

\[
X_{ij}+X_{i+1,j+1}
-
X_{i,j+1}
-
X_{i+1,j}
=
s_{ij}.
\]

The canonical form has poles at

\[
X_{ij}=0.
\]

These poles correspond to physical factorization channels.

---

## Appendix F: Cosmological Polytope Sketch

For a graph \(G\) with vertices \(v\) and edges \(e\), introduce variables associated with energies.

The cosmological polytope \(\mathcal{P}_G\) is defined by linear inequalities reflecting graph connectivity.

The wavefunction coefficient is obtained by restricting the canonical form to the late-time hyperplane:

\[
\psi_G
=
\Omega(\mathcal{P}_G)
\big|_{\sum E=0}.
\]

Boundaries correspond to:

1. total-energy poles,
2. partial-energy poles,
3. flat-space factorization,
4. cosmological soft limits.

---

## Selected References

1. R. Donagi and E. Witten, “Super Atiyah Classes and Obstructions to Splitting of Supercurves,” *Pure and Applied Mathematics Quarterly* **10**, 473 (2014).  
2. N. Arkani-Hamed and J. Trnka, “The Amplituhedron,” *Journal of High Energy Physics* **1410**, 030 (2014).  
3. N. Arkani-Hamed, F. Cachazo, and J. Kaplan, “What Is the Simplest Quantum Field Theory?” *Journal of High Energy Physics* **1009**, 016 (2010).  
4. N. Arkani-Hamed, F. Cachado, C. Cheung, and J. Kaplan, “The S-Matrix in Twistor Space,” *Journal of High Energy Physics* **1003**, 110 (2010).  
5. L. Mason and D. Skinner, “Scattering Amplitudes and BCFW in Twistor Space,” *Journal of High Energy Physics* **1007**, 077 (2010).  
6. A. Hodges, “Eliminating Spurious Poles from Gauge-Theoretic Amplitudes,” *Journal of High Energy Physics* **1305**, 135 (2013).  
7. R. Britto, F. Cachazo, B. Feng, and E. Witten, “Direct Proof of Tree-Level Recursion Relation in Yang-Mills Theory,” *Physical Review Letters* **94**, 181602 (2005).  
8. N. Arkani-Hamed, J. L. Bourjot, F. Cachazo, and J. Trnka, “Local Integrals for Planar Scattering Amplitudes,” *Communications in Mathematical Physics* **328**, 1 (2014).  
9. N. Arkani-Hamed, Y. Bai, S. He, and G. Yan, “Scattering Forms and the Positive Geometry of Kinematics, Color and the Worldsheet,” *Journal of High Energy Physics* **1805**, 096 (2018).  
10. N. Arkani-Hamed, S. He, and T. Lam, “Positive Geometry and Scattering Forms,” *Journal of High Energy Physics* (2018).  
11. N. Arkani-Hamed, P. Benincasa, and A. Pochinsky, “The Cosmological Polytope and the Wavefunction of the Universe,” *Journal of High Energy Physics* **1711**, 123 (2017).  
12. P. Benincasa, “From the Flat-Space S-Matrix to the Wavefunction of the Universe,” arXiv:1811.02515.  
13. S. Fomin and A. Zelevinsky, “Cluster Algebras I: Foundations,” *Journal of the American Mathematical Society* **15**, 497 (2002).  
14. J. Golden, A. B. Goncharov, M. Spradlin, C. Vergu, and A. Volovich, “Motivic Amplitudes and Cluster Coordinates,” *Journal of High Energy Physics* **1401**, 091 (2014).  
15. J. M. Drummond, J. Henn, G. P. Korchemsky, and E. Sokatchev, “Dual Superconformal Symmetry of Scattering Amplitudes in \(\mathcal{N}=4\) Super-Yang-Mills Theory,” *Nuclear Physics B* **828**, 317 (2010).  
16. F. Cachazo, S. He, and E. Y. Yuan, “Scattering of Massless Particles in Arbitrary Dimensions,” *Physical Review Letters* **113**, 171601 (2014).  
17. F. Cachazo, S. He, and E. Y. Yuan, “Scattering Equations and Matrices: From Einstein to Yang-Mills, DBI and NLSM,” *Journal of High Energy Physics* **1507**, 149 (2015).  
18. N. Arkani-Hamed, Y. Bai, and T. Lam, “Positive Geometries and Canonical Forms,” *Journal of High Energy Physics* **1711**, 039 (2017).  
19. S. Caron-Huot, “Superconformal Symmetry and Two-Loop Amplitudes in Planar \(\mathcal{N}=4\) Super Yang-Mills,” *Journal of High Energy Physics* **1112**, 066 (2011).  
20. L. J. Dixon, J. M. Drummond, and J. M. Henn, “Bootstrapping the Three-Loop Hexagon,” *Journal of High Energy Physics* **1111**, 023 (2011).  
21. D. Speyer and L. Williams, “The Tropical Totally Positive Grassmannian,” *Journal of Algebraic Combinatorics* **22**, 189 (2005).  
22. N. Arkani-Hamed, T. Lam, and M. Spradlin, “Positive Configuration Space,” *Communications in Mathematical Physics* **384**, 909 (2021).  
23. H. Elvang and Y.-t. Huang, *Scattering Amplitudes in Gauge Theory and Gravity* (Cambridge University Press, 2015).  
24. J. M. Henn and J. C. Plefka, *Scattering Amplitudes in Gauge Theories* (Springer, 2014).  
25. C. Cheung, “TASI Lectures on Scattering Amplitudes,” arXiv:1708.03872.
