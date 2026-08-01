# Relativity 26.0 — Contextuality Relativity  
## Physical Properties as Context-Relative Invariants

**White paper / academic preprint**

---

## Abstract

Contextuality Relativity is the hypothesis that physical properties are not absolute attributes possessed by systems independently of measurement, but relational facts defined relative to measurement contexts. Quantum contextuality, especially in the Kochen–Specker theorem, demonstrates that one cannot consistently assign pre-existing definite values to all observables in a way independent of the compatible set of observables measured alongside them. The basic probabilistic object is therefore not an unconditional probability \(P(O)\), but a context-conditioned probability,

\[
P(O\mid C),
\]

where \(C\) is a compatible measurement context. Bell nonlocality, Kochen–Specker contextuality, and Spekkens-style generalized contextuality are special cases of a deeper principle:

\[
\boxed{
\text{Properties are context-relative, not system-absolute.}
}
\]

This framework reinterprets measurement context as a physical frame, analogous to a reference frame in relativity. Just as general relativity forbids privileged coordinates, Contextuality Relativity forbids privileged measurement contexts. The invariant content of physics is not a global assignment of values, but the empirical model: the consistent family of context-relative probabilities. Contextuality becomes an obstruction to global valuation, mathematically analogous to curvature or topological nontriviality. This white paper develops the formal structure, physical interpretation, experimental relevance, and foundational consequences of Contextuality Relativity.

---

## 1. Introduction

Classical physics assumes that systems possess properties independently of observation.

A particle has a position. A spin has a component along every axis. A field has a value at every point. Measurement reveals what was already there.

Quantum mechanics challenges this assumption.

A spin-\(\frac{1}{2}\) particle does not possess definite values of \(S_x\), \(S_y\), and \(S_z\) simultaneously. A quantum system may possess a value for an observable only relative to a measurement context in which that observable is compatible with the rest of the measurement.

The Kochen–Specker theorem makes this precise. In Hilbert spaces of dimension three or higher, there is no assignment of definite values to all projection operators that preserves the functional relations required by quantum mechanics and is independent of measurement context.

Thus:

\[
\boxed{
\text{There is no global, context-independent valuation of quantum properties.}
}
\]

Contextuality Relativity elevates this theorem to a relativistic principle.

A measurement context is not an arbitrary experimental detail. It is a frame in which properties become definite. Different contexts define different frames. No context is privileged. Physical reality is the invariant empirical structure that relates all contexts.

---

## 2. Measurement Contexts

A measurement context is a set of jointly measurable observables.

In quantum theory, observables are represented by self-adjoint operators. A set of observables

\[
C=\{A_1,A_2,\ldots,A_n\}
\]

forms a context if they are mutually compatible:

\[
[A_i,A_j]=0
\quad
\forall i,j.
\]

Equivalently, they can be measured jointly without mutual disturbance.

For projective measurements, a context corresponds to a set of commuting projectors

\[
\{P_i\}
\]

satisfying

\[
P_iP_j=\delta_{ij}P_i,
\]

\[
\sum_i P_i=I.
\]

The Born rule gives the probability of outcome \(i\) in context \(C\) as

\[
P(i\mid C)
=
\operatorname{Tr}(\rho P_i).
\]

The context \(C\) is not optional. It defines the set of properties that can be jointly actualized.

---

## 3. Context-Conditioned Probabilities

In classical probability, one writes

\[
P(O),
\]

the probability that observable \(O\) has outcome \(O\).

In Contextuality Relativity, the basic object is

\[
P(O\mid C),
\]

the probability of outcome \(O\) given that \(O\) is measured within context \(C\).

