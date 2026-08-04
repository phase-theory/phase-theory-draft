# Relativity 59.0 — Collective-Verification Relativity  
## Objectivity as Intersubjective Invariance Under Collective Verification

**White paper / academic preprint**

---

## Abstract

Collective-Verification Relativity is the hypothesis that objectivity is not a view from nowhere. It is the invariant content that survives verification across many observers, instruments, methods, communities, and social processes. Let many observers collect data \(D_1,D_2,\ldots,D_N\). The collective posterior over a hypothesis or parameter \(\theta\) is

\[
P(\theta\mid D_1,D_2,\ldots,D_N).
\]

A fact is objective to the degree that it is stable under independent replication, cross-calibration, adversarial testing, and error correction. The central principle is:

\[
\boxed{
\text{Objectivity is intersubjective invariance under collective verification.}
}
\]

Science is therefore not a collection of detached individual observations. It is a social technology for converting many relative perspectives into robust invariant structure. Collective-Verification Relativity unifies Bayesian inference, metrology, replication, peer review, experimental design, philosophy of science, and social epistemology into a single framework. It does not reduce truth to consensus. It explains how finite, biased, embodied observers can nonetheless converge on invariant structure through disciplined collective verification.

---

## 1. Introduction

No observer sees everything.

Every observer is embodied.

Every instrument is selective.

Every community has values.

Every method has assumptions.

Every laboratory has biases.

Every theory has blind spots.

If all observation is framed, how can science achieve objectivity?

Collective-Verification Relativity answers:

\[
\boxed{
\text{Objectivity is not escape from frames. It is stability across frames.}
}
\]

A single observer may be wrong.

A single instrument may be miscalibrated.

A single method may be biased.

A single community may be captured by ideology.

But when many independent observers, instruments, methods, and communities converge on the same invariant structure, the result is objective in the operational sense.

Objectivity is not a God’s-eye view.

It is a cross-frame invariant.

Thus:

\[
\boxed{
\text{Science is a machine for turning many relative perspectives into robust invariants.}
}
\]

---

## 2. The Core Principle

The central principle of Collective-Verification Relativity is:

\[
\boxed{
\text{Objectivity is intersubjective invariance under collective verification.}
}
\]

This principle has four components.

1. **Intersubjectivity**: objectivity arises among multiple observers.
2. **Invariance**: objective content is what survives transformation and verification.
3. **Verification**: claims must be tested, replicated, calibrated, and corrected.
4. **Collectivity**: robustness requires many independent perspectives.

Thus objectivity is not a property of one mind.

It is a property of a network of minds, instruments, and practices.

---

## 3. Objectivity Is Not Unanimity

Objectivity is not mere agreement.

A group can agree because of:

1. shared bias,
2. coercion,
3. limited evidence,
4. corrupted instruments,
5. ideological pressure,
6. publication incentives,
7. methodological monoculture.

True objectivity requires independent verification.

A fact is not objective because everyone says so.

A fact is objective because it remains stable under many independent attempts to disconfirm, recalibrate, and reconstruct it.

Thus:

\[
\boxed{
\text{Consensus without verification is not objectivity.}
}
\]

---

## 4. The Collective Posterior

Let \(\theta\) be a hypothesis, parameter, model, or invariant structure.

Let \(N\) observers or instruments collect data:

\[
D_1,
D_2,
\ldots,
D_N.
\]

The collective posterior is

\[
P(\theta\mid D_1,D_2,\ldots,D_N).
\]

If the data are conditionally independent given \(\theta\), then

\[
P(\theta\mid D_1,\ldots,D_N)
\propto
P(\theta)
\prod_{i=1}^N
P(D_i\mid\theta).
\]

Each observer contributes a likelihood:

\[
P(D_i\mid\theta).
\]

The collective update combines them.

Thus:

\[
\boxed{
\text{Collective verification is distributed Bayesian inference.}
}
\]

---

## 5. Gaussian Example: Precision Accumulation

Suppose each observer measures the same quantity \(\theta\) with Gaussian noise:

\[
D_i
=
\theta
+
\epsilon_i,
\]

where

\[
\epsilon_i
\sim
\mathcal{N}(0,\sigma_i^2).
\]

