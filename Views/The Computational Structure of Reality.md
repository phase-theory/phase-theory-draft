The Computational Structure of Reality

Quantum Circuit Complexity, Physical Observables, and the Constraints on Dynamical Realizability

Abstract

The Computational Structure of Reality (CSR) investigates whether computational complexity provides quantitative constraints on the physical states, correlations, and dynamical configurations that can be prepared or realized by finite physical systems.

The central hypothesis is that the computational resources required to construct a quantum state may be related to independently defined physical properties of that state. These properties include multipartite entanglement, quantum Fisher information, correlation structure, distinguishability, and, in more speculative settings, effective geometric quantities.

The framework begins with a carefully specified quantum circuit complexity,
[
\mathcal C_{\epsilon}(\psi)

\min\left{
G(U):
\left|
|\psi\rangle-U|0\rangle
\right|
\leq\epsilon
\right},
]
where (G(U)) is the gate count relative to a specified gate set, architecture, and ancilla convention. The dependence on these choices is not incidental: complexity is not an intrinsic scalar until its operational definition has been fixed.

A central requirement of CSR is therefore the construction of relations that remain meaningful under physically reasonable changes of computational representation. A proposed physical law cannot depend arbitrarily on whether one chooses a particular universal gate set, a different encoding, or a different numerical precision.

The paper develops a resource-theoretic and operational formulation of computational structure. It distinguishes circuit complexity, state complexity, dynamical complexity, description length, and computational cost. It establishes an exact theorem for the (n)-qubit Greenberger–Horne–Zeilinger (GHZ) family: under a circuit model with product-state inputs, arbitrary two-qubit entangling gates, and unrestricted one-qubit gates, the minimum number of two-qubit gates required for exact preparation is (n-1). The same family possesses quantum Fisher information (F_Q=n^2) with respect to a specified collective generator. Consequently, the independently defined observable and the preparation complexity satisfy the exact relation
[
\boxed{
F_Q=(\mathcal C+1)^2.
}
]

The theorem provides a concrete quantitative connection between a well-defined computational resource and a physical observable. It does not establish a universal law relating complexity to geometry, gravity, or spacetime. Rather, it demonstrates the form such a result must take: a specified state family, a fixed operational model, an independently defined observable, and a proof of the relationship.

The paper then develops general bounds linking circuit complexity to entanglement generation, quantum Fisher information, correlation structure, and dynamical preparation. It identifies conditions under which complexity can become robust under changes of gate set and representation. Finally, it formulates a research program for determining whether computational constraints can generate effective geometric descriptions or restrict the dynamically realizable states of physical systems.

The principal conclusion is that computational complexity can provide rigorous constraints on physical state preparation and distinguishability. Whether it also determines or constrains effective geometry remains an open question requiring independent geometric definitions and quantitative theorems.

⸻

1. Introduction

1.1 The computational question

Modern physics increasingly employs computational structures to describe physical systems.

Quantum mechanics represents states in Hilbert spaces. Quantum field theory uses operator algebras and functional integrals. Statistical mechanics employs partition functions and state counting. Quantum information theory describes correlations through channels, entropies, and distinguishability measures.

These descriptions raise a fundamental question:

Are computational resources merely external tools used to describe physical reality, or do they impose intrinsic constraints on which physical configurations can be prepared, distinguished, and dynamically realized?

The distinction is substantial.

If computational complexity is merely a property of a chosen description, it may have no direct physical significance. If, however, it bounds the resources required by physically implementable processes, it becomes an operational property of the system.

The second possibility motivates the Computational Structure of Reality.

1.2 Central hypothesis

The central hypothesis is that physical realizability may be constrained by computational resources.

Let
[
\mathcal H
]
be a physical Hilbert space and let
[
|\psi\rangle\in\mathcal H
]
be a target state.

A circuit model specifies:

* an initial state;
* an allowed gate set;
* an interaction architecture;
* permitted ancillary systems;
* a norm or fidelity criterion;
* an accuracy threshold.

The complexity of preparing the target state is then an operational quantity.

For a specified circuit model (\mathfrak G), define
[
\boxed{
\mathcal C_{\epsilon}^{\mathfrak G}(\psi)

\min_{U\in\mathfrak U_{\mathfrak G}}
\left{
G(U):
\left|
|\psi\rangle-U|0\rangle
\right|
\leq\epsilon
\right}.
}
]

The superscript (\mathfrak G) emphasizes that complexity depends on the computational model.

The theory asks whether there exist physical observables (O(\psi)) for which
[
O(\psi)=f!\left(\mathcal C_{\epsilon}^{\mathfrak G}(\psi)\right)
]
or, more generally,
[
\mathcal B!\left(
O(\psi),\mathcal C_{\epsilon}^{\mathfrak G}(\psi)
\right)\leq 0.
]

The strongest results would establish inequalities or equalities whose physical meaning survives reasonable changes of computational convention.

1.3 What CSR does not assume

The framework does not assume:

1. that the universe is literally a digital computer;
2. that all physical laws are algorithms;
3. that every physical state has a short circuit description;
4. that computational complexity uniquely determines geometry;
5. that complexity is an absolute scalar independent of representation;
6. that quantum gravity is necessarily a computational process.

These are separate hypotheses requiring separate evidence.

CSR begins with operationally defined quantum systems and attempts to establish quantitative relationships before extending the framework to spacetime or cosmology.

1.4 Main objectives

The research program has six objectives:

1. Define physically meaningful computational complexity measures.
2. Determine how complexity constrains entanglement generation and state preparation.
3. Derive quantitative relationships between complexity and independently defined observables.
4. Establish robustness under gate-set changes, encodings, and accuracy conventions.
5. Investigate whether computational constraints induce effective geometric structures.
6. Identify falsifiable consequences in experimentally accessible quantum systems.

⸻

2. Mathematical Foundations

2.1 Quantum state space

Let a system consist of (n) distinguishable qubits:
[
\mathcal H_n=(\mathbb C^2)^{\otimes n}.
]

A pure state is represented by
[
|\psi\rangle\in\mathcal H_n,
\qquad
\langle\psi|\psi\rangle=1.
]

A mixed state is a density operator
[
\rho\geq0,
\qquad
\operatorname{Tr}\rho=1.
]

The distinction matters because pure-state circuit complexity and mixed-state preparation complexity need not coincide.

For a pure state, one may define complexity relative to a reference state. For a mixed state, one must additionally specify whether the preparation process includes purification, environmental degrees of freedom, measurements, or classical randomness.

2.2 Reference states

Choose a reference state
[
|\psi_0\rangle.
]

The standard computational reference is
[
|0\rangle^{\otimes n}.
]

The choice of reference state is part of the definition of complexity.

If two reference states are related by a circuit of bounded complexity, then their associated complexity measures differ by at most an additive amount determined by the connecting circuit.

If the reference states themselves require a number of gates growing with system size to interconvert, the resulting complexity measures can differ substantially.

2.3 Gate sets

A gate set is a collection
[
\mathfrak G={G_1,\ldots,G_m}
]
of allowed unitary operations.

A circuit is a finite composition
[
U=G_{i_k}\cdots G_{i_2}G_{i_1}.
]

Its gate count is
[
G(U)=k
]
when every elementary gate is assigned unit cost.

A more general weighted cost is
[
G_w(U)=\sum_{j=1}^{k}w(G_{i_j}),
]
where
[
w(G_i)>0.
]

Weighted costs are useful when different gates require different physical resources.

