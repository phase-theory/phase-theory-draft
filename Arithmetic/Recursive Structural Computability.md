# Recursive Structural Computability

**Preprint**

## Abstract

This paper develops **Recursive Structural Computability** (RSC), a formal framework in which computation is defined not as manipulation of fixed symbolic strings over static alphabets, but as the recursive transformation of mathematical structures. In RSC, the fundamental computational states are typed relational or algebraic structures, programs are structure-transforming morphisms or rewrite systems, and recursion is interpreted as the generation of evolving structural trajectories whose limits, normal forms, or invariants constitute outputs. We introduce a category-theoretic and tensorial semantics for structural transformations, define an operational calculus of primitive structural operations, rewrite rules, guarded recursion, and structural search, and establish the metatheory of RSC: universality, undecidability of structural halting, a structural analogue of Rice’s theorem, and a recursion theorem for self-referential structural programs. A tensor calculus for structural evolution is developed, allowing transformations to be represented as kernels, contractions, and polynomial operators over semirings. We then define structural complexity classes, including RSC-P, RSC-NP, and parameterized structural classes based on width, depth, and entanglement. Finally, we discuss applications to theoretical computer science, complexity theory, automated reasoning, and artificial intelligence. The central claim is that RSC preserves the extensional boundary of Turing computability while substantially refining the intensional ontology of computation: what is computed is no longer a string function but a structural trajectory, and what is measured is not merely time and space but structural depth, relational entanglement, and transformational complexity.

**Keywords:** computability, structural computation, recursive transformations, category theory, tensor calculus, graph rewriting, complexity theory, automated reasoning, world models.

---

## 1. Introduction

Classical computability theory is built on a stable symbolic substrate: natural numbers, words, tapes, terms, or finite sequences. A computation is a map from an input encoding to an output encoding, and the structure of the objects being represented is usually external to the computational formalism. This paradigm is powerful, but it obscures a fact central to modern mathematics and computer science: many computational processes do not operate on static strings, but on **structures** that evolve, decompose, quotient, bind, extend, and reorganize themselves.

Examples include:

- graph algorithms that transform connectivity, flow, or dependency structure;
- theorem provers that transform sequents, proof graphs, term algebras, and constraint systems;
- program analyzers that propagate dataflow facts over control-flow structures;
- algebraic completion procedures such as Knuth–Bendix or Gröbner basis construction;
- neural and neurosymbolic systems that update relational latent states;
- self-modifying or self-improving systems whose own computational architecture is transformed during execution.

In such settings, the natural object of computation is not a fixed string but a **mathematical structure undergoing recursive transformation**.

Recursive Structural Computability (RSC) formalizes this perspective. The framework is organized around four principles.

1. **Structures are first-class computational states.**  
   A state is a typed relational, algebraic, or categorical structure, not merely an encoding.

2. **Programs are structural transformations.**  
   A program is a morphism, rewrite rule, tensor operator, or recursive functional acting on structures.

3. **Recursion generates structural trajectories.**  
   Recursive programs define sequences or chains of structures whose fixed points, normal forms, or invariants are outputs.

4. **Complexity is intrinsic to structural change.**  
   Cost is measured by transformational depth, matching complexity, tensor rank, gluing size, quotient complexity, and relational entanglement.

The present paper gives a self-contained formal foundation for RSC. We define structural universes, effective presentations, structural programs, operational and denotational semantics, tensorial representations, complexity classes, and application domains. The resulting theory is deliberately general: it can be instantiated over graphs, relational databases, term algebras, proof systems, algebraic presentations, causal graphs, or latent structures in machine learning.

The principal contributions are as follows.

- A formal definition of RSC programs as recursively defined structural transformations.
- An operational semantics based on structural rewriting and pushout gluing.
- A denotational semantics based on continuous functionals over partial structures.
- A tensor calculus for structural transformations and recursive structural evolution.
- Metatheoretic results: universality, undecidability, structural Rice theorem, and self-reference.
- Structural complexity classes and parameterized structural measures.
- Applications to theoretical computer science, automated reasoning, complexity theory, and AI.

---

## 2. Structural Universes and Effective Presentations

### 2.1 Typed relational structures

Fix a finite typed signature

\[
\Sigma = (S, R, \operatorname{ar}),
\]

where \(S\) is a finite set of sorts, \(R\) is a finite set of relation symbols, and

\[
\operatorname{ar}: R \to S^{*}
\]

assigns to each relation symbol a finite sequence of sorts. Functions can be encoded as relations with functionality constraints, and constants as nullary functions or distinguished elements.

A finite \(\Sigma\)-structure \(A\) consists of:

1. a finite carrier set \(A_s\) for each sort \(s \in S\);
2. for each relation symbol \(r \in R\) with arity \((s_1,\dots,s_k)\), a relation

\[
R^A_r \subseteq A_{s_1} \times \cdots \times A_{s_k}.
\]

A homomorphism \(f:A \to B\) is a family of maps \(f_s:A_s \to B_s\) preserving relations:

\[
(a_1,\dots,a_k) \in R^A_r
\implies
(f_{s_1}(a_1),\dots,f_{s_k}(a_k)) \in R^B_r.
\]

Let \(\mathbf{FinStr}_\Sigma\) denote the category of finite \(\Sigma\)-structures and homomorphisms. When embeddings are required, as in many rewriting systems, one restricts to the subcategory of injective homomorphisms.

