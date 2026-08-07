# Phase Field Theory: A Field-Theoretic Foundation for Phase Physics

**Marlon Hanks**
*Independent Researcher*

**January 2026**

*Subject areas:* Quantum Field Theory / Emergent Gravity / Topological Matter / Phase Foundations
*Keywords:* phase field theory, nonlinear sigma model, Sakharov induction, topological solitons, phaset excitations, combinatorial rigidity, admissible update orderings, phase relativity

**Preprint. Under review.**

---

## Abstract

Physical reality, per Phase Relativity Theory, is not any single effective description but the full phase diagram: the set of dominant saddles, their transitions, and the universal data invariant across them. Phase Physics — comprising Phase Theory, Phase Mechanics, Phase Engineering, and their deployments in the Molecular Holonomic Qubit series, Graviton Decoupled Qubits, and Phaset — occupies one such saddle: the phase in which a continuous global phase substrate $\Phi$ is the dominant effective ontology, giving rise to spacetime geometry, gauge structure, and matter as its emergent content. Phase Field Theory (PFT) formalizes this saddle as a field theory proper: an action-level, Lagrangian formulation of $\Phi$ together with its gauged nonlinear sigma model target $U(1)\times SU(2)\times SU(3)$, its induced-gravity coupling via the Sakharov mechanism, and its topological soliton sector identified with matter. Where Phase Theory establishes this saddle's axiomatic structure, culminating in Axiom 6's Combinatorial Rigidity, Phase Field Theory supplies the machinery for treating $\Phi$ dynamically within it: field quantization on the Phase Configuration Manifold, propagators and interaction vertices for phaset excitations, and a renormalization-group treatment of admissibility constraints across scales. PFT is the effective Lagrangian of the $\Phi$-phase in the sense of Phase Relativity's own formal framework — one entry, not the whole, of the invariant phase diagram — while remaining the structural center that Phase Mechanics, Phase Engineering, and their downstream deployments draw on directly. We outline the action functional and its symmetry content, the correspondence between phaset field excitations and known quasiparticle analogues (phasons, amplitudons, rotons), and identify the central open problem separating PFT from a completed quantization of its saddle: constructing a consistent path-integral measure over admissible update orderings.

---

## 1. Introduction

### 1.1 The Phase-Relativistic Context

Phase / Landscape Relativity [1] establishes the meta-principle governing all effective physical descriptions:

$$\boxed{\text{Laws are phase-relative; the invariant is the full phase diagram and its universal data.}}$$

The partition function of any underlying theory $T$ with parameter space $\mathcal{M}$ admits a saddle decomposition

$$Z[\lambda] = \sum_{s \in \text{Saddles}} e^{-I_s[\lambda]}, \qquad \lambda \in \mathcal{M}, \tag{1.1}$$

and a *phase* is a connected region $P_\alpha \subseteq \mathcal{M}$ within which a single saddle (or a degenerate family) dominates. Each phase $P_\alpha$ carries its own effective description

$$E_\alpha = \bigl(\mathcal{H}_\alpha,\;\mathcal{L}_\alpha,\;\mathcal{O}_\alpha,\;S_\alpha\bigr), \tag{1.2}$$

comprising an effective Hilbert space, Lagrangian, ontology, and symmetry structure. The invariant physical content is not $E_\alpha$ for any particular $\alpha$ but the full phase diagram

$$\mathcal{D} = \bigl(\{P_\alpha\},\;\text{transitions},\;\text{universal data}\bigr). \tag{1.3}$$

Phase Theory [2] identifies and axiomatizes one particular saddle of this diagram: the **$\Phi$-phase**, in which the dominant effective ontology is a continuous phase substrate $\Phi : \mathcal{M} \to T$ whose global organization, topology, and consistency enforcement give rise to spacetime, matter, gauge interactions, and gravity. In the $\Phi$-phase, the effective Lagrangian $\mathcal{L}_\Phi$ is not a quantum field theory on a pre-existing spacetime but a theory *from which* spacetime, fields, and particles emerge.

The present paper — **Phase Field Theory (PFT)** — is the field-theoretic formalization of this saddle. It provides the Lagrangian, the quantization procedure, the propagator structure, and the renormalization-group machinery required to treat $\Phi$ as a dynamical field within the $\Phi$-phase, while respecting the meta-principle that the $\Phi$-phase is one entry in the invariant diagram $\mathcal{D}$, not the diagram itself.

### 1.2 Scope and Relation to Phase Theory

Phase Theory [2] establishes the axiomatic foundation:

| Axiom | Content |
|---|---|
| Axiom 1 | Global Phase Consistency: $\Phi^* = \arg\min_\Phi I[\Phi]$ |
| Axiom 2 | Update Ordering: time is the partial order of a DAG |
| Axiom 3 | Topological Stability: particles are sector-stable minima |
| Axiom 4 | Coherence Limitation: $J(\Phi_A;\Phi_B) \leq C\cdot\min(|\partial A|,|\partial B|)$ |
| Axiom 5 | Metric Emergence: $g_{\mu\nu} = \alpha\langle D_\mu\Phi\cdot D_\nu\Phi\rangle_{\text{coh}}$ |
| **Axiom 6** | **Combinatorial Rigidity** (new; §9) |

Phase Theory is *axiomatic and ontological*: it states what the $\Phi$-phase is and what emerges from it. PFT is *dynamical and computational*: it supplies the action, the path integral, the Feynman rules, and the RG flow that allow one to *calculate* within the $\Phi$-phase. The relationship is analogous to that between the Wightman axioms of QFT and the Lagrangian path-integral machinery used in practice: the axioms constrain; the field theory computes.

### 1.3 Phase Mechanics, Phase Engineering, and Deployments

PFT is the theoretical core of a broader program:

- **Phase Mechanics** applies PFT's propagator and vertex structure to compute scattering amplitudes, bound-state spectra, and transition rates for phaset excitations and topological solitons.
- **Phase Engineering** exploits the controllable sectors of PFT — particularly the holonomic and topological sectors — to design devices whose operation depends on phase-substrate properties rather than on conventional electromagnetic or semiconductor physics.
- **Deployments** include the *Molecular Holonomic Qubit* series (§12.2), *Graviton Decoupled Qubits* (§12.3), and the *Phaset* architecture (§12.4), each of which draws directly on PFT's field content and symmetry structure.

### 1.4 Organization

§2 defines the Phase Configuration Manifold and the field content. §3 constructs the full PFT action. §4 analyzes the symmetry content. §5 develops the Sakharov induced-gravity sector. §6 treats topological solitons as matter. §7 performs field quantization and derives propagators. §8 identifies the phaset excitation spectrum and its quasiparticle analogues. §9 introduces Axiom 6 (Combinatorial Rigidity) and its field-theoretic consequences. §10 develops the RG treatment of admissibility. §11 addresses Phase Mechanics. §12 sketches Phase Engineering deployments. §13 states the central open problem. §14 discusses the phase-relativistic status of PFT. Appendices collect conventions, proof sketches, and the quasiparticle correspondence table.

Throughout we use natural units $\hbar = c = 1$, metric signature $(-,+,+,+)$, Greek indices $\mu,\nu,\ldots$ for emergent spacetime, Latin indices $a,b,\ldots$ for target-manifold (internal) dimensions, and capital Latin indices $A,B,\ldots$ for adjoint-representation indices.

---

## 2. The Phase Configuration Manifold

### 2.1 The Base Space and the Phase Field

The phase substrate is a continuous map

$$\Phi : \mathcal{M} \longrightarrow T, \tag{2.1}$$

where $\mathcal{M}$ is a connected topological base space (pre-geometric; no metric *a priori*) and $T$ is the target manifold. Following Phase Theory [2, Eq. (10)], we take

$$T = U(1) \times SU(2) \times SU(3). \tag{2.2}$$

The field $\Phi$ is a section of the associated bundle $E = P(\mathcal{M},T) \times_T T$ over a principal $T$-bundle $P(\mathcal{M},T) \to \mathcal{M}$. In a local trivialization, $\Phi$ is represented by a $T$-valued function $\Phi^a(x)$, $a = 1,\ldots,\dim T$, where $\dim T = 1 + 3 + 8 = 12$.

### 2.2 The Phase Configuration Manifold $\mathscr{C}$

The **Phase Configuration Manifold** is the space of all admissible phase configurations modulo gauge equivalence:

$$\mathscr{C} \;=\; \bigl\{\Phi \in \Gamma(E)\;\big|\; I[\Phi] < \infty,\;\text{Axioms 1–6 satisfied}\bigr\}\;\big/\;\mathcal{G}, \tag{2.3}$$

where $\mathcal{G} = \text{Map}(\mathcal{M},T)$ is the gauge group and $I[\Phi]$ is the phase-inconsistency functional. The quotient by $\mathcal{G}$ removes gauge redundancy; the Axiom constraints (particularly Axiom 6, §9) restrict the admissible configurations further.

$\mathscr{C}$ is not a smooth manifold in general. It decomposes into **topological sectors**

$$\mathscr{C} = \bigsqcup_{\sigma} \mathscr{C}_\sigma, \tag{2.4}$$

where $\sigma$ labels the homotopy class $[\Phi] \in [\mathcal{M},T]$. Within each sector $\mathscr{C}_\sigma$, the configurations are connected by continuous deformations; between sectors, they are not. This decomposition is the field-theoretic origin of particle identity and superselection rules.

### 2.3 Emergent Spacetime as a Coarse-Grained Limit

