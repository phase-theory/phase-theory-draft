General Relativity × Knot Theory

Topology of Closed Null Geodesics and Link Invariants of Spacetime

Part VIII — Classification of Spacetimes by Null Topology

⸻

51. Introduction: Toward a Topological Taxonomy of Relativity

The previous parts developed a sequence of structures:

[
(M,g)
\rightarrow
\mathcal N_c
\rightarrow
\mathfrak N
\rightarrow
\mathcal L
\rightarrow
\mathcal J[g]
\rightarrow
(H_1^N,\Omega_N).
]

The resulting framework no longer treats curvature as the sole global descriptor of spacetime.

Instead, spacetime becomes characterized by the topology of its closed-null flow.

The objective of this part is to construct a complete classification principle.

The central question is:

When should two spacetimes be considered topologically identical from the viewpoint of light?

The proposal developed here is:

Two spacetimes are equivalent when their complete null-link spectra coincide.

This establishes a new taxonomy independent of ordinary manifold topology.

⸻

52. Null-Topological Equivalence

52.1 Motivation

Classical Lorentzian classification distinguishes spacetimes through:

* metric tensors,
* curvature invariants,
* holonomy,
* causal structure,
* manifold topology.

These descriptors do not directly classify recurrent light organization.

Null topology introduces a new equivalence relation.

⸻

52.2 Spectrum Equivalence

Let:

[
(M,g),
\qquad
(M’,g’)
]

be admissible null-knot spacetimes.

Recall:

[
\mathcal L(M,g)

{
([L],\lambda,\mu,\mathfrak I)
}.
]

⸻

Definition 19 (Null-Link Equivalence)

Define:

[
\boxed{
(M,g)
\sim_N
(M’,g’)
}
]

iff:

[
\boxed{
\mathcal L(M,g)

\mathcal L(M’,g’)
}
]

after normalization of length scales.

Explicitly:

[
\hat{\mathcal L}(M,g)

\hat{\mathcal L}(M’,g’).
]

This relation identifies spacetimes possessing identical closed-null topology.

⸻

52.3 Equivalence Class

Define:

[
[(M,g)]_N

{
(M’,g’):
(M’,g’)\sim_N(M,g)
}.
]

The collection:

[
\mathfrak T_N

{
[(M,g)]_N
}
]

is called the Null-Topological Moduli Space.

⸻

Theorem 9 (Equivalence Properties)

The relation:

[
\sim_N
]

is:

1. reflexive,

[
(M,g)\sim_N(M,g),
]

2. symmetric,

[
(M,g)\sim_N(M’,g’)
\Rightarrow
(M’,g’)\sim_N(M,g),
]

3. transitive.

Proof.

Inherited directly from set equality on normalized spectra.

∎

⸻

53. Spectral Separation and Classification Metrics

Equivalent spectra classify identical null topology.

To distinguish inequivalent geometries we introduce distances.

⸻

53.1 Spectral Separation Functional

Define:

[
D_N:
\mathfrak T_N\times\mathfrak T_N
\rightarrow
\mathbb R.
]

Proposed form:

[
\boxed{
D_N^2

\alpha D_\lambda^2
+
\beta D_J^2
+
\gamma D_H^2
+
\delta D_M^2
}
]

where:

[
D_\lambda
]

compares orbit spectra,

[
D_J
]

compares polynomial invariants,

[
D_H
]

compares homology sectors,

[
D_M
]

compares multiplicities.

⸻

53.2 Strong Equivalence

Define:

[
(M,g)\equiv_N(M’,g’)
]

iff:

[
D_N=0.
]

Strong equivalence preserves complete null organization.

⸻

53.3 Weak Equivalence

Define:

[
(M,g)\approx_N(M’,g’)
]

iff:

[
D_N<\epsilon.
]

This captures approximate optical universality.

⸻

54. Topological Phase Diagram of Spacetime

The null-link spectrum introduces a phase structure.

A spacetime becomes a point inside an abstract topological phase space.

⸻

54.1 Phase Coordinates

Assign coordinates:

[
X_N

(
H_N,
\langle g\rangle,
\mathfrak M,
S_N
).
]

Components:

[
H_N
]

null-link entropy rate,

