# Manufacturable Core Photonic Elements from Universal Phase Theory

**Technical concept portfolio**  
**Prepared for the UPT photonic-circuit programme**  
**22 August 2026**

## Abstract

This note identifies five **manufacturable, core photonic-circuit elements** obtained by realizing the UPT phase hierarchy on a controllable integrated-optical graph. The central design move is to treat a photonic circuit not as a collection of independent waveguides and rings, but as a finite phase bundle whose local optical fields, tunable couplings, and closed-loop transports define a phase configuration \(\Phi\). The device equation is formulated as \(\mathscr F[\Phi;\lambda]=0\); its linearization, bifurcation determinant, and susceptibility identify calibration, critical switching, and topological transport functions at circuit level.

The proposed library is: **(E1) the susceptibility-calibrated interferometric cell**, a self-identifying \(2\times2\) programmable primitive; **(E2) the bifurcation dimer link**, a tunable SSH-class coupling primitive; **(E3) the Wilson-loop holonomy plaquette**, a phase-curvature and synthetic-gauge primitive; **(E4) the domain-wall resonance block**, a protected resonant filter/delay macrocell; and **(E5) the phase-curvature interferometer**, an interferometric reader for holonomy and local phase geometry. These are not proposals for exotic materials. They are circuit-level elements composed of foundry-recognizable waveguides, directional couplers or MZIs, phase shifters, microrings, weak taps, and monitor photodiodes. Silicon-photonic foundries already supply the relevant component classes, while silicon-photonic MEMS offers a credible low-static-power tuning path.[1] [2]

> **Design conclusion.** The first tape-out should be the coupled pair **E1 + E2**, with E5 included as an on-chip metrology structure. This produces a directly useful programmable primitive while establishing the local stability, susceptibility, and bifurcation measurements from which E3 and E4 can be built without changing the material stack.

| Element | UPT structural object | Immediate circuit function | Baseline process | Priority |
|---|---|---|---|---|
| **E1. Susceptibility-calibrated interferometric cell (SCIC)** | \(\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}\) | Self-calibrated programmable \(2\times2\) transformation | SOI/SiN routing + MZI + phase shifters + Ge monitor PDs | **1** |
| **E2. Bifurcation dimer link (BDL)** | \(\Delta_\Phi=0\), kernel order parameter | Reconfigurable coupling and topological phase switch | Coupled rings or dual-rail waveguides + tunable MZI link | **1** |
| **E5. Phase-curvature interferometer (PCI)** | Phase metric and holonomy readout | On-chip phase-geometry and Wilson-loop meter | MZI with internal calibrated loop and monitor PDs | **1** |
| **E3. Wilson-loop holonomy plaquette (WHP)** | \(A_\mu[\Phi]\), \(F_{\mu\nu}\), \(U_\gamma\) | Synthetic flux, geometric router, tilable gauge cell | Four tunable links; optional microring recirculation | **2** |
| **E4. Domain-wall resonance block (DWR)** | Winding-sector interface and localized defect state | Defect-tolerant channel filter / resonant delay node | Eight–sixteen BDLs in 1-D lattice | **2** |

## 1. Photonic realization of the UPT hierarchy

Let \(\mathcal G=(V,E)\) be the graph of an integrated photonic circuit. A vertex \(v\in V\) is a directional mode, a microring mode, or a dual-rail mode pair; an edge \(e\in E\) is a phase-controlled optical transport segment. The base graph is not itself the physical observable. It is the discrete support on which the photonic phase configuration is defined.

Let \(E_\Phi\to\mathcal G\) be a rank-\(d\) complex phase bundle. At vertex \(v\), \(\Phi_v\in\mathbb C^d\) is the local modal-amplitude column. For a single waveguide or ring, \(d=1\); for a dual rail, polarization pair, or spatial mode doublet, \(d=2\). A controllable edge implements a transport map

\[
U_e(\lambda_e)=e^{-\alpha_e/2}\,C_e(\theta_e)P_e(\phi_e)\in \mathrm{GL}(d,\mathbb C),
\]

