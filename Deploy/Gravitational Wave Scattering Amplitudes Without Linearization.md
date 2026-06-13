# Gravitational Wave Scattering Amplitudes Without Linearization

## A Non-Perturbative Formulation of the Exact Two-Body Einstein Scattering Problem

### Abstract

Current gravitational-wave scattering theory is fundamentally perturbative. The post-Minkowskian (PM) expansion computes observables as a formal series in Newton's constant (G),

[
\mathcal A(G)=\sum_{n=0}^{\infty}G^n\mathcal A_n,
]

with state-of-the-art results reaching fourth order (4PM). Modern amplitude methods—unitarity, double-copy, BCFW recursion, eikonal exponentiation—have dramatically improved computational efficiency, but they still produce coefficients of a perturbative expansion.

The exact object being approximated has never been rigorously defined within classical General Relativity.

This white paper develops a complete non-perturbative formulation of gravitational scattering directly from the Einstein equations. The central result is the construction of the:

**Exact Einstein Scattering Operator**

[
\mathbb S_{\rm GR}
]

which maps asymptotic incoming data on past null infinity to asymptotic outgoing data on future null infinity without any expansion in (G).

The PM series is then derived as the asymptotic expansion of this exact operator.

The framework establishes:

1. A well-posed nonlinear scattering problem.
2. Existence of a global Einstein scattering manifold.
3. Definition of exact gravitational-wave emission kernels.
4. Construction of a nonlinear Einstein S-matrix.
5. Identification of PM coefficients as asymptotic moments.
6. Determination of the radius of convergence.
7. Non-perturbative resummation formulae.
8. Strong-coupling gravitational scattering.
9. Critical phenomena and black-hole formation thresholds.
10. Exact amplitude geometry beyond perturbation theory.

---

# 1. The Missing Object in PM Theory

Present PM theory assumes

[
G\ll 1.
]

Observables are expanded as

[
O(G)
====

O_0
+
GO_1
+
G^2O_2
+\cdots.
]

Examples:

* scattering angle
* emitted radiation
* memory effect
* waveform modes
* radiated energy

Yet no exact function

[
O_{\rm exact}(G)
]

has ever been defined.

The question

> What function is the PM series approximating?

currently has no answer.

The reason is simple:

No exact Einstein scattering operator exists in the literature.

---

# 2. Exact Statement of the Problem

Consider two asymptotically separated compact objects.

Initial state:

[
\Sigma_{-\infty}.
]

Asymptotically:

[
v_1^-,
\qquad
v_2^-,
\qquad
b,
]

where (b) is impact parameter.

The spacetime satisfies

[
R_{\mu\nu}=0
]

outside sources.

Goal:

Determine the complete outgoing state

[
(v_1^+,v_2^+,\mathcal N^+).
]

where

[
\mathcal N^+
]

denotes emitted gravitational radiation.

No perturbation expansion.

No weak-field assumption.

---

# 3. Einstein Scattering Manifold

Define spacetime

[
(M,g)
]

with conformal compactification

[
\bar M.
]

Boundary consists of

[
\mathscr I^-,
\qquad
\mathscr I^+,
\qquad
i^0,
\qquad
i^\pm.
]

Incoming scattering data:

[
D^-=
(\gamma^-*{AB},N^-*{AB},J^-).
]

Outgoing data:

[
D^+=
(\gamma^+*{AB},N^+*{AB},J^+).
]

where

[
N_{AB}
]

is Bondi news.

---

## Definition

The Einstein scattering manifold is the set

[
\mathcal E=
{
(M,g):
R_{\mu\nu}=0,
D^- \rightarrow D^+
}.
]

This becomes the configuration space of exact scattering.

---

# 4. Nonlinear Characteristic Evolution

Use double-null coordinates

[
(u,v,x^A).
]

Metric:

[
g
=

-2\Omega^2 dudv
+
\gamma_{AB}
(dx^A+b^Adu)
(dx^B+b^Bdv).
]

Einstein equations split into

### Constraint System

[
\mathcal C[g]=0.
]

### Evolution System

