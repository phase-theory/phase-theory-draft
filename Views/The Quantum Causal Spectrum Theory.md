The Quantum Causal Spectrum Theory

Spectral Invariants of Lorentzian Causality, Quantum Propagation, and Representation-Stable Physical Observables

Research preprint · October 24, 2026

Abstract

The Quantum Causal Spectrum Theory (QCST) investigates whether the causal structure of a Lorentzian spacetime and the propagation of quantum fields upon it can be characterized by a common family of spectral invariants. Its central premise is that causal relations and quantum propagation, although mathematically distinct, encode overlapping information about which events can influence which others, how disturbances propagate, and how spacetime geometry constrains the support and singularity structure of quantum correlations.

The central difficulty is structural. Riemannian spectral geometry often relies on positive elliptic operators with discrete spectra, whereas Lorentzian wave operators are typically hyperbolic, indefinite in their natural geometric formulation, and potentially endowed with continuous spectrum. Their spectral behavior depends on global causal properties, boundary conditions, state selection, and the choice of operator realization. Consequently, a causal spectrum cannot be defined merely by replacing a Riemannian Laplacian with a Lorentzian wave operator.

This paper develops a mathematically controlled research framework. It defines a causal relation operator on a globally hyperbolic spacetime, constructs a bounded integral operator from its causal ordering, distinguishes this operator from the quantum causal propagator, and identifies conditions under which their spectral data can be related to quantum-field observables. The framework uses compactly supported localization, operator ideals, resolvent and singular-value invariants, and the microlocal structure of two-point functions. A conditional theorem establishes that, under explicit assumptions connecting the causal operator to a localized quantum response operator, stability of the causal invariant implies stability of specified measurable propagator observables. A complementary obstruction result shows why causal support alone generally cannot determine the full quantum propagator.

The resulting theory does not assert that a universal causal spectrum has already been discovered. Instead, it provides definitions, conditional results, failure criteria, and a testable path from Lorentzian causal order to spectral data and then to quantum propagation. The principal research question is whether one can identify nontrivial spectral invariants that remain stable under changes of representation while retaining experimentally accessible information about quantum-field propagation.

Keywords: Lorentzian geometry; causal order; quantum field theory in curved spacetime; causal propagator; spectral invariants; microlocal analysis; hyperbolic operators; Green functions; representation stability.

1. Introduction: The spectral content of causality

The geometry of a Lorentzian spacetime determines which events can causally influence which others. For events , the relation

x\preceq_g y

means that lies in the causal future of , subject to the convention that the relation includes equality. In a time-oriented spacetime, this relation is encoded by the causal future and past,

J^+(x),\qquad J^-(x).

Quantum field theory introduces a second description of propagation. A field equation determines a differential operator, while its retarded, advanced, and causal Green operators encode how sources affect fields. For a free scalar field, a representative operator is

P_g=\Box_g+m^2+\xi R_g,

where is the Lorentzian d’Alembertian, is the mass parameter, is a curvature coupling, and is the scalar curvature. Sign conventions for and the mass term vary; throughout this paper, the sign convention is chosen so that is a normally hyperbolic operator up to the indicated lower-order terms.

When suitable retarded and advanced Green operators exist, write

G_{\mathrm{ret}},\qquad G_{\mathrm{adv}}.

The causal propagator is defined by

E=G_{\mathrm{ret}}-G_{\mathrm{adv}}.

Its distributional kernel is supported on causal influence: it vanishes when its arguments are causally unrelated in the appropriate sense. Yet the causal propagator is not the same object as a positive-frequency two-point function, a Feynman propagator, or a detector response. These objects encode different combinations of causal dynamics and quantum state information.

QCST asks whether a suitably defined spectral object can connect these descriptions without erasing their distinctions.

The research problem has three layers:

* Causal layer: encode causal relations in an operator or operator family.
* Quantum layer: encode propagation in a Green operator or quantum correlation kernel.
* Invariant layer: identify spectral quantities that transform predictably under changes of representation and correlate with measurable propagation.

A successful theory must specify the operators, their domains, their spectral notions, the allowed transformations, and the observable quantities before asserting any relation between them.

1.1 The central hypothesis

Let denote a causal operator constructed from the causal structure of , and let denote a localized quantum propagation operator associated with the field dynamics and state .

The central hypothesis is that there may exist a map

\mathcal I:
\operatorname{Spec}(\mathfrak C)
\longrightarrow
\mathcal O_{\mathrm{prop}},

where is a collection of invariant or measurable properties of quantum propagation.

The hypothesis is deliberately weaker than a claim that the causal spectrum uniquely determines the propagator. Such uniqueness would generally require additional information about the field equation, the quantum state, boundary conditions, and the spacetime’s global structure.

1.2 The standard of success

The theory will count as successful only if it provides:

* a mathematically well-defined causal operator;
* spectral invariants that are not artifacts of arbitrary normalization or representation;
* a specified quantum propagator observable;
* a theorem connecting the causal invariant to that observable;
* a clear statement of the assumptions under which the theorem holds;
* and a counterexample or no-go criterion identifying when the proposed connection fails.

A spectral resemblance between two operators is not enough. Nor is reproducing a known geometric quantity sufficient unless the quantum-propagation relation supplies additional explanatory or predictive content.

2. Mathematical setting and conventions

Let be a smooth, time-oriented, globally hyperbolic Lorentzian manifold of dimension , with metric signature . Global hyperbolicity is adopted initially because it supplies a well-controlled causal structure and, for normally hyperbolic operators, well-posed Cauchy evolution and unique advanced and retarded Green operators under standard hypotheses.

Let denote the positive Lorentzian volume density. The space consists of smooth compactly supported test functions, and denotes distributions.

For the scalar field, define

P_g=\Box_g+m^2+\xi R_g,

with the understanding that the signs of and the mass term are fixed consistently with the chosen convention for the Klein–Gordon equation. The causal propagator is

E_g=G_{\mathrm{ret}}-G_{\mathrm{adv}}.

For test functions , the bilinear pairing

E_g(f,h)

\int_M f(x)(E_gh)(x)\,d\mu_g(x)

is well-defined under the standard distributional interpretation.

The causal propagator defines the commutator structure of the free field. In a common convention,

\\widehat\\phi(f),\\widehat\\phi(h)

i\,E_g(f,h)\,\mathbf 1,

up to an overall factor of depending on the normalization of the field and propagator. This relation is fundamental: the commutator is fixed by the field equation and causal dynamics, whereas the symmetric two-point correlations depend on the chosen state.

For a suitable state , define the two-point distribution

