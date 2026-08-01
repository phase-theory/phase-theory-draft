# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume II — Two-Body Scattering and the Generalized Lüscher Framework

## Technical Appendices

---

# Appendix 25 — Detailed Derivations

## 25.1 Introduction

The purpose of this appendix is to provide the mathematical derivations underlying the quantization conditions developed throughout Volume II.

The central result is the emergence of finite-volume spectral equations from the exact Bethe–Salpeter framework.

---

## 25.2 Bethe–Salpeter Equation

Consider the connected four-point function

[
G_4
===

G_0
+
G_0 K G_4,
]

where

[
G_0
]

is the disconnected two-particle propagator and

[
K
]

is the Bethe–Salpeter kernel.

Iterating gives

[
G_4
===

G_0
+
G_0KG_0
+
G_0KG_0KG_0
+\cdots.
]

Formally,

[
G_4
===

(1-G_0K)^{-1}G_0.
]

Poles occur when

[
\det(1-G_0K)=0.
]

---

## 25.3 Finite-Volume Replacement

Compactification replaces momentum integrals by sums:

[
\int\frac{d^3q}{(2\pi)^3}
\rightarrow
\frac1{L^3}
\sum_q.
]

Thus

[
G_0
\rightarrow
G_{0,L}.
]

The finite-volume pole condition becomes

[
\det
(1-G_{0,L}K)
============

0.

]

---

## 25.4 Separation of Infinite- and Finite-Volume Parts

Write

[
G_{0,L}
=======

G_{0,\infty}
+
\Delta G_L.
]

Then

[
1-G_{0,L}K
==========

(1-G_{0,\infty}K)
\Big[
1-
(1-G_{0,\infty}K)^{-1}
\Delta G_L K
\Big].
]

Taking determinants yields

[
\det
\Big[
1+\mathcal M F_L
\Big]
=====

0.

]

This is the generalized Lüscher quantization condition.

---

## 25.5 Partial-Wave Projection

The scattering amplitude admits the expansion

