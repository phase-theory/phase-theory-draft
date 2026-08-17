# Dynamic Mathematical Ontology

**Preprint**

---

## Abstract

We develop **Dynamic Mathematical Ontology** (DMO), a formal theory in which existence is not a static predicate but a dynamical operator-governed process. Objects are treated as structural entities whose ontological status evolves through **ontological transitions**, while **existence operators** determine the actual part of an object at each stage. The theory introduces four primitive notions: existence operators, ontological transitions, structural persistence, and creation/annihilation maps. We axiomatize DMO using quantale-valued existence degrees, graded monoidal categories, and process categories fibred over stages of becoming. We prove an existence-closure theorem, a structural persistence theorem, and a creation–annihilation idempotence theorem, and we give a tensorial calculus for finite-dimensional or linear representations. A modal substructural logic, **Dynamic Existential Logic**, is introduced as the internal language of DMO models. Applications are given to mathematical foundations, logic, computer science, and formal knowledge systems.

**Keywords:** dynamic ontology, existence operator, categorical semantics, quantale, structural persistence, creation and annihilation, modal logic, process category, formal foundations.

---

## 1. Introduction

Classical mathematical ontology is ordinarily static. A set either belongs to a universe or it does not; a type is either inhabited or empty; a proposition is either true in a model or false. Even when mathematics studies change, the objects that change are normally presupposed as already existing. The ontology itself is fixed.

Dynamic Mathematical Ontology reverses this order. We treat **existence itself as a dynamical phenomenon**. Objects may be generated, actualized, persist, become latent, merge, split, or be annihilated. The central question is not merely “What exists?” but:

> By what formal rules does something come to exist, cease to exist, or persist through transformation?

The present paper develops a rigorous mathematical framework for this question.

The theory is built around four primitive concepts.

1. **Existence operators**  
   Operators that select the actual part of a potential structure at a given ontological stage.

2. **Ontological transitions**  
   Morphisms or process maps by which structures pass from one ontological stage to another.

3. **Structural persistence**  
   The invariant core of an object that survives a transition.

4. **Creation and annihilation maps**  
   Formal operations by which objects are generated from a vacuum or returned to it.

The framework is deliberately general. It can be instantiated in set-theoretic foundations, type theory, categorical logic, process calculi, resource-sensitive computation, and dynamic knowledge representation.

The principal contributions are the following.

1. A quantale-valued theory of existence degrees.
2. A categorical semantics based on graded monoidal process categories.
3. Axioms for dynamic existence operators.
4. A formal account of structural persistence as invariant cores.
5. Creation and annihilation laws with tensorial formulations.
6. A sound modal logic of dynamic existence.
7. Applications to foundations, logic, computation, and formal knowledge systems.

The paper is organized as follows. Section 2 introduces ontological quantales. Section 3 develops static existence operators. Section 4 defines dynamic mathematical ontologies and proves the existence-closure theorem. Section 5 gives the tensorial calculus. Section 6 formalizes structural persistence. Section 7 treats creation and annihilation. Section 8 introduces Dynamic Existential Logic. Section 9 presents examples. Section 10 discusses applications. Section 11 lists open problems. Section 12 concludes.

---

## 2. Ontological Degrees and Quantales

Existence in DMO is not assumed to be Boolean. An object may exist fully, partially, potentially, probabilistically, resource-sensitively, or to a degree determined by evidence, consistency, availability, or actualization. We therefore model existence degrees using quantales.

### Definition 2.1: Ontological quantale

An **ontological quantale** is a complete lattice \((Q,\leq)\) equipped with an associative binary operation

\[
\otimes : Q \times Q \to Q
\]

and a unit \(1 \in Q\), such that \(\otimes\) preserves arbitrary joins in each variable:

\[
a \otimes \bigvee_i b_i = \bigvee_i (a \otimes b_i),
\qquad
\left(\bigvee_i a_i\right) \otimes b = \bigvee_i (a_i \otimes b).
\]

We write \(0 = \bigvee \varnothing\) for the bottom element. In most applications \(Q\) is commutative and unital:

\[
a \otimes b = b \otimes a,
\qquad
1 \otimes a = a.
\]

If \(Q\) is residuated, we write \(a \Rightarrow b\) for the right adjoint to \(a \otimes -\).

Intuitively:

- \(1\) denotes full existence.
- \(0\) denotes nonexistence.
- \(a \otimes b\) denotes combined existence strength.
- \(\bigvee\) denotes existential aggregation over alternative transitions.
- \(\bigwedge\) denotes universal or necessary constraints.

### Examples 2.2

1. **Boolean ontology**  
   \[
   Q = \{0,1\}, \quad a \otimes b = a \wedge b.
   \]  
   Objects either exist or do not exist.

2. **Fuzzy ontology**  
   \[
   Q = [0,1], \quad a \otimes b = \min(a,b)
   \]
   or
   \[
   a \otimes b = ab.
   \]

3. **Resource ontology**  
   \[
   Q = \mathbb{N} \cup \{\infty\},
   \]
   ordered by reverse order or by availability, with \(\otimes\) interpreted as addition or minimum, depending on whether existence is measured by cost or capacity.

