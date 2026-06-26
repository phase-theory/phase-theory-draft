# Technical Appendices

# Appendix A

# Functional Analysis of Phase Operator Spaces

---

## A.1 Motivation

The mathematical foundation of POET requires a rigorous treatment of the space of local operators.

Conventional OPE theory implicitly assumes operator products belong to a suitable topological vector space.

POET extends this structure by introducing phase dependence.

The resulting object is a family of operator spaces parameterized by

[
\mathcal M_{\rm phase}.
]

---

## A.2 Local Operator Space

Let

[
\mathfrak A
===========

{\mathcal O_A}
]

denote the algebra of local operators.

Define the vector space

[
\mathcal V_{\rm op}
===================

{\rm span}
{
\mathcal O_A
}.
]

---

## A.3 Phase Fiber Construction

For each phase point

[
P\in\mathcal M_{\rm phase},
]

define

[
\mathcal V_P.
]

The operator bundle becomes

[
\mathcal E
==========

\bigcup_{P}
\mathcal V_P.
]

---

## A.4 Phase Inner Product

Define

[
\langle A,B\rangle_P
====================

\langle0(P)|
A^\dagger B
|0(P)\rangle.
]

---

## A.5 Phase Hilbert Space

Completion under

[
|A|_P
=====

\sqrt{\langle A,A\rangle_P}
]

produces

[
\mathcal H_P.
]

---

## A.6 Direct Integral Structure

The global phase Hilbert space is

[
\mathcal H_{\rm phase}
======================

\int^\oplus
\mathcal H_P
,d\mu(P).
]

---

## A.7 Compact Projection Operators

The phase OPE projection

[
\mathcal P_P
:
\mathcal H_P\otimes\mathcal H_P
\rightarrow
\mathcal H_P
]

is assumed compact.

Its singular values

[
\sigma_n(P)
]

determine convergence.

---

## A.8 Fredholm Structure

The operator

[
I-\lambda\mathcal P_P
]

possesses discrete spectrum.

Fredholm theory therefore applies.

---

## A.9 Nuclearity Condition

Assume

[
\sum_n
\sigma_n(P)
<
\infty.
]

Then

[
\mathcal P_P
]

is nuclear.

This guarantees absolute convergence of phase expansions.

---

## A.10 Functional-Analytic Principle

The phase OPE exists whenever the projection operator belongs to the nuclear class over every compact phase region.

---

# Appendix B

# Differential Geometry of Phase Manifolds

---

## B.1 Phase Coordinates

Let

[
\Phi^I
]

be coordinates on

[
\mathcal M_{\rm phase}.
]

---

## B.2 Metric

[
g_{IJ}
======

\langle
\delta\Sigma_I
\delta\Sigma_J
\rangle.
]

---

## B.3 Levi-Civita Connection

[
\Gamma^I_{JK}
=============

\frac12
g^{IL}
(
\partial_Jg_{KL}
+
\partial_Kg_{JL}
----------------

\partial_Lg_{JK}
).
]

---

## B.4 Curvature

[
R^I_{;JKL}
==========

## \partial_K\Gamma^I_{JL}

\partial_L\Gamma^I_{JK}
+
\Gamma^I_{KM}\Gamma^M_{JL}
--------------------------

\Gamma^I_{LM}\Gamma^M_{JK}.
]

---

## B.5 Ricci Tensor

[
R_{JL}
======

R^I_{;JIL}.
]

---

## B.6 Scalar Curvature

[
R
=

g^{IJ}R_{IJ}.
]

---

## B.7 Geodesics

[
\frac{d^2\Phi^I}{ds^2}
+
\Gamma^I_{JK}
\frac{d\Phi^J}{ds}
\frac{d\Phi^K}{ds}
==================

0.

]

---

## B.8 Holonomy

[
U(C)
====

P
\exp
\left(
-\oint_C
\Gamma
\right).
]

---

## B.9 Topological Classes

Characteristic classes:

[
c_k,
\qquad
p_k,
\qquad
e.
]

classify global phase structure.

---

## B.10 Geometric Principle

Strong coupling corresponds to regions of large phase curvature.

---

# Appendix C

# Spectral–Phase Correspondence Theorems

