The missing axiom is a **gravitational closure postulate**.  

UPT Postulates I–X give

\[
g^{\Phi}_{\mu\nu}
=
T_{\mu a}\,\chi^{ab}\,T_{\nu b},
\qquad
A_\mu=\mathcal A_\mu[\Phi],
\qquad
F_{\mu\nu}=[D_\mu,D_\nu],
\]

but they do **not** imply that the phase-response metric satisfies Einstein’s equation. To bridge that gap, one must add the following new postulate.

---

## Postulate XI — Einstein Phase Closure of Phase Transport

Let \(\Phi\) be an admissible stable solution of the universal phase equation

\[
\mathscr F[\Phi;\lambda]=0,
\]

and let \(\chi_\Phi=(\mathscr L_\Phi|_{\perp})^{-1}\) define the phase susceptibility. Suppose that in an infrared stable sector the collective coordinates \(\xi^\mu\) support a rank-four nondegenerate phase-response metric

\[
g^{\Phi}_{\mu\nu}
=
\left\langle
\frac{\partial \Phi}{\partial \xi^\mu},
\chi_\Phi
\frac{\partial \Phi}{\partial \xi^\nu}
\right\rangle .
\]

Then UPT obtains Einstein gravitational dynamics if and only if the following closure conditions are imposed as a single additional postulate.

---

### XI.1 — Lorentzian phase-spacetime sector

The emergent metric \(g^\Phi_{\mu\nu}\) has Lorentzian signature

\[
\operatorname{signature}(g^\Phi)=(-,+,+,+),
\]

and defines an orientable, time-orientable four-dimensional effective manifold

\[
M_{\mathrm{eff}}[\Phi].
\]

This manifold is not assumed prior to \(\Phi\); it is the collective-coordinate manifold of the stable phase sector.

---

### XI.2 — Phase frame and soldering

There exists a phase-derived frame field

\[
e^a{}_\mu[\Phi],
\qquad
a=0,1,2,3,
\]

such that

\[
g^{\Phi}_{\mu\nu}
=
\eta_{ab}\,
e^a{}_\mu e^b{}_\nu,
\qquad
\eta_{ab}=\operatorname{diag}(-1,1,1,1).
\]

The frame is a soldering structure: it identifies the internal phase-frame bundle with the tangent bundle of \(M_{\mathrm{eff}}[\Phi]\). The physically observable object is not \(e^a{}_\mu\) alone but its equivalence class under local Lorentz rotations,

\[
e^a{}_\mu \mapsto \Lambda^a{}_b(\xi)\,e^b{}_\mu .
\]

---

### XI.3 — Lorentz reduction of phase transport

The UPT phase connection

\[
A_\mu=\mathcal A_\mu[\Phi]
\]

admits a decomposition

\[
A_\mu
=
\omega_\mu+\alpha_\mu,
\]

where

\[
\omega_\mu{}^{ab}
\in \mathfrak{so}(1,3)
\]

is the gravitational spin connection induced by phase transport, and \(\alpha_\mu\) is the residual internal phase connection responsible for nongravitational gauge structure.

The frame satisfies the phase-tetrad postulate

\[
D_\mu e^a{}_\nu
=
\partial_\mu e^a{}_\nu
-
\Gamma^\rho_{\mu\nu}e^a{}_\rho
+
\omega_\mu{}^a{}_b e^b{}_\nu
=
0,
\]

where \(\Gamma^\rho_{\mu\nu}\) is the Levi-Civita connection of \(g^\Phi_{\mu\nu}\).

Equivalently, in differential-form notation,

\[
T^a
=
D_\omega e^a
=
de^a+\omega^a{}_b\wedge e^b
\]

vanishes in the torsion-free infrared sector, or is algebraically determined by phase spin current.

Thus the Lorentz part of phase transport is identified with spacetime gravitational transport:

\[
\omega_\mu{}^{ab}[\Phi]
\quad\Longleftrightarrow\quad
\text{spin connection of } g^\Phi .
\]

