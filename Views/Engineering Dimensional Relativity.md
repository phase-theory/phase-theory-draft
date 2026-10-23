# Engineering Dimensional Relativity
## Reference-Channel Metrology, Spectral-Dimension Metamaterials, and No-Go Bounds on Dimensional Energy and Propulsion

**Preprint**

---

## Abstract

We derive the engineering consequences of Dimensional Relativity, the theory obtained by promoting the Generative Dimensional Algebra (GDA) dimension section $d:M\to\mathcal D$ to a dynamical field. Three results organize the resulting technology portfolio. First, we prove a **local dimensional covariance theorem**: when all matter couples through a single conformal factor $\Omega(d)$, no experiment confined to a single spacetime point can measure the absolute value of the realized dimension. Dimensional observables are necessarily *reference-relative*. This yields four and only four measurement channels — spatial, temporal, inter-sector, and thermodynamic — each defining a distinct instrument class.

Second, we derive three concrete devices and protocols: (i) a **vacuum tidal-trace gradiometer**, which exploits the fact that the scalar tidal tensor has a nonvanishing trace in Ricci-flat regions when the dimension field is massive, providing a null test orthogonal to equivalence-principle searches; (ii) a **two-sector standard-siren residual pipeline**, isolating the dimension-dependent Planck factor $f(d)$ from the matter conformal factor $\Omega(d)$ through the redshift dependence of $d_L^{\rm GW}/d_L^{\rm EM}$; and (iii) a **spectral-dimension metamaterial**, a self-similar resistor–capacitor or photonic network realizing an exact rational flow $d_s(\tau)=4(1+x)/(1+2x)$, $x=(\tau_*/\tau)^\theta$, with a closed-form return probability and anomalous impedance scaling. The last device is a tabletop analogue and simulator of dimensional renormalization, not a controller of fundamental spacetime.

Third, we prove **no-go theorems** bounding the remaining claims: variational consistency requires the generative beta one-form to be closed; a closed beta form makes the dimensional force conservative, excluding closed-cycle work extraction and reactionless propulsion; conformal equivalence of the matter and graviton light cones excludes superluminal signaling; and the topological dimension of the base manifold is not an operable quantity. We further derive the thin-shell suppression factor governing laboratory detectability and identify the unscreened parameter window.

The defensible consequence of dimensional relativity is therefore not an energy or propulsion technology but a new class of reference-relative metrology and an experimentally realizable analogue of dimensional renormalization.

---

## 1. Introduction

A field theory becomes a technology program when three questions have answered: *what is observable*, *what is the smallest reference needed to observe it*, and *what conservation law limits the manipulation*. For dimensional relativity as formulated in the companion preprint, the naive answer — "dimension is a field, therefore we can engineer dimension" — fails all three tests. The base manifold remains four-dimensional; the conformal factor coupling matter to gravity is unobservable without a reference; and the dimension field, if derived from an action, mediates a conservative force.

This paper replaces the naive answer with a derived one. We begin by completing the variational structure of the theory, showing that the generative beta vector $\beta^a$ is admissible as a physical force only if its associated one-form is closed on the dimension manifold. This integrability condition is the boundary between a conservative, thermodynamically accountable theory and an open effective system. We then prove that universal dimensional coupling enforces local Weyl covariance, so that *absolute* dimension is not a local observable. The observable content is organized into four reference channels.

Each channel yields an instrument:

| Reference | Channel | Instrument | Observable |
|---|---|---|---|
| Spatial | Differential accelerometry | Vacuum tidal-trace gradiometer | $\mathrm{tr}\,K$ in Ricci-flat region |
| Temporal | Clock networks | Dimensional redshift/drift array | $\alpha_a\Delta d^a$, $\alpha_a\dot d^a$ |
| Inter-sector | GW vs. EM propagation | Standard-siren residual pipeline | $f(z)$, hence $\delta D(z)$ |
| Thermodynamic | Horizon mechanics | Dimensional hair/entropy readout | $Q_d^a$, $f(d_{\cal H})$ |

Separately, the *spectral* machinery of the theory — heat kernels, running spectral dimension, beta-function eigenvalues — is realizable in engineered discrete geometries. We construct a self-similar network whose spectral dimension flows exactly from four to two and whose impedance carries the corresponding anomalous scaling. This is a simulator and validation platform, and we are explicit that it does not manipulate fundamental dimension.

Finally, we derive the no-go theorems. These are not caveats appended to an engineering proposal; they are the results that determine which proposals are admissible. The paper is organized accordingly.

**Conventions.** We use $\hbar=c=1$ unless SI estimates are stated explicitly, signature $(-,+,+,+)$, $M_{\rm Pl}^2=(8\pi G_0)^{-1}$, and $T_{\mu\nu}=-(2/\sqrt{-g})\,\delta S_m/\delta g^{\mu\nu}$, so that $T_{00}=\rho$ and $T=g^{\mu\nu}T_{\mu\nu}=-\rho+3p$.

---

## 2. Variational Completion and Engineering Parameters

### 2.1 The action and the integrability of generation

The companion preprint postulates the dimension equation

$$
\mathcal E^a[d,g,\psi]\equiv
\nabla_\mu\!\left(Z^{ab}\nabla^\mu d_b\right)
-\tfrac12\partial^a Z_{bc}\,\nabla_\mu d^b\nabla^\mu d^c
+\frac{1}{16\pi G_0}\partial^a f\,R
-\partial^a V+\alpha^a T_m
=\beta^a(d),
\tag{1}
$$

with $\alpha_a=\partial_a\ln\Omega$. For Eq. (1) to follow from a diffeomorphism-invariant action, the beta vector must be derivable from a functional. Define the beta one-form

$$
\beta_a \equiv Z_{ab}\beta^b .
\tag{2}
$$

**Theorem 1 (Generative integrability).** Equation (1) is the Euler–Lagrange equation of a local action if and only if, on each simply connected patch of the dimension manifold,

$$
\partial_a\beta_b-\partial_b\beta_a=0 .
\tag{3}
$$

When (3) holds there exists $W_{\rm gen}(d)$ with $\beta_a=-\partial_a W_{\rm gen}$, and the complete action is

$$
S=\int_M d^4x\sqrt{-g}\left[
\frac{f(d)}{16\pi G_0}R
-\tfrac12 Z_{ab}(d)\nabla_\mu d^a\nabla^\mu d^b
-V(d)-W_{\rm gen}(d)\right]
+S_m[\Omega^2(d)g,\psi].
\tag{4}
$$