### 2.2 Effective presentations

To make structures computationally accessible, we work with **effective presentations**.

A finite presentation \(p\) is a finite description of a structure by generators, sorts, relations, equations, or constraints. Its interpretation is a structure

\[
\llbracket p \rrbracket.
\]

Two presentations \(p,q\) are equivalent if

\[
\llbracket p \rrbracket \cong \llbracket q \rrbracket.
\]

We fix an effective enumeration of presentations

\[
p_0,p_1,p_2,\dots
\]

and a Gödel coding

\[
\ulcorner p \urcorner \in \mathbb{N}.
\]

For a finite structure \(A\), we write \(\ulcorner A \urcorner\) for the code of some chosen presentation of \(A\). For computability-theoretic results, only effectiveness of presentation and decoding is required. For complexity-theoretic results, we often use **rigid ordered presentations**, where a distinguished linear order is included in the signature, thereby eliminating presentation ambiguity up to ordered isomorphism.

### 2.3 Structural maps and invariance

The natural maps in RSC are not arbitrary functions on codes but **structural maps**.

A partial map

\[
F:\operatorname{Obj}(\mathbf{FinStr}_\Sigma) \rightharpoonup \operatorname{Obj}(\mathbf{FinStr}_\Sigma)
\]

is called **structural** if it is invariant under isomorphism:

\[
A \cong B
\implies
\left(
F(A)\downarrow \iff F(B)\downarrow
\right)
\]

and, when defined,

\[
F(A) \cong F(B).
\]

This condition expresses that computation depends on structure, not on accidental presentation. In ordered or rigid encodings, isomorphism invariance may be weakened to order-preserving invariance, enabling simulation of ordinary symbolic computation.

---

## 3. The RSC Calculus

RSC programs are built from primitive structural operations, structural rewrite rules, composition, conditionals, recursion, and search.

### 3.1 Primitive structural operations

The primitive operations are effective transformations of finite structures. Typical primitives include:

1. **Identity**

\[
\mathbf{id}: A \mapsto A.
\]

2. **Empty structure**

\[
\varnothing_\Sigma.
\]

3. **Singleton generation**

\[
\mathbf{1}_s
\]

for a sort \(s\).

4. **Disjoint union / coproduct**

\[
A \sqcup B.
\]

5. **Monoidal structural product**

\[
A \otimes B.
\]

The product may be categorical product, tensor product of relational structures, or another effective monoidal structure.

6. **Substructure selection**

\[
\operatorname{Sub}(A,\varphi),
\]

where \(\varphi\) is a decidable structural predicate.

7. **Quotienting**

\[
\operatorname{Quot}(A,E),
\]

where \(E\) is a definable equivalence relation on \(A\).

8. **Free extension**

\[
\operatorname{Free}_\Sigma(X)
\]

generated by a finite set \(X\).

9. **Gluing**

\[
\operatorname{Glue}_I(A,B),
\]

the pushout gluing of \(A\) and \(B\) along an interface \(I\).

10. **Relation insertion and deletion**

\[
\operatorname{Add}_r(a_1,\dots,a_k),
\qquad
\operatorname{Del}_r(a_1,\dots,a_k).
\]

11. **Reduct and expansion**

\[
\operatorname{Reduct}_\Gamma(A),
\qquad
\operatorname{Expand}(A,\psi).
\]

These operations are assumed to be effective: given finite presentations, one can compute presentations of the output structures.

### 3.2 Structural rewrite rules

A central mechanism in RSC is structural rewriting.

A rewrite rule is a span of finite structures

\[
L \xleftarrow{\ell} I \xrightarrow{r} R,
\]

where:

- \(L\) is the left-hand side pattern;
- \(R\) is the right-hand side replacement;
- \(I\) is the interface preserved by the rule.

A rule applies to a structure \(A\) via a match

\[
m:L \to A.
\]

Under appropriate dangling conditions, the direct transformation

\[
A \Rightarrow_{\rho,m} B
\]

is obtained by deleting the part of \(m(L)\) not required by the interface and gluing in \(R\). Categorically, this is expressed by pushout diagrams. In the double-pushout formulation, one forms

\[
A \leftarrow L \rightarrow D
\]

and then

\[
D \leftarrow I \rightarrow R,
\]

yielding \(B\).

This gives a local, compositional account of structural change.

### 3.3 Syntax of RSC programs

Let \(\mathcal{B}\) be a set of decidable structural predicates. RSC programs are generated by the grammar

\[
P ::=
\mathbf{skip}
\mid
\mathbf{fail}
\mid
\rho
\mid
P;Q
\mid
\mathbf{if}\ \beta\ \mathbf{then}\ P\ \mathbf{else}\ Q
\mid
\mathbf{while}\ \beta\ \mathbf{do}\ P
\mid
\mathbf{rec}\ X.P
\mid
\mu X.\beta(X).
\]

Here:

- \(\rho\) is a structural rewrite rule or primitive operation;
- \(P;Q\) is sequential composition;
- \(\beta\) is a decidable structural predicate;
- \(\mathbf{rec}\ X.P\) defines a recursive structural transformation by self-reference;
- \(\mu X.\beta(X)\) is a structural search operator returning the least structure, under a fixed effective enumeration, satisfying \(\beta\).