2.4 State complexity

For a target state (|\psi\rangle), define
[
\boxed{
\mathcal C_{\epsilon}^{\mathfrak G}(\psi)

\min_{U}
\left{
G(U):
\left|
|\psi\rangle-U|\psi_0\rangle
\right|_2
\leq\epsilon
\right}.
}
]

This is an absolute-vector-distance convention.

Because quantum states are physically unchanged by a global phase, a phase-insensitive alternative is
[
d_{\mathrm{ray}}(\psi,\phi)

\min_{\theta\in\mathbb R}
\left|
|\psi\rangle-e^{i\theta}|\phi\rangle
\right|_2.
]

Equivalently, for normalized pure states,
[
d_{\mathrm{ray}}(\psi,\phi)^2

2-2|\langle\psi|\phi\rangle|.
]

The two conventions should not be silently interchanged.

2.5 Circuit complexity versus physical preparation cost

Gate count is not identical to laboratory cost.

A circuit containing (k) gates may have:

* different total execution times;
* different energy consumption;
* different control precision requirements;
* different error accumulation;
* different communication requirements.

A physically grounded complexity measure may therefore be a resource vector:
[
\mathbf C(\psi)

\left(
C_{\mathrm{gate}},
C_{\mathrm{depth}},
C_{\mathrm{time}},
C_{\mathrm{energy}},
C_{\mathrm{communication}},
C_{\mathrm{precision}}
\right).
]

A scalar complexity is obtained only after specifying a cost functional:
[
C_{\mathrm{phys}}(\psi)

\mathcal F(\mathbf C(\psi)).
]

There is no general reason to assume that one scalar captures every physical preparation resource.

⸻

3. The Computational Architecture of a Physical System

3.1 Interaction graphs

A quantum circuit architecture may be represented by a graph
[
\mathcal G=(V,E),
]
where:

* vertices correspond to physical subsystems;
* edges specify permitted two-body interactions.

A two-qubit gate is allowed only between vertices connected by an edge.

The architecture may be all-to-all, one-dimensional, two-dimensional, or more general.

The architecture affects complexity.

A state that requires (O(n)) gates on an all-to-all architecture may require greater circuit depth or gate count under locality restrictions.

3.2 Circuit depth

Gate count does not determine parallel execution time.

The depth (D(U)) is the minimum number of sequential layers required to schedule the circuit such that gates acting in the same layer have disjoint supports.

For a circuit with (k) gates,
[
D(U)\leq k.
]

The depth can be much smaller than the gate count.

For physical realizability, depth may be more relevant than gate count when operations occur in parallel.

3.3 Locality

Let each elementary gate act on at most (r) subsystems.

Locality restricts the speed at which correlations can propagate.

In spatially local quantum systems, Lieb–Robinson bounds provide an approximate causal structure for the propagation of information.

A circuit model with local gates therefore has stronger physical content than one permitting arbitrary nonlocal gates at unit cost.

3.4 Ancillary systems

Ancillas may reduce the complexity of some tasks.

A preparation protocol may begin with
[
|\psi_0\rangle\otimes|0\rangle_A
]
and produce
[
|\psi\rangle\otimes|\chi\rangle_A.
]

One must specify whether:

* ancillas are free;
* their preparation is charged;
* they must be returned to a reference state;
* measurements and discarding are allowed.

Without this specification, two complexity values may describe different operational tasks.

3.5 The computational model as physical structure

The gate set and interaction graph can represent the control capabilities of an actual device.

In this case, complexity is not merely an abstract property of a state. It is a measure of the difficulty of producing the state with a specified physical architecture.

The theory must nevertheless distinguish device-relative complexity from any proposed architecture-independent physical quantity.

⸻

4. Complexity and Physical Equivalence

4.1 Complexity is not invariant under arbitrary encoding

Suppose a physical state is represented in two computational bases related by a unitary transformation (V).

Then
[
|\psi\rangle\mapsto V|\psi\rangle.
]

If (V) is computationally expensive, the circuit complexity can change substantially.

Thus a physical statement based on complexity must specify which transformations of representation are physically admissible.

4.2 Bounded-overhead equivalence

Let (\mathfrak G_1) and (\mathfrak G_2) be two computational models.

Suppose every gate in (\mathfrak G_1) can be simulated using at most (a) gates from (\mathfrak G_2), up to error (\delta), and conversely every gate in (\mathfrak G_2) can be simulated using at most (b) gates from (\mathfrak G_1).

Then, under compatible approximation conventions,
[
\mathcal C_{\epsilon+\delta k}^{\mathfrak G_2}(\psi)
\leq
a\mathcal C_\epsilon^{\mathfrak G_1}(\psi)
]
for a circuit of (k) gates, with a corresponding reverse inequality.

More carefully, if each simulated gate incurs error at most (\delta), a straightforward hybrid bound gives total error at most (k\delta).

The resulting comparison is meaningful only when the accuracy budget is handled explicitly.

4.3 Asymptotic complexity classes

For families of states
[
{|\psi_n\rangle}_{n=1}^{\infty},
]
one may study asymptotic growth:
[
\mathcal C(\psi_n)=O(n),
]
[
\mathcal C(\psi_n)=O(n^2),
]
[
\mathcal C(\psi_n)=O(2^n).
]

If two gate models simulate one another with polynomial or constant overhead, certain asymptotic classifications remain stable.

This suggests that asymptotic complexity classes may be more robust than exact gate counts.

However, a polynomial-overhead equivalence is not sufficient to preserve every quantitative physical relation. A proposed law such as
[
O(\psi)=C(\psi)^2
]
is sensitive to changes in normalization and overhead.

The strongest candidate physical relations should therefore use either operationally fixed costs or quantities invariant under a clearly specified equivalence class of implementations.

⸻

5. Entanglement as a Computational Resource

5.1 Product states and entangled states

A pure state is fully separable if it can be written
[
|\psi\rangle

|\psi_1\rangle\otimes\cdots\otimes|\psi_n\rangle.
]

A state that cannot be expressed in this form is entangled.

Entanglement can be characterized through bipartite partitions.

For a partition
[
A\cup B={1,\ldots,n},
]
the reduced state is
[
\rho_A=\operatorname{Tr}_B|\psi\rangle\langle\psi|.
]

The entanglement entropy is
[
S(A)

-\operatorname{Tr}(\rho_A\log\rho_A).
]

For a pure bipartite state,
[
S(A)=S(B).
]

5.2 Gate-induced entanglement

A one-qubit unitary cannot create entanglement between previously unentangled subsystems.

A two-qubit gate can create entanglement only between the two subsystems on which it acts.

This elementary observation leads to a graph-theoretic constraint on circuit complexity.

5.3 Interaction graph of a circuit

Given a circuit preparing an (n)-qubit state, construct a graph
[
\mathcal G_U=(V,E_U),
]
where (V={1,\ldots,n}), and an edge ((i,j)) is included if at least one two-qubit gate acts on qubits (i) and (j).

If the initial state is a product state and (\mathcal G_U) is disconnected, the final state factorizes across the connected components.

Therefore, a genuinely multipartite-entangled target state requires a connected interaction graph.

A connected graph on (n) vertices contains at least (n-1) edges.

Since each two-qubit gate can introduce at most one new edge,
[
\boxed{
G_2(U)\geq n-1
}
]
for any circuit that prepares a state entangled across every nontrivial bipartition.

Here (G_2(U)) is the number of two-qubit gates.

