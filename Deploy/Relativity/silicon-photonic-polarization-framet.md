# The Silicon Photonic Polarization-Qubit Chip: An Integrated-Waveguide Framet Bridging the Optical and Silicon Branches

**Preprint — August 2, 2026**
**M. Brownlee — Dust LLC**

**Keywords:** framet, silicon photonics, silicon-on-insulator, integrated polarization optics, waveguide birefringence, admissibility group, invariant subspace, on-chip Pancharatnam phase

---

## Abstract

The silicon photonic polarization-qubit chip is the analogous tier's synthesis candidate, combining the free-space polarization-optics framet of candidate #5 with the silicon-fabrication lineage developed by candidate #4 (passive substrate) and candidate #8 (active spin host). Built on a silicon-on-insulator (SOI) platform, this device replaces candidate #5's bulk waveplates and polarizers with lithographically defined waveguide birefringence, polarization rotators, and splitters, giving the same Poincaré-sphere \(SU(2)\) representation and admissibility-invariant circular-polarization sector as candidate #5, but realized as a chip-scale, mass-fabricable, thermally and mechanically stable integrated device rather than a free-space tabletop optical train. This paper develops the waveguide-birefringence local frame, re-derives candidate #5's invariant-subspace and Pancharatnam-phase constructions in the integrated-photonics setting, and identifies this candidate's distinguishing structural contribution: because the waveguide geometry (rather than a physical crystal cut, as in a bulk waveplate) sets the birefringent axis, a single chip can host an *array* of independently-designed local frames at fixed, lithographically fixed orientations across its surface — a monolithic, non-reconfigurable but arbitrarily dense analog of the Pancharatnam-Berry metasurface (candidate #11), fabricated using the same silicon photonic process flow already surveyed as a genuine-tier frame-transport platform (candidate #15, the silicon photonic ring-resonator gyroscope). As with all analogous-tier candidates, no coupling to the gravitational tetrad or spin connection is present or claimed.

---

## 1. Introduction

### 1.1 Position in the survey

This candidate sits at the intersection of three threads already developed in this programme:

- **Candidate #5** established the free-space polarization qubit as an analogous framet, with circular polarization as the axial-invariant state and the Pancharatnam phase as the historically original geometric-phase demonstration.
- **Candidates #4 and #8** established silicon's two structural roles in this survey — passive substrate and active spin host, respectively.
- **Candidate #15**, in the genuine tier of the broader survey, uses silicon photonic ring resonators for Sagnac-effect rotation sensing, establishing that silicon photonic fabrication is already a mature platform for polarization- and phase-sensitive integrated optics at the precision this paper's construction requires.

This paper's contribution is to show that candidate #5's polarization-qubit framet transfers essentially without modification to the integrated-photonics setting, while gaining the array-density and fabrication-reproducibility advantages already established for silicon photonics elsewhere in this survey.

### 1.2 Scope statement

As with candidates #1–8, this paper treats the silicon photonic polarization qubit strictly as a representation-theoretic and geometric-phase demonstration platform. No coupling to \(e^a{}_\mu\) or \(\omega^{ab}{}_\mu\), torsion sensitivity, or physical frame-transport measurement is present or claimed. Full discussion in Section 7.

---

## 2. Physical System

### 2.1 Waveguide birefringence as the local frame

An SOI waveguide's cross-sectional geometry (width, height, and any intentional asymmetry) determines its effective-index difference between the transverse-electric (TE) and transverse-magnetic (TM) guided modes — the on-chip analog of a bulk waveplate's fast/slow axis birefringence. Because this geometry is set at the mask-design stage and fixed by the lithography and etch process, each waveguide segment's "fast axis" (in practice, the TE/TM mode basis orientation relative to the chip's crystal and layout axes) is a **fixed, lithographically determined local frame**, in the same structural sense as the NV center's crystal axis (candidate #1) rather than the reconfigurable frame of the trapped ion or bulk waveplate (candidates #2, #5). Reconfigurability, where desired, is achieved not by physically rotating an element (impossible for a fixed waveguide) but by cascading multiple fixed-axis elements at different lithographically-set angles — the on-chip analog of composing HWP/QWP rotations at fixed angles, developed in Section 2.3.

### 2.2 Integrated polarization control elements

Standard SOI polarization photonics building blocks include polarization rotators (adiabatic waveguide tapers or asymmetric directional couplers that rotate the TE/TM basis by a designed angle), polarization splitters/rotator-splitters (which separate or interconvert TE and TM components), and, in more advanced designs, thermo-optic or electro-optic phase shifters that impart a controllable relative phase between polarization components without physically rotating any element. Together these give access to arbitrary on-chip \(SU(2)\) polarization transformations, composed from fixed-angle rotator elements and tunable phase shifters, in direct analogy to candidate #5's HWP/QWP composition (Appendix B of that paper) but with the rotation angles baked into the lithographic design rather than set by a mechanical rotation stage.

