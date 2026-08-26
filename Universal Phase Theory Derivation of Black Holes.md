# Universal Phase Theory Derivation of Black Holes

## Phase Defects, Emergent Causal Boundaries, Topological Sectors, and Horizon Thermodynamics

**Universal Phase Theory Research Series**  
**Comprehensive White Paper — August 2026**  
**Prepared for Dust LLC**

---

## Abstract

Universal Phase Theory (UPT) takes phase configuration, rather than spacetime geometry or matter fields, as the primitive structural datum. This paper develops the black-hole sector of that program. A black hole is derived as a **stable compact phase-defect sector** whose response geometry contains a future outer causal boundary. The derivation begins with a phase bundle \(\pi:E_\Phi\to\mathcal X\), a universal phase field \(\Phi\in\Gamma(E_\Phi)\), and the universal phase equation

\[
\mathscr F[\Phi;\lambda]=0.
\]

Its linearization is the phase stability operator \(\mathscr L_\Phi=D_\Phi\mathscr F\), its critical locus is controlled by \(\Delta_\Phi=\operatorname{Det}_{\Phi}(\mathscr L_\Phi)\), and its stable response is governed by the susceptibility \(\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}\). A Lorentzian effective geometry arises when the reduced phase characteristic polynomial factorizes through a non-degenerate hyperbolic response form. A future outer phase-trapping boundary is then the codimension-one locus on which the outgoing expansion of the induced phase-area form vanishes, the ingoing expansion is negative, and the outward stability derivative is negative. Under an asymptotic phase-vacuum condition, that quasi-local boundary generates a global phase-event horizon.

The mechanism of formation is a phase bifurcation. At a critical configuration \(\Phi_c\), a nontrivial kernel of \(\mathscr L_{\Phi_c}\) supplies the black-hole order parameters. Lyapunov–Schmidt reduction turns the infinite-dimensional universal phase equation into a finite-dimensional reduced horizon equation. The normal form fixes the formation universality class, branch stability, and critical scaling. The phase defect is classified by relative homotopy, cohomological charge, and phase holonomy; its exterior mass, angular momentum, and gauge charges are phase Noether charges. Horizon thermodynamics follows from the covariant phase current and a phase boundary entropy. The Bekenstein–Hawking coefficient and Hawking temperature emerge when the UPT phase sector satisfies, respectively, an induced area-density condition and a regular Euclidean phase-holonomy/KMS condition.

The resulting ontology is

\[
\boxed{
\Phi
\;\longrightarrow\;
\text{topological phase sector}
\;\longrightarrow\;
\text{response geometry}
\;\longrightarrow\;
\text{phase connection}
\;\longrightarrow\;
\text{horizon field structure}
\;\longrightarrow\;
\text{black-hole excitation}
\;\longrightarrow\;
\text{observable mass, charge, entropy, and radiation}.
}
\]

The construction identifies which aspects of black-hole structure follow from the UPT operator hierarchy and which require explicit sector conditions. It thereby converts the black-hole problem from a postulate of curved spacetime into a classification problem for stable phase configurations.

**Keywords:** Universal Phase Theory, black holes, emergent spacetime, phase defects, trapping horizons, bifurcation, Lyapunov–Schmidt reduction, phase holonomy, Noether charge, horizon entropy.

---

## 1. Statement of the Problem

Black-hole physics is usually formulated after a Lorentzian manifold, a metric, a causal cone, and a gravitational field equation have already been supplied. In that formulation, a horizon is a geometric boundary in spacetime and the black hole is classified by the geometry it supports. UPT reverses the order of construction. It asks for the phase configuration whose stable organization generates a causal geometry with a compact no-escape boundary.

The primary black-hole question is therefore not

\[
\text{Which metric solves a gravitational field equation?}
\]

but

\[
\boxed{
\text{Which admissible and stable phase configurations induce a causal response geometry containing a compact outer trapping sector?}
}
\]

This change of starting point is material. A metric, an event horizon, a surface gravity, an area, and a mass are all observables or effective structures in the UPT hierarchy. They are not primitive inputs. The supplied UPT foundational manuscript fixes the underlying postulates: phase primacy, structural configuration, admissibility, stability, transition, emergence, topological protection, universality, relational observability, and scale dependence [1].

The present paper derives the black-hole architecture in five stages. First, it constructs an effective Lorentzian response geometry from the stability spectrum and phase susceptibility. Second, it defines a UPT black hole as a phase-defect sector characterized by a future outer phase-trapping boundary. Third, it establishes formation by Lyapunov–Schmidt reduction at a phase bifurcation. Fourth, it identifies the topological, bundle-theoretic, and Noether-charge data that label the defect. Fifth, it derives the horizon first law, entropy, and temperature in the phase description and states the conditions under which those quantities reproduce the established effective geometric relations of black-hole mechanics [2] [3] [4] [5].

> **Definition 1.1 — UPT black hole.** A UPT black hole is an admissible phase configuration \(\Phi_{\mathrm{BH}}\) for which the induced response geometry possesses a compact, stable, future outer phase-trapping hypersurface \(\mathcal H_\Phi\), separating a non-escapable phase sector from an asymptotic phase vacuum, and for which the configuration carries a nontrivial invariant phase-defect class or a dynamically isolated phase-charge sector.

The definition contains no primitive metric. The response geometry and the causal boundary are constructed functionals of \(\Phi\).

| Layer | UPT object | Black-hole meaning | Status |
|---|---|---|---|
| Primitive | \(\Phi\in\Gamma(E_\Phi)\) | Generalized phase configuration | Postulate I–II |
| Admissibility | \(\mathscr F[\Phi;\lambda]=0\) | Allowed defect configuration | Postulate III |
| Stability | \(\mathscr L_\Phi\), \(\Delta_\Phi\), \(\boldsymbol\chi_\Phi\) | Formation threshold and stable branch | Postulates IV–V |
| Topology | \([\Phi]\), \(Q_{\mathrm{top}}\), \(\operatorname{Hol}_\Phi\) | Defect protection and discrete labels | Postulate VII |
| Geometry | \(g^\Phi_{\mu\nu}=\mathcal G_{\mu\nu}[\Phi]\) | Effective causal cone, area, curvature | Postulate VI |
| Boundary | \(\mathcal H_\Phi\) | Phase-trapping / effective horizon | Derived after geometry |
| Observables | \(E_\Phi,J_\Phi,Q_\Phi,S_\Phi,T_\Phi\) | Mass, spin, charge, entropy, temperature | Postulate IX |

---

## 2. Universal Phase Data and the Non-Insertion Principle

Let \(\mathcal X\) be a differentiable, stratified, or generalized base domain. It is not assumed to be a physical spacetime. Let

\[
\pi:E_\Phi\longrightarrow \mathcal X
\]

be a phase bundle with fiber \(\mathcal M_\Phi\), structure group \(\mathscr G_\Phi\), and configuration space \(\mathcal C_\Phi=\Gamma(E_\Phi)\). A physical phase state is an admissible orbit in the quotient

\[
\mathcal P_\Phi=\mathcal C_\Phi/\mathscr G_\Phi.
\]

The universal equation is a smooth equivariant section

\[
\mathscr F:\mathcal C_\Phi\times\Lambda\longrightarrow\mathcal Y_\Phi,
\qquad
\mathscr F[\Phi;\lambda]=0,
\tag{2.1}
\]