The emergent spacetime $(M_4, g_{\mu\nu})$ is not the domain of $\Phi$ but a *derived* structure. By Axiom 5 [2, Eq. (4)],

$$g_{\mu\nu}(x) = \alpha\,\langle D_\mu\Phi(x)\cdot D_\nu\Phi(x)\rangle_{\text{coh}}, \tag{2.5}$$

where $\langle\cdot\rangle_{\text{coh}}$ denotes averaging over the coherence domain of linear extent $\ell_{\text{coh}}$. The emergent spacetime is the effective geometry seen by excitations whose wavelengths satisfy $\lambda \gg \ell_{\text{coh}}$. Below this scale, the notion of a smooth metric breaks down and the full phase-topological description on $\mathscr{C}$ must be used.

We denote the emergent spacetime coordinates by $x^\mu$ and the pre-geometric base-space labels by $\mathbf{p} \in \mathcal{M}$. The map $\mathbf{p} \mapsto x^\mu(\mathbf{p})$ is itself emergent and defined only in the coherent regime.

---

## 3. The PFT Action Functional

### 3.1 Structure

The full PFT action is

$$S_{\text{PFT}}[\Phi, A, g] = S_{\text{NLSM}} + S_{\text{topo}} + S_{\text{Sakharov}} + S_{\text{coh}}, \tag{3.1}$$

comprising four sectors:

1. **$S_{\text{NLSM}}$**: the gauged nonlinear sigma model on $T$;
2. **$S_{\text{topo}}$**: topological (Wess–Zumino, $\theta$-term) contributions;
3. **$S_{\text{Sakharov}}$**: the induced-gravity sector;
4. **$S_{\text{coh}}$**: the coherence-limitation and admissibility sector.

### 3.2 The Gauged Nonlinear Sigma Model

The kinetic and gauge-coupling terms are

$$S_{\text{NLSM}} = -\frac{1}{2}\int_{M_4} d^4x\,\sqrt{-g}\;\Bigl[K_{ab}(\Phi)\,D_\mu\Phi^a\,D^\mu\Phi^b + 2\,V(\Phi)\Bigr], \tag{3.2}$$

where:

- $K_{ab}(\Phi)$ is the target-space metric (phase-stiffness tensor) on $T$. For the product group $T = U(1)\times SU(2)\times SU(3)$, it decomposes as

$$K_{ab} = K^{(1)} \oplus K^{(2)} \oplus K^{(3)}, \tag{3.3}$$

with $K^{(1)} = R_1^2$ (a single radius for the $U(1)$ factor), $K^{(2)}_{ij} = R_2^2\,\delta_{ij}$ (bi-invariant metric on $SU(2)$), and $K^{(3)}_{AB} = R_3^2\,\delta_{AB}$ (Killing metric on $SU(3)$). The radii $R_1, R_2, R_3$ set the phase stiffnesses of the three sectors and are related to the gauge couplings by $g_i^{-2} \propto R_i^2$.

- $D_\mu\Phi^a = \partial_\mu\Phi^a + A_\mu^A\,(T_A)^a{}_b\,\Phi^b$ is the gauge-covariant derivative, with $A_\mu = A_\mu^A T_A$ the connection on $P(\mathcal{M},T)$ and $T_A$ the generators of $\mathfrak{t} = \mathfrak{u}(1)\oplus\mathfrak{su}(2)\oplus\mathfrak{su}(3)$.

- $V(\Phi) \geq 0$ is the phase potential, vanishing on the vacuum manifold $\mathcal{V}_0 = \{\Phi : V(\Phi)=0\}$ and positive elsewhere. The vacuum manifold's topology determines the pattern of spontaneous symmetry breaking and the resulting Goldstone/Higgs spectrum.

The gauge-field kinetic term is included as

$$S_{\text{gauge}} = -\frac{1}{4}\int_{M_4} d^4x\,\sqrt{-g}\;\text{Tr}\bigl(F_{\mu\nu}F^{\mu\nu}\bigr), \tag{3.4}$$

with $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu + [A_\mu,A_\nu]$ the curvature of the connection. In components,

$$F^A_{\mu\nu} = \partial_\mu A^A_\nu - \partial_\nu A^A_\mu + f^A{}_{BC}\,A^B_\mu\,A^C_\nu, \tag{3.5}$$

where $f^A{}_{BC}$ are the structure constants of $\mathfrak{t}$.

### 3.3 Topological Terms

The topological sector includes:

**(i) Wess–Zumino–Witten term.** For the $SU(2)$ factor, the WZW term at level $k_{\text{WZ}}$ is

$$S_{\text{WZW}} = \frac{k_{\text{WZ}}}{24\pi^2}\int_{B_5} \text{Tr}\bigl(\Phi^{-1}d\Phi\bigr)^5, \tag{3.6}$$

where $B_5$ is a five-dimensional manifold with $\partial B_5 = M_4$. This term is non-trivial when $\pi_5(SU(2)) \neq 0$ (in fact $\pi_5(SU(2)) = \mathbb{Z}_2$; for $SU(3)$, $\pi_5(SU(3)) = \mathbb{Z}$, giving a genuine WZW term).

**(ii) $\theta$-terms.** For each simple factor,

$$S_\theta = \sum_{i=2,3} \frac{\theta_i}{32\pi^2}\int_{M_4} \text{Tr}\bigl(F^{(i)}_{\mu\nu}\,\widetilde{F}^{(i)\mu\nu}\bigr)\,d^4x, \tag{3.7}$$

where $\widetilde{F}^{\mu\nu} = \frac{1}{2}\epsilon^{\mu\nu\rho\sigma}F_{\rho\sigma}$. The $\theta$-angles are parameters of the phase diagram $\mathcal{D}$ and label distinct vacua within the $\Phi$-phase.

**(iii) Skyrmion current coupling.** The baryon current, identified with the topological current of the $SU(2)$ sector,

$$B^\mu = \frac{1}{24\pi^2}\,\epsilon^{\mu\nu\rho\sigma}\,\text{Tr}\bigl(\Phi^{-1}\partial_\nu\Phi\;\Phi^{-1}\partial_\rho\Phi\;\Phi^{-1}\partial_\sigma\Phi\bigr), \tag{3.8}$$

couples to the $\omega$-meson analog in the vector-meson sector. In PFT, this current is the Noether current associated with the topological stability of the $\pi_3(SU(2)) = \mathbb{Z}$ sector.

### 3.4 The Sakharov Induced-Gravity Sector

Gravity in PFT is not fundamental. It is induced by quantum fluctuations of the phase field $\Phi$ and the gauge fields $A_\mu$ on the emergent geometry, following the Sakharov mechanism [3]. The induced gravitational action is

$$S_{\text{Sakharov}} = \int_{M_4} d^4x\,\sqrt{-g}\;\Bigl[-\Lambda_{\text{ind}} + \frac{1}{16\pi G_{\text{ind}}}\,R + a_1\,R^2 + a_2\,R_{\mu\nu}R^{\mu\nu} + a_3\,R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma}\Bigr], \tag{3.9}$$

where the induced Newton's constant and cosmological constant are determined by the one-loop effective action of the $\Phi$ and $A_\mu$ fields:

$$\frac{1}{G_{\text{ind}}} = \frac{1}{12\pi}\sum_s (-1)^{F_s}\,N_s\,m_s^2\,\ln\frac{\Lambda_{\text{UV}}^2}{m_s^2}, \tag{3.10}$$

$$\Lambda_{\text{ind}} = \frac{1}{64\pi^2}\sum_s (-1)^{F_s}\,N_s\,m_s^4\,\ln\frac{\Lambda_{\text{UV}}^2}{m_s^2}. \tag{3.11}$$

Here the sum runs over all species $s$ of phase-field excitations (phasons, amplitudons, gauge modes, solitons), $F_s$ is the fermion number, $N_s$ the multiplicity, $m_s$ the mass, and $\Lambda_{\text{UV}} \sim 1/\ell_{\text{coh}}$ is the ultraviolet cutoff set by the coherence scale.

The key structural point is that **the graviton is not a fundamental field in PFT**. The metric $g_{\mu\nu}$ is a composite operator (Eq. (2.5)), and the Einstein–Hilbert term in Eq. (3.9) is generated radiatively. At energies below $\Lambda_{\text{UV}}$, the induced-gravity description is valid; above it, the full phase-topological dynamics on $\mathscr{C}$ must be used.

The higher-curvature terms ($R^2$, $R_{\mu\nu}R^{\mu\nu}$, etc.) encode the leading corrections to Einstein gravity and are suppressed by powers of $\Lambda_{\text{UV}}^{-2}$. Their coefficients $a_i$ are calculable from the heat-kernel expansion of the $\Phi$-field operator.

### 3.5 The Coherence and Admissibility Sector

The coherence limitation (Axiom 4) and the combinatorial rigidity (Axiom 6, §9) impose non-local constraints on admissible configurations. At the action level, these are encoded by a constraint functional

$$S_{\text{coh}} = \int_{M_4} d^4x\,\sqrt{-g}\;\lambda(x)\,\Bigl[J\bigl(\Phi_A;\Phi_B\bigr) - C\cdot\min(|\partial A|,|\partial B|)\Bigr]_+, \tag{3.12}$$

where $[\cdot]_+ = \max(\cdot,0)$ enforces the bound, $\lambda(x)$ is a Lagrange-multiplier field, and the mutual information $J$ is computed from the two-point correlator of $\Phi$. This term is non-polynomial in $\Phi$ and is the source of significant technical difficulty in the quantization program (§13).

