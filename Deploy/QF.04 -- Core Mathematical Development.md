# The Operator Product Expansion Beyond Perturbation Theory

## Volume IV — Core Mathematical Development

### Parts 16–21

---

# 16. Spectral Construction of OPE Coefficients

## 16.1 Objective

Volumes I–III proposed that the OPE is fundamentally a spectral decomposition in operator space.

The next task is to construct the coefficient functions directly from exact spectral data.

Let

[
H|n\rangle = E_n|n\rangle
]

with

[
0 = E_0 < E_1 < E_2 < \cdots .
]

The complete physical information of the theory is encoded in

[
\mathcal S
==========

\left{
E_n,
\langle m|\mathcal O_A|n\rangle
\right}.
]

NOET seeks a map

[
\mathcal S
\longrightarrow
C_{AB}^{;;C}(x).
]

---

## 16.2 Bilocal Product Operator

Define

[
\mathcal B_{AB}(x)
==================

\mathcal O_A(x)\mathcal O_B(0).
]

Using Heisenberg evolution,

[
\mathcal O_A(x)
===============

e^{iP\cdot x}
\mathcal O_A(0)
e^{-iP\cdot x}.
]

Insert spectral completeness:

[
\mathbf 1
=========

\sum_n |n\rangle\langle n|.
]

Then

[
\mathcal B_{AB}(x)
==================

\sum_n
e^{-ip_n\cdot x}
\mathcal O_A(0)
|n\rangle
\langle n|
\mathcal O_B(0).
]

---

## 16.3 Operator Basis

Let

[
{\mathcal O_C}
]

denote a complete orthonormal operator basis in (\mathcal H_O).

Define

[
(\mathcal O_A,\mathcal O_B)
===========================

\langle0|
\mathcal O_A^\dagger
\mathcal O_B
|0\rangle.
]

Then

[
(\mathcal O_C,\mathcal O_D)
===========================

\delta_{CD}.
]

The OPE coefficient is identified with the projection

[
C_{AB}^{;;C}(x)
===============

(\mathcal O_C,\mathcal B_{AB}(x)).
]

---

## 16.4 Spectral Formula

Substituting the spectral decomposition yields

[
C_{AB}^{;;C}(x)
===============

\sum_n
e^{-ip_n\cdot x}
\Xi_{AB,n}^{;;;;C},
]

where

[
\Xi_{AB,n}^{;;;;C}
==================

\langle0|
\mathcal O_C^\dagger
\mathcal O_A
|n\rangle
\langle n|
\mathcal O_B
|0\rangle.
]

This is the central spectral representation of NOET.

---

## 16.5 Euclidean Representation

After Wick rotation,

[
t\rightarrow -i\tau,
]

we obtain

[
C_{AB}^{;;C}(r)
===============

\sum_n
e^{-E_n r}
\Xi_{AB,n}^{;;;;C}.
]

The coefficient functions become Laplace transforms of exact spectral data.

---

## 16.6 Spectral Measure Form

Introduce

[
d\mu_{AB}^{;;C}(E)
==================

\sum_n
\Xi_{AB,n}^{;;;;C}
\delta(E-E_n)dE.
]

Then

[
\boxed{
C_{AB}^{;;C}(r)
===============

\int_0^\infty
e^{-Er}
d\mu_{AB}^{;;C}(E).
}
]

The OPE coefficient is therefore a spectral transform.

---

# 17. Convergence Theorems

## 17.1 The Convergence Problem

The central unresolved question of OPE theory is whether

[
\sum_C
C_{AB}^{;;C}(x)
\mathcal O_C
]

converges.

NOET converts this into a problem of spectral growth.

---

## 17.2 Spectral Growth Function

Define

[
N(E)
====

#{E_n<E}.
]

Suppose

[
N(E)
\sim
e^{\alpha E}.
]

Then

[
\rho(E)
=======

\frac{dN}{dE}
]

determines asymptotic state density.

---

## 17.3 Theorem 1 (Spectral OPE Convergence)

Assume

