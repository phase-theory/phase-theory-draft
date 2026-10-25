Quantum Non-Equilibrium from Universal Phase Theory

A Foundational Derivation, Mathematical Closure Audit, and Experimental Proof Program

Universal Phase Theory (UPT) — Research Preprint

Abstract

The objective of this paper is to determine whether quantum non-equilibrium can be derived from Universal Phase Theory (UPT), rather than introduced as an independent postulate. The target is a mathematically precise departure from Born-equilibrium statistics and a derivation of the conditions under which that departure could become physically observable.

The central distinction is between three propositions:

* A phase configuration can contain information not represented by a conventional quantum state.
* A physical distribution over phase configurations can differ from the probability distribution induced by the Born rule.
* That difference can generate measurable violations of Born-rule statistics.

The first proposition does not, by itself, establish the second; the second does not, by itself, establish the third. A complete derivation must connect all three through explicit mathematical maps and a physically justified measurement theory.

We therefore formulate the problem in the language of UPT’s phase-first hierarchy, derive the relevant conditions for non-equilibrium, identify the assumptions necessary to obtain observable deviations, and establish a proof-and-falsification program. The paper distinguishes formal theorems from conditional results and unresolved physical conjectures.

The decisive question is not whether UPT can accommodate quantum non-equilibrium mathematically. It is whether the theory’s foundational structure forces, permits, or empirically selects a non-equilibrium distribution without importing the desired conclusion into its premises.

Epistemic discipline. The foundational UPT manuscript explicitly identifies the Born rule as an unresolved derivation problem: it proposes an invariant additive phase measure , but states that the derivation has not yet been completed. Consequently, a proof of quantum non-equilibrium cannot honestly be obtained by assuming the Born rule as a derived UPT theorem and then declaring a departure from it. The correct derivation must expose this dependency, establish the conditional mathematical results, and identify the additional theorem needed to close the theory.

The paper below follows that standard. It develops a precise UPT construction of quantum non-equilibrium as a candidate, derives its mathematical criteria and observable consequences, and separates what follows from the present foundations from what remains to be proved physically.

Quantum Non-Equilibrium from Universal Phase Theory

A Conditional Derivation of Phase-Measure Deviation, Dynamical Persistence, and Observable Departures from Born Statistics

Universal Phase Theory — Foundational Research Preprint
October 2026

Abstract

We investigate whether quantum non-equilibrium can be derived from Universal Phase Theory (UPT) as a consequence of phase structure, rather than introduced as an independent physical postulate.

The foundational object is a generalized phase configuration \Phi\in\mathcal C_\Phi, constrained by the universal admissibility equation

\[
\mathscr F[\Phi;\lambda]=0,
\]

with linearized stability operator

\[
\mathscr L_\Phi=D_\Phi\mathscr F[\Phi;\lambda].
\]

The central problem is probabilistic: under what conditions can a distribution over admissible phase configurations differ from the statistical distribution associated with the emergent quantum state, and when must that difference produce an observable departure from the Born rule?

We establish five results.

First, the admissibility equation, phase stability operator, susceptibility, topology, and emergent geometry do not by themselves determine a unique probability measure. A derivation of quantum non-equilibrium therefore requires a measure-theoretic extension of the existing UPT architecture.

Second, given a well-defined reference measure associated with Born-equilibrium statistics, every absolutely continuous candidate distribution can be represented by a nonnegative density f. The condition f\neq1 almost everywhere characterizes distributional departure from that reference measure.

Third, distributional departure does not necessarily imply an observable deviation. A measurement-response map must distinguish the nonequilibrium component of the phase distribution from the equilibrium component.

Fourth, under an explicitly specified measure-preserving phase flow, the fine-grained density ratio is transported along trajectories. Coarse-grained relaxation, when it occurs, requires additional assumptions about mixing and observational resolution.

Fifth, the resulting theory yields a falsifiable experimental program based on deviations from Born probabilities, with quantitative predictions, systematic controls, and independent replication.

The principal conclusion is precise: UPT presently supplies a framework in which quantum non-equilibrium can be formulated, but a complete derivation of its physical existence requires additional phase-measure, dynamical, and measurement theorems. The paper establishes the mathematical consequences of those theorems conditionally and specifies the closure conditions needed to turn the construction into a physical prediction.

Keywords: Universal Phase Theory; quantum non-equilibrium; phase measure; Born rule; phase configuration space; probability reconstruction; phase dynamics; quantum measurement; falsifiability.

⸻

Part I. The foundational problem

1. Phase primacy and the statistical question

Universal Phase Theory begins with the structural organization of phase rather than taking spacetime, particles, quantum states, or probability measures as primitive.

Let

\Phi:\mathcal X\longrightarrow\mathcal M_\Phi

be a generalized phase configuration on a foundational domain \mathcal X. Let \mathcal C_\Phi denote its admissible configuration space, and let \(\mathscr G_\Phi\) be the group or groupoid of admissible phase transformations.

Physical phase configurations are represented by equivalence classes

\[
[\Phi]\in\mathcal C_\Phi/\mathscr G_\Phi.
\]

Admissibility is imposed by

\[
\boxed{\mathscr F[\Phi;\lambda]=0,}
\tag{1.1}
\]

where \lambda denotes admissible control data.

The phase stability operator is

\[
\boxed{\mathscr L_\Phi=D_\Phi\mathscr F[\Phi;\lambda],}
\tag{1.2}
\]

and, on a suitable complement to gauge and collective zero modes, the phase susceptibility is

\[
\boxed{\boldsymbol\chi_\Phi
=\mathscr L_\Phi^{-1}.}
\tag{1.3}
\]

These operators characterize admissibility, local structural response, stability, and phase transitions.

They do not, without further structure, define the probability of an outcome.

That distinction is decisive. A deterministic equation can constrain which configurations are admissible without specifying how an ensemble of configurations is distributed. Stability can select persistent configurations without selecting their statistical weights. Topology can classify sectors without determining the frequency with which those sectors occur.

