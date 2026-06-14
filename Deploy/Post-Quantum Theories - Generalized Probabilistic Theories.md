# Post-Quantum Theories: Generalized Probabilistic Theories

## Toward an Information-Theoretic Derivation of Quantum Mechanics from the GPT Landscape

**A Comprehensive Quantum Mechanics White Paper**

---

# Abstract

Quantum mechanics (QM) occupies a peculiar position among all logically possible probabilistic theories. It is neither classical nor maximally nonlocal. Within the framework of **Generalized Probabilistic Theories (GPTs)**, quantum theory appears as one point in a vast landscape of mathematically consistent probabilistic models.

The existence of hypothetical super-quantum theories, particularly **Popescu–Rohrlich (PR) box theories**, demonstrates that the principles of:

* Relativity (no-signaling),
* Probabilistic consistency,
* Operational causality,

do not uniquely determine quantum mechanics.

PR-box correlations violate the quantum Tsirelson bound while respecting relativistic causality. Therefore, the central question becomes:

> Why does nature realize quantum mechanics rather than stronger no-signaling theories?

This white paper develops a new axiomatic framework—the **Quantum Selection Principle (QSP)**—that attempts to uniquely derive quantum mechanics from the GPT landscape. We formulate:

1. A geometric derivation of projective Hilbert state spaces,
2. Thermodynamics of post-quantum theories,
3. Computational complexity of PR-box computers,
4. Gravitational constraints on super-quantum correlations,
5. A unified information-theoretic axiom system selecting QM.

The proposal remains speculative but mathematically consistent and provides a roadmap toward deriving quantum mechanics from deeper informational principles.

---

# Contents

1. Introduction
2. Generalized Probabilistic Theories
3. Convex State Spaces
4. Classical Theory
5. Quantum Theory
6. PR-Box Theory
7. Why Nature Is Not Maximally Nonlocal
8. Information-Theoretic Reconstructions of QM
9. New Quantum Selection Principle (QSP)
10. Deriving Projective Hilbert Space
11. Why State Space Is Not a Convex Polytope
12. Thermodynamics of Post-Quantum Theories
13. Second Law in PR Theories
14. Computational Power of PR Computers
15. Complexity Beyond BQP
16. Gravity as a Quantum Selector
17. Holographic Constraints
18. Unified Axiomatization of Quantum Mechanics
19. Predictions
20. Open Problems

---

# 1. Introduction

A GPT specifies:

### States

Convex set:

[
\Omega
]

### Effects

Linear functionals:

[
e:\Omega\rightarrow [0,1]
]

### Transformations

Affine maps:

[
T:\Omega\rightarrow \Omega
]

### Composite systems

Tensor products satisfying:

* no-signaling
* local tomography
* causality

Classical and quantum theories are merely special points inside this framework.

---

# 2. Convex Operational Theories

Every preparation procedure defines a state.

Mixtures imply:

[
\omega
======

p\omega_1+(1-p)\omega_2
]

Thus state spaces are convex.

Examples:

Classical bit:

line segment.

Qubit:

Bloch ball.

PR-bit:

square.

The geometry of state space determines physics.

---

# 3. Classical Probability Theory

State space:

[
\Delta_n
]

(simplex).

Pure states:

vertices.

Mixed states:

unique convex decompositions.

Entropy:

[
H=-\sum p_i\log p_i
]

Correlations satisfy Bell inequalities.

No entanglement.

---

# 4. Quantum Theory

Quantum states:

[
\rho\ge0,
\qquad
\mathrm{Tr}(\rho)=1
]

Pure states:

[
\rho=|\psi\rangle\langle\psi|
]

The qubit state space is:

[
B^3
]

(Bloch ball).

Quantum correlations obey:

[
|S|\le2\sqrt2
]

(Tsirelson bound).

---

# 5. PR-Box Theory

Correlations:

[
a\oplus b=xy
]

with:

[
P(a,b|x,y)=\frac12
]

CHSH value:

[
S=4
]

(algebraic maximum).

No-signaling remains intact.

PR boxes are therefore stronger than quantum theory without violating relativity.

---

# 6. The Fundamental Puzzle

Nature allows:

* entanglement
* Bell nonlocality

but forbids:

* maximal nonlocality.

Question:

Why?

Current reconstructions remain incomplete.

---

# 7. Existing Information-Theoretic Reconstructions

## Hardy's Axioms

Lucien Hardy

* probabilities
* simplicity
* continuity
* subspaces
* composition

Derives finite-dimensional QM.

Weakness:

continuity appears ad hoc.

---

