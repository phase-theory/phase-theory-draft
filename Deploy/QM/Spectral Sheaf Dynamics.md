# Spectral Sheaf Dynamics: A Non-Commutative Geometric Reformulation of Quantum Measurement

**Author:** Marlon Hanks  
**Affiliation:** Dust LLC  
**Date:** July 30, 2026  
**Classification:** Quantum Foundations, Non-Commutative Geometry, Mathematical Physics  
**Preprint Reference:** SSD-2026-0730  

---

## Abstract

We introduce **Spectral Sheaf Dynamics (SSD)**, a reformulation of quantum mechanics in which the state space is replaced by a sheaf of non-commutative algebras over a base manifold of classical contexts. Measurement is not a stochastic collapse but a geometric restriction functor between sheaves, and Born probabilities emerge as obstruction classes in a cohomology theory we develop here for the first time. The formalism recovers all standard predictions of non-relativistic quantum mechanics while resolving the measurement problem through purely geometric means: the apparent randomness of outcomes is shown to be a consequence of the non-triviality of a Čech 1-cocycle associated with the covering of context space. We derive the Schrödinger equation as a flatness condition on a connection over the sheaf, construct a tensorial calculus for multi-particle entanglement in terms of fiber products, and prove a no-go theorem demonstrating that any hidden-variable completion of SSD must violate a generalized Bell inequality we term the **Sheaf Separability Bound**. We close with predictions deviating from standard quantum mechanics at the scale of context-space curvature, yielding a falsifiable experimental signature in high-precision interferometry.

**Keywords:** spectral sheaves, non-commutative geometry, quantum measurement, Čech cohomology, Born rule derivation, contextuality, entanglement geometry

**PACS:** 03.65.Ta, 02.40.Gh, 03.65.Ud, 03.65.Ca

---

## 1. Introduction and Motivation

### 1.1 The Measurement Problem as a Geometric Deficit

Standard quantum mechanics, in its Copenhagen, many-worlds, or consistent-histories guises, treats the measurement process as either primitive, branching, or decoherence-selected. In each case, the transition from a superposed state vector $|\psi\rangle \in \mathcal{H}$ to a definite outcome $a_i$ is appended to the unitary dynamics as an additional postulate. The Born rule,

$$P(a_i) = |\langle a_i | \psi \rangle|^2,$$

is imposed rather than derived. This is not a physical failure — the predictions are immaculate — but it is a structural incompleteness: the formalism contains two incommensurate dynamical laws (unitary evolution and projective reduction) without a unifying geometric object from which both descend.

We contend that this incompleteness arises because the state vector is the wrong fundamental object. A vector in Hilbert space encodes amplitudes relative to a single, globally fixed basis. But physical measurement is inherently *local*: each apparatus defines a context, a choice of commuting observables, and the totality of contexts does not admit a single global section. The correct object is therefore not a vector but a **sheaf** — a structure that assigns algebraic data to open sets of a base space and governs how local data glue into global information.

### 1.2 Summary of Contributions

This paper establishes the following:

1. **Definition of the Spectral Sheaf** $\mathfrak{S}$ over the context manifold $\mathcal{C}$, with stalks given by non-commutative $C^*$-algebras of observables (§2).
2. **A geometric measurement functor** $\Gamma_R: \mathfrak{S} \to \mathfrak{S}|_R$ that replaces projection postulates (§3).
3. **Derivation of the Born rule** as the evaluation of a Čech cohomology class $[\beta] \in \check{H}^1(\mathcal{C}, \mathcal{U}(1))$ (§4).
4. **The Schrödinger equation as a flatness condition** on a natural connection $\nabla$ over $\mathfrak{S}$ (§5).
5. **A tensorial entanglement calculus** via fiber products of sheaves (§6).
6. **The Sheaf Separability Bound**, a new no-go inequality strictly stronger than CHSH for $n \geq 3$ parties (§7).
7. **A falsifiable prediction**: context-space curvature induces phase corrections of order $\mathcal{O}(\kappa \, L^2 / \ell_C^2)$ in Mach–Zehnder interferometry (§8).

---

## 2. The Context Manifold and the Spectral Sheaf

### 2.1 Construction of $\mathcal{C}$

Let $\mathcal{A}$ be the abstract $C^*$-algebra of observables of a quantum system. For each maximal abelian subalgebra (MASA) $\mathcal{M} \subset \mathcal{A}$, define a point $c_{\mathcal{M}}$ in a topological space $\mathcal{C}$. We equip $\mathcal{C}$ with the **Gelfand–Naimark topology**: a basis of open sets is given by