where \(\alpha_e\) is the optical loss, \(\theta_e\) is the tunable coupling coordinate, \(\phi_e\) is a propagation or differential phase, and \(\lambda_e=(\theta_e,\phi_e,\alpha_e,\ldots)\) belongs to the local control manifold \(\Lambda_e\). In a dual-rail implementation, a useful unitary idealization is

\[
C(\theta)=
\begin{pmatrix}
\cos(\theta/2) & i\sin(\theta/2)\\
i\sin(\theta/2) & \cos(\theta/2)
\end{pmatrix},
\qquad
P(\phi)=
\begin{pmatrix}
e^{i\phi/2} & 0\\
0 & e^{-i\phi/2}
\end{pmatrix}.
\]

A network with coherent injection \(s\) and one-round-trip transport \(\mathcal U(\lambda)\) obeys the circuit phase equation

\[
\boxed{\mathscr F[\Phi;\lambda]\equiv \bigl(I-\mathcal U(\lambda)\bigr)\Phi-s=0.}
\tag{1}
\]

This is the experimentally specified realization of the universal UPT equation. It converts a phase configuration into a measurable circuit state. The UPT operator hierarchy becomes

\[
\boxed{
\mathscr L_\Phi=D_\Phi\mathscr F=I-\mathcal U(\lambda),\qquad
\Delta_\Phi=\operatorname{Det}_{\Phi}\!\bigl(\mathscr L_\Phi\bigr),\qquad
\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}.
}
\tag{2}
\]

For a passive lossy circuit, \(\rho(\mathcal U)<1\), so \(\boldsymbol\chi_\Phi\) is finite. A small singular value of \(I-\mathcal U\) is then not an assumed physical instability; it is a **large but measurable coherent response**. A true singular point requires a specified physical mechanism—gain, nonlinear feedback, or a lossless idealization—and must be demonstrated rather than inserted. This distinction is decisive for manufacturable photonics.

| UPT level | Integrated-photonic realization | Measured object |
|---|---|---|
| \(\Phi\) | Complex guided-mode amplitudes on a directed graph | Coherent transmission, ring field, near-field tap |
| Topology | Winding, Wilson loop, bandgap sector, graph defect class | Spectral flow, edge/domain-wall state, loop phase |
| Geometry | Response metric \(g_{ij}^{\Phi}\) on control space | Local cross-sensitivity and calibration curvature |
| Connection | Tunable edge transport \(U_e\) | Transfer matrix of a link or MZI |
| Fields | Distributed guided optical field | Power/phase distribution across ports |
| Particles/excitations | Discrete resonant, edge, or defect optical mode | Resonance pole, mode profile, linewidth |
| Observables | Gauge-invariant transmission and loop quantities | \(|S_{ij}|^2\), eigenphases, \(\operatorname{tr}U_\gamma\) |

The physical circuit thereby instantiates the full UPT ontological sequence

\[
\Phi\;\longrightarrow\;\text{topology}\;\longrightarrow\;\text{geometry}\;\longrightarrow\;\text{connections}\;\longrightarrow\;\text{fields}\;\longrightarrow\;\text{discrete modes}\;\longrightarrow\;\text{observables}.
\]

The sequence must be read constructively. A topological sector is not declared from a layout; it is computed from \(\mathcal U(\lambda)\) or the associated band operator. A phase metric is not a geometric metaphor; it is a control-response tensor measured from local perturbations. Connections are implemented by calibrated transport maps. The resulting observable is a transmission spectrum, a transfer matrix, a delay, or a mode occupation.

## 2. Phase reduction, response geometry, and fabrication-aware design rule

At a chosen operating configuration \((\Phi_c,\lambda_c)\), let \(K=\ker\mathscr L_{\Phi_c}\) and let \(R\) be its complement. Writing

\[
\Phi=\Phi_c+\eta^a e_a+\xi,
\qquad \xi\in R,
\]

with \(\{e_a\}\) a basis for \(K\), Lyapunov–Schmidt reduction gives a solved noncritical component \(\xi=\xi(\eta,\lambda)\) and a finite-dimensional reduced equation

\[
\boxed{\varphi^a(\eta,\lambda)=0.}
\tag{3}
\]

