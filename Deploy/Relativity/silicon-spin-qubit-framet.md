# The Silicon Spin Qubit: An Isotopically Purified Framet and the All-Silicon Closure of the Analogous Tier

**Preprint — August 2, 2026**
**M. Brownlee — Dust LLC**

**Keywords:** framet, silicon spin qubit, phosphorus donor, quantum dot, isotopic purification, ²⁸Si, admissibility group, invariant subspace, semiconductor vacuum

---

## Abstract

The silicon spin qubit — realized either as a substitutional phosphorus donor electron/nuclear spin (the Kane-type architecture) or as a gate-defined quantum dot in isotopically purified silicon or Si/SiGe heterostructures — closes the analogous tier's fabrication lineage back to silicon proper, complementing candidate #4's silicon-*substrate* transmon (where silicon plays a passive structural role) with a platform in which silicon is the **active** spin-carrying medium itself. This paper develops the silicon spin qubit as an analogous framet in the same structural sense as candidates #1–7: an applied bias field defines the local frame, the donor or dot's electron and/or nuclear spin carries an \(SU(2)\) representation, and a field-aligned sublevel serves as the admissibility-invariant subspace. Its distinguishing structural contribution to this survey is at the level of *frame-noise suppression* rather than frame or connection structure per se: isotopic purification to ²⁸Si (the only silicon isotope with zero nuclear spin) removes the dominant source of local magnetic-field fluctuation that would otherwise randomly perturb the admissibility group itself from shot to shot, giving this platform the most stable admissibility group of any candidate surveyed to date and, correspondingly, the longest measured coherence times of any solid-state spin qubit. We also address this candidate's direct relevance to the materials-feasibility discussion of the theoretic-tier spin-doped silicon composite (candidate #24), since silicon donor spin qubits and the SDSC's proposed active layer both confront the same silicon spin-density/coherence tradeoff, from opposite ends: the donor qubit deliberately minimizes ambient spin density to maximize coherence, while the SDSC deliberately maximizes it to source a torsion field. As with all analogous-tier candidates, no coupling to the gravitational tetrad or spin connection is present or claimed.

---

## 1. Introduction

### 1.1 Two silicon roles, now both covered

Candidate #4 (superconducting transmon) noted explicitly that silicon serves there only as a low-loss dielectric substrate, with the active quantum element (the Josephson junction and its aluminum or niobium electrodes) fabricated on top of, rather than within, the silicon crystal. This paper addresses the complementary case: silicon as the active spin-carrying host itself, either through a substitutional dopant's bound electron and nuclear spin (Section 2.2) or through electrostatically confined conduction-band electrons in a gate-defined quantum dot (Section 2.3). Together, candidates #4 and #8 give the analogous tier complete coverage of the two distinct roles silicon plays across the broader framet survey's fabrication-focused candidates — passive substrate (transmon, and the genuine-tier silicon MEMS gyroscopes) and active spin host (this paper, and the theoretic-tier spin-doped silicon composite, candidate #24).

### 1.2 Why isotopic purification is the structurally interesting feature

Natural silicon is 92.2% \(^{28}\mathrm{Si}\) (nuclear spin \(I=0\)), 4.7% \(^{29}\mathrm{Si}\) (\(I=1/2\)), and 3.1% \(^{30}\mathrm{Si}\) (\(I=0\)). The \(^{29}\mathrm{Si}\) nuclear spins, though a small minority species, are the dominant source of magnetic-field noise experienced by an electron or donor spin qubit in natural silicon, through the hyperfine and dipolar coupling of the qubit to the surrounding nuclear spin bath. Isotopic enrichment to \(^{28}\mathrm{Si}\) at the 99.9%+ level — technologically demanding but experimentally established — removes this noise source almost entirely, producing what the field has termed a "semiconductor vacuum": an electronic or nuclear spin environment as close to magnetically silent as any solid-state host achieved to date. This paper's central structural claim is that isotopic purification should be understood, in the framet language developed across candidates #1–7, as **engineered stabilization of the admissibility group itself** — not a change to the invariant-subspace construction, but a reduction in the rate at which the *ambient* local field (and hence the admissibility group \(G\)) is randomly perturbed by an uncontrolled environmental bath.

