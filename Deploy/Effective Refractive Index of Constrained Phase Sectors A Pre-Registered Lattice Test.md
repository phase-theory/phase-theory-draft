# Effective Refractive Index of Constrained Phase Sectors: A Pre-Registered Lattice Test

Oct 25, 2026 · @Marlon Hanks

## Purpose and scope

This note pre-registers a lattice test of whether confining a gauge sector between boundaries shifts its effective light-cone slope, and in which direction. The quantity measured is n = c\_ref / c\_region, where both speeds come from the same bare couplings and only the geometry differs.

Status: auxiliary and standalone. It is not a numbered TN, does not alter the Phase I baseline (TN-10, TN-18, Closure Report), and does not open Phase II. Any result enters the ledger only through the five questions below.

It does not claim a sub-vacuum medium exists. It tests the one case in standard physics with a computed sign, the Casimir/Scharnhorst shift, in the discrete Wilson-action setting UPT already uses.

## Claim ledger

The test adds no postulate, and only its last stage can carry UPT-specific evidence.

| Question | Answer |
| --- | --- |
| Postulate | None added. Uses the TN-06/TN-13 Wilson action (β = 2N/g₀² convention) unchanged, plus a boundary condition. |
| Inevitable consequence | The classical limit of the anisotropic Wilson action gives c² = β\_s/β\_t in lattice units. This is standard lattice gauge theory, not a UPT result. |
| Falsifiability | Four hypotheses H0–H3 with thresholds fixed before any run (see Pre-registered hypotheses). |
| Remaining freedom | Gauge group, β, β\_t/β\_s, plate separation L, transverse size, plate implementation. Sweeps allowed; none tuned to a target n. |
| UPT-specificity | Stages A–C are generic lattice gauge theory, the same status as TN-04. Only Stage D (DAG substrate) can be UPT-specific, and it is conditional on DAG regularity, still open per TN-13 and TN-14. |

## Setup

The anisotropic Wilson action splits plaquettes into spatial and temporal classes, and the ratio of their couplings sets the lattice light-cone slope.

```latex
S = \beta_s \sum_{P\in\text{spatial}} \Big(1-\tfrac{1}{N}\,\mathrm{Re\,tr}\,U_P\Big) + \beta_t \sum_{P\in\text{temporal}} \Big(1-\tfrac{1}{N}\,\mathrm{Re\,tr}\,U_P\Big)
```

```latex
\varepsilon \leftrightarrow \beta_t,\qquad \frac{1}{\mu}\leftrightarrow \beta_s,\qquad c_{\rm lat}^2=\frac{\beta_s}{\beta_t},\qquad n=\frac{c_{\rm ref}}{c_{\rm region}}
```

The relation c\_lat² = β\_s/β\_t is tree-level. Quantum corrections renormalize the anisotropy, so the observable is the measured c\_lat, never the bare ratio. The reference speed c\_ref is measured directly in unbounded runs at the same couplings.

Two distinct questions hide under "sub-vacuum phase":

- **Bare sub-vacuum:** a sector with a different β\_t/β\_s. UPT admits a family of these and, per TN-18, selects none.
- **Induced sub-vacuum:** the same bare couplings, with a constraint (plates) shifting the effective index. This note tests only this case.

Open issue: β\_t and β\_s presuppose a time/space split of plaquettes, which a DAG does not supply. Stage D therefore needs a foliation-free observable and is not specified here.

## Stages

A matter-free sector cannot reproduce the QED Scharnhorst effect, so the stages are built to establish a null baseline first and test self-interaction second.

| Stage | System | Expected result | UPT-specific? |
| --- | --- | --- | --- |
| A | Compact U(1), unbounded and periodic, Coulomb phase (β above the bulk transition, about 1.01 for the Wilson action) | Free-photon dispersion; δ = 0 after lattice-momentum correction | No |
| B | Compact U(1), two plates (tangential boundary links frozen), separation L | Null: no vacuum polarization without charged matter, so any shift is an artifact | No |
| C | SU(2), same plates, weak coupling with L inside the string-tension scale | Gluon self-interaction may shift c\_eff; sign is the open question | No |
| D | DAG substrate with a constraint region | Not specified; needs a foliation-free observable and DAG regularity | Yes, conditional |

The Scharnhorst shift in QED comes from virtual electron-positron loops. Adding charged matter here is deliberately excluded, because TN-12 showed matter destroys rigidity in every known case. The consequence is that this note tests whether gauge self-interaction alone can do the job, which standard theory does not predict.

## Observable and protocol

The effective speed is a fit parameter of the mode spectrum, extracted from Euclidean correlators, because a Euclidean Monte Carlo cannot propagate a real-time pulse.

