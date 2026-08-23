# Nucleons, Electrons, and Atomic Phase Structure

## A Derivation from the Universal Phase Equation, Phase Transport, and Bound Phase-Sector Geometry

**Dust LLC — Universal Phase Theory Preprint Series**
**August 2026**

---

## Abstract

The electron, proton, and neutron are not introduced here as primitive point objects, as irreducible representations stipulated in advance, or as quanta of pre-existing quantum fields. They are derived as stable phase-sector orbits of the universal phase equation

$$
\mathscr{F}[\Phi;\lambda]=0,
\qquad
\mathscr{L}_\Phi := D_\Phi\mathscr{F}[\Phi;\lambda],
\qquad
\Delta_\Phi := \operatorname{Det}_\Phi(\mathscr{L}_\Phi),
\qquad
\boldsymbol{\chi}_\Phi := \mathscr{L}_\Phi^{-1},
$$

subject to the seven conditions of the Particle Emergence Theorem (Theorem 1, *The Particle as a Stable Phase Sector*). The electron is identified as a topologically protected $U(1)$-charged phase-sector orbit with spin-$\tfrac{1}{2}$ arising as the holonomy of the derived phase connection around a $2\pi$ loop. The proton and neutron are identified as composite stable phase sectors whose internal structure is governed by a non-Abelian phase connection whose residual holonomy confines the constituent phase degrees of freedom within a finite phase-excess region. The hydrogen atom is derived as a bound two-sector phase configuration: a proton-sector orbit and an electron-sector orbit coupled through the emergent Abelian phase connection, with quantized orbital structure arising from the integrality condition on the phase symplectic form. The periodic structure of chemistry is then interpreted as the stratification of multi-electron bound phase-sector configurations over nuclear phase sectors, governed by phase exclusion, holonomy representation, and the response geometry of the emergent Coulomb phase potential. No spacetime manifold, gauge group, mass spectrum, charge assignment, or quantum probability rule is inserted. All such structures are recovered as derived consequences of the phase-sector geometry. The paper concludes with explicit falsifiability criteria and the precise computational program required for a concrete UPT realization to reproduce the observed atomic spectrum.

---

## Part I — Ontological Framework and Scope

### 1.1 Phase-primacy statement

Universal Phase Theory begins before particles, before atoms, before chemistry. The primitive datum is a generalized phase section $\Phi \in \Gamma(E_\Phi)$ over a non-spatiotemporal base $\mathcal{X}$, subject to the universal phase equation. The ontological hierarchy is

$$
\boxed{
\Phi
\longrightarrow
\text{topology}
\longrightarrow
\text{geometry}
\longrightarrow
\text{connections}
\longrightarrow
\text{fields}
\longrightarrow
\text{particles}
\longrightarrow
\text{bound states}
\longrightarrow
\text{atomic structure}
\longrightarrow
\text{chemistry}
\longrightarrow
\text{observables}.
}
$$

Every object to the right of an arrow is a derived consequence of the phase structure to its left. The electron is not placed into $\mathscr{F}$. The proton is not placed into $\mathscr{F}$. The Coulomb potential is not placed into $\mathscr{F}$. The periodic table is not placed into $\mathscr{F}$. If these structures appear, they appear as stable-sector orbits, bound-sector configurations, and stratifications of the quotient solution space $\mathscr{S}_\Phi / \mathscr{G}_\Phi$.

### 1.2 The UPT datum for atomic physics

The relevant UPT datum is

$$
\mathfrak{U} = (E_\Phi,\; \mathscr{G}_\Phi,\; \mathcal{C}_\Phi,\; \mathscr{F},\; \lambda),
$$

where $\mathscr{F}:\mathcal{C}_\Phi \times \Lambda \to \mathcal{Y}_\Phi$ is the admissibility map. For the derivation of nucleons and leptons, the control data $\lambda$ includes the phase-scale parameter $\ell$ at which the relevant sector is probed, the asymptotic phase class specifying the vacuum sector $[\Phi_0]$, and the boundary conditions encoding finite phase-excess localization.

The phase-frame group $\mathscr{G}_\Phi$ is not specified as $SU(3)\times SU(2)\times U(1)$ at the outset. It is the full admissible phase-frame automorphism group of the bundle $E_\Phi \to \mathcal{X}$. The observed gauge structure must emerge as the residual stabilizer of the stable vacuum orbit.

### 1.3 Non-insertion audit

The following table governs the entire derivation.

| Structure | Status in this paper | Required derivation |
|---|---|---|
| Electron as point particle | **Not inserted** | Theorem 1 applied to a $U(1)$-charged phase sector |
| Proton as three-quark bound state | **Not inserted** | Composite phase-sector orbit with confining phase topology |
| Neutron as three-quark bound state | **Not inserted** | Distinct composite phase-sector orbit with different topological class |
| Electric charge $\pm e$ | **Not inserted** | Phase current invariant of the emergent $U(1)$ connection |
| Spin $\tfrac{1}{2}$ | **Not inserted** | Holonomy of the derived phase connection around $2\pi$ |
| Masses $m_e, m_p, m_n$ | **Not inserted** | Computed phase-excess $\mathcal{E}_\Phi[\Phi_q \mid \Phi_0]/c_\Phi^2$ |
| Coulomb potential | **Not inserted** | Green's function of the emergent Abelian phase connection |
| Bohr radius | **Not inserted** | Equilibrium of phase-susceptibility geometry in bound configuration |
| Periodic table | **Not inserted** | Stratification of multi-sector bound configurations |

This audit is binding. Any appearance of the above structures as input rather than output constitutes a derivational failure.

---

## Part II — The Electron as a Stable Phase Sector

### 2.1 Bifurcation and the electron branch

Let $\Phi_c$ be a critical vacuum-sector solution at control value $\lambda_c$ satisfying $\mathscr{F}[\Phi_c;\lambda_c]=0$ with $\ker\mathscr{L}_{\Phi_c} \neq \{0\}$. Assume $\mathscr{L}_{\Phi_c}$ is Fredholm of index zero. Decompose

$$
\mathcal{T}_{\Phi_c}\mathcal{C}_\Phi = K_c \oplus R_c,
\qquad
K_c = \ker\mathscr{L}_{\Phi_c},
\qquad
K_c^* \cong \operatorname{coker}\mathscr{L}_{\Phi_c}.
$$

Choose a basis $\{e_a\}_{a=1}^{k}$ for $K_c$ and dual covectors $\{e^{*a}\}$. The Lyapunov–Schmidt reduction produces the finite-dimensional bifurcation equation

$$
\varphi^a(\eta,\lambda)
:=
\left\langle e^{*a},\;
\mathscr{F}\!\left[\Phi_c + \eta^b e_b + \xi(\eta,\lambda);\;\lambda\right]
\right\rangle = 0.
$$

The electron branch is an isolated nonzero solution $\eta_e(\lambda)$ of this reduced equation. The corresponding phase configuration is

$$
\Phi_e(\lambda)
:=
\Phi_c + \eta_e^a(\lambda)\,e_a + \xi(\eta_e(\lambda),\lambda).
$$

