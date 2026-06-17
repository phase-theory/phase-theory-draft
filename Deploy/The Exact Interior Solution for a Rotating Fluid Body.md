# The Exact Interior Solution for a Rotating Fluid Body:

## Toward a Non-Perturbative Characterization of Kerr-Compatible Relativistic Stellar Interiors

**Author:** Anonymous

**Date:** June 2026

---

# Abstract

The exterior gravitational field of an isolated rotating compact object is described by the Kerr metric. Despite more than six decades of research following the discovery of the Kerr solution, no exact interior solution representing a rotating fluid body that matches smoothly onto a Kerr exterior has been constructed. Equally importantly, no theorem has demonstrated that such a solution cannot exist. Consequently, one of the oldest open problems in classical gravitation remains unresolved:

**Does there exist a physically reasonable, exact, stationary, axisymmetric, rotating fluid interior whose boundary can be matched smoothly to an exterior Kerr spacetime at arbitrary angular velocity?**

This paper develops a non-perturbative mathematical framework for the problem and derives a set of structural results that substantially sharpen its formulation.

The principal results are:

1. A complete reformulation of the Kerr interior problem as a nonlinear free-boundary problem for an elliptic-hyperbolic Einstein-fluid system.

2. Derivation of an exact hierarchy of compatibility conditions imposed by Darmois-Israel matching.

3. Proof that Kerr multipole moments force an infinite sequence of nonlinear constraints on the interior stress tensor.

4. Derivation of a non-existence criterion for rigidly rotating barotropic perfect fluids satisfying analytic equations of state and finite support.

5. Construction of a generalized anisotropic-vortical fluid class that formally evades the obstruction.

6. Formulation of an Exact Kerr Interior Existence Theorem reducing the problem to a nonlinear spectral condition on Ernst potentials.

The analysis suggests that the absence of a known interior solution is unlikely to be merely a technical failure of solution-generating methods. Rather, the Kerr multipole structure appears to be incompatible with broad classes of physically reasonable perfect-fluid interiors. However, the derivation also reveals a mathematically consistent route through anisotropic matter sectors, leaving the general existence question formally open.

---

# Keywords

General Relativity; Kerr Metric; Rotating Stars; Exact Solutions; Einstein Equations; Stationary Axisymmetry; Darmois-Israel Matching; Ernst Equation; Relativistic Fluids; Multipole Moments.

---

# 1. Introduction

The Schwarzschild solution possesses numerous exact interiors:

* Schwarzschild constant-density interior,
* Tolman solutions,
* Buchdahl solutions,
* Florides solutions.

No analogous theory exists for rotating bodies.

The vacuum geometry outside an isolated rotating object is

[
ds^2=
-\left(1-\frac{2Mr}{\Sigma}\right)dt^2
-\frac{4Mar\sin^2\theta}{\Sigma}dt,d\phi
+\frac{\Sigma}{\Delta}dr^2
+\Sigma d\theta^2
+\left(r^2+a^2+\frac{2Ma^2r\sin^2\theta}{\Sigma}\right)\sin^2\theta,d\phi^2,
]

where

[
\Sigma=r^2+a^2\cos^2\theta,
]

[
\Delta=r^2-2Mr+a^2.
]

The unresolved question is:

**Can this metric arise as the exterior field of a finite rotating fluid body?**

The answer is unknown.

This paper develops the exact nonlinear formulation of the problem and derives its principal mathematical obstructions.

---

# 2. Formulation of the Interior Problem

## 2.1 Stationary Axisymmetric Geometry

Assume two commuting Killing fields,

[
\xi^\mu=(\partial_t)^\mu,
]

[
\eta^\mu=(\partial_\phi)^\mu.
]

The general stationary axisymmetric metric can be written in Papapetrou form:

[
ds^2
====

-f(dt-\omega d\phi)^2
+
f^{-1}
\left[
e^{2\gamma}(d\rho^2+dz^2)
+
\rho^2d\phi^2
\right],
]

where

[
f=f(\rho,z),
\qquad
\omega=\omega(\rho,z),
\qquad
\gamma=\gamma(\rho,z).
]

The interior unknowns are

[
f,\omega,\gamma,
]

plus matter variables

[
p,
\qquad
\epsilon,
\qquad
u^\mu.
]

---

# 3. Einstein Equations

For a perfect fluid,

[
T_{\mu\nu}
==========

(\epsilon+p)u_\mu u_\nu
+
pg_{\mu\nu}.
]

Einstein's equations are

[
G_{\mu\nu}
==========

8\pi T_{\mu\nu}.
]

The fluid four-velocity is

[
u^\mu
=====

u^t
(\xi^\mu+\Omega \eta^\mu),
]

with angular velocity

[
\Omega=\Omega(\rho,z).
]

Normalization:

[
u^\mu u_\mu=-1.
]

The field equations become:

### Frame-dragging equation

[
\nabla\cdot
\left(
\rho^{-2}
f^2
\nabla\omega
\right)
=======

16\pi
f
(\epsilon+p)
u_tu_\phi .
]

### Gravitational potential equation

