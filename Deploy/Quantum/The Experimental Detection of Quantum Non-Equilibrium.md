The Experimental Detection of Quantum Non-Equilibrium

A rigorous framework for testing departures from the Born rule, nonequilibrium quantum ensembles, and the limits of standard quantum mechanics

The central experimental problem is to determine whether a physical quantum system can exist in a state of quantum non-equilibrium: a state whose statistical distribution differs from the equilibrium distribution prescribed by ordinary quantum mechanics, potentially allowing observable deviations from the Born rule.

The correct experiment must do more than reveal an anomalous measurement, an unusual interference pattern, or an apparent violation of quantum statistics. It must identify a mathematically precise non-equilibrium hypothesis, derive a quantitative prediction that differs from standard quantum theory, control conventional sources of error, and produce a result that cannot be explained by known equilibrium physics.

There is an important distinction at the outset: quantum non-equilibrium is not a single universally defined phenomenon. In the framework of pilot-wave theory, it commonly means a nonequilibrium distribution that differs from the Born-equilibrium distribution . In other approaches, it can refer to nonthermal quantum states, nonequilibrium open-system dynamics, or deviations from standard quantum statistical predictions. These are distinct physical claims and require different experiments.

This paper develops the most direct experimental program for the first meaning—the possibility of a distribution —while establishing what an experiment could prove, what it could only constrain, and what would be required to distinguish fundamental quantum non-equilibrium from ordinary nonequilibrium physics.

Abstract

We formulate an experimental program for detecting quantum non-equilibrium, defined in the de Broglie–Bohm framework by a hidden-variable distribution that departs from the Born-equilibrium distribution . The objective is to establish whether such departures occur in nature and, if so, whether they produce measurable statistical consequences.

The central result is methodological: a valid detection requires a specified nonequilibrium model, an operationally accessible observable, and a predicted statistical deviation that survives all conventional explanations. A violation of the Born rule would establish a departure from standard quantum statistical predictions under the tested conditions, but identifying that departure specifically with pilot-wave quantum non-equilibrium would require additional model-dependent evidence.

We develop a two-track strategy. The first is a laboratory program combining precision tests of quantum probabilities, polarization measurements, interferometry, and independent controls. The second is a search for primordial nonequilibrium signatures in cosmological fluctuations, where early-universe models offer a possible mechanism for preserving deviations that may have relaxed away in ordinary laboratory systems. Both approaches are situated within existing research on nonequilibrium pilot-wave dynamics and modern Born-rule tests.

The proposed experiment is not represented as already completed, and no existing result is claimed to prove quantum non-equilibrium. The purpose is to specify the experimental conditions under which such a claim could become scientifically justified.

Keywords: quantum non-equilibrium; Born rule; pilot-wave theory; de Broglie–Bohm mechanics; quantum relaxation; hidden-variable distributions; interferometry; cosmological perturbations; statistical model selection.

1. The precise question to be tested

The phrase quantum non-equilibrium must be defined before an experiment can test it.

Let denote the quantum state of a system, with representing its configuration variables. In standard quantum mechanics, the probability density for a position measurement is

P_{\mathrm{B}}(q,t)=|\Psi(q,t)|^2,

where the wavefunction is normalized:

\int_{\Omega}|\Psi(q,t)|^2\,dq=1.

In pilot-wave theory, the configuration has an actual trajectory guided by the wavefunction. An ensemble of configurations can be described by a distribution , normalized as

\int_{\Omega}\rho(q,t)\,dq=1.

Quantum equilibrium is the condition

\rho(q,t)=|\Psi(q,t)|^2.

Quantum non-equilibrium is therefore defined by

\boxed{\rho(q,t)\neq|\Psi(q,t)|^2}

on a set of nonzero measure.

This is a statement about an underlying ensemble distribution, not merely about whether a system is hot, driven, entangled, far from thermal equilibrium, or in a coherent superposition.

1.1 Three hypotheses that must not be conflated

Hypothesis : Standard quantum statistics

P(a\mid\psi,M)=\langle\psi|\Pi_a|\psi\rangle

All tested outcomes follow the Born rule for the specified preparation and measurement.

