# The Organic Transistor

## A Unified Field Theory of Gate-Modulated Transport in Disordered Mixed Conductors

**Preprint — 23 November 2026**

---

### Abstract

We construct a closed, self-consistent field theory of the organic transistor and derive its device equations as controlled asymptotic reductions rather than as postulated compact models. The central claim is structural: the organic field-effect transistor (OFET) and the organic electrochemical transistor (OECT) are not distinct device classes but boundary-controlled instances of a single degenerate gradient flow on a mixed ionic–electronic conductor, distinguished by the *codimension of the gate's action* on the state manifold. From this axiomatization we derive: (i) an exact first integral of the equilibrium accumulation-layer problem — the Maxwell stress equals the carrier osmotic pressure, ε E²/2 = p(n) — valid for arbitrary statistics and density of states, yielding a confinement-length trichotomy and the closed form ℓ = 2ε k_BT/(q C_i A) in the nondegenerate limit; (ii) a tensorial homogenization of the Miller–Abrahams/Marcus hopping network, with a variational characterization of the effective mobility tensor μ^{ij}, an arithmetic–harmonic duality for layered films, and an exact parity–analyticity obstruction ruling out Poole–Frenkel behaviour as a zero-field asymptote; (iii) an identifiability theory of mobility extraction, comprising an infinite-dimensional fibre theorem in the linear regime, a constructive identification theorem on the saturation branch, and an explicit one-parameter degeneracy that survives gate-only contact models; (iv) a universal gain–delay identity f_T·τ = (2π)^{−1} ∂ln I_D/∂ln Q, exact under the gradual-channel approximation for any μ(n); (v) a gain–bandwidth invariance theorem for OECTs, proving that g_m·f_c is independent of film thickness and volumetric capacitance in the ion-limited regime; and (vi) a dispersion–noise duality α + β = 1 linking the fractional order of trap-limited transport to the exponent of drain-current 1/f^β noise. All results are proved under explicitly stated hypotheses; §10 catalogues the failure modes, counterexamples, and open problems. Numerical parameter regimes are tabulated and nine falsifiable predictions are stated.

**MSC 2020.** 35Q81, 35R60, 82D37, 82C41, 26A33, 49S05, 93B30, 35B40.

**Keywords.** organic field-effect transistor; organic electrochemical transistor; hopping transport; Gaussian disorder; stochastic homogenization; generalized Einstein relation; gradient flow; identifiability; fractional transport; transconductance.

---

## 1. Introduction

### 1.1 The object of study

An organic transistor is a three-terminal device in which the current-carrying medium is a van-der-Waals-bonded molecular or polymeric solid, and in which the control terminal modulates the population — and, in the electrochemical case, the chemical identity — of the mobile charge carriers. The defining physical facts are three, and they are quantitative rather than qualitative:

1. **Energetic disorder dominates thermal energy.** Site energies are distributed with standard deviation σ ≈ 50–150 meV, so σ̂ ≡ σ/k_BT ≈ 2–6 at 300 K. Band transport is not the generic regime; it is the exception.
2. **The permittivity is small.** ε_r ≈ 3–4, whence the Onsager capture radius r_c = q²/(4πε k_BT) ≈ 16 nm at 300 K, an order of magnitude larger than the intermolecular spacing. Coulomb interactions are unscreened on the scale of the microstructure.
3. **The lattice is soft and permeable.** Polaron reorganization energies λ_r ≈ 0.1–0.3 eV are comparable to electronic transfer integrals J ≈ 10–100 meV, and small ions can enter the bulk. Electronic and ionic charge are therefore *co-variables*, not separate problems.

Each of these facts invalidates a standard silicon-device idealization. Together they demand a theory in which the transport coefficients are functionals of the state, the electrostatics is nonlinear beyond the Debye–Hückel regime, and the gate may act volumetrically.

### 1.2 Why a field theory is needed

The literature on organic transistors is rich in compact models and poor in identifiability. The practical consequence is a measurement crisis: reported mobilities for the same material span two orders of magnitude, and non-ideal transfer characteristics — double slopes, "kinks", apparent threshold shifts — are routinely attributed to material physics when they are consequences of the extraction procedure. This is not a sociological problem. It is a mathematical one: the inverse problem "given I_D(V_G, V_D), recover μ(n) and the contact law" has, as we prove in §7, an infinite-dimensional fibre. No amount of measurement precision resolves it. What resolves it is a structural theorem identifying which branch of the characteristic is contact-immune, and under what hypotheses.

Our programme is therefore: *derive the device equation as a theorem, then derive the extraction procedure as a theorem, then derive the figures of merit as theorems.* Compact models appear only as leading-order terms with error estimates attached.

### 1.3 Statement of contributions

Numbered results below are proved in the text unless explicitly labelled **Claim** (asymptotic, under a stated closure) or **Conjecture**.

- **T1 (§2).** Port–gradient-flow formulation: the governing system is a degenerate gradient flow of a free-energy functional ℱ with density-dependent dissipation metric; the exact port–dissipation identity dℱ/dt = Σ_k V_k I_k − 𝔇 holds, and the OFET/OECT distinction is the codimension of the gate constraint (Definition 2.7).
- **T2 (§3).** Exact first integral ε E²/2 = p(n) (Theorem 3.3); confinement-length trichotomy for p ∝ n^m (Theorem 3.5); closed form ℓ = 2ε k_BT/(q C_i A) and its disorder renormalization k_BT ↦ E_c (Corollaries 3.6–3.8); anisotropic geometric-mean permittivity lemma (Lemma 3.2).
- **T3 (§4).** Variational characterization and homogenization of the hopping mobility tensor (Theorems 4.3–4.4); arithmetic–harmonic layer duality (Proposition 4.6); exact equilibrium energy ε_∞ = −σ²/k_BT and the sharp-mobility-edge bound c ≤ 1/2 on the disorder exponent (Proposition 4.10); parity–analyticity obstruction to Poole–Frenkel asymptotics (Theorem 4.12).
- **T4 (§5).** Fractional transport theorem: exponential trap tails of characteristic energy E_c generate a Riemann–Liouville time-fractional drift–diffusion equation of order α = k_BT/E_c, with the generalized Einstein ratio invariant under subordination (Theorem 5.5).
- **T5 (§6).** Gradual-channel reduction as a two-scale solvability condition with O(ε) error and an explicit validity domain set by the scale length λ = √(ε_s t_s t_i/ε_i) (Theorem 6.3, Proposition 6.7); transmission-line contact theorem including the derived law R_c ∝ A^{−1/2} (Theorem 6.9).
- **T6 (§7).** Fibre theorem (Theorem 7.2), saturation-branch identification theorem (Theorem 7.5), residual-conductivity degeneracy (Proposition 7.9), fixed-V_D saturation-crossing artifact (Theorem 7.11), and a regularized inversion with an O(√(Mδ)) rate.
- **T7 (§8).** OECT reduction to the Bernards–Malliaras form at leading order (Theorem 8.4); gain–bandwidth invariance (Theorem 8.8).
- **T8 (§9).** Universal gain–delay identity (Theorem 9.2); attempt-frequency ceiling on f_T; dispersion–noise duality α + β = 1 (Theorem 9.9); exact subthreshold-swing bound and its trap renormalization.

### 1.4 Relation to prior work; what is new

The individual ingredients are classical: Miller–Abrahams rates [1], critical-path percolation [2], the Gaussian disorder model [3] and its density-dependent extension [4,5], variable-range-hopping field-effect mobility [6], multiple-trap-and-release transport [7,8], fractional CTRW [9,10], the Bernards–Malliaras OECT model [11], the generalized Einstein relation [12], stochastic homogenization of random conductances [13–15], and the variational structure of Fokker–Planck and Poisson–Nernst–Planck systems [16,17].

What is new here is the *architecture and the inverse theory*. Specifically: the osmotic-pressure first integral and the resulting confinement trichotomy (T2); the identification of the sheet-charge Coulomb kernel with the geometric-mean permittivity in anisotropic films (Lemma 3.2); the parity–analyticity obstruction (T3); the fibre and identification theorems together with the explicit residual-conductivity degeneracy and the saturation-crossing artifact (T6); the universal gain–delay identity (T8); the OECT gain–bandwidth invariance theorem (T7); and the statement of dispersion–noise duality as an exact exponent sum rule with a common microscopic parameter (T8). The codimension classification of gate action (T1) is, to our knowledge, the first formulation in which OFET and OECT are literally the same equation with different boundary codimension.

We are explicit where a numerical constant is inherited rather than derived: the value c = 4/9 in the Gaussian disorder exponent (§4.6) is a critical-path closure constant corroborated by Monte Carlo simulation [3], not a theorem of this paper. We prove the *scaling law* and bound the constant.

### 1.5 Notation and conventions

Latin indices i, j, k ∈ {1,2,3} label spatial components in a fixed Cartesian frame on Ω ⊂ ℝ³; repeated indices are summed; the ambient metric is δ_ij, so index position is cosmetic and we write μ^{ij}, ε^{ij}, D^{ij} for the components of (2,0)-tensors and μ^i{}_j for the associated (1,1)-tensor. Coordinates x^i = (x¹, x², x³) with x¹ along the channel, x³ ≡ z normal to the dielectric interface, z = 0 at the semiconductor/dielectric plane and z increasing into the film.

q > 0 is the elementary charge. E_i = −∂_iφ. ε^{ij} is the *absolute* permittivity tensor (F m⁻¹); ε without index denotes its isotropic value or ε_s where ambiguity is possible. β = (k_BT)^{−1}. n, p are electron and hole volume densities (m⁻³); c_± ionic densities; N_s the sheet density (m⁻²); σ_s the sheet conductance (S, i.e. S per square); C_i the areal gate capacitance (F m⁻²); C* the volumetric capacitance (F m⁻³). μ denotes mobility magnitude (m² V⁻¹ s⁻¹) and μ^{ij} its tensor. A ≡ V_G − V_th is the overdrive. σ (no subscript) is the disorder width; σ̂ ≡ σ/k_BT. a is the localization length; ν₀ the attempt frequency. L, W, d (or t_s) are channel length, width, film thickness; t_i the dielectric thickness.

Equations are displayed in plain-text mathematics with `_` for subscripts and `^` for superscripts; ∂_i denotes partial differentiation; ⟨·⟩ denotes ensemble average; ∎ terminates a proof. Numerical values use SI internally and report Å/nm/cm² where the literature does.

---

## 2. Kinematics, Thermodynamics, and the Port Structure

### 2.1 The state manifold

**Definition 2.1 (Mixed conductor).** A *mixed ionic–electronic conductor* on a bounded Lipschitz domain Ω ⊂ ℝ³ is a quadruple u = (n, p, c_+, c_−) of nonnegative densities in L¹(Ω), together with a fixed background ρ_fix ∈ L^∞(Ω), subject to the elliptic constraint

  ∂_i(ε^{ij} ∂_j φ) = −ρ,  ρ = q(p − n + c_+ − c_−) + ρ_fix,  (2.1)

with φ prescribed on the gate and ohmic contacts and ε^{ij}∂_jφ n_i prescribed elsewhere. Uniform ellipticity 0 < ε₋|ξ|² ≤ ε^{ij}ξ_iξ_j ≤ ε₊|ξ|² is assumed throughout.

The constraint (2.1) makes φ a *nonlocal functional* of u; this is the source of every essential difficulty and of every essential structure below.

### 2.2 Statistics, chemical potential, osmotic pressure

Let g(ε) be the density of transport-site energies per unit volume, normalized ∫g = N. Occupation is Fermi–Dirac; write

  n(ζ) = ∫ g(ε) f(ε − ζ) dε,  f(x) = (1 + e^{βx})^{−1},  (2.2)

with ζ the electronic chemical potential measured in the same reference as ε. We assume g such that ζ ↦ n is a strictly increasing C² bijection onto (0, N); this holds for Gaussian, exponential, and parabolic-band g. Denote its inverse ζ_e(n), and likewise ζ_h(p), ζ_±(c_±).

**Definition 2.2 (Osmotic potential and pressure).** Define

  Ψ_a(u) = ∫₀^u ζ_a(s) ds,  p_a(u) = u ζ_a(u) − Ψ_a(u) = ∫₀^u s ζ_a′(s) ds.  (2.3)

Ψ_a is the grand-potential density; p_a is the osmotic pressure. The second equality in (2.3) follows by integration by parts and is the Gibbs–Duhem relation dp = u dζ at fixed T. Ψ_a is strictly convex since Ψ_a″ = ζ_a′ > 0.

Three cases recur:

| regime | ζ(n) | p(n) | exponent m in p ∝ n^m |
|---|---|---|---|
| nondegenerate (Boltzmann) | k_BT ln(n/N₀) | n k_BT | 1 |
| exponential tail, width E_c ≫ k_BT | E_c ln(n/N₁) | n E_c | 1 |
| 2D constant DOS (degenerate) | n/g₂ | n²/(2g₂) | 2 |
| 3D parabolic band (degenerate) | ∝ n^{2/3} | ∝ n^{5/3} | 5/3 |

The exponential-tail entry is derived, not assumed; see Lemma 5.2.

### 2.3 The generalized Einstein relation, tensorial form

Let μ_a^{ij} be the mobility tensor of species a (constructed in §4), symmetric positive semidefinite, and let the particle flux be

  Γ_a^i = s_a μ_a^{ij} u_a E_j − D_a^{ij} ∂_j u_a,  s_e = s_− = −1, s_h = s_+ = +1.  (2.4)