4. **Boolean-valued ontology**  
   If \(\mathcal{B}\) is a complete Boolean algebra, then
   \[
   Q = \mathcal{B}, \quad a \otimes b = a \wedge b.
   \]
   This is useful for forcing and Boolean-valued models.

5. **Probabilistic or measure-theoretic ontology**  
   With suitable restrictions, one may take measurable truth values or capacities.

The choice of \(Q\) determines the mode of existence being formalized.

---

## 3. Static Existence Operators

We begin with a static theory of existence operators on a fixed structural category. The dynamic theory will be obtained by indexing these operators over stages.

Let \(\mathcal{C}\) be a symmetric monoidal category

\[
(\mathcal{C},\otimes,I)
\]

with zero object \(0\), when such an object is needed. We assume \(\mathcal{C}\) is \(Q\)-graded.

### Definition 3.1: \(Q\)-graded category

A **\(Q\)-graded category** is a category \(\mathcal{C}\) together with a grade assignment

\[
|{-}| : \operatorname{Mor}(\mathcal{C}) \to Q
\]

such that:

1. Identity grade:
   \[
   |\operatorname{id}_A| = 1.
   \]

2. Composition inequality:
   \[
   |g \circ f| \geq |f| \otimes |g|.
   \]

3. Monoidal compatibility:
   \[
   |f \otimes g| = |f| \otimes |g|.
   \]

A morphism \(f\) is **fully actual** if \(|f|=1\), **potential** if \(0 < |f| < 1\), and **null** if \(|f|=0\), assuming \(Q\) has a meaningful order.

The inequality for composition allows weakening: a composite may be more actual than the mere product of its parts, for example when additional structure actualizes it.

### Definition 3.2: Existence operator

An **existence operator** on an object \(A \in \mathcal{C}\) is an idempotent endomorphism

\[
\mathfrak{E}_A : A \to A
\]

such that

\[
\mathfrak{E}_A^2 = \mathfrak{E}_A.
\]

The image of \(\mathfrak{E}_A\), when it exists, is the **actual part** of \(A\).

The **existence degree** of \(A\) is

\[
e(A) = |\mathfrak{E}_A|.
\]

We say:

- \(A\) is **fully actual** if \(e(A)=1\).
- \(A\) is **nonexistent** if \(e(A)=0\).
- \(A\) is **partially actual** otherwise.

### Definition 3.3: Monoidal existence structure

A family of existence operators \(\{\mathfrak{E}_A\}_{A \in \mathcal{C}}\) is **monoidal** if:

1. Unit actualization:
   \[
   \mathfrak{E}_I = \operatorname{id}_I.
   \]

2. Tensor actualization:
   \[
   \mathfrak{E}_{A \otimes B} = \mathfrak{E}_A \otimes \mathfrak{E}_B.
   \]

3. Zero annihilation:
   \[
   \mathfrak{E}_0 = 0.
   \]

### Proposition 3.4: Existence degree of composites

If the existence operators are monoidal, then

\[
e(A \otimes B) = e(A) \otimes e(B).
\]

**Proof.**  
By definition,

\[
e(A \otimes B)
= |\mathfrak{E}_{A \otimes B}|.
\]

By monoidality,

\[
\mathfrak{E}_{A \otimes B}
=
\mathfrak{E}_A \otimes \mathfrak{E}_B.
\]

Hence, by monoidal grading,

\[
|\mathfrak{E}_{A \otimes B}|
=
|\mathfrak{E}_A| \otimes |\mathfrak{E}_B|
=
e(A) \otimes e(B).
\]

∎

This proposition formalizes the idea that the existence of a composite system is determined by the existence of its components and the mode of composition.

---

## 4. Dynamic Mathematical Ontologies

We now pass from static existence operators to dynamic ontologies.

The central idea is that existence operators vary over **stages**. A stage may represent time, computational state, proof state, forcing extension, epistemic state, or process phase.

Let \(\mathsf{T}\) be a small category of stages. In many cases \(\mathsf{T}\) is a poset, monoid, or preorder.

### Definition 4.1: Dynamic Mathematical Ontology

A **Dynamic Mathematical Ontology** is a tuple

\[
\mathcal{D}
=
(Q,\mathcal{C},\mathsf{T},\mathfrak{E},\mathsf{P},\rho,V)
\]

where:

1. \(Q\) is an ontological quantale.

2. \(\mathcal{C}\) is a symmetric monoidal \(Q\)-graded category of structural types.

3. \(\mathsf{T}\) is a category of ontological stages.

4. For each stage \(t \in \mathsf{T}\) and object \(A \in \mathcal{C}\), there is an existence operator

   \[
   \mathfrak{E}_{t,A} : A \to A
   \]

   satisfying idempotence:

   \[
   \mathfrak{E}_{t,A}^2 = \mathfrak{E}_{t,A}.
   \]

5. The family \(\mathfrak{E}_t\) is monoidal:

   \[
   \mathfrak{E}_{t,I} = \operatorname{id}_I,
   \]

   \[
   \mathfrak{E}_{t,A \otimes B}
   =
   \mathfrak{E}_{t,A} \otimes \mathfrak{E}_{t,B}.
   \]

