# The Distributed Spin-Qubit Magnetometer Network: A Multi-Node Framet and the Network-Level Invariant Sector

**Preprint — August 2, 2026**
**M. Brownlee — Dust LLC**

**Keywords:** framet, distributed sensor network, NV-center magnetometry, baseline correlation, admissibility group, network invariant subspace, entanglement-enhanced sensing, timing synchronization

---

## Abstract

Candidates #1 through #6 established the admissibility-group and invariant-subspace formalism of *Frame Theory* §7–8 on progressively larger and more structured single platforms, culminating in candidate #6's spatially extended optical-lattice framet with a measurable synthetic connection between neighboring sites. This paper develops a structurally distinct extension: a **distributed network** of independent, widely separated spin-qubit magnetometer nodes (built from NV centers, as in candidate #1, or other addressable spin platforms), in which each node carries its own local frame and admissibility-invariant subspace, but the physically interesting quantity is not any single node's invariant state — it is the network-level correlation structure that survives independent, uncoordinated local reorientation of each node's own frame. We formalize this as an extension of §8.4's invariant-subspace construction to a *tensor-product, multi-frame* setting, distinguish it carefully from candidate #6's single-lattice synthetic-connection picture (the nodes here are not connected by any physical or synthetic gauge field; they are correlated only through shared preparation, entanglement, or common external signals), and propose a concrete network architecture and protocol for identifying which measured correlations are admissibility-invariant in this multi-frame sense and which are frame-relative artifacts of a particular node's local orientation choice. As with every candidate in this tier, no coupling to the gravitational tetrad or spin connection is present or claimed.

---

## 1. Introduction

### 1.1 A different kind of "multi-point" system

Candidate #6 closed the gap of a spatially extended *connected* frame bundle — many local frames related by a measurable, engineered connection. This paper addresses a different structural question, raised implicitly by candidate #1's original framing (multiple physically separated defects, flagged there as candidate #7 in the broader survey) but not developed there: what happens when the local frames at different points are **not** connected by any physical or synthetic gauge field at all, and are instead independent, potentially uncorrelated, potentially very far apart (meters to kilometers, in realistic distributed-sensing deployments), with the only relationship between them being whatever is imposed at preparation time or inferred after the fact from correlated measurement statistics?

This is the operational situation for essentially all real distributed quantum-sensor networks — arrays of magnetometers, clocks, or gravimeters deployed for geodesy, magnetic anomaly detection, or fundamental-physics searches (e.g., dark-matter transient-signal networks) — and it is a genuinely distinct structural case from candidate #6's lattice, worth treating on its own terms within this survey.

### 1.2 Scope statement

As with candidates #1–6, this paper treats the distributed network strictly as a representation-theoretic and correlation-structure demonstration. No claim of gravitational coupling, torsion sensitivity, or physical frame-transport measurement is made for any individual node or for the network's inter-node correlations. Full discussion in Section 7.

---

## 2. Physical System

### 2.1 Node architecture

Each network node is, in the baseline design, a single NV-center magnetometer of the type developed in candidate #1: a confocal-addressed defect with independent ODMR readout, independent microwave control, and — critically for this paper — an independently orientable local frame, since each node's diamond sample is mounted, and potentially crystallographically oriented, independently of every other node. Nodes are assumed to be separated by distances ranging from centimeters (a benchtop multi-node testbed) to kilometers (a realistic field-deployed network), connected only by classical communication links (for timestamp and control-parameter exchange) and, in the entangled variant of Section 4, by a shared photonic entanglement-distribution channel.

### 2.2 Independent local frames

Unlike candidate #6's lattice, where neighboring sites are connected by a physical tunneling process and a genuine (if synthetic) gauge connection, the nodes here have **no direct physical connection** between their local frames at all. Node \(k\)'s admissibility group is

\[
G_k = \mathrm{Stab}(\hat n_k) \simeq U(1)_{\hat n_k}\subset SU(2),
\]

exactly as in candidate #1, but with \(\hat n_k\) chosen entirely independently for each \(k\), by whatever mounting or crystal-growth process produced that particular node's sample. There is, in general, no known relationship between \(\hat n_1,\hat n_2,\ldots,\hat n_N\) unless one is deliberately engineered (Section 4.3).

### 2.3 Shared external signals

The physically interesting use case for such a network — magnetic anomaly detection, geomagnetic mapping, or a coordinated search for a transient exotic-physics signal — depends on each node's *invariant*, frame-independent observable (typically the local magnetic field magnitude, extracted from the zero-field-split ODMR spectrum in a manner insensitive to \(\hat n_k\)'s particular orientation) responding to a common external stimulus, allowing baseline correlation or triangulation across nodes despite each node's local frame being unrelated to any other's.

