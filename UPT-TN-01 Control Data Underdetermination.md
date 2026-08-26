# Technical Note UPT–TN–01

## On the Underdetermination of Control Data in the Generation-Locking Candidate, and a Proposed Uniqueness Postulate

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## Scope

This note is written entirely within the Universal Phase Theory (UPT) formalism — the datum $\mathfrak U=(E_\Phi,\mathscr G_\Phi,\mathcal C_\Phi,\mathscr F,\Lambda)$, the operator hierarchy $\mathscr L_\Phi, \Delta_\Phi, \boldsymbol\chi_\Phi$, and the admissibility equation $\mathscr F[\Phi;\lambda]=0$. It does not draw on the earlier Phase Theory axiom system (Axioms 1–6, PTN-01), which UPT supersedes rather than extends. Where the earlier axiom-based programme is philosophically motivated, UPT is treated here as what it claims to be: a mathematical structure whose consequences are computed, not narrated.

This note formalizes a specific negative result obtained by direct computation on the generation-locking candidate ("*Three Generations and the Yukawa Hierarchy from Universal Phase Geometry*"), diagnoses its source precisely within UPT's own vocabulary, and proposes a candidate postulate that would resolve it — without claiming that postulate is yet established.

---

## 1. Restatement of the candidate construction

The generation-locking candidate instantiates the UPT control datum with:

- a trilinear phase-locking invariant $I = \eta_L\eta_R\eta_H + \text{c.c.}$, reduced to the composite map $P(\zeta)=\zeta^3$;
- three stable phase-locking branches $\zeta_k = e^{2\pi i k/3}$, identified with three generation sheets $\mathcal G_1,\mathcal G_2,\mathcal G_3$;
- a phase-distance law between the Higgs-aligned sheet and generation sheet $n$,
$$
S_n = 2\pi\hbar_\Phi\,|3-n|,
$$
- and a Yukawa eigenvalue law
$$
Y_{f,n} = Y_\Phi\,\Delta_{f,n}^{1/2}\exp(-S_{f,n}/\hbar_\Phi).
$$

Here $\hbar_\Phi$ (equivalently, in the continuum realization tested below, the potential coupling $\lambda$ of $V(\theta)=\lambda(1-\cos 3\theta)$) is **control data**: $\lambda \in \Lambda$, per the UPT datum's own definition. It is not part of $\mathscr F$, $\mathscr L_\Phi$, or any derived operator. It is external input, exactly as $\lambda$ is external input in every other UPT construction (cf. the scale parameter $\ell$ in Postulate X, Scale Dependence).

---

## 2. Direct computation

Using the natural continuum completion of $P(\zeta)=\zeta^3$ — a phase coordinate $\theta$ on a circle with potential $V(\theta,\lambda)=\lambda(1-\cos3\theta)$, whose minima at $\theta=0,\tfrac{2\pi}{3},\tfrac{4\pi}{3}$ reproduce the three locked branches exactly — the domain-wall (instanton) action between generation sheets was computed directly:
$$
S(\theta_0\to\theta_1;\lambda) = \int_{\theta_0}^{\theta_1}\sqrt{2\big(V(\theta,\lambda)-V_{\min}\big)}\;d\theta.
$$

Two results follow from this computation, not from assumption:

**(a) Scale underdetermination.** For any target ratio $\rho>1$ there exists $\lambda\in\Lambda$ such that the leading-order candidate reproduces $y_t/y_e=\rho$ exactly. Explicit solutions were exhibited for $\rho \in \{10,\ 10^2,\ 3.4\times10^5,\ 10^{10},\ 10^{20}\}$, each requiring only a different value of $\lambda$. No target ratio is excluded by the construction.

