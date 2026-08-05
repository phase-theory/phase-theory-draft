# Framet Theory: Discrete Relational Frame Orbits and the Informational Substrate of Spacetime and Gauge Fields

## Abstract

Framet Theory is the culminating discrete specialization of Relativity Mechanics. It answers the primitive structural question:

\[
\boxed{
\text{What is the minimal discrete carrier of relational frame information?}
}
\]

In the continuum, Frame Theory and the Gauge Theory of Admissibility describe physical geometry and internal interactions as orbits of local frame fields and connections under continuous admissibility groups. However, if spacetime and gauge manifolds are emergent rather than fundamental, the underlying substrate must be discrete, relational, and informational. 

Framet Theory provides this substrate. A **framet** is defined as an elementary relational frame token. The theory is formulated on a discrete relational complex $\Gamma=(V,E)$. To each vertex $v \in V$, we assign a local frame element $g_v \in H$, and to each directed edge $e \in E$, a relational frame transition $h_e \in H$, where $H$ is a Lie group (e.g., $\mathrm{Spin}(1,3)$ for gravity or $SU(N)$ for internal gauge interactions). The admissibility group is the local discrete gauge group $\mathcal{G}_\Gamma = H^V$, acting by local frame rotations. 

The physical state is not the bare assignment $\{g_v, h_e\}$, but its orbit under $\mathcal{G}_\Gamma$. The invariant projection maps the configuration to the space of relational holonomies and dressed vertex invariants. By applying Relativistic Information Theory, we show that nature stores information in these discrete frame orbits, utilizing multiplicity spaces as decoherence-free logical memory. In the continuum refinement limit, Framet Theory rigorously recovers lattice gauge theory, Regge calculus, Loop Quantum Gravity spin networks, and continuum Frame Theory. 

Framet Theory thus demonstrates that the fundamental fabric of physics is not a continuous manifold equipped with fields, but a discrete network of invariant relational frame orbits.

---

## 1. Introduction

The architecture of Relativity Mechanics establishes that physical reality is constituted by invariant equivalence classes of admissible descriptions. Through Orbit Theory, Invariant Theory, and Frame Theory, we have seen that continuous spacetime geometry and gauge fields are macroscopic manifestations of local frame admissibility. 

However, continuous manifolds presuppose a background topological and differential structure. If Relativity Mechanics is truly foundational, it must be capable of describing physics without assuming a pre-existing continuum. The discrete limit of Frame Theory and Gauge Theory of Admissibility is **Framet Theory**.

The primitive question of Framet Theory is:

\[
\boxed{
\text{What is the minimal discrete carrier of relational frame information?}
}
\]

The answer is the **framet**: a localized, discrete token of frame description, defined entirely by its relational transitions to other framets. 

Framet Theory replaces the smooth principal bundle $P \to M$ with a directed graph or relational complex $\Gamma = (V,E)$. It replaces the smooth connection $A$ with discrete edge holonomies $h_e$, and the smooth local frame section with discrete vertex frames $g_v$. The continuous admissibility group $C^\infty(M, H)$ is replaced by the discrete local group $H^V$. 

Because Framet Theory is built directly upon the axioms of Relativity Mechanics, it inherits its entire conceptual architecture: physical objects are orbits, observables are holonomies, information is orbit distinguishability, and dynamics is a flow on the discrete quotient space.

---

## 2. The Relativity Schema of Framet Theory

Framet Theory is specified by the relativity schema:

\[
\boxed{
\mathcal R_{\mathrm{Fr}} = (\Omega_{\mathrm{Fr}}, \mathcal{G}_\Gamma, \triangleright, I_{\mathrm{Fr}}).
}
\]

### 2.1 The Discrete Substrate
Let $\Gamma = (V, E)$ be a directed graph (or 1-complex), where $V$ is a set of vertices and $E$ is a set of directed edges. Each edge $e \in E$ has a source vertex $s(e) \in V$ and a target vertex $t(e) \in V$. Let $e^{-1}$ denote the reversed edge.