where \(\Lambda\) is the control manifold and \(\mathcal Y_\Phi\) is the target bundle of phase constraints. For a variational realization, \(\mathscr F=\delta S_\Phi/\delta\Phi\), but no particular phase action is needed for the local bifurcation analysis.

At a solution \(\Phi_0\), variation gives

\[
\mathscr F[\Phi_0+\varepsilon\psi;\lambda]
=
\varepsilon\,\mathscr L_{\Phi_0}\psi+O(\varepsilon^2),
\qquad
\mathscr L_{\Phi}:=D_\Phi\mathscr F[\Phi;\lambda].
\tag{2.2}
\]

The phase bifurcation functional and susceptibility are

\[
\Delta_\Phi:=\operatorname{Det}_{\Phi}(\mathscr L_\Phi),
\qquad
\boldsymbol\chi_\Phi:=\left.\mathscr L_\Phi^{-1}\right|_{(\ker\mathscr L_\Phi)^\perp},
\tag{2.3}
\]

with \(\operatorname{Det}_{\Phi}\) understood as the appropriate Fredholm determinant, spectral determinant, Evans function, or spectral-flow invariant. The phase-critical set is

\[
\Sigma_\Phi=\{\Phi\in\mathcal C_\Phi:\Delta_\Phi=0\}.
\tag{2.4}
\]

The non-insertion principle is exact: the following objects are forbidden as primitive assumptions in a UPT derivation of black holes,

\[
\boxed{
(g_{\mu\nu},\;\mathcal H,\;A_{\mathcal H},\;\kappa,\;M,\;G,\;S_{\mathrm{BH}}).
}
\tag{2.5}
\]

They may occur only as derived functionals, matching parameters, or effective limits. A phase action may contain internal bilinear forms, bundle representations, and local response coefficients; none is a spacetime metric unless the phase construction itself maps it to one.

| Quantity | UPT derivation route | Forbidden shortcut |
|---|---|---|
| Lorentzian metric | Hyperbolic phase response and induced coframe | Postulating a background Lorentzian manifold |
| Horizon | Vanishing outgoing phase expansion | Declaring \(r=2GM/c^2\) at the outset |
| Mass | Asymptotic phase Noether/Hamiltonian charge | Inserting a Schwarzschild mass parameter |
| Surface gravity | Inaffinity of the induced horizon generator | Assigning \(\kappa\) from a metric ansatz |
| Entropy | Phase boundary microstate/Noether charge | Postulating \(A/4G\hbar\) |
| Hawking temperature | Euclidean phase holonomy or KMS response | Identifying temperature with \(\kappa\) without the quantum condition |

---

## 3. Emergent Response Geometry

### 3.1 Critical polarizations and phase response

Let \(\{e_a\}\) be a local frame of the dynamically relevant phase-polarization bundle \(K_\Phi\subset T_\Phi\mathcal C_\Phi\). In a stable sector, the response of the phase configuration to a control displacement is measured by

\[
T_{\mu a}[\Phi]
:=
\big\langle e_a,\nabla_\mu\Phi\big\rangle_\Phi,
\tag{3.1}
\]

where \(\nabla\) is a connection on \(E_\Phi\) and \(\langle\cdot,\cdot\rangle_\Phi\) is an invariant fiber pairing. The susceptibility response tensor is

\[
\mathsf G^{\Phi}_{\mu\nu}
:=
T_{\mu a}\,\chi^{ab}\,T_{\nu b},
\qquad
\chi^{ab}:=\langle e^a,\boldsymbol\chi_\Phi e^b\rangle_\Phi.
\tag{3.2}
\]

Equation (3.2) is the UPT metric precursor. It measures the structural distinguishability of neighboring phase configurations. Its singular loci occur at phase-critical surfaces because a soft phase mode produces a divergent or non-analytic response.

A metric requires more than a symmetric response form. Let the relevant phase polarization split as

\[
K_\Phi=K^-_\Phi\oplus K^+_\Phi,
\tag{3.3}
\]

with one distinguished negative response direction and \(d-1\) positive directions. The signature form induced by the spectral projectors \(\Pi_\pm\) is

\[
\mathfrak h_\Phi(u,v)
:=-\langle\Pi_-u,\Pi_-v\rangle_\Phi
+\langle\Pi_+u,\Pi_+v\rangle_\Phi.
\tag{3.4}
\]

Choose a phase coframe map \(\mathcal E^A{}_a[\Phi]\) satisfying

\[
e^A{}_{\mu}[\Phi]
:=
\mathcal E^A{}_a[\Phi]\,T_{\mu}{}^a,
\qquad
A=0,\ldots,d-1.
\tag{3.5}
\]

The effective response metric is then

\[
\boxed{
 g^{\Phi}_{\mu\nu}
:=
 h_{AB}^{\Phi}\,e^A{}_{\mu}e^B{}_{\nu},
\qquad
h_{AB}^{\Phi}=\operatorname{diag}(-1,+1,\ldots,+1),
}
\tag{3.6}
\]

where the signature in \(h^\Phi\) is the normalized image of the phase spectral splitting (3.4), not an independently posited spacetime metric. The conformal normalization of \(g^\Phi\) is fixed by a phase clock or response calibration. Thus causal time is the negative phase-response direction selected by the stable vacuum.

### 3.2 Hyperbolicity criterion

The response tensor is geometrically meaningful only if the reduced phase propagation is hyperbolic. Let \(\mathscr L^{\mathrm{red}}_\Phi\) denote the stability operator after gauge and constrained phase directions are removed. Let its principal symbol be

\[
\sigma_p(\mathscr L^{\mathrm{red}}_\Phi)(x,k).
\]

The **phase hyperbolicity condition** is the factorization

\[
\det\sigma_p(\mathscr L^{\mathrm{red}}_\Phi)(x,k)
=
C_\Phi(x,k)
\bigl(g^{\Phi\,\mu\nu}k_\mu k_\nu\bigr)^r,
\qquad C_\Phi(x,k)\neq0,
\tag{3.7}
\]

on an open sector \(\mathcal U_\Phi\subset\mathcal X\). The null covectors of the effective geometry are therefore the characteristic covectors of phase propagation.

> **Proposition 3.1 — Emergent causal geometry.** Suppose that the coframe map (3.5) has rank \(d\), the spectral form (3.4) has Lorentzian signature, and the reduced principal symbol satisfies (3.7). Then the quotient of \(\mathcal U_\Phi\) by phase-redundant directions possesses a Lorentzian effective manifold \(M_{\mathrm{eff}}[\Phi]\) with metric \(g^\Phi\). Its null cones coincide with the characteristic cones of the reduced universal phase equation.
>
> **Proof.** Rank \(d\) gives a non-degenerate coframe, (3.4) gives a bilinear form of signature \((-+\cdots+)\), and (3.6) therefore defines a Lorentzian metric. Equation (3.7) identifies its null polynomial with the characteristic polynomial of the dynamical phase operator. Hence propagation, causal reachability, and phase signal cones are governed by \(g^\Phi\). \(\square\)

This proposition is the decisive transition from phase structure to causal geometry. It does not assert that every phase configuration is spacetime-like. It isolates the **Lorentzian phase sector** in which a black-hole definition becomes available.

### 3.3 Phase transport and induced connection

Phase comparison between neighboring fibers is governed by

