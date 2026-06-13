# Quantum Mechanics of Genuinely Infinite Systems

## Toward a Complete Operator-Algebraic Framework for Macroscopic Quantum Reality

### White Paper

---

# Abstract

Standard quantum mechanics is built upon the Hilbert-space formulation developed by von Neumann. For finite systems and systems with finitely many degrees of freedom, this framework is mathematically complete: all irreducible representations of the canonical commutation relations are unitarily equivalent by the Stone–von Neumann theorem.

However, every physically important many-body quantum system ultimately lies outside this regime.

The thermodynamic limit (N\to\infty), quantum fields with infinitely many modes, phase transitions, spontaneous symmetry breaking, topological order, black-hole horizons, thermal states, and cosmological quantum fields all inhabit a domain where the Stone–von Neumann theorem fails. There exist infinitely many physically inequivalent Hilbert-space realizations of the same observable algebra.

The traditional Hilbert-space picture therefore ceases to be fundamental.

Instead, the primary object becomes the algebra of observables itself, together with its states and representations. This leads naturally to the framework of C*-algebras, von Neumann algebras, modular theory, and algebraic quantum mechanics.

Despite more than half a century of development, this framework remains disconnected from mainstream quantum physics. Most practical calculations still employ finite-volume approximations whose conceptual foundations become ambiguous in the infinite limit.

This paper develops a unified formulation of Quantum Mechanics of Genuinely Infinite Systems (QGIS), intended as a complete physical theory of macroscopic quantum systems. We formulate:

1. Infinite-system quantum states as positive functionals on observable algebras.
2. Measurement theory directly in the thermodynamic limit.
3. Dynamics via modular automorphism groups.
4. Quantum chaos in operator-algebraic settings.
5. Entropy beyond von Neumann entropy.
6. A classification of macroscopic quantum phases through representation theory.
7. A generalized framework connecting QFT, condensed matter, gravity, and statistical mechanics.

The resulting theory suggests that the correct ontology of quantum physics is algebraic rather than Hilbert-space based.

---

# 1. Introduction

The conventional presentation of quantum mechanics begins with:

* Hilbert space ( \mathcal H )
* Observables as self-adjoint operators
* States as density matrices
* Unitary evolution

This works remarkably well for:

* atoms
* molecules
* finite spin systems
* quantum information processors

Yet essentially every macroscopic system violates the assumptions underlying this formulation.

Examples include:

* ferromagnets
* superconductors
* Bose condensates
* quantum fields
* thermal reservoirs
* black-hole exterior regions

The central reason is:

### Infinite systems possess inequivalent quantum realizations.

The same canonical algebra can generate infinitely many Hilbert spaces not related by unitary transformations.

Thus:

[
\text{Hilbert space}
\neq
\text{fundamental object}.
]

The observable algebra is fundamental.

---

# 2. Failure of Stone–von Neumann

Finite systems satisfy

[
[q_i,p_j]=i\hbar\delta_{ij}.
]

Stone–von Neumann implies uniqueness of irreducible representations.

For infinitely many degrees of freedom,

[
i=1,2,3,\ldots,\infty
]

uniqueness disappears.

Different vacua produce different Hilbert spaces:

[
\mathcal H_1,
\mathcal H_2,
\mathcal H_3,\ldots
]

with

[
\mathcal H_i
\not\simeq
\mathcal H_j.
]

Consequences:

* spontaneous symmetry breaking
* superselection sectors
* thermal states
* inequivalent vacua
* topological phases

become mathematically inevitable.

---

# 3. Observable Algebras as Fundamental Objects

The fundamental object is a C*-algebra

[
\mathfrak A.
]

Observables satisfy

[
A,B\in\mathfrak A.
]

with norm

[
|A^*A|=|A|^2.
]

Physical meaning:

[
\mathfrak A
===========

\text{all measurable observables}.
]

No Hilbert space is assumed.

---

# 4. States as Positive Linear Functionals

Instead of vectors,

[
|\psi\rangle,
]

a state becomes