Hypothesis : Operational statistical deviation

P_{\mathrm{obs}}(a\mid\psi,M)\neq\langle\psi|\Pi_a|\psi\rangle

A reproducible discrepancy exists after calibration, background subtraction, and statistical correction.

Hypothesis : Pilot-wave quantum non-equilibrium

\rho(q,t)\neq|\Psi(q,t)|^2

An underlying distribution differs from quantum equilibrium and quantitatively accounts for the observed discrepancy through a specified dynamical model.

These hypotheses have different evidential requirements.

Rejecting does not automatically establish . A Born-rule discrepancy could arise from an incorrect quantum-state reconstruction, detector bias, unmodelled environmental dynamics, or genuinely new physics unrelated to pilot-wave theory.

Conversely, a nonequilibrium distribution in hidden-variable space need not produce a detectable deviation in every measurement. The measurement interaction may fail to reveal the relevant degrees of freedom, or the observable may be insensitive to the deviation.

The correct experiment must therefore test the statistical predictions of a specified nonequilibrium model rather than assume that every unusual quantum phenomenon is evidence of non-equilibrium.

2. Mathematical foundation

2.1 Guidance dynamics

For a nonrelativistic particle of mass in a potential , let the wavefunction obey the Schrödinger equation

i\hbar\frac{\partial\Psi}{\partial t}

\left(-\frac{\hbar^2}{2m}\nabla^2+V\right)\Psi.

Writing

\Psi=R e^{iS/\hbar},

with , gives the pilot-wave guidance law

\frac{dQ}{dt}

v^\Psi(Q,t),
\qquad
v^\Psi=\frac{\nabla S}{m}.

Equivalently, wherever ,

v^\Psi

\frac{\hbar}{m}
\operatorname{Im}\left(\frac{\nabla\Psi}{\Psi}\right).

The associated probability current is

J^\Psi

\frac{\hbar}{m}
\operatorname{Im}(\Psi^*\nabla\Psi).

The Schrödinger equation implies the continuity equation

\frac{\partial |\Psi|^2}{\partial t}
+
\nabla\cdot J^\Psi=0.

Since , this becomes

\frac{\partial |\Psi|^2}{\partial t}
+
\nabla\cdot\left(|\Psi|^2v^\Psi\right)=0.

An ensemble of guided configurations transported by the same velocity field satisfies

\frac{\partial\rho}{\partial t}
+
\nabla\cdot(\rho v^\Psi)=0.

The two distributions therefore obey continuity equations with the same velocity field.

2.2 The nonequilibrium invariant

Where , define

f(q,t)=\frac{\rho(q,t)}{|\Psi(q,t)|^2}.

Combining the two continuity equations yields

\boxed{
\frac{\partial f}{\partial t}
+
v^\Psi\cdot\nabla f=0
}

or, along a trajectory ,

\boxed{\frac{df(Q(t),t)}{dt}=0.}

This is an important structural result. The fine-grained ratio is conserved along the pilot-wave trajectories.

Consequently, a nonuniform initial ratio cannot simply disappear at the fine-grained level under this dynamics. Apparent relaxation toward equilibrium can instead arise through filamentation and mixing, followed by coarse-graining. The distinction between fine-grained conservation and coarse-grained relaxation is central to the proposed experimental program.

2.3 A quantitative measure of non-equilibrium

A useful distance between the two distributions is the total-variation distance

D_{\mathrm{TV}}(\rho,P_{\mathrm B})

\frac12\int_{\Omega}
\left|\rho(q)-P_{\mathrm B}(q)\right|\,dq.

It satisfies

0\leq D_{\mathrm{TV}}\leq1,

with if and only if the distributions agree almost everywhere.

For a measurable region ,

\left|
\int_A\rho\,dq-
\int_A P_{\mathrm B}\,dq
\right|
\leq D_{\mathrm{TV}}.

Thus, if the underlying configuration distribution could be operationally sampled, total variation would quantify the largest possible difference in event probability between the two distributions.

However, this inequality does not establish that an ordinary quantum measurement directly samples the hidden configuration. That mapping must be derived from the actual measurement interaction.

3. What would count as experimental proof?