6. \(\mathsf{P}\) is the **process category** whose objects are pairs \((A,t)\), and whose morphisms

   \[
   f : (A,t) \to (B,s)
   \]

   are morphisms \(f : A \to B\) in \(\mathcal{C}\) satisfying the actuality compatibility condition

   \[
   f
   =
   \mathfrak{E}_{s,B} \circ f \circ \mathfrak{E}_{t,A}.
   \]

   The identity morphism on \((A,t)\) is

   \[
   \operatorname{id}_{(A,t)} = \mathfrak{E}_{t,A}.
   \]

7. Each process morphism \(f\) has a transition strength

   \[
   \rho(f) \in Q
   \]

   such that

   \[
   \rho(\operatorname{id}_{(A,t)}) = 1
   \]

   and

   \[
   \rho(g \circ f)
   =
   \rho(f) \otimes \rho(g).
   \]

8. \(V\) is a distinguished **vacuum object** satisfying

   \[
   \mathfrak{E}_{t,V} = \operatorname{id}_V
   \]

   for all \(t\).

The morphisms of \(\mathsf{P}\) are called **ontological transitions**.

### Interpretation

An object \(A\) at stage \(t\) is not simply an object of \(\mathcal{C}\). It is a pair \((A,t)\), together with an existence operator \(\mathfrak{E}_{t,A}\). The operator determines which part of \(A\) is actual at stage \(t\).

A transition

\[
f : (A,t) \to (B,s)
\]

is legitimate only if it sends the actual part of \(A\) at \(t\) into the actual part of \(B\) at \(s\). This is expressed by the compatibility condition

\[
f
=
\mathfrak{E}_{s,B} f \mathfrak{E}_{t,A}.
\]

Thus transitions are not arbitrary structure maps; they are existence-respecting process maps.

### Proposition 4.2: Actuality preservation

Let

\[
f : (A,t) \to (B,s)
\]

be an ontological transition. If \(x : U \to A\) is actual at stage \(t\), i.e.

\[
\mathfrak{E}_{t,A} \circ x = x,
\]

then \(f \circ x\) is actual at stage \(s\):

\[
\mathfrak{E}_{s,B} \circ f \circ x = f \circ x.
\]

**Proof.**  
Using the transition compatibility condition,

\[
f = \mathfrak{E}_{s,B} f \mathfrak{E}_{t,A}.
\]

Therefore,

\[
f \circ x
=
\mathfrak{E}_{s,B} f \mathfrak{E}_{t,A} x.
\]

Since \(x\) is actual at \(t\),

\[
\mathfrak{E}_{t,A} x = x.
\]

Hence,

\[
f \circ x
=
\mathfrak{E}_{s,B} f x.
\]

Thus \(f x\) is actual at stage \(s\). ∎

### Definition 4.3: Existence valuation

An **existence valuation** on \(\mathcal{D}\) is a function

\[
e : \operatorname{Obj}(\mathsf{P}) \to Q
\]

such that for every transition

\[
f : (A,t) \to (B,s)
\]

the propagation inequality holds:

\[
e(B,s) \geq e(A,t) \otimes \rho(f).
\]

When \(e(A,t) = |\mathfrak{E}_{t,A}|\), we say the valuation is induced by the existence operators.

The inequality says: if \(A\) exists to degree \(e(A,t)\), and there is a transition of strength \(\rho(f)\) from \(A\) to \(B\), then \(B\) must exist to at least the combined degree.

### Theorem 4.4: Existence-closure theorem

Let \(\mathcal{D}\) be a DMO and let \(e_0\) be an initial existence valuation. Define an operator

\[
\Phi : Q^{\operatorname{Obj}(\mathsf{P})} \to Q^{\operatorname{Obj}(\mathsf{P})}
\]

by

\[
(\Phi e)(B,s)
=
e(B,s)
\vee
\bigvee_{f:(A,t)\to(B,s)}
\left(
e(A,t) \otimes \rho(f)
\right).
\]

Then:

1. \(\Phi\) is monotone.
2. \(\Phi\) is inflationary:
   \[
   e \leq \Phi e.
   \]
3. The least fixed point of \(\Phi\) above \(e_0\) exists.
4. This least fixed point is the least dynamically closed existence valuation extending \(e_0\).

**Proof.**  
Monotonicity follows because \(\otimes\) preserves joins and \(e \mapsto e(B,s)\) is monotone. Inflationarity is immediate from the definition of \(\Phi\).

The set of valuations

\[
Q^{\operatorname{Obj}(\mathsf{P})}
\]

is a complete lattice, since \(Q\) is complete. By the Knaster–Tarski theorem, every monotone operator on a complete lattice has a least fixed point above any prefixed point. Therefore the least fixed point of \(\Phi\) above \(e_0\) exists.

A valuation \(e\) is dynamically closed precisely when

\[
\Phi e = e.
\]

Thus the least fixed point is the least dynamically closed valuation extending \(e_0\). ∎

We call this fixed point the **ontological closure** of the initial valuation.

