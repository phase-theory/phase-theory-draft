# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

## Volume I — Foundations of Finite-Volume Quantum Field Theory

# Part V — Scattering Foundations

---

# 29. LSZ Reduction in Finite Volume

## 29.1 Motivation

The Lehmann–Symanzik–Zimmermann (LSZ) reduction formula provides the bridge between correlation functions and scattering amplitudes in infinite-volume quantum field theory.

The standard derivation assumes:

1. Asymptotic free states.
2. Continuous momentum spectra.
3. Infinite temporal and spatial extent.
4. Existence of an S-matrix.

None of these assumptions hold exactly in finite volume.

Consequently LSZ must be reformulated.

---

## 29.2 Failure of Asymptotic States

For compact spatial manifold

[
\Sigma,
]

particles repeatedly encounter one another.

A wave packet cannot permanently separate from interaction regions.

Thus the limits

[
t\rightarrow\pm\infty
]

do not generate genuinely free states.

The conventional scattering picture therefore ceases to be fundamental.

---

## 29.3 Spectral States as Fundamental Objects

Finite-volume theories possess exact energy eigenstates

[
|n,L\rangle.
]

These replace asymptotic particle states.

The complete dynamics are encoded in

[
{E_n(L),,Z_n(L)}.
]

---

## 29.4 Finite-Volume Reduction Formula

Let

[
C_N(x_1,\ldots,x_N)
===================

\langle0|
T{\phi(x_1)\cdots\phi(x_N)}
|0\rangle.
]

Insertion of a complete spectral basis yields

[
C_N
===

\sum_n
\frac{
\langle0|\phi|n\rangle
\langle n|\phi|0\rangle
}
{E_n}.
]

We define the finite-volume transition functional

[
\mathcal A_L
============

\lim_{\epsilon\to0}
\prod_i
(\Box_i+m_i^2)
C_N.
]

This quantity replaces the conventional scattering amplitude.

---

## 29.5 Spectral LSZ Theorem

**Theorem.**

For compact spatial manifolds, all observable transition information is recoverable from poles of finite-volume correlation functions.

The role played by asymptotic states in infinite volume is replaced by exact spectral states.

---

## 29.6 Decompactification Limit

As

[
L\rightarrow\infty,
]

spectral levels become dense and

[
\mathcal A_L
\rightarrow
\mathcal M,
]

where

[
\mathcal M
]

is the ordinary scattering amplitude.

Thus standard LSZ emerges as a singular limit of spectral LSZ.

---

# 30. Spectral Reconstruction Theorem

## 30.1 Central Question

Can one reconstruct the complete dynamics of a quantum field theory from finite-volume spectra?

This question lies at the heart of the entire finite-volume program.

---

## 30.2 Spectral Data Set

Define

[
\mathcal S
==========

{
E_n(L,\theta,g)
}.
]

The set contains:

* all energy levels,
* all volumes,
* all twists,
* all admissible geometries.

---

## 30.3 Inverse Spectral Problem

We seek a map

[
\mathcal S
\longrightarrow
\mathcal D,
]

where

[
\mathcal D
]

denotes complete dynamical information.

---

## 30.4 Reconstruction Hypothesis

We postulate:

[
\mathcal D
==========

F(\mathcal S).
]

All physical observables are functionals of spectral geometry.

---

## 30.5 Spectral Completeness Principle

The finite-volume spectrum contains all measurable information about the theory.

No additional asymptotic data are fundamentally required.

---

## 30.6 Reconstruction Theorem (Proposed)

Let

[
\mathcal S
==========

{E_n(L,\theta,g)}
]

be known for every compactification.

Then:

1. Correlation functions are uniquely determined.
2. Transition amplitudes are uniquely determined.
3. Bound-state properties are uniquely determined.
4. Infinite-volume scattering data are uniquely determined.

Therefore

[
\mathcal S
]

forms a complete observable basis.

---

## 30.7 Significance

Lüscher theory becomes merely the lowest-order manifestation of a more general spectral reconstruction principle.

---

# 31. Finite-Volume States

## 31.1 Exact Eigenstates

Finite-volume states satisfy

[
H_L|n,L\rangle
==============

E_n(L)|n,L\rangle.
]

The spectrum is discrete.

---

## 31.2 One-Particle States

For momentum label

[
k_n
===

\frac{2\pi n}{L},
]

[
|k_n\rangle
===========

a_n^\dagger|0\rangle.
]

---

## 31.3 Multi-Particle States

The exact basis consists of

[
|n_1,n_2,\ldots,n_N\rangle.
]

Interactions mix these states.

The physical eigenstates are

[
|\alpha,L\rangle.
]

---

## 31.4 Spectral Density

Define

[
\rho_L(E)
=========

\sum_n
\delta(E-E_n).
]

In finite volume,

[
\rho_L
]

is discrete.

---

## 31.5 State Geometry

Each state possesses volume dependence:

[
|n,L\rangle.
]

Volume becomes an intrinsic quantum number.

---

## 31.6 State Continuation Principle

Every finite-volume state continuously evolves into an infinite-volume scattering or bound state under decompactification.

---

# 32. Finite-Volume Transition Amplitudes

## 32.1 Matrix Elements

Physical observables arise from

[
\langle m,L|
\mathcal O
|n,L\rangle.
]

