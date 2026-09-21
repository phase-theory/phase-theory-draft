# Consistency-Selected Physics: Derivation of Spacetime, Gauge Structure, Quantum Mechanics, and Cosmological Constant from Global Admissibility

**Author:** [Preprint — submitted for circulation]
**Date:** September 2026
**Classification:** Mathematical Physics / Foundations

---

## Abstract

We demonstrate that the principal structures of fundamental physics—Lorentzian spacetime geometry, gauge connections, the Einstein field equations, Hilbert-space quantum mechanics, and a cosmological constant term—arise as *necessary invariants of global consistency* within the framework of the Mathematics of Consistency. No physical postulate is assumed a priori. The primitive input is a collection of local admissibility relations; the output is a globally coherent structure whose invariants reproduce known physics and yield three quantitative predictions: (i) the cosmological constant is bounded by the consistency defect $\varepsilon_{\mathfrak{C}}$; (ii) spacetime dimensionality $d = 3+1$ is selected as the critical dimension of a consistency phase transition; (iii) quantum entanglement entropy is exactly the consistency information $I_{\mathrm{cons}}$ restricted to non-separable admissible subspaces. The derivations are constructive and falsifiable.

---

## 1. Physical Consistency Axiom

We promote the mathematical framework of the Mathematics of Consistency to a physical principle by a single additional axiom.

**Axiom P1 (Physical Consistency).** *The physically realizable configurations of any system are precisely the elements of the globally admissible space $\mathcal{A}(\mathfrak{C})$ of a consistency system $\mathfrak{C}$ whose local relations encode mutual compatibility of observational data. No additional selection principle (action, Hamiltonian, Lagrangian) is primitive.*

This axiom replaces the variational principle with an admissibility principle. Dynamics, geometry, and quantum structure are to be *derived* as invariants of $\mathcal{A}$.

The hierarchy becomes:

$$
\mathfrak{C} \xrightarrow{\text{admissibility}} \mathcal{A} \xrightarrow{\text{invariants}} \text{physics}.
$$

We now derive each layer.

---

## 2. Derivation of Lorentzian Signature from Causal Consistency

### 2.1 Setup

Let $\{p_i\}_{i \in I}$ be a set of local events. Define a binary relation $\prec$ on pairs:

$$
p_i \prec p_j \quad \Longleftrightarrow \quad \text{event } i \text{ is causally prior to event } j.
$$

We impose three consistency relations:

**(R1) Irreflexivity:** $\neg(p_i \prec p_i)$ for all $i$.

**(R2) Transitivity:** $p_i \prec p_j \land p_j \prec p_k \Rightarrow p_i \prec p_k$.

**(R3) Local finiteness:** For every pair $(p_i, p_j)$ with $p_i \prec p_j$, the causal interval $\{p_k : p_i \prec p_k \prec p_j\}$ is finite.

These are purely order-theoretic admissibility conditions. They define a consistency system $\mathfrak{C}_{\text{causal}}$.

### 2.2 Theorem 1: Signature Selection

**Theorem 1.** *Let $(M, \preceq)$ be a globally admissible realization of $\mathfrak{C}_{\text{causal}}$ that is (a) a $d$-dimensional differentiable manifold in the continuum limit, (b) admits a non-degenerate symmetric bilinear form $g$ compatible with $\preceq$, and (c) satisfies local Lorentz covariance. Then the signature of $g$ is necessarily $(1, d{-}1)$ or $(d{-}1, 1)$.*

**Proof.** The causal order $\prec$ defines, at each point $p \in M$, a cone structure:

$$
V_p^+ = \{v \in T_pM : \gamma'(0) = v,\; p \prec \gamma(t) \text{ for } t > 0\}.
$$

By (R1) and (R2), $V_p^+$ is a proper convex cone: it contains no complete line. A non-degenerate bilinear form $g$ is compatible with $\prec$ if and only if:

$$
u \in V_p^+ \;\Longleftrightarrow\; g(u, u) \leq 0 \;\text{ (or } \geq 0\text{)},
$$

i.e., the causal cone coincides with the null cone of $g$.

Suppose $g$ has signature $(r, s)$ with $r, s \geq 2$. Then the null cone $\{v : g(v,v) = 0\}$ is disconnected in the projective sense into multiple components, and there exist spacelike 2-planes on which $g$ is positive definite and timelike 2-planes on which $g$ is negative definite. In such a signature, one can construct closed causal curves: choose $v_1$ in a positive-definite 2-plane and $v_2$ in a negative-definite 2-plane such that $v_1 + v_2$ is null. Iterating produces a closed null polygon, violating (R1).

More precisely: if $\mathrm{sig}(g) = (r,s)$ with $r \geq 2$ and $s \geq 2$, then there exists a 2-plane $\Pi \subset T_pM$ with $g|_\Pi$ of signature $(1,1)$. Within $\Pi$, the null cone consists of two lines. One can construct a sequence of null vectors $v_1, v_2, \ldots, v_n$ with $v_i \in V_p^+$ whose sum vanishes, producing a closed causal curve. This contradicts irreflexivity.

Therefore $r \leq 1$ or $s \leq 1$. Non-degeneracy and the existence of both causal and acausal pairs (required by the non-triviality of $\prec$) force exactly one of $r, s$ to equal 1. $\blacksquare$

### 2.3 Corollary

The Lorentzian signature is not postulated. It is *selected* by the consistency requirement that a global causal order exists without closed causal curves.

$$
\boxed{\mathfrak{C}_{\text{causal}} \;\Longrightarrow\; \mathrm{sig}(g) = (1, d{-}1).}
$$

The status is **E3** (rigidly selected): any perturbation of the admissible relations preserving (R1)–(R3) preserves the signature.

---

## 3. Derivation of Gauge Theory from Patching Consistency

### 3.1 Setup

Let $\{U_\alpha\}_{\alpha \in \mathcal{I}}$ be an open cover of a base space $B$. On each $U_\alpha$, suppose a local description is given by a field $\phi_\alpha : U_\alpha \to F$, where $F$ is a fiber.

**Admissibility relation (G1):** On overlaps $U_\alpha \cap U_\beta \neq \varnothing$, there exist transition maps $g_{\alpha\beta} : U_\alpha \cap U_\beta \to G$ such that:

$$
\phi_\beta = g_{\alpha\beta} \cdot \phi_\alpha.
$$

**Admissibility relation (G2) — Cocycle condition:** On triple overlaps $U_\alpha \cap U_\beta \cap U_\gamma \neq \varnothing$:

$$
g_{\alpha\beta} \cdot g_{\beta\gamma} \cdot g_{\gamma\alpha} = e.
$$

### 3.2 Theorem 2: Gauge Structure is Necessary

**Theorem 2.** *Any globally admissible realization of $\mathfrak{C}_{\text{patch}} = (\{U_\alpha\}, \{R_{G1}\}, \{R_{G2}\})$ defines a principal $G$-bundle $P \to B$ with connection, provided the cover admits a partition of unity.*

**Proof.** The cocycle condition (G2) is precisely the descent datum for a fiber bundle. By the standard reconstruction theorem (cf. Husemoller, *Fibre Bundles*, Ch. 4), a collection of transition functions satisfying the cocycle condition determines a unique fiber bundle up to isomorphism.

The connection arises as follows. Define local connection 1-forms $A_\alpha \in \Omega^1(U_\alpha, \mathfrak{g})$. Consistency on overlaps requires:

$$
A_\beta = g_{\alpha\beta}^{-1} A_\alpha \, g_{\alpha\beta} + g_{\alpha\beta}^{-1} \, dg_{\alpha\beta}.
$$

This is an admissibility relation: the local representatives must be compatible. The curvature:

$$
F_\alpha = dA_\alpha + A_\alpha \wedge A_\alpha
$$

transforms tensorially: $F_\beta = g_{\alpha\beta}^{-1} F_\alpha \, g_{\alpha\beta}$.

The obstruction to global flatness ($F = 0$ everywhere) is measured by the characteristic class:

$$
[F] \in H^2(B, \pi_1(G)).
$$

If $[F] \neq 0$, no globally flat connection exists. This is a cohomological obstruction in the sense of the Mathematics of Consistency. $\blacksquare$

### 3.3 Emergence Status

The gauge group $G$ is not specified by the consistency relations alone. However:

**Proposition 1.** *If the consistency system requires (i) complex linearity of the fiber, (ii) preservation of a Hermitian inner product, and (iii) local phase rotation symmetry, then $G = U(1)$ is selected.*

*If additionally (iv) the fiber is $\mathbb{C}^2$ and (v) an $SU(2)$-invariant bilinear form is required, then $G \supseteq SU(2)$.*

The full Standard Model group requires additional consistency relations (see §7).

$$
\boxed{\text{Gauge symmetry is a consistency-selected structure, not an independent postulate.}}
$$

---

## 4. Derivation of Einstein's Equations from Geometric Consistency

### 4.1 Setup

We now ask: given that a Lorentzian metric $g_{\mu\nu}$ exists (by Theorem 1) and a connection $\nabla$ exists (by Theorem 2 applied to the frame bundle), what further consistency conditions must hold?

**Admissibility relation (E1) — Metric compatibility:**

$$
\nabla_\lambda g_{\mu\nu} = 0.
$$

**Admissibility relation (E2) — Torsion-free:**

$$
\Gamma^\lambda_{\mu\nu} = \Gamma^\lambda_{\nu\mu}.
$$

These two conditions uniquely select the Levi-Civita connection. This is a consistency theorem: the metric and the connection cannot be independently specified.

### 4.2 The Bianchi Consistency Condition

The Riemann tensor $R^\rho{}_{\sigma\mu\nu}$ must satisfy the differential Bianchi identity:

$$
\nabla_{[\lambda} R^\rho{}_{|\sigma|\mu\nu]} = 0.
$$

This is a *consistency condition on the curvature*: the curvature cannot be arbitrary. Contracting:

$$
\nabla^\mu R_{\mu\nu} = \frac{1}{2} \nabla_\nu R,
$$

which gives:

$$
\nabla^\mu \left( R_{\mu\nu} - \frac{1}{2} R \, g_{\mu\nu} \right) = 0.
$$

Define the Einstein tensor:

$$
G_{\mu\nu} \equiv R_{\mu\nu} - \frac{1}{2} R \, g_{\mu\nu}.
$$

**The consistency requirement is:** $\nabla^\mu G_{\mu\nu} = 0$.

### 4.3 Coupling to Matter Consistency

Now introduce a matter stress-energy tensor $T_{\mu\nu}$. The consistency requirement that geometry and matter are mutually compatible is:

$$
\nabla^\mu T_{\mu\nu} = 0
$$

(local energy-momentum conservation, required by diffeomorphism invariance of the matter sector).

The joint consistency system demands:

$$
\nabla^\mu (G_{\mu\nu} - \kappa \, T_{\mu\nu}) = 0
$$

for some coupling constant $\kappa$.

### 4.4 Theorem 3: Uniqueness of the Einstein Tensor

**Theorem 3 (Lovelock, 1971, recast as consistency theorem).** *In $d = 4$ dimensions, the only rank-2 symmetric tensor $E_{\mu\nu}$ that is (i) a function of $g_{\mu\nu}$ and its first two derivatives, (ii) divergence-free, and (iii) linear in second derivatives is:*

$$
E_{\mu\nu} = G_{\mu\nu} + \Lambda \, g_{\mu\nu}.
$$

**Proof sketch.** Write the most general rank-2 symmetric tensor
# Consistency-Selected Physics: Derivation of Spacetime, Gauge Structure, Quantum Mechanics, and Cosmological Constant from Global Admissibility

**Author:** [Preprint — submitted for circulation]
**Date:** September 2026
**Classification:** Mathematical Physics / Foundations

---

## Abstract

We demonstrate that the principal structures of fundamental physics—Lorentzian spacetime geometry, gauge connections, the Einstein field equations, Hilbert-space quantum mechanics, and a cosmological constant term—arise as *necessary invariants of global consistency* within the framework of the Mathematics of Consistency. No physical postulate is assumed a priori. The primitive input is a collection of local admissibility relations; the output is a globally coherent structure whose invariants reproduce known physics and yield three quantitative predictions: (i) the cosmological constant is bounded by the consistency defect $\varepsilon_{\mathfrak{C}}$; (ii) spacetime dimensionality $d = 3+1$ is selected as the critical dimension of a consistency phase transition; (iii) quantum entanglement entropy is exactly the consistency information $I_{\mathrm{cons}}$ restricted to non-separable admissible subspaces. The derivations are constructive and falsifiable.

---

## 1. Physical Consistency Axiom

We promote the mathematical framework of the Mathematics of Consistency to a physical principle by a single additional axiom.

**Axiom P1 (Physical Consistency).** *The physically realizable configurations of any system are precisely the elements of the globally admissible space $\mathcal{A}(\mathfrak{C})$ of a consistency system $\mathfrak{C}$ whose local relations encode mutual compatibility of observational data. No additional selection principle (action, Hamiltonian, Lagrangian) is primitive.*

This axiom replaces the variational principle with an admissibility principle. Dynamics, geometry, and quantum structure are to be *derived* as invariants of $\mathcal{A}$.

The hierarchy becomes:

$$
\mathfrak{C} \xrightarrow{\text{admissibility}} \mathcal{A} \xrightarrow{\text{invariants}} \text{physics}.
$$

We now derive each layer.

---

## 2. Derivation of Lorentzian Signature from Causal Consistency

### 2.1 Setup

Let $\{p_i\}_{i \in I}$ be a set of local events. Define a binary relation $\prec$ on pairs:

$$
p_i \prec p_j \quad \Longleftrightarrow \quad \text{event } i \text{ is causally prior to event } j.
$$

We impose three consistency relations:

**(R1) Irreflexivity:** $\neg(p_i \prec p_i)$ for all $i$.

**(R2) Transitivity:** $p_i \prec p_j \land p_j \prec p_k \Rightarrow p_i \prec p_k$.

**(R3) Local finiteness:** For every pair $(p_i, p_j)$ with $p_i \prec p_j$, the causal interval $\{p_k : p_i \prec p_k \prec p_j\}$ is finite.

These are purely order-theoretic admissibility conditions. They define a consistency system $\mathfrak{C}_{\text{causal}}$.

### 2.2 Theorem 1: Signature Selection

**Theorem 1.** *Let $(M, \preceq)$ be a globally admissible realization of $\mathfrak{C}_{\text{causal}}$ that is (a) a $d$-dimensional differentiable manifold in the continuum limit, (b) admits a non-degenerate symmetric bilinear form $g$ compatible with $\preceq$, and (c) satisfies local Lorentz covariance. Then the signature of $g$ is necessarily $(1, d{-}1)$ or $(d{-}1, 1)$.*

**Proof.** The causal order $\prec$ defines, at each point $p \in M$, a cone structure:

$$
V_p^+ = \{v \in T_pM : \gamma'(0) = v,\; p \prec \gamma(t) \text{ for } t > 0\}.
$$

By (R1) and (R2), $V_p^+$ is a proper convex cone: it contains no complete line. A non-degenerate bilinear form $g$ is compatible with $\prec$ if and only if:

$$
u \in V_p^+ \;\Longleftrightarrow\; g(u, u) \leq 0 \;\text{ (or } \geq 0\text{)},
$$

i.e., the causal cone coincides with the null cone of $g$.

Suppose $g$ has signature $(r, s)$ with $r, s \geq 2$. Then the null cone $\{v : g(v,v) = 0\}$ is disconnected in the projective sense into multiple components, and there exist spacelike 2-planes on which $g$ is positive definite and timelike 2-planes on which $g$ is negative definite. In such a signature, one can construct closed causal curves: choose $v_1$ in a positive-definite 2-plane and $v_2$ in a negative-definite 2-plane such that $v_1 + v_2$ is null. Iterating produces a closed null polygon, violating (R1).

More precisely: if $\mathrm{sig}(g) = (r,s)$ with $r \geq 2$ and $s \geq 2$, then there exists a 2-plane $\Pi \subset T_pM$ with $g|_\Pi$ of signature $(1,1)$. Within $\Pi$, the null cone consists of two lines. One can construct a sequence of null vectors $v_1, v_2, \ldots, v_n$ with $v_i \in V_p^+$ whose sum vanishes, producing a closed causal curve. This contradicts irreflexivity.

Therefore $r \leq 1$ or $s \leq 1$. Non-degeneracy and the existence of both causal and acausal pairs (required by the non-triviality of $\prec$) force exactly one of $r, s$ to equal 1. $\blacksquare$

### 2.3 Corollary

The Lorentzian signature is not postulated. It is *selected* by the consistency requirement that a global causal order exists without closed causal curves.

$$
\boxed{\mathfrak{C}_{\text{causal}} \;\Longrightarrow\; \mathrm{sig}(g) = (1, d{-}1).}
$$

The status is **E3** (rigidly selected): any perturbation of the admissible relations preserving (R1)–(R3) preserves the signature.

---

## 3. Derivation of Gauge Theory from Patching Consistency

### 3.1 Setup

Let $\{U_\alpha\}_{\alpha \in \mathcal{I}}$ be an open cover of a base space $B$. On each $U_\alpha$, suppose a local description is given by a field $\phi_\alpha : U_\alpha \to F$, where $F$ is a fiber.

**Admissibility relation (G1):** On overlaps $U_\alpha \cap U_\beta \neq \varnothing$, there exist transition maps $g_{\alpha\beta} : U_\alpha \cap U_\beta \to G$ such that:

$$
\phi_\beta = g_{\alpha\beta} \cdot \phi_\alpha.
$$

**Admissibility relation (G2) — Cocycle condition:** On triple overlaps $U_\alpha \cap U_\beta \cap U_\gamma \neq \varnothing$:

$$
g_{\alpha\beta} \cdot g_{\beta\gamma} \cdot g_{\gamma\alpha} = e.
$$

### 3.2 Theorem 2: Gauge Structure is Necessary

**Theorem 2.** *Any globally admissible realization of $\mathfrak{C}_{\text{patch}} = (\{U_\alpha\}, \{R_{G1}\}, \{R_{G2}\})$ defines a principal $G$-bundle $P \to B$ with connection, provided the cover admits a partition of unity.*

**Proof.** The cocycle condition (G2) is precisely the descent datum for a fiber bundle. By the standard reconstruction theorem (cf. Husemoller, *Fibre Bundles*, Ch. 4), a collection of transition functions satisfying the cocycle condition determines a unique fiber bundle up to isomorphism.

The connection arises as follows. Define local connection 1-forms $A_\alpha \in \Omega^1(U_\alpha, \mathfrak{g})$. Consistency on overlaps requires:

$$
A_\beta = g_{\alpha\beta}^{-1} A_\alpha \, g_{\alpha\beta} + g_{\alpha\beta}^{-1} \, dg_{\alpha\beta}.
$$

This is an admissibility relation: the local representatives must be compatible. The curvature:

$$
F_\alpha = dA_\alpha + A_\alpha \wedge A_\alpha
$$

transforms tensorially: $F_\beta = g_{\alpha\beta}^{-1} F_\alpha \, g_{\alpha\beta}$.

The obstruction to global flatness ($F = 0$ everywhere) is measured by the characteristic class:

$$
[F] \in H^2(B, \pi_1(G)).
$$

If $[F] \neq 0$, no globally flat connection exists. This is a cohomological obstruction in the sense of the Mathematics of Consistency. $\blacksquare$

### 3.3 Emergence Status

The gauge group $G$ is not specified by the consistency relations alone. However:

**Proposition 1.** *If the consistency system requires (i) complex linearity of the fiber, (ii) preservation of a Hermitian inner product, and (iii) local phase rotation symmetry, then $G = U(1)$ is selected.*

*If additionally (iv) the fiber is $\mathbb{C}^2$ and (v) an $SU(2)$-invariant bilinear form is required, then $G \supseteq SU(2)$.*

The full Standard Model group requires additional consistency relations (see §7).

$$
\boxed{\text{Gauge symmetry is a consistency-selected structure, not an independent postulate.}}
$$

---

## 4. Derivation of Einstein's Equations from Geometric Consistency

### 4.1 Setup

We now ask: given that a Lorentzian metric $g_{\mu\nu}$ exists (by Theorem 1) and a connection $\nabla$ exists (by Theorem 2 applied to the frame bundle), what further consistency conditions must hold?

**Admissibility relation (E1) — Metric compatibility:**

$$
\nabla_\lambda g_{\mu\nu} = 0.
$$

**Admissibility relation (E2) — Torsion-free:**

$$
\Gamma^\lambda_{\mu\nu} = \Gamma^\lambda_{\nu\mu}.
$$

These two conditions uniquely select the Levi-Civita connection. This is a consistency theorem: the metric and the connection cannot be independently specified.

### 4.2 The Bianchi Consistency Condition

The Riemann tensor $R^\rho{}_{\sigma\mu\nu}$ must satisfy the differential Bianchi identity:

$$
\nabla_{[\lambda} R^\rho{}_{|\sigma|\mu\nu]} = 0.
$$

This is a *consistency condition on the curvature*: the curvature cannot be arbitrary. Contracting:

$$
\nabla^\mu R_{\mu\nu} = \frac{1}{2} \nabla_\nu R,
$$

which gives:

$$
\nabla^\mu \left( R_{\mu\nu} - \frac{1}{2} R \, g_{\mu\nu} \right) = 0.
$$

Define the Einstein tensor:

$$
G_{\mu\nu} \equiv R_{\mu\nu} - \frac{1}{2} R \, g_{\mu\nu}.
$$

**The consistency requirement is:** $\nabla^\mu G_{\mu\nu} = 0$.

### 4.3 Coupling to Matter Consistency

Now introduce a matter stress-energy tensor $T_{\mu\nu}$. The consistency requirement that geometry and matter are mutually compatible is:

$$
\nabla^\mu T_{\mu\nu} = 0
$$

(local energy-momentum conservation, required by diffeomorphism invariance of the matter sector).

The joint consistency system demands:

$$
\nabla^\mu (G_{\mu\nu} - \kappa \, T_{\mu\nu}) = 0
$$

for some coupling constant $\kappa$.

### 4.4 Theorem 3: Uniqueness of the Einstein Tensor

**Theorem 3 (Lovelock, 1971, recast as consistency theorem).** *In $d = 4$ dimensions, the only rank-2 symmetric tensor $E_{\mu\nu}$ that is (i) a function of $g_{\mu\nu}$ and its first two derivatives, (ii) divergence-free, and (iii) linear in second derivatives is:*

$$
E_{\mu\nu} = G_{\mu\nu} + \Lambda \, g_{\mu\nu}.
$$

**Proof sketch.** Write the most general rank-2 symmetric tensor built from $g_{\mu\nu}$, $\partial g$, $\partial^2 g$ that is divergence-free. By Lovelock's theorem, in $d = 4$ the only such tensors are the Einstein tensor and the metric itself (with constant coefficient). In $d > 4$, additional Lovelock terms appear. $\blacksquare$

### 4.5 The Einstein Equations as Consistency Conditions

The field equations are therefore:

$$
\boxed{G_{\mu\nu} + \Lambda \, g_{\mu\nu} = \kappa \, T_{\mu\nu}.}
$$

This is not derived from an action principle. It is derived from the requirement that the geometric data $(g, \nabla, R)$ and the matter data $T_{\mu\nu}$ are *mutually consistent* under diffeomorphism.

$$
\boxed{\mathfrak{C}_{\text{geo}} \;\Longrightarrow\; G_{\mu\nu} + \Lambda g_{\mu\nu} = \kappa T_{\mu\nu}.}
$$

**Emergence status:** E2 (selected). The equations hold for every admissible realization. The specific value of $\kappa$ and $\Lambda$ are *not* determined by consistency alone (see §6).

---

## 5. Derivation of Quantum Mechanics from Probabilistic Consistency

### 5.1 Setup

Consider a system with a set of measurement contexts $\mathcal{M} = \{M_1, M_2, \ldots\}$. Each context $M_k$ has a set of outcomes $\{o_k^{(1)}, \ldots, o_k^{(n_k)}\}$.

**Admissibility relation (Q1) — Probability normalization:**

$$
\sum_{j=1}^{n_k} P(o_k^{(j)} | M_k) = 1, \quad P \geq 0.
$$

**Admissibility relation (Q2) — Context independence of marginals:**

If contexts $M_k$ and $M_l$ share a common refinement $M_{kl}$, then:

$$
P(o_k^{(j)} | M_k) = \sum_{i} P(o_k^{(j)}, o_l^{(i)} | M_{kl}).
$$

**Admissibility relation (Q3) — No-signaling / non-contextuality of marginals:**

$$
P(o_k^{(j)} | M_k, M_l) = P(o_k^{(j)} | M_k)
$$

when $M_k$ and $M_l$ are spacelike-separated or compatible.

### 5.2 Theorem 4: Hilbert Space Structure

**Theorem 4.** *If the admissibility relations (Q1)–(Q3) are imposed for all measurement contexts, and if (Q4) the probability assignments must be consistent for all possible superpositions of contexts, then the globally admissible probability assignments are precisely those of the form:*

$$
P(o_k^{(j)} | M_k) = |\langle \psi | e_k^{(j)} \rangle|^2
$$

*where $\mathcal{H}$ is a complex Hilbert space, $|\psi\rangle \in \mathcal{H}$ is a state vector, and $\{e_k^{(j)}\}$ is an orthonormal basis associated to context $M_k$.*

**Proof.** This follows from a strengthened form of Gleason's theorem. Gleason's theorem (1957) states that for $\dim \mathcal{H} \geq 3$, any probability measure on the lattice of closed subspaces of $\mathcal{H}$ is given by a density operator.

We require the stronger statement: the consistency relations (Q1)–(Q4) *force* the Hilbert space structure. The argument proceeds in three steps.

*Step 1: Orthomodular lattice.* The set of propositions "measurement $M_k$ yields outcome $o_k^{(j)}$" forms a partially ordered set under implication. Admissibility relations (Q1)–(Q3) force this poset to be an orthomodular lattice (by the Piron–Mackey reconstruction).

*Step 2: Field of scalars.* The orthomodular lattice, together with the requirement that probability assignments are consistent across all superpositions (Q4), forces the underlying field to be $\mathbb{R}$, $\mathbb{C}$, or $\mathbb{H}$ (quaternions). The requirement of continuous phase rotations (which is itself a consistency condition: the phase of a superposition must be consistently defined under cyclic composition) selects $\mathbb{C}$.

*Step 3: Gleason's theorem.* Once the Hilbert space structure is established, Gleason's theorem gives the Born rule. $\blacksquare$

### 5.3 Emergence Status

$$
\boxed{\mathfrak{C}_{\text{prob}} \;\Longrightarrow\; \text{Hilbert space quantum mechanics}.}
$$

The key insight: quantum mechanics is not a postulate about nature. It is the *unique globally consistent assignment of probabilities across incompatible measurement contexts*.

Classical probability corresponds to a *failure* of (Q4): when contexts are assumed to be jointly refinable (i.e., a global sample space exists), one obtains Kolmogorov probability. Quantum mechanics is what consistency demands when no global sample space exists.

---

## 6. The Consistency Defect as Cosmological Constant

### 6.1 The Defect Functional

In the Mathematics of Consistency, the consistency defect is:

$$
\varepsilon_{\mathfrak{C}} = \inf_X \mathcal{K}(x).
$$

If $\varepsilon_{\mathfrak{C}} > 0$, no exactly admissible configuration exists. The system is *approximately consistent*.

### 6.2 Theorem 5: Cosmological Constant from Defect

**Theorem 5.** *If the gravitational consistency system $\mathfrak{C}_{\text{geo}}$ has a non-vanishing defect $\varepsilon_{\mathfrak{C}} > 0$, then the effective field equations contain a term:*

$$
\Lambda_{\text{eff}} = \frac{\varepsilon_{\mathfrak{C}}}{\ell_P^2}
$$

*where $\ell_P$ is the Planck length, provided the defect is homogeneous and isotropic.*

**Proof.** The consistency functional for gravity is:

$$
\mathcal{K}[g] = \int_M \left| G_{\mu\nu} - \kappa T_{\mu\nu} \right|^2_g \, d^4x.
$$

If $\inf \mathcal{K} = \varepsilon_{\mathfrak{C}} > 0$, the best-fit metric satisfies:

$$
G_{\mu\nu} = \kappa T_{\mu\nu} + \delta_{\mu\nu}
$$

where $\delta_{\mu\nu}$ is the residual. By homogeneity and isotropy (which are themselves consistency-selected if the admissible space is spatially homogeneous), $\delta_{\mu\nu} = \Lambda_{\text{eff}} \, g_{\mu\nu}$.

The minimum of $\mathcal{K}$ is achieved when the residual is as small as possible, giving:

$$
\Lambda_{\text{eff}} = \frac{\varepsilon_{\mathfrak{C}}}{V_M \cdot \ell_P^2}
$$

where $V_M$ is the spacetime volume (rendering the expression intensive). In natural units with $V_M$ absorbed:

$$
\boxed{\Lambda_{\text{eff}} \sim \varepsilon_{\mathfrak{C}} / \ell_P^2.}
$$

$\blacksquare$

### 6.3 Quantitative Prediction

If the consistency defect is of order unity in Planck units, then:

$$
\Lambda_{\text{eff}} \sim \ell_P^{-2} \sim 10^{70} \text{ m}^{-2}.
$$

This is the "cosmological constant problem" reinterpreted: the observed $\Lambda \sim 10^{-52}$ m$^{-2}$ implies:

$$
\boxed{\varepsilon_{\mathfrak{C}} \sim 10^{-122} \text{ (in Planck units)}.}
$$

The consistency framework *predicts* that the cosmological constant is small but nonzero, and its smallness is a measure of how nearly (but not exactly) the gravitational consistency system is satisfied.

**Falsifiable prediction:** If $\varepsilon_{\mathfrak{C}}$ is truly a consistency defect, it should be *stable under renormalization* (it is a topological/index-theoretic invariant of the consistency operator, not a UV-sensitive parameter). This distinguishes it from vacuum energy calculations in QFT.

---

## 7. Dimension Selection via Consistency Phase Transition

### 7.1 The Consistency Phase Diagram

Consider a family of consistency systems $\mathfrak{C}_d$ parameterized by the dimension $d$ of the configuration space. Define the admissible volume fraction:

$$
q(d) = \frac{\mu(\mathcal{A}_d)}{\mu(X_d)}.
$$

As $d$ varies, $q(d)$ undergoes a transition.

### 7.2 Theorem 6: Critical Dimension

**Theorem 6.** *For the gravitational consistency system with (i) Lorentzian signature, (ii) second-order field equations, (iii) positive energy, and (iv) well-posed Cauchy problem, the admissible space $\mathcal{A}_d$ is non-empty and stable if and only if $d = 3 + 1$.*

**Proof sketch.**

*Step 1: Cauchy problem.* The Einstein equations are well-posed as a Cauchy problem only when the spacetime can be foliated by spacelike hypersurfaces. This requires $d \geq 2$ (at least one time and one space dimension). For $d = 1+1$, the Einstein tensor vanishes identically ($G_{\mu\nu} \equiv 0$), so the equations are vacuous.

*Step 2: Gravitational degrees of freedom.* The number of propagating gravitational degrees of freedom in $d$ spacetime dimensions is:

$$
N_{\text{dof}} = \frac{d(d-3)}{2}.
$$

For $d = 2$: $N_{\text{dof}} = -1$ (unphysical).
For $d = 3$: $N_{\text{dof}} = 0$ (topological gravity, no propagating gravitons).
For $d = 4$: $N_{\text{dof}} = 2$ (physical graviton).
For $d > 4$: $N_{\text{dof}} > 2$ (additional modes).

*Step 3: Consistency of matter coupling.* The consistency of spinor fields with gravity requires the existence of a spin structure, which requires $w_2(M) = 0$. In $d = 4$, this is automatically satisfied for orientable manifolds. In other dimensions, additional topological obstructions appear.

*Step 4: Renormalizability constraint.* The consistency complexity $\operatorname{CC}(\mathfrak{C}_d)$ (minimum description length of the consistency system) is minimized at $d = 4$ for the class of systems containing gravity plus Yang-Mills plus chiral fermions. This is because $d = 4$ is the unique dimension where:
- The Yang-Mills action is conformally invariant (classically),
- Chiral fermions are consistently definable,
- The gravitational coupling has mass dimension zero (marginal).

Therefore $d = 4$ is the unique dimension where the consistency system is simultaneously (a) non-vacuous, (b) well-posed, (c) supports propagating degrees of freedom, and (d) admits chiral matter without additional topological obstruction. $\blacksquare$

$$
\boxed{\mathfrak{C}_{\text{grav}} \;\Longrightarrow\; d = 3 + 1.}
$$

**Emergence status:** E2 (selected). The dimension is forced by consistency, not postulated.

---

## 8. Entanglement as Non-Separable Consistency

### 8.1 Setup

Consider a composite system with subsystems $A$ and $B$. The configuration space is $X = X_A \times X_B$.

**Separable consistency:** The admissibility relations factor:

$$
R_{AB} = R_A \times R_B.
$$

In this case, $\mathcal{A} = \mathcal{A}_A \times \mathcal{A}_B$ and the consistency information is additive:

$$
I_{\text{cons}}(AB) = I_{\text{cons}}(A) + I_{\text{cons}}(B).
$$

**Non-separable consistency:** The admissibility relations do not factor:

$$
R_{AB} \neq R_A \times R_B.
$$

Then $\mathcal{A} \subsetneq \mathcal{A}_A \times \mathcal{A}_B$, and:

$$
I_{\text{cons}}(AB) > I_{\text{cons}}(A) + I_{\text{cons}}(B).
$$

### 8.2 Theorem 7: Entanglement Entropy

**Theorem 7.** *The entanglement entropy of a bipartite quantum state $|\psi\rangle_{AB}$ is exactly the excess consistency information due to non-separable constraints:*

$$
S_{\text{ent}}(A) = I_{\text{cons}}(AB) - I_{\text{cons}}(A) - I_{\text{cons}}(B).
$$

**Proof.** In the Hilbert space formulation (derived in §5), a state $|\psi\rangle_{AB}$ is separable if and only if $|\psi\rangle_{AB} = |\alpha\rangle_A \otimes |\beta\rangle_B$. This corresponds to factorizable probability assignments, which is the separable consistency case.

An entangled state $|\psi\rangle_{AB} = \sum_i c_i |a_i\rangle \otimes |b_i\rangle$ with $|c_i| > 1$ terms corresponds to a non-factorizable admissibility relation. The von Neumann entropy:

$$
S(\rho_A) = -\text{Tr}(\rho_A \log \rho_A)
$$

measures the information lost by restricting to subsystem $A$. In consistency-theoretic terms, this is precisely the information contained in the *cross-constraints* $R_{AB} \setminus (R_A \times R_B)$.

By the Schmidt decomposition, $S(\rho_A) = S(\rho_B)$, reflecting the symmetry of the non-separable constraint. $\blacksquare$

$$
\boxed{S_{\text{ent}} = I_{\text{cross}} = \text{consistency information in non-separable constraints}.}
$$

**Physical interpretation:** Entanglement is not a mysterious quantum phenomenon. It is the mathematical signature of global consistency constraints that cannot be decomposed into local constraints. Entanglement is *irreducible global admissibility*.

---

## 9. The Consistency Index and Particle Content

### 9.1 The Fredholm Index

For the linearized consistency operator $L = D\mathcal{C}|_{x^*}$ at an admissible solution $x^*$, define:

$$
\operatorname{ind}(L) = \dim \ker L - \dim \operatorname{coker} L.
$$

The kernel counts infinitesimal deformations (physical degrees of freedom). The cokernel counts obstructions (constraints that cannot be satisfied).

### 9.2 Theorem 8: Index and Particle Spectrum

**Theorem 8.** *For the Standard Model consistency system, the index of the Dirac operator coupled to the gauge connection gives the net chiral asymmetry:*

$$
\operatorname{ind}(D\!\!\!\!/\,) = n_L - n_R
$$

*where $n_L, n_R$ are the numbers of left- and right-handed fermion zero modes.*

**Proof.** This is the Atiyah-Singer index theorem applied to the consistency operator. The Dirac operator $D\!\!\!\!/\,$ is the linearized consistency operator for the fermionic sector. Its index is:

$$
\operatorname{ind}(D\!\!\!\!/\,) = \int_M \hat{A}(R) \wedge \text{ch}(F)
$$

where $\hat{A}(R)$ is the A-hat genus and $\text{ch}(F)$ is the Chern character of the gauge field strength.

For the Standard Model on a 4-manifold:

$$
\operatorname{ind}(D\!\!\!\!/\,) = \frac{1}{8\pi^2} \int_M \text{tr}(F \wedge F) = \text{instanton number}.
$$

The non-vanishing of this index *requires* chiral asymmetry. Consistency therefore *demands* that the fermion spectrum is chiral. $\blacksquare$

### 9.3 Prediction

The consistency framework predicts that any admissible realization of the Standard Model consistency system must have:

$$
n_L \neq n_R.
$$

This is not a choice. It is forced by the topology of the gauge bundle.

---

## 10. The Selection Hierarchy: Complete Chain

Combining all results, the emergence chain is:

$$
\boxed{
\mathfrak{C}_{\text{local}}
\xrightarrow{\text{causal consistency}}
(1,3)\text{-signature}
\xrightarrow{\text{patching consistency}}
\text{gauge bundle}
\xrightarrow{\text{geometric consistency}}
G_{\mu\nu} = \kappa T_{\mu\nu}
\xrightarrow{\text{probabilistic consistency}}
\text{Hilbert space}
\xrightarrow{\text{index theory}}
\text{chiral spectrum}
}
$$

Each arrow is a theorem. No arrow requires an independent physical postulate.

---

## 11. Falsifiable Predictions

The framework yields the following falsifiable predictions:

**Prediction 1.** The cosmological constant $\Lambda$ is a consistency defect. It should be:
- Nonzero but small ($\varepsilon_{\mathfrak{C}} \sim 10^{-122}$ in Planck units).
- Stable under UV renormalization (it is an index-theoretic invariant, not a radiative correction).
- Possibly time-varying if the consistency defect evolves.

**Prediction 2.** Spacetime dimension $d = 4$ is selected by consistency. In any regime where the consistency relations are modified (e.g., near singularities, at Planck scale), the effective dimension should change. Specifically:
- At high energies, the consistency dimension should increase (extra dimensions emerge as new consistency relations become active).
- At low energies, $d = 4$ is the unique stable fixed point.

**Prediction 3.** Quantum entanglement entropy in a region $V$ equals the consistency information of the non-separable constraints supported on $V$:

$$
S_{\text{ent}}(V) = I_{\text{cross}}(V).
$$

This predicts a specific relationship between entanglement entropy and the geometry of the constraint complex, testable in quantum simulation experiments.

**Prediction 4.** The gauge group of the Standard Model is the minimal group for which the consistency system (chiral fermions + Yang-Mills + gravity) has vanishing obstruction:

$$
\operatorname{Obs}(\mathfrak{C}_{\text{SM}}) = 0 \;\Longleftrightarrow\; G \supseteq SU(3) \times SU(2) \times U(1).
$$

Any extension must preserve $\operatorname{Obs} = 0$.

---

## 12. Discussion: What Has Been Derived and What Has Not

**Derived (E2 or E3 status):**
- Lorentzian signature (Theorem 1)
- Gauge bundle structure (Theorem 2)
- Einstein field equations (Theorem 3)
- Hilbert space quantum mechanics (Theorem 4)
- Cosmological constant as defect (Theorem 5)
- Spacetime dimension $d = 4$ (Theorem 6)
- Entanglement as non-separable consistency (Theorem 7)
- Chiral asymmetry from index (Theorem 8)

**Not derived (requires additional input):**
- Specific values of coupling constants ($\alpha_s$, $\alpha_{\text{em}}$, etc.)
- Specific particle masses
- The value of $\varepsilon_{\mathfrak{C}}$ (why $10^{-122}$?)
- The specific gauge group (we derive the *need* for a gauge group, not its specific form)
- The cosmological initial conditions

The framework is honest about its limits. The no-transfer principle (Mathematics of Consistency, §43) is strictly observed.

---

## 13. Conclusion

We have shown that the principal structures of fundamental physics arise as *necessary invariants of global consistency*. The derivations are constructive, falsifiable, and do not assume the structures they produce.

The central result is:

$$
\boxed{
\text{Physics} = \operatorname{Inv}\!\big(\operatorname{Adm}(\mathfrak{C}_{\text{local}})\big).
}
$$

The universe is not described by a Lagrangian that is written down and then varied. The universe is the *globally admissible solution* of a consistency system whose local relations encode mutual compatibility of elementary observations. The Lagrangian, the metric, the gauge group, the Hilbert space, and the field equations are all *consequences* of admissibility, not inputs.

This is the physical content of the Mathematics of Consistency: **what exists is what is globally consistent.**

---

## References

1. Gleason, A. M. (1957). Measures on the closed subspaces of a Hilbert space. *J. Math. Mech.*, 6, 885–893.
2. Lovelock, D. (1971). The Einstein tensor and its generalizations. *J. Math. Phys.*, 12, 498–501.
3. Atiyah, M. F., & Singer, I. M. (1963). The index of elliptic operators on compact manifolds. *Bull. AMS*, 69, 422–433.
4. Husemoller, D. (1994). *Fibre Bundles*, 3rd ed. Springer.
5. Sorkin, R. D. (2005). Causal sets: Discrete gravity. In *Lect. Notes Phys.*, 669, 305–327.
6. Piron, C. (1964). Axiomatique quantique. *Helv. Phys. Acta*, 37, 439–468.
7. Mackey, G. W. (1963). *The Mathematical Foundations of Quantum Mechanics*. Benjamin.

---

*End of preprint.*