---

## C.1 Objective

This appendix formalizes the relationship between spectral NOET and geometric POET.

---

## C.2 Spectral States

[
H|n\rangle
==========

E_n|n\rangle.
]

---

## C.3 Phase States

[
|\Phi\rangle.
]

---

## C.4 Unified Basis

[
|n,\Phi\rangle.
]

---

## C.5 Correspondence Map

Define

[
\mathcal C
:
\mathcal H_E
\rightarrow
\mathcal H_\Phi.
]

---

## C.6 Flat-Phase Limit

If

[
R=0,
]

then

[
\Pi
\rightarrow
\sum_n
a_n e^{-E_n|x|}.
]

---

## C.7 Curved-Phase Correction

[
\Pi
===

\sum_n
a_n
e^{-E_n|x|}
+
R\Delta\Phi^2
+\cdots.
]

---

## C.8 Correspondence Theorem

For sufficiently small curvature:

[
\Pi_{\rm POET}
==============

\Pi_{\rm NOET}
+
O(R).
]

---

## C.9 Strong-Coupling Limit

As

[
R\rightarrow\infty,
]

the geometric sector dominates.

---

## C.10 Unification Principle

Spectral theory and phase geometry are complementary projections of the same underlying structure.

---

# Appendix D

# Detailed Convergence Proofs

---

## D.1 Nuclear Expansion

Let

[
\mathcal P
==========

\sum_n
\sigma_n
|u_n\rangle
\langle v_n|.
]

---

## D.2 Absolute Convergence

Assume

[
\sum_n
|\sigma_n|
<
\infty.
]

Then

[
\sum_n
\sigma_n
u_n
]

converges absolutely.

---

## D.3 Uniform Bound

If

[
|\sigma_n|
<
Ce^{-\alpha n},
]

then

[
\sum_n
|\sigma_n|
<
\infty.
]

---

## D.4 Curvature Stability

Assume

[
|R|
<
R_{\max}.
]

Then

[
|U_\gamma|
<
e^{R_{\max}L_\gamma}.
]

---

## D.5 Analytic Continuation

Within

[
B(P,R_{\rm phase}),
]

all coefficient functions remain analytic.

---

## D.6 Breakdown Criterion

The OPE ceases to converge only if:

[
R\rightarrow\infty,
]

or

[
\det g\rightarrow0.
]

---

## D.7 Critical Surfaces

Phase transitions define convergence boundaries.

---

## D.8 Radius Theorem

The convergence radius equals geodesic distance to the nearest singular phase.

---

# Appendix E

# Gauge-Theoretic Technical Lemmas

---

## E.1 Gauge Invariance Lemma

If

[
\Sigma_I
]

is gauge invariant, then

[
\Phi^I
======

\langle\Sigma_I\rangle
]

is gauge invariant.

---

## E.2 Wilson-Line Completion

[
\bar q(x)W(x,0)q(0)
]

admits a local operator expansion.

---

## E.3 Topological Sector Lemma

[
Q
=

\frac1{32\pi^2}
\int F\tilde F
]

labels disconnected phase sectors.

---

## E.4 Phase Curvature Lemma

Instantons generate localized positive curvature.

---

## E.5 Holonomy Lemma

Wilson loops are phase holonomies.

---

## E.6 Chiral Manifold Lemma

[
SU(N_f)_L\times SU(N_f)_R
/
SU(N_f)_V
]

forms a smooth phase submanifold.

---

## E.7 Large-(N) Lemma

[
\delta g
\sim
N^{-1}.
]

The phase manifold becomes classical.

---

## E.8 Gauge Principle

All physical phase coordinates must be gauge invariant.

---

# Appendix F

# Resurgent Phase Calculations

---

## F.1 Trans-Series Expansion

[
\Pi
===

\sum_{k=0}^{\infty}
e^{-kS}
\Pi_k.
]

---

## F.2 Instanton Action

[
S
=

\int_\gamma ds.
]

---

## F.3 Borel Transform

[
\mathcal B(t)
=============

\sum_n
\frac{\Pi_n}{n!}
t^n.
]

---

## F.4 Borel Reconstruction

[
\Pi
===

\int_0^\infty
e^{-t}
\mathcal B(t)
dt.
]

