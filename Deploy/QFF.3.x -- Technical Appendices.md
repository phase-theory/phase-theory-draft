# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume III — Three-Body Quantum Field Theory in Finite Volume

## Technical Appendices

---

# Appendix 21 — Integral Equation Methods

## 21.1 Introduction

The modern theory of finite-volume three-body quantum field dynamics is fundamentally an integral-equation theory. Although the quantization conditions derived in the main text are expressed as determinant equations, their derivation, interpretation, and numerical implementation rely upon coupled integral equations governing three-body scattering amplitudes and resolvents.

This appendix develops the mathematical machinery underlying these constructions.

---

## 21.2 Three-Body Scattering Equation

Let

[
\mathcal M_3(E)
]

denote the full three-body scattering amplitude.

The exact operator equation may be written

[
\mathcal M_3
============

K_3
+
K_3 G_0 \mathcal M_3,
]

where

[
G_0(E)
======

(E-H_0+i\epsilon)^{-1}
]

is the free resolvent.

Formally,

[
\mathcal M_3
============

(1-K_3G_0)^{-1}K_3.
]

---

## 21.3 Fredholm Structure

The equation

[
\phi
====

f+\lambda K\phi
]

belongs to the class of Fredholm equations of the second kind.

Three-body scattering amplitudes satisfy analogous equations:

[
\mathcal M
==========

\mathcal K
+
\mathcal K G_0 \mathcal M.
]

Existence and uniqueness follow from compactness of the kernel.

---

## 21.4 Compact-Space Integral Operators

In finite volume,

[
\int \frac{d^3k}{(2\pi)^3}
]

is replaced by

[
\frac1{L^3}
\sum_k.
]

The kernel becomes