The search operator may diverge if no such structure exists. It supplies the analogue of unbounded minimization.

### 3.4 Operational semantics

A configuration is a pair

\[
(P,A),
\]

where \(P\) is a program and \(A\) is a finite structure.

The small-step reduction relation is written

\[
(P,A) \longrightarrow (Q,B).
\]

Key rules include:

1. **Sequential composition**

\[
(P;Q,A) \longrightarrow (P,A),
\]

with continuation handling after \(P\) terminates.

2. **Rule application**

If \(A \Rightarrow_{\rho,m} B\), then

\[
(\rho,A) \longrightarrow (\mathbf{skip},B).
\]

3. **Conditional branching**

If \(\beta(A)\) holds,

\[
(\mathbf{if}\ \beta\ \mathbf{then}\ P\ \mathbf{else}\ Q,A)
\longrightarrow
(P,A),
\]

otherwise

\[
(\mathbf{if}\ \beta\ \mathbf{then}\ P\ \mathbf{else}\ Q,A)
\longrightarrow
(Q,A).
\]

4. **While iteration**

If \(\beta(A)\) holds,

\[
(\mathbf{while}\ \beta\ \mathbf{do}\ P,A)
\longrightarrow
(P; \mathbf{while}\ \beta\ \mathbf{do}\ P,A),
\]

otherwise

\[
(\mathbf{while}\ \beta\ \mathbf{do}\ P,A)
\longrightarrow
(\mathbf{skip},A).
\]

5. **Recursive unfolding**

\[
(\mathbf{rec}\ X.P,A)
\longrightarrow
(P[\mathbf{rec}\ X.P / X],A).
\]

6. **Structural search**

\[
(\mu X.\beta(X),A)
\longrightarrow
(\mathbf{skip},C)
\]

where \(C\) is the first structure in the canonical enumeration satisfying \(\beta\), if such a structure exists.

A computation terminates when it reaches

\[
(\mathbf{skip},B),
\]

and the output is \(B\). Divergence is represented by infinite reduction sequences.

### 3.5 Denotational semantics

To give a compositional semantics, define a domain \(\mathcal{D}_\Sigma\) of partial finite \(\Sigma\)-structures ordered by information extension:

\[
A \sqsubseteq B
\]

if \(B\) extends \(A\) by additional defined elements or relations. The least element is

\[
\bot,
\]

the completely undefined structure.

An RSC program \(P\) denotes a continuous function

\[
\llbracket P \rrbracket : \mathcal{D}_\Sigma \to \mathcal{D}_\Sigma.
\]

The semantic clauses are:

\[
\llbracket \mathbf{skip} \rrbracket = \mathbf{id},
\]

\[
\llbracket P;Q \rrbracket = \llbracket Q \rrbracket \circ \llbracket P \rrbracket,
\]

\[
\llbracket \mathbf{if}\ \beta\ \mathbf{then}\ P\ \mathbf{else}\ Q \rrbracket(A)
=
\begin{cases}
\llbracket P \rrbracket(A), & \beta(A) \text{ true},\\
\llbracket Q \rrbracket(A), & \beta(A) \text{ false},
\end{cases}
\]

and

\[
\llbracket \mathbf{while}\ \beta\ \mathbf{do}\ P \rrbracket
=
\operatorname{lfp}\left(F \mapsto
A \mapsto
\begin{cases}
F(\llbracket P \rrbracket(A)), & \beta(A),\\
A, & \neg \beta(A)
\end{cases}
\right).
\]

For recursion, let \(P\) contain a program variable \(X\). It defines a continuous functional

\[
\Phi_P(f) = \llbracket P \rrbracket_{X=f}.
\]

Then

\[
\llbracket \mathbf{rec}\ X.P \rrbracket
=
\operatorname{lfp}(\Phi_P).
\]

By the Kleene fixed-point theorem,

\[
\operatorname{lfp}(\Phi_P)
=
\bigsqcup_{n \ge 0} \Phi_P^n(\bot).
\]

This equation is the denotational core of RSC: recursion is the progressive construction of a structure through an ascending chain of approximations.

### 3.6 Adequacy

**Theorem 3.1 (Adequacy).**  
For every RSC program \(P\) and finite structure \(A\), if

\[
(P,A) \Downarrow B
\]

operationally, then

\[
\llbracket P \rrbracket(A)=B.
\]

Conversely, if \(\llbracket P \rrbracket(A)=B\) and \(B\) is finite and compact, then there exists a terminating operational derivation

\[
(P,A) \Downarrow B.
\]

**Proof sketch.**  
The first direction is by induction on the length of the operational derivation. Primitive rules are sound by construction. Sequential composition and conditionals follow from the semantic clauses. Recursion follows because operational unfolding generates the Kleene chain approximating the least fixed point. The converse follows by compactness: a finite output is reached at some finite stage of the chain, and the operational rules can realize that finite approximation. \(\square\)

---

## 4. Recursive Structural Computability

### 4.1 RSC-computable transformations

A partial structural transformation

\[
F:\operatorname{Obj}(\mathbf{FinStr}_\Sigma) \rightharpoonup \operatorname{Obj}(\mathbf{FinStr}_\Sigma)
\]

is **RSC-computable** if there exists an RSC program \(P\) such that for every finite structure \(A\),

\[
\llbracket P \rrbracket(A) \cong F(A)
\]

whenever \(F(A)\) is defined, and both are undefined together.