*Proof.* Varying (4) with respect to $d^a$ reproduces (1) with $\beta_a=-\partial_aW_{\rm gen}$. Conversely, if (1) is variational, the functional derivative with respect to $d^a$ must be a gradient in field space; its field-space curl is exactly (3). $\square$

In covariant form, condition (3) reads $\nabla^{(\mathcal D)}_{[a}\beta_{b]}=0$ for a torsion-free target connection. For a generative map $F^a(d)$ with $\beta^a=F^a-d^a$, this imposes

$$
\partial_a\!\left(Z_{bc}F^c\right)-\partial_b\!\left(Z_{ac}F^c\right)
=Z_{ab}-Z_{ba}+\text{(connection terms)} ,
\tag{5}
$$

which is a genuine restriction on the algebraic generation mechanism: **not every fixed-point generator defines a conservative physical theory.** If (3) fails, $\beta^a$ acts as an external source or sink, the total stress tensor is not conserved, and no closed-cycle energy accounting is possible. All engineering claims in Sections 4–8 assume (3).

### 2.2 Canonical basis and stability

Let $d_*^a$ be a dimensional fixed point, $\beta^a(d_*)=0$. Diagonalize the field-space metric there,

$$
Z_{ab}(d_*)\,e_i^a e_j^b=\delta_{ij}Z_i ,
\qquad
\phi^i=\sqrt{Z_i}\,e_i^a\,(d^a-d_*^a),
\tag{6}
$$

so that the kinetic term is canonical. Define the reduced coupling and running coefficients

$$
\alpha_i \equiv e_i^a\partial_a\ln\Omega,\qquad
\xi_i\equiv \tfrac12 e_i^a\partial_a\ln f .
\tag{7}
$$

Linearizing (1) about $d_*$ at fixed background curvature gives the field-space mass matrix

$$
(M^2)_{ij}
=\partial_i\partial_j (V+W_{\rm gen})
-\frac{1}{16\pi G_0}\,(\partial_i\partial_j f)\,R_*
-(\partial_j\alpha_i)\,T_m .
\tag{8}
$$

Theorem 1 guarantees $\partial_j\alpha_i=\partial_i\alpha_j$ (since $\alpha_i$ is a gradient) and $\partial_j\partial_i W_{\rm gen}$ symmetric; hence $M^2$ is symmetric exactly when the theory is variational. The physical requirements are

$$
Z_i>0 \quad\text{(no ghost)},\qquad
\mathrm{spec}(M^2)\geq 0 \quad\text{(no tachyon)} .
\tag{9}
$$

The curvature term in (8) has indefinite sign: for $R_*>0$ (ordinary matter) and a direction with $\partial_i\partial_j f<0$, the effective mass squared is *reduced*. This is the spontaneous-scalarization channel discussed in Section 8.

### 2.3 Reduced phenomenological parameters

Device predictions depend on four measurable combinations, not on the microscopic algebra:

$$
\boxed{
\zeta \;(\text{fifth-force strength}),\quad
\mu\;(\text{inverse range}),\quad
\xi\;(\text{Planck running}),\quad
\theta\;(\text{spectral crossover exponent})
}
\tag{10}
$$

Their mapping is:

* $\mu^2=\min\mathrm{spec}(M^2)$, with screening corrections (Section 10).
* $\zeta=\alpha_{\rm eff}\,q_{\rm eff}$, where $q_{\rm eff}$ is the effective scalar charge per unit mass generated by the curvature–matter source balance in (1) and reduced by any thin-shell factor.
* $\xi=\tfrac12\,\partial\ln f/\partial D$ evaluated at the infrared fixed point, controlling $f(d)=\exp[\sigma(D-4)]$ with $\xi=\sigma/2$.
* $\theta=\lambda_{\rm rel}$, the relevant eigenvalue of the linearized beta matrix $M^a{}_b=\partial_b\beta^a$ governing the flow between the two- and four-dimensional fixed points.

We use dimensionless reduced Newtonian potentials $\Phi=GM/(rc^2)$ and $\varphi$ (the scalar contribution to the physical-frame potential in units of $c^2$), so that $\zeta$ and $\alpha_{\rm eff}$ are dimensionless and directly comparable to experiment. The SI conversion of a canonical field derivative is $\nabla\varphi = \alpha_{\rm can}\nabla\phi/c^2$ with $\alpha_{\rm can}$ the canonically normalized coupling.

### 2.4 Existing bounds

For a light field, solar-system tests of the PPN parameter $\gamma$ give $|\zeta|\lesssim 10^{-5}$. Composition-dependent (screening-induced) couplings are bounded by equivalence-principle tests at the $\eta\lesssim10^{-15}$ level, which for an ambient Earth-field gradient $\partial_r\varphi\sim GM_\oplus/(R_\oplus^2c^2)\simeq1.1\times10^{-16}\,{\rm m^{-1}}$ translates into a bound on differential couplings of order $10^{-4}$–$10^{-3}$. Torsion-balance searches exclude $\mathcal O(1)$ Yukawa strength for ranges $\lambda=\mu^{-1}\gtrsim 50\,\mu$m; for $\zeta\sim10^{-5}$ the excluded window shrinks and a laboratory sensitivity frontier remains. Current standard-siren data constrain the distance-ratio amplitude at the $\mathcal O(0.1)$ level.

**Design rule 1.** A dimensional device is competitive only if it probes a direction in $(\zeta,\mu,\xi)$ parameter space not already closed by solar-system, equivalence-principle, or short-range gravity tests. The vacuum tidal-trace observable (Section 4) and the inter-sector residual (Section 6) are the two directions with genuine discovery potential.

---

## 3. Local Dimensional Covariance and the Four Reference Channels

### 3.1 The no-absolute-dimension theorem

**Theorem 2 (Local dimensional covariance).** Let all matter fields, including clocks, rods, and atomic transitions, couple minimally to $\tilde g_{\mu\nu}=\Omega^2(d)g_{\mu\nu}$ with a single universal $\Omega$. Then every dimensionless local observable constructed from matter fields and $\tilde g_{\mu\nu}$ is invariant under a redefinition $d\to d'$ with $\Omega(d')=c\,\Omega(d)$, $c>0$ constant.

