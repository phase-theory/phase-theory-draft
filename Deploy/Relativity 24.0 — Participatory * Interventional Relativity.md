# Relativity 24.0 — Participatory / Interventional Relativity  
## The Observer as Physical Intervention and the Relativity of Facts

**White paper / academic preprint**

---

## Abstract

Participatory / Interventional Relativity is the operational completion of the relational turn in quantum physics. It replaces the classical ideal of a passive observer who discovers pre-existing facts with a physical principle: an observer is a system that intervenes, measures, records, and thereby defines a frame in which relational facts become actual. The basic probabilistic object is not merely an unconditional probability \(P(O)\), but an intervention-conditioned probability,

\[
P(O\,|\,\mathrm{do}(I)),
\]

where \(\mathrm{do}(I)\) denotes a physical intervention performed by an observer or apparatus. In quantum theory, interventions are represented by instruments, quantum channels, process tensors, or process matrices. Facts are not absolute global properties. They are records established relative to an intervention context. This framework gives operational meaning to Wheeler’s participatory universe, extends quantum reference frames and relational quantum mechanics, clarifies delayed-choice and Wigner’s-friend scenarios, and provides a language for quantum causal models with definite or indefinite causal order. The central principle is:

\[
\boxed{
\text{To observe is to intervene; to intervene is to define a frame.}
}
\]

Participatory Relativity does not imply solipsism or arbitrary reality. It asserts that physical facts are relational achievements produced by interactions between systems, constrained by a global quantum process and made objective through stable, redundant records.

---

## 1. Introduction

Classical physics imagines an observer outside the world.

The observer looks in, records pre-existing properties, and does not disturb the system in any fundamental way. Measurement reveals what was already there.

Quantum physics undermines this picture.

A measurement is not a passive revelation. It is a physical interaction. It changes the state. It creates a record. It defines the basis in which a fact becomes definite.

John Archibald Wheeler expressed this radical idea in the phrase “participatory universe.” He suggested that observers are not detached spectators but participants in the emergence of physical reality.

Participatory / Interventional Relativity makes this idea precise.

It says:

\[
\boxed{
\text{An observer is not a mind outside nature. An observer is a physical intervention inside nature.}
}
\]

The observer chooses an operation, couples to a system, produces a record, and thereby defines a frame of facts.

This is not mysticism. It is the operational structure of quantum theory, quantum causal inference, and relational quantum mechanics.

---

## 2. From Observation to Intervention

In ordinary probability theory, one writes

\[
P(O),
\]

the probability of observing outcome \(O\).

But observation is not merely conditioning on information. It is an action.

The relevant object is

\[
P(O\,|\,\mathrm{do}(I)),
\]

the probability of outcome \(O\) given that intervention \(I\) is performed.

The notation \(\mathrm{do}(I)\) comes from causal inference. It distinguishes between seeing and doing.

For example,

\[
P(Y\,|\,X=x)
\]

is the probability of \(Y\) given that we observe \(X=x\).

But

\[
P(Y\,|\,\mathrm{do}(X=x))
\]

is the probability of \(Y\) given that we intervene to set \(X=x\).

These are not the same.

Observation reveals correlations. Intervention tests causation.

Participatory Relativity elevates this distinction to a physical principle.

---

## 3. Classical Interventions and the Do-Calculus

Consider a set of classical variables \(V_1,\ldots,V_n\) with a causal directed acyclic graph.

The pre-intervention joint distribution factorizes as

\[
P(v_1,\ldots,v_n)
=
\prod_i
P(v_i\,|\,\mathrm{pa}_i),
\]

where \(\mathrm{pa}_i\) are the parents of \(V_i\) in the causal graph.

An intervention \(\mathrm{do}(X=x)\) removes the arrows into \(X\) and fixes \(X=x\).

The post-intervention distribution is

\[
P(v\,|\,\mathrm{do}(X=x))
=
\prod_{i:V_i\neq X}
P(v_i\,|\,\mathrm{pa}_i)
\bigg|_{X=x}.
\]

This is the truncated factorization formula.

If a set of variables \(Z\) satisfies the backdoor criterion, then

\[
P(Y\,|\,\mathrm{do}(X=x))
=
\sum_z
P(Y\,|\,X=x,Z=z)
P(Z=z).
\]

Thus interventions allow one to infer causal effects from observational data under suitable conditions.

Participatory Relativity takes this structure and quantizes it.

---

## 4. Quantum Interventions

In quantum theory, an intervention is represented by a quantum instrument.

A quantum instrument is a collection of completely positive trace-nonincreasing maps,

