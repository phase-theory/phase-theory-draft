# Relativity 35.0 — Semantic Relativity  
## The Theory-Relativity of Physical Meaning

**White paper / academic preprint**

---

## Abstract

Semantic Relativity is the hypothesis that the meaning of physical terms is not absolute but relative to a theory, model, operational context, scale, and interpretive framework. Terms such as “particle,” “field,” “event,” “observer,” “vacuum,” “time,” “measurement,” “mass,” “space,” and “law” do not possess fixed trans-theoretic meanings. Their meaning is determined by their role within a formal structure, an operational protocol, and an empirical model. A semantic interpretation may be represented as a functor,

\[
I:
\mathbf{Theory}
\rightarrow
\mathbf{EmpiricalModel},
\]

mapping formal theories to empirical models. The same formal structure may admit different interpretations, and different formal structures may yield the same empirical model. The central principle is:

\[
\boxed{
\text{Physical meaning is model-relative, but invariant empirical structure is physical.}
}
\]

Semantic Relativity is not semantic relativism. It does not claim that all meanings are equally valid or that truth is arbitrary. It claims that vocabulary must not be mistaken for reality. Physical content resides not in words or formal symbols alone, but in the invariant empirical structure preserved under admissible reinterpretations, dualities, gauge transformations, coarse-grainings, and theory changes.

---

## 1. Introduction

Physics is written in words and symbols.

We speak of particles, fields, forces, events, observers, measurements, vacua, time, space, energy, mass, and laws. These terms feel stable. They appear in textbooks as if they name fixed ingredients of reality.

But the history of physics shows otherwise.

The meaning of “mass” changed from Newtonian mechanics to special relativity to quantum field theory. The meaning of “particle” changed from classical point bodies to quantum excitations to detector clicks to string modes. The meaning of “vacuum” changed from empty space to ground state to observer-relative thermal state to holographic code-subspace structure. The meaning of “time” changed from absolute Newtonian time to proper time to dynamical spacetime coordinate to internal relational variable to emergent thermodynamic parameter.

Thus physical terms are not rigid labels attached to eternal entities.

They are nodes in a theoretical and operational structure.

Semantic Relativity makes this explicit.

It says:

\[
\boxed{
\text{The meaning of a physical term is its role within a theory-model-context structure.}
}
\]

This does not undermine physics. It clarifies physics.

It prevents us from confusing the map for the territory, the formalism for the world, or the vocabulary of one successful theory for the final furniture of reality.

---

## 2. The Semantic Problem in Physics

A physical theory contains at least three layers:

1. a formal syntax,
2. a mathematical structure,
3. an empirical interpretation.

The formal syntax includes symbols such as

\[
\psi,
\quad
\phi(x),
\quad
g_{\mu\nu},
\quad
\hat{H},
\quad
T_{\mu\nu}.
\]

The mathematical structure includes Hilbert spaces, manifolds, algebras, groups, categories, path integrals, and differential equations.

The empirical interpretation connects these structures to operations, measurements, observations, and predictions.

The semantic problem is:

\[
\text{Which parts of the formalism correspond to physical reality?}
\]

Semantic Relativity answers cautiously:

\[
\text{Only the invariant empirical structure under admissible reinterpretations is unqualifiedly physical.}
\]

Everything else may be representation, redundancy, approximation, or effective description.

---

## 3. The Structure of a Theory

A physical theory may be represented as a tuple,

\[
T
=
\left(
\mathcal{L},
\mathcal{M},
\mathcal{D},
\mathcal{O},
\mathcal{P},
\mathcal{V}
\right),
\]

where:

- \(\mathcal{L}\) is a formal language or signature,
- \(\mathcal{M}\) is a class of mathematical models,
- \(\mathcal{D}\) is a dynamics or action principle,
- \(\mathcal{O}\) is an algebra or category of observables,
- \(\mathcal{P}\) is a probability or prediction rule,
- \(\mathcal{V}\) is a domain of validity.

For example, in classical mechanics:

\[
\mathcal{L}
=
\{q^i,p_i,H,t\},
\]

\[
\mathcal{M}
=
\text{phase spaces},
\]

