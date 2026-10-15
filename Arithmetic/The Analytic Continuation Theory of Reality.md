The Analytic Continuation Theory of Reality

A Mathematical Framework for Relating Physical Regimes Through Generating Functions, Complex Singularities, and Analytic Branches

Research preprint · October 15, 2026 · Complex analysis, mathematical physics, and quantum field theory

Abstract

This paper develops the Analytic Continuation Theory of Reality (ACTR), a proposed framework for investigating whether apparently distinct physical regimes can be represented as different analytic branches, boundary values, asymptotic sectors, or singular limits of a common generating function. The central object is

Z(\lambda)=\int_{\mathcal X}
e^{-S(x,\lambda)}\,d\mu(x),

where is a configuration space, is an action or generalized exponent, is a measure, and denotes one or more control parameters that may be complexified.

The framework begins with a crucial distinction: analytic connection is a mathematical relation, not a proof of physical equivalence. Two formulas may be analytic continuations of one another while representing different boundary conditions, different integration contours, different states, different observables, or different operational regimes. Conversely, physically distinct phases may arise from different thermodynamic limits or nonperturbative sectors of one underlying analytic construction.

ACTR therefore treats the relationship between mathematics and physical interpretation as a layered problem. The first layer establishes the domain of holomorphy of . The second characterizes its zeros, singularities, monodromy, and asymptotic expansions. The third identifies candidate branches and their continuation paths. The fourth determines whether those branches correspond to distinct physical regimes through observables, positivity, stability, causal structure, and measurement protocols.

A conditional branch-correspondence theorem is formulated: if two regime-specific descriptions arise from boundary values or continuations of the same holomorphic germ along admissible paths, if their observables continue consistently, and if their physical reconstruction maps satisfy explicit compatibility conditions, then the descriptions are analytically related within the stated domain. Physical equivalence follows only under additional operational and dynamical hypotheses.

The paper also distinguishes ordinary analytic continuation from Stokes phenomena, Lee–Yang zeros, metastable branches, phase transitions, and the inequivalent limits that can arise in quantum field theory. A research program is proposed for determining when a common generating function explains multiple physical descriptions—and when it merely provides a shared mathematical representation.

Keywords: analytic continuation; generating functions; partition functions; complex singularities; branch points; monodromy; quantum field theory; Lee–Yang zeros; Stokes phenomena; physical equivalence; nonperturbative analysis.

1. Introduction: One Mathematical Object, Multiple Physical Descriptions

Physical theories often employ different mathematical representations in different regimes. A system may admit a Euclidean formulation for calculating correlation functions, a Lorentzian formulation for causal evolution, a low-energy effective description, a high-temperature expansion, or a semiclassical approximation. The existence of several descriptions raises a foundational question:

Can these descriptions be understood as different analytic manifestations of one underlying mathematical object?

The proposal investigated here is that, under appropriate conditions, they may be represented by a common generating function whose analytic structure organizes their relationships.

Let denote a control parameter. It may represent temperature, coupling strength, chemical potential, external field, mass, complexified time, or a collection of such variables. Consider

Z(\lambda)=
\int_{\mathcal X}
e^{-S(x,\lambda)}\,d\mu(x).
\tag{1.1}

For real parameters in a domain where the integral converges, may be a partition function, a normalization functional, a path-integral amplitude, or a more abstract generating object. When is complexified, the same integral may define a holomorphic function on some domain, provided that convergence and differentiation under the integral sign can be justified.

Analytic continuation then permits a function initially defined on one domain to be extended to another. The extension may encounter singularities, branch points, or changes in asymptotic behavior. These features can organize the relationship between descriptions that appear unrelated when expressed in their original variables.

However, three propositions must not be conflated:

* Common representation: two descriptions can be encoded by one generating object.
* Analytic connection: the relevant functions are restrictions, boundary values, or continuations of the same analytic germ.
* Physical equivalence: the descriptions encode the same physical content under a specified correspondence between states, observables, dynamics, and measurements.

The first does not guarantee the second, and the second does not guarantee the third.

ACTR is designed to make these distinctions mathematically explicit.

1.1 The central hypothesis

The working hypothesis is that some apparently different physical regimes are not independent mathematical constructions but belong to a structured family of analytic descriptions generated by a common object.

In its simplest form,

\mathcal R_i
\longleftrightarrow
\mathcal B_iZ,
\tag{1.2}

where is a physical regime and denotes the analytic branch, boundary value, asymptotic sector, or singular limit of associated with that regime.

The hypothesis is deliberately conditional. It does not assert that every physical regime belongs to a single analytic family, nor that every singularity has a physical meaning. The objective is to derive criteria under which such a correspondence can be established.

1.2 The primary research questions

The theory asks:

* When does the integral in (1.1) define a holomorphic function?
* Which zeros and singularities are intrinsic to the generating function rather than artifacts of a representation?
* When does analytic continuation generate genuinely distinct branches?
* How do branch points and monodromy constrain the possible relationships between regimes?
* When do asymptotic expansions describe different approximations to one analytic function, and when do they signal distinct nonperturbative sectors?
* What additional evidence is required to interpret analytic branches as physical regimes?
* Can a criterion distinguish genuine regime correspondence from formal resemblance?

The main result will be a conditional theorem connecting analytic branches to physical descriptions without identifying analytic continuation with physical equivalence.

2. Mathematical Foundations and Definitions

2.1 Configuration spaces and generating functions

Let be a measurable configuration space equipped with a measure . Let be a parameter domain, and let

S:\mathcal X\times\Lambda\to\mathbb C

be a complex-valued action or exponent.

We define

Z(\lambda)=
\int_{\mathcal X}
e^{-S(x,\lambda)}\,d\mu(x)
\tag{2.1}

where the integral exists.

The symbol is not restricted to a physical action in the Lagrangian sense. It may be a free-energy functional, a large-deviation rate function, a statistical weight exponent, or a complexified effective action.

The minimal mathematical requirements are measurability in , suitable parameter dependence in , and sufficient integrability for the integral to exist.

A central difficulty is that these conditions may hold only on a subset of . The generating function can be holomorphic on one region and fail to extend as a single-valued holomorphic function across another.

2.2 Holomorphic generating functions

A function is holomorphic if it is complex differentiable at every point of the open domain .

A useful sufficient condition for (2.1) is the following.

Proposition 2.1 — Holomorphy under an integrable majorant.

Let be open. Suppose that for almost every , the function

\lambda\mapsto e^{-S(x,\lambda)}

is holomorphic on . Suppose further that for every compact , there exists an integrable function such that

\sup_{\lambda\in K}
\left|e^{-S(x,\lambda)}\right|
\le g_K(x),
\qquad
\int_{\mathcal X}g_K(x)\,d\mu(x)<\infty.
\tag{2.2}

Then is holomorphic on .

Proof. For each compact subset , the integrand is pointwise holomorphic and uniformly dominated by an integrable function. The standard theorem on holomorphic parameter-dependent integrals therefore permits integration and complex differentiation on compact subdomains. Consequently, is holomorphic throughout .

This proposition provides a starting point, not a universal guarantee. In infinite-dimensional path integrals, the measure may be formal, the action may require regularization, and the continuum limit may not preserve the desired bounds. Those issues must be resolved before holomorphy is claimed.

2.3 Analytic germs

An analytic germ at is the equivalence class of holomorphic functions that agree on some neighborhood of .

Two expressions that agree on a nonempty open neighborhood define the same germ there. The identity theorem then forces their agreement throughout any connected domain to which both extend holomorphically.

This observation is important for ACTR: local agreement can establish a unique analytic relationship, but only within the assumptions that make continuation possible.

