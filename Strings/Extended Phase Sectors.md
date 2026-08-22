# Extended Phase Sectors

## A Universal Phase Theory Derivation of Line-Like Excitations, Emergent Geometry, and Gauge Transport

**Dust LLC — Foundational Physics Preprint**  
**August 2026**

---

## Abstract

Universal Phase Theory (UPT) is developed here as a pregeometric theory of **extended phase sectors**. The primitive object is a generalized phase section \(\Phi\in\Gamma(E_\Phi)\) over an underlying relational domain \(\mathcal X\); neither a spacetime metric, a preassigned gauge group, nor an elementary extended object is postulated. Admissible configurations obey the universal phase equation

\[
\mathscr F[\Phi;\lambda]=0,
\]

whose linearization defines the phase stability operator \(\mathscr L_\Phi=D_\Phi\mathscr F\), the phase bifurcation invariant \(\Delta_\Phi=\operatorname{Det}_{\Phi}(\mathscr L_\Phi)\), and, on regular strata, the phase susceptibility \(\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}\). We prove the local reduction of the infinite-dimensional phase equation to a finite-dimensional critical equation by Lyapunov–Schmidt decomposition. The reduced equation supplies order parameters, normal-form tensors, and the local universality class of an emergent sector.

The central result is structural. A line-like excitation is not elementary: it is a codimension-two stable phase sector, defined only after a vacuum manifold, a phase connection, and a finite-energy condition have emerged from \(\Phi\). Its conserved charge is the homotopy class of the vacuum restriction, its transport is governed by phase holonomy, and its tension is the excess phase energy per unit emergent length. Geometry is constructed from response rather than assumed: the tensor \(g^{\Phi}_{ij}=T_{ia}\chi^{ab}T_{jb}\) supplies a phase distinguishability metric on the quotient of control directions. A Lorentzian physical metric, causal cone, Einstein limit, quantum probability rule, observed gauge group, and particle spectrum are consequently not inserted into the framework. They are explicit derivational obligations. The paper states the necessary theorems, the minimal data required for an explicit realization, and falsifiability criteria by which the proposal can fail.

**Keywords:** Universal Phase Theory; emergent geometry; Lyapunov–Schmidt reduction; phase connection; holonomy; topological defect; line-like excitation; phase susceptibility; universality.

---

## 1. Phase-First Formulation

The foundational error of many unification programs is to begin with objects whose origin is the question: a metric, a Hilbert space, a gauge bundle, a collection of particles, or an elementary extended excitation. UPT reverses that order. It begins with a generalized phase configuration and asks which structures are selected as stable, relationally observable organizations of that configuration.

> **Universal Phase Principle.** Every persistent physical structure is a stable relational organization of an admissible phase configuration; every physical transition is a change in the stability, topology, symmetry, or scale-class of that organization.

Let \(\pi_\Phi:E_\Phi\to\mathcal X\) be a phase bundle over a generalized domain \(\mathcal X\). At the foundational level \(\mathcal X\) is only an organizational domain equipped with the minimum differential, categorical, or combinatorial structure required to define local comparison. It is **not** identified with spacetime. A phase state is a section

\[
\Phi\in\mathcal C_\Phi:=\Gamma(E_\Phi),
\qquad
\Phi:\mathcal X\longrightarrow\mathcal M_\Phi,
\]

with \(\mathcal M_\Phi\) permitted to be stratified, non-Abelian, or higher-geometric. The physical configuration space is the quotient

\[
\mathcal P_\Phi=\mathcal C_\Phi/\mathscr G_\Phi,
\]

where \(\mathscr G_\Phi\) is the groupoid of admissible phase-frame transformations. A physical observable is a functional \(\mathcal O[\Phi]\) invariant under this action. Thus absolute phase data are not physical merely because they can be written; only relational invariants survive the quotient.

The paper adopts the complete UPT hierarchy

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
\text{observables}.}
\]

The ordering is not stylistic. It forbids importing a particle catalog in order to explain particles, importing a metric in order to explain geometry, or importing a gauge group in order to explain gauge structure.