**Proposition 2.3 (Generalized Einstein relation).** Vanishing flux at equilibrium for arbitrary imposed potential gradients is equivalent to

  D_a^{ij} = (1/q) (∂p_a/∂u_a) μ_a^{ij} = (1/q) u_a ζ_a′(u_a) μ_a^{ij}.  (2.5)

*Proof.* At equilibrium the electrochemical potential μ̄_a = ζ_a(u_a) + s_a qφ is spatially constant, so ζ_a′(u_a) ∂_j u_a = −s_a q ∂_jφ = s_a q E_j. Substituting into (2.4),

  Γ_a^i = s_a μ_a^{ij} u_a E_j − D_a^{ij} ζ_a′(u_a)^{−1} s_a q E_j = s_a [u_a μ_a^{ij} − q D_a^{ij}/ζ_a′(u_a)] E_j.

Since E_j is arbitrary (the equilibrium constraint fixes only μ̄_a, not φ pointwise), the bracket vanishes, giving (2.5). Conversely (2.5) makes Γ_a ≡ 0 whenever μ̄_a is constant. ∎

**Corollary 2.4.** In the nondegenerate limit (2.5) reduces to D^{ij} = (k_BT/q) μ^{ij}. In the exponential-tail regime k_BT is replaced by E_c: *disorder enhances diffusion relative to drift by the factor E_c/k_BT = α^{−1}.* This single factor reappears in the confinement length (§3), the fractional order (§5), and the noise exponent (§9).

**Remark 2.5.** Proposition 2.3 is a statement about *equilibrium*. Its extension to a biased device is a hypothesis, not a theorem; see Hypothesis H3 and §10.3.

### 2.4 Free energy and the gradient structure

Define the total free energy

  ℱ[u] = ∫_Ω [Ψ_e(n) + Ψ_h(p) + Ψ_+(c_+) + Ψ_−(c_−)] dx
    + ½ ∫_Ω ε^{ij} ∂_iφ ∂_jφ dx + ∫_Ω ρ_fix φ dx + ∫_Ω Σ_± ΔG_± c_± dx,  (2.6)

with ΔG_± the ion-insertion free energies (zero for an ion-impermeable film, formally ΔG_± → +∞). The last term encodes the chemistry of the mixed conductor.

**Lemma 2.6.** δℱ/δu_a = ζ_a(u_a) + s_a qφ + ΔG_a = μ̄_a + ΔG_a.

*Proof.* Variation of the electrostatic term with (2.1) gives δ(½∫ε|∇φ|² + ∫ρ_fixφ)/δu_a = s_a qφ after integrating by parts and using the symmetry of ε^{ij}; the Ψ terms give ζ_a directly. ∎

**Theorem 2.7 (Port–gradient-flow structure).** The transport equations

  ∂_t u_a = ∂_i [ (u_a/q) μ_a^{ij} ∂_j (δℱ/δu_a) ]  (2.7)

are (i) equivalent to (2.4) with (2.5); (ii) a degenerate gradient flow of ℱ with respect to the density-weighted metric M_a^{ij} = (u_a/q)μ_a^{ij}; and (iii) satisfy the exact port–dissipation identity

  dℱ/dt = Σ_k V_k I_k − 𝔇,  𝔇 = Σ_a (1/q) ∫_Ω u_a μ_a^{ij} ∂_iμ̄_a ∂_jμ̄_a dx ≥ 0,  (2.8)

the sum running over terminals with prescribed potentials V_k and outward currents I_k.

*Proof.* (i) Expand (2.7) using Lemma 2.6: (u_a/q)μ_a^{ij}∂_j(ζ_a + s_aqφ) = (u_aζ_a′/q)μ_a^{ij}∂_ju_a + s_a u_a μ_a^{ij}∂_jφ = D_a^{ij}∂_ju_a − s_a μ_a^{ij}u_a E_j = −Γ_a^i. Hence (2.7) is ∂_tu_a = −∂_iΓ_a^i.

(ii) Immediate from (i), convexity of Ψ_a, and positive semidefiniteness of μ_a^{ij} (Theorem 4.4).

(iii) dℱ/dt = Σ_a ∫ (δℱ/δu_a) ∂_tu_a = Σ_a ∫ μ̄_a ∂_i[(u_a/q)μ_a^{ij}∂_jμ̄_a] (the ΔG_a are constants and the total species mass changes only through terminals). Integrate by parts: the volume term is −𝔇, nonnegative because μ_a^{ij} ⪰ 0 and u_a ≥ 0. The boundary term is Σ_a ∮ μ̄_a (u_a/q)μ_a^{ij}∂_jμ̄_a n_i. On an ohmic contact held at V_k, local equilibrium gives μ̄_a = s_a q V_k + const, and the surface integral of the flux is the terminal current; summing species yields Σ_k V_kI_k. On insulating boundaries the flux vanishes. ∎

**Definition 2.8 (Codimension of gate action).** Let 𝒢 ⊂ ∂Ω ∪ Ω be the support of the gate-induced constraint. The gate is of *codimension one* (interfacial) if the gate datum acts only through a boundary condition on a surface, and of *codimension zero* (volumetric) if it acts through a bulk field coupled to a conserved species present in Ω.

**Corollary 2.9 (Passivity and the meaning of transconductance).** In steady state dℱ/dt = 0 and Σ_kV_kI_k = 𝔇: all delivered power is dissipated. An ideally capacitive gate has I_G = 0 and contributes *no power*; it acts solely by deforming the constraint set, hence the minimizer of 𝔇 at fixed source–drain bias. Transconductance is therefore the sensitivity of a dissipation-minimizing flux to a *constraint parameter*, not to an injected power. A volumetric gate (OECT) is a genuine port: it injects ions, does work, and stores it in the bulk. This is the precise sense in which the OECT buys transconductance with gate charge.

We quantify the distinction by the dimensionless **penetration number**

  Π ≡ C* d / C_i,  (2.9)

with C* ≡ q² ∂p/∂ζ the volumetric chemical capacitance. Π ≪ 1: interfacial (OFET, electrolyte-gated OFET). Π ≫ 1: volumetric (OECT). For PEDOT:PSS, C* ≈ 40 F cm⁻³ = 4×10⁷ F m⁻³, d = 100 nm, C_i = 10 nF cm⁻² = 10⁻⁴ F m⁻²: Π ≈ 4×10⁴. The two device families are the two ends of a single parameter axis.

---

## 3. Electrostatics of the Channel: Exact Results

### 3.1 Anisotropy

Molecular crystals are dielectrically anisotropic: ε^{ij} = diag(ε_∥, ε_∥, ε_⊥) in the film frame, with anisotropy ratios up to ~2.

**Lemma 3.1 (Affine reduction).** Under x¹ = √(ε_∥/ε_⊥) x̃¹, x² = √(ε_∥/ε_⊥) x̃², x³ = x̃³, equation (2.1) becomes ε_⊥ ∇̃²φ = −ρ̃ with ρ̃ = ρ (densities per unit *physical* volume transform with the Jacobian; sheet densities N_s are invariant). Consequently every purely vertical (z-only) electrostatic result holds with ε → ε_⊥, and lateral lengths in the equivalent isotropic problem are compressed by √(ε_⊥/ε_∥).

*Proof.* Direct substitution; ε_∥(ε_⊥/ε_∥)∂_x̃² + ε_⊥∂_z² = ε_⊥(∂_x̃¹² + ∂_x̃²² + ∂_z²). ∎

**Lemma 3.2 (Geometric-mean permittivity for sheet charges).** Let a sheet charge density σ₂ e^{ik·x_∥} sit at z = 0 in an unbounded anisotropic medium. Then the potential on the sheet is

  φ̂(k) = σ₂ / (2|k| √(ε_∥ ε_⊥)).  (3.1)

Hence all *in-plane* Coulomb interactions in the accumulation layer — carrier–carrier, carrier–trap, exciton binding within the sheet — are governed by the geometric mean ε_eff = √(ε_∥ε_⊥), not by either principal value.

*Proof.* Away from z = 0, (2.1) with ρ = 0 gives ε_∥(−k²)φ̂ + ε_⊥φ̂″ = 0, so φ̂ ∝ e^{−|k|z√(ε_∥/ε_⊥)} for z > 0 and the mirror image for z < 0. The jump condition ε_⊥[∂_zφ̂]_{0⁻}^{0⁺} = −σ₂ gives −2ε_⊥|k|√(ε_∥/ε_⊥) φ̂(0) = −σ₂, i.e. (3.1). ∎

**Corollary 3.3.** The in-sheet Onsager radius is r_c = q²/(4π√(ε_∥ε_⊥) k_BT). For ε_∥ = 4ε₀, ε_⊥ = 3ε₀ at 300 K, r_c = 16.1 nm. The accumulation layer is thus a strongly correlated two-dimensional plasma on the scale of its own thickness — a fact silently discarded by every drift–diffusion compact model, including ours (§10.4).

### 3.2 The first integral

Consider equilibrium in the film, z > 0, with no flux, negligible background doping, and n → 0, E → 0 as z → ∞. Isotropic notation (ε ≡ ε_⊥ by Lemma 3.1).

**Theorem 3.4 (Maxwell stress = osmotic pressure).** Under the above conditions,

  ½ ε E_z(z)² = p(n(z))  for all z > 0.  (3.2)

*Proof.* Zero flux gives ζ_e(n) − qφ = const, hence ζ_e′(n)n′ = qφ′. Poisson (2.1) with ρ = −qn gives εφ″ = qn. Multiply by φ′:

  ε φ″φ′ = q n φ′ = n ζ_e′(n) n′ = p′(n) n′ = (p(n))′,

using Definition 2.2. The left side is (½ε(φ′)²)′. Integrating and using the decay conditions to fix the constant at zero yields (3.2) with E_z = −φ′. ∎

This identity is exact for arbitrary g, arbitrary degeneracy, and arbitrary temperature. It states that the electrostatic tension pulling carriers toward the interface is balanced pointwise by their osmotic pressure. It is the mechanical content of the accumulation layer.

**Corollary 3.5 (Surface density and confinement length).** Let N_s = ∫₀^∞ n dz and define ℓ ≡ N_s/n(0). Gauss's law at the interface, ε|E_z(0)| = qN_s, combined with (3.2) gives

  p(n(0)) = q²N_s²/(2ε),  (3.3)

which determines n(0) implicitly for any statistics. In the nondegenerate case p = nk_BT:

  n(0) = q²N_s²/(2ε k_BT),  ℓ = 2ε k_BT/(q² N_s) = 2ε (k_BT/q)/(C_i A),  (3.4)

where the last step uses qN_s = C_iA (charge-sheet gate relation, all induced charge mobile).

Equation (3.4) is the central electrostatic result of this paper. It is closed-form, parameter-free, and says that **the channel thickness is inversely proportional to overdrive**: the gate compresses the channel electrostatically.

**Theorem 3.6 (Confinement trichotomy).** Suppose p(n) = K n^m with K > 0, m > 0. Then the equilibrium profile is obtained by the quadrature

  z(n) = (√(2ε)/q) ∫_n^{n₀} (1/s) (d√p/ds) ds,  n₀ = n(0),  (3.5)

and:

1. **m < 2:** algebraic decay, n(z) ≍ z^{−2/(2−m)} as z → ∞; explicitly
  n(z) = n₀ (1 + z/ℓ_m)^{−2/(2−m)}, ℓ_m = [2(2−m)/m]·(√(2εK)/q)·n₀^{(m−2)/2}·(m/2).
  For m = 1 this is exactly n(z) = n₀(1 + z/ℓ)⁻² with ℓ = √(2εk_BT/(q²n₀)), consistent with (3.4).
2. **m = 2:** exponential decay, n(z) = n₀ e^{−z/ℓ₂}, ℓ₂ = √(2Kε)/q.
3. **m > 2:** compact support. n vanishes identically beyond a finite depth z_* < ∞; the accumulation layer has a sharp edge.

*Proof.* From (3.2), φ′ = −√(2p/ε) (field directed so as to attract electrons), and ζ_e′ n′ = qφ′ gives n′ = −(q/ζ_e′)√(2p/ε). Since ζ_e′ = p′/n = n ζ_e′... more directly, ζ_e′ = p′(n)/n, so n′ = −(q n/p′)√(2p/ε) and dz = −(p′/(qn))√(ε/2) dp^{1/2}·... using p′/(n√p) = (2/n) d√p/dn we obtain (3.5). For p = Kn^m, d√p/ds = (m/2)√K s^{m/2−1}, so the integrand is (m/2)√K s^{m/2−2}. Integrating from n to n₀:

  z(n) = (√(2ε)/q)(m/2)√K · [s^{m/2−1}/(m/2−1)]_n^{n₀}.

If m < 2 the exponent m/2 − 1 < 0, the bracket is dominated by n^{m/2−1} for n ≪ n₀, and solving for n gives the stated algebraic law with exponent −1/(1 − m/2) = −2/(2−m). If m = 2 the integral is logarithmic, giving exponential decay. If m > 2 the exponent is positive and z(n → 0) is finite, equal to z_* = (√(2ε)/q)(m/2)√K n₀^{m/2−1}/(m/2−1). ∎

**Remark 3.7.** The trichotomy is physically complete: m = 1 covers Boltzmann and exponential-tail statistics; m = 2 is the degenerate two-dimensional gas (constant 2D DOS), i.e. exactly the monolayer limit; m = 5/3 is the degenerate three-dimensional band. The compact-support case m > 2 is the Thomas–Fermi-like sharp-edge regime and is not realized in organic films at accessible densities, but it delimits the theory.

