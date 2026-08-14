# The Optical Polarization Qubit: A Waveplate-Referenced Framet and the Historical Origin of Geometric Phase

**Preprint — August 2, 2026**
**M. Brownlee — Dust LLC**

**Keywords:** framet, polarization qubit, Poincaré sphere, waveplate, Pancharatnam phase, geometric phase, admissibility group, invariant subspace, optical local frame

---

## Abstract

The optical polarization qubit is the analogous-tier candidate with the deepest historical connection to the mathematics *Frame Theory* itself deploys: the Pancharatnam phase, the first geometric phase ever identified in physics, was discovered in exactly this system — the phase acquired by a light beam's polarization state under a sequence of polarizer/waveplate transformations — decades before Berry's more general adiabatic quantum-mechanical treatment that candidate #2 (trapped ion) used to demonstrate an abelian holonomy. This paper develops the polarization qubit as an analogous framet in which a waveplate's fast axis defines the local frame, the photon's two-dimensional polarization state carries an \(SU(2)\)-type representation via the Poincaré sphere (formally the same representation as a spin-1/2 particle's Bloch sphere), and the admissibility-invariant subspace is realized either trivially (circular polarization, invariant under rotation about the propagation axis) or, in a two-photon extension, as a polarization-entangled Bell state directly analogous to candidates #3–4's spin/qubit singlets. Because this candidate was already flagged in the broader framet survey as the physical mechanism underlying the Pancharatnam-Berry metasurface (candidate #11), this paper also serves to connect the single-qubit analogous tier explicitly to that metamaterial candidate, clarifying that the metasurface is, structurally, a spatially patterned array of the single-qubit device developed here. As with all analogous-tier candidates, no coupling to the gravitational tetrad or spin connection is present or claimed.

---

## 1. Introduction

### 1.1 Historical priority

In 1956, S. Pancharatnam showed that when a beam of polarized light is subjected to a cyclic sequence of polarization transformations (via polarizers and/or waveplates) returning it to its original polarization state, the emergent beam acquires a phase shift determined entirely by the geometry of the path traced on the Poincaré sphere — specifically, half the solid angle enclosed — independent of the details of how the path was traversed. This is, in modern language, exactly the geometric (holonomy) phase later generalized by Berry to arbitrary adiabatic quantum evolution, and used in candidate #2's Section 4.3 to demonstrate an abelian holonomy in a trapped-ion system. The Pancharatnam construction predates Berry's by nearly three decades and was carried out in precisely the polarization-optics setting this paper now formalizes as a framet.

This historical fact matters for the survey's internal consistency: candidate #2 borrowed the general Berry-phase formalism to demonstrate abelian holonomy in a matter-qubit system, while the optical polarization qubit is the system in which the *specific case* of that formalism was first discovered, using light rather than matter. Including it in the survey closes a historical gap as much as a structural one.

### 1.2 Scope statement

Consistent with candidates #1–4, this paper treats the polarization qubit strictly as a representation-theoretic and (in the geometric-phase sense) connection-formalism demonstration. No coupling to \(e^a{}_\mu\) or \(\omega^{ab}{}_\mu\), torsion sensitivity, or frame-transport measurement is present or claimed. Full discussion in Section 7.

---

## 2. Physical System

### 2.1 The waveplate-defined local frame

