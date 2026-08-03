# Relativity 51.0 — Emergent-Level Relativity  
## Laws, Variables, and Causality as Level-Relative Frames

**White paper / academic preprint**

---

## Abstract

Emergent-Level Relativity is the hypothesis that laws, variables, and causal descriptions are relative to organizational level. A microphysical description and a macrophysical description may both be valid, but neither is absolutely privileged. Let \(C\) be a coarse-graining map from microstates to macrostates,

\[
C:
\Gamma_{\text{micro}}
\rightarrow
\Gamma_{\text{macro}}.
\]

Effective macroscopic dynamics \(T_{\text{macro}}\) are valid when they approximately commute with coarse-graining:

\[
T_{\text{macro}}C
\approx
CT_{\text{micro}}.
\]

The central principle is:

\[
\boxed{
\text{Laws are level-relative; consistency across levels is the invariant.}
}
\]

Chemistry is not “less real” than particle physics. Biology is not “less real” than chemistry. Economics, psychology, ecology, and computation are not mere metaphors imposed on matter. Each organizational level possesses its own valid variables, regularities, interventions, and causal descriptions. Emergent-Level Relativity does not deny microphysics. It denies micro-absolutism. The invariant physical content is not the law of one level, but the web of consistent relations among levels.

---

## 1. Introduction

Physics has often been tempted by a single-level ontology.

Atoms are real; tables are approximations.

Fields are real; particles are emergent.

Quantum states are real; classical trajectories are illusions.

Microphysics is real; everything else is derivative.

Emergent-Level Relativity rejects this hierarchy of reality.

It does not say that higher levels float free of lower levels.

It says that levels are frames of description.

Each level has:

1. its own variables,
2. its own laws,
3. its own stable patterns,
4. its own interventions,
5. its own causal descriptions,
6. its own domain of validity.

A gas molecule is not more real than pressure.

A neuron is not more real than cognition.

A quark is not more real than a cell.

Each is real within a level-frame.

The relation between levels is not reduction to one privileged description.

It is constrained consistency across frames.

Thus:

\[
\boxed{
\text{Levels are not layers of reality ranked by truth. They are frames of effective description.}
}
\]

---

## 2. Levels as Frames

A level of organization may be represented as a frame,

\[
L
=
\left(
\Gamma_L,
\mathcal{V}_L,
\mathcal{D}_L,
\mathcal{I}_L,
\mathcal{O}_L
\right),
\]

where:

- \(\Gamma_L\) is the state space of the level,
- \(\mathcal{V}_L\) is its variable set,
- \(\mathcal{D}_L\) is its dynamics or law structure,
- \(\mathcal{I}_L\) is its set of interventions,
- \(\mathcal{O}_L\) is its observable algebra.

Examples include:

1. particle physics,
2. nuclear physics,
3. atomic physics,
4. chemistry,
5. molecular biology,
6. cell biology,
7. physiology,
8. neuroscience,
9. psychology,
10. ecology,
11. economics,
12. computation,
13. engineering.

Each level is not a fiction.

It is a stable frame in which certain variables are accessible, controllable, and lawlike.

Thus:

\[
\boxed{
\text{An organizational level is a physical frame of description.}
}
\]

---

## 3. Coarse-Graining and Level Relations

Let the microphysical state space be

\[
\Gamma_{\text{micro}}.
\]

Let the macrophysical state space be

\[
\Gamma_{\text{macro}}.
\]

A coarse-graining map,

\[
C:
\Gamma_{\text{micro}}
\rightarrow
\Gamma_{\text{macro}},
\]

assigns each microstate to a macrostate.

For a microstate \(x\),

\[
M
=
C(x).
\]

The preimage of a macrostate is the set of microstates compatible with it:

\[
C^{-1}(M)
=
\{x\in\Gamma_{\text{micro}}\mid C(x)=M\}.
\]

Macroscopic variables are usually functions on macrostates or conditional expectations over microstates.