\[
D_\mu\Phi=\partial_\mu\Phi+\mathcal A_\mu[\Phi]\cdot\Phi,
\tag{3.8}
\]

with curvature

\[
\mathcal F_{\mu\nu}[\Phi]
=[D_\mu,D_\nu]
=
\partial_\mu\mathcal A_\nu-
\partial_\nu\mathcal A_\mu+
[\mathcal A_\mu,\mathcal A_\nu].
\tag{3.9}
\]

The induced affine connection is defined by coframe compatibility,

\[
\nabla^{\Phi}_{\mu}e^A{}_{\nu}
:=
\partial_\mu e^A{}_{\nu}
+\omega^{A}{}_{B\mu}[\Phi]e^B{}_{\nu}
-\Gamma^{\Phi\rho}{}_{\mu\nu}e^A{}_{\rho}=0.
\tag{3.10}
\]

When phase torsion vanishes in the effective sector, \(\Gamma^\Phi\) is the Levi–Civita connection of \(g^\Phi\). When it does not vanish, the torsion is an observable phase-transport defect and contributes to the effective exterior dynamics.

```mermaid
flowchart LR
    P[Universal phase field Φ] --> F[Admissibility equation F[Φ;λ]=0]
    F --> L[Stability operator LΦ]
    L --> C[Susceptibility χΦ and critical kernel]
    C --> G[Response coframe and metric gΦ]
    G --> H[Phase connection and causal cones]
    H --> T[Future outer phase-trapping boundary HΦ]
    T --> O[Mass, charge, entropy, temperature]
```

---

## 4. Phase-Defect Definition of a Black Hole

### 4.1 Phase-area form and expansions

Let \(\mathcal S\subset M_{\mathrm{eff}}[\Phi]\) be a compact codimension-two surface. The induced phase metric is

\[
q^{\Phi}_{AB}
:=
(g^\Phi)_{\mu\nu}E_A{}^\mu E_B{}^\nu,
\tag{4.1}
\]

where \(E_A\) spans \(T\mathcal S\). The phase-area form is

\[
\varepsilon^{\Phi}_{\mathcal S}
:=
\sqrt{\det q^\Phi}\,d^{d-2}y,
\qquad
A_\Phi[\mathcal S]
:=
\int_{\mathcal S}\varepsilon^{\Phi}_{\mathcal S}.
\tag{4.2}
\]

Let \(\ell^\mu_\Phi\) and \(n^\mu_\Phi\) be the future-directed outgoing and ingoing null normals, normalized by

\[
g^\Phi_{\mu\nu}\ell^\mu_\Phi n^\nu_\Phi=-1.
\tag{4.3}
\]

The **phase expansions** are entirely induced phase observables,

\[
\Theta^{\Phi}_{(\ell)}
:=
\frac{1}{\sqrt{q^\Phi}}\mathcal L_{\ell_\Phi}\sqrt{q^\Phi}
=
\frac12q_\Phi^{AB}\mathcal L_{\ell_\Phi}q^\Phi_{AB},
\tag{4.4}
\]

\[
\Theta^{\Phi}_{(n)}
:=
\frac{1}{\sqrt{q^\Phi}}\mathcal L_{n_\Phi}\sqrt{q^\Phi}
=
\frac12q_\Phi^{AB}\mathcal L_{n_\Phi}q^\Phi_{AB}.
\tag{4.5}
\]

Every quantity in (4.4)–(4.5) is a functional of \(\Phi\), \(D\Phi\), and \(\boldsymbol\chi_\Phi\) through the response metric and induced connection.

> **Definition 4.1 — Future outer phase-trapping surface.** A compact surface \(\mathcal S\) is future outer phase trapped if
>
> \[
> \Theta^{\Phi}_{(\ell)}=0,
> \qquad
> \Theta^{\Phi}_{(n)}<0,
> \qquad
> \mathcal L_{n_\Phi}\Theta^{\Phi}_{(\ell)}<0.
> \tag{4.6}
> \]
>
> A hypersurface \(\mathcal H_\Phi\) foliated by such surfaces is a future outer phase-trapping horizon.

The last inequality is the phase version of outward stability: moving inward converts the marginal surface into a trapped surface, while moving outward restores escape. Once an effective metric exists, Definition 4.1 is a future outer trapping-horizon condition in the quasi-local sense used in established black-hole dynamics [3]. The difference is ontological: here the trapping structure is induced by phase response rather than assumed as an initial spacetime property.

### 4.2 Interior, exterior, and global phase event horizon

The local phase-trapping definition is sufficient for formation and dynamics. A global boundary requires an asymptotic phase vacuum \(\Phi_\infty\) with a well-defined asymptotic characteristic region \(\mathscr I^+_\Phi\). Let

\[
\mathcal B_\Phi
:=
M_{\mathrm{eff}}[\Phi]\setminus J^-_\Phi(\mathscr I^+_\Phi)
\tag{4.7}
\]

be the non-escapable phase basin. Its boundary

\[
\mathcal E_\Phi:=\partial\mathcal B_\Phi
\tag{4.8}
\]

is the **phase-event horizon**. The causal relation \(J^-_\Phi\) is generated by the characteristic cones in Proposition 3.1. Therefore the global horizon is not a separate geometric insertion; it is the phase-propagation boundary of the asymptotic sector.

> **Proposition 4.2 — Phase-trapping correspondence.** On a Lorentzian phase sector satisfying Proposition 3.1, every future outer phase-trapping horizon \(\mathcal H_\Phi\) is an effective future outer trapping horizon of \(g^\Phi\). If the exterior tends to a complete asymptotic phase vacuum and no outward phase-characteristic from the trapped region reaches \(\mathscr I^+_\Phi\), \(\mathcal H_\Phi\) lies inside or coincides with \(\mathcal E_\Phi\).
>
> **Proof.** Equations (4.4)–(4.6) are the standard null-expansion conditions evaluated in the induced response geometry. Hyperbolicity identifies phase propagation with causal propagation. The global conclusion follows from the definition of \(\mathcal B_\Phi\). \(\square\)

### 4.3 Black holes as phase defects

Let \(\mathcal D_\Phi\) be a compact phase core and \(\mathcal V_\Phi=M_{\mathrm{eff}}\setminus\mathcal D_\Phi\) the exterior. A localized phase defect obeys

\[
\Phi\vert_{\partial\mathcal V_\Phi}\longrightarrow\Phi_\infty,
\qquad
[\Phi]\neq[\Phi_\infty]
\quad\text{in an admissible relative phase class}.
\tag{4.9}
\]

The relevant classification is generally relative rather than absolute:

\[
[\Phi]\in\pi_{d-1}(\mathcal M_\Phi,\mathcal M_{\Phi,\infty})
\quad\text{or}\quad
[\Phi]\in H^{d-1}(\mathcal V_\Phi,\partial\mathcal V_\Phi;\mathbb Z),
\tag{4.10}
\]

with the specific degree determined by the codimension and phase target. The defect charge is

\[
Q_{\mathrm{top}}[\Phi]
:=
\int_{\mathcal C}\Phi^*\omega_{\mathrm{top}},
qquad
d\omega_{\mathrm{top}}=0,
\tag{4.11}
\]

for a linking cycle \(\mathcal C\) and a representative closed phase form \(\omega_{\mathrm{top}}\).

