# Observer Theory: Mathematical Observers in Relativity Mechanics

## Abstract

Observer Theory is the third derived theory of Relativity Mechanics. It answers the primitive question:

\[
\boxed{
\text{Who or what describes?}
}
\]

The answer is not philosophical but mathematical. An observer is defined as a map from a physical description space to an observer description space:

\[
\boxed{
O:\Omega\rightarrow D_O.
}
\]

Here \(\Omega\) is the space of admissible physical descriptions, and \(D_O\) is the description space accessible to, produced by, or internal to the observer \(O\). Observers are therefore not primitive conscious subjects, external metaphysical agents, or undefined measurement devices. They are mathematical objects: structured maps between description spaces, equipped with their own admissibility relations, report algebras, and transformation laws.

An observer is admissible when its observation map is compatible with the admissibility group of the underlying Relativity Mechanics schema. If \(G\) acts on \(\Omega\) and \(G_O\) acts on \(D_O\), then \(O\) is admissible when

\[
\boxed{
O(g\cdot\omega)=\rho(g)\cdot O(\omega)
}
\]

for all \(g\in G\), where \(\rho:G\to \operatorname{Aut}(D_O)\) is the induced action on the observer’s description space. Observer reports become physically meaningful only when they are invariant under the observer’s own admissibility structure. Thus observer-dependent descriptions become observer-independent facts only after the appropriate orbit quotient.

Observer Theory provides a unified mathematical treatment of classical observers, inertial frames, local laboratories, reference systems, gauge frames, quantum measurement devices, and quantum reference frames. It explains how observer-relative quantities — energy, local field components, clock readings, detector outcomes — become physically meaningful when the observer is included as part of the total relational description.

The central principle is:

\[
\boxed{
\text{An observer is a mathematical map between description spaces, not a philosophical subject.}
}
\]

---

## 1. Introduction

Relativity Mechanics begins with the observation that physical descriptions contain both invariant content and descriptive redundancy. Orbit Theory identifies physical objects with orbits

\[
[\omega]=G\cdot\omega.
\]

Invariant Theory identifies measurable quantities with functions satisfying

\[
f(g\cdot\omega)=f(\omega).
\]

Observer Theory now addresses the next question:

\[
\boxed{
\text{How are such orbits and invariants accessed by observers?}
}
\]

Physics often speaks informally of observers, reference frames, laboratories, detectors, clocks, and measuring apparatus. But in a foundational framework, these notions must be mathematically defined. Otherwise, “observer” becomes an undefined philosophical term.

Observer Theory solves this by defining an observer as a structured map

\[
O:\Omega\to D_O.
\]

The domain \(\Omega\) is the description space of the physical system or total physical situation. The codomain \(D_O\) is the observer’s own description space: the space of readings, records, pointer values, detector outcomes, frame components, or relational data available to that observer.

This definition does not identify the observer with consciousness. It does not privilege human observation. It does not introduce a transcendental viewpoint outside physics. An observer is a physical or mathematical structure that extracts a description from another description.

Thus:

\[
\boxed{
\text{Observers become mathematical objects.}
}
\]

Once observers are mathematical objects, they can be classified, compared, composed, constrained, quantized, and incorporated into the orbit ontology of Relativity Mechanics.

---

## 2. Relativity Mechanics Preliminaries

A Relativity Mechanics theory is specified by the schema

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

where:

- \(\Omega\) is a description space,
- \(G\) is an admissibility group,
- \(\triangleright:G\times\Omega\to\Omega\) is the action,
- \(I:\Omega\to\Omega/G\) is the invariant projection.

We write

\[
g\cdot\omega:=g\triangleright\omega.
\]

The orbit of \(\omega\) is

\[
[\omega]=G\cdot\omega.
\]

Physical objects are orbits. Physical observables are invariant functions:

\[
f(g\cdot\omega)=f(\omega).
\]

Observer Theory extends this structure by introducing explicit observer maps.

---

## 3. The Primitive Definition of an Observer

