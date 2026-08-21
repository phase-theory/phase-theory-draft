# Universal Mathematical Evolution Theory

## A Formal Framework for Generative Dynamics of Mathematical Structures

**Preprint**

---

## Abstract

We develop **Universal Mathematical Evolution Theory** (UMET), a formal framework in which mathematical structures are not treated as static objects but as states in a generative dynamical landscape. The central object is a universal evolution operator

\[
\mathfrak{U}:\mathcal{M}\longrightarrow \mathcal{M},
\]

where \(\mathcal{M}\) denotes a universe-bounded category of admissible mathematical structures. Structures evolve by universal generative laws governing generation, stability, interaction, specialization, and emergence. We construct \(\mathfrak{U}\) as a free monadic closure over a primitive generative endofunctor, thereby giving a precise categorical semantics for structural evolution. We define evolution trajectories, universal invariants, evolutionary fixed points, and structural phase transitions. A linearized tensor calculus for evolutionary dynamics is introduced, allowing spectral, probabilistic, and thermodynamic analyses of structural evolution. Classical mathematical domains — algebra, topology, geometry, analysis, logic, probability, and category theory — are interpreted as phases within a unified evolutionary landscape. Applications include foundations of mathematics, automated theorem discovery, artificial intelligence, complex systems, mathematical physics, and formal scientific modeling.

**Keywords:** universal evolution, mathematical structures, monads, categorical dynamics, structural invariants, fixed points, phase transitions, foundations of mathematics, automated theorem discovery.

---

## 1. Introduction

Classical foundations of mathematics have largely been formulated as ontologies of stable objects: sets, types, categories, structures, theories, or models. Even when change appears — through construction, completion, classification, deformation, or proof — it is usually treated as an external operation performed on already constituted objects.

Universal Mathematical Evolution Theory proposes a reversal of emphasis. Instead of asking first *what mathematical objects are*, we ask:

> **By what universal laws do mathematical structures generate, transform, stabilize, interact, specialize, and give rise to new structures?**

In UMET, mathematical structures are treated as **structural states** inside an evolutionary landscape. The evolution is not physical time but a formal generative ordering: one structure may give rise to another by completion, quotient, enrichment, categorification, internalization, extension, or emergence of new sorts and operations.

The central primitive object is the universal evolution operator

\[
\mathfrak{U}:\mathcal{M}\longrightarrow \mathcal{M},
\]

where \(\mathcal{M}\) is a category of admissible mathematical structures. The operator \(\mathfrak{U}\) assigns to a structure its **universal evolutionary envelope**, namely the coherent totality of admissible one-step generative transformations of that structure. Individual evolutionary branches are obtained by admissible specializations, quotients, or projections of \(\mathfrak{U}(S)\).

UMET is built around six primitive notions:

1. **Evolution operators**: functors, monads, or transition systems generating structural change.
2. **Structural states**: mathematical structures regarded as points or objects in \(\mathcal{M}\).
3. **Evolution trajectories**: chains, graphs, or flows of structural states under evolution.
4. **Universal invariants**: functors or quantities preserved by admissible evolution.
5. **Evolutionary fixed points**: structures closed under the universal evolution operator.
6. **Structural phase transitions**: singular changes in evolutionary behavior, invariant structure, or limit formation.

The purpose of this paper is to give a rigorous formal architecture for these notions, to prove basic existence and stability theorems, and to show how standard mathematical disciplines appear as phases of a single generative dynamics.

---

## 2. The Universe of Admissible Structures

A universal theory of all mathematical structures cannot be naively formulated over the absolute totality of all structures without encountering size-theoretic paradoxes. We therefore work relative to a fixed Grothendieck universe or inaccessible cardinal. This is not a philosophical restriction but a standard foundational device. Extensions to larger universes are obtained by changing the universe parameter.

Fix a strongly inaccessible cardinal \(\kappa\). Let \(V_\kappa\) denote the corresponding universe of \(\kappa\)-small sets.

### 2.1 Signatures and structural states

We use a flexible many-sorted, possibly higher-order, notion of signature. This permits algebraic, logical, topological, geometric, analytic, probabilistic, and categorical structures to be represented uniformly.

**Definition 2.1.** A **signature** \(\Sigma\) is a tuple

\[
\Sigma=(\mathsf{Sorts}_\Sigma,\mathsf{Ops}_\Sigma,\mathsf{Rels}_\Sigma,\mathsf{Types}_\Sigma)
\]

where:

- \(\mathsf{Sorts}_\Sigma\) is a \(\kappa\)-small set of sorts;
- \(\mathsf{Ops}_\Sigma\) is a set of function symbols with specified arities
  \[
  f:(s_1,\dots,s_n)\to s;
  \]
- \(\mathsf{Rels}_\Sigma\) is a set of relation symbols with specified arities
  \[
  R\subseteq s_1\times\cdots\times s_n;
  \]
- \(\mathsf{Types}_\Sigma\) optionally encodes higher-order type constructors, dependent types, power sorts, function-space constructors, or categorical structure.

A signature may encode, for example, the language of groups, topological spaces, metric spaces, measure spaces, first-order theories, categories, or higher categories.

**Definition 2.2.** A **structural state** \(S\) is a tuple

\[
S=(\Sigma_S, |S|, I_S, \mathcal{A}_S),
\]

where:

- \(\Sigma_S\) is a signature;
- \(|S|=(|S|_s)_{s\in \mathsf{Sorts}_\Sigma}\) is a family of \(\kappa\)-small carriers;
- \(I_S\) interprets the operation, relation, and type symbols of \(\Sigma_S\) on \(|S|\);
- \(\mathcal{A}_S\) is a set of axioms, axiom schemata, or structural conditions imposed on \(S\).

A structural state is therefore a presented mathematical structure together with its adopted axiomatic regime.

This formulation intentionally includes both semantic structures and their presentations. In many applications it is useful to treat a mathematical object not merely as a model but as a pair consisting of a syntax/signature and a compatible interpretation.

### 2.2 The category of structures

Let \(\mathbf{Str}_\kappa\) be the category whose objects are \(\kappa\)-small structural states and whose morphisms are structure-preserving interpretations.

A morphism

\[
F:S\longrightarrow T
\]

consists of:

1. a translation of signatures
   \[
   F_\Sigma:\Sigma_S\longrightarrow \Sigma_T;
   \]
2. maps on carriers
   \[
   F_s:|S|_s\longrightarrow |T|_{F_\Sigma(s)};
   \]
3. preservation of operations, relations, and type constructors;
4. compatibility with axioms, meaning that the image of the axioms of \(S\) is valid in \(T\), or that \(F\) is an interpretation of \(S\) inside \(T\).

We denote by

\[
\mathcal{M}:=\operatorname{Obj}(\mathbf{Str}_\kappa)
\]