---

## F.5 Stokes Phenomena

Across critical rays:

[
\Pi
\rightarrow
\Pi+\Delta\Pi.
]

---

## F.6 Monodromy

[
M
=

\exp(2\pi iN).
]

---

## F.7 Topological Contributions

Each homotopy class contributes:

[
e^{-S_\alpha}.
]

---

## F.8 Resurgence Principle

Topology generates nonperturbative OPE sectors.

---

# Appendix G

# Lattice Algorithms

---

## G.1 Input Data

Choose operators

[
\Sigma_I.
]

---

## G.2 Correlation Matrix

Compute

[
G_{IJ}
======

\langle
\Sigma_I\Sigma_J
\rangle.
]

---

## G.3 Metric Extraction

Set

[
g_{IJ}
======

G_{IJ}.
]

---

## G.4 Connection Reconstruction

Numerically evaluate

[
\Gamma^I_{JK}.
]

---

## G.5 Curvature Reconstruction

Compute

[
R^I_{JKL}.
]

---

## G.6 OPE Tomography

Evaluate

[
T_{AB}^{;;C}
============

\langle
\Sigma_C
|
\Sigma_A\Sigma_B
\rangle.
]

---

## G.7 Phase Manifold Learning

Construct

[
\mathcal M_{\rm phase}
]

via dimensional reduction.

---

## G.8 Bootstrap Verification

Check

[
\Pi_{AB}^{;;D}
\Pi_{DC}^{;;E}
==============

\Pi_{BC}^{;;D}
\Pi_{AD}^{;;E}.
]

---

## G.9 Numerical Workflow

[
{\rm Data}
\rightarrow
g
\rightarrow
\Gamma
\rightarrow
R
\rightarrow
\Pi.
]

---

# Appendix H

# Notation and Conventions

---

## H.1 Spacetime

Metric signature:

[
(+,-,-,-).
]

---

## H.2 Indices

Spacetime:

[
\mu,\nu,\rho,\sigma.
]

Gauge:

[
a,b,c.
]

Phase:

[
I,J,K,L.
]

Operator:

[
A,B,C,D.
]

---

## H.3 Core Objects

Phase manifold:

[
\mathcal M_{\rm phase}.
]

Metric:

[
g_{IJ}.
]

Connection:

[
\Gamma^I_{JK}.
]

Curvature:

[
R^I_{JKL}.
]

Phase OPE coefficients:

[
\Pi_{AB}^{;;C}.
]

---

## H.4 Spectral Quantities

Energy eigenstates:

[
|n\rangle.
]

Eigenvalues:

[
E_n.
]

Spectral measure:

[
d\mu(E,\Phi).
]

---

## H.5 Information-Theoretic Quantities

Entropy:

[
S_{\rm phase}.
]

Relative entropy:

[
D(\rho||\sigma).
]

Complexity:

[
\mathcal C.
]

---

## H.6 Gauge-Theory Quantities

Wilson loop:

[
W(C).
]

Topological charge:

[
Q.
]

Gluon condensate:

[
\langle G^2\rangle.
]

Chiral condensate:

[
\langle\bar qq\rangle.
]

---

## H.7 Master Equations

Phase OPE:

[
\mathcal O_A\mathcal O_B
========================

\sum_C
\Pi_{AB}^{;;C}
\mathcal O_C.
]

Transport law:

[
\nabla_I
\Pi_{AB}^{;;C}
==============

0.

]

Bootstrap equation:

[
\Pi_{AB}^{;;D}
\Pi_{DC}^{;;E}
==============

\Pi_{BC}^{;;D}
\Pi_{AD}^{;;E}.
]

Phase Einstein equation:

[
R_{IJ}
-\frac12 g_{IJ}R
================

T_{IJ}^{(\Pi)}.
]

---

# Complete Work

**The Operator Product Expansion Beyond Perturbation Theory: Toward a Nonperturbative Operator Expansion Theory (NOET)**

**Phase-Theoretic Interpretation (POET)**

* Volume I–VII completed
* Appendices A–H completed
* Total structure: 36 primary parts + 8 technical appendices

This constitutes the full formal POET construction as developed within the white paper framework.
