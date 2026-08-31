# Technical Note UPT–TN–14

## Continuum Regularity of the UPT Update DAG: A Pre-Registered Test That Corrected Itself Mid-Analysis

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Pre-registered criterion (stated before running anything)

Per the requested methodological safeguard, the criterion was fixed before measurement: regularity is **supported** if (a) $\sigma_d(\text{interval size})$ decreases as interval size grows for $\mathcal X_{\rm UPT}$, and (b) that decrease tracks $\mathcal X_{\rm regular}$ (a genuine 4D Minkowski sprinkling) rather than $\mathcal X_{\rm random}$ (a Kleitman–Rothschild-type 3-layer random poset — the standard, well-documented example of a combinatorially typical but maximally non-manifold-like finite poset). Regularity is **not supported** if $\mathcal X_{\rm UPT}$ fails to track $\mathcal X_{\rm regular}$'s behavior.

**This criterion turned out to be necessary but not sufficient, and that correction — discovered by running the experiment, not assumed in advance — is itself part of this note's result.** Reporting it plainly rather than quietly substituting a better criterion after the fact.

---

## 2. Construction

- $\mathcal X_{\rm UPT}$: transitive percolation ($N=300$, $p=0.10$) — the exact growth model tested in TN-07/TN-08.
- $\mathcal X_{\rm regular}$: Poisson sprinkling into 4D Minkowski space ($N=300$) — the calibrated-good reference from TN-07.
- $\mathcal X_{\rm random}$: a 3-layer Kleitman–Rothschild poset ($N=300$) — combinatorially typical among *all* finite posets, and known in the causal set literature to be essentially never manifold-like (the "entropy problem" of causal set theory: most finite posets look like this, not like a sprinkling).

"Local regions" were defined intrinsically for all three, with no coordinates used: **Alexandrov intervals** $I(p,q)=\{x: p\preceq x\preceq q\}$, sampled by drawing many random related pairs and binning the resulting intervals by size, then computing the Myrheim–Meyer ordering fraction $r$ within each interval.

---

## 3. Results

| Interval size | $\sigma_r$, $\mathcal X_{\rm UPT}$ | $\sigma_r$, $\mathcal X_{\rm regular}$ | $\sigma_r$, $\mathcal X_{\rm random}$ (KR) |
|---|---|---|---|
| [8,16) | 0.1040 | 0.0790 | **0.0140** |
| [16,28) | 0.0661 | 0.0527 | **0.0177** |
| [28,45) | 0.0513 | too few samples | 0.0103 |
| [45,70) | 0.0386 | too few samples | too few samples |
| [70,110) | 0.0321 | too few samples | too few samples |
| [110,300) | 0.0420 | too few samples | too few samples |

**The pre-registered criterion is immediately complicated by the KR reference.** The known-bad ensemble has the *smallest* variance of the three, not the largest — it decreases (mildly) with size just like the other two. Low $\sigma_r$ does not distinguish manifold-like from non-manifold-like structure; a poset can be *consistently* non-geometric just as easily as *consistently* geometric, and a KR poset's rigid 3-layer structure produces exactly this: stable, low-variance, but not corresponding to any finite embedding dimension. **The originally pre-registered criterion is therefore insufficient on its own — this is a genuine correction to the stated methodology, not a redefinition of success after seeing a favorable result** (the correction makes the test *harder* to pass, not easier).

---

## 4. The more decisive signal: mean stability, not just variance

The mean ordering fraction across scales is the sharper diagnostic, because Myrheim–Meyer theory predicts $r$ should be approximately **scale-invariant** for a genuine fixed-dimension causal set (independent of interval size, for a homogeneous sprinkling) — not merely low-variance.

| Interval size | mean $r$, $\mathcal X_{\rm UPT}$ | mean $r$, $\mathcal X_{\rm regular}$ |
|---|---|---|
| [8,16) | 0.733 | 0.445 |
| [16,28) | 0.591 | 0.309 |
| [28,45) | 0.551 | (too few) |
| [45,70) | 0.559 | — |
| [70,110) | 0.619 | — |
| [110,300) | **0.722** | — |

