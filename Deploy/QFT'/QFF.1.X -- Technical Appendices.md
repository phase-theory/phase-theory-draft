# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

## Volume I — Foundations of Finite-Volume Quantum Field Theory

# Technical Appendices

---

# Appendix 35 — Spectral Geometry

## 35.1 Introduction

Finite-volume quantum field theory is fundamentally a spectral theory. The primary observables are not scattering amplitudes but spectra:

[
\mathcal S=
{E_n(L,\theta,g)}.
]

The mathematical framework governing such spectra is spectral geometry.

Spectral geometry studies the relationship between geometric structures and eigenvalue distributions of differential operators.

The central question is:

[
\text{Geometry}
\longleftrightarrow
\text{Spectrum}.
]

---

## 35.2 Laplace–Beltrami Operator

Let

[
(\Sigma,g)
]

be a compact Riemannian manifold.

The Laplace–Beltrami operator is

[
\Delta
======

\frac1{\sqrt g}
\partial_i
\left(
\sqrt g,g^{ij}\partial_j
\right).
]

The eigenvalue problem is

[
-\Delta u_n
===========

\lambda_n u_n.
]

Compactness implies

[
0=\lambda_0
<
\lambda_1
\le
\lambda_2
\le
\cdots.
]

---

## 35.3 Weyl Asymptotics

The counting function

[
N(\Lambda)
==========

#{\lambda_n<\Lambda}
]

satisfies

[
N(\Lambda)
==========

\frac{\operatorname{Vol}(\Sigma)}
{6\pi^2}
\Lambda^{3/2}
+
\mathcal O(\Lambda).
]

Thus the high-energy spectrum determines volume.

---

## 35.4 Heat Kernel

Define

[
K(x,y;s)
========

\langle x|
e^{-s\Delta}
|y\rangle.
]

The trace satisfies

[
K(s)
====

\sum_n
e^{-s\lambda_n}.
]

For small (s),

[
K(s)
\sim
(4\pi s)^{-3/2}
\sum_{k=0}^{\infty}
a_k s^k.
]

---

## 35.5 Geometric Invariants

The first coefficients are

[
a_0
===

\operatorname{Vol}(\Sigma),
]

[
a_1
===

\frac16
\int_\Sigma
R,dV,
]

[
a_2
===

\frac1{360}
\int_\Sigma
\left(
5R^2
-2R_{ij}R^{ij}
+2R_{ijkl}R^{ijkl}
\right)dV.
]

These coefficients govern ultraviolet renormalization.

---

## 35.6 Spectral Geometry Reconstruction Conjecture

We postulate:

**Conjecture.**

The complete finite-volume spectrum

[
\mathcal S
==========

{E_n(L,\theta,g)}
]

uniquely determines all physical observables.

This statement generalizes the inverse spectral problem to interacting quantum field theory.

---

## 35.7 Spectral–Physical Duality

Geometry determines spectrum:

[
(\Sigma,g)
\rightarrow
\mathcal S.
]

Finite-volume QFT proposes the converse:

[
\mathcal S
\rightarrow
\mathcal D,
]

where

[
\mathcal D
]

denotes complete dynamics.

This duality underlies the entire reconstruction program developed in later volumes.

---

# Appendix 36 — Functional Analysis

## 36.1 Hilbert Spaces

Let

[
\mathcal H
==========

L^2(\Sigma).
]

The inner product is

[
\langle f,g\rangle
==================

\int_\Sigma
f^*(x)g(x)dV.
]

Compactness guarantees separability.

---

## 36.2 Orthonormal Bases

The spectral theorem yields

[
\mathcal H
==========

\overline{
\operatorname{span}
{u_n}
}.
]

Every state possesses an expansion

[
f
=

\sum_n
c_nu_n.
]

---

## 36.3 Bounded Operators

An operator

[
A
:
\mathcal H
\rightarrow
\mathcal H
]

is bounded if

[
|Af|
\le
M|f|.
]

Bounded operators form a Banach algebra

[
\mathcal B(\mathcal H).
]

---

## 36.4 Self-Adjoint Operators

Physical observables satisfy

[
A=A^\dagger.
]

The Hamiltonian

[
H
]

must be self-adjoint to ensure unitary evolution.

---

## 36.5 Spectral Resolution

For self-adjoint

[
H,
]

[
H
=

\sum_n
E_n
|n\rangle
\langle n|.
]

The discrete structure follows from compactness.

---

## 36.6 Resolvent Theory

Define

[
R(z)
====

(H-z)^{-1}.
]

Poles occur at

[
z=E_n.
]

Thus finite-volume correlation functions are meromorphic.

---

## 36.7 Functional Calculus

For analytic functions

[
f(H)
====

\sum_n
f(E_n)
|n\rangle
\langle n|.
]

Examples include

[
e^{-itH},
]

[
e^{-\beta H},
]

and

[
\ln H.
]

These objects appear repeatedly throughout finite-volume field theory.