\[
\{\mathcal{I}_k\},
\]

such that

\[
\sum_k \mathcal{I}_k
\]

is trace-preserving.

If a system is in state \(\rho\), the probability of outcome \(k\) is

\[
P(k)
=
\operatorname{Tr}
\left[
\mathcal{I}_k(\rho)
\right].
\]

The post-intervention state is

\[
\rho_k
=
\frac{
\mathcal{I}_k(\rho)
}{
P(k)
}.
\]

A projective measurement is a special case:

\[
\mathcal{I}_k(\rho)
=
P_k \rho P_k,
\]

where \(P_k\) are projectors satisfying

\[
\sum_k P_k=I.
\]

But interventions are more general than measurements. They include preparations, transformations, feedback operations, erasures, and controlled couplings.

Thus:

\[
\boxed{
\text{Measurement is one kind of intervention, not the whole of observation.}
}
\]

---

## 5. Intervention-Conditioned Quantum Probabilities

Let an observer perform intervention \(\mathcal{I}_i\) and later observe outcome \(o\) associated with effect \(E_o\).

The intervention-conditioned probability is

\[
P(o\,|\,\mathrm{do}(\mathcal{I}_i))
=
\operatorname{Tr}
\left[
E_o
\mathcal{I}_i(\rho)
\right].
\]

If the intervention has outcome \(i\), the joint probability is

\[
P(i,o)
=
\operatorname{Tr}
\left[
E_o
\mathcal{I}_i(\rho)
\right].
\]

The conditional probability of \(o\) given \(i\) is

\[
P(o\,|\,i)
=
\frac{
\operatorname{Tr}
\left[
E_o
\mathcal{I}_i(\rho)
\right]
}{
\operatorname{Tr}
\left[
\mathcal{I}_i(\rho)
\right]
}.
\]

This is the quantum version of

\[
P(O\,|\,\mathrm{do}(I)).
\]

The intervention is not a passive update of knowledge. It is a physical map on the state.

---

## 6. Quantum Causal Models

Classical causal models use directed acyclic graphs. Quantum causal models generalize this structure.

A quantum causal model consists of:

1. quantum systems as nodes,
2. quantum channels as causal influences,
3. instruments as interventions,
4. conditional independence constraints,
5. a global process.

For a simple bipartite scenario, system \(A\) may influence system \(B\) through a channel

\[
\mathcal{E}_{A\to B}.
\]

If \(A\) is prepared in state \(\rho_A\), then

\[
\rho_B
=
\mathcal{E}_{A\to B}(\rho_A).
\]

An intervention at \(A\) changes the downstream statistics at \(B\).

The probability of outcome \(b\) after intervention \(\mathcal{I}_a\) at \(A\) is

\[
P(b\,|\,\mathrm{do}(\mathcal{I}_a))
=
\operatorname{Tr}
\left[
E_b
\mathcal{E}_{A\to B}
\left(
\mathcal{I}_a(\rho_A)
\right)
\right].
\]

Thus causal structure is encoded in how interventions propagate.

---

## 7. Process Tensors and Quantum Combs

For multi-time processes, a single channel is insufficient. One needs a process tensor or quantum comb.

A quantum comb describes a sequence of interventions at times \(t_0,t_1,\ldots,t_n\).

The process tensor \(\Upsilon_{n:0}\) is a positive operator acting on the tensor product of input and output spaces at each time.

A sequence of interventions

\[
\{\mathcal{I}_{k_0}^{(0)},
\mathcal{I}_{k_1}^{(1)},
\ldots,
\mathcal{I}_{k_n}^{(n)}\}
\]

has Choi operators

\[
J_{k_j}^{(j)}.
\]

The probability of the outcome sequence \(\mathbf{k}=(k_0,\ldots,k_n)\) is

\[
P(\mathbf{k})
=
\operatorname{Tr}
\left[
\left(
J_{k_n}^{(n)}
\otimes
\cdots
\otimes
J_{k_0}^{(0)}
\right)
\Upsilon_{n:0}
\right].
\]

This is the most general operational probability rule for quantum processes with interventions.

It replaces the simple state-update picture with a global process constrained by local interventions.

Thus:

\[
\boxed{
\text{Reality is not a state evolving under observation. It is a process responding to interventions.}
}
\]

---

## 8. Process Matrices and Indefinite Causal Order

In ordinary quantum causal models, causal order is fixed.

But quantum theory permits indefinite causal order.

The process-matrix formalism describes correlations between local interventions without assuming a global causal order.

Let observers \(A,B,\ldots\) perform local instruments with Choi operators