A germ is not a physical theory. It is a local mathematical object from which analytic extensions may be constructed.

2.4 Branches and continuation paths

Let be a holomorphic germ at a base point . A path

\gamma:0,1\to\Lambda_{\mathrm{reg}},
\qquad
\gamma(0)=\lambda_0,
\tag{2.3}

is a continuation path if the germ can be analytically continued along the path. Here denotes the region in which the relevant continuation is locally regular.

Continuation along may produce a germ at . We write

Z_\gamma=\operatorname{Cont}_\gamma(Z_0).
\tag{2.4}

If different paths with the same endpoints produce different terminal germs, the continuation is path-dependent. This behavior is the analytic origin of monodromy and multivalued branches.

A branch is therefore not simply a different formula. It is a local analytic realization obtained through a specified continuation procedure.

2.5 Physical regimes

For this paper, a physical regime is a tuple

\mathcal R_i=
(\mathcal H_i,\mathcal A_i,\omega_i,
\mathcal D_i,\mathcal P_i),
\tag{2.5}

where:

* is a state space or its appropriate generalization;
* is an algebra of observables;
* is a state or expectation functional;
* encodes dynamics or equations of motion;
* specifies the operational or measurement structure.

Not every application requires a Hilbert-space formulation. The tuple is intended to force explicit identification of the structures needed to interpret a mathematical branch physically.

Two regimes may share a generating function while differing in one or more components of (2.5). Whether those differences are merely representational or physically substantive is a separate question.

3. The Analytic Architecture of the Generating Function

The generating function contains several kinds of information that must be distinguished before it can be used to relate physical regimes.

3.1 Derivatives and generating observables

Suppose is differentiable with respect to , and differentiation under the integral is valid. Then

\frac{dZ}{d\lambda}

-\int_{\mathcal X}
\frac{\partial S}{\partial\lambda}
e^{-S(x,\lambda)}\,d\mu(x).
\tag{3.1}

Where , define the normalized expectation

\langle A\rangle_\lambda

\frac{1}{Z(\lambda)}
\int_{\mathcal X}
A(x,\lambda)e^{-S(x,\lambda)}\,d\mu(x).
\tag{3.2}

It follows that

\frac{d}{d\lambda}\log Z(\lambda)

-\left\langle
\frac{\partial S}{\partial\lambda}
\right\rangle_\lambda.
\tag{3.3}

Higher derivatives of generate connected response functions, subject to the usual conditions on the parameter dependence of . For a linear coupling

S(x,\lambda)=S_0(x)-\lambda A(x),
\tag{3.4}

we obtain

Z(\lambda)=\int_{\mathcal X}
e^{-S_0(x)+\lambda A(x)}\,d\mu(x),
\tag{3.5}

and

\frac{d^n}{d\lambda^n}\log Z(\lambda)

\kappa_n(A),
\tag{3.6}

where is the -th connected cumulant of , when the normalized measure is positive and the relevant moments exist. For complex weights, the same derivative identities remain algebraically meaningful but need not define probabilistic cumulants.

Thus, the analytic structure of constrains not only the normalization of a theory but also its hierarchy of responses.

3.2 The logarithm and the free-energy representation

A frequently used transformed quantity is

W(\lambda)=\log Z(\lambda).
\tag{3.7}

This transformation is locally well-defined wherever , after choosing a logarithmic branch. The distinction between and is fundamental.

The generating function may be single-valued even when is multivalued. For example, if winds around the origin as traces a closed loop, then

\Delta_\gamma\log Z

2\pi i\,n_\gamma,
\qquad n_\gamma\in\mathbb Z,
\tag{3.8}

provided is nonzero along the loop.

In statistical mechanics, one often defines a free-energy density by

f(\lambda)

-\lim_{V\to\infty}
\frac{1}{V}\log Z_V(\lambda),
\tag{3.9}

where denotes volume or another extensive parameter.

Even if each finite-volume is entire, the limiting function may be nonanalytic. The order of limits, normalization, and branch choice therefore matters. Nonanalyticity of the thermodynamic free energy does not imply that the finite-volume partition function itself has a singularity at the same point.

3.3 The cumulant expansion and its limitations

Expanding around , one may write formally

Z(\lambda)=
\sum_{n=0}^{\infty}
\frac{\lambda^n}{n!}
\left.\frac{d^nZ}{d\lambda^n}\right|_{\lambda=0}.
\tag{3.10}

When this series converges in a neighborhood, it defines there. Its radius of convergence is bounded by the distance to the nearest singularity of the analytic function represented by the series.

A divergent perturbation series can nevertheless encode valuable information. It may be asymptotic to a well-defined function rather than convergent to it. In that case, a summation prescription—such as Borel summation, where applicable—is needed to reconstruct the intended function.

The series alone does not always determine the full nonperturbative answer. Distinct functions can share the same asymptotic power series while differing by contributions that are exponentially small in the expansion parameter.

This fact will become central to the theory: the analytic object may contain physical information that no finite-order or even complete formal power series uniquely captures.

4. The Singular Set: Zeros, Poles, Branch Points, and Essential Singularities

The analytic behavior of is governed by the locations and types of its singularities and zeros.

Let

\Sigma_Z

\{\lambda:\ Z
\text{ fails to admit the required local holomorphic extension}\}
\tag{4.1}

denote a singular set, understood relative to the chosen representation and domain. Zeros should be recorded separately, since a zero of is not itself a singularity of , although it is a singularity of .

4.1 Zeros of the generating function

A zero satisfies

Z(\lambda_*)=0.
\tag{4.2}

If is holomorphic near and not identically zero, then the zero has finite multiplicity , and locally

Z(\lambda)

(\lambda-\lambda_*)^m h(\lambda),
\qquad h(\lambda_*)\neq 0.
\tag{4.3}

Consequently,

\log Z(\lambda)

m\log(\lambda-\lambda_*)+\log h(\lambda).
\tag{4.4}

The logarithm has a branch singularity at the zero, even though itself is locally holomorphic.

Zeros can therefore obstruct the continuation of derived quantities without obstructing the continuation of the underlying partition function.

4.2 Lee–Yang zeros and phase transitions

In finite statistical-mechanical systems, partition functions often depend analytically on an external field or fugacity. Their zeros may lie away from the physical real axis. As the system size increases, these zeros can accumulate toward a real parameter value.

This is the basis of the Lee–Yang approach to phase transitions.

Let be a finite-volume partition function, and suppose

\lambda_{j,V}\in\mathbb C

are its zeros. A thermodynamic singularity may emerge when the limiting zero distribution approaches the physical parameter domain as .

The important logical sequence is

\text{finite-volume zeros}
\longrightarrow
\text{limiting zero distribution}
\longrightarrow
\text{possible nonanalytic thermodynamic behavior}.
\tag{4.5}

The final implication requires additional assumptions. A sequence of zeros approaching a real value is highly informative, but the nature of the limiting singularity depends on their density, scaling, and the definition of the thermodynamic limit.

ACTR interprets these zero distributions as potential boundaries between analytic descriptions. It does not assume that every zero marks a distinct physical phase.

4.3 Poles

A pole at is characterized by a local representation

Z(\lambda)

\frac{h(\lambda)}
{(\lambda-\lambda_*)^m},
\qquad h(\lambda_*)\neq0.
\tag{4.6}

Poles may arise from the generating function itself, from a transformed observable, from a resolvent, or from a chosen normalization.

These cases must be distinguished. A pole in a Green function may represent a physical excitation under appropriate spectral conditions. A pole introduced by dividing by a vanishing normalization may be removable from the underlying physical observable.

The location of a pole alone is not sufficient to establish a particle, a state, or a dynamical instability.

4.4 Algebraic branch points