No finite experiment proves an unrestricted universal statement with mathematical certainty. Experimental evidence can, however, establish a robust and reproducible violation of a precisely specified null hypothesis, with quantified uncertainty and independently replicated results.

For the present problem, a compelling detection would require five conditions:

* A precise null model. The standard quantum predictions, detector response, and allowed systematic uncertainties are specified before data collection.
* A quantitative alternative. A nonequilibrium model predicts the sign, magnitude, and measurement dependence of the deviation.
* Independent observables. Multiple measurements probe different consequences of the same fitted nonequilibrium parameters.
* Exclusion of conventional explanations. Calibration errors, environmental effects, source drift, selection bias, and data-processing artifacts are bounded.
* Independent replication. A separate apparatus or research group reproduces the effect and its predicted dependence on controlled parameters.

If the aim is specifically to establish , there is an additional requirement: the observed data must identify a nonequilibrium distribution within a model that connects hidden configurations to measurable outcomes. Without this connection, the experiment establishes an operational anomaly, not the underlying ontology.

4. The principal experimental challenge

The central difficulty is not merely detecting a deviation from a probability law. It is obtaining a physical ensemble that is predicted to retain a nonequilibrium distribution.

In the standard pilot-wave framework, the Born-equilibrium distribution is dynamically preserved. Nonequilibrium initial conditions are permitted mathematically, but the theory does not provide a universally accepted, experimentally validated laboratory procedure that prepares a known distribution on demand.

A proposal that assumes access to such a distribution without specifying its origin is incomplete.

There are three possible routes:

Route A — Laboratory Born-rule tests

Test probability relations in controlled optical, atomic, or spin systems. This is the most direct route to testing standard quantum statistics, but a deviation alone does not identify its cause.

Route B — Short-lived high-energy systems

Test targeted spin or polarization probabilities for particles produced in high-energy collisions. Such tests can probe extreme regimes and very short timescales, although they still require a model linking the tested probabilities to nonequilibrium.

Route C — Primordial quantum fluctuations

Search cosmological data for specific departures predicted by models in which early-universe quantum nonequilibrium survives expansion and becomes imprinted on primordial fluctuations. This route addresses a possible origin of nonequilibrium rather than preparing it in a laboratory.

These approaches are complementary, not interchangeable. The first offers experimental control; the second explores a distinct physical regime; the third potentially addresses why nonequilibrium might have existed in the first place.

5. The proposed experiment: a controlled, multichannel test of quantum probability

The recommended laboratory program is a pre-registered, multichannel Born-rule test combining precision polarization measurements with interferometric probability reconstruction.

This is the most defensible starting point because it provides independently measurable quantities, well-defined equilibrium predictions, and a route to testing extensions of quantum theory. It does not, by itself, solve the nonequilibrium-preparation problem. That limitation is part of the experimental design rather than something to conceal.

5.1 Experimental objectives

The experiment must answer four separate questions:

* Do observed outcome probabilities agree with standard quantum predictions?
* Are any deviations reproducible across distinct measurement arrangements?
* Do the deviations follow the quantitative relationships predicted by a specified nonequilibrium model?
* Can the data distinguish that model from other modifications of quantum mechanics?

The experiment should be designed around the final two questions from the beginning. Otherwise, an anomalous result might be statistically significant yet theoretically inconclusive.

5.2 Apparatus architecture

1. Controlled quantum source

Single photons or another well-characterized quantum system; independent source-state diagnostics

2. Randomized preparation and measurement settings

Multiple polarization bases and interferometer configurations, selected independently of the source output

3A. Polarization channel

Outcome frequencies and expectation values

3B. Interferometry channel

Path probabilities and interference observables

4. Blind statistical reconstruction

Compare standard quantum predictions with pre-specified alternative models and calibrated systematic uncertainties

5. Independent replication

Repeat the predicted effect using a second apparatus and an independently analyzed data set

The polarization and interferometry channels should share a common calibration and analysis framework but have independently characterized detectors. This reduces the possibility that a single instrumental artifact generates an apparent agreement between different observables.

5.3 Why polarization is useful

For a two-state quantum system, a measurement along a unit vector can be represented by

