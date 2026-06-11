# Off-Shell Physics

### The Spectral Content of Interacting Propagators as an Unmined Phenomenological Resource, with a Formalization of the Physical Meaning of Branch Cuts in Full QCD Propagators

*A Quantum Field Theory White Paper*

*Version 1.0 — June 2026*

---

## Abstract

The modern amplitudes program has been spectacularly successful by treating off-shell structure as scaffolding to be removed: on-shell recursion, unitarity cuts, generalized unitarity, and the analytic bootstrap all express scattering data in terms of gauge-invariant, on-shell building blocks, and they relegate the off-shell continuation of correlation functions to the status of an unphysical, scheme-dependent artifact. This white paper argues the opposite thesis. The off-shell two-point function of an interacting field — its full analytic structure across the entire complex momentum plane, not merely its poles — is a carrier of genuine, in-principle-measurable physical content. We give a self-contained formalization of that content through the Källén–Lehmann (KL) representation and its generalizations, and we develop in detail the physics encoded in the **branch cuts** of full QCD propagators (gluon, ghost, quark). We show that (i) the *position* of the leading cut encodes thresholds and asymptotic-state masses; (ii) the *discontinuity across the cut* (the spectral function) is a positive-definite probability density for physical degrees of freedom and a *signed*, sum-rule-constrained density for confined ones; (iii) the *failure* of the ordinary KL representation in QCD — manifested as complex-conjugate (cc) poles, negative spectral weight, and cuts off the real axis — is not a pathology but a quantitative diagnostic of confinement and of the breakdown of a particle interpretation; and (iv) anomalous thresholds and Landau singularities of dressed vertices carry compositeness and binding-radius information. We close by laying out a concrete phenomenological program — the "unmined resource" — spanning transport coefficients, dilepton and photon emissivities, spectral sum rules, hadron-structure observables, and reconstruction methodology, together with the obstructions (the ill-posed inverse problem, reflection-positivity violation) that must be confronted to harvest it.

---

## Table of Contents

