# Technical Note UPT–TN–12

## Is Postulate XI's Rigidity Condition Even Satisfiable? Yes — But Only by a Fragile, Special Class of Theories

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. The question, made precise

TN-11 flagged that condition 4 of Postulate XI (control-data closure) is stricter than what Maxwell, Yang–Mills, or linearized GR satisfy — but stopped short of asking whether *any* nontrivial local field theory could satisfy it. This note asks that question directly, before any attempt to construct a UPT realization of it (per the discipline TN-10 established).

Three distinct meanings of "rigid," as distinguished:
- **A.** No continuous family of physically inequivalent Lagrangians at all.
- **B.** Dimensionful constants ($c,\hbar,G$) are permitted (they only fix units), but no continuous deformation changes observable *dimensionless* predictions.
- **C.** The dynamics is fixed, but the solution space (moduli of classical configurations) may still have continuous parameters.

Postulate XI's condition 4, read against its own statement ("any remaining parameter must be... an observable topological/spectral invariant... or removed as a true redundancy"), is best read as **interpretation B**. This note adopts that reading and tests it.

Define $\mathfrak T = \{\text{admissible actions}\}/\{\text{field redefinitions + gauge redundancies}\}$. Interpretation B requires $\dim\mathfrak T = 0$ in the sector of dimensionless couplings.

---

## 2. The RG framing, and a gap in the proposed method

The proposing document suggests classifying directions in $\mathfrak T$ via the linearized RG matrix $M^i{}_j = \partial\beta^i/\partial\lambda^j$ at a fixed point, with relevant/marginal/irrelevant directions read off from its eigenvalues. **This method, on its own, is insufficient** — and this is a real gap worth stating precisely rather than glossing over, because the cleanest counterexample below depends on it.

At the free (Gaussian) fixed point of Yang–Mills theory, the coupling $g=0$ is *classically marginal* ($\beta(g)\sim -b_0g^3+\dots$ near $g=0$, so $d\beta/dg|_{g=0}=0$ exactly — a linear-order eigenvalue of precisely zero). Reading only the linearized matrix $M$, one would classify $g$ as a marginal direction — an apparent modulus, i.e. evidence *against* rigidity. But the correct, established, nonperturbative fact (asymptotic freedom, dimensional transmutation) is that this "marginal" direction is not actually a modulus at all: the one-loop *cubic* term in $\beta(g)$ ties every value of the bare coupling to a single physical scale $\Lambda_{\rm QCD}$, so there is only one physical theory (for a fixed gauge group), not a one-parameter family. **The linearized-RG test proposed in the framing document would have missed this** — it requires going beyond linear order to nonperturbative RG behavior. This is flagged as a correction to the proposed method, not merely a caveat.

---

## 3. Stress test, dimensional analysis verified directly

Classical scaling dimensions (mass dimension, $\hbar=c=1$) were computed directly rather than recalled from memory, to avoid an arithmetic error entering the argument: scalar field $[\phi]=(d-2)/2$, fermion $[\psi]=(d-1)/2$, gauge field $[A]=(d-2)/2$, giving coupling dimensions $[\lambda_{\phi^4}]=0$ in $d=4$ (marginal — matches the standard result), $[e]_{\rm QED}=0$ in $d=4$ (marginal), $[G]=-2$ in $d=4$ (dimensionful, sets the Planck length), $[\Lambda]=2$ in $d=4$, and the physically meaningful combination $[\Lambda G]=0$ — a genuine dimensionless parameter when $\Lambda\neq0$.

| Theory | Dimensionless physical coupling(s) | $\dim\mathfrak T$ (sector) | Status |
|---|---|---|---|
| Free Maxwell (no charged matter) | none | 0 | Rigid, but trivially — it's a free theory |
| QED (Maxwell + charged fermion) | $\alpha$ (fine structure) | $\geq1$ | **Not rigid** |
| **Pure Yang–Mills (no matter)** | none — $g$ removed by asymptotic freedom + dimensional transmutation | **0** | **Rigid**, and nontrivially so (interacting, confining, nonperturbative) |
| Yang–Mills + matter (QCD) | quark mass ratios, $\theta_{\rm QCD}$ | $\geq1$ | **Not rigid** |
| **Pure GR, $\Lambda=0$, no matter** | none (only $G$, purely dimensionful) | **0** | Rigid *if* the asymptotic-safety conjecture holds at the relevant fixed point — **less settled than the YM case**, flagged as conjectural |
| GR $+\ \Lambda$ | $\Lambda G$ | $\geq1$ | **Not rigid** |
| Free massless scalar | none (Gaussian fixed point) | 0 | Rigid, but trivially |
| Interacting $\phi^4$, $d=4$ | $\lambda$ | Marginally irrelevant (Landau pole / "triviality") | Effectively rigid only in the strict continuum limit — a subtle, separate result (lattice triviality), not asserted with the same confidence as the YM case |