---

# Appendix 37 — Compact Operator Theorems

## 37.1 Compact Operators

An operator

[
K
:
\mathcal H
\rightarrow
\mathcal H
]

is compact if bounded sets map to relatively compact sets.

Compact operators generalize finite-dimensional matrices.

---

## 37.2 Spectral Theorem for Compact Operators

Let

[
K
=

K^\dagger.
]

Then

[
K u_n
=====

\mu_nu_n,
]

with

[
\mu_n\to0.
]

The spectrum is discrete.

---

## 37.3 Compact Resolvent Theorem

**Theorem.**

If

[
(H-z)^{-1}
]

is compact, then

[
H
]

possesses purely discrete spectrum.

---

### Proof

Applying the compact spectral theorem to

[
R(z),
]

its eigenvalues satisfy

[
\nu_n\to0.
]

Since

[
\nu_n
=====

(E_n-z)^{-1},
]

the corresponding energies form a countable sequence diverging toward infinity.

∎

---

## 37.4 Application to Finite-Volume QFT

Elliptic differential operators on compact manifolds possess compact resolvents.

Consequently:

[
\operatorname{Spec}(H)
======================

{E_n}.
]

This result explains why finite-volume theories exhibit discrete spectra.

---

## 37.5 Fredholm Alternative

For compact operators,

[
(I-K)x=y
]

possesses either:

1. A unique solution, or
2. A finite-dimensional kernel.

Many finite-volume quantization conditions arise as Fredholm determinant equations.

---

## 37.6 Determinant Formulation

For compact operators,

[
\det(I-K)
]

is well defined.

Energy levels satisfy

[
\det(I-K(E,L))
==============

0.

]

This form will become central in Volumes II–IV.

---

## 37.7 Universal Quantization Principle

Every finite-volume spectrum may be represented as the zero set of a Fredholm determinant constructed from compact operators.

This principle generalizes Lüscher-type quantization conditions.

---

# Appendix 38 — Group-Theoretic Conventions

## 38.1 Rotational Symmetry

Infinite-volume theories possess

[
SO(3)
]

symmetry.

Representations are labeled by

[
\ell
====

0,1,2,\ldots.
]

---

## 38.2 Spherical Harmonics

The basis functions satisfy

[
L^2Y_{\ell m}
=============

\ell(\ell+1)
Y_{\ell m}.
]

---

## 38.3 Cubic Symmetry

Finite cubic volumes preserve only

[
O_h.
]

The irreducible representations are

[
A_1,,
A_2,,
E,,
T_1,,
T_2.
]

---

## 38.4 Subduction

Infinite-volume angular momentum decomposes according to

[
SO(3)
\rightarrow
O_h.
]

Examples:

[
\ell=0
\rightarrow
A_1,
]

[
\ell=1
\rightarrow
T_1,
]

[
\ell=2
\rightarrow
E\oplus T_2.
]

---

## 38.5 Translation Group

For

[
T^3,
]

translations form

[
U(1)^3.
]

Representations are labeled by discrete momenta

[
k_i
===

\frac{2\pi n_i}{L}.
]

---

## 38.6 Little Groups

For nonzero total momentum

[
P,
]

the relevant symmetry becomes the subgroup preserving (P).

These little groups organize moving-frame spectra.

---

## 38.7 Internal Symmetries

Gauge and flavor symmetries are denoted generically by

[
G_{\rm int}.
]

Examples:

[
U(1),
]

[
SU(2),
]

[
SU(3).
]

---

## 38.8 Product Structure

Finite-volume states transform under

[
G_{\rm FV}
==========

G_{\rm space}
\times
G_{\rm int}.
]

The full representation labels are therefore

[
(\Lambda,\alpha),
]

where

[
\Lambda
]

is a spatial irrep and

[
\alpha
]

an internal irrep.

---

## 38.9 Symmetry Reconstruction Theorem

As

[
L\rightarrow\infty,
]

the sequence of finite-volume representations reconstructs the continuous representations of

[
SO(3).
]

Thus ordinary angular momentum theory emerges from finite-volume representation theory.

---

# Final Remarks on Volume I

Volume I has established the conceptual and mathematical foundations of finite-volume quantum field theory. Compact geometry, discrete spectra, spectral observables, generalized locality, finite-volume renormalization, and spectral scattering theory have been unified into a single framework. The technical appendices provide the mathematical infrastructure required for the subsequent development of exact quantization conditions and inverse spectral reconstruction.

The central conclusion is that finite-volume quantum field theory is not merely a numerical approximation to infinite-volume physics. It is a mathematically complete framework whose primary observables are spectral and geometric. Infinite-volume quantum field theory emerges through decompactification as a singular limiting phase of this more general compact-space theory.

These foundations prepare the way for Volume II, where two-body scattering, coupled channels, and generalized Lüscher quantization conditions will be derived from first principles and incorporated into the broader spectral reconstruction program.