W_\omega(x,y)

\omega\!\left(\widehat\phi(x)\widehat\phi(y)\right).

For a free scalar field in a Hadamard state, has a prescribed short-distance singularity structure. In particular, its wavefront set is constrained by the null-geodesic flow and time orientation. This provides an established microlocal bridge between spacetime causality and quantum correlations. QCST seeks to complement, not replace, that bridge with spectral information.

The distinction between causal response and state-dependent quantum correlations is essential to the theory. Standard results on globally hyperbolic spacetimes establish the support properties of advanced and retarded Green operators, while microlocal analysis constrains the singularities of physically admissible two-point functions. QCST builds upon these results by asking which aspects of this information can be compressed into a stable spectral signature.

A closely related research direction already exists: work presented at the Perimeter Institute in May 2026 discusses spectral densities of causal propagators in continuum and causal-set settings, including a conjecture for their asymptotic behavior. This makes it particularly important to formulate QCST as a precise program of invariant construction and theorem proving, rather than to claim that the idea of studying causal-propagator spectra is itself unprecedented.

3. Why ordinary spectral geometry does not transfer directly

On a compact Riemannian manifold, the Laplace–Beltrami operator

-\Delta_g

is a positive elliptic operator under its standard self-adjoint realization. Its spectrum is discrete, subject to multiplicities, and its eigenvalue asymptotics encode geometric information through Weyl-type laws and heat-kernel coefficients.

A Lorentzian wave operator has a different mathematical character. In local coordinates, its principal symbol is proportional to

p_g(x,\xi)=g^{\mu\nu}(x)\xi_\mu\xi_\nu.

Because is indefinite, vanishes on a nontrivial null cone in cotangent space. The operator is hyperbolic, not elliptic. On a noncompact spacetime or a spacetime with noncompact Cauchy surfaces, the relevant spectrum may be continuous; on other domains, boundary conditions and operator realizations may alter the spectral problem.

Three common but invalid shortcuts must therefore be excluded.

Shortcut A: treating the Lorentzian wave operator as a positive elliptic operator. Its principal symbol and energy structure do not support that substitution.

Shortcut B: assuming every causal propagator has a discrete eigenvalue sequence. The causal propagator is naturally a distributional operator between test-function and solution spaces; it need not be a compact operator on a canonical Hilbert space.

Shortcut C: interpreting an arbitrary spectrum as an observable. A spectrum can depend on the chosen function space, inner product, regulator, boundary conditions, and operator normalization. A physical invariant must specify which changes leave its meaning unchanged.

QCST therefore begins not with the spectrum of on an unspecified domain, but with explicitly defined causal and quantum operators whose boundedness and spectral properties can be established.

4. A causal relation operator

4.1 From causal order to a measurable kernel

Let be a relatively compact, causally well-behaved region. Assume its closure is contained in a globally hyperbolic neighborhood and that the induced causal relation is measurable.

Choose a smooth, nonnegative localization weight supported in . Define a finite measure

d\nu_\rho(x)=\rho(x)\,d\mu_g(x).

For a fixed time orientation, define the future-order kernel

K_g(x,y)=
\begin{cases}
1, & x\preceq_g y,\\
0, & \text{otherwise}.
\end{cases}

The associated causal integral operator is

(\mathfrak C_{g,\rho}f)(x)

\int_\Omega K_g(x,y)f(y)\,d\nu_\rho(y).

The direction of the kernel is a convention: reversing the time orientation exchanges future and past ordering. The choice must be fixed when comparing operators.

This definition is intentionally simple. It converts a causal relation into an integral operator while leaving the quantum field equation out of the construction. The causal kernel depends on causal order and the chosen measure, not on a quantum state.

4.2 Boundedness and compactness

Since is bounded and , the kernel belongs to

L^2(\Omega\times\Omega,
d\nu_\rho\otimes d\nu_\rho).

Consequently, is a Hilbert–Schmidt operator on , with

\|\mathfrak C_{g,\rho}\|_{\mathrm{HS}}^2

\int_{\Omega\times\Omega}
|K_g(x,y)|^2\,d\nu_\rho(x)d\nu_\rho(y).

In particular, it is bounded and compact. Its Hilbert–Schmidt norm is finite.

This is a genuine spectral construction, but its interpretation requires care. The norm is the measure of the ordered pairs in , weighted by the chosen localization density. It is not a universal scalar invariant of the spacetime independent of localization.

The compactness of guarantees a well-defined sequence of singular values

s_1(\mathfrak C_{g,\rho})
\geq
s_2(\mathfrak C_{g,\rho})
\geq\cdots\geq 0,
\qquad
s_j\to0,

counted with multiplicity. These singular values are robust candidates for the causal spectrum, provided the localization prescription and the transformation law are made explicit.

The operator need not be self-adjoint. Indeed, for a time-oriented kernel, the future relation is generally not symmetric. Its eigenvalues can therefore be complex, and singular values may be more stable than eigenvalues under perturbations. This distinction will be retained throughout the paper.

4.3 What the causal operator does—and does not—encode

The operator encodes a weighted version of causal precedence. It does not, by itself, encode the complete Lorentzian metric.

The causal order of a sufficiently regular, time-oriented Lorentzian spacetime constrains the conformal geometry. Recovering the full metric also requires a volume element or equivalent scale information under appropriate hypotheses. In the present construction, the measure mixes geometric volume with the externally selected weight . Thus, an inverse theorem must distinguish causal information from information introduced by the localization prescription.

We will use the phrase causal spectral signature for a family of invariants extracted from , with the region, measure, and normalization included as part of the signature’s definition.

5. Three distinct spectral objects

QCST must not collapse three different operators into one.

Object I — Causal-order operator

\mathfrak C_{g,\rho}

Constructed from the causal relation. It contains no mass parameter or quantum state unless those are added by a separate construction.

Object II — Causal propagator

E_g=G_{\mathrm{ret}}-G_{\mathrm{adv}}

Determined by the field operator and causal Green-function problem. Its kernel is distributional and is naturally defined before a Hilbert-space spectral realization is chosen.

Object III — Quantum two-point function

W_\omega(x,y)

Encodes state-dependent correlations. Its commutator part is constrained by , but the full two-point function is not fixed by causal order alone.

The first object is introduced to create a bounded spectral problem. The second expresses the causal dynamics of the field. The third supplies the state-dependent information required for quantum fluctuations and many operational predictions.

The central task is to establish a mathematically controlled map between these objects—not to identify them by definition.

6. Localized causal-propagation operators

