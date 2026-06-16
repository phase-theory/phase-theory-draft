# Entanglement Entropy as a UV-Complete Observable

## Toward a Non-Perturbative Foundation of Quantum Information in Quantum Field Theory

**A Comprehensive White Paper**

**Version:** 1.0
**Field:** Quantum Field Theory, Quantum Information, Quantum Gravity
**Status:** Foundational Research Framework and Formal Development
**Date:** June 2026

---

# Abstract

Entanglement entropy has emerged as one of the most profound quantities in modern theoretical physics. It plays a central role in quantum information theory, black hole thermodynamics, holography, tensor network constructions of spacetime, and proposals for emergent gravity. Yet, from the perspective of continuum quantum field theory (QFT), entanglement entropy remains fundamentally problematic.

The entanglement entropy of spatial subregions in local QFTs generically exhibits ultraviolet (UV) divergences:

[
S_A\sim \frac{\alpha ,\mathrm{Area}(\partial A)}{\epsilon^{d-2}}+\cdots
]

where:

* (A) is a spatial region,
* (\partial A) is its entangling surface,
* (\epsilon) is a UV regulator,
* (\alpha) is scheme dependent.

Consequently, the entropy itself is not a regulator-independent observable.

This creates a foundational tension:

**Gravity and holography suggest that spacetime geometry is fundamentally encoded in entanglement, yet the QFT quantity from which geometry is supposedly constructed is itself UV-divergent and scheme-dependent.**

This white paper develops a comprehensive theoretical framework addressing:

> Can entanglement entropy be elevated to a UV-complete, physically measurable observable in QFT?

We formulate:

1. A precise classification of entanglement divergences.
2. A renormalization theory of quantum information observables.
3. A non-perturbative Entanglement Renormalization Group (ERG).
4. UV-complete definitions of entropy-like quantities.
5. Operator-algebraic and relative-entropy formulations.
6. Connections to holography, tensor networks, and emergent spacetime.
7. A formal program for Entanglement Effective Field Theory (EEFT).
8. A proposed Entanglement Completion Principle (ECP) defining physically measurable entanglement observables.

The central conclusion is:

> Entanglement entropy itself is not a UV-complete observable. However, equivalence classes of entropic quantities, relative entropies, modular observables, and renormalized entanglement functionals may constitute UV-complete observables of quantum field theories.

---

# 1. Introduction

The last two decades have witnessed an extraordinary convergence:

### Quantum Information

↓

### Quantum Field Theory

↓

### Quantum Gravity

↓

### Emergent Spacetime

Examples include:

* AdS/CFT
* Ryu–Takayanagi formula
* Quantum error correction
* Tensor networks
* ER=EPR
* Entanglement wedge reconstruction
* Complexity geometry
* Quantum extremal surfaces

All rely on one assumption:

> Entanglement is physically meaningful.

However, in continuum QFT:

[
S_A=\infty
]

for every nontrivial spatial region.

Thus:

**How can infinite, regulator-dependent quantities give rise to finite spacetime geometry?**

This is the central paradox.

---

# 2. Entanglement Entropy in QFT

For a bipartition:

[
\mathcal H=\mathcal H_A\otimes \mathcal H_{\bar A}
]

the reduced density matrix is

[
\rho_A
=\mathrm{Tr}_{\bar A}\rho
]

Entanglement entropy:

[
S_A
===

-\mathrm{Tr}
(\rho_A\log\rho_A)
]

For finite systems:

* finite,
* measurable,
* basis independent.

For QFT:

[
S_A=\infty
]

because infinitely many short-distance modes straddle the entangling surface.

---

# 3. Origin of UV Divergences

The two-point function:

[
\langle \phi(x)\phi(y)\rangle
\sim
\frac1{|x-y|^{d-2}}
]

diverges as:

[
x\rightarrow y
]

Near the entangling surface there exist infinitely many pairs of highly correlated modes.

Each contributes:

[
dS>0
]

The cumulative contribution diverges.

Hence:

[
S_A
\propto
\mathrm{Area}(\partial A)
\int_\epsilon
\frac{dr}{r^{d-1}}
]

yielding:

[
S_A
===

\frac{c_0 A}{\epsilon^{d-2}}
+
\frac{c_1}{\epsilon^{d-4}}
+\cdots
]

---

# 4. The Area Law

For (d>2):

[
S_A
===

\alpha
\frac{\mathrm{Area}(\partial A)}
{\epsilon^{d-2}}
+\cdots
]

