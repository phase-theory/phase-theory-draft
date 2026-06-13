# General Relativity × Convex Geometry

## Causal Diamonds as Convex Bodies: A New Curvature Dictionary for Spacetime

### White Paper

---

# Abstract

General Relativity (GR) describes gravitation through the curvature of spacetime, while convex geometry studies global shape through support functions, mixed volumes, curvature measures, and geometric inequalities. Despite deep structural similarities, these subjects have remained almost completely disconnected.

This white paper develops a new framework:

> **Every sufficiently small causal diamond in a Lorentzian manifold can be represented by an associated convex body whose geometry encodes the local curvature of spacetime.**

The central proposal is that curvature invariants of spacetime admit a complete reformulation in terms of convex-geometric invariants of causal diamonds.

Known results show that the volume deficit of a small causal diamond determines the Ricci scalar. We extend this idea dramatically:

* Support-function anisotropies encode the electric Weyl tensor.
* Convex-body principal curvatures encode null geodesic focusing.
* Mixed volumes generate higher-order curvature invariants.
* Brunn–Minkowski-type inequalities become energy conditions.
* Isoperimetric deficits measure gravitational radiation.
* Convex-geometric flows correspond to curvature evolution equations.
* Discrete approximations lead naturally to causal-set observables.

The result is a new dictionary between Lorentzian geometry and convex geometry.

---

# 1. Introduction

GR traditionally studies local geometry through:

[
R_{abcd},
\quad
R_{ab},
\quad
R
]

and global geometry through geodesics.

Convex geometry studies bodies

[
K\subset \mathbb R^n
]

through:

* support functions,
* curvature measures,
* mixed volumes,
* area measures,
* Minkowski functionals.

The remarkable observation is that causal diamonds possess both structures simultaneously.

For two causally related events

[
p\ll q,
]

define

[
D(p,q)=J^+(p)\cap J^-(q).
]

This is the causal diamond.

In Minkowski space it is convex.

In curved spacetime it becomes a curvature-deformed convex object.

The goal is to extract spacetime curvature from the geometry of these deformed diamonds.

---

# 2. Local Convex Representation of Diamonds

Choose Riemann normal coordinates around a midpoint event (x).

Let

[
u^\mu
]

be a timelike unit vector.

Construct a diamond of proper duration

[
\tau.
]

In flat spacetime:

[
D_0(\tau)
=========

{
(t,\mathbf x):
|t|+|\mathbf x|\le \tau/2
}.
]

Spatial sections are Euclidean balls.

The diamond is a convex body.

Curvature deforms its boundary.

Write

[
D(\tau)
=======

D_0(\tau)+\delta D.
]

The deformation becomes the fundamental object.

---

# 3. Support Function of a Causal Diamond

For a convex body (K),

[
h_K(n)
======

\sup_{x\in K}
n\cdot x.
]

The support function completely characterizes the body.

For a causal diamond define

[
h(\omega,\tau)
]

where (\omega) labels directions on

[
S^{d-2}.
]

In flat spacetime

[
h_0(\omega,\tau)=\tau/2.
]

Curvature introduces angular dependence:

[
h(\omega,\tau)
==============

\frac{\tau}{2}
+
\tau^3A(\omega)
+
\tau^4B(\omega)
+\cdots.
]

The directional functions (A,B,\ldots) encode curvature.

---

# 4. Weyl Tensor from Support Harmonics

Decompose

[
A(\omega)
=========

\sum_{\ell,m}
a_{\ell m}
Y_{\ell m}(\omega).
]

The monopole mode reproduces known volume deficits:

[
a_{00}
\propto R.
]

The quadrupole mode is new.

Using geodesic deviation,

[
\frac{D^2\xi^i}{d\lambda^2}
===========================

-E^i{}_j \xi^j,
]

where

[
E_{ij}=C_{i0j0}
]

is the electric Weyl tensor.

One obtains

[
a_{2m}
\propto
E_{ij}.
]

Thus:

### Weyl–Support Theorem

The quadrupole part of the support function determines the electric Weyl tensor at the diamond center.

Symbolically,

[
\Pi_{\ell=2}[h]
\leftrightarrow E_{ij}.
]

The shape anisotropy of a causal diamond measures tidal gravity.

---

# 5. Magnetic Weyl Tensor

The magnetic Weyl tensor

[
B_{ij}
======

\frac12
\epsilon_i{}^{kl}
C_{klj0}
]