The collection of all RSC-computable transformations is denoted

\[
\mathsf{RSC}_\Sigma.
\]

### 4.2 Effective realizability

**Theorem 4.1 (Effective realizability).**  
Every RSC-computable transformation is partial recursive on structure codes.

That is, if \(F\) is RSC-computable, there exists a partial recursive function

\[
\varphi_F:\mathbb{N} \rightharpoonup \mathbb{N}
\]

such that

\[
\varphi_F(\ulcorner A \urcorner)=\ulcorner F(A) \urcorner
\]

whenever \(F(A)\) is defined.

**Proof.**  
The proof is by structural induction on RSC programs.

- Primitive structural operations are effective by assumption.
- Rewrite rule application is effective because finite matching and pushout construction are decidable for finite presentations.
- Sequential composition corresponds to composition of partial recursive functions.
- Conditionals are computable because structural predicates are decidable.
- While loops correspond to effective iteration.
- Recursive programs are interpreted by computable Kleene chains.
- The search operator corresponds to unbounded minimization over an effective enumeration of finite structures.

Thus the entire program can be compiled into a Turing machine operating on codes. \(\square\)

Therefore RSC does not exceed Turing computability extensionally.

### 4.3 Structural completeness

To obtain a converse, we impose a standard presentation discipline. Assume the signature contains a distinguished linear order, or otherwise that inputs are given in rigid effective presentations.

**Theorem 4.2 (Structural completeness under rigid presentations).**  
Let \(F\) be a partial map on finite structures such that:

1. \(F\) is invariant under ordered isomorphism;
2. there exists a partial recursive function \(\varphi\) with

\[
\varphi(\ulcorner A \urcorner)=\ulcorner F(A) \urcorner
\]

whenever defined.

Then \(F\) is RSC-computable.

**Proof sketch.**  
An RSC program first converts the input structure into its ordered code representation as a rigid structure. It then simulates the Turing machine computing \(\varphi\) using local structural rewrite rules over a graph encoding of the Turing machine tape, state, and transition relation. Upon halting, it decodes the output code into a finite structure. Because all simulation steps are finite local structural transformations, the resulting transformation is RSC-computable. \(\square\)

This result clarifies the position of RSC: it does not enlarge the class of computable functions, but it changes the **intensional structure** of computation. The same extensional function may have radically different structural programs, structural depths, tensor ranks, and transformational costs.

### 4.4 Universality

Because RSC programs are finite syntactic objects, they can be effectively enumerated:

\[
P_0,P_1,P_2,\dots
\]

Define the universal structural machine

\[
U(e,A) = \llbracket P_e \rrbracket(A).
\]

**Theorem 4.3 (Universality).**  
The function \(U\) is RSC-computable.

**Proof.**  
The interpreter simulates the operational semantics of \(P_e\) on \(A\). Each syntactic construct of RSC has an effective structural implementation. Recursive unfolding and search are simulated by dovetailing. \(\square\)

### 4.5 Undecidability of structural halting

Define the structural halting set

\[
\mathsf{HALT}_{\mathsf{RSC}}
=
\{(e,A): \llbracket P_e \rrbracket(A) \downarrow\}.
\]

**Theorem 4.4.**  
\(\mathsf{HALT}_{\mathsf{RSC}}\) is undecidable.

**Proof.**  
Reduce the ordinary Turing machine halting problem. Given a Turing machine \(M\) and input \(w\), construct a finite structure \(A_{M,w}\) encoding the initial tape, state, and transition table. Construct an RSC program \(P_M\) whose rewrite rules simulate one transition of \(M\) as a local structural transformation. Then

\[
P_M(A_{M,w}) \downarrow
\]

if and only if \(M(w)\) halts. If \(\mathsf{HALT}_{\mathsf{RSC}}\) were decidable, the classical halting problem would be decidable. Contradiction. \(\square\)

### 4.6 Structural Rice theorem

Let \(\mathcal{P}\) be a property of RSC-computable transformations. We say \(\mathcal{P}\) is extensional if

\[
\llbracket P \rrbracket = \llbracket Q \rrbracket
\implies
(\mathcal{P}(P) \iff \mathcal{P}(Q)).
\]

**Theorem 4.5 (Structural Rice theorem).**  
Every nontrivial extensional property of RSC-computable transformations is undecidable.

**Proof sketch.**  
Let \(\mathcal{P}\) be nontrivial. Choose programs \(P_0,P_1\) such that \(P_0\) lacks \(\mathcal{P}\) and \(P_1\) has \(\mathcal{P}\). Given an index \(e\) for a machine whose halting behavior is under investigation, construct a program \(Q_e\) that first simulates \(P_e\) on a fixed input. If the simulation halts, \(Q_e\) behaves as \(P_1\); otherwise it diverges or behaves as \(P_0\), depending on whether the totally undefined transformation satisfies \(\mathcal{P}\). Deciding \(\mathcal{P}\) would then decide halting. \(\square\)

### 4.7 Structural recursion theorem

**Theorem 4.6 (Structural recursion theorem).**  
Let

\[
h:\mathbb{N} \to \mathbb{N}
\]

be a computable function mapping indices of RSC programs to indices of RSC programs. Then there exists an index \(e\) such that

\[
\llbracket P_e \rrbracket
\cong
\llbracket P_{h(e)} \rrbracket.
\]