**Corollary 3.8 (Disorder renormalization of the channel thickness).** In the exponential-tail regime p = nE_c (Lemma 5.2), so (3.4) becomes

  ℓ = 2ε E_c/(q C_i A) = (E_c/k_BT)·ℓ_Boltzmann = α^{−1} ℓ_Boltzmann.  (3.6)

Energetic disorder *spreads* the channel by exactly the inverse fractional order.

### 3.3 Numbers, and the theory's own boundary of validity

Take ε_s = 3.5ε₀ = 3.10×10⁻¹¹ F m⁻¹, a polymer dielectric with ε_i = 3ε₀ and t_i = 300 nm, so C_i = 8.85×10⁻⁵ F m⁻² (8.85 nF cm⁻²). At A = 10 V: N_s = C_iA/q = 5.52×10¹⁵ m⁻² (5.5×10¹¹ cm⁻²), and

  ℓ_Boltzmann = 2(3.10×10⁻¹¹)(0.02585)/(8.85×10⁻⁴) = 1.81 nm.

With E_c = 100 meV, α = 0.2585 and ℓ = 7.0 nm. Both are small compared with a 30–100 nm film; the former is *one to two molecular monolayers*. This is the rigorous justification of the two-dimensional reduction: **the OFET channel is a monolayer-scale object, and μ_FE is an interface measurement, not a bulk measurement.**

Now push the gate: an electrolyte or ionic-liquid dielectric with C_i ≈ 10 µF cm⁻² = 10⁻¹ F m⁻² at A = 1 V gives qN_s = 0.1 C m⁻² and (3.4) returns ℓ = 1.6×10⁻¹¹ m = 0.016 nm — smaller than a nucleus. The formula has not failed arithmetically; it has failed *physically*, and it announces its own failure. The correct reading: at such C_iA the nondegenerate assumption p ∝ n is untenable, the continuum description of a molecular lattice is untenable, and the system crosses to m ≥ 2 statistics (exponential/sharp-edge confinement, Theorem 3.6) or to volumetric doping (Π ≫ 1). The dimensionless validity conditions are

  ℓ ≫ a_mol (≈ 0.5–1.5 nm)  and  n(0) ≪ N (site density).  (3.7)

Violation of (3.7) is precisely the OFET → OECT crossover. The theory thus contains its own phase boundary.

---

## 4. The Dissipation Metric: Hopping Transport

### 4.1 Microscopic dynamics

Let {x_i} be a stationary ergodic point process of transport sites in ℝ³ with intensity N, decorated with i.i.d. site energies ε_i ~ g. The carrier performs a Markov jump process with rates

  Miller–Abrahams: ν_ij = ν₀ e^{−2r_ij/a} · min{1, e^{−β(Δε_ij + qF·r_ij)}}, r_ij = x_j − x_i,  (4.1)

  Marcus: ν_ij = (2π/ħ)|J_ij|² (4πλ_r k_BT)^{−1/2} exp[−(Δε_ij + qF·r_ij + λ_r)²/(4λ_r k_BT)],  (4.2)

with J_ij the transfer integral, λ_r the reorganization energy, F the local field. (4.1) is the λ_r → ∞ classical limit of (4.2) up to prefactors, with the asymmetry that upward hops pay activation and downward hops do not. Both satisfy detailed balance at F = 0 with respect to the Gibbs measure ∝ e^{−βε_i}.

**Hypothesis H1.** The point process is stationary and ergodic under translations; the energy decoration is i.i.d. and independent of positions; J_ij = J(r_ij) with |J(r)| ≤ J₀e^{−r/a}.

**Hypothesis H2 (Scale separation).** The disorder correlation length a_c ≡ max(a, N^{−1/3}) is small compared with the scale over which n and F vary: a_c ≪ min(ℓ, L, λ).

H2 is what licenses a *local* constitutive law μ^{ij}(n, F) at all. It fails inside the accumulation layer when ℓ ~ a_c (Corollary 3.8 with strong disorder), which is a genuine open problem (§10.2).

### 4.2 Homogenization and the variational principle

At F = 0 the process is reversible with symmetric edge conductances

  c_ij = β q² N^{-1} π_i ν_ij = c_ji,  π_i ∝ e^{−βε_i},  (4.3)

and the associated Dirichlet form on functions u on sites is

  𝔈(u,u) = ½ Σ_{i,j} c_ij (u_i − u_j)².  (4.4)

**Theorem 4.3 (Finite-volume variational characterization).** For a finite network with boundary sets 𝒜, ℬ, the effective conductance is

  C_eff = inf{ 𝔈(u,u) : u|_𝒜 = 1, u|_ℬ = 0 }  (Dirichlet principle),
  C_eff = sup{ |𝔧|²/𝔈*(𝔧,𝔧) : 𝔧 a unit 𝒜→ℬ flow }  (Thomson principle),

and C_eff is monotone nondecreasing in each c_ij (Rayleigh monotonicity).

*Proof.* Standard: 𝔈 is a positive quadratic form; the minimizer is the harmonic extension (discrete Laplace equation), and evaluation of 𝔈 at the minimizer equals the boundary flux. The dual follows by Legendre transform on the flow constraint. Monotonicity is immediate since the admissible set is unchanged and the objective increases pointwise in c. ∎

**Theorem 4.4 (Homogenized mobility tensor).** Assume H1 and uniform ellipticity 0 < c₋ ≤ c_ij ≤ c₊ for neighbours. Then there exists a deterministic, symmetric, positive-definite tensor D^{ij} such that, almost surely, the rescaled process converges to Brownian motion with covariance 2D^{ij}t, and

  ξ_i D^{ij} ξ_j = inf_{χ} ½ ⟨ Σ_j c_{0j} (ξ·r_{0j} + χ(ω, j) − χ(ω, 0))² ⟩,  (4.5)

the infimum over stationary, mean-zero, curl-free correctors χ. Moreover μ^{ij} = (q/k_BT) D^{ij} in the nondegenerate dilute limit, and μ^{ij} ⪰ 0 with equality only in the degenerate case c ≡ 0.

*Proof.* The convergence and the corrector formula are the Kozlov–Papanicolaou–Varadhan–Kipnis–Varadhan theory of random walks among random conductances [13–15]; the quadratic-form characterization (4.5) is the infinite-volume limit of Theorem 4.3 with affine boundary data, the infimum being over gradient perturbations of the affine field. Symmetry follows from reversibility (Onsager [18]); positive definiteness from (4.5) and irreducibility of the neighbour graph. The Einstein conversion is Proposition 2.3 in the dilute nondegenerate limit. ∎

**Remark 4.5 (Why the classical theorem is not enough).** Miller–Abrahams conductances (4.3) are log-heavy-tailed: c_ij spans e^{−2r/a−βΔε} over many decades. Uniform ellipticity *fails catastrophically* precisely in the regime σ̂ ≫ 1 that defines organic semiconductors. Theorem 4.4 therefore establishes structure (symmetry, positivity, variational bounds, monotonicity) but not the value of the exponent. The value requires critical-path asymptotics (§4.6). We regard the honest separation of these two statements as essential; conflating them is the origin of much confusion in the field.

### 4.3 Orientation and layer averaging

**Proposition 4.6 (Anisotropy and the arithmetic–harmonic duality).** Let t^i be the unit vector along the channel. Then:

1. The measured channel mobility is the contraction μ_t = t^i μ_ij t^j. In a single-crystal film with in-plane principal mobilities μ₁, μ₂ and channel at angle θ to axis 1, μ_t(θ) = μ₁cos²θ + μ₂sin²θ. Extremal orientations are the principal axes; no orientation exceeds max(μ₁,μ₂).
2. For a layered film with layer thicknesses d_l and layer sheet densities N_l, the in-plane sheet conductance is the *arithmetic* (parallel) mean, σ_s = Σ_l q μ_t,l N_l, so μ_FE = Σ_l μ_t,l N_l / Σ_l N_l: transport is dominated by the **best** layers.
3. Out-of-plane (contact-injection) transport is the *harmonic* (series) mean, R_⊥ = Σ_l d_l/σ_⊥,l: transport is dominated by the **worst** layers.

*Proof.* (1) is the definition of the contraction together with symmetry of μ_ij and the elementary trigonometric identity. (2) follows from current continuity in parallel channels sharing a common lateral field: total current is the sum of layer currents, each σ_l E, and the sheet density is the sum. (3) follows from current continuity in series: the same normal current density crosses each layer, so potential drops add, i.e. resistances add. ∎

**Corollary 4.7.** Combining with Corollary 3.5: since ℓ ≈ 1–2 nm, only the first one or two monolayers carry appreciable N_l, and μ_FE is a weighted average dominated by the *interfacial* monolayer. This proves, rather than asserts, the extreme sensitivity of OFET mobility to dielectric surface chemistry, and the coexistence of high FET mobility with poor diode injection in the same film.

### 4.4 Exact scaling structure

**Proposition 4.8 (Scaling form).** Under H1–H2 with Miller–Abrahams rates, the homogenized mobility obeys the exact dimensional reduction

  μ^{ij} = (q ν₀ a²/k_BT) · 𝔐^{ij}(σ̂, n a³, qFa/σ, a N^{1/3}),  (4.6)

with 𝔐^{ij} a dimensionless tensor function of four dimensionless groups.

*Proof.* Buckingham Π on the parameter set {ν₀, a, k_BT, σ, n, F, q, N}; ν₀a²q/k_BT has the dimensions of mobility, and the four listed groups are a complete independent set. ∎

This is a strong constraint on admissible compact models: any proposed μ(n, F, T) must be expressible in these variables. The extended Gaussian disorder model [4,5] is, correctly, a fit to 𝔐.

**Lemma 4.9 (Exact equilibrium energy).** For Gaussian g with mean 0 and variance σ², in the nondegenerate limit the mean occupied site energy is exactly

  ε_∞ = ⟨ε⟩_eq = −σ²/k_BT = −σ̂ σ.  (4.7)

*Proof.* ⟨ε⟩_eq = ∫ε g(ε)e^{−βε}dε / ∫g(ε)e^{−βε}dε. Completing the square, g(ε)e^{−βε} ∝ exp[−(ε + σ²β)²/(2σ²)], a Gaussian of mean −σ²β and variance σ². ∎

Equation (4.7) is exact and is the anchor of all activation arguments: carriers relax to a level *below* the DOS centroid by σ̂ standard deviations. Simultaneously ∫g e^{−βε} = N e^{σ̂²/2}, the Boltzmann partition enhancement that will produce the disorder exponent.

### 4.5 Traps and the density dependence

**Lemma 4.10 (Exponential tail: exact filling law).** Let g_t(ε) = (N_t/E_c)e^{ε/E_c} for ε ≤ 0 (transport edge at 0), E_c > k_BT, and ζ ≪ −k_BT. Then

  n_t = N_t e^{ζ/E_c}/(1 − α),  α ≡ k_BT/E_c,  p_t(n_t) = n_t E_c.  (4.8)

*Proof.* Split n_t = ∫_{−∞}^ζ g_t + ∫_ζ^0 g_t e^{β(ζ−ε)}. The first term is N_t e^{ζ/E_c}. In the second, the exponent is ε(1/E_c − 1/k_BT) = −bε with b = β − E_c^{−1} > 0, so the integral equals e^{βζ}(e^{−bζ} − 1)/b ≍ e^{ζ/E_c}/b. Summing, n_t ≍ N_t e^{ζ/E_c}(1 + 1/(bE_c)) = N_t e^{ζ/E_c}/(1−α) since bE_c = (1−α)/α. Inverting, ζ = E_c ln[(1−α)n_t/N_t], so ζ′ = E_c/n_t and p_t = ∫ s ζ′ ds = n_t E_c. ∎

**Proposition 4.11 (Trap-limited mobility power law).** With free-carrier density n_f = N_c e^{βζ} and band mobility μ₀, in the trap-dominated regime n_t ≫ n_f,

  μ_eff = μ₀ n_f/(n_f + n_t) ≍ μ₀ (1−α)(N_c/N_t)^{?} · n_t^{(1−α)/α} ∝ n^{(1−α)/α}.  (4.9)

*Proof.* Substitute e^{ζ/E_c} = (1−α)n_t/N_t into n_f = N_c e^{βζ} = N_c[(1−α)n_t/N_t]^{βE_c} and use βE_c = 1/α. Then μ_eff ≍ μ₀ n_f/n_t ∝ n_t^{1/α − 1}. ∎

This reproduces the Vissenberg–Matters variable-range-hopping field-effect mobility exponent (T₀/T − 1) [6] and the measured density dependence unifying FET and diode transport [19] — here as a two-line corollary of the filling law rather than as a percolation computation. For E_c = 100 meV at 300 K, (1−α)/α = 2.87, in the observed range 1–3.

### 4.6 The disorder exponent: scaling law, bound, and closure constant

**Claim 4.12 (Critical-path scaling; asymptotic, under stated closure).** In the dilute limit n a³ → 0 with σ̂ → ∞ and aN^{1/3} fixed, the homogenized mobility satisfies

  ln μ = −c σ̂² + O(σ̂ ln σ̂),  (4.10)

with c > 0 a pure number determined by a dimensionless percolation optimization.

