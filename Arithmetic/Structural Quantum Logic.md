# Structural Quantum Logic

**Preprint**

---

## Abstract

Structural Quantum Logic (SQL) is a logical framework in which propositions, truth values, and inference rules are treated as geometric and algebraic structures rather than as static Boolean assignments. In SQL, logical operations are interpreted as transformations of structured spaces: orthogonal complementation is reflection in a Hilbert lattice, conjunction is intersection or sequential filtering, disjunction is closed linear span, tensor product is composition of independent structures, and implication arises through adjoint dynamics. Truth values are not merely elements of \(\{0,1\}\); they evolve inside state–effect spaces under physical or computational transformations. This paper develops a complete formal foundation for SQL: its syntax, algebraic semantics, categorical semantics, proof theory, dynamic truth calculus, and applications to quantum foundations, automated reasoning, formal verification, and computing. The central claim is that logic becomes more expressive when its truth values are allowed to inhabit structural spaces and evolve by structure-preserving maps.

---

## 1. Introduction

Classical logic is founded on the assumption that every proposition possesses a definite truth value in the two-element Boolean algebra
\[
\mathbf{2}=\{0,1\}.
\]
This assumption is adequate for deterministic classical systems but becomes inadequate for quantum systems, where propositions correspond to experimental possibilities such as “the spin along the \(z\)-axis is up.” Such propositions do not form a Boolean algebra; they form a non-distributive lattice of closed subspaces or projection operators on a Hilbert space.

The historical origin of this observation is the Birkhoff–von Neumann proposal that quantum logic is the lattice of closed subspaces of Hilbert space. SQL generalizes this idea in three directions.

1. **Structural semantics.** Logical connectives are interpreted as operations with intrinsic geometry: meet, join, orthogonal complement, tensor product, and adjoint transformations.

2. **Dynamic truth.** A truth value is not merely a scalar probability or Boolean bit. It is an evaluation of a proposition against a state inside a structural space, and it evolves when either the state, the proposition, or the ambient structure evolves.

3. **Resource-sensitive proof theory.** Quantum information cannot generally be copied or discarded without changing logical content. SQL therefore distinguishes classical structural rules from genuinely quantum resource rules.

The central objects of SQL are **structural spaces**. In their simplest Hilbert-space form, a structural space consists of:

\[
\mathscr{S}(\mathcal{H})
=
\bigl(
\mathcal{D}(\mathcal{H}),
\operatorname{Eff}(\mathcal{H}),
\operatorname{Chan}(\mathcal{H})
\bigr),
\]
where:

- \(\mathcal{D}(\mathcal{H})\) is the convex set of density operators, representing states;
- \(\operatorname{Eff}(\mathcal{H})\) is the effect algebra of positive operators \(0\le E\le I\), representing propositions or tests;
- \(\operatorname{Chan}(\mathcal{H})\) is the category of completely positive maps, representing dynamics, measurements, and computational processes.

The truth degree of a proposition \(E\) in a state \(\rho\) is the canonical pairing
\[
\tau_\rho(E)
=
\operatorname{Tr}(\rho E).
\]
This scalar is only the observable shadow of a richer structural truth value: the pair \((\rho,E)\), or more generally the whole orbit of such pairs under transformations.

SQL is therefore a logic of **structured truth**:

\[
\text{truth} \;\neq\; \{0,1\},
\qquad
\text{truth} \;\in\; \text{structural space}.
\]

The purpose of this paper is to develop SQL as a formal system suitable for quantum foundations, automated reasoning, formal verification, and quantum computing.

---

## 2. Preliminaries

Let \(\mathcal{H}\) be a finite-dimensional complex Hilbert space. Denote by \(\mathcal{B}(\mathcal{H})\) the algebra of bounded linear operators on \(\mathcal{H}\). In finite dimension, \(\mathcal{B}(\mathcal{H})\) is the full matrix algebra \(M_d(\mathbb{C})\), where \(d=\dim\mathcal{H}\).

### 2.1 States

A **state** is a positive trace-class operator \(\rho\) with unit trace:
\[
\rho\ge 0,
\qquad
\operatorname{Tr}(\rho)=1.
\]
The set of states is
\[
\mathcal{D}(\mathcal{H})
=
\{\rho\in \mathcal{B}(\mathcal{H}) : \rho\ge 0,\ \operatorname{Tr}(\rho)=1\}.
\]
Pure states are rank-one projections
\[
\rho_\psi = |\psi\rangle\langle\psi|,
\qquad
\|\psi\|=1.
\]

### 2.2 Effects and sharp propositions

An **effect** is a positive operator bounded above by the identity:
\[
\operatorname{Eff}(\mathcal{H})
=
\{E\in \mathcal{B}(\mathcal{H}) : 0\le E\le I\}.
\]
Effects represent unsharp propositions or probabilistic tests.

A **sharp proposition** is a projection:
\[
\operatorname{Proj}(\mathcal{H})
=
\{P\in\mathcal{B}(\mathcal{H}) : P=P^\dagger=P^2\}.
\]
Sharp propositions correspond to closed subspaces of \(\mathcal{H}\). If \(P\) is a projection, its range is
\[
\operatorname{ran}(P)
=
\{\psi\in\mathcal{H}:P\psi=\psi\}.
\]

The order on effects is the Löwner order:
\[
E\le F
\iff
F-E\ge 0.
\]
For projections, this order reduces to subspace inclusion:
\[
P\le Q
\iff
\operatorname{ran}(P)\subseteq \operatorname{ran}(Q).
\]

### 2.3 Channels and instruments

A **quantum channel** is a completely positive trace-preserving map
\[
\Phi:\mathcal{B}(\mathcal{H})\to \mathcal{B}(\mathcal{K}).
\]
In Kraus form,
\[
\Phi(\rho)
=
\sum_k K_k \rho K_k^\dagger,
\qquad
\sum_k K_k^\dagger K_k = I.
\]
Its Heisenberg dual is the unital completely positive map
\[
\Phi^\dagger(E)
=
\sum_k K_k^\dagger E K_k.
\]
The duality relation is
\[
\operatorname{Tr}(\Phi(\rho)E)
=
\operatorname{Tr}(\rho \Phi^\dagger(E)).
\]