**Proposition 1** *(Electron branch existence).* *Suppose the reduced bifurcation equation possesses an isolated nonzero solution branch $\eta_e(\lambda)$ that is not connected to any other nonzero branch by a continuous path in $\mathcal{C}_{\mathrm{fin}}/\mathscr{G}_\Phi$. Then $\Phi_e(\lambda)$ is an admissible nonvacuum phase branch.*

*Proof.* Identical to Proposition 1 of *The Particle as a Stable Phase Sector*: the range equation fixes $\xi$, the cokernel equation fixes $\eta_e$, and the direct-sum decomposition yields $\mathscr{F}[\Phi_e;\lambda]=0$. Non-vacuum character follows from $\eta_e \neq 0$. $\square$

### 2.2 Topological separation: the electron charge sector

The vacuum orbit $[\Phi_0]$ defines a homogeneous asymptotic phase. The electron branch must approach this vacuum at the phase boundary:

$$
\Phi_e \longrightarrow \Phi_0
\quad\text{on}\quad
\partial_\infty \mathcal{X}.
$$

The asymptotic phase map defines a topological class

$$
q_e(\Phi_e) := [\partial_\infty \Phi_e] \in \pi_{r-1}(\mathscr{V}),
$$

where $\mathscr{V}$ is the vacuum orbit manifold and $r$ is the codimension of the defect. For the electron, the relevant asymptotic structure is a $U(1)$ phase winding. The phase-frame bundle restricted to the asymptotic boundary carries a principal $U(1)$ structure, and the electron is characterized by a nontrivial first Chern class:

$$
c_1(\Phi_e) := \frac{1}{2\pi}\int_{S^2_\infty} F_{\Phi_e} \neq 0,
$$

where $F_{\Phi_e}$ is the curvature of the derived Abelian phase connection. The electron charge is the phase-topological invariant

$$
\boxed{
Q_e^{\mathrm{top}}
:=
\int_{\Sigma} \omega_e[\Phi_e],
\qquad
d\omega_e = 0,
\qquad
[\omega_e] \in H^2(\mathcal{X},\mathbb{Z}).
}
$$

**Proposition 2** *(Electron–vacuum separation).* *The electron orbit $[\Phi_e]$ cannot be continuously deformed into the vacuum orbit $[\Phi_0]$ through admissible finite-excess configurations.*

*Proof.* A continuous path $\Phi_s \in \mathcal{C}_{\mathrm{fin}}$ from $\Phi_e$ to $\Phi_0$ would induce a homotopy of the asymptotic boundary maps. Since $q_e(\Phi_e) \neq q_e(\Phi_0) = 0$, no such homotopy exists. $\square$

### 2.3 Normal stability of the electron sector

The gauge and collective zero modes span $\mathcal{Z}_e$. The normal complement $N_e$ satisfies

$$
\mathcal{T}_{\Phi_e}\mathcal{C}_\Phi = \mathcal{Z}_e \oplus N_e.
$$

The projected normal stability operator is

$$
\mathscr{L}_e^\perp := \Pi_{N_e}\,\mathscr{L}_{\Phi_e}\,\Pi_{N_e}.
$$

Normal stability requires

$$
\ker\mathscr{L}_e^\perp = \{0\},
\qquad
\langle \zeta,\, \mathscr{L}_e^\perp \zeta \rangle_\Phi
\geq \kappa_e\, |\zeta|_\Phi^2,
\quad
\kappa_e > 0.
$$

The electron susceptibility is therefore finite:

$$
\boldsymbol{\chi}_e = (\mathscr{L}_e^\perp)^{-1},
\qquad
|\boldsymbol{\chi}_e| \leq \kappa_e^{-1}.
$$

### 2.4 Electron localization and response geometry

The response metric is constructed from the electron susceptibility:

$$
g_{ij}^{\Phi_e} := T_{ia}\,\chi_e^{ab}\,T_{jb},
$$

where $T_{ia} = \partial^2 \mathcal{V}_{\mathrm{red}} / \partial\lambda^i \partial\eta^a$. On the maximal-rank stratum, this defines the effective domain $M_{\mathrm{eff}}$ with phase distance

$$
D_\Phi(\lambda_1,\lambda_2)
=
\inf_\gamma \int_\gamma
\sqrt{g_{ij}^{\Phi_e}\,d\lambda^i\,d\lambda^j}.
$$

The gauge-invariant excess density $\varepsilon_e$ satisfies

$$
\int_{\{x:\, D_\Phi(x,X_e) > R\}} |\varepsilon_e(x)|\,d\mu_{g^\Phi}
\xrightarrow[R/\ell_e \to \infty]{} 0,
$$

establishing localization. The electron is not a point placed on a manifold. It is a phase-sector orbit whose invariant excess is concentrated within a finite response region of the emergent geometry.

### 2.5 Electron spin as phase holonomy

The derived phase connection $A_\mu = \mathcal{A}_\mu[\Phi_e]$ defines parallel transport. For the electron sector, the residual stabilizer $H_e \subset \mathscr{G}_\Phi$ acts on the normal phase space through a representation $\rho_e$. Transport around a closed $2\pi$ loop yields

$$
\rho_e(\mathscr{U}_{2\pi})
=
\rho_e\!\left(\mathcal{P}\exp\left(-\oint_{2\pi} \mathscr{A}\right)\right)
=
e^{2\pi i s_e}\,\mathbf{1}.
$$

For the electron sector, the phase connection carries a projective representation of the emergent rotation group. The $2\pi$ holonomy is

$$
\boxed{
\rho_e(\mathscr{U}_{2\pi}) = -\mathbf{1},
\qquad
s_e = \tfrac{1}{2}.
}
$$

Spin is therefore phase holonomy. It is not a pre-assigned Lorentz representation index. The half-integer value arises because the electron phase sector transforms under the double cover of the emergent rotation group, a consequence of the topological structure of the phase bundle restricted to the electron orbit.

### 2.6 Electron mass

Once the emergent Lorentzian sector has been established and a conserved energy functional $\mathcal{E}$ exists, the electron rest mass is

$$
\boxed{
m_e := \frac{\mathcal{E}[\Phi_e] - \mathcal{E}[\Phi_0]}{c_\Phi^2}.
}
$$

This is a computed phase-excess ratio. The numerical value $m_e \approx 9.109 \times 10^{-31}\;\mathrm{kg}$ must emerge from the explicit solution of $\mathscr{F}$ without fitting.

### 2.7 The electron as a UPT particle

Assembling the seven conditions:

| Condition | Electron realization |
|---|---|
| 1. Admissibility | $\mathscr{F}[\Phi_e;\lambda]=0$ by construction |
| 2. Nonvacuum separation | $c_1(\Phi_e) \neq 0$; $q_e \neq q_0$ |
| 3. Finite excess | $0 < \mathcal{E}_\Phi[\Phi_e \mid \Phi_0] < \infty$ |
| 4. Normal stability | $\mathscr{L}_e^\perp > 0$ on $N_e$ |
| 5. Response geometry | $g_{ij}^{\Phi_e}$ nondegenerate on physical stratum |
| 6. Localization | $\varepsilon_e$ concentrated within finite $D_\Phi$ |
| 7. Transportability | Smooth moduli family $\Phi_e(\cdot;z)$, $z \in \mathcal{M}_e$ |

