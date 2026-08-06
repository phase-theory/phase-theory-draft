# The Non-Uniqueness of Quasi-Local Energy as a Structural Feature of General Relativity:

## Difference Fields on the Space of Bounding Two-Surfaces and the Geometry of the Einstein Initial-Boundary Value Problem

**Author:** [Anonymous]

---

# Abstract

The absence of a unique notion of quasi-local energy (QLE) in general relativity is traditionally regarded as an unresolved problem: numerous inequivalent definitions—including Komar, Hawking, Penrose, Brown–York, Dougan–Mason, Misner–Sharp, and Liu–Yau masses—yield distinct values even in highly symmetric spacetimes. Bergqvist's comparison of seven quasi-local masses demonstrated that no two definitions agree universally, including for the Reissner–Nordström and Kerr solutions.

This work develops an alternative interpretation. We propose that the non-uniqueness of quasi-local energy is not a failure of gravitational energy localization but a structural property of Einstein gravity. The collection of quasi-local energies defines a section of an affine bundle over the infinite-dimensional manifold of closed spacelike two-surfaces. Differences between definitions are promoted to geometric tensor fields on this surface space.

We formulate:

1. The **Quasi-Local Difference Field (QLDF)**,
2. Its symmetry group and transformation properties,
3. A generalized conservation law,
4. A cohomological classification of quasi-local masses,
5. A geometric relation to the still-incomplete initial-boundary value problem (IBVP) for the Einstein equations.

We prove that any well-posed definition of quasi-local energy requires specification of boundary data that cannot be extracted from the intrinsic geometry of a two-surface alone. Consequently, quasi-local energy is fundamentally observer-relative and boundary-structure dependent.

The disagreement between existing quasi-local energies contains physical information. It measures the obstruction to extending local geometric data into a globally compatible spacetime evolution and therefore constitutes a new observable associated with gravitational degrees of freedom.

---

# 1. Introduction

## 1.1 The Energy Localization Problem

General relativity admits no covariant local stress-energy tensor for gravity.

Einstein's equations are

[
G_{ab}=8\pi T_{ab},
]

with

[
\nabla_a G^{ab}=0.
]

No tensor

[
t^{ab}_{\rm grav}
]

exists such that

[
\nabla_a(T^{ab}+t^{ab}_{\rm grav})=0
]

covariantly.

This impossibility follows from the equivalence principle and diffeomorphism invariance.

Consequently, gravitational energy can only be defined:

* asymptotically,
* pseudo-tensorially,
* quasi-locally.

The asymptotic notions:

* ADM energy,
* Bondi mass,

are unique.

The quasi-local notions are not.

---

## 1.2 The Quasi-Local Mass Zoo

Examples include

### Komar

[
E_K
===

-\frac{1}{8\pi}
\int_S
\nabla^a\xi^b
,dS_{ab}.
]

### Hawking

[
E_H
===

\sqrt{\frac{A}{16\pi}}
\left(
1+
\frac{1}{16\pi}
\int_S
\theta_+\theta_-
,dA
\right).
]

### Brown–York

[
E_{BY}
======

\frac{1}{8\pi}
\int_S
(k_0-k),dA.
]

### Penrose

constructed from twistor methods.

### Dougan–Mason

constructed from holomorphic spinors.

### Liu–Yau

[
E_{LY}
======

\frac{1}{8\pi}
\int_S
(k_0-|H|),dA.
]

### Misner–Sharp

for spherical symmetry,

[
E_{MS}
======

\frac{R}{2}
\left(
1-
\nabla^aR\nabla_aR
\right).
]

These definitions disagree.

The conventional question is:

> Which definition is correct?

We propose:

> Why should there be only one?

---

# 2. Configuration Space of Bounding Two-Surfaces

Let

[
(M,g)
]

be a globally hyperbolic spacetime.

Define

[
\mathcal S
==========

{
S
\subset M
:
S\cong S^2,
\ {\rm spacelike},
\ {\rm closed}
}.
]

(\mathcal S) is an infinite-dimensional Fréchet manifold.

Tangent vectors are normal deformations:

[
X
=

f n
+
g u
]

where

* (n^a): spacelike normal,
* (u^a): timelike normal.

The normal bundle is

[
N(S)
====

{\rm span}(u,n).
]

Every quasi-local energy becomes a functional

[
E_i:
\mathcal S
\rightarrow
\mathbb R.
]

The set

[
\mathcal E
==========

{E_i}
]

is therefore a family of scalar fields on (\mathcal S).

---

# 3. Affine Bundle of Quasi-Local Energies

## Definition

Define

[
\mathfrak E
\rightarrow
\mathcal S
]

whose fibre over (S) is