[
\mathcal M(k,\hat p,\hat p')
============================

4\pi
\sum_{\ell m}
Y_{\ell m}(\hat p)
\mathcal M_\ell(k)
Y_{\ell m}^\ast(\hat p').
]

Projection yields

[
\mathcal M_{\ell\ell'}.
]

Finite-volume symmetry reduction generates off-diagonal terms.

---

## 25.6 Coupled-Channel Derivation

Introduce channel indices

[
\alpha,\beta.
]

The amplitude becomes

[
\mathcal M_{\alpha\beta}.
]

The quantization condition generalizes to

[
\det
\Big[
\mathcal M^{-1}
+
F
\Big]
=====

0.

]

The determinant now acts simultaneously in:

1. Channel space,
2. Partial-wave space,
3. Cubic-irrep space.

---

## 25.7 Bound-State Derivation

Near a bound-state pole,

[
\mathcal M(E)
=============

\frac{g_B^2}
{E_B-E}
+\cdots.
]

Substituting into the quantization condition yields

[
E_B(L)-E_B
\propto
e^{-\kappa L}.
]

Thus exponential finite-volume corrections emerge directly from pole structure.

---

## 25.8 Moving-Frame Derivation

For

[
P
=

\frac{2\pi}{L}d,
]

the Lorentz factor is

[
\gamma
======

\frac{E}{E^\ast}.
]

The summation lattice transforms as

[
r
=

\gamma^{-1}
(n-\alpha d).
]

Substitution into the finite-volume loop function yields the Rummukainen–Gottlieb quantization condition.

---

## 25.9 Determinant Universality

All two-body finite-volume quantization conditions derived in this volume reduce to

[
\boxed{
\det
\left[
\mathcal M^{-1}
+
F
\right]
=======

0
}
]

with the geometric operator

[
F
]

specialized to the relevant compactification.

---

# Appendix 26 — Pole Structure Analysis

## 26.1 Analytic Structure of Scattering Amplitudes

Scattering amplitudes are analytic functions of

[
s=E^2
]

except at singularities.

These singularities encode all physical information.

---

## 26.2 Classification of Singularities

The principal singularities are:

1. Bound-state poles,
2. Resonance poles,
3. Virtual-state poles,
4. Branch points,
5. Multi-particle cuts.

---

## 26.3 Bound-State Poles

Bound states satisfy

[
s_B
<
s_{\rm th}.
]

The amplitude behaves as

[
\mathcal M
\sim
\frac{g_B^2}
{s_B-s}.
]

These poles occur on the physical sheet.

---

## 26.4 Resonance Poles

Resonances occur on unphysical sheets:

[
s_R
===

(M_R-i\Gamma_R/2)^2.
]

Near the pole,

[
\mathcal M
\sim
\frac{g_R^2}
{s_R-s}.
]

---

## 26.5 Virtual States

Virtual states lie below threshold but on unphysical sheets.

They satisfy

[
k=-i\kappa.
]

These states frequently arise in near-threshold systems.

---

## 26.6 Branch Points

Each channel threshold generates a branch point:

[
s=s_{\rm th}.
]

The amplitude contains square-root behavior:

[
k
=

\sqrt{s-s_{\rm th}}.
]

---

## 26.7 Riemann-Sheet Structure

For

[
N
]

channels, the amplitude possesses

[
2^N
]

Riemann sheets.

Pole locations must always be specified relative to a particular sheet.

---

## 26.8 Finite-Volume Pole Reconstruction

Finite-volume spectra determine:

[
\mathcal M(E)
]

along the real axis.

Analytic continuation reconstructs the full singularity structure.

---

## 26.9 Pole Reconstruction Theorem

Given a sufficiently complete set of finite-volume energy levels

[
{E_n(L)},
]

the complete set of isolated poles of the two-body scattering amplitude is uniquely recoverable.

---

## 26.10 Spectral–Pole Correspondence

There exists a one-to-one correspondence between:

[
\text{Spectral trajectories}
]

and

[
\text{Analytic singularities}.
]

This correspondence underlies inverse finite-volume scattering theory.

---

# Appendix 27 — Numerical Algorithms

## 27.1 Overview

Practical finite-volume spectroscopy requires efficient numerical extraction of scattering amplitudes from spectral data.

This appendix develops algorithms suitable for large-scale implementation.

---

## 27.2 Input Data

Assume measured energies

[
E_n(L_i,P_j,\Lambda_k).
]

The dataset contains:

* volumes,
* momentum sectors,
* irreducible representations.

---

## 27.3 Center-of-Mass Reconstruction

For each level compute

[
E^\ast
======

\sqrt{E^2-P^2}.
]

Then evaluate

[
k^\ast
======

\sqrt{
\frac{E^{\ast2}}4
-m^2
}.
]

---

## 27.4 Evaluation of Zeta Functions

Generalized zeta functions satisfy

[
Z_{lm}(s;q^2)
=============

\sum_n
\frac{
Y_{lm}(n)
}{
(n^2-q^2)^s
}.
]

Direct summation converges slowly.

---

### Ewald Acceleration

Split

[
Z_{lm}
======

Z_{lm}^{\rm short}
+
Z_{lm}^{\rm long}.
]

This produces exponential convergence.

---

## 27.5 Quantization Residual

Define

[
R(E,\theta)
===========

\det
\Big[
\mathcal M^{-1}(E;\theta)
+
F(E,L)
\Big].
]

Model parameters

[
\theta
]

are determined by minimizing

[
\chi^2
======

\sum_n
R_n^2.
]

---

## 27.6 K-Matrix Fitting

A common parametrization is

[
K(E)
====

\sum_a
\frac{g_a^2}
{m_a^2-E^2}
+
\sum_k c_k E^{2k}.
]

The fitted K-matrix yields

[
\mathcal M(E).
]

---

## 27.7 Pole Search Algorithm

After fitting:

1. Construct

[
\mathcal M(E).
]

2. Continue into complex energy.

3. Search for

[
\det \mathcal M^{-1}(E)=0.
]

4. Identify resonance poles.

---

## 27.8 Multi-Channel Optimization

For coupled channels:

[
\mathcal M
\rightarrow
\mathcal M_{\alpha\beta}.
]

Optimization employs matrix-valued residuals.

Typical methods include:

* Newton iteration,
* Levenberg–Marquardt,
* Bayesian inference,
* Hamiltonian Monte Carlo.

---

## 27.9 Spectral Reconstruction Pipeline

The complete algorithm is:

[
{E_n}
\rightarrow
E^\ast
\rightarrow
F
\rightarrow
K
\rightarrow
\mathcal M
\rightarrow
\text{Poles}.
]

---

## 27.10 Complexity Estimates

For

[
N_E
]

energy levels and

[
N_p
]

fit parameters,

matrix evaluation scales approximately as

[
\mathcal O(N_E N_p^2).
]

Parallelization over irreps and momentum sectors is straightforward.

---

## 27.11 Numerical Stability Criterion

Stable reconstruction requires:

[
N_E
\gg
N_p.
]

Over-parameterized amplitudes produce nonphysical poles and poor predictive power.

---

## 27.12 Universal Reconstruction Algorithm

Any two-body finite-volume scattering problem can be solved numerically through repeated evaluation of the determinant equation

[
\boxed{
\det
\left[
\mathcal M^{-1}
+
F
\right]
=======

0.

}
]

The distinction between elastic, coupled-channel, moving-frame, and generalized compactification problems lies entirely in the construction of the geometric operator

[
F.
]

---

# Concluding Remarks on Volume II

Volume II has developed the complete modern theory of two-body scattering in finite-volume quantum field theory. Beginning with exact two-particle states and the Bethe–Salpeter formalism, the analysis progressed through generalized Lüscher quantization, moving-frame dynamics, coupled-channel scattering, resonance reconstruction, bound-state spectroscopy, and geometric generalizations beyond cubic compactifications.

The technical appendices have shown that all formulations are manifestations of a single determinant framework connecting finite-volume spectra to infinite-volume amplitudes. The resulting theory provides a mathematically unified description of elastic scattering, inelastic transitions, resonances, composite particles, and generalized compact-space dynamics.

Most importantly, the formalism reveals that finite-volume spectra are not merely computational intermediaries. They constitute a complete physical observable from which scattering amplitudes, analytic structures, and dynamical singularities may be reconstructed. This perspective prepares the transition to Volume III, where the genuine frontier of finite-volume quantum field theory begins: the systematic treatment of three-body and many-body dynamics beyond the reach of traditional Lüscher methods.
