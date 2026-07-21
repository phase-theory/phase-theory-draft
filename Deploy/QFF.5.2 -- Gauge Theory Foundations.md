# Quantum Field Theory in Finite Volume as a Systematic Physical Framework

# Volume V — Spin, Gauge Fields, and QCD

## Part II — Gauge Theory Foundations

---

# 5. Gauge Fields on Compact Spaces

## 5.1 Introduction

Gauge theories possess a fundamentally geometric character. In infinite volume, gauge fields are connections on principal bundles over Minkowski spacetime. Compactification changes the topology of the underlying manifold and thereby modifies the global structure of gauge fields.

The finite-volume formulation of gauge theory is therefore not merely a discretized version of ordinary gauge theory but a genuinely distinct geometric theory whose observables depend on both local dynamics and global topology.

---

## 5.2 Principal Bundle Structure

Let

[
M=\mathbb R\times \Sigma
]

where

[
\Sigma
]

is a compact spatial manifold.

Gauge fields are connections on a principal bundle

[
P(M,G),
]

with structure group

[
G.
]

Examples include

[
U(1),
\qquad
SU(2),
\qquad
SU(3).
]

The connection one-form is

[
A=A_\mu^aT^a dx^\mu.
]

---

## 5.3 Compactification and Topology

For

[
\Sigma=\mathbb T^3,
]

noncontractible cycles exist:

[
\gamma_i,
\qquad
i=1,2,3.
]

Gauge fields may possess nontrivial holonomies around these cycles.

Consequently the gauge configuration space becomes disconnected into topological sectors.

---

## 5.4 Field Strength

The curvature two-form is

[
F=dA+A\wedge A.
]

In component notation,

[
F_{\mu\nu}^a
============

## \partial_\mu A_\nu^a

\partial_\nu A_\mu^a
+
f^{abc}A_\mu^bA_\nu^c.
]

Compactification leaves the local form unchanged but alters global solutions.

---

## 5.5 Gauge Transformations

Gauge transformations satisfy

[
A_\mu
\rightarrow
A_\mu^U
=======

U A_\mu U^{-1}
+
iU\partial_\mu U^{-1}.
]

On compact manifolds,

[
U(x)
]

must respect boundary conditions and may possess nontrivial winding number.

---

## 5.6 Large Gauge Transformations

Unlike infinitesimal transformations, large gauge transformations cannot be continuously deformed to the identity.

They satisfy

[
U\notin \mathcal G_0.
]

The quotient

[
\mathcal G/\mathcal G_0
]

defines the global gauge structure.

---

## 5.7 Gauge Configuration Space

The physical configuration space is

[
\mathcal A/\mathcal G,
]

where

[
\mathcal A
]

is the space of connections.

Compactification modifies the topology of this quotient.

---

## 5.8 Compact-Space Gauge Modes

Gauge fields admit Fourier decomposition:

[
A_\mu(x)
========

\sum_n
A_{\mu,n}
e^{i2\pi n\cdot x/L}.
]

Unlike scalar fields, the zero modes play a dynamical role.

---

## 5.9 Gauge Vacuum Structure

The vacuum sector becomes

[
\mathcal V
==========

\bigcup_k \mathcal V_k.
]

Different sectors are connected through large gauge transformations.

This structure becomes crucial for non-Abelian gauge theories.

---

## 5.10 Compact Gauge Field Theorem

The physical content of a finite-volume gauge theory is determined not only by local field strengths but also by the global topology of the compact manifold through its noncontractible gauge holonomies.

---

# 6. Wilson Loops

## 6.1 Motivation

Gauge fields themselves are not physical observables.

Physical information is encoded in gauge-invariant quantities.

The most fundamental of these is the Wilson loop.

---

## 6.2 Definition

For a closed curve

[
C,
]

define

[
W(C)
====

{\rm Tr}
,P
\exp
\left(
ig
\oint_C
A_\mu dx^\mu
\right).
]

The symbol

[
P
]

denotes path ordering.

---

## 6.3 Gauge Invariance

Under gauge transformations,

[
W(C)
]

remains invariant.

Wilson loops therefore provide physical observables independent of gauge choice.

---

## 6.4 Holonomy Interpretation

Wilson loops measure the holonomy of the gauge connection.

Geometrically,

[
W(C)
]

describes parallel transport around a closed path.

---

## 6.5 Noncontractible Cycles

On

[
\mathbb T^3,
]

loops wrapping compact directions cannot be shrunk to a point.

The associated observables

[
W_i
===

W(\gamma_i)
]

characterize global gauge structure.

---

## 6.6 Polyakov Loops

For compact Euclidean time,

[
\tau\sim\tau+\beta,
]

define

[
P
=

{\rm Tr}
,
P
\exp
\left(
ig
\int_0^\beta
A_0 d\tau
\right).
]

Polyakov loops diagnose confinement.

---

## 6.7 Area Law

In a confining phase,

[
\langle W(C)\rangle
\sim
e^{-\sigma A(C)}.
]

The coefficient

[
\sigma
]

is the string tension.

---

## 6.8 Perimeter Law

In a deconfined phase,

[
\langle W(C)\rangle
\sim
e^{-\mu P(C)}.
]

The scaling behavior distinguishes phases.

---

## 6.9 Wilson Loop Spectrum

The collection

[
{W(C)}
]

forms a gauge-invariant algebra.

Its eigenvalues encode the global structure of the gauge theory.

---

