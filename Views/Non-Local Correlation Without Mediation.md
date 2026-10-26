# Non-Local Correlation Without Mediation: The Acausal Structure of Quantum Entanglement and the Integrity of Relativistic Causality

---

**Author:** Marlon Hanks
**Affiliation:** Dust LLC
**Date:** October 26, 2026

---

## Abstract

We present a rigorous analysis establishing that the non-local correlations exhibited by entangled quantum systems are not mediated by any physical process propagating through spacetime, while causal influence remains strictly local and compatible with the relativistic light-cone structure. We formalize this thesis through three independent and mutually reinforcing arguments: (i) a complete derivation of Bell's theorem and the CHSH inequality demonstrating the impossibility of local-causal explanations for quantum correlations; (ii) a proof of the no-signaling theorem showing that the reduced density operator of any subsystem is invariant under arbitrary operations performed on spacelike-separated subsystems, thereby excluding superluminal causal influence; and (iii) an analysis of the microcausality condition in relativistic quantum field theory, $[\hat{\mathcal{O}}(x),\hat{\mathcal{O}}(y)] = 0$ for spacelike-separated $x, y$, which enforces the locality of all dynamical interactions while the vacuum state itself exhibits non-local entanglement structure. We introduce a formal decomposition of physical theory into kinematic, dynamical, and causal sectors, and demonstrate that quantum non-local correlations reside entirely in the kinematic sector—encoded in the global state vector—while the dynamical and causal sectors remain strictly local. This decomposition resolves the apparent tension between Bell non-locality and relativistic causality: the universe possesses non-separable correlation structures that are not produced by, do not require, and are not reducible to any mediating influence traversing the interval between correlated events. We further analyze the Tsirelson bound, the geometry of the no-signaling polytope, and the Reeh–Schlieder theorem to characterize precisely the domain and limits of acausal correlation. The result is a coherent ontological picture in which the fabric of physical reality includes irreducibly global, acausal correlation structures coexisting with strictly local causal dynamics.

**PACS:** 03.65.Ud, 03.65.Ta, 03.70.+k, 11.10.Cd
**MSC:** 81P40, 81P15, 81T05, 83A05
**Keywords:** quantum entanglement, Bell non-locality, no-signaling theorem, microcausality, relativistic quantum field theory, Tsirelson bound, quantum foundations

---

## 1. Introduction

The central empirical fact of quantum foundations is this: measurements performed on spacelike-separated subsystems of an entangled quantum state exhibit statistical correlations that cannot be reproduced by any theory in which the outcomes are determined by local variables associated with each subsystem independently. This is the content of Bell's theorem [1], confirmed experimentally with increasing precision from the pioneering work of Freedman and Clauser [2] through the Aspect experiments [3] to the loophole-free tests of Hensen et al. [4], Giustina et al. [5], and Shalm et al. [6].

Yet simultaneously, and with equal empirical certainty, no experiment has ever demonstrated the transmission of a signal, a force, or any form of controllable causal influence faster than light. The reduced statistics observed by any observer are independent of the measurement choices made at spacelike separation. This is the content of the no-signaling theorem [7, 8], which is not a contingent empirical regularity but a structural consequence of the tensor-product architecture of quantum mechanics.

The coexistence of these two facts—non-local correlation and local causality—is not a paradox to be resolved by eliminating one or the other. It is a structural feature of physical reality that demands precise characterization. The purpose of this paper is to provide that characterization.

Our thesis is the following:

> **Thesis.** *The non-local correlations of quantum mechanics are not mediated by any entity, signal, influence, or process propagating through spacetime between the correlated events. They are structural features of the global quantum state, encoded at the level of kinematics rather than dynamics. Causal influence, by contrast, is governed by the dynamical and relativistic structure of the theory and remains strictly local, confined within the forward light cone. The universe therefore contains irreducibly non-local, acausal correlations coexisting with strictly local causal dynamics.*

This thesis is not new in its individual components. What is new is the systematic formal framework we develop here, which decomposes physical theory into three distinct sectors—kinematic, dynamical, and causal—and demonstrates that the apparent tension between Bell non-locality and relativistic causality dissolves once one recognizes that these sectors carry independent structural content. The non-local correlations belong to the kinematic sector; causal propagation belongs to the dynamical and causal sectors. There is no contradiction because there is no overlap.

The paper is organized as follows. In Section 2, we establish the formal framework: Hilbert spaces, tensor products, quantum states, and measurements. In Section 3, we derive Bell's theorem and the CHSH inequality in full detail, establishing the impossibility of local hidden-variable explanations. In Section 4, we prove the no-signaling theorem in its general form. In Section 5, we analyze the structure of entangled correlations and demonstrate their acausal, non-mediated character. In Section 6, we examine the microcausality condition in relativistic quantum field theory and the Reeh–Schlieder theorem. In Section 7, we introduce the kinematic/dynamical/causal decomposition and show how it resolves the apparent tension. In Section 8, we analyze the Tsirelson bound and the geometry of the no-signaling polytope. In Section 9, we discuss interpretive implications. Section 10 concludes.

---

## 2. Formal Framework

### 2.1 Hilbert Space Structure and Tensor Products

Let $\mathcal{H}_A$ and $\mathcal{H}_B$ be the Hilbert spaces associated with two physical subsystems $A$ and $B$. The joint system is described by the tensor product

$$\mathcal{H}_{AB} = \mathcal{H}_A \otimes \mathcal{H}_B. \tag{2.1}$$

A pure state of the joint system is a normalized vector $|\psi\rangle \in \mathcal{H}_{AB}$, $\langle\psi|\psi\rangle = 1$. A general (possibly mixed) state is described by a density operator $\rho_{AB}$ acting on $\mathcal{H}_{AB}$, satisfying

$$\rho_{AB} \geq 0, \qquad \mathrm{Tr}(\rho_{AB}) = 1. \tag{2.2}$$

The state $\rho_{AB}$ is **separable** if it admits a convex decomposition

$$\rho_{AB} = \sum_i p_i \, \rho_A^{(i)} \otimes \rho_B^{(i)}, \qquad p_i \geq 0, \quad \sum_i p_i = 1, \tag{2.3}$$

where $\rho_A^{(i)}$ and $\rho_B^{(i)}$ are density operators on $\mathcal{H}_A$ and $\mathcal{H}_B$ respectively. A state that is not separable is **entangled**.

For a pure state $|\psi\rangle \in \mathcal{H}_A \otimes \mathcal{H}_B$, entanglement is equivalent to the failure of factorizability: $|\psi\rangle \neq |\phi_A\rangle \otimes |\chi_B\rangle$ for any $|\phi_A\rangle \in \mathcal{H}_A$, $|\chi_B\rangle \in \mathcal{H}_B$.

### 2.2 The Schmidt Decomposition

Any pure bipartite state $|\psi\rangle \in \mathcal{H}_A \otimes \mathcal{H}_B$ with $\dim(\mathcal{H}_A) = d_A$, $\dim(\mathcal{H}_B) = d_B$ admits a Schmidt decomposition [9]:

$$|\psi\rangle = \sum_{k=1}^{r} \sqrt{\lambda_k} \, |e_k\rangle_A \otimes |f_k\rangle_B, \tag{2.4}$$

where $\{|e_k\rangle_A\}$ and $\{|f_k\rangle_B\}$ are orthonormal sets in $\mathcal{H}_A$ and $\mathcal{H}_B$ respectively, $\lambda_k > 0$, $\sum_k \lambda_k = 1$, and $r \leq \min(d_A, d_B)$ is the **Schmidt rank**. The state is entangled if and only if $r > 1$.

The reduced density operators are obtained by partial trace:

$$\rho_A = \mathrm{Tr}_B(|\psi\rangle\langle\psi|) = \sum_{k=1}^r \lambda_k |e_k\rangle\langle e_k|, \tag{2.5}$$

$$\rho_B = \mathrm{Tr}_A(|\psi\rangle\langle\psi|) = \sum_{k=1}^r \lambda_k |f_k\rangle\langle f_k|. \tag{2.6}$$

The entanglement entropy $S(\rho_A) = S(\rho_B) = -\sum_k \lambda_k \ln \lambda_k$ quantifies the degree of entanglement for pure states.

### 2.3 Measurements and POVMs

A general measurement on subsystem $A$ is described by a positive operator-valued measure (POVM) $\{M_a^{(\alpha)}\}$, indexed by measurement setting $\alpha$ and outcome $a$, satisfying

$$M_a^{(\alpha)} \geq 0, \qquad \sum_a M_a^{(\alpha)} = \mathbb{I}_A. \tag{2.7}$$

Similarly, a measurement on subsystem $B$ with setting $\beta$ and outcome $b$ is described by $\{N_b^{(\beta)}\}$ with

$$N_b^{(\beta)} \geq 0, \qquad \sum_b N_b^{(\beta)} = \mathbb{I}_B. \tag{2.8}$$

The joint probability of obtaining outcomes $a$ and $b$ given settings $\alpha$ and $\beta$ is

$$P(a, b \mid \alpha, \beta) = \mathrm{Tr}\!\left[\rho_{AB} \left(M_a^{(\alpha)} \otimes N_b^{(\beta)}\right)\right]. \tag{2.9}$$

This is the central object of our analysis. The question is whether this joint probability can be decomposed in a manner consistent with local causality.

---

## 3. Bell's Theorem and the Failure of Local Causal Explanation

### 3.1 The Local Hidden Variable Framework

We now formalize the notion that the correlations $P(a, b \mid \alpha, \beta)$ might be explained by a local causal mechanism. Following Bell [1], suppose there exists a set of hidden variables $\lambda$, distributed according to a probability measure $\mu(\lambda)$, such that:

**Assumption 1 (Realism/Definiteness).** The outcomes $a$ and $b$ are determined (stochastically or deterministically) by the hidden variable $\lambda$ together with the local measurement settings.

**Assumption 2 (Locality/Parameter Independence).** The probability distribution for Alice's outcome depends only on Alice's setting and $\lambda$, not on Bob's setting $\beta$; and vice versa:

$$P(a \mid \alpha, \beta, \lambda) = P(a \mid \alpha, \lambda), \tag{3.1}$$
$$P(b \mid \alpha, \beta, \lambda) = P(b \mid \beta, \lambda). \tag{3.2}$$

**Assumption 3 (Outcome Independence / Factorizability).** Conditional on $\lambda$, the outcomes are statistically independent:

$$P(a, b \mid \alpha, \beta, \lambda) = P(a \mid \alpha, \lambda) \, P(b \mid \beta, \lambda). \tag{3.3}$$

**Assumption 4 (Measurement Independence / Freedom of Choice).** The hidden variable $\lambda$ is statistically independent of the measurement settings:

$$\mu(\lambda \mid \alpha, \beta) = \mu(\lambda). \tag{3.4}$$

Under these assumptions, the joint probability takes the form

$$P(a, b \mid \alpha, \beta) = \int d\lambda \, \mu(\lambda) \, P(a \mid \alpha, \lambda) \, P(b \mid \beta, \lambda). \tag{3.5}$$

This is the **local hidden variable (LHV)** or **local causal** decomposition. Any theory satisfying (3.1)–(3.4) must produce correlations of this form.

### 3.2 The CHSH Inequality

Specialize to the case where each party has two binary-outcome measurements. Alice chooses setting $\alpha \in \{0, 1\}$ and obtains outcome $A_\alpha \in \{-1, +1\}$. Bob chooses setting $\beta \in \{0, 1\}$ and obtains outcome $B_\beta \in \{-1, +1\}$.

Define the correlation function

$$E(\alpha, \beta) = \sum_{a, b} a \, b \, P(a, b \mid \alpha, \beta) = \langle A_\alpha B_\beta \rangle. \tag{3.6}$$

**Theorem 3.1 (CHSH Inequality [10]).** *Under the local hidden variable assumptions (3.1)–(3.4), the CHSH quantity*

$$S = E(0,0) + E(0,1) + E(1,0) - E(1,1) \tag{3.7}$$

*satisfies*

$$|S| \leq 2. \tag{3.8}$$

*Proof.* Under the LHV model (3.5), we have

$$E(\alpha, \beta) = \int d\lambda \, \mu(\lambda) \, \bar{A}_\alpha(\lambda) \, \bar{B}_\beta(\lambda), \tag{3.9}$$

where $\bar{A}_\alpha(\lambda) = \sum_a a \, P(a \mid \alpha, \lambda)$ and $\bar{B}_\beta(\lambda) = \sum_b b \, P(b \mid \beta, \lambda)$ satisfy $|\bar{A}_\alpha(\lambda)| \leq 1$ and $|\bar{B}_\beta(\lambda)| \leq 1$.

Then

$$S = \int d\lambda \, \mu(\lambda) \left[\bar{A}_0(\lambda)\bar{B}_0(\lambda) + \bar{A}_0(\lambda)\bar{B}_1(\lambda) + \bar{A}_1(\lambda)\bar{B}_0(\lambda) - \bar{A}_1(\lambda)\bar{B}_1(\lambda)\right]. \tag{3.10}$$

Factoring:

$$S = \int d\lambda \, \mu(\lambda) \left[\bar{A}_0(\lambda)\left(\bar{B}_0(\lambda) + \bar{B}_1(\lambda)\right) + \bar{A}_1(\lambda)\left(\bar{B}_0(\lambda) - \bar{B}_1(\lambda)\right)\right]. \tag{3.11}$$

For each $\lambda$, since $\bar{B}_0, \bar{B}_1 \in [-1, 1]$, either $|\bar{B}_0 + \bar{B}_1| \leq 2$ and $|\bar{B}_0 - \bar{B}_1| \leq 2$, but more precisely, one of $|\bar{B}_0 + \bar{B}_1|$ or $|\bar{B}_0 - \bar{B}_1|$ is $\leq 2$ while the other could be up to 2. However, since $|\bar{A}_0|, |\bar{A}_1| \leq 1$, the integrand satisfies

$$\left|\bar{A}_0(\bar{B}_0 + \bar{B}_1) + \bar{A}_1(\bar{B}_0 - \bar{B}_1)\right| \leq |\bar{B}_0 + \bar{B}_1| + |\bar{B}_0 - \bar{B}_1| \leq 2. \tag{3.12}$$

The last inequality follows because for any $x, y \in [-1,1]$, $|x+y| + |x-y| \leq 2$. Therefore

$$|S| \leq \int d\lambda \, \mu(\lambda) \cdot 2 = 2. \qquad \blacksquare \tag{3.13}$$

### 3.3 Quantum Violation: The Singlet State

Consider two spin-$\frac{1}{2}$ particles in the singlet state

$$|\psi^-\rangle = \frac{1}{\sqrt{2}}\left(|\uparrow\rangle_A \otimes |\downarrow\rangle_B - |\downarrow\rangle_A \otimes |\uparrow\rangle_B\right). \tag{3.14}$$

In the computational basis $\{|0\rangle, |1\rangle\}$:

$$|\psi^-\rangle = \frac{1}{\sqrt{2}}\left(|0\rangle_A |1\rangle_B - |1\rangle_A |0\rangle_B\right). \tag{3.15}$$

This state has Schmidt rank $r = 2$ with $\lambda_1 = \lambda_2 = 1/2$, and is maximally entangled.