**Proof.**  
The proof follows the classical Kleene recursion theorem. Since RSC programs can be encoded as finite structures and interpreted by a universal RSC machine, the usual s-m-n construction applies. The only difference is that equality of computed transformations is taken up to structural isomorphism. \(\square\)

This theorem formalizes self-reference in RSC. It implies that RSC supports programs capable of transforming their own structural descriptions.

---

## 5. Tensorial Semantics of Structural Transformations

Structural transformations can often be represented as tensor operations over finite carriers. This is particularly useful for complexity analysis and for connections with algebraic, statistical, and neural computation.

### 5.1 Structural tensors

Assume, for simplicity, that the underlying carrier sets are fixed during a transformation. For each relation symbol \(r \in R\) of arity \(k\), define a tensor

\[
R^{(r)} \in \mathcal{K}^{n_1 \times \cdots \times n_k},
\]

where \(\mathcal{K}\) is a semiring and \(n_i\) is the size of the \(i\)-th sort component.

For Boolean relational structures, take

\[
\mathcal{K} = (\{0,1\}, \vee, \wedge).
\]

For weighted or probabilistic structures, one may use

\[
\mathcal{K} = (\mathbb{R}_{\ge 0}, +, \times)
\]

or another suitable semiring.

The full structure tensor is

\[
\mathbb{S}_A
=
\{ R^{(r)} \}_{r \in R}.
\]

Using multi-index notation, write

\[
R^{(r)}_{I_r},
\]

where

\[
I_r = (i_1,\dots,i_{\operatorname{ar}(r)}).
\]

Repeated indices are summed over the appropriate semiring operation, following an Einstein-like convention.

### 5.2 Linear structural kernels

A linear structural transformation over fixed carriers is given by a family of kernels

\[
K^{r'}_{I' J},
\]

mapping input relation tensors to output relation tensors:

\[
R'^{(r')}_{I'}
=
\bigoplus_{r \in R}
\bigoplus_{J}
K^{r'}_{I' J}
\otimes
R^{(r)}_{J}.
\]

Here \(\oplus\) and \(\otimes\) denote the semiring sum and product.

For the Boolean semiring, this becomes

\[
R'^{(r')}_{I'}
=
\bigvee_{r,J}
\left(
K^{r'}_{I'J}
\wedge
R^{(r)}_{J}
\right).
\]

### 5.3 Composition as contraction

Let \(\Phi\) and \(\Psi\) be linear structural transformations with kernels \(K\) and \(L\). Their composition \(\Psi \circ \Phi\) has kernel

\[
M^{r''}_{I'' J}
=
\bigoplus_{r',J'}
L^{r''}_{I'' J'}
\otimes
K^{r'}_{J' J}.
\]

Thus

\[
(\Psi \circ \Phi)(\mathbb{S})
=
\Psi(\Phi(\mathbb{S})).
\]

This is the structural analogue of matrix multiplication, generalized to higher-rank tensors and multiple relation symbols.

### 5.4 Polynomial structural operators

Many structural transformations are nonlinear. For example, the existence of a triangle depends on a conjunction of three edges. We therefore allow polynomial structural operators:

\[
R'^{(r')}_{I'}
=
\bigoplus_{m=1}^{M}
c_{m}
\bigotimes_{a=1}^{d_m}
\left(
\bigoplus_{J_{m,a}}
K^{r',m,a}_{I' J_{m,a}}
\otimes
R^{(r_{m,a})}_{J_{m,a}}
\right).
\]

Here \(d_m\) is the degree of the \(m\)-th monomial. In Boolean form, such operators express conjunctions and disjunctions of structural patterns.

For example, if \(E\) is an edge relation, the predicate “\(i,j,k\) form a triangle” is

\[
T_{ijk}
=
E_{ij} \wedge E_{jk} \wedge E_{ki}.
\]

In tensor notation,

\[
T_{ijk}
=
E_{ij} E_{jk} E_{ki}
\]

over the Boolean semiring.

### 5.5 Recursive structural evolution

A recursive structural transformation can be written as an iterative tensor evolution:

\[
\mathbb{S}^{(0)} = \mathbb{S},
\]

\[
\mathbb{S}^{(t+1)} = \Phi(\mathbb{S}^{(t)}).
\]

If \(\Phi\) is monotone with respect to the information order on tensors, then the sequence

\[
\mathbb{S}^{(0)}
\sqsubseteq
\mathbb{S}^{(1)}
\sqsubseteq
\mathbb{S}^{(2)}
\sqsubseteq
\cdots
\]

has a least upper bound. The output of the recursive process is

\[
\mu \Phi
=
\bigsqcup_{t \ge 0}
\Phi^t(\bot).
\]

In a finite lattice, this chain stabilizes. This gives a tensorial account of recursive structural computation.

### 5.6 Example: transitive closure

Let \(E\) be the edge tensor of a directed graph:

\[
E_{ij} = 1
\]

if there is an edge from \(i\) to \(j\), and \(0\) otherwise.

Define

\[
\Phi(E)_{ij}
=
E_{ij}
\vee
\bigvee_k
E_{ik} \wedge E_{kj}.
\]

In Einstein notation over the Boolean semiring,

\[
E'_{ij}
=
E_{ij}
\vee
E_{ik} E_{kj}.
\]

The transitive closure is