A direct spectral analysis of is complicated by its distributional nature. We therefore introduce localization and regularization explicitly.

Let be real-valued switching functions or detector profiles. The localized causal response is the bilinear functional

\mathcal R_g(a,b)

\int_\Omega\int_\Omega
a(x)E_g(x,y)b(y)\,
d\mu_g(x)d\mu_g(y),

understood as the distributional pairing of with the smooth compactly supported product .

This quantity is well-defined under the usual distributional hypotheses. It is also directly connected to the field commutator, and hence to the response of the field algebra to localized test-function smearings.

To obtain a bounded operator suitable for spectral comparison, introduce a smoothing map

S_\epsilon:C_c^\infty(\Omega)\to L^2(\Omega,d\nu_\rho),
\qquad \epsilon>0,

with a smooth integral kernel and a specified normalization. Define

\mathfrak Q_{\epsilon}

S_\epsilon E_g S_\epsilon^*,

whenever the chosen smoothing and duality conventions make this composition well-defined. More generally, if the causal propagator is represented between Sobolev spaces, one may use smoothing maps on both sides to obtain a bounded operator on a chosen Hilbert space.

The operator is not a unique canonical object. It depends on the smoothing prescription, the localization region, and the chosen function-space realization. QCST must therefore prove either:

* convergence of its proposed invariants as , in a specified topology; or
* stability of the invariants across a clearly defined class of admissible smoothing prescriptions.

Without such a result, the regularized spectrum is a property of the measurement or regulator scheme, not a regulator-independent property of spacetime.

6.1 State-dependent propagation

For a quantum state , the corresponding localized two-point operator can be written formally as

\mathfrak W_{\omega,\epsilon}

S_\epsilon W_\omega S_\epsilon^*,

again with the precise domain and pairing fixed by the chosen representation. The regularization can render the operator bounded or compact under appropriate conditions, but these properties must be proved for the chosen setup rather than assumed universally.

The relation between and reflects the commutator identity. In a fixed convention,

W_\omega(x,y)-W_\omega(y,x)

\pm iE_g(x,y),

with the sign determined by the field-commutator convention. Hence the antisymmetric part of the two-point function is fixed by causal dynamics, whereas its symmetric part contains state-dependent information.

This separation is a fundamental limitation on any proposed theorem: a causal invariant can constrain commutator-related propagation data without uniquely determining the full quantum state.

7. Defining a representation-stable causal spectrum

A spectrum is meaningful only relative to a class of representations and a specified equivalence relation.

Let . Suppose two representations of the same causal data are related by a unitary map

U:\mathcal H_\rho\to\mathcal H_{\rho’}.

If the represented operators satisfy

\mathfrak C’ = U\mathfrak C U^{-1},

then their spectra, singular values, and operator norms agree. This is the simplest representation-invariance result, and it is a standard consequence of unitary equivalence.

But different localization measures may change the operator itself rather than merely its representation. A change of density can be transferred to an unweighted space by a unitary multiplication map only when the measures are related appropriately and the operator kernel is transformed consistently. If the measure change modifies the physical weighting, unitary equivalence need not hold.

7.1 Invariant candidates

The following quantities form a hierarchy of possible invariants.

(i) Singular-value sequence

\Sigma_{\mathrm{sv}}(\mathfrak C)

\{s_j(\mathfrak C)\}_{j\ge1}.

This is invariant under unitary equivalence. It is stable under norm perturbations in standard operator settings, although individual singular-value comparisons must be stated with their relevant hypotheses.

(ii) Schatten moments

For such that ,

M_p(\mathfrak C)

\operatorname{Tr}\!\left\[
(\\mathfrak C^\*\\mathfrak C)^{p/2}
\\right\]

\sum_j s_j(\mathfrak C)^p.

For , this is the squared Hilbert–Schmidt norm. Higher moments emphasize different parts of the singular-value distribution.

(iii) Resolvent data

Where the resolvent exists,

R_{\mathfrak C}(z)

(zI-\mathfrak C)^{-1}.

Resolvent norms and suitably defined spectral measures can be useful when eigenvalues are unstable. Since may be non-normal, its resolvent can be large far from its spectrum. That pseudospectral sensitivity is physical or numerical information to analyze, not a detail to discard.

(iv) Regularized determinant data

For an appropriate Schatten-class operator and a compatible determinant prescription, one may define a regularized determinant

\det\nolimits_p(I-z\mathfrak C).

Its zeros and analytic behavior encode spectral information, but its existence and invariance depend on the operator class and the determinant normalization.

No single member of this list is automatically the correct physical invariant. QCST should select invariants according to a stated theorem and an operational target, not merely because they are mathematically available.

8. The causal–quantum correspondence problem

The principal mathematical question can now be stated precisely.

Given a localized causal-order operator and a regularized causal-propagation operator , can one find a map such that

\mathfrak Q_\epsilon
\approx
\mathcal F(\mathfrak C)

in a topology strong enough to control physically relevant observables?

In general, this cannot hold as a universal exact identity. The causal-order operator contains no field mass, curvature coupling, gauge representation, or quantum-state choice. The propagator depends on the field operator, while state-dependent correlators require still more information. Distinct field theories can inhabit the same spacetime and share the same causal order while having different propagation kernels.

The appropriate target is therefore a conditional correspondence. We seek a class of theories , a fixed localization and regularization scheme, and a family of propagation observables for which the causal spectrum constrains a measurable quantity.

Let

\mathbf I_C

\big(I_1(\mathfrak C),\ldots,I_r(\mathfrak C)\big)

be a finite vector of causal spectral invariants, and let

\mathbf O_Q

\big(O_1(\mathfrak Q_\epsilon),\ldots,
O_s(\mathfrak Q_\epsilon)\big)

be a vector of quantum-propagation observables. A target relation takes the form

\mathbf O_Q

\mathcal F_{\mathfrak T}
(\mathbf I_C;\boldsymbol\theta)
+\boldsymbol\varepsilon,

where denotes independently specified field parameters and represents a controlled approximation error.

This equation is a research ansatz, not a theorem. The substantive work is to establish the map , determine the admissible parameters, bound the error, and prove that the result is not merely a restatement of the field equation.

8.1 What could be predicted?

Potential targets include:

* norms of localized retarded responses;
* singular values of a regularized commutator operator;
* frequency-resolved detector response under a fixed state prescription;
* spectral densities of causal propagators;
* propagation-tail amplitudes in specified geometric regimes;
* stability of response observables under controlled geometric perturbations.