A black-hole phase sector need not be protected solely by a nonzero integer charge. It can instead be dynamically isolated by a gap in the phase stability spectrum or by a disconnected component of the admissible quotient. The complete defect condition is therefore

\[
\boxed{
\text{black-hole sector}
=
\text{compact future outer phase-trapping sector}
\cap
\bigl(
\text{topologically protected}
\;\cup\;
\text{spectrally isolated}
\bigr).
}
\tag{4.12}
\]

---

## 5. Formation by Phase Bifurcation

### 5.1 Critical phase configuration

A black hole forms when an admissible non-trapping phase branch loses stability or when a defect branch becomes globally dominant. Let \(\Phi_c\) satisfy

\[
\mathscr F[\Phi_c;\lambda_c]=0,
\qquad
\ker\mathscr L_{\Phi_c}=K_c\neq\{0\},
\qquad
\Delta_{\Phi_c}=0.
\tag{5.1}
\]

Choose a basis \(\{e_a\}_{a=1}^k\) of \(K_c\) and split the configuration and target spaces as

\[
T_{\Phi_c}\mathcal C_\Phi=K_c\oplus R_c,
\qquad
\mathcal Y_\Phi=\operatorname{coker}\mathscr L_{\Phi_c}\oplus\operatorname{Ran}\mathscr L_{\Phi_c}.
\tag{5.2}
\]

Write

\[
\Phi=\Phi_c+\eta^ae_a+w,
\qquad w\in R_c.
\tag{5.3}
\]

Let \(P\) project onto the cokernel and \(Q=1-P\). The range equation

\[
Q\mathscr F[\Phi_c+\eta^ae_a+w;\lambda]=0
\tag{5.4}
\]

is solved locally by \(w=W(\eta,\lambda)\). Substitution gives the reduced phase equation

\[
\boxed{
\varphi_A(\eta,\lambda)
:=
P_A\mathscr F[\Phi_c+\eta^ae_a+W(\eta,\lambda);\lambda]=0,
}
\tag{5.5}
\]

where \(A=1,\ldots,\dim\operatorname{coker}\mathscr L_{\Phi_c}\). The black-hole order parameters are the components of \(\eta\) that couple to the trapping functional.

### 5.2 The reduced horizon functional

Define the outgoing phase-expansion functional on the reduced branch by

\[
\mathfrak T(\eta,\lambda)
:=
\Theta^{\Phi(\eta,\lambda)}_{(\ell)},
\qquad
\Phi(\eta,\lambda)=\Phi_c+\eta^ae_a+W(\eta,\lambda).
\tag{5.6}
\]

The local black-hole formation system is

\[
\varphi_A(\eta,\lambda)=0,
\qquad
\mathfrak T(\eta,\lambda)=0,
\qquad
\Theta^{\Phi(\eta,\lambda)}_{(n)}<0,
qquad
\mathcal L_{n_\Phi}\Theta^{\Phi(\eta,\lambda)}_{(\ell)}<0.
\tag{5.7}
\]

Thus horizon formation is not an added boundary condition. It is a codimension-enhanced solution of the reduced universal phase equation.

Near \((\eta,\lambda)=(0,\lambda_c)\),

\[
\varphi_A
=
M_{Ai}\,\delta\lambda^i
+\frac12B_{Aab}\eta^a\eta^b
+\frac16C_{Aabc}\eta^a\eta^b\eta^c
+O(\|\eta\|^4,\|\delta\lambda\|\,\|\eta\|),
\tag{5.8}
\]

and

\[
\mathfrak T
=
\tau_i\,\delta\lambda^i+
\tau_a\eta^a+
\frac12\tau_{ab}\eta^a\eta^b+\cdots.
\tag{5.9}
\]

The tensors \(M\), \(B\), \(C\), and \(\tau\) are calculable jets of the universal phase equation and the response metric functional. They define the local formation universality class.

> **Proposition 5.1 — Bifurcation derivation of a phase horizon.** Suppose \(\mathscr L_{\Phi_c}\) is Fredholm of index zero, (5.4) is solvable on \(R_c\), and the augmented map \((\varphi,\mathfrak T)\) has a transverse zero satisfying the final two inequalities in (5.7). Then a branch of admissible phase configurations with a future outer phase-trapping surface bifurcates from \(\Phi_c\).
>
> **Proof.** Lyapunov–Schmidt reduction converts \(\mathscr F=0\) into (5.5). Transversality of the augmented zero set gives a local solution branch by the finite-dimensional implicit-function theorem. The sign conditions in (5.7) are open conditions, hence persist on a sufficiently small branch neighborhood. Definition 4.1 then identifies the resulting hypersurface as a future outer phase-trapping horizon. \(\square\)

### 5.3 One-mode normal form and universal onset scaling

For a simple critical mode \(\eta\in\mathbb R\) and one control \(\mu\), the generic fold normal form is

\[
\varphi(\eta,\mu)
=a(\mu-\mu_c)+b\eta^2+O(\eta^3,(\mu-\mu_c)\eta),
\qquad ab\neq0.
\tag{5.10}
\]

The branches are

\[
\eta_\pm(\mu)
=
\pm\left[-\frac{a}{b}(\mu-\mu_c)\right]^{1/2}
+O(\mu-\mu_c).
\tag{5.11}
\]

If \(\tau_\eta\neq0\), the marginal-trapping condition in (5.9) selects a phase-horizon branch whose order parameter scales as

\[
\eta_{\mathrm{BH}}\sim |\mu-\mu_c|^{1/2}.
\tag{5.12}
\]

Any smooth horizon observable \(\mathcal O_\Phi(\eta)\) with leading coupling \(\partial_\eta\mathcal O_\Phi\neq0\) inherits

\[
\mathcal O_{\mathrm{BH}}-\mathcal O_c
\sim |\mu-\mu_c|^{1/2}.
\tag{5.13}
\]

This is not a claim that every collapse process has exponent \(1/2\). It is the UPT universality prediction for the nondegenerate one-mode fold class. A different kernel representation, symmetry, conservation law, or relevant scale mode produces a different normal form and exponent.

### 5.4 Stability of the black-hole branch

For variational phase dynamics, let \(\mathcal V_{\mathrm{red}}(\eta;\lambda)\) satisfy

\[
\varphi_a=\frac{\partial\mathcal V_{\mathrm{red}}}{\partial\eta^a}.
\tag{5.14}
\]

The reduced stability matrix is

\[
\mathsf H_{ab}^{\mathrm{red}}
:=
\frac{\partial^2\mathcal V_{\mathrm{red}}}{\partial\eta^a\partial\eta^b}.
\tag{5.15}
\]

A branch is phase-stable if \(\mathsf H^{\mathrm{red}}\) is positive on physical order-parameter directions and the horizon deformation operator

\[
\mathcal S_\Phi f
:=
\delta_{f n_\Phi}\Theta^{\Phi}_{(\ell)}
\tag{5.16}
\]

has principal eigenvalue \(\lambda_0(\mathcal S_\Phi)>0\) under the chosen outward convention. The first criterion stabilizes the phase core; the second stabilizes the marginal boundary. Their conjunction defines a stable black-hole phase sector.

---

## 6. Topology, Holonomy, and Black-Hole Quantum Numbers

### 6.1 Relative phase topology

The exterior of a localized defect is characterized by the restriction