\[
E^{*}
=
\mu \Phi.
\]

**Proposition 5.1.**  
For finite graphs, \(E^{*}_{ij}=1\) if and only if there is a directed path from \(i\) to \(j\).

**Proof.**  
By induction on path length. If there is a path of length \(1\), \(E_{ij}=1\). If there is a path of length \(n+1\), there exists \(k\) such that \(i\) reaches \(k\) in \(n\) steps and \(k\) reaches \(j\) in one step. Monotone iteration of \(\Phi\) adds precisely such compositions. Since the graph is finite, the chain stabilizes after at most \(n-1\) nontrivial path-length increases. \(\square\)

This example illustrates the central RSC idea: a computable object is not directly given but is the fixed point of a recursive structural transformation.

---

## 6. Structural Complexity Theory

RSC induces a complexity theory in which cost is attached to structural transformation rather than to symbol manipulation alone.

### 6.1 Cost model

Let \(|A|\) denote the size of a finite structure \(A\). A typical definition is

\[
|A|
=
\sum_{s \in S} |A_s|
+
\sum_{r \in R} |R^A_r|.
\]

For a rewrite rule \(\rho\), the cost of one application includes:

1. the cost of finding a match;
2. the cost of checking applicability conditions;
3. the cost of constructing the pushout or replacement structure;
4. the cost of quotienting, if identifications are introduced.

For fixed rule size, matching cost is polynomial in \(|A|\), though the degree depends on the size of the left-hand side.

For tensor programs, cost is governed by contraction complexity. If a tensor operator has maximum rank \(d\), naive contraction costs on the order of

\[
O(|A|^d).
\]

Sparsity, symmetry, and decomposition can reduce this substantially.

### 6.2 Structural complexity classes

Define the following classes.

**Definition 6.1 (RSC-P).**  
A structural transformation \(F\) is in \(\mathsf{RSC}\text{-}\mathsf{P}\) if there exists a deterministic RSC program \(P\) computing \(F\) and a polynomial \(p\) such that for every input structure \(A\), the computation terminates within at most \(p(|A|)\) structural steps.

**Definition 6.2 (RSC-NP).**  
A structural transformation or decision problem is in \(\mathsf{RSC}\text{-}\mathsf{NP}\) if there exists a nondeterministic RSC program with polynomially bounded branches such that acceptance occurs iff some structural transformation path reaches a designated accepting structure.

**Definition 6.3 (Parameterized RSC).**  
Let \(\kappa(A)\) be a structural parameter, such as treewidth, modular width, quotient rank, or tensor rank. A transformation is in

\[
\mathsf{RSC}\text{-}\mathsf{FPT}(\kappa)
\]

if it can be computed in time

\[
f(\kappa(A)) \cdot |A|^{O(1)}.
\]

### 6.3 Structural parameters

Several intrinsic parameters are relevant.

1. **Structural depth.**  
   The maximum recursion depth needed to reach a normal form.

2. **Structural width.**  
   The maximum arity or tensor rank involved in a transformation.

3. **Gluing complexity.**  
   The size of interfaces used in pushout composition.

4. **Quotient complexity.**  
   The cost of computing equivalence closures or congruence closures.

5. **Entanglement.**  
   The degree to which multiple relation symbols must be jointly transformed.

A rough entanglement measure is the minimal number of relation tensors that must appear in the same monomial of a polynomial structural operator.

### 6.4 Closure properties

**Proposition 6.1.**  
\(\mathsf{RSC}\text{-}\mathsf{P}\) is closed under:

1. sequential composition;
2. bounded parallel composition;
3. polynomially bounded guarded recursion;
4. finite disjoint unions;
5. quotienting by polynomial-time decidable equivalence relations;
6. polynomial-time computable tensor contractions.

**Proof sketch.**  
Each operation increases total cost by at most polynomial factors, provided recursion depth and branching are polynomially bounded. Quotienting by an effectively computable equivalence relation can be implemented by union-find or closure propagation within polynomial cost. \(\square\)

### 6.5 Relation to classical complexity

When structures are encoded as ordered strings, RSC programs can simulate ordinary Turing machines by representing tapes, states, and transitions as structures.

**Theorem 6.1 (Classical correspondence).**  
Under rigid ordered encodings and polynomial primitive operations, the class of decision problems induced by \(\mathsf{RSC}\text{-}\mathsf{P}\) coincides with \(\mathsf{P}\).

**Proof sketch.**  
Every RSC-P program can be compiled into a polynomial-time Turing machine by Theorem 4.1 and the polynomial cost assumption. Conversely, any polynomial-time Turing machine can be simulated by a polynomial-size family of local structural rewrite rules acting on a graph encoding of the machine configuration. Since the number of simulated steps is polynomial, the resulting RSC program is polynomially bounded. \(\square\)

Thus RSC does not alter the extensional boundary of polynomial-time computability under standard encodings. Its advantage is **fine-grained**: it distinguishes computations by structural organization, recursion depth, and transformational locality.

### 6.6 Structural speedup

Many classical algorithms become naturally expressible as recursive structural decompositions.

Let \(A\) admit a decomposition tree \(T\), for example a tree decomposition, modular decomposition, or congruence decomposition. Suppose:

1. each bag or module has size at most \(w\);
2. the transformation \(\Phi\) is local to modules;
3. child summaries can be combined at cost \(g(w)\).

