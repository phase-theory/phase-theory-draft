# Universal Mathematical Compression Theory  
## Axiomatic Foundations, Tensorial Calculus, and Structural Applications

**Preprint**

---

## Abstract

We develop **Universal Mathematical Compression Theory (UMCoT)**, a formal theory of compression for arbitrary mathematical structures. Unlike classical information theory, which primarily compresses symbol sequences relative to a stochastic source, UMCoT treats compression as an intrinsic structural operation acting on mathematical objects themselves: groups, graphs, proofs, theories, tensors, relational databases, ontologies, and general finitely presented structures. The central object is a compression operator

\[
\mathfrak{C}:\mathcal{S}\rightarrow \mathcal{S},
\]

where \(\mathcal{S}\) is a category of structured presentations. The operator is constrained by axioms of **fidelity**, **reversibility**, and **optimality** relative to a chosen invariant functor and descriptive complexity measure. We give a categorical semantics of compression as selection of minimal representatives in essential-equivalence classes, prove idempotence and entropy-type lower bounds, formulate a tensorial calculus for composite structures, and establish the noncomputability of globally optimal compression in universal descriptive settings. Applications are developed to data compression, automated theorem proving, knowledge representation, and computational complexity. The resulting framework unifies minimum-description-length principles, proof compression, quotienting by symmetry, low-rank tensor approximation, and structure-preserving simplification under one axiomatic theory.

**Keywords:** compression, structural complexity, Kolmogorov complexity, category theory, tensor decomposition, theorem proving, knowledge representation, minimum description length.

---

## 1. Introduction

Compression is usually formulated as the transformation of a message into a shorter message from which the original can be recovered, either exactly or approximately. Classical source coding, Kolmogorov complexity, minimum description length, and lossy approximation theory each capture a facet of this phenomenon. However, in mathematics and mathematical computation, the objects to be compressed are often not strings but **structures**: algebraic objects, combinatorial objects, proofs, theories, categorical diagrams, relational schemas, tensors, and semantic knowledge bases.

For example:

- a finite group given by a multiplication table may be compressed by a short presentation;
- a graph may be compressed by quotienting by automorphisms or by low-rank approximation of its adjacency tensor;
- a proof may be compressed by extracting repeated subproofs as lemmas;
- an axiomatic theory may be compressed by replacing a redundant axiom set with a shorter equivalent one;
- a knowledge base may be compressed by passing to a query-equivalent core;
- a high-dimensional tensor may be compressed by tensor-rank decomposition while preserving selected contractions or spectral invariants.

These examples suggest that compression is not fundamentally about bits, but about **preserving essential invariants while reducing structural description cost**. UMCoT formalizes this principle.

The central claim of this paper is the following.

> **Thesis.** Compression is a universal structural operation: given a class of structures, a notion of essential invariant, and a descriptive complexity measure, an optimal compression operator selects, within each essential-equivalence class, a minimally describable representative.

We therefore introduce a compression operator

\[
\mathfrak{C}:\mathcal{S}\rightarrow \mathcal{S},
\]

subject to formal axioms. The operator acts on structured presentations, not merely on abstract isomorphism classes, because compression is sensitive to presentation, naming, coordinate choice, redundancy, and encoding. The invariant functor determines what is essential; the descriptive complexity measure determines what counts as short.

The contributions of this paper are:

1. an axiomatic definition of universal mathematical compression;
2. a categorical semantics of compression as optimal representative selection;
3. proofs of idempotence, entropy bounds, counting bounds, and noncomputability;
4. a tensorial calculus for composite and multilinear compression;
5. applications to data compression, automated theorem proving, knowledge representation, and complexity theory.

---

## 2. Structured Presentations, Invariants, and Descriptive Complexity

### 2.1 The category of structured presentations

Fix a universe of finitely describable mathematical presentations. Let

\[
\mathcal{S}
\]

denote a locally small category whose objects are **structured presentations**. An object \(S\in \mathcal{S}\) may be a finite algebra, a graph, a proof, a tensor with indices, a first-order theory, a database instance, an ontology, or a packaged compressed object together with reconstruction data.

Morphisms in \(\mathcal{S}\) are structure-preserving maps appropriate to the class under consideration: homomorphisms, interpretations, reductions, proof transformations, or tensor contractions. The precise choice of morphisms is part of the theory’s parameters.

A crucial point is that objects of \(\mathcal{S}\) are **presentations**, not bare semantic equivalence classes. Two presentations may represent the same mathematical content while having different descriptive costs. Compression acts on this difference.

We equip \(\mathcal{S}\) with a presentation-size functional

\[
\ell:\operatorname{Obj}(\mathcal{S})\rightarrow \mathbb{N}\cup\{\infty\}.
\]

For example, \(\ell(S)\) may count symbols, nonzero tensor entries, graph edges, proof inference steps, axioms, or stored parameters. In applications, \(\ell\) is the raw storage cost of the presentation.

### 2.2 Invariant functors and essential equivalence

Let \(\mathcal{M}\) be a category or metric category of invariant values, equipped with a distance

\[
d_{\mathcal{M}}:\operatorname{Obj}(\mathcal{M})\times \operatorname{Obj}(\mathcal{M})\rightarrow [0,\infty].
\]

An **invariant functor**

\[
\mathcal{I}:\mathcal{S}\rightarrow \mathcal{M}
\]

assigns to each structured presentation its essential semantic content. Examples include:

- the isomorphism class of a finite algebra;
- the theorem set of a formal theory;
- the query-answer semantics of an ontology;
- the decoded source message in lossless data compression;
- the low-order spectral moments of a tensor;
- the homotopy type of a topological presentation;
- the provable sequent associated with a proof.

For \(S,T\in\mathcal{S}\), define the invariant distance

\[
d_{\mathcal{I}}(S,T)
=
d_{\mathcal{M}}\bigl(\mathcal{I}(S),\mathcal{I}(T)\bigr).
\]

For \(\varepsilon\ge 0\), write