\[
\Phi_\infty:\partial\mathcal V_\Phi\longrightarrow\mathcal M_{\Phi,\infty}.
\tag{6.1}
\]

Two defects are phase-equivalent only if an admissible homotopy preserves the asymptotic phase vacuum and does not cross the singular set of the universal phase equation. The topological label is therefore relative:

\[
\mathfrak q_\Phi
in
\pi_{d-1}(\mathcal M_\Phi,\mathcal M_{\Phi,\infty})/\mathscr G_\Phi.
\tag{6.2}
\]

For a closed \((d-2)\)-cycle \(\mathcal C\) linking the core, a cohomological label is

\[
Q_I^{\mathrm{top}}
=
\int_{\mathcal C}\Phi^*\omega_I,
\qquad
[\omega_I]\in H^{d-2}(\mathcal M_\Phi;\mathbb Z).
\tag{6.3}
\]

The integer lattice of \(Q_I^{\mathrm{top}}\) supplies an intrinsic source of discrete black-hole sectors. Such sectors are not assumed to be particle charges; they are classifications of phase-defect configurations.

> **Proposition 6.1 — Topological phase protection.** If \(Q_I^{\mathrm{top}}[\Phi_{\mathrm{BH}}]\neq0\) and the asymptotic phase class is fixed, no continuous admissible deformation can relax \(\Phi_{\mathrm{BH}}\) to the trivial phase vacuum without crossing a singular, non-admissible, or topology-changing configuration.
>
> **Proof.** The integral (6.3) is invariant under smooth admissible homotopies because \(d\omega_I=0\). The trivial vacuum has vanishing relative charge. A deformation connecting the two must therefore leave the admissible homotopy class. \(\square\)

### 6.2 Phase holonomy and exterior charge

The phase connection generates holonomy

\[
\mathcal U_\gamma[\Phi]
=
\mathcal P\exp\left(-\oint_\gamma\mathcal A[\Phi]\right).
\tag{6.4}
\]

For loops \(\gamma\) linking the phase core, the conjugacy class

\[
[\mathcal U_\gamma]\in\operatorname{Conj}(\mathscr G_\Phi)
\tag{6.5}
\]

is gauge invariant. Its class functions, such as \(\operatorname{Tr}\mathcal U_\gamma\), are observable phase transport invariants. In an Abelian sector,

\[
\mathcal U_\gamma=e^{i q_\gamma},
\qquad
q_\gamma=\oint_\gamma\mathcal A,
\tag{6.6}
\]

and quantization can follow from compactness of the phase group or from the integral structure of the phase bundle.

The UPT charge hierarchy is therefore

\[
\boxed{
\text{topological charge}
\;\longrightarrow\;
\text{phase holonomy}
\;\longrightarrow\;
\text{induced connection flux}
\;\longrightarrow\;
\text{effective exterior charge}.
}
\tag{6.7}
\]

This is the phase-theoretic mechanism by which a compact black-hole defect can carry gauge-like charges without introducing a matter field as primitive.

### 6.3 Phase hair and no-hair reduction

Let \(\mathcal I_\Phi\) denote the invariant algebra generated by asymptotic Noether charges, linking holonomies, and cohomological charges. The black-hole exterior is characterized by

\[
\mathfrak H_{\mathrm{ext}}[\Phi]
:=
\{\mathcal O\in\mathcal I_\Phi:\mathcal O\text{ is measurable at }\partial\mathcal V_\Phi\}.
\tag{6.8}
\]

A phase no-hair regime occurs when renormalization or exterior stability drives all but finitely many elements of \(\mathfrak H_{\mathrm{ext}}\) to irrelevant response couplings. A phase-hair regime occurs when a nontrivial holonomy class or boundary mode remains relevant. Thus no-hair behavior is a universality statement about exterior phase response, not an initial assumption.

---

## 7. Effective Exterior Geometry and Classical Limits

### 7.1 Phase field equations for the emergent metric

The induced metric obeys an effective closure equation obtained by varying the phase action or by projecting the universal phase equation onto the response-coframe sector:

\[
\mathcal E_{\mu\nu}[\Phi]
:=
\frac{2}{\sqrt{-g^\Phi}}
\frac{\delta S_\Phi}{\delta g_\Phi^{\mu\nu}}
=0.
\tag{7.1}
\]

The Einstein regime is the particular long-wavelength phase fixed point for which

\[
G_{\mu\nu}[g^\Phi]+\Lambda_{\mathrm{eff}}g^\Phi_{\mu\nu}
=
8\pi G_{\mathrm{eff}}\,T^{\Phi}_{\mu\nu}
+\mathcal C^{\Phi}_{\mu\nu},
\tag{7.2}
\]

where \(\mathcal C^{\Phi}_{\mu\nu}\) contains scale-dependent phase corrections. Equation (7.2) is not assumed in the fundamental UPT layer. It is the explicit matching condition for the phase sector to reproduce an Einstein-like effective limit.

In a static, spherically symmetric, asymptotically vacuum phase sector, the response metric can be written

\[
ds_\Phi^2
=-N_\Phi^2(r)c^2dt^2
+\frac{dr^2}{N_\Phi^2(r)}
+r^2d\Omega^2,
\tag{7.3}
\]

with

\[
N_\Phi^2(r)
=
1-
\frac{2G_{\mathrm{eff}}M_\Phi}{c^2r}
+
\mathcal U_\Phi(r).
\tag{7.4}
\]

Here \(M_\Phi\) is an asymptotic phase charge and \(\mathcal U_\Phi\) is a calculable UPT correction functional determined by the running phase susceptibility, holonomy sector, and non-Einstein response terms. The horizon radius solves

\[
N_\Phi^2(r_{\mathcal H})=0.
\tag{7.5}
\]

The Schwarzschild exterior is the special fixed-point realization

\[
\mathcal U_\Phi(r)=0,
\qquad
r_{\mathcal H}=\frac{2G_{\mathrm{eff}}M_\Phi}{c^2}.
\tag{7.6}
\]

Thus the Schwarzschild radius is not a UPT axiom. It is the root of the response lapse in the Einstein-like phase fixed point.

### 7.2 Phase curvature and core regularization

From the response metric and induced connection, define

\[
R^{\Phi\rho}{}_{\sigma\mu\nu},
\qquad
R^\Phi_{\mu\nu},
qquad
\mathcal R_\Phi,
qquad
\mathcal K_\Phi:=R^{\Phi}_{\mu\nu\rho\sigma}R_\Phi^{\mu\nu\rho\sigma}.
\tag{7.7}
\]

A classical curvature singularity corresponds, in UPT, to a breakdown of the response-coframe map, an unbounded phase susceptibility, or a failure of the phase sector to remain admissible. A regular phase core exists if

\[
\sup_{\mathcal D_\Phi}\|\boldsymbol\chi_\Phi\|<\infty,
\qquad
\inf_{\mathcal D_\Phi}|\det e^A{}_{\mu}|>0,
\qquad
\sup_{\mathcal D_\Phi}\mathcal K_\Phi<\infty.
\tag{7.8}
\]

Equation (7.8) identifies a precise non-singularity program: singularity resolution is achieved neither by deleting the interior nor by inserting a regular metric, but by proving susceptibility saturation and coframe non-degeneracy in the phase core.

---

## 8. Phase Noether Charges and Horizon Mechanics

### 8.1 Covariant phase current