In E2 and E4, \(\eta\) is the amplitude of the gap-closing or domain-wall mode. In E1, it is the pair of interferometric control errors. In E3 and E5, it is the loop-eigenphase or the dual-rail holonomy coordinate. The reduction therefore assigns an experimentally addressable order parameter to every candidate component; no element is accepted into the library merely because it has a visually compelling geometry.

Let \(\eta^a(\lambda^i)\) be locally measured from optical transfer data, and define

\[
T_{ia}=\frac{\partial\eta_a}{\partial\lambda^i},
\qquad
S_{ab}=\frac{\partial^2\Phi_{\mathrm{eff}}}{\partial\eta^a\partial\eta^b},
\qquad
\chi^{ab}=(S^{-1})^{ab}.
\]

The UPT response metric is

\[
\boxed{g_{ij}^{\Phi}=T_{ia}\chi^{ab}T_{jb}.}
\tag{4}
\]

For photonic hardware, \(g_{ij}^{\Phi}\) is a direct design object. Its diagonal entries quantify usable phase authority per actuator; off-diagonal entries quantify thermal, mechanical, carrier, or optical cross-talk. The governing manufacturability rule is therefore:

> **A tunable core element is accepted only when its specified operating region has a finite, calibratable susceptibility and a response metric whose off-diagonal terms remain bounded under wafer-scale parameter variation.**

The material platform already supports this programme. Standard silicon photonics supplies routing, couplers, fast modulation, continuous tuning, germanium photodetection, and advanced design kits.[2] Thermo-optic, free-carrier, and MEMS phase controls all exist; the principal scaling question is not whether a phase can be moved, but whether loss, static power, speed, and cross-talk remain compatible with the architecture.[1] [3]

## 3. Proposed core element E1: susceptibility-calibrated interferometric cell

### 3.1 Definition

**E1** is a tunable \(2\times2\) MZI or MEMS directional coupler with two independent controls \((\theta,\phi)\), two weak monitor taps, and a local calibration model. It implements an optical connection together with its measured tangent response. Its transfer map is

\[
\Phi_{\mathrm{out}}=U_{\mathrm{SCIC}}(\theta,\phi)\Phi_{\mathrm{in}},
\qquad
U_{\mathrm{SCIC}}=e^{-\alpha/2}C(\theta)P(\phi).
\tag{5}
\]

The monitor outputs \(y_m\) provide an experimental Jacobian

\[
J_{mi}=\frac{\partial y_m}{\partial\lambda^i},
\qquad \lambda^i\in\{\theta,\phi\},
\tag{6}
\]

which determines the local phase susceptibility after calibration of the optical observation map. Unlike an ordinary MZI, E1 stores a local response certificate: its splitting ratio, internal differential phase, loss, and cross-sensitivity are observed rather than presumed.

| Property | E1 implementation | UPT content | Manufacturable realization |
|---|---|---|---|
| Connection | Tunable \(U_{\mathrm{SCIC}}\in\mathrm{U}(2)\) in the low-loss idealization | \(A_\mu=\mathcal A_\mu[\Phi]\) | Two couplers + two arms + differential/common phase controls |
| Local geometry | Monitor-derived \(J\) and \(g_{ij}^{\Phi}\) | Susceptibility-induced metric | 0.5–2% taps + Ge PDs or external calibration port |
| Stability | Minimum singular value of local response map | \(\mathscr L_\Phi\), \(\Delta_\Phi\) | Dither calibration and digitally stored compact model |
| Reconfiguration | Bar, cross, arbitrary splitting, phase correction | Phase transport | Thermal baseline; MEMS for static configuration; carrier/BTO for speed |

### 3.2 Why it is a new core element

The MZI alone is established. **E1 is not a claim that the MZI is new.** The proposed element is the *self-characterizing phase connection*: MZI, monitors, dither protocol, local inverse response, and exported covariance are one PDK object. This changes the elementary abstraction from “set a heater voltage” to “request a connection with certified \((\theta,\phi,\chi)\).” That is the correct primitive for a UPT circuit, because connection and phase geometry are co-generated.

### 3.3 First validation