A **test** or **instrument** may be trace-nonincreasing. For a projection \(P\), the Lüders filter is
\[
\mathcal{I}_P(\rho)
=
P\rho P.
\]
Its dual is
\[
\mathcal{I}_P^\dagger(E)
=
P E P.
\]

### 2.4 Tensor notation

For composite systems we write
\[
\mathcal{H}_{AB}
=
\mathcal{H}_A\otimes \mathcal{H}_B.
\]
In index notation,
\[
\rho
=
\rho^{i_A i_B}_{j_A j_B}
\,
|i_A\rangle\langle j_A|
\otimes
|i_B\rangle\langle j_B|,
\]
and an effect is
\[
E
=
E^{j_A j_B}_{i_A i_B}
\,
|i_A\rangle\langle j_A|
\otimes
|i_B\rangle\langle j_B|.
\]
The truth pairing is the contraction
\[
\tau_\rho(E)
=
\rho^{i_A i_B}_{j_A j_B}
E^{j_A j_B}_{i_A i_B}.
\]

---

## 3. Syntax and Semantics of SQL

SQL is defined in layers. The **sharp static fragment** interprets propositions as projections. The **effect fragment** interprets propositions as effects. The **dynamic fragment** adds transformations acting on propositions. The **tensor fragment** describes composite systems and resource structure.

### 3.1 Language

Let \(\mathsf{Prop}\) be a set of atomic propositions. The SQL language is generated by the grammar
\[
\varphi
::=
p
\mid
\neg \varphi
\mid
\varphi\wedge\psi
\mid
\varphi\vee\psi
\mid
\varphi\Rightarrow\psi
\mid
\varphi\otimes\psi
\mid
[\Phi]\varphi,
\]
where:

- \(p\in\mathsf{Prop}\);
- \(\neg\) is orthocomplementation;
- \(\wedge\) is conjunction;
- \(\vee\) is disjunction;
- \(\Rightarrow\) is implication;
- \(\otimes\) is tensor conjunction;
- \([\Phi]\) is a dynamic modality associated with a completely positive map \(\Phi\).

In the sharp fragment, formulas are interpreted as projections. In the effect fragment, formulas are interpreted as effects. In the dynamic fragment, formulas are pulled back along transformations.

### 3.2 Sharp semantic clauses

Let \(\mathcal{H}\) be fixed. A sharp interpretation is a map
\[
\llbracket -\rrbracket : \mathsf{Form}\to \operatorname{Proj}(\mathcal{H})
\]
satisfying:
\[
\llbracket \neg\varphi\rrbracket
=
I-\llbracket\varphi\rrbracket,
\]
\[
\llbracket \varphi\wedge\psi\rrbracket
=
\llbracket\varphi\rrbracket
\wedge
\llbracket\psi\rrbracket,
\]
\[
\llbracket \varphi\vee\psi\rrbracket
=
\llbracket\varphi\rrbracket
\vee
\llbracket\psi\rrbracket,
\]
where \(\wedge\) and \(\vee\) are the meet and join of the projection lattice.

For projections \(P,Q\),
\[
\operatorname{ran}(P\wedge Q)
=
\operatorname{ran}(P)\cap \operatorname{ran}(Q),
\]
and
\[
\operatorname{ran}(P\vee Q)
=
\overline{\operatorname{ran}(P)+\operatorname{ran}(Q)}.
\]
In finite dimension the closure is redundant.

The implication is the Sasaki hook:
\[
P\Rightarrow Q
:=
P^\perp \vee (P\wedge Q),
\]
where
\[
P^\perp = I-P.
\]

### 3.3 Effect semantic clauses

In the effect fragment, an interpretation is a map
\[
\llbracket -\rrbracket : \mathsf{Form}\to \operatorname{Eff}(\mathcal{H})
\]
with
\[
\llbracket \neg\varphi\rrbracket
=
I-\llbracket\varphi\rrbracket.
\]
For commuting effects, conjunction may be interpreted by the product:
\[
\llbracket\varphi\wedge\psi\rrbracket
=
\llbracket\varphi\rrbracket
\llbracket\psi\rrbracket
\quad
\text{if }
[\llbracket\varphi\rrbracket,\llbracket\psi\rrbracket]=0.
\]
In general, SQL distinguishes several conjunctions:

1. **Static sharp conjunction**:
   \[
   P\wedge Q.
   \]

2. **Tensor conjunction**:
   \[
   E\otimes F.
   \]

3. **Sequential test conjunction**:
   \[
   P;Q := \mathcal{I}_P^\dagger(Q)=PQP.
   \]

The sequential conjunction expresses the proposition “\(Q\) holds after a successful test of \(P\).”

For a state \(\rho\),
\[
\operatorname{Tr}(\rho\, PQP)
=
\operatorname{Tr}(P\rho P\, Q),
\]
which is the unnormalized probability that \(Q\) holds after the filter \(P\).

### 3.4 Dynamic modality

Let \(\Phi\) be a completely positive map. The dynamic modality is interpreted by Heisenberg pullback:
\[
\llbracket [\Phi]\varphi\rrbracket
=
\Phi^\dagger(\llbracket\varphi\rrbracket).
\]
Thus the truth degree satisfies
\[
\tau_\rho([\Phi]\varphi)
=
\operatorname{Tr}
\bigl(
\rho\,\Phi^\dagger(\llbracket\varphi\rrbracket)
\bigr)
=
\operatorname{Tr}
\bigl(
\Phi(\rho)\,\llbracket\varphi\rrbracket
\bigr).
\]
Therefore:
\[
\boxed{
\tau_\rho([\Phi]\varphi)
=
\tau_{\Phi(\rho)}(\varphi)
}
\]
This equation is the basic law of truth evolution in SQL.

### 3.5 Tensor semantics

For systems \(\mathcal{H}_A,\mathcal{H}_B\),
\[
\llbracket \varphi\otimes\psi\rrbracket
=
\llbracket\varphi\rrbracket_A
\otimes
\llbracket\psi\rrbracket_B.
\]
More general propositions on \(\mathcal{H}_A\otimes\mathcal{H}_B\) need not factorize. Entangled propositions are effects on the tensor product space that cannot be written as a simple tensor.

