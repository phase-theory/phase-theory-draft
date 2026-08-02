# Relativity Mechanics: The Framet
## Formal Definition, Degeneracy Chain, and the Physical Realization of Frame-Relative Information

**White paper / academic preprint**

---

## Abstract

Relativity 1.0 established a general schema, \(\mathcal{R}=(\Omega,G,\rhd,I)\), in which a physical quantity is a description \(\omega\in\Omega\) together with an admissibility group \(G\) acting via \(\rhd\), and the physical content is the invariant \(I(\omega)=[\omega]\in\Omega/G\). That paper left the schema abstract. This paper gives it a physical carrier.

We define the **framet**: a physical system whose accessible, logical state is not a configuration but an orbit — a system engineered so that its readout is, by construction, a \(G\)-invariant observable. The framet is built by the same move Phase Mechanics used to build the phaset from the qubit, run one level higher: where Phase Mechanics generalized the qubit by restoring amplitude and topological-sector structure that the qubit discards, Relativity Mechanics generalizes the phaset by restoring the admissibility group \(G\) that a phaset — like a qubit — is ordinarily assumed not to need. This yields an exact degeneracy chain,

\[
\text{qubit} \;\subset\; \text{phaset} \;\subset\; \text{framet},
\]

with each inclusion realized by a precise limit: a phaset is a framet with trivial \(G\); a qubit is a phaset with frozen coherence amplitude and trivial topological sector, and therefore also a framet with all three restrictions imposed at once.

The physical mechanism already exists in the laboratory. Two qubits subjected to a common (collective) but otherwise unknown \(SU(2)\) rotation possess a one-dimensional invariant subspace — the singlet — and four qubits possess a two-dimensional invariant subspace sufficient to encode one fully robust logical qubit. This is the decoherence-free-subspace construction of Zanardi–Rasetti and Lidar–Chuang–Whaley, experimentally verified by Kwiat et al. We show that this construction is, in the vocabulary of this series, already a framet, and we use it as the terrestrial probe requested for the physical realization of Relativity Mechanics. The central principle is:

\[
\boxed{
\text{A framet does not store a configuration. It stores an orbit — and it is exactly as robust as the admissibility group it is built to ignore.}
}
\]

---

## 1. Introduction

Relativity 1.0 closed with a formal object, \(\mathcal{R}=(\Omega,G,\rhd,I)\), and a claim that this object is domain-general: the same schema that relativizes spacetime coordinates under the Lorentz group also relativizes probability assignments under refinement and coarse-graining (Relativity 31.0). What it did not do — deliberately, since it was a foundational paper — is say what a *physical device* built to realize that schema would look like.

This paper answers that question. The answer is not a new kind of qubit; it is a new relationship between a system and the group acting on it. Where Phase Mechanics took the qubit and restored the amplitude and topological structure it discards, arriving at the phaset, this paper takes the phaset (or the qubit, taken as a phaset with that structure re-frozen) and restores the one thing *it* still discards: the admissibility group \(G\) that Relativity 1.0 showed no physical quantity can be defined without. The result is the framet.

The paper proceeds by first restating, self-containedly, the two pieces of formalism it depends on (§2–3); then defining the framet and its physical carrier (§4–6); establishing the degeneracy chain rigorously (§8); giving physical realizability criteria (§10); and finally grounding all of it in a construction that requires no new physics to build, only a new frame in which to interpret an experiment that has already been performed (§12–14).

---

## 2. Recap: The Relativity Structure Schema

A relativity structure is a tuple \(\mathcal{R}=(\Omega,G,\rhd,I)\):

- \(\Omega\) is a set of frame-relative descriptions;
- \(G\) is a group (or groupoid) of admissible transformations;
- \(\rhd:G\times\Omega\to\Omega\) is a group action;
- \(I:\Omega\to\Omega/G\) sends a description to its orbit \([\omega]=\{g\rhd\omega:g\in G\}\).

Physical law constrains \(I(\omega)\), never \(\omega\) itself (Relativity 1.0, §13). For the spacetime case, \(\Omega\) is the set of event coordinates, \(G\) is the Lorentz or diffeomorphism group, and \(I\) returns the interval \(ds^2\) or a curvature invariant. This paper takes \(\Omega\) to be a Hilbert space (or a phaset configuration space, §14), \(G\) to be a physically realizable group of transformations acting on that space, and asks what a device looks like whose only accessible output is \(I(\omega)\).