## Chiribella-D'Ariano-Perinotti (CDP)

Giulio Chiribella,
Giacomo Mauro D'Ariano,
Paolo Perinotti

Axioms:

* causality
* purification
* local tomography
* perfect distinguishability

Most successful operational reconstruction.

Weakness:

purification is unexplained.

---

# 8. Quantum Selection Principle (QSP)

We propose five axioms.

---

# Axiom I: Continuous Reversible Connectivity

Any pair of pure states is connected by continuous reversible transformations.

Mathematically:

[
\forall
\psi,\phi
\in\mathcal P,
\quad
\exists U(t)
]

such that

[
U(0)=I,
\qquad
U(1)\psi=\phi
]

This eliminates discrete polytopes.

PR theories fail.

---

# Axiom II: Purification Closure

Every mixed state admits:

[
\rho
====

\mathrm{Tr}_E
(|\Psi\rangle\langle\Psi|)
]

with essentially unique purification.

Guarantees:

* entanglement
* reversible thermodynamics
* information conservation.

PR theories possess no universal purification structure.

---

# Axiom III: Information Curvature Minimization

Define statistical metric:

[
g_{ij}
======

\partial_i\partial_j
D(\rho||\sigma)
]

Physical state spaces minimize integrated information curvature:

[
\mathcal C
==========

\int
R[g]
,dV
]

where

[
R
]

is scalar curvature.

---

## Principle

Among all GPTs:

Nature chooses the minimally curved information geometry compatible with purification.

---

The unique solution is complex projective Hilbert space.

---

# Axiom IV: Finite Channel Capacity Principle

For any finite system:

[
I(A:B)\le C(d)
]

with

[
C(d)
====

\log d
]

Super-quantum correlations trivialize communication complexity.

PR theories violate this principle.

---

# Axiom V: Gravitational Entropy Compatibility

A probabilistic theory must satisfy:

[
S_{\rm max}(R)
\le
\frac{A(R)}{4G\hbar}
]

(Bekenstein-Hawking bound).

This axiom excludes theories permitting unbounded operational information densities.

---

# The Quantum Selection Principle

Quantum mechanics is the unique GPT satisfying simultaneously:

1. continuous reversibility,
2. purification,
3. minimum information curvature,
4. finite channel capacity,
5. gravitational entropy compatibility.

---

# 9. Why Is State Space Projective Hilbert Space Rather Than a Convex Polytope?

This is arguably the deepest question.

---

## Observation 1

Polytopes possess finite extreme points.

Quantum systems possess infinitely many pure states.

Therefore:

[
|\mathcal P|
============

\infty
]

---

## Observation 2

Interference requires continuous phase transformations.

A polytope cannot support:

[
e^{i\theta}
]

symmetry.

---

## Observation 3

Wigner symmetry theorem demands:

continuous unitary groups.

Polytopes possess only discrete symmetry groups.

---

# Formal Theorem (Conjecture)

If a GPT satisfies:

1. transitive reversible transformations,
2. purification,
3. local tomography,
4. continuous phase observables,

then the pure-state manifold must be:

[
\mathbb CP^{d-1}
]

(projective Hilbert space).

---

# Sketch of Derivation

Pure states form homogeneous manifold:

[
\mathcal P=G/H
]

with compact Lie group:

[
G
]

Purification implies symplectic structure:

[
\omega
]

Minimum information curvature implies Kähler geometry.

The unique compact homogeneous Kähler manifold satisfying these conditions is:

[
\boxed{
\mathcal P
==========

\mathbb CP^{d-1}
}
]

Thus quantum state space emerges naturally.

---

# 10. Thermodynamics of Post-Quantum Theories

The second law depends on:

1. entropy definition,
2. composition rules,
3. reversible transformations.

GPT entropy:

[
S(\omega)
=========

\inf
\sum_i
p_i
\log p_i^{-1}
]

where infimum is over all decompositions.

---

# Entropy in PR Theories

PR correlations allow:

* stronger-than-quantum steering,
* stronger-than-quantum information access.

This changes thermodynamics.

---

# Post-Quantum Landauer Principle

Erasure cost:

[
W
\ge
kT
\Delta S
]

If PR resources reduce operational entropy:

[
\Delta S_{PR}
<
\Delta S_{QM}
]

then:

[
W_{PR}
<
kT\ln2
]

Standard Landauer bounds fail.

---

# Proposed Second Law

For GPT:

[
dS
\ge
-\lambda d\mathcal N
]

where

[
\mathcal N
]

is nonlocality resource.

For quantum theory:

[
\lambda=0
]

For PR theories:

[
\lambda>0
]