Assume a local phase Lagrangian \(d\)-form \(\mathbf L_\Phi\) with variation

\[
\delta\mathbf L_\Phi
=
\mathbf E_\Phi\cdot\delta\Phi+d\boldsymbol\Theta_\Phi(\Phi,\delta\Phi).
\tag{8.1}
\]

For an infinitesimal phase symmetry generated by \(\xi\), define the phase Noether current

\[
\mathbf J^\Phi_\xi
:=
\boldsymbol\Theta_\Phi(\Phi,\delta_\xi\Phi)
-\iota_\xi\mathbf L_\Phi.
\tag{8.2}
\]

On shell,

\[
d\mathbf J^\Phi_\xi=0,
\qquad
\mathbf J^\Phi_\xi=d\mathbf Q^\Phi_\xi+oldsymbol\xi\cdot\mathbf C_\Phi,
\tag{8.3}
\]

where \(\mathbf C_\Phi\) is the phase constraint form. The asymptotic energy, angular momentum, and gauge charges are boundary integrals of \(\mathbf Q^\Phi\) with the standard symplectic correction:

\[
\delta H^\Phi_\xi
=
\int_{\partial\Sigma}
\left(
\delta\mathbf Q^\Phi_\xi-
\iota_\xi\boldsymbol\Theta_\Phi
right).
\tag{8.4}
\]

This is the UPT origin of black-hole observables. The covariant Noether-charge structure parallels the established effective gravitational construction in which stationary black-hole entropy is a horizon Noether charge [4].

### 8.2 Phase surface gravity

Let \(\xi^\mu_\Phi\) be a stationary horizon generator of \(\mathcal H_\Phi\). Its phase surface gravity is defined through the induced connection,

\[
\xi_\Phi^\nu\nabla^\Phi_\nu\xi_\Phi^\mu
\overset{\mathcal H_\Phi}{=}
\kappa_\Phi\,\xi_\Phi^\mu.
\tag{8.5}
\]

Equivalently, the response lapse obeys

\[
\kappa_\Phi
=
\frac{c^2}{2}
\left.\frac{dN_\Phi^2}{dr}\right|_{r=r_{\mathcal H}}
\tag{8.6}
\]

in the static phase sector (7.3). Since \(N_\Phi\) is derived from \(\Phi\), \(\kappa_\Phi\) is a phase response observable.

### 8.3 Phase entropy and the first law

For a stationary phase horizon with generator normalized to unit \(\kappa_\Phi\), define the covariant phase entropy

\[
S^{\mathrm{cov}}_\Phi
:=
2\pi k_B
\int_{\mathcal S_\Phi}
\mathbf Q^\Phi_{\hat\xi},
\qquad
\hat\xi:=\kappa_\Phi^{-1}\xi_\Phi,
\tag{8.7}
\]

in units where the action is normalized by \(\hbar\). The microscopic phase entropy is

\[
S^{\mathrm{micro}}_\Phi
:=
k_B\log\Omega_\Phi(\mathcal B_\Phi),
\tag{8.8}
\]

where \(\Omega_\Phi(\mathcal B_\Phi)\) is the gauge-reduced count or measure of admissible phase boundary microconfigurations compatible with the macroscopic horizon data \(\mathcal B_\Phi\). The entropy-identification condition is

\[
S^{\mathrm{micro}}_\Phi=S^{\mathrm{cov}}_\Phi+S_{\mathrm{ct}},
\tag{8.9}
\]

where \(S_{\mathrm{ct}}\) denotes fixed renormalization counterterms determined by the phase measure.

For perturbations between stationary phase black holes, the covariant identity (8.4) gives

\[
\boxed{
\delta E_\Phi
=
\frac{\kappa_\Phi}{2\pi k_B}\,\delta S_\Phi
+
\Omega_\Phi\,\delta J_\Phi
+
\sum_I\Psi^I_\Phi\,\delta Q_I^\Phi
+
\delta W_{\mathrm{phase}}.
}
\tag{8.10}
\]

The work term \(\delta W_{\mathrm{phase}}\) contains variations of relevant phase couplings or non-equilibrium response moduli. It vanishes in a fixed-coupling isolated phase sector. Equation (8.10) is the UPT phase first law.

### 8.4 Area law as a phase-state-density result

The horizon area is the phase-area functional \(A_\Phi=A_\Phi[\mathcal S_\Phi]\). The local boundary-state condition is

\[
\log\Omega_\Phi(\mathcal B_\Phi)
=
\alpha_\Phi A_\Phi
+\beta_\Phi\log\left(\frac{A_\Phi}{\ell_\Phi^{d-2}}\right)
+O(A_\Phi^0).
\tag{8.11}
\]

Then

\[
S_\Phi
=
k_B\alpha_\Phi A_\Phi
+k_B\beta_\Phi\log\left(\frac{A_\Phi}{\ell_\Phi^{d-2}}\right)+\cdots.
\tag{8.12}
\]

The effective Bekenstein–Hawking regime is obtained if the induced phase density satisfies

\[
\alpha_\Phi
=
\frac{c^3}{4\hbar G_{\mathrm{eff}}}.
\tag{8.13}
\]

This coefficient is not inserted. It is fixed by the normalization of the phase action, the phase boundary measure, and the long-wavelength coupling \(G_{\mathrm{eff}}\). Equation (8.13) is consequently a non-negotiable matching result for any UPT realization that claims recovery of the semiclassical area law.

### 8.5 Temperature from Euclidean phase holonomy

Analytically continue the stationary phase flow to Euclidean phase time \(\tau_\Phi\). Regularity of the phase coframe at the horizon requires the Euclidean orbit of \(\xi_\Phi\) to close without a conical phase defect:

\[
\beta_\Phi\kappa_\Phi=2\pi.
\tag{8.14}
\]

The equivalent bundle condition is trivialization of the contractible Euclidean phase-time holonomy around the horizon,

\[
\operatorname{Hol}_{\partial D^2}
\bigl(\mathcal A^{E,\Phi}_{\mathrm{time}}\bigr)=\mathbf 1
\quad\Longleftrightarrow\quad
\beta_\Phi\kappa_\Phi=2\pi.
\tag{8.15}
\]

The phase temperature is therefore

\[
\boxed{
T_\Phi
=
\frac{\hbar\kappa_\Phi}{2\pi k_Bc}.
}
\tag{8.16}
\]

A KMS condition for phase correlation functions provides the equivalent Lorentzian characterization. In the effective geometric regime, (8.16) matches the Hawking temperature relation [5]. The regular Euclidean phase-holonomy condition is the UPT derivation of the temperature assignment.

---

## 9. Dynamical Horizons, Entropy Production, and Evaporation

### 9.1 Phase focusing law

The response geometry yields the null phase-focusing identity

\[
\mathcal L_{\ell_\Phi}\Theta^{\Phi}_{(\ell)}
=
-\frac{1}{d-2}\left(\Theta^{\Phi}_{(\ell)}\right)^2
-\sigma^{\Phi}_{\mu\nu}\sigma_\Phi^{\mu\nu}
-\mathcal R^\Phi_{\mu\nu}\ell_\Phi^\mu\ell_\Phi^\nu
+\mathcal T_{\mathrm{tor}}^\Phi,
\tag{9.1}
\]