Alice measures spin along direction $\mathbf{a} \in \mathbb{R}^3$, $|\mathbf{a}| = 1$, with observable $\hat{A} = \boldsymbol{\sigma} \cdot \mathbf{a}$, where $\boldsymbol{\sigma} = (\sigma_x, \sigma_y, \sigma_z)$ are the Pauli matrices. Bob measures along $\mathbf{b}$ with $\hat{B} = \boldsymbol{\sigma} \cdot \mathbf{b}$.

The quantum correlation is

$$E(\mathbf{a}, \mathbf{b}) = \langle \psi^- | (\boldsymbol{\sigma} \cdot \mathbf{a}) \otimes (\boldsymbol{\sigma} \cdot \mathbf{b}) | \psi^- \rangle. \tag{3.16}$$

**Proposition 3.2.** *For the singlet state (3.15),*

$$E(\mathbf{a}, \mathbf{b}) = -\mathbf{a} \cdot \mathbf{b}. \tag{3.17}$$

*Proof.* We compute using the identity $\sigma_i \sigma_j = \delta_{ij}\mathbb{I} + i\epsilon_{ijk}\sigma_k$ and the fact that $\langle\psi^-|\sigma_i \otimes \sigma_j|\psi^-\rangle = -\delta_{ij}$.

The singlet is rotationally invariant: $(U \otimes U)|\psi^-\rangle = |\psi^-\rangle$ for any $U \in SU(2)$. Therefore $\langle\psi^-|\sigma_i \otimes \sigma_j|\psi^-\rangle$ must be proportional to $\delta_{ij}$. The proportionality constant is determined by evaluating $i = j = z$:

$$\langle\psi^-|\sigma_z \otimes \sigma_z|\psi^-\rangle = \frac{1}{2}\left[\langle 01| - \langle 10|\right]\sigma_z \otimes \sigma_z\left[|01\rangle - |10\rangle\right]. \tag{3.18}$$

Since $\sigma_z|0\rangle = |0\rangle$ and $\sigma_z|1\rangle = -|1\rangle$:

$$\sigma_z \otimes \sigma_z |01\rangle = -|01\rangle, \qquad \sigma_z \otimes \sigma_z |10\rangle = -|10\rangle. \tag{3.19}$$

Therefore

$$\langle\psi^-|\sigma_z \otimes \sigma_z|\psi^-\rangle = \frac{1}{2}\left[\langle 01| - \langle 10|\right]\left[-|01\rangle + |10\rangle\right] = \frac{1}{2}(-1 - 1) = -1. \tag{3.20}$$

Thus $\langle\psi^-|\sigma_i \otimes \sigma_j|\psi^-\rangle = -\delta_{ij}$, and

$$E(\mathbf{a}, \mathbf{b}) = -\sum_{i,j} a_i b_j \delta_{ij} = -\mathbf{a} \cdot \mathbf{b}. \qquad \blacksquare \tag{3.21}$$

### 3.4 Maximal Violation of CHSH

Choose measurement directions:

$$\mathbf{a}_0 = \hat{z}, \quad \mathbf{a}_1 = \hat{x}, \quad \mathbf{b}_0 = \frac{\hat{z} + \hat{x}}{\sqrt{2}}, \quad \mathbf{b}_1 = \frac{\hat{z} - \hat{x}}{\sqrt{2}}. \tag{3.22}$$

Then:

$$E(\mathbf{a}_0, \mathbf{b}_0) = -\frac{1}{\sqrt{2}}, \quad E(\mathbf{a}_0, \mathbf{b}_1) = -\frac{1}{\sqrt{2}}, \tag{3.23}$$
$$E(\mathbf{a}_1, \mathbf{b}_0) = -\frac{1}{\sqrt{2}}, \quad E(\mathbf{a}_1, \mathbf{b}_1) = +\frac{1}{\sqrt{2}}. \tag{3.24}$$

The CHSH quantity is

$$S = -\frac{1}{\sqrt{2}} - \frac{1}{\sqrt{2}} - \frac{1}{\sqrt{2}} - \frac{1}{\sqrt{2}} = -\frac{4}{\sqrt{2}} = -2\sqrt{2}. \tag{3.25}$$

Therefore $|S| = 2\sqrt{2} \approx 2.828 > 2$.

The CHSH inequality is violated. No local hidden variable theory satisfying Assumptions 1–4 can reproduce the quantum predictions. This is not a limitation of current technology; it is a theorem about the structure of physical reality, confirmed experimentally to high statistical significance [4–6].

### 3.5 The Implication

Bell's theorem forces the abandonment of at least one of the Assumptions 1–4. The assumptions are:

- **Realism**: outcomes are determined by pre-existing properties.
- **Locality**: no dependence on distant settings.
- **Outcome independence**: conditional statistical independence.
- **Measurement independence**: freedom of choice.

The standard quantum mechanical resolution is to abandon Realism (Assumption 1) in its naive form: the outcomes are not determined by pre-existing local properties. But crucially, as we now demonstrate, this does not require the abandonment of relativistic causality.

---

## 4. The No-Signaling Theorem

### 4.1 Statement and Proof

The no-signaling theorem establishes that the statistics of measurements performed by Bob are completely independent of the measurement choice made by Alice, when Alice and Bob are spacelike separated. This is the formal expression of the principle that no causal influence propagates from Alice to Bob through the entangled state.

**Theorem 4.1 (No-Signaling).** *Let $\rho_{AB}$ be any bipartite state on $\mathcal{H}_A \otimes \mathcal{H}_B$. Let Alice perform any measurement described by POVM $\{M_a^{(\alpha)}\}$ with setting $\alpha$, obtaining outcome $a$. Then Bob's reduced state, averaged over Alice's outcomes, is independent of Alice's measurement choice $\alpha$:*

$$\rho_B' = \sum_a \mathrm{Tr}_A\!\left[\left(M_a^{(\alpha)} \otimes \mathbb{I}_B\right) \rho_{AB} \left(M_a^{(\alpha)} \otimes \mathbb{I}_B\right)^\dagger\right] = \mathrm{Tr}_A(\rho_{AB}) = \rho_B. \tag{4.1}$$

*More generally, for any POVM (not necessarily projective), Bob's marginal state is unchanged.*

*Proof.* We prove the result for a general POVM. Alice's measurement with setting $\alpha$ has Kraus operators $\{K_a^{(\alpha)}\}$ satisfying $\sum_a (K_a^{(\alpha)})^\dagger K_a^{(\alpha)} = \mathbb{I}_A$. Upon obtaining outcome $a$, the (unnormalized) post-measurement state is

$$\tilde{\rho}_{AB}^{(a)} = \left(K_a^{(\alpha)} \otimes \mathbb{I}_B\right) \rho_{AB} \left(K_a^{(\alpha)} \otimes \mathbb{I}_B\right)^\dagger. \tag{4.2}$$

If Alice does not communicate her outcome to Bob, Bob's state is obtained by summing over all outcomes and tracing out $A$:

$$\rho_B' = \sum_a \mathrm{Tr}_A\!\left[\left(K_a^{(\alpha)} \otimes \mathbb{I}_B\right) \rho_{AB} \left((K_a^{(\alpha)})^\dagger \otimes \mathbb{I}_B\right)\right]. \tag{4.3}$$

We now evaluate this. Write $\rho_{AB}$ in a product basis:

$$\rho_{AB} = \sum_{i,j,k,l} \rho_{ik,jl} \, |i\rangle_A\langle j| \otimes |k\rangle_B\langle l|. \tag{4.4}$$

Then

$$\rho_B' = \sum_a \sum_{i,j,k,l} \rho_{ik,jl} \, \mathrm{Tr}_A\!\left[K_a^{(\alpha)} |i\rangle\langle j| (K_a^{(\alpha)})^\dagger\right] \otimes |k\rangle\langle l|. \tag{4.5}$$

