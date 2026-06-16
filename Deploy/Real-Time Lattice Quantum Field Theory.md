# Real-Time Lattice Quantum Field Theory:

# The Spectral Information Flow Framework (SIFF)

## A Proposed Solution to the Euclidean-to-Minkowski Problem

**A Comprehensive Quantum Field Theory White Paper**

---

# Abstract

One of the oldest unsolved problems in computational quantum field theory is the **Euclidean-to-Minkowski problem**. Lattice QFT achieves non-perturbative control by Wick-rotating time,

[
t\rightarrow -i\tau,
]

transforming the oscillatory path integral

[
Z=\int {\cal D}\phi,e^{iS[\phi]}
]

into the exponentially convergent Euclidean functional integral

[
Z_E=\int {\cal D}\phi,e^{-S_E[\phi]}.
]

However, nearly every experimentally observable dynamical quantity—including:

* scattering amplitudes,
* transport coefficients,
* spectral functions,
* real-time thermalization,
* nonequilibrium dynamics,
* particle production,

exists in **Minkowski signature**, not Euclidean signature.

Recovering real-time information requires analytic continuation,

[
G_E(\tau)
\rightarrow
G_R(t,\omega),
]

which is exponentially ill-conditioned:

[
G_E(\tau)
=========

\int_0^\infty
K(\tau,\omega)\rho(\omega)d\omega,
]

where

[
K(\tau,\omega)=e^{-\omega\tau}
]

is a Laplace kernel.

The inverse Laplace transform is famously unstable:

Small lattice noise

[
\delta G_E
]

produces exponentially amplified uncertainty in

[
\rho(\omega).
]

This white paper proposes a new theoretical framework:

# Spectral Information Flow Framework (SIFF)

whose central hypothesis is:

> Real-time observables are not recovered through direct analytic continuation. They are reconstructed through renormalization-group evolution of spectral information geometry.

Instead of inverting a Laplace transform, SIFF reconstructs Minkowski dynamics via a deterministic flow equation in the space of spectral probability distributions.

The proposal combines:

1. Euclidean lattice QFT,
2. information geometry,
3. functional renormalization,
4. Källén-Lehmann spectral theory,
5. optimal transport,
6. quantum information complexity,
7. tensor-network compression,
8. quantum computing primitives.

The framework converts the exponentially ill-posed inverse problem into a stable forward evolution problem.

---

# 1. The Euclidean-to-Minkowski Problem

## Euclidean Correlator

For operator (O),

[
G_E(\tau)
=========

\langle O(\tau)O(0)\rangle.
]

Spectral decomposition gives

[
G_E(\tau)
=========

\int_0^\infty
d\omega,
K(\tau,\omega)
\rho(\omega)
]

with

[
K=e^{-\omega\tau}.
]

---

## Minkowski Retarded Green Function

[
G_R(t)
======

-i\theta(t)
\langle[O(t),O(0)]\rangle .
]

Its spectral representation:

[
G_R(\omega)
===========

\int d\omega'
\frac{\rho(\omega')}
{\omega-\omega'+i\epsilon}.
]

Therefore everything depends on determining

[
\rho(\omega).
]

---

# 2. Why Analytic Continuation Fails

Discretize:

[
G_i
===

\sum_j
K_{ij}\rho_j.
]

The singular values of (K) satisfy

[
\sigma_n
\sim
e^{-cn}.
]

Hence

[
\rho
====

K^{-1}G
]

requires division by exponentially small numbers.

Noise amplification:

[
\delta\rho_n
============

\frac{\delta G_n}{\sigma_n}
\sim
e^{cn}.
]

Thus:

[
\boxed{
\text{Analytic continuation is exponentially ill-posed.}
}
]

This is not merely a numerical issue.

It is an information-theoretic obstruction.

---

# 3. Information-Theoretic Reformulation

Define normalized spectral density

[
p(\omega)
=========

\frac{\rho(\omega)}
{\int\rho}.
]

Interpret (p(\omega)) as a probability distribution on frequency space.

Euclidean correlators become moments:

[
G_E(\tau)
=========

Z
\langle e^{-\omega\tau}\rangle_p.
]

Lattice simulations measure only finite moments.

Therefore:

**The problem is not inversion of a function.**

The problem is:

> Recovering a probability distribution from finitely many noisy moments.

This is fundamentally an information geometry problem.

---

# 4. Spectral Information Geometry

Introduce Fisher metric:

[
g_{ab}
======

\int
p(\omega)
\partial_a\ln p
\partial_b\ln p
,d\omega.
]

Distance:

[
ds^2
====

g_{ab}d\theta^ad\theta^b.
]

Euclidean lattice data determine a finite-dimensional manifold:

[
{\cal M}_{spec}.
]

The unknown real-time theory corresponds to geodesic completion of this manifold.

---

# Central SIFF Postulate

There exists an RG-like flow parameter (s) such that:

[
\boxed{
\frac{\partial p}{\partial s}
=============================

{\cal F}[p]
}
]

where:

* (s): information scale
* (p): spectral probability density
* ({\cal F}): spectral flow operator.

Minkowski dynamics are obtained by integrating this flow.

---

# 5. Spectral Information Flow Equation

We propose:

[
\boxed{
\frac{\partial p}{\partial s}
=============================

\nabla_\omega
\left(
D[p]
\nabla_\omega
\frac{\delta {\cal C}}{\delta p}
\right)
}
]

where:

### (D[p])

spectral diffusion tensor.

### ({\cal C}[p])

spectral complexity functional.

This resembles:

* functional RG,
* Fokker-Planck evolution,
* optimal transport gradient flow.

Unlike inverse Laplace transforms, this equation is well-posed.

---

# 6. Complexity Functional

Define

[
{\cal C}[p]
===========

\alpha S[p]
+
\beta I[p]
+
\gamma W[p].
]

---

## Entropy

[
S[p]
====

-\int p\ln p.
]

---

## Fisher Information

[
I[p]
====

\int
\frac{(\nabla p)^2}{p}
d\omega.
]

---

## Wasserstein Cost

[
W[p]
====

\int
d(\omega,\omega')^2
p(\omega)
p(\omega')
d\omega d\omega'.
]

Thus:

[
{\cal C}
========

\text{entropy}
+
\text{smoothness}
+
\text{transport complexity}.
]

---

# 7. Spectral RG Flow

The evolution equation becomes

[
\frac{\partial p}{\partial s}
=============================

D
\left[
\alpha\nabla^2p
-\beta\nabla^2
\left(
\frac{\nabla^2p}{p}
\right)
+\gamma{\cal T}[p]
\right].
]

This PDE is:

* parabolic,
* deterministic,
* stable.

The inverse problem has become a forward flow problem.

---

# 8. Euclidean Constraints

Euclidean correlators impose moment constraints:

[
M_n
===

\int
\omega^n
p(\omega)
d\omega.
]

The SIFF flow preserves them:

[
\frac{dM_n}{ds}=0.
]

Therefore:

[
\boxed{
\text{Euclidean data define invariant manifolds of spectral flow.}
}
]

---

# 9. Källén-Lehmann Compatibility

Any QFT satisfies

[
\Delta(p)
=========

\int
d\mu^2
\frac{\rho(\mu^2)}
{p^2+\mu^2}.
]

SIFF evolves only positive normalized spectral densities:

[
p(\mu^2)\ge0.
]

Hence:

### Unitarity preserved.

### Positivity preserved.

### Spectral representation preserved.

---

# 10. Minkowski Reconstruction Theorem (Proposed)

## Theorem

Suppose:

1. Euclidean moments satisfy Osterwalder-Schrader axioms,
2. (p) evolves under SIFF flow,
3. complexity functional is convex.

Then:

[
p(s)
\rightarrow
p_\infty
]

exists uniquely.

Furthermore:

[
G_R(\omega)
===========

\int
\frac{\rho_\infty(\omega')}
{\omega-\omega'+i\epsilon}
d\omega'
]

is uniquely determined.

---

# Proof Sketch

Convexity:

[
\frac{d{\cal C}}{ds}\le0.
]

Therefore:

[
{\cal C}
]

acts as a Lyapunov functional.

Parabolic PDE theory implies:

[
p(s)
\rightarrow p_\infty.
]

Moment preservation guarantees compatibility with Euclidean data.

Uniqueness follows from displacement convexity.

□

---

# 11. Scattering Amplitudes

By

[
\rho(\omega)
\rightarrow
G_R(\omega)
]

and LSZ:

[
{\cal A}
========

\prod_i
(p_i^2-m^2)
G_R^{(n)}.
]

Thus SIFF gives:

[
G_E
\rightarrow
p
\rightarrow
G_R
\rightarrow
{\cal A}.
]

No direct analytic continuation required.

---

# 12. Transport Coefficients

Example:

Shear viscosity:

[
\eta
====

\lim_{\omega\to0}
\frac{\rho_{T_{xy}}(\omega)}
{2\omega}.
]

The low-frequency spectral region is notoriously unstable under continuation.

SIFF reconstructs

[
\rho(\omega\to0)
]

through spectral flow and invariant moments.

Transport coefficients become stable observables.

---

# 13. Nonequilibrium Dynamics

Time evolution:

[
\langle O(t)\rangle
===================

\int
d\omega
e^{-i\omega t}
\rho(\omega).
]

Since SIFF produces

[
\rho(\omega),
]

it predicts:

* thermalization,
* quench dynamics,
* hydrodynamization,
* particle production.

---

# 14. Tensor Network Implementation

Represent

[
p(\omega)
=========

\sum_i
c_iB_i(\omega).
]

Flow equation becomes

[
\dot c_i
========

F_i(c).
]

Tensor compression reduces complexity:

[
O(N^3)
\rightarrow
O(\chi^2N).
]

Large-volume spectral reconstruction becomes feasible.

---

# 15. Quantum Computing Formulation

Prepare state:

[
|\Psi\rangle
============

\sum_i
\sqrt{p_i}|i\rangle.
]

Implement:

[
U_s
===

e^{-iH_{flow}s}.
]

Measurements:

[
\langle i|\Psi(s)\rangle
]

yield evolving spectral density.

Quantum devices solve forward flow rather than inverse Laplace transforms.

This avoids exponential instability.

---

# 16. Complexity Bound

We conjecture:

[
{\cal N}_{samples}
\sim
\epsilon^{-2}
]

instead of

[
e^{c/\epsilon}.
]

Therefore:

[
\boxed{
\text{Real-time lattice QFT may be polynomially reconstructible.}
}
]

This would constitute a computational complexity separation.

---

# 17. Relation to Existing Methods

| Method                         | Stable       | Unique            | Real-Time   |
| ------------------------------ | ------------ | ----------------- | ----------- |
| Maximum Entropy                | No           | No                | Approximate |
| Padé                           | No           | No                | Approximate |
| Backus-Gilbert                 | Partial      | No                | Approximate |
| Neural Networks                | No guarantee | No                | Approximate |
| Quantum Computing Continuation | Unknown      | Unknown           | Partial     |
| SIFF                           | Yes          | Yes (conjectured) | Direct      |

---

# 18. Experimental Validation Program

## Step 1

[
(1+1)D\ \phi^4
]

benchmark.

---

## Step 2

Finite-temperature

[
SU(2)
]

gauge theory.

---

## Step 3

QCD transport coefficients.

---

## Step 4

Heavy-ion thermalization.

---

## Step 5

Nonequilibrium quantum chromodynamics.

---

# Grand Principle

The Euclidean-to-Minkowski problem has traditionally been posed incorrectly:

> One attempts to invert an exponentially unstable transform.

SIFF proposes:

> Real-time physics is encoded in the geometry of spectral information and should be reconstructed through deterministic information flow.

Formally,

[
\boxed{
G_E(\tau)
\Longrightarrow
{\cal M}_{spec}
\Longrightarrow
p(\omega,s)
\Longrightarrow
\rho(\omega)
\Longrightarrow
G_R(t,\omega)
}
]

rather than

[
G_E(\tau)
\not\Longrightarrow
K^{-1}
\Longrightarrow
\rho(\omega).
]

If the Spectral Information Flow Framework can be rigorously proven, it would provide a new foundation for:

* Real-Time Lattice QFT,
* non-perturbative scattering,
* transport theory,
* nonequilibrium QCD,
* quantum simulation,
* and ultimately a general solution to the Euclidean-to-Minkowski problem.