A branch point may occur when the local behavior is of Puiseux type,

Z(\lambda)
\sim
\sum_{k=k_0}^{\infty}
a_k(\lambda-\lambda_*)^{k/r},
\qquad r\geq2.
\tag{4.7}

A circuit around can permute the local branches. For a square-root branch,

Z(\lambda)\sim
(\lambda-\lambda_*)^{1/2},
\tag{4.8}

one circuit changes the sign of the square root.

Such branch points can arise from eigenvalue collisions, discriminants, thresholds, or multivalued solutions of implicit equations. Their physical interpretation depends on what the branches represent.

4.5 Essential singularities

An essential singularity exhibits behavior not reducible to a finite-order pole or removable singularity. A canonical example is

Z(\lambda)=e^{1/\lambda}
\tag{4.9}

at .

Essential singularities can organize highly nonuniform behavior and asymptotic sectors. In physical applications, they may appear in coupling limits, nonperturbative expansions, or exponential contributions invisible to ordinary power series.

Yet an essential singularity is a mathematical classification, not automatically a physical catastrophe. A physical interpretation requires identifying the observable that becomes singular and showing that the singular behavior survives appropriate changes of representation.

4.6 Singularities of derived observables

Let

\mathcal O(\lambda)=
\frac{N(\lambda)}{Z(\lambda)}.
\tag{4.10}

Even if and are entire, may have poles at zeros of , unless cancellations occur.

Conversely, a singularity in one representation may disappear in another invariant observable. ACTR therefore distinguishes:

* singularities of the primitive generating function;
* singularities introduced by logarithms, ratios, or normalization;
* singularities of physical observables;
* singularities caused by an approximation or a limiting procedure.

The relevant singular set for a physical regime is not necessarily alone.

5. Branch Structure, Monodromy, and Analytic Continuation

5.1 Continuation as a path-dependent operation

Suppose is a germ at a base point . If the germ can be continued along paths in a punctured domain

\Lambda_{\mathrm{reg}}

\Lambda\setminus\Sigma,
\tag{5.1}

then the result at a terminal point may depend on the homotopy class of the path.

Let and begin at and end at . In general,

\operatorname{Cont}{\gamma_1}(Z_0)
\neq
\operatorname{Cont}{\gamma_2}(Z_0).
\tag{5.2}

If they differ, the difference is not arbitrary. Under standard continuation conditions, it is governed by the topology of the regular domain and the monodromy of the analytic object.

5.2 Monodromy representation

For a suitably well-behaved multivalued analytic function, continuation around loops based at induces transformations of the local branches. These transformations form a monodromy action of the fundamental group,

\rho:\pi_1(\Lambda_{\mathrm{reg}},\lambda_0)
\longrightarrow
\operatorname{Aut}(\mathscr B_{\lambda_0}),
\tag{5.3}

where denotes the relevant set of local branches.

The notation is schematic: the target is the appropriate group of branch permutations or analytic automorphisms for the problem at hand.

The monodromy representation records how local descriptions are transformed by continuation around singular sets.

ACTR interpretation. If multiple physical descriptions correspond to branches in , their analytic relationships may be organized by . However, the monodromy action alone does not identify those branches with physical states or phases.

5.3 Example: a square-root branch

Consider

Z(\lambda)=\sqrt{1-\lambda}.
\tag{5.4}

Choose the positive branch near . The Taylor series is

Z(\lambda)

1-\frac{\lambda}{2}
-\frac{\lambda^2}{8}
-\frac{\lambda^3}{16}
-\cdots,
\qquad |\lambda|<1.
\tag{5.5}

The branch point at limits this expansion. Analytic continuation around exchanges the two square-root branches.

The expressions

Z_+(\lambda)=+\sqrt{1-\lambda},
\qquad
Z_-(\lambda)=-\sqrt{1-\lambda}
\tag{5.6}

are not two unrelated analytic functions on the full branched covering surface. They are different local branches of one multivalued analytic object.

But the equation does not tell us whether and describe two physical phases, two conventions for a square root, two spectral sheets, or one physical solution with a redundant sign. That interpretation must be supplied by the model.

5.4 Branch selection by physical constraints

In a physical problem, admissible branches may be selected by conditions such as:

\begin{aligned}
&\text{reality:} && \mathcal O(\lambda)\in\mathbb R
\quad \text{for real physical }\lambda,\\
&\text{positivity:} && \langle A^\dagger A\rangle\geq0,\\
&\text{stability:} && \operatorname{Re}\omega_j\leq0
\quad\text{for decaying-mode conventions},\\
&\text{causality:} && \text{prescribed analytic boundary values},\\
&\text{normalization:} && \omega(I)=1.
\end{aligned}
\tag{5.7}

These requirements are examples, not universal conditions. The relevant constraints depend on the theory and the meaning of the generating function.

The central methodological rule is that a mathematically accessible branch need not be a physically admissible branch.

6. The Main Result: A Conditional Branch-Correspondence Theorem

The target of ACTR is not merely to prove that two formulas are analytically connected. It is to determine when such a connection supports a controlled correspondence between physical regimes.

6.1 Formal setup

Let be a connected regular domain containing a base point . Let be a holomorphic germ at , and let be paths along which can be analytically continued to points .

Denote the resulting germs by

Z_i=\operatorname{Cont}_{\gamma_i}(Z_0).
\tag{6.1}

For each candidate regime , let denote a family of observables indexed by . Suppose each observable is represented, in the relevant domain, by a function constructed from the generating object and any explicitly specified auxiliary data.

A regime-specific reconstruction map

\mathfrak P_i:
\{\text{analytic data near }\lambda_i\}
\longrightarrow
\mathcal R_i
\tag{6.2}

assigns physical meaning to the continued analytic data.

Such a map may encode a choice of state, contour, boundary condition, Hilbert-space representation, real-time prescription, or thermodynamic limit. Its specification is essential: it cannot be inferred from analytic continuation alone.

6.2 Theorem 6.1 — Conditional analytic branch correspondence

Theorem. Let be a holomorphic germ at , and let be continuation paths through a domain in which the required analytic continuations exist. Suppose the following conditions hold.

1. Common germ. Both regime-specific generating functions arise from the same germ , rather than merely from expressions with similar notation.

2. Admissible continuation. The germ can be continued along both paths, and every singularity crossed or approached is handled by a specified continuation, boundary-value, or limiting prescription.

3. Observable compatibility. The observables used to characterize the two regimes are analytic continuations of common generating observables, or are related by explicitly defined transformation laws.

4. Normalization and domain control. Zeros, poles, branch choices, and limiting procedures affecting the observables are identified, and no unaccounted singular factor changes the quantities being compared.

5. Physical reconstruction compatibility. The maps and assign the continued analytic data to the two proposed regimes in a manner consistent with the specified state spaces, observable algebras, dynamics, and operational prescriptions.

Then the two regime descriptions are analytically branch-related: their generating data are obtained from a common analytic germ by the stated continuation procedures, and their corresponding observables satisfy the continuation relations wherever those relations are defined.

If, in addition, there exists a bijective correspondence between the relevant physical state spaces or state sectors that preserves the specified observable algebra, expectation values, dynamics, and operational predictions, then the two descriptions are equivalent relative to that declared physical equivalence criterion.

Proof. Conditions 1 and 2 establish the common analytic origin and the existence of the relevant continued germs. Condition 3 ensures that the observables are related by continuation rather than merely by a formal resemblance of expressions. Condition 4 excludes unaccounted changes introduced by zeros, singular normalizations, or incompatible limits. Consequently, the generating data and their compatible observables satisfy the stated analytic branch relations.

