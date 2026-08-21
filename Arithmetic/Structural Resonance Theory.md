# Structural Resonance Theory  
## A Variational Framework for Compatibility of Mathematical Structures

**White Paper**

**Keywords:** structural resonance, internal symmetry, spectral graph theory, harmonic analysis, representation theory, invariant tensors, geometric deep learning.  
**Mathematics Subject Classification (2020):** 05C50, 22E45, 43A65, 58J50, 68T07.

---

## Abstract

Structural Resonance Theory (SRT) introduces a mathematical relation that refines and generalizes equivalence. The central object is a resonance functional  
\[
\mathcal{R}(A,B)\in[0,1],
\]
assigned to two structured mathematical objects \(A\) and \(B\). The functional measures the degree to which the internal symmetries, spectral operators, and invariant tensors of \(A\) and \(B\) admit a mutually compatible alignment. Equivalence is recovered as the extremal case \(\mathcal{R}(A,B)=1\), while nontrivial values of \(\mathcal{R}\) define a graded notion of structural compatibility.

We develop an axiomatic and variational formulation of SRT in finite-dimensional Hilbertian settings, derive a representation-theoretic expression for resonance in terms of characters and intertwiner spaces, obtain explicit spectral formulas for graphs, extend the framework to harmonic analysis on compact groups and homogeneous spaces, and formulate consequences for machine learning, including resonance kernels, contrastive resonance losses, and symmetry-aware representation learning.

The central thesis is:

> **Mathematical structures resonate through compatible internal symmetries. Resonance, not equivalence, is the primary structural relation.**

---

# 1. Introduction

Classical mathematics organizes objects through equivalence relations: isomorphism of groups, homeomorphism of spaces, unitary equivalence of representations, isometry of metric spaces, isomorphism of graphs. Equivalence is binary and rigid. Two objects either belong to the same equivalence class or they do not.

Many natural and mathematical situations require a more flexible relation. Two graphs may be non-isomorphic yet nearly indistinguishable at the level of their spectra. Two representations may not be equivalent yet share a large common isotypic component. Two manifolds may not be isometric yet possess highly correlated Laplace spectra. Two neural representations may not be identical but may carry compatible symmetry constraints.

Structural Resonance Theory proposes that the correct primitive relation is not equivalence but **resonance**.

Given two structured objects \(A\) and \(B\), we define a resonance functional
\[
\mathcal{R}(A,B)
\]
that measures the maximal compatibility of their internal symmetries. The value \(\mathcal{R}(A,B)=1\) corresponds to perfect resonance, which includes isomorphism as a special case. Values strictly between \(0\) and \(1\) quantify partial resonance, approximate compatibility, or shared substructure. Values near \(0\) indicate structural incompatibility.

The theory is organized around three principles.

### Principle 1: Structures carry internal symmetries.

A structure is not merely an underlying set. It is a system of operators, tensors, spectra, and transformation laws. Its internal symmetry is encoded by the group or algebra of transformations preserving its defining data.

### Principle 2: Resonance is an optimal alignment.

The resonance between two structures is obtained by maximizing over admissible alignments. These alignments may be unitary maps, orthogonal couplings, intertwiners, partial isometries, or symmetry correspondences. The objective penalizes failure of the alignment to preserve symmetry, spectral operators, and invariant tensors.

### Principle 3: Equivalence is the zero-energy limit.

Equivalence arises when there exists an alignment with zero resonance action. In that case,
\[
\mathcal{R}(A,B)=1.
\]
But the theory does not collapse to equivalence. It provides a continuous scale of compatibility.

The present paper develops SRT in a form suitable for spectral graph theory, harmonic analysis, representation theory, and machine learning.

---

# 2. Axiomatic Framework

We work primarily in finite-dimensional Hilbertian settings. The constructions extend to suitable infinite-dimensional completions, but the finite-dimensional formulation already contains the essential structure.

---

## 2.1 Structured Hilbertian objects

Let \(\mathbb{F}\in\{\mathbb{R},\mathbb{C}\}\).

### Definition 2.1

A **structured Hilbertian object** is a tuple
\[
A=(H_A,G_A,U_A,L_A,\mathcal{T}_A),
\]
where:

1. \(H_A\) is a finite-dimensional Hilbert space over \(\mathbb{F}\).
2. \(G_A\) is a compact group.
3. \(U_A:G_A\to \mathrm{U}(H_A)\) is a continuous unitary representation.
4. \(L_A:H_A\to H_A\) is a positive semidefinite self-adjoint operator satisfying
   \[
   U_A(g)L_AU_A(g)^*=L_A
   \]
   for all \(g\in G_A\).
5. \(\mathcal{T}_A=\{T_A^{(s)}\}_{s\in S}\) is a finite family of tensors
   \[
   T_A^{(s)}\in H_A^{\otimes p_s}\otimes (H_A^*)^{\otimes q_s},
   \]
   invariant under the induced action:
   \[
   U_A(g)^{\otimes p_s}T_A^{(s)}
   (U_A(g)^*)^{\otimes q_s}
   =
   T_A^{(s)}.
   \]

The operator \(L_A\) is typically a Laplacian, Hamiltonian, adjacency operator, or diffusion operator. The tensors \(T_A^{(s)}\) encode higher-order structure: adjacency tensors, curvature tensors, feature tensors, interaction tensors, or invariant observables.

If no symmetry group is specified, one may take \(G_A\) to be the automorphism group of the full tensor-operator system, or an ambient group acting naturally on \(H_A\).

---

## 2.2 Isomorphism

### Definition 2.2

Two structured objects
\[
A=(H_A,G_A,U_A,L_A,\mathcal{T}_A),
\qquad
B=(H_B,G_B,U_B,L_B,\mathcal{T}_B)
\]
are **isomorphic** if there exist:

1. a group isomorphism \(\alpha:G_A\to G_B\),
2. a unitary map \(W:H_A\to H_B\),

such that
\[
W U_A(g) = U_B(\alpha(g)) W,
\]
\[
W L_A W^* = L_B,
\]
and, for every tensor \(T_A^{(s)}\),
\[
W_* T_A^{(s)} = T_B^{(s)}.
\]

The push-forward \(W_*T\) is defined below.

---

## 2.3 Tensorial transport

Let \(\Phi:H_A\to H_B\) be a linear map. In coordinates, write
\[
\Phi^a{}_i
\]
for the matrix elements relative to bases of \(H_A\) and \(H_B\). If \(\Phi\) is unitary or isometric, its adjoint has components
\[
(\Phi^*)^j{}_b = \overline{\Phi^b{}_j}.
\]