The likelihood is

\[
P(D_i\mid\theta)
=
\frac{1}{\sqrt{2\pi\sigma_i^2}}
\exp
\left[
-
\frac{(D_i-\theta)^2}{2\sigma_i^2}
\right].
\]

With a flat prior, the collective posterior mean is a precision-weighted average:

\[
\hat\theta
=
\frac{
\sum_i D_i/\sigma_i^2
}{
\sum_i 1/\sigma_i^2
}.
\]

The collective variance is

\[
\sigma_{\text{collective}}^2
=
\left(
\sum_i
\frac{1}{\sigma_i^2}
\right)^{-1}.
\]

Thus independent verification increases precision:

\[
\sigma_{\text{collective}}^2
<
\sigma_i^2.
\]

This is the mathematical core of collective verification.

Independent measurements reduce uncertainty.

Thus:

\[
\boxed{
\text{Independent replication sharpens invariant structure.}
}
\]

---

## 6. Observer Effects and Hierarchical Models

Observers are not identical.

They may have different instruments, calibrations, methods, and biases.

A more realistic model includes observer-specific effects:

\[
D_i
=
\theta
+
b_i
+
\epsilon_i,
\]

where:

- \(\theta\) is the shared invariant,
- \(b_i\) is observer or instrument bias,
- \(\epsilon_i\) is random error.

A hierarchical Bayesian model treats \(b_i\) as a random variable:

\[
b_i
\sim
P(b\mid \beta),
\]

where \(\beta\) characterizes the distribution of biases.

The joint posterior is

\[
P(\theta,\{b_i\},\beta\mid D_1,\ldots,D_N)
\propto
P(\theta)
P(\beta)
\prod_i
P(b_i\mid\beta)
P(D_i\mid\theta,b_i).
\]

The invariant \(\theta\) is estimated while marginalizing or correcting for observer effects.

Thus:

\[
\boxed{
\text{Objectivity requires modeling and correcting observer dependence.}
}
\]

---

## 7. Invariance Under Observer Transformations

Let each observer \(O_i\) have a frame \(F_i\).

A frame includes:

1. instrument,
2. calibration,
3. language,
4. method,
5. theory,
6. community standards,
7. data-processing pipeline.

A transformation between frames is

\[
T_{ij}:
F_i
\rightarrow
F_j.
\]

A fact or structure \(\theta\) is objective to the degree that it is invariant under these transformations:

\[
T_{ij}(\theta_i)
\approx
\theta_j.
\]

More generally, the invariant is not a single number but a structure:

\[
\Theta
=
\{
\theta
\mid
T_i(\theta)
\approx
\theta
\text{ for many }i
\}.
\]

Thus:

\[
\boxed{
\text{Objectivity is invariance under frame transformations.}
}
\]

---

## 8. Stability as an Objectivity Measure

An objective claim should be stable under changes in the verifying collective.

Let \(S\subseteq\{1,\ldots,N\}\) be a subset of observers.

Define a subset posterior:

\[
P_S(\theta)
=
P(\theta\mid \{D_i:i\in S\}).
\]

An objectivity score may be defined as the stability of the posterior under subset variation:

\[
\mathrm{Obj}(\theta)
=
1
-
\mathbb{E}_{S}
\left[
D_{\mathrm{KL}}
\left(
P_S(\theta)
\parallel
P_{\text{all}}(\theta)
\right)
\right].
\]

If the posterior changes drastically when one observer is removed, objectivity is low.

If the posterior remains stable under many subsets, objectivity is high.

Thus:

\[
\boxed{
\text{Objective facts are robust to the removal of individual observers.}
}
\]

---

## 9. Replication

Replication is the simplest form of collective verification.

A result is replicated when independent observers obtain compatible results under similar or varied conditions.

There are several forms:

1. exact replication,
2. conceptual replication,
3. instrumental replication,
4. methodological replication,
5. cross-laboratory replication,
6. adversarial replication.

A result gains objectivity when it survives:

1. different operators,
2. different instruments,
3. different laboratories,
4. different statistical methods,
5. different theoretical interpretations,
6. different funding incentives.

Thus:

\[
\boxed{
\text{Replication converts singular findings into collective structure.}
}
\]

