# Reference Transformation Theory: Morphisms Between Admissibility Structures and the Transformation of Physical Frameworks

## Abstract

Reference Transformation Theory is the fourth derived theory of Relativity Mechanics. It addresses the primitive structural question:

\[
\boxed{
\text{How are different physical descriptions, frames, theories, or frameworks related?}
}
\]

In Relativity Mechanics, a physical framework is determined by a description space \(\Omega\), an admissibility group \(G\), and the quotient

\[
\Omega/G,
\]

whose points are physical orbits. When two admissibility structures exist,

\[
(\Omega_1,G_1),
\qquad
(\Omega_2,G_2),
\]

one must study maps between their physical state spaces:

\[
\boxed{
\Phi:\Omega_1/G_1\longrightarrow \Omega_2/G_2.
}
\]

Such maps describe changes of reference framework, changes of admissibility group, reductions, embeddings, coarse-grainings, dualities, limits, and theory transformations.

This paper develops Reference Transformation Theory as the rigorous theory of morphisms between admissibility structures. We define equivariant lifts, quotient maps, observable pullbacks, dynamical compatibility, stratified transformations, group homomorphisms, and equivalence of frameworks. We show that coordinate transformations, frame-to-metric projections, gauge transformations, symmetry breaking, nonrelativistic limits, quantum reference-frame changes, and string dualities are all special cases of reference transformations.

The central principle is:

\[
\boxed{
\text{A change of physical framework is a well-defined map between orbit spaces.}
}
\]

Reference Transformation Theory therefore provides the mathematical language in which Relativity Mechanics describes not only objects and observables, but also the relations between entire physical frameworks.

---

## 1. Introduction

Relativity Mechanics is built on the schema

\[
\mathcal R=(\Omega,G,\triangleright,I),
\]

where \(\Omega\) is a description space, \(G\) is an admissibility group, and

\[
I:\Omega\to\Omega/G
\]

is the invariant projection. Orbit Theory identifies physical objects with orbits

\[
[\omega]=G\cdot\omega.
\]

Invariant Theory identifies observables with functions on the quotient:

\[
\mathcal O_{\rm phys}=C^\infty(\Omega/G).
\]

Observer Theory introduces maps by which observers access descriptions.

Reference Transformation Theory now asks the next structural question:

\[
\boxed{
\text{What happens when there are two admissibility frameworks?}
}
\]

Suppose we have two description spaces,

\[
\Omega_1,\qquad \Omega_2,
\]

and two admissibility groups,

\[
G_1,\qquad G_2.
\]

Their physical state spaces are

\[
Q_1=\Omega_1/G_1,
\qquad
Q_2=\Omega_2/G_2.
\]

A reference transformation is a map

\[
\boxed{
\Phi:Q_1\to Q_2.
}
\]

Such a map may express:

1. a change of coordinates,
2. a change of frame,
3. a change of gauge,
4. a change of observer,
5. a reduction of a theory,
6. a limit of a theory,
7. a duality,
8. a symmetry breaking,
9. a quantization or classicalization map,
10. a transformation between different physical theories.

Thus Reference Transformation Theory is the theory of framework change.

Its guiding principle is:

\[
\boxed{
\text{Physical frameworks are related by maps between their orbit spaces.}
}
\]

---

## 2. Admissibility Structures

An admissibility structure is a triple

\[
\mathcal A=(\Omega,G,\triangleright),
\]

where \(G\) acts on \(\Omega\). The associated physical quotient is

\[
Q=\Omega/G.
\]

The projection is

\[
I:\Omega\to Q,
\qquad
I(\omega)=[\omega].
\]

A full Relativity Mechanics framework also includes observables and dynamics, but the kinematical core is the quotient

\[
Q=\Omega/G.
\]

We shall denote two such structures by

\[
\mathcal A_1=(\Omega_1,G_1,\triangleright_1),
\]

\[
\mathcal A_2=(\Omega_2,G_2,\triangleright_2).
\]

Their quotients are

\[
Q_1=\Omega_1/G_1,
\qquad
Q_2=\Omega_2/G_2.
\]

Reference Transformation Theory studies maps

\[
\Phi:Q_1\to Q_2.
\]

---

## 3. Reference Transformations

### 3.1 Basic definition