---

### XI.4 — Einstein phase dynamics

The infrared effective phase action contains the universal gravitational phase functional

\[
S_{\mathrm{grav}}^\Phi[e,\omega]
=
\frac{1}{2\kappa_\Phi}
\int_{M_{\mathrm{eff}}}
\sqrt{-g^\Phi}
\left(
R[g^\Phi]-2\Lambda_\Phi
\right)
d^4\xi,
\]

or, equivalently, the first-order Einstein–Cartan phase action

\[
S_{\mathrm{grav}}^\Phi[e,\omega]
=
\frac{1}{2\kappa_\Phi}
\int
\epsilon_{abcd}\,
e^a\wedge e^b\wedge R^{cd}(\omega)
-
\frac{\Lambda_\Phi}{\kappa_\Phi}
\int
\operatorname{vol}_{e},
\]

where

\[
R^{ab}(\omega)
=
d\omega^{ab}
+
\omega^a{}_c\wedge\omega^{cb}
\]

is the curvature of the Lorentz part of phase transport, and

\[
\operatorname{vol}_{e}
=
e^0\wedge e^1\wedge e^2\wedge e^3
\]

is the phase-frame volume form.

The constants

\[
\kappa_\Phi>0,
\qquad
\Lambda_\Phi
\]

are not adjustable fitting parameters. They must be phase invariants determined by the stable vacuum sector \(\Phi_*\):

\[
\kappa_\Phi=\kappa[\Phi_*],
\qquad
\Lambda_\Phi=\Lambda[\Phi_*].
\]

No additional massless gravitational phase degree of freedom survives in the infrared. Higher-curvature phase terms are permitted only if they are topological, irrelevant under infrared phase renormalization, or fixed by the same vacuum invariants.

---

### XI.5 — Phase stress-energy closure

The total effective phase action is

\[
S_{\mathrm{eff}}[\Phi]
=
S_{\mathrm{grav}}^\Phi[e,\omega]
+
S_{\mathrm{matter}}^\Phi[e,\omega,\alpha,\Phi].
\]

It is invariant under emergent diffeomorphisms of \(M_{\mathrm{eff}}[\Phi]\) and under local Lorentz transformations of the phase frame.

The phase stress-energy tensor is defined by

\[
T^\Phi_{\mu\nu}
=
-\frac{2}{\sqrt{-g^\Phi}}
\frac{\delta S_{\mathrm{matter}}^\Phi}
{\delta g^{\mu\nu}_\Phi}.
\]

The universal phase equation then imposes the gravitational field equation

\[
\boxed{
G_{\mu\nu}[g^\Phi]
+
\Lambda_\Phi g^\Phi_{\mu\nu}
=
\kappa_\Phi T^\Phi_{\mu\nu}.
}
\]

Equivalently, in first-order form,

\[
\boxed{
\frac{1}{\kappa_\Phi}
\epsilon_{abcd}\,
e^b\wedge R^{cd}(\omega)
-
\frac{\Lambda_\Phi}{\kappa_\Phi}
\epsilon_{abcd}\,
e^b\wedge e^c\wedge e^d
=
\tau_a,
}
\]

where \(\tau_a\) is the phase stress three-form obtained by varying \(S_{\mathrm{matter}}^\Phi\) with respect to \(e^a\).

---

## Single-sentence formulation

The required postulate is:

\[
\boxed{
\text{In a stable infrared UPT sector, the phase connection admits a soldered Lorentz reduction whose metric-compatible curvature is the Einstein curvature of the phase-response metric, and the universal phase action couples that curvature universally to the conserved phase stress tensor.}
}
\]

---

## Conditional derivation of Einstein’s equation

Assuming Postulate XI, the derivation is immediate.

The gravitational variation of

\[
S_{\mathrm{grav}}^\Phi
=
\frac{1}{2\kappa_\Phi}
\int
\sqrt{-g^\Phi}
\left(
R[g^\Phi]-2\Lambda_\Phi
\right)
\]