\[
\mathcal{D}
=
\text{Hamilton's equations},
\]

\[
\mathcal{O}
=
\text{functions on phase space},
\]

\[
\mathcal{P}
=
\text{deterministic prediction or statistical ensemble},
\]

\[
\mathcal{V}
=
\text{macroscopic, low-velocity, nonquantum regime}.
\]

In quantum field theory:

\[
\mathcal{L}
=
\{\phi,\psi,A_\mu,\mathcal{L},\hbar\},
\]

\[
\mathcal{M}
=
\text{Hilbert spaces, algebras, path integrals},
\]

\[
\mathcal{D}
=
\text{Euler--Lagrange or Schwinger--Dyson equations},
\]

\[
\mathcal{O}
=
\text{operator algebras},
\]

\[
\mathcal{P}
=
\text{Born rule},
\]

\[
\mathcal{V}
=
\text{specified energy and curvature regime}.
\]

A term’s meaning depends on its place in this structure.

---

## 4. Interpretation as a Functor

Semantic Relativity formalizes interpretation categorically.

Let \(\mathbf{Theory}\) be a category whose objects are theories and whose morphisms are translations, reductions, embeddings, or dualities.

Let \(\mathbf{EmpiricalModel}\) be a category whose objects are empirical models and whose morphisms are transformations preserving observational structure.

An interpretation is a functor,

\[
I:
\mathbf{Theory}
\rightarrow
\mathbf{EmpiricalModel}.
\]

For a theory \(T\), the interpreted empirical model is

\[
I(T).
\]

For a theory morphism

\[
f:T\rightarrow T',
\]

the interpretation assigns a corresponding empirical map,

\[
I(f):I(T)\rightarrow I(T').
\]

Functoriality requires

\[
I(g\circ f)
=
I(g)\circ I(f),
\]

and

\[
I(\mathrm{id}_T)
=
\mathrm{id}_{I(T)}.
\]

Thus interpretation is structure-preserving.

It is not arbitrary annotation. It maps theoretical structure into empirical structure in a coherent way.

---

## 5. Empirical Models

An empirical model may be represented as

\[
E
=
\left(
\mathcal{C},
\mathcal{A},
\mathcal{O},
P
\right),
\]

where:

- \(\mathcal{C}\) is a set of experimental contexts,
- \(\mathcal{A}\) is a set of actions or interventions,
- \(\mathcal{O}\) is a set of possible outcomes,
- \(P\) is a probability assignment,

\[
P:
\mathcal{C}\times\mathcal{A}
\rightarrow
\mathrm{Prob}(\mathcal{O}).
\]

Thus an empirical model tells us what happens when we do something in some context.

The basic empirical object is not a naked proposition. It is an intervention-outcome probability:

\[
P(o\mid a,C).
\]

Semantic Relativity is therefore operational at its core.

Meaning is tied to what can be done and what can be observed.

---

## 6. Same Formalism, Different Interpretations

A single formal structure may admit multiple interpretations.

Quantum mechanics is the clearest example.

The formalism includes:

\[
\ket{\psi},
\quad
\hat{H},
\quad
\hat{O},
\quad
P(o)=\bra{\psi}P_o\ket{\psi}.
\]

But the interpretation of \(\ket{\psi}\) varies.

It may be interpreted as:

1. a physical wave,
2. a state of knowledge,
3. a branch-relative state,
4. a betting disposition,
5. a tool for predicting measurement outcomes,
6. a vector in a high-dimensional configuration space,
7. an information-theoretic constraint.

The formalism may remain unchanged while the semantics differ.

Thus:

\[
\boxed{
\text{Formalism underdetermines interpretation.}
}
\]

Semantic Relativity does not say all interpretations are equally true. It says that if two interpretations yield the same empirical model, their difference is semantic or metaphysical rather than empirical.

---

## 7. Different Formalisms, Same Empirical Model

The converse also occurs.

Different formal structures may yield the same empirical model.

Examples include:

1. Schrödinger and Heisenberg pictures,
2. Lagrangian and Hamiltonian formulations,
3. path-integral and canonical quantization,
4. wave mechanics and matrix mechanics,
5. general relativity and teleparallel gravity,
6. AdS bulk gravity and boundary CFT,
7. electric-magnetic dual descriptions,
8. bosonization in two dimensions,
9. Kramers–Wannier dual Ising descriptions,
10. different gauge choices in gauge theory.

Let \(T\) and \(T'\) be formally different theories. If there exists an empirical isomorphism,

\[
I(T)
\cong
I(T'),
\]

then the two theories are empirically equivalent.

The physical content is not \(T\) alone or \(T'\) alone. It is the equivalence class,

\[
[T]
=
\{T'\mid I(T')\cong I(T)\}.
\]

Thus:

\[
\boxed{
\text{Physical content is invariant under empirically equivalent redescriptions.}
}
\]

---

## 8. The Meaning of “Particle”

The term “particle” illustrates semantic relativity.

### 8.1 Newtonian Meaning

In Newtonian mechanics, a particle is a localized body with a trajectory,

\[
x^i(t).
\]

It possesses definite position and momentum at all times.

### 8.2 Relativistic Meaning

In special relativity, a particle is associated with a worldline and an invariant mass,

\[
m^2c^2
=
p_\mu p^\mu.
\]

Mass is no longer velocity-dependent in the modern invariant sense.

### 8.3 Wigner Meaning

In relativistic quantum theory, a particle is an irreducible representation of the Poincaré group.

Mass and spin are Casimir invariants:

\[
P_\mu P^\mu
=
m^2c^2,
\]

\[
W_\mu W^\mu
=
-m^2c^2 s(s+1)\hbar^2,
\]

where \(W_\mu\) is the Pauli–Lubanski vector.

Thus a particle is not a tiny object. It is a representation-theoretic structure.

### 8.4 Quantum Field-Theoretic Meaning

In quantum field theory, particles are excitations of fields.

A one-particle state is created by an operator acting on the vacuum:

\[
\ket{f}
=
a^\dagger(f)\ket{0}.
\]

But particles are not always well-defined. In curved spacetime or accelerated frames, the notion of particle becomes observer-dependent.

### 8.5 Detector Meaning

Operationally, a particle may mean a detector click.

The probability of a click is given by an instrument:

\[
P(k)
=
\operatorname{Tr}
\left[
\mathcal{I}_k(\rho)
\right].
\]

Thus “particle” may mean a detection event rather than a persistent substance.

### 8.6 String-Theoretic Meaning

In string theory, what appears as a particle may be a vibrational mode of a string.

Thus the same word “particle” has different meanings in different theories.

---

## 9. The Meaning of “Field”

The term “field” also shifts.

### 9.1 Classical Field

A classical field is a function on spacetime,

\[
\phi:M\rightarrow V.
\]

For example,

\[
\phi(x)
\]

assigns a value to each spacetime point \(x\).

### 9.2 Quantum Field

A quantum field is not a classical function. It is an operator-valued distribution,

\[
\hat{\phi}(x),
\]

satisfying commutation or anticommutation relations:

\[
[\hat{\phi}(x),\hat{\phi}(y)]
=
0
\]

for spacelike separation.

### 9.3 Gauge Field

A gauge field is a connection,

\[
A_\mu,
\]

but the physical content is not the connection itself. It is the gauge orbit,

\[
[A_\mu],
\]

or gauge-invariant quantities such as field strengths,

\[
F_{\mu\nu},
\]

and Wilson loops,

\[
W(C)
=
\operatorname{Tr}
\mathcal{P}
\exp
\oint_C A.
\]

### 9.4 Effective Field

In effective field theory, a field may be a low-energy collective variable.

It need not be fundamental.

Thus “field” may mean classical variable, quantum operator, gauge connection, or emergent collective excitation.

---

## 10. The Meaning of “Event”

The meaning of “event” is also theory-relative.

### 10.1 Classical Event

In Newtonian physics, an event is something occurring at a place and absolute time:

\[
(x,y,z,t).
\]

### 10.2 Relativistic Event

In special and general relativity, an event is a point in spacetime.

But the coordinates assigned to it are frame-dependent:

\[
x^\mu
\rightarrow
x'^\mu(x).
\]

Einstein emphasized that physical events are coincidences: meetings of worldlines, pointer alignments, field coincidences.

A relational event may be written as

\[
\phi\big|_{T^\mu(x)=X^\mu},
\]

meaning the value of \(\phi\) where reference fields \(T^\mu\) take values \(X^\mu\).

### 10.3 Quantum Event

In quantum theory, an event may be a measurement outcome.

It is not a pre-existing property. It is an actualized outcome within a context.

Thus “event” may mean spacetime point, field coincidence, detector outcome, or history proposition.

---

## 11. The Meaning of “Observer”

The term “observer” is especially prone to semantic confusion.

### 11.1 Classical Observer

In classical physics, an observer is often an idealized coordinate frame.

### 11.2 Relativistic Observer

In relativity, an observer may be a timelike worldline with a tetrad,

\[
e^a{}_\mu(\tau),
\]

defining a local frame.

### 11.3 Quantum Observer

In quantum theory, an observer may be a physical system that becomes correlated with another system:

\[
\sum_i c_i\ket{s_i}\ket{O_0}
\rightarrow
\sum_i c_i\ket{s_i}\ket{O_i}.
\]

### 11.4 Operational Observer

Operationally, an observer is an intervention-capable system that records outcomes.

### 11.5 Algebraic Observer

In algebraic quantum field theory, an observer may be associated with an accessible algebra of observables,

\[
\mathcal{A}(\mathcal{O}),
\]

defined over a spacetime region \(\mathcal{O}\).

Thus “observer” may mean coordinate frame, physical system, recording apparatus, algebraic access structure, or intervention protocol.

---

## 12. The Meaning of “Vacuum”

The vacuum is another semantically unstable term.

### 12.1 Classical Vacuum

Classically, vacuum means absence of matter.

### 12.2 Quantum Vacuum

In quantum field theory, the vacuum is the ground state of a Hamiltonian:

\[
\hat{H}\ket{0}
=
E_0\ket{0}.
\]

Equivalently, it is annihilated by annihilation operators:

\[
a_k\ket{0}=0.
\]

### 12.3 Observer-Relative Vacuum

The Unruh effect shows that the vacuum is observer-relative.

The Minkowski vacuum appears thermal to an accelerated observer:

\[
T_{\text{Unruh}}
=
\frac{\hbar a}{2\pi k_{\text{B}}c}.
\]

Thus “empty space.

### 12.5 Holographic Vacuum

In holography, the vacuum may be a highly entangled boundary state whose bulk interpretation is a smooth geometry.

Thus “vacuum” may mean emptiness, ground state, thermal state, false vacuum, or code-subspace reference state.

---

## 13. The Meaning of “Time”

The meaning of time is perhaps the deepest example of semantic relativity.

### 13.1 Newtonian Time

In Newtonian mechanics, time is absolute:

\[
t.
\]

It flows uniformly for all observers.

### 13.2 Relativistic Time

In special relativity, time is frame-dependent. Proper time along a worldline is

\[
d\tau^2
=
-
\frac{1}{c^2}
g_{\mu\nu}dx^\mu dx^\nu.
\]

### 13.3 Dynamical Time

In general relativity, time is part of dynamical geometry.

There is no preferred global time in general spacetimes.

### 13.4 Quantum Time

In ordinary quantum mechanics, time is an external parameter:

\[
i\hbar\frac{d}{dt}\ket{\psi(t)}
=
\hat{H}\ket{\psi(t)}.
\]

### 13.5 Timeless Quantum Gravity

In canonical quantum gravity, the Wheeler–DeWitt equation is

\[
\hat{\mathcal{H}}\Psi=0.
\]

There is no external time parameter.

### 13.6 Relational Time

Time may be defined relationally using an internal clock variable \(T\):

\[
P(O\mid T=t).
\]

### 13.7 Thermal Time

In some approaches, time flow is generated by a modular Hamiltonian:

\[
K
=
-\ln\rho.
\]

Thus “time” may mean absolute parameter, proper time, coordinate time, internal clock, modular flow, or emergent thermodynamic direction.

---

## 14. The Meaning of “Measurement”

The term “measurement” also shifts.

### 14.1 Classical Measurement

Classically, measurement reveals a pre-existing value.

### 14.2 Projective Measurement

In elementary quantum mechanics, measurement is represented by projectors \(P_i\):

\[
P(i)
=
\operatorname{Tr}(\rho P_i).
\]

### 14.3 POVM Measurement

More generally, measurement is represented by effects \(E_i\):

\[
P(i)
=
\operatorname{Tr}(\rho E_i),
\]

with

\[
E_i\geq 0,
\qquad
\sum_i E_i=I.
\]

### 14.4 Instrument Measurement

A quantum instrument includes both outcome probabilities and post-measurement states:

\[
\rho_i
=
\frac{\mathcal{I}_i(\rho)}
{\operatorname{Tr}[\mathcal{I}_i(\rho)]}.
\]

### 14.5 Decoherence-Based Measurement

Measurement may be understood as entanglement with an environment producing effective classical records.

### 14.6 Interventional Measurement

Operationally, measurement is an intervention:

\[
P(o\mid \mathrm{do}(I),C).
\]

Thus “measurement” may mean revelation, projection, information update, physical interaction, decoherence process, or intervention.

---

## 15. Semantic Variance and Theory Change

When theories change, meanings change.

This is not merely linguistic.

The term “mass” in Newtonian mechanics is not exactly the same concept as “mass” in special relativity or quantum field theory.

Newtonian mass is additive and invariant under Galilean transformations.

Relativistic mass is replaced by invariant rest mass,

\[
m^2c^2
=
p_\mu p^\mu.
\]

In quantum field theory, mass may be a pole of a propagator:

\[
G(p)
\sim
\frac{1}{p^2+m^2-i\epsilon}.
\]

Thus the same word refers to different theoretical roles.

Semantic Relativity acknowledges this.

It does not imply that communication across theories is impossible. It implies that translation is required.

---

## 16. Semantic Equivalence

Two interpretations \(I\) and \(J\) of a theory \(T\) are semantically equivalent if they yield the same empirical model:

\[
I(T)
\cong
J(T).
\]

More explicitly, for every context \(C\), action \(a\), and outcome \(o\),

\[
P_I(o\mid a,C)
=
P_J(o\mid a,C).
\]

If this holds, the interpretations are empirically indistinguishable.

Their differences may be metaphysical, explanatory, or pragmatic, but not empirical.

Thus:

\[
\boxed{
\text{Semantic equivalence is empirical equivalence under interpretation.}
}
\]

---

## 17. Semantic Invariants

If meanings are relative, what is invariant?

The invariant is the empirical structure preserved under admissible reinterpretations.

Candidate invariants include:

1. probability distributions over outcomes,
2. correlation functions,
3. scattering amplitudes,
4. causal order where operationally accessible,
5. anomaly data,
6. symmetry constraints,
7. topological invariants,
8. entanglement structure,
9. thermodynamic relations,
10. consistency conditions across contexts.

For example, in quantum field theory, correlation functions,

\[
\left\langle
\phi(x_1)\cdots\phi(x_n)
\right\rangle,
\]

are central empirical invariants.

In gauge theory, Wilson loops,

\[
W(C),
\]

are gauge-invariant.

In holography, boundary correlators,

\[
\left\langle
\mathcal{O}_1\cdots\mathcal{O}_n
\right\rangle,
\]

are invariant under bulk-boundary duality.

Thus:

\[
\boxed{
\text{Semantic invariants are the empirical structures that survive reinterpretation.}
}
\]

---

## 18. Gauge Redundancy and Semantic Quotient

Gauge theories reveal that much formal structure is semantically redundant.

A gauge potential \(A_\mu\) and its gauge transform \(A_\mu^g\) represent the same physical state:

\[
A_\mu
\sim
A_\mu^g.
\]

The physical object is the equivalence class,

\[
[A_\mu].
\]

Thus the meaning of \(A_\mu\) is not a direct physical field. It is a representative of a gauge orbit.

Semantic Relativity generalizes this.

Many theoretical terms may be representatives of equivalence classes rather than direct names of reality.

The physical meaning is obtained after quotienting by redundancy:

\[
\text{physical meaning}
=
\text{formal meaning}/\text{redundancy}.
\]

---

## 19. Duality and Semantic Relativity

Dualities are powerful examples of semantic relativity.

Two theories may use different variables, different geometries, and different ontologies, yet yield the same empirical predictions.

For example, in AdS/CFT,

\[
Z_{\text{CFT}}[J]
=
Z_{\text{gravity}}
\left[
\phi\big|_{\partial}=J
\right].
\]

The bulk term “particle” may correspond to a boundary operator excitation.

The bulk term “geometry” may correspond to entanglement structure in the boundary theory.

The bulk term “radial direction” may correspond to renormalization scale.

Thus the meanings of bulk terms are dual-relative.

The invariant is the shared empirical and categorical structure.

---

## 20. Effective Theories and Semantic Domains

Effective field theory shows that meaning is scale-relative.

At energies \(E\ll M\), one writes

\[
\mathcal{L}_{\text{eff}}
=
\mathcal{L}_{\text{ren}}
+
\sum_i
\frac{c_i}{M^{\Delta_i-4}}
\mathcal{O}_i.
\]

The terms in \(\mathcal{L}_{\text{eff}}\) have meaning within the domain of validity.

A field that appears fundamental at one scale may be composite at another.

A particle that appears elementary at low energy may be a bound state at high energy.

A spacetime geometry that appears smooth at large scales may be emergent from microscopic quantum information.

Thus:

\[
\boxed{
\text{Semantic domains are scale-dependent.}
}
\]

---

## 21. Operational Semantics

Semantic Relativity is naturally operational.

The meaning of a term is given by its role in intervention-outcome structures.

For an intervention \(I\), context \(C\), and outcome \(o\), the basic empirical probability is

\[
P(o\mid \mathrm{do}(I),C).
\]

A term has physical meaning if it contributes to the organization of such probabilities.

For example, “electron” means something like:

1. a preparation protocol,
2. a set of detector responses,
3. a representation of the Poincaré group,
4. a field excitation,
5. a stable track in a cloud chamber,
6. a pole in a propagator,
7. a charge and mass pattern in scattering experiments.

No single one of these exhausts the meaning.

The meaning is the network of operational and theoretical roles.

---

## 22. Semantic Relativity and Structural Realism

Semantic Relativity is compatible with structural realism.

Structural realism says that what persists through theory change is not the ontology of objects but the invariant structure of relations.

For example, Fresnel’s optical equations and Maxwell’s electromagnetic theory differ in ontology, but share mathematical structure.

Similarly, different quantum interpretations may differ in ontology but share Hilbert-space structure and Born-rule probabilities.

Thus:

\[
\boxed{
\text{Reality is captured by invariant structure, not by fixed vocabulary.}
}
\]

Semantic Relativity is the semantic counterpart of structural realism.

---

## 23. Semantic Relativity Is Not Relativism

Semantic Relativity must be distinguished from semantic relativism.

Relativism says:

\[
\text{All meanings or truths are equally valid.}
\]

Semantic Relativity says:

\[
\text{Meanings are theory-relative, but empirical adequacy and invariant structure are not arbitrary.}
\]

An interpretation is admissible only if it satisfies constraints such as:

1. empirical adequacy,
2. internal consistency,
3. composability,
4. covariance,
5. stability under refinement,
6. agreement with established limits,
7. predictive power,
8. explanatory coherence.

Thus not every interpretation is acceptable.

The relativity of meaning is constrained by the absoluteness of empirical structure.

---

## 24. The Measurement Problem as Semantic Tension

The quantum measurement problem is partly a semantic problem.

The term “measurement” is used in multiple incompatible ways:

1. as ordinary physical interaction,
2. as special collapse process,
3. as information update,
4. as branching,
5. as decoherence,
6. as intervention,
7. as primitive event.

Different interpretations resolve the tension differently.

Collapse theories modify the dynamics.

Everettian theories remove collapse and interpret branching.

Bohmian theories add hidden variables.

QBism interprets the quantum state as personal belief.

Relational quantum mechanics interprets facts as relative to systems.

Decoherence explains effective classicality but not unique outcomes by itself.

Semantic Relativity clarifies the landscape:

\[
\boxed{
\text{Many measurement puzzles arise because one vocabulary is forced to serve multiple theoretical roles.}
}
\]

---

## 25. Semantic Relativity in Quantum Gravity

Quantum gravity intensifies semantic relativity.

Terms such as “spacetime,” “point,” “geometry,” “locality,” and “time” may lose their ordinary meanings.

In causal-set theory, spacetime points are replaced by causal elements.

In loop quantum gravity, geometry is quantized into spin-network states.

In string theory, particles are string modes and geometry may be dual to gauge theory.

In holography, bulk spacetime is reconstructed from boundary entanglement.

In group field theory, spacetime may emerge from combinatorial structures.

Thus the vocabulary of general relativity may be effective rather than fundamental.

Semantic Relativity demands humility:

\[
\boxed{
\text{The terms of our current best theory may be placeholders for deeper structures.}
}
\]

---

## 26. Formal Semantic Equivalence

Let \(T\) and \(T'\) be theories.

Let \(I\) and \(I'\) be interpretations into empirical models.

Define empirical equivalence by

\[
T
\sim_{\text{emp}}
T'
\]

if there exists an isomorphism

\[
\eta:
I(T)
\rightarrow
I'(T')
\]

preserving all intervention-outcome probabilities:

\[
P_T(o\mid a,C)
=
P_{T'}(\eta(o)\mid \eta(a),\eta(C)).
\]

The physical content of a theory is then the equivalence class,

\[
[T]_{\text{emp}}.
\]

Semantic Relativity says that vocabulary belongs to representatives, while physical content belongs to equivalence classes.

---

## 27. Natural Transformations and Interpretive Equivalence

If two interpretations \(I\) and \(J\) of the same theory \(T\) are related by a natural transformation,

\[
\eta:
I
\Rightarrow
J,
\]

then for every theory morphism \(f:T\to T'\), the diagram commutes:

\[
J(f)\circ\eta_T
=
\eta_{T'}\circ I(f).
\]

This means the reinterpretation is coherent across the whole theoretical structure.

Thus semantic equivalence is not piecemeal. It is structural.

---

## 28. Semantic Layers in Physics

Physical language operates at several semantic layers.

### 28.1 Mathematical Layer

Symbols and equations.

### 28.2 Model Layer

Structured mathematical objects satisfying equations.

### 28.3 Operational Layer

Preparations, transformations, measurements, interventions.

### 28.4 Phenomenological Layer

Observed patterns, tracks, clicks, images, spectra.

### 28.5 Ontological Layer

Claims about what exists.

Semantic Relativity says that confusion arises when one layer is mistaken for another.

A wavefunction may be mathematical, operational, and ontological in different interpretations.

A coordinate may be mathematical but not ontological.

A gauge potential may be mathematically useful but physically redundant.

A particle may be phenomenologically real but ontologically emergent.

---

## 29. Semantic Invariance and Objectivity

Objectivity is not the absence of interpretation.

Objectivity is invariance under admissible interpretations.

A fact is objective to the degree that it is stable across:

1. observers,
2. instruments,
3. coordinate systems,
4. gauge choices,
5. dual descriptions,
6. coarse-grainings,
7. theoretical formulations.

Thus:

\[
\boxed{
\text{Objectivity is intersubjective and inter-theoretic invariance.}
}
\]

Semantic Relativity does not destroy objectivity. It refines it.

---

## 30. Axioms of Semantic Relativity

The framework may be organized around twelve axioms.

### Axiom 1: Terms Have Theory-Relative Meaning

Physical terms acquire meaning within a theory-model-context structure.

### Axiom 2: Interpretation Is Functorial

Interpretations map theories to empirical models while preserving structure.

### Axiom 3: Formalism Underdetermines Interpretation

The same formalism may admit multiple interpretations.

### Axiom 4: Different Formalisms May Be Empirically Equivalent

Distinct mathematical structures may yield the same empirical model.

### Axiom 5: Meaning Is Operational

Meaning is tied to interventions, contexts, and outcomes.

### Axiom 6: Redundancy Must Be Quotiented

Gauge, coordinate, and dual redundancies are not physical meaning.

### Axiom 7: Scale Determines Semantic Domain

Terms may change meaning across scales and effective theories.

### Axiom 8: Invariant Empirical Structure Is Physical

What survives admissible reinterpretation is physical content.

### Axiom 9: Vocabulary Is Not Reality

Words and symbols are representatives, not the world itself.

### Axiom 10: Semantic Equivalence Is Empirical Equivalence

Interpretations with identical empirical models are semantically equivalent physically.

### Axiom 11: Semantic Relativity Is Not Relativism

Meaning is constrained by consistency, empirical adequacy, and invariance.

### Axiom 12: Theory Change Requires Semantic Translation

Conceptual progress often requires reinterpreting old terms in new structures.

---

## 31. Relation to Previous Versions of Relativity

Semantic Relativity connects to earlier versions.

| Version | Relation |
|---|---|
| Special Relativity | Simultaneity terms are frame-relative |
| General Relativity | Coordinates and events are relationally defined |
| Quantum Reference Frames | Observers are physical systems |
| Contextuality Relativity | Properties are context-relative |
| Probability / Measure Relativity | Probabilities are measure-relative |
| Nomological Relativity | Laws may be effective and domain-relative |
| Identity Relativity | Objects are equivalence classes of structure |
| Boundary / Nothingness Relativity | Boundaries are description-relative |
| Meta-Relativity | Descriptions themselves are relative |
| Semantic Relativity | Meaning itself is theory- and model-relative |

The progression is:

\[
\text{relative motion}
\rightarrow
\text{relative geometry}
\rightarrow
\text{relative frames}
\rightarrow
\text{relative properties}
\rightarrow
\text{relative laws}
\rightarrow
\text{relative identity}
\rightarrow
\text{relative boundaries}
\rightarrow
\text{relative meaning}.
\]

---

## 32. Experimental and Practical Relevance

Semantic Relativity is not merely philosophical.

It matters in practice.

### 32.1 Quantum Information

Operational definitions of states, channels, measurements, and entanglement are essential.

### 32.2 Gauge Theory

Recognizing gauge redundancy prevents mistaking gauge-dependent quantities for observables.

### 32.3 Quantum Gravity

Semantic humility prevents reifying semiclassical spacetime terms beyond their domain.

### 32.4 Cosmology

Terms such as “universe,” “observer,” and “beginning” require careful interpretation.

### 32.5 Experimental Design

Measurements must be defined by interventions and calibration protocols.

### 32.6 Theory Comparison

Dualities and effective theories require careful semantic translation.

Thus Semantic Relativity is a practical discipline of conceptual hygiene.

---

## 33. Open Problems

Several major problems remain.

### 33.1 Formalizing Meaning

A fully rigorous theory of physical meaning remains incomplete.

### 33.2 Interpretive Equivalence

When are two interpretations truly equivalent rather than merely similar?

### 33.3 Semantic Holism

Do terms acquire meaning only from the whole theory?

### 33.4 Quantum Gravity Vocabulary

What do “space,” “time,” and “event” mean in a pre-geometric theory?

### 33.5 Consciousness and Observation

How should first-person observation be incorporated without confusion?

### 33.6 Underdetermination

How should one choose between empirically equivalent interpretations?

### 33.7 Semantic Evolution

How do meanings stabilize across scientific revolutions?

### 33.8 Artificial Modeling

How should machine-learning models represent theory-relative meaning without reification?

---

## 34. What Einstein Would Think

Einstein would appreciate Semantic Relativity.

His own work was deeply semantic.

He asked:

\[
\text{What do we mean by simultaneity?}
\]

He answered operationally: simultaneity is defined by synchronization procedures using light signals.

He did not merely revise equations. He revised meaning.

General relativity similarly revised the meaning of coordinates, geometry, and inertia.

Einstein would therefore recognize the central lesson:

\[
\boxed{
\text{Physical concepts must be tied to operations, invariants, and empirical structure.}
}
\]

However, Einstein was a realist. He would resist the idea that meaning is all there is.

Semantic Relativity need not deny realism. It says that realism must be directed toward invariant structure, not toward contingent vocabulary.

Einstein might accept this as a mature form of physical realism.

---

## 35. Summary of Core Structures

### Interpretation functor

\[
I:
\mathbf{Theory}
\rightarrow
\mathbf{EmpiricalModel}.
\]

### Empirical probability

\[
P(o\mid a,C).
\]

### Empirical equivalence

\[
I(T)
\cong
I(T').
\]

### Physical content as equivalence class

\[
[T]_{\text{emp}}.
\]

### Gauge quotient

\[
[A_\mu].
\]

### Effective Lagrangian

\[
\mathcal{L}_{\text{eff}}
=
\mathcal{L}_{\text{ren}}
+
\sum_i
\frac{c_i}{M^{\Delta_i-4}}
\mathcal{O}_i.
\]

### Born rule

\[
P(i)
=
\operatorname{Tr}(\rho E_i).
\]

### Intervention probability

\[
P(o\mid \mathrm{do}(I),C)
=
\operatorname{Tr}
\left[
E_o\mathcal{I}_I(\rho)
\right].
\]

### Central principle

\[
\boxed{
\text{Physical meaning is model-relative, but invariant empirical structure is physical.}
}
\]

---

## 36. Conclusion

Relativity 35.0, Semantic Relativity, asserts that the meaning of physical terms is not absolute.

“Particle,” “field,” “event,” “observer,” “vacuum,” “time,” and “measurement” do not have fixed meanings across all theories. Their meanings are determined by formal structure, operational role, scale, context, and interpretation.

The central formal object is the interpretation functor,

\[
I:
\mathbf{Theory}
\rightarrow
\mathbf{EmpiricalModel}.
\]

The central principle is:

\[
\boxed{
\text{Physical meaning is model-relative, but invariant empirical structure is physical.}
}
\]

Semantic Relativity prevents us from mistaking the vocabulary of one description for reality itself.

It teaches that words are not things, equations are not ontology, and formal symbols are not final entities.

Reality is not captured by a privileged dictionary. It is captured by the invariant structure that survives all admissible translations, dualities, gauge quotients, coarse-grainings, and reinterpretations.

This is Semantic Relativity.

---

## Appendix A: Functorial Interpretation

Let \(\mathbf{Theory}\) have theories as objects and theory translations as morphisms.

Let \(\mathbf{EmpiricalModel}\) have empirical models as objects and empirical transformations as morphisms.

An interpretation is a functor,

\[
I:
\mathbf{Theory}
\rightarrow
\mathbf{EmpiricalModel}.
\]

For a morphism \(f:T\to T'\),

\[
I(f):I(T)\to I(T').
\]

Functoriality requires

\[
I(g\circ f)
=
I(g)\circ I(f),
\]

and

\[
I(\mathrm{id}_T)
=
\mathrm{id}_{I(T)}.
\]

Thus interpretation preserves theoretical structure in empirical structure.

---

## Appendix B: Empirical Equivalence

Two interpreted theories \(I(T)\) and \(I'(T')\) are empirically equivalent if there exists an isomorphism

\[
\eta:I(T)\to I'(T')
\]

such that for all contexts \(C\), actions \(a\), and outcomes \(o\),

\[
P_T(o\mid a,C)
=
P_{T'}(\eta(o)\mid \eta(a),\eta(C)).
\]

The physical content is the equivalence class,

\[
[T]_{\text{emp}}.
\]

---

## Appendix C: Particle as Poincaré Representation

In relativistic quantum theory, one-particle states transform under unitary representations of the Poincaré group.

The Casimir invariants are

\[
P_\mu P^\mu
=
m^2c^2,
\]

and

\[
W_\mu W^\mu
=
-m^2c^2s(s+1)\hbar^2.
\]

Thus “particle” means an irreducible representation labeled by mass and spin.

---

## Appendix D: Observer-Relative Vacuum

For a field expansion in modes \(u_k\),

\[
\phi
=
\sum_k
\left(
a_k u_k
+
a_k^\dagger u_k^*
\right),
\]

the vacuum satisfies

\[
a_k\ket{0}=0.
\]

A different mode expansion \(v_j\) gives different operators \(b_j\), related by Bogoliubov transformations:

\[
b_j
=
\sum_k
\left(
\alpha_{jk}a_k
+
\beta_{jk}a_k^\dagger
\right).
\]

If \(\beta_{jk}\neq 0\), then

\[
b_j\ket{0_a}
\neq
0.
\]

Thus the vacuum of one observer may contain particles for another.

---

## Appendix E: Measurement as Instrument

A quantum instrument is a set of completely positive maps

\[
\{\mathcal{I}_i\},
\]

such that

\[
\sum_i \mathcal{I}_i
\]

is trace-preserving.

The probability of outcome \(i\) is

\[
P(i)
=
\operatorname{Tr}
\left[
\mathcal{I}_i(\rho)
\right].
\]

The post-measurement state is

\[
\rho_i
=
\frac{\mathcal{I}_i(\rho)}
{\operatorname{Tr}[\mathcal{I}_i(\rho)]}.
\]

Thus “measurement” is not a primitive word but an operational structure.

---

## Selected References

1. A. Einstein, “On the Electrodynamics of Moving Bodies,” *Annalen der Physik* **17**, 891 (1905).  
2. A. Einstein, “The Foundation of the General Theory of Relativity,” *Annalen der Physik* **49**, 769 (1916).  
3. P. W. Bridgman, *The Logic of Modern Physics* (Macmillan, 1927).  
4. R. Carnap, *The Logical Syntax of Language* (Routledge, 1937).  
5. T. S. Kuhn, *The Structure of Scientific Revolutions* (University of Chicago Press, 1962).  
6. P. Feyerabend, “Explanation, Reduction, and Empiricism,” in *Minnesota Studies in the Philosophy of Science* (1962).  
7. P. Suppes, “A Comparison of the Meaning and Uses of Models in Mathematics and the Empirical Sciences,” *Synthese* **12**, 287 (1960).  
8. B. C. van Fraassen, *The Scientific Image* (Oxford University Press, 1980).  
9. E. P. Wigner, “On Unitary Representations of the Inhomogeneous Lorentz Group,” *Annals of Mathematics* **40**, 149 (1939).  
10. W. G. Unruh, “Notes on Black-Hole Evaporation,” *Physical Review D* **14**, 870 (1976).  
11. R. M. Wald, *Quantum Field Theory in Curved Spacetime and Black Hole Thermodynamics* (University of Chicago Press, 1994).  
12. C. Rovelli, “Relational Quantum Mechanics,” *International Journal of Theoretical Physics* **35**, 1637 (1996).  
13. Č. Brukner and A. Zeilinger, “Operationally Invariant Measure of the Distance between Quantum States,” *Physical Review A* **63**, 022113 (2001).  
14. R. W. Spekkens, “Evidence for the Epistemic View of Quantum States: A Toy Theory,” *Physical Review A* **75**, 032110 (2007).  
15. H. Halvorson, “What Scientific Theories Could Not Be,” *Philosophy of Science* **79**, 183 (2012).  
16. J. Ladyman, “Structural Realism,” *Stanford Encyclopedia of Philosophy* (2020 edition).  
17. S. Weinberg, *The Quantum Theory of Fields*, Vols. 1–3 (Cambridge University Press, 1995–2000).  
18. J. M. Maldacena, “The Large \(N\) Limit of Superconformal Field Theories and Supergravity,” *Advances in Theoretical and Mathematical Physics* **2**, 231 (1998).  
19. D. Wallace, *The Emergent Multiverse* (Oxford University Press, 2012).  
20. C. A. Fuchs, N. D. Mermin, and R. Schack, “An Introduction to QBism with an Application to the Locality of Quantum Mechanics,” *American Journal of Physics* **82**, 749 (2014).  
21. G. C. Ghirardi, A. Rimini, and T. Weber, “Unified Dynamics for Microscopic and Macroscopic Systems,” *Physical Review D* **34**, 470 (1986).  
22. D. Bohm, “A Suggested Interpretation of the Quantum Theory in Terms of Hidden Variables,” *Physical Review* **85**, 166 (1952).  
23. H. Weyl, *The Theory of Groups and Quantum Mechanics* (Dover, 1931).  
24. S. Weinberg, “Effective Field Theory, Past and Future,” *International Journal of Modern Physics A* **31**, 1630007 (2016).  
25. J. D. Norton, “Are We at the Dawn of a New Revolution in the Philosophy of Science?” *Philosophy of Science* (various works on semantic view and relativity).
