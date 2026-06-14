# Indefinite Causal Order & Quantum Causality

## From Quantum Switches to Process-Matrix Field Theory, Quantum Gravity, and Computational Complexity

### A Comprehensive Quantum Mechanics White Paper

---

# Abstract

Quantum mechanics traditionally assumes that physical events occur within a definite causal structure: operation A precedes operation B, or vice versa. The emergence of the quantum switch and the process matrix formalism has demonstrated that quantum theory permits situations in which the order of events itself exists in coherent superposition. Such phenomena cannot be represented by any classical stochastic mixture of causal orders.

Indefinite causal order (ICO) has become one of the most profound conceptual developments in modern quantum foundations because it suggests that spacetime causal structure may not be fundamental. Experimental demonstrations have shown communication and computational advantages, yet the ontology, field-theoretic extension, gravitational interpretation, and computational complexity of ICO remain largely undeveloped.

This white paper develops a comprehensive formal framework for quantum causality and proposes:

1. **Causal Indefiniteness Resource Theory (CIRT)**, demonstrating that indefinite causal order constitutes a resource beyond entanglement and coherence.
2. **Process Matrix Quantum Field Theory (PM-QFT)**, extending process matrices to continuous spacetime and quantum fields.
3. **Quantum Switch Gravity (QSG)**, formalizing causal superpositions of spacetime geometries and topologies.
4. **A new computational complexity hierarchy**, introducing complexity classes based upon access to indefinite causal order.

The central thesis is:

> Causal structure itself is a quantum degree of freedom.

The quantum state describes not merely matter and fields but also the ordering relations among physical events.

---

# 1. Introduction

Classical physics assumes:

```
A → B
or
B → A
```

with a fixed partial order.

Quantum theory already generalized:

* states → superpositions,
* trajectories → path integrals,
* particle number → Fock spaces,
* geometry → quantum gravity proposals.

Indefinite causal order suggests another generalization:

```
(A→B)+(B→A)
```

where causal order itself becomes quantum.

This possibility is experimentally realized through the quantum switch and theoretically formalized by the process matrix framework.

The implications are potentially enormous:

* spacetime may emerge from quantum causal correlations,
* quantum gravity may require causally nonseparable histories,
* computational power may exceed standard circuit models.

---

# 2. The Quantum Switch

## Standard Circuit

A control qubit:

|0⟩ :

```
A→B
```

|1⟩ :

```
B→A
```

The quantum switch prepares

[
|\psi_c\rangle
=\alpha |0\rangle+\beta |1\rangle
]

giving

[
|\Psi\rangle
============

\alpha |0\rangle\otimes(B\circ A)|\phi\rangle
+
\beta |1\rangle\otimes(A\circ B)|\phi\rangle
]

which is not reducible to a probabilistic mixture.

---

# 3. Process Matrix Formalism

The process matrix formalism removes background causal assumptions.

Operations:

[
M_A,;M_B
]

Probability:

[
P(M_A,M_B)
==========

{\rm Tr}
\left[
W(M_A\otimes M_B)
\right]
]

where

[
W
]

is the process matrix.

Unlike density matrices:

* (W) need not correspond to a state on a fixed spacetime,
* (W) encodes causal relations themselves.

---

# 4. Causal Nonseparability

Definite order processes:

[
W^{A\prec B}
]

or

[
W^{B\prec A}
]

Causal mixtures:

[
W
=

pW^{A\prec B}
+
(1-p)W^{B\prec A}
]

Indefinite order:

[
W
\neq
pW^{A\prec B}
+
(1-p)W^{B\prec A}
]

Such processes are called **causally nonseparable**.

---

# 5. Causal Witnesses

Analogous to entanglement witnesses.

A causal witness:

[
S
]

satisfies

[
{\rm Tr}(SW)\ge0
]

for all causally separable processes.

Violation:

[
{\rm Tr}(SW)<0
]

certifies indefinite causal order.

---

# 6. Resource Theory of Causal Indefiniteness (CIRT)

The major unresolved question:

> Is causal indefiniteness merely another form of coherence or entanglement?

We argue no.

---

# 7. Causal Hilbert Space

Introduce

[
\mathcal H_C
]

whose basis vectors are causal orders:

[
|A\prec B\rangle,
\qquad
|B\prec A\rangle,
\qquad
|A\parallel B\rangle,
\qquad
|A\leftrightarrow B\rangle
]

General state:

[
|\Omega\rangle
==============

\sum_i
c_i
|C_i\rangle
]