For a micro-observable \(A\), the corresponding macro-variable may be

\[
A_{\text{macro}}(M)
=
\mathbb{E}
[
A
\mid
C(x)=M
].
\]

Thus macroscopic variables are not arbitrary.

They are stable averages, typical values, or collective coordinates over microstates.

---

## 4. Effective Dynamics and Approximate Commutation

Let the microdynamics be

\[
T_{\text{micro}}:
\Gamma_{\text{micro}}
\rightarrow
\Gamma_{\text{micro}}.
\]

Let the macrodynamics be

\[
T_{\text{macro}}:
\Gamma_{\text{macro}}
\rightarrow
\Gamma_{\text{macro}}.
\]

The macrodynamics is valid when it approximately commutes with coarse-graining:

\[
T_{\text{macro}}C
\approx
CT_{\text{micro}}.
\]

Diagrammatically:

\[
\begin{array}{ccc}
\Gamma_{\text{micro}}
&
\xrightarrow{T_{\text{micro}}}
&
\Gamma_{\text{micro}}
\\
\downarrow C
&
&
\downarrow C
\\
\Gamma_{\text{macro}}
&
\xrightarrow{T_{\text{macro}}}
&
\Gamma_{\text{macro}}
\end{array}
\]

If the diagram approximately commutes for the relevant class of states, then the macroscopic law is autonomous.

This is the mathematical condition for emergence.

Thus:

\[
\boxed{
\text{A higher-level law is valid when coarse-graining and dynamics approximately commute.}
}
\]

---

## 5. Why Exact Commutation Is Rare

Exact commutation is rare because microscopic dynamics contains far more information than macroscopic dynamics preserves.

Microstates contain:

1. microscopic phases,
2. correlations,
3. fluctuations,
4. irrelevant degrees of freedom,
5. microscopic noise,
6. detailed boundary conditions.

Macrostates discard most of this.

Therefore macroscopic laws are usually:

1. approximate,
2. stochastic,
3. dissipative,
4. irreversible,
5. domain-limited,
6. robust under microvariation.

This does not make them unreal.

It makes them effective.

---

## 6. Probability, Entropy, and Coarse-Graining

Coarse-graining naturally introduces entropy.

If a macrostate \(M\) corresponds to many microstates, its Boltzmann entropy is

\[
S(M)
=
k_{\text{B}}
\ln
|C^{-1}(M)|.
\]

In probabilistic form, for a distribution \(p(x)\),

\[
S[p]
=
- k_{\text{B}}
\sum_x p(x)\ln p(x).
\]

Coarse-graining loses information.

The macrostate distribution is

\[
P(M)
=
\sum_{x\in C^{-1}(M)}
p(x).
\]

The information lost is

\[
I_{\text{lost}}
=
S[P]
-
S[p]
\geq
0,
\]

under appropriate conditions.

Thus higher-level descriptions are informationally compressed.

But compression does not mean unreality.

It means level-relative abstraction.

---

## 7. Irreversibility as Level-Relative Law

Microscopic laws are often reversible.

Classical Hamiltonian dynamics satisfies

\[
T_{\text{micro}}^{-1}
\]

exists.

Quantum unitary dynamics satisfies

\[
U^{-1}
=
U^\dagger.
\]

But macroscopic laws are often irreversible:

\[
\frac{\partial u}{\partial t}
=
D\nabla^2 u,
\]

\[
\frac{dS}{dt}
\geq
0.
\]

This is not a contradiction.

Irreversibility is level-relative.

It emerges because coarse-graining discards microscopic correlations.

The second law is not an absolute microscopic law.

It is a robust macroscopic law valid for typical microstates under coarse-graining.

Thus:

\[
\boxed{
\text{Irreversibility is an emergent-level invariant.}
}
\]

---

## 8. Statistical Mechanics as Emergent-Level Relativity

Statistical mechanics provides the paradigm.

Microlevel:

\[
x
=
(q_i,p_i)_{i=1}^N.
\]

Macrolevel variables:

\[
T,
\quad
P,
\quad
V,
\quad
S,
\quad
U.
\]

The coarse-graining map assigns microstates to thermodynamic macrostates.

The microdynamics is Hamiltonian:

\[
\dot q_i
=
\frac{\partial H}{\partial p_i},
\]

\[
\dot p_i
=
-
\frac{\partial H}{\partial q_i}.
\]

The macrodynamics is thermodynamic:

\[
dU
=
T dS
-
P dV
+
\mu dN.
\]

Neither level is absolutely privileged.

Microphysics explains the conditions of validity of thermodynamics.

Thermodynamics describes robust regularities invisible at the microlevel.

Temperature is not a property of a single microstate in the same way as position.

But temperature is physically real at the macrolevel.

---

## 9. Hydrodynamics as an Effective Level

Hydrodynamics is another emergent level.

The variables are coarse-grained densities:

\[
\rho(x,t),
\quad
u(x,t),
\quad
T(x,t).
\]

The equations are conservation laws:

\[
\partial_t \rho
+
\nabla\cdot(\rho u)
=
0,
\]

\[
\partial_t(\rho u)
+
\nabla\cdot(\rho u\otimes u + P)
=
0,
\]

\[
\partial_t e
+
\nabla\cdot((e+P)u)
=
0.
\]

These equations are not fundamental microscopic laws.

They are universal long-wavelength laws constrained by conservation laws and symmetry.

They are valid when gradients are small compared with microscopic scales.

Thus hydrodynamics is level-relative.

But it is not optional.

For fluids, it is often the only efficient and stable description.

---

## 10. Chemistry as an Autonomous Level

Chemistry emerges from quantum mechanics but is not erased by it.

The Born–Oppenheimer approximation separates electronic and nuclear motion.

The molecular Hamiltonian is approximately separated:

\[
H
=
T_{\text{nuc}}
+
H_{\text{el}}(r;R).
\]

For fixed nuclear positions \(R\), one solves the electronic Schrödinger equation,

\[
H_{\text{el}}(r;R)
\psi_{\text{el}}(r;R)
=
E_{\text{el}}(R)
\psi_{\text{el}}(r;R).
\]

The electronic energy \(E_{\text{el}}(R)\) defines a potential-energy surface for nuclear motion.

Chemical concepts such as:

1. bonds,
2. orbitals,
3. valence,
4. reaction pathways,
5. functional groups,
6. acidity,
7. catalysis,

are not fundamental particle-physics terms.

They are level-relative structures.

But they are physically real within the chemical level.

Thus:

\[
\boxed{
\text{Chemistry is not less real than quantum mechanics. It is a different valid frame.}
}
\]

---

## 11. Biology as an Autonomous Level

Biology is even richer.

Biological variables include:

1. genes,
2. cells,
3. organisms,
4. populations,
5. species,
6. ecosystems,
7. metabolic networks,
8. developmental pathways,
9. behavioral strategies.

These are not fundamental physics variables.

But they support robust laws, regularities, and interventions.

Population genetics, for example, uses equations such as

\[
\dot p_i
=
p_i(f_i-\bar f)
+
\text{mutation}
+
\text{migration}.
\]

Natural selection is not a metaphor.

It is a level-relative causal process.

It supervenes on molecular biology, but it is not eliminated by it.

Thus:

\[
\boxed{
\text{Biology is not less real than chemistry. It is an autonomous organizational level.}
}
\]

---

## 12. Computation as a Level

Computation provides a particularly clear example.

A physical computer may be implemented in:

1. silicon,
2. vacuum tubes,
3. DNA,
4. optics,
5. superconducting circuits,
6. mechanical gears,
7. biological neurons.

The same algorithm can be multiply realized.

The software level has variables such as:

1. data structures,
2. functions,
3. memory addresses,
4. control flow,
5. errors,
6. inputs and outputs.

These are not fundamental hardware variables.

But they are causally and explanatorily indispensable.

A software bug is real.