These quantities differ in their physical interpretation. A detector transition probability, for example, depends on its coupling, switching function, trajectory, and quantum state; it cannot be equated with a causal spectral invariant without accounting for these additional inputs.

8.2 A necessary distinction: support versus amplitude

Causal order determines whether a signal can propagate between two events. It does not, by itself, determine the amplitude, phase, polarization, or frequency dependence of that propagation.

For a normally hyperbolic scalar equation, the singular support of a Green kernel is constrained by null propagation, while curvature and lower-order terms can affect transport coefficients and interior tails. The causal relation constrains the propagation domain; the differential operator determines more detailed dynamics.

The distinction is illustrated locally by a Hadamard representation of a retarded Green function. In four spacetime dimensions, under appropriate local hypotheses and convention choices, it takes the schematic form

G_{\mathrm{ret}}(x,x’)

\Theta_+(x,x’)
\leftU(x,x')\\delta(\\sigma(x,x'))
+
V(x,x')\\Theta(-\\sigma(x,x'))
\\right,

where is Synge’s world function, is the null-cone coefficient, and is the tail term. The causal cone determines where the direct singular contribution can occur, but the coefficients depend on the field operator and geometry.

QCST must therefore seek spectral information that captures more than the existence of causal influence.

9. A conditional stability theorem

We now state a theorem that can be proved at the level of bounded operators and that isolates the additional hypothesis needed for physical interpretation.

Definition 9.1 — Causal spectral signature

Let be a compact causal-order operator on a Hilbert space . For a fixed integer , define the truncated signature

\mathbf I_r(\mathfrak C)

\big(s_1(\mathfrak C),\ldots,s_r(\mathfrak C)\big).

The truncation is operationally useful when only a finite portion of the singular spectrum can be estimated. It is not assumed to be a complete invariant of the causal structure.

Definition 9.2 — Localized propagation observable

Let be a bounded operator on a Hilbert space , constructed from a fixed field theory, state prescription if relevant, localization, and smoothing procedure. Let

\mathcal O:\mathcal B(\mathcal H_Q)\to\mathbb R

be a Lipschitz-continuous observable on a specified operator class, with

|\mathcal O(A)-\mathcal O(B)|
\le L_{\mathcal O}\|A-B\|.

Examples may include the norm of a bounded response operator or a bounded functional of its matrix elements. A detector probability is covered only after its measurement model has been translated into such an operator functional and the relevant assumptions have been verified.

Theorem 9.1 — Conditional stability of causal spectral predictions

Let be compact operators on a common Hilbert space, and let be bounded localized propagation operators. Assume:

1. Causal perturbation control. The causal operators satisfy \|\\mathfrak C_1-\\mathfrak C_2|\\le\\delta. \\

2. Quantum correspondence. There exists a fixed map , defined on the relevant causal-operator class, such that \|\\mathfrak Q_i-\\mathcal F(\\mathfrak C_i)| \\le\\eta_i,\\qquad i=1,2. \\

3. Lipschitz correspondence. The map obeys \\[ |\\mathcal F(A)-\\mathcal F(B)| \\le L_{\\mathcal F}|A-B| \\\] on that class.

4. Observable continuity. is Lipschitz-continuous with constant on a set containing the relevant propagation operators.

Then

\boxed{
\left|\mathcal O(\mathfrak Q_1)
-\mathcal O(\mathfrak Q_2)\right|
\le
L_{\mathcal O}
\left(
L_{\mathcal F}\delta+\eta_1+\eta_2
\right).
}

Proof

By the triangle inequality,

\begin{aligned}
\|\mathfrak Q_1-\mathfrak Q_2\|
&\le
\|\mathfrak Q_1-\mathcal F(\mathfrak C_1)\|\\
&\quad+
\|\mathcal F(\mathfrak C_1)
-\mathcal F(\mathfrak C_2)\|\\
&\quad+
\|\mathcal F(\mathfrak C_2)-\mathfrak Q_2\|\\
&\le
\eta_1+L_{\mathcal F}\delta+\eta_2.
\end{aligned}

Applying the Lipschitz bound for gives the claimed inequality.

Interpretation

The theorem establishes a rigorous stability statement: if the causal operators are close, if a physically justified correspondence exists and is stable, and if the correspondence error is controlled, then the selected propagation observable is stable.

The theorem does not establish the correspondence itself. The nontrivial physical burden is assumption 2, together with the derivation of the map and its domain. A theory that simply postulates to fit observed propagation would not have solved the causal-spectrum problem.

The result becomes scientifically substantive when is derived from the field equation, the causal construction, and independently fixed physical parameters, with bounds that remain valid under a meaningful class of geometric perturbations.

10. A spectral perturbation corollary

For compact operators on a common Hilbert space, the singular values satisfy the standard perturbation estimate

|s_j(A)-s_j(B)|\le \|A-B\|

for each , under the usual ordering of singular values.

Corollary 10.1 — Stability of a finite causal signature

Under the causal perturbation hypothesis of Theorem 9.1,

\left\|
\mathbf I_r(\mathfrak C_1)

\mathbf I_r(\mathfrak C_2)
\right\|_{\infty}
\le\delta.

Thus, if the causal-order operator changes by at most in operator norm, every retained singular value changes by at most .

This is a mathematical stability result for the chosen operator realization. It is not yet a theorem about perturbations of the spacetime metric: a separate geometric estimate is needed to bound

\|\mathfrak C_{g_1,\rho_1}
-\mathfrak C_{g_2,\rho_2}\|

in terms of a metric difference. Such a bound is nontrivial because a small metric perturbation can alter causal relations near null boundaries. Changes in the indicator kernel need not be uniformly small even when the metric is close in a conventional smooth topology.

The corollary is therefore a first stage in the argument, not its completion.

11. A no-go result: causal order cannot determine the full quantum propagator

The central correspondence hypothesis must be constrained by a simple obstruction.

Theorem 11.1 — Field-parameter obstruction

Let be fixed and globally hyperbolic. Consider two scalar field operators

P_{m_1,\xi_1}

\Box_g+m_1^2+\xi_1R_g,P_{m_2,\xi_2}

\Box_g+m_2^2+\xi_2R_g,

for parameter choices that yield well-defined advanced and retarded Green operators. If their causal propagators differ,

E_{m_1,\xi_1}\ne E_{m_2,\xi_2},

then no map depending only on the causal order of can determine both causal propagators uniquely.

Proof

The causal order of the spacetime is identical for the two theories because the background causal structure is unchanged. Any function of that causal order alone therefore has the same value for both theories. If the causal propagators differ, that function cannot equal both propagators. Hence causal order alone is insufficient.