This Hilbert space is independent of ordinary system Hilbert spaces.

Therefore:

[
\mathcal H
==========

\mathcal H_{\rm matter}
\otimes
\mathcal H_C
]

Causal degrees of freedom become genuine quantum variables.

---

# 8. Causal Entropy

Define causal density matrix:

[
\rho_C
======

{\rm Tr}_{\rm matter}
|\Omega\rangle\langle\Omega|
]

Causal entropy:

[
S_C
===

-{\rm Tr}
(\rho_C\ln\rho_C)
]

This measures uncertainty of causal structure itself.

Properties:

* vanishes for definite order,
* maximal for equal superpositions,
* independent of entanglement entropy.

---

# 9. Causal Entanglement

Define:

[
|\Psi\rangle
============

\frac{
|0\rangle|A\prec B\rangle
+
|1\rangle|B\prec A\rangle
}{\sqrt2}
]

Matter becomes entangled with causal structure.

The entanglement entropy differs from ordinary Bell entanglement because one subsystem is the causal ordering relation itself.

This constitutes a new resource.

---

# 10. Resource Monotones

Define:

### Causal Coherence

[
C_{\rm caus}
============

\sum_{i\neq j}
|\rho_{C,ij}|
]

### Causal Negativity

[
N_C
===

\frac{
||W^{T_C}||_1-1
}{2}
]

### Causal Relative Entropy

[
R_C
===

\min_{W_s}
S(W||W_s)
]

These vanish for definite order and are independent of ordinary entanglement monotones.

---

# 11. Theorem: ICO Is Strictly Beyond Entanglement

Consider:

### State 1

Maximally entangled Bell state.

No causal superposition.

### State 2

Product matter state.

Maximal causal superposition.

Then

[
E_1>E_2
]

but

[
R_C(2)>R_C(1)=0
]

Thus:

Entanglement ordering and causal ordering are incomparable.

Therefore:

> Indefinite causal order is a fundamentally new quantum resource.

---

# 12. Process Matrix Quantum Field Theory (PM-QFT)

Current process matrices assume finite-dimensional systems.

Quantum gravity requires fields.

Introduce spacetime event operators:

[
\Phi(x)
]

and process functional

[
\mathcal W[\Phi]
]

such that

[
P[\Phi]
=======

\int
D\Phi
,
\mathcal W[\Phi]
]

This generalizes

[
W
]

to continuous spacetime.

---

# 13. Causal Path Integrals

Ordinary path integral:

[
Z
=

\int D\phi
e^{iS[\phi]}
]

PM-QFT:

[
Z_C
===

\sum_C
\int D\phi
e^{iS[\phi,C]}
]

where

[
C
]

denotes causal structure.

The sum runs over:

* causal graphs,
* causal orders,
* topologies.

Matter and causality co-fluctuate.

---

# 14. Causal Gauge Symmetry

Ordinary gauge theory:

[
A_\mu
\rightarrow
A_\mu+\partial_\mu\Lambda
]

PM-QFT introduces:

[
C
\rightarrow
U_C C
]

where

[
U_C
]

acts on causal Hilbert space.

Physical observables become invariant under transformations of causal frame.

This is a quantum analog of diffeomorphism invariance.

---

# 15. Process Tensor Fields

Introduce causal field:

[
\chi(x)
]

whose expectation value determines local order:

[
\langle\chi(x)\rangle
=====================

+1
\Rightarrow
A\prec B
]

[
\langle\chi(x)\rangle
=====================

-1
\Rightarrow
B\prec A
]

[
\langle\chi(x)\rangle
=====================

0
]

indicates maximal indefiniteness.

Lagrangian:

[
\mathcal L_C
============

\frac12
(\partial\chi)^2
----------------

V(\chi)
]

causal order behaves as a quantum field.

---

# 16. Causal Indefiniteness and Gravity

Quantum gravity strongly suggests:

[
g_{\mu\nu}
]

must be quantized.

But causal structure derives from:

[
g_{\mu\nu}
]

through light cones.

Therefore:

if geometry is quantized,

causal order must also be quantized.

---

# 17. Quantum Switch Gravity (QSG)

Consider two metrics:

[
g_1
]

and

[
g_2
]

with opposite causal ordering.

Define:

[
|\Psi_g\rangle
==============

\frac{
|g_1\rangle
+
|g_2\rangle
}{\sqrt2}
]

Then:

[
(A\prec B)
+
(B\prec A)
]

