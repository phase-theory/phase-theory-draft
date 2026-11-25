# Organic Electronics Engineering

## Invariant-First Design of Soft, Disordered, Permeable Semiconductor Systems

**Preprint — 25 November 2026**
*Paper II in the series. Companion to Paper I, "The Organic Transistor: A Unified Field Theory of Gate-Modulated Transport in Disordered Mixed Conductors" (2026), cited throughout as [I].*

---

### Abstract

We develop organic electronics as a design science rather than a materials catalogue. The organizing thesis is that the discipline's central obstacle is not low mobility or poor stability but **non-identifiability**: constitutive parameters of soft, disordered, permeable semiconductors are not recoverable from terminal measurements and are not transferable between device contexts, so specifications written in terms of "the mobility" or "the trap density" are ill-posed. We prove an exponent-matrix identifiability theorem that computes, for any power-law observable set, the exact dimension of the unidentifiable fibre and the ring of identifiable invariants, and we advocate **invariant-first design**: specify invariants, then select any material–process point in the fibre satisfying manufacturing constraints. Around this calculus we derive the engineering laws of the field as theorems with explicit hypotheses: a delocalization scaling λ_eff = λ_mono/N for reorganization energy; a derived interfacial polar-disorder law σ_d ∝ p√N/(ε z) explaining the low-k dielectric rule; the exact Dykhne geometric-mean theorem for polycrystalline in-plane transport; an Onsager doping ceiling e^{−r_c/a} and a dopant-overlap ionization threshold N* = (4a)^{−3}; the Mark–Helfrich trap-limited space-charge law derived in full; a drying stratification factor Pe/(1−e^{−Pe}) and a coating-speed ceiling v ≤ L_oven D/H²; the exact dipole-over-mirror Green-dyadic rates and a sharp outcoupling orientation bound ρ(n) = (c²+c+4)/4 ≤ 3/2; the exact triplet–triplet roll-off curve with J_{1/2} = 4qw/(k_TT τ²) and an outcoupling–Purcell trade-off theorem with current-dependent weight ω = (s−1)/(2s); exact spherical-domain exciton harvesting and an optimal bulk-heterojunction domain size R* ∝ (L_D² d)^{1/3}; an Urbach voltage-penalty theorem with a hard threshold at E_U = k_BT; an exact disorder-cancellation in the hopping Seebeck coefficient with universal optimum S* = 2k_B/q; channel-cracking and shear-lag strain-isolation laws; a multilayer barrier n² lag-time theorem and a derived WVTR requirement; and a **dispersive consistency theorem** unifying four independent measurements through one parameter, α = β_K = 1 − β = 1/(m−1). Eight no-go theorems delimit the achievable design space. Fourteen falsifiable predictions are stated.

**MSC 2020.** 82D37, 82D80, 35Q81, 74R10, 74F15, 76R50, 78A25, 93B30, 90C90, 26A33.

**Keywords.** organic electronics; invariant-first design; identifiability; molecular doping; space-charge-limited current; outcoupling; efficiency roll-off; bulk heterojunction; Urbach energy; organic thermoelectrics; channel cracking; barrier permeation; bias stress; printed circuits.

---

## 1. Introduction

### 1.1 The engineering object

Organic electronics is the engineering of electronic function in solids held together by van der Waals forces. That single structural fact generates the entire discipline's difficulty and its entire opportunity. Because cohesion is weak:

- **Electronic bandwidth is small.** Transfer integrals J ≈ 10–100 meV compete with reorganization energies λ_r ≈ 0.1–0.3 eV and with energetic disorder σ ≈ 50–150 meV. Transport is a hopping problem whose coefficients are functionals of state [I, §4].
- **The lattice is soft.** Young's moduli E ≈ 0.1–20 GPa span four decades across a single device stack, against 130 GPa for silicon. Mechanics is a first-class design variable, not a packaging afterthought.
- **The solid is permeable.** Water, oxygen, and small ions enter. This is a liability for encapsulation and an asset for electrochemistry and sensing.
- **The permittivity is low.** ε_r ≈ 3–4 gives an Onsager radius r_c ≈ 16 nm at 300 K, sixteen lattice spacings. Coulomb interactions are unscreened on the scale of the microstructure, which controls doping, recombination, and injection.
- **The microstructure is process-created.** Unlike a wafer, whose structure is set by crystal growth before any device step, an organic film's morphology is created *during* deposition and drying. Process and property are not separable.

### 1.2 The central difficulty is not mobility

The field's self-diagnosis has long been "mobility is too low" and "lifetime is too short." Both are true and both are, as engineering statements, incomplete. The deeper obstacle is this:

> **The parameters we use to specify organic materials are not identifiable from the measurements we make, and are not invariant across the device contexts in which we use them.**

Paper I proved this for the transistor: linear-regime transfer data admits an infinite-dimensional fibre of (mobility, contact-resistance) pairs [I, Thm 7.1], and even the saturation branch leaves a residual-conductivity degeneracy [I, Prop 7.5]. The consequence is not merely that reported mobilities scatter by two orders of magnitude. It is that a specification such as "μ ≥ 1 cm² V⁻¹ s⁻¹" is, absent a stated extraction protocol and hypothesis set, **not a specification at all** — it does not partition the space of deliverable devices.

The same pathology recurs everywhere. "The" bimolecular recombination coefficient of a blend is not measurable independently of the domain size that sets it. "The" trap density inferred from bias stress depends on the dispersive model assumed. "The" volumetric capacitance of a mixed conductor cannot be separated from film thickness by any terminal measurement [I, Thm 8.5]. In each case the reported number is a coordinate on a fibre, presented as a point.

### 1.3 Thesis: invariant-first design

We propose to reorganize the discipline around a different primitive. Let θ ∈ ℝ^p_+ be constitutive parameters and O: ℝ^p_+ → ℝ^m_+ the terminal observables. Define θ ~ θ′ iff O(θ) = O(θ′). An engineering specification must be a function on the quotient ℝ^p_+/~. Functions on the quotient are exactly the **invariants**.

**Invariant-first design** is the practice of:

1. fixing the observable set O that the application actually consumes;
2. computing the invariant ring and the fibre dimension (Theorem 2.3);
3. writing performance targets as inequalities on invariants;
4. treating all remaining parameter freedom as a *manufacturing* choice — cost, thickness, throughput, mechanical compliance — to be optimized within the fibre;
5. auditing which fibre directions, invisible in O, are visible in reliability, and adding them to O.

Step 5 is the subtle one and is, we argue, the principal source of unexplained field failures: a drift along a fibre direction is by construction invisible in the acceptance test and may be decisive for lifetime. We formalize this as **silent variability** (§2.5).

### 1.4 Contributions

Results are proved under stated hypotheses. Items marked **Claim** are asymptotic under an explicit closure; **Conjecture** and **Open Problem** are not load-bearing.

- **T1 (§2).** Exponent-matrix and constant-rank identifiability theorems; the invariant rings of the OFET, OECT, OLED, OPV and thermoelectric generator; the invariant-Jacobian variability law; silent variability.
- **T2 (§3).** Delocalization scaling of reorganization energy; interfacial polar-disorder law and the derived low-k rule; exact Dykhne polycrystal theorem; Onsager doping ceiling and overlap ionization threshold; conductivity maximum; full Mark–Helfrich derivation; injection number and the ohmic-contact criterion; Helmholtz dipole-layer design rule.
- **T3 (§4).** Drying stratification factor; Marangoni reversal criterion; Ohnesorge jettability window; coating-speed ceiling; coarsening-limited morphology retention; registration-dominated variability law.
- **T4 (§5).** Exact dipole-over-mirror decay rates from the Green dyadic; orientation-resolved escape-cone capture and the sharp bound ρ ≤ 3/2; exact TTA roll-off curve; outcoupling–Purcell trade-off theorem.
- **T5 (§6).** Exact spherical-domain harvesting; two-carrier Hecht identity; optimal domain size; reciprocity-based voltage budget; energy-gap-law slope; Urbach threshold theorem.
- **T6 (§7).** Volumetric invariants; tissue–device mechanical matching; exact disorder cancellation in the hopping Seebeck coefficient; universal optimum Seebeck and ZT ceiling.
- **T7 (§8).** Channel-cracking onset law; neutral-plane theorem; shear-lag strain isolation; barrier–flexibility feasibility condition.
- **T8 (§9).** Tortuosity tensor; multilayer n² lag theorem; dose-limited WVTR requirement; Kohlrausch–dispersion identity and the **dispersive consistency theorem**; acceleration-model audit.
- **T9 (§10–11).** Noise-margin/gain/scale-length chain; Pelgrom-versus-registration dichotomy; yield; cost model; the design chart and eight no-go theorems.

### 1.5 Relation to prior work

Every physical ingredient is established: hopping transport [1–6], Onsager geminate escape [7,8], molecular doping [9–11], injection theory [12–14], trap-limited SCLC [15,16], random-conductor duality [17,18], drying and printing [19–22], dipole radiation in microcavities [23–26], OLED roll-off [27,28], photovoltaic reciprocity and non-radiative loss [29–31], mixed-conductor devices [32,33], organic thermoelectrics [34–36], thin-film fracture and stretchable mechanics [37–40], barriers [41–43], dispersive relaxation [44,45], and variability [46].

New here is the architecture: the identifiability calculus and its application as a design methodology; the specific closed forms and bounds listed above, several of which (the orientation bound ρ ≤ 3/2, the Urbach threshold, the Seebeck optimum, the n² barrier law, the dispersive consistency theorem) are, to our knowledge, stated here for the first time in this sharp form; and the systematic separation of theorem from closure throughout.

### 1.6 Notation

Latin indices i,j,k,l ∈ {1,2,3}; repeated indices summed; ambient metric δ_ij. x³ ≡ z is the film normal. q > 0 elementary charge; β = (k_BT)^{−1}; ε^{ij} absolute permittivity tensor, ε its isotropic value. σ (no subscript) energetic disorder width, σ̂ = σ/k_BT. σ_ij stress, ε_ij strain (context distinguishes from permittivity and disorder). a localization length; a_mol molecular spacing; ν₀ attempt frequency. C_i areal capacitance (F m⁻²); C* volumetric capacitance (F m⁻³). μ mobility magnitude, μ^{ij} its tensor. Θ^{ij} dipole orientation tensor (§5). C_ijkl elastic stiffness. 𝔾_ij dyadic Green function. r_c = q²/(4πεk_BT) Onsager radius; 𝔠 = r_c/a Coulomb number. α = k_BT/E_c fractional order; l = 1/α. ℝ_+ = (0,∞).

Numerics are SI internally, reported in Å, nm, cm², eV, meV where the literature does. Plain-text mathematics: `_` subscript, `^` superscript. ∎ ends a proof.

---

## 2. The Invariant Calculus

### 2.1 The design chain

**Definition 2.1 (Design chain).** The design chain is the composition

  𝒫 --(process map Π)--> 𝒨 --(constitutive map Φ)--> 𝒞 --(device map Ψ)--> 𝒟 --(system map Σ)--> 𝒮,

where 𝒫 is the space of process recipes (ink formulation, deposition, drying, annealing, patterning), 𝒨 the space of microstructures, 𝒞 the space of constitutive laws, 𝒟 the space of terminal device characteristics, 𝒮 the space of system specifications.

The essential structural fact of organic electronics is that **Π is not injective and Φ is not injective**, and that the non-injectivity of Φ is *not* removable by better measurement of 𝒟, because Ψ is also non-injective. Silicon device engineering is the special case in which Φ is nearly injective (band transport with a handful of well-separated parameters) and Π is nearly trivial (the crystal is given). Organic electronics has neither simplification.

**Definition 2.2 (Observable set and fibre).** Fix a C¹ map O: ℝ^p_+ → ℝ^m_+ of terminal observables. The *fibre* through θ is F(θ) = {θ′ : O(θ′) = O(θ)}. The *identifiable functions* are the functions constant on fibres.

### 2.2 The identifiability theorems

**Theorem 2.3 (Exponent-matrix identifiability).** Suppose the observables are monomials,

  O_j(θ) = c_j ∏_{i=1}^p θ_i^{A_ji},  c_j > 0,  A ∈ ℝ^{m×p}.  (2.1)

Let r = rank A. Then:

1. In log-coordinates y = ln θ, the fibres are the affine subspaces y + ker A. Hence dim F = p − r.
2. The identifiable monomials are exactly θ^b with b ∈ row(A) ⊂ ℝ^p.
3. The multiplicative group G = {κ ∈ ℝ^p_+ : ln κ ∈ ker A} acts on parameter space preserving all observables, and the invariant ring of monomials is generated by any basis of row(A).

*Proof.* (1) ln O_j = ln c_j + Σ_i A_ji y_i, so O(θ) = O(θ′) iff A(y − y′) = 0. (2) θ^b is constant on fibres iff b·v = 0 for all v ∈ ker A, i.e. b ∈ (ker A)^⊥ = row(A). (3) Immediate from (2) and the definition of the action. ∎

**Theorem 2.4 (Local identifiability, general observables).** Let O be C¹ with log-Jacobian Λ_ji(θ) = ∂ln O_j/∂ln θ_i. If rank Λ = r is constant on a neighbourhood U of θ₀, then F(θ₀) ∩ U is a (p−r)-dimensional C¹ submanifold with tangent space ker Λ(θ₀), and a C¹ function f is locally identifiable iff d ln f ∈ row Λ.

*Proof.* Constant-rank theorem applied to ln O ∘ exp gives local coordinates in which ln O is a projection onto the first r coordinates; the level sets are the coordinate slices. Identifiability of f is constancy along the slices, i.e. annihilation of df by ker Λ, i.e. membership in row Λ. ∎

**Corollary 2.5 (Design rule).** To make a parameter identifiable, add an observable whose log-gradient has a component outside the current row space. Adding observables *inside* the row space — however precise — never reduces the fibre.

This corollary is the formal statement of why measuring the same transfer curve ten thousand times does not determine the mobility, and why a single four-probe measurement does.

### 2.3 Invariants of the principal device classes

We apply Theorem 2.3 to each major class. Throughout, geometry (W, L) is assumed known and bias is held fixed, so both are absorbed into constants.

**(a) Unipolar transistor.** Parameters θ = (μ, C_i, L). Observables: saturation current I_sat ∝ μC_i/L and cutoff frequency f_T ∝ μ/L² [I, Cor 9.3]. Then

  A = [ 1  1 −1 ;  1  0 −2 ],  rank 2, dim F = 1, ker A = span{(2,−1,1)}.

The fibre action is μ ↦ κ²μ, C_i ↦ C_i/κ, L ↦ κL. A basis of row(A) gives the invariants

  **𝔦₁ = μ/L²  (speed),  𝔦₂ = C_i L  (gate charge per unit width per volt).**  (2.2)

*Interpretation.* From DC current and bandwidth alone, "the mobility" is not specifiable; the transit-time constant and the areal gate charge are. A third observable — four-probe conductance, subthreshold swing, or an independent capacitance measurement — breaks the fibre.

**(b) Electrochemical transistor.** θ = (μ, C*, d). Observables g_m ∝ μC*d and f_c ∝ (C*d)^{−1} [I, Thm 8.5]:

  A = [ 1 1 1 ; 0 −1 −1 ],  rank 2, dim F = 1, ker A = span{(0,1,−1)}.

Invariants: **μ and C*d**. Thickness and volumetric capacitance are *separately unidentifiable* and enter only through their product — the algebraic origin of the thickness-invariance theorems of Paper I.