### Corollary 4.5: Deterministic transition systems

If for each label \(\lambda\) there is at most one transition from \((A,t)\), then the closure equation becomes

\[
e(B,s)
=
e(B,s)
\vee
\bigvee_{\lambda}
\left(
e(A,t) \otimes \rho_\lambda(A)
\right).
\]

This recovers weighted automata and dynamic epistemic update as special cases.

---

## 5. Tensorial Formulation

When \(\mathcal{C}\) is a category of modules, vector spaces, sheaves, or other linear structures, existence operators and transitions admit tensor notation.

Let \(M\) be a \(Q\)-module with basis indexed by structural modes. An ontological state is represented by a tensor

\[
x = x^i e_i.
\]

We use Einstein summation convention.

### 5.1 Existence operators

An existence operator at stage \(t\) is a tensor

\[
(E_t)^i{}_j
\]

acting by

\[
(E_t x)^i = (E_t)^i{}_j x^j.
\]

Idempotence is

\[
(E_t)^i{}_j (E_t)^j{}_k = (E_t)^i{}_k.
\]

A state is actual at stage \(t\) iff

\[
(E_t)^i{}_j x^j = x^i.
\]

The existence degree may be represented by a scalar functional

\[
\varepsilon_t(x) = \omega_i (E_t)^i{}_j x^j,
\]

where \(\omega_i\) is a fixed counit or evaluation covector.

### 5.2 Transitions

A transition from stage \(t\) to stage \(s\) is represented by a tensor

\[
(T_{t,s})^i{}_j.
\]

It acts by

\[
x'^{i} = (T_{t,s})^i{}_j x^j.
\]

Actuality compatibility becomes

\[
T_{t,s} E_t = E_s T_{t,s},
\]

or in components,

\[
(T_{t,s})^i{}_j (E_t)^j{}_k
=
(E_s)^i{}_j (T_{t,s})^j{}_k.
\]

If \(x\) is actual at \(t\), then

\[
E_s T_{t,s} x
=
T_{t,s} E_t x
=
T_{t,s} x,
\]

so \(T_{t,s}x\) is actual at \(s\).

### 5.3 Composite systems

For two systems \(A\) and \(B\), the combined state space is

\[
M_A \otimes M_B.
\]

The composite existence operator is

\[
(E_{AB})^{ik}{}_{jl}
=
(E_A)^i{}_j (E_B)^k{}_l.
\]

A composite transition is

\[
(T_{AB})^{ik}{}_{jl}
=
(T_A)^i{}_j (T_B)^k{}_l.
\]

Thus

\[
E_{AB} = E_A \otimes E_B,
\qquad
T_{AB} = T_A \otimes T_B.
\]

### 5.4 Existence conservation

Let \(T : M_t \to M_s\) be a transition. Define the existence scalar

\[
\varepsilon_t(x) = \omega_i (E_t)^i{}_j x^j.
\]

We say \(T\) is **existence-conserving** if

\[
\varepsilon_s(Tx) = \varepsilon_t(x)
\]

for all \(x\).

In tensor form this requires

\[
\omega_i (E_s)^i{}_j (T)^j{}_k
=
\omega_k (E_t)^k{}_k?
\]

More invariantly, if \(\eta_t = \omega \circ E_t\), then existence conservation is

\[
\eta_s \circ T = \eta_t.
\]

Equivalently,

\[
\omega_i (E_s)^i{}_j T^j{}_k
=
\omega_i (E_t)^i{}_k.
\]

This is the DMO analogue of a conservation law.

---

## 6. Ontological Transition Calculus

We can present DMO transitions as an inference system.

### Rules

1. **Actuality rule**

   If \(x\) is actual at stage \(t\), and \(f : (A,t) \to (B,s)\) is a transition, then \(f(x)\) is actual at stage \(s\):

   \[
   \frac{
   x = \mathfrak{E}_{t,A}x
   \quad
   f = \mathfrak{E}_{s,B} f \mathfrak{E}_{t,A}
   }{
   f(x) = \mathfrak{E}_{s,B} f(x)
   }.
   \]

2. **Composition rule**

   \[
   \frac{
   f : (A,t) \to (B,s)
   \quad
   g : (B,s) \to (C,r)
   }{
   g \circ f : (A,t) \to (C,r)
   }
   \]

   with transition strength

   \[
   \rho(g \circ f) = \rho(f) \otimes \rho(g).
   \]

3. **Tensor rule**

   If

   \[
   f : (A,t) \to (B,s),
   \qquad
   g : (C,t) \to (D,s),
   \]

   then

   \[
   f \otimes g :
   (A \otimes C,t)
   \to
   (B \otimes D,s)
   \]

   with

   \[
   \rho(f \otimes g)
   =
   \rho(f) \otimes \rho(g).
   \]

4. **Existence propagation rule**

   \[
   \frac{
   f : (A,t) \to (B,s)
   }{
   e(B,s) \geq e(A,t) \otimes \rho(f)
   }.
   \]

5. **Vacuum rule**

   The vacuum object \(V\) is always actual:

   \[
   \mathfrak{E}_{t,V} = \operatorname{id}_V.
   \]