The theorem is elementary, but its implications are fundamental. It rules out a universal reconstruction of the full quantum propagator from an unadorned causal-order spectrum.

It does not rule out more restricted results. For example, a causal signature augmented with field mass, curvature coupling, operator class, and boundary or state data might constrain propagation in a specified model family. But the additional data must be named explicitly and must not be hidden inside an allegedly universal causal invariant.

11.1 State dependence supplies a second obstruction

Even with the field equation and causal propagator fixed, multiple admissible quantum states can have different two-point functions. For a free field, the antisymmetric part is fixed by the commutator, while the symmetric part may vary across states.

Therefore,

\text{causal order}
\not\Rightarrow
\text{unique propagator}
\not\Rightarrow
\text{unique quantum state}.

The first non-implication follows from the field-parameter obstruction. The second follows from the state freedom of quantum field theory. A valid QCST result must specify whether it concerns causal response, commutator spectra, state-dependent correlations, or a restricted observable derived from them.

12. The microlocal bridge: null propagation and quantum singularities

The most established bridge between Lorentzian causality and quantum propagation is microlocal rather than purely spectral.

For a normally hyperbolic operator, the principal symbol defines the characteristic set

\operatorname{Char}(P_g)

\{(x,\xi)\in T^*M\setminus 0:
g^{\mu\nu}(x)\xi_\mu\xi_\nu=0\}.

The characteristic covectors are null. The Hamiltonian flow generated by the principal symbol transports singularities along null bicharacteristics, which project to null geodesics under the standard geometric assumptions.

For a Hadamard two-point function , its wavefront set has a constrained form determined by pairs of points connected by null geodesics, together with a time-orientation condition. This is not an ordinary eigenvalue spectrum. It is directional information in cotangent space that specifies where the distribution fails to be smooth and in which covector directions its singularities occur. The microlocal Hadamard condition is a central result in quantum field theory on curved spacetime.

QCST should treat this structure as an established baseline. The proposed spectral invariant should ideally add one or more of the following:

* a quantitative measure of causal propagation beyond the location of singular support;
* a stable compression of propagation data under a specified family of representations;
* a relation between spectral density and an operationally measurable response;
* a new inverse or stability theorem that cannot be obtained directly from existing microlocal propagation results.

A spectrum that merely re-encodes the null characteristic set without additional quantitative content would be mathematically interesting but would not, by itself, establish a new theory of quantum propagation.

13. Spectral density of the causal propagator

A more direct QCST branch studies the spectrum of a causal propagator or a regulated version of it. This is distinct from the causal-order operator defined in Section 4.

Suppose a model supplies a Hilbert-space realization of the causal propagator, with a specified regularization or finite-volume prescription. If is compact, its singular-value counting function can be defined by

N_{\mathfrak E}(s)

\#\{j:s_j(\mathfrak E)>s\},
\qquad s>0.

If an appropriate spectral measure exists in a noncompact setting, one may instead study a density per unit spacetime volume or a density relative to a specified limiting procedure. The choice of definition is part of the mathematical model.

An asymptotic law such as

N_{\mathfrak E}(s)
\sim C\,s^{-\alpha}
\qquad (s\downarrow0)

would describe the accumulation of small singular values. The exponent and coefficient may depend on spacetime dimension, operator order, regularization, domain, and geometric scale. They cannot be presumed universal.

This approach is especially relevant because research on the spectral density of causal propagators has already formulated asymptotic conjectures in continuum and causal-set contexts. QCST’s contribution would need to be a specific theorem, a rigorously established relation to measured propagation, a sharper stability statement, or a demonstrated extension to a clearly defined model class.

13.1 Why the spectrum requires a realization

A distributional kernel does not automatically define a compact operator on . In infinite spacetime volume, even boundedness may fail for a naive realization. A spectral density also cannot be defined unambiguously without specifying how volume limits, cutoffs, and operator normalization are handled.

A defensible spectral-density theorem must state:

* the operator domain and target space;
* the regularization and its normalization;
* the limiting procedure, if any;
* the order of the large-volume and short-distance limits;
* the class of geometries and field operators;
* and the sense in which the asymptotic law is uniform.

These are not technical afterthoughts. They determine what the spectrum means.

14. A concrete test model: flat spacetime

Any proposed causal spectral theory should begin with a model in which the causal structure and field propagator are independently known.

Consider a bounded region of -dimensional Minkowski spacetime, with its standard causal order. Choose a smooth compactly supported localization weight and construct

\mathfrak C_{\eta,\rho}f(x)

\int_\Omega
\mathbf 1_{\{y\in J^-(x)\}}f(y)\,d\nu_\rho(y).

This operator is Hilbert–Schmidt by the argument in Section 4. Its singular-value sequence is therefore well-defined.

Now choose a Klein–Gordon field with mass . Its causal propagator is determined by

P_m=\Box_\eta+m^2

under the fixed sign convention. The massless and massive theories share the same background causal order but have different propagation kernels in general.

This supplies an immediate benchmark:

* The causal-order operator is unchanged when the mass changes.
* The field propagator changes with the mass.
* Therefore, a mass-independent causal spectrum cannot uniquely determine the full propagator.
* A useful spectral correspondence must either target a mass-independent feature, include as an independent input, or restrict itself to a narrower model family.

14.1 A dimensionless spectral normalization

The raw singular values of depend on the measure and its overall scale. If the measure is rescaled by

d\nu_\rho\longmapsto a\,d\nu_\rho,
\qquad a>0,

then the integral operator is rescaled by , so all singular values are rescaled by the same factor. This makes raw spectral magnitudes unsuitable as scale-free invariants.

A candidate normalization is

\widehat{\mathfrak C}

\frac{\mathfrak C}{\|\mathfrak C\|_{\mathrm{HS}}},

provided . Then

\|\widehat{\mathfrak C}\|_{\mathrm{HS}}=1.

This removes one overall amplitude scale but does not remove dependence on the shape of , the localization region, or the causal geometry. Nor does it preserve every physically meaningful scale. QCST should therefore retain both the normalized shape spectrum and the dimensional normalization, rather than treating normalization as a substitute for a physical model.

14.2 The flat-space validation sequence

A minimal computational study should proceed in the following order:

* Choose a bounded causal diamond with a specified coordinate representation.
* Sample events according to a declared sampling measure.
* Construct the discrete causal-order matrix .
* Compute its singular values and test convergence under increased sampling density.
* Construct a discretized causal propagator for several independently specified masses.
* Apply a fixed regularization and localization prescription.
* Compare the causal and propagation spectra without tuning the field parameters to enforce agreement.
* Test whether any proposed spectral relation predicts a response observable not used in its construction.