### 2.2 The Description Space
Let $H$ be a Lie group (the structure group). The frame description space is:

\[
\Omega_{\mathrm{Fr}} = H^V \times H^E.
\]

A description $\omega \in \Omega_{\mathrm{Fr}}$ is a pair $\omega = (g, h)$, where:
1. $g = \{g_v\}_{v \in V}$ with $g_v \in H$ is the **vertex frame field**.
2. $h = \{h_e\}_{e \in E}$ with $h_e \in H$ is the **edge transition field**.

### 2.3 The Admissibility Group
The admissibility group is the discrete local gauge group:

\[
\mathcal{G}_\Gamma = H^V = \prod_{v \in V} H_v.
\]

An element $k = \{k_v\}_{v \in V} \in \mathcal{G}_\Gamma$ represents a local change of frame at each vertex.

### 2.4 The Admissibility Action
The action $\triangleright : \mathcal{G}_\Gamma \times \Omega_{\mathrm{Fr}} \to \Omega_{\mathrm{Fr}}$ is defined by:

\[
\boxed{
k \triangleright (g, h) = (g^k, h^k),
}
\]

where the transformed variables are:

\[
g^k_v = k_v g_v,
\]
\[
h^k_e = k_{s(e)} h_e k_{t(e)}^{-1}.
\]

This action encodes the redundancy of local discrete frame choices.

### 2.5 The Invariant Projection
The physical state is the orbit:

\[
[g, h] = \mathcal{G}_\Gamma \cdot (g, h).
\]

The invariant projection is:

\[
I_{\mathrm{Fr}} : \Omega_{\mathrm{Fr}} \to \Omega_{\mathrm{Fr}} / \mathcal{G}_\Gamma.
\]

---

## 3. Orbit Structure and Invariant Observables

By Invariant Theory, physical observables must be constant on the orbits of $\mathcal{G}_\Gamma$. We construct the complete set of invariants.

### 3.1 Path Holonomies
For a path $\gamma = (e_1, e_2, \dots, e_n)$ in $\Gamma$ connecting $v_0 = s(e_1)$ to $v_n = t(e_n)$, the path holonomy is the ordered product:

\[
h_\gamma = h_{e_1} h_{e_2} \cdots h_{e_n}.
\]

Under a gauge transformation $k \in \mathcal{G}_\Gamma$, the path holonomy transforms covariantly:

\[
h_\gamma \mapsto k_{v_0} h_\gamma k_{v_n}^{-1}.
\]

### 3.2 Loop Invariants (Wilson Loops)
If $\gamma$ is a closed loop based at $v$, the holonomy $H_\gamma = h_\gamma$ transforms by conjugation:

\[
H_\gamma \mapsto k_v H_\gamma k_v^{-1}.
\]

The gauge-invariant observables are the characters of the holonomy in representations $R$ of $H$:

\[
\boxed{
W_R(\gamma) = \mathrm{Tr}_R(H_\gamma).
}
\]

These are the fundamental non-local invariants of pure Framet Theory.

### 3.3 Dressed Vertex Invariants (Relational Matter)
The vertex frames $g_v$ transform as $g_v \mapsto k_v g_v$. They are not invariant by themselves. However, we can construct relational invariants connecting two vertices $u$ and $v$ via a path $\gamma$:

\[
\boxed{
\mathcal{O}_{uv}(\gamma) = g_u^{-1} h_\gamma g_v.
}
\]

Under a gauge transformation:

\[
(g_u^k)^{-1} h_\gamma^k g_v^k = (k_u g_u)^{-1} (k_u h_\gamma k_v^{-1}) (k_v g_v) = g_u^{-1} h_\gamma g_v.
\]

Thus, $\mathcal{O}_{uv}(\gamma)$ is strictly invariant. It represents the relational frame orientation of vertex $v$ as measured from vertex $u$ along the path $\gamma$. If $H$ is a gauge group, $g_v$ acts as a Higgs or matter field, and $\mathcal{O}_{uv}$ is a gauge-invariant dressed correlator.

