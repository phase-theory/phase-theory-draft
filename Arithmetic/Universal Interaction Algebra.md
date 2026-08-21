# Universal Interaction Algebra

**Preprint**

---

## Abstract

This paper develops **Universal Interaction Algebra** (UIA), an algebraic framework in which *interaction*, rather than elementhood or binary composition, is the primitive notion. Classical algebraic operations \(a*b\) are replaced by multiway **interaction tensors**
\[
\mathcal I(A_1,A_2,\ldots,A_r),
\]
whose arguments are objects, states, agents, subsystems, or contextual probes. Objects are not assumed to be given by intrinsic attributes; they are recovered from their total interaction profile against all possible contexts. After establishing an axiomatic tensorial foundation, we prove that finitary universal algebra embeds into UIA via structure tensors, and that algebraic identities become tensor contraction identities. We then develop three principal application domains: network theory, where UIA gives a unified tensor calculus for hypergraphs, message passing, and nonlinear diffusion; quantum theory, where interaction rank quantifies entanglement and locality is expressed as bounded tensor arity; and multi-agent mathematics, where payoff tensors, Nash equilibria, potential games, and coalition values are formulated as interaction-algebraic structures. The resulting framework provides a common language for algebra, networks, quantum systems, and multi-agent dynamics.

**Keywords:** interaction tensor, universal algebra, tensor networks, nondegenerate pairing, hypergraphs, quantum entanglement, potential games, multi-agent systems.

**MSC 2020:** 08A05, 15A69, 81P45, 91A10, 05C65.

---

## 1. Introduction

Classical algebra usually begins with a carrier set \(S\) and operations such as
\[
*:S\times S\to S,\qquad (a,b)\mapsto a*b.
\]
The elements of \(S\) are treated as primary, and the operation is a rule acting on them. This perspective is extraordinarily successful, but it becomes strained in settings where the elementary entities are not naturally isolated points, but are instead known only through their relations to other entities. Examples include:

1. **Networks**, where nodes acquire meaning through adjacency, hyperedge participation, and message-passing behavior.
2. **Quantum systems**, where subsystems are identified through correlations, entanglement, and interaction Hamiltonians.
3. **Multi-agent systems**, where agents are characterized by strategies, payoffs, and responses to other agents.
4. **Modern algebraic physics**, where observables, processes, and correlations often precede the notion of an underlying object.

The guiding principle of Universal Interaction Algebra is therefore:

> **Interaction is primitive. Objects are the totality of their possible interactions.**

Instead of beginning with a binary operation \(a*b\), we introduce interaction tensors
\[
\mathcal I(A_1,A_2,\ldots,A_r),
\]
which assign a scalar, amplitude, or typed output to an ordered or typed collection of arguments. A binary product, when desired, is not primitive but is recovered from a ternary interaction tensor by pairing the output leg with a test object:
\[
\langle A*B,\,C\rangle = \mathcal I(A,B,C).
\]
Thus the usual multiplication is replaced by an interaction-with-a-probe. More generally, an \(n\)-ary operation is induced from an \((n+1)\)-ary interaction tensor.

UIA is “universal” in two senses:

1. **Arity universality.** Interactions may be unary, binary, ternary, or higher-order. Hyperedges, many-body Hamiltonians, and multi-agent payoff structures are naturally higher-order.
2. **Algebraic universality.** Classical algebraic structures can be encoded inside UIA. Operations become induced maps, identities become tensor contraction identities, and homomorphisms become interaction-preserving linear maps.

The present paper develops the formal foundation of UIA and demonstrates its scope in algebra, network theory, quantum systems, and multi-agent mathematics.

---

## 2. Axiomatic Foundation

### 2.1 Object spaces and pairings

Let \(\mathbb K\) be a field, typically \(\mathbb R\) or \(\mathbb C\). Let \(V\) be a finite-dimensional \(\mathbb K\)-vector space, or more generally a free module over a commutative ring when one wants a purely algebraic version. We equip \(V\) with a nondegenerate bilinear pairing
\[
\langle\cdot,\cdot\rangle:V\times V\to \mathbb K.
\]
In coordinates, choose a basis \(\{e_i\}\) of \(V\) and write
\[
g_{ij}=\langle e_i,e_j\rangle,
\]
with inverse matrix \(g^{ij}\), so that
\[
g_{ik}g^{kj}=\delta_i{}^j.
\]
The pairing identifies \(V\) with its dual:
\[
V\cong V^*,\qquad v\mapsto \langle v,\cdot\rangle.
\]

Elements of \(V\) are called **states** or **object vectors**. In concrete applications, basis vectors often represent elementary classical objects, while general vectors represent superpositions, mixed strategies, coarse-grained objects, or effective states.

**Typed version.** In many applications one has a family of spaces \(\{V_\alpha\}_{\alpha\in T}\). An interaction tensor then has type
\[
\mathcal I\in V_{\alpha_1}^*\otimes\cdots\otimes V_{\alpha_r}^*.
\]
All formulas below admit this typed generalization without essential change. For simplicity, the main development is untyped.

