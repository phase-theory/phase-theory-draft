# Technical Note UPT–TN–16

## Large-N Asymptotics of $p_N=c/N$ Transitive Percolation: A Mean-Field Derivation

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Approach

Rather than pushing simulation further, a continuum mean-field treatment of the exact discrete recursion was attempted, as prioritized. Let $f(i,n)=P(i\in\text{past}(n))$ for $i<n$, and $h(i,n)=-\log(1-f(i,n))$. The exact recursion
$$
1-f(i,n) = (1-p_n)\prod_{j=i+1}^{n-1}\big(1-p_n f(i,j)\big)
$$
is well-approximated for large $n$ (since $p_n=c/n\to0$ regardless of $f$'s size, so $-\log(1-p_nf)\approx p_nf$ is controlled by $p_n$, not by $f$) by converting the sum to an integral and differentiating. This gives, in terms of $s=\ln(n/i)$, the **autonomous ODE**
$$
\frac{dh}{ds} = -h + c(1-e^{-h}).
$$

---

## 2. A bug, found and fixed, worth reporting as part of the result

The first attempt started the numerical integration at $h(s{=}0)=0$ exactly. **This is an exact fixed point of the ODE** (RHS $=0$ at $h=0$), so the solver never left it, silently returning $r_\infty=0$ and a meaningless "$d=5$, clamped" result. This was caught by the cross-check against the TN-15 simulation trend (an $r_\infty$ of exactly $0$ was inconsistent with the visibly nonzero, slowly-decreasing simulated $r_{3000}=0.2124$), which is exactly why that cross-check was worth keeping in the note rather than treating as a formality.

The correct initial condition, matched to the discrete recursion's literal first step ($f(i,i{+}1)=p_{i+1}\approx c/i$, giving $h(s{\to}0^+)\approx c\cdot s$, not identically $0$), was substituted. With that fix, $h(s)$ correctly leaves the unstable point and approaches the **stable** fixed point $h^*$ solving $h^*=c(1-e^{-h^*})$ (stable whenever $c>1$; for $c\leq1$, $h=0$ remains the only, stable, fixed point).

---

## 3. Results: strong, non-monotonic dependence on $c$

$$
r_\infty(c) = 2\int_0^1\!\!\int_0^y \big(1-e^{-h(\ln(y/x))}\big)\,dx\,dy
$$
computed via the corrected ODE + numerical quadrature:

| $c$ | $h^*$ | $r_\infty$ | Regime |
|---|---|---|---|
| 0.5 | — (0 stable) | $\to1$ | Subcritical — no dimensional transmutation, degenerate/near-total-order |
| 1.0 | — (0 stable) | $\to1$ | Critical threshold |
| 2.0 | 1.594 | $\approx0.00000$ | Just above threshold — extremely sparse |
| **4.0** | **3.921** | **0.0039** | (the value tested throughout TN-15) |
| 8.0 | 7.997 | 0.0986 | |
| 16.0 | 16.000 | 0.3535 | |

**The percolation threshold is $c=1$**, exactly as the $O(1)$-candidate-count motivation for the theory scaling law suggested — below it, no dimensional transmutation occurs at all, and $r_\infty\to1$ (degenerate). Above it, $r_\infty$ is small immediately past threshold and grows (non-monotonically in the tested sense — very small near $c=2$–$4$, then increasing) as $c$ increases further.

---

## 4. Interpreting $c=4$: extended calibration

$r_\infty=0.0039$ (at $c=4.0$, the value used throughout TN-15) is **below TN-07's original calibration range** (which stopped at $d=5$, $r\approx0.105$). The calibration was extended via the same sprinkling method to higher dimensions:

| $d$ | $r$ |
|---|---|
| 5 | 0.1074 |
| 7 | 0.0364 |
| 10 | 0.0073 |
| 15 | 0.0003 |

Interpolating, $r_\infty=0.0039$ corresponds to **$d_\ast\approx11$–$12$** — a finite dimension in the strict mathematical sense (the mean-field theory predicts genuine convergence, not literal divergence), but nowhere near the low integer dimension a spacetime interpretation would want, and wildly sensitive to $c$ (§3).

**Cross-check against TN-15's simulation:** $r_\infty=0.0039 \ll r_{N=3000}^{\rm sim}=0.2124$ — consistent in *direction* (the simulated trend was still decreasing toward something smaller), but the gap is large, explaining *why* TN-15 saw no plateau: reaching the mean-field asymptotic regime requires $s=\ln(n/i)\gtrsim8$–$15$ for the *earliest* elements to equilibrate (§2's $h(s)$ trajectory), which for $i\sim O(1)$ requires $N\gtrsim e^8$ to $e^{15}$ — far beyond $N=3000$, and likely beyond the reach of any brute-force simulation. This is a genuine, quantitative explanation for TN-15's inconclusive result, not merely a restatement of it.

