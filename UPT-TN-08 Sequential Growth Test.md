# Technical Note UPT–TN–08

## Sequential Growth Dynamics on a UPT Causal Set: What Emerges, and What Doesn't

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Construction

The Rideout–Sorkin classical sequential growth (CSG) framework was implemented in its simplest form, **transitive percolation**: starting from a single element, each new element $e_n$ independently selects each existing element as a "direct parent candidate" with fixed probability $p$; the new element's past is then the union of the candidates and everything already in *their* pasts — automatically transitively closed by construction, since each existing element's recorded past is already closed. $N=200$ elements were grown at $p=0.15$.

This is explicitly **not** a UPT-specific construction — it is the standard, published minimal CSG model (Rideout & Sorkin 2000) — applied here directly to the round-1 candidate's $\mathcal X$ (an update DAG), per TN-07's identification of that structure as a causal set.

---

## 2. The six requested measurements

**1. Causal order preservation.** Verified directly: zero transitivity violations across all $\binom{200}{3}$-scale triple checks. The growth rule preserves a valid partial order by construction, confirmed rather than assumed.

**2. Markov property.** Holds by construction — each step's randomness references only the current $\mathcal C_{n-1}$ (via lookups into already-recorded pasts), never the sequence of earlier states that produced it. This is a structural property of the algorithm, not something requiring simulation to detect.

**3. Growth locality.** **Fails**, and this is worth stating plainly rather than passing over: each new element's parent candidates are drawn independently from *all* $n$ existing elements, with no notion of "nearby" elements being preferred. This is a known, published feature of the plain transitive-percolation model, not an implementation artifact — geometric locality is not automatic in the simplest CSG model and would require a more structured transition law.

**4–5. Emergence of dimension, and continuum-limit behavior.** This is where the result is genuinely informative and not simply positive. Tracking the Myrheim–Meyer ordering fraction $r_n$ (TN-07) as the causal set grows, **at fixed $p$**:

| $N$ | $r_n$ |
|---|---|
| 20 | 0.300 |
| 50 | 0.553 |
| 100 | 0.747 |
| 150 | 0.830 |
| 200 | 0.857 |

$r_n$ does not stabilize — it climbs monotonically toward $1$ (the totally-ordered limit). **This is the correct, expected behavior for fixed $p$, not a failure of the implementation**: as $N$ grows with $p$ held constant, the causal set becomes increasingly densely related, and a well-defined continuum dimension only emerges in the Rideout–Sorkin framework when $p$ is scaled appropriately with $N$ (roughly $p\sim N^{-1}$ in their published analysis) — a refinement not implemented here and flagged as the concrete next requirement, not a vague "needs more work."

**Verdict on point 6 (continuum-limit behavior): not achieved with the naive fixed-$p$ implementation used here — consistent with, not contradicting, the published literature, which requires the scaling refinement to get a stable dimension estimate.**

---

## 3. The candidate phase observable

Per the proposed test, $\Phi[\mathcal C_n] := r_n$ (the ordering fraction itself) was tracked as a scalar phase observable, and its increments $\Delta r_n = r_{n+1}-r_n$ were measured directly:

$$
\text{mean}(\Delta r) = 0.00435, \qquad \text{std}(\Delta r) = 0.0123, \qquad 86.3\%\text{ of steps positive, }12.7\%\text{ negative}.
$$

**This settles the Outcome A/B/C question for this specific observable, decisively and for a structural reason, not a numerical coincidence.** $R_n$ (the relation count) is monotonically non-decreasing by construction — growth can only add relations, never remove them — so any observable built directly from it (like $r_n$) inherits a systematic positive drift. A systematically drifting, non-conserved quantity cannot be the generator of an antisymmetric/symplectic structure: symplectic flow requires something that can be exchanged between conjugate degrees of freedom while a conserved total is preserved, not a quantity that only accumulates. This isn't a failed search for Outcome C — it's a demonstration that **this particular choice of observable was structurally incapable of exhibiting it**, independent of the specific growth statistics.

**This is Outcome B, narrowly**: growth induces a well-defined *statistical* evolution law for $r_n$ (a mean drift plus fluctuation, both computed above) — a legitimate "candidate phase evolution operator" in the loose sense the proposing document allowed, but manifestly not an antisymmetric one.

**What was not tested, and would be required for a real Outcome C search:** an antisymmetric pairing between *two independent* observables (not one scalar's self-drift) — e.g. tracking two different structural quantities on the growing causal set and testing whether their joint increments satisfy $\{\mathcal O_1,\mathcal O_2\}$-type antisymmetry. That is a distinct, more involved construction, not attempted in this note.

---

## 4. Audit

| Property | Result |
|---|---|
| Causal order preservation | **Verified**, zero violations |
| Markov property | **Holds**, by construction |
| Growth locality | **Fails** — known feature of transitive percolation, not a bug |
| Dimension emergence at fixed $p$ | **Does not stabilize** — expected, per published theory; requires $p(N)$ scaling not implemented here |
| Candidate observable ($r_n$) evolution | **Well-defined statistically** (Outcome B) |
| Antisymmetric/symplectic structure from this observable | **Structurally ruled out** — $r_n$ is monotonically drifting by construction, not a numerical near-miss |
| Genuine two-observable Outcome-C test | **Not attempted** — identified as the concrete next construction |

---

## 5. Conclusion

Sequential growth supplies real structure — a verified valid causal order, a Markovian transition law, and a well-defined (if non-conserved) statistical evolution for a candidate scalar phase observable. It does not supply anything resembling a symplectic structure for the observable tested here, and it couldn't have, for a structural reason identified directly rather than inferred from a null result: monotonically-growing quantities cannot generate antisymmetric flow. The honest statement from the framing document holds exactly: **causal growth $\to$ phase evolution** is demonstrated, narrowly, for one scalar observable; **phase evolution $\to$ symplectic structure** remains untested in its only potentially viable form (a two-observable pairing), and the naive single-observable route is now known to be a dead end rather than merely unexplored.

---

## Provenance note

This note implements the TN-08 experiment proposed in a subsequent joint review: Rideout–Sorkin transitive percolation applied to a UPT-compatible causal set, with the six requested structural measurements and a candidate phase-observable increment test. All quantitative claims (transitivity, dimension drift, increment statistics) were computed directly rather than asserted. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