## 6.10 Wilson Loop Theorem

In finite-volume gauge theory, all topological information about the gauge connection is encoded in the spectrum of Wilson loops wrapping the compact manifold.

---

# 7. Gauge Fixing

## 7.1 Redundancy of Gauge Variables

Gauge fields contain unphysical degrees of freedom.

A consistent quantization requires elimination of this redundancy.

---

## 7.2 Gauge Conditions

A gauge condition takes the form

[
G[A]=0.
]

Common examples include:

Lorenz gauge:

[
\partial_\mu A^\mu=0,
]

Coulomb gauge:

[
\nabla\cdot A=0.
]

---

## 7.3 Compact-Space Constraints

In finite volume, gauge conditions must be compatible with boundary conditions.

Not every infinite-volume gauge choice remains admissible.

---

## 7.4 Faddeev–Popov Construction

Insert

[
1
=

\Delta_{FP}[A]
\int D\alpha,
\delta(G[A^\alpha]).
]

The determinant

[
\Delta_{FP}
]

removes gauge overcounting.

---

## 7.5 Ghost Fields

Introduce anticommuting fields

[
c,
\qquad
\bar c.
]

The ghost action becomes

[
S_{gh}
======

\int
\bar c
,
M_{FP}
,c.
]

---

## 7.6 Gauge-Fixed Action

The full action becomes

[
S
=

S_{YM}
+
S_{gf}
+
S_{gh}.
]

This formulation permits perturbative quantization.

---

## 7.7 Zero-Mode Problem

Compact spaces possess gauge zero modes satisfying

[
M_{FP}\phi=0.
]

These require special treatment because they invalidate naive inversion procedures.

---

## 7.8 Gribov Ambiguities

Distinct gauge configurations may satisfy the same gauge condition.

Such configurations are known as Gribov copies.

Compact manifolds accentuate this phenomenon.

---

## 7.9 Fundamental Modular Region

The physically distinct configurations lie within

[
\mathcal F.
]

Restriction to

[
\mathcal F
]

eliminates redundant copies.

---

## 7.10 Gauge-Fixing Theorem

Finite-volume gauge fixing is equivalent to selecting a representative from each gauge orbit while accounting for compact-space zero modes and Gribov ambiguities.

---

# 8. BRST Structure

## 8.1 Introduction

Gauge fixing breaks manifest gauge symmetry.

The resulting theory retains a hidden symmetry known as BRST symmetry.

This symmetry guarantees consistency and unitarity.

---

## 8.2 BRST Transformations

Introduce a Grassmann parameter

[
\epsilon.
]

The BRST transformations are

[
\delta A_\mu^a
==============

\epsilon
(D_\mu c)^a,
]

[
\delta c^a
==========

-\frac{\epsilon}{2}
f^{abc}
c^bc^c,
]

[
\delta\bar c^a
==============

\epsilon B^a.
]

---

## 8.3 Nilpotency

The BRST operator satisfies

[
Q_{BRST}^2=0.
]

Nilpotency is the central algebraic property of the theory.

---

## 8.4 Cohomology

Physical states satisfy

[
Q_{BRST}|\psi\rangle=0.
]

States differing by

[
Q_{BRST}|\chi\rangle
]

are identified.

The physical Hilbert space is

[
\mathcal H_{phys}
=================

{\rm Ker}(Q_{BRST})
/
{\rm Im}(Q_{BRST}).
]

---

## 8.5 Compact-Space BRST Charge

The BRST charge is

[
Q_{BRST}
========

\int_\Sigma d^3x,J^0_{BRST}.
]

Compactification modifies the mode expansion of this operator.

---

## 8.6 Ghost Number Symmetry

Assign

[
{\rm gh}(c)=1,
\qquad
{\rm gh}(\bar c)=-1.
]

Physical observables possess ghost number zero.

---

## 8.7 BRST-Invariant Action

The gauge-fixed action satisfies

[
Q_{BRST}S=0.
]

This invariance replaces gauge invariance after quantization.

---

## 8.8 BRST and Topology

Large gauge transformations contribute nontrivially to BRST cohomology.

Compact manifolds therefore enrich the structure of physical state spaces.

---

## 8.9 Operator-Algebra Formulation

The BRST complex defines a differential graded algebra

[
(\mathcal A,Q_{BRST}).
]

Physical observables correspond to cohomology classes.

---

## 8.10 BRST Reconstruction Theorem

The physical content of a finite-volume gauge theory is completely characterized by the BRST cohomology of its compact-space gauge configuration space.

---

# Conclusions of Part II

Gauge theories in compact volume possess a richer structure than their infinite-volume counterparts because global topology becomes dynamical. Four central objects emerge:

[
\mathcal A/\mathcal G,
\qquad
W(C),
\qquad
\Delta_{FP},
\qquad
Q_{BRST}.
]

These represent the gauge-orbit space, Wilson-loop observables, Faddeev–Popov structure, and BRST cohomology. Together they provide the mathematical foundation for finite-volume Yang–Mills theory and prepare the way for the treatment of QCD, confinement, topological sectors, and nonperturbative gauge dynamics.

The next part of Volume V is naturally:

### Part III — Non-Abelian Gauge Theory and QCD

9. Yang–Mills Theory in Finite Volume
10. Color Confinement
11. Finite-Volume Gluodynamics
12. Topological Charge and Instantons
13. θ-Vacua in Compact Space
14. Finite-Volume QCD Spectroscopy.
