General Relativity × Singularity Theory

A Catastrophe-Theoretic Classification of Geodesic Caustics from Einstein Geometry

Part I — Foundations, Variational Geometry, and the Caustic Classification Program

⸻

Abstract

Geodesic congruences in General Relativity generically develop focusing singularities. Under the energy conditions and global assumptions of the classical focusing theorems, neighboring geodesics intersect and produce caustics—points at which the exponential map ceases to be locally invertible. Independently, catastrophe theory establishes a complete classification of structurally stable singularities of smooth maps in low codimension, yielding the ADE hierarchy of folds, cusps, swallowtails, butterflies, and umbilic singularities.

This work develops a unified geometric theory identifying spacetime caustics with catastrophes of the Lorentzian exponential map. The central objective is to derive a complete taxonomy of physically realizable caustic singularities directly from Einstein curvature and the dynamics of geodesic congruences.

We formulate a Lorentzian catastrophe bundle over spacetime, define Einstein–Thom admissibility conditions, and derive curvature criteria selecting allowable catastrophe classes for timelike and null congruences. The principal conjectural result established in this opening paper is that generic geodesic caustics in four-dimensional General Relativity belong to a restricted ADE spectrum whose realization is determined by optical tidal invariants and codimension constraints.

This framework converts singularity formation from a local focusing statement into a complete classification problem.

⸻

1. Introduction

The geometry of spacetime is encoded through the Einstein equations:

[
G_{ab}+\Lambda g_{ab}=8\pi T_{ab}.
]

The equations determine curvature; curvature determines geodesic deviation; geodesic deviation determines focusing.

Classical singularity theorems demonstrate that geodesics may become incomplete, but provide limited information regarding the internal structure of the focusing event itself.

The missing problem is:

What kinds of singularities can geodesic focusing produce?

Catastrophe theory supplies a natural language.

If

[
\exp_p:T_pM\rightarrow M
]

denotes the exponential map, then geodesic caustics occur precisely where

[
\det D\exp_p=0.
]

This identifies caustics as singularities of smooth maps.

Thom–Arnold theory classifies generic singularities.

The proposal of this work is:

Einstein curvature determines the unfolding parameters of catastrophe geometry.

⸻

2. Geometric Framework

Let

[
(M,g)
]

be a smooth Lorentzian manifold.

Define a congruence:

[
\Gamma=
{
\gamma_s(\lambda)
}.
]

For tangent vector field

[
u^a
]

the connecting vector satisfies:

[
\frac{D^2\xi^a}{d\lambda^2}

-R^a{}_{bcd}
u^b\xi^cu^d.
]

Define Jacobi operator:

[
J(\lambda):
T_pM\rightarrow T_{\gamma(\lambda)}M.
]

Caustics arise whenever:

[
\ker J\neq0.
]

Equivalently:

[
\det J=0.
]

This is the catastrophe locus.

⸻

Definition 2.1 (Lorentzian Catastrophe Set)

The catastrophe set associated with congruence (\Gamma):

[
\mathcal C_\Gamma

{
q\in M:
\det(D\exp)=0
}.
]

⸻

Definition 2.2 (Einstein Control Parameters)

Introduce local control coordinates:

[
\mu^I

(
R_{ab}u^au^b,
C_{abcd},
\sigma_{ab},
\omega_{ab},
\theta
).
]

These determine catastrophe unfolding.

⸻

3. Optical Dynamics and Singularity Formation

Congruence evolution is governed by Raychaudhuri.

Timelike:

[
\dot\theta

-\frac13\theta^2
-\sigma^2
+\omega^2
-R_{ab}u^au^b.
]

Null:

[
\dot\theta

-\frac12\theta^2
-\sigma^2
-R_{ab}k^ak^b.
]

Focusing occurs if:

[
R_{ab}v^av^b\ge0.
]

This guarantees finite affine-time degeneration.

But Raychaudhuri determines only collapse.

It does not determine singularity type.

That requires higher-order structure.

⸻

4. Thom–Arnold Catastrophe Theory

Consider smooth potential:

[
V(x;\mu).
]

Catastrophes occur where:

[
\nabla_xV=0
]

and Hessian degenerates:

[
\det\partial_i\partial_jV=0.
]

Elementary catastrophes:

