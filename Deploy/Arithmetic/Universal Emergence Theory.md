# Universal Emergence Theory  
## Emergence Operators, Stability Classes, Novelty Invariants, and Hierarchical Organization

**Preprint**

---

## Abstract

We develop **Universal Emergence Theory (UET)**, a formal mathematical framework in which emergence is not treated as a descriptive label attached to complex systems, but as a primitive mathematical operation. The central object is an **emergence operator**
\[
\mathcal E:\mathcal P\longrightarrow \mathcal S,
\]
mapping collections or configurations of primitive entities \(\mathcal P\) to emergent structures \(\mathcal S\). We axiomatize this operation through a categorical and geometric theory built from five fundamental objects: emergence operators, hierarchical levels, stability classes, novelty invariants, and emergence morphisms.

The core thesis of UET is that emergence is mathematically characterized by the failure of a system’s global structure to be equivalent to the independent composition of its parts. In categorical language, emergence is encoded by a **lax monoidal functor** whose structure maps are not isomorphisms. In differential or tensorial realizations, emergence is represented by irreducible higher-order emergence tensors whose components cannot be reduced to lower-order compositions. Stable emergent structures are classified by **stability classes**, while irreducible structural innovation is measured by **novelty invariants** taking values in cokernels, Grothendieck groups, cohomology rings, or characteristic classes.

The resulting framework applies uniformly to complex systems, biological organization, artificial intelligence, network science, statistical mechanics, and theoretical physics. UET does not merely describe emergence; it supplies a formal calculus for computing, comparing, stabilizing, and classifying emergent phenomena.

**Keywords:** emergence, category theory, monoidal functors, stability, novelty, hierarchy, complex systems, tensor calculus, renormalization, geometric structures.

---

## 1. Introduction

Emergence is usually described informally: a whole is said to possess properties that are not present in, or not predictable from, its parts. This language is useful but mathematically imprecise. It conflates epistemic limitation with structural irreducibility, and it rarely supplies invariant criteria for deciding when emergence has occurred, how stable it is, or how it composes across scales.

**Universal Emergence Theory (UET)** proposes a different starting point.

We treat emergence as a **fundamental operation**:
\[
\mathcal E:\mathcal P\longrightarrow \mathcal S,
\]
where \(\mathcal P\) denotes a domain of primitive entities or configurations, and \(\mathcal S\) denotes a domain of structured wholes. The central problem is not whether emergence “exists,” but how the map \(\mathcal E\) behaves under composition, perturbation, coarse-graining, and iteration.

The guiding principle of UET is:

> **Emergence is the nontrivial failure of a whole to decompose into the independent assembly of its parts.**

This failure is not a defect. It is the mathematical signature of new structure.

In this paper we construct UET as a formal preprint-level theory. The framework is intentionally general: \(\mathcal P\) and \(\mathcal S\) may be sets, manifolds, vector spaces, categories, sheaves, or higher categorical structures. The essential content lies in the axioms governing the emergence operator.

The primitive objects of UET are:

1. **Emergence operators**  
   Maps or functors \(\mathcal E\) producing emergent structures from primitive configurations.

2. **Hierarchical levels**  
   Iterated domains \(\mathcal P_0,\mathcal P_1,\mathcal P_2,\dots\) in which emergent structures at one level become primitive entities at the next.

3. **Stability classes**  
   Equivalence classes of emergent structures under admissible perturbations.

4. **Novelty invariants**  
   Algebraic, geometric, or cohomological quantities measuring irreducible structural innovation.

5. **Emergence morphisms**  
   Structure-preserving maps between emergent systems.

The central contributions of this paper are as follows.

1. We formulate emergence as a **lax monoidal functor**, making precise the idea that the emergent whole is not equivalent to the composition of emergent parts.

2. We define **novelty objects** as kernels and cokernels of assembly maps, and we introduce scalar and categorical **novelty invariants**.

3. We develop a **tensorial calculus of emergence**, in which irreducible emergence is represented by higher-order tensors modulo reducible subspaces.

4. We define **stability classes** through deformation equivalence and, in smooth settings, through Morse-theoretic criteria.

5. We formalize **hierarchical organization** as an iterated tower of emergence operators and, under natural coherence conditions, as a monadic structure.

6. We indicate applications to statistical mechanics, biological organization, artificial intelligence, network science, and theoretical physics.

The present paper is foundational. It establishes the formal skeleton of UET. Subsequent work may develop model-specific realizations, computational algorithms for novelty estimation, and empirical criteria for stability classification.

---

## 2. Primitive Entities and Primitive Categories

### 2.1 Primitive domains

Let \(\mathcal P\) denote a collection of **primitive entities**. In the most general formulation, \(\mathcal P\) is not merely a set but a category.

\[
\mathsf{Prim}
\]

Objects of \(\mathsf{Prim}\) are primitive entities or primitive configurations. Morphisms are admissible primitive transformations.

Examples include:

- finite sets of particles,
- graphs,
- local degrees of freedom,
- symbolic alphabets,
- molecular components,
- neural units,
- fields on a lattice,
- elementary events in a causal set.

To compose primitive entities, we equip \(\mathsf{Prim}\) with a symmetric monoidal structure:
\[
(\mathsf{Prim},\otimes,I),
\]
where \(\otimes\) denotes primitive assembly and \(I\) denotes the empty or trivial primitive configuration.

Thus if \(P,Q\in \mathsf{Prim}\), then
\[
P\otimes Q
\]
is the primitive configuration obtained by placing \(P\) and \(Q\) together.

The monoidal product need not be Cartesian. It may encode disjoint union, tensor product, concatenation, graph join, spatial composition, or any operation appropriate to the domain.

### 2.2 Primitive state spaces

In many applications, \(\mathcal P\) is a state space rather than a category. For example,
\[
\mathcal P = \mathbb R^n,
\]
with coordinates
\[
p^i,\qquad i=1,\dots,n.
\]
Here a primitive configuration is a point
\[
p=(p^1,\dots,p^n)\in \mathcal P.
\]
The categorical and state-space formulations are compatible: a state space may be viewed as a category whose objects are points and whose morphisms are admissible paths or transformations.

### 2.3 Observables

Let
\[
\mathsf{Obs}:\mathsf{Prim}\longrightarrow \mathsf{Set}
\]
or
\[
\mathsf{Obs}:\mathsf{Prim}\longrightarrow \mathsf{Vect}
\]
be an observable functor. For each primitive configuration \(P\), \(\mathsf{Obs}(P)\) is the set or vector space of measurable primitive properties.

Observables will be used to define stability: an emergent structure is stable if its relevant observable content persists under perturbations of the primitive substrate.

---

## 3. Emergence Operators