A waveplate is a birefringent optical element whose fast and slow axes, fixed by the crystal cut and mount orientation, define a reference direction transverse to the beam propagation axis. For a wave plate mounted in a rotatable holder, this reference direction — call it \(\hat f\), the fast-axis direction — is directly analogous to the trapped ion's field-defined axis \(\hat b(t)\) of candidate #2: it is set by external apparatus (here, a mechanical rotation stage) rather than fixed permanently as in the NV center's crystal lattice (candidate #1), and it can be reconfigured between measurements or, with a fast electro-optic or liquid-crystal variable retarder, within a single measurement sequence.

### 2.2 The Poincaré sphere as a Bloch sphere

The polarization state of a fully polarized light beam is described by a point on the Poincaré sphere, with poles corresponding to right- and left-circular polarization, the equator to linear polarization at all orientations, and intermediate latitudes to elliptical polarization. This is mathematically identical in structure to the Bloch sphere representation of a spin-1/2 or two-level qubit state used throughout candidates #1–4: the Poincaré sphere *is* a Bloch sphere, with the identification

\[
|H\rangle\leftrightarrow|0\rangle,\qquad|V\rangle\leftrightarrow|1\rangle,
\]

for horizontal/vertical linear polarization as the computational basis, or equivalently \(|R\rangle,|L\rangle\) (circular polarization) as an alternative basis, exactly as \(|0\rangle,|1\rangle\) versus \(|+\rangle,|-\rangle\) are alternative bases for a matter qubit.

### 2.3 Waveplates as \(SU(2)\) rotation generators

A half-wave plate (HWP) at fast-axis angle \(\theta\) acts on the Poincaré sphere as a rotation by \(\pi\) about an axis in the equatorial plane at angle \(2\theta\); a quarter-wave plate (QWP) acts as a rotation by \(\pi/2\) about the corresponding axis. Arbitrary \(SU(2)\) single-qubit rotations are achievable via composed HWP/QWP sequences, giving the polarization qubit the same universal single-qubit control available to the transmon (candidate #4) via IQ-phase/amplitude engineering, but realized through purely passive, static (non-time-dependent) optical elements — a third distinct physical mechanism (after crystal lattice, applied field/microwave) for realizing arbitrary \(SU(2)\) control within this survey.

---

## 3. Correspondence to the Framet Formalism

### 3.1 Circular polarization as the axial-invariant state

Propagation-axis rotation — rotating the entire optical setup about the beam's own propagation direction — leaves circularly polarized light unchanged up to the geometric (Pancharatnam-type) phase discussed in Section 4, while linearly or elliptically polarized light (away from circular) transforms nontrivially, acquiring a rotated orientation. This gives circular polarization the same structural role as \(|m_s=0\rangle\) (candidate #1) or \(|F,m_F=0\rangle\) (candidate #2): invariance under the axial stabilizer subgroup of a chosen propagation direction,

\[
G_{\mathrm{pol}} = \mathrm{Stab}(\hat k)\simeq U(1)_{\hat k}\subset SU(2),
\]

with \(\hat k\) the beam propagation direction rather than a crystal or field axis — a further variant on "what physically defines the frame direction" across the analogous tier.

### 3.2 Polarization-entangled photon pairs

Spontaneous parametric down-conversion (SPDC) and related nonlinear-optical processes routinely generate polarization-entangled photon pairs in Bell states, including the singlet-like combination

\[
|\Psi^-\rangle = \frac{1}{\sqrt2}\left(|H\rangle_1|V\rangle_2 - |V\rangle_1|H\rangle_2\right),
\]

which, under the polarization-to-spin identification of Section 2.2, is exactly the same abstract state as the NMR/ESR nuclear-spin singlet (candidate #3) and the two-transmon Bell singlet (candidate #4), and inherits the identical full-\(SU(2)\)-invariance property under simultaneous, correlated waveplate rotation of both photons' measurement bases. This gives the polarization qubit a third independent physical realization of the full-admissibility-group invariant subspace \(\mathcal I_{SU(2)}\), alongside candidates #3 and #4 — now demonstrated across nuclear spins, superconducting circuits, and photons.

### 3.3 Explicit dictionary

| Frame Theory (§2, §7–8) | Polarization-qubit realization |
|---|---|
| Local frame direction | Waveplate fast axis \(\hat f\) (transverse); propagation axis \(\hat k\) (axial invariance case) |
| Admissibility group \(G\subseteq\mathrm{Spin}(1,3)\) | \(SU(2)\), realized via composed HWP/QWP sequences |
| State space \(\mathcal S\) | Photon polarization state, Poincaré/Bloch sphere |
| Invariant subspace, axial case | Circular polarization \(|R\rangle\) or \(|L\rangle\) |
| Invariant subspace, full-group case | Two-photon polarization-entangled singlet \(|\Psi^-\rangle\) |
| Holonomy \(\mathcal H[\gamma]\) | Pancharatnam-Berry geometric phase from a closed polarization-transformation loop |
| Local Lorentz transformation \(\Lambda(x)\) | Waveplate rotation \(\theta\to\theta'\) |

---

## 4. The Pancharatnam-Berry Geometric Phase

### 4.1 Direct measurement protocol

1. Prepare a linearly polarized beam.
2. Pass it through a sequence of polarizers and/or waveplates implementing a closed path on the Poincaré sphere — e.g., three linear polarizers at successively rotated angles \(0^\circ\to\alpha\to\beta\to0^\circ\), tracing a closed geodesic triangle.
3. Interfere the output beam with a reference (unperturbed) beam derived from the same source.
4. Measure the interference fringe shift, which directly gives the accumulated phase

\[
\phi_{\mathrm{Pancharatnam}} = -\frac{1}{2}\Omega(\gamma),
\]

with \(\Omega(\gamma)\) the solid angle enclosed by the closed path on the Poincaré sphere — the same functional form as the trapped-ion Berry phase of candidate #2, Appendix C, with the spin-1/2 factor of \(m_F\) replaced by the photon's intrinsic two-level (spin-1 photon, but polarization restricted to the transverse two-dimensional subspace) structure.

### 4.2 Relation to the Pancharatnam-Berry metasurface (candidate #11)

The Pancharatnam-Berry metasurface, flagged in the broader framet survey as an analogous-tier metamaterial candidate, is constructed from an array of nanoscale waveplate-equivalent meta-atoms, each set to a locally engineered fast-axis rotation angle, such that light traversing the metasurface at each spatial location acquires a local geometric phase determined by that location's meta-atom orientation. This paper's single-element protocol (Section 4.1) is therefore the elementary building block of that metasurface: the metasurface is precisely a spatially patterned array of the local-frame construction developed here, with the waveplate fast-axis angle promoted from a single global experimental parameter to a function of transverse position, \(\hat f(x,y)\) — the optical analog of a spatially-varying tetrad field \(e^a{}_\mu(x)\) raised as an open question in candidate #1's Appendix D and only partially addressed there via discrete crystallographic orientation. The polarization qubit and the metasurface should therefore be read as a single-point/many-point pair within this survey, in the same relationship as candidate #1's single-defect NV framet and its proposed multi-orientation array (candidate #1, Section 4.2).

---

## 5. Comparison Across the Analogous Tier

| Property | NV center (#1) | Trapped ion (#2) | NMR/ESR (#3) | Transmon (#4) | Polarization qubit (#5) |
|---|---|---|---|---|---|
| Frame origin | Fixed crystal axis | Controllable applied field | Controllable applied field | Synthetic microwave IQ frame | Rotatable waveplate axis |
| Full-\(SU(2)\)-invariant state | Not directly (axial only) | Not directly (axial only) | Singlet (nuclear spin) | Singlet analog (circuit qubit) | Singlet analog (photon pair) |
| Holonomy type | Not accessible | Abelian (first quantum-mechanical demonstration) | Not directly probed | Non-abelian (engineered dark space) | Abelian (historically first demonstration, pre-dating Berry) |
| Operating environment | Room temperature, solid-state | Vacuum, laser-cooled | Room temperature or cryogenic | Millikelvin, dilution refrigerator | Room temperature, tabletop optics |
| Natural multi-point/array extension | Multi-orientation crystal array | Multi-ion independent-frame chain | Multi-pair ensemble (inherent) | Multi-transmon coupled lattice | Pancharatnam-Berry metasurface (#11) |

The polarization qubit is, alongside the NV center, the most experimentally accessible member of the analogous tier — requiring only tabletop linear optics rather than cryogenics, vacuum systems, or microwave engineering — while simultaneously carrying the deepest historical claim to having originated the geometric-phase mathematics the entire tier's holonomy demonstrations depend on.

---

## 6. What This Device Does Not Measure

Consistent with candidates #1–4:

- **No coupling to \(e^a{}_\mu\) or \(\omega^{ab}{}_\mu\).** Polarization transformation is governed by classical and quantum electrodynamics in a birefringent medium; nothing couples to the gravitational tetrad or spin connection.
- **No torsion sensitivity.** Photon polarization carries no net electron or nuclear spin density in the sense required to source or respond to the torsion-mediated coupling of §5.3.
- **No frame-transport measurement.** The waveplate axis \(\hat f\) is set by a mechanical rotation stage in the laboratory, not by inertial or gravitational parallel transport; it bears no relationship to \(\omega^{ab}{}_\mu\)-mediated frame transport, unlike the genuine-tier gyroscope candidates.
- **The Pancharatnam-Berry phase of Section 4 is an abelian phase in an optical polarization-transformation space**, structurally analogous to but not identical in physical origin to the trapped-ion Berry phase of candidate #2, and — as with all analogous-tier holonomies in this survey — is not a measurement of the non-abelian gravitational connection holonomy of §7.3, for which only candidate #4's engineered dark-space construction has so far demonstrated the correct (non-abelian) algebraic type.

---

## 7. Discussion: Five Platforms, One Formalism

With candidates #1–5 now complete, the analogous tier has demonstrated the admissibility-group and invariant-subspace formalism of §7–8 across five independent physical substrates — solid-state defect spin, trapped atomic ion, coupled nuclear/electron spin ensembles, superconducting circuit, and photon polarization — using three distinct physical mechanisms for realizing the local frame (crystal lattice, applied field, and now passive birefringent optics), three demonstrations of the full-\(SU(2)\)-invariant singlet/Bell state (candidates #3–5), and both abelian (candidates #2, #5) and non-abelian (candidate #4) holonomy realizations. The cross-platform reproducibility of the singlet-invariance result in particular — identical group-theoretic content, verified independently in nuclear spins, superconducting qubits, and photons — is, within the scope this survey claims for itself, a meaningful consistency check on the representation theory underlying §7–8, even though none of these platforms individually or collectively bears on the gravitational dynamics of §2–6.

---

## 8. Conclusion

The optical polarization qubit realizes the terrestrial framet's passive-optics case: a rotatable waveplate axis supporting arbitrary \(SU(2)\) single-qubit control, a circular-polarization axial-invariant state directly analogous to candidates #1–2's invariant sublevels, a polarization-entangled two-photon singlet reproducing candidates #3–4's full-group-invariance result on a third independent platform, and the historically original demonstration of the abelian geometric phase later generalized as the Berry phase used throughout this survey. Its structural relationship to the Pancharatnam-Berry metasurface (candidate #11) as the single-point building block of that spatially-extended device gives this candidate a direct bridge to the metamaterial branch of the broader framet survey. As with all analogous-tier candidates, no coupling to the gravitational sector of the underlying theory is present or claimed.

---

## Appendix A: Symbol Glossary

| Symbol | Meaning |
|---|---|
| \(\hat f\) | waveplate fast-axis direction |
| \(\hat k\) | beam propagation axis |
| \(|H\rangle,|V\rangle\) | horizontal/vertical linear polarization basis states |
| \(|R\rangle,|L\rangle\) | right/left circular polarization basis states |
| \(\Omega(\gamma)\) | solid angle enclosed by a closed path on the Poincaré sphere |
| \(\phi_{\mathrm{Pancharatnam}}\) | Pancharatnam geometric phase |

## Appendix B: Waveplate Action as an \(SU(2)\) Element

A waveplate with retardance \(\delta\) and fast axis at angle \(\theta\) acts on the Jones vector (equivalently, the qubit state vector) as the unitary

\[
W(\theta,\delta) = R(\theta)\begin{pmatrix}e^{-i\delta/2}&0\\0&e^{i\delta/2}\end{pmatrix}R(-\theta),
\]

with \(R(\theta)\) the ordinary \(2\times2\) rotation matrix. For \(\delta=\pi\) (half-wave plate), this reduces to a rotation by \(\pi\) about the equatorial axis at angle \(2\theta\) on the Poincaré sphere; for \(\delta=\pi/2\) (quarter-wave plate), a rotation by \(\pi/2\) about the same axis. Composition of HWP and QWP elements at various angles generates the full \(SU(2)\) group, establishing the claim of Section 2.3.

## Appendix C: Two-Photon Singlet Invariance

As in candidate #3, Appendix B and candidate #4, Appendix C, the invariance calculation for \(|\Psi^-\rangle\) proceeds identically under the identification \(|H\rangle\to|\uparrow\rangle\), \(|V\rangle\to|\downarrow\rangle\): the state is annihilated by all three generators of the collective \(SU(2)\) transformation \(U(g)\otimes U(g)\), independent of the physical nature of the two-level systems being combined — the third independent confirmation, within this survey, that the underlying representation theory is substrate-agnostic.

## Appendix D: Open Questions for Future Polarization-Qubit Framet Work

- Can a dynamically reconfigurable (electro-optic or liquid-crystal) waveplate array realize the spatially-varying admissibility-group demonstration proposed for the metasurface (candidate #11) but with real-time, rather than fixed-fabrication, control over \(\hat f(x,y,t)\) — extending Section 4.2's static structural correspondence to an actively controllable one?
- Does a three-photon or higher-order polarization-entangled state (GHZ-type) realize an invariant subspace under a larger admissibility group than \(SU(2)\), in parallel with the open question raised for multi-spin NMR states in candidate #3, Appendix D?
- Can the Pancharatnam-phase protocol of Section 4.1 be adapted to demonstrate a *non-abelian* holonomy using higher-dimensional photonic degrees of freedom (e.g., orbital angular momentum combined with polarization), bringing the photonic platform into structural parity with the transmon's non-abelian holonomy result (candidate #4)?

---

## Selected References

1. S. Pancharatnam, "Generalized theory of interference and its applications," *Proceedings of the Indian Academy of Sciences A*.
2. M. V. Berry, "The adiabatic phase and Pancharatnam's phase for polarized light," *Journal of Modern Optics*.
3. R. Bhandari, "Polarization of light and topological phases," *Physics Reports*.
4. P. G. Kwiat et al., "New high-intensity source of polarization-entangled photon pairs," *Physical Review Letters*.
5. Companion foundational work: *Frame Theory: A Local-Frame Formulation of Gravitation and the Admissibility Structure of General Relativity*, §7–8.
6. Companion white papers: *The NV-Center Spin Qubit Array* (candidate #1); *The Trapped-Ion Qubit* (candidate #2); *The NMR/ESR Ensemble* (candidate #3); *The Superconducting Transmon Qubit* (candidate #4).
7. Companion survey: terrestrial framet candidate list, item #5 and item #11 (Pancharatnam-Berry metasurface).
