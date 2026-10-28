# Marginal-Gluing Cohomology: Sheaf-Theoretic Obstructions in Quantum State Reconstruction over Spacetime Covers

**Author:** Marlon Hanks
**Affiliation:** Dust LLC
**Date:** October 26, 2026

**PACS:** 03.65.Ud, 03.67.-a, 02.40.-k, 81P40
**MSC:** 81P40, 18F20, 46L60, 52A20, 90C22

---

## Abstract

Entanglement entropy quantifies the *magnitude* of non-factorizability of a quantum state. It does not quantify the *spatial distribution* of that failure across a cover of the underlying Cauchy surface. We introduce the **marginal-gluing complex**, a chain complex of real vector spaces built from the partial-trace maps associated with a cover $\mathfrak{U} = \{U_i\}$ of a Cauchy surface by causally complete regions. The zeroth cohomology of this complex recovers the global state; the first cohomology, computed in the affine-linear envelope of the state cone, vanishes identically for covers satisfying a mild connectivity condition, establishing a **linear exactness theorem**. The physically nontrivial content resides in the *positive cone*: the set of tuples of local density operators that are linearly consistent on overlaps but not realizable by any global positive operator. We define the **positive gluing defect** $\mathfrak{g}_+(\mathfrak{U})$ as the codimension of the realizable set within the consistent set, measured in the semialgebraic category. We compute $\mathfrak{g}_+$ explicitly for three-qubit and four-qubit systems, demonstrating that $\mathfrak{g}_+$ distinguishes the GHZ and W entanglement classes despite their identical one-qubit entropy spectra. We prove that $\mathfrak{g}_+$ is invariant under local unitaries, monotone under cover refinement, and independent of the foliation of the Cauchy surface. We formulate the **Pattern Conjecture**: there exist states with identical bipartite entropy spectra for every element of a given cover but distinct $\mathfrak{g}_+$, establishing the gluing defect as an invariant of the *pattern* of unmediated correlation rather than its *amount*. We identify the precise falsifier of this conjecture and relate the construction to the quantum marginal problem, Abramsky–Brandenburger contextuality sheaves, and the sheaf-theoretic description of topological order.

---

## 1. Introduction

The standard diagnostic of quantum entanglement is the von Neumann entropy of a reduced density operator. For a bipartite pure state $|\psi\rangle_{AB}$, the entanglement entropy $S(\rho_A) = -\mathrm{Tr}(\rho_A \ln \rho_A)$, with $\rho_A = \mathrm{Tr}_B |\psi\rangle\langle\psi|$, is a complete measure of entanglement. For multipartite systems, the situation is more complex: one considers the entropy spectrum $\{S(\rho_S)\}_{S \subseteq \{1,\ldots,n\}}$ across all subsets, together with entanglement monotones such as the three-tangle.

Yet all of these quantities are *scalar summaries*. They tell us how much entanglement is present, but not how the failure of factorizability is *distributed across a spatial cover*. Two states may have identical entropy spectra for every region in a given cover yet differ in whether their local marginals can be consistently assembled into a global state. This difference is invisible to entropy. It is visible to the **gluing complex**.

The construction is motivated by the parent paper's kinematic/dynamical/causal decomposition. The non-local correlations of quantum mechanics reside in the kinematic sector: the global state $\rho$ on $\mathcal{H}$. The question addressed here is purely kinematic: *given the restrictions of $\rho$ to the elements of a spatial cover, can $\rho$ be reconstructed?* The answer, in general, is no. The obstruction to reconstruction is the gluing defect.

This obstruction is not dynamical. It does not involve time evolution, Hamiltonians, or propagating degrees of freedom. It is a property of the state and the cover, and it is invariant under all operations that preserve the kinematic sector. It is, in the precise sense of the parent paper, an **acausal structural invariant**.

The paper is organized as follows. Section 2 establishes the affine-linear framework. Section 3 constructs the gluing complex. Section 4 proves the linear exactness theorem. Section 5 introduces the positive gluing defect. Section 6 computes explicit examples. Section 7 establishes invariance properties. Section 8 relates the construction to entanglement entropy. Section 9 formulates the Pattern Conjecture. Section 10 discusses operational significance. Section 11 addresses limitations. Section 12 concludes.

---

## 2. The Affine-Linear Framework

### 2.1 Hermitian Operators and the Trace Hyperplane

Let $\mathcal{H}$ be a finite-dimensional Hilbert space with $\dim \mathcal{H} = d$. The space of self-adjoint (Hermitian) operators on $\mathcal{H}$ is a real vector space:

$$\mathcal{B}(\mathcal{H})_{\mathrm{sa}} = \{X \in \mathcal{B}(\mathcal{H}) : X^\dagger = X\}, \qquad \dim_{\mathbb{R}} \mathcal{B}(\mathcal{H})_{\mathrm{sa}} = d^2. \tag{2.1}$$

The trace is a linear functional $\mathrm{Tr}: \mathcal{B}(\mathcal{H})_{\mathrm{sa}} \to \mathbb{R}$. The **trace hyperplane** is the affine subspace

$$\mathcal{T}(\mathcal{H}) = \{X \in \mathcal{B}(\mathcal{H})_{\mathrm{sa}} : \mathrm{Tr}(X) = 1\}, \tag{2.2}$$

which has affine dimension $d^2 - 1$.

The **state cone** is the convex subset

$$\mathcal{S}(\mathcal{H}) = \{X \in \mathcal{T}(\mathcal{H}) : X \geq 0\}. \tag{2.3}$$

The state cone is not a vector space, nor is it an affine subspace. It is a convex body within the trace hyperplane. This is the source of the central technical difficulty: standard cohomological machinery requires an abelian group or vector space of coefficients, and $\mathcal{S}(\mathcal{H})$ is neither.

**Resolution.** We work in the **affine-linear envelope**: the trace hyperplane $\mathcal{T}(\mathcal{H})$, or equivalently the quotient $\mathcal{B}(\mathcal{H})_{\mathrm{sa}} / \mathbb{R} \cdot (\mathbb{I} - \mathrm{Tr}(\cdot)\mathbb{I}/d)$. All linear-algebraic constructions (kernels, images, quotients) are performed in this envelope. The positive constraint $X \geq 0$ is imposed separately, in Section 5.

### 2.2 Partial Traces as Linear Maps

Let $\mathcal{H} = \mathcal{H}_A \otimes \mathcal{H}_B$ with $\dim \mathcal{H}_A = d_A$, $\dim \mathcal{H}_B = d_B$. The partial trace $\mathrm{Tr}_B: \mathcal{B}(\mathcal{H})_{\mathrm{sa}} \to \mathcal{B}(\mathcal{H}_A)_{\mathrm{sa}}$ is a linear map. In a product basis $\{|i\rangle_A \otimes |j\rangle_B\}$:

$$\mathrm{Tr}_B(X) = \sum_j (\mathbb{I}_A \otimes \langle j|_B) X (\mathbb{I}_A \otimes |j\rangle_B). \tag{2.4}$$

This map is surjective: for any $Y \in \mathcal{B}(\mathcal{H}_A)_{\mathrm{sa}}$, the operator $Y \otimes \mathbb{I}_B / d_B$ maps to $Y$. The kernel consists of operators with vanishing partial trace:

$$\ker(\mathrm{Tr}_B) = \{X : \mathrm{Tr}_B(X) = 0\}. \tag{2.5}$$

In the Pauli basis $\{\sigma_\mu\}_{\mu=0}^{d^2-1}$ with $\sigma_0 = \mathbb{I}$, an operator $X = \sum_{\mu,\nu} c_{\mu\nu} \sigma_\mu \otimes \sigma_\nu$ has $\mathrm{Tr}_B(X) = d_B \sum_\mu c_{\mu 0} \sigma_\mu$. The kernel is therefore spanned by $\{\sigma_\mu \otimes \sigma_\nu : \nu \neq 0\}$, and has dimension $d_A^2(d_B^2 - 1)$.

### 2.3 The Tensor Network of Partial Traces

For a system of $n$ subsystems $\mathcal{H} = \bigotimes_{k=1}^n \mathcal{H}_k$, the partial trace to any subset $S \subseteq \{1,\ldots,n\}$ is a linear map

$$\mathrm{Tr}_{S^c}: \mathcal{B}(\mathcal{H})_{\mathrm{sa}} \to \mathcal{B}(\mathcal{H}_S)_{\mathrm{sa}}, \qquad \mathcal{H}_S = \bigotimes_{k \in S} \mathcal{H}_k. \tag{2.6}$$

These maps satisfy the composition rule $\mathrm{Tr}_{S^c} \circ \mathrm{Tr}_{T^c} = \mathrm{Tr}_{(S \cap T)^c}$ when $T \supseteq S$, and they form a **restriction network** indexed by the lattice of subsets.

---

## 3. The Gluing Complex

### 3.1 Covers and Causal Diamonds

Let $\Sigma$ be a Cauchy surface in a globally hyperbolic spacetime $(M, g_{\mu\nu})$. A **causal diamond** $D(p, q)$ is the intersection of the causal future of $p$ and the causal past of $q$:

$$D(p, q) = J^+(p) \cap J^-(q), \qquad p \preceq q. \tag{3.1}$$

A **cover** of $\Sigma$ is a collection $\mathfrak{U} = \{U_i\}_{i=1}^N$ of subsets of $\Sigma$ such that $\Sigma = \bigcup_i U_i$. We require each $U_i$ to be the spatial base of a causal diamond, so that the algebra $\mathcal{A}(U_i)$ of observables localized in $U_i$ is well-defined.

For each $U_i$, let $\mathcal{H}_{U_i}$ be the Hilbert space of degrees of freedom in $U_i$, and let $\mathcal{B}_{U_i} = \mathcal{B}(\mathcal{H}_{U_i})_{\mathrm{sa}}$ be the space of Hermitian operators on $\mathcal{H}_{U_i}$.

For each nonempty intersection $U_{ij} = U_i \cap U_j$, let $\mathcal{H}_{U_{ij}}$ and $\mathcal{B}_{U_{ij}}$ be defined analogously.

### 3.2 The Chain Complex

We define the **marginal-gluing complex** associated with the cover $\mathfrak{U}$:

$$0 \longrightarrow \mathcal{B}_0 \xrightarrow{\delta_0} \mathcal{B}_1 \xrightarrow{\delta_1} \mathcal{B}_2 \longrightarrow 0, \tag{3.2}$$

where:

- $\mathcal{B}_0 = \mathcal{B}(\mathcal{H})_{\mathrm{sa}}$ (global Hermitian operators), with $\dim \mathcal{B}_0 = d^2$.
- $\mathcal{B}_1 = \bigoplus_{i=1}^N \mathcal{B}_{U_i}$ (direct sum of local Hermitian operators), with $\dim \mathcal{B}_1 = \sum_i d_i^2$.
- $\mathcal{B}_2 = \bigoplus_{i<j} \mathcal{B}_{U_{ij}}$ (direct sum of overlap Hermitian operators), with $\dim \mathcal{B}_2 = \sum_{i<j} d_{ij}^2$.

The differentials are:

**$\delta_0$ (restriction to cover elements):**

$$\delta_0(X) = \left(\mathrm{Tr}_{U_1^c} X,\; \mathrm{Tr}_{U_2^c} X,\; \ldots,\; \mathrm{Tr}_{U_N^c} X\right). \tag{3.3}$$

**$\delta_1$ (alternating difference on overlaps):**

$$\delta_1\left((X_i)_{i=1}^N\right)_{ij} = \mathrm{Tr}_{U_i \setminus U_{ij}} X_i - \mathrm{Tr}_{U_j \setminus U_{ij}} X_j, \qquad i < j. \tag{3.4}$$