1. **Operators:** gauge-invariant electric-flux and plaquette operators, projected onto definite momentum along the plates (k\_∥) and mode number n across the gap.
2. **Energies:** extract E\_n(k\_∥) from correlator decay with a variational (GEVP) analysis; use lattice momenta (2/a) sin(ka/2), not continuum k.
3. **Fit:** E² = c\_eff² (k̂\_∥² + p̂\_n²), with p\_n = nπ/L\_eff. L\_eff is fitted, since frozen boundary links make the true plate separation uncertain by order one lattice spacing; the slope in k̂\_∥² gives c\_eff independent of L\_eff.
4. **Index:** δ(L) = c\_∞/c\_eff(L) − 1, with c\_∞ measured on an unbounded lattice at identical couplings. δ < 0 means c\_eff exceeds c\_∞.
5. **Geometries per coupling:** plates, periodic with the same L, and unbounded. Transverse and Euclidean-time extents at least 4L.
6. **Sizes and statistics:** L in {6, 8, 12, 16, 24} sites; blocked bootstrap for autocorrelation; all parameter values and sample counts written to a run register before the first run.

Proxy caveat: this measures dispersion along the plates in a waveguide geometry. The Scharnhorst statement concerns propagation normal to the plates, so a match here is evidence of a shift, not a reproduction of that calculation.

## Pre-registered hypotheses

Four tests, ordered so that each gates the next; thresholds are fixed here and not revised after any run.

| ID | Stage | Pass criterion | If it fails |
| --- | --- | --- | --- |
| H0 | A, B | U(1) with plates: abs(δ) within 2σ of zero at every L, after lattice-momentum correction | The observable has an uncontrolled systematic. Stop; Stage C is uninterpretable. |
| H1 | C | SU(2): δ has one resolved sign at 3σ or better for at least 3 values of L. All three outcomes (δ < 0, δ ≈ 0, δ > 0) are recorded with equal weight. | No resolved sign: report as null at the achieved precision. |
| H2 | C | Two independent plate implementations (frozen tangential links; frozen boundary plaquettes) agree on δ within 2σ | δ is a boundary-implementation artifact; no physical claim. |
| H3 | C | At fixed physical L (fixed ratio to the string-tension scale), δ is measured at 3 or more lattice spacings and extrapolates in a² to a nonzero limit | A shift that vanishes as a → 0 is a lattice artifact. |

No scaling law in L is assumed. The L⁻⁴ form of QED comes from the electron mass setting a scale, and a matter-free sector may supply none. The fitted L-dependence is reported as a result, not tested against a prediction.

## Confounders and frozen rules

Three systematics can mimic a shift, and three rules carried over from the UPT ledger govern how results are used.

**Confounders and their controls**

- **Boundary offset (L\_eff):** fitted jointly; H2 tests two plate implementations.
- **Finite volume and Euclidean time:** runs at transverse and time extents of 4L and 6L must agree within 2σ.
- **Anisotropy renormalization:** c\_∞ is measured, never inferred from β\_t/β\_s.
- **Confinement (SU(2)):** each coupling is admitted only if L is below the string-tension scale at that coupling, checked in the run register.

**Frozen rules**

1. No tuning of β, β\_t/β\_s or L to obtain n < 1. Sweeps are legitimate; target-fitting is not (TN-17 rule).
2. No new postulate or selector is added to rescue a null result (TN-18 rule).
3. A falsified or null outcome stays in the ledger at equal weight: a falsified genuine prediction is evidence about the theory.

## Interpretation of outcomes

No outcome of this test identifies a sub-vacuum medium; the strongest result is a constraint-induced n < 1 in a matter-free non-Abelian sector.

| Outcome | Ledger entry |
| --- | --- |
| H0 fails | Observable invalid. No claim made at any stage. |
| H0 passes, Stage C null | Matter-free self-interaction gives no detectable shift. Consistent with Scharnhorst needing matter loops, which TN-12 shows are incompatible with rigidity. Tension recorded, not resolved. |
| Stage C, δ > 0 with H2, H3 passed | Constraint-induced subluminal shift. No sub-vacuum behavior; recorded as a demonstrated result. |
| Stage C, δ < 0 with H2, H3 passed | First lattice evidence of constraint-induced n < 1 in SU(2). Entered as demonstrated (lattice, generic), not UPT-specific until Stage D. |

Two limits hold in every case. A fitted low-momentum speed is a dispersion property and says nothing about the signal front velocity, which is set by the high-momentum limit and the lattice cutoff. And the bare sub-vacuum question, which sector has a lower ε\_r μ\_r, stays unselected per TN-18.