Condition 5 supplies the independent interpretation maps needed to identify those analytic data with physical regimes. This yields an analytic correspondence between the descriptions.

The final claim requires the additional physical isomorphism: a bijective mapping that preserves the chosen observables, states, dynamics, and operational predictions. Without it, the theorem establishes analytic branch correspondence only, not physical equivalence.

6.3 What the theorem does—and does not—establish

The theorem is deliberately conditional. It does not derive a universal generating function for all physical theories, nor does it show that every pair of regimes is connected by analytic continuation.

Its contribution is a precise separation of two tasks:

\boxed{
\text{analytic continuation}
\quad\neq\quad
\text{physical equivalence}
}
\tag{6.3}

The first task is governed by complex analysis. The second requires additional structure from mathematical physics.

The theorem also makes the role of physical reconstruction maps explicit. Without such maps, a generating function is mathematically underdetermined as a description of reality: the same analytic object may admit several interpretations, while different analytic objects may encode equivalent observable predictions.

6.4 A uniqueness corollary

Corollary 6.1 — Uniqueness on a connected regular domain.

Suppose two candidate generating functions and are holomorphic on a connected domain and agree on a subset with an accumulation point in . Then

Z_1(\lambda)=Z_2(\lambda)
\qquad
\forall\lambda\in\Omega.
\tag{6.4}

This is the identity theorem.

The corollary provides a powerful test: if two proposed generating functions agree on a sufficiently rich set inside a common holomorphy domain, they cannot be distinct analytic functions there. Any apparent disagreement must arise from leaving the domain, changing a branch, changing a limiting prescription, or changing the physical interpretation.

The corollary does not imply that two theories agreeing on one observable have identical state spaces or dynamics. The identity theorem applies to the functions that actually agree, not to every structure that might be associated with them.

7. Asymptotic Expansions and the Multiplicity of Descriptions

Analytic continuation is often accompanied by asymptotic analysis. Distinct physical regimes may correspond not to distinct branches of the exact function, but to different asymptotic descriptions of the same function.

This distinction is essential.

7.1 Asymptotic expansions

Let be a function defined for small positive . An expansion

F(g)\sim\sum_{n=0}^{\infty}a_ng^n,
\qquad g\to0^+,
\tag{7.1}

means that for every fixed ,

F(g)-\sum_{n=0}^{N}a_ng^n
=o(g^N)
\tag{7.2}

under the relevant convention for the asymptotic scale.

An asymptotic expansion need not converge. Its coefficients may grow factorially, making the series divergent even though the function is well-defined.

The expansion can still be useful if truncating it at an appropriate order approximates the function in a controlled regime.

7.2 Beyond-all-orders contributions

Consider

F(g)=F_{\mathrm{pert}}(g)+Ce^{-A/g},
\qquad A>0,\quad g\to0^+.
\tag{7.3}

For every fixed integer ,

e^{-A/g}=o(g^N).
\tag{7.4}

Therefore and have the same formal power-series asymptotic expansion in , even though they are different functions whenever .

This gives an explicit obstruction to reconstructing reality from perturbative coefficients alone. Two descriptions can agree to every algebraic order and still differ nonperturbatively.

In field theory, terms of this type can arise from instanton sectors, tunneling contributions, or other nonperturbative effects, depending on the model and its boundary conditions.

7.3 Transseries

A more informative representation is a transseries,

F(g)\sim
\sum_{k=0}^{\infty}
\sigma^k e^{-kA/g}
\sum_{n=0}^{\infty}a_{k,n}g^n.
\tag{7.5}

Here is a sector parameter and is an action-like quantity. The expression organizes perturbative fluctuations around several exponentially weighted sectors.

A transseries is not automatically a convergent representation of an exact function. Its coefficients, sector weights, summation prescription, and analytic domain must be specified.

Nevertheless, it provides a natural language for ACTR because distinct asymptotic sectors can be related by analytic continuation and Stokes phenomena while remaining invisible to a single perturbative expansion.

7.4 Borel analysis

Suppose

F_{\mathrm{pert}}(g)\sim
\sum_{n=0}^{\infty}a_ng^{n+1}.
\tag{7.6}

The formal Borel transform is

\widehat F(t)=
\sum_{n=0}^{\infty}
\frac{a_n}{n!}t^n.
\tag{7.7}

If the Borel transform has suitable analytic continuation and growth properties, a directional Borel sum may be defined by

\mathcal S_\theta F(g)

\int_{0}^{e^{i\theta}\infty}
e^{-t/g}\widehat F(t)\,dt,
\tag{7.8}

with the precise prefactors determined by the convention used in (7.6)–(7.7).

When singularities of lie on or near the integration ray, the integral may require a lateral prescription or may fail to exist in this simple form. Different lateral sums can differ by exponentially small terms.

The important conclusion is that the analytic structure of the Borel transform can govern the relation between asymptotic descriptions. But a summation prescription is part of the definition of the reconstructed function, not an optional technical detail.

8. Stokes Phenomena: When Asymptotic Regimes Exchange Dominance

8.1 Stokes lines and asymptotic sectors

Consider two contributions,

F(g)\sim
F_0(g)+
C\,e^{-A/g}F_1(g).
\tag{8.1}

For complex , the relative magnitude of the exponential contribution is controlled by

\left|e^{-A/g}\right|

e^{-\operatorname{Re}(A/g)}.
\tag{8.2}

As the argument of changes, the exponential may be strongly suppressed in one angular sector and enhanced in another. The rays on which the asymptotic ordering changes are associated with Stokes geometry, with exact conventions depending on the problem.

Crossing a Stokes line can change the asymptotic representation: a contribution that was exponentially subdominant may become relevant, and the coefficients used to describe asymptotic sectors may undergo a jump.

The underlying analytic function need not be singular on that line. A Stokes line is not automatically a physical phase boundary or a singularity of .

8.2 Stokes data as relational information

Suppose a function has asymptotic expansions in adjacent sectors and . The two expansions may differ in their exponentially small terms even when their leading perturbative coefficients coincide.

The relation between the expansions is encoded by Stokes data. Schematically,

\mathcal A_{i+1}

\mathfrak S_i(\mathcal A_i),
\tag{8.3}

where represents the asymptotic data in sector , and is the relevant Stokes transformation.

This is not a universal formula for all Stokes problems; it represents the structural idea that neighboring asymptotic descriptions are connected by a transformation determined by the analytic problem.

For ACTR, Stokes data provide a possible bridge between regimes that appear discontinuous when described only by dominant asymptotic terms.

8.3 Distinguishing Stokes transitions from physical transitions

A Stokes transition may be purely representational: the exact function remains regular while the preferred asymptotic expansion changes.

A physical phase transition, by contrast, requires a physically meaningful nonanalyticity or a change in the relevant limiting state structure, according to the model’s definition of phase.

The two may be related, but neither implies the other in general.

A rigorous analysis should ask:

* Is the exact generating function singular at the proposed transition?
* Is only the asymptotic representation changing?
* Does a physical observable exhibit a nonanalyticity?
* Does the thermodynamic, semiclassical, or continuum limit create the singularity?
* Does the change affect measurable predictions or only the computational representation?

Without these distinctions, asymptotic rearrangements can be mistaken for ontological transitions.

9. Physical Regimes as Boundary Values and Limiting Descriptions

A common analytic object can support different physical interpretations without requiring a literal multivalued function. Two especially important mechanisms are boundary values and singular limits.

9.1 Boundary-value prescriptions

Suppose a function is holomorphic in a complex domain approaching a real parameter axis. Distinct physical prescriptions may be defined by

Z_+(\lambda)=
\lim_{\epsilon\downarrow0}
Z(\lambda+i\epsilon),
\qquad
Z_-(\lambda)=
\lim_{\epsilon\downarrow0}
Z(\lambda-i\epsilon).
\tag{9.1}

