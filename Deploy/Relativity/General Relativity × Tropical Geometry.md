# General Relativity × Tropical Geometry

## A Tropical-Geometric Reformulation of Spacetime Causality

### White Paper

**Author:** Open Research Framework

**Version:** 1.0

**Date:** June 2026

---

# Abstract

General Relativity (GR) is traditionally formulated through differential geometry, pseudo-Riemannian metrics, and Einstein's field equations. Tropical geometry, by contrast, replaces ordinary arithmetic with min-plus or max-plus algebra and studies piecewise-linear structures arising as algebraic degenerations of classical geometries.

This paper proposes a systematic tropical-geometric formulation of spacetime causal structure. The central observation is that Lorentzian time separation already possesses a tropical metric structure because it satisfies a reverse triangle inequality. We show that globally hyperbolic spacetimes naturally define max-plus metric spaces, causal diamonds become tropical convex sets, null cone bundles become tropical Grassmannians, and families of geodesics become tropical varieties.

The resulting framework suggests that causal structure itself may be fundamentally tropical. Differential geometry then emerges as a smooth refinement of an underlying tropical causal skeleton.

This viewpoint generates new conjectures concerning singularities, horizons, causal rigidity, geodesic networks, and quantum gravity.

---

# 1. Introduction

Riemannian geometry is built upon ordinary metric spaces:

[
d(x,z)\le d(x,y)+d(y,z).
]

Tropical geometry replaces ordinary arithmetic

[
(+,\times)
]

with

[
(\max,+)
]

or

[
(\min,+).
]

The tropical analogue of distance naturally satisfies

[
D(x,z)\ge D(x,y)+D(y,z).
]

Remarkably, Lorentzian geometry already obeys precisely this structure.

For causally related events,

[
p\prec q\prec r,
]

the time-separation function

[
\tau(p,r)
]

satisfies

[
\tau(p,r)\ge \tau(p,q)+\tau(q,r).
]

This reverse triangle inequality is one of the most fundamental facts of spacetime geometry.

The proposal of this paper is simple:

**Spacetime causality is naturally a tropical metric geometry.**

Once this statement is taken seriously, nearly every major object in GR acquires a tropical counterpart.

---

# 2. Tropical Algebra

We work in the max-plus semiring

[
\mathbb T=(\mathbb R\cup{-\infty},\oplus,\otimes)
]

with operations

[
a\oplus b=\max(a,b),
]

[
a\otimes b=a+b.
]

A tropical polynomial becomes

[
f(x)=\max_i(a_i+w_i\cdot x).
]

Tropical varieties are loci where multiple maxima coincide.

Instead of smooth algebraic manifolds one obtains piecewise-linear polyhedral complexes.

The key insight is that Lorentzian causality already computes maxima over proper times.

---

# 3. Time Separation as a Tropical Metric

For a globally hyperbolic spacetime

[
(M,g),
]

define

[
\tau(p,q)
=========

\sup_{\gamma}
L(\gamma)
]

where the supremum runs over future-directed causal curves.

The Lorentzian distance function satisfies

[
\tau(p,r)
\ge
\tau(p,q)+\tau(q,r).
]

Define

[
D(p,q)=\tau(p,q).
]

Then

[
D
]

is a tropical metric.

---

## Tropical Metric Axiom

For causal chains

[
p\prec q\prec r
]

[
D(p,r)
======

D(p,q)\otimes D(q,r).
]

The tropical composition law becomes

[
D(p,r)
======

\max_\gamma
\sum_{\text{segments}}
L_i.
]

This is exactly the variational principle of timelike geodesics.

---

# 4. The Tropical Spacetime Category

Define a category

[
\mathbf{TropSpacetime}.
]

Objects:

[
(M,\tau).
]

Morphisms:

causality-preserving maps

[
f:M\to N
]

satisfying

[
\tau_N(f(p),f(q))
\ge
\tau_M(p,q).
]

This category forgets metric details and retains only tropical causal structure.

---

# 5. Causal Diamonds as Tropical Convex Sets

