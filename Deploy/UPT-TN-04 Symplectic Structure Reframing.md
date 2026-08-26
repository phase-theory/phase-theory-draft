# Technical Note UPT–TN–04

## Derivation of $\omega_\Phi$: A Sharper Reframing, and Where the Real Test Actually Lives

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Two problems with the proposed construction, before any computation

The proposed chain $\mathscr F[\Phi]=0 \to \mathscr L_\Phi \to \mathcal P_\Phi \to \omega_\Phi$, built via a Legendre transform of $L_{\mathrm{eff}}(\xi,\dot\xi)$, has two issues that need resolving before the "is $\omega_\Phi$ unique" question can even be posed correctly.

**1.1 The construction presupposes a time parameter UPT has not yet supplied.** Writing $\dot\xi^i = d\xi^i/d\tau$ requires a distinguished parameter $\tau$ along which $\Phi$ evolves. But UPT's own ontological hierarchy places time and spacetime as *derived*, downstream structures — $\mathcal X$ is explicitly not assumed to be spacetime, and the emergent metric $g^\Phi_{\mu\nu}$ (from which any notion of "time direction" would come) appears only later in the chain, built from $\chi_\Phi$, which itself is built from $\mathscr L_\Phi$. A Legendre transform along $\tau$ therefore quietly imports the one structure the whole programme claims not to assume. This is a real circularity, not a technicality.

