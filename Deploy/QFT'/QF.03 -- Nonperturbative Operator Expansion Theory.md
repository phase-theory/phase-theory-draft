# The Operator Product Expansion Beyond Perturbation Theory

## Volume III — Nonperturbative Operator Expansion Theory (NOET)

### Parts 11–15

---

# 11. Operator-State Geometry

## 11.1 Motivation

The central premise of NOET is that the conventional OPE is attempting to describe a deeper geometric structure.

Standard formulations treat local operators as algebraic objects.

However, every local operator simultaneously defines a family of states:

[
|A\rangle
=========

\mathcal O_A(0)|0\rangle.
]

The collection of such states forms a geometric manifold embedded within the full Hilbert space.

The OPE will be reinterpreted as a local geometric projection law on this manifold.

---

## 11.2 Operator-State Correspondence Beyond CFT

In conformal theories,

[
\mathcal O_A
\leftrightarrow
|A\rangle.
]

NOET postulates that a generalized correspondence exists even without conformal symmetry.

Define

[
\mathcal S
==========

{
\mathcal O_A|0\rangle
}.
]

This set forms the **operator-state manifold**.

Unlike CFT, the manifold is generally curved.

Its geometry encodes:

* mass gaps,
* confinement,
* spontaneous symmetry breaking,
* topological sectors.

---

## 11.3 Metric Structure

Introduce

[
G_{AB}
======

\langle0|
\mathcal O_A^\dagger
\mathcal O_B
|0\rangle.
]

This defines a positive semidefinite metric.

The induced line element becomes

[
ds^2
====

G_{AB}
d\phi^A
d\phi^B.
]

Operator space therefore acquires intrinsic geometry.

---

## 11.4 Operator Connections

Under renormalization,

[
\mathcal O_A
\rightarrow
Z_A^{;B}\mathcal O_B.
]

Define

[
\Gamma_A^{;B}
=============

(Z^{-1}dZ)_A^{;B}.
]

This acts as a connection on operator space.

The renormalization group becomes parallel transport.

---

## 11.5 Curvature

The curvature tensor is

[
R_A^{;B}
========

d\Gamma_A^{;B}
+
\Gamma_A^{;C}
\wedge
\Gamma_C^{;B}.
]

NOET interprets nonzero curvature as an obstruction to exact finite-dimensional closure of the OPE.

Flat operator geometry corresponds to CFT-like exact closure.

Curved geometry corresponds to strongly coupled theories.

---

## 11.6 Geometric OPE Principle

Let

[
P_x:
\mathfrak O_x\otimes\mathfrak O_x
\rightarrow
\mathfrak O_x
]

denote the local projection operator.

Then

[
\mathcal O_A(x)\mathcal O_B(0)
==============================

P_x(\mathcal O_A\otimes\mathcal O_B).
]

The OPE becomes a geometric projection law rather than merely a perturbative expansion.

---

# 12. Local Operator Banach and Hilbert Structures

## 12.1 Need for Functional Analysis

The OPE contains infinitely many operators.

A rigorous nonperturbative framework requires completion of operator space.

The finite linear span

[
\mathfrak O
===========

\mathrm{span}
{\mathcal O_A}
]

must therefore be enlarged.

---

## 12.2 Operator Norm

Define

[
|\mathcal O|
============

\sup_{\psi}
\frac{|\mathcal O\psi|}
{|\psi|}.
]

The completion yields a Banach space

[
\mathcal B_O.
]

This becomes the fundamental space of local observables.

---

## 12.3 Hilbert Completion

Using the vacuum metric,

[
(\mathcal O_A,\mathcal O_B)
===========================

\langle0|
\mathcal O_A^\dagger
\mathcal O_B
|0\rangle,
]

construct

[
\mathcal H_O.
]

We call this the **operator Hilbert space**.

---

## 12.4 Nuclearity Hypothesis

### Postulate NOET-1

For every bounded spacetime region,

[
\mathcal H_O(\Omega)
]

is nuclear.

Consequently:

[
\sum_n
\lambda_n
<
\infty
]

for the singular values of compact operator maps.

This condition guarantees controllable infinite-dimensional expansions.

---

## 12.5 Compactness of Local Products

Consider

[
M:
\mathcal H_O\otimes\mathcal H_O
\rightarrow
\mathcal H_O.
]

NOET assumes:

### Postulate NOET-2

(M) is compact.

Therefore a singular-value decomposition exists:

[
M
=

\sum_n
\sigma_n
|u_n\rangle\langle v_n|.
]

The OPE becomes a spectral decomposition of a compact map.

---

## 12.6 Consequence

Compactness implies a discrete spectrum.

Thus local operator multiplication admits a countable decomposition:

[
\mathcal O_A\mathcal O_B
========================

\sum_n
\sigma_n
\Phi_n.
]

This becomes the starting point for nonperturbative convergence analysis.

---

# 13. Spectral Resolution of Operator Products

## 13.1 Fundamental Principle

The exact theory is characterized by

[
H|n\rangle
==========

E_n|n\rangle.
]

Instead of expanding in coupling constants, NOET expands in energy eigenstates.

---

## 13.2 Spectral Kernel

Insert completeness:

[
\mathbf1
========

\sum_n
|n\rangle\langle n|.
]

Then

[
\mathcal O_A(x)\mathcal O_B(0)
==============================

\sum_n
\mathcal O_A(x)|n\rangle
\langle n|\mathcal O_B(0).
]

Define

[
K_{AB}^{(n)}(x)
===============

\mathcal O_A(x)|n\rangle
\langle n|\mathcal O_B(0).
]

These are exact spectral kernels.

---

## 13.3 Projection onto Local Operators

Let

[
\Pi_C
]

project onto the operator basis element (\mathcal O_C).