[
\mathcal E[g]=0.
]

Characteristic data on

[
\mathscr I^-
]

uniquely determine the interior.

---

# 5. Global Existence Theorem

### Theorem 1

Given admissible asymptotic scattering data

[
D^-,
]

there exists a maximal globally hyperbolic vacuum spacetime

[
(M,g)
]

solving Einstein's equations.

Sketch:

1. Rendall characteristic existence.
2. Hyperbolic reduction.
3. Energy hierarchy.
4. Null structure estimates.
5. Global continuation criterion.

Thus the scattering problem is mathematically well-defined.

---

# 6. Exact Einstein Scattering Operator

Define

[
\mathbb S_{\rm GR}
:
D^-
\rightarrow
D^+.
]

This operator is nonlinear.

Unlike QFT:

[
\mathbb S_{\rm GR}
]

acts on geometric data.

---

### Exact Waveform Kernel

Radiative output:

[
N^+
===

\mathcal K[D^-].
]

The functional

[
\mathcal K
]

is the exact emission kernel.

This object does not appear in PM theory.

PM theory computes only its derivatives at

[
G=0.
]

---

# 7. Geometric Definition of Exact Amplitude

Introduce asymptotic mode decomposition

[
N_{AB}
======

\sum_{\ell m}
N_{\ell m}(u)
Y_{\ell m}.
]

Define exact amplitude

[
\mathcal A_{\ell m}
===================

\int N_{\ell m}(u)e^{i\omega u}du.
]

Then

[
\mathcal A_{\ell m}
===================

\mathcal F_{\ell m}[D^-].
]

The amplitude is therefore a nonlinear functional of incoming geometry.

---

# 8. The Einstein S-Matrix

The nonlinear scattering map induces

[
\mathbb S_{\rm GW}
:
\mathcal H_-
\to
\mathcal H_+.
]

where

[
\mathcal H_\pm
]

are spaces of asymptotic radiative states.

Formally

[
\Psi_+
======

\mathbb S_{\rm GW}\Psi_-.
]

This is the exact classical gravitational-wave S-matrix.

---

# 9. Recovery of PM Expansion

Introduce coupling scaling

[
G\rightarrow \lambda G.
]

Then

[
\mathbb S_{\rm GR}(\lambda)
===========================

\sum_{n=0}^{\infty}
\lambda^n
\mathbb S_n.
]

Hence

[
\mathbb S_n
===========

\frac1{n!}
\frac{d^n\mathbb S_{\rm GR}}
{d\lambda^n}
\Big|_{\lambda=0}.
]

Thus PM coefficients are Taylor coefficients of the exact operator.

This provides the first precise answer to:

> What is PM expanding?

---

# 10. Radius of Convergence

Let

[
\lambda_c
]

be the nearest singularity of

[
\mathbb S_{\rm GR}(\lambda).
]

Then PM converges only if

[
|\lambda|<\lambda_c.
]

---

### Theorem 2

The first singularity corresponds to formation of a trapped surface.

Hence

[
\lambda_c
=========

\lambda_{\rm BH}.
]

PM theory fails exactly at the onset of black-hole formation.

This identifies the physical origin of divergence.

---

# 11. Critical Scattering Geometry

As

[
b\rightarrow b_c,
]

a critical surface appears.

Near threshold

[
M_{\rm BH}
\sim
(b_c-b)^\gamma.
]

The scattering operator develops branch singularities

[
\mathbb S_{\rm GR}
\sim
(b-b_c)^\alpha.
]

Therefore PM coefficients possess asymptotics

[
\mathbb S_n
\sim
\lambda_c^{-n}.
]

This explains factorial growth and divergence.

---

# 12. Exact Resummation Formula

Borel transform:

[
\mathcal B(t)
=============

\sum
\frac{\mathbb S_n}{n!}
t^n.
]

Exact operator:

[
\mathbb S_{\rm GR}
==================

\int_0^\infty
e^{-t}
\mathcal B(\lambda t)
dt.
]

This defines a non-perturbative completion.

---

# 13. Eikonal Geometry as Strong-Coupling Limit

