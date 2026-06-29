# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

## Volume I — Foundations of Finite-Volume Quantum Field Theory

# Part III — Field Theory

---

# 15. Scalar Fields in Finite Volume

## 15.1 Fundamental Construction

Let

[
\Sigma
]

be a compact Riemannian manifold with metric

[
g_{ij}.
]

The spacetime manifold is

[
\mathcal M
==========

\mathbb R\times\Sigma.
]

A real scalar field

[
\phi(t,x)
]

is governed by

[
S[\phi]
=======

\frac12
\int_{\mathcal M}
d^4x,\sqrt{|g|}
\left(
g^{\mu\nu}
\partial_\mu\phi
\partial_\nu\phi
-m^2\phi^2
\right).
]

Variation yields

[
(\Box+m^2)\phi=0.
]

---

## 15.2 Mode Expansion

The Laplace-Beltrami operator satisfies

[
-\Delta u_n=\lambda_n u_n.
]

The field expands as

[
\phi(t,x)
=========

\sum_n
q_n(t)u_n(x).
]

Substitution gives

[
\ddot q_n+\omega_n^2 q_n=0,
]

with

[
\omega_n
========

\sqrt{m^2+\lambda_n}.
]

The field theory decomposes into an infinite set of coupled oscillators.

---

## 15.3 Finite-Volume Spectrum

The Hamiltonian becomes

[
H
=

\sum_n
\omega_n
\left(
a_n^\dagger a_n+\frac12
\right).
]

Unlike infinite volume,

[
\omega_n
]

forms a discrete sequence.

---

## 15.4 Zero Modes

Compact manifolds generally possess

[
\lambda_0=0.
]

The corresponding mode

[
u_0
===

V^{-1/2}
]

requires separate treatment.

Zero modes dominate infrared physics and strongly influence spontaneous symmetry breaking.

---

## 15.5 Finite-Volume Scalar Theorem

A free scalar quantum field on a compact manifold is equivalent to a countable collection of harmonic oscillators labeled by the Laplacian spectrum.

---

# 16. Fermionic Fields

## 16.1 Spin Structure

Fermionic theories require a spin structure on

[
\Sigma.
]

The spinor bundle is

[
S(\Sigma).
]

Fields satisfy

[
\psi(x)\in S(\Sigma).
]

---

## 16.2 Dirac Action

The action is

[
S
=

\int d^4x\sqrt{|g|}
,
\bar\psi
(i\gamma^\mu\nabla_\mu-m)
\psi.
]

The field equation becomes

[
(i\gamma^\mu\nabla_\mu-m)\psi=0.
]

---

## 16.3 Dirac Spectrum

The Dirac operator satisfies

[
D\chi_n=\lambda_n\chi_n.
]

Compactness implies

[
{\lambda_n}
]

is discrete.

The fermion field expands as

[
\psi
====

\sum_n
b_n(t)\chi_n.
]

---

## 16.4 Anticommutation Relations

Creation and annihilation operators obey

[
{b_n,b_m^\dagger}
=================

\delta_{nm}.
]

The finite-volume fermionic Fock space follows directly.

---

## 16.5 Boundary Dependence

Periodic and antiperiodic boundary conditions generate different spectra:

Periodic:

[
p_i
===

\frac{2\pi n_i}{L}.
]

Antiperiodic:

[
p_i
===

\frac{(2n_i+1)\pi}{L}.
]

The vacuum energy therefore depends on the spin structure.

---

## 16.6 Finite-Volume Index Structure

Compact manifolds allow topological characterization through

[
\operatorname{Index}(D).
]

The spectral asymmetry becomes physically observable.

---

# 17. Vector Fields

## 17.1 Abelian Gauge Fields

For electromagnetism

[
A_\mu
]

the action is

[
S
=

-\frac14
\int
F_{\mu\nu}
F^{\mu\nu}.
]

---

## 17.2 Gauge Redundancy

Gauge transformations

[
A_\mu
\rightarrow
A_\mu+\partial_\mu\alpha
]

remain valid on compact spaces.

However global gauge sectors appear.