Quantum non-equilibrium is therefore not a consequence of phase primacy alone. It is a problem of the relation between phase configurations, probability measures, and observable outcomes.

2. Definition of quantum non-equilibrium

Let \mathcal C_\Phi be equipped with a measurable structure \Sigma_\Phi. Suppose that a physically meaningful probability measure \mu_{\mathrm{eq}} has been defined for a specified equilibrium model.

A candidate physical ensemble is described by another probability measure \mu.

We define distributional quantum non-equilibrium relative to that equilibrium model by

\[
\boxed{\mu\neq\mu_{\mathrm{eq}}.}
\tag{2.1}
\]

The word relative is essential. A departure is meaningful only after the reference measure has been specified.

For the particular case of Born-equilibrium statistics, let \mathcal H_{\mathrm{eff}} be an emergent Hilbert space and let

\[
\mathcal Q:\mathcal C_\Phi
\longrightarrow\mathbb P(\mathcal H_{\mathrm{eff}})
\tag{2.2}
\]

be a phase-to-quantum-state map, where \mathbb P(\mathcal H_{\mathrm{eff}}) denotes the space of rays.

For a normalized state |\psi\rangle and a measurement represented by positive operators E_a, standard quantum mechanics predicts

\[
P_{\mathrm B}(a\mid\psi,M)
=
\langle\psi|E_a|\psi\rangle,
\qquad
\sum_a E_a=I.
\tag{2.3}
\]

For a projective measurement in an orthonormal basis,

E_a=|a\rangle\langle a|,

and therefore

\[
P_{\mathrm B}(a\mid\psi,M)
=
|\langle a|\psi\rangle|^2.
\tag{2.4}
\]

A UPT model of quantum non-equilibrium must explain how a physical distribution over phase configurations can depart from the distribution that reproduces (2.3)–(2.4).

It is not enough to introduce another symbol for probability. The phase measure must be independently defined and its relationship to observed frequencies established.

3. Three distinct propositions

The derivation must keep the following statements separate.

Proposition A — Phase information beyond the quantum state.

There may exist distinct admissible configurations \Phi_1,\Phi_2 satisfying

\mathcal Q(\Phi_1)=\mathcal Q(\Phi_2)

while

[\Phi_1]\neq[\Phi_2].

This establishes that the emergent quantum state does not uniquely determine the underlying phase configuration.

Proposition B — Distinct phase distributions.

There may exist physically admissible measures \mu and \mu_{\mathrm{eq}} satisfying

\mu\neq\mu_{\mathrm{eq}}.

This requires an ensemble structure and a physically meaningful rule for constructing or selecting measures.

Proposition C — Observable departure.

There may exist a measurement M and outcome a for which

P_\mu(a\mid M)\neq P_{\mathrm B}(a\mid M).

This requires a measurement-response map capable of distinguishing the two distributions.

Neither Proposition A nor Proposition B alone entails Proposition C.

The task of the present paper is to derive the exact mathematical conditions connecting these three levels.

⸻

Part II. The measure-theoretic extension of UPT

4. Phase configurations and their emergent quantum states

Let (\mathcal C_\Phi,\Sigma_\Phi) be the measurable space of admissible phase configurations, after quotienting by physically redundant phase transformations where appropriate.

The quantum-state map is

\[
\mathcal Q:\mathcal C_\Phi
\rightarrow\mathbb P(\mathcal H_{\mathrm{eff}}).
\tag{4.1}
\]

For a fixed emergent quantum state [\psi], define its phase fiber

\[
\mathcal F_\psi
=
\mathcal Q^{-1}([\psi]).
\tag{4.2}
\]

The fiber contains every admissible phase configuration that produces the same effective quantum state.

If \mathcal F_\psi contains more than one physically distinct configuration, then the emergent state map is many-to-one. This permits the possibility that different phase ensembles project onto the same effective state while possessing different distributions over underlying phase configurations.

However, the existence of a nontrivial fiber does not imply that every distinction within the fiber is measurable.

The measurement theory must determine which distinctions have operational consequences.

5. Pushforward measures and the Born reference

Given a phase measure \mu, its pushforward under the state map is

\[
\mathcal Q_*\mu(B)
=
\mu\bigl(\mathcal Q^{-1}(B)\bigr)
\tag{5.1}
\]

for measurable sets B in the emergent state space.

This operation transfers a measure over phase configurations to a measure over effective quantum states.

It does not, by itself, derive the Born rule. The Born rule assigns probabilities to outcomes conditional on a state and a measurement; the pushforward in (5.1) instead describes the distribution of emergent states in an ensemble.

To connect the two, UPT needs an outcome-response kernel.

Define

\[
K(a\mid\Phi,M)\in[0,1],
\tag{5.2}
\]

with

\[
\sum_a K(a\mid\Phi,M)=1
\tag{5.3}
\]

for each admissible configuration and measurement.

The kernel represents the probability of outcome a conditional on the underlying phase configuration and the measurement interaction. In a deterministic realization, it may reduce to an indicator function,

\[
K(a\mid\Phi,M)
=
\mathbf 1\{A_M(\Phi)=a\}.
\tag{5.4}
\]

In a stochastic realization, it remains a normalized conditional distribution.

The predicted outcome probability is then

\[
\boxed{
P_\mu(a\mid M)
=
\int_{\mathcal C_\Phi}
K(a\mid\Phi,M)\,d\mu(\Phi).
}
\tag{5.5}
\]

Equation (5.5) is the fundamental bridge between phase statistics and empirical statistics.

A completed UPT derivation must derive or justify both the phase measure and the kernel. Neither follows merely from the notation \(\mathscr F[\Phi;\lambda]=0\).

6. The equilibrium measure

Suppose that an equilibrium measure \mu_{\mathrm{eq}} exists and that its response kernel reproduces the Born rule:

\[
\boxed{
\int_{\mathcal C_\Phi}
K(a\mid\Phi,M)\,d\mu_{\mathrm{eq}}(\Phi)
=
\langle\psi|E_a|\psi\rangle.
}
\tag{6.1}
\]