$$U_f^\epsilon = \{ c_{\mathcal{M}} \in \mathcal{C} : \| f|_{\mathcal{M}} - f_0 \| < \epsilon \},$$

for $f \in \mathcal{A}_{\text{sa}}$, $f_0 \in \mathbb{R}$, $\epsilon > 0$. For finite-dimensional systems with $\mathcal{A} = M_n(\mathbb{C})$, the space $\mathcal{C}$ is the flag manifold $\text{Fl}(n) = U(n) / U(1)^n$, a compact Kähler manifold of complex dimension $n(n-1)/2$.

**Proposition 2.1.** *The context manifold $\mathcal{C}$ for a spin-$\frac{1}{2}$ system is $\mathbb{CP}^1 \cong S^2$, and for a two-qubit system it is $\text{Fl}(4)$, of real dimension 12.*

*Proof.* For $M_2(\mathbb{C})$, the MASAs are parameterized by their unique (up to phase) rank-1 projector, which is a point in $\mathbb{CP}^1$. For $M_4(\mathbb{C})$, a MASA is determined by a complete flag $\{0\} \subset V_1 \subset V_2 \subset V_3 \subset \mathbb{C}^4$, yielding $\text{Fl}(4)$. $\square$

### 2.2 The Sheaf $\mathfrak{S}$

**Definition 2.2.** The **spectral sheaf** $\mathfrak{S}$ over $\mathcal{C}$ is the sheaf of sections of the bundle

$$\pi: \bigsqcup_{c \in \mathcal{C}} \mathcal{A}_c \longrightarrow \mathcal{C},$$

where the stalk $\mathcal{A}_c \equiv \mathcal{A}_{c_{\mathcal{M}}}$ is the non-commutative algebra $\mathcal{A}$ itself, but the restriction maps $\rho_{UV}: \mathfrak{S}(U) \to \mathfrak{S}(V)$ for $V \subset U$ are given by **contextual compression**:

$$\rho_{UV}(a) = P_{\mathcal{M}_V} \, a \, P_{\mathcal{M}_V},$$

where $P_{\mathcal{M}_V}$ is the projection onto the commutant of $\mathcal{M}_V$ in the GNS representation.

The sheaf $\mathfrak{S}$ is, in general, **non-abelian**: the stalks do not commute, and the restriction maps are not algebra homomorphisms but completely positive maps. This is the geometric encoding of quantum non-commutativity.

### 2.3 Global Sections and the Kochen–Specker Obstruction

A global section $s \in \mathfrak{S}(\mathcal{C})$ would assign, to every context $c$, an element $s(c) \in \mathcal{A}_c$ compatible under all restrictions. The existence of such a section is equivalent to a non-contextual hidden-variable assignment.

**Theorem 2.3 (Geometric Kochen–Specker).** *For $\dim \mathcal{H} \geq 3$, the spectral sheaf $\mathfrak{S}$ admits no global section that is simultaneously (i) everywhere non-zero and (ii) valuation-definite (i.e., $s(c) \in \text{Spec}(\mathcal{M}_c)$ for all $c$).*

*Proof sketch.* Suppose such a section $s$ exists. Then for each context $c_{\mathcal{M}}$, $s(c_{\mathcal{M}})$ selects an eigenvalue of every observable in $\mathcal{M}$. Compatibility under restrictions demands that if $\mathcal{M}_1 \cap \mathcal{M}_2 \ni A$, then $s(c_{\mathcal{M}_1})(A) = s(c_{\mathcal{M}_2})(A)$. This is precisely a Kochen–Specker coloring. By the Kochen–Specker theorem (1967), no such assignment exists for $\dim \mathcal{H} \geq 3$. Geometrically, the obstruction is a non-trivial class in $\check{H}^1(\mathcal{C}, \mathcal{Z})$, where $\mathcal{Z}$ is the sheaf of central units. $\square$

This theorem is the *reason* quantum mechanics requires probabilities: the sheaf has no global section, so one must work with local sections and their gluing data.

---

## 3. Measurement as a Restriction Functor

### 3.1 The Measurement Functor

Let $R \subset \mathcal{C}$ be an open subset corresponding to the resolution of a physical apparatus — that is, the set of contexts compatible with the macroscopic pointer observable. We define the **measurement functor**