### 3.6 The Complete Action

Collecting all terms, the PFT action is

$$\boxed{S_{\text{PFT}} = S_{\text{NLSM}}[\Phi,A] + S_{\text{gauge}}[A] + S_{\text{topo}}[\Phi,A] + S_{\text{Sakharov}}[g] + S_{\text{coh}}[\Phi].} \tag{3.13}$$

This action is a functional on $\mathscr{C}$ (Eq. (2.3)), not on a fixed spacetime. The metric $g_{\mu\nu}$ is itself a composite of $\Phi$ (Eq. (2.5)), and the integral measure $d^4x\,\sqrt{-g}$ is defined only in the emergent coherent regime.

---

## 4. Symmetry Content

### 4.1 Gauge Symmetry

The local gauge symmetry is

$$\Phi(x) \to g(x)\cdot\Phi(x), \qquad A_\mu(x) \to g(x)A_\mu(x)g^{-1}(x) + g(x)\partial_\mu g^{-1}(x), \tag{4.1}$$

for $g(x) \in T$. The full gauge group is $\mathcal{G} = \text{Map}(\mathcal{M}, T)$. All terms in $S_{\text{PFT}}$ are gauge-invariant by construction.

### 4.2 Global Symmetries and Their Phase-Relative Realization

The global symmetry structure is phase-relative in the sense of Phase / Landscape Relativity [1, §9]. In the $\Phi$-phase:

- The *center symmetry* $\mathbb{Z}_3 \subset SU(3)$ is unbroken in the confined sector and spontaneously broken in the deconfined sector. The Polyakov loop $\langle L\rangle$ serves as the order parameter.
- The *chiral symmetry* $SU(N_f)_L \times SU(N_f)_R$ is spontaneously broken to $SU(N_f)_V$ by the phase condensate $\langle\bar{\psi}\psi\rangle \neq 0$ in the low-energy sector.
- The *topological symmetry* associated with the conservation of the Skyrmion current $B^\mu$ (Eq. (3.8)) is exact and non-perturbative.

### 4.3 Shift Symmetry and the Phason

In the $U(1)$ sector, the phase field $\theta(x)$ (the coordinate on $U(1) \cong S^1$) enjoys an approximate shift symmetry

$$\theta(x) \to \theta(x) + \text{const}, \tag{4.2}$$

which is exact in the absence of the potential $V(\Phi)$ and broken to a discrete subgroup by topological effects (instantons, vortices). The Goldstone mode of this broken shift symmetry is the **phason** (§8.1).

### 4.4 Diffeomorphism Invariance (Emergent)

Diffeomorphism invariance is not a fundamental symmetry of PFT. It is an *emergent* symmetry valid in the coherent, weak-strain regime where the metric $g_{\mu\nu}$ is well-defined. Under a diffeomorphism $x^\mu \to x'^\mu(x)$, the composite metric transforms as a tensor and the Sakharov action (3.9) is invariant. Below the coherence scale, diffeomorphism invariance breaks down, and the fundamental symmetry is the gauge group $\mathcal{G}$ acting on $\mathscr{C}$.

### 4.5 Anomaly Structure

The gauge and gravitational anomalies of the $\Phi$-phase must cancel for consistency. The anomaly polynomial for the fermionic sector (arising from the topological soliton spectrum, §6) is

$$\mathcal{I}_6 = \text{tr}\,F^3 - \frac{1}{8}\text{tr}\,F\,\text{tr}\,R^2, \tag{4.3}$$

evaluated in the appropriate representation. The condition $\mathcal{I}_6 = 0$ constrains the allowed topological sectors and is a **phase-diagram invariant** in the sense of Phase Relativity: it must hold in any phase connected to the $\Phi$-phase by a continuous transition.

---

## 5. Sakharov Induction in Detail

### 5.1 The One-Loop Effective Action

The Sakharov mechanism operates as follows. Consider the Euclidean partition function of the phase field $\Phi$ and gauge field $A_\mu$ on a curved background $g_{\mu\nu}$:

$$Z[g] = \int \mathcal{D}\Phi\,\mathcal{D}A\;e^{-S_{\text{NLSM}}[\Phi,A,g] - S_{\text{gauge}}[A,g]}. \tag{5.1}$$

Integrating out the $\Phi$ and $A$ fluctuations generates the one-loop effective action for $g_{\mu\nu}$:

$$\Gamma_{\text{1-loop}}[g] = -\ln Z[g] = \int d^4x\sqrt{g}\;\Bigl[\Lambda_{\text{ind}} - \frac{R}{16\pi G_{\text{ind}}} + \cdots\Bigr]. \tag{5.2}$$

The coefficients are computed via the heat-kernel expansion. For a scalar operator $\Delta = -\nabla^2 + X$ acting on the phase field, the heat-kernel coefficients are

$$\text{Tr}\,e^{-t\Delta} = \frac{1}{(4\pi t)^2}\int d^4x\sqrt{g}\;\sum_{n=0}^{\infty} t^n\,a_n(x), \tag{5.3}$$

with

$$a_0 = 1, \qquad a_1 = \frac{R}{6} - X, \qquad a_2 = \frac{1}{180}\bigl(R_{\mu\nu\rho\sigma}R^{\mu\nu\rho\sigma} - R_{\mu\nu}R^{\mu\nu}\bigr) + \frac{1}{72}R^2 + \cdots \tag{5.4}$$

The $a_1$ coefficient generates the Einstein–Hilbert term; $a_2$ generates the higher-curvature corrections.

### 5.2 Induced Newton's Constant

For the phase field $\Phi$ with $\dim T = 12$ real components and the gauge fields $A_\mu$ with $\dim\mathfrak{t} = 12$ generators, the induced Newton's constant is

$$\frac{1}{G_{\text{ind}}} = \frac{N_\Phi}{12\pi}\,\Lambda_{\text{UV}}^2 + \frac{N_A}{20\pi}\,\Lambda_{\text{UV}}^2 + \text{(massive species corrections)}, \tag{5.5}$$

