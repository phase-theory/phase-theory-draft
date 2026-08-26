# Phase Topology Microscopy of Electron–Hydrogen Scattering
## Exact Phase-Shift Matrix and Cross-Section Functionals from the Universal Phase Equation

**Dust LLC — Universal Phase Theory Preprint Series**  
**Formal Supplement to *Phase Topology Microscopy of the Hydrogen Atom***  
**26 August 2026**

---

## Abstract

This supplement formulates the exact Phase Topology Microscopy (PTM) scattering observables for electron–hydrogen interaction. The incident electron, target hydrogen atom, scattering channels, asymptotic geometry, phase-shift matrix, and cross-section are all treated as derived structures of the universal phase equation,

\[
\mathscr F[\Phi;\lambda]=0,
\qquad
\mathscr L_\Phi=D_\Phi\mathscr F[\Phi;\lambda],
\qquad
\Delta_\Phi=\operatorname{Det}_\Phi(\mathscr L_\Phi),
\qquad
\boldsymbol\chi_\Phi=(\Pi_N\mathscr L_\Phi\Pi_N)^{-1}.
\tag{A.1}
\]

The scattering configuration is a finite-flux solution with an electron-sector orbit asymptotically separated from the stable hydrogen orbit. After the universal equation has generated an emergent stationary transport parameter, a physical response geometry, and a prequantum scattering sector, its projected linearization defines an exact scattering generator \(\mathbb H_{eH,\Phi}\). Feshbach projection of this generator yields an exact energy-dependent optical phase interaction that contains elastic response, target excitation, ionization, exchange, polarization, virtual phase sectors, and all unresolved channels without the insertion of an empirical scattering potential.

The PTM scattering matrix is defined by Møller phase transport. In a flux-normalized channel frame its on-shell matrix is

\[
S^{\mathfrak j}_{\Phi,ba}(E)
=
\delta_{ba}\mathbf1
-2\pi i\,
\varrho_b(E)^{1/2}
\Gamma_b(E)^\dagger
\mathbb T^{+,\mathfrak j}_\Phi(E)
\Gamma_a(E)
\varrho_a(E)^{1/2}.
\tag{A.2}
\]

The exact Hermitian PTM K matrix and matrix phase shift are

\[
\mathbb K^{\mathfrak j}_\Phi
=-i(S^{\mathfrak j}_\Phi-\mathbf1)(S^{\mathfrak j}_\Phi+\mathbf1)^{-1},
\qquad
\boldsymbol\Delta^{\mathfrak j}_\Phi
=\arctan\mathbb K^{\mathfrak j}_\Phi,
\qquad
S^{\mathfrak j}_\Phi=e^{2i\boldsymbol\Delta^{\mathfrak j}_\Phi}.
\tag{A.3}
\]

The differential, integrated channel, elastic, inelastic, and total cross-sections then follow as invariant phase-flux ratios. The physical amplitude is automatically direct-minus-exchange for the emergent fermionic electron sector because the two electron-sector histories are projected by the derived exchange action on the phase bundle. The final construction supplies a calculable PTM scattering map containing topological flow, holonomy, phase shifts, cross-sections, and Wigner–Smith phase response. It specifies the exact quantities that an explicit universal phase equation must compute in order to make a falsifiable electron–hydrogen scattering prediction. [1] [2] [3]

---

## 1. Scattering datum and asymptotic phase factorization

Let \(\Phi_H=\Phi_p\star\Phi_{e_H}\) be the stable bound hydrogen orbit derived from the universal phase equation. Let \(\Phi_{e}^{\rm in}\) be a second electron-sector orbit prepared at asymptotic phase distance from \(\Phi_H\). The electron–hydrogen scattering configuration is not a point particle incident upon a prescribed atomic potential. It is the scattering-sector solution

\[
\boxed{
\mathscr F[\Phi_{eH}^{(+)};\lambda_{eH}(E)]=0,
\qquad
\Phi_{eH}^{(+)}
\underset{D_{eH}\to\infty}{\longrightarrow}
\Phi_H\sqcup\Phi_e^{\rm in}+\zeta_{eH}^{(+)}.
}
\tag{1.1}
\]