---

## 4. Answer to TN-12's central question

$$
\boxed{\textbf{Rigidity in interpretation B is not impossible. Pure Yang–Mills theory is a genuine, well-established counterexample to "every nontrivial interacting local theory has a continuous physical deformation."}}
$$

This is not a marginal or contested fact — asymptotic freedom and dimensional transmutation in pure (matter-free) Yang–Mills are among the most rigorously established results in quantum field theory. So the strongest reading of Postulate XI's condition 4 **survives its existence test**: it describes a mathematically inhabited class of theories, not an empty one.

**But the inhabited class is fragile, and this is the sharper, more useful part of the answer.** Every example of a rigid theory found above achieves rigidity by having *minimal field content* — no charged matter (Maxwell), no matter at all (Yang–Mills, GR), or by being exactly free (scalar). The moment matter, a cosmological constant, or any additional coupled sector is introduced, rigidity is lost — not gradually, but immediately, by the appearance of a new dimensionless ratio (a mass ratio, $\alpha$, $\Lambda G$). No example was found (or is claimed to exist) of a rigid theory with rich enough structure to support something resembling the observed particle spectrum.

---

## 5. Consequence for UPT specifically

This reframes the open question for Postulate XI more sharply than TN-11 could, and does so independent of UPT (per the requested discipline):

$$
\boxed{\textbf{Does UPT's phase sector need to remain "pure" (minimal, matter-free, single-sector) to have any chance of satisfying condition 4 — and if so, is that compatible with ever supporting the generation/coupling structure TN-01 was originally trying to derive?}}
$$

This is now a genuine tension, not a vague one. Every attempt earlier in this thread to give UPT enough structure to address the fermion sector (TN-01's Yukawa candidate, TN-05–06's $SU(2)$ holonomy sector) *added* structure — precisely the kind of addition that, per §3–4 above, destroys rigidity in every known example. If Postulate XI is the correct requirement for a fundamental dynamical completion, satisfying it and satisfying the original motivation for the programme (deriving a realistic particle spectrum) may be in direct tension, not sequential goals.

---

## 6. Audit

| Claim | Status |
|---|---|
| Interpretation B is the correct reading of condition 4 | Adopted, not independently proven — a reading choice, flagged as such |
| Linearized RG eigenvalues alone can detect rigidity | **False** — corrected; nonperturbative behavior (asymptotic freedom) is required, shown via the $g=0$ Yang–Mills example |
| Pure Yang–Mills has $\dim\mathfrak T=0$ | **Established**, standard QFT result (asymptotic freedom + dimensional transmutation), not new to this note |
| Pure GR ($\Lambda=0$) has $\dim\mathfrak T=0$ | **Conjectural** — contingent on asymptotic safety, explicitly flagged as less certain than the YM case |
| Rigidity is achievable by *some* nontrivial theory | **Yes** — existence test passed |
| Rigidity is achievable by a theory rich enough for a realistic spectrum | **No known example**; identified as the open tension for UPT specifically |

---

## 7. Recommendation

Per the proposed staged discipline (TN-10: what does UPT establish; TN-11: what postulate would be required; TN-12: is it satisfiable; TN-13: only then, can UPT realize it), this note answers TN-12 affirmatively but narrowly: **rigidity is mathematically inhabited, not empty, but every known inhabitant is minimal in a way that appears to conflict with the programme's original goals.** TN-13, if attempted, should not search for a UPT realization of Postulate XI in the abstract. It should first ask whether a "pure," minimal UPT phase sector (no fermion/generation structure at all) can satisfy condition 4 — treating that as the actual existence question — before asking whether such a rigid, minimal sector could subsequently be extended to anything resembling the observed particle content, given that every example in §3 shows extension destroys rigidity.

---

## Provenance note

This note tests the satisfiability of Postulate XI's condition 4, per the request in a subsequent joint review, independent of any UPT-specific construction. The dimensional-analysis results in §3 were computed directly (symbolic scaling-dimension derivation) rather than recalled, to avoid arithmetic error. The correction to the proposed linearized-RG methodology (§2) — that it cannot by itself detect the Yang–Mills rigidity mechanism — is original to this audit. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