---

### 2.2 Interaction tensors and interaction profiles

An **interaction tensor of arity \(r\)** is an element
\[
\mathcal I\in (V^*)^{\otimes r}.
\]
Equivalently, \(\mathcal I\) is a multilinear form
\[
\mathcal I:V^{\times r}\to \mathbb K.
\]
In components,
\[
\mathcal I(A_1,\ldots,A_r)
=
I_{i_1\cdots i_r}A_1^{i_1}\cdots A_r^{i_r},
\]
with Einstein summation convention.

The central conceptual shift is that an object \(A\) is known through its **interaction profile**.

For each interaction tensor \(\mathcal I\) of arity \(r\), define the \(A\)-contextual interaction map
\[
\Phi_A^{(\mathcal I)}:V^{\times (r-1)}\to \mathbb K
\]
by
\[
\Phi_A^{(\mathcal I)}(B_2,\ldots,B_r)
=
\mathcal I(A,B_2,\ldots,B_r).
\]
Collecting over all arities and all distinguished interaction tensors gives the full profile
\[
\Phi_A=\{\Phi_A^{(\mathcal I)}\}_{\mathcal I}.
\]

We impose the following separation principle.

**Axiom 1: Interaction separation.**  
If
\[
\Phi_A=\Phi_B
\]
for all interaction tensors and all contexts, then
\[
A=B.
\]
Equivalently, if \(A\neq 0\), then there exists an interaction tensor \(\mathcal I\) and a context \((B_2,\ldots,B_r)\) such that
\[
\mathcal I(A,B_2,\ldots,B_r)\neq 0.
\]

Thus objects are determined by how they interact with all possible contexts.

---

### 2.3 Induced operations from interaction tensors

Suppose \(\mathcal I\) is an interaction tensor of arity \(n+1\). It induces an \(n\)-ary operation
\[
\mu_{\mathcal I}:V^{\times n}\to V
\]
by the relation
\[
\boxed{
\langle \mu_{\mathcal I}(A_1,\ldots,A_n),\,Z\rangle
=
\mathcal I(A_1,\ldots,A_n,Z)
}
\]
for every test object \(Z\in V\).

In coordinates, if
\[
\mathcal I\in (V^*)^{\otimes (n+1)}
\]
has components \(I_{i_1\cdots i_n k}\), then
\[
\boxed{
\mu_{\mathcal I}(A_1,\ldots,A_n)^m
=
I_{i_1\cdots i_n k}
A_1^{i_1}\cdots A_n^{i_n}
g^{km}.
}
\]

In particular, a ternary tensor \(\mathcal I\in (V^*)^{\otimes 3}\) induces a binary operation
\[
A*B=\mu_{\mathcal I}(A,B)
\]
by
\[
\langle A*B,C\rangle=\mathcal I(A,B,C).
\]
In components,
\[
\boxed{
(A*B)^m=I_{ij k}A^i B^j g^{km}.
}
\]

Thus the familiar binary operation \(A*B\) is not primitive; it is the shadow of a ternary interaction after the output leg has been paired with a test object.

---

### 2.4 Composition by contraction

Interaction tensors compose by **index contraction**. Let
\[
\mathcal I\in (V^*)^{\otimes r},
\qquad
\mathcal J\in (V^*)^{\otimes s}.
\]
After permuting legs if necessary, define their contraction along one leg by
\[
\boxed{
(\mathcal I\bullet \mathcal J)_{i_1\cdots i_{r-1}j_1\cdots j_{s-1}}
=
I_{i_1\cdots i_{r-1}a}
g^{ab}
J_{j_1\cdots j_{s-1}b}.
}
\]
Evaluated on vectors,
\[
(\mathcal I\bullet \mathcal J)(X_1,\ldots,X_{r-1},Y_1,\ldots,Y_{s-1})
=
I_{i_1\cdots i_{r-1}a}
g^{ab}
J_{j_1\cdots j_{s-1}b}
X_1^{i_1}\cdots X_{r-1}^{i_{r-1}}
Y_1^{j_1}\cdots Y_{s-1}^{j_{s-1}}.
\]

This is exactly the tensor-network operation of joining two vertices by an internal edge and summing over the internal index.

Let \(\mathscr I\) be a collection of interaction tensors. Its **interaction algebra** is the smallest linear space of tensors containing \(\mathscr I\) and closed under leg permutations and contractions. We denote it by
\[
\operatorname{Int}(\mathscr I).
\]

---

### 2.5 Definition of a Universal Interaction Algebra

We can now state the central definition.

A **Universal Interaction Algebra** over \(\mathbb K\) is a triple
\[
\mathfrak A=(V,\langle\cdot,\cdot\rangle,\mathscr I),
\]
where \(V\) is a vector space, \(\langle\cdot,\cdot\rangle\) is a nondegenerate bilinear pairing, and \(\mathscr I\) is a graded family of interaction tensors
\[
\mathscr I=\bigoplus_{r\geq 1}\mathscr I_r,
\qquad
\mathscr I_r\subseteq (V^*)^{\otimes r},
\]
satisfying the following axioms.