This lower bound does not require a particular universal gate set.

⸻

6. Main Exact Result: Complexity of the GHZ State

6.1 Definition

The (n)-qubit GHZ state is
[
\boxed{
|\mathrm{GHZ}_n\rangle

\frac{1}{\sqrt2}
\left(
|0\rangle^{\otimes n}
+
|1\rangle^{\otimes n}
\right).
}
]

It is entangled across every nontrivial bipartition.

For any nonempty proper subset (A), its reduced density matrix is
[
\rho_A

\frac12
\left(
|0\rangle_A\langle0|
+
|1\rangle_A\langle1|
\right).
]

Therefore
[
S(A)=\log2.
]

6.2 Circuit model

Consider the following model:

1. The initial state is (|0\rangle^{\otimes n}).
2. Arbitrary one-qubit unitaries are allowed at zero cost for the purpose of counting entangling gates.
3. Arbitrary two-qubit unitaries are allowed.
4. No ancillary qubits are permitted.
5. The target is prepared exactly.
6. Only the number of two-qubit gates is counted.

Let
[
\mathcal C_2(\psi)
]
denote the minimum number of two-qubit gates required to prepare (|\psi\rangle).

6.3 Lower bound

Because the GHZ state is entangled across every nontrivial bipartition, its circuit interaction graph must be connected.

A connected graph on (n) vertices requires at least
[
n-1
]
edges.

Each two-qubit gate can contribute at most one distinct edge.

Thus
[
\boxed{
\mathcal C_2(\mathrm{GHZ}_n)\geq n-1.
}
]

6.4 Upper bound

The GHZ state can be prepared using:

1. A Hadamard gate on the first qubit.
2. A sequence of (n-1) controlled-NOT gates, each connecting the first qubit to one additional qubit.

The circuit is
[
|\mathrm{GHZ}_n\rangle

\left(
\prod_{j=2}^{n}\mathrm{CNOT}_{1j}
\right)
H_1|0\rangle^{\otimes n}.
]

The preparation uses exactly (n-1) two-qubit gates.

Therefore
[
\mathcal C_2(\mathrm{GHZ}_n)\leq n-1.
]

6.5 Exact theorem

Theorem 6.1 — Exact Two-Qubit Gate Complexity of the GHZ Family

For the circuit model defined above,
[
\boxed{
\mathcal C_2(\mathrm{GHZ}_n)=n-1.
}
]

Proof.

The interaction-graph argument establishes the lower bound
[
\mathcal C_2(\mathrm{GHZ}_n)\geq n-1.
]

The Hadamard-plus-CNOT construction establishes the upper bound
[
\mathcal C_2(\mathrm{GHZ}_n)\leq n-1.
]

Combining the two inequalities gives
[
\mathcal C_2(\mathrm{GHZ}_n)=n-1.
]
(\square)

This theorem is exact for the specified model. It is not a claim about every possible gate architecture, ancilla convention, or weighted physical cost.

⸻

7. An Independent Physical Observable: Quantum Fisher Information

The previous theorem establishes the computational cost of preparing the GHZ family.

To construct a physical relationship, an independently defined observable is required.

Quantum Fisher information provides such an observable.

7.1 Parameterized quantum states

Consider a parameter-dependent state
[
|\psi_\theta\rangle

e^{-i\theta G}|\psi\rangle,
]
where (G) is a Hermitian generator.

The quantum Fisher information for a pure state is
[
\boxed{
F_Q(|\psi\rangle,G)

4\left(
\langle G^2\rangle_\psi

\langle G\rangle_\psi^2
\right)

4(\Delta G)^2.
}
]

It quantifies the sensitivity of the state to changes in (\theta).

The quantum Cramér–Rao inequality gives
[
\operatorname{Var}(\hat\theta)
\geq
\frac{1}{\nu F_Q},
]
for (\nu) independent repetitions under the usual regularity assumptions.

Quantum Fisher information is therefore connected to an operational measurement task.

7.2 Collective generator

Define
[
J_z=\frac12\sum_{j=1}^{n}\sigma_z^{(j)}.
]

For the GHZ state,
[
J_z|0\rangle^{\otimes n}

\frac n2|0\rangle^{\otimes n},
]
[
J_z|1\rangle^{\otimes n}

-\frac n2|1\rangle^{\otimes n}.
]

Consequently,
[
\langle J_z\rangle=0,
]
and
[
\langle J_z^2\rangle=\frac{n^2}{4}.
]

The variance is
[
(\Delta J_z)^2=\frac{n^2}{4}.
]

Thus
[
\boxed{
F_Q(\mathrm{GHZ}_n,J_z)=n^2.
}
]

7.3 Complexity-observable theorem

Combining the exact complexity theorem with the independent quantum Fisher information calculation gives the following result.

Theorem 7.1 — Exact Complexity–Metrological Sensitivity Relation

For the (n)-qubit GHZ family, under the circuit model of Theorem 6.1 and with collective generator
[
J_z=\frac12\sum_{j=1}^{n}\sigma_z^{(j)},
]
the minimum two-qubit gate complexity and quantum Fisher information satisfy
[
\boxed{
F_Q=(\mathcal C_2+1)^2.
}
]

Proof.

The exact circuit complexity is
[
\mathcal C_2=n-1.
]

The quantum Fisher information is
[
F_Q=n^2.
]

Therefore
[
F_Q=(n-1+1)^2
=(\mathcal C_2+1)^2.
]
(\square)

7.4 Physical interpretation

The theorem establishes a precise relation between two independently defined quantities:

* (\mathcal C_2): the minimum number of two-qubit gates required for exact preparation;
* (F_Q): the sensitivity of the prepared state to a collective phase generated by (J_z).

The relation is not a universal law for arbitrary states.

It is an exact identity for a specified state family and operational model.

Nevertheless, it demonstrates a central possibility of CSR: a physical observable may be quantitatively constrained by the computational resources required to realize the state.

7.5 Metrological implication

The quantum Cramér–Rao inequality becomes
[
\operatorname{Var}(\hat\theta)
\geq
\frac{1}{\nu(\mathcal C_2+1)^2}.
]

Thus, for this family, increasing the minimum preparation complexity increases the achievable collective phase sensitivity quadratically.

This statement assumes ideal state preparation, ideal measurements, and the specified collective generator. Noise and imperfect control can reduce the operational sensitivity.

⸻

8. General Complexity Bounds from Quantum Fisher Information

The GHZ result suggests a broader question: can quantum Fisher information be bounded in terms of preparation complexity for more general states?

A useful result can be obtained for circuits composed of bounded-support gates.

8.1 Bounded-support circuits

Let
[
|\psi\rangle=U|0\rangle^{\otimes n}
]
be prepared by a circuit with (K) gates.

Assume:

* every gate acts on at most (r) qubits;
* the initial state is a product state;
* the observable generator is
    [
    G=\frac12\sum_{j=1}^{n}\sigma_z^{(j)};
    ]
* each gate may be an arbitrary unitary on its support.

8.2 Backward propagation

The quantum Fisher information is
[
F_Q=4\operatorname{Var}_{0}(U^\dagger G U).
]

Write
[
G=\sum_j g_j,
\qquad
g_j=\frac12\sigma_z^{(j)}.
]

Under conjugation by a circuit, the support of an initially local operator can expand only through gates that intersect its existing support.

A gate acting on at most (r) qubits can enlarge an operator’s support by at most (r-1) new qubits.