If both limits exist, they need not coincide. Their difference may encode discontinuity across a cut, a spectral density, or a response associated with a prescribed causal boundary condition.

For a simple function with a cut, the two boundary values are related by the discontinuity

\operatorname{Disc}Z(\lambda)

Z_+(\lambda)-Z_-(\lambda).
\tag{9.2}

A nonzero discontinuity is not by itself evidence of two physical worlds. It may arise from the choice of boundary value used to define a Green function or response function.

The physical content depends on the prescription and on the observables constructed from it.

9.2 Euclidean and Lorentzian descriptions

A prominent example is the relation between Euclidean and Lorentzian formulations of field theory. In suitable settings, complexification of time permits the formal substitution

t=-i\tau
\tag{9.3}

or an equivalent rotation of the time coordinate.

A Lorentzian oscillatory factor

e^{iS_L}
\tag{9.4}

may be related to a Euclidean weight

e^{-S_E}
\tag{9.5}

under an appropriate continuation, with conventions and signs determined by the action and metric signature.

This relationship is not universally justified by the formal substitution alone. The continuation must be compatible with the action, integration contour, boundary conditions, and convergence properties. In quantum field theory, further conditions—such as reflection positivity in appropriate Euclidean formulations—can be necessary for reconstruction of a physical Hilbert space and Lorentzian theory.

Thus, the Euclidean and Lorentzian formulations may be analytically related while their physical interpretation depends on additional reconstruction theorems.

9.3 Singular limits and emergent regimes

Let be a sequence of generating functions indexed by a system size, cutoff, or regulator. Each may be holomorphic on a domain , while the limiting object

Z_\infty(\lambda)=
\lim_{N\to\infty}Z_N(\lambda)
\tag{9.6}

may fail to be holomorphic on a larger domain.

Uniform convergence on compact subsets of a domain preserves holomorphy. If the convergence is only pointwise, or if the domain of uniform convergence excludes a critical region, the limit may develop nonanalytic behavior.

The order of operations can therefore matter:

\lim_{N\to\infty}
\operatorname{Cont}{\gamma}Z_N
\quad\text{need not coincide with}\quad
\operatorname{Cont}{\gamma}
\left(\lim_{N\to\infty}Z_N\right).
\tag{9.7}

Equation (9.7) is not a claim that the two expressions always differ; it identifies a possible obstruction requiring proof of interchangeability.

In ACTR, a new physical regime may emerge from a singular limit even when no distinct branch exists at finite .

10. A Worked Model: Competing Saddles and Regime Selection

To make the framework concrete, consider the integral

Z_N(\lambda)=
\int_{\mathcal C}
e^{-N S(z,\lambda)}a(z,\lambda)\,dz,
\tag{10.1}

where , is an integration contour, and and are analytic in a suitable domain.

This form appears in steepest-descent problems, semiclassical approximations, large-deviation theory, and certain matrix or field-theoretic integrals.

10.1 Saddle-point expansion

Suppose the saddle points satisfy

\frac{\partial S}{\partial z}
\bigg|{z=z_j(\lambda)}=0,
\qquad
\frac{\partial^2 S}{\partial z^2}
\bigg|{z=z_j(\lambda)}\neq0.
\tag{10.2}

Locally, the implicit-function theorem permits analytic dependence , provided the nondegeneracy condition persists.

The action evaluated at the saddle is

S_j(\lambda)=S(z_j(\lambda),\lambda).
\tag{10.3}

A leading steepest-descent approximation has the form

Z_N(\lambda)
\sim
\sum_j
n_j(\lambda)
a(z_j,\lambda)
\left(
\frac{2\pi}{N S_{zz}(z_j,\lambda)}
\right)^{1/2}
e^{-N S_j(\lambda)}.
\tag{10.4}

The coefficients depend on how the original integration contour decomposes into steepest-descent cycles. The square-root factors require branch choices, and the formula is valid only under suitable assumptions about saddles, contours, and the large- limit.

The expression shows how a single integral can admit several saddle descriptions.

10.2 Dominant saddles

For real positive , a saddle with smaller often contributes more strongly because

\left|e^{-N S_j}\right|

e^{-N\operatorname{Re}S_j}.
\tag{10.5}

As changes, two saddles may exchange dominance. The condition

\operatorname{Re}S_1(\lambda)

\operatorname{Re}S_2(\lambda)
\tag{10.6}

marks a possible change in the dominant asymptotic description.

But equality of real parts does not automatically imply a physical phase transition. Interference, contour coefficients, subleading contributions, and the order of limits can alter the conclusion.

10.3 A two-saddle approximation

Suppose, in a domain of validity,

Z_N(\lambda)
\approx
A_1(\lambda)e^{-N S_1(\lambda)}
+
A_2(\lambda)e^{-N S_2(\lambda)}.
\tag{10.7}

Zeros satisfy approximately

e^{-NS_1(\\lambda)-S_2(\\lambda)}

-\frac{A_2(\lambda)}{A_1(\lambda)}.
\tag{10.8}

If and are nonzero, taking a logarithm with an explicitly chosen branch yields

-NS_1(\\lambda)-S_2(\\lambda)

\log\!\left(-\frac{A_2(\lambda)}{A_1(\lambda)}\right)
+2\pi i k,
\qquad k\in\mathbb Z.
\tag{10.9}

This relation can generate families of approximate zeros. As increases, those zeros may become dense along curves determined by the competition between the saddle actions.

This mechanism links saddle competition, complex zeros, and possible limiting nonanalyticities.

10.4 Interpretation within ACTR

The two saddle contributions can be interpreted as competing asymptotic sectors of one integral. Under suitable continuation, the saddles themselves may exchange analytic identities, and the contour decomposition may change across Stokes regions.

Three distinct claims must nevertheless be separated:

* Mathematical claim: the integral has multiple saddle contributions.
* Asymptotic claim: different saddles dominate in different parameter regions.
* Physical claim: the dominant contributions correspond to distinct physical phases or regimes.

The first two may be established by complex analysis and asymptotic methods. The third requires identifying physical observables and showing that the large- or other relevant limit supports the proposed interpretation.

11. Quantum Field Theory: What the Generating Functional Can Establish

The finite-dimensional integral in (1.1) is a useful prototype. In quantum field theory, the analogous object is a functional integral over fields.

11.1 The generating functional

For a field coupled to a source , one writes formally

ZJ=
\int\mathcal D\phi\,
\exp\left\[
iS_L\[\\phi\]
+i\int d^dx\,J(x)\phi(x)
\right]
\tag{11.1}

in Lorentzian conventions, or

Z_EJ=
\int\mathcal D\phi\,
\exp\left\[
-S_E\[\\phi\]
+\int d^dx\,J(x)\phi(x)
\right]
\tag{11.2}

in a Euclidean convention.

These expressions require careful interpretation. The functional measure may be formal; regularization and renormalization may be required; and the choice of integration contour can determine which solutions or sectors contribute.

The generating functional is therefore not fully specified by its integrand alone.

11.2 Connected and one-particle-irreducible generating functions

Where , define

WJ=\log ZJ.
\tag{11.3}

Functional derivatives of generate connected correlation functions, under the usual conventions.

A classical field or expectation field may be defined by

\varphi(x)=
\frac{\delta WJ}{\delta J(x)}.
\tag{11.4}

If the map can be inverted, a Legendre transform defines an effective action,

\Gamma\\varphi

\int d^dx\,J(x)\varphi(x)-WJ,
\tag{11.5}

with the appropriate source-field pairing and convention.

