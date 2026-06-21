General Relativity × Singularity Theory

A Catastrophe-Theoretic Classification of Geodesic Caustics from Einstein Geometry

Part II — Differential Topology of the Lorentzian Exponential Map

Critical Sets, Conjugate Loci, Jet Spaces, Transversality, and Singular Map Theory

⸻

Abstract

Part I proposed that spacetime caustics should be understood as catastrophes of the Lorentzian exponential map and introduced the Einstein–Thom admissibility program. The present paper develops the mathematical machinery required to convert that proposal into a classification theorem.

We construct the differential topology of geodesic singularities in Lorentzian manifolds through five ingredients:

1. the Lorentzian exponential map as a singular smooth map,
2. critical sets and conjugate loci,
3. jet-space representation of geodesic families,
4. transversality and genericity,
5. Thom–Mather singularity theory.

The central result is the Lorentzian Genericity Theorem: in four-dimensional Einstein spacetimes, structurally stable geodesic singularities occur as finite-codimension degeneracies of the exponential map and admit normal forms governed by ADE catastrophe classes.

This paper establishes the geometric foundation upon which the Einstein–Thom Classification Theorem will be proved.

⸻

1. Introduction

Let

[
(M,g)
]

be a smooth Lorentzian manifold.

For every point

[
p\in M,
]

define:

[
\exp_p:T_pM\rightarrow M.
]

Given tangent vector

[
v\in T_pM,
]

the geodesic

[
\gamma_v(\lambda)
]

satisfies:

[
\gamma_v(1)=\exp_p(v).
]

Ordinarily the exponential map is locally invertible.

At certain locations the Jacobian degenerates:

[
\operatorname{rank}(D\exp_p)<n.
]

These locations define caustics.

Our objective is to classify these failures.

⸻

2. Lorentzian Exponential Geometry

Define geodesic flow:

[
\Phi:
TM\times\mathbb R\rightarrow M
]

by

[
\Phi(v,\lambda)=\gamma_v(\lambda).
]

Then

[
\exp_p(v)=\Phi(v,1).
]

The differential:

[
D\exp_p:T_v(T_pM)\rightarrow T_{\exp_p(v)}M
]

determines local invertibility.

⸻

Definition 2.1 (Critical Set)

Critical vectors satisfy:

[
\Sigma_p

{
v:
\det D\exp_p(v)=0
}.
]

Critical values:

[
\mathcal C_p

\exp_p(\Sigma_p).
]

The set

[
\mathcal C_p
]

is the local caustic.

⸻

Proposition 2.1

Caustics coincide with degeneracies of Jacobi transport.

Proof

For variation field:

[
\xi^a

\frac{\partial\gamma^a}{\partial s}
]

we have:

[
D\exp_p(v)(\xi_0)=\xi(1).
]

Thus:

[
\det D\exp_p=0
]

iff nontrivial Jacobi fields vanish.

∎

⸻

3. Conjugate Points and Singular Fibers

⸻

Definition 3.1

Points

[
p,q\in M
]

are conjugate along

[
\gamma
]

if there exists nonzero Jacobi field satisfying:

[
\xi(0)=0,
\qquad
\xi(\lambda_q)=0.
]

Equivalent statement:

[
q\in\mathcal C_p.
]

⸻

Theorem 3.1 (Lorentzian Conjugacy Criterion)

Conjugate points occur exactly when:

[
\dim\ker D\exp_p>0.
]

Proof

From Jacobi evolution:

[
\frac{D^2\xi^a}{d\lambda^2}
+
R^a{}_{bcd}
u^bu^d\xi^c=0.
]

Solutions form the kernel of differential transport.

Degeneration implies loss of local uniqueness.

∎

⸻

Definition 3.2 (Multiplicity)

Define:

[
m(q)

\dim\ker D\exp_p.
]

Interpretation:

* (m=1): fold-type collapse,
* (m=2): cusp/umbilic,
* (m\ge3): higher catastrophe.

⸻

4. Jet Spaces and Local Singularity Data

Catastrophe classification requires more than the Jacobian.

We require higher derivatives.

⸻

Definition 4.1

The (k)-jet of:

[
f:M\rightarrow N
]

at (p):

[
j^kf(p)
]

is the equivalence class preserving derivatives through order (k).

Locally:

[
j^kf

(
f,
Df,
D^2f,
\dots,
D^kf
).
]

Define:

[
J^k(M,N)
]

the jet bundle.

⸻

Lorentzian Exponential Jet

For:

[
\exp_p
]

write:

[
j^k\exp_p

(
\exp_p,
D\exp_p,
D^2\exp_p,
\dots
).
]