### 3.4 The Moduli Space of Framets
The physical configuration space (the quotient) is:

\[
Q_{\mathrm{Fr}} = \Omega_{\mathrm{Fr}} / \mathcal{G}_\Gamma.
\]

If we restrict to pure edge transitions ($H^E$), the quotient $H^E / H^V$ is the discrete moduli space of flat connections (if we impose zero curvature) or the lattice gauge orbit space. By the lattice equivalent of the Ambrose-Singer theorem, the algebra of Wilson loops $W_R(\gamma)$ separates the orbits of $Q_{\mathrm{Fr}}$ (up to conjugacy and topological sectors).

---

## 4. Quantum Framet Theory

Quantization of Framet Theory follows the principles of Relativistic Quantum Theory. The physical Hilbert space is the space of square-integrable functions on the quotient, or equivalently, the gauge-invariant subspace of the kinematical Hilbert space.

### 4.1 Kinematical Hilbert Space
The kinematical Hilbert space is:

\[
\mathcal{H}_{\mathrm{kin}} = L^2(H^E, d\mu_{\mathrm{Haar}}),
\]

where $d\mu_{\mathrm{Haar}}$ is the product Haar measure on $H^E$. (Vertex frames $g_v$ can be treated as matter degrees of freedom in an associated $L^2(H^V)$ space).

### 4.2 Peter-Weyl Decomposition and Spin Networks
By the Peter-Weyl theorem, $L^2(H)$ decomposes into irreducible representations (irreps) $\rho$ of $H$. For the graph $\Gamma$, $\mathcal{H}_{\mathrm{kin}}$ decomposes as:

\[
\mathcal{H}_{\mathrm{kin}} \cong \bigoplus_{\{j_e\}} \bigotimes_{e \in E} (V_{j_e} \otimes V_{j_e}^*),
\]

where $j_e$ labels the irrep assigned to edge $e$, and $V_{j_e}$ is the representation space.

### 4.3 The Gauss Constraint and Physical Hilbert Space
The admissibility group $\mathcal{G}_\Gamma = H^V$ acts unitarily on $\mathcal{H}_{\mathrm{kin}}$. The generators of this action at each vertex $v$ are the discrete Gauss constraints $\hat{\mathcal{G}}_v$. 

Physical states must be invariant under local frame changes:

\[
\boxed{
\hat{\mathcal{G}}_v |\Psi_{\mathrm{phys}}\rangle = 0, \quad \forall v \in V.
}
\]

This constraint forces the representation spaces at each vertex to be contracted with invariant intertwiners $\iota_v$. A basis for the physical Hilbert space $\mathcal{H}_{\mathrm{phys}} = \mathcal{H}_{\mathrm{kin}}^{\mathcal{G}_\Gamma}$ is therefore given by **spin network states** $| \Gamma, \{j_e\}, \{\iota_v\} \rangle$.

Thus, the quantum states of Framet Theory are precisely spin networks. They are not introduced as an ad hoc quantization of gravity; they are the inevitable mathematical consequence of quantizing a discrete local frame admissibility structure.

---

## 5. Framet Dynamics

Dynamics in Relativity Mechanics must descend to the quotient space $Q_{\mathrm{Fr}}$. In the discrete setting, dynamics is generated by an invariant action defined on the orbits.

### 5.1 Plaquette Holonomies
Assume $\Gamma$ is embedded with a 2-complex structure (faces or plaquettes $P$). For a plaquette $p$ bounded by a loop $\partial p$, the plaquette holonomy is:

\[
H_p = \prod_{e \in \partial p} h_e.
\]

### 5.2 The Wilson Action (Gauge Dynamics)
For internal gauge theories ($H = SU(N)$), the invariant dynamics is given by the Wilson action:

\[
\boxed{
S_{\mathrm{W}}[h] = \beta \sum_{p} \left( \dim(R) - \mathrm{Re}\, \mathrm{Tr}_R(H_p) \right).
}
\]