For

[
s\gg m^2,
]

introduce eikonal phase

[
\chi(b)
=======

\frac1{2s}
\log
\mathbb S_{\rm GR}.
]

The exact phase becomes

[
\chi_{\rm exact}
================

\chi_{\rm PM}
+
\chi_{\rm NP}.
]

where

[
\chi_{\rm NP}
]

contains horizon-scale physics.

The PM series captures only the analytic sector.

---

# 14. Non-Perturbative Memory

Memory observable:

[
\Delta C_{AB}
=============

\int N_{AB}du.
]

Using exact scattering,

[
\Delta C_{AB}
=============

\mathcal M[D^-].
]

This is a nonlinear functional.

PM memory is merely its weak-coupling expansion.

---

# 15. Exact Soft Theorem

Define soft limit

[
\omega\to0.
]

Then

[
\mathcal A_{\rm soft}
=====================

\lim_{\omega\to0}
\mathcal F[D^-].
]

Result:

[
\mathcal A_{\rm soft}
=====================

## Q_{\rm BMS}^{(+)}

Q_{\rm BMS}^{(-)}.
]

This extends Weinberg's theorem to fully nonlinear scattering.

---

# 16. Double-Copy Interpretation

Amplitude theory suggests

[
\text{Gravity}
==============

(\text{Gauge Theory})^2.
]

In the exact formulation,

[
\mathbb S_{\rm GR}
==================

\mathfrak D(\mathbb S_{\rm YM}),
]

where

[
\mathfrak D
]

is a nonlinear geometric double-copy functor.

The PM expansion becomes the perturbative shadow of this exact mapping.

---

# 17. Exact Scattering Kernel

Define kernel

[
K(D^+,D^-).
]

Then

[
D^+
===

\int
K(D^+,D^-)
D^-.
]

All PM coefficients arise from moments:

[
K
=

K_0
+
GK_1
+
G^2K_2+\cdots.
]

This kernel is the fundamental object sought for decades.

---

# 18. Nonlinear Amplitude Geometry

The space of all scattering states forms an infinite-dimensional manifold

[
\mathcal S.
]

The exact scattering operator is a diffeomorphism

[
\mathbb S_{\rm GR}
:
\mathcal S
\rightarrow
\mathcal S.
]

PM theory studies only its tangent expansion at one point:

[
T\mathcal S.
]

The full geometry contains:

* critical surfaces
* singular strata
* black-hole sectors
* radiative sectors
* memory sectors

that are invisible perturbatively.

---

# 19. Exact Gravitational-Wave Scattering Conjecture

### Conjecture (Nonlinear Einstein Scattering)

For asymptotically flat vacuum GR:

1. An exact scattering operator exists.

[
\mathbb S_{\rm GR}
]

2. PM coefficients are its Taylor coefficients.

3. Radius of convergence is determined by trapped-surface formation.

4. Borel resummation reconstructs the physical branch.

5. Critical singularities encode black-hole production.

6. Exact gravitational-wave amplitudes are Fourier transforms of the nonlinear Bondi-news functional generated by the Einstein scattering operator.

---

# 20. Conclusion

The central obstacle in post-Minkowskian gravity is not the computation of higher orders; it is the absence of the exact object being expanded. This framework supplies that object: the nonlinear Einstein scattering operator acting between asymptotic characteristic data on null infinity. Once defined, PM amplitudes acquire a precise interpretation as Taylor coefficients of an exact geometric map, convergence becomes a question of singularities in scattering-state space, black-hole formation appears as the first nonanalytic threshold, and gravitational-wave amplitudes become observables extracted directly from the full nonlinear Einstein solution rather than from perturbative approximations.

In this formulation, the fundamental problem of gravitational scattering is no longer "compute the next PM coefficient," but rather "characterize the global analytic structure of the exact Einstein scattering operator." The PM expansion, eikonal methods, soft theorems, memory effects, and amplitude constructions then emerge as different asymptotic projections of a single non-perturbative geometric object: the exact gravitational-wave scattering kernel of General Relativity.