#### Axiom U1: Multilinearity

Every interaction tensor is multilinear in its arguments.

#### Axiom U2: Interaction separation

The combined interaction profiles separate points of \(V\). That is, if
\[
\mathcal I(A,B_2,\ldots,B_r)
=
\mathcal I(A',B_2,\ldots,B_r)
\]
for all \(\mathcal I\in\mathscr I\) and all contexts \(B_2,\ldots,B_r\), then \(A=A'\).

#### Axiom U3: Contraction closure

The interaction algebra \(\operatorname{Int}(\mathscr I)\) is closed under tensor contraction. In particular, if \(\mathcal I,\mathcal J\in\operatorname{Int}(\mathscr I)\), then every contraction
\[
\mathcal I\bullet \mathcal J
\]
belongs again to \(\operatorname{Int}(\mathscr I)\), up to the appropriate arity reduction.

#### Axiom U4: Coherence of contractions

All contraction diagrams that have the same boundary legs and the same formal connectivity define the same tensor. Equivalently, evaluation of interaction networks is independent of the order in which internal contractions are performed.

For a designated ternary interaction tensor representing a binary product, coherence reduces to associativity identities, derived below.

#### Axiom U5: Units and vacua, when specified

If a given interaction tensor is declared to have a unit, then there exists a distinguished vector \(\mathbf 1\in V\) satisfying the appropriate unit identities. More generally, one may include vacuum tensors that behave as caps, cups, or traces in the contraction calculus.

A **pointed UIA** is a UIA together with distinguished unit or vacuum tensors. An **unpointed UIA** need not possess units.

---

### 2.6 Conceptual interpretation

In a UIA, an object \(A\) is not primarily a point with internal attributes. It is a functional on the space of contexts:
\[
A\longmapsto \Phi_A.
\]
The object is the totality of its interactions. Algebraic operations are derived by choosing an interaction tensor and closing one leg against a test object. Composition is contraction. Equality of objects is equality of all interaction profiles. Equality of algebraic laws is equality of tensor networks.

This is the precise algebraic implementation of the principle:

\[
\boxed{
\text{Objects are determined by interactions; interactions compose by contraction.}
}
\]

---

## 3. Classical Algebra as Interaction Algebra

### 3.1 Binary products from ternary interactions

Let \(\mathcal I\in (V^*)^{\otimes 3}\). Define
\[
A*B=\mu_{\mathcal I}(A,B)
\]
by
\[
\langle A*B,C\rangle=\mathcal I(A,B,C).
\]
In components,
\[
(A*B)^m=I_{ij k}A^iB^j g^{km}.
\]

#### Commutativity

The product is commutative iff
\[
\boxed{
I_{ij k}=I_{ji k}.
}
\]

#### Right and left units

A vector \(\mathbf 1\in V\) is a left unit iff
\[
\boxed{
\mathbf 1^i I_{ij k}=g_{jk}.
}
\]
Indeed,
\[
(\mathbf 1*B)^m
=
\mathbf 1^i B^j I_{ij k}g^{km}
=
B^j g_{jk}g^{km}
=
B^m.
\]
Similarly, \(\mathbf 1\) is a right unit iff
\[
\boxed{
\mathbf 1^k I_{ij k}=g_{ij}.
}
\]

---

### 3.2 Associativity as a tensor identity

We derive the associativity condition for the induced product.

Compute
\[
((A*B)*C)^q.
\]
First,
\[
(A*B)^m=I_{ij a}A^iB^j g^{am}.
\]
Then
\[
((A*B)*C)^q
=
I_{mn p}(A*B)^m C^n g^{pq}.
\]
Substituting,
\[
((A*B)*C)^q
=
A^iB^jC^n
I_{ij a}g^{am}I_{mn p}g^{pq}.
\]

Similarly,
\[
(A*(B*C))^q
=
I_{a m p}A^a(B*C)^m g^{pq}.
\]
Since
\[
(B*C)^m=I_{j n b}B^jC^n g^{bm},
\]
we obtain
\[
(A*(B*C))^q
=
A^aB^jC^n
I_{j n b}g^{bm}I_{a m p}g^{pq}.
\]

Thus the product is associative, i.e.
\[
(A*B)*C=A*(B*C)
\]
for all \(A,B,C\), iff
\[
\boxed{
I_{ij}{}^{m} I_{m n p}
=
I_{j n}{}^{m} I_{i m p},
}
\]
where
\[
I_{ij}{}^{m}=I_{ij a}g^{am}.
\]

This is the UIA form of associativity. It is not an identity between elements but an identity between interaction tensors under contraction.

---

### 3.3 Lie algebras and Jacobi as a contraction identity

Let \(\mathfrak g\) be a Lie algebra with basis \(\{e_i\}\) and structure constants
\[
[e_i,e_j]=f_{ij}{}^k e_k.
\]
Choose the orthonormal pairing
\[
\langle e_i,e_j\rangle=\delta_{ij}.
\]
Define a ternary interaction tensor
\[
I_{ij k}=f_{ij}{}^m\delta_{mk}=f_{ij k}.
\]
Then the bracket is recovered by
\[
[A,B]^m=I_{ij k}A^iB^j\delta^{km}.
\]

Antisymmetry becomes
\[
\boxed{
I_{ij k}=-I_{ji k}.
}
\]

The Jacobi identity
\[
[[A,B],C]+[[B,C],A]+[[C,A],B]=0
\]
is equivalent to the contraction identity
\[
\boxed{
I_{ij}{}^{m}I_{m k l}
+
I_{jk}{}^{m}I_{m i l}
+
I_{ki}{}^{m}I_{m j l}
=0.
}
\]

Thus Lie algebra structure is encoded by a single ternary interaction tensor satisfying antisymmetry and a quadratic contraction identity.

---

### 3.4 Representation theorem for finitary algebras

We now show that ordinary finitary universal algebra embeds into UIA.

Let \(\mathcal A=(A,(\mu_\lambda)_{\lambda\in\Lambda})\) be an algebra with underlying set \(A\) and operations
\[
\mu_\lambda:A^{n_\lambda}\to A.
\]
Let \(V=\mathbb K[A]\) be the free vector space on \(A\), with basis \(\{e_a\}_{a\in A}\). Equip \(V\) with the orthonormal pairing
\[
\langle e_a,e_b\rangle=\delta_{ab}.
\]

For each operation \(\mu_\lambda\), define an interaction tensor
\[
\mathcal I^{(\lambda)}\in (V^*)^{\otimes (n_\lambda+1)}
\]
on basis elements by
\[
\mathcal I^{(\lambda)}(e_{a_1},\ldots,e_{a_{n_\lambda}},e_b)
=
\begin{cases}
1, & \mu_\lambda(a_1,\ldots,a_{n_\lambda})=b,\\
0, & \text{otherwise}.
\end{cases}
\]
Extend multilinearly.

Then the induced operation satisfies
\[
\mu_{\mathcal I^{(\lambda)}}(e_{a_1},\ldots,e_{a_{n_\lambda}})
=
e_{\mu_\lambda(a_1,\ldots,a_{n_\lambda})}.
\]
Thus the original operation is recovered exactly.

**Theorem 3.1 — Universal Representation Theorem.**  
Every finitary algebra with chosen basis embeds into a Universal Interaction Algebra. Algebraic identities in the original signature are equivalent to tensor contraction identities among the corresponding interaction tensors.

*Proof.*  
For basis elements, the induced operation was just shown to coincide with the original operation. By multilinearity, it coincides on all of \(V\). An algebraic term corresponds to a tensor network whose vertices are interaction tensors and whose internal edges are contractions using \(g^{ij}\). Equality of terms for all assignments is therefore equality of the corresponding tensor contractions. Conversely, equality of the contracted tensors implies equality of the induced operations on basis elements, hence equality of terms in the original algebra. ∎

**Corollary 3.2.**  
Universal algebra is a special case of UIA in which interactions are restricted to generating operation tensors and their contractions.

---

## 4. Network Theory as Interaction Algebra

Network theory is perhaps the most natural setting for UIA. Nodes interact through edges and hyperedges. These interactions may be pairwise or higher-order, deterministic or probabilistic, linear or nonlinear.

### 4.1 Hypergraphs and local interaction tensors

Let \(G=(V_G,E)\) be a finite hypergraph. Each vertex \(i\in V_G\) carries a state space \(W_i\). A hyperedge \(e\in E\) connects a subset of vertices
\[
\partial e\subseteq V_G.
\]
Assign to each hyperedge an interaction tensor
\[
\mathcal J_e\in \bigotimes_{i\in \partial e} W_i^*.
\]
If each vertex \(i\) has a state vector \(x_i\in W_i\), the local interaction energy is
\[
E_e(x_{\partial e})
=
\mathcal J_e\left(\bigotimes_{i\in \partial e}x_i\right).
\]
In components,
\[
E_e(x_{\partial e})
=
J_{e;a_e}\prod_{i\in \partial e}x_i^{a_i},
\]
where \(a_e=(a_i)_{i\in\partial e}\).

The total interaction energy is
\[
\boxed{
E(x)=\sum_{e\in E}J_{e;a_e}\prod_{i\in \partial e}x_i^{a_i}.
}
\]

This is a direct UIA object: the network is a collection of interaction tensors indexed by hyperedges.

---

### 4.2 Partition functions and tensor contractions

If the state spaces are discrete, one can define a partition function
\[
Z
=
\sum_{x}
\prod_{e\in E}
T_e(x_{\partial e}),
\]
where
\[
T_e=\exp(-\beta \mathcal J_e)
\]
or any other local interaction factor. In tensor notation,
\[
\boxed{
Z
=
\operatorname{Contr}_G\left(\{T_e\}_{e\in E}\right).
}
\]
That is, one takes the tensor product of all local tensors and contracts indices corresponding to shared vertices.

Thus a graphical model, spin system, constraint satisfaction problem, or probabilistic network is a UIA whose global observable is a contraction of local interaction tensors.

---

### 4.3 Message passing as tensor contraction

Message-passing algorithms are naturally expressed as contractions of interaction tensors.

For a hyperedge \(e\) and a vertex \(i\in\partial e\), define the message from \(e\) to \(i\) by
\[
\boxed{
m_{e\to i}^{a_i}
=
\sum_{a_{\partial e\setminus\{i\}}}
T_e^{a_{\partial e}}
\prod_{j\in \partial e\setminus\{i\}}
m_{j\to e}^{a_j}.
}
\]
The variable-to-factor message is
\[
\boxed{
m_{i\to e}^{a_i}
\propto
\prod_{e'\in \partial i\setminus\{e\}}
m_{e'\to i}^{a_i}.
}
\]

These equations are exactly local contractions in the interaction algebra of the network.

---

### 4.4 Gradient dynamics and generalized Laplacians

Suppose each \(W_i\) is Euclidean with metric \(g_i\). The gradient flow of the interaction energy is
\[
\dot x_i
=
-\nabla_i E.
\]
In components,
\[
\boxed{
\dot x_i^{b}
=
-
\sum_{e\ni i}
J_{e;a_e}
g_i^{b a_i}
\prod_{j\in \partial e\setminus\{i\}}x_j^{a_j}.
}
\]

For pairwise interactions, let
\[
E(x)=-\frac12 I_{ij}^{ab}x_i^a x_j^b,
\]
where \(I_{ij}^{ab}=I_{ji}^{ba}\). Then
\[
\frac{\partial E}{\partial x_i^a}
=
- I_{ij}^{ab}x_j^b,
\]
so gradient flow gives
\[
\boxed{
\dot x_i^a
=
I_{ij}^{ab}x_j^b.
}
\]

If states are scalar and \(I_{ij}=L_{ij}\), one recovers linear network dynamics
\[
\dot x_i=L_{ij}x_j.
\]
When \(L\) is a graph Laplacian, this is the usual consensus or diffusion dynamics.

**Proposition 4.1.**  
If the pairwise interaction tensor is symmetric,
\[
I_{ij}^{ab}=I_{ji}^{ba},
\]
then the dynamics
\[
\dot x_i^a=I_{ij}^{ab}x_j^b
\]
has Lyapunov function
\[
E(x)=-\frac12 I_{ij}^{ab}x_i^a x_j^b.
\]
Indeed,
\[
\frac{dE}{dt}
=
-\sum_i \|\dot x_i\|^2
\le 0.
\]

Thus symmetric interaction networks are gradient systems.

---

### 4.5 Interaction rank and community structure

Given a partition of vertices \(V_G=S\sqcup S^c\), group all indices belonging to \(S\) and \(S^c\). A global interaction tensor may be reshaped into a matrix
\[
\mathcal I_{A,B},
\]
where \(A\) indexes states on \(S\) and \(B\) indexes states on \(S^c\).

Define the **interaction rank across the cut** by
\[
\operatorname{rank}_S(\mathcal I)
=
\operatorname{rank}(\mathcal I_{A,B}).
\]
If
\[
\operatorname{rank}_S(\mathcal I)=1,
\]
the interaction factorizes across the cut:
\[
\mathcal I(A,B)=\mathcal I_S(A)\mathcal I_{S^c}(B).
\]
Higher rank indicates irreducible coupling between the two communities.

This gives a tensorial notion of community structure: low interaction rank across a cut means the two parts interact only through a small number of effective modes.

---

## 5. Quantum Systems as Interaction Algebras

Quantum theory is naturally tensorial. Hilbert spaces tensorize, amplitudes are tensors, observables are tensors, and channels are higher-order tensors. UIA provides a unifying language for these structures.

### 5.1 Quantum states as interaction tensors

Let
\[
\mathcal H=\bigotimes_{i=1}^n \mathcal H_i
\]
be a finite-dimensional multipartite Hilbert space. A pure state is a tensor
\[
\Psi\in \mathcal H,
\]
with components
\[
\Psi_{a_1\cdots a_n}.
\]
The amplitude of a configuration \((a_1,\ldots,a_n)\) is precisely the evaluation of the state tensor on basis probes:
\[
\Psi_{a_1\cdots a_n}
=
\Psi(e_{a_1},\ldots,e_{a_n})
\]
after identifying \(\mathcal H\) with a suitable dual via the Hilbert inner product.

Thus a quantum state is an interaction tensor assigning amplitudes to joint measurement contexts.

---

### 5.2 Interaction rank and entanglement

Let \(S\subset \{1,\ldots,n\}\) and \(S^c\) its complement. Reshape \(\Psi_{a_1\cdots a_n}\) into a matrix
\[
\Psi_{A,B},
\]
where \(A\) denotes the multi-index \((a_i)_{i\in S}\) and \(B\) denotes \((a_j)_{j\in S^c}\).

Define the **interaction rank across \(S\)** by
\[
\operatorname{rank}_S(\Psi)
=
\operatorname{rank}(\Psi_{A,B}).
\]

By the Schmidt decomposition,
\[
\Psi
=
\sum_{\alpha=1}^{r_S}
\lambda_\alpha\,
u_\alpha\otimes v_\alpha,
\]
where
\[
r_S=\operatorname{rank}_S(\Psi).
\]

**Theorem 5.1 — Productness and interaction rank.**  
The state \(\Psi\) is product across \(S|S^c\) iff
\[
\operatorname{rank}_S(\Psi)=1.
\]

*Proof.*  
If \(\Psi=u\otimes v\), then the reshaped matrix has rank one. Conversely, if the reshaped matrix has rank one, it is a single outer product, so \(\Psi\) factorizes. ∎

The reduced density matrix on \(S\) has eigenvalues
\[
p_\alpha=\lambda_\alpha^2.
\]
The entanglement entropy is
\[
S(\rho_S)
=
-\sum_{\alpha=1}^{r_S}p_\alpha\log p_\alpha.
\]
Since there are at most \(r_S\) nonzero eigenvalues,
\[
\boxed{
S(\rho_S)\le \log r_S.
}
\]

Thus interaction rank bounds entanglement entropy. Entanglement is precisely irreducible tensorial interaction between subsystems.

---

### 5.3 Hamiltonians as interaction tensors

A many-body Hamiltonian can be written as a sum of local interaction tensors:
\[
\boxed{
H
=
\sum_{S\subseteq \{1,\ldots,n\}}
H_S,
}
\]
where
\[
H_S
=
\sum_{a_S}
h_S^{a_S}
\bigotimes_{i\in S}O_{i,a_i}.
\]
Here \(O_{i,a_i}\) are local operators and \(h_S^{a_S}\) are components of an interaction coefficient tensor.

The **order** of the interaction is the maximum size of \(S\) for which \(H_S\neq 0\). A \(k\)-local Hamiltonian has interaction arity at most \(k\).

Given a bipartition \(A\sqcup B\), write
\[
H=H_A\otimes I_B+I_A\otimes H_B+H_{AB}.
\]
The term \(H_{AB}\) is the nonlocal interaction tensor across the cut.

**Proposition 5.2.**  
If \(H_{AB}=0\), then
\[
e^{-itH}=e^{-itH_A}\otimes e^{-itH_B}.
\]
Consequently, product states remain product states and entanglement cannot be generated.

*Proof.*  
The two summands commute, so the exponential factorizes. If
\[
\Psi(0)=\psi_A\otimes\psi_B,
\]
then
\[
\Psi(t)
=
(e^{-itH_A}\psi_A)\otimes(e^{-itH_B}\psi_B).
\]
Thus the interaction rank across the cut remains one. ∎

Therefore, nonzero nonlocal interaction tensors are necessary for dynamical entanglement generation.

---

### 5.4 Quantum channels as higher-order interactions

A quantum channel
\[
\mathcal E:\operatorname{End}(\mathcal H_{\mathrm{in}})
\to
\operatorname{End}(\mathcal H_{\mathrm{out}})
\]
can be represented in Kraus form:
\[
\mathcal E(X)=\sum_\mu K_\mu X K_\mu^\dagger.
\]
In components,
\[
\mathcal E^{b b'}{}_{a a'}
=
\sum_\mu
K_\mu^{b}{}_{a}
\overline{K}_\mu^{\,b'}{}_{a'}.
\]
Trace preservation is the contraction identity
\[
\boxed{
\sum_b \mathcal E^{b b}{}_{a a'}
=
\delta_{a a'}.
}
\]
Complete positivity is the statement that the tensor admits a Kraus decomposition.

A channel is therefore a higher-order interaction tensor mapping input contexts to output contexts. Composition of channels is contraction of their tensorial representations.

---

## 6. Multi-Agent Mathematics

UIA provides a natural language for games, strategic interaction, learning dynamics, and coalition formation.

### 6.1 Payoff tensors

Let \(N=\{1,\ldots,n\}\) be a set of agents. Agent \(i\) has a finite action set \(A_i\). Let
\[
V_i=\mathbb R^{A_i}
\]
be the vector space of mixed strategies. A mixed strategy is a probability vector
\[
p_i=(p_i^a)_{a\in A_i}\in \Delta(A_i)\subset V_i.
\]

The payoff to agent \(i\) is given by a payoff tensor
\[
P^{(i)}\in \bigotimes_{j=1}^n V_j^*.
\]
In components,
\[
P^{(i)}_{a_1\cdots a_n}
\]
is the payoff to agent \(i\) when the joint action profile is \((a_1,\ldots,a_n)\).

The expected payoff under mixed strategy profile \(p=(p_1,\ldots,p_n)\) is
\[
\boxed{
U_i(p)
=
P^{(i)}_{a_1\cdots a_n}
\prod_{j=1}^n p_j^{a_j}.
}
\]

Thus a game is a UIA whose distinguished interaction tensors are payoff tensors.

---

### 6.2 Marginal payoffs and Nash equilibria

The marginal payoff to agent \(i\) for action \(a\) is
\[
\boxed{
G_i^a(p)
=
\frac{\partial U_i}{\partial p_i^a}
=
P^{(i)}_{a a_{-i}}
\prod_{j\neq i}p_j^{a_j}.
}
\]

A mixed strategy profile \(p^*\) is a Nash equilibrium iff for every agent \(i\),
\[
p_i^*\in \arg\max_{p_i\in\Delta(A_i)}U_i(p_i,p_{-i}^*).
\]
Equivalently, there exist scalars \(\lambda_i\) such that
\[
\boxed{
G_i^a(p^*)\le \lambda_i
}
\]
for all actions \(a\), with equality whenever \(p_i^{*,a}>0\).

This is the standard Karush–Kuhn–Tucker condition written in interaction-tensor form.

---

### 6.3 Replicator dynamics as interaction flow

A natural learning dynamics is the replicator equation:
\[
\boxed{
\dot p_i^a
=
p_i^a\left(G_i^a(p)-U_i(p)\right).
}
\]
In UIA language, the vector field is obtained by contracting the payoff tensors with the current strategy tensors and subtracting the average payoff.

Fixed points of this flow include Nash equilibria, though not all fixed points need be Nash equilibria without additional support conditions.

---

### 6.4 Potential games and interaction cohomology

A game is an **exact potential game** if there exists a potential function
\[
\Phi:A_1\times\cdots\times A_n\to \mathbb R
\]
such that for every agent \(i\), every unilateral change \(a_i\to a_i'\), and every fixed \(a_{-i}\),
\[
P^{(i)}_{a_i a_{-i}}-P^{(i)}_{a_i' a_{-i}}
=
\Phi_{a_i a_{-i}}-\Phi_{a_i' a_{-i}}.
\]

In tensor language, the collection of payoff tensors defines a discrete one-form on the joint action graph. A potential exists iff this one-form is exact, i.e. its curl vanishes.

A local tensorial condition is the following. For every pair of agents \(i,j\), every pair of actions \(a_i,a_i'\) for \(i\), every pair \(a_j,a_j'\) for \(j\), and every fixed \(a_{-ij}\), one must have
\[
\boxed{
\begin{aligned}
&\left[
P^{(i)}_{a_i a_j a_{-ij}}
-
P^{(i)}_{a_i' a_j a_{-ij}}
\right]
-
\left[
P^{(i)}_{a_i a_j' a_{-ij}}
-
P^{(i)}_{a_i' a_j' a_{-ij}}
\right]
\\
&\quad=
\left[
P^{(j)}_{a_i a_j a_{-ij}}
-
P^{(j)}_{a_i a_j' a_{-ij}}
\right]
-
\left[
P^{(j)}_{a_i' a_j a_{-ij}}
-
P^{(j)}_{a_i' a_j' a_{-ij}}
\right].
\end{aligned}
}
\]

This is the vanishing of the interaction curl tensor. When it holds, a potential \(\Phi\) can be reconstructed by path-independent summation.

**Theorem 6.1.**  
A finite game is an exact potential game iff its interaction curl tensor vanishes.

This gives a cohomological interpretation of potential games: payoff tensors define a discrete interaction one-form, and potentials are primitives of closed interaction forms.

---

### 6.5 Coalitions and Möbius inversion

Let \(C\subseteq N\) be a coalition. A coalition value may be represented by a tensorial value function
\[
v(C),
\]
obtained by contracting the payoff tensors over the strategies of agents in \(C\) and fixing or marginalizing outside agents.

The **interaction index** of coalition \(C\) is obtained by Möbius inversion:
\[
\boxed{
\theta_C
=
\sum_{T\subseteq C}
(-1)^{|C|-|T|}
v(T).
}
\]
The original value is recovered as
\[
v(C)=\sum_{T\subseteq C}\theta_T.
\]

The Shapley value can be written as
\[
\boxed{
\phi_i
=
\sum_{C\subseteq N\setminus\{i\}}
\frac{|C|!(n-|C|-1)!}{n!}
\left(v(C\cup\{i\})-v(C)\right).
}
\]

In UIA, coalition formation is the decomposition of a global interaction tensor into sub-interactions indexed by subsets of agents.

---

## 7. Coarse-Graining, Effective Interactions, and Morphisms

### 7.1 Effective interaction tensors

Suppose a system has external variables \(x\) and internal variables \(y\). Let local interaction tensors be \(\{\mathcal I_\nu\}\). The effective interaction on the external variables is obtained by summing or integrating out the internal variables:
\[
\boxed{
\mathcal I^{\mathrm{eff}}(x)
=
\sum_y
\prod_\nu
\mathcal I_\nu(x_\nu,y_\nu).
}
\]
In tensor notation, this is a contraction over internal indices.

Because UIAs are contraction-closed, the effective tensor belongs to the same interaction algebra whenever the original tensors do. This gives an algebraic formulation of renormalization.

---

### 7.2 Interaction nullspace and separated quotient

If the separation axiom fails, define the interaction nullspace
\[
\mathcal N
=
\left\{
A\in V:
\mathcal I(A,B_2,\ldots,B_r)=0
\text{ for all }\mathcal I,\,B_2,\ldots,B_r
\right\}.
\]
Then the quotient
\[
\overline V=V/\mathcal N
\]
inherits a separated UIA structure. Thus every pre-UIA has a canonical separated quotient.

---

### 7.3 Morphisms of UIAs

Let
\[
\mathfrak A=(V,\langle\cdot,\cdot\rangle,\mathscr I),
\qquad
\mathfrak B=(W,\langle\cdot,\cdot\rangle,\mathscr J)
\]
be UIAs. A linear map
\[
F:V\to W
\]
is a **UIA morphism** if it preserves the relevant interaction tensors:
\[
\boxed{
\mathcal J(F(A_1),\ldots,F(A_r))
=
\mathcal I(A_1,\ldots,A_r)
}
\]
for corresponding distinguished tensors, and if it commutes with the pairing up to the desired notion of isometry or adjointness.

If \(F\) is surjective, it describes coarse-graining. If \(F\) is injective, it describes embedding. If \(F\) is an isomorphism, it describes equivalence of interaction algebras.

---

## 8. Synthesis

Universal Interaction Algebra reorganizes algebra around three primitive operations:

1. **Evaluation of interaction tensors:**
   \[
   \mathcal I(A_1,\ldots,A_r).
   \]
2. **Induction of operations by testing an output leg:**
   \[
   \langle \mu(A_1,\ldots,A_n),Z\rangle
   =
   \mathcal I(A_1,\ldots,A_n,Z).
   \]
3. **Composition by contraction:**
   \[
   (\mathcal I\bullet\mathcal J)_{i_1\cdots i_{r-1}j_1\cdots j_{s-1}}
   =
   I_{i_1\cdots i_{r-1}a}
   g^{ab}
   J_{j_1\cdots j_{s-1}b}.
   \]

From these primitives, one recovers:

- binary and multiary algebraic operations,
- associativity, commutativity, units, and Lie identities as tensor contraction identities,
- network energies, partition functions, and message-passing equations,
- quantum entanglement, locality, and channels,
- game-theoretic payoffs, equilibria, learning dynamics, and coalition values.

The essential conceptual inversion is:

\[
\boxed{
\text{Not } a*b \text{ first, but } \mathcal I(a,b,c) \text{ first.}
}
\]

The product \(a*b\) is only the projection of an interaction onto a chosen test leg. More generally, mathematical structure is the invariant content of a network of interactions under contraction and recontextualization.

---

## 9. Conclusion

Universal Interaction Algebra provides a unified tensorial foundation for mathematics in which interaction is primitive. Objects are recovered from their interaction profiles, operations are induced by test pairings, and algebraic laws are contraction identities. The framework is sufficiently general to encode universal algebra, yet sufficiently structured to yield concrete calculi for networks, quantum systems, and multi-agent dynamics.

The principal advantages of UIA are:

1. **Uniformity.** The same tensorial language treats algebraic operations, hypergraph interactions, quantum amplitudes, and strategic payoffs.
2. **Higher-order structure.** Multiway interactions are primitive, not reducible to pairwise operations.
3. **Compositional clarity.** Composition is contraction, matching the graphical calculus of tensor networks.
4. **Contextuality.** Objects are defined by their behavior under all contexts, in precise analogy with relational and categorical philosophies.
5. **Effective theory.** Coarse-graining and renormalization are natural consequences of contraction closure.

Future work includes: categorical formulations in terms of operads, props, and monoidal categories; homological invariants of interaction complexes; infinite-dimensional and measure-theoretic UIAs; learning of interaction tensors from data; and applications to quantum gravity, network control, and multi-agent mechanism design.

---

## References

1. S. Mac Lane, *Categories for the Working Mathematician*, Springer, 1998.  
2. R. Penrose, “Applications of negative dimensional tensors,” in *Combinatorial Mathematics and its Applications*, Academic Press, 1971.  
3. T. G. Kolda and B. W. Bader, “Tensor decompositions and applications,” *SIAM Review*, 51(3):455–500, 2009.  
4. F. Verstraete, V. Murg, and J. I. Cirac, “Matrix product states, projected entangled pair states, and variational renormalization group methods for quantum spin systems,” *Advances in Physics*, 57(2):143–224, 2008.  
5. M. A. Nielsen and I. L. Chuang, *Quantum Computation and Quantum Information*, Cambridge University Press, 2000.  
6. D. Monderer and L. S. Shapley, “Potential games,” *Games and Economic Behavior*, 14(1):124–143, 1996.
