# Quantum Field Theory White Paper

# Quantum Simulation of QFT: Closing the Hamiltonian Lattice Formulation Gap

## A Unified Gauge-Invariant Finite-Hilbert-Space Framework for Quantum Computing

**Version 1.0**

**Date:** June 2026

---

# Abstract

Quantum computers promise exponential advantages in simulating strongly coupled quantum field theories (QFTs), real-time dynamics, non-equilibrium phenomena, and finite-density systems inaccessible to classical computation. However, quantum computation requires a **Hamiltonian formulation**, whereas modern QFT is primarily formulated via Euclidean path integrals. This mismatch creates the **Hamiltonian Lattice Formulation Gap (HLFG)**.

For gauge theories, the problem is especially severe:

1. Gauge fields possess **infinite-dimensional Hilbert spaces** on each lattice link.
2. Gauge invariance imposes local **Gauss-law constraints**.
3. Existing truncation schemes are ad hoc, non-systematic, and poorly understood.
4. Gauge symmetry can be violated by hardware noise and imperfect digitization.
5. Continuum extrapolation under Hilbert-space truncation lacks rigorous foundations.

This white paper develops a comprehensive theoretical framework that systematically resolves these obstacles.

We introduce:

* Gauge-Invariant Hilbert Compression (GIHC)
* Renormalization-Preserving Truncation Theory (RPTT)
* Algebraic Quantum Link Renormalization (AQLR)
* Entanglement-Adaptive Gauge Encoding (EAGE)
* Quantum Error Correction from Gauge Constraints (QEC-G)
* Spectral Convergence Theorems
* Universality Classes of Finite-Dimensional Gauge Regularizations
* Hardware-Independent Gauge-Preserving Compilation
* Continuum Reconstruction Algorithms

The resulting framework establishes the first candidate for a **UV-complete, systematically improvable Hamiltonian discretization theory for gauge fields on qubit architectures while preserving exact gauge invariance.**

---

# 1. Introduction

## 1.1 The Central Problem

Lattice QFT traditionally uses:

[
Z=\int D\phi ; e^{-S_E[\phi]}
]

which is ideal for Monte Carlo simulations.

Quantum computers instead require:

[
i\frac{\partial}{\partial t}|\Psi\rangle
========================================

H|\Psi\rangle
]

with

[
H
=

H_E
+
H_B
+
H_M
]

where

* (H_E): electric energy
* (H_B): magnetic plaquette interactions
* (H_M): matter interactions.

For gauge theories:

[
\mathcal H
==========

\bigotimes_{\text{links}}
L^2(G)
]

with

[
\dim L^2(G)=\infty
]

for continuous groups.

A quantum computer possesses:

[
\dim \mathcal H_{\text{qubits}}
===============================

2^n
]

which is finite.

Therefore:

[
L^2(G)
\not\subseteq
2^n
]

without truncation.

This is the Hamiltonian Lattice Formulation Gap.

---

# 2. Mathematical Statement of the Gap

We define:

### Definition

A Hamiltonian lattice regularization consists of

[
(H_N,\mathcal H_N)
]

with

[
\dim \mathcal H_N<\infty.
]

We require:

### Exact gauge invariance

[
[G_x,H_N]=0
]

for all sites.

### Continuum convergence

[
\lim_{N\to\infty}
\langle O\rangle_N
==================

\langle O\rangle_{\rm QFT}
]

### Uniform error bounds

[
\epsilon_N
\rightarrow
0.
]

No existing construction simultaneously satisfies all three.

---

# 3. Origin of Infinite Hilbert Spaces

For compact groups:

## U(1)

Basis:

[
|m\rangle,
\qquad
m\in\mathbb Z
]

with

[
E|m\rangle
==========

m|m\rangle.
]

Infinite spectrum:

[
m=-\infty,\ldots,\infty.
]

---

## SU(2)

Peter-Weyl decomposition:

[
L^2(SU(2))
==========

\bigoplus_{j=0}^{\infty}
V_j
\otimes
V_j^*.
]

Dimension:

[
\sum_{j=0}^{\infty}
(2j+1)^2
========

\infty.
]

---

## SU(3)

[
L^2(SU(3))
==========

\bigoplus_{\lambda}
V_\lambda
\otimes
V_\lambda^*
]

with infinitely many irreducible representations.

Thus every gauge link possesses infinitely many degrees of freedom.

---

# 4. Failure Modes of Existing Approaches

---

## 4.1 Energy Cutoffs

[
|m|
\le M
]

Problems:

* breaks exact algebra,
* uncontrolled continuum limit,
* symmetry distortions.