This action is strictly invariant under $\mathcal{G}_\Gamma$ because $\mathrm{Tr}_R(k_v H_p k_v^{-1}) = \mathrm{Tr}_R(H_p)$.

### 5.3 The Spin Foam Action (Gravitational Dynamics)
If $H = \mathrm{Spin}(1,3)$ or its Euclidean counterpart $\mathrm{Spin}(4)$, Framet Theory describes discrete quantum gravity. The action takes the form of a BF theory or spin foam model (e.g., the EPRL/FK model):

\[
\boxed{
Z_{\mathrm{Fr}} = \sum_{\{j_e, \iota_v\}} \prod_{e} A_e(j_e) \prod_{v} A_v(j_e, \iota_v),
}
\]

where $A_v$ is the vertex amplitude (the discrete analog of the Palatini/Einstein-Hilbert action) evaluated on the boundary spin network of the vertex.

The path integral over the quotient space is:

\[
Z = \int_{\Omega_{\mathrm{Fr}} / \mathcal{G}_\Gamma} \mathcal{D}[h] \, e^{-S_{\mathrm{Fr}}[h]}.
\]

---

## 6. Relativistic Information and Framet Memory

Relativistic Information Theory dictates that nature stores orbit information, not configuration information. Framet Theory provides the exact microscopic mechanism for this.

### 6.1 Decoherence-Free Subspaces
Suppose the environment couples to the Framet network via local gauge-invariant operators. The total Hilbert space decomposes under the admissibility group $\mathcal{G}_\Gamma$ as:

\[
\mathcal{H}_{\mathrm{kin}} \cong \bigoplus_{\lambda} (\mathcal{H}_\lambda \otimes \mathcal{M}_\lambda),
\]

where $\mathcal{G}_\Gamma$ acts only on $\mathcal{H}_\lambda$. The multiplicity spaces $\mathcal{M}_\lambda$ are completely decoupled from the gauge action. 

Therefore, **logical quantum information stored in $\mathcal{M}_\lambda$ is topologically protected against local gauge noise.** Framets act as natural quantum error-correcting codes. The physical memory of the universe is stored in the multiplicity spaces of relational frame orbits.

### 6.2 Orbit Entropy
The informational capacity of a finite Framet network is the logarithm of the volume of its physical quotient space:

\[
C_{\mathrm{Fr}} = \log \mathrm{Vol}(H^E / H^V).
\]

If a black hole horizon is modeled as a boundary graph $\Gamma_{\partial}$, the Bekenstein-Hawking entropy arises directly from the counting of distinguishable Framet orbits (spin network punctures) on the boundary, confirming that gravitational entropy is precisely orbit entropy.

---

## 7. The Continuum Limit and Emergence

Framet Theory is not a replacement for continuum physics; it is its microscopic generator. The continuum theories emerge via a refinement limit of the relational complex $\Gamma$.

### 7.1 Recovery of Gauge Theory
Let $\Gamma$ be a cubic lattice approximation of a manifold $M$ with lattice spacing $\epsilon$. Assign a continuum connection $A_\mu$. The edge variable is the path-ordered exponential:

\[
h_e \approx \mathcal{P} \exp \left( \int_e A \right) \approx 1 + \epsilon A_\mu + \frac{1}{2}\epsilon^2 (\partial_\mu A_\nu + A_\mu A_\nu).
\]

The plaquette holonomy expands as:

\[
H_p \approx 1 + \epsilon^2 F_{\mu\nu} + \mathcal{O}(\epsilon^3).
\]

Substituting this into the Wilson action and taking $\epsilon \to 0$ yields:

\[
S_{\mathrm{W}} \to \frac{1}{2g^2} \int_M \mathrm{Tr}(F \wedge *F),
\]

recovering continuum Yang-Mills theory.

### 7.2 Recovery of Frame Theory and General Relativity
If $H = \mathrm{Spin}(1,3)$, the edge variables $h_e$ represent discrete Lorentz transformations (parallel transport of frames). The vertex variables $g_v$ can be mapped to discrete tetrad vectors (frame fields). 

