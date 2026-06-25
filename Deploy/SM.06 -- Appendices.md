# Appendices A–H

## Technical Supplement to

## Matrix Models Beyond BFSS and IKKT

---

# Appendix A

# Detailed Derivations of the Universal Matrix Action

## A.1 Bosonic Sector

Begin from the universal matrix coordinates

[
\mathbb X^M
===========

\mathbb X^M_A T^A
]

where

[
T^A
]

are generators of a matrix algebra.

Define

[
F^{MN}
======

i[\mathbb X^M,\mathbb X^N].
]

The simplest gauge-invariant action is

[
S_B
===

-\frac14
{\rm Tr}
(F_{MN}F^{MN}).
]

Substituting

[
F_{MN}
======

i[\mathbb X_M,\mathbb X_N]
]

gives

[
S_B
===

-\frac14
{\rm Tr}
([\mathbb X_M,\mathbb X_N]
[\mathbb X^M,\mathbb X^N]).
]

Variation yields

[
\delta S_B
==========

*

{\rm Tr}
\left(
[\mathbb X^N,
[\mathbb X_N,\mathbb X_M]]
\delta \mathbb X^M
\right).
]

Therefore the equations of motion are

[
[\mathbb X^N,
[\mathbb X_N,\mathbb X_M]]
==========================

0.

]

These generalize both BFSS and IKKT dynamics.

---

## A.2 Classical Matrix Vacua

A vacuum satisfies

[
[\mathbb X_M,\mathbb X_N]=0.
]

All matrices may therefore be simultaneously diagonalized,

[
\mathbb X_M
===========

U D_M U^{-1}.
]

The eigenvalues

[
\lambda_i^M
]

define emergent spacetime points.

Thus geometry emerges as the moduli space of commuting matrices.

---

# Appendix B

# Supersymmetry Algebra

## B.1 Universal Supercharge

Introduce fermions

[
\Theta.
]

Supersymmetry transformations are

[
\delta \mathbb X^M
==================

i\bar\epsilon\Gamma^M\Theta,
]

[
\delta\Theta
============

\frac12
[\mathbb X^M,\mathbb X^N]
\Gamma_{MN}\epsilon.
]

---

## B.2 Closure Calculation

Applying two transformations yields

[
[\delta_1,\delta_2]
\mathbb X^M.
]

After Fierz rearrangements,

[
[\delta_1,\delta_2]
\mathbb X^M
===========

v^N
[\mathbb X_N,\mathbb X^M],
]

where

[
v^N
===

2i\bar\epsilon_2
\Gamma^N
\epsilon_1.
]

The supersymmetry algebra closes into a gauge transformation.

---

## B.3 Large-N Supersymmetry

As

[
N\rightarrow\infty,
]

matrix commutators become Poisson brackets,

[
[A,B]
\rightarrow
i{A,B}.
]

The matrix supersymmetry algebra approaches the continuum supergravity algebra.

---

# Appendix C

# Matrix Compactification Theory

## C.1 Compact Matrix Coordinates

Compact dimensions satisfy

[
U_i
===

e^{iR_i X_i}.
]

Periodicity requires

[
U_iU_j
======

e^{i\theta_{ij}}
U_jU_i.
]

This defines a noncommutative torus.

---

## C.2 Effective Radius

The compactification radius is

[
R_i^2
=====

\frac1N
{\rm Tr}
(X_i^2).
]

Different radii correspond to different matrix vacua.

---

## C.3 Flux Quantization

Matrix flux is

[
F_{ij}
======

[X_i,X_j].
]

Quantization requires

[
\frac1{2\pi}
\int F
======

n.
]

The integer (n) determines the topological sector.

---

# Appendix D

# Emergent Metric Construction

## D.1 Spectral Metric

Define fluctuations

[
\delta X^\mu
============

## X^\mu

\langle X^\mu\rangle.
]

The emergent metric is

[
g_{\mu\nu}
==========

\frac1N
{\rm Tr}
(\delta X_\mu\delta X_\nu).
]

---

## D.2 Eigenvalue Geometry

Let

[
\lambda_i^\mu
]

be eigenvalues.

Distances are

[
d_{ij}^2
========

(\lambda_i^\mu-\lambda_j^\mu)
(\lambda_{i\mu}-\lambda_{j\mu}).
]

The continuum metric arises from the large-(N) limit of this spectral distance.

---

## D.3 Curvature Operator

Curvature originates from commutator fluctuations:

[
R_{\mu\nu\rho\sigma}
\sim
\left<
[X_\mu,X_\nu]
[X_\rho,X_\sigma]
\right>.
]

