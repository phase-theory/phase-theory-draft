# Relativity 44.0 — Algorithmic / Substrate Relativity  
## Substrate as Gauge and Algorithmic Invariant Structure as Physical

**White paper / academic preprint**

---

## Abstract

Algorithmic / Substrate Relativity is the hypothesis that the computational substrate of physics is not fundamental. Continuous and discrete substrates, classical and quantum substrates, cellular-automaton substrates, tensor-network substrates, categorical process substrates, and analog computational substrates may be physically equivalent when they preserve the same algorithmic and observable invariants. If two computational models simulate one another efficiently,

\[
M
\leftrightarrow
M',
\]

then their substrate differences are gauge. The central principle is:

\[
\boxed{
\text{Substrate is gauge; algorithmic invariant structure is physical.}
}
\]

This framework extends the Church–Turing thesis from computability to physical law and elevates computational complexity to a physical category. Not everything that is encoded is efficiently accessible. Some physical truths may be present in a description but hidden behind computational horizons. Algorithmic / Substrate Relativity unifies digital physics, quantum simulation, tensor-network holography, lattice field theory, categorical quantum mechanics, black-hole scrambling, and complexity-horizon physics into a single principle. It implies that the question “Is reality continuous or discrete, classical or quantum, circuit-like or categorical?” is not absolute. It is a question of substrate frame. The invariant is the algorithmic structure preserved under efficient intertranslation.

---

## 1. Introduction

Physics has often been shaped by its computational metaphors.

Classical mechanics imagined the universe as a clockwork system. Statistical mechanics imagined it as a gas of microscopic states. Quantum field theory imagined it as fields evolving through path integrals. Quantum information theory imagines it as qubits, channels, and circuits. Holography imagines spacetime as an error-correcting code. Digital physics imagines reality as a cellular automaton or computation.

Algorithmic / Substrate Relativity asks a sharper question:

\[
\text{Is any computational substrate fundamental?}
\]

The answer proposed here is no.

A substrate is a way of representing physical process. It may be continuous or discrete, classical or quantum, local or categorical, circuit-based or tensor-network-based. But if two substrates preserve the same observable and algorithmic invariants, then their differences are not differences in physical reality.

They are differences in gauge.

This does not mean that all substrates are equally useful. Some substrates make certain structures transparent. Others hide them. Some allow efficient simulation. Others require exponential overhead.

Thus Algorithmic / Substrate Relativity introduces a crucial refinement:

\[
\boxed{
\text{Computational complexity is physical.}
}
\]

A truth may be encoded in a system but not efficiently accessible to an observer. Black-hole interiors, scrambled quantum information, and hard many-body ground states are examples.

Thus substrate relativity is not merely about computability. It is about computational accessibility under physical resource constraints.

---

## 2. What Is a Computational Substrate?

A computational substrate is a framework for representing physical states, dynamics, and observations.

Examples include:

1. continuous differential equations,
2. discrete cellular automata,
3. classical Turing machines,
4. reversible logic circuits,
5. quantum circuits,
6. quantum field-theoretic path integrals,
7. lattice gauge theories,
8. tensor networks,
9. categorical process theories,
10. graph-rewriting systems,
11. algebraic automata,
12. holographic codes.

A substrate is not merely hardware. It is an ontological and mathematical medium in which physical law is expressed.

For example:

- Newtonian mechanics uses continuous trajectories.
- Lattice QCD uses discrete spacetime lattices.
- Quantum computation uses qubits and unitary circuits.
- Tensor-network theory uses entangled graph contractions.
- Categorical quantum mechanics uses morphisms in monoidal categories.
- Cellular automata use local update rules on discrete grids.

Each substrate suggests a different ontology.

Algorithmic / Substrate Relativity says that none of these ontologies is automatically fundamental.

---

## 3. The Core Principle

The central principle is:

\[
\boxed{
\text{Substrate is gauge; algorithmic invariant structure is physical.}
}
\]

This means:

1. The choice of substrate is a choice of representation.
2. Substrate differences that do not affect invariant structure are gauge.
3. Physical reality is the equivalence class of substrates under efficient intertranslation.
4. Computational complexity determines what is operationally accessible.
5. Encoded but inefficiently accessible structure may be physically real but observationally hidden.

Thus the fundamental question is not:

\[
\text{What is the substrate?}
\]

The fundamental question is:

\[
\text{What structure is invariant under substrate transformations?}
\]

---

## 4. Computational Models and Simulations

Let a computational model be a tuple,

\[
M
=
\left(
\mathcal{S}_M,
\mathcal{D}_M,
\mathcal{O}_M,
\mathcal{C}_M
\right),
\]

where:

- \(\mathcal{S}_M\) is a state space,
- \(\mathcal{D}_M\) is a dynamics or transition rule,
- \(\mathcal{O}_M\) is an observable algebra or measurement structure,
- \(\mathcal{C}_M\) is a cost or resource structure.

A simulation of \(M\) by \(M'\) is a map,

\[
\Phi:
\mathcal{S}_M
\rightarrow
\mathcal{S}_{M'},
\]

such that dynamics approximately commute:

\[
\Phi\circ\mathcal{D}_M
\approx
\mathcal{D}_{M'}\circ\Phi.
\]

Observables must also be preserved:

\[
O_M
\approx
\Phi^*O_{M'}.
\]

The simulation has an overhead function,

\[
T_{M\to M'}(n),
\]

where \(n\) measures input size, time, energy, or other physical resources.

If the overhead is efficient, for example polynomial,

\[
T_{M\to M'}(n)
=
\mathrm{poly}(n),
\]

then the simulation is efficient.

If two models efficiently simulate each other,

\[
M
\leftrightarrow
M',
\]

then they are computationally equivalent as physical substrates.

---

## 5. Substrate Gauge Equivalence

Define substrate gauge equivalence as follows.

Two models \(M\) and \(M'\) are substrate-equivalent,

\[
M\sim M',
\]

if there exist efficient simulations both ways preserving observables and empirical predictions:

\[
M
\leftrightarrow
M',
\]

\[
P_M(E)
=
P_{M'}(E').
\]

The physical content is the equivalence class,

\[
[M].
\]

Thus:

\[
\boxed{
\text{Physical reality is a substrate-equivalence class.}
}
\]

This generalizes familiar gauge ideas.

In gauge theory,

\[
A_\mu
\sim
A_\mu+\partial_\mu\lambda.
\]

In substrate relativity,

\[
M
\sim
M'
\]

when substrate differences do not affect invariant predictions.

---

## 6. Computability Versus Complexity

The classical Church–Turing thesis says that any effectively computable function can be computed by a Turing machine.

This thesis is about computability.

It says that the class of computable functions is robust across reasonable computational substrates.

Algorithmic / Substrate Relativity extends this idea:

\[
\text{Physical law should be robust across reasonable computational substrates.}
\]

But computability is not enough.

Physical observers are finite and resource-bounded.

Therefore complexity matters.

A function may be computable but infeasible.

A truth may be encoded but inaccessible.

A state may exist but be impossible to prepare.

A reconstruction may be possible in principle but require exponential time.

Thus:

\[
\boxed{
\text{Physical reality is not only what is computable. It is what is computable under physical constraints.}
}
\]

---

## 7. The Physical Church–Turing Thesis

The physical Church–Turing thesis says that any physically realizable computation can be simulated by a universal Turing machine.

A stronger version, the extended physical Church–Turing thesis, says that any physically reasonable computation can be simulated efficiently by a probabilistic Turing machine.

Quantum computation challenges the extended version.

A quantum computer can solve certain problems, such as integer factorization, more efficiently than known classical algorithms.

Shor’s algorithm factors integers in polynomial time:

\[
O((\log N)^3).
\]

The best known classical algorithms are subexponential but not polynomial.

Thus quantum substrates may be efficiently more powerful than classical substrates for some tasks.

This does not refute substrate relativity. It refines it.

Substrate differences are gauge only when efficient intertranslation preserves the relevant physical tasks.

If one substrate can efficiently simulate another only with exponential overhead, then the substrate difference is operationally real for bounded observers.

Thus:

\[
\boxed{
\text{Substrate equivalence is resource-relative.}
}
\]

---

## 8. Complexity Classes as Physical Categories

Complexity classes are not merely mathematical abstractions. They classify what physical systems can efficiently compute or encode.

Important classes include:

\[
\mathrm{P},
\quad
\mathrm{NP},
\quad
\mathrm{BPP},
\quad
\mathrm{BQP},
\quad
\mathrm{QMA},
\quad
\mathrm{PSPACE},
\quad
\mathrm{EXP}.
\]

For physical systems, these classes correspond to tasks such as:

1. simulating dynamics,
2. preparing ground states,
3. estimating partition functions,
4. decoding scrambled information,
5. reconstructing interiors,
6. sampling quantum circuits,
7. solving constraint satisfaction problems,
8. evaluating path integrals.

For example, estimating the ground-state energy of a local Hamiltonian is QMA-hard.

Thus some physical questions are not merely difficult. They belong to hard complexity classes.

This makes complexity physical.

---

## 9. Algorithmic Invariants

If substrate is gauge, what is invariant?

Algorithmic invariants include:

1. computable observables,
2. complexity classes of physical tasks,
3. causal structure,
4. symmetry groups,
5. conservation laws,
6. entropy scaling,
7. entanglement structure,
8. topological order,
9. correlation functions,
10. scattering amplitudes,
11. decoding complexity,
12. universality class.

Two substrates may use different states and different update rules, but if they preserve these invariants, they represent the same physical structure.

Thus:

\[
\boxed{
\text{The invariant is not the machine. It is the algorithmic structure.}
}
\]

---

## 10. Continuous and Discrete Substrates

A major question is whether spacetime is continuous or discrete.

Algorithmic / Substrate Relativity says that this question is not absolute.

A continuous field theory may be approximated by a lattice theory with spacing \(a\).

The lattice action is

\[
S_a[\phi]
=
\sum_x
a^d
\mathcal{L}_a(\phi(x)).
\]

The continuum limit is

\[
a\to0.
\]

If the lattice theory flows to the same renormalization-group fixed point as the continuum theory, then the lattice and continuum descriptions are physically equivalent in the infrared.

Thus discreteness may be a regulator, not an ontology.

Conversely, a continuum theory may be an effective description of a discrete substrate.

The invariant is the universality class.

Thus:

\[
\boxed{
\text{Continuous and discrete substrates may be gauge-equivalent in the same universality class.}
}
\]

---

## 11. Cellular Automata and Digital Physics

Cellular automata are discrete dynamical systems defined on lattices.

A cellular automaton consists of:

1. a lattice,
2. a finite alphabet of cell states,
3. a local update rule.

The update rule is often written as

\[
s_i(t+1)
=
f(s_{i-r}(t),\ldots,s_{i+r}(t)).
\]

Some cellular automata are computationally universal.

Digital physics proposes that the universe itself may be a cellular automaton or discrete computation.

Algorithmic / Substrate Relativity neither fully endorses nor rejects this proposal.

It says:

\[
\text{If a cellular automaton efficiently reproduces the invariant structure of known physics, then its discreteness is not automatically false.}
\]

But it also imposes constraints.

A viable discrete substrate must reproduce:

1. Lorentz invariance or an acceptable deformation,
2. quantum mechanics,
3. gauge symmetry,
4. chiral fermions,
5. gravity,
6. observed locality,
7. thermodynamic behavior,
8. cosmological structure.

This is a severe constraint.

Thus digital physics remains speculative, but substrate relativity gives it a precise criterion: invariant algorithmic structure, not mere discreteness.

---

## 12. Reversible Computation and Physical Law

Fundamental microscopic physics appears largely reversible.

Classical irreversible computation can be made reversible.

A reversible gate satisfies a bijective map,

\[
(x,y)
\mapsto
(x,y\oplus f(x)).
\]

The Toffoli gate is universal for reversible classical computation.

Landauer’s principle states that erasing one bit of information dissipates at least

\[
E
\geq
k_{\text{B}}T\ln 2.
\]

Thus information processing has thermodynamic cost.

This connects substrate relativity to thermodynamics.

A substrate is not merely logical. It is physical.

Its operations consume energy, entropy, space, and time.

Thus:

\[
\boxed{
\text{Computation is a physical process, not an abstract abstraction.}
}
\]

---

## 13. Quantum Substrates

Quantum computation introduces a new substrate.

A qubit is a two-dimensional quantum system,

\[
\ket{\psi}
=
\alpha\ket{0}
+
\beta\ket{1}.
\]

An \(n\)-qubit state lives in a Hilbert space of dimension

\[
2^n.
\]

Quantum evolution is unitary:

\[
\ket{\psi(t)}
=
U(t)\ket{\psi(0)}.
\]

Measurement is described by operators \(M_i\) satisfying

\[
\sum_i M_i^\dagger M_i=I.
\]

The probability of outcome \(i\) is

\[
P(i)
=
\bra{\psi}M_i^\dagger M_i\ket{\psi}.
\]

Quantum substrates can efficiently simulate certain quantum systems that appear intractable classically.

Feynman’s insight was that quantum systems should be simulated by quantum systems.

Thus:

\[
\boxed{
\text{Quantum physics may require quantum substrates for efficient representation.}
}
\]

---

## 14. Quantum Universality and Fault Tolerance

Quantum circuits are universal if they can approximate any unitary transformation.

A universal gate set may include, for example,

\[
\{H,S,T,\mathrm{CNOT}\}.
\]

The Solovay–Kitaev theorem shows that finite universal gate sets can approximate arbitrary unitaries efficiently.

Fault-tolerant quantum computation shows that reliable quantum computation is possible below an error threshold.

This is important for substrate relativity.

It means that the details of the physical quantum substrate may be gauge if the same logical quantum computation can be protected and implemented efficiently.

Thus:

\[
\boxed{
\text{Fault tolerance makes logical quantum structure substrate-independent.}
}
\]

---

## 15. Tensor Networks as Substrates

Tensor networks provide another computational substrate.

A tensor network represents a quantum state as a graph of contracted tensors.

For example, a matrix product state is

\[
\ket{\psi}
=
\sum_{s_1,\ldots,s_n}
\mathrm{Tr}
\left(
A^{s_1}_1
A^{s_2}_2
\cdots
A^{s_n}_n
\right)
\ket{s_1\cdots s_n}.
\]

The bond dimension \(\chi\) controls entanglement.

For a bipartition,

\[
S
\leq
\log\chi.
\]

Thus tensor networks efficiently represent area-law states but generally not volume-law states.

Multiscale entanglement renormalization ansatz, or MERA, represents critical states and has a geometry resembling hyperbolic space.

In holography, tensor networks model how bulk geometry emerges from boundary entanglement.

Thus tensor networks are not merely numerical tools. They are candidate substrates for emergent spacetime.

But again, the tensor network is not necessarily fundamental.

The invariant is the entanglement and correlation structure it represents.

---

## 16. Categorical Substrates

Categorical quantum mechanics uses categories as substrates.

A physical process is a morphism,

\[
f:A\to B.
\]

Systems are objects.

Composition is sequential process:

\[
g\circ f.
\]

Tensor product is parallel process:

\[
f\otimes g.
\]

A symmetric monoidal category provides the abstract structure of quantum processes.

A theory is a functor,

\[
Z:
\mathbf{Proc}
\to
\mathbf{Hilb}.
\]

Different categorical presentations may be equivalent:

\[
\mathbf{C}
\simeq
\mathbf{D}.
\]

If two categorical substrates are equivalent and preserve empirical structure, their differences are gauge.

Thus:

\[
\boxed{
\text{Categorical equivalence is substrate gauge equivalence.}
}
\]

---

## 17. Holography as Substrate Relativity

Holography is a profound example of substrate relativity.

In AdS/CFT,

\[
Z_{\text{CFT}}[J]
=
Z_{\text{gravity}}
\left[
\phi\big|_{\partial}=J
\right].
\]

The boundary theory and the bulk theory use different substrates.

The boundary substrate is quantum field theoretic.

The bulk substrate is gravitational and geometric.

Yet they are dual.

Bulk particles, black holes, and geometry correspond to boundary operators, states, and entanglement patterns.

Thus the substrate difference is gauge.

The invariant is the shared observable structure.

---

## 18. Complexity and Holographic Interiors

Holography also shows that complexity is physical.

A black-hole interior may be encoded in the boundary state.

But reconstructing it may require enormous computational resources.

The Harlow–Hayden argument suggests that decoding certain interior information from Hawking radiation may require time exponential in the black-hole entropy:

\[
t_{\text{decode}}
\sim
e^{S_{\text{BH}}}.
\]

Thus the interior can be encoded but not efficiently accessible.

This is a complexity horizon.

The information is not absent. It is computationally hidden.

Thus:

\[
\boxed{
\text{Some physical structure is real but inaccessible to bounded observers.}
}
\]

This is one of the central insights of Algorithmic / Substrate Relativity.

---

## 19. Scrambling and Fast Scramblers

Black holes are fast scramblers.

Scrambling is the process by which local information becomes nonlocally encoded across many degrees of freedom.

The scrambling time for a black hole is approximately

\[
t_{\text{scr}}
\sim
\frac{\beta}{2\pi}
\log S,
\]

where \(S\) is the entropy.

After scrambling, information is not destroyed. It is hidden in complex correlations.

Thus the physical state contains the information, but simple observables cannot access it.

This makes computational complexity an objective feature of the physical situation.

---

## 20. Complexity Bounds as Physical Laws

Computation is constrained by physics.

The Margolus–Levitin bound states that a system with energy \(E\) above its ground state can perform at most

\[
\nu
\leq
\frac{2E}{\pi\hbar}
\]

elementary operations per second.

The Bekenstein bound states that a system of radius \(R\) and energy \(E\) can contain at most

\[
I
\leq
\frac{2\pi E R}{\hbar c\ln 2}
\]

bits of information.

Landauer’s principle states that erasing one bit costs at least

\[
E
\geq
k_{\text{B}}T\ln 2.
\]

These bounds show that information, energy, entropy, space, and time are inseparable.

Thus computational substrates are not abstract. They are physical.

---

## 21. Complexity as a Physical Horizon

Define a resource budget \(R\) for an observer.

Let \(C_{\text{decode}}(I)\) be the complexity of decoding information \(I\).

The accessible information set is

\[
\mathcal{A}_R
=
\{
I
\mid
C_{\text{decode}}(I)
\leq
R
\}.
\]

The complexity horizon is the boundary,

\[
\mathcal{H}_R
=
\partial\mathcal{A}_R.
\]

Information beyond the horizon satisfies

\[
C_{\text{decode}}(I)
>
R.
\]

It is encoded but inaccessible.

Thus:

\[
\boxed{
\text{A complexity horizon separates encoded reality from accessible reality.}
}
\]

This generalizes causal horizons.

A causal horizon says:

\[
\text{You cannot reach it.}
\]

A complexity horizon says:

\[
\text{You cannot compute it.}
\]

Both are physical limits.

---

## 22. Algorithmic Invariance and Universality

Universality is central to substrate relativity.

A computational system is universal if it can simulate a wide class of systems.

Turing universality concerns classical computation.

Quantum universality concerns approximation of unitary transformations.

Topological quantum computation uses anyonic braiding to implement universal gates.

In each case, the details of the substrate may vary, but the universal computational class is invariant.

Thus:

\[
\boxed{
\text{Universality classes are algorithmic invariants.}
}
\]

This is analogous to universality in statistical mechanics.

Different microscopic systems can share the same critical behavior.

Different computational substrates can share the same algorithmic structure.

---

## 23. Substrate Relativity and Renormalization

Renormalization-group theory supports substrate relativity.

A lattice model and a continuum field theory may flow to the same fixed point.

The microscopic substrate is irrelevant in the technical sense.

The long-distance physics depends only on relevant operators and symmetries.

Thus the substrate is gauge at low energies.

The invariant is the universality class.

This is one of the deepest confirmations of substrate relativity in physics.

---

## 24. Substrate Relativity and Quantum Field Theory

Quantum field theory can be formulated in multiple substrates:

1. canonical operator formalism,
2. path integrals,
3. lattice regularizations,
4. algebraic quantum field theory,
5. perturbative Feynman diagrams,
6. bootstrap equations,
7. holographic duals,
8. tensor networks.

These formulations are not identical in every respect.

But they often preserve the same observable algebra and correlation functions.

Thus they are substrate-relative presentations.

The invariant is the physical content of the theory: correlators, symmetries, anomalies, and operator algebra.

---

## 25. Substrate Relativity and Quantum Gravity

Quantum gravity may require substrate relativity.

Candidate quantum-gravity substrates include:

1. strings,
2. branes,
3. spin networks,
4. spin foams,
5. causal sets,
6. group field theory,
7. tensor models,
8. causal dynamical triangulations,
9. holographic codes,
10. quantum circuits,
11. categorical structures.

No single substrate has been established as fundamental.

Algorithmic / Substrate Relativity suggests that this may be no accident.

The fundamental structure may be substrate-independent.

The substrates may be different efficient presentations of the same invariant process-structure.

Thus:

\[
\boxed{
\text{Quantum gravity may be an algorithmic invariant, not a particular computational medium.}
}
\]

---

## 26. Encoded but Inaccessible Truths

A key consequence of Algorithmic / Substrate Relativity is that truth and accessibility diverge.

A physical system may encode information that cannot be efficiently decoded.

Examples include:

1. scrambled black-hole information,
2. interior operators behind complexity horizons,
3. ground states of QMA-hard Hamiltonians,
4. partition functions of frustrated spin systems,
5. generic quantum circuit outputs,
6. high-energy scattering in chaotic systems,
7. fine-grained cosmological histories.

This does not mean the information is unreal.

It means that reality is stratified by computational accessibility.

Thus:

\[
\boxed{
\text{Physical reality includes encoded structure that bounded observers may not access.}
}
\]

---

## 27. Substrate Relativity and Digital Ontology

Digital ontology says that reality is fundamentally discrete computation.

Algorithmic / Substrate Relativity gives a more cautious formulation.

It says:

\[
\text{If reality can be represented by a discrete computational substrate without loss of invariant structure, then discreteness is possible.}
\]

But it also says:

\[
\text{If a continuous substrate preserves the same invariants more efficiently, then continuity may be equally valid.}
\]

The question is not:

\[
\text{Is reality digital?}
\]

The question is:

\[
\text{What invariant structure must any substrate preserve?}
\]

This avoids premature ontological commitment.

---

## 28. Substrate Relativity and Artificial Models

Artificial computational models can illuminate physical law.

Cellular automata, neural networks, quantum circuits, and tensor networks can model physical phenomena.

But one must distinguish:

1. a model that simulates physics,
2. a substrate that is physically equivalent,
3. a metaphor that is merely illustrative.

Algorithmic / Substrate Relativity provides the criterion:

\[
\boxed{
\text{A model is physically equivalent if it preserves invariant algorithmic and observable structure under efficient translation.}
}
\]

---

## 29. Formal Framework

Let \(\mathcal{M}\) be the class of computational models.

Let \(\sim\) be efficient substrate equivalence.

Then physical reality is the quotient,

\[
\mathcal{R}_{\text{alg}}
=
\mathcal{M}/\sim.
\]

A physical invariant is a function,

\[
I:
\mathcal{M}
\to
\mathcal{V},
\]

such that

\[
M\sim M'
\quad
\Rightarrow
\quad
I(M)=I(M').
\]

Candidate invariants include:

\[
I(M)
=
\{
\text{observable algebra},
\text{complexity classes},
\text{symmetries},
\text{entropy scaling},
\text{causal structure}
\}.
\]

Thus:

\[
\boxed{
\text{Reality is the invariant content of substrate-equivalence classes.}
}
\]

---

## 30. Axioms of Algorithmic / Substrate Relativity

The framework may be organized around twelve axioms.

### Axiom 1: Substrates Are Representations

Continuous, discrete, classical, quantum, categorical, and tensor-network substrates are representations.

### Axiom 2: Efficient Intertranslation Is Gauge

If two substrates efficiently simulate each other while preserving observables, their differences are gauge.

### Axiom 3: Invariants Are Physical

Physical reality is the invariant algorithmic structure.

### Axiom 4: Complexity Is Physical

Computational complexity is a physical category.

### Axiom 5: Accessibility Is Resource-Relative

What is accessible depends on energy, time, memory, and entropy.

### Axiom 6: Encoded Structure Can Be Real

Information may be physically real but computationally inaccessible.

### Axiom 7: Universality Defines Equivalence

Universality classes are substrate invariants.

### Axiom 8: Substrate Choice Is Pragmatic

Some substrates make structure transparent; others hide it.

### Axiom 9: Physical Bounds Constrain Computation

Energy, entropy, and causal structure bound computation.

### Axiom 10: Quantum Substrates Are Not Optional

Quantum physics may require quantum substrates for efficient representation.

### Axiom 11: Holography Is Substrate Relativity

Bulk-boundary duality is a substrate equivalence.

### Axiom 12: Reflexivity Is Required

The framework applies to its own computational description.

---

## 31. Relation to Previous Relativities

Algorithmic / Substrate Relativity integrates earlier relativities.

| Relativity | Contribution |
|---|---|
| General Relativity | Geometry is frame-relative |
| Quantum Reference Frames | Observers are physical systems |
| Complexity-Horizon Relativity | Computational inaccessibility is physical |
| Substance Relativity | Entities are frame-relative |
| Scale Relativity | Laws are scale-relative |
| Meta-Relativity | Descriptions are quotiented by equivalence |
| Algorithmic / Substrate Relativity | Computational substrates are gauge |

The progression is:

\[
\text{relative motion}
\rightarrow
\text{relative geometry}
\rightarrow
\text{relative frames}
\rightarrow
\text{relative substances}
\rightarrow
\text{relative substrates}.
\]

---

## 32. Scientific Status

Algorithmic / Substrate Relativity is not a single empirical theory.

It is a meta-framework.

It is supported by:

1. universality in statistical mechanics,
2. lattice field theory,
3. quantum computation,
4. fault tolerance,
5. holographic duality,
6. tensor-network methods,
7. black-hole information theory,
8. categorical quantum mechanics,
9. reversible computation,
10. physical complexity bounds.

It becomes scientifically powerful when applied to specific models with specific equivalence criteria.

It becomes vacuous if every substrate is declared equivalent without demonstrating efficient preservation of invariants.

Thus the framework must be disciplined by explicit simulation overheads and invariant structures.

---

## 33. Open Problems

Several major problems remain.

### 33.1 Physical Church–Turing Thesis

What computations are physically realizable?

### 33.2 Quantum Gravity Substrate

Is there a preferred substrate for quantum gravity, or only substrate equivalence?

### 33.3 Continuum Versus Discrete

Can discrete substrates reproduce Lorentz invariance and quantum field theory efficiently?

### 33.4 Complexity of Field Theory

What is the computational complexity of realistic quantum field theories?

### 33.5 Black-Hole Decoding

Can complexity horizons be made precise in full quantum gravity?

### 33.6 Tensor-Network Emergence

Can tensor networks produce full dynamical spacetime?

### 33.7 Categorical Foundations

Can categorical substrates fully replace set-theoretic or Hilbert-space formulations?

### 33.8 Resource Frames

How should physical resource frames be formally defined?

---

## 34. What Einstein Would Think

Einstein would be intrigued by Algorithmic / Substrate Relativity.

He sought invariant structure beneath coordinate representations.

Substrate relativity generalizes this: invariant structure beneath computational representations.

He might be skeptical of digital ontology and quantum information as fundamental.

But he would respect the principle:

\[
\boxed{
\text{The arbitrary features of representation should not be mistaken for physical reality.}
}
\]

If substrate is arbitrary, then substrate is gauge.

This is a natural extension of general covariance into computation.

---

## 35. Summary of Core Equations

### Computational model

\[
M
=
\left(
\mathcal{S}_M,
\mathcal{D}_M,
\mathcal{O}_M,
\mathcal{C}_M
\right).
\]

### Simulation commutation

\[
\Phi\circ\mathcal{D}_M
\approx
\mathcal{D}_{M'}\circ\Phi.
\]

### Efficient equivalence

\[
M
\leftrightarrow
M'
\quad
\text{with polynomial overhead}.
\]

### Substrate quotient

\[
\mathcal{R}_{\text{alg}}
=
\mathcal{M}/\sim.
\]

### Margolus–Levitin bound

\[
\nu
\leq
\frac{2E}{\pi\hbar}.
\]

### Bekenstein bound

\[
I
\leq
\frac{2\pi E R}{\hbar c\ln 2}.
\]

### Landauer bound

\[
E
\geq
k_{\text{B}}T\ln 2.
\]

### Complexity horizon

\[
\mathcal{A}_R
=
\{
I
\mid
C_{\text{decode}}(I)
\leq
R
\}.
\]

### Central principle

\[
\boxed{
\text{Substrate is gauge; algorithmic invariant structure is physical.}
}
\]

---

## 36. Conclusion

Relativity 44.0, Algorithmic / Substrate Relativity, asserts that the computational substrate of physics is not fundamental.

Continuous and discrete, classical and quantum, cellular and categorical, circuit and tensor-network substrates may be different presentations of the same physical structure.

If two substrates efficiently simulate each other while preserving observable and algorithmic invariants, their differences are gauge.

The central principle is:

\[
\boxed{
\text{Substrate is gauge; algorithmic invariant structure is physical.}
}
\]

But complexity is physical.

Some truths are encoded but not efficiently accessible. Some structures are real but hidden behind computational horizons. Some substrates are efficient for certain physics and inefficient for others.

Thus the fundamental question is not what substrate reality is made of.

The fundamental question is:

\[
\text{What invariant algorithmic structure survives all efficient substrate transformations?}
\]

This is Algorithmic / Substrate Relativity.

---

## Appendix A: Efficient Simulation

Let \(M\) and \(M'\) be computational models.

A simulation \(\Phi:M\to M'\) has overhead

\[
T_{M\to M'}(n).
\]

The simulation is efficient if

\[
T_{M\to M'}(n)
=
O(\mathrm{poly}(n)).
\]

If efficient simulations exist both ways,

\[
M
\leftrightarrow
M',
\]

then \(M\) and \(M'\) are substrate-equivalent.

---

## Appendix B: Complexity Horizon

Let \(R\) be an observer’s computational budget.

Let \(C_{\text{decode}}(I)\) be the complexity of decoding information \(I\).

The accessible set is

\[
\mathcal{A}_R
=
\{
I
\mid
C_{\text{decode}}(I)
\leq
R
\}.
\]

The complexity horizon is

\[
\mathcal{H}_R
=
\partial\mathcal{A}_R.
\]

Information beyond \(\mathcal{H}_R\) is encoded but inaccessible.

---

## Appendix C: Physical Complexity Bounds

The Margolus–Levitin bound is

\[
\nu
\leq
\frac{2E}{\pi\hbar}.
\]

The Bekenstein bound is

\[
I
\leq
\frac{2\pi E R}{\hbar c\ln 2}.
\]

Landauer’s principle is

\[
E_{\text{erase}}
\geq
k_{\text{B}}T\ln 2.
\]

These bounds show that computation is constrained by energy, entropy, space, and time.

---

## Appendix D: Tensor-Network Entanglement Bound

For a tensor network with bond dimension \(\chi\), the entanglement entropy across a cut satisfies

\[
S
\leq
\log\chi.
\]

Thus tensor networks efficiently represent low-entanglement states.

Generic volume-law states require exponential bond dimension.

Thus substrate efficiency depends on entanglement structure.

---

## Appendix E: Categorical Substrate Equivalence

Let \(\mathbf{C}\) and \(\mathbf{D}\) be categorical substrates.

An equivalence of categories consists of functors,

\[
F:\mathbf{C}\to\mathbf{D},
\]

\[
G:\mathbf{D}\to\mathbf{C},
\]

with natural isomorphisms,

\[
GF
\cong
\mathrm{id}_{\mathbf{C}},
\]

\[
FG
\cong
\mathrm{id}_{\mathbf{D}}.
\]

If physical theories are functors into \(\mathbf{Hilb}\) or another semantic category, then equivalent categorical substrates represent the same physical process structure.

---

## Selected References

1. A. M. Turing, “On Computable Numbers, with an Application to the Entscheidungsproblem,” *Proceedings of the London Mathematical Society* **2-42**, 230 (1936).  
2. A. Church, “An Unsolvable Problem of Elementary Number Theory,” *American Journal of Mathematics* **58**, 345 (1936).  
3. D. Deutsch, “Quantum Theory, the Church–Turing Principle and the Universal Quantum Computer,” *Proceedings of the Royal Society A* **400**, 97 (1985).  
4. R. P. Feynman, “Simulating Physics with Computers,” *International Journal of Theoretical Physics* **21**, 467 (1982).  
5. S. Lloyd, “Universal Quantum Simulators,” *Science* **273**, 1073 (1996).  
6. E. Bernstein and U. Vazirani, “Quantum Complexity Theory,” *SIAM Journal on Computing* **26**, 1411 (1997).  
7. P. W. Shor, “Algorithms for Quantum Computation: Discrete Logarithms and Factoring,” *Proceedings of the 35th Annual Symposium on Foundations of Computer Science* (1994).  
8. L. K. Grover, “A Fast Quantum Mechanical Algorithm for Database Search,” *Proceedings of the 28th Annual ACM Symposium on Theory of Computing* (1996).  
9. M. A. Nielsen and I. L. Chuang, *Quantum Computation and Quantum Information* (Cambridge University Press, 2000).  
10. J. Preskill, “Quantum Computing in the NISQ Era and Beyond,” *Quantum* **2**, 79 (2018).  
11. S. Aaronson, *Quantum Computing Since Democritus* (Cambridge University Press, 2013).  
12. R. Landauer, “Irreversibility and Heat Generation in the Computing Process,” *IBM Journal of Research and Development* **5**, 183 (1961).  
13. N. Margolus and L. B. Levitin, “The Maximum Speed of Dynamical Evolution,” *Physica D* **120**, 188 (1998).  
14. J. D. Bekenstein, “Universal Upper Bound on the Entropy-to-Energy Ratio for Bounded Systems,” *Physical Review D* **23**, 287 (1981).  
15. H. J. Bremermann, “Optimization through Evolution and Recombination,” in *Self-Organizing Systems* (1962).  
16. K. G. Wilson, “Confinement of Quarks,” *Physical Review D* **10**, 2445 (1974).  
17. J. B. Kogut and L. Susskind, “Hamiltonian Formulation of Wilson’s Lattice Gauge Theories,” *Physical Review D* **11**, 395 (1975).  
18. G. ’t Hooft, “Cellular Automata as Models of Quantum Gravity,” in *Quantum Gravity* (1988).  
19. S. Wolfram, *A New Kind of Science* (Wolfram Media, 2002).  
20. E. Fredkin and T. Toffoli, “Conservative Logic,” *International Journal of Theoretical Physics* **21**, 219 (1982).  
21. G. Vidal, “Entanglement Renormalization,” *Physical Review Letters* **99**, 220405 (2007).  
22. B. Swingle, “Entanglement Renormalization and Holography,” *Physical Review D* **86**, 065007 (2012).  
23. F. Pastawski, B. Yoshida, D. Harlow, and J. Preskill, “Holographic Quantum Error-Correcting Codes,” *Journal of High Energy Physics* **1506**, 149 (2015).  
24. S. Abramsky and B. Coecke, “A Categorical Semantics of Quantum Protocols,” *Proceedings of the 19th IEEE Symposium on Logic in Computer Science* (2004).  
25. B. Coecke and A. Kissinger, *Picturing Quantum Processes* (Cambridge University Press, 2017).  
26. P. Hayden and J. Preskill, “Black Holes as Mirrors: Quantum Information in Random Subsystems,” *Journal of High Energy Physics* **0709**, 120 (2007).  
27. Y. Sekino and L. Susskind, “Fast Scramblers,” *Journal of High Energy Physics* **0810**, 065 (2008).  
28. D. Harlow and P. Hayden, “Quantum Computation vs. Firewalls,” *Journal of High Energy Physics* **1306**, 085 (2013).  
29. L. Susskind, “Computational Complexity and Black Hole Horizons,” *Fortschritte der Physik* **64**, 24 (2016).  
30. A. R. Brown, D. A. Roberts, L. Susskind, B. Swingle, and Y. Zhao, “Complexity, Action, and Black Holes,” *Physical Review D* **93**, 086006 (2016).