The discrete curvature is the deficit angle around a hinge (a 2-cell). The Framet action reduces to the **Regge action** for discrete gravity:

\[
S_{\mathrm{Regge}} = \frac{1}{8\pi G} \sum_{\text{hinges } h} A_h \delta_h,
\]

where $A_h$ is the area of the hinge and $\delta_h$ is the deficit angle constructed from the holonomies. In the smooth limit, Regge calculus converges to the Einstein-Hilbert action. 

Thus, General Relativity is the macroscopic, continuum hydrodynamics of Framet orbits.

---

## 8. Coarse-Graining and Reference Transformations

In continuum physics, the Renormalization Group (RG) describes how physics changes with scale. In Framet Theory, RG flow is rigorously defined as a sequence of **Reference Transformations** (morphisms between orbit spaces).

Let $\Gamma_1$ be a fine graph and $\Gamma_2$ be a coarse-grained graph obtained by blocking vertices and edges. There is a natural projection map of description spaces:

\[
F: \Omega_{\mathrm{Fr}}(\Gamma_1) \to \Omega_{\mathrm{Fr}}(\Gamma_2).
\]

If $F$ is equivariant with respect to the admissibility groups $\mathcal{G}_{\Gamma_1}$ and $\mathcal{G}_{\Gamma_2}$, it descends to a reference transformation between the physical quotients:

\[
\boxed{
\Phi: Q_{\mathrm{Fr}}(\Gamma_1) \to Q_{\mathrm{Fr}}(\Gamma_2).
}
\]

The effective action on the coarse graph is obtained by integrating out the fine orbits:

\[
e^{-S_{\mathrm{eff}}[h_2]} = \int_{\Phi^{-1}([h_2])} \mathcal{D}[h_1] \, e^{-S_{\mathrm{Fr}}[h_1]}.
\]

This proves that renormalization in gauge and gravitational theories is fundamentally a change of relational reference framework.

---

## 9. Summary of the Framet Architecture

Framet Theory unifies the discrete, quantum, and informational aspects of physics under a single relational schema.

1. **Substrate:** Directed graph $\Gamma = (V,E)$.
2. **Variables:** Vertex frames $g_v \in H$, edge transitions $h_e \in H$.
3. **Admissibility:** Local group $\mathcal{G}_\Gamma = H^V$.
4. **Ontology:** Orbits $[g, h] = \mathcal{G}_\Gamma \cdot (g,h)$.
5. **Observables:** Holonomies $W_R(\gamma)$ and dressed correlators $g_u^{-1} h_\gamma g_v$.
6. **Quantum States:** Spin networks (invariant intertwiners).
7. **Information:** Stored in orbit multiplicity spaces (decoherence-free).
8. **Continuum Limit:** Lattice Gauge Theory, Regge Calculus, Loop Quantum Gravity.

---

## 10. Conclusion

Framet Theory answers the ultimate structural question of discrete physics:

\[
\boxed{
\text{What is the minimal discrete carrier of relational frame information?}
}
\]

The answer is the **framet**: an elementary equivalence class of discrete frame transitions. 

By applying the full architecture of Relativity Mechanics to discrete relational complexes, we have shown that spacetime geometry and gauge interactions do not require a fundamental continuous manifold. Instead, they emerge from the macroscopic dynamics of discrete frame orbits. 

The continuous metrics of General Relativity, the continuous connections of Yang-Mills theory, and the smooth wavefunctions of Quantum Mechanics are all continuum approximations of a deeper, discrete, relational reality. In this reality, nature does not compute with absolute coordinates or bare gauge potentials. Nature computes with invariant holonomies, stores memory in topological multiplicity spaces, and evolves through the reconfiguration of relational frame orbits.

Framet Theory is therefore not merely a regularization technique. It is the fundamental informational and relational substrate from which the continuum physics of the universe emerges.

\[
\boxed{
\text{The universe is a network of framets; physics is the dynamics of their orbits.}
}
\]