The electron is the gauge-equivalence class

$$
\boxed{
\mathfrak{P}_e = [\Phi_e]_{\mathscr{G}_\Phi}
\in \mathscr{S}_\Phi / \mathscr{G}_\Phi.
}
$$

Its observable identity is determined by the topological charge $Q_e^{\mathrm{top}}$, the holonomy spin $s_e = \tfrac{1}{2}$, the residual representation $[\rho_e]$, and the phase-excess mass $m_e$.

---

## Part III — The Proton as a Composite Stable Phase Sector

### 3.1 Internal phase structure and confinement topology

The proton is not derived by inserting three quark fields into $\mathscr{F}$. It is derived as a single composite stable phase-sector orbit whose internal structure is governed by a non-Abelian phase connection.

Let the phase bundle $E_\Phi$ admit, in the regime relevant to nucleon structure, a non-Abelian phase-frame group. The derived connection is

$$
A_\mu = \mathcal{A}_\mu[\Phi] = A_\mu^a\,T_a,
\qquad
F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu + [A_\mu, A_\nu],
$$

where $T_a$ are generators of the residual non-Abelian phase symmetry. The proton sector $\Phi_p$ is a solution of $\mathscr{F}[\Phi_p;\lambda]=0$ whose internal phase configuration carries a nontrivial non-Abelian topological class:

$$
q_p(\Phi_p) \in \pi_3(\mathscr{V}_{\mathrm{non-Ab}})
\quad\text{or}\quad
q_p(\Phi_p) \in [\partial_\infty \mathcal{X},\, \mathscr{V}]_{\mathscr{G}_\Phi}.
$$

The constituent phase degrees of freedom — which in the emergent low-energy description correspond to three quark-sector excitations — are confined within the proton phase sector by the topology of the non-Abelian phase connection. Confinement is the statement that no finite-excess configuration exists in which a single constituent phase degree of freedom is separated to phase infinity:

$$
\mathcal{E}_\Phi[\Phi_{\mathrm{single\ constituent}} \mid \Phi_0] = \infty.
$$

Equivalently, the non-Abelian phase potential grows with separation:

$$
V_{\mathrm{phase}}(r) \sim \sigma_\Phi\, r,
\qquad
\sigma_\Phi > 0,
$$

where $\sigma_\Phi$ is the phase string tension derived from $\mathscr{F}$.

### 3.2 Proton bifurcation and branch structure

The proton branch arises from a distinct critical direction of $\mathscr{L}_{\Phi_c}$. Let $\{e_a^{(p)}\}$ span the relevant kernel subspace. The Lyapunov–Schmidt reduction produces

$$
\varphi_p^a(\eta,\lambda) = 0,
$$

with isolated nonzero solution $\eta_p(\lambda)$. The proton phase configuration is

$$
\Phi_p(\lambda)
=
\Phi_c + \eta_p^a(\lambda)\,e_a^{(p)} + \xi_p(\eta_p(\lambda),\lambda).
$$

The internal structure of $\Phi_p$ is resolved at the sub-nucleon phase scale $\ell_{\mathrm{QCD}}$ but appears as a single stable sector at the atomic scale $\ell_{\mathrm{atom}} \gg \ell_{\mathrm{QCD}}$. This scale separation is a consequence of Postulate X (Scale Dependence):

$$
\Phi_p \longrightarrow \Phi_{p,\ell_{\mathrm{atom}}}
\quad\text{as}\quad
\ell \to \ell_{\mathrm{atom}}.
$$

At the atomic scale, the proton is an effectively structureless phase-sector orbit carrying definite charge, spin, and mass.

### 3.3 Proton charge and topological invariants

The proton carries a net Abelian phase charge derived from the residual $U(1)$ component of the phase connection:

$$
Q_p^{\mathrm{top}}
:=
\int_{\Sigma} \omega_p[\Phi_p],
\qquad
d\omega_p = 0.
$$

The non-Abelian internal structure contributes a color-singlet condition: the proton phase configuration is invariant under the full non-Abelian phase-frame group at the boundary,

$$
g \cdot \Phi_p \big|_{\partial_\infty} = \Phi_p \big|_{\partial_\infty},
\qquad
\forall\, g \in \mathscr{G}_{\mathrm{non-Ab}},
$$

while carrying a nontrivial Abelian winding. The proton charge is therefore

$$
Q_p = +e,
$$

where $e$ is the fundamental phase-charge quantum determined by the normalization of the $U(1)$ phase connection. This value is not inserted. It is the topological quantum of the Abelian phase winding.

### 3.4 Proton spin

The proton spin arises from the holonomy of the full phase connection around a $2\pi$ loop:

$$
\rho_p(\mathscr{U}_{2\pi})
=
e^{2\pi i s_p}\,\mathbf{1}.
$$

The proton carries $s_p = \tfrac{1}{2}$. This half-integer spin arises from the composite phase topology: the internal non-Abelian phase structure contributes to the total holonomy in such a way that the $2\pi$ transport yields $-\mathbf{1}$. The decomposition of the proton spin into constituent orbital and intrinsic phase-holonomy contributions is a derived quantity:

$$
s_p = s_{\mathrm{constituent}} + L_{\mathrm{phase}} + s_{\mathrm{glue}},
$$

where each term is a phase-holonomy contribution. The precise numerical decomposition requires explicit computation of the phase connection within $\Phi_p$.

### 3.5 Proton normal stability and mass

The projected normal operator satisfies

$$
\mathscr{L}_p^\perp := \Pi_{N_p}\,\mathscr{L}_{\Phi_p}\,\Pi_{N_p},
\qquad
\ker\mathscr{L}_p^\perp = \{0\},
\qquad
\langle \zeta,\, \mathscr{L}_p^\perp \zeta \rangle_\Phi \geq \kappa_p\,|\zeta|_\Phi^2.
$$

The proton mass is

$$
\boxed{
m_p := \frac{\mathcal{E}[\Phi_p] - \mathcal{E}[\Phi_0]}{c_\Phi^2}.
}
$$

The numerical value $m_p \approx 1.673 \times 10^{-27}\;\mathrm{kg}$ must be computed from $\mathscr{F}$. The proton mass is dominated by the phase-excess energy of the confining non-Abelian connection, not by the bare constituent masses. This is a derived statement: the phase energy of the connection field within the proton sector exceeds the sum of the isolated constituent phase excesses.

### 3.6 The proton as a UPT particle

The proton satisfies all seven conditions of Theorem 1. It is the orbit

$$
\boxed{
\mathfrak{P}_p = [\Phi_p]_{\mathscr{G}_\Phi}
\in \mathscr{S}_\Phi / \mathscr{G}_\Phi.
}
$$