These quantities are directly measurable in lattice calculations.

---

## 32.2 Spectral Transition Functions

Define

[
T_{mn}(L)
=========

\langle m,L|
\mathcal O
|n,L\rangle.
]

These replace scattering amplitudes as primary observables.

---

## 32.3 Volume Dependence

The matrix elements satisfy

[
T_{mn}(L)
=========

T_{mn}^{(\infty)}
+
\Delta T_{mn}(L).
]

The correction encodes finite-volume dynamics.

---

## 32.4 Resonance Information

Resonances appear through avoided level crossings.

The finite-volume spectrum therefore directly records unstable particles.

---

## 32.5 Spectral Transition Principle

All scattering information is encoded in the geometry-dependent matrix

[
T_{mn}(L).
]

---

## 32.6 Generalized Amplitude Space

Finite-volume dynamics define an operator

[
\mathcal T_L
]

acting on the discrete spectral Hilbert space.

This operator becomes the S-matrix in the infinite-volume limit.

---

# 33. Finite-Volume Unitarity

## 33.1 Conventional Unitarity

Infinite-volume scattering satisfies

[
S^\dagger S=1.
]

This relation follows from probability conservation.

---

## 33.2 Absence of an S-Matrix

In finite volume,

[
S
]

does not exist fundamentally.

Therefore unitarity must be reformulated.

---

## 33.3 Spectral Evolution Operator

Define

[
U(t)
====

e^{-iH_L t}.
]

Since

[
H_L
===

H_L^\dagger,
]

one obtains

[
U^\dagger U=1.
]

---

## 33.4 Spectral Unitarity

Probability conservation becomes

[
\sum_n
|\langle n|
U(t)
|m\rangle|^2
============

1.

]

This relation defines finite-volume unitarity.

---

## 33.5 Transition Algebra

For spectral amplitudes

[
T_{mn},
]

unitarity implies

[
\operatorname{Im}T_{mn}
=======================

\sum_k
T_{mk}
T_{kn}^*.
]

The sum runs over discrete states.

---

## 33.6 Finite-Volume Optical Theorem

The optical theorem becomes

[
\operatorname{Im}
T_{nn}
======

\sum_k
|T_{nk}|^2.
]

This is the discrete analogue of the continuum result.

---

## 33.7 Unitarity Reconstruction Theorem

As

[
L\rightarrow\infty,
]

spectral unitarity converges to conventional S-matrix unitarity.

---

# 34. Finite-Volume Correspondence Principle

## 34.1 Statement

A complete finite-volume theory must reproduce ordinary quantum field theory when

[
L\rightarrow\infty.
]

This requirement serves as the analogue of the classical correspondence principle.

---

## 34.2 Spectral Convergence

Discrete eigenvalues satisfy

[
E_n(L)
\rightarrow
E.
]

The spectrum becomes continuous.

---

## 34.3 State Convergence

Finite-volume eigenstates satisfy

[
|n,L\rangle
\rightarrow
|p\rangle.
]

Momentum eigenstates emerge dynamically.

---

## 34.4 Correlator Convergence

For every local operator,

[
G_L(x)
\rightarrow
G_\infty(x).
]

---

## 34.5 Scattering Convergence

Finite-volume transition operators satisfy

[
\mathcal T_L
\rightarrow
\mathcal T_\infty.
]

The conventional S-matrix emerges.

---

## 34.6 Strong Correspondence Principle

**Principle.**

Every finite-volume observable possesses a well-defined decompactification limit that reproduces the corresponding infinite-volume observable.

---

## 34.7 Correspondence Theorem

Let

[
\mathcal O_L
]

be any renormalized finite-volume observable.

Then

[
\lim_{L\to\infty}
\mathcal O_L
============

\mathcal O_\infty.
]

Thus infinite-volume quantum field theory is recovered as the decompactified phase of finite-volume QFT.

---

## 34.8 Philosophical Consequence

The traditional hierarchy

[
\text{Infinite Theory}
\rightarrow
\text{Finite Approximation}
]

is replaced by

[
\text{Finite Theory}
\rightarrow
\text{Infinite Limit}.
]

Infinite-volume QFT becomes a limiting regime rather than the foundational theory.

---

# Conclusions of Part V

The conventional framework of scattering theory is reconstructed entirely within compact space. Asymptotic states are replaced by exact spectral states, scattering amplitudes by finite-volume transition operators, and S-matrix unitarity by spectral unitarity. The central object of the theory becomes the geometry-dependent spectrum

[
\mathcal S
==========

{E_n(L,\theta,g)},
]

from which correlation functions, transition amplitudes, resonance properties, and ultimately infinite-volume observables can be reconstructed.

The principal result of Part V is the formulation of a spectral foundation for scattering theory. Lüscher’s quantization condition appears as a special case of a broader reconstruction program in which finite-volume spectra are elevated to the status of primary observables. The correspondence theorem then guarantees that conventional quantum field theory emerges as the decompactification limit of this more general compact-space framework.

This concludes the main body of **Volume I — Foundations of Finite-Volume Quantum Field Theory**. The technical appendices that follow will develop the mathematical proofs underlying spectral geometry, compact operator theory, harmonic analysis, generalized LSZ reduction, and the spectral reconstruction program introduced throughout the volume.
