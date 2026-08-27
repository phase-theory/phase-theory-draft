# Independent Audit of the UPT Candidate Realization and Technical Notes TN-01–TN-10

**Dust LLC — Universal Phase Theory**  
**Falsification-first technical audit**  
**27 August 2026**

---

## Executive determination

The packet contains several **genuine, narrow, and useful results**, including a reproducible compact-manifold spectral calculation, a correct model-conditional identification of the \(SU(2)\) torus character variety with the pillowcase, and clear negative results for the particular static Wilson reduction and the particular scalar/paired observables tested. Its strongest contribution is methodological: it increasingly distinguishes a derived result, a generic theorem, a stipulated ingredient, an untested possibility, and a failed construction.

It does **not**, however, establish a candidate realization of the Universal Phase Function in the strong foundational sense. The broad functional in the initial candidate is still under-specified and its displayed Euler–Lagrange equation is not the variational derivative of the stated general action unless additional fixed-background conditions are imposed. The successful subcalculations use different, independently stipulated models: a triple-well quantum mechanics on \(S^1\), a static \(SU(2)\) plaquette model on \(T^2\), and a causal-set growth model. No single, defined \(\mathscr F[\Phi;\lambda]\) has been shown to generate all three.

Two corrections are decisive for the final ledger. First, **TN-09 applies the symplectic preservation condition to the wrong matrix**: it regresses increments \(\Delta x=Mx\), but tests \(M^TJM=J\), which applies to a finite symplectic map \(x' = Mx\). The appropriate generator test is \(M^TJ+JM=0\), or, for an Euler one-step map \(F=I+M\), \(F^TJF=J\). The reported matrix fails exact preservation under the correct tests as well, but only at the reported step scale \(\simeq10^{-3}\), not by the stated order-unity margin. Without raw trajectories, covariance estimates, timestep normalization, and noise-map analysis, the claim of a decisive general failure of symplectic dynamics is not supported.

Second, **TN-07’s Myrheim–Meyer validation is only valid in \(d=1,2\)** as reported. Its \(d=3,4,5\) ordering fractions do not match the standard values for uniform sprinklings into Minkowski Alexandrov intervals. This does not refute causal-set kinematics; it means that the implementation/region used for the higher-dimensional benchmark has not been validated by the evidence shown.

> **Final status:** UPT currently has **model-conditional topology and conventional spectral constructions**, several **clean failures of specific dynamics proposals**, and no UPT-specific derivation of dynamics, Lorentzian geometry, gauge structure, quantum probability, or physical spectra. The exact missing structure is a uniquely selected, non-ad-hoc dynamical phase functional whose parameters, causal structure, and symplectic class pass the tests below.

---

## 1. Audit convention

The audit uses the following labels.

| Label | Meaning |
|---|---|
| **[Def]** | A definition or stipulated construction. |
| **[A]** | An additional assumption or input. |
| **[IM]** | Mathematics imported from an established theory. |
| **[D]** | A conclusion derived from explicitly stated premises. |
| **[NV]** | A numerical result reproduced or directly verifiable from supplied numerical specification. |
| **[CV]** | Conditional validation: correct only when stated hypotheses are supplied. |
| **[F]** | A failure of the specific construction or implication tested. |
| **[U]** | Unverified from the supplied packet; raw code, data, or a complete model is missing. |

A statement that is true of an arbitrary action, ordinary compact-manifold quantum mechanics, gauge theory, or causal-set model is classified as **generic**, even if it is fully correct. It is not UPT-specific evidence unless UPT independently derives the special hypotheses that make the statement applicable.

---

## 2. The claimed universal functional: what is defined and what is missing

The source candidate writes, schematically,

\[
\mathcal S_\Phi
=
\frac12\int_{\mathcal X}G^{AB}(\Phi)
\langle D_A\Phi,D_B\Phi\rangle_\Phi\,d\mu_\Phi
-
\int_{\mathcal X}V_\Phi(\Phi)\,d\mu_\Phi
+\mathcal S_{\mathrm{topo}},
\qquad
D_A\Phi=\partial_A\Phi+\mathcal A_A[\Phi]\Phi.
\tag{1}
\]

This is a **functional template [Def]**, not yet an explicit universal action. It requires at least the following data.

| Object in (1) | What is required before \(\delta\mathcal S_\Phi/\delta\Phi\) is defined | Status in the candidate |
|---|---|---|
| \(\mathcal X\), \(\partial_A\) | A differential base, dimension, regularity and boundary/asymptotic conditions. | [A] |
| \(E_\Phi\to\mathcal X\) | A specified bundle/target, transition data and function space. | [A] |
| \(G^{AB}(\Phi)\) | A nondegenerate contravariant tensor or other pairing of base directions. | [A] |
| \(d\mu_\Phi\) | A measure or density; if phase dependent, its variational derivative. | [A] / unspecified |
| \(\langle\cdot,\cdot\rangle_\Phi\) | A fiber bilinear/Hermitian form and its variation. | [A] / unspecified |
| \(\mathcal A_A[\Phi]\) | A concrete equivariant functional, its representation, and \(\delta\mathcal A_A/\delta\Phi\). | [A] / unspecified |
| \(V(I_1,\ldots,I_N)\) | An invariant basis, finite degree/regularity and coefficient-selection principle. | [A] / parameter-rich |
| \(\mathcal S_{\mathrm{topo}}\) | Degree, integrand, quantization/normalization and variational boundary conditions. | [A] / unspecified |
| \(\mathcal S_{\mathrm{stab}}\) | An actual defined term. It appears in the opening decomposition but is absent from the compact realization. | [U] |

### 2.1 Variational correction

The displayed candidate field equation,

\[
D_A(G^{AB}D_B\Phi)+\frac{\delta V_\Phi}{\delta\Phi}
+\frac{\delta\mathcal S_{\mathrm{topo}}}{\delta\Phi}=0,
\tag{2}
\]

is **not** the Euler–Lagrange equation of the general template (1) when \(G^{AB}\), \(\mathcal A_A\), \(d\mu_\Phi\), and \(\langle\cdot,\cdot\rangle_\Phi\) depend on \(\Phi\). Their variation produces additional terms. In schematic covariant notation,

\[
\delta\mathcal S_{\mathrm{grad}}
=
\int_{\mathcal X}
\left[
- D_A^{\dagger}\bigl(G^{AB}D_B\Phi\bigr)
+\frac12(\delta_\Phi G^{AB})\langle D_A\Phi,D_B\Phi\rangle
+\mathcal J_{\delta\mathcal A}
+\mathcal J_{\delta\langle\ ,\ \rangle}
+\mathcal J_{\delta\mu}
\right]\delta\Phi.
\tag{3}
\]

Here \(D_A^{\dagger}\) itself depends on the measure and pairing, while \(\mathcal J\) denotes the induced functional-derivative terms. Equation (2) follows only after a restrictive additional assumption: the base response tensor, measure, fiber pairing, and connection are fixed background data or have independently supplied equations and are held fixed in the \(\Phi\)-variation. That assumption is incompatible with claiming that all of these structures are derived solely from \(\Phi\).

> **Determination 1.** The global \(\mathscr F\) in the source candidate is **not yet explicit or shown well posed**. Individual restricted submodels may be well posed, but the universal functional template is not a completed phase equation. **[D], [F]** for the claim of a completed realization.

### 2.2 The stability and emergence bottleneck survives the test packet

The candidate intends to use

\[
\mathscr L_\Phi=D_\Phi\mathscr F,
\qquad
\boldsymbol\chi_\Phi=(\mathscr L_\Phi|_\perp)^{-1},
\qquad
 g_{ij}^\Phi=\langle T_i,\boldsymbol\chi_\Phi T_j\rangle.
\tag{4}
\]

These operations require an actual operator domain, boundary conditions, a specified normal complement, removal of gauge/collective zero modes, and proof that the restricted operator is Fredholm/invertible. The packet does not provide these for a unified \(\mathscr F\). Furthermore, on a stable real variational branch with positive Hessian \(H\), \(\chi=H^{-1}>0\), so

\[
v^i g_{ij}^\Phi v^j
=
\langle T(v),\chi T(v)\rangle\ge0.
\tag{5}
\]

The response form is positive semidefinite and satisfies

\[
\operatorname{rank}g^\Phi\le\operatorname{rank}T\le\dim\mathcal O.
\tag{6}
\]

It cannot be a Lorentzian spacetime metric without an additional indefinite/causal structure. None of TN-01–TN-10 removes this obstruction. The promotion of a moduli metric \(g_{ij}\) to a local spacetime metric \(g_{\mu\nu}\) also needs a derived localization map, not merely a relabeling of indices.

> **Determination 2.** The packet supplies no successful test of the central arrow \(\boldsymbol\chi_\Phi\to g_{\mu\nu}^{\mathrm{Lorentz}}\). **[F]** as a current derivation; not a proof that no future UPT realization can supply it.

---

## 3. TN-02 audit: the proper parameter-identifiability criterion

TN-02 correctly counts the coefficients of a polynomial in \(N\) scalar invariants through total degree \(D\):

\[
P(N,D)=\binom{N+D}{D},
\qquad
P_{\mathrm{phys}}(N,D)=\binom{N+D}{D}-1.
\tag{7}
\]

For \((N,D)=(3,3)\), \(P_{\mathrm{phys}}=19\). This is correct combinatorics **[D]**. The following rank refinement is required.

Let \(\Theta\) be the finite, quotient parameter space after all representational redundancies have been removed, let \(p=\dim\Theta\), and let \(\mathcal O:\Theta\to\mathbb R^M\) be the map to independently defined observables. Then the TN-02 local criteria are

\[
J^A{}_{\alpha}=\frac{\partial\mathcal O^A}{\partial\theta^\alpha},
\qquad
r=\operatorname{rank}J.
\tag{8}
\]

| Claimed result | Necessary local condition | What it does *not* prove |
|---|---|---|
| The \(p\) parameters are locally identifiable from observables. | \(r=p\le M\). | Global uniqueness or numerical conditioning. |
| The map can locally match \(M\) independent outputs. | \(r=M\le p\). | That every target is globally attained. A local regular-value/constant-rank qualification is still required. |
| The theory has parameter-free observable relations. | \(r<M\), **and** the missing-rank directions are not caused by inaccessible outputs or model pathology. | That every rank deficiency is a successful physical prediction. |

This is the appropriate two-sided version of TN-02. The output-sensitivity formulation is standard for local structural identifiability.[1]

### 3.1 Application to the triple-well quantum calculation

For TN-03’s operator,

\[
\widehat H
=-\frac{\hbar_\Phi^2}{2R^2}\frac{d^2}{d\theta^2}
+\lambda(1-\cos3\theta),
\tag{9}
\]

define \(E_*=\hbar_\Phi^2/(2R^2)\) and \(g=\lambda/E_*=2R^2\lambda/\hbar_\Phi^2\). Its complete spectrum has the form

\[
E_n=E_*\,\varepsilon_n(g).
\tag{10}
\]

Thus spectral data depends on the three listed quantities \((R,\lambda,\hbar_\Phi)\) through only two combinations \((E_*,g)\). The transformation

\[
(R,\hbar_\Phi,\lambda)
\mapsto
(cR,c\hbar_\Phi,\lambda)
\tag{11}
\]

leaves (10) invariant. Before an independent physical normalization of \(\hbar_\Phi\) or \(R\) is supplied, the raw three-parameter description has a TN-02 null direction. Setting all three numbers equal to one is a permitted **test convention [A]**, not a prediction.

### 3.2 Application to flat Wilson reduction

On the flat locus \(U_p=I\), TN-06 has the exact identity

\[
S_W\big|_{\mathcal M_{\mathrm{flat}}}
=\kappa_\Phi\left(1-\tfrac12\operatorname{Tr}I\right)=0.
\tag{12}
\]

Every observable obtained solely from the reduced value of this action has \(\partial\mathcal O/\partial\kappa_\Phi=0\). Its parameter-response rank is therefore zero along this sector. This proves that no normalization \(J(\kappa_\Phi)\) can be extracted from the on-moduli static action. **[D]**

> **Determination 3.** TN-02 remains the controlling safeguard. None of the apparently positive tests fixes the functional degrees of freedom \(G^{AB}\), \(\mathcal A_A\), \(d\mu_\Phi\), invariant basis, potential parameters, topological coefficient, causal growth law, or the scale parameters of (9). Hence the unified candidate has not passed TN-02; its observable map is not yet defined. **[D], [U]**

---

## 4. Note-by-note status

| Note | Independent finding | Correct audited status |
|---|---|---|
| **TN-01** | The distinction between an unconstrained scale parameter and a parameter-free ratio pattern is methodologically sound. However the note supplies neither the exact observable map/domain proving surjectivity nor the running-mass dataset, common renormalization scale, or calculation used for the reported factors. | **[CV]** scale nonprediction; **[U]** numerical spectrum falsification pending reproducible data. The broad candidate remains under-specified, so “\(\mathscr F\) is well posed” applies at most to a restricted triple-well submodel. |
| **TN-02** | Formula (7) is correct. Raw coefficient count is only a lower-bound alarm; rank is the relevant test. | **[D]** counting; **[CV]** rank criterion after correcting its local/global statements; **[F]** for any predictive claim based on a polynomial fit alone. |
| **TN-03** | The listed Fourier-Galerkin eigenvalues were independently reproduced through cutoff 40. The cutoff-20 to cutoff-40 ground-state difference is \(7.21\times10^{-14}\). | **[NV]** conventional self-adjoint compact spectral problem. **[F]** as derivation of quantum kinematics, \(\hbar_\Phi\), \(R\), \(\lambda\), or Born probability. |
| **TN-04** | The covariant phase-space reframing correctly recognizes generic action-based symplectic structure and the role of gauge reduction/integrality. \(H^2(T^*S^1;\mathbb Z)=0\) makes the stated prequantization test vacuous. | **[IM]**, generic; **[D]** vacuity for \(T^*S^1\); not UPT-specific evidence. A covariant construction still presupposes a variational field theory, orientation/hypersurfaces and suitable boundary conditions. |
| **TN-05** | For stipulated \(\mathcal X=T^2\), stipulated \(SU(2)\), and the flatness equation, the moduli/character variety is \((S^1\times S^1)/\mathbb Z_2\), the pillowcase. Its underlying topological space is \(S^2\), with four orbifold singular points. | **[D], [CV]** as a model-conditional topology result. The base topology and gauge group are inputs; Euler characteristic alone must not be used to erase orbifold structure. The trace pairing’s overall normalization is conventional unless independently fixed. |
| **TN-06** | Equation (12) is exact, and a static action with no derivative term does not yield a temporal canonical momentum by differentiation. | **[D], [F]** for deriving \(J\) from this reduced static Wilson action. The result does not rule out every covariant symplectic construction for a separately specified full gauge action. Transverse numerical coefficient needs raw parameterization to reproduce. |
| **TN-07** | A finite DAG’s reachability relation is a finite poset, hence a causal-set kinematic structure. The \(d=2\) ordering-fraction check is correct. For Alexandrov-interval sprinklings the expected fractions are \(1,1/2,8/35,1/10,128/3003\) for \(d=1,\ldots,5\); the printed d=3–5 values disagree. | **[NV]** only for the d=1–2 benchmark; **[U]** for the d=3–5 implementation; **[IM]** causal-set input. It is an estimator of dimension under manifoldlike conditions, not a derivation that arbitrary order uniquely determines geometry. |
| **TN-08** | Causal-order and Markov properties follow from the named growth algorithm. Fixed-\(p\) transitive percolation does not demonstrate local continuum dynamics. A single scalar observable cannot carry a nondegenerate antisymmetric two-form. | **[D]** kinematics and one-dimensional symplectic obstruction; **[F]** for this scalar route. Monotonicity strengthens the mismatch but is not the fundamental dimensional obstruction. |
| **TN-09** | Non-monotonicity and nonzero oriented area do not establish symplecticity. The reported test applies \(M^TJM=J\) to an increment regression rather than a map. Proper tests show a nonzero but step-scale defect. | **[F]** for exact symplecticity of the reported *mean linear drift* under either corrected interpretation; **[U]** for the stronger conclusion that this stochastic process cannot have any symplectic description. |
| **TN-10** | The consolidation correctly advises against open-ended candidate hunting. It inherits the TN-07 validation gap and TN-09 test error, however. | **[CV]** after the present corrections. It must not state that an emergent UPT geometry or a decisive three-way dynamical failure has been verified. |

---

## 5. Independent numerical checks

The numerical findings listed below were independently reconstructed from the formulas printed in the packet. They establish the arithmetic/numerics only for the declared models.

| Check | Result | Audit implication |
|---|---|---|
| Triple-well Fourier operator, cutoff \(40\) | \(E_0=0.89118615974076\), followed by \(1.31703451404149\) (twice), \(3.12572940863168\) (twice), \(5.48149732673584\), \(5.59027311206580\). | TN-03 values are reproducible **[NV]**. |
| Triple-well convergence | \(|E_0^{(20)}-E_0^{(40)}|=7.205\times10^{-14}\). | Strong convergence for the specified spectral discretization; no physical parameter prediction. |
| TN-09 printed increment matrix | \(\operatorname{tr}M=1.00561\times10^{-3}\); \(\det M=-1.7030613\times10^{-7}\). | \(M^TJM=J\) is not the appropriate test for an increment matrix. |
| Correct TN-09 generator test | \(\max|M^TJ+JM|=1.00561\times10^{-3}\). | The quoted mean drift is not exactly Hamiltonian/symplectic as a continuous generator. Statistical significance is unknown. |
| Correct TN-09 one-step Euler test | For \(F=I+M\), \(\det F=1.0010054397\) and \(\max|F^TJF-J|=1.00544\times10^{-3}\). | Exact discrete symplecticity fails for that approximate map, but not at the report’s stated order-unity scale. |
| Myrheim–Meyer baseline | Independent 40-trial, \(N=500\), fixed-seed Alexandrov sprinklings reproduce \((1,0.49683,0.22462,0.09920,0.04319)\) for \(d=1\)–5. | Confirms the standard fractions and identifies the unvalidated TN-07 d=3–5 benchmark. |

The corresponding scripts and JSON data accompany this audit.

---

## 6. Corrected claim ledger

| Claim | Classification | Basis and limit |
|---|---|---|
| A specified triple-well operator on \(S^1\) has a real discrete normalizable spectrum. | **Established but generic [NV], [IM]** | Independently reproduced. It is ordinary spectral theory once \(S^1\), metric, Hilbert space, \(\hbar_\Phi\), and potential are input. |
| A flat \(SU(2)\) torus sector has pillowcase underlying topology. | **Established conditionally [D], [IM]** | Requires the stipulated torus base, compact group, commuting-pair constraint, and gauge quotient. It is not topology derived from phase primacy alone. |
| The static one-plaquette Wilson action generates a nonzero on-moduli symplectic coefficient. | **Failed [D], [F]** | The restricted action is identically zero and contains no velocity term. |
| The UPT causal DAG can be read as causal-set kinematics. | **Established but generic [Def], [IM]** | True when reachability gives a locally finite poset. It does not derive manifoldlike geometry or dynamics. |
| TN-07 validates higher-dimensional Myrheim–Meyer recovery. | **Unverified [U]** | Only d=1–2 match the stated baseline; d=3–5 require code/region audit. |
| The tested paired-observable growth dynamics is decisively non-symplectic by \(M^TJM\ne J\). | **Test invalid as stated; corrected narrow failure [F]** | The wrong matrix was tested. Correct tests reject exact preservation for the mean regression but do not establish the claimed sweeping failure. |
| The broad action template defines a unique well-posed UPT universal equation. | **Failed / unestablished [F]** | Undefined functional data and missing variational terms remain. |
| Stable response geometry yields Lorentzian spacetime. | **Failed / unestablished [D], [F]** | Positive stable response form is positive semidefinite; the localization and signature problem persists. |
| The test packet derives a UPT-specific quantum structure. | **Unestablished [F]** | The spectral calculation imports standard quantization; symplectic existence is generic for variational theories and physical probability remains open. |
| Fermion hierarchy/spectrum is predicted by the generation-locking candidate. | **Failed conditionally [CV], [F]** | The reported equal-spacing prediction is a legitimate test target, but its numerical falsification needs reproducible PDG-scale data; free-scale issue remains decisive. |

---

## 7. Research questions that are now well posed

The present evidence makes four questions mandatory before another physical-spectrum or dynamics candidate is pursued.

| Required question | Pass condition | Fail condition |
|---|---|---|
| **Functional closure** | Give one full \(\mathcal S_\Phi\), exact bundle/base/function spaces, all measures/pairings, all variations, and a proof of covariance/well-posedness. | A template retains undefined \(G\), \(\mathcal A\), \(V\), measure, or topological terms. |
| **Non-ad-hoc selection** | Prove that explicitly stated postulates select a unique action or a finite quotient family before comparison with physical outputs. | A potential, group, topology, kinetic term, or growth law is chosen because it produces a desired downstream feature. |
| **Causal-response theorem** | Derive a nondegenerate Lorentzian bilinear form and causal/localization map from phase data, with rank and signature demonstrated. | A positive moduli metric is relabeled as spacetime, or a time direction is inserted before the derivation. |
| **TN-02 prediction test** | Define \(\Theta/\!\sim\), \(\mathcal O\), \(J=D\mathcal O\), ranks, and data not used in fitting. | Parameter counts are substituted for ranks, or a high-rank fit is called a prediction. |

No further search over observable pairs, growth rules, or topological models should be treated as foundational evidence until the second condition supplies an independently motivated selection principle. Otherwise the search itself becomes a hidden model parameter and reproduces the TN-02 failure mode at the level of candidate choice.

---

## References

[1] A. Iliadis, “[Structural identifiability and sensitivity](https://doi.org/10.1007/s10928-019-09624-9),” *Journal of Pharmacokinetics and Pharmacodynamics* **46**, 127–135 (2019).

[2] D. P. Rideout and R. D. Sorkin, “[Evidence for a continuum limit in causal set dynamics](https://doi.org/10.1103/PhysRevD.63.104011),” *Physical Review D* **63**, 104011 (2001).

[3] A. Vanderbauwhede, “[Lyapunov–Schmidt Method for Dynamical Systems](https://doi.org/10.1007/978-1-4614-1806-1_56),” in *Mathematics of Complexity and Dynamical Systems* (Springer, 2012).

[4] User-provided **Candidate Realization of the Universal Phase Equation**, *Pasted_content_40.txt*.

[5] User-provided **UPT Technical Notes TN-01–TN-10**, *Pasted_content_41.txt* through *Pasted_content_50.txt*.

---

## Reproducibility files

The following accompanying files reproduce the independent checks reported in Section 5:

- `verify_upt_test_packet.py` and `upt_test_packet_independent_checks.json`;
- `verify_myrheim_meyer.py` and `myrheim_meyer_independent_check.json`;
- `upt_test_packet_audit_findings.md`.