\[
S\approx_{\varepsilon}T
\quad\Longleftrightarrow\quad
d_{\mathcal{I}}(S,T)\le \varepsilon.
\]

When \(\varepsilon=0\), we write \(S\approx T\). The relation \(\approx_{\varepsilon}\) expresses **\(\varepsilon\)-fidelity** relative to the chosen invariants. If \(\mathcal{I}\) is complete for the intended semantics, then \(S\approx T\) is lossless semantic equivalence.

### 2.3 Descriptions and descriptive complexity

Let \(\Phi\) be a description scheme. Formally, \(\Phi\) consists of:

1. a finite alphabet \(\Sigma\);
2. a set of finite descriptions \(\Sigma^{*}\);
3. a partial semantic map

\[
\llbracket \cdot \rrbracket_{\Phi}:\Sigma^{*}\rightharpoonup \operatorname{Obj}(\mathcal{S}).
\]

A string \(\delta\in\Sigma^{*}\) describes the structured presentation

\[
S_{\delta}=\llbracket \delta\rrbracket_{\Phi}.
\]

The length of \(\delta\) is denoted \(|\delta|\).

The **descriptive complexity** of a structured presentation \(S\) relative to \(\Phi\) is

\[
\kappa_{\Phi}(S)
=
\min\left\{|\delta|:\llbracket\delta\rrbracket_{\Phi}=S\right\},
\]

with \(\kappa_{\Phi}(S)=\infty\) if no finite description exists.

More important for compression is the **essential descriptive complexity** of \(S\) at fidelity \(\varepsilon\):

\[
\kappa_{\Phi,\varepsilon}(S)
=
\inf\left\{
\kappa_{\Phi}(T):
T\in\mathcal{S},\ d_{\mathcal{I}}(S,T)\le \varepsilon
\right\}.
\]

This is the shortest description of any structure that preserves the essential invariants of \(S\) up to tolerance \(\varepsilon\).

When \(\varepsilon=0\),

\[
\kappa_{\Phi,0}(S)
=
\inf\left\{
\kappa_{\Phi}(T):
\mathcal{I}(T)=\mathcal{I}(S)
\right\}.
\]

Thus \(\kappa_{\Phi,\varepsilon}\) measures the intrinsic compressibility of \(S\) relative to the chosen invariant notion.

### 2.4 Fidelity, cost, and the charged-information principle

A compression theory must avoid artificial compression by hiding information outside the compressed object. We therefore adopt the **charged-information principle**:

> All information required to reconstruct the essential content of \(S\), including dictionaries, bases, codebooks, decompressors, or side parameters, must be included inside \(\mathfrak{C}(S)\) or charged in \(\kappa_{\Phi}(\mathfrak{C}(S))\).

This principle prevents pathological compressors that appear optimal only because they rely on an uncharged external oracle.

---

## 3. Axioms of Universal Mathematical Compression

We now define the central object of UMCoT.

### 3.1 Compression operators

Let \(\varepsilon\ge 0\). An **\(\varepsilon\)-compression operator** relative to \((\mathcal{S},\mathcal{I},\Phi)\) is a map

\[
\mathfrak{C}:\mathcal{S}\rightarrow \mathcal{S}
\]

satisfying the following axioms.

#### Axiom I: Fidelity

For every \(S\in\mathcal{S}\),

\[
d_{\mathcal{I}}\bigl(S,\mathfrak{C}(S)\bigr)\le \varepsilon.
\]

Equivalently,

\[
S\approx_{\varepsilon}\mathfrak{C}(S).
\]

Thus compression preserves the selected invariants up to tolerance \(\varepsilon\).

#### Axiom II: Reversibility where possible

There exists a decompression operator

\[
\mathfrak{D}:\mathcal{S}\rightarrow \mathcal{S}
\]

such that

\[
d_{\mathcal{I}}\bigl(S,\mathfrak{D}(\mathfrak{C}(S))\bigr)\le \varepsilon.
\]

If \(\varepsilon=0\) and the invariant functor is complete for the intended semantics, we require

\[
\mathcal{I}\bigl(\mathfrak{D}(\mathfrak{C}(S))\bigr)
=
\mathcal{I}(S).
\]

We distinguish three levels.

1. **Essential reversibility.**  
   The decompressor recovers a structure with the same essential invariants.

2. **Structural reversibility.**  
   The decompressor recovers an object equivalent to \(S\) under a specified equivalence relation stronger than invariant equality.

3. **Presentation reversibility.**  
   The decompressor recovers the original presentation exactly.

Presentation reversibility is rarely possible after genuine compression; essential reversibility is the natural universal requirement.

#### Axiom III: Optimality

For every \(S\in\mathcal{S}\),

\[
\kappa_{\Phi}\bigl(\mathfrak{C}(S)\bigr)
=
\kappa_{\Phi,\varepsilon}(S).
\]

Equivalently,

\[
\kappa_{\Phi}\bigl(\mathfrak{C}(S)\bigr)
=
\inf\left\{
\kappa_{\Phi}(T):
d_{\mathcal{I}}(S,T)\le \varepsilon
\right\}.
\]

Thus \(\mathfrak{C}(S)\) is a minimally describable representative of the \(\varepsilon\)-fidelity class of \(S\).

If the infimum is not attained, one may instead require \(\eta\)-optimality:

\[
\kappa_{\Phi}\bigl(\mathfrak{C}(S)\bigr)
\le
\kappa_{\Phi,\varepsilon}(S)+\eta.
\]

#### Axiom IV: Normality

There is a full subcategory

\[
\mathcal{N}\subseteq \mathcal{S}
\]

of **compressed normal forms** such that

\[
\mathfrak{C}(S)\in \mathcal{N}
\]

for all \(S\). Normality ensures that compressed objects have a canonical syntactic or structural shape: reduced proofs, canonical presentations, sparse tensors, quotient graphs, core ontologies, or normal-form theories.

#### Axiom V: Functoriality, when applicable

If compression is to be compatible with morphisms, then for each morphism

\[
f:S\rightarrow T
\]

there should exist a compressed morphism