A four-cell E1 test matrix should estimate the full \(8\times8\) response matrix under independent perturbations. The primary falsification criterion is strict: if the locally inferred \(g_{ij}^{\Phi}\) does not predict output drift and cross-talk better than a voltage-only independent-actuator model, E1 has not established a useful UPT-derived design advantage. The optical component remains useful, but the susceptibility layer is rejected or redesigned.

## 4. Proposed core element E2: bifurcation dimer link

### 4.1 Definition

**E2** is a two-site resonant or dual-rail module whose intracell and intercell couplings \(J_A\) and \(J_B\) are individually controlled by E1 links. In the chiral, loss-balanced approximation, its Bloch operator is

\[
H_{\mathrm{BDL}}(k)=
\begin{pmatrix}
0 & J_A+J_Be^{-ik}\\
J_A+J_Be^{ik} & 0
\end{pmatrix}
=
\bigl(J_A+J_B\cos k\bigr)\sigma_x+J_B\sin k\,\sigma_y.
\tag{7}
\]

The bandgap closes at \(|J_A|=|J_B|\). The winding sector is

\[
\nu=\frac{1}{2\pi i}\int_{-\pi}^{\pi}\partial_k\log\!\bigl(J_A+J_Be^{-ik}\bigr)\,dk
=
\begin{cases}
1,&|J_B|>|J_A|,\\
0,&|J_B|<|J_A|.
\end{cases}
\tag{8}
\]

At the transition the reduced order parameter is the gap-closing mode \(\eta\). Taking a resonator round-trip operator \(\mathcal U_{\mathrm{BDL}}\), the device equations are precisely

\[
\mathscr F_{\mathrm{BDL}}=(I-\mathcal U_{\mathrm{BDL}})\Phi-s=0,
\quad
\mathscr L_{\Phi}=I-\mathcal U_{\mathrm{BDL}},
\quad
\Delta_\Phi=\operatorname{Det}_{\Phi}(I-\mathcal U_{\mathrm{BDL}}).
\tag{9}
\]

The experimentally accessible transition is a **bandgap closing and reopening**, diagnosed by a zero of the appropriate reduced spectral determinant. It must not be mislabeled a nonlinear optical instability unless nonlinear feedback is deliberately integrated.

| Requirement | Baseline implementation | Measured falsification condition |
|---|---|---|
| Independent \(J_A,J_B\) | Two E1 MZI links between ring or dual-rail sites | Couplings cannot be fitted independently from transfer data |
| Controlled detuning | One local phase shifter per site | Site detuning overwhelms the intended gap closure |
| Gap-sector change | Scan \(J_A/J_B\) across unity | No observed closure/reopening in the calibrated spectrum |
| Topological classification | Winding from transfer/band reconstruction | Claimed \(\nu\) changes without a gap closure |

### 4.2 Circuit role

E2 is the minimal **phase-transition transistor** of the library. It does not amplify electrically. It makes a discrete change in the qualitative transport sector—trivial versus winding—through a continuous, calibrated change of coupling. This is the lowest-complexity manufacturable bridge from UPT bifurcation theory to protected photonic functionality. A large-scale CMOS-fabricated programmable topological silicon-photonic circuit has already shown that individual ring phases and MZI-mediated couplings can be controlled at scale; that work validates the ingredients, not this proposed PDK-level abstraction.[4]

## 5. Proposed core element E3: Wilson-loop holonomy plaquette

### 5.1 Definition

**E3** is a closed four-link dual-rail network, with an E1 transport operator on every edge. The plaquette holonomy is

\[
\boxed{
U_{\square}=U_4U_3U_2U_1,
\qquad
U_{\square}=\mathcal P\exp\!\left(-\oint_{\partial\square}A\right).
}
\tag{10}
\]

For a rank-one phase bundle, \(U_{\square}=e^{i\varphi_{\square}}\) and \(\varphi_{\square}\) is a programmable Abelian synthetic flux. For a dual rail,

\[
U_j=C(\theta_j)P(\phi_j),
\qquad
[U_i,U_j]\neq0
]

in general, so E3 realizes a non-Abelian transport object. Its gauge-invariant primary readout is the Wilson quantity

