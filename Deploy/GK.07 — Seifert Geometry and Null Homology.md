General Relativity × Knot Theory

Topology of Closed Null Geodesics and Link Invariants of Spacetime

Part VII — Seifert Geometry and Null Homology

⸻

45. Introduction: Geometry Beneath Polynomial Invariants

Part VI introduced algebraic compression of null topology through:

[
J_N,
\qquad
\mathcal H_N,
\qquad
\mathcal J[g].
]

Polynomial invariants classify topology without explicitly constructing bounding geometry.

The present part develops the geometric substrate beneath those invariants.

Classical knot theory associates to every oriented link a spanning surface.

General relativity requires an extension in which closed null geodesics bound generalized surfaces compatible with Lorentzian causal structure.

The objective is to construct:

[
\text{Null Knots}
\rightarrow
\text{Seifert Geometry}
\rightarrow
\text{Homology}
\rightarrow
\text{Cobordism}.
]

⸻

46. Seifert Surfaces Bounded by Null Loops

46.1 Classical Construction

For a knot:

[
K:S^1\hookrightarrow\Sigma,
]

a Seifert surface is a compact orientable surface:

[
S
]

satisfying:

[
\partial S=K.
]

Its genus measures geometric complexity.

The challenge in Lorentzian geometry is that null trajectories possess degenerate tangent structure.

⸻

46.2 Null Seifert Surface

Let:

[
\gamma\in\mathcal N_c.
]

Define a Null Seifert Surface as a smooth immersion:

[
\boxed{
\mathcal S:
\Sigma_g\hookrightarrow M
}
]

such that:

[
\partial\Sigma_g=\gamma,
]

and:

[
g|_{T\Sigma}
]

remains nondegenerate except along the null boundary.

Boundary condition:

[
g(\dot\gamma,\dot\gamma)=0.
]

Interior condition:

[
\det(g_{ab})\neq0.
]

Thus only the boundary carries null degeneracy.

⸻

46.3 Optical Normal Field

Introduce local basis:

[
{e_1,e_2}
\subset
T\Sigma.
]

Define induced metric:

[
h_{ab}

g(e_a,e_b).
]

Introduce generalized normal:

[
N^\mu
]

satisfying:

[
g(N,e_a)=0.
]

Near the null boundary:

[
g(N,N)\rightarrow0.
]

This defines a continuous causal transition.

⸻

46.4 Existence Condition

A null knot admits a Seifert surface iff:

[
[\gamma]

0
\in
H_1(M).
]

Nontrivial homology obstructs filling.

⸻

Definition 16 (Null Seifert Set)

Define:

[
\boxed{
\mathfrak S(\gamma)

{
\Sigma:
\partial\Sigma=\gamma
}
}
]

This set parameterizes all allowable fillings.

⸻

47. Genus of Null Families

Topology enters through minimal complexity.

⸻

47.1 Null Seifert Genus

For:

[
\gamma
]

define:

[
\boxed{
g_N(\gamma)

\min_{\Sigma\in\mathfrak S(\gamma)}
g(\Sigma)
}
]

Interpretation:

minimum number of handles required to fill the closed light orbit.

⸻

47.2 Null Genus of Multi-Component Links

For:

[
L

{
\gamma_1,\ldots,\gamma_n
},
]

define:

[
\Sigma

\cup_i\Sigma_i.
]

Total genus:

[
\boxed{
g_N(L)

\sum_i g_N(\gamma_i)
+\Delta_g
}
]

where:

[
\Delta_g
]

measures interaction topology.

⸻

47.3 Curvature-Corrected Genus

Geometry modifies complexity.

Define effective genus:

[
\boxed{
g_{\mathrm{eff}}

g_N
+
\alpha
\int_\Sigma
R,dA
}
]

Interpretation:

curvature contributes to topological cost.

⸻

Theorem 7 (Genus Stability)

Suppose:

[
g\rightarrow g+\epsilon h.
]

If:

1. no orbit collision occurs,
2. isotopy class preserved,

then:

[
g_N

\mathrm{constant}.
]

Proof.

Boundary isotopy extends to spanning surfaces.

Genus cannot change continuously.

∎

⸻

47.4 Genus Spectrum

Define:

[
\Gamma(M,g)

{
g_N(L_i)
}.
]

Multiplicity:

[
m(g).
]