[
K_L(k,k').
]

Since the momentum lattice is discrete, the operator is compact.

---

## 21.5 Spectator Integral Equation

Using the spectator representation,

[
T(k,k')
=======

B(k,k')
+
\sum_q
B(k,q)G(q)T(q,k').
]

This equation is the fundamental dynamical relation of finite-volume three-body theory.

---

## 21.6 Faddeev Decomposition

The amplitude is decomposed:

[
T=T_1+T_2+T_3.
]

Each component satisfies

[
T_i
===

t_i
+
t_i G_0
\sum_{j\neq i}
T_j.
]

This removes disconnected singularities and ensures exact counting of scattering processes.

---

## 21.7 Resolvent Equations

The compact-space resolvent

[
R(E)
====

(E-H)^{-1}
]

satisfies

[
R
=

R_0
+
R_0VR.
]

Repeated substitution generates the Neumann expansion:

[
R
=

R_0
+
R_0VR_0
+
R_0VR_0VR_0
+\cdots.
]

---

## 21.8 Kernel Singularities

Three-body kernels contain:

[
\frac1{E-E_q},
]

[
\frac1{(E-E_q)^2},
]

and logarithmic threshold structures.

Special regularization procedures are required.

---

## 21.9 Divergence-Free Reformulation

Introducing

[
K_{\mathrm{df},3}
]

removes disconnected singular contributions.

The resulting integral equations become numerically stable and possess well-defined infinite-volume limits.

---

## 21.10 Spectral Fredholm Theorem

The finite-volume spectrum corresponds precisely to the values of (E) for which the associated Fredholm determinant vanishes.

---

# Appendix 22 — Diagrammatic Expansions

## 22.1 Overview

Finite-volume quantization conditions originate from the resummation of infinitely many Feynman diagrams.

This appendix develops the diagrammatic foundations of the formalism.

---

## 22.2 Three-Particle Correlator

Consider

[
C_L(E)
======

\langle
\mathcal O
\mathcal O^\dagger
\rangle.
]

Its perturbative expansion contains all three-body intermediate states.

Diagrammatically,

[
C_L
===

\sum_{n=0}^{\infty}
C^{(n)}.
]

---

## 22.3 Skeleton Expansion

A skeleton decomposition expresses the correlator through:

* fully dressed propagators,
* two-body kernels,
* three-body kernels.

Symbolically,

[
C
=

G
+
GKG
+
GKGKG
+\cdots.
]

---

## 22.4 Spectator Topologies

The fundamental three-body topology is

[
(12)3.
]

Repeated rescattering generates

[
(12)3
\rightarrow
(23)1
\rightarrow
(31)2.
]

These spectator transitions define the dominant finite-volume contributions.

---

## 22.5 Finite-Volume Loops

The central geometric quantity is

[
\Delta_L
========

\frac1{L^3}
\sum_k
------

\int
\frac{d^3k}{(2\pi)^3}.
]

Every power-law finite-volume effect originates from this operator.

---

## 22.6 Ladder Diagrams

Repeated pairwise scattering generates ladder contributions:

[
K_2G_0K_2G_0K_2+\cdots.
]

Resummation yields

[
T_2
===

\frac{K_2}{1-K_2G_0}.
]

---

## 22.7 Three-Body Connected Diagrams

Connected diagrams cannot be factorized into two-body subamplitudes.

They define

[
K_3.
]

Examples include:

* triple-contact interactions,
* cyclic rescattering loops,
* irreducible triangle topologies.

---

## 22.8 Diagrammatic Origin of (F_3)

Summing all finite-volume loop corrections generates

[
F_3.
]

This operator contains no dynamical couplings.

It depends only on:

* geometry,
* volume,
* kinematics.

---

## 22.9 Diagrammatic Origin of (K_{\mathrm{df},3})

Removing singular pairwise contributions leaves

[
K_{\mathrm{df},3}.
]

This object is the diagrammatic representation of irreducible three-body dynamics.

---

## 22.10 Diagrammatic Reconstruction Theorem

Every finite-volume three-body quantization condition can be derived from a resummation of spectator-exchange diagram classes.

---

# Appendix 23 — Numerical Implementations

## 23.1 Introduction

Practical extraction of physical amplitudes from finite-volume spectra requires numerical realization of the theoretical framework.

This appendix outlines the principal computational methods.

---

## 23.2 Momentum-Lattice Truncation

The spectator momentum set

[
k
=

\frac{2\pi}{L}n
]

is infinite.

A cutoff

[
|k|<\Lambda
]

must be introduced.

The resulting matrix dimension is finite.

---

## 23.3 Partial-Wave Truncation

The expansion

[
\ell=0,1,2,\ldots
]

is truncated at

[
\ell_{\max}.
]

Near threshold,

[
\ell_{\max}=0
]

often provides a useful first approximation.

---

## 23.4 Matrix Representation

The quantization operator

[
Q_3(E)
======

I-G_3(\mathbb K_2+K_3)
]

is represented numerically as a finite matrix.

The spectrum is determined from

[
\det Q_3(E)=0.
]

---

## 23.5 Root-Finding Algorithms

Energy levels are obtained by solving

[
\det Q_3(E)=0.
]

Common methods include:

* Newton iteration,
* secant methods,
* contour integration,
* eigenvalue tracking.

---

## 23.6 Spectral Flow Analysis

As

[
L
]

varies, energy levels move continuously.

Tracking

[
E_n(L)
]

provides a powerful diagnostic for resonance identification.

---

## 23.7 Parameter Estimation

The kernel

[
K_{\mathrm{df},3}
]

is parameterized:

[
K_{\mathrm{df},3}
=================

\sum_i c_i O_i.
]

The coefficients

[
c_i
]

are extracted by fitting finite-volume spectra.

---

## 23.8 Bayesian Reconstruction

Modern lattice analyses frequently employ Bayesian inference.

Given measured levels

[
E_n^{\rm data},
]

one constructs

[
P(c_i|E_n).
]

Posterior distributions determine physical amplitudes and uncertainties.

---

## 23.9 Infinite-Volume Extrapolation

After determining

[
K_{\mathrm{df},3},
]

one solves the corresponding infinite-volume integral equations to reconstruct

[
\mathcal M_3(E).
]

Resonance poles are then obtained through analytic continuation.

---

## 23.10 High-Performance Computing

Three-body quantization conditions generate matrices containing millions of elements.

Efficient implementation requires:

* sparse linear algebra,
* Krylov methods,
* parallel diagonalization,
* GPU acceleration.

---

## 23.11 Numerical Stability Criterion

A numerical implementation is considered convergent when:

[
\frac{\partial E_n}
{\partial \Lambda}
\rightarrow0,
]

and

[
\frac{\partial E_n}
{\partial \ell_{\max}}
\rightarrow0.
]

---

## 23.12 Computational Reconstruction Theorem

Given sufficiently dense finite-volume spectral data and convergent numerical truncations, the complete physical three-body scattering amplitude may be reconstructed algorithmically.

---

# Technical Appendix Conclusions

The mathematical infrastructure underlying finite-volume three-body quantum field theory consists of three interconnected layers:

1. **Integral equations**, which encode the exact dynamical content of three-body scattering.

2. **Diagrammatic expansions**, which reveal how finite-volume geometry modifies relativistic quantum field dynamics and generate the quantization conditions.

3. **Numerical implementations**, which transform finite-volume spectra into physical observables through spectral inversion and amplitude reconstruction.

Together these appendices provide the rigorous analytical and computational foundation for the main results of Volume III. They establish finite-volume three-body QFT as a complete operator-theoretic, diagrammatic, and numerical framework capable of extracting physical three-body scattering information directly from compact-space spectra.