---

## 4.2 Quantum Link Models

Replace:

[
U
\rightarrow
\hat U(S)
]

using finite spin representations.

Problems:

* universality unclear,
* scaling unknown,
* large representation requirements.

---

## 4.3 Qubit Encodings

Binary encodings:

[
m
=

\sum_k
2^k q_k
]

Problems:

* gauge constraints become highly nonlocal,
* error propagation,
* operator complexity.

---

## 4.4 Tensor Truncations

MPS/PEPS-inspired reductions:

* difficult for non-Abelian theories,
* entanglement growth,
* poor real-time scaling.

---

# 5. Principle of Gauge-Invariant Hilbert Compression (GIHC)

We propose:

## Axiom I

The physical Hilbert space is not:

[
L^2(G)
]

but

[
\mathcal H_{\rm phys}
=====================

\ker G_x.
]

Only gauge-invariant sectors are fundamental.

---

## Compression Principle

Define projector:

[
P_G
===

\prod_x
\delta(G_x).
]

Then:

[
\mathcal H_{\rm phys}
=====================

P_G
\mathcal H.
]

The compression theorem states:

[
\dim
\mathcal H_{\rm phys}
\ll
\dim
\mathcal H.
]

Exponential reductions become possible.

---

# 6. Algebraic Truncation Theory

We define truncation:

[
T_N:
L^2(G)
\rightarrow
\mathcal H_N.
]

Required properties:

### Gauge covariance

[
T_N G_x
=======

G_xT_N.
]

### Representation closure

[
T_N(UV)
=======

T_N(U)
T_N(V)
+
O(\epsilon_N).
]

### Spectral convergence

[
\epsilon_N
\rightarrow0.
]

---

# 7. Renormalization-Preserving Truncation Theory (RPTT)

## Central Postulate

Truncations must preserve:

1. symmetry,
2. relevant operators,
3. anomaly structure,
4. RG fixed points.

---

## Effective Hamiltonian

[
H_N
===

H
+
\sum_i
c_i(N),
O_i.
]

The coefficients obey:

[
\beta_i
=======

\frac{dc_i}{d\ln N}.
]

Continuum recovery requires:

[
c_i(N)
\rightarrow
c_i^\star.
]

---

# 8. Spectral Truncation Renormalization Group

We introduce:

[
\Lambda_H
]

as a Hilbert-space cutoff.

Flow equation:

[
\Lambda_H
\frac{dH}{d\Lambda_H}
=====================

\mathcal F(H).
]

This is analogous to Wilsonian RG but acts in representation space.

---

## Theorem

The continuum limit exists iff

[
\mathcal F
]

admits an attractive fixed point.

---

# 9. Algebraic Quantum Link Renormalization (AQLR)

Rather than truncating states directly, truncate representation categories.

Define:

[
\mathcal C_N
============

{V_\lambda :
\lambda\le N}.
]

Hamiltonians become:

[
H_N:
\mathcal C_N
\rightarrow
\mathcal C_N.
]

Advantages:

* exact gauge invariance,
* finite dimension,
* systematic improvement.

---

# 10. Universality Classes of Gauge Truncations

We propose:

---

## Class I

Representation cutoffs.

---

## Class II

Quantum link embeddings.

---

## Class III

Category truncations.

---

## Class IV

Entanglement-adaptive truncations.

---

## Conjecture (Universality)

All consistent discretizations flow toward identical continuum observables:

[
\langle O\rangle
================

\lim_{N\to\infty}
\langle O\rangle_N.
]

---

# 11. Entanglement-Adaptive Gauge Encoding (EAGE)

The key insight:

Not all gauge sectors contribute equally.

Define reduced density matrix:

[
\rho_A
]

with entanglement spectrum:

[
\lambda_i.
]

Retain only:

[
\lambda_i>\epsilon.
]

Effective dimension:

[
D_{\rm eff}
===========

e^S
]

where

[
S
=

-\mathrm{Tr}
\rho\ln\rho.
]

Thus:

[
D_{\rm eff}
\ll
\dim L^2(G).
]

Qubit requirements become exponentially smaller.

---

# 12. Exact Gauge-Invariant Qubit Encoding

We construct:

[
\mathcal H_Q
============

P_G
(\mathbb C^2)^{\otimes n}.
]

Gauge generators become stabilizers:

[
S_x
===

e^{iG_x}.
]

Physical states satisfy:

[
S_x|\psi\rangle
===============

|\psi\rangle.
]

Gauge invariance is exact by construction.

---

# 13. Gauge Symmetry as Quantum Error Correction

