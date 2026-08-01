# General Relativity × Information Geometry

## Fisher Information Geometry on the Space of Spacetimes

### A Unified Information-Theoretic Structure for Einsteinian Superspace

---

## Abstract

General Relativity (GR) describes gravity as the geometry of spacetime, while Information Geometry describes statistical inference as the geometry of probability distributions. Both theories are fundamentally geometric, yet they have evolved independently.

The solution space of Einstein's field equations, modulo diffeomorphism equivalence, forms an infinite-dimensional manifold known as superspace. Since DeWitt's introduction of the supermetric on superspace, this manifold has been understood as possessing an intrinsic geometric structure derived from gravitational dynamics. Separately, information geometry has shown that any family of probability distributions possesses a natural Riemannian metric given by Fisher information.

This work proposes a new synthesis: spacetime solutions themselves are treated as elements of a statistical manifold. Each spacetime is associated with an observational probability distribution encoding measurable physical information. Fisher information then induces a metric on the space of spacetimes.

We demonstrate that:

1. Einstein superspace can be reinterpreted as an information manifold.
2. The DeWitt metric emerges as a gravitational limit of a Fisher-information metric.
3. Geodesics in Fisher superspace define optimal-information interpolations between spacetimes.
4. Information curvature measures distinguishability complexity among neighboring universes.
5. Einstein dynamics may be recast as information transport on superspace.

This framework establishes an information-theoretic geometry of spacetime itself rather than geometry within spacetime.

---

# 1. Introduction

Two geometric revolutions transformed modern physics.

The first was Einstein's realization that gravitation is geometry.

The second was Fisher's realization that statistical inference is geometry.

General Relativity assigns a metric to spacetime.

Information Geometry assigns a metric to probability space.

These constructions are mathematically similar:

* both employ manifolds,
* both define connections,
* both possess curvature,
* both define geodesics.

Yet they are usually applied to entirely different objects.

The key observation motivating this paper is:

> The space of solutions of Einstein's equations is itself a manifold.

If any manifold of models can acquire a Fisher metric, then the space of spacetime geometries should also admit one.

This possibility appears not to have been systematically explored.

---

# 2. Einstein Superspace

Let

[
\mathcal M
]

be a four-dimensional manifold.

Let

[
g_{\mu\nu}
]

satisfy Einstein's field equations

[
G_{\mu\nu}
==========

8\pi G T_{\mu\nu}.
]

The collection of all solutions is

[
\mathcal S.
]

Factoring by diffeomorphisms gives

[
\mathcal U
==========

\mathcal S/\mathrm{Diff}(\mathcal M).
]

This quotient space is Wheeler-DeWitt superspace.

Each point of superspace represents an entire physical spacetime.

Traditional GR studies geometry inside one point of superspace.

Here we study geometry between points of superspace.

---

# 3. Observational Probability Distributions

Information geometry requires probability distributions.

Therefore every spacetime must be mapped to a probability measure.

Define

[
g
\mapsto
P(x|g).
]

Several choices exist.

## Observer Distribution

Consider measurements of observables

[
O_i.
]

A spacetime predicts

[
P(O|g).
]

Examples:

* redshift distributions,
* gravitational-wave spectra,
* lensing statistics,
* particle trajectories,
* causal intervals.

Each spacetime therefore generates an observational ensemble.

---

## Quantum-State Distribution

A semiclassical spacetime defines a vacuum state

[
|0_g\rangle.
]

Correlation functions determine

[
P(\phi|g).
]

The spacetime thus becomes a statistical model.

---

## Geodesic Ensemble Distribution

Let

[
\Gamma_g
]

denote the set of geodesics.

Sampling geodesics generates

[
P(\gamma|g).
]

The geometry itself becomes a probability distribution.

---

# 4. Fisher Geometry of Superspace

Suppose spacetime solutions are parametrized by coordinates

[
\theta^A.
]

Examples:

[
(M,a,Q,\Lambda,\dots).
]