---

## 3. Recap: The Phaset

Phase Mechanics defines the phaset as a point on the Phase Configuration Manifold — a stratified fiber bundle carrying, at minimum, a coherence amplitude, a phase, and a topological sector. The qubit is recovered as the special case in which the amplitude is frozen (fixed at a reference value) and the topological sector is trivial, leaving only the phase degree of freedom — a two-level system, the Bloch sphere.

We will not re-derive the Phase Configuration Manifold here; we treat it as an already-established object and use only the one fact this paper needs from it: **a phaset is a configuration, not yet a frame-relative one.** Nothing in the definition of a phaset specifies an admissibility group \(G\) or asks what survives a change of frame. That is the gap this paper fills.

---

## 4. Formal Definition of the Framet

**Definition (Framet).** Let \(\Omega\) be a configuration space (a Hilbert space, or a phaset configuration space) and let \(G\) be a group with an action \(\rhd\) on \(\Omega\), physically realized as a class of transformations (an unknown or fluctuating rotation, boost, or re-phasing) that the device cannot be assumed to be free of. A **framet** is a physical system \(\mathcal{F}=(\Omega,G,\rhd,I,\rho)\) in which:

1. the physical carrier's raw state is some \(\rho\) supported on \(\Omega\) (or a mixture over the orbit of some \(\omega\in\Omega\) induced by an unknown \(g\in G\)), and
2. the only state the device is designed to prepare, manipulate, or read out is the invariant \(I(\rho)\) — i.e., every operation used on the framet is required to commute with the action of \(G\).

The framet is thus not merely "a system with some symmetry." It is a system in which the logical information has been deliberately relocated from \(\Omega\) to \(\Omega/G\), so that whatever physically implements \(g\in G\) — a stray rotation, an uncalibrated reference frame, a boost — acts as the identity on the information that matters.

\[
\boxed{
\text{A qubit is defined by its state. A framet is defined by what it refuses to depend on.}
}
\]

---

## 5. Invariant Subspaces and the Physical Meaning of \(I\)

For a compact group \(G\) with a unitary representation \(U(g)\) on a Hilbert space \(\mathcal{H}\), the projector onto the \(G\)-invariant subspace is

\[
P_{\mathrm{inv}} = \int_G U(g)\,d\mu(g),
\]

with \(\mu\) the normalized Haar measure (\(\mu(G)=1\)). This is a standard fact of representation theory (the projection formula onto the trivial isotypic component): \(P_{\mathrm{inv}}\) commutes with every \(U(g)\), and its image,

\[
\mathcal{H}_{\mathrm{inv}} = P_{\mathrm{inv}}\,\mathcal{H} = \{\,|\phi\rangle\in\mathcal{H} : U(g)|\phi\rangle=|\phi\rangle\ \forall g\in G\,\},
\]

is exactly the physical realization of \(I:\Omega\to\Omega/G\) restricted to states: a state prepared in \(\mathcal{H}_{\mathrm{inv}}\) is, by construction, its own invariant. No further averaging or post-processing is needed — the orbit and the representative coincide.

For an *irreducible* representation acting on a single elementary system, \(\mathcal{H}_{\mathrm{inv}}\) is generically trivial (zero- or one-dimensional): a single qubit under an unknown \(SU(2)\) rotation has no nontrivial invariant state, precisely because the whole point of irreducibility is that \(G\) acts transitively enough to mix everything together. A nontrivial framet therefore requires a *reducible* representation — which is exactly what a composite, multi-subsystem carrier provides (§7).

---

## 6. Collective Admissibility Groups and Relational Encoding

The admissibility groups of Relativity 1.0 (Lorentz, diffeomorphism) act on a single event's coordinates. The admissibility groups relevant to a laboratory framet act **collectively**: the same unknown group element \(g\) acts on every subsystem of the carrier simultaneously,

\[
U(g)^{\otimes n} = U(g)\otimes U(g)\otimes\cdots\otimes U(g),
\]

because the physical source of \(g\) — an uncalibrated shared reference frame, a fiber's unknown birefringence, a common magnetic field drift — is common to all \(n\) subsystems by construction (they are co-located, co-propagated, or otherwise physically coupled to the same environment). This is the regime in which decoherence-free subspaces (DFS) against collective noise were first identified (Zanardi & Rasetti, 1997; Lidar, Chuang & Whaley, 1998), and it is the regime this paper adopts as the framet's native physical setting.