For a tensor
\[
T\in H_A^{\otimes p}\otimes (H_A^*)^{\otimes q},
\]
the push-forward \(\Phi_*T\) is the tensor in
\[
H_B^{\otimes p}\otimes (H_B^*)^{\otimes q}
\]
with components
\[
(\Phi_*T)^{a_1\cdots a_p}{}_{b_1\cdots b_q}
=
\Phi^{a_1}{}_{i_1}\cdots \Phi^{a_p}{}_{i_p}
(\Phi^*)^{j_1}{}_{b_1}\cdots (\Phi^*)^{j_q}{}_{b_q}
T^{i_1\cdots i_p}{}_{j_1\cdots j_q}.
\]

For unitary \(\Phi\), this is the natural transformation law of tensors. For partial isometries, the same formula applies after restriction to the initial and final subspaces.

---

## 2.4 Symmetry couplings

When \(G_A\) and \(G_B\) differ, one must specify how their symmetries are compared. We introduce a coupling of their Haar measures.

Let \(dg_A\) and \(dg_B\) be normalized Haar probability measures on \(G_A\) and \(G_B\). A **symmetry coupling** is a probability measure
\[
\mu\in \mathrm{Prob}(G_A\times G_B)
\]
whose marginals are Haar:
\[
(\pi_A)_*\mu = dg_A,
\qquad
(\pi_B)_*\mu = dg_B.
\]

The set of such couplings is denoted
\[
\mathscr{C}(G_A,G_B).
\]

If \(G_A=G_B=G\), the diagonal coupling
\[
\mu_{\mathrm{diag}} = (\mathrm{id},\mathrm{id})_*dg
\]
is the natural choice. If the groups are unrelated, one may optimize over \(\mathscr{C}(G_A,G_B)\).

---

## 2.5 Alignments

For simplicity, suppose first that
\[
\dim H_A=\dim H_B=n.
\]
An **alignment** is a unitary map
\[
\Phi:H_A\to H_B.
\]

More generally, for structures of different sizes or for substructure resonance, one may allow partial isometries
\[
\Phi:H_A\to H_B,
\]
satisfying
\[
\Phi^*\Phi=P_A,
\qquad
\Phi\Phi^*=P_B,
\]
where \(P_A\) and \(P_B\) are orthogonal projections. In that case tensors are compressed to the relevant subspaces before comparison.

The space of admissible alignments is denoted
\[
\mathcal{A}(A,B).
\]

---

## 2.6 The resonance action

Let \(\Phi\in\mathcal{A}(A,B)\) and \(\mu\in\mathscr{C}(G_A,G_B)\). Define the normalized symmetry energy
\[
E_{\mathrm{sym}}(A,B;\mu,\Phi)
=
\frac{1}{2\|\Phi\|_{\mathrm{HS}}^2}
\int_{G_A\times G_B}
\left\|
\Phi U_A(g)-U_B(h)\Phi
\right\|_{\mathrm{HS}}^2
\,d\mu(g,h).
\]

Define the spectral energy
\[
E_{\mathrm{spec}}(A,B;\Phi)
=
\frac{
\left\|
L_B\Phi-\Phi L_A
\right\|_{\mathrm{HS}}^2
}{
\|L_A\|_{\mathrm{HS}}^2+\|L_B\|_{\mathrm{HS}}^2
}.
\]
If both Laplacians vanish, set \(E_{\mathrm{spec}}=0\).

For each tensor \(T_A^{(s)}\in\mathcal{T}_A\) with corresponding tensor \(T_B^{(s)}\in\mathcal{T}_B\), define the tensorial energy
\[
E_{\mathrm{ten}}^{(s)}(A,B;\Phi)
=
\frac{
\left\|
\Phi_*T_A^{(s)}-T_B^{(s)}
\right\|^2
}{
\|T_A^{(s)}\|^2+\|T_B^{(s)}\|^2
}.
\]

The **resonance action** is
\[
S(A,B;\mu,\Phi)
=
\lambda_{\mathrm{sym}}E_{\mathrm{sym}}(A,B;\mu,\Phi)
+
\lambda_{\mathrm{spec}}E_{\mathrm{spec}}(A,B;\Phi)
+
\sum_{s\in S}
\lambda_s E_{\mathrm{ten}}^{(s)}(A,B;\Phi),
\]
where
\[
\lambda_{\mathrm{sym}},\lambda_{\mathrm{spec}},\lambda_s\geq 0
\]
are resonance weights.

---

## 2.7 The resonance functional

### Definition 2.3

The **structural resonance functional** is
\[
\boxed{
\mathcal{R}(A,B)
=
\sup_{\mu\in\mathscr{C}(G_A,G_B)}
\sup_{\Phi\in\mathcal{A}(A,B)}
\exp\left(
- S(A,B;\mu,\Phi)
\right).
}
\]

If \(\mathcal{A}(A,B)=\varnothing\), set
\[
\mathcal{R}(A,B)=0.
\]

Because every energy term is nonnegative,
\[
0\leq \mathcal{R}(A,B)\leq 1.
\]

The value \(\mathcal{R}(A,B)=1\) means that there exists an alignment with zero action. The value \(\mathcal{R}(A,B)\approx 0\) means that no energetically compatible alignment exists.

One may also define a resonance distance
\[
d_{\mathcal{R}}(A,B)
=
-\log \mathcal{R}(A,B),
\]
with the convention \(d_{\mathcal{R}}=\infty\) when \(\mathcal{R}=0\).

---

## 2.8 Elementary properties

### Proposition 2.1

Let \(A,B\) be structured Hilbertian objects.

1. **Boundedness.**
   \[
   0\leq \mathcal{R}(A,B)\leq 1.
   \]

2. **Isomorphism invariance.**  
   If \(A\cong A'\) and \(B\cong B'\), then
   \[
   \mathcal{R}(A,B)=\mathcal{R}(A',B').
   \]

3. **Automorphism invariance.**  
   If \(g\cdot A\) denotes the action of an automorphism of \(A\), then
   \[
   \mathcal{R}(g\cdot A,h\cdot B)=\mathcal{R}(A,B).
   \]

4. **Symmetry.**  
   Under the natural adjoint alignment \(\Phi^*\) and transposed coupling \(\mu^\top\),
   \[
   \mathcal{R}(A,B)=\mathcal{R}(B,A).
   \]

5. **Equivalence limit.**  
   If \(A\cong B\), then
   \[
   \mathcal{R}(A,B)=1.
   \]
   Conversely, if the tensor-operator data are separating and the admissible alignments are restricted to exact structure-preserving maps, then
   \[
   \mathcal{R}(A,B)=1
   \]
   implies \(A\cong B\).

6. **Stability.**  
   If the operators and tensors are perturbed continuously, the resonance action varies continuously, and therefore \(\mathcal{R}\) varies continuously away from zero.