Then a recursive RSC program can compute the fixed point by traversing \(T\).

**Proposition 6.2 (Structural speedup).**  
Under the above conditions, the transformation can be computed in time

\[
O(|T| \cdot g(w)).
\]

If a naive global iteration costs

\[
O(|A|^\alpha),
\]

then RSC yields a speedup whenever

\[
|T| \cdot g(w) \ll |A|^\alpha.
\]

This explains the power of structural computation on bounded-width, modular, or hierarchically organized instances.

---

## 7. Applications

### 7.1 Theoretical computer science

RSC provides a unified semantics for several areas.

#### Program transformation

Programs, types, and control-flow graphs can be represented as structures. Program optimizations become structural rewrite rules. Recursive program analyses are fixed points of monotone structural operators.

#### Semantics of programming languages

Operational semantics can be represented as structural rewriting over syntactic structures with binding, contexts, and substitution. RSC gives a natural account of structural congruence, evaluation contexts, and higher-order reduction.

#### Type theory and dependent structures

Types can be treated as structural invariants. Type checking and elaboration become transformations of dependent structures. Recursive structural computation models normalization and proof normalization.

### 7.2 Complexity theory

RSC suggests a refinement of complexity analysis based not only on input size but on structural organization.

Potential directions include:

- structural parameterized complexity;
- complexity of quotient and congruence closure;
- tensor-rank-based lower bounds;
- structural compression and its effect on complexity;
- intrinsic complexity of isomorphism-invariant problems.

RSC also clarifies why certain problems are easy on structured instances: the recursive decomposition reduces effective structural depth and entanglement.

### 7.3 Automated reasoning

Automated reasoning is naturally structural.

#### Proof search as structural transformation

A proof state is a structure containing sequents, hypotheses, goals, and constraints. Inference rules are structural rewrite rules. Proof search is a trajectory in the space of proof structures.

A proof system can be represented as

\[
\Sigma_{\text{proof}} = (S_{\text{seq}}, R_{\text{infer}}),
\]

where sequents and inference relations are structural components.

#### Soundness and completeness

Let \(\mathcal{R}\) be a set of inference rules encoded as RSC rewrite rules.

Soundness means every structural transformation preserves validity:

\[
A \Rightarrow_{\rho} B
\implies
(\operatorname{Valid}(A) \Rightarrow \operatorname{Valid}(B)).
\]

Completeness means that for every provable theorem, there exists a finite RSC trajectory from axioms to the theorem under a fair search strategy.

#### Congruence closure

Given a set of equations \(E\) over terms, congruence closure is the least congruence containing \(E\). In RSC, this is a recursive quotient transformation:

\[
A_{t+1}
=
\operatorname{Quot}(A_t, E_t),
\]

where \(E_t\) is expanded by congruence rules:

\[
f(a_1,\dots,a_n) \sim f(b_1,\dots,b_n)
\]

whenever

\[
a_i \sim b_i
\]

for all \(i\).

Tensorially, if \(E_{ab}\) denotes equivalence, then for a unary function \(f\),

\[
E'_{f(a),f(b)}
=
E_{f(a),f(b)}
\vee
E_{a,b}.
\]

For \(n\)-ary \(f\),

\[
E'_{f(\bar a), f(\bar b)}
=
E_{f(\bar a), f(\bar b)}
\vee
\bigwedge_{i=1}^n E_{a_i,b_i}.
\]

The fixed point is the congruence closure.

### 7.4 Artificial intelligence

RSC provides a formal substrate for AI systems that reason over structured latent states.

#### Structural world models

Define a parameterized structural world model as a tuple

\[
\mathcal{W}_\theta
=
(S_0, \Phi_\theta, \Omega, R),
\]

where:

- \(S_0\) is an initial latent structure;
- \(\Phi_\theta\) is an RSC transformation parameterized by \(\theta\);
- \(\Omega\) is an observation extraction map;
- \(R\) is a reward or consistency functional.

The recursive evolution is

\[
S_{t+1}
=
\Phi_\theta(S_t).
\]

Learning consists in choosing \(\theta\) so that predicted structural trajectories match observed ones:

\[
\min_\theta
\sum_t
d\left(
\Phi_\theta(S_t),
S_{t+1}
\right),
\]

where \(d\) is a structural distance, such as edit distance, graph kernel distance, or tensor norm discrepancy.

#### Recursive self-improvement

A self-modifying agent may update not only its latent state but also its transformation rules:

\[
\theta_{t+1}
=
\Theta(\theta_t, S_t, \tau_t),
\]

where \(\tau_t\) is a trace of previous structural transformations. If \(\Theta\) is itself an RSC-computable transformation, the system remains within the RSC framework.

This gives a formal account of controlled self-modification: the agent’s architecture evolves, but its evolution is governed by computable structural rules and can be constrained by invariants.

#### Neurosymbolic integration

Tensorial RSC is compatible with neural architectures because tensor contractions can be learned approximately. A neural module may implement an approximate structural kernel

\[
K_\theta,
\]

while symbolic constraints enforce invariants such as:

- conservation of identity;
- causal acyclicity;
- type correctness;
- proof soundness;
- safety invariants.

Thus RSC can serve as a formal bridge between symbolic reasoning and learned structural dynamics.

---

## 8. Case Studies

### 8.1 Graph reachability and closure

Let \(G=(V,E)\). The reachability relation is the least fixed point of