*Closure and argument.* By Ambegaokar–Halperin–Langer [2], ln σ_eff ≍ −ξ_c where ξ_c is the smallest ξ for which the subnetwork {2r_ij/a + β·(activation) ≤ ξ} percolates. By Lemma 4.9 the occupied population sits at ε_∞ = −σ̂σ; transport requires promotion to a transport level ε_t, at cost β(ε_t − ε_∞) = σ̂² + βε_t. If the percolation optimization returns ε_t = −c′σ̂σ with c′ a pure number (as it does when the only energy scale is σ and the only dimensionless spatial parameter is aN^{1/3}, whose logarithm enters subleadingly), then ln μ = −(1 − c′)σ̂² + subleading, i.e. (4.10) with c = 1 − c′. The canonical value is c = 4/9, equivalently μ ∝ exp[−(2σ/3k_BT)²], established by Monte Carlo simulation of the Gaussian disorder model [3] and reproduced by transport-energy analyses [20]. ∎ (closure)

We do **not** claim 4/9 as a theorem. We do prove a bound.

**Proposition 4.13 (Sharp-edge bound: c ≤ 1/2).** Let μ_sharp be the mobility of the truncated model in which all sites with ε < 0 are deleted from the network (an idealized mobility edge at the DOS centroid). Then μ ≥ μ_sharp, and in the nondegenerate dilute limit

  ln μ_sharp = −½σ̂² + O(ln σ̂).  (4.11)

Consequently c ≤ 1/2 in (4.10).

*Proof.* Deleting sites sets their incident conductances to zero; by Rayleigh monotonicity (Theorem 4.3) the effective conductance cannot increase, so μ ≥ μ_sharp. For the truncated model, the mobile fraction is the Boltzmann weight above the edge: n_f/n_tot = [∫₀^∞ g e^{−βε}]/[∫_{−∞}^∞ g e^{−βε}] = Θ(1)·e^{−σ̂²/2} by Lemma 4.9's completion of the square, since the numerator is O(N) while the denominator is N e^{σ̂²/2}. The residual spatial percolation factor among the retained half of the sites contributes exp[O(ln σ̂)] because the retained concentration is N/2, independent of σ̂. Multiplying by the band mobility gives (4.11). Combining with (4.10) yields c ≤ 1/2. ∎

The inequality has a clean physical reading: *variable-range hopping below any putative mobility edge can only add channels, so a sharp-edge model always underestimates μ.* The canonical 4/9 ≈ 0.444 < 0.5 is consistent, and the gap 1/2 − 4/9 = 1/18 quantifies the percolative enhancement.

### 4.7 Field dependence: an obstruction theorem

**Theorem 4.14 (Parity and smoothness).** Assume H1 with a disorder law invariant under spatial inversion, and let μ^{ij}(F) be defined by J^i = q n μ^{ij}(F) F_j in the homogenized steady state. Then:

1. μ^{ij}(F) = μ^{ij}(−F) exactly. In particular the leading field correction is O(|F|²).
2. If the site-energy density g is C^∞ (e.g. Gaussian) or the rates are Marcus (4.2), then F ↦ μ^{ij}(F) is C^∞ (resp. real-analytic) in a neighbourhood of F = 0.
3. Consequently the Poole–Frenkel form μ ∝ exp(γ√|F|) is **inadmissible as an F → 0 asymptote**. It can only be an intermediate-range interpolant.

*Proof.* (1) Let T be the inversion x ↦ −x. By H1 the disorder law is T-invariant. The rate matrix at field −F is the T-image of the transpose-conjugate of the rate matrix at F; the stationary measure maps accordingly, and the mean drift reverses: J(−F) = −J(F). Dividing by −F gives μ(−F) = μ(F).

(2) For Marcus rates the dependence on F is through exp[−(Δ + qF·r)²/(4λ_rk_BT)], entire in F; uniform integrability from |J(r)| ≤ J₀e^{−r/a} and the Gaussian energy tail permits differentiation under the ensemble average. For Miller–Abrahams the single-bond rate is only Lipschitz in F, but the ensemble average smooths it: writing δ = qF·r and h(δ) = ∫g(Δ)min{1, e^{−β(Δ+δ)}}dΔ = ∫_{−δ}^∞ g(Δ)e^{−β(Δ+δ)}dΔ + ∫_{−∞}^{−δ} g(Δ)dΔ, we find h′(δ) = −β∫_{−δ}^∞ g(Δ)e^{−β(Δ+δ)}dΔ (the boundary terms g(−δ) cancel identically), and each further differentiation produces one more boundary term proportional to a derivative of g at −δ. Smoothness of g therefore transfers to h, and hence to μ after the (uniformly convergent) spatial sum.

(3) exp(γ√|F|) has unbounded second derivative as F → 0 for γ ≠ 0, contradicting (2); and it is not even in the required analytic sense. ∎

**Corollary 4.15.** The universally observed ln μ ∝ √F over one to two decades in organic films is a *crossover*, not an asymptotic law. Any physically admissible closed form must be even and smooth at the origin; the standard interpolant

  μ(F) = μ(0) exp[ 𝒜(σ̂) ( √(1 + ℬ (qFa/σ)²) − 1 ) ]  (4.12)

satisfies both requirements and reduces to O(F²) at small field, as it must. The "effective temperature" T_eff(F) defined by D/μ ≡ k_BT_eff/q is a *one-number summary* of a nonequilibrium steady state, not a temperature: it need not reproduce higher cumulants (§10.3).

---

## 5. Trap Kinetics and Fractional Transport

### 5.1 The multiple-trap-and-release integral equation

Let free carriers with band mobility μ₀ be exchanged with a trap population of depth distribution ρ(E), E ≥ 0 measured from the transport edge, with release time τ(E) = τ₀e^{βE} and capture rate ω_c. Quasi-stationary occupancy gives the free fraction

  φ_f = [1 + ∫ρ(E) ω_c τ(E) dE]^{−1},  μ_eff = μ₀ φ_f,  (5.1)

whenever the integral converges. For ρ(E) = E_c^{−1}e^{−E/E_c} and E_c > k_BT the integral **diverges**: ∫e^{E(β − 1/E_c)}dE = ∞. This divergence is not a pathology of the model; it is the mathematical signature of dispersion.

**Proposition 5.1.** When E_c > k_BT, no finite mean release time exists, (5.1) is inadmissible, and the transport equation is non-Markovian in time.

*Proof.* Divergence as computed. The mean waiting time of the associated continuous-time random walk is infinite, so no diffusion limit with a local time derivative exists; the correct limit is a subordinated process [9,10]. ∎

### 5.2 The fractional transport theorem

**Theorem 5.2 (Fractional drift–diffusion).** Let trap depths be distributed as ρ(E) = E_c^{−1}e^{−E/E_c}, E ≥ 0, with Arrhenius release τ = τ₀e^{βE}, and let α = k_BT/E_c ∈ (0,1). Let 𝓛 be the drift–diffusion generator

  𝓛 n = ∂_i(D^{ij}∂_j n − s μ^{ij} n E_j).  (5.2)

Then the coarse-grained carrier density obeys

  ∂_t n = ₀D_t^{1−α} 𝓛 n,  ₀D_t^{1−α} h = (1/Γ(α)) ∂_t ∫₀^t (t−s)^{α−1} h(s) ds,  (5.3)

with D^{ij}, μ^{ij} the *trap-free* coefficients. Moreover the ratio D^{ij}/μ^{ij} is unchanged by the subordination: the generalized Einstein relation (2.5) is invariant.

*Proof.* Survival probability of a trapped carrier:

  P(τ > t) = P(E > k_BT ln(t/τ₀)) = exp[−(k_BT/E_c) ln(t/τ₀)] = (τ₀/t)^α,

so ψ(t) = α τ₀^α t^{−1−α} for t ≫ τ₀. By the standard Tauberian theorem, ψ̃(s) = 1 − Γ(1−α)(τ₀s)^α + o(s^α) as s → 0. In the Montroll–Weiss formulation the memory kernel of the generalized master equation is K̃(s) = sψ̃(s)/(1−ψ̃(s)) → s^{1−α}/[Γ(1−α)τ₀^α]. Absorbing τ₀^α into the definition of 𝓛 (i.e. measuring time in units of τ₀) and recognizing s^{1−α} as the Laplace symbol of ₀D_t^{1−α} gives (5.3); the spatial operator is untouched because trapping is local in space. Invariance of D/μ holds because subordination rescales the operational time of the *same* spatial process, multiplying D^{ij} and μ^{ij} by an identical factor; their ratio, being a property of the jump kernel's asymmetry, is preserved. Full computation in Appendix B. ∎

**Corollary 5.3 (Time-of-flight signature).** The transient current in a time-of-flight configuration obeys I(t) ∝ t^{−(1−α)} for t < t_T and t^{−(1+α)} for t > t_T, with the two exponents summing to −2 — the Scher–Montroll universality [9]. Measuring both slopes overdetermines α and constitutes a consistency test rarely applied.

**Corollary 5.4 (Mobility power law recovered).** The tail of ψ encodes the same α as the filling law (4.8), hence the mobility exponent (1−α)/α of Proposition 4.11. Dispersive kinetics and density-dependent mobility are *the same parameter viewed twice*.

**Remark 5.5.** Equation (5.3) is not a modelling flourish. It is the unique scaling limit of the stated microscopic trap kinetics, and it predicts memory effects — dependence of the transfer curve on sweep rate and history — with a *power-law*, not exponential, kernel. This is the correct origin of hysteresis in trap-rich OFETs, distinct from ionic hysteresis in OECTs (§8.5).

---

## 6. The Device Equation as an Asymptotic Reduction

### 6.1 Scaling

Introduce the small parameters

  ε₁ = d/L (aspect ratio), ε₂ = λ_D/L (screening), ε₃ = a_c/ℓ (microstructure),  (6.1)

with λ_D² = ε/(q²∂n/∂ζ) the local Debye length. Rescale x¹ = L X, x³ = d Z, φ = (k_BT/q)Φ, n = n₀ ñ. The system (2.7) becomes, at leading order in ε₁, a one-dimensional problem in X with a *slaved* transverse profile — the profile computed exactly in §3.

### 6.2 The gradual-channel theorem

**Hypothesis H3 (Local equilibrium closure).** Within each transverse slice, the carrier distribution is the equilibrium distribution of §3 evaluated at the local quasi-Fermi level ζ(X); the constitutive law μ^{ij}(n, F) of §4 applies pointwise with the local n and the local *lateral* field.

**Theorem 6.1 (Gradual-channel reduction).** Assume H1–H3, ε₁ ≪ 1, and L ≫ λ with λ the scale length of Proposition 6.5. Define the sheet density N_s(X) and sheet conductance

  σ_s(X) = q ∫₀^d μ_t(n(z,X)) n(z,X) dz.  (6.2)

Then at leading order the transverse problem is solved by Theorem 3.4, the solvability condition of the O(ε₁) problem is current continuity ∂_X(W σ_s ∂_X V) = 0, and the drain current admits the exact quadrature

  I_D = (W/L) ∫₀^{V_D^ch} σ_s(V) dV,  (6.3)

where V(x¹) is the local channel potential relative to the source and V_D^ch is the *intrinsic* channel bias. The relative error in (6.3) is O(ε₁) + O(e^{−L/λ}) + O(λ/L).

*Proof.* Expand Φ = Φ₀(Z; X) + ε₁Φ₁ + …, ñ = ñ₀ + ε₁ñ₁. At O(1) the transverse equation is exactly the equilibrium problem of §3 with ζ parametrized by X, solved by Theorem 3.4 and the quadrature (3.5). At O(ε₁) the equation for Φ₁ is a linear elliptic problem in Z whose right-hand side involves ∂_X of the leading-order flux; the transverse operator has a one-dimensional cokernel (the constant, by the Neumann/Dirichlet structure), and the Fredholm solvability condition is precisely the vanishing of the transverse-integrated divergence of the lateral flux, i.e. ∂_X(Wσ_s∂_XV) = 0. Integrating once in X and using I_D = −Wσ_s∂_XV constant gives (6.3) after changing variables from X to V. The error terms arise respectively from the neglected O(ε₁) flux, from source/drain boundary layers whose penetration depth is λ (Proposition 6.5), and from the pinch-off region of length O(λ) (§7.4). ∎

**Corollary 6.2 (Charge-sheet form).** With all induced charge mobile, qN_s = C_i(A − V), and

  σ_s(V) = μ(N_s) C_i (A − V) ≡ σ̃(A − V).  (6.4)

Defining the **sheet-conductance potential**

  G(w) ≡ ∫₀^w σ̃(u) du,  G(0) = 0, G′ = σ̃,  (6.5)

equation (6.3) becomes the compact, fully nonlinear device equation

  (L/W) I_D = G(A) − G(A − V_D^ch).  (6.6)

For μ constant, G(w) = ½μC_iw², recovering I_D = (W/L)μC_i(AV_D − V_D²/2) and I_D,sat = (W/2L)μC_iA². For μ ∝ n^γ, σ̃(u) = k u^{1+γ} and

  I_D = (W/L) k [A^{2+γ} − (A − V_D^ch)^{2+γ}]/(2+γ).  (6.7)

Equation (6.6) is the object on which the entire inverse theory of §7 is built. Its virtue is that *all* of the material physics is compressed into the single scalar function G, and all of the contact physics into the single scalar relation V_D^ch = V_D − I_DR_c.

### 6.3 Where the reduction fails: the scale length