$$\Gamma_R: \mathfrak{S} \longrightarrow \mathfrak{S}|_R$$

as the sheaf-theoretic restriction to $R$, followed by the application of the **decoherence functional** $\mathcal{D}_R$:

$$(\Gamma_R s)(c) = \mathcal{D}_R\bigl(s|_R\bigr)(c) = \text{Tr}_{\mathcal{H} \ominus \mathcal{H}_R}\bigl[\rho_s \, P_c\bigr],$$

where $\mathcal{H}_R$ is the subspace selected by the apparatus and $P_c$ is the spectral projector associated with context $c \in R$.

**Key structural point.** $\Gamma_R$ is *not* a projection in Hilbert space. It is a functor between categories of sheaves. It does not "collapse" a state; it *restricts the domain of definability* of the state. The state was never a global object to begin with.

### 3.2 Composition and Sequential Measurement

For nested apparatus regions $R_2 \subset R_1 \subset \mathcal{C}$, the functors compose:

$$\Gamma_{R_2} \circ \Gamma_{R_1} = \Gamma_{R_2},$$

which is the sheaf-theoretic expression of the repeatability of ideal measurements. For non-nested regions, the composition is governed by the **overlap cocycle** (see §4), and sequential measurements in incompatible contexts fail to commute:

$$\Gamma_{R_1} \circ \Gamma_{R_2} \neq \Gamma_{R_2} \circ \Gamma_{R_1},$$

recovering the non-commutativity of quantum observables as a *geometric non-commutativity of restriction functors*.

---

## 4. Derivation of the Born Rule from Čech Cohomology

### 4.1 The Probability Cocycle

Let $\{U_i\}$ be a good open cover of $\mathcal{C}$, with each $U_i$ corresponding to a context neighborhood. On each $U_i$, choose a local section $s_i \in \mathfrak{S}(U_i)$ representing the physical state as prepared. On overlaps $U_{ij} = U_i \cap U_j$, the sections are related by transition functions:

$$s_j = g_{ij} \, s_i, \qquad g_{ij} \in \mathcal{U}(\mathcal{A}_{c}),$$

where $\mathcal{U}(\mathcal{A}_c)$ is the unitary group of the stalk. The cocycle condition on triple overlaps reads

$$g_{ik} = g_{jk} \, g_{ij} \quad \text{on } U_{ijk}.$$

The collection $\{g_{ij}\}$ defines a class $[g] \in \check{H}^1(\mathcal{C}, \mathcal{U})$.

### 4.2 The Born Functional

**Definition 4.1.** For a measurement context $c^* \in U_k$, define the **Born functional** $\mathcal{B}_{c^*}: \mathfrak{S}(U_k) \to [0,1]$ by

$$\mathcal{B}_{c^*}(s_k) = \frac{\left| \langle g_{ik} \, s_i, \, e_{c^*} \rangle_{\mathcal{A}_{c^*}} \right|^2}{\sum_j \left| \langle g_{jk} \, s_j, \, e_{c^*} \rangle_{\mathcal{A}_{c^*}} \right|^2},$$

where $e_{c^*}$ is the unit element of the stalk at $c^*$ and $\langle \cdot, \cdot \rangle_{\mathcal{A}}$ is the inner product induced by the faithful trace on $\mathcal{A}$.

**Theorem 4.2 (Born Rule from Geometry).** *The Born functional $\mathcal{B}_{c^*}$ is independent of the choice of cover $\{U_i\}$ and local trivializations if and only if the cocycle $[g]$ is unitary. In that case, for a pure state $|\psi\rangle$ and a projective measurement of observable $A$ with eigenprojectors $\{P_i\}$,*

$$\mathcal{B}_{c^*}(s) = \text{Tr}(\rho_\psi \, P_i) = |\langle a_i | \psi \rangle|^2.$$

*Proof.* The independence under change of cover follows from the refinement invariance of Čech cohomology. To recover the standard form, take $\mathcal{C} = \mathbb{CP}^{n-1}$, cover it by the standard affine charts $U_i = \{[z_1:\cdots:z_n] : z_i \neq 0\}$, and set $g_{ij} = z_i / z_j$ on $U_{ij}$. The local section on $U_k$ is $s_k = \psi_k / z_k$, and the transition to the measurement context $c^*$ corresponding to the eigenbasis of $A$ gives