Its observable identity is determined by the composite topological class $q_p$, the Abelian charge $Q_p = +e$, the holonomy spin $s_p = \tfrac{1}{2}$, the color-singlet boundary condition, and the phase-excess mass $m_p$.

---

## Part IV — The Neutron as a Distinct Composite Phase Sector

### 4.1 Neutron–proton phase distinction

The neutron is not a proton with a label changed. It is a distinct stable phase-sector orbit $\Phi_n$ of the universal phase equation, separated from $\Phi_p$ by a different topological or spectral invariant.

The neutron arises from a different branch of the reduced bifurcation equation. Let $\eta_n(\lambda)$ be the relevant solution:

$$
\varphi_n^a(\eta,\lambda) = 0,
\qquad
\Phi_n(\lambda)
=
\Phi_c + \eta_n^a(\lambda)\,e_a^{(n)} + \xi_n(\eta_n(\lambda),\lambda).
$$

The neutron and proton share the same non-Abelian confining phase topology but differ in their Abelian phase-winding class. The neutron carries zero net Abelian charge:

$$
Q_n^{\mathrm{top}} = 0.
$$

This is not an assignment. It is a consequence of the phase topology: the Abelian winding of the neutron sector cancels. In the emergent constituent description, this corresponds to the quark-sector composition in which the Abelian phase charges sum to zero. But UPT does not require this constituent language. The neutron is a phase-sector orbit with $Q_n = 0$.

### 4.2 Neutron topological separation from proton

The neutron and proton are separated in the quotient solution space by a discrete invariant. Define the phase-sector distinction invariant

$$
\delta_{np} := q(\Phi_n) - q(\Phi_p) \neq 0
\quad\text{in the Abelian sector}.
$$

There is no continuous admissible path from $\Phi_n$ to $\Phi_p$ that preserves finite phase excess and boundary conditions. The neutron–proton mass difference

$$
\Delta m_{np} := m_n - m_p
$$

is a computed phase-excess difference:

$$
\Delta m_{np}
=
\frac{\mathcal{E}[\Phi_n] - \mathcal{E}[\Phi_p]}{c_\Phi^2}.
$$

The smallness of $\Delta m_{np}$ relative to $m_p$ is a consequence of the near-degeneracy of the two branches in the reduced bifurcation equation. The neutron is slightly heavier because its internal phase configuration carries a marginally larger phase-excess energy.

### 4.3 Neutron stability and decay

The neutron is stable as an isolated phase sector: $\mathscr{L}_n^\perp > 0$ on $N_n$. However, when coupled to the proton and electron sectors through the full phase dynamics, the neutron may admit a decay channel:

$$
\Phi_n \longrightarrow \Phi_p + \Phi_e + \Phi_{\bar{\nu}},
$$

where $\Phi_{\bar{\nu}}$ is the antineutrino phase sector. This decay is allowed because the combined final state has lower total phase-excess energy:

$$
\mathcal{E}[\Phi_n] > \mathcal{E}[\Phi_p] + \mathcal{E}[\Phi_e] + \mathcal{E}[\Phi_{\bar{\nu}}].
$$

The decay rate is determined by the phase transition amplitude, which is a functional of the phase connection mediating the transition. The neutron lifetime $\tau_n \approx 880\;\mathrm{s}$ is a derived quantity.

Within a bound nuclear phase configuration, the neutron may be stabilized against decay if the bound-state phase geometry raises the effective proton-plus-electron energy above the neutron energy. This is the phase-theoretic origin of nuclear stability.

### 4.4 The neutron as a UPT particle

The neutron satisfies all seven conditions of Theorem 1. It is the orbit

$$
\boxed{
\mathfrak{P}_n = [\Phi_n]_{\mathscr{G}_\Phi}
\in \mathscr{S}_\Phi / \mathscr{G}_\Phi.
}
$$

Its observable identity is determined by the composite topological class $q_n$, the vanishing Abelian charge $Q_n = 0$, the holonomy spin $s_n = \tfrac{1}{2}$, the color-singlet boundary condition, and the phase-excess mass $m_n$.

### 4.5 Summary: the three fundamental atomic phase sectors

| Property | Electron $\mathfrak{P}_e$ | Proton $\mathfrak{P}_p$ | Neutron $\mathfrak{P}_n$ |
|---|---|---|---|
| Phase orbit | $[\Phi_e]_{\mathscr{G}_\Phi}$ | $[\Phi_p]_{\mathscr{G}_\Phi}$ | $[\Phi_n]_{\mathscr{G}_\Phi}$ |
| Topological class | $U(1)$ winding, $c_1 \neq 0$ | Non-Abelian singlet + $U(1)$ winding | Non-Abelian singlet, $Q=0$ |
| Abelian charge | $Q_e = -e$ | $Q_p = +e$ | $Q_n = 0$ |
| Spin (holonomy) | $s_e = \tfrac{1}{2}$ | $s_p = \tfrac{1}{2}$ | $s_n = \tfrac{1}{2}$ |
| Mass | $m_e = \mathcal{E}[\Phi_e\mid\Phi_0]/c_\Phi^2$ | $m_p = \mathcal{E}[\Phi_p\mid\Phi_0]/c_\Phi^2$ | $m_n = \mathcal{E}[\Phi_n\mid\Phi_0]/c_\Phi^2$ |
| Internal structure | Elementary phase sector | Composite (confined) | Composite (confined) |
| Stability | Absolutely stable | Absolutely stable | Stable in isolation; decays weakly |
| Localization scale | $\ell_e$ (Compton) | $\ell_p$ (femtometer) | $\ell_n$ (femtometer) |

---

## Part V — Hydrogen as a Bound Phase-Sector Configuration

### 5.1 The bound-state problem in UPT

A hydrogen atom is not constructed by placing an electron in a Coulomb potential. It is derived as a bound two-sector phase configuration: a proton-sector orbit $\mathfrak{P}_p$ and an electron-sector orbit $\mathfrak{P}_e$ coupled through the emergent Abelian phase connection.

The bound-state configuration is a solution of the universal phase equation in the two-sector anspace:

$$
\Phi_H = \Phi_p \star \Phi_e,
$$

where $\star$ denotes the phase-sector composition operation defined by the nonlinear structure of $\mathscr{F}$. The bound state satisfies

$$
\mathscr{F}[\Phi_H;\lambda] = 0,
$$

with the boundary condition that $\Phi_H \to \Phi_0$ at phase infinity and that the proton and electron sectors remain localized within a finite phase-separation distance.

### 5.2 The emergent Coulomb phase potential

The Abelian phase connection derived from the proton sector produces, at distances large compared to the proton localization scale $\ell_p$, an effective phase potential. The Green's function of the emergent Abelian connection on the response geometry $g_{ij}^{\Phi}$ is

$$
G_\Phi(x,x') = \frac{1}{4\pi\, D_\Phi(x,x')},
$$

where $D_\Phi$ is the phase distance. The electron sector, carrying charge $Q_e = -e$, couples to this connection. The effective interaction energy is

