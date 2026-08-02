# The Spin-Doped Silicon Composite: A Monolithic Source-Readout Framet for Spin-Torsion Coupling Detection

**Preprint — August 2, 2026**
**M. Brownlee — Dust LLC**

**Keywords:** framet, spin-torsion coupling, Einstein–Cartan theory, dilute magnetic semiconductor, MEMS torsion balance, monolithic integration, Frame Theory, axial current, torsion balance, silicon photonics readout

---

## Abstract

The spin-polarized torsion-balance experiment is the only class of terrestrial apparatus that directly probes the connection-sourcing field equation of Frame Theory,

\[
\epsilon_{abcd}\,e^c\wedge T^d = \kappa\,\sigma_{ab},
\]

rather than merely representing the admissibility group \(SU(2)\subset\mathrm{Spin}(1,3)\) or tracking local frame transport kinematically. Existing realizations of this experiment (Eöt-Wash and successors) separate the two functional roles the apparatus requires — a macroscopically spin-polarized source mass, and a high-\(Q\) mechanical suspension with sensitive angular readout — onto physically distinct components, typically a rare-earth or transition-metal ferrimagnet source mounted on a fused-silica or beryllium-copper torsion fiber. This paper proposes and analyzes the **spin-doped silicon composite (SDSC)**: a single monolithic silicon-based device in which the spin source and the MEMS suspension/readout structure are fabricated as one continuous crystal, using dilute magnetic-semiconductor doping (transition-metal or rare-earth substitutional/interstitial doping of a silicon or silicon-germanium lattice) to endow the mechanical element itself with a controllable net electron spin polarization.

We derive the expected torsion-mediated torque on such a device from the axial-current torsion relation of Frame Theory §5.3 and Appendix D, develop a materials-science feasibility analysis of candidate dopant systems (Mn, Fe, Co, Gd, Eu in Si and Si\(_{1-x}\)Ge\(_x\)), propose a differential dual-oscillator MEMS architecture that cancels common-mode noise while isolating the spin-density-dependent torque, and construct a sensitivity budget comparing the SDSC concept against existing macroscopic torsion-balance bounds. We find that no dopant system presently combines sufficient room-temperature net spin polarization, chemical stability in a fabricable silicon host, and compatibility with standard MEMS release processes; the SDSC is therefore classified as a **theoretic framet candidate** — a well-posed, falsifiable design whose realization is blocked by materials feasibility rather than by any flaw in the underlying measurement principle. We identify the specific materials-science thresholds that would need to be crossed for a working device, and outline near-term partial realizations (hybrid bonded structures, cryogenic operation) that relax those thresholds at the cost of full monolithicity.

---

## 1. Introduction

### 1.1 Why a monolithic device

Section 5.3 of *Frame Theory* establishes that spinorial matter sources an algebraic torsion field through

\[
T_{abc} = -\frac{\kappa}{4}\,\epsilon_{abcd}\,j_5^d,
\]

where \(j_5^a = \bar\psi\gamma^a\gamma^5\psi\) is the axial current. Because the torsion equation contains no derivatives of torsion, the field does not propagate — it exists only in the immediate presence of spin density, and its effect on a nearby test system falls off with the geometric separation between source and detector, not merely with signal-to-noise considerations. Every existing terrestrial spin-torsion search therefore performs a delicate design tradeoff: the spin-polarized source must sit as close as possible to the mechanical detector to maximize coupling, while the detector must be built from materials with vanishingly small intrinsic spin density and minimal magnetic susceptibility, so that its own suspension does not source a torsion field or respond magnetically to the source's stray dipole field. This has historically meant two different materials for two different jobs: a ferrimagnetic or paramagnetic source (often a Dy\(_6\)Fe\(_{23}\)-type or GdIG-type compound) glued or clamped to a fused-silica, tungsten, or beryllium-copper suspension chosen for mechanical \(Q\) and magnetic inertness, with the spin source and the mechanical element as two bonded but materially distinct bodies.