These rules generate the minimal dynamically closed ontology from a set of primitive transitions.

---

## 7. Structural Persistence

A central requirement of any ontology is identity through change. DMO formalizes this through **structural persistence**.

### Definition 7.1: Persistent substructure

Let

\[
f : (A,t) \to (B,s)
\]

be an ontological transition. A **persistent structure** for \(f\) is a span

\[
P
\xrightarrow{p_A}
A,
\qquad
P
\xrightarrow{p_B}
B
\]

such that:

1. \(p_A\) and \(p_B\) are monomorphisms.

2. \(p_A\) is actual at \(t\):

   \[
   \mathfrak{E}_{t,A} p_A = p_A.
   \]

3. \(p_B\) is actual at \(s\):

   \[
   \mathfrak{E}_{s,B} p_B = p_B.
   \]

4. The square commutes:

   \[
   f \circ p_A = p_B.
   \]

The object \(P\) is the **persisting core**.

### Definition 7.2: Persistence core

A **persistence core** of \(f\) is a terminal object in the category of persistent structures for \(f\).

Explicitly, \(\Pi_f\) is a persistence core if for every persistent structure

\[
Q \xrightarrow{q_A} A,
\qquad
Q \xrightarrow{q_B} B,
\]

there exists a unique morphism

\[
u : Q \to \Pi_f
\]

such that

\[
p_A u = q_A,
\qquad
p_B u = q_B.
\]

We write

\[
\Pi_f
\]

for the maximal structure preserved by \(f\).

### Definition 7.3: Endotransition persistence

If \(f : (A,t) \to (A,s)\) is an endotransition on the same structural type, persistence is often represented by an idempotent

\[
P : A \to A
\]

such that

\[
P^2 = P.
\]

If \(t=s\), the strongest persistence condition is

\[
f P = P f.
\]

The image of \(P\) is the invariant part of \(A\).

### Proposition 7.4: Invariance theorem

Let \(T : M \to M\) be a linear transition operator and let \(P : M \to M\) be an idempotent. If

\[
T P = P T,
\]

then \(\operatorname{im}(P)\) is invariant under \(T\).

**Proof.**  
Let \(x \in \operatorname{im}(P)\). Then \(Px = x\). We compute

\[
P(Tx)
=
(PT)x
=
(TP)x
=
T(Px)
=
Tx.
\]

Thus \(Tx \in \operatorname{im}(P)\). ∎

Conversely, if a direct-sum decomposition

\[
M = \operatorname{im}(P) \oplus \ker(P)
\]

is preserved by \(T\), then \(T\) commutes with \(P\).

### Theorem 7.5: Maximal persistence theorem

Assume that:

1. \(\mathcal{C}\) has finite limits and images.
2. Existence operators determine subobjects of actual parts.
3. Transition morphisms preserve actual parts.

Then for every ontological transition

\[
f : (A,t) \to (B,s)
\]

there exists a maximal persistent substructure, unique up to isomorphism.

In algebraic form, if idempotents form a complete lattice, the maximal source persistence projector is

\[
P_t
=
\bigvee
\left\{
R \leq \mathfrak{E}_{t,A}
\; \middle| \;
\exists S \leq \mathfrak{E}_{s,B}
\text{ such that }
f R = S f
\right\}.
\]

The corresponding target persistence projector is

\[
P_s
=
\bigvee
\left\{
S \leq \mathfrak{E}_{s,B}
\; \middle| \;
\exists R \leq \mathfrak{E}_{t,A}
\text{ such that }
f R = S f
\right\}.
\]

These projectors define the maximal invariant core preserved by \(f\).

**Proof sketch.**  
The set of idempotents below \(\mathfrak{E}_{t,A}\) is a complete lattice. The condition \(fR = Sf\) is closed under joins because composition is linear or join-preserving in typical graded categories. Hence the join exists and yields the greatest source projector satisfying the persistence equation. The target projector is defined dually. Universality follows from the universal property of joins in the lattice of subobjects. ∎

### Interpretation

Structural persistence is not identity of underlying substrate. It is identity of the maximal invariant structural core under ontological transition. An object may change its accidental properties while its persistent core remains actual.

This provides a mathematical account of diachronic identity.

---

## 8. Creation and Annihilation Maps

We now formalize generation and destruction.

### Definition 8.1: Vacuum object

A **vacuum object** \(V\) is an object satisfying:

1. Full actuality:

   \[
   \mathfrak{E}_{t,V} = \operatorname{id}_V.
   \]

2. Scalar endomorphisms:

   \[
   \operatorname{End}_{\mathsf{P}}(V) \cong Q.
   \]

Thus every endomorphism of the vacuum is multiplication by an existence scalar.

### Definition 8.2: Creation map

A **creation map** for an object \(A\) from stage \(t\) to stage \(s\) is a transition

\[
c_{t,A} : (V,t) \to (A,s).
\]

It must satisfy

\[
c_{t,A}
=
\mathfrak{E}_{s,A} c_{t,A}.
\]

Thus creation produces an actual object.

Its transition strength is