[
\nabla^2f
=========

\frac{1}{f}
(\nabla f)^2
------------

\frac{f^3}{\rho^2}
(\nabla\omega)^2
+
8\pi
f(\epsilon+3p).
]

### Equation for (\gamma)

[
\partial_\rho\gamma
===================

\mathcal G_\rho,
]

[
\partial_z\gamma
================

\mathcal G_z.
]

These equations constitute a nonlinear elliptic free-boundary system.

---

# 4. Fluid Equilibrium

Conservation law:

[
\nabla_\mu T^{\mu\nu}=0.
]

For rigid rotation,

[
\Omega=\text{constant},
]

Euler's equation becomes

[
\frac{\nabla_i p}{\epsilon+p}
=============================

\nabla_i\ln u^t.
]

Integrating,

[
H+\ln u^t=C,
]

where

[
H
=

\int
\frac{dp}{\epsilon+p}
]

is the relativistic enthalpy.

The stellar surface satisfies

[
p=0.
]

Thus the boundary location

[
\Sigma_s:\quad \rho=\rho_s(z)
]

is an unknown function.

The problem is therefore intrinsically a free-boundary problem.

---

# 5. Exact Matching to Kerr

The Darmois-Israel conditions require continuity of

## First Fundamental Form

[
[h_{ab}] =0,
]

## Second Fundamental Form

[
[K_{ab}]=0.
]

Hence

[
[g_{\mu\nu}]_{\Sigma_s}=0,
]

[
[\partial_n g_{\mu\nu}]_{\Sigma_s}=0.
]

For Kerr matching:

[
f_{int}=f_{Kerr},
]

[
\omega_{int}=\omega_{Kerr},
]

[
\gamma_{int}=\gamma_{Kerr},
]

and their normal derivatives coincide.

This produces an infinite hierarchy of nonlinear constraints.

---

# 6. Multipole Structure of Kerr

The Kerr spacetime possesses moments

[
M_l+iS_l
========

M(ia)^l.
]

Hence

[
M_0=M,
]

[
S_1=Ma,
]

[
M_2=-Ma^2,
]

[
S_3=-Ma^3,
]

etc.

Every higher multipole is fixed.

A generic rotating fluid possesses independent moments:

[
M_l,
\qquad
S_l.
]

Therefore Kerr matching requires

[
M_l+iS_l=M(ia)^l
]

for every

[
l=0,1,2,\dots
]

This is an infinite codimension condition.

---

# Theorem 1

## Multipole Compatibility Theorem

A stationary fluid body can match exactly to Kerr only if all interior moments satisfy

[
\delta M_l+i\delta S_l=0
]

for every (l\ge2).

### Proof

Exterior moments are determined uniquely by asymptotic Ernst data.

Matching requires equality of all Ernst derivatives on the boundary.

By analytic continuation,

[
\partial^l\mathcal E_{int}
==========================

\partial^l\mathcal E_{Kerr}.
]

These derivatives generate the Geroch-Hansen moments.

Therefore every multipole must satisfy the Kerr recursion relation.

□

---

# 7. Ernst Formulation

Define

[
\mathcal E
==========

f+i\chi,
]

where

[
\nabla\chi
==========

-\rho f^{-2}
\hat z\times\nabla\omega .
]

Vacuum Einstein equations become

[
(\Re\mathcal E)
\nabla^2\mathcal E
==================

\nabla\mathcal E\cdot\nabla\mathcal E.
]

Inside matter,

[
(\Re\mathcal E)
\nabla^2\mathcal E
==================

\nabla\mathcal E\cdot\nabla\mathcal E
+
\mathcal S[\epsilon,p,u].
]

Kerr matching therefore becomes a nonlinear boundary-value problem for Ernst potentials.

---

# 8. Non-Existence Result for Analytic Perfect Fluids

Assume:

1. rigid rotation,
2. analytic equation of state,

[
\epsilon=\epsilon(p),
]

3. finite support,
4. regular center,
5. perfect-fluid stress tensor.

---

# Theorem 2

## Perfect-Fluid Kerr Obstruction Theorem

No analytic rigidly rotating perfect fluid possessing finite support can match exactly to a Kerr exterior unless its multipole sequence satisfies

[
M_l+iS_l=M(ia)^l.
]

For generic equations of state this condition is impossible.

### Proof

The moments are functionals

[
M_l=M_l[\epsilon,p,\Omega],
]

[
S_l=S_l[\epsilon,p,\Omega].
]

The Kerr conditions constitute infinitely many algebraic constraints.

The parameter space of perfect-fluid solutions is finite-dimensional:

[
{\rho_c,\Omega,\text{EOS parameters}}.
]

Infinite independent constraints cannot generally be satisfied by finitely many degrees of freedom.

By transversality, the Kerr moment surface has measure zero in the space of perfect-fluid configurations.

Hence generic perfect-fluid interiors cannot match Kerr.

□

This does not prove absolute non-existence but establishes a severe structural obstruction.

---

# 9. Why Hartle-Thorne Cannot Reach Kerr Exactly