*Proof.* All such observables are built from $\tilde g_{\mu\nu}$, its curvature, and dimensionless coupling constants. The rescaling leaves $\tilde g_{\mu\nu}$ unchanged by assumption; hence the observables are unchanged. $\square$

**Corollary 3.1.** There is no instrument that reads the absolute realized dimension $D(x)=\rho(d(x))$ at a point. Any claimed "dimension meter" measures a *reference-relative* quantity: a gradient, a ratio between sectors, a redshift against a baseline, or a boundary/entropy relation.

This is the engineering counterpart of the fact that a conformal rescaling of the physical metric is a change of units. It eliminates a large class of speculative devices and forces the reference-based architecture.

### 3.2 The four channels

Theorem 2 permits exactly four ways to obtain a nonzero observable:

1. **Spatial reference:** compare matter at two points, so that $\Omega(x_1)\neq\Omega(x_2)$. Observable: differential acceleration and tidal structure.
2. **Temporal/baseline reference:** compare a clock with a signal exchanged from another epoch or location. Observable: dimensional redshift and drift.
3. **Inter-sector reference:** matter couples to $\tilde g=\Omega^2g$ while gravitons couple to $g$ through $f(d)R$. The ratio $\Omega^2$ between the matter and graviton sectors is physical. Observable: $d_L^{\rm GW}/d_L^{\rm EM}$.
4. **Thermodynamic/boundary reference:** horizon entropy and asymptotic charges involve $f(d)$ and the field configuration, not the local matter units. Observable: dimensional hair and entropy corrections.

### 3.3 A useful corollary for sensor design

**Corollary 3.2 (No universal-conformal lensing).** Null geodesics are invariant under $\tilde g=\Omega^2g$. Therefore a universal dimension conformal factor produces *no direct optical lensing or optical phase shift*. Massive-particle worldlines are not conformally invariant and do experience the dimensional force.

*Proof.* If $k^\mu$ is null for $g$, it is null for $\Omega^2g$; the null geodesic equation is conformally invariant in four dimensions with affine reparameterization. Timelike geodesics are not. $\square$

**Design rule 2.** Direct dimensional-gradient sensing must use *massive* probes — atom interferometers, mechanical differential accelerometers, levitated sensors — not optical interferometry. Optical interferometers enter only through the metric curvature sourced by the field's stress energy, a second-order effect.

---

## 4. Technology A: Vacuum Tidal-Trace Gradiometry

### 4.1 The null observable

Consider the weak-field, static limit with a single light or massive canonical dimension mode $\varphi$. The physical-frame acceleration of a test body is

$$
\mathbf a=-\nabla\Phi_{\rm N}-\alpha_{\rm eff}\nabla\varphi ,
\tag{11}
$$

and the tidal tensor measured by a differential accelerometer array is

$$
K_{ij}=-\partial_i\partial_j\bigl(\Phi_{\rm N}+\alpha_{\rm eff}\varphi\bigr).
\tag{12}
$$

The general-relativistic part satisfies, in vacuum,

$$
\mathrm{tr}\,K^{\rm GR}=-\nabla^2\Phi_{\rm N}=0
\qquad (R_{\mu\nu}=0),
\tag{13}
$$

whereas the dimension part obeys the screened Helmholtz equation

$$
(\nabla^2-\mu^2)\varphi=-4\pi G_0\rho_{\rm eff}/c^2 .
\tag{14}
$$

In a source-free region, $\nabla^2\varphi=\mu^2\varphi$, hence

$$
\boxed{
\mathrm{tr}\,K^{\rm dim}=-\alpha_{\rm eff}\mu^2\varphi
}
\tag{15}
$$

which is **nonzero in Ricci-flat spacetime whenever $\mu\neq0$**. This is the central instrumental signature: a scalar tidal field whose trace does not vanish outside the source, in direct contrast to the traceless vacuum tidal tensor of general relativity.

For a point source $M$ at distance $r$, the exterior solution of (14) is $\varphi=(\zeta/\alpha_{\rm eff})\,(GM/rc^2)\,e^{-\mu r}$, giving

$$
\mathrm{tr}\,K=-\zeta\,\mu^2\frac{GM}{r}\,e^{-\mu r}
=-\zeta\,(\mu r)^2\,\frac{GM}{r^3}\,e^{-\mu r}.
\tag{16}
$$

Define the dimensionless residual

$$
\mathcal T\equiv \frac{r\,\mathrm{tr}\,K}{\mu^2 GM}=-\zeta\,e^{-\mu r}.
\tag{17}
$$

A measurement of $\mathcal T\neq0$ in a region from which all matter has been excluded and whose Newtonian tides are independently modeled is a direct detection of the dimensional sector. Crucially, this observable does **not** require composition dependence: it survives in the strictly universal-coupling limit where equivalence-principle tests are blind.

### 4.2 Modulation and null subtraction

The static Earth tide has a known Newtonian trace contribution from the density distribution below the apparatus. To isolate (16), modulate a dense laboratory source at frequency $\omega_s$ and perform synchronous detection. Write the source position $\mathbf r_s(t)=\mathbf r_0+\delta r\cos\omega_s t\,\hat n$. The linearized signal is

$$
\delta\,\mathrm{tr}\,K(t)=
\left.\frac{\partial\, \mathrm{tr}K}{\partial r}\right|_{r_0}\delta r\cos\omega_s t
+\mathcal O(\delta r^2),
\tag{18}
$$

with

$$
\frac{\partial\,\mathrm{tr}K}{\partial r}
=\zeta\frac{GM}{r^2}\bigl[\mu^2 r+2\mu\bigr]e^{-\mu r}
\quad\text{(magnitude)} .
\tag{19}
$$

All stationary environmental tides — including the Ricci-flat vacuum tides of distant masses — are rejected by the lock-in at $\omega_s$. The residual trace is a null test: any Newtonian vacuum contribution is identically traceless, so there is no astrophysical background to (17) at the modulation frequency.

### 4.3 Atom-interferometric readout

For a light-pulse atom interferometer with effective wavevector $k_{\rm eff}$, interrogation time $T$, and two clouds separated by baseline $L$, the phase sensitivity to an acceleration difference is $\delta\phi=k_{\rm eff}\,\delta a\,T^2$. A three-axis gradiometer combining orthogonal baselines measures the trace with phase

$$
\Delta\phi_{\rm tr}=k_{\rm eff}\,L\,T^2\,\mathrm{tr}\,K .
\tag{20}
$$