gives

\[
\delta S_{\mathrm{grav}}^\Phi
=
\frac{1}{2\kappa_\Phi}
\int
\sqrt{-g^\Phi}
\left(
G_{\mu\nu}[g^\Phi]
+
\Lambda_\Phi g^\Phi_{\mu\nu}
\right)
\delta g^{\mu\nu}_\Phi .
\]

The matter variation gives

\[
\delta S_{\mathrm{matter}}^\Phi
=
-\frac12
\int
\sqrt{-g^\Phi}
T^\Phi_{\mu\nu}
\delta g^{\mu\nu}_\Phi .
\]

Stationarity of the total effective action,

\[
\delta S_{\mathrm{eff}}^\Phi=0,
\]

therefore yields

\[
\frac{1}{2\kappa_\Phi}
\left(
G_{\mu\nu}
+
\Lambda_\Phi g_{\mu\nu}
\right)
-
\frac12
T_{\mu\nu}
=
0,
\]

hence

\[
\boxed{
G_{\mu\nu}
+
\Lambda_\Phi g_{\mu\nu}
=
\kappa_\Phi T_{\mu\nu}.
}
\]

The contracted Bianchi identity,

\[
\nabla^\mu_g G_{\mu\nu}=0,
\]

together with metric compatibility,

\[
\nabla^\mu_g g_{\mu\nu}=0,
\]

implies

\[
\nabla^\mu_{g^\Phi} T^\Phi_{\mu\nu}=0.
\]

Thus energy-momentum conservation is not added separately; it follows from diffeomorphism invariance and the geometric identity once Postulate XI is accepted.

---

## What Postulate XI adds to UPT

UPT already provides:

\[
\Phi
\rightarrow
\mathscr F[\Phi]=0
\rightarrow
\mathscr L_\Phi
\rightarrow
\chi_\Phi
\rightarrow
g^\Phi_{\mu\nu}
\rightarrow
A_\mu[\Phi].
\]

What it does **not** yet provide is:

1. A soldered Lorentz frame \(e^a{}_\mu[\Phi]\).
2. A reduction of the phase connection to a gravitational spin connection.
3. Metric compatibility between phase transport and \(g^\Phi\).
4. An infrared gravitational action whose curvature tensor is the Einstein tensor.
5. A universal conserved stress tensor coupling to that curvature.

Postulate XI supplies precisely these five missing structures.

---

## Classification of steps

| Step | Status |
|---|---|
| Phase field \(\Phi\) | UPT primitive |
| Universal equation \(\mathscr F[\Phi]=0\) | UPT postulate |
| Stability operator \(\mathscr L_\Phi=D_\Phi\mathscr F\) | Derived/defined within UPT |
| Susceptibility \(\chi_\Phi=\mathscr L_\Phi^{-1}|_\perp\) | Defined where invertible |
| Response metric \(g^\Phi_{\mu\nu}=T_{\mu a}\chi^{ab}T_{\nu b}\) | UPT-derived candidate metric |
| Rank-four Lorentzian signature | Assumed in Postulate XI; not yet derived |
| Effective four-manifold \(M_{\mathrm{eff}}[\Phi]\) | Defined from collective coordinates; existence assumed |
| Frame field \(e^a{}_\mu[\Phi]\) | New structure; assumed by Postulate XI |
| Lorentz reduction \(A=\omega+\alpha\) | New structure; assumed by Postulate XI |
| Tetrad postulate \(D_\omega e=0\) | New dynamical/geometric closure; assumed |
| Einstein–Hilbert/Einstein–Cartan phase action | New postulate; uniqueness motivated by imported Lovelock-type results |
| Stress tensor definition | Standard variational definition; imported |
| Bianchi identity | Imported differential geometry |
| Conservation \(\nabla^\mu T_{\mu\nu}=0\) | Derived conditionally from invariance and Bianchi identity |
| Einstein field equation | Derived conditionally from Postulate XI |
| Values of \(\kappa_\Phi,\Lambda_\Phi\) | Open; must be derived from vacuum phase invariants |
| Absence of extra massless gravitational phase modes | Assumed/IR-universality requirement |