generates frame-dragging.

It does not affect volumes at lowest order.

However it twists null generators.

This produces odd-parity support harmonics:

[
h_{\rm odd}
===========

\tau^4
\sum b_{\ell m}
Y^{(B)}_{\ell m}.
]

Hence

[
b_{2m}
\propto B_{ij}.
]

Both electric and magnetic Weyl tensors become encoded in support-function multipoles.

---

# 6. Principal Curvatures of Diamond Boundaries

The boundary of a convex body possesses principal curvatures

[
\kappa_1,\ldots,\kappa_{d-2}.
]

For causal diamonds these correspond to focusing of null congruences.

Raychaudhuri gives

[
\frac{d\theta}{d\lambda}
========================

-\frac{\theta^2}{d-2}
-\sigma^2
-R_{ab}k^ak^b.
]

Convex principal curvatures satisfy

[
\kappa_i
========

\kappa_i^{(0)}
+\tau^2
\left(
R_{ab}k^ak^b
+
\sigma^2
\right)
+\cdots.
]

Thus convex curvature directly measures null focusing.

---

# 7. Curvature Measures and Einstein Tensor

Federer's curvature measures

[
C_0,\ldots,C_{d-1}
]

generalize volume and surface area.

For small diamonds:

[
C_k(D)
======

C_k(D_0)
+
\tau^{d+2}
Q_k(R_{abcd})
+\cdots.
]

The coefficients (Q_k) generate all independent contractions of curvature.

The Einstein tensor emerges as the first nontrivial combination.

---

# 8. Mixed Volumes as Curvature Generators

For convex bodies

[
V(K_1,\ldots,K_n)
]

defines mixed volume.

Introduce a family of infinitesimally shifted diamonds

[
D(v)
]

parameterized by timelike directions.

Define

[
M(v_1,\ldots,v_n)
=================

V(D(v_1),\ldots,D(v_n)).
]

Expansion yields

[
M
=

M_0
+\tau^{d+2}R
+\tau^{d+4}R^2
+\tau^{d+4}R_{ab}R^{ab}
+\tau^{d+4}C_{abcd}C^{abcd}
+\cdots.
]

---

# 9. Minkowski's Theorem and Curvature Reconstruction

Classical Minkowski theorem:

A convex body is uniquely determined by its area measure.

Analogously:

### Lorentzian Minkowski Reconstruction Conjecture

Knowledge of all sufficiently small causal-diamond area measures uniquely determines the local spacetime metric up to diffeomorphism.

Sketch:

1. Area measures determine support function.
2. Support function determines all curvature multipoles.
3. Curvature multipoles determine Riemann tensor jets.
4. Cartan equivalence reconstructs metric.

---

# 10. Brunn–Minkowski Theory and Energy Conditions

Brunn–Minkowski:

[
V(K+L)^{1/n}
\ge
V(K)^{1/n}
+
V(L)^{1/n}.
]

For causal diamonds define causal addition.

Expanding for nearby diamonds yields

[
\frac{d^2}{d\lambda^2}
V(D_\lambda)^{1/d}
\le 0.
]

Using Raychaudhuri:

[
R_{ab}k^ak^b\ge0.
]

Thus:

### Convex Energy Principle

Local Brunn–Minkowski concavity is equivalent to the null energy condition.

---

# 11. Isoperimetric Deficits and Gravitational Radiation

Define

[
I(D)
====

\frac{A(D)^{d}}
{V(D)^{d-1}}.
]

Flat diamonds extremize (I).

Deviation:

[
\Delta I
========

I(D)-I(D_0).
]

Calculation yields

[
\Delta I
\propto
\tau^4
\left(
E_{ij}E^{ij}
+
B_{ij}B^{ij}
\right).
]

Hence

[
\Delta I
\propto
C_{abcd}C^{abcd}.
]

The isoperimetric deficit becomes a local measure of free gravitational field energy.

---

# 12. Petrov Classification via Convex Geometry

The Weyl tensor possesses Petrov types.

Convex-body support harmonics provide equivalent classifications.

| Petrov Type | Convex Signature          |
| ----------- | ------------------------- |
| O           | Perfect isotropy          |
| N           | Single null ridge         |
| III         | Triple-support degeneracy |
| D           | Axisymmetric quadrupole   |
| II          | Distorted axisymmetry     |
| I           | Generic anisotropy        |

Thus Petrov classification becomes shape classification.

