# Technical Note UPT–TN–05

## The First Topologically Nontrivial UPT Phase Sector: Four Gates, Two Passed Outright, One Passed by Citation, One Open

**Dust LLC — Universal Phase Theory Technical Note**
**August 2026**

---

## 1. Construction

Per the four-gate proposal, the topology must be an *output* of $\mathscr F[\Phi]=0$, not declared. The construction:

- **Base.** $\mathcal X = T^2$ (a torus base) — this is a genuine new stipulation, flagged as such: choosing $\mathcal X$ to have this topology is required scaffolding to allow two independent, non-contractible closed phase loops to exist at all. It is not itself derived from anything upstream.
- **Phase data.** Two independent holonomies $U_1,U_2 \in SU(2)$, the group-valued edge data of the round-1 discrete candidate (chosen non-Abelian here, since $U(1)$ plaquette holonomy is a single circle with no room for a nontrivial 2-cycle — the $U(1)$ case tested in TN-03/04 is exactly why that route was topologically trivial).
- **Admissibility.** $\mathscr F[\Phi]=0$ in the flat (zero-curvature) sector requires the plaquette holonomy $W_{12}=U_1U_2U_1^{-1}U_2^{-1}=1$, i.e. $U_1,U_2$ **commute**. This is the actual admissibility condition doing the work, not an assumption about the target space.

---

## Gate 1 — Emergent topology: $H^2(\mathcal M_\Phi;\mathbb Z)\neq0$?

Any two commuting elements of $SU(2)$ lie in a common maximal torus (standard Lie theory), so the flat-connection moduli space is
$$
\mathcal M_\Phi = (U(1)\times U(1))/W = T^2/\mathbb Z_2,
$$
where $W=\mathbb Z_2$ is the Weyl group of $SU(2)$, acting diagonally as $(\theta_1,\theta_2)\mapsto(-\theta_1,-\theta_2)$.

**This was not asserted — it was computed.** A toroidal grid was built explicitly (vertices/edges/faces, periodic), the involution was applied, and orbits were counted directly (not via the abstract orbifold formula) to get the quotient CW complex's Euler characteristic. Result, robust across grid resolutions $n=4,6,8,10,12$:
$$
\chi(T^2) = 0 \quad\text{(confirmed)}, \qquad \chi(T^2/\mathbb Z_2) = 2 \quad\text{(confirmed, all }n\text{)}.
$$
$\chi=2$ for a closed orientable surface forces genus $0$, i.e. $T^2/\mathbb Z_2 \cong S^2$ topologically — the classical "pillowcase" result, here verified directly rather than cited. Hence
$$
\boxed{H^2(\mathcal M_\Phi;\mathbb Z) = H^2(S^2;\mathbb Z) \cong \mathbb Z \neq 0.}
$$
**Gate 1: passed, and verified by direct computation**, not by choosing $\mathcal M_\Phi=S^2$ by hand — the sphere is a consequence of flatness plus $SU(2)$ commuting-pair structure.

---

## Gate 2 — Nonzero symplectic period on a 2-cycle?

The covariant phase space construction from TN-04, applied to a gauge theory on a surface, is not a new computation here — it is a well-established result in gauge theory (Atiyah–Bott 1983; foundational to Chern–Simons theory, Witten 1989): the moduli space of flat $G$-connections on a surface $\Sigma$ carries a canonical symplectic form
$$
\omega(\delta_1 A,\delta_2 A) = \int_\Sigma \operatorname{Tr}(\delta_1 A \wedge \delta_2 A),
$$
built from the Killing/trace form on $\mathfrak{su}(2)$, with **no free normalization function chosen by hand** — the form is canonical given the gauge group and the trace pairing. Restricted to the $S^2$ pillowcase, this reduces (via the standard identification of the moduli space with a coadjoint-orbit-like sphere) to a multiple of the round-sphere area form, $\omega = J\sin\theta\,d\theta\wedge d\phi$, with period $\int_{S^2}\omega = 4\pi J$.

**Gate 2: passed by direct citation of an established result**, not independently re-derived in this note. This is disclosed as a citation, not a computation performed here.

---

## Gate 3 — No arbitrary normalization: is $J$ derived, not free?

This is where the construction currently stops short of the standard set by the four-gate test.