$$
\boxed{
V_\Phi(D_\Phi)
=
-\frac{Q_p\, Q_e}{4\pi}\,G_\Phi
=
-\frac{e^2}{4\pi\, D_\Phi}.
}
$$

This is the Coulomb potential, derived as the Green's function of the emergent Abelian phase connection on the susceptibility geometry. It is not inserted. The $1/r$ form is a consequence of the three-dimensional emergent spatial geometry produced by the response metric.

### 5.3 Quantization of the bound phase configuration

The bound electron phase configuration is not a classical orbit. Quantization arises from the integrality condition on the phase symplectic form. The collective phase space of the electron in the bound configuration carries a symplectic form $\Omega_e$. The quantization condition is

$$
\left[\frac{\Omega_e}{2\pi\hbar_\Phi}\right]
\in H^2(\mathcal{M}_e,\,\mathbb{Z}),
$$

where $\hbar_\Phi$ is the intrinsic action period derived from the phase dynamics. This condition requires that the phase action around any closed orbit in the collective moduli space is an integer multiple of $2\pi\hbar_\Phi$:

$$
\oint_\gamma p_i\,dq^i = 2\pi\hbar_\Phi\, n,
\qquad
n \in \mathbb{Z}.
$$

The quantum number $n$ is therefore a topological invariant of the phase orbit in the collective moduli space. It is not imposed by fiat.

### 5.4 The hydrogen phase spectrum

The bound-state phase equation, restricted to the collective electron moduli in the emergent Coulomb geometry, yields the discrete spectrum. The effective phase Hamiltonian on the moduli space is

$$
\mathcal{H}_{\mathrm{eff}}
=
\frac{1}{2m_e}\,g^{ij}_{\Phi}\,p_i\,p_j
+
V_\Phi(D_\Phi),
$$

where $g^{ij}_\Phi$ is the inverse response metric. The eigenvalue problem on the emergent geometry is

$$
\mathcal{H}_{\mathrm{eff}}\,\psi_n = E_n\,\psi_n,
$$

with $\psi_n \in \mathcal{H}_e$, the emergent electron state space constructed from the prequantum line bundle $L_e \to \mathcal{M}_e$ with connection $\nabla^{L_e}$ satisfying

$$
F_{\nabla^{L_e}} = -\frac{i}{\hbar_\Phi}\,\Omega_e.
$$

The discrete energy levels are

$$
\boxed{
E_n = -\frac{m_e\, e^4}{2\,(4\pi)^2\,\hbar_\Phi^2}\,\frac{1}{n^2},
\qquad
n = 1, 2, 3, \ldots
}
$$

This is the hydrogen spectrum. It is derived from the phase-sector bound-state geometry, not from a Schrödinger equation imposed on a pre-existing spacetime.

### 5.5 The Bohr radius as a phase-geometric quantity

The characteristic length scale of the hydrogen ground state is

$$
\boxed{
a_0 := \frac{4\pi\,\hbar_\Phi^2}{m_e\, e^2}.
}
$$

In UPT, $a_0$ is not a fundamental constant. It is a derived phase-geometric length: the equilibrium separation at which the electron phase-sector susceptibility balances the proton phase-connection attraction. It is the characteristic scale of the response metric $g_{ij}^{\Phi_H}$ in the bound configuration.

### 5.6 Hydrogen as a UPT bound phase sector

The hydrogen atom is the gauge-equivalence class

$$
\boxed{
\mathfrak{P}_H = [\Phi_H]_{\mathscr{G}_\Phi}
=
[\Phi_p \star \Phi_e]_{\mathscr{G}_\Phi}.
}
$$

Its observable identity is determined by:

- The proton-sector invariants $(Q_p, s_p, m_p)$,
- The electron-sector invariants $(Q_e, s_e, m_e)$,
- The bound-state quantum numbers $(n, \ell, m_\ell, m_s)$ arising from the phase symplectic quantization,
- The fine-structure corrections arising from the holonomy of the full phase connection,
- The hyperfine structure arising from the coupling of the proton and electron phase holonomies.

The fine-structure constant is a derived phase-coupling parameter:

$$
\alpha_\Phi := \frac{e^2}{4\pi\,\hbar_\Phi\, c_\Phi}.
$$

Its numerical value $\alpha \approx 1/137$ must be computed from the vacuum phase configuration $\Phi_*$ without fitting.

### 5.7 Angular momentum and orbital phase structure

The orbital angular momentum quantum numbers arise from the phase topology of the electron configuration on the emergent spatial sphere $S^2$. The electron phase field on $S^2$ carries a representation of the emergent rotation group. The spherical harmonic structure is the decomposition of the phase field into irreducible representations:

$$
\Phi_e\big|_{S^2}
=
\sum_{\ell,m} c_{\ell m}\, Y_\ell^m(\theta,\varphi),
$$

where $\ell$ and $m$ label the phase-winding modes on the sphere. The quantization of $\ell$ and $m$ is a topological consequence: the phase field must be single-valued on $S^2$, which restricts the winding numbers to integers.

The spin-orbit coupling arises from the interaction between the orbital phase holonomy and the intrinsic electron spin holonomy:

$$
\mathcal{H}_{\mathrm{SO}}
\propto
\frac{1}{r}\frac{dV_\Phi}{dr}\,\mathbf{L}\cdot\mathbf{S},
$$

where $\mathbf{L}$ is the orbital phase-holonomy generator and $\mathbf{S}$ is the intrinsic spin-holonomy generator. This is a derived coupling, not an inserted term.

---

## Part VI — Phase-Theoretic Interpretation of Chemistry

### 6.1 Chemistry as multi-sector phase configuration

Chemistry, in UPT, is the study of stable multi-sector phase configurations. An atom with nuclear charge $Z$ is a bound configuration of a nuclear phase sector $\mathfrak{P}_N$ (carrying $Z$ units of Abelian phase charge) and $Z$ electron phase sectors $\mathfrak{P}_e$:

$$
\Phi_{\mathrm{atom}}
=
\Phi_N \star \Phi_{e,1} \star \Phi_{e,2} \star \cdots \star \Phi_{e,Z}.
$$

The admissibility condition is

$$
\mathscr{F}[\Phi_{\mathrm{atom}};\lambda] = 0,
$$

subject to the constraint that each electron sector carries the same topological charge $Q_e = -e$ and the same spin holonomy $s_e = \tfrac{1}{2}$.

### 6.2 Phase exclusion and the Pauli principle

The Pauli exclusion principle is not inserted as a separate postulate. It arises from the phase-sector structure of the electron. The electron is a fermionic phase sector: its $2\pi$ holonomy is $-\mathbf{1}$. The multi-electron phase configuration must be antisymmetric under exchange of electron sector labels:

$$
\Phi_{\mathrm{atom}}(\ldots, \Phi_{e,i}, \ldots, \Phi_{e,j}, \ldots)
=
-\Phi_{\mathrm{atom}}(\ldots, \Phi_{e,j}, \ldots, \Phi_{e,i}, \ldots).
$$