\hat{\sigma}_{\mathbf n}=\mathbf n\cdot\boldsymbol{\sigma},

where denotes the Pauli matrices.

For a pure state with Bloch vector , standard quantum mechanics predicts

\langle\hat{\sigma}_{\mathbf n}\rangle
=\mathbf s\cdot\mathbf n

and

P(+\mid\mathbf n)
=\frac{1+\mathbf s\cdot\mathbf n}{2}.

For measurements along different directions, these expectation values obey specific linear relations. Certain deterministic hidden-variable models predict that deviations from equilibrium can break those relations. This gives the experiment a more discriminating target than simply looking for an unexpected count rate.

The essential procedure is to measure the same preparation in several incompatible bases, compare the observed probabilities with the predicted values, and test the consistency relations jointly.

A single anomalous basis is insufficient. The alternative model must predict how the anomaly changes when the measurement direction changes.

5.4 Why interferometry is useful

For a three-path interferometer, let denote the detection probability when all three paths are open, with corresponding probabilities for the relevant subsets of paths.

Define the third-order interference term

\begin{aligned}
I_3={}&P_{ABC}-P_{AB}-P_{AC}-P_{BC}\\
&+P_A+P_B+P_C.
\end{aligned}

Under the ordinary Born-rule framework, with the appropriate experimental normalization and background corrections,

I_3=0.

A statistically significant nonzero result would indicate a departure from the expected pairwise interference structure. However, it would not uniquely demonstrate pilot-wave nonequilibrium. Higher-order interference, generalized probability theories, and experimental imperfections are not interchangeable explanations, and they must be analyzed separately.

Three-path and multiparticle interference tests have already been investigated experimentally. The objective of a new experiment should therefore be to improve discrimination, systematic control, or sensitivity—not to present the mere construction of a three-path interferometer as a new discovery.

6. The indispensable requirement: an explicit nonequilibrium prediction

The most important theoretical task is to specify how the proposed hidden-variable distribution produces a measurable outcome.

Suppose the model contains a distribution

\rho_\lambda(q)

and a measurement procedure , with an outcome map

a=A_M(q,\lambda).

Here represents any additional fixed model parameters. The predicted outcome probability is

P_\rho(a\mid M)

\int_{\Omega}
\rho_\lambda(q)\,
\mathbf 1A_M(q,\\lambda)=a\,dq,

where is the indicator function.

The standard equilibrium prediction is obtained by replacing with the Born distribution, provided the model’s measurement dynamics justify that identification.

The experimental signature is then

\Delta P_a(M)

P_\rho(a\mid M)

P_{\mathrm B}(a\mid M).

This quantity must be calculated before the experiment can be considered a quantitative test of the model.

In particular, the proposal must specify:

* the nonequilibrium distribution or its finite-dimensional parameterization;
* how the distribution is generated or selected physically;
* the system’s dynamics between preparation and measurement;
* the complete measurement interaction;
* the predicted outcome probabilities;
* the effects of decoherence, coarse-graining, and detector response.

If these ingredients are absent, the hypothesis can accommodate too many possible outcomes after the fact. Such flexibility makes a model difficult to falsify.

6.1 A practical parameterization

For a finite-dimensional experimental data set, write the predicted probability as

P(a\mid M,\boldsymbol{\theta})

P_{\mathrm B}(a\mid M)
+
\sum_{k=1}^{K}\theta_k F_{ak}(M),

where are pre-specified deviation templates and are the parameters to be estimated.

The probability constraints require

P(a\mid M,\boldsymbol{\theta})\geq0,
\qquad
\sum_aP(a\mid M,\boldsymbol{\theta})=1.

The parameters must also obey any restrictions imposed by the underlying dynamics. The template functions cannot be chosen freely after inspecting the results.

A nonzero fitted would establish a statistical deviation within this model family. Identifying it as quantum non-equilibrium would additionally require showing that the parameters correspond to a physically admissible and that the model correctly predicts the observations.

7. Statistical analysis and decision criteria

Let be the number of observed outcomes in measurement configuration , with

N_j=\sum_a n_{aj}.

For independent trials, the likelihood is