\[
\rho(c_{t,A}) = \gamma_A \in Q.
\]

### Definition 8.3: Annihilation map

An **annihilation map** for \(A\) from stage \(t\) to stage \(s\) is a transition

\[
a_{t,A} : (A,t) \to (V,s)
\]

satisfying

\[
a_{t,A}
=
a_{t,A} \mathfrak{E}_{t,A}.
\]

Thus annihilation acts only on the actual part of \(A\).

Its transition strength is

\[
\rho(a_{t,A}) = \alpha_A \in Q.
\]

### Axiom 8.4: Vacuum return law

The composite

\[
a_{t,A} \circ c_{t,A} : (V,t) \to (V,r)
\]

is a scalar multiple of the vacuum identity:

\[
a_{t,A} c_{t,A}
=
\theta_A \operatorname{id}_V
\]

for some

\[
\theta_A \in Q.
\]

We call \(\theta_A\) the **creation–annihilation yield** of \(A\).

In many models,

\[
\theta_A = \gamma_A \otimes \alpha_A.
\]

### Theorem 8.5: Creation–annihilation idempotence

Assume \(\theta_A\) is invertible in \(Q\). Define

\[
P_A
=
\theta_A^{-1} c_{t,A} a_{t,A}.
\]

Then

\[
P_A^2 = P_A.
\]

Thus \(P_A\) is an idempotent projecting onto the created persistent sector of \(A\).

**Proof.**  
We compute:

\[
P_A^2
=
\theta_A^{-2}
c a c a.
\]

Using the vacuum return law,

\[
a c = \theta_A \operatorname{id}_V.
\]

Therefore,

\[
P_A^2
=
\theta_A^{-2}
c (\theta_A \operatorname{id}_V) a
=
\theta_A^{-1}
c a
=
P_A.
\]

∎

When \(\theta_A = 1\), creation and annihilation form a perfect reversible cycle at the level of the vacuum.

### 8.6 Tensorial form

Let \(C^i\) be the creation vector and \(A_j\) the annihilation covector. Then:

\[
c(1) = C^i e_i,
\]

\[
a(x) = A_i x^i.
\]

The vacuum return law is

\[
A_i C^i = \theta.
\]

The induced projector is

\[
(P_A)^i{}_j
=
\theta^{-1} C^i A_j.
\]

Then

\[
(P_A)^i{}_k (P_A)^k{}_j
=
\theta^{-2} C^i A_k C^k A_j
=
\theta^{-2} C^i \theta A_j
=
\theta^{-1} C^i A_j
=
(P_A)^i{}_j.
\]

### 8.7 Fock-style extension

For a system with elementary types indexed by \(I\), one may form an ontological Fock object

\[
\mathcal{F}
=
\bigoplus_{n \geq 0}
\operatorname{Sym}^n(M),
\]

or an exterior version for exclusive types.

Creation and annihilation operators

\[
C_i, A_i
\]

may satisfy generalized commutation relations

\[
A_i C_j
=
\theta_i \delta_{ij} I
+
\sigma C_j A_i,
\]

where:

- \(\sigma = 1\) gives bosonic or accumulative ontology.
- \(\sigma = -1\) gives fermionic or exclusive ontology.
- \(\sigma = 0\) gives strict linear or resource-sensitive ontology.

This provides a bridge to process algebra, linear logic, and quantum-like ontologies.

---

## 9. Dynamic Existential Logic

We now introduce a logical calculus internal to DMO.

### Definition 9.1: Syntax

Let \(\mathsf{Prop}\) be a set of atomic propositions. The formulas of **Dynamic Existential Logic** are generated by

\[
\varphi,\psi
::=
p
\mid
\varphi \wedge \psi
\mid
\varphi \vee \psi
\mid
\varphi \Rightarrow \psi
\mid
E_q \varphi
\mid
\langle \lambda \rangle \varphi
\mid
[\lambda]\varphi
\mid
\mathsf{C}_A \varphi
\mid
\mathsf{A}_A \varphi.
\]

Here:

- \(E_q \varphi\) asserts that \(\varphi\) holds with existence degree at least \(q\).
- \(\langle \lambda \rangle \varphi\) asserts that after some \(\lambda\)-transition, \(\varphi\) holds.
- \([\lambda]\varphi\) asserts that after every \(\lambda\)-transition, \(\varphi\) holds.
- \(\mathsf{C}_A \varphi\) asserts that after creation of \(A\), \(\varphi\) holds.
- \(\mathsf{A}_A \varphi\) asserts that after annihilation of \(A\), \(\varphi\) holds.

### Semantics

A formula \(\varphi\) is interpreted as a function

\[
\llbracket \varphi \rrbracket
:
\operatorname{Obj}(\mathsf{P})
\to
Q.
\]

For a transition label \(\lambda\), define

\[
\llbracket \langle \lambda \rangle \varphi \rrbracket(A,t)
=
\bigvee_{f:(A,t)\to_\lambda(B,s)}
\left(
\rho(f) \otimes \llbracket \varphi \rrbracket(B,s)
\right).
\]

If \(Q\) is residuated, define