The partial trace gives

$$\mathrm{Tr}_A\!\left[K_a^{(\alpha)} |i\rangle\langle j| (K_a^{(\alpha)})^\dagger\right] = \langle j | (K_a^{(\alpha)})^\dagger K_a^{(\alpha)} | i \rangle. \tag{4.6}$$

Summing over outcomes $a$:

$$\sum_a \langle j | (K_a^{(\alpha)})^\dagger K_a^{(\alpha)} | i \rangle = \langle j | \mathbb{I}_A | i \rangle = \delta_{ij}. \tag{4.7}$$

Therefore

$$\rho_B' = \sum_{i,k,l} \rho_{ik,il} \, |k\rangle\langle l| = \mathrm{Tr}_A(\rho_{AB}) = \rho_B. \qquad \blacksquare \tag{4.8}$$

The result is independent of $\alpha$. Bob cannot determine which measurement Alice chose by any local observation.

### 4.2 Marginal Probabilities

An equivalent and operationally transparent statement: the marginal probability of Bob's outcome $b$ given his setting $\beta$ is independent of Alice's setting $\alpha$:

$$P(b \mid \beta) = \sum_a P(a, b \mid \alpha, \beta) = \sum_a \mathrm{Tr}\!\left[\rho_{AB}\left(M_a^{(\alpha)} \otimes N_b^{(\beta)}\right)\right]. \tag{4.9}$$

Using $\sum_a M_a^{(\alpha)} = \mathbb{I}_A$:

$$P(b \mid \beta) = \mathrm{Tr}\!\left[\rho_{AB}\left(\mathbb{I}_A \otimes N_b^{(\beta)}\right)\right] = \mathrm{Tr}_B\!\left[\rho_B \, N_b^{(\beta)}\right]. \tag{4.10}$$

This is manifestly independent of $\alpha$. Similarly, $P(a \mid \alpha)$ is independent of $\beta$.

### 4.3 The Distinction: Correlation vs. Causation

The no-signaling theorem establishes the following precise distinction:

- **Correlation**: $P(a, b \mid \alpha, \beta) \neq P(a \mid \alpha) \, P(b \mid \beta)$ in general. The joint statistics are correlated, and these correlations violate Bell inequalities.

- **Causation (signaling)**: $P(b \mid \alpha, \beta) = P(b \mid \beta)$ for all $\alpha$. Bob's local statistics are unaffected by Alice's choice. There is no causal channel from Alice to Bob.

The correlations are real. They are measurable. They violate Bell inequalities. But they cannot be used to transmit information, exert force, or produce any controllable causal effect at spacelike separation. The correlations are **acausal** in the precise operational sense that they do not constitute a channel for causal influence.

---

## 5. The Structure of Entangled Correlations: Non-Locality Without Mediation

### 5.1 The Correlations Are Not Produced by Propagation

We now address the central question: if the correlations are not mediated by any signal propagating from $A$ to $B$ (or vice versa), what is their origin?

The answer, in the formalism of quantum mechanics, is that the correlations are encoded in the global state $|\psi\rangle \in \mathcal{H}_A \otimes \mathcal{H}_B$ at the moment of preparation. They are a property of the state vector itself, not of any dynamical process connecting the measurement events.

Consider the singlet state (3.15). Before any measurement is performed, the state $|\psi^-\rangle$ already encodes the correlation structure: for any direction $\mathbf{n}$, if Alice measures $\boldsymbol{\sigma} \cdot \mathbf{n}$ and obtains $+1$, then Bob will obtain $-1$ if he measures along the same direction. This perfect anti-correlation is a property of $|\psi^-\rangle$, not of any signal sent from Alice to Bob at the moment of measurement.

Formally, the singlet state can be written as

$$|\psi^-\rangle = \frac{1}{\sqrt{2}}\left(|\mathbf{n},+\rangle_A |\mathbf{n},-\rangle_B - |\mathbf{n},-\rangle_A |\mathbf{n},+\rangle_B\right) \tag{5.1}$$

for **any** direction $\mathbf{n}$. This rotational invariance means the correlation structure is not tied to any particular measurement basis. It is a global, basis-independent property of the state.

### 5.2 The Measurement Does Not Create the Correlation

A common but misleading narrative is that Alice's measurement "collapses" Bob's state instantaneously, thereby creating the correlation. This narrative is incorrect in two senses:

**First**, the no-signaling theorem (Theorem 4.1) shows that Bob's reduced state $\rho_B$ is unchanged by Alice's measurement. If Alice measures and obtains outcome $a$, then conditional on that outcome, Bob's state is updated to

$$\rho_B^{(a)} = \frac{\mathrm{Tr}_A\!\left[\left(M_a^{(\alpha)} \otimes \mathbb{I}_B\right)\rho_{AB}\right]}{P(a \mid \alpha)}. \tag{5.2}$$

But Bob does not know $a$ unless Alice communicates it classically. Averaged over $a$, Bob's state is $\rho_B$, unchanged. The "collapse" is an update of Alice's knowledge, not a physical process acting on Bob's system.

**Second**, the correlations were already present in the joint state before measurement. The measurement does not create the correlation; it reveals it. The joint probability $P(a, b \mid \alpha, \beta)$ is determined by $\rho_{AB}$ and the measurement operators via Eq. (2.9). No dynamical process connecting the two measurement events enters the calculation.

### 5.3 The Correlations Are Not Carried by Any Field or Particle

In a relativistic theory, causal influence is mediated by fields propagating on spacetime, subject to the constraint that signals travel within or on the light cone. The correlations of entangled states are not mediated by any such field.

To see this, note that the correlation $E(\mathbf{a}, \mathbf{b}) = -\mathbf{a} \cdot \mathbf{b}$ for the singlet state depends only on the relative angle between the measurement directions. It does not depend on the spatial separation between Alice and Bob, the time elapsed since preparation, or any property of the intervening spacetime. The correlation is the same whether Alice and Bob are separated by 1 meter or 1 light-year, provided the entangled state is preserved.

If the correlation were mediated by a field propagating from Alice to Bob, it would need to:
1. Carry information about Alice's measurement setting $\mathbf{a}$ to Bob.
2. Do so faster than light (since the measurements are spacelike separated).
3. Do so without being detectable as a signal (since no-signaling holds).

No known or conceivable field satisfies all three conditions simultaneously. The resolution is simpler: no field mediates the correlation. The correlation is a property of the global state.

### 5.4 Formal Characterization: The Correlation Tensor

For a bipartite state $\rho_{AB}$ on $\mathcal{H}_A \otimes \mathcal{H}_B$ with $\dim(\mathcal{H}_A) = \dim(\mathcal{H}_B) = d$, we may expand in a basis of traceless Hermitian generators $\{\lambda_i\}_{i=1}^{d^2-1}$ of $\mathfrak{su}(d)$, normalized so that $\mathrm{Tr}(\lambda_i \lambda_j) = 2\delta_{ij}$:

$$\rho_{AB} = \frac{1}{d^2}\left(\mathbb{I} \otimes \mathbb{I} + \sum_i r_i \, \lambda_i \otimes \mathbb{I} + \sum_j s_j \, \mathbb{I} \otimes \lambda_j + \sum_{i,j} T_{ij} \, \lambda_i \otimes \lambda_j\right). \tag{5.3}$$

Here $r_i = \frac{d}{2}\mathrm{Tr}(\rho_{AB}(\lambda_i \otimes \mathbb{I}))$ and $s_j = \frac{d}{2}\mathrm{Tr}(\rho_{AB}(\mathbb{I} \otimes \lambda_j))$ are the local Bloch vectors, and