---

## 17.3 Harmonic Modes

Compact manifolds possess harmonic one-forms

[
h_i.
]

Gauge fields decompose into

[
A
=

d\alpha
+
\delta\beta
+
h.
]

The harmonic sector has no infinite-volume analogue.

---

## 17.4 Wilson Loops

Physical observables include

[
W(C)
====

\exp
\left(
i\oint_C A
\right).
]

Compact topology makes noncontractible loops observable.

---

## 17.5 Massive Vector Fields

For Proca theory

[
(\Box+m^2)A_\mu=0.
]

The mode decomposition follows exactly as in the scalar case.

---

## 17.6 Topological Gauge Sectors

Finite volume naturally introduces sectors labeled by

[
H^1(\Sigma).
]

These sectors contribute independently to the partition function.

---

# 18. Canonical Quantization

## 18.1 Canonical Variables

For a scalar field,

[
\pi
===

\frac{\partial\mathcal L}
{\partial\dot\phi}
==================

\dot\phi.
]

The phase space consists of

[
(\phi,\pi).
]

---

## 18.2 Equal-Time Commutators

Quantization imposes

[
[\phi(x),\pi(y)]
================

i\delta_\Sigma(x,y).
]

The compact delta function satisfies

[
\int_\Sigma
\delta_\Sigma(x,y)f(y)
======================

f(x).
]

---

## 18.3 Mode Quantization

Expanding

[
\phi
====

\sum_n q_nu_n,
]

[
\pi
===

\sum_n p_nu_n,
]

gives

[
[q_n,p_m]
=========

i\delta_{nm}.
]

---

## 18.4 Creation Operators

Define

[
a_n
===

\sqrt{\frac{\omega_n}{2}}
q_n
+
\frac{i}{\sqrt{2\omega_n}}
p_n.
]

Then

[
[a_n,a_m^\dagger]
=================

\delta_{nm}.
]

---

## 18.5 Finite-Volume Quantization Principle

Canonical quantization proceeds exactly as in infinite volume after replacing momentum labels by spectral labels.

---

# 19. Path Integral Quantization

## 19.1 Functional Integral

The generating functional is

[
Z[J]
====

\int D\phi
,
e^{iS+iJ\phi}.
]

Compactness modifies only the spectral measure.

---

## 19.2 Mode Representation

Expanding

[
\phi
====

\sum_n q_nu_n,
]

one obtains

[
D\phi
=====

\prod_n dq_n.
]

The functional integral becomes an infinite-dimensional ordinary integral.

---

## 19.3 Gaussian Theory

For free fields,

[
Z[J]
====

(\det K)^{-1/2}
\exp
\left(
-\frac12
JK^{-1}J
\right).
]

The operator

[
K
=

-\Box+m^2
]

possesses discrete eigenvalues.

---

## 19.4 Spectral Determinants

Finite-volume partition functions naturally involve

[
\det K
======

\prod_n\lambda_n.
]

Spectral zeta-function methods become fundamental.

---

## 19.5 Compact Functional Measure

Compactness eliminates infrared ambiguities associated with continuum momentum integration.

---

# 20. Finite-Volume Propagators

## 20.1 Definition

The propagator satisfies

[
(\Box+m^2)G(x,y)
================

\delta_\Sigma(x,y).
]

---

## 20.2 Spectral Representation

Using eigenfunctions,

[
G(x,y)
======

\sum_n
\frac{
u_n(x)u_n^*(y)
}
{\omega_n^2}.
]

---

## 20.3 Image Representation

For

[
T^3,
]

[
G_L(x)
======

\sum_{n\in\mathbb Z^3}
G_\infty(x+nL).
]

This explicitly exhibits winding sectors.

---

## 20.4 Exponential Corrections

Finite-volume effects behave as

[
e^{-mL}.
]

These terms arise from wrapped propagation around the compact manifold.

---

## 20.5 Universal Structure

Every finite-volume propagator can be decomposed into

[
G_L
===

G_\infty
+
\Delta G.
]

The correction

[
\Delta G
]

contains complete geometric information.

