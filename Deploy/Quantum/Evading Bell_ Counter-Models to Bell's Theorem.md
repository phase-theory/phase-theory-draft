# Evading Bell: The Logical Anatomy of Bell's Theorem and the Constructive Counter-Models That Reproduce Quantum Correlations

**White Paper — Dust LLC**

---

## Abstract

Bell's theorem is a mathematical result: any theory satisfying a specific set of premises (local causality, measurement independence, single definite outcomes) obeys inequalities that quantum mechanics violates. A theorem has no counterexample in the strict sense. It can, however, be *evaded* by models that deny a premise while still reproducing the quantum predictions. This paper (1) states the theorem and its premises precisely, (2) reviews the experimental record, (3) catalogues the explicit counter-models by the premise each one relaxes, (4) works through one fully explicit model (the Toner–Bacon protocol), (5) analyses claimed "refutations" of the theorem that fail, and (6) proposes a checklist any claimed counterexample must pass. The central thesis: **a legitimate "counterexample to Bell" is always a model that names the premise it gives up and pays that price openly.**

---

## 1. The Theorem

### 1.1 Setup

Two parties, Alice and Bob, receive spatially separated halves of a source. Alice chooses setting *a* ∈ {a, a′}, Bob chooses *b* ∈ {b, b′}. Outcomes are *A, B* ∈ {+1, −1}. The observable data are the conditional probabilities P(A, B | a, b).

### 1.2 Premises

A hidden-variable model introduces a variable λ with distribution ρ(λ) and writes

P(A, B | a, b) = ∫ dλ ρ(λ) P(A | a, b, λ) P(B | a, b, λ).

Bell's derivation requires:

- **P1. Factorisation (local causality).** P(A | a, b, λ) = P(A | a, λ) and P(B | a, b, λ) = P(B | b, λ). Alice's outcome does not depend on Bob's setting, and vice versa, once λ is given.
- **P2. Measurement independence (statistical independence).** ρ(λ | a, b) = ρ(λ). The hidden variable is uncorrelated with the choice of settings.
- **P3. Outcome definiteness.** Each measurement has one actual outcome, representable as a value (or probability) assigned given λ and the setting.
- **P4. Single, forward-causal ordering.** Settings are chosen after λ is fixed, and λ is not influenced by the later settings.

(P4 is usually folded into P2; it is separated here because retrocausal models attack it specifically.)

### 1.3 The CHSH form

Define E(a,b) = ⟨AB⟩ and

S = E(a,b) + E(a,b′) + E(a′,b) − E(a′,b′).

Under P1–P4, every λ gives a value A(a,λ)\[B(b,λ) + B(b′,λ)\] + A(a′,λ)\[B(b,λ) − B(b′,λ)\] = ±2, since one bracket is 0 and the other ±2. Averaging gives

**|S| ≤ 2** (the local bound).