where \(\mathcal T_{\mathrm{tor}}^\Phi\) contains phase-torsion and non-metric response contributions. In an Einstein-like torsion-free fixed point,

\[
\mathcal R^\Phi_{\mu\nu}\ell_\Phi^\mu\ell_\Phi^\nu
=
8\pi G_{\mathrm{eff}}T^\Phi_{\mu\nu}\ell_\Phi^\mu\ell_\Phi^\nu.
\tag{9.2}
\]

If the total phase flux satisfies

\[
8\pi G_{\mathrm{eff}}T^\Phi_{\ell\ell}-\mathcal T_{\mathrm{tor}}^\Phi\geq0,
\tag{9.3}
\]

a future outer phase-trapping horizon has non-decreasing phase area. This is the UPT condition for the classical second law. The effective trapping-horizon framework likewise relates outer-horizon area variation to a local energy flux [3].

### 9.2 Phase entropy balance

Let \(v\) parameterize the horizon foliation. The entropy balance is

\[
\frac{dS_\Phi}{dv}
=
\frac{1}{T_\Phi}
\left[
\mathcal F_E^\Phi-
\Omega_\Phi\mathcal F_J^\Phi-
\sum_I\Psi^I_\Phi\mathcal F_{Q_I}^\Phi
\right]
+
\Pi_\Phi,
\tag{9.4}
\]

where \(\mathcal F_E^\Phi\), \(\mathcal F_J^\Phi\), and \(\mathcal F_{Q_I}^\Phi\) are phase fluxes across \(\mathcal H_\Phi\), while \(\Pi_\Phi\geq0\) is irreversible phase entropy production generated by coarse-grained mode mixing. The generalized phase second law is

\[
\frac{d}{dv}\left(S_\Phi+S_{\mathrm{ext}}^\Phi\right)\geq0.
\tag{9.5}
\]

### 9.3 Quantum phase leakage

A stationary exterior phase vacuum can acquire nontrivial outgoing correlations when the horizon phase holonomy has thermal periodicity. The outgoing phase number flux has the general form

\[
\langle N_{\omega,I}\rangle_\Phi
=
\frac{\Gamma_{\omega,I}^\Phi}
{\exp\!\left[\hbar\omega/(k_BT_\Phi)\right]\mp1},
\tag{9.6}
\]

where \(\Gamma_{\omega,I}^\Phi\) is a phase-transmission functional and the sign is determined by the effective phase representation. The energy balance becomes

\[
\frac{dE_\Phi}{dt}
=-\mathcal P_{\mathrm{out}}^\Phi+
\mathcal P_{\mathrm{in}}^\Phi,
\tag{9.7}
\]

with the corresponding decrease in horizon area allowed because the outgoing quantum phase flux violates the classical positivity condition (9.3). The standard Hawking result establishes precisely this distinction between classical area monotonicity and the generalized entropy law [5].

---

## 10. What UPT Derives, What Its Realizations Must Supply

The UPT black-hole construction is a derivation in the structural sense: once a phase realization supplies the universal equation and lies in the specified response sector, the horizon, its formation bifurcation, phase charges, and thermodynamic architecture are fixed by the operator hierarchy. A particular numerical exterior or entropy coefficient is fixed only after the realization supplies its microscopic phase action and state measure.

| Result | Derived from UPT hierarchy | Required phase-sector condition | Not inserted by assumption |
|---|---|---|---|
| Stable compact black-hole sector | \(\mathscr F=0\), reduced stability, compact trapping surface | Lorentzian response geometry and outer stability | A metric black hole |
| Causal horizon | Phase characteristic cones and asymptotic vacuum | Hyperbolicity and asymptotic completeness | Event horizon definition in a prior spacetime |
| Formation threshold | \(\ker\mathscr L_{\Phi_c}\neq0\), Lyapunov–Schmidt reduction | Fredholm/transversality conditions | A collapse radius |
| Critical exponent | Reduced normal form | Symmetry and codimension class | A universal numerical exponent |
| Topological sector | Relative homotopy/cohomology, holonomy | Nontrivial target-bundle structure | Charge spectrum |
| Mass and angular momentum | Phase symplectic/Noether boundary charges | Stationary asymptotic phase symmetry | ADM parameters |
| First law | Covariant phase current | Integrable stationary charge sector | Thermodynamic analogy |
| Area scaling | Boundary phase state count | Local extensive boundary density | \(A/4G\hbar\) |
| Hawking temperature | Euclidean phase holonomy / KMS relation | Regular Euclidean response section | \(T\propto\kappa\) |
| Einstein–Schwarzschild limit | Low-energy phase fixed point | Closure equation (7.2), \(\mathcal U_\Phi=0\) | Einstein equations or Schwarzschild geometry |

This distinction gives UPT a direct standard of completion. A candidate universal phase equation is not sufficient because it has a black-hole-like solution. It must calculate the response metric, prove the trapping inequalities, identify the defect class, derive the asymptotic charges, and reproduce or falsify the effective entropy and radiation conditions.

---

## 11. Formal Propositions

> **Theorem 11.1 — Phase black-hole existence theorem.** Let \(\Phi_{\mathrm{BH}}\) solve \(\mathscr F[\Phi;\lambda]=0\). Suppose:
>
> 1. the phase response satisfies the rank, signature, and hyperbolicity conditions of Proposition 3.1;
> 2. \(\Phi_{\mathrm{BH}}\) contains a compact codimension-two surface obeying (4.6);
> 3. the coupled core and horizon stability operators obey \(\mathsf H^{\mathrm{red}}>0\) and \(\lambda_0(\mathcal S_\Phi)>0\);
> 4. the exterior approaches an asymptotic phase vacuum; and
> 5. the configuration is topologically protected or spectrally isolated as in (4.12).
>
> Then \(\Phi_{\mathrm{BH}}\) defines a stable UPT black-hole state. Its effective exterior contains a future outer trapping horizon and, under the no-escape condition, a phase-event horizon.
>
> **Proof.** Condition 1 produces \(M_{\mathrm{eff}}[\Phi]\) and its phase causal cones. Condition 2 produces a future outer phase-trapping horizon by Definition 4.1. Condition 3 prevents a small physical phase perturbation from destabilizing either the core or marginal boundary. Condition 4 permits the global basin definition (4.7). Condition 5 isolates the defect from the trivial phase vacuum. The conclusion follows from Propositions 3.1 and 4.2. \(\square\)

> **Theorem 11.2 — Phase first law.** Let \(\Phi_s\) be a one-parameter family of stationary UPT black holes with an integrable phase symplectic form, fixed phase couplings, and a bifurcate phase horizon generated by \(\xi_\Phi\). Then the phase Hamiltonian variation obeys (8.10) with \(\delta W_{\mathrm{phase}}=0\).
>
> **Proof.** Integrate the on-shell identity (8.4) over a hypersurface bounded by an asymptotic phase sphere and a horizon cross-section. The boundary at infinity defines \(\delta E_\Phi\), \(\delta J_\Phi\), and \(\delta Q_I^\Phi\). The horizon boundary is \(\kappa_\Phi\delta S_\Phi/(2\pi k_B)\) by (8.5)–(8.7). Equality of the two boundary variations yields (8.10). \(\square\)