The invertibility requirement matters. If the response map becomes singular or multiple branches of exist, the effective action may require branch-specific definitions.

Consequently, different branches of can induce different branches of , but the relationship depends on the invertibility and domain of the Legendre transform.

11.3 Analyticity and correlation functions

For a finite-dimensional generating function, derivatives of produce cumulants. In a field theory, functional derivatives similarly produce connected correlation functions.

If the source dependence is analytic in a domain and the necessary functional derivatives exist, the generating functional organizes an entire hierarchy of observables.

However, the analyticity of does not by itself guarantee:

* existence of a continuum quantum field theory;
* positivity of the physical state space;
* unitarity;
* causal propagation;
* uniqueness of a vacuum;
* equivalence of distinct representations;
* or equivalence of Euclidean and Lorentzian theories.

These properties require separate assumptions and results.

11.4 Analytic continuation of correlation functions

Suppose Euclidean correlation functions are known on a domain and possess suitable spectral and growth properties. Analytic continuation may reconstruct Lorentzian correlation functions or time-ordered Green functions.

The reconstruction is not an unconstrained substitution. It relies on the analytic domains, singularity structure, spectral properties, and boundary-value prescriptions appropriate to the theory.

The same Euclidean formula may be insufficient to distinguish physical sectors unless the state, boundary conditions, and reconstruction conditions are specified.

ACTR therefore treats continuation of correlation functions as a strong mathematical relation whose physical significance depends on the reconstruction theorem applicable to the particular model.

12. Contours, Complex Saddles, and the Missing Data of a Path Integral

The expression

Z(\lambda)=
\int_{\mathcal X}e^{-S(x,\lambda)}\,d\mu(x)
\tag{12.1}

can conceal a decisive choice: the integration domain or contour.

When the variables and action are complexified, different contours may yield different integrals, even when the integrand is identical.

12.1 Contour dependence

Let and be two admissible contours. Then

Z_{\mathcal C_1}(\lambda)

\int_{\mathcal C_1}
e^{-S(z,\lambda)}a(z,\lambda)\,dz,
\tag{12.2}Z_{\mathcal C_2}(\lambda)

\int_{\mathcal C_2}
e^{-S(z,\lambda)}a(z,\lambda)\,dz.
\tag{12.3}

Even when the integrand is the same, these integrals need not agree. If the contours are deformable into one another without crossing singularities and with suitable control of boundary contributions, they may be equal. If not, they may represent different analytic functions or different branches of a broader construction.

Thus, the action alone may not uniquely specify .

12.2 Lefschetz thimbles

In complex saddle-point analysis, an integration contour can often be decomposed into a sum of steepest-descent cycles, or thimbles,

\mathcal C
\sim
\sum_\sigma n_\sigma\mathcal J_\sigma.
\tag{12.4}

The coefficients depend on the contour and the relevant intersection data. The decomposition is model-dependent and requires appropriate nondegeneracy and convergence conditions.

As parameters vary, the thimble basis or the decomposition coefficients can change across Stokes walls. The exact integral may remain well-defined even as its saddle representation changes.

12.3 Consequence for the theory

A common integrand does not guarantee a common generating function. The contour is part of the mathematical specification.

For ACTR, a complete branch record should therefore include

\mathfrak A_i=
(Z_i,\gamma_i,\mathcal C_i,\mathfrak r_i),
\tag{12.5}

where:

* is the local analytic description;
* is the continuation path;
* is the relevant integration contour, where applicable;
* is the physical reconstruction prescription.

The fourth component is what prevents an analytic construction from being mistaken for a complete physical theory.

13. A Hierarchy of Equivalence: From Formula to Physical Reality

ACTR requires an explicit vocabulary for the different strengths of a relationship between descriptions.

13.1 Syntactic resemblance

Two formulas may have similar algebraic forms:

Z_1(\lambda)\sim Z_2(\lambda).
\tag{13.1}

This is the weakest relationship. Similar notation or parallel derivations do not establish mathematical equality.

13.2 Local analytic identity

Two functions are locally identical if they agree on an open neighborhood in a common domain.

The identity theorem can then extend this equality throughout the connected common domain, subject to the theorem’s assumptions.

13.3 Analytic continuation equivalence

Two descriptions are analytically continuation-related if they arise from the same germ through specified continuation paths or compatible boundary-value procedures.

This relationship is stronger than local resemblance but weaker than physical equivalence.

13.4 Observable equivalence

Two descriptions are observationally equivalent relative to a declared observable family if they produce the same predictions for that family under corresponding parameter assignments.

Let denote the chosen observable family. Then a restricted equivalence may be written

\mathcal R_1
\sim_{\mathfrak O}
\mathcal R_2
\tag{13.2}

when the corresponding predictions agree for every observable in over the specified experimental domain.

This is relative equivalence. Equality on a restricted observable family does not prove equality of all possible predictions.

13.5 Dynamical equivalence

A stronger criterion requires a correspondence between states and dynamics that preserves the relevant evolution and observables. Depending on the setting, this may be an isomorphism, a unitary equivalence, an equivalence of state categories, or another precisely defined structure-preserving map.

13.6 Ontological identity

The strongest claim—that two descriptions represent the same underlying reality—is not established by complex analysis alone. It requires an interpretation of what the mathematical structures represent and why the chosen equivalence relation is physically fundamental.

ACTR does not assume that ontological identity follows from any lower level in this hierarchy.

The hierarchy can be summarized as

\begin{aligned}
\text{formal resemblance}
&\;\not\Rightarrow\;
\text{analytic identity},\\
\text{analytic identity}
&\;\not\Rightarrow\;
\text{physical equivalence},\\
\text{observable equivalence}
&\;\not\Rightarrow\;
\text{unrestricted dynamical equivalence}.
\end{aligned}
\tag{13.3}

These are logical non-implications, not claims that the relationships can never coincide.

14. The Reconstruction Problem: From Analytic Branches to Physical Regimes

The main obstacle identified in the research proposal is that analytic continuation can connect expressions without establishing that their physical interpretations are equivalent.

This obstacle can be formalized as a reconstruction problem.

14.1 The forward map

Let denote a class of physical models, and let denote a class of analytic data. Suppose there is a forward map

\mathcal F:\mathfrak P\to\mathfrak A,
\tag{14.1}

which assigns a generating function, analytic germ, or family of correlation functions to a physical model.

The inverse problem asks whether the physical model can be reconstructed from the analytic data.

In general, need not be injective. Distinct physical models may yield the same generating function for a restricted set of observables.

Therefore,

\mathcal F(\mathcal R_1)=
\mathcal F(\mathcal R_2)
\tag{14.2}

does not imply

\mathcal R_1=\mathcal R_2.
\tag{14.3}

It establishes only that the models share the same image under the specified forward map.

14.2 Identifiability

A model is identifiable relative to if the analytic data uniquely determine the model up to a declared equivalence relation.

Let denote the chosen equivalence on physical models. The appropriate requirement is

\mathcal F(\mathcal R_1)=
\mathcal F(\mathcal R_2)
\quad\Longrightarrow\quad
\mathcal R_1\approx\mathcal R_2.
\tag{14.4}

This is not guaranteed by analytic continuation. It must be proved for the model class and the chosen observable data.

14.3 Minimal reconstruction data

A candidate reconstruction program should determine which data are sufficient. Depending on the theory, these may include:

* the generating function and its domain of holomorphy;
* the singular set and local singularity types;
* the zero distribution and its scaling behavior;
* monodromy and branch-selection rules;
* asymptotic and transseries data;
* contour and boundary-condition information;
* normalized correlation functions;
* positivity, spectral, or stability constraints;
* a definition of the physical state space and observable algebra.

