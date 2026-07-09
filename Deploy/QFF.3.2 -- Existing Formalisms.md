# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume III — Three-Body Quantum Field Theory in Finite Volume

## Part II — Existing Formalisms

---

# 5. Hansen–Sharpe Formalism

## 5.1 Introduction

The first complete relativistic finite-volume three-body quantization condition was developed by

Maxwell Hansen

and

Stephen Sharpe.

Their work transformed the three-body problem from an unsolved conceptual obstacle into a mathematically well-defined field-theoretic framework.

The central achievement was the derivation of a finite-volume quantization condition relating three-particle energy levels to infinite-volume scattering quantities while maintaining relativistic covariance, exact finite-volume kinematics, and three-body unitarity.

---

## 5.2 Fundamental Challenge

For two particles, finite-volume effects arise from repeated propagation around compact dimensions.

For three particles, however:

* one particle may act as a spectator,
* pairwise interactions continuously rearrange,
* disconnected singularities appear,
* infinitely many rescattering topologies contribute.

Consequently the finite-volume spectrum cannot be described solely through ordinary two-body amplitudes.

---

## 5.3 Spectator Decomposition

The Hansen–Sharpe framework adopts a spectator representation.

At any stage of a scattering process:

[
(k,\ell,m)
]

labels:

* spectator momentum (k),
* pair angular momentum (\ell),
* magnetic quantum number (m).

The Hilbert space becomes

[
\mathcal H_{\rm spec}
=====================

{k,\ell,m}.
]

Finite-volume operators act on this enlarged space.

---

## 5.4 Two-Body Subsystem Dynamics

For fixed spectator momentum

[
k,
]

the remaining pair scatters through the ordinary two-body K-matrix:

[
\mathcal K_2(k).
]

Thus two-body physics enters as an essential building block.

However it is not sufficient.

---

## 5.5 Emergence of Genuine Three-Body Structure

Repeated pairwise rescattering generates contributions that cannot be represented solely through

[
\mathcal K_2.
]

A new irreducible object emerges:

[
\mathcal K_{\mathrm{df},3}.
]

The subscript

[
\mathrm{df}
]

denotes divergence free.

This quantity contains genuine three-body dynamics.

---

## 5.6 Finite-Volume Geometric Operator

As in two-body theory, compactification generates a universal geometric operator.

For three particles:

[
F_3.
]

Unlike the two-body function

[
F,
]

the operator

[
F_3
]

acts in spectator space.

Its structure is substantially more complicated.

---

## 5.7 Basic Philosophy

The finite-volume spectrum is determined by the interaction between:

1. Infinite-volume dynamics,
2. Finite-volume geometry.

This separation survives the transition from two-body to three-body systems.

---

## 5.8 Hansen–Sharpe Principle

Three-body finite-volume spectra are governed by a universal geometric operator coupled to an irreducible three-body interaction kernel.

This principle forms the foundation of all modern finite-volume three-body approaches.

---

# 6. Relativistic Field-Theoretic Derivation

## 6.1 Correlation Functions

The derivation begins with the finite-volume correlator

[
C_L(E)
======

\int d^4x,
e^{iEt}
\langle
\mathcal O(x)
\mathcal O^\dagger(0)
\rangle.
]

Finite-volume energies correspond to poles of

[
C_L.
]

---

## 6.2 Skeleton Expansion

The correlator is expanded into:

* dressed propagators,
* two-particle kernels,
* three-particle kernels.

Diagrammatically,

[
C_L
===

C^{(0)}
+
C^{(1)}
+
C^{(2)}
+\cdots.
]

Infinite classes of diagrams must be resummed.

---

## 6.3 Sum–Integral Difference

The key finite-volume effect arises from

[
\frac1{L^3}
\sum_k
------

\int
\frac{d^3k}{(2\pi)^3}.
]

This difference generates power-law finite-volume corrections.

All exponentially suppressed terms are discarded.

---

## 6.4 Spectator Pole Isolation

Singular finite-volume effects arise when one propagator goes on shell.

The corresponding momentum is identified as the spectator momentum:

[
k.
]

This observation motivates the spectator formalism.

---

## 6.5 Effective Finite-Volume Operator

Resumming all singular contributions yields

[
F_3.
]

This operator encodes:

* compactification,
* spectator propagation,
* pair rescattering.

No dynamical information enters its definition.

---

## 6.6 Infinite-Volume Kernel

After subtraction of finite-volume singularities one obtains

[
\mathcal K_{\mathrm{df},3}.
]

This quantity is independent of

[
L.
]

It contains all genuine three-body dynamics.

---

## 6.7 Exact Separation

The resulting structure mirrors two-body theory:

[
\text{Dynamics}
\longleftrightarrow
\mathcal K_{\mathrm{df},3},
]

[
\text{Geometry}
\longleftrightarrow
F_3.
]

This separation is the central conceptual achievement of the field-theoretic derivation.

---

## 6.8 Relativistic Consistency

The construction preserves:

* relativistic covariance,
* crossing symmetry,
* exact finite-volume kinematics,
* three-body unitarity.

No nonrelativistic approximations are required.

---

## 6.9 Field-Theoretic Reconstruction Principle

The finite-volume three-body spectrum is generated entirely from the interplay of a universal geometric operator and a divergence-free infinite-volume interaction kernel.

---

# 7. Divergence-Free K-Matrix

## 7.1 Motivation

The ordinary three-body scattering amplitude