**(c) Emissive diode.** θ = (η_out, Φ_PL, w, k_TT, τ) with observables EQE ∝ η_out Φ_PL and J_{1/2} ∝ w/(k_TT τ²) (§5). rank 2, dim F = 3. Invariants: **η_out Φ_PL** and **w/(k_TT τ²)**. The photoluminescence quantum yield and the outcoupling fraction cannot be separated by electrical-plus-optical efficiency measurement alone; an integrating-sphere or angle-resolved measurement is required.

**(d) Photovoltaic cell.** θ = (L_D, μτ, d, E_g, E_U). Observables: J_sc, V_oc, FF. The harvesting–collection product depends on (L_D/R, μτV/d²) (§6), so the identifiable transport combinations are **L_D/R** and **μτV/d²** — the exciton and carrier *Damköhler numbers* — not L_D and μτ separately. Domain size R is a microstructure variable, measurable by scattering, and must be supplied externally.

**(e) Thermoelectric generator.** θ = (S, σ, κ). Observables: open-circuit voltage ∝ SΔT, matched power ∝ S²σΔT², and efficiency ∝ ZT. Invariants: **S** and **σ/κ**. Conductivity and thermal conductivity are individually identifiable only if a thermal measurement is added.

**Table 2.1 — Invariant rings.**

| Class | Parameters p | Observables m | Fibre dim | Generators of invariant ring |
|---|---|---|---|---|
| OFET | 3 | 2 | 1 | μ/L², C_iL |
| OECT | 3 | 2 | 1 | μ, C*d |
| OLED | 5 | 2 | 3 | η_outΦ_PL, w/(k_TTτ²) |
| OPV | 5 | 3 | 2 | L_D/R, μτV/d², E_g−qV_oc |
| TEG | 3 | 3 | 0 | S, σ, κ |

### 2.4 Variability propagation

**Proposition 2.6 (Invariant Jacobian).** Let ln θ have covariance C_θ. To first order,

  Cov(ln O) = Λ C_θ Λᵀ.  (2.3)

In particular, variability along ker Λ contributes nothing to Cov(ln O).

*Proof.* Linearize ln O = ln c + Λ ln θ and apply the covariance of a linear map. ∎

**Definition 2.7 (Silent variability).** A parameter fluctuation δln θ ∈ ker Λ is *silent* with respect to O. It is *dangerous* if it is not silent with respect to a second observable set O′ (typically reliability: lifetime, drift, hysteresis).

**Proposition 2.8 (Silent-variability hazard).** Let Λ′ be the log-Jacobian of the reliability observables. The dangerous subspace is ker Λ ∩ (ker Λ′)^⊥, of dimension dim ker Λ − dim(ker Λ ∩ ker Λ′). It is nontrivial whenever the reliability observables are not functionally dependent on O.

*Proof.* Elementary linear algebra on the two row spaces. ∎

**Engineering consequence.** In the OECT, the fibre direction (0,1,−1) — trading thickness against volumetric capacitance — is silent in gain and bandwidth but *not* silent in large-signal switching time, which scales as d² [I, Prop 8.7], nor in mechanical compliance, which scales with total stack thickness (§8). Acceptance testing on {g_m, f_c} therefore cannot detect a drift that will fail the device in the field. **The observable set must be closed under the failure modes, not merely under the performance modes.** This is, we argue, the single most consequential methodological conclusion of this paper.

### 2.5 The soft-semiconductor group table

The design manifold is coordinatized by dimensionless groups. We fix the canonical set.

**Table 2.2 — Canonical dimensionless groups.**

| Group | Definition | Name | Typical range | Governing result |
|---|---|---|---|---|
| σ̂ | σ/k_BT | disorder number | 1.2–6 | [I, §4] |
| 𝔠 | r_c/a = q²/(4πεa k_BT) | Coulomb number | 8–25 | §3.4, §3.6 |
| 𝔭 | λ_r/(2|J|) | polaron number | 0.5–10 | §3.1 |
| α | k_BT/E_c | fractional order | 0.2–0.9 | §9.4 |
| Π | C*d/C_i | penetration number | 10⁻³–10⁵ | [I, §2] |
| 𝔨 | ℓ/a_mol | confinement number | 1–20 | [I, §3] |
| Pe | v_ev H/D | drying Péclet | 0.05–20 | §4.1 |
| Oh | η/√(ργa_n) | Ohnesorge | 0.02–1 | §4.3 |
| 𝔪 | E_f/E_s | modulus mismatch | 10⁻³–10⁴ | §8 |
| 𝔫 | L/λ | scaling number | 1–100 | §10.2 |
| 𝔲 | E_U/k_BT | Urbach number | 0.8–3 | §6.5 |
| 𝔤 | Γ_f/(E_f h) | fracture number | 10⁻⁴–10⁻¹ | §8.2 |

Every design rule in this paper is an inequality on these groups. §11 collects them.

---

## 3. Constitutive Engineering: Carriers, Contacts, Dopants

### 3.1 Reorganization energy and delocalization

The Marcus rate between sites i,j is

  ν_ij = (2π/ħ)|J_ij|²(4πλ_r k_BT)^{−1/2} exp[−(Δε_ij + λ_r)²/(4λ_r k_BT)].  (3.1)

The reorganization energy is a sum over normal modes,

  λ_r = ½ Σ_k ω_k² ΔQ_k²,  (3.2)

with ΔQ_k the displacement of mode k between neutral and charged geometries (mass-weighted coordinates).

**Theorem 3.1 (Delocalization scaling).** Let a charge be symmetrically delocalized over N equivalent units, each carrying an identical set of intramolecular modes with monomer reorganization energy λ_mono, and let inter-unit modes be stiff (ω → ∞, ΔQ → 0). Then

  λ_eff = λ_mono/N.  (3.3)

*Proof.* Normalize the charge amplitudes c_a on units a = 1..N with Σ|c_a|² = 1; symmetry gives |c_a|² = 1/N. Linear electron–phonon coupling to the local mode on unit a is proportional to the charge density there, so the effective coupling is g_a = g/N in the amplitude convention where λ = Σ_a g_a²/(ħω) with g the monomer coupling. There are N such modes (one per unit, degenerate), so λ_eff = N·(g/N)²/(ħω) = g²/(Nħω) = λ_mono/N. Stiff inter-unit modes contribute nothing by hypothesis. ∎

**Corollary 3.2 (Molecular design rule).** Since the Marcus activation energy at Δε = 0 is λ_r/4, halving λ_r by doubling delocalization multiplies the rate by ≈ exp[λ_mono/(8k_BT)·(1−1/2)] — for λ_mono = 0.3 eV, a factor of ≈ 18 at 300 K. **Delocalization is the highest-leverage molecular design variable in the field**, exceeding realistic gains in J.

**Caveat (stated, not concealed).** The hypothesis of symmetric delocalization is precisely what disorder destroys: for σ̂ ≫ 1 the polaron localizes on one or two units and (3.3) fails. Theorem 3.1 is therefore a statement about the *achievable ceiling* in ordered, low-disorder systems (rubrene, C8-BTBT, DNTT), not about amorphous polymers. The design programme it defines — reduce σ̂ so that delocalization survives — is the correct reading.

**Definition 3.3.** The polaron number 𝔭 = λ_r/(2|J|) separates regimes: 𝔭 ≪ 1, band-like coherent transport; 𝔭 ≫ 1, small-polaron hopping. With λ_r = 0.2 eV, J = 0.05 eV, 𝔭 = 2 — the generic organic condition, and the reason no single transport picture applies across the field.

### 3.2 Interfacial polar disorder and the low-k rule

Randomly oriented permanent dipoles in the gate dielectric create a random electrostatic landscape in the channel, adding to the intrinsic disorder.

**Theorem 3.4 (Polar-disorder law).** Let the dielectric surface carry a random uncorrelated sheet of dipoles of areal density N_d and moment magnitude p, with isotropic orientation, at distance z from the transport plane, embedded in permittivity ε. Then the induced site-energy variance is

  σ_d² = (π N_d /3) · [q p/(4πε z²)]² · (1 + O(z²N_d)),  σ_d = (qp/(4πε)) √(πN_d/3) / z.  (3.4)

*Proof.* The interaction energy of charge q with a dipole **p** at in-plane separation r and normal offset z is U = q p cosθ/(4πε(r²+z²)) with θ the angle between **p** and the separation vector. For isotropic orientations ⟨cosθ⟩ = 0 and ⟨cos²θ⟩ = 1/3, and cross-terms between distinct dipoles vanish by independence. Hence

  σ_d² = N_d ∫₀^∞ 2πr dr · (qp)²/(3(4πε)²(r²+z²)²) = N_d (qp)²/(3(4πε)²) · 2π · (1/(2z²)) = πN_d(qp)²/(3(4πε)²z²).

The correction term accounts for the breakdown of the point-dipole approximation at r ≲ z. ∎

**Corollary 3.5 (Numerical design rule).** For p = 2 D = 6.67×10⁻³⁰ C m, N_d = 10¹⁸ m⁻² (one dipole per nm²), z = 1 nm, ε = 3ε₀: qp/(4πεz²) = 3.2×10⁻²¹ J = 20 meV, and σ_d ≈ 20 meV. For a strongly polar dielectric with p = 5 D, σ_d ≈ 50 meV. Since μ ∝ exp[−c(σ₀²+σ_d²)/(k_BT)²] [I, Claim 4.12] with c ≈ 4/9, adding σ_d = 50 meV to σ₀ = 70 meV at 300 K reduces μ by

  exp[−(4/9)((86² − 70²)/25.85²)] = exp[−(4/9)(2496/668)] = exp[−1.66] ≈ 0.19.

A fivefold mobility loss from dielectric chemistry alone. This *derives*, rather than reports, the low-k dielectric rule [47].

**Design rules from (3.4).** σ_d ∝ p√N_d/(εz): (i) use low-polarity dielectrics (p ≲ 1 D: CYTOP, PMMA, polystyrene); (ii) insert a spacer — σ_d ∝ 1/z, so 2 nm of inert polymer halves the penalty; (iii) high ε helps *only if* it is achieved without introducing permanent dipoles (electronic/ionic polarizability, not orientational).

### 3.3 Polycrystalline averaging: an exact theorem

Grain orientation is a primary process variable in solution-processed small-molecule films. The in-plane average is not arithmetic.

**Theorem 3.6 (Dykhne geometric mean).** Let a two-dimensional conducting medium be statistically isotropic and self-dual under 90° rotation of the local conductivity tensor, with local principal conductivities σ₁, σ₂ (grains of random orientation, no texture). Then the effective isotropic conductivity is exactly

  σ_eff = √(σ₁σ₂).  (3.5)

*Proof.* In two dimensions the duality transformation σ ↦ σ^D = (det σ)σ^{−1} composed with a 90° rotation maps the conductivity problem to another conductivity problem with the same effective determinant relation σ_eff(σ)·σ_eff(σ^D) = det σ [17,18]. For a statistically isotropic ensemble of grains with fixed principal values, the rotated-and-dualized ensemble has the same statistics (the principal values swap and the orientation distribution is invariant), so σ_eff(σ^D) = σ_eff(σ). Hence σ_eff² = σ₁σ₂. ∎

**Corollary 3.7 (Engineering consequence).** In a randomly oriented polycrystalline film, in-plane mobility is the *geometric* mean of the principal mobilities. Contrast the arithmetic (parallel) mean for stacked layers [I, Prop 4.6]. Consequences:

1. Anisotropy is penalized: for μ₁/μ₂ = 10, the polycrystal delivers √10 ≈ 3.16 times μ₂, not 5.5 μ₂.
2. **Improving the slow axis is exactly as valuable as improving the fast axis**, since ∂ln σ_eff/∂ln σ₁ = ∂ln σ_eff/∂ln σ₂ = 1/2. Molecular design that raises only the π-stacking direction is half-wasted in an untextured film.
3. Texture breaks self-duality and restores arithmetic-like weighting — which is why alignment techniques (blade coating, off-centre spin coating, zone casting) yield gains exceeding any plausible intrinsic improvement.

### 3.4 Doping: the Onsager ceiling and the overlap threshold

Molecular doping proceeds by integer charge transfer from host to dopant (p-type: host HOMO → dopant LUMO). The ionized dopant remains as a fixed Coulomb centre binding the released carrier.

**Theorem 3.8 (Onsager doping ceiling).** Let a carrier thermalize at separation r₀ from its parent ionized dopant in a medium of Onsager radius r_c. At zero field the escape probability is

  P_esc = exp(−r_c/r₀).  (3.6)

With r₀ ≈ a and Coulomb number 𝔠 = r_c/a, the doping efficiency is bounded by η_dop ≤ e^{−𝔠}.

*Proof.* Onsager's solution of the Smoluchowski problem for a Coulomb-attracted pair [7]: the escape probability from initial separation r₀ is exp(−r_c/r₀), obtained by integrating the radial flux equation with the Coulomb drift and absorbing boundary at infinity. Setting r₀ = a gives the bound; any additional loss channel (deep CT state, back-transfer) only reduces it. ∎

For ε_r = 3.5, a = 1 nm: r_c = 16.1 nm, 𝔠 = 16.1, e^{−𝔠} = 1.0×10⁻⁷. **Isolated dopants in a low-permittivity organic solid are essentially unionized.** Doping nevertheless works, at efficiencies of 1–50%, because dopants are never isolated. The next theorem supplies the mechanism.

**Theorem 3.9 (Dopant-overlap ionization threshold).** Let ionized dopants have density N with mean spacing R = N^{−1/3}. In the superposed Coulomb landscape of two neighbouring centres, the escape barrier from a site at distance a from one centre is

  ΔU/k_BT = 𝔠 (1 − 4a/R),  (3.7)

vanishing at R = 4a. Hence complete ionization for

  N ≥ N* = (4a)^{−3},  and  η_dop ≈ exp[−𝔠(1 − 4a N^{1/3})] for N < N*.  (3.8)

For a = 1 nm, N* = 1.56×10²⁵ m⁻³ = 1.6×10¹⁹ cm⁻³.

*Proof.* Two positive centres at 0 and R give electron potential energy U(x) = −(q²/4πε)[1/x + 1/(R−x)] along the connecting line. The saddle is at the midpoint x = R/2 with U = −4q²/(4πεR). The bound state is cut off at x = a with U ≈ −q²/(4πεa). Hence

  ΔU = U(R/2) − U(a) = (q²/4πε)(1/a − 4/R) = k_BT r_c(1/a − 4/R) = k_BT 𝔠(1 − 4a/R).

Thermal escape over the saddle gives (3.8); at R = 4a the barrier vanishes and every dopant ionizes. ∎

**Corollary 3.10 (Derived design rules).**

1. The threshold N* ≈ 10¹⁹ cm⁻³ is precisely the empirically observed onset of efficient molecular doping [9–11]. The theory reproduces it from ε, a, and T alone.
2. N* ∝ a⁻³ and 𝔠 ∝ ε⁻¹: **high-permittivity hosts dop at lower concentrations**, with η_dop exponentially sensitive to ε. Raising ε_r from 3.5 to 10 reduces 𝔠 from 16 to 5.6 and raises the isolated-dopant efficiency from 10⁻⁷ to 3.7×10⁻³ — a 37000-fold improvement.
3. Dopants with large, delocalized counter-ion charge distributions increase the effective r₀ (the charge centroid is further from the carrier), directly attacking the exponent in (3.6). This is the correct rationale for bulky weakly-coordinating dopants.

### 3.5 The conductivity maximum

Doping adds carriers but also adds Coulomb disorder. There is therefore an optimum.