Not every item is needed in every theory. The task is to establish a minimal sufficient set rather than to accumulate mathematical data without a reconstruction criterion.

15. A Stability Criterion for Branch Correspondence

A branch relationship can exist mathematically yet be unstable under perturbations. If a tiny change in the action, contour, regulator, or input data changes the branch structure, the proposed correspondence may have limited explanatory power.

15.1 Perturbing the generating function

Let depend on a perturbation parameter . Suppose a zero satisfies

Z(\lambda_*(\varepsilon);\varepsilon)=0.
\tag{15.1}

If

\frac{\partial Z}{\partial\lambda}
(\lambda_*(0);0)\neq0,
\tag{15.2}

then the implicit-function theorem gives a locally differentiable zero trajectory, and

\frac{d\lambda_*}{d\varepsilon}

\frac{\partial_\varepsilon Z}
{\partial_\lambda Z}
\bigg|{(\lambda*(\varepsilon),\varepsilon)}.
\tag{15.3}

A simple zero therefore moves continuously under sufficiently regular perturbations.

At a multiple zero, condition (15.2) fails. The zero may split into several zeros with fractional-power dependence on the perturbation, reflecting a more delicate local branch structure.

15.2 Stability of a branch relation

Let and be branches associated with two proposed regimes. A stability analysis should assess:

* whether the branches persist under perturbations;
* whether the continuation paths remain admissible;
* whether singularities move continuously or collide;
* whether the physical admissibility conditions remain satisfied;
* whether the observable correspondence survives the perturbation.

A formal continuation that exists only under exact fine-tuning may still be mathematically valid, but it should not be presented as a robust explanation of distinct regimes without further evidence.

15.3 Conditioning of the reconstruction map

If the reconstruction map is differentiable, its local sensitivity can be represented schematically by

\delta\mathcal R

D\mathfrak P\\delta\\mathfrak A
+o(\|\delta\mathfrak A\|).
\tag{15.4}

A large norm of indicates that small changes in analytic data can produce large changes in the reconstructed physical description.

Because physical models are not generally elements of a single normed vector space, this equation is schematic until appropriate metrics on the data and model spaces have been defined. A concrete application must specify those spaces and norms.

ACTR’s stability requirement is thus a research criterion rather than a universal theorem: robust branch correspondence requires controlled dependence on the analytic data used to establish it.

16. Falsifiable Consequences and Diagnostic Predictions

A framework intended to connect analytic structure with physical regimes must specify what would count against a proposed correspondence.

16.1 The common-germ test

For two candidate descriptions, identify an overlapping domain where both are claimed to be analytic. If they disagree there on the same purported generating function, the common-germ claim fails unless the discrepancy is explained by a declared normalization, transformation, or branch choice.

The test is especially sharp when the functions agree on an open set: the identity theorem fixes their analytic relationship throughout the connected common domain.

16.2 The singularity-consistency test

A proposed branch transition should be checked against the singularities of the exact object and of the relevant observables.

If the claimed physical transition is supposed to arise from a singularity, but the relevant observable remains analytic under the stated limit and assumptions, the proposed singularity mechanism is unsupported.

Conversely, a nonanalyticity in a thermodynamic limit may support a phase-transition interpretation, but only after the limiting procedure and observable are explicitly identified.

16.3 The branch-admissibility test

Every proposed physical branch must satisfy the applicable reality, positivity, normalization, stability, and causal requirements.

A branch that violates a necessary physical condition cannot be identified with the intended physical regime merely because it is analytically reachable.

16.4 The reconstruction test

The same analytic data may be compatible with several physical models. If the theory cannot distinguish them using its declared observables and reconstruction assumptions, then the physical interpretation is not identifiable.

This does not refute the mathematical branch relation. It limits what can be inferred from it.

16.5 The perturbative-completeness test

If two proposed regimes are distinguished only by a perturbative expansion, one must determine whether nonperturbative contributions alter the claimed distinction.

Agreement to every order in a formal expansion is not sufficient to establish equality of the underlying functions.

16.6 The limit-order test

If the proposed regime depends on a continuum, thermodynamic, semiclassical, or infinite-volume limit, test whether the relevant analytic continuation commutes with that limit.

If it does not, the theory must state which order defines the physical quantity and why.

Together, these tests turn ACTR from a broad analogy into an auditable research program.

17. Research Program and Technical Milestones

The framework can be developed through a sequence of increasingly demanding tasks.

Stage I — Finite-dimensional analytic models

Begin with integrals of the form

Z(\lambda)=
\int_{\mathcal C}
e^{-S(z,\lambda)}a(z,\lambda)\,dz
\tag{17.1}

where the contour, action, and parameter domain are explicit.

Prove holomorphy on the claimed domain, classify zeros and singularities, and determine the continuation structure. Compare exact results with saddle-point approximations.

Success criterion: a complete analytic description of a nontrivial model, including a controlled account of its branches and limiting behavior.

Stage II — Branch and monodromy classification

For models with multiple branches, determine the regular domain, the relevant fundamental group, and the monodromy action. Establish which branch relations are invariant under permissible changes of representation.

Success criterion: a classification that distinguishes intrinsic branch structure from branch choices introduced by a particular formula.

Stage III — Asymptotic and nonperturbative reconstruction

Develop Borel or other summation methods where appropriate. Determine which additional data are required beyond perturbative coefficients, and quantify the role of exponentially small sectors.

Success criterion: a reconstruction procedure with explicit assumptions and an error or ambiguity analysis.

Stage IV — Statistical-mechanical limits

Study sequences of finite-volume partition functions. Relate complex zeros to limiting free-energy singularities and characterize the scaling laws governing the approach to critical points.

Success criterion: a rigorous link between the finite-size analytic structure and a specified thermodynamic regime.

Stage V — Quantum field theory

Select a model with a well-defined regularization and a known reconstruction framework. Compare Euclidean and Lorentzian correlation functions, identify boundary prescriptions, and establish the conditions under which continuation preserves the required physical structure.

Success criterion: an explicit correspondence theorem for a particular theory, not merely a formal Wick rotation.

Stage VI — Physical identifiability

Specify a class of models and an observable family. Determine whether the analytic data uniquely identify a physical model up to a stated equivalence relation.

Success criterion: an injectivity or classification theorem, or a concrete counterexample demonstrating non-identifiability.

Stage VII — Predictive applications

Only after the earlier stages are complete should the framework be used to propose new physical phenomena. Predictions should arise from a derived singularity, zero distribution, branch relation, or reconstruction condition and should be expressed in measurable quantities.

Success criterion: a prediction whose parameter choices and analytic assumptions are fixed independently of the data used to test it.

18. Limitations and Open Problems

The proposed theory is not a universal explanation of physical reality. It is a framework for investigating a particular class of mathematical relationships.

18.1 No guarantee of a common generating function

Some physical descriptions may not admit a common analytic generating object of the form (1.1). Others may share only a restricted family of observables.

The existence of a common representation must be demonstrated in each application.

18.2 No automatic physical meaning for singularities

Complex singularities may reflect genuine physical thresholds, spectral features, or critical behavior. They may also arise from normalization, coordinates, approximations, or the chosen representation.

The physical significance of a singularity is not determined by its complex-analytic type alone.

18.3 Nonuniqueness of analytic reconstruction

A local analytic germ can have multiple continuations when the relevant domain is not simply connected or when singularities create nontrivial monodromy. Asymptotic expansions may also fail to determine exponentially small contributions.

A reconstruction theorem must therefore specify the analytic data and the uniqueness conditions it uses.

18.4 The continuum and infinite-volume problems

Quantum field theories often involve regulators, renormalization, and limits in which analyticity may not be preserved uniformly. Thermodynamic phase transitions likewise depend on infinite-volume behavior.