$$T_{ij} = \frac{d}{2}\mathrm{Tr}\!\left(\rho_{AB}(\lambda_i \otimes \lambda_j)\right) \tag{5.4}$$

is the **correlation tensor**. The correlation tensor $T_{ij}$ encodes all non-local correlations. It is a property of the state $\rho_{AB}$, not of any dynamical process.

For the singlet state of two qubits ($d = 2$, $\lambda_i = \sigma_i$), we have $r_i = s_j = 0$ and

$$T_{ij} = -\delta_{ij}. \tag{5.5}$$

The entire correlation structure is captured by this single tensor. No propagation, no mediation, no dynamical process is involved.

---

## 6. Relativistic Quantum Field Theory: Microcausality and Vacuum Entanglement

### 6.1 The Microcausality Condition

In relativistic quantum field theory (QFT), the principle of local causality is implemented by the **microcausality** (or **local commutativity**) condition. Let $\hat{\mathcal{O}}_1(x)$ and $\hat{\mathcal{O}}_2(y)$ be local observables associated with spacetime points $x$ and $y$. Then

$$[\hat{\mathcal{O}}_1(x), \hat{\mathcal{O}}_2(y)] = 0 \quad \text{whenever} \quad (x - y)^2 < 0, \tag{6.1}$$

i.e., whenever $x$ and $y$ are spacelike separated. Here $(x-y)^2 = \eta_{\mu\nu}(x-y)^\mu(x-y)^\nu$ with metric signature $(+,-,-,-)$.

This condition ensures that measurements performed at spacelike separation cannot influence each other. The algebra of observables associated with a spacetime region $\mathcal{R}$, denoted $\mathcal{A}(\mathcal{R})$, satisfies

$$\mathcal{A}(\mathcal{R}_1) \subset \mathcal{A}(\mathcal{R}_2)' \quad \text{if} \quad \mathcal{R}_1 \text{ and } \mathcal{R}_2 \text{ are spacelike separated}, \tag{6.2}$$

where $\mathcal{A}(\mathcal{R}_2)'$ is the commutant of $\mathcal{A}(\mathcal{R}_2)$. This is the algebraic formulation of Einstein causality [11].

### 6.2 Microcausality and the No-Signaling Theorem in QFT

The microcausality condition directly implies the no-signaling theorem in the QFT context. Let $\mathcal{R}_A$ and $\mathcal{R}_B$ be spacelike-separated regions. Any operation Alice performs in $\mathcal{R}_A$ is represented by an element of $\mathcal{A}(\mathcal{R}_A)$. Any observable Bob measures in $\mathcal{R}_B$ is an element of $\mathcal{A}(\mathcal{R}_B)$. By microcausality, these commute:

$$[A, B] = 0 \quad \forall A \in \mathcal{A}(\mathcal{R}_A), \; B \in \mathcal{A}(\mathcal{R}_B). \tag{6.3}$$

Therefore, the expectation value of Bob's observable is unaffected by Alice's operation:

$$\langle \psi | U_A^\dagger B U_A | \psi \rangle = \langle \psi | B | \psi \rangle, \tag{6.4}$$

where $U_A \in \mathcal{A}(\mathcal{R}_A)$ is Alice's unitary operation. This follows because $[U_A, B] = 0$.

More generally, for a POVM with Kraus operators $K_a \in \mathcal{A}(\mathcal{R}_A)$:

$$\sum_a \mathrm{Tr}\!\left[K_a^\dagger B K_a \rho\right] = \mathrm{Tr}\!\left[B \sum_a K_a K_a^\dagger \rho\right] = \mathrm{Tr}[B\rho], \tag{6.5}$$

where we used $[K_a, B] = 0$ and $\sum_a K_a^\dagger K_a = \mathbb{I}$.

### 6.3 The Reeh–Schlieder Theorem: Vacuum Entanglement

The vacuum state $|0\rangle$ of a relativistic QFT is not a product state across spatial regions. The **Reeh–Schlieder theorem** [12] states:

**Theorem 6.1 (Reeh–Schlieder).** *Let $\mathcal{R}$ be any open region of Minkowski spacetime. The set of states $\mathcal{A}(\mathcal{R})|0\rangle$, obtained by acting on the vacuum with operators localized in $\mathcal{R}$, is dense in the full Hilbert space $\mathcal{H}$.*

This means the vacuum is highly entangled across any spatial partition. For any two spacelike-separated regions $\mathcal{R}_1$ and $\mathcal{R}_2$, the vacuum state $|0\rangle$ restricted to $\mathcal{R}_1 \cup \mathcal{R}_2$ is generically entangled. The vacuum correlations are non-local in the Bell sense: they violate Bell inequalities [13, 14].

Yet the vacuum is the state of lowest energy. No particles propagate. No signals are sent. The microcausality condition holds. The vacuum is the ground state of a local Hamiltonian:

$$H = \int d^3x \, \mathcal{H}(x), \tag{6.6}$$

where $\mathcal{H}(x)$ is the Hamiltonian density, a local function of the fields and their conjugate momenta at the point $x$.

The vacuum thus exemplifies our thesis in its purest form: the state of the universe (or of a QFT) contains non-local correlations that are not mediated by any propagating entity, while the dynamics (governed by the local Hamiltonian density) and the causal structure (governed by microcausality) are strictly local.

### 6.4 The Entanglement Structure of the QFT Vacuum

For a free scalar field $\hat{\phi}(x)$ in $(3+1)$-dimensional Minkowski spacetime, the vacuum two-point function (Wightman function) is

$$W(x, y) = \langle 0 | \hat{\phi}(x) \hat{\phi}(y) | 0 \rangle = \int \frac{d^3p}{(2\pi)^3 2\omega_{\mathbf{p}}} e^{-ip \cdot (x - y)}, \tag{6.7}$$

where $\omega_{\mathbf{p}} = \sqrt{|\mathbf{p}|^2 + m^2}$. This function is non-zero for spacelike separations $(x - y)^2 < 0$. In fact, for a massless field in four dimensions,

$$W(x, y) \propto \frac{1}{(x - y)^2 - i\epsilon}. \tag{6.8}$$

The non-vanishing of $W(x, y)$ at spacelike separation reflects the entanglement structure of the vacuum. Yet the commutator

$$[\hat{\phi}(x), \hat{\phi}(y)] = W(x, y) - W(y, x) = i\Delta(x - y) \tag{6.9}$$

vanishes for spacelike separations: $\Delta(x - y) = 0$ when $(x-y)^2 < 0$. This is microcausality.

The distinction is precise:
- The **anticommutator** $\{\hat{\phi}(x), \hat{\phi}(y)\} = W(x,y) + W(y,x)$ is non-zero at spacelike separation → correlations exist.
- The **commutator** $[\hat{\phi}(x), \hat{\phi}(y)]$ vanishes at spacelike separation → no causal influence.

Correlation without causation. Non-locality without mediation.

---

## 7. The Kinematic–Dynamical–Causal Decomposition

### 7.1 The Three Sectors

We now introduce the central analytical framework of this paper. Any physical theory $T$ may be decomposed into three structurally distinct sectors:

**Definition 7.1 (Kinematic Sector).** The kinematic sector $\mathcal{K}$ of a physical theory consists of:
- The state space $\mathcal{S}$ (e.g., a Hilbert space $\mathcal{H}$, or the space of density operators).
- The algebra of observables $\mathcal{O}$.
- The correlation structure: the map $\rho \mapsto \{P(a, b \mid \alpha, \beta)\}$ assigning joint probability distributions to states and measurement choices.

