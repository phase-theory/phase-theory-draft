# The Cold-Atom Optical-Lattice Framet: A Spatially Extended Local Frame from Spinor Bose-Einstein Condensates

**Preprint — August 2, 2026**
**M. Brownlee — Dust LLC**

**Keywords:** framet, spinor Bose-Einstein condensate, optical lattice, angular momentum states, synthetic gauge field, admissibility group, invariant subspace, spatially extended frame

---

## Abstract

The five analogous-tier candidates surveyed so far (NV center, trapped ion, NMR/ESR ensemble, transmon, polarization qubit) each realize the admissibility-group formalism of *Frame Theory* §7–8 at a single point, or at most a small discrete set of points (candidate #1's four crystallographic orientations, candidate #4's coupled-qubit lattice). None realizes a continuous, spatially extended field of local frames analogous to a tetrad field \(e^a{}_\mu(x)\) varying smoothly over an extended region — a gap flagged explicitly as an open question in candidates #1 (Appendix D), #4 (Appendix D), and #5 (Section 4.2, via the still-unbuilt dynamically reconfigurable metasurface). This paper develops the spinor Bose-Einstein condensate (BEC) in an optical lattice as the analogous-tier candidate that closes this gap directly: the lattice's spatially periodic potential defines a local frame at every lattice site simultaneously, the condensate's internal hyperfine spin manifold carries an \(SU(2)\) (or higher-spin) representation at each site, and — via established synthetic gauge field techniques — an engineered, spatially varying, genuinely non-abelian connection can be imposed across the lattice, giving this platform access to a laboratory analog of spatial curvature \(R^{ab}{}_{\mu\nu}\neq0\), a capability no other analogous-tier candidate in this survey has yet reached. As with all analogous-tier candidates, we are explicit throughout that no coupling to the physical gravitational tetrad or spin connection is present or claimed — the curvature realized here lives in a synthetic gauge-field sense, in the condensate's internal and lattice-momentum space, not in physical spacetime.

---

## 1. Introduction

### 1.1 The missing spatial extension

Reviewing the analogous tier to this point: candidate #1 (NV center) proposed a multi-orientation array approximating a spatially varying frame only in the weak sense of discrete crystallographic sectors; candidate #4 (transmon) proposed a coupled-qubit lattice as an open question, without a worked construction; candidate #5 (polarization qubit) connected explicitly to the Pancharatnam-Berry metasurface (candidate #11) as its natural spatial extension, but that metasurface is a *fixed*, fabrication-defined pattern, not a dynamically reconfigurable or internally dynamical field. None of the five prior candidates realizes a system in which the local frame varies continuously over space **and** the connection relating neighboring frames is itself a dynamical, measurable quantity with nontrivial curvature — the two properties that, together, would make a laboratory system structurally analogous to a genuine tetrad-and-connection field rather than a single point or a static fabricated pattern.

Ultracold atoms in optical lattices, prepared as spinor condensates and subjected to engineered synthetic gauge fields, provide exactly this. This is an active, well-established area of atomic physics — synthetic non-abelian gauge fields for neutral atoms have been realized experimentally using Raman-assisted tunneling and related laser-coupling schemes — and this paper's contribution is to make explicit the correspondence between that established experimental toolkit and the framet formalism of §2 and §7–8.

### 1.2 Scope statement

As with candidates #1–5, this paper treats the cold-atom lattice framet strictly as a representation-theoretic and synthetic-connection demonstration platform. No coupling to the physical gravitational tetrad \(e^a{}_\mu\) or spin connection \(\omega^{ab}{}_\mu\) is present or claimed; the "curvature" realized in Section 4 is a curvature of a synthetic (laser-engineered) gauge connection in a condensed-matter system, not a physical spacetime curvature. Full discussion in Section 7.

---

## 2. Physical System

### 2.1 The optical lattice as a spatially extended frame

An optical lattice is formed by interfering laser beams to create a spatially periodic potential, in which ultracold atoms (typically alkali species such as \(^{87}\mathrm{Rb}\), \(^{40}\mathrm{K}\), or \(^{6}\mathrm{Li}\), cooled to quantum degeneracy) are trapped at the potential minima. Each lattice site \(\mathbf x_i\) hosts a local trapping geometry set by the interfering laser beam directions and polarizations — directly analogous to the local frame direction of every prior candidate in this survey, but now indexed by a discrete spatial coordinate \(i\) covering, in a typical experiment, \(10^2\)–\(10^5\) sites, giving a genuinely extended (if discretized) analog of the base manifold \(M\) over which the frame bundle of §2.1 is defined.

### 2.2 Spinor condensates and internal representation

For atoms with nonzero total spin \(F\) (e.g. the \(F=1\) or \(F=2\) hyperfine ground-state manifolds of \(^{87}\mathrm{Rb}\)), the condensate wavefunction at each site carries an internal spinor degree of freedom transforming under \(SU(2)\) exactly as in candidates #1–5, but now with a *field* of such spinors, one per lattice site, rather than a single spin. This gives the platform access to internal representation structure identical to the NV center's spin-1 case (\(F=1\)) at every site simultaneously, spatially extended across the lattice.

### 2.3 Synthetic gauge fields

Using Raman-assisted tunneling — in which laser-induced two-photon transitions couple internal spin states while imparting a controlled momentum kick, engineered to depend on the tunneling direction and the atom's internal state — experimentalists can imprint a synthetic vector potential, and, with appropriately chosen multi-level coupling schemes, a genuinely non-abelian synthetic gauge field, onto the atoms' center-of-mass motion through the lattice. The atom accumulates a Peierls-type phase (abelian case) or matrix-valued holonomy (non-abelian case) upon tunneling between sites, exactly as a charged particle would in a real magnetic vector potential, or as a spin-carrying particle would under a real non-abelian connection — the synthetic-gauge-field literature explicitly uses this correspondence, independent of any framet framing, and this paper simply identifies it with the connection \(\omega^{ab}{}_\mu\) structure of §2.4 in the sense made precise in Section 3.

---

## 3. Correspondence to the Framet Formalism

### 3.1 The lattice as a discretized frame bundle

Following §2.1's description of the frame bundle \(P\to M\), the optical lattice realizes a discretized analog: a base "manifold" of lattice sites \(\{\mathbf x_i\}\), each carrying a local internal Hilbert space (the on-site spinor) playing the role of the fiber. The admissibility group at each site is, as in candidates #1–5,

\[
G_{\mathrm{site}} = SU(2),
\]

realized through the same internal hyperfine structure used throughout the analogous tier, but now the *connection* relating the fiber at site \(i\) to the fiber at a neighboring site \(j\) is a genuinely new structural element not present in any single-point candidate: the synthetic gauge field itself.

### 3.2 Synthetic connection and its holonomy

The Raman-assisted tunneling amplitude between neighboring sites \(i,j\) can be written as a matrix-valued hopping element

\[
t_{ij} = t_0\,U_{ij},
\qquad U_{ij}\in SU(2)\ \text{(non-abelian case)},
\]

directly analogous to the discretized (lattice-gauge-theory) form of a Wilson line for the connection \(\omega^{ab}{}_\mu\) of §2.4,

\[
U_{ij} \;\longleftrightarrow\; \mathcal P\exp\left(\int_i^j\omega\right).
\]

The holonomy around a closed plaquette (a minimal closed loop of four lattice sites) is then

\[
\mathcal H[\Box] = U_{i\to j}U_{j\to k}U_{k\to l}U_{l\to i},
\]

directly realizing the holonomy construction of §7.3 in its *spatially extended, plaquette-based* form — as opposed to the single-loop-in-time holonomy realized by the trapped ion (candidate #2, abelian) and the transmon (candidate #4, non-abelian, but in a control-parameter space rather than physical space).

### 3.3 Synthetic curvature

Crucially, because the lattice provides many plaquettes rather than a single loop, this platform allows the holonomy to be measured as a *function of position* across the lattice, and — if the applied synthetic gauge field is engineered to vary spatially — the plaquette holonomy itself can vary from plaquette to plaquette, giving a direct measurement of nonzero synthetic curvature,

\[
R_{\mathrm{synthetic}}(\mathbf x_i) \;\neq\; 0,
\]

realized as the non-triviality of \(\mathcal H[\Box_i]\) as \(i\) ranges over the lattice. This is the single capability that most clearly distinguishes this candidate from #1–5: every prior analogous-tier candidate could realize at most a single holonomy value (one loop, one measurement), whereas the optical lattice realizes a *field* of holonomies, i.e., a discretized curvature field, directly analogous in structure (though, as always in this tier, not in physical origin) to \(R^{ab}{}_{\mu\nu}(x)\) as a genuine field over the base manifold in §2.4.

### 3.4 Explicit dictionary

| Frame Theory (§2, §7–8) | Cold-atom lattice realization |
|---|---|
| Base manifold \(M\) | Discretized lattice of trap sites \(\{\mathbf x_i\}\) |
| Frame bundle \(P\to M\) | Lattice sites, each carrying an internal spinor fiber |
| Admissibility group \(G\) at a point | \(SU(2)\), hyperfine spin manifold |
| Connection \(\omega^{ab}{}_\mu\) | Synthetic gauge field from Raman-assisted tunneling |
| Holonomy \(\mathcal H[\gamma]\) | Plaquette Wilson loop \(\mathcal H[\Box]\) |
| Curvature \(R^{ab}{}_{\mu\nu}\) | Synthetic curvature, spatially varying plaquette holonomy |
| Invariant subspace \(\mathcal I_G\) | On-site \(m_F=0\)-type state, or engineered dark-state manifold per site |

---

## 4. Proposed Experimental Program

### 4.1 Direct plaquette holonomy measurement

1. Load a spinor BEC into a two-dimensional optical lattice.
2. Apply Raman-assisted tunneling with a spatially uniform synthetic gauge field, engineered to realize a known abelian (uniform synthetic magnetic flux per plaquette) or non-abelian gauge structure.
3. Use interferometric or Bloch-oscillation-based techniques (already established in the synthetic-gauge-field literature for measuring Chern numbers and Berry curvature in cold-atom systems) to extract the plaquette holonomy \(\mathcal H[\Box]\) directly.
4. Compare the measured holonomy to the value predicted from the applied laser coupling parameters, validating the identification of Section 3.2.

### 4.2 Spatially varying curvature

Extend the protocol of Section 4.1 by engineering a spatially inhomogeneous synthetic gauge field (e.g., via a spatially varying Raman beam intensity profile) and mapping the resulting plaquette-to-plaquette variation in \(\mathcal H[\Box_i]\) across the lattice, directly realizing the spatially varying curvature field discussed in Section 3.3 — the first candidate in this survey capable of this measurement in physical (rather than control-parameter) space.

### 4.3 On-site invariant-subspace verification

As a consistency check reproducing candidates #1–5's single-point results, verify that the on-site internal state, prepared in an axially invariant sublevel (e.g. \(m_F=0\) of the local hyperfine manifold), remains invariant under a controlled local rotation of the on-site quantization axis (realized via a site-addressed local magnetic or optical field), independent of the synthetic gauge field connecting that site to its neighbors — demonstrating that the single-point invariance results of candidates #1–5 and the multi-point connection structure of Sections 4.1–4.2 are logically independent features of the same platform, exactly as §2's frame bundle and §7's admissibility structure are independent (though related) structural layers in the foundational theory.

---

## 5. Comparison Across the Analogous Tier

| Property | NV center (#1) | Trapped ion (#2) | NMR/ESR (#3) | Transmon (#4) | Polarization qubit (#5) | Cold-atom lattice (#6) |
|---|---|---|---|---|---|---|
| Number of simultaneous local frames | 1 (or 4 discrete orientations) | 1 (or few, per ion) | Ensemble (\(\sim10^{15}\)+, unaddressed) | 1 (or few, coupled) | 1 (or metasurface array, #11, fixed pattern) | \(10^2\)–\(10^5\), individually addressable |
| Connection between neighboring frames | Not defined | Not defined | Not defined | Engineered (open question, Appendix D) | Not defined (static metasurface only) | Synthetic gauge field, engineered and measurable |
| Curvature measurement | Not accessible | Not accessible | Not accessible | Not accessible (single loop only) | Not accessible (static pattern only) | Directly accessible, spatially resolved |
| Holonomy type | N/A | Abelian | N/A | Non-abelian (control-parameter space) | Abelian (historically first) | Abelian or non-abelian, spatially varying, in physical space |

This candidate is the clearest structural upgrade over #1–5 with respect to §2's frame-bundle-over-a-manifold picture specifically, at some cost in the single-site cleanliness that made candidates #1 and #5 the most experimentally simple platforms in the survey.

---

## 6. What This Device Does Not Measure

Consistent with candidates #1–5:

- **No coupling to \(e^a{}_\mu\) or \(\omega^{ab}{}_\mu\).** The synthetic gauge field of Section 2.3 is generated entirely by laser light coupling to atomic internal states and center-of-mass motion; it has no physical relationship to the gravitational tetrad or spin connection, despite the structural correspondence developed in Section 3.
- **No torsion sensitivity.** As with candidates #1–5, the spin densities involved are far too small, and in any case not coupled through the correct interaction channel, to relate to the macroscopic torsion-sourcing mechanism of §5.3.
- **No physical frame-transport measurement.** The lattice sites and synthetic gauge field are laboratory-defined and static (or laser-controlled) in the lab frame; they do not track inertial or gravitational motion, unlike the genuine-tier gyroscope and atom-chip candidates elsewhere in this survey — indeed, cold-atom Sagnac interferometry (a genuine-tier candidate, #17 in the broader survey) uses a structurally different measurement principle (matter-wave interference along a physical path) from the synthetic-gauge-field construction used here, and the two should not be conflated despite both using cold atoms.
- **"Curvature" here is synthetic-gauge-field curvature**, a real and rigorously measurable quantity in its own right within condensed-matter and atomic physics, but not a measurement of spacetime curvature \(R^{ab}{}_{\mu\nu}[g]\) in any physical sense; the correspondence claimed in Section 3.3 is exclusively at the level of mathematical structure (both are curvatures of a connection over a base manifold), not physical origin.

---

## 7. Discussion: The First Spatially Extended Analogous Candidate

The central contribution of this paper is structural rather than experimental novelty — synthetic gauge fields in optical lattices are an established, mature area of atomic physics, and this paper's role is to make explicit what has, to our knowledge, not been stated before in this form: that the plaquette-holonomy construction already used routinely in that field is exactly the discretized Wilson-line/curvature construction of §7.3 and §2.4, realized over a genuine (if discretized and synthetic) base manifold rather than a single point or a fixed fabrication pattern. This closes the "spatially extended frame" gap left open by candidates #1, #4, and #5, and gives the analogous tier its first platform on which the full frame-bundle-plus-connection-plus-curvature picture of §2 can be demonstrated as an integrated whole, rather than piecemeal across separate single-site and single-loop measurements on different platforms.

---

## 8. Conclusion

The cold-atom optical-lattice framet, realized through spinor Bose-Einstein condensates and synthetic non-abelian gauge fields, closes the principal structural gap in the analogous tier of this survey: a genuinely spatially extended local frame, a measurable connection between neighboring frames, and — uniquely among candidates #1–6 — a directly measurable, spatially resolved synthetic curvature field. Its on-site physics reproduces the single-point admissibility and invariant-subspace results of candidates #1–5, while its lattice structure realizes the frame-bundle-over-a-manifold picture of §2.1 as an integrated experimental system rather than a discrete or static approximation. As with every candidate in this tier, the correspondence is exclusively structural: no coupling to the physical gravitational tetrad or spin connection is present or claimed, and the curvature measured is that of a laser-engineered synthetic gauge field, not spacetime itself.

---

## Appendix A: Symbol Glossary

| Symbol | Meaning |
|---|---|
| \(\mathbf x_i\) | position of lattice site \(i\) |
| \(F\) | atomic total hyperfine spin quantum number |
| \(t_{ij}\) | tunneling amplitude between sites \(i,j\) |
| \(U_{ij}\) | matrix-valued synthetic connection element (discretized Wilson line) |
| \(\mathcal H[\Box]\) | plaquette holonomy (Wilson loop) |
| \(R_{\mathrm{synthetic}}(\mathbf x_i)\) | synthetic curvature at site \(i\) |

## Appendix B: Peierls Substitution and the Abelian Case

For the simpler abelian synthetic gauge field case (uniform synthetic magnetic flux per plaquette, realized via lattice shaking or simple Raman coupling without internal-state mixing), the tunneling amplitude acquires a Peierls phase,

\[
t_{ij} = t_0\,e^{i\phi_{ij}},
\]

and the plaquette holonomy reduces to the sum of phases around the loop,

\[
\mathcal H[\Box] = \exp\left(i\sum_{\langle ij\rangle\in\Box}\phi_{ij}\right) = e^{i\Phi},
\]

with \(\Phi\) the total synthetic flux through the plaquette — the discretized abelian special case of the non-abelian construction in Section 3.2, and the most experimentally mature realization of the holonomy measurement proposed in Section 4.1.

## Appendix C: Relation to Topological Band Structure

The synthetic curvature field of Section 3.3, integrated over the full lattice (or Brillouin zone, in the itinerant rather than localized picture), gives the Chern number characterizing the topological band structure of the lattice — a quantity already routinely measured in cold-atom synthetic-gauge-field experiments via center-of-mass drift measurements and related techniques. This provides an independent, already-established experimental route to the curvature-field claim of Section 3.3, external to the framet-specific protocol proposed in Section 4.2.

## Appendix D: Open Questions for Future Cold-Atom Framet Work

- Can the on-site invariant-subspace verification of Section 4.3 be combined with the plaquette-holonomy measurement of Section 4.1 into a single protocol demonstrating that admissibility-invariant states at different sites remain invariant under parallel transport around a closed loop connecting them — the cold-atom analog of the combined invariance-plus-transport question raised as an open question in candidate #4, Appendix D?
- Does the three-dimensional extension of this lattice architecture (rather than the two-dimensional case emphasized in Section 4) permit a closer structural approximation to the full \(\mathrm{Spin}(1,3)\) connection, given that a 2D lattice's plaquette structure naturally accesses fewer independent holonomy loops than a 3D lattice would?
- Is there a meaningful way to engineer a synthetic gauge field whose curvature satisfies a discretized analog of the Bianchi identity \(DR^{ab}=0\) of §2.6 as an emergent rather than imposed property, and would violating it (by engineering an inconsistent gauge field) produce a measurable, physically interesting inconsistency in the lattice's band structure?

---

## Selected References

1. Y.-J. Lin, R. L. Compton, K. Jiménez-García, J. V. Porto, I. B. Spielman, "Synthetic magnetic fields for ultracold neutral atoms," *Nature*.
2. N. Goldman, G. Juzeliūnas, P. Öhberg, I. B. Spielman, "Light-induced gauge fields for ultracold atoms," *Reports on Progress in Physics*.
3. M. Aidelsburger et al., "Measuring the Chern number of Hofstadter bands with ultracold bosonic atoms," *Nature Physics*.
4. D. Jaksch, P. Zoller, "Creation of effective magnetic fields in optical lattices: the Hofstadter butterfly for cold neutral atoms," *New Journal of Physics*.
5. Companion foundational work: *Frame Theory: A Local-Frame Formulation of Gravitation and the Admissibility Structure of General Relativity*, §2, §7–8.
6. Companion white papers: *The NV-Center Spin Qubit Array* (candidate #1); *The Trapped-Ion Qubit* (candidate #2); *The NMR/ESR Ensemble* (candidate #3); *The Superconducting Transmon Qubit* (candidate #4); *The Optical Polarization Qubit* (candidate #5).
7. Companion survey: terrestrial framet candidate list, item #6.