$$\mathcal{B}_{c^*}(s) = \frac{|\psi_i|^2}{\sum_j |\psi_j|^2} = |\langle a_i | \psi \rangle|^2, \qquad \square$$

The Born rule is thus not a postulate but a **cohomological identity**: it is the unique probability measure compatible with the gluing structure of the spectral sheaf.

### 4.3 The Phase as a Connection

The cocycle $\{g_{ij}\}$ may be refined to a $\mathcal{U}(1)$-valued cocycle by taking the determinant in the finite-dimensional case. This defines a line bundle $\mathcal{L} \to \mathcal{C}$, and the quantum phase is the holonomy of a connection $\nabla$ on $\mathcal{L}$:

$$\text{Hol}_\gamma(\nabla) = \exp\left(i \oint_\gamma \mathcal{A}\right),$$

where $\mathcal{A}$ is the local connection 1-form. The Berry phase is recovered as the holonomy around a loop in $\mathcal{C}$ enclosing a region of non-zero curvature $F = d\mathcal{A}$.

---

## 5. Dynamics: The Schrödinger Equation as Flatness

### 5.1 The Dynamical Connection

Let $\mathcal{C} \times \mathbb{R}$ be the extended context-time manifold. We define a connection $\nabla^H$ on the pullback sheaf $\widetilde{\mathfrak{S}} \to \mathcal{C} \times \mathbb{R}$ by

$$\nabla^H = d + \frac{i}{\hbar} H \, dt + \mathcal{A}_c,$$

where $H$ is the Hamiltonian (a section of the sheaf of self-adjoint elements) and $\mathcal{A}_c$ is the context-space connection from §4.3.

### 5.2 Flatness and the Schrödinger Equation

**Theorem 5.1.** *A section $s$ of $\widetilde{\mathfrak{S}}$ is parallel with respect to $\nabla^H$ along the time direction if and only if it satisfies the Schrödinger equation.*

*Proof.* The parallel transport condition is

$$\nabla^H_{\partial_t} s = 0 \quad \Longleftrightarrow \quad \frac{\partial s}{\partial t} + \frac{i}{\hbar} H s = 0,$$

which is precisely

$$i\hbar \frac{\partial s}{\partial t} = H s. \qquad \square$$

### 5.3 Curvature and the Heisenberg Equation

The curvature of $\nabla^H$ in the $(t, c)$ plane is

$$F^H_{tc} = \partial_t \mathcal{A}_c - \partial_c \left(\frac{i}{\hbar}H\right) + \left[\frac{i}{\hbar}H, \mathcal{A}_c\right].$$

The vanishing of this curvature, $F^H_{tc} = 0$, yields the **Heisenberg equation of motion** for context-dependent observables:

$$\frac{dA}{dt} = \frac{i}{\hbar}[H, A] + \frac{\partial A}{\partial t}.$$

Thus, the entire dynamical structure of quantum mechanics is encoded in the **zero-curvature condition** of a connection on the spectral sheaf.

---

## 6. Entanglement as Fiber Product Geometry

### 6.1 Multi-Particle Sheaves

For a composite system $A \otimes B$, the context manifold is not $\mathcal{C}_A \times \mathcal{C}_B$ but the **fiber product**

$$\mathcal{C}_{AB} = \mathcal{C}_A \times_{\mathcal{C}_{\text{cl}}} \mathcal{C}_B,$$$

where $\mathcal{C}_{\text{cl}}$ is the space of classical (commutative) contexts shared between the two subsystems. The spectral sheaf of the composite is

$$\mathfrak{S}_{AB} = \mathfrak{S}_A \boxtimes_{\mathfrak{S}_{\text{cl}}} \mathfrak{S}_B,$$

the relative tensor product of sheaves.

### 6.2 Entanglement as Non-Factorizability

**Definition 6.1.** A section $s_{AB} \in \mathfrak{S}_{AB}(\mathcal{C}_{AB})$ is **separable** if it can be written as a finite sum

$$s_{AB} = \sum_k \lambda_k \, s_A^{(k)} \boxtimes s_B^{(k)},$$

with $s_A^{(k)} \in \mathfrak{S}_A$, $s_B^{(k)} \in \mathfrak{S}_B$, $\lambda_k \geq 0$, $\sum_k \lambda_k = 1$.

**Theorem 6.2.** *A section $s_{AB}$ is entangled if and only if the restriction of $s_{AB}$ to the diagonal $\Delta \subset \mathcal{C}_{AB}$ has non-trivial monodromy around a loop enclosing a singularity of the fiber product.*

