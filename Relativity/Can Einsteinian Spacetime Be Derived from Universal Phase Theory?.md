# Can Einsteinian Spacetime Be Derived from Universal Phase Theory?

## A Foundational Derivation Audit, No-Go Result for the Minimal Postulates, and Program for a Non-Ad Hoc Completion

**Dust LLC**  
**Foundational Research Preprint**  
**27 August 2026**

---

## Abstract

This paper tests, rather than presupposes, the proposition that Einsteinian spacetime follows from the minimal postulates of Universal Phase Theory (UPT). The starting datum is a generalized phase section \(\Phi\in\Gamma(E_\Phi)\), subject to the universal phase equation \(\mathscr F[\Phi;\lambda]=0\), its linearization \(\mathscr L_\Phi=D_\Phi\mathscr F\), the bifurcation condition \(\Delta_\Phi=\operatorname{Det}_{\mathrm{red}}\mathscr L_\Phi=0\), and the susceptibility \(\boldsymbol\chi_\Phi=\mathscr L_\Phi^{-1}\) where the inverse exists. We retain only the UPT postulates necessary to formulate this hierarchy and to discuss emergence, observability, and scale dependence. Every further structure is separately classified as **defined**, **assumed**, **imported from established mathematics**, **derived**, **conjectural**, **numerically verified**, or **failed**.

The analysis produces three conditional results. First, under standard Fredholm and smoothness hypotheses, Lyapunov–Schmidt reduction derives a finite-dimensional critical order-parameter space. Second, with an independently supplied real symmetric, invertible reduced Hessian \(S\) and a map from controls to reduced coordinates, the tensor

\[
 g^{\Phi}_{ij}=T_{ia}\chi^{ab}T_{jb},
 \qquad T_{ia}=\partial_i\eta_a,
 \qquad \chi=S^{-1},
\]

is a well-defined response tensor away from criticality. Third, if this tensor is positive definite, it defines a Riemannian geometry on a control or moduli manifold. None of these results yields a four-dimensional Lorentzian event manifold, a universal causal cone, diffeomorphism gauge redundancy, a massless helicity-two sector, universal metric coupling, or the Einstein field equation.

The decisive obstruction is structural. In a stable real variational phase, \(S\succ0\) implies \(g^\Phi\succeq0\); thus the susceptibility construction is generically Riemannian rather than Lorentzian. At a critical configuration and on soliton collective coordinates, the same construction is undefined because the desired tangent vectors lie in \(\ker\mathscr L_\Phi\), precisely where \(\boldsymbol\chi_\Phi\) does not exist. A normal-subspace pseudoinverse removes the divergence by annihilating the collective directions and therefore produces a degenerate tensor. Deterministic finite-difference calculations for the \(\phi^4\) kink confirm this spectral obstruction. Additional counterexamples show that UPT I–X do not select dimension four, do not enforce a common characteristic cone, and do not fix the response-metric normalization.

Accordingly, the minimal UPT postulates **do not derive Einsteinian spacetime**, and the supplied susceptibility-metric proposal fails as a generic derivation of a Lorentzian spacetime metric. This is a negative result about the present premise set, not a denial that a more restrictive phase theory could realize general relativity. We state the exact additional postulates that would be required for such a completion and apply the requested TN-02 parameter-identifiability/rank criterion to show that no present parameter-to-observable map exists on which an Einsteinian fit could be claimed.

> **Main result.** From the minimal UPT postulates and operator hierarchy, one derives conditional phase reduction and, with additional data, response geometry. The implication \(\mathrm{UPT}_{\min}\Rightarrow\mathrm{Einsteinian\ spacetime}\) is **failed**. The construction terminates before Lorentzian metric structure and before Einstein dynamics.

**Keywords:** Universal Phase Theory; emergent spacetime; response geometry; Lyapunov–Schmidt reduction; Lorentzian signature; identifiability; Lovelock theorem; emergent gravity; no-go analysis.

---

## 1. Statement of the problem and audit protocol

The foundational question is whether spacetime geometry, rather than being included in the starting data, can arise from a universal phase substrate. The question is sharpened here to the implication

\[
\boxed{
 \mathrm{UPT}_{\min}
 \stackrel{?}{\Longrightarrow}
 \bigl(M^4,g_{\mu\nu},\nabla,\mathcal E_{\mu\nu}\bigr)_{\mathrm{Einstein}}
}
\tag{1.1}
\]

where the right-hand side denotes an operational event manifold \(M^4\), a nondegenerate Lorentzian metric \(g\), its torsion-free metric connection \(\nabla\), and a low-energy dynamics whose leading metric equation is

\[
G_{\mu\nu}[g]+\Lambda g_{\mu\nu}
=\kappa T_{\mu\nu},
\qquad
\nabla^\mu T_{\mu\nu}=0.
\tag{1.2}
\]

Equation (1.1) is not taken as a definition of success. It is an exact target against which the derivation is audited. In particular, a tensor called a metric, a curved moduli space, or a geodesic equation does not by itself establish (1.2). The Einstein–Hilbert variational construction begins with a Lorentzian manifold and a nondegenerate dynamical metric; its variation then yields the vacuum Einstein tensor, while diffeomorphism invariance entails the Bianchi identity.[5] The present task is to establish whether those antecedents are consequences of UPT rather than imported ingredients.

Every line of the construction carries one of the following status labels.

| Label | Meaning in this paper |
|---|---|
| **Defined** | A notation, space, or criterion introduced by stipulation; no ontological consequence is claimed. |
| **Assumed** | A substantive condition not implied by UPT I–X. |
| **Imported** | A theorem or construction from established mathematics or physics, with all hypotheses retained. |
| **Derived** | A conclusion that follows from earlier stated assumptions by an explicit argument. |
| **Conjectural** | A proposed UPT realization without a derivation from the retained premises. |
| **Numerically verified** | A deterministic numerical check of a stated mathematical example; not an empirical verification. |
| **Failed** | A required implication is false in the stated generality, undefined, or cannot be formed from the available data. |

The audit adopts a non-repair rule. When a required structure is absent, no term, symmetry, dimension, sign, or parameter is added merely to obtain Einstein gravity. The missing principle is named, and the construction stops at that point.

---

## 2. Minimal UPT premise set