An observer is defined by the following primitive data.

### Definition 3.1: Observer structure

An observer \(\mathsf O\) over a Relativity Mechanics schema \(\mathcal R=(\Omega,G,\triangleright,I)\) is a tuple

\[
\boxed{
\mathsf O=(D_O,O,\rho,\mathcal M_O),
}
\]

where:

1. \(D_O\) is the observer description space,
2. \(O:\Omega\to D_O\) is the observation map,
3. \(\rho:G\to\operatorname{Aut}(D_O)\) is the observer representation of admissibility transformations,
4. \(\mathcal M_O\) is the report algebra or report space of the observer.

In the minimal formulation, the essential structure is simply

\[
\boxed{
O:\Omega\to D_O.
}
\]

The additional structures specify how the observer transforms under admissibility transformations and what counts as a valid observer report.

---

## 4. Observer Description Spaces

The observer description space \(D_O\) may be:

1. a manifold of pointer readings,
2. a space of clock and rod values,
3. a space of local frame components,
4. a space of detector outcomes,
5. a space of probability distributions,
6. a Hilbert-space measurement record,
7. a symbolic or computational record space.

Examples include:

\[
D_O=\mathbb R
\]

for a single real-valued reading,

\[
D_O=\mathbb R^4
\]

for spacetime coordinate readings,

\[
D_O=T^*\mathbb R^3
\]

for momentum measurements,

\[
D_O=\operatorname{Prob}(Y)
\]

for probabilistic outcomes,

\[
D_O=\mathcal H_O
\]

for a quantum observer Hilbert space.

The observer description space is not required to coincide with the physical description space \(\Omega\). Indeed, the power of Observer Theory lies in the fact that different observers may have different description spaces.

---

## 5. Observation Maps

The observation map

\[
O:\Omega\to D_O
\]

assigns to each physical description \(\omega\) the description registered by the observer.

If \(\omega\) describes a complete physical situation, then

\[
O(\omega)
\]

is the observer’s description of that situation.

For example:

- A clock observer may extract a time reading.
- A spatial frame observer may extract relative positions.
- A detector may extract an outcome label.
- A local Lorentz observer may extract tetrad components.
- A gauge observer may extract internal components relative to a local gauge frame.

The map \(O\) is the mathematical representation of observational access.

---

## 6. Admissible Observers

An observer is physically meaningful only if it is compatible with the admissibility structure of the underlying theory.

Suppose \(G\) acts on \(\Omega\). Suppose \(D_O\) carries an action of \(G\) through a representation

\[
\rho:G\to\operatorname{Aut}(D_O).
\]

We say that \(O\) is an admissible observer if

\[
\boxed{
O(g\cdot\omega)=\rho(g)\cdot O(\omega)
}
\]

for all \(g\in G\), \(\omega\in\Omega\).

This is the observer equivariance condition.

It says that changing the physical description by an admissibility transformation changes the observer’s description by the corresponding observer-side transformation.

If \(\rho\) is trivial,

\[
\rho(g)=\operatorname{id}_{D_O},
\]

then the observer map itself is invariant:

\[
O(g\cdot\omega)=O(\omega).
\]

In that case, the observer directly produces an invariant description.

More generally, the observer’s raw description may transform covariantly, and invariant facts are obtained only after quotienting the observer description space.

---

## 7. Descent of Observer Maps to Quotients

An admissible observer induces a map between orbit spaces.

### Theorem 7.1: Observer descent

Let

\[
O:\Omega\to D_O
\]

be an observer map satisfying

\[
O(g\cdot\omega)=\rho(g)\cdot O(\omega).
\]

Then \(O\) descends to a well-defined map

\[
\bar O:\Omega/G\to D_O/\rho(G)
\]

given by

\[
\bar O([\omega])=[O(\omega)].
\]

### Proof

We must show that \(\bar O\) is independent of representative.

Let

\[
\omega'=g\cdot\omega.
\]

Then

