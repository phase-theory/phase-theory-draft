General Relativity × Knot Theory

Topology of Closed Null Geodesics and Link Invariants of Spacetime

Part IV — Link Structure of Null Geodesic Families

⸻

22. From Individual Null Knots to Null Links

Part III established that isolated closed null geodesics may be interpreted as embedded knot classes.

Physical spacetimes, however, rarely generate single isolated periodic trajectories.

Instead, families of closed light paths emerge.

The central object therefore becomes not a knot but a link.

Define:

[
L

{
\gamma_1,\ldots,\gamma_n
},
]

where:

[
\gamma_i:S^1\hookrightarrow M
]

are pairwise disjoint closed null geodesics.

The objective of this part is to define measurable topological quantities associated with such families.

⸻

23. Pairwise Linking Numbers

23.1 Classical Construction

For two disjoint oriented closed curves:

[
K_1,K_2\subset\mathbb R^3,
]

the classical Gauss linking number is:

[
Lk(K_1,K_2)

\frac1{4\pi}
\oint_{K_1}
\oint_{K_2}
\frac{
(r-r’)
\cdot
(dr\times dr’)
}{
|r-r’|^3
}.
]

This quantity counts signed winding.

Properties:

[
Lk\in\mathbb Z,
]

[
Lk(K_1,K_2)=Lk(K_2,K_1),
]

and isotopy preserves (Lk).

⸻

23.2 Null-Link Number

Let:

[
\gamma_i,\gamma_j
\in
\mathcal N_c.
]

Choose admissible projection:

[
\pi:
M\rightarrow\Sigma.
]

Define projected curves:

[
K_i=\pi(\gamma_i),
\qquad
K_j=\pi(\gamma_j).
]

Define null linking:

[
\boxed{
\mathfrak L_{ij}

Lk(K_i,K_j)
}
]

provided isotopy class is foliation-independent.

⸻

23.3 Covariant Formulation

Projection should not determine physics.

Introduce world functions.

Define:

[
\sigma(x,y)
]

as Synge’s world function.

Define separation:

[
n^\mu

\nabla^\mu\sigma.
]

Then:

[
\boxed{
\mathfrak L_{ij}

\frac1{4\pi}
\oint_{\gamma_i}
\oint_{\gamma_j}
\epsilon_{\mu\nu\rho\sigma}
,
u^\mu
v^\nu
,
\frac{
n^\rho
\nabla^\sigma\sigma
}{
(2\sigma)^{3/2}
}
}
]

where:

[
u^\mu=\dot\gamma_i,
\qquad
v^\mu=\dot\gamma_j.
]

This reduces locally to Gauss linking.

⸻

Theorem 2 (Metric Isotopy Invariance)

Suppose:

1. closed null orbits remain embedded,
2. no orbit crossing occurs,
3. spacetime remains null-knot admissible.

Then:

[
\delta\mathfrak L_{ij}=0.
]

Proof.

The integrand changes smoothly.

Topological degree remains fixed unless singular coincidence occurs.

Thus linking number is preserved.

∎

⸻

24. Generalized Gauss Linking Integral in Curved Spacetime

24.1 Geometric Motivation

Curvature alters notions of distance and parallel transport.

Classical linking must therefore be reconstructed using intrinsic geometry.

⸻

24.2 Parallel Transport Kernel

Define propagator:

[
P^\mu{}_{\nu’}(x,y).
]

Transport tangent vectors:

[
\tilde v^\mu

P^\mu{}_{\nu’}v^{\nu’}.
]

Construct generalized kernel:

[
G(x,y)

\frac{
P^\mu{}_{\nu’}
}{
(2\sigma)^{3/2}
}.
]

⸻

24.3 Curved-Space Linking Functional

Define:

[
\boxed{
\mathcal G[g]
(\gamma_i,\gamma_j)

\frac1{4\pi}
\oint
\oint
\epsilon_{\mu\nu\rho\sigma}
u^\mu
\tilde v^\nu
n^\rho
d\lambda
d\lambda’
}
]

Interpretation:

[
\mathcal G:
\mathcal N_c\times\mathcal N_c
\rightarrow
\mathbb Z.
]

⸻

24.4 Curvature Expansion

For small curvature:

[
g

\eta+h,
]

obtain:

[
\mathcal G

Lk
+
\delta_gLk
+
O(h^2).
]

First correction:

[
\delta_gLk
\propto
\int
R_{\mu\nu\rho\sigma}.
]

Thus spacetime geometry modifies optical linking.

⸻

Definition 7 (Curvature-Induced Linking)