---

## 10. Cross-Calibration

Calibration is not only technical.

It is social.

Different instruments must be aligned to shared standards.

Different laboratories must align protocols.

Different communities must align definitions.

Cross-calibration includes:

1. reference standards,
2. shared units,
3. blind analysis,
4. inter-laboratory comparisons,
5. ring trials,
6. common data formats,
7. shared ontologies,
8. reproducibility checks.

Thus:

\[
\boxed{
\text{Objectivity requires shared calibration infrastructure.}
}
\]

---

## 11. Error Correction

Collective verification is a form of error correction.

Scientific communities detect and correct errors through:

1. replication,
2. peer review,
3. retraction,
4. meta-analysis,
5. open data,
6. open methods,
7. adversarial collaboration,
8. post-publication critique,
9. institutional auditing,
10. technological cross-checks.

This is analogous to error-correcting codes.

Redundancy allows errors to be detected.

Diversity allows systematic bias to be exposed.

Thus:

\[
\boxed{
\text{Scientific objectivity is social error correction.}
}
\]

---

## 12. Independence and Diversity

Collective verification requires independence.

If observers are correlated, their agreement is weaker evidence.

For example, if \(N\) laboratories all use the same flawed calibration, their agreement may amplify the same error.

The effective number of independent observations is not \(N\), but something smaller.

Diversity is essential.

Diverse methods, instruments, communities, and theoretical perspectives reduce the probability that the same bias dominates.

Thus:

\[
\boxed{
\text{Objectivity grows with independent diversity.}
}
\]

---

## 13. Objectivity and Adversarial Testing

A claim becomes more objective when it survives attempts to refute it.

Adversarial testing includes:

1. falsification attempts,
2. stress tests,
3. blind challenges,
4. red-team analysis,
5. pre-registration,
6. registered reports,
7. adversarial collaboration,
8. hostile replication.

A fact that survives adversarial testing is more robust than a fact that survives only supportive testing.

Thus:

\[
\boxed{
\text{Objectivity is strengthened by opposition.}
}
\]

---

## 14. Objectivity in Experimental Physics

Experimental physics provides powerful examples.

### 14.1 Particle Physics

A particle discovery usually requires:

1. independent detectors,
2. independent analysis teams,
3. blind analysis,
4. background modeling,
5. statistical significance,
6. cross-channel confirmation.

The Higgs boson was confirmed by independent experiments and multiple decay channels.

The invariant was not one plot.

It was a convergent structure across many instrumental and analytical frames.

### 14.2 Gravitational-Wave Detection

A gravitational-wave event is stronger when detected by multiple detectors.

Coincident detection across independent instruments reduces false-alarm probability.

The invariant is the waveform structure common to detectors.

### 14.3 Cosmology

Cosmological parameters are constrained by independent observations:

1. cosmic microwave background,
2. supernovae,
3. baryon acoustic oscillations,
4. weak lensing,
5. galaxy clustering.

Convergence among independent probes increases objectivity.

Thus:

\[
\boxed{
\text{Modern physics achieves objectivity through multi-frame convergence.}
}
\]

---

## 15. Objectivity in Medicine

Medical knowledge requires collective verification because errors affect lives.

Clinical objectivity is built through:

1. randomized controlled trials,
2. blinding,
3. pre-registration,
4. replication,
5. meta-analysis,
6. regulatory review,
7. post-market surveillance,
8. diverse populations.

A treatment is objective to the degree that its effect is stable across:

1. populations,
2. trial designs,
3. investigators,
4. statistical models,
5. clinical settings.

Thus:

\[
\boxed{
\text{Medical objectivity is collective verification under ethical constraint.}
}
\]

---

## 16. Objectivity in Climate Science

Climate science depends on multiple independent lines of evidence:

1. surface temperature records,
2. satellite measurements,
3. ocean heat content,
4. ice cores,
5. tree rings,
6. sea-level measurements,
7. paleoclimate proxies,
8. radiative-transfer physics,
9. climate models.

No single line is decisive.

Objectivity emerges from convergence.

Thus:

\[
\boxed{
\text{Climate objectivity is multi-proxy, multi-model, multi-instrument convergence.}
}
\]