\mathcal L(\boldsymbol{\theta})

\prod_j
\frac{N_j!}{\prod_a n_{aj}!}
\prod_a
P(a\mid M_j,\boldsymbol{\theta})^{n_{aj}}.

The null hypothesis is , while the alternative permits the specified deviations.

A likelihood-ratio statistic is

\Lambda

2\left\[
\\log\\mathcal L(\\widehat{\\boldsymbol{\\theta}})
-
\\log\\mathcal L(\\mathbf0)
\\right\].

Its null distribution must be established using the appropriate regularity conditions or calibrated by simulation. If parameters lie on boundaries, measurements are correlated, or nuisance parameters are weakly identified, the usual asymptotic approximation may fail.

The statistical protocol should include the following safeguards.

Pre-registration. Specify the primary observables, exclusions, model family, and decision criteria before unblinding the data.

Systematic-error budget. Include source impurity, detector efficiency, background counts, timing offsets, setting-dependent losses, drift, and imperfect path closure.

Multiple-testing correction. Correct for the number of measurement configurations and alternative models examined. A nominally significant result discovered among thousands of exploratory comparisons is not equivalent to a pre-specified discovery.

Independent replication. Require a separate confirmation data set with the same predicted dependence on the experimental controls.

Model comparison. Compare the nonequilibrium hypothesis against plausible conventional explanations, not only against an idealized null model.

A conventional discovery threshold, such as five standard deviations where appropriate, can be a useful criterion, but statistical significance is not sufficient. The result must also be robust to systematic uncertainties and reproducible under the predicted changes in measurement configuration.

8. The source problem: how could non-equilibrium be obtained?

This is the decisive obstacle to a direct laboratory demonstration.

In pilot-wave theory, is mathematically possible, but it does not follow that ordinary laboratory preparation can produce or preserve it. Standard quantum operations are normally analyzed using equilibrium statistics, and one cannot assume that an ordinary state-preparation procedure gives direct control over hidden configurations.

There are three strategies worth pursuing.

8.1 Strategy A: Search for naturally occurring nonequilibrium

The experiment could search for systems that have not undergone sufficient relaxation to quantum equilibrium.

A candidate source would need a physical mechanism that explains:

* why its initial distribution departed from equilibrium;
* why subsequent evolution did not erase the observable departure;
* why the proposed detector remains sensitive to the deviation;
* why the observed signature is not generated by conventional dynamics.

Without such a mechanism, selecting a source because it appears exotic is not an adequate experimental justification.

8.2 Strategy B: Test extreme dynamical regimes

High-energy processes provide a separate opportunity to investigate whether standard probability relations continue to hold under extreme conditions.

A 2025 study by Valentini and Varma proposed targeted Born-rule tests using spin and polarization probabilities associated with high-energy collisions, including photon and tau-lepton processes. It identifies both potential observables and substantial challenges in implementing them.

This provides a concrete research direction, but it does not establish that high-energy collisions create nonequilibrium ensembles. That connection must be derived and tested rather than assumed.

8.3 Strategy C: Search for cosmological remnants

The early universe may offer conditions unavailable in terrestrial experiments. In particular, models of pilot-wave quantum nonequilibrium have proposed that nonstandard primordial field fluctuations could be amplified or transferred to observable cosmological scales during inflation.

This leads to a distinct experimental program involving the cosmic microwave background and primordial perturbations.

The crucial limitation is that cosmological anomalies have many possible causes. A low-multipole power deficit, unusual phase correlation, or non-Gaussian signal would not by itself establish nonequilibrium. The model must predict a joint pattern of observables that distinguishes it from ordinary cosmological parameters, foregrounds, and instrumental effects.

9. The cosmological experiment

If the objective is to test whether quantum non-equilibrium existed before ordinary laboratory systems reached equilibrium, the cosmological route may be conceptually more direct than attempting to manufacture it in a laboratory.

Let denote a primordial curvature perturbation mode. In a simple statistically homogeneous and isotropic description, its two-point statistics are characterized by a power spectrum , conventionally defined through

\left\langle
\mathcal R_{\mathbf k}
\mathcal R_{\mathbf k’}^*
\right\rangle