| UPT postulate | Operational content in the present construction |
|---|---|
| I. Phase primacy | \(\Phi\), not geometry or matter, is the primitive structural variable. |
| II. Structural configuration | A state is an orbit in \(\mathcal C_\Phi\) under admissible phase transformations. |
| III. Admissibility | Physical configurations solve \(\mathscr F[\Phi;\lambda]=0\). |
| IV. Stability | Persistent structures are spectrally or topologically stable solutions. |
| V. Transition | Phase change occurs at loss of invertibility or exchange of stable branches. |
| VI. Emergence | Geometry, connections, and fields are functionals of \(\Phi\). |
| VII. Topological protection | Charges and sectors arise from invariants of the phase vacuum. |
| VIII. Universality | Infrared structure depends on relevant phase data, not arbitrary microscopic coordinates. |
| IX. Relational observability | Only gauge-invariant and operational phase relations are observable. |
| X. Scale dependence | \(\Phi\mapsto\Phi_\ell\) may change the effective variables and laws. |

The mathematical ingredients used below—Fredholm linearization, Lyapunov–Schmidt reduction, bundle connections, characteristic geometry, and topological classification—are established tools. Their role is reorganized here: they are not independent pieces of physics but successive consequences to be extracted from one universal phase problem [1] [2] [3].

---

## 2. The Universal Phase Equation and Its Operators

### 2.1 Admissibility as a section equation

Let \(\mathcal Y_\Phi\to\mathcal C_\Phi\times\Lambda\) be a target bundle, where \(\Lambda\) is the control manifold. The universal phase equation is a covariant section equation

\[
\boxed{\mathscr F[\Phi;\lambda]=0,\qquad
\mathscr F:\mathcal C_\Phi\times\Lambda\longrightarrow\Gamma(\mathcal Y_\Phi).}
\tag{2.1}
\]

The variables \(\lambda^i\) label admissible deformations, conserved sector data, boundary data, or resolution scale. They are not automatically coordinates of physical spacetime. In a variational realization, one has

\[
S_\Phi[\Phi;\lambda]
 =\int_{\mathcal X}
 \mathcal L_\Phi\bigl(\Phi,\mathfrak D\Phi,\mathfrak D^2\Phi,
 \mathcal I_\Phi;\lambda\bigr)\,d\mu_\Phi,
\qquad
\mathscr F_A=\frac{\delta S_\Phi}{\delta\Phi^A}.
\tag{2.2}
\]

Here \(\mathfrak D\) is an emergent or proto-transport operator, \(\mathcal I_\Phi\) denotes admissible topological densities, and \(d\mu_\Phi\) is a phase measure. Equation (2.2) is a structural template, not an insertion of a spacetime volume form. An explicit UPT realization must construct \(d\mu_\Phi\), \(\mathfrak D\), and \(\mathcal L_\Phi\) from phase data or state exactly which minimal pregeometric data they require.

At a solution \(\Phi_0\), the first variation is

\[
\mathscr F_A[\Phi_0+\varepsilon\varphi;\lambda]
=\varepsilon\,(\mathscr L_{\Phi_0}\varphi)_A+O(\varepsilon^2),
\qquad
(\mathscr L_\Phi)_A{}^{B}:=D_{\Phi^B}\mathscr F_A.
\tag{2.3}
\]

The universal phase stability operator is therefore

\[
\boxed{\mathscr L_\Phi=D_\Phi\mathscr F.}
\tag{2.4}
\]

On a regular phase stratum, the response to a source \(J_A\) is

\[
\mathscr L_\Phi\,\delta\Phi=-J,
\qquad
\delta\Phi^A=-(\boldsymbol\chi_\Phi)^{AB}J_B,
\qquad
\boxed{\boldsymbol\chi_\Phi:=\mathscr L_\Phi^{-1}.}
\tag{2.5}
\]

The inverse is not globally defined. Its failure is physical: it identifies critical directions in which infinitesimal relational perturbations create macroscopic phase reorganization.

### 2.2 Critical strata and phase bifurcation

For a Fredholm stability operator of index zero, define the generalized bifurcation invariant

\[
\boxed{
\Delta_\Phi:=\operatorname{Det}_{\Phi}(\mathscr L_\Phi),
\qquad
\Sigma_\Phi:=\{[\Phi]\in\mathcal P_\Phi:\Delta_\Phi=0\}.}
\tag{2.6}
\]

The determinant is interpreted as the appropriate spectral invariant: a finite determinant in finite rank, a regularized Fredholm determinant, an Evans function, spectral flow, or a lowest-eigenvalue criterion in the corresponding analytic category. The invariant statement is

\[
[\Phi]\in\Sigma_\Phi
\quad\Longleftrightarrow\quad
\ker\mathscr L_\Phi\neq\{0\}
\quad\text{or}\quad
\mathscr L_\Phi\text{ changes Fredholm character}.
\tag{2.7}
\]