---

## 3. Correspondence to the Framet Formalism

### 3.1 Tensor-product state space

Following §7.4's definition of \(G\)-admissibility for a single system, the natural extension to \(N\) independent nodes is a tensor-product state space

\[
\mathcal S_{\mathrm{net}} = \mathcal S_1\otimes\mathcal S_2\otimes\cdots\otimes\mathcal S_N,
\]

with each factor carrying its own independent admissibility group \(G_k\). The network-level admissibility group relevant to *uncoordinated* local reorientation is the direct product

\[
G_{\mathrm{net}} = G_1\times G_2\times\cdots\times G_N,
\]

acting factor-wise, \(U(g_1,\ldots,g_N) = U_1(g_1)\otimes\cdots\otimes U_N(g_N)\), in contrast to the *collective, correlated* action \(U(g)\otimes U(g)\otimes\cdots\) used for the multi-particle singlet states of candidates #3–5, where the same group element acted identically on every factor. This distinction — independent per-node group action versus collective identical action — is the paper's central formal point, and is the reason network-level invariance is a strictly different (and generically much more restrictive) condition than the single-collective-rotation invariance already demonstrated for entangled pairs in candidates #3–5.

### 3.2 The network-level invariant subspace

The network-level invariant subspace,

\[
\mathcal I_{G_{\mathrm{net}}} = \left\{\Phi\in\mathcal S_{\mathrm{net}}\;\middle|\;U(g_1,\ldots,g_N)\Phi=\Phi,\ \forall (g_1,\ldots,g_N)\in G_{\mathrm{net}}\right\},
\]

is invariant under *independent* rotation of every node's own axial subgroup, simultaneously and arbitrarily. This is a much stronger condition than any single-node invariant subspace: a product state of independent per-node invariant states, \(|\Psi\rangle=\bigotimes_k|m_s=0\rangle_k\), trivially satisfies it, but any state carrying non-classical correlations between nodes' *frame-relative* degrees of freedom (the \(m_s=\pm1\) sublevels) generically does not, because there is no mechanism to correlate a phase or population change at node \(k\) under \(\hat n_k\)-rotation with a compensating change at node \(j\neq k\) when the two rotations are chosen completely independently.

### 3.3 What survives: the invariant observable, not the invariant state

The more physically relevant construction for this platform, and the one actually used in real distributed magnetometry, is not the full state-level invariant subspace of Section 3.2 but the invariant *observable* condition of §7.4,

\[
U(g_1,\ldots,g_N)\,A\,U(g_1,\ldots,g_N)^{-1} = A,\qquad\forall(g_1,\ldots,g_N)\in G_{\mathrm{net}}.
\]

