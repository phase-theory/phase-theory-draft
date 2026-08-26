# Phase Topology Microscopy of the Hydrogen Atom
## An Inverse Structural Derivation of the Bound Proton–Electron Phase Sector

**Dust LLC — Universal Phase Theory Preprint Series**  
**White Paper / Foundational Preprint**  
**26 August 2026**

---

## Abstract

This paper formulates **Phase Topology Microscopy (PTM) of the hydrogen atom** as an inverse structural theory within Universal Phase Theory (UPT). The hydrogen atom is not introduced as a point proton plus an electron evolving in a prescribed Coulomb potential, nor as a Hilbert-space representation with a spectral table appended to it. It is constructed as the gauge-equivalence class of a stable, finite-excess, two-sector phase configuration,

\[
\mathfrak P_H
=
[\Phi_H]_{\mathscr G_\Phi}
=
[\Phi_p\star\Phi_e]_{\mathscr G_\Phi},
\qquad
\mathscr F[\Phi_H;\lambda_H]=0,
\]

where \(\mathscr F\) is the universal phase equation, \(\star\) is the nonlinear phase-sector composition induced by that equation, and \(\mathscr G_\Phi\) is the admissible phase-frame groupoid. The analysis begins before spatial geometry, gauge fields, particles, electric charge, and quantum state space. It develops the exact conditions under which the bound orbit is reconstructed from invariant response data.

The universal operator hierarchy is retained throughout:

\[
\boxed{
\mathscr F[\Phi;\lambda]=0,
\qquad
\mathscr L_\Phi:=D_\Phi\mathscr F[\Phi;\lambda],
\qquad
\Delta_\Phi:=\operatorname{Det}_{\Phi}(\mathscr L_\Phi),
\qquad
\boldsymbol\chi_\Phi:=
\left(\Pi_N\mathscr L_\Phi\Pi_N\right)^{-1}.
}
\tag{0.1}
\]

Lyapunov–Schmidt reduction generates the finite bound-sector order parameters from \(\ker\mathscr L_{\Phi_{H,c}}\). The projected susceptibility generates an emergent response metric,

\[
 g^{(H)}_{ij}=T^{(H)}_{ia}\chi_H^{ab}T^{(H)}_{jb},
\tag{0.2}
\]

which defines phase distance, localization, and the Green kernel of the derived Abelian connection. The atom is externally neutral when the boundary phase charges cancel, \(Q_H^\infty=Q_p+Q_e=0\), while retaining a nontrivial **relative** topological class and a nontrivial transport holonomy on the bound collective moduli space. This distinction supplies the phase-topological architecture of a neutral atom.

We prove a Hydrogen PTM Reconstruction Theorem: given admissibility, finite phase excess, normal stability, nondegenerate response geometry, collective transportability, and a separating family of gauge-invariant topological, spectral, holonomy, and transition channels, the PTM map reconstructs the hydrogen phase orbit up to its precisely defined observation kernel. We then prove the asymptotic spectral theorem: if the phase response geometry develops a three-dimensional spatial stratum, the derived connection has the required inverse-distance Green asymptotic, and the collective symplectic class is integral, then the bound phase spectrum has the Rydberg form \(E_n\propto -n^{-2}\). Fine, hyperfine, and selection structure are placed in the curvature and holonomy of the same derived connection rather than appended as independently chosen operators.

The result is a formal white paper and a computational research programme. It specifies what UPT derives at the structural level, what an explicit universal phase equation must calculate, and what empirical hydrogen data exclude a candidate realization. The measured ionization threshold, Lyman and Balmer lines, Rydberg scale, and 1S–2S precision interval are treated as targets of the derived phase theory, never as data inserted into \(\mathscr F\). [8] [9] [10]

**Keywords:** Universal Phase Theory; Phase Topology Microscopy; hydrogen atom; phase bundle; susceptibility geometry; Lyapunov–Schmidt reduction; holonomy; relative topology; emergent spectrum; inverse structural theory; atomic phase sector.

---

## Contents