A memory leak is real.

An algorithmic complexity bound is real.

Thus:

\[
\boxed{
\text{Computational level is a genuine emergent level.}
}
\]

---

## 13. Renormalization and Level Relativity

The renormalization group provides a mathematical theory of level relations.

Under scale transformations, microscopic couplings flow:

\[
\frac{dg_i}{d\ln\mu}
=
\beta_i(g).
\]

At large scales, many microscopic details become irrelevant.

Different microscopic theories flow to the same universality class.

The macroscopic laws depend only on:

1. dimension,
2. symmetries,
3. conservation laws,
4. relevant operators.

Thus macroscopic laws are autonomous.

They are not arbitrary.

They are universal consequences of level structure.

Thus:

\[
\boxed{
\text{Universality is the invariant signature of emergent-level relativity.}
}
\]

---

## 14. Causality Across Levels

A common objection is:

\[
\text{If microphysics is causally complete, how can higher levels be causal?}
\]

Emergent-Level Relativity answers that causality itself is level-relative.

At the microlevel, causality is described by microscopic interactions.

At the macrolevel, causality is described by interventions on macrovariables.

Let \(M\) be a macrovariable and \(Y\) an outcome.

The macro-causal effect is

\[
P(Y\mid \mathrm{do}_{\text{macro}}(M=m)).
\]

This is realized by many possible micro-interventions.

If the effect is stable across the realization class,

\[
C^{-1}(M=m),
\]

then the macro-causal description is robust.

Thus macro-causation is not a violation of micro-causation.

It is a stable pattern of micro-causal structure under coarse-graining.

Thus:

\[
\boxed{
\text{Higher-level causes are robust intervention invariants across microrealizers.}
}
\]

---

## 15. Downward Causation Without Contradiction

The phrase “downward causation” is often misleading.

It can suggest that higher levels inject new microscopic forces.

Emergent-Level Relativity does not require this.

What it requires is that higher-level variables organize, constrain, and select microdynamics.

For example:

1. A cell membrane constrains molecular flux.
2. An organism’s behavior selects environmental interactions.
3. An institution constrains individual actions.
4. A computer architecture constrains transistor switching.
5. A developmental pathway constrains gene expression.

These are not magical forces.

They are boundary conditions, constraints, and control structures at higher organizational levels.

Thus:

\[
\boxed{
\text{Downward causation is level-relative constraint, not microphysical violation.}
}
\]

---

## 16. Multiple Realizability

Higher-level structures are often multiply realizable.

The same functional pattern can be realized by different microphysical substrates.

Examples include:

1. computation in different hardware,
2. flight in birds, bats, and aircraft,
3. replication in DNA and potential artificial polymers,
4. memory in neurons and silicon,
5. thermodynamic behavior in many molecular systems.

Multiple realizability shows that higher-level laws are not tied to one microphysical implementation.

They are autonomous relational patterns.

Thus:

\[
\boxed{
\text{Multiple realizability is evidence of level-relative law.}
}
\]

---

## 17. The Invariant: Cross-Level Consistency

If laws are level-relative, what is invariant?

The invariant is consistency across levels.

This includes:

1. approximate commutation of dynamics and coarse-graining,
2. conservation-law compatibility,
3. thermodynamic consistency,
4. causal stability under interventions,
5. universality under renormalization,
6. empirical agreement across measurements,
7. computational simulability where feasible,
8. robustness under microvariation.

Thus:

\[
\boxed{
\text{The invariant is not one level’s law. It is the coherence of the level structure.}
}
\]

---

## 18. Levels Are Not Absolute

Levels are not perfectly sharp.

There is no universal boundary between:

1. chemistry and biology,
2. biology and psychology,
3. physics and chemistry,
4. hardware and software,
5. individual and collective.

Levels are effective partitions.

They are chosen by:

1. scale,
2. stability,
3. control,
4. observability,
5. intervention,
6. explanatory power.

Thus levels are not Platonic strata.