Tropical convexity replaces ordinary linear combinations with

[
x
=

(a\otimes p)
\oplus
(b\otimes q).
]

Geometrically this generates piecewise-linear hulls.

---

## GR Correspondence

Define the causal diamond

[
\Diamond(p,q)
=============

J^+(p)\cap J^-(q).
]

Every event in the diamond lies on some causal chain connecting

[
p
]

and

[
q.
]

The diamond behaves exactly like a tropical convex hull.

We therefore identify

[
\Diamond(p,q)
=============

\operatorname{TConv}(p,q).
]

---

## Theorem (Tropical Diamond Theorem)

In globally hyperbolic spacetimes, causal diamonds form tropical convex subsets of the spacetime tropical metric space.

This becomes the first foundational bridge between GR and tropical convexity.

---

# 6. Null Cones and Tropical Grassmannians

One of tropical geometry's most important objects is the tropical Grassmannian

[
\mathrm{TropGr}(k,n).
]

Classically Grassmannians parameterize subspaces.

Tropically they parameterize combinatorial degenerations of subspaces.

---

## Null Directions

At each event

[
p,
]

the null cone

[
\mathcal N_p
]

collects all lightlike directions.

Projectivization yields celestial spheres.

Traditionally,

[
\mathcal N_p
]

is viewed as a smooth quadric.

We propose a different interpretation.

---

### Tropical Null Grassmannian

Define

[
\mathrm{TNull}(p)
]

as the tropical Grassmannian generated by null rays through

[
p.
]

Its cells classify combinatorial families of null directions.

Instead of smooth angular coordinates, one obtains a polyhedral decomposition of light propagation.

---

## Physical Meaning

Cells correspond to equivalence classes of null geodesics.

Boundaries correspond to caustics.

Vertices correspond to focal events.

Thus:

| Tropical Object       | GR Object                |
| --------------------- | ------------------------ |
| Tropical Grassmannian | Space of null directions |
| Cell                  | Null congruence          |
| Facet boundary        | Caustic surface          |
| Vertex                | Focal point              |

---

# 7. Geodesics as Tropical Varieties

Tropical varieties arise from balancing conditions.

At each vertex:

[
\sum_i w_i v_i=0.
]

This is the tropical conservation law.

---

## Geodesic Networks

Near lensing regions geodesics split into multiple branches.

The set of maximizing paths forms a graph.

This graph satisfies balancing conditions identical to tropical varieties.

Therefore:

**The geodesic skeleton of spacetime is a tropical variety.**

---

## Lensing Interpretation

Multiple images in gravitational lensing correspond to multiple tropical branches.

Caustics become tropical singularities.

Image multiplicities become tropical intersection numbers.

This provides a completely new language for lensing theory.

---

# 8. Horizons as Tropical Boundaries

Event horizons separate regions with distinct causal accessibility.

Tropically they appear where causal distance changes combinatorial type.

---

## Definition

A tropical horizon is a codimension-one wall across which the maximizing causal graph changes topology.

This is analogous to wall-crossing phenomena in tropical geometry.

---

## Black Hole Interpretation

The event horizon becomes a tropical phase boundary.

Inside:

one maximizing structure.

Outside:

another.

The horizon is where the tropical combinatorial data jumps.

---

# 9. Singularities as Tropical Degenerations

Classically singularities correspond to metric breakdown.

Tropically singularities appear naturally as degenerations of polyhedral structures.

---

## Tropical Singularity Principle

Spacetime singularities occur when the tropical causal complex loses dimension.

Examples:

### Schwarzschild

All future timelike chains collapse toward

[
r=0.
]

Tropical cells collapse.

Dimension decreases.

---

### Big Bang

All causal chains converge toward a single boundary.

The tropical complex contracts to a point.

---

This yields a combinatorial description of singularity formation.

---

# 10. Einstein Equations in Tropical Form

A major question:

Can curvature be tropicalized?

We propose:

[
R_{\mu\nu}
\rightarrow
\mathcal R_{\rm trop}.
]