The supplied UPT manuscripts organize the theory into ten postulates. Not all are required even to formulate the present test. The minimal retained subset is stated below, with the status of each use made explicit.

| UPT element | Minimal formal content used here | Status | What it does **not** supply |
|---|---|---|---|
| I. Phase Primacy | A primitive phase structure \(\Phi\) may underlie effective structures. | **Assumed** | A base manifold, metric signature, action, or field equation. |
| II. Structural Configuration | \(\Phi\in\mathcal C_\Phi\), a generalized phase configuration space. | **Assumed** | Smooth/Banach/Hilbert structure or a physical event set. |
| III. Admissibility | \(\mathscr F[\Phi;\lambda]=0\). | **Assumed** | The form, locality, covariance, variational origin, or order of \(\mathscr F\). |
| IV. Stability | Stability is governed by \(\mathscr L_\Phi=D_\Phi\mathscr F\). | **Defined** once differentiability is supplied | Self-adjointness, a spectral domain, a positive energy, or invertibility. |
| V. Transition | \(\ker\mathscr L_\Phi\neq0\) permits a local transition. | **Assumed/conditional** | Dimension four or an event manifold. |
| VI. Emergence | Candidate observables are functionals \(\mathcal O[\Phi]\). | **Assumed** | The specific functional \(\mathcal O=g_{\mu\nu}\), its signature, or its equations. |
| IX. Relational observability | Only invariant, operationally accessible phase relations count as observables. | **Assumed** | A construction of operational events, clocks, rods, or matter probes. |
| X. Scale dependence | Effective descriptions may be \(\ell\)-dependent. | **Assumed** | A coarse-graining map, fixed point, or infrared symmetry restoration. |

Postulates VII (topological protection) and VIII (universality) may constrain a realization, but neither generates a nondegenerate Lorentzian bilinear form. They are therefore not minimal inputs to the derivation below. Their failure to enforce the desired result is tested in §8.

To make the operator hierarchy mathematical rather than schematic, introduce the following **defined** completion of the minimal data. Let \(\pi_\Phi:E_\Phi\to\mathcal X\) be a phase bundle over an abstract substrate \(\mathcal X\), let \(\mathcal C_\Phi\subset\Gamma(E_\Phi)\) be a differentiable configuration manifold, and let

\[
\mathscr F:\mathcal U\times\Lambda\longrightarrow\mathcal Y_\Phi,
\qquad
(\Phi,\lambda)\longmapsto\mathscr F[\Phi;\lambda],
\tag{2.1}
\]

be differentiable on an open set \(\mathcal U\subset\mathcal C_\Phi\). Here \(\Lambda\) is a control manifold and \(\mathcal Y_\Phi\) a target bundle or function space. These choices are **assumptions**, not consequences of I–X. In particular, no identification \(\mathcal X=M^4\) is made.

The UPT hierarchy then reads

\[
\boxed{
\begin{aligned}
&\mathscr F[\Phi;\lambda]=0, &&\text{admissible phase configurations},\\
&\mathscr L_\Phi:=D_\Phi\mathscr F[\Phi;\lambda], &&\text{phase stability operator},\\
&\Delta_\Phi:=\operatorname{Det}_{\rm red}(\mathscr L_\Phi), &&\text{bifurcation diagnostic},\\
&\boldsymbol\chi_\Phi:=\bigl(\mathscr L_\Phi|_{\mathcal N}\bigr)^{-1}, &&\text{susceptibility, where defined}.
\end{aligned}}
\tag{2.2}
\]

The qualifier “where defined” is essential. In infinite dimensions, a determinant needs a Fredholm or regularized-determinant framework, while an inverse needs a specified closed complement \(\mathcal N\), boundary conditions, and an invertibility statement. Those are **imported** functional-analytic requirements.

---

## 3. What counts as Einsteinian spacetime?

The target must be decomposed before it can be derived. We use six logically independent conditions.

| Condition | Required result | Status relative to minimal UPT |
|---|---|---|
| \(\mathrm{E}_1\) | A smooth four-dimensional manifold \(M\) of operational events. | **Not derived** |
| \(\mathrm{E}_2\) | A smooth nondegenerate symmetric \(g\in\Gamma(S^2T^*M)\) of inertia \((1,3)\) or \((3,1)\). | **Not derived** |
| \(\mathrm{E}_3\) | All low-energy matter modes have one universal characteristic null cone \(g^{\mu\nu}k_\mu k_\nu=0\). | **Not derived** |
| \(\mathrm{E}_4\) | Local \(\mathrm{Diff}(M)\) redundancy, with the corresponding Noether identity. | **Not derived** |
| \(\mathrm{E}_5\) | A local, low-energy, generally covariant metric action whose leading equation is (1.2). | **Not derived** |
| \(\mathrm{E}_6\) | Universal coupling, geodesic limit, and a massless helicity-two gravitational sector. | **Not derived** |

The distinction between \(\mathrm E_2\) and \(\mathrm E_5\) is decisive. Once a pseudo-Riemannian metric is supplied, its Levi–Civita connection and curvature are standard **imported** differential geometry. But neither curvature nor geodesics select the Einstein field equation. Conversely, Lovelock’s theorem classifies second-order, symmetric, divergence-free natural metric tensors; in four dimensions it singles out the Einstein tensor together with the metric term under its stated hypotheses.[1] It does not establish those hypotheses from phase structure.

> **Target principle.** “Emergent geometry” is established only upon \(\mathrm E_1\)–\(\mathrm E_2\). “Einsteinian spacetime” is established only upon \(\mathrm E_1\)–\(\mathrm E_6\).

---

## 4. What the UPT operator hierarchy derives

### 4.1 Regular phase branches

Let \((\Phi_0,\lambda_0)\) satisfy \(\mathscr F[\Phi_0;\lambda_0]=0\). If \(\mathscr L_{\Phi_0}\) is a bounded isomorphism between the chosen Banach spaces, the implicit-function theorem is **imported** to obtain a local branch \(\Phi(\lambda)\) satisfying

\[
\mathscr F[\Phi(\lambda);\lambda]=0,
\qquad
\Phi(\lambda_0)=\Phi_0.
\tag{4.1}
\]

This is a **derived** local persistence statement conditional on the Banach-manifold setup and invertibility. Differentiating (4.1) gives