Here \(\sqcup\) denotes asymptotic disjoint composition in the quotient solution space, \(D_{eH}\) is the phase distance induced by the scattering response metric, and \(\zeta_{eH}^{(+)}\) is the outgoing phase response. The superscript \((+)\) selects the outgoing phase-flux boundary condition. The asymptotic factorization condition is itself part of the solution class of \(\mathscr F\); it is not a decomposition placed into a pre-existing three-dimensional space.

Let \(\mathcal Z_{eH}\) be the span of exact phase-frame motions and collective moduli of the scattering configuration, and select a normal complement

\[
T_{\Phi_{eH}}\mathcal C_\Phi=\mathcal Z_{eH}\oplus N_{eH}.
\tag{1.2}
\]

The physical scattering response is governed by

\[
\mathscr L_{eH,\Phi}^{\perp}
:=
\Pi_{N_{eH}}D_\Phi\mathscr F[\Phi_{eH};\lambda_{eH}]\Pi_{N_{eH}},
\qquad
\boldsymbol\chi_{eH,\Phi}
:=
(\mathscr L_{eH,\Phi}^{\perp})^{-1}.
\tag{1.3}
\]

The projection is not optional. An unprojected scattering resolvent would count exact phase frame changes, translation of the atomic collective centre, or gauge-equivalent exchange descriptions as physical scattering response.

The scattering construction requires the same UPT hierarchy as the bound-state construction:

\[
\Phi
\longrightarrow
\text{topological sector}
\longrightarrow
\text{response geometry}
\longrightarrow
\text{phase connection}
\longrightarrow
\text{asymptotic transport}
\longrightarrow
\text{scattering observables}.
\tag{1.4}
\]

In particular, the response metric

\[
 g^{(eH)}_{ij}=T_{ia}^{(eH)}\chi_{eH}^{ab}T_{jb}^{(eH)}
\tag{1.5}
\]

defines the physical phase-distance stratum on which asymptotic flux, scattering angle, and channel velocity are meaningful. The asymptotic connection \(\mathcal A_{eH}[\Phi]\) defines transport frames for the channel fibres. Both are derived phase functionals.

---

## 2. Emergent scattering generator and channel projectors

Once the phase dynamics supplies an emergent stationary transport parameter \(\tau_\Phi\), a conserved phase flux, and a prequantum scattering bundle, the projected linearization determines a self-adjoint physical scattering generator,

\[
\boxed{
\mathbb H_{eH,\Phi}
=
\mathbb H_{\rm as,\Phi}
+
\mathbb V_{eH,\Phi}.
}
\tag{2.1}
\]

The reference generator \(\mathbb H_{\rm as,\Phi}\) contains all asymptotically nonvanishing response geometry and connection transport. The residual operator \(\mathbb V_{eH,\Phi}\) is the interaction induced by the full nonlinear phase solution after asymptotic factorization. It is not an assumed electron–atom potential.

A channel at total phase energy \(E\) is denoted

\[
a=(n,\alpha;\mathbf k_a,\sigma_a;\mathfrak j,\gamma_a).
\tag{2.2}
\]

The labels have a derivational meaning:

| Channel datum | PTM origin |
|---|---|
| \(n\) | Discrete hydrogen phase-sector spectral stratum |
| \(\alpha\) | Residual holonomy or internal phase label of the target orbit |
| \(\mathbf k_a\) | Asymptotic relative phase momentum on the response geometry |
| \(\sigma_a\) | Incident electron-sector transport label |
| \(\mathfrak j\) | Irreducible block of the derived rotation–holonomy transport group |
| \(\gamma_a\) | Multiplicity space within the residual transport representation |

A channel opens when

\[
E>E_n^H,
\qquad
E=E_n^H+\varepsilon_a(k_a),
\qquad
v_a(E):=\frac{\partial\varepsilon_a}{\partial k_a}>0.
\tag{2.3}
\]