For (d=2):

[
S_A
===

\frac{c}{3}
\log
\frac{L}{\epsilon}
]

where:

* (c) = central charge.

The logarithmic coefficient is universal.

The leading divergence is not.

---

# 5. Scheme Dependence

Different regulators:

### Lattice cutoff

[
\epsilon=a
]

### Pauli–Villars

[
\epsilon=M^{-1}
]

### Heat kernel

[
\epsilon=\sqrt{s}
]

produce different coefficients:

[
\alpha
\rightarrow
\alpha'
]

Thus:

[
S_A
\neq
\text{observable}
]

because:

[
S_A
\rightarrow
S_A+\Delta S
]

under regulator changes.

---

# 6. Why This Is a Crisis for Emergent Spacetime

The Ryu–Takayanagi formula:

[
S_A
===

\frac{\mathrm{Area}(\gamma_A)}
{4G_N}
]

suggests:

Geometry

[
\Longleftrightarrow
]

Entanglement.

But:

Geometry is finite.

Entanglement entropy is not.

Thus:

[
\infty
\Longrightarrow
\text{finite geometry}
]

requires a missing principle.

This gap is one of the deepest unresolved problems in QFT.

---

# 7. Algebraic QFT Perspective

In local QFT:

[
\mathcal H
\neq
\mathcal H_A\otimes
\mathcal H_{\bar A}
]

Instead:

[
\mathcal A(A)
]

is a type III von Neumann algebra.

Type III algebras possess:

* no density matrix,
* no trace,
* no tensor factorization.

Therefore:

[
S_A
]

is not fundamentally defined.

The UV divergence is a manifestation of:

### incorrect Hilbert-space factorization.

This observation radically changes the problem.

---

# 8. Entropy as an Emergent Quantity

The entropy divergence implies:

Entanglement entropy is not a primitive observable.

Rather:

[
S_A
===

S_{\rm universal}
+
S_{\rm regulator}
]

where:

[
S_{\rm regulator}
]

is nonphysical.

The challenge becomes:

Extract:

[
S_{\rm universal}
]

in a UV-complete manner.

---

# 9. Relative Entropy

Define:

[
S(\rho||\sigma)
===============

\mathrm{Tr}
\left(
\rho\log\rho
------------

\rho\log\sigma
\right)
]

Remarkably:

UV divergences cancel.

Relative entropy is:

* finite,
* regulator independent,
* positive,
* monotonic.

Thus:

[
S(\rho||\sigma)
]

is already a UV-complete information observable.

This suggests:

**Differences of entropies are more fundamental than entropy itself.**

---

# 10. Modular Hamiltonians

Define:

[
\rho_A
======

e^{-K_A}
]

where

[
K_A
===

-\log\rho_A
]

is the modular Hamiltonian.

The first law:

[
\delta S
========

\delta\langle K\rangle
]

is finite.

Modular operators are often better behaved than:

[
S_A
]

itself.

This strongly suggests that:

### modular geometry may be fundamental.

---

# 11. Mutual Information

Define:

[
I(A:B)
======

S_A
+
S_B
---

S_{AB}
]

Leading divergences cancel:

[
I(A:B)<\infty
]

Therefore:

Mutual information is:

* UV finite,
* measurable,
* operational.

It may represent the physically meaningful notion of entanglement.

---

# 12. Renormalized Entanglement Entropy

For spherical regions:

### 2D

[
C(R)
====

R
\frac{dS}{dR}
]

### 3D

[
\mathcal F(R)
=============

(R\partial_R-1)S
]

### 4D

[
\mathcal S(R)
=============

\left(
R\partial_R-1
\right)
R\partial_R S
]

These combinations eliminate power-law divergences.

Result:

Finite entropic observables.

---

# 13. Entanglement Renormalization Group (ERG)

We propose:

## Postulate

There exists an exact flow:

[
\Lambda
\frac{\partial
\mathcal E}
{\partial\Lambda}
=================

\beta_{\mathcal E}
]

where:

[
\mathcal E
]

is a space of entanglement observables.

Analogous to:

Wilsonian RG:

[
\Lambda
\partial_\Lambda S_{\rm eff}
============================

\beta
]

ERG defines:

a renormalization theory of quantum information.

---

# 14. Entanglement Counterterms

Introduce:

[
S_{\rm ren}
===========

## S_{\rm bare}

S_{\rm ct}
]