**(b) Leading-order pattern falsification.** The candidate's own equal-spacing law, $S_n\propto|3-n|$, predicts a **parameter-free** consequence: the ratio between adjacent generations should be constant across the whole spectrum, independent of $\lambda$ or $\hbar_\Phi$. Tested against PDG fermion masses, this consequence fails in all three fermion families (up-type quarks, down-type quarks, charged leptons), with the two adjacent-generation ratios differing by factors of 4–12$\times$ per family, in inconsistent directions across families.

**(c) Degeneracy under relaxation.** Dropping the falsified equal-spacing law and allowing each family its own two phase distances $(S_1,S_2)$ produces an exact, residual-free fit to every family's mass ratios — because the relaxed construction has exactly as many free parameters (two per family) as data points (two ratios per family) to fit.

---

## 3. Formal diagnosis

**Proposition (Control-Data Underdetermination).** *Let $\mathfrak U=(E_\Phi,\mathscr G_\Phi,\mathcal C_\Phi,\mathscr F,\Lambda)$ be a UPT datum whose admissibility map $\mathscr F$ is well-posed and whose solution branches are fully classified (as in the generation-locking candidate). If the map*
$$
\lambda \;\longmapsto\; \big(\text{observable ratios computed from } \Phi(\lambda)\big)
$$
*is surjective onto the full physically meaningful range of those ratios, then no observation of those ratios constrains $\lambda$, and the admissibility map $\mathscr F$ — however well-posed — carries no predictive content for them.*

This is not a statement that $\mathscr F$ is wrong, incomplete, or unsolved. Sections 1–2 confirm the opposite: $\mathscr F$ is explicit, its branches are explicit, and its leading-order consequence is explicit enough to be tested and falsified (finding (b)). The failure is located precisely in $\Lambda$: the control-data space is **unconstrained by any UPT postulate**, so results (a) and (c) are not surprising — they are the generic behavior of any admissibility map once its control data is left free.

This distinguishes the present finding sharply from an ordinary "not yet computed" gap. It identifies *which* object in the UPT datum is underdetermined ($\Lambda$, not $\mathscr F$), which is the correct diagnostic register for a mathematical framework: the equation is not the problem; the space of admissible inputs to it is.

---

## 4. Proposed resolution: a Control-Data Uniqueness postulate

UPT's postulates so far (as catalogued in *Universal Phase Theory*) fix the structure of $E_\Phi$, $\mathscr G_\Phi$, $\mathscr F$, and the operator hierarchy, but say nothing about how $\lambda$ is selected when multiple sectors of $\Phi$ coexist. The proposal here is a single additional requirement:

> **Postulate (Control-Data Uniqueness).** *When the phase bundle $E_\Phi$ decomposes, at a given scale, into coupled sub-sectors $\Phi = \Phi_1 \star \Phi_2 \star \cdots \star \Phi_k$ (e.g. a generation-locking sector coupled to the gauge/geometric sector from which $\hbar_\Phi$, $\ell_\Phi$, and $\alpha_\Phi$ are separately derivable), the physical control datum $\lambda_{\mathrm{phys}}\in\Lambda$ is not free per sub-sector. It is the value at which the total action*
> $$
> S_\Phi^{\mathrm{tot}}[\Phi_1\star\cdots\star\Phi_k;\lambda]
> $$
> *is jointly stationary across all sub-sectors simultaneously — not the value at which any single sub-sector's reduced action is stationary in isolation.*

Under this postulate, $\lambda$ used in the generation-locking sector cannot be chosen independently of the $\lambda$-dependence of, for instance, the emergent phase-susceptibility scale $\ell_\Phi$ (Part 6 of the earlier candidate-$\mathscr F$ paper) or the derived fine-structure parameter $\alpha_\Phi = e^2/(4\pi\hbar_\Phi c_\Phi)$ (the atomic-structure paper, §5.6). A single joint stationarity condition, if it has an isolated solution, would remove exactly the freedom exploited in Section 2(a) and 2(c) above.