For a separable state
\[
\rho_{AB}
=
\rho_A\otimes\rho_B,
\]
we have
\[
\tau_{\rho_{AB}}(\varphi\otimes\psi)
=
\tau_{\rho_A}(\varphi)
\,
\tau_{\rho_B}(\psi).
\]
For entangled states this factorization fails.

### 3.6 Entailment

Semantic entailment is defined by the Löwner order.

For effects \(E,F\),
\[
E\models F
\iff
E\le F.
\]
For sharp propositions,
\[
P\models Q
\iff
\operatorname{ran}(P)\subseteq \operatorname{ran}(Q).
\]
A sequent
\[
\varphi_1,\dots,\varphi_n \vdash \psi
\]
is valid in the sharp additive fragment when
\[
\llbracket\varphi_1\rrbracket
\wedge
\cdots
\wedge
\llbracket\varphi_n\rrbracket
\le
\llbracket\psi\rrbracket.
\]
In the tensor fragment, contexts are interpreted tensorially rather than by meet.

---

## 4. Algebraic Structure of Sharp SQL

The sharp fragment of SQL is based on the projection lattice
\[
\mathcal{L}(\mathcal{H})
=
\operatorname{Proj}(\mathcal{H}).
\]

### 4.1 Orthomodular lattice

The projection lattice is a complete orthomodular lattice.

It has:

- bottom element \(0\);
- top element \(I\);
- meet \(P\wedge Q\);
- join \(P\vee Q\);
- orthocomplement \(P^\perp=I-P\).

The orthocomplement satisfies:
\[
P\wedge P^\perp = 0,
\qquad
P\vee P^\perp = I,
\qquad
(P^\perp)^\perp=P.
\]

The lattice is not generally distributive. Instead, it satisfies the orthomodular law.

### 4.2 Orthomodular law

**Theorem 4.1.**  
If \(P,Q\in\operatorname{Proj}(\mathcal{H})\) and \(P\le Q\), then
\[
Q
=
P\vee(P^\perp\wedge Q).
\]

**Proof.**  
The inequality \(P\le Q\) means
\[
\operatorname{ran}(P)\subseteq \operatorname{ran}(Q).
\]
Let \(q\in \operatorname{ran}(Q)\). Since \(\operatorname{ran}(P)\subseteq \operatorname{ran}(Q)\), we may decompose \(q\) orthogonally as
\[
q = p + r,
\]
where
\[
p = Pq\in \operatorname{ran}(P),
\qquad
r = q-p.
\]
Because \(p\in\operatorname{ran}(Q)\) and \(q\in\operatorname{ran}(Q)\), we have
\[
r = q-p \in \operatorname{ran}(Q).
\]
Also,
\[
Pr = P(q-Pq)=Pq-P^2q=Pq-Pq=0,
\]
so \(r\in \operatorname{ran}(P)^\perp\). Hence
\[
r\in \operatorname{ran}(Q)\cap \operatorname{ran}(P)^\perp
=
\operatorname{ran}(P^\perp\wedge Q).
\]
Thus
\[
\operatorname{ran}(Q)
=
\operatorname{ran}(P)
+
\operatorname{ran}(P^\perp\wedge Q).
\]
The sum is orthogonal, so the corresponding projection is the join:
\[
Q
=
P\vee(P^\perp\wedge Q).
\]
\(\square\)

This theorem is the structural replacement for the Boolean decomposition law.

### 4.3 Failure of distributivity

In classical logic, the distributive law holds:
\[
A\wedge(B\vee C)
=
(A\wedge B)\vee(A\wedge C).
\]
In SQL, this law fails in general.

Let \(\mathcal{H}=\mathbb{C}^2\). Define
\[
P_{z+}
=
|0\rangle\langle 0|
=
\begin{pmatrix}
1&0\\
0&0
\end{pmatrix},
\]
\[
P_{z-}
=
|1\rangle\langle 1|
=
\begin{pmatrix}
0&0\\
0&1
\end{pmatrix},
\]
and
\[
P_{x+}
=
|+\rangle\langle +|
=
\frac12
\begin{pmatrix}
1&1\\
1&1
\end{pmatrix},
\]
where
\[
|+\rangle
=
\frac{|0\rangle+|1\rangle}{\sqrt2}.
\]

Since
\[
P_{z+}\vee P_{z-}=I,
\]
we have
\[
P_{x+}\wedge(P_{z+}\vee P_{z-})
=
P_{x+}\wedge I
=
P_{x+}.
\]
But the one-dimensional subspaces corresponding to \(P_{x+}\), \(P_{z+}\), and \(P_{z-}\) are distinct lines in \(\mathbb{C}^2\). Therefore
\[
P_{x+}\wedge P_{z+}=0,
\qquad
P_{x+}\wedge P_{z-}=0.
\]
Hence
\[
(P_{x+}\wedge P_{z+})
\vee
(P_{x+}\wedge P_{z-})
=
0\vee 0
=
0.
\]
Thus
\[
P_{x+}\wedge(P_{z+}\vee P_{z-})
\neq
(P_{x+}\wedge P_{z+})
\vee
(P_{x+}\wedge P_{z-}).
\]

This non-distributivity is not a defect. It is the algebraic signature of quantum incompatibility.

### 4.4 Classical fragments

Let \(\mathcal{A}\subseteq\mathcal{B}(\mathcal{H})\) be a commutative \(C^*\)-subalgebra. By the spectral theorem,
\[
\mathcal{A}\cong C(X)
\]
for some finite set \(X\). The projections of \(\mathcal{A}\) are characteristic functions:
\[
\operatorname{Proj}(\mathcal{A})
\cong
\{\chi_S:S\subseteq X\}.
\]
Therefore \(\operatorname{Proj}(\mathcal{A})\) is a Boolean algebra.

**Theorem 4.2.**  
Inside any commutative context, SQL reduces to classical Boolean logic.

**Proof.**  
In a commutative subalgebra, projections correspond to subsets of a finite set. Meet is intersection, join is union, and orthocomplement is set-theoretic complement. These operations satisfy distributivity, excluded middle, and non-contradiction. Hence the sharp fragment restricted to a commutative context is Boolean. \(\square\)

