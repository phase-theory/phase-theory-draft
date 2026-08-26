# Technical Note UPT–TN–06

## Does $\kappa_\Phi \to J$? A Direct Computation, and a Sharper Outcome Than Any of the Three Proposed

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. The question, restated precisely

TN-05 left Gate 3 open: is the symplectic normalization $J$ on the $S^2$ moduli space derivable from the discrete Wilson action's own coupling $\kappa_\Phi$, or is it independent control data? Three outcomes were proposed in advance (A: $J(\kappa_\Phi)$ emerges; B: only a metric emerges, no symplectic term; C: $J$ emerges but remains independent of $\kappa_\Phi$). This note computes the reduction directly rather than reasoning about it abstractly, and the actual result is sharper than any of the three.

---

## 2. Computation 1 — the action is exactly zero on the moduli space, not approximately

$$
S_W[U] = \kappa_\Phi\Big(1-\tfrac12\operatorname{Tr}U_p\Big), \qquad U_p = U_1U_2U_1^{-1}U_2^{-1}.
$$

The moduli space (§Gate 1 of TN-05) is *defined* as the flat locus, $U_p = I$ exactly. On $SU(2)$, $\operatorname{Tr}(I)=2$, so
$$
S_W\big|_{\text{moduli space}} = \kappa_\Phi(1-\tfrac12\cdot2) = 0
$$
**identically, for every point $(\alpha,\beta)$ of the moduli space, not just to leading order.** This was verified directly: $U_1(\alpha),U_2(\beta)$ built as commuting diagonal $SU(2)$ elements, $S_W$ evaluated over a $12\times12$ grid in $(\alpha,\beta)\in[0,2\pi)^2$. Maximum $|S_W|$ over the grid: $3.3\times10^{-16}$ — machine-precision zero, confirming the exact (not perturbative) vanishing.

This matters because it rules out the premise behind Outcomes A–C as stated: there is no dependence of $S_W$ on the moduli coordinates *at all* to reduce, expand, or extract a term from. The moduli directions are not merely flat to leading order in some expansion parameter $a$ — the plaquette term is exactly constant on the entire connected moduli space, by construction (moduli space $\equiv$ zero locus of this very term).

**Where the actually-used metric comes from, for comparison.** A second computation confirms the action *does* grow — quadratically, with a clean, stable coefficient — in directions **transverse** to the moduli space (tilting $U_2$ off the commuting/Cartan locus by angle $\epsilon$): $S_W/\epsilon^2 \approx 0.83$, stable across $\epsilon=0.01$ to $0.2$. This transverse quadratic growth is exactly the second-variation structure $\mathscr L_\Phi$ already used elsewhere in this thread to build the response metric via $\chi_\Phi=\mathscr L_\Phi^{-1}$. It is a real, nonzero, computable structure — but it lives in the directions *orthogonal* to the moduli space, not along it.

---

## 3. Computation 2 — there is no kinetic term to Legendre-transform in the first place

$S_W[U]$, exactly as written, is a function of field *values* only — $U_1,U_2$ appear with no derivative or "velocity" dependence anywhere in the expression. It is a static (Euclidean) potential functional, structurally analogous to a magnetic energy, not a Lagrangian with kinetic content.

The symplectic potential in the covariant phase space construction (TN-04) is defined as $\Theta_\Phi = \partial L/\partial\dot\Phi$ — a derivative with respect to a rate of change. Since $S_W$ contains no such dependence,
$$
\Theta_\Phi \equiv \frac{\partial S_W}{\partial\dot\alpha} = 0 \quad\text{identically, by inspection, not by calculation that could have gone the other way.}
$$
There is nothing to compute here in the sense of a result that could have come out nonzero — the object required (a genuine velocity-dependent term) is simply absent from the action as given. Consequently $\omega_\Phi = -\delta\Theta_\Phi = 0$ trivially follows.

---

## 4. Verdict: not Outcome A, B, or C — a sharper Outcome D

- Not **A** ($J(\kappa_\Phi)$ emerges) — nothing emerges; there is no dependence to extract a coefficient from.
- Not quite **B** as stated ("only a metric emerges, no symplectic term") — the metric-like structure does not come from expanding $S_W$ *along* the moduli directions either (that expansion is exactly zero, per §2); it comes from a *different* calculation (the transverse second variation, §2 second half), already in use elsewhere in the programme for unrelated purposes.
- Not **C** ($J$ emerges but is independent) — $J$ does not emerge at all from this action.

