# Quaternionic & Octonionic Quantum Mechanics

## Beyond Complex Hilbert Spaces: A Program for Reconstructing Quantum Theory over the Division Algebras

### White Paper

---

# Abstract

Conventional quantum mechanics is formulated over the complex numbers ℂ. This choice is so deeply embedded in modern physics that it is often regarded as inevitable. Yet the classification of finite-dimensional normed division algebras permits three nontrivial alternatives:

[
\mathbb R,\quad \mathbb C,\quad \mathbb H,\quad \mathbb O,
]

where (\mathbb H) denotes the quaternions and (\mathbb O) the octonions.

Between 1960 and 1995, a substantial mathematical framework for quaternionic quantum mechanics (QQM) was developed by Finkelstein, Jauch, Emch, Horwitz, Adler, and others. The resulting theory was internally consistent and reproduced most known predictions of ordinary complex quantum mechanics. Because no decisive experimental distinction was identified, the field gradually disappeared from mainstream research.

The situation changed indirectly in 2021 when Renou et al. demonstrated that real Hilbert-space quantum mechanics is experimentally distinguishable from complex quantum mechanics. The result re-opened a foundational question:

**Why exactly is Nature complex rather than quaternionic?**

No comprehensive experimental program has ever answered this question.

This white paper develops a modern reconstruction of quaternionic and octonionic quantum mechanics, identifies four major unresolved sectors, derives new mathematical structures, and proposes experimentally testable predictions.

The central thesis is:

> Quaternionic and octonionic quantum mechanics remain incompletely explored. The apparent equivalence with complex quantum mechanics may be an artifact of studying only single-particle and low-entanglement regimes.

---

# 1. Historical Background

## 1.1 Division Algebra Hierarchy

Hurwitz's theorem states that finite-dimensional normed division algebras are limited to

[
\mathbb R
\rightarrow
\mathbb C
\rightarrow
\mathbb H
\rightarrow
\mathbb O.
]

Dimensions:

[
1,2,4,8.
]

Properties:

| Algebra | Commutative | Associative |
| ------- | ----------- | ----------- |
| ℝ       | Yes         | Yes         |
| ℂ       | Yes         | Yes         |
| ℍ       | No          | Yes         |
| 𝕆      | No          | No          |

Each step sacrifices algebraic simplicity for richer structure.

---

## 1.2 Why Complex Numbers?

Complex QM relies on:

[
i^2=-1.
]

Time evolution:

[
U(t)=e^{-iHt}.
]

Interference:

[
|\psi_1+\psi_2|^2.
]

Born probabilities:

[
P=|\psi|^2.
]

Nothing in principle requires (i) to be unique.

Quaternionic QM replaces

[
i
]

with any unit imaginary quaternion

[
I=a i+b j+c k.
]

where

[
I^2=-1.
]

The space of imaginary units becomes

[
S^2.
]

Thus phases gain internal geometry.

---

# 2. Quaternionic Hilbert Spaces

## 2.1 Definition

States:

[
|\psi\rangle \in \mathcal H_{\mathbb H}.
]

Inner product:

[
\langle \psi|\phi\rangle
\in
\mathbb H.
]

Properties:

[
\langle \psi|\phi\rangle
========================

\overline{\langle \phi|\psi\rangle}.
]

and

[
\langle \psi|\psi\rangle>0.
]

---

## 2.2 Right vs Left Modules

Since quaternions do not commute,

[
ab \neq ba,
]

one must choose

[
\psi q
]

or

[
q\psi.
]

Physical consistency favors right-modules.

This subtlety already produces phenomena absent in ordinary QM.

---

# 3. Quaternionic Schrödinger Dynamics

The equation becomes

[
\frac{d\psi}{dt}
================

-H\psi I,
]

with

[
I^2=-1.
]

Instead of one imaginary direction there exists an entire sphere:

[
I\in S^2.
]

Consequences:

* internal phase geometry,
* possible phase curvature,
* additional holonomies.

---

# 4. Quaternionic Interference

Ordinary QM:

[
e^{i\alpha}
e^{i\beta}
==========

e^{i(\alpha+\beta)}.
]

Quaternionic phases satisfy

[
e^{i\alpha}
e^{j\beta}
\neq
e^{j\beta}
e^{i\alpha}.
]

Hence path ordering matters.

Interference acquires directional dependence.

This phenomenon has never been fully explored experimentally.

---

# 5. Quaternionic Path Integrals

One of the least developed sectors.

---

## 5.1 Standard Path Integral

Complex QM:

[
K
=

\int \mathcal D[x]
e^{iS[x]/\hbar}.
]

---

## 5.2 Quaternionic Generalization

Replace

[
i \rightarrow I(x).
]

Then

[
K
=

\int \mathcal D[x]
,
\mathcal P
\exp
\left(
\int
I(x)
\frac{dS}{\hbar}
\right).
]