The key fact, worked out explicitly in §12–13, is that \(U(g)^{\otimes n}\) generically *does* possess a nontrivial invariant subspace even when a single-particle \(U(g)\) does not — because the tensor product of irreducible representations decomposes into a sum of irreducibles, one of which (the trivial one) survives projection by \(P_{\mathrm{inv}}\).

---

## 7. Framet Composability and Multi-Framet Systems

Two framets \(\mathcal{F}_1=(\Omega_1,G,\rhd_1,I_1,\rho_1)\) and \(\mathcal{F}_2=(\Omega_2,G,\rhd_2,I_2,\rho_2)\) sharing a common admissibility group \(G\) compose into a joint framet on \(\Omega_1\otimes\Omega_2\), with \(G\) acting diagonally: \(g\rhd(\omega_1\otimes\omega_2) = (g\rhd_1\omega_1)\otimes(g\rhd_2\omega_2)\). The invariant subspace of the joint system is not simply the tensor product of the two invariant subspaces — it also picks up cross terms from non-invariant components of \(\mathcal{H}_1\) and \(\mathcal{H}_2\) that combine, under the diagonal action, into new invariants. This is precisely the mechanism by which two one-dimensional single-pair invariant subspaces (§12) combine into a two-dimensional joint invariant subspace (§13): the whole is more invariant than the sum of its parts.

---

## 8. The Degeneracy Chain: Qubit ⊂ Phaset ⊂ Framet

**Proposition (Degeneracy Chain).**

1. *Framet → Phaset.* If \(G=\{e\}\) (the trivial group), then \(U(e)=\mathbb{1}\) is the only group element, \(P_{\mathrm{inv}}=\mathbb{1}\), and \(\mathcal{H}_{\mathrm{inv}}=\mathcal{H}\). The invariance condition is vacuous, and a framet over \(\Omega\) with trivial \(G\) is exactly a bare configuration in \(\Omega\) — a phaset, if \(\Omega\) is taken to be the Phase Configuration Manifold.

2. *Phaset → Qubit.* Independently of \(G\), freezing the phaset's coherence amplitude to a fixed reference value and restricting to the trivial topological sector collapses the Phase Configuration Manifold to the Bloch sphere — the qubit (established in Phase Mechanics).

3. *Framet → Qubit.* Composing both restrictions — \(G=\{e\}\) and frozen amplitude/trivial sector — collapses a framet directly to a qubit.