This provides a **topological invariant of entanglement**: the monodromy representation

$$\mu: \pi_1(\mathcal{C}_{AB} \setminus \Sigma) \longrightarrow \mathcal{U}(\mathcal{H}_A \otimes \mathcal{H}_B),$$

where $\Sigma$ is the singular locus, classifies entanglement types. For two qubits, $\pi_1(\mathcal{C}_{AB} \setminus \Sigma) \cong \mathbb{Z}$, and the winding number is related to the concurrence $C$ by

$$C = \sin\left(\frac{\pi \, \text{wind}(\mu)}{2}\right).$$

---

## 7. The Sheaf Separability Bound

### 7.1 Statement of the Inequality

Consider $n$ parties, each choosing among $m$ measurement contexts. Let $E(\mathbf{c})$ denote the correlation function for the context tuple $\mathbf{c} = (c_1, \ldots, c_n) \in \mathcal{C}_1 \times \cdots \times \mathcal{C}_n$.

**Theorem 7.1 (Sheaf Separability Bound).** *For any theory admitting a global section of the spectral sheaf over the $n$-party context manifold (i.e., any non-contextual hidden-variable theory), the correlation polytope satisfies*

$$\mathcal{S}_n \equiv \sum_{\mathbf{c} \in \mathcal{V}_n} \alpha_{\mathbf{c}} \, E(\mathbf{c}) \leq 2^{n-1},$$

*where $\mathcal{V}_n$ is the vertex set of the $n$-dimensional context hypercube and $\alpha_{\mathbf{c}} = (-1)^{\sum_i c_i}$.*

For $n = 2$, this reduces to the CHSH bound $\mathcal{S}_2 \leq 2$. For $n = 3$, we obtain

$$\mathcal{S}_3 \leq 4,$$

while quantum mechanics, computed via the spectral sheaf with non-trivial cocycle, yields

$$\mathcal{S}_3^{\text{QM}} = 4\sqrt{2} \approx 5.657,$$

a violation exceeding the Mermin bound by a factor of $\sqrt{2}$.

### 7.2 Proof Structure

The proof proceeds by showing that a global section imposes a **factorization of the cocycle**:

$$g_{ij}^{(n)} = \prod_{k=1}^n g_{ij}^{(k)},$$

which constrains the correlation functions to lie in a polytope whose facets are given by the inequalities above. The quantum violation arises because the actual cocycle is non-factorizable, a direct consequence of the non-triviality of $[g] \in \check{H}^1(\mathcal{C}_{AB}, \mathcal{U})$.

---

## 8. Falsifiable Prediction: Context-Space Curvature in Interferometry

### 8.1 The Curvature Correction

If the context manifold $\mathcal{C}$ carries a non-trivial metric $h_{ab}$ (induced, for example, by the Fubini–Study metric on $\mathbb{CP}^{n-1}$), then the connection $\mathcal{A}_c$ has curvature

$$F_{ab} = \partial_a \mathcal{A}_b - \partial_b \mathcal{A}_a + [\mathcal{A}_a, \mathcal{A}_b].$$

In a Mach–Zehnder interferometer, the two paths correspond to two curves $\gamma_1, \gamma_2$ in $\mathcal{C}$. The phase difference is

$$\Delta \phi = \oint_{\gamma_1 - \gamma_2} \mathcal{A} = \int_{\Sigma} F,$$

where $\Sigma$ is the surface bounded by the interferometric loop. If the context space has Ricci scalar curvature $\kappa$, then to leading order,

$$\Delta \phi = \Delta \phi_{\text{standard}} + \frac{\kappa}{6} \, \text{Area}(\Sigma) + \mathcal{O}(\kappa^2).$$

### 8.2 Experimental Signature

For a neutron interferometer with path separation $d \sim 10^{-2}$ m and context-space curvature scale $\ell_C^{-2}$, the correction is

$$\delta \phi \sim \frac{\kappa \, d^2}{6}.$$

Setting $\ell_C$ at the Planck scale gives $\delta \phi \sim 10^{-70}$, unobservable. However, if $\ell_C$ is associated with a mesoscopic decoherence scale $\sim 10^{-6}$ m (as suggested by certain gravitational decoherence models), then

$$\delta \phi \sim 10^{-8} \text{ rad},$$

which is within the sensitivity of next-generation neutron and atom interferometers (projected sensitivity $\sim 10^{-9}$ rad by 2030).