\[
M_A^a,
\quad
M_B^b,
\quad
\ldots
\]

The probability of outcomes \(a,b,\ldots\) is

\[
P(a,b,\ldots)
=
\operatorname{Tr}
\left[
W
\left(
M_A^a
\otimes
M_B^b
\otimes
\cdots
\right)
\right],
\]

where \(W\) is the process matrix.

The process matrix satisfies linear constraints ensuring valid probabilities:

\[
W\geq 0,
\]

\[
\mathcal{L}(W)=0.
\]

The quantum switch is the canonical example.

A control qubit determines the order of operations \(A\) and \(B\):

\[
\ket{0}\ket{\psi}
\mapsto
\ket{0}\,B A\ket{\psi},
\]

\[
\ket{1}\ket{\psi}
\mapsto
\ket{1}\,A B\ket{\psi}.
\]

For a control superposition,

\[
\frac{1}{\sqrt{2}}
\left(
\ket{0}+\ket{1}
\right),
\]

the resulting process has no definite causal order between \(A\) and \(B\).

Thus interventions themselves can be placed in quantum superposition.

Participatory Relativity must therefore allow not only observer-relative frames but observer-defined causal frames.

---

## 9. The Observer as a Physical System

In Participatory Relativity, an observer is not outside the formalism.

An observer is a physical system \(O\) with:

1. internal degrees of freedom,
2. memory states,
3. measurement apparatuses,
4. intervention capabilities,
5. records.

A measurement interaction may be modeled as

\[
\ket{s}\ket{O_0}
\rightarrow
\ket{s}\ket{O_s},
\]

where \(\ket{O_s}\) is a record state.

For a superposition,

\[
\sum_s c_s\ket{s}\ket{O_0}
\rightarrow
\sum_s c_s\ket{s}\ket{O_s}.
\]

Relative to the observer \(O\), one outcome is recorded.

Relative to an external observer \(W\), the combined system may remain in a superposition.

This is the core of Wigner’s-friend scenarios.

Participatory Relativity says that both descriptions can be valid, because facts are relative to intervention contexts.

---

## 10. Relational Facts

A fact is not a free-floating property of the universe.

A fact is a stable correlation between a system and a record.

Let \(S\) be a system and \(O\) an observer. After an intervention, the joint state contains correlations:

\[
\rho_{SO}
=
\sum_s p_s
\ket{s}\bra{s}_S
\otimes
\ket{O_s}\bra{O_s}.
\]

Relative to \(O\), the fact is:

\[
S=s.
\]

Relative to another system \(W\) that has not interacted with \(O\), the state may still be coherent.

Thus:

\[
\boxed{
\text{Facts are relational records, not absolute properties.}
}
\]

This is the operational meaning of relational quantum mechanics.

---

## 11. Intervention Frames

An intervention context defines a frame.

An intervention frame includes:

1. the choice of system,
2. the choice of observable,
3. the measurement basis,
4. the time of intervention,
5. the coarse-graining,
6. the reference system,
7. the record structure,
8. the accessible algebra of observables.

Changing the intervention frame can change which facts are defined.

This generalizes the notion of a reference frame.

In special relativity, a frame is a choice of coordinates and motion.

In quantum reference frames, a frame is a quantum system relative to which other systems are described.

In Participatory Relativity, a frame is an intervention context relative to which facts become actual.

Thus:

\[
\boxed{
\text{A frame is not merely a coordinate system. It is an intervention that defines facts.}
}
\]

---

## 12. Wheeler’s Participatory Universe

Wheeler’s participatory universe was motivated by delayed-choice experiments.

In a Mach–Zehnder interferometer, a photon can exhibit wave-like interference or particle-like which-path behavior depending on whether a final beamsplitter is inserted.

The delayed-choice version inserts or removes the beamsplitter after the photon has entered the apparatus.

The photon does not possess a pre-existing answer to the question:

\[
\text{Did it take one path or both?}
\]

The answer depends on the final intervention.

In path-integral language, the amplitude is

\[
\mathcal{A}
=
\sum_{\text{paths}}
e^{iS[\text{path}]/\hbar}.
\]

The final measurement context determines which question is asked of the sum over histories.

Thus the fact is not revealed. It is enacted by the intervention.

Wheeler’s slogan becomes:

\[
\boxed{
\text{No phenomenon is a phenomenon until it is an observed phenomenon.}
}
\]

Participatory Relativity gives this slogan a formal structure: interventions define the questions, and quantum processes supply the conditional answers.

---

## 13. Delayed Choice as Intervention Conditioning