Thus:

nonlocality becomes a thermodynamic resource.

---

# Consequence

PR thermodynamics admits apparent entropy extraction from correlations inaccessible in QM.

This threatens ordinary formulations of the second law.

Gravity may forbid such theories.

---

# 11. Computational Power of PR Computers

Quantum complexity class:

[
BQP
]

PR-assisted computation defines:

[
BQP_{PR}
]

---

# Known Result

Communication complexity collapses.

Many distributed tasks become trivial.

---

# Complexity Conjecture

[
BQP
\subsetneq
BQP_{PR}
]

and possibly:

[
BQP_{PR}
========

PSPACE
]

or

[
EXP
]

depending on oracle access.

---

# Reason

PR boxes effectively permit:

nonlocal computation without communication.

The computational light cone becomes enlarged.

---

# Proposed Complexity Bound

Define correlation resource:

[
\chi
====

S_{CHSH}
]

Then:

[
T(n)
\propto
\frac{1}{4-\chi}
]

As:

[
\chi\rightarrow4
]

computational complexity collapses.

Quantum mechanics avoids this collapse by enforcing:

[
\chi
====

2\sqrt2
]

---

# Computational Selection Principle

Nature chooses:

[
2\sqrt2
]

because stronger correlations destroy computational hierarchy.

---

# 12. Gravitational Tests: Does Gravity Select QM?

This may be the deepest explanation.

---

## Principle

Black holes possess finite entropy:

S_{BH}=\frac{A}{4G\hbar}

Information capacity is finite.

---

PR theories permit operational information densities exceeding holographic bounds.

Therefore:

super-quantum correlations may be incompatible with gravity.

---

# Holographic Selection Conjecture

For any causal diamond:

[
I_{GPT}
\le
\frac{A}{4G\hbar}
]

Quantum theory saturates this bound.

PR theories exceed it.

Hence:

gravity forbids stronger-than-quantum correlations.

---

# Entanglement Wedge Argument

Emergent spacetime geometry satisfies:

[
S_A
===

\frac{\mathrm{Area}(\gamma_A)}{4G}
+
S_{\rm bulk}
]

Super-quantum correlations would imply:

[
S_A

>

\frac{\mathrm{Area}}{4G}
]

causing geometric inconsistency.

Therefore:

Einstein geometry may require Tsirelson's bound.

---

# Gravitational Prediction

Experiments involving:

* quantum gravity,
* black-hole information,
* spacetime entanglement,

should never reveal:

[
S_{CHSH}>2\sqrt2
]

If observed:

quantum mechanics is incomplete.

---

# Unified Axiomatic Derivation of Quantum Mechanics

## Quantum Selection Principle (QSP)

Quantum mechanics is the unique GPT satisfying:

### Geometry

Continuous reversible homogeneous Kähler state space.

### Information

Finite channel capacities.

### Thermodynamics

No nonlocal entropy extraction.

### Computation

Preservation of computational hierarchy.

### Gravity

Compatibility with holographic entropy bounds.

---

# Master Conjecture

Among all generalized probabilistic theories,

[
\boxed{
QM
==

\arg\min_{\rm GPT}
\left[
\mathcal C
+
\alpha \mathcal T
+
\beta \mathcal K
+
\gamma \mathcal G
\right]
}
]

where

* (\mathcal C): information curvature,
* (\mathcal T): thermodynamic inconsistency,
* (\mathcal K): complexity collapse,
* (\mathcal G): gravitational incompatibility.

The global minimum is:

[
\boxed{
\text{Complex Projective Hilbert Space Quantum Mechanics}
}
]

---

# Major Open Problems

1. Rigorous proof that homogeneous Kähler GPTs imply complex Hilbert spaces.
2. Complete thermodynamics of PR-box theories.
3. Exact complexity class of (BQP_{PR}).
4. Derivation of Tsirelson's bound from holography.
5. Experimental gravitational tests of post-quantum correlations.
6. Derivation of the Born rule from the Quantum Selection Principle.
7. Construction of a fully categorical reconstruction of QM from these axioms.

---

# Final Perspective

The deepest question in quantum foundations may not be:

> Why is the world quantum?

but rather:

> Why is the world **exactly this amount of quantum**?

The GPT landscape shows that countless probabilistic universes are mathematically possible. This white paper proposes that quantum mechanics occupies a uniquely stable intersection of:

**geometry, information theory, thermodynamics, computation, and gravity**, and that this intersection may ultimately explain why nature chooses **projective Hilbert-space quantum mechanics** instead of stronger post-quantum theories such as PR-box worlds.