Average genus:

[
\langle g\rangle

\frac{
\sum
m_i g_i
}{
\sum m_i
}.
]

This quantity contributes directly to polynomial coefficients.

⸻

48. Homological Decomposition

Polynomial invariants remain incomplete without global topology.

Homology organizes null-link sectors.

⸻

48.1 Null Cycle Space

Closed null loops generate cycles.

Define:

[
Z_1^N
\subset
Z_1(M).
]

Boundaries:

[
B_1^N.
]

Construct quotient:

[
\boxed{
H_1^N(M)

Z_1^N/B_1^N
}
]

called the Null Homology Group.

⸻

48.2 Null Homology Classes

Each closed orbit defines:

[
[\gamma]
\in
H_1^N(M).
]

Equivalent trajectories satisfy:

[
[\gamma_1]=[\gamma_2].
]

Distinct classes cannot be continuously filled into one another.

⸻

48.3 Homological Decomposition of the Spectrum

Partition:

[
\mathcal L(M,g)

\bigsqcup_a
\mathcal L_a.
]

Each sector satisfies:

[
[L]
\in
H_1^N(M)_a.
]

Thus:

[
\boxed{
\mathcal L

\bigoplus_a
\mathcal L_a
}
]

This decomposition isolates independent optical topologies.

⸻

48.4 Homological Weight Functional

Define:

[
\omega_a

\frac{
|\mathcal L_a|
}{
|\mathcal L|
}.
]

Then:

[
\sum_a\omega_a=1.
]

Interpretation:

fraction of null topology stored in each homological sector.

⸻

Definition 17 (Null Homological Complexity)

Define:

[
\boxed{
C_H

-\sum_a
\omega_a
\log\omega_a
}
]

This entropy measures topological fragmentation.

⸻

49. Cobordism of Null Geodesics

Homology classifies cycles.

Cobordism classifies transitions.

⸻

49.1 Null Cobordism

Two null links:

[
L_1,
L_2
]

are cobordant if:

[
\exists
W
]

such that:

[
\partial W

L_1
\cup
(-L_2).
]

Interpretation:

a continuous spacetime sheet transforms one optical topology into another.

⸻

49.2 Lorentzian Cobordism Surface

Define immersion:

[
W:
\Sigma\times[0,1]
\hookrightarrow M.
]

Boundary:

[
W_0=L_1,
]

[
W_1=L_2.
]

Interior metric:

[
\mathrm{rank}(g|_W)

]

Degeneracy allowed only on null boundaries.

⸻

Definition 18 (Null Cobordism Class)

Define:

[
\boxed{
[L_1]\sim_C[L_2]
}
]

iff a null cobordism exists.

Equivalence classes:

[
\Omega_N.
]

⸻

49.3 Cobordism Action

Associate functional:

[
\boxed{
\mathcal A_C(W)

\int_W
(R+\lambda K),dV
}
]

where:

[
K
]

is null extrinsic curvature.

Transitions prefer minimal action.

⸻

Theorem 8 (Cobordism Conservation)

If:

1. metric evolution smooth,
2. no singular reconnection,

then:

[
[L(t)]
\in
\Omega_N
]

remains constant.

Proof.

Smooth isotopy induces smooth cobordism.

Class preserved.

∎

⸻

49.4 Cobordism Category of Null Flow

Objects:

[
\mathrm{Obj}

\mathfrak N.
]

Morphisms:

[
\mathrm{Mor}

\Omega_N.
]

Composition:

[
W_1\circ W_2.
]

This defines category:

[
\boxed{
\mathbf{NullCob}
}
]

which encodes allowable causal-topological evolution.

⸻

50. Fifth Structural Principle

Principle V — Topology Emerges Through Fillings

Closed null geodesics are not isolated curves.

They organize into surfaces, homology sectors, and cobordism classes.

Symbolically:

[
(M,g)
\rightarrow
\mathcal L
\rightarrow
H_1^N
\rightarrow
\Omega_N.
]

The geometry of spacetime becomes recoverable through the topology of how light loops may be filled.

⸻

Transition to Part VIII

Part VIII develops the first complete classification proposal:

Classification of Spacetimes by Null Topology

including:

* equivalence of spacetimes by null-link spectra,
* topological phase diagrams,
* reconstruction classes,
* emergence of a null-topological taxonomy.