Let \(I\) denote the intervention of inserting or removing the final beamsplitter.

Let \(O\) denote the observed outcome.

The relevant probability is not

\[
P(O),
\]

but

\[
P(O\,|\,\mathrm{do}(I)).
\]

If \(I\) is the interference measurement, then

\[
P(O\,|\,\mathrm{do}(I_{\text{int}}))
\]

shows interference fringes.

If \(I\) is the which-path measurement, then

\[
P(O\,|\,\mathrm{do}(I_{\text{path}}))
\]

shows particle-like statistics.

The system does not carry a context-independent answer.

The intervention defines the observable, and the observable defines the fact.

---

## 14. Wigner’s Friend and Relational Consistency

In Wigner’s friend scenario, an observer \(F\) measures a system \(S\).

Relative to \(F\), an outcome occurs:

\[
S=s.
\]

Relative to Wigner \(W\), the joint system may be described as

\[
\sum_s c_s
\ket{s}_S
\ket{F_s}_F.
\]

Are these descriptions contradictory?

Participatory Relativity says no.

They are facts relative to different intervention frames.

The descriptions must satisfy consistency conditions when the frames interact.

If Wigner measures the friend in the record basis, he will find a record consistent with the friend’s outcome.

If Wigner measures in a complementary basis, he may observe coherence, but then the friend’s record basis is not the relevant fact basis.

Thus:

\[
\boxed{
\text{Different observers may have different facts, but those facts must be consistently composable when compared.}
}
\]

---

## 15. Quantum Darwinism and Objective Facts

If facts are relational, how does objectivity arise?

Quantum Darwinism provides an answer.

A system \(S\) interacts with an environment \(E\) composed of many fragments \(E_1,\ldots,E_N\).

Redundant records of \(S\) are imprinted in the environment:

\[
\ket{s}\ket{E_0}
\rightarrow
\ket{s}
\ket{E_s^{(1)}}
\ket{E_s^{(2)}}
\cdots
\ket{E_s^{(N)}}.
\]

The global state becomes approximately

\[
\rho_{SE}
=
\sum_s p_s
\ket{s}\bra{s}_S
\otimes
\rho_{E_1}^{(s)}
\otimes
\rho_{E_2}^{(s)}
\otimes
\cdots
\otimes
\rho_{E_N}^{(s)}.
\]

Many observers can independently access fragments of the environment and infer the same pointer state of \(S\).

Thus objective facts are not absolute facts. They are facts that are redundantly recorded and stable under many non-disturbing interventions.

Objectivity becomes intersubjective redundancy.

---

## 16. Participatory Cosmology

Participatory Relativity has cosmological implications.

The universe has no external observer.

All observations are internal interventions performed by subsystems of the universe.

Cosmological facts are therefore not facts seen from outside. They are records established inside.

The cosmic microwave background, galaxy distributions, primordial perturbations, and local measurements are all intervention-relative records.

The wavefunction of the universe, if it exists, is not observed from outside. It is constrained by internal interventions.

Thus cosmology becomes participatory:

\[
\boxed{
\text{The universe observes itself through internal interventions.}
}
\]

Wheeler’s “self-excited circuit” is the universe generating records of itself from within itself.

---

## 17. Intervention in Quantum Field Theory

In quantum field theory, an intervention is a local operation in a spacetime region.

Let \(\mathcal{O}\) be a spacetime region. An intervention may be represented by a completely positive map

\[
\mathcal{I}_{\mathcal{O}}
\]

acting on the algebra of observables \(\mathcal{A}(\mathcal{O})\).

Correlation functions become intervention-conditioned:

\[
\left\langle
\phi(x_1)\cdots
\mathcal{I}_{\mathcal{O}}
\cdots
\phi(x_n)
\right\rangle.
\]

The choice of intervention defines which question is asked of the field.

In the path-integral picture, an intervention modifies boundary or intermediate conditions:

\[
\mathcal{A}(O\,|\,\mathrm{do}(I))
=
\int_{\text{histories compatible with }I}
\mathcal{D}\phi
\,
e^{iS[\phi]/\hbar}
\,
O[\phi].
\]

Thus even field-theoretic facts are intervention-conditioned.

---

## 18. Gravity and Observer-Relative Facts

In general relativity, observers define local frames.

An observer’s tetrad

\[
e^a{}_\mu(x)
\]

defines a local Lorentz frame.

Measurements are made relative to this frame.

In quantum gravity, this becomes deeper.

A relational observable has the form

\[
O_{S|O},
\]

meaning the value of system \(S\) relative to observer \(O\).