1. [Foundational statement and derivational discipline](#1-foundational-statement-and-derivational-discipline)  
2. [The hydrogen UPT datum and the two-sector solution space](#2-the-hydrogen-upt-datum-and-the-two-sector-solution-space)  
3. [Bifurcation, reduced order parameters, and the bound branch](#3-bifurcation-reduced-order-parameters-and-the-bound-branch)  
4. [Stability, susceptibility, and emergent response geometry](#4-stability-susceptibility-and-emergent-response-geometry)  
5. [Atomic topology: external neutrality and internal relative class](#5-atomic-topology-external-neutrality-and-internal-relative-class)  
6. [The hydrogen phase-topological microscope](#6-the-hydrogen-phase-topological-microscope)  
7. [Reconstruction theorem and observability kernel](#7-reconstruction-theorem-and-observability-kernel)  
8. [Prequantum bound geometry and the hydrogen spectrum](#8-prequantum-bound-geometry-and-the-hydrogen-spectrum)  
9. [Holonomy, transport, and topology-resolved spectroscopy](#9-holonomy-transport-and-topology-resolved-spectroscopy)  
10. [Scale flow and phase images of the atom](#10-scale-flow-and-phase-images-of-the-atom)  
11. [Empirical programme and falsifiability criteria](#11-empirical-programme-and-falsifiability-criteria)  
12. [Research questions and computational closure](#12-research-questions-and-computational-closure)  
13. [Conclusion](#13-conclusion)  
14. [References](#references)

---

## 1. Foundational statement and derivational discipline

Universal Phase Theory takes **phase** as the primitive structural substrate. Geometry, connection, field, particle, and observable are ordered products of stable phase organization rather than independently stipulated layers of ontology. The fundamental hierarchy is therefore

\[
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
\text{observables}.
}
\tag{1.1}
\]

For atomic structure, the hierarchy continues through bound-sector composition:

\[
\Phi
\longrightarrow
\text{stable sectors}
\longrightarrow
\text{bound sector}
\longrightarrow
\text{atomic topology}
\longrightarrow
\text{response geometry}
\longrightarrow
\text{spectroscopy}.
\tag{1.2}
\]

The direction of explanation matters. A conventional atomic construction begins with a spatial manifold, an electromagnetic gauge field, a proton, an electron, and a quantum Hamiltonian. A UPT construction begins with none of these as primitive. Its datum is an admissible generalized phase section and the universal structural equation. The hydrogen atom emerges only when a composed phase configuration is stable, localized, transportable, topologically distinguishable, and reconstructible from invariant channels. This paper specializes the PTM inverse programme to that problem. [1] [2] [3]

> **Definition 1.1 (Hydrogen phase-topology microscopy).** Hydrogen PTM is the scale-indexed inverse map which reconstructs the bound phase-sector orbit \(\mathfrak P_H\) from invariant topological, geometrical, spectral, transport, and transition responses of an admissible configuration.

The paper maintains a strict non-insertion audit. A structure may be used as a **benchmark** after derivation, but it may not be smuggled into the universal equation, its stability operator, its observation map, or its boundary labels. The distinction is mathematical, not rhetorical.

| Structure | Forbidden insertion | Required UPT origin in this paper |
|---|---|---|
| Spatial distance \(r\) | A background Euclidean or Lorentzian metric | Susceptibility metric \(g^{(H)}\) and phase distance \(D_H\) |
| Electron and proton | Primitive point particles or prescribed fields | Stable, finite-excess phase-sector orbits \([\Phi_e]\), \([\Phi_p]\) |
| Coulomb kernel | An external \(-e^2/(4\pi r)\) potential | Green kernel of the derived Abelian phase connection on the physical response stratum |
| Electric charge | A numeric source coefficient | Boundary/relative phase class and derived phase current |
| Spin | A representation appended to a particle label | Holonomy of the derived phase connection |
| Quantum number \(n\) | A preassigned Hilbert-space index | Integral symplectic class of the collective phase geometry |
| Rydberg constant | A fitted spectral parameter | Compound invariant \(R_\Phi\) calculated from \(\mu_\Phi\), \(\kappa_\Phi\), and \(\hbar_\Phi\) |
| Fine and hyperfine terms | Added correction Hamiltonians | Curvature and short-scale response of the full composite phase sector |
| Probabilities | Born weights specified at the starting point | A later phase-invariant operational measure |

This audit makes the white paper falsifiable at its foundation. A candidate \(\mathscr F\) that begins with a chosen gauge group, a known charge table, a Coulomb potential, or measured atomic constants reformulates atomic physics in phase language; it does not derive atomic structure from phase.

---

## 2. The hydrogen UPT datum and the two-sector solution space

Let

\[
\pi_\Phi:E_\Phi\rightarrow\mathcal X
\tag{2.1}
\]

be a generalized phase bundle. The base \(\mathcal X\) is deliberately not assumed to be spacetime or a spatial manifold. Let \(\mathscr G_\Phi\) denote the full admissible phase-frame group, groupoid, or higher automorphism structure, and let \(\mathcal C_\Phi\subseteq\Gamma(E_\Phi)\) be the admissible configuration space. The hydrogen datum is

\[
\boxed{
\mathfrak U_H=
(E_\Phi,\mathscr G_\Phi,\mathcal C_\Phi,\mathcal Y_\Phi,\Lambda,\mathscr F;\Phi_0),
\qquad
\mathscr F:\mathcal C_\Phi\times\Lambda\rightarrow\mathcal Y_\Phi.
}
\tag{2.2}
\]

Here \(\Phi_0\) is a stable vacuum orbit and the solution space is

\[
\mathscr S_\Phi(\lambda)
:=
\{\Phi\in\mathcal C_\Phi:\mathscr F[\Phi;\lambda]=0\}.
\tag{2.3}
\]

Physical content lies in the quotient \(\mathscr S_\Phi/\mathscr G_\Phi\), not in an absolute phase representative. The atomic configuration is a composed orbit

\[
\Phi_H=\n\Phi_p\star\Phi_e,
\qquad
\mathfrak P_H=[\Phi_H]_{\mathscr G_\Phi},
\tag{2.4}
\]

where \(\star\) is a nonlinear composition law induced by the solution structure of \(\mathscr F\). It is not a tensor-product rule assumed from particle quantum mechanics. The operation is defined by the existence of a bound, finite-excess solution in a two-sector neighbourhood of the quotient configuration space.

The component sectors are characterized before they are called proton or electron. A phase orbit \([\Phi_q]\) is an elementary stable sector when it has finite invariant excess, normal stability, a localizable response geometry, and an invariant distinction from the vacuum. The labels \(p\) and \(e\) identify the two sector types that a successful microscopic \(\mathscr F\) must generate at the atomic scale. [2] [3]

If a variational realization exists, the universal equation is the Euler–Lagrange condition of a phase action,

\[
S_\Phi[\Phi;\lambda]
=
\int_{\mathcal X}
\mathcal L_\Phi(\Phi,\nabla\Phi,\ldots;\lambda)
\,d\mu_\Phi,
\qquad
\mathscr F[\Phi;\lambda]
=
\frac{\delta S_\Phi}{\delta\Phi}.
\tag{2.5}
\]

Neither \(d\mu_\Phi\) nor \(\nabla\) presupposes the physical spacetime geometry. They belong to the generalized phase datum. The physical geometry arises later as a stable response structure.

The full UPT hierarchy for the atom is the operator chain

\[
\mathscr F[\Phi;\lambda]=0,
\qquad
\mathscr L_\Phi=D_\Phi\mathscr F[\Phi;\lambda],
\qquad
\Delta_\Phi=\operatorname{Det}_{\Phi}(\mathscr L_\Phi),
\qquad
\boldsymbol\chi_\Phi=
\left(\Pi_N\mathscr L_\Phi\Pi_N\right)^{-1}.
\tag{2.6}
\]

The bifurcation operator \(\Delta_\Phi\) identifies configurations at which the physical normal stability operator loses invertibility. The susceptibility is always a projected inverse: exact phase-frame motions and collective translations do not represent physical divergent response. A theory that inverts \(\mathscr L_\Phi\) before this projection mistakes redundancy for instability. [1] [2]

---

## 3. Bifurcation, reduced order parameters, and the bound branch

Let \(\Phi_{H,c}\) be a critical parent configuration at \(\lambda_c\), satisfying

\[
\mathscr F[\Phi_{H,c};\lambda_c]=0,
\qquad
\Delta_{\Phi_{H,c}}=0,
\qquad
K_H:=\ker\mathscr L_{\Phi_{H,c}}\neq\{0\}.
\tag{3.1}
\]

Assume \(\mathscr L_{\Phi_{H,c}}\) is Fredholm of index zero. The standard Fredholm splitting is

\[
T_{\Phi_{H,c}}\mathcal C_\Phi=K_H\oplus R_H,
\qquad
\mathcal Y_\Phi=K_H^*\oplus R_H^*.
\tag{3.2}
\]

Choose a basis \(e_a\) of \(K_H\) and its dual basis \(e^{*a}\) in the cokernel. Each sufficiently small configuration can be written as

\[
\Phi=
\Phi_{H,c}+\eta^ae_a+\xi,
\qquad
\xi\in R_H.
\tag{3.3}
\]

The range equation

\[
P_R\mathscr F[\Phi_{H,c}+\eta^ae_a+\xi;\lambda]=0
\tag{3.4}
\]

fixes a slaved normal deformation \(\xi=\xi(\eta,\lambda)\). The residual equation is the finite-dimensional hydrogen phase equation

\[
\boxed{
\varphi_H^a(\eta,\lambda)
=
\left\langle e^{*a},
\mathscr F\left[
\Phi_{H,c}+\eta^be_b+\xi(\eta,\lambda);\lambda
\right]\right\rangle=0.
}
\tag{3.5}
\]

The reduced coordinates are not phenomenological order parameters selected after the fact. They are the kernel directions forced by the loss of phase stability. In a local two-sector chart they may be organized as

\[
\eta^a=
\bigl(
\eta_p^\alpha,
\eta_e^\beta,
\eta_{\mathrm{rel}}^A,
\eta_{\mathrm{int}}^r
\bigr),
\tag{3.6}
\]

where \(\eta_{\mathrm{rel}}^A\) becomes a bound collective coordinate only after the response geometry is shown to be physical.

For a variational realization, the reduced equation is the gradient of a reduced phase potential,

\[
\varphi_{H,a}
=
\frac{\partial\mathcal V_{H,\mathrm{red}}}{\partial\eta^a},
\tag{3.7}
\]

with normal form

\[
\mathcal V_{H,\mathrm{red}}
=
\mathcal V_c
+
\frac12A_{ab}(\lambda)\eta^a\eta^b
+
\frac{1}{3!}B_{abc}(\lambda)\eta^a\eta^b\eta^c
+
\frac{1}{4!}C_{abcd}(\lambda)\eta^a\eta^b\eta^c\eta^d
+\cdots.
\tag{3.8}
\]

Every coefficient includes the slaved range contribution \(\xi(\eta,\lambda)\). Consequently a Coulomb-like interaction cannot be declared to be one term in \(\mathcal V_{H,\mathrm{red}}\); the interaction is a calculated contraction of phase derivatives and range response.

> **Proposition 3.1 (Bound-branch construction).** Suppose \(\mathscr F\) is sufficiently differentiable, \(\mathscr L_{\Phi_{H,c}}\) is Fredholm of index zero, and the reduced equation (3.5) has an isolated nonzero solution \(\eta_H(\lambda)\). Then
> \[
> \Phi_H(\lambda)
> =
> \Phi_{H,c}+
> \eta_H^ae_a+
> \xi(\eta_H,\lambda)
> \tag{3.9}
> \]
> is an admissible bound phase branch.

**Proof.** The range equation annihilates the \(R_H^*\) component of \(\mathscr F\). The reduced equation annihilates the cokernel component. Their direct-sum decomposition therefore gives \(\mathscr F[\Phi_H;\lambda]=0\). The nonzero reduced coordinate separates the branch from the critical parent configuration. \(\square\)

Proposition 3.1 produces a candidate atomic sector. It becomes a hydrogen atom only after it is shown to satisfy finite excess, normal stability, localization, transportability, topological distinction, and observational reconstruction.

---

## 4. Stability, susceptibility, and emergent response geometry

Let \(\mathcal Z_H\) be the tangent space to the exact phase-frame orbit and to the collective moduli family of \(\Phi_H\). Select a physical normal complement,

\[
T_{\Phi_H}\mathcal C_\Phi
=
\mathcal Z_H\oplus N_H.
\tag{4.1}
\]

The normal stability operator and susceptibility are

\[
\boxed{
\mathscr L_H^\perp
:=
\Pi_{N_H}\mathscr L_{\Phi_H}\Pi_{N_H},
\qquad
\boldsymbol\chi_H
:=
(\mathscr L_H^\perp)^{-1}.
}
\tag{4.2}
\]

For a conservative phase realization, stability requires

\[
\ker\mathscr L_H^\perp=\{0\},
\qquad
\langle\zeta,\mathscr L_H^\perp\zeta\rangle_\Phi
\geq
\kappa_H\|\zeta\|_\Phi^2,
\qquad
\kappa_H>0,
\tag{4.3}
\]

for every \(\zeta\in N_H\). The finite phase excess is

\[
0<
\mathcal E_\Phi[\Phi_H\mid\Phi_0]
:=
\mathcal E_\Phi[\Phi_H]-\mathcal E_\Phi[\Phi_0]
<\infty.
\tag{4.4}
\]

In the atomic regime, the important structural point is that the normal operator is **not** the direct sum of isolated-sector operators. The two-sector composition has the block form

\[
\mathscr L_H^\perp
=
\begin{pmatrix}
\mathscr L_p^\perp & \mathscr K_{pe}\\
\mathscr K_{ep} & \mathscr L_e^\perp
\end{pmatrix}_{N_H}.
\tag{4.5}
\]

The off-diagonal maps \(\mathscr K_{pe}\) and \(\mathscr K_{ep}\) are the genuine phase binding response. They emerge from the nonlinear composition law; they are not force terms added after the elementary sectors are named.

When \(\mathscr L_p^\perp\) is invertible on the projected physical complement, the effective electron-sector response in the proton background is the Schur complement

\[
\boxed{
\mathscr L_{e\mid p}^{\perp}
=
\mathscr L_e^\perp
-
\mathscr K_{ep}
(\mathscr L_p^\perp)^{-1}
\mathscr K_{pe}.
}
\tag{4.6}
\]

Correspondingly,

\[
\boldsymbol\chi_{e\mid p}
=
\left(
\mathscr L_e^\perp-
\mathscr K_{ep}
(\mathscr L_p^\perp)^{-1}
\mathscr K_{pe}
\right)^{-1}.
\tag{4.7}
\]

Equation (4.6) is a central microscopic statement. It locates the bound-state response in the universal operator hierarchy. Spectral deformation of the electron sector, including finite-core and transport effects, occurs through the exact phase response of the composed configuration. It is not produced by adding a potential to an otherwise isolated electron Hamiltonian.

The same factorization constrains the phase bifurcation operator:

\[
\Delta_H
sim
\operatorname{Det}(\mathscr L_p^\perp)
\operatorname{Det}\!\left(
\mathscr L_e^\perp-
\mathscr K_{ep}(\mathscr L_p^\perp)^{-1}\mathscr K_{pe}
\right),
\tag{4.8}
\]

up to regularization and exact-zero-mode factors. A bound criticality occurs precisely when the effective normal response develops a zero mode. Thus a phase transition in the atom is diagnosed through \(\Delta_H\), not through an externally chosen change in an atomic parameter.

Let \(\lambda^i\) denote branch controls and \(\eta^a\) the reduced phase coordinates. Define

\[
S_{ab}^{(H)}
:=
\frac{\partial^2\mathcal V_{H,\mathrm{red}}}{\partial\eta^a\partial\eta^b},
\qquad
\chi_H^{ab}:=(S_H^{-1})^{ab},
\qquad
T_{ia}^{(H)}
:=
\frac{\partial^2\mathcal V_{H,\mathrm{red}}}{\partial\lambda^i\partial\eta^a}.
\tag{4.9}
\]

Differentiation of the reduced equilibrium equation gives

\[
\frac{\partial\eta^a}{\partial\lambda^i}
=-\chi_H^{ab}T^{(H)}_{ib}.
\tag{4.10}
\]

The emergent response metric is therefore

\[
\boxed{
 g^{(H)}_{ij}
=
T^{(H)}_{ia}\chi_H^{ab}T^{(H)}_{jb}.
}
\tag{4.11}
\]

On the maximal-rank physical stratum, phase distance is defined by

\[
D_H(\lambda_1,\lambda_2)
=
\inf_{\gamma:\lambda_1\to\lambda_2}
\int_\gamma
\sqrt{g^{(H)}_{ij}\,d\lambda^i d\lambda^j}.
\tag{4.12}
\]

Localization means concentration of a gauge-invariant phase-excess density \(\varepsilon_H\) in finite phase distance from a collective centre \(X_H\):

\[
\int_{\{x:D_H(x,X_H)>R\}}
|\varepsilon_H(x)|\,d\mu_{g_H}
\longrightarrow0
\qquad
(R/\ell_H\rightarrow\infty).
\tag{4.13}
\]

The atom is consequently not a point placed at a position. It is an extended phase sector whose invariant excess becomes localized in a geometry generated by its own response.

---

## 5. Atomic topology: external neutrality and internal relative class

The topology of an elementary sector is encoded by the asymptotic phase map and by characteristic data of the derived phase connection. Let

\[
\mathcal A_H=\mathcal A[\Phi_H]
\tag{5.1}
\]

be the connection generated by the bound configuration, with curvature

\[
\mathcal F_H
=
d\mathcal A_H+
\mathcal A_H\wedge\mathcal A_H.
\tag{5.2}
\]

For a sector \(q\), an asymptotic Abelian phase invariant can be represented in a residual Abelian regime by

\[
Q_q
=
\frac{1}{2\pi}
\int_{\Sigma_2}
\operatorname{tr}_{\rho_q}(\mathcal F_q)
\in\mathbb Z,
\tag{5.3}
\]

or, in fully equivariant notation, by a relative orbit class

\[
q(\Phi_q)
\in
[\partial_\infty\mathcal X,\mathscr V]_{\mathscr G_\Phi},
\tag{5.4}
\]

where \(\mathscr V\) is the vacuum orbit manifold.

The hydrogen composition is externally neutral when the boundary sum map annihilates the sector pair,

\[
Q_H^\infty
=
Q_p+Q_e
=0.
\tag{5.5}
\]

This relation does not annihilate the atom’s microscopic topology. The correct bound invariant is relative data on the collective moduli manifold \(\mathcal M_{H,\mathrm{rel}}\):

\[
\boxed{
\vartheta_H
\in
H^2\!\left(
\mathcal M_{H,\mathrm{rel}},
\partial\mathcal M_{H,\mathrm{rel}};
\mathbb Z
\right)
\quad\text{or}\quad
[\mathcal A_H]_{\mathrm{rel}}
\in
\mathrm{Hol}(\mathcal M_{H,\mathrm{rel}})/\mathrm{conj}.
}
\tag{5.6}
\]

The exterior boundary channel records net far-field phase flux. The relative channel records how the component sectors are assembled inside the bound configuration. These are distinct functorial images of the phase bundle. Neutrality is therefore compatible with an internally nontrivial phase topology.

> **Proposition 5.1 (Neutrality–topology separation).** If \(Q_p+Q_e=0\), then \(Q_H^\infty=0\). This condition does not imply \(\vartheta_H=0\) or trivial relative holonomy.

**Proof.** The exterior class is the image of sector data under a boundary-sum homomorphism. The relative class lies in the relative cohomology or holonomy quotient of the collective moduli pair. The corresponding maps have distinct kernels. Cancellation of the boundary image therefore places no requirement that the relative class vanish. \(\square\)

This proposition is the topological core of hydrogen PTM. A neutral atom does not disappear from phase microscopy; it changes the channel through which its structure is visible. Exterior charge response cancels, while internal holonomy, relative topology, spectral response, and curvature remain available to the observation map.

The stability and topology conditions are independent.

| Protection mechanism | Mathematical condition | Atomic role | Insufficient by itself for |
|---|---|---|---|
| Relative topological separation | \(\vartheta_H\neq\vartheta_0\), or an inequivalent relative holonomy class | Prevents continuous identification with the vacuum or an unbound trivial configuration under admissible finite-excess deformation | A stable localized representative |
| Normal spectral protection | \(\mathscr L_H^\perp\geq\kappa_H>0\) on the physical complement | Prevents normal growth of bound-sector perturbations | A nontrivial topological identity |
| Finite phase excess | \(0<\mathcal E_\Phi[\Phi_H\mid\Phi_0]<\infty\) | Excludes delocalized background redefinitions | Discrete internal structure |
| Integral collective class | \([\Omega_H/(2\pi\hbar_\Phi)]\in H^2(\mathcal M_{H,\mathrm{rel}},\mathbb Z)\) | Supports global phase quantization | A derived probability measure |

---

## 6. The hydrogen phase-topological microscope

PTM reverses the forward UPT hierarchy. The forward process is

\[
\Phi
\rightarrow
\text{topology}
\rightarrow
\text{geometry}
\rightarrow
\text{connection}
\rightarrow
\text{field}
\rightarrow
\text{particle}
\rightarrow
\text{observable}.
\tag{6.1}
\]

The hydrogen microscope performs the inverse structural reconstruction,

\[
\text{invariant atomic observations}
\rightarrow
\text{response geometry}
\rightarrow
\text{topology and holonomy}
\rightarrow
\text{stable bound sector}
\rightarrow
[\Phi_H]_{\mathscr G_\Phi}.
\tag{6.2}
\]

Let \(\rho_\ell\) be a scale-dependent coarse-graining of phase configurations. The scale \(\ell\) is a resolution parameter of phase response; it is not a spatial ruler assumed before geometry. Let \(\mathcal A_H\) be a family of invariant observation channels. The hydrogen PTM operator is

\[
\boxed{
\mathfrak M_{H,\ell}:
\mathscr S_{H,\mathrm{st}}/\mathscr G_\Phi
\longrightarrow
\mathcal D_H(\ell),
\qquad
\mathfrak M_{H,\ell}([\Phi_H])
=
\bigl(\mathcal O^{(\ell)}_A[\Phi_H]\bigr)_{A\in\mathcal A_H}.
}
\tag{6.3}
\]

Gauge invariance is mandatory:

\[
\mathcal O_A^{(\ell)}[g\cdot\Phi]
=
\mathcal O_A^{(\ell)}[\Phi],
\qquad
g\in\mathscr G_\Phi.
\tag{6.4}
\]

A minimal hydrogen channel algebra is

\[
\begin{aligned}
\mathcal O_{\mathrm{top},\ell}
&=
\bigl(Q_H^\infty,\vartheta_H,\mathrm{SF}_\ell\bigr),\\
\mathcal O_{\mathrm{geom},\ell}
&=
\bigl(g^{(H)}_\ell,\operatorname{Ric}[g^{(H)}_\ell],D_{H,\ell}\bigr),\\
\mathcal O_{\mathrm{spec},\ell}
&=
\sigma_{\mathrm{disc}}(\mathscr L_H^\perp)
\cup
\sigma(\widehat{\mathcal H}_{H,\ell}),\\
\mathcal O_{\mathrm{hol},\ell}
&=
\left\{
\operatorname{conj}
\mathcal P\exp\left(-\oint_\gamma\mathcal A_H\right)
\right\}_{\gamma},\\
\mathcal O_{\mathrm{tr},\ell}
&=
\left\{
\langle\psi_f,\widehat{\mathcal J}_{B,\ell}\psi_i\rangle
\right\}_{i,f,B}.
\end{aligned}
\tag{6.5}
\]

The channels have different reconstruction functions.

| Channel | Invariant response | Reconstructed phase content |
|---|---|---|
| Topological | Relative class, boundary class, spectral flow | Sector distinction, neutrality, and protected internal phase organization |
| Geometric | Susceptibility metric, curvature, phase distance | Localization, dimensional stratum, and response-volume growth |
| Spectral | Projected normal and collective spectra | Stability gap, bound ladder, continua, and internal modes |
| Holonomy | Conjugacy classes of loop transport | Residual representation data and curvature response |
| Transition | Gauge-invariant matrix elements | Observable line algebra and selection structure |
| Scale | Coarse-grained images and response flow | Persistence, fusion, erasure, and decoupling of phase structures |

Two orbits are observationally indistinguishable at scale \(\ell\) precisely when

\[
[\Phi_1]\sim_{\mathrm{obs},\ell}[\Phi_2]
\quad\Longleftrightarrow\quad
\mathfrak M_{H,\ell}([\Phi_1])
=
\mathfrak M_{H,\ell}([\Phi_2]).
\tag{6.6}
\]

The PTM image at finite resolution is therefore the exact ambiguity class

\[
\mathfrak P_{\mathrm{obs},\ell}([\Phi_H])
:=[\Phi_H]_{\sim_{\mathrm{obs},\ell}},
\tag{6.7}
\]

not an unjustified single microscopic representative.

![Figure 1. Phase Topology Microscopy reconstruction hierarchy for hydrogen. The vertical chain displays the UPT derivation from phase section to falsifiable atomic observation. The side branches separate neutral exterior response from persistent internal relative topology.](https://private-us-east-1.manuscdn.com/sessionFile/HaSuHPpgxwXEfLnGBXAjcu/sandbox/Q1239orNcdZ21ZVLlP3kUX-images_1787734905018_na1fn_L2hvbWUvdWJ1bnR1L3VwdF9oeWRyb2dlbl93aGl0ZV9wYXBlci9oeWRyb2dlbl9wdG1faGllcmFyY2h5.png?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvSGFTdUhQcGd4d1hFZkxuR0JYQWpjdS9zYW5kYm94L1ExMjM5b3JOY2RaMjFaVkxsUDNrVVgtaW1hZ2VzXzE3ODc3MzQ5MDUwMThfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwzVndkRjlvZVdSeWIyZGxibDkzYUdsMFpWOXdZWEJsY2k5b2VXUnliMmRsYmw5d2RHMWZhR2xsY21GeVkyaDUucG5nIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzg5NDMwNDAwfX19XX0_&Key-Pair-Id=K2QY5QTL8JSY6C&Signature=MEUCIBrCEwsXWKdHAwVErQSpfF8znLiEGkTV7nZk00Y-t0BSAiEAgN~as7-4nXlFK82I~44yk0wcjZ8cDsnAwogBuGfy2x8_)

*Figure 1. The bound hydrogen orbit is reconstructed only after the stable two-sector composition generates its own susceptibility geometry, connection, relative topology, spectrum, and gauge-invariant observation map.*

---

## 7. Reconstruction theorem and observability kernel

Define the stable finite-excess hydrogen sector space by

\[
\mathscr S_{H,\mathrm{st}}
:=
\left\{
\Phi_H\in\mathscr S_\Phi:
\begin{array}{l}
0<\mathcal E_\Phi[\Phi_H\mid\Phi_0]<\infty,\\
\mathscr L_H^\perp\text{ is normally stable},\\
\Phi_H\text{ is localized in }g^{(H)},\\
\Phi_H\text{ admits a smooth collective moduli family}
\end{array}
\right\}.
\tag{7.1}
\]

> **Theorem 7.1 (Hydrogen Phase Topology Microscopy Reconstruction).** Let \(\mathfrak U_H\) be a hydrogen UPT datum and let \([\Phi_H]\in\mathscr S_{H,\mathrm{st}}/\mathscr G_\Phi\). Suppose that:
>
> 1. **Admissibility:** \(\mathscr F[\Phi_H;\lambda_H]=0\).
> 2. **Bound-sector separation:** the orbit has nontrivial relative topological data \(\vartheta_H\neq\vartheta_0\), or is isolated from the vacuum/unbound sector by a calculated normal spectral invariant.
> 3. **Finite phase excess:** equation (4.4) holds.
> 4. **Normal stability:** equation (4.3), or the appropriate stable dynamical analogue, holds after projection.
> 5. **Response geometry:** \(g^{(H)}\) is nondegenerate on the physical localization stratum.
> 6. **Localization and transportability:** equations (4.12)–(4.13) define finite localization and the collective kinetic tensor is nondegenerate.
> 7. **Observation completeness:** equality of all channels in a separating family \(\mathcal A_{H,\mathrm{sep}}\) identifies two stable bound orbits only up to the residual observation kernel.
>
> Then \(\mathfrak M_{H,\ell}\) reconstructs \(\mathfrak P_H=[\Phi_H]_{\mathscr G_\Phi}\) up to that residual kernel. If the kernel is trivial on \(\mathscr S_{H,\mathrm{st}}/\mathscr G_\Phi\), the reconstruction is unique.

**Proof.** Admissibility puts \(\Phi_H\) in the quotient solution space. The separation condition prevents collapse to the vacuum orbit or to an unbound phase-sector class. Finite excess rules out a delocalized redefinition of the background. Normal stability makes the susceptibility bounded on the physical complement, preserving the orbit under small normal deformation. The nondegenerate response metric defines phase distance; localization concentrates the invariant excess within finite distance. Transportability supplies a smooth family of physically inequivalent collective configurations. The topological, geometric, spectral, holonomy, and transition channels separate exactly those quotient distinctions which they resolve. Equality of all separating channels leaves only the observation kernel. If the kernel is identity, no residual ambiguity remains. \(\square\)

> **Corollary 7.2 (Atomic objecthood).** A hydrogen atom is a particle-like object in UPT precisely as the reconstructed bound orbit \(\mathfrak P_H\), not as a primitive point source or a stipulated two-body state.

The theorem gives a controlled inverse interpretation of atomic data. Spectral lines alone do not reconstruct an orbit unless their observation kernel is understood. Topological and holonomy channels alone do not fix localization unless the response geometry is computed. A valid atomic microscope combines these channels rather than declaring any one of them to be the atom.

> **Proposition 7.3 (Finite-resolution separation).** If the Jacobian of \(\mathfrak M_{H,\ell}\) restricted to the physical normal quotient has full rank at \([\Phi_H]\), then sufficiently small phase-sector perturbations are locally distinguishable at resolution \(\ell\).

**Proof.** Full rank makes the observation map an immersion on a local quotient chart. The inverse-function theorem gives local separation of nearby quotient points. \(\square\)

This is a local criterion. Global uniqueness still requires that separated distant phase sectors not share the complete observation signature.

---

## 8. Prequantum bound geometry and the hydrogen spectrum

A discrete atomic spectrum requires more than a stable classical bound phase configuration. The collective relative phase manifold must possess a symplectic structure derived from phase transport. Let

\[
\Omega_H
\in
\Omega^2(\mathcal M_{H,\mathrm{rel}})
\tag{8.1}
\]

be its closed nondegenerate two-form. Quantization occurs when the period class is integral:

\[
\boxed{
\left[
\frac{\Omega_H}{2\pi\hbar_\Phi}
\right]
\in
H^2(\mathcal M_{H,\mathrm{rel}},\mathbb Z).
}
\tag{8.2}
\]

The integrality condition yields a prequantum line bundle

\[
L_H\longrightarrow\mathcal M_{H,\mathrm{rel}},
\qquad
F_{\nabla^{L_H}}
=-\frac{i}{\hbar_\Phi}\Omega_H.
\tag{8.3}
\]

An admissible polarization or an equivalent phase-selection principle then defines the emergent state section space. The atomic quantum label is not placed in a Hilbert-space basis at the start; it enters through the global period structure of the bound collective geometry. [1] [4]

The derived connection determines the long-range phase Green kernel. On a physical response stratum with three-dimensional asymptotic volume growth, the Green equation is

\[
\Delta_{g_H}G_H(x,x')
=-\delta_{g_H}(x,x'),
\qquad
G_H(x,x')
\sim
\frac{1}{4\pi D_H(x,x')}.
\tag{8.4}
\]

The inverse-distance form is not assumed. It is the diagnostic consequence of a three-dimensional emergent response geometry. The phase interaction is then

\[
V_H[D_H]
=-\kappa_\Phi G_H
\sim
-\frac{\kappa_\Phi}{4\pi D_H},
\tag{8.5}
\]

where \(\kappa_\Phi\) is a calculated coupling invariant of the composed phase branch. A normalization convention may absorb \(4\pi\) into \(\kappa_\Phi\); no physical conclusion is changed.

The covariant collective Hamiltonian has the structural form

\[
\boxed{
\widehat{\mathcal H}_H
=
-
\frac{\hbar_\Phi^2}{2\mu_\Phi}
\Delta_{g_H}^{\nabla^{L_H}}
+
V_H[D_H]
+
\widehat{\mathcal H}_{\mathrm{hol}}
+
\widehat{\mathcal H}_{\mathrm{core}}.
}
\tag{8.6}
\]

Here \(\mu_\Phi\) is the derived relative inertia on the collective phase manifold, \(\widehat{\mathcal H}_{\mathrm{hol}}\) is curvature/holonomy response, and \(\widehat{\mathcal H}_{\mathrm{core}}\) is the short-scale response inherited from the composite phase branch. All are functionals of the same phase solution and its projected stability operator.

> **Theorem 8.1 (Asymptotic hydrogen spectral law).** Suppose the universal phase equation produces: (i) a three-dimensional physical response stratum; (ii) the Green asymptotic (8.4); (iii) an integral symplectic class (8.2); and (iv) an asymptotic inverse-distance collective potential \(V_H=-\kappa_\Phi/D_H+o(D_H^{-1})\). Then the scalar bound-sector spectrum is
> \[
> E_n^{(0)}
> =
> -
> \frac{\mu_\Phi\kappa_\Phi^2}{2\hbar_\Phi^2}
> \frac{1}{n^2},
> \qquad n\in\mathbb N.
> \tag{8.7}
> \]
> Its transition wavenumbers are
> \[
> \widetilde\nu_{n_i\to n_f}
> =
> R_\Phi
> \left(
> \frac{1}{n_f^2}-\frac{1}{n_i^2}
> \right),
> \qquad
> R_\Phi
> :=
> \frac{\mu_\Phi\kappa_\Phi^2}{2hc\hbar_\Phi^2}.
> \tag{8.8}
> \]

**Proof.** The volume-growth condition fixes the radial Green asymptotic of the response Laplacian. The derived connection thereby supplies the inverse-distance relative interaction. Integrality of \(\Omega_H/(2\pi\hbar_\Phi)\) supplies a globally consistent prequantum line bundle. Separation of the covariant radial equation with regularity at the phase origin and normalizable decay at phase infinity yields discrete principal classes \(n\in\mathbb N\) and the eigenvalues in (8.7). Taking differences gives (8.8). \(\square\)

The theorem does not permit the numerical Rydberg scale to be a fitted entry. The compound invariant \(R_\Phi\) must be calculated from the phase equation. The measured Rydberg constant, \(R_\infty=10\,973\,731.568\,157(12)\,\mathrm{m}^{-1}\), is therefore a high-precision target for the derived asymptotic phase sector. [9]

The full threshold is fixed by the complete phase response, not only by the asymptotic scalar law:

\[
E_{\mathrm{ion}}^{(H)}
=
\mathcal E_\Phi[\Phi_p\mid\Phi_0]
+
\mathcal E_\Phi[\Phi_e\mid\Phi_0]
-
\mathcal E_\Phi[\Phi_H\mid\Phi_0]
+
\delta E_{\mathrm{core}}+
\delta E_{\mathrm{hol}}.
\tag{8.9}
\]

For neutral protium, the empirical target is \(13.598433\,\mathrm{eV}\), or \(109678.7717\,\mathrm{cm}^{-1}\), for the ground-state ionization energy. [8]

---

## 9. Holonomy, transport, and topology-resolved spectroscopy

The derived connection permits comparison of phase configurations along loops of the collective moduli manifold. For \(\gamma\subset\mathcal M_{H,\mathrm{rel}}\), define

\[
\mathscr U_\gamma
=
\mathcal P\exp\left(-\oint_\gamma\mathcal A_H\right).
\tag{9.1}
\]

Its conjugacy class is gauge invariant. Internal labels are therefore transport data of the phase bundle, not primitive particle indices. Curvature is

\[
\mathscr R_H
=
[\nabla^{L_H},\nabla^{L_H}]
=
\mathcal F_H.
\tag{9.2}
\]

Fine, hyperfine, and finite-core sensitivity occupy a single structural location in UPT: the curvature and short-scale response of the composed phase sector. For a multiplet state \(\psi_{n\alpha}\), the leading line-structure correction is

\[
\delta E_{n\alpha}
=
\left\langle
\psi_{n\alpha},
\bigl(
\widehat{\mathcal H}_{\mathrm{hol}}[\mathscr R_H]
+
\widehat{\mathcal H}_{\mathrm{core}}[\Phi_p,\Phi_e]
\bigr)
\psi_{n\alpha}
\right\rangle
+
O(\mathscr R_H^2).
\tag{9.3}
\]

This relation establishes the derivational obligation. The full internal phase connection must calculate the observed splitting pattern from the same \(\mathscr F\) that generated the basic bound orbit. A table of spin couplings inserted after the spectrum is obtained is not a UPT derivation.

The selection algebra is likewise a holonomy statement. Let \(H_H\) denote the residual transport stabilizer, and let \(\rho_i\), \(\rho_f\), and \(\rho_B\) represent initial state, final state, and observation channel. A gauge-invariant transition amplitude has the form

\[
\mathfrak A_{fi}[B]
=
\langle\psi_f,\widehat{\mathcal J}_B\psi_i\rangle.
\tag{9.4}
\]

> **Proposition 9.1 (Holonomy selection rule).**
> \[
> \mathfrak A_{fi}[B]=0
> \quad\text{unless}\quad
> \operatorname{Hom}_{H_H}
> \left(
> \rho_f,
> \rho_B\otimes\rho_i
> \right)
> \neq\{0\}.
> \tag{9.5}
> \]

**Proof.** A physical transition amplitude is an invariant scalar. Such a scalar exists exactly when the tensor product of the final dual representation, channel representation, and initial representation contains the trivial representation. This condition is equivalent to the nonvanishing intertwiner space in (9.5). \(\square\)

The ordinary angular-momentum selection rules are the low-energy coordinatization of this theorem only after the residual transport group and its representations are calculated from the phase bundle. The theorem therefore reverses the conventional order: holonomy creates the representation content that later appears as an atomic selection table.

Collective transport is also derived. If \(z^A\) are collective moduli of the phase family \(\Phi_H(\cdot;z)\), the induced kinetic tensor is

\[
\gamma_{AB}(z)
=
\int_{M_{\mathrm{eff}}}
\left\langle
\partial_A\Phi_H,
\mathscr W_{\Phi_H}\partial_B\Phi_H
\right\rangle_\Phi
\,d\mu_{g_H}.
\tag{9.6}
\]

When \(\gamma\) is nondegenerate, the adiabatic collective equation is

\[
\ddot z^A+
\Gamma^A{}_{BC}[\gamma]\dot z^B\dot z^C
=
\gamma^{AB}\mathscr F^{\mathrm{hol}}_{BC}\dot z^C+\cdots.
\tag{9.7}
\]

A point trajectory is then the infrared image of an extended atomic phase configuration. It is not the starting ontology of the atom. [2] [4]

---

## 10. Scale flow and phase images of the atom

UPT Postulate X imposes scale dependence:

\[
\Phi\longrightarrow\Phi_\ell.
\tag{10.1}
\]

Hydrogen PTM is consequently not a single image but a compatible family,

\[
\operatorname{Img}_{\mathrm{PTM}}(\Phi_H)
:=
\left\{
\mathfrak M_{H,\ell}([\Phi_H])
\right\}_{\ell\in\mathfrak L}.
\tag{10.2}
\]

For \(\ell_1<\ell_2\), a coherent microscope satisfies

\[
\mathfrak M_{H,\ell_2}
=
\mathcal R_{\ell_2\leftarrow\ell_1}
\circ
\mathfrak M_{H,\ell_1},
\tag{10.3}
\]

where \(\mathcal R\) is the renormalization map on observation data. The associated topological flow is

\[
\Theta_{\ell_2}(\Phi_H)
=
\mathcal T_{\ell_2\leftarrow\ell_1}
\bigl(
\Theta_{\ell_1}(\Phi_H),
 g^{(H)}_{\ell_1},
\mathscr L_{H,\ell_1}^\perp
igr).
\tag{10.4}
\]

The scale interpretation is exact.

| Scale event | Mathematical signature | Hydrogen PTM meaning |
|---|---|---|
| Topological persistence | \(\vartheta_{H,\ell_2}=\vartheta_{H,\ell_1}\) | The bound relative class remains resolved |
| Sector fusion | Several short-scale classes have one coarse image | Proton substructure appears as a single atomic core sector |
| Topological erasure | A nontrivial class maps to the vacuum image | A microscopic distinction is unresolved in the available atomic channel |
| Spectral decoupling | \(\omega_n(\ell)\) leaves the observation band | An internal phase mode remains in the exact sector but is not observed as an atomic line |
| Critical enlargement | \(\kappa_H(\ell)\to0\) | Susceptibility diverges and the atomic image approaches a phase transition |
| Holonomy crossover | Conjugacy class or curvature response changes under \(\mathcal T\) | A new selection or splitting regime becomes visible |

> **Proposition 10.1 (Visibility threshold).** An isolated normal or collective mode is PTM-visible at scale \(\ell\) only if its spectral projector remains separated from the continuum by a positive gap and its frequency lies in the observation band of \(\mathfrak M_{H,\ell}\).

This distinguishes the existence of phase structure from its finite-resolution visibility. A microscopic core mode can influence atomic holonomy without appearing as an independently resolvable excitation. Conversely, a proposed UPT correction must show the scale flow that carries it into a measurable line shift, scattering response, or transition threshold.

---

## 11. Empirical programme and falsifiability criteria

Hydrogen is a decisive UPT test sector because its observed spectrum is exceptionally constrained. NIST lists a ground-state ionization energy of \(13.598433\,\mathrm{eV}\) for \(^{1}\mathrm H\), and reports resolved Ritz wavelengths at approximately \(1215\,\text{Å}\), \(6562\,\text{Å}\), and \(4861\,\text{Å}\) for Lyman-\(\alpha\), Balmer-\(\alpha\), and Balmer-\(\beta\), respectively. [8] The CODATA 2022 value of the Rydberg constant has relative standard uncertainty \(1.1\times10^{-12}\). [9] The 1S–2S transition is an especially exacting target: the metastable 2S level has a \(1.3\,\mathrm{Hz}\) natural linewidth and the transition is accessible through two-photon spectroscopy at \(243\,\mathrm{nm}\). [10]

These facts impose a strict benchmark hierarchy on a candidate universal phase equation. They are not calibration values. A parameter choice tuned to them has not generated atomic structure; it has encoded the answer in the input.

| UPT reconstruction channel | Quantity that must be calculated | External benchmark | Failure condition |
|---|---|---|---|
| Sector existence | Explicit \(\Phi_p\), \(\Phi_e\), and \(\Phi_H\) solving one \(\mathscr F\) | Stable hydrogen sector | No finite-excess, normally stable bound branch |
| Exterior phase topology | Boundary sum \(Q_p+Q_e\) | Neutral atomic far-field response | Residual exterior charge after composition |
| Response geometry | \(g_H=T_H\chi_HT_H^{\mathsf T}\), volume growth, and \(G_H\) | Derived inverse-distance binding channel | Prescribed metric or inserted \(1/r\) kernel |
| Principal spectrum | \(R_\Phi=\mu_\Phi\kappa_\Phi^2/(2hc\hbar_\Phi^2)\) | \(R_\infty=10\,973\,731.568\,157(12)\,\mathrm{m}^{-1}\) [9] | Fitted compound invariant or incorrect \(n^{-2}\) ladder |
| Ionization threshold | Complete phase-excess difference | \(13.598433\,\mathrm{eV}\) for \(^{1}\mathrm H\) [8] | Mismatch after all core and holonomy contributions |
| Optical observation map | Covariant transition differences and intertwiners | Lyman-\(\alpha\), Balmer-\(\alpha\), Balmer-\(\beta\) [8] | Wrong line pattern, series limits, or selection algebra |
| Curvature response | \(\mathscr R_H\) and core susceptibility | Fine/hyperfine structure | Inserted spin or correction coefficients |
| Precision sector | Complete bound phase response | 1S–2S precision test [10] | Incompatibility with the observed precision interval |
| Predictive scale flow | \(\mathcal T_{\ell_2\leftarrow\ell_1}\) | A quantitative unmeasured response | Reproduction only by fitted known quantities |

The criteria are logically independent.

> **Criterion A — Universal admissibility.** A concrete \(\mathscr F\) must generate the elementary and bound phase branches without a particle field, a Coulomb potential, or a background spacetime metric as input.

> **Criterion B — Topological derivation.** Charge-like and neutral-composite data must be computed as invariant boundary and relative classes of the phase bundle. Integer labels assigned at the start are not derived topology.

> **Criterion C — Geometric derivation.** The susceptibility metric must have a calculated physical stratum, signature, localization scale, and Green kernel. An arbitrary metric terminates the phase-geometry derivation.

> **Criterion D — Spectral stability.** The projected operator \(\mathscr L_H^\perp\) must have the required stable normal spectrum. Exact gauge and collective zero modes must be removed before the spectrum is interpreted.

> **Criterion E — Atomic spectrum.** One and the same phase equation must calculate the Rydberg scale, ionization threshold, line series, and internal splittings without independently fitted atomic constants.

> **Criterion F — Transport origin.** The residual holonomy group and all line-selection intertwiners must be calculated from \(\mathcal A_H[\Phi_H]\). A predeclared spin or angular-momentum table fails this criterion.

> **Criterion G — Scale prediction.** The UPT realization must generate at least one quantitative scale-dependent prediction in scattering, line shift, topology, response, or transition structure that is not used to set its parameters.

The first six criteria validate the reconstruction of known hydrogen structure. The seventh establishes predictive status. Without it, a UPT construction remains a structural parametrization rather than an empirically advancing foundational theory.

---

## 12. Research questions and computational closure

The white paper transforms the phrase “phase topology microscopy of hydrogen” into a finite sequence of explicit mathematical computations.

| Research question | Required calculation | Decisive output |
|---|---|---|
| Which phase bundle admits the atomic vacuum? | Classify \(E_\Phi\), \(\mathscr G_\Phi\), \(\mathscr V\), and admissible finite-excess boundary data | An explicit stable vacuum orbit with no inserted physical spacetime |
| Which phase branches are proton and electron sectors? | Solve \(\mathscr F=0\), identify \(\ker\mathscr L\), and perform Lyapunov–Schmidt reduction | Stable, isolated, finite-excess sector orbits |
| Why do they bind? | Calculate the off-diagonal response operators \(\mathscr K_{pe}\), \(\mathscr K_{ep}\) and the Schur complement | A stable composite branch and derived relative interaction |
| Why does an inverse-distance regime occur? | Evaluate \(g_H\), its rank/signature, and its response-Laplacian Green kernel | Three-dimensional asymptotic volume growth and \(D_H^{-1}\) kernel |
| Why is the atom neutral but structured? | Compute boundary and relative cohomology/holonomy invariants | \(Q_H^\infty=0\) with \(\vartheta_H\) or relative holonomy nontrivial |
| Why is the spectrum discrete? | Derive \(\Omega_H\), \(\hbar_\Phi\), its period class, and \(\widehat{\mathcal H}_H\) | A calculated discrete spectral ladder |
| Why are transitions allowed or forbidden? | Compute the residual transport group, representations, and intertwiner algebra | Selection rules from holonomy rather than imported labels |
| Why are internal shifts observed? | Resolve curvature and core response across scales | Fine/hyperfine and finite-core phase images |
| What distinguishes UPT empirically? | Compute \(\mathcal T_{\ell_2\leftarrow\ell_1}\) and a new observable | A quantitative prediction that can be confirmed or excluded |

A numerical implementation must preserve this order. It must first discretize or otherwise represent the phase bundle and gauge quotient, solve the universal equation for vacuum and finite-excess sectors, construct the projected stability operator, and verify normal stability. It must then compute the reduced susceptibility, response metric, connection, topological classes, and observation map. The spectrum is obtained only after these structures exist.

The following computation pipeline is the operational closure of the paper:

\[
\begin{aligned}
&(E_\Phi,\mathscr G_\Phi,\mathscr F)
\;\longrightarrow\;
\Phi_0,\Phi_p,\Phi_e,\Phi_H
\;\longrightarrow\;
\mathscr L_H^\perp,\boldsymbol\chi_H\\
&\longrightarrow\;
 g_H,\mathcal A_H,\mathcal F_H
\;\longrightarrow\;
(\vartheta_H,\Omega_H,\mathcal M_{H,\mathrm{rel}})
\;\longrightarrow\;
\widehat{\mathcal H}_H,\mathfrak M_{H,\ell}
\;\longrightarrow\;
\text{spectra, line data, and new predictions}.
\end{aligned}
\tag{12.1}
\]

No arrow may be reversed by empirical insertion. In particular, the measured Rydberg scale may validate \(R_\Phi\), but it may not determine the phase parameters that are then claimed to generate it.

---

## 13. Conclusion

Phase Topology Microscopy of the hydrogen atom treats the atom as a reconstructible phase object. Its defining entity is

\[
\boxed{
\mathfrak P_H
=
[\Phi_p\star\Phi_e]_{\mathscr G_\Phi},
\qquad
\mathscr F[\Phi_H;\lambda_H]=0.
}
\tag{13.1}
\]

The result is not a re-description of the conventional atom in unfamiliar words. It fixes the mathematical order in which atomic structure is allowed to enter a foundational theory. The universal phase equation supplies admissibility. Its derivative supplies the stability operator. The projected inverse supplies susceptibility. Susceptibility generates response geometry. Geometry supports phase distance and localization. Derived connections supply curvature and holonomy. Relative topology distinguishes the internally structured neutral composite. Integral collective phase geometry supports a discrete spectrum. Gauge-invariant response channels reconstruct the atomic orbit.

The central conclusions are these. First, a neutral atom can be externally topologically trivial while internally carrying a nontrivial relative phase class; neutrality is a boundary statement, not the absence of phase organization. Second, the physical binding response is located in the off-diagonal blocks and Schur complement of the full projected phase stability operator. Third, the inverse-distance regime and Rydberg spectrum are conditional consequences of a three-dimensional susceptibility geometry, a derived connection, and an integral collective symplectic class. Fourth, fine, hyperfine, and selection structure belong to holonomy and curvature of the same phase configuration. Fifth, PTM reconstructs the atom only up to its calculable observation kernel, thereby excluding false microscopic uniqueness.

Hydrogen now supplies a sharp boundary for UPT. A viable universal phase equation must produce the stable proton and electron sectors, their neutral bound composition, the emergent response geometry, the full spectral hierarchy, and at least one novel quantitative result without importing particle content, gauge data, metric structure, or measured atomic constants. The theory is confirmed or excluded at that level of calculation.

---

## References

[1] Dust LLC, *Universal Phase Theory: A Foundational Mathematical Framework for Phase Structure, Emergent Geometry, Dynamics, Topology, and Physical Reality*, supplied manuscript, August 2026. [Source file](file:///home/ubuntu/upload/UniversalPhaseTheory(2).md)

[2] Dust LLC, *The Particle as a Stable Phase Sector: A Derivation from the Universal Phase Equation, Topological Separation, and Phase Transport*, supplied manuscript, August 2026. [Source file](file:///home/ubuntu/upload/TheParticleasaStablePhaseSector(2).md)

[3] Dust LLC, *Nucleons, Electrons, and Atomic Phase Structure: A Derivation from the Universal Phase Equation, Phase Transport, and Bound Phase-Sector Geometry*, supplied manuscript, August 2026. [Source file](file:///home/ubuntu/upload/Nucleons,Electrons,andAtomicPhaseStructure.md)

[4] Dust LLC, *Phase Topology Microscopy: An Inverse Structural Theory for Reconstructing Stable Phase Sectors from Relational Observables*, supplied manuscript, August 2026. [Source file](file:///home/ubuntu/upload/PhaseTopologyMicroscopy(1).md)

[5] Dust LLC, *Universal Mathematical Phase Theory: A Formal Framework for Structural Phases, Bifurcation Operators, Order Parameters, and Universality Classes*, supplied manuscript. [Source file](file:///home/ubuntu/upload/UniversalMathematicalPhaseTheory(2).md)

[6] E. Zeidler, *Nonlinear Functional Analysis and Its Applications I: Fixed-Point Theorems*, Springer, 1986. The Lyapunov–Schmidt/Fredholm reduction is used here as a structural reduction of the UPT phase equation. [Publisher record](https://link.springer.com/book/9781461261938)

[7] N. M. J. Woodhouse, *Geometric Quantization*, 2nd ed., Oxford University Press, 1997. The prequantum integrality condition is used here only as the relevant mathematical template for the derived collective phase bundle. [Publisher record](https://global.oup.com/academic/product/geometric-quantization-9780198502702)

[8] National Institute of Standards and Technology, *Atomic Data for Hydrogen (H)*. The reference lists \(^{1}\mathrm H\) energy data and resolved Ritz wavelengths, including the quoted ionization energy and principal Lyman/Balmer benchmarks. [NIST Atomic Data](https://physics.nist.gov/PhysRefData/Handbook/Tables/hydrogentable1.htm)

[9] National Institute of Standards and Technology, *CODATA Value: Rydberg Constant*, 2022 CODATA recommended values. [NIST CODATA](https://physics.nist.gov/cgi-bin/cuu/Value?ryd)

[10] Max Planck Institute of Quantum Optics, *1S–2S Absolute Frequency Measurement*. [MPQ Hydrogen Spectroscopy](https://www.mpq.mpg.de/6503711/1s2stransition)