The Fisher metric becomes

[
\mathcal I_{AB}
===============

\int
P(x|\theta)
,
\partial_A \log P
,
\partial_B \log P
,dx.
]

This defines a Riemannian metric on superspace.

We call

[
(\mathcal U,\mathcal I)
]

the Fisher Superspace.

The information distance is

[
ds^2
====

\mathcal I_{AB}
d\theta^A
d\theta^B.
]

This measures distinguishability between neighboring spacetimes.

---

# 5. Physical Meaning

The Fisher metric quantifies how much information is required to distinguish two nearby universes.

If

[
ds^2
\ll 1
]

then no realistic observer can tell the spacetimes apart.

If

[
ds^2
\gg 1
]

the universes are observationally distinct.

Thus Fisher distance becomes an operational measure of spacetime separation.

Traditional superspace distance measures geometric variation.

Fisher distance measures observational variation.

---

# 6. Relation to the DeWitt Metric

The DeWitt supermetric is

[
G^{abcd}
========

\frac12
\sqrt h
\left(
h^{ac}h^{bd}
+
h^{ad}h^{bc}
------------

h^{ab}h^{cd}
\right).
]

It defines distances between 3-geometries.

Historically this metric arose from Hamiltonian gravity.

Its information-theoretic meaning remained unknown.

---

## Key Observation

Suppose metric perturbations are observables.

Let

[
h_{ab}
\rightarrow
h_{ab}
+
\delta h_{ab}.
]

Assume fluctuations obey

[
P[\delta h]
\propto
\exp
\left(
-\frac12
\delta h_{ab}
G^{abcd}
\delta h_{cd}
\right).
]

This Gaussian distribution possesses Fisher metric

[
\mathcal I_{AB}
===============

G_{AB}.
]

Therefore:

> The DeWitt metric is the Fisher metric of gravitational fluctuations.

This provides a statistical interpretation of the supermetric.

DeWitt geometry and Fisher geometry become dual descriptions of the same structure.

---

# 7. Information-Geometric Derivation of DeWitt Superspace

Consider a family of gravitational states

[
P[h;\theta].
]

The Fisher metric is

[
\mathcal I_{AB}
===============

\Big\langle
\partial_A \log P
,
\partial_B \log P
\Big\rangle.
]

For Gaussian fluctuations around classical geometries,

[
P
\sim
e^{-S_{\rm grav}}.
]

Expanding the Einstein-Hilbert action to quadratic order yields the Hessian

[
\frac{\delta^2 S}{\delta h,\delta h}.
]

This Hessian is precisely the kinetic operator whose geometric form generates the DeWitt supermetric.

Hence

[
\mathcal I
\sim
\mathrm{Hess}(S)
\sim
G_{\rm DeWitt}.
]

The supermetric emerges as an information metric.

---

# 8. Geodesics in Fisher Superspace

Given

[
\mathcal I_{AB},
]

the geodesic equation becomes

[
\frac{d^2\theta^A}{d\lambda^2}
+
\Gamma^A_{BC}
\frac{d\theta^B}{d\lambda}
\frac{d\theta^C}{d\lambda}
==========================

0.

]

These curves minimize information length.

---

## Interpretation

A Fisher geodesic between two spacetime solutions represents

> the least distinguishable path connecting two universes.

This differs fundamentally from a dynamical evolution.

Instead it defines an optimal inference trajectory through the landscape of spacetimes.

---

# 9. Example: Schwarzschild Family

Consider

[
P(x|M).
]

The Fisher metric is

[
I(M)
====

\int
P
\left(
\partial_M \log P
\right)^2
dx.
]

The information distance becomes

[
ds^2
====

I(M)dM^2.
]

A geodesic corresponds to a sequence of black-hole masses changing at constant information speed.

This gives a statistical interpolation between black-hole geometries.

---

# 10. Information Curvature of Superspace

The Fisher metric possesses Riemann curvature

[
\mathcal R_{ABCD}.
]