---

# 21. Green Functions

## 21.1 n-Point Functions

Define

[
G_n
===

\langle0|
T\phi(x_1)\cdots\phi(x_n)
|0\rangle.
]

---

## 21.2 Spectral Expansion

Insertion of complete states yields

[
G_n
===

\sum_\alpha
\frac{
\langle0|\phi|\alpha\rangle
\langle\alpha|\phi|0\rangle
}
{E_\alpha}.
]

All intermediate states are discrete.

---

## 21.3 Analytic Structure

Infinite-volume branch cuts are replaced by pole towers:

[
\frac1{s-m^2}
\rightarrow
\sum_n
\frac{Z_n}
{s-E_n^2}.
]

---

## 21.4 Reconstruction Principle

The complete finite-volume Green-function hierarchy determines the finite-volume theory uniquely.

---

## 21.5 Spectral Green-Function Theorem

All finite-volume correlation functions are meromorphic functions whose poles correspond to discrete energy eigenstates.

---

# 22. Cluster Properties

## 22.1 Infinite-Volume Cluster Decomposition

Ordinary QFT requires

[
\langle AB\rangle
\rightarrow
\langle A\rangle
\langle B\rangle
]

for large separation.

---

## 22.2 Compact-Space Difficulty

No arbitrarily large separations exist.

Consequently conventional cluster decomposition cannot hold exactly.

---

## 22.3 Finite-Volume Cluster Function

Define

[
C_{AB}(d)
=========

## \langle AB\rangle

\langle A\rangle
\langle B\rangle.
]

---

## 22.4 Generalized Cluster Principle

For

[
d\ll L,
]

local cluster behavior reproduces infinite-volume physics.

For

[
d\sim L,
]

topological recurrences appear.

---

## 22.5 Exponential Restoration

For massive theories

[
C_{AB}
\sim
e^{-md}
+
e^{-m(L-d)}.
]

The second term measures wrapped propagation.

---

## 22.6 Finite-Volume Cluster Theorem

Cluster decomposition is locally valid and globally modified by topology.

---

# 23. Finite-Volume Effective Actions

## 23.1 Quantum Effective Action

Introduce

[
W[J]
====

-i\ln Z[J].
]

The classical field is

[
\phi_c
======

\frac{\delta W}{\delta J}.
]

---

## 23.2 Legendre Transform

The effective action is

[
\Gamma[\phi_c]
==============

## W[J]

J\phi_c.
]

---

## 23.3 One-Loop Effective Action

For fluctuations around a background field,

[
\Gamma
======

S
+
\frac{i}{2}
\ln\det K.
]

The determinant depends explicitly on the compact geometry.

---

## 23.4 Spectral Representation

Using eigenvalues

[
\lambda_n,
]

[
\Gamma
======

S
+
\frac{i}{2}
\sum_n
\ln\lambda_n.
]

---

## 23.5 Geometric Quantum Corrections

Compactification generates new contributions

[
\Delta\Gamma(L).
]

These encode Casimir energies, finite-size shifts, and topological effects.

---

## 23.6 Effective Geometry Principle

The effective action is a functional not only of fields but also of compact geometry:

[
\Gamma
======

\Gamma[\phi,g,L,\theta].
]

This principle is unique to finite-volume QFT.

---

# Conclusions of Part III

Quantum fields on compact spatial manifolds retain the full conceptual structure of relativistic quantum field theory while acquiring fundamentally new spectral and geometric features. Scalar, fermionic, and vector fields are naturally expanded in discrete eigenmodes of compact operators; canonical and path-integral quantization remain valid after replacement of continuum momentum space by spectral mode space. Propagators, Green functions, and effective actions become intrinsically geometric objects whose analytic structure is governed by discrete spectra rather than continuous cuts.

The central lesson of Part III is that finite-volume QFT is not merely an approximation to ordinary field theory. It is a fully consistent quantum field theory whose observables are encoded in spectral geometry, whose locality is modified by topology, and whose dynamics depend explicitly upon compactification data. These structures form the foundation for the renormalization theory developed in Part IV.