A finite causal matrix is a numerical approximation to the specified causal-order operator, not automatically a faithful discretization of a continuum Lorentzian wave operator. The two approximations require separate convergence analyses.

15. A discrete realization and continuum limit

A discrete setting may help isolate which aspects of the proposed theory are algebraic and which depend on smooth geometry.

Let be the adjacency matrix of a finite causal order on sampled events, with

(C_N)_{ij}

\begin{cases}
1,&x_i\preceq x_j,\ i\ne j,\\
0,&\text{otherwise}.
\end{cases}

The diagonal is set to zero here to avoid including reflexive relations in the adjacency matrix. Other conventions are possible, but they must be fixed consistently.

The matrix is generally non-symmetric. Its eigenvalues need not be real, and eigenvalues alone may be unstable under perturbations. Its singular values,

s_1(C_N)\ge\cdots\ge s_N(C_N)\ge0,

are well-defined and can be compared across finite models.

However, the raw singular values scale with and with the sampling density. A continuum comparison requires a normalization and a sampling scheme derived from the intended continuum operator. One possible objective is to show convergence of empirical singular-value distributions after normalization:

\mu_N

\frac1N\sum_{j=1}^N
\delta_{\lambda_j^{(N)}},

where denotes a chosen normalized spectral quantity. If singular values rather than eigenvalues are used, the corresponding measure should be defined over instead.

A continuum theorem would need to specify the mode of convergence—weak convergence of measures, convergence of individual leading singular values, convergence in an operator ideal, or another well-defined notion. Different forms of convergence preserve different information.

15.1 A discrete propagator is a second construction

To test quantum propagation, the causal set or discrete event structure must also support a defined discrete wave operator or causal propagator. Let denote such an object when its construction has been specified.

It is not enough to choose by an arbitrary matrix formula and then observe a correlation between its spectrum and that of . The discrete dynamics must be independently motivated, and its continuum behavior must be established or tested against a known target.

The research problem is to determine whether a suitably normalized spectral signature of constrains the response encoded by , with errors that can be controlled as .

This approach offers a practical route to falsification. If no stable relation survives changes in sampling density, regulator, or admissible discretization, then the proposed invariant is not robust enough for the intended continuum interpretation.

16. Beyond eigenvalues: response signatures

Eigenvalues are not always the most informative spectral data for non-self-adjoint operators. Two non-normal operators can have similar eigenvalues but very different resolvent behavior, transient amplification, or singular-value distributions.

QCST should therefore compare a family of response signatures rather than a single eigenvalue list.

For a bounded propagation operator , candidate descriptors include:

\begin{aligned}
\mathcal S_1(\mathfrak Q)&=\|\mathfrak Q\|,\\
\mathcal S_2(\mathfrak Q)&=\|\mathfrak Q\|_{\mathrm{HS}},
\\
\mathcal S_3(\mathfrak Q)&=
\big(s_1(\mathfrak Q),\ldots,s_r(\mathfrak Q)\big),
\\
\mathcal S_4(\mathfrak Q;z)&=
\|(zI-\mathfrak Q)^{-1}\|,
\end{aligned}

where each expression is used only when the corresponding operator class and inverse exist.

The resolvent signature is particularly delicate. It may reveal strong sensitivity even when the eigenvalues barely move. But it can also be highly dependent on the chosen representation and norm. Any claimed invariance must specify the transformation class under which it is preserved.

16.1 A proposed causal response fingerprint

For a fixed model family, define a combined fingerprint

\mathfrak F_{\mathrm{QCST}}

\left(
\mathbf I_r(\mathfrak C),
\mathbf S_r(\mathfrak Q_\epsilon),
\mathbf D_{\mathrm{mic}}(W_\omega)
\right),

where:

* is a truncated causal singular-value signature;
* is a specified propagation-response signature;
* denotes selected microlocal or singular-support data, when available.

This is a structured data object, not yet a new invariant. Its components are derived from different mathematical structures, and the combined object may retain localization, state, and regulator dependence.

The research objective is to identify a quotient or equivalence class of such fingerprints that is stable under a declared family of representation changes and still discriminates between physically distinct propagation regimes.

17. Relation to measurable quantum-field observables

A theoretical spectrum becomes physically useful when it predicts an operationally defined quantity.

For a two-level detector with energy gap , coupling , trajectory , and switching function , a leading-order transition probability in a specified state has the schematic form

\mathcal P_\omega
\propto
\lambda^2
\int d\tau\,d\tau’\,
\chi(\tau)\chi(\tau’)
e^{-i\Omega(\tau-\tau’)}
W_\omega(x(\tau),x(\tau’)),

with the overall sign and frequency convention fixed by the detector model.

This observable depends on the state-dependent two-point function, not merely on the causal propagator. It is therefore an especially stringent test of QCST: a causal spectral invariant may constrain the commutator or response kernel while leaving state-dependent contributions undetermined.

A more direct initial target is a classical or linear-response measurement. For a localized source , define

\delta\phi=G_{\mathrm{ret}}J.

For a specified detector profile , the measured smeared response is

\mathcal A_gh,J

\langle h,G_{\mathrm{ret}}J\rangle,

where the pairing is defined with the appropriate measure and function spaces.

A spectral theorem might constrain , a response norm over a class of source profiles, or the stability of the response under perturbations. The target must be chosen in advance. A post hoc correlation between a spectrum and a measured response is not sufficient to establish a predictive law.

17.1 The proposed measurement theorem

A physically meaningful next theorem would have the following structure.

Target theorem. For a specified class of globally hyperbolic backgrounds, field operators, localization functions, and admissible states, there exists a representation-stable causal spectral invariant and a function such that

\left|
\mathcal A_gh,J-F(I_C;\boldsymbol\theta)
\right|
\le \varepsilon,

where contains independently measured or theoretically fixed field parameters and is an explicit error bound.

To establish this theorem, the program must prove that:

* is well-defined and stable under the specified representation changes;
* the source and detector classes are fixed independently;
* the map follows from the field dynamics rather than a fit to the target response;
* the error estimate is uniform over the claimed model class;
* the result predicts at least one response observable not used to construct or calibrate .

This is the intended empirical endpoint of QCST. The theorem is a research target, not a result established by the definitions above.

18. Geometric perturbations and causal instability

A major obstacle is that causal order can be discontinuous under geometric perturbation in ways that ordinary operator-norm stability estimates do not capture.

Let

g_\varepsilon=g+\varepsilon h+O(\varepsilon^2)