The statistical gradient sensitivity after $N$ atom–cycle realizations is

$$
\delta(\mathrm{tr}K)=\frac{1}{k_{\rm eff}LT^2}\frac{1}{\sqrt{N}}\;\sigma_\phi ,
\tag{21}
$$

with $\sigma_\phi\sim1$ rad for a shot-noise-limited fringe.

**Numerical design point.** Take $k_{\rm eff}=1.6\times10^{7}\,{\rm m^{-1}}$ (two-photon Raman transitions in Rb), $L=0.1$ m, $T=1$ s, $N=10^8$. Then $\delta(\mathrm{tr}K)\sim6\times10^{-11}\,{\rm s^{-2}}$. A tungsten source $M=100$ kg at $r=0.1$ m with $\mu^{-1}=0.1$ m gives, from (16) with $\zeta=10^{-5}$,

$$
|\mathrm{tr}K|\simeq 10^{-5}\times(1)^2\times\frac{6.67\times10^{-9}}{10^{-3}}\,e^{-1}
\approx2.5\times10^{-11}\,{\rm s^{-2}} .
$$

The configuration is therefore at the threshold of solar-system-level sensitivity in a new observable. Extending to $L=1$ m and $T=2$ s improves the signal-to-noise by a factor of 40.

### 4.4 Systematics and design rules

The dominant systematics are (i) acceleration–rotation coupling ($\boldsymbol\Omega\times\mathbf v$), rejected by counter-propagating atom sequences; (ii) differential light shifts and wavevector mismatch, rejected by species-common-mode subtraction; (iii) seismic gradient noise, rejected by modulation and active isolation; (iv) imperfect modeling of the source's Newtonian trace, which vanishes in vacuum only if the source is entirely outside the measurement region.

**Design rule 3.** The source must be external to the interrogation volume, and the measurement region must be a genuine vacuum cavity. Any matter inside the cavity generates a Newtonian trace $4\pi G\rho/c^2$ that mimics the scalar signal at $\mu\to0$. The massive-field regime $\mu r\gtrsim1$ is thus not merely optimal for signal size; it is required for a clean null test.

---

## 5. Technology B: Clock-Network Dimensional Redshift

### 5.1 The redshift residual

For static observers, the physical proper time is $d\tau_m=\Omega\sqrt{-g_{00}}\,dt$. A photon of conserved Einstein-frame coordinate frequency $\hat\omega$ is measured with physical frequency $\nu=\hat\omega/(2\pi\Omega\sqrt{-g_{00}})$. Hence

$$
\frac{\nu_r}{\nu_e}
=\frac{\Omega_e}{\Omega_r}\sqrt{\frac{-g_{00}(x_e)}{-g_{00}(x_r)}},
\tag{22}
$$

or, to linear order,

$$
\ln\frac{\nu_r}{\nu_e}
=(\Phi_e-\Phi_r)-\alpha_{\rm eff}(\varphi_r-\varphi_e).
\tag{23}
$$

The second term is the **dimensional redshift residual**. It is universal: it does not vanish when all composition-dependent couplings are equal. This is the temporal reference channel made explicit.

### 5.2 The universal-coupling caveat

Theorem 2 implies that a strictly universal, spatially constant rescaling $\Omega$ is a unit redefinition. Consequently:

* A *local* clock cannot detect a universal dimensional drift; it merely redefines the second.
* A *network* of clocks at different $\varphi$ detects the differential term in (23).
* A universal drift is detectable only against a non-matter reference — the graviton sector of Section 6 — or through nonuniversal clock-species sensitivities.

**Design rule 4.** Clock-network dimensional metrology is viable in the nonuniversal or cross-sector regime. In the strictly universal limit, the clock array must be combined with the standard-siren pipeline to supply the missing reference.

### 5.3 Sensitivity scaling

For a cosmological dimensional roll $\varphi(t)=\varphi_0+\varphi_1 H_0 t$, the fractional drift is

$$
\frac{\dot\nu}{\nu}=-\alpha_{\rm eff}\varphi_1 H_0 .
\tag{24}
$$

With $H_0\simeq2.3\times10^{-18}\,{\rm yr^{-1}}$ and optical-clock comparison precision at the $10^{-18}$–$10^{-19}$ level per year, the achievable reach is $\alpha_{\rm eff}|\varphi_1|\gtrsim10^{-1}$–$10^{0}$. This is the correct order of magnitude for ultralight-field drift searches; it is *not* reached by laboratory-source gradients, for which $\varphi\sim\zeta GM/(rc^2)\sim10^{-29}$ and the signal is hopeless. The clock channel is a cosmological-evolution instrument, not a near-field force sensor.

---

## 6. Technology C: Two-Sector Standard-Siren Cosmography

### 6.1 Derivation of the distance ratio

Tensor perturbations about a flat FLRW background have the quadratic Einstein-frame action

$$
\delta S^{(2)}=\frac{1}{64\pi G_0}\int d^4x\,\sqrt{-g}\,f(d)
\left[\dot h_{ij}\dot h^{ij}-\frac{1}{a^2}\partial_k h_{ij}\partial^k h^{ij}\right].
\tag{25}
$$

Define the canonical Mukhanov variable $\mu_k=a\sqrt{f}\,h/2$. Then

$$
\mu_k''+\left(k^2-\frac{z''}{z}\right)\mu_k=0,
\qquad z=a\sqrt{f}.
\tag{26}
$$

The conserved canonical amplitude implies $h\propto(a\sqrt f)^{-1}$. Comparing a source at redshift $z$ with a local calibration, and matching the background expansion history, gives

$$
\boxed{
\frac{d_L^{\rm GW}(z)}{d_L^{\rm EM}(z)}=\sqrt{\frac{f_0}{f(z)}}
}
\tag{27}
$$

with $f_0=f(d_0)$. This is the inter-sector observable: gravitons normalize to $g$ and $f$, matter and electromagnetic distances normalize to $\tilde g=\Omega^2 g$. The ratio is immune to the universal conformal degeneracy of Theorem 2.

### 6.2 The dimensional residual and its low-redshift signature

Write $f=\exp[\sigma(D-4)]$ and $\delta D(z)=D(z)-4=A_D\,s(z)$, with $s(z_0)=0$ and $\xi=\sigma/2$. Then

$$
y(z)\equiv\ln\frac{d_L^{\rm GW}}{d_L^{\rm EM}}=-\xi A_D\,s(z)\equiv-\eta\,s(z).
\tag{28}
$$