The zero-field-split transition frequency at each node individually satisfies this (it is invariant under that node's own axial rotation, as established in candidate #1, Table 1), and therefore any classical function of the *set* of per-node zero-field-split frequencies — in particular, any baseline correlation, triangulated field gradient, or common-mode transient signature extracted from the network — is automatically network-admissible in this sense, without requiring any entanglement or coordination between nodes at all. This is the paper's key structural clarification: **useful distributed-sensing correlations do not require the strong state-level invariance of Section 3.2; they require only that each node's own contributed observable be independently admissible**, a much weaker and more easily satisfied condition that already holds for ordinary, unentangled NV magnetometer networks as currently deployed.

### 3.4 Explicit dictionary

| Frame Theory (§7–8) | Distributed network realization |
|---|---|
| Single admissibility group \(G\) | Per-node group \(G_k=U(1)_{\hat n_k}\) |
| Network admissibility group (uncoordinated case) | Direct product \(G_{\mathrm{net}}=\prod_k G_k\) |
| Network admissibility group (collective/entangled case) | Diagonal subgroup, \(g_1=g_2=\cdots=g_N\) (as in candidates #3–5's collective rotation) |
| State-level invariant subspace \(\mathcal I_{G_{\mathrm{net}}}\) | Product of per-node invariant states, or genuinely correlated multi-node invariant states (Section 4) |
| Invariant observable | Per-node zero-field-split frequency; any classical function of the set of such frequencies |
| Frame-relative quantity | Any inter-node phase or coherence referenced across independently-oriented axes without a shared reference |

---

## 4. Entanglement-Enhanced Network Variant

### 4.1 Motivation

Section 3.3 established that ordinary (unentangled) network correlations are already admissibility-invariant in the weak, observable-level sense. A stronger question, of independent interest in the quantum-sensing literature, is whether **entangling** distant nodes (via photonic Bell-pair distribution to NV centers, an experimentally demonstrated capability) can realize genuine state-level network invariance in the sense of Section 3.2 for a nontrivial (non-product) state, and whether doing so provides any sensing advantage.

### 4.2 GHZ-type network states

An \(N\)-node Greenberger-Horne-Zeilinger (GHZ) state,

\[
|\mathrm{GHZ}\rangle = \frac{1}{\sqrt2}\left(|0\rangle^{\otimes N} + |1\rangle^{\otimes N}\right),
\]

distributed across the network via entanglement swapping, is invariant under the *collective, correlated* subgroup \(g_1=g_2=\cdots=g_N\) of \(G_{\mathrm{net}}\) — reproducing the diagonal-subgroup case noted in Section 3.4's dictionary — but is not invariant under fully independent per-node rotation, consistent with the general result of Section 3.2. This is the network-scale generalization of the two-particle singlet construction of candidates #3–5, and known Heisenberg-limited sensing protocols using GHZ-distributed sensor networks exploit exactly this collective-rotation invariance/covariance structure for phase estimation.

### 4.3 A genuinely per-node-independent invariant state

The only way to realize an invariant subspace under the *full*, non-collective \(G_{\mathrm{net}}\) with a non-classical (correlated) state is to construct correlations that live entirely in the frame-independent sector at each node individually — for instance, correlating the *timing* of spin-flip events (a classical, frame-independent channel at each node) rather than any coherence or phase relationship between nodes' frame-relative sublevels. This is achievable with existing distributed-magnetometry protocols and underscores Section 3.3's point: the practically useful invariant structure in this platform is carried by classical, per-node-invariant observables, not by exotic multi-node entangled states, which instead realize the weaker, collective-subgroup invariance illustrated in Section 4.2.

---

## 5. Proposed Network Architecture and Protocol

1. Deploy \(N\ge3\) independently-mounted NV magnetometer nodes at known relative positions, each with independent crystallographic orientation \(\hat n_k\) and independent microwave/optical control and readout, following candidate #1's single-node design.
2. Establish a classical timing and control-parameter synchronization link (GPS-disciplined clock or equivalent) across all nodes.
3. Record each node's zero-field-split transition frequency continuously, verifying per-node admissibility invariance under local field perturbation exactly as in candidate #1's Section 5.1 protocol, performed independently at each node.
4. Compute baseline cross-correlations of the recorded per-node invariant observables and verify, by direct comparison against a simulated null (uncorrelated-noise) model, that any detected common-mode signal (e.g., a coordinated magnetic transient) is consistent with the network-admissible construction of Section 3.3.
5. As an extension, distribute GHZ or Bell-pair entanglement across a subset of nodes (Section 4.2) and repeat the correlation analysis, comparing the entangled-network sensitivity to the classical (unentangled) baseline of steps 1–4.

---

## 6. What This System Does Not Measure

Consistent with candidates #1–6:

- **No coupling to \(e^a{}_\mu\) or \(\omega^{ab}{}_\mu\).** Each node's individual physics is identical to candidate #1's; the network layer adds only classical or entanglement-based correlation structure among independent nodes, with no gravitational coupling introduced by the act of networking them.
- **No connection between nodes, physical or synthetic.** This is the key structural distinction from candidate #6: there is no tunneling amplitude, no synthetic gauge field, and no measurable holonomy relating one node's frame to another's — nodes are correlated only through shared preparation (entanglement) or shared external signals (common-mode fields), never through anything playing the role of \(\omega^{ab}{}_\mu\) itself.
- **No torsion sensitivity or frame-transport measurement**, for the same reasons given in candidate #1, Section 6, applied independently at each node.
- **Baseline correlation for magnetic-anomaly or geodetic sensing is an established, practically useful application of this architecture in its own right**, entirely independent of any framet interpretation; this paper's contribution is solely to characterize which parts of that established application correspond to which parts of §7–8's admissibility formalism, not to claim new sensing capability.

---

## 7. Discussion: Independence as the Structurally Interesting Case

Where candidate #6 was structurally interesting because its nodes *were* connected (by a real, engineered, measurable connection), this candidate is structurally interesting for the opposite reason: its nodes are deliberately **not** connected, and the paper's contribution is to show precisely what invariance structure survives that absence. The result — that useful multi-node correlations require only independent per-node observable-level admissibility, not any exotic state-level invariance under the full uncoordinated product group — is, we believe, the correct general lesson for any distributed sensing network built from admissibility-respecting individual nodes, and clarifies why entanglement (Section 4), while providing a known metrological (Heisenberg-limit) advantage for the collective-rotation-invariant GHZ case, is not required for the basic admissibility consistency of a distributed network's classical correlation structure.

---

## 8. Conclusion

The distributed spin-qubit magnetometer network extends the single-node admissibility and invariant-subspace formalism of candidate #1 to a genuinely multi-node setting in which, unlike candidate #6's connected lattice, no physical or synthetic connection relates the independent nodes' local frames. We show that the network-level invariance relevant to real distributed-sensing applications is carried by per-node invariant *observables* rather than by any exotic multi-node invariant *state*, that entangled (GHZ-type) network states realize a weaker, collective-subgroup invariance structurally analogous to candidates #3–5's two-particle singlets, and that a concrete, buildable protocol exists to verify both cases experimentally using established NV-magnetometry and entanglement-distribution techniques. As with every candidate in this tier, no coupling to the gravitational sector of the underlying theory is present or claimed.

---

## Appendix A: Symbol Glossary

| Symbol | Meaning |
|---|---|
| \(N\) | number of network nodes |
| \(\hat n_k\) | crystallographic axis of node \(k\) |
| \(G_k\) | per-node admissibility group |
| \(G_{\mathrm{net}}\) | network admissibility group, direct product of per-node groups |
| \(\mathcal I_{G_{\mathrm{net}}}\) | network-level state invariant subspace |
| \(|\mathrm{GHZ}\rangle\) | \(N\)-node Greenberger-Horne-Zeilinger entangled state |

## Appendix B: Why Product States Suffice for Observable-Level Invariance

For a product state \(\Phi=\bigotimes_k|\phi_k\rangle\) with each \(|\phi_k\rangle\in\mathcal I_{G_k}\) individually, direct computation gives

\[
U(g_1,\ldots,g_N)\Phi = \bigotimes_k U_k(g_k)|\phi_k\rangle = \bigotimes_k|\phi_k\rangle = \Phi,
\]

for any independent choice of \(g_k\in G_k\), confirming that per-node invariance is both necessary and sufficient for product-state network invariance, with no entanglement required — the formal basis for Section 3.3's claim.

## Appendix C: GHZ State Non-Invariance Under Independent Rotation

For the GHZ state of Section 4.2, an independent rotation of node 1 alone by angle \(\theta_1\) about \(\hat n_1\) (with all other nodes unrotated) introduces a relative phase between the \(|0\rangle^{\otimes N}\) and \(|1\rangle^{\otimes N}\) branches proportional to \(\theta_1\) alone, which is not compensated by any other node's transformation and therefore changes the state — direct confirmation that the GHZ state fails the full network-invariance condition of Section 3.2 whenever the applied group element departs from the diagonal (collective-rotation) subgroup.

## Appendix D: Open Questions for Future Network Framet Work

- Can a hybrid architecture combining candidate #6's connected-lattice structure at short range (within a single deployed sensor cluster) with candidate #7's independent-node structure at long range (between clusters) be used to demonstrate both invariance regimes within a single experimental system?
- Is there a meaningful intermediate case — partial, time-varying correlation between a subset of nodes' local frames, short of a full engineered connection — that would require a generalization of the direct-product admissibility group \(G_{\mathrm{net}}\) of Section 3.1 to something structurally closer to a genuine (if still synthetic) connection, bridging this candidate and candidate #6?
- What is the practical Heisenberg-limit sensing advantage, if any, of the entangled GHZ-network variant (Section 4.2) over the classical baseline (Section 3.3) for a realistic long-baseline (kilometer-scale) magnetic anomaly detection task, given realistic entanglement-distribution loss and decoherence over such distances?

---

## Selected References

1. J. F. Barry et al., "Sensitivity optimization for NV-diamond magnetometry," *Reviews of Modern Physics*.
2. D. Kómár et al., "A quantum network of clocks," *Nature Physics*.
3. Q. Zhuang, Z. Zhang, J. H. Shapiro, "Distributed quantum sensing using continuous-variable multipartite entanglement," *Physical Review A*.
4. E. Bagan, M. A. Ballester, R. Muñoz-Tapia, O. Romero-Isart, "Optimal full estimation of qubit mixed states," *Physical Review A* (GHZ-state sensing context).
5. Companion foundational work: *Frame Theory: A Local-Frame Formulation of Gravitation and the Admissibility Structure of General Relativity*, §7–8.
6. Companion white papers: *The NV-Center Spin Qubit Array* (candidate #1); *The Trapped-Ion Qubit* (candidate #2); *The NMR/ESR Ensemble* (candidate #3); *The Superconducting Transmon Qubit* (candidate #4); *The Optical Polarization Qubit* (candidate #5); *The Cold-Atom Optical-Lattice Framet* (candidate #6).
7. Companion survey: terrestrial framet candidate list, item #7.