The vanishing locus does not by itself determine the transition. It identifies where a change is possible. The transition type follows from the reduced nonlinear equation and, for global branch exchange, from the relative phase action.

---

## 3. Critical Reduction and the Origin of Order Parameters

The first rigorous bridge from the universal phase equation to finite physical data is Lyapunov–Schmidt reduction. The following proposition is the local structural engine of UPT.

### Proposition 3.1 — Phase reduction theorem

Let \(\mathscr F:\mathcal C_\Phi\times\Lambda\to\mathcal Y_\Phi\) be \(C^r\), \(r\geq3\), and suppose \(\mathscr F[\Phi_c;\lambda_c]=0\). Assume \(\mathscr L_c:=\mathscr L_{\Phi_c}\) is Fredholm of index zero with finite critical kernel

\[
K:=\ker\mathscr L_c=\operatorname{span}\{e_a\}_{a=1}^{k}.
\]

Then, in a neighborhood of \((\Phi_c,\lambda_c)\), the solution set of \(\mathscr F=0\) is equivalent to the zero set of a finite-dimensional reduced phase equation

\[
\boxed{\varphi^a(\eta,\lambda)=0,\qquad \eta\in K.}
\tag{3.1}
\]

The coefficients \(\eta^a\) are the canonical local phase order parameters.

### Proof

Choose closed complements \(R\) and \(R^*\) such that

\[
\mathcal C_\Phi=K\oplus R,
\qquad
\mathcal Y_\Phi=\operatorname{coker}(\mathscr L_c)\oplus R^*.
\tag{3.2}
\]

Write a nearby configuration as

\[
\Phi=\Phi_c+\eta^ae_a+\xi,
\qquad \xi\in R.
\tag{3.3}
\]

Let \(P\) project onto \(\operatorname{coker}(\mathscr L_c)\). The equation splits into

\[
(1-P)\mathscr F[\Phi_c+\eta^ae_a+\xi;\lambda]=0,
\qquad
P\mathscr F[\Phi_c+\eta^ae_a+\xi;\lambda]=0.
\tag{3.4}
\]

The derivative of the first equation with respect to \(\xi\) is \(\mathscr L_c|_R\), which is invertible. The implicit function theorem yields a unique smooth map \(\xi=\xi(\eta,\lambda)\). Substitution into the second equation gives

\[
\varphi^a(\eta,\lambda)
:=\langle e^{*a},P\mathscr F[\Phi_c+\eta^be_b+\xi(\eta,\lambda);\lambda]\rangle=0.
\tag{3.5}
\]

Therefore the full local solution geometry is encoded by \(\varphi\) on \(K\). \(\square\)

Expanding (3.5), with \(\delta\lambda^i=\lambda^i-\lambda_c^i\), gives

\[
\varphi^a=M^a{}_i\delta\lambda^i
+\frac12C^a{}_{bc}\eta^b\eta^c
+\frac16D^a{}_{bcd}\eta^b\eta^c\eta^d
+O(\eta^4,\eta\delta\lambda,\delta\lambda^2).
\tag{3.6}
\]

The tensors \(M\), \(C\), and \(D\) are phase-unfolding tensors. Together with the action of the residual phase symmetry on \(K\), they classify the local normal form. This is the precise meaning of universality in the present construction: nonessential microscopic coordinates can change while the contact-equivalence class of \(\varphi\) remains fixed [1] [2].

### Proposition 3.2 — Global branch transition criterion

Suppose the theory is variational and possesses two distinct locally stable reduced branches \(\eta_{(r)}(\lambda)\) and \(\eta_{(s)}(\lambda)\). Let \(\mathcal V_{\mathrm{red}}\) denote the reduced phase action. A global phase transition occurs at \(\lambda_c\) when

\[
\mathcal V_{\mathrm{red}}(\eta_{(r)}(\lambda_c),\lambda_c)
=
\mathcal V_{\mathrm{red}}(\eta_{(s)}(\lambda_c),\lambda_c),
\tag{3.7}
\]

while both reduced Hessians remain nondegenerate. This transition need not lie on \(\Delta_\Phi=0\).

The distinction between (2.6) and (3.7) is indispensable. A local critical stratum is a loss of response invertibility; a global transition is a change in the dominant stable phase. Neither condition can substitute for the other.

---

## 4. Response Geometry: Metric Without Metric Primitivity

Geometry emerges in UPT from controlled phase distinguishability. Let \(\eta^a(\lambda)\) be a regular reduced branch and let