**Proposition 6.3 (Exact scale length).** Consider the two-dimensional Laplace problem in film (0 < z < t_s, permittivity ε_s) and dielectric (−t_i < z < 0, permittivity ε_i), with the gate an AC ground at z = −t_i and a Neumann condition at z = t_s. Lateral penetration modes φ ∝ e^{−x/λ} obey the exact transcendental dispersion relation

  ε_s tan(k t_s) = ε_i coth(k t_i),  λ = 1/k.  (6.8)

In the thin-body/thin-oxide limit k t_s, k t_i ≪ 1,

  λ = √(ε_s t_s t_i / ε_i).  (6.9)

*Proof.* Separation gives φ_s = e^{−x/λ}(A sin kz + B cos kz) with k = 1/λ, and φ_i = e^{−x/λ}C sinh(k(z+t_i)). Continuity of φ at z = 0 gives B = C sinh(kt_i); continuity of ε∂_zφ gives ε_sA = ε_iC cosh(kt_i); the Neumann condition at t_s gives A = B tan(kt_s). Eliminating A, B, C yields (6.8). Expanding tan and coth gives k² = ε_i/(ε_st_st_i). ∎

**Corollary 6.4.** For ε_s = 3.5ε₀, ε_i = 3ε₀, t_s = 30 nm, t_i = 300 nm: λ = 102 nm. Threshold shift and drain-induced barrier lowering scale as e^{−L/λ}; at L = 1 µm this is 4×10⁻⁵ (negligible), at L = 200 nm it is 0.14 (severe). **Organic short-channel behaviour is controlled by the dielectric thickness, not the semiconductor thickness alone**, and the frequent substitution t_s → ℓ in (6.9) is incorrect: the film is undoped, so source field lines traverse the whole body.

### 6.4 Contacts: the transmission-line theorem

Under the source/drain metallization, current transfers from the metal into the sheet over a finite length. Let ρ_c (Ω m²) be the specific contact resistivity, defined by the normal current density j_z = V/ρ_c with V the local sheet-to-metal potential difference, and let σ_s be the sheet conductance under the contact.

**Theorem 6.5 (Transmission line).** With contact length L_c, the lateral current per unit width i(x) and potential V(x) satisfy

  di/dx = V/ρ_c,  i = −σ_s dV/dx ⟹ d²V/dx² = V/L_T², L_T ≡ √(ρ_c σ_s).  (6.10)

With i(L_c) = 0 (open far end) and V(0) = V₀,

  V(x) = V₀ cosh((L_c − x)/L_T)/cosh(L_c/L_T),
  R_c W = √(ρ_c/σ_s) · coth(L_c/L_T).  (6.11)

In particular R_cW → √(ρ_c/σ_s) = σ_s^{−1}L_T for L_c ≫ L_T.

*Proof.* Charge continuity in the sheet with distributed injection gives the first equation; the lateral Ohm law the second; eliminating i gives the modified Helmholtz equation. The solution with the stated boundary conditions is (6.11)₁; then i(0) = −σ_sV′(0) = (σ_sV₀/L_T)tanh(L_c/L_T) and R_cW = V₀/i(0) gives (6.11)₂. ∎

**Corollary 6.6 (Derived gate dependence of contact resistance).** With σ_s = μC_iA and ρ_c gate-independent,

  R_cW = √(ρ_c/(μC_iA)) ∝ A^{−1/2},  L_T = √(ρ_c μC_iA) ∝ A^{1/2}.  (6.12)

Contact resistance *decreases* as the inverse square root of overdrive, while the current-crowding length *grows* as its square root. Both are testable and both are routinely ignored.

**Numbers.** ρ_c = 10⁻⁷ Ω m² (10⁻³ Ω cm²), μ = 1 cm² V⁻¹s⁻¹, C_i = 8.85 nF cm⁻², A = 10 V: σ_s = 8.85×10⁻⁸ S (R_s = 11.3 MΩ/sq), L_T = 94 nm, R_cW = 1.06 Ω m = 106 Ω cm. These are the observed magnitudes. Note L_T ≈ 100 nm is comparable to L in aggressively scaled devices, in which case the contact and channel problems do not decouple and Theorem 6.1's error term is not small.

**Proposition 6.7 (Barrier lowering and the injection crossover).** For a Schottky barrier with image-force lowering, the barrier reduction is ΔΦ = √(qE_m/(4πε_s)) (volts), obtained by maximizing U(x) = −q²/(16πε_sx) − qEx at x_m = √(q/(16πε_sE_m)). At E_m = 10⁸ V m⁻¹ and ε_s = 3.5ε₀, ΔΦ = 0.20 V — comparable to typical injection barriers. Hence ρ_c is itself gate- and drain-dependent, ρ_c ∝ exp[β q(Φ_B − ΔΦ)], and (6.12) is a *lower bound* on the steepness of R_c(A). The device is injection-limited when R_c ≫ R_ch and bulk-limited otherwise; the crossover overdrive A_* solves √(ρ_c/(μC_iA_*)) = L/(WμC_iA_*), i.e.

  A_* = L²/(W²ρ_c μ C_i).  (6.13)

*Proof.* The image-force computation is the elementary maximization stated (both terms of U are equal at x_m, so ΔU = −2qE_mx_m). The crossover follows by equating R_cW from (6.11) with R_chW = L/σ_s and solving. ∎

### 6.5 Composite model

Collecting Theorem 6.1, Corollary 6.2, and Theorem 6.5, the uniformly valid leading-order device model is the implicit scalar equation

  (L/W) I_D = G(A) − G(A − V_D + I_D R_c(I_D, V_G)),  R_cW = √(ρ_c/σ_s)coth(L_c/L_T).  (6.14)

Equation (6.14) is the master equation of the organic transistor. Everything in §7 concerns its inversion; everything in §8 concerns its volumetric generalization.

---

## 7. Identifiability: What Can and Cannot Be Extracted

### 7.1 The fibre theorem

Fix the geometry (W, L known) and consider the linear regime V_D → 0. Write Σ(A) for the *measured* normalized sheet conductance,

  Σ(A) ≡ lim_{V_D→0} (L/W) I_D/V_D,  r(A) ≡ W R_c(A)/L.  (7.1)

**Theorem 7.1 (Non-identifiability in the linear regime).** From (6.14),

  1/Σ(A) = 1/σ_s(A) + r(A).  (7.2)

Consequently the map (σ_s, r) ↦ Σ has fibres parameterized by *arbitrary* measurable r with 0 ≤ r(A) < 1/Σ(A): for each such r, σ_s ≡ (1/Σ − r)^{−1} is a positive sheet conductance reproducing the data exactly. The intrinsic mobility μ(n) = σ_s(A)/(C_iA) is therefore **not identifiable** from linear-regime transfer data, for any gate dependence of the contact, however smooth, however small.

*Proof.* In the linear regime (6.14) reduces to Ohm's law for the series combination R_ch + R_c with R_ch = L/(Wσ_s). Multiplying by W/L gives (7.2). The fibre description is immediate: (7.2) constrains only the sum of the two reciprocals. ∎

This is not a statement about noise. It is an exact structural degeneracy, and it is the mathematical content of the mobility-extraction crisis [21,22]. No fitting procedure, no reliability factor, and no amount of data on this branch can resolve it.

### 7.2 The saturation branch is contact-immune

**Theorem 7.2 (Identification on the saturation branch).** Assume: (i) Theorem 6.1 holds; (ii) σ̃(0) = 0 (vanishing sheet conductance at threshold); (iii) channel-length modulation is neglected; (iv) R_c is finite and depends only on terminal variables. Then for V_D ≥ V_D,sat the drain current saturates at

  (L/W) I_D,sat(A) = G(A),  (7.3)

*independently of R_c*. Consequently

  σ̃(A) = (L/W) dI_D,sat/dA,  μ(N_s = C_iA/q) = (L/W) (dI_D,sat/dA)/(C_i A),  (7.4)

and μ(n) is identified pointwise on the range of densities probed. Combining with (7.2), the contact law is then also identified:

  r(A) = 1/Σ(A) − 1/σ̃(A).  (7.5)

*Proof.* Pinch-off occurs when the intrinsic channel bias reaches A, i.e. V_D^ch = A, since σ̃(A − V_D^ch) → 0 there by (ii). At that point (6.6) gives (L/W)I_D = G(A) − G(0) = G(A). For larger V_D the excess drops across the pinch-off region and the contacts; by (iii) the effective channel length is unchanged, so I_D remains at G(A)W/L. The value depends only on G, i.e. only on the intrinsic constitutive law — contacts determine *where* saturation occurs, not *at what current*. Differentiating (7.3) in A gives (7.4) since G′ = σ̃ and G(0) = 0. Equation (7.5) is (7.2) rearranged. ∎

**Corollary 7.3 (Practical protocol).** Measure the full output family; identify the plateau current at each V_G; differentiate the plateau current with respect to V_G; divide by C_iA. This yields the intrinsic μ(n) *without any contact model*. Then use the linear branch to obtain R_c(V_G). The two branches are complementary, not redundant.

**Remark 7.4 (Hypotheses are load-bearing).** (ii) fails whenever a residual conductivity exists (Proposition 7.6). (iii) fails at O(λ/L): the pinch-off region has length O(λ), so the theorem holds to relative accuracy O(λ/L) — with λ = 102 nm and L = 1 µm, ~10%, which is *not* negligible and must be reported. (iv) fails if the contact barrier is modulated by the drain field through the semiconductor (a genuine 2D effect); this is bounded by the same e^{−L/λ} estimate.

### 7.3 A surviving one-parameter degeneracy

**Proposition 7.5 (Residual-conductivity degeneracy).** Let σ_s(A) = μC_iA + qκ with κ > 0 constant (a gate-independent residual sheet carrier density). Then σ̃(0) = qκ ≠ 0, pinch-off does not occur, the output characteristics do not saturate, and Theorem 7.2 is void. Moreover the pair (μ, κ) and a gate-only contact law r(A) ∝ A^{−2} generate, to first order in κ, identical linear-regime data to a pure μ model with a different contact.

*Proof.* Non-saturation is immediate since σ̃ never vanishes. For the degeneracy, perturb G(w) = ½μC_iw² by εψ(w) with ψ affine, ψ(w) = c₁w (ψ(0) = 0 forced by G(0) = 0). Then G′ = μC_iw + εc₁, i.e. σ̃ = μC_iA + εc₁, so qκ = εc₁. In the linear regime the induced change in 1/Σ is absorbed by r(A) = εc₁/(μC_iA)² · (const), a function of A alone. Explicitly, 1/Σ = 1/(μC_iA + qκ) + r; expanding to first order in κ and choosing r = qκ/(μC_iA)² leaves Σ unchanged. ∎

Thus even restricting the contact to depend on gate voltage alone does not restore identifiability: an additive residual conductivity is exactly exchangeable against a specific A^{−2} contact law. Uniqueness requires either the saturation branch (Theorem 7.2) or an independent contact measurement (four-probe, TLM), or a structural constraint such as "μ is a pure power law with no additive constant *and* κ = 0", which must be justified physically rather than assumed for convenience.

### 7.4 The double-slope artifact

The most frequently reported non-ideality is an apparent mobility that rises steeply near threshold and then rolls over, producing two slopes in √|I_D| versus V_G. We show this is generically a *kinematic artifact of the extraction*, not a material property.

**Theorem 7.6 (Fixed-V_D saturation crossing).** Let ρ_c be constant, μ constant, and let the saturation mobility be extracted at fixed V_D by the naive formula

  μ_ext(A) ≡ 2L I_D(A, V_D)/(W C_i A²).  (7.6)

Then the device saturates iff A(1 + (c/2)√A) ≤ V_D, where c ≡ √(ρ_cμC_i)/L. Hence there is a unique crossing overdrive A_c solving

  A_c(1 + (c/2)√A_c) = V_D,  (7.7)

such that μ_ext(A) = μ exactly for A ≤ A_c and μ_ext(A) < μ, strictly decreasing, for A > A_c. The apparent characteristic therefore exhibits a peak-and-rolloff ("kink", double slope) at A_c *even for a perfectly ideal, constant-mobility, trap-free semiconductor*.

*Proof.* From Corollary 6.2 with γ = 0, I_sat = (W/2L)μC_iA². From Corollary 6.6, R_cW = √(ρ_c/(μC_iA)), so

  I_sat R_c = (μC_iA²/(2L))√(ρ_c/(μC_iA)) = (c/2) A^{3/2}.

Saturation requires V_D ≥ A + I_satR_c = A(1 + (c/2)√A), a strictly increasing function of A; hence the stated threshold A_c exists and is unique. For A ≤ A_c the device is saturated and (7.6) returns μ identically. For A > A_c the device is in the linear regime, where I_D < I_sat(A), so μ_ext < μ; monotone decrease follows because I_D grows subquadratically in A while the denominator grows as A². ∎

**Corollary 7.7.** The artifact vanishes if extraction is performed on the true plateau (V_D ≫ V_D,sat) or if the full output family is used. Conversely, *any* report of a mobility kink obtained at a single fixed V_D without verifying saturation is uninformative about the material. Together with Theorem 7.1 this places a sharp burden of proof on the extraction protocol, and gives a precise mathematical formulation of the concerns raised in [21,22].

### 7.5 Regularized inversion

Theorem 7.2 reduces extraction to numerical differentiation, which is mildly ill-posed (degree one).

**Proposition 7.8 (Stability rate).** Let measured plateau data I_δ satisfy ‖I_δ − I‖_{L²} ≤ δ and let the true σ̃ obey ‖σ̃″‖_∞ ≤ M. Then a central-difference reconstruction with step h obeys

  ‖σ̃_h − σ̃‖_∞ ≤ M h²/6 + 2δ/h,  (7.8)