[
\omega:\mathfrak A\rightarrow \mathbb C.
]

with

[
\omega(A^*A)\ge0,
]

and

[
\omega(I)=1.
]

Expectation values:

[
\langle A\rangle
================

\omega(A).
]

This remains meaningful even when no global Hilbert-space description exists.

---

# 5. GNS Reconstruction

Every state generates a Hilbert space.

Gelfand–Naimark–Segal construction:

[
(\mathcal H_\omega,\pi_\omega,\Omega_\omega).
]

such that

[
\omega(A)
=========

\langle
\Omega_\omega,
\pi_\omega(A)
\Omega_\omega
\rangle.
]

Thus:

State first → Hilbert space second.

This reverses standard QM.

---

# 6. Macroscopic Phases as Representations

Different phases correspond to inequivalent GNS representations.

Examples:

Ferromagnet

[
\omega_\uparrow
]

and

[
\omega_\downarrow
]

generate

[
\mathcal H_\uparrow
]

and

[
\mathcal H_\downarrow.
]

No unitary operator connects them.

Therefore phase transitions become transitions between representations.

---

# 7. Haag–Kastler Local Quantum Physics

For spacetime region

[
O,
]

assign algebra

[
\mathfrak A(O).
]

Properties:

### Isotony

[
O_1\subset O_2
\Rightarrow
\mathfrak A(O_1)\subset\mathfrak A(O_2).
]

### Locality

Spacelike separated regions commute.

### Covariance

Symmetry acts on algebra.

This formulation avoids field-operator singularities.

---

# 8. Measurement in Infinite Systems

## Problem

Textbook measurement theory assumes:

[
\mathcal H_S\otimes\mathcal H_A.
]

But apparatuses are macroscopic.

They should be represented by:

[
N\rightarrow\infty.
]

No rigorous measurement theory exists in this regime.

---

# 9. Infinite-System Measurement Principle

We propose:

Measurement corresponds to representation selection.

Microscopic system:

[
\omega_S.
]

Macroscopic apparatus:

[
\omega_A.
]

Interaction drives:

[
\omega_S\otimes\omega_A
\rightarrow
\omega_{A,i}.
]

where

[
\omega_{A,i}
]

lies in distinct sectors.

Observed outcomes become superselection-sector selection.

Collapse becomes:

[
\text{sector emergence}.
]

---

# 10. Superselection from Thermodynamic Amplification

Infinite systems create exact orthogonality:

[
\langle
\Omega_i,
\Omega_j
\rangle
=0.
]

for

[
i\neq j.
]

Thus pointer states become rigorously distinguishable.

This provides a mathematically exact measurement theory.

---

# 11. Modular Theory

For a von Neumann algebra

[
\mathcal M
]

and faithful state

[
\omega,
]

Tomita-Takesaki yields:

[
(\Delta,J).
]

Modular operator:

[
\Delta.
]

Modular conjugation:

[
J.
]

Generates automorphisms:

[
\sigma_t(A)
===========

\Delta^{it}
A
\Delta^{-it}.
]

---

# 12. Modular Time as Physical Time

Traditional dynamics:

[
U(t)=e^{-iHt}.
]

Infinite systems often lack global Hamiltonians.

We propose:

[
\text{Physical time}
====================

\text{modular flow}.
]

This extends the thermal-time hypothesis.

Time becomes state-dependent.

---

# 13. Thermal States

KMS condition:

[
\omega(A\sigma_{i\beta}(B))
===========================

\omega(BA).
]

generalizes Gibbs states.

Thermodynamics emerges naturally from algebraic structure.

No finite partition function required.

---

# 14. Type-III Algebras

Local QFT algebras are type III.

Type III algebras possess:

* no trace
* no density matrices
* no ordinary entropy

This is one of the deepest conceptual issues in modern physics.

---

# 15. Entropy Beyond von Neumann

Ordinary entropy:

[
S=-\operatorname{Tr}(\rho\log\rho)
]

fails.

We propose replacing entropy by relative modular entropy:

[
S(\omega|\phi).
]

defined through modular operators.