Then

[
C_{AB}^{;;C}(x)
===============

\sum_n
\mathrm{Tr}
\Big[
\Pi_C
K_{AB}^{(n)}(x)
\Big].
]

This equation is the first nonperturbative candidate for OPE coefficients.

No Feynman diagrams appear.

---

## 13.4 Spectral OPE Formula

The proposed exact expansion becomes

[
\boxed{
\mathcal O_A(x)\mathcal O_B(0)
==============================

\sum_C
\left(
\sum_n
\Xi_{AB,n}^{;;;;C}
e^{-E_n|x|}
\right)
\mathcal O_C(0)
}
]

where

[
\Xi_{AB,n}^{;;;;C}
]

are operator-state overlaps.

The coefficient functions are therefore Laplace transforms of spectral data.

---

## 13.5 Interpretation

The OPE coefficients are not fundamental.

They emerge from:

1. the exact spectrum,
2. operator-state overlaps,
3. local projection geometry.

Thus the spectral problem replaces the perturbative problem.

---

## 13.6 First Spectral Convergence Criterion

If

[
\rho(E)
]

is the density of states and

[
|\Xi(E)|
<
e^{-\alpha E},
]

then

[
\int dE,
\rho(E)
e^{-E|x|}
\Xi(E)
]

converges.

Therefore OPE convergence reduces to a spectral-growth condition.

---

# 14. Dynamical Condensate Fields

## 14.1 The Condensate Problem

In conventional QCD,

[
\langle\bar qq\rangle,
\qquad
\langle G^2\rangle
]

enter as external inputs.

This is conceptually unsatisfactory.

A complete OPE should generate them internally.

---

## 14.2 Condensates as Collective Coordinates

NOET introduces condensate fields

[
\Sigma_i(x).
]

Examples:

[
\Sigma_q
========

\bar qq,
]

[
\Sigma_G
========

G_{\mu\nu}^aG^{a\mu\nu}.
]

These are promoted from expectation values to dynamical geometric coordinates.

---

## 14.3 Effective Condensate Manifold

Define

[
\mathcal M_{\rm cond}
=====================

{\Sigma_i}.
]

The vacuum corresponds to a point

[
\Sigma_i^{(0)}.
]

Fluctuations become

[
\delta\Sigma_i.
]

The vacuum itself becomes a dynamical geometric object.

---

## 14.4 Condensate Action

Introduce

[
S_{\rm cond}
============

\int d^4x
\left[
\frac12
G_{ij}
\partial_\mu\Sigma_i
\partial^\mu\Sigma_j
--------------------

V(\Sigma)
\right].
]

The vacuum is determined through

[
\frac{\delta S_{\rm cond}}
{\delta\Sigma_i}
================

0.

]

Thus condensates emerge from equations of motion.

---

## 14.5 Condensates in the OPE

The expansion becomes

[
\mathcal O_A(x)\mathcal O_B(0)
==============================

\sum_C
C_{AB}^{;;C}(x,\Sigma)
\mathcal O_C(0).
]

The coefficients now depend on dynamical condensate coordinates.

---

## 14.6 Self-Consistency Condition

Vacuum expectation values satisfy

[
\Sigma_i
========

\langle
\Sigma_i
\rangle.
]

Together with spectral equations, this generates a closed system.

The condensates are no longer external phenomenological parameters.

---

# 15. Nonperturbative OPE Hypothesis

## 15.1 Statement

The central postulate of NOET is:

### NOET-3

For every local QFT possessing:

1. a separable Hilbert space,
2. a local operator algebra,
3. a bounded-below Hamiltonian,

there exists a spectral operator expansion

[
\mathcal O_A(x)\mathcal O_B(0)
==============================

\sum_C
\mathcal C_{AB}^{;;C}(x)
\mathcal O_C(0),
]

where

[
\mathcal C_{AB}^{;;C}
]

is determined entirely by exact spectral data.

---

## 15.2 Spectral Construction

The coefficients satisfy

[
\boxed{
\mathcal C_{AB}^{;;C}(x)
========================

\sum_n
\Xi_{AB,n}^{;;;;C}
e^{-E_n|x|}
}
]

with

[
\Xi_{AB,n}^{;;;;C}
==================

\langle0|
\mathcal O_C^\dagger
|n\rangle
\langle n|
\mathcal O_A\mathcal O_B
|0\rangle.
]

---

## 15.3 Recovery of Perturbation Theory

If

[
g\ll1,
]

the spectrum becomes approximately free:

[
E_n
===

E_n^{(0)}
+
O(g).
]

Expanding the spectral coefficients reproduces the conventional perturbative OPE.

Thus perturbation theory emerges as a limiting approximation.

---

## 15.4 Recovery of Conformal OPE

For scale-invariant spectra,

[
E_n
\propto
\Delta_n,
]

the spectral kernels reduce to conformal blocks.

The exact CFT OPE is recovered.

---

## 15.5 Strong-Coupling Regime

For

[
g\sim1,
]

the spectral formula remains meaningful.

Confinement modifies:

[
E_n.
]

Chiral symmetry breaking modifies:

[
\Xi_{AB,n}^{;;;;C}.
]

The OPE survives without reference to Feynman diagrams.

---

## 15.6 Roadmap to Volume IV

The NOET framework is now defined.

The remaining task is mathematical.

We must establish:

1. existence,
2. convergence,
3. radius of validity,
4. uniqueness,
5. renormalization consistency.

Volume IV develops these results through:

* Spectral Construction of OPE Coefficients
* Convergence Theorems
* Radius of Convergence and Analytic Domains
* Resurgent Structure
* Renormalization Group Completion
* Nonperturbative Bootstrap Equations

which together form the mathematical core of Nonperturbative Operator Expansion Theory.