\[
\llbracket [\lambda]\varphi \rrbracket(A,t)
=
\bigwedge_{f:(A,t)\to_\lambda(B,s)}
\left(
\rho(f) \Rightarrow \llbracket \varphi \rrbracket(B,s)
\right).
\]

The creation modality is interpreted by

\[
\llbracket \mathsf{C}_A \varphi \rrbracket(V,t)
=
\rho(c_{t,A})
\otimes
\llbracket \varphi \rrbracket(A,s).
\]

The annihilation modality is interpreted by

\[
\llbracket \mathsf{A}_A \varphi \rrbracket(A,t)
=
\rho(a_{t,A})
\otimes
\llbracket \varphi \rrbracket(V,s).
\]

The existence modality is interpreted by thresholding:

\[
\llbracket E_q \varphi \rrbracket(A,t)
=
\begin{cases}
1, & \text{if } q \leq \llbracket \varphi \rrbracket(A,t), \\
0, & \text{otherwise},
\end{cases}
\]

in the Boolean case, or more generally by a residuated threshold operator.

### Axioms

1. **Monotonicity of existence**

   If \(q \leq r\), then

   \[
   E_r \varphi \to E_q \varphi.
   \]

2. **Dynamic K axiom**

   \[
   [\lambda](\varphi \to \psi)
   \to
   ([\lambda]\varphi \to [\lambda]\psi).
   \]

3. **Duality**

   \[
   \langle \lambda \rangle \varphi
   \leftrightarrow
   \neg [\lambda]\neg\varphi
   \]

   when negation is available.

4. **Creation axiom**

   \[
   \mathsf{C}_A \top
   \to
   E_{\gamma_A} \top.
   \]

5. **Annihilation axiom**

   \[
   \mathsf{A}_A \top
   \to
   \text{Vac}.
   \]

   Here \(\text{Vac}\) denotes the proposition that the current state is vacuum.

6. **Persistence axiom**

   If \(P\) is a persistent invariant, then

   \[
   P \to [\lambda]P.
   \]

### Theorem 9.2: Soundness

If a formula \(\varphi\) is derivable in Dynamic Existential Logic, then for every DMO model \(\mathcal{D}\),

\[
\llbracket \varphi \rrbracket(A,t) = 1
\]

for all objects \((A,t)\).

**Proof sketch.**  
The semantic clauses are constructed so that each axiom evaluates to top. Modus ponens preserves top because the implication is residuated. The dynamic K axiom follows from the meet-preservation of the box modality. Creation and annihilation axioms follow from the transition-strength inequalities. Persistence follows from the invariance condition \(fP=Pf\). ∎

Completeness is an open problem and depends on the chosen quantale and transition category.

---

## 10. Examples

### Example 10.1: Boolean two-state ontology

Let

\[
Q = \{0,1\},
\]

and let there be two objects:

\[
V, \quad A.
\]

Let

\[
e_t(V)=1.
\]

At stage \(0\), let

\[
e_0(A)=0.
\]

Introduce a creation transition

\[
c : (V,0) \to (A,1)
\]

with

\[
\rho(c)=1.
\]

Then the propagation law gives

\[
e_1(A)
\geq
e_0(V) \otimes \rho(c)
=
1 \otimes 1
=
1.
\]

Hence

\[
e_1(A)=1.
\]

The object \(A\) comes into existence.

If we add annihilation

\[
a : (A,1) \to (V,2),
\]

with \(\rho(a)=1\), then

\[
e_2(V)
\geq
e_1(A) \otimes 1
=
1.
\]

The vacuum remains fully actual.

---

### Example 10.2: Fuzzy concept actualization

Let

\[
Q = [0,1]
\]

with product t-norm.

Suppose a concept \(B\) is potentially related to concept \(A\) by evidence transition \(\lambda\) with strength

\[
\rho_\lambda = 0.7.
\]

If

\[
e_t(A)=0.8,
\]

then the induced existence of \(B\) is at least

\[
e_s(B)
\geq
0.8 \cdot 0.7
=
0.56.
\]

If there are multiple supporting transitions, the closure rule uses the supremum:

\[
e_s(B)
=
e_s(B)
\vee
\bigvee_i
e_t(A_i) \rho_i.
\]

This gives a natural model of evidential or probabilistic actualization.

---

### Example 10.3: Linear tensor model

Let

\[
M = Q^2
\]

with basis

\[
e_0 = \text{vacuum mode},
\qquad
e_1 = \text{object mode}.
\]

Before creation, let

\[
E_0
=
\begin{pmatrix}
1 & 0 \\
0 & 0
\end{pmatrix}.
\]

After creation, let

\[
E_1
=
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}.
\]

The creation vector is

\[
C =
\begin{pmatrix}
0 \\
1
\end{pmatrix}.
\]

The annihilation covector is

\[
A =
\begin{pmatrix}
0 & 1
\end{pmatrix}.
\]

Then

\[
A C = 1.
\]

The induced projector onto the created object is

\[
P = C A
=
\begin{pmatrix}
0 & 0 \\
0 & 1
\end{pmatrix}.
\]

One checks

\[
P^2 = P.
\]

