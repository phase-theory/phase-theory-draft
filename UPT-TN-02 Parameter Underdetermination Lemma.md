# Technical Note UPT–TN–02

## The Parameter-Underdetermination Lemma for Polynomial-Potential Realizations of 𝓕

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Statement

Let a candidate realization of the universal phase equation be specified by a variational functional
$$
\mathscr F[\Phi] = \frac{\delta \mathcal S_\Phi}{\delta\Phi} = 0,
\qquad
\mathcal S_\Phi = \mathcal S_{\mathrm{grad}} + \mathcal S_{\mathrm{int}} + \mathcal S_{\mathrm{topo}} + \mathcal S_{\mathrm{stab}},
$$
with a potential built from $N$ phase invariants $I_1,\ldots,I_N$ as an unrestricted symmetric polynomial of total degree $D$:
$$
V(I_1,\ldots,I_N) = \sum_{|\alpha|\le D} c_\alpha\, I^\alpha.
$$

**Lemma (Parameter-Underdetermination).** *The number of independent coefficients in $V$ is*
$$
\boxed{P(N,D) = \binom{N+D}{D}, \qquad P_{\mathrm{phys}}(N,D) = \binom{N+D}{D}-1}
$$
*(excluding the physically irrelevant constant term). If the theory's total control-data dimension — including $V$'s coefficients together with the unspecified functional data $G^{AB}(\Phi)$, $\mathcal A_A[\Phi]$, the invariant basis $\{I_n\}$, and $\mathcal S_{\mathrm{topo}}$ — satisfies*
$$
\dim\Theta_{\mathrm{free}} \ge M,
$$
*where $M$ is the number of independent target observables, then reproduction of any specific observed vector $\mathbf y_{\mathrm{obs}}\in\mathbb R^M$ by the realization does not, by itself, constitute predictive success.*

This confirms and generalizes the direct count performed in UPT-TN-01's addendum and the companion analysis of the continuum candidate: $P_{\mathrm{phys}}(3,3)=19$ already exceeds the $M=15$ output requirements enumerated for a full candidate realization, before $G^{AB}$, $\mathcal A_A$, or $\mathcal S_{\mathrm{topo}}$ contribute any further freedom. The count is a lower bound on the true underdetermination, not an estimate of it.

---

## 2. The sharper criterion: rank, not count

Parameter count alone is a weak diagnostic — a model could have many parameters but still make sharp predictions if most combinations are unobservable. The operationally correct criterion is the rank of the observable map.

Let $\mathcal O:\Theta\to\mathbb R^M$ send theory parameters to computed observables (masses, mixing angles, gauge content, etc.). Define
$$
r = \operatorname{rank}\left(\frac{\partial \mathcal O_i}{\partial\theta_j}\right).
$$

- If $r < M$: some observables are not independently controllable by the theory at all — no choice of parameters can fit them independently of each other. This is a genuine, falsifiable structural constraint (a *good* outcome for predictivity, in the sense that it makes correlated predictions — cf. UPT-TN-01's finding that the equal-spacing law made a real, testable, and falsified prediction).
- If $r = M$ but $\dim\Theta_{\mathrm{free}} \gg M$: the map is locally surjective, and a continuous family of parameter choices reproduces any given observation. This is the situation diagnosed in Section 1 and in every generation/Yukawa computation performed in this thread.

$$
\boxed{\text{fit} \neq \text{prediction.}}
$$

A construction demonstrates predictive content only by exhibiting $r<M$ relations among observables that hold *before* fitting — analogous to how UPT-TN-01's equal-spacing law was a genuine, falsifiable, parameter-free relation (which then failed against data), as distinct from the exact per-family fit that followed it (which had $r=M$, $\dim\Theta_{\mathrm{free}}=M$, and therefore tested nothing).

---

## 3. Consequence for the candidate-realization programme

Sections 1–2 imply that the correct next move for any future candidate realization is **not** to begin with an unrestricted polynomial ansatz and hope that fitting succeeds. The polynomial ansatz is an effective-theory parametrization by construction, and effective theories are underdetermined by design until an independent principle fixes the coefficients.

The required standard is instead:

$$
\boxed{\text{derive the admissible action from a minimal, independently motivated axiom set.}}
$$

Candidate axioms to test for uniqueness power (untested in this note — a further open task):

- phase covariance,
- locality in phase configuration space,
- boundedness / stability of the vacuum,
- reparameterization invariance,
- finite phase information density,
- topological consistency,
- existence of a stable vacuum sector.

If such a set forces a unique or finite-dimensional family of admissible $\mathcal S_\Phi$, the resulting coefficients become physically meaningful rather than fitted. Whether any such set does so is not established here; it is the correct next falsifiable question, replacing "does the polynomial fit the data" with "does anything force the polynomial's shape at all."

---

## 4. Audit

| Claim | Status |
|---|---|
| $P(N,D)=\binom{N+D}{D}$ | Derived (combinatorics of symmetric polynomials) |
| $P_{\mathrm{phys}}(3,3)=19$ | Confirmed by direct count |
| $19 > 15$ (coefficients exceed requirements) | Confirmed |
| True $\dim\Theta_{\mathrm{free}}$ exceeds coefficient count alone | Asserted, not separately quantified — $G^{AB}$, $\mathcal A_A$, $\{I_n\}$, $\mathcal S_{\mathrm{topo}}$ are functional (infinite-dimensional) data whose freedom was not bounded in this note |
| Fit vs. prediction distinguished by rank $r$ | Stated as the correct criterion; not computed for any specific realization here |
| A minimal axiom set uniquely fixes $\mathcal S_\Phi$ | **Open** — this is the proposed next task, not a result |

---

## 5. Conclusion

This note converts an informal complaint ("too many free coefficients") into a reusable structural lemma with a sharper companion criterion (rank of the observable map, not raw parameter count). It applies to any future polynomial-potential candidate realization of $\mathscr F$, not only the ones already tested in this thread, and it identifies the correct standard such a candidate must meet before any fit to observed masses, couplings, or generation structure can be treated as evidence rather than curve-fitting.

---

## Provenance note

This note formalizes a joint diagnostic developed across two independent AI-assisted analyses of the same candidate-realization document: a direct coefficient count, and its subsequent generalization into a rank-based fit/prediction criterion. It is written entirely within the UPT datum $\mathfrak U=(E_\Phi,\mathscr G_\Phi,\mathcal C_\Phi,\mathscr F,\Lambda)$ and supersedes any framing in terms of the earlier Phase Theory axiom system, per current programme direction.