SQL therefore contains classical logic as a local fragment.

---

## 5. Dynamic Truth Calculus

SQL treats truth as evolving under transformations.

### 5.1 Truth degrees

Given a state \(\rho\) and an effect \(E\), the truth degree is
\[
\tau_\rho(E)
=
\operatorname{Tr}(\rho E).
\]
This number lies in \([0,1]\). For a projection \(P\),
\[
\tau_\rho(P)
\]
is the probability that the sharp proposition \(P\) is verified.

For a pure state \(|\psi\rangle\),
\[
\tau_\psi(P)
=
\langle\psi|P|\psi\rangle.
\]

### 5.2 Evolution by channels

Let \(\Phi\) be a channel. If the state evolves as
\[
\rho\mapsto \Phi(\rho),
\]
then the truth degree of a fixed proposition \(E\) becomes
\[
\tau_{\Phi(\rho)}(E)
=
\operatorname{Tr}(\Phi(\rho)E)
=
\operatorname{Tr}(\rho\Phi^\dagger(E)).
\]
Equivalently, the proposition evolves in the Heisenberg picture:
\[
E\mapsto \Phi^\dagger(E).
\]
Thus SQL identifies logical transformation with adjoint action.

### 5.3 Unitary evolution

Let
\[
U(t)=e^{-iHt}
\]
be a unitary evolution generated by a Hermitian Hamiltonian \(H\). The Schrödinger evolution of the state is
\[
\rho(t)
=
U(t)\rho U(t)^\dagger.
\]
The Heisenberg evolution of an effect is
\[
E(t)
=
U(t) E U(t)^\dagger.
\]
Differentiating,
\[
\frac{d\rho}{dt}
=
-i[H,\rho],
\]
and
\[
\frac{dE}{dt}
=
i[H,E].
\]
The truth degree is
\[
\theta(t)
=
\operatorname{Tr}(\rho(t)E(t)).
\]
Then
\[
\frac{d\theta}{dt}
=
\operatorname{Tr}
\left(
\frac{d\rho}{dt}E
+
\rho\frac{dE}{dt}
\right)
\]
\[
=
-i\operatorname{Tr}([H,\rho]E)
+
i\operatorname{Tr}(\rho[H,E]).
\]
Using cyclicity of trace,
\[
\operatorname{Tr}([H,\rho]E)
=
\operatorname{Tr}(H\rho E)-\operatorname{Tr}(\rho H E)
=
\operatorname{Tr}(\rho E H)-\operatorname{Tr}(\rho H E)
=
\operatorname{Tr}(\rho[E,H]).
\]
Similarly,
\[
\operatorname{Tr}(\rho[H,E])
=
-\operatorname{Tr}(\rho[E,H]).
\]
Therefore
\[
\frac{d\theta}{dt}=0.
\]
Hence closed co-evolution of state and proposition preserves truth degree.

This is the SQL analogue of conservation of logical content under reversible dynamics.

### 5.4 Measurement update

Let \(\{P_k\}_k\) be a projective measurement with
\[
\sum_k P_k=I,
\qquad
P_kP_j=\delta_{kj}P_k.
\]
The non-selective measurement channel is
\[
\mathcal{M}(\rho)
=
\sum_k P_k\rho P_k.
\]
The truth value of an effect \(E\) after measurement is
\[
\tau_{\mathcal{M}(\rho)}(E)
=
\operatorname{Tr}
\left(
\sum_k P_k\rho P_k E
\right)
=
\sum_k
\operatorname{Tr}
\left(
\rho P_k E P_k
\right).
\]

If outcome \(k\) is selected, the normalized post-measurement state is
\[
\rho_k
=
\frac{P_k\rho P_k}{\operatorname{Tr}(\rho P_k)}.
\]
The truth degree of \(E\) after the outcome is
\[
\tau_{\rho_k}(E)
=
\frac{\operatorname{Tr}(\rho P_k E P_k)}
{\operatorname{Tr}(\rho P_k)}.
\]
For \(E=P_k\), this gives
\[
\tau_{\rho_k}(P_k)=1.
\]
Measurement is therefore a logical actualization operation.

### 5.5 Truth trajectories

A **truth trajectory** is a family
\[
\Theta(t)
=
(\rho(t),E(t))
\]
together with its evaluation
\[
\theta(t)
=
\operatorname{Tr}(\rho(t)E(t)).
\]
In SQL, the primary object is not the scalar \(\theta(t)\), but the structured pair \((\rho(t),E(t))\) and the transformation law that generates it.

A logical proposition may evolve because:

1. the state evolves;
2. the proposition is pulled back by a channel;
3. the ambient system is transformed;
4. the context changes.

Thus truth becomes a path in a state–effect bundle.

---

## 6. Tensor Structure and Entanglement

The tensor product is essential to SQL because quantum systems compose non-classically.

### 6.1 Local propositions

For propositions \(P_A\in\operatorname{Proj}(\mathcal{H}_A)\) and \(Q_B\in\operatorname{Proj}(\mathcal{H}_B)\),
\[
P_A\otimes Q_B
\]
is the proposition that \(P_A\) holds locally and \(Q_B\) holds locally.

For a product state
\[
\rho_{AB}=\rho_A\otimes\rho_B,
\]
we have
\[
\tau_{\rho_{AB}}(P_A\otimes Q_B)
=
\tau_{\rho_A}(P_A)
\tau_{\rho_B}(Q_B).
\]

### 6.2 Entangled propositions

Not every proposition on \(\mathcal{H}_A\otimes\mathcal{H}_B\) is local. An entangled proposition may be a projection onto an entangled subspace.

For example, the Bell state
\[
|\Phi^+\rangle
=
\frac{|00\rangle+|11\rangle}{\sqrt2}
\]
defines the rank-one projection
\[
P_{\Phi^+}
=
|\Phi^+\rangle\langle\Phi^+|.
\]
The proposition
\[
P_{\Phi^+}
\]
is irreducibly structural: it concerns the composite system as a whole.