Equation (6.1) is the equilibrium correspondence condition.

It is not yet a theorem of the current UPT foundations. It is a closure condition that a complete derivation must establish.

The same point applies to the phase-branch formulation. If accessible branches are assigned measures \mu_i, the normalized probabilities

\[
P_i=\frac{\mu_i}{\sum_j\mu_j}
\tag{6.2}
\]

reproduce the Born rule only if the branch measure is independently shown to satisfy

\[
\mu_i=C|\langle i|\psi\rangle|^2
\tag{6.3}
\]

for a common positive normalization factor C.

Defining the branch measure by (6.3) would reproduce the Born rule by construction rather than derive it.

For the remainder of the paper, \mu_{\mathrm{eq}} is treated as a reference measure satisfying (6.1), conditional on a successful Born-measure derivation.

⸻

Part III. The mathematical derivation of non-equilibrium

7. The density-ratio theorem

Assume that a candidate measure \mu is absolutely continuous with respect to \mu_{\mathrm{eq}}. By the Radon–Nikodym theorem, there exists a measurable function

\[
f(\Phi)
=
\frac{d\mu}{d\mu_{\mathrm{eq}}}(\Phi)
\tag{7.1}
\]

such that

\[
d\mu(\Phi)=f(\Phi)\,d\mu_{\mathrm{eq}}(\Phi).
\tag{7.2}
\]

Because \mu is a probability measure,

\[
f(\Phi)\geq0
\quad \mu_{\mathrm{eq}}\text{-almost everywhere}
\tag{7.3}
\]

and

\[
\boxed{
\int_{\mathcal C_\Phi}
f(\Phi)\,d\mu_{\mathrm{eq}}(\Phi)=1.
}
\tag{7.4}
\]

The equilibrium distribution corresponds to

\[
f(\Phi)=1
\quad \mu_{\mathrm{eq}}\text{-almost everywhere}.
\tag{7.5}
\]

Therefore,

\[
\boxed{
\mu\neq\mu_{\mathrm{eq}}
\iff
f\neq1
\text{ on a set of positive }\mu_{\mathrm{eq}}\text{-measure}.
}
\tag{7.6}
\]

Theorem 1 — Measure-theoretic criterion for phase non-equilibrium

Let \mu_{\mathrm{eq}} and \mu be probability measures on the same measurable phase-configuration space. If \mu\ll\mu_{\mathrm{eq}}, then the following are equivalent:

1. \mu=\mu_{\mathrm{eq}}.
2. f=d\mu/d\mu_{\mathrm{eq}}=1 almost everywhere.
3. The integral of f-1 over every measurable subset of \mathcal C_\Phi vanishes.

Consequently, distributional non-equilibrium is equivalent to the existence of a measurable subset A such that

\[
\int_A f\,d\mu_{\mathrm{eq}}
\neq
\mu_{\mathrm{eq}}(A).
\tag{7.7}
\]

Proof. If \mu=\mu_{\mathrm{eq}}, uniqueness of the Radon–Nikodym derivative gives f=1 almost everywhere. Conversely, if f=1 almost everywhere, equation (7.2) implies equality of the measures. If the measures differ, the signed measure \mu-\mu_{\mathrm{eq}} is nonzero, so there exists a measurable set A on which it does not vanish. The converse follows immediately. \square

This theorem is exact. It establishes the mathematical criterion for a distributional departure from an already defined equilibrium measure.

It does not establish that such a measure occurs in nature or that the deviation is observable.

8. A concrete family of nonequilibrium distributions

The criterion can be made explicit without assigning an arbitrary physical meaning to the density ratio.

Let h:\mathcal C_\Phi\rightarrow\mathbb R be a bounded measurable function with

\[
\int h\,d\mu_{\mathrm{eq}}=0.
\tag{8.1}
\]

For sufficiently small \epsilon, define

\[
f_\epsilon(\Phi)=1+\epsilon h(\Phi).
\tag{8.2}
\]

If

\[
|\epsilon|\,\|h\|_\infty<1,
\tag{8.3}
\]

then f_\epsilon\geq0. Furthermore,

\[
\int f_\epsilon\,d\mu_{\mathrm{eq}}
=
1+\epsilon\int h\,d\mu_{\mathrm{eq}}
=1.
\tag{8.4}
\]

Thus

\[
d\mu_\epsilon
=
(1+\epsilon h)\,d\mu_{\mathrm{eq}}
\tag{8.5}
\]

defines a normalized probability measure.

Whenever h is not zero almost everywhere and \epsilon\neq0,

\[
\mu_\epsilon\neq\mu_{\mathrm{eq}}.
\tag{8.6}
\]

This construction proves the mathematical possibility of a continuous family of measures departing from equilibrium.

It does not derive a physical preparation mechanism. The function h is a mathematical perturbation until a phase-dynamical or cosmological process selects it.

8.1 The physical selection problem

For a genuine UPT derivation, h must not be an unconstrained fitting function. It must arise from a specified physical mechanism, such as a nonequilibrium initial condition, a phase transition, or a nontrivial measure inherited from an earlier phase regime.

A complete theory must explain why the mechanism generates the selected h, how its parameters are fixed, and why the resulting distribution persists until observation.

Without that explanation, equation (8.5) is a construction of possible measures, not a prediction of a particular measure.

9. Why phase non-equilibrium need not be observable

Using equations (5.5) and (7.2),

\[
P_\mu(a\mid M)
=
\int K(a\mid\Phi,M)f(\Phi)\,d\mu_{\mathrm{eq}}(\Phi).
\tag{9.1}
\]

Subtracting the equilibrium probability gives

\[
\boxed{
\Delta P_a(M)
=
\int K(a\mid\Phi,M)
\bigl[f(\Phi)-1\bigr]\,
d\mu_{\mathrm{eq}}(\Phi).
}
\tag{9.2}
\]

This equation is the central observable criterion of the theory.

Even if f\neq1, the integral in (9.2) can vanish for every accessible measurement. Non-equilibrium then exists at the level of the underlying measure but remains statistically invisible to the tested measurement family.