[
\langle g\rangle
]

mean Seifert genus,

[
\mathfrak M
]

multiplicity functional,

[
S_N
]

ensemble entropy.

⸻

54.2 Null Phase Space

Define:

[
\boxed{
\mathscr P_N

{
X_N
}
}
]

Every admissible spacetime occupies a region.

Metric evolution becomes trajectory:

[
X_N(t).
]

⸻

54.3 Critical Surfaces

Transitions occur where:

[
\det(I-M)=0.
]

Define phase boundary:

[
\Sigma_C.
]

Crossing:

[
\Sigma_C
]

changes null topology.

⸻

Definition 20 (Null Topological Phase)

A phase is a connected component:

[
\mathscr C
\subset
\mathscr P_N
]

with invariant:

[
\mathcal L=\mathrm{constant}.
]

⸻

54.4 Order Parameters

Introduce:

[
\Theta_1

H_N,
]

[
\Theta_2

S_G,
]

[
\Theta_3

\deg\mathcal J.
]

Topological phase transitions occur when any parameter becomes nonanalytic.

⸻

55. New Spacetime Taxonomy

We now propose a classification system.

⸻

Class 0 — Null-Trivial Spacetimes

Condition:

[
\mathcal L=\varnothing.
]

Properties:

* no closed null orbits,
* globally hyperbolic,
* no optical recurrence.

Examples:

ordinary causal geometries.

⸻

Class I — Periodic Optical Spacetimes

Condition:

[
|\mathcal L|<\infty.
]

Properties:

* finite null-link spectrum,
* isolated optical sectors.

⸻

Class II — Linked Optical Spacetimes

Condition:

[
\exists
L:
\mathfrak L\neq0.
]

Properties:

* nontrivial pairwise linking,
* conserved optical charge.

⸻

Class III — Knot-Dense Spacetimes

Condition:

[
H_N>0.
]

Properties:

* infinitely many knot sectors,
* positive spectral entropy.

⸻

Class IV — Homologically Stratified Spacetimes

Condition:

[
\mathrm{rank}
(H_1^N)>1.
]

Properties:

* multiple null homology sectors,
* structured topology.

⸻

Class V — Polynomially Chaotic Spacetimes

Condition:

[
\deg\mathcal J\rightarrow\infty.
]

Properties:

* divergent knot complexity,
* fractal null spectra.

⸻

Class VI — Spectrally Complete Spacetimes

Condition:

[
\mathcal L
]

uniquely determines geometry.

Properties:

* reconstruction possible,
* maximal optical information.

⸻

Definition 21 (Null Topological Dimension)

Define:

[
\boxed{
d_N

\limsup_{\Lambda\to\infty}
\frac{
\log N(\Lambda)
}{
\log\Lambda
}
}
]

Interpretation:

effective dimensionality of null topology.

⸻

56. Reconstruction Classes

Classification is meaningful only if spectra contain geometry.

⸻

Definition 22 (Reconstructible Class)

A class:

[
\mathfrak C
]

is reconstructible if:

[
\mathcal L(M,g)
\Rightarrow
[(M,g)].
]

⸻

Theorem 10 (Spectral Reconstruction Criterion)

Suppose:

1. null spectrum complete,
2. multiplicity finite,
3. homology finite rank.

Then:

[
\mathcal L
]

determines null-topological class.

Proof.

Equivalent spectra imply identical polynomial and homological data.

Classification follows.

∎

⸻

Corollary

Curvature invariants alone do not generally determine:

[
[(M,g)]_N.
]

Null topology supplies independent information.

⸻

57. Sixth Structural Principle

Principle VI — Light Defines Geometry

Two spacetimes are equivalent whenever their complete closed-null topology is equivalent.

Symbolically:

[
\boxed{
(M,g)
\sim_N
(M’,g’)
\iff
\mathcal L(M,g)

\mathcal L(M’,g’)
}
]

Geometry is reinterpreted as an equivalence class of null-link organization.

⸻

Transition to Part IX

Part IX turns from abstract classification to explicit spacetime models:

Applications to Known Solutions of Einstein Geometry

including:

* rotating geometries,
* compactified spacetimes,
* trapped photon regions,
* explicit computation of null-link spectra.