For the local proposition
\[
P_{z+}\otimes I,
\]
we compute
\[
\tau_{\Phi^+}(P_{z+}\otimes I)
=
\langle\Phi^+|P_{z+}\otimes I|\Phi^+\rangle
=
\frac12.
\]
Similarly,
\[
\tau_{\Phi^+}(P_{z+}\otimes P_{z+})
=
\frac12,
\]
and
\[
\tau_{\Phi^+}(P_{z-}\otimes P_{z-})
=
\frac12.
\]
Thus the Bell state satisfies perfect correlation in the \(z\)-basis even though neither subsystem possesses a definite local \(z\)-value.

This demonstrates the central SQL principle: truth can be global rather than reducible to local assignments.

---

## 7. Contextuality and the Impossibility of Global Boolean Truth

A **context** is a commutative subalgebra of observables. Equivalently, it is a set of mutually compatible propositions.

SQL admits local Boolean valuations inside contexts but generally denies the existence of a global Boolean valuation.

### 7.1 Kochen–Specker obstruction

For \(\dim\mathcal{H}\ge 3\), there is no function
\[
\nu:\operatorname{Proj}(\mathcal{H})\to\{0,1\}
\]
such that:

1. \(\nu(I)=1\);
2. \(\nu(P^\perp)=1-\nu(P)\);
3. for every family of mutually orthogonal projections \(\{P_i\}\),
   \[
   \nu\left(\sum_i P_i\right)
   =
   \sum_i \nu(P_i).
   \]

This is the Kochen–Specker theorem. It shows that quantum propositions cannot be assigned global classical truth values while preserving functional structure.

### 7.2 Peres–Mermin square

A compact demonstration of contextuality occurs in a two-qubit system. Let
\[
X=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix},
\quad
Y=
\begin{pmatrix}
0&-i\\
i&0
\end{pmatrix},
\quad
Z=
\begin{pmatrix}
1&0\\
0&-1
\end{pmatrix}.
\]
Consider the following nine observables:

\[
\begin{array}{ccc}
X\otimes I & I\otimes X & X\otimes X\\
I\otimes Y & Y\otimes I & Y\otimes Y\\
X\otimes Y & Y\otimes X & Z\otimes Z
\end{array}
\]

Each row consists of commuting observables, and each column consists of commuting observables. Their products are:

\[
\begin{aligned}
(X\otimes I)(I\otimes X)(X\otimes X)&=I,\\
(I\otimes Y)(Y\otimes I)(Y\otimes Y)&=I,\\
(X\otimes Y)(Y\otimes X)(Z\otimes Z)&=I,
\end{aligned}
\]
for the rows, and
\[
\begin{aligned}
(X\otimes I)(I\otimes Y)(X\otimes Y)&=I,\\
(I\otimes X)(Y\otimes I)(Y\otimes X)&=I,\\
(X\otimes X)(Y\otimes Y)(Z\otimes Z)&=-I,
\end{aligned}
\]
for the columns.

Suppose there were a noncontextual truth assignment
\[
v(O)\in\{+1,-1\}
\]
to each observable \(O\), preserving the product relations in every context. Then the product of the three row values would be \(+1\), while the product of the three column values would be \(-1\). But both products multiply the same nine assigned values, giving a contradiction:
\[
+1=-1.
\]

Therefore no global classical valuation exists.

SQL interprets this as follows: truth is local to contexts and must be transported between contexts by structure-preserving maps. There is no single Boolean universe containing all quantum truth values.

---

## 8. Proof Theory of SQL

SQL admits several proof systems. We present a sharp algebraic calculus, a dynamic calculus, and a tensor resource calculus.

### 8.1 Sharp sequent calculus

A sharp sequent has the form
\[
\Gamma\vdash A,
\]
where \(\Gamma\) is a finite set of formulas and \(A\) is a formula. Semantically,
\[
\Gamma\vdash A
\]
is valid if
\[
\bigwedge_{B\in\Gamma}\llbracket B\rrbracket
\le
\llbracket A\rrbracket.
\]

The basic rules are:

#### Identity and cut

\[
\frac{}{A\vdash A}
\ \mathrm{Id}
\]

\[
\frac{\Gamma\vdash A \qquad \Delta,A\vdash B}
{\Gamma,\Delta\vdash B}
\ \mathrm{Cut}
\]

#### Conjunction

\[
\frac{\Gamma\vdash A \qquad \Gamma\vdash B}
{\Gamma\vdash A\wedge B}
\ \wedge R
\]

\[
\frac{\Gamma,A\vdash C}
{\Gamma,A\wedge B\vdash C}
\ \wedge L_1
\qquad
\frac{\Gamma,B\vdash C}
{\Gamma,A\wedge B\vdash C}
\ \wedge L_2
\]

#### Disjunction

\[
\frac{\Gamma\vdash A}
{\Gamma\vdash A\vee B}
\ \vee R_1
\qquad
\frac{\Gamma\vdash B}
{\Gamma\vdash A\vee B}
\ \vee R_2
\]

\[
\frac{\Gamma,A\vdash C \qquad \Gamma,B\vdash C}
{\Gamma,A\vee B\vdash C}
\ \vee L
\]

#### Orthocomplement

\[
\frac{\Gamma\vdash A}
{\Gamma,\neg A\vdash 0}
\]

\[
\frac{}{\vdash A\vee \neg A}
\]

\[
\frac{}{\neg\neg A\vdash A}
\qquad
\frac{}{A\vdash \neg\neg A}
\]

#### Orthomodularity

If \(A\vdash B\) is derivable, then one may derive
\[
B\vdash A\vee(\neg A\wedge B)
\]
and
\[
A\vee(\neg A\wedge B)\vdash B.
\]

This rule encodes the orthomodular decomposition theorem.

### 8.2 Soundness

**Theorem 8.1.**  
If \(\Gamma\vdash A\) is derivable in the sharp sequent calculus, then
\[
\bigwedge_{B\in\Gamma}\llbracket B\rrbracket
\le
\llbracket A\rrbracket.
\]

**Proof.**  
By induction on derivations.

- Identity is reflexivity of \(\le\).
- Cut is transitivity of \(\le\).
- The \(\wedge\)-rules express the universal property of meet.
- The \(\vee\)-rules express the universal property of join.
- Orthocomplement rules follow from \(P\wedge P^\perp=0\) and \(P\vee P^\perp=I\).
- The orthomodularity rule is sound by Theorem 4.1.