For a circuit of (K) gates, the support of an initially one-qubit operator is therefore bounded by
[
s\leq1+(r-1)K.
]

For a Pauli operator with operator norm (1/2), the variance is bounded by (1/4).

A crude but useful upper bound follows from the fact that the evolved generator can be expressed as a sum of (n) terms, each supported on at most (s) qubits. The resulting bound is not generally sharp, but it establishes that a finite-depth local circuit cannot generate unrestricted global sensitivity without sufficient causal spread.

8.3 A rigorous general bound

A simpler rigorous bound follows directly from the range of (G).

For any state,
[
\operatorname{Var}(G)
\leq
\frac{(\lambda_{\max}-\lambda_{\min})^2}{4}.
]

For
[
G=J_z,
]
the spectral range is (n), so
[
F_Q=4\operatorname{Var}(J_z)\leq n^2.
]

This is the absolute metrological bound.

To relate it sharply to circuit complexity, one needs additional assumptions about locality, circuit depth, and the support growth of correlations.

8.4 Research implication

The GHZ identity is one member of a broader possible class:
[
F_Q\leq f(\mathcal C,n,\mathcal G).
]

The function (f) must depend on the generator and architecture.

A universal state-independent relation
[
F_Q=f(\mathcal C)
]
cannot hold without further restrictions, because different generators and state families can have very different sensitivities at the same circuit complexity.

⸻

9. Complexity and Multipartite Entanglement

9.1 Bipartite Schmidt rank

For a pure state across a bipartition (A|B), write the Schmidt decomposition:
[
|\psi\rangle

\sum_{j=1}^{\chi}
\sqrt{\lambda_j}
|a_j\rangle|b_j\rangle.
]

The Schmidt rank is
[
\chi=\operatorname{rank}\rho_A.
]

A two-qubit gate crossing the bipartition has operator Schmidt rank at most four.

Consequently, applying such a gate can increase the Schmidt rank by at most a factor of four.

If a circuit begins in a product state and uses (K_{A:B}) two-qubit gates crossing the cut, then
[
\boxed{
\chi_A
\leq4^{K_{A:B}}.
}
]

Therefore,
[
\boxed{
K_{A:B}
\geq
\frac12\log_2\chi_A.
}
]

This is a lower bound on the number of gates crossing the cut.

9.2 Entanglement entropy

Since
[
S(A)\leq\log_2\chi_A,
]
we obtain
[
S(A)\leq2K_{A:B}
]
when entropy is measured in bits.

Equivalently,
[
\boxed{
K_{A:B}\geq\frac12S(A).
}
]

This bound is not generally tight. It establishes that large bipartite entanglement requires a minimum number of gates crossing the partition.

9.3 Multiple cuts

A state may possess large entanglement across many distinct partitions.

Each partition imposes a separate lower bound:
[
K_{A:B}\geq\frac12S(A).
]

These bounds can constrain the architecture and depth of any preparation circuit.

Care is required when combining them because a single gate can cross multiple different partitions.

9.4 Connection to tensor networks

Tensor-network bond dimensions encode restrictions on entanglement.

For matrix product states,
[
|\psi\rangle

\sum_{{i_k}}
\operatorname{Tr}
(A_1^{i_1}\cdots A_n^{i_n})
|i_1\cdots i_n\rangle.
]

A bond dimension (\chi) bounds the Schmidt rank across the corresponding cut.

Tensor-network complexity and circuit complexity are related but not identical.

An efficient tensor-network representation does not necessarily imply a short circuit under every gate architecture, and a short circuit need not have a small representation in every tensor-network format.

9.5 Physical significance

Entanglement provides an independently defined physical property that can constrain preparation resources.

The result is strongest when the entanglement measure is operationally meaningful and the circuit architecture reflects physically permitted interactions.

⸻

10. Complexity and Distinguishability

10.1 State distinguishability

Two pure quantum states have trace distance
[
D(\psi,\phi)

\frac12
\left|
|\psi\rangle\langle\psi|

|\phi\rangle\langle\phi|
\right|_1.
]

For pure states,
[
D(\psi,\phi)

\sqrt{1-|\langle\psi|\phi\rangle|^2}.
]

This determines the optimal distinguishability of the states in a single-shot measurement.

10.2 Computationally restricted distinguishability

In practice, not every measurement is accessible.

Let (\mathfrak M_K) denote a set of measurements implementable with at most (K) gates.

Define
[
D_K(\rho,\sigma)

\sup_{M\in\mathfrak M_K}
D_{\mathrm{TV}}
\bigl(
P_M^\rho,P_M^\sigma
\bigr),
]
where (D_{\mathrm{TV}}) is the total variation distance between measurement outcome distributions.

Then
[
D_K(\rho,\sigma)
\leq
D(\rho,\sigma).
]

The restricted distinguishability is monotone in the computational budget:
[
K_1\leq K_2
\quad\Longrightarrow\quad
D_{K_1}(\rho,\sigma)
\leq
D_{K_2}(\rho,\sigma).
]

10.3 Operational meaning

Two states may be perfectly distinguishable in principle but difficult to distinguish using restricted measurements.

This introduces a distinction between:

* physical distinguishability;
* computationally accessible distinguishability.

The second depends on the measurement architecture.

10.4 Complexity-limited observers

A physical observer with finite control resources may be unable to access every distinction encoded in a quantum state.

This does not imply that inaccessible distinctions are unreal.

It means that operationally available information depends on the computational resources of the measurement process.

This is a useful framework for analyzing finite-resource observers without identifying their limitations with fundamental ontological limitations.

⸻

11. Complexity and Dynamical Realizability

11.1 Unitary evolution

Consider a system evolving under
[
i\frac{d}{dt}|\psi(t)\rangle

H(t)|\psi(t)\rangle.
]

The evolution operator satisfies
[
|\psi(t)\rangle=U(t)|\psi(0)\rangle.
]

A time-dependent Hamiltonian can generate a continuous family of states.

The circuit complexity of the final state is not necessarily equal to the number of elementary physical interactions that occurred.

Different Hamiltonians may generate the same state with different physical costs.

11.2 Time-dependent complexity

Define
[
\mathcal C_\epsilon(t)

\mathcal C_\epsilon(\psi(t)).
]

This quantity need not be monotonic.

A system can become more complex and later return to a low-complexity state.

For example, a unitary evolution followed by its inverse restores the original state:
[
U^\dagger U|\psi_0\rangle=|\psi_0\rangle.
]

The trajectory may pass through states of high complexity even though the final state has zero complexity relative to the reference.

11.3 Complexity growth

For a time-independent Hamiltonian,
[
U(t)=e^{-iHt}.
]

The complexity growth rate depends on the gate architecture and the cost assigned to approximating the continuous evolution.

A general upper bound can be obtained by decomposing the evolution into short-time steps:
[
e^{-iHt}

\left(e^{-iH\Delta t}\right)^N,
\qquad
N\Delta t=t.
]

The number of gates required depends on the locality and decomposition properties of (H).

11.4 Physical versus circuit complexity

Circuit complexity measures the shortest allowed implementation.

Physical evolution follows the actual Hamiltonian, which may not implement the shortest circuit.

Therefore,
[
\mathcal C_{\mathrm{actual\ evolution}}
\geq
\mathcal C_{\mathrm{minimum}}
]
when the actual evolution is expressible in the same gate model, but the difference may be substantial.

The minimum complexity is an optimization over possible implementations, not a record of the actual dynamical history.

⸻