The object mode becomes actual after the creation transition.

---

## 11. Applications

Dynamic Mathematical Ontology is not merely a metaphysical formalism. It provides structural tools for several mathematical and computational domains.

---

### 11.1 Foundations of mathematics

Classical set theory assumes a fixed universe \(V\). DMO suggests replacing this with a dynamic family of universes or structural stages.

A set may be:

- potential,
- partially actualized,
- fully actual,
- preserved across extensions,
- collapsed or annihilated.

This is particularly relevant to forcing.

Let \(M\) be a ground model and \(\mathbb{P}\) a forcing notion. A \(\mathbb{P}\)-name \(\dot{x}\) is a potential object. Its existence degree in a Boolean-valued model may be taken as

\[
e(\dot{x}) = \llbracket \dot{x} \neq \varnothing \rrbracket.
\]

A generic extension

\[
M \subseteq M[G]
\]

is an ontological transition. The interpretation map

\[
\dot{x} \mapsto \dot{x}_G
\]

is an actualization operator.

Persistence appears in the fact that ordinals, well-foundedness, and many ground-model facts persist through forcing. Thus DMO gives a categorical and quantale-valued semantics for potentialist set theory.

---

### 11.2 Logic

DMO generalizes several logical traditions.

1. **Free logic**  
   Terms may fail to denote existing objects. Existence becomes an explicit operator.

2. **Modal logic**  
   Transitions induce possibility and necessity operators.

3. **Linear logic**  
   Creation and annihilation correspond to resource introduction and elimination.

4. **Constructive mathematics**  
   Existence is tied to actualization by proof or construction.

5. **Dynamic epistemic logic**  
   Existence degrees may encode knowledge, evidence, or information availability.

The logic \(E_q\varphi\) allows one to reason not only about truth but about the degree to which a truth is ontologically available.

---

### 11.3 Computer science

DMO has natural computational interpretations.

#### Memory allocation

Let objects be heap locations. Existence means allocated and reachable. Creation is allocation; annihilation is deallocation or garbage collection.

A transition is a program step. The compatibility condition

\[
f = E_s f E_t
\]

prevents use-after-free: a program step cannot act on a non-actual heap location.

#### Linear types and session types

Linear resources must be created and consumed exactly once. This corresponds to the case where the quantale is resource-sensitive and creation–annihilation yield satisfies

\[
\theta = 1.
\]

#### Process calculi

In the \(\pi\)-calculus, names and channels are created, passed, and garbage-collected. DMO gives an ontological semantics for name creation and scope extrusion.

#### Program invariants

Structural persistence corresponds to program invariants. If \(P\) is an invariant and \(T\) is a program transition, then

\[
T P = P T.
\]

Thus persistence theorem becomes a categorical invariant-preservation theorem.

---

### 11.4 Formal knowledge systems

In knowledge graphs, databases, and ontologies, entities change over time.

An entity may be:

- created,
- merged,
- split,
- deprecated,
- restored,
- assigned a confidence value.

Let \(Q=[0,1]\). An entity’s existence degree may represent confidence, temporal validity, or evidential support.

A merge transition

\[
f : (A,t) \to (C,s)
\]

may satisfy

\[
e_s(C)
\geq
e_t(A) \vee e_t(B).
\]

Structural persistence provides formal identity criteria: the persistent core may be an invariant identifier, schema key, or essential relation.

Creation and annihilation correspond to entity insertion and deletion. DMO gives a categorical foundation for schema evolution, temporal knowledge graphs, and belief revision.

---

## 12. Open Problems

Several directions remain open.

1. **Completeness of Dynamic Existential Logic**  
   For which quantales and transition categories is the logic complete?

2. **Higher categorical DMO**  
   Existence operators and transitions should be lifted to \(\infty\)-categories and homotopical settings.

3. **Quantum ontologies**  
   The Fock-style creation/annihilation calculus suggests connections to quantum field theory and categorical quantum mechanics.

4. **Internal language**  
   A type theory whose terms are ontological transitions and whose types are dynamic existence operators should be developed.

5. **Set-theoretic models**  
   A full DMO semantics for forcing, large cardinal potentialism, and Boolean-valued universes remains to be constructed.

6. **Computational implementations**  
   DMO could inform dynamic ontology languages, provenance systems, and resource-aware databases.

---

## 13. Conclusion

Dynamic Mathematical Ontology proposes a formal shift: existence is not a static background condition but a mathematically governed process. By introducing existence operators, ontological transitions, structural persistence, and creation/annihilation maps, we obtain a unified framework for reasoning about becoming, actualization, and destruction.

The theory combines quantale-valued degrees, graded monoidal categories, process categories, tensorial calculus, and modal logic. It conservatively extends static ontology: when existence operators are constant and transitions are identities, DMO reduces to ordinary static mathematics. In its full form, however, it provides a language for dynamic foundations, resource-sensitive logic, computational state evolution, and formal knowledge systems.

The central thesis is therefore:

> To exist mathematically is not merely to be an element of a fixed universe; it is to be actualized by an operator, preserved through transitions, and governed by formal laws of creation and annihilation.

---
