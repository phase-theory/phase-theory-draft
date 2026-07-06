# Part I — Historical and Mathematical Foundations

# Chapter 3

# Worldsheet Conformal Field Theory

---

## 3.1 Introduction

The mathematical foundation of free fermionic string constructions is two-dimensional conformal field theory (2D CFT). Unlike conventional quantum field theories defined directly on spacetime, perturbative string theory is formulated as a quantum field theory on the two-dimensional worldsheet swept out by a propagating string. Every physical state, interaction, and symmetry observed in spacetime originates from the conformal dynamics of this two-dimensional surface.

For free fermionic constructions, the worldsheet theory is especially powerful because it is exactly solvable. Instead of specifying a six-dimensional compact manifold explicitly, the internal degrees of freedom are represented by free fermions satisfying carefully chosen boundary conditions. Modular invariance and generalized GSO projections then determine the complete perturbative spectrum.

This chapter develops the conformal field theoretic framework upon which the remainder of the free fermionic formalism is built.

---

# 3.2 The String Worldsheet

A relativistic string propagating through a (D)-dimensional spacetime traces a two-dimensional surface,

[
\Sigma ,
]

called the **worldsheet**.

Coordinates on the worldsheet are denoted

[
(\tau,\sigma),
]

where

* (\tau) represents worldsheet time,
* (\sigma) parameterizes the string.

The embedding into spacetime is described by

[
X^\mu(\tau,\sigma),
\qquad
\mu=0,\ldots,D-1.
]

For closed strings,

[
\sigma
\sim
\sigma+2\pi .
]

Introducing complex coordinates,

[
z
=

e^{\tau+i\sigma},
\qquad
\bar z
======

e^{\tau-i\sigma},
]

greatly simplifies the conformal structure.

The worldsheet metric

[
h_{ab}
]

may be gauge-fixed using diffeomorphism and Weyl invariance, reducing the classical action to a free conformal field theory.

For the bosonic coordinates,