Advantages:

* exists for type III algebras
* local
* representation-independent

Potentially fundamental.

---

# 16. Algebraic Quantum Chaos

Current chaos diagnostics:

[
C(t)
====

-\langle [A(t),B]^2\rangle.
]

depend on Hilbert-space realizations.

Infinite systems require algebraic versions.

Define

[
\lambda_A
=========

\limsup_{t\to\infty}
\frac1t
\log
|
[A,\sigma_t(B)]
|.
]

This provides an operator-algebraic Lyapunov exponent.

---

# 17. Modular Chaos Conjecture

We conjecture:

Positive modular Lyapunov exponent

[
\lambda_A>0
]

characterizes quantum chaos independent of representation.

This remains an open problem.

---

# 18. Information Flow in Infinite Systems

Information is encoded not in vectors but in state spaces:

[
\mathcal S(\mathfrak A).
]

Dynamics acts on convex geometry.

This suggests a geometric theory of information beyond density matrices.

---

# 19. Black Holes

Horizon algebras are type III.

Entropy paradoxes arise because finite-dimensional intuition fails.

In QGIS:

Black-hole entropy becomes modular entropy.

Information loss becomes a question of representation change.

---

# 20. Quantum Fields

QFT becomes a special case:

[
\mathfrak A(O)
]

for every spacetime region.

Particles become representation-dependent excitations.

Fields become secondary constructs.

---

# 21. Condensed Matter

Topological phases:

* quantum Hall states
* spin liquids
* topological superconductors

naturally correspond to inequivalent representations and sector structures.

The algebraic formulation unifies symmetry breaking and topological order.

---

# 22. Proposed Axioms of QGIS

### Axiom I

Reality is described by a C*-algebra

[
\mathfrak A.
]

### Axiom II

Physical states are positive normalized functionals.

### Axiom III

Hilbert spaces arise via GNS reconstruction.

### Axiom IV

Macroscopic phases correspond to inequivalent representations.

### Axiom V

Measurements are representation-selection processes.

### Axiom VI

Dynamics is generated by automorphism groups.

### Axiom VII

Thermal dynamics is modular dynamics.

### Axiom VIII

Entropy is modular-relative entropy.

### Axiom IX

Physical observables are algebraic invariants.

---

# 23. Major Open Problems

## Problem A

Macroscopic Measurement Theorem

Prove emergence of exact Born probabilities from thermodynamic sector selection.

---

## Problem B

Modular Time Dynamics

Determine when modular flow reproduces ordinary time evolution.

---

## Problem C

Type-III Entropy

Construct unique entropy satisfying:

* locality
* monotonicity
* thermodynamic consistency

for all type-III algebras.

---

## Problem D

Algebraic Quantum Chaos

Develop:

* modular OTOCs
* algebraic Lyapunov spectra
* representation-independent chaos indicators

---

## Problem E

Classification of Infinite Quantum Phases

Create a complete classification of phases via:

* representations
* sectors
* modular invariants

analogous to classifying manifolds by topology.

---

# 24. Central Thesis

The standard Hilbert-space formulation of quantum mechanics is the finite-system approximation of a deeper theory.

For genuinely infinite systems:

[
\boxed{
\text{Algebra}
\rightarrow
\text{State}
\rightarrow
\text{Representation}
}
]

replaces

[
\boxed{
\text{Hilbert Space}
\rightarrow
\text{Operator}
\rightarrow
\text{State}
}
]

as the fundamental hierarchy.

Quantum Mechanics of Genuinely Infinite Systems (QGIS) provides a unified framework for:

* thermodynamic limits,
* quantum field theory,
* spontaneous symmetry breaking,
* topological phases,
* quantum measurement,
* black-hole horizons,
* quantum statistical mechanics,

and suggests that the true structure of quantum reality is not a single Hilbert space, but a landscape of representations generated by an underlying observable algebra. The remaining challenge is to transform modular theory, sector theory, and type-III operator algebras from specialized mathematical machinery into operational physics principles capable of describing macroscopic quantum phenomena directly.