Thus every derivable sequent is semantically valid. \(\square\)

### 8.3 Dynamic proof rules

Dynamic modalities obey monotonicity and composition.

#### Monotonicity

\[
\frac{A\vdash B}{[\Phi]A\vdash [\Phi]B}
\]

This is sound because \(\Phi^\dagger\) is positive.

#### Identity

For the identity channel \(I\),
\[
[I]A \dashv\vdash A.
\]

#### Composition

Because pullbacks are contravariant,
\[
[\Phi][\Psi]A
\dashv\vdash
[\Psi\circ\Phi]A.
\]
Indeed,
\[
[\Phi][\Psi]A
\]
is interpreted as
\[
\Phi^\dagger(\Psi^\dagger(\llbracket A\rrbracket))
=
(\Psi\circ\Phi)^\dagger(\llbracket A\rrbracket).
\]

### 8.4 Tensor proof theory

The tensor fragment is resource-sensitive. A tensor sequent
\[
\Gamma\vdash A
\]
treats \(\Gamma\) as a multiset of resources.

#### Tensor right

\[
\frac{\Gamma\vdash A \qquad \Delta\vdash B}
{\Gamma,\Delta\vdash A\otimes B}
\]

#### Tensor left

\[
\frac{\Gamma,A,B\vdash C}
{\Gamma,A\otimes B\vdash C}
\]

#### Unit

The tensor unit \(1\) represents the trivial system.

\[
\frac{}{\cdot\vdash 1}
\]

### 8.5 Structural rules and no-cloning

In classical logic, contraction is valid:
\[
A\vdash A\wedge A.
\]
In tensor SQL, the corresponding quantum rule would be
\[
A\vdash A\otimes A.
\]
This is not valid for arbitrary quantum propositions.

The reason is no-cloning. Suppose there were a universal copying operation
\[
\Delta:\mathcal{H}\to\mathcal{H}\otimes\mathcal{H}
\]
such that for an orthonormal basis \(\{|0\rangle,|1\rangle\}\),
\[
\Delta|0\rangle=|0\rangle\otimes|0\rangle,
\qquad
\Delta|1\rangle=|1\rangle\otimes|1\rangle.
\]
By linearity,
\[
\Delta\left(\frac{|0\rangle+|1\rangle}{\sqrt2}\right)
=
\frac{|00\rangle+|11\rangle}{\sqrt2}.
\]
But a true copier would have to produce
\[
\frac{|0\rangle+|1\rangle}{\sqrt2}
\otimes
\frac{|0\rangle+|1\rangle}{\sqrt2}
=
\frac{|00\rangle+|01\rangle+|10\rangle+|11\rangle}{2}.
\]
These vectors are not equal. Therefore universal copying is impossible.

SQL internalizes this fact at the proof-theoretic level: contraction is valid only in classical contexts, i.e. in commutative subalgebras where a preferred basis exists and copying is legitimate.

---

## 9. Logical Geometry and Incompatibility

SQL treats logical operations as geometric operations.

### 9.1 Negation as orthogonal reflection

Negation maps a subspace to its orthogonal complement:
\[
\neg P = P^\perp.
\]
Geometrically, this is reflection through the origin into the orthogonal space.

### 9.2 Conjunction as intersection

For sharp propositions,
\[
P\wedge Q
\]
is projection onto
\[
\operatorname{ran}(P)\cap \operatorname{ran}(Q).
\]
Thus conjunction is geometric intersection.

### 9.3 Disjunction as span

The disjunction
\[
P\vee Q
\]
is projection onto
\[
\operatorname{ran}(P)+\operatorname{ran}(Q).
\]
Thus disjunction is linear span.

### 9.4 Tensor as Segre-type composition

The tensor proposition
\[
P\otimes Q
\]
corresponds to the tensor product of subspaces:
\[
\operatorname{ran}(P\otimes Q)
=
\operatorname{ran}(P)\otimes \operatorname{ran}(Q).
\]
This is the logical operation corresponding to independent composition.

### 9.5 Incompatibility and uncertainty

Two propositions \(E,F\) are compatible if
\[
[E,F]=EF-FE=0.
\]
If they are incompatible, they cannot be simultaneously sharp.

For self-adjoint operators \(A,B\), define variances in state \(\rho\):
\[
(\Delta A)_\rho^2
=
\operatorname{Tr}(\rho A^2)
-
\operatorname{Tr}(\rho A)^2,
\]
\[
(\Delta B)_\rho^2
=
\operatorname{Tr}(\rho B^2)
-
\operatorname{Tr}(\rho B)^2.
\]
The Robertson uncertainty relation gives
\[
\Delta A\,\Delta B
\ge
\frac12
\left|
\operatorname{Tr}(\rho[A,B])
\right|.
\]
For projections \(P,Q\), nonzero commutator implies that no state can make both \(P\) and \(Q\) simultaneously sharp unless the state lies in a common invariant subspace where they commute.

Thus logical incompatibility is expressed geometrically by noncommutativity and quantitatively by uncertainty relations.

---

## 10. Applications

SQL is not merely a foundational reconstruction. It has concrete applications.

---

## 10.1 Quantum Foundations

SQL clarifies several foundational issues.

### 10.1.1 Measurement