\[
\mathfrak{C}(f):\mathfrak{C}(S)\rightarrow \mathfrak{C}(T)
\]

such that the diagram commutes up to controlled equivalence:

\[
\mathfrak{C}(f)\circ \mathfrak{C}(S)
\simeq
\mathfrak{C}(T)\circ f.
\]

In strict form,

\[
\mathfrak{C}(f)\circ \mathfrak{C}
=
\mathfrak{C}\circ f.
\]

This axiom is optional but desirable in categorical applications.

#### Axiom VI: Monoidal compatibility

If \((\mathcal{S},\otimes)\) is monoidal, compression should interact with tensorial composition. A natural compatibility condition is

\[
\mathfrak{C}(S\otimes T)
\approx_{\varepsilon}
\mathfrak{C}(S)\otimes \mathfrak{C}(T)\oplus \Delta(S,T),
\]

where \(\Delta(S,T)\) is the **correlation defect**, measuring information that is present only jointly in \(S\) and \(T\). If \(\Delta=0\), compression is separable. If \(\Delta\neq 0\), joint compression outperforms componentwise compression.

This axiom is fundamental for tensor compression, probabilistic graphical models, and composite proof systems.

---

## 4. Elementary Consequences

### 4.1 Compression does not increase optimal complexity

**Theorem 4.1.**  
Let \(\mathfrak{C}\) satisfy fidelity and optimality. Then

\[
\kappa_{\Phi}\bigl(\mathfrak{C}(S)\bigr)
\le
\kappa_{\Phi}(S).
\]

**Proof.**  
Since \(S\approx_{\varepsilon}S\), the object \(S\) itself belongs to the feasible class

\[
\{T:d_{\mathcal{I}}(S,T)\le \varepsilon\}.
\]

Therefore,

\[
\kappa_{\Phi,\varepsilon}(S)
\le
\kappa_{\Phi}(S).
\]

By optimality,

\[
\kappa_{\Phi}\bigl(\mathfrak{C}(S)\bigr)
=
\kappa_{\Phi,\varepsilon}(S),
\]

and the result follows. \(\square\)

Thus an admissible compressor cannot increase descriptive complexity relative to the chosen invariant class.

### 4.2 Idempotence of optimal compression

Assume \(\varepsilon=0\) and suppose \(\approx\) is transitive. Let

\[
\mathfrak{C}^{2}=\mathfrak{C}\circ \mathfrak{C}.
\]

**Theorem 4.2.**  
If \(\mathfrak{C}\) is losslessly optimal, then

\[
\kappa_{\Phi}\bigl(\mathfrak{C}^{2}(S)\bigr)
=
\kappa_{\Phi}\bigl(\mathfrak{C}(S)\bigr).
\]

If, in addition, compressed normal forms are unique up to isomorphism within each invariant class, then

\[
\mathfrak{C}^{2}(S)\cong \mathfrak{C}(S).
\]

**Proof.**  
By fidelity,

\[
\mathfrak{C}(S)\approx S.
\]

Applying compression to \(\mathfrak{C}(S)\),

\[
\mathfrak{C}^{2}(S)\approx \mathfrak{C}(S)\approx S.
\]

Hence \(\mathfrak{C}^{2}(S)\) is feasible for \(S\). Optimality for \(S\) gives

\[
\kappa_{\Phi}\bigl(\mathfrak{C}(S)\bigr)
\le
\kappa_{\Phi}\bigl(\mathfrak{C}^{2}(S)\bigr).
\]

But \(\mathfrak{C}^{2}(S)\) is the compression of \(\mathfrak{C}(S)\), so optimality applied to \(\mathfrak{C}(S)\) gives

\[
\kappa_{\Phi}\bigl(\mathfrak{C}^{2}(S)\bigr)
\le
\kappa_{\Phi}\bigl(\mathfrak{C}(S)\bigr).
\]

Therefore equality holds. If the minimizer in the normal-form subcategory is unique up to isomorphism, the two compressed objects are isomorphic. \(\square\)

Thus optimal compression is formally a projection onto a class of minimal representatives.

### 4.3 Existence by choice

**Proposition 4.3.**  
Assume:

1. every feasible class

   \[
   \{T:d_{\mathcal{I}}(S,T)\le \varepsilon\}
   \]

   contains at least one finitely describable object;

2. description lengths take values in \(\mathbb{N}\).

Then, assuming global choice, there exists an \(\varepsilon\)-compression operator satisfying fidelity and optimality.

**Proof.**  
For each \(S\), consider the set of description lengths

\[
L_S=
\left\{
|\delta|:
d_{\mathcal{I}}\bigl(S,\llbracket\delta\rrbracket_{\Phi}\bigr)\le \varepsilon
\right\}.
\]

By assumption \(L_S\neq\varnothing\). Since \(L_S\subseteq\mathbb{N}\), it has a least element \(n_S\). Choose a description \(\delta_S\) of length \(n_S\) satisfying the fidelity condition, and define

\[
\mathfrak{C}(S)=\llbracket\delta_S\rrbracket_{\Phi}.
\]

Then \(\mathfrak{C}\) satisfies fidelity and optimality by construction. \(\square\)

This existence theorem is nonconstructive. In universal descriptive settings, optimal compression is generally not computable.

---

## 5. Categorical Semantics

UMCoT admits a clean categorical interpretation.

### 5.1 Essential quotient categories

Define the essential equivalence relation

\[
S\sim T
\quad\Longleftrightarrow\quad
\mathcal{I}(S)=\mathcal{I}(T)
\]

in the lossless case. Let

\[
\mathcal{S}/{\sim}
\]

be the quotient category whose objects are essential-equivalence classes.

Let

\[
\pi:\mathcal{S}\rightarrow \mathcal{S}/{\sim}
\]

be the quotient functor.

A lossless compression operator may be viewed as a section

\[
\sigma:\mathcal{S}/{\sim}\rightarrow \mathcal{S}
\]

such that

\[
\pi\circ\sigma=\operatorname{id}_{\mathcal{S}/{\sim}},
\]