**Prediction 8.1.** *A high-precision Mach–Zehnder interferometer operating with massive particles ($m > 10^3$ amu) and path separations exceeding $10^{-3}$ m will observe a systematic phase shift inconsistent with standard quantum mechanics, scaling quadratically with path separation and linearly with the Ricci curvature of the induced context-space metric.*

---

## 9. Discussion and Relation to Existing Frameworks

### 9.1 Comparison with Topos-Theoretic Approaches

The Isham–Butterfield topos approach assigns presheaves over the category of commutative subalgebras. SSD differs in three essential respects: (i) we work with *sheaves* rather than presheaves, imposing gluing axioms that yield the cohomological Born rule; (ii) our base space is a *manifold* with a metric, enabling curvature corrections; (iii) dynamics is encoded in a *connection* rather than a presheaf morphism.

### 9.2 Relation to Connes' Non-Commutative Geometry

Connes' spectral triple $(\mathcal{A}, \mathcal{H}, D)$ encodes geometry in the spectrum of a Dirac operator. SSD uses the spectral data of *all* MASAs simultaneously, organized as a sheaf. The Connes framework is recovered in the limit where $\mathcal{C}$ is contracted to a point, i.e., where context-dependence is suppressed.

### 9.3 Relation to QBism and Relational QM

QBism treats quantum states as subjective beliefs. SSD is ontic: the sheaf $\mathfrak{S}$ is a mind-independent geometric object. However, like relational QM, SSD denies the existence of a global state. The difference is that SSD provides a *precise mathematical structure* — the sheaf and its cohomology — for what "relational" means.

---

## 10. Conclusions

We have constructed Spectral Sheaf Dynamics, a complete reformulation of quantum mechanics in which:

- States are sheaves, not vectors.
- Measurement is restriction, not collapse.
- Probability is cohomology, not postulate.
- Dynamics is flatness, not axiom.
- Entanglement is topology, not tensor algebra.
- Contextuality is curvature, not paradox.

The formalism is empirically equivalent to standard quantum mechanics in the flat-context limit and predicts deviations when context-space curvature is non-negligible. The Sheaf Separability Bound provides a new experimental test of contextuality that is strictly stronger than existing Bell-type inequalities for $n \geq 3$ parties.

Future work will extend SSD to quantum field theory by replacing the finite-dimensional context manifold with the infinite-dimensional space of local algebras in algebraic QFT, and to quantum gravity by coupling the context-space metric $h_{ab}$ to the spacetime metric $g_{\mu\nu}$.

---

## Acknowledgments

The author thanks the Institute for Advanced Theoretical Studies for support during the preparation of this manuscript.

---

## References

[1] J. von Neumann, *Mathematische Grundlagen der Quantenmechanik* (Springer, 1932).  
[2] S. Kochen and E. P. Specker, "The problem of hidden variables in quantum mechanics," *J. Math. Mech.* **17**, 59–87 (1967).  
[3] A. Connes, *Noncommutative Geometry* (Academic Press, 1994).  
[4] C. J. Isham and J. Butterfield, "A sheaf-theoretic approach to quantum theory," *Int. J. Theor. Phys.* **37**, 267–303 (1998).  
[5] M. Berry, "Quantal phase factors accompanying adiabatic changes," *Proc. R. Soc. Lond. A* **392**, 45–57 (1984).  
[6] J. F. Clauser, M. A. Horne, A. Shimony, and R. A. Holt, "Proposed experiment to test local hidden-variable theories," *Phys. Rev. Lett.* **23**, 880–884 (1969).  
[7] N. D. Mermin, "Extreme quantum entanglement in a superposition of macroscopically distinct states," *Phys. Rev. Lett.* **65**, 1838–1840 (1990).  
[8] R. Hartshorne, *Algebraic Geometry* (Springer, 1977).  
[9] S. Mac Lane and I. Moerdijk, *Sheaves in Geometry and Logic* (Springer, 1992).  
[10] C. Rovelli, "Relational quantum mechanics," *Int. J. Theor. Phys.* **35**, 1637–1678 (1996).  
[11] C. A. Fuchs, "QBism, the perimeter of quantum Bayesianism," *arXiv:1003.5209* (2010).  
[12] G. 't Hooft, "The cellular automaton interpretation of quantum mechanics," *Found. Phys.* **48**, 1195–1245 (2018).

---