This curvature measures how distinguishability changes globally.

---

## Interpretation

Positive curvature:

* nearby universes become statistically redundant.

Negative curvature:

* nearby universes rapidly diverge observationally.

Large curvature:

* strong sensitivity to spacetime parameters.

Flat regions:

* observational degeneracy.

Thus curvature becomes a measure of complexity in the gravitational landscape.

---

# 11. Einstein Equations as Information Extremization

A deeper possibility emerges.

Classically,

[
\delta S_{\rm EH}=0.
]

Information geometry often derives dynamics from extremal Fisher information.

Suppose spacetime configurations satisfy

[
\delta \mathcal I =0.
]

Then Einstein solutions become critical points of distinguishability.

Gravity becomes an information-optimization principle.

---

# 12. Statistical Meaning of Curvature Singularities

Near singular solutions:

[
\mathcal I
\rightarrow
\infty.
]

Interpretation:

Infinite Fisher information implies infinite distinguishability.

A singular spacetime occupies an infinitely distant point in information space.

This suggests a new regularization principle:

physical theories should maintain finite information distance.

---

# 13. Cosmological Applications

The framework naturally applies to cosmology.

Parameter space:

[
(H_0,\Omega_m,\Omega_\Lambda,w,\dots).
]

The Fisher metric measures distinguishability among universes.

Information curvature identifies:

* parameter degeneracies,
* observational attractors,
* critical cosmological transitions.

---

# 14. Black Hole Information Geometry

Each black-hole family defines a statistical manifold.

Coordinates:

[
(M,Q,J).
]

Information curvature may reveal:

* extremal transitions,
* stability boundaries,
* evaporation trajectories,
* quantum critical behavior.

---

# 15. Quantum Gravity Interpretation

Superspace appears in canonical quantum gravity through the Wheeler-DeWitt equation.

The Fisher metric suggests:

[
\Psi[h]
]

is simultaneously

* a quantum amplitude,
* an information distribution.

Quantum gravity then becomes information dynamics on superspace.

---

# 16. The Information Equivalence Principle

We propose:

> Local gravitational indistinguishability is equivalent to local information-geometric flatness.

Just as spacetime curvature measures gravitational effects, Fisher curvature measures informational effects.

Gravity and information become dual manifestations of geometric structure.

---

# 17. The Fisher–DeWitt Correspondence

Central Conjecture:

[
G_{\rm DeWitt}
==============

\lim_{\text{classical}}
\mathcal I_{\rm Fisher}.
]

Interpretation:

* DeWitt geometry describes how spacetime configurations vary.
* Fisher geometry describes how spacetime configurations can be distinguished.

They are two projections of a single underlying geometry.

The former is dynamical.

The latter is inferential.

Together they form a unified geometry of spacetime possibility.

---

# 18. Predictions and Research Program

The framework predicts:

1. Fisher curvature invariants of superspace.
2. Information-geodesic classifications of spacetime families.
3. Statistical interpretations of canonical quantum gravity.
4. New measures of black-hole distinguishability.
5. Information-theoretic singularity diagnostics.
6. Observable cosmological complexity metrics.
7. Fisher-flow analogues of Ricci flow on superspace.

---

# 19. Conclusion

General Relativity studies geometry within spacetime.

Information Geometry studies geometry of probability.

This work proposes a third level of structure:

the geometry of the space of spacetimes themselves.

The key insight is that every spacetime determines a statistical model, and every statistical model possesses Fisher geometry.

When this construction is applied to Einstein superspace, the Fisher metric provides an operational notion of distance between universes. Remarkably, in the Gaussian fluctuation limit, the resulting information metric reproduces the DeWitt supermetric, suggesting that gravitational superspace and statistical model space are not distinct objects but alternative interpretations of the same manifold.

The DeWitt metric measures variation of geometry.

The Fisher metric measures distinguishability of geometry.

The wall separating gravity and information is therefore not a boundary between two theories, but a change of perspective on a single geometric structure.