\[
S_{ab}:=\frac{\partial^2\mathcal V_{\mathrm{red}}}{\partial\eta^a\partial\eta^b},
\qquad
T_{ia}:=\frac{\partial^2\mathcal V_{\mathrm{red}}}{\partial\lambda^i\partial\eta^a}.
\tag{4.1}
\]

Differentiating the equilibrium equation \(\partial\mathcal V_{\mathrm{red}}/\partial\eta^a=0\) yields

\[
S_{ab}\,\partial_i\eta^b+T_{ia}=0,
\qquad
\partial_i\eta^a=-\chi^{ab}T_{ib},
qquad
\chi^{ab}:=(S^{-1})^{ab}.
\tag{4.2}
\]

Define the response metric

\[
\boxed{g^{\Phi}_{ij}:=T_{ia}\chi^{ab}T_{jb}.}
\tag{4.3}
\]

If the stable reduced Hessian is positive on physical directions, \(g^\Phi\) is positive semidefinite and descends, after quotienting null gauge directions, to a metric on the regular relational control manifold \(\mathcal R_\Phi\). The associated phase distance is

\[
D_\Phi(\lambda_0,\lambda_1)
=\inf_{\gamma:\lambda_0\to\lambda_1}
\int_\gamma\sqrt{g^{\Phi}_{ij}\,d\lambda^i d\lambda^j}.
\tag{4.4}
\]

This formula establishes a strict ontological reversal: distance is the least distinguishable phase deformation, not a primitive separation. In particular, the divergence of \(\chi\) near \(\Sigma_\Phi\) produces geometric singularity in response space,

\[
\Delta_\Phi\to0
\quad\Longrightarrow\quad
\|g^\Phi\|\to\infty
\quad\text{along an active critical direction}.
\tag{4.5}
\]

The connection compatible with \(g^\Phi\) has coefficients

\[
\Gamma^{i}{}_{jk}[\Phi]
=\frac12(g_\Phi^{-1})^{i\ell}
\bigl(\partial_jg^{\Phi}_{\ell k}+\partial_kg^{\Phi}_{\ell j}-\partial_\ell g^{\Phi}_{jk}\bigr),
\tag{4.6}
\]

and curvature \(R^{i}{}_{jkl}[\Phi]\) follows in the ordinary manner. Curvature is thus an invariant of the variation of phase response.

A response metric is not yet a physical spacetime metric. In particular, (4.3) is naturally positive on a stable equilibrium branch. A Lorentzian signature requires a dynamical construction from the principal symbol of the phase propagation operator, not an analytic continuation imposed by hand. This distinction prevents a common category error: a metric of distinguishability is not automatically a metric of causality.

---

## 5. Phase Transport, Bundle Structure, and Holonomy

Let \(P_\Phi\to\mathcal R_\Phi\) be the principal bundle of admissible phase frames, with structural group \(G_\Phi\) determined by the automorphisms of the phase fiber. A local frame change \(u:\mathcal R_\Phi\to G_\Phi\) acts by \(\Phi\mapsto u\cdot\Phi\). Comparison of phase states at neighboring relational locations requires a connection one-form

\[
\boxed{A^\Phi=A_i^\Phi\,d\lambda^i\in\Omega^1(P_\Phi,\mathfrak g_\Phi),
\qquad A_i^\Phi=\mathcal A_i[\Phi].}
\tag{5.1}
\]

For a phase tensor \(\Psi\) in a representation \(\rho\), the phase-covariant derivative is

\[
\nabla_i^{\Phi}\Psi=\partial_i\Psi+\rho_*(A_i^\Phi)\Psi.
\tag{5.2}
\]

Under a phase-frame transformation,

\[
A_i^\Phi\longmapsto uA_i^\Phi u^{-1}-(\partial_i u)u^{-1},
\qquad
F_{ij}^\Phi:=\partial_iA_j^\Phi-\partial_jA_i^\Phi+[A_i^\Phi,A_j^\Phi].
\tag{5.3}
\]

The curvature \(F^\Phi\) measures the noncommutativity of infinitesimal phase comparison:

\[
[\nabla_i^\Phi,\nabla_j^\Phi]\Psi=\rho_*(F_{ij}^\Phi)\Psi.
\tag{5.4}
\]

For a closed relational loop \(\gamma\), phase transport produces the holonomy

\[
\boxed{U_\gamma[\Phi]=\mathcal P\exp\!\left(-\oint_\gamma A^\Phi\right).}
\tag{5.5}
\]

A nontrivial conjugacy class \([U_\gamma]\) is a gauge-invariant obstruction to globally identifying phase frames. This is the UPT origin of gauge-like structure: not a group inserted as an independent force law, but the residual nontriviality of phase transport once a phase-frame bundle has emerged.