minimized at h = (6δ/M)^{1/3} with error O(M^{1/3}δ^{2/3}); with only ‖σ̃′‖_∞ ≤ M₁ and a one-sided difference, the optimal rate is O(√(M₁δ)) at h = 2√(δ/M₁). Tikhonov regularization with the H¹ penalty and Morozov discrepancy choice achieves the same order while enforcing σ̃ ≥ 0 and σ̃′ ≥ 0 (physical monotonicity).

*Proof.* Taylor's theorem with remainder gives the truncation term; the noise term follows from the triangle inequality on the difference quotient. Optimization in h is elementary calculus. The constrained Tikhonov statement follows from standard regularization theory for mildly ill-posed linear problems with convex constraints. ∎

**Remark 7.9.** Monotonicity σ̃′ ≥ 0 is *not* universally valid: in OECTs, dedoping reduces Coulomb scattering from fixed anionic sites, so μ can *increase* as p decreases (§10.1). The constraint must be imposed only where physically justified.

---

## 8. The Volumetric Branch: Organic Electrochemical Transistors

### 8.1 The coupled system

In an OECT the film is permeable to ions (ΔG_± finite in (2.6)). Specialize to a p-type depletion-mode mixed conductor: fixed anionic acceptor density N_A, mobile holes p, mobile injected cations c. Electroneutrality in the bulk (Π ≫ 1, screening length ≪ d) gives

  p(x) + c(x) = N_A.  (8.1)

The gate injects cations; each injected cation compensates one acceptor and removes one hole. This is *chemical* switching, not electrostatic induction.

The local cation population is set by the local electrochemical driving force. With C* = q²∂p/∂ζ the volumetric capacitance and V_p ≡ qN_A/C* the full-dedoping ("pinch-off") voltage, local equilibrium with the electrolyte at potential V_G gives

  c(x) = (C*/q)(V_G − V(x)),  p(x) = N_A − (C*/q)(V_G − V(x)),  (8.2)

and hence the local bulk conductivity

  σ(x) = qμ p(x) = μ C* (V_p − V_G + V(x)).  (8.3)

### 8.2 Reduction to the Bernards–Malliaras form

**Theorem 8.1.** Under (8.1)–(8.3), constant μ, uniform film thickness d, and the gradual-channel approximation applied to the *bulk* conductance, the drain current is

  I_D = (Wd/L) μC* [(V_p − V_G)V_D + V_D²/2],  (8.4)

with saturation at V_D,sat = V_G − V_p and

  |I_D,sat| = (Wd/2L) μC* (V_p − V_G)²,  g_m = (Wd/L) μC* (V_p − V_G).  (8.5)

*Proof.* The bulk analogue of (6.3) is I_D = (Wd/L)∫₀^{V_D}σ(V)dV; substitute (8.3) and integrate. Pinch-off occurs where σ vanishes, i.e. V = V_G − V_p, giving V_D,sat; substituting into (8.4) gives (8.5)₁ since (V_p − V_G)(V_G − V_p) + (V_G − V_p)²/2 = −(V_p − V_G)²/2. Differentiation in V_G gives (8.5)₂. ∎

Equations (8.5) are the Bernards–Malliaras model [11] — here *derived* as the leading-order term of the mixed-conductor gradient flow under explicit hypotheses, rather than posited. The figure of merit μC* (units F cm⁻¹ V⁻¹ s⁻¹) emerges as the sole material combination entering the transconductance, which is why it is the correct benchmarking quantity [23].

**Corollary 8.2 (The volumetric advantage).** g_m^OECT/g_m^OFET = (C*d/C_i)·(V_p − V_G)/A = Π·(V_p−V_G)/A. With Π ≈ 4×10⁴ (§2.4), OECT transconductance exceeds OFET transconductance at equal geometry and bias by four orders of magnitude. This is not a mobility advantage; it is a *capacitance-density* advantage, purchased with gate charge.

### 8.3 Two clocks and the gain–bandwidth invariance

**Lemma 8.3 (Electronic clock).** The electronic transit time is τ_e = L²/(μ|V_D|) up to an O(1) factor (Theorem 9.1).

**Lemma 8.4 (Ionic clock).** The gate must deliver charge Q_G = C*·(WdL)·δV to change the channel state by δV. If the ionic path is dominated by electrolyte of resistivity ρ_e and thickness ℓ_e over the channel area WL, then R_ion = ρ_eℓ_e/(WL) and

  τ_i = R_ion C_G = ρ_e ℓ_e C* d,  (8.6)

*independent of L and W*, and linear in d.

*Proof.* Q_G = C*·volume·δV; R_ion is the electrolyte resistance of a slab of area WL and thickness ℓ_e; the product is (8.6). ∎

**Theorem 8.5 (Gain–bandwidth invariance).** In the ion-limited regime τ_i ≫ τ_e, the small-signal bandwidth is f_c = 1/(2πτ_i) and

  g_m · f_c = W μ (V_p − V_G) / (2π L ρ_e ℓ_e),  (8.7)

which is **independent of the film thickness d and of the volumetric capacitance C***.

*Proof.* Multiply (8.5)₂ by 1/(2πτ_i) with (8.6): the factors d and C* cancel identically. ∎

**Corollary 8.6 (Design consequences).** Thickness and volumetric capacitance trade gain against bandwidth at *fixed product*. They are not routes to simultaneous improvement. The only levers that improve both are: increasing μ, increasing W/L, and decreasing the electrolyte resistivity–thickness product ρ_eℓ_e. In particular, the widespread practice of reporting large g_m from thick films without reporting bandwidth is a measurement of Π, not of material quality.

**Numbers.** μ = 1 cm²V⁻¹s⁻¹, C* = 100 F cm⁻³ = 10⁸ F m⁻³, ρ_e = 1 Ω m (0.1 M), ℓ_e = 100 µm, d = 100 nm: τ_i = 1×10⁻⁴×10⁸×10⁻⁷ = 10⁻³ s, f_c ≈ 160 Hz. With ℓ_e = 10 µm and d = 20 nm: τ_i = 20 µs, f_c ≈ 8 kHz. The crossover thickness d* = τ_e/(ρ_eℓ_eC*) is ~0.2 nm for L = 10 µm — i.e. **OECTs are essentially always ion-limited**, and the electronic transit time is irrelevant to their bandwidth. This is a sharp, falsifiable structural statement.

### 8.4 Dedoping as a moving front

When the gate step is large, (8.2) fails locally and the film separates into dedoped and doped regions divided by a front at x = s(t). In the dedoped region σ ≈ 0; in the doped region σ = qμN_A. Ion transport to the front is diffusion-limited with diffusivity D_i; the front condition is a Stefan-type balance

  q N_A ṡ = −q D_i ∂_x c |_{x=s⁻} ⟹ ṡ = −(D_i/N_A) ∂_x c|_{s⁻}.  (8.8)

**Proposition 8.7.** With a fixed surface cation concentration c₀ at the electrolyte interface and a semi-infinite film, (8.8) admits the similarity solution s(t) = 2Λ√(D_i t) with Λ determined by the transcendental relation Λ e^{Λ²} erfc(Λ) = (c₀/N_A)/√π · … (the standard one-phase Stefan closure). In particular s ∝ √t, so the dedoping time for a film of thickness d scales as d²/D_i, *quadratically*, whereas the small-signal charging time (8.6) scales linearly.

*Proof.* Standard one-phase Stefan similarity reduction; the substitution η = x/(2√(D_it)) reduces the diffusion equation to an ODE with the error-function solution, and the front condition fixes Λ. ∎

**Corollary 8.8.** Large-signal switching and small-signal bandwidth in OECTs are governed by *different scaling laws in d*. Reporting one and inferring the other is invalid. This resolves an apparent inconsistency in the literature between d-linear and d-quadratic switching claims: they are different regimes, not contradictory measurements.

### 8.5 Hysteresis, retention, and synaptic linearity

With the gate open-circuited, (2.7) with (2.6) is a genuine gradient flow: ℱ decreases monotonically, 𝔇 ≥ 0, and the state relaxes toward the minimizer of ℱ subject to conserved total ion number. Retention loss is therefore *thermodynamically inevitable* unless a barrier in ΔG_± or an ionic blocking layer arrests the flow — a Lyapunov statement, not an engineering accident.

**Proposition 8.9 (Weight-update linearity).** If an OECT is used as an analog synaptic element with state variable c (equivalently Q_G), then the conductance update per unit injected charge is

  dσ/dc = −q μ(p) + q (dμ/dp)(dp/dc) p = −q[μ(p) + p μ′(p)] (using dp/dc = −1).  (8.9)

Hence updates are linear in charge **iff μ is independent of p**, and the fractional nonlinearity is |1 + pμ′/μ|. Coulomb-scattering-limited transport in heavily doped films gives μ′ > 0 (dedoping improves mobility), producing *compressive* nonlinearity of one sign; trap-filling gives μ′ < 0 in the p-variable, of the other sign.

*Proof.* Differentiate σ = qμ(p)p with p = N_A − c. ∎

This gives a materials-level design criterion for neuromorphic OECTs that is independent of circuit compensation: engineer dμ/dp ≈ 0, i.e. operate at the mobility maximum.

---

## 9. Universal Bounds and Figures of Merit

### 9.1 The exact charge-control identities

**Theorem 9.1 (Transit-time identity).** Under Theorem 6.1, with Q ≡ W∫₀^L qN_s(x)dx the total mobile channel charge and v(x) the local drift velocity,

  τ ≡ ∫₀^L dx/v(x) = Q/I_D  (9.1)

exactly, for any μ(n), any statistics, any disorder.

*Proof.* Current continuity gives I_D = W qN_s(x)v(x), so 1/v = WqN_s/I_D; integrate over x. ∎

**Theorem 9.2 (Universal gain–delay identity).** Let f_T ≡ g_m/(2πC_gg) with C_gg ≡ ∂Q/∂V_G the intrinsic gate capacitance and g_m ≡ ∂I_D/∂V_G. Then

  f_T · τ = (1/2π) ∂ln I_D/∂ln Q.  (9.2)

*Proof.* f_Tτ = [g_m/(2πC_gg)]·[Q/I_D] = (1/2π)(∂I_D/∂Q)(Q/I_D) = (1/2π)∂ln I_D/∂ln Q. ∎

This identity is model-independent within the quasi-static gradual-channel regime and replaces the loose folklore "f_T ≈ 1/(2πτ)" with an exact statement whose correction factor is a logarithmic derivative.

**Corollary 9.3 (Power-law family, exact).** For μ ∝ n^γ (σ̃ = k u^{1+γ}) in saturation:

  I_D = (W/L)kA^{2+γ}/(2+γ),  Q = WLC_iA(2+γ)/(3+γ),  τ = L²(2+γ)²/[(3+γ)μ(A)A],
  f_T = μ(A)A(3+γ)/[2πL²(2+γ)],  f_T·τ = (2+γ)/(2π).  (9.3)

*Proof.* Direct integration of (6.6) and (9.1) with dx = (Wσ̃/I_D)dV; the algebra is given in Appendix C. The last equality agrees with (9.2) since I_D ∝ A^{2+γ} and Q ∝ A. ∎

For γ = 0 this gives f_T = 3μA/(4πL²) and f_Tτ = 1/π — a factor of **two** larger than the naive 1/(2πτ). For velocity-saturated transport (I_D ∝ Q) one recovers f_T = 1/(2πτ) = v_sat/(2πL). The factor is not a convention; it is ∂ln I/∂ln Q, and it must be stated.

### 9.2 The attempt-frequency ceiling

**Proposition 9.4 (Kinetic ceiling).** In a hopping system the drift velocity is bounded by v ≤ a ν₀ ≡ v_max, since a hop of length ≤ a occurs at rate ≤ ν₀. Hence

  f_T ≤ (2+γ) v_max/(2πL).  (9.4)

With a = 1 nm and ν₀ = 10¹³ s⁻¹, v_max = 10⁴ m s⁻¹, giving f_T ≤ 16 GHz at L = 100 nm (γ = 0) and ≤ 1.6 GHz at L = 1 µm.

*Proof.* The bound on v is immediate from the rate structure. Combine with (9.3) and μ(A)A/L ≤ v_max. ∎

This is a hard ceiling independent of materials optimization: **organic transistors cannot reach silicon RF performance at equal geometry**, because v_max is set by the attempt frequency and localization length, both of which are molecular constants. The route to bandwidth is scaling L, not improving μ — and scaling L is limited by λ (Proposition 6.3), which is limited by t_i, which is limited by tunnelling and by Π. The theory closes on itself.

### 9.3 Intrinsic gain

**Proposition 9.5.** The intrinsic gain is g_m/g_d with g_d = ∂I_D/∂V_D. Under channel-length modulation with pinch-off length ΔL ≃ λ, g_d/I_D ≃ λ/(L − ΔL), so

  g_m/g_d ≃ (2+γ)(L/λ − 1).  (9.5)

*Proof.* g_m/I_D = (2+γ)/A from (9.3); g_d/I_D from I_D ∝ 1/(L − ΔL) with ΔL ≃ λ. ∎

With λ = 102 nm, L = 1 µm, γ = 0: gain ≈ 18. Organic analog gain is limited by the *same* scale length that limits short-channel immunity.

### 9.4 Noise, and the dispersion–noise duality