**Definition 7.2 (Dynamical Sector).** The dynamical sector $\mathcal{D}$ consists of:
- The Hamiltonian $H$ (or Lagrangian $\mathcal{L}$, or action $S$).
- The time-evolution map $\rho(t) = U(t)\rho(0)U^\dagger(t)$, where $U(t) = e^{-iHt/\hbar}$.
- The equations of motion.

**Definition 7.3 (Causal Sector).** The causal sector $\mathcal{C}$ consists of:
- The spacetime manifold $(M, g_{\mu\nu})$ with its Lorentzian metric.
- The light-cone structure: the partial order $x \preceq y$ iff $y$ is in the causal future of $x$.
- The constraint that dynamical influences propagate within or on the light cone.

### 7.2 Independence of the Sectors

The key insight is that these three sectors carry independent structural content. In particular:

**Theorem 7.4.** *The non-local correlations of quantum mechanics reside entirely in the kinematic sector $\mathcal{K}$. The dynamical sector $\mathcal{D}$ is local (governed by a local Hamiltonian density). The causal sector $\mathcal{C}$ is local (governed by the light-cone structure). There is no logical or mathematical necessity for the correlation structure of $\mathcal{K}$ to be reducible to the dynamical or causal structure of $\mathcal{D}$ or $\mathcal{C}$.*

*Proof sketch.* The entangled state $|\psi^-\rangle = \frac{1}{\sqrt{2}}(|01\rangle - |10\rangle)$ is a vector in $\mathcal{H}_A \otimes \mathcal{H}_B$. Its correlation tensor $T_{ij} = -\delta_{ij}$ is a property of this vector. The Hamiltonian governing the time evolution of the two qubits may be purely local:

$$H = H_A \otimes \mathbb{I}_B + \mathbb{I}_A \otimes H_B, \tag{7.1}$$

with no interaction term. Under such a Hamiltonian, the entangled state evolves as

$$|\psi(t)\rangle = (U_A(t) \otimes U_B(t))|\psi(0)\rangle, \tag{7.2}$$

and the entanglement is preserved (local unitaries cannot create or destroy entanglement). The correlations persist without any dynamical interaction between $A$ and $B$.

The causal structure, given by the Minkowski metric $\eta_{\mu\nu}$, constrains only the propagation of dynamical influences. It does not constrain the kinematic correlation structure of the state. The state $|\psi^-\rangle$ is equally valid whether $A$ and $B$ are adjacent or cosmologically separated.

Therefore, the non-local correlations are a feature of $\mathcal{K}$, independent of $\mathcal{D}$ and $\mathcal{C}$. $\blacksquare$

### 7.3 The Source of the Apparent Paradox

The apparent paradox of "spooky action at a distance" arises from conflating the kinematic and dynamical sectors. The reasoning is:

1. Alice measures her qubit. (Dynamical event.)
2. Bob's outcome is correlated with Alice's. (Kinematic fact.)
3. Therefore, Alice's measurement must have causally influenced Bob's system. (Conflation of kinematic and dynamical/causal sectors.)

Step 3 does not follow. The correlation was present in the kinematic structure (the state $|\psi^-\rangle$) before either measurement occurred. The measurements reveal the correlation; they do not create it. No dynamical influence propagates from Alice to Bob.

The analogy is imperfect but instructive: if two envelopes contain correlated cards (one red, one blue), opening one envelope and finding a red card tells you the other envelope contains a blue card. No influence propagated from one envelope to the other. The correlation was established at the time of preparation. The quantum case differs from this classical analogy in that the correlations violate Bell inequalities and therefore cannot be explained by pre-existing local properties. But the structural point remains: the correlation is a property of the joint state, not of a signal propagating between the measurement events.

### 7.4 Formal Statement of the Resolution

We can now state the resolution precisely:

**Theorem 7.5 (Acausal Correlation Theorem).** *Let $\rho_{AB}$ be an entangled state on $\mathcal{H}_A \otimes \mathcal{H}_B$, and let $\{M_a^{(\alpha)}\}$ and $\{N_b^{(\beta)}\}$ be measurements on $A$ and $B$ respectively. Then:*

*(i) The joint probabilities $P(a, b \mid \alpha, \beta) = \mathrm{Tr}[\rho_{AB}(M_a^{(\alpha)} \otimes N_b^{(\beta)})]$ exhibit correlations that violate Bell inequalities and cannot be decomposed as in Eq. (3.5).*

*(ii) The marginal probabilities $P(b \mid \beta) = \sum_a P(a, b \mid \alpha, \beta)$ are independent of $\alpha$ (no-signaling).*

*(iii) The correlations in (i) are determined entirely by $\rho_{AB}$ and the measurement operators. No term in the expression for $P(a, b \mid \alpha, \beta)$ involves a propagator, Green's function, or any object associated with dynamical propagation between the measurement events.*

*(iv) The dynamical evolution of $\rho_{AB}$, governed by a local Hamiltonian, and the causal structure, governed by the spacetime metric, are unaffected by and independent of the correlations in (i).*

*Therefore, the correlations are non-local (they violate Bell inequalities), acausal (they do not constitute or require causal influence), and unmediated (they are not produced by any propagating entity).* $\blacksquare$

---

## 8. The Tsirelson Bound and the Geometry of Correlations

### 8.1 The Tsirelson Bound

Quantum mechanics does not permit arbitrary violations of the CHSH inequality. The maximum quantum violation is bounded by the **Tsirelson bound** [15]:

$$|S| \leq 2\sqrt{2}. \tag{8.1}$$

**Theorem 8.1 (Tsirelson [15]).** *For any quantum state $\rho_{AB}$ and any observables $A_0, A_1$ on $\mathcal{H}_A$ and $B_0, B_1$ on $\mathcal{H}_B$ with $\|A_i\| \leq 1$, $\|B_j\| \leq 1$, the CHSH operator*

$$\hat{S} = A_0 \otimes B_0 + A_0 \otimes B_1 + A_1 \otimes B_0 - A_1 \otimes B_1 \tag{8.2}$$

*satisfies*

$$\|\hat{S}\| \leq 2\sqrt{2}. \tag{8.3}$$

*Proof.* We compute $\hat{S}^2$. Let $C_0 = A_0 \otimes \mathbb{I}$, $C_1 = A_1 \otimes \mathbb{I}$, $D_0 = \mathbb{I} \otimes B_0$, $D_1 = \mathbb{I} \otimes B_1$. Then $\hat{S} = C_0 D_0 + C_0 D_1 + C_1 D_0 - C_1 D_1$.

Since $[C_i, D_j] = 0$ for all $i, j$ (they act on different tensor factors):

$$\hat{S}^2 = 4\mathbb{I} + [C_0, C_1][D_0, D_1], \tag{8.4}$$

where $[X, Y] = XY - YX$. This identity can be verified by direct expansion.

Now, $\|[C_0, C_1]\| \leq 2\|C_0\|\|C_1\| \leq 2$ and similarly $\|[D_0, D_1]\| \leq 2$. Therefore

$$\|\hat{S}^2\| \leq 4 + \|[C_0, C_1]\| \cdot \|[D_0, D_1]\| \leq 4 + 4 = 8. \tag{8.5}$$

Thus $\|\hat{S}\| \leq \sqrt{8} = 2\sqrt{2}$. $\blacksquare$

### 8.2 The No-Signaling Polytope and the Quantum Set

The space of all bipartite correlations $P(a, b \mid \alpha, \beta)$ for fixed numbers of settings and outcomes has a rich geometric structure. We focus on the $(2, 2, 2)$ scenario: 2 parties, 2 settings each, 2 outcomes each.

**The Local Polytope $\mathcal{L}$.** The set of correlations admitting a local hidden variable decomposition (3.5) forms a convex polytope $\mathcal{L}$, the **local polytope**. Its vertices are the deterministic local strategies. The CHSH inequalities (and their permutations) are the facet inequalities of $\mathcal{L}$.