### Proposition 5.1 — Holonomy criterion for spinorial phase sectors

Suppose an emergent rotational loop \(\gamma_{2\pi}\) acts on a stable phase excitation through a representation \(\rho\) of the phase holonomy group. If

\[
\rho(U_{\gamma_{2\pi}})=-\mathbf 1,
\tag{5.6}
\]

then the excitation transforms spinorially under the corresponding emergent rotation. More generally,

\[
\rho(U_{\gamma_{2\pi}})=e^{2\pi i s}\mathbf 1
\tag{5.7}
\]

identifies the holonomy label \(s\) modulo the representation’s periodicity.

The proposition is conditional on an emergent rotation group and a well-defined phase-frame representation. It does not derive the observed spin spectrum. It specifies the mechanism any UPT derivation of spin must realize.

---

## 6. Topological Classification and Extended Phase Sectors

### 6.1 Vacuum manifold and defect charge

Let \(\Phi_*\) be a stable vacuum branch. Its residual symmetry is

\[
H_{\Phi_*}:=\{g\in G_\Phi:g\cdot\Phi_*=\Phi_*\},
\tag{6.1}
\]

and the vacuum manifold is the orbit

\[
\mathcal V_\Phi\simeq G_\Phi/H_{\Phi_*},
\tag{6.2}
\]

when the orbit description is valid. A finite-energy localized configuration must approach \(\mathcal V_\Phi\) on the boundary of an emergent transverse domain. If a defect has emergent codimension \(q\), that boundary is \(S^{q-1}\), and its topological sector is

\[
[\Phi_\infty]\in\pi_{q-1}(\mathcal V_\Phi).
\tag{6.3}
\]

A codimension-two sector is characterized by

\[
[\Phi_\infty]\in\pi_1(\mathcal V_\Phi).
\tag{6.4}
\]

This is the precise UPT definition of a **line-like phase excitation**. The one-dimensional extension is an emergent property of the codimension-two topology in the phase-generated geometry. It is not an ontologically primitive object.

When the relevant factor of \(\mathcal V_\Phi\) is compact Abelian, a local representative may be written \(e^{i\vartheta}\), and the defect charge is

\[
Q_\mathrm{line}[\Phi]
=\frac{1}{2\pi}\oint_{S^1}d\vartheta
\in\mathbb Z.
\tag{6.5}
\]

For non-Abelian or higher bundles, the charge is replaced by the appropriate homotopy, characteristic, index, or holonomy invariant. No particular topology—and hence no particular charge spectrum—is postulated at this stage.

### 6.2 Tension and stability

Assume a phase-energy functional \(E_\Phi\) has emerged on a spatial slice of the effective geometry. Let \(\mathscr D\) be a translationally homogeneous line-like sector of emergent length \(L\). Its tension is the asymptotic excess phase energy

\[
\boxed{
\tau_\mathscr D
:=\lim_{L\to\infty}\frac{E_\Phi[\Phi_\mathscr D]-E_\Phi[\Phi_*]}{L}.}
\tag{6.6}
\]

The quantity is physically meaningful only after both the effective length and the energy functional have been derived. A phase sector is stable when it has either spectral stability,

\[
\sigma(\mathscr L_{\Phi_\mathscr D})\cap\mathbb R_- =\varnothing
\quad\text{in the conservative energy convention},
\tag{6.7}
\]

or topological stability through a nontrivial sector (6.3), or both. Topological stability protects a configuration from continuous relaxation to \(\Phi_*\); it does not ensure dynamical stability against all finite-energy breakup channels.

### Proposition 6.1 — Topological obstruction to vacuum relaxation

Let \(\Phi_\mathscr D\) be a finite-energy codimension-two configuration with \([\Phi_\infty]\neq0\in\pi_1(\mathcal V_\Phi)\). Any continuous finite-energy path \(\Phi_s\), \(s\in[0,1]\), from \(\Phi_\mathscr D\) to the vacuum must either leave the finite-energy configuration space or pass through a configuration for which the vacuum boundary condition fails.

### Proof

Finite energy fixes the boundary map into \(\mathcal V_\Phi\). A continuous finite-energy deformation induces a homotopy of this map, preserving its class in \(\pi_1(\mathcal V_\Phi)\). The vacuum has trivial boundary class, contradicting \([\Phi_\infty]\neq0\). \(\square\)