[
|\Xi_{AB,n}^{;;;;C}|
<
Ke^{-\beta E_n}
]

for some

[
\beta>0.
]

Then

[
\sum_n
e^{-E_n r}
\Xi_{AB,n}^{;;;;C}
]

converges absolutely whenever

[
r+\beta>\alpha.
]

### Proof

Estimate

[
|C|
\le
K
\sum_n
e^{-(r+\beta)E_n}.
]

Approximating by the density of states:

[
|C|
\le
K
\int_0^\infty
\rho(E)
e^{-(r+\beta)E}
dE.
]

Since

[
\rho(E)
\sim e^{\alpha E},
]

the integral converges if

[
r+\beta>\alpha.
]

QED.

---

## 17.4 Corollary

Convergence is governed not by coupling constants but by the competition between:

1. spectral growth,
2. overlap suppression.

This is a fundamentally nonperturbative criterion.

---

## 17.5 Theorem 2 (Compact Operator Product)

Under Postulate NOET-2,

[
M:
\mathcal H_O\otimes\mathcal H_O
\rightarrow
\mathcal H_O
]

is compact.

Therefore

[
M
=

\sum_n
\sigma_n
|u_n\rangle\langle v_n|.
]

The OPE becomes

[
\mathcal O_A\mathcal O_B
========================

\sum_n
\sigma_n
u_n.
]

Since

[
\sigma_n\rightarrow0,
]

the expansion converges in operator norm.

QED.

---

## 17.6 Interpretation

The OPE becomes mathematically analogous to:

* Fourier expansions,
* spectral decompositions,
* singular-value expansions.

Convergence is no longer mysterious.

It is controlled by compactness and spectral decay.

---

# 18. Radius of Convergence and Analytic Domains

## 18.1 Traditional Problem

Perturbative OPE theory provides no universal radius of convergence.

NOET identifies the radius spectrally.

---

## 18.2 Analytic Continuation

The Laplace representation

[
C(r)
====

\int_0^\infty
e^{-Er}
d\mu(E)
]

defines an analytic function for

[
\Re(r)>0.
]

Singularities arise from the spectral measure.

---

## 18.3 Spectral Singularity Set

Define

[
\Sigma
======

{s_k}.
]

These singular points correspond to:

* thresholds,
* bound-state poles,
* branch cuts,
* topological sectors.

---

## 18.4 Definition of OPE Radius

The nonperturbative OPE radius is

[
\boxed{
R_{\rm OPE}
===========

\min_k |s_k|.
}
]

This is the distance to the nearest singularity of the spectral transform.

---

## 18.5 Theorem 3

If the spectral measure possesses a gap

[
E\ge M,
]

then

[
R_{\rm OPE}
\ge
M^{-1}.
]

### Interpretation

Mass gaps enlarge the domain of convergence.

Confining theories therefore naturally support finite OPE domains.

---

## 18.6 Physical Meaning

The radius is controlled by:

[
R_{\rm OPE}
\sim
\min
{
m_{\rm gap}^{-1},
\Lambda_{\rm topo}^{-1},
\Lambda_{\rm branch}^{-1}
}.
]

The convergence domain is determined by genuine physical scales.

---

# 19. Resurgent Structure of the OPE

## 19.1 Motivation

Perturbative OPE coefficients possess factorial growth:

[
c_n
\sim
n!.
]

This indicates hidden nonperturbative sectors.

---

## 19.2 Trans-Series Expansion

NOET proposes

[
C(r)
====

\sum_{k=0}^{\infty}
e^{-kS}
\Phi_k(r).
]

Each sector corresponds to a distinct vacuum saddle.

---

## 19.3 Spectral Interpretation

Instantons contribute

[
E_n
\rightarrow
E_n + kS.
]

The spectral transform becomes

[
C(r)
====

\sum_k
e^{-kS}
\int
e^{-Er}
d\mu_k(E).
]

Resurgence emerges automatically.

---

## 19.4 Renormalon Cancellation

Perturbative ambiguity:

[
\delta C
\sim
e^{-S}.
]

Nonperturbative sectors contribute

[
+,
e^{-S}.
]

Cancellation yields

[
\delta C_{\rm total}
====================

0.

]

Thus renormalons are reinterpreted as incomplete spectral decompositions.

---

## 19.5 Resurgent OPE Principle

### NOET-4

Every asymptotic perturbative OPE is the truncation of an exact spectral-resurgent expansion.

---

# 20. Renormalization Group Completion

## 20.1 RG Consistency

The OPE must remain invariant under changes of renormalization scale.

---

## 20.2 Operator Connection

Define

[
\nabla_\mu
==========

\partial_\mu+\Gamma_\mu.
]

The anomalous dimensions act as a gauge connection on operator space.

---

## 20.3 Spectral RG Equation

The coefficient functions satisfy

[
\left(
\mu\frac{\partial}{\partial\mu}
+
\beta(g)\frac{\partial}{\partial g}
\right)
C_{AB}^{;;C}
============

-\Gamma_{AB}^{;;;;C}C.
]

---

## 20.4 Covariant Form

Introduce

[
D_\mu C
=======

\partial_\mu C
+
\Gamma C.
]

Then

[
D_\mu C
=======

0.

]

The OPE coefficients are covariantly constant sections of the operator bundle.

---

## 20.5 RG Fixed Points

At

[
\beta(g_*)=0,
]

the connection becomes flat.

NOET reduces to ordinary conformal bootstrap theory.

Thus CFT emerges as a special case.

---

## 20.6 Nonperturbative RG Completion

The complete coefficient function becomes

[
C=
C_{\rm pert}
+
C_{\rm spectral}
+
C_{\rm topological}.
]

The RG acts consistently on all sectors simultaneously.

---

# 21. Nonperturbative Bootstrap Equations

## 21.1 Associativity Requirement

Operator multiplication must satisfy

[
(\mathcal O_A\mathcal O_B)\mathcal O_C
======================================

\mathcal O_A(\mathcal O_B\mathcal O_C).
]

This generates consistency constraints.

---

## 21.2 Spectral OPE Algebra

Insert

[
\mathcal O_A\mathcal O_B
========================

\sum_D
C_{AB}^{;;D}
\mathcal O_D.
]

Then

[
\sum_D
C_{AB}^{;;D}
C_{DC}^{;;E}
============

\sum_F
C_{AF}^{;;E}
C_{BC}^{;;F}.
]

---

## 21.3 Spectral Form

Using the spectral representation:

[
C_{AB}^{;;D}
============

\sum_n
\Xi_{AB,n}^{;;;;D}
e^{-E_n r},
]

one obtains nonlinear equations for:

[
E_n,
\qquad
\Xi_{AB,n}^{;;;;D}.
]

---

## 21.4 Master Bootstrap Equation

[
\boxed{
\sum_{D,n,m}
\Xi_{AB,n}^{;;;;D}
\Xi_{DC,m}^{;;;;E}
e^{-(E_n+E_m)r}
===============

\sum_{F,n,m}
\Xi_{AF,n}^{;;;;E}
\Xi_{BC,m}^{;;;;F}
e^{-(E_n+E_m)r}
}
]

This equation replaces perturbative diagrammatics.

---

## 21.5 Bootstrap Reconstruction Conjecture

### NOET-5

Given:

[
{E_n},
\qquad
\Xi_{AB,n}^{;;;;C},
]

satisfying:

1. positivity,
2. locality,
3. associativity,
4. spectral convergence,

the complete nonperturbative OPE is uniquely determined.

---

## 21.6 Summary of Volume IV

The mathematical core of NOET has now been established.

Key results include:

1. Spectral representation of OPE coefficients.
2. Convergence criteria based on state density.
3. Spectral definition of the OPE radius.
4. Resurgent completion of asymptotic expansions.
5. Renormalization-group covariance.
6. Nonperturbative bootstrap equations.

The next volume applies this framework to gauge theories, confinement, condensates, and QCD.