A **reference transformation** from \(\mathcal A_1\) to \(\mathcal A_2\) is a map

\[
\boxed{
\Phi:\Omega_1/G_1\to \Omega_2/G_2.
}
\]

If the quotients carry topology, smooth structure, stratification, measure, or algebraic structure, then \(\Phi\) is required to preserve the relevant structure.

For example:

- in topological settings, \(\Phi\) should be continuous;
- in smooth settings, \(\Phi\) should be smooth on strata;
- in measurable settings, \(\Phi\) should be measurable;
- in quantum settings, \(\Phi\) should preserve probabilistic or algebraic structure.

The minimal requirement is well-definedness on orbits.

---

### 3.2 The central condition

A map between quotients is physically meaningful only if it does not depend on arbitrary representatives.

That is, if

\[
[\omega_1]=[\omega_1']
\]

in \(\Omega_1/G_1\), then one must have

\[
\Phi([\omega_1])=\Phi([\omega_1']).
\]

This is automatic if \(\Phi\) is defined on the quotient, but it becomes nontrivial when one attempts to define \(\Phi\) using representatives.

Reference Transformation Theory therefore studies conditions under which representative-level constructions descend to the quotient.

---

## 4. Lifts and Equivariant Maps

Most reference transformations arise from maps between description spaces.

Let

\[
F:\Omega_1\to\Omega_2
\]

be a map between description spaces. We say that \(F\) is a **lift** of \(\Phi\) if the following diagram commutes:

\[
\begin{array}{ccc}
\Omega_1 & \xrightarrow{F} & \Omega_2 \\
\downarrow I_1 & & \downarrow I_2 \\
\Omega_1/G_1 & \xrightarrow{\Phi} & \Omega_2/G_2
\end{array}
\]

That is,

\[
\boxed{
\Phi\circ I_1=I_2\circ F.
}
\]

Equivalently,

\[
\Phi([\omega])=[F(\omega)].
\]

For this to be well defined, \(F\) must map \(G_1\)-orbits into \(G_2\)-orbits.

A sufficient and structurally natural condition is equivariance.

---

### 4.1 Equivariant morphisms

Suppose there is a group homomorphism

\[
\alpha:G_1\to G_2.
\]

A map

\[
F:\Omega_1\to\Omega_2
\]

is \(\alpha\)-equivariant if

\[
\boxed{
F(g\cdot\omega)=\alpha(g)\cdot F(\omega)
}
\]

for all \(g\in G_1\), \(\omega\in\Omega_1\).

An equivariant map induces a well-defined reference transformation

\[
\Phi:\Omega_1/G_1\to\Omega_2/G_2
\]

by

\[
\Phi([\omega])=[F(\omega)].
\]

---

### 4.2 The descent theorem

**Theorem 4.1.**  
Let \(F:\Omega_1\to\Omega_2\) and \(\alpha:G_1\to G_2\) satisfy

\[
F(g\cdot\omega)=\alpha(g)\cdot F(\omega).
\]

Then the map

\[
\Phi([\omega])=[F(\omega)]
\]

is well defined.

**Proof.**  
Let \(\omega'=g\cdot\omega\). Then

\[
F(\omega')
=
F(g\cdot\omega)
=
\alpha(g)\cdot F(\omega).
\]

Therefore \(F(\omega')\) and \(F(\omega)\) lie in the same \(G_2\)-orbit. Hence

\[
[F(\omega')]=[F(\omega)].
\]

Thus \(\Phi([\omega])\) is independent of the representative \(\omega\).

\(\square\)

This theorem is the foundational result of Reference Transformation Theory.

It says:

\[
\boxed{
\text{Equivariant maps between description spaces induce maps between physical frameworks.}
}
\]

---

## 5. The Category of Reference Transformations

Reference Transformation Theory naturally defines a category.

### Definition 5.1: The category \(\mathbf{Rel}\)

The category of admissibility structures, denoted \(\mathbf{Rel}\), has:

- objects: admissibility structures \((\Omega,G)\);
- morphisms: equivalence classes of equivariant pairs \((F,\alpha)\), where

\[
F:\Omega_1\to\Omega_2,
\]

\[
\alpha:G_1\to G_2,
\]

and

\[
F(g\cdot\omega)=\alpha(g)\cdot F(\omega).
\]

Composition is defined by composition of maps and homomorphisms:

\[
(F_{23},\alpha_{23})\circ(F_{12},\alpha_{12})
=
(F_{23}\circ F_{12},\alpha_{23}\circ\alpha_{12}).
\]

The identity morphism is

\[
(\operatorname{id}_\Omega,\operatorname{id}_G).
\]

There is a quotient functor

\[
Q:\mathbf{Rel}\to\mathbf{Quot}
\]

sending

\[
(\Omega,G)
\mapsto
\Omega/G,
\]

and

\[
(F,\alpha)
\mapsto
\Phi: \Omega_1/G_1\to\Omega_2/G_2.
\]

Thus Reference Transformation Theory may be formulated either at the level of equivariant description maps or at the level of induced quotient maps.

---

## 6. Observable Transformations

A reference transformation transforms observables by pullback.

Let

\[
\Phi:Q_1\to Q_2
\]

be a reference transformation, where

\[
Q_i=\Omega_i/G_i.
\]

An observable on framework 2 is a function

\[
f_2\in C^\infty(Q_2).
\]

Its pullback to framework 1 is

\[
\Phi^*f_2
=
f_2\circ\Phi
\in C^\infty(Q_1).
\]

Thus

\[
\boxed{
\Phi^*:C^\infty(Q_2)\to C^\infty(Q_1).
}
\]

This is the algebraic expression of reference transformation.

If \(\Phi\) is a diffeomorphism, then

\[
\Phi^*:C^\infty(Q_2)\to C^\infty(Q_1)
\]

is an algebra isomorphism.

If \(\Phi\) is surjective, then \(\Phi^*\) is injective: observables in framework 2 are faithfully represented in framework 1.

If \(\Phi\) is injective, then not every observable of framework 1 need arise from framework 2.

Thus the direction of the map is reversed at the level of observables.

---

## 7. Dynamical Reference Transformations

Reference Transformation Theory also applies to dynamics.

Suppose the two frameworks possess physical flows on their quotient spaces:

\[
\bar X_1\in\Gamma(TQ_1),
\qquad
\bar X_2\in\Gamma(TQ_2).
\]

A reference transformation

\[
\Phi:Q_1\to Q_2
\]

is dynamically compatible if

\[
\boxed{
\Phi_*\bar X_1=\bar X_2\circ\Phi.
}
\]

Equivalently, if \(\varphi_t^{(1)}\) and \(\varphi_t^{(2)}\) are the flows,

\[
\boxed{
\Phi\circ\varphi_t^{(1)}
=
\varphi_t^{(2)}\circ\Phi.
}
\]

This is a conjugacy or semi-conjugacy condition.

If \(\Phi\) is invertible and the above holds, the two dynamical systems are dynamically equivalent.

If \(\Phi\) is surjective but not injective, framework 2 is a reduced or coarse-grained dynamics of framework 1.

If \(\Phi\) is injective but not surjective, framework 1 describes a subsystem or sector of framework 2.

Thus Reference Transformation Theory classifies dynamical relationships between physical frameworks.

---

## 8. Transformations Induced by Group Relations

Many reference transformations arise directly from relations between admissibility groups.

### 8.1 Group inclusion and orbit merging

Suppose the same description space \(\Omega\) carries two admissibility groups with

\[
G_1\subset G_2.
\]

Then every \(G_1\)-orbit lies inside a \(G_2\)-orbit. There is a natural projection

\[
\boxed{
\pi:\Omega/G_1\to\Omega/G_2
}
\]

defined by

\[
\pi([\omega]_{G_1})=[\omega]_{G_2}.
\]

This map is well defined because if

\[
\omega'=g\cdot\omega
\]

with \(g\in G_1\), then \(g\in G_2\) as well, so \(\omega'\) is also in the same \(G_2\)-orbit.

Physically, passing from \(G_1\) to \(G_2\) merges formerly distinct descriptions into larger equivalence classes.

Thus:

\[
\boxed{
\text{Enlarging the admissibility group reduces the number of physical distinctions.}
}
\]

The observable algebras satisfy

\[
C^\infty(\Omega)^{G_2}
\subset
C^\infty(\Omega)^{G_1}.
\]

More admissibility means fewer invariant observables.

---

### 8.2 Group reduction and orbit splitting

If one passes from a larger group \(G_2\) to a smaller subgroup \(G_1\), then orbits split. There is generally no canonical map

\[
\Omega/G_2\to\Omega/G_1
\]

unless additional structure, such as a section or gauge fixing, is chosen.

When such a section exists locally, one obtains local reference transformations. Globally, obstructions may arise.

This is the mathematical origin of gauge-fixing ambiguity and Gribov-type phenomena.

---

### 8.3 Group homomorphisms

More generally, suppose there is a homomorphism

\[
\alpha:G_1\to G_2.
\]

If there exists a map

\[
F:\Omega_1\to\Omega_2
\]

satisfying

\[
F(g\cdot\omega)=\alpha(g)\cdot F(\omega),
\]

then \(F\) induces

\[
\Phi:\Omega_1/G_1\to\Omega_2/G_2.
\]

This is the general form of a representable reference transformation.

---

### 8.4 Group contractions and limits

Many physical limits are reference transformations induced by group contractions.

For example, the Galilei group arises as a contraction of the Poincaré group in the limit

\[
c\to\infty.
\]

At the Lie algebra level, the Lorentz boost generators are rescaled, and the commutation relations degenerate into the Galilean algebra.

A nonrelativistic limit may therefore be represented as a singular family of reference transformations

\[
\Phi_c:Q_{\rm Poincaré}\to Q_{\rm Galilei}
\]

whose limit exists only after appropriate quotienting, scaling, or projectivization.

Thus theory limits are not merely approximations. They are reference transformations between admissibility structures.

---

## 9. Types of Reference Transformations

Reference Transformation Theory distinguishes several fundamental classes of framework transformations.

### 9.1 Automorphisms of a framework

An automorphism is an invertible reference transformation

\[
\Phi:Q\to Q.
\]

It preserves the physical framework while reorganizing its descriptions.

Examples include:

- coordinate transformations,
- passive frame rotations,
- gauge transformations,
- canonical transformations,
- unitary basis changes.

Automorphisms express redundancy within a single framework.

---

### 9.2 Embeddings

An embedding is an injective reference transformation

\[
\Phi:Q_1\hookrightarrow Q_2.
\]

It represents one framework as a sector, subsystem, or subtheory of another.

Examples include:

- a particle sector inside a field theory,
- a symmetry-reduced model inside a full theory,
- a low-energy subspace inside a high-energy theory.

---

### 9.3 Projections and coarse-grainings

A projection is a surjective reference transformation

\[
\Phi:Q_1\twoheadrightarrow Q_2.
\]

It represents coarse-graining, reduction, or loss of descriptive detail.

Examples include:

- thermodynamic limits,
- hydrodynamic reductions,
- quotienting by additional symmetries,
- tracing out environmental degrees of freedom,
- passing from microscopic to macroscopic variables.

---

### 9.4 Equivalences and dualities

An equivalence is an invertible reference transformation preserving the full physical structure:

\[
\Phi:Q_1\to Q_2,
\]

with

\[
\Phi^*:C^\infty(Q_2)\to C^\infty(Q_1)
\]

an isomorphism of observable algebras, and with compatible dynamics.

A duality is an equivalence between frameworks that may look completely different at the level of representatives.

Thus dual frameworks have different description spaces and possibly different admissibility groups, but isomorphic physical quotients.

\[
\boxed{
\text{A duality is an isomorphism of orbit structures.}
}
\]

---

## 10. Stratified and Singular Reference Transformations

In many physical theories, quotient spaces are not smooth manifolds. They are stratified spaces.

For a Lie group action, orbit-type strata are

\[
\Omega_{(H)}/G,
\]

where \(H\) is a stabilizer subgroup.

A reference transformation

\[
\Phi:Q_1\to Q_2
\]

should respect stratification whenever possible. That is, it should map strata of \(Q_1\) into strata of \(Q_2\), or at least be smooth on each stratum.

If stabilizers are important, one may use the stacky quotient

\[
[\Omega/G].
\]

Then a reference transformation is a morphism of stacks

\[
[\Omega_1/G_1]\to[\Omega_2/G_2].
\]

This preserves residual automorphism data that the coarse quotient forgets.

Thus Reference Transformation Theory admits three levels:

1. coarse quotient maps,
2. stratified quotient maps,
3. stacky morphisms.

The appropriate level depends on the physical theory.

---

## 11. Coordinate Transformations as Reference Transformations

The simplest reference transformations are coordinate transformations.

Let \(\Omega\) be a space of fields on a manifold \(M\). A diffeomorphism

\[
\phi:M\to M
\]

acts by pullback:

\[
\phi\cdot g=\phi^*g,
\]

\[
\phi\cdot\psi=\phi^*\psi.
\]

If coordinates are treated as part of the description, then changing coordinates is a representative-level transformation. The physical quotient by diffeomorphisms identifies coordinate-related descriptions.

In Reference Transformation Theory, a coordinate transformation is an automorphism of the description space that descends to the identity on the diffeomorphism quotient:

\[
\Phi:\Omega/\operatorname{Diff}(M)\to\Omega/\operatorname{Diff}(M),
\]

\[
\Phi([g])=[g].
\]

Thus coordinate transformations are internal re-descriptions within a single orbit.

---

## 12. Frame-to-Metric Transformation

Frame Theory provides a fundamental example.

Let

\[
\Omega_{\rm frame}
\]

be the space of Lorentz coframes \(e^I_\mu\). Let

\[
G_{\rm frame}
=
C^\infty(M,\mathrm{Spin}(1,3)).
\]

The metric is the invariant

\[
g_{\mu\nu}
=
\eta_{IJ}e^I_\mu e^J_\nu.
\]

Define

\[
F:\Omega_{\rm frame}\to\Omega_{\rm met},
\]

\[
F(e)=g(e).
\]

Since

\[
F(\Lambda e)=F(e)
\]

for local spin transformations \(\Lambda\), the map descends to

\[
\Phi:\Omega_{\rm frame}/G_{\rm frame}
\to
\Omega_{\rm met}.
\]

In fact, up to orientation and time-orientation,

\[
\Omega_{\rm frame}/G_{\rm frame}
\cong
\mathrm{Met}_{1,3}(M).
\]

If one further quotients by diffeomorphisms, one obtains

\[
\mathrm{Met}_{1,3}(M)/\operatorname{Diff}(M).
\]

Thus the passage from frames to metrics to geometries is a chain of reference transformations.

\[
\boxed{
\text{Frame Theory}\longrightarrow\text{metric geometry}\longrightarrow\text{diffeomorphism geometry}.
}
\]

---

## 13. Gauge Transformations as Internal Reference Transformations

In Gauge Theory of Admissibility, the physical quotient is

\[
\mathcal A/\mathcal G,
\]

where \(\mathcal A\) is the space of connections and \(\mathcal G\) is the gauge group.

A gauge transformation

\[
u\in\mathcal G
\]

acts by

\[
A\mapsto A^u.
\]

At the quotient level, gauge transformations are trivial automorphisms:

\[
[A]\mapsto[A].
\]

However, changes of trivialization, bundle embeddings, and group homomorphisms induce nontrivial reference transformations between gauge-theoretic frameworks.

For example, if

\[
\iota:H\hookrightarrow G
\]

is an embedding of structure groups, then a reduction of a \(G\)-bundle to an \(H\)-bundle defines a reference transformation from \(H\)-gauge descriptions to \(G\)-gauge descriptions.

Conversely, symmetry breaking may produce a projection from a \(G\)-framework to an \(H\)-framework determined by the stabilizer of a vacuum orbit.

Thus gauge-theoretic changes of internal frame are reference transformations.

---

## 14. Symmetry Breaking as Reference Transformation

Consider a gauge group \(G\) and a Higgs field \(\phi\) taking values in a representation space \(V\). The vacuum orbit is

\[
\mathcal O_{\phi_0}=G\cdot\phi_0.
\]

The unbroken subgroup is the stabilizer

\[
H=G_{\phi_0}.
\]

Before symmetry breaking, the relevant internal admissibility group is \(G\). After choosing a vacuum orbit, the residual manifest admissibility group is \(H\).

The reference transformation is not a destruction of gauge admissibility. It is a passage from the full \(G\)-orbit description to a description organized around the orbit and stabilizer pair

\[
(G,H).
\]

Thus spontaneous symmetry breaking is a reorganization of the quotient structure.

\[
\boxed{
\text{Symmetry breaking is a change in orbit-stabilizer structure, not a violation of admissibility.}
}
\]

---

## 15. Quantum Reference Transformations

Reference Transformation Theory also applies to quantum frameworks.

Let \(\mathcal H_1\) and \(\mathcal H_2\) be Hilbert spaces carrying admissibility representations

\[
\rho_1:G_1\to U(\mathcal H_1),
\]

\[
\rho_2:G_2\to U(\mathcal H_2).
\]

The physical quantum state spaces are projective quotients

\[
Q_1=\mathbb P(\mathcal H_1)/G_1,
\]

\[
Q_2=\mathbb P(\mathcal H_2)/G_2.
\]

A quantum reference transformation may be induced by a linear map

\[
U:\mathcal H_1\to\mathcal H_2
\]

satisfying an intertwining condition

\[
\boxed{
U\rho_1(g)=\rho_2(\alpha(g))U
}
\]

for a group homomorphism

\[
\alpha:G_1\to G_2.
\]

Then \(U\) maps \(G_1\)-orbits in \(\mathbb P(\mathcal H_1)\) to \(G_2\)-orbits in \(\mathbb P(\mathcal H_2)\), inducing

\[
\Phi:Q_1\to Q_2.
\]

If \(U\) is unitary and invertible, the quantum frameworks are unitarily equivalent.

If \(U\) is not invertible, it may describe a reduction, projection, decoherence-free sector embedding, or classical limit.

---

## 16. Quantum Reference Frames

A quantum reference frame is a physical system used to define relational descriptions.

Let the total Hilbert space be

\[
\mathcal H_{\rm tot}
=
\mathcal H_S\otimes\mathcal H_R,
\]

where \(S\) is a system and \(R\) is a reference system.

Suppose \(G\) acts diagonally:

\[
U_{\rm tot}(g)
=
U_S(g)\otimes U_R(g).
\]

Physical states satisfy

\[
U_{\rm tot}(g)|\Psi\rangle=|\Psi\rangle.
\]

Changing from the perspective of one quantum reference frame to another is a reference transformation between relational description spaces.

At the quotient level, one studies maps

\[
\Phi:
(\mathcal H_S\otimes\mathcal H_R)/G
\to
(\mathcal H_S\otimes\mathcal H_{R'})/G.
\]

Such maps may be implemented by unitary changes of reference system, conditioning maps, or perspective-neutral transformations.

Thus quantum reference-frame transformations are a special class of Reference Transformation Theory.

---

## 17. Classical Limit as Reference Transformation

The classical limit of quantum theory may also be understood as a reference transformation.

Let

\[
Q_{\rm quantum}
=
\mathbb P(\mathcal H)/G,
\]

and let

\[
Q_{\rm classical}
\]

be a classical phase space or orbit space.

A semiclassical map may associate coherent states \(|\alpha\rangle\) to phase-space points \(z\in Q_{\rm classical}\):

\[
z\mapsto [|\alpha(z)\rangle].
\]

In the opposite direction, a classical limit map may send quantum orbits to classical orbits:

\[
\Phi_{\hbar}:Q_{\rm quantum}\to Q_{\rm classical},
\]

with

\[
\hbar\to0.
\]

This map is usually singular and requires appropriate quotienting, coarse-graining, or decoherence.

Thus quantization and classicalization are not merely formal procedures. They are reference transformations between different admissibility frameworks.

---

## 18. Dualities as Reference Equivalences

A duality is an isomorphism between physical quotients:

\[
\Phi:Q_1\to Q_2,
\]

such that:

1. \(\Phi\) is invertible,
2. \(\Phi^*\) is an isomorphism of observable algebras,
3. dynamics is conjugate,
4. probabilities or expectation values are preserved.

The two frameworks may have different description spaces:

\[
\Omega_1\neq\Omega_2,
\]

different admissibility groups:

\[
G_1\neq G_2,
\]

and different representative variables.

But their physical orbit spaces are equivalent.

Examples include:

- position-momentum duality,
- bosonization,
- mirror symmetry,
- T-duality,
- S-duality,
- AdS/CFT-type holographic dualities.

In Reference Transformation Theory, a duality is not an identity of descriptions. It is an isomorphism of orbit structures.

\[
\boxed{
\text{Dual theories have equivalent orbit spaces but inequivalent description spaces.}
}
\]

---

## 19. String Dualities as Reference Transformations

In string theory, the description space includes worldsheet embeddings, metrics, and background fields:

\[
\Omega_{\rm str}
=
\{X,h_{ab},G_{\mu\nu},B_{\mu\nu},\Phi,\dots\}.
\]

The admissibility group includes worldsheet diffeomorphisms and Weyl transformations:

\[
G_{\rm ws}
=
\operatorname{Diff}(\Sigma)\ltimes\operatorname{Weyl}(\Sigma).
\]

String dualities introduce additional identifications. For example, T-duality identifies a string compactified on a circle of radius \(R\) with one compactified on radius

\[
R'=\frac{\alpha'}{R}.
\]

At the level of physical moduli, T-duality is an automorphism or equivalence of the quotient space.

Thus string dualities are reference transformations that enlarge the admissibility structure by identifying apparently distinct backgrounds.

---

## 20. Reference Transformations and Observers

Observer Theory and Reference Transformation Theory are closely related.

An observer is a map

\[
O:\Omega\to D_O.
\]

A transformation between observers

\[
O_1:\Omega\to D_1,
\]

\[
O_2:\Omega\to D_2
\]

is a map

\[
T:D_1\to D_2
\]

such that

\[
O_2=T\circ O_1.
\]

This is a reference transformation between observer description spaces.

If \(T\) is equivariant, the transformation preserves admissibility.

If \(T\) is invertible, the observers are equivalent.

If no such \(T\) exists, the observers are fundamentally inequivalent.

Thus Reference Transformation Theory provides the mathematical language for comparing observers.

---

## 21. Reference Transformations and Constraints

In constrained systems, the physical quotient is formed from a constraint surface.

Let

\[
\Sigma_i\subset\Omega_i
\]

be the constraint surfaces, and let \(G_i\) be the gauge groups generated by first-class constraints.

The physical spaces are

\[
Q_i=\Sigma_i/G_i.
\]

A reference transformation between constrained frameworks is a map

\[
\Phi:\Sigma_1/G_1\to\Sigma_2/G_2.
\]

It must preserve admissibility:

\[
\Phi([\omega_1])=[F(\omega_1)]
\]

with

\[
F(\Sigma_1)\subset\Sigma_2.
\]

At the level of constraints, one often has a map between constraint algebras:

\[
\alpha:\mathfrak g_1\to\mathfrak g_2.
\]

If the constraints are mapped consistently, the reference transformation descends to the physical quotients.

This is essential for reductions, gauge fixing, and quantization.

---

## 22. Probabilistic Reference Transformations

When physical states are probability measures on quotient spaces, a reference transformation must also transform states.

Let

\[
\mu_1
\]

be a probability measure on \(Q_1\). A reference transformation

\[
\Phi:Q_1\to Q_2
\]

pushes it forward to a measure on \(Q_2\):

\[
\mu_2=\Phi_*\mu_1.
\]

For any observable \(f_2\in C^\infty(Q_2)\),

\[
\int_{Q_2} f_2\,d\mu_2
=
\int_{Q_1} (f_2\circ\Phi)\,d\mu_1.
\]

Thus expectation values are preserved under the pullback-pushforward pair.

In quantum theory, the analogous structure is given by completely positive maps, pullbacks of POVMs, or algebra homomorphisms.

---

## 23. Conditions for a Good Reference Transformation

A physically meaningful reference transformation should satisfy several conditions.

### 23.1 Well-definedness on orbits

It must not depend on representatives.

### 23.2 Compatibility with admissibility

It should be induced by equivariant data when possible.

### 23.3 Compatibility with observables

It should pull back physical observables to physical observables:

\[
\Phi^*:C^\infty(Q_2)\to C^\infty(Q_1).
\]

### 23.4 Compatibility with dynamics

It should intertwine physical flows:

\[
\Phi\circ\varphi_t^{(1)}
=
\varphi_t^{(2)}\circ\Phi.
\]

### 23.5 Compatibility with probabilities

It should map states consistently:

\[
\mu_2=\Phi_*\mu_1.
\]

### 23.6 Compatibility with quantum structure

In quantum settings, it should preserve transition probabilities, expectation values, or algebraic relations.

A transformation satisfying all relevant conditions is an admissible reference transformation.

---

## 24. Equivalence of Physical Frameworks

Two physical frameworks are equivalent if there exists a reference transformation

\[
\Phi:Q_1\to Q_2
\]

such that:

1. \(\Phi\) is invertible,
2. \(\Phi^*\) is an isomorphism of observable algebras,
3. dynamics is conjugate,
4. state spaces are mapped consistently,
5. stabilizer or stacky data are preserved if relevant.

In that case,

\[
\boxed{
\mathcal R_1\simeq\mathcal R_2.
}
\]

The two frameworks may use different variables, different groups, and different description spaces, but they encode the same physical orbit structure.

Thus equivalence of theories is not equality of descriptions. It is isomorphism of quotients.

---

## 25. Reference Transformation Theory Within Relativity Mechanics

Reference Transformation Theory occupies a central place in the Relativity Mechanics architecture.

- Orbit Theory gives objects: orbits.
- Invariant Theory gives observables: invariants.
- Observer Theory gives access: observer maps.
- Reference Transformation Theory gives relations between frameworks: quotient maps.

Without Reference Transformation Theory, Relativity Mechanics could describe a single admissibility framework but not transformations between frameworks.

With Reference Transformation Theory, Relativity Mechanics becomes a meta-theory capable of describing:

1. frame changes,
2. gauge changes,
3. observer changes,
4. theory reductions,
5. physical limits,
6. dualities,
7. symmetry breaking,
8. quantization,
9. classicalization,
10. unification maps.

Thus Reference Transformation Theory is the categorical layer of Relativity Mechanics.

---

## 26. Summary of the Formal Structure

Given two admissibility structures

\[
\mathcal A_1=(\Omega_1,G_1),
\qquad
\mathcal A_2=(\Omega_2,G_2),
\]

their physical quotients are

\[
Q_1=\Omega_1/G_1,
\qquad
Q_2=\Omega_2/G_2.
\]

A reference transformation is

\[
\boxed{
\Phi:Q_1\to Q_2.
}
\]

A representable reference transformation arises from a pair

\[
(F,\alpha),
\]

where

\[
F:\Omega_1\to\Omega_2,
\]

\[
\alpha:G_1\to G_2,
\]

and

\[
\boxed{
F(g\cdot\omega)=\alpha(g)\cdot F(\omega).
}
\]

Then

\[
\boxed{
\Phi([\omega])=[F(\omega)].
}
\]

Observables transform by pullback:

\[
\boxed{
\Phi^*:C^\infty(Q_2)\to C^\infty(Q_1).
}
\]

Dynamics transforms by conjugacy:

\[
\boxed{
\Phi\circ\varphi_t^{(1)}
=
\varphi_t^{(2)}\circ\Phi.
}
\]

States transform by pushforward:

\[
\boxed{
\mu_2=\Phi_*\mu_1.
}
\]

Framework equivalence is an invertible reference transformation preserving all physical structure.

---

## 27. Conclusion

Reference Transformation Theory answers the structural question:

\[
\boxed{
\text{How are different physical frameworks related?}
}
\]

The answer is:

\[
\boxed{
\text{By maps between their orbit spaces.}
}
\]

Given two admissibility groups \(G_1\) and \(G_2\), the central object of study is

\[
\boxed{
\Phi:\Omega_1/G_1\to\Omega_2/G_2.
}
\]

Such maps describe changes of reference, changes of theory, reductions, limits, dualities, and equivalences. They may be induced by equivariant maps between description spaces, by group homomorphisms, by inclusions or enlargements of admissibility groups, or by singular limiting procedures.

Reference Transformation Theory thus completes the relational architecture of Relativity Mechanics. Orbit Theory tells us what physical objects are. Invariant Theory tells us what can be measured. Observer Theory tells us how observers access descriptions. Reference Transformation Theory tells us how entire frameworks of description are related.

The central principle is:

\[
\boxed{
\text{A change of physical framework is a well-defined transformation between equivalence classes of admissible descriptions.}
}
\]