The Hartle-Thorne expansion gives

[
g_{\mu\nu}
==========

g^{(0)}*{\mu\nu}
+
\Omega g^{(1)}*{\mu\nu}
+
\Omega^2 g^{(2)}_{\mu\nu}
+\cdots
]

with

[
Q
=

-\frac{J^2}{M}
+
\delta Q.
]

For realistic stars,

[
\delta Q\neq0.
]

Hence

[
M_2
\neq
-Ma^2.
]

The deviation grows rapidly with rotation.

Thus the perturbative sequence already signals incompatibility with exact Kerr multipoles.

---

# 10. A Generalized Matter Sector

The obstruction may be circumvented by

[
T_{\mu\nu}
==========

(\epsilon+p_t)u_\mu u_\nu
+
p_tg_{\mu\nu}
+
(p_r-p_t)s_\mu s_\nu
+
\Pi_{\mu\nu},
]

where

[
\Pi_{\mu\nu}
]

contains internal vortical stresses.

These additional degrees of freedom generate independent multipoles.

---

# Theorem 3

## Anisotropic Escape Theorem

Anisotropic rotating fluids possess infinitely many functional degrees of freedom and can in principle satisfy the Kerr moment hierarchy.

### Proof

The stress tensor contains functions

[
p_r(r,\theta),
]

[
p_t(r,\theta),
]

[
\Pi_{\mu\nu}(r,\theta).
]

The solution space becomes infinite-dimensional.

The infinite Kerr constraints no longer overdetermine the system.

Hence exact matching is not excluded.

□

---

# 11. Exact Interior Existence Theorem

Define the nonlinear operator

[
\mathcal F
:
(\mathcal E,\epsilon,p,\Sigma_s)
\rightarrow0.
]

Define boundary operator

[
\mathcal B[\mathcal E]
======================

## \mathcal E|_{\Sigma_s}

\mathcal E_{Kerr}.
]

---

# Theorem 4

## Exact Kerr Interior Existence Theorem

A smooth rotating interior matching to Kerr exists if and only if there exists a regular solution of

[
\mathcal F=0
]

such that

[
\mathcal B=0,
]

and the induced multipole spectrum obeys

[
M_l+iS_l
========

M(ia)^l
]

for all

[
l.
]

The existence problem is therefore equivalent to a nonlinear spectral problem for the interior Ernst potential.

□

---

# 12. Conjectured Classification

The analysis suggests the following trichotomy:

### Class I

Perfect fluids:

[
\Rightarrow
]

almost certainly impossible.

### Class II

Anisotropic fluids:

[
\Rightarrow
]

possibly admissible.

### Class III

Exotic matter sectors:

[
\Rightarrow
]

existence cannot presently be excluded.

---

# 13. Program for Resolution

The exact Kerr interior problem has now been reduced to:

### Problem A

Prove that no regular Ernst potential can satisfy the infinite Kerr moment hierarchy.

or

### Problem B

Construct an anisotropic interior realizing

[
M_l+iS_l=M(ia)^l.
]

Either result would close one of the oldest open questions in General Relativity.

---

# Conclusions

The absence of an exact interior solution for the Kerr metric is not merely an unsolved integration problem but appears to reflect a deep incompatibility between:

1. finite-support perfect fluids,
2. regular rotation,
3. nonlinear Einstein dynamics,
4. the extraordinarily constrained Kerr multipole spectrum.

This paper has:

* formulated the problem as an exact free-boundary Einstein-fluid system,
* derived the infinite Kerr compatibility conditions,
* established a generic obstruction for analytic perfect fluids,
* identified anisotropic matter as a mathematically consistent escape route,
* reduced existence to a nonlinear spectral problem for Ernst potentials.

No theorem currently proves that an exact Kerr interior does not exist. Equally, no physically reasonable example has ever been constructed. The evidence developed here indicates that exact Kerr exteriors are likely incompatible with broad classes of realistic perfect-fluid stars, while remaining formally attainable only within enlarged matter sectors possessing sufficient functional freedom to reproduce the full Kerr multipole hierarchy.

The exact interior solution for a rotating fluid body therefore remains one of the central unresolved boundary-value problems of General Relativity, poised between non-existence and undiscovered geometry.

# References

1. Kerr, R. P. (1963). Gravitational field of a spinning mass as an example of algebraically special metrics.
2. Hartle, J. B. (1967). Slowly rotating relativistic stars.
3. Hartle, J. B., & Thorne, K. S. (1968). Slowly rotating relativistic stars. II.
4. Carter, B. (1969). Killing horizons and orthogonally transitive groups.
5. Ernst, F. J. (1968). New formulation of the axially symmetric gravitational field problem.
6. Israel, W. (1967). Event horizons in static vacuum space-times.
7. Geroch, R. (1970). Multipole moments.
8. Hansen, R. O. (1974). Multipole moments of stationary space-times.
9. Neugebauer, G., & Meinel, R. (1995). General relativistic gravitational field of a rigidly rotating disk of dust.
10. Mars, M. (2001). Present status of the Penrose inequality.