### 2.3 On-chip Poincaré-sphere representation

The identification of Section 2.2 of candidate #5 — \(|H\rangle\leftrightarrow|0\rangle\), \(|V\rangle\leftrightarrow|1\rangle\), or equivalently the on-chip \(|\mathrm{TE}\rangle,|\mathrm{TM}\rangle\) basis — carries over without modification: the on-chip polarization state occupies the same Poincaré/Bloch sphere as the free-space case, with the waveguide's guided-mode structure replacing free-space propagation as the physical carrier.

---

## 3. Correspondence to the Framet Formalism

### 3.1 Fixed-array admissibility groups

Each waveguide segment \(k\) on the chip, with its own lithographically-set TE/TM basis orientation \(\theta_k\), carries its own local admissibility group

\[
G_k = \mathrm{Stab}(\hat f_k) \simeq U(1)_{\hat f_k}\subset SU(2),
\]

directly analogous to candidate #5's Section 3.1 construction, but now — as with the multi-orientation NV array of candidate #1, Section 4.2, and unlike the single reconfigurable waveplate of candidate #5's baseline device — realized as a spatial array of *fixed*, independently-set local frames across a single chip, each frame's orientation chosen once at design time and unchangeable after fabrication (absent the tunable phase-shifter elements of Section 2.2, which modulate relative phase rather than the birefringent axis orientation itself).

### 3.2 Circular polarization as the on-chip invariant state

By the identical argument given in candidate #5, Section 3.1, circularly polarized light propagating in a waveguide segment is invariant under the axial stabilizer of the propagation direction — though it is worth noting explicitly that "circular polarization" in a strongly guided, high-index-contrast SOI waveguide is a more subtle construction than in free space, since the guided TE and TM modes generally have different effective indices and group velocities, so a true propagation-invariant circular state requires either a symmetric (square or near-square) waveguide cross-section engineered to equalize TE/TM effective index, or restriction to a specific coupling point (e.g., directly at a symmetric junction) rather than being invariant along an arbitrary length of standard rectangular waveguide. This is a genuine engineering constraint not present in the free-space case, and is treated further in Section 5.

### 3.3 On-chip Pancharatnam phase

A closed sequence of on-chip polarization rotator elements — implementing a lithographically fixed path on the Poincaré sphere, analogous to candidate #5's polarizer-triangle protocol (Section 4.1 of that paper) but with each "polarizer angle" replaced by a fixed rotator-element design angle — produces the same geometric phase,

\[
\phi_{\mathrm{Pancharatnam}} = -\frac{1}{2}\Omega(\gamma),
\]

now measurable via on-chip interferometry (a Mach-Zehnder interferometer comparing the rotator-sequence arm against a reference arm) rather than free-space beam interference, giving a chip-integrated version of candidate #5's Section 4.1 protocol.

### 3.4 Explicit dictionary

| Frame Theory (§2, §7–8) | Silicon photonic chip realization |
|---|---|
| Local frame direction | Waveguide TE/TM birefringent axis, lithographically fixed per segment |
| Admissibility group \(G_k\) per segment | \(U(1)_{\hat f_k}\subset SU(2)\) |
| State space | On-chip guided-mode polarization state (TE/TM basis) |
| Invariant subspace, axial case | Engineered circular polarization at a symmetric waveguide cross-section |
| Holonomy \(\mathcal H[\gamma]\) | On-chip Pancharatnam phase from a cascaded rotator sequence, read via integrated Mach-Zehnder interferometry |
| Multi-frame array | Chip-wide layout of independently-designed rotator segments, fixed at fabrication |

---

## 4. Relation to the Pancharatnam-Berry Metasurface (Candidate #11)

Candidate #5, Section 4.2 identified the free-space Pancharatnam-Berry metasurface as the natural spatial extension of the single free-space waveplate framet, with the metasurface's meta-atom array promoting the waveplate angle to a continuous function of transverse position, \(\hat f(x,y)\). The silicon photonic chip developed here is a structurally distinct, complementary extension: rather than patterning a *transverse* (surface-normal, free-space-propagation) array of local frames as the metasurface does, this platform patterns a *longitudinal, in-plane* sequence and network of local frames along and across guided-wave paths on a chip, with light confined to and routed through the waveguide network rather than propagating freely through the patterned surface. Both are, in the terms of §2.1's frame bundle language, spatially extended arrays of the single-point local frame construction of candidate #5 — one extended across a free-space transverse plane (the metasurface), the other extended across a guided-wave circuit topology (this chip) — and a natural open question, raised in Section 7, is whether a single fabrication process could combine both extensions into one hybrid free-space/guided-wave device.