Theorem 2 — Observable-deviation criterion

Suppose the equilibrium measure satisfies the Born correspondence condition (6.1). Then a phase ensemble \mu=f\mu_{\mathrm{eq}} produces a Born-rule violation if and only if there exists an accessible measurement M and outcome a such that

\[
\boxed{
\int K(a\mid\Phi,M)(f-1)\,d\mu_{\mathrm{eq}}\neq0.
}
\tag{9.3}
\]

Proof. Equation (9.1) gives the probability under \mu. Equation (6.1) gives the Born probability under \mu_{\mathrm{eq}}. Their difference is exactly (9.2). The probabilities differ precisely when the integral is nonzero. \square

This result separates a distributional claim from an observational claim. It also identifies the exact task of measurement theory: find observables whose response functions have nonzero overlap with the nonequilibrium component f-1.

10. The measurement-blindness theorem

Let \(\mathscr K\) be the family of all accessible response functions

\[
\mathscr K
=
\{K(a\mid\cdot,M):a,M\text{ accessible}\}.
\tag{10.1}
\]

Define the nonequilibrium perturbation

\[
g=f-1.
\tag{10.2}
\]

Normalization implies

\[
\int g\,d\mu_{\mathrm{eq}}=0.
\tag{10.3}
\]

If

\[
\int Kg\,d\mu_{\mathrm{eq}}=0
\qquad
\text{for every }K\in\mathscr K,
\tag{10.4}
\]

then all accessible measurement probabilities agree with equilibrium predictions.

The set of all such perturbations is the measurement-blind subspace

\[
\mathscr N_{\mathscr K}
=
\left\{
g:
\int g\,d\mu_{\mathrm{eq}}=0,\
\int Kg\,d\mu_{\mathrm{eq}}=0
\ \forall K\in\mathscr K
\right\}.
\tag{10.5}
\]

Proposition 1 — Measurement blindness

If \(g\in\mathscr N_{\mathscr K}\) and f=1+g\geq0, then \mu\neq\mu_{\mathrm{eq}} may hold even though no accessible measurement detects the departure.

Proof. The first condition in (10.5) ensures normalization. The second makes equation (9.2) vanish for every accessible response function. If g\neq0 on a set of positive measure, equation (7.6) still gives \mu\neq\mu_{\mathrm{eq}}. \square

This proposition establishes a fundamental limitation. The existence of extra phase information beyond the emergent quantum state does not guarantee a Born-rule violation.

If the response kernel depends only on the emergent state \mathcal Q(\Phi), and the nonequilibrium perturbation preserves the relevant conditional distribution within every phase fiber, then the additional phase structure can be statistically invisible.

A successful UPT theory must therefore derive not only the phase measure but also a measurement interaction that is sensitive to its nonequilibrium component.

⸻

Part IV. Quantifying departure from equilibrium

11. Total-variation distance

Define the total-variation distance between the candidate and equilibrium measures by

\[
D_{\mathrm{TV}}(\mu,\mu_{\mathrm{eq}})
=
\sup_{A\in\Sigma_\Phi}
|\mu(A)-\mu_{\mathrm{eq}}(A)|.
\tag{11.1}
\]

For absolutely continuous measures,

\[
D_{\mathrm{TV}}
=
\frac12
\int|f-1|\,d\mu_{\mathrm{eq}}.
\tag{11.2}
\]

This quantity satisfies

\[
0\leq D_{\mathrm{TV}}\leq1,
\tag{11.3}
\]

and vanishes if and only if the measures are equal.

For any response function K\in[0,1],

\[
\left|
\int K\,d\mu-\int K\,d\mu_{\mathrm{eq}}
\right|
\leq D_{\mathrm{TV}}.
\tag{11.4}
\]

Hence

\[
\boxed{|\Delta P_a(M)|\leq D_{\mathrm{TV}}.}
\tag{11.5}
\]

This is an upper bound on the probability deviation, not a guarantee of detectability. A large underlying distance can coexist with small observed deviations if the measurement family is insensitive to the relevant phase structure.

For a finite family of measured events A_1,\ldots,A_n, define the operational distance

\[
D_{\mathrm{op}}
=
\sup_{A\in\mathscr A_{\mathrm{meas}}}
|\mu(A)-\mu_{\mathrm{eq}}(A)|,
\tag{11.6}
\]

where \(\mathscr A_{\mathrm{meas}}\) is the family of events actually measurable by the apparatus.

Then

\[
D_{\mathrm{op}}\leq D_{\mathrm{TV}}.
\tag{11.7}
\]

The distinction between the full phase-space distance and the operational distance is essential for experimental design.

12. Relative entropy

Where the integral exists, define the Kullback–Leibler divergence

\[
D_{\mathrm{KL}}(\mu\Vert\mu_{\mathrm{eq}})
=
\int f\ln f\,d\mu_{\mathrm{eq}}.
\tag{12.1}
\]

It obeys

\[
D_{\mathrm{KL}}\geq0,
\tag{12.2}
\]

with equality if and only if \mu=\mu_{\mathrm{eq}}.

For a small perturbation f=1+\epsilon h, with \int h\,d\mu_{\mathrm{eq}}=0, expansion gives

\[
\begin{aligned}
D_{\mathrm{KL}}
&=
\int(1+\epsilon h)\ln(1+\epsilon h)
\,d\mu_{\mathrm{eq}}\\
&=
\frac{\epsilon^2}{2}
\int h^2\,d\mu_{\mathrm{eq}}
+O(\epsilon^3).
\end{aligned}
\tag{12.3}
\]

The first-order term vanishes because the perturbation preserves normalization.

Equation (12.3) gives a natural quadratic measure of small phase-distribution departures. It can be used to organize a perturbative analysis, but it does not determine which nonequilibrium modes are physically generated.

⸻

Part V. Dynamics and persistence

13. The phase evolution law

UPT represents dynamics schematically through an evolution law