emerges naturally.

The quantum switch becomes a superposition of geometries.

---

# 18. Superposed Topologies

Path integral:

[
Z
=

\sum_{\mathcal T}
\int
Dg
e^{iS[g,\mathcal T]}
]

where

[
\mathcal T
]

is topology.

Different topologies imply different causal connectivities.

Therefore:

topological superposition induces causal superposition.

---

# 19. Gravitational Process Matrix

Define:

[
W_g[g_1,g_2]
]

which assigns amplitudes to pairs of geometries.

Probability:

[
P
=

\int
Dg_1Dg_2
W_g[g_1,g_2]
]

This is the gravitational analog of process matrices.

---

# 20. Emergent Spacetime from Causal Condensation

We propose:

Spacetime is a condensate of microscopic causal qubits.

Elementary degrees:

[
|A\prec B\rangle,
\qquad
|B\prec A\rangle
]

Macroscopic geometry:

[
g_{\mu\nu}
==========

\langle
\hat G_{\mu\nu}(C)
\rangle
]

Metric emerges as an order parameter of causal quantum matter.

This provides a physical ontology for indefinite causal order.

---

# 21. Quantum Algorithms with ICO

Known advantages:

* communication complexity reduction,
* channel discrimination,
* query complexity improvements.

But no systematic algorithmic framework exists.

We propose:

## Causal Fourier Transform

[
|C\rangle
\rightarrow
\sum_k
e^{ikC}
|k\rangle
]

## Causal Interference Algorithms

Interference between computational histories of different causal orders.

## Causal Search

Search over orderings simultaneously.

---

# 22. Causal Circuit Model

Standard circuit:

[
U_n\cdots U_2U_1
]

Causal circuit:

[
\sum_C
\alpha_C
U_C
]

where

[
U_C
]

acts according to order (C).

Computations occur over superpositions of computational graphs.

---

# 23. Complexity Theory of Indefinite Causal Order

Define:

### BQP-C

Polynomial quantum computation with coherent causal superposition.

### BQP-ICO

Polynomial quantum computation with arbitrary process matrices.

### PostBQP-ICO

Indefinite causal computation with postselection.

Conjectured hierarchy:

[
{\rm BQP}
\subsetneq
{\rm BQP\text{-}C}
\subseteq
{\rm BQP\text{-}ICO}
\subseteq
{\rm PSPACE}
]

---

# 24. Causal Query Complexity

Standard oracle:

[
f(x)
]

ICO oracle:

[
f_{A\prec B}
+
f_{B\prec A}
]

Certain promise problems may require:

[
O(N)
]

queries classically,

[
O(\sqrt N)
]

quantumly,

but

[
O(\log N)
]

with causal superposition.

This suggests genuine computational advantage.

---

# 25. Causal Computational Supremacy Conjecture

**Conjecture**

There exists a family of promise problems:

[
L_{ICO}
]

such that

[
L_{ICO}
\in
{\rm BQP\text{-}ICO
}
]

but

[
L_{ICO}
\notin
{\rm BQP}
]

unless the polynomial hierarchy collapses.

If true, indefinite causal order constitutes a new computational primitive beyond ordinary quantum computation.

---

# 26. Experimental Program

Near-term tests:

1. Multi-switch photonic processors.
2. Superconducting causal qubits.
3. Trapped-ion process matrices.
4. Gravitationally induced causal superpositions.
5. Quantum-network causal routers.
6. Topological quantum switch simulators.
7. Process-matrix tomography.
8. Causal field analog simulators.

---

# 27. Central Principles of Quantum Causality

### Principle I

Causal order is a quantum degree of freedom.

### Principle II

Indefinite causal order is an independent resource beyond entanglement and coherence.

### Principle III

Quantum field theory must sum over causal structures.

### Principle IV

Quantum gravity is necessarily a theory of superposed causal relations.

### Principle V

Computational complexity changes when causal order becomes coherent.

---

# Final Unified Picture

The proposed ontology is:

```
Matter Fields
      ↓
Quantum States
      ↓
Quantum Causal States
      ↓
Process Matrix QFT
      ↓
Superposed Geometries
      ↓
Emergent Spacetime
```

In this framework:

* states are quantum,
* geometry is quantum,
* topology is quantum,
* and causality itself is quantum.

Indefinite causal order is therefore not a curiosity of quantum information theory but a candidate foundational principle:

> The universe may be a quantum superposition not only of what exists and where it exists, but also of which events cause which others.
