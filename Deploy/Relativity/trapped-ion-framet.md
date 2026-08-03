# The Trapped-Ion Qubit: A Field-Defined Framet and the Case for Dynamical Frame Reconfigurability

**Preprint — August 2, 2026**
**M. Brownlee — Dust LLC**

**Keywords:** framet, trapped ion, hyperfine qubit, quantization axis, SU(2) representation, admissibility group, invariant subspace, dynamical frame control, Paul trap

---

## Abstract

The trapped-ion qubit extends the structural correspondence established for the NV-center framet (candidate #1) in one decisive respect: where the NV center's local frame is fixed permanently by the host crystal lattice, the trapped ion's local frame — the quantization axis set by an externally applied, actively controlled magnetic field — is **dynamically reconfigurable** by the experimenter. This paper develops the trapped-ion qubit as an analogous framet realizing the admissibility group \(SU(2)\subset\mathrm{Spin}(1,3)\) of *Frame Theory* §7–8, in which the hyperfine (or Zeeman) ground-state manifold carries the relevant \(SU(2)\) representation and specific stretched or clock states serve as the admissibility-invariant subspace \(\mathcal I_G\). We show that the field-defined nature of the ion's local frame allows a class of experiments unavailable to the lattice-fixed NV framet: direct, controlled rotation of the admissibility group itself, live demonstration of how frame-relative and invariant quantities exchange roles under a change of \(G\), and multi-ion architectures in which each trapped ion carries an independently steerable local frame within a shared trap — the closest bench-realizable analog to a frame bundle with a freely specifiable connection. As with the NV-center paper, we are explicit that this remains a representation-theoretic realization with no coupling to the gravitational tetrad or spin connection.

---

## 1. Introduction

### 1.1 The trapped ion as the second framet calibration instrument

Candidate #1 established that the NV-center's crystal axis and spin-1 triplet instantiate the terrestrial admissibility structure of §8.3 with high fidelity but with one structural limitation: the frame \(\hat n\) is fixed by the host lattice and cannot be varied within a single defect. A trapped ion removes this limitation. In a Paul or Penning trap, a single ion (commonly \(^9\mathrm{Be}^+\), \(^{40}\mathrm{Ca}^+\), \(^{171}\mathrm{Yb}^+\), or \(^{137}\mathrm{Ba}^+\)) is held in a time-averaged harmonic potential by oscillating electric fields, and its internal hyperfine or Zeeman ground-state structure is split and oriented by an externally applied, experimenter-controlled static magnetic field \(\mathbf B\). The quantization axis \(\hat b = \mathbf B/|\mathbf B|\) plays the role of the local frame direction, exactly as \(\hat n\) does for the NV center — but \(\hat b\) can be rotated in the laboratory at will, in real time, by reconfiguring the applied field.

This single difference — a controllable versus a fixed frame — is what elevates the trapped-ion framet beyond a second instance of the same demonstration. It allows the admissibility group itself to be treated as an experimental variable, which is the aspect of §7.4's formalism that the NV-center paper could establish only in the discrete, four-orientation sense of its Appendix D open questions.

### 1.2 Scope statement

As with candidate #1, this paper is explicit that the trapped-ion framet is a representation-theoretic realization of §7–8, not a probe of §2–6's gravitational dynamics. No trapped-ion experiment described here couples to \(e^a{}_\mu\) or \(\omega^{ab}{}_\mu\), sources or responds to torsion, or measures inertial frame transport. The full discussion of this boundary is repeated in Section 7, following the convention established in the NV-center paper.

---

## 2. Physical System

### 2.1 The field-defined local frame

The quantization axis of a trapped ion is set by the vector sum of any applied static magnetic bias field and, where relevant, residual stray fields at the ion's location. In a well-controlled trap, the applied bias field dominates and is set by a pair (or set) of coils external to the vacuum chamber, giving

\[
\hat b(t) = \frac{\mathbf B_{\mathrm{applied}}(t) + \mathbf B_{\mathrm{stray}}}{|\mathbf B_{\mathrm{applied}}(t)+\mathbf B_{\mathrm{stray}}|}.
\]

Because \(\mathbf B_{\mathrm{applied}}(t)\) is directly programmable, \(\hat b(t)\) is a **time-dependent, experimenter-specified local frame** — the ion realizes not a single frame, as the NV center does, but a continuous family of frames parameterized by the coil currents. This is the structural feature this paper is built around.

### 2.2 Hyperfine and Zeeman ground-state manifold

Depending on the ion species, the relevant ground-state manifold is either a hyperfine multiplet (for ions with nonzero nuclear spin, e.g. \(^9\mathrm{Be}^+\), \(^{171}\mathrm{Yb}^+\), \(^{137}\mathrm{Ba}^+\)) or a pure electronic Zeeman multiplet (for ions used in optical or metastable-state qubits, e.g. \(^{40}\mathrm{Ca}^+\)). In either case, the manifold decomposes into total angular momentum sectors, each of which carries a representation of \(SU(2)\) with respect to rotations about \(\hat b\), in the same sense developed for the NV triplet in candidate #1's Section 2.2.

For a hyperfine "clock" qubit, e.g. the \(F=1,m_F=0\) and \(F=2,m_F=0\) states used in \(^9\mathrm{Be}^+\) or \(^{171}\mathrm{Yb}^+\) clock transitions, both computational basis states are themselves \(m_F=0\) sublevels — states annihilated by the axial angular momentum projection operator along \(\hat b\), in direct analogy to the NV center's \(m_s=0\) invariant state.

### 2.3 Coherent control and readout

Trapped-ion qubits are controlled via resonant microwave, RF, or two-photon Raman transitions, and read out via state-dependent fluorescence (electron shelving/quantum-jump detection), giving single-shot readout fidelities exceeding 99.9% in mature systems. This gives a readout channel structurally analogous to the NV center's ODMR fluorescence contrast, but with substantially higher fidelity in state-of-the-art systems, and — crucially for Section 4 — readout that remains well-defined under active reconfiguration of \(\hat b\).

---

## 3. Correspondence to the Framet Formalism

### 3.1 Admissibility group as a controllable object

Following the dictionary established for candidate #1, the trapped ion's admissibility group is the axial stabilizer of the current field direction,

\[
G_{\mathrm{ion}}(t) = \mathrm{Stab}(\hat b(t)) \simeq U(1)_{\hat b(t)} \subset SU(2).
\]

The critical structural extension over the NV-center case is that \(G_{\mathrm{ion}}(t)\) is not a fixed subgroup determined by crystal growth; it is a subgroup **selected in real time by the experimenter**, exactly matching the language of §7.4 — "the admissibility group selected by the physical situation" — in its most literal, controllable form available on the candidate list. Where the NV-center paper could only enumerate four discrete admissibility groups (one per crystallographic orientation), the trapped ion realizes a continuous one-parameter (indeed, two-parameter, over the sphere of field directions) family.

### 3.2 The stretched-state and clock-state invariant subspaces

Two distinct invariant-subspace constructions are available in a trapped ion, corresponding to two different physical roles \(m_F=0\) or "stretched" states can play:

**Clock states** (\(m_F=0\) in both qubit levels): these are, as in Section 2.2, eigenstates of the axial angular momentum projection with eigenvalue zero, and are therefore invariant under \(G_{\mathrm{ion}}(t)\) rotation in exactly the sense of §7.4 and candidate #1's Section 3.2:

\[
\hat F_{\hat b}\,|F,m_F=0\rangle = 0.
\]

This is also, not coincidentally, the reason clock-state qubits are first-magnetic-field-insensitive and hence used for the highest-coherence trapped-ion qubits in the field — the framet-invariance property and the metrological first-order field-insensitivity property are the same statement viewed from two different motivations.

**Stretched states** (\(m_F=\pm F_{\max}\)): these are the states of *maximal* projection along \(\hat b\), and are therefore maximally frame-relative rather than invariant — included here for contrast, since they are the states most commonly used for direct magnetic-field magnitude sensing (as opposed to the framet-invariant clock states used for the invariant-subspace demonstration of Section 4).

### 3.3 Explicit dictionary

| Frame Theory (§2, §7–8) | Trapped-ion realization |
|---|---|
| Local frame direction | Field-defined quantization axis \(\hat b(t)\) |
| Admissibility group \(G\subseteq\mathrm{Spin}(1,3)\) | \(U(1)_{\hat b(t)}\subset SU(2)\), experimenter-tunable |
| State space \(\mathcal S\) | Hyperfine/Zeeman ground-state manifold |
| Invariant subspace \(\mathcal I_G\) | Clock states, \(m_F=0\) |
| Frame-relative quantities (§7.2) | Stretched states \(m_F=\pm F_{\max}\), off-axis coherences |
| Invariant quantities (§7.3) | Clock transition frequency, \(m_F=0\) population |
| Local Lorentz transformation \(\Lambda(x)\) | Applied field rotation \(\hat b(t_1)\to\hat b(t_2)\) |

---

## 4. Proposed Experimental Program

### 4.1 Live demonstration of admissibility-group rotation

Because \(\hat b(t)\) is controllable, the trapped-ion framet supports an experiment unavailable to the NV-center platform: preparing a state invariant under one admissibility group, physically rotating the field to instantiate a *different* admissibility group, and observing that the same state is no longer invariant under the new group unless it is also rotated.

Protocol:

1. Apply field along \(\hat b_1\); prepare the ion in the clock state \(|F,m_F=0\rangle_{\hat b_1}\).
2. Rotate the applied field adiabatically (slow compared to Larmor precession, fast compared to decoherence) to a new direction \(\hat b_2\neq\hat b_1\).
3. Perform state tomography in the \(\hat b_2\)-quantized basis.
4. Observe that the state prepared as "invariant" in the \(\hat b_1\) frame now has nonzero population and coherence spread across the \(\hat b_2\)-frame sublevels, unless \(\hat b_2\) is co-rotated with the internal state via an active compensating pulse sequence.

This is a direct, controllable experimental realization of the transformation law of §2.3 and §7.2 — \(e^a{}_\mu\mapsto\Lambda^a{}_b e^b{}_\mu\) — applied to the admissibility group itself rather than merely to a passive coordinate frame, since the ion's internal state does not automatically co-rotate with the field unless actively driven to do so.

### 4.2 Two-ion independent-frame architecture

In a linear Paul trap or segmented trap array, two (or more) ions can in principle be subjected to independently controllable local field gradients (via segmented trap electrodes and local field coils, or via species-selective addressing in a mixed-species chain), giving each ion its own quantization axis \(\hat b^{(1)}(t)\), \(\hat b^{(2)}(t)\). This is the trapped-ion analog of the NV-center multi-orientation array (candidate #1, Section 4.2), but with each local frame independently and continuously steerable rather than fixed to one of four discrete crystallographic directions — the strongest available bench realization of a frame bundle with per-point (per-ion) reconfigurable orientation.

### 4.3 Holonomy-style closed-loop protocol

Following the field rotation of Section 4.1, a closed-loop protocol — rotating \(\hat b\) around a closed path on the sphere of directions and returning to \(\hat b_1\) — allows measurement of any geometric (Berry) phase acquired by the internal state, in direct analogy to the holonomy construction of §7.3,

\[
\mathcal H[\gamma] = \mathcal P\exp\left(\oint_\gamma\omega\right),
\]

specialized to the abelian \(U(1)\) connection induced by adiabatic field rotation rather than the full non-abelian \(\mathrm{Spin}(1,3)\) connection of the gravitational theory. This gives the trapped-ion framet a further structural feature the NV-center platform cannot easily access: a bench-measurable analog of a connection holonomy, using standard Berry-phase trapped-ion protocols already established in the field.

---

## 5. Comparison to the NV-Center Framet

| Property | NV center (#1) | Trapped ion (#2) |
|---|---|---|
| Frame origin | Fixed by host crystal lattice | Set by applied field, fully controllable |
| Number of accessible frames per device | 4 (discrete, crystallographic) | Continuous (any direction on sphere) |
| Readout | Optical (ODMR), room temperature | Fluorescence/shelving, typically requires trap vacuum/cooling |
| Invariant subspace | \(m_s=0\) | \(m_F=0\) clock states |
| Holonomy/connection demonstration | Not directly accessible | Directly accessible via field-rotation Berry phase |
| Multi-frame bundle demonstration | Discrete four-orientation, single crystal | Continuous, per-ion independently steerable |

The two platforms are complementary rather than redundant: the NV center demonstrates that the admissibility structure is real in a *fixed*, solid-state, room-temperature setting; the trapped ion demonstrates that the same structure supports *active, controllable* transformations, including a bench realization of holonomy, which is the closest either analogous-tier candidate comes to touching the connection-transport language of §7.3 — while still, as emphasized throughout, carrying zero gravitational coupling.

---

## 6. What This Device Does Not Measure

Repeating the discipline established for candidate #1:

- **No coupling to \(e^a{}_\mu\) or \(\omega^{ab}{}_\mu\).** The ion's Hamiltonian is set by applied electromagnetic fields and internal atomic structure; nothing couples to the gravitational tetrad or spin connection.
- **No torsion sensitivity.** The atomic spin density involved is far too small and far too well-isolated from any macroscopic spin-polarized source to have any relation to the torsion-sourcing mechanism of §5.3.
- **No frame-transport measurement.** The field-defined axis \(\hat b(t)\) is set by laboratory apparatus, not by inertial transport; it has no relationship to \(\omega^{ab}{}_\mu\)-mediated parallel transport, unlike the gyroscope-class genuine candidates (#4, #13–18).
- **The Berry-phase holonomy of Section 4.3 is abelian and field-induced**, not the non-abelian \(\mathrm{Spin}(1,3)\) holonomy of §7.3; the correspondence is structural (both are holonomies of a connection under transport around a closed loop) but the connection being measured is an ordinary electromagnetic/adiabatic one, not the gravitational spin connection.

---

## 7. Discussion: The Value of a Controllable Frame

The central methodological point of this paper is that a *controllable* local frame is pedagogically and experimentally stronger than a fixed one for demonstrating admissibility-group formalism, precisely because it allows the group \(G\) itself to be varied and its effect on invariance directly observed, rather than only observed as a static fact about one fixed frame. This mirrors the theoretical structure of §7.4 more completely than the NV-center paper could: "the admissibility group selected by the physical situation" is best demonstrated by a system in which the physical situation — here, the applied field direction — is itself an experimental knob. The tradeoff is operational complexity: trapped-ion systems require vacuum, laser cooling, and (for most species) cryogenic or near-cryogenic trap electrode temperatures, versus the room-temperature, comparatively simple operation of the NV-center platform.

---

## 8. Conclusion

The trapped-ion qubit realizes the same SU(2) admissibility structure as the NV-center framet, with the decisive addition of a dynamically controllable local frame. Clock-state sublevels (\(m_F=0\)) serve as the admissibility-invariant subspace \(\mathcal I_G\) in direct analogy to the NV center's \(m_s=0\) state, while the field-defined quantization axis allows live experimental demonstration of admissibility-group rotation, multi-ion independently-steerable local frames, and — uniquely among the analogous-tier candidates surveyed so far — a bench-realizable holonomy measurement structurally analogous to (though physically distinct from) the connection-transport formalism of §7.3. As with candidate #1, this remains firmly in the analogous tier: a precise, controllable representation-theoretic realization of the terrestrial admissibility group, with no coupling to the gravitational sector of the theory.

---

## Appendix A: Symbol Glossary

| Symbol | Meaning |
|---|---|
| \(\hat b(t)\) | field-defined quantization axis, time-dependent |
| \(F\), \(m_F\) | total angular momentum quantum number and projection |
| \(G_{\mathrm{ion}}(t)\) | axial admissibility subgroup, \(U(1)_{\hat b(t)}\subset SU(2)\) |
| \(\hat F_{\hat b}\) | angular momentum projection operator along \(\hat b\) |
| \(\mathcal H[\gamma]\) | holonomy of a closed field-rotation loop \(\gamma\) |

## Appendix B: Clock-State Field Insensitivity as Invariance

To first order in applied field magnitude, the energy of a clock transition \(|F_1,m_F=0\rangle\to|F_2,m_F=0\rangle\) is independent of \(|\mathbf B|\); this is the standard justification for using such transitions as atomic clocks and high-coherence qubits. In the framet language of Section 3.2, this first-order insensitivity is the energetic signature of the state's invariance under the admissibility group \(G_{\mathrm{ion}}\): a state with \(m_F=0\) has zero axial angular-momentum projection, so its energy (which couples to \(|\mathbf B|\) through the projection quantum number at leading order) is insensitive to the field magnitude, though it remains sensitive at second order through quadratic Zeeman shifts not captured by the linear admissibility-invariance argument alone.

## Appendix C: Relation to Adiabatic Berry Phase

For a spin-\(F\) state adiabatically transported around a closed loop \(\gamma\) on the sphere of field directions, the accumulated geometric phase is proportional to the solid angle enclosed by \(\gamma\),

\[
\phi_{\mathrm{Berry}} = -m_F\,\Omega(\gamma),
\]

where \(\Omega(\gamma)\) is the solid angle. Because \(m_F=0\) clock states acquire zero geometric phase under this construction, they are trivially holonomy-invariant as well as admissibility-invariant — the two invariance properties coincide for the same reason: zero axial angular momentum projection.

## Appendix D: Open Questions for Future Trapped-Ion Framet Work

- Can a fully non-abelian holonomy (rather than the abelian \(U(1)\) Berry phase of Appendix C) be engineered in a trapped-ion system, e.g. via degenerate dressed-state manifolds, to more closely approximate the non-abelian \(\mathrm{Spin}(1,3)\) connection structure of §7.3?
- Can the two-ion independent-frame architecture of Section 4.2 be scaled to a chain sufficient to demonstrate an engineered, spatially-varying admissibility group across many ions — the trapped-ion analog of the spatially-varying tetrad field raised as an open question for the NV-center array?
- Is there a meaningful entangled-state extension of the invariant-subspace construction — i.e., a multi-ion entangled state invariant under simultaneous, correlated rotation of multiple independently-defined local frames — that would extend the single-particle admissibility formalism of §7.4 to a genuinely multi-frame invariant sector?

---

## Selected References

1. D. J. Wineland, "Nobel Lecture: Superposition, entanglement, and raising Schrödinger's cat," *Reviews of Modern Physics*.
2. C. Langer et al., "Long-lived qubit memory using atomic ions," *Physical Review Letters*.
3. M. V. Berry, "Quantal phase factors accompanying adiabatic changes," *Proceedings of the Royal Society A*.
4. C. Monroe, R. Raussendorf, A. Ruthven, K. R. Brown, P. Maunz, L.-M. Duan, J. Kim, "Large-scale modular quantum-computer architecture with atomic memory and photonic interconnects," *Physical Review A*.
5. Companion foundational work: *Frame Theory: A Local-Frame Formulation of Gravitation and the Admissibility Structure of General Relativity*, §7–8.
6. Companion white paper: *The NV-Center Spin Qubit Array* (candidate #1).
7. Companion survey: terrestrial framet candidate list, item #2.