> **Corollary 11.3 — Einstein fixed-point correspondence.** If the phase closure equation reduces to (7.2) with \(\mathcal C^\Phi_{\mu\nu}=0\), the phase boundary density satisfies (8.13), and the Euclidean phase holonomy condition (8.15) holds, then the UPT black-hole sector reproduces the effective Einstein-horizon first law, Bekenstein–Hawking entropy, and Hawking temperature.

---

## 12. Falsifiability Program

UPT black holes are scientifically constrained by the explicit operator data. Each candidate phase realization supplies a determinate \(\mathscr F\), \(\mathscr L_\Phi\), phase bundle, asymptotic vacuum, and phase measure. The following tests are decisive.

| Test | UPT calculation | Observable consequence | Falsification criterion |
|---|---|---|---|
| Response-geometry test | Compute (3.2)–(3.7) | Causal cones and effective metric | No Lorentzian hyperbolic sector exists |
| Horizon test | Solve (5.7) and evaluate (4.6) | Existence and location of a phase horizon | No compact stable outer-trapping branch occurs |
| Formation universality | Compute jets \(M,B,C,\tau\) | Critical exponents and threshold scaling | Observed/simulated scaling disagrees with the reduced normal form |
| Ringdown spectrum | Locate poles/zeros of \(\mathscr L_\Phi^{-1}\) | Quasinormal response frequencies and damping | Measured spectrum cannot be matched by a single phase operator |
| Phase-hair test | Compute \(\operatorname{Conj}(\mathcal U_\gamma)\) and boundary charges | Extra conserved/near-conserved exterior labels | Required holonomy signatures are absent |
| Entropy test | Derive \(\Omega_\Phi(\mathcal B_\Phi)\) | Area coefficient and logarithmic corrections | \(\alpha_\Phi\neq c^3/(4\hbar G_{\mathrm{eff}})\) in the claimed Einstein regime |
| Temperature test | Verify (8.15) or phase KMS relation | \(T_\Phi=\hbar\kappa_\Phi/(2\pi k_Bc)\) | Thermal correlation periodicity differs |
| Core test | Evaluate (7.8) | Bounded or divergent tidal response | Claimed regular core has unbounded susceptibility or curvature |

The strongest UPT prediction is structural rather than merely parametric: **a black-hole threshold is a phase critical manifold and therefore possesses a calculable universality class**. A realization that merely reproduces an exterior metric but lacks a phase bifurcation operator, a stable defect classification, or a boundary microstate measure has not completed the UPT derivation.

---

## 13. Research Questions

The black-hole sector now reduces to a finite set of formal problems.

| Question | Mathematical task | Completion criterion |
|---|---|---|
| Universal equation | Specify \(\mathscr F[\Phi;\lambda]\) on a concrete phase bundle | Well-posed admissible solution space |
| Lorentzian vacuum | Derive spectral splitting and symbol factorization | Proposition 3.1 holds dynamically |
| Black-hole branch | Perform Lyapunov–Schmidt reduction at \(\Delta_\Phi=0\) | Solve (5.7) with stable outer trapping |
| Defect classification | Compute relative homotopy, cohomology, and holonomy | Classify allowed black-hole sectors |
| Exterior limit | Derive \(\mathcal E_{\mu\nu}[\Phi]\) | Identify \(G_{\mathrm{eff}}\), \(\mathcal U_\Phi\), and deviations |
| Entropy measure | Construct the gauge-reduced phase boundary measure | Derive \(\alpha_\Phi\) and subleading terms |
| Quantum horizon state | Prove Euclidean phase regularity or KMS analyticity | Derive (8.16) and emission spectrum |
| Information transport | Track phase-holonomy correlations through evaporation | Establish unitary or nonunitary phase evolution explicitly |

The program is organized by the same UPT hierarchy at every scale:

\[
\Phi
\rightarrow
\text{phase topology}
\rightarrow
\text{response geometry}
\rightarrow
\text{phase transport}
\rightarrow
\text{effective fields}
\rightarrow
\text{stable black-hole excitation}
\rightarrow
\text{relational observables}.
\tag{13.1}
\]

---

## 14. Conclusion

A black hole in Universal Phase Theory is a stable compact organization of phase. Its defining boundary is not inserted as an event horizon in a pre-existing spacetime. It arises when the universal phase equation admits a phase-defect branch whose induced response geometry contains a future outer trapping hypersurface. The horizon forms at a phase critical set, its local dynamics is governed by Lyapunov–Schmidt reduction, its persistent identity is secured by relative topology or spectral isolation, and its mass, spin, gauge charges, entropy, and temperature are phase observables.

The construction delivers a complete derivational sequence:

\[
\boxed{
\begin{aligned}
&\mathscr F[\Phi;\lambda]=0
\\
&\Longrightarrow\quad
\mathscr L_\Phi=D_\Phi\mathscr F,
\quad
\Delta_\Phi=\operatorname{Det}_{\Phi}(\mathscr L_\Phi),
\quad
\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}
\\
&\Longrightarrow\quad
\ker\mathscr L_{\Phi_c}
\overset{\mathrm{LS}}{\Longrightarrow}
\varphi(\eta,\lambda)=0
\\
&\Longrightarrow\quad
 g^\Phi_{\mu\nu}
=
\mathcal G_{\mu\nu}[\Phi],
\quad
\Theta_{(\ell)}^\Phi=0,
\quad
\Theta_{(n)}^\Phi<0,
\quad
\mathcal L_n\Theta_{(\ell)}^\Phi<0
\\
&\Longrightarrow\quad
\mathcal H_\Phi,
\;[\Phi]_{\mathrm{rel}},
\;\operatorname{Hol}_\Phi,
\;E_\Phi,
\;J_\Phi,
\;Q_\Phi,
\;S_\Phi,
\;T_\Phi.
\end{aligned}
}
\]

UPT thereby replaces the statement “a black hole is a spacetime solution” with the deeper statement:

> **A black hole is a stable, topologically or spectrally isolated phase-defect state whose phase response generates a compact causal no-escape boundary.**

The next stage is not conceptual extension but explicit construction: a concrete universal phase equation must be solved, its phase bundle classified, its reduced black-hole branch calculated, and its entropy and radiation coefficients confronted with observation.

---

## References

<a id="ref-1"></a>[1] **Universal Phase Theory**, *A Foundational Mathematical Framework for Phase Structure, Emergent Geometry, Dynamics, Topology, and Physical Reality*, supplied manuscript, August 2026.

[2] A. Ashtekar and B. Krishnan, [*Isolated and Dynamical Horizons and Their Applications*](https://pmc.ncbi.nlm.nih.gov/articles/PMC5253930/), *Living Reviews in Relativity* **7**, 10 (2004).

[3] S. A. Hayward, [*General Laws of Black-Hole Dynamics*](https://arxiv.org/abs/gr-qc/9303006), *Physical Review D* **49**, 6467 (1994).

[4] R. M. Wald, [*Black Hole Entropy is Noether Charge*](https://arxiv.org/abs/gr-qc/9307038), *Physical Review D* **48**, R3427 (1993).

[5] S. W. Hawking, [*Particle Creation by Black Holes*](https://authors.library.caltech.edu/records/2wsvj-qrt68), *Communications in Mathematical Physics* **43**, 199–220 (1975).

[6] J. M. Bardeen, B. Carter, and S. W. Hawking, [*The Four Laws of Black Hole Mechanics*](https://inspirehep.net/literature/81181), *Communications in Mathematical Physics* **31**, 161–170 (1973).