In a diffeomorphism-invariant theory, there are no absolute local observables. Observables must be relational:

\[
\phi(x)
\quad
\text{is not gauge-invariant,}
\]

but

\[
\phi\big|_{T^\mu(x)=X^\mu}
\]

is relational, where \(T^\mu\) are physical reference fields.

Participatory Relativity adds:

\[
\boxed{
\text{The relational frame is established by an intervention.}
}
\]

The observer does not merely choose coordinates. The observer physically couples to reference systems and creates records.

---

## 19. Black Holes and Complementarity

Black holes provide a profound example.

An exterior observer describes Hawking radiation and horizon degrees of freedom.

An infalling observer describes a smooth horizon and interior modes.

These descriptions are not globally simultaneous classical accounts. They are intervention-relative descriptions.

The exterior observer’s facts are defined by interventions outside the horizon.

The infalling observer’s facts are defined by interventions crossing the horizon.

In code-subspace language, interior operators are valid only within appropriate code subspaces and relative to appropriate observer algebras.

Thus black-hole complementarity is a form of Participatory Relativity:

\[
\boxed{
\text{Interior and exterior facts are relative to different intervention contexts.}
}
\]

---

## 20. Causation as Interventional Structure

Participatory Relativity also clarifies causation.

In classical physics, causation is often imagined as a relation between events.

In interventionist causality, causation is defined by response to interventions.

\(X\) causes \(Y\) if changing \(X\) by intervention changes the distribution of \(Y\):