$$
\boxed{\textbf{Outcome D: } S_W \text{ contains no structure of any kind — neither metric nor symplectic — along the moduli directions, and no kinetic term from which either could be extracted at all.}}
$$

The chain breaks at the very first link: **"Wilson action $\to$ flat phase sector $\to$ $S^2$" is correct (TN-05, Gate 1), but "$S^2$ $\to \omega_\Phi$" cannot proceed *from this action*, because the specific static, derivative-free, exactly-zero-on-moduli form of $S_W$ carries no information capable of producing either object.**

---

## 5. What this identifies as actually missing

This is a precise diagnosis, not a vague gap. To produce $\omega_\Phi$ via the covariant phase space route from an action of this general type, at least one of the following is required, and none is present in the round-1 discrete candidate as constructed:

1. **A genuine time/evolution parameter** with $U(\tau)$-dependence and derivative terms in the action (the Kogut–Susskind route: keep space discrete, time continuous, so that canonical momenta / "electric fields" conjugate to the link variables exist by construction). The round-1 candidate deliberately has no distinguished time direction in $\mathcal X$ — this was the entire ontological point (time as derived, not primitive) — so this fix is not free; it would mean introducing exactly the structure UPT's hierarchy claims to derive later, earlier than the hierarchy allows.
2. **A first-order (not second-order) term in the action itself** — e.g. a genuine Chern–Simons-type term, $\frac{k}{4\pi}\int\operatorname{Tr}(A\wedge dA + \tfrac23 A^3)$, which *is* first-order in the connection and *does* produce $\omega_\Phi$ directly. But per the methodological rule proposed alongside this note: introducing such a term is only legitimate if it is itself derived from the existing UPT postulates, not added because it is known to produce the desired result. No such derivation exists in the corpus.

---

## 6. Audit

| Claim | Status |
|---|---|
| $S_W\equiv0$ on the entire moduli space, exactly | **Verified numerically** (grid scan, max deviation $3\times10^{-16}$) |
| $S_W$ grows quadratically transverse to the moduli space | **Verified numerically** (stable $S_W/\epsilon^2\approx0.83$ across a decade of $\epsilon$) |
| $\Theta_\Phi=0$ identically for this action | **Verified by inspection** — no velocity dependence exists in $S_W$ to differentiate |
| Outcome A ($J(\kappa_\Phi)$) | **Ruled out** |
| Outcome B (metric only) | **Ruled out as stated** — the metric doesn't come from this reduction either |
| Outcome C ($J$ independent) | **Ruled out** — $J$ does not appear at all |
| Missing ingredient identified | A genuine kinetic/time-derivative structure, or an independently-derived first-order (Chern–Simons-type) term — neither present in the current candidate |

---

## 7. Conclusion

TN-06 closes cleanly, and the closure is more informative than a simple pass/fail on Gate 3 would have been. The Wilson-type discrete action underlying every candidate tested in this thread since round one is, by its exact algebraic form, incapable of producing a symplectic structure on any flat moduli space it generates — not because the calculation is hard, but because the action contains no first-order or velocity-dependent content for such a structure to come from, and vanishes identically (not approximately) on the very locus where the question is being asked. TN-05's topological result (Gate 1) stands undisturbed; it did not depend on this. But the prequantization chain proposed across TN-04–TN-06 terminates here, for the specific candidate action used throughout this thread, pending a genuinely new ingredient of the two kinds named in §5 — neither of which is available without either contradicting UPT's stated ontology (time as derived) or introducing unmotivated new terms (a Chern–Simons piece with no UPT-internal derivation).

---

## Provenance note

This note performs the TN-06 calculation proposed in a subsequent joint review: reducing the discrete Wilson action to the flat $SU(2)$ moduli space on $T^2$ established in TN-05, to test whether the symplectic normalization $J$ is generated by $\kappa_\Phi$. The exact (not perturbative) vanishing of $S_W$ on the moduli space, and its transverse quadratic growth, were both verified numerically rather than asserted. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