---

## 2. Physical System

### 2.1 The applied-field local frame

As with the trapped ion (candidate #2) and the NMR/ESR ensemble (candidate #3), the silicon spin qubit's local frame is set by an externally applied static magnetic field \(\mathbf B_0\), giving a quantization axis \(\hat z=\mathbf B_0/|\mathbf B_0|\) directly analogous to those two platforms' field-defined frames, with the same controllability (field magnitude and orientation are experimenter-set parameters) established there.

### 2.2 Donor-bound spins (Kane-type architecture)

A substitutional phosphorus donor in silicon binds one extra electron in a hydrogenic orbital around the donor nucleus, giving access to two coupled spin-1/2 degrees of freedom: the donor electron spin and the \(^{31}\mathrm{P}\) nuclear spin (\(I=1/2\), the natural and only stable phosphorus isotope). This two-spin system carries the same coupled spin-1/2-pair structure exploited in candidate #3's NMR singlet construction, with the donor's hyperfine coupling playing the role of the J-coupling used there — giving the silicon donor qubit access, in principle, to the same full-\(SU(2)\)-invariant singlet-state construction demonstrated for nuclear spins (candidate #3), superconducting qubits (candidate #4), and photons (candidate #5), now on a fourth independent physical substrate.

### 2.3 Gate-defined quantum dots

An alternative and increasingly dominant architecture confines a small number of conduction-band electrons (down to a single electron) in an electrostatic potential well created by patterned surface gates on a Si/SiGe heterostructure or Si-MOS (metal-oxide-semiconductor) stack. The confined electron's spin carries the same spin-1/2 \(SU(2)\) representation as the donor electron of Section 2.2, addressed via electron spin resonance (ESR) or, in exchange-coupled multi-dot architectures, via the same singlet-triplet manifold structure developed for coupled spin pairs in candidate #3.

### 2.4 Readout

Both architectures are read out via spin-to-charge conversion — using Pauli spin blockade or energy-selective tunneling to convert the spin state into a measurable charge-sensor signal — rather than the optical readout of the NV center (candidate #1) or the fluorescence/shelving readout of the trapped ion (candidate #2). This gives the silicon spin qubit a readout mechanism structurally distinct from every prior candidate in this survey, closer in spirit to the transmon's dispersive microwave readout (candidate #4) in that it is an electrical rather than optical measurement, though the underlying physical mechanism (charge sensing of a spin-dependent tunneling event) is distinct from both.

---

## 3. Correspondence to the Framet Formalism

### 3.1 Standard single-spin dictionary

The single-electron or single-donor case reproduces the axial-invariance structure of candidates #1–2 exactly:

\[
G_{\mathrm{Si}} = U(1)_{\hat z}\subset SU(2),
\qquad
\mathcal I_{G_{\mathrm{Si}}} = \{|{\downarrow}\rangle\}\ \text{or}\ \{|{\uparrow}\rangle\},
\]

with the spin ground state along the field axis serving as the (trivially) invariant reference, exactly as the axial sublevels did for the NV center and trapped ion.

### 3.2 The donor two-spin singlet

Applying the singlet construction of candidate #3, Appendix B to the donor electron-nuclear pair (or, in the quantum-dot case, to an exchange-coupled two-electron double dot), the singlet state

\[
|S\rangle = \frac{1}{\sqrt2}\left(|\uparrow\downarrow\rangle - |\downarrow\uparrow\rangle\right)
\]

is again the full-\(SU(2)\)-invariant subspace, by the identical algebraic argument given in candidate #3, Appendix B and reproduced across candidates #4 and #5. The two-electron double-quantum-dot singlet, in particular, is the standard readout basis state for silicon spin qubits using Pauli-blockade detection, meaning that — unlike candidates #3–5, where the singlet had to be specifically prepared and verified as a demonstration — the silicon quantum-dot platform uses the framet-invariant singlet state as its **default operational readout reference** in ordinary device operation, giving this candidate the most immediately available experimental access to the full-group-invariance demonstration of any platform surveyed so far.

### 3.3 Isotopic purification as admissibility-group stabilization

In natural silicon, each \(^{29}\mathrm{Si}\) nuclear spin in the vicinity of the qubit contributes a small, randomly oriented local field via the Fermi contact and dipolar hyperfine interaction, so that the *effective* local frame direction experienced by the qubit fluctuates in time as the nuclear bath evolves:

\[
\hat z_{\mathrm{eff}}(t) = \frac{\mathbf B_0 + \delta\mathbf B_{\mathrm{bath}}(t)}{|\mathbf B_0+\delta\mathbf B_{\mathrm{bath}}(t)|}.
\]

This is, in the language of §7.4, a randomly time-varying admissibility group \(G(t)=U(1)_{\hat z_{\mathrm{eff}}(t)}\), rather than the fixed or deterministically-controlled group realized by every prior candidate in this survey. A state prepared as invariant under \(G(0)\) generically drifts out of invariance under \(G(t)\) as the bath evolves — this drift is, in fact, the microscopic origin of the qubit's \(T_2^*\) dephasing time. Isotopic purification to \(^{28}\mathrm{Si}\) removes essentially all of \(\delta\mathbf B_{\mathrm{bath}}(t)\), stabilizing \(G(t)\to G\) to a degree unmatched by any other analogous-tier candidate's ambient environment, and is the direct physical reason isotopically purified silicon donor and quantum-dot qubits hold some of the longest measured coherence times of any solid-state spin qubit platform.

### 3.4 Explicit dictionary

| Frame Theory (§7–8) | Silicon spin qubit realization |
|---|---|
| Local frame direction | Applied field axis \(\hat z\) |
| Admissibility group, single spin | \(U(1)_{\hat z}\subset SU(2)\) |
| Invariant subspace, single spin | Field-aligned ground sublevel |
| Invariant subspace, full-group case | Donor electron-nuclear singlet, or double-dot two-electron singlet |
| Admissibility-group stability | Isotopic purification (\(^{28}\mathrm{Si}\)) suppresses bath-induced \(G(t)\) fluctuation |
| Readout | Spin-to-charge conversion (Pauli blockade), using the singlet as default reference |

---

## 4. Proposed Experimental Program

### 4.1 Direct \(T_2^*\)-versus-isotopic-purity correspondence

1. Fabricate matched donor or quantum-dot devices in natural-abundance silicon and in isotopically enriched \(^{28}\mathrm{Si}\) (\(\gtrsim99.9\%\)).
2. Measure \(T_2^*\) via Ramsey interferometry on the single-spin axial-invariant sublevel structure of Section 3.1, in both material variants.
3. Independently characterize the residual \(^{29}\mathrm{Si}\) concentration via mass spectrometry or NMR of the bulk material.
4. Verify the predicted scaling of dephasing rate with residual nuclear spin density, giving a direct, quantitative experimental link between the admissibility-group stability argument of Section 3.3 and the standard, already-established coherence-time literature for this platform — this protocol requires no new fabrication or measurement technique beyond what is already standard practice in the field; its contribution is the reinterpretation of an established result in framet terms.

### 4.2 Singlet-invariance verification using the default readout channel

Because the double-dot singlet is already the standard readout reference state (Section 3.2), the field-rotation invariance protocol used in candidates #2 and #3 (rotate the applied field, verify the singlet's population and coherence are unaffected while a control triplet state's are) can be implemented on this platform using entirely standard Pauli-blockade charge-sensing hardware, without requiring any specialized tomography apparatus beyond what silicon spin-qubit labs already operate — the most experimentally low-overhead realization of the full-group-invariance protocol among candidates #3, #4, #5, and this paper.

---

## 5. Comparison Across the Analogous Tier

| Property | NV center (#1) | Trapped ion (#2) | NMR/ESR (#3) | Transmon (#4) | Polarization qubit (#5) | Cold-atom lattice (#6) | Silicon spin qubit (#8) |
|---|---|---|---|---|---|---|---|
| Frame origin | Fixed crystal axis | Controllable applied field | Controllable applied field | Synthetic microwave frame | Rotatable waveplate | Lattice + synthetic gauge field | Controllable applied field |
| Active spin-carrying material | Diamond (carbon) | Trapped atomic ion | Nuclear/electron spins in solution or solid | Superconducting circuit (Al/Nb on Si) | Photon | Neutral atoms | Silicon itself (donor or dot) |
| Default full-group-invariant readout state | Not default (requires special prep) | Not default | Not default (requires special prep) | Not default | Not default | Not default | **Default operational readout state** |
| Dominant coherence-limiting mechanism addressed structurally | N/A | N/A | N/A | N/A | N/A | N/A | Nuclear spin bath, removable by isotopic purification |
| Fabrication lineage to genuine-tier silicon candidates | None | None | None | Substrate only | None | None | **Direct — silicon is the active element** |

This candidate is unique in the analogous tier for using the full-group-invariant singlet as its everyday operational reference rather than as a specially prepared demonstration state, and for having a direct, quantitative, already-measured experimental link (Section 4.1) between a materials-engineering choice and the stability of the admissibility group itself.

---

## 6. Relation to the Spin-Doped Silicon Composite (Candidate #24)

This paper and the earlier treatment of the spin-doped silicon composite (SDSC, candidate #24) confront the same underlying silicon materials-science tradeoff — achievable dopant/impurity spin density versus achievable coherence or mechanical quality — from opposite design goals. The silicon spin qubit of this paper deliberately **minimizes** ambient nuclear spin density (via isotopic purification) to maximize coherence time, treating any stray spin density as a noise source to be engineered away. The SDSC deliberately **maximizes** electron spin density (via transition-metal or rare-earth doping) to source a macroscopic torsion field, treating the resulting mechanical/coherence degradation as an acceptable cost. The two papers are, in effect, studies of the two opposite ends of the same silicon spin-density design axis: this paper demonstrates that the low-spin-density end of that axis is not only feasible but already a mature, commercially relevant technology (isotopically purified silicon qubits are an active industrial quantum-computing development effort), which indirectly reinforces candidate #24's Section 3.2 finding that the *high*-spin-density end of the same axis remains comparatively immature and materials-limited — the two ends of the tradeoff are not symmetric in current technological readiness.

---

## 7. What This Device Does Not Measure

Consistent with candidates #1–7:

- **No coupling to \(e^a{}_\mu\) or \(\omega^{ab}{}_\mu\).** The donor or dot spin Hamiltonian is set by hyperfine coupling, exchange interaction, and applied fields; no term couples to the gravitational tetrad or spin connection.
- **No torsion sensitivity.** The spin densities involved (single donor or single/few confined electrons) are, if anything, engineered to be as isolated as possible from any macroscopic spin bath, the opposite of the torsion-sourcing requirement of §5.3 and candidate #24.
- **No frame-transport measurement.** The applied field \(\mathbf B_0\) is laboratory-controlled, not inertially transported, exactly as in candidates #2–3.
- **Isotopic purification stabilizes an already-non-gravitational admissibility group**; the "noise" being suppressed in Section 3.3 is ordinary nuclear hyperfine and dipolar coupling, with no relationship to any gravitational or torsion-field fluctuation.

---

## 8. Conclusion

The silicon spin qubit — whether realized as a phosphorus donor or a gate-defined quantum dot — closes the analogous tier's coverage of silicon as an active spin-carrying framet material, complementing candidate #4's passive-substrate role. Its single-spin structure reproduces the axial-invariance case of candidates #1–2; its donor or double-dot singlet reproduces the full-\(SU(2)\)-invariance case of candidates #3–5 using, uniquely in this survey, the platform's own default operational readout state; and its isotopic-purification engineering illustrates a structural feature not previously developed in this tier — that the admissibility group itself can be an experimentally stabilized quantity, with environmental noise reinterpreted as an unwanted, randomly time-varying perturbation of \(G\). Its relationship to the theoretic-tier spin-doped silicon composite (candidate #24) frames the two papers as complementary studies of opposite ends of the same silicon spin-density design tradeoff. As with every candidate in this tier, no coupling to the gravitational sector of the underlying theory is present or claimed.

---

## Appendix A: Symbol Glossary

| Symbol | Meaning |
|---|---|
| \(\hat z\) | applied-field quantization axis |
| \(^{28}\mathrm{Si}\), \(^{29}\mathrm{Si}\), \(^{30}\mathrm{Si}\) | silicon isotopes (nuclear spin \(0\), \(1/2\), \(0\) respectively) |
| \(T_2^*\) | inhomogeneous (free-induction) dephasing time |
| \(\delta\mathbf B_{\mathrm{bath}}(t)\) | fluctuating local field from residual nuclear spin bath |
| \(G(t)\) | time-dependent (bath-perturbed) admissibility group |

## Appendix B: Hyperfine Coupling and Bath-Induced Dephasing

The electron spin's coupling to a single nearby \(^{29}\mathrm{Si}\) nuclear spin is described by the contact hyperfine term \(A\,\hat S\cdot\hat I\), and the aggregate effect of \(N_{\mathrm{bath}}\) such nuclei within the electron wavefunction's extent produces a Gaussian-distributed effective field with variance scaling as the residual \(^{29}\mathrm{Si}\) concentration \(x_{29}\). The resulting Ramsey dephasing envelope,

\[
\langle S_z(t)\rangle \propto \exp\left[-(t/T_2^*)^2\right],\qquad T_2^*\propto x_{29}^{-1/2}\ \text{(scaling regime)},
\]

gives the quantitative prediction tested by the protocol of Section 4.1, and is the standard theoretical treatment already used in the isotopic-purification literature for this platform, reproduced here to make its connection to the admissibility-group-stability language of Section 3.3 explicit.

## Appendix C: Donor Two-Spin Singlet Invariance

As in candidates #3–5, the singlet invariance calculation for the donor electron-nuclear pair (or double-dot two-electron pair) proceeds identically to candidate #3, Appendix B, under the identification of the two coupled spin-1/2 systems with the donor electron and \(^{31}\mathrm{P}\) nucleus (or the two dot-confined electrons): the state is annihilated by all three generators of the collective \(SU(2)\) rotation, independent of the specific physical carriers of the two spins — the fourth independent confirmation, across candidates #3, #4, #5, and this paper, that the underlying representation theory is substrate-agnostic.

## Appendix D: Open Questions for Future Silicon Spin-Qubit Framet Work

- Can the admissibility-group-stability framing of Section 3.3 be extended to a quantitative figure of merit — an effective "admissibility coherence time" — that could be compared directly across all analogous-tier candidates in this survey, given that each platform's local frame is subject to a different dominant noise mechanism (crystal strain for #1, field-coil noise for #2, bath fluctuations for this paper, etc.)?
- Does the double-dot singlet's role as the *default* readout state (Section 3.2) suggest that other candidates in this survey could be redesigned so that their full-group-invariant state becomes the default operational reference rather than a specially prepared demonstration state, and would this offer any practical advantage for a future combined multi-platform framet calibration standard?
- What is the quantitative relationship, if any, between the achievable isotopic purity discussed here and the achievable dopant concentration discussed for the spin-doped silicon composite (candidate #24) — i.e., does the same crystal-growth and purification technology base set a joint constraint on how close a single silicon material system could come to simultaneously supporting both a low-noise qubit region and a high-spin-density torsion-source region on one wafer?

---

## Selected References

1. J. J. Pla et al., "A single-atom electron spin qubit in silicon," *Nature*.
2. M. Veldhorst et al., "An addressable quantum dot qubit with fault-tolerant control-fidelity," *Nature Nanotechnology*.
3. K. M. Itoh, H. Watanabe, "Isotope engineering of silicon and diamond for quantum computing and sensing applications," *MRS Communications*.
4. A. M. Tyryshkin et al., "Electron spin coherence exceeding seconds in high-purity silicon," *Nature Materials*.
5. Companion foundational work: *Frame Theory: A Local-Frame Formulation of Gravitation and the Admissibility Structure of General Relativity*, §7–8.
6. Companion white papers: *The NV-Center Spin Qubit Array* (candidate #1); *The Trapped-Ion Qubit* (candidate #2); *The NMR/ESR Ensemble* (candidate #3); *The Superconducting Transmon Qubit* (candidate #4); *The Optical Polarization Qubit* (candidate #5); *The Cold-Atom Optical-Lattice Framet* (candidate #6); *The Distributed Spin-Qubit Magnetometer Network* (candidate #7); *The Spin-Doped Silicon Composite* (candidate #24).
7. Companion survey: terrestrial framet candidate list, item #8.