1. [Motivation: Why Off-Shell Is Not a Defect](#1-motivation)
2. [The Off-Shell Vertex and the Virtuality Continuum](#2-the-off-shell-vertex)
3. [The Källén–Lehmann Representation: Derivation and Anatomy](#3-the-kallen-lehmann-representation)
4. [The Physical Content Encoded in Analytic Structure](#4-the-physical-content)
5. [Branch Cuts in Full QCD Propagators — A Formalization](#5-branch-cuts-in-full-qcd-propagators)
6. [Generalized Spectral Representations: Complex Poles and Off-Axis Cuts](#6-generalized-spectral-representations)
7. [Reflection Positivity, the Schwinger Function, and Confinement](#7-reflection-positivity)
8. [Anomalous Thresholds and Dressed Vertices](#8-anomalous-thresholds)
9. [The Unmined Phenomenological Resource — A Program](#9-the-unmined-resource)
10. [The Inverse Problem: Obstructions and Methodology](#10-the-inverse-problem)
11. [Conjectures, Open Problems, and Falsifiable Predictions](#11-open-problems)
12. [Conclusions](#12-conclusions)
13. [Notation and Conventions](#13-notation)
14. [Annotated References](#14-references)

---

<a name="1-motivation"></a>
## 1. Motivation: Why Off-Shell Is Not a Defect

A Feynman diagram is built from interaction vertices that are *defined off the mass shell*. An internal line carries a four-momentum $k$ that is not constrained by $k^2 = m^2$; the propagator $1/(k^2 - m^2 + i\epsilon)$ is integrated over all virtualities. This is not a regrettable feature of a particular calculational scheme — it is forced by locality. A local interaction term $\mathcal{L}_{\rm int}(x)$ couples fields at a single spacetime point; Fourier-transforming a product of fields at coincident points convolves their momenta with no on-shell constraint. Virtuality is the momentum-space shadow of locality.

The on-shell amplitudes program has, for excellent reasons, sought to bypass off-shell intermediate data:

- **Gauge artifacts.** Off-shell Green's functions are gauge-dependent and field-redefinition–dependent. Only on-shell, amputated, gauge-invariant combinations are observable in the $S$-matrix.
- **Redundancy.** Off-shell currents carry "pure gauge" and "contact" pieces that cancel in any complete amplitude.
- **Efficiency.** BCFW recursion, generalized unitarity, and the analytic bootstrap construct amplitudes from on-shell lower-point data, never touching the off-shell continuation.

These are real virtues *for the $S$-matrix*. But the $S$-matrix is not the only observable in QFT, and the off-shell two-point function is special among off-shell objects:

> **Central claim.** The interacting propagator $G(p)$, viewed as an analytic function on the complex $p^2$ plane, is — up to field renormalization — a *physical* object. Its full analytic structure (poles, residues, branch points, discontinuities, and their locations on physical and unphysical Riemann sheets) is a gauge-fixed but physically interpretable encoding of the spectrum, lifetimes, thresholds, and bound-state/compositeness content of the theory. The discontinuity across its cuts — the **spectral function** — is, for physical fields, a positive probability density directly tied to inclusive cross sections; for confined fields, it is a signed, sum-rule-constrained density whose very signs diagnose confinement.

The "poles-only" habit — read off masses and widths from the nearest singularities and discard the rest — throws away the continuum. The continuum *is* the multiparticle physics: thresholds, final-state interactions, anomalous (compositeness) thresholds, transport spectral weight, and emission rates. This white paper formalizes that content and argues that the QCD propagator cut structure is a largely **unmined phenomenological resource**.

---

<a name="2-the-off-shell-vertex"></a>
## 2. The Off-Shell Vertex and the Virtuality Continuum

### 2.1 Off-shell Green's functions

Let $\phi$ be an interacting field. The connected $n$-point functions
$$
G_n(x_1,\dots,x_n) = \langle \Omega | T\,\phi(x_1)\cdots\phi(x_n) |\Omega\rangle_{\rm conn}
$$
are defined for all configurations of arguments and, in momentum space, for all virtualities of the external legs. The LSZ reduction formula extracts the $S$-matrix by amputating external propagators and going on shell,
$$
\langle f | i T | i \rangle = \left(\prod_a \lim_{p_a^2\to m_a^2}\frac{p_a^2 - m^2}{\sqrt{Z}}\right) G_n(p_1,\dots,p_n),
$$
discarding everything except the leading multiple pole. LSZ is a *projection*: it is information-destroying by design. The off-shell $G_n$ contains strictly more than the $S$-matrix it projects onto.

### 2.2 The 1PI vertex and the effective action

The off-shell content is organized by the effective action $\Gamma[\phi]$, whose functional derivatives are the one-particle-irreducible (1PI) vertices $\Gamma_n$. The two-point 1PI function is the inverse propagator,
$$
G_2(p) = \frac{i}{\Gamma_2(p)}, \qquad \Gamma_2(p) = p^2 - m_0^2 - \Sigma(p^2),
$$
with $\Sigma$ the self-energy. The self-energy is intrinsically off-shell: it is a function of $p^2$ *everywhere*, and its analytic structure (Section 5) is what dresses the bare pole into the full singularity manifold of the interacting theory. The statement "vertices are defined off-shell" is, at the level of the two-point function, the statement that $\Sigma(p^2)$ is a nontrivial analytic function whose imaginary part across cuts is physical.

### 2.3 Why the two-point function is privileged

For $n>2$, off-shell Green's functions mix genuine dynamics with gauge and reparametrization redundancy. For $n=2$, the situation is cleaner:

- The position of the pole (a complex number) is gauge-independent in gauge theories for *physical* states (Nielsen identities) and gauge-fixing-independent for the pole mass even when the residue and continuum are not.
- The spectral function of a *physical, color-singlet, gauge-invariant* interpolating operator is unambiguously positive and tied to a total cross section via the optical theorem.

It is precisely this privileged status that makes the propagator's off-shell structure a resource rather than a redundancy. The subtleties for QCD's *elementary* fields (gluon, quark, ghost) — which are gauge-variant and confined — are not a retreat from this claim but its sharpest application: there, the *violation* of the clean structure is itself the physics (Sections 5–7).

---

<a name="3-the-kallen-lehmann-representation"></a>
## 3. The Källén–Lehmann Representation: Derivation and Anatomy

### 3.1 Derivation for a scalar field

Consider a Hermitian scalar field $\phi$ in a theory with a positive-definite Hilbert space, a unique vacuum $|\Omega\rangle$, and a complete set of eigenstates $|\lambda\rangle$ of the four-momentum $P^\mu$ with $P^\mu|\lambda_{\mathbf p}\rangle = p^\mu|\lambda_{\mathbf p}\rangle$. Insert the resolution of the identity into the Wightman function and use Lorentz invariance plus translation invariance:
$$
\langle \Omega | \phi(x)\phi(0)|\Omega\rangle
= \int_0^\infty \frac{d\mu^2}{2\pi}\,\rho(\mu^2)\,\Delta_+(x;\mu^2),
$$
where $\Delta_+(x;\mu^2)$ is the free Wightman function of mass $\mu$, and
$$
\boxed{\;\rho(\mu^2) = (2\pi)\sum_\lambda \delta(\mu^2 - m_\lambda^2)\,|\langle\Omega|\phi(0)|\lambda\rangle|^2 \;\ge 0\;}
$$
is the **spectral density**. Positivity of $\rho$ is a direct consequence of the positive-definiteness of the state-space norm: it is a sum of squared moduli of overlaps. From here the time-ordered (Feynman) propagator inherits the representation
$$
\boxed{\;G(p^2) = \int_0^\infty \frac{d\mu^2}{2\pi}\,\frac{\rho(\mu^2)}{p^2 - \mu^2 + i\epsilon}\;}
$$
(plus possible subtractions to ensure convergence at large $\mu^2$). This is the **Källén–Lehmann (KL) spectral representation**. It is *exact* and *nonperturbative*.

### 3.2 Anatomy of the representation

The KL representation displays the full analytic structure transparently:

- **Isolated pole.** A stable one-particle state of mass $m$ contributes $\rho(\mu^2) \supset 2\pi Z\,\delta(\mu^2 - m^2)$, giving a simple pole $G(p^2)\supset Z/(p^2-m^2+i\epsilon)$. The residue $Z$ is the field-strength/wavefunction renormalization, $0\le Z\le 1$, and equals the squared overlap of the field with the one-particle state.
- **Continuum / branch cut.** Multiparticle states with $\mu^2 \ge \mu_{\rm th}^2$ contribute a continuous $\rho(\mu^2)$, generating a **branch cut** of $G$ running along the real axis from the lowest multiparticle threshold $\mu_{\rm th}^2$ (e.g. $(2m)^2$ for two-particle production) to $+\infty$. Across this cut,
$$
\boxed{\;\rho(\mu^2) = \frac{1}{\pi}\,\mathrm{Im}\,G(\mu^2 + i\epsilon) = \frac{1}{2\pi i}\,\mathrm{Disc}\,G(\mu^2)\;}
$$
The branch cut *is* the multiparticle continuum. The discontinuity across it is the spectral function.
- **Resonance / unstable particle.** An unstable state does **not** appear as a real-axis pole. It appears as a complex pole on the *second (unphysical) Riemann sheet*, reached by analytic continuation through the cut. Its location $p^2 = M^2 - iM\Gamma$ encodes mass $M$ and width $\Gamma$; on the physical sheet it manifests only as a *bump* in the continuous $\rho(\mu^2)$ on the real axis. This is the precise sense in which "a resonance is a feature of the cut, not a pole of the propagator."

### 3.3 Spectral sum rules

The large-$p^2$ (UV) behavior of $G$, fixed by renormalization-group (RG) improved perturbation theory and asymptotic freedom in QCD, constrains the integral of $\rho$ through superconvergence and sum-rule relations of the form
$$
\int_0^\infty d\mu^2\,\rho(\mu^2)\,\mu^{2n} = (\text{UV-determined constant}),
$$
for suitable $n$ (when the integrals converge). These sum rules tie the IR/continuum content of $\rho$ to the UV anomalous dimensions and are the backbone of the phenomenological program in Section 9. The canonical commutation relation enforces, for an elementary canonically normalized field, the **unsubtracted sum rule** $\int_0^\infty \frac{d\mu^2}{2\pi}\rho(\mu^2) = 1$, partitioning unit spectral weight between the pole ($Z$) and the continuum ($1-Z$).

### 3.4 Fermion and vector generalizations

For a Dirac field the representation carries Dirac structure,
$$
S(p) = \int_0^\infty d\mu \left[\frac{\rho_1(\mu)\,\slashed{p} + \rho_2(\mu)\,\mu}{p^2-\mu^2+i\epsilon}\right],
$$
with separate scalar and vector spectral densities $\rho_{1,2}$ obeying positivity constraints ($\rho_1\ge 0$, $|\rho_2|\le\rho_1$ for physical fermions). For a vector field one separates transverse and longitudinal parts, each with its own spectral density; gauge invariance (Ward–Takahashi/Slavnov–Taylor identities) constrains the longitudinal sector. These generalizations are essential below because the QCD fields are a quark (Dirac), a gluon (vector), and a ghost (Grassmann scalar).

---

<a name="4-the-physical-content"></a>
## 4. The Physical Content Encoded in Analytic Structure

We now itemize, in increasing subtlety, the physical information carried by the off-shell propagator beyond its leading pole. This is the conceptual core of the "unmined resource."

| Analytic feature | Physical content | Observable handle |
|---|---|---|
| Real-axis pole at $p^2=m^2$ | Stable asymptotic particle, mass $m$ | Particle mass; particle in spectrum |
| Pole residue $Z$ | Field–state overlap | Normalization of inclusive rates; $1-Z$ = continuum weight |
| Leading branch point $\mu_{\rm th}^2$ | Lowest multiparticle threshold | Production threshold; final-state phase space |
| Shape of $\rho$ above threshold | Multiparticle continuum, final-state interactions | Inclusive cross section (optical theorem) |
| Bump in $\rho$ / 2nd-sheet pole | Resonance mass $M$ and width $\Gamma$ | Lineshape; lifetime $\tau=1/\Gamma$ |
| Anomalous threshold below normal threshold | Compositeness / bound-state size | Form-factor radius; molecular vs. compact structure |
| $\rho(\omega\to 0)$ (transport peak) | Zero-frequency response | Transport coefficients (viscosity, conductivity, diffusion) |
| Sign of $\rho$ | Positivity (physical) vs. its violation (confined) | Confinement diagnostic |
| Complex-conjugate poles on principal sheet | Absence of particle interpretation | Confinement / non-unitary effective d.o.f. |
| Off-real-axis cuts | Breakdown of standard causality/KL representation | Non-trivial confining analytic structure |

The right-hand column is the thesis in operational form: each analytic feature maps to something one can, at least in principle, measure or constrain. The amplitudes-program reflex keeps only the first two rows. The remaining rows are the resource.

### 4.1 The optical theorem as the bridge

For a *physical* current $J$ (e.g. the electromagnetic current), the spectral function of its two-point correlator is, by the optical theorem, proportional to a total cross section:
$$
\rho_{JJ}(s) \;\propto\; \mathrm{Im}\,\Pi(s) \;\propto\; \sigma_{\rm tot}(e^+e^-\to\text{hadrons}) \quad (\text{at } s>0).
$$
This is the cleanest demonstration that a propagator's *cut* (not its pole) is a direct observable: the famous $R$-ratio is literally a propagator discontinuity. Everything in this white paper is, in a sense, the systematic generalization of this single fact to the full set of QCD correlators and to off-shell, gauge-variant constituents.

---

<a name="5-branch-cuts-in-full-qcd-propagators"></a>
## 5. Branch Cuts in Full QCD Propagators — A Formalization

We now address the explicit charge of this white paper: **to formalize the physical content of the branch cuts in full QCD propagators.** We treat the Landau-gauge gluon, ghost, and quark propagators, and we are careful to distinguish what is rigorous, what is scheme/gauge dependent, and what is conjectural.

### 5.1 Setup and conventions

Work in Euclidean signature where lattice and functional (Dyson–Schwinger, DSE; functional renormalization group, fRG) methods produce data, and analytically continue to Minkowski/complex momenta. Write the Euclidean momentum as $p^2 = p_E^2 \ge 0$ (spacelike). The transverse gluon and the ghost propagators in Landau gauge are
$$
D_{\mu\nu}(p) = \left(\delta_{\mu\nu} - \frac{p_\mu p_\nu}{p^2}\right)\frac{Z(p^2)}{p^2}, \qquad
D_{\rm gh}(p) = -\frac{G(p^2)}{p^2},
$$
with dressing functions $Z, G$. The quark propagator is
$$
S(p) = \frac{1}{i\slashed{p}\,A(p^2) + B(p^2)} = \frac{-i\slashed{p}\,A + B}{p^2 A^2 + B^2}, \qquad M(p^2) = \frac{B}{A}.
$$
The complex momentum-squared variable will be denoted $z \equiv p^2 \in \mathbb{C}$. The "Minkowski axis" corresponds to $z<0$ (timelike) in this Euclidean convention; the branch cut of an ordinary KL propagator lies on the timelike real axis $z\le -\mu_{\rm th}^2$.

### 5.2 The ideal (KL-compatible) cut and its physical content

If a QCD correlator admitted an ordinary KL representation, its analytic structure would be: a function holomorphic in the cut $z$-plane, with a **single branch cut on the timelike real axis** starting at the lowest physical threshold, and discontinuity $\rho \ge 0$. The physics of *that* cut is unambiguous and is the baseline against which QCD's deviations are measured:

1. **Threshold = lowest accessible multiparticle (color-singlet) state.** Because gluons and quarks are confined, the lowest physical states reachable by a colored interpolating field are color-singlet combinations. For the ghost, which interpolates no asymptotic state at all, the leading non-analyticity is a logarithmic scattering cut tied to ghost–gluon multiparticle states.

2. **Discontinuity = decay/scattering density.** The imaginary part of the dressing across the cut measures the rate at which a virtual constituent "dissolves" into the multiparticle continuum — the dressing of the propagator by interactions. For the gluon this is the gluon self-energy's absorptive part (gluon$\to$gluon-gluon, gluon$\to$ghost-ghost, gluon$\to$quark-antiquark loops); for the quark it is the quark self-energy's absorptive part (quark$\to$quark+gluon).

3. **Logarithmic UV cut = asymptotic freedom.** RG improvement makes the dressing functions behave as powers of $\log z$ at large spacelike $z$. A logarithm has a branch cut. This **perturbative logarithmic cut** is present in *every* QCD correlator and runs along the entire timelike axis; its discontinuity is the perturbative spectral tail fixed by anomalous dimensions. This is the model-independent, always-present cut, and its strength is set by $\gamma$ and $\beta_0$.

> **Formalization 1 (Perturbative tail).** For any QCD propagator dressing $F(z)$ with one-loop anomalous dimension $\gamma$ and $\beta_0$, the large-$|z|$ discontinuity satisfies
> $$\rho_F(\mu^2)\big|_{\mu^2\to\infty} \;\sim\; \frac{\text{const}\times\gamma/\beta_0}{\mu^2\,(\ln \mu^2/\Lambda^2)^{1+\gamma/\beta_0}},$$
> i.e. the asymptotic spectral density is *positive* and fixed by the UV. This is the unique part of the QCD cut that is rigorously known and supplies the spectral sum-rule anchors of Section 9.

### 5.3 The non-ideal structure: what full QCD actually shows

The accumulated evidence from lattice QCD, DSE, fRG, and effective massive (Curci–Ferrari / Gribov–Zwanziger) models is that the **gluon propagator in Landau gauge does not admit an ordinary KL representation**. Its non-analytic structure is richer than a single positive cut. The established and well-motivated features are:

- **Positivity violation.** The reconstructed gluon spectral function is *negative* over a substantial range of $\mu^2$ (often: positive at low scales, then negative; in some one-loop massive models negative over the whole range). A negative $\rho$ is impossible for a physical field because $\rho$ would be a sum of squared norms. Its negativity signals that the gluon does not correspond to a positive-norm asymptotic state. [Refs. 1, 2, 3, 5]
- **Complex-conjugate (cc) poles.** Fits to lattice data (Gribov–Stingl form), one-loop massive Yang–Mills, refined Gribov–Zwanziger (RGZ), and Padé analyses repeatedly find a pair of complex-conjugate poles $z = w, \bar w$ with $\mathrm{Im}\,w\neq 0$, on (or just off) the principal sheet. A genuine cc pole pair on the principal sheet *forbids* an ordinary KL representation entirely. [Refs. 1, 2, 5, 7]
- **A residual cut.** Beyond the cc poles, a branch cut (logarithmic, tied to the perturbative tail and to multiparticle thresholds) persists along the timelike axis. Padé reconstructions of lattice data find a pair of cc poles *plus* a branch cut along the negative real $p^2$ axis for the gluon, and a single $p^2=0$ pole plus a cut for the ghost. [Ref. 7]

> **Formalization 2 (Generalized analytic structure of the gluon).** The full Landau-gauge gluon propagator $D(z)$ is, to current best evidence, a meromorphic-plus-cut function of the form
> $$ D(z) = \underbrace{\frac{R}{z - w} + \frac{\bar R}{z - \bar w}}_{\text{cc-pole part}} \;+\; \underbrace{\int_{\mu_{\rm th}^2}^{\infty}\frac{d\mu^2}{2\pi}\,\frac{\rho(\mu^2)}{z + \mu^2}}_{\text{cut part}} \;+\;(\text{subtractions}),$$
> where $R,\bar R$ are (generically complex) residues and $\rho$ is a *real but not sign-definite* spectral density associated with the timelike cut. The presence of the first term is the precise mathematical statement that the gluon is not a particle in a positive-norm Hilbert space.

### 5.4 The physical content of each cut feature — itemized

This is the requested formalization, made explicit feature by feature.

**(a) The timelike logarithmic cut (always present).**
*Content:* gluon/quark dressing by perturbative and semi-perturbative multiparticle radiation; carries asymptotic freedom in its discontinuity. *Sign:* positive at asymptotically large $\mu^2$ (Formalization 1). *Observable proxy:* contributes to the UV tail of any current–current spectral function and hence to the $R$-ratio and to QCD sum-rule moments. This is the most directly "physical" cut and the firmest anchor of the program.

**(b) The infrared portion of the cut (sign-changing).**
*Content:* the nonperturbative reshaping of the dressing — dynamical mass generation, the Schwinger mechanism, screening. The location where $\rho$ crosses zero is a nonperturbative scale (typically a few hundred MeV to $\sim 1$ GeV). *Sign:* changes sign; negative weight here is the spectral image of confinement. *Observable proxy:* the zero-crossing of the position-space (Schwinger) function, Section 7; finite-$T$ screening masses.

**(c) Complex-conjugate poles.**
*Content:* an effective, finite-"lifetime"-like, *non-unitary* excitation. A cc pole pair encodes an oscillatory, exponentially damped contribution to the position-space correlator, $\sim e^{-\mathrm{Re}(\sqrt{w})\,|t|}\cos(\mathrm{Im}(\sqrt{w})\,|t| + \varphi)$, i.e. a "particle" that cannot propagate to asymptotic distances with positive probability. *Physical reading:* the cc poles are the analytic fingerprint of confinement in the constituent's own propagator — the constituent has been removed from the asymptotic spectrum. *Caveat:* whether the cc poles sit exactly on the principal sheet (genuine non-analyticity) or on a secondary sheet (resonance-like) is **disputed** and is gauge-fixing/truncation dependent. [Refs. 1, 2, 7]

**(d) Off-real-axis branch cuts (induced).**
*Content:* a striking, and underappreciated, consequence of (c). If the gluon has cc poles, then *via the ghost loop and the quark loop these poles induce additional branch cuts off the real axis* in the ghost and quark propagators, and these in turn back-react to induce off-axis cuts in the gluon. The naive "single pair of cc poles" picture is therefore not self-consistent: a fully consistent confining solution carries a *cascade* of off-axis cuts. [Ref. 2] *Physical reading:* the constituents' non-analytic structures are mutually entangled by the equations of motion; confinement is a collective analytic phenomenon, not a property of one propagator in isolation.

> **Formalization 3 (Cut propagation / cascade).** In the coupled gluon–ghost(–quark) functional equations, a non-KL feature (cc pole or off-axis cut) in any one propagator propagates, through the self-energy loops, into off-axis cuts in the others. Consequently, the analytic structure of full QCD propagators is a *fixed point of a cut-propagation map*; the existence of a globally consistent confining structure is the statement that this map has a (non-KL) fixed point. The minimal self-consistent confining scenario is **not** "one cc-pole pair," but a coupled set of cc poles plus matched off-axis cuts. [Ref. 2]

**(e) Quark cut and the constituent mass.**
*Content:* the quark self-energy develops a branch cut starting at a scattering threshold $\lambda_{\rm scat}\ge m_{q,\rm pole}$ associated with quark+gluon intermediate states. Below a critical quark–gluon vertex strength the quark retains a KL representation (a real pole plus a positive-then-negative cut); above it (as needed to generate the physical amount of dynamical chiral symmetry breaking through a single classical vertex structure), the quark develops *additional* cc pole pairs located near $m_{q,\rm pole} + p_{\rm glue}^{\rm peak}$. These extra poles, with residues of opposite sign, largely cancel in Euclidean correlators (KL holds to the permille level numerically) but would violate causality if they survived into $S$-matrix elements. [Refs. 7, 10] *Physical reading:* the cut structure of the quark propagator is the analytic encoding of dynamical mass generation and chiral symmetry breaking; the *near-cancellation* of cc-pole residues is why hadron phenomenology built on quasi-causal quark propagators works as well as it does.

### 5.5 Summary of the formalization

The branch cuts of full QCD propagators encode, in order of robustness:

1. **(Rigorous)** Asymptotic freedom and anomalous dimensions, in the universal positive UV tail of the discontinuity.
2. **(Well-established, scheme/gauge dependent)** Nonperturbative mass generation and the onset of confinement, in the sign-changing IR portion of the cut and the zero-crossing scale.
3. **(Strongly evidenced, partly disputed)** Loss of the particle interpretation for elementary colored fields, in positivity violation, complex-conjugate poles, and the cascade of off-axis cuts.
4. **(Phenomenologically actionable)** Final-state interactions, thresholds, and — for gauge-invariant composite operators — directly measurable inclusive rates, in the shape of the (positive) spectral density of color-singlet correlators.

---

<a name="6-generalized-spectral-representations"></a>
## 6. Generalized Spectral Representations: Complex Poles and Off-Axis Cuts

When the ordinary KL representation fails, one does not abandon spectral methods; one *generalizes* them. The key technical device is contour deformation in the complex $z$-plane together with bookkeeping of every singularity enclosed.

### 6.1 The generalized representation with cc poles

Start from Cauchy's theorem for $D(z)$ on a large contour, assuming the arc at infinity is killed by subtractions. Deforming onto the timelike cut and around the cc poles yields
$$
\boxed{\;D(z) = \frac{R}{z-w} + \frac{\bar R}{z-\bar w} + \int_{\mu_{\rm th}^2}^{\infty}\frac{d\mu^2}{2\pi}\,\frac{\rho(\mu^2)}{z+\mu^2}\;}
$$
with $\rho(\mu^2) = \tfrac{1}{\pi}\mathrm{Im}\,D(-\mu^2 - i\epsilon)$ still defined as the jump across the cut. The cc-pole residues are extracted by small contours around $w,\bar w$. This is the representation used to prove reflection-positivity violation analytically in massive Yang–Mills and RGZ models. [Refs. 1, 2, 5]

### 6.2 Finite temperature: separate frequency/momentum dependence

At $T>0$ Lorentz invariance is broken and the propagator depends on the Matsubara frequency $\omega_n$ and $|\mathbf p|$ separately, not just on $p^2$. The generalized representation is re-derived so that the spectral function $\rho_{T,L}(\omega,\mathbf p)$ — for transverse ($T$) and longitudinal ($L$) channels — is the discontinuity in the complex frequency variable, and the cc-pole contribution appears alongside it. This is the natural language for finite-$T$ phenomenology (Section 9), because the *electric* (longitudinal) and *magnetic* (transverse) gluon channels have different analytic structures (different ratios of real to imaginary parts of their pole masses, e.g. as seen in finite-$T$ lattice fits). [Refs. 1, 3, 4]

### 6.3 Counting relations: poles vs. sign of the spectral function

A powerful structural result links the number of cc poles to the sign of the spectral function via the argument principle / Cauchy theorem applied to $\ln D(z)$, under mild assumptions on the asymptotics. Schematically: the number of poles minus zeros enclosed equals a winding integral of the phase of $D$ along the cut, so a globally negative spectral function *requires* an even number of cc poles (e.g. one cc pair gives multiplicity-two structure). This is why "negative $\rho$ everywhere" and "a pair of cc poles" appear together in the massive Yang–Mills analysis — they are two faces of the same counting relation. [Ref. 5] These relations turn qualitative confinement statements into *quantitative constraints* on the allowed analytic structure.

### 6.4 Strong coupling and proliferation of cuts

In matter–gauge theories tuned to an infrared Banks–Zaks fixed point, one can compute propagators analytically across the whole complex plane. At weak coupling a genuine KL representation is achieved for gluon, quark, and ghost (for suitable gauge parameter). At strong coupling, a **proliferation of complex-conjugate branch cuts** renders any causal (KL) representation impossible. Scaling exponents determine the presence/absence of non-analyticities. [Ref. 5] This provides a controlled theoretical laboratory in which the transition "KL $\to$ non-KL" is dialed by coupling — the cleanest demonstration that branch-cut structure is dynamical content, not an artifact.

---

<a name="7-reflection-positivity"></a>
## 7. Reflection Positivity, the Schwinger Function, and Confinement

### 7.1 The Schwinger function as a position-space probe of the cut

Define the (zero-spatial-momentum) **Schwinger function** as the temporal Fourier transform of the Euclidean propagator,
$$
\mathcal{C}(t) = \int_{-\infty}^{\infty}\frac{dp_4}{2\pi}\,e^{ip_4 t}\,D(p_4^2) = \int_0^\infty \frac{d\mu^2}{2\pi}\,\rho(\mu^2)\,\frac{e^{-\mu|t|}}{2\mu}.
$$
The second equality uses the KL form. If $\rho \ge 0$ (physical field), then $\mathcal{C}(t) \ge 0$ for all $t$ — this is **reflection (Osterwalder–Schrader) positivity**, the Euclidean expression of a positive-norm Hilbert space.

> **Formalization 4 (Positivity-violation theorem, operational form).** If the Schwinger function $\mathcal{C}(t)$ becomes negative for some $t$, the spectral function $\rho$ cannot be everywhere non-negative, and the field has no interpretation as a positive-norm asymptotic particle. The **zero-crossing time** $t_0$ (where $\mathcal{C}(t_0)=0$) is a gauge-fixed but well-defined nonperturbative length scale.

### 7.2 The QCD result

Both lattice QCD and DSE/fRG find that the Landau-gauge **gluon Schwinger function has a zero crossing** at $t_0 \approx 1\ \mathrm{fm}\ (\approx 5\ \mathrm{GeV}^{-1})$ and is negative beyond it — robustly, across $SU(2)$ and $SU(3)$, quenched and unquenched, and in RGZ and massive-model fits. [Refs. 2-direct, 6, 8 in the gluon search; e.g. arXiv hep-ph/0309078, RGZ one-loop, position-space lattice studies] This is the cleanest, most model-independent evidence that the gluon is not a physical particle: its propagator cut carries *negative spectral weight*. The analytic proof in massive Yang–Mills and RGZ proceeds exactly by splitting $\mathcal{C}(t)$ into a cc-pole contribution and a cut contribution and showing the sum is forced negative. [Refs. 1, 5]

> **Physical content of the cut, restated via $\mathcal{C}(t)$.** The branch-cut discontinuity $\rho(\mu^2)$ is the *weight function* that, when Laplace-transformed by $e^{-\mu|t|}$, builds the position-space correlator. Confinement is the statement that this weight is signed in such a way that the correlator changes sign — i.e. the constituent cannot be detected at large Euclidean separation with positive probability. The branch cut is thus not a blemish on the propagator; it is the carrier of the confinement signal.

### 7.3 The ghost: a foil

The ghost propagator is expected to *retain* a KL representation (it is causal in the relevant sense): a massless pole at $p^2=0$ with residue $1/Z_c$ plus a positive logarithmic scattering tail. Recent reconstructions and direct calculations show no violation. [Ref. 2] The contrast — gluon non-KL, ghost KL — is itself physical: the ghost's role is to cancel unphysical gluon polarizations, and its clean analytic structure is consistent with it never appearing as an asymptotic colored state while also never acquiring the cc-pole pathology (its off-axis cuts, when present, are *induced* by the gluon's cc poles, Formalization 3).

---

<a name="8-anomalous-thresholds"></a>
## 8. Anomalous Thresholds and Dressed Vertices

Off-shell physics is not confined to two-point functions. Dressed (off-shell) three-point vertices carry their own non-analytic structure, and a particular class of singularities — **anomalous thresholds** (a.k.a. triangle/Landau singularities) — encodes *compositeness* and *binding* information that is invisible to the pole.

### 8.1 Normal vs. anomalous thresholds

A vertex/triangle function $F(q^2)$ generically has a **normal threshold** at $q^2 = (m_1+m_2)^2$ from putting an internal pair on shell — the standard unitarity cut. For suitable external masses, however, a branch point can **migrate from the unphysical sheet onto the physical sheet through the normal cut**, producing an **anomalous threshold** at $q^2 = t_0 < (m_1+m_2)^2$. [Refs. triangle-diagram analyses 2, 3 in the anomalous-threshold search]

> **Formalization 5 (Compositeness from anomalous thresholds).** For a bound state of mass $M$ formed from constituents of mass $m$, the anomalous threshold appears (in the equal-mass case) for all $M^2 > 2m^2$, i.e. *below* the normal unitary threshold $M^2 = 4m^2$. For a weakly bound state, $M = 2m - \epsilon_B$ with $\epsilon_B \ll m$, the *location* of the anomalous threshold in $q^2$ is controlled by — and hence measures — the (large) **radius** of the bound state. The anomalous cut's discontinuity therefore encodes whether a hadron is a compact $q\bar q$/$qqq$ object or a spatially extended molecule.

This is a textbook-grade example of the central thesis: the anomalous threshold is *pure off-shell, pure cut* content; it carries information (compositeness, hadronic size) that no on-shell pole position can supply. It is directly relevant to the structure of exotic hadrons (e.g. near-threshold $XYZ$/pentaquark states), where the question "molecule or compact state?" is precisely a question about the anomalous-threshold/branch-point content of the relevant correlators and form factors.

### 8.2 Soft-gluon limit and the first singularity of the quark

The location of the quark propagator's first singularity is controlled by the behavior of the combined gluon-propagator$\times$quark-gluon-vertex in the soft-gluon limit. If that product diverges (as in many vertex *models*), the first singularity is pushed into the complex plane (cc poles); in full QCD the product stays finite (consistent with the Schwinger or quartet confinement mechanisms), keeping the dominant singularity on or near the real timelike axis. [Refs. 7, 10] The off-shell vertex structure thus directly sculpts the quark's cut — another instance of the off-shell vertex being a carrier of physical (here, confinement-mechanism) content.

---

<a name="9-the-unmined-resource"></a>
## 9. The Unmined Phenomenological Resource — A Program

We now formalize the claim that the full spectral decomposition of interacting propagators — *not just poles* — is a largely unmined phenomenological resource, by laying out concrete channels through which propagator cut structure feeds measurable physics.

### 9.1 Transport coefficients (zero-frequency spectral weight)

Kubo formulas express transport coefficients as the zero-frequency slope of a spectral function:
$$
\eta = \pi \lim_{\omega\to 0}\frac{\rho_{\eta}(\omega,\mathbf 0)}{\omega}, \qquad
\sigma_{\rm el} = \frac{1}{6}\lim_{\omega\to 0}\frac{\rho_{JJ}(\omega,\mathbf 0)}{\omega}, \quad\text{etc.}
$$
where $\rho_\eta$ is the spectral function of the energy–momentum tensor (shear viscosity), $\rho_{JJ}$ that of the electromagnetic current (conductivity). The transport peak is a *low-frequency feature of the cut*, completely invisible to a poles-only reading. Functional and lattice approaches now compute these from full propagators/vertices: gluon spectral functions feed a closed loop equation for the energy-momentum-tensor spectral function, yielding $\eta/s$ with a minimum near $1.25\,T_c$ around $0.1$; quark-meson fRG with analytic continuation yields $\eta/s$ near the critical endpoint. [Refs. transport search 1, 3, 4]

> **Resource (i).** The infrared shape of the gluon and quark spectral functions — the part of the cut nearest $\omega=0$ — *is* the transport sector of the quark–gluon plasma. Improving these spectral reconstructions directly sharpens predictions for $\eta/s$, electrical conductivity, and heavy-quark diffusion measured in heavy-ion collisions.

### 9.2 Electromagnetic emissivities (dileptons and photons)

Thermal dilepton and photon production rates are *literally* spectral functions of the in-medium electromagnetic current:
$$
\frac{dN_{\ell^+\ell^-}}{d^4x\,d^4q} \;\propto\; \frac{1}{q^2}\,\frac{\rho_{JJ}(q_0,\mathbf q)}{e^{q_0/T}-1}.
$$
The vector-meson ($\rho,\omega,\phi$) spectral functions — their in-medium broadening and the melting of their poles into the continuum — are the theory input behind the dilepton excess measured at SPS/RHIC/LHC. This is the spectral-function-as-observable paradigm at its most direct. [Refs. transport search 1, 3]

> **Resource (ii).** The medium modification of hadronic spectral functions — pole shifts, width growth, continuum reshaping — is an experimentally accessible window on chiral symmetry restoration and deconfinement. The cut, not the vacuum pole, is what the dilepton spectrum measures.

### 9.3 QCD spectral sum rules

SVZ-type sum rules equate weighted integrals of a hadronic spectral function (the cut) to an operator-product expansion (OPE) controlled by condensates:
$$
\int_0^\infty ds\,W(s)\,\rho_H(s) = \sum_n C_n\,\langle \mathcal{O}_n\rangle.
$$
The left side is purely cut content; the right side connects it to the QCD vacuum (gluon condensate $\langle G^2\rangle$, quark condensate $\langle\bar q q\rangle$, etc.). Sum rules are the most mature mining of propagator/correlator cuts and remain a frontier for excited and exotic states. The universal positive UV tail (Formalization 1) and the spectral sum rules of Section 3.3 are what make these constraints predictive.

> **Resource (iii).** Every QCD sum rule is an identity between a measured spectral function (cut) and vacuum condensates. Systematic use of the *full* spectral shape (continuum models beyond the "pole + step-function continuum" ansatz) is an open frontier.

### 9.4 Hadron structure, form factors, and compositeness

Anomalous thresholds (Section 8) in electromagnetic and transition form factors encode hadronic radii and compositeness. Dispersive analyses of form factors — writing $F(q^2)$ as an integral over its cut — are the rigorous, model-independent route to charge radii (e.g. the proton radius via the spectral function of the isovector form factor) and to discriminating molecular vs. compact exotics.

> **Resource (iv).** The branch-cut (spectral) representation of form factors converts off-shell vertex structure into measurable radii and compositeness statements. Anomalous thresholds are an underused diagnostic for near-threshold exotic hadrons.

### 9.5 Bound-state equations with realistic analytic input

Bethe–Salpeter and Faddeev equations for mesons and baryons require quark and gluon propagators as input *in the complex momentum plane*. The cc poles and cuts of these propagators set the domain of validity of standard solution methods and can, if mishandled, corrupt extracted masses and decay constants. Conversely, *correct* incorporation of the analytic structure (cc-pole residue cancellations, Formalization in 5.4(e)) is what allows light-hadron observables to be computed reliably despite the elementary fields being confined. [Refs. 7, 10]

> **Resource (v).** Faithful analytic continuation of propagators — including their non-KL features — is a prerequisite for next-generation precision in functional hadron spectroscopy. The cut structure is not a nuisance to be regulated away; it is the boundary condition of the bound-state problem.

### 9.6 Finite-$T$ thermodynamics and the equation of state

The electric/magnetic split of the gluon spectral function (Section 6.2) controls Debye screening, the Polyakov loop, and the approach to the ideal-gas limit. The differing analytic structures of $D_L$ and $D_T$ at $T>0$ (different cc-pole/cut content) are a direct theory input to the equation of state and to screening-mass spectroscopy on the lattice. [Refs. 1, 3, 4]

---

<a name="10-the-inverse-problem"></a>
## 10. The Inverse Problem: Obstructions and Methodology

Harvesting the resource requires solving an **ill-posed inverse problem**: reconstructing the real-frequency spectral function $\rho(\omega)$ from data known only at discrete Euclidean (spacelike/imaginary-time) points. This is the central technical obstruction and deserves an explicit accounting.

### 10.1 Why it is hard

The KL kernel $K(\tau,\omega) = e^{-\omega\tau}$ (or $1/(p^2+\mu^2)$ in momentum space) is exponentially smoothing: vastly different $\rho(\omega)$ map to nearly identical Euclidean data within error bars. The reconstruction
$$
G(\tau) = \int d\omega\,K(\tau,\omega)\,\rho(\omega)
$$
must be inverted from noisy, finite data — an exponentially ill-conditioned problem. There is no unique solution without additional input (priors, regularization, or analyticity assumptions).

### 10.2 Methods

- **Maximum Entropy Method (MEM).** Bayesian reconstruction with an entropic prior; standard for lattice spectral functions, including gluon spectral functions and transport. Tends to oversmooth sharp features. [Ref. 4]
- **Backus–Gilbert / Bailas–Hansen–Lupo.** Resolution-controlled linear methods giving smeared spectral functions with rigorous resolution kernels; well-suited to transport. [Ref. transport 3]
- **Sparse modeling (SpM) / compressed sensing.** Exploits sparsity in a singular-value basis; reduces bias, can resolve band edges; applied to energy–momentum-tensor correlators for $\eta$. [Ref. transport 2]
- **Padé / rational approximation.** Directly models poles and cuts; Padé sequences on lattice gluon/ghost data recover cc poles and a real-axis cut. Sensitive to data noise but transparent about analytic structure. [Ref. 7]
- **Tikhonov regularization + Morozov discrepancy.** Used to extract KL densities from gluon/ghost data with controlled regularization, including careful handling of the ghost IR singularity. [Ref. 7]
- **Functional analytic continuation.** fRG/DSE flows continued at the level of the flow equations (rather than reconstructed post hoc), giving direct real-time spectral functions. [Refs. transport 1; gluon/ghost spectral DSE 2]

### 10.3 Methodological recommendations

1. **Build in known analytic structure.** Impose the universal positive UV tail (Formalization 1), known thresholds, and sum rules (Section 3.3) as hard constraints. This drastically reduces the reconstruction's null space.
2. **Allow non-KL structure explicitly.** Do not assume a single positive cut. Use representations that admit cc poles and off-axis cuts (Section 6), and *test* for them (e.g. via the Schwinger-function zero crossing, Section 7) rather than assuming them away.
3. **Respect cut propagation.** In coupled-system reconstructions, enforce self-consistency of the cut-propagation map (Formalization 3): a cc pole assumed in the gluon must be matched by induced off-axis cuts in ghost/quark.
4. **Cross-validate observables.** Use independent observables that probe the same spectral region (e.g. transport from both $\eta$-correlators and conductivity; radii from both dispersive and lattice form factors) to break reconstruction degeneracies.

---

<a name="11-open-problems"></a>
## 11. Conjectures, Open Problems, and Falsifiable Predictions

1. **Existence of a consistent confining analytic structure.** Is there a globally self-consistent, finite set of cc poles and off-axis cuts that solves the coupled gluon–ghost–quark functional equations exactly (the fixed point of Formalization 3)? Current evidence suggests the minimal "single cc-pole pair" is inconsistent and a cascade is required; the full structure is not yet known. [Ref. 2]
2. **Principal- vs. secondary-sheet cc poles.** Are the gluon cc poles genuinely on the principal sheet (true non-analyticity, hard breakdown of KL) or on a secondary sheet (resonance-like)? This is gauge-fixing/truncation dependent and unresolved. [Refs. 1, 7]
3. **Gauge dependence of the analytic structure.** How much of the cc-pole/off-axis-cut structure is physical vs. an artifact of Landau gauge? Nielsen identities constrain the *pole position of physical states* but not obviously the full elementary-propagator structure. A gauge-invariant formulation (e.g. via gauge-invariant composite operators, or the gauge-scalar/Fradkin–Shenker viewpoint) is needed. [Ref. 1]
4. **Quark cc poles and causality.** The extra quark cc poles required for full chiral symmetry breaking via a single classical vertex structure violate causality if they survive in $S$-matrix elements; full QCD presumably avoids them through the other tensor structures of the quark–gluon vertex. Demonstrating this in full QCD is open. [Refs. 7, 10]

**Falsifiable predictions implied by the framework:**
- The gluon Schwinger function must have a zero crossing near $\sim 1$ fm in *any* correct gauge-fixed computation/measurement-proxy; its disappearance would refute the negative-spectral-weight picture. *(Confirmed so far across lattice, DSE, fRG, RGZ.)* [Refs. 6, 8, RGZ]
- Transport coefficients reconstructed from full gluon/quark spectral functions must agree with those extracted from heavy-ion phenomenology within the strongly coupled window; a sustained discrepancy would indict the spectral input.
- Near-threshold exotic hadrons identified as molecules must exhibit the predicted anomalous-threshold (large-radius) signature in their transition form factors. [Refs. 2, 3 anomalous]

---

<a name="12-conclusions"></a>
## 12. Conclusions

Off-shell structure in QFT is not a defect to be eliminated; for the two-point function it is a carrier of physical content with a precise mathematical home — the Källén–Lehmann representation and its generalizations. We have formalized that content and, in particular, the physical meaning of the **branch cuts in full QCD propagators**:

- The **discontinuity across the cut is the spectral function**: a positive probability density for physical (gauge-invariant, color-singlet) channels — directly the $R$-ratio, dilepton rates, and transport spectral weight — and a *signed, sum-rule-constrained* density for the confined elementary fields.
- The **universal positive UV tail** of the cut encodes asymptotic freedom; the **sign-changing IR portion** encodes nonperturbative mass generation; the **complex-conjugate poles, positivity violation, and induced off-axis cuts** encode the loss of a particle interpretation — i.e. confinement — for gluon and quark.
- Confinement is an *analytic* statement: the gluon Schwinger function changes sign (zero crossing near 1 fm), provably so in massive Yang–Mills and RGZ models via the cc-pole-plus-cut decomposition.
- **Anomalous thresholds** of dressed vertices encode compositeness and hadronic radii — pure off-shell, pure cut information with no on-shell pole counterpart.

The **unmined phenomenological resource** is the systematic use of the *full* spectral decomposition — beyond poles — across transport, electromagnetic emissivities, sum rules, hadron structure, bound-state equations, and finite-$T$ thermodynamics. The principal obstruction is the ill-posed inverse problem of analytic continuation; the principal opportunity is that built-in analytic-structure constraints (UV tail, thresholds, sum rules, cut-propagation self-consistency) can tame it. The amplitudes program taught us to compute the $S$-matrix without off-shell scaffolding. The complementary lesson of this white paper is that the off-shell propagator's cut structure is not scaffolding at all — it is, for QCD, where confinement, mass generation, and the thermodynamics of the quark–gluon plasma are written.

---

<a name="13-notation"></a>
## 13. Notation and Conventions

| Symbol | Meaning |
|---|---|
| $G(p), D(p), S(p)$ | Full scalar, gluon, quark propagators |
| $\Sigma, \Pi$ | Self-energy / polarization |
| $\rho(\mu^2)$ | Spectral function (cut discontinuity) |
| $Z$ | Field-strength renormalization / pole residue |
| $z = p^2 \in \mathbb{C}$ | Complex momentum-squared variable |
| $w, \bar w$ | Complex-conjugate pole locations |
| $\mathcal{C}(t)$ | Schwinger function (position space) |
| $t_0$ | Schwinger-function zero-crossing scale |
| $Z(p^2), G(p^2)$ | Gluon, ghost dressing functions |
| $A, B, M$ | Quark vector/scalar dressing and mass function |
| $T,L$ | Transverse / longitudinal (vector) channels |
| KL, DSE, fRG, RGZ | Källén–Lehmann; Dyson–Schwinger; functional RG; refined Gribov–Zwanziger |
| cc | complex-conjugate |

*Euclidean conventions used for lattice/functional data; spacelike $p^2\ge 0$, timelike cut at $z\le -\mu_{\rm th}^2$. Sign and factor conventions vary across the literature; the structural statements are convention-independent.*

---

<a name="14-references"></a>
## 14. Annotated References

Representative, load-bearing sources for the technical claims above (selection, not exhaustive):

1. **One-loop analytic structure of the deep-infrared Landau-gauge gluon propagator**, arXiv:2509.23889 / Phys. Rev. D (2025). Generalized spectral representation with cc poles plus cut; physical reading of poles (deltas), peaks (secondary-sheet poles), and cuts; finite-$T$ extension. https://arxiv.org/html/2509.23889
2. **On the complex structure of Yang–Mills theory**, arXiv:2202.09333 (2022). Cut-propagation cascade: gluon cc poles induce off-axis cuts in the ghost and back into the gluon; the single-cc-pair scenario is inconsistent; ghost retains KL. https://arxiv.org/html/2202.09333
3. **Reflection positivity and complex analysis of the Yang–Mills theory (massive model)**, Eur. Phys. J. C 80 (2020) 87, arXiv:1912.06261. Analytic proof of reflection-positivity violation from cc poles + negative spectral function; Gribov–Stingl form explained. https://link.springer.com/article/10.1140/epjc/s10052-020-7632-4
4. **Spectral functions of gauge theories with Banks–Zaks fixed points**, Phys. Rev. D 107 (2023) 025011. KL achieved at weak coupling; proliferation of cc branch cuts at strong coupling; scaling-exponent criteria for non-analyticity. https://link.aps.org/doi/10.1103/PhysRevD.107.025011
5. **The causal structure of the quark propagator**, arXiv:2412.12033 / Eur. Phys. J. C (2025). Critical vertex strength for KL; additional quark cc poles from chiral symmetry breaking; near-cancellation of residues; soft-gluon-limit control of the first singularity. https://arxiv.org/html/2412.12033v1
6. **Infrared gluon propagator in the Refined Gribov–Zwanziger scenario at one loop**, arXiv:2405.07779 (2024). One-loop RGZ gluon: complex poles, positivity violation, Schwinger-function zero crossing $\sim 5\ \mathrm{GeV}^{-1}$, fits to $SU(2)/SU(3)$ lattice. https://arxiv.org/html/2405.07779
7. **Källén–Lehmann spectroscopy for (un)physical degrees of freedom** and **Padé/Tikhonov reconstructions of lattice gluon/ghost propagators**. cc poles + real-axis cut for the gluon; massless pole + cut for the ghost; ill-posed inversion and regularization. (e.g. SciSpace PDF; ResearchGate 352386712.)
8. **Gluon Schwinger function / positivity from DSE and lattice**, e.g. arXiv:hep-ph/0309078 and position-space lattice studies (PoS, EPJ Web Conf.). Zero crossing near 1 fm; dominant quark singularity near $350$–$500$ MeV.
9. **Gluon spectral functions and transport coefficients in Yang–Mills theory**, arXiv:1308.4960 (2013). MEM gluon spectral functions; closed loop equation for the EMT spectral function; $\eta/s$ minimum $\approx 0.115$ near $1.25\,T_c$. https://arxiv.org/abs/1308.4960
10. **fRG real-time spectral functions, dileptons, and transport at finite $T$** (ECT* program and related). Analytic continuation at the level of flow equations; mesonic spectral functions and $\eta/s$ near the critical endpoint. https://www.ectstar.eu/research/hadrons-and-qcd-matter/
11. **Analytic properties of triangle Feynman diagrams / anomalous thresholds**, MDPI Physics 3 (2020) 9 and related. Migration of branch points onto the physical sheet; anomalous threshold below the normal threshold; binding-radius interpretation. https://www.mdpi.com/2571-712X/3/1/9
12. Standard texts for the KL representation and resonance/second-sheet structure: Weinberg, *The Quantum Theory of Fields* Vol. I; Peskin & Schroeder, Ch. 7; Serone, *Notes on QFT* (resonances on the second sheet). https://userswww.pd.infn.it/~feruglio/Serone.pdf

---

*End of white paper. Prepared as a self-contained conceptual and technical formalization; structural claims are convention-independent, while quantitative gauge-fixed statements (cc-pole positions, zero-crossing scales) carry the scheme/gauge caveats noted in Sections 5, 7, and 11.*