\[
\mathcal W_{\square}=\frac{1}{2}\operatorname{tr}U_{\square}.
\tag{11}
\]

The physical significance is exact: \(U_{\square}\neq I\) means that an optical state transported around the loop differs from its initial local frame. This is a laboratory realization of nontrivial phase transport, not a metaphorical use of curvature.

### 5.2 Device function

E3 is a tilable **synthetic-gauge tile**. A single plaquette is a tunable loop filter, geometric phase shifter, or route-selective four-port. A lattice of plaquettes yields programmable flux patterns, edge channels, and phase-texture routing. Its essential advantage over a bare resonant loop is that the loop invariant is designed, calibrated, and externally addressable at the level of transport matrices.

| Specification | E3 target | Test |
|---|---|---|
| Abelian flux control | Sweep \(\varphi_{\square}\) over \([0,2\pi)\) | Interferometric loop phase tracks setpoint modulo \(2\pi\) |
| Non-Abelian transport | Use at least two noncommuting \(C(\theta_j)P(\phi_j)\) links | Reversing segment order changes \(U_{\square}\) while fixed-frame \(\mathcal W_{\square}\) follows prediction |
| Local-frame redundancy | Apply programmable rail-frame changes at vertices | \(\operatorname{tr}U_{\square}\) remains invariant within metrology error |
| Manufacturability | Four E1 links with compact routing | Measured excess loss does not close the intended spectral window |

The required topology is not speculative at material level. Programmable microring/MZI circuits on CMOS silicon have already realized individually programmed site phases and coupling strengths in two-dimensional topological lattices.[4] E3 isolates that system-level capability into a reusable core tile.

## 6. Proposed core element E4: domain-wall resonance block

### 6.1 Definition

**E4** is a finite chain of E2 links in which the dimerization changes sign across an interface:

\[
\cdots (J_A,J_B)(J_A,J_B)\;\vert\;(J_B,J_A)(J_B,J_A)\cdots .
\tag{12}
\]

When the two sides occupy distinct winding sectors and the protecting gap remains open, the interface supports a localized phase defect mode. In UPT language, \(\Phi_{\mathrm{DW}}\) is a stable localized configuration selected by a topological invariant. In circuit language, it is an accessible resonant state whose spatial localization, linewidth, and coupling to bus ports are designed.

A practical first design uses eight to sixteen ring sites, E1-calibrated tunable links, an input bus, a drop bus, and tap monitors at the interface. Its finite network equation remains Eq. (1); the defect mode is found from the eigenvalue branch of \(\mathcal U\) closest to unit round-trip phase. The relevant classification is not inferred from a bright spot at the interface; it requires an observed bulk-gap closure/reopening under a controlled interpolation between the two coupling sectors.

### 6.2 Circuit function

E4 is a **reconfigurable topological channel filter and resonant delay node**. It is suited to channel selection, protected recirculating state storage, and robust insertion of a localized intermediate mode between two otherwise distinct transport regions. A silicon-slab topological ring resonator has already been fabricated and operated as notch and channel-drop filters, establishing the device-level direction.[5]

| Use case | UPT mechanism | Observable success criterion |
|---|---|---|
| Channel-drop filter | Domain-wall discrete phase sector | Defect resonance appears only in the intended sector and couples to drop port |
| Reconfigurable delay node | Localized resonant excitation | Group delay peak is programmable with the interface mode |
| Defect routing | Topological transport around a controlled vacancy | High-transmission route persists under permitted link disorder |
| Calibration benchmark | Phase-stability spectrum | Extracted gap and localization length agree with calibrated link model |

Topological protection is not a blanket immunity to loss, backscattering, thermal drift, or arbitrary symmetry breaking. E4 derives robust transport only against perturbations that preserve the relevant gap and protecting structure. The permitted perturbation class must be part of its PDK contract.

## 7. Proposed core element E5: phase-curvature interferometer

### 7.1 Definition

**E5** is a balanced MZI in which one arm contains E3, or a calibrated closed transport loop, and the other arm contains a reference connection. Let \(\phi_r\) be the reference-arm phase and \(U_\gamma\) the internal loop holonomy. For a prepared internal state \(|\psi\rangle\), the normalized monitor signal is