Measurement is not a mysterious collapse of truth but an update of the structural truth pair \((\rho,P)\). If a proposition \(P\) is verified, the state updates by the Lüders rule:
\[
\rho\mapsto
\frac{P\rho P}{\operatorname{Tr}(\rho P)}.
\]
The proposition becomes actual:
\[
\tau_{\rho'}(P)=1.
\]

### 10.1.2 Contextuality

Contextuality is the failure of global Boolean truth. SQL accepts local truth valuations and treats transitions between contexts as morphisms.

### 10.1.3 Entanglement

Entangled propositions show that truth may be irreducibly global. SQL’s tensor semantics provides a natural logical language for this phenomenon.

---

## 10.2 Automated Reasoning

SQL supports automated reasoning about quantum systems.

### 10.2.1 Inequality checking

Many SQL entailments reduce to operator inequalities:
\[
E\le F
\iff
F-E\ge 0.
\]
For finite-dimensional systems, these are semidefinite constraints.

For example, to verify
\[
P\le Q,
\]
one checks whether \(Q-P\) is positive semidefinite.

### 10.2.2 Semidefinite programming

Effects and channels can be represented by positive semidefinite matrices. A channel \(\Phi\) can be represented by its Choi matrix
\[
J_\Phi
=
\sum_{i,j}
|i\rangle\langle j|
\otimes
\Phi(|i\rangle\langle j|).
\]
Complete positivity is
\[
J_\Phi\ge 0,
\]
and trace preservation is
\[
\operatorname{Tr}_{\mathcal{K}}(J_\Phi)=I.
\]
Thus many SQL verification conditions become semidefinite programs.

### 10.2.3 Proof search

A SQL automated theorem prover can operate as follows:

1. Parse formulas into effect or projection expressions.
2. Normalize using orthomodular identities.
3. Translate entailments into matrix inequalities.
4. Use SDP solvers or algebraic decision procedures.
5. Extract countermodels when entailment fails.
6. Produce proof certificates in the SQL sequent calculus.

For fixed finite dimension, many problems can be encoded in the first-order theory of real closed fields, though computational complexity may be high.

---

## 10.3 Formal Verification

SQL provides a natural foundation for verifying quantum programs and protocols.

### 10.3.1 Quantum Hoare logic

Let a quantum command \(C\) be interpreted by a channel \(\Phi_C\). Let \(P,Q\) be effect-valued assertions.

A Hoare triple
\[
\{P\}\ C\ \{Q\}
\]
is valid if every state satisfying \(P\) is transformed into a state satisfying \(Q\).

The weakest precondition is
\[
\operatorname{wp}(C,Q)
=
\Phi_C^\dagger(Q).
\]
Then
\[
\{P\}\ C\ \{Q\}
\]
is valid exactly when
\[
P\le \Phi_C^\dagger(Q).
\]

**Proof.**  
For all states \(\rho\),
\[
\tau_{\Phi_C(\rho)}(Q)
=
\operatorname{Tr}(\Phi_C(\rho)Q)
=
\operatorname{Tr}(\rho\Phi_C^\dagger(Q)).
\]
Thus \(P\) guarantees \(Q\) after execution iff
\[
\operatorname{Tr}(\rho P)
\le
\operatorname{Tr}(\rho\Phi_C^\dagger(Q))
\]
for all \(\rho\), which is equivalent to
\[
P\le \Phi_C^\dagger(Q).
\]
\(\square\)

### 10.3.2 Example: Pauli \(X\) gate

Let
\[
X=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}.
\]
The channel is
\[
\Phi_X(\rho)=X\rho X.
\]
Let
\[
P_{z+}=|0\rangle\langle 0|,
\qquad
P_{z-}=|1\rangle\langle 1|.
\]
We verify
\[
\{P_{z+}\}\ X\ \{P_{z-}\}.
\]
The weakest precondition is
\[
\Phi_X^\dagger(P_{z-})
=
X P_{z-} X
=
P_{z+}.
\]
Therefore
\[
P_{z+}\le P_{z+},
\]
so the specification is valid.

### 10.3.3 Example: measurement destroys coherence

Let \(\mathcal{M}_Z\) be the non-selective \(Z\)-measurement:
\[
\mathcal{M}_Z(\rho)
=
P_{z+}\rho P_{z+}
+
P_{z-}\rho P_{z-}.
\]
Let
\[
P_{x+}
=
|+\rangle\langle +|.
\]
Then
\[
\operatorname{wp}(\mathcal{M}_Z,P_{x+})
=
P_{z+}P_{x+}P_{z+}
+
P_{z-}P_{x+}P_{z-}.
\]
Since
\[
P_{z+}P_{x+}P_{z+}
=
\frac12 P_{z+},
\]
and
\[
P_{z-}P_{x+}P_{z-}
=
\frac12 P_{z-},
\]
we obtain
\[
\operatorname{wp}(\mathcal{M}_Z,P_{x+})
=
\frac12 I.
\]
Thus
\[
\{P_{z+}\}\ \mathcal{M}_Z\ \{P_{x+}\}
\]
is valid only if
\[
P_{z+}\le \frac12 I,
\]
which is false. Therefore a \(Z\)-measurement does not preserve \(X\)-polarization. This is a simple SQL verification of measurement disturbance.

---

## 10.4 Computing

SQL has direct relevance to quantum computing.

### 10.4.1 Type systems for quantum programs

Propositions may serve as types or resource annotations. The tensor connective \(\otimes\) describes independent quantum resources. The failure of contraction encodes no-cloning.

A typing judgement
\[
x:A,\ y:B \vdash t:A\otimes B
\]
expresses that a program combines two resources without duplicating them.

### 10.4.2 Proofs as circuits

Under a Curry–Howard-style correspondence, SQL proofs may be interpreted as quantum circuits or more general completely positive maps.

- Tensor introduction corresponds to preparing composite systems.
- Tensor elimination corresponds to consuming composite resources.
- Dynamic modalities correspond to circuit fragments.
- Cut elimination corresponds to circuit normalization or optimization.

### 10.4.3 Tensor-network compilation

Because SQL formulas may be tensorial, proof normalization can be compiled into tensor-network contractions. This provides a logical semantics for optimizing quantum circuits and tensor-network algorithms.

### 10.4.4 Verification of quantum protocols

Protocols such as teleportation, superdense coding, and error correction can be specified by SQL entailments.

For example, teleportation can be expressed schematically as an entailment from a Bell-resource context and a classical communication context to the transfer of an unknown state proposition. The proof of the protocol becomes a derivation in SQL.

---

## 11. Categorical Semantics

SQL admits a clean categorical semantics.

Let \(\mathbf{C}\) be a dagger compact category with finite biproducts. The category \(\mathbf{Hilb}_{fd}\) of finite-dimensional Hilbert spaces is the prototypical example.

A **structural quantum logic model** consists of:

1. a dagger compact category \(\mathbf{C}\);
2. a truth assignment
   \[
   \Omega:\mathbf{C}^{op}\to \mathbf{EffAlg},
   \]
   assigning to each object \(X\) an effect algebra \(\Omega(X)\);