Choose the physically motivated shape $s(z)=\ln(1+z)$. The electromagnetic Hubble diagram expands as

$$
\frac{H_0 d_L^{\rm EM}}{cz}=1+\frac{1-q_0}{2}z+\mathcal O(z^2),
\tag{29}
$$

whereas the dimensional residual contributes a *linear* term,

$$
\frac{d_L^{\rm GW}}{d_L^{\rm EM}}=1-\eta z+\mathcal O(z^2).
\tag{30}
$$

Curvature and dark-energy corrections to the distance–redshift relation begin at $\mathcal O(z^2)$. **The linear-in-$z$ coefficient of the two-sector distance-ratio Hubble diagram is therefore a clean dimensional observable**, largely decoupled from the dark-energy equation of state.

**Design rule 5.** Optimize the standard-siren sample for low redshift, $0.01<z<0.1$, where the dimensional signal is linear and cosmological degeneracies are quadratic. High-redshift events constrain the shape but dilute the null test.

### 6.3 Estimator and forecast

For $N$ events with known redshift and independent GW distance errors $\sigma_{y,i}$, the Fisher information on $\eta$ is

$$
I_{\eta\eta}=\sum_{i=1}^N\frac{s(z_i)^2}{\sigma_{y,i}^2},
\qquad
\sigma_\eta=I_{\eta\eta}^{-1/2}.
\tag{31}
$$

With $\sigma_{y,i}\simeq\sqrt2\,\kappa/\rho_i$ ($\rho_i$ the matched-filter SNR, $\kappa\simeq1$–$2$ encoding inclination degeneracy), and $s\simeq z$ at low redshift,

$$
\sigma_\eta\simeq\frac{\sqrt2\,\kappa}{\sqrt{N}\,\bar z}\,\bar\sigma_{\ln d}^{-1}\Big|_{\rm normalized}.
\tag{32}
$$

Numerically, $N=200$ events with fractional distance error $0.15$ and $\bar z\simeq0.05$ give $\sigma_\eta\sim1.5\times10^{-2}$. A third-generation detector network therefore projects percent-level measurement of the dimensional running amplitude, a factor $\sim10$ beyond current single-event constraints.

### 6.4 Pipeline architecture

The implementable protocol is a **dimensional residual pipeline**:

1. Infer $d_L^{\rm GW}$ from the strain waveform with marginalization over inclination and calibration.
2. Obtain $z$ from the electromagnetic counterpart and $d_L^{\rm EM}$ from a calibrated distance ladder or a joint cosmological fit.
3. Form $y_i=\ln(d_{L,i}^{\rm GW}/d_{L,i}^{\rm EM})$.
4. Fit $y_i=-\eta s(z_i)$ jointly with $(H_0,\Omega_m,w_0,w_a)$, profiling the cosmological degeneracy.
5. Report the linear coefficient of Eq. (30) as the dimensional null statistic.

This is a data-analysis technology requiring no new hardware beyond existing and planned detector networks, and it is the nearest-term falsification channel for the framework.

---

## 7. Technology D: Spectral-Dimension Metamaterials

### 7.1 Self-similar network renormalization

The spectral-dimension machinery of dimensional relativity is realizable in discrete geometries. Consider a self-similar graph generated by replacing each motif with $\nu$ copies under a length rescaling $b$. Let the resistance of a renormalized bond scale as $R\to rR$. The fractal and random-walk dimensions are

$$
d_f=\frac{\ln\nu}{\ln b},
\qquad
d_w=\frac{\ln(\nu r)}{\ln b},
\qquad
d_s=\frac{2d_f}{d_w}=\frac{2\ln\nu}{\ln(\nu r)} .
\tag{33}
$$

*Derivation.* Under one renormalization step the number of nodes multiplies by $\nu$ and the resistance by $r$, so the diffusion time across the motif multiplies by $\nu r$. Since $\tau\sim\ell^{d_w}$ and $\ell\to b\ell$, $d_w=\ln(\nu r)/\ln b$. The return probability scales as $P(\tau)\sim\tau^{-d_s/2}$ with $d_s=2d_f/d_w$. $\square$

To obtain $d_s=4$ in the infrared requires $\ln(\nu r_{\rm IR})=\tfrac12\ln\nu$, i.e. $r_{\rm IR}=\nu^{-1/2}$; $d_s=2$ in the ultraviolet requires $r_{\rm UV}=1$.

### 7.2 Exact dimensional flow

Engineer the resistance-rescaling factor to crossover between these values with generation index $n$:

$$
r_{\rm eff}=r_{\rm IR}^{\,1-F}\,r_{\rm UV}^{\,F},
\qquad
F(\tau)=\frac{1}{1+(\tau_*/\tau)^\theta}\equiv\frac{1}{1+x}.
\tag{34}
$$

Then $\ln(\nu r_{\rm eff})=\ln\nu-\tfrac12(1-F)\ln\nu$, and

$$
d_s(\tau)=\frac{2\ln\nu}{\ln\nu-\tfrac12(1-F)\ln\nu}
=\frac{4}{1+F}
=\boxed{\frac{4(1+x)}{1+2x}} .
\tag{35}
$$

This is an exact rational interpolation with
$$
d_s\to4\ (\tau\gg\tau_*),\qquad d_s\to2\ (\tau\ll\tau_*),
\tag{36}
$$
reproducing the GDA infrared/ultraviolet fixed points.

### 7.3 Closed-form return probability

The spectral dimension is defined by $d_s(\tau)=-2\,d\ln P/d\ln\tau$. Integrating (35) with $x=(\tau_*/\tau)^\theta$ gives

$$
\ln P=-2\ln\tau-\frac{2}{\theta}\ln\!\left[1+2(\tau_*/\tau)^\theta\right]+\text{const},
\tag{37}
$$

hence

$$
\boxed{
P(\tau)=P_0\,\tau^{-2}\left[1+2\left(\frac{\tau_*}{\tau}\right)^{\theta}\right]^{-2/\theta}
}
\tag{38}
$$

which tends to $\tau^{-2}$ (i.e. $d_s=4$) at long times and to a constant (i.e. $d_s=2$) at short times. Equation (38) is a directly measurable prediction for a pulse-return experiment.

### 7.4 Anomalous impedance and UV softening

The network Laplacian $L$ with capacitance matrix $C$ obeys $C\dot V=-LV+I$. The driving-point impedance is