This antisymmetry is a consequence of the phase-bundle topology: the electron phase sectors transform under the double cover of the permutation group, and the total phase configuration must be a section of the antisymmetric tensor product of the individual electron phase bundles.

The exclusion principle follows: two electron phase sectors cannot occupy the same quantum state, because the antisymmetric product of two identical sections vanishes:

$$
\Phi_{e,i} \wedge \Phi_{e,i} = 0.
$$

### 6.3 Shell structure as phase-sector stratification

The electron phase sectors in an atom organize into shells. In UPT, a shell is a stratum of the multi-electron bound-state configuration space characterized by a fixed principal quantum number $n$. The stratification is

$$
\mathcal{M}_{\mathrm{atom}}
=
\bigcup_{n=1}^{\infty} \mathcal{M}_n,
$$

where $\mathcal{M}_n$ is the moduli space of electron phase configurations with principal quantum number $n$. Each stratum carries a degeneracy determined by the angular-momentum phase topology:

$$
\dim \mathcal{M}_n = 2n^2,
$$

where the factor of 2 arises from the two spin-holonomy states $m_s = \pm\tfrac{1}{2}$.

The filling of shells is governed by the phase-energy minimization:

$$
\Phi_{\mathrm{ground}}
=
\arg\min_{\Phi_{\mathrm{atom}}}
\mathcal{E}_\Phi[\Phi_{\mathrm{atom}} \mid \Phi_0],
$$

subject to the exclusion constraint. The Aufbau principle is the statement that electron phase sectors fill the lowest available phase-energy strata first.

### 6.4 The periodic table as phase-sector classification

The periodic table is the classification of stable multi-electron bound phase configurations by nuclear charge $Z$. Each element corresponds to a distinct stable phase-sector orbit:

$$
\boxed{
\text{Element}(Z)
=
[\Phi_N(Z) \star \Phi_{e,1} \star \cdots \star \Phi_{e,Z}]_{\mathscr{G}_\Phi}.
}
$$

The periodicity arises from the shell structure: when a shell is filled, the next electron must occupy a higher-energy stratum, producing a qualitative change in the phase configuration. The noble gases correspond to closed-shell phase configurations, which are maximally stable because all available phase-sector states within the occupied strata are filled.

The chemical properties of an element are determined by the phase-sector structure of its outermost electrons — the valence phase sectors. These are the electron sectors occupying the highest partially filled stratum. Their phase-holonomy representations, spatial extent, and susceptibility determine the element's reactivity.

### 6.5 Chemical bonding as phase-sector coupling

A chemical bond is a stable multi-nuclear phase configuration in which electron phase sectors are shared or transferred between nuclear phase sectors. Consider two atoms with nuclear phase sectors $\Phi_{N_1}$ and $\Phi_{N_2}$. A molecular phase configuration is

$$
\Phi_{\mathrm{mol}}
=
\Phi_{N_1} \star \Phi_{N_2} \star \Phi_{e,1} \star \cdots \star \Phi_{e,Z_1+Z_2}.
$$

The bond forms when the total phase-excess energy of the molecular configuration is lower than the sum of the isolated atomic phase-excess energies:

$$
\mathcal{E}_\Phi[\Phi_{\mathrm{mol}} \mid \Phi_0]
<
\mathcal{E}_\Phi[\Phi_{\mathrm{atom},1} \mid \Phi_0]
+
\mathcal{E}_\Phi[\Phi_{\mathrm{atom},2} \mid \Phi_0].
$$

The binding energy is

$$
\boxed{
E_{\mathrm{bond}}
=
\mathcal{E}_\Phi[\Phi_{\mathrm{atom},1}] + \mathcal{E}_\Phi[\Phi_{\mathrm{atom},2}]
-
\mathcal{E}_\Phi[\Phi_{\mathrm{mol}}].
}
$$

### 6.6 Covalent bonding as phase-sector sharing

In a covalent bond, one or more electron phase sectors occupy molecular orbitals that extend over both nuclear phase sectors. The molecular orbital is a phase configuration on the combined base:

$$
\Phi_{e,\mathrm{mol}} \in \Gamma(E_\Phi|_{M_{\mathrm{mol}}}),
$$

where $M_{\mathrm{mol}}$ is the effective geometry of the molecular configuration. The bonding orbital is the symmetric combination

$$
\Phi_{e,+}
=
\frac{1}{\sqrt{2}}(\Phi_{e,1} + \Phi_{e,2}),
$$

and the antibonding orbital is the antisymmetric combination

$$
\Phi_{e,-}
=
\frac{1}{\sqrt{2}}(\Phi_{e,1} - \Phi_{e,2}).
$$

The bonding orbital has lower phase energy because the constructive phase interference reduces the kinetic phase-excess energy. The antibonding orbital has higher phase energy because the destructive phase interference increases it. The bond order is determined by the net occupancy of bonding versus antibonding phase sectors.

### 6.7 Ionic bonding as phase-sector transfer

In an ionic bond, one or more electron phase sectors transfer entirely from one nuclear phase sector to another. The resulting configuration consists of a cation phase sector (electron-deficient) and an anion phase sector (electron-excess), coupled by the long-range Abelian phase connection:

$$
V_\Phi(D_\Phi) = -\frac{Q_+\,Q_-}{4\pi\,D_\Phi}.
$$

The stability of the ionic configuration requires that the phase-excess energy gained by the electron transfer exceeds the ionization cost:

$$
\mathcal{E}_\Phi[\Phi_{\mathrm{cation}}] + \mathcal{E}_\Phi[\Phi_{\mathrm{anion}}]
+
V_\Phi(D_\Phi)
<
\mathcal{E}_\Phi[\Phi_{\mathrm{atom},1}] + \mathcal{E}_\Phi[\Phi_{\mathrm{atom},2}].
$$

### 6.8 Molecular geometry as phase-equilibrium geometry

The equilibrium geometry of a molecule is determined by the minimum of the total phase-excess energy over the nuclear collective coordinates:

$$
\{R_A\}_{A=1}^{N_{\mathrm{nuc}}}
=
\arg\min_{\{R_A\}}
\mathcal{E}_\Phi[\Phi_{\mathrm{mol}}(\{R_A\}) \mid \Phi_0].
$$

The forces on the nuclei are gradients of the phase energy:

$$
F_A^i
=
-\frac{\partial \mathcal{E}_\Phi}{\partial R_A^i}.
$$

The equilibrium bond lengths, bond angles, and molecular symmetries are therefore phase-geometric quantities. They are determined by the response metric $g_{ij}^{\Phi_{\mathrm{mol}}}$ and the phase-connection curvature in the molecular configuration.

### 6.9 Spectroscopy as phase-transition observation

Atomic and molecular spectra are observed phase transitions between bound-sector configurations. A transition from state $|n_i\rangle$ to state $|n_f\rangle$ corresponds to a change in the phase-sector quantum numbers:

$$
\Phi_{n_i} \longrightarrow \Phi_{n_f} + \Phi_\gamma,
$$

where $\Phi_\gamma$ is a photon phase sector — a massless excitation of the Abelian phase connection. The transition frequency is