\[
I_\pm=\frac{I_0}{2}\left[1\pm \mathcal V\,\operatorname{Re}\!\left(e^{i\phi_r}\langle\psi|U_\gamma|\psi\rangle\right)\right],
\tag{13}
\]

where \(\mathcal V\) is the calibrated visibility. By sweeping \(\phi_r\), E5 reconstructs the complex loop expectation value. With two prepared rail states, it reconstructs the entries of \(U_\gamma\) up to the chosen measurement completeness.

### 7.2 Why it is essential

E5 converts phase transport into a falsifiable observable. Without an on-chip holonomy reader, E3 is merely a controlled layout. With E5, the connection, curvature, and loop invariant are metrological objects. E5 is therefore the required bridge from the UPT connection hierarchy to a foundry test structure.

| Test | Prediction | Failure that rejects the interpretation |
|---|---|---|
| Reference scan | \(I_\pm\) is sinusoidal in \(\phi_r\) with calibrated contrast | No stable retrieval of loop phase beyond ordinary drift |
| Loop reconfiguration | Retrieved \(U_\gamma\) follows product of independently characterized links | Product model fails outside measurement uncertainty |
| Gauge-frame test | Wilson trace is invariant under internal rail-frame changes | Claimed invariant changes under a pure frame transformation |
| Disorder scan | Response follows \(g_{ij}^{\Phi}\) in the operating neighbourhood | Metric does not predict sensitivity ranking |

## 8. Manufacturability architecture and development sequence

The elements are deliberately arranged in a manufacturable dependency order. E1 uses no non-standard photonic physics. E2 uses E1 twice. E5 provides the metrology for E3. E4 is a finite composition of E2. This structure prevents the programme from prematurely relying on a large lattice before the local phase connection has been characterized.

| Tape-out stage | Contents | Process choice | Primary decision gate |
|---|---|---|---|
| **A. Local connection** | E1 matrix, passive references, monitor PDs | Standard SOI PDK; thermo-optic controls | Can the susceptibility model predict cross-talk and correct \(\theta,\phi\)? |
| **B. Transition primitive** | E2 dimers, spectral taps, on-chip E5 | Same stack; MEMS variant optional | Does the observed spectrum close/reopen at calibrated \(|J_A|=|J_B|\)? |
| **C. Holonomy tile** | Single E3 + E5 tomography | Same stack, careful symmetric routing | Does \(\mathcal W_\square\) match the calibrated ordered product? |
| **D. Protected macrocell** | E4 chain with defect and disorder structures | Low-loss SOI or SiN routing plus active control | Does an interface mode persist over the predeclared perturbation class? |
| **E. Tiled circuit** | Array of E3/E4 blocks | MEMS or heterogeneous fast-control option | Can local calibrated elements scale without response-metric collapse? |

Thermo-optic tuning is the baseline for stages A–D because it is widely available and low loss; it also introduces static-power and thermal-cross-talk limitations at scale.[1] [3] Silicon-photonic MEMS is the preferred configuration layer for a large static mesh because foundry-integrated MEMS couplers and phase shifters can be compact, low loss, broadband, and low power, including wafer-level sealing and standard photonic-component co-integration.[2] Fast data-path modulation is a separate requirement and should not be imposed on the first UPT phase-configuration experiment.

## 9. Derivation boundary: what the UPT construction derives and what the chip must supply

UPT supplies a strict organizational derivation once the photonic transport equation is physically specified. It does not authorize insertion of unmeasured device parameters, protected sectors, or response metrics by declaration.

| Derived from the specified phase equation | Must be physically supplied and measured |
|---|---|
| \(\mathscr L_\Phi\), \(\Delta_\Phi\), and \(\boldsymbol\chi_\Phi\) of the circuit | Material dispersion, loss, backscatter, coupling coefficients, actuator transfer curves |
| Order-parameter space after a measured or modeled kernel appears | Whether a true singularity is accessible in a passive lossy circuit |
| Phase-response metric \(g_{ij}^{\Phi}\) | Monitor calibration, detector noise, electronic feedback bandwidth |
| Holonomy \(U_\gamma\) and gauge-invariant Wilson quantities | Link matrices and the selected internal-mode basis |
| Winding sector and domain-wall mode of a calibrated lattice | The symmetry/gap conditions required to protect that sector |
| Observable spectra, transfers, and mode profiles | Packaging, thermal boundary conditions, process spread, and yield |