Let \(P_a(E)\) be the corresponding asymptotic channel projector. Then

\[
P(E)=\sum_{a\in\mathrm{open}(E)}P_a(E),
\qquad
Q(E)=\mathbf1-P(E).
\tag{2.4}
\]

The incident electron and the electron bound inside the target hydrogen orbit belong to the same emergent electron phase sector. Their exchange is an action \(\mathsf P_{e,e_H}\) on the two-electron asymptotic phase fibre. The physical channel projection is therefore

\[
\boxed{
P_a^{\rm phys}(E)=P_a(E)\Pi_{\varepsilon_\rho},
\qquad
\Pi_{\varepsilon_\rho}:=
\frac12\left(\mathbf1+\varepsilon_\rho\mathsf P_{e,e_H}\right).
}
\tag{2.5}
\]

For the emergent fermionic electron sector, the exchange character is \(\varepsilon_\rho=-1\). This is the exact phase-bundle origin of exchange antisymmetry in electron–hydrogen scattering.

---

## 3. Exact Feshbach phase interaction

The open phase channels are affected by every closed or unresolved phase sector. Their exact effect is given by the Feshbach-reduced generator,

\[
\boxed{
\mathbb H_{\rm eff}^{P,+}(E)
=
P\mathbb H_{eH,\Phi}P
+
P\mathbb H_{eH,\Phi}Q
\bigl(E-Q\mathbb H_{eH,\Phi}Q+i0\bigr)^{-1}
Q\mathbb H_{eH,\Phi}P.
}
\tag{3.1}
\]

With \(\mathbb V=\mathbb H_{eH,\Phi}-\mathbb H_{\rm as,\Phi}\), define the exact PTM optical phase interaction by

\[
\boxed{
\mathbb U^{P,+}_\Phi(E)
=
P\mathbb VP
+
P\mathbb VQ
\bigl(E-Q\mathbb H_{eH,\Phi}Q+i0\bigr)^{-1}
Q\mathbb VP.
}
\tag{3.2}
\]

Equation (3.2) contains the complete dynamical content normally separated into direct scattering, exchange, polarization, virtual excitation, resonant intermediate configurations, and ionization coupling. In PTM these are not a sum of phenomenological atomic potentials. They are the projected resolvent of one universal phase generator.

The exact transition operator is

\[
\boxed{
\mathbb T^+_\Phi(E)
=
\mathbb V
+
\mathbb V
\bigl(E-\mathbb H_{\rm as,\Phi}+i0\bigr)^{-1}
\mathbb T^+_\Phi(E).
}
\tag{3.3}
\]

On the physical open space this becomes

\[
\mathbb T^+_{PP,\Phi}(E)
=
\mathbb U^{P,+}_\Phi(E)
+
\mathbb U^{P,+}_\Phi(E)
\bigl(E-P\mathbb H_{\rm as,\Phi}P+i0\bigr)^{-1}
\mathbb T^+_{PP,\Phi}(E).
\tag{3.4}
\]

These relations are exact once \(\mathbb H_{eH,\Phi}\) is derived from the universal phase equation. They define the scattering computation without importing an electron–hydrogen interaction potential.

---

## 4. Møller phase transport and the exact PTM S matrix

The asymptotic phase Møller maps are

\[
\Omega_\pm
:=
\operatorname*{s-lim}_{\tau_\Phi\to\pm\infty}
\exp\!\left(\frac{i}{\hbar_\Phi}\mathbb H_{eH,\Phi}\tau_\Phi\right)
\exp\!\left(-\frac{i}{\hbar_\Phi}\mathbb H_{\rm as,\Phi}\tau_\Phi\right).
\tag{4.1}
\]

The exact scattering map is

\[
\mathbb S_\Phi:=\Omega_+^\dagger\Omega_-.
\tag{4.2}
\]

Let \(\Gamma_a(E)\) inject a flux-normalized asymptotic channel fibre into the physical scattering sector and let \(\varrho_a(E)\) be its invariant density of states. The on-shell PTM S matrix is