If the same observable \(A\) appears in two different contexts \(C\) and \(C'\), one may have

\[
P(a\mid A,C)
=
P(a\mid A,C'),
\]

but the joint distributions over the full contexts may differ:

\[
P(a,b\mid A,B,C)
\neq
P(a,b'\mid A,B',C').
\]

Thus the observable may have a stable marginal probability, but its correlations with other observables depend on context.

This is the first sign that properties are not absolute.

---

## 4. Noncontextual Hidden-Variable Models

A hidden-variable model attempts to explain quantum probabilities by underlying variables \(\lambda\).

In an ontological model, a preparation \(P\) produces a distribution

\[
\mu_P(\lambda),
\]

and a measurement \(M\) produces outcomes \(k\) with response functions

\[
\xi_M(k\mid\lambda).
\]

The observed probability is

\[
p(k\mid P,M)
=
\int d\lambda\,
\mu_P(\lambda)
\xi_M(k\mid\lambda).
\]

A model is measurement-noncontextual if operationally equivalent measurements are represented by identical response functions.

It is preparation-noncontextual if operationally equivalent preparations are represented by identical distributions.

A fully noncontextual model satisfies:

\[
P\sim P'
\Rightarrow
\mu_P(\lambda)=\mu_{P'}(\lambda),
\]

\[
M\sim M'
\Rightarrow
\xi_M(k\mid\lambda)=\xi_{M'}(k\mid\lambda).
\]

Contextuality means that no such model can reproduce the observed probabilities.

Thus:

\[
\boxed{
\text{Contextuality is the impossibility of a noncontextual ontological explanation.}
}
\]

---

## 5. Kochen–Specker Contextuality

The Kochen–Specker theorem concerns value assignments to quantum observables.

Let \(v(A)\) be a proposed definite value of observable \(A\). A noncontextual valuation satisfies:

1. If \(A\) has eigenvalues \(\{a_i\}\), then

\[
v(A)\in\{a_i\}.
\]

2. If \(A=f(B)\), then

\[
v(A)=f(v(B)).
\]

3. If \(A\) and \(B\) commute, then

\[
v(A+B)=v(A)+v(B),
\]

\[
v(AB)=v(A)v(B).
\]

For projection operators \(P\), this implies

\[
v(P)\in\{0,1\}.
\]

For a complete projective measurement context

\[
\sum_i P_i=I,
\]

one must have

\[
\sum_i v(P_i)=1.
\]

The Kochen–Specker theorem states that in Hilbert space dimension \(d\geq 3\), there exists no assignment

\[
v:
\{\text{projectors}\}
\rightarrow
\{0,1\}
\]

satisfying these conditions for all contexts.

Thus:

\[
\boxed{
\text{Quantum observables cannot possess context-independent definite values.}
}
\]

---

## 6. The Peres–Mermin Square

A particularly elegant proof of contextuality is the Peres–Mermin square.

Consider two qubits. Let \(X,Y,Z\) be Pauli operators. Define the following nine observables:

\[
\begin{array}{ccc}
X\otimes I & I\otimes X & X\otimes X \\
I\otimes Y & Y\otimes I & Y\otimes Y \\
X\otimes Y & Y\otimes X & Z\otimes Z
\end{array}
\]

Each row and each column is a context of mutually commuting observables.

The product of the three observables in each row is \(+I\):

\[
(X\otimes I)(I\otimes X)(X\otimes X)=I,
\]

\[
(I\otimes Y)(Y\otimes I)(Y\otimes Y)=I,
\]

\[
(X\otimes Y)(Y\otimes X)(Z\otimes Z)=I.
\]

The product of the first two columns is also \(+I\):

\[
(X\otimes I)(I\otimes Y)(X\otimes Y)=I,
\]

\[
(I\otimes X)(Y\otimes I)(Y\otimes X)=I.
\]

But the product of the third column is \(-I\):

\[
(X\otimes X)(Y\otimes Y)(Z\otimes Z)=-I.
\]

Suppose a noncontextual value assignment \(v\) existed, with

\[
v(O)\in\{\pm 1\}.
\]

Each observable appears in exactly two contexts. Therefore the product of all six context products must be \(+1\), because every value appears twice:

\[
\prod_{\text{contexts}}
\prod_{O\in C}
v(O)
=
+1.
\]

But the quantum operator products require five contexts to have product \(+1\) and one context to have product \(-1\). Therefore the product of the six context products must be \(-1\).

Contradiction.

Thus no noncontextual assignment exists.

This is a finite, algebraic demonstration of Contextuality Relativity.

---

## 7. Bell Nonlocality as Contextuality

Bell nonlocality is a special case of contextuality in which the contexts are defined by spacelike-separated measurement choices.

Consider two parties, Alice and Bob. Alice chooses setting \(x\), Bob chooses setting \(y\). They obtain outcomes \(a,b\).

The empirical probabilities are

\[
P(a,b\mid x,y).
\]

A local hidden-variable model has the form

\[
P(a,b\mid x,y)
=
\int d\lambda\,
\rho(\lambda)
P(a\mid x,\lambda)
P(b\mid y,\lambda).
\]

This is a noncontextual model in which the response to Alice’s measurement depends only on \(x\) and \(\lambda\), not on Bob’s context \(y\), and vice versa.

The CHSH inequality bounds all such models:

\[
S
=
E_{00}+E_{01}+E_{10}-E_{11}
\leq 2.
\]

Quantum mechanics allows

\[
S
=
2\sqrt{2}.
\]

Thus Bell violation is contextuality: the outcome statistics cannot be explained by a model in which measurement responses are independent of the full measurement context.

In Contextuality Relativity, locality is a special noncontextuality condition:

\[
\boxed{
\text{Bell locality is noncontextuality with respect to spacelike-separated contexts.}
}
\]

---

## 8. Generalized Contextuality

Spekkens generalized contextuality extends the idea beyond projective measurements.

In generalized contextuality, contextuality applies to:

1. preparations,
2. transformations,
3. measurements,
4. POVMs,
5. mixed states,
6. noisy operations.

The central principle is operational equivalence.

If two procedures yield the same statistics for all possible tests, then a noncontextual model must represent them identically.

For preparations:

\[
P\sim P'
\Rightarrow
\mu_P(\lambda)=\mu_{P'}(\lambda).
\]

For measurement effects:

\[
[E_k\mid M]\sim [E_l\mid M']
\Rightarrow
\xi_M(k\mid\lambda)=\xi_{M'}(l\mid\lambda).
\]

Generalized contextuality shows that even qubit systems, which evade Kochen–Specker contextuality for projectors, can exhibit contextuality when preparations and noisy measurements are included.

Thus:

\[
\boxed{
\text{Contextuality is not a peculiarity of high-dimensional projective measurements. It is a general feature of operational theories.}
}
\]

---

## 9. Sheaf-Theoretic Contextuality

Abramsky and Brandenburger gave a powerful mathematical formulation of contextuality using sheaves.

A measurement scenario is a triple

\[
(X,\mathcal{M},O),
\]

where:

- \(X\) is a set of measurements,
- \(\mathcal{M}\) is a collection of compatible subsets \(C\subseteq X\),
- \(O\) is a set of outcomes.

For each context \(C\in\mathcal{M}\), an empirical model assigns a probability distribution

\[
e_C
\in
\operatorname{Prob}(O^C).
\]

These distributions must satisfy compatibility: if \(C'\subseteq C\), then the marginal of \(e_C\) to \(C'\) equals \(e_{C'}\):

\[
e_C|_{C'}
=
e_{C'}.
\]

A deterministic global assignment is a function

\[
g:X\rightarrow O.
\]

A noncontextual hidden-variable model is a probability distribution over such global assignments whose marginals reproduce the empirical distributions:

\[
e_C
=
\sum_{g}
p(g)
\delta_{g|_C}.
\]

Contextuality means that no such global distribution exists.

Strong contextuality means that no deterministic global assignment is even compatible with the support of the empirical model.

Thus:

\[
\boxed{
\text{Contextuality is the failure of local data to glue into a global section.}
}
\]

This is mathematically analogous to the failure of local coordinate charts to define a global section of a nontrivial bundle.

---

## 10. Contextuality as Curvature

Contextuality Relativity suggests a geometric interpretation.

For each context \(C\), let \(F_C\) be the set of possible value assignments within that context.

The collection

\[
\{F_C\}_{C\in\mathcal{M}}
\]

forms a bundle-like structure over the space of contexts.

Compatibility conditions define transition maps between overlapping contexts:

\[
T_{C\to C'}:
F_C
\rightarrow
F_{C'}.
\]

A noncontextual hidden-variable model is a global section:

\[
s(C)\in F_C
\]

such that for all compatible \(C,C'\),

\[
T_{C\to C'}s(C)=s(C').
\]

Contextuality is the obstruction to the existence of such a global section.

This obstruction is analogous to curvature or topological nontriviality.

In the Peres–Mermin square, transporting a value assignment around the loop of contexts produces a sign flip:

\[
T_\gamma v = -v.
\]

The holonomy is nontrivial.

Thus:

\[
\boxed{
\text{Contextuality is the curvature of the bundle of possible properties.}
}
\]

This is the geometric heart of Contextuality Relativity.

---

## 11. Contextuality and Compatibility

Contextuality requires compatibility.

If observables cannot be jointly measured, there is no single context in which their joint properties are defined.

For quantum observables, compatibility is commutativity:

\[
[A,B]=0.
\]

For POVMs, compatibility means the existence of a joint POVM \(G_{ij}\) such that

\[
E_i
=
\sum_j G_{ij},
\]

\[
F_j
=
\sum_i G_{ij}.
\]

Contextuality is not merely incompatibility. It is the impossibility of assigning consistent values across all compatible contexts.

Thus:

\[
\boxed{
\text{Contextuality is not the absence of joint measurability. It is the failure of global valuation across joint measurability structures.}
}
\]

---

## 12. Contextuality Inequalities

Contextuality can be tested through inequalities analogous to Bell inequalities.

### 12.1 KCBS Inequality

The Klyachko–Can–Binicioglu–Shumovsky scenario involves five cyclically exclusive projectors \(P_i\), satisfying

\[
P_iP_{i+1}=0,
\]

with indices modulo 5.

Noncontextual models satisfy

\[
\sum_{i=1}^5
\langle P_i\rangle
\leq 2.
\]

Quantum mechanics allows

\[
\sum_{i=1}^5
\langle P_i\rangle
=
\sqrt{5}.
\]

This violates the noncontextual bound.

### 12.2 Graph-Theoretic Contextuality

Given an exclusivity graph \(G\), vertices represent events and edges represent exclusivity.

The noncontextual bound is the independence number:

\[
\alpha(G).
\]

The quantum bound is the Lovász theta function:

\[
\vartheta(G).
\]

The general no-signaling or generalized probabilistic bound is often the fractional packing number.

For the pentagon graph,

\[
\alpha(C_5)=2,
\]

\[
\vartheta(C_5)=\sqrt{5}.
\]

Thus contextuality is expressed as

\[
\alpha(G)
<
\vartheta(G).
\]

This graph-theoretic formulation reveals contextuality as a structural property of exclusivity relations.

---

## 13. Contextual Fraction

The degree of contextuality can be quantified by the contextual fraction.

An empirical model \(e\) may be decomposed as

\[
e
=
\lambda e_{\text{C}}
+
(1-\lambda)e_{\text{NC}},
\]

where \(e_{\text{C}}\) is contextual and \(e_{\text{NC}}\) is noncontextual.

The contextual fraction is

\[
\operatorname{CF}(e)
=
\min
\left\{
\lambda
\mid
e=\lambda e_{\text{C}}+(1-\lambda)e_{\text{NC}}
\right\}.
\]

If

\[
\operatorname{CF}(e)=0,
\]

the model is noncontextual.

If

\[
\operatorname{CF}(e)=1,
\]

the model is maximally contextual.

This provides a resource-theoretic measure of contextuality.

---

## 14. Contextuality as a Quantum Resource

Contextuality is not merely foundational. It is a resource for quantum information processing.

It has been linked to:

1. magic-state quantum computation,
2. measurement-based quantum computation,
3. quantum randomness certification,
4. quantum cryptography,
5. quantum communication advantages,
6. sub-theories of quantum computation.

In magic-state computation, non-stabilizer states provide the resource needed for universal quantum computation. Many such states exhibit contextuality.

In measurement-based quantum computation, certain computational speedups require contextual correlations.

Thus:

\[
\boxed{
\text{Contextuality is not a defect of quantum theory. It is a computational resource.}
}
\]

---

## 15. Contextuality and Relativity of Frames

Contextuality Relativity interprets measurement contexts as frames.

In special relativity, an inertial frame defines a decomposition of spacetime into space and time.

In quantum theory, a measurement context defines a decomposition of possibility into jointly definite properties.

Just as no inertial frame is privileged, no measurement context is privileged.

A property such as “the value of \(A\)” is not absolute. It is defined relative to a context \(C\) containing \(A\).

Thus:

\[
\boxed{
\text{A measurement context is a quantum frame of properties.}
}
\]

Changing context is analogous to changing reference frame.

The invariant is not the value assigned in one context, but the full empirical model relating all contexts.

---

## 16. Contextuality and Relational Quantum Mechanics

Relational quantum mechanics says that quantum states and facts are relative to systems.

Contextuality Relativity refines this by specifying the role of measurement contexts.

A fact is not merely relative to an observer. It is relative to a compatible set of interventions and records.

If observer \(O\) measures context \(C\), then relative to \(O\),

\[
P(O_C\mid C)
\]

is actualized.

Another observer may measure a different context \(C'\). The two descriptions need not be globally mergeable into a single assignment of all properties.

They are consistent only on their common operational overlaps.

Thus:

\[
\boxed{
\text{Relational facts are contextual facts.}
}
\]

---

## 17. Contextuality and Participatory Relativity

Participatory Relativity says that observation is intervention.

Contextuality Relativity says that every intervention defines a context.

The probability of an outcome is therefore not merely

\[
P(O),
\]

but

\[
P(O\mid \mathrm{do}(I),C),
\]

where \(I\) is an intervention and \(C\) is the compatible context established by that intervention.

Thus participation creates the context in which properties become definite.

---

## 18. Contextuality in Quantum Field Theory

In algebraic quantum field theory, observables are assigned to spacetime regions:

\[
\mathcal{O}
\mapsto
\mathcal{A}(\mathcal{O}).
\]

Microcausality requires that spacelike-separated observables commute:

\[
[A(\mathcal{O}_1),B(\mathcal{O}_2)]=0
\quad
\text{if}
\quad
\mathcal{O}_1
\text{ spacelike }
\mathcal{O}_2.
\]

Thus spacelike-separated measurements define compatible contexts.

Bell contextuality appears naturally in local quantum field theory. The Reeh–Schlieder theorem and vacuum entanglement imply strong nonclassical correlations across regions.

Thus contextuality is not limited to finite-dimensional systems. It is embedded in relativistic quantum field theory.

---

## 19. Contextuality and Spacetime

If measurement contexts are physical frames, then the structure of contexts may itself be related to spacetime structure.

In classical spacetime, contexts can be organized by causal compatibility:

\[
C_1
\sim
C_2
\]

if their measurements can be jointly implemented without causal conflict.

In quantum gravity, causal structure may be indefinite. Then the context structure itself may become quantum.

This suggests a possible relation between contextuality and emergent spacetime:

\[
\boxed{
\text{The geometry of contexts may underlie the geometry of spacetime.}
}
\]

Contextuality obstructions may be interpreted as curvature or topological structure in the space of possible properties.

---

## 20. Axioms of Contextuality Relativity

The framework may be organized around nine axioms.

### Axiom 1: Contexts Are Physical

A measurement context is a physically realizable set of compatible interventions.

### Axiom 2: Properties Are Contextual

An observable has a definite value only relative to a context containing it.

### Axiom 3: Probabilities Are Context-Conditioned

The basic probability is

\[
P(O\mid C).
\]

### Axiom 4: No Context Is Privileged

Physical law is invariant under changes among admissible contexts.

### Axiom 5: Empirical Models Are Invariant Content

The physical content is the compatible family of context-relative probabilities.

### Axiom 6: Noncontextual Global Valuations Are Not Required

Reality need not admit a global assignment of values to all observables.

### Axiom 7: Contextuality Is an Obstruction

Contextuality is the obstruction to gluing local valuations into a global section.

### Axiom 8: Compatibility Defines Geometry

The structure of compatible contexts defines a relational geometry of properties.

### Axiom 9: Contextuality Is a Resource

Contextual correlations are physically useful and operationally meaningful.

---

## 21. Experimental Relevance

Contextuality has been tested in many physical systems.

Experimental platforms include:

1. trapped ions,
2. photonic systems,
3. superconducting qubits,
4. nuclear magnetic resonance,
5. neutron interferometry,
6. solid-state spins,
7. high-dimensional quantum systems.

Tests include:

1. Kochen–Specker set experiments,
2. Peres–Mermin square implementations,
3. KCBS inequality violations,
4. state-independent contextuality tests,
5. Bell-CHSH violations,
6. sequential measurement contextuality,
7. contextuality in noisy qubit systems.

These experiments confirm that contextuality is not merely philosophical. It is an empirical feature of nature.

---

## 22. Open Problems

Several major problems remain.

### 22.1 Contextuality in Infinite Dimensions

A complete theory of contextuality for quantum field theory and continuous variables remains incomplete.

### 22.2 Contextuality and Gravity

The relation between contextuality, causal structure, and quantum gravity is largely unexplored.

### 22.3 Dynamical Contexts

Most treatments assume fixed measurement contexts. A theory of dynamical or quantum-controlled contexts is needed.

### 22.4 Contextuality and Time

How contextuality relates to temporal ordering, causal inference, and histories formulations remains open.

### 22.5 Resource Theory

A unified resource theory of contextuality across all quantum models is still developing.

### 22.6 Contextuality and Objectivity

How objective classical reality emerges from contextual quantum facts requires further clarification.

### 22.7 Contextuality and Observers

A full account of observer-relative contexts in Wigner’s-friend and cosmological scenarios remains open.

---

## 23. What Einstein Would Think

Einstein would resist Contextuality Relativity.

He believed in an observer-independent reality. The idea that properties are not possessed by systems independently of measurement contexts would trouble him.

But Einstein would recognize the structural lesson.

General relativity taught that coordinates are not physical. Contextuality Relativity teaches that context-independent properties are not physical.

The invariant is not a value assigned in one frame. It is the lawful relation among all frames.

Einstein might reject the ontology. But he would respect the invariance principle.

---

## 24. Summary of Core Equations

### Context-conditioned probability

\[
P(O\mid C).
\]

### Compatibility

\[
[A_i,A_j]=0.
\]

### Born rule in context

\[
P(i\mid C)
=
\operatorname{Tr}(\rho P_i).
\]

### Ontological model

\[
p(k\mid P,M)
=
\int d\lambda\,
\mu_P(\lambda)
\xi_M(k\mid\lambda).
\]

### Noncontextuality conditions

\[
P\sim P'
\Rightarrow
\mu_P(\lambda)=\mu_{P'}(\lambda),
\]

\[
M\sim M'
\Rightarrow
\xi_M(k\mid\lambda)=\xi_{M'}(k\mid\lambda).
\]

### Kochen–Specker valuation

\[
v(P)\in\{0,1\},
\]

\[
\sum_i v(P_i)=1.
\]

### Bell local hidden-variable model

\[
P(a,b\mid x,y)
=
\int d\lambda\,
\rho(\lambda)
P(a\mid x,\lambda)
P(b\mid y,\lambda).
\]

### CHSH inequality

\[
S
=
E_{00}+E_{01}+E_{10}-E_{11}
\leq 2.
\]

### Quantum CHSH violation

\[
S=2\sqrt{2}.
\]

### KCBS inequality

\[
\sum_{i=1}^5
\langle P_i\rangle
\leq 2.
\]

### Quantum KCBS value

\[
\sum_{i=1}^5
\langle P_i\rangle
=
\sqrt{5}.
\]

### Graph-theoretic bounds

\[
\alpha(G)
\leq
\vartheta(G).
\]

### Contextual fraction

\[
\operatorname{CF}(e)
=
\min
\left\{
\lambda
\mid
e=\lambda e_{\text{C}}+(1-\lambda)e_{\text{NC}}
\right\}.
\]

### Central principle

\[
\boxed{
\text{Properties are context-relative, not system-absolute.}
}
\]

---

## 25. Conclusion

Relativity 26.0, Contextuality Relativity, asserts that physical properties are not absolute attributes of systems. They are defined relative to measurement contexts.

The basic object is not

\[
P(O),
\]

but

\[
P(O\mid C).
\]

The Kochen–Specker theorem shows that no global, context-independent valuation of quantum observables exists. Bell nonlocality shows that this contextuality includes spacelike-separated measurement choices. Generalized contextuality shows that the phenomenon extends to preparations, transformations, and noisy operations.

The invariant content of physics is not a global assignment of values. It is the empirical model: the consistent family of context-relative probabilities.

Contextuality is not a failure of realism. It is a refinement of realism. Reality is not a collection of pre-existing properties. It is a structured network of contextual relations.

The central principle is:

\[
\boxed{
\text{Properties are context-relative, not system-absolute.}
}
\]

Contextuality Relativity extends the relativistic revolution into the structure of properties themselves.

Just as motion is relative, geometry is relative, frames are relative, locality is relative, and description is relative, so too are properties relative.

This is Relativity 26.0.

---

## Appendix A: Kochen–Specker Valuation Rules

Let \(A\) be an observable with spectral decomposition

\[
A
=
\sum_i a_i P_i.
\]

A valuation \(v\) assigns a real number \(v(A)\).

The Kochen–Specker rules require:

\[
v(A)\in\{a_i\},
\]

\[
v(f(A))=f(v(A)),
\]

and for commuting \(A,B\),

\[
v(A+B)=v(A)+v(B),
\]

\[
v(AB)=v(A)v(B).
\]

For projectors,

\[
v(P)\in\{0,1\}.
\]

For a complete context,

\[
\sum_i P_i=I,
\]

one must have

\[
\sum_i v(P_i)=1.
\]

The Kochen–Specker theorem proves that no such valuation exists for all projectors in Hilbert space dimension \(d\geq 3\).

---

## Appendix B: Peres–Mermin Contradiction

The Peres–Mermin square is

\[
\begin{array}{ccc}
X\otimes I & I\otimes X & X\otimes X \\
I\otimes Y & Y\otimes I & Y\otimes Y \\
X\otimes Y & Y\otimes X & Z\otimes Z
\end{array}
\]

Row products:

\[
R_1=R_2=R_3=+I.
\]

Column products:

\[
C_1=C_2=+I,
\qquad
C_3=-I.
\]

A noncontextual \(\pm1\) assignment would require the product of all six context products to be \(+1\), because each observable appears twice.

But the quantum products give

\[
(+1)^5(-1)=-1.
\]

Contradiction.

---

## Appendix C: Sheaf-Theoretic Contextuality

A measurement scenario is

\[
(X,\mathcal{M},O).
\]

An empirical model assigns to each context \(C\in\mathcal{M}\) a distribution

\[
e_C\in\operatorname{Prob}(O^C).
\]

Compatibility requires

\[
e_C|_{C'}=e_{C'}
\quad
\text{for } C'\subseteq C.
\]

A noncontextual model is a distribution \(p(g)\) over global assignments

\[
g:X\to O
\]

such that

\[
e_C
=
\sum_g p(g)\delta_{g|_C}.
\]

Contextuality is the nonexistence of such \(p(g)\).

---

## Appendix D: Graph-Theoretic Contextuality

Let \(G=(V,E)\) be an exclusivity graph.

Vertices \(v\in V\) represent events. Edges represent pairwise exclusivity.

The noncontextual maximum is

\[
\alpha(G),
\]

the independence number.

The quantum maximum is

\[
\vartheta(G),
\]

the Lovász theta number.

Contextuality occurs when

\[
\alpha(G)<\vartheta(G).
\]

For the pentagon,

\[
\alpha(C_5)=2,
\qquad
\vartheta(C_5)=\sqrt{5}.
\]

---

## Appendix E: Contextuality as Bundle Obstruction

Let \(F_C\) be the set of value assignments in context \(C\).

For overlapping contexts \(C,C'\), define transition maps

\[
T_{C\to C'}:F_C\to F_{C'}.
\]

A global valuation is a section \(s\) satisfying

\[
s(C)\in F_C,
\]

\[
T_{C\to C'}s(C)=s(C').
\]

Contextuality means no such section exists.

For a closed loop of contexts \(\gamma\), the holonomy may be nontrivial:

\[
T_\gamma v\neq v.
\]

The Peres–Mermin square gives

\[
T_\gamma v=-v.
\]

Thus contextuality is a nontrivial holonomy in the bundle of properties.

---

## Selected References

1. S. Kochen and E. P. Specker, “The Problem of Hidden Variables in Quantum Mechanics,” *Journal of Mathematics and Mechanics* **17**, 59 (1967).  
2. J. S. Bell, “On the Einstein Podolsky Rosen Paradox,” *Physics Physique Fizika* **1**, 195 (1964).  
3. J. S. Bell, “On the Problem of Hidden Variables in Quantum Mechanics,” *Reviews of Modern Physics* **38**, 447 (1966).  
4. A. Peres, “Two Simple Proofs of the Kochen-Specker Theorem,” *Journal of Physics A* **24**, L175 (1991).  
5. N. D. Mermin, “Simple Unified Form for the Major No-Hidden-Variables Theorems,” *Physical Review Letters* **65**, 3373 (1990).  
6. A. Cabello, “Experimentally Testable State-Independent Quantum Contextuality,” *Physical Review Letters* **101**, 210401 (2008).  
7. A. A. Klyachko, M. A. Can, S. Binicioglu, and A. S. Shumovsky, “Simple Test for Hidden Variables in Spin-1 Systems,” *Physical Review Letters* **101**, 020403 (2008).  
8. S. Abramsky and A. Brandenburger, “The Sheaf-Theoretic Structure of Non-Locality and Contextuality,” *New Journal of Physics* **13**, 113036 (2011).  
9. R. W. Spekkens, “Contextuality for Preparations, Transformations, and Unsharp Measurements,” *Physical Review A* **71**, 052108 (2005).  
10. M. Howard, J. Wallman, V. Veitch, and J. Emerson, “Contextuality Supplies the ‘Magic’ for Quantum Computation,” *Nature* **510**, 351 (2014).  
11. R. Raussendorf, “Contextuality in Measurement-Based Quantum Computation,” *Physical Review A* **88**, 022322 (2013).  
12. C. Budroni, A. Cabello, O. Gühne, M. Kleinmann, and J.-Å. Larsson, “Quantum Contextuality,” *Reviews of Modern Physics* **94**, 045007 (2022).  
13. A. Cabello, S. Severini, and A. Winter, “Graph-Theoretic Approach to Quantum Correlations,” *Physical Review Letters* **112**, 040401 (2014).  
14. L. E. Ballentine, *Quantum Mechanics: A Modern Development* (World Scientific, 1998).  
15. A. Fine, “Hidden Variables, Joint Probability, and the Bell Inequalities,” *Physical Review Letters* **48**, 291 (1982).