12. Geometric Formulations of Complexity

A more ambitious version of CSR seeks to connect complexity with geometry.

This requires a geometric formulation of the space of states or unitary transformations.

12.1 Unitary group geometry

For an (n)-qubit system, unitary transformations belong to
[
U(2^n).
]

A circuit can be represented as a path through this group.

Let
[
U(s),\qquad s\in[0,1],
]
be a continuous path from the identity to a target unitary.

Define the instantaneous generator
[
H(s)=i\frac{dU}{ds}U^\dagger.
]

Then
[
\frac{dU}{ds}=-iH(s)U(s).
]

12.2 Cost geometry

Assign a cost function
[
F(H)
]
to each generator.

The length of a path is
[
L[U]

\int_0^1F(H(s)),ds.
]

The geometric complexity is the minimal path length:
[
\boxed{
\mathcal C_{\mathrm{geom}}(U)

\inf_{U(0)=I,\ U(1)=U}
L[U].
}
]

This construction is related to geometric approaches to quantum circuit complexity.

12.3 Penalty metrics

A common construction decomposes the generator into components:
[
H=\sum_I h_I T_I.
]

A quadratic cost may be defined by
[
F(H)^2

\sum_I p_I h_I^2,
]
where (p_I) penalizes certain directions.

For example, highly nonlocal generators may receive larger penalties.

The choice of penalties is part of the computational model.

12.4 State-space geometry

A state-space metric can be induced from a metric on the unitary group after quotienting by the subgroup that leaves the reference state unchanged.

The resulting geometry measures the distance between physical state rays under the chosen cost.

This produces a candidate geometric realization of computational complexity.

12.5 The central limitation

The metric is not automatically the physical spacetime metric.

It is a metric on a computational configuration space.

Identifying it with physical geometry would require an independent map:
[
\mathcal G_{\mathrm{comp}}
\longrightarrow
g_{\mu\nu}^{\mathrm{phys}}.
]

Such a map must preserve relevant structures and produce observable consequences.

Without that derivation, the connection remains a mathematical analogy.

⸻

13. Complexity and Effective Geometry

13.1 The geometric hypothesis

The speculative geometric hypothesis is that certain physical geometries may encode patterns of computational complexity.

One may seek a relation of the form
[
g_{\mu\nu}^{\mathrm{eff}}

\mathcal G_{\mu\nu}[\mathcal C,\mathcal I,\ldots],
]
where (\mathcal I) represents independent information-theoretic data.

The map must be derived rather than postulated.

13.2 Candidate geometric observables

Potential targets include:

* geodesic distances in state space;
* entanglement-wedge volumes in holographic models;
* correlation lengths;
* tensor-network bond dimensions;
* effective causal distances;
* curvature-like quantities constructed from information metrics.

Each candidate has a different physical interpretation.

13.3 Information geometry

For a family of quantum states
[
\rho(\lambda^1,\ldots,\lambda^m),
]
one can define a quantum information metric.

For pure states, the Fubini–Study metric is
[
ds^2

\langle d\psi|d\psi\rangle

|\langle\psi|d\psi\rangle|^2.
]

For mixed states, one may use the Bures metric or the quantum Fisher information metric.

These metrics quantify distinguishability between nearby states.

13.4 Complexity geometry versus information geometry

The information metric measures local distinguishability.

The complexity metric measures the cost of moving through a state or unitary space under a chosen gate cost.

They are not generally the same.

A system can have nearby states in the information metric that require a large circuit transformation under a restricted gate architecture.

Conversely, a low-cost circuit can generate a state that is highly distinguishable from the reference.

13.5 A possible relation

A future theory may establish bounds of the form
[
d_{\mathrm{info}}(\psi,\phi)
\leq
f\bigl(d_{\mathrm{comp}}(\psi,\phi)\bigr)
]
or
[
d_{\mathrm{comp}}(\psi,\phi)
\leq
g\bigl(d_{\mathrm{info}}(\psi,\phi),n,\mathfrak G\bigr).
]

The functions (f) and (g) would depend on the allowed gates and system size.

A universal equivalence between information distance and computational distance should not be assumed.

⸻

14. Tensor Networks and Emergent Spatial Structure

14.1 Tensor-network representation

A many-body quantum state may be represented by a tensor network.

For a matrix product state,
[
|\psi\rangle

\sum_{i_1,\ldots,i_n}
\operatorname{Tr}
\left(
A_1^{i_1}\cdots A_n^{i_n}
\right)
|i_1\cdots i_n\rangle.
]

For more general systems, one may use projected entangled-pair states, tree tensor networks, or multiscale entanglement renormalization ansätze.

14.2 Network geometry

The tensor network defines a graph.

Its vertices represent tensors, and its edges represent contracted indices.

The graph can be assigned an effective geometry using:

* graph distance;
* bond dimension;
* edge weights;
* entanglement entropy;
* correlation structure.

14.3 Computational interpretation

A low-complexity tensor network may provide an efficient representation of a state.

Its graph geometry can organize correlations and approximate physical locality.

However, the tensor-network graph is not automatically physical space.

A network may be reorganized through gauge transformations or alternative decompositions without changing the represented state.

14.4 A testable geometric proposal

A rigorous proposal would define a graph metric
[
d_{\mathrm{TN}}(i,j)
]
and compare it with an independently measured correlation distance
[
d_{\mathrm{corr}}(i,j).
]

For example, if connected correlations obey
[
|\langle O_iO_j\rangle_c|
\sim e^{-d_{\mathrm{corr}}(i,j)/\xi},
]
one can test whether
[
d_{\mathrm{corr}}(i,j)
\approx
\alpha d_{\mathrm{TN}}(i,j)+\beta
]
holds in a controlled family of states.

Such a relation would connect computational representation to an independent physical observable.

It would still not establish that the network geometry is fundamental spacetime.

⸻

15. Complexity, Holography, and Gravitational Geometry

15.1 Holographic motivation

In certain holographic theories, quantum states of a boundary theory are related to geometric configurations in a higher-dimensional gravitational description.

This motivates the study of whether boundary computational complexity has a geometric representation in the bulk.

15.2 Complexity-volume proposal

One proposed relation is
[
\mathcal C
\propto
\frac{V_{\mathrm{max}}}{G_N L},
]
where:

* (V_{\mathrm{max}}) is a maximal bulk spatial volume;
* (G_N) is Newton’s constant;
* (L) is a characteristic curvature scale.

15.3 Complexity-action proposal

Another proposal relates complexity to the gravitational action evaluated on a Wheeler–DeWitt region:
[
\mathcal C
\propto
\frac{I_{\mathrm{WDW}}}{\pi\hbar}.
]

These are conjectural prescriptions in particular holographic settings, not universal established identities.

15.4 CSR interpretation

The holographic proposals suggest that computational complexity may encode information about gravitational geometry.

However, they do not establish that complexity universally generates spacetime.

The relevant gravitational quantities are independently defined within a specific bulk theory.

The correspondence must be tested against:

* normalization ambiguities;
* ultraviolet divergences;
* boundary counterterms;
* state dependence;
* time dependence;
* choice of reference state;
* gate-set dependence.

15.5 Required theorem

A stronger CSR result would establish a relation such as
[
\mathcal C_{\mathrm{boundary}}

\mathcal F(g_{\mu\nu}^{\mathrm{bulk}})
]
for a specified holographic model, with a derivation that determines the normalization and removes arbitrary computational conventions.