\[
\boxed{
\text{qubit} = \text{framet}\Big|_{G=\{e\},\ \text{frozen amplitude},\ \text{trivial sector}}\ \subset\
\text{phaset} = \text{framet}\Big|_{G=\{e\}}\ \subset\ \text{framet}.
\]

Each inclusion is a restriction of structure that the more general object carries and the more specialized object does not: the phaset restores amplitude and topology that the qubit discards; the framet restores, on top of that, the admissibility group that the phaset discards. Formal derivations are collected in Appendix D.

---

## 9. Physical Realizability: What a Framet Needs

Not every pair \((\Omega,G)\) yields a device that is useful, or even buildable. We propose six criteria, in the spirit of — but independent from — the Phase DiVincenzo Criteria already on record for the phaset.

### RDC-1: Admissibility-Group Realizability
\(G\) must correspond to an actual, physically occurring class of uncertainty or transformation acting on the substrate (an unknown collective rotation, boost, or re-phasing) — not a merely formal symmetry with no physical source.

### RDC-2: Nontrivial Invariant Subspace
The joint representation \(U(g)^{\otimes n}\) must possess an invariant subspace \(\mathcal{H}_{\mathrm{inv}}\) of dimension \(\geq 2\), sufficient to encode at least one logical degree of freedom.

### RDC-3: Frame-Blind Preparability
States within \(\mathcal{H}_{\mathrm{inv}}\) must be preparable with high fidelity without first determining the ambient value of \(g\).

### RDC-4: \(G\)-Invariant Gate Set
Logical operations must be implementable using physical operations that commute with \(U(g)^{\otimes n}\) for all \(g\in G\), so that gates do not themselves require knowledge of the frame.

### RDC-5: Invariant Readout
A measurement (observable or POVM) must exist whose outcome depends only on \(I(\rho)\), never on the specific representative \(\rho\) within its orbit.

### RDC-6: Differential Decoherence
The decoherence rate of the logical (invariant) degrees of freedom under realistic noise must be measurably lower than the decoherence rate of the raw, frame-dependent degrees of freedom of the same physical carrier. Without RDC-6, a framet is a valid formal construction with no operational advantage over an ordinary phaset or qubit — RDC-6 is the criterion that makes it worth building.

---

## 10. Differential Decoherence: The Physical Payoff

RDC-6 is the framet's reason for existing. An ordinary qubit or phaset stores information in \(\omega\in\Omega\) directly; any physical process implementing an unrecorded, unknown \(g\in G\) — a stray rotation of a polarization analyzer, an uncontrolled magnetic-field drift, an uncalibrated relative phase between two stations — corrupts \(\omega\) and hence the stored information. A framet stores information in \(I(\omega)=[\omega]\in\Omega/G\); the same physical process, by definition of \(\mathcal{H}_{\mathrm{inv}}\), leaves \(I(\omega)\) exactly fixed.

This is not immunity to *all* noise — only to noise that factors through the admissibility group \(G\) the framet was built against. Noise that acts differently on different subsystems (rather than collectively) is not suppressed by this construction, and remains an open engineering problem (§18).

---

## 11. Worked Example: The Frame-Invariant Qubit (FIQ)

Recall the proposal from the preceding discussion: two spatially separated stations, an entangled photon pair, each station's polarization analyzer independently uncalibrated relative to the other. In the framet vocabulary:

- \(\Omega = \mathcal{H}=\mathbb{C}^2\otimes\mathbb{C}^2\), the two-photon polarization space;
- \(G=SU(2)\), realized physically as an unknown *collective* rotation common to both photons (valid when both photons traverse a shared unstable channel, e.g. co-propagation through the same fiber before separation, or a shared magnetic environment);
- \(\rhd\) is the representation \(U(g)\otimes U(g)\);
- \(I\) is the projection onto the invariant subspace identified explicitly in §12.

This is the FIQ construction proposed earlier, now given its precise place in the framet formalism: it is the minimal (two-qubit) instance of a framet with \(G=SU(2)\).

---

## 12. The Singlet Construction: A Framet That Already Exists

The two-qubit space decomposes under collective \(SU(2)\) as

\[
\mathbb{C}^2\otimes\mathbb{C}^2 = \underbrace{\mathrm{span}\{|\psi^-\rangle\}}_{\text{spin-0, singlet}} \ \oplus\ \underbrace{\mathrm{span}\{|00\rangle,\,|\psi^+\rangle,\,|11\rangle\}}_{\text{spin-1, triplet}},
\]

where \(|\psi^{\pm}\rangle = (|01\rangle\pm|10\rangle)/\sqrt2\). For any \(U\in SU(2)\),

\[
(U\otimes U)\,|\psi^-\rangle = \det(U)\,|\psi^-\rangle = |\psi^-\rangle,
\]

since \(\det(U)=1\) by definition of \(SU(2)\). The singlet is therefore exactly invariant under *any* collective rotation — a one-dimensional \(\mathcal{H}_{\mathrm{inv}}\), realized without approximation, not merely to leading order. This is the smallest nontrivial framet: it satisfies RDC-1 through RDC-3 and RDC-5 immediately, but a single singlet is only one-dimensional and so cannot by itself encode a logical qubit (RDC-2 requires dimension \(\geq 2\)) — it can only serve as an invariant flag or a single robust bit-flag, not a full logical qubit.

---

## 13. The Four-Photon Logical Qubit

Four qubits under collective \(SU(2)\) decompose, by iterated Clebsch–Gordan coupling, into total-spin sectors \(j=0,1,2\), and the \(j=0\) (fully invariant) sector has **multiplicity 2** — there are two linearly independent ways to combine four spin-\(\tfrac12\) systems into total spin zero. This two-dimensional invariant subspace, spanned for example by

\[
|0_L\rangle \propto |\psi^-\rangle_{12}\otimes|\psi^-\rangle_{34},\qquad
|1_L\rangle \propto \Big(2|\psi^-\rangle_{13}\otimes|\psi^-\rangle_{24} - |0_L\rangle\Big)\ \text{(suitably normalized)},
\]

is exactly RDC-2's dimension-\(\geq 2\) requirement, satisfied with equality. This is a genuine logical qubit that is, by construction, invariant under any collective \(SU(2)\) rotation of all four photons — a framet in the full sense of §4, not merely the flag of §12.

This construction is not proposed here for the first time as physics: it is the decoherence-free-subspace logical qubit of Zanardi & Rasetti (1997) and Lidar, Chuang & Whaley (1998), and it was **experimentally demonstrated** by Kwiat, Berglund, Altepeter & White (2000), who verified that a two-photon-pair encoding of this kind survives collective decoherence that destroys an unencoded qubit on the same apparatus. What this paper adds is not a new experiment but a new reading of an existing one: **the Kwiat et al. demonstration already is a physical realization of a framet**, and it is offered here as the terrestrial probe requested for Relativity Mechanics.

---

## 14. Terrestrial Probe Protocol

Building directly on §13, a minimal terrestrial probe explicitly targeting the Relativity Mechanics interpretation — rather than only the DFS/quantum-computing interpretation already published — would:

1. Prepare the four-photon \(j=0\) logical qubit (or the simpler one-dimensional singlet flag of §12) using standard spontaneous parametric down-conversion sources.
2. Introduce a controlled, collective \(SU(2)\) rotation (e.g., a birefringent element common to the shared channel) and verify that logical-qubit fidelity is preserved across the full range of applied rotation — the direct laboratory analogue of Relativity 1.0 §7's demonstration that \(ds^2\) is unchanged across a family of Lorentz frames.
3. In parallel, measure an *uncoded* single-photon polarization qubit through the same collective rotation, showing its fidelity degrades linearly with the (unknown) rotation angle — the direct analogue of Relativity 1.0 §9's frame-dependence of simultaneity and length.
4. Report the ratio of the two decoherence rates as the operational measure of RDC-6, and report it as a function of \(|G|\)-content (i.e., the range of rotation angles actually sampled), testing whether robustness scales as predicted by the dimension of \(\mathcal{H}_{\mathrm{inv}}\).

No new experimental technique is required; the apparatus is the one already used for DFS demonstrations. What is new is treating step 2 and step 3 side by side, explicitly, as a single measurement of the invariant/representative distinction that is this paper's subject.

---

## 15. Framed Phasets: Connecting to the Phase Configuration Manifold

Where \(\Omega\) is taken to be the Phase Configuration Manifold itself (rather than a bare Hilbert space), a framet becomes a *framed phaset*: an admissibility group \(G\) acting on the amplitude, phase, and topological-sector coordinates jointly, with logical information relocated to whatever combination of those coordinates is \(G\)-invariant. We do not attempt a full derivation of this case here, since it depends on structural detail of the Phase Configuration Manifold's stratification beyond what this paper needs for its Hilbert-space-level result (§12–13); we flag it explicitly as the natural next step and return to it in §18.

---

## 16. Relation to the Admissibility Groups of the Relativity Series

The worked example of §11–13 uses \(G=SU(2)\), a physically convenient but comparatively simple admissibility group. Relativity 1.0's roadmap (§19) and Relativity 31.0's measure-relativity results point to considerably richer groups: refinements and coarse-grainings (Relativity 31.0), context relabelings (the Contextuality Relativity specialization referenced there), and eventually the full diffeomorphism group of general relativity itself. Nothing in the framet's definition (§4) restricts \(G\) to compact groups with a well-behaved Haar measure — that restriction was adopted here only because it makes the invariant projector of §5 elementary to write down and the terrestrial probe of §14 buildable with existing hardware. Extending the framet construction to noncompact or infinite-dimensional \(G\) is left as the clearest concrete link to the rest of the series (§18).

---

## 17. Postulates of the Framet

### FP-1 (Substrate)
Every framet is built from an underlying configuration space \(\Omega\), which may be a Hilbert space, a phaset configuration space, or any other admissible domain in the sense of Relativity 1.0.

### FP-2 (Collective Action)
Nontrivial invariant subspaces are most readily engineered by having \(G\) act collectively and identically across two or more subsystems of the substrate; a single, elementary, irreducibly-transforming system generically admits no nontrivial invariant state (§5).

### FP-3 (Invariant Readout)
A framet's logical information is accessed only through \(G\)-invariant observables; measuring a non-invariant observable of the same carrier degrades or destroys the encoded information's frame-robustness.

### FP-4 (Degeneracy)
Setting \(G\) to the trivial group collapses a framet to its underlying substrate configuration (a phaset, or, with amplitude and topology also frozen, a qubit) — §8.

### FP-5 (Compositionality)
Framets sharing a common admissibility group compose (§7); composing enough elementary invariant subspaces can produce a joint invariant subspace of higher dimension than any factor possesses alone (§13).

---

## 18. Open Problems

### 18.1 Noncompact and Infinite-Dimensional \(G\)
The Haar-measure projector of §5 assumes \(G\) compact. Extending the framet construction to the noncompact groups (Lorentz, \(\mathrm{Diff}(M)\)) that motivate the rest of the series is unresolved.

### 18.2 The Framed Phaset
§15's connection to the full Phase Configuration Manifold is stated but not derived; a proper treatment requires engaging the manifold's stratification directly.

### 18.3 Noise Beyond the Collective Case
RDC-6's robustness gain is specific to noise that factors through \(G\) collectively (FP-2). Local, subsystem-specific noise is not suppressed by this construction, and no framet-level analogue of standard quantum error correction has yet been proposed to cover it.

### 18.4 Higher-Dimensional Logical Encodings
§13 gives one logical qubit from four physical qubits. The scaling of invariant-subspace dimension with photon number, and the resulting logical-qubit-per-physical-qubit rate, is not worked out here.

### 18.5 Relation to Gauge Redundancy
Relativity 1.0 (§22.5) left open the distinction between gauge redundancy and genuine frame-relativity. The framet is built entirely on the frame-relative side of that distinction (§4 requires \(G\) to correspond to an actual physical source of uncertainty); whether a "gauge framet" is a coherent notion at all is left open.

---

## 19. Summary of Core Equations

### The framet
\[
\mathcal{F}=(\Omega,\,G,\,\rhd,\,I,\,\rho).
\]

### Invariant projector
\[
P_{\mathrm{inv}} = \int_G U(g)\,d\mu(g),\qquad \mathcal{H}_{\mathrm{inv}} = P_{\mathrm{inv}}\mathcal{H}.
\]

### Degeneracy chain
\[
\text{qubit} = \text{framet}\big|_{G=\{e\},\ \text{frozen amplitude},\ \text{trivial sector}}\ \subset\ \text{phaset} = \text{framet}\big|_{G=\{e\}}\ \subset\ \text{framet}.
\]

### Singlet invariance
\[
(U\otimes U)|\psi^-\rangle = \det(U)|\psi^-\rangle = |\psi^-\rangle,\qquad U\in SU(2).
\]

### Four-photon invariant subspace
\[
\dim\big(\mathcal{H}_{\mathrm{inv}}^{(4)}\big) = 2\quad\text{(multiplicity of }j=0\text{ in four coupled spin-}\tfrac12\text{ systems).}
\]

### Central principle
\[
\boxed{
\text{A framet does not store a configuration. It stores an orbit — and it is exactly as robust as the admissibility group it is built to ignore.}
}
\]

---

## 20. Conclusion

This paper gave Relativity 1.0's abstract schema, \(\mathcal{R}=(\Omega,G,\rhd,I)\), a physical carrier: the framet, a system engineered so that its logical, accessible state is an orbit \(I(\omega)\) rather than a raw configuration \(\omega\). The construction sits in an exact degeneracy chain with the two primitives already on record in this corpus — qubit \(\subset\) phaset \(\subset\) framet — with each step a precise restriction of structure rather than an analogy.

Unlike the phaset's terrestrial probes, which required new deployment proposals against untested substrates, the framet's minimal terrestrial probe requires no new physics: the decoherence-free-subspace logical qubit of Zanardi–Rasetti and Lidar–Chuang–Whaley, built from four photons in two entangled pairs and experimentally verified by Kwiat et al. in 2000, already satisfies every criterion of §9. What this paper contributes is the reading of that result as a physical realization of Relativity Mechanics — and a protocol (§14) for making that reading an explicit, reportable measurement rather than an implicit one.

\[
\boxed{
\text{A framet does not store a configuration. It stores an orbit — and it is exactly as robust as the admissibility group it is built to ignore.}
}
\]

This is Relativity Mechanics: the Framet.

---

## Appendix A: The Invariant Projector for Compact \(G\)

For a compact group \(G\) with normalized Haar measure \(\mu\) and a unitary representation \(U\), define \(P=\int_G U(g)\,d\mu(g)\). For any \(h\in G\), left-invariance of Haar measure gives

\[
U(h)P = \int_G U(h)U(g)\,d\mu(g) = \int_G U(hg)\,d\mu(g) = \int_G U(g')\,d\mu(g') = P,
\]

so \(P\) commutes with every \(U(h)\) and its image is exactly the \(G\)-invariant subspace. Idempotency, \(P^2=P\), follows the same way, confirming \(P\) is a genuine projector.

## Appendix B: Clebsch–Gordan Decomposition of Two Qubits

Two spin-\(\tfrac12\) representations couple as \(\tfrac12\otimes\tfrac12 = 0\oplus 1\). The \(j=0\) singlet is \(|\psi^-\rangle=(|01\rangle-|10\rangle)/\sqrt2\); the \(j=1\) triplet is spanned by \(|00\rangle\), \(|\psi^+\rangle=(|01\rangle+|10\rangle)/\sqrt2\), and \(|11\rangle\). Direct computation confirms \((U\otimes U)|\psi^-\rangle=\det(U)|\psi^-\rangle\) for any \(2\times2\) unitary \(U\), giving exact invariance when \(U\in SU(2)\).

## Appendix C: The Four-Photon Logical Qubit

Coupling four spin-\(\tfrac12\) systems proceeds in two stages: \(\big(\tfrac12\otimes\tfrac12\big)\otimes\big(\tfrac12\otimes\tfrac12\big) = (0\oplus1)\otimes(0\oplus1) = (0\otimes0)\oplus(0\otimes1)\oplus(1\otimes0)\oplus(1\otimes1)\). The \(j=0\) sector receives one copy from \(0\otimes0\) and one further copy from the \(j=0\) piece of \(1\otimes1=0\oplus1\oplus2\), for a total multiplicity of 2 — the two-dimensional invariant subspace used in §13.

## Appendix D: Formal Statement of the Degeneracy Chain

Let \(\mathcal{F}=(\Omega,G,\rhd,I,\rho)\) be a framet with \(\Omega=M_\Phi\), the Phase Configuration Manifold. Setting \(G=\{e\}\) forces \(\mathcal{H}_{\mathrm{inv}}=\mathcal{H}\) (Appendix A with \(G\) trivial), so the invariance condition of Definition §4 is satisfied by every \(\rho\); the framet's constraint set is empty, and \(\mathcal{F}\) reduces to a bare phaset. Independently, restricting \(M_\Phi\) to fixed amplitude and trivial topological sector reduces it, by the definition already on record in Phase Mechanics, to the Bloch sphere. Composing both restrictions on a framet with \(G=\{e\}\) yields both reductions simultaneously, giving the qubit as claimed in §8.

---

## Selected References

1. Relativity 1.0 — Relativity Mechanics: Motion, Frame, and Invariance as the Seed Case of a General Relational Ontology, Dust LLC preprint (2026).
2. Relativity 31.0 — Probability / Measure Relativity: Probability as a Measure-, Context-, and Coarse-Graining-Relative Structure, Dust LLC preprint (2026).
3. PM-DECL-001 and PM-1, Phase Mechanics foundational papers (phaset definition, Phase Configuration Manifold, Phase DiVincenzo Criteria), Dust LLC preprint series (2026).
4. P. Zanardi and M. Rasetti, "Noiseless Quantum Codes," *Physical Review Letters* **79**, 3306 (1997).
5. D. A. Lidar, I. L. Chuang, and K. B. Whaley, "Decoherence-Free Subspaces for Quantum Computation," *Physical Review Letters* **81**, 2594 (1998).
6. P. G. Kwiat, A. J. Berglund, J. B. Altepeter, and A. G. White, "Experimental Verification of Decoherence-Free Subspaces," *Science* **290**, 498 (2000).
7. S. D. Bartlett, T. Rudolph, and R. W. Spekkens, "Classical and Quantum Communication Without a Shared Reference Frame," *Physical Review Letters* **91**, 027901 (2003).
8. S. D. Bartlett, T. Rudolph, and R. W. Spekkens, "Reference Frames, Superselection Rules, and Quantum Information," *Reviews of Modern Physics* **79**, 555 (2007).
9. A. Peres and D. R. Terno, "Quantum Information and Relativity Theory," *Reviews of Modern Physics* **76**, 93 (2004).
10. L. Viola, E. Knill, and S. Lloyd, "Dynamical Decoupling of Open Quantum Systems," *Physical Review Letters* **82**, 2417 (1999).