**Theorem 9.6 (McWhorter spectrum from the exponential tail).** Let traps have depths E ≥ 0 with density ρ(E) = E_c^{−1}e^{−E/E_c} and release times τ = τ₀e^{βE}. Then the density of time constants is

  ρ_τ(τ) = α τ₀^α τ^{−1−α},  α = k_BT/E_c,  (9.6)

and the superposition of Lorentzians gives, for 0 < α < 1,

  S_I(f) ∝ ∫₀^∞ ρ_τ(τ) 4τ/(1 + (2πfτ)²) dτ = C(α) f^{−(1−α)},  C(α) = 4α τ₀^α ∫₀^∞ u^{−α}/(1+u²)du.  (9.7)

*Proof.* Change variables: dE/dτ = k_BT/τ, so ρ_τ = ρ(E)·k_BT/τ = (k_BT/E_c)(τ₀/τ)^α/τ = ατ₀^ατ^{−1−α}. Substituting into the Lorentzian superposition and setting u = 2πfτ gives the stated power of f; the u-integral converges at 0 because α < 1 and at ∞ because the integrand is u^{−α−2}. ∎

**Corollary 9.7 (Dispersion–noise duality).** The fractional transport order α of Theorem 5.2 and the drain-current noise exponent β defined by S_I ∝ f^{−β} satisfy

  **α + β = 1.**  (9.8)

Both are determined by the *single* microscopic parameter E_c. Limits: α → 1 (E_c ≪ k_BT, no dispersion) gives β → 0, white noise; α → 0 (deep tails, strong dispersion) gives β → 1, ideal 1/f.

Equation (9.8) is an experimentally stringent consistency test: measure the time-of-flight dispersion exponent and the noise exponent on the same film; their sum must be unity. To our knowledge this test has not been systematically applied to organic transistors, although the underlying connection between trapping statistics and 1/f noise is long established [24,25]. Its violation would falsify the exponential-tail hypothesis, and its confirmation would fix E_c twice over.

**Corollary 9.8 (Input-referred noise).** S_I/I_D² = (g_m/I_D)² S_{V_th}, so the input-referred gate-voltage noise is S_{V_th} = S_I/(g_m²). At fixed bias current, maximizing g_m/I_D minimizes input-referred noise; from (9.3), g_m/I_D = (2+γ)/A, so *low overdrive* is optimal — the same conclusion as in silicon, but with γ from the disorder, not the band.

### 9.5 Subthreshold swing: exact bound and trap renormalization

**Proposition 9.9.** In subthreshold, I_D ∝ n_f ∝ e^{βζ} and the gate couples through the capacitive divider dζ/dV_G = q/(1 + C_t/C_i) with C_t = q²∂n_t/∂ζ the trap capacitance. Hence

  S ≡ dV_G/d(log₁₀I_D) = (k_BT/q) ln10 · (1 + C_t/C_i) ≥ 59.6 mV/dec at 300 K.  (9.9)

For the exponential tail, C_t = q²n_t/E_c = q n_t α/(k_BT) by (4.8).

*Proof.* Logarithmic differentiation of I_D ∝ e^{βζ} and the series-capacitance divider. The bound follows from C_t ≥ 0. ∎

**Remark 9.10 (A correction to folklore).** It is often asserted that the subthreshold swing of an organic transistor is "set by E_c", i.e. S ≈ (E_c/q)ln10. Equation (9.9) shows this holds *only* if 1 + C_t/C_i = E_c/k_BT, i.e. C_t/C_i = (1−α)/α — a specific, non-generic capacitance ratio. Since C_t ∝ n_t varies with gate bias, a constant swing over decades is itself evidence *against* a simple exponential-tail picture and demands explanation. We flag this as an unresolved tension (§10.5).

### 9.6 Sensing limits

**Proposition 9.11 (Nernstian ceiling and volumetric amplification).** For an ion- or analyte-sensitive gate in which the transduction is a shift of the interfacial chemical potential, δζ = (k_BT/z)ln(a/a₀) for activity a and charge number z, giving δV_th = δζ/q and the Nernstian slope 59.6/z mV per decade at 300 K. The current response is δI_D = g_m δV_th, so the *sensitivity* is g_m while the *thermodynamic* transduction is fixed. Consequently the limit of detection in activity is

  δln a|min = z q √(S_{V_th} Δf)/g_m,  (9.10)

with Δf the measurement bandwidth. Since OECTs maximize g_m at fixed geometry (Corollary 8.2) but also maximize S_{V_th} through 1/f noise (§9.4), the optimum is not automatically volumetric: substituting (8.7) shows that in the ion-limited regime the detectivity improves only as √(W/L)/√(ρ_eℓ_e), independent of d.

*Proof.* Chain rule from the Nernst relation through g_m; noise-limited resolution is the input-referred noise integrated over the bandwidth. The scaling statement follows from Theorem 8.5 and Corollary 9.8. ∎

This is, again, a thickness-invariance theorem — the third in this paper. Thickness invariance appears to be the organizing principle of volumetric organic devices.

---

## 10. Sharpness, Degenerate Cases, Counterexamples, and Open Problems

### 10.1 Failure of monotonicity

The constraint σ̃′ ≥ 0 used in §7.5 is not universal. In a heavily doped mixed conductor, fixed anionic sites are Coulomb scattering centres; dedoping (decreasing p) reduces their screened density relative to carriers and can *increase* μ. Then μ′(p) > 0 while p decreases with V_G, and σ̃ can be non-monotone. All identification results of §7.2 remain valid (they do not use monotonicity), but the regularized inversion must drop the constraint. This is a genuine, physically realized counterexample to a convenient mathematical assumption.

### 10.2 Failure of scale separation

Hypothesis H2 requires a_c ≪ ℓ. With ℓ ≈ 1.8 nm (Boltzmann) and a_c ≈ 1 nm, the inequality is marginal; with disorder-broadened ℓ ≈ 7 nm it is comfortable; with high-C_i gates driving ℓ below a molecular diameter it is violated outright. In the violated regime there is *no local constitutive law*: μ is a functional of the profile, not a function of the local density. The correct object is a nonlocal mobility kernel μ^{ij}(z, z′), and the homogenization must be performed jointly with the confinement, not after it. **Open Problem 1.** Construct the joint homogenization–confinement limit and determine whether the resulting μ_FE differs from the local prediction by an O(1) factor. We conjecture it does, and that this is a leading cause of the discrepancy between FET and time-of-flight mobilities in the same film.

### 10.3 Failure of the Einstein relation out of equilibrium

Proposition 2.3 is an equilibrium theorem. Under bias, the field tilts the landscape, detailed balance is broken, and D/μ = k_BT_eff/q defines at best a single number. **Proposition 10.1.** A nonequilibrium steady state admitting an effective temperature that reproduces D/μ need not reproduce the third or higher cumulants of displacement; hence T_eff is not a temperature in the fluctuation–dissipation sense. *Proof:* the second cumulant fixes one scalar; the third is an independent functional of the tilted rate matrix and is generically nonzero where the equilibrium value vanishes by parity (Theorem 4.14). ∎ Consequently "effective temperature" models of field-dependent mobility are internally consistent only at the level of second moments and must not be used to predict noise.

### 10.4 Neglected correlations

Corollary 3.3 gives r_c ≈ 16 nm ≫ ℓ ≈ 2 nm. The accumulation layer is therefore a strongly coupled two-dimensional plasma, and the mean-field Poisson–Boltzmann treatment of §3 neglects correlation corrections to p(n). **Open Problem 2.** Compute the leading correlation correction to the first integral (3.2) for a 2D one-component plasma with ε_eff = √(ε_∥ε_⊥) and determine its effect on ℓ(A). The relevant coupling parameter is Γ = q²/(4πε_eff a_2D k_BT) with a_2D = (πN_s)^{−1/2}; at N_s = 5.5×10¹⁵ m⁻², a_2D = 7.6 nm and Γ ≈ 2.1 — *not* weak coupling. The mean-field result (3.4) is therefore an estimate with uncontrolled corrections at high overdrive, and we state it as such.

### 10.5 The swing tension

Remark 9.10 identifies a genuine inconsistency between the exponential-tail model (which fits mobility, dispersion, and noise) and the observed near-constancy of subthreshold swings over several decades. **Open Problem 3.** Either the tail is not exponential over the relevant range, or the swing is dominated by a different capacitance (interface states with a flat spectrum), or the current in subthreshold is not proportional to n_f. These are distinguishable by combining (9.8) with (9.9) on the same device.

### 10.6 The bipolar case and the recombination zone

For ambipolar operation, electrons and holes coexist and recombine. The capture-limited (Langevin) coefficient follows exactly from the Onsager radius:

**Proposition 10.2.** k_L = 4π r_c (D_n + D_p) = q(μ_n + μ_p)/ε, with r_c = q²/(4πεk_BT).

*Proof.* Diffusion-limited capture at the radius where Coulomb energy equals k_BT gives the Smoluchowski rate 4πr_c(D_n+D_p); substitute r_c and the Einstein relation. ∎ Numerically k_L ≈ 1.0×10⁻⁶ cm³ s⁻¹ for μ_n + μ_p = 2 cm²V⁻¹s⁻¹, ε_r = 3.5.

**Proposition 10.3 (Emission-zone position).** In a light-emitting organic transistor with both channels saturated, the recombination plane sits at

  x_rec/L = μ_p A_p²/(μ_p A_p² + μ_n A_n²),  I_D = (WC_i/2L)(μ_pA_p² + μ_nA_n²),  (10.1)

with A_p, A_n the hole and electron overdrives at their respective injecting contacts.

*Proof.* Each channel obeys (6.6) over its own length L_p = x_rec, L_n = L − x_rec; equating currents and using L_p + L_n = L gives (10.1). ∎ Balanced transport (μ_pA_p² = μ_nA_n²) centres the zone; the formula is a direct design rule for avoiding electrode quenching.

### 10.7 What has not been proved

For clarity we list the load-bearing unproved elements: the constant c = 4/9 in (4.10); the local closure H3 in the strong-confinement regime; the neglect of correlations (§10.4); the identification ΔL ≃ λ in Proposition 9.5 (an estimate, not a theorem); and the one-phase Stefan closure in Proposition 8.7 (which neglects the electronic counter-flux). None of these is concealed in a later derivation; each is flagged where used.

**Conjecture 1 (Universality of the gain–delay factor).** For any unipolar organic transistor in the quasi-static regime with monotone σ̃, 1 ≤ ∂ln I_D/∂ln Q ≤ 2 + γ_max, with the lower bound attained only under velocity saturation.

**Conjecture 2 (Thickness invariance is generic).** Every figure of merit that is a product of a transconductance-like quantity and a bandwidth-like quantity in the volumetric regime is invariant under d ↦ κd, C* ↦ C*/κ. Theorems 8.5 and Proposition 9.11 are instances; we conjecture a general statement following from the fact that d and C* enter (2.6) only through the product C*d.

**Conjecture 3 (Identifiability from the full family).** The full two-parameter family I_D(V_G, V_D), measured on an open set and under hypotheses (i)–(iv) of Theorem 7.2 with κ = 0, determines (σ̃, R_c) uniquely. Theorem 7.2 proves this on the saturation branch; extension to the full family with V_D-dependent contacts remains open.

---

## 11. Physical Realizations, Parameter Regimes, and Falsifiable Predictions

### 11.1 Regime table

| Quantity | Symbol | small-molecule crystal | polymer film | mixed conductor (OECT) |
|---|---|---|---|---|
| disorder width | σ | 30–60 meV | 80–150 meV | 50–120 meV |
| σ̂ at 300 K | σ/k_BT | 1.2–2.3 | 3.1–5.8 | 1.9–4.6 |
| localization length | a | 0.3–1 nm | 0.2–0.5 nm | 0.3–1 nm |
| permittivity | ε_r | 3–4 (anisotropic) | 3–3.5 | 3–5 (+ ionic) |
| mobility | μ | 1–40 cm²/Vs | 10⁻³–1 cm²/Vs | 0.1–10 cm²/Vs |
| areal capacitance | C_i | 1–100 nF/cm² | 1–100 nF/cm² | 1–10 µF/cm² (EDL) |
| volumetric capacitance | C* | — | — | 10–100 F/cm³ |
| confinement length (3.4) | ℓ | 1–3 nm | 2–10 nm | ≈ d (Π ≫ 1) |
| penetration number (2.9) | Π | ≪ 1 | ≪ 1 | 10³–10⁵ |
| scale length (6.9) | λ | 30–150 nm | 50–200 nm | — (bulk device) |
| transfer length (6.10) | L_T | 10–100 nm | 50–500 nm | ≫ d |
| fractional order | α | 0.5–0.9 | 0.2–0.5 | 0.3–0.7 |
| noise exponent (9.8) | β | 0.1–0.5 | 0.5–0.8 | 0.3–0.7 |

### 11.2 Nine falsifiable predictions