Flat spacetime corresponds to vanishing expectation value.

---

# Appendix E

# Large-N Proofs

## E.1 Planar Dominance

The partition function admits a genus expansion

[
Z
=

\sum_g
N^{2-2g}
Z_g.
]

As

[
N\rightarrow\infty,
]

only planar diagrams survive.

Therefore

[
Z
\approx
N^2 Z_0.
]

---

## E.2 Emergence of Continuum Geometry

The eigenvalue density

[
\rho_N(\lambda)
]

satisfies

[
\int d\lambda,
\rho_N(\lambda)
===============

N.
]

Define

[
\hat\rho
========

\frac{\rho_N}{N}.
]

The limit

[
\lim_{N\to\infty}
\hat\rho
========

\rho
]

produces a continuous manifold.

---

## E.3 Large-N Factorization

Connected correlators satisfy

[
\langle AB\rangle
=================

\langle A\rangle
\langle B\rangle
+
O(N^{-2}).
]

This implies classical behavior emerges at infinite rank.

---

# Appendix F

# Anomaly Calculations

## F.1 Gauge Variation

Under

[
\delta A
========

D\Lambda,
]

the effective action transforms as

[
\delta \Gamma
=============

\int
{\rm Tr}
(\Lambda, \mathcal A).
]

Consistency requires

[
\mathcal A=0.
]

---

## F.2 Matrix Green–Schwarz Mechanism

Introduce matrix two-form fields

[
B_{MN}.
]

Their variation is

[
\delta B
========

\omega_2.
]

The anomaly-canceling term becomes

[
S_{GS}
======

{\rm Tr}
(BX_8).
]

---

## F.3 Factorization Condition

The anomaly polynomial must factorize:

[
I_{12}
======

X_4X_8.
]

This reproduces the standard Green–Schwarz structure in the continuum limit.

---

## F.4 Exceptional Sector Constraints

For the proposed (E_8\times E_8) phase,

[
{\rm Tr}(F^6)
=============

\alpha
{\rm Tr}(F^4)
{\rm Tr}(F^2)
+
\beta
({\rm Tr}(F^2))^3.
]

Only representations satisfying this relation remain anomaly-free.

---

# Appendix G

# Numerical Algorithms and Monte Carlo Framework

## G.1 Hybrid Monte Carlo

Introduce conjugate momenta

[
P_M.
]

The simulation Hamiltonian is

[
H
=

\frac12
{\rm Tr}(P_M^2)
+
S[X].
]

Leapfrog integration preserves symplectic structure.

---

## G.2 Observable Extraction

Key observables include

[
D_{\rm eff},
]

[
I=n_L-n_R,
]

and

[
G_{\rm vac}.
]

These determine dimensionality, chirality, and gauge symmetry.

---

## G.3 Computational Scaling

Naively,

[
{\rm Cost}
\sim
N^5.
]

Block-diagonal algorithms reduce this toward

[
N^3.
]

This is essential for phenomenological exploration.

---

# Appendix H

# Universal Matrix Phase Diagram

## H.1 Order Parameters

The proposed theory possesses three primary order parameters:

[
D_{\rm eff}
]

(emergent dimension),

[
G_{\rm vac}
]

(gauge symmetry),

and

[
I
]

(chiral index).

---

## H.2 Phase Structure

Different regions of parameter space correspond to

[
{\text{IIA},\text{IIB},\text{I},
\text{SO(32)},
E_8\times E_8}.
]

These are interpreted as phases rather than distinct fundamental theories.

---

## H.3 Universal Matrix Conjecture

The complete non-perturbative phase space is

[
\mathcal U
==========

\bigcup_i
\mathcal P_i,
]

where each

[
\mathcal P_i
]

is a string-theoretic phase.

The conjecture underlying the present work is that all physically admissible quantum-gravitational vacua reside within (\mathcal U).

---

# Appendix Summary

The appendices establish the technical backbone of the proposed framework:

* Derivation of the master matrix equations of motion.
* Closure of the generalized supersymmetry algebra.
* Matrix compactification through noncommutative toroidal sectors.
* Spectral construction of emergent metrics and curvature.
* Large-(N) arguments for continuum geometry.
* Generalized Green–Schwarz anomaly cancellation.
* Numerical algorithms for simulation.
* A universal phase diagram unifying BFSS, IKKT, Type I, SO(32), and (E_8\times E_8) sectors.

Together they define a candidate mathematical architecture for a universal matrix formulation extending beyond currently known matrix models.