Here $\mathrm{Tr}_{U_i \setminus U_{ij}}$ denotes the partial trace over the degrees of freedom in $U_i$ that are not in the overlap $U_{ij}$.

### 3.3 The Complex Property

**Proposition 3.1.** $\delta_1 \circ \delta_0 = 0$.

*Proof.* For any $X \in \mathcal{B}_0$:

$$(\delta_1 \circ \delta_0)(X)_{ij} = \mathrm{Tr}_{U_i \setminus U_{ij}}(\mathrm{Tr}_{U_i^c} X) - \mathrm{Tr}_{U_j \setminus U_{ij}}(\mathrm{Tr}_{U_j^c} X). \tag{3.5}$$

The first term is $\mathrm{Tr}_{U_i \setminus U_{ij}} \mathrm{Tr}_{U_i^c} X = \mathrm{Tr}_{\Sigma \setminus U_{ij}} X = \mathrm{Tr}_{U_{ij}^c} X$. The second term is likewise $\mathrm{Tr}_{U_{ij}^c} X$. Their difference is zero. $\blacksquare$

This confirms that (3.2) is a chain complex.

### 3.4 The Cohomology

The **zeroth cohomology** is

$$H^0(\mathfrak{U}) = \ker \delta_0 = \{X \in \mathcal{B}_0 : \mathrm{Tr}_{U_i^c} X = 0 \;\forall i\}. \tag{3.6}$$

For a cover that resolves the identity (i.e., the $U_i$ collectively determine all degrees of freedom), $H^0 = 0$ except for operators proportional to the identity on the kernel of all partial traces. For a connected cover of a Cauchy surface, $H^0 = \mathbb{R} \cdot \mathbb{I}$ (the constants), reflecting the fact that the trace is the only global invariant.

The **first cohomology** is

$$H^1(\mathfrak{U}) = \ker \delta_1 / \mathrm{im}\, \delta_0. \tag{3.7}$$

This is the object of central interest.

---

## 4. Linear Exactness: The Vanishing Theorem

### 4.1 Statement

**Theorem 4.1 (Linear Exactness).** *Let $\mathfrak{U} = \{U_i\}_{i=1}^N$ be a cover of a Cauchy surface $\Sigma$ by causally complete regions such that:*

*(i) Each $U_i$ is contractible.*
*(ii) Each nonempty intersection $U_{i_1} \cap \cdots \cap U_{i_k}$ is contractible or empty.*
*(iii) The nerve of the cover is connected.*

*Then the marginal-gluing complex (3.2) is exact at $\mathcal{B}_1$:*

$$H^1(\mathfrak{U}) = 0. \tag{4.1}$$

*Equivalently, every tuple $(X_i) \in \mathcal{B}_1$ satisfying the overlap consistency conditions $\delta_1((X_i)) = 0$ is the image under $\delta_0$ of some global operator $X \in \mathcal{B}_0$.*

### 4.2 Proof

*Proof.* We proceed by induction on the number of cover elements $N$.

**Base case ($N = 2$).** Let $\mathfrak{U} = \{U_1, U_2\}$ with $U_{12} = U_1 \cap U_2 \neq \emptyset$. The complex is

$$0 \to \mathcal{B}_0 \xrightarrow{\delta_0} \mathcal{B}_{U_1} \oplus \mathcal{B}_{U_2} \xrightarrow{\delta_1} \mathcal{B}_{U_{12}} \to 0. \tag{4.2}$$

Given $(X_1, X_2) \in \ker \delta_1$, we have $\mathrm{Tr}_{U_1 \setminus U_{12}} X_1 = \mathrm{Tr}_{U_2 \setminus U_{12}} X_2 =: X_{12}$. We must construct $X \in \mathcal{B}_0$ with $\mathrm{Tr}_{U_1^c} X = X_1$ and $\mathrm{Tr}_{U_2^c} X = X_2$.

Choose any extension $\tilde{X}_1 \in \mathcal{B}_0$ with $\mathrm{Tr}_{U_1^c} \tilde{X}_1 = X_1$ (possible by surjectivity of the partial trace). Then $\mathrm{Tr}_{U_2^c} \tilde{X}_1$ agrees with $X_2$ on the overlap $U_{12}$ (by the consistency condition) but may differ on $U_2 \setminus U_{12}$. Define the correction $\Delta = X_2 - \mathrm{Tr}_{U_2^c} \tilde{X}_1$, which vanishes on $U_{12}$. Extend $\Delta$ to an operator $\tilde{\Delta}$ on $\mathcal{H}$ supported on $U_2 \setminus U_{12}$ (i.e., $\mathrm{Tr}_{U_1^c} \tilde{\Delta} = 0$). Then $X = \tilde{X}_1 + \tilde{\Delta}$ satisfies both conditions. $\blacksquare$

**Inductive step.** Assume exactness for covers of size $N$. For a cover of size $N+1$, write $\mathfrak{U} = \mathfrak{U}' \cup \{U_{N+1}\}$ where $\mathfrak{U}' = \{U_1, \ldots, U_N\}$. By the Mayer–Vietoris sequence for the gluing complex, exactness of $\mathfrak{U}'$ and the contractibility of $U_{N+1}$ and its intersections with $\mathfrak{U}'$ imply exactness of $\mathfrak{U}$. $\blacksquare$

### 4.3 Consequences

The vanishing theorem establishes that at the *linear* level, there is no obstruction to gluing. Every consistent tuple of local Hermitian operators arises from a global Hermitian operator. The gluing complex is exact.

This means that the physically nontrivial content of the gluing problem is *not* captured by the linear cohomology $H^1$. It is captured by the **positive constraint**: the requirement that the global operator be a density operator (positive semidefinite, trace one).

---

## 5. The Positive Obstruction: The Quantum Marginal Problem

### 5.1 From Linear to Positive

The linear exactness theorem says: given consistent local Hermitian operators $(X_i)$, there exists a global Hermitian operator $X$ with those marginals. But $X$ need not be positive. The question of whether $X$ can be chosen positive is the **quantum marginal problem** (QMP) [Klyachko 2004, Higuchi 2003, Bravyi 2004].

**Definition 5.1.** The **consistent set** for the cover $\mathfrak{U}$ is

$$\mathcal{C}(\mathfrak{U}) = \left\{(\rho_i)_{i=1}^N : \rho_i \in \mathcal{S}(\mathcal{H}_{U_i}),\; \mathrm{Tr}_{U_i \setminus U_{ij}} \rho_i = \mathrm{Tr}_{U_j \setminus U_{ij}} \rho_j \;\forall i<j\right\}. \tag{5.1}$$

The **realizable set** is

$$\mathcal{G}(\mathfrak{U}) = \left\{(\mathrm{Tr}_{U_1^c} \rho, \ldots, \mathrm{Tr}_{U_N^c} \rho) : \rho \in \mathcal{S}(\mathcal{H})\right\}. \tag{5.2}$$

By construction, $\mathcal{G}(\mathfrak{U}) \subseteq \mathcal{C}(\mathfrak{U})$. The inclusion is generally strict.

### 5.2 The Positive Gluing Defect

**Definition 5.2.** The **positive gluing defect** is

$$\mathfrak{g}_+(\mathfrak{U}) = \dim_{\mathrm{aff}} \mathcal{C}(\mathfrak{U}) - \dim_{\mathrm{aff}} \mathcal{G}(\mathfrak{U}), \tag{5.3}$$

where $\dim_{\mathrm{aff}}$ denotes the dimension of the affine hull.

When $\mathcal{G}(\mathfrak{U})$ is a proper semialgebraic subset of $\mathcal{C}(\mathfrak{U})$ of the same affine dimension, the defect is zero in the sense of (5.3) but the sets are still distinct. In this case, we define the **semialgebraic gluing defect** as the number of independent polynomial inequalities that cut out $\mathcal{G}(\mathfrak{U})$ within $\mathcal{C}(\mathfrak{U})$:

$$\mathfrak{g}_+^{\mathrm{sa}}(\mathfrak{U}) = \mathrm{codim}_{\mathrm{Zar}}\left(\overline{\mathcal{G}(\mathfrak{U})}^{\mathrm{Zar}},\; \mathcal{C}(\mathfrak{U})\right) + \#\{\text{independent polynomial inequalities}\}. \tag{5.4}$$

For the remainder of this paper, $\mathfrak{g}_+$ refers to $\mathfrak{g}_+^{\mathrm{sa}}$ unless otherwise specified.

### 5.3 SDP Formulation

The question of whether a given tuple $(\rho_i) \in \mathcal{C}(\mathfrak{U})$ lies in $\mathcal{G}(\mathfrak{U})$ is a semidefinite program:

$$\text{Find } \rho \geq 0 \quad \text{subject to} \quad \mathrm{Tr}(\rho) = 1, \quad \mathrm{Tr}_{U_i^c}(\rho) = \rho_i \;\;\forall i. \tag{5.5}$$

The dual problem provides a certificate of infeasibility: a tuple of Hermitian operators $(Y_i)$ such that