The finite-dimensional integral cannot simply be assumed to retain all its analytic properties after these operations.

18.5 Equivalence depends on the declared physical structure

Two models may agree on partition functions or selected correlation functions yet differ in their state spaces, superselection sectors, global observables, or dynamics.

Any claim of equivalence must state which structures are required to be preserved.

18.6 The foundational question remains open

The strongest possible interpretation of ACTR would be that apparently different physical descriptions are manifestations of a deeper analytic object. The mathematical framework permits this possibility but does not establish it universally.

The unresolved task is to identify a nontrivial class of physical theories for which the common analytic object can be derived, its branches classified, and its physical reconstruction proved rather than postulated.

19. Conclusion: Analytic Unity Without Presumed Physical Identity

The Analytic Continuation Theory of Reality begins from a simple but consequential observation: a single analytic object can support multiple local descriptions, asymptotic sectors, boundary values, and limiting regimes.

The generating function

Z(\lambda)=
\int_{\mathcal X}
e^{-S(x,\lambda)}\,d\mu(x)
\tag{19.1}

offers a natural setting in which to investigate this possibility. Its derivatives encode response information; its zeros constrain the logarithmic free energy; its singularities delimit analytic domains; its branch structure records path-dependent continuation; and its asymptotic expansions describe behavior in distinct parameter sectors.

The mathematical results establish several principles.

First, holomorphy must be proved from the integral’s convergence and parameter dependence. Second, zeros, poles, branch points, and essential singularities play different roles and cannot be treated as interchangeable markers of physical transitions. Third, Stokes phenomena and asymptotic sector changes can reorganize a description without creating a singularity in the exact function. Fourth, singular limits can generate physical nonanalyticities even when the finite-system generating functions remain analytic.

The central theorem provides a conditional criterion for analytic branch correspondence. It establishes that regime-specific generating data can be related through a common germ when continuation exists, observables continue consistently, singularities and normalization are controlled, and physical reconstruction maps are specified. A stronger claim of physical equivalence requires additional structure-preserving correspondence between states, observables, dynamics, and operational predictions.

This separation is not a weakness of the framework. It is its defining discipline.

A mathematical unity can be genuine without being an identity of physical interpretations. A pair of descriptions can be analytically connected while remaining operationally inequivalent. Conversely, descriptions that look radically different may be related by a rigorous continuation and reconstruction procedure.

The most promising research direction is therefore not to assert that all physical realities are branches of one function. It is to determine, theory by theory, when a common analytic structure exists, what its singularities and monodromy reveal, what information is lost in asymptotic truncations, and what additional conditions permit physical reconstruction.

The governing principle of ACTR is:

Analytic continuation establishes a relation between mathematical descriptions. Physical equivalence must be established by a separate theorem.

Appendix A. A Compact Formal Specification of ACTR

The following definitions summarize the framework in a form suitable for implementation in a particular mathematical model.

A.1 Analytic data

Define the analytic data record

\mathfrak D_Z=
(\Lambda,Z,\Sigma_Z,\mathcal Z_Z,\mathfrak M_Z,\mathfrak A_Z),
\tag{A.1}

where:

* is the domain of definition;
* is the generating function or analytic germ;
* is the relevant singular set;
* is the zero set;
* records monodromy data where applicable;
* records the asymptotic sectors and their domains.

For path-integral models, the record should be augmented with contour, regularization, and boundary-condition data.

A.2 Branch record

For a continuation path , define

\mathfrak B_i=
\left(
\gamma_i,
\operatorname{Cont}_{\gamma_i}Z_0,
\mathfrak O_i,
\mathfrak r_i
\right),
\tag{A.2}

where is the selected family of observables and is the physical reconstruction prescription.

Two records are analytically related when the continuation and observable-compatibility conditions of Theorem 6.1 hold.

A.3 Physical reconstruction

Let

\mathfrak P_i=\mathfrak r_i(\mathfrak B_i)
\tag{A.3}

denote the resulting physical model or regime, whenever the reconstruction is mathematically defined.

The inverse problem is to determine whether is unique, whether it preserves the required physical structures, and whether different branches reconstruct equivalent models.

A.4 ACTR audit conditions

A proposed application should report:

* The exact definition of .
* The domain on which is proved holomorphic.
* The singularities, zeros, and branch points relevant to the analysis.
* The continuation paths and any boundary-value prescriptions.
* The asymptotic expansions and their domains of validity.
* The role of contours, regulators, and limiting procedures.
* The observable family used to compare regimes.
* The physical reconstruction map.
* The precise equivalence relation claimed.
* The evidence that would falsify the proposed correspondence.

A theory that cannot supply these elements may still provide a useful analogy, but it has not yet established a rigorous analytic continuation theory of the physical regimes it seeks to relate.

Appendix B. Three Claims That Must Remain Distinct

Claim	Mathematical or physical requirement	What it establishes
A common generating function exists	A well-defined shared integral or generating functional	Common representation
Two descriptions are analytic branches of one object	A common germ, admissible continuation, and consistent observable relations	Analytic branch correspondence
Two descriptions are physically equivalent	A specified structure-preserving correspondence of physical states, observables, dynamics, and predictions	Equivalence under a declared physical criterion

These claims form a hierarchy of increasingly demanding obligations, not a chain of automatic implications.

Selected References

The following works provide established mathematical and physical foundations for the proposed framework. They are background sources, not evidence that ACTR itself has already been established as a distinct physical theory.

* Ahlfors, L. V. Complex Analysis. 3rd ed. McGraw-Hill, 1979.
* Conway, J. B. Functions of One Complex Variable I. 2nd ed. Springer, 1978.
* Olver, F. W. J. Asymptotics and Special Functions. A K Peters, 1997.
* Bleistein, N., and Handelsman, R. A. Asymptotic Expansions of Integrals. Dover Publications, 1986.
* Berry, M. V. “Uniform Asymptotic Smoothing of Stokes’s Discontinuities.” Proceedings of the Royal Society A 422 (1989): 7–21.
* Écalle, J. Les fonctions résurgentes. Publications Mathématiques d’Orsay, 1981–1985.
* Zinn-Justin, J. Quantum Field Theory and Critical Phenomena. 4th ed. Oxford University Press, 2002.
* Itzykson, C., and Drouffe, J.-M. Statistical Field Theory. Cambridge University Press, 1989.
* Lee, T. D., and Yang, C. N. “Statistical Theory of Equations of State and Phase Transitions. II. Lattice Gas and Ising Model.” Physical Review 87 (1952): 410–419.
* Yang, C. N., and Lee, T. D. “Statistical Theory of Equations of State and Phase Transitions. I. Theory of Condensation.” Physical Review 87 (1952): 404–409.
* Osterwalder, K., and Schrader, R. “Axioms for Euclidean Green’s Functions.” Communications in Mathematical Physics 31 (1973): 83–112.
* Osterwalder, K., and Schrader, R. “Axioms for Euclidean Green’s Functions II.” Communications in Mathematical Physics 42 (1975): 281–305.
* Witten, E. “Analytic Continuation of Chern–Simons Theory.” In Chern–Simons Gauge Theory: 20 Years After, AMS/IP Studies in Advanced Mathematics, 2011.
* Pham, F. Singularities of Integrals. Springer, 2011.
* Costin, O. Asymptotics and Borel Summability. Chapman & Hall/CRC, 2008.

The decisive next step is to apply the framework to a specific generating functional and prove a nontrivial result about its branch structure, reconstruction map, or physical identifiability. Until that is done, ACTR is best understood as a proposed mathematical research program with a conditional theorem—not as an established universal theory of reality.