Type	Potential
Fold (A_2)	(x^3+\mu x)
Cusp (A_3)	(x^4+\mu_1x^2+\mu_2x)
Swallowtail (A_4)	(x^5+\mu_1x^3+\mu_2x^2+\mu_3x)
Butterfly (A_5)	(x^6+\cdots)
Hyperbolic Umbilic (D_4^+)	(x^3+y^3+\mu xy)
Elliptic Umbilic (D_4^-)	(x^3-xy^2)
Parabolic Umbilic (D_5)	higher degeneration

We reinterpret these as local models for exponential-map failure.

⸻

5. Lorentzian Catastrophe Correspondence

Let

[
\Phi:
(\lambda,\eta^i)
\rightarrow x^\mu
]

parameterize geodesic flow.

Critical set:

[
\operatorname{rank}(D\Phi)<n.
]

⸻

Postulate LC1 — Geodesic Catastrophe Equivalence

Every structurally stable caustic of a geodesic congruence is locally diffeomorphic to an ADE catastrophe.

⸻

Postulate LC2 — Curvature Control Principle

Control variables are generated entirely by Einstein curvature and optical invariants.

⸻

6. Einstein–Thom Admissibility

Not every catastrophe is physically realizable.

Lorentzian dynamics imposes restrictions.

Define tidal operator:

[
\mathcal T^i{}_j

-R^i{}_{0j0}.
]

Expand near caustic:

[
\det J

a_0+a_1\lambda+a_2\lambda^2+\cdots
]

Degeneracy order:

[
m

\min{
k:
a_k\neq0
}.
]

⸻

Theorem 1 (Curvature–Catastrophe Selection)

For generic four-dimensional Einstein spacetimes:

[
m
\le4
]

for codimension ≤3 singularities.

Consequently admissible generic caustics belong to:

[
A_2,A_3,A_4,D_4.
]

Butterfly and higher classes require nongeneric curvature tuning.

Sketch of Proof

Structural stability restricts codimension.

Geodesic flow contributes one evolution parameter.

Observer screen contributes two transverse coordinates.

Total unfolding dimension:

[
k\le3.
]

Arnold classification then truncates.

∎

⸻

7. Physical Interpretation

Fold (A_2)

Condition:

[
\lambda_1=0,
\qquad
\lambda_2\neq0.
]

Single transverse eigenvalue collapses.

Interpretation:

* first image pair creation,
* ordinary lensing caustic,
* Schwarzschild-like focusing.

⸻

Cusp (A_3)

Condition:

[
\lambda_1=0,
\quad
\dot\lambda_1=0.
]

Interpretation:

* triple image transitions,
* merging critical curves,
* anisotropic Weyl focusing.

⸻

Swallowtail (A_4)

Condition:

[
\ddot\lambda_1=0.
]

Interpretation:

* recursive image creation,
* evolving lens geometry.

⸻

Umbilic (D_4)

Condition:

[
\lambda_1=\lambda_2=0.
]

Interpretation:

simultaneous collapse of principal optical axes.

⸻

8. Lorentzian ADE Diagram

[
A_2
\rightarrow
A_3
\rightarrow
A_4
]

[
\downarrow
]

[
D_4
]

with transitions driven by increasing Weyl anisotropy.

⸻

9. First Global Conjecture

Conjecture G1 (Generic Einstein Caustic Spectrum)

Let

[
(M,g)
]

satisfy Einstein equations with smooth matter.

Then almost all null and timelike caustics belong to:

[
{A_2,A_3,D_4}.
]

Higher catastrophes occupy measure-zero subsets of initial data.

⸻

10. Program of Subsequent Parts

Part II:
Microlocal geometry of the exponential map.

Part III:
Rigorous classification theorem.

Part IV:
Null congruences and Penrose limits.

Part V:
Lensing observables and image multiplicities.

Part VI:
Black hole photon-ring catastrophes.

Part VII:
Cosmological caustic networks.

Part VIII:
Quantum extensions.

⸻

Conclusion

General Relativity predicts focusing.

Catastrophe theory predicts classification.

Combining them yields a new objective:

derive every possible spacetime caustic directly from Einstein geometry.

The exponential map becomes the bridge between curvature and singularity taxonomy.

This framework proposes that geodesic singularities are not arbitrary defects of evolution but members of a finite, universal Lorentzian catastrophe hierarchy.
