# UPT Postulate XI — Covariant Phase-Soldering and Metric Response

## A precise bridge from phase transport to Einsteinian field equations

### 1. Statement

> **Postulate XI (Covariant Phase-Soldering and Metric Response).**  
> There exists a scale interval \(\ell\ge \ell_{\mathrm{IR}}\) and a stable equivalence class of admissible phase configurations \([\Phi_\ell]\subset\mathcal C_\Phi/\mathscr G_\Phi\) for which phase transport induces, without a preassigned spacetime metric, an operational four-manifold \(M_\ell\), a rank-four Lorentz coframe bundle \(F_{\mathrm{Lor}}M_\ell\), and a nondegenerate soldering form
> \[
> e[\Phi_\ell]\in\Omega^1\!\left(M_\ell;\mathbb R^{1,3}\right),
> \qquad
> e^a{}_{\mu}[\Phi_\ell]:T_xM_\ell\xrightarrow{\sim}\mathbb R^{1,3}.
> \tag{XI.1}
> \]
> The induced metric and connection are the phase-invariant functionals
> \[
> g_{\mu\nu}[\Phi_\ell]
> :=\eta_{ab}e^a{}_{\mu}[\Phi_\ell]e^b{}_{\nu}[\Phi_\ell],
> \qquad
> \omega^{ab}[\Phi_\ell]\in\Omega^1\!\left(M_\ell;\mathfrak{so}(1,3)\right),
> \tag{XI.2}
> \]
> with \(\det g\ne0\), \(\operatorname{In}(g)=(1,3)\) or \((3,1)\), and torsion vanishing in the infrared:
> \[
> D_{\omega[\Phi_\ell]}e[\Phi_\ell]
> =O\!\left((L_\ell\nabla)^{-1}\right).
> \tag{XI.3}
> \]
> The infrared phase effective action obtained by integrating out every phase mode not represented by \((e,\omega)\) is local, invariant under phase-induced local Lorentz transformations and phase-induced diffeomorphisms of \(M_\ell\), and has a derivative expansion whose unique unsuppressed metric sector is
> \[
> \Gamma_\ell[\Phi]
> =\frac{1}{2\kappa_\ell}
> \int_{M_\ell}\epsilon_{abcd}\,e^a\wedge e^b\wedge R^{cd}[\omega]
> -\frac{\Lambda_\ell}{12\kappa_\ell}
> \int_{M_\ell}\epsilon_{abcd}\,e^a\wedge e^b\wedge e^c\wedge e^d
> +\Gamma_{\mathrm{op}}[e,\Psi]
> +O\!\left((L_\ell\nabla)^{-2}\right),
> \tag{XI.4}
> \]
> where \(\Psi\) denotes all operationally defined low-energy collective sectors. Their principal symbols share the null cone of \(g[\Phi_\ell]\), and their stress tensor is defined by
> \[
> T_{\mu\nu}
> :=-\frac{2}{\sqrt{-g}}
> \frac{\delta\Gamma_{\mathrm{op}}}{\delta g^{\mu\nu}}.
> \tag{XI.5}
> \]
> The coefficients \(\kappa_\ell\) and \(\Lambda_\ell\) are either fixed phase invariants or components of an explicitly stated finite observable map satisfying the TN-02 rank condition.

This is one postulate, not a theorem of UPT I–X. Its clauses are inseparable: a phase connection alone does not yield a spacetime connection; a coframe alone does not yield a dynamical Einstein tensor; and a metric action alone does not guarantee universal causal propagation.

---

## 2. Why the postulate is the missing bridge

The phase-transport structure available in minimal UPT is an internal principal-bundle connection,

\[
A^\Phi\in\Omega^1(N;\operatorname{ad}P_\Phi),
\qquad
F^\Phi=dA^\Phi+A^\Phi\wedge A^\Phi,
\qquad
\operatorname{Hol}_\gamma(A^\Phi)
=\mathcal P\exp\!\left(-\oint_\gamma A^\Phi\right).
\tag{XI.6}
\]

It compares phase frames along curves in a candidate manifold \(N\). It does **not** identify those frames with tangent vectors. Equation (XI.1) supplies exactly the omitted datum: the coframe is a nondegenerate bundle morphism, or soldering form, that identifies the phase-frame representation with the tangent bundle of an operationally reconstructed manifold. It is the required bridge

\[
(P_\Phi,A^\Phi,\operatorname{Hol}A^\Phi)
\quad\xRightarrow[\text{Postulate XI}]{}\quad
(F_{\mathrm{Lor}}M,e,\omega)
\quad\Longrightarrow\quad
(g,\nabla).
\tag{XI.7}
\]

The words **operational four-manifold** are substantive. The postulate does not set the former phase substrate \(\mathcal X\) equal to spacetime. It requires a rule \(\mathfrak E\) intrinsic to phase-equivalence classes such that

\[
M_\ell=\mathfrak E[\Phi_\ell],
\qquad
\dim M_\ell=4,
\tag{XI.8}
\]

and requires this rule to be covariant under admissible phase transformations. If a candidate realization begins by declaring \(\mathcal X=M^4\), it does not satisfy (XI.8) and has not implemented the postulate.

---

## 3. Conditional derivation of Einstein’s equation

The derivation below is valid **only after** Postulate XI has been accepted and realized.

Varying (XI.4) with respect to \(\omega^{ab}\) yields the infrared torsion condition

\[
D_\omega(e^a\wedge e^b)=0
\quad\Longrightarrow\quad
D_\omega e^a=0,
\tag{XI.9}
\]

for an invertible tetrad and in the absence of unsuppressed spin-torsion sources. Thus \(\omega=\omega(e)\) is the Levi–Civita spin connection. Variation with respect to \(e^a{}_{\mu}\), equivalently the metric, gives

