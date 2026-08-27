# Technical Note UPT–TN–09

## Paired Phase Observables on the Growing Causal Set: A Clean Failure of the Preservation Criterion

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Construction

Two observables $(Q_n,P_n)$ were built directly from the causal growth process, per the requirement that they arise from phase structure rather than arbitrary graph statistics: at each growth step, every newly formed causal relation contributes an independent random phase kick $\theta\sim\mathrm{Unif}[0,2\pi)$, and $Q,P$ accumulate its real/imaginary parts,
$$
Q_n = Q_{n-1}+\sum_{c}\cos\theta_{n,c}, \qquad P_n = P_{n-1}+\sum_{c}\sin\theta_{n,c}.
$$
This is the direct discretization of the document's $U_1=e^{iQT}$, $U_2=e^{iPT}$ suggestion: $(Q_n,P_n)$ are the accumulated real/imaginary parts of a product of per-relation holonomy-like phase factors. **This is a genuine new stipulation** — one specific way phase observables could arise from causal growth, not derived from deeper UPT postulates — flagged as such, not the only possible construction.

---

## 2. Non-monotonicity: the TN-08 problem is fixed

$\Delta Q$: 48.8% positive / 49.8% negative. $\Delta P$: 47.8% / 50.8%. Both well clear of the 86%/14% one-sided split that sank $R_n$ in TN-08. This construction genuinely avoids the structural obstruction identified there.

---

## 3. Oriented area — computed, but flagged against over-reading

$$
A_N = \sum_n\big(Q_n\Delta P_n - P_n\Delta Q_n\big) = -4256.4 \quad\text{(single realization, }N=300\text{).}
$$
This is nonzero, but **this number alone is not evidence of symplectic structure** and should not be presented as such. A generic 2D random walk with no conserved structure whatsoever also accumulates a nonzero oriented area over its trajectory (the discrete analogue of Lévy area for Brownian motion) — the statistic is sensitive to path history, not necessarily to any underlying conservation law. It is reported here for completeness, per the request, but the actual test is §4.

---

## 4. The ensemble transition operator

Per the document's stronger prescription, an ensemble-averaged linear transition operator was estimated by pooling $Q_n,P_n,\Delta Q_n,\Delta P_n$ across 40 independent growth realizations ($N=300$, $p=0.15$ each) and performing linear regression of $(\Delta Q,\Delta P)$ against $(Q,P)$:
$$
M = \begin{pmatrix}1.075\times10^{-3} & -2.339\times10^{-4}\\ -4.092\times10^{-4} & -6.939\times10^{-5}\end{pmatrix}.
$$
Decomposing:
$$
M_{\rm sym} = \begin{pmatrix}1.075\times10^{-3} & -3.216\times10^{-4}\\ -3.216\times10^{-4} & -6.939\times10^{-5}\end{pmatrix},
\qquad
M_{\rm asym} = \begin{pmatrix}0 & 8.77\times10^{-5}\\ -8.77\times10^{-5} & 0\end{pmatrix}.
$$
The antisymmetric part is nonzero — but it is the **same order of magnitude** as the symmetric part, not dominant. This alone (per the document's own caution) does not establish anything; it only licenses the next test.

---

## 5. The preservation test — decisive, and it fails

For $J=\begin{pmatrix}0&1\\-1&0\end{pmatrix}$ (the standard symplectic form), genuine preservation requires $M^TJM=J$ exactly. Computed directly:
$$
M^TJM = \begin{pmatrix}\sim10^{-23} & -1.70\times10^{-7}\\ 1.70\times10^{-7} & \sim10^{-24}\end{pmatrix}, \qquad \max|M^TJM - J| = 1.0000.
$$
This is not a near-miss — $M^TJM$ is essentially the **zero matrix**, off by the full magnitude of $J$ itself. The reason is direct: $\det(M) \approx -4\times10^{-8} \approx 0$, whereas symplectic preservation in 2D requires $\det(M)=1$ exactly. $M$ is a strong **contraction** (both estimated eigenvalues near zero) — the ensemble-averaged dynamics damps $(Q,P)$ toward the origin rather than rotating or shearing them in an area-preserving way. This is the opposite of symplectic behavior, not merely its absence.

---

## 6. Why this happened, structurally

The linear regression estimates the *mean* drift of $(Q,P)$ conditional on their current values. Because $Q_n,P_n$ are themselves accumulated sums of many independent, zero-mean random phase kicks, their own magnitudes grow diffusively ($\sim\sqrt n$) while any systematic *restoring* dependence on $(Q,P)$ is weak — the fitted $M$ is small because the process is close to an unbiased random walk, not because of a delicate near-cancellation of a true symplectic structure. A genuine Hamiltonian oscillator would show $M$ with real eigenvalues equal in magnitude and opposite in sign to leading order (a rotation-like structure with $\det M=1$); what was found instead is a weak, near-singular contraction — qualitatively different, not just quantitatively short of the target.

---

## 7. Audit

| Test | Result |
|---|---|
| $(Q,P)$ non-monotonic | **Confirmed** (near 50/50 sign splits, unlike TN-08's $R_n$) |
| Oriented area $A_N$ | Computed, nonzero, but **not interpretable alone** as evidence of structure |
| $M_{\rm asym}\neq0$ | **True**, but same order as $M_{\rm sym}$ — not dominant |
| Preservation $M^TJM=J$ | **Fails outright** — $\max$ deviation $=1.0$, the full scale of $J$ |
| $\det(M)=1$ (required for 2D symplectic map) | **Fails** — $\det(M)\approx0$ |
| Qualitative character of $M$ | Weak contraction (diffusive/dissipative-looking), not rotation-like |

---

## 8. Conclusion

This is a clean, decisive negative result for the specific construction tested, not an inconclusive one. The stopping rule set out in advance — correlation $\neq$ symplecticity, nonzero antisymmetry $\neq \omega_\Phi$ — is honored: a nonzero $M_{\rm asym}$ was found and explicitly not treated as sufficient. The actual preservation criterion, $M^TJM=J$, was tested directly and fails by the largest margin possible for a $2\times2$ system (order-unity deviation against order-unity $J$), for a structural reason (the estimated dynamics is a near-singular contraction, not a rotation) rather than a marginal near-miss that more data might close.

This does not close off the broader question — a different observable construction, a different growth model (beyond plain transitive percolation), or examining individual histories rather than only the ensemble-averaged operator, could behave differently. But for the specific, UPT-motivated holonomy-based $(Q,P)$ pair and the specific causal growth model used throughout TN-07–TN-09, causal growth does not generate symplectic dynamics for phase observables built this way. That is a real, falsifiable result, obtained by doing the calculation the document specified rather than a weaker proxy for it.

---

## Provenance note

This note implements the TN-09 experiment proposed in a subsequent joint review: paired non-monotonic phase observables derived from holonomy-type structure on the sequentially growing causal set, with the ensemble transition operator estimated by linear regression across 40 independent realizations and tested directly against the symplectic preservation criterion $M^TJM=J$. All quantitative results were computed directly. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