and such that \(\sigma([S])\) is a minimal-complexity representative of the class \([S]\). Then

\[
\mathfrak{C}=\sigma\circ\pi.
\]

In words: compression first forgets inessential presentation detail, then selects the optimal representative of the resulting essential class.

### 5.2 Compressed normal forms as a reflective subcategory

Let \(\mathcal{N}\subseteq\mathcal{S}\) be the full subcategory of compressed normal forms. If every essential-equivalence class contains a unique normal form of minimal descriptive complexity, then the inclusion

\[
i:\mathcal{N}\hookrightarrow \mathcal{S}
\]

has a left adjoint-like compression functor

\[
\mathfrak{C}:\mathcal{S}\rightarrow \mathcal{N}
\]

satisfying

\[
\mathfrak{C}\circ i\cong \operatorname{id}_{\mathcal{N}}.
\]

This is not always an adjunction in the classical sense, because compression is often cost-driven rather than hom-driven. Nevertheless, it behaves categorically as a reflector onto a subcategory of optimal representatives.

### 5.3 Universal property of optimal compression

For each \(S\in\mathcal{S}\), define the feasible category

\[
\mathbf{Feas}_{\varepsilon}(S)
\]

whose objects are pairs \((T,\alpha)\), where

\[
T\in\mathcal{S}
\]

and \(\alpha\) is a certificate that

\[
d_{\mathcal{I}}(S,T)\le \varepsilon.
\]

Define a preorder on objects by