\[
\mathscr D\Phi=\mathscr K[\Phi].
\tag{13.1}
\]

To derive the evolution of an ensemble, equation (13.1) must induce a well-defined flow

\[
T_t:\mathcal C_\Phi\rightarrow\mathcal C_\Phi.
\tag{13.2}
\]

Assume that this flow is sufficiently regular and that both the equilibrium and candidate measures are transported by it.

Define the evolved measures by

\[
\mu_t=(T_t)_*\mu_0,
\qquad
\mu_{\mathrm{eq},t}=(T_t)_*\mu_{\mathrm{eq},0}.
\tag{13.3}
\]

If \mu_0\ll\mu_{\mathrm{eq},0}, then the evolved density ratio is

\[
f_t
=
\frac{d\mu_t}{d\mu_{\mathrm{eq},t}}.
\tag{13.4}
\]

Theorem 3 — Transport of the nonequilibrium density ratio

Under an invertible measurable phase flow T_t, with the measures in (13.3), the density ratio obeys

\[
\boxed{f_t(\Phi)=f_0(T_{-t}\Phi)}
\tag{13.5}
\]

almost everywhere with respect to \mu_{\mathrm{eq},t}.

Proof. For any measurable set A,

\mu_t(A)=\mu_0(T_{-t}A)
=\int_{T_{-t}A}f_0\,d\mu_{\mathrm{eq},0}.

Changing variables under the pushforward measure gives

\mu_t(A)
=
\int_A f_0(T_{-t}\Phi)\,d\mu_{\mathrm{eq},t}(\Phi).

Uniqueness of the Radon–Nikodym derivative yields equation (13.5). \square

This theorem is a measure-theoretic transport result. It does not require the flow to be Hamiltonian, but it does require that the same flow transport both measures.

In a Hamiltonian or pilot-wave realization, it can be specialized to the familiar continuity-equation formulation. In UPT, the corresponding phase flow and reference measure must first be explicitly constructed.

14. Fine-grained persistence

Equation (13.5) shows that an invertible deterministic flow rearranges the density ratio rather than automatically setting it equal to unity.

If f_0\neq1, then

f_t\neq1

as a measure-theoretic statement under the invertible pushforward, unless the initial measure already coincides with the reference measure.

This is the mathematical sense in which fine-grained nonequilibrium can persist.

It does not follow that the deviation remains observable. Phase-space structures can become progressively finer, and a finite-resolution detector may fail to resolve them.

15. Coarse-grained relaxation

Let \mathcal P denote a coarse-graining operation associated with the finite resolution of an apparatus. A coarse-grained density ratio may be written schematically as

\[
\bar f_t=\mathcal P f_t.
\tag{15.1}
\]

Even when f_t\neq1, the coarse-grained ratio may approach unity:

\[
\bar f_t\longrightarrow1.
\tag{15.2}
\]

Such convergence requires appropriate dynamical mixing and assumptions about the coarse-graining procedure. It is not implied by phase primacy alone.

A useful diagnostic is the coarse-grained divergence

\[
\overline D_{\mathrm{KL}}(t)
=
\int \bar f_t\ln\bar f_t\,
d\mu_{\mathrm{eq},t}.
\tag{15.3}
\]

Under suitable conditional-expectation coarse-graining, convexity of x\ln x gives a non-increase relative to the corresponding fine-grained divergence. Whether the divergence actually approaches zero depends on the dynamics and the resolution scale.

Proposition 2 — A necessary relaxation audit

A proposed UPT nonequilibrium experiment is incomplete if it predicts a nonzero initial phase-distribution deviation but does not determine whether that deviation survives at the measurement time.

Justification. The measurable probability depends on the evolved measure through equation (9.1). If the relevant deviation is averaged away by the apparatus response, its initial existence does not imply an observable final effect.

This is not a no-go theorem for detection. It is a requirement that the source, transport, and measurement stages be modeled together.

⸻

Part VI. The connection to the Born rule

16. Why the Born rule is a closure condition

The UPT foundational program proposes that branch probabilities arise from phase measures:

\[
P_i=\frac{\mu_i}{\sum_j\mu_j}.
\tag{16.1}
\]

It also identifies the desired relation

\[
\mu_i\propto|\langle i|\psi\rangle|^2.
\tag{16.2}
\]

The unresolved problem is to derive the measure \mu_i from the underlying phase structure.

The relevant conditions include:

1. Additivity for mutually exclusive outcomes.
2. Invariance under admissible phase-frame transformations.
3. Consistency under composition of systems.
4. Continuity under admissible changes in phase configuration.
5. Normalization.
6. Compatibility with interference.
7. Consistency across different measurement contexts.

These conditions are substantive, but their mere listing does not prove that the Born measure is unique. They must be formalized as mathematical hypotheses on a specified phase measure and outcome structure.

A Gleason-type reconstruction, for example, requires a precise Hilbert-space event structure and assumptions about the probability assignment. It cannot be invoked simply because UPT uses phase and interference.

For two-dimensional Hilbert spaces, the standard Gleason theorem does not apply in its simplest form without additional assumptions. A UPT derivation must handle this case explicitly rather than claim universal coverage from a higher-dimensional result.

17. The logical dependence of non-equilibrium

Suppose the Born correspondence theorem is eventually established:

\[
P_{\mu_{\mathrm{eq}}}(a\mid M)
=
\langle\psi|E_a|\psi\rangle.
\tag{17.1}
\]

Then the nonequilibrium deviation follows from equation (9.2):

\[
\Delta P_a(M)
=
\int K(a\mid\Phi,M)(f-1)\,
d\mu_{\mathrm{eq}}.
\tag{17.2}
\]

This is a conditional theorem: once the equilibrium correspondence and measurement model are valid, the difference between the two predicted probability assignments is exactly the response-weighted density-ratio deviation.

But there are two logically distinct research programs.

Program I — Derive Born equilibrium.

Construct the phase measure and show that the equilibrium ensemble reproduces equation (17.1).

Program II — Derive nonequilibrium physics.