### Proof sketch

The energies are defined using Hilbert-Schmidt and tensor norms, hence are nonnegative. If \(A\cong B\), choose the isomorphism \(W\) and the induced group coupling. Then all commutators and tensor mismatches vanish, so \(S=0\), giving \(\mathcal{R}=1\).

Isomorphism invariance follows by conjugating alignments and transporting couplings. Symmetry follows by replacing \(\Phi\) with \(\Phi^*\) and observing that
\[
\|L_B\Phi-\Phi L_A\|_{\mathrm{HS}}
=
\|(L_B\Phi-\Phi L_A)^*\|_{\mathrm{HS}}
=
\|L_A\Phi^*-\Phi^*L_B\|_{\mathrm{HS}},
\]
with analogous identities for tensorial and symmetry energies. Stability follows from Lipschitz continuity of the norm and of the push-forward map on isometries. \(\square\)

---

# 3. Representation-Theoretic Resonance

We now specialize to the case where both structures carry representations of the same compact group \(G\):
\[
G_A=G_B=G.
\]
The coupling \(\mu\) is taken to be the diagonal Haar coupling.

This is the cleanest setting in which the role of internal symmetry can be made explicit.

---

## 3.1 Isotypic decomposition

Let \(\widehat{G}\) denote the set of equivalence classes of irreducible unitary representations of \(G\). For \(\pi\in\widehat{G}\), let \(V_\pi\) be the carrier space and let
\[
d_\pi=\dim V_\pi.
\]

Any finite-dimensional unitary representation \(U_A\) decomposes as
\[
H_A
\cong
\bigoplus_{\pi\in\widehat{G}}
V_\pi\otimes M_A^\pi,
\]
where \(M_A^\pi\) is the multiplicity space. Let
\[
m_A^\pi=\dim M_A^\pi.
\]

Similarly,
\[
H_B
\cong
\bigoplus_{\pi\in\widehat{G}}
V_\pi\otimes M_B^\pi,
\qquad
m_B^\pi=\dim M_B^\pi.
\]

The character of \(U_A\) is
\[
\chi_A(g)=\operatorname{Tr}U_A(g).
\]

By Schur orthogonality,
\[
\langle \chi_B,\chi_A\rangle_G
=
\int_G \chi_B(g)\overline{\chi_A(g)}\,dg
=
\sum_{\pi\in\widehat{G}}
m_A^\pi m_B^\pi.
\]

Moreover,
\[
\dim\operatorname{Hom}_G(H_A,H_B)
=
\sum_{\pi\in\widehat{G}}
m_A^\pi m_B^\pi.
\]

Thus the inner product of characters measures the dimension of the space of symmetry-compatible linear maps.

---

## 3.2 Symmetry profiles

Choose weights
\[
w_\pi\geq 0,
\]
typically with \(w_{\mathbf{1}}=0\) if one wishes to exclude the trivial representation from the symmetry profile. Define the **symmetry profile**
\[
s_A=(w_\pi m_A^\pi)_{\pi\in\widehat{G}}.
\]

The **symmetry resonance** is the cosine similarity of symmetry profiles:
\[
\boxed{
\mathcal{R}_{\mathrm{sym}}(A,B)
=
\frac{
\sum_{\pi\in\widehat{G}} w_\pi^2 m_A^\pi m_B^\pi
}{
\sqrt{
\sum_{\pi\in\widehat{G}} w_\pi^2 (m_A^\pi)^2
}
\sqrt{
\sum_{\pi\in\widehat{G}} w_\pi^2 (m_B^\pi)^2
}
}.
}
\]

If both profiles vanish, set \(\mathcal{R}_{\mathrm{sym}}=1\), meaning that no nontrivial symmetry obstruction is present.

When \(w_\pi=1\) for all \(\pi\),
\[
\mathcal{R}_{\mathrm{sym}}(A,B)
=
\frac{
\dim\operatorname{Hom}_G(H_A,H_B)
}{
\sqrt{
\dim\operatorname{End}_G(H_A)
}
\sqrt{
\dim\operatorname{End}_G(H_B)
}
}.
\]

This formula gives a precise representation-theoretic interpretation: resonance is normalized intertwiner overlap.

---

## 3.3 Theorem: symmetry obstruction

### Theorem 3.1

Let \(A\) and \(B\) carry representations of a compact group \(G\).

1. If
   \[
   \operatorname{Hom}_G(H_A,H_B)=0,
   \]
   then in the hard-symmetry limit
   \[
   \lambda_{\mathrm{sym}}\to\infty,
   \]
   the resonance functional vanishes:
   \[
   \mathcal{R}(A,B)=0.
   \]

2. If
   \[
   \operatorname{Hom}_G(H_A,H_B)\neq 0,
   \]
   then there exist nonzero alignments \(\Phi\) with
   \[
   E_{\mathrm{sym}}(A,B;\mu_{\mathrm{diag}},\Phi)=0.
   \]

3. The dimension of the zero-symmetry-energy alignment space is
   \[
   \dim\operatorname{Hom}_G(H_A,H_B)
   =
   \langle \chi_B,\chi_A\rangle_G.
   \]

### Proof

The Reynolds operator
\[
\Pi(\Phi)
=
\int_G U_B(g)^*\Phi U_A(g)\,dg
\]
is the orthogonal projection from \(\operatorname{Hom}(H_A,H_B)\) onto
\[
\operatorname{Hom}_G(H_A,H_B).
\]

If \(\Phi\in\operatorname{Hom}_G(H_A,H_B)\), then
\[
\Phi U_A(g)=U_B(g)\Phi
\]
for all \(g\), and therefore
\[
E_{\mathrm{sym}}=0.
\]

If \(\operatorname{Hom}_G(H_A,H_B)=0\), then \(\Pi=0\), so no nonzero alignment has zero symmetry energy. In the limit \(\lambda_{\mathrm{sym}}\to\infty\), the exponential suppresses all positive-energy alignments, giving \(\mathcal{R}=0\). The dimension formula follows from character orthogonality. \(\square\)

---

## 3.4 Spectral resonance on isotypic components

Assume now that \(L_A\) and \(L_B\) commute with the \(G\)-actions. By Schur’s lemma, they take the block form
\[
L_A
\cong
\bigoplus_{\pi\in\widehat{G}}
I_{V_\pi}\otimes S_A^\pi,
\]
where
\[
S_A^\pi:M_A^\pi\to M_A^\pi
\]
is self-adjoint. Similarly,
\[
L_B
\cong
\bigoplus_{\pi\in\widehat{G}}
I_{V_\pi}\otimes S_B^\pi.
\]