\[
O(\omega')=O(g\cdot\omega)=\rho(g)\cdot O(\omega).
\]

Therefore \(O(\omega')\) and \(O(\omega)\) lie on the same \(\rho(G)\)-orbit in \(D_O\). Hence

\[
[O(\omega')]=[O(\omega)].
\]

Thus \(\bar O\) is well defined.

\(\square\)

This theorem is central. It says that an admissible observer does not merely map descriptions to descriptions. It maps physical objects to observer objects.

\[
\boxed{
\text{Admissible observers descend to maps between orbits.}
}
\]

---

## 8. Observer Reports

An observer report is a function or map defined on the observer description space.

Let

\[
r:D_O\to Y
\]

be a report map, where \(Y\) is an outcome space.

The observed quantity is the pullback

\[
r_O:\Omega\to Y,
\]

\[
r_O(\omega)=r(O(\omega)).
\]

If \(Y=\mathbb R\), then \(r\) is a real-valued observer report.

The report \(r\) is physically meaningful only if it does not depend on redundant features of the observer description.

If \(D_O\) carries an action of \(\rho(G)\), then a report \(r\) is invariant if

\[
\boxed{
r(\rho(g)\cdot d)=r(d)
}
\]

for all \(g\in G\), \(d\in D_O\).

Then the pulled-back report satisfies

\[
r_O(g\cdot\omega)
=
r(O(g\cdot\omega))
=
r(\rho(g)\cdot O(\omega))
=
r(O(\omega))
=
r_O(\omega).
\]

Therefore:

\[
\boxed{
r_O\in C^\infty(\Omega)^G.
}
\]

Thus observer reports become physical observables precisely when they are invariant under the observer’s admissibility action.

---

## 9. The Observer Report Algebra

The report algebra of an observer is

\[
\mathcal M_O\subset C^\infty(D_O).
\]

The physical report algebra is

\[
\mathcal M_O^{\rm phys}
=
\mathcal M_O\cap C^\infty(D_O)^{\rho(G)}.
\]

The observer-induced observable algebra is

\[
\boxed{
\mathcal A_O
=
O^*\bigl(\mathcal M_O^{\rm phys}\bigr).
}
\]

Explicitly,

\[
\mathcal A_O
=
\{
r\circ O
\mid
r\in \mathcal M_O^{\rm phys}
\}.
\]

Since each \(r\in\mathcal M_O^{\rm phys}\) is invariant on \(D_O\), each \(r\circ O\) is invariant on \(\Omega\). Therefore

\[
\mathcal A_O
\subset
C^\infty(\Omega)^G.
\]

Thus an observer defines a subalgebra of the full physical observable algebra.

This gives a precise meaning to observational accessibility:

\[
\boxed{
\text{An observable is accessible to observer }O
\text{ if it lies in }O^*(\mathcal M_O^{\rm phys}).
}
\]

---

## 10. Observational Completeness

An observer may or may not be capable of distinguishing all physical orbits.

### Definition 10.1: Orbit separation

An observer \(O\) separates physical orbits if for any two distinct orbits

\[
[\omega]\neq[\omega'],
\]

there exists a physical report \(r\in\mathcal M_O^{\rm phys}\) such that

\[
r(O(\omega))\neq r(O(\omega')).
\]

Equivalently, the descended map

\[
\bar O:\Omega/G\to D_O/\rho(G)
\]

is injective.

If \(\bar O\) is injective, then the observer can distinguish all physical objects in the quotient.

If \(\bar O\) is also surjective onto the relevant observer quotient, then the observer provides a complete description of the physical orbit space.

### Definition 10.2: Observational completeness

An observer is observationally complete if

\[
O^*\bigl(C^\infty(D_O)^{\rho(G)}\bigr)
=
C^\infty(\Omega)^G.
\]

That is, every physical observable can be expressed as an invariant observer report.

Most physical observers are not observationally complete. A thermometer does not measure all physical invariants. A detector does not access the full quantum state. A local frame does not measure global topology. Observer Theory makes this limitation mathematically explicit.

---

## 11. Observer Equivalence

Two observers may encode the same physical information in different forms.

Let

\[
\mathsf O_1=(D_1,O_1,\rho_1,\mathcal M_1),
\]

\[
\mathsf O_2=(D_2,O_2,\rho_2,\mathcal M_2).
\]

An observer transformation from \(\mathsf O_1\) to \(\mathsf O_2\) is a map

\[
\Phi:D_1\to D_2
\]

such that

\[
O_2=\Phi\circ O_1.
\]

If \(\Phi\) is an equivariant isomorphism,

\[
\Phi(\rho_1(g)d)=\rho_2(g)\Phi(d),
\]

then the two observers are equivalent.

Equivalence means:

\[
\boxed{
\mathsf O_1\cong\mathsf O_2.
}
\]

Their raw description spaces may differ, but their physical report algebras are the same.

If \(\Phi\) is not invertible, then one observer is a coarse-graining of the other.

If \(\Phi\) is injective but not surjective, then one observer is a refinement of the other.

Thus Observer Theory allows a precise hierarchy of observational resolution.

---

## 12. Observer Composition

Observers can be composed.

Suppose

\[
O_1:\Omega\to D_1
\]

and

\[
F:D_1\to D_2.
\]

Then

\[
O_2=F\circ O_1
\]

is a new observer.

If \(F\) is invariant,

\[
F(\rho_1(g)d)=F(d),
\]

then \(O_2\) directly produces invariant reports.

If \(F\) is equivariant,

\[
F(\rho_1(g)d)=\rho_2(g)F(d),
\]

then \(O_2\) is again an admissible observer.

Thus observation can be organized as a category of description maps.

---

## 13. Product Observers and Multiple Observers

Given observers

\[
O_1:\Omega\to D_1,
\]

\[
O_2:\Omega\to D_2,
\]

one may define the product observer

\[
O_{12}:\Omega\to D_1\times D_2
\]

by

\[
O_{12}(\omega)=(O_1(\omega),O_2(\omega)).
\]

The product observer records the joint descriptions of multiple observers.

If the observers have admissibility actions \(\rho_1,\rho_2\), then the product action is

\[
\rho_{12}(g)(d_1,d_2)
=
(\rho_1(g)d_1,\rho_2(g)d_2).
\]

Physical consensus among observers corresponds to invariant functions on the product observer space:

\[
r(d_1,d_2)
\]

satisfying

\[
r(\rho_1(g)d_1,\rho_2(g)d_2)=r(d_1,d_2).
\]

Thus intersubjective agreement is not a philosophical notion. It is an invariant on a product description space.

---

## 14. Observers as Physical Systems

In Relativity Mechanics, observers themselves are physical. Therefore an observer should also be describable by a description space and an admissibility group.

Let the observer as a physical system have description space

\[
\Omega_O.
\]

The observer’s state is an orbit

\[
[\omega_O]\in\Omega_O/G_O.
\]

When the observed system and the observer are considered together, the total description space is

\[
\Omega_{\rm tot}
=
\Omega_S\times\Omega_O.
\]

The admissibility group acts diagonally:

\[
g\cdot(\omega_S,\omega_O)
=
(g\cdot\omega_S,g\cdot\omega_O).
\]

A relational observable involving both system and observer is a function

\[
F:\Omega_S\times\Omega_O\to\mathbb R
\]

satisfying

\[
F(g\cdot\omega_S,g\cdot\omega_O)
=
F(\omega_S,\omega_O).
\]

This is the correct relational treatment of observer-dependent quantities.

For example, the energy of a particle measured by an observer is not an invariant of the particle alone. It is an invariant of the particle-observer pair.

Thus:

\[
\boxed{
\text{Observer-dependent quantities become physical when the observer is included in the orbit.}
}
\]

---

## 15. Observer-Relative Quantities

Many standard physical quantities are observer-relative.

Examples include:

1. energy,
2. momentum components,
3. electric and magnetic field decomposition,
4. simultaneity,
5. local frame components,
6. detector outcomes,
7. clock readings.

These quantities are not invariant under the full admissibility group if considered as functions of the observed system alone. They become meaningful when the observer is included.

Let \(u\) denote an observer state, for example a four-velocity. Let \(p\) denote a particle momentum. The energy measured by the observer is

\[
E_u(p)
=
-p_\mu u^\mu.
\]

Under a Lorentz transformation \(\Lambda\),

\[
p\mapsto \Lambda p,
\]

\[
u\mapsto \Lambda u.
\]

Then

\[
E_{\Lambda u}(\Lambda p)
=
-(\Lambda p)_\mu(\Lambda u)^\mu
=
-p_\mu u^\mu
=
E_u(p).
\]

Thus the measured energy is not invariant under transformations of the particle alone, but it is invariant under simultaneous transformation of particle and observer.

In Relativity Mechanics language:

\[
E(p,u)
\]

is an invariant on the combined description space.

This resolves the apparent tension between observer-dependence and objectivity.

\[
\boxed{
\text{Observer-relative does not mean non-physical; it means relational.}
}
\]

---

## 16. Classical Observers

### 16.1 Newtonian observers

In Newtonian mechanics, an observer may be represented by a worldline

\[
X_O(t)
\]

and a spatial frame.

The observer description of a particle trajectory \(\mathbf x_i(t)\) may be

\[
O(\mathbf x_i)
=
\mathbf x_i(t)-X_O(t).
\]

Relative positions,

\[
\mathbf x_i-\mathbf x_j,
\]

are invariant under Galilean transformations. Absolute position is not.

Thus a Newtonian observer extracts relative spatial descriptions from Galilean orbits.

---

### 16.2 Inertial observers in special relativity

An inertial observer may be represented by a timelike four-velocity

\[
u^\mu,
\qquad
u^\mu u_\mu=-1.
\]

A local observer may also carry an orthonormal tetrad

\[
e_I^\mu,
\qquad
e_0^\mu=u^\mu.
\]

The observer measures components of a tensor by projection. For a momentum vector \(p^\mu\),

\[
E=-p_\mu u^\mu,
\]

\[
p^I=p_\mu e_I^\mu.
\]

For the electromagnetic field,

\[
E_I=F_{\mu\nu}u^\mu e_I^\nu,
\]

\[
B^I=\frac12\epsilon^I{}_{JK}F_{\mu\nu}e_J^\mu e_K^\nu.
\]

These components are observer-frame dependent. But the full relation between field and observer is Lorentz covariant. Scalar invariants such as

\[
F_{\mu\nu}F^{\mu\nu}
\]

and

\[
F_{\mu\nu}\tilde F^{\mu\nu}
\]

are observer-independent.

Thus special-relativistic observers are local frame maps whose reports become physical after Lorentz quotient.

---

### 16.3 Observers in general relativity

In general relativity, coordinate labels are not physical. Observers must be described relationally.

A common construction uses scalar fields as clocks and rods:

\[
T^A:M\to\mathbb R,
\qquad A=0,1,2,3.
\]

The observer description of a scalar field \(\phi\) at the event where the clocks read \(\tau^A\) is

\[
\mathcal O_\phi(\tau)
=
\phi(p),
\]

where \(p\) is the point satisfying

\[
T^A(p)=\tau^A.
\]

Under a diffeomorphism \(\varphi\),

\[
T^A\mapsto \varphi^*T^A,
\]

\[
\phi\mapsto \varphi^*\phi,
\]

\[
p\mapsto \varphi(p).
\]

But the value \(\phi(p)\) is unchanged. Therefore

\[
\mathcal O_\phi(\tau)
\]

is diffeomorphism invariant.

Thus in generally covariant theories, observers are relational reference systems.

---

## 17. Relational Observables as Observer Reports

Relational observables are a central class of observer reports.

Let \(T^A\) be reference fields and let \(f\) be a physical field. Define

\[
O_{f,T}(\tau)
=
f\big|_{T=\tau}.
\]

A diffeomorphism-invariant integral representation is

\[
O_{f,T}(\tau)
=
\int_M d^4x\,\sqrt{-g}\,
\delta^4(T(x)-\tau)
f(x),
\]

assuming the map \(x\mapsto T(x)\) is sufficiently well behaved.

Under diffeomorphisms, the measure, delta distribution, and scalar fields transform consistently, leaving the integral invariant.

Thus observer reports in gravity are naturally relational.

---

## 18. Gauge Observers

In Gauge Theory of Admissibility, an observer may choose an internal gauge frame.

Let \(G\) be the internal gauge group. A gauge observer may describe matter fields relative to a local internal basis. The observer description space \(D_O\) carries a representation of \(G\).

A matter field transforms as

\[
\psi\mapsto u\psi,
\]

where

\[
u:M\to G.
\]

A gauge observer’s raw components transform accordingly. Physical reports must be gauge singlets.

Examples of gauge-invariant observer reports include:

\[
\bar\psi\psi,
\]

\[
\operatorname{tr}(F_{\mu\nu}F^{\mu\nu}),
\]

\[
W_R(C)
=
\operatorname{Tr}_R
\mathcal P
\exp
\left(
\oint_C A
\right).
\]

Thus in gauge theory, an observer may internally frame the system, but only gauge-invariant reports are physically admissible.

---

## 19. Quantum Observers

Observer Theory extends naturally to quantum physics.

In quantum theory, a physical description may be a density operator \(\rho\) on a Hilbert space \(\mathcal H\). A quantum measurement is described by a positive operator-valued measure (POVM)

\[
E(\Delta),
\]

where \(\Delta\) is a measurable subset of an outcome space \(Y\).

The quantum observer map is

\[
O_E:\mathcal S(\mathcal H)\to \operatorname{Prob}(Y),
\]

defined by

\[
O_E(\rho)(\Delta)
=
\operatorname{Tr}(\rho E(\Delta)).
\]

Here \(\mathcal S(\mathcal H)\) is the space of quantum states.

If the admissibility group \(G\) acts unitarily on \(\mathcal H\),

\[
\rho\mapsto U(g)\rho U(g)^\dagger,
\]

then an invariant quantum observer satisfies

\[
\boxed{
U(g)E(\Delta)U(g)^\dagger=E(\Delta).
}
\]

Then the outcome probabilities are invariant:

\[
\operatorname{Tr}(U(g)\rho U(g)^\dagger E(\Delta))
=
\operatorname{Tr}(\rho E(\Delta)).
\]

If the outcome space itself transforms under \(G\), one uses covariant POVMs:

\[
U(g)E(\Delta)U(g)^\dagger
=
E(g\Delta).
\]

In that case, the observer’s raw outcomes transform, but relational probabilities remain well defined when the outcome frame is included.

Thus a quantum observer is a measurement map satisfying the appropriate equivariance or invariance condition.

---

## 20. Quantum Reference Frames

A quantum reference frame is an observer whose reference system is itself quantum.

Let the system Hilbert space be \(\mathcal H_S\) and the reference-system Hilbert space be \(\mathcal H_R\). The total Hilbert space is

\[
\mathcal H_{\rm tot}
=
\mathcal H_S\otimes\mathcal H_R.
\]

Suppose \(G\) acts diagonally:

\[
U_{\rm tot}(g)
=
U_S(g)\otimes U_R(g).
\]

Physical states satisfy

\[
U_{\rm tot}(g)|\Psi\rangle
=
|\Psi\rangle.
\]

A quantum observer conditions the system description on a reading of the reference system. If \(\Pi_r\) is a projector associated with the reference reading \(r\), then the conditional state is

\[
\rho_{S|r}
=
\frac{
\operatorname{Tr}_R
\left[
(\mathbf 1_S\otimes\Pi_r)
\rho_{\rm tot}
\right]
}{
p(r)
},
\]

with

\[
p(r)
=
\operatorname{Tr}
\left[
(\mathbf 1_S\otimes\Pi_r)
\rho_{\rm tot}
\right].
\]

If the projectors \(\Pi_r\) transform covariantly, the relational conditional state is well defined under the admissibility group.

Thus quantum reference frames are observer structures in which the observer map is implemented by quantum conditioning.

---

## 21. Stochastic Observers

Not all observers are deterministic. A general classical observer may be described by a stochastic kernel

\[
K(\omega,dd),
\]

which assigns to each physical description \(\omega\) a probability distribution over \(D_O\).

The observer map is then

\[
O:\Omega\to \operatorname{Prob}(D_O).
\]

Admissibility requires equivariance:

\[
K(g\cdot\omega,\cdot)
=
\rho(g)_*K(\omega,\cdot).
\]

For an invariant report \(r\), the expected report is

\[
\langle r\rangle_O(\omega)
=
\int_{D_O} r(d)\,K(\omega,dd).
\]

If \(r\) is invariant, then

\[
\langle r\rangle_O(g\cdot\omega)
=
\langle r\rangle_O(\omega).
\]

Thus stochastic observers are naturally incorporated into Observer Theory.

---

## 22. Observer Limitations and Information

Observer Theory makes observational limitation precise.

An observer may fail to be complete in several ways:

1. \(O\) may not separate orbits.
2. \(\mathcal M_O^{\rm phys}\) may be a proper subalgebra of \(C^\infty(\Omega)^G\).
3. \(D_O\) may have lower dimension than \(\Omega/G\).
4. The observer may be noisy.
5. The observer may be quantum-limited.
6. The observer may have access only to a subsystem.

These are not philosophical defects. They are mathematical properties of the observer map.

Observer Theory therefore provides the foundation for Relativistic Information Theory: information is invariant distinguishability accessible through observer maps.

---

## 23. Observer Transformations and Reference Transformation Theory

Observer Theory naturally leads to Reference Transformation Theory.

Given two observers

\[
O_1:\Omega\to D_1,
\]

\[
O_2:\Omega\to D_2,
\]

one may ask whether there exists a map

\[
T_{12}:D_1\to D_2
\]

such that

\[
O_2=T_{12}\circ O_1.
\]

If such a map exists, then the second observer’s descriptions can be computed from the first observer’s descriptions.

If \(T_{12}\) is equivariant, then the transformation preserves admissibility structure.

If \(T_{12}\) is invertible, the observers are intertranslatable.

If no such map exists, the observers are genuinely inequivalent.

Thus changes of observer, frame, reference system, or even theoretical description are morphisms between observer structures.

---

## 24. Observer Theory and Frame Theory

Frame Theory is a special case of Observer Theory.

In Frame Theory, the admissible descriptions are local frames

\[
e^I_\mu.
\]

A local observer may be identified with a timelike frame vector

\[
e_0^\mu=u^\mu
\]

and spatial frame vectors

\[
e_i^\mu.
\]

The observer description space consists of local Lorentz components.

For a tensor \(T\), the observer measures

\[
T^{I J \cdots}{}_{K L \cdots}
=
e^I_{\mu}e^J_{\nu}\cdots
e_K^{\rho}e_L^{\sigma}\cdots
T^{\mu\nu\cdots}{}_{\rho\sigma\cdots}.
\]

Under local spin transformations,

\[
e^I\mapsto \Lambda^I{}_J e^J,
\]

the components transform covariantly. Invariant reports are obtained by contraction or relational completion.

Thus a frame is a particular mathematical observer.

---

## 25. Observer Theory and Gauge Theory of Admissibility

In Gauge Theory of Admissibility, observers may be internal gauge frames.

For a gauge group \(G\), an internal observer may describe fields relative to a local trivialization. Under a gauge transformation,

\[
\psi\mapsto u\psi,
\]

\[
A\mapsto uAu^{-1}+\frac{i}{g}(\partial u)u^{-1}.
\]

The observer’s raw internal components transform. Physical reports are gauge-invariant combinations.

Thus gauge observers are internal observers. Their admissible reports are singlets under the gauge group.

---

## 26. Observer Theory and Invariant Theory

Observer Theory does not replace Invariant Theory. It operationalizes it.

Invariant Theory says:

\[
\boxed{
f(g\cdot\omega)=f(\omega).
}
\]

Observer Theory says:

\[
\boxed{
\text{An observer can report }f\text{ if }f= r\circ O
\text{ for some invariant report }r.
}
\]

Thus the invariant algebra is the total space of physical observability, while an observer report algebra is the portion of that space accessible to a given observer.

---

## 27. Observer Theory and Orbit Theory

Orbit Theory says:

\[
\boxed{
\text{Physical object}=[\omega].
}
\]

Observer Theory says:

\[
\boxed{
\text{Observer access is a map between orbit spaces.}
}
\]

An admissible observer induces

\[
\bar O:\Omega/G\to D_O/\rho(G).
\]

Therefore observers do not access raw descriptions. They access orbits, possibly through limited or noisy maps.

---

## 28. Philosophical Consequences Without Philosophy

Observer Theory eliminates the need for philosophical ambiguity.

An observer is not:

1. a conscious subject,
2. an undefined measurement agent,
3. a transcendental viewpoint,
4. a primitive epistemic authority.

An observer is:

\[
\boxed{
O:\Omega\to D_O.
}
\]

Together with:

1. an observer description space,
2. an admissibility representation,
3. a report algebra,
4. an equivariance condition.

This makes observers compatible with the orbit ontology of Relativity Mechanics.

Observers are physical structures, and their reports are physical only when invariant under the relevant admissibility transformations.

---

## 29. Summary of the Observer-Theoretic Schema

The essential structure of Observer Theory is as follows.

Given a Relativity Mechanics schema

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

an observer is

\[
\boxed{
\mathsf O=(D_O,O,\rho,\mathcal M_O).
}
\]

The core observation map is

\[
\boxed{
O:\Omega\to D_O.
}
\]

Admissibility requires

\[
\boxed{
O(g\cdot\omega)=\rho(g)\cdot O(\omega).
}
\]

The observer descends to

\[
\boxed{
\bar O:\Omega/G\to D_O/\rho(G).
}
\]

A report

\[
r:D_O\to Y
\]

is physical if

\[
\boxed{
r(\rho(g)d)=r(d).
}
\]

The observed quantity is

\[
\boxed{
r_O=r\circ O.
}
\]

The observer report algebra is

\[
\boxed{
\mathcal A_O=
O^*\bigl(C^\infty(D_O)^{\rho(G)}\bigr).
}
\]

This algebra is a subalgebra of the full invariant observable algebra:

\[
\mathcal A_O\subset C^\infty(\Omega)^G.
\]

Observer equivalence, refinement, composition, and consensus are defined by morphisms between observer structures.

---

## 30. Conclusion

Observer Theory answers the primitive question:

\[
\boxed{
\text{Who or what describes?}
}
\]

The answer is mathematical:

\[
\boxed{
\text{An observer is a map }O:\Omega\to D_O.
}
\]

Observers are not philosophical subjects. They are structured relations between description spaces. They are constrained by admissibility, governed by equivariance, and evaluated through invariant reports.

Observer-dependent quantities are not rejected. They are understood as relational structures involving both system and observer. When the observer is included in the total admissibility orbit, observer-relative quantities become invariant physical facts.

Thus Observer Theory completes the first triad of Relativity Mechanics:

\[
\text{Orbit Theory} \rightarrow \text{objects},
\]

\[
\text{Invariant Theory} \rightarrow \text{observables},
\]

\[
\text{Observer Theory} \rightarrow \text{access}.
\]

Together they establish the relational architecture of physical description.

\[
\boxed{
\text{Observers are mathematical objects; observation is equivariant descent between description spaces.}
}
\]