[
\mathcal M_3
]

contains singularities arising from pairwise scattering processes.

These singularities obscure genuine three-body physics.

A subtraction procedure is therefore required.

---

## 7.2 Divergent Contributions

Consider repeated pair interactions:

[
(12)
\rightarrow
(23)
\rightarrow
(31).
]

The resulting amplitude contains disconnected poles.

These contributions diverge near two-body resonances.

---

## 7.3 Subtraction Procedure

Define

[
\mathcal K_{\mathrm{df},3}
]

by removing all pairwise divergent pieces from

[
\mathcal M_3.
]

Symbolically,

[
\mathcal M_3
============

\mathcal M_{\rm div}
+
\mathcal K_{\mathrm{df},3}.
]

---

## 7.4 Properties

The divergence-free kernel satisfies:

1. Finite at pair poles,
2. Infinite-volume quantity,
3. Independent of compactification,
4. Encodes irreducible three-body interactions.

---

## 7.5 Spectator Representation

In spectator space,

[
\mathcal K_{\mathrm{df},3}
==========================

\mathcal K_{\mathrm{df},3}
(k,\ell,m;
k',\ell',m').
]

It acts as an infinite-dimensional operator.

---

## 7.6 Isotropic Approximation

The simplest truncation assumes

[
\mathcal K_{\mathrm{df},3}
==========================

{\rm constant}.
]

This approximation has been widely used in practical lattice studies.

It captures leading three-body effects near threshold.

---

## 7.7 Beyond the Isotropic Limit

More generally:

[
\mathcal K_{\mathrm{df},3}
==========================

\sum_n
c_n
\mathcal O_n.
]

The coefficients

[
c_n
]

parameterize genuine three-body interactions.

---

## 7.8 Physical Interpretation

The kernel

[
\mathcal K_{\mathrm{df},3}
]

plays the same role in three-body theory that

[
K
]

plays in two-body scattering.

It is the fundamental dynamical object of finite-volume three-particle physics.

---

## 7.9 Divergence-Free Kernel Theorem

All finite-volume three-body energy levels depend upon the infinite-volume dynamics exclusively through

[
\mathcal K_{\mathrm{df},3}.
]

---

# 8. Quantization Conditions

## 8.1 Spectral Problem

Finite-volume energies correspond to poles of the three-particle correlator.

After resummation, these poles satisfy a determinant equation.

---

## 8.2 Hansen–Sharpe Quantization Condition

The central result is

[
\boxed{
\det
\Big[
\mathcal K_{\mathrm{df},3}^{-1}
+
F_3
\Big]
=====

0.

}
]

This equation generalizes the Lüscher relation to three particles.

---

## 8.3 Structure of the Determinant

The determinant acts over:

* spectator momentum,
* partial waves,
* cubic irreducible representations.

The space is formally infinite dimensional.

Practical calculations require truncation.

---

## 8.4 Two-Body Limit

When irreducible three-body interactions vanish:

[
\mathcal K_{\mathrm{df},3}
\rightarrow0,
]

the formalism reduces to repeated two-body scattering embedded in three-particle kinematics.

This provides a consistency check.

---

## 8.5 Threshold Expansion

Near

[
E=3m,
]

the determinant may be expanded systematically.

This yields threshold observables such as:

* three-body scattering lengths,
* effective-range parameters,
* bound-state properties.

---

## 8.6 Numerical Implementation

The practical procedure is:

1. Compute finite-volume spectra,
2. Construct (F_3),
3. Parameterize (\mathcal K_{\mathrm{df},3}),
4. Solve the determinant condition,
5. Fit parameters to spectral data.

---

## 8.7 Infinite-Volume Reconstruction

The finite-volume kernel is not itself observable.

One must reconstruct the physical amplitude

[
\mathcal M_3.
]

This requires solving integral equations relating

[
\mathcal K_{\mathrm{df},3}
]

to

[
\mathcal M_3.
]

The mapping remains one of the most technically demanding aspects of the formalism.

---

## 8.8 Present Limitations

Current implementations face several challenges:

* partial-wave truncation,
* coupled channels,
* resonant subchannels,
* spinful particles,
* numerical instability,
* four-body contamination.

These limitations motivate the developments of subsequent volumes.

---

## 8.9 Existing-Formalism Theorem

The Hansen–Sharpe framework provides the first mathematically consistent relativistic finite-volume three-body quantization condition. It establishes that finite-volume three-particle spectra are governed by a determinant equation involving a universal geometric operator and a divergence-free three-body interaction kernel.

---

# Conclusions of Part II

Modern finite-volume three-body theory rests upon the Hansen–Sharpe construction and its subsequent refinements. Through a relativistic field-theoretic derivation, the three-body spectrum is expressed in terms of two fundamental objects: the geometric finite-volume operator

[
F_3
]

and the divergence-free kernel

[
\mathcal K_{\mathrm{df},3}.
]

This achievement places three-body scattering on conceptual footing analogous to two-body Lüscher theory while simultaneously revealing the profound increase in complexity associated with genuine many-body dynamics.

The principal limitation of existing approaches is that they remain formulations rather than complete solutions. The relationship between (\mathcal K_{\mathrm{df},3}) and the physical scattering amplitude is indirect, coupled-channel extensions remain incomplete, and systematic treatment of higher-body sectors has not yet been achieved. These shortcomings define the frontier that the remainder of this volume seeks to overcome.