A \(G\)-equivariant alignment has the form
\[
\Phi
=
\bigoplus_{\pi\in\widehat{G}}
I_{V_\pi}\otimes Q_\pi,
\]
where
\[
Q_\pi:M_A^\pi\to M_B^\pi
\]
is a partial isometry.

Then
\[
L_B\Phi-\Phi L_A
\cong
\bigoplus_{\pi\in\widehat{G}}
I_{V_\pi}\otimes
\left(
S_B^\pi Q_\pi-Q_\pi S_A^\pi
\right).
\]

Taking Hilbert-Schmidt norms gives
\[
\|L_B\Phi-\Phi L_A\|_{\mathrm{HS}}^2
=
\sum_{\pi\in\widehat{G}}
d_\pi
\left\|
S_B^\pi Q_\pi-Q_\pi S_A^\pi
\right\|_{\mathrm{F}}^2.
\]

Thus spectral resonance reduces to alignment of multiplicity-space operators.

Define the normalized conditional spectral energy
\[
E_L(Q)
=
\frac{
\sum_{\pi}
d_\pi
\left\|
S_B^\pi Q_\pi-Q_\pi S_A^\pi
\right\|_{\mathrm{F}}^2
}{
\sum_{\pi}
d_\pi
\left(
\|S_A^\pi\|_{\mathrm{F}}^2+\|S_B^\pi\|_{\mathrm{F}}^2
\right)
}.
\]

---

## 3.5 Tensor resonance and selection rules

An invariant tensor
\[
T_A\in (H_A^{\otimes p}\otimes (H_A^*)^{\otimes q})^G
\]
may be identified with a \(G\)-intertwiner
\[
T_A:
H_A^{\otimes q}
\longrightarrow
H_A^{\otimes p}.
\]

Using the decomposition of \(H_A\), the tensor \(T_A\) decomposes into Clebsch-Gordan coefficients and multiplicity-space tensors. Schematically,
\[
T_A
=
\sum_{\alpha}
C_\alpha
\otimes
\tau_A^\alpha,
\]
where \(C_\alpha\) are invariant coupling tensors and
\[
\tau_A^\alpha
\]
are tensors on multiplicity spaces.

An equivariant alignment
\[
\Phi=\bigoplus_\pi I_\pi\otimes Q_\pi
\]
acts on the multiplicity tensors:
\[
\tau_A^\alpha
\mapsto
Q_*\tau_A^\alpha.
\]

The tensorial resonance energy is therefore
\[
E_T(Q)
=
\sum_\alpha
\omega_\alpha
\frac{
\left\|
Q_*\tau_A^\alpha-\tau_B^\alpha
\right\|^2
}{
\|\tau_A^\alpha\|^2+\|\tau_B^\alpha\|^2
}.
\]

Thus resonance is constrained by representation-theoretic selection rules: only those components coupled by shared irreducible representations contribute.

---

## 3.6 Factorized resonance functional

In the common-group setting, it is natural to write
\[
\boxed{
\mathcal{R}(A,B)
=
\mathcal{R}_{\mathrm{sym}}(A,B)
\cdot
\mathcal{R}_{\mathrm{cond}}(A,B),
}
\]
where
\[
\mathcal{R}_{\mathrm{cond}}(A,B)
=
\sup_{Q}
\exp\left(
-\lambda_L E_L(Q)-\lambda_T E_T(Q)
\right).
\]

The factor \(\mathcal{R}_{\mathrm{sym}}\) measures overlap of internal symmetry types. The factor \(\mathcal{R}_{\mathrm{cond}}\) measures compatibility of spectral and tensorial data on the shared symmetry sectors.

This factorization is one of the central analytical structures of SRT.

---

# 4. Spectral Graph Resonance

We now develop the graph-theoretic instantiation of SRT. This yields explicit formulas in spectral graph theory and connects resonance to graph matching, spectral clustering, and graph neural networks.

---

## 4.1 Graphs as structured objects

Let \(G=(V,E,w,X)\) be a weighted graph with \(|V|=n\), edge weights \(w_{ij}\geq 0\), and node features
\[
X_G\in \mathbb{R}^{n\times f}.
\]

Let
\[
H_G=\mathbb{R}^n.
\]

The adjacency tensor is the symmetric bilinear form
\[
A_G\in \operatorname{Sym}^2(H_G^*)
\]
with components
\[
(A_G)_{ij}=w_{ij}.
\]

The degree matrix is
\[
D_{ii}=\sum_j w_{ij}.
\]

The combinatorial Laplacian is
\[
L_G=D-A_G.
\]

The automorphism group is
\[
\operatorname{Aut}(G)
=
\{
P\in S_n:
P^\top A_G P=A_G,\;
P^\top X_G=X_G
\}.
\]

A graph is thus a structured object
\[
G=(H_G,\operatorname{Aut}(G),U_G,L_G,A_G,X_G),
\]
where \(U_G\) is the permutation representation of \(\operatorname{Aut}(G)\).

---

## 4.2 Graph resonance

Let \(G\) and \(H\) be graphs on the same number \(n\) of vertices. We first define the continuous resonance relaxation using orthogonal alignments.

For \(Q\in O(n)\), define the adjacency push-forward
\[
(Q_*A_G)_{ab}
=
Q_{ai}Q_{bj}(A_G)_{ij}.
\]

Define normalized energies
\[
\widehat E_L(Q)
=
\frac{
\|L_HQ-QL_G\|_{\mathrm{F}}^2
}{
\|L_G\|_{\mathrm{F}}^2+\|L_H\|_{\mathrm{F}}^2
},
\]
\[
\widehat E_A(Q)
=
\frac{
\|A_H-Q_*A_G\|_{\mathrm{F}}^2
}{
\|A_G\|_{\mathrm{F}}^2+\|A_H\|_{\mathrm{F}}^2
},
\]
\[
\widehat E_X(Q)
=
\frac{
\|X_H-QX_G\|_{\mathrm{F}}^2
}{
\|X_G\|_{\mathrm{F}}^2+\|X_H\|_{\mathrm{F}}^2
}.
\]

The **graph resonance functional** is
\[
\boxed{
\mathcal{R}_{\mathrm{graph}}(G,H)
=
\max_{Q\in O(n)}
\exp\left(
-\lambda_L \widehat E_L(Q)
-\lambda_A \widehat E_A(Q)
-\lambda_X \widehat E_X(Q)
\right).
}
\]

If one requires exact combinatorial equivalence, replace \(O(n)\) by the permutation group \(S_n\). The orthogonal relaxation is the natural continuous resonance functional.

---

## 4.3 Spectral reduction