**Claim 3.11 (Conductivity optimum; asymptotic under stated closure).** Model the dopant-induced energetic disorder as the RMS of the superposed Coulomb potential of randomly placed ionized centres, cut off at the mean spacing R = N^{−1/3}:

  σ_C² = (q²/4πε)² N ∫₀^R 4πr² dr/r² = 4π (q²/4πε)² N^{2/3}.  (3.9)

With μ ∝ exp[−c(σ₀²+σ_C²)/(k_BT)²] and n = ηN, the conductivity σ_el = qnμ is maximized at

  N_opt = [3/(2B)]^{3/2},  B = 4πc 𝔠² a²,  hence N_opt ∝ c^{−3/2} 𝔠⁻³ a⁻³ ∝ ε³.  (3.10)

*Closure and argument.* Equation (3.9) treats the Coulomb landscape as uncorrelated and Gaussian, cutting the divergent integral at R. Substituting into the disorder exponent gives ln σ_el = ln(qημ₀N) − c σ₀²/(k_BT)² − B N^{2/3}. Setting d/dN = 0: 1/N = (2/3)B N^{−1/3}, so N^{2/3} = 3/(2B). ∎ (closure)

**Sharpness caveat.** With c = 4/9, 𝔠 = 16, a = 1 nm, (3.10) gives N_opt ≈ 3×10¹⁶ cm⁻³, two to three decades below observed optima. We regard this as a genuine failure of the *uncorrelated-Gaussian* closure, not of the scaling: the Coulomb landscape of a random charge array is strongly spatially correlated, and correlated disorder is far less effective at localizing than uncorrelated disorder of the same variance. **Open Problem 1.** Compute the localization exponent for a correlated Coulomb landscape and determine the effective c. The scaling N_opt ∝ ε³ is unaffected and is itself a strong prediction.

### 3.6 Injection and space-charge-limited transport

**Theorem 3.12 (Mott–Gurney).** For trap-free, field-independent, unipolar injection-limited-free transport across a film of thickness d with an ohmic injecting contact,

  J = (9/8) ε μ V²/d³.  (3.11)

*Proof.* With ρ = ε dE/dx and J = qμnE = μρE = μεE dE/dx, integrate: ½εμE² = Jx (E(0) = 0 at the ohmic contact). So E(x) = √(2Jx/(εμ)) and V = ∫₀^d E dx = (2/3)√(2J/(εμ)) d^{3/2}. Solving gives (3.11). ∎

**Theorem 3.13 (Mark–Helfrich trap-limited SCLC).** Let the trap distribution be exponential with characteristic energy E_c, l ≡ E_c/k_BT = 1/α > 1, transport-edge effective density N_v, total trap density N_t, and let trapped charge dominate free charge. Then

  J = q^{1−l} μ N_v [ε l/(N_t(l+1))]^l [(2l+1)/(l+1)]^{l+1} V^{l+1}/d^{2l+1}.  (3.12)

*Proof.* From the filling law [I, Lemma 4.10], n_f = N_v e^{βζ} and n_t = N_t e^{ζ/E_c}, so n_f = N_v(n_t/N_t)^l. Poisson in the trap-dominated limit: dE/dx = qn_t/ε. Current continuity: J = qμ n_f E, so n_t = N_t(J/(qμN_v E))^{1/l}. Hence

  E^{1/l} dE = A dx,  A ≡ (qN_t/ε)(J/(qμN_v))^{1/l}.

Integrating with E(0) = 0: (l/(l+1))E^{(l+1)/l} = Ax, so E(x) = [(l+1)Ax/l]^{l/(l+1)}. Then

  V = ∫₀^d E dx = [(l+1)A/l]^{l/(l+1)} · (l+1)/(2l+1) · d^{(2l+1)/(l+1)}.

Inverting for A and substituting into J = qμN_v(Aε/(qN_t))^l yields (3.12) after collecting powers. ∎

**Corollary 3.14 (Two independent handles on α).** The SCLC exponent is m = l + 1 = 1 + 1/α, and the thickness exponent is 2l+1 = 2m−1. Measuring the *pair* (m, thickness exponent) overdetermines α and tests the exponential-tail hypothesis: any deviation from 2m−1 falsifies it. Combined with §9.4 this becomes a four-fold test.

**Definition 3.15 (Injection number).** Θ ≡ J_inj(E)/J_SCLC(E) at the operating field, with J_inj the contact's supply capability. Θ ≪ 1: injection-limited; Θ ≫ 1: space-charge-limited (contact effectively ohmic).

**Proposition 3.16 (Schottky injection and the ohmic criterion).** With image-force lowering, the thermionic supply is

  J_inj = A*T² exp[−β(Φ_B − ΔΦ)],  ΔΦ = √(qE/(4πε)),  (3.13)

so ln J_inj is linear in √E (equivalently √V at fixed d). The contact is ohmic (Θ ≥ 1) when

  Φ_B ≤ k_BT ln(A*T²/J_SCLC) + √(qE/(4πε)).  (3.14)

*Proof.* The image potential −q²/(16πεx) plus the applied −qEx is maximized at x_m = √(q/(16πεE)), where both terms equal −q√(qE/(16πε))/... evaluating gives barrier reduction qΔΦ with ΔΦ = √(qE/(4πε)). Substituting into Richardson–Dushman and imposing Θ ≥ 1 gives (3.14). ∎

**Corollary 3.17.** At E = 10⁸ V m⁻¹ and ε_r = 3.5, ΔΦ = 0.20 V. At 300 K with J_SCLC = 10³ A m⁻² and A*T² ≈ 10⁹ A m⁻², k_BT ln(10⁶) = 0.36 V, so the ohmic criterion is Φ_B ≲ 0.56 V. **Barriers below ~0.5 eV are ohmic at operating fields; barriers above ~0.8 eV are not.** This is the quantitative content of "energy-level alignment."

### 3.7 Contact engineering by dipole layers

**Proposition 3.18 (Helmholtz shift).** An oriented interfacial dipole sheet of areal density N_dip and normal moment component p_⊥ shifts the vacuum level by

  Δφ = N_dip p_⊥/(ε₀ε_r).  (3.15)

For Δφ = 0.5 V, p_⊥ = 1 D, ε_r = 3: N_dip = 4.0×10¹⁸ m⁻² = 4×10¹⁴ cm⁻² — approximately one monolayer.

*Proof.* A dipole sheet is a double layer; the potential step across it follows from Gauss's law applied to the two charge sheets, giving (3.15). Numerical substitution is direct. ∎

**Design rule.** A self-assembled monolayer of ~1 D oriented molecules is sufficient to move a metal work function by half an electronvolt — enough to convert a non-ohmic contact to ohmic by (3.14). This is why SAM treatment is the highest-yield-per-effort contact intervention available, and why it saturates: once a monolayer is complete, N_dip cannot increase.

---

## 4. Process Engineering: From Ink to Microstructure

### 4.1 Drying and vertical stratification

**Theorem 4.1 (Stratification factor).** Consider a drying film of instantaneous thickness H with a receding free surface at evaporation velocity v_ev, a non-volatile solute of diffusivity D, no flux through the substrate, and local equilibrium rejection at the surface. In the quasi-steady surface frame the solute profile is φ(ξ) = φ_s e^{−v_ev ξ/D} with ξ measured from the surface, and the surface enrichment is

  **φ_s/φ̄ = Pe/(1 − e^{−Pe}),  Pe ≡ v_ev H/D.**  (4.1)

*Proof.* Solute conservation at the receding surface requires the diffusive flux away from the surface to balance the convective accumulation: D ∂φ/∂ξ|₀ = v_ev φ_s (signs chosen with ξ into the film). The quasi-steady advection–diffusion equation in the surface frame, D φ″ + v_ev φ′ = 0, gives φ = φ_s e^{−v_ev ξ/D}. Averaging,

  φ̄ = (1/H)∫₀^H φ_s e^{−v_ev ξ/D}dξ = φ_s (D/(v_ev H))(1 − e^{−Pe}) = φ_s(1−e^{−Pe})/Pe.

Inverting gives (4.1). ∎

**Corollary 4.2 (Skinning criterion).** For Pe ≪ 1, φ_s/φ̄ → 1 (uniform film). For Pe ≫ 1, φ_s/φ̄ → Pe (surface skin). The design rule is

  **Pe < 1 ⟺ v_ev < D/H.**  (4.2)

With D = 10⁻¹⁰ m² s⁻¹ (small molecule in a good solvent) and wet thickness H = 10 µm: v_ev < 10⁻⁵ m s⁻¹ = 10 µm s⁻¹. Typical spin-coating evaporation rates are 1–100 µm s⁻¹, so Pe spans 0.1–10: **the process operates precisely across the stratification transition**, which is why solvent choice and atmosphere control dominate reproducibility.

**Corollary 4.3 (Vertical composition control in blends).** For a binary blend with D₁ ≫ D₂ (e.g., fullerene versus polymer), the slow component enriches at the surface by (4.1) while the fast component remains uniform. Since the OFET channel is the *bottom* 1–2 nm [I, Cor 3.5] and the OPV/OLET contacts are at both surfaces, **the same ink produces different devices depending on Pe alone**. Deliberate use of Pe > 1 to place the semiconductor at the dielectric interface is a legitimate and underused design strategy.

### 4.2 Coffee-ring flow and Marangoni reversal

**Proposition 4.4 (Deegan flow).** For a pinned contact line at radius R with evaporative flux J(r) ∝ (R−r)^{−λ}, λ = (π−2θ_c)/(2π−2θ_c) (θ_c the contact angle), mass conservation with a pinned edge forces an outward radial flow

  ū(r) ∝ (1/(ρ H(r))) ∫₀^r J(r′) r′ dr′,  (4.3)

divergent at the edge, transporting solute to the perimeter and producing a ring deposit.

*Proof.* The flux singularity follows from the Laplace problem for vapour concentration with the same boundary geometry as the electrostatic problem of a charged disc, whose edge singularity is (R−r)^{−λ} with the stated exponent [19,20]. Height-averaged mass conservation with a pinned contact line (no recession allowed) forces the depth-integrated radial flux to equal the integrated evaporative loss inside r, giving (4.3). ∎

**Definition 4.5 (Marangoni number).** Ma ≡ |dγ/dT| ΔT H/(η D_s) (thermal) or |dγ/dc| Δc H/(η D_s) (solutal), with ΔT, Δc the surface-driven gradients, η viscosity, D_s solute diffusivity.

**Claim 4.6 (Reversal criterion; closure).** Ring formation is suppressed when the Marangoni recirculation velocity exceeds the Deegan outward velocity at the edge, i.e. Ma > Ma_c with Ma_c = O(1) set by the contact-angle geometry. *Closure:* the recirculation velocity scales as u_Ma ~ |dγ/dT|ΔT/(η) · (H/L) and the comparison is made at r ≈ R − H. The O(1) constant is geometry-dependent and must be calibrated per ink. ∎ (closure)

**Design rules.** (i) Depin the contact line (surfactant, substrate patterning) — removes the constraint that generates (4.3). (ii) Use a binary solvent with a high-boiling, low-surface-tension component to generate an inward solutal Marangoni flow. (iii) Increase η (polymer additive) to suppress both flows and rely on diffusion — at the cost of raising Pe.

### 4.3 Jettability: the Ohnesorge window

**Proposition 4.7 (Printability window).** For a nozzle of radius a_n and ink with viscosity η, density ρ, surface tension γ, define

  Oh = η/√(ργ a_n),  Z = 1/Oh.  (4.4)

Reliable single-droplet ejection requires approximately 1 ≲ Z ≲ 10.

*Proof of the two bounds.* The capillary (Rayleigh) time is τ_c = √(ρa_n³/γ) and the viscous–capillary time τ_v = ηa_n/γ; Oh = τ_v/τ_c. **Lower Z bound (Oh large):** ejection requires the imposed pressure pulse to do work against viscous dissipation within a capillary time; when τ_v ≫ τ_c the ligament cannot thin and no drop detaches. **Upper Z bound (Oh small):** an inviscid ligament is Rayleigh–Plateau unstable with fastest-growing wavelength λ_RP ≈ 9.02 a_n and growth rate ~ τ_c^{−1}; when viscosity is too low, the trailing ligament breaks into multiple satellites rather than coalescing with the main drop. Both bounds are ratios of the same two timescales, hence a window in Z. The numerical bounds 1 and 10 are empirical calibrations of the O(1) constants [21,22]. ∎

**Corollary 4.8 (Feature resolution).** The deposited dot diameter is set by the drop volume and the equilibrium contact angle: d_dot = (6V_drop/π · f(θ_c))^{1/3} with f the spherical-cap factor. Since V_drop ≳ a_n³ and a_n ≳ 5 µm for reliable jetting at typical ink properties, **inkjet resolution is bounded near 10–20 µm**, an order of magnitude above the OFET scale length λ ≈ 100 nm [I, Prop 6.3]. Printed organic circuits are therefore *not* short-channel-limited; they are *registration-limited* (§4.6, §10.3).

### 4.4 The coating-speed ceiling

**Theorem 4.9 (Throughput–quality constraint).** In continuous coating with an oven of length L_oven, wet thickness H, solute diffusivity D, and evaporation velocity v_ev, the line speed v satisfies

  v ≤ L_oven v_ev/H  (complete drying)  and  v ≤ L_oven D/H²  (no skinning, Pe < 1).  (4.5)

The second is binding whenever v_ev > D/H.

*Proof.* Residence time is L_oven/v; drying time is H/v_ev; equating gives the first bound. Imposing (4.2), v_ev ≤ D/H, and substituting gives the second. ∎

**Numbers.** L_oven = 5 m, D = 10⁻¹⁰ m² s⁻¹, H = 10 µm: v ≤ 5 m s⁻¹ (300 m min⁻¹) — not binding. H = 100 µm: v ≤ 0.05 m s⁻¹ (3 m min⁻¹) — binding. **The H⁻² scaling is the fundamental throughput penalty for thick films**, and it compounds the OECT design tension: thick films give gain [I, Cor 8.2] but cost throughput quadratically and bandwidth linearly [I, Lemma 8.4].

### 4.5 Morphology metastability

Blend morphology is kinetically trapped, not equilibrium. Coarsening follows Lifshitz–Slyozov–Wagner kinetics for diffusion-limited Ostwald ripening,

  R(t)³ − R₀³ = K t,  K ∝ D γ_int c_eq V_m²/(RT),  (4.6)

with γ_int the interfacial energy and c_eq the equilibrium solubility of the dispersed phase.

**Proposition 4.10 (Retention criterion).** For domain growth not to exceed a fraction f of R₀ over lifetime t_life,

  D ≤ f³ R₀³/(K̂ t_life),  K̂ = K/D.  (4.7)

With R₀ = 15 nm, f = 0.2 (20% growth), t_life = 10 yr = 3.2×10⁸ s: ΔR³ ≈ 0.73 R₀³ = 2.5×10⁻²⁴ m³, requiring K ≤ 7.7×10⁻³³ m³ s⁻¹.

**Design rule (glass-transition margin).** Since D in the amorphous matrix follows Vogel–Fulcher rather than Arrhenius near T_g, the practical criterion is **T_g ≥ T_op + 50 K**, with crosslinking or high-T_g side chains as the lever. This is a *kinetic* stabilization, not thermodynamic: the morphology is never stable, only slow.

### 4.6 Registration and the variability law

**Theorem 4.11 (Registration-limited variability).** Let overlay/placement error have standard deviation σ_reg, independent of feature size. For a printed transistor with channel length L and width W,

  (σ_I/I)² ≈ (σ_reg/L)² + (σ_reg/W)² + (σ_μ/μ)² + (σ_{C_i}/C_i)² + 4(σ_A/A)².  (4.8)