They are pragmatic, physical, and mathematically constrained frames.

---

## 19. Reduction Without Elimination

Emergent-Level Relativity supports a non-eliminative view of reduction.

Reduction is not replacement.

It is the establishment of consistency relations.

A higher-level theory is reduced in the weak sense when its domain of validity is explained by lower-level structure.

But it is not eliminated.

Thermodynamics is not eliminated by statistical mechanics.

Chemistry is not eliminated by quantum mechanics.

Biology is not eliminated by molecular chemistry.

Each remains valid in its own frame.

Thus:

\[
\boxed{
\text{Reduction explains validity conditions; it does not erase levels.}
}
\]

---

## 20. Formal Category-Theoretic View

Let levels be objects in a category of descriptions.

Coarse-graining maps are morphisms:

\[
C_{ij}:
L_i
\rightarrow
L_j.
\]

Dynamics at each level are endomorphisms:

\[
T_i:
L_i
\rightarrow
L_i.
\]

Level consistency requires approximate commutative diagrams:

\[
T_j C_{ij}
\approx
C_{ij} T_i.
\]

The invariant structure is the network of levels connected by these morphisms.

Thus:

\[
\boxed{
\text{Reality is the coherent category of level descriptions.}
}
\]

---

## 21. Emergence as Stability

Emergence is often treated as mysterious.

Emergent-Level Relativity demystifies it.

A pattern is emergent when it is:

1. stable under microvariation,
2. robust under noise,
3. efficiently described at a higher level,
4. causally accessible by level-appropriate interventions,
5. approximately autonomous under its own dynamics.

Thus emergence is not magic.

It is stability under coarse-graining.

---

## 22. Examples of Emergent-Level Laws

### 22.1 Pressure

Pressure is not a property of a single molecule.

But it is real for a gas.

It is defined by momentum flux across surfaces.

It obeys robust laws such as the ideal gas law:

\[
PV
=
Nk_{\text{B}}T.
\]

### 22.2 Temperature

Temperature is not a microscopic coordinate.

But it is real at equilibrium.

It is the parameter conjugate to entropy:

\[
\frac{1}{T}
=
\left(
\frac{\partial S}{\partial U}
\right)_{V,N}.
\]

### 22.3 Viscosity

Viscosity is a transport coefficient emerging from molecular collisions.

It appears in Navier–Stokes equations.

It is not fundamental, but it is measurable and lawlike.

### 22.4 Chemical Bond

A chemical bond is not a fundamental particle.

But it is a stable electronic relational structure.

It explains molecular geometry and reactivity.

### 22.5 Gene

A gene is not a fundamental physical object.

But it is a stable hereditary information unit within biological organization.

### 22.6 Market Price

A market price is not a microscopic variable.

But it is a robust collective variable that coordinates behavior.

---

## 23. Emergent-Level Relativity and Quantum Mechanics

Quantum mechanics introduces special level issues.

The microlevel may be quantum, while the macrolevel is classical.

Decoherence explains how classical variables become stable:

\[
\rho
\rightarrow
\sum_i p_i
\ket{i}\bra{i}.
\]

The environment selects pointer states.

Macroscopic variables become approximately classical.

Thus classical reality is an emergent level.

It is not fundamental.

But it is stable and real.

---

## 24. Emergent-Level Relativity and Biology

Biology challenges simplistic reductionism.

Biological organization involves:

1. self-maintenance,
2. replication,
3. regulation,
4. adaptation,
5. information processing,
6. evolutionary history.

These are not fundamental physics terms.

But they are indispensable biological variables.

The question is not:

\[
\text{Are biological laws reducible to physics?}
\]

The better question is:

\[
\text{Under what conditions are biological level descriptions valid?}
\]

Emergent-Level Relativity answers: when biological variables form stable, intervention-robust, approximately autonomous dynamics.

---

## 25. Emergent-Level Relativity and Mind

Mind and cognition are also level-relative.

Neural variables are real.

Psychological variables are also real.

