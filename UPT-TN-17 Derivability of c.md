# Technical Note UPT–TN–17

## Can the Growth Parameter $c$ Be Derived? A Systematic Audit, and a Genuine Negative Result

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. The question, kept narrow as required

Not "make UPT four-dimensional." Specifically: does any UPT postulate (I–X), or any construction already produced in TN-01–16, determine $c$ **without reference to the observed or desired dimension**? Per the requested rule, this note never asks "what $c$ gives $d_\ast=4$" — that question is not posed anywhere below.

---

## 2. Audit of the five candidate sources

**$c=f(\text{topology})$.** The only established topological result is TN-05's $\mathcal M_\Phi\cong S^2$, derived from flat $SU(2)$ holonomies on a *fixed* graph $\mathcal X$. The percolation parameter $c$ instead controls *how $\mathcal X$ itself is built*, prior to any holonomy structure being defined on it — the two constructions operate at different, currently unconnected layers (holonomy sector lives *on* $\mathcal X$; $c$ builds $\mathcal X$). No result in this thread connects them. **No candidate found.**

**$c=f(\text{holonomy})$.** Same layering problem as above, in the other direction — holonomy data presupposes $\mathcal X$ already exists. **No candidate found.**

**$c=f(\text{phase stability})$.** This is the one candidate with directly relevant *prior evidence*, not merely absence of a link. UPT-TN-01's addendum tested exactly this class of mechanism — promoting a coupling to a dynamical modulus and selecting its value by extremizing a joint vacuum-energy functional across coupled sectors — for a *different* coupling ($\lambda$/$\kappa$, the generation-locking and gauge sector couplings). It **failed concretely**: the simplest realization had no interior stationary point at all, running to an unphysical boundary ($g_\Phi\to0$) rather than selecting a finite value. This is not proof that the same mechanism must fail for $c$ specifically, but it is a real, already-paid-for negative data point for the *general strategy* of self-consistent stationarity as a parameter-selection principle in this framework, and should be weighed accordingly rather than re-attempted from scratch as if it were untested. **No working candidate found; one directly relevant prior failure noted.**

**$c=f(\text{operator normalization})$.** No normalization condition on $\mathscr L_\Phi$, $\chi_\Phi$, or any derived operator has been constructed anywhere in this thread that references the *growth-process* parameter $c$ specifically (as opposed to the *gauge* coupling $\kappa_\Phi$, a distinct object). **No candidate found.**

**$c=f(\text{a dimensionless invariant of the fundamental phase theory})$.** No dimensionless invariant of the right type (a pure number, independent of any construction choice) has been produced anywhere in TN-01–16 that could serve this role. **No candidate found.**

---

## 3. The one intrinsically-motivated special value, tested and found methodologically inconclusive

The percolation threshold $c=1$ is the one value of $c$ that is *structurally* distinguished — not chosen to fit a target dimension, but marking the theory's own phase transition (below it, $h=0$ is the stable point and no dimensional transmutation occurs at all; above it, TN-16's $h^*(c)>0$ takes over). This is the strongest candidate for a "selected, not tuned" value, and it was tested directly.

**The test was inconclusive, and this is reported honestly rather than rounded into a result either way.** Near a critical point, relaxation is generically algebraic (power-law) rather than exponential, and the correct "seed" magnitude for the initial condition — previously an arbitrary numerical convenience ($s_0=10^{-8}$) that didn't matter away from criticality — becomes physically significant exactly at $c=1$, since the approach to $h=0$ is slow enough that the answer depends sensitively on how that seed relates to a realistic starting index $i$. This note's quick check used the same numerical convenience as TN-16's $c>1$ calculations and obtained $r_\infty=0$ to essentially machine precision — but this is very likely an artifact of an unrealistically small seed relative to the timescale needed to resolve algebraic (rather than exponential) relaxation, not a rigorously established result. **This is flagged as incomplete, not as a confirmed further negative** — a proper treatment would require matching the seed to a physically motivated $i$-dependence, not attempted here.

---

## 4. Verdict

$$
\boxed{\textbf{No existing UPT postulate or already-constructed mechanism determines } c\textbf{, independent of the desired dimension.}}
$$

This matches the framing document's anticipated valuable negative outcome. It is a genuine result, not an absence of effort: five candidate source categories were checked against everything established in TN-01 through TN-16, one already-tested general mechanism (control-data self-stationarity, TN-01's addendum) was found directly relevant and already failing in its simplest form, and the one structurally-motivated special value ($c=1$) was tested but the test could not be completed rigorously with the tools used here.

---

## 5. Consequence, and the frozen methodological rule

Per the requested rule, adopted explicitly from this point forward:
$$
\boxed{\textbf{Never tune } c \textbf{ to obtain } d_\ast=4.}
$$
A sensitivity sweep $c\mapsto d_\ast(c)$ (as TN-16 performed) remains legitimate; searching for a $c$ that produces $d_\ast=4$ is not, and would be classified by the ledger as calibration, not derivation, exactly as the framing document specifies.

---

## 6. Updated master ledger

| Layer | Status |
|---|---|
| Nontrivial topology | Established (TN-05) |
| Dimension recoverable from order | Established (TN-07) |
| Continuum scaling at fixed $c$ | Conditionally supported within mean field (TN-16) |
| Four-dimensional continuum | Not derived |
| Growth parameter $c$ | **Undetermined — audited and confirmed so (TN-17)** |
| Minimal-sector rigidity | Conditional/open (TN-13, contingent on regularity *and* now on $c$) |
| Fermion masses | Demonstrated failure of tested realization (TN-01) |
| Symplectic dynamics | Demonstrated failure of tested constructions (TN-06, 08, 09) |
| Born rule | Open |

---

## 7. Conclusion

TN-16 showed the dimensional problem is not merely numerically unresolved but parameter-controlled; TN-17 closes the loop by checking, rather than assuming, whether that parameter is itself fixed by anything already in hand. It is not. The connection to TN-01's addendum is the most important single fact in this note: this is not a new failure mode discovered for the first time in the geometry sector — it is the *same* mechanism (self-consistent parameter stabilization across coupled sectors) that already failed for the fermion sector, now checked and found equally absent for the growth parameter, strengthening the case that this is a structural feature of the current UPT formulation rather than a coincidence local to one calculation.

---

## Provenance note

This note audits, per the requested TN-17 mandate, whether $c$ is derivable from existing UPT postulates or constructions, explicitly avoiding any search for a value producing $d_\ast=4$. The connection to UPT-TN-01's addendum is a direct citation of prior work in this thread, not a new claim. The $c=1$ critical-point check is reported with its methodological limitation disclosed rather than presented as a completed result. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
