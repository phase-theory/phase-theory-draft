# Technical Note UPT–TN–13

## Does Minimal UPT Satisfy Postulate XI? A Conditional Yes, With the Condition Named Precisely

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Scope, per the tightened mandate

No fermions, generations, Yukawa couplings, or Standard Model targets appear anywhere in this note. The object under test is the smallest system that retains already-demonstrated UPT structure: $\Phi$, $\mathscr F[\Phi]=0$, $\mathcal M_\Phi$, and the $SU(2)$ holonomy sector from TN-05/06 — i.e. the round-1 discrete candidate's Wilson-type action, with no matter fields added. The question, per the three-way distinction requested:

- **Coupling rigidity** — is $\kappa_\Phi$ a physical modulus, or removable as a unit choice?
- **Solution rigidity** — does $\mathcal M_\Phi$ have continuous moduli? (Explicitly *not* the Postulate-XI question — flagged so it isn't miscounted.)
- **Theory rigidity** — is there a continuous family of physically inequivalent theories? (This is the actual test.)

---

## 2. Solution rigidity — present, and irrelevant to the verdict

$\mathcal M_\Phi \cong S^2$ (TN-05) is a continuous moduli space of flat connections — different points correspond to different classical vacua of the *same* theory (fixed $\kappa_\Phi$), related by nothing more exotic than which flat configuration is realized, analogous to different classical solutions of a fixed Lagrangian. Per the requested distinction, this does **not** count against condition 4. Recording it separately here specifically to prevent it from being miscounted, as the framing document required.

---

## 3. Coupling rigidity — the key structural identification

The TN-06 discrete action, $S_W = \kappa_\Phi(1-\tfrac12\operatorname{Tr}U_p)$, was checked directly against the standard Wilson lattice-gauge convention $S_W=\beta\sum_p(1-\tfrac1N\operatorname{Re}\operatorname{Tr}U_p)$: for $SU(2)$, $1/N=1/2$ — **an exact match, not an analogy.** $\kappa_\Phi$, as literally used throughout TN-05/06, *is* the standard lattice coupling $\beta=2N/g_0^2$, not a UPT-invented quantity dressed in lattice language.

This licenses importing an established result directly, rather than merely by analogy: pure (matter-free) $SU(N)$ lattice gauge theory with the Wilson action is known — both perturbatively and via decades of numerical lattice QCD — to exhibit **asymptotic scaling**:
$$
a\,\Lambda_{\rm lattice} = (b_0 g_0^2)^{-b_1/(2b_0^2)}\exp\!\left(-\frac{1}{2b_0 g_0^2}\right), \qquad b_0=\frac{11N}{48\pi^2},\ \ b_1=\frac{34N^2}{3(16\pi^2)^2}.
$$
This is the *lattice-regularized* version of exactly the continuum dimensional-transmutation mechanism established in TN-12 for pure Yang–Mills: as the continuum limit is taken, every bare $\kappa_\Phi$ maps to the *same* physical theory, differing only by an overall scale $\Lambda_{\rm lattice}$ — a unit choice, not a physical modulus. **$\kappa_\Phi$ is therefore not a coupling-rigidity failure**, exactly on the same grounds as continuum pure Yang–Mills.

---

## 4. Theory rigidity — the actual verdict, and its condition

Combining §2–3: if this identification transfers cleanly, minimal UPT (the pure $SU(2)$ holonomy sector) inherits $\dim\mathfrak T=0$ directly from the established Yang–Mills result, and **Postulate XI's condition 4 survives its first UPT-specific test.**

**But the transfer is not automatic, and stating the condition precisely is the actual content of this note.** The asymptotic-scaling result is proven and numerically verified for *regular, translation-invariant lattices* approximating a fixed-dimensional continuum (overwhelmingly, hypercubic lattices in $d=4$). UPT's actual $\mathcal X$ is an **update DAG** — a general, locally finite partial order, not assumed regular or translation-invariant (TN-07's causal-set identification is explicit about this). Whether the same beta-function structure, and hence the same trading of $\kappa_\Phi$ for a single scale, holds on an irregular causal-set-like graph is **not established by anything cited in this note** — it would need either (a) a demonstration that the relevant DAG resembles a regular lattice closely enough in the continuum limit (a real, checkable question, connecting to TN-07's dimension-estimation machinery), or (b) a separate RG analysis for graph-valued gauge theories, which does not currently exist in this thread or, to this note's knowledge, in the general literature.

$$
\boxed{\textbf{Minimal UPT satisfies theory rigidity } \emph{if and only if} \textbf{ its update-DAG substrate is regular enough, in the relevant continuum limit, for the standard lattice asymptotic-scaling mechanism to apply. This has not been shown.}}
$$

This is a precise, falsifiable condition — not a restatement of "more work is needed." It says exactly what would have to be true (DAG regularity in an appropriate limit) for the positive result to transfer, and exactly where to look to check it (TN-07's dimension-estimator machinery, applied to whatever specific $\mathcal X$ a future construction proposes, checking not just that a dimension emerges but that it emerges *uniformly enough* for a translation-invariant continuum limit).

---

## 5. Audit

| Test | Result |
|---|---|
| Solution rigidity ($\mathcal M_\Phi$ has moduli) | **True**, but explicitly not counted against condition 4, per the requested distinction |
| $\kappa_\Phi$ is literally the standard lattice coupling $\beta$ | **Verified directly** (convention match, not analogy) |
| Coupling rigidity via dimensional transmutation | **Established** *for regular lattices* — directly inherited from TN-12's Yang–Mills result |
| Theory rigidity for minimal UPT on a general DAG | **Conditional — not established**; the condition is DAG regularity in the continuum limit, precisely named |
| Solution rigidity conflated with theory rigidity | **Avoided** — the two are kept separate throughout, per the framing document's requirement |

---

## 6. What this does and doesn't license next

Per the requested stopping rule: this is not a failure requiring repair, and not an unconditional success either. It is a genuine conditional result, and the condition is the deliverable. **TN-14, if pursued, should not attempt to add matter, generations, or phenomenology** (per §5's ladder) — the immediate next question, prior to any of that, is whether the specific graph structures already used in this thread (TN-05's torus, TN-07's sprinkled causal sets) are regular enough for asymptotic scaling to hold, using machinery already built (the Myrheim–Meyer estimator, applied not just to recover a dimension but to check its uniformity/stability across the graph — a stronger requirement than TN-07 tested for).

The tension flagged in TN-12 remains fully intact and is not resolved by this note: *if* minimal UPT achieves theory rigidity on some regular-enough substrate, the harder question — whether that rigidity survives the addition of matter sectors needed for a realistic spectrum — is exactly as open as TN-12 left it, and this note does not narrow that gap, only the one immediately prior to it.

---

## Provenance note

This note tests theory rigidity for the minimal $SU(2)$-holonomy UPT sector, per the tightened TN-13 mandate in a subsequent joint review (no matter, no phenomenology). The exact match between TN-06's action convention and the standard Wilson lattice coupling was verified directly (symbolic check), licensing direct rather than analogical import of the established lattice asymptotic-scaling result. The regularity condition on $\mathcal X$ required for this transfer is identified precisely as the open gap, not asserted to hold. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