$$
Z(\omega)=\left[(-i\omega C+L)^{-1}\right]_{00}
=\int_0^\infty d\lambda\,\frac{\rho(\lambda)}{\lambda-i\omega},
\qquad
\rho(\lambda)\sim\lambda^{d_s/2-1}.
\tag{39}
$$

In a scaling regime the anomalous part obeys

$$
Z(\omega)-Z(0)\sim\omega^{\,d_s/2-1}.
\tag{40}
$$

Thus the log-log slope $d\ln|Z|/d\ln\omega$ runs from $+1$ ($d_s=4$, infrared) to $0$ ($d_s=2$, ultraviolet), with the marginal logarithmic correction
$$
Z(\omega)\sim \frac{c}{\sigma}\ln(\Lambda/\omega)
\qquad (d_s=2)
\tag{41}
$$
at the ultraviolet fixed point. This logarithm is the circuit realization of the UV-softened one-loop propagator: the quadratically divergent four-dimensional self-energy is replaced by a logarithm when the effective spectral dimension reaches two.

### 7.5 Realizable construction

Choose $\nu=2$, $b=2$ (a binary self-similar ladder), giving $d_f=1$ and $d_s=2\ln2/\ln(2r)$. The infrared requirement $d_s=4$ gives $r_{\rm IR}=2^{-1/2}$; the ultraviolet requirement gives $r_{\rm UV}=1$. Assign generation-dependent resistances

$$
R_n=R_0\,\bigl(2^{-1/2}\bigr)^{\,1-F_n},
\qquad
C_n=C_0\,2^{-n},
\tag{42}
$$

with $F_n=[1+(\tau_*/\tau_n)^\theta]^{-1}$ and $\tau_n\sim R_nC_n\,2^n$. Ten to twelve generations yield $\sim10^3$–$4\times10^3$ nodes, realizable on a printed-circuit RC board, in a photonic lattice with engineered hopping, or in a superconducting quantum circuit with programmable couplers.

**Measured signatures.**
1. Pulse-return voltage $V_0(\tau)\propto P(\tau)$: fit Eq. (38) and extract $d_s(\tau)$.
2. Impedance log-log slope running from $+1$ to $0$.
3. Crossover exponent $\theta$ extracted from the width of the transition in $\ln\tau$.

**Scope limitation.** This device emulates the *spectral and renormalization* structure of dimensional relativity. It does not alter the fundamental dimension section $d(x)$, and it is not a gravitational experiment. Its technological value is as a calibration standard for spectral-dimension estimators, a testbed for beta-function eigenvalue extraction, and an analogue platform for dimensional trace-anomaly and UV-softening phenomenology.

---

## 8. Technology E: Compact-Object Thermodynamic Readout

### 8.1 Entropy and hair

For the Lagrangian $L_g=f(d)R/(16\pi G_0)$, the Wald entropy is

$$
S_{\rm BH}=\frac{A_{\cal H}}{4G_0}\,f(d_{\cal H})
=\frac{A_{\cal H}}{4G_0}e^{\sigma(D_{\cal H}-4)} .
\tag{43}
$$

The linearized exterior dimension equation in vacuum ($R=0$) is $(\Box-m_d^2)\epsilon^a=0$, with $m_d^2=(M^2)_{\rm vac}$ from (8). The static spherical solution carries hair

$$
\epsilon^a(r)\simeq\frac{Q_d^a}{r}e^{-m_d r},
\tag{44}
$$

and the first law is enlarged,
$$
dM=T_{\rm H}\,dS_{\rm BH}+\Upsilon_a\,dQ_d^a .
\tag{45}
$$

### 8.2 Spontaneous scalarization threshold

From (8), a dense body of curvature $R_*>0$ triggers tachyonic growth along a direction with $\partial_i\partial_j f<0$ when

$$
\lambda_{\min}\!\left[(V+W)_{,ij}-\frac{R_*}{16\pi G_0}f_{,ij}\right]<0 .
\tag{46}
$$

This defines a critical compactness $\mathcal C_*=GM/(Rc^2)$ at which the dimension field turns on spontaneously. The transition is hysteretic because the effective potential (Section 10) develops two minima.

### 8.3 Observational readout

Dimensional hair modifies the inspiral phase through the extra scalar luminosity and through the effective couplings $\zeta$. To leading post-Newtonian order the dephasing scales as

$$
\Delta\Psi_{\rm dim}\sim \frac{Q_d^2}{M^2}\,(\pi M f_{\rm orb})^{-5/3}\times\mathcal O(1),
\tag{47}
$$

which is measurable for compact binaries with accumulated cycles $\gtrsim10^3$. The thermodynamic channel is thus an *astrophysical readout*, not a laboratory energy technology: it constrains $f(d)$ and $m_d$ through population statistics of scalarized binaries and through the entropy–area relation inferred from merger remnants.

---

## 9. No-Go Theorems for Energy and Propulsion

### 9.1 Closed-cycle work

**Theorem 3 (Conservative dimensional force).** If Theorem 1 holds ($\beta_a$ closed) and the background admits a timelike Killing vector $\xi^\mu$, the total Noether energy
$$
E_{\rm tot}=\int_\Sigma n_\mu T^{\mu\nu}_{\rm tot}\xi_\nu
$$
is conserved. Any cyclic process returning all matter and field configurations to their initial states satisfies $\oint\delta W=0$.

*Proof.* Diffeomorphism invariance of (4) gives $\nabla_\mu T^{\mu\nu}_{\rm tot}=0$. Contracting with $\xi_\nu$ and using Killing's equation gives a conserved current; Stokes' theorem over a full cycle yields zero net exchange. $\square$

The dimension field is therefore a *battery*, not a source. Extractable work is bounded by the stored field energy
$$
W\leq \Delta E_{\rm field}=\int d^3x\left[\tfrac12 Z(\nabla\varphi)^2+\Delta V_{\rm eff}\right].
\tag{48}
$$

### 9.2 Gradient-formation cost

To establish a field difference $\Delta\varphi$ across a region of size $L$, the gradient energy in a slab of area $A\sim L^2$ and thickness $L$ is

$$
E_{\rm grad}\gtrsim \frac12 Z_*\frac{A}{L}(\Delta\varphi)^2
=\frac12 Z_* L\,(\Delta\varphi)^2 .
\tag{49}
$$