1. **ℓ ∝ 1/A.** The channel confinement length, measured by e.g. impedance or in-situ optical probes, scales inversely with overdrive with the *parameter-free* coefficient 2ε(k_BT/q)/C_i of (3.4).
2. **Disorder broadening by α⁻¹.** Films with independently measured E_c show ℓ larger than the Boltzmann value by exactly E_c/k_BT.
3. **R_cW ∝ A^{−1/2}** with L_T ∝ A^{+1/2} at fixed ρ_c (Corollary 6.6), steepening when image-force lowering is active.
4. **Saturation-branch contact immunity.** μ(n) extracted from dI_D,sat/dV_G agrees with four-probe μ, while linear-branch extraction does not (Theorem 7.2 vs. Theorem 7.1).
5. **The A_c kink.** The double-slope position obeys (7.7) and shifts with V_D and ρ_c as predicted, at *fixed* material (Theorem 7.6).
6. **α + β = 1.** Time-of-flight dispersion and drain-current noise exponents sum to unity on the same film (Corollary 9.7).
7. **Gain–bandwidth thickness invariance.** g_m·f_c is unchanged when d is varied at fixed W/L and electrolyte (Theorem 8.5).
8. **Two scaling laws in d.** Small-signal τ ∝ d, large-signal dedoping τ ∝ d² (Lemma 8.4, Proposition 8.7).
9. **No Poole–Frenkel asymptote.** μ(F) is even and quadratic at small F; the √F law is confined to an intermediate window (Theorem 4.14).

Predictions 4–8 are directly actionable with standard instrumentation and constitute, collectively, a decisive test of the framework.

---

## 12. Conclusion

The organic transistor is not a silicon transistor with different numbers. It is a device whose transport coefficients are functionals of its own state, whose channel is a molecular monolayer, whose control terminal may act volumetrically, and whose measurement is structurally degenerate. We have shown that all four features follow from one variational structure — a gate-constrained degenerate gradient flow on a mixed conductor — and that the classical compact models are its leading-order asymptotic reductions with computable error terms.

Three results deserve emphasis for their practical consequence. The first integral ε E²/2 = p(n) gives the channel thickness in closed form and thereby proves that field-effect mobility is an interface measurement. The identifiability theorems prove that linear-regime mobility extraction is *impossible in principle* and that saturation-branch extraction is *possible in principle*, with explicit hypotheses and explicit failure modes; this converts a methodological dispute into a mathematical statement. The gain–bandwidth invariance theorem proves that the celebrated transconductance of electrochemical devices is bought, not earned, and identifies the only three levers that improve gain and speed together.

The theory also bounds its own domain: it predicts sub-molecular confinement lengths at high gate capacitance and thereby announces the crossover to volumetric operation; it identifies the marginality of scale separation in the monolayer channel; and it computes a plasma coupling parameter of order two, which means the mean-field electrostatics on which it rests is an estimate with uncontrolled corrections. We regard the explicit exhibition of these boundaries as part of the result, not as a caveat to it.

---

## Appendix A. The corrector problem and bounds

Let 𝒬_R = [−R,R]³ and let 𝔈_R be the Dirichlet form (4.4) restricted to sites in 𝒬_R. For a unit vector ξ, define the affine-plus-corrector trial field u_i = ξ·x_i + χ_i with χ stationary, mean-zero. Then by Theorem 4.3,

  ξ_i D_R^{ij} ξ_j = |𝒬_R|^{−1} inf_{χ} 𝔈_R(ξ·x + χ, ξ·x + χ),

and D_R^{ij} is monotone in R in the sense of quadratic forms under nested Dirichlet restrictions, giving convergence along subsequences; ergodicity (H1) upgrades this to almost-sure convergence to a deterministic limit and identifies the limit with (4.5). The dual Thomson principle provides lower bounds by exhibiting divergence-free unit flows; choosing flows supported on the critical percolation path yields the AHL lower bound used in Claim 4.12, while choosing the affine field itself (χ = 0) yields the elementary upper bound

  ξ_i D^{ij} ξ_j ≤ ½⟨Σ_j c_{0j}(ξ·r_{0j})²⟩,

which is the mean-field (effective-medium) estimate and *overestimates* D by a factor exponential in σ̂² — the quantitative reason mean-field hopping theories fail.

## Appendix B. Montroll–Weiss to fractional operator

Let the carrier perform a CTRW with jump kernel w(x) (finite second moment, drift b) and waiting density ψ. The Montroll–Weiss equation for the Fourier–Laplace transform of the propagator is

  ñ(k,s) = [1 − ψ̃(s)]/s · 1/[1 − ψ̃(s)ŵ(k)].

With ψ̃(s) = 1 − Γ(1−α)(τ₀s)^α + o(s^α) and ŵ(k) = 1 − ik·b − ½k_iΣ^{ij}k_j + …, expansion gives

  s ñ − n(0) = s^{1−α}/[Γ(1−α)τ₀^α] · [−ik·b − ½k_iΣ^{ij}k_j] ñ + o(1).

Recognizing s^{1−α} as the symbol of ₀D_t^{1−α} and inverting the transforms yields (5.3) with μ^{ij} = qb^{(i}…/k_BT and D^{ij} = Σ^{ij}/(2τ₀^α) — both carrying the *same* factor τ₀^{−α}, whence the invariance of D/μ claimed in Theorem 5.2. The Riemann–Liouville form follows from the identity ℒ{₀D_t^{1−α}h} = s^{1−α}h̃(s) for h with vanishing initial fractional integral.

## Appendix C. Algebra of the power-law family

With σ̃(u) = ku^{1+γ}, k = μ₀C_i/u₀^γ:

I_D = (W/L)∫₀^A ku^{1+γ}du = (W/L)kA^{2+γ}/(2+γ).

For the charge, change variables using dx = (Wσ̃/I_D)dV:

Q = W∫₀^L qN_s dx = (W²/I_D)∫₀^A (C_iu)(ku^{1+γ})du = (W²kC_i/I_D)A^{3+γ}/(3+γ)
 = WLC_iA(2+γ)/(3+γ).

Then C_gg = ∂Q/∂A = WLC_i(2+γ)/(3+γ), g_m = (W/L)kA^{1+γ}, and

f_T = g_m/(2πC_gg) = kA^{1+γ}(3+γ)/[2πL²C_i(2+γ)] = μ(A)A(3+γ)/[2πL²(2+γ)],
τ = Q/I_D = L²(2+γ)²/[(3+γ)μ(A)A],

with μ(A) ≡ μ₀(A/u₀)^γ. Multiplying gives f_Tτ = (2+γ)/(2π), consistent with (9.2).

## Appendix D. Principal symbols

| symbol | meaning | SI unit |
|---|---|---|
| a | localization length | m |
| A | overdrive V_G − V_th | V |
| α | fractional order k_BT/E_c | — |
| β (noise) | exponent of S_I ∝ f^{−β} | — |
| C_i | areal gate capacitance | F m⁻² |
| C* | volumetric capacitance q²∂p/∂ζ | F m⁻³ |
| d, t_s | film thickness | m |
| D^{ij}, μ^{ij} | diffusion, mobility tensors | m² s⁻¹, m² V⁻¹ s⁻¹ |
| ε^{ij} | absolute permittivity tensor | F m⁻¹ |
| E_c | exponential tail energy | J |
| ℱ | free energy functional (2.6) | J |
| G | sheet-conductance potential (6.5) | S V = A |
| λ | scale length (6.9) | m |
| ℓ | confinement length N_s/n(0) | m |
| L_T | transfer length √(ρ_cσ_s) | m |
| N_s | sheet carrier density | m⁻² |
| Π | penetration number C*d/C_i | — |
| p(n) | osmotic pressure (2.3) | Pa |
| ρ_c | specific contact resistivity | Ω m² |
| σ, σ̂ | disorder width, σ/k_BT | J, — |
| σ_s | sheet conductance | S |
| σ̃ | intrinsic sheet-conductance function | S |
| τ | transit time Q/I_D | s |
| ζ_a | chemical potential of species a | J |

---

## References

[1] A. Miller and E. Abrahams, *Impurity conduction at low concentrations*, Phys. Rev. **120** (1960) 745.
[2] V. Ambegaokar, B. I. Halperin, J. S. Langer, *Hopping conductivity in disordered systems*, Phys. Rev. B **4** (1971) 2612.
[3] H. Bässler, *Charge transport in disordered organic photoconductors: a Monte Carlo simulation study*, Phys. Status Solidi B **175** (1993) 15.
[4] W. F. Pasveer et al., *Unified description of charge-carrier mobilities in disordered semiconducting polymers*, Phys. Rev. Lett. **94** (2005) 206601.
[5] R. Coehoorn, W. F. Pasveer, P. A. Bobbert, M. A. J. Michels, *Charge-carrier concentration dependence of the hopping mobility in organic materials with Gaussian disorder*, Phys. Rev. B **72** (2005) 155206.
[6] M. C. J. M. Vissenberg and M. Matters, *Theory of the field-effect mobility in amorphous organic transistors*, Phys. Rev. B **57** (1998) 12964.
[7] T. Tiedje and A. Rose, *A physical interpretation of dispersive transport in disordered semiconductors*, Solid State Commun. **37** (1981) 49.
[8] G. Horowitz, *Organic field-effect transistors*, Adv. Mater. **10** (1998) 365.
[9] H. Scher and E. W. Montroll, *Anomalous transit-time dispersion in amorphous solids*, Phys. Rev. B **12** (1975) 2455.
[10] R. Metzler and J. Klafter, *The random walk's guide to anomalous diffusion: a fractional dynamics approach*, Phys. Rep. **339** (2000) 1.
[11] D. A. Bernards and G. G. Malliaras, *Steady-state and transient behavior of organic electrochemical transistors*, Adv. Funct. Mater. **17** (2007) 3538.
[12] Y. Roichman and N. Tessler, *Generalized Einstein relation for disordered semiconductors — implications for device performance*, Appl. Phys. Lett. **80** (2002) 1948.
[13] S. M. Kozlov, *Averaging of random operators*, Math. USSR Sb. **37** (1980) 167.
[14] G. C. Papanicolaou and S. R. S. Varadhan, *Boundary value problems with rapidly oscillating random coefficients*, in Random Fields (Esztergom, 1979), North-Holland.
[15] C. Kipnis and S. R. S. Varadhan, *Central limit theorem for additive functionals of reversible Markov processes and applications to simple exclusions*, Commun. Math. Phys. **104** (1986) 1.
[16] R. Jordan, D. Kinderlehrer, F. Otto, *The variational formulation of the Fokker–Planck equation*, SIAM J. Math. Anal. **31** (1998) 1.
[17] D. Kinderlehrer, L. Monsaingeon, X. Xu, *A Wasserstein gradient flow approach to Poisson–Nernst–Planck equations*, ESAIM Control Optim. Calc. Var. **23** (2017) 137.
[18] L. Onsager, *Reciprocal relations in irreversible processes I, II*, Phys. Rev. **37** (1931) 405; **38** (1931) 2265.
[19] C. Tanase, E. J. Meijer, P. W. M. Blom, D. M. de Leeuw, *Unification of the hole transport in polymeric field-effect transistors and light-emitting diodes*, Phys. Rev. Lett. **91** (2003) 216601.
[20] S. D. Baranovskii et al., *Theoretical description of charge transport in disordered organic semiconductors*, Phys. Status Solidi B **251** (2014) 487.
[21] H. H. Choi, K. Cho, C. D. Frisbie, H. Sirringhaus, V. Podzorov, *Critical assessment of charge mobility extraction in FETs*, Nat. Mater. **17** (2018) 2.
[22] E. G. Bittle, J. I. Basham, T. N. Jackson, O. D. Jurchescu, D. J. Gundlach, *Mobility overestimation due to gated contacts in organic field-effect transistors*, Nat. Commun. **7** (2016) 10908.
[23] S. Inal, J. Rivnay, A.-O. Suiu, G. G. Malliaras, I. McCulloch, *Conjugated polymers in bioelectronics*, Acc. Chem. Res. **51** (2018) 1368.
[24] A. L. McWhorter, *1/f noise and germanium surface properties*, in Semiconductor Surface Physics, Univ. of Pennsylvania Press (1957).
[25] L. K. J. Vandamme and G. Trefán, *1/f noise in polyacene thin film transistors*, IEE Proc. Circuits Devices Syst. **152** (2005) 401.
[26] R. A. Marcus, *Electron transfer reactions in chemistry: theory and experiment*, Rev. Mod. Phys. **65** (1993) 599.
[27] T. Holstein, *Studies of polaron motion II: the "small" polaron*, Ann. Phys. **8** (1959) 343.
[28] V. Coropceanu et al., *Charge transport in organic semiconductors*, Chem. Rev. **107** (2007) 926.
[29] H. Oberhofer, K. Reuter, J. Blumberger, *Charge transport in molecular materials: an assessment of computational methods*, Chem. Rev. **117** (2017) 10319.
[30] V. Podzorov et al., *Intrinsic charge transport on the surface of organic semiconductors*, Phys. Rev. Lett. **93** (2004) 086602.
[31] D. J. Frank, Y. Taur, H.-S. P. Wong, *Generalized scale length for two-dimensional effects in MOSFETs*, IEEE Electron Device Lett. **19** (1998) 385.
[32] H. H. Berger, *Models for contacts to planar devices*, Solid-State Electron. **15** (1972) 145.
[33] J. Rivnay, R. M. Owens, G. G. Malliaras, *The rise of organic bioelectronics*, Chem. Mater. **26** (2014) 679.
[34] C. L. Braun, *Electric field assisted dissociation of charge transfer states as a mechanism of photocarrier production*, J. Chem. Phys. **80** (1984) 2634.
[35] M. Pope and C. E. Swenberg, *Electronic Processes in Organic Crystals and Polymers*, 2nd ed., Oxford Univ. Press (1999).

---

*Manuscript ends. All numbered results not explicitly attributed to prior work are proved here under the stated hypotheses; results labelled Claim, Conjecture, or Open Problem are not load-bearing for any theorem without explicit flagging at the point of use.*