\[
\boxed{
S^{\mathfrak j}_{\Phi,ba}(E)
=
\delta_{ba}\mathbf1_{\gamma_a}
-2\pi i\,
\varrho_b(E)^{1/2}
\Gamma_b(E)^\dagger
\mathbb T^{+,\mathfrak j}_\Phi(E)
\Gamma_a(E)
\varrho_a(E)^{1/2}.
}
\tag{4.3}
\]

If every open phase-flux channel is included,

\[
S_\Phi^{\mathfrak j\dagger}(E)S_\Phi^{\mathfrak j}(E)=\mathbf1.
\tag{4.4}
\]

When an observational subspace omits open target-excitation or ionization channels, its restricted S matrix is contractive. The deficit is not a loss of phase flux. It is an exact reconstruction of flux entering channels excluded by the observation map.

In a parallel asymptotic phase frame, the matrix factorizes as

\[
S_\Phi^{\mathfrak j}(E)
=
\mathcal U_{\rm out}^{\mathfrak j}(E)
\widetilde S_{\rm dyn}^{\mathfrak j}(E)
\mathcal U_{\rm in}^{\mathfrak j}(E)^{-1},
\tag{4.5}
\]

where \(\mathcal U_{\rm in/out}\) are Wilson transports of the derived phase connection. This factorization separates but does not disconnect dynamical phase response from transport holonomy. The spectrum of \(S_\Phi^{\mathfrak j}\), its conjugacy class, and its trace cross-sections are gauge invariant.

---

## 5. Exact K matrix and phase-shift matrix

The PTM K matrix is the Cayley transform of the complete flux-preserving S matrix:

\[
\boxed{
\mathbb K_\Phi^{\mathfrak j}(E)
:=-i
\bigl(S_\Phi^{\mathfrak j}(E)-\mathbf1\bigr)
\bigl(S_\Phi^{\mathfrak j}(E)+\mathbf1\bigr)^{-1}.
}
\tag{5.1}
\]

Equation (4.4) implies

\[
\mathbb K_\Phi^{\mathfrak j}(E)
=
\mathbb K_\Phi^{\mathfrak j\dagger}(E).
\tag{5.2}
\]

The exact **matrix phase shift** is the Hermitian functional calculus

\[
\boxed{
\boldsymbol\Delta_\Phi^{\mathfrak j}(E)
:=
\arctan\mathbb K_\Phi^{\mathfrak j}(E),
\qquad
S_\Phi^{\mathfrak j}(E)
=
\exp\!\left[2i\boldsymbol\Delta_\Phi^{\mathfrak j}(E)\right].
}
\tag{5.3}
\]

Equivalently,