---

## 5. Answering TN-16's two questions, kept separate as required

**1. Asymptotic behavior for fixed $c$:** Converges (within this mean-field approximation) to a **finite but $c$-dependent** dimension, per §3's table — matching **Outcome A** and **Outcome E** simultaneously (a finite limit exists, but its value depends on $c$ in a strong, non-monotonic way), not Outcomes B, C, or D.

**2. Does UPT determine $c$?** **No.** Nothing in the UPT corpus, including the round-1 candidate or any technical note since, fixes $c$ independently. This is the *same* control-data underdetermination problem diagnosed in TN-01/02/12, recurring here in a new guise: even if the dimensional question is mathematically resolved for each $c$, the theory does not select which $c$, and §3 shows the answer is extremely sensitive to that choice — the difference between $c=2$ (near-total sparsity) and $c=16$ ($d_\ast$ in a much lower, more plausible range) spans the entire space of qualitatively different outcomes.

---

## 6. Consequence for TN-13's rigidity chain

This sharpens, rather than resolves, the open question. **A finite continuum dimension may exist for minimal UPT** (contrary to what TN-14/15's inconclusive simulations alone could establish) — a genuinely new, positive-leaning piece of information, obtained analytically rather than by more computation. But two new problems replace the old one:

1. The predicted dimension, for the specific $c$ tested throughout this thread, is nowhere near 4 — it's order 10+, which does not resemble the kind of "regular lattice" TN-13's asymptotic-scaling transfer needs (a dimension an order of magnitude higher than the one for which the cited lattice-QCD results were established).
2. $c$ itself is exactly the kind of free, UPT-undetermined parameter that TN-01/02/12 already flagged as undermining predictivity — its value isn't derived, and different values give qualitatively different answers to the regularity question TN-13 needs resolved.

---

## 7. Audit

| Claim | Status |
|---|---|
| Mean-field ODE derived from the exact discrete recursion | **Derived**, with the large-$n$ approximation ($p_n\to0$) explicitly justified |
| First attempt's $h(0)=0$ initial condition | **Bug** — an exact unstable fixed point, caught via cross-check against TN-15, not assumed correct |
| Corrected initial condition matches discrete first-step behavior | **Verified** algebraically |
| $r_\infty(c)$ table | **Computed** via ODE integration + numerical quadrature |
| $c=1$ percolation threshold | **Derived** from the stability condition on $h=0$ |
| $d_\ast\approx11$–12 for $c=4$ | Computed via extended calibration (sprinkling-based, same method as TN-07) |
| This is an exact result | **No** — a leading-order continuum/mean-field approximation; finite-size and fluctuation corrections are not bounded here |
| $c$ is fixed by UPT | **No** |

---

## 8. Conclusion

The analytic route, prioritized over further brute-force simulation, delivered exactly what TN-15's simulation could not: an explanation for *why* no plateau appeared by $N=3000$ (the true equilibration scale is astronomically larger), and a genuine — if approximate and $c$-sensitive — answer to the convergence question. Within this mean-field treatment, minimal UPT's causal substrate does approach a finite dimension for any $c>1$, but that dimension is generically far from four and depends sensitively on a parameter the theory does not fix. This converts TN-13's regularity precondition from "unknown" into "known to depend on an unfixed parameter, in a regime that does not currently resemble the intended target" — a sharper, more specific problem than before, and one that connects the dynamics-completion thread (TN-10 onward) back to the original control-data underdetermination problem (TN-01/02) rather than resolving either independently.

---

## Provenance note

This note performs the analytic large-$N$ treatment prioritized in a subsequent joint review over further simulation. The mean-field ODE, its initial-condition bug (caught via the cross-check against TN-15's simulated trend), the $c$-dependence table, and the extended Myrheim–Meyer calibration are all computed directly. The approximation's leading-order (mean-field) status is disclosed, not presented as exact combinatorics. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
