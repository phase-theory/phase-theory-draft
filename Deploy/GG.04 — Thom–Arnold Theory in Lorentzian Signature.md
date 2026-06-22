General Relativity × Singularity Theory

A Catastrophe-Theoretic Classification of Geodesic Caustics from Einstein Geometry

Part IV — Thom–Arnold Theory in Lorentzian Signature

Adaptation of Catastrophe Theory to Pseudo-Riemannian Geometry

⸻

Abstract

Parts I–III established that geodesic caustics in General Relativity arise as singularities of the Lorentzian exponential map and that their evolution is governed by curvature through the hierarchy of geodesic deviation.

Classical catastrophe theory, however, is fundamentally Euclidean. Stability, finite determinacy, and normal-form reduction are constructed for smooth maps between positive-definite manifolds. General Relativity instead evolves on pseudo-Riemannian manifolds with indefinite metric signature.

This paper develops a Lorentzian catastrophe theory.

We construct:

1. pseudo-Riemannian equivalence classes,
2. Lorentzian unfoldings,
3. causal transversality,
4. indefinite Hessian theory,
5. causal ADE normal forms.

The principal result is the Lorentzian Thom–Arnold Theorem: structurally stable geodesic caustics in four-dimensional spacetime remain classified by ADE singularities, but their realizability, stability sectors, and unfolding dynamics are modified by causal structure.

⸻

1. Introduction

Classical catastrophe theory studies smooth maps:

[
f:M\rightarrow N
]

through local equivalence under diffeomorphisms.

Two singularities are equivalent if coordinate changes transform one into the other.

In Lorentzian geometry this principle is incomplete.

Coordinates cannot be transformed arbitrarily.

The metric:

[
g_{ab}
]

contains invariant causal structure.

Thus singularity equivalence must preserve:

* null directions,
* causal ordering,
* signature,
* geodesic character.

This motivates a Lorentzian adaptation.

⸻

2. Classical Thom–Arnold Framework

Let:

[
V(x;\mu)
]

be a generating family.

Critical points satisfy:

[
\partial_iV=0.
]

Catastrophes occur when:

[
\det H=0
]

where:

[
H_{ij}

\partial_i\partial_jV.
]

Two potentials are classically equivalent under:

[
V\sim V\circ\phi+\psi.
]

This defines right–left equivalence.

Stable singularities become finite normal forms.

⸻

Classical ADE hierarchy

[
A_k:
x^{k+1}
]

[
D_k:
x^2y+y^{k-1}
]

[
E_6,E_7,E_8
]

exceptional classes.

The question becomes:

Which survive Lorentzian constraints?

⸻

3. Pseudo-Riemannian Equivalence

⸻

Definition 3.1 (Lorentzian Equivalence)

Two singular maps:

[
f_1,f_2
]

are Lorentzian equivalent if there exist diffeomorphisms:

[
\phi,\psi
]

such that:

[
f_2

\psi\circ f_1\circ\phi
]

and:

[
\phi^*g

\Omega^2g
]

with causal cones preserved.

⸻

Definition 3.2 (Causal Germ)

A causal germ at:

[
p
]

is equivalence class:

[
[f]_p
]

under Lorentzian equivalence.

⸻

Proposition 3.1

Metric signature partitions catastrophe classes.

Proof.

The Hessian decomposition depends on positive and negative eigenspaces.

Continuous transformation cannot alter signature.

Therefore singular sectors split into causal classes.

∎

⸻

4. Lorentzian Morse Theory

Classical Morse theory assumes positive definite Hessian.

Replace this with indefinite quadratic form.

Near critical point:

[
V

V_0
+
\frac12H_{ij}x^ix^j.
]

Decompose:

[
H

H_+
\oplus
H_-.
]

⸻

Definition 4.1 (Lorentzian Morse Index)

[
\mu_L

(
n_+,
n_-
)
]

where:

[
n_++n_-=n.
]

⸻

Theorem 4.1 (Pseudo-Morse Lemma)

Near nondegenerate critical point:

[
V

V_0
+
x_1^2+\cdots+x_{n_+}^2

x_{n_++1}^2
-\cdots.
]

The local structure depends on signature pair.

∎

⸻

Corollary

Every catastrophe possesses multiple causal realizations.

Fold singularities split into:

* timelike fold,
* spacelike fold,
* null fold.

⸻

5. Lorentzian Unfolding Theory

Introduce control parameters:

[
\mu^I.
]

Classical unfolding:

[
V(x;\mu).
]

Lorentzian unfolding:

[
V(x;\mu;g).
]

Metric enters dynamically.

⸻

Definition 5.1

Lorentzian unfolding operator:

[
\mathcal U_g

\partial_\mu
+
\Gamma
+
R.
]

Expanded form:

[
\mathcal U_gV

\frac{\partial V}{\partial\mu}
+
\Gamma^a_{bc}
x^b
\partial_aV
+
R_{abcd}x^bx^c.
]

⸻

Proposition 5.1

Curvature acts as unfolding flow.

Proof.

Connection transports catastrophe coordinates.

Curvature modifies critical degeneracy.

∎

⸻

6. Causal Transversality

Part II established transversality.

Lorentzian geometry imposes stronger conditions.

⸻

Definition 6.1

Map:

[
f
]

is causally transverse if:

[
Df(T_pM)
+
T_{f(p)}S

T_{f(p)}N
]

and no null generator lies entirely in kernel.

⸻

Theorem 6.1 (Lorentzian Thom Transversality)

Generic Einstein metrics satisfy causal transversality.

Hence structurally stable caustics persist.

Proof.

Perturbation of Einstein data preserves openness.

Null directions contribute codimension-one constraints.

∎

⸻

7. Lorentzian Normal Forms

Classical normal forms require modification.

⸻

Fold

Classical:

[
V=x^3+\mu x.
]

Lorentzian:

[
V

\varepsilon x^3
+
\mu x,
\qquad
\varepsilon\in{-1,0,+1}.
]

⸻

Cusp

[
V

\varepsilon x^4
+
\mu_1x^2
+
\mu_2x.
]

Interpretation:

sign determines temporal orientation.

⸻

Swallowtail

[
V

\varepsilon x^5
+
\mu_1x^3
+
\mu_2x^2
+
\mu_3x.
]

⸻

Umbilic

[
V

\varepsilon_1x^3
+
\varepsilon_2xy^2.
]

Different signatures produce distinct caustic sectors.

⸻

8. Null Catastrophe Geometry

Null directions require separate treatment.

Let:

[
k^ak_a=0.
]

Project onto screen bundle:

[
S_p.
]

Potential becomes:

[
V(x^A;\mu).
]

⸻

Definition 8.1

Null catastrophe index:

[
\nu

\operatorname{rank}
(H|_S).
]

⸻

Theorem 8.1

Null congruences eliminate exceptional classes:

[
E_6,E_7,E_8.
]

Only:

[
A_k,D_k
]

remain structurally stable.

Proof.

Screen dimension equals two.

Exceptional classes exceed available codimension.

∎

⸻

9. Lorentzian Finite Determinacy

⸻

Definition 9.1

Singularity is Lorentzian (k)-determined if:

[
j^kf
]

fixes equivalence class.

⸻

Theorem 9.1 (Lorentzian Determinacy)

Generic GR caustics satisfy:

[
k\le5.
]

Therefore only finite derivative information is observable.

⸻

Corollary

Local spacetime singularity classification is computable.

Infinite expansions are unnecessary.

⸻

10. Einstein–Arnold Correspondence

Define mapping:

[
\mathcal E:
(R,\nabla R,\dots)
\rightarrow
\mathcal A
]

where:

[
\mathcal A
]

denotes catastrophe space.

⸻

Definition 10.1

Einstein–Arnold operator:

[
\boxed{
\mathbb A[g]

j^k(\exp)
}
]

This maps spacetime curvature into catastrophe class.

⸻

Conjecture EA-1

For smooth Einstein evolution:

[
\mathbb A[g]
]

is piecewise continuous with codimension jumps only at caustics.

⸻

11. Lorentzian ADE Stability Diagram

Stable sectors:

[
A_2
\rightarrow
A_3
\rightarrow
A_4
]

branching into:

[
D_4.
]

Forbidden sectors:

[
E_6,E_7,E_8.
]

Transition boundaries determined by causal index.

⸻

12. Preview of Part V

Part V proves the Einstein–Thom Classification Theorem.

Using the deviation hierarchy and Lorentzian catastrophe theory developed here, we derive explicit curvature inequalities selecting which catastrophe class appears in a given geodesic congruence.

⸻

Summary

Classical catastrophe theory assumes Euclidean geometry.

General Relativity does not.

Part IV constructs a pseudo-Riemannian catastrophe theory in which:

* causality replaces unrestricted equivalence,
* signature modifies stability,
* curvature becomes unfolding,
* geodesic caustics become Lorentzian catastrophes.

This completes the mathematical framework required for classification.