Let
\[
L_G=U\Lambda U^\top,
\qquad
L_H=V M V^\top
\]
be orthogonal spectral decompositions, with
\[
\Lambda=\operatorname{diag}(\lambda_1,\dots,\lambda_n),
\qquad
M=\operatorname{diag}(\mu_1,\dots,\mu_n).
\]

For \(Q\in O(n)\), set
\[
C=V^\top Q U.
\]
Then \(C\in O(n)\), and
\[
Q=VCU^\top.
\]

Now compute:
\[
L_HQ-QL_G
=
V M V^\top Q
-
Q U\Lambda U^\top.
\]
Using \(V^\top Q U=C\), we obtain
\[
L_HQ-QL_G
=
V(MC-C\Lambda)U^\top.
\]

Therefore
\[
\|L_HQ-QL_G\|_{\mathrm{F}}^2
=
\|MC-C\Lambda\|_{\mathrm{F}}^2.
\]

Since \(M\) and \(\Lambda\) are diagonal,
\[
(MC-C\Lambda)_{ij}
=
\mu_i C_{ij}-C_{ij}\lambda_j
=
(\mu_i-\lambda_j)C_{ij}.
\]

Hence
\[
\boxed{
\|L_HQ-QL_G\|_{\mathrm{F}}^2
=
\sum_{i,j=1}^n
(\mu_i-\lambda_j)^2 C_{ij}^2.
}
\]

Thus the spectral graph resonance becomes
\[
\boxed{
\mathcal{R}_{\mathrm{spec}}(G,H)
=
\max_{C\in O(n)}
\exp\left(
-\frac{\lambda_L}{\sigma_L^2}
\sum_{i,j=1}^n
(\mu_i-\lambda_j)^2 C_{ij}^2
\right),
}
\]
where
\[
\sigma_L^2=
\|L_G\|_{\mathrm{F}}^2+\|L_H\|_{\mathrm{F}}^2.
\]

This is a spectrally weighted orthogonal Procrustes problem.

---

## 4.4 Feature anchoring

Node features break eigenvector gauge freedom. In the eigenbasis,
\[
X_G\mapsto U^\top X_G,
\qquad
X_H\mapsto V^\top X_H.
\]

The feature energy becomes
\[
\widehat E_X(C)
=
\frac{
\|V^\top X_H-CU^\top X_G\|_{\mathrm{F}}^2
}{
\|X_G\|_{\mathrm{F}}^2+\|X_H\|_{\mathrm{F}}^2
}.
\]

Thus the full spectral-feature resonance is
\[
\mathcal{R}_{\mathrm{spec},X}(G,H)
=
\max_{C\in O(n)}
\exp\left(
-\lambda_L \widehat E_L(C)
-\lambda_X \widehat E_X(C)
\right).
\]

The features select preferred bases inside degenerate eigenspaces.

---

## 4.5 Exact isomorphism and rigidity

### Theorem 4.1

Let \(G\) and \(H\) be finite weighted graphs on \(n\) vertices.

1. If the admissible alignments are restricted to permutation matrices \(P\in S_n\), then
   \[
   \mathcal{R}_{\mathrm{graph}}(G,H)=1
   \]
   if and only if \(G\) and \(H\) are isomorphic as weighted featured graphs.

2. If the admissible alignments are \(Q\in O(n)\), then
   \[
   \mathcal{R}_{\mathrm{spec}}(G,H)=1
   \]
   if and only if there exists \(Q\in O(n)\) such that
   \[
   L_HQ=QL_G.
   \]
   If additionally adjacency and feature energies vanish, then
   \[
   A_H=Q_*A_G,
   \qquad
   X_H=QX_G.
   \]
   This is orthogonal equivalence of structured graphs.

3. If the Laplacian spectrum is simple and the feature matrix separates eigenspaces, then any orthogonal equivalence is, up to signs, a permutation equivalence. If the adjacency tensor has nonnegative entries and no signed cancellation, the signs are forced to be positive, yielding graph isomorphism.

### Proof sketch

If \(P\in S_n\) is an isomorphism, then
\[
P^\top A_H P=A_G,
\qquad
P^\top L_H P=L_G,
\qquad
P^\top X_H=X_G,
\]
so all energies vanish and \(\mathcal{R}=1\).

Conversely, if the energies vanish, the defining equalities hold. For simple spectra, the eigenvectors are determined up to signs. Features or nonnegative adjacency constraints remove sign ambiguity, forcing a permutation. \(\square\)

Thus equivalence is recovered as the maximal resonance state.

---

## 4.6 Stability of spectral resonance

It is often useful to replace the exponential energy by a positive kernel. Let
\[
\kappa:\mathbb{R}\to[0,1]
\]
be a Lipschitz function with Lipschitz constant \(L_\kappa\). For example,
\[
\kappa(t)=e^{-\beta t^2}.
\]

Define the kernelized spectral resonance
\[
\boxed{
\mathcal{R}_\kappa(G,H)
=
\max_{C\in O(n)}
\frac{1}{n}
\sum_{i,j=1}^n
\kappa(\lambda_i-\mu_j)C_{ij}^2.
}
\]

### Theorem 4.2