A monolithic device collapses this separation. If a single crystal can be doped to carry a controllable net electron spin density *and* micromachined into a high-\(Q\) torsional MEMS resonator, the spin source and the detector become the same body: the torsion field sourced by the doped lattice acts on the very structure whose deflection is being read out, eliminating the bonded-interface loss channel, geometric standoff distance, and differential thermal expansion that dominate the systematic error budget of bonded designs. This is the motivating idea behind the SDSC.

### 1.2 Relation to prior candidates

This design was flagged as item #24 in a survey of terrestrial framet candidates, explicitly as the "unification" of two separately-limited silicon designs:

- **Silicon MEMS torsion-balance suspension/readout** — silicon MEMS provides excellent mechanical \(Q\) and lithographic precision, but undoped silicon's room-temperature intrinsic electron spin density is far too low to serve as a usable spin source.
- **Spin-polarized torsion-balance experiment (Eöt-Wash-type)** — the established experimental class that actually probes \(\sigma_{ab}\to T^a\), but built from non-silicon, non-MEMS materials, so it cannot inherit silicon fabrication's precision, reproducibility, or scalability.

The SDSC asks whether a doped-silicon host can be engineered to simultaneously satisfy both roles. This paper is the first attempt at a complete feasibility treatment of that question.

### 1.3 Structure of this paper

Section 2 rederives the expected torque signal from Frame Theory's torsion-source relation, specialized to a doped-silicon slab geometry. Section 3 surveys candidate dopant systems against the spin-density and stability thresholds the signal derivation requires. Section 4 proposes a differential dual-oscillator device architecture. Section 5 constructs a sensitivity and systematic-error budget. Section 6 outlines a fabrication pathway. Section 7 states the paper's central negative result and the specific thresholds a future materials advance would need to clear. Section 8 concludes.

---

## 2. Torque Signal from a Doped-Silicon Source

### 2.1 Axial current of a doped lattice

For a crystal with substitutional or interstitial paramagnetic dopants of number density \(n_s\) and mean electron spin polarization \(\langle S_z\rangle\) along an applied bias field \(\hat z\), the macroscopic axial current reduces, in the non-relativistic limit appropriate to a solid-state host, to

\[
j_5^a \;\approx\; 2\,n_s\,\langle S^a\rangle,
\]

where \(\langle S^a\rangle\) is the expectation value of the electron spin operator per dopant, summed over unpaired electrons per site and averaged over the sample. This is the same substitution used to connect the Dirac-field axial current of §5.3 to a laboratory spin-polarized sample in ordinary spin-torsion experiments; nothing about the silicon host changes the form of the relation, only the achievable value of \(n_s\langle S^a\rangle\).

### 2.2 Torque on a co-located test structure

Following the torsion-mediated interaction Lagrangian of §5.3,

\[
\mathcal{L}_{\mathrm{int}} \sim \kappa\left(\bar\psi\gamma^a\gamma^5\psi\right)\left(\bar\psi\gamma_a\gamma^5\psi\right),
\]