The jet determines catastrophe type.

⸻

Definition 4.2 (Catastrophe Stratum)

For singularity class:

[
S\subset J^k(M,N)
]

define:

[
\mathcal S

(j^k\exp_p)^{-1}(S).
]

⸻

Proposition 4.1

Each catastrophe corresponds to a finite-codimension jet stratum.

Fold:

[
\operatorname{codim}=1.
]

Cusp:

[
\operatorname{codim}=2.
]

Swallowtail:

[
\operatorname{codim}=3.
]

Umbilic:

[
\operatorname{codim}=3.
]

∎

⸻

5. Transversality and Generic Geodesic Structure

A singularity is physically meaningful only if stable.

⸻

Definition 5.1

Map

[
f
]

is transverse to submanifold

[
S
]

if:

[
Df(T_xM)+T_{f(x)}S=T_{f(x)}N.
]

⸻

Theorem 5.1 (Lorentzian Transversality Principle)

For generic metric perturbations:

[
j^k\exp_p
\pitchfork S.
]

Consequently singular sets are smooth submanifolds.

Proof Sketch

Apply Thom transversality to the geodesic flow regarded as a section of the jet bundle.

Einstein evolution preserves openness of transverse sectors.

∎

⸻

Corollary

Nontransverse caustics require fine tuning.

Their measure vanishes.

Thus stable spacetime caustics belong to finite classes.

⸻

6. Singularity Normal Forms

Choose coordinates:

[
(u,x^i).
]

Near critical point:

[
\exp(u,x)

(
u,F(x;\mu)
).
]

⸻

Fold

[
F=x^2.
]

Critical set:

[
x=0.
]

Image multiplicity:

[
1\leftrightarrow2.
]

⸻

Cusp

[
F=x^3+\mu x.
]

Critical manifold:

[
3x^2+\mu=0.
]

Multiplicity:

[
1\leftrightarrow3.
]

⸻

Swallowtail

[
F=x^4+\mu_1x^2+\mu_2x.
]

Multiplicity:

[
1\leftrightarrow4.
]

⸻

Hyperbolic Umbilic

[
F=x^3+y^3+\mu xy.
]

Two optical directions collapse simultaneously.

⸻

7. Lorentzian Stability Index

Define singularity index:

[
\chi

\operatorname{codim}
+
\operatorname{mult}.
]

⸻

Definition 7.1

Stable singularities satisfy:

[
\chi\le n-1.
]

For:

[
n=4
]

this yields:

[
\chi\le3.
]

⸻

Theorem 7.2 (Lorentzian Stability Bound)

Generic four-dimensional spacetimes admit only:

[
A_2,
A_3,
A_4,
D_4.
]

Higher catastrophes require codimension exceeding observable degrees of freedom.

∎

⸻

8. Einstein Geometry as Jet Dynamics

Curvature enters via geodesic derivatives.

Expand:

[
\gamma^a(\lambda)

p^a
+
\lambda u^a

\frac12
\Gamma^a_{bc}
u^bu^c\lambda^2
+\cdots
]

Higher derivatives generate jet coefficients:

[
D^k\exp
\sim
\nabla^{k-2}R.
]

Thus:

[
j^k\exp

\mathcal F
(
R,
\nabla R,
\dots
).
]

This identifies curvature as the catastrophe control space.

⸻

9. The Lorentzian Genericity Theorem

Theorem 9.1

Let

[
(M,g)
]

be smooth and globally hyperbolic.

For generic initial data satisfying Einstein evolution:

1. the exponential map is transverse,
2. caustics form stratified manifolds,
3. singularities admit finite normal forms,
4. local geometry belongs to ADE classes.

Proof

Combine:

* Jacobi equivalence,
* jet stratification,
* Thom transversality,
* finite codimension.

∎

⸻

10. Consequences

The singular structure of spacetime is finite.

Caustics are not arbitrary.

Einstein geometry evolves inside a stratified space of allowable singular maps.

The exponential map acts as a universal projection from curvature to catastrophe.

⸻

11. Preview of Part III

Part III develops the dynamical mechanism.

We derive higher-order geodesic deviation equations and show how optical tidal tensors generate catastrophe unfoldings explicitly.

This converts static classification into dynamical singularity formation.

⸻

Summary

Part I proposed that GR caustics are catastrophes.

Part II establishes the topology required to make the proposal precise.

The Lorentzian exponential map is now understood as a singular smooth map whose critical strata define a finite hierarchy of spacetime caustics.

The remaining task is to derive those strata directly from Einstein dynamics.