[
S_X
===

-\frac{1}{4\pi\alpha'}
\int d^2\sigma
,
\partial_aX^\mu
\partial^aX_\mu .
]

The resulting equations of motion are

[
\partial\bar\partial X^\mu
==========================

0,
]

whose general solution separates into independent left- and right-moving components,

[
X^\mu(z,\bar z)
===============

X_L^\mu(z)
+
X_R^\mu(\bar z).
]

This factorization is one of the defining properties of two-dimensional conformal field theory and underlies the heterotic construction.

---

# 3.3 Two-Dimensional Conformal Field Theory

A conformal transformation preserves local angles while allowing arbitrary local rescalings of the metric,

[
g_{ab}
\rightarrow
e^{2\omega}
g_{ab}.
]

In two dimensions the conformal symmetry algebra becomes infinite dimensional.

Holomorphic transformations

[
z
\rightarrow
f(z)
]

and antiholomorphic transformations

[
\bar z
\rightarrow
\bar f(\bar z)
]

generate two independent copies of the Virasoro algebra.

The energy-momentum tensor splits accordingly,

[
T(z),
\qquad
\bar T(\bar z),
]

with Laurent expansions

[
T(z)
====

\sum_{n=-\infty}^{\infty}
\frac{L_n}{z^{n+2}},
]

[
\bar T(\bar z)
==============

\sum_{n=-\infty}^{\infty}
\frac{\bar L_n}{\bar z^{n+2}}.
]

The Virasoro generators satisfy

[
[L_m,L_n]
=========

(m-n)L_{m+n}
+
\frac{c}{12}
m(m^2-1)
\delta_{m+n,0},
]

where

[
c
]

is the **central charge**.

The infinite-dimensional conformal symmetry provides sufficient constraints to solve many worldsheet theories exactly, including those underlying free fermionic constructions.

---

# 3.4 Left- and Right-Moving Sectors

The decomposition

[
X^\mu
=====

X_L
+
X_R
]

extends to all worldsheet degrees of freedom.

In heterotic string theory the two sectors are fundamentally different.

The right-moving sector is supersymmetric and contains

* spacetime bosons,
* worldsheet fermions,
* superconformal symmetry.

The left-moving sector remains bosonic but includes additional internal degrees of freedom responsible for gauge symmetry.

Symbolically,

[
\mathcal H
==========

\mathcal H_L
\otimes
\mathcal H_R.
]

The central charges satisfy

[
c_R
===

15,
]

[
c_L
===

26.

]

The difference

[
26-15=11
]

is compensated by sixteen additional left-moving internal dimensions, which ultimately generate the gauge groups

[
E_8\times E_8
]

or

[
SO(32).
]

This asymmetric construction is the defining feature of heterotic string theory.

---

# 3.5 Free Worldsheet Fermions

Instead of describing the internal dimensions geometrically, free fermionic models replace them with free Majorana fermions living on the worldsheet.

Each fermion

[
f(z)
]

has action

[
S_f
===

\frac{i}{2\pi}
\int
d^2z
,
f
\bar\partial
f.
]

Its equation of motion is simply

[
\bar\partial f=0,
]

showing that the field is holomorphic.

A free fermion admits two possible boundary conditions,

[
f(\sigma+2\pi)
==============

*

f(\sigma),
]

or

[
f(\sigma+2\pi)
==============

*

f(\sigma).
]

These correspond respectively to

* **Neveu–Schwarz (NS)** sectors,
* **Ramond (R)** sectors.

More generally,

[
f(\sigma+2\pi)
==============

*

e^{i\pi\alpha}
f(\sigma),
]

where

[
\alpha
]

is specified by the basis vectors introduced in later chapters.

The mode expansion becomes

[
f(z)
====

\sum_r
\frac{f_r}{z^{r+1/2}},
]

where

[
r
\in
\mathbb Z+\frac12
]

for NS sectors,

and

[
r
\in
\mathbb Z
]

for Ramond sectors.

Quantization yields

[
{f_r,f_s}
=========

\delta_{r+s,0}.
]

Every physical state is constructed by acting with these creation operators upon an appropriate vacuum.

---

# 3.6 Operator Product Expansions

The exact solvability of free fermion theories follows from their simple operator product expansions (OPEs).

For a single Majorana fermion,

[
f(z)
f(w)
\sim
\frac{1}{z-w}.
]

Similarly,

[
\partial X^\mu(z)
\partial X^\nu(w)
\sim
----

\frac{\alpha'}{2}
\frac{\eta^{\mu\nu}}
{(z-w)^2}.
]

These OPEs determine all correlation functions through Wick's theorem.

The energy-momentum tensor of a free fermion is

[
T(z)
====

-\frac12
:
f
\partial f
:.
]

Its self-OPE reproduces the Virasoro algebra with central charge

[
c
=

\frac12
]

for each real Majorana fermion.

Thus collections of free fermions possess additive central charges,

[
c_{\rm total}
=============

\sum_i c_i.
]

This additive property is fundamental to the construction of modular-invariant heterotic models.

---

# 3.7 Central Charge and Conformal Consistency

Quantum conformal invariance requires cancellation of the Weyl anomaly.

The anomaly is measured by the total central charge,

[
c_{\rm matter}
+
c_{\rm ghosts}
==============

0.

]

For superstrings,

[
c_{\rm ghosts}
==============

-15,
]

requiring

[
c_{\rm matter}
==============

15
]

for the supersymmetric sector.

Similarly,

[
26
]

is required in the bosonic sector.

Each free field contributes

| Field            | Central Charge |
| ---------------- | -------------: |
| Real scalar      |            (1) |
| Majorana fermion |          (1/2) |
| Complex fermion  |            (1) |

The heterotic construction therefore carefully balances the field content so that the complete worldsheet theory satisfies

[
c_L=26,
\qquad
c_R=15.
]

Failure of this condition destroys conformal invariance and renders the string theory inconsistent.

---

# 3.8 Worldsheet Supersymmetry

The right-moving sector possesses local supersymmetry generated by the supercurrent

[
G(z).
]

For free fields,

[
G
=

\psi^\mu
\partial X_\mu.
]

The supercurrent together with

[
T(z)
]

generates the super-Virasoro algebra,

[
{G_r,G_s}
=========

2L_{r+s}
+
\frac{c}{3}
\left(
r^2-\frac14
\right)
\delta_{r+s,0}.
]

Physical states satisfy

[
L_n
|\Psi\rangle
============

0,
\qquad
n>0,
]

[
G_r
|\Psi\rangle
============

0,
\qquad
r>0,
]

together with the mass-shell condition

[
L_0
|\Psi\rangle
============

a
|\Psi\rangle.
]

These constraints eliminate negative-norm states and ensure the consistency of the quantum theory.

---

# 3.9 Worldsheet Fermion Content of Free Fermionic Models

The canonical four-dimensional heterotic free fermionic formulation employs forty-four real worldsheet fermions,

[
{
\psi^\mu,
\chi^i,
y^i,
\omega^i
;
|;
\bar y^i,
\bar\omega^i,
\bar\psi^{1,\ldots,5},
\bar\eta^{1,2,3},
\bar\phi^{1,\ldots,8}
}.
]

These fields naturally divide into several sectors:

* spacetime fermions,
* internal supersymmetric fermions,
* compactification fermions,
* observable gauge fermions,
* hidden-sector gauge fermions.

The assignment of boundary conditions to this finite collection of fermions completely specifies a free fermionic vacuum. Consequently, all geometric information relevant to perturbative physics is encoded algebraically in a finite set of discrete boundary-condition vectors rather than in continuous metric data.

---

# 3.10 Summary

Two-dimensional conformal field theory provides the exact mathematical language in which free fermionic heterotic models are formulated. The decomposition into left- and right-moving sectors, the free-fermion representation of internal degrees of freedom, the Virasoro and super-Virasoro algebras, and the requirement of central-charge cancellation together define a consistent quantum worldsheet theory.

The principal advantage of the free-fermionic approach is that compactification data are represented by discrete algebraic structures while preserving exact conformal invariance. This exact solvability enables direct calculation of spectra, gauge symmetries, and interaction terms without requiring explicit knowledge of an underlying compactification metric. Building on these foundations, the following chapter develops the bosonization correspondence and shows how free worldsheet fermions encode the compact internal dimensions that are represented geometrically in other formulations of heterotic string theory.