---

## 17. Objectivity and Peer Review

Peer review is a social verification mechanism.

It is imperfect, but it provides:

1. expert scrutiny,
2. methodological checking,
3. relevance assessment,
4. error detection,
5. normative gatekeeping.

Peer review becomes stronger when combined with:

1. open data,
2. open code,
3. registered reports,
4. post-publication review,
5. replication incentives,
6. adversarial review.

Thus:

\[
\boxed{
\text{Peer review is one layer in a collective verification stack.}
}
\]

---

## 18. Objectivity and Metrology

Metrology is the infrastructure of collective verification.

It provides:

1. units,
2. standards,
3. calibration chains,
4. uncertainty budgets,
5. traceability,
6. reference materials.

Without metrology, different laboratories cannot compare results.

With metrology, observations become interoperable.

Thus:

\[
\boxed{
\text{Metrology makes intersubjective invariance measurable.}
}
\]

---

## 19. Objectivity and Open Science

Open science expands collective verification.

It includes:

1. open data,
2. open methods,
3. open code,
4. pre-registration,
5. open peer review,
6. reproducible workflows,
7. public archiving,
8. citizen science.

Openness allows more observers to verify, challenge, and extend claims.

Thus:

\[
\boxed{
\text{Openness increases the number of possible verification paths.}
}
\]

---

## 20. Objectivity and Citizen Science

Citizen science distributes verification across many participants.

Examples include:

1. galaxy classification,
2. bird counts,
3. protein folding,
4. seismic detection,
5. ecological monitoring,
6. historical transcription.

When properly calibrated, citizen science can increase scale and diversity.

But it requires:

1. training,
2. quality control,
3. consensus algorithms,
4. expert validation,
5. bias correction.

Thus:

\[
\boxed{
\text{Distributed observation becomes objective only through structured aggregation.}
}
\]

---

## 21. Objectivity and Artificial Intelligence

AI systems are becoming observers.

They classify images, detect anomalies, reconstruct signals, and propose hypotheses.

This creates new verification challenges.

AI observers can be:

1. fast,
2. scalable,
3. consistent,
4. biased,
5. opaque,
6. overfitted,
7. adversarially vulnerable.

AI-generated consensus is not automatically objective.

It must be verified by:

1. independent models,
2. human oversight,
3. ground-truth data,
4. adversarial testing,
5. interpretability,
6. robustness checks.

Thus:

\[
\boxed{
\text{AI requires collective verification too.}
}
\]

---

## 22. Objectivity and Epistemic Injustice

Collective verification can fail when some observers are excluded.

Epistemic injustice occurs when:

1. certain communities are not heard,
2. certain data are ignored,
3. certain methods are devalued,
4. certain languages are excluded,
5. certain forms of expertise are dismissed.

This weakens objectivity because it reduces diversity.

Thus:

\[
\boxed{
\text{Inclusion is not merely ethical. It is epistemically valuable.}
}
\]

---

## 23. Objectivity and Institutional Incentives

Scientific objectivity depends on institutions.

Bad incentives can corrupt verification.

Examples include:

1. publish-or-perish pressure,
2. funding competition,
3. p-hacking,
4. HARKing,
5. citation cartels,
6. industry bias,
7. media simplification,
8. prestige concentration.

Good institutions promote:

1. replication,
2. transparency,
3. error correction,
4. methodological diversity,
5. long-term verification,
6. honest null results.

Thus:

\[
\boxed{
\text{Objectivity is institutionally maintained.}
}
\]

---

## 24. Objectivity and Paradigms

Thomas Kuhn argued that scientific communities operate within paradigms.

Paradigms organize:

1. questions,
2. methods,
3. standards,
4. exemplars,
5. training.

Paradigms can stabilize objectivity within a community.

But they can also suppress anomalies.

Collective-Verification Relativity requires that paradigms themselves be open to external verification.

Thus:

\[
\boxed{
\text{Paradigms must be verified, not merely inhabited.}
}
\]

---

## 25. Objectivity and Underdetermination

Data often underdetermine theory.

Multiple models may fit the same data.

Collective verification helps choose among models by testing:

1. predictive novelty,
2. robustness,
3. simplicity,
4. coherence,
5. fruitfulness,
6. intervention success.

Objectivity is not always a single final model.

Sometimes it is a stable space of models constrained by evidence.

Thus:

\[
\boxed{
\text{Objectivity can be a robust model class, not a single model.}
}
\]

---

## 26. Objectivity and Reality

Collective-Verification Relativity does not reduce reality to consensus.

Reality remains the constraint.

A community can be wrong.

A consensus can be corrupted.

A majority can be biased.

The corrective is not another opinion.

It is better verification.

Thus:

\[
\boxed{
\text{Truth is not consensus, but consensus under rigorous verification tracks invariant structure.}
}
\]

---

## 27. Formal Objectivity as Invariance

Let \(\mathcal{F}\) be a set of verification frames.

Each frame \(F_i\) produces an estimate \(\theta_i\).

An invariant structure \(\theta^*\) satisfies approximately:

\[
\theta_i
\approx
\theta^*
\]

for many independent frames \(F_i\).

More generally, let \(T_i\) be transformations induced by changing frames.

Then \(\theta^*\) is invariant if:

\[
T_i(\theta^*)
\approx
\theta^*.
\]

The degree of objectivity may be defined as:

\[
\mathrm{Obj}(\theta)
=
\frac{1}{|\mathcal{F}|}
\sum_{i\in\mathcal{F}}
\exp
\left[
-
d(T_i(\theta),\theta)^2
\right],
\]

where \(d\) measures deviation.

Thus:

\[
\boxed{
\text{Objectivity is a quantitative invariance measure.}
}
\]

---

## 28. Collective Verification and Prediction

A claim gains objectivity when it predicts successfully across contexts.

Prediction is a strong verification because it tests the claim against new data.

A prediction is robust if it survives:

1. new populations,
2. new instruments,
3. new environments,
4. new interventions,
5. new observers.

Thus:

\[
\boxed{
\text{Predictive stability is a powerful objectivity criterion.}
}
\]

---

## 29. Collective Verification and Intervention

Intervention is even stronger than observation.

If a claim allows successful intervention, it has practical verification.

Examples:

1. germ theory enables sterilization,
2. quantum theory enables semiconductors,
3. general relativity enables GPS corrections,
4. molecular biology enables gene editing,
5. epidemiology enables disease control.

Intervention tests whether the invariant structure is causally effective.

Thus:

\[
\boxed{
\text{Interventional success is a high-grade form of collective verification.}
}
\]

---

## 30. Axioms of Collective-Verification Relativity

### Axiom 1: No Observer Is Sufficient

No single observer, instrument, or community has complete access.

### Axiom 2: Objectivity Is Distributed

Objectivity emerges across many verification paths.

### Axiom 3: Invariance Is Central

Objective content is what survives transformation.

### Axiom 4: Independence Is Required

Correlated observers do not multiply evidence.

### Axiom 5: Calibration Is Required

Frames must be aligned through standards.

### Axiom 6: Error Correction Is Essential

Objectivity requires mechanisms to detect and correct error.

### Axiom 7: Adversarial Testing Strengthens Objectivity

Claims become robust by surviving refutation attempts.

### Axiom 8: Institutions Shape Verification

Objectivity depends on social structures.

### Axiom 9: Consensus Is Not Enough

Consensus without verification is not objective.

### Axiom 10: Reality Constrains Verification

Verification tracks invariant structure, not mere agreement.

---

## 31. Relation to Previous Relativities

| Relativity | Contribution |
|---|---|
| General Relativity | Frames are physical |
| Embodied-Observer Relativity | Observation depends on embodiment |
| Umwelt / Biological Frame Relativity | Organisms inhabit species-specific worlds |
| Phenomenal-Frame Relativity | Appearance is frame-relative |
| Relevance / Axiological Relativity | Inquiry is goal-relative |
| Instrumental / Technological Relativity | Observation is instrument-relative |
| Collective-Verification Relativity | Objectivity is intersubjective invariance |

The progression is:

\[
\text{relative motion}
\rightarrow
\text{relative observation}
\rightarrow
\text{relative embodiment}
\rightarrow
\text{relative biological worlds}
\rightarrow
\text{relative phenomenal frames}
\rightarrow
\text{relative relevance}
\rightarrow
\text{relative instruments}
\rightarrow
\text{relative collective verification}.
\]