the torque exerted on a test spin population \(j_5'^a\) separated from a source population \(j_5^a\) by a displacement \(\mathbf r\) takes the short-range, non-propagating form characteristic of algebraic (non-dynamical) torsion:

\[
\boldsymbol\tau \;\sim\; \kappa\, V_{\mathrm{overlap}}\,\left(n_s\langle\mathbf S\rangle\right)\times\left(n_s'\langle\mathbf S'\rangle\right),
\]

where \(V_{\mathrm{overlap}}\) is the effective interaction volume set by the coupling's spatial falloff. Because the interaction is contact-like rather than inverse-square, the SDSC's central design advantage — reducing source-to-detector separation from millimeters (bonded designs) to zero (monolithic doping across the resonator body) — enters the signal multiplicatively through \(V_{\mathrm{overlap}}\), not merely as a linear standoff-distance correction. This is the quantitative version of the qualitative claim in §1.1.

### 2.3 Comparison quantity: effective spin density

For comparison across dopant systems, define the effective areal spin density of a doped resonator arm as

\[
\Sigma_s \;=\; n_s\langle S_z\rangle\, t,
\]

with \(t\) the doped-layer thickness. This is the single figure of merit used in Section 3 to rank candidate dopant systems, since the predicted torque scales linearly with \(\Sigma_s\) for a fixed device geometry and readout sensitivity.

---

## 3. Dopant System Survey

The central engineering requirement is a dopant species that (a) substitutes into or occupies interstitial sites in a silicon or Si\(_{1-x}\)Ge\(_x\) lattice at concentrations high enough to yield a usable \(\Sigma_s\), (b) retains a net, field-alignable electron spin at or near room temperature rather than being fully quenched by crystal-field splitting or forming a antiferromagnetically-coupled compensated state, and (c) is chemically and thermally compatible with standard MEMS release and metallization steps (typically involving HF vapor release, elevated-temperature oxide growth, and RIE/DRIE etching).

| Candidate dopant | Host | Nominal spin state | Known limitation |
|---|---|---|---|
| Mn (substitutional) | Si, Si\(_{1-x}\)Ge\(_x\) | high-spin \(d^5\), \(S=5/2\) if isolated | forms MnSi and Mn\(_4\)Si\(_7\) secondary phases at doping levels needed for usable \(n_s\); isolated substitutional Mn in Si is a deep acceptor with strong spin-lattice coupling that suppresses net polarization above cryogenic temperatures |
| Fe (interstitial) | Si | \(S=2\) high-spin, if interstitial and isolated | fast diffusion and precipitation into FeSi\(_2\) clusters at device-relevant thermal budgets; interstitial Fe is not thermally stable through standard oxide/anneal steps |
| Co | Si | variable, often low-spin in Si crystal field | crystal-field quenching dominates; achievable net polarization is low even at cryogenic temperature |
| Gd (dilute rare-earth) | Si, SiGe | \(4f^7\), \(S=7/2\), shielded by outer \(5s^25p^6\) shells | very low solid solubility in Si; requires ion implantation with post-implant damage that degrades mechanical \(Q\) |
| Eu | Si, SiGe | \(4f^7\), \(S=7/2\) | same solubility/implant-damage tradeoff as Gd; some evidence of favorable magnetic ordering temperatures in EuO-type compounds, but not in a silicon host at usable concentration |
| Mn-doped GaAs-on-Si (heteroepitaxial) | Si substrate, GaAs:Mn active layer | ferromagnetic below \(T_c\sim 200\,\mathrm{K}\) in optimized films | requires cryogenic or near-cryogenic operation; heteroepitaxial layer is not itself the mechanical resonator body, reintroducing a bonded/grown interface and partially defeating the monolithicity goal |

No entry in this table simultaneously satisfies all three requirements at room temperature. The strongest partial candidates — substitutional Mn and heteroepitaxial Mn:GaAs-on-Si — both require either cryogenic operation or accept a residual layer interface, which is discussed further in Section 7.

### 3.1 Why rare-earth shielding does not solve the problem

The rare-earth ions (Gd\(^{3+}\), Eu\(^{2+}))\) are attractive in principle because their \(4f\) magnetic moments are shielded by filled outer shells and are therefore far less sensitive to the local crystal field than transition-metal \(3d\) electrons — this is precisely why they are used in the ferrimagnetic source masses of conventional (non-silicon) torsion-balance experiments. The obstacle in a silicon host is not crystal-field quenching but solid solubility: rare-earth atoms are large relative to the silicon lattice constant and have very low equilibrium solubility in crystalline Si, so achieving the doping density required for a usable \(\Sigma_s\) forces either non-equilibrium introduction (ion implantation) or precipitation into silicide clusters, both of which degrade the single-crystal mechanical properties the MEMS resonator needs for high \(Q\).