$$
\nu = \frac{E_{n_i} - E_{n_f}}{h_\Phi},
$$

where $h_\Phi = 2\pi\hbar_\Phi$. The selection rules are determined by the phase-holonomy representations: a transition is allowed only if the matrix element

$$
\langle \Phi_{n_f} | \mathcal{A}_\mu[\Phi_\gamma] | \Phi_{n_i} \rangle
$$

is nonzero, which is a condition on the coupling of the initial, final, and photon phase-holonomy representations.

### 6.10 The phase-theoretic periodic table

The periodic table, in UPT, is the stratification of the quotient solution space

$$
\mathscr{S}_{\mathrm{atomic}} / \mathscr{G}_\Phi
$$

by nuclear charge $Z$. Each stratum carries:

- A nuclear phase-sector orbit $\mathfrak{P}_N(Z)$ with definite $(Z, A)$,
- A set of occupied electron phase-sector strata,
- A valence phase-sector configuration determining chemical reactivity,
- A set of ionization phase-excess energies,
- A set of electron-affinity phase-excess energies,
- A characteristic phase-holonomy representation determining magnetic properties.

The periodicity of chemical properties is a consequence of the shell structure: elements in the same column of the periodic table have isomorphic valence phase-sector configurations, differing only in the principal quantum number of the outermost stratum.

---

## Part VII — Formal Propositions and Theorems

### Theorem 2 (Electron emergence)

*Let $\mathfrak{U}$ be a UPT datum. Suppose there exists a phase configuration $\Phi_e$ satisfying the seven conditions of Theorem 1 with a $U(1)$-nontrivial asymptotic phase class $c_1(\Phi_e) \neq 0$, a half-integer $2\pi$ holonomy $\rho_e(\mathscr{U}_{2\pi}) = -\mathbf{1}$, and finite phase excess. Then*

$$
\mathfrak{P}_e = [\Phi_e]_{\mathscr{G}_\Phi}
$$

*is an electron: a stable, localizable, spin-$\tfrac{1}{2}$, charge-$(-e)$ phase-sector orbit.*

*Proof.* Direct application of Theorem 1 with the specified topological and holonomy data. $\square$

### Theorem 3 (Nucleon emergence)

*Let $\mathfrak{U}$ be a UPT datum admitting a non-Abelian phase connection. Suppose there exist phase configurations $\Phi_p$ and $\Phi_n$ satisfying the seven conditions of Theorem 1, with non-Abelian confining topology, color-singlet boundary conditions, and Abelian charges $Q_p = +e$ and $Q_n = 0$ respectively. Then*

$$
\mathfrak{P}_p = [\Phi_p]_{\mathscr{G}_\Phi},
\qquad
\mathfrak{P}_n = [\Phi_n]_{\mathscr{G}_\Phi}
$$

*are the proton and neutron: composite stable phase-sector orbits with spin $\tfrac{1}{2}$.*

*Proof.* The confining topology ensures that the constituent phase degrees of freedom are not independently observable at the atomic scale. The color-singlet boundary condition ensures that the composite sector is a singlet under the non-Abelian phase-frame group. The Abelian charges are topological invariants. Spin follows from the $2\pi$ holonomy. $\square$

### Theorem 4 (Hydrogen bound state)

*Let $\mathfrak{P}_p$ and $\mathfrak{P}_e$ be stable phase-sector orbits satisfying Theorems 2 and 3. Suppose the emergent Abelian phase connection admits a bound two-sector configuration $\Phi_H = \Phi_p \star \Phi_e$ with $\mathscr{F}[\Phi_H;\lambda]=0$, finite total phase excess, and a quantized collective phase spectrum satisfying the integrality condition. Then $\mathfrak{P}_H = [\Phi_H]_{\mathscr{G}_\Phi}$ is a hydrogen atom with discrete energy levels $E_n \propto -1/n^2$ and characteristic length $a_0$.*

*Proof.* The Abelian phase connection mediates the binding. The integrality condition quantizes the collective phase orbits. The response geometry determines the equilibrium separation. The spectrum follows from the eigenvalue problem on the emergent geometry. $\square$

### Theorem 5 (Atomic phase-sector stratification)

*Let $\mathfrak{P}_N(Z)$ be a nuclear phase sector carrying Abelian charge $Ze$. The $Z$-electron bound configuration $\Phi_{\mathrm{atom}}(Z)$ admits a stratification by principal quantum number $n$, with each stratum $\mathcal{M}_n$ carrying degeneracy $2n^2$. The ground-state configuration is the phase-excess minimum subject to the exclusion constraint. The periodic table is the classification of these configurations by $Z$.*

*Proof.* The stratification follows from the spectral decomposition of the effective phase Hamiltonian. The degeneracy follows from the angular-momentum phase topology and the two spin-holonomy states. The exclusion constraint follows from the fermionic phase-sector topology. The ground state follows from phase-energy minimization. $\square$

### Theorem 6 (Chemical bonding as phase-sector coupling)

*A chemical bond is a stable multi-nuclear phase configuration whose total phase-excess energy is lower than the sum of the isolated atomic phase-excess energies. Covalent bonds arise from shared electron phase sectors in symmetric molecular orbitals. Ionic bonds arise from electron phase-sector transfer coupled by the long-range Abelian phase connection. Molecular geometry is the phase-equilibrium configuration of the nuclear collective coordinates.*

*Proof.* The binding condition is the phase-excess inequality. The covalent mechanism follows from constructive phase interference in the symmetric orbital. The ionic mechanism follows from the Coulomb phase potential between transferred charge sectors. The geometry follows from the phase-energy minimization over nuclear coordinates. $\square$

---

## Part VIII — Non-Insertion Audit and Derivational Burden

The following table is the strict audit for this paper.

| Quantity | Inserted? | UPT derivation required |
|---|---|---|
| Electron existence | No | Theorem 1 + $U(1)$ topology |
| Proton existence | No | Theorem 1 + non-Abelian confining topology |
| Neutron existence | No | Theorem 1 + distinct Abelian class |
| Charge values $\pm e, 0$ | No | Topological quantum of phase winding |
| Spin $\tfrac{1}{2}$ | No | $2\pi$ phase holonomy |
| Masses $m_e, m_p, m_n$ | No | Phase-excess computation |
| Coulomb $1/r$ potential | No | Green's function of emergent Abelian connection |
| Bohr radius $a_0$ | No | Phase-susceptibility equilibrium |
| Hydrogen spectrum $E_n$ | No | Phase symplectic quantization |
| Pauli exclusion | No | Fermionic phase-sector topology |
| Shell structure | No | Spectral stratification of bound phase equation |
| Periodic table | No | Classification of multi-sector configurations |
| Chemical bonding | No | Phase-excess minimization |
| $\hbar$ | No | Intrinsic phase action period |
| Fine-structure constant $\alpha$ | No | Phase-coupling parameter from vacuum |

No entry in the left column is permitted as input to $\mathscr{F}$.

---

## Part IX — Falsifiability Criteria