A belief, memory, intention, or perception is not a fundamental particle.

But it may be a stable pattern of neural, bodily, and environmental relations.

The proper question is not whether mental states are “really” neural states.

The proper question is:

\[
\text{What level-relative descriptions are stable and causally effective?}
\]

This avoids both dualism and crude eliminativism.

---

## 26. Axioms of Emergent-Level Relativity

The framework may be organized around twelve axioms.

### Axiom 1: Levels Are Frames

Organizational levels are frames of description, not absolute layers of being.

### Axiom 2: Variables Are Level-Relative

Variables belong to levels.

### Axiom 3: Laws Are Effective

Laws are valid within domains of stability.

### Axiom 4: Coarse-Graining Defines Level Relations

Levels are related by coarse-graining and refinement maps.

### Axiom 5: Effective Dynamics Requires Approximate Commutation

\[
T_{\text{macro}}C
\approx
CT_{\text{micro}}.
\]

### Axiom 6: Higher Levels Are Not Less Real

Higher-level patterns are real if stable and intervention-robust.

### Axiom 7: Causality Is Level-Relative

Causal descriptions depend on level-appropriate interventions.

### Axiom 8: Multiple Realizability Is Central

The same higher-level pattern may have many lower-level realizers.

### Axiom 9: Reduction Is Consistency, Not Elimination

Lower levels explain validity conditions, not unreality.

### Axiom 10: Invariance Is Cross-Level Coherence

The invariant is consistency across levels.

### Axiom 11: Universality Is Emergent-Level Evidence

Universality classes reveal autonomous macro-laws.

### Axiom 12: Reflexivity Is Required

Level descriptions apply to the observers who use them.

---

## 27. Relation to Previous Relativities

Emergent-Level Relativity integrates earlier versions.

| Relativity | Relativized Structure | Invariant |
|---|---|---|
| General Relativity | Coordinates and geometry | Diffeomorphism-invariant structure |
| Scale Relativity | Resolution | RG-invariant universality |
| Phase Relativity | Effective laws and ontology | Phase diagram and universal data |
| Substance Relativity | Substances | Process-structure |
| Network Relativity | Nodes and adjacency | Relational invariants |
| Pure Relation / Relata Relativity | Objects | Relational fixed points |
| Emergent-Level Relativity | Organizational levels | Cross-level consistency |

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
\text{relative levels}.
\]

---

## 28. Scientific Status

Emergent-Level Relativity is supported by established science.

It is grounded in:

1. statistical mechanics,
2. thermodynamics,
3. hydrodynamics,
4. renormalization-group theory,
5. chemistry,
6. biology,
7. computational theory,
8. complex systems,
9. causal modeling,
10. philosophy of science.

It is not a single empirical theory.

It is a meta-framework for understanding the relation among sciences.

It becomes scientifically powerful when applied to specific level relations with explicit coarse-graining maps, variables, and dynamics.

---

## 29. Open Problems

Several major problems remain.

### 29.1 Exact Level Boundaries

How should levels be objectively partitioned?

### 29.2 Irreversibility

How exactly do irreversible macro-laws emerge from reversible micro-laws?

### 29.3 Downward Causation

How can higher-level constraints be formally represented without overdetermination?

### 29.4 Life and Mind

What are the precise conditions for biological and cognitive level autonomy?

### 29.5 Computational Irreducibility

When can higher-level behavior be efficiently reduced to microsimulation?

### 29.6 Quantum-to-Classical Transition

How do classical level variables emerge from quantum substrates?

### 29.7 Level-Relative Probability

How should probabilities be assigned across levels?

### 29.8 Strong Emergence

Are there level laws that cannot be derived even in principle?

### 29.9 Normative Levels

How do goals, functions, and values fit into level descriptions?

### 29.10 Universal Formalism

Can all levels be represented in a single categorical framework?

---

## 30. What Einstein Would Think

Einstein would be cautious.

He sought unified fundamental laws.

He might resist the idea that biology or psychology possess autonomous laws.