Establish a physical mechanism that generates f\neq1, derive its evolution, and show that equation (17.2) predicts a measurable deviation.

Completing Program I does not complete Program II. Completing Program II requires Program I or another independently justified reference measure.

The two results cannot be obtained merely by defining one distribution as the Born distribution and another as its deviation.

18. A formal non-implication result

The present UPT foundations specify an admissibility equation and structural operators, but do not uniquely specify a probability measure over admissible phase configurations.

This gives a precise underdetermination argument.

Consider a finite set of admissible phase sectors

\mathcal S=\{\Phi_1,\Phi_2\}.

Suppose both satisfy the same admissibility constraints. The structural equations may distinguish their stability or observables, but no probability assignment follows unless a measure rule is added.

For example, both

\[
\mu^{(1)}(\Phi_1)=\frac12,
\qquad
\mu^{(1)}(\Phi_2)=\frac12
\tag{18.1}
\]

and

\[
\mu^{(2)}(\Phi_1)=\frac34,
\qquad
\mu^{(2)}(\Phi_2)=\frac14
\tag{18.2}
\]

are normalized measures on the same two-element set.

The equations of admissibility alone do not select one over the other.

This example does not claim that both measures satisfy every possible future UPT probability axiom. It shows that the current structural equation, by itself, is insufficient to determine the ensemble weights.

Theorem 4 — Probability underdetermination of the present structural axioms

The relation

\[
\mathscr F[\Phi;\lambda]=0,
\]

together with the definitions of \(\mathscr L_\Phi\), \boldsymbol\chi_\Phi, phase stability, and topological sector, does not by itself imply a unique probability measure over admissible configurations.

Proof. The admissibility equation determines a solution set

\[
\mathcal S_\Phi
=
\{\Phi\in\mathcal C_\Phi:
\mathscr F[\Phi;\lambda]=0\}.
\]

The definitions of the linearized operator and susceptibility constrain local response, while topological invariants classify configurations or sectors. None of these definitions assigns a normalized weight to each measurable subset of \mathcal S_\Phi. Distinct probability measures can therefore be defined on the same solution set unless further axioms or dynamical selection rules restrict them. The two-sector example (18.1)–(18.2) exhibits this nonuniqueness at the level of the structural equation. \square

The conclusion is methodological but strong: neither Born equilibrium nor quantum non-equilibrium is currently a theorem of the structural UPT axioms alone.

This is the central closure gap the next version of UPT must resolve.

⸻

Part VII. What would constitute a UPT derivation?

19. The missing phase-measure theorem

A complete derivation needs a measure assignment

\[
\mathfrak M:
(\mathcal C_\Phi,\mathscr G_\Phi,\mathscr F,\mathscr K)
\longrightarrow\mathcal P(\mathcal C_\Phi),
\tag{19.1}
\]

where \mathcal P(\mathcal C_\Phi) denotes a suitable space of probability measures.

The map \mathfrak M cannot be defined solely by the desired Born probabilities. It must be derived from independently stated phase-theoretic principles.

A candidate theorem would take the form:

Phase-measure reconstruction theorem. Under specified conditions of phase-frame invariance, branch additivity, composition consistency, continuity, and measurement-response compatibility, there exists a unique normalized phase measure whose induced outcome probabilities satisfy the Born rule.

This theorem is not established by the current UPT equations. Its assumptions must be stated precisely, and its uniqueness claim must be proved rather than inferred from the intended result.

The next task is therefore to construct the measure from the phase configuration space and show that the measurement kernel induces the required probability assignment.

20. The missing nonequilibrium-generation theorem

Even after the equilibrium measure is derived, the theory needs a mechanism that produces a physical measure different from it.

A candidate dynamical statement is

\[
\mu_0\neq\mu_{\mathrm{eq},0}.
\tag{20.1}
\]

But equation (20.1) is a hypothesis, not a derivation.

A stronger theorem would identify an admissible class of initial phase configurations and prove that a specified phase transition, boundary condition, or pre-equilibrium regime generates

\[
\mu_0=f_0\mu_{\mathrm{eq},0},
\qquad
f_0\neq1.
\tag{20.2}
\]

The mechanism must predict the functional form of f_0, or at least restrict it to a finite-dimensional family.

If arbitrary initial distributions are allowed, the theory can accommodate nonequilibrium but does not explain why a particular deviation occurs.

21. The missing observability theorem

The final closure condition is

\[
\exists(a,M):
\int K(a\mid\Phi,M)(f-1)\,
d\mu_{\mathrm{eq}}\neq0.
\tag{21.1}
\]

A complete theory must show that the physically generated nonequilibrium component lies outside the measurement-blind subspace.

This is an identifiability problem.

Let \mathcal V_{\mathrm{phys}} be the set of nonequilibrium perturbations generated by the theory’s allowed dynamics. The desired condition is

\[
\boxed{
\mathcal V_{\mathrm{phys}}
\cap\mathscr N_{\mathscr K}
=
\{0\}
}
\tag{21.2}
\]

for the measurement family used to establish the relevant form of non-equilibrium.

Equation (21.2) would ensure that no nonzero physically admissible deviation remains invisible to every measurement in that family.

In practice, full identifiability may be too strong for a finite apparatus. The weaker requirement is that the particular predicted perturbation be distinguishable from zero by at least one accessible observable, with a quantitatively adequate signal-to-noise ratio.

⸻

Part VIII. Experimental consequences

22. Deriving the measurable signal

For a specified nonequilibrium model, let

\[
f_\theta(\Phi)
=
1+\theta h(\Phi)+O(\theta^2),
\tag{22.1}
\]

where h is fixed by the model and \theta is a physical parameter.

Normalization requires

\[
\int h\,d\mu_{\mathrm{eq}}=0.
\tag{22.2}
\]

Substitution into equation (9.2) gives the first-order prediction

\[
\boxed{
\Delta P_a(M)
=
\theta
\int K(a\mid\Phi,M)h(\Phi)\,
d\mu_{\mathrm{eq}}
+O(\theta^2).
}
\tag{22.3}
\]