### 3.1 Basic definition

At the level of object classes, an **emergence operator** is a map
\[
\mathcal E:\operatorname{Obj}(\mathsf{Prim})\longrightarrow \operatorname{Obj}(\mathsf{Struct}),
\]
where \(\mathsf{Struct}\) is a category of structured systems.

More fully, an emergence operator is a functor
\[
\mathcal E:\mathsf{Prim}\longrightarrow \mathsf{Struct}.
\]

For each primitive configuration \(P\), the object
\[
\mathcal E(P)
\]
is the emergent structure generated by \(P\).

For each primitive morphism
\[
f:P\longrightarrow Q,
\]
there is an induced emergent morphism
\[
\mathcal E(f):\mathcal E(P)\longrightarrow \mathcal E(Q).
\]

This ensures that transformations of primitive configurations induce transformations of emergent structures.

### 3.2 Lax monoidal structure

Let \(\mathsf{Struct}\) also be symmetric monoidal:
\[
(\mathsf{Struct},\boxtimes,J).
\]

A mere functor \(\mathcal E\) is not enough to encode emergence. We must specify how the emergent structure of a composite system relates to the composite of the emergent structures of its parts.

Thus we equip \(\mathcal E\) with a **lax monoidal structure**:
\[
m_{P,Q}:\mathcal E(P)\boxtimes \mathcal E(Q)
\longrightarrow
\mathcal E(P\otimes Q),
\]
together with a unit map
\[
u:J\longrightarrow \mathcal E(I).
\]

The map \(m_{P,Q}\) is called the **assembly map**.

It expresses the attempt to build the emergent whole \(\mathcal E(P\otimes Q)\) from the independent emergent structures \(\mathcal E(P)\) and \(\mathcal E(Q)\).

If \(m_{P,Q}\) is an isomorphism for all \(P,Q\), then the emergence operator is **additive** or **reducible**. In that case, the whole carries no irreducible novelty beyond the parts.

If \(m_{P,Q}\) fails to be an isomorphism, emergence is present.

This is the first central principle of UET:

> **Emergence is measured by the failure of the assembly map to be an isomorphism.**

### 3.3 Reducible and emergent operators

Let \(\mathcal E:\mathsf{Prim}\to \mathsf{Struct}\) be lax monoidal.

We say that \(\mathcal E\) is **reducible** if for all \(P,Q\), the assembly map
\[
m_{P,Q}:\mathcal E(P)\boxtimes \mathcal E(Q)\to \mathcal E(P\otimes Q)
\]
is an isomorphism.

We say that \(\mathcal E\) is **emergent** if there exist \(P,Q\) for which \(m_{P,Q}\) is not an isomorphism.

This definition is structural rather than epistemic. Emergence is not a statement about what an observer can predict. It is a statement about the non-equivalence of two mathematical compositions.

### 3.4 Emergence as a section

In geometric settings, one may regard \(\mathcal E\) as a section of a bundle.

Let
\[
\pi:\mathsf{Tot}\longrightarrow \mathcal P
\]
be a bundle over the primitive configuration space. The fiber over \(p\in \mathcal P\) is the space of possible emergent structures generated by \(p\).

An emergence operator is then a section
\[
\sigma:\mathcal P\longrightarrow \mathsf{Tot}
\]
such that
\[
\pi\circ \sigma=\operatorname{id}_{\mathcal P}.
\]

In this picture, emergence assigns to each primitive configuration a distinguished emergent realization.

---

## 4. Axioms of Universal Emergence Theory

We now state the axioms that define a UET structure.

Let
\[
\mathsf{Prim}=(\mathcal P,\otimes,I)
\]
and
\[
\mathsf{Struct}=(\mathcal S,\boxtimes,J)
\]
be symmetric monoidal categories.

A **Universal Emergence Structure** is a tuple
\[
\mathfrak U=
(\mathcal E,m,u,\Sigma,\nu,\mathcal H)
\]
where:

- \(\mathcal E:\mathsf{Prim}\to \mathsf{Struct}\) is a functor,
- \((m,u)\) is a lax monoidal structure,
- \(\Sigma\) is a stability functor,
- \(\nu\) is a novelty invariant,
- \(\mathcal H\) is a hierarchical organization.

The axioms are as follows.

---

### Axiom UET-1: Functoriality

For every primitive morphism
\[
f:P\to Q,
\]
the emergence operator assigns a morphism
\[
\mathcal E(f):\mathcal E(P)\to \mathcal E(Q)
\]
such that
\[
\mathcal E(\operatorname{id}_P)=\operatorname{id}_{\mathcal E(P)}
\]
and
\[
\mathcal E(g\circ f)=\mathcal E(g)\circ \mathcal E(f).
\]

This ensures that emergence respects primitive transformations.

---

### Axiom UET-2: Lax compositionality

For all primitive objects \(P,Q,R\), the assembly maps
\[
m_{P,Q}:\mathcal E(P)\boxtimes \mathcal E(Q)\to \mathcal E(P\otimes Q)
\]
satisfy associativity coherence:
\[
m_{P\otimes Q,R}\circ (m_{P,Q}\boxtimes \operatorname{id})
=
m_{P,Q\otimes R}\circ (\operatorname{id}\boxtimes m_{Q,R}).
\]

The unit coherence is similarly required:
\[
m_{I,P}\circ (u\boxtimes \operatorname{id})
=
\lambda_{\mathcal E(P)},
\]
\[
m_{P,I}\circ (\operatorname{id}\boxtimes u)
=
\rho_{\mathcal E(P)},
\]
where \(\lambda,\rho\) are the left and right unitors in \(\mathsf{Struct}\).

---

### Axiom UET-3: Nontriviality

There exist primitive objects \(P,Q\) such that
\[
m_{P,Q}
\]
is not an isomorphism.

Equivalently, the emergence operator is not merely a strong monoidal functor.

This axiom excludes purely additive theories in which the whole is always equivalent to the sum of the parts.

---

### Axiom UET-4: Stability

There exists a stability functor
\[
\Sigma:\mathsf{Struct}\longrightarrow \mathsf{Poset}
\]
assigning to each emergent structure \(S\) a stability class
\[
\Sigma(S).
\]