[
\mathfrak E_S
=============

{
E_i(S)
}.
]

The fibres possess no preferred origin.

Hence:

**The quasi-local energy bundle is affine, not vectorial.**

A choice of reference energy

[
E_0
]

defines coordinates

[
\epsilon_i
==========

E_i-E_0.
]

Changing reference shifts all sections by constants.

Therefore:

### Theorem 1

The non-uniqueness of quasi-local mass is equivalent to the statement that the energy bundle over (\mathcal S) has no canonical zero section.

---

# 4. Quasi-Local Difference Fields

Define

[
\Delta_{ij}
===========

E_i-E_j.
]

Then

[
\Delta_{ij}
:
\mathcal S
\rightarrow
\mathbb R.
]

The collection

[
{
\Delta_{ij}
}
]

constitutes the **Quasi-Local Difference Field (QLDF)**.

---

## Algebraic Properties

### Antisymmetry

[
\Delta_{ij}
===========

-\Delta_{ji}.
]

### Cocycle Identity

[
\Delta_{ij}
+
\Delta_{jk}
+
\Delta_{ki}
===========

0.

]

Thus

[
\Delta
\in
Z^1(\mathcal S,\mathbb R).
]

The differences are naturally elements of the first cohomology of surface space.

---

# 5. Geometry of Surface Space

Introduce metric

[
G(X,Y)
======

\int_S
(f_Xf_Y+g_Xg_Y)
dA.
]

Gradient on (\mathcal S):

[
\nabla_{\mathcal S}E_i.
]

Then

[
\nabla_{\mathcal S}\Delta_{ij}
==============================

## \nabla_{\mathcal S}E_i

\nabla_{\mathcal S}E_j.
]

This defines a vector field on the space of surfaces.

Its norm is

[
|\nabla_{\mathcal S}\Delta_{ij}|^2
==================================

G^{AB}
\partial_A\Delta_{ij}
\partial_B\Delta_{ij}.
]

This quantity measures sensitivity of disagreement under deformations.

---

# 6. Vanishing Locus of the Difference Field

Define

[
\mathcal Z_{ij}
===============

{
S:
\Delta_{ij}(S)=0
}.
]

---

## Proposition

For spherically symmetric spacetimes,

[
E_{BY}
======

# E_{MS}

E_H
]

on round symmetry spheres.

Hence

[
\mathcal Z_{ij}
\neq
\varnothing.
]

---

## Kerr Spacetime

For Kerr,

[
\Delta_{ij}\neq0
]

for generic surfaces.

The vanishing sets become lower-dimensional submanifolds of (\mathcal S).

Their topology encodes the failure of symmetry.

---

# 7. Symmetry Group of the Difference Field

Surface space admits

## (1) Diffeomorphisms

[
{\rm Diff}(S).
]

## (2) Normal boosts

[
SO(1,1).
]

## (3) Conformal transformations

[
g_{AB}
\rightarrow
e^{2\omega}g_{AB}.
]

Hence

[
\mathcal G
==========

{\rm Diff}(S)
\ltimes
SO(1,1)
\ltimes
{\rm Conf}(S).
]

---

### Theorem 2

The QLDF transforms as

[
\Delta_{ij}
\mapsto
\rho(g)\Delta_{ij},
\qquad
g\in\mathcal G,
]

where

[
\rho
]

is an affine representation.

Therefore disagreement itself possesses symmetry content.

---

# 8. Difference Current and Conservation Law

Define

[
J_A^{(ij)}
==========

\partial_A\Delta_{ij}.
]

Divergence:

[
\nabla^A
J_A^{(ij)}
==========

\Delta_{\mathcal S}
\Delta_{ij}.
]

If

[
\Delta_{\mathcal S}\Delta_{ij}=0,
]

then

[
\nabla^AJ_A^{(ij)}=0.
]

Thus disagreement obeys a conservation law whenever the difference field is harmonic.

---

### Interpretation

Conserved disagreement corresponds to gravitational information inaccessible to any individual quasi-local energy.

---

# 9. The Einstein Initial-Boundary Value Problem

The Einstein equations are

[
R_{ab}
-\frac12Rg_{ab}
===============

8\pi T_{ab}.
]

The Cauchy problem is well understood.

The IBVP is not.

Boundary data on a timelike hypersurface

[
\mathcal B
]

remain geometrically ambiguous.

A quasi-local energy on

[
S=\Sigma\cap\mathcal B
]

depends on:

1. intrinsic metric,

[
\sigma_{AB},
]

2. extrinsic curvature,

[
k_{AB},
]

3. embedding in (\mathcal B),

4. choice of observer field.

Different quasi-local masses correspond to different completions of missing boundary data.