### 3.2 The mechanical-magnetic tradeoff

Every dopant strategy in Table 1 trades against resonator \(Q\) in the same direction: higher dopant concentration increases \(\Sigma_s\) but also increases lattice disorder, secondary-phase precipitation, and dopant-induced internal friction, all of which reduce mechanical \(Q\) and raise the thermal-noise floor of the angular readout (Section 5). This is the quantitative core of the paper's negative feasibility finding — the two functions the monolithic device is asked to perform pull the same material parameter (dopant concentration) in opposite directions.

---

## 4. Proposed Device Architecture

Notwithstanding the materials-feasibility finding of Section 3, we specify a complete device architecture, both to make the sensitivity budget concrete and because the design is directly reusable once (or if) a suitable dopant system is identified.

### 4.1 Differential dual-oscillator layout

The device consists of two nominally identical silicon torsional MEMS resonators fabricated side by side on the same die:

- **Active arm:** doped with the chosen spin-source species at the maximum concentration consistent with acceptable \(Q\) degradation, biased by an on-chip integrated coil or permanent-magnet film to align \(\langle S_z\rangle\).
- **Reference arm:** identical geometry and process flow, but either undoped or doped with an isotope/species chosen to have equal mass and elastic loading but no net spin (e.g., isotopically-selected, non-magnetic dopant of matched atomic mass).

Both arms are driven and read out capacitively or optically in a differential configuration. Common-mode effects — thermal drift, seismic and acoustic coupling, stray electric fields, gravitational gradients from the building and local environment — cancel to first order; a differential deflection synchronous with periodic reversal of the active arm's spin-bias field is the target signal, in direct analogy to the modulation-and-lock-in technique used in existing spin-coupling searches.

### 4.2 Readout