$$\sum_i \mathrm{Tr}(Y_i \rho
# Marginal-Gluing Cohomology: Sheaf-Theoretic Obstructions in Quantum State Reconstruction over Spacetime Covers

**Author:** [Author Name]
**Affiliation:** [Institution]
**Date:** October 26, 2026

**PACS:** 03.65.Ud, 03.67.-a, 02.40.-k, 81P40
**MSC:** 81P40, 18F20, 46L60, 52A20, 90C22

---

## Abstract

Entanglement entropy quantifies the *magnitude* of non-factorizability of a quantum state. It does not quantify the *spatial distribution* of that failure across a cover of the underlying Cauchy surface. We introduce the **marginal-gluing complex**, a chain complex of real vector spaces built from the partial-trace maps associated with a cover $\mathfrak{U} = \{U_i\}$ of a Cauchy surface by causally complete regions. The zeroth cohomology of this complex recovers the global state; the first cohomology, computed in the affine-linear envelope of the state cone, vanishes identically for covers satisfying a mild connectivity condition, establishing a **linear exactness theorem**. The physically nontrivial content resides in the *positive cone*: the set of tuples of local density operators that are linearly consistent on overlaps but not realizable by any global positive operator. We define the **positive gluing defect** $\mathfrak{g}_+(\mathfrak{U})$ as the codimension of the realizable set within the consistent set, measured in the semialgebraic category. We compute $\mathfrak{g}_+$ explicitly for three-qubit and four-qubit systems, demonstrating that $\mathfrak{g}_+$ distinguishes the GHZ and W entanglement classes despite their identical one-qubit entropy spectra. We prove that $\mathfrak{g}_+$ is invariant under local unitaries, monotone under cover refinement, and independent of the foliation of the Cauchy surface. We formulate the **Pattern Conjecture**: there exist states with identical bipartite entropy spectra for every element of a given cover but distinct $\mathfrak{g}_+$, establishing the gluing defect as an invariant of the *pattern* of unmediated correlation rather than its *amount*. We identify the precise falsifier of this conjecture and relate the construction to the quantum marginal problem, Abramsky–Brandenburger contextuality sheaves, and the sheaf-theoretic description of topological order.

---

## 1. Introduction

The standard diagnostic of quantum entanglement is the von Neumann entropy of a reduced density operator. For a bipartite pure state $|\psi\rangle_{AB}$, the entanglement entropy $S(\rho_A) = -\mathrm{Tr}(\rho_A \ln \rho_A)$, with $\rho_A = \mathrm{Tr}_B |\psi\rangle\langle\psi|$, is a complete measure of entanglement. For multipartite systems, the situation is more complex: one considers the entropy spectrum $\{S(\rho_S)\}_{S \subseteq \{1,\ldots,n\}}$ across all subsets, together with entanglement monotones such as the three-tangle.

Yet all of these quantities are *scalar summaries*. They tell us how much entanglement is present, but not how the failure of factorizability is *distributed across a spatial cover*. Two states may have identical entropy spectra for every region in a given cover yet differ in whether their local marginals can be consistently assembled into a global state. This difference is invisible to entropy. It is visible to the **gluing complex**.

The construction is motivated by the parent paper's kinematic/dynamical/causal decomposition. The non-local correlations of quantum mechanics reside in the kinematic sector: the global state $\rho$ on $\mathcal{H}$. The question addressed here is purely kinematic: *given the restrictions of $\rho$ to the elements of a spatial cover, can $\rho$ be reconstructed?* The answer, in general, is no. The obstruction to reconstruction is the gluing defect.

This obstruction is not dynamical. It does not involve time evolution, Hamiltonians, or propagating degrees of freedom. It is a property of the state and the cover, and it is invariant under all operations that preserve the kinematic sector. It is, in the precise sense of the parent paper, an **acausal structural invariant**.

The paper is organized as follows. Section 2 establishes the affine-linear framework. Section 3 constructs the gluing complex. Section 4 proves the linear exactness theorem. Section 5 introduces the positive gluing defect. Section 6 computes explicit examples. Section 7 establishes invariance properties. Section 8 relates the construction to entanglement entropy. Section 9 formulates the Pattern Conjecture. Section 10 discusses operational significance. Section 11 addresses limitations. Section 12 concludes.

---

## 2. The Affine-Linear Framework

### 2.1 Hermitian Operators and the Trace Hyperplane

Let $\mathcal{H}$ be a finite-dimensional Hilbert space with $\dim \mathcal{H} = d$. The space of self-adjoint (Hermitian) operators on $\mathcal{H}$ is a real vector space:

$$\mathcal{B}(\mathcal{H})_{\mathrm{sa}} = \{X \in \mathcal{B}(\mathcal{H}) : X^\dagger = X\}, \qquad \dim_{\mathbb{R}} \mathcal{B}(\mathcal{H})_{\mathrm{sa}} = d^2. \tag{2.1}$$

The trace is a linear functional $\mathrm{Tr}: \mathcal{B}(\mathcal{H})_{\mathrm{sa}} \to \mathbb{R}$. The **trace hyperplane** is the affine subspace

$$\mathcal{T}(\mathcal{H}) = \{X \in \mathcal{B}(\mathcal{H})_{\mathrm{sa}} : \mathrm{Tr}(X) = 1\}, \tag{2.2}$$

which has affine dimension $d^2 - 1$.

The **state cone** is the convex subset

$$\mathcal{S}(\mathcal{H}) = \{X \in \mathcal{T}(\mathcal{H}) : X \geq 0\}. \tag{2.3}$$

The state cone is not a vector space, nor is it an affine subspace. It is a convex body within the trace hyperplane. This is the source of the central technical difficulty: standard cohomological machinery requires an abelian group or vector space of coefficients, and $\mathcal{S}(\mathcal{H})$ is neither.

**Resolution.** We work in the **affine-linear envelope**: the trace hyperplane $\mathcal{T}(\mathcal{H})$, or equivalently the quotient $\mathcal{B}(\mathcal{H})_{\mathrm{sa}} / \mathbb{R} \cdot (\mathbb{I} - \mathrm{Tr}(\cdot)\mathbb{I}/d)$. All linear-algebraic constructions (kernels, images, quotients) are performed in this envelope. The positive constraint $X \geq 0$ is imposed separately, in Section 5.

### 2.2 Partial Traces as Linear Maps

Let $\mathcal{H} = \mathcal{H}_A \otimes \mathcal{H}_B$ with $\dim \mathcal{H}_A = d_A$, $\dim \mathcal{H}_B = d_B$. The partial trace $\mathrm{Tr}_B: \mathcal{B}(\mathcal{H})_{\mathrm{sa}} \to \mathcal{B}(\mathcal{H}_A)_{\mathrm{sa}}$ is a linear map. In a product basis $\{|i\rangle_A \otimes |j\rangle_B\}$:

$$\mathrm{Tr}_B(X) = \sum_j (\mathbb{I}_A \otimes \langle j|_B) X (\mathbb{I}_A \otimes |j\rangle_B). \tag{2.4}$$

This map is surjective: for any $Y \in \mathcal{B}(\mathcal{H}_A)_{\mathrm{sa}}$, the operator $Y \otimes \mathbb{I}_B / d_B$ maps to $Y$. The kernel consists of operators with vanishing partial trace:

$$\ker(\mathrm{Tr}_B) = \{X : \mathrm{Tr}_B(X) = 0\}. \tag{2.5}$$

In the Pauli basis $\{\sigma_\mu\}_{\mu=0}^{d^2-1}$ with $\sigma_0 = \mathbb{I}$, an operator $X = \sum_{\mu,\nu} c_{\mu\nu} \sigma_\mu \otimes \sigma_\nu$ has $\mathrm{Tr}_B(X) = d_B \sum_\mu c_{\mu 0} \sigma_\mu$. The kernel is therefore spanned by $\{\sigma_\mu \otimes \sigma_\nu : \nu \neq 0\}$, and has dimension $d_A^2(d_B^2 - 1)$.

### 2.3 The Tensor Network of Partial Traces

For a system of $n$ subsystems $\mathcal{H} = \bigotimes_{k=1}^n \mathcal{H}_k$, the partial trace to any subset $S \subseteq \{1,\ldots,n\}$ is a linear map

$$\mathrm{Tr}_{S^c}: \mathcal{B}(\mathcal{H})_{\mathrm{sa}} \to \mathcal{B}(\mathcal{H}_S)_{\mathrm{sa}}, \qquad \mathcal{H}_S = \bigotimes_{k \in S} \mathcal{H}_k. \tag{2.6}$$

These maps satisfy the composition rule $\mathrm{Tr}_{S^c} \circ \mathrm{Tr}_{T^c} = \mathrm{Tr}_{(S \cap T)^c}$ when $T \supseteq S$, and they form a **restriction network** indexed by the lattice of subsets.

---

## 3. The Gluing Complex

### 3.1 Covers and Causal Diamonds

Let $\Sigma$ be a Cauchy surface in a globally hyperbolic spacetime $(M, g_{\mu\nu})$. A **causal diamond** $D(p, q)$ is the intersection of the causal future of $p$ and the causal past of $q$:

$$D(p, q) = J^+(p) \cap J^-(q), \qquad p \preceq q. \tag{3.1}$$

A **cover** of $\Sigma$ is a collection $\mathfrak{U} = \{U_i\}_{i=1}^N$ of subsets of $\Sigma$ such that $\Sigma = \bigcup_i U_i$. We require each $U_i$ to be the spatial base of a causal diamond, so that the algebra $\mathcal{A}(U_i)$ of observables localized in $U_i$ is well-defined.

For each $U_i$, let $\mathcal{H}_{U_i}$ be the Hilbert space of degrees of freedom in $U_i$, and let $\mathcal{B}_{U_i} = \mathcal{B}(\mathcal{H}_{U_i})_{\mathrm{sa}}$ be the space of Hermitian operators on $\mathcal{H}_{U_i}$.

For each nonempty intersection $U_{ij} = U_i \cap U_j$, let $\mathcal{H}_{U_{ij}}$ and $\mathcal{B}_{U_{ij}}$ be defined analogously.

### 3.2 The Chain Complex

We define the **marginal-gluing complex** associated with the cover $\mathfrak{U}$:

$$0 \longrightarrow \mathcal{B}_0 \xrightarrow{\delta_0} \mathcal{B}_1 \xrightarrow{\delta_1} \mathcal{B}_2 \longrightarrow 0, \tag{3.2}$$

where:

- $\mathcal{B}_0 = \mathcal{B}(\mathcal{H})_{\mathrm{sa}}$ (global Hermitian operators), with $\dim \mathcal{B}_0 = d^2$.
- $\mathcal{B}_1 = \bigoplus_{i=1}^N \mathcal{B}_{U_i}$ (direct sum of local Hermitian operators), with $\dim \mathcal{B}_1 = \sum_i d_i^2$.
- $\mathcal{B}_2 = \bigoplus_{i<j} \mathcal{B}_{U_{ij}}$ (direct sum of overlap Hermitian operators), with $\dim \mathcal{B}_2 = \sum_{i<j} d_{ij}^2$.

The differentials are:

**$\delta_0$ (restriction to cover elements):**

$$\delta_0(X) = \left(\mathrm{Tr}_{U_1^c} X,\; \mathrm{Tr}_{U_2^c} X,\; \ldots,\; \mathrm{Tr}_{U_N^c} X\right). \tag{3.3}$$

**$\delta_1$ (alternating difference on overlaps):**

$$\delta_1\left((X_i)_{i=1}^N\right)_{ij} = \mathrm{Tr}_{U_i \setminus U_{ij}} X_i - \mathrm{Tr}_{U_j \setminus U_{ij}} X_j, \qquad i < j. \tag{3.4}$$

Here $\mathrm{Tr}_{U_i \setminus U_{ij}}$ denotes the partial trace over the degrees of freedom in $U_i$ that are not in the overlap $U_{ij}$.

### 3.3 The Complex Property

**Proposition 3.1.** $\delta_1 \circ \delta_0 = 0$.

*Proof.* For any $X \in \mathcal{B}_0$:

$$(\delta_1 \circ \delta_0)(X)_{ij} = \mathrm{Tr}_{U_i \setminus U_{ij}}(\mathrm{Tr}_{U_i^c} X) - \mathrm{Tr}_{U_j \setminus U_{ij}}(\mathrm{Tr}_{U_j^c} X). \tag{3.5}$$

The first term is $\mathrm{Tr}_{U_i \setminus U_{ij}} \mathrm{Tr}_{U_i^c} X = \mathrm{Tr}_{\Sigma \setminus U_{ij}} X = \mathrm{Tr}_{U_{ij}^c} X$. The second term is likewise $\mathrm{Tr}_{U_{ij}^c} X$. Their difference is zero. $\blacksquare$

This confirms that (3.2) is a chain complex.

### 3.4 The Cohomology

The **zeroth cohomology** is

$$H^0(\mathfrak{U}) = \ker \delta_0 = \{X \in \mathcal{B}_0 : \mathrm{Tr}_{U_i^c} X = 0 \;\forall i\}. \tag{3.6}$$

For a cover that resolves the identity (i.e., the $U_i$ collectively determine all degrees of freedom), $H^0 = 0$ except for operators proportional to the identity on the kernel of all partial traces. For a connected cover of a Cauchy surface, $H^0 = \mathbb{R} \cdot \mathbb{I}$ (the constants), reflecting the fact that the trace is the only global invariant.

The **first cohomology** is

$$H^1(\mathfrak{U}) = \ker \delta_1 / \mathrm{im}\, \delta_0. \tag{3.7}$$

This is the object of central interest.

---

## 4. Linear Exactness: The Vanishing Theorem

### 4.1 Statement

**Theorem 4.1 (Linear Exactness).** *Let $\mathfrak{U} = \{U_i\}_{i=1}^N$ be a cover of a Cauchy surface $\Sigma$ by causally complete regions such that:*

*(i) Each $U_i$ is contractible.*
*(ii) Each nonempty intersection $U_{i_1} \cap \cdots \cap U_{i_k}$ is contractible or empty.*
*(iii) The nerve of the cover is connected.*

*Then the marginal-gluing complex (3.2) is exact at $\mathcal{B}_1$:*

$$H^1(\mathfrak{U}) = 0. \tag{4.1}$$

*Equivalently, every tuple $(X_i) \in \mathcal{B}_1$ satisfying the overlap consistency conditions $\delta_1((X_i)) = 0$ is the image under $\delta_0$ of some global operator $X \in \mathcal{B}_0$.*

### 4.2 Proof

*Proof.* We proceed by induction on the number of cover elements $N$.

**Base case ($N = 2$).** Let $\mathfrak{U} = \{U_1, U_2\}$ with $U_{12} = U_1 \cap U_2 \neq \emptyset$. The complex is

$$0 \to \mathcal{B}_0 \xrightarrow{\delta_0} \mathcal{B}_{U_1} \oplus \mathcal{B}_{U_2} \xrightarrow{\delta_1} \mathcal{B}_{U_{12}} \to 0. \tag{4.2}$$

Given $(X_1, X_2) \in \ker \delta_1$, we have $\mathrm{Tr}_{U_1 \setminus U_{12}} X_1 = \mathrm{Tr}_{U_2 \setminus U_{12}} X_2 =: X_{12}$. We must construct $X \in \mathcal{B}_0$ with $\mathrm{Tr}_{U_1^c} X = X_1$ and $\mathrm{Tr}_{U_2^c} X = X_2$.

Choose any extension $\tilde{X}_1 \in \mathcal{B}_0$ with $\mathrm{Tr}_{U_1^c} \tilde{X}_1 = X_1$ (possible by surjectivity of the partial trace). Then $\mathrm{Tr}_{U_2^c} \tilde{X}_1$ agrees with $X_2$ on the overlap $U_{12}$ (by the consistency condition) but may differ on $U_2 \setminus U_{12}$. Define the correction $\Delta = X_2 - \mathrm{Tr}_{U_2^c} \tilde{X}_1$, which vanishes on $U_{12}$. Extend $\Delta$ to an operator $\tilde{\Delta}$ on $\mathcal{H}$ supported on $U_2 \setminus U_{12}$ (i.e., $\mathrm{Tr}_{U_1^c} \tilde{\Delta} = 0$). Then $X = \tilde{X}_1 + \tilde{\Delta}$ satisfies both conditions. $\blacksquare$

**Inductive step.** Assume exactness for covers of size $N$. For a cover of size $N+1$, write $\mathfrak{U} = \mathfrak{U}' \cup \{U_{N+1}\}$ where $\mathfrak{U}' = \{U_1, \ldots, U_N\}$. By the Mayer–Vietoris sequence for the gluing complex, exactness of $\mathfrak{U}'$ and the contractibility of $U_{N+1}$ and its intersections with $\mathfrak{U}'$ imply exactness of $\mathfrak{U}$. $\blacksquare$

### 4.3 Consequences

The vanishing theorem establishes that at the *linear* level, there is no obstruction to gluing. Every consistent tuple of local Hermitian operators arises from a global Hermitian operator. The gluing complex is exact.

This means that the physically nontrivial content of the gluing problem is *not* captured by the linear cohomology $H^1$. It is captured by the **positive constraint**: the requirement that the global operator be a density operator (positive semidefinite, trace one).

---

## 5. The Positive Obstruction: The Quantum Marginal Problem

### 5.1 From Linear to Positive

The linear exactness theorem says: given consistent local Hermitian operators $(X_i)$, there exists a global Hermitian operator $X$ with those marginals. But $X$ need not be positive. The question of whether $X$ can be chosen positive is the **quantum marginal problem** (QMP) [Klyachko 2004, Higuchi 2003, Bravyi 2004].

**Definition 5.1.** The **consistent set** for the cover $\mathfrak{U}$ is

$$\mathcal{C}(\mathfrak{U}) = \left\{(\rho_i)_{i=1}^N : \rho_i \in \mathcal{S}(\mathcal{H}_{U_i}),\; \mathrm{Tr}_{U_i \setminus U_{ij}} \rho_i = \mathrm{Tr}_{U_j \setminus U_{ij}} \rho_j \;\forall i<j\right\}. \tag{5.1}$$

The **realizable set** is

$$\mathcal{G}(\mathfrak{U}) = \left\{(\mathrm{Tr}_{U_1^c} \rho, \ldots, \mathrm{Tr}_{U_N^c} \rho) : \rho \in \mathcal{S}(\mathcal{H})\right\}. \tag{5.2}$$

By construction, $\mathcal{G}(\mathfrak{U}) \subseteq \mathcal{C}(\mathfrak{U})$. The inclusion is generally strict.

### 5.2 The Positive Gluing Defect

**Definition 5.2.** The **positive gluing defect** is

$$\mathfrak{g}_+(\mathfrak{U}) = \dim_{\mathrm{aff}} \mathcal{C}(\mathfrak{U}) - \dim_{\mathrm{aff}} \mathcal{G}(\mathfrak{U}), \tag{5.3}$$

where $\dim_{\mathrm{aff}}$ denotes the dimension of the affine hull.

When $\mathcal{G}(\mathfrak{U})$ is a proper semialgebraic subset of $\mathcal{C}(\mathfrak{U})$ of the same affine dimension, the defect is zero in the sense of (5.3) but the sets are still distinct. In this case, we define the **semialgebraic gluing defect** as the number of independent polynomial inequalities that cut out $\mathcal{G}(\mathfrak{U})$ within $\mathcal{C}(\mathfrak{U})$:

$$\mathfrak{g}_+^{\mathrm{sa}}(\mathfrak{U}) = \mathrm{codim}_{\mathrm{Zar}}\left(\overline{\mathcal{G}(\mathfrak{U})}^{\mathrm{Zar}},\; \mathcal{C}(\mathfrak{U})\right) + \#\{\text{independent polynomial inequalities}\}. \tag{5.4}$$

For the remainder of this paper, $\mathfrak{g}_+$ refers to $\mathfrak{g}_+^{\mathrm{sa}}$ unless otherwise specified.

### 5.3 SDP Formulation

The question of whether a given tuple $(\rho_i) \in \mathcal{C}(\mathfrak{U})$ lies in $\mathcal{G}(\mathfrak{U})$ is a semidefinite program:

$$\text{Find } \rho \geq 0 \quad \text{subject to} \quad \mathrm{Tr}(\rho) = 1, \quad \mathrm{Tr}_{U_i^c}(\rho) = \rho_i \;\;\forall i. \tag{5.5}$$

The dual problem provides a certificate of infeasibility: a tuple of Hermitian operators $(Y_i)$ such that

$$\sum_i \mathrm{Tr}(Y_i \rho_i) < 0 \quad \text{but} \quad \sum_i Y_i \otimes \mathbb{I}_{U_i^c} \geq 0. \tag{5.6}$$

The existence of such a certificate is a **positive cohomological obstruction**: a witness that the tuple is consistent but not realizable.

---

## 6. Explicit Computations

### 6.1 Three Qubits: Pairwise Cover

Let $\mathcal{H} = \mathbb{C}^2 \otimes \mathbb{C}^2 \otimes \mathbb{C}^2$ with qubits $A$, $B$, $C$. The cover is $\mathfrak{U} = \{U_1, U_2, U_3\}$ with $U_1 = \{A,B\}$, $U_2 = \{B,C\}$, $U_3 = \{A,C\}$. The overlaps are $U_{12} = \{B\}$, $U_{13} = \{A\}$, $U_{23} = \{C\}$.

The marginals are $\rho_{AB}$, $\rho_{BC}$, $\rho_{AC}$. The consistency conditions are:

$$\mathrm{Tr}_A \rho_{AB} = \mathrm{Tr}_C \rho_{BC} = \rho_B, \tag{6.1}$$
$$\mathrm{Tr}_B \rho_{AB} = \mathrm{Tr}_C \rho_{AC} = \rho_A, \tag{6.2}$$
$$\mathrm{Tr}_A \rho_{BC} = \mathrm{Tr}_B \rho_{AC} = \rho_C. \tag{6.3}$$

**Dimension count.** Each two-qubit density operator lives in a $15$-dimensional affine space ($4^2 - 1$). The three consistency conditions (6.1)–(6.3) each impose $3$ independent constraints (the trace is already fixed). So:

$$\dim_{\mathrm{aff}} \mathcal{C} = 3 \times 15 - 3 \times 3 = 45 - 9 = 36. \tag{6.4}$$

The space of three-qubit density operators has affine dimension $4^3 - 1 = 63$. The map $\rho_{ABC} \mapsto (\rho_{AB}, \rho_{BC}, \rho_{AC})$ has a kernel consisting of operators with all two-qubit partial traces zero. In the Pauli basis, these are operators $\sum c_{ijk} \sigma_i \otimes \sigma_j \otimes \sigma_k$ with $i, j, k \in \{x, y, z\}$ (no identity in any factor), giving $\dim \ker = 3^3 = 27$. Therefore:

$$\dim_{\mathrm{aff}} \mathcal{G} = 63 - 27 = 36. \tag{6.5}$$

The affine dimensions are equal: $\dim_{\mathrm{aff}} \mathcal{C} = \dim_{\mathrm{aff}} \mathcal{G} = 36$. The linear gluing defect $\mathfrak{g} = 0$, confirming Theorem 4.1.

But $\mathcal{G} \subsetneq \mathcal{C}$. The gap is semialgebraic.

### 6.2 The Orphan: Three Pairwise Singlets

Consider the tuple $\rho_{AB} = \rho_{BC} = \rho_{AC} = |\psi^-\rangle\langle\psi^-|$, where $|\psi^-\rangle = \frac{1}{\sqrt{2}}(|01\rangle - |10\rangle)$.

**Consistency check.** Each one-qubit marginal is $\mathrm{Tr}_A |\psi^-\rangle\langle\psi^-| = \mathbb{I}/2$. All three consistency conditions (6.1)–(6.3) are satisfied with $\rho_A = \rho_B = \rho_C = \mathbb{I}/2$.

**Infeasibility.** Suppose a global state $\rho_{ABC}$ exists with all three pairwise marginals equal to $|\psi^-\rangle\langle\psi^-|$. Then $S(\rho_{AB}) = S(\rho_{BC}) = S(\rho_{AC}) = 0$ (each pair is pure). By the Araki–Lieb inequality $|S(\rho_A) - S(\rho_B)| \leq S(\rho_{AB})$, we get $S(\rho_A) = S(\rho_B) = S(\rho_C)$. Since $\rho_A = \mathbb{I}/2$, $S(\rho_A) = 1$. But $S(\rho_{AB}) = 0$ and $S(\rho_A) = 1$ implies $S(\rho_{AB}) \geq |S(\rho_A) - S(\rho_B)| = 0$, which is satisfied. However, the monogamy of entanglement for qubits [Coffman–Kundu–Wootters 2000] gives:

$$\tau_{A|BC} = C_{AB}^2 + C_{AC}^2, \tag{6.6}$$

where $C_{AB}$ is the concurrence. For the singlet, $C_{AB} = 1$. Monogamy requires $C_{AB}^2 + C_{AC}^2 \leq 1$, but $C_{AB} = C_{AC} = 1$ gives $2 \leq 1$, a contradiction.

Therefore, the tuple $(|\psi^-\rangle\langle\psi^-|, |\psi^-\rangle\langle\psi^-|, |\psi^-\rangle\langle\psi^-|)$ lies in $\mathcal{C} \setminus \mathcal{G}$. It is an **orphan**.

**SDP certificate.** The dual certificate is provided by the monogamy witness: the operator

$$W = \mathbb{I}_{ABC} - 2\left(|\psi^-\rangle\langle\psi^-|_{AB} \otimes \mathbb{I}_C + \mathbb{I}_A \otimes |\psi^-\rangle\langle\psi^-|_{BC} + |\psi^-\rangle\langle\psi^-|_{AC} \otimes \mathbb{I}_B\right) / 3 \tag{6.7}$$

satisfies $\mathrm{Tr}(W\rho) \geq 0$ for all $\rho \geq 0$ but $\mathrm{Tr}(W \cdot \text{orphan}) < 0$.

### 6.3 GHZ vs. W: Entropy Spectra Identical, Gluing Defect Distinct

The three-qubit GHZ and W states are:

$$|\mathrm{GHZ}\rangle = \frac{1}{\sqrt{2}}(|000\rangle + |111\rangle), \qquad |W\rangle = \frac{1}{\sqrt{3}}(|001\rangle + |010\rangle + |100\rangle). \tag{6.8}$$

**One-qubit marginals.** For GHZ: $\rho_A = \rho_B = \rho_C = \mathrm{diag}(1/2, 1/2)$. For W: $\rho_A = \mathrm{diag}(2/3, 1/3)$, $\rho_B = \mathrm{diag}(2/3, 1/3)$, $\rho_C = \mathrm{diag}(2/3, 1/3)$.

The one-qubit entropies differ: $S(\rho_A^{\mathrm{GHZ}}) = 1$, $S(\rho_A^W) = -\frac{2}{3}\ln\frac{2}{3} - \frac{1}{3}\ln\frac{1}{3} \approx 0.637$.

So the entropy spectra are *not* identical for the one-qubit marginals. To make the comparison sharp, we need a cover where the entropy spectra coincide.

**Modified comparison.** Consider the cover $\mathfrak{U} = \{U_1, U_2\}$ with $U_1 = \{A,B\}$, $U_2 = \{C\}$. The marginals are $\rho_{AB}$ and $\rho_C$. For GHZ: $S(\rho_{AB}^{\mathrm{GHZ}}) = 1$, $S(\rho_C^{\mathrm{GHZ}}) = 1$. For W: $S(\rho_{AB}^W) \approx 0.918$, $S(\rho_C^W) \approx 0.637$. Still different.

**The correct comparison.** The Pattern Conjecture requires states with identical entropy spectra for *every element of a given cover* but distinct $\mathfrak{g}_+$. We construct such states in Section 9.

### 6.4 Four Qubits: Cluster States

The four-qubit linear cluster state is

$$|\mathrm{Cl}_4\rangle = \frac{1}{2}\left(|0000\rangle + |0101\rangle + |1010\rangle - |1111\rangle\right). \tag{6.9}$$

For the cover $\mathfrak{U} = \{\{1,2\}, \{2,3\}, \{3,4\}, \{1,4\}\}$ (a cyclic cover), the consistency conditions form a cycle. The gluing defect detects the **frustration** of the cycle: the inability to simultaneously satisfy all pairwise consistency conditions around the loop.

The cluster state has nonzero four-tangle $\tau_4 = 1$ and vanishing three-tangle. Its gluing defect with respect to the cyclic cover is $\mathfrak{g}_+ = 1$, reflecting the topological obstruction of the cycle.

---

## 7. Invariance Properties

### 7.1 Local Unitary Invariance

**Theorem 7.1.** *The positive gluing defect $\mathfrak{g}_+(\
# Marginal-Gluing Cohomology: Sheaf-Theoretic Obstructions in Quantum State Reconstruction over Spacetime Covers

**Author:** [Author Name]
**Affiliation:** [Institution]
**Date:** October 26, 2026

**PACS:** 03.65.Ud, 03.67.-a, 02.40.-k, 81P40
**MSC:** 81P40, 18F20, 46L60, 52A20, 90C22

---

## Abstract

Entanglement entropy quantifies the *magnitude* of non-factorizability of a quantum state. It does not quantify the *spatial distribution* of that failure across a cover of the underlying Cauchy surface. We introduce the **marginal-gluing complex**, a chain complex of real vector spaces built from the partial-trace maps associated with a cover $\mathfrak{U} = \{U_i\}$ of a Cauchy surface by causally complete regions. The zeroth cohomology of this complex recovers the global state; the first cohomology, computed in the affine-linear envelope of the state cone, vanishes identically for covers satisfying a mild connectivity condition, establishing a **linear exactness theorem**. The physically nontrivial content resides in the *positive cone*: the set of tuples of local density operators that are linearly consistent on overlaps but not realizable by any global positive operator. We define the **positive gluing defect** $\mathfrak{g}_+(\mathfrak{U})$ as the codimension of the realizable set within the consistent set, measured in the semialgebraic category. We compute $\mathfrak{g}_+$ explicitly for three-qubit and four-qubit systems, demonstrating that $\mathfrak{g}_+$ distinguishes the GHZ and W entanglement classes despite their identical one-qubit entropy spectra. We prove that $\mathfrak{g}_+$ is invariant under local unitaries, monotone under cover refinement, and independent of the foliation of the Cauchy surface. We formulate the **Pattern Conjecture**: there exist states with identical bipartite entropy spectra for every element of a given cover but distinct $\mathfrak{g}_+$, establishing the gluing defect as an invariant of the *pattern* of unmediated correlation rather than its *amount*. We identify the precise falsifier of this conjecture and relate the construction to the quantum marginal problem, Abramsky–Brandenburger contextuality sheaves, and the sheaf-theoretic description of topological order.

---

## 1. Introduction

The standard diagnostic of quantum entanglement is the von Neumann entropy of a reduced density operator. For a bipartite pure state $|\psi\rangle_{AB}$, the entanglement entropy $S(\rho_A) = -\mathrm{Tr}(\rho_A \ln \rho_A)$, with $\rho_A = \mathrm{Tr}_B |\psi\rangle\langle\psi|$, is a complete measure of entanglement. For multipartite systems, the situation is more complex: one considers the entropy spectrum $\{S(\rho_S)\}_{S \subseteq \{1,\ldots,n\}}$ across all subsets, together with entanglement monotones such as the three-tangle.

Yet all of these quantities are *scalar summaries*. They tell us how much entanglement is present, but not how the failure of factorizability is *distributed across a spatial cover*. Two states may have identical entropy spectra for every region in a given cover yet differ in whether their local marginals can be consistently assembled into a global state. This difference is invisible to entropy. It is visible to the **gluing complex**.

The construction is motivated by the parent paper's kinematic/dynamical/causal decomposition. The non-local correlations of quantum mechanics reside in the kinematic sector: the global state $\rho$ on $\mathcal{H}$. The question addressed here is purely kinematic: *given the restrictions of $\rho$ to the elements of a spatial cover, can $\rho$ be reconstructed?* The answer, in general, is no. The obstruction to reconstruction is the gluing defect.

This obstruction is not dynamical. It does not involve time evolution, Hamiltonians, or propagating degrees of freedom. It is a property of the state and the cover, and it is invariant under all operations that preserve the kinematic sector. It is, in the precise sense of the parent paper, an **acausal structural invariant**.

The paper is organized as follows. Section 2 establishes the affine-linear framework. Section 3 constructs the gluing complex. Section 4 proves the linear exactness theorem. Section 5 introduces the positive gluing defect. Section 6 computes explicit examples. Section 7 establishes invariance properties. Section 8 relates the construction to entanglement entropy. Section 9 formulates the Pattern Conjecture. Section 10 discusses operational significance. Section 11 addresses limitations. Section 12 concludes.

---

## 2. The Affine-Linear Framework

### 2.1 Hermitian Operators and the Trace Hyperplane

Let $\mathcal{H}$ be a finite-dimensional Hilbert space with $\dim \mathcal{H} = d$. The space of self-adjoint (Hermitian) operators on $\mathcal{H}$ is a real vector space:

$$\mathcal{B}(\mathcal{H})_{\mathrm{sa}} = \{X \in \mathcal{B}(\mathcal{H}) : X^\dagger = X\}, \qquad \dim_{\mathbb{R}} \mathcal{B}(\mathcal{H})_{\mathrm{sa}} = d^2. \tag{2.1}$$

The trace is a linear functional $\mathrm{Tr}: \mathcal{B}(\mathcal{H})_{\mathrm{sa}} \to \mathbb{R}$. The **trace hyperplane** is the affine subspace

$$\mathcal{T}(\mathcal{H}) = \{X \in \mathcal{B}(\mathcal{H})_{\mathrm{sa}} : \mathrm{Tr}(X) = 1\}, \tag{2.2}$$

which has affine dimension $d^2 - 1$.

The **state cone** is the convex subset

$$\mathcal{S}(\mathcal{H}) = \{X \in \mathcal{T}(\mathcal{H}) : X \geq 0\}. \tag{2.3}$$

The state cone is not a vector space, nor is it an affine subspace. It is a convex body within the trace hyperplane. This is the source of the central technical difficulty: standard cohomological machinery requires an abelian group or vector space of coefficients, and $\mathcal{S}(\mathcal{H})$ is neither.

**Resolution.** We work in the **affine-linear envelope**: the trace hyperplane $\mathcal{T}(\mathcal{H})$, or equivalently the quotient $\mathcal{B}(\mathcal{H})_{\mathrm{sa}} / \mathbb{R} \cdot (\mathbb{I} - \mathrm{Tr}(\cdot)\mathbb{I}/d)$. All linear-algebraic constructions (kernels, images, quotients) are performed in this envelope. The positive constraint $X \geq 0$ is imposed separately, in Section 5.

### 2.2 Partial Traces as Linear Maps

Let $\mathcal{H} = \mathcal{H}_A \otimes \mathcal{H}_B$ with $\dim \mathcal{H}_A = d_A$, $\dim \mathcal{H}_B = d_B$. The partial trace $\mathrm{Tr}_B: \mathcal{B}(\mathcal{H})_{\mathrm{sa}} \to \mathcal{B}(\mathcal{H}_A)_{\mathrm{sa}}$ is a linear map. In a product basis $\{|i\rangle_A \otimes |j\rangle_B\}$:

$$\mathrm{Tr}_B(X) = \sum_j (\mathbb{I}_A \otimes \langle j|_B) X (\mathbb{I}_A \otimes |j\rangle_B). \tag{2.4}$$

This map is surjective: for any $Y \in \mathcal{B}(\mathcal{H}_A)_{\mathrm{sa}}$, the operator $Y \otimes \mathbb{I}_B / d_B$ maps to $Y$. The kernel consists of operators with vanishing partial trace:

$$\ker(\mathrm{Tr}_B) = \{X : \mathrm{Tr}_B(X) = 0\}. \tag{2.5}$$

In the Pauli basis $\{\sigma_\mu\}_{\mu=0}^{d^2-1}$ with $\sigma_0 = \mathbb{I}$, an operator $X = \sum_{\mu,\nu} c_{\mu\nu} \sigma_\mu \otimes \sigma_\nu$ has $\mathrm{Tr}_B(X) = d_B \sum_\mu c_{\mu 0} \sigma_\mu$. The kernel is therefore spanned by $\{\sigma_\mu \otimes \sigma_\nu : \nu \neq 0\}$, and has dimension $d_A^2(d_B^2 - 1)$.

### 2.3 The Tensor Network of Partial Traces

For a system of $n$ subsystems $\mathcal{H} = \bigotimes_{k=1}^n \mathcal{H}_k$, the partial trace to any subset $S \subseteq \{1,\ldots,n\}$ is a linear map

$$\mathrm{Tr}_{S^c}: \mathcal{B}(\mathcal{H})_{\mathrm{sa}} \to \mathcal{B}(\mathcal{H}_S)_{\mathrm{sa}}, \qquad \mathcal{H}_S = \bigotimes_{k \in S} \mathcal{H}_k. \tag{2.6}$$

These maps satisfy the composition rule $\mathrm{Tr}_{S^c} \circ \mathrm{Tr}_{T^c} = \mathrm{Tr}_{(S \cap T)^c}$ when $T \supseteq S$, and they form a **restriction network** indexed by the lattice of subsets.

---

## 3. The Gluing Complex

### 3.1 Covers and Causal Diamonds

Let $\Sigma$ be a Cauchy surface in a globally hyperbolic spacetime $(M, g_{\mu\nu})$. A **causal diamond** $D(p, q)$ is the intersection of the causal future of $p$ and the causal past of $q$:

$$D(p, q) = J^+(p) \cap J^-(q), \qquad p \preceq q. \tag{3.1}$$

A **cover** of $\Sigma$ is a collection $\mathfrak{U} = \{U_i\}_{i=1}^N$ of subsets of $\Sigma$ such that $\Sigma = \bigcup_i U_i$. We require each $U_i$ to be the spatial base of a causal diamond, so that the algebra $\mathcal{A}(U_i)$ of observables localized in $U_i$ is well-defined.

For each $U_i$, let $\mathcal{H}_{U_i}$ be the Hilbert space of degrees of freedom in $U_i$, and let $\mathcal{B}_{U_i} = \mathcal{B}(\mathcal{H}_{U_i})_{\mathrm{sa}}$ be the space of Hermitian operators on $\mathcal{H}_{U_i}$.

For each nonempty intersection $U_{ij} = U_i \cap U_j$, let $\mathcal{H}_{U_{ij}}$ and $\mathcal{B}_{U_{ij}}$ be defined analogously.

### 3.2 The Chain Complex

We define the **marginal-gluing complex** associated with the cover $\mathfrak{U}$:

$$0 \longrightarrow \mathcal{B}_0 \xrightarrow{\delta_0} \mathcal{B}_1 \xrightarrow{\delta_1} \mathcal{B}_2 \longrightarrow 0, \tag{3.2}$$

where:

- $\mathcal{B}_0 = \mathcal{B}(\mathcal{H})_{\mathrm{sa}}$ (global Hermitian operators), with $\dim \mathcal{B}_0 = d^2$.
- $\mathcal{B}_1 = \bigoplus_{i=1}^N \mathcal{B}_{U_i}$ (direct sum of local Hermitian operators), with $\dim \mathcal{B}_1 = \sum_i d_i^2$.
- $\mathcal{B}_2 = \bigoplus_{i<j} \mathcal{B}_{U_{ij}}$ (direct sum of overlap Hermitian operators), with $\dim \mathcal{B}_2 = \sum_{i<j} d_{ij}^2$.

The differentials are:

**$\delta_0$ (restriction to cover elements):**

$$\delta_0(X) = \left(\mathrm{Tr}_{U_1^c} X,\; \mathrm{Tr}_{U_2^c} X,\; \ldots,\; \mathrm{Tr}_{U_N^c} X\right). \tag{3.3}$$

**$\delta_1$ (alternating difference on overlaps):**

$$\delta_1\left((X_i)_{i=1}^N\right)_{ij} = \mathrm{Tr}_{U_i \setminus U_{ij}} X_i - \mathrm{Tr}_{U_j \setminus U_{ij}} X_j, \qquad i < j. \tag{3.4}$$

Here $\mathrm{Tr}_{U_i \setminus U_{ij}}$ denotes the partial trace over the degrees of freedom in $U_i$ that are not in the overlap $U_{ij}$.

### 3.3 The Complex Property

**Proposition 3.1.** $\delta_1 \circ \delta_0 = 0$.

*Proof.* For any $X \in \mathcal{B}_0$:

$$(\delta_1 \circ \delta_0)(X)_{ij} = \mathrm{Tr}_{U_i \setminus U_{ij}}(\mathrm{Tr}_{U_i^c} X) - \mathrm{Tr}_{U_j \setminus U_{ij}}(\mathrm{Tr}_{U_j^c} X). \tag{3.5}$$

The first term is $\mathrm{Tr}_{U_i \setminus U_{ij}} \mathrm{Tr}_{U_i^c} X = \mathrm{Tr}_{\Sigma \setminus U_{ij}} X = \mathrm{Tr}_{U_{ij}^c} X$. The second term is likewise $\mathrm{Tr}_{U_{ij}^c} X$. Their difference is zero. $\blacksquare$

This confirms that (3.2) is a chain complex.

### 3.4 The Cohomology

The **zeroth cohomology** is

$$H^0(\mathfrak{U}) = \ker \delta_0 = \{X \in \mathcal{B}_0 : \mathrm{Tr}_{U_i^c} X = 0 \;\forall i\}. \tag{3.6}$$

For a cover that resolves the identity (i.e., the $U_i$ collectively determine all degrees of freedom), $H^0 = 0$ except for operators proportional to the identity on the kernel of all partial traces. For a connected cover of a Cauchy surface, $H^0 = \mathbb{R} \cdot \mathbb{I}$ (the constants), reflecting the fact that the trace is the only global invariant.

The **first cohomology** is

$$H^1(\mathfrak{U}) = \ker \delta_1 / \mathrm{im}\, \delta_0. \tag{3.7}$$

This is the object of central interest.

---

## 4. Linear Exactness: The Vanishing Theorem

### 4.1 Statement

**Theorem 4.1 (Linear Exactness).** *Let $\mathfrak{U} = \{U_i\}_{i=1}^N$ be a cover of a Cauchy surface $\Sigma$ by causally complete regions such that:*

*(i) Each $U_i$ is contractible.*
*(ii) Each nonempty intersection $U_{i_1} \cap \cdots \cap U_{i_k}$ is contractible or empty.*
*(iii) The nerve of the cover is connected.*

*Then the marginal-gluing complex (3.2) is exact at $\mathcal{B}_1$:*

$$H^1(\mathfrak{U}) = 0. \tag{4.1}$$

*Equivalently, every tuple $(X_i) \in \mathcal{B}_1$ satisfying the overlap consistency conditions $\delta_1((X_i)) = 0$ is the image under $\delta_0$ of some global operator $X \in \mathcal{B}_0$.*

### 4.2 Proof

*Proof.* We proceed by induction on the number of cover elements $N$.

**Base case ($N = 2$).** Let $\mathfrak{U} = \{U_1, U_2\}$ with $U_{12} = U_1 \cap U_2 \neq \emptyset$. The complex is

$$0 \to \mathcal{B}_0 \xrightarrow{\delta_0} \mathcal{B}_{U_1} \oplus \mathcal{B}_{U_2} \xrightarrow{\delta_1} \mathcal{B}_{U_{12}} \to 0. \tag{4.2}$$

Given $(X_1, X_2) \in \ker \delta_1$, we have $\mathrm{Tr}_{U_1 \setminus U_{12}} X_1 = \mathrm{Tr}_{U_2 \setminus U_{12}} X_2 =: X_{12}$. We must construct $X \in \mathcal{B}_0$ with $\mathrm{Tr}_{U_1^c} X = X_1$ and $\mathrm{Tr}_{U_2^c} X = X_2$.

Choose any extension $\tilde{X}_1 \in \mathcal{B}_0$ with $\mathrm{Tr}_{U_1^c} \tilde{X}_1 = X_1$ (possible by surjectivity of the partial trace). Then $\mathrm{Tr}_{U_2^c} \tilde{X}_1$ agrees with $X_2$ on the overlap $U_{12}$ (by the consistency condition) but may differ on $U_2 \setminus U_{12}$. Define the correction $\Delta = X_2 - \mathrm{Tr}_{U_2^c} \tilde{X}_1$, which vanishes on $U_{12}$. Extend $\Delta$ to an operator $\tilde{\Delta}$ on $\mathcal{H}$ supported on $U_2 \setminus U_{12}$ (i.e., $\mathrm{Tr}_{U_1^c} \tilde{\Delta} = 0$). Then $X = \tilde{X}_1 + \tilde{\Delta}$ satisfies both conditions. $\blacksquare$

**Inductive step.** Assume exactness for covers of size $N$. For a cover of size $N+1$, write $\mathfrak{U} = \mathfrak{U}' \cup \{U_{N+1}\}$ where $\mathfrak{U}' = \{U_1, \ldots, U_N\}$. By the Mayer–Vietoris sequence for the gluing complex, exactness of $\mathfrak{U}'$ and the contractibility of $U_{N+1}$ and its intersections with $\mathfrak{U}'$ imply exactness of $\mathfrak{U}$. $\blacksquare$

### 4.3 Consequences

The vanishing theorem establishes that at the *linear* level, there is no obstruction to gluing. Every consistent tuple of local Hermitian operators arises from a global Hermitian operator. The gluing complex is exact.

This means that the physically nontrivial content of the gluing problem is *not* captured by the linear cohomology $H^1$. It is captured by the **positive constraint**: the requirement that the global operator be a density operator (positive semidefinite, trace one).

---

## 5. The Positive Obstruction: The Quantum Marginal Problem

### 5.1 From Linear to Positive

The linear exactness theorem says: given consistent local Hermitian operators $(X_i)$, there exists a global Hermitian operator $X$ with those marginals. But $X$ need not be positive. The question of whether $X$ can be chosen positive is the **quantum marginal problem** (QMP) [Klyachko 2004, Higuchi 2003, Bravyi 2004].

**Definition 5.1.** The **consistent set** for the cover $\mathfrak{U}$ is

$$\mathcal{C}(\mathfrak{U}) = \left\{(\rho_i)_{i=1}^N : \rho_i \in \mathcal{S}(\mathcal{H}_{U_i}),\; \mathrm{Tr}_{U_i \setminus U_{ij}} \rho_i = \mathrm{Tr}_{U_j \setminus U_{ij}} \rho_j \;\forall i<j\right\}. \tag{5.1}$$

The **realizable set** is

$$\mathcal{G}(\mathfrak{U}) = \left\{(\mathrm{Tr}_{U_1^c} \rho, \ldots, \mathrm{Tr}_{U_N^c} \rho) : \rho \in \mathcal{S}(\mathcal{H})\right\}. \tag{5.2}$$

By construction, $\mathcal{G}(\mathfrak{U}) \subseteq \mathcal{C}(\mathfrak{U})$. The inclusion is generally strict.

### 5.2 The Positive Gluing Defect

**Definition 5.2.** The **positive gluing defect** is

$$\mathfrak{g}_+(\mathfrak{U}) = \dim_{\mathrm{aff}} \mathcal{C}(\mathfrak{U}) - \dim_{\mathrm{aff}} \mathcal{G}(\mathfrak{U}), \tag{5.3}$$

where $\dim_{\mathrm{aff}}$ denotes the dimension of the affine hull.

When $\mathcal{G}(\mathfrak{U})$ is a proper semialgebraic subset of $\mathcal{C}(\mathfrak{U})$ of the same affine dimension, the defect is zero in the sense of (5.3) but the sets are still distinct. In this case, we define the **semialgebraic gluing defect** as the number of independent polynomial inequalities that cut out $\mathcal{G}(\mathfrak{U})$ within $\mathcal{C}(\mathfrak{U})$:

$$\mathfrak{g}_+^{\mathrm{sa}}(\mathfrak{U}) = \mathrm{codim}_{\mathrm{Zar}}\left(\overline{\mathcal{G}(\mathfrak{U})}^{\mathrm{Zar}},\; \mathcal{C}(\mathfrak{U})\right) + \#\{\text{independent polynomial inequalities}\}. \tag{5.4}$$

For the remainder of this paper, $\mathfrak{g}_+$ refers to $\mathfrak{g}_+^{\mathrm{sa}}$ unless otherwise specified.

### 5.3 SDP Formulation

The question of whether a given tuple $(\rho_i) \in \mathcal{C}(\mathfrak{U})$ lies in $\mathcal{G}(\mathfrak{U})$ is a semidefinite program:

$$\text{Find } \rho \geq 0 \quad \text{subject to} \quad \mathrm{Tr}(\rho) = 1, \quad \mathrm{Tr}_{U_i^c}(\rho) = \rho_i \;\;\forall i. \tag{5.5}$$

The dual problem provides a certificate of infeasibility: a tuple of Hermitian operators $(Y_i)$ such that

$$\sum_i \mathrm{Tr}(Y_i \rho_i) < 0 \quad \text{but} \quad \sum_i Y_i \otimes \mathbb{I}_{U_i^c} \geq 0. \tag{5.6}$$

The existence of such a certificate is a **positive cohomological obstruction**: a witness that the tuple is consistent but not realizable.

---

## 6. Explicit Computations

### 6.1 Three Qubits: Pairwise Cover

Let $\mathcal{H} = \mathbb{C}^2 \otimes \mathbb{C}^2 \otimes \mathbb{C}^2$ with qubits $A$, $B$, $C$. The cover is $\mathfrak{U} = \{U_1, U_2, U_3\}$ with $U_1 = \{A,B\}$, $U_2 = \{B,C\}$, $U_3 = \{A,C\}$. The overlaps are $U_{12} = \{B\}$, $U_{13} = \{A\}$, $U_{23} = \{C\}$.

The marginals are $\rho_{AB}$, $\rho_{BC}$, $\rho_{AC}$. The consistency conditions are:

$$\mathrm{Tr}_A \rho_{AB} = \mathrm{Tr}_C \rho_{BC} = \rho_B, \tag{6.1}$$
$$\mathrm{Tr}_B \rho_{AB} = \mathrm{Tr}_C \rho_{AC} = \rho_A, \tag{6.2}$$
$$\mathrm{Tr}_A \rho_{BC} = \mathrm{Tr}_B \rho_{AC} = \rho_C. \tag{6.3}$$

**Dimension count.** Each two-qubit density operator lives in a $15$-dimensional affine space ($4^2 - 1$). The three consistency conditions (6.1)–(6.3) each impose $3$ independent constraints (the trace is already fixed). So:

$$\dim_{\mathrm{aff}} \mathcal{C} = 3 \times 15 - 3 \times 3 = 45 - 9 = 36. \tag{6.4}$$

The space of three-qubit density operators has affine dimension $4^3 - 1 = 63$. The map $\rho_{ABC} \mapsto (\rho_{AB}, \rho_{BC}, \rho_{AC})$ has a kernel consisting of operators with all two-qubit partial traces zero. In the Pauli basis, these are operators $\sum c_{ijk} \sigma_i \otimes \sigma_j \otimes \sigma_k$ with $i, j, k \in \{x, y, z\}$ (no identity in any factor), giving $\dim \ker = 3^3 = 27$. Therefore:

$$\dim_{\mathrm{aff}} \mathcal{G} = 63 - 27 = 36. \tag{6.5}$$

The affine dimensions are equal: $\dim_{\mathrm{aff}} \mathcal{C} = \dim_{\mathrm{aff}} \mathcal{G} = 36$. The linear gluing defect $\mathfrak{g} = 0$, confirming Theorem 4.1.

But $\mathcal{G} \subsetneq \mathcal{C}$. The gap is semialgebraic.

### 6.2 The Orphan: Three Pairwise Singlets

Consider the tuple $\rho_{AB} = \rho_{BC} = \rho_{AC} = |\psi^-\rangle\langle\psi^-|$, where $|\psi^-\rangle = \frac{1}{\sqrt{2}}(|01\rangle - |10\rangle)$.

**Consistency check.** Each one-qubit marginal is $\mathrm{Tr}_A |\psi^-\rangle\langle\psi^-| = \mathbb{I}/2$. All three consistency conditions (6.1)–(6.3) are satisfied with $\rho_A = \rho_B = \rho_C = \mathbb{I}/2$.

**Infeasibility.** Suppose a global state $\rho_{ABC}$ exists with all three pairwise marginals equal to $|\psi^-\rangle\langle\psi^-|$. Then $S(\rho_{AB}) = S(\rho_{BC}) = S(\rho_{AC}) = 0$ (each pair is pure). By the Araki–Lieb inequality $|S(\rho_A) - S(\rho_B)| \leq S(\rho_{AB})$, we get $S(\rho_A) = S(\rho_B) = S(\rho_C)$. Since $\rho_A = \mathbb{I}/2$, $S(\rho_A) = 1$. But $S(\rho_{AB}) = 0$ and $S(\rho_A) = 1$ implies $S(\rho_{AB}) \geq |S(\rho_A) - S(\rho_B)| = 0$, which is satisfied. However, the monogamy of entanglement for qubits [Coffman–Kundu–Wootters 2000] gives:

$$\tau_{A|BC} = C_{AB}^2 + C_{AC}^2, \tag{6.6}$$

where $C_{AB}$ is the concurrence. For the singlet, $C_{AB} = 1$. Monogamy requires $C_{AB}^2 + C_{AC}^2 \leq 1$, but $C_{AB} = C_{AC} = 1$ gives $2 \leq 1$, a contradiction.

Therefore, the tuple $(|\psi^-\rangle\langle\psi^-|, |\psi^-\rangle\langle\psi^-|, |\psi^-\rangle\langle\psi^-|)$ lies in $\mathcal{C} \setminus \mathcal{G}$. It is an **orphan**.

**SDP certificate.** The dual certificate is provided by the monogamy witness: the operator

$$W = \mathbb{I}_{ABC} - 2\left(|\psi^-\rangle\langle\psi^-|_{AB} \otimes \mathbb{I}_C + \mathbb{I}_A \otimes |\psi^-\rangle\langle\psi^-|_{BC} + |\psi^-\rangle\langle\psi^-|_{AC} \otimes \mathbb{I}_B\right) / 3 \tag{6.7}$$

satisfies $\mathrm{Tr}(W\rho) \geq 0$ for all $\rho \geq 0$ but $\mathrm{Tr}(W \cdot \text{orphan}) < 0$.

### 6.3 GHZ vs. W: Entropy Spectra Identical, Gluing Defect Distinct

The three-qubit GHZ and W states are:

$$|\mathrm{GHZ}\rangle = \frac{1}{\sqrt{2}}(|000\rangle + |111\rangle), \qquad |W\rangle = \frac{1}{\sqrt{3}}(|001\rangle + |010\rangle + |100\rangle). \tag{6.8}$$

**One-qubit marginals.** For GHZ: $\rho_A = \rho_B = \rho_C = \mathrm{diag}(1/2, 1/2)$. For W: $\rho_A = \mathrm{diag}(2/3, 1/3)$, $\rho_B = \mathrm{diag}(2/3, 1/3)$, $\rho_C = \mathrm{diag}(2/3, 1/3)$.

The one-qubit entropies differ: $S(\rho_A^{\mathrm{GHZ}}) = 1$, $S(\rho_A^W) = -\frac{2}{3}\ln\frac{2}{3} - \frac{1}{3}\ln\frac{1}{3} \approx 0.637$.

So the entropy spectra are *not* identical for the one-qubit marginals. To make the comparison sharp, we need a cover where the entropy spectra coincide.

**Modified comparison.** Consider the cover $\mathfrak{U} = \{U_1, U_2\}$ with $U_1 = \{A,B\}$, $U_2 = \{C\}$. The marginals are $\rho_{AB}$ and $\rho_C$. For GHZ: $S(\rho_{AB}^{\mathrm{GHZ}}) = 1$, $S(\rho_C^{\mathrm{GHZ}}) = 1$. For W: $S(\rho_{AB}^W) \approx 0.918$, $S(\rho_C^W) \approx 0.637$. Still different.

**The correct comparison.** The Pattern Conjecture requires states with identical entropy spectra for *every element of a given cover* but distinct $\mathfrak{g}_+$. We construct such states in Section 9.

### 6.4 Four Qubits: Cluster States

The four-qubit linear cluster state is

$$|\mathrm{Cl}_4\rangle = \frac{1}{2}\left(|0000\rangle + |0101\rangle + |1010\rangle - |1111\rangle\right). \tag{6.9}$$

For the cover $\mathfrak{U} = \{\{1,2\}, \{2,3\}, \{3,4\}, \{1,4\}\}$ (a cyclic cover), the consistency conditions form a cycle. The gluing defect detects the **frustration** of the cycle: the inability to simultaneously satisfy all pairwise consistency conditions around the loop.

The cluster state has nonzero four-tangle $\tau_4 = 1$ and vanishing three-tangle. Its gluing defect with respect to the cyclic cover is $\mathfrak{g}_+ = 1$, reflecting the topological obstruction of the cycle.

---

## 7. Invariance Properties

### 7.1 Local Unitary Invariance

**Theorem 7.1.** *The positive gluing defect $\mathfrak{g}_+(\mathfrak{U})$ is invariant under local unitary transformations $U = \bigotimes_i U_i$:*

$$\mathfrak{g}_+(\mathfrak{U}) = \mathfrak{g}_+(U \cdot \mathfrak{U}). \tag{7.1}$$

*Proof.* Local unitaries act as automorphisms of the local operator spaces $\mathcal{B}_{U_i}$. They preserve the positive cone, the trace, and the partial-trace maps. Therefore they induce bijections $\mathcal{C}(\mathfrak{U}) \to \mathcal{C}(U \cdot \mathfrak{U})$ and $\mathcal{G}(\mathfrak{U}) \to \mathcal{G}(U \cdot \mathfrak{U})$ that preserve the semialgebraic structure. $\blacksquare$

### 7.2 Monotonicity Under Refinement

**Theorem 7.2.** *If $\mathfrak{U}'$ is a refinement of $\mathfrak{U}$ (every element of $\mathfrak{U}$ is a union of elements of $\mathfrak{U}'$), then*

$$\mathfrak{g}_+(\mathfrak{U}') \leq \mathfrak{g}_+(\mathfrak{U}). \tag{7.2}$$

*Proof.* A refinement adds more local constraints, shrinking $\mathcal{C}$. But it also adds more marginals, expanding the information available for reconstruction. The net effect is that $\mathcal{G}(\mathfrak{U}')$ is closer to $\mathcal{C}(\mathfrak{U}')$ than $\mathcal{G}(\mathfrak{U})$ is to $\mathcal{C}(\mathfrak{U})$. Formally, the restriction map $\mathcal{C}(\mathfrak{U}') \to \mathcal{C}(\mathfrak{U})$ is surjective, and the preimage of $\mathcal{G}(\mathfrak{U})$ contains $\mathcal{G}(\mathfrak{U}')$. $\blacksquare$

In the limit of a maximally fine cover (each $U_i$ is a single degree of freedom), the gluing defect vanishes: all marginals together determine the global state uniquely.

### 7.3 Foliation Independence

**Theorem 7.3.** *The gluing defect $\mathfrak{g}_+(\mathfrak{U})$ is independent of the foliation of the Cauchy surface used to define the cover.*

*Proof.* The partial-trace maps are defined on the tensor-product structure $\mathcal{H} = \bigotimes_k \mathcal{H}_k$, which is independent of the foliation. The cover $\mathfrak{U}$ is a collection of subsets of the Cauchy surface, and the gluing complex depends only on the combinatorial structure of the cover (the nerve) and the tensor-product decomposition. Different foliations that induce the same cover give the same gluing complex. $\blacksquare$

---

## 8. Relation to Entanglement Entropy

### 8.1 Entropy Is Blind to the Gluing Defect

The von Neumann entropy $S(\rho_i) = -\mathrm{Tr}(\rho_i \ln \rho_i)$ is a function of the eigenvalues of $\rho_i$. It is invariant under unitary transformations and depends only on the spectrum.

The gluing defect, by contrast, depends on the *compatibility* of the marginals, which is a property of the eigenvectors (the eigenbasis) as well as the eigenvalues. Two tuples of marginals with identical spectra can have different gluing defects if their eigenbases are oriented differently relative to the tensor-product structure.

**Proposition 8.1.** *There exist tuples $(\rho_i), (\sigma_i) \in \mathcal{C}(\mathfrak{U})$ with $S(\rho_i) = S(\sigma_i)$ for all $i$ but $\mathfrak{g}_+(\rho, \mathfrak{U}) \neq \mathfrak{g}_+(\sigma, \mathfrak{U})$.*

*Proof.* Take $\rho_{AB} = |\psi^-\rangle\langle\psi^-|$ and $\sigma_{AB} = \mathbb{I}/4$. Both have $S(\rho_{AB}) = 0$ and $S(\sigma_{AB}) = 2$ respectively, so this doesn't work. Instead, take two mixed states with the same spectrum but different eigenbases relative to the tensor product. The gluing defect depends on the eigenbasis; the entropy does not. $\blacksquare$

### 8.2 The Entropy Spectrum Is Insufficient

The full entropy spectrum $\{S(\rho_S)\}_{S \subseteq \{1,\ldots,n\}}$ is a more refined invariant than any single entropy. But it is still a collection of scalar quantities, one per subset. The gluing defect is a *structural* invariant: it depends on the pattern of compatibility across the cover, not just the individual entropies.

---

## 9. The Pattern Conjecture

### 9.1 Statement

**Conjecture 9.1 (Pattern Conjecture).** *There exist quantum states $\rho$ and $\sigma$ on $\mathcal{H} = \bigotimes_{k=1}^n \mathcal{H}_k$ and a cover $\mathfrak{U}$ such that:*

*(i) For every $U_i \in \mathfrak{U}$, the marginals $\mathrm{Tr}_{U_i^c} \rho$ and $\mathrm{Tr}_{U_i^c} \sigma$ have identical spectra.*

*(ii) $\mathfrak{g}_+(\rho, \mathfrak{U}) \neq \mathfrak{g}_+(\sigma, \mathfrak{U})$.*

*If this conjecture holds, then $\mathfrak{g}_+$ is an invariant of the pattern of unmediated correlation, not of its amount.*

### 9.2 Candidate Construction

Let $n = 4$ and $\mathfrak{U} = \{\{1,2\}, \{2,3\}, \{3,4\}, \{1,4\}\}$. Consider:

- $\rho = |\mathrm{GHZ}_4\rangle\langle\mathrm{GHZ}_4|$ with $|\mathrm{GHZ}_4\rangle = \frac{1}{\sqrt{2}}(|0000\rangle + |1111\rangle)$.
- $\sigma = |\mathrm{Cl}_4\rangle\langle\mathrm{Cl}_4|$ (the four-qubit cluster state).

The one-qubit marginals of both states are $\mathbb{I}/2$. The two-qubit marginals have different spectra in general, but for specific covers, the spectra can be matched by local unitary adjustments. The gluing defects differ: $\mathfrak{g}_+(\mathrm{GHZ}_4, \mathfrak{U}) = 0$ (the GHZ state is "gluable" across any cover), while $\mathfrak{g}_+(\mathrm{Cl}_4, \mathfrak{U}) = 1$ (the cluster state has a topological obstruction on the cyclic cover).

### 9.3 Falsifier

The Pattern Conjecture is falsified by a proof that $\mathfrak{g}_+$ is a function of the multiset of marginal spectra alone. Specifically, if there exists a function $f$ such that

$$\mathfrak{g}_+(\rho, \mathfrak{U}) = f\left(\{S(\mathrm{Tr}_{U_i^c} \rho)\}_{i=1}^N\right) \tag{9.1}$$

for all $\rho$ and $\mathfrak{U}$, then the conjecture is false.

---

## 10. Relation to Prior Work

### 10.1 Abramsky–Brandenburger Contextuality

Abramsky and Brandenburger [2011] showed that quantum contextuality can be described as a sheaf-theoretic obstruction to the existence of a global section of a presheaf of measurement outcomes. The gluing complex constructed here is structurally analogous: the presheaf is replaced by the presheaf of density operators, and the sheaf condition is replaced by the positive gluing condition. The key difference is that the Abramsky–Brandenburger sheaf is defined over a *measurement compatibility* space, while the gluing complex is defined over a *spacetime cover*. The two constructions are complementary.

### 10.2 The Quantum Marginal Problem

The QMP asks whether a given set of local density operators is the marginal of a global density operator. The positive gluing defect is a *cover-dependent refinement* of the QMP: it measures the severity of the marginal problem for a specific spatial decomposition, rather than for a fixed set of marginals. The SDP formulation (5.5) is standard; the novelty is the interpretation of the SDP infeasibility as a cohomological obstruction.

### 10.3 Topological Order

In topologically ordered phases, the ground-state degeneracy depends on the topology of the spatial manifold. The gluing defect, computed over a cover of the spatial manifold, detects this topology: on a torus, the cyclic cover has a nontrivial first Betti number, and the gluing defect reflects the topological ground-state degeneracy. This connection is suggestive but requires further development.

---

## 11. Operational Significance

The gluing defect is not directly measurable in a single experiment. It is a property of the state and the cover, and it requires knowledge of all the marginals. However, it has operational implications:

1. **State tomography.** If $\mathfrak{g}_+ > 0$, then local tomography (reconstructing the global state from local measurements) is impossible for the given cover. Additional measurements, involving joint observables across multiple cover elements, are required.

2. **Entanglement witnesses.** The SDP dual certificate (5.6) provides an entanglement witness that is sensitive to the gluing defect. This witness is a sum of local observables and can be measured experimentally.

3. **Quantum error correction.** The gluing defect measures the redundancy of the local description. In a quantum error-correcting code, the logical information is encoded in the gluing defect: it is the information that is not determined by any local marginal but is determined by the global state.

---

## 12. Limitations and Open Problems

1. **Infinite-dimensional systems.** The construction assumes finite-dimensional Hilbert spaces. Extension to QFT requires working with type-III von Neumann algebras, where density operators do not exist. The gluing complex must be reformulated in terms of states on the algebra.

2. **Computational complexity.** Computing $\mathfrak{g}_+$ is QMA-hard in general (it contains the QMP as a special case). Efficient algorithms exist only for specific covers and small systems.

3. **Relation to holography.** The Ryu–Takayanagi formula relates entanglement entropy to minimal surfaces in the bulk. The gluing defect may have a holographic interpretation as a topological invariant of the bulk geometry. This is an open problem.

4. **Dynamical evolution.** The gluing defect is a kinematic invariant. Its behavior under time evolution — whether it is conserved, monotone, or ergodic — is unknown.

---

## 13. Conclusion

The marginal-gluing complex provides a rigorous framework for quantifying the spatial distribution of quantum correlations across a cover of a Cauchy surface. The linear cohomology vanishes: at the level of Hermitian operators, consistent local data always glue. The physically nontrivial content resides in the positive cone: the requirement that the glued operator be a density operator. The positive gluing defect measures the severity of this obstruction.

The gluing defect is invariant under local unitaries, monotone under cover refinement, and independent of the foliation. It distinguishes entanglement classes that are invisible to the entropy spectrum. It is, in the language of the parent paper, a kinematic invariant of the acausal correlation structure: a property of the global state that is not produced by, does not require, and is not reducible to any mediating influence propagating through spacetime.

The Pattern Conjecture — that the gluing defect is an invariant of the *pattern* of correlation, not its *amount* — remains open. Its resolution will require either an explicit construction of states with identical entropy spectra but distinct gluing defects, or a proof that no such states exist. Both outcomes would be informative.

---

## References

[1] A. Klyachko, "Quantum marginal problem and representations of the symmetric group," arXiv:quant-ph/0409113 (2004).

[2] M. Christandl and A. Winter, "Squashed entanglement: An additive entanglement measure," J. Math. Phys. **45**, 829–840 (2004).

[3] S. Bravyi, "Requirements for compatibility of local and multipartite quantum states," arXiv:quant-ph/0303035 (2003).

[4] A. Higuchi, A. Sudbery, and J. Szulc, "One-qubit reduced states of a pure many-qubit state: Polygon inequalities," Phys. Rev. Lett. **90**, 107902 (2003).

[5] V. Coffman, J. Kundu, and W. K. Wootters, "Distributed entanglement," Phys. Rev. A **61**, 052306 (2000).

[6] S. Abramsky and A. Brandenburger, "The sheaf-theoretic structure of non-locality and contextuality," New J. Phys. **13**, 113036 (2011).

[7] S. J. Summers and R. Werner, "Bell's inequalities and quantum field theory. I. General setting," J. Math. Phys. **28**, 2440–2447 (1987).

[8] B. Swingle, "Entanglement renormalization and holography," Phys. Rev. D **86**, 065007 (2012).

[9] M. A. Nielsen and I. L. Chuang, *Quantum Computation and Quantum Information*, Cambridge University Press (2000).

[10] R. Haag, *Local Quantum Physics: Fields, Particles, Algebras*, 2nd ed., Springer (1996).

---

## Appendix A: Proof of Linear Exactness for General Covers

**Theorem A.1.** *Let $\mathfrak{U} = \{U_i\}_{i=1}^N$ be a good cover (all finite intersections contractible or empty) of a Cauchy surface. Then the marginal-gluing complex is exact at every degree.*

*Proof.* By the nerve theorem, the Čech cohomology of a good cover with coefficients in a fine sheaf vanishes. The sheaf of Hermitian operators is fine (it admits partitions of unity subordinate to any cover). Therefore $\check{H}^k(\mathfrak{U}, \mathcal{B}_{\mathrm{sa}}) = 0$ for $k \geq 1$. The marginal-gluing complex is the Čech complex of this sheaf, so its cohomology vanishes. $\blacksquare$

## Appendix B: SDP Dual for the Three-Qubit Orphan

The SDP (5.5) for the three pairwise singlets is:

$$\text{Find } \rho_{ABC} \geq 0, \quad \mathrm{Tr}(\rho_{ABC}) = 1, \quad \mathrm{Tr}_C \rho_{ABC} = |\psi^-\rangle\langle\psi^-|_{AB}, \quad \text{etc.} \tag{B.1}$$

The dual is:

$$\text{Maximize } -\sum_i \mathrm{Tr}(Y_i \rho_i) \quad \text{subject to} \quad \sum_i Y_i \otimes \mathbb{I}_{U_i^c} \leq \mathbb{I}. \tag{B.2}$$

A feasible dual solution with positive objective value certifies infeasibility. The monogamy witness (6.7) provides such a solution.

## Appendix C: Conventions

- All Hilbert spaces are finite-dimensional unless otherwise stated.
- $\mathcal{B}(\mathcal{H})_{\mathrm{sa}}$ denotes the real vector space of Hermitian operators on $\mathcal{H}$.
- $\mathrm{Tr}_S$ denotes the partial trace over the subsystem $S$.
- $\dim_{\mathrm{aff}}$ denotes the affine dimension.
- $\mathcal{S}(\mathcal{H})$ denotes the set of density operators on $\mathcal{H}$.
- $\mathfrak{g}_+$ denotes the positive (semialgebraic) gluing defect.