be a smooth family of Lorentzian metrics, with a symmetric tensor. Even when is close to in a chosen smooth topology, null cones shift. Event pairs near a null boundary may change causal classification.

Consequently, the indicator kernels

K_{g_\varepsilon}(x,y)

\mathbf1_{\{x\preceq_{g_\varepsilon}y\}}

need not vary uniformly with . Under additional regularity and measure assumptions, one may be able to prove convergence in or another weaker norm, but this must be established for the perturbation class.

18.1 A useful perturbation program

The appropriate sequence of results is:

Step 1 — Causal-boundary control. Establish a bound on the measure of event pairs whose causal classification changes under .

Step 2 — Kernel control. Convert the causal-boundary estimate into a bound on

\|K_{g_\varepsilon}-K_g\|_{L^2}.

Step 3 — Operator control. Use the Hilbert–Schmidt estimate to obtain

\|\mathfrak C_{g_\varepsilon,\rho}
-\mathfrak C_{g,\rho}\|
\le
\|\mathfrak C_{g_\varepsilon,\rho}
-\mathfrak C_{g,\rho}\|_{\mathrm{HS}}.

Step 4 — Spectral control. Apply singular-value perturbation inequalities to obtain stability of the finite causal signature.

Step 5 — Propagation control. Independently bound the variation of the relevant Green operators and prove a causal-to-propagation correspondence for the selected observable.

The fifth step is essential. A stable causal spectrum does not automatically imply a stable quantum response unless the propagation map is itself controlled.

19. Uniqueness and inverse reconstruction

A spectrum is generally a compressed representation of an operator. It need not uniquely identify the operator, much less the geometry from which the operator was constructed.

Even for familiar elliptic problems, distinct geometries can share spectral data of a given type. In the present non-self-adjoint setting, equality of eigenvalue sets is particularly weak: it can omit singular-value information, eigenvector structure, and resolvent sensitivity.

QCST must distinguish three inverse problems:

* Operator identification: does the chosen spectral signature determine the causal operator up to the intended equivalence?
* Causal reconstruction: does the operator determine the causal order, or only a weaker invariant of it?
* Geometric reconstruction: does the recovered causal structure, together with additional scale information, determine the relevant Lorentzian geometry under stated hypotheses?

The answer to one does not imply the answers to the others.

19.1 A conditional inverse criterion

Let be a declared class of admissible localized causal structures, modulo an equivalence relation . Let map each structure to a chosen spectral signature.

An inverse reconstruction result would require an injectivity condition of the form

\mathfrak I(g_1)=\mathfrak I(g_2)
\quad\Longrightarrow\quad
g_1\sim g_2

for .

For a practical reconstruction theorem, injectivity should be supplemented by a stability estimate, for example

d_{\mathcal G}(g_1,g_2)
\le
\Psi\!\left(
d_{\mathcal I}(\mathfrak I(g_1),\mathfrak I(g_2))
\right),

where and are explicitly defined distances and as .

Neither injectivity nor stability follows from the operator definition alone. They are open mathematical obligations for any chosen spectral signature.

20. A hierarchy of claims

To prevent the program from conflating mathematical construction with physical discovery, its claims should be ranked by evidential status.

Established mathematics

Level I — Operator construction

A bounded causal-order integral operator can be defined on a finite-measure region with a measurable causal kernel. The resulting Hilbert–Schmidt operator is compact and has a singular-value sequence.

Established mathematics

Level II — Abstract stability

Singular values of compact operators are stable under operator-norm perturbations. Conditional propagation-observable bounds follow when an explicit Lipschitz correspondence and controlled approximation errors are assumed.

Requires proof

Level III — Geometric stability

Metric perturbations must be shown to induce controlled changes in the causal operator for a specified class of backgrounds and localizations.

Open research target

Level IV — Causal-to-quantum correspondence

A nontrivial relation between causal spectral data and a propagator observable must be derived from the field dynamics, with independent physical parameters and error bounds.

Unestablished universal claim

Level V — Complete spectral reconstruction

No general result has been established here showing that a universal causal spectrum uniquely determines Lorentzian geometry, the quantum propagator, or a quantum state.

This hierarchy is part of the theory’s mathematical content. It prevents a conditional operator estimate from being presented as a completed physical law.

21. Falsifiable research program

QCST should advance through a sequence of gates. Each gate must produce a result that can fail independently.

Gate	Required result	Failure criterion
G1: Definition	A causal operator with fixed domain, measure, and normalization	Dependence on unspecified conventions
G2: Spectral existence	A well-defined spectrum or singular-value distribution	Operator realization or limiting measure fails
G3: Representation stability	Explicit invariance under a declared transformation class	Invariants change under allowed representation changes
G4: Geometric stability	A bound from metric perturbations to causal-operator perturbations	Null-boundary changes defeat the proposed bound
G5: Quantum correspondence	A derived relation to a specified propagation operator	Relation requires unconstrained fitting
G6: Observable theorem	A measurable response with an explicit error estimate	No independent observable follows
G7: Inverse identifiability	A reconstruction or discrimination theorem	Distinct admissible models share the proposed signature
G8: Independent validation	Prediction on data not used to construct the invariant	Predictive performance disappears out of sample

The program should not skip directly from G2 to G6. A computable spectrum is not evidence of a physical correspondence, and a physical correspondence is not evidence of a complete inverse reconstruction.

21.1 Benchmark suite

A minimally convincing study should compare:

* Minkowski spacetime with massless and massive scalar fields;
* curved globally hyperbolic spacetimes with known Green-function behavior;
* different Hadamard states on the same background;
* multiple localization regions and switching functions;
* controlled metric perturbations;
* finite causal-set approximations with independently specified discrete dynamics.

The same causal invariant should be evaluated across these cases without silently changing its definition. If state dependence or field-parameter dependence enters the target observable, the analysis must identify where that information enters the correspondence.

22. Principal failure modes and limits

22.1 Non-identifiability

A finite spectral signature may discard information needed to distinguish causal structures. Increasing the number of invariants may improve discrimination, but completeness cannot be assumed.

22.2 Regulator dependence

A regularized causal propagator may acquire spectral features from the smoothing kernel, finite-volume cutoff, or boundary prescription. A continuum limit must show which features survive.

22.3 State dependence

The causal propagator fixes the field commutator, not the complete two-point function. A proposed relation to detector probabilities must specify the state or quantify over a declared state class.

22.4 Non-normality

Eigenvalues can fail to provide stable information about a non-normal operator. Singular values and resolvent data may be more appropriate, but their interpretation and invariance properties must be proved.