This proposition derives a protected sector once the vacuum manifold is specified. It does **not** identify that sector with a known elementary particle, does not impose a particle mass, and does not supply a gauge representation. Those data must be computed from an explicit universal phase equation.

| Quantity | Derived from an explicit UPT model | Forbidden insertion |
|---|---|---|
| Extendedness | Codimension and finite-energy vacuum boundary condition | An elementary line object placed in the action |
| Charge | \(\pi_{q-1}(\mathcal V_\Phi)\), characteristic class, or holonomy | An assigned numerical charge table |
| Tension or mass | Excess phase energy and stability spectrum | A prescribed spectrum of tensions or masses |
| Gauge representation | Action of the emergent phase-frame group on a mode | A selected particle representation |
| Interaction | Nonlinear overlap and connection curvature | A force law chosen independently of \(\Phi\) |

---

## 7. Scale Dependence and the Phase Origin of Effective Fields

UPT has no fixed commitment to the degrees of freedom visible at all resolutions. Let \(\mathcal R_b\) be an admissible phase coarse-graining transformation with scale factor \(b>1\):

\[
\Phi\longmapsto\Phi_b:=\mathcal R_b[\Phi].
\tag{7.1}
\]

A scale-stable phase functional satisfies

\[
\mathcal R_b[S_\Phi^*]=S_\Phi^*.
\tag{7.2}
\]

Linearization around \(S_\Phi^*\) gives eigenoperators

\[
D\mathcal R_b\big|_{S_\Phi^*}\mathcal O_\alpha=b^{y_\alpha}\mathcal O_\alpha.
\tag{7.3}
\]

The signs of \(y_\alpha\) classify relevant, marginal, and irrelevant phase deformations. A field is therefore an effective coordinate on an infrared-stable phase sector, not necessarily a primitive variable. The same statement applies to a line-like phase excitation: at one scale it may be resolved as a topological configuration; at another, it may appear as a pointlike mode in the lower-resolution geometry.

The effective action takes the schematic form

\[
S_{\Phi,\ell}^{\mathrm{eff}}
=\sum_\alpha c_\alpha(\ell)\,\mathcal O_\alpha[\Phi_\ell],
\tag{7.4}
\]

with the coefficients \(c_\alpha\) determined by phase coarse-graining. The universality claim is limited and exact: two microscopic phase realizations belong to the same infrared class only if their flows share the same fixed data, symmetries, topological sector, and relevant operator content. UPT does not license the claim that all phase manifolds generate one universal low-energy physics.

---

## 8. Emergent Causality, Quantum Kinematics, and Gravity

### 8.1 Causal cone from phase propagation

Let \(\mathscr P_\Phi\) denote the linearized propagation operator for perturbations about a scale-stable phase background. Its principal symbol \(\sigma_p(\mathscr P_\Phi;k)\) defines the characteristic set

\[
\operatorname{Char}(\mathscr P_\Phi)
=\{k\neq0:\det\sigma_p(\mathscr P_\Phi;k)=0\}.
\tag{8.1}
\]

An effective Lorentzian sector exists only if, after an emergent manifold and cotangent structure have been identified, this characteristic equation reduces in the infrared to

\[
g_\mathrm{eff}^{\mu\nu}[\Phi]k_\mu k_\nu=0
\tag{8.2}
\]

with signature \((-,+,+,+)\). Equation (8.2) is a **criterion**, not a consequence of the response metric alone. It states what an explicit phase dynamics must produce to yield causal propagation and Lorentz symmetry.

### 8.2 Phase amplitude and quantum structure

A complex effective amplitude can arise on a reduced two-dimensional symplectic phase sector. Let \((\rho,\theta)\) be local amplitude and relational phase coordinates, and set

\[
\psi=\sqrt\rho\,e^{i\theta/\hbar_\mathrm{eff}}.
\tag{8.3}
\]

If coarse-graining produces the effective action

\[
S_{\mathrm{red}}
=\int dt\,d^dx\left[-\rho\!\left(\partial_t\theta+
\frac{\lvert\nabla\theta\rvert^2}{2m_\mathrm{eff}}+V\right)
-\frac{\hbar_\mathrm{eff}^2}{8m_\mathrm{eff}}\frac{\lvert\nabla\rho\rvert^2}{\rho}\right],
\tag{8.4}
\]

its Euler–Lagrange equations combine into the Schrödinger equation for \(\psi\). This is a conditional emergence theorem: a quantum wave equation follows once the phase action has generated the symplectic pair, the particular gradient term, and \(\hbar_\mathrm{eff}\). The framework does not derive those ingredients merely by naming \(\Phi\) a phase.