The geometric terms scale as **1/L and 1/W**, not as 1/√(WL).

*Proof.* I_sat ∝ (W/L)μC_iA²; take log-differentials and add independent variances. The geometric contributions are δL/L and δW/W with δL, δW ~ σ_reg fixed by the tool, not by the feature. ∎

**Corollary 4.12 (Contrast with Pelgrom).** In lithographic silicon, edge roughness averages down over the feature perimeter, giving σ_Vth ∝ 1/√(WL) [46]. In printing, the error is a *rigid placement offset* that does not average with feature size. Consequences:

1. **Averaging over area does not help.** Paralleling N identical devices reduces the random component as N^{−1/2} but not the systematic overlay component at all.
2. **Only increasing L helps, linearly.** Doubling L halves the geometric variability but quarters f_T [I, Cor 9.3]. This is the printed-circuit speed–matching trade-off, and it is *not* the silicon one.
3. Self-aligned printing (surface-energy patterning, dewetting-defined gaps) removes σ_reg from L entirely and is therefore worth more than any mobility improvement of comparable effort.

---

## 5. Emissive Devices: Outcoupling, Roll-off, and the Microcavity Trade-off

### 5.1 Efficiency factorization

**Proposition 5.1.** The external quantum efficiency factorizes as

  EQE = γ · η_r · Φ_PL · η_out,  (5.1)

with γ the charge-balance factor (fraction of injected carriers forming excitons), η_r the fraction of excitons in emissive states (1/4 for spin-statistical fluorescence, 1 for phosphorescence or efficient TADF), Φ_PL the effective photoluminescence quantum yield in the stack, and η_out the outcoupling fraction.

*Proof.* Sequential conditional probabilities along the chain injection → exciton formation → emissive-state population → radiative decay → photon escape; independence is exact by construction of the conditional factors. ∎

**Warning (identifiability).** Electrical-plus-optical measurement determines only the product η_outΦ_PL (§2.3c). Reporting "η_out = 20%" without an independent Φ_PL or an optical model is a fibre coordinate presented as a point.

### 5.2 The dipole orientation tensor and the Green dyadic

**Definition 5.2 (Orientation tensor).** Let **p** be the transition dipole unit vector of an emitter. Define

  Θ^{ij} = ⟨p^i p^j⟩,  tr Θ = 1,  Θ_h ≡ Θ^{11} + Θ^{22} = 1 − Θ^{33}.  (5.2)

Isotropic: Θ = δ^{ij}/3, Θ_h = 2/3. Perfectly in-plane: Θ = diag(½,½,0), Θ_h = 1. Θ_h is measurable by angle-resolved polarized emission.

**Theorem 5.3 (Exact rates over a perfect mirror).** For an emitter of index n at distance d from a perfectly conducting plane, with u ≡ 2k(2d)... writing u = 4πn d/λ₀ (the round-trip phase), the normalized decay rates for dipoles parallel and perpendicular to the plane are

  Γ_∥/Γ₀ = 1 − (3/2)[ sin u/u − sin u/u³ + cos u/u² ],  (5.3)
  Γ_⊥/Γ₀ = 1 + 3[ sin u/u³ − cos u/u² ].  (5.4)

*Proof.* The decay rate is proportional to Im[**p**·𝔾(**r**,**r**)·**p**]. Split 𝔾 into free-space plus reflected; the reflected part equals the free-space dyadic evaluated at the image position, distance 2d along ẑ, with image sign s = −1 for parallel and s = +1 for perpendicular components. The free-space dyadic is

  𝔾_ij(r) = (e^{ikr}/(4πk²r³))[(k²r² + ikr − 1)δ_ij + (−k²r² − 3ikr + 3)r̂_i r̂_j].

For r̂ = ẑ and u = k(2d):

  Im 𝔾_xx = (1/(4πk²r³))[(u²−1)sin u + u cos u],  Im 𝔾_zz = (1/(4πk²r³))[2 sin u − 2u cos u].

Using k²r³ = 8k²d³ = u³/k, these become (k/(4πu³))[…] and (k/(4πu³))[…]. Normalizing by the free-space value Im 𝔾_xx(0) = k/(6π) gives the factors (3/(2u³))[(u²−1)sin u + u cos u] and (3/u³)[sin u − u cos u]. Adding with the image signs yields (5.3)–(5.4). ∎

**Checks.** u → 0: Γ_∥ → 0 (parallel dipole quenched by its image), Γ_⊥ → 2 (perpendicular dipole doubled). Both are the correct electrostatic limits. ∎

**Corollary 5.4 (Orientation-resolved rate).**

  Γ/Γ₀ = Θ_h Γ_∥/Γ₀ + (1 − Θ_h) Γ_⊥/Γ₀.  (5.5)

*Proof.* Θ^{11} = Θ^{22} = Θ_h/2 by in-plane isotropy; contract with the diagonal rate dyadic. ∎

### 5.3 The outcoupling orientation bound

**Theorem 5.5 (Escape-cone capture).** In a medium of index n with escape cone θ_c = arcsin(1/n), c ≡ cos θ_c = √(1−n^{−2}), the fraction of emitted power inside one escape cone is

  F_h = ½ − (3/8)c − (1/8)c³  (Θ_h = 1),
  F_v = ½ − (3/4)c + (1/4)c³  (Θ_h = 0),
  F(Θ_h) = Θ_h F_h + (1−Θ_h)F_v = (1−c)/2 + (3c/(8n²))(Θ_h − 2/3).  (5.6)

*Proof.* The normalized angular power densities are p_h(θ) = 3(1+cos²θ)/(16π) (φ-averaged in-plane dipole) and p_v(θ) = 3sin²θ/(8π) (normal dipole); both integrate to unity over 4π. Integrating 2π sinθ dθ from 0 to θ_c:

  F_h = (3/8)[4/3 − c − c³/3],  F_v = (3/4)[2/3 − c + c³/3],

giving the stated forms. Consistency: (2/3)F_h + (1/3)F_v = (1−c)/2, the isotropic result ✓. The difference F_h − F_v = (3/8)c(1−c²) = 3c/(8n²) gives the linear form. ∎

**Theorem 5.6 (Sharp orientation bound).** The enhancement of escape-cone capture by purely horizontal versus isotropic dipoles is

  **ρ(n) = F_h/F_iso = (c² + c + 4)/4,  c = √(1 − n^{−2}),**  (5.7)

monotonically increasing in n, with ρ(1) = 1 and **ρ(∞) = 3/2**.

*Proof.* Divide (5.6) by (1−c)/2: ρ = [1 − (3/4)c − (1/4)c³]/(1−c). Factor the numerator: 1 − (3/4)c − (1/4)c³ = (1/4)(1−c)(c²+c+4), verified by expansion. Cancel (1−c). Monotonicity: c increases with n and (c²+c+4)/4 increases in c. Limits: c → 0 gives 1; c → 1 gives 6/4. ∎

**Corollary 5.7 (Engineering bound).** For n = 1.5, ρ = 1.33; for n = 1.8, ρ = 1.38; asymptotically 1.50. **Perfect horizontal orientation can improve outcoupling by at most 50%, and realistically by 30–40%.** A device claiming η_out = 40% from 20% by orientation alone has exceeded the bound and must be invoking a different mechanism (microcavity redistribution, scattering structure, index matching).

**Sharpness.** Theorem 5.6 is a ray-optics escape-cone bound; it neglects waveguided and plasmonic channels, which reduce absolute η_out but affect the *ratio* less. Full dyadic-Green computation in the actual stack is required for absolute values; the bound is on the orientation lever, not on total achievable η_out (which can exceed 30% with extraction structures).

### 5.4 Efficiency roll-off: exact solution

**Theorem 5.8 (TTA roll-off curve).** Let triplets be generated at rate G = J/(qw) in a recombination zone of width w, decay with lifetime τ, and annihilate bimolecularly with rate constant k_TT (½k_TT T² loss). In steady state,

  J_{1/2} = 4 q w/(k_TT τ²),  **η(J)/η₀ = 2/[1 + √(1 + 8J/J_{1/2})].**  (5.8)

*Proof.* Steady state: G = T/τ + ½k_TT T². The radiative fraction is η/η₀ = (T/τ)/G = 1/(1 + ½k_TTτT). Set u = ½k_TTτT; then T = 2u/(k_TTτ) and

  G = 2u/(k_TTτ²) + 2u²/(k_TTτ²) ⟹ J = qwG = (2qw/(k_TTτ²))(u + u²).

Half efficiency occurs at u = 1, giving J_{1/2} = 4qw/(k_TTτ²). Writing J/J_{1/2} = (u+u²)/2 and solving the quadratic, u = [−1 + √(1+8J/J_{1/2})]/2, so η/η₀ = 1/(1+u) = 2/[1+√(1+8J/J_{1/2})]. ∎

**Corollary 5.9 (Roll-off design levers).** J_{1/2} ∝ w/(k_TTτ²). Three levers: widen the recombination zone (double-emitter or graded host), shorten τ (Purcell enhancement, §5.5), reduce k_TT (spatially separate emitters, dilute doping — at the cost of charge trapping). The **quadratic** dependence on τ makes lifetime engineering the strongest lever.

### 5.5 The outcoupling–Purcell trade-off

Both η_out and the Purcell factor F_P = Γ/Γ₀ depend on the emitter–cathode distance d through u = 4πnd/λ₀. They are not independently optimizable.

**Theorem 5.10 (Current-weighted optimum).** Let the emitter be radiatively dominated so τ ≈ τ_rad/F_P, hence J_{1/2} ∝ F_P². Define s ≡ √(1 + 8J/J_{1/2}) and ω ≡ (s−1)/(2s) ∈ [0,½). Then the total efficiency η(J,d) = η_out(d)·η₀·2/(1+s) is stationary in d iff

  **d ln η_out/dd + 2ω(J) · d ln F_P/dd = 0.**  (5.9)

In particular: as J → 0, ω → 0 and the optimum maximizes η_out alone; as J → ∞, ω → ½ and the optimum maximizes the **product η_out·F_P**.

*Proof.* ln η = ln η_out − ln(1+s) + const. Differentiate: d ln η/dd = d ln η_out/dd − (1+s)^{−1} ds/dd. From s² = 1 + 8J/J_{1/2}, 2s ds/dd = −8J J_{1/2}^{−1} d ln J_{1/2}/dd, so ds/dd = −(4J/(sJ_{1/2})) d ln J_{1/2}/dd. Hence

  d ln η/dd = d ln η_out/dd + [4J/((1+s)sJ_{1/2})] d ln J_{1/2}/dd.

Using 8J/J_{1/2} = s²−1, the bracket equals (s²−1)/(2s(1+s)) = (s−1)/(2s) = ω. With J_{1/2} ∝ F_P², d ln J_{1/2}/dd = 2 d ln F_P/dd, giving (5.9). Limits follow from s → 1 and s → ∞. ∎

**Corollary 5.11 (Practical consequence).** The optimal cavity thickness for a display pixel (J ~ 1–10 mA cm⁻²) and for a lighting panel or laser diode (J ~ 1–100 A cm⁻²) are *different*, and the shift is calculable from (5.9) with (5.3)–(5.4). Reporting a single "optimized thickness" without stating the current density is incomplete. This theorem also explains why bright, low-roll-off devices frequently sit at a cavity position that is suboptimal for small-signal EQE.

### 5.6 Operational degradation

**Claim 5.12 (Degradation order; closure).** If the degradation rate is proportional to the product of exciton and polaron densities (exciton–polaron annihilation producing hot, bond-breaking states), then in steady state X ∝ J and P ∝ J^{1/2} (space-charge) or P ∝ J (ohmic), giving degradation rate ∝ J^{3/2} or J². Since lifetime is inversely proportional to degradation rate at fixed accumulated damage,

  LT50 ∝ J^{−n},  n ∈ [1, 2].  (5.10)

*Closure:* the identification of the damaging species with the exciton–polaron product, and the assumption of a fixed critical damage dose. Observed acceleration exponents n ≈ 1.5–1.8 for phosphorescent OLEDs are consistent with the intermediate case. ∎ (closure)

**Testable content.** The exponent n is a *mechanism diagnostic*: n = 1 indicates unimolecular (pure exciton) degradation; n = 2 indicates bimolecular exciton–polaron. Measuring n across a decade of J and correlating with emitter/host energetics is a decisive experiment that is rarely performed.

---

## 6. Photovoltaic Devices: Geometry, Voltage, and the Urbach Threshold

### 6.1 Exciton harvesting in a domain: exact solution

**Theorem 6.1 (Spherical harvesting).** Let excitons be generated uniformly at rate G in a sphere of radius R, diffuse with D_X, decay with lifetime τ_X (L_D = √(D_Xτ_X)), and be quenched perfectly at the surface. The fraction reaching the surface is

  **η_harv(x) = (3/x)[coth x − 1/x],  x ≡ R/L_D.**  (6.1)

Asymptotics: η_harv = 1 − x²/15 + O(x⁴) for x ≪ 1; η_harv = 3/x − 3/x² + O(e^{−x}) for x ≫ 1.

*Proof.* Steady diffusion–reaction: D_X∇²n − n/τ_X + G = 0 with n(R) = 0 and regularity at 0. The solution is

  n(r) = Gτ_X[1 − (R/r) sinh(r/L_D)/sinh(R/L_D)].

The fraction lost to bulk decay is (1/(GV))∫ n/τ_X dV, so the harvested fraction is

  η_harv = (1/V)∫ (R/r) sinh(r/L_D)/sinh x dV = (3/(R² sinh x))∫₀^R r sinh(r/L_D)dr.

Evaluating ∫₀^R r sinh(r/L_D)dr = L_D R cosh x − L_D² sinh x and simplifying gives (6.1). The small-x expansion uses coth x = 1/x + x/3 − x³/45 + …; the large-x limit uses coth x → 1. ∎

**Corollary 6.2.** η_harv ≥ 0.9 requires x ≤ 1.2, i.e. R ≤ 1.2 L_D. With L_D = 5–20 nm for typical organic semiconductors, this is the origin of the 10–20 nm domain requirement — derived here with the exact prefactor rather than asserted.

### 6.2 Charge collection: the two-carrier Hecht identity

**Theorem 6.3.** Let electron and hole drift lengths be λ_n = μ_nτ_nV/d, λ_p = μ_pτ_pV/d, with uniform generation across thickness d and collection at opposite electrodes. Under Ramo's theorem with exponential trapping,

  η_coll = g(λ_n) + g(λ_p),  g(λ) ≡ (λ/d) − (λ/d)²(1 − e^{−d/λ}).  (6.2)

Limits: for λ ≫ d, g → ½ − d/(6λ); for λ ≪ d, g → λ/d.

*Proof.* A carrier generated at x with distance x to its collecting electrode travels a distance s ~ Exp(λ) before trapping; by Ramo the induced charge is min(s,x)/d, with expectation (λ/d)(1 − e^{−x/λ}). Averaging over uniform x ∈ [0,d]:

  (1/d)∫₀^d (λ/d)(1−e^{−x/λ})dx = (λ/d²)[d − λ(1−e^{−d/λ})] = g(λ).

The two carrier types contribute additively with x and d−x respectively, and by symmetry both averages equal g. ∎

**Corollary 6.4 (Balanced-transport requirement).** For λ_n = λ_p = λ ≫ d, η_coll ≈ 1 − d/(3λ). For strongly imbalanced transport, λ_p ≪ λ_n, η_coll ≈ ½ + λ_p/d: **half the photogenerated charge is lost regardless of how good the fast carrier is.** This is the quantitative statement of why mobility balance, not mobility magnitude, governs fill factor.