where $N_\Phi = \dim T = 12$ and $N_A = \dim\mathfrak{t} = 12$. The ultraviolet cutoff is $\Lambda_{\text{UV}} = 1/\ell_{\text{coh}}$, the inverse coherence length. Setting $G_{\text{ind}} = G_N$ (the observed Newton's constant) fixes

$$\ell_{\text{coh}} \sim \sqrt{\frac{N_\Phi + N_A}{12\pi\,G_N^{-1}}} \sim \ell_P, \tag{5.6}$$

where $\ell_P$ is the Planck length. The coherence scale and the Planck scale coincide, consistent with Phase Theory's identification of the coherence limit with the ultraviolet cutoff of quantum gravity.

### 5.3 Graviton as a Composite Bound State

In PFT, the graviton $h_{\mu\nu}$ (the quantum of the metric perturbation $g_{\mu\nu} = \eta_{\mu\nu} + h_{\mu\nu}$) is a **composite bound state** of phase-field excitations. It is not an elementary field in the action (3.13). Its propagator is generated by the resummation of $\Phi$-loop bubbles:

$$\langle h_{\mu\nu}(p)\,h_{\rho\sigma}(-p)\rangle = \frac{P_{\mu\nu\rho\sigma}}{p^2\bigl[1 + \Pi(p^2)\bigr]}, \tag{5.7}$$

where $P_{\mu\nu\rho\sigma}$ is the spin-2 projector and $\Pi(p^2)$ is the vacuum polarization from $\Phi$ loops. At $p^2 \ll \Lambda_{\text{UV}}^2$, $\Pi(p^2) \approx (16\pi G_{\text{ind}})^{-1}$, recovering the standard graviton propagator. At $p^2 \sim \Lambda_{\text{UV}}^2$, the composite structure becomes visible and the propagator deviates from the Einstein form.

---

## 6. Topological Soliton Sector and Matter

### 6.1 Solitons as Particles

In PFT, matter is identified with the topological soliton sector of the nonlinear sigma model. The relevant homotopy groups of $T = U(1)\times SU(2)\times SU(3)$ are:

| Homotopy | Value | Defect | Physical Identification |
|---|---|---|---|
| $\pi_1(U(1))$ | $\mathbb{Z}$ | Vortex lines | Electrically charged leptons |
| $\pi_2(T)$ | $0$ | — | No stable monopoles |
| $\pi_3(SU(2))$ | $\mathbb{Z}$ | Skyrmions | Baryons |
| $\pi_3(SU(3))$ | $\mathbb{Z}$ | $SU(3)$ Skyrmions | Exotic baryonic states |

A soliton in topological sector $\sigma$ is a field configuration $\Phi_\sigma$ that minimizes $I[\Phi]$ within $\sigma$ (Axiom 3). Its mass is

$$m_\sigma = \min_{\Phi\in\mathscr{C}_\sigma} I[\Phi]. \tag{6.1}$$

### 6.2 The Skyrme Term and Soliton Stabilization

To stabilize solitons against collapse (Derrick's theorem), the action must include a four-derivative Skyrme term:

$$S_{\text{Skyrme}} = \frac{1}{32e^2}\int d^4x\,\sqrt{-g}\;\text{Tr}\bigl[\Phi^{-1}\partial_\mu\Phi,\;\Phi^{-1}\partial_\nu\Phi\bigr]^2, \tag{6.2}$$

where $e$ is the Skyrme coupling. In PFT, this term arises naturally from the next-to-leading-order expansion of the phase-stiffness tensor $K_{ab}(\Phi)$ and from integrating out the massive amplitudon modes (§8.2).

### 6.3 The Particle Quintuple

Each soliton species is labeled by the invariant quintuple [2, Eq. (17)]

$$\Xi = (k,\;Q_H,\;t,\;\chi,\;R), \tag{6.3}$$

where $k \in \pi_1(U(1)) = \mathbb{Z}$ is the winding number (electric charge), $Q_H$ is the knot charge (baryon/lepton number), $t$ is the radial excitation level (generation), $\chi$ is the framing/chirality (spin), and $R$ is the holonomy class (gauge representation). The mass spectrum $m(\Xi)$ is determined by Eq. (6.1) and the specific form of $K_{ab}$ and $V(\Phi)$.

### 6.4 Confinement from Holonomy

Confinement of the $SU(3)$ sector is enforced by global phase consistency (Axiom 1). An isolated quark corresponds to a phase configuration with non-trivial $SU(3)$ holonomy around a large loop:

$$\text{Hol}(A,\gamma) = \mathcal{P}\exp\bigl(\oint_\gamma A\bigr) \neq \mathbf{1}_{SU(3)}. \tag{6.4}$$

This violates global phase consistency on any contractible loop. Quarks must combine into color-singlet configurations (baryons, mesons) for which the total holonomy is trivial. The confining potential is

$$V(r) = \sigma_{\text{string}}\,r + \text{const}, \qquad \sigma_{\text{string}} \propto R_3^2\,K^{(3)}, \tag{6.5}$$

where $\sigma_{\text{string}}$ is the string tension determined by the $SU(3)$ phase stiffness.

---

## 7. Field Quantization on $\mathscr{C}$

### 7.1 The Path Integral

The quantum theory is defined by the path integral over the Phase Configuration Manifold:

$$Z_{\text{PFT}}[J] = \int_{\mathscr{C}} \mathcal{D}\Phi\,\mathcal{D}A\;\exp\bigl(iS_{\text{PFT}}[\Phi,A] + i\int J\cdot\Phi\bigr). \tag{7.1}$$

Several features distinguish this from an ordinary QFT path integral:

**(i) The domain is $\mathscr{C}$, not a linear space.** The integral is over maps $\Phi:\mathcal{M}\to T$ modulo gauge, with the target $T$ a compact nonlinear manifold. The measure $\mathcal{D}\Phi$ is the Liouville measure on the space of maps, weighted by the target-space metric $K_{ab}$:

$$\mathcal{D}\Phi = \prod_x \sqrt{\det K_{ab}(\Phi(x))}\;\prod_a d\Phi^a(x). \tag{7.2}$$

**(ii) Topological sector decomposition.** The integral decomposes as

$$Z_{\text{PFT}} = \sum_\sigma \int_{\mathscr{C}_\sigma}\mathcal{D}\Phi\,\mathcal{D}A\;e^{iS_{\text{PFT}}} = \sum_\sigma Z_\sigma. \tag{7.3}$$

Each sector $Z_\sigma$ is a saddle in the Phase Relativity sense (Eq. (1.1)). The dominant sector at a given energy scale determines the effective particle content.

**(iii) The admissibility constraint.** The coherence and rigidity constraints (Axioms 4, 6) restrict the domain of integration. Formally,

$$\mathcal{D}\Phi\big|_{\text{admissible}} = \mathcal{D}\Phi\;\cdot\;\Theta\bigl[\text{Axioms 4,6}\bigr], \tag{7.4}$$

where $\Theta$ is a functional step-function enforcing the constraints. The construction of this constrained measure is the central open problem (§13).

### 7.2 Gauge Fixing and Ghosts

Gauge fixing proceeds via the Faddeev–Popov procedure. In the background-field gauge,

$$\mathcal{L}_{\text{GF}} = -\frac{1}{2\xi}\bigl(D_\mu^{\text{bg}}\,a^\mu\bigr)^2, \qquad \mathcal{L}_{\text{ghost}} = \bar{c}\,D_\mu^{\text{bg}}\,D^\mu c, \tag{7.5}$$

where $a_\mu$ is the quantum fluctuation of $A_\mu$ around a background $A_\mu^{\text{bg}}$, and $c,\bar{c}$ are the ghost fields. For the product group $T$, the ghosts decompose into $U(1)$, $SU(2)$, and $SU(3)$ sectors.

### 7.3 The Phaset Propagator

Expanding $\Phi$ around a classical background $\Phi_0$ (a vacuum or soliton configuration),

$$\Phi(x) = \Phi_0(x)\,\exp\bigl(i\pi^a(x)\,T_a\bigr), \tag{7.6}$$

the fluctuation fields $\pi^a(x)$ are the **phaset fields**. The quadratic action for $\pi^a$ in a flat emergent background is

$$S^{(2)}_{\text{phaset}} = \frac{1}{2}\int d^4x\;\Bigl[K_{ab}\,\partial_\mu\pi^a\,\partial^\mu\pi^b - M^2_{ab}\,\pi^a\pi^b\Bigr], \tag{7.7}$$

where $M^2_{ab} = \partial^2 V/\partial\Phi^a\partial\Phi^b\big|_{\Phi_0}$ is the mass matrix. The Feynman propagator is

$$\Delta^{ab}_F(p) = \frac{i\,(K^{-1})^{ab}}{p^2 - M^2 + i\epsilon}. \tag{7.8}$$

For massless phasons ($M^2 = 0$ in the $U(1)$ Goldstone sector), this reduces to

$$\Delta_F(p) = \frac{i}{p^2 + i\epsilon}. \tag{7.9}$$

### 7.4 Interaction Vertices

The interaction vertices are read off from the nonlinear sigma model expansion. The three-phaset vertex is

$$V^{abc}_{(3)}(p_1,p_2,p_3) = -i\,f^{abc}\,K_{ad}\,(p_1 - p_2)^d, \tag{7.10}$$

where $f^{abc}$ are the structure constants of $\mathfrak{t}$, and the four-phaset vertex is

$$V^{abcd}_{(4)} = -i\Bigl[f^{abe}f^{cde}(K_{\mu\nu}^{(1)} - K_{\mu\nu}^{(2)}) + f^{ace}f^{bde}(K_{\mu\nu}^{(2)} - K_{\mu\nu}^{(3)}) + \cdots\Bigr], \tag{7.11}$$

with the full expression determined by the target-space curvature $R_{abcd}$ of $K_{ab}$. The vertices are organized by the number of derivatives (momentum factors) and are non-renormalizable in the power-counting sense, as expected for a nonlinear sigma model in $d=4$.

### 7.5 The Gauge-Field Propagator

The gauge-field propagator in the Feynman gauge ($\xi = 1$) is

$$D^{AB}_{\mu\nu}(p) = \frac{-i\,\delta^{AB}\,\eta_{\mu\nu}}{p^2 + i\epsilon}. \tag{7.12}$$

In the confined $SU(3)$ sector, this propagator is modified non-perturbatively: the gluon acquires a dynamical mass $m_g \sim \sigma_{\text{string}}^{1/2}$ via the Gribov mechanism, and the propagator takes the Gribov form

$$D^{AB}_{\mu\nu}(p) = \frac{-i\,\delta^{AB}}{p^2 + \gamma_G^4/p^2}\Bigl(\eta_{\mu\nu} - \frac{p_\mu p_\nu}{p^2}\Bigr), \tag{7.13}$$

where $\gamma_G$ is the Gribov parameter. This modification is a direct consequence of the holonomy constraint (6.4) and is calculable within PFT.

---

## 8. The Phaset Excitation Spectrum

### 8.1 Phasons

**Phasons** are the Goldstone modes of the spontaneously broken shift symmetry (4.2) in the $U(1)$ sector. They are massless, gapless excitations of the phase field $\theta(x)$:

$$\mathcal{L}_{\text{phason}} = \frac{R_1^2}{2}\,\partial_\mu\theta\,\partial^\mu\theta. \tag{8.1}$$

Phasons are the PFT analog of:
- **Phonons** in a crystal (longitudinal phase oscillations of the lattice order parameter);
- **Phase phonons** in incommensurate charge-density waves;
- The **axion** in Peccei–Quinn symmetry breaking (if $\theta$ is promoted to a pseudoscalar).

In the $\Phi$-phase, the photon is identified with the coherent propagating mode of the $U(1)$ phason sector [2, §XIV]. The phason's linear dispersion $\omega = v_\theta\,|\mathbf{k}|$ (with $v_\theta = c$ in the emergent spacetime) is the origin of the speed of light.

### 8.2 Amplitudons

**Amplitudons** are the massive radial excitations of the phase field, corresponding to oscillations in the $|\Phi|$ direction (transverse to the vacuum manifold $\mathcal{V}_0$). Their Lagrangian is

$$\mathcal{L}_{\text{amplitudon}} = \frac{1}{2}\,\partial_\mu\varphi\,\partial^\mu\varphi - \frac{1}{2}\,m_\varphi^2\,\varphi^2 + \mathcal{O}(\varphi^3), \tag{8.2}$$

with $m_\varphi^2 = \partial^2 V/\partial|\Phi|^2\big|_{\mathcal{V}_0}$.

Amplitudons are the PFT analog of:
- **Amplitudons** in incommensurate charge-density waves (oscillations of the order-parameter amplitude);
- The **Higgs boson** in the electroweak theory (radial excitation of the Higgs condensate);
- **Massive amplitude modes** in antiferromagnets.

In PFT, the Higgs boson is identified with the lowest amplitudon of the $SU(2)$ sector. Its mass $m_H = 125\;\text{GeV}$ fixes the curvature of $V(\Phi)$ at the $SU(2)$ vacuum.

### 8.3 Rotons

**Rotons** are gapped excitations with a non-monotonic dispersion relation $\omega(k)$ possessing a local minimum at finite momentum $k = k_0$:

$$\omega(k) = \Delta_R + \frac{(k-k_0)^2}{2\mu_R} + \cdots, \tag{8.3}$$

where $\Delta_R$ is the roton gap and $\mu_R$ the effective roton mass.

In PFT, rotons arise from the nonlinear self-interaction of phasons in the $SU(2)$ and $SU(3)$ sectors. They are the PFT analog of:
- **Rotons** in superfluid $^4$He (Feynman's roton);
- **Magnons** in frustrated magnets with non-monotonic spin-wave spectra.

Rotons in the $SU(3)$ sector are intimately connected to confinement: the roton gap $\Delta_R$ is related to the string tension by $\Delta_R \sim \sqrt{\sigma_{\text{string}}}$. The roton minimum reflects the energetic preference for flux-tube formation at intermediate distances.

### 8.4 Summary: Quasiparticle Correspondence

| PFT Excitation | Sector | Mass | Quasiparticle Analog | Physical Identification |
|---|---|---|---|---|
| Phason | $U(1)$ | $0$ | Phonon / phase phonon | Photon (coherent mode) |
| Amplitudon | $SU(2)$ | $m_\varphi$ | Amplitudon / Higgs | Higgs boson |
| Amplitudon | $SU(3)$ | $m_\varphi^{(3)}$ | Amplitude mode | Scalar glueball analog |
| Roton | $SU(2), SU(3)$ | $\Delta_R$ | Roton / magnon | Confined-sector excitation |
| Gauge mode | $SU(2)$ | $m_W, m_Z$ | Plasmon | $W^\pm, Z$ bosons |
| Gauge mode | $SU(3)$ | $0$ (confined) | Gluon | Gluon (confined) |
| Soliton | $\pi_3(SU(2))$ | $m_\sigma$ | Skyrmion | Baryons (proton, neutron) |
| Vortex | $\pi_1(U(1))$ | $m_\ell$ | Abrikosov vortex | Charged leptons |

### 8.5 Spectral Function and the Phaset

The full spectral function of the phase field,

$$\rho(\omega,\mathbf{k}) = -\frac{1}{\pi}\text{Im}\;\Delta_F(\omega,\mathbf{k}), \tag{8.4}$$

contains contributions from all excitation types. The **phaset** is the collective term for any quantum of phase-field excitation: phasons, amplitudons, rotons, and gauge modes are all phaset species. In the Phase Engineering context (§12), the phaset is the operational unit — the excitation that is created, manipulated, and detected by phase-engineering devices.

---

## 9. Axiom 6: Combinatorial Rigidity

### 9.1 Statement

Phase Theory's original five axioms [2] govern the phase substrate's consistency, temporal ordering, topological stability, coherence, and metric emergence. However, they do not fully constrain the *combinatorial structure* of the update ordering (Axiom 2's DAG). Axiom 6 closes this gap.

> **Axiom 6 (Combinatorial Rigidity).** The directed acyclic graph of updates $\mathcal{G}_u = (V_u, E_u)$ is combinatorially rigid: its edge set $E_u$ is determined, up to isomorphism, by the topological sector $\sigma$ and the boundary data $\partial\Phi|_{\partial\mathcal{M}}$. No continuous deformation of $\Phi$ within $\mathscr{C}_\sigma$ may alter the combinatorial type of $\mathcal{G}_u$. Equivalently, the automorphism group $\text{Aut}(\mathcal{G}_u)$ is discrete, and the moduli space of admissible DAG structures within a fixed topological sector is zero-dimensional.

### 9.2 Motivation

Without Axiom 6, the update ordering could be continuously deformed within a topological sector, generating a continuum of inequivalent causal structures. This would violate the emergent Lorentz invariance (which requires a unique light-cone structure up to conformal rescaling) and would render the path integral (7.1) ill-defined, as the integration domain would include a continuous family of causal structures.

Combinatorial rigidity ensures that the causal structure is **locked** to the topological sector: changing the causal structure requires changing the topological sector, which is a discrete, non-perturbative event (a phase transition in the Phase Relativity sense).

### 9.3 Field-Theoretic Implementation

At the level of the PFT action, Axiom 6 is implemented by a rigidity constraint on the update-ordering field. Let $\mathcal{O}(x,y) \in \{0,1\}$ be the ordering function, with $\mathcal{O}(x,y) = 1$ if update $x$ precedes update $y$ in the DAG. The rigidity condition is

$$\frac{\delta \mathcal{O}}{\delta \Phi^a(x)} = 0 \quad \text{for all continuous deformations within } \mathscr{C}_\sigma. \tag{9.1}$$

This is a non-local, non-polynomial constraint. In the continuum limit, it becomes a constraint on the causal Green's function $G_C(x,y)$:

$$\delta_\Phi\,G_C(x,y) = 0 \quad \text{within a fixed sector}. \tag{9.2}$$

The Lagrange multiplier enforcing this constraint contributes to $S_{\text{coh}}$ (Eq. (3.12)) and is the source of the measure problem (§13).

### 9.4 Consequences

**(i) Discrete causal phase transitions.** Changes in the DAG structure are quantized. They correspond to topological phase transitions in the phase diagram $\mathcal{D}$, not to continuous deformations. This is the field-theoretic expression of Phase Relativity's principle that phase transitions are boundaries between effective worlds [1, §4].

**(ii) Absence of causal fluctuations.** In the $\Phi$-phase, the causal structure does not fluctuate quantum-mechanically. This distinguishes PFT from causal-set approaches [4], where the causal order is a dynamical quantum variable. In PFT, the causal order is rigid within a sector; quantum fluctuations occur *on* the fixed causal background, not *of* it.

**(iii) Superselection of causal sectors.** Different DAG structures belong to different superselection sectors. No local operator can connect them. This is the field-theoretic origin of the No-Closed-Phase-Loop Theorem [2, Theorem 20.1]: the DAG's acyclicity is not merely a constraint but a topological invariant of the causal sector.

### 9.5 Relation to the Phase Diagram

In the Phase Relativity framework, Axiom 6 implies that the $\Phi$-phase's saddle structure includes a **discrete label** for the causal sector:

$$Z_{\Phi\text{-phase}} = \sum_{\text{causal sectors } \gamma}\;\sum_{\sigma}\;Z_{\sigma,\gamma}. \tag{9.3}$$

The sum over $\gamma$ is a sum over combinatorially distinct DAG structures. Each $(\sigma,\gamma)$ pair is a sub-saddle. The full $\Phi$-phase saddle is the sum over all of them. This structure mirrors the saddle-sum (1.1) of Phase Relativity: the $\Phi$-phase itself has an internal saddle decomposition.

---

## 10. Renormalization Group and Admissibility

### 10.1 The Nonlinear Sigma Model $\beta$-Function

The gauged NLSM on $T$ is perturbatively non-renormalizable in $d = 4$. The target-space metric $K_{ab}$ runs under the RG:

$$\mu\frac{dK_{ab}}{d\mu} = -\frac{1}{2\pi}\,R_{ab}[K] + \mathcal{O}(K^{-1}), \tag{10.1}$$

where $R_{ab}[K]$ is the Ricci tensor of the target-space metric. For $T = U(1)\times SU(2)\times SU(3)$:

- The $U(1)$ factor has $R_{ab} = 0$: the phason coupling does not run (at one loop).
- The $SU(2)$ factor has $R_{ab} \propto \delta_{ab}$: the coupling runs as in a standard $SU(2)$ gauge theory.
- The $SU(3)$ factor has $R_{ab} \propto \delta_{ab}$: the coupling runs as in QCD, exhibiting asymptotic freedom.

### 10.2 Admissibility Constraints Across Scales

The coherence limitation (Axiom 4) and combinatorial rigidity (Axiom 6) are not fixed constraints but **scale-dependent admissibility conditions**. Under RG flow from the ultraviolet ($\mu \sim \Lambda_{\text{UV}} = 1/\ell_{\text{coh}}$) to the infrared ($\mu \ll \Lambda_{\text{UV}}$):

- At the UV scale, the coherence domain is a single point: $\ell_{\text{coh}}(\Lambda_{\text{UV}}) \sim 0$, and the admissibility constraint is maximally restrictive. Only configurations satisfying exact global phase consistency are admissible.
- At intermediate scales, the coherence domain grows: $\ell_{\text{coh}}(\mu) \sim 1/\mu$, and the admissibility constraint relaxes. Configurations that are locally but not globally consistent become admissible.
- At the IR scale, the coherence domain is macroscopic, and the admissibility constraint reduces to the standard gauge-invariance and causality conditions of effective QFT.

The RG flow of the admissibility constraint is encoded in the running of the Lagrange multiplier $\lambda(x)$ in $S_{\text{coh}}$:

$$\mu\frac{d\lambda}{d\mu} = \beta_\lambda(\lambda, K_{ab}, g_i), \tag{10.2}$$

where $g_i$ are the gauge couplings. The fixed points of this flow correspond to phase transitions in the Phase Relativity sense: at a fixed point, the admissibility constraint is scale-invariant, and the system exhibits conformal symmetry.

### 10.3 The Admissibility Anomaly

A subtle issue arises: the admissibility constraint, being non-local and non-polynomial, may not be preserved by renormalization. If the renormalized constraint differs from the bare constraint, the theory suffers from an **admissibility anomaly**:

$$\mathcal{A}_{\text{adm}} = \mu\frac{d}{d\mu}\bigl[\text{Axioms 4,6}\bigr]_{\text{ren}} \neq 0. \tag{10.3}$$

The cancellation of $\mathcal{A}_{\text{adm}}$ is a consistency condition on the $\Phi$-phase. We conjecture (without proof) that $\mathcal{A}_{\text{adm}} = 0$ if and only if the topological sector $\sigma$ supports a consistent emergent metric (i.e., the Sakharov mechanism produces a non-degenerate $g_{\mu\nu}$). This conjecture, if true, would link the consistency of the admissibility constraint to the existence of gravity in the $\Phi$-phase.

---

## 11. Phase Mechanics

### 11.1 Definition

**Phase Mechanics** is the computational discipline that applies PFT's propagator and vertex structure to compute physical observables: scattering amplitudes, bound-state spectra, transition rates, and correlation functions for phaset excitations and topological solitons.

### 11.2 Scattering Amplitudes

The $S$-matrix for phaset scattering is computed from the LSZ reduction formula applied to the correlation functions of $\pi^a(x)$:

$$\langle p_1',\ldots,p_n'|\,S\,|p_1,\ldots,p_m\rangle = \prod_i \lim_{p_i^2\to m_i^2}(p_i^2 - m_i^2)\;\widetilde{G}^{(n+m)}(p_1,\ldots,p_m,p_1',\ldots,p_n'), \tag{11.1}$$

where $\widetilde{G}^{(n+m)}$ is the Fourier transform of the $(n+m)$-point Green's function computed from the path integral (7.1).

At tree level, the amplitudes are determined by the vertices (7.10), (7.11). At one loop, the NLSM's non-renormalizability requires the introduction of counterterms at $\mathcal{O}(p^4)$, parameterized by the low-energy constants of the chiral Lagrangian.

### 11.3 Soliton Scattering

Soliton–soliton scattering (e.g., baryon–baryon scattering) is computed using the collective-coordinate method. The soliton is parameterized by its position $\mathbf{X}(t)$, orientation $R(t) \in SU(2)$, and internal shape modes. The effective Lagrangian for the collective coordinates is

$$L_{\text{coll}} = \frac{1}{2}M_\sigma\,\dot{\mathbf{X}}^2 + \frac{1}{2}\mathcal{I}\,\text{Tr}(\dot{R}\dot{R}^{-1}) + V_{\text{int}}(\mathbf{X}_1 - \mathbf{X}_2, R_1, R_2), \tag{11.2}$$

where $M_\sigma$ is the soliton mass, $\mathcal{I}$ the moment of inertia, and $V_{\text{int}}$ the interaction potential. The quantization of $L_{\text{coll}}$ yields the baryon spectrum and scattering phase shifts.

### 11.4 Phaset Transport Coefficients

In the hydrodynamic regime ($\omega\tau \ll 1$, where $\tau$ is the phaset relaxation time), the phase substrate supports collective modes described by effective transport coefficients:

- **Phase viscosity** $\eta_\Phi$: the resistance of the phase substrate to shear deformation. Related to the imaginary part of the retarded phaset correlator.
- **Phase conductivity** $\sigma_\Phi$: the response of the phase substrate to an external gauge field. In the $U(1)$ sector, $\sigma_\Phi$ is related to the electrical conductivity.
- **Phase diffusion constant** $D_\Phi$: the rate at which phase inhomogeneities relax. Related to the phason propagator at small $k$.

These transport coefficients are computable from PFT using the Kubo formulae applied to the phaset Green's functions.

---

## 12. Phase Engineering and Deployments

### 12.1 Phase Engineering: Principles

**Phase Engineering** is the discipline of designing and fabricating devices whose operation depends on the controlled manipulation of phase-substrate properties — specifically, the creation, transport, interference, and detection of phaset excitations in specified topological sectors.

Phase Engineering draws on PFT for:
- The phaset propagator (7.8) and vertex structure (7.10, 7.11), which determine the allowed interactions;
- The topological sector decomposition (7.3), which identifies the protected degrees of freedom;
- The coherence limitation (Axiom 4), which bounds the information capacity of any phase-engineering device;
- The Sakharov mechanism (§5), which determines the gravitational background in which the device operates.

### 12.2 Molecular Holonomic Qubit Series

The **Molecular Holonomic Qubit** (MHQ) series exploits the holonomic (geometric-phase) structure of the $U(1)\times SU(2)$ sector to implement quantum gates.

A molecule with $n$ degenerate electronic states defines an $n$-dimensional Hilbert space. Adiabatic transport of the molecular configuration around a closed loop $\gamma$ in parameter space induces a unitary holonomy

$$U(\gamma) = \mathcal{P}\exp\bigl(-\oint_\gamma A_i\,dR^i\bigr) \in U(n), \tag{12.1}$$

where $A_i$ is the Berry connection and $R^i$ are the nuclear coordinates. In PFT, this holonomy is identified with the holonomy of the phase-substrate connection $A$ (Eq. (6.4)) restricted to the $U(1)\times SU(2)$ sector.

The MHQ series comprises:
- **MHQ-1**: single-qubit gates via $U(1)$ holonomy (Abelian geometric phase);
- **MHQ-2**: two-qubit gates via $SU(2)$ holonomy (non-Abelian geometric phase);
- **MHQ-3**: error-protected qubits via topological sectors with $\pi_1(U(1)) = \mathbb{Z}$ winding protection.

The key advantage is **topological protection**: the holonomy $U(\gamma)$ depends only on the topology of $\gamma$ (its homotopy class), not on the details of the path. Small perturbations of the path do not change the gate, providing intrinsic error protection. PFT provides the quantitative framework for computing the holonomy, the coherence time, and the gate fidelity.

### 12.3 Graviton Decoupled Qubits

In PFT, gravity is a composite phenomenon (§5.3): the graviton is a bound state of phaset excitations, and its coupling to matter is mediated by the Sakharov mechanism. The coupling strength is

$$g_{\text{grav}} \sim \frac{E}{M_{\text{Pl}}}, \tag{12.2}$$

where $E$ is the energy of the system. For qubit-scale systems ($E \sim$ meV–eV), this coupling is extraordinarily small.

**Graviton Decoupled Qubits** (GDQs) exploit this by encoding quantum information in topological sectors that are *exactly* decoupled from the gravitational sector. Specifically, a qubit encoded in a topological sector $\sigma$ with zero phase-inconsistency-energy variation under metric perturbations,

$$\frac{\delta m_\sigma}{\delta g_{\mu\nu}} = 0, \tag{12.3}$$

is immune to gravitational decoherence. PFT identifies such sectors: they are the sectors in which the soliton's mass $m_\sigma$ is determined entirely by topological invariants (winding number, knot charge) and not by the metric.

GDQs are relevant for quantum computing in gravitational environments (satellite-based quantum communication, quantum sensors in varying gravitational potentials) where gravitational decoherence is a limiting factor.

### 12.4 Phaset Architecture

The **Phaset** is a device architecture that uses coherent phaset excitations as the operational medium for information processing. In contrast to conventional semiconductor or superconducting qubits, the Phaset operates in the phase substrate directly:

- **Information encoding**: in the topological quantum numbers $\Xi = (k,Q_H,t,\chi,R)$ of a localized phaset excitation;
- **Gate operations**: by controlled braiding of phaset excitations (exploiting the braid-group statistics of the topological sector);
- **Readout**: by measuring the holonomy of the phase-substrate connection around the phaset.

The Phaset's coherence time is bounded by Axiom 4:

$$\tau_{\text{coh}} \leq \frac{C\cdot|\partial A|}{J_{\text{noise}}}, \tag{12.4}$$

where $|\partial A|$ is the boundary area of the Phaset's coherence domain and $J_{\text{noise}}$ is the environmental noise power. PFT provides the tools to compute $J_{\text{noise}}$ from the phaset propagator and the environmental spectral density.

The Phaset architecture is the primary deployment target of Phase Engineering and the subject of ongoing experimental development.

---

## 13. The Central Open Problem: The Measure over Admissible Update Orderings

### 13.1 Statement of the Problem

The path integral (7.1) requires a measure $\mathcal{D}\Phi$ on the Phase Configuration Manifold $\mathscr{C}$. For the nonlinear sigma model sector, this measure is known (Eq. (7.2)). However, the admissibility constraints — Axiom 4 (coherence limitation) and Axiom 6 (combinatorial rigidity) — restrict the domain of integration to a subset of $\mathscr{C}$ that is not a smooth submanifold.

Specifically, the combinatorial rigidity of Axiom 6 requires that the update-ordering DAG $\mathcal{G}_u$ is fixed within each topological sector. The space of admissible DAGs is a discrete set (zero-dimensional moduli space), not a continuum. The path integral must therefore include a **sum over admissible DAG structures**:

$$Z_{\text{PFT}} = \sum_{\gamma \in \text{Adm}(\sigma)} \int_{\mathscr{C}_{\sigma,\gamma}} \mathcal{D}\Phi\,\mathcal{D}A\;e^{iS_{\text{PFT}}}, \tag{13.1}$$

where $\text{Adm}(\sigma)$ is the (discrete) set of admissible DAG structures compatible with the topological sector $\sigma$.

The problem is: **no consistent, diffeomorphism-invariant measure is known for the sum over $\gamma$.** The space of DAGs is a combinatorial object, not a smooth manifold, and the standard tools of functional integration do not apply.

### 13.2 Why This Is Hard

**(i) Non-locality.** The admissibility constraint is non-local: it involves the global structure of the DAG, not just local field values. The functional $\Theta[\text{Axioms 4,6}]$ in Eq. (7.4) cannot be written as a local Lagrangian density.

**(ii) Combinatorial vs. continuum tension.** The DAG is a discrete combinatorial object; the phase field $\Phi$ is a continuous field. The measure must integrate over the continuous field while summing over the discrete DAG. These are fundamentally different types of integration.

**(iii) Background independence.** The emergent spacetime $(M_4,g_{\mu\nu})$ is itself a composite of $\Phi$. The measure cannot be defined with respect to a fixed background metric. A background-independent measure on $\mathscr{C}$ is required, but no such measure is known for nonlinear sigma models with topological constraints.

**(iv) Anomaly cancellation.** As noted in §10.3, the admissibility constraint may suffer from an anomaly under renormalization. The measure must be defined so as to cancel $\mathcal{A}_{\text{adm}}$, but the mechanism for this cancellation is unknown.

### 13.3 Partial Results and Approaches

Several approaches are under investigation:

**(a) Lattice regularization.** Discretize $\mathcal{M}$ on a lattice and define the DAG structure on the lattice. The sum over admissible DAGs becomes a finite (but exponentially large) combinatorial sum. The continuum limit $\text{lattice} \to 0$ must be taken carefully to recover Axiom 6's rigidity.

**(b) Causal-set methods.** Borrow techniques from causal-set theory [4] to define a measure on the space of DAGs. The Benincasa–Dowker action [5] provides a discrete analog of the Einstein–Hilbert action on a causal set; a similar construction may provide a discrete analog of $S_{\text{PFT}}$ on the admissible DAG.

**(c) Tensor-network representation.** Represent the path integral as a tensor network, with the DAG structure encoded in the network's connectivity. The admissibility constraint becomes a constraint on the allowed tensor-network topologies. This approach connects to the amplituhedron program [6] and to holographic error-correcting codes [7].

**(d) Homotopy-theoretic methods.** Use the theory of $\infty$-categories and homotopy type theory to define a measure on the space of admissible configurations. The Phase Configuration Manifold $\mathscr{C}$ is replaced by an $\infty$-groupoid, and the path integral becomes a homotopy-theoretic trace.

None of these approaches is complete. The construction of the admissible measure remains the central open problem of PFT.

### 13.4 Significance

Resolving this problem would amount to a complete quantization of the $\Phi$-phase: a well-defined, background-independent path integral over all admissible phase configurations, incorporating the full topological, causal, and coherence structure of Phase Theory's axioms. It would provide the non-perturbative definition of PFT that is currently lacking and would enable the computation of observables (soliton masses, scattering amplitudes, phase-transition rates) from first principles.

In the Phase Relativity framework, resolving this problem would complete the specification of one saddle of the invariant phase diagram $\mathcal{D}$ — the $\Phi$-phase — to the point where its universal data (critical exponents, anomaly coefficients, topological entanglement entropy) could be computed exactly. The $\Phi$-phase would then be a fully characterized entry in $\mathcal{D}$, on equal footing with any other phase.

---

## 14. The Phase-Relativistic Status of PFT

### 14.1 PFT as One Saddle

Phase / Landscape Relativity demands reflexivity [1, Axiom 12]: the phase-relativistic analysis must apply to our own phase. PFT is the effective Lagrangian of the $\Phi$-phase. It is not the final theory. It is one effective description, valid in the saddle where the phase substrate $\Phi$ is the dominant ontology.

In another saddle — a nongeometric phase, a stringy phase, a topological phase with no continuous $\Phi$ — PFT would not apply. The entities it describes (phasons, amplitudons, solitons, the emergent metric) would not exist. The laws it encodes would be replaced by other effective laws.

### 14.2 The Invariant Is the Diagram

The invariant physical content is not PFT but the full phase diagram $\mathcal{D}$ (Eq. (1.3)), of which PFT is one entry. The universal data of the $\Phi$-phase — its critical exponents, anomaly coefficients, topological entanglement entropy, and saddle structure — are phase-diagram invariants. They survive dualities and phase transitions. They are the physical content that PFT contributes to $\mathcal{D}$.

### 14.3 Falsifiability Within the Phase

Within the $\Phi$-phase, PFT makes specific, falsifiable predictions:

1. **Finite new-particle spectrum**: $\sim 25 \pm 10$ new species below 100 TeV [2, §XXV.1];
2. **Topology-dependent annihilation channels**: branching ratios differing from standard QFT [2, §XXV.2];
3. **Refractive gravity deviations**: corrections $H_{\mu\nu}$ to Einstein's equations in the strong-field regime [2, §XXV.3];
4. **Non-EFT dark-sector recoil**: momentum-transfer distributions not capturable by contact operators [2, §XXV.4];
5. **No antigravity**: $g_{\bar{H}} = g_H$ for antihydrogen [2, §XXV.5];
6. **No causal loops**: structural exclusion of closed timelike curves [2, §XXV.6];
7. **Hawking spectrum deviations**: non-thermal corrections near coherence saturation [2, §XXV.7];
8. **CMB topological signatures**: non-Gaussian B-mode polarization patterns [2, §XXV.8].

Each prediction is a test of the $\Phi$-phase's validity. Falsification of any prediction would indicate that the $\Phi$-phase is not the correct saddle at the relevant energy scale — not that the phase diagram $\mathcal{D}$ is wrong, but that our phase location within it has been misidentified.

### 14.4 Relation to Other Saddles

PFT's relationship to other approaches is mediated by the phase diagram:

- **String theory** may describe a different saddle of $\mathcal{D}$, in which the dominant ontology is not a phase substrate but a collection of extended objects. The two saddles may be connected by a duality (phase duality, [1, §24]) if they share the same universal data.
- **Loop quantum gravity** may describe a nongeometric phase in which the emergent metric of PFT has dissolved into spin-network structure.
- **Causal-set theory** captures the DAG structure of Axiom 2 but not the continuous phase field of Axiom 1. It may describe a partial or limiting aspect of the $\Phi$-phase.

The phase diagram $\mathcal{D}$ accommodates all of these as distinct entries. PFT's claim is not to be the unique description but to be the correct description *of the $\Phi$-phase*.

---

## 15. Conclusion

Phase Field Theory provides the field-theoretic machinery for the $\Phi$-phase: the saddle of the invariant phase diagram in which a continuous phase substrate $\Phi : \mathcal{M} \to U(1)\times SU(2)\times SU(3)$ is the dominant effective ontology. The PFT action (3.13) comprises a gauged nonlinear sigma model, topological terms, a Sakharov induced-gravity sector, and a coherence/admissibility sector. The field content includes phasons, amplitudons, rotons, gauge modes, and topological solitons, organized by the topological sector decomposition of the Phase Configuration Manifold $\mathscr{C}$.

The symmetry content — local $U(1)\times SU(2)\times SU(3)$ gauge invariance, approximate shift symmetry, emergent diffeomorphism invariance, and topological symmetry — determines the allowed interactions and the structure of the Feynman rules. The Sakharov mechanism generates gravity as a composite, induced phenomenon; the graviton is a bound state of phaset excitations, not a fundamental field.

Axiom 6 (Combinatorial Rigidity) constrains the causal structure to be locked to the topological sector, preventing continuous deformation of the update-ordering DAG and ensuring the stability of the emergent Lorentzian geometry. The renormalization-group treatment of admissibility constraints reveals a scale-dependent relaxation of the coherence and rigidity conditions, with fixed points corresponding to phase transitions.

The downstream program — Phase Mechanics, Phase Engineering, and the Molecular Holonomic Qubit, Graviton Decoupled Qubit, and Phaset deployments — draws directly on PFT's propagator structure, topological sector decomposition, and coherence bounds.

The central open problem is the construction of a consistent path-integral measure over admissible update orderings: a background-independent, combinatorially rigid, anomaly-free integration measure on the full Phase Configuration Manifold. Resolving this problem would complete the non-perturbative quantization of the $\Phi$-phase and fully characterize its contribution to the invariant phase diagram.

PFT is one entry in the phase diagram $\mathcal{D}$ — the entry we inhabit. The invariant is $\mathcal{D}$ itself.

---

## Appendix A: Conventions and Notation

| Symbol | Meaning |
|---|---|
| $\Phi$ | Phase substrate field, $\Phi:\mathcal{M}\to T$ |
| $\mathcal{M}$ | Pre-geometric base space |
| $T = U(1)\times SU(2)\times SU(3)$ | Target manifold |
| $K_{ab}(\Phi)$ | Phase-stiffness tensor (target-space metric) |
| $V(\Phi)$ | Phase potential |
| $A_\mu$ | Gauge connection on $P(\mathcal{M},T)$ |
| $F_{\mu\nu}$ | Gauge curvature |
| $D_\mu$ | Gauge-covariant derivative |
| $I[\Phi]$ | Phase-inconsistency functional |
| $\mathscr{C}$ | Phase Configuration Manifold |
| $\mathscr{C}_\sigma$ | Topological sector $\sigma$ of $\mathscr{C}$ |
| $g_{\mu\nu}$ | Emergent metric tensor |
| $\ell_{\text{coh}}$ | Coherence length |
| $\Lambda_{\text{UV}} = 1/\ell_{\text{coh}}$ | Ultraviolet cutoff |
| $G_{\text{ind}}$ | Induced Newton's constant |
| $\pi^a(x)$ | Phaset fluctuation field |
| $\Delta_F^{ab}(p)$ | Phaset Feynman propagator |
| $\Xi = (k,Q_H,t,\chi,R)$ | Particle invariant quintuple |
| $\mathcal{G}_u$ | Update-ordering DAG |
| $\text{Adm}(\sigma)$ | Set of admissible DAG structures in sector $\sigma$ |
| $\rho(\omega,\mathbf{k})$ | Phaset spectral function |
| $\sigma_{\text{string}}$ | Confining string tension |
| $\gamma_G$ | Gribov parameter |
| $R_i$ | Phase-stiffness radius of the $i$-th factor |
| $e$ | Skyrme coupling |
| $k_{\text{WZ}}$ | Wess–Zumino level |
| $\theta_i$ | $\theta$-angle of the $i$-th simple factor |

Metric signature: $(-,+,+,+)$. Natural units: $\hbar = c = 1$. Greek indices: emergent spacetime. Latin indices: target manifold. Capital Latin: adjoint representation.

---

## Appendix B: Proof Sketches

### B.1 Metric Emergence from the Sakharov Mechanism

**Claim.** The Einstein equations emerge from the one-loop effective action of the phase field.

**Sketch.** Following Jacobson [8], consider a local Rindler horizon in the emergent spacetime. The coherence limitation (Axiom 4) gives the horizon entropy $S = A/(4\ell_{\text{coh}}^2)$. The Clausius relation $\delta Q = T\,\delta S$, with $T = \hbar/(2\pi\ell_{\text{coh}})$ the Unruh temperature and $\delta Q = T_{\mu\nu}\,\xi^\mu\,d\Sigma^\nu$ the heat flux, yields

$$R_{\mu\nu} - \tfrac{1}{2}g_{\mu\nu}R + \Lambda g_{\mu\nu} = 8\pi G_{\text{ind}}\,T_{\mu\nu}, \tag{B.1}$$

with $G_{\text{ind}}$ given by Eq. (3.10). The argument holds at every point of the emergent spacetime. $\blacksquare$

### B.2 Finiteness of the Topological Sector Sum

**Claim.** For any energy cutoff $E$, the number of topological sectors $\sigma$ with $m_\sigma < E$ is finite.

**Sketch.** The mass $m_\sigma$ grows at least as $|k|^2$ with winding number $k$ (from the gradient energy) and at least linearly with knot complexity. The number of winding classes with $|k| < \sqrt{E}$ is finite ($\mathbb{Z}$ is discrete). The number of knot types with crossing number below $E$ is finite [9]. Therefore the number of sectors with $m_\sigma < E$ is finite. $\blacksquare$

### B.3 Combinatorial Rigidity Implies Discrete Causal Sectors

**Claim.** Axiom 6 implies that the space of causal structures within a fixed topological sector is discrete.

**Sketch.** Axiom 6 states that the DAG $\mathcal{G}_u$ is determined, up to isomorphism, by $(\sigma, \partial\Phi|_{\partial\mathcal{M}})$. The moduli space of admissible DAGs is therefore $\text{Aut}(\mathcal{G}_u)\backslash\{\text{DAGs compatible with }\sigma\}$, which is zero-dimensional by the rigidity assumption. Hence the causal structure is a discrete label, not a continuous modulus. $\blacksquare$

---

## Appendix C: Quasiparticle Correspondence Table

| PFT excitation | Dispersion | Condensed-matter analog | QFT analog | Status |
|---|---|---|---|---|
| $U(1)$ phason | $\omega = c\|k\|$ | Phonon (longitudinal) | Photon | Identified |
| $SU(2)$ phason | $\omega = c\|k\|$ (broken) | Magnon (Goldstone) | Pion | Identified |
| Amplitudon ($SU(2)$) | $\omega = \sqrt{m_\varphi^2 + c^2k^2}$ | Amplitudon (CDW) | Higgs boson | Identified |
| Amplitudon ($SU(3)$) | $\omega = \sqrt{(m_\varphi^{(3)})^2 + c^2k^2}$ | Amplitude mode | Scalar glueball | Predicted |
| Roton ($SU(2)$) | $\omega = \Delta_R + (k-k_0)^2/(2\mu_R)$ | Roton ($^4$He) | — | Predicted |
| Roton ($SU(3)$) | $\omega = \Delta_R + (k-k_0)^2/(2\mu_R)$ | Roton (frustrated magnet) | Confined-sector mode | Predicted |
| $W^\pm, Z$ gauge mode | $\omega = \sqrt{m_W^2 + c^2k^2}$ | Plasmon | $W^\pm, Z$ | Identified |
| Gluon (confined) | Gribov-modified | — | Gluon | Identified (confined) |
| Skyrmion | Massive, non-relativistic | Magnetic skyrmion | Baryon | Identified |
| $U(1)$ vortex | Massive, string-like | Abrikosov vortex | Charged lepton | Identified |

---

## References

[1] Phase / Landscape Relativity: Phase-Relative Laws, Ontologies, and the Invariance of the Phase Diagram. *Relativity 47.0 White Paper* (2026).

[2] M. Hanks, "Phase Theory: A Unified Theory of Matter, Light, and Geometry," preprint (January 2026).

[3] A. D. Sakharov, "Vacuum quantum fluctuations in curved space and the theory of gravitation," *Dokl. Akad. Nauk SSSR* **177**, 70 (1967); English transl.: *Sov. Phys. Dokl.* **12**, 1040 (1968).

[4] R. D. Sorkin, "Causal sets: discrete gravity," in *Lectures on Quantum Gravity*, ed. A. Gomberoff and D. Marolf (Springer, 2005), pp. 305–327.

[5] D. M. T. Benincasa and F. Dowker, "The scalar curvature of a causal set," *Phys. Rev. Lett.* **104**, 181301 (2010).

[6] N. Arkani-Hamed and J. Trnka, "The amplituhedron," *JHEP* **1410**, 030 (2014).

[7] A. Almheiri, X. Dong, and D. Harlow, "Bulk locality and quantum error correction in AdS/CFT," *JHEP* **1504**, 163 (2015).

[8] T. Jacobson, "Thermodynamics of spacetime: the Einstein equation of state," *Phys. Rev. Lett.* **75**, 1260 (1995).

[9] C. Ernst and D. W. Sumners, "The growth of the number of prime knots," *Math. Proc. Cambridge Philos. Soc.* **102**, 303 (1987).

[10] L. D. Landau and E. M. Lifshitz, *Statistical Physics* (Pergamon, 1969).

[11] S. Weinberg, *The Quantum Theory of Fields*, Vols. 1–3 (Cambridge University Press, 1995–2000).

[12] E. Witten, "Anti-de Sitter space, thermal phase transition, and confinement in gauge theories," *Adv. Theor. Math. Phys.* **2**, 505 (1998).

[13] S. R. Coleman, "The fate of the false vacuum. 1. Semiclassical theory," *Phys. Rev. D* **15**, 2929 (1977).

[14] X.-G. Wen, *Quantum Field Theory of Many-Body Systems* (Oxford University Press, 2004).

[15] P. M. Chaikin and T. C. Lubensky, *Principles of Condensed Matter Physics* (Cambridge University Press, 1995).

[16] N. Goldenfeld, *Lectures on Phase Transitions and the Renormalization Group* (Addison-Wesley, 1992).

[17] K. G. Wilson and J. Kogut, "The renormalization group and the $\epsilon$ expansion," *Phys. Rep.* **12**, 75 (1974).

[18] J. M. Maldacena, "The large-$N$ limit of superconformal field theories and supergravity," *Adv. Theor. Math. Phys.* **2**, 231 (1998).

[19] S. W. Hawking and D. N. Page, "Thermodynamics of black holes in anti-de Sitter space," *Commun. Math. Phys.* **87**, 577 (1983).

[20] A. Zee, *Quantum Field Theory in a Nutshell* (Princeton University Press, 2010).

[21] M. E. Peskin and D. V. Schroeder, *An Introduction to Quantum Field Theory* (Addison-Wesley, 1995).

[22] P. W. Anderson, "More is different," *Science* **177**, 393 (1972).

[23] A. Kitaev, "Fault-tolerant quantum computation by anyons," *Ann. Phys.* **303**, 2 (2003).

[24] R. B. Laughlin, "Anomalous quantum Hall effect," *Phys. Rev. Lett.* **50**, 1395 (1983).

[25] L. Susskind, "The world as a hologram," *J. Math. Phys.* **36**, 6377 (1995).

[26] G. 't Hooft, "Dimensional reduction in quantum gravity," in *Salamfestschrift*, ed. A. Ali et al. (World Scientific, 1994).

[27] J. D. Bekenstein, "Black holes and entropy," *Phys. Rev. D* **7**, 2333 (1973).

[28] S. Sachdev, *Quantum Phase Transitions* (Cambridge University Press, 2011).

[29] E. Fradkin, *Field Theories of Condensed Matter Physics* (Cambridge University Press, 2013).

[30] M. R. Douglas, "The statistics of string/M theory vacua," *JHEP* **0305**, 046 (2003).

---

*Phase Field Theory — Hanks (2026). Preprint. Under review.*