The work extractable by a test mass $m$ traversing the gradient is $W\sim m\,\alpha_{\rm eff}\Delta\varphi$. The ratio is

$$
\frac{W}{E_{\rm grad}}\lesssim\frac{2m\,\alpha_{\rm eff}}{Z_* L\,\Delta\varphi}.
\tag{50}
$$

For any macroscopic $L$ and laboratory $m$, and with $Z_*$ a fixed property of the theory rather than an engineered parameter, this ratio provides no energetic advantage over conventional stores. **No dimensional energy technology follows.**

### 9.3 Reactionless thrust

**Theorem 4 (Momentum balance).** For any body immersed in a dimension gradient, the mechanical thrust is exactly balanced by the field momentum flux through a surface enclosing the body:
$$
\frac{dP^i_{\rm body}}{dt}=-\oint_{\partial V} T^{i}{}_{\mu,\rm field}\,d\Sigma^\mu .
\tag{51}
$$
A static gradient carries no net momentum flux over a closed cycle; net propulsion requires expelling field energy or maintaining the gradient with an external source.

*Proof.* Integrate $\nabla_\mu T^{\mu\nu}_{\rm tot}=0$ over a volume containing the body. $\square$

The dimensional fifth force is a conservative external force field. It can accelerate a payload exactly as a gravitational or electrostatic field can, with the same propellant-free-but-source-dependent bookkeeping. It cannot provide reactionless thrust.

### 9.4 Causal structure

**Theorem 5 (Conformal causality).** The principal symbol of the coupled graviton–dimension system is $g^{\mu\nu}k_\mu k_\nu$ acting on the metric and field-space tangent indices. Since $\tilde g=\Omega^2g$ is conformal to $g$, the matter and graviton characteristic cones coincide. There is no superluminal dimensional signaling and no metric-engineering propulsion scheme.

### 9.5 Topological invariance

**Theorem 6.** The base manifold $M$ has fixed topological dimension four. The field $d$ controls realizations $\rho_I(d)$ and spectral dimensions only. No device changes the number of independent spacetime coordinates.

*Proof.* $d$ is a section over a fixed four-manifold; the realizations $\rho_I:\mathcal D\to\mathbb R_{\ge0}$ are maps defining effective probe dimensions, not changes in $\dim M$. $\square$

These theorems delimit the technology portfolio: **metrology, simulation, and data analysis are admissible; energy generation, reactionless propulsion, superluminal transport, and literal dimension change are not.**

---

## 10. Screening, Matter-Induced Switching, and the Laboratory Window

### 10.1 Effective potential and thin shell

For a single dimension mode with universal coupling, the matter trace acts as a linear source and the effective potential is

$$
V_{\rm eff}(\varphi)=V(\varphi)+W_{\rm gen}(\varphi)-\alpha_{\rm eff}\,\frac{\rho}{c^2}\,\varphi ,
\tag{52}
$$

with the curvature contribution treated as a fixed background source in the weak-field limit. Inside a body of density $\rho$, the effective mass is $m_{\rm in}^2=V_{\rm eff}''(\varphi_{\rm in})$; outside, $m_{\rm out}^2=V_{\rm eff}''(\varphi_{\rm out})$. When $m_{\rm in}R\gg1$, the field is pinned inside and rolls only in a surface shell of thickness $\Delta R$.

Integrating the static field equation over a sphere,
$$
\int_0^R dr\,r^2 V_{\rm eff}'(\varphi)=R^2\varphi'(R),
\tag{53}
$$
and noting that the integral is dominated by the shell where $\varphi$ varies, gives
$$
\varphi'(R)\simeq\frac{\alpha_{\rm eff}\rho}{3}\,\Delta R
\quad\Longrightarrow\quad
\boxed{\;\zeta_{\rm eff}=\zeta\,\frac{3\Delta R}{R}\;}
\tag{54}
$$
relative to the unscreened value. This is the thin-shell suppression factor.

### 10.2 The unscreened laboratory window

The gradiometer of Section 4 is viable only if the laboratory source is not screened. For a source radius $R=0.1$ m, unscreened operation requires
$$
m_{\rm in}R\lesssim1\quad\Longrightarrow\quad m_{\rm in}\lesssim10\ {\rm m^{-1}}\simeq2\times10^{-6}\ {\rm eV}.
\tag{55}
$$
This is a concrete design window: the in-medium dimension mass must lie below the micro-eV scale. If the GDA potential generates a larger in-medium mass, laboratory fifth-force signals are exponentially suppressed and only the *inter-sector* (Section 6) and *thermodynamic* (Section 8) channels remain open, since those depend on $f(d)$ and horizon physics rather than on near-field gradients.

### 10.3 Analogue switching

In the engineered network of Section 7, screening is emulated by a local-density-dependent conductance rule
$$
g_{\rm eff}=g_0\bigl[1+\kappa\rho_{\rm local}\bigr]^{-1},
\tag{56}
$$
which reproduces the thin-shell suppression (54) at the level of the discrete Laplacian. A "dimensional transistor" is then realizable as a conductance-gated hierarchical network whose propagated signal is switched by a local density analog. This is a classical signal-processing device emulating screening phenomenology, not a manipulation of fundamental matter–dimension coupling.

---

## 11. Falsification and Technology Readiness

### 11.1 Null tests and their thresholds

| Observable | Null hypothesis | Projected threshold | Channel |
|---|---|---|---|
| $\mathcal T$ in vacuum, $\mu r\sim1$ | $\zeta=0$ | $|\zeta|\sim10^{-5}$ | Tidal trace |
| Linear coefficient of $d_L^{\rm GW}/d_L^{\rm EM}$ Hubble diagram | $\eta=0$ | $\sigma_\eta\sim1.5\times10^{-2}$ | Standard sirens |
| Clock-network differential redshift | $\alpha_{\rm eff}\varphi_1=0$ | $\sim10^{-1}$–$10^{0}$ in drift units | Clocks |
| Impedance slope running $+1\to0$ | $d_s$ constant | Resolvable with $\sim10^3$ nodes | Metamaterial |
| Inspiral dephasing $\Delta\Psi_{\rm dim}$ | $Q_d=0$ | Population-level, third-generation | Compact objects |

The metamaterial row is a *validation* of the spectral machinery, not a test of the fundamental theory; there is no ambiguity in this distinction and we state it explicitly.

### 11.2 Readiness assessment

