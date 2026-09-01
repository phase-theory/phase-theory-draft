# Technical Note UPT–TN–18

## The Selection Problem: A Full Parameter Audit and a Search for Existing Selectors

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Two separate tasks, kept apart

Per the framing, this note does two things and does not conflate them: (A) audit *every* dimensionless parameter introduced across TN-01–17 against a five-category classification; (B) check whether any of the four logically possible selector types already follows from existing UPT postulates. Neither task proposes a new selector — per the frozen rule adopted below, that would be out of scope for an audit.

---

## 2. Full parameter audit

| Parameter | Introduced in | Category | Basis |
|---|---|---|---|
| $\lambda$ (generation-locking potential coupling) | Yukawa candidate / TN-01 | **5 — Free/unexplained** | Shown to fit any target hierarchy from $10\times$ to $10^{20}\times$ |
| $A,B$ (relative sector weightings) | TN-01 addendum | **5 — Free/unexplained** | Tested across two orders of magnitude; mechanism failed regardless (no interior minimum for any ratio) |
| $a_n,b_{mn},c_{mnp},\ldots$ (polynomial potential coefficients) | Continuum candidate / TN-02 | **5 — Free/unexplained** | $P_{\rm phys}(3,3)=19$ exceeds the 15 stated output requirements |
| $\hbar_\Phi$ | Throughout (TN-01, 03, 05, 06, 16) | **5 — Free/unexplained** | Never independently fixed anywhere in the corpus |
| $R$ (moduli-space radius, $S^1$ toy) | TN-03 | **5 — Free/unexplained** | Arbitrary toy-model input |
| $\kappa_\Phi$ (Wilson/gauge coupling) | TN-05, 06, 13 | **5, conditionally 3** | TN-13: *would* move to "fixed by known equivalence" (dimensional transmutation) *if* DAG regularity holds — but that precondition is itself unresolved (TN-14/15), so the escape is currently blocked, not achieved |
| $J$ (symplectic normalization on $S^2$) | TN-05 (Gate 3), TN-06 | **5 — Free/unexplained** | TN-06 didn't just fail to derive it — it showed the specific candidate action ($S_W$) structurally *cannot* supply it (no velocity terms, exactly zero on the moduli space) |
| $c$ (percolation growth parameter) | TN-08 onward, audited TN-17 | **5 — Free/unexplained** | Five candidate sources checked directly against the full corpus; none found |

**Summary statistic:** of eight dimensionless parameters introduced across the entire eighteen-note sequence, **seven are Category 5 outright, and the eighth ($\kappa_\Phi$) is Category 5 in the theory's current state**, with its only escape route blocked by a separate open question. **Zero parameters currently qualify as Category 1, 2, or 3 unconditionally.** This is not a selective sample — it is every dimensionless parameter this thread's own notes introduced, checked against the same standard.

---

## 3. Selector audit: does any of the four types already exist?

**1. $\mathcal C_{\rm UPT}=\operatorname{argmin}_{\mathcal C}\mathcal A[\mathcal C]$.** This requires an action functional defined *over the space of possible $\mathcal X$'s* (or possible $c$'s), not over field configurations $\Phi$ on a *fixed* $\mathcal X$. Every action constructed in this thread ($S_W$, $S_\Phi$, the polynomial $\mathcal S_\Phi$) is of the latter kind. **No candidate exists.**

**2. $c=c(\text{fixed point})$.** TN-16 found a genuine critical value, $c=1$ — but this is a percolation phase transition in the growth probability, not an RG fixed point of a running coupling in the field-theoretic sense the framing document intends, and TN-17 already tested it directly and found the check methodologically inconclusive (near-critical relaxation is algebraic, and the seed-matching used elsewhere in this thread isn't rigorous there). **No confirmed candidate exists.**

**3. $c=c(\text{topological invariant})$.** TN-05's topological result ($\mathcal M_\Phi\cong S^2$) concerns the flat $SU(2)$ holonomy sector on a *fixed* graph; nothing in that construction references or constrains $c$, which governs how the graph itself is built. These remain two disconnected layers, exactly as TN-13 §2 already noted for $\kappa_\Phi$'s relationship to topology. **No candidate exists.**

**4. $c=c(\text{stability condition})$.** This is precisely what TN-01's addendum attempted (for different couplings) and TN-17 cited as directly relevant prior evidence: the mechanism was tested concretely and found to have no interior stationary point. **No working candidate exists, and one specific attempt already failed.**

$$
\boxed{\textbf{None of the four selector types is currently realized by any construction in the UPT corpus. This is recorded as an axiomatic gap.}}
$$

---

## 4. The sharper ontological statement

Per the reasoning in the framing document, the emergence chain as actually demonstrated is not
$$
\Phi \to \mathcal X \to g_{\mu\nu},
$$
but
$$
\Phi \to \mathcal X_c \to g_{\mu\nu}^{(c)},
$$
with $c$ (and, conditionally, $\kappa_\Phi$) left as an external index on a *family* of possible emergent geometries, not a single determined one. This is a more precise and more honest restatement of TN-16/17's findings than "the predicted dimension is wrong" — the issue is one level upstream of any specific numerical prediction.

---

## 5. Two frozen rules, now both explicit

$$
\boxed{\text{1. Do not search for } c \text{ such that } d_\ast=4. \quad\quad \text{2. Do not introduce a selection functional solely because an existing parameter is undetermined.}}
$$

Rule 2 is why this note does not propose a candidate $\mathcal A[\mathcal C]$, fixed-point condition, or stability principle of its own. Per the framing document's own logic: if UPT needs a new selector, the correct statement is that UPT requires an additional postulate — not that this note should supply one and present the result as a prediction.

---

## 6. Status update

$$
\boxed{
\begin{array}{ll}
\text{Structural emergence:} & \text{promising and partially demonstrated (TN-05, TN-07)} \\
\text{Unique physical selection:} & \text{not demonstrated — audited and found absent (this note)} \\
\text{Phenomenological realization:} & \text{currently unsuccessful (TN-01)} \\
\text{Fundamental dynamical completion:} & \text{unresolved (TN-06, 08, 09; conditionally open via TN-11-17)}
\end{array}
}
$$

This closes Phase I's line of inquiry into whether existing UPT machinery secretly already contains a selection principle. It does not. The distinction the framing document draws is the correct one to carry forward: Phase I asked whether the architecture survives audit (largely yes, per TN-05/07's genuine positive results); the next phase's question is different in kind — what additional principle, if any, would be *required*, not whether one can be invented and retrofitted.

---

## 7. Audit of this audit

| Claim | Status |
|---|---|
| Every dimensionless parameter in TN-01–17 classified | **Done** — 8 parameters, table in §2 |
| 7/8 unconditionally Category 5 | **Confirmed by direct count** |
| $\kappa_\Phi$'s conditional Category 3 status | Contingent on TN-13/14/15's unresolved regularity question — not an achieved escape |
| All four selector types checked against actual (not hypothetical) UPT constructions | **Done**, §3 |
| A new selector proposed in this note | **No** — explicitly avoided per Rule 2 |

---

## Provenance note

This note performs the TN-18 audit proposed in a subsequent joint review: a full parameter classification (not previously compiled in this consolidated form) and a check of four selector types against the actual corpus rather than hypothetical constructions. No new computation was required or performed; all classifications restate and cross-reference findings already established in TN-01 through TN-17. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