\[
D_\Phi\mathscr F\,[\partial_i\Phi]+\partial_i\mathscr F=0,
\qquad
\partial_i\Phi=-\boldsymbol\chi_\Phi\,\partial_i\mathscr F,
\tag{4.2}
\]

when \(\boldsymbol\chi_\Phi\) exists. Equation (4.2) is a standard response identity. It supplies sensitivity of a phase branch to controls, not a spacetime metric.

### 4.2 Critical phase directions and Lyapunov–Schmidt reduction

Let \((\Phi_c,\lambda_c)\) be critical. Assume, in addition to UPT, that

\[
\mathscr L_c:=\mathscr L_{\Phi_c}
\quad\text{is Fredholm of index }0,
\qquad
K:=\ker\mathscr L_c,
\qquad
\dim K=k<\infty.
\tag{4.3}
\]

Choose closed complements \(\mathcal C_\Phi=K\oplus R\) and \(\mathcal Y_\Phi=\operatorname{coker}\mathscr L_c\oplus R'\), with projection \(P:\mathcal Y_\Phi\to\operatorname{coker}\mathscr L_c\). These splittings and the regularity needed below are **assumed/imported**; they do not follow from the formal symbol \(\Delta_\Phi=0\).

Writing \(\delta\Phi=u^ae_a+w\), \(e_a\in K\), the universal equation becomes

\[
(I-P)\mathscr F(\Phi_c+u^ae_a+w;\lambda)=0,
\qquad
P\mathscr F(\Phi_c+u^ae_a+w;\lambda)=0.
\tag{4.4}
\]

By the implicit-function theorem on the regular complement, the first equation determines \(w=w(u,\lambda)\) locally. Substitution gives the reduced equation

\[
\varphi(u,\lambda)
:=P\mathscr F\bigl(\Phi_c+u^ae_a+w(u,\lambda);\lambda\bigr)=0,
\qquad
\varphi:K\times\Lambda\to\operatorname{coker}\mathscr L_c.
\tag{4.5}
\]

Thus the following is a valid conditional UPT theorem.

> **Proposition 4.1 (critical-coordinate reduction).** Under (4.3), the stated splittings, and the regularity hypotheses of Lyapunov–Schmidt reduction, the local phase-transition problem is equivalent to the finite-dimensional equation (4.5). The coordinates \(u^a\) are critical phase order parameters.
>
> **Status:** **Imported** theorem plus **derived** application.

The conclusion is strong but limited. It produces a vector space of dimension \(k\), not a manifold of events. Neither \(k=4\) nor the Lorentz group occurs in (4.3)–(4.5). The claim

\[
\ker\mathscr L_c\Longrightarrow M^4
\tag{4.6}
\]

is therefore **failed** in the stated generality.

### 4.3 Topology and phase sectors

For a finite-excess configuration with an asymptotic vacuum manifold \(\mathcal V_\Phi\), one may **define** a sector label

\[
q=[f_q]\in\pi_r(\mathcal V_\Phi),
\qquad
f_q:S^r\to\mathcal V_\Phi.
\tag{4.7}
\]

This is an **imported** homotopy classification. A nontrivial \(q\) can obstruct a deformation between sector representatives, conditional on appropriate boundary and finite-excess conditions. It does not determine the dimensionality, signature, or dynamics of a spacetime. Contractible \(\mathcal V_\Phi\) gives \(\pi_r(\mathcal V_\Phi)=0\) for \(r>0\), an admissible counterexample to any claim that UPT topological protection generically creates spacetime structure.

The UPT ontological hierarchy is consequently refined as follows:

\[
\Phi
\longrightarrow
\text{topological sectors}
\longrightarrow
\text{conditional reduced/moduli geometry}
\longrightarrow
\text{conditional connections}
\longrightarrow
\text{collective fields}
\longrightarrow
\text{stable sectors}
\longrightarrow
\text{observables}.
\tag{4.8}
\]

The arrows in (4.8) are a **research program**, not all derivations. In particular, the arrow from phase geometry to spacetime remains open and is tested next.

---

## 5. Susceptibility geometry: construction and obstruction

### 5.1 Conditional definition of a response tensor

The supplied UPT candidate proposes a phase-response metric. To formulate it, add the following data:

\[
\eta:\Lambda\to\mathbb R^k,
\qquad
T_{ia}:=\partial_i\eta_a,
\qquad
S_{ab}:=\partial_a\partial_b\Phi_{\rm eff}(\eta),
\qquad
\chi^{ab}:=(S^{-1})^{ab}.
\tag{5.1}
\]

The existence of a reduced potential \(\Phi_{\rm eff}\), a real symmetric Hessian \(S\), and an invertible \(S\) are **additional assumptions**. They require a variational or gradient realization of the universal equation. They do not follow from \(\mathscr F=0\), which may be nonvariational and may have non-self-adjoint linearization.

When these assumptions hold, define

\[
\boxed{
 g^\Phi_{ij}:=T_{ia}\chi^{ab}T_{jb}
}
\tag{5.2}
\]

on the control manifold or on a chosen manifold of collective coordinates. Equation (5.2) is **defined**, not derived from UPT I–X. Symmetry of \(g^\Phi\) is inherited from the assumed symmetry of \(S\).

### 5.2 Stable response is not Lorentzian

> **Proposition 5.1 (stable-response signature).** Let \(S\) be real symmetric and positive definite. Let \(T: T_\lambda\Lambda\to\mathbb R^k\) be real. Then \(g^\Phi=T\,S^{-1}T^{\mathsf T}\) is positive semidefinite. If \(T\) has full row rank, it is positive definite on its image. In particular, it cannot have Lorentzian inertia.
>
> **Status:** **Derived**.

**Proof.** For every \(v\in T_\lambda\Lambda\),

\[
v^ig^\Phi_{ij}v^j
=(T^{\mathsf T}v)^a(S^{-1})_{ab}(T^{\mathsf T}v)^b\ge0,
\tag{5.3}
\]

because \(S^{-1}\succ0\). A Lorentzian bilinear form possesses both positive and negative directions, which (5.3) excludes. \(\square\)

This is not a merely semantic objection. Stability in a static real variational realization is conventionally represented by a positive quadratic form. The signature desired for spacetime is therefore not a consequence of the UPT response formula; it conflicts with the most direct stable realization of that formula. Selecting an indefinite \(S\) would not repair the conclusion: it would be an **assumption** of an unstable or constrained phase structure and would still not establish exactly one timelike direction or hyperbolic propagation.

The response tensor has an independent rank limitation:

\[
\operatorname{rank}g^\Phi
\le\operatorname{rank}T
\le k.
\tag{5.4}
\]

Hence even nondegeneracy requires at least as many independent reduced directions as the proposed spacetime dimension. UPT has not derived \(k=4\), nor an event interpretation of those directions.

### 5.3 The collective-coordinate singularity

The candidate construction also proposes that position arise as a coordinate \(X^i\) on a moduli space of localized phase configurations \(\Phi_q(X)\). Translation invariance gives tangent vectors

\[
T_i=\partial_{X^i}\Phi_q.
\tag{5.5}
\]

For a family of exact solutions, differentiate \(\mathscr F[\Phi_q(X)]=0\):

\[
0=\partial_{X^i}\mathscr F[\Phi_q(X)]
=\mathscr L_qT_i.
\tag{5.6}
\]

Therefore \(T_i\in\ker\mathscr L_q\). But the UPT susceptibility is defined only where the stability operator is invertible, or after restriction to a normal complement. Consequently \(\boldsymbol\chi_qT_i\) is undefined in the unprojected theory.

> **Proposition 5.2 (zero-mode obstruction).** For any exact phase-solution modulus, the response expression \(\langle T_i,\mathscr L_q^{-1}T_j\rangle\) is undefined without an extra prescription. If the inverse is replaced by the inverse on the normal complement and the tangent is projected out, the resulting tensor annihilates the collective tangent direction and is degenerate.
>
> **Status:** **Derived**.

No allowed step turns this failure into a Lorentzian spacetime. A collective-coordinate metric can instead be obtained from an independently supplied kinetic inner product, for example \(G^{\rm mod}_{ij}=\langle\partial_i\Phi_q,\mathscr K_q\partial_j\Phi_q\rangle\). That is a standard moduli-space construction, but \(\mathscr K_q\) is not determined by the susceptibility, and it is an extra **assumption** in the supplied candidate phase action. It yields a geometry of solution moduli; it does not by itself yield an event spacetime.

### 5.4 Normalization nonuniqueness

Let \(h[\Phi;\lambda]\) be any nowhere-zero scalar functional and define

\[
\widetilde{\mathscr F}[\Phi;\lambda]
:=h[\Phi;\lambda]\,\mathscr F[\Phi;\lambda].
\tag{5.7}
\]

The equations \(\widetilde{\mathscr F}=0\) and \(\mathscr F=0\) have identical solution sets. At a solution \(\Phi_0\),

\[
D_\Phi\widetilde{\mathscr F}\big|_{\Phi_0}
=h(\Phi_0;\lambda)\,D_\Phi\mathscr F\big|_{\Phi_0},
\qquad
\widetilde\chi=h^{-1}\chi
\tag{5.8}
\]

in the commuting scalar case. Thus the phase solution set and its topology do not fix the normalization of (5.2). A physical metric may admit coordinate conventions, but the relative normalization controlling a gravitational coupling cannot be left arbitrary if the construction claims a derived Newton scale.

> **Proposition 5.3 (response-normalization ambiguity).** The UPT equation viewed only as a zero set does not determine the normalization of the susceptibility response metric.
>
> **Status:** **Derived**. The attempted derivation of a uniquely normalized physical metric is **failed**.

A normalization principle could arise from a completed action, path-integral measure, or operational clock-and-rod construction. None is present in the minimal postulates.

---

## 6. From phase response to Einstein dynamics: conditional continuation and terminal point

### 6.1 Phase transport, holonomy, and the missing soldering map

Assume, only for this subsection, that a family of phase frames defines a principal \(\mathscr G_\Phi\)-bundle \(P_\Phi\to N\) over a candidate collective manifold \(N\). A phase transport law is then represented by a connection

\[
A^\Phi\in\Omega^1(N,\operatorname{ad}P_\Phi),
\qquad
F^\Phi=dA^\Phi+A^\Phi\wedge A^\Phi,
\tag{6.1}
\]

and its transport around a closed curve \(\gamma\subset N\) is the holonomy

\[
\operatorname{Hol}_\gamma(A^\Phi)
=\mathcal P\exp\left(-\oint_\gamma A^\Phi\right)
\in\mathscr G_\Phi.
\tag{6.2}
\]

Equations (6.1)–(6.2) are **defined/imported** principal-bundle geometry once \(N\), \(P_\Phi\), and \(\mathscr G_\Phi\) are assumed. They capture an obstruction to globally identifying phase frames. They do not, however, make \(A^\Phi\) the affine connection of an emergent spacetime. A spacetime metric connection acts on \(TM\) or on an orthonormal frame bundle reduced to \(O(1,3)\); an internal phase connection acts on the fibers of \(P_\Phi\). The identification would require a nondegenerate soldering form

\[
e\in\Omega^1\bigl(M,\mathbb R^{1,3}\bigr),
\qquad
e^a{}_{\mu}:T_xM\xrightarrow{\sim}\mathbb R^{1,3},
\qquad
g_{\mu\nu}=\eta_{ab}e^a{}_{\mu}e^b{}_{\nu},
\tag{6.3}
\]

plus a derivation of the Lorentz group and the Minkowski form \(\eta_{ab}\). No such bundle morphism follows from phase transport or holonomy. The claim

\[
(P_\Phi,A^\Phi,\operatorname{Hol}A^\Phi)
\Longrightarrow
(F_{\mathrm{Lor}}M,\omega^{\mathrm{LC}})
\tag{6.4}
\]

is therefore **failed** for minimal UPT. This separates the potentially fruitful emergence of internal gauge structure from the distinct problem of gravitational geometry.

### 6.2 Geometry does not imply spacetime

Suppose counterfactually that a future phase realization produces a smooth manifold \(N\) and a nondegenerate tensor \(g^\Phi\in\Gamma(S^2T^*N)\). The Levi–Civita connection

\[
\Gamma^\rho{}_{\mu\nu}[g^\Phi]
=\tfrac12(g^\Phi)^{\rho\sigma}
\left(\partial_\mu g^\Phi_{\sigma\nu}
+\partial_\nu g^\Phi_{\sigma\mu}
-\partial_\sigma g^\Phi_{\mu\nu}\right)
\tag{6.5}
\]

and curvature \(R^\rho{}_{\sigma\mu\nu}[g^\Phi]\) then follow by **imported** differential geometry. This establishes neither that \(N\) is an operational event manifold nor that the tensor has Lorentzian inertia. A moduli manifold may be Riemannian, finite dimensional, and physically useful without describing spacetime.

The causal test is more stringent. For every low-energy collective field \(\varphi_A\), let its linearized principal symbol be \(P_A(k)\). Einsteinian kinematics requires a common cone,

\[
\det P_A(k)=0
\quad\Longleftrightarrow\quad
(g^\Phi)^{\mu\nu}k_\mu k_\nu=0
\qquad\text{for all light }A.
\tag{6.6}
\]

Equation (6.6) requires locality, hyperbolicity, and universality of characteristic surfaces. It is not implied by a response tensor. Critical surveys of emergent-gravity constructions emphasize that without strong symmetry protection, distinct modes generically produce multimetric or more general effective geometries; recovery of a diffeomorphism-invariant regime additionally requires decoupling of extra degrees of freedom or operational invisibility of background structures.[3]

### 6.3 The conditional Einstein theorem is not a UPT derivation

For clarity, consider the following **conditional completion**, whose premises are deliberately stronger than minimal UPT:

\[
\begin{aligned}
\mathrm{A}_1:&\quad \text{A phase construction produces an operational smooth }M^4.\\
\mathrm{A}_2:&\quad \text{It produces a nondegenerate Lorentzian }g_{\mu\nu}[\Phi].\\
\mathrm{A}_3:&\quad \text{All light collective sectors share }g\text{ as their characteristic metric.}\\
\mathrm{A}_4:&\quad \text{The infrared effective action is local and }\mathrm{Diff}(M)\text{-invariant.}\\
\mathrm{A}_5:&\quad \text{The pure metric Euler--Lagrange tensor is symmetric, natural, divergence-free,}\\
&\quad \text{and of differential order at most two.}\\
\mathrm{A}_6:&\quad \text{Matter couples universally to }g\text{ and supplies a conserved }T_{\mu\nu}.\\
\mathrm{A}_7:&\quad \text{The metric sector has the required two massless helicity-two polarizations.}
\end{aligned}
\tag{6.7}
\]

Under \(\mathrm A_1\)–\(\mathrm A_5\), the four-dimensional Lovelock classification implies

\[
\mathcal E_{\mu\nu}[g]
=a\,G_{\mu\nu}[g]+b\,g_{\mu\nu}.
\tag{6.8}
\]

Provided \(a\ne0\), defining \(\Lambda=b/a\) and normalizing the universal coupling gives (1.2). This is a **derived conditional consequence** of the added assumptions plus Lovelock’s theorem.[1] It is not a derivation from the UPT postulates because \(\mathrm A_1\)–\(\mathrm A_7\) contain the relevant spacetime, gauge, and dynamical content.

The independent massless-spin-two route reaches the same conclusion only conditionally: locality, linear gauge invariance, and consistent self-coupling of a massless spin-two field determine the nonlinear Einstein completion.[2] That route begins with a spin-two gauge field on a background spacetime; it does not make such a field emerge from an arbitrary phase equation. It therefore cannot be used to bridge the missing UPT steps.

### 6.4 Precise terminal result

The construction from UPT terminates before \(\mathrm A_1\). The available data neither construct an event manifold nor produce a nondegenerate Lorentzian response tensor. Even if one set aside the response obstruction and asserted \(\mathrm A_1\)–\(\mathrm A_2\), \(\mathrm A_3\)–\(\mathrm A_7\) remain unproved. Thus the desired chain

\[
\Phi
\to \mathscr L_\Phi
\to\boldsymbol\chi_\Phi
\to g^\Phi
\to (M^4,g)
\to G_{\mu\nu}=\kappa T_{\mu\nu}
\tag{6.9}
\]

breaks at the third arrow for the proposed susceptibility construction and at the fourth arrow for the minimal UPT postulates.

| Transition | Audit outcome | Status |
|---|---|---|
| \(\Phi\to\mathscr F,\mathscr L\) | Formal operator hierarchy given differentiability. | **Defined/assumed** |
| \(\ker\mathscr L\to\) finite critical coordinates | Valid under Fredholm Lyapunov–Schmidt hypotheses. | **Derived conditionally** |
| Critical coordinates \(\to g^\Phi=T\chi T^{\mathsf T}\) | Requires variational Hessian, control map, and inverse. | **Defined with assumptions** |
| Stable \(g^\Phi\to\) Lorentzian metric | Contradicted by Proposition 5.1. | **Failed** |
| Collective moduli \(\to g^\Phi\) through \(\chi\) | Undefined; pseudoinverse is degenerate. | **Failed** |
| \(g^\Phi\to M^4\) | No event construction or dimension selection. | **Open** |
| \(g^\Phi\to\) Einstein equation | Requires (6.3), none derived. | **Open; not established** |

---

## 7. TN-02 parameter-identifiability and rank audit

No formal statement called “TN-02” appears in the three supplied manuscripts. To honor the requested criterion without inventing an undocumented rule, this paper uses its stated operational content: **where adjustable parameters and multiple observables occur, identifiability is assessed by the rank of the observable Jacobian.**

Let a specified realization contain a finite parameter vector \(\theta=(\theta^1,\dots,\theta^p)\) and predict \(m\) independent observables

\[
\mathcal O(\theta)=\bigl(\mathcal O_1(\theta),\dots,\mathcal O_m(\theta)\bigr).
\tag{7.1}
\]

Define

\[
J_{Ai}(\theta):=\frac{\partial\mathcal O_A}{\partial\theta^i}.
\tag{7.2}
\]

> **TN-02 operational criterion.** Local identifiability requires \(m\ge p\) and \(\operatorname{rank}J=p\). For a target vector \(\mathcal O^\star\), the linearized compatibility test is
> \[
> \operatorname{rank}J
> =\operatorname{rank}\bigl[J\mid \mathcal O^\star-\mathcal O(\theta)\bigr].
> \tag{7.3}
> \]
> A new parameter may not be added solely to absorb a failed component of the target residual.

A candidate phase action containing a phase derivative, substrate coupling tensor, invariant potential, topological term, connection functional, coarse-graining map, and kinetic operator is not a finite-predictive realization until all of those objects are fixed by postulates or reduced to a stated finite parameterization. The supplied candidate equation,

\[
\mathscr F[\Phi]
=\frac{\delta}{\delta\Phi}
\left\{
\int_{\mathcal X}
\left[
\tfrac12G^{AB}(\Phi)\langle D_A\Phi,D_B\Phi\rangle
-V(I_1[\Phi],\ldots,I_n[\Phi])
\right]d\mu_\Phi
+\mathcal S_{\rm topo}[\Phi]
\right\},
\tag{7.4}
\]

contains functional, not merely numerical, freedom. Choosing \(G^{AB}\), \(D_A\), \(V\), \(\mathcal S_{\rm topo}\), and a scale map to force a target metric would violate the non-ad hoc rule. With these functions unspecified, neither \(p\) nor the map (7.1) exists. The TN-02 verdict is therefore **failed/unassessable**, not passed.

If a future realization fixes (7.4), a minimally relevant target vector would include

\[
\mathcal O=
\bigl(d_{\rm eff},\operatorname{In}(g),\{c_A/c_B\},N_{\rm grav},
\Lambda,\kappa,\alpha_{\rm PPN},\beta_{\rm PPN},\ldots\bigr),
\tag{7.5}
\]

where \(\operatorname{In}(g)\) is metric inertia, \(\{c_A/c_B\}\) tests a universal cone, and \(N_{\rm grav}\) counts propagating graviton polarizations. The first five entries are structural outputs, not fit knobs. The rank test must be applied to the full output vector, including failed cone and polarization observables, rather than only to constants that happen to agree with a desired limit.

A deterministic illustration is included in the accompanying numerical audit. For three parameters and three observables with

\[
J=
\begin{pmatrix}
1&1&0\\
2&2&0\\
0&0&2
\end{pmatrix},
\qquad
\operatorname{rank}J=2<3,
\tag{7.6}
\]

the parameters remain nonidentifiable despite the equal count \(m=p=3\). The smallest singular value is \(8.23\times10^{-17}\). This is **numerically verified** and illustrates why observable count is not a substitute for rank.

---

## 8. Falsification suite

### 8.1 Analytical limiting cases

The following constructions obey the retained UPT premise types but violate one or more desired conclusions. They falsify the general implication (1.1), not every possible future UPT realization.

| Test | Construction | Result | Classification |
|---|---|---|---|
| Stable signature | \(S=\operatorname{diag}(1,2,3,4)\), \(T=I_4\). | \(g^\Phi=\operatorname{diag}(1,1/2,1/3,1/4)\) is positive definite. | **Derived counterexample** |
| Critical kernel | A nontrivial \(\ker\mathscr L_c\) of dimension \(k\). | Reduction gives \(\mathbb R^k\), with no principle fixing \(k=4\). | **Derived insufficiency** |
| Collective modulus | \(\mathscr L_q\partial_X\Phi_q=0\). | The susceptibility is undefined on \(\partial_X\Phi_q\). | **Derived counterexample** |
| Multicone phase | Two stable linear modes with \(\omega^2=c_A^2|k|^2\), \(c_1\ne c_2\). | Their characteristic cones differ. | **Derived counterexample** |
| Topological triviality | \(\mathcal V_\Phi\) contractible. | No nonzero \(\pi_r(\mathcal V_\Phi)\) protects sectors. | **Imported topology / counterexample** |
| Dimensional freedom | Abstract bases of dimensions \(1,3,5\). | UPT I–X can be formulated in each case. | **Defined counterexample** |
| Response scaling | \(\widetilde{\mathscr F}=h\mathscr F\), \(h\ne0\). | Identical zeros, rescaled susceptibility and response tensor. | **Derived counterexample** |

The multicone test is particularly important. A phase theory can have mathematically healthy excitations while failing Einsteinian universality because different collective sectors see different characteristic forms. This possibility is a central issue in emergent-gravity analyses; Lorentz invariance and a single metric do not arise automatically from generic microscopic dynamics.[3] Concrete signature-emergence models likewise demonstrate the distinction: one model obtains hyperbolic perturbations around special background solutions of a theory that first assumes a Riemannian manifold and scalar fields, but its emergent gravity is scalar Nordström gravity rather than Einstein tensor gravity.[4]

### 8.2 Dimensional analysis

Let the reduced coordinates \(\eta^a\) be dimensionless and the controls have dimensions \([\lambda^i]=L^{\alpha_i}T^{\beta_i}\). Then \([T_{ia}]=[\lambda^i]^{-1}\). If \(S_{ab}=\partial_a\partial_b\Phi_{\rm eff}\), then \([\chi^{ab}]=[\Phi_{\rm eff}]^{-1}\), so

\[
[g^\Phi_{ij}]
=[\lambda^i]^{-1}[\lambda^j]^{-1}[\Phi_{\rm eff}]^{-1}.
\tag{8.1}
\]

This dimension is not fixed by the UPT hierarchy. Without a derived relation between phase normalization, physical duration, physical length, and the normalization of the effective action, there is no derivation of \(c\), \(\kappa\), or the mass dimension of the Einstein–Hilbert coefficient. In units \(c=\hbar=1\), the four-dimensional Einstein–Hilbert coefficient has mass dimension two.[5] The phase-response formula contains no derivation that supplies this scale. The conclusion that Newton’s constant is derived is **failed**.

### 8.3 Numerical spectral and rank checks

The accompanying deterministic program uses no observational data and no fitted parameters. It checks the exact counterexamples on a finite grid or finite matrix representation.

| Calculation | Protocol | Numerical output | Audit result |
|---|---|---|---|
| \(\phi^4\) kink zero mode | Discretize \(\mathscr L=-\partial_x^2+4-6\operatorname{sech}^2x\) on \([-14,14]\) with 801 interior points. | Lowest eigenvalue \(-2.32235\times10^{-4}\); overlap squared with translation tangent \(0.999999985\). | **Numerically verified** near-zero mode; the exact continuum mode blocks \(\mathscr L^{-1}\). |
| Projected kink response | Invert only eigenvalues larger than \(10^{-3}\). | \(\langle T,\chi_\perp T\rangle=2.34533\times10^{-9}\). | **Numerically verified** degeneration after projection. |
| Stable response | \(S=\operatorname{diag}(1,2,3,4)\), \(T=I_4\). | \(\operatorname{spec}(g)=(0.25,1/3,1/2,1)\). | **Numerically verified** positive inertia \((4,0,0)\). |
| Cone mismatch | \(c_1=1\), \(c_2=1.25\), \(|k|=2\). | \(\omega_1=2\), \(\omega_2=2.5\). | **Numerically verified** distinct cones. |
| TN-02 example | Matrix (7.6). | Singular values \((3.16228,2,8.23\times10^{-17})\); rank \(2\). | **Numerically verified** rank deficiency. |

The small negative kink eigenvalue is a finite-box/Dirichlet discretization residual of the exact translation zero mode; its overlap with \(\operatorname{sech}^2x\) identifies the mode. The numerical calculation is not used to establish the theorem; it checks the expected singular behavior of the concrete representative.

---

## 9. Additional postulates required for a non-ad hoc UPT completion

The negative result identifies what a future formulation must add. The following are not silently adopted in this paper. Each is a possible **new postulate**, to be independently justified and then falsified.

| Missing structure | Required new postulate | Why it is not contained in UPT I–X |
|---|---|---|
| Event manifold | **P-E (event reconstruction):** a functorial, operational construction \(\mathfrak E[\Phi]=M\) whose stable phase has \(\dim M=4\). | Emergence permits functionals but does not specify an event construction or select dimension. |
| Lorentzian signature | **P-L (causal phase):** the principal symbol of the fundamental or collective phase dynamics possesses exactly one time direction in the stable infrared phase. | A stable response Hessian yields a positive semidefinite form. |
| Universal cone | **P-U (cone universality):** all propagating operational sectors share the same characteristic cone after coarse graining. | One phase field may support multiple modes with inequivalent principal symbols. |
| Diffeomorphism redundancy | **P-D (emergent gauge identity):** the infrared quotient of phase-frame transformations acts as \(\mathrm{Diff}(M)\), inducing a Noether identity. | A general phase equation has no metric gauge transformation or Bianchi identity. |
| Metric dynamics | **P-H (metric effective action):** coarse graining yields a local action of the derived metric with controlled derivative expansion. | Scale dependence alone is not a renormalization map or action calculation. |
| Einstein selection | **P-2 (second-order metric sector):** the leading metric Euler tensor is natural, symmetric, divergence-free, and second order. | This is the content needed to invoke Lovelock, not a result of a generic response metric. |
| Graviton and coupling | **P-G (universal helicity-two phase sector):** exactly two massless spin-two modes couple universally to all operational matter. | Topological or spectral stability does not determine helicity, masslessness, or universality. |
| Parameter prediction | **P-N (normalization and identifiability):** all phase-action coefficients and normalizations are fixed or are independently observable through a full-rank map. | \(\mathscr F=0\) is invariant under rescalings and the supplied realization has unspecified functional freedom. |

Only after a candidate UPT theory proves, rather than declares, P-E through P-N can it claim an Einstein limit. At that stage, the correct statement would be conditional: a concrete phase model realizes the postulates and is tested against \(\mathrm E_1\)–\(\mathrm E_6\). It would not be a consequence of phase primacy alone.

---

## 10. Research questions and falsifiability criteria

### 10.1 Formal research questions

The decisive open questions are mathematical, not rhetorical.

| Question | Required demonstration | Failure condition |
|---|---|---|
| Q1. Event reconstruction | Construct \(M=\mathfrak E[\Phi]\) with a proof of smoothness and \(\dim M=4\). | Dependence on a pre-existing four-manifold or a freely selected dimension. |
| Q2. Lorentzian emergence | Derive inertia \((1,3)\) from the phase principal symbol or a nondegenerate bilinear construction. | Positive response metric, more than one time direction, or instability. |
| Q3. Single cone | Prove \(P_A(k)\propto g^{\mu\nu}k_\mu k_\nu\) for every light mode. | Birefringence, multimetric propagation, or uncontrolled Lorentz violation. |
| Q4. Gauge identity | Derive the phase-originating transformation whose infrared action is \(\delta g_{\mu\nu}=\nabla_\mu\xi_\nu+\nabla_\nu\xi_\mu\). | An effective metric equation without the associated Noether/Bianchi identity. |
| Q5. Einstein operator | Compute the coarse-grained effective action and verify P-2 rather than inserting \(\sqrt{-g}R\). | Einstein–Hilbert term postulated, tuned, or mixed with unsuppressed extra modes. |
| Q6. Parameter closure | Specify \(\theta\mapsto\mathcal O\), show \(\operatorname{rank}J=p\), and show target compatibility. | More independent functional/parameter freedom than identifiable observables. |
| Q7. Empirical bridge | Derive the weak-field, wave, and cosmological observables from the same identified realization. | Separate tuning of each observational sector. |

### 10.2 Falsifiability criteria

A specific UPT realization that asserts an Einstein limit is falsified within this program if any one of the following occurs:

1. Its purported response metric is positive semidefinite in the alleged physical phase, or becomes singular on the collective coordinates required to define position.
2. The effective dimension is not robustly four under the proposed scale map and phase-sector perturbations.
3. Distinct matter or collective modes possess different low-energy characteristic cones.
4. The metric equation lacks an emergent gauge identity, has extra unsuppressed polarizations, or cannot be obtained from a local infrared action without insertion of the target term.
5. The full TN-02 Jacobian is rank deficient, or matching the Einstein limit demands parameters that enter only to repair target residuals.
6. The phase theory cannot furnish a finite nonzero gravitational coupling with the dimensions and normalization required by its own operational units.

These are direct failure criteria, not aesthetic preferences. They implement the distinction between a phase-inspired analogy and a derivation.

---

## 11. Formal claim ledger

The ledger separates what the UPT framework establishes at its present level from what belongs to established mathematics, what fails, and what remains open.

| Claim | Classification | Formal verdict | Basis |
|---|---|---|---|
| A differentiable universal equation has a linear stability operator \(\mathscr L_\Phi=D_\Phi\mathscr F\). | **Defined** | Established as notation once differentiability is assumed. | Equation (2.2). |
| A critical Fredholm kernel yields finite local order parameters via Lyapunov–Schmidt reduction. | **Imported / derived conditionally** | Established under (4.3) and splitting hypotheses. | Proposition 4.1. |
| Topological invariants can classify phase sectors when boundary and finite-excess hypotheses hold. | **Imported / conditional** | Established generically in topology, not uniquely UPT-specific. | Equation (4.7). |
| A real stable reduced Hessian yields a response geometry \(g^\Phi=T S^{-1}T^{\mathsf T}\). | **Defined / derived conditionally** | A positive-semidefinite tensor on a selected control/moduli manifold. | Equation (5.2), Proposition 5.1. |
| Response geometry is uniquely physical spacetime geometry. | **Failed** | Its normalization is ambiguous; its domain is a chosen control/moduli space; no event reconstruction is derived. | Proposition 5.3; §6. |
| Stable phase response generically yields Lorentzian signature. | **Failed** | Stable real variational response is positive semidefinite. | Proposition 5.1. |
| Susceptibility produces a metric on exact soliton translation moduli. | **Failed** | The translation tangent is a zero mode; the inverse is undefined or projected response is degenerate. | Proposition 5.2; §8.3. |
| UPT I–X select \(d=4\). | **Failed** | The abstract substrate/configuration framework is dimensionally underdetermined. | §8.1. |
| UPT I–X enforce a universal Lorentz cone. | **Failed** | Multiple healthy phase modes can carry inequivalent principal cones. | §8.1–§8.3. |
| UPT I–X derive diffeomorphism invariance and the Bianchi identity. | **Failed** | No emergent local gauge transformation or action symmetry has been obtained. | §6. |
| Lovelock uniqueness yields the Einstein tensor in four dimensions. | **Established but generic** | Conditional on a pseudo-Riemannian metric and its natural, second-order, symmetric, divergence-free dynamics. | [1] |
| Consistent local massless spin-two self-coupling produces Einstein nonlinearity. | **Established but generic** | Conditional on the prior linear spin-two gauge theory; not a phase-emergence result. | [2] |
| A UPT realization can be parameter-identified and match Einstein observables. | **Open / presently unassessable** | No fixed realization, finite parameter list, or observable map exists; TN-02 cannot be passed. | §7. |
| A more restrictive UPT theory can derive Einsteinian spacetime. | **Open** | Requires proof of P-E through P-N without target insertion. | §9–§10. |

---

## 12. Conclusion

The minimal UPT postulates support a coherent structural program: phase configurations are admissible solutions of a universal equation; their linearized stability controls regularity and bifurcation; critical kernels can yield finite-dimensional order parameters; topological and spectral data can organize stable sectors; and effective observables may be sought as functionals of phase structure. These are legitimate foundations for an emergence program.

They do not presently derive Einsteinian spacetime. The key proposed bridge, \(g^\Phi=T\chi T^{\mathsf T}\), has a precisely identified domain and limitation. In a stable real variational phase it produces a positive-semidefinite response tensor, not a Lorentzian metric. On exact collective moduli it encounters the zero modes that make the susceptibility noninvertible. A projection prescription removes the singularity only by degenerating the directions intended to define emergent position. No step supplies an operational four-manifold, one universal causal cone, local diffeomorphism redundancy, a two-polarization massless spin-two sector, or an Einstein–Hilbert effective action.

The correct result is therefore negative and terminal: **Einstein’s spacetime is not derived from UPT I–X or from the supplied candidate realization.** It must not be inserted through a Lorentzian substrate, a chosen signature, a hand-selected Einstein–Hilbert term, a declared gauge group, or a parameter fit. A constructive continuation is possible only through explicit new postulates P-E through P-N and a fixed phase realization that survives the listed signature, zero-mode, cone, topology, dimensional, normalization, and TN-02 rank tests.

This conclusion converts an undifferentiated foundational aspiration into a falsifiable research program. The next decisive result is not a further analogy between phase and geometry. It is a concrete universal phase equation whose independently specified solution space yields \(\mathrm E_1\)–\(\mathrm E_6\) and whose complete parameter-to-observable map is identifiable without repair parameters.

---

## Source manuscripts supplied for this analysis

| Identifier | Manuscript | Role in the audit |
|---|---|---|
| S1 | *Universal Phase Theory: A Foundational Mathematical Framework for Phase Structure, Emergent Geometry, Dynamics, Topology, and Physical Reality* (uploaded manuscript). | Source of UPT postulates I–X, the operator hierarchy, the susceptibility-response metric, and the stated Einstein-limit research question. |
| S2 | *Universal Mathematical Phase Theory: A Formal Framework for Structural Phases, Bifurcation Operators, Order Parameters, and Universality Classes* (uploaded manuscript). | Source of the structural-phase, stability, and Lyapunov–Schmidt formalism. |
| S3 | *Candidate Realization of the Universal Phase Equation* (uploaded manuscript). | Source of the candidate variational equation and the proposed phase-to-susceptibility-to-metric chain. |

## References

[1] A. Navarro and J. Navarro, “[Lovelock’s theorem revisited](https://arxiv.org/html/1005.2386v4),” *Journal of Geometry and Physics* **61**, 1950–1959 (2011).  

[2] S. Deser, “[Self-interaction and gauge invariance](https://link.springer.com/article/10.1007/BF00759198),” *General Relativity and Gravitation* **1**, 9–18 (1970).  

[3] L. Sindoni, “[Emergent Models for Gravity: an Overview of Microscopic Models](https://arxiv.org/html/1110.0686v2),” *SIGMA* **8**, 027 (2012).  

[4] F. Girelli, S. Liberati, and L. Sindoni, “[Emergence of Lorentzian signature and scalar gravity](https://doi.org/10.1103/PhysRevD.79.044019),” *Physical Review D* **79**, 044019 (2009).  

[5] D. Tong, “[General Relativity, §4: The Einstein Equations](https://www.damtp.cam.ac.uk/user/tong/gr/grhtml/S4.html),” University of Cambridge lecture notes, accessed 27 August 2026.

[1]: https://arxiv.org/html/1005.2386v4
[2]: https://link.springer.com/article/10.1007/BF00759198
[3]: https://arxiv.org/html/1110.0686v2
[4]: https://doi.org/10.1103/PhysRevD.79.044019
[5]: https://www.damtp.cam.ac.uk/user/tong/gr/grhtml/S4.html