\[
E_{ij}'
=
E_{ij}
\vee
E_{ik}E_{kj}.
\]

In RSC, this is not an algorithm imposed externally but a structural recursive definition. Different algorithms correspond to different structural schedules:

- naive iteration;
- Warshall-style ordered iteration;
- decomposition-based recursion;
- sparse tensor contraction.

The mathematical object is the same fixed point, but the structural complexity differs.

### 8.2 Dataflow analysis

A control-flow graph \(C\) carries dataflow facts \(D\). A dataflow analysis is a monotone structural operator

\[
\Phi(D,C).
\]

The analysis result is

\[
D^{*}
=
\mu_D \Phi(D,C).
\]

RSC expresses this directly as recursive transformation of the joint structure \((C,D)\). The structural perspective exposes opportunities for optimization through control-flow decomposition, loop nesting, and modular summarization.

### 8.3 Saturation-based theorem proving

In first-order theorem proving, clauses are structures and inference rules generate new clauses. Saturation is a recursive structural process:

\[
C_{t+1}
=
C_t
\cup
\operatorname{Infer}(C_t).
\]

The saturated set is a fixed point:

\[
C^{*}
=
\mu C. C \cup \operatorname{Infer}(C).
\]

RSC treats saturation as structural closure under transformation rules. Fairness conditions become conditions on structural trajectories.

---

## 9. Open Problems

RSC raises several research directions.

### 9.1 Intrinsic structural complexity

Can one define a presentation-independent complexity measure for structural transformations?

A candidate is

\[
C_{\mathrm{intr}}(F,A)
=
\min_{B \cong A}
C(F,B),
\]

but this may be hard to compute. More robust notions may use canonical decompositions or invariant cost models.

### 9.2 Optimal structural kernels

Given a transformation \(F\), what is the minimal tensor rank, depth, or entanglement required to compute it?

This leads to a structural analogue of circuit complexity.

### 9.3 Probabilistic and quantitative RSC

Replacing Boolean semirings with probabilistic or tropical semirings yields probabilistic structural computation. The fixed-point theory must then handle measures, expectations, and convergence conditions.

### 9.4 Infinite and coinductive structures

The present framework emphasizes finite structures. Extending RSC to infinite structures, domains, and coinductive transformations requires guarded recursion, metric semantics, or coalgebraic methods.

### 9.5 Certified RSC compilers

Because RSC programs transform structures, compilation must preserve not only input-output behavior but also structural invariants. Certified compilation from RSC to executable rewriting systems is a natural verification target.

### 9.6 Learning structural invariants

For AI applications, a central problem is learning invariants that constrain structural evolution:

\[
\forall t,\quad I(S_t) \text{ holds}.
\]

Combining learned kernels with proof-carrying invariants is a promising direction for safe recursive self-modification.

---

## 10. Conclusion

Recursive Structural Computability reframes computation as the recursive transformation of mathematical structures. Programs are not merely functions on encodings; they are structural morphisms, rewrite systems, tensor operators, and recursive functionals. The framework preserves the classical extensional limits of computability while providing a richer intensional vocabulary for analyzing computation in domains where structure itself evolves.

The formal apparatus developed here—operational rewriting, denotational fixed points, tensor calculus, universality, undecidability, and structural complexity—shows that RSC is not a metaphor but a rigorous computational paradigm. Its most significant consequences may lie not in changing what is computable, but in clarifying **how** computation organizes, decomposes, and transforms structure.

In this sense, RSC suggests a broader thesis:

> Computation is not primarily the manipulation of symbols; it is the law-governed evolution of structures.

---

## Appendix A. Notation

\[
\Sigma
\]

finite typed signature.

\[
\mathbf{FinStr}_\Sigma
\]

category of finite \(\Sigma\)-structures.

\[
\llbracket p \rrbracket
\]

structure denoted by presentation \(p\).

\[
\ulcorner A \urcorner
\]

code or presentation index of structure \(A\).

\[
\llbracket P \rrbracket
\]

denotation of RSC program \(P\).

\[
\mu \Phi
\]

least fixed point of monotone structural operator \(\Phi\).

\[
\mathbb{S}_A
\]

structure tensor of \(A\).

\[
\mathsf{RSC}\text{-}\mathsf{P}
\]

polynomial-time recursive structural transformations.

---

## Selected References

1. S. C. Kleene, *Introduction to Metamathematics*, 1952.  
2. A. M. Turing, “On Computable Numbers, with an Application to the Entscheidungsproblem,” 1936.  
3. A. Tarski, “A Lattice-Theoretical Fixpoint Theorem and Its Applications,” 1955.  
4. H. Ehrig, K. Ehrig, U. Prange, G. Taentzer, *Fundamentals of Algebraic Graph Transformation*, 2006.  
5. S. Mac Lane, *Categories for the Working Mathematician*, 1971.  
6. F. W. Lawvere, “Functorial Semantics of Algebraic Theories,” 1963.  
7. D. Sangiorgi, *Introduction to Bisimulation and Coinduction*, 2011.  
8. M. Droste, W. Kuich, H. Vogler, eds., *Handbook of Weighted Automata*, 2009.  
9. J. Pearl, *Causality*, 2009.  
10. T. G. Kolda, B. W. Bader, “Tensor Decompositions and Applications,” *SIAM Review*, 2009.