### 6.3 The optimal domain size

**Claim 6.5 (Optimal morphology; asymptotic under stated closure).** Let bimolecular recombination be interface-limited so that τ_rec ∝ R (interfacial area per volume ∝ 1/R), giving λ = βR with β ≡ μτ₀V/(dR₀) dimensionless. In the regime R ≪ L_D and λ ≫ d,

  η_IQE ≈ [1 − R²/(15L_D²)]·[1 − d/(3βR)],

minimized-loss at

  **R* = (5 L_D² d/(2β))^{1/3} ∝ (L_D² d)^{1/3}.**  (6.3)

*Closure and argument.* The identification τ_rec ∝ R assumes recombination occurs predominantly at donor–acceptor interfaces and that carrier densities are morphology-independent. Expanding the product to first order in each loss and differentiating: 2R/(15L_D²) = d/(3βR²), so R³ = 5L_D²d/(2β). ∎ (closure)

**Numbers.** L_D = 10 nm, d = 100 nm, β = 10: R* = 13.6 nm — the observed optimum. **Design content:** the optimal domain size grows as the *cube root* of thickness, so thicker cells (for absorption) require coarser morphology, and the tolerance is weak (a factor 8 in d requires only a factor 2 in R). Conversely, materials with longer L_D (non-fullerene acceptors, L_D ≈ 20–40 nm) permit proportionally coarser, more stable, more crystalline morphologies — a *derived* rationale for the NFA revolution.

### 6.4 The voltage budget

**Proposition 6.6 (Reciprocity and non-radiative loss).** By Rau's reciprocity between photovoltaic quantum efficiency and electroluminescent emission [29],

  E_g/q = V_oc + ΔV_rad + ΔV_nr,  **ΔV_nr = (k_BT/q) ln(1/EQE_EL).**  (6.4)

*Proof.* Detailed balance relates the dark saturation current to the integrated blackbody-weighted EQE_PV; the radiative open-circuit voltage V_oc,rad follows from J_sc/J_0,rad. Non-radiative recombination multiplies J_0 by 1/EQE_EL, shifting V_oc by −(k_BT/q)ln(1/EQE_EL). ∎

**Numbers.** EQE_EL = 10⁻⁴ → ΔV_nr = 0.238 V; 10⁻⁶ → 0.357 V; 10⁻⁹ → 0.536 V. Organic cells with EQE_EL ~ 10⁻⁶–10⁻⁸ thus lose 0.36–0.48 V non-radiatively, the dominant single loss in the field.

**Claim 6.7 (Energy-gap-law slope; closure).** For charge-transfer states with non-radiative rate governed by the energy-gap law, k_nr ∝ exp(−γ_E E_CT/ħω_eff), (6.4) gives ΔV_nr = (k_BT/q)(γ_E E_CT/ħω_eff + const), hence

  **dV_oc/dE_CT = (1/q)(1 − γ_E k_BT/ħω_eff).**  (6.5)

With ħω_eff ≈ 0.17 eV (C=C stretch) and γ_E ≈ 1, the slope is 0.85 — matching the observed sub-unity slope of V_oc versus gap [30,31]. *Closure:* single effective mode, linear gap law, E_CT-independent prefactor. ∎ (closure)

**Design rule.** The lever is ħω_eff: **deuteration or rigidification that lowers the dominant accepting mode frequency raises the slope toward unity** and reduces ΔV_nr at fixed gap. This is a molecular, not a morphological, intervention.

### 6.5 The Urbach threshold theorem

Let the sub-gap absorption be exponential with Urbach energy E_U over a spectral extent Δ_tail below the gap: EQE(E) = exp[(E−E_g)/E_U] for E_g − Δ_tail ≤ E < E_g.

**Theorem 6.8 (Urbach voltage penalty).** In the Wien limit φ_bb ∝ E²e^{−E/k_BT}, the radiative dark current acquires an enhancement factor exp[Δ_tail(1/k_BT − 1/E_U)] when E_U > k_BT, and no enhancement when E_U ≤ k_BT. Hence

  **ΔV_U = (Δ_tail/q)·(1 − k_BT/E_U)_+ ,**  (6.6)

with (·)_+ the positive part. In particular the penalty vanishes identically for E_U ≤ k_BT = 25.9 meV at 300 K.

*Proof.* The dark-current integrand below the gap is

  I(E) ∝ exp[(E−E_g)/E_U − E/k_BT] = e^{−E_g/E_U} e^{bE},  b ≡ 1/E_U − 1/k_BT.

If b > 0 (E_U < k_BT), I increases with E and the integral is dominated by the upper limit E_g, contributing ≈ I(E_g)/b = e^{−E_g/k_BT}/b: the same exponential as an ideal step absorber, with only a prefactor change. If b < 0 (E_U > k_BT), I decreases with E and the integral is dominated by the lower limit E_g − Δ_tail, contributing ≈ exp[−E_g/k_BT + Δ_tail(1/k_BT − 1/E_U)]/|b|. The enhancement relative to the ideal case is the stated exponential; converting to a voltage via (k_BT/q)ln(·) gives (6.6). ∎

**Corollary 6.9 (Sharp engineering target).** With Δ_tail = 0.2 eV and E_U = 50 meV, ΔV_U = 0.2(1 − 0.518) = 0.096 V. With E_U = 30 meV, ΔV_U = 0.027 V. With E_U = 25 meV, ΔV_U = 0.

**There is a hard threshold at E_U = k_BT, below which further disorder reduction yields no voltage benefit.** This converts "reduce disorder" from an open-ended aspiration into a bounded, falsifiable target: **drive E_U below 26 meV, then stop optimizing it and work on EQE_EL instead.** The two levers are not interchangeable, and (6.6) tells you which one is currently binding.

### 6.6 Thickness–absorption trade-off

**Proposition 6.10.** With absorption coefficient α_abs and a reflecting back electrode, J_sc ∝ (1 − e^{−2α_abs d}) while η_coll decreases with d (Theorem 6.3) and R* increases with d (Claim 6.5). The product is maximized at a thickness d* satisfying

  2α_abs e^{−2α_abs d*}/(1 − e^{−2α_abs d*}) = −∂ln η_coll/∂d.  (6.7)

For α_abs = 10⁵ cm⁻¹ = 10⁷ m⁻¹, the absorption term saturates by d ≈ 150 nm; collection typically binds before that in low-mobility blends. **In high-mobility NFA systems the optimum shifts to 300–500 nm**, which is precisely what is observed, and which is a *consequence* of improved μτ rather than of improved absorption.

---

## 7. Mixed Conduction, Bioelectronics, and Thermoelectrics

### 7.1 Volumetric invariants

Paper I established that OECT gain and bandwidth are separately thickness-dependent but their product is not [I, Thm 8.5]. Theorem 2.3(b) supplies the algebraic reason: the fibre direction (0,1,−1) in (μ, C*, d). We extend the accounting to the system level.

**Proposition 7.1 (Complete OECT invariant set).** For an OECT amplifier specified by transconductance g_m, bandwidth f_c, input-referred noise S_V, and large-signal switching time t_sw, the observable set has log-Jacobian of rank 3 in (μ, C*, d, ρ_eℓ_e), with invariants

  μ,  C*d,  ρ_eℓ_e,  and the *separate* appearance of d in t_sw ∝ d²/D_i.  (7.1)

Adding t_sw to the observable set breaks the thickness degeneracy.

*Proof.* g_m ∝ μC*d, f_c ∝ (ρ_eℓ_eC*d)^{−1}, t_sw ∝ d²/D_i. The exponent matrix on (μ, C*, d, ρ_eℓ_e) has rows (1,1,1,0), (0,−1,−1,−1), (0,0,2,0), rank 3, kernel spanned by (0,1,−1,0)·… computing: from row 3, the d-component of any kernel vector is 0; then rows 1 and 2 force μ-component 0 and C*-component 0. So rank 3 with kernel {(0,0,0,0)}? Re-examine: rows (1,1,1,0), (0,−1,−1,−1), (0,0,2,0). Row-reduce: from row 3, e_d direction is controlled; rows 1,2 then give two independent constraints on (μ, C*, ρ_eℓ_e). Rank 3, p = 4, kernel dim 1 spanned by (0,1,0,−1): C* ↦ κC*, ρ_eℓ_e ↦ ρ_eℓ_e/κ. Indeed g_m and f_c both invariant, t_sw invariant. ∎

**Correction to the naive statement.** Adding t_sw removes the *thickness* degeneracy but leaves a C*–electrolyte degeneracy. The remaining fibre direction is physically meaningful: a denser mixed conductor paired with a thinner/more conductive electrolyte is indistinguishable at this level of specification. To break it, add an impedance measurement that separates ionic resistance from chemical capacitance. **This is exactly the audit prescribed by §2.5, worked through.**

### 7.2 Tissue–device mechanical matching

**Proposition 7.2 (Impedance matching, mechanical).** The interfacial shear stress between a device of modulus E_d, thickness h_d and tissue of modulus E_t under strain mismatch Δε is, by shear lag,

  τ_max ≈ E_d h_d Δε/ℓ_SL,  ℓ_SL = √(E_d h_d t_t/G_t).  (7.2)

Minimizing τ_max at fixed function requires minimizing E_d h_d — the *membrane stiffness*, not the modulus alone.

*Proof.* Shear-lag balance (derived in §8.4) gives the transfer length ℓ_SL and the peak interfacial shear at the island edge; substituting yields (7.2). ∎

**Numbers.** Brain tissue E_t ≈ 1–10 kPa; PDMS E ≈ 1 MPa; polyimide E ≈ 3 GPa. For a 1 µm polyimide device, E_dh_d = 3×10³ N m⁻¹; for a 1 µm PDMS device, 1 N m⁻¹ — a 3000-fold reduction in interfacial stress at identical strain mismatch. **This, not conductivity, is the reason for elastomeric substrates in chronic implants.**

### 7.3 The hopping Seebeck coefficient: exact disorder cancellation

**Theorem 7.3.** For a Gaussian density of states of variance σ² and total density N, in the nondegenerate limit, with the transport energy equal to the equilibrium occupied energy ε_∞ = −σ²/k_BT [I, Lemma 4.9], the Seebeck coefficient is

  **S = −(k_B/q) ln(N/n),**  (7.3)

*independent of σ*.

*Proof.* Boltzmann occupation gives n = ∫g(ε)e^{−β(ε−ζ)}dε = N e^{βζ}e^{σ̂²/2}, so ζ = k_BT ln(n/N) − σ²/k_BT. The Seebeck coefficient of a hopping conductor is S = −(ε_tr − ζ)/(qT) with ε_tr the transport energy. Substituting ε_tr = ε_∞ = −σ²/k_BT:

  ε_tr − ζ = −σ²/k_BT − k_BT ln(n/N) + σ²/k_BT = −k_BT ln(n/N) = k_BT ln(N/n).

Hence (7.3); the disorder terms cancel identically. ∎

**Remark 7.4.** This is the transport-edge picture [34] obtained here as a two-line consequence of the exact equilibrium energy. Its content is important and counterintuitive: **disorder reduces conductivity but does not, to this order, reduce the Seebeck coefficient at fixed carrier density.** The widespread intuition that disorder "broadens the transport distribution and kills S" is not correct for Gaussian DOS in the nondegenerate limit; disorder acts on S only through its effect on the *achievable* n and on the position of ε_tr relative to ε_∞.

### 7.4 The optimum Seebeck and the ZT ceiling

**Theorem 7.5 (Universal optimum Seebeck).** For σ_el = qnμ with μ ∝ n^γ, the power factor PF = S²σ_el is maximized at

  ln(N/n*) = 2/(1+γ),  **S* = 2k_B/[q(1+γ)].**  (7.4)

In particular γ = 0 gives S* = 2k_B/q = 172 µV K⁻¹, independent of every material parameter.

*Proof.* PF ∝ n^{1+γ} ln²(N/n). Let y = ln(N/n); then n^{1+γ} = N^{1+γ}e^{−(1+γ)y} and PF ∝ y²e^{−(1+γ)y}. Setting d/dy = 0: 2y = (1+γ)y², so y = 2/(1+γ). Substituting into (7.3) gives S*. ∎

**Corollary 7.6.** For the disorder-driven density exponent γ = (1−α)/α ≈ 2.9 [I, Prop 4.11], S* ≈ 44 µV K⁻¹; for weakly density-dependent mobility, S* → 172 µV K⁻¹. Measured optima in doped polymers cluster at 100–200 µV K⁻¹ [35], implying **γ_eff ≈ 0–1 in the heavily doped regime** — much weaker than in the intrinsic FET regime. This is a genuine, testable inconsistency in the field's parameter set and points to degenerate screening of the trap-filling mechanism at high doping.

**Theorem 7.7 (ZT ceiling).** With Wiedemann–Franz κ_e = Lσ_el T and lattice contribution κ_lat,

  ZT = S²/(L + κ_lat/(σ_el T)) ≤ S²/L.  (7.5)

For nondegenerate statistics L ≈ 2(k_B/q)² = 1.49×10⁻⁸ W Ω K⁻², so at the optimum S* = 2k_B/q the ceiling is **ZT ≤ 2**.

*Proof.* Substitute κ = κ_e + κ_lat into ZT = S²σ_elT/κ and divide numerator and denominator by Lσ_elT. The bound is the κ_lat → 0 limit. ∎

**Numbers.** κ_lat = 0.3 W m⁻¹K⁻¹, σ_el = 10⁴ S m⁻¹, T = 300 K: Lσ_elT = 0.045 W m⁻¹K⁻¹, so ZT = 2/(1+6.7) = 0.26 — the observed range for organic thermoelectrics. **Reaching ZT = 1 requires σ_el ≳ 7×10⁴ S m⁻¹ (700 S cm⁻¹) at S = 172 µV K⁻¹**, which is a conductivity target, not a Seebeck target. The theorem thus reorders the research priorities: the binding constraint is σ, and by §3.5 that is a doping-efficiency problem, and by §3.4 that is a permittivity problem.

---

## 8. Mechanical Engineering of the Stack

### 8.1 Elasticity and the transformed section

The stack is a laminate of layers with stiffness tensors C_ijkl^{(a)}. For isotropic layers under plane strain, the relevant modulus is E′ = E/(1−ν²).

**Theorem 8.1 (Neutral plane).** For a laminate of layers a with modulus E_a′, thickness t_a, and mid-plane position z̄_a, the bending neutral plane is at

  **z_n = Σ_a E_a′ t_a z̄_a / Σ_a E_a′ t_a.**  (8.1)

The bending strain at height z is ε(z) = (z − z_n)/R_curv.