\[
G_{\mu\nu}[g]+
\Lambda_\ell g_{\mu\nu}
=\kappa_\ell T_{\mu\nu}
+O\!\left((L_\ell\nabla)^{-2}\right).
\tag{XI.10}
\]

The phase-induced diffeomorphism invariance of \(\Gamma_\ell\) gives the Noether identity

\[
\nabla^\mu
\left(G_{\mu\nu}+\Lambda_\ell g_{\mu\nu}-\kappa_\ell T_{\mu\nu}\right)=0,
\qquad
\nabla^\mu T_{\mu\nu}=0
\tag{XI.11}
\]

on the operational matter equations. Equation (XI.10) is then an **Einstein limit** of the phase theory, not a term introduced separately into the microscopic universal phase equation.

The logical status is summarized below.

| Step | Status | Reason |
|---|---|---|
| \(\mathscr F[\Phi;\lambda]=0\), \(\mathscr L_\Phi=D_\Phi\mathscr F\), \(\Delta_\Phi\), \(\boldsymbol\chi_\Phi\) | UPT I–X formalism | It organizes phase stability and response but supplies neither an event manifold nor a Lorentz coframe. |
| Phase connection \(A^\Phi\) and holonomy | Defined / bundle-theoretic | It is an internal phase transport structure. |
| \(M_\ell,e,\omega\) from phase transport | **New postulate** | This is the phase–tangent-bundle identification absent from UPT I–X. |
| Lorentzian inertia and single causal cone | **New postulate** | A stable susceptibility metric is generally positive semidefinite and cannot supply this result. |
| Local invariant infrared functional \(\Gamma_\ell\) | **New postulate** | Scale dependence alone does not yield an action, locality, or diffeomorphism gauge symmetry. |
| Einstein equation (XI.10) | Derived conditionally | It follows from varying (XI.4), subject to the stated infrared conditions. |

---

## 4. Non-ad hoc content and TN-02 closure

Postulate XI is not permitted to be implemented by simply appending an Einstein–Hilbert action to \(S_\Phi\). The required map is

\[
\mathfrak B_\ell:
[\Phi_\ell]
\longmapsto
\left(M_\ell,e[\Phi_\ell],\omega[\Phi_\ell],\Gamma_\ell\right),
\tag{XI.12}
\]

and each item in its codomain must be computed from phase configurations, phase transport, and the specified coarse-graining map. The Lorentz group, the coframe rank, the signature, and the coefficients in (XI.4) must be outputs of this map or independently measured parameters of a closed realization; they may not be selected because they reproduce the target theory.

For a realization with adjustable parameter vector \(\theta\in\mathbb R^p\), define an observable vector that includes structural as well as numerical outputs:

\[
\mathcal O(\theta)=
\left(
 d_{\rm eff},\operatorname{In}(g),
 \{C_A-C_B\}_{A,B},
 N_{\rm grav},
 \kappa_\ell,\Lambda_\ell,
 \ldots
\right).
\tag{XI.13}
\]

Here \(C_A\) is the characteristic cone of the operational mode \(\Psi_A\), and \(N_{\rm grav}\) is the number of unsuppressed massless gravitational polarizations. Let

\[
J_{Ai}=\frac{\partial\mathcal O_A}{\partial\theta^i}.
\tag{XI.14}
\]

The TN-02 admissibility test is

\[
m\ge p,
\qquad
\operatorname{rank}J=p,
\qquad
\operatorname{rank}J=
\operatorname{rank}\left[J\mid\mathcal O^{\star}-\mathcal O(\theta)\right].
\tag{XI.15}
\]

A realization failing (XI.15) has not derived its Einstein limit; it has merely retained nonidentifiable freedom. The structural components of \(\mathcal O\) cannot be omitted from this rank test.

---

## 5. Falsifiability conditions

Postulate XI is rejected for a candidate phase realization if any one of the following is established.

| Failure mode | Decisive test |
|---|---|
| No emergent event manifold | The alleged \(M_\ell\) is assumed as the base space, has nonrobust dimension, or lacks an operational reconstruction \(\mathfrak E[\Phi_\ell]\). |
| No true soldering | \(e^a{}_{\mu}\) is rank deficient, is freely added, or does not arise from a phase-invariant map. |
| Wrong signature | \(g=\eta_{ab}e^a\otimes e^b\) is degenerate, Euclidean, ultrahyperbolic, or signature-unstable. |
| Multimetric propagation | Two low-energy operational modes have inequivalent characteristic cones. |
| Missing gauge identity | The coarse-grained action lacks phase-induced diffeomorphism invariance or fails the Noether identity (XI.11). |
| Extra gravitational content | The infrared metric sector has unsuppressed scalar/vector modes, higher-derivative ghosts, or more than two massless helicity-two polarizations. |
| Target insertion | \(\sqrt{-g}R\), \(\eta_{ab}\), \(\dim M=4\), or \(\kappa_\ell\) is imposed without derivation or independent calibration. |
| Identifiability failure | The full structural-and-numerical map violates (XI.15). |

---

## 6. Scope

Postulate XI is stronger than the prior UPT postulates because it carries the exact missing content: the emergence of a Lorentzian tangent geometry from phase transport, the gauge identity needed for a conserved Einstein tensor, and an infrared action with a controlled derivative expansion. It is therefore **not** a consequence of phase primacy, phase stability, susceptibility, topology, or holonomy alone.

If a concrete universal phase equation realizes (XI.1)–(XI.15) without target insertion, UPT yields Einstein gravity in the infrared to the stated derivative order. If it cannot, UPT remains a phase-structural framework without an established gravitational completion.