the class of admissible structures in the chosen universe. In categorical arguments we work directly with \(\mathbf{Str}_\kappa\).

For the existence theorems below we assume either that \(\mathbf{Str}_\kappa\) itself is locally presentable, or that we have fixed a locally presentable subcategory of \(\mathbf{Str}_\kappa\) determined by a chosen generative signature. This is a standard and mild technical assumption.

---

## 3. The Universal Evolution Operator

### 3.1 Primitive generative endofunctors

Evolution in UMET is generated by primitive structural operations. These are the elementary laws by which one structure gives rise to another.

Typical primitive operations include:

1. **Free extension**:
   \[
   \Gamma_{\mathrm{free}}(S)
   \]
   freely adds operations, terms, or generators.

2. **Quotient or specialization**:
   \[
   \Gamma_{\mathrm{quot}}(S)
   \]
   imposes equations, identifications, or additional axioms.

3. **Completion**:
   \[
   \Gamma_{\mathrm{comp}}(S)
   \]
   adds limits, Cauchy completions, Dedekind completions, compactifications, or colimits.

4. **Product and coproduct formation**:
   \[
   \Gamma_{\times}(S),\qquad \Gamma_{\amalg}(S)
   \]
   produce composite or alternative structures.

5. **Internalization**:
   \[
   \Gamma_{\mathrm{int}}(S)
   \]
   forms function spaces, power objects, endomorphism structures, or internal languages.

6. **Categorification**:
   \[
   \Gamma_{\mathrm{cat}}(S)
   \]
   promotes objects to morphisms, structures to categories, or categories to higher categories.

7. **Emergent extension**:
   \[
   \Gamma_{\mathrm{em}}(S)
   \]
   introduces new sorts, operations, or relations not definable from the old core.

Collect these primitive operations into a single generative endofunctor

\[
\Gamma:\mathbf{Str}_\kappa\longrightarrow \mathbf{Str}_\kappa.
\]

In the simplest case,

\[
\Gamma
=
\Gamma_{\mathrm{free}}
\amalg
\Gamma_{\mathrm{quot}}
\amalg
\Gamma_{\mathrm{comp}}
\amalg
\Gamma_{\times}
\amalg
\Gamma_{\mathrm{int}}
\amalg
\Gamma_{\mathrm{cat}}
\amalg
\Gamma_{\mathrm{em}}.
\]

More generally, \(\Gamma\) may be a weighted or indexed sum of primitive operations. The precise choice of \(\Gamma\) determines a particular evolutionary regime. UMET itself is the study of the universal dynamics generated by such \(\Gamma\).

We require \(\Gamma\) to be \(\kappa\)-accessible. Intuitively, this means that the primitive generative laws are determined by their action on \(\kappa\)-small presentations and commute with sufficiently filtered colimits.

### 3.2 The universal evolution operator as a free monad

The universal evolution operator is not merely a single application of a primitive rule. It must encode the coherent totality of all iterated generative transformations.

We therefore define \(\mathfrak{U}\) as the **free monad** on the primitive generative endofunctor \(\Gamma\).

**Definition 3.1.** A **universal evolution operator** on \(\mathbf{Str}_\kappa\) is a monad

\[
(\mathfrak{U},\eta,\mu)
\]

together with a natural transformation

\[
\iota:\Gamma\longrightarrow \mathfrak{U},
\]

such that \((\mathfrak{U},\eta,\mu,\iota)\) is initial among all monads \(M\) equipped with a natural transformation \(\Gamma\to M\).

Thus \(\mathfrak{U}\) is the universal coherent closure of structures under the primitive generative operations encoded by \(\Gamma\).

The unit

\[
\eta_S:S\longrightarrow \mathfrak{U}(S)
\]

embeds a structure into its evolutionary envelope. The multiplication

\[
\mu_S:\mathfrak{U}(\mathfrak{U}(S))\longrightarrow \mathfrak{U}(S)
\]

flattens iterated evolution into a single coherent evolutionary stage.

The monad laws are:

\[
\mu_S\circ \eta_{\mathfrak{U}(S)}=\mathrm{id}_{\mathfrak{U}(S)},
\]

\[
\mu_S\circ \mathfrak{U}(\eta_S)=\mathrm{id}_{\mathfrak{U}(S)},
\]

\[
\mu_S\circ \mu_{\mathfrak{U}(S)}
=
\mu_S\circ \mathfrak{U}(\mu_S).
\]

The universal recursion equation satisfied by \(\mathfrak{U}\) is

\[
\mathfrak{U}(S)\cong S\amalg \Gamma(\mathfrak{U}(S)).
\]

A point of \(\mathfrak{U}(S)\) is therefore either the original structure \(S\) or the result of applying a primitive generative operation to an already evolved structure.

### 3.3 Existence and universality

**Theorem 3.1.** Let \(\mathbf{Str}_\kappa\) be locally \(\kappa\)-presentable and let

\[
\Gamma:\mathbf{Str}_\kappa\longrightarrow \mathbf{Str}_\kappa
\]

be a \(\kappa\)-accessible endofunctor. Then the free monad \(\mathfrak{U}\) on \(\Gamma\) exists. Moreover, \(\mathfrak{U}\) is initial among monads equipped with a natural transformation from \(\Gamma\).

**Proof.** Consider the transfinite construction

\[
T_0=\mathrm{Id},
\]

\[
T_{\alpha+1}=\mathrm{Id}+\Gamma\circ T_\alpha,
\]

and for a limit ordinal \(\lambda\),

\[
T_\lambda=\operatorname*{colim}_{\alpha<\lambda}T_\alpha.
\]

Because \(\Gamma\) is \(\kappa\)-accessible and \(\mathbf{Str}_\kappa\) is locally \(\kappa\)-presentable, this chain stabilizes at a sufficiently large regular ordinal. Its colimit \(T\) carries a canonical natural transformation

\[
\Gamma\circ T\longrightarrow T
\]

and a unit

\[
\mathrm{Id}\longrightarrow T.
\]

By initiality of the constructed algebra, \(T\) extends uniquely to a monad \(\mathfrak{U}\). The multiplication is induced by the unique homomorphism

\[
\mathfrak{U}(\mathfrak{U}(S))\longrightarrow \mathfrak{U}(S)
\]

given by the algebra structure on \(\mathfrak{U}(S)\). The monad laws follow from uniqueness of homomorphisms into initial algebras.

For initiality among monads, suppose \(M\) is a monad with a natural transformation

\[
\alpha:\Gamma\longrightarrow M.
\]

Then for each \(S\), the structure

\[
S+\Gamma(M(S))\longrightarrow M(S)
\]

is given by the unit of \(M\) and the composite