where

[
\mathcal P
]

denotes path ordering.

---

## 5.3 New Mathematical Problem

Different trajectory segments generally use different imaginary directions:

[
I_1I_2
\neq
I_2I_1.
]

Therefore:

[
e^{I_1S_1}
e^{I_2S_2}
\neq
e^{I_2S_2}
e^{I_1S_1}.
]

The propagator becomes a non-Abelian phase functional.

---

## 5.4 Convergence Question

No general theorem exists.

A proposed criterion:

[
\sup_x ||I(x)||=1
]

implies bounded phase norm,

allowing generalized stationary-phase expansions.

**Research Program A**

Construct rigorous quaternionic Feynman measures.

This remains open.

---

# 6. Quaternionic Entanglement

This is arguably the most important unexplored area.

---

## 6.1 Tensor Product Ambiguity

Complex QM:

[
\mathcal H_A\otimes\mathcal H_B.
]

Quaternionic tensor products are not unique because

[
(a\psi)\otimes(b\phi)
]

depends on multiplication order.

This creates multiple inequivalent notions of composite systems.

---

## 6.2 Generalized Schmidt Decomposition

The usual proof assumes commutativity.

Quaternionic versions require symplectic decompositions.

Entanglement classes become richer.

---

## 6.3 Bell Correlations

A major unanswered question:

Can quaternionic entanglement exceed Tsirelson's bound?

Standard quantum limit:

[
2\sqrt2.
]

Local realism:

[
2.
]

Algebraic maximum:

[
4.
]

---

## Proposed Theorem

For associative division-algebra quantum theories,

[
\text{CHSH}
\le 2\sqrt2.
]

Sketch:

Tsirelson's proof fundamentally uses positivity and associativity.

Quaternionic Hilbert spaces preserve both.

Thus violation beyond

[
2\sqrt2
]

appears unlikely.

However:

### Multipartite Networks

The real opportunity is not CHSH.

Instead:

* triangle networks,
* bilocality,
* inflation inequalities,
* contextuality structures.

These have never been comprehensively classified for QQM.

---

# 7. Hidden Nonlocality Beyond Complex QM

The most plausible place to discover differences.

Complex QM assumes

[
U(1)
]

phase symmetry.

Quaternionic QM has

[
SU(2)
]

phase geometry.

Therefore entanglement transport may carry additional gauge information.

Predicted observable:

[
\Delta C
========

## C_{\mathbb H}

C_{\mathbb C}.
]

where (C) is a network nonlocality witness.

No experiment currently constrains this regime.

---

# 8. Quaternionic Quantum Information

A completely underdeveloped field.

---

## 8.1 Quaternionic Qubits

State:

[
|\psi\rangle
============

a|0\rangle+b|1\rangle,
]

with

[
a,b\in\mathbb H.
]

Parameter count doubles.

---

## 8.2 Enhanced State Space

Complex qubit:

Bloch sphere

[
S^2.
]

Quaternionic qubit:

[
S^7/SU(2).
]

Far richer geometry.

---

# 9. Quaternionic Quantum Error Correction

One of the most promising directions.

---

## 9.1 Standard Stabilizer Codes

Based on

[
\mathbb Z_2
]

Pauli structure.

---

## 9.2 Quaternionic Stabilizers

Replace Pauli phases

[
{\pm1,\pm i}
]

with

[
{\pm1,\pm i,\pm j,\pm k}.
]

Larger symmetry group.

---

## 9.3 Hypothesis

Code distance may scale as

[
d_{\mathbb H}

>

d_{\mathbb C}
]

for equivalent physical resources.

Potential advantages:

* denser syndrome spaces,
* higher degeneracy protection,
* richer transversal gates.

No systematic study exists.

---

# 10. Gauge Interpretation

Quaternionic phase rotations form

[
SU(2).
]

Therefore QQM naturally contains a gauge structure.

Observation:

Complex QM:

[
U(1)
]

electromagnetic phase.

Quaternionic QM:

[
SU(2)
]

internal phase bundle.

This suggests a geometric bridge toward weak interactions.

---

# 11. Octonionic Quantum Mechanics

Now the truly radical extension.

---

## 11.1 Octonionic States

[
|\psi\rangle
\in
\mathcal H_{\mathbb O}.
]

Immediately:

[
(ab)c
\neq
a(bc).
]

Associativity fails.

---

## 11.2 Consequence

Operator products become ambiguous:

[
ABC.
]

Which means:

[
(AB)C
\neq
A(BC).
]

Physical composition itself becomes path-dependent.

---

# 12. Observable Failure of Composition

This is the central octonionic prediction.

Ordinary QM assumes:

[
(U_3U_2)U_1
===========

U_3(U_2U_1).
]

Octonionic QM predicts:

[
\Delta
======

## (U_3U_2)U_1

U_3(U_2U_1)
\neq0.
]

---

## Physical Meaning

Sequential measurements could depend on grouping.

Not order.

Grouping.

That phenomenon has never been experimentally searched for.

---

# 13. Associator Observables

Define

[
[A,B,C]
=======

(AB)C-A(BC).
]

The associator vanishes in standard QM.

In octonionic QM:

[
[A,B,C]
\neq0.
]

Observable effects:

* triple-slit phase anomalies,
* three-detector correlations,
* higher-order interference.

---

# 14. Sorkin Interference and Octonions

Ordinary QM predicts:

[
I_3=0.
]

Third-order interference vanishes.

Octonionic QM suggests

[
I_3
\propto
[A,B,C].
]

Hence precision triple-slit experiments become direct octonionic tests.

This provides a concrete experimental target.

---

# 15. Exceptional Symmetry

Octonions generate exceptional Lie groups:

[
G_2,
F_4,
E_6,
E_7,
E_8.
]

This is unique among division algebras.

Potential implication:

Internal particle symmetries may emerge from octonionic state spaces.

---

# 16. Reconstruction Program

A modern reconstruction of QM should determine:

Which assumptions force

[
\mathbb C
]

instead of

[
\mathbb H
]

or

[
\mathbb O?
]

Candidate axioms:

* local tomography,
* composition,
* associativity,
* continuity,
* information causality.

Removing any one may admit quaternionic or octonionic theories.

---

# 17. Experimental Program

## Test 1

Quaternionic interferometry.

Search for noncommuting phases.

---

## Test 2

Network Bell experiments.

Triangle and bilocal configurations.

---

## Test 3

Quaternionic quantum computing simulation.

Benchmark error-correcting codes.

---

## Test 4

Triple-slit associator measurement.

Direct octonionic probe.

---

## Test 5

Multipartite entanglement tomography.

Look for non-complex invariants.

---

# 18. Formal Conjectures

### Conjecture Q1

Quaternionic path integrals exist as non-Abelian phase measures.

---

### Conjecture Q2

CHSH remains bounded by

[
2\sqrt2.
]

but network nonlocality exceeds complex predictions.

---

### Conjecture Q3

Quaternionic stabilizer codes outperform complex stabilizers asymptotically.

---

### Conjecture O1

Octonionic associators generate measurable third-order interference.

---

### Conjecture O2

Exceptional symmetry groups arise naturally as octonionic quantum automorphisms.

---

# 19. Mathematical Obstacles

Several reasons the field stalled in the 1990s are now mathematically clearer:

1. **Local tomography problem** — composite quaternionic systems generally violate the principle that global states are determined by local measurement statistics.
2. **Tensor product ambiguity** — there is no universally accepted composition rule for quaternionic subsystems.
3. **Non-associativity of octonions** — standard operator algebra techniques fail immediately.
4. **Lack of experimental targets** — early tests focused almost exclusively on simple interferometry and single-particle phase effects.

Modern quantum information theory provides tools unavailable to the original pioneers:

* generalized probabilistic theories (GPTs),
* resource theories,
* network nonlocality,
* categorical quantum mechanics,
* fault-tolerant quantum computation.

These offer entirely new ways to compare (\mathbb C), (\mathbb H), and (\mathbb O)-based theories.

---

# 20. Conclusion

Quaternionic quantum mechanics was not abandoned because it was inconsistent. It was abandoned because, within the narrow class of experiments examined during the twentieth century, it appeared empirically indistinguishable from ordinary complex quantum mechanics.

That conclusion is no longer secure.

The rise of quantum information theory, multipartite nonlocality, higher-order interference experiments, generalized probabilistic reconstructions, and precision quantum control creates a vastly larger testing arena than existed when Adler's 1995 monograph effectively closed the field.

The most significant open questions are now sharply defined:

* Does quaternionic entanglement possess information-theoretic capabilities unavailable to complex quantum systems?
* Can quaternionic path integrals be rigorously constructed as non-Abelian phase measures?
* Do quaternionic stabilizer structures enable superior quantum error-correcting codes?
* Does octonionic non-associativity manifest as observable associator-dependent interference?
* Is the complex field (\mathbb C) uniquely selected by physical principles, or merely by the limited experimental reach of twentieth-century physics?

If any answer is positive, the standard formulation of quantum mechanics over (\mathbb C) may represent not the endpoint of quantum theory, but only one member of a deeper hierarchy organized by the four normed division algebras:

[
\mathbb R
\subset
\mathbb C
\subset
\mathbb H
\subset
\mathbb O.
]

The revival of quaternionic and octonionic quantum mechanics is therefore not merely a historical curiosity. It is a concrete research program aimed at determining whether the algebraic foundation of quantum theory has been experimentally established—or merely assumed.