The result would need to predict a gravitational observable not used to define the complexity prescription.

⸻

16. Computational Constraints and Physical Realizability

16.1 The realizability question

Let
[
\mathcal S_{\mathrm{phys}}
]
be a set of physically allowed states and let
[
\mathcal S_{\mathrm{comp}}(K)

\left{
|\psi\rangle:
\mathcal C_\epsilon(\psi)\leq K
\right}.
]

Then
[
\mathcal S_{\mathrm{comp}}(K)
]
is the set of states accessible within computational budget (K).

The physically realizable subset is
[
\mathcal S_{\mathrm{real}}(K)

\mathcal S_{\mathrm{phys}}
\cap
\mathcal S_{\mathrm{comp}}(K).
]

This is a precise operational construction.

16.2 Dynamical constraints

Suppose the physical Hamiltonian belongs to a permitted family
[
H(t)\in\mathfrak H.
]

The reachable set at time (T) is
[
\mathcal R(T)

\left{
U_H(T)|\psi_0\rangle:
H(t)\in\mathfrak H
\right}.
]

The computationally restricted reachable set is
[
\mathcal R_K(T)

\left{
|\psi\rangle\in\mathcal R(T):
\mathcal C_\epsilon(\psi)\leq K
\right}.
]

This separates two different restrictions:

1. dynamical reachability under the allowed Hamiltonians;
2. computational complexity under the specified circuit model.

A state can be dynamically reachable but computationally expensive to synthesize under a different gate model.

16.3 Finite-resource physical systems

A real device has finite:

* energy;
* time;
* control bandwidth;
* spatial connectivity;
* precision;
* memory;
* environmental isolation.

These limitations define a physically meaningful resource region.

The computational question becomes whether the resource region imposes nontrivial constraints on accessible states.

16.4 No immediate computational ontology

A finite device cannot prepare every mathematically definable state with finite resources.

That fact does not imply that the unprepared states are physically nonexistent.

The distinction between mathematical possibility and operational realizability must remain explicit.

⸻

17. Complexity and the Arrow of Time

17.1 Complexity is not automatically monotonic

For unitary evolution,
[
|\psi(t)\rangle=U(t)|\psi_0\rangle,
]
the state complexity can rise and fall.

A system may evolve toward a highly complex state and later return to its initial state under a reversed evolution.

Therefore,
[
\frac{d\mathcal C}{dt}\geq0
]
is not a general theorem.

17.2 Typical growth

In large chaotic systems, complexity may grow for extended periods before saturating at a large value.

This is a statistical or model-dependent expectation, not a universal property of quantum dynamics.

17.3 Entropy and complexity

Thermodynamic entropy and circuit complexity are different quantities.

A maximally mixed state may have high entropy but admit a simple statistical description.

A pure state may have zero von Neumann entropy but enormous circuit complexity relative to a reference state.

Thus,
[
S(\rho)\not\equiv\mathcal C(\rho).
]

17.4 Complexity as a possible temporal diagnostic

A complexity measure may nevertheless distinguish dynamical histories that are invisible to coarse thermodynamic variables.

A useful research question is whether a suitable coarse-grained complexity exhibits robust growth under specified chaotic dynamics.

The required result would need to distinguish:

* exact complexity;
* coarse-grained complexity;
* ensemble-averaged complexity;
* state complexity;
* operator complexity.

These quantities need not share the same monotonicity properties.

⸻

18. Approximate Complexity and Stability

18.1 Approximation threshold

Exact state preparation may be impossible with a finite gate set.

The physically relevant measure is therefore often
[
\mathcal C_\epsilon(\psi).
]

The threshold (\epsilon) determines the allowed state error.

18.2 Norm conventions

For pure states, define
[
d_2(\psi,\phi)

\min_\theta
\left|
|\psi\rangle-e^{i\theta}|\phi\rangle
\right|_2.
]

The trace distance is
[
D(\psi,\phi)

\frac12
\left|
|\psi\rangle\langle\psi|

|\phi\rangle\langle\phi|
\right|_1.
]

For pure states,
[
D(\psi,\phi)

\sqrt{1-|\langle\psi|\phi\rangle|^2}.
]

The two distances are related but not identical.

18.3 Stability of observables

If an observable (O) is bounded, then
[
|\langle O\rangle_\psi-\langle O\rangle_\phi|
\leq
2|O|D(\psi,\phi).
]

This inequality connects preparation accuracy to observable accuracy.

For the collective generator
[
J_z=\frac12\sum_j\sigma_z^{(j)},
]
the operator norm is
[
|J_z|=\frac n2.
]

The expectation value is therefore stable under small trace distance, but quantum Fisher information involves second moments and requires corresponding bounds on (J_z^2).

18.4 Why approximate complexity is difficult

A small state error does not necessarily imply a small change in exact circuit complexity.

A tiny perturbation can change whether an exact algebraic representation exists.

Conversely, a state may be approximated efficiently even if its exact preparation requires a large circuit.

Thus approximate complexity is often more operationally meaningful than exact complexity, but its stability must be analyzed separately.

⸻

19. Robustness Under Changes of Computational Convention

19.1 The convention problem

A central obstacle to CSR is that complexity depends on arbitrary-looking choices.

A proposed physical relationship must distinguish genuine resource dependence from representational artifacts.

19.2 Gate-set equivalence

Two universal gate sets are computationally equivalent in the sense that each can approximate gates from the other with finite overhead, subject to precision-dependent costs.

If the overhead is bounded uniformly per elementary gate, asymptotic gate complexity may be stable up to constant factors.

If the overhead grows with system size or accuracy, the comparison is weaker.

19.3 Accuracy dependence

A physically meaningful complexity law must state how complexity changes with (\epsilon).

For example, one may investigate
[
\mathcal C_\epsilon(\psi)
\sim
A(\psi)\log^p(1/\epsilon)
]
for a specified state family.

The exponent and coefficient may depend on the gate set and approximation theorem.

19.4 Reference-state dependence

If two reference states differ by a circuit of complexity (K_0), then
[
|\mathcal C_{\psi_0}(\psi)

\mathcal C_{\phi_0}(\psi)|
\leq K_0
]
under compatible exact circuit conventions.

This follows by composing a preparation circuit from one reference with the circuit connecting the references.

If (K_0) scales with system size, the reference choice can affect leading asymptotic behavior.

19.5 Physical convention invariance

A candidate fundamental complexity measure should be invariant, or transform in a controlled way, under changes that correspond to physically equivalent implementations.

This motivates defining complexity relative to an equivalence class of architectures rather than one arbitrary gate list.

A possible asymptotic definition is
[
\mathfrak C(\psi)

\inf_{\mathfrak G\in[\mathfrak G]{\mathrm{phys}}}
\limsup{n\to\infty}
\frac{\log(1+\mathcal C^{\mathfrak G}(\psi_n))}
{\log n}.
]

This construction is a research proposal, not a universally established physical observable. Its validity depends on a defensible definition of physically equivalent gate architectures.

⸻

20. A General Computational-Physical Correspondence

20.1 State families

Let
[
\mathcal F={|\psi_\lambda\rangle:\lambda\in\Lambda}
]
be a family of physical states.

Let
[
\mathcal C_\epsilon(\lambda)
]
be the preparation complexity.

Let
[
O(\lambda)
]
be an independently defined physical observable.

20.2 Correspondence relation