This boundary is the strength of the programme. The UPT formulation yields a falsifiable design language: phase geometry is accepted only if it predicts local response; a bifurcation sector is accepted only if its determinant and spectral evolution are observed; topology is accepted only if a predeclared invariant is stable under its permitted perturbation class.

## 10. Priority recommendation and research questions

The recommended first architecture is a **six-element E1 array containing two E2 dimers and one E5 interferometric monitor**. It is sufficiently small to permit full transfer-matrix characterization yet contains every required structural layer: phase connection, response geometry, bifurcation coordinate, and a gauge-invariant loop readout. The same mask can include a passive reference, a thermal version, and a MEMS-compatible layout variant.

| Rank | Element set | Why it should be first | Principal research question |
|---|---|---|---|
| **1** | E1 + E2 + E5 | Maximizes learned structure per active component; no exotic process | Does the measured susceptibility metric support robust local compilation? |
| **2** | E3 + E5 | Establishes programmable holonomy as an observable circuit primitive | Can ordered noncommuting transport be reconstructed and stabilized on chip? |
| **3** | E4 | Converts local phase-transition control into protected functional routing/filtering | Which loss and symmetry-breaking terms bound the usable protection window? |
| **4** | E3 lattice | Demonstrates emergent transport geometry at circuit scale | Do calibrated local tiles remain composable under large-array thermal and loss disorder? |

The core research questions are precise. First, does a local susceptibility model improve calibration sufficiently to serve as a PDK contract rather than a post hoc fit? Second, can UPT phase metric \(g_{ij}^{\Phi}\) rank and predict fabrication- and control-induced cross-sensitivity? Third, can holonomy be programmed as a gauge-invariant transfer quantity independent of local frame choice? Fourth, can a topological defect mode remain functional across a quantitatively specified perturbation ensemble? Each admits a negative answer. Each negative answer refines or rejects a particular proposed element without weakening the rigor of the programme.

## References

[1] H. Sun *et al.*, “[Silicon Photonic Phase Shifters and Their Applications: A Review](https://pmc.ncbi.nlm.nih.gov/articles/PMC9504597/),” *Micromachines* **13**, 1509 (2022).

[2] N. Quack *et al.*, “[Integrated silicon photonic MEMS](https://www.nature.com/articles/s41378-023-00498-z),” *Microsystems & Nanoengineering* **9**, 27 (2023).

[3] S. Shekhar *et al.*, “[Roadmapping the next generation of silicon photonics](https://www.nature.com/articles/s41467-024-44750-0),” *Nature Communications* **15**, 751 (2024).

[4] T. Dai *et al.*, “[A programmable topological photonic chip](https://pmc.ncbi.nlm.nih.gov/articles/PMC11230904/),” *Nature Materials* **23**, 928–936 (2024).

[5] L. Gu *et al.*, “[A topological photonic ring-resonator for on-chip channel filters](https://arxiv.org/abs/2105.07171),” *Journal of Lightwave Technology* **39**, 6312–6321 (2021).

[6] PsiQuantum team, “[A manufacturable platform for photonic quantum computing](https://www.nature.com/articles/s41586-025-08820-7),” *Nature* **641**, 876–883 (2025).

---

**Source basis.** The formal UPT definitions, including \(\mathscr F[\Phi;\lambda]=0\), \(\mathscr L_\Phi\), \(\Delta_\Phi\), \(\boldsymbol\chi_\Phi\), Lyapunov–Schmidt reduction, emergent phase metric, phase transport, and holonomy are adapted to the circuit setting from the supplied UPT manuscript materials. The cited literature supports statements concerning present-day integrated-photonic components, fabrication platforms, and prior experimental demonstrations.