But he would respect the central demand:

\[
\boxed{
\text{Descriptions must be consistent.}
}
\]

Emergent-Level Relativity does not abandon unity.

It redefines unity.

Unity is not one level explaining all others away.

Unity is coherent consistency across levels.

Einstein would recognize this as a form of generalized covariance:

\[
\text{Physical law must be coherent under changes of organizational frame.}
\]

This is the lesson of Emergent-Level Relativity.

---

## 31. Summary of Core Equations

### Coarse-graining map

\[
C:
\Gamma_{\text{micro}}
\rightarrow
\Gamma_{\text{macro}}.
\]

### Macrostate

\[
M
=
C(x).
\]

### Preimage

\[
C^{-1}(M)
=
\{x\mid C(x)=M\}.
\]

### Macro-variable as conditional expectation

\[
A_{\text{macro}}(M)
=
\mathbb{E}
[
A
\mid
C(x)=M
].
\]

### Effective dynamics condition

\[
T_{\text{macro}}C
\approx
CT_{\text{micro}}.
\]

### Boltzmann entropy

\[
S(M)
=
k_{\text{B}}
\ln
|C^{-1}(M)|.
\]

### Renormalization flow

\[
\frac{dg_i}{d\ln\mu}
=
\beta_i(g).
\]

### Macro-causal effect

\[
P(Y\mid \mathrm{do}_{\text{macro}}(M=m)).
\]

### Level frame

\[
L
=
\left(
\Gamma_L,
\mathcal{V}_L,
\mathcal{D}_L,
\mathcal{I}_L,
\mathcal{O}_L
\right).
\]

### Central principle

\[
\boxed{
\text{Laws are level-relative; consistency across levels is the invariant.}
}
\]

---

## 32. Conclusion

Relativity 51.0, Emergent-Level Relativity, asserts that laws, variables, and causal descriptions are relative to organizational level.

Microphysics is not false.

But it is not the only valid frame.

Chemistry is not less real than particle physics.

Biology is not less real than chemistry.

Psychology is not less real than biology.

Computation is not less real than hardware.

Each level is a valid frame when its variables are stable, its dynamics are approximately autonomous, and its interventions are robust.

The central equation is:

\[
T_{\text{macro}}C
\approx
CT_{\text{micro}}.
\]

The central principle is:

\[
\boxed{
\text{Laws are level-relative; consistency across levels is the invariant.}
}
\]

Reality is not a single-layer hierarchy.

It is a coherent structure of levels.

This is Emergent-Level Relativity.

---

## Appendix A: Coarse-Graining Diagram

The microdynamics and macrodynamics are related by:

\[
\begin{array}{ccc}
\Gamma_{\text{micro}}
&
\xrightarrow{T_{\text{micro}}}
&
\Gamma_{\text{micro}}
\\
\downarrow C
&
&
\downarrow C
\\
\Gamma_{\text{macro}}
&
\xrightarrow{T_{\text{macro}}}
&
\Gamma_{\text{macro}}
\end{array}
\]

Approximate commutation means:

\[
T_{\text{macro}}C
\approx
CT_{\text{micro}}.
\]

This is the condition for effective macrodynamics.

---

## Appendix B: Conditional Expectation of Macro-Variables

Given a micro-observable \(A\), its macroscopic value is

\[
A_{\text{macro}}(M)
=
\frac{
\sum_{x\in C^{-1}(M)}
p(x)A(x)
}{
\sum_{x\in C^{-1}(M)}
p(x)
}.
\]

This defines a stable macro-variable when fluctuations are small or controlled.

---

## Appendix C: Entropy of Coarse-Graining

The Boltzmann entropy of a macrostate is

\[
S(M)
=
k_{\text{B}}
\ln
|C^{-1}(M)|.
\]

A macrostate with more compatible microstates has higher entropy.

Thus thermodynamic behavior emerges from counting under coarse-graining.

---

## Appendix D: Renormalization and Universality