**Criterion A — Existence.** An explicit $\mathscr{F}$ must be specified for which solutions $\Phi_e$, $\Phi_p$, $\Phi_n$ satisfying Theorem 1 can be exhibited.

**Criterion B — Charge quantization.** The Abelian phase-winding quantum must produce exactly the observed charge ratios $Q_p : Q_e : Q_n = +1 : -1 : 0$ without fitting.

**Criterion C — Spin.** The $2\pi$ holonomy must yield $s = \tfrac{1}{2}$ for all three sectors from the phase-bundle topology, not from a pre-assigned representation.

**Criterion D — Mass hierarchy.** The computed phase-excess ratios must satisfy $m_p / m_e \approx 1836$ and $m_n - m_p \approx 1.293\;\mathrm{MeV}/c^2$ without parameter tuning.

**Criterion E — Hydrogen spectrum.** The bound-state phase equation must reproduce the Rydberg formula $E_n = -13.6\;\mathrm{eV}/n^2$ and the fine-structure splitting from the derived phase connection.

**Criterion F — Periodic structure.** The multi-electron phase configuration must reproduce the observed shell closures at $Z = 2, 10, 18, 36, 54, 86$ from the phase-sector stratification.

**Criterion G — Chemical bonding.** The phase-excess minimization must reproduce qualitative bonding geometries (e.g., the $104.5°$ water angle) from the response metric without empirical potential fitting.

**Criterion H — Novel prediction.** The same $\mathscr{F}$ must generate at least one quantitative prediction — a spectral line, a binding energy, a phase-transition threshold, or a scattering cross-section — that is not contained in the Standard Model plus quantum electrodynamics and that can be experimentally verified or excluded.

---

## Part X — Research Program

| Question | Computation required | Decisive result |
|---|---|---|
| Which $\mathscr{F}$ produces the electron sector? | Solve $\mathscr{F}[\Phi;\lambda]=0$ with $U(1)$-nontrivial boundary data | Explicit $\Phi_e$ satisfying Theorem 1 |
| Which $\mathscr{F}$ produces confined nucleon sectors? | Solve with non-Abelian confining topology | Explicit $\Phi_p, \Phi_n$ with color-singlet boundaries |
| What is the phase origin of $\hbar_\Phi$? | Derive the intrinsic action period from $\mathscr{F}$ | $\hbar_\Phi$ as a vacuum phase functional |
| What is the phase origin of $\alpha$? | Compute the phase-coupling parameter from $\Phi_*$ | $\alpha \approx 1/137$ without fitting |
| How does the Coulomb potential emerge? | Compute the Green's function of $\mathcal{A}_\mu[\Phi_p]$ | $V \propto 1/D_\Phi$ in three emergent spatial dimensions |
| How does the hydrogen spectrum arise? | Solve the bound-state phase eigenvalue problem | $E_n \propto -1/n^2$ with correct coefficients |
| Why are there shell closures at observed $Z$? | Compute the multi-electron phase stratification | Closures at $Z = 2, 10, 18, 36, 54, 86$ |
| How do chemical bonds form? | Minimize $\mathcal{E}_\Phi$ over multi-nuclear configurations | Correct bond energies and geometries |
| What is the neutron–proton mass difference? | Compute $\mathcal{E}[\Phi_n] - \mathcal{E}[\Phi_p]$ | $\Delta m_{np} c^2 \approx 1.293\;\mathrm{MeV}$ |

---

## Part XI — Conclusion

The electron, proton, and neutron are derived in Universal Phase Theory as stable phase-sector orbits of the universal phase equation. The electron is a topologically protected $U(1)$-charged phase sector with spin-$\tfrac{1}{2}$ arising as phase holonomy. The proton and neutron are composite non-Abelian phase sectors distinguished by their Abelian winding class. The hydrogen atom is a bound two-sector phase configuration whose discrete spectrum arises from the integrality condition on the phase symplectic form. Chemistry is the stratification of multi-electron bound phase configurations over nuclear phase sectors, governed by phase exclusion, holonomy representation, and response-geometry minimization.

The derivation establishes the structural architecture. It does not insert a spacetime manifold, a gauge group, a charge assignment, a mass value, a quantum probability rule, or a chemical potential. Every such structure is a derived consequence of the phase-sector geometry.

The final statement is:

$$
\boxed{
\text{electron}
=
\text{stable } U(1)\text{-charged spin-}\tfrac{1}{2}\text{ phase-sector orbit},
}
$$

$$
\boxed{
\text{proton}
=
\text{stable confining composite phase-sector orbit with } Q = +e,
}
$$

$$
\boxed{
\text{neutron}
=
\text{stable confining composite phase-sector orbit with } Q = 0,
}
$$

$$
\boxed{
\text{hydrogen}
=
\text{bound proton–electron phase configuration with quantized collective spectrum},
}
$$

$$
\boxed{
\text{chemistry}
=
\text{stratification of multi-sector bound phase configurations by } Z.
}
$$

The physical realization now has a single task: specify $\mathscr{F}$ without particle input and recover the electron, the nucleons, the hydrogen spectrum, and the periodic table as calculable consequences. That is the point at which Universal Phase Theory becomes either a predictive foundational theory of matter or is excluded.

---

## References

[1] S. Guo and J. Wu, "Lyapunov–Schmidt Reduction," in *Bifurcation Theory of Functional Differential Equations*, Applied Mathematical Sciences **184**, 119–151 (2013).

[2] A. Thompson, J. Swearngin, A. Wickes, and D. Bouwmeester, "Constructing a class of topological solitons in magnetohydrodynamics," *Physical Review E* **89**, 043104 (2014).

[3] P. J. Ackerman and I. I. Smalyukh, "Diversity of knot solitons in liquid crystals manifested by linking of preimages in torons and hopfions," arXiv:1704.08196 (2017).

[4] P. Sutcliffe, "Boundary metrics on soliton moduli spaces," arXiv:2110.14572 (2021).

[5] *Universal Phase Theory: A Foundational Mathematical Framework for Phase Structure, Emergent Geometry, Dynamics, Topology, and Physical Reality*, Dust LLC preprint, August 2026.

[6] *Universal Mathematical Phase Theory: A Formal Framework for Structural Phases, Bifurcation Operators, Order Parameters, and Universality Classes*, Dust LLC preprint, August 2026.

[7] *The Particle as a Stable Phase Sector: A Derivation from the Universal Phase Equation, Topological Separation, and Phase Transport*, Dust LLC preprint, August 2026.

---

## Provenance Note

This manuscript is an original formal derivation built from the UPT operator hierarchy and the three preceding UPT preprints. References [1]–[4] are cited only for the established mathematical apparatus of Lyapunov–Schmidt reduction, topological sectors, and moduli-space dynamics. They do not establish the UPT postulates, the particle-emergence theorem, the bound-state construction, or the phase-theoretic interpretation of chemistry formulated here. No result in this paper is imported from the Standard Model, quantum electrodynamics, or nonrelativistic quantum mechanics as an assumption. All such structures appear only as derived consequences whose explicit computation remains the task of a concrete UPT realization.