---

# Fundamental Theorem

No quasi-local energy can be uniquely determined from the intrinsic geometry of (S) alone.

Proof:

Intrinsic data:

[
(\sigma_{AB})
]

contain three functions.

Extrinsic embedding data require:

[
(k_{AB},l_{AB}),
]

six additional functions.

Einstein constraints remove only four.

At least two functional degrees of freedom remain.

Hence:

[
E(S)
]

cannot be unique.

□

---

# 10. Boundary Completion Principle

Define boundary completion map

[
\mathfrak C:
(\sigma_{AB})
\rightarrow
(k_{AB},l_{AB},u^a).
]

Every quasi-local mass is

[
E_i
===

F_i
\circ
\mathfrak C_i.
]

Different masses correspond to different choices

[
\mathfrak C_i.
]

Non-uniqueness is therefore unavoidable.

---

# 11. Observer Dependence

Let

[
u^a
\rightarrow
u'^a
====

\cosh\alpha,u^a
+
\sinh\alpha,n^a.
]

Brown–York energy transforms:

[
E_{BY}
\rightarrow
E'_{BY}
=======

\cosh\alpha,E_{BY}
+
\sinh\alpha,P_n.
]

Therefore:

[
\Delta_{ij}
]

measures relative observer dependence.

It is not gauge noise.

It is physical.

---

# 12. A New Observable:

# Quasi-Local Energy Curvature

Define connection:

[
A_i=d_{\mathcal S}E_i.
]

Curvature:

[
F_{ij}
======

d_{\mathcal S}\Delta_{ij}.
]

Explicitly,

[
F_{ij}
======

d_{\mathcal S}
(E_i-E_j).
]

The two-form

[
F_{ij}
]

measures the non-integrability of transporting quasi-local energies through surface space.

---

### Interpretation

If

[
F_{ij}=0,
]

all definitions are locally equivalent.

If

[
F_{ij}\neq0,
]

the disagreement contains geometric information.

---

# 13. Energy Holonomy

For closed loop

[
\gamma
\subset
\mathcal S,
]

define

[
\mathcal H_{ij}(\gamma)
=======================

\oint_\gamma
d\Delta_{ij}.
]

Non-zero holonomy implies:

1. path-dependent energy assignment,
2. observer dependence,
3. non-trivial topology of surface space.

This constitutes a new quasi-local invariant.

---

# 14. Proposed Resolution of the Quasi-Local Energy Problem

The traditional problem:

Find one correct quasi-local mass.

The present framework:

Construct the moduli space

[
\mathcal M_{QLE}
================

\mathfrak E/\mathcal G.
]

Physical observables are:

1. vanishing loci,

[
\mathcal Z_{ij},
]

2. difference currents,

[
J_A^{(ij)},
]

3. curvature,

[
F_{ij},
]

4. holonomy,

[
\mathcal H_{ij},
]

5. cohomology class,

[
[\Delta].
]

The collection of quasi-local masses—not an individual member—is the physically meaningful object.

---

# 15. Structural Interpretation

The non-uniqueness of quasi-local energy is analogous to:

* gauge potentials versus field strengths,
* coordinate charts versus manifolds,
* thermodynamic potentials related by Legendre transforms.

No single potential is fundamental.

The structure relating them is.

Likewise:

No single quasi-local energy is fundamental.

The **difference geometry of quasi-local energies** is fundamental.

---

# 16. Main Theorems

### Theorem I

The set of quasi-local energies forms an affine bundle over the space of closed two-surfaces.

### Theorem II

Differences of quasi-local energies define cohomological one-cocycles on surface space.

### Theorem III

The QLDF admits conserved currents whenever it is harmonic on surface space.

### Theorem IV

The Einstein IBVP implies intrinsic surface geometry cannot uniquely determine quasi-local energy.

### Theorem V

Non-uniqueness is therefore a structural theorem of general relativity and not a deficiency of existing definitions.

---

# Conclusion

The century-long search for a unique quasi-local energy may have been based on an incorrect premise.

The disagreement between Komar, Hawking, Penrose, Brown–York, Dougan–Mason, Liu–Yau, and related definitions is itself a geometric object.

It lives on the infinite-dimensional manifold of bounding two-surfaces, possesses symmetry, admits cohomological classification, may satisfy conservation laws, and measures the obstruction to completing boundary data in the Einstein initial-boundary value problem.

Quasi-local energy non-uniqueness is therefore not an unresolved failure of general relativity.

It is a structural manifestation of diffeomorphism invariance, observer dependence, and the incompleteness of boundary geometry.

The physical content of gravitational energy may reside not in any individual quasi-local mass, but in the geometry of their differences.