Under coarse-graining by scale factor \(b\), couplings transform:

\[
g_i
\rightarrow
g_i'.
\]

The flow is

\[
\frac{dg_i}{d\ln b}
=
\beta_i(g).
\]

Fixed points satisfy

\[
\beta_i(g_*)=0.
\]

Different microscopic systems in the same basin of attraction share universal macroscopic laws.

---

## Appendix E: Macro-Causal Stability

A macro-intervention

\[
\mathrm{do}_{\text{macro}}(M=m)
\]

corresponds to a family of micro-interventions over

\[
C^{-1}(m).
\]

The macro-causal effect is robust if for most microrealizations \(x\in C^{-1}(m)\),

\[
P(Y\mid \mathrm{do}_{\text{micro}}(x))
\approx
P(Y\mid \mathrm{do}_{\text{macro}}(M=m)).
\]

Thus macro-causation is stability across realization classes.

---

## Selected References

1. P. W. Anderson, “More Is Different,” *Science* **177**, 393 (1972).  
2. R. B. Laughlin, *A Different Universe: Reinventing Physics from the Bottom Down* (Basic Books, 2005).  
3. N. Goldenfeld, *Lectures on Phase Transitions and the Renormalization Group* (Addison-Wesley, 1992).  
4. L. P. Kadanoff, “Scaling Laws for Ising Models near \(T_c\),” *Physics* **2**, 263 (1966).  
5. K. G. Wilson, “The Renormalization Group and Critical Phenomena,” *Reviews of Modern Physics* **47**, 773 (1975).  
6. R. Zwanzig, *Nonequilibrium Statistical Mechanics* (Oxford University Press, 2001).  
7. H. Mori, “Transport, Collective Motion, and Brownian Motion,” *Progress of Theoretical Physics* **33**, 423 (1965).  
8. E. T. Jaynes, “Information Theory and Statistical Mechanics,” *Physical Review* **106**, 620 (1957).  
9. E. T. Jaynes, *Probability Theory: The Logic of Science* (Cambridge University Press, 2003).  
10. J. Pearl, *Causality: Models, Reasoning, and Inference* (Cambridge University Press, 2000).  
11. J. Woodward, *Making Things Happen: A Theory of Causal Explanation* (Oxford University Press, 2003).  
12. W. C. Wimsatt, “The Ontology of Complex Systems: Levels, Domains, and Perspectives,” *Canadian Journal of Philosophy* **20**, 207 (1990).  
13. W. C. Wimsatt, *Re-Engineering Philosophy for Limited Beings* (Harvard University Press, 2007).  
14. J. Ladyman and D. Ross, *Every Thing Must Go: Metaphysics Naturalized* (Oxford University Press, 2007).  
15. J. Ladyman, “Structural Realism,” *Stanford Encyclopedia of Philosophy* (2020 edition).  
16. E. Mayr, *What Evolution Is* (Basic Books, 2001).  
17. F. J. Kauffman, *The Origins of Order: Self-Organization and Selection in Evolution* (Oxford University Press, 1993).  
18. D. C. Dennett, *Darwin’s Dangerous Idea* (Simon & Schuster, 1995).  
19. T. Nagel, “What Is It Like to Be a Bat?” *Philosophical Review* **83**, 435 (1974).  
20. H. A. Simon, *The Sciences of the Artificial* (MIT Press, 1969).  
21. R. C. Lewontin, “The Units of Selection,” *Annual Review of Ecology and Systematics* **1**, 1 (1970).  
22. G. G. Simpson, *The Major Features of Evolution* (Columbia University Press, 1953).  
23. C. Craver, *Explaining the Brain: Mechanisms and the Mosaic Unity of Neuroscience* (Oxford University Press, 2007).  
24. W. Bialek, *Biophysics: Searching for Principles* (Princeton University Press, 2012).  
25. S. A. Kauffman, *At Home in the Universe: The Search for Laws of Self-Organization and Complexity* (Oxford University Press, 1995).