Quantum mechanics, for the singlet state with E(a,b) = −a·b, reaches **|S| = 2√2 ≈ 2.828** (Tsirelson's bound). The no-signalling maximum is **|S| = 4** (the Popescu–Rohrlich box).

### 1.4 The logical form

Bell's theorem is the implication

P1 ∧ P2 ∧ P3 ∧ P4 ⟹ |S| ≤ 2.

Observing |S| > 2 therefore establishes only ¬(P1 ∧ P2 ∧ P3 ∧ P4): *at least one premise is false*. It does not say which. Every legitimate counter-model chooses one.

---

## 2. Experimental Status

Tests of the inequality violation have progressively closed loopholes:

- **Detection loophole** (low detector efficiency lets a local model fake the violation by selective detection): closed in ion and photon experiments.
- **Locality / light-cone loophole** (settings and outcomes not spacelike separated): closed in the 2015 Delft NV-centre experiment and contemporaneous photonic experiments (NIST, Vienna).
- **Freedom-of-choice loophole** (settings correlated with λ): constrained, not eliminated, by using distant-quasar and human-generated random settings (e.g. cosmic Bell tests, the 2016–2018 experiments and the BIG Bell Test). These push any conspiracy of correlation back in time to the emission of the quasar light (billions of years) but cannot logically exclude a pre-existing correlation.

Conclusion: the quantum prediction S > 2 is empirically established. At least one of P1–P4 fails in nature. The open question is *which*.

---

## 3. Counter-Models by Premise Relaxed

### 3.1 Relaxing P1: nonlocal hidden variables

**Bohmian mechanics (de Broglie–Bohm).** Particles have definite positions guided by a universal wavefunction. The velocity of one particle depends instantaneously on the configuration of the other. It reproduces all quantum predictions, so it is a valid model of the quantum correlations. It violates P1 and requires a preferred foliation (or an equivalent structure) to define "instantaneously," yet it is operationally no-signalling because of quantum equilibrium.

**Toner–Bacon communication models.** Singlet correlations can be reproduced exactly by classical shared randomness plus **one bit** of communication from Alice to Bob (worked in Section 4). This quantifies the price of dropping P1: very little.

### 3.2 Relaxing P2: superdeterminism

If λ is correlated with the settings, ρ(λ | a, b) ≠ ρ(λ), the inequality derivation fails. A superdeterministic model must specify a mechanism (e.g. 't Hooft's cellular-automaton interpretation; Hossenfelder–Palmer's formulation with a constrained state space). Its cost is conceptual: experimenters' choices and particle states share a common cause, which many consider to undercut the epistemology of experiment. Its virtue is that it is local and fully deterministic. Whether it makes distinct testable predictions is an active research question.

### 3.3 Relaxing P3: no single outcome

**Everett / many-worlds.** All outcomes occur; "the" outcome of a measurement is branch-relative. Locality is retained because correlations arise only when branches are compared (the comparison event is local). Bell's theorem's P3 does not hold in the form required, so the inequality is not derivable. The cost is ontological: a branching universal wavefunction and the problem of recovering probabilities (the Born rule).

### 3.4 Relaxing P4: retrocausal and time-symmetric models

If the settings can influence the hidden variable through a backward-in-time link, ρ(λ | a, b) ≠ ρ(λ) but with a *causal* rather than conspiratorial explanation.

- **Transactional interpretation (Cramer):** emission and absorption "handshake" via advanced and retarded waves.
- **Price's argument; Wharton's all-at-once (Lagrangian) models:** physical systems are solved as boundary-value problems across time, not initial-value problems.
- **Two-state-vector formalism (Aharonov et al.).**

Retrocausal models are local in a spacetime-continuous sense (every influence travels along timelike or lightlike curves, forward or backward), yet they violate the *forward-only* assumption inside P4. This is the natural home for any framework in which time has non-trivial global structure, such as closed or circular time.

### 3.5 Relaxing the form of λ: contextual and measurement-dependent models

Models where the outcome function depends on the measurement context beyond the local setting (as in Hess–Philipp's time-dependent hidden-variable argument) are included here. Care is needed: such models usually reintroduce a hidden P1 or P2 violation, and the burden is on the author to show they do not.

---

## 4. A Fully Explicit Counter-Model: Toner–Bacon (2003)

**Goal:** reproduce the singlet correlation E(a,b) = −a·b exactly, for any unit vectors a, b ∈ S².

**Resources:** two shared uniformly random unit vectors λ₁, λ₂ ∈ S², and one bit of communication from Alice to Bob.

**Protocol:**

1. Alice receives setting a. She outputs **A = −sgn(a·λ₁)**.
2. Alice sends Bob one bit **c = sgn(a·λ₁) · sgn(a·λ₂)**.
3. Bob receives setting b and the bit c. He outputs **B = sgn(b·(λ₁ + c·λ₂))**.

**Result:** the joint distribution gives E(a,b) = −a·b, and each marginal is uniform on ±1. Hence |S| = 2√2.

**Interpretation:**

- It is a valid counter-model to the *conclusion* "no classical model can reproduce quantum correlations," because it reproduces them.
- It does not contradict Bell's theorem: step 2 violates P1 (Bob's output depends on Alice's setting through c).
- It shows P1 can be relaxed at a cost of exactly one bit per run for the singlet.
- The same bit is not available as a signal in the actual experiment; the model is therefore a *simulation* of the statistics, not an ontological claim. Bohmian mechanics is the claim that the nonlocal link is real.

---

## 5. Claimed Refutations That Fail

Many papers claim to "disprove" or "find a counterexample to" Bell's theorem itself. They fall into recognisable classes.

| Class | Typical claim | Where it breaks |
| --- | --- | --- |
| **Algebraic reinterpretation** | Clifford-algebra or geometric-algebra models (e.g. Christian's S³ model) reproduce −a·b locally | Averaging over a non-commuting, setting-dependent sign convention reintroduces a hidden violation of P1 or P2; the model fails when simulated event by event |
| **Detection-efficiency models** | A local model reproduces S > 2 with lossy detectors | Valid only below the critical efficiency (≈ 82.8% for CHSH with maximally entangled states); fails in loophole-free experiments |
| **Coincidence-time models** | Time-window matching creates the apparent violation | Closed by experiments with fixed, pre-defined time windows |
| **Misapplied probability** | "Bell wrongly assumes joint probabilities exist" | Bell's inequality needs only the existence of the marginal local functions, and the CHSH derivation does not assume a joint distribution for non-commuting observables |
| **Rejecting the mathematics** | The ±2 bracket argument is "invalid" | It is an elementary identity and can be checked by exhaustion over the 16 deterministic assignments |

**Lesson:** a model that matches the singlet statistics *and* simultaneously satisfies P1–P4 does not exist. A claimed one contains an error, usually an unacknowledged premise violation.

---

## 6. Admissibility Checklist for a Claimed Counter-Model

A model purporting to counter Bell's theorem should pass all of the following.

1. **Name the premise.** State which of P1–P4 (or which implicit assumption) is relaxed.
2. **Reproduce the statistics.** Give explicit P(A,B | a,b) matching quantum predictions for all four CHSH setting pairs, not only the maxima.
3. **No-signalling (or justify otherwise).** Show that marginals at one wing are independent of the other wing's setting, or state explicitly that signalling is permitted.
4. **Event-by-event simulation.** Provide a runnable algorithm that generates individual outcomes, not only averaged correlators. Run it against the CHSH sum.
5. **State the cost.** Quantify the resource (bits of communication, degree of correlation between λ and settings, branching structure, causal-loop structure).
6. **Distinct predictions.** Identify any empirical consequence that differs from standard quantum mechanics, or state that none exists (making it an interpretation).
7. **Consistency with Tsirelson's bound.** If the model exceeds 2√2, it must say why (it is then not quantum mechanics).

---

## 7. Discussion

The landscape of Bell-evading models is best read as a table of *prices*:

| Model family | Premise given up | Price |
| --- | --- | --- |
| Bohmian mechanics | P1 | Preferred frame; instantaneous configuration-space dependence |
| Toner–Bacon | P1 | One bit of communication per singlet |
| Superdeterminism | P2 | Common-cause correlation between settings and states |
| Many-worlds | P3 | Branching ontology; derivation of Born probabilities |
| Retrocausal / time-symmetric | P4 | Backward-in-time influence; boundary-value dynamics |

For researchers developing frameworks with unconventional temporal structure (circular time, bidirectional action, closed timelike structure), the retrocausal row is the relevant one. Such a framework counters Bell's *conclusion* precisely when it (a) is explicit about its boundary conditions across time, (b) is consistent with no-signalling at the operational level, and (c) passes Section 6.

---

## 8. Conclusion

There is no counterexample to Bell's theorem as a mathematical statement. There are, however, well-defined and fully consistent models that reproduce the quantum correlations by giving up one of its premises. The productive research question is not "is Bell wrong?" but "**which premise does nature relax, and can any experiment tell the candidates apart?**" Any new model should be presented in that form: premise named, statistics reproduced, cost quantified, simulation provided.

---

## References (key sources)

1. J. S. Bell, "On the Einstein Podolsky Rosen paradox," *Physics* 1, 195 (1964).
2. J. F. Clauser, M. A. Horne, A. Shimony, R. A. Holt, *Phys. Rev. Lett.* 23, 880 (1969).
3. B. Tsirelson, *Lett. Math. Phys.* 4, 93 (1980).
4. S. Popescu, D. Rohrlich, *Found. Phys.* 24, 379 (1994).
5. B. F. Toner, D. Bacon, *Phys. Rev. Lett.* 91, 187904 (2003).
6. B. Hensen et al., *Nature* 526, 682 (2015) (loophole-free test, Delft).
7. D. Bohm, *Phys. Rev.* 85, 166 (1952).
8. G. 't Hooft, *The Cellular Automaton Interpretation of Quantum Mechanics* (Springer, 2016).
9. S. Hossenfelder, T. Palmer, "Rethinking superdeterminism," *Front. Phys.* 8, 139 (2020).
10. H. Price, *Time's Arrow and Archimedes' Point* (Oxford, 1996); K. Wharton, N. Argaman, *Rev. Mod. Phys.* 92, 021002 (2020).
11. J. Cramer, *Rev. Mod. Phys.* 58, 647 (1986).
12. J.-Å. Larsson, R. Gill, *Europhys. Lett.* 67, 707 (2004).