For every emergent structure \(\mathcal E(P)\), there exists an admissible neighborhood \(U_P\subseteq \mathsf{Prim}\) such that for all \(P'\in U_P\),
\[
\Sigma(\mathcal E(P'))=\Sigma(\mathcal E(P)).
\]

This axiom asserts local structural robustness of emergent organization.

---

### Axiom UET-5: Novelty invariance

There exists an invariant
\[
\nu:\mathsf{Struct}\longrightarrow \mathcal N
\]
where \(\mathcal N\) is an algebraic target such as a Grothendieck group, cohomology ring, or ordered monoid.

The invariant must satisfy:

1. **Isomorphism invariance**  
   If \(S\cong T\), then
   \[
   \nu(S)=\nu(T).
   \]

2. **Nontriviality detection**  
   If \(m_{P,Q}\) fails to be an isomorphism in an appropriate sense, then
   \[
   \nu(\mathcal E(P\otimes Q))
   \neq
   \nu(\mathcal E(P)\boxtimes \mathcal E(Q)).
   \]

3. **Stability compatibility**  
   If \(S\) and \(T\) lie in the same stability class, then
   \[
   \nu(S)=\nu(T)
   \]
   for all stability-sensitive novelty invariants.

---

### Axiom UET-6: Hierarchical closure

For each level \(n\geq 0\), there exists a primitive category
\[
\mathsf{Prim}_n
\]
and an emergence operator
\[
\mathcal E_n:\mathsf{Prim}_n\to \mathsf{Prim}_{n+1}.
\]

Thus the emergent structures at level \(n\) become primitive entities at level \(n+1\).

The hierarchy is coherent if there exist realization functors
\[
\pi_n:\mathsf{Prim}_{n+1}\to \mathsf{Prim}_n
\]
such that, for suitable objects,
\[
\pi_n(\mathcal E_n(P))\cong P.
\]

This expresses the fact that higher-level emergent structures are realized by, but not reducible to, lower-level configurations.

---

### Axiom UET-7: Emergence morphisms

There exists a category \(\mathsf{Em}\) whose objects are emergent structures
\[
(P,\mathcal E(P))
\]
and whose morphisms preserve the emergence relation, stability classes, and novelty invariants.

This category provides the natural notion of equivalence and comparison between emergent systems.

---

## 5. Stability Classes

Stability is essential because not every structural novelty qualifies as a robust emergent phenomenon. UET therefore distinguishes transient irregularities from stable emergent organizations.

### 5.1 Deformation equivalence

Assume \(\mathsf{Struct}\) is enriched over topological spaces. Let
\[
d_{\mathsf{Struct}}
\]
be an admissible metric or pseudometric on emergent structures.

Let
\[
\mathsf{Obs}:\mathsf{Struct}\to \mathsf{ObsCat}
\]
be an observable functor.

Two emergent structures \(S,T\in \mathsf{Struct}\) are **stably equivalent**, written
\[
S\sim_\sigma T,
\]
if there exists a continuous path
\[
\gamma:[0,1]\to \mathsf{Struct}
\]
such that
\[
\gamma(0)=S,\qquad \gamma(1)=T,
\]
and the relevant observable content remains invariant along the path:
\[
\mathsf{Obs}(\gamma(t))\cong \mathsf{Obs}(S)
\]
for all \(t\in[0,1]\), up to admissible equivalence.

The **stability class** of \(S\) is the equivalence class
\[
[S]_\sigma.
\]

The stability functor
\[
\Sigma:\mathsf{Struct}\to \mathsf{Poset}
\]
assigns
\[
\Sigma(S)=[S]_\sigma.
\]

The partial order may encode relative robustness:
\[
[S]_\sigma \leq [T]_\sigma
\]
means that the stability basin of \(T\) contains or dominates that of \(S\).

### 5.2 Structural stability of emergence

An emergence operator \(\mathcal E\) is **structurally stable at \(P\)** if there exists an admissible neighborhood \(U_P\) such that for all \(P'\in U_P\),
\[
[\mathcal E(P')]_\sigma=[\mathcal E(P)]_\sigma.
\]

Equivalently, small changes in the primitive configuration do not change the stability class of the emergent structure.

This is the categorical analogue of structural stability in dynamical systems.

### 5.3 Smooth stability criterion

Suppose \(\mathcal P\) and \(\mathcal S\) are smooth manifolds and
\[
\mathcal E:\mathcal P\to \mathcal S
\]
is smooth.

Let
\[
V:\mathcal S\to \mathbb R
\]
be a stability potential. An emergent state
\[
s=\mathcal E(p)
\]
is stable if it is a local minimum of \(V\) restricted to the relevant constraint manifold.

The Hessian is
\[
H_{AB}(s)=\frac{\partial^2 V}{\partial s^A\partial s^B}(s).
\]

If \(H_{AB}\) is positive definite on the tangent space of the constraint manifold, then \(s\) is locally stable.

The **Morse index**
\[
\mu(s)=\#\{\text{negative eigenvalues of }H(s)\}
\]
classifies the type of instability.

Thus a refined stability class may be written as
\[
\Sigma(s)=\bigl(\mu(s),\ker H(s),\text{basin type}\bigr).
\]

### 5.4 Stability theorem

**Theorem 5.1 (Local stability of smooth emergence).**  
Let \(\mathcal E:\mathcal P\to \mathcal S\) be smooth. Let \(p_0\in \mathcal P\) and \(s_0=\mathcal E(p_0)\). Suppose:

1. The Jacobian
   \[
   D\mathcal E|_{p_0}
   \]
   has constant rank in a neighborhood of \(p_0\).

2. The stability potential \(V\) has a nondegenerate Hessian at \(s_0\) when restricted to the image of \(D\mathcal E\).

Then there exists a neighborhood \(U\) of \(p_0\) such that for all \(p\in U\), the emergent state \(\mathcal E(p)\) lies in the same stability class as \(\mathcal E(p_0)\).

**Proof sketch.**  
Constant rank implies that locally \(\mathcal E(\mathcal P)\) is a smooth submanifold of \(\mathcal S\). Nondegeneracy of the restricted Hessian implies, by the Morse lemma, that the local qualitative form of \(V\) is unchanged under small perturbations. Hence the basin type and Morse index remain constant, which yields stability-class equivalence. \(\square\)

---

## 6. Novelty Invariants

Novelty invariants quantify the irreducible content of an emergent structure.

There are several equivalent formulations depending on the ambient mathematical structure.

---

## 6.1 Novelty objects in additive categories

Assume \(\mathsf{Struct}\) is additive or abelian, and that \(\boxtimes\) is compatible with biproducts.

For primitive objects \(P,Q\), there is a canonical assembly map
\[
\alpha_{P,Q}:
\mathcal E(P)\oplus \mathcal E(Q)
\longrightarrow
\mathcal E(P\otimes Q).
\]

This map is obtained by combining the inclusions of the parts into the whole with the lax monoidal structure.

Define the **redundancy object**
\[
\operatorname{Red}(P,Q)=\ker(\alpha_{P,Q})
\]
and the **novelty object**
\[
\operatorname{Nov}(P,Q)=\operatorname{coker}(\alpha_{P,Q}).
\]

Thus there is an exact sequence
\[
0
\longrightarrow
\operatorname{Red}(P,Q)
\longrightarrow
\mathcal E(P)\oplus \mathcal E(Q)
\overset{\alpha_{P,Q}}{\longrightarrow}
\mathcal E(P\otimes Q)
\longrightarrow
\operatorname{Nov}(P,Q)
\longrightarrow
0.
\]

Interpretation:

- \(\operatorname{Red}(P,Q)\) measures overdetermination or constraint among parts.
- \(\operatorname{Nov}(P,Q)\) measures features of the whole not captured by the separate parts.

If
\[
\operatorname{Nov}(P,Q)\neq 0,
\]
then the composite system possesses irreducible novelty.

If
\[
\operatorname{Red}(P,Q)\neq 0,
\]
then the parts are not independent in their contribution to the whole.

A system is **strongly emergent** when both novelty and stability are nontrivial:
\[
\operatorname{Nov}(P,Q)\neq 0
\]
and
\[
[\mathcal E(P\otimes Q)]_\sigma
\]
is stable under perturbations.

---

## 6.2 Grothendieck novelty invariant

Let \(K_0(\mathsf{Struct})\) be the Grothendieck group of the category of emergent structures.

Define the **Grothendieck novelty invariant**
\[
\nu_K(P,Q)
=
[\mathcal E(P\otimes Q)]
-
[\mathcal E(P)]
-
[\mathcal E(Q)]
\in K_0(\mathsf{Struct}).
\]

If \(\mathcal E(I)\) is nontrivial, one may include the empty contribution:
\[
\nu_K(P,Q)
=
[\mathcal E(P\otimes Q)]
-
[\mathcal E(P)]
-
[\mathcal E(Q)]
+
[\mathcal E(I)].
\]

From the exact sequence above,
\[
\nu_K(P,Q)
=
[\operatorname{Nov}(P,Q)]
-
[\operatorname{Red}(P,Q)].
\]

Thus the Grothendieck novelty invariant separates genuinely new structure from redundancy.

---

## 6.3 Möbius novelty for many parts

Let \(A=\{1,\dots,n\}\) be a finite set of primitive components
\[
P_i,\qquad i\in A.
\]

For each subset \(B\subseteq A\), define
\[
P_B=\bigotimes_{i\in B} P_i.
\]

The irreducible \(A\)-fold novelty is defined by Möbius inversion:
\[
\Delta_A(\mathcal E)
=
\sum_{B\subseteq A}
(-1)^{|A|-|B|}
[\mathcal E(P_B)]
\in K_0(\mathsf{Struct}).
\]

For \(n=2\),
\[
\Delta_{\{1,2\}}(\mathcal E)
=
[\mathcal E(P_1\otimes P_2)]
-
[\mathcal E(P_1)]
-
[\mathcal E(P_2)]
+
[\mathcal E(I)].
\]

For \(n=3\),
\[
\begin{aligned}
\Delta_{\{1,2,3\}}(\mathcal E)
&=
[\mathcal E(P_1\otimes P_2\otimes P_3)]
-
[\mathcal E(P_1\otimes P_2)]
-
[\mathcal E(P_1\otimes P_3)]
-
[\mathcal E(P_2\otimes P_3)]
\\
&\quad
+
[\mathcal E(P_1)]
+
[\mathcal E(P_2)]
+
[\mathcal E(P_3)]
-
[\mathcal E(I)].
\end{aligned}
\]

If
\[
\Delta_A(\mathcal E)\neq 0,
\]
then the system exhibits irreducible \(A\)-wise emergence.

This is the categorical analogue of higher-order interaction information.

---

## 6.4 Cohomological novelty

In geometric settings, novelty may be topological.

Let
\[
\pi:\mathcal E\longrightarrow \mathcal P
\]
be an emergence bundle. Suppose \(\mathcal E\) carries a connection
\[
\nabla=d+A,
\]
with local connection one-form
\[
A^A{}_{B}=A^A{}_{B i}\,dp^i.
\]

The curvature is
\[
F^\nabla=dA+A\wedge A,
\]
with components
\[
F^A{}_{Bij}
=
\partial_i A^A{}_{B j}
-
\partial_j A^A{}_{B i}
+
A^A{}_{C i}A^C{}_{B j}
-
A^A{}_{C j}A^C{}_{B i}.
\]

If the curvature is nonzero, the emergent structure depends on the path taken through primitive configuration space. This path dependence is a geometric form of emergence.

The characteristic classes
\[
c_k(\mathcal E)
=
\left[\operatorname{Tr}\left((F^\nabla)^k\right)\right]
\in H^{2k}(\mathcal P)
\]
are topological novelty invariants.

If
\[
c_k(\mathcal E)\neq 0
\]
for some \(k\), the emergence bundle is topologically nontrivial.

Thus emergence may be obstructed from global trivialization.

---

## 7. Emergence Tensors

When \(\mathcal P\) and \(\mathcal S\) are vector spaces or manifolds with local coordinates, emergence can be expressed tensorially.

Let
\[
p^i,\qquad i=1,\dots,n
\]
be coordinates on \(\mathcal P\), and let
\[
s^A,\qquad A=1,\dots,m
\]
be coordinates on \(\mathcal S\).

A smooth emergence operator is locally a map
\[
s^A=\mathcal E^A(p).
\]

Expanding around a base point \(p_0\), and writing
\[
\delta p^i=p^i-p_0^i,
\]
we obtain
\[
\mathcal E^A(p)
=
\mathcal E^A(p_0)
+
E^A{}_i\,\delta p^i
+
\frac{1}{2!}E^A{}_{ij}\,\delta p^i\delta p^j
+
\frac{1}{3!}E^A{}_{ijk}\,\delta p^i\delta p^j\delta p^k
+\cdots,
\]
where
\[
E^A{}_{i_1\cdots i_k}
=
\left.
\frac{\partial^k \mathcal E^A}
{\partial p^{i_1}\cdots \partial p^{i_k}}
\right|_{p_0}.
\]

The tensors
\[
E^A{}_{i_1\cdots i_k}
\]
are the **order-\(k\) emergence tensors**.

---

### 7.1 Reducible and irreducible emergence

Not every higher derivative represents genuine emergence. Some terms factor through lower-order structures.

Let
\[
\operatorname{Hom}^k_{\mathrm{sym}}(\mathcal P,\mathcal S)
\]
be the space of symmetric \(k\)-linear maps from \(\mathcal P\) to \(\mathcal S\).

Let
\[
\mathcal R_k
\subset
\operatorname{Hom}^k_{\mathrm{sym}}(\mathcal P,\mathcal S)
\]
be the subspace of maps reducible to compositions of lower-order maps.

The **irreducible emergence tensor** of order \(k\) is the equivalence class
\[
\mathcal N^A{}_{i_1\cdots i_k}
=
\left[
E^A{}_{i_1\cdots i_k}
\right]
\in
\operatorname{Hom}^k_{\mathrm{sym}}(\mathcal P,\mathcal S)/\mathcal R_k.
\]

If
\[
\mathcal N^A{}_{i_1\cdots i_k}\neq 0,
\]
then the system exhibits irreducible order-\(k\) emergence.

The **novelty rank** at order \(k\) is
\[
\nu_k
=
\operatorname{rank}
\left(
\mathcal N^A{}_{i_1\cdots i_k}
\right).
\]

The total local novelty rank is
\[
\nu_{\mathrm{loc}}
=
\sum_{k\geq 2}\nu_k.
\]

The sum begins at \(k=2\) because \(k=1\) corresponds to linear propagation of primitive data, not emergent interaction.

---

### 7.2 Tensor transformation law

Under primitive coordinate transformations
\[
p'^i=p'^i(p),
\]
and emergent coordinate transformations
\[
s'^A=s'^A(s),
\]
the full emergence tensors transform with additional lower-order correction terms. However, modulo the reducible subspace \(\mathcal R_k\), the irreducible emergence tensor transforms tensorially:
\[
\mathcal N'^A{}_{i_1\cdots i_k}
=
\frac{\partial s'^A}{\partial s^B}
\frac{\partial p^{j_1}}{\partial p'^{i_1}}
\cdots
\frac{\partial p^{j_k}}{\partial p'^{i_k}}
\,
\mathcal N^B{}_{j_1\cdots j_k}.
\]

Thus the vanishing or nonvanishing of \(\mathcal N\) is coordinate invariant.

---

### 7.3 Pairwise and higher-order emergence

For two primitive sectors \(P_1,P_2\), the leading emergent interaction is encoded in
\[
E^A{}_{ij},
\]
where \(i\) indexes degrees of freedom in \(P_1\) and \(j\) indexes degrees of freedom in \(P_2\).

If
\[
E^A{}_{ij}
=
u^A{}_i v_j
+
w^A{}_j z_i
\]
for suitable lower-order factors, then the interaction is reducible.

If no such decomposition exists, the pairwise emergence tensor is irreducible.

For three sectors, the irreducible three-way emergence tensor is
\[
\mathcal N^A{}_{ijk}.
\]
It captures structure that cannot be reduced to any combination of one-body or two-body effects.

This provides a rigorous analogue of synergy, but without appealing to information-theoretic interpretation unless desired.

---

## 8. Hierarchical Organization

Emergence is rarely a one-step phenomenon. Structures generated at one level become constituents at a higher level.

UET formalizes this through hierarchical towers.

### 8.1 Hierarchical tower

A **hierarchical emergence system** is a sequence of categories
\[
\mathsf{Prim}_0,
\mathsf{Prim}_1,
\mathsf{Prim}_2,
\dots
\]
together with emergence operators
\[
\mathcal E_n:\mathsf{Prim}_n\longrightarrow \mathsf{Prim}_{n+1}.
\]

The interpretation is:

- Level \(0\): microscopic primitives.
- Level \(1\): emergent structures generated from level \(0\).
- Level \(2\): emergent structures generated from level \(1\), now treated as primitives.
- And so on.

Thus
\[
P_{n+1}=\mathcal E_n(P_n)
\]
for a hierarchical chain.

### 8.2 Realization functors

For each \(n\), assume there exists a realization functor
\[
\pi_n:\mathsf{Prim}_{n+1}\to \mathsf{Prim}_n.
\]

It forgets higher-level structure and returns the lower-level substrate.

We require
\[
\pi_n(\mathcal E_n(P_n))\cong P_n.
\]

This expresses realizability: a higher-level emergent structure is realized by a lower-level configuration.

But the converse need not hold:
\[
\mathcal E_n(\pi_n(P_{n+1}))\not\cong P_{n+1}
\]
in general.

The difference is higher-level novelty.

### 8.3 Higher-level novelty

At level \(n\), the assembly map is
\[
m^{(n)}_{P,Q}:
\mathcal E_n(P)\boxtimes \mathcal E_n(Q)
\to
\mathcal E_n(P\otimes Q).
\]

The corresponding novelty object is
\[
\operatorname{Nov}_n(P,Q)
=
\operatorname{coker}(m^{(n)}_{P,Q}).
\]

Hierarchical emergence is nontrivial if for some \(n\),
\[
\operatorname{Nov}_n(P,Q)\neq 0.
\]

A hierarchy is **strongly emergent** if there are infinitely many levels \(n\) for which novelty is nontrivial and stable.

### 8.4 Monadic formulation

Under suitable coherence assumptions, hierarchical emergence can be encoded by a monad.

Let
\[
U_n:\mathsf{Prim}_{n+1}\to \mathsf{Prim}_n
\]
be a forgetful or realization functor.

Define the endofunctor
\[
T_n=U_n\circ \mathcal E_n:
\mathsf{Prim}_n\to \mathsf{Prim}_n.
\]

If there exist natural transformations
\[
\eta_n:\operatorname{id}_{\mathsf{Prim}_n}\to T_n
\]
and
\[
\mu_n:T_n^2\to T_n
\]
satisfying the usual monad laws, then \(T_n\) is a **hierarchical emergence monad**.

The unit \(\eta_n\) embeds a primitive configuration into its emergent closure.

The multiplication \(\mu_n\) collapses iterated emergence:
\[
T_n(T_n(P))\longrightarrow T_n(P).
\]

Algebras over \(T_n\) represent stable emergent organizations closed under the relevant hierarchical operation.

This monadic viewpoint is especially useful for recursive systems, self-organization, and fixed-point phenomena.

---

## 9. Emergence Morphisms

To compare emergent systems, we require morphisms preserving emergence structure.

### 9.1 Strict emergence morphisms

Let
\[
(P,\mathcal E(P))
\]
and
\[
(Q,\mathcal E(Q))
\]
be emergent systems.

A **strict emergence morphism**
\[
(P,\mathcal E(P))\longrightarrow (Q,\mathcal E(Q))
\]
is a primitive morphism
\[
f:P\to Q
\]
such that the induced square commutes:
\[
\mathcal E(f):\mathcal E(P)\to \mathcal E(Q).
\]

In diagrammatic form:
\[
\begin{CD}
P @>{f}>> Q\\
@V{\mathcal E}VV @VV{\mathcal E}V\\
\mathcal E(P) @>{\mathcal E(f)}>> \mathcal E(Q)
\end{CD}
\]

This is simply a morphism in the arrow category of \(\mathcal E\).

### 9.2 Lax emergence morphisms

A more flexible notion allows an independent emergent morphism
\[
g:\mathcal E(P)\to \mathcal E(Q)
\]
together with a coherence cell
\[
\theta:
g\Longrightarrow \mathcal E(f)
\]
or
\[
\theta:
\mathcal E(f)\Longrightarrow g,
\]
depending on variance.

This is useful when the higher-level map is not completely determined by the lower-level map.

### 9.3 Stability-preserving morphisms

An emergence morphism is **stability-preserving** if
\[
\Sigma(\mathcal E(P))\leq \Sigma(\mathcal E(Q))
\]
or, in the stronger form,
\[
\Sigma(\mathcal E(P))=\Sigma(\mathcal E(Q)).
\]

This formalizes the idea that one emergent system can be transformed into another without destroying its organizational class.

### 9.4 Novelty-preserving morphisms

An emergence morphism is **novelty-preserving** if
\[
\nu(\mathcal E(P))=\nu(\mathcal E(Q)).
\]

More generally, one may allow monotone novelty maps:
\[
\nu(\mathcal E(P))\leq \nu(\mathcal E(Q)).
\]

The category \(\mathsf{Em}\) of emergent systems with such morphisms is the natural ambient category for UET.

---

## 10. Dynamics of Emergence

Static emergence operators describe structure. Many applications require dynamics.

### 10.1 Pushforward dynamics

Let primitive configurations evolve according to
\[
\dot p^i=f^i(p).
\]

The induced emergent dynamics is
\[
\dot s^A
=
\frac{\partial \mathcal E^A}{\partial p^i}\dot p^i
=
\frac{\partial \mathcal E^A}{\partial p^i}f^i(p).
\]

In tensor notation,
\[
\dot s^A
=
E^A{}_i f^i.
\]

If the emergent dynamics can be written autonomously as
\[
\dot s^A=F^A(s),
\]
then the emergence operator is dynamically closed.

Dynamic closure is a strong form of emergence: the higher-level structure not only exists but evolves according to its own effective laws.

### 10.2 Covariant emergence

If emergence is path-dependent, we introduce a connection on the emergence bundle.

The covariant derivative of the emergent state is
\[
\frac{D s^A}{dt}
=
\dot s^A
+
\Gamma^A{}_{B i}s^B \dot p^i,
\]
where
\[
\Gamma^A{}_{B i}
\]
is an emergence connection.

The curvature
\[
F^A{}_{Bij}
\]
measures failure of path independence.

Thus,
\[
F^A{}_{Bij}\neq 0
\]
means that the emergent structure obtained from a primitive configuration may depend on the historical route by which that configuration was assembled.

This is a precise mathematical version of historical emergence.

### 10.3 Variational formulation

Let \(L_{\mathsf{Prim}}(p,\dot p)\) be a primitive Lagrangian and \(L_{\mathsf{Em}}(s,\dot s)\) an emergent Lagrangian.

A constrained variational principle for emergence is
\[
\delta
\int
\left[
L_{\mathsf{Prim}}(p,\dot p)
+
L_{\mathsf{Em}}(s,\dot s)
+
\lambda_A\left(s^A-\mathcal E^A(p)\right)
\right]dt
=0.
\]

The Lagrange multipliers \(\lambda_A\) enforce the emergence constraint.

The resulting Euler–Lagrange equations describe coupled primitive-emergent dynamics.

---

## 11. Applications and Interpretative Models

UET is not tied to a specific domain. We now indicate how the formalism specializes to several major areas.

---

## 11.1 Statistical mechanics

Let \(\Gamma\) be the microstate space of a many-body system.

Primitive configurations are microscopic states:
\[
p=x\in \Gamma.
\]

The emergence operator is coarse-graining:
\[
\mathcal E:\Gamma\to \mathcal M,
\]
where \(\mathcal M\) is a space of macrostates.

For example,
\[
\mathcal E(x)=\mu_x,
\]
where \(\mu_x\) is an empirical measure or local thermodynamic profile.

The assembly map compares the macrostate of the full system with the combination of macrostates of subsystems.

Novelty appears when thermodynamic phases, order parameters, or broken symmetries cannot be reconstructed from independent subsystem descriptions.

Stability classes correspond to thermodynamic phases.

The stability potential is the free energy:
\[
V(m)=F(m).
\]

The Hessian
\[
H_{AB}=\frac{\partial^2 F}{\partial m^A\partial m^B}
\]
detects phase stability and criticality.

At critical points,
\[
\det H=0,
\]
and stability classes change. This corresponds to phase transitions.

The renormalization group is a hierarchical emergence tower:
\[
\mathsf{Prim}_n\to \mathsf{Prim}_{n+1},
\]
where each level integrates out shorter-scale degrees of freedom.

Novelty invariants correspond to universal quantities such as critical exponents, topological order parameters, or anomalies.

---

## 11.2 Biological organization

Let primitive entities be molecular components:
\[
P=\text{genes, proteins, metabolites, signaling factors}.
\]

The emergence operator maps molecular interaction networks to cellular or tissue-level organization:
\[
\mathcal E(P)=\text{phenotype, regulatory state, tissue architecture}.
\]

Stability classes correspond to homeostatic regimes or attractor basins.

A cell type is a stable emergent class:
\[
[\mathcal E(P)]_\sigma.
\]

Novelty invariants measure regulatory structures not reducible to individual molecular activity.

For example, a feedback loop can generate a stable phenotype even when no individual molecule possesses that property.

In UET, biological organization is represented by a hierarchy:
\[
\text{molecules}
\to
\text{cells}
\to
\text{tissues}
\to
\text{organs}
\to
\text{organisms}.
\]

Each level is an emergent category relative to the one below.

Path dependence in development is captured by nonzero curvature of the emergence bundle:
\[
F^\nabla\neq 0.
\]

Thus developmental history can affect final organization.

---

## 11.3 Artificial intelligence

Let
\[
p=\theta
\]
be the parameter configuration of a model, or a collection of architectural components.

The emergence operator maps parameters and architecture to capabilities or representations:
\[
\mathcal E(\theta)=\text{representation space, capability profile, behavioral policy}.
\]

For large models, capabilities often appear only when multiple components interact:
\[
\operatorname{Nov}(\text{layers},\text{data},\text{scale})\neq 0.
\]

Stability classes correspond to robustness basins:
\[
[\mathcal E(\theta)]_\sigma
\]
under perturbations of weights, data distribution, or inference parameters.

Higher-order emergence tensors quantify irreducible interactions among layers, attention heads, modalities, or training objectives.

For example, a capability may not be attributable to any single layer or dataset feature. In UET, this is expressed as a nonzero higher-order novelty invariant:
\[
\Delta_A(\mathcal E)\neq 0.
\]

Hierarchical emergence corresponds to layered abstraction:
\[
\text{tokens}
\to
\text{embeddings}
\to
\text{features}
\to
\text{concepts}
\to
\text{policies}
\to
\text{agentic behavior}.
\]

---

## 11.4 Network science

Let a primitive configuration be a graph
\[
G=(V,E).
\]

The emergence operator maps graphs to higher-order structures:
\[
\mathcal E(G)=\text{communities, motifs, simplicial complexes, spectral phases}.
\]

For example,
\[
\mathcal E(G)=H_k(G),
\]
where \(H_k\) is a homology group obtained from a clique or Vietoris–Rips complex.

Novelty appears when global topological features are not reducible to local edge statistics.

The assembly map compares the topology of the full graph with the topologies of subgraphs.

If
\[
H_k(G)\neq 0
\]
while all lower-order pieces fail to account for this homology, then
\[
\operatorname{Nov}\neq 0.
\]

Stability classes correspond to persistence intervals in persistent homology.

A topological feature persistent over a wide filtration interval belongs to a stable emergence class.

---

## 11.5 Theoretical physics

In fundamental physics, primitive entities may be local degrees of freedom, algebraic observables, or pregeometric relational data.

The emergence operator may produce:
\[
\mathcal E(\text{local data})=\text{spacetime geometry},
\]
or
\[
\mathcal E(\text{microscopic rules})=\text{effective field theory}.
\]

Gauge constraints are a natural source of novelty. The full physical state space is not the product of local degrees of freedom but a constrained quotient.

In UET, constraints produce nontrivial kernels:
\[
\operatorname{Red}(P,Q)\neq 0,
\]
while gauge-invariant global degrees of freedom produce novelty:
\[
\operatorname{Nov}(P,Q)\neq 0.
\]

Anomalies are cohomological novelty invariants. If a classical symmetry cannot be preserved quantum mechanically, the obstruction is represented by a nontrivial cohomology class:
\[
[\omega]\in H^{d+1}(BG,\mathbb Z)
\]
or a related cohomology group.

Spacetime emergence may be modeled by an emergence bundle whose curvature encodes path-dependent geometric realization. Nonzero characteristic classes indicate that no global reduction to independent local data is possible.

The hierarchy of effective field theories is a hierarchical UET tower:
\[
\mathsf{Prim}_0
\to
\mathsf{Prim}_1
\to
\mathsf{Prim}_2
\to\cdots,
\]
where each level integrates out shorter-distance structure and generates new effective degrees of freedom.

---

## 12. Main Structural Results

We collect several central propositions of UET.

---

### Proposition 12.1: Reducibility criterion

An emergence operator \(\mathcal E\) is reducible if and only if all assembly maps
\[
m_{P,Q}
\]
are isomorphisms.

**Proof.**  
If all \(m_{P,Q}\) are isomorphisms, then for every composite system,
\[
\mathcal E(P\otimes Q)
\cong
\mathcal E(P)\boxtimes \mathcal E(Q),
\]
so the emergent whole is equivalent to the composition of emergent parts. Conversely, if the operator is reducible, the whole must be equivalent to the independent assembly of parts for all \(P,Q\), hence \(m_{P,Q}\) must be an isomorphism. \(\square\)

---

### Proposition 12.2: Novelty detection

In an additive realization, if
\[
\operatorname{Nov}(P,Q)\neq 0,
\]
then
\[
\mathcal E(P\otimes Q)
\]
contains structure not generated by
\[
\mathcal E(P)\oplus \mathcal E(Q).
\]

**Proof.**  
By definition,
\[
\operatorname{Nov}(P,Q)
=
\operatorname{coker}(\alpha_{P,Q}).
\]
If the cokernel is nonzero, the assembly map is not surjective. Hence there exist elements of \(\mathcal E(P\otimes Q)\) not in the image of the independent parts. \(\square\)

---

### Proposition 12.3: Stability invariance of novelty

If a novelty invariant \(\nu\) is stability-sensitive and
\[
S\sim_\sigma T,
\]
then
\[
\nu(S)=\nu(T).
\]

**Proof.**  
Stability equivalence is generated by admissible deformations preserving the relevant observable structure. By Axiom UET-5, stability-sensitive novelty invariants are invariant under such deformations. Hence the invariant is constant on stability classes. \(\square\)

---

### Proposition 12.4: Higher-order emergence is not pairwise reducible

If
\[
\Delta_{\{1,2,3\}}(\mathcal E)\neq 0,
\]
then the three-way emergent structure cannot be expressed as a combination of one-body and two-way emergent contributions.

**Proof.**  
The Möbius formula subtracts all lower-order contributions from the full composite. If the resulting class in \(K_0\) is nonzero, the full class is not equal to the alternating sum of lower-order classes. Hence irreducible three-way structure remains. \(\square\)

---

### Theorem 12.5: Hierarchical novelty propagation

Suppose a hierarchical system satisfies
\[
\operatorname{Nov}_n(P,Q)\neq 0
\]
at level \(n\), and suppose the level-\(n\) novelty object is mapped by \(\mathcal E_{n+1}\) to a nontrivial object at level \(n+1\). Then level-\(n\) emergence induces nontrivial higher-level novelty.

**Proof sketch.**  
Apply the emergence operator \(\mathcal E_{n+1}\) to the exact sequence defining \(\operatorname{Nov}_n\). If the induced map on novelty objects is nonzero and the target category preserves exactness sufficiently, then the image of \(\operatorname{Nov}_n\) contributes a nonzero subobject or quotient to \(\operatorname{Nov}_{n+1}\). Thus novelty propagates upward. \(\square\)

This theorem formalizes the idea that emergent structure at one level can seed further emergence at higher levels.

---

## 13. Classification Program

UET suggests a classification problem for emergent systems.

Given an emergence operator \(\mathcal E\), classify:

1. **Its reducibility type**  
   Determine where \(m_{P,Q}\) is an isomorphism, epimorphism, monomorphism, or neither.

2. **Its stability classes**  
   Partition \(\mathcal S\) into equivalence classes under stable deformation.

3. **Its novelty spectrum**  
   Compute
   \[
   \{\nu_k\}_{k\geq 2}
   \]
   or
   \[
   \{\Delta_A(\mathcal E)\}_A.
   \]

4. **Its hierarchical depth**  
   Determine the maximal or infinite sequence of nontrivial levels
   \[
   \mathsf{Prim}_0\to \mathsf{Prim}_1\to\cdots.
   \]

5. **Its geometric obstruction class**  
   If an emergence bundle exists, compute characteristic classes
   \[
   c_k(\mathcal E).
   \]

6. **Its morphism category**  
   Identify transformations preserving stability and novelty.

This classification program is analogous to the classification of phases in physics, but applies to general emergent systems.

---

## 14. Computational Considerations

Although this paper is foundational, UET suggests concrete computational tasks.

### 14.1 Estimating emergence tensors

Given data samples of primitive configurations and emergent observables, one may estimate derivatives
\[
E^A{}_{i_1\cdots i_k}
\]
by regression, automatic differentiation, or kernel methods.

The irreducible novelty rank is estimated by projecting estimated tensors onto the quotient
\[
\operatorname{Hom}^k_{\mathrm{sym}}/\mathcal R_k.
\]

### 14.2 Stability detection

Stability classes may be approximated by:

- perturbation sampling,
- persistence diagrams,
- Lyapunov exponents,
- free-energy minima,
- attractor basins,
- topological invariants over filtrations.

### 14.3 Hierarchical inference

Given multi-scale data, one can attempt to reconstruct functors
\[
\mathcal E_n:\mathsf{Prim}_n\to \mathsf{Prim}_{n+1}
\]
by learning maps between representations at successive scales.

The failure of compositionality at each level provides an empirical novelty signal.

---

## 15. Conceptual Implications

UET changes the conceptual status of emergence.

Traditionally, emergence is treated as a secondary phenomenon: a system is emergent if it appears to have properties not explainable by its parts.

In UET, emergence is primary. It is an operation with formal properties, invariants, and classification theory.

The central conceptual shift is:

> Emergence is not a relation between levels. It is the operation by which levels are generated.

This does not deny the importance of reduction. Rather, it clarifies the precise sense in which reduction can fail.

Reduction corresponds to the existence of an isomorphism
\[
\mathcal E(P\otimes Q)
\cong
\mathcal E(P)\boxtimes \mathcal E(Q).
\]

Emergence corresponds to the failure of that isomorphism in a stable, invariant manner.

Thus UET provides a non-mystical but non-reductive account of emergence.

---

## 16. Limitations and Scope

The present framework is formal. It does not by itself provide:

1. a unique choice of primitive category,
2. a unique emergence operator for a given physical system,
3. a universal metric on emergent structures,
4. a complete computational algorithm for novelty estimation.

These choices are model-dependent.

However, UET supplies the invariant mathematical skeleton into which such model-specific choices can be inserted.

The value of the theory lies in making precise what must be specified, what must be measured, and what must be preserved under transformation.

---

## 17. Future Directions

Several extensions are natural.

1. **Probabilistic UET**  
   Replace deterministic emergence operators with Markov kernels or stochastic functors.

2. **Quantum UET**  
   Use monoidal categories of Hilbert spaces, operator algebras, or process theories.

3. **Higher-categorical UET**  
   Model emergence between higher structures using \((\infty,1)\)-categories or homotopy type theory.

4. **Information-theoretic UET**  
   Relate novelty invariants to mutual information, interaction information, and partial information decomposition.

5. **Computational UET**  
   Develop algorithms for estimating emergence tensors and stability classes from data.

6. **Physical UET**  
   Apply the framework to spacetime emergence, gauge theory, and renormalization.

7. **Biological UET**  
   Formalize organizational closure, autopoiesis, and developmental trajectories.

8. **AI UET**  
   Quantify emergent capabilities in large models through higher-order novelty invariants.

---

## 18. Conclusion

Universal Emergence Theory proposes a rigorous mathematical treatment of emergence as a fundamental operation.

The central structure is an emergence operator
\[
\mathcal E:\mathcal P\to \mathcal S
\]
equipped with lax monoidal composition, stability classes, novelty invariants, hierarchical organization, and morphisms.

The central mathematical insight is that emergence is detected by the failure of assembly maps to be isomorphisms. This failure can be measured algebraically by kernels and cokernels, geometrically by curvature and characteristic classes, and locally by irreducible emergence tensors.

Stability ensures that emergent novelty is not a transient artifact. Hierarchy ensures that emergent structures can become new primitives, generating multi-scale organization. Morphisms provide the appropriate notion of comparison and equivalence.

UET therefore transforms emergence from a qualitative notion into a formal object of mathematical analysis.

The framework is intentionally general, but its definitions are sharp enough to support theorem proving, model building, and computational approximation. It provides a foundation for a universal science of emergent organization.

---

## Appendix A: Summary of Core Definitions

| Object | Definition |
|---|---|
| Primitive category | \(\mathsf{Prim}=(\mathcal P,\otimes,I)\) |
| Emergent category | \(\mathsf{Struct}=(\mathcal S,\boxtimes,J)\) |
| Emergence operator | \(\mathcal E:\mathsf{Prim}\to \mathsf{Struct}\) |
| Assembly map | \(m_{P,Q}:\mathcal E(P)\boxtimes \mathcal E(Q)\to \mathcal E(P\otimes Q)\) |
| Reducibility | \(m_{P,Q}\) is an isomorphism |
| Novelty object | \(\operatorname{Nov}(P,Q)=\operatorname{coker}(\alpha_{P,Q})\) |
| Redundancy object | \(\operatorname{Red}(P,Q)=\ker(\alpha_{P,Q})\) |
| Stability class | \([S]_\sigma\) under admissible deformation |
| Emergence tensor | \(E^A{}_{i_1\cdots i_k}\) |
| Irreducible emergence tensor | \(\mathcal N^A{}_{i_1\cdots i_k}\) modulo reducible subspace |
| Hierarchical tower | \(\mathsf{Prim}_0\to \mathsf{Prim}_1\to \mathsf{Prim}_2\to\cdots\) |
| Emergence morphism | Morphism preserving \(\mathcal E\), \(\Sigma\), and \(\nu\) |

---

## Appendix B: Notation

\[
\mathcal P
\]
Primitive domain.

\[
\mathcal S
\]
Emergent domain.

\[
\mathcal E
\]
Emergence operator.

\[
m_{P,Q}
\]
Assembly map.

\[
\Sigma
\]
Stability functor.

\[
\nu
\]
Novelty invariant.

\[
\operatorname{Nov}(P,Q)
\]
Novelty object.

\[
\operatorname{Red}(P,Q)
\]
Redundancy object.

\[
\Delta_A(\mathcal E)
\]
Möbius novelty invariant for subset \(A\).

\[
E^A{}_{i_1\cdots i_k}
\]
Order-\(k\) emergence tensor.

\[
\mathcal N^A{}_{i_1\cdots i_k}
\]
Irreducible emergence tensor.

\[
F^\nabla
\]
Curvature of emergence connection.

\[
c_k(\mathcal E)
\]
Characteristic novelty class.

---