In the Chern–Simons/Atiyah–Bott literature, $J$ (there, the level $k$) is fixed by requiring the *quantum theory* be well-defined (integrality of $k$ is not derived from something more primitive — it is precisely the prequantization condition itself, imposed as a consistency requirement, not obtained independently of it). Whether $J$ can instead be fixed *before* imposing integrality — by identifying it with the plaquette coupling $\kappa_\Phi$ already present in the round-1 discrete candidate's action $\mathcal S_{\rm grad}+\mathcal S_{\rm int}$ — has **not been shown here**. Doing so would require an explicit derivation connecting the discrete Wilson-action coupling to the continuum Atiyah–Bott normalization, which is a real, nontrivial calculation (it plausibly exists in the lattice-gauge-theory literature in some form, but was not performed or located for this note).

**Gate 3: open.** Flagging $J$ as identified with $\kappa_\Phi$ without doing this derivation would repeat exactly the TN-02 failure mode (introducing a free coefficient and calling it derived). This note does not do that.

---

## Gate 4 — Nontrivial quantization?

*Conditional* on Gate 3 being resolved, the standard result is
$$
\frac{1}{2\pi\hbar_\Phi}\int_{S^2}\omega_\Phi = \frac{2J}{\hbar_\Phi} \in \mathbb Z
\quad\Longrightarrow\quad
J = \frac{n}{2}\hbar_\Phi, \quad n\in\mathbb Z,
$$
i.e. exactly the familiar half-integer angular-momentum-type quantization from $SU(2)$ representation theory. This is a real restriction *if* $J$ is independently fixed — but as an unconditional UPT result, it inherits Gate 3's gap: without an independent fixing of $J$, this is the standard geometric-quantization statement for coadjoint orbits of $SU(2)$, true for any theory with this moduli space, not a UPT-specific prediction.

**Gate 4: conditionally passed, contingent on Gate 3.**

---

## 2. Overall verdict, honestly stated

Per the three possible outcomes named in advance:

- Not **Failure** ($H^2=0$) — ruled out by direct computation.
- Not **Topological success but dynamical failure** ($H^2\neq0$, $\int\omega=0$) — the Atiyah–Bott form is nonzero on this moduli space by construction.
- Not yet **Genuine UPT success** — that requires Gate 3, which is unresolved.

The honest description of where this note leaves things: **the candidate phase geometry possesses a moduli space with the correct topology and a canonical (non-arbitrary, in the gauge-theory sense) symplectic structure with nonzero period — but whether the resulting quantization condition is a *consequence* of the specific UPT action rather than an *input* to it remains open.** This is exactly the caution the proposing document itself asked for: not to conflate a topologically genuine result with a fully derived one.

---

## 3. Audit

| Gate | Result | Basis |
|---|---|---|
| 1. $H^2(\mathcal M_\Phi)\neq0$ | **Passed** | Direct simplicial computation ($\chi=2$ confirmed across 5 grid sizes) |
| 2. $\int_{\Sigma_2}\omega_\Phi\neq0$ | **Passed** | Cited (Atiyah–Bott 1983) — not independently re-derived here |
| 3. $J$ derived, not free | **Open** | No derivation connecting $\kappa_\Phi$ to the Atiyah–Bott normalization was performed or located |
| 4. Nontrivial quantization | **Conditionally passed** | True *if* Gate 3 resolves; otherwise a generic $SU(2)$ geometric-quantization fact, not UPT-specific |
| $\mathcal X=T^2$ | Flagged as new stipulation | Required scaffolding for two independent loops to exist; not derived |

---

## 4. Conclusion

This is the first construction in the thread where topology genuinely comes out of the admissibility condition rather than being assumed, and it does so on a real, verified computation (Gate 1) rather than a citation. That is a substantive, if narrow, advance over every prior toy model, all of which had $H^2=0$ and could not exercise the prequantization condition at all. But the note stops exactly where the honesty standard set by TN-02 requires it to stop: Gate 3 is the actual UPT-specific claim, and it has not been established. Closing it — deriving $J$ from $\kappa_\Phi$ and the discrete action, rather than from the Chern–Simons literature's own consistency requirement — is the concrete next task, and it is a real calculation, not a rhetorical one.

---

## Provenance note

This note responds to the UPT-TN-05 proposal in a subsequent joint review, constructing the first topologically nontrivial UPT candidate ($SU(2)$ flat connections on $T^2$) rather than declaring $\mathcal M_\Phi=S^2$ by hand. The $T^2/\mathbb Z_2\cong S^2$ (pillowcase) identification was verified directly via simplicial Euler-characteristic computation rather than asserted; the Atiyah–Bott symplectic form and its role in Chern–Simons level quantization are cited from established gauge theory (Atiyah–Bott 1983; Witten 1989), not re-derived. Written entirely within the UPT datum; supersedes any Phase Theory framing per current programme direction.