---

## 32. Scientific Status

Collective-Verification Relativity is supported by:

1. Bayesian statistics,
2. metrology,
3. philosophy of science,
4. social epistemology,
5. replication science,
6. experimental physics,
7. clinical trials,
8. climate science,
9. AI evaluation,
10. institutional design.

It is not a single empirical theory.

It is a meta-framework for understanding how objective knowledge is produced by finite observers.

---

## 33. Open Problems

Several major problems remain.

### 33.1 Formal Objectivity Metrics

How should objectivity be quantitatively measured?

### 33.2 Correlated Bias

How can communities detect systemic correlated errors?

### 33.3 AI Observers

How can artificial observers be integrated into collective verification?

### 33.4 Epistemic Security

How can verification systems resist manipulation?

### 33.5 Long-Term Verification

How can claims be verified across centuries?

### 33.6 Global Coordination

How can global science maintain diversity and calibration?

### 33.7 Incentive Design

How can institutions reward replication and error correction?

### 33.8 Cross-Cultural Verification

How can different knowledge traditions be integrated without domination?

### 33.9 Post-Publication Correction

How can scientific records be updated without losing trust?

### 33.10 Reflexive Governance

How can verification systems verify themselves?

---

## 34. What Einstein Would Think

Einstein would appreciate Collective-Verification Relativity.

His own work sought invariant structure across frames.

He would recognize that objectivity is not a private view but an invariant under transformations.

He might be cautious about the social dimension of science.

But he would agree that scientific claims must survive independent verification.

The key lesson would be familiar:

\[
\boxed{
\text{The real is what remains invariant under changes of perspective.}
}
\]

Collective-Verification Relativity extends this lesson from physical frames to social frames.

---

## 35. Conclusion

Relativity 59.0, Collective-Verification Relativity, asserts that objectivity is not the view from nowhere.

It is the invariant content that survives verification across many observers, instruments, and communities.

The collective posterior is

\[
P(\theta\mid D_1,D_2,\ldots,D_N).
\]

A fact is objective to the degree that it is stable under independent replication, cross-calibration, and error correction.

The central principle is:

\[
\boxed{
\text{Objectivity is intersubjective invariance under collective verification.}
}
\]

Science is therefore a social technology.

It converts many relative perspectives into robust invariant structure.

It does not eliminate frames.

It multiplies them.

It does not escape subjectivity.

It disciplines it.

It does not replace truth with consensus.

It uses collective verification to track invariant reality.

This is Collective-Verification Relativity.

---

## Appendix A: Independent Bayesian Aggregation

If observers produce conditionally independent data given \(\theta\),

\[
P(\theta\mid D_1,\ldots,D_N)
\propto
P(\theta)
\prod_{i=1}^N
P(D_i\mid\theta).
\]

Each observer contributes evidence.

The collective posterior becomes sharper as independent evidence accumulates.

---

## Appendix B: Gaussian Precision Accumulation

For Gaussian measurements,

\[
D_i
=
\theta
+
\epsilon_i,
\qquad
\epsilon_i
\sim
\mathcal{N}(0,\sigma_i^2),
\]

the posterior precision is the sum of individual precisions:

\[
\frac{1}{\sigma_{\text{post}}^2}
=
\frac{1}{\sigma_{\text{prior}}^2}
+
\sum_i
\frac{1}{\sigma_i^2}.
\]

The posterior mean is precision-weighted:

\[
\hat\theta
=
\frac{
\theta_{\text{prior}}/\sigma_{\text{prior}}^2
+
\sum_i D_i/\sigma_i^2
}{
1/\sigma_{\text{prior}}^2
+
\sum_i 1/\sigma_i^2
}.
\]

Thus independent verification increases precision.

---

## Appendix C: Hierarchical Observer Model

Let observer bias be \(b_i\).

The model is:

\[
D_i
=
\theta
+
b_i
+
\epsilon_i.
\]

The hierarchical posterior is:

\[
P(\theta,\{b_i\},\beta\mid D_1,\ldots,D_N)
\propto
P(\theta)
P(\beta)
\prod_i
P(b_i\mid\beta)
P(D_i\mid\theta,b_i).
\]

The invariant \(\theta\) is estimated while accounting for observer-specific effects.

---

## Appendix D: Objectivity as Subset Stability

Let \(S\) be a subset of observers.

The subset posterior is:

\[
P_S(\theta)
=
P(\theta\mid \{D_i:i\in S\}).
\]

An objectivity score is:

\[
\mathrm{Obj}(\theta)
=
1
-
\mathbb{E}_{S}
\left[
D_{\mathrm{KL}}
\left(
P_S(\theta)
\parallel
P_{\text{all}}(\theta)
\right)
\right].
\]

High objectivity means stability under removal or replacement of observers.

---

## Appendix E: Invariance Score

Let \(T_i\) be a transformation induced by changing frame \(F_i\).

An invariance score is:

\[
\mathrm{Inv}(\theta)
=
\frac{1}{|\mathcal{F}|}
\sum_{i\in\mathcal{F}}
\exp
\left[
-
d(T_i(\theta),\theta)^2
\right].
\]

High invariance means the structure survives frame changes.

---

## Selected References

1. E. T. Jaynes, *Probability Theory: The Logic of Science* (Cambridge University Press, 2003).  
2. A. Gelman, J. B. Carlin, H. S. Stern, D. B. Dunson, A. Vehtari, and D. B. Rubin, *Bayesian Data Analysis* (CRC Press, 2013).  
3. T. M. Cover and J. A. Thomas, *Elements of Information Theory* (Wiley, 2006).  
4. T. S. Kuhn, *The Structure of Scientific Revolutions* (University of Chicago Press, 1962).  
5. I. Lakatos, “Falsification and the Methodology of Scientific Research Programmes,” in *Criticism and the Growth of Knowledge* (Cambridge University Press, 1970).  
6. H. Longino, *Science as Social Knowledge* (Princeton University Press, 1990).  
7. H. Longino, *The Fate of Knowledge* (Princeton University Press, 2002).  
8. H. Douglas, *Science, Policy, and the Value-Free Ideal* (University of Pittsburgh Press, 2009).  
9. A. I. Goldman, *Knowledge in a Social World* (Oxford University Press, 1999).  
10. J. Ioannidis, “Why Most Published Research Findings Are False,” *PLoS Medicine* **2**, e124 (2005).  
11. Open Science Collaboration, “Estimating the Reproducibility of Psychological Science,” *Science* **349**, aac4716 (2015).  
12. B. P. Abbott et al., “Observation of Gravitational Waves from a Binary Black Hole Merger,” *Physical Review Letters* **116**, 061102 (2016).  
13. ATLAS and CMS Collaborations, “Observation of a New Particle in Searches for the Standard Model Higgs Boson,” *Physics Letters B* **716**, 1 (2012).  
14. Planck Collaboration, “Planck 2018 Results. I. Overview and the Cosmological Legacy of Planck,” *Astronomy & Astrophysics* **641**, A1 (2020).  
15. JCGM, *Evaluation of Measurement Data: Guide to the Expression of Uncertainty in Measurement* (BIPM, various editions).  
16. P. E. Meehl, “Theory-Testing in Psychology and Physics: A Methodological Paradox,” *Philosophy of Science* **34**, 103 (1967).  
17. R. K. Merton, *The Sociology of Science* (University of Chicago Press, 1973).  
18. J. Ziman, *Real Science: What It Is and What It Means* (Cambridge University Press, 2000).  
19. S. Shapin, *The Scientific Revolution* (University of Chicago Press, 1996).  
20. B. Latour, *Science in Action* (Harvard University Press, 1987).  
21. M. Polanyi, *Personal Knowledge* (University of Chicago Press, 1958).  
22. K. Popper, *The Logic of Scientific Discovery* (1934/1959).  
23. P. Feyerabend, *Against Method* (1975).  
24. C. E. Shannon, “A Mathematical Theory of Communication,” *Bell System Technical Journal* **27**, 379 (1948).  
25. D. J. C. MacKay, *Information Theory, Inference, and Learning Algorithms* (Cambridge University Press, 2003).