\[
\Gamma(M(S))
\xrightarrow{\alpha_{M(S)}}
M(M(S))
\xrightarrow{\mu_S}
M(S).
\]

By initiality of \(\mathfrak{U}(S)\), this induces a unique natural transformation

\[
\mathfrak{U}(S)\longrightarrow M(S).
\]

These maps assemble into a monad morphism. Hence \(\mathfrak{U}\) is universal. \(\square\)

This theorem provides the formal foundation of UMET: once primitive generative laws are specified, there exists a universal coherent evolutionary closure.

### 3.4 Successors, trajectories, and the evolutionary landscape

The monadic operator \(\mathfrak{U}\) gives a deterministic universal envelope. Individual evolutionary paths are obtained by taking admissible specializations of that envelope.

**Definition 3.2.** An **admissible successor** of a structure \(S\) is a structure \(T\) equipped with an admissible quotient or projection

\[
q:\mathfrak{U}(S)\twoheadrightarrow T
\]

such that the composite

\[
S\xrightarrow{\eta_S}\mathfrak{U}(S)\xrightarrow{q}T
\]

is an admissible evolutionary extension of \(S\).

We write

\[
T\in \operatorname{Succ}(S)
\]

if \(T\) is an admissible successor of \(S\).

The **evolutionary graph** of \(\mathcal{M}\) is the directed class whose vertices are isomorphism classes of structures and whose edges are admissible successor relations:

\[
S\longrightarrow T
\quad\Longleftrightarrow\quad
T\in \operatorname{Succ}(S).
\]

Weights may be assigned to edges if one wishes to study probabilistic or statistical evolution.

**Definition 3.3.** A **discrete evolution trajectory** is a sequence

\[
S_0,S_1,S_2,\dots
\]

such that

\[
S_{n+1}\in \operatorname{Succ}(S_n)
\]

for all \(n\).

A **transfinite trajectory** is an ordinal-indexed chain

\[
(S_\alpha)_{\alpha<\lambda}
\]

such that:

\[
S_{\alpha+1}\in \operatorname{Succ}(S_\alpha),
\]

and for limit ordinals \(\delta<\lambda\),

\[
S_\delta\cong \operatorname*{colim}_{\alpha<\delta}S_\alpha
\]

whenever the colimit exists.

The evolutionary landscape is therefore a directed generative space, possibly branching, whose paths are mathematical histories.

**Definition 3.4.** The **evolutionary distance** from \(S\) to \(T\) is

\[
d(S,T)=\min\{n\in\mathbb{N}:T\in \operatorname{Succ}^n(S)\},
\]

if such an \(n\) exists, and \(d(S,T)=\infty\) otherwise.

Weighted versions may be defined using costs, complexities, or probabilities assigned to primitive generative operations.

---

## 4. Axioms of Universal Evolution

We now state the universal generative laws governing UMET. These axioms are structural rather than domain-specific. They express the minimal formal behavior required of a universal evolutionary dynamics.

Let

\[
\mathfrak{U}:\mathbf{Str}_\kappa\longrightarrow \mathbf{Str}_\kappa
\]

be the universal evolution operator.

### Axiom UMET-I: Generation

For every admissible structure \(S\), the unit

\[
\eta_S:S\longrightarrow \mathfrak{U}(S)
\]

is an admissible evolutionary extension.

Moreover, unless \(S\) is evolutionarily terminal, there exists at least one proper admissible successor

\[
T\in \operatorname{Succ}(S)
\]

such that \(T\not\cong S\).

In equations:

\[
S\leq \mathfrak{U}(S),
\]

where \(\leq\) denotes the relation of admissible extension.

This axiom asserts that every structure possesses a nontrivial generative horizon.

### Axiom UMET-II: Coherent Stability

There exists a **core functor**

\[
\mathsf{C}:\mathbf{Str}_\kappa\longrightarrow \mathbf{Str}_\kappa
\]

and a natural monomorphism

\[
c_S:\mathsf{C}(S)\hookrightarrow S
\]

such that stable evolution preserves the core:

\[
\mathsf{C}(\mathfrak{U}_{\mathrm{st}}(S))\cong \mathsf{C}(S).
\]

Here \(\mathfrak{U}_{\mathrm{st}}\) denotes the stable part of evolution generated by non-emergent primitive operations.

Equivalently, for every stable successor

\[
q:S\to T,
\]

the induced map

\[
\mathsf{C}(S)\longrightarrow \mathsf{C}(T)
\]

is an isomorphism.

This axiom formalizes the fact that genuine evolution may transform a structure while preserving an invariant structural identity.

### Axiom UMET-III: Interaction

Assume \(\mathbf{Str}_\kappa\) is equipped with a monoidal product

\[
\otimes:\mathbf{Str}_\kappa\times \mathbf{Str}_\kappa\longrightarrow \mathbf{Str}_\kappa.
\]

Then evolution of composite structures is not necessarily the mere product of individual evolutions. There is a natural comparison map

\[
\chi_{S,T}:
\mathfrak{U}(S)\otimes \mathfrak{U}(T)
\longrightarrow
\mathfrak{U}(S\otimes T).
\]

The failure of \(\chi_{S,T}\) to be an isomorphism defines an **interaction structure**

\[
\mathsf{I}(S,T)
=
\operatorname{cofib}(\chi_{S,T})
\]

in an exact or abelian envelope of \(\mathbf{Str}_\kappa\).

Schematically:

\[
0
\longrightarrow
\mathfrak{U}(S)\otimes \mathfrak{U}(T)
\longrightarrow
\mathfrak{U}(S\otimes T)
\longrightarrow
\mathsf{I}(S,T)
\longrightarrow
0.
\]

In tensor notation, if the evolution of a simple structure has components \(U^a{}_b\), then the evolution of a composite system has components

\[
U^{ab}{}_{cd}
=
U^a{}_c U^b{}_d
+
I^{ab}{}_{cd},
\]

where \(I^{ab}{}_{cd}\) is the interaction tensor.

This axiom encodes the emergence of correlations, entanglements, and new relational laws in composite mathematical systems.

### Axiom UMET-IV: Specialization

Let

\[
\pi:S\longrightarrow R
\]

be a specialization morphism, for example a quotient, forgetful map, restriction, or reduct.

Then there is an induced specialization of evolutionary envelopes

\[
\mathfrak{U}(\pi):\mathfrak{U}(S)\longrightarrow \mathfrak{U}(R)
\]

such that the diagram

\[
\begin{array}{ccc}
S & \xrightarrow{\eta_S} & \mathfrak{U}(S) \\
\downarrow \pi & & \downarrow \mathfrak{U}(\pi) \\
R & \xrightarrow{\eta_R} & \mathfrak{U}(R)
\end{array}
\]

commutes.