\[
P(Y\,|\,\mathrm{do}(X=x))
\neq
P(Y\,|\,\mathrm{do}(X=x')).
\]

In quantum theory, this becomes:

\[
P(b\,|\,\mathrm{do}(\mathcal{I}_a))
\neq
P(b\,|\,\mathrm{do}(\mathcal{I}_{a'})).
\]

Thus causation is not passive correlation. It is sensitivity to intervention.

This fits naturally with quantum causal models and process matrices.

---

## 21. No-Signaling and Participatory Constraints

If observers participate in creating facts, can they create arbitrary realities?

No.

Interventions are constrained by the global quantum process.

No-signaling requires that an intervention by Alice cannot change Bob’s marginal statistics if no causal channel connects them:

\[
\sum_a P(a,b\,|\,\mathrm{do}(\mathcal{I}_a))
=
P(b).
\]

Thus participatory facts are not subjective whims.

They are constrained by:

1. the quantum state or process,
2. causal structure,
3. conservation laws,
4. unitarity,
5. consistency of records,
6. redundancy and decoherence.

Participation is real, but it is not omnipotent.

---

## 22. Relation to Quantum Reference Frames

Relativity 7.0, Quantum Reference Frames, showed that frames are quantum systems.

Participatory Relativity extends this:

A quantum reference frame is not merely a system relative to which states are described. It is a system relative to which interventions define facts.

Thus:

\[
\text{quantum frame}
\rightarrow
\text{intervention frame}
\rightarrow
\text{relational facts}.
\]

The observer is not only a coordinate anchor. The observer is an agent of physical intervention.

---

## 23. Relation to Relational Quantum Mechanics

Relational quantum mechanics says that quantum states are relative to systems.

Participatory Relativity gives this an operational foundation.

A state is not merely information relative to an observer. It is a tool for predicting the consequences of interventions relative to that observer.

Thus:

\[
\boxed{
\text{States are intervention-relative predictive structures.}
}
\]

Facts are the records produced when interventions occur.

---

## 24. Relation to Code-Subspace Relativity

Code-Subspace Relativity says that bulk spacetime is a protected approximate encoding inside a code subspace.

Participatory Relativity says that observers access that code subspace through interventions.

Different observers may reconstruct different but consistent logical operators depending on their accessible boundary regions.

Thus interior spacetime facts are observer- and intervention-relative.

---

## 25. Axioms of Participatory Relativity

The framework may be organized around nine axioms.

### Axiom 1: Observers Are Physical Systems

An observer is a system capable of interventions, records, and memory.

### Axiom 2: Observation Is Intervention

To observe is to perform a physical operation, not to passively reveal a pre-existing property.

### Axiom 3: Probabilities Are Intervention-Conditioned

The basic probability is

\[
P(O\,|\,\mathrm{do}(I)).
\]

### Axiom 4: Facts Are Relational Records

A fact is a stable correlation between a system and a record relative to an intervention context.

### Axiom 5: Frames Are Intervention Contexts

A frame is defined by the choice of intervention, observable, basis, coarse-graining, and reference system.

### Axiom 6: Global Processes Constrain Local Interventions

Local interventions are embedded in a global quantum process.

### Axiom 7: Consistency Is Required Upon Comparison

Different observer-relative facts must compose consistently when observers interact.

### Axiom 8: Objectivity Is Redundant Recordability

Objective facts are those redundantly recorded in many accessible subsystems.

### Axiom 9: Causation Is Intervention Sensitivity

\(X\) causes \(Y\) if interventions on \(X\) change the probabilities of \(Y\).

---

## 26. Experimental Relevance

Participatory Relativity is not merely philosophical. It is reflected in experiments.

### 26.1 Delayed-Choice Experiments

Delayed-choice interferometry shows that the measurement context determines whether wave-like or particle-like facts are recorded.

### 26.2 Quantum Eraser Experiments

Quantum erasers show that which-path facts can be erased or restored by later interventions on entangled partners.

### 26.3 Bell Tests

Bell experiments demonstrate that correlations cannot be explained by pre-existing local facts independent of measurement interventions.

### 26.4 Quantum Switch Experiments

Experiments with the quantum switch demonstrate that causal order itself can be placed under intervention control.

### 26.5 Wigner’s-Friend Experiments

Photonic and superconducting implementations of Wigner’s-friend scenarios test the consistency of observer-relative facts.

### 26.6 Quantum Darwinism Experiments

Experiments in photon scattering, spin environments, and superconducting circuits demonstrate redundant record formation.

These experiments support the operational core of Participatory Relativity.

---

## 27. Open Problems

Several major problems remain.

### 27.1 Measurement Problem

Participatory Relativity clarifies the role of intervention but does not by itself solve the measurement problem.

### 27.2 Observer Definition

A precise physical criterion for what counts as an observer or record remains open.

### 27.3 Wigner’s-Friend No-Go Theorems

Extended Wigner’s-friend scenarios raise subtle consistency constraints.

### 27.4 Indefinite Causal Order

A complete theory of interventions in indefinite causal structures is still developing.

### 27.5 Quantum Gravity

Interventions in diffeomorphism-invariant quantum gravity require relational reference systems and code-subspace reconstruction.

### 27.6 Cosmological Participation

A rigorous formulation of internal observation in quantum cosmology remains incomplete.

### 27.7 Agency and Free Intervention

The status of “free” interventions in a deterministic or block-universe picture requires clarification.

---

## 28. What Einstein Would Think

Einstein would resist Participatory Relativity.

He believed in an observer-independent reality. He famously asked whether the Moon exists only when someone looks at it.

Participatory Relativity does not deny the Moon. It says that the Moon’s definite properties are established through stable physical interactions and redundant records.

But Einstein would dislike the idea that facts are relative to intervention contexts.

Still, he would recognize the operational lesson.

His own relativity began by asking what observers can measure. Participatory Relativity asks a deeper question:

\[
\text{What does it mean to measure at all?}
\]

The answer is that measurement is intervention.

Einstein might reject the participatory ontology. But he would respect the operational rigor.

---

## 29. Summary of Core Equations

### Intervention-conditioned probability

\[
P(O\,|\,\mathrm{do}(I)).
\]

### Classical post-intervention distribution

\[
P(v\,|\,\mathrm{do}(X=x))
=
\prod_{i:V_i\neq X}
P(v_i\,|\,\mathrm{pa}_i)
\bigg|_{X=x}.
\]

### Quantum instrument probability

\[
P(k)
=
\operatorname{Tr}
\left[
\mathcal{I}_k(\rho)
\right].
\]

### Post-intervention state

\[
\rho_k
=
\frac{
\mathcal{I}_k(\rho)
}{
P(k)
}.
\]

### Intervention-conditioned quantum probability

\[
P(o\,|\,\mathrm{do}(\mathcal{I}_i))
=
\operatorname{Tr}
\left[
E_o
\mathcal{I}_i(\rho)
\right].
\]

### Process-tensor probability

\[
P(\mathbf{k})
=
\operatorname{Tr}
\left[
\left(
J_{k_n}^{(n)}
\otimes
\cdots
\otimes
J_{k_0}^{(0)}
\right)
\Upsilon_{n:0}
\right].
\]

### Process-matrix probability

\[
P(a,b,\ldots)
=
\operatorname{Tr}
\left[
W
\left(
M_A^a
\otimes
M_B^b
\otimes
\cdots
\right)
\right].
\]

### Measurement as entangling intervention

\[
\sum_s c_s\ket{s}\ket{O_0}
\rightarrow
\sum_s c_s\ket{s}\ket{O_s}.
\]

### Quantum Darwinist record state

\[
\rho_{SE}
=
\sum_s p_s
\ket{s}\bra{s}_S
\otimes
\rho_{E_1}^{(s)}
\otimes
\cdots
\otimes
\rho_{E_N}^{(s)}.
\]

### Relational observable

\[
O_{S|O}.
\]

### Central principle

\[
\boxed{
\text{To observe is to intervene; to intervene is to define a frame.}
}
\]

---

## 30. Conclusion

Relativity 24.0, Participatory / Interventional Relativity, replaces the passive observer with the active participant.

The observer is not outside the world. The observer is a physical system that intervenes, measures, records, and defines a frame of facts.

The basic object of physics is not unconditional probability. It is intervention-conditioned probability:

\[
P(O\,|\,\mathrm{do}(I)).
\]

Facts are not absolute. They are relational records established by interventions. Objectivity is not a view from nowhere. It is the stability and redundancy of records across many possible interventions.

This framework operationalizes Wheeler’s participatory universe, extends relational quantum mechanics and quantum reference frames, clarifies delayed-choice and Wigner’s-friend scenarios, and provides a language for quantum causal models with definite or indefinite causal order.

The central principle is:

\[
\boxed{
\text{To observe is to intervene; to intervene is to define a frame.}
}
\]

Participatory Relativity does not make reality arbitrary. It makes reality relational, constrained, and enacted through physical interaction.

The universe is not a spectacle observed from outside. It is a participatory process in which observers are internal interventions.

This is Relativity 24.0.

---

## Appendix A: Rules of the Classical Do-Calculus

Given a causal graph \(G\), the intervention distribution is

\[
P(v\,|\,\mathrm{do}(X=x))
=
\prod_{i:V_i\neq X}
P(v_i\,|\,\mathrm{pa}_i)
\bigg|_{X=x}.
\]

The backdoor adjustment formula is

\[
P(Y\,|\,\mathrm{do}(X=x))
=
\sum_z
P(Y\,|\,X=x,Z=z)
P(Z=z),
\]

provided \(Z\) blocks all backdoor paths from \(X\) to \(Y\).

The front-door formula is

\[
P(Y\,|\,\mathrm{do}(X=x))
=
\sum_m
P(m\,|\,X=x)
\sum_{x'}
P(Y\,|\,X=x',M=m)
P(x').
\]

These rules distinguish observation from intervention.

---

## Appendix B: Quantum Instruments and Choi Operators

A quantum instrument \(\{\mathcal{I}_k\}\) consists of completely positive maps satisfying

\[
\sum_k \mathcal{I}_k
=
\mathcal{E},
\]

where \(\mathcal{E}\) is trace-preserving.

The Choi operator of \(\mathcal{I}_k\) is

\[
J_k
=
(\mathcal{I}_k\otimes \mathbb{I})
\left(
\ket{\Phi^+}\bra{\Phi^+}
\right),
\]

where

\[
\ket{\Phi^+}
=
\sum_i \ket{i}\ket{i}.
\]

The probability of outcome \(k\) for input state \(\rho\) is

\[
P(k)
=
\operatorname{Tr}
\left[
J_k
(\rho^T\otimes I)
\right].
\]

This provides a fully quantum representation of interventions.

---

## Appendix C: Process Tensor Probability

For a multi-time quantum process, the process tensor \(\Upsilon_{n:0}\) encodes all causal influences.

A sequence of interventions with Choi operators

\[
J_{k_0}^{(0)},
\ldots,
J_{k_n}^{(n)}
\]

produces outcome sequence probability

\[
P(k_0,\ldots,k_n)
=
\operatorname{Tr}
\left[
\left(
J_{k_n}^{(n)}
\otimes
\cdots
\otimes
J_{k_0}^{(0)}
\right)
\Upsilon_{n:0}
\right].
\]

This is the quantum generalization of intervention-conditioned probability.

---

## Appendix D: Relational Measurement Model

Let a system be in state

\[
\ket{\psi}_S
=
\sum_s c_s\ket{s}_S.
\]

Let an observer begin in ready state \(\ket{O_0}\).

A measurement interaction gives

\[
U
\left(
\sum_s c_s\ket{s}_S
\ket{O_0}
\right)
=
\sum_s c_s
\ket{s}_S
\ket{O_s}.
\]

Relative to the observer, a record \(s\) exists.

Relative to a superobserver who has not intervened, the joint state may remain coherent.

Thus facts are relative to intervention context.

---

## Appendix E: Quantum Switch as Interventional Indefinite Order

Let \(A\) and \(B\) be operations.

The quantum switch acts as

\[
\ket{0}_C\ket{\psi}_S
\mapsto
\ket{0}_C
B A\ket{\psi}_S,
\]

\[
\ket{1}_C\ket{\psi}_S
\mapsto
\ket{1}_C
A B\ket{\psi}_S.
\]

For a control superposition,

\[
\frac{1}{\sqrt{2}}
\left(
\ket{0}+\ket{1}
\right)
\ket{\psi},
\]

the final state is

\[
\frac{1}{\sqrt{2}}
\left(
\ket{0}B A\ket{\psi}
+
\ket{1}A B\ket{\psi}
\right).
\]

The order of interventions is not definite.

Thus the intervention context itself can be quantum.

---

## Selected References

1. J. A. Wheeler, “Law Without Law,” in *Quantum Theory and Measurement*, ed. J. A. Wheeler and W. H. Zurek (Princeton University Press, 1983).  
2. J. A. Wheeler, “Information, Physics, Quantum: The Search for Links,” in *Complexity, Entropy, and the Physics of Information* (Addison-Wesley, 1990).  
3. J. Pearl, *Causality: Models, Reasoning, and Inference* (Cambridge University Press, 2000).  
4. P. Spirtes, C. Glymour, and R. Scheines, *Causation, Prediction, and Search* (MIT Press, 2000).  
5. M. S. Leifer and R. W. Spekkens, “Towards a Formulation of Quantum Theory as a Causally Neutral Theory of Bayesian Inference,” *Physical Review A* **88**, 052130 (2013).  
6. J. Allen, J. Barrett, D. Horsman, C. M. Lee, and S. Spekkens, “Quantum Common Causes and Quantum Causal Models,” *Physical Review X* **7**, 031021 (2017).  
7. R. Chiribella, G. M. D’Ariano, and P. Perinotti, “Quantum Circuits with Indefinite Causal Structure,” *Physical Review Letters* **101**, 060401 (2008).  
8. G. Chiribella, G. M. D’Ariano, and P. Perinotti, “Theoretical Framework for Quantum Networks,” *Physical Review A* **80**, 022339 (2009).  
9. O. Oreshkov, F. Costa, and Č. Brukner, “Quantum Correlations with No Causal Order,” *Nature Communications* **3**, 1092 (2012).  
10. G. Rubino et al., “Experimental Verification of an Indefinite Causal Order,” *Science Advances* **3**, e1602589 (2017).  
11. K. Goswami et al., “Indefinite Causal Order in a Quantum Switch,” *Physical Review Letters* **121**, 090503 (2018).  
12. C. Rovelli, “Relational Quantum Mechanics,” *International Journal of Theoretical Physics* **35**, 1637 (1996).  
13. C. Rovelli, “Relational Quantum Mechanics,” in *Compendium of Quantum Physics* (Springer, 2009).  
14. Č. Brukner, “On the Quantum Measurement Problem,” in *Quantum [Un]Speakables II* (Springer, 2017).  
15. D. Frauchiger and R. Renner, “Quantum Theory Cannot Consistently Describe the Use of Itself,” *Nature Communications* **9**, 3711 (2018).  
16. W. H. Zurek, “Decoherence, Einselection, and the Quantum Origins of the Classical,” *Reviews of Modern Physics* **75**, 715 (2003).  
17. W. H. Zurek, “Quantum Darwinism,” *Nature Physics* **5**, 181 (2009).  
18. J.-A. Larsson, “Bell’s Inequality and Detector Inefficiency in the Aspect Experiment,” *Physical Review A* **57**, 3304 (1998).  
19. V. Jacques et al., “Experimental Realization of Wheeler’s Delayed-Choice Gedanken Experiment,” *Science* **315**, 966 (2007).  
20. X.-S. Ma et al., “Quantum Erasure with Causally Disconnected Choice,” *Proceedings of the National Academy of Sciences* **110**, 1221 (2013).  
21. A. Peres, *Quantum Theory: Concepts and Methods* (Kluwer, 1995).  
22. H. M. Wiseman and G. J. Milburn, *Quantum Measurement and Control* (Cambridge University Press, 2009).  
23. M. A. Nielsen and I. L. Chuang, *Quantum Computation and Quantum Information* (Cambridge University Press, 2000).  
24. C. M. Lee and J. Barrett, “Computation in Generalized Probabilistic Theories,” *New Journal of Physics* **17**, 053001 (2015).  
25. R. W. Spekkens, “Evidence for the Epistemic View of Quantum States: A Toy Theory,” *Physical Review A* **75**, 032110 (2007).