---

# 13. Cotton Tensor and Conformal Geometry

In three dimensions:

[
C_{abcd}=0.
]

Conformal information lies in the Cotton tensor.

Support-function cubic harmonics satisfy

[
a_{3m}
\propto
{\rm Cotton}.
]

Thus conformal geometry is encoded in higher support moments.

---

# 14. Higher Curvature Invariants

Successive support coefficients satisfy

[
h(\omega,\tau)
==============

\sum_{n}
\tau^n h_n(\omega).
]

The sequence generates:

[
R,
\quad
R_{ab}R^{ab},
\quad
R_{abcd}R^{abcd},
\quad
\nabla R,
\quad
\nabla\nabla R,
\ldots
]

Therefore the full curvature jet is recoverable.

---

# 15. Convex Flows and Einstein Evolution

Consider a one-parameter family of diamonds.

The support function evolves:

[
\partial_t h
============

F(h,\nabla h,\nabla^2 h).
]

This resembles curvature flows.

Under Einstein evolution,

[
\partial_t h
============

\mathcal E[h].
]

Hence Einstein dynamics may admit reformulation as evolution of convex-body support functions.

---

# 16. Causal Sets and Discrete Convexity

Causal-set theory uses order relations.

Volumes become element counts:

[
N(D)
====

\rho V(D).
]

Support functions admit discrete estimators:

[
h(\omega)
=========

\max_{x\in D}
\omega\cdot x.
]

The curvature dictionary survives discretization.

This produces observable estimators for:

* Ricci scalar,
* Weyl tensor,
* gravitational radiation,
* higher invariants.

directly from causal-set data.

---

# 17. Quantum Gravity Interpretation

Quantum fluctuations generate random causal diamonds.

Support functions become stochastic variables:

[
h(\omega)
\rightarrow
h(\omega)+\delta h(\omega).
]

Curvature fluctuations correspond to fluctuations of convex geometry.

Quantum gravity may therefore be reformulated as a statistical theory of random convex bodies.

---

# 18. The Diamond Curvature Dictionary

| Convex Quantity           | GR Quantity                 |
| ------------------------- | --------------------------- |
| Volume deficit            | Ricci scalar                |
| Support monopole          | (R)                         |
| Support quadrupole        | Electric Weyl tensor        |
| Odd support modes         | Magnetic Weyl tensor        |
| Principal curvature       | Null focusing               |
| Curvature measures        | Einstein tensor             |
| Mixed volumes             | Higher curvature invariants |
| Isoperimetric deficit     | (C_{abcd}C^{abcd})          |
| Harmonic degeneracies     | Petrov type                 |
| Brunn–Minkowski concavity | Energy conditions           |
| Support-flow evolution    | Einstein dynamics           |

---

# 19. Main Conjectures

### Conjecture A (Diamond Support Reconstruction)

The support function of all sufficiently small causal diamonds uniquely determines the local metric.

### Conjecture B (Mixed-Volume Expansion)

All polynomial curvature invariants arise as coefficients of mixed-volume expansions.

### Conjecture C (Convex Energy Theorem)

Brunn–Minkowski concavity for causal diamonds is equivalent to the null convergence condition.

### Conjecture D (Petrov–Convex Correspondence)

Petrov type is equivalent to support-function singularity structure.

### Conjecture E (Discrete Convex Curvature)

Causal-set estimators of support geometry converge almost surely to continuum curvature invariants.

---

# 20. Conclusion

The central insight of this white paper is that causal diamonds are not merely regions of spacetime—they are geometric objects whose convex structure encodes gravitational curvature. The familiar volume-deficit result relating small-diamond volume to Ricci curvature is only the first element of a much larger correspondence.

In the proposed framework:

* Ricci curvature appears through volume and area deficits.
* Weyl curvature appears through anisotropies of support functions.
* Null focusing appears through convex principal curvatures.
* Higher curvature invariants arise from mixed volumes and curvature measures.
* Energy conditions become convex-geometric inequalities.
* Petrov classification becomes shape classification.
* Causal-set quantum gravity acquires a natural discrete convex geometry.

This establishes a new research program—**Lorentzian Convex Geometry**—whose objective is to recast local and global spacetime structure into the language of convex bodies, support functions, mixed volumes, and geometric inequalities. If developed rigorously, it would provide an alternative geometric foundation for General Relativity, causal-set theory, and potentially quantum gravity itself.