3. for each morphism \(f:X\to Y\), a pullback
   \[
   \Omega(f):\Omega(Y)\to \Omega(X);
   \]
4. tensorial structure
   \[
   \Omega(X)\times\Omega(Y)\to \Omega(X\otimes Y).
   \]

In \(\mathbf{Hilb}_{fd}\),
\[
\Omega(\mathcal{H})=\operatorname{Eff}(\mathcal{H}).
\]
For a channel \(\Phi:\mathcal{H}\to\mathcal{K}\),
\[
\Omega(\Phi)=\Phi^\dagger.
\]

A proposition is a morphism into the truth object, or equivalently an element of \(\Omega(X)\). A state is a morphism
\[
\rho:I\to X
\]
in the categorical sense, or a density operator in \(\mathbf{Hilb}_{fd}\). The truth pairing is the categorical composition of state and proposition.

This semantics makes SQL a special case of a broader principle:

\[
\text{Logic} = \text{structure-preserving transformations in a categorical semantics}.
\]

---

## 12. Structural Truth and Logical Evolution

The essential conceptual shift in SQL is this:

\[
\text{Classical logic:}
\quad
\varphi\mapsto \{0,1\};
\]

\[
\text{Structural quantum logic:}
\quad
(\rho,E)\mapsto \operatorname{Tr}(\rho E)
\quad
\text{inside a transformed structural space}.
\]

Truth is no longer a static label. It is a relation between a state and a proposition, and that relation evolves.

The fundamental law is:
\[
\tau_\rho([\Phi]\varphi)
=
\tau_{\Phi(\rho)}(\varphi).
\]
This single equation unifies:

- Heisenberg evolution;
- Schrödinger evolution;
- measurement update;
- logical pullback;
- weakest preconditions;
- protocol verification.

SQL thereby converts logical consequence into structural dynamics.

---

## 13. Limitations and Open Problems

Several problems remain open.

1. **Complete axiomatization for finite-dimensional Hilbert lattices.**  
   The projection lattices of Hilbert spaces satisfy additional identities beyond general orthomodular lattices. A complete proof theory for all finite-dimensional SQL validities requires dimension-sensitive axioms.

2. **Infinite-dimensional systems.**  
   In infinite dimensions, one must use projection lattices of von Neumann algebras or effect algebras with appropriate topology.

3. **Non-sharp connectives.**  
   There is no unique canonical extension of meet and join to arbitrary noncommuting effects. SQL therefore supports multiple conjunctions, each with operational meaning.

4. **Complexity of automated reasoning.**  
   Semidefinite fragments are tractable in many cases, but full noncommutative lattice reasoning can be computationally hard.

5. **Proof-theoretic normalization.**  
   A full cut-elimination theorem for the combined orthomodular, dynamic, and tensor calculus requires careful treatment of interaction between additive, multiplicative, and modal rules.

These problems define a research program rather than a defect. SQL is designed to be extensible.

---

## 14. Conclusion

Structural Quantum Logic provides a rigorous framework in which logical operations are geometric, algebraic, and dynamic. Truth values are not static Boolean atoms; they inhabit structural spaces and evolve under physical or computational transformations.

The core principles of SQL are:

1. Propositions are structured objects.
2. Logical connectives are geometric operations.
3. Truth is a state–effect pairing.
4. Dynamics acts by adjoint pullback.
5. Tensor structure captures composition and entanglement.
6. Classical logic arises as a commutative fragment.
7. Contextuality forbids global Boolean truth.
8. Proof theory must respect quantum resource constraints.

SQL therefore provides a unified language for quantum foundations, automated reasoning, formal verification, and quantum computing. It replaces the classical picture of truth as a static assignment with a richer picture: truth as structure, and structure as motion.

---

## Appendix A: Summary of Core Definitions

### Structural space

\[
\mathscr{S}(\mathcal{H})
=
\bigl(
\mathcal{D}(\mathcal{H}),
\operatorname{Eff}(\mathcal{H}),
\operatorname{Chan}(\mathcal{H})
\bigr).
\]

### Truth degree

\[
\tau_\rho(E)
=
\operatorname{Tr}(\rho E).
\]

### Dynamic modality

\[
\llbracket [\Phi]\varphi\rrbracket
=
\Phi^\dagger(\llbracket\varphi\rrbracket).
\]

### Truth evolution law

\[
\tau_\rho([\Phi]\varphi)
=
\tau_{\Phi(\rho)}(\varphi).
\]

### Sharp entailment

\[
P\models Q
\iff
P\le Q.
\]

### Tensor proposition

\[
\llbracket \varphi\otimes\psi\rrbracket
=
\llbracket\varphi\rrbracket\otimes\llbracket\psi\rrbracket.
\]

### Weakest precondition

\[
\operatorname{wp}(C,Q)
=
\Phi_C^\dagger(Q).
\]

### Hoare validity

\[
\{P\}\ C\ \{Q\}
\iff
P\le \Phi_C^\dagger(Q).
\]

---

## References

1. G. Birkhoff and J. von Neumann, “The Logic of Quantum Mechanics,” *Annals of Mathematics*, 1936.  
2. G. W. Mackey, *Mathematical Foundations of Quantum Mechanics*, 1963.  
3. C. Piron, *Foundations of Quantum Physics*, 1976.  
4. S. Kochen and E. P. Specker, “The Problem of Hidden Variables in Quantum Mechanics,” *Journal of Mathematics and Mechanics*, 1967.  
5. A. Peres, “Incompatible Results of Quantum Measurements,” *Physics Letters A*, 1990.  
6. N. D. Mermin, “Simple Unified Form for the Major No-Hidden-Variables Theorems,” *Physical Review Letters*, 1990.  
7. C. J. Isham and J. Butterfield, “Topos Perspective on the Kochen–Specker Theorem,” *International Journal of Theoretical Physics*, 1998.  
8. S. Abramsky and B. Coecke, “A Categorical Semantics of Quantum Protocols,” *LICS*, 2004.  
9. P. Selinger, “A Survey of Graphical Languages for Monoidal Categories,” 2011.  
10. M. A. Nielsen and I. L. Chuang, *Quantum Computation and Quantum Information*, Cambridge University Press, 2000.