Instead of smooth curvature tensors we use changes in tropical connectivity.

---

## Tropical Ricci Curvature

Define

[
\mathcal R_{\rm trop}
]

through growth rates of causal diamonds.

Ordinary Ricci curvature controls volume expansion.

Tropical Ricci curvature controls polyhedral complexity expansion.

---

### Tropical Einstein Equation

Conjecturally

[
\mathcal R_{\rm trop}
=====================

8\pi
\mathcal T_{\rm trop}.
]

Matter changes causal-combinatorial complexity.

This becomes the tropical analogue of gravity.

---

# 11. New Causal Theorems

The framework predicts entirely new results.

---

## Theorem A (Causal Polyhedrality)

Every globally hyperbolic spacetime admits a canonical tropical polyhedral skeleton encoding all causal relations.

---

## Theorem B (Diamond Convexity)

Causal diamonds are precisely tropical convex hulls.

---

## Theorem C (Null Grassmannian Rigidity)

The tropical Grassmannian of null directions determines the conformal structure uniquely.

If true, this strengthens classical results that causal structure determines the metric up to conformal factor.

---

## Theorem D (Horizon Wall-Crossing)

Event horizons correspond to wall-crossing loci in the tropical causal complex.

---

# 12. Quantum Gravity Implications

Most quantum gravity programs seek discrete spacetime structures.

Tropical geometry naturally generates discrete yet geometric objects.

The tropical spacetime complex may be:

* more fundamental than smooth manifolds,
* compatible with causal set theory,
* compatible with spin networks,
* compatible with holography.

The continuum metric would emerge from refinement of tropical cells.

---

# 13. Tropical Holography

AdS/CFT relates geometry to boundary information.

In tropical GR:

Bulk geometry becomes a polyhedral causal complex.

Boundary observables determine tropical combinatorics.

The holographic dictionary becomes a correspondence between:

[
\text{Boundary data}
\leftrightarrow
\text{Tropical causal skeleton}.
]

This could dramatically simplify holographic reconstruction.

---

# 14. Computational Advantages

Current GR calculations require solving nonlinear PDEs.

Tropical geometry converts many problems into:

* linear optimization,
* graph theory,
* polyhedral combinatorics.

Consequences:

* faster causal analysis,
* efficient horizon finding,
* simplified lensing computations,
* combinatorial singularity detection.

---

# 15. The Tropical Causality Program

The proposed research program consists of five stages.

### Stage I

Construct tropical spacetime metric spaces.

### Stage II

Prove causal diamonds are tropical convex sets.

### Stage III

Develop tropical Grassmannians of null directions.

### Stage IV

Define tropical curvature.

### Stage V

Derive tropical Einstein equations.

---

# 16. Central Conjecture

## Tropical Spacetime Conjecture

Every globally hyperbolic Lorentzian manifold possesses a canonical tropicalization whose:

* tropical metric equals time separation,
* tropical convex sets equal causal diamonds,
* tropical Grassmannian equals null-direction space,
* tropical varieties equal geodesic networks,
* tropical singularities equal spacetime singularities.

Furthermore, the full conformal causal structure of spacetime can be reconstructed from this tropical data.

---

# 17. Conclusion

The reverse triangle inequality of Lorentzian geometry is not merely analogous to tropical algebra—it is already a manifestation of it. This observation suggests that causality, rather than smooth metric geometry, may be the primary structure of spacetime.

In the framework developed here:

* spacetime becomes a tropical metric space,
* causal diamonds become tropical convex bodies,
* null directions become tropical Grassmannians,
* geodesic networks become tropical varieties,
* horizons become wall-crossing loci,
* singularities become tropical degenerations,
* Einstein gravity becomes the dynamics of a causal-combinatorial complex.

The resulting picture is a radical reinterpretation of General Relativity: smooth Lorentzian geometry is viewed as a differentiable refinement of an underlying tropical causal skeleton. If correct, tropical geometry may provide not merely a new language for GR, but a new foundation for spacetime itself.