Define:

[
\Delta\mathfrak L

\mathcal G-Lk.
]

This measures topological distortion generated purely by gravity.

⸻

25. Multi-Component Null Links

Pairwise linking is incomplete.

Families of null trajectories exhibit collective topology.

⸻

25.1 Null Link Systems

Define:

[
L_n

{
\gamma_1,\ldots,\gamma_n
}.
]

Constraint:

[
\gamma_i\cap\gamma_j=\varnothing.
]

⸻

25.2 Linking Matrix

Define:

[
\mathbf L

(\mathfrak L_{ij}).
]

Properties:

[
\mathbf L^T=\mathbf L,
]

[
\mathfrak L_{ii}=0.
]

Example:

[
\mathbf L

\begin{pmatrix}
0&2&-1\
2&0&3\
-1&3&0
\end{pmatrix}.
]

This matrix encodes pairwise topology.

⸻

25.3 Higher Linking Invariants

Pairwise data may vanish.

Example:

Borromean topology.

Introduce Milnor invariants:

[
\mu_{ijk}.
]

Define null Milnor invariant:

[
\mu^N_{ijk}.
]

Interpretation:

[
\mu^N\neq0
]

while:

[
\mathfrak L_{ij}=0.
]

This detects irreducible optical entanglement.

⸻

25.4 Hyperlink Functional

Define:

[
\boxed{
\mathfrak H(L_n)

\sum
\mathfrak L_{ij}
+
\sum
\mu^N_{ijk}
+\cdots
}
]

This becomes the total topological charge.

⸻

26. Link Spectra

The complete collection of null links defines a spacetime observable.

⸻

26.1 Link Counting Measure

Define:

[
N(L)

#
{
L_n:
\ell(L_n)<L
}.
]

⸻

26.2 Null-Link Spectrum

Define:

[
\boxed{
\mathcal L(M,g)

{
(L_n,\mathbf L)
}
}
]

This spectrum records:

* orbit lengths,
* multiplicities,
* link matrices,
* higher invariants.

⸻

26.3 Spectral Density

Define:

[
\rho(\lambda)

\sum_i
\delta(\lambda-\lambda_i).
]

where:

[
\lambda_i
]

labels link classes.

Entropy:

[
S_L

\log|\mathcal L|.
]

Interpretation:

[
S_L
]

measures causal topological complexity.

⸻

Definition 8 (Null-Link Entropy)

Define:

[
\boxed{
H_N

\limsup_{L\to\infty}
\frac1L
\log N(L)
}
]

Large values correspond to rich optical topology.

⸻

27. Topological Conservation Laws

If null links are physical observables, they require evolution laws.

⸻

27.1 Metric Evolution

Consider:

[
g\rightarrow g(t).
]

Null flow evolves.

Question:

Which quantities remain fixed?

⸻

27.2 Conserved Linking Charge

Define:

[
Q_L

\sum_{i<j}
\mathfrak L_{ij}.
]

⸻

Theorem 3 (Link Conservation)

Suppose:

1. metric evolution smooth,
2. no orbit collision,
3. no causal singularity.

Then:

[
\frac{dQ_L}{dt}=0.
]

Proof.

Linking changes only under crossing.

Smooth isotopy preserves crossing number.

Thus:

[
Q_L=\text{constant}.
]

∎

⸻

27.3 Topological Flux Equation

Introduce null-topology current:

[
J^\mu_{\mathrm{top}}.
]

Postulate:

[
\nabla_\mu J^\mu_{\mathrm{top}}=0.
]

Integral form:

[
\frac{d}{dt}
\int
J^0,dV=0.
]

Interpretation:

null topology behaves as a conserved quantity.

⸻

27.4 Link Reconnection Events

Topological conservation fails if:

[
\exists
\gamma_i\cap\gamma_j.
]

Then:

[
\Delta Q_L\neq0.
]

Interpretation:

gravitational knot transition.

⸻

28. Second Structural Principle

We now formulate the second organizing principle.

Principle II — Topological Optical Charge

The link structure of closed null geodesics behaves as a conserved global observable.

Symbolically:

[
(M,g)
\longrightarrow
\mathcal L(M,g)
]

where:

[
\mathcal L
]

contains more information than local curvature.

Spacetime geometry becomes partially encoded in the topology of light itself.

⸻

Transition to Part V

Part V introduces the central invariant of the theory:

The Null-Link Spectrum

including:

* complete spectrum construction,
* multiplicity measures,
* entropy,
* metric invariance,
* the first candidate for spacetime classification.