Let \(G,G'\) be graphs on the same vertex set, with Laplacian eigenvalues \(\lambda_i\) and \(\lambda_i'\). Then
\[
\left|
\mathcal{R}_\kappa(G,H)
-
\mathcal{R}_\kappa(G',H)
\right|
\leq
\frac{L_\kappa}{n}
\sum_{i=1}^n
|\lambda_i-\lambda_i'|.
\]

Moreover, by the Hoffman-Wielandt inequality,
\[
\sum_{i=1}^n
|\lambda_i-\lambda_i'|^2
\leq
\|L_G-L_{G'}\|_{\mathrm{F}}^2,
\]
so
\[
\left|
\mathcal{R}_\kappa(G,H)
-
\mathcal{R}_\kappa(G',H)
\right|
\leq
\frac{L_\kappa}{\sqrt{n}}
\|L_G-L_{G'}\|_{\mathrm{F}}.
\]

### Proof

Let \(C\) be optimal for \(\mathcal{R}_\kappa(G,H)\). Then
\[
\mathcal{R}_\kappa(G,H)
=
\frac{1}{n}
\sum_{i,j}
\kappa(\lambda_j-\mu_i)C_{ij}^2.
\]

Using the same \(C\) as a feasible alignment for \(G'\),
\[
\mathcal{R}_\kappa(G',H)
\geq
\frac{1}{n}
\sum_{i,j}
\kappa(\lambda_j'-\mu_i)C_{ij}^2.
\]

Therefore
\[
\mathcal{R}_\kappa(G,H)-\mathcal{R}_\kappa(G',H)
\leq
\frac{1}{n}
\sum_{i,j}
\left|
\kappa(\lambda_j-\mu_i)-\kappa(\lambda_j'-\mu_i)
\right|
C_{ij}^2.
\]

By Lipschitz continuity,
\[
\left|
\kappa(\lambda_j-\mu_i)-\kappa(\lambda_j'-\mu_i)
\right|
\leq
L_\kappa |\lambda_j-\lambda_j'|.
\]

Since \(C\in O(n)\),
\[
\sum_i C_{ij}^2=1.
\]
Thus
\[
\mathcal{R}_\kappa(G,H)-\mathcal{R}_\kappa(G',H)
\leq
\frac{L_\kappa}{n}
\sum_j |\lambda_j-\lambda_j'|.
\]

Reversing the roles of \(G\) and \(G'\) gives the absolute value. The Hoffman-Wielandt inequality gives the second bound. \(\square\)

This theorem shows that structural resonance is stable under perturbations of graph weights.

---

## 4.7 Graphs of different sizes

For graphs with \(n\) and \(m\) vertices, use rectangular couplings
\[
C\in\mathbb{R}^{m\times n}
\]
satisfying
\[
C^\top C\leq I_n,
\qquad
CC^\top\leq I_m.
\]

These are partial isometries. The spectral energy remains
\[
E_L(C)
=
\sum_{i=1}^m\sum_{j=1}^n
(\mu_i-\lambda_j)^2 C_{ij}^2.
\]

This defines **partial resonance**, useful for subgraph matching, graph coarsening, and hierarchical learning.

To prevent degenerate low-rank alignments from dominating, one may include a rank regularization term
\[
-\eta \log \operatorname{rank}(C)
\]
or normalize by the effective rank.

---

# 5. Harmonic Analysis and Resonance

Structural resonance extends naturally to harmonic analysis. The central idea is that Fourier coefficients are symmetry-resolved components of a function or operator.

---

## 5.1 Fourier resonance on compact groups

Let \(G\) be a compact group with normalized Haar measure \(dg\). Let \(f,g\in L^2(G)\). For \(\pi\in\widehat{G}\), define the Fourier transform
\[
\widehat f(\pi)
=
\int_G f(x)\pi(x)^*\,dx.
\]

The Plancherel theorem gives
\[
\|f\|_{L^2(G)}^2
=
\sum_{\pi\in\widehat{G}}
d_\pi
\|\widehat f(\pi)\|_{\mathrm{HS}}^2.
\]

Because Fourier coefficients are matrix-valued, there is an internal gauge freedom. We allow unitary alignments
\[
Q_\pi\in \mathrm{U}(d_\pi).
\]

Define the **Fourier resonance**
\[
\boxed{
\mathcal{R}_{\mathrm{Fourier}}(f,g)
=
\sup_{\{Q_\pi\}}
\exp\left(
-
\frac{
\sum_{\pi\in\widehat{G}}
d_\pi
\left\|
\widehat g(\pi)-Q_\pi\widehat f(\pi)
\right\|_{\mathrm{HS}}^2
}{
\|f\|_2^2+\|g\|_2^2
}
\right).
}
\]

This measures the maximal alignment of the spectral components of \(f\) and \(g\).

---

## 5.2 Translation invariance

Let \(L_a f(x)=f(a^{-1}x)\) denote left translation. Then
\[
\widehat{L_a f}(\pi)
=
\pi(a)\widehat f(\pi).
\]

Similarly, for right translation \(R_a f(x)=f(xa)\),
\[
\widehat{R_a f}(\pi)
=
\widehat f(\pi)\pi(a).
\]

Therefore, if \(g=L_a f\), choose
\[
Q_\pi=\pi(a),
\]
and the Fourier resonance energy vanishes:
\[
\mathcal{R}_{\mathrm{Fourier}}(f,L_a f)=1.
\]

More generally, if
\[
g(x)=f(a^{-1}xb),
\]
then
\[
\widehat g(\pi)
=
\pi(a)\widehat f(\pi)\pi(b),
\]
and resonance is obtained by left and right unitary alignments.

Thus Fourier resonance identifies functions modulo symmetry orbits. It generalizes equality on quotient spaces.

---

## 5.3 Homogeneous spaces

Let \(X=G/K\) be a compact homogeneous space. The space \(L^2(G/K)\) decomposes into \(K\)-spherical representations:
\[
L^2(G/K)
\cong
\bigoplus_{\pi\in\widehat{G}_K}
V_\pi\otimes (V_\pi^K)^*.
\]

Here \(\widehat{G}_K\) denotes the set of irreducible representations with nonzero \(K\)-fixed vectors.

The resonance functional restricts to spherical components. The relevant multiplicity spaces are the spaces of \(K\)-fixed vectors. Thus harmonic resonance on homogeneous spaces is the representation-theoretic resonance of Section 3 applied to spherical data.

---

## 5.4 Manifolds and heat resonance

Let \(M\) be a compact Riemannian manifold with Laplace-Beltrami operator \(\Delta_M\). Let
\[
0=\lambda_0\leq \lambda_1\leq\lambda_2\leq\cdots
\]
be its eigenvalues, with orthonormal eigenfunctions \(\phi_j\).

A purely spectral resonance may be defined using a spectral measure
\[
\mu_M
=
\sum_{j=0}^\infty a_j\delta_{\lambda_j},
\]
where \(a_j\geq 0\) are weights, for example heat weights
\[
a_j=e^{-\tau\lambda_j}.
\]

Given a positive kernel
\[
\kappa(\lambda,\mu)=e^{-\beta(\lambda-\mu)^2},
\]
define
\[
\boxed{
\mathcal{R}_{\mathrm{spec}}(M,N)
=
\frac{
\iint \kappa(\lambda,\mu)\,d\mu_M(\lambda)d\mu_N(\mu)
}{
\sqrt{
\iint \kappa(\lambda,\mu)\,d\mu_M(\lambda)d\mu_M(\mu)
}
\sqrt{
\iint \kappa(\lambda,\mu)\,d\mu_N(\lambda)d\mu_N(\mu)
}
}.
}
\]

This measures spectral compatibility without requiring a pointwise correspondence between manifolds.

To include geometry, one may use heat operators. For a map or coupling \(\Phi\) between function spaces, define
\[
E_{\mathrm{heat}}(\Phi)
=
\frac{
\int_0^T w(t)
\left\|
e^{-t\Delta_N}\Phi-\Phi e^{-t\Delta_M}
\right\|_{\mathrm{HS}}^2
dt
}{
\int_0^T w(t)
\left(
\|e^{-t\Delta_M}\|_{\mathrm{HS}}^2+
\|e^{-t\Delta_N}\|_{\mathrm{HS}}^2
\right)
dt
}.
\]

Then
\[
\mathcal{R}_{\mathrm{heat}}(M,N)
=
\sup_{\Phi}
\exp\left(
-\lambda_{\mathrm{heat}} E_{\mathrm{heat}}(\Phi)
\right).
\]

This is the diffusion-theoretic analogue of graph resonance.

---

# 6. Machine Learning Applications

Structural Resonance Theory provides a mathematical foundation for symmetry-aware learning.

---

## 6.1 Resonance kernels

Given a dataset of structured objects
\[
\{A_i\}_{i=1}^N,
\]
define the resonance kernel
\[
K(A_i,A_j)
=
\mathcal{R}(A_i,A_j)^\gamma,
\qquad
\gamma>0.
\]

For graphs, one may use
\[
K_{\mathrm{graph}}(G_i,G_j)
=
\mathcal{R}_{\mathrm{spec}}(G_i,G_j)
\]
or a learned weighted combination of spectral, adjacency, and feature resonances.

Such kernels can be used in support vector machines, Gaussian processes, kernel ridge regression, and graph classification.

---

## 6.2 Resonance distance and contrastive learning

Define
\[
d_{\mathcal{R}}(A,B)
=
-\log \mathcal{R}(A,B).
\]

A triplet resonance loss is
\[
\boxed{
\mathcal{L}_{\mathrm{triplet}}
=
\left[
d_{\mathcal{R}}(A,A^+)
-
d_{\mathcal{R}}(A,A^-)
+
m
\right]_+,
}
\]
where \(A^+\) is structurally compatible with \(A\), \(A^-\) is incompatible, and \(m>0\) is a margin.

An InfoNCE-style resonance loss is
\[
\boxed{
\mathcal{L}_{\mathrm{NCE}}
=
-\log
\frac{
\exp(\mathcal{R}(A,A^+)/\tau)
}{
\sum_{k}
\exp(\mathcal{R}(A,A_k)/\tau)
}.
}
\]

Because \(\mathcal{R}\in[0,1]\), one may also use logit coordinates
\[
s(A,B)=\log\frac{\mathcal{R}(A,B)}{1-\mathcal{R}(A,B)}
\]
for temperature scaling.

---

## 6.3 Equivariant neural networks as resonance matchers

Let \(G\) be a symmetry group. A neural network layer
\[
F:V_{\mathrm{in}}\to V_{\mathrm{out}}
\]
is \(G\)-equivariant if
\[
F(\rho_{\mathrm{in}}(g)x)
=
\rho_{\mathrm{out}}(g)F(x)
\]
for all \(g\in G\). In other words, \(F\) is an intertwiner.

The weights of such a layer are invariant tensors in
\[
\operatorname{Hom}_G(
V_{\mathrm{in}}\otimes W,
V_{\mathrm{out}}
),
\]
where \(W\) is a parameter space. By Schur’s lemma and Clebsch-Gordan decomposition, only certain irreducible channels are admissible.

SRT gives a natural diagnostic: a learned representation \(F(x)\) resonates with a target structure \(Y\) if
\[
\mathcal{R}(F(x),Y)
\]
is high. One may train with a symmetry regularization term
\[
\mathcal{L}_{\mathrm{sym}}
=
1-\mathcal{R}_{\mathrm{sym}}(F(x),Y).
\]

This encourages the multiplicity profile of the learned representation to match the symmetry profile of the task.

---

## 6.4 Graph neural networks and spectral resonance

For graph-structured data, SRT suggests a layer of resonance-aware readout. Given graph embeddings \(Z_G\in\mathbb{R}^{n\times d}\), define a resonance similarity
\[
\mathcal{R}_{\mathrm{spec},Z}(G,H)
=
\max_{C\in O(n)}
\exp\left(
-\lambda_L E_L(C)
-\lambda_Z E_Z(C)
\right),
\]
where
\[
E_Z(C)
=
\|V^\top Z_H-CU^\top Z_G\|_{\mathrm{F}}^2.
\]

This is differentiable if the orthogonal maximization is replaced by a soft assignment, for example a Sinkhorn relaxation:
\[
C_{ij}
\approx
\exp\left(
-\beta(\mu_i-\lambda_j)^2
\right)
\]
followed by row and column normalization.

Such resonance layers can be inserted into graph neural networks to compare global spectral structure rather than only local neighborhood aggregation.

---

## 6.5 Generalization effect

Resonance-based representations are invariant or equivariant under internal symmetry groups. This reduces the effective dimensionality of the learning problem.

Let \(G\) act on an input space \(X\). If a feature map
\[
\Phi:X\to \mathcal{H}
\]
is \(G\)-invariant, it factors through the quotient:
\[
X\longrightarrow X/G\longrightarrow \mathcal{H}.
\]

For finite \(G\), under uniformity assumptions, the effective covering number satisfies
\[
\mathcal{N}(\varepsilon,X/G)
\lesssim
\frac{\mathcal{N}(\varepsilon,X)}{|G|}.
\]

Thus symmetry-compatible resonance can reduce sample complexity. More generally, resonance encourages learning on the space of structural orbits rather than on raw configurations.

---

# 7. Variational Structure of Resonance

The resonance functional is variational. Its critical points satisfy equations that generalize eigenvalue alignment and orthogonal Procrustes conditions.

Consider the spectral graph energy
\[
E(Q)
=
\|L_HQ-QL_G\|_{\mathrm{F}}^2,
\qquad
Q\in O(n).
\]

Expand:
\[
E(Q)
=
\operatorname{Tr}(Q^\top L_H^2Q)
+
\operatorname{Tr}(L_G^2)
-
2\operatorname{Tr}(Q^\top L_H Q L_G).
\]

The Euclidean gradient is
\[
\nabla E(Q)
=
2\left(
L_H^2Q+QL_G^2-2L_HQL_G
\right).
\]

The Riemannian gradient on \(O(n)\) is obtained by projecting onto the tangent space:
\[
\operatorname{grad}_{O(n)}E
=
\nabla E
-
Q\operatorname{sym}(Q^\top \nabla E),
\]
where
\[
\operatorname{sym}(X)=\frac{X+X^\top}{2}.
\]

Therefore critical points satisfy
\[
\boxed{
Q^\top
\left(
L_H^2Q+QL_G^2-2L_HQL_G
\right)
\in \operatorname{Sym}(n).
}
\]

In the eigenbasis, with \(C=V^\top Q U\), the energy is
\[
E(C)
=
\sum_{i,j}
(\mu_i-\lambda_j)^2 C_{ij}^2.
\]

The Euclidean gradient has entries
\[
(\nabla E)_{ij}
=
2(\mu_i-\lambda_j)^2 C_{ij}.
\]

The orthogonality constraint gives the stationarity condition
\[
\operatorname{skew}(C^\top \nabla E)=0.
\]

Thus resonance alignments are solutions of a nonlinear eigen-alignment problem. In the hard limit where the spectrum is simple and the weights strongly penalize mismatch, the solutions approach permutations matching close eigenvalues.

---

# 8. Illustrative Examples

## 8.1 Cycle graphs

Let \(C_n\) be the unweighted cycle graph on \(n\) vertices. Its Laplacian eigenvalues are
\[
\lambda_k
=
2-2\cos\left(\frac{2\pi k}{n}\right),
\qquad
k=0,\dots,n-1.
\]

If \(n=m\), then \(C_n\cong C_m\), and
\[
\mathcal{R}_{\mathrm{spec}}(C_n,C_m)=1.
\]

If \(n\) and \(m\) are large and close, the spectra are close in normalized Hausdorff or Wasserstein sense, and the spectral resonance is high. If \(n\) and \(m\) differ substantially, the resonance decreases.

The automorphism group of \(C_n\) is the dihedral group \(D_n\). Representation-theoretic resonance detects whether the two cycle structures share compatible dihedral symmetry sectors.

---

## 8.2 Complete and empty graphs

Let \(K_n\) be the complete graph. Its Laplacian eigenvalues are
\[
0,\quad n,\dots,n.
\]

Let \(E_n\) be the empty graph. Its Laplacian is zero, with all eigenvalues equal to \(0\).

The spectral overlap is concentrated at the zero eigenvalue. After normalization, the resonance is low if the nonzero spectrum is weighted strongly. Thus SRT distinguishes highly connected and disconnected structures even though both are simple.

---

## 8.3 Representations of \(S^1\)

Let \(G=S^1\). The irreducible representations are one-dimensional characters
\[
\chi_m(e^{i\theta})=e^{im\theta},
\qquad
m\in\mathbb{Z}.
\]

Let
\[
A=V_1\oplus V_2,
\qquad
B=V_1\oplus V_3.
\]

The multiplicity vectors are
\[
m_A=(1,1,0),
\qquad
m_B=(1,0,1)
\]
on the modes \((1,2,3)\).

With unit weights,
\[
\mathcal{R}_{\mathrm{sym}}(A,B)
=
\frac{1}{\sqrt{2}\sqrt{2}}
=
\frac{1}{2}.
\]

Thus the two representations share one symmetry channel and differ in another.

If instead
\[
A=V_1\oplus V_{-1},
\qquad
B=V_1\oplus V_{-1},
\]
then
\[
\mathcal{R}_{\mathrm{sym}}(A,B)=1.
\]

---

## 8.4 Isospectral manifolds

There exist non-isometric Riemannian manifolds with identical Laplace spectra. For such manifolds,
\[
\mathcal{R}_{\mathrm{spec}}(M,N)=1
\]
if only spectral data are used.

If eigenfunction tensors, heat kernels, or curvature tensors are included, the resonance may drop below \(1\). This illustrates a key point of SRT: resonance depends on the chosen structural data. Equivalence with respect to one level of structure need not imply equivalence at a deeper level.

---

# 9. Conceptual Implications

Structural Resonance Theory changes the foundational relation between mathematical objects.

In classical settings:
\[
A\sim B
\quad
\Longleftrightarrow
\quad
\text{\(A\) and \(B\) are equivalent}.
\]

In SRT:
\[
\mathcal{R}(A,B)\in[0,1]
\quad
\Longleftrightarrow
\quad
\text{\(A\) and \(B\) resonate to degree \(\mathcal{R}(A,B)\)}.
\]

Equivalence becomes the special case
\[
A\cong B
\quad
\Longrightarrow
\quad
\mathcal{R}(A,B)=1.
\]

The theory suggests a hierarchy of structural relations:

1. **Isomorphism:** exact equality of all structure.
2. **Resonance:** existence of a low-energy alignment.
3. **Partial resonance:** alignment of substructures or shared symmetry sectors.
4. **Spectral resonance:** agreement of operators after alignment.
5. **Symmetry resonance:** agreement of representation-theoretic content.
6. **Tensor resonance:** agreement of invariant higher-order data.

This hierarchy is not merely philosophical. It yields computable functionals in graph theory, harmonic analysis, and machine learning.

---

# 10. Conclusion

We have introduced Structural Resonance Theory, a framework in which the primary relation between mathematical structures is not equivalence but resonance.

The central construction is the resonance functional
\[
\mathcal{R}(A,B)
=
\sup_{\mu,\Phi}
\exp(-S(A,B;\mu,\Phi)),
\]
where the action measures failure of an alignment \(\Phi\) to preserve internal symmetries, spectral operators, and invariant tensors.

The main results are:

1. An axiomatic definition of structured Hilbertian objects and resonance functionals.
2. A representation-theoretic formula relating symmetry resonance to normalized character inner products and intertwiner spaces.
3. A spectral graph resonance formula reducing to an orthogonal Procrustes problem over eigenbases.
4. Stability estimates for perturbed Laplacians.
5. A harmonic analysis formulation using Fourier coefficients and Plancherel theory.
6. Machine learning applications, including resonance kernels, contrastive losses, and equivariant representation learning.

The central message is that structure is not best understood through rigid equivalence classes, but through the spectrum of possible resonances between internal symmetries.

Equivalence is the boundary case. Resonance is the general law.

---

# References

1. A. A. Kirillov, *Elements of the Theory of Representations*, Springer, 1976.  
2. J.-P. Serre, *Linear Representations of Finite Groups*, Springer, 1977.  
3. W. Fulton and J. Harris, *Representation Theory: A First Course*, Springer, 1991.  
4. B. C. Hall, *Lie Groups, Lie Algebras, and Representations*, Springer, 2015.  
5. F. R. K. Chung, *Spectral Graph Theory*, American Mathematical Society, 1997.  
6. A. Grigor’yan, *Heat Kernel and Analysis on Manifolds*, American Mathematical Society, 2009.  
7. M. M. Bronstein, J. Bruna, Y. LeCun, A. Szlam, P. Vandergheynst, “Geometric Deep Learning: Going beyond Euclidean Data,” *IEEE Signal Processing Magazine*, 2017.  
8. R. Kondor and T. Smidt, “Generalization to Symmetric Groups and Equivariant Convolutional Networks,” *ICML*, 2018.  
9. H. Maron et al., “Invariant and Equivariant Graph Networks,” *ICLR*, 2019.  
10. P. Ramachandran, P. Fatourou, and M. Bronstein, “Geometric Deep Learning: Grids, Groups, Graphs, Geodesics, and Gauges,” 2021.