**$\mathcal X_{\rm UPT}$'s mean $r$ is not scale-invariant — it dips and then rises back toward $0.72$ at the largest intervals**, drifting toward the totally-ordered limit $r\to1$ exactly as TN-08 found for the *global* ordering fraction at fixed $p$. This is the same pathology recurring at the local, interval level: fixed-$p$ transitive percolation does not produce a structure that looks the same at different scales, which is precisely what "continuum regularity" requires.

**Honest limitation on the comparison:** $\mathcal X_{\rm regular}$ could only be sampled at the two smallest bins ($N=300$ was not large enough to produce many big Alexandrov intervals in a 4D sprinkling at this density) — the reference series is too short to say definitively whether it *would* stabilize at larger sizes. This limits how strong a positive claim can be made for the "good" reference, but does not weaken the negative finding for $\mathcal X_{\rm UPT}$, which is based on its own internal (non-monotonic, upward-drifting) trend, not on a comparison requiring the reference to be fully resolved.

---

## 5. Verdict

$$
\boxed{\textbf{Evidence from this test does not support continuum regularity for transitive percolation at fixed } p.}
$$

This is not a new failure — it is the same root cause TN-08 already identified (fixed $p$ does not give a stable dimension as $N$ grows) reappearing at the level of local sub-regions rather than the global causal set, confirming that TN-08's finding was not an artifact of looking only at the global statistic. TN-13's conditional rigidity result therefore **remains unmet, and this note narrows why**: not merely "regularity hasn't been checked," but "the specific growth model already in use in this thread shows a concrete, internally-consistent symptom of irregularity (non-scale-invariant local dimension), independently of any comparison to reference ensembles."

**What would need to change, precisely:** TN-08 already flagged, and did not implement, the known fix — scaling $p$ with $N$ (per Rideout–Sorkin's own published asymptotic-scaling analysis for transitive percolation) rather than holding it fixed. This note's finding sharpens the motivation for that specific, previously-identified fix, rather than introducing a new requirement.

---

## 6. Audit

| Claim | Status |
|---|---|
| Criterion pre-registered before measurement | **Done**, per requested safeguard |
| Pre-registered criterion (variance decrease) sufficient on its own | **False** — corrected mid-analysis; KR poset also shows low/decreasing variance |
| Mean-stability (scale-invariance of $r$) is the sharper diagnostic | Identified as the correct complementary test |
| $\mathcal X_{\rm UPT}$ (fixed-$p$ percolation) shows scale-invariant local dimension | **No** — mean $r$ drifts non-monotonically, rising toward 1 at large scales |
| This reproduces a known TN-08 pathology at the local level | **Yes** |
| $\mathcal X_{\rm regular}$ reference fully resolved at all tested scales | **No** — under-sampled at larger interval sizes at this $N$; an honest data limitation |
| Continuum regularity established for minimal UPT | **Not established; current evidence leans negative** |

---

## 7. Conclusion

This note did what TN-13 required and no more: it did not touch matter, phenomenology, or the Standard Model, and it tested exactly the named precondition (DAG regularity) directly, with the criterion fixed in advance. The result is a genuine, if qualified, negative: the specific causal-growth model used throughout this thread does not show the scale-invariant local structure that continuum regularity requires, for a reason already identified in TN-08 and now confirmed to operate at the local (not just global) level. The path forward is precise, not vague: implement the $p(N)$ scaling TN-08 named but did not test, and rerun this same local-regularity diagnostic before revisiting TN-13's conditional rigidity claim.

---

## Provenance note

This note tests the DAG-regularity precondition identified in TN-13, per the narrowed TN-14 mandate in a subsequent joint review (regularity only, no matter or phenomenology). The pre-registered criterion, its own mid-analysis correction (variance alone is insufficient; the KR poset reference exposed this), and the mean-stability diagnostic that replaced it are all reported as they occurred, including the limitation in the $\mathcal X_{\rm regular}$ reference sampling. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
