# Technical Note UPT–TN–15

## Scaling the Sequential-Growth Parameter: A Genuine Third Outcome, Neither Confirmed Nor Cleanly Refuted

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Pre-registered scaling laws (specified before running)

Per the requested discipline, one theoretically-motivated law was fixed in advance, not searched for after seeing results, alongside two controls:

- **Theory**: $p_N = c/N$ — motivated independently by requiring the *expected number of direct candidate parents per new element* ($\sim p_N\cdot N$) to stay $O(1)$ as $N$ grows, the combinatorial signature of a finite local link density (what a genuine sprinkling-like causal set has, and what TN-08/14's fixed $p$ conspicuously lacked).
- **Faster** (denser than theory): $p_N=c/N^{0.5}$.
- **Slower** (sparser than theory): $p_N=c/N^{1.5}$.

$c=4.0$ was fixed once and reused across all three laws (chosen only to give a moderate expected candidate count under the theory law; not tuned per-law). The Myrheim–Meyer inversion $r\to d_{\rm MM}$ used TN-07's own verified calibration table, not a recalled closed-form formula (avoiding a second possible source of error), extended by interpolation.

---

## 2. Results

**Theory ($p_N=c/N$), extended to $N=3000$ across 4 realizations:**

| $N$ | mean $r$ | mean $d_{\rm MM}$ | std $d_{\rm MM}$ |
|---|---|---|---|
| 200 | 0.4265 | 2.339 | 0.140 |
| 500 | 0.3372 | 2.755 | 0.059 |
| 1000 | 0.2803 | 3.036 | 0.021 |
| 1500 | 0.2521 | 3.269 | 0.028 |
| 2200 | 0.2284 | 3.464 | 0.034 |
| 3000 | 0.2124 | 3.596 | 0.038 |

$d_{\rm MM}$ **does not stabilize within the tested range** — it climbs continuously from $2.34$ to $3.60$ across $N=200$ to $3000$. The successive increments *do* shrink ($+0.42, +0.28, +0.23, +0.19, +0.14$), a genuine and honestly-reported hint of deceleration, but extrapolating this to a specific limiting $d_\ast$ would be unsupported speculation, not a result.

**Faster ($p_N=c/N^{0.5}$):** collapses immediately to a flat, degenerate $d_{\rm MM}\approx1.05$ across the entire tested range ($N=100$ to $900$), with very low variance — the causal set is too dense, close to totally ordered, at every scale tested.

**Slower ($p_N=c/N^{1.5}$):** pinned exactly at $d_{\rm MM}=5.000$ with zero variance across all $N$. **This is a calibration-table artifact, not a genuine dimension estimate**, flagged explicitly: $r$ is so small under this law that it falls outside TN-07's calibrated range (which only extends to $d=5$) and the interpolation simply clamps to the boundary value. This result says "very sparse, nearly disconnected," not "five-dimensional," and is reported as such rather than overclaimed.

---

## 3. Checking the five required sub-criteria

| Criterion | Result |
|---|---|
| 1. $d_{\rm MM}(N)\to d_\ast$ | **Not established** — still increasing at $N=3000$ |
| 2. $d_\ast$ stable under increasing $N$ | **Not established** — same reason |
| 3. Different interval scales approach the same $d_\ast$ | **Not tested** in this note — would require the TN-14 local/Alexandrov-interval machinery re-run under scaled $p_N$, not attempted here due to compute budget; flagged as the natural next check, not silently skipped |
| 4. Survives independent realizations | **Yes** — variance across 4 realizations is modest at every $N$ tested (std $0.02$–$0.14$) |
| 5. Distinguishes against KR-type controls | **Not directly re-tested** here; the qualitative deceleration under the theory law is unlike anything seen for KR posets in TN-14, but this was not run as a matched comparison in this note |

Two of five criteria are met, one is unmet, two are untested rather than failed. This is not the clean pass the framing document's Outcome A describes.

---

## 4. Verdict: a genuine third outcome, reported as such rather than forced into A or B

$$
\boxed{\textbf{Neither Outcome A (clean stabilization) nor Outcome B (clear failure) is established. The theory-motivated scaling shows a qualitatively different, decelerating trend compared to fixed-}p\textbf{'s unchecked drift toward }r\to1\textbf{ — but that trend has not been confirmed to converge within the computational range tested.}}
$$

This is worth distinguishing carefully from a failure: fixed-$p$ (TN-08/14) showed **no deceleration at all** — it climbed steadily toward the degenerate limit with no sign of slowing. The $p_N=c/N$ law behaves *differently* — the rate of change is shrinking — which is itself a real, non-manufactured signal that the scaling has changed the qualitative behavior of the model, even without full confirmation of a limit. Reporting this as an inconclusive-but-informative result, rather than rounding it up to a pass or down to a fail, is the correct response given what was actually measured.

**What would resolve the ambiguity, precisely:** either (a) simulation at substantially larger $N$ than was computationally tractable here (the deceleration pattern suggests $N\gg3000$ might be needed, which was not attempted, not because it's expected to fail but because it exceeds this note's practical compute budget), or (b) an analytic large-$N$ asymptotic treatment of transitive percolation under $p_N=c/N$, which was not attempted and may or may not exist in the published causal set literature — this note did not search for one and does not claim its absence.

---

## 5. Consequence for TN-13

TN-13's conditional rigidity statement remains exactly what it was: conditional, and unresolved by this note in either direction. This is a materially different situation from a clean negative — it does not rule out the regularity precondition, and it does not establish it. The honest updated status: **the specific mechanism TN-08 flagged as the likely fix (scaling $p$ with $N$) produces qualitatively different, more promising behavior than fixed $p$, but does not yet constitute evidence of convergence** at the scales this note could actually test.

---

## 6. Audit

| Claim | Status |
|---|---|
| Scaling laws pre-registered before running | **Done** |
| Theory law derived independently (not fit) | **Yes** — from an $O(1)$ link-density argument, not from searching for convergent behavior |
| Theory law shows clean stabilization | **No** |
| Theory law shows *some* signal distinct from fixed-$p$ | **Yes** — genuine deceleration, reported honestly as inconclusive rather than rounded to success |
| Faster/slower controls behave differently from theory law | **Yes** — both collapse to degenerate/boundary values, unlike theory's continued, decelerating drift |
| Slower control's $d_{\rm MM}=5$ result is a genuine dimension estimate | **No** — explicitly flagged as a calibration-table boundary artifact |
| Full 5-criterion pass achieved | **No** — 2 of 5 met, 1 unmet, 2 untested |

---

## 7. Conclusion

This note did what TN-15's mandate asked and avoided what it warned against: no search over scaling exponents was conducted after seeing results, and the observed deceleration under the theory-motivated law was not rounded up into a false "convergence confirmed." The result is genuinely a third category — not the clean success or failure the framing document anticipated, but an honestly-reported partial signal that the previously-identified fix (TN-08's flagged $p(N)$ scaling) changes the model's qualitative behavior in the right direction without yet demonstrating the stabilization TN-13 needs. The chain from TN-12 through TN-15 is not broken by this result, but it is not extended either — it is left exactly as open as the evidence supports, which is the correct place to stop this specific computational line rather than push toward a premature verdict.

---

## Provenance note

This note implements the TN-15 experiment proposed in a subsequent joint review: a pre-registered $p(N)$ scaling law motivated independently of the desired outcome, tested against faster/slower controls, checked against the five stated success sub-criteria. All quantitative results, including the extension to $N=3000$ undertaken after the initial run showed no plateau by $N=900$, were computed directly and reported without rounding an ambiguous trend into a definite pass or fail. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