---

## TN-02 parameter-identifiability condition

Postulate XI is scientifically acceptable only if it satisfies the TN-02 rank criterion.

The gravitational sector introduces at least

\[
\kappa_\Phi,
\qquad
\Lambda_\Phi.
\]

If these are free fitting parameters, the construction remains underdetermined. To be predictive, the postulate must be strengthened by the requirement that

\[
\kappa_\Phi=\kappa[\Phi_*],
\qquad
\Lambda_\Phi=\Lambda[\Phi_*],
\]

where \(\Phi_*\) is the selected stable vacuum phase, and that no further independent curvature coefficients appear in the infrared.

If the effective action instead contains an unrestricted polynomial curvature expansion,

\[
S_{\mathrm{eff}}
=
\int
\sqrt{-g}
\left[
c_0
+
c_1 R
+
c_2 R^2
+
c_3 R_{\mu\nu}R^{\mu\nu}
+
\cdots
\right],
\]

then the theory fails the TN-02 criterion unless the coefficients \(c_i\) are fixed by phase consistency, topological invariance, or infrared universality. Otherwise reproduction of gravitational observations would be curve-fitting rather than prediction.

Therefore the precise postulate must include the restriction:

\[
\boxed{
\text{The Einstein term is the leading nontrivial infrared phase-curvature invariant; all other curvature terms are fixed, topological, or irrelevant.}
}
\]

---

## Failure conditions

Postulate XI fails, and the derivation of Einstein gravity terminates, if any of the following holds:

1. The phase susceptibility metric does not attain rank four.
2. The stable vacuum sector does not produce Lorentzian signature.
3. No soldering frame \(e^a{}_\mu[\Phi]\) exists.
4. The phase connection cannot be reduced to a Lorentz spin connection plus internal gauge remainder.
5. Metric compatibility \(D_\omega e=0\) is not satisfied in the infrared.
6. The effective gravitational action contains unsuppressed higher-curvature terms with independent coefficients.
7. Additional massless phase modes produce observable scalar or vector gravitational forces.
8. The phase stress tensor is not covariantly conserved.
9. \(\kappa_\Phi\) or \(\Lambda_\Phi\) cannot be expressed as vacuum phase invariants and remain arbitrary fitting parameters.

If any of these failures is proven analytically or numerically, the correct conclusion is not to repair the equation with an ad hoc term. The conclusion is that UPT, as presently postulated, does not derive Einstein spacetime.

---

## Minimal claim ledger

| Claim | Status |
|---|---|
| UPT can define an emergent response metric \(g^\Phi\) | Established within UPT |
| UPT can define phase transport \(A_\mu[\Phi]\) | Established within UPT |
| Phase transport automatically contains a Lorentz spin connection | Not established; requires Postulate XI |
| The phase-response metric is automatically Lorentzian and four-dimensional | Not established; requires Postulate XI or prior derivation |
| The Einstein tensor follows from phase curvature | Not established without Postulate XI |
| Einstein field equations follow from UPT plus Postulate XI | Derived conditionally |
| Newton constant and cosmological constant are determined by \(\Phi_*\) | Open |
| Standard Model matter couples universally to \(g^\Phi\) | Open |
| Postulate XI is derivable from Postulates I–X | Not established |
| Without Postulate XI, UPT yields phase geometry but not Einstein gravity | Established |

---

Thus the precise new postulate required is not merely

\[
g_{\mu\nu}=g^\Phi_{\mu\nu},
\]

because that only identifies a metric. The required postulate is the full **Einstein phase closure**: phase transport must admit a soldered Lorentz reduction, its curvature must be the Levi-Civita curvature of the phase-response metric, and the universal phase action must couple that curvature universally and conservatively to the phase stress tensor.