**What this postulate does not do.** It does not, by itself, produce a number. Whether $S_\Phi^{\mathrm{tot}}$ has an isolated stationary point, a continuous family of them, or none, is an open computation requiring an explicit joint action over an explicit multi-sector $\mathscr F$ — which has not been constructed. This postulate converts an unacknowledged free parameter into an explicit, falsifiable mathematical question. It does not answer that question.

---

## 5. Falsifiability of the proposed postulate

- **Criterion 1 — Existence.** An explicit multi-sector $\mathscr F$ and total action $S_\Phi^{\mathrm{tot}}$ must be constructed in which the generation-locking sector and at least one independently-anchored sector (e.g. the gauge/geometric sector) are both present.
- **Criterion 2 — Isolation.** The joint stationarity condition must select an isolated $\lambda_{\mathrm{phys}}$ (or a discrete, finite set), not a continuous family — a continuous family would leave the underdetermination intact in reduced form.
- **Criterion 3 — Independence.** The resulting $\lambda_{\mathrm{phys}}$ must be computable without reference to the fermion mass ratios it is subsequently used to predict. If $\lambda_{\mathrm{phys}}$ can only be identified by checking which value reproduces $y_t/y_e$, Criterion 3 is failed and the postulate has not resolved anything — it has only relocated the free parameter.
- **Criterion 4 — Pattern correction.** Independently of the scale question, any successor construction must also replace the falsified equal-spacing law $S_n \propto |3-n|$ (finding (b)) with a phase-distance function whose family-dependence is *derived* from the joint action, not fit per family (finding (c)) — otherwise Criterion 1's construction inherits the same degeneracy at one level down.

---

## 6. Status

| Question | Status after this note |
|---|---|
| Is $\mathscr F$ for the generation-locking sector well-posed? | Yes — confirmed by direct computation |
| Does it predict $N_{\mathrm{gen}}=3$? | Yes, given the trilinear-invariant assumption (assumption itself not derived) |
| Does it predict the Yukawa hierarchy scale? | **No** — Section 2(a), unconstrained $\lambda$ |
| Does its leading-order pattern match the fermion spectrum? | **No** — Section 2(b), falsified against PDG data |
| Is the degeneracy fixable by relaxing the pattern? | **No** — Section 2(c), becomes an exact fit with no residual, hence no test |
| Is there a UPT-native diagnosis of the failure? | Yes — Section 3, located in $\Lambda$, not $\mathscr F$ |
| Is there a candidate postulate to resolve it? | Proposed, Section 4 — **unproven**, and Criterion 3 above is the test it must pass to avoid merely relocating the same free parameter |

---

## 7. Conclusion

The generation-locking candidate is mathematically well-formed and its leading-order consequence is sharp enough to be computed and tested — which is more than can be said of an unconstructed schema. Tested, it fails on two independent fronts: its scale is unconstrained (any hierarchy is reproducible), and its shape is wrong (the one parameter-free prediction it makes is contradicted by data). Both failures are located in the same place: the control-data space $\Lambda$ has no UPT postulate governing it when multiple sectors of $\Phi$ must share a single physical scale.

The Control-Data Uniqueness postulate proposed here names the missing ingredient precisely, in UPT's own mathematical language, without pretending to have supplied it. Its own Criterion 3 is the safeguard against the note becoming another version of the problem it diagnoses: a resolution is only real if $\lambda_{\mathrm{phys}}$ can be computed from the joint action *before* anyone checks it against $y_t/y_e$, not after.

---

## Provenance note

This note responds to and formalizes findings obtained by direct numerical computation on the candidate construction of *Three Generations and the Yukawa Hierarchy from Universal Phase Geometry* (Dust LLC, August 2026), diagnosed strictly within the UPT datum $\mathfrak U=(E_\Phi,\mathscr G_\Phi,\mathcal C_\Phi,\mathscr F,\Lambda)$. It supersedes any analogous framing in terms of the earlier Phase Theory axiom system, per current programme direction.