A computational-physical correspondence is a relation
[
\boxed{
\Phi\bigl(
\mathcal C_\epsilon(\lambda),
O(\lambda),
\lambda
\bigr)=0
}
]
or an inequality
[
\boxed{
\Phi\bigl(
\mathcal C_\epsilon(\lambda),
O(\lambda),
\lambda
\bigr)\leq0.
}
]

The relation is nontrivial if:

1. the complexity is defined independently of (O);
2. the observable is defined independently of complexity;
3. the relationship is proved from the model;
4. the result is not merely a reparameterization;
5. the relation has consequences for states not used to establish it.

20.3 Classification of results

There are four levels of strength.

Level I — Correlation

Numerical data suggest a relationship between complexity and an observable.

Level II — Model-specific bound

An inequality is derived for a specified family.

Level III — Exact theorem

A precise equality or sharp inequality is proved.

Level IV — Robust physical law

The relationship survives admissible changes of gate set, representation, precision, and physical implementation, with controlled transformation rules.

The GHZ result in this paper is a Level III theorem within its specified circuit model.

It is not a Level IV universal law.

⸻

21. New Research Directions

21.1 Complexity bounds on correlation length

For local many-body systems, one may investigate whether the correlation length satisfies a bound
[
\xi\leq f(D,r,\mathcal C),
]
where (D) is circuit depth and (r) is gate range.

This would connect circuit resources to spatial correlation structure.

The result must distinguish exact correlations from exponentially small tails allowed by Lieb–Robinson bounds.

21.2 Complexity and topological order

Topologically ordered states may require nontrivial circuits to prepare from product states under local operations.

A research target is a lower bound on preparation complexity in terms of topological entanglement or code distance.

The bound must be robust against local ancillary systems and allowed measurements.

21.3 Complexity and quantum error correction

For a quantum code with distance (d), one may ask whether encoding complexity is bounded below by a function of (d), locality, and code parameters.

A useful result would relate the resources required to prepare encoded states to independently defined error-correction performance.

21.4 Complexity and thermalization

A chaotic system may generate states whose circuit complexity grows rapidly.

One may investigate relations between complexity growth and independent dynamical diagnostics such as out-of-time-order correlators.

The relationship must not be assumed to be universal.

21.5 Complexity and phase transitions

Ground states across a quantum phase transition may exhibit changes in entanglement structure and preparation complexity.

A possible target is a scaling law
[
\mathcal C(L,\delta)
\sim
L^\alpha\mathcal F(L/\xi),
]
where (\delta) measures distance from criticality.

Such a law would need to be derived for a specified model and complexity definition.

21.6 Complexity and effective dimension

Tensor-network representations suggest that the structure of entanglement may define an effective dimension.

A possible program is to compare:

* graph dimension;
* spectral dimension;
* correlation dimension;
* computational complexity growth.

A genuine result would establish a quantitative relation among these independently defined quantities.

⸻

22. Experimental Program

22.1 GHZ-state preparation

The exact theorem can be tested using trapped ions, superconducting qubits, photonic systems, or other platforms capable of preparing multipartite entangled states.

For increasing (n), one can measure:

* two-qubit gate count;
* circuit depth;
* state fidelity;
* quantum Fisher information;
* sensitivity to collective phase shifts.

22.2 Metrological verification

The collective phase encoding is
[
U_\theta=e^{-i\theta J_z}.
]

For a GHZ state,
[
U_\theta|\mathrm{GHZ}_n\rangle

\frac1{\sqrt2}
\left(
e^{-in\theta/2}|0\rangle^{\otimes n}
+
e^{in\theta/2}|1\rangle^{\otimes n}
\right).
]

The relative phase changes by
[
n\theta.
]

The ideal quantum Fisher information is
[
F_Q=n^2.
]

Experimentally, the relevant comparison is between the observed Fisher information and the actual preparation resources.

22.3 Noise

For a noisy state
[
\rho_\theta,
]
the mixed-state quantum Fisher information must be used.

It can be defined through the symmetric logarithmic derivative (L_\theta):
[
\partial_\theta\rho_\theta

\frac12(L_\theta\rho_\theta+\rho_\theta L_\theta),
]
[
F_Q(\rho_\theta)

\operatorname{Tr}(\rho_\theta L_\theta^2).
]

Noise may destroy the ideal quadratic scaling.

22.4 Scaling analysis

The central experimental test is whether
[
F_Q\approx(\mathcal C_2+1)^2
]
holds for the ideal GHZ preparation family and how the relation degrades under realistic errors.

The exact theorem predicts the ideal relation. The experiment tests the physical implementation and noise model.

22.5 Beyond GHZ states

A more demanding experiment would compare families with different entanglement structures but similar preparation costs.

This would determine whether the GHZ relation is a special property of one state family or part of a broader complexity-observable law.

⸻

23. Falsifiability and Failure Conditions

CSR must be formulated so that proposed relationships can fail.

23.1 Complexity-definition failure

If a claimed law changes arbitrarily under equivalent gate sets or harmless re-encodings, it does not define a robust physical relationship.

23.2 Observable-dependence failure

If the observable is defined using the complexity measure itself, the proposed correspondence is circular.

23.3 Architecture failure

A result derived for all-to-all interactions may fail for local architectures.

The domain of validity must be stated.

23.4 Approximation failure

A relation valid only at exact preparation may be operationally irrelevant if no physical device can meet the required precision.

The behavior under nonzero (\epsilon) must be investigated.

23.5 Universality failure

A relation established for one state family cannot be promoted to a universal law without additional theorems.

The GHZ relation
[
F_Q=(\mathcal C_2+1)^2
]
does not establish this identity for arbitrary quantum states.

23.6 Geometric failure

If a proposed complexity geometry does not reproduce independently measured physical distances, causal relations, or curvature observables, its interpretation as physical geometry fails.

23.7 Dynamical failure

If complexity does not exhibit the predicted growth or resource dependence under the specified Hamiltonian, the proposed dynamical correspondence is falsified or requires revision.

⸻

24. Principal Obstacles

24.1 Representation dependence

The largest obstacle is the dependence of complexity on gate set, encoding, and reference state.

A physical theory cannot rest on an arbitrary computational convention.

24.2 Intractability

Computing circuit complexity is generally difficult.

Even when a circuit provides an upper bound, proving optimality may be computationally inaccessible.

24.3 Approximation

Physical states are rarely prepared exactly.

Approximate complexity can differ sharply from exact complexity.

24.4 Physical resource calibration

Gate count does not automatically correspond to time, energy, or thermodynamic cost.

A physically meaningful cost functional requires calibration against actual implementations.

24.5 Geometry identification

The existence of a metric on state space does not establish that it is spacetime geometry.

A separate derivation is required.

24.6 Universal applicability

Different systems may have fundamentally different computational architectures.

A single universal complexity measure may not exist.

24.7 Observable independence

The physical observable must be defined independently of complexity.

Otherwise, the theory risks becoming tautological.

⸻

25. The Research Program

The development of CSR should proceed through a sequence of increasingly demanding results.

Phase I — Operational foundations

Define:

* reference states;
* gate sets;
* interaction graphs;
* ancilla conventions;
* accuracy measures;
* weighted physical costs.

Phase II — Exact model theorems

Establish sharp complexity bounds for specific state families.

The GHZ result provides an initial benchmark.

Phase III — Observable correspondence

Derive relationships between complexity and independently defined quantities such as:

* quantum Fisher information;
* entanglement entropy;
* correlation length;
* code distance;
* dynamical response.

Phase IV — Robustness

Establish controlled behavior under:

* gate-set changes;
* encoding changes;
* reference-state changes;
* approximation thresholds;
* local architectural restrictions.

Phase V — Dynamical theory

Study complexity growth under specified Hamiltonians and derive bounds from locality, conservation laws, and control constraints.

Phase VI — Geometric reconstruction

Determine whether complexity and information metrics can jointly reconstruct effective geometric structures.

Phase VII — Physical validation

Compare the resulting predictions with quantum simulations, laboratory experiments, and, where appropriate, gravitational models.

⸻

26. Conclusions

The Computational Structure of Reality investigates whether computational resources impose quantitative constraints on the physical states and processes that can be realized.

Its starting point is the operational complexity
[
\mathcal C_{\epsilon}^{\mathfrak G}(\psi)

\min_U
\left{
G(U):
d(\psi,U\psi_0)\leq\epsilon
\right}.
]

This quantity is meaningful only relative to a specified computational architecture, reference state, and approximation convention.

The paper establishes an exact result for the GHZ family:
[
\boxed{
\mathcal C_2(\mathrm{GHZ}_n)=n-1.
}
]

It independently establishes
[
\boxed{
F_Q(\mathrm{GHZ}_n,J_z)=n^2.
}
]

Consequently,
[
\boxed{
F_Q=(\mathcal C_2+1)^2.
}
]

This is a precise quantitative relationship between a computational preparation resource and an operationally defined physical observable.

The result demonstrates that computational complexity can constrain physical properties without requiring a speculative identification of complexity with spacetime geometry.

The broader framework also establishes several important distinctions:

* state complexity is not thermodynamic entropy;
* minimum circuit complexity is not necessarily actual dynamical cost;
* information geometry is not computational geometry;
* computational geometry is not automatically spacetime geometry;
* mathematical state existence is not identical to finite-resource physical realizability.

The strongest future direction is to determine whether complexity bounds can be made robust under physically equivalent computational representations and whether those bounds constrain effective geometry or dynamical structure.

A successful theory must derive its observables independently, establish quantitative relations, and demonstrate that those relations survive changes in computational convention.

The governing research principle is therefore:

[
\boxed{
\text{Computational resources}
\longrightarrow
\text{State-preparation constraints}
\longrightarrow
\text{Observable bounds}
\longrightarrow
\text{Possible geometric structure}.
}
]

The first three stages admit rigorous mathematical development and experimentally accessible tests. The final stage remains an open research problem.

The Computational Structure of Reality is consequently best regarded as a developing physical-mathematical program: one that begins with operational quantum complexity, derives exact constraints where possible, and treats the emergence of geometry as a theorem to be established rather than a premise to be assumed.

⸻

References

1. Nielsen, M. A., and Chuang, I. L. Quantum Computation and Quantum Information. Cambridge University Press, 2000.
2. Kitaev, A. Y., Shen, A. H., and Vyalyi, M. N. Classical and Quantum Computation. American Mathematical Society, 2002.
3. Nielsen, M. A. “A Geometric Approach to Quantum Circuit Lower Bounds.” Quantum Information and Computation 6 (2006): 213–262.
4. Dowling, M. R., and Nielsen, M. A. “The Geometry of Quantum Computation.” Quantum Information and Computation 8 (2008): 861–899.
5. Hayden, P., and Preskill, J. “Black Holes as Mirrors: Quantum Information in Random Subsystems.” Journal of High Energy Physics 2007 (2007): 120.
6. Lloyd, S. “Ultimate Physical Limits to Computation.” Nature 406 (2000): 1047–1054.
7. Bennett, C. H. “Logical Reversibility of Computation.” IBM Journal of Research and Development 17 (1973): 525–532.
8. Bennett, C. H. “The Thermodynamics of Computation—A Review.” International Journal of Theoretical Physics 21 (1982): 905–940.
9. Vedral, V. “The Role of Relative Entropy in Quantum Information Theory.” Reviews of Modern Physics 74 (2002): 197–234.
10. Horodecki, R., Horodecki, P., Horodecki, M., and Horodecki, K. “Quantum Entanglement.” Reviews of Modern Physics 81 (2009): 865–942.
11. Braunstein, S. L., and van Loock, P. “Quantum Information with Continuous Variables.” Reviews of Modern Physics 77 (2005): 513–577.
12. Braunstein, S. L., and Caves, C. M. “Statistical Distance and the Geometry of Quantum States.” Physical Review Letters 72 (1994): 3439–3443.
13. Helstrom, C. W. Quantum Detection and Estimation Theory. Academic Press, 1976.
14. Holevo, A. S. Probabilistic and Statistical Aspects of Quantum Theory. North-Holland, 1982.
15. Tóth, G., and Apellaniz, I. “Quantum Metrology from a Quantum Information Science Perspective.” Journal of Physics A: Mathematical and Theoretical 47 (2014): 424006.
16. Pezzè, L., Smerzi, A., Oberthaler, M. K., Schmied, R., and Treutlein, P. “Quantum Metrology with Nonclassical States of Atomic Ensembles.” Reviews of Modern Physics 90 (2018): 035005.
17. Greenberger, D. M., Horne, M. A., and Zeilinger, A. “Going Beyond Bell’s Theorem.” In Bell’s Theorem, Quantum Theory, and Conceptions of the Universe. Kluwer, 1989.
18. Lieb, E. H., and Robinson, D. W. “The Finite Group Velocity of Quantum Spin Systems.” Communications in Mathematical Physics 28 (1972): 251–257.
19. Hastings, M. B. “An Area Law for One-Dimensional Quantum Systems.” Journal of Statistical Mechanics (2007): P08024.
20. Vidal, G. “Efficient Classical Simulation of Slightly Entangled Quantum Computations.” Physical Review Letters 91 (2003): 147902.
21. Verstraete, F., and Cirac, J. I. “Renormalization Algorithms for Quantum-Many Body Systems in Two and Higher Dimensions.” arXiv:cond-mat/0407066 (2004).
22. Swingle, B. “Entanglement Renormalization and Holography.” Physical Review D 86 (2012): 065007.
23. Susskind, L. “Computational Complexity and Black Hole Horizons.” Fortschritte der Physik 64 (2016): 24–43.
24. Brown, A. R., Roberts, D. A., Susskind, L., Swingle, B., and Zhao, Y. “Complexity, Action, and Black Holes.” Physical Review D 93 (2016): 086006.
25. Brown, A. R., Roberts, D. A., Susskind, L., Swingle, B., and Zhao, Y. “Holographic Complexity Equals Bulk Action?” Physical Review Letters 116 (2016): 191301.
26. Chapman, S., Heller, M. P., Marrochio, H., and Pastawski, F. “Toward a Definition of Complexity for Quantum Field Theory States.” Physical Review Letters 120 (2018): 121602.
27. Jefferson, R. A., and Myers, R. C. “Circuit Complexity in Quantum Field Theory.” Journal of High Energy Physics 2017 (2017): 107.
28. Osborne, T. J. “Efficient Approximation of the Dynamics of One-Dimensional Quantum Spin Systems.” Physical Review Letters 97 (2006): 157202.
29. Nielsen, M. A., Dowling, M. R., Gu, M., and Doherty, A. C. “Quantum Computation as Geometry.” Science 311 (2006): 1133–1135.
30. Eisert, J., Cramer, M., and Plenio, M. B. “Area Laws for the Entanglement Entropy.” Reviews of Modern Physics 82 (2010): 277–306.