If \(\pi\) is a quotient, then \(\mathfrak{U}(\pi)\) is again a quotient. Thus specialization and evolution are compatible.

This axiom says that simplifying or restricting a structure before evolving is coherently related to evolving before simplifying.

### Axiom UMET-V: Emergence

There exist structures \(S\) and admissible successors

\[
T\in \operatorname{Succ}(S)
\]

such that the core of \(T\) is not isomorphic to any stable extension of the core of \(S\):

\[
\mathsf{C}(T)\not\cong \mathsf{C}(S')
\]

for every stable extension \(S'\) of \(S\).

Equivalently, \(T\) contains new sorts, operations, relations, or type constructors that are not definable from the stable core of \(S\).

This axiom guarantees that UMET is not merely a theory of deformation or conservative extension. It allows genuinely new mathematical structure to arise.

---

## 5. Evolutionary Dynamics and Fixed Points

### 5.1 The partial order of structural extension

Define a preorder on structures by

\[
S\leq T
\]

if there exists an admissible extension morphism

\[
S\longrightarrow T.
\]

Passing to isomorphism classes gives a partially ordered class.

The universal evolution operator is inflationary:

\[
S\leq \mathfrak{U}(S).
\]

It is also monotone: if \(S\leq T\), then

\[
\mathfrak{U}(S)\leq \mathfrak{U}(T).
\]

This monotonicity follows from functoriality.

### 5.2 Existence of evolutionary fixed points

A structure \(S\) is an **evolutionary fixed point** if

\[
\mathfrak{U}(S)\cong S.
\]

More precisely, we require an isomorphism

\[
\theta:\mathfrak{U}(S)\xrightarrow{\sim} S
\]

such that

\[
\theta\circ \eta_S=\mathrm{id}_S.
\]

Such a structure is closed under universal evolution.

**Theorem 5.1.** Let \((P,\leq)\) be a chain-complete poset of isomorphism classes of admissible structures. Suppose

\[
\mathfrak{U}:P\longrightarrow P
\]

is monotone and inflationary:

\[
x\leq \mathfrak{U}(x).
\]

Then for every \(x\in P\), there exists a fixed point \(p\in P\) such that

\[
x\leq p,
\qquad
\mathfrak{U}(p)=p.
\]

**Proof.** This is the Bourbaki–Witt fixed-point theorem. Define a transfinite chain:

\[
x_0=x,
\]

\[
x_{\alpha+1}=\mathfrak{U}(x_\alpha),
\]

and for limit ordinals \(\lambda\),

\[
x_\lambda=\sup_{\alpha<\lambda}x_\alpha.
\]

Because \(P\) is chain-complete, each limit supremum exists. Since \(\mathfrak{U}\) is inflationary and monotone, the chain is increasing. If the chain never stabilizes, it yields a strictly increasing proper class of elements, contradicting the set-boundedness of \(P\) inside the chosen universe. Hence there exists an ordinal \(\alpha\) such that

\[
x_{\alpha+1}=x_\alpha.
\]

Then

\[
\mathfrak{U}(x_\alpha)=x_\alpha.
\]

Taking \(p=x_\alpha\) gives the result. \(\square\)

**Corollary 5.1.** If the poset of structures under conservative extension has cardinality at most \(\lambda\), then every monotone inflationary evolution operator reaches a fixed point by some ordinal \(<\lambda^+\).

### 5.3 Limit continuity and fixed-point formation

Let

\[
S_0\longrightarrow S_1\longrightarrow S_2\longrightarrow\cdots
\]

be a trajectory with

\[
S_{n+1}=\mathfrak{U}(S_n).
\]

Let

\[
S_\omega=\operatorname*{colim}_{n<\omega}S_n.
\]

**Theorem 5.2.** If \(\mathfrak{U}\) preserves the colimit of the chain \((S_n)\), then \(S_\omega\) is an evolutionary fixed point.

**Proof.** We compute:

\[
\mathfrak{U}(S_\omega)
=
\mathfrak{U}\left(\operatorname*{colim}_{n<\omega}S_n\right)
\cong
\operatorname*{colim}_{n<\omega}\mathfrak{U}(S_n).
\]

But

\[
\mathfrak{U}(S_n)=S_{n+1}.
\]

Therefore

\[
\mathfrak{U}(S_\omega)
\cong
\operatorname*{colim}_{n<\omega}S_{n+1}.
\]

The shifted chain \((S_{n+1})_{n<\omega}\) is cofinal in \((S_n)_{n<\omega}\), so

\[
\operatorname*{colim}_{n<\omega}S_{n+1}
\cong
\operatorname*{colim}_{n<\omega}S_n
=
S_\omega.
\]

Hence

\[
\mathfrak{U}(S_\omega)\cong S_\omega.
\]

Thus \(S_\omega\) is a fixed point. \(\square\)

This result is fundamental: evolutionary fixed points often arise as limits of iterated generative processes.

---

## 6. Universal Invariants and Conservation Laws

Evolutionary invariants are the structural quantities preserved by admissible transformations.

**Definition 6.1.** An **evolutionary invariant** is a functor

\[
I:\mathbf{Str}_\kappa\longrightarrow \mathcal{D}
\]

such that for every admissible evolutionary step

\[
S\longrightarrow T,
\]

the induced morphism

\[
I(S)\longrightarrow I(T)
\]

is an isomorphism.

Equivalently, \(I\) is constant on connected components of the evolutionary graph.

A stronger condition is **universal invariance under \(\mathfrak{U}\)**:

\[
I\circ \mathfrak{U}\cong I.
\]

If \(I\) preserves the relevant colimits, then invariance under the primitive generator \(\Gamma\) implies invariance under the universal evolution operator \(\mathfrak{U}\).

**Theorem 6.1.** Suppose

\[
I\circ \Gamma\cong I.
\]

If \(I\) preserves the colimits used in the construction of \(\mathfrak{U}\), then

\[
I\circ \mathfrak{U}\cong I.
\]

**Proof.** The free monad \(\mathfrak{U}\) is built as a colimit of iterates of \(\Gamma\):

\[
\mathfrak{U}
\cong
\operatorname*{colim}_{n<\omega}
\left(
\mathrm{Id}
+
\Gamma
+
\Gamma^2
+
\cdots
+
\Gamma^n
\right),
\]

with coherent transition maps. If \(I\circ \Gamma\cong I\), then by induction

\[
I\circ \Gamma^n\cong I
\]

for all \(n\). Since \(I\) preserves the relevant colimits,

\[
I\circ \mathfrak{U}
\cong
\operatorname*{colim}_{n<\omega}I\circ \Gamma^n
\cong
I.
\]

Thus \(I\) is invariant under universal evolution. \(\square\)

### 6.1 Conservation along trajectories

**Theorem 6.2.** Let \(I\) be an evolutionary invariant and let

\[
S_0\longrightarrow S_1\longrightarrow S_2\longrightarrow\cdots
\]

be an evolution trajectory. Then there are canonical isomorphisms

\[
I(S_0)\cong I(S_1)\cong I(S_2)\cong\cdots.
\]

**Proof.** Each arrow \(S_n\to S_{n+1}\) is an admissible evolutionary step. By definition of invariant, the induced map

\[
I(S_n)\longrightarrow I(S_{n+1})
\]

is an isomorphism. Composing these isomorphisms gives canonical identifications along the trajectory. \(\square\)

This is the structural analogue of a conservation law.

### 6.2 Symmetries and Noetherian invariants

Let \(\operatorname{Aut}(\mathfrak{U})\) denote the group of natural automorphisms of the evolution operator \(\mathfrak{U}\). An automorphism

\[
\alpha:\mathfrak{U}\xrightarrow{\sim}\mathfrak{U}
\]

is a symmetry of the evolutionary dynamics.

Given such a symmetry, define the fixed subcategory

\[
\mathbf{Str}_\kappa^\alpha
\]

consisting of structures \(S\) for which the action of \(\alpha_S\) is trivial up to specified isomorphism.

**Proposition 6.1.** The fixed subcategory of a symmetry of \(\mathfrak{U}\) is evolutionarily invariant.

**Proof.** If \(S\) is fixed by \(\alpha\), then the evolutionary envelope \(\mathfrak{U}(S)\) inherits a compatible \(\alpha\)-fixed structure because \(\alpha\) is natural. Any admissible quotient or successor defined invariantly from \(\mathfrak{U}(S)\) remains fixed. Hence the property of being \(\alpha\)-fixed is preserved by evolution. \(\square\)

This gives a categorical analogue of Noether’s principle: symmetries of the evolutionary operator determine invariant structural sectors.

---

## 7. Structural Phase Transitions

A central novelty of UMET is the treatment of qualitative changes in mathematical structure as **phase transitions**.

### 7.1 Parameterized evolution

Let \(\Theta\) be a parameter space. A parameterized evolutionary system is a family of generative endofunctors

\[
\Gamma_\theta:\mathbf{Str}_\kappa\longrightarrow \mathbf{Str}_\kappa,
\qquad
\theta\in \Theta.
\]

Let

\[
\mathfrak{U}_\theta
\]

be the corresponding universal evolution operators.

Given an initial structure \(S_0\), define the evolutionary limit

\[
S_\infty(\theta)
=
\operatorname*{colim}_{n<\omega}
\mathfrak{U}_\theta^n(S_0),
\]

whenever the colimit exists.

Let

\[
O:\mathbf{Str}_\kappa\longrightarrow \mathcal{D}
\]

be an observable, for example a functor returning a cardinal, a homology theory, a spectrum, a logical theory, a complexity measure, or a categorical invariant.

### 7.2 Definition of phase transition

**Definition 7.1.** A **structural phase transition** occurs at \(\theta_c\in\Theta\) if the observable

\[
\theta\longmapsto O(S_\infty(\theta))
\]

fails to be continuous, smooth, analytic, or otherwise regular at \(\theta_c\), relative to the natural topology or order structure on \(\mathcal{D}\).

Equivalently, a phase transition occurs when

\[
O\left(\operatorname*{colim}_{n<\omega}
\mathfrak{U}_{\theta_c}^n(S_0)\right)
\neq
\operatorname*{colim}_{n<\omega}
O\left(\mathfrak{U}_{\theta_c}^n(S_0)\right),
\]

or when the limit structure \(S_\infty(\theta)\) changes its isomorphism type abruptly.

### 7.3 Continuity criterion

**Theorem 7.1.** Suppose:

1. \(\theta\mapsto \Gamma_\theta\) is continuous in the operator topology;
2. each \(\mathfrak{U}_\theta\) preserves the colimits defining \(S_\infty(\theta)\);
3. \(O\) preserves those colimits;
4. the colimits vary continuously with \(\theta\).

Then

\[
\theta\longmapsto O(S_\infty(\theta))
\]

is continuous.

Therefore, discontinuity of \(O(S_\infty(\theta))\) implies that at least one of the assumptions fails. Such a failure is the formal signature of a structural phase transition.

**Proof.** By definition,

\[
S_\infty(\theta)
=
\operatorname*{colim}_{n<\omega}
\mathfrak{U}_\theta^n(S_0).
\]

Applying \(O\), and using preservation of colimits,

\[
O(S_\infty(\theta))
\cong
\operatorname*{colim}_{n<\omega}
O(\mathfrak{U}_\theta^n(S_0)).
\]

If \(\theta\mapsto \Gamma_\theta\) is continuous, then so is \(\theta\mapsto \mathfrak{U}_\theta\), by the universal construction of \(\mathfrak{U}_\theta\) as a colimit of iterates of \(\Gamma_\theta\). Hence the right-hand side varies continuously, provided colimits vary continuously. Thus \(O(S_\infty(\theta))\) is continuous. \(\square\)

### 7.4 Spectral phase transitions

In the linearized theory developed below, evolution is represented by an operator

\[
\widehat{\mathfrak{U}}_\theta
\]

on a module generated by structures. If \(\widehat{\mathfrak{U}}_\theta\) is stochastic or compact, its long-time behavior is governed by its leading spectrum.

Let

\[
\Delta(\theta)
\]

denote the spectral gap between the leading eigenvalue and the rest of the spectrum. A phase transition may occur when

\[
\Delta(\theta_c)=0.
\]

In that case, relaxation to equilibrium becomes singular, and macroscopic structural reorganization may occur.

---

## 8. Linearized Tensor Calculus of Evolution

To analyze evolution quantitatively, we linearize the category of structures.

Let \(K\) be a field or semiring. Let \(K[\mathcal{M}]\) be the free \(K\)-module generated by isomorphism classes \([S]\) of admissible structures.

Write

\[
e_S
\]

for the basis vector associated with \(S\).

### 8.1 The evolutionary propagator

A weighted evolutionary system defines a linear operator

\[
\widehat{\mathfrak{U}}:K[\mathcal{M}]\longrightarrow K[\mathcal{M}]
\]

by

\[
\widehat{\mathfrak{U}}(e_S)
=
\sum_{T\in \operatorname{Succ}(S)}
w(T\mid S)e_T,
\]

where \(w(T\mid S)\in K\) is the weight, amplitude, or probability of the transition \(S\to T\).

In index notation,

\[
(\widehat{\mathfrak{U}})^T{}_S
=
w(T\mid S).
\]

A structural state vector is a formal sum

\[
p=\sum_S p^S e_S.
\]

Evolution acts by

\[
p'^{T}
=
\widehat{\mathfrak{U}}^T{}_S p^S,
\]

using Einstein summation convention.

For discrete time,

\[
p_{n+1}=\widehat{\mathfrak{U}}p_n.
\]

For continuous time, one may define a master equation

\[
\frac{d p^S}{dt}
=
L^S{}_T p^T,
\]

where \(L\) is an evolutionary generator, often of the form

\[
L=\widehat{\mathfrak{U}}-I.
\]

### 8.2 Invariants and fixed distributions

A covector

\[
\phi=\sum_S \phi_S e^S
\]

is an evolutionary invariant if

\[
\phi_T \widehat{\mathfrak{U}}^T{}_S
=
\phi_S.
\]

Equivalently,

\[
\phi \widehat{\mathfrak{U}}=\phi.
\]

A fixed distribution satisfies

\[
\widehat{\mathfrak{U}}^T{}_S p^S=p^T.
\]

Thus invariants are left eigenvectors with eigenvalue \(1\), while fixed structural distributions are right eigenvectors with eigenvalue \(1\).

### 8.3 Interaction tensor

Suppose structures decompose into component spaces indexed by \(i,j,\dots\). Let a composite structure have tensor coordinates

\[
s^{ij}.
\]

If two structures evolve independently, the composite evolution operator is the tensor product

\[
U^{i'j'}{}_{ij}
=
U_1^{i'}{}_{i}
U_2^{j'}{}_{j}.
\]

In the presence of interaction, we write

\[
U^{i'j'}{}_{ij}
=
U_1^{i'}{}_{i}
U_2^{j'}{}_{j}
+
J^{i'j'}{}_{ij},
\]

where

\[
J^{i'j'}{}_{ij}
\]

is the interaction tensor.

**Proposition 8.1.** If \(J=0\), product states remain product states. If \(J\neq 0\), initially uncorrelated structures may become correlated.

**Proof.** Let

\[
p^{ij}=a^i b^j.
\]

If \(J=0\), then

\[
p'^{i'j'}
=
U_1^{i'}{}_{i}
U_2^{j'}{}_{j}
a^i b^j
=
\left(U_1^{i'}{}_{i}a^i\right)
\left(U_2^{j'}{}_{j}b^j\right),
\]

which is again a product state.

If \(J\neq 0\), then

\[
p'^{i'j'}
=
\left(U_1^{i'}{}_{i}a^i\right)
\left(U_2^{j'}{}_{j}b^j\right)
+
J^{i'j'}{}_{ij}a^i b^j.
\]

The second term need not factorize. Therefore correlations can be generated. \(\square\)

This provides a precise tensorial criterion for emergent interaction.

### 8.4 Entropy and structural thermodynamics

Assume \(K=\mathbb{R}\) and that \(\widehat{\mathfrak{U}}\) is stochastic:

\[
\widehat{\mathfrak{U}}^T{}_S\geq 0,
\qquad
\sum_T \widehat{\mathfrak{U}}^T{}_S=1.
\]

Let \(p\) and \(q\) be probability distributions on structures. The relative entropy is

\[
D(p\|q)
=
\sum_S p^S\log\frac{p^S}{q^S}.
\]

Let

\[
p'=\widehat{\mathfrak{U}}p,
\qquad
q'=\widehat{\mathfrak{U}}q.
\]

**Theorem 8.1.** Relative entropy decreases under stochastic evolution:

\[
D(p'\|q')\leq D(p\|q).
\]

**Proof.** We have

\[
p'^T=\sum_S \widehat{\mathfrak{U}}^T{}_S p^S,
\qquad
q'^T=\sum_S \widehat{\mathfrak{U}}^T{}_S q^S.
\]

For each \(T\), define weights

\[
\lambda^T_S
=
\frac{\widehat{\mathfrak{U}}^T{}_S q^S}{q'^T}.
\]

Then \(\lambda^T_S\geq 0\) and \(\sum_S\lambda^T_S=1\). Moreover,

\[
\frac{p'^T}{q'^T}
=
\sum_S
\lambda^T_S
\frac{p^S}{q^S}.
\]

The function \(x\mapsto x\log x\) is convex. Hence

\[
\frac{p'^T}{q'^T}
\log
\frac{p'^T}{q'^T}
\leq
\sum_S
\lambda^T_S
\frac{p^S}{q^S}
\log
\frac{p^S}{q^S}.
\]

Multiplying by \(q'^T\) and summing over \(T\) gives

\[
D(p'\|q')
\leq
\sum_S
p^S
\log
\frac{p^S}{q^S}
=
D(p\|q).
\]

Thus relative entropy is nonincreasing. \(\square\)

If \(\widehat{\mathfrak{U}}\) is doubly stochastic and \(q\) is uniform, this implies that Shannon entropy

\[
H(p)=-\sum_S p^S\log p^S
\]

is nondecreasing.

This permits a thermodynamic interpretation of structural evolution.

### 8.5 Structural free energy

Given an energy functional

\[
E:\mathcal{M}\longrightarrow \mathbb{R},
\]

define the free energy of a distribution \(p\) by

\[
F(p)
=
\sum_S p^S E(S)
+
\beta^{-1}
\sum_S p^S\log p^S.
\]

If the evolutionary dynamics satisfies a detailed-balance condition with respect to the Gibbs distribution

\[
p_\beta(S)
=
\frac{1}{Z(\beta)}e^{-\beta E(S)},
\]

then \(F(p)\) decreases along trajectories. Critical points of \(F\) correspond to equilibrium structural phases.

---

## 9. Classical Mathematics as Evolutionary Phases

UMET does not replace classical branches of mathematics. It reinterprets them as stable phases inside a broader evolutionary landscape.

A **phase** is a region of the evolutionary landscape characterized by dominant invariants, dominant primitive operations, and typical fixed-point structures.

One may define a phase vector

\[
\Phi(S)
=
\left(
\Phi_{\mathrm{alg}}(S),
\Phi_{\mathrm{top}}(S),
\Phi_{\mathrm{geom}}(S),
\Phi_{\mathrm{an}}(S),
\Phi_{\mathrm{log}}(S),
\Phi_{\mathrm{prob}}(S),
\Phi_{\mathrm{cat}}(S)
\right),
\]

where each component measures the relative dominance of a structural regime.

### 9.1 Algebraic phase

In the algebraic phase, structures are dominated by operations and equations.

Primitive operations:

- free algebra generation;
- quotient by congruences;
- localization;
- completion with respect to ideals;
- passage to categories of modules.

Typical evolutionary path:

\[
\text{magma}
\longrightarrow
\text{semigroup}
\longrightarrow
\text{monoid}
\longrightarrow
\text{group}.
\]

Here evolution proceeds by adding axioms or freely adjoining inverses.

Universal invariants include:

- term algebras;
- congruence lattices;
- homological algebra invariants;
- Grothendieck groups.

Fixed points include algebraically closed fields, injective modules under appropriate closure operations, and complete local rings under completion.

### 9.2 Topological phase

In the topological phase, the dominant structure is a lattice of opens, a convergence structure, or a continuity regime.

Primitive operations:

- generation of topologies from subbases;
- quotient topologies;
- compactification;
- separation axiom refinement;
- sheafification.

Typical evolutionary path:

\[
\text{set}
\longrightarrow
\text{topological space}
\longrightarrow
\text{Hausdorff space}
\longrightarrow
\text{compact Hausdorff space}.
\]

Universal invariants include:

- homotopy type;
- connected components;
- cohomology;
- lattice of open sets.

Fixed points include compactifications such as the Stone–Čech compactification, and complete regular locales under appropriate completion.

### 9.3 Geometric phase

The geometric phase adds metric, smooth, symplectic, or Riemannian structure.

Primitive operations:

- smooth atlas generation;
- metric completion;
- curvature flows;
- deformation of complex structures;
- moduli formation.

Typical evolutionary path:

\[
\text{topological manifold}
\longrightarrow
\text{smooth manifold}
\longrightarrow
\text{Riemannian manifold}
\longrightarrow
\text{moduli-stable geometric structure}.
\]

Universal invariants include:

- characteristic classes;
- curvature invariants;
- Gromov–Hausdorff limits;
- symplectic capacities.

Fixed-point-like objects include Ricci solitons, calibrated submanifolds, and stable bundles under appropriate flow-induced evolution.

### 9.4 Analytic phase

The analytic phase is governed by limits, completeness, continuity, and differentiation.

Primitive operations:

- Cauchy completion;
- Dedekind completion;
- completion of normed spaces;
- passage to Banach or Hilbert spaces;
- sheaf cohomology and analytic continuation.

Typical evolutionary path:

\[
\mathbb{Q}
\longrightarrow
\mathbb{R}
\longrightarrow
\mathbb{C}
\longrightarrow
\text{function spaces}
\longrightarrow
\text{distribution spaces}.
\]

Universal invariants include:

- completeness;
- spectral data;
- cohomology;
- functional calculus.

Fixed points include complete metric spaces under Cauchy completion and Hilbert spaces under Hilbert-space completion.

### 9.5 Logical phase

In the logical phase, structures are theories, proofs, models, and interpretations.

Primitive operations:

- conservative extension;
- definitional extension;
- forcing;
- ultraproduct formation;
- sheaf semantics;
- model completion.

Typical evolutionary path:

\[
\text{axiom system}
\longrightarrow
\text{consistent extension}
\longrightarrow
\text{complete theory}
\longrightarrow
\text{saturated model}.
\]

Universal invariants include:

- proof-theoretic strength;
- interpretability degree;
- Lindenbaum algebra;
- model-theoretic stability.

Fixed points correspond to complete theories, saturated models, or model companions where they exist. Gödelian limitations appear as obstructions to effective fixed points for sufficiently strong arithmetic theories.

### 9.6 Probabilistic phase

The probabilistic phase is dominated by measure, randomness, filtration, and expectation.

Primitive operations:

- measure completion;
- conditional expectation;
- filtration enlargement;
- martingale closure;
- passage to spaces of random variables.

Typical evolutionary path:

\[
\text{pre-measure algebra}
\longrightarrow
\sigma\text{-algebra}
\longrightarrow
\text{complete probability space}
\longrightarrow
\text{martingale limit}.
\]

Universal invariants include:

- measure algebra;
- entropy;
- stochastic integrals;
- filtration type.

Fixed points include completed probability spaces and martingale convergence limits.

### 9.7 Categorical phase

The categorical phase treats structures as objects of functorial transformation.

Primitive operations:

- passage to functor categories;
- presheaf completion;
- sheafification;
- localization;
- categorification;
- passage to \(\infty\)-categories.

Typical evolutionary path:

\[
\text{set}
\longrightarrow
\text{category}
\longrightarrow
\text{topos}
\longrightarrow
\infty\text{-topos}.
\]

Universal invariants include:

- universal properties;
- representability;
- adjunctions;
- higher coherences.

Fixed points include presheaf topoi under free colimit completion, idempotent monads, and higher-categorical closures.

### 9.8 Phase table

| Phase | Dominant Generative Operations | Typical Invariants | Fixed-Point Examples |
|---|---|---|---|
| Algebra | Free generation, quotient, localization | Congruence lattices, homology | Algebraically closed fields, complete rings |
| Topology | Open-set generation, compactification | Homotopy type, cohomology | Compactifications, complete locales |
| Geometry | Metricization, deformation, curvature flow | Characteristic classes, curvature invariants | Solitons, stable bundles |
| Analysis | Completion, limit formation | Spectra, completeness | Banach/Hilbert completions |
| Logic | Conservative extension, forcing | Interpretability, stability | Complete theories, saturated models |
| Probability | Measure completion, filtration | Entropy, measure algebra | Martingale limits |
| Category | Functorialization, sheafification | Universal properties, adjunctions | Presheaf topoi, idempotent monads |

---

## 10. Applications

### 10.1 Foundations of mathematics

UMET provides a dynamic foundation in which mathematical being is replaced by mathematical becoming. Instead of reducing all mathematics to a static universe of sets or types, UMET treats mathematics as a structured generative process.

This framework allows one to compare foundational systems by their evolutionary behavior:

- What structures can they generate?
- What invariants do they preserve?
- What fixed points do they admit?
- What phase transitions are possible?

Foundational disagreements can then be analyzed as different choices of primitive generative laws.

### 10.2 Automated theorem discovery

The evolutionary graph provides a natural search space for theorem discovery.

Given an initial structure \(S_0\) and a target property \(P\), one may search for a trajectory

\[
S_0\longrightarrow S_1\longrightarrow \cdots \longrightarrow S_n
\]

such that \(P(S_n)\) holds.

A basic evolutionary theorem-discovery algorithm is:

1. Initialize \(S_0\).
2. Generate admissible successors \(\operatorname{Succ}(S_n)\).
3. Compute invariants \(I(S_{n+1})\).
4. Discard branches violating target invariant constraints.
5. Test desired property \(P\).
6. Iterate.

Invariants drastically prune the search space. Fixed points provide natural termination criteria.

A theorem may be interpreted as a stable consequence along an evolutionary trajectory.

### 10.3 Artificial intelligence

UMET suggests a generative architecture for mathematical reasoning systems.

A learned model may approximate an evolution operator

\[
\widehat{\mathfrak{U}}_\theta
\]

parameterized by neural weights \(\theta\). Training objectives can include:

- preservation of known invariants;
- successful completion of trajectories;
- proof validity;
- structural coherence;
- discovery of fixed points;
- minimization of evolutionary free energy.

This differs from pattern-matching approaches to theorem proving. The system is trained not merely to verify statements but to generate lawful structural transformations.

### 10.4 Complex systems

Complex systems often exhibit emergent organization. UMET models emergence through the tensor interaction term

\[
J^{i'j'}{}_{ij}
\]

and through emergent generative operations \(\Gamma_{\mathrm{em}}\).

Macroscopic laws correspond to fixed points or slow manifolds of the evolutionary dynamics. Phase transitions correspond to abrupt reorganization of system-level structure.

### 10.5 Mathematical physics

Several constructions in mathematical physics already have UMET-like form.

Examples:

- The renormalization group is an evolution operator on effective theories.
- Fixed points correspond to conformal field theories.
- Phase transitions correspond to singularities in thermodynamic limits.
- Tensor networks represent hierarchical structural evolution.
- Path integrals may be interpreted as sums over evolutionary trajectories.

UMET generalizes these ideas from physical state spaces to mathematical structures themselves.

### 10.6 Formal scientific modeling

Scientific models evolve under new data, symmetries, and idealizations. UMET treats model revision as structural evolution.

A model \(M\) evolves by:

- quotienting by observational indistinguishability;
- completing missing limits;
- extending by new variables;
- internalizing uncertainty;
- passing to higher-level effective structures.

Thus UMET provides a formal meta-theory of scientific model evolution.

---

## 11. Open Problems

The present paper establishes the formal architecture of UMET. Many problems remain.

### Problem 11.1: Canonical primitive generative signature

Is there a canonical choice of \(\Gamma\) from which the major structures of mathematics arise with minimal redundancy?

### Problem 11.2: Classification of fixed points

Classify evolutionary fixed points for natural choices of \(\Gamma\). In particular, classify completion-fixed, algebraically closed, categorically complete, and logically saturated fixed points.

### Problem 11.3: Invariant completeness

Determine whether there exists a finite or recursively enumerable family of universal invariants capable of distinguishing all evolutionary phases of interest.

### Problem 11.4: Effective evolution

For which generative signatures is the successor relation

\[
T\in \operatorname{Succ}(S)
\]

decidable or semi-decidable?

### Problem 11.5: Learned evolution operators

Can neural or symbolic systems learn approximations to \(\mathfrak{U}\) that preserve formal invariants and produce valid mathematical extensions?

### Problem 11.6: UMET and incompleteness

Clarify the relation between evolutionary fixed points and Gödelian incompleteness. A plausible conjecture is that sufficiently expressive logical systems do not admit computable complete fixed points, although they may admit non-effective or semantic fixed points.

### Problem 11.7: Higher-categorical UMET

Extend UMET to fully \(\infty\)-categorical and homotopical settings, where evolutionary paths are not merely sequences but higher coherent diagrams.

---

## 12. Conclusion

Universal Mathematical Evolution Theory provides a unified formal framework for understanding mathematics as a generative dynamical system. The central construction is the universal evolution operator

\[
\mathfrak{U}:\mathcal{M}\longrightarrow \mathcal{M},
\]

defined as the free monadic closure of primitive generative laws. This operator yields a rigorous semantics for structural becoming.

Within this framework:

- mathematical structures are states;
- constructions are evolutionary steps;
- trajectories are mathematical histories;
- invariants are conserved structural quantities;
- fixed points are closed or complete structures;
- phase transitions are singular changes in evolutionary regime.

Algebra, topology, geometry, analysis, logic, probability, and category theory appear not as isolated domains but as phases of a single universal evolutionary landscape.

UMET therefore offers both a foundational perspective and a technical apparatus for the study of mathematical generation, discovery, and emergence.

---

## Appendix A: Summary of Axioms

### Axiom UMET-I: Generation

\[
S\leq \mathfrak{U}(S).
\]

Every structure admits a nontrivial evolutionary envelope.

### Axiom UMET-II: Coherent Stability

There exists a core functor \(\mathsf{C}\) such that stable evolution preserves cores:

\[
\mathsf{C}(\mathfrak{U}_{\mathrm{st}}(S))\cong \mathsf{C}(S).
\]

### Axiom UMET-III: Interaction

For composite structures,

\[
\mathfrak{U}(S\otimes T)
\]

contains but is not necessarily equivalent to

\[
\mathfrak{U}(S)\otimes \mathfrak{U}(T).
\]

The difference is encoded by an interaction structure

\[
\mathsf{I}(S,T).
\]

In tensor notation:

\[
U^{ab}{}_{cd}
=
U^a{}_cU^b{}_d
+
I^{ab}{}_{cd}.
\]

### Axiom UMET-IV: Specialization

For each specialization \(\pi:S\to R\), there exists an induced map

\[
\mathfrak{U}(\pi):\mathfrak{U}(S)\to \mathfrak{U}(R)
\]

making the evolutionary unit natural.

### Axiom UMET-V: Emergence

There exist successors \(T\in \operatorname{Succ}(S)\) whose core is not definable from the stable core of \(S\):

\[
\mathsf{C}(T)\not\cong \mathsf{C}(S')
\]

for all stable extensions \(S'\) of \(S\).

---

## Appendix B: Notation

| Symbol | Meaning |
|---|---|
| \(\mathcal{M}\) | Class or category of admissible mathematical structures |
| \(\mathbf{Str}_\kappa\) | Category of \(\kappa\)-small structural states |
| \(S,T\) | Structural states |
| \(\Gamma\) | Primitive generative endofunctor |
| \(\mathfrak{U}\) | Universal evolution operator |
| \(\eta\) | Evolutionary unit |
| \(\mu\) | Monad multiplication |
| \(\operatorname{Succ}(S)\) | Admissible successors of \(S\) |
| \(d(S,T)\) | Evolutionary distance |
| \(\mathsf{C}\) | Core functor |
| \(\mathsf{I}(S,T)\) | Interaction structure |
| \(I\) | Evolutionary invariant |
| \(\widehat{\mathfrak{U}}\) | Linearized evolutionary propagator |
| \(U^T{}_S\) | Transition amplitude/weight from \(S\) to \(T\) |
| \(J^{i'j'}{}_{ij}\) | Interaction tensor |
| \(S_\infty(\theta)\) | Parameterized evolutionary limit |
| \(\Delta(\theta)\) | Spectral gap of linearized evolution |

---

## References and Conceptual Antecedents

The formal machinery used here draws on the theory of monads, accessible categories, locally presentable categories, categorical algebra, fixed-point theorems, Markov operators, and spectral theory. The present work reorganizes these ingredients into a unified theory of mathematical evolution.