(2\pi)^3\delta^{(3)}(\mathbf k-\mathbf k’)
P_{\mathcal R}(k).

A particular nonequilibrium model may predict a modified spectrum

P_{\mathcal R}(k)

P_{\mathrm{eq}}(k)\,\xi(k),

where is the equilibrium prediction and is a model-specific transfer function.

For example, a suppression of long-wavelength power could be represented by

0<\xi(k)<1

over a specified range of small . This expression is a parameterization, not a universal prediction of quantum non-equilibrium.

The actual experiment would test the following sequence:

* Derive from a specific initial nonequilibrium distribution and its evolution.
* Propagate the predicted primordial statistics through the relevant cosmological transfer functions.
* Calculate the resulting temperature and polarization angular spectra.
* Fit the model jointly to available cosmological observations.
* Compare it with standard cosmological models and competing explanations.
* Test independent predictions involving correlations, phases, or higher-order statistics.

The last step is essential. A model that merely adjusts the power spectrum to match an existing anomaly has limited explanatory force. A successful model should predict additional observables that were not used to tune its parameters.

A cosmological result could support the existence of primordial departures from Born-equilibrium statistics, but the inference would remain conditional on the cosmological model and its mapping from quantum field statistics to observed perturbations.

10. Falsification conditions

A scientifically useful proposal must state what would count against it.

The experiment should distinguish three possible outcomes.

Outcome I: No detectable deviation

The observations agree with the Born-rule predictions within a quantified uncertainty. This constrains the tested deviation templates and parameter ranges; it does not establish that nonequilibrium is impossible in all systems.

Outcome II: An anomaly without model agreement

A deviation is detected, but its dependence on measurement settings, source conditions, or other observables fails to match the proposed nonequilibrium dynamics. This rejects the tested model or requires a revised explanation; it does not confirm quantum non-equilibrium.

Outcome III: A replicated, model-specific deviation

A deviation survives independent systematic checks, follows the pre-specified nonequilibrium predictions across multiple observables, and is reproduced independently. This would constitute strong evidence for the tested extension of quantum theory and, if the hidden-variable mapping is independently justified, for quantum non-equilibrium.

The third outcome is the desired result. Its significance comes not from the size of an anomaly alone, but from the convergence of independent measurements on a constrained dynamical explanation.

11. The role of relaxation

A further difficulty is that a nonequilibrium distribution may evolve toward coarse-grained equilibrium before it is measured.

The fine-grained conservation of does not imply that every experimentally accessible distribution will remain detectably nonequilibrium. Mixing can create structure on scales smaller than the resolution of an apparatus.

A useful diagnostic is the relative-entropy functional

D_{\mathrm{KL}}(\rho\Vert P_{\mathrm B})

\int \rho(q)
\ln\frac{\rho(q)}{P_{\mathrm B}(q)}\,dq,

provided the relevant distributions are normalized and the integral exists.

This quantity is nonnegative and vanishes when the distributions agree almost everywhere. In a coarse-grained relaxation scenario, the corresponding coarse-grained divergence may decrease even though the fine-grained ratio remains conserved along trajectories.

The experimental consequence is immediate: the proposed preparation, transport, and detection stages must be analyzed as a single dynamical system. It is not enough to posit a nonequilibrium distribution at an inaccessible initial time if the predicted signal becomes unobservable before the final measurement.

The duration of the experiment, spatial resolution, environmental coupling, and phase-space mixing must therefore enter the sensitivity model.

12. What a Born-rule violation would—and would not—prove

The logic of inference must remain precise.

A verified Born-rule violation would establish that the standard quantum statistical description fails under the tested conditions, assuming conventional experimental explanations have been excluded.

It would not, by itself, prove that pilot-wave theory is correct. Alternative theories could also predict deviations from Born-rule statistics, and generalized probability theories may depart from standard quantum mechanics in different ways.

Likewise, a violation of a higher-order interference constraint would test a particular structural feature of the standard probability rule. It would not automatically identify the underlying cause as a nonequilibrium hidden-variable distribution.

For a specifically pilot-wave interpretation, the strongest evidence would combine:

* a reproducible probability anomaly;
* a quantitative nonequilibrium distribution or constrained parameterization;
* a dynamical model connecting that distribution to the measured outcomes;
* consistency across independent measurement arrangements;
* and successful predictions of additional effects not used in fitting the original data.

The inference should proceed from the observable discrepancy to the model, and only then to the proposed underlying distribution. Reversing that order risks treating a desired interpretation as an experimental result.

13. Recommended experimental program

The research program should proceed in stages.

Stage	Primary task	Required deliverable
I. Theory	Specify a nonequilibrium model and derive its observables	A falsifiable probability-level prediction
II. Calibration	Establish detector response and the standard quantum baseline	A complete uncertainty budget
III. Laboratory test	Measure polarization and interferometric probabilities	A blinded, pre-registered data set
IV. Model discrimination	Compare equilibrium, nonequilibrium, and conventional alternatives	Parameter bounds or a robust model preference
V. Replication	Repeat the predicted effect independently	Confirmation with independent apparatus and analysis
VI. Source investigation	Test high-energy or cosmological mechanisms for nonequilibrium	Evidence for, or constraints on, a physically motivated source

The laboratory test should be initiated first because it offers the greatest experimental control. In parallel, theory work should address the preparation problem rather than merely proposing more sensitive detectors.

High-energy and cosmological programs should then be pursued where their physical assumptions provide a distinct advantage.

14. Final conclusion

The correct experiment for quantum non-equilibrium is not simply a double-slit experiment, a Bell test, a quantum-entanglement demonstration, or a search for an unusual quantum state. None of those, by itself, establishes a departure from the Born-equilibrium distribution.

The decisive experiment is a controlled and independently replicated test of a quantitative prediction that differs from standard quantum statistics and is specifically derived from a physically defined nonequilibrium model.

The most practical laboratory starting point is a multichannel Born-rule test using polarization measurements and interferometry, with pre-registered probability relations, blinded analysis, explicit systematic controls, and independent replication. High-energy polarization experiments provide a complementary route into extreme regimes, while cosmological observations may test models in which primordial nonequilibrium leaves a surviving statistical signature.

The unresolved central issue is the origin and accessibility of the nonequilibrium distribution itself. Pilot-wave dynamics permits , but mathematical permission is not experimental preparation, and a statistical anomaly is not an identification of its cause.

Accordingly, the strongest possible result would establish a reproducible deviation, show that the deviation follows a pre-specified nonequilibrium model across independent observables, and exclude credible competing explanations. That would provide compelling evidence for quantum non-equilibrium within the tested framework.

Until such evidence exists, quantum non-equilibrium remains a testable theoretical possibility—not an experimentally established fact.

Selected references

1. Valentini, A. “Inflationary cosmology as a probe of primordial quantum mechanics.” Physical Review D 82, 063513 (2010). DOI: 10.1103/PhysRevD.82.063513⁠￼.

2. Valentini, A., and Varma, M. “Toward a test of the Born rule in high-energy collisions.” Physical Review D 112, 112024 (2025). DOI: 10.1103/4llk-pt1j⁠￼.

3. Colin, S., and Valentini, A. “Instability of quantum equilibrium in Bohm’s dynamics.” Proceedings of the Royal Society A 470, 20140288 (2014). DOI: 10.1098/rspa.2014.0288⁠￼.

4. Conlon, L. O., et al. “Testing the postulates of quantum mechanics with coherent states of light and homodyne detection.” New Journal of Physics (2024). DOI: 10.1088/1367-2630/ad4203⁠￼.

5. “Many-particle interference to test Born’s rule.” Physical Review Research 2, 012051 (2020). Physical Review Research⁠￼.

6. Valentini, A. “Signal-locality in hidden-variables theories.” Physics Letters A 297, 273–278 (2002). DOI: 10.1016/S0375-9601(02)00438-3⁠￼.

7. Valentini, A. “Quantum gravity and quantum probability.” (2021). arXiv:2104.07966⁠￼.

The references establish that quantum-equilibrium dynamics, primordial nonequilibrium scenarios, and targeted Born-rule tests are existing lines of research. They do not establish that quantum non-equilibrium has already been detected.