Define the response coefficient

\[
C_a(M)
=
\int K(a\mid\Phi,M)h(\Phi)\,
d\mu_{\mathrm{eq}}.
\tag{22.4}
\]

Then

\[
\Delta P_a(M)=\theta C_a(M)+O(\theta^2).
\tag{22.5}
\]

The experiment should be designed so that C_a(M) is nonzero and sufficiently large relative to statistical and systematic uncertainty.

A model that cannot calculate C_a(M) before data collection is not yet ready for a decisive test.

23. Polarization and interferometric tests

For a two-outcome measurement, write the predicted equilibrium probabilities as

P_{\mathrm B}(+|M)=p,
\qquad
P_{\mathrm B}(-|M)=1-p.

A normalized nonequilibrium perturbation must preserve total probability:

\[
\Delta P_+(M)+\Delta P_-(M)=0.
\tag{23.1}
\]

The measured deviation can therefore be parameterized as

\[
P_\theta(+|M)=p+\theta C(M)+O(\theta^2),
\tag{23.2}
\]

\[
P_\theta(-|M)=1-p-\theta C(M)+O(\theta^2).
\tag{23.3}
\]

Polarization experiments provide multiple measurement bases. Interferometric experiments provide controlled variations in relative phase, path structure, and detection geometry.

A UPT model should predict a common set of nonequilibrium parameters across these measurements. Independently fitting unrelated anomalies in each configuration would not establish a shared phase-distribution mechanism.

Three-path interference can provide an additional structural test. If the proposed UPT measurement model predicts a nonzero third-order interference term, that prediction must be derived explicitly. A nonzero term would not automatically identify the cause as quantum non-equilibrium; it would test a particular extension of the Born probability structure.

24. Statistical inference

For measurement settings M_j, outcomes a, and counts n_{aj}, let

N_j=\sum_a n_{aj}.

Assuming independent trials, the likelihood is

\[
\mathcal L(\theta,\boldsymbol\eta)
=
\prod_j
\frac{N_j!}{\prod_a n_{aj}!}
\prod_a
P(a|M_j,\theta,\boldsymbol\eta)^{n_{aj}},
\tag{24.1}
\]

where \boldsymbol\eta denotes nuisance parameters describing source imperfections, detector efficiencies, background events, and other systematic effects.

The null hypothesis is

\[
H_0:\theta=0,
\tag{24.2}
\]

and the alternative is

\[
H_1:\theta\neq0
\tag{24.3}
\]

within the specified UPT model.

The analysis should include:

* preregistered measurement settings and primary observables;
* a calibrated Born-equilibrium reference;
* blind analysis of the primary data;
* explicit modeling of systematic uncertainties;
* correction for multiple comparisons;
* parameter estimation and confidence intervals;
* independent replication;
* tests of the predicted dependence on measurement settings.

A statistically significant deviation is necessary for a positive experimental result, but not sufficient for identifying its physical cause.

The stronger result would be a replicated anomaly whose variation across independent observables agrees with the UPT-derived coefficients C_a(M).

25. The source and persistence problem

The experimental program also requires a physical source of nonequilibrium.

There are three broad possibilities.

A. A laboratory-prepared nonequilibrium ensemble. This requires a demonstrated mechanism that prepares a phase distribution distinct from the equilibrium measure. It cannot be assumed that ordinary quantum-state preparation provides such access.

B. A nonequilibrium distribution retained from an earlier dynamical regime. This requires a calculation of the distribution’s evolution and of its survival under phase mixing, environmental interactions, and finite detector resolution.

C. A primordial nonequilibrium distribution. This requires a model that connects early-universe phase dynamics to a present observable, such as a specified feature of primordial fluctuations. Cosmological anomalies alone would not establish this connection; the predicted signature must discriminate the model from competing explanations.

These possibilities are physically distinct. UPT must select or constrain the mechanism rather than treating them as interchangeable sources of the same desired outcome.

⸻

Part IX. Falsifiability and the logical ledger

26. The proof-status ledger

The present derivation yields the following classification.

Claim	Status	Required basis
Phase configurations obey an admissibility equation	Foundational UPT postulate	Explicit construction of \(\mathscr F\)
Stability is characterized by a linearized phase operator	Structural framework	Functional-analytic conditions on \(\mathscr L_\Phi\)
A distribution can differ from a reference probability measure	Proven mathematical possibility	Theorem 1
Such a deviation can be parameterized by f=d\mu/d\mu_{\mathrm{eq}}	Proven under absolute continuity	Radon–Nikodym theorem
A distributional deviation necessarily changes measured probabilities	False in general	Measurement-blindness proposition
Observable deviations obey equation (9.2)	Proven conditionally	A defined kernel and reference measure
The density ratio is transported by a common invertible phase flow	Proven conditionally	Theorem 3
The UPT foundations uniquely derive the Born measure	Not established	Phase-measure reconstruction theorem
UPT generates a physical distribution with f\neq1	Not established	Nonequilibrium-generation theorem
A generated deviation is experimentally accessible	Not established	Observability and identifiability theorem
Quantum non-equilibrium exists in nature	Open empirical question	Reproducible evidence and model discrimination

This ledger is part of the derivation, not an appendix to it. It prevents mathematical possibility from being mistaken for physical actuality.

27. Falsification conditions

The proposed UPT extension would be weakened or rejected in the following circumstances.

Failure of measure reconstruction. If the stated phase axioms admit multiple inequivalent probability measures and no additional physically justified principle selects the Born measure, UPT has not derived standard quantum probabilities.

Failure of nonequilibrium generation. If the specified dynamics preserve the equilibrium measure and no admissible source produces f\neq1, the proposed mechanism for generating nonequilibrium fails.

Failure of observability. If the predicted perturbation belongs to the measurement-blind subspace for every physically accessible measurement, the proposed experimental signature does not exist within that measurement theory.

Failure of quantitative prediction. If the model cannot calculate the sign, magnitude, and setting dependence of its deviation before data collection, it is not a decisive empirical alternative.