**1.2 The fix — but it dissolves the question, rather than answering it.** The correct tool for a field theory on a general base $\mathcal X$, with no pre-existing time direction, is the **covariant phase space** construction (Peierls 1952; Crnkovic–Witten 1987; Zuckerman 1987; the same formalism underlies Wald's covariant phase space methods in gravity): for an action $\mathcal S_\Phi[\Phi]$ whose variation takes the form $\delta\mathcal S_\Phi = \mathscr F[\Phi]\,\delta\Phi + d\Theta_\Phi(\delta\Phi)$ (a boundary term, here $d$ meaning exterior derivative on $\mathcal X$), one defines the symplectic current $\omega_\Phi = \delta\Theta_\Phi$ and integrates it over any codimension-1 hypersurface $\Sigma\subset\mathcal X$:
$$
\omega_\Phi(\delta_1\Phi,\delta_2\Phi) = \int_\Sigma \big(\delta_1\Theta_\Phi(\delta_2\Phi) - \delta_2\Theta_\Phi(\delta_1\Phi)\big).
$$
This requires only that $\mathcal X$ admit a codimension-1 slicing — a far weaker requirement than "time exists" — and standard field theory gives a general theorem: **on-shell** (i.e. on the space of solutions to $\mathscr F[\Phi]=0$), $\omega_\Phi$ is independent of the choice of $\Sigma$, provided there is no flux through the boundary at infinity.

Here is the dissolving part. **This theorem holds for *any* field theory defined by an action principle** — Maxwell theory, Yang–Mills, general relativity, a free scalar field, anything. It is not a UPT-specific derivation. Section 1 of the candidate document *defines* $\mathscr F[\Phi]\equiv\delta\mathcal S_\Phi/\delta\Phi=0$ from the outset — i.e. stipulates that UPT is variational. Given that stipulation, the existence and slice-independence of $\omega_\Phi$ follows immediately from a 70-year-old general theorem, with zero UPT-specific content used in the proof. Asking "does UPT generate $\omega_\Phi$" and expecting a nontrivial yes/no is asking a question whose answer was fixed the moment $\mathscr F$ was defined as an Euler–Lagrange equation. It cannot fail, and therefore cannot be evidence for anything specific to UPT.

---

## 2. Where the real, falsifiable question is hiding

The covariant phase space theorem gives existence and slice-independence for free. What it does **not** give for free is:

$$
\boxed{\left[\frac{\omega_\Phi}{2\pi\hbar_\Phi}\right] \in H^2(\mathcal P_\Phi,\mathbb Z)}
\qquad\text{(the prequantization integrality condition).}
$$

This is genuinely model-dependent: it depends on the actual topology of $\mathcal P_\Phi$ (the physical, gauge-reduced solution space), which is fixed by the specific choice of $\mathcal X$, $M_\Phi$, and the gauge-frame group $\mathscr G_\Phi$ — exactly the candidate-specific data that has been under test throughout this thread. **This is the correct target for TN-04**, not the generic existence question.

Two further genuine (non-generic) questions survive alongside it:

- **Nondegeneracy after gauge reduction.** $\omega_\Phi$ as constructed may be degenerate on the full configuration space if there are gauge redundancies (directions in $\ker\mathscr L_\Phi$ corresponding to $\mathscr G_\Phi$-orbits); it must be checked, model by model, that quotienting by these redundancies produces a genuinely symplectic (nondegenerate) $\mathcal P_\Phi$. This is standard but not automatic, and can fail for specific $G_{AB}$.
- **Uniqueness modulo canonical transformation.** If two admissible actions $\mathcal S_\Phi^{(1)}, \mathcal S_\Phi^{(2)}$ satisfying the same UPT postulates give inequivalent symplectic classes $[\omega^{(1)}]\neq[\omega^{(2)}]$, UPT has not fixed a unique quantum kinematic structure — this restates TN-02's underdetermination lemma at the level of quantization rather than resolving it.

---

## 3. Test against the models already on the table

The only concrete candidate with an explicit, solved phase space so far is the $T^*S^1$ toy from UPT-TN-03 ($\theta$ on a circle, both the free case and the triple-well $V=\lambda(1-\cos3\theta)$ case).

**Result:** $H^2(T^*S^1;\mathbb Z) = 0$. $T^*S^1$ is homotopy-equivalent to $S^1$ (a cylinder deformation-retracts onto its core circle), and a 1-dimensional space has no 2-cycles. The prequantization condition therefore holds **vacuously** — there is only one cohomology class ($0$) for $[\omega/2\pi\hbar_\Phi]$ to land in, so satisfying it proves nothing about $R$, $\lambda$, or $\hbar_\Phi$, and cannot fail for any choice of them.

This means **neither toy model tested so far in this thread is capable of exercising the one genuinely nontrivial part of the quantization proposal.** A test with real content requires a moduli space $\mathcal P_\Phi$ with a nontrivial second cohomology — e.g. the moduli space of flat connections on a graph with independent plaquette loops (from the discrete candidate realization tested in round 1), or any configuration space containing an $S^2$-like sector. None of the constructions produced in this thread so far reach that bar.

---

## 4. Audit

| Question | Status |
|---|---|
| Does a naive Legendre transform along $\tau$ derive $\omega_\Phi$? | Only if $\tau$ is assumed — circular, given UPT's own ontology (§1.1) |
| Does the covariant phase space method avoid that circularity? | Yes — standard, well-established formalism (§1.2) |
| Does its success constitute UPT-specific evidence? | **No** — it is a generic theorem for any action-based field theory; UPT's stipulation that $\mathscr F$ is variational makes the outcome automatic |
| Is there a genuinely model-dependent, falsifiable question remaining? | **Yes** — the prequantization integrality condition, §2 |
| Has it been tested? | Attempted against the only solved candidate ($T^*S^1$); the test came back **vacuous**, not passed or failed, because $H^2=0$ for that topology |
| Is there a construction in this thread with nontrivial enough topology to test it for real? | **No** — this is the concrete next construction task, not yet done |

---

## 5. Conclusion

TN-04 does not deliver the clean positive-or-negative result the candidate document hoped for, and it should not be read as either. What it delivers instead is a correction of the question itself: the existence of $\omega_\Phi$ was never actually at stake once $\mathscr F$ was defined variationally — that part is guaranteed by general field-theory mathematics, independent of anything UPT-specific, and treating its success as evidence would have been a mistake in either direction (a "yes" proves nothing; a hypothetical "no" would only mean the action wasn't actually variational, contradicting the setup). The real, model-dependent, falsifiable content is the prequantization integrality condition on $\mathcal P_\Phi$ — and no construction produced so far in this programme has a topologically rich enough moduli space to put that condition to a real test. That is now the well-defined next task, and it is a construction problem (build a candidate with a nontrivial $H^2(\mathcal P_\Phi)$), not a further round of toy verification on the models already in hand.

---

## Provenance note

This note responds to the UPT-TN-04 proposal in a subsequent joint review, which asked whether universal phase dynamics induces a canonical symplectic structure. It reframes that question using the covariant phase space formalism (Peierls; Crnkovic–Witten; Zuckerman) to remove a circularity in the originally proposed Legendre-transform route, identifies the prequantization integrality condition as the actual locus of any UPT-specific content, and reports that the only solved candidate model in this thread ($T^*S^1$) has cohomology too trivial to test it. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