22.5 Circular reconstruction

If the causal spectrum is defined using the target propagator, and the same propagator is then claimed to follow from that spectrum, the proposed theorem is circular. The causal invariant must be constructed independently of the target observable.

22.6 Trivial correspondence

The identity becomes uninformative if is defined after the fact to reproduce . The map must be derived or constrained independently and must generate testable consequences.

22.7 Mistaking mathematical stability for physical universality

A perturbation bound on one Hilbert space does not imply that the same bound applies to all spacetimes, all field theories, or all operational measurements. Every theorem must retain its stated hypotheses.

23. New conjectures and candidate theorems

The following propositions define plausible directions for original mathematical work. They are research conjectures or targets, not established results of this paper.

Conjecture 23.1 — Causal spectral compression

For a suitably restricted class of localized globally hyperbolic geometries, there exists a countable family of normalized causal spectral invariants that separates causal structures up to a specified equivalence relation.

The key unresolved question is whether the family can be made both complete on the chosen class and stable under controlled geometric perturbations. A countable list of invariants is not automatically complete, and completeness may conflict with strong stability requirements.

Conjecture 23.2 — Restricted propagator determination

For a fixed normally hyperbolic field operator family with independently specified lower-order parameters, there exists a causal spectral signature that constrains a nontrivial class of localized propagator observables with uniform error bounds.

This conjecture deliberately does not claim that causal order alone determines the propagator. It proposes that spectral information, combined with a restricted dynamical model, may yield stable quantitative constraints beyond causal support.

Conjecture 23.3 — Spectral universality under admissible localization

There may exist normalized causal spectral statistics whose limiting values are independent of the detailed shape of the localization weight within a restricted class, while retaining sensitivity to selected geometric scales.

To establish this conjecture, one would need to identify the admissible localization class, define the normalization, and prove or numerically establish convergence with explicit error estimates. The conjecture should be rejected if the statistics remain strongly dependent on localization details that cannot be calibrated independently.

Candidate theorem 23.4 — Spectral-to-response estimate

Let be a class of admissible Lorentzian backgrounds and let be a representation-stable causal spectral signature. Suppose a field-theoretic construction yields a map from this signature and independently specified parameters to a bounded response observable. The desired theorem would establish

\left|
\mathcal A_{g_1}h,J

\mathcal A_{g_2}h,J
\right|
\le
\Psi\!\left(
d_{\mathcal I}(\mathfrak I(g_1),\mathfrak I(g_2))
\right)
+
\varepsilon_{\mathrm{model}},

for all , with as and a controlled model error .

The substantive theorem would have to derive , establish the correspondence, and state the dependence on source, detector, field parameters, and regularization. Merely assuming such a map would not establish the result.

24. Research architecture

The theory can be organized into five connected mathematical modules.

Module A — Lorentzian causal data

Causal order, volume measure, localization, geometric perturbations

Module B — Causal operator

Boundedness, compactness, singular values, resolvent and determinant data

Module C — Field propagation

Normally hyperbolic operators, Green functions, causal propagators, regularization

Module D — Correspondence theorem

Operator estimates, representation stability, error bounds, inverse identifiability

Module E — Physical validation

Localized response, detector observables, independent prediction, falsification

The arrows represent separate proof obligations. In particular, the transition from Module B to Module C is not automatic: the causal-order operator and the field propagator are independently defined objects. Module D must establish their connection for a specified class of models.

25. Conclusions

The Quantum Causal Spectrum Theory begins with a plausible and mathematically meaningful question: can the causal structure of Lorentzian spacetime and the propagation of quantum fields be related through spectral invariants that survive changes of representation?

This paper has established a framework for addressing that question without assuming the desired result.

First, a measurable causal-order kernel on a finite-measure region defines a Hilbert–Schmidt operator and therefore a compact spectral problem. Its singular values offer a natural starting point because the operator need not be self-adjoint.

Second, the causal-order operator, the causal propagator, and the state-dependent two-point function are distinct. Their relationship must be derived rather than built into the definitions.

Third, a conditional stability theorem establishes that a controlled correspondence between causal and quantum operators yields controlled variation of a selected propagation observable. The theorem is rigorous but conditional: the central physical task is to derive the correspondence map and prove its stability.

Fourth, a no-go result excludes the strongest naive claim. Causal order alone cannot uniquely determine propagators for different field theories on the same spacetime. Any viable spectral correspondence must identify its dynamical inputs and state precisely what it predicts.

Finally, existing microlocal results already establish a deep connection between Lorentzian null propagation and quantum-field singularities, while current research investigates spectral densities of causal propagators. QCST must build upon these foundations and demonstrate additional value through a new invariant, a sharper theorem, a controlled reconstruction, or an independently testable response prediction.

The decisive standard is therefore not whether causal and quantum operators possess spectra. It is whether one can prove that a precisely defined, representation-stable causal invariant constrains a physically measurable propagation property, with independently specified dynamics and explicit error bounds.

The central open theorem remains:

\boxed{
\text{causal spectral invariant}
\ \Longrightarrow\
\text{quantitatively constrained quantum response}
}

The implication must be proved for a specified model class. Until then, QCST is a structured mathematical research program rather than an established universal law of quantum spacetime.

Selected references

* Bär, C., Ginoux, N., and Pfäffle, F. (2007). Wave Equations on Lorentzian Manifolds and Quantization. European Mathematical Society.
* Radzikowski, M. J. (1996). “Micro-Local Approach to the Hadamard Condition in Quantum Field Theory on Curved Space-Time.” Communications in Mathematical Physics, 179, 529–553.
* Sahlmann, H., and Verch, R. (2001). “Microlocal Spectrum Condition and Hadamard Form for Vector-Valued Quantum Fields in Curved Space-Time.” Reviews in Mathematical Physics, 13, 1203–1246.
* Avetisyan, Z., and Capoferri, M. (2021). “Partial Differential Equations and Quantum States in Curved Spacetimes.” Mathematics, 9(16).
* Bombelli, L., Lee, J., Meyer, D., and Sorkin, R. D. (1987). “Space-Time as a Causal Set.” Physical Review Letters, 59, 521–524.
* Surya, S. (2019). “The Causal Set Approach to Quantum Gravity.” Living Reviews in Relativity, 22, 5.
* Kouchekzadeh Yazdi, Y. (2026). “Spectral Density of the Causal Propagator.” Perimeter Institute, May 21, 2026.

The references establish background and neighboring research directions; they do not imply that the proposed QCST correspondence conjectures have already been proved.