Experimental null result. If a sensitive experiment finds no deviation, the tested parameter range and model must be constrained. This does not rule out every conceivable nonequilibrium distribution, but it can falsify a specific model that predicted a detectable effect.

Failure of replication. If an apparent anomaly disappears under independent calibration or cannot be reproduced, it does not establish quantum non-equilibrium.

⸻

Part X. The complete conditional theorem

28. UPT quantum-non-equilibrium theorem

The preceding results can be consolidated into a single statement.

Theorem 5 — Conditional derivation of observable quantum non-equilibrium from a phase ensemble.

Let \mathcal C_\Phi be a measurable space of admissible UPT phase configurations, and suppose the following conditions hold.

1. Phase-to-quantum correspondence. A well-defined map \mathcal Q assigns emergent quantum states to admissible phase configurations.
2. Equilibrium-measure closure. A probability measure \mu_{\mathrm{eq}} and measurement-response kernel K satisfy the Born correspondence condition (6.1).
3. Physical nonequilibrium generation. A physical mechanism generates a normalized measure
    d\mu=f\,d\mu_{\mathrm{eq}},
    with f\geq0, \int f\,d\mu_{\mathrm{eq}}=1, and f\neq1 on a set of positive measure.
4. Observable identifiability. There exists an accessible outcome a and measurement M for which
    \int K(a\mid\Phi,M)(f-1)\,
    d\mu_{\mathrm{eq}}\neq0.
5. Dynamical persistence. The nonequilibrium component survives the physical evolution and detector coarse-graining sufficiently to retain the nonzero response in condition 4.

Then the observed probability differs from the Born prediction:

\[
\boxed{
P_\mu(a\mid M)
\neq
\langle\psi|E_a|\psi\rangle.
}
\tag{28.1}
\]

Proof. By condition 2,

\langle\psi|E_a|\psi\rangle
=
\int K(a\mid\Phi,M)\,d\mu_{\mathrm{eq}}.

By condition 3,

P_\mu(a\mid M)
=
\int K(a\mid\Phi,M)f\,d\mu_{\mathrm{eq}}.

Subtracting gives

P_\mu(a\mid M)-\langle\psi|E_a|\psi\rangle
=
\int K(a\mid\Phi,M)(f-1)\,
d\mu_{\mathrm{eq}}.

Condition 4 makes the right-hand side nonzero, while condition 5 ensures that the relevant deviation remains present at the actual measurement stage. Hence equation (28.1) follows. \square

The theorem establishes the logical sufficiency of the stated conditions. It does not establish that UPT already satisfies them.

In particular, conditions 2, 3, and 4 remain substantive derivation targets. The theorem is not a proof that nature contains quantum non-equilibrium. It is the precise theorem that a completed UPT model would need to instantiate to establish an observable departure from Born statistics.

⸻

Part XI. Research conclusions

29. What has been derived

The analysis establishes the following mathematical structure.

First, quantum non-equilibrium can be defined rigorously as a probability measure over admissible phase configurations that differs from a specified equilibrium reference.

Second, if the candidate measure is absolutely continuous with respect to the reference, its departure is characterized exactly by the density ratio f\neq1.

Third, the difference between equilibrium and nonequilibrium outcome probabilities is the response-weighted integral

\Delta P_a(M)
=
\int K(a\mid\Phi,M)(f-1)\,
d\mu_{\mathrm{eq}}.

Fourth, a distributional departure can remain unobservable if its component lies in the measurement-blind subspace.

Fifth, an invertible common phase flow transports the density ratio, while observable relaxation depends on mixing, coarse-graining, and the measurement response.

Sixth, the existing UPT structural equation does not uniquely determine a probability measure. A separate phase-measure reconstruction theorem is indispensable.

These are genuine mathematical conclusions. They establish the architecture of a rigorous UPT theory of quantum non-equilibrium without assuming that the desired physical result has already been demonstrated.

30. What remains to be derived

The central unresolved tasks are:

\boxed{
\begin{aligned}
&\text{Construct the phase measure},\\
&\text{derive Born-equilibrium statistics},\\
&\text{generate }f\neq1\text{ physically},\\
&\text{derive its dynamical evolution},\\
&\text{prove observational identifiability},\\
&\text{predict a reproducible experimental signature}.
\end{aligned}
}

The most important conceptual distinction is between a theory that permits non-equilibrium and a theory that predicts it.

A general phase configuration space may admit many measures. That fact does not establish that any particular nonequilibrium measure is physically realized. A model may contain phase information not represented in a Hilbert state. That fact does not establish that measurements can access the information. An observable anomaly may violate a Born-rule prediction. That fact does not uniquely identify the underlying mechanism as UPT.

Each inference requires its own derivation.

31. Final statement

Universal Phase Theory offers a possible foundation for treating probability as an emergent property of phase structure. Its central opportunity is to derive the relationship between phase configurations, statistical measures, and observable events from a common admissibility and dynamical framework.

Quantum non-equilibrium is a natural problem within that program because it asks whether the distribution of underlying phase configurations must coincide with the distribution inferred from the emergent quantum state.

The mathematical answer is conditional but exact:

\boxed{
\text{Observable quantum non-equilibrium}
\iff
\text{a physically generated phase-measure deviation has a nonzero measurable response}.
}

To elevate this statement from a conditional theorem to a physical derivation, UPT must establish the equilibrium measure, identify a mechanism that generates a distinct measure, derive its evolution, and show that its deviation survives into an experimentally accessible observable.

The correct next step is therefore not to declare quantum non-equilibrium proved. It is to close the phase-measure theorem and the nonequilibrium-generation theorem. Those are the missing mathematical gates between UPT’s phase-first ontology and an experimentally testable claim about quantum probability.

If those gates can be passed without inserting the Born rule or the desired deviation into the premises, quantum non-equilibrium would become a derived and falsifiable consequence of the theory rather than an additional assumption.

Until then, the derivation establishes mathematical possibility, conditional consequences, and a precise research program—not the empirical existence of quantum non-equilibrium.