*Proof.* Pure bending with no net axial force requires ∫E′(z)(z−z_n)dz = 0. Evaluating layer by layer (each layer's first moment is E_a′t_a z̄_a) and solving for z_n gives (8.1). The strain distribution follows from the Kirchhoff hypothesis of plane sections. ∎

**Corollary 8.2 (Neutral-plane engineering).** Placing the active layer at z_n eliminates its bending strain to first order. Since z_n is a *modulus-weighted* centroid, a thin stiff overlayer moves it far more than a thick compliant one. A 100 nm SiN_x layer (E = 250 GPa) contributes E′t = 2.5×10⁴ N m⁻¹, equal to 25 µm of polyimide (E = 3 GPa) or 25 mm of PDMS (E = 1 MPa). **Encapsulation is therefore also a mechanical design element, and must be co-designed with the barrier (§9).**

### 8.2 Channel cracking

**Theorem 8.3 (Crack-onset strain).** For a film of thickness h, modulus E_f′, fracture energy Γ_f, under equibiaxial tension, the energy release rate for a through-thickness channel crack is G = Z σ²h/E_f′ with Z = O(1) depending on the elastic mismatch (Z ≈ 2 for a matched substrate). Setting G = Γ_f gives

  **ε_c = √(Γ_f/(Z E_f′ h)) ∝ h^{−1/2}.**  (8.2)

*Proof.* Dimensional analysis fixes G ∝ σ²h/E_f′ (the only combination with units of energy per area built from σ, h, E′); the dimensionless prefactor Z is computed by the elastic boundary-value problem [37,38]. With σ = E_f′ε, G = Z E_f′ε²h; equating to Γ_f and solving gives (8.2). ∎

**Numbers.** Polymer semiconductor: Γ_f = 1 J m⁻², E_f′ = 1 GPa, h = 100 nm, Z = 2 → ε_c = 7.1%. Small-molecule crystal: Γ_f = 0.5 J m⁻², E_f′ = 15 GPa → ε_c = 1.3%.

**Corollary 8.4 (Two design rules).** (i) ε_c ∝ h^{−1/2}: halving thickness buys √2 in strain tolerance — the mechanical counterpart of the throughput penalty (4.5) and the OECT gain lever. (ii) The material figure of merit is **√(Γ_f/E_f′)**, the *fracture compliance*: compliant, tough films beat stiff, strong ones. This is why semicrystalline polymers with amorphous tie regions outperform single crystals in flexible applications despite lower mobility.

### 8.3 Shear-lag strain isolation

**Theorem 8.5 (Island strain isolation).** For a stiff island of length L, membrane stiffness E_fh_f, bonded to a compliant substrate of shear modulus G_s and thickness t_s, define the shear-lag length

  ℓ = √(E_f h_f t_s/G_s).  (8.3)

Under remote substrate strain ε_app, the island strain profile is ε_f(x) = ε_app[1 − cosh(x/ℓ)/cosh(L/2ℓ)] and the mean island strain is

  **⟨ε_f⟩/ε_app = 1 − (2ℓ/L)tanh(L/(2ℓ)) ≈ L²/(12ℓ²) for L ≪ ℓ.**  (8.4)

*Proof.* Force balance on an island element with interfacial shear τ = G_s(u_f − u_sub)/t_s gives E_fh_f u_f″ = τ. Writing ε_f = u_f′ and differentiating, ε_f″ = (G_s/(E_fh_ft_s))(ε_f − ε_app) = (ε_f − ε_app)/ℓ². With traction-free island ends (ε_f(±L/2) = 0) the solution is the stated cosh form. Averaging over [−L/2, L/2] gives (8.4); the small-L expansion uses tanh x ≈ x − x³/3. ∎

**Numbers.** E_f = 1 GPa, h_f = 1 µm, t_s = 100 µm, G_s = 0.1 MPa: ℓ = √(10⁹·10⁻⁶·10⁻⁴/10⁵) = 10⁻³ m = 1 mm. For L = 100 µm: ⟨ε_f⟩/ε_app = (10⁻⁴)²/(12×10⁻⁶) = 8.3×10⁻⁴. **A 100 µm island on PDMS experiences 0.08% of the applied strain.** At 50% applied strain the island sees 0.04% — far below any ε_c from (8.2).

**Corollary 8.6 (Island–bridge design rule).** Isolation improves *quadratically* with decreasing island size. The binding constraint is therefore not the island but the interconnect, which must accommodate the full strain. Serpentine, fractal, or buckled interconnects convert tensile strain into bending, for which the strain is t_interconnect/(2R_bend) rather than the applied strain — a geometric, not material, solution.

### 8.4 The barrier–flexibility feasibility condition

**Theorem 8.7.** Let a barrier consist of n dyads of total period p_b, so t_b = n p_b, with lifetime T ∝ n² (§9.2) and bending strain at the outermost device layer ε_bend = t_total/(2R_curv). Given a required lifetime T_req and bend radius R_req with allowable strain ε_max, a feasible design exists iff

  **√(T_req/T₁) ≤ [2R_req ε_max − t_other]/p_b,**  (8.5)

where T₁ is the single-dyad lifetime and t_other the non-barrier stack thickness.

*Proof.* Lifetime imposes n ≥ √(T_req/T₁); mechanics imposes n ≤ (2R_reqε_max − t_other)/p_b. Both are satisfiable iff (8.5). ∎

**Consequence.** Barrier and flexibility requirements are *directly antagonistic* through a single integer n, and (8.5) is a hard feasibility test that should precede any materials selection. Neutral-plane placement (§8.1) relaxes it by removing the barrier from the high-strain position — which is why symmetric encapsulation is not a luxury.

---

## 9. Barrier and Reliability Engineering

### 9.1 Permeation fundamentals and the tortuosity tensor

**Proposition 9.1 (Lag time).** For Fickian diffusion through a slab of thickness L with diffusivity D and upstream concentration stepped from 0 to c₀, the steady flux is J_∞ = Dc₀/L and the extrapolated time lag is

  t_lag = L²/(6D).  (9.1)

*Proof.* Solve ∂_tc = D∂_z²c with c(0,t) = c₀, c(L,t) = 0, c(z,0) = 0. The downstream accumulated quantity Q(t) = ∫₀^t (−D∂_zc)|_L dt′ has the large-t asymptote Q(t) → (Dc₀/L)(t − L²/(6D)), obtained by integrating the eigenfunction series and summing Σ(−1)^{k+1}/k² = π²/12. The intercept defines t_lag. ∎

**Proposition 9.2 (Tortuosity tensor).** For a matrix of diffusivity D₀ loaded with volume fraction φ of aligned impermeable platelets of aspect ratio α = width/thickness, the effective diffusivity tensor is strongly anisotropic:

  D_eff^{zz} = D₀(1−φ)/(1 + αφ/2),  D_eff^{xx} ≈ D₀(1−φ).  (9.2)

*Proof sketch.* The Nielsen construction: a permeant must detour around each platelet, adding a lateral path length α/2 per platelet encounter; the number of encounters along the thickness is proportional to φ, giving the path-length factor (1+αφ/2) and hence the reduced normal diffusivity. The in-plane path is unobstructed apart from the volume exclusion factor (1−φ). ∎ (elementary geometric closure; the O(1) constant is model-dependent)

**Design rule.** High-aspect-ratio fillers (α ~ 100–1000, exfoliated clay or graphene) at φ = 0.05 give a 3–26× reduction in normal permeation with negligible in-plane penalty and modest mechanical cost. This is a *tensorial* design lever: one is engineering D^{ij}, not a scalar.

### 9.2 The multilayer n² theorem

**Theorem 9.3 (Dyad lag-time scaling).** In an organic/inorganic multilayer barrier with n dyads, inorganic layers impermeable except at sparse defects of areal density ρ_d, and polymer planarization layers of thickness h_p and diffusivity D_p, the permeant must traverse a laterally tortuous path of mean length per dyad ℓ_lat ≈ ½ρ_d^{−1/2}. Hence

  **t_lag ≈ (n ℓ_lat)²/(6D_p) ∝ n²,  J_∞ ∝ 1/(n ℓ_lat) ∝ 1/n.**  (9.3)

*Proof.* Successive inorganic layers have uncorrelated defect positions, so a permeant reaching a defect in layer k must diffuse laterally in the polymer to find a defect in layer k+1, a mean distance of order half the defect spacing. The total path is nℓ_lat, executed by diffusion in the polymer, giving the stated lag time by (9.1) with L → nℓ_lat. Steady flux is inversely proportional to path length. ∎

**Corollary 9.4 (The central barrier design rule).** **Steady-state WVTR improves linearly in n; transient lifetime improves quadratically.** For devices failing by a *finite accumulated dose* (cathode corrosion, dark-spot nucleation), the relevant figure is the lag time, and dyad count is quadratically valuable. This resolves the apparent discrepancy between modest measured WVTR improvements and large measured lifetime improvements in multilayer barriers [41].

**Corollary 9.5 (Defect density is the real lever).** t_lag ∝ ρ_d^{−1}: halving defect density doubles lifetime as effectively as adding √2 more dyads, at zero thickness cost. **Particle control and planarization outrank dyad count.**

### 9.3 Dose-limited lifetime and the WVTR requirement

**Theorem 9.6 (Derived WVTR specification).** Let failure occur when a reactive getter/cathode of thickness h_Ca, density ρ_Ca, molar mass M_Ca has consumed a water dose corresponding to utilization fraction u of its capacity (Ca + 2H₂O → Ca(OH)₂ + H₂). Then the critical dose is

  D_c = 2u ρ_Ca h_Ca M_w/M_Ca,  and  **WVTR_max = D_c/t_life.**  (9.4)

*Proof.* Stoichiometry: moles of Ca per area = ρ_Cah_Ca/M_Ca; each consumes 2 H₂O; multiply by M_w and by the utilization u. Dividing by the required lifetime gives the maximum tolerable flux. ∎

**Numbers.** h_Ca = 100 nm, ρ_Ca = 1550 kg m⁻³, M_Ca = 0.040 kg mol⁻¹, M_w = 0.018 kg mol⁻¹, u = 1: D_c = 1.4×10⁻⁴ kg m⁻² = 0.14 g m⁻². For t_life = 10⁴ h = 417 days, WVTR_max = 3.4×10⁻⁴ g m⁻² day⁻¹.

The canonical OLED requirement is ~10⁻⁶ g m⁻² day⁻¹, i.e. **u ≈ 3×10⁻³**: failure occurs when only 0.3% of the cathode capacity is consumed, because damage is *localized* at defects and dark spots are visible long before uniform corrosion.

**Honest statement.** The utilization u is the empirically calibrated element of this derivation; it is not predicted. But the derivation makes its role explicit and gives the correct scaling: WVTR_max ∝ u h_Ca/t_life. **Thicker cathodes buy lifetime linearly**, which is a real and underused lever, and the localization factor u is the quantity that improved barrier *uniformity* (rather than improved average WVTR) attacks.

### 9.4 Bias stress and the dispersive consistency theorem

**Theorem 9.7 (Kohlrausch–dispersion identity).** Let carrier trapping be governed by an exponential depth distribution with characteristic energy E_c and Arrhenius release, so the waiting-time density is ψ(t) ∝ t^{−1−α} with α = k_BT/E_c [I, Thm 5.2]. Then the fraction of carriers remaining mobile obeys fractional relaxation of order α, whose solution is the Mittag-Leffler function

  φ(t) = E_α(−(t/τ)^α),  (9.5)

with short-time behaviour φ(t) ≈ exp[−(t/τ)^α/Γ(1+α)] and long-time behaviour φ(t) ≈ (t/τ)^{−α}/Γ(1−α). Consequently the stretched-exponential (Kohlrausch) exponent fitted to bias-stress threshold drift satisfies

  **β_K = α.**  (9.6)

*Proof.* The trapping kinetics with kernel ψ give a fractional relaxation equation D_t^α φ = −τ^{−α}φ, whose solution is (9.5) [44]. The two asymptotic forms are standard properties of E_α. Since bias-stress threshold shift is proportional to the trapped charge, ΔV_th(t) = ΔV_∞[1 − φ(t)], fitting the short-to-intermediate-time behaviour with a stretched exponential returns exponent α. ∎

**Theorem 9.8 (Dispersive consistency theorem).** Under the single-exponential-tail hypothesis, the following four independently measurable quantities are determined by one parameter:

  **α = β_K = 1 − β_noise = 1/(m_SCLC − 1),**  (9.7)

where α is the time-of-flight dispersion exponent [I, Cor 5.3], β_K the bias-stress Kohlrausch exponent (9.6), β_noise the drain-current 1/f^β exponent [I, Cor 9.7], and m_SCLC the trap-limited space-charge exponent (3.12).

*Proof.* Combine Theorem 9.7, [I, Thm 5.2 and Cor 9.7] (α + β = 1), and Theorem 3.13 (m = 1 + 1/α). ∎

**Corollary 9.9 (A four-fold falsification test).** Any one of {α, β_K, β_noise, m_SCLC} predicts the other three. Measuring all four on the same film is a stringent, inexpensive test of the exponential-tail hypothesis that underlies essentially all organic device modelling. **Violation localizes the failure**: if α and β_noise agree but β_K does not, the bias stress is not trap-limited (ionic motion, dipolar relaxation, or contact degradation); if m_SCLC disagrees, the tail is not exponential over the probed range.

To our knowledge this four-fold consistency test has never been systematically applied. It is the single most economical experiment proposed in this paper.

### 9.5 Acceleration models

**Proposition 9.10 (Peck-type acceleration).** For permeation-limited failure with water flux J ∝ (RH)^m and thermally activated reaction with barrier E_a,

  t_life ∝ (RH)^{−m} exp(E_a/k_BT) · exp(−γV).  (9.8)

The dose model of §9.3 predicts m = 1 (flux proportional to vapour pressure). Observed Peck exponents are m ≈ 2–3 [45].

**Open Problem 2.** The discrepancy m_observed > 1 is unexplained by pure permeation. Candidate resolutions: (i) reaction order > 1 in water at the cathode; (ii) RH-dependent solubility (non-Henry sorption, clustering at high activity); (iii) hygroscopic swelling opening percolation paths. These are distinguishable by measuring sorption isotherms and permeation separately from device lifetime. **Until resolved, accelerated-lifetime extrapolation in RH is not justified**, and reported lifetime projections at use conditions from 85/85 testing carry an uncontrolled systematic error.

---

## 10. Circuit and System Engineering

### 10.1 Noise margin and the gain requirement

**Theorem 10.1 (Noise margin).** For a symmetric inverter with rail-to-rail output, trip point V_DD/2, and piecewise-linear transfer characteristic of slope −A between the rails, the unity-gain points are at V_{IL,IH} = (V_DD/2)(1 ∓ 1/A) and

  **NM_L = NM_H = (V_DD/2)(1 − 1/|A|).**  (10.1)

Positive noise margin requires |A| > 1.

*Proof.* The linear segment is V_out = V_DD/2 − A(V_in − V_DD/2). It reaches V_DD at V_in = (V_DD/2)(1 − 1/A) and 0 at V_in = (V_DD/2)(1 + 1/A). Outside this range the gain is zero, so the unity-gain points are exactly these. NM_L = V_IL − V_OL = V_IL and NM_H = V_OH − V_IH = V_DD − V_IH; both equal (V_DD/2)(1−1/A). ∎

### 10.2 Gain from the scale length

**Proposition 10.2.** For a complementary organic inverter with both devices saturated, the small-signal gain is A = g_m/(g_{o,n}+g_{o,p}). Using g_m/g_d ≃ (2+γ)(L/λ − 1) per device [I, Prop 9.5] and equal contributions,

  A ≃ (2+γ)(L/λ − 1)/2.  (10.2)

Combining with (10.1), a target noise margin NM = κV_DD requires

  **L/λ ≥ 1 + 4/[ (2+γ)(1 − 2κ) ].**  (10.3)

*Proof.* Substitute (10.2) into (10.1), set NM = κV_DD so 1 − 1/A = 2κ, hence A = 1/(1−2κ), and solve (10.2) for L/λ. ∎

**Numbers.** For γ = 0 and κ = 0.4 (NM = 0.4V_DD): A = 5, L/λ ≥ 6. With printed dielectrics giving λ ≈ 1 µm [I, Prop 6.3], L ≥ 6 µm. Inkjet resolution is 10–20 µm (§4.3), so the design is feasible but *not* aggressively scalable. **Printed organic logic is limited by dielectric thickness (through λ) and by registration (through variability), not by mobility.**

### 10.3 Variability: two distinct laws

**Proposition 10.3 (Pelgrom component).** From random occupancy of interface/gap traps of areal density D_t with occupancy p,

  σ_{V_th} = (q/C_i)√(D_t p(1−p)/(WL)) ≡ A_VT/√(WL).  (10.4)

*Proof.* Trapped charge variance = q²D_tWL·p(1−p) (binomial); dividing by (C_iWL)² and taking the square root gives (10.4). ∎

**Theorem 10.4 (Dichotomy).** The total variability is

  σ²_{ln I} = (A_VT/(A√(WL)))²·(∂ln I/∂V_th)² + (σ_reg/L)² + (σ_reg/W)² + …  (10.5)

The first term scales as (WL)^{−1}, the geometric terms as L^{−2}, W^{−2}. **In lithographic devices the first dominates; in printed devices the second does.**

*Proof.* Combine (10.4) and Theorem 4.11. ∎

**Design consequence.** In printed circuits, increasing device *area* at fixed L does not reduce variability, whereas increasing L does — linearly. This inverts the silicon sizing intuition and must be encoded in the design rules. Self-aligned printing, which removes σ_reg from L, is therefore the highest-value process innovation for printed logic.

### 10.4 Yield

**Proposition 10.5 (Poisson yield).** For a circuit of area A_c with fatal-defect density D₀,

  Y = exp(−D₀A_c).  (10.6)

For a system of N_c independent circuits, Y_sys = Y^{N_c}. To achieve Y_sys ≥ 0.9 with N_c = 10³ requires D₀A_c ≤ 1.05×10⁻⁴.

*Proof.* Poisson statistics of independent fatal defects; the numerical requirement solves exp(−10³D₀A_c) = 0.9. ∎

**Consequence.** For A_c = 1 mm² = 10⁻⁶ m², D₀ ≤ 105 m⁻² ≈ 1 defect per 100 cm². Particle control at this level is a cleanroom-class requirement, and it is the *same* lever that controls barrier defect density ρ_d (§9.2). **A single contamination-control investment pays into both yield and lifetime** — an instance of a fibre direction that is *not* silent, and therefore correctly prioritized.

### 10.5 Invariant-first specification: worked protocol

**Table 10.1 — Measurement-to-invariant map.**

| Target invariant | Measurement that identifies it | Fibre direction it kills |
|---|---|---|
| μ/L² (OFET speed) | ring oscillator delay or f_T | (μ, C_i, L) → 2 combos |
| C_iL (gate charge) | C–V at operating frequency | with above, fully identifies |
| μ(n) intrinsic | dI_D,sat/dV_G [I, Thm 7.2] | contact-law fibre |
| R_c(V_G) | linear branch minus intrinsic [I, (7.5)] | — |
| C*d (OECT) | g_m at known Wd/L and bias | (C*, d) partially |
| d separately | large-signal t_sw ∝ d² [I, Prop 8.7] | remaining thickness fibre |
| η_outΦ_PL | EQE at known γ, η_r | — |
| Φ_PL separately | integrating sphere on the actual stack | outcoupling fibre |
| Θ_h | angle-resolved polarized PL | orientation fibre |
| L_D/R | transient absorption + GISAXS | morphology fibre |
| μτV/d² | photo-CELIV or TPC | — |
| α | any one of four (Thm 9.8) | dispersion model |
| E_U | FTPS/PDS absorption edge | — |
| EQE_EL | EL quantum efficiency | non-radiative loss |

**Protocol.** (1) List the application's observables. (2) Compute Λ and its kernel (Thm 2.3/2.4). (3) List the failure-mode observables. (4) Compute the dangerous subspace (Prop 2.8). (5) Add measurements until the dangerous subspace is empty. (6) Write the specification on the resulting invariant set. (7) Optimize the remaining fibre freedom for cost, thickness, and throughput.

This is a complete, implementable methodology, and it is the paper's principal engineering deliverable.

### 10.6 Cost model

**Proposition 10.6.** Cost per functional area is

  C_area = [Σ_k c_k^{mat} + C_eq/(v · w_line · U · Y)]/1,  (10.7)

with c_k^{mat} material costs per area, C_eq line capital amortization rate, v line speed (bounded by (4.5)), w_line web width, U uptime, Y yield (10.6).

**Consequence.** The throughput ceiling v ≤ L_ovenD/H² enters the cost inversely and the yield exponentially. For thick-film devices (OECTs, OPVs) the H² penalty is the dominant cost driver, and it is *the same H* that provides gain and absorption. **Thickness is simultaneously the gain lever, the bandwidth penalty, the throughput penalty, the mechanical penalty, and the cost penalty.** No other single variable in the field carries so many competing consequences, and any thickness choice must be justified against all five.

---

## 11. Synthesis: The Design Chart and the No-Go Theorems

### 11.1 The design chart

**Table 11.1 — Governing inequalities.**

| Group | Target | Reason | Result |
|---|---|---|---|
| σ̂ | minimize; but see 𝔲 | mobility, dispersion | [I, §4] |
| 𝔠 | ≤ 6 (raise ε) | doping efficiency e^{−𝔠} | Thm 3.8 |
| 𝔭 | ≤ 1 | delocalization survives | Thm 3.1 |
| N_dop | ≥ (4a)^{−3} | complete ionization | Thm 3.9 |
| σ_d | ≤ 0.3σ₀ | interface disorder | Thm 3.4 |
| Pe | < 1 (or ≫ 1 deliberately) | stratification control | Thm 4.1 |
| Z = 1/Oh | 1–10 | jettability | Prop 4.7 |
| 𝔫 = L/λ | ≥ 6 | noise margin | Prop 10.2 |
| σ_reg/L | ≤ 0.05 | matching | Thm 4.11 |
| Θ_h | → 1 | outcoupling (≤ 1.5×) | Thm 5.6 |
| R/L_D | ≤ 1.2 | harvesting ≥ 90% | Thm 6.1 |
| λ_n/λ_p | ≈ 1 | collection | Cor 6.4 |
| 𝔲 = E_U/k_BT | ≤ 1 | zero Urbach penalty | Thm 6.8 |
| EQE_EL | maximize | ΔV_nr | Prop 6.6 |
| S | 2k_B/[q(1+γ)] | power factor | Thm 7.5 |
| 𝔤 = Γ_f/(E_fh) | maximize | strain tolerance | Thm 8.3 |
| L/ℓ_SL | ≪ 1 | strain isolation | Thm 8.5 |
| n (dyads) | per (8.5) | lifetime vs. flexibility | Thm 8.7 |
| ρ_d | minimize | t_lag ∝ ρ_d^{−1} | Cor 9.5 |
| T_g − T_op | ≥ 50 K | morphology retention | Prop 4.10 |
| D₀A_c | ≤ 10⁻⁴/N_c | yield | Prop 10.5 |

### 11.2 Eight no-go theorems

These are upper bounds that no materials optimization can circumvent. They delimit the design space and should be checked *before* a programme is initiated.

**N1 (Kinetic ceiling).** f_T ≤ (2+γ)aν₀/(2πL). With a = 1 nm, ν₀ = 10¹³ s⁻¹: f_T ≤ 16 GHz at L = 100 nm. Organic transistors cannot match silicon RF at equal geometry [I, Prop 9.4].

**N2 (Onsager doping ceiling).** Isolated-dopant efficiency ≤ e^{−𝔠}; at ε_r = 3.5, a = 1 nm this is 10⁻⁷. Efficient doping *requires* dopant overlap or high permittivity (Thm 3.8–3.9).

**N3 (Orientation bound).** Purely horizontal dipoles improve escape-cone outcoupling by at most 3/2 (Thm 5.6). Claims beyond this require a different mechanism.

**N4 (Volumetric thickness invariance).** g_m·f_c is independent of d and C* in the ion-limited regime; only μ, W/L, and ρ_eℓ_e improve both [I, Thm 8.5].

**N5 (Thermoelectric ceiling).** ZT ≤ S²/L; at the optimum Seebeck, ZT ≤ 2 for nondegenerate statistics (Thm 7.7).

**N6 (Fracture–thickness law).** ε_c ∝ h^{−1/2}: strain tolerance and film thickness are antagonistic with a fixed exponent (Thm 8.3).

**N7 (Registration variability).** Printed-circuit variability scales as σ_reg/L, not (WL)^{−1/2}; area averaging does not cure it (Thm 4.11, 10.4).

**N8 (Urbach threshold).** Disorder reduction below E_U = k_BT yields no further open-circuit voltage benefit (Thm 6.8). Beyond that point, effort must move to EQE_EL.

### 11.3 The design algorithm

1. **Fix the observable set** O from the application, including failure-mode observables (§2.5).
2. **Compute the invariant ring** and fibre dimension (Thm 2.3/2.4); audit the dangerous subspace (Prop 2.8) and add measurements to empty it.
3. **Check the no-go theorems** N1–N8 against the targets. If a target violates one, renegotiate the target or change the architecture — do not initiate a materials programme.
4. **Set invariant targets** from Table 11.1.
5. **Choose a point in the fibre** by optimizing manufacturing: thickness against (4.5), (8.2), (8.5), (10.7); geometry against (10.3), (4.8); materials against cost.
6. **Verify the dispersive consistency theorem** (9.7) on the actual film. If it fails, the constitutive model is wrong and every downstream extraction is suspect.
7. **Re-audit for silent variability** whenever the process changes, since a process change moves the point within the fibre and may activate a previously dormant failure mode.

---

## 12. Sharpness, Failure Modes, and Open Problems

### 12.1 Where the closures are load-bearing

We list every unproved element used above, with its location and its consequence if false.

| Element | Location | Consequence if false |
|---|---|---|
| c = 4/9 disorder exponent | §3.2, §3.5 (from [I]) | numerical prefactors, not scalings |
| Uncorrelated-Gaussian Coulomb landscape | Claim 3.11 | N_opt off by 2–3 decades (known failure) |
| τ_rec ∝ R | Claim 6.5 | R* exponent may differ from 1/3 |
| Single-mode energy-gap law | Claim 6.7 | slope (6.5) not universal |
| Z ≈ 2 crack prefactor | Thm 8.3 | O(1) in ε_c |
| Nielsen tortuosity constant | Prop 9.2 | O(1) in D_eff |
| Uncorrelated defects, dyad lag | Thm 9.3 | n² may degrade toward n |
| Utilization u | Thm 9.6 | WVTR spec scales linearly with u |
| Exciton–polaron damage | Claim 5.12 | acceleration exponent n |
| Ma_c = O(1) | Claim 4.6 | reversal threshold ink-specific |

None is concealed at the point of use.

### 12.2 Known failures of the framework

**(a) Correlated disorder.** The Gaussian-un-correlated assumption fails for Coulomb landscapes (§3.5) and for dipolar landscapes with short-range order. The variance is not the right summary statistic; the correlation function is. **Open Problem 1** (restated): compute the localization exponent for a correlated random potential with correlation length ξ_c, and determine the effective c(ξ_c/a).

**(b) Non-exponential tails.** The dispersive consistency theorem (9.7) is a *test*, and it will sometimes fail. A Gaussian DOS gives non-exponential tails and hence a non-constant effective α; the four measurements will then disagree in a specific, calculable way. This is a feature, not a defect: the theorem is a discriminator.

**(c) Degenerate statistics.** Theorems 7.3 and 7.5 assume nondegeneracy. At the doping levels required by Thm 3.9 (10¹⁹ cm⁻³) and above, degeneracy sets in, ε_tr ≠ ε_∞, and the disorder cancellation (7.3) fails. The observed S* ≈ 100–200 µV/K versus predicted 44 µV/K (Cor 7.6) is direct evidence that this regime is reached in practice. **Open Problem 3:** extend §7.3–7.4 to degenerate hopping with a self-consistent transport energy.

**(d) The Peck exponent.** §9.5, Open Problem 2. Unresolved and practically consequential.

**(e) Morphology–transport coupling.** Claim 6.5 treats μ and τ_rec as separable functions of R. In reality both depend on the same percolation geometry. **Open Problem 4:** solve the joint percolation–reaction problem on a realistic blend morphology and determine whether R* ∝ (L_D²d)^{1/3} survives.

### 12.3 Conjectures

**Conjecture 1 (Invariant completeness).** For every organic device class, the invariant ring computed from the union of performance and failure-mode observables is finitely generated and separates points of the physically admissible parameter set. (Equivalently: there are no *irreducibly* unidentifiable but consequential parameters.)

**Conjecture 2 (Thickness antagonism is universal).** Film thickness enters gain, bandwidth, throughput, strain tolerance, and cost with exponents (+1, −1, −2, −1/2, −1) respectively in the regimes considered here, and these exponents are structural consequences of the governing equations rather than of any material.

**Conjecture 3 (Registration universality).** Any patterning technology whose error is a rigid placement offset rather than an edge-roughness process exhibits 1/L variability, and no amount of device-area averaging restores Pelgrom scaling.

---

## 13. Falsifiable Predictions

1. **Doping threshold.** Efficient ionization onset at N* = (4a)^{−3}, shifting as ε³ across a permittivity series (Thm 3.9, Claim 3.11).
2. **Dielectric disorder.** Mobility loss quantitatively predicted by (3.4) from independently measured p, N_d, z; halving with a 2 nm spacer.
3. **Polycrystal geometric mean.** Untextured films of a highly anisotropic crystal deliver √(μ₁μ₂); texturing beats it (Thm 3.6).
4. **Stratification factor.** Vertical composition profile follows Pe/(1−e^{−Pe}) across an evaporation-rate series (Thm 4.1).
5. **Coating ceiling.** Maximum defect-free line speed scales as H^{−2} at fixed oven length (Thm 4.9).
6. **Orientation bound.** No orientation-only outcoupling enhancement exceeds 1.5× (Thm 5.6).
7. **Roll-off curve.** η(J) follows 2/[1+√(1+8J/J_{1/2})] with a single fitted J_{1/2} over three decades of current (Thm 5.8).
8. **Cavity shift.** Optimal emitter–cathode distance shifts with current density according to (5.9) (Thm 5.10).
9. **Domain-size scaling.** R* ∝ d^{1/3} across a thickness series at fixed materials (Claim 6.5).
10. **Urbach threshold.** ΔV_oc penalty vanishes for E_U ≤ 26 meV and follows (6.6) above it (Thm 6.8).
11. **Seebeck optimum.** PF peaks at S = 2k_B/[q(1+γ)] with γ independently measured from the density-dependent mobility (Thm 7.5).
12. **Strain isolation.** Mean island strain scales as L² at fixed stack (Thm 8.5).
13. **Barrier n² law.** Lifetime scales as n² while steady WVTR scales as n^{−1} (Thm 9.3).
14. **Dispersive consistency.** α = β_K = 1 − β_noise = 1/(m_SCLC − 1) on the same film (Thm 9.8).

Predictions 6, 10, 13, and 14 are inexpensive, decisive, and require no new instrumentation. They constitute the minimal experimental programme implied by this paper.

---

## 14. Conclusion

Organic electronics has been practised as a materials science with device demonstrations attached. We have argued that it should be practised as a design science with an explicit identifiability calculus attached, because its constitutive parameters are neither measurable nor transferable in the way the field's vocabulary assumes.

The calculus is not abstract. It says that "the mobility" is not specifiable from DC and AC transistor data alone, but μ/L² and C_iL are; that thickness and volumetric capacitance in an electrochemical device are separately unidentifiable but their product is; that the outcoupling fraction and the quantum yield cannot be separated by an efficiency measurement; and — most consequentially — that a parameter drift invisible in the acceptance test may be decisive for lifetime, so the observable set must be closed under failure modes rather than performance modes.

Around this calculus we have derived the field's engineering laws as theorems: a doping threshold at 10¹⁹ cm⁻³ from the Onsager radius alone; a fivefold mobility penalty from dielectric dipoles computed from first principles; an exact geometric-mean law for polycrystals that reorders molecular design priorities; a sharp 3/2 bound on orientation-enhanced outcoupling; an exact roll-off curve and a current-weighted cavity optimum; a cube-root law for bulk-heterojunction domain size; a hard voltage threshold at E_U = k_BT that converts "reduce disorder" into a bounded target; a universal optimum Seebeck of 2k_B/q; a quadratic dyad law for barrier lifetime; and a four-fold consistency theorem that tests the entire dispersive-transport framework with one film and four measurements.

Eight no-go theorems bound what is achievable. Several of them are unwelcome: the kinetic ceiling forbids silicon-class RF at equal geometry; the thickness-invariance theorem says the celebrated electrochemical transconductance is bought rather than earned; the registration law says printed circuits cannot be matched by area averaging. We regard the explicit statement of these bounds as the most useful thing an engineering theory can do. A field that knows its ceilings can allocate effort; a field that does not, optimizes parameters that are not identifiable against targets that are not achievable.

---

## Appendix A. Green dyadic and the mirror rates

The free-space dyadic in the near/far decomposition is

  𝔾_ij(r) = (e^{ikr}/(4πk²r³))[(k²r² + ikr − 1)δ_ij + (−k²r² − 3ikr + 3)r̂_ir̂_j].

For r̂ = ẑ, the transverse component is 𝔾_xx = (e^{iu}/(4πk²r³))(u² + iu − 1) and the longitudinal 𝔾_zz = (e^{iu}/(4πk²r³))(2 − 2iu), u = kr. Taking imaginary parts:

  Im 𝔾_xx = [(u²−1)sin u + u cos u]/(4πk²r³),
  Im 𝔾_zz = [2 sin u − 2u cos u]/(4πk²r³).

With r = 2d and k²r³ = u³/k, both become (k/(4πu³))×[…]. Normalizing by Im 𝔾_xx(0) = k/(6π) multiplies by 6π/k, giving (3/(2u³))[(u²−1)sin u + u cos u] and (3/u³)[sin u − u cos u]. Image signs s = −1 (parallel), +1 (perpendicular) give (5.3)–(5.4). Small-u checks: Γ_∥ → 0, Γ_⊥ → 2. ∎

## Appendix B. Mark–Helfrich integration

From dE/dx = (qN_t/ε)(J/(qμN_vE))^{1/l} ≡ A E^{−1/l}:

  E^{1/l}dE = A dx ⟹ (l/(l+1))E^{(l+1)/l} = Ax ⟹ E = [(l+1)Ax/l]^{l/(l+1)}.
  V = ∫₀^d E dx = [(l+1)A/l]^{l/(l+1)}·(l+1)/(2l+1)·d^{(2l+1)/(l+1)}.
  A = (l/(l+1))·[V(2l+1)/(l+1)]^{(l+1)/l}·d^{−(2l+1)/l}.
  J = qμN_v(Aε/(qN_t))^l = q^{1−l}μN_v[εl/(N_t(l+1))]^l[(2l+1)/(l+1)]^{l+1}V^{l+1}d^{−(2l+1)}. ∎

## Appendix C. Escape-cone integrals

Normalized patterns: p_h = 3(1+cos²θ)/(16π), p_v = 3sin²θ/(8π), p_iso = 1/(4π); each integrates to 1 over 4π. With c = cos θ_c:

  F_h = (3/8)∫₀^{θ_c}(1+cos²θ)sinθ dθ = (3/8)[4/3 − c − c³/3],
  F_v = (3/4)∫₀^{θ_c}sin³θ dθ = (3/4)[2/3 − c + c³/3],
  F_iso = (1−c)/2.

Consistency: (2/3)F_h + (1/3)F_v = (1−c)/2 ✓. Ratio ρ = F_h/F_iso = (c²+c+4)/4 by factoring 1 − (3/4)c − (1/4)c³ = (1/4)(1−c)(c²+c+4). Limits ρ(1)=1, ρ(∞)=3/2. ∎

## Appendix D. Shear-lag solution

Force balance: E_fh_f u_f″ = G_s(u_f − u_sub)/t_s. With ε_f = u_f′ and remote ε_app:

  ε_f″ = (ε_f − ε_app)/ℓ², ℓ² = E_fh_ft_s/G_s.

Traction-free ends ε_f(±L/2) = 0 give ε_f = ε_app[1 − cosh(x/ℓ)/cosh(L/2ℓ)]. Mean:

  ⟨ε_f⟩ = ε_app[1 − (2ℓ/L)tanh(L/2ℓ)] → ε_app L²/(12ℓ²) for L ≪ ℓ. ∎

## Appendix E. Principal symbols

| Symbol | Meaning | SI unit |
|---|---|---|
| A, Λ | exponent matrix, log-Jacobian | — |
| 𝔠 | Coulomb number r_c/a | — |
| C_i, C* | areal, volumetric capacitance | F m⁻², F m⁻³ |
| Θ^{ij}, Θ_h | dipole orientation tensor, in-plane fraction | — |
| 𝔾_ij | dyadic Green function | m⁻¹ |
| Γ_∥, Γ_⊥, F_P | normalized decay rates, Purcell factor | — |
| ρ(n) | orientation enhancement bound | — |
| J_{1/2} | half-efficiency current density | A m⁻² |
| L_D, R, R* | exciton diffusion length, domain size, optimum | m |
| λ_n, λ_p | carrier drift lengths | m |
| E_U, 𝔲 | Urbach energy, E_U/k_BT | J, — |
| S, L | Seebeck coefficient, Lorenz number | V K⁻¹, W Ω K⁻² |
| Γ_f, Z, ε_c | fracture energy, crack prefactor, onset strain | J m⁻², —, — |
| ℓ_SL | shear-lag length | m |
| t_lag, ρ_d | permeation lag time, defect density | s, m⁻² |
| Pe, Oh, Z | Péclet, Ohnesorge, inverse Ohnesorge | — |
| σ_reg | registration error | m |
| α, β_K, β_noise, m | dispersion, Kohlrausch, noise, SCLC exponents | — |
| λ | scale length √(ε_st_st_i/ε_i) [I] | m |
| 𝔫 | scaling number L/λ | — |

---

## References

[1] H. Bässler, *Charge transport in disordered organic photoconductors*, Phys. Status Solidi B **175** (1993) 15.
[2] V. Coropceanu et al., *Charge transport in organic semiconductors*, Chem. Rev. **107** (2007) 926.
[3] R. A. Marcus, *Electron transfer reactions in chemistry: theory and experiment*, Rev. Mod. Phys. **65** (1993) 599.
[4] T. Holstein, *Studies of polaron motion II*, Ann. Phys. **8** (1959) 343.
[5] A. Miller, E. Abrahams, *Impurity conduction at low concentrations*, Phys. Rev. **120** (1960) 745.
[6] V. Ambegaokar, B. I. Halperin, J. S. Langer, *Hopping conductivity in disordered systems*, Phys. Rev. B **4** (1971) 2612.
[7] L. Onsager, *Initial recombination of ions*, Phys. Rev. **54** (1938) 554.
[8] C. L. Braun, *Electric field assisted dissociation of charge transfer states*, J. Chem. Phys. **80** (1984) 2634.
[9] B. Lüssem, M. Riede, K. Leo, *Doping of organic semiconductors*, Phys. Status Solidi A **210** (2013) 9.
[10] I. Salzmann, G. Heimel, M. Oehzelt, S. Winkler, N. Koch, *Molecular electrical doping of organic semiconductors*, Acc. Chem. Res. **49** (2016) 370.
[11] V. I. Arkhipov, P. Heremans, E. V. Emelianova, H. Bässler, *Effect of doping on the density-of-states distribution and carrier hopping*, Phys. Rev. B **71** (2005) 045214.
[12] J. C. Scott, G. G. Malliaras, *Charge injection and recombination at the metal–organic interface*, Chem. Phys. Lett. **299** (1999) 115.
[13] P. R. Emtage, J. J. O'Dwyer, *Richardson–Schottky effect in insulators*, Phys. Rev. Lett. **16** (1966) 356.
[14] N. F. Mott, R. W. Gurney, *Electronic Processes in Ionic Crystals*, Oxford (1940).
[15] P. Mark, W. Helfrich, *Space-charge-limited currents in organic crystals*, J. Appl. Phys. **33** (1962) 205.
[16] M. A. Lampert, P. Mark, *Current Injection in Solids*, Academic Press (1970).
[17] A. M. Dykhne, *Conductivity of a two-dimensional two-phase system*, Sov. Phys. JETP **32** (1971) 63.
[18] J. B. Keller, *A theorem on the conductivity of a composite medium*, J. Math. Phys. **5** (1964) 548.
[19] R. D. Deegan et al., *Capillary flow as the cause of ring stains from dried liquid drops*, Nature **389** (1997) 827.
[20] H. Hu, R. G. Larson, *Evaporation of a sessile droplet on a substrate*, J. Phys. Chem. B **106** (2002) 1334.
[21] B. Derby, *Inkjet printing of functional and structural materials*, Annu. Rev. Mater. Res. **40** (2010) 395.
[22] J. E. Fromm, *Numerical calculation of the fluid dynamics of drop-on-demand jets*, IBM J. Res. Dev. **28** (1984) 322.
[23] R. R. Chance, A. Prock, R. Silbey, *Molecular fluorescence and energy transfer near interfaces*, Adv. Chem. Phys. **37** (1978) 1.
[24] K. H. Drexhage, *Influence of a dielectric interface on fluorescence decay time*, J. Lumin. **1–2** (1970) 693.
[25] K. Neyts, *Simulation of light emission from thin-film microcavities*, J. Opt. Soc. Am. A **15** (1998) 962.
[26] W. Brütting, J. Frischeisen, T. D. Schmidt, B. J. Scholz, C. Mayr, *Device efficiency of organic light-emitting diodes*, Phys. Status Solidi A **210** (2013) 44.
[27] M. A. Baldo et al., *Highly efficient phosphorescent emission from organic electroluminescent devices*, Nature **395** (1998) 151.
[28] N. C. Giebink, S. R. Forrest, *Quantum efficiency roll-off at high brightness in fluorescent and phosphorescent OLEDs*, Phys. Rev. B **77** (2008) 235315.
[29] U. Rau, *Reciprocity relation between photovoltaic quantum efficiency and electroluminescent emission of solar cells*, Phys. Rev. B **76** (2007) 085303.
[30] K. Vandewal et al., *On the origin of the open-circuit voltage of polymer–fullerene solar cells*, Nat. Mater. **8** (2009) 904.
[31] J. Benduhn et al., *Intrinsic non-radiative voltage losses in fullerene-based organic solar cells*, Nat. Energy **2** (2017) 17053.
[32] D. A. Bernards, G. G. Malliaras, *Steady-state and transient behavior of organic electrochemical transistors*, Adv. Funct. Mater. **17** (2007) 3538.
[33] J. Rivnay et al., *Organic electrochemical transistors*, Nat. Rev. Mater. **3** (2018) 17086.
[34] S. D. Kang, G. J. Snyder, *Charge-transport model for conducting polymers*, Nat. Mater. **16** (2017) 252.
[35] O. Bubnova et al., *Semi-metallic polymers*, Nat. Mater. **13** (2014) 190.
[36] B. Russ, A. Glaudell, J. J. Urban, M. L. Chabinyc, R. A. Segalman, *Organic thermoelectric materials for energy harvesting and temperature control*, Nat. Rev. Mater. **1** (2016) 16050.
[37] J. L. Beuth, *Cracking of thin bonded films in residual tension*, Int. J. Solids Struct. **29** (1992) 1657.
[38] J. W. Hutchinson, Z. Suo, *Mixed mode cracking in layered materials*, Adv. Appl. Mech. **29** (1992) 63.
[39] S. P. Lacour, S. Wagner, Z. Huang, Z. Suo, *Stretchable gold conductors on elastomeric substrates*, Appl. Phys. Lett. **82** (2003) 2404.
[40] D.-H. Kim et al., *Epidermal electronics*, Science **333** (2011) 838.
[41] G. L. Graff et al., *Mechanisms of vapor permeation through multilayer barrier films*, J. Appl. Phys. **96** (2004) 1840.
[42] P. E. Burrows et al., *Gas permeation and lifetime tests on polymer-based barrier coatings*, Appl. Phys. Lett. **65** (1994) 2922.
[43] L. E. Nielsen, *Models for the permeability of filled polymer systems*, J. Macromol. Sci. A **1** (1967) 929.
[44] R. Metzler, J. Klafter, *The random walk's guide to anomalous diffusion*, Phys. Rep. **339** (2000) 1.
[45] D. S. Peck, *Comprehensive model for humidity testing correlation*, Proc. IEEE IRPS (1986) 44.
[46] M. J. M. Pelgrom, A. C. J. Duinmaijer, A. P. G. Welbers, *Matching properties of MOS transistors*, IEEE J. Solid-State Circuits **24** (1989) 1433.
[47] J. Veres, S. D. Ogier, S. W. Leeming, D. C. Cupertino, S. M. Khaffaf, *Low-k insulators as the choice of dielectrics in organic field-effect transistors*, Adv. Funct. Mater. **13** (2003) 199.
[48] H. Sirringhaus, *25th anniversary article: organic field-effect transistors — the path beyond amorphous silicon*, Adv. Mater. **26** (2014) 1319.
[49] W. Shockley, H. J. Queisser, *Detailed balance limit of efficiency of p-n junction solar cells*, J. Appl. Phys. **32** (1961) 510.
[50] L. J. A. Koster, V. D. Mihailetchi, P. W. M. Blom, *Bimolecular recombination in polymer/fullerene bulk heterojunction solar cells*, Appl. Phys. Lett. **88** (2006) 052104.
[51] K. Hecht, *Zum Mechanismus des lichtelektrischen Primärstromes in isolierenden Kristallen*, Z. Phys. **77** (1932) 235.
[52] H. Uoyama, K. Goushi, K. Shizu, H. Nomura, C. Adachi, *Highly efficient organic light-emitting diodes from delayed fluorescence*, Nature **492** (2012) 234.
[53] D. M. Mathijssen et al., *Dynamics of threshold-voltage shifts in organic and amorphous silicon field-effect transistors*, Phys. Rev. Lett. **99** (2007) 066601.
[54] M. Nikolka et al., *High operational and environmental stability of high-mobility conjugated polymer field-effect transistors*, Nat. Mater. **16** (2017) 356.
[55] M. C. J. M. Vissenberg, M. Matters, *Theory of the field-effect mobility in amorphous organic transistors*, Phys. Rev. B **57** (1998) 12964.
[56] S. R. Forrest, *The path to ubiquitous and low-cost organic electronic appliances on plastic*, Nature **428** (2004) 911.

---

*Manuscript ends. All numbered results not explicitly attributed to prior work are proved here under the stated hypotheses. Items labelled Claim, Conjecture, or Open Problem carry stated closures and are flagged at every point of use; none is load-bearing for a theorem without such flagging. Results inherited from Paper I are cited as [I, …] and are not re-proved.*