\[
S_\Phi^{\mathfrak j}(E)
=
U_\Phi^{\mathfrak j}(E)
\operatorname{diag}\left(e^{2i\delta^{\mathfrak j}_{\Phi,\nu}(E)\right)
U_\Phi^{\mathfrak j\dagger}(E).
\tag{5.4}
\]

The eigenphases \(\delta^{\mathfrak j}_{\Phi,\nu}\) are the primary PTM phase-shift observables. In coupled electron–hydrogen channels, the eigenvector transport \(U_\Phi^{\mathfrak j}\) is also observable through transition-resolved cross-sections. An eigenphase table alone does not determine a specified target final state.

A resonance occurs when the analytically continued projected resolvent in (3.1) has a pole. Its observable signature is a rapid eigenphase flow, governed by a positive eigenvalue of the Wigner–Smith phase-response matrix defined below. The same event appears in UPT as a scattering-sector near-zero of the reduced phase bifurcation operator.

---

## 6. Exact scattering amplitude and identical-sector exchange

Let \(\mathcal Y_{a\mu}^{\mathfrak j}(\widehat k)\) be flux-normalized harmonics of the derived asymptotic rotation–holonomy bundle. In the convention in which their scalar limit is the ordinary spherical-harmonic basis, the exact partial-wave amplitude is

\[
\boxed{
\mathsf f_{ba}(\widehat k_b,\widehat k_a;E)
=
\frac{2\pi}{i\sqrt{k_ak_b}}
\sum_{\mathfrak j}\sum_{\mu,\lambda}
\mathcal Y_{b\mu}^{\mathfrak j}(\widehat k_b)
\bigl[S^{\mathfrak j}_{\Phi,ba}(E)-\delta_{ba}\mathbf1\bigr]_{\mu\lambda}
\mathcal Y_{a\lambda}^{\mathfrak j\dagger}(\widehat k_a).
}
\tag{6.1}
\]

For a single scalar channel on a flat asymptotic response stratum, (6.1) becomes

\[
\boxed{
f_\Phi(\theta;E)
=
\frac{1}{2ik}
\sum_{\ell=0}^{\infty}(2\ell+1)
\left(e^{2i\delta_{\Phi,\ell}(E)}-1\right)
P_\ell(\cos\theta).
}
\tag{6.2}
\]

The physical amplitude is the exchange-projected amplitude,

\[
\boxed{
\mathsf f_{ba}^{\rm phys}
=
\mathsf f_{ba}^{\rm dir}
+
\varepsilon_\rho\,
\mathsf X_{e,e_H}\!\cdot\mathsf f_{ba}^{\rm ex},
\qquad
\varepsilon_\rho=-1
\quad\text{for the emergent fermionic electron sector}.
}
\tag{6.3}
\]

The exchange map \(\mathsf X_{e,e_H}\) simultaneously rearranges asymptotic phase arguments and channel transport fibres. Equation (6.3) is therefore not a phenomenological direct-minus-exchange prescription. It is the image of the phase-bundle exchange projector (2.5).

---

## 7. Differential and integrated PTM cross-sections

Let \(v_a=\partial\varepsilon_a/\partial k_a\) and \(v_b=\partial\varepsilon_b/\partial k_b\) be the incident and outgoing asymptotic phase group velocities. Let \(d_a\) be the dimension of the unobserved incoming transport multiplet. The exact differential cross-section is the ratio of outgoing to incident invariant phase flux:

\[
\boxed{
\frac{d\sigma^{\Phi}_{b\leftarrow a}}{d\Omega_b}(E)
=
\frac{v_b(E)}{v_a(E)}\,
\frac{1}{d_a}
\operatorname{tr}_{\gamma_a,\gamma_b}
\left[
\mathsf f_{ba}^{\rm phys\dagger}
\mathsf f_{ba}^{\rm phys}
\right].
}
\tag{7.1}
\]

For a prepared incoming transport density matrix \(\rho_a\), the polarization-resolved observable is

\[
\frac{d\sigma^{\Phi}_{b\leftarrow\rho_a}}{d\Omega_b}
=
\frac{v_b}{v_a}
\operatorname{tr}
\left(
\mathsf f_{ba}^{\rm phys}\rho_a
\mathsf f_{ba}^{\rm phys\dagger}
\right).
\tag{7.2}
\]

Orthonormality of the asymptotic phase harmonics gives the exact integrated channel cross-section,

\[
\boxed{
\sigma^{\Phi}_{b\leftarrow a}(E)
=
\frac{\pi}{k_a^2d_a}
\sum_{\mathfrak j}
\operatorname{tr}
\left[
\bigl(S^{\mathfrak j}_{\Phi,ba}-\delta_{ba}\mathbf1\bigr)^\dagger
\bigl(S^{\mathfrak j}_{\Phi,ba}-\delta_{ba}\mathbf1\bigr)
\right].
}
\tag{7.3}
\]

The common prefactor in (7.3) applies to electron–hydrogen channels sharing the same asymptotic reduced phase inertia. In the general response geometry, \(k_a^{-2}\) is replaced by the invariant inverse incident flux-area factor determined by \(g^{(eH)}\) and the channel injection \(\Gamma_a(E)\). The operator expression in (4.3) remains exact in either normalization.

The elastic, inelastic, and total PTM cross-sections are

\[
\sigma^{\Phi}_{\rm el,a}
=
\frac{\pi}{k_a^2d_a}
\sum_{\mathfrak j}
\operatorname{tr}
\left[
\bigl(S_{\Phi,aa}^{\mathfrak j}-\mathbf1\bigr)^\dagger
\bigl(S_{\Phi,aa}^{\mathfrak j}-\mathbf1\bigr)
\right],
\tag{7.4}
\]

\[
\sigma^{\Phi}_{\rm inel,a}
=
\frac{\pi}{k_a^2d_a}
\sum_{\mathfrak j}\sum_{b\neq a}^{\rm open}
\operatorname{tr}
\left[
S_{\Phi,ba}^{\mathfrak j\dagger}S_{\Phi,ba}^{\mathfrak j}
\right],
\tag{7.5}
\]

\[
\boxed{
\sigma^{\Phi}_{\rm tot,a}
=
\frac{2\pi}{k_a^2d_a}
\sum_{\mathfrak j}
\operatorname{Re}\operatorname{tr}
\left(
\mathbf1-S_{\Phi,aa}^{\mathfrak j}\right)
=
\sigma^{\Phi}_{\rm el,a}+\sigma^{\Phi}_{\rm inel,a}.
}
\tag{7.6}
\]

Equation (7.6) is the PTM optical theorem. It follows from the flux unitarity of the complete scattering matrix and shows that every loss of elastic phase flux is reconstructed as a calculated open-channel transition.

---

## 8. Cross-sections in terms of the phase-shift matrix

The matrix identity

\[
\frac{S_\Phi^{\mathfrak j}-\mathbf1}{2i}
=
 e^{i\boldsymbol\Delta_\Phi^{\mathfrak j}}
\sin\boldsymbol\Delta_\Phi^{\mathfrak j}
\tag{8.1}
\]

gives, for a complete purely elastic \(\mathfrak j\)-block,

\[
\boxed{
\sigma^{\Phi,\mathfrak j}_{\rm el,a}(E)
=
\frac{4\pi}{k_a^2d_a}
\operatorname{tr}_a
\left[
\sin^2\boldsymbol\Delta_\Phi^{\mathfrak j}(E)
\right].
}
\tag{8.2}
\]

When the phase channel is scalar and uncoupled,

\[
\boxed{
\sigma_{\rm el}^{\Phi}(E)
=
\frac{4\pi}{k^2}
\sum_{\ell=0}^{\infty}(2\ell+1)
\sin^2\delta_{\Phi,\ell}(E).
}
\tag{8.3}
\]

Thus the exact PTM phase shift is not an analogy to an ordinary quantum phase shift. It is the eigenphase of the derived asymptotic phase transport map. The scalar formula is the special infrared form of the matrix formula once the response geometry admits a rotational asymptotic stratum and the residual holonomy block is one-dimensional.

---

## 9. PTM response, resonances, and scattering topology

Define the Wigner–Smith PTM response matrix,

\[
\boxed{
\mathbb Q_\Phi^{\mathfrak j}(E)
:=-iS_\Phi^{\mathfrak j\dagger}(E)
\frac{\partial S_\Phi^{\mathfrak j}(E)}{\partial E}.
}
\tag{9.1}
\]

Its trace is the exact phase-eigenvalue flow density,

\[
\operatorname{tr}\mathbb Q_\Phi^{\mathfrak j}(E)
=
2\frac{\partial}{\partial E}
\operatorname{tr}\boldsymbol\Delta_\Phi^{\mathfrak j}(E).
\tag{9.2}
\]

A PTM resonance is a pole of the analytic continuation of the Feshbach projected resolvent in (3.1). Its observable image is a rapid eigenphase winding and a positive time-delay eigenvalue. The associated scattering-sector phase index over an interval free of threshold branch points is

\[
\boxed{
\mathcal N_\Phi^{\mathfrak j}(E_2,E_1)
:=
\frac{1}{\pi}
\operatorname{tr}
\left[
\boldsymbol\Delta_\Phi^{\mathfrak j}(E_2)-
\boldsymbol\Delta_\Phi^{\mathfrak j}(E_1)
\right]
=
\frac{1}{2\pi}
\int_{E_1}^{E_2}
\operatorname{tr}\mathbb Q_\Phi^{\mathfrak j}(E)\,dE.
}
\tag{9.3}
\]

After a closed spectral-flow cycle, \(\mathcal N_\Phi^{\mathfrak j}\) is the integral PTM scattering index. It connects the topological observation channel directly to a measurable energy-dependent phase shift.

The complete scattering microscope is therefore

\[
\boxed{
\mathfrak M_{eH,\ell}^{\rm scat}([\Phi_H];E)
=
\left(
\Theta_{eH,\ell},
\{S_\Phi^{\mathfrak j}\}_{\mathfrak j},
\{\boldsymbol\Delta_\Phi^{\mathfrak j}\}_{\mathfrak j},
\{\mathsf f_{ba}\}_{a,b},
\{\sigma_{b\leftarrow a}\}_{a,b},
\mathbb Q_\Phi
\right).
}
\tag{9.4}
\]

It reconstructs scattering as a scale-indexed invariant phase image: topology identifies the allowed sector histories, susceptibility geometry defines flux and asymptotic distance, holonomy supplies the channel transport algebra, the S matrix records on-shell scattering, and the phase-shift matrix supplies the spectral-flow structure.

---

## 10. Falsifiability conditions for the electron–hydrogen scattering sector

| Requirement | Exact UPT computation | Failure condition |
|---|---|---|
| Scattering branch | Solve \(\mathscr F[\Phi_{eH}^{(+)};\lambda(E)]=0\) with factorized finite-flux asymptotics | No physical scattering sector exists |
| Phase geometry | Compute \(g^{(eH)}\) and its asymptotic flux stratum | Cross-section relies on an imported background geometry |
| Exchange | Compute the phase-bundle exchange character \(\varepsilon_\rho\) | Direct-minus-exchange amplitude inserted by hand |
| Channel space | Calculate hydrogen strata, thresholds, and channel injections | A preassigned atomic channel table |
| Interaction | Evaluate the Feshbach resolvent (3.2) from \(\mathbb H_{eH,\Phi}\) | An empirical scattering potential replaces the phase resolvent |
| Unitarity | Verify (4.4) on the complete open channel space | Unaccounted phase-flux loss |
| Phase shifts | Compute \(\boldsymbol\Delta_\Phi^{\mathfrak j}(E)\) from \(\mathscr F\) | Fitted phase-shift matrix |
| Cross-sections | Evaluate (7.1)–(7.6) from the derived S matrix | Cross-section not generated by the universal equation |
| Novel PTM result | Predict a resonance, threshold law, phase index, or polarization asymmetry not fitted to data | No new empirical content |

The numerical value of any electron–hydrogen cross-section is obtained only after the explicit universal phase equation, its stable hydrogen branch, its physical scattering generator, and its channel transport data have been computed. Equations (1.1)–(9.4) are the exact PTM functional definition of that calculation.

---

## References

[1] Dust LLC, *Universal Phase Theory: A Foundational Mathematical Framework for Phase Structure, Emergent Geometry, Dynamics, Topology, and Physical Reality*, supplied manuscript, August 2026.

[2] Dust LLC, *Phase Topology Microscopy: An Inverse Structural Theory for Reconstructing Stable Phase Sectors from Relational Observables*, supplied manuscript, August 2026.

[3] Dust LLC, *Nucleons, Electrons, and Atomic Phase Structure: A Derivation from the Universal Phase Equation, Phase Transport, and Bound Phase-Sector Geometry*, supplied manuscript, August 2026.

[4] J. Servais and J. Dohet-Eraly, “Low-energy \(S\)-wave scattering of \(\mathrm H+e^-\) by a Lagrange-mesh method,” *Physical Review A* **109**, 052818 (2024); arXiv:2404.04191. The work provides a conventional electron–hydrogen \(S\)-matrix and phase-shift benchmark outside the UPT derivation. [arXiv record](https://arxiv.org/abs/2404.04191)