Similarly, interference follows from relational composition,

\[
\lvert\psi_1+\psi_2\rvert^2
=\lvert\psi_1\rvert^2+\lvert\psi_2\rvert^2
+2\operatorname{Re}(\psi_1^*\psi_2),
\tag{8.5}
\]

but the probability rule \(P=\lvert\psi\rvert^2\) remains a required derivation. A successful UPT derivation must show that the phase measure is additive on exclusive branches, invariant under phase-frame changes, composition consistent, continuous, and uniquely fixed by the emergent dynamics.

### 8.3 Gravitational limit

If the coarse-grained phase response generates a shared effective metric \(g_{\mu\nu}^{\mathrm{eff}}[\Phi]\) for every stable excitation, free propagation takes the phase-geometric form

\[
u^\nu\nabla_\nu^{(\Phi)}u^\mu=0.
\tag{8.6}
\]

Universality of free fall then follows from common coupling to the same emergent geometry, not from a separately imposed gravitational charge. The required long-distance result is stronger:

\[
\mathcal R_\ell[S_\Phi]
\xrightarrow[\ell\to\infty]{}
\int d^4x\sqrt{-g_\mathrm{eff}}
\left[\frac{R[g_\mathrm{eff}]}{16\pi G_\mathrm{eff}}
+\mathcal L_\mathrm{eff}\right].
\tag{8.7}
\]

Only a demonstrated derivation of (8.7), including the correct propagating content and controlled corrections, establishes an Einstein regime. An analogy between phase response and curvature is not sufficient.

---

## 9. What the Construction Derives and What It Must Still Produce

The universal formalism has real content before a model is solved: it defines the operator hierarchy, proves reduction near criticality, identifies the necessary topology of protected extended sectors, and provides a response-geometric and bundle-theoretic route to fields. It does not yet determine the world.

| Structural statement | Status within UPT |
|---|---|
| Critical phase directions are \(\ker\mathscr L_\Phi\) | Derived from the definition and linearization of \(\mathscr F\) |
| Finite-dimensional order parameters exist near finite-kernel Fredholm criticality | Proven by Proposition 3.1 |
| Codimension-two sectors are classified by \(\pi_1(\mathcal V_\Phi)\) | Derived once a vacuum manifold and finite-energy condition are established |
| Gauge curvature is nontrivial phase transport | Derived from the connection on the emergent phase-frame bundle |
| A response metric exists on regular phase-control directions | Defined by (4.3), subject to positivity and quotient conditions |
| A physical \(3+1\)-dimensional Lorentzian metric exists | Must be derived from the propagation operator and coarse-grained phase geometry |
| The observed gauge group and representations emerge | Must be derived from \(\mathcal M_\Phi\), \(\mathscr G_\Phi\), and vacuum stabilizer data |
| Standard particle masses and generations emerge | Must be obtained from stable spectra and topological sectors without parameter insertion |
| Quantum probability and the Einstein limit emerge | Must be derived, not inferred from formal resemblance |

This separation is not a weakness to conceal. It is the condition that makes UPT a scientific program rather than an unfalsifiable vocabulary.

---

## 10. Falsifiability Program and Research Questions

An explicit UPT realization is scientifically viable only if it produces controlled, noninserted low-energy structure and a quantitative discriminator. The following conditions are jointly decisive.

### Falsifiability criteria

| Criterion | Required calculation | Failure condition |
|---|---|---|
| **F1: Pregeometric closure** | Specify \(\mathcal M_\Phi\), \(\mathscr G_\Phi\), \(S_\Phi\), and measure data without a hidden spacetime metric or particle list | The model presupposes the geometry, gauge group, or spectrum it claims to derive |
| **F2: Geometric emergence** | Derive a nondegenerate effective manifold, metric, dimension, and causal cone from phase response and propagation | No controlled Lorentzian sector or universal causal propagation appears |
| **F3: Gauge derivation** | Compute the phase-frame bundle, connection, residual group, and representations of stable modes | The observed gauge structure is chosen as input rather than selected by phase topology and vacuum data |
| **F4: Spectral derivation** | Classify stable localized sectors, their charges, masses, spins, and decay channels | Spectrum requires arbitrary assignment or disagrees with established bounds |
| **F5: Quantitative novelty** | Derive at least one numerical departure from the relevant effective theory | All predictions reduce to already fitted effective parameters or no discriminating prediction exists |

The first research question is therefore not “which known object is represented by a phase defect?” It is:

\[
\boxed{\text{What is the minimal }(\mathcal M_\Phi,\mathscr G_\Phi,S_\Phi)\text{ for which the full hierarchy closes?}}
\tag{10.1}
\]

The subsequent questions follow in a fixed logical order:

1. Which phase manifold admits stable sectors but does not encode the target gauge group by construction?
2. Which universal phase equation has a well-posed variational or dynamical formulation and a controlled coarse-graining flow?
3. Which vacuum branch produces a four-dimensional Lorentzian characteristic geometry?
4. Which residual phase-frame group acts on the stable spectrum, and why does its representation content match observation?
5. Which phase invariant fixes charge quantization, generation structure, and spinorial holonomy?
6. Which unique dimensionless observable distinguishes the model from the current low-energy effective description?

The computational program is correspondingly phase-first:

\[
\text{specify }\mathcal M_\Phi
\rightarrow
\text{construct }S_\Phi
\rightarrow
\text{solve }\mathscr F=0
\rightarrow
\text{compute }\sigma(\mathscr L_\Phi)
\rightarrow
\text{classify topology}
\rightarrow
\text{derive geometry and transport}
\rightarrow
\text{extract spectra}.
\tag{10.2}
\]

At no stage may a desired particle or spacetime structure be used as a boundary condition and then counted as a prediction.

---

## 11. Conclusion

UPT admits a precise formulation of extended physical structure without positing an elementary extended object. The primitive datum is the universal phase configuration \(\Phi\). The universal phase equation \(\mathscr F[\Phi;\lambda]=0\) selects admissible configurations; the stability operator \(\mathscr L_\Phi=D_\Phi\mathscr F\) determines local persistence; the bifurcation invariant \(\Delta_\Phi=\operatorname{Det}_{\Phi}(\mathscr L_\Phi)\) identifies critical phase strata; and the susceptibility \(\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}\) turns response into geometry.

The Lyapunov–Schmidt theorem proves that critical phase behavior is carried by a finite order-parameter space. The phase-frame bundle and its connection yield transport, curvature, and holonomy. The vacuum manifold yields topological sectors. A stable codimension-two sector yields a line-like excitation with charge, tension, and interaction determined by phase topology and phase energy. In this hierarchy, extension, force, and geometry are derivative properties of the same phase organization.

The program now has a clear standard of success. It must identify a universal phase action that generates, rather than assumes, a Lorentzian geometry, quantum kinematics, gauge structure, stable particle spectrum, and a quantitative novel prediction. If it cannot do so without hidden insertion, phase primacy is inadequate as a foundational substrate. If it can, the distinction between geometry, connection, field, particle, and extended excitation becomes a scale-dependent organization of one universal phase structure.

\[
\boxed{
\Phi
\Rightarrow
\mathscr F
\Rightarrow
\mathscr L_\Phi
\Rightarrow
\Sigma_\Phi
\Rightarrow
\text{topology}
\Rightarrow
\text{geometry}
\Rightarrow
\text{transport}
\Rightarrow
\text{stable sectors}
\Rightarrow
\text{observables}.}
\]

---

## References

[1] M. G. Crandall and P. H. Rabinowitz, “Bifurcation from Simple Eigenvalues,” *Journal of Functional Analysis* **8**, 321–340 (1971). <https://doi.org/10.1016/0022-1236(71)90015-2>

[2] J. E. Marsden and M. McCracken, *The Hopf Bifurcation and Its Applications* (Springer, 1976). <https://doi.org/10.1007/978-1-4612-6374-6>

[3] S. Kobayashi and K. Nomizu, *Foundations of Differential Geometry, Vol. I* (Wiley, 1963). <https://doi.org/10.1002/9780470157334>

[4] J. Milnor, *Morse Theory* (Princeton University Press, 1963). <https://press.princeton.edu/books/paperback/9780691080086/morse-theory>

[5] K. G. Wilson and J. Kogut, “The Renormalization Group and the \(\epsilon\) Expansion,” *Physics Reports* **12**, 75–199 (1974). <https://doi.org/10.1016/0370-1573(74)90023-4>

[6] M. Nakahara, *Geometry, Topology and Physics*, 2nd ed. (CRC Press, 2003). <https://doi.org/10.1201/9780367806931>

[7] P. W. Anderson, “More Is Different,” *Science* **177**, 393–396 (1972). <https://doi.org/10.1126/science.177.4047.393>

---

*This manuscript is an original UPT formulation. It begins from phase primacy and contains no dependence on any prior phase-framework ontology.*