with:

[
S_{\rm ct}
==========

\sum_n
c_n
\int_{\partial A}
d^{d-2}x
\sqrt h,
\mathcal I_n
]

where:

[
\mathcal I_n
]

are geometric invariants:

* area,
* extrinsic curvature,
* intrinsic curvature.

This is entirely analogous to QFT renormalization.

---

# 15. Entanglement Effective Field Theory (EEFT)

We propose a new framework:

## Degrees of Freedom

Information fields:

[
\Phi_E
]

with action:

[
\Gamma_E[\Phi_E]
]

The EEFT expansion:

[
\Gamma_E
========

\sum_n
g_n
\mathcal O_n[\Phi_E]
]

RG equations:

[
\Lambda
\partial_\Lambda g_n
====================

\beta_n
]

The observables are:

* mutual information,
* relative entropy,
* modular energies,
* renormalized entropies.

---

# 16. UV Completion Principle

### Definition

A quantum information quantity:

[
\mathcal O_E
]

is UV complete iff:

1. regulator independent;
2. finite;
3. operationally measurable;
4. stable under RG flow.

Formally:

[
\Lambda
\partial_\Lambda
\mathcal O_E
============

0
]

This defines:

## Entanglement Completion Principle (ECP)

---

# 17. Emergent Geometry from UV-Complete Entanglement

The metric may emerge from:

[
g_{\mu\nu}
==========

\mathcal G
[
I(A:B),
S(\rho||\sigma),
K_A
]
]

rather than:

[
g_{\mu\nu}
==========

\mathcal G[S_A]
]

This removes dependence on divergent quantities.

The proposal:

**Spacetime emerges from renormalized information observables rather than bare entanglement entropy.**

---

# 18. Tensor Networks and Continuum Limit

Tensor networks naturally implement:

entanglement RG.

MERA:

[
\text{layers}
\leftrightarrow
\text{energy scales}
]

suggests:

[
\text{geometry}
===============

\text{renormalized entanglement flow}
]

The continuum limit requires:

UV-complete information observables.

This paper provides their formal definition.

---

# 19. ER=EPR Revisited

ER=EPR assumes:

entanglement creates connectivity.

However:

bare entropy diverges.

A refined statement is:

[
\text{ER}
=========

\text{EPR}_{\rm ren}
]

where:

[
\text{EPR}_{\rm ren}
====================

{
I,
S(\rho||\sigma),
K,
S_{\rm ren}
}
]

Only renormalized entanglement quantities can support finite geometry.

---

# 20. Central Conjecture

## Entanglement Universality Conjecture (EUC)

For every UV-complete QFT there exists a finite information manifold:

[
\mathfrak I
===========

{
I,
S_{\rm rel},
K,
S_{\rm ren},
\cdots
}
]

such that:

1. all elements are regulator independent;
2. all obey exact ERG equations;
3. spacetime geometry emerges from (\mathfrak I);
4. bare entanglement entropy is merely a coordinate-dependent representation.

---

# 21. Open Problems

### Exact ERG equation

Unknown.

### Complete classification of entanglement counterterms

Unknown.

### Algebraic derivation of EEFT

Unknown.

### Operational measurement in continuum QFT

Incomplete.

### Reconstruction of geometry solely from UV-complete information observables

Open.

### Non-perturbative lattice verification

Open.

### Extension to gauge theories and gravity

Open.

---

# Final Conclusions

The conventional entanglement entropy:

[
S_A
]

is:

* UV divergent,
* regulator dependent,
* not fundamentally defined in algebraic QFT,
* not a UV-complete observable.

However, the following quantities are strong candidates for fundamental observables:

[
\boxed{
I(A:B)
}
]

[
\boxed{
S(\rho||\sigma)
}
]

[
\boxed{
K_A
}
]

[
\boxed{
S_{\rm ren}
}
]

This leads to the central thesis of this white paper:

> **Bare entanglement entropy is not fundamental. The fundamental objects of quantum field theory are renormalized information observables whose equivalence classes remain invariant under entanglement renormalization group flow. Spacetime, if emergent from entanglement, must emerge from these UV-complete information structures rather than from divergent entanglement entropy itself.**

This framework establishes a new research program:

# Quantum Information Renormalization Theory (QIRT)

with

[
\boxed{
\text{Geometry}
===============

\text{RG-Invariant Information}
}
]

as its foundational principle.