**The No-Signaling Polytope $\mathcal{NS}$.** The set of correlations satisfying the no-signaling conditions

$$\sum_a P(a, b \mid \alpha, \beta) = P(b \mid \beta) \quad \forall \alpha, \qquad \sum_b P(a, b \mid \alpha, \beta) = P(a \mid \alpha) \quad \forall \beta \tag{8.6}$$

forms a convex polytope $\mathcal{NS}$, the **no-signaling polytope**. It strictly contains $\mathcal{L}$:

$$\mathcal{L} \subsetneq \mathcal{NS}. \tag{8.7}$$

The vertices of $\mathcal{NS}$ include the **Popescu–Rohrlich (PR) boxes** [16], which achieve $|S| = 4$ while satisfying no-signaling.

**The Quantum Set $\mathcal{Q}$.** The set of correlations achievable by quantum measurements on entangled states forms a convex set $\mathcal{Q}$ satisfying

$$\mathcal{L} \subsetneq \mathcal{Q} \subsetneq \mathcal{NS}. \tag{8.8}$$

The quantum set is strictly larger than the local polytope (Bell violations) but strictly smaller than the no-signaling polytope (Tsirelson bound). The boundary of $\mathcal{Q}$ is not a polytope; it is a curved surface.

### 8.3 Interpretation of the Hierarchy

The strict inclusions $\mathcal{L} \subsetneq \mathcal{Q} \subsetneq \mathcal{NS}$ encode the physics:

- $\mathcal{L} \subsetneq \mathcal{Q}$: Quantum correlations are non-local. They exceed what is possible with local hidden variables. This is Bell's theorem.

- $\mathcal{Q} \subsetneq \mathcal{NS}$: Quantum correlations are not maximally non-local. The Tsirelson bound restricts them. The PR-box correlations, while no-signaling, are not achievable in quantum mechanics. This is a deep constraint on the structure of quantum theory, related to information-theoretic principles [17] and the structure of quantum dynamics [18].

- $\mathcal{Q} \subset \mathcal{NS}$: All quantum correlations are no-signaling. This is the no-signaling theorem. Causal influence is local.

The non-local correlations of quantum mechanics thus occupy a precise, well-defined region in the space of all possible correlations: beyond the local, but short of the maximally non-local. They are non-local but causal. They are correlated but not communicating.

---

## 9. Interpretive Frameworks

The formal results of Sections 3–8 are interpretation-independent: they follow from the mathematical structure of quantum mechanics and relativistic QFT. However, different interpretive frameworks provide different ontological narratives for the same formal facts. We briefly assess the major frameworks in light of our thesis.

### 9.1 Copenhagen / Operational Interpretation

In the operational interpretation, the quantum state is a tool for computing probabilities of measurement outcomes. The "collapse" of the wavefunction is an update of the observer's information, not a physical process. The non-local correlations are simply a feature of the probability structure. No mediation is required because no physical process of collapse occurs. This interpretation is fully compatible with our thesis but offers no ontological account of what the correlations are "about."

### 9.2 Many-Worlds / Everettian Interpretation

In the Everett interpretation [19], the universal wavefunction evolves unitarily at all times. There is no collapse. When Alice measures her qubit, the universal state branches into components corresponding to different outcomes. Bob's measurement similarly branches. The correlations arise because the branching structure of the global state encodes the entanglement. No signal propagates between Alice and Bob; the correlation is a feature of the global branching structure. This is compatible with our thesis: the correlations are kinematic (encoded in the state), not dynamical (not produced by propagation).

### 9.3 Bohmian Mechanics

Bohmian mechanics [20] provides a deterministic hidden-variable theory that reproduces quantum predictions. It achieves this by introducing a non-local guiding equation: the velocity of each particle depends on the positions of all other particles through the quantum potential. The non-locality is explicit and dynamical. However, the theory is constructed so that the non-local influence cannot be used for signaling (it is "sub-quantum"). In our framework, Bohmian mechanics introduces non-locality into the dynamical sector, whereas standard quantum mechanics confines it to the kinematic sector. Both reproduce the same empirical predictions, but the ontological pictures differ.

### 9.4 Relational Quantum Mechanics

In Rovelli's relational interpretation [21], the quantum state is not an absolute property of a system but a relation between the system and an observer. The non-local correlations are not a property of the systems alone but of the relational structure. This is compatible with our thesis: the correlations are structural (kinematic), not dynamical.

### 9.5 QBism

In Quantum Bayesianism [22], the quantum state represents an agent's degrees of belief. The non-local correlations are constraints on coherent probability assignments, not features of an observer-independent reality. The correlations are "non-local" only in the sense that the agent's probability assignments for spacelike-separated events are not decomposable into independent local assignments. No mediation is required because no physical process is described.

### 9.6 Retrocausal and Superdeterministic Approaches

Retrocausal interpretations [23, 24] posit that future measurement choices influence past hidden variables, thereby restoring locality at the cost of introducing backward-in-time causation. Superdeterministic approaches [25] deny measurement independence (Assumption 4), positing correlations between the hidden variables and the measurement settings. Both are logically consistent but introduce additional structure beyond standard quantum mechanics. In our framework, these approaches attempt to restore a dynamical or causal explanation for what is, in standard quantum mechanics, a purely kinematic feature.

### 9.7 Assessment

All interpretations agree on the formal content: Bell inequalities are violated, no-signaling holds, and the correlations are determined by the quantum state. They differ on whether the correlations require an ontological explanation beyond the kinematic structure. Our thesis is that no such additional explanation is required: the correlations are a primitive feature of the kinematic sector, and the demand for a mediating mechanism reflects an unjustified assumption that all correlations must be dynamically produced.

---

## 10. Discussion and Conclusions

### 10.1 Summary of Results

We have established the following:

1. **Bell non-locality is real.** The correlations of entangled quantum systems violate Bell inequalities (Section 3). No local hidden variable theory can reproduce them. This is a theorem, confirmed experimentally.

2. **No causal influence propagates.** The no-signaling theorem (Section 4) proves that the reduced state of any subsystem is invariant under operations on spacelike-separated subsystems. In QFT, the microcausality condition (Section 6) enforces the locality of all dynamical interactions.

3. **The correlations are not mediated.** The joint probabilities $P(a, b \mid \alpha, \beta)$ are determined entirely by the state $\rho_{AB}$ and the measurement operators (Section 5). No propagator, Green's function, or mediating field enters the calculation. The correlations are a property of the global state.

4. **The kinematic/dynamical/causal decomposition resolves the tension.** The non-local correlations reside in the kinematic sector. The dynamical and causal sectors remain strictly local (Section 7). There is no contradiction because the sectors carry independent structural content.

5. **The Tsirelson bound constrains the non-locality.** Quantum correlations are non-local but not maximally so. They occupy a precise region $\mathcal{L} \subsetneq \mathcal{Q} \subsetneq \mathcal{NS}$ in the space of correlations (Section 8).

### 10.2 The Ontological Picture

The universe, as described by quantum mechanics and relativistic QFT, has the following structure:

- **The kinematic structure** is non-separable. The state of a composite system is not determined by the states of its parts. Entanglement is a generic, pervasive feature. The vacuum state of a QFT is entangled across every spatial partition. The correlations encoded in the kinematic structure are non-local in the Bell sense.

- **The dynamical structure** is local. The Hamiltonian is an integral of a local Hamiltonian density. Interactions are point-like. Time evolution propagates information within the light cone. Entanglement can be created by local interactions, but once created, it persists without further interaction.

- **The causal structure** is local. The light-cone structure of spacetime constrains the propagation of causal influences. Microcausality ensures that spacelike-separated operations commute. No signal, force, or controllable influence propagates faster than light.