Silicon photonic integrated readout (per the Sagnac/ring-resonator gyroscope work surveyed as candidates #14–15 in the broader framet list) is proposed over capacitive readout for this application, because the torque signal predicted in Section 2 is expected to be extremely small and benefits from the lower noise floor achievable with optical interferometric angle sensing at the required bandwidth. A Michelson- or Fabry–Pérot-based free-space or on-chip interferometer referencing a mirror pad on the torsional arm is the baseline readout concept.

### 4.3 Bias-field reversal and lock-in

Periodic reversal of the spin-alignment bias field (at a frequency chosen away from mechanical resonances and known vibrational lines of the supporting structure) allows lock-in extraction of the spin-torsion signal from the much larger static and low-frequency background, following the standard technique of the Eöt-Wash-type experiments this design is meant to miniaturize and integrate.

---

## 5. Sensitivity Budget

### 5.1 Thermal noise floor

The angular thermal noise floor of a torsional MEMS resonator of moment of inertia \(I\), resonant frequency \(\omega_0\), and quality factor \(Q\) at temperature \(T\) is

\[
\sqrt{S_{\theta\theta}(\omega_0)} \;=\; \sqrt{\frac{4k_BT}{I\omega_0 Q}}.
\]

Typical silicon MEMS torsional resonators achieve \(Q\sim 10^4\text{–}10^6\) in vacuum packaging at room temperature, and higher at cryogenic temperature. Any dopant-induced \(Q\) degradation (Section 3.2) directly raises this noise floor, which is why the materials tradeoff identified above is not a secondary concern but the primary obstacle to a competitive sensitivity.

### 5.2 Comparison to existing bounds

Existing macroscopic spin-torsion searches using bonded ferrimagnetic sources on fused-silica or tungsten suspensions have placed the tightest existing terrestrial bounds on axial-vector spin-spin couplings of the type predicted in §5.3 of *Frame Theory*. A monolithic SDSC device, even with an optimistic \(\Sigma_s\) from the most favorable dopant candidate in Table 1, is not expected to surpass these bounds unless the mechanical-magnetic tradeoff of Section 3.2 can be resolved without an order-of-magnitude \(Q\) penalty — because the interaction-volume advantage described in Section 2.2 must overcome a comparably large loss in achievable \(\Sigma_s\) relative to a dedicated (non-MEMS-compatible) rare-earth ferrimagnet source.

### 5.3 Systematic error channels unique to the monolithic design

- **Magnetic cross-talk between arms:** the active arm's bias field and any residual moment must be shielded from the reference arm to avoid reintroducing a non-torsion magnetic coupling that mimics the target signal.
- **Piezoresistive/piezomagnetic coupling:** dopant-induced strain sensitivity can couple the bias-field reversal directly into a mechanical signal through non-torsion channels (magnetostriction of the doped lattice), which must be characterized and subtracted using the reference arm.
- **Dopant-gradient-induced static torque:** any inhomogeneity in dopant concentration across the resonator body produces a static (non-reversing) offset that must be distinguished from a true reversing signal by the lock-in scheme of Section 4.3.

---

## 6. Fabrication Pathway

A staged fabrication approach is proposed, moving from the least to most materials-feasible variants:

1. **Baseline (near-term, buildable now):** undoped or lightly Fe/Mn-doped silicon torsional MEMS fabricated by standard DRIE/SOI processes, used to validate the mechanical, readout, and lock-in architecture with a synthetic (non-spin) reversing signal, establishing the device's noise floor independent of the materials question.
2. **Cryogenic Mn:Si or Mn:GaAs-on-Si variant:** operated below the ordering temperature of the dopant system, accepting reduced \(Q\) from cryogenic packaging complexity in exchange for a materially real (if imperfect and non-fully-monolithic, in the heteroepitaxial case) spin source.
3. **Aspirational monolithic room-temperature variant:** contingent on a materials-science advance in high-solubility, crystal-field-resistant dopants compatible with silicon MEMS thermal budgets — not demonstrated as of this writing, and the primary open problem this paper identifies.

---

## 7. Discussion: Why This Remains a Theoretic Candidate

The central finding of this paper is that the spin-doped silicon composite is well-posed as a *measurement concept* — Section 2 shows the torsion-mediated torque it would need to detect is a real, calculable quantity within Frame Theory, and Section 4 shows a concrete, buildable device architecture exists to attempt the measurement — but it is blocked as a *materials system* by the tradeoff identified in Section 3.2: every silicon-compatible dopant strategy surveyed either fails to reach a usable spin density at room temperature, or reaches it only by introducing lattice disorder that degrades the mechanical \(Q\) the measurement depends on.

This is not a claim that no such dopant system can exist — it is a claim about the current state of silicon magnetic-doping materials science. The specific threshold a future advance would need to clear is a dopant (or dopant complex) with solid solubility in crystalline Si or SiGe above the level needed for a competitive \(\Sigma_s\), combined with crystal-field or shielding behavior sufficient to preserve net spin polarization at or near room temperature, combined with chemical stability through standard MEMS thermal processing — three conditions that, to our knowledge, no presently characterized dopant-host system satisfies simultaneously. This paper's contribution is to state that threshold precisely, in the same quantitative terms as the signal it would enable, so that progress in dilute magnetic semiconductor materials science can be evaluated directly against the requirements of a working framet device.

---

## 8. Conclusion

The spin-doped silicon composite is a theoretically well-defined and mechanically buildable device concept for a monolithic torsion-source/torsion-readout framet, unifying the two roles that existing spin-torsion experiments perform with separate materials. Its predicted signal follows directly from the axial-current torsion relation of Frame Theory §5.3, and its architecture is a straightforward extension of established differential MEMS torsion-balance and silicon photonic readout techniques. Its realization is presently blocked by a materials-science tradeoff between achievable spin density and mechanical quality factor in silicon-compatible dopant hosts, not by any conceptual or measurement-principle obstacle. It is classified as a theoretic candidate on that basis, with the specific materials thresholds for promotion to a genuine candidate stated in Section 7.

---

## Appendix A: Symbol Glossary

| Symbol | Meaning |
|---|---|
| \(j_5^a\) | axial current |
| \(n_s\) | dopant number density |
| \(\langle S_z\rangle\) | mean electron spin polarization along bias axis |
| \(\Sigma_s\) | effective areal spin density figure of merit |
| \(V_{\mathrm{overlap}}\) | effective torsion-coupling interaction volume |
| \(I\) | resonator moment of inertia |
| \(Q\) | mechanical quality factor |
| \(\omega_0\) | resonant angular frequency |

## Appendix B: Derivation Note on Section 2.2

The contact-like (non-propagating) form of the torque expression follows directly from the algebraic character of the torsion field equation established in §4.2 of *Frame Theory*: because the connection equation contains no derivatives of torsion, \(T^a\) is fixed pointwise by the local spin current rather than obeying a wave equation, so the interaction between spatially separated spin populations is confined to their region of physical overlap or near-overlap, rather than falling off as an inverse-square propagating field. This is the theoretical basis for the paper's central design claim that monolithic (zero-standoff) source-detector integration yields a multiplicative rather than incremental sensitivity gain.

## Appendix C: Candidate Dopant Comparison — Summary Ranking

1. Mn:GaAs-on-Si (heteroepitaxial, cryogenic) — most experimentally mature magnetic-semiconductor system, but not fully monolithic and requires cryogenic operation
2. Substitutional Mn:Si (cryogenic) — fully monolithic, but low achievable \(\Sigma_s\) and secondary-phase formation at usable doping levels
3. Interstitial Fe:Si — thermally unstable through MEMS processing; not viable without major process modification
4. Gd or Eu in Si/SiGe — most favorable spin physics (shielded \(4f\) moment) but blocked by solid-solubility limits
5. Co:Si — crystal-field quenching dominates; lowest-ranked candidate

## Appendix D: Open Experimental Questions

- What is the maximum substitutional Mn concentration in device-grade silicon achievable without secondary-phase (MnSi, Mn\(_4\)Si\(_7\)) nucleation, under a thermal budget compatible with standard MEMS release processes?
- Can a co-doping strategy (e.g., charge-compensating a magnetic dopant with a shallow donor or acceptor) suppress secondary-phase formation without proportionally suppressing net spin polarization?
- What is the achievable mechanical \(Q\) of a Mn- or Fe-doped single-crystal silicon torsional resonator as a function of doping concentration, and does this relationship admit a usable operating point given the sensitivity budget of Section 5?
- Does a bonded (non-monolithic) hybrid — a thin, high-solubility magnetic-semiconductor film transferred onto an undoped high-\(Q\) silicon MEMS resonator — recover most of the interaction-volume advantage of Section 2.2 while avoiding the mechanical-magnetic tradeoff of Section 3.2, and is this a more promising near-term path than full monolithic doping?

---

## Selected References

1. F. W. Hehl, P. von der Heyde, G. D. Kerlick, J. M. Nester, "General relativity with spin and torsion: Foundations and prospects," *Reviews of Modern Physics*.
2. E. G. Adelberger, B. R. Heckel, A. E. Nelson, "Tests of the gravitational inverse-square law," *Annual Review of Nuclear and Particle Science*.
3. T. Dietl, H. Ohno, "Dilute ferromagnetic semiconductors: Physics and spintronic structures," *Reviews of Modern Physics*.
4. C. Weisbuch, B. Vinter, *Quantum Semiconductor Structures*, Academic Press.
5. Companion foundational work: *Frame Theory: A Local-Frame Formulation of Gravitation and the Admissibility Structure of General Relativity*, §5.3, Appendix D.
6. Companion survey: terrestrial framet candidate list, item #24.