\[
(T,\alpha)\preceq (T',\alpha')
\quad\Longleftrightarrow\quad
\kappa_{\Phi}(T)\le \kappa_{\Phi}(T').
\]

Then \(\mathfrak{C}(S)\) is a weakly initial minimal object in \(\mathbf{Feas}_{\varepsilon}(S)\): for every feasible \(T\),

\[
\kappa_{\Phi}(\mathfrak{C}(S))
\le
\kappa_{\Phi}(T).
\]

This is the universal property of optimal compression.

---

## 6. Entropy, Counting, and Incompressibility

We now prove bounds that any admissible compressor must obey.

### 6.1 Essential entropy bound

Let \(X\) be a finite random variable taking values in \(\mathcal{S}\), with distribution \(p\). Let

\[
Z=\mathcal{I}(X)
\]

be the induced invariant random variable. Suppose the compressor is lossless with respect to \(\mathcal{I}\) and produces prefix-free descriptions of lengths

\[
L_X=\kappa_{\Phi}(\mathfrak{C}(X)).
\]

Then the expected compressed length satisfies

\[
\mathbb{E}[L_X]\ge H(Z),
\]

where

\[
H(Z)=-\sum_z q(z)\log_2 q(z)
\]

is the Shannon entropy of the invariant distribution.

**Proof.**  
Lossless reversibility requires distinct invariant classes to receive distinct decodable descriptions. Let \(q(z)\) be the probability of invariant class \(z\). Let \(L_z\) be the minimum code length assigned to any object in class \(z\). Since the code is prefix-free, the Kraft inequality gives

\[
\sum_z 2^{-L_z}\le 1.
\]

Then

\[
\mathbb{E}[L_X]
\ge
\sum_z q(z)L_z.
\]

By Gibbs’ inequality,

\[
\sum_z q(z)L_z
\ge
-\sum_z q(z)\log_2 q(z)
=
H(Z).
\]

Thus

\[
\mathbb{E}[L_X]\ge H(Z).
\]

\(\square\)

If the invariant is the full source message, \(Z=X\), and the classical source-coding bound is recovered:

\[
\mathbb{E}[L_X]\ge H(X).
\]

If the invariant forgets information, the lower bound becomes the **essential entropy** \(H(\mathcal{I}(X))\).

### 6.2 Counting bound

Let \(S_1,\dots,S_N\) have pairwise distinct invariants. Suppose a lossless compressor compresses all of them to descriptions of length at most \(m\). By Kraft’s inequality,

\[
N2^{-m}\le 1,
\]

hence

\[
m\ge \log_2 N.
\]

Therefore, among \(N\) distinct essential classes, at least one requires compressed length at least \(\lceil \log_2 N\rceil\).

More generally, at most \(2^m\) distinct invariant classes can be compressed into descriptions of length at most \(m\).

### 6.3 Compression gain and redundancy

Define the compression gain

\[
G(S)=\kappa_{\Phi}(S)-\kappa_{\Phi}(\mathfrak{C}(S)).
\]

For a distribution \(p\) on structures, the expected gain satisfies

\[
\mathbb{E}[G(S)]
\le
\mathbb{E}[\kappa_{\Phi}(S)]-H(\mathcal{I}(S)).
\]

Thus compression gain is bounded by the difference between raw descriptive complexity and essential entropy. Structures with high redundancy admit large gain; structures already close to essential entropy are nearly incompressible.

---

## 7. Noncomputability of Universal Optimal Compression

Let \(\mathcal{S}\) contain finite binary strings as structured presentations, let \(\mathcal{I}\) be the identity invariant, and let \(\Phi\) be a universal Turing-machine description scheme. Then

\[
\kappa_{\Phi}(x)
\]

coincides, up to an additive constant, with Kolmogorov complexity \(K(x)\).

**Theorem 7.1.**  
There is no total computable operator \(\mathfrak{C}\) that, for every finite binary string \(x\), outputs a description achieving

\[
\kappa_{\Phi}(\mathfrak{C}(x))=K(x)
\]

from which a shortest program for \(x\) can be effectively extracted.

**Proof sketch.**  
If such a computable compressor existed, one could compute \(K(x)\) by computing the length of the compressed optimal object. But Kolmogorov complexity is not computable. The standard diagonal argument applies: if \(K\) were computable, one could search for the first string of complexity exceeding a given bound, thereby producing a short description of that string, a contradiction. Hence universal optimal compression is not computable. \(\square\)

This theorem does not prohibit effective computable approximations. It shows only that globally optimal compression over universal description languages is intrinsically noncomputable.

---

## 8. Tensorial Compression Calculus

Many mathematical structures are composite. UMCoT treats such structures using tensorial notation.

### 8.1 Tensorization of structures

Let

\[
\mathcal{T}:\mathcal{S}\rightarrow \mathbf{Vect}^{\otimes n}
\]

be a tensorization functor assigning to a structured presentation \(S\) a tensor

\[
A(S)=A_{i_1 i_2\cdots i_n}.
\]

Examples:

- a matrix is a rank-2 tensor \(A_{ij}\);
- a graph adjacency matrix is \(A_{ij}\);
- a hypergraph incidence structure is \(A_{i_1\cdots i_n}\);
- a relational database may be represented as a boolean tensor;
- a probability distribution over variables is a tensor \(P_{i_1\cdots i_n}\);
- a proof system may be tensorized over formula and inference indices.

The invariant functor may be expressed through selected tensor contractions. For invariant tensors \(G^{(r)}\), define invariants

\[
I_r(A)=G^{(r)i_1\cdots i_n}A_{i_1\cdots i_n}.
\]

Compression must preserve these contractions up to tolerance.

### 8.2 Encoder and decoder tensors

Let

\[
A_{i_1\cdots i_n}
\]

be the tensor associated with \(S\). A tensorial compression scheme is given by an encoder tensor

\[
E^{a_1\cdots a_m}_{i_1\cdots i_n}
\]

and a decoder tensor

\[
D^{i_1\cdots i_n}_{a_1\cdots a_m}.
\]

The compressed core is

\[
B_{a_1\cdots a_m}
=
E^{i_1\cdots i_n}_{a_1\cdots a_m}
A_{i_1\cdots i_n}.
\]

The reconstruction is

\[
\widehat{A}_{i_1\cdots i_n}
=
D^{i_1\cdots i_n}_{a_1\cdots a_m}
B_{a_1\cdots a_m}.
\]

The fidelity condition is

\[
\|A-\widehat{A}\|\le \varepsilon,
\]

for a chosen norm. The compressed structure stores \(B\), and possibly \(E,D\) if they are not canonical.

The descriptive cost is therefore

\[
\ell(E)+\ell(D)+\ell(B),
\]

or, in canonical schemes, only \(\ell(B)\) plus the invariant cost of reconstructing \(E\) and \(D\).

### 8.3 Low-rank compression

A central example is CP-style low-rank approximation. For a tensor

\[
A\in V_1\otimes\cdots\otimes V_n,
\]

with \(\dim V_i=d_i\), a rank-\(R\) approximation has the form

\[
A_{i_1\cdots i_n}
\approx
\sum_{r=1}^{R}
\lambda_r
u^{(1)}_{r,i_1}
u^{(2)}_{r,i_2}
\cdots
u^{(n)}_{r,i_n}.
\]

The compressed object consists of

\[
\{\lambda_r,u^{(1)}_r,\dots,u^{(n)}_r\}_{r=1}^{R}.
\]

The parameter count is

\[
R\left(1+\sum_{i=1}^{n}d_i\right).
\]

Define the \(\varepsilon\)-compression rank by

\[
\rho_{\varepsilon}(A)
=
\min\left\{
R:
\exists \widehat{A}\text{ of rank }\le R
\text{ with }
\|A-\widehat{A}\|\le \varepsilon
\right\}.
\]

Then optimal low-rank compression seeks

\[
\rho_{\varepsilon}(A)
\]

subject to the charged-information principle.

For matrices, the Eckart–Young theorem gives the optimal rank-\(r\) approximation in Frobenius norm. If

\[
A=\sum_{k=1}^{d}\sigma_k u_k v_k^{\top}
\]

is the singular value decomposition, then the best rank-\(r\) approximation is

\[
A_r=\sum_{k=1}^{r}\sigma_k u_k v_k^{\top},
\]

and the error is

\[
\|A-A_r\|_F
=
\left(
\sum_{k=r+1}^{d}\sigma_k^2
\right)^{1/2}.
\]

Thus matrix compression has a canonical optimal solution under unitarily invariant norms. For higher-order tensors, rank minimization is generally NP-hard, but UMCoT still supplies the abstract optimality criterion.

### 8.4 Symmetry compression

Suppose a group \(G\) acts on the tensor space. Decompose the representation into irreducible components:

\[
V_1\otimes\cdots\otimes V_n
\cong
\bigoplus_{\alpha} W_{\alpha}.
\]

Let \(P_{\alpha}\) be the projector onto \(W_{\alpha}\). Then

\[
A=\sum_{\alpha}P_{\alpha}A.
\]

If the invariant functor depends only on certain irreducible components, compression may discard or coarsen the others. A symmetry-aware compressor stores:

1. the relevant irreducible labels \(\alpha\);
2. multiplicities;
3. invariant components \(P_{\alpha}A\);
4. reconstruction rules for discarded components, if lossy.

This yields compression by representation theory.

### 8.5 Correlation defect

For composite objects \(S\otimes T\), define the correlation defect

\[
\Delta(S,T)
=
\kappa_{\Phi}\bigl(\mathfrak{C}(S\otimes T)\bigr)
-
\kappa_{\Phi}\bigl(\mathfrak{C}(S)\otimes\mathfrak{C}(T)\bigr).
\]

If \(\Delta(S,T)<0\), joint compression is more efficient than separate compression. In tensor language, negative defect corresponds to exploitable multilinear correlation.

---

## 9. Canonical Compression Calculus

Although universal optimal compression is noncomputable, many practical compressors arise from a sequence of canonical structural operations.

Define the following operators:

1. **Normalization**

   \[
   \nu:\mathcal{S}\rightarrow\mathcal{S},
   \]

   removing syntactic redundancy without changing semantics.

2. **Quotienting**

   \[
   q:\mathcal{S}\rightarrow\mathcal{S},
   \]

   factoring by symmetry, congruence, bisimulation, or gauge equivalence.

3. **Decomposition**

   \[
   \delta:\mathcal{S}\rightarrow\mathcal{S}^{\otimes},
   \]

   splitting a structure into irreducible or weakly interacting components.

4. **Approximation**

   \[
   \sigma_{\varepsilon}:\mathcal{S}\rightarrow\mathcal{S},
   \]

   replacing components by simpler ones within fidelity tolerance \(\varepsilon\).

5. **Encoding**

   \[
   \eta:\mathcal{S}\rightarrow\mathcal{S},
   \]

   applying entropy coding, sparse storage, or canonical serialization.

A canonical compression pipeline has the form

\[
\mathfrak{C}
=
\eta
\circ
\sigma_{\varepsilon}
\circ
\delta
\circ
q
\circ
\nu.
\]

Each stage must satisfy a local fidelity condition:

\[
d_{\mathcal{I}}(S,\nu(S))=0,
\]

\[
d_{\mathcal{I}}(\nu(S),q(\nu(S)))=0,
\]

\[
d_{\mathcal{I}}(\delta(q\nu(S)),q\nu(S))=0,
\]

\[
d_{\mathcal{I}}(\sigma_{\varepsilon}\delta q\nu(S),\delta q\nu(S))\le \varepsilon.
\]

By the triangle inequality,

\[
d_{\mathcal{I}}(S,\mathfrak{C}(S))\le \varepsilon.
\]

Thus the pipeline is admissible. If each stage is optimal within its subproblem and cross-stage redundancies are eliminated, the pipeline is globally optimal relative to the chosen operator class.

---

## 10. Application I: Data Compression

Classical data compression is recovered as a special case of UMCoT.

Let a source emit finite strings

\[
x\in \Sigma^n.
\]

Take \(\mathcal{S}\) to be structured presentations of strings together with decoding metadata. For lossless compression, choose

\[
\mathcal{I}(S)=x,
\]

the decoded string. Then fidelity requires

\[
\mathcal{I}(\mathfrak{C}(S))=x.
\]

The essential descriptive complexity is

\[
\kappa_{\varepsilon}(x)
=
\min\{|\delta|:\operatorname{Dec}(\delta)=x\}.
\]

For a stochastic source with distribution \(p(x)\), UMCoT gives

\[
\mathbb{E}[L]\ge H(X),
\]

which is Shannon’s source-coding theorem in invariant form.

For universal compression, one minimizes

\[
\ell(M)+\ell(x\mid M),
\]

where \(M\) is a model. This is precisely a minimum-description-length instance of

\[
\kappa_{\Phi,\varepsilon}(x).
\]

### 10.1 Images and tensors

An image may be represented as a tensor

\[
A_{ijk},
\]

where \(i,j\) index spatial position and \(k\) indexes color channel. Compression may proceed by:

1. transforming to a spectral basis;
2. quantizing coefficients;
3. retaining dominant singular or wavelet components;
4. entropy coding the residual.

In UMCoT notation,

\[
\widehat{A}_{ijk}
=
D^{ijk}_{a}B_{a},
\]

where \(a\) indexes retained coefficients. The fidelity constraint may be perceptual:

\[
\|A-\widehat{A}\|_{\mathrm{perceptual}}\le \varepsilon.
\]

The invariant functor may preserve luminance moments, edges, or task-relevant features rather than raw pixel values.

---

## 11. Application II: Automated Theorem Proving

UMCoT provides a formal foundation for proof compression and theory compression.

### 11.1 Proof categories

Let \(T\) be a formal theory. Define a proof category \(\mathbf{Proof}_T\) as follows:

- objects are formulas or sequents;
- morphisms are proofs;
- composition is proof concatenation or cut.

A proof of a theorem \(\varphi\) from assumptions \(\Gamma\) is a morphism

\[
\pi:\Gamma\rightarrow \varphi.
\]

The invariant functor is

\[
\mathcal{I}(\pi)=(\Gamma,\varphi),
\]

or, semantically,

\[
\mathcal{I}(\pi)=\text{the entailment }\Gamma\models\varphi.
\]

The descriptive complexity \(\ell(\pi)\) may count symbols, inference steps, or DAG nodes.

A proof compressor is an operator

\[
\mathfrak{C}:\mathbf{Proof}_T\rightarrow \mathbf{Proof}_T
\]

such that

\[
\mathcal{I}(\mathfrak{C}(\pi))=\mathcal{I}(\pi),
\]

and

\[
\ell(\mathfrak{C}(\pi))
=
\min\{
\ell(\pi'):\mathcal{I}(\pi')=\mathcal{I}(\pi)
\}.
\]

Thus proof compression is optimal compression in the category of proofs.

### 11.2 Lemma extraction

Suppose a subproof \(P\) of size \(s\) occurs \(n\) times in a proof DAG. Introduce a named lemma \(L\) with statement cost \(h\), proof cost \(s\), and reference cost \(c\) per occurrence.

Before compression, the total contribution is

\[
ns.
\]

After compression, it is

\[
s+h+nc.
\]

The gain is therefore

\[
G=(n-1)s-h-nc.
\]

Lemma extraction is beneficial precisely when

\[
(n-1)s>h+nc.
\]

This inequality is a special case of UMCoT optimality: the lemma is introduced only if it reduces the total descriptive complexity of the proof while preserving the proved sequent.

### 11.3 Theory compression

Let \(T\) be an axiomatic theory with theorem set

\[
\operatorname{Th}(T).
\]

Define

\[
\mathcal{I}(T)=\operatorname{Th}(T).
\]

A theory compressor seeks a theory \(T'\) such that

\[
\operatorname{Th}(T')=\operatorname{Th}(T),
\]

while minimizing axiom length or symbol count:

\[
\ell(T')=
\min\{
\ell(T''):\operatorname{Th}(T'')=\operatorname{Th}(T)
\}.
\]

This formalizes axiom minimization, redundancy elimination, and definition extension as compression.

---

## 12. Application III: Knowledge Representation

Knowledge bases, ontologies, and relational databases are natural objects in \(\mathcal{S}\).

### 12.1 Query-preserving compression

Let \(O\) be an ontology or database instance. Let \(\mathcal{Q}\) be a query language. Define the invariant

\[
\mathcal{I}_{\mathcal{Q}}(O)
=
\{
(q,\operatorname{Ans}(q,O)):q\in\mathcal{Q}
\}.
\]

A query-preserving compressor satisfies

\[
\mathcal{I}_{\mathcal{Q}}(\mathfrak{C}(O))
=
\mathcal{I}_{\mathcal{Q}}(O).
\]

The optimal compressed knowledge base is a minimal representative of the query-equivalence class of \(O\).

### 12.2 Cores and conjunctive queries

For finite relational structures and Boolean conjunctive queries, query equivalence is closely related to homomorphic equivalence. A **core** of a finite structure \(A\) is a minimal substructure \(C(A)\) such that

\[
C(A)\rightarrow A
\]

and

\[
A\rightarrow C(A),
\]

where arrows denote homomorphisms.

Cores are unique up to isomorphism and are minimal query-preserving compressions for conjunctive query semantics. Thus, in UMCoT terms,

\[
\mathfrak{C}(A)=C(A)
\]

is the lossless optimal compressor relative to conjunctive-query invariants.

### 12.3 Bisimulation quotienting

For modal logics, the appropriate invariant is bisimulation equivalence. If \(M\) is a transition system or Kripke structure, its bisimulation quotient

\[
M/{\sim}
\]

preserves all modal formulas and is often the minimal such presentation. Hence

\[
\mathfrak{C}(M)=M/{\sim}
\]

is a canonical UMCoT compression.

### 12.4 Tensorial knowledge compression

A relational knowledge base may be represented as a ternary tensor

\[
R_{ijk},
\]

where \(i\) and \(j\) index entities and \(k\) indexes relations. Low-rank compression takes the form

\[
R_{ijk}
\approx
\sum_{r=1}^{R}
\lambda_r
u_{r,i}
v_{r,j}
w_{r,k}.
\]

The invariant functor may preserve selected query answers, relation frequencies, or embedding-level predictions. UMCoT then supplies the fidelity and optimality criteria for such compressed representations.

---

## 13. Application IV: Computational Complexity

UMCoT interacts with computational complexity in several ways.

### 13.1 Structural Kolmogorov complexity

For a structured presentation \(S\), define its structural Kolmogorov complexity by

\[
K_{\Phi}(S)=\kappa_{\Phi}(S).
\]

The essential complexity is

\[
K_{\Phi}^{\varepsilon}(S)=\kappa_{\Phi,\varepsilon}(S).
\]

The compression deficit

\[
\Delta K(S)=K_{\Phi}(S)-K_{\Phi}^{\varepsilon}(S)
\]

measures how much presentation-level redundancy can be removed without altering essential invariants.

### 13.2 Complexity of optimal compression

Although universal optimal compression is noncomputable, restricted finite versions are often NP-hard.

Consider a macro-compression problem. A structured presentation \(S\) contains a set of repeated substructures. A macro may replace a set of occurrences, but each macro incurs a definition cost. The compression gain is

\[
G=
\text{saved occurrence cost}
-
\text{macro definition cost}
-
\text{reference costs}.
\]

Choosing macros to maximize gain generalizes weighted set cover. Therefore:

**Proposition 13.1.**  
Deciding whether a finite presentation admits a macro-compression of gain at least \(K\) is NP-hard in general.

**Proof sketch.**  
Reduce weighted set cover to macro selection. Let universe elements correspond to repeated substructures, and let macros correspond to sets. Assign savings and costs so that a macro collection achieves target gain exactly when the corresponding sets cover the universe within the allowed cost. Since set cover is NP-hard, the compression decision problem is NP-hard. \(\square\)

Thus, even when optimal compression is well-defined, computing it may be intractable.

### 13.3 Witness compression

Let \(R\subseteq\{0,1\}^{n}\times\{0,1\}^{m}\) be a polynomially balanced relation. A witness \(y\) for \(x\) may be compressed to a structured object \(c\) such that a polynomial-time decompressor recovers a valid witness \(y'\) with

\[
R(x,y').
\]

The invariant is the existence of a valid witness, or the witness itself if lossless witness recovery is required. UMCoT provides a framework for studying minimal witness descriptions, succinct certificates, and proof-carrying compression.

### 13.4 Compression and lower bounds

If a class of structures has essential entropy \(H\), then any lossless representation must use at least \(H\) bits on average. Therefore, incompressibility relative to an invariant functor can be used to prove representation lower bounds.

For example, if a family of graphs has \(N\) distinct invariant classes, then some member requires at least

\[
\log_2 N
\]

bits to describe losslessly. This recovers elementary counting lower bounds in a universal form.

---

## 14. Examples

### 14.1 Finite group compression

Let \(G\) be a finite group given by its multiplication table. The raw presentation has size

\[
\ell(G)=|G|^2.
\]

A compressed presentation may be a group presentation

\[
\langle g_1,\dots,g_k\mid r_1,\dots,r_m\rangle.
\]

The invariant functor is the isomorphism class of the group:

\[
\mathcal{I}(G)=[G].
\]

The compressed complexity is the length of the presentation plus the cost of verifying or reconstructing the group. Optimal compression seeks the shortest presentation of \(G\) among all presentations of the same group.

This problem is highly nontrivial and generally not computably decidable in full generality, but it fits exactly into UMCoT.

### 14.2 Graph quotient compression

Let \(G=(V,E)\) be a graph with adjacency tensor

\[
A_{ij}.
\]

Suppose an equitable partition of \(V\) into blocks \(B_1,\dots,B_k\) is found. The quotient graph \(Q\) has vertices \(1,\dots,k\), with edge densities

\[
p_{ab}
=
\frac{|E(B_a,B_b)|}{|B_a||B_b|}.
\]

The compressed structure is

\[
\mathfrak{C}(G)=(Q,\{|B_a|\}).
\]

If the original graph can be reconstructed exactly from the quotient plus internal descriptions, the compression is lossless. Otherwise it is lossy, with fidelity measured by agreement of graph invariants such as cut norms, spectra, or subgraph densities.

### 14.3 Tensor compression

Let

\[
A\in\mathbb{R}^{d_1}\otimes\cdots\otimes\mathbb{R}^{d_n}.
\]

A rank-\(R\) UMCoT compressor stores

\[
\{\lambda_r,u^{(1)}_r,\dots,u^{(n)}_r\}_{r=1}^{R}.
\]

The reconstruction is

\[
\widehat{A}_{i_1\cdots i_n}
=
\sum_{r=1}^{R}
\lambda_r
u^{(1)}_{r,i_1}
\cdots
u^{(n)}_{r,i_n}.
\]

The optimality criterion is

\[
R=\rho_{\varepsilon}(A),
\]

subject to the chosen norm and invariant constraints.

### 14.4 Proof compression by cut elimination and lemma sharing

A proof may contain redundant detours. Cut elimination can reduce certain forms of redundancy but may increase proof length. UMCoT treats cut elimination as one possible transformation in the feasible class, not as automatically optimal. The optimal compressed proof minimizes total descriptive complexity after considering:

- cut elimination;
- lemma extraction;
- proof DAG sharing;
- definitional abbreviation;
- normalization of inference sequences.

Thus UMCoT reconciles normalization and compression: normal forms are useful only insofar as they reduce descriptive complexity relative to the invariant theorem.

---

## 15. Limitations and Impossibility Phenomena

UMCoT clarifies why compression cannot be absolute.

### 15.1 Invariant dependence

Compression is always relative to an invariant functor. If the invariant functor is too weak, compression may destroy important information. If it is too strong, little compression is possible.

There is no canonical invariant functor for all mathematics. The choice of \(\mathcal{I}\) encodes the semantics of the application.

### 15.2 No universal computable optimum

When \(\Phi\) is universal and \(\mathcal{I}\) is identity, optimal compression computes Kolmogorov complexity. Hence no universal computable optimum exists.

### 15.3 Entropy barriers

Lossless compression cannot beat essential entropy. Structures whose invariant distribution is already uniform over many classes are incompressible on average.

### 15.4 Tensor hardness

For higher-order tensors, optimal rank compression is computationally hard. Thus even well-posed finite compression problems may be intractable.

### 15.5 Reversibility tradeoffs

Strong reversibility limits compression. If every presentation detail must be recovered, many semantic redundancies cannot be removed. Essential reversibility permits greater compression but accepts that only invariant content is recovered.

---

## 16. Synthesis

UMCoT can be summarized by the following diagram:

\[
S
\longrightarrow
\mathcal{I}(S)
\longrightarrow
\text{essential equivalence class}
\longrightarrow
\mathfrak{C}(S).
\]

The first arrow extracts essential invariants. The second arrow passes to the class of structures preserving those invariants. The third arrow selects a minimally describable representative.

Equivalently,

\[
\boxed{
\text{Compression}
=
\text{invariant preservation}
+
\text{quotienting by redundancy}
+
\text{optimal representative selection}.
}
\]

In tensorial form,

\[
\boxed{
A_{i_1\cdots i_n}
\mapsto
B_{a_1\cdots a_m}
\mapsto
\widehat{A}_{i_1\cdots i_n},
\qquad
\|A-\widehat{A}\|\le\varepsilon,
\qquad
\ell(B)\text{ minimal}.
}
\]

In proof-theoretic form,

\[
\boxed{
\pi:\Gamma\to\varphi
\quad\mapsto\quad
\mathfrak{C}(\pi):\Gamma\to\varphi,
\qquad
\ell(\mathfrak{C}(\pi))\text{ minimal}.
}
\]

In knowledge-representation form,

\[
\boxed{
O
\quad\mapsto\quad
\mathfrak{C}(O),
\qquad
\operatorname{Ans}(q,\mathfrak{C}(O))
=
\operatorname{Ans}(q,O),
\qquad
\ell(\mathfrak{C}(O))\text{ minimal}.
}
\]

These are not analogies. They are instances of the same axiomatic scheme.

---

## 17. Conclusion

Universal Mathematical Compression Theory proposes that compression is not a technique restricted to files or messages, but a fundamental structural operation in mathematics. Given a class of structured presentations, a choice of essential invariants, and a descriptive complexity measure, compression becomes the selection of optimal representatives in invariant-preserving equivalence classes.

The axioms of fidelity, reversibility, and optimality provide a minimal yet powerful foundation. The categorical formulation reveals compression as a section of an essential quotient, selecting normal forms of least descriptive cost. The tensorial calculus extends the theory to composite, multilinear, and symmetry-rich structures. The applications show that data compression, proof compression, theory minimization, ontology compression, and structural complexity are unified under a single formal framework.

The theory also exposes inherent limits: optimal universal compression is noncomputable, entropy bounds constrain average gain, and finite compression problems are frequently NP-hard. These limitations are not defects; they delineate the exact mathematical territory in which compression is possible.

UMCoT therefore provides both a foundation and a research program: to identify the right invariants, the right descriptive costs, and the right normal forms for each mathematical domain, and to construct compressors that are provably optimal relative to those choices.

---

## References

1. C. E. Shannon, *A Mathematical Theory of Communication*, Bell System Technical Journal, 1948.  
2. A. N. Kolmogorov, *Three Approaches to the Quantitative Definition of Information*, 1965.  
3. G. J. Chaitin, *On the Length of Programs for Computing Finite Binary Sequences*, Journal of the ACM, 1966.  
4. J. Rissanen, *Modeling by Shortest Data Description*, Automatica, 1978.  
5. S. Mac Lane, *Categories for the Working Mathematician*, Springer.  
6. T. G. Kolda and B. W. Bader, *Tensor Decompositions and Applications*, SIAM Review, 2009.  
7. L. Libkin, *Elements of Finite Model Theory*, Springer.  
8. M. Huth and M. Ryan, *Logic in Computer Science*, Cambridge University Press.  
9. A. S. Tropp, *An Introduction to Matrix Concentration Inequalities*, Foundations and Trends in Machine Learning, 2015.  
10. D. Knuth, *The Art of Computer Programming*, Addison-Wesley.