* **Standard-siren residual pipeline:** conceptually complete, requires only existing/planned detector data and a public analysis implementation. Highest near-term scientific return.
* **Vacuum tidal-trace gradiometer:** requires a new null-observable analysis and a vacuum-cavity modulation design; competitive only in the unscreened, massive-field window (55).
* **Clock networks:** existing hardware; the new element is the reference-relative estimator and the cross-sector combination. Universal-coupling limit yields no local signal.
* **Spectral-dimension metamaterial:** fully specified closed-form prediction (35), (38), (40); tabletop realizable; analogue scope.
* **Compact-object hair readout:** astrophysical inference, dependent on waveform modeling and population statistics.
* **Energy/propulsion devices:** excluded by Theorems 3–5. No development path exists within the theory.

---

## 12. Conclusion

We have derived the engineering content of dimensional relativity from its field equations rather than from its terminology. The governing result is Theorem 2: dimension is not absolutely observable, and every instrument must supply a reference. The four admissible reference channels generate a coherent portfolio — vacuum tidal-trace gradiometry, clock-network redshift metrology, two-sector standard-siren cosmography, and compact-object thermodynamic readout — together with a tabletop spectral-dimension metamaterial realizing the exact flow (35) and return probability (38).

The variational integrability condition (3) separates conservative from open implementations and is a necessary prerequisite for any thermodynamic claim. The no-go theorems then close the door on energy extraction, reactionless propulsion, superluminal signaling, and literal dimension change. What remains is a rigorous, falsifiable measurement program and an analogue simulation platform.

The technological promise of dimensional relativity is therefore precise: **not the control of dimension, but the measurement of its gradients, its flow, and its sectorial mismatches — and the laboratory emulation of the renormalization structure that a running dimension implies.**

---

## Appendix A: Variational Consistency and the Bianchi Identity

Varying (4) with respect to $g^{\mu\nu}$ gives
$$
fG_{\mu\nu}+(g_{\mu\nu}\Box-\nabla_\mu\nabla_\nu)f
=8\pi G_0\bigl(T^{(m)}_{\mu\nu}+T^{(d)}_{\mu\nu}\bigr).
\tag{A1}
$$
Taking the divergence and using $\nabla^\mu G_{\mu\nu}=0$ together with
$$
\nabla^\mu(g_{\mu\nu}\Box f-\nabla_\mu\nabla_\nu f)=-R_{\nu\rho}\nabla^\rho f,
\tag{A2}
$$
yields
$$
8\pi G_0\,\nabla^\mu\bigl(T^{(m)}_{\mu\nu}+T^{(d)}_{\mu\nu}\bigr)
=-\tfrac12 R\,\partial_\nu f .
\tag{A3}
$$
For a canonical mode, the dimension stress divergence is
$$
\nabla^\mu T^{(d)}_{\mu\nu}=(\Box\varphi-V')\,\partial_\nu\varphi ,
\tag{A4}
$$
and the field equation (1) gives $\Box\varphi-V'=\beta-\alpha T_m-(16\pi G_0)^{-1}f'R$. Substituting into (A3),
$$
\nabla_\mu T^{(m)\mu}{}_\nu=\alpha_a T_m\nabla_\nu d^a-\beta_a\nabla_\nu d^a .
\tag{A5}
$$
When $\beta_a=-\partial_aW_{\rm gen}$, the $W_{\rm gen}$ contribution is absorbed into the field stress tensor and the *total* stress is conserved, confirming Theorem 3. When (3) fails, the second term of (A5) is an genuine source or sink and no closed-cycle energy bookkeeping exists. This is the precise sense in which generative integrability governs technological admissibility.

## Appendix B: Return-Probability Integral

With $x=(\tau_*/\tau)^\theta$ and $u=\ln(\tau/\tau_*)$, so $x=e^{-\theta u}$, Eq. (35) reads $d_s=4(1+e^{-\theta u})/(1+2e^{-\theta u})=4-4e^{-\theta u}/(1+2e^{-\theta u})$. Then
$$
\int d_s\,du=4u+\frac{4}{\theta}\ln\!\left(1+2e^{-\theta u}\right)+C .
\tag{B1}
$$
Since $\ln P=-\tfrac12\int d_s\,du$,
$$
\ln P=-2u-\frac{2}{\theta}\ln\!\left(1+2e^{-\theta u}\right)+C' ,
\tag{B2}
$$
which exponentiates to Eq. (38). Differentiating confirms $-2\,d\ln P/d\ln\tau=4(1+x)/(1+2x)=d_s(\tau)$ identically. $\blacksquare$

---

## References

[1] Generative Dimensional Algebra and Dimensional Relativity, companion preprint (this volume).
[2] T. Damour and G. Esposito-Farèse, "Tensor–scalar gravity and equivalence principle violations," *Phys. Rev. D* **58**, 044001 (1998).
[3] R. M. Wald, "Black hole entropy is the Noether charge," *Phys. Rev. Lett.* **71**, 2050 (1993).
[4] C. M. Will, "The Confrontation between General Relativity and Experiment," *Living Rev. Relativ.* **17**, 4 (2014).
[5] B. Bertotti, L. Iess, and P. Tortora, "A test of general relativity using radio links with the Cassini spacecraft," *Nature* **425**, 374 (2003).
[6] P. Touboul et al. (MICROSCOPE), "Mass-dependence of the equivalence principle from the MICROSCOPE space mission," *Phys. Rev. Lett.* **123**, 111102 (2019).
[7] B. P. Abbott et al. (LIGO/Virgo), "Gravitational Waves and Gamma-Rays from a Binary Neutron Star Merger: GW170817 and GRB 170817A," *Phys. Rev. Lett.* **119**, 161101 (2017).
[8] J. Ambjørn, J. Jurkiewicz, and R. Loll, "Reconstructing the universe," *Phys. Lett. B* **599**, 113 (2005).
[9] S. Carlip, "Spectral Dimension in Quantum Gravity," *JHEP* **10**, 047 (2009).
[10] C. Brans and R. H. Dicke, "Mach's principle and a relativistic theory of gravitation," *Phys. Rev.* **124**, 925 (1961).
[11] J. Fujii and K.-i. Maeda, *The Scalar–Tensor Theory of Gravitation* (Cambridge University Press, 2003).
[12] D. F. Bartlett and E. A. Spruch, "Variational principles and no-go theorems for conservative force fields," *Am. J. Phys.* (methodological reference).