---

## 5. Fabrication Considerations and Engineering Constraints

### 5.1 TE/TM effective-index engineering for the invariant state

As noted in Section 3.2, realizing a genuinely propagation-invariant circular-polarization state on a standard high-index-contrast SOI waveguide requires deliberate cross-sectional engineering (near-square core geometry, or specialized polarization-independent waveguide designs already studied in the silicon photonics literature for polarization-diversity applications) to equalize TE and TM effective indices. This is a solved engineering problem in the sense that polarization-independent and polarization-maintaining SOI waveguide designs are already an active, mature area of silicon photonics, but it means the invariant-state demonstration on this platform requires a specific, non-default waveguide cross-section rather than being automatically available on arbitrary chip real estate, unlike the free-space case (candidate #5) where circular polarization is invariant under axial rotation regardless of any medium-engineering choice.

### 5.2 Fixed-array versus reconfigurable tradeoff

Because the local frame orientation is lithographically fixed (Section 2.1), this platform trades candidate #2 and #5's real-time reconfigurability for fabrication reproducibility and array density: a single SOI chip can host many more independently-oriented local frame elements, at much smaller pitch, than any free-space optical table or trapped-ion apparatus could practically accommodate, at the cost of being unable to demonstrate the live admissibility-group-rotation protocol of candidate #2, Section 4.1 on any single fixed element (though the effect can be approximated by routing light through different, differently-oriented fixed elements, giving a spatially rather than temporally sampled version of the same underlying transformation).

---

## 6. Proposed Chip Architecture

A test chip is proposed comprising:

1. A row of fixed-angle polarization rotator elements at systematically varied design angles \(\theta_k\), each followed by an on-chip polarimeter (integrated polarization-diverse photodetector pair) for direct \(SU(2)\)-transformation verification, reproducing candidate #5, Appendix B's waveplate-action calculation in lithographic rather than mechanical form.
2. A symmetric-cross-section waveguide segment engineered per Section 5.1, with input and output polarization-diverse grating couplers, to verify the propagation-invariant circular-polarization state directly.
3. A cascaded rotator-sequence Mach-Zehnder interferometer implementing the on-chip Pancharatnam-phase protocol of Section 3.3, with multiple independent loop geometries to sample different enclosed solid angles \(\Omega(\gamma)\) and verify the predicted phase-versus-solid-angle relationship.
4. A dense two-dimensional array of independently-routed rotator segments at varied orientations, as a chip-scale, guided-wave analog of the multi-orientation frame array first proposed for the NV center (candidate #1, Section 4.2) and the metasurface comparison of Section 4 above.

---

## 7. What This Device Does Not Measure

Consistent with candidates #1–8:

- **No coupling to \(e^a{}_\mu\) or \(\omega^{ab}{}_\mu\).** Waveguide birefringence and polarization rotation arise from classical dielectric waveguide electrodynamics; nothing couples to the gravitational tetrad or spin connection.
- **No torsion sensitivity.** As with candidate #5, guided photons carry no net spin density relevant to the torsion-sourcing mechanism of §5.3.
- **No frame-transport measurement.** The waveguide birefringent axes are fixed by lithography, not by inertial transport; this distinguishes the present candidate sharply from candidate #15 (the silicon photonic *ring-resonator gyroscope*), which uses a structurally different measurement principle — Sagnac-effect phase accumulation from physical rotation of the entire chip — despite both candidates sharing the same SOI fabrication platform and, in candidate #15's case, similar-looking integrated interferometry. The two should not be conflated: this paper's Mach-Zehnder interferometer (Section 3.3) measures a *geometric* phase from a fixed polarization-transformation sequence, not a *rotation-induced* Sagnac phase.

---

## 8. Discussion: The Synthesis Candidate

This paper is explicitly a synthesis rather than a structural novelty within the analogous tier: every individual construction used here — waveguide birefringence as a local frame, circular polarization as an axial invariant, cascaded rotators producing a Pancharatnam phase — is a direct lithographic translation of candidate #5's free-space constructions, using the fabrication platform already established as mature and precise by candidate #15 in the genuine tier. Its value to the survey is in demonstrating that the free-space, single-point analogous-tier results are not an artifact of free-space optics specifically, and in providing the fabrication path by which a dense, chip-scale array of the single-element framet construction becomes practical — closing, in a different physical modality, the same "spatially extended frame array" question that candidate #6 addressed for cold-atom lattices and candidate #1 raised (only partially) for NV centers.

---

## 9. Conclusion

The silicon photonic polarization-qubit chip transfers candidate #5's free-space polarization framet to an integrated SOI platform, replacing mechanically rotatable waveplates with lithographically fixed waveguide birefringence and polarization rotator elements. It reproduces the axial-invariant circular-polarization construction (with the added engineering requirement of TE/TM effective-index equalization) and the Pancharatnam geometric-phase measurement, now realized via on-chip Mach-Zehnder interferometry, and offers a fabrication-reproducible, dense-array extension of the single-point construction analogous to, but structurally distinct from, both the free-space Pancharatnam-Berry metasurface (candidate #11) and the cold-atom lattice's connected frame-bundle picture (candidate #6). As with every candidate in this tier, no coupling to the gravitational sector of the underlying theory is present or claimed, and this candidate is explicitly distinguished from the structurally similar-looking but functionally distinct silicon photonic ring-resonator gyroscope (candidate #15) in the genuine tier.

---

## Appendix A: Symbol Glossary

| Symbol | Meaning |
|---|---|
| SOI | silicon-on-insulator |
| TE, TM | transverse-electric, transverse-magnetic guided modes |
| \(\theta_k\) | design orientation angle of rotator segment \(k\) |
| \(\hat f_k\) | birefringent axis of waveguide segment \(k\) |
| \(\Omega(\gamma)\) | solid angle enclosed on the Poincaré sphere by a cascaded rotator sequence |

## Appendix B: Polarization Rotator as an On-Chip \(SU(2)\) Element

An adiabatic waveguide taper rotator implementing a design rotation angle \(\theta\) acts on the on-chip Jones vector identically to the bulk waveplate construction of candidate #5, Appendix B, with the mechanical rotation angle \(\theta\) of that construction replaced by the lithographic design angle of the taper geometry, and the retardance \(\delta\) set by the taper length and adiabaticity rather than by crystal thickness. The resulting \(SU(2)\) matrix form is identical; only the physical mechanism generating the rotation angle differs.

## Appendix C: TE/TM Index-Matching Condition

For a rectangular SOI waveguide core of width \(w\) and height \(h\), the TE-TM effective-index splitting \(\Delta n_{\mathrm{eff}} = n_{\mathrm{TE}}-n_{\mathrm{TM}}\) vanishes at a specific aspect ratio \(w/h\) dependent on the core and cladding refractive indices and the operating wavelength — the design condition underlying the propagation-invariant circular-polarization waveguide segment proposed in Section 5.1 and Section 6, item 2.

## Appendix D: Open Questions for Future Silicon Photonic Framet Work

- Can a single fabrication process combine this paper's guided-wave rotator network with candidate #5's free-space metasurface concept (candidate #11) — e.g., a chip with both on-chip routing and a patterned free-space output grating implementing a metasurface-like transverse phase profile — to realize a genuinely hybrid guided/free-space frame array?
- Does the dense rotator array proposed in Section 6, item 4 permit a chip-scale demonstration of spatially varying holonomy analogous to the cold-atom lattice's plaquette curvature measurement (candidate #6, Section 4.2), using a two-dimensional mesh of interferometrically-linked rotator loops rather than a single Mach-Zehnder sequence?
- What is the practical fabrication-tolerance limit on independently verifying each element's design angle \(\theta_k\) post-fabrication, and how does process variation across a chip affect the fidelity of the multi-frame array construction proposed here relative to the discrete, physically distinct fabrication of the NV-center multi-orientation array (candidate #1)?

---

## Selected References

1. D. Dai, J. E. Bowers, "Silicon-based on-chip multiplexing technologies and devices for Peta-bit optical interconnects," *Nanophotonics*.
2. W. Bogaerts et al., "Silicon microring resonators," *Laser & Photonics Reviews*.
3. H. Guan et al., "Compact and low loss silicon photonic waveguide polarization rotator," *Optics Express* (representative polarization-rotator design literature).
4. Y. Xu, J. Yao, "Compact polarization-independent silicon photonic devices," representative survey of the polarization-diversity engineering referenced in Section 5.1.
5. Companion foundational work: *Frame Theory: A Local-Frame Formulation of Gravitation and the Admissibility Structure of General Relativity*, §2, §7–8.
6. Companion white papers: *The NV-Center Spin Qubit Array* (candidate #1); *The Superconducting Transmon Qubit* (candidate #4); *The Optical Polarization Qubit* (candidate #5); *The Cold-Atom Optical-Lattice Framet* (candidate #6); *The Silicon Spin Qubit* (candidate #8).
7. Companion survey: terrestrial framet candidate list, item #9, item #11 (Pancharatnam-Berry metasurface), and item #15 (silicon photonic ring-resonator gyroscope, genuine tier).