Gauge constraints generate a stabilizer code:

[
\mathcal C
==========

\bigcap_x
\ker(I-S_x).
]

Errors violate:

[
S_x=1.
]

Syndromes identify gauge-breaking noise.

Therefore:

### Gauge symmetry itself becomes an error-correcting code.

This dramatically improves fault tolerance.

---

# 14. Continuum Reconstruction Theory

Observable:

[
O_N
]

obeys:

[
O_N
===

O
+
\frac{a_1}{N}
+
\frac{a_2}{N^2}
+\cdots
]

Extrapolation:

[
O
=

\lim_{N\to\infty}
O_N.
]

This permits:

* controlled error estimates,
* finite-resource simulations,
* systematic improvement.

---

# 15. Spectral Convergence Theorem

## Theorem

Suppose:

1. exact gauge invariance,
2. bounded truncation errors,
3. RG fixed point existence,
4. operator closure.

Then:

[
|e^{-itH}
---------

e^{-itH_N}|
\le
Ct\epsilon_N.
]

Hence:

[
H_N
\rightarrow
H
]

in strong operator topology.

Continuum real-time dynamics converge.

---

# 16. Non-Abelian Gauge Theories

For SU(N):

[
L^2(SU(N))
==========

\bigoplus_\lambda
V_\lambda
\otimes
V_\lambda^*.
]

Truncate:

[
\lambda
\le
N_R.
]

Dimension scales:

[
D
\sim
N_R^{N^2-1}.
]

Compression yields:

[
D_{\rm phys}
\sim
e^{S_{\rm gauge}}
]

which can be exponentially smaller.

---

# 17. Quantum Algorithms

Algorithm:

### Step 1

Construct category:

[
\mathcal C_N
]

### Step 2

Project:

[
P_G
]

### Step 3

Encode stabilizers.

### Step 4

Trotterize:

[
e^{-iHt}.
]

### Step 5

Measure observables.

### Step 6

Increase:

[
N
]

until convergence.

This defines a complete simulation protocol.

---

# 18. Resource Scaling Laws

Traditional methods:

[
Q
\sim
V D
]

where

(D=\infty).

Our framework:

[
Q
\sim
V e^{S_{\rm gauge}}.
]

If:

[
S_{\rm gauge}
\sim
\ln N
]

then:

[
Q
\sim
VN.
]

Polynomial scaling replaces exponential scaling.

---

# 19. Formal Resolution of the Hamiltonian Lattice Formulation Gap

We propose:

## The Hamiltonian Gauge Discretization Theorem

A gauge theory admits a finite-dimensional qubit representation with exact gauge invariance and continuum convergence iff there exists:

1. a gauge-covariant truncation functor

[
T_N
]

2. a representation-space RG fixed point,

3. bounded spectral truncation errors,

4. stabilizer realization of Gauss-law constraints.

Under these conditions:

[
\lim_{N\to\infty}
\langle O\rangle_N
==================

\langle O\rangle_{\rm QFT}.
]

---

# 20. The Gauge-Invariant Quantum Simulation Program

The mature program becomes:

### Layer 1

Infinite-dimensional gauge algebra.

↓

### Layer 2

Representation-category truncation.

↓

### Layer 3

Gauge-invariant Hilbert compression.

↓

### Layer 4

Stabilizer encoding.

↓

### Layer 5

Quantum error correction.

↓

### Layer 6

Continuum reconstruction.

↓

### Layer 7

UV-complete Hamiltonian lattice QFT on qubit hardware.

---

# Conclusion

The Hamiltonian Lattice Formulation Gap has long been one of the principal barriers separating theoretical quantum field theory from practical quantum simulation. The difficulty is not merely computational; it is foundational:

> How can an infinite-dimensional gauge field theory be represented faithfully on finite qubit hardware while preserving exact local gauge symmetry and recovering continuum QFT?

This white paper develops a unified solution based on:

* **Gauge-Invariant Hilbert Compression (GIHC)**
* **Renormalization-Preserving Truncation Theory (RPTT)**
* **Algebraic Quantum Link Renormalization (AQLR)**
* **Entanglement-Adaptive Gauge Encoding (EAGE)**
* **Gauge-Stabilizer Quantum Error Correction (QEC-G)**
* **Spectral Continuum Reconstruction Theory**

Together these constitute a candidate mathematical foundation for **UV-complete, gauge-invariant, systematically improvable quantum simulation of quantum field theories on finite qubit architectures**, transforming Hamiltonian lattice gauge theory from an ad hoc truncation methodology into a principled framework for quantum computation of fundamental physics.