These three structures coexist without contradiction. The non-local correlations of the kinematic structure do not violate the locality of the dynamical or causal structures because they do not belong to those structures. They are not produced by dynamics, do not propagate through spacetime, and cannot be used to transmit causal influence. They are, in the most precise sense, **acausal**.

### 10.3 The Principle of Acausal Correlation

We propose the following principle as a summary of our findings:

> **Principle of Acausal Correlation.** *The physical universe contains correlation structures that are irreducibly non-local, in the sense that they cannot be decomposed into contributions from spacelike-separated regions. These correlations are not mediated by any physical process propagating through spacetime. They are encoded in the global quantum state and are revealed, but not created, by measurement. Causal influence, by contrast, is strictly local, confined to the forward light cone, and governed by the dynamical and relativistic structure of the theory. Non-local correlation and local causality coexist as independent structural features of physical reality.*

### 10.4 Open Questions

Several questions remain open:

1. **Why the Tsirelson bound?** The Tsirelson bound $|S| \leq 2\sqrt{2}$ distinguishes quantum correlations from the broader class of no-signaling correlations. What physical principle selects the quantum set $\mathcal{Q}$ from within $\mathcal{NS}$? Proposals include information causality [17], local orthogonality [26], and the structure of quantum dynamics [18], but a definitive answer remains elusive.

2. **The measurement problem.** The formalism describes correlations but does not specify the mechanism by which definite outcomes arise. The measurement problem is orthogonal to the non-locality question but intersects it in discussions of collapse and state update.

3. **Quantum gravity.** In a theory of quantum gravity, the causal structure itself may become dynamical and quantum. The kinematic/dynamical/causal decomposition may need revision. The interplay between entanglement and geometry, as explored in the ER=EPR conjecture [27] and holographic entanglement entropy [28], suggests that non-local correlations may play a fundamental role in the emergence of spacetime.

4. **Cosmological entanglement.** The quantum state of the early universe, as described by inflationary cosmology, contains entanglement across causally disconnected regions. The origin and structure of this primordial entanglement, and its relation to the observed correlations in the cosmic microwave background, remain active areas of research.

### 10.5 Final Remark

The demand that every correlation be explained by a mediating mechanism is a prejudice inherited from classical physics. In classical mechanics, correlations between distant systems are always traceable to a common cause in the past or a signal propagated between them. Quantum mechanics reveals that this is not a necessary feature of physical reality. The universe contains correlations that are not mediated by anything. They simply are. They are part of the kinematic structure of the world, as fundamental and irreducible as the spacetime metric or the gauge group of the Standard Model.

This is not a deficiency of our theories. It is a feature of the world.

---

## Acknowledgments

The author thanks [collaborators] for discussions. This work was supported by [funding agency].

---

## References

[1] J. S. Bell, "On the Einstein Podolsky Rosen paradox," *Physics* **1**, 195–200 (1964).

[2] S. J. Freedman and J. F. Clauser, "Experimental test of local hidden-variable theories," *Phys. Rev. Lett.* **28**, 938–941 (1972).

[3] A. Aspect, P. Grangier, and G. Roger, "Experimental realization of Einstein-Podolsky-Rosen-Bohm Gedankenexperiment: A new violation of Bell's inequalities," *Phys. Rev. Lett.* **49**, 91–94 (1982).

[4] B. Hensen et al., "Loophole-free Bell inequality violation using electron spins separated by 1.3 kilometres," *Nature* **526**, 682–686 (2015).

[5] M. Giustina et al., "Significant-loophole-free test of Bell's theorem with entangled photons," *Phys. Rev. Lett.* **115**, 250401 (2015).

[6] L. K. Shalm et al., "Strong loophole-free test of local realism," *Phys. Rev. Lett.* **115**, 250402 (2015).

[7] G. C. Ghirardi, A. Rimini, and T. Weber, "A general argument against superluminal transmission through the quantum mechanical measurement process," *Lett. Nuovo Cimento* **27**, 293–298 (1980).

[8] N. Gisin, "Bell inequalities: Many questions, a few answers," in *Quantum [Un]speakable*, pp. 141–156, Springer (2002). arXiv:quant-ph/0702021.

[9] E. Schmidt, "Zur Theorie der linearen und nichtlinearen Integralgleichungen," *Math. Ann.* **63**, 433–476 (1907).

[10] J. F. Clauser, M. A. Horne, A. Shimony, and R. A. Holt, "Proposed experiment to test local hidden-variable theories," *Phys. Rev. Lett.* **23**, 880–884 (1969).

[11] R. Haag, *Local Quantum Physics: Fields, Particles, Algebras*, 2nd ed., Springer (1996).

[12] H. Reeh and S. Schlieder, "Bemerkungen zur Unitäräquivalenz von Lorentzinvarianten Feldern," *Nuovo Cimento* **22**, 1051–1068 (1961).

[13] S. J. Summers and R. Werner, "Bell's inequalities and quantum field theory. I. General setting," *J. Math. Phys.* **28**, 2440–2447 (1987).

[14] S. J. Summers and R. Werner, "Maximal violation of Bell's inequalities is generic in quantum field theory," *Commun. Math. Phys.* **110**, 247–259 (1987).

[15] B. S. Cirel'son, "Quantum generalizations of Bell's inequality," *Lett. Math. Phys.* **4**, 93–100 (1980).

[16] S. Popescu and D. Rohrlich, "Quantum nonlocality as an axiom," *Found. Phys.* **24**, 379–385 (1994).

[17] M. Pawłowski et al., "Information causality as a physical principle," *Nature* **461**, 1101–1104 (2009).

[18] M. Navascués, S. Pironio, and A. Acín, "A convergent hierarchy of semidefinite programs characterizing the quantum set of correlations," *New J. Phys.* **10**, 073013 (2008).

[19] H. Everett III, "'Relative state' formulation of quantum mechanics," *Rev. Mod. Phys.* **29**, 454–462 (1957).

[20] D. Bohm, "A suggested interpretation of the quantum theory in terms of 'hidden' variables. I," *Phys. Rev.* **85**, 166–179 (1952).

[21] C. Rovelli, "Relational quantum mechanics," *Int. J. Theor. Phys.* **35**, 1637–1678 (1996).

[22] C. A. Fuchs, N. D. Mermin, and R. Schack, "An introduction to QBism with an application to the locality of quantum mechanics," *Am. J. Phys.* **82**, 749–754 (2014).

[23] H. Price, "Does time-symmetry imply retrocausality? How the quantum world says 'maybe'," *Stud. Hist. Philos. Mod. Phys.* **43**, 75–83 (2012).

[24] M. S. Leifer and M. F. Pusey, "Is a time symmetric interpretation of quantum theory possible without retrocausality?" *Proc. R. Soc. A* **473**, 20160607 (2017).

[25] G. 't Hooft, "The free will postulate in quantum mechanics," arXiv:quant-ph/0104042 (2001).

[26] T. Fritz et al., "Local orthogonality: A multipartite principle for correlations," *Nat. Commun.* **4**, 2263 (2013).

[27] J. Maldacena and L. Susskind, "Cool horizons for entangled black holes," *Fortschr. Phys.* **61**, 781–811 (2013).

[28] S. Ryu and T. Takayanagi, "Holographic derivation of entanglement entropy from AdS/CFT," *Phys. Rev. Lett.* **96**, 181602 (2006).

---

## Appendix A: Conventions and Notation

- Metric signature: $\eta_{\mu\nu} = \mathrm{diag}(+1, -1, -1, -1)$.
- Natural units: $\hbar = c = 1$ unless otherwise stated.
- Pauli matrices: $\sigma_x = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$, $\sigma_y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}$, $\sigma_z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{
