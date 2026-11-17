# Correlation–Causal Cone Disparity (CCCD)

## A Covariant Framework for the Quantitative Separation of Correlation Support and Causal-Response Support in Relativistic Quantum Theory

Research status: Foundational framework and proposed research programme\
Subject: Relativistic quantum field theory, quantum correlations, causal response, spacetime support, operational distinguishability, and universal correlation–causation relations

## Abstract

Correlation and causal influence are mathematically distinct relations. A quantum field theory may exhibit nonvanishing correlations between observables localized at spacelike-separated regions while simultaneously enforcing the vanishing of retarded response between those regions. The former describes statistical dependence within a physical state; the latter describes the response of an observable to a specified intervention or perturbation. Their supports therefore need not coincide.

This work develops Correlation–Causal Cone Disparity (CCCD) as a quantitative framework for characterizing that mismatch. The central objects are a state-dependent correlation function \\(K\_\omega(x,y)\\), a retarded response function \\(R\_\omega(x,y)\\), and their respective supports within a finite observational domain. The framework distinguishes exact mathematical support from experimentally resolvable support, pointwise nonvanishing from distributional support, and causal propagation from statistical dependence.

A finite-domain disparity functional is constructed from spacetime measures on the correlation and response supports. Several complementary measures are introduced: absolute support discrepancy, normalized correlation-only support, response-only support, overlap, and scale-dependent disparity profiles. These quantities are explicitly dependent on the observable pair, state, operational protocol, spacetime region, resolution scale, and threshold convention. They are not presumed to be universal constants.

The relativistic foundation is established through the distinction between the Wightman function, the commutator, and the retarded Green function. In a microcausal relativistic quantum field theory, the commutator vanishes at spacelike separation, enforcing the absence of retarded causal response there, while the Wightman correlation can remain nonzero. A massive free scalar field provides an explicit example.

The paper then formulates the principal research question: whether the disparity between correlation and causal-response support obeys universal quantitative constraints determined by the physical state, field content, spectral structure, mass scale, temperature, and spacetime geometry. The proposed research programme includes spectral representations, Källén–Lehmann analysis, finite-resolution operational reconstruction, controlled state comparisons, and statistical tests of candidate scaling laws.

The basic support distinction is established physics. The CCCD framework is a proposed quantitative organization of that distinction. Its scientific novelty would depend on proving a nontrivial universal inequality, identifying a new invariant, or establishing a state-sensitive scaling law that cannot be reduced to known consequences of microcausality, spectral theory, clustering, or fluctuation–dissipation relations.

Central proposition: Correlation support and causal-response support are different structures, and their disparity may contain quantitative information about the state and dynamical organization of a quantum field.

## 1. Introduction

### 1.1 The distinction between correlation and causation

In ordinary classical intuition, a relationship between two events is often interpreted through a chain of influence. If two physical quantities exhibit statistical dependence, one may suspect that one has affected the other, or that both have been affected by a common cause.

Relativistic quantum theory requires a more careful distinction.

Two observables can exhibit nonzero correlations even when the spacetime separation between their localization regions is spacelike. Yet a local intervention at one region cannot produce a causal response at the other region outside the light cone, provided the theory satisfies relativistic microcausality and the intervention is implemented through the appropriate local operations.

Thus two different mathematical questions arise:

1. Where can statistical dependence be detected?
2. Where can a local perturbation produce a causal response?

The answers are not generally identical.

The first question concerns the state of the field. The second concerns its dynamical response under a specified perturbation.

The distinction is not merely semantic. It separates the geometry of quantum statistical dependence from the geometry of causal propagation.

### 1.2 The CCCD hypothesis

Let \\(M\\) be a spacetime manifold equipped with Lorentzian metric \\(g\_{\mu\nu}\\). Let \\(x,y\in M\\) denote spacetime points, or more generally labels for localized observable regions.

For a specified quantum state \\(\omega\\), define:

\\[ K\_\omega(x,y) \\]

as a connected correlation function, and

\\[ R\_\omega(x,y) \\]

as a retarded causal-response function.

Their supports are formally:

\\[ \boxed{ \mathcal S_K(\omega) = \\{(x,y)\in M\times M: K\_\omega(x,y)\neq0\\} } \\]

and

\\[ \boxed{ \mathcal S_R(\omega) = \\{(x,y)\in M\times M: R\_\omega(x,y)\neq0\\}. } \\]

These definitions require qualification for distributions, which will be addressed below.

The fundamental CCCD proposition is:

\\[ \boxed{ \mathcal S_K(\omega) \neq \mathcal S_R(\omega) } \\]

for physically relevant relativistic quantum states and observables.

This proposition alone is not a new theorem. It expresses a familiar feature of quantum field theory. The proposed research question is whether the difference admits a systematic quantitative characterization.

### 1.3 Research objectives

The present work has six objectives:

1. Define correlation and causal-response supports in a mathematically consistent manner.
2. Construct finite-domain measures of their discrepancy.
3. Establish the relativistic field-theoretic basis for their separation.
4. Derive explicit examples in which correlation extends beyond causal-response support.
5. Identify possible universal relations involving state, spectral structure, and spacetime geometry.
6. Formulate experimental and computational tests capable of distinguishing a genuinely new CCCD law from established results.

The theory is deliberately operational. It does not presume that nonzero correlation is evidence of a hidden superluminal mechanism, nor that vanishing response proves the absence of every conceivable underlying mediator.

## 2. Mathematical foundations

### 2.1 Spacetime and localization

Let \\((M,g)\\) be a globally hyperbolic Lorentzian spacetime of dimension \\(d\\). Its causal structure is determined by the metric and the associated light cones.

For two events \\(x,y\in M\\), define:

\\[ x\preceq y \\]

if \\(y\\) lies in the causal future of \\(x\\), including the null boundary.

The chronological future is denoted \\(I^+(x)\\), and the causal future by \\(J^+(x)\\). Correspondingly, the causal past is \\(J^-(x)\\).

Two events are spacelike separated if neither lies in the causal future or past of the other:

\\[ x\notin J^+(y), \qquad y\notin J^+(x). \\]

For field-theoretic observables, point localization is often too singular. We therefore introduce localized test functions \\(f,g\in C_0^\infty(M)\\) and define smeared observables:

\\[ \mathcal O(f) = \int_M d\mu_g(x)\\,f(x)\mathcal O(x), \\]

where

\\[ d\mu_g(x)=\sqrt{|g|}\\,d^dx. \\]

The support of \\(f\\) determines the spacetime region in which the observable is localized.

This allows the formalism to be applied to finite detector regions rather than idealized point measurements.

### 2.2 Quantum states and expectation values

Let \\(\mathcal A(M)\\) be the local observable algebra associated with the spacetime. A state is a positive normalized linear functional:

\\[ \omega:\mathcal A(M)\rightarrow\mathbb C, \\]

satisfying:

\\[ \omega(A^\dagger A)\geq0, \qquad \omega(I)=1. \\]

For two observables \\(A(x)\\) and \\(B(y)\\), define the connected correlation:

\\[ \boxed{ K\_\omega(x,y) = \omega(A(x)B(y)) - \omega(A(x))\omega(B(y)). } \\]

For Hermitian observables, the complex ordering dependence may be handled by considering the real symmetrized correlation:

\\[ K\_\omega^{\mathrm{sym}}(x,y) = \frac12\omega(\\{A(x),B(y)\\}) - \omega(A(x))\omega(B(y)). \\]

The choice between ordered and symmetrized correlation functions is physically consequential. It must be specified before a CCCD measure is calculated.

The connected function removes the product of one-point expectations. It therefore isolates statistical dependence at the level of the chosen observables.

It does not, by itself, distinguish quantum entanglement from classical statistical correlation.

### 2.3 Causal response

Let a perturbation couple to an observable \\(B\\) through an external source \\(j(y)\\):

\\[ H\_{\mathrm{int}}(t) = -\int\_{\Sigma_t}d\Sigma_y\\,j(y)B(y). \\]

The linear response of \\(A(x)\\) to this perturbation is defined by:

\\[ \delta\omega(A(x)) = \int_M d\mu_g(y)\\, R\_\omega^{A B}(x,y)j(y) + O(j^2). \\]

With a conventional sign choice, the retarded response function is:

\\[ \boxed{ R\_\omega^{A B}(x,y) = i\theta(x\succ y) \omega([A(x),B(y)]). } \\]

Here \\(x\succ y\\) means that \\(x\\) lies to the future of \\(y\\), and units with \\(\hbar=1\\) are used.

The sign depends on the convention for the interaction Hamiltonian and response definition. None of the support results below depends on this sign.

The Heaviside factor imposes retarded temporal ordering. The commutator determines whether a perturbation can affect the later observable.

This is the central distinction:

\\[ K\_\omega^{AB}(x,y) \quad\text{measures correlation}, \\]

whereas

\\[ R\_\omega^{AB}(x,y) \quad\text{measures linear causal response}. \\]

They are different functions, with different physical meanings.

### 2.4 Distributional support

Quantum field operators are generally operator-valued distributions. Their correlation and response functions need not be ordinary functions.

Consequently, the expression \\(K(x,y)\neq0\\) should not be interpreted naively at every point.

For a distribution \\(T\\), define its distributional support:

\\[ \operatorname{supp}T = M\times M\setminus \bigcup \left\\{ U: T|\_U=0 \right\\}, \\]

where \\(U\\) ranges over open subsets of \\(M\times M\\).

The rigorous support definitions are therefore:

\\[ \boxed{ \mathcal S_K = \operatorname{supp}K\_\omega, \qquad \mathcal S_R = \operatorname{supp}R\_\omega. } \\]

For detector measurements, one instead works with smeared quantities:

\\[ K\_\omega(f,g) = \omega(\mathcal O(f)\mathcal O(g)) - \omega(\mathcal O(f))\omega(\mathcal O(g)), \\]

and

\\[ R\_\omega(f,g) = \int d\mu_g(x)d\mu_g(y)\\, f(x)R\_\omega(x,y)g(y). \\]

The support of the smeared response depends on the detector profiles and the allowed source functions.

This distinction prevents a mathematical distributional statement from being mistaken for a directly measurable pointwise assertion.

## 3. Relativistic microcausality and support separation

### 3.1 Microcausality

A relativistic quantum field theory satisfying microcausality obeys:

\\[ \boxed{ [\mathcal O_A(x),\mathcal O_B(y)]=0 } \\]

whenever \\(x\\) and \\(y\\) are spacelike separated, for bosonic local observables.

For fermionic fields, the corresponding condition is graded commutativity; physical local observables still commute at spacelike separation.

Since the retarded response contains the commutator,

\\[ R\_\omega^{AB}(x,y) = i\theta(x\succ y) \omega([A(x),B(y)]), \\]

it follows that:

\\[ \boxed{ R\_\omega^{AB}(x,y)=0 \quad \text{for spacelike-separated }x,y. } \\]

The result is state-independent once the operator algebra satisfies microcausality, although the nonzero values of the response inside the causal region may depend on the state.

Thus:

\\[ \mathcal S_R \subseteq \overline{J^+} \\]

in the appropriate ordered pair space, subject to the precise conventions for source and response arguments.

This is the causal-support constraint.

### 3.2 Correlation functions need not vanish at spacelike separation

The Wightman function is:

\\[ W\_\omega(x,y) = \omega(\mathcal O(x)\mathcal O(y)). \\]

Microcausality constrains its antisymmetric part:

\\[ W\_\omega(x,y)-W\_\omega(y,x) = \omega([\mathcal O(x),\mathcal O(y)]). \\]

At spacelike separation:

\\[ W\_\omega(x,y)=W\_\omega(y,x). \\]

But this does not imply:

\\[ W\_\omega(x,y)=0. \\]

The symmetric part may remain nonzero.

For connected correlations, one can therefore have:

\\[ K\_\omega(x,y)\neq0 \\]

while simultaneously:

\\[ R\_\omega(x,y)=0. \\]

The resulting spacetime region belongs to the correlation support but not to the causal-response support.

This is the elementary relativistic manifestation of CCCD.

### 3.3 Correlation does not imply signaling

Suppose two laboratories, \\(A\\) and \\(B\\), occupy spacelike-separated regions. A joint state may contain nontrivial correlations between their observables.

A local trace-preserving quantum operation at \\(A\\) cannot alter the unconditional statistics observed at \\(B\\), under the standard assumptions of local quantum operations and relativistic locality.

Conditioned statistics can change when outcomes are compared, but that comparison requires classical communication or another causal channel.

Therefore the existence of a nonzero spacelike correlation does not establish a superluminal causal influence.

The distinction between unconditional response and conditional statistical updating is essential. CCCD concerns the former when defining causal-response support.

### 3.4 The two support regions

Introduce the spacelike domain:

\\[ \mathcal D\_{\mathrm{SL}} = \\{(x,y)\in M\times M: x\notin J^+(y),\ y\notin J^+(x)\\}. \\]

For a microcausal theory:

\\[ \mathcal S_R\cap\mathcal D\_{\mathrm{SL}} = \varnothing. \\]

Yet it is possible that:

\\[ \mathcal S_K\cap\mathcal D\_{\mathrm{SL}} \neq\varnothing. \\]

Consequently:

\\[ \boxed{ \mathcal S_K\setminus\mathcal S_R \neq\varnothing. } \\]

The converse inclusion is not generally guaranteed. Correlations can vanish at some locations where a response function remains nonzero, depending on the state and observable definitions.

The two supports are therefore not generally nested.

## 4. A canonical example: the massive free scalar field

The support distinction can be demonstrated explicitly in a standard relativistic quantum field theory.

### 4.1 Field equation

Consider a real scalar field \\(\phi(x)\\) in \\(3+1\\)-dimensional Minkowski spacetime, satisfying:

\\[ (\Box+m^2)\phi(x)=0, \\]

with:

\\[ \Box = \partial_t^2-\nabla^2. \\]

In the Minkowski vacuum \\(|0\rangle\\), the Wightman function is:

\\[ W_0(x-y) = \langle0|\phi(x)\phi(y)|0\rangle. \\]

Let:

\\[ s^2 = (t_x-t_y)^2 - |\mathbf x-\mathbf y|^2. \\]

For spacelike separation, define:

\\[ r = \sqrt{|\mathbf x-\mathbf y|^2-(t_x-t_y)^2}. \\]

The vacuum Wightman function is:

\\[ \boxed{ W_0(x-y) = \frac{m}{4\pi^2r}K_1(mr), \qquad s^2<0, } \\]

where \\(K_1\\) is the modified Bessel function of the second kind.

For \\(m>0\\) and \\(r>0\\),

\\[ K_1(mr)>0. \\]

Therefore:

\\[ \boxed{ W_0(x-y)\neq0 \quad \text{for spacelike separation}. } \\]

The vacuum one-point function vanishes, so the connected two-point function is simply:

\\[ K_0(x,y)=W_0(x-y). \\]

Thus the correlation support includes spacelike-separated pairs.

### 4.2 Retarded response

The retarded Green function is proportional to:

\\[ G_R(x-y) = i\theta(t_x-t_y) \langle0|[\phi(x),\phi(y)]|0\rangle, \\]

with the overall sign depending on convention.

The Pauli–Jordan commutator function vanishes outside the light cone:

\\[ [\phi(x),\phi(y)]=0 \qquad \text{for }s^2<0. \\]

Hence:

\\[ \boxed{ G_R(x-y)=0 \quad \text{for spacelike separation}. } \\]

The result is exact, not an approximation.

### 4.3 Explicit disparity

For the massive vacuum:

\\[ K_0(x,y)\neq0 \quad\text{at spacelike separation}, \\]

while:

\\[ G_R(x-y)=0 \quad\text{at spacelike separation}. \\]

Therefore:

\\[ \boxed{ \mathcal S_K \not\subseteq \mathcal S_R. } \\]

This example demonstrates the fundamental CCCD phenomenon using established quantum field theory.

It does not establish a new physical law. It supplies a controlled baseline against which a new quantitative CCCD proposal must be tested.

### 4.4 Massless limit

For \\(m\rightarrow0\\), using:

\\[ K_1(z)\sim\frac1z \qquad (z\rightarrow0), \\]

the spacelike Wightman function becomes:

\\[ W_0(x-y) \sim \frac{1}{4\pi^2r^2}. \\]

It remains nonzero for spacelike separation.

Thus the support distinction is not a peculiarity of massive fields.

### 4.5 Interpretation

The vacuum is not an absence of correlations. It is a state with nontrivial quantum fluctuations and spatially structured correlations.

The retarded function, by contrast, describes the propagation of a perturbation through the field's causal dynamics.

The vacuum correlation can therefore extend over spacelike-separated regions without enabling a signal to propagate between them.

This is the simplest concrete realization of the CCCD thesis.

## 5. Defining a quantitative disparity

The central mathematical challenge is to turn the qualitative support difference into a well-defined quantity.

### 5.1 Finite observational domain

Let:

\\[ \Omega\subset M\times M \\]

be a finite observational domain.

It may be defined by:

- a bounded laboratory spacetime region;
- a finite interval of source–detector separations;
- a specified set of detector trajectories;
- a compact region of spacetime pair coordinates;
- or a finite family of smeared observables.

A measure on spacetime is required.

Let:

\\[ d\mu\_\Omega(x,y) = w(x,y)\\, d\mu_g(x)d\mu_g(y), \\]

where \\(w\geq0\\) is a specified nonnegative weight function.

The weight may encode detector coverage, sampling density, or a chosen geometrical normalization. It must not be selected after observing the result in a way that artificially enhances the disparity.

Define the total observational measure:

\\[ \mu\_\Omega(\Omega) = \int\_\Omega d\mu\_\Omega. \\]

For finite, nonzero \\(\mu\_\Omega(\Omega)\\), normalized support measures can be constructed.

### 5.2 Absolute support measures

Define:

\\[ \mu_K = \mu\_\Omega(\mathcal S_K\cap\Omega), \\]

\\[ \mu_R = \mu\_\Omega(\mathcal S_R\cap\Omega), \\]

and:

\\[ \mu\_{K\cap R} = \mu\_\Omega( \mathcal S_K\cap\mathcal S_R\cap\Omega ). \\]

The correlation-only support measure is:

\\[ \mu\_{K\setminus R} = \mu\_\Omega( (\mathcal S_K\setminus\mathcal S_R)\cap\Omega ). \\]

Similarly:

\\[ \mu\_{R\setminus K} = \mu\_\Omega( (\mathcal S_R\setminus\mathcal S_K)\cap\Omega ). \\]

These quantities distinguish the two possible directions of support mismatch.

### 5.3 Symmetric support discrepancy

A natural first measure is the normalized symmetric difference:

\\[ \boxed{ \mathfrak D\_{\mathrm{CCCD}} = \frac{ \mu\_\Omega[ (\mathcal S_K\triangle\mathcal S_R)\cap\Omega ] }{ \mu\_\Omega(\Omega) }. } \\]

Here:

\\[ \mathcal S_K\triangle\mathcal S_R = (\mathcal S_K\setminus\mathcal S_R) \cup (\mathcal S_R\setminus\mathcal S_K). \\]

If the supports agree almost everywhere within the observational domain:

\\[ \mathfrak D\_{\mathrm{CCCD}}=0. \\]

If they are disjoint almost everywhere:

\\[ \mathfrak D\_{\mathrm{CCCD}} = \frac{\mu_K+\mu_R}{\mu\_\Omega(\Omega)}. \\]

Since the union cannot exceed \\(\Omega\\), the measure lies in:

\\[ 0\leq\mathfrak D\_{\mathrm{CCCD}}\leq1. \\]

This quantity is mathematically simple, but it has a major limitation: exact support is often unstable under arbitrarily small perturbations and difficult to reconstruct experimentally.

### 5.4 Correlation-only and response-only disparity

Define the normalized directional components:

\\[ \boxed{ \mathfrak D\_{K\setminus R} = \frac{\mu\_{K\setminus R}} {\mu\_\Omega(\Omega)} } \\]

and

\\[ \boxed{ \mathfrak D\_{R\setminus K} = \frac{\mu\_{R\setminus K}} {\mu\_\Omega(\Omega)}. } \\]

Then:

\\[ \mathfrak D\_{\mathrm{CCCD}} = \mathfrak D\_{K\setminus R} + \mathfrak D\_{R\setminus K}. \\]

These directional measures are physically useful because correlation-only support and response-only support need not have the same interpretation.

For microcausal theories, the first quantity is especially relevant when restricted to spacelike separation.

### 5.5 Spacelike disparity

Define:

\\[ \Omega\_{\mathrm{SL}} = \Omega\cap\mathcal D\_{\mathrm{SL}}. \\]

Since a microcausal theory has no spacelike retarded response, the spacelike correlation-only measure simplifies to:

\\[ \boxed{ \mathfrak D\_{\mathrm{SL}} = \frac{ \mu\_\Omega(\mathcal S_K\cap\Omega\_{\mathrm{SL}}) }{ \mu\_\Omega(\Omega) }. } \\]

Alternatively, normalize only by the spacelike observational region:

\\[ \boxed{ \widehat{\mathfrak D}\_{\mathrm{SL}} = \frac{ \mu\_\Omega(\mathcal S_K\cap\Omega\_{\mathrm{SL}}) }{ \mu\_\Omega(\Omega\_{\mathrm{SL}}) }. } \\]

The latter measures the fraction of the sampled spacelike domain occupied by correlation support.

The distinction between the two normalizations must be retained. The first quantifies spacelike disparity relative to the full experimental domain; the second quantifies its prevalence within the spacelike region.

### 5.6 Support overlap

Define the support-overlap coefficient:

\\[ \boxed{ \mathcal O\_{KR} = \frac{ \mu\_{K\cap R} }{ \mu_K+\mu_R-\mu\_{K\cap R} } } \\]

whenever the denominator is nonzero.

This is the measure-theoretic Jaccard overlap of the two supports.

It satisfies:

\\[ 0\leq\mathcal O\_{KR}\leq1. \\]

A value of unity indicates equality of supports up to sets of measure zero. A value of zero indicates disjoint supports up to measure-zero intersections.

This coefficient is useful for comparisons between states, models, and experimental configurations, but it is not an intrinsic scalar of the quantum state alone.

### 5.7 Support measures are not correlation strengths

A region where the correlation is infinitesimally small counts as part of the exact support just as much as a region where the correlation is large.

Thus support discrepancy alone discards amplitude information.

A complete CCCD analysis should therefore pair support measures with weighted amplitude measures.

## 6. Finite-resolution CCCD

### 6.1 Why exact support is experimentally inadequate

Suppose a correlation function has a nonzero but exponentially suppressed tail. Mathematically, that tail may extend over a very large region. Yet no finite experiment can reliably distinguish an arbitrarily small nonzero value from zero.

The exact support measure may therefore overstate the physically observable extent of correlations.

This is particularly important for massive fields, where spacelike vacuum correlations decay exponentially at large invariant distance.

A practical CCCD framework must incorporate finite resolution.

### 6.2 Thresholded support

Let \\(\varepsilon_K>0\\) and \\(\varepsilon_R>0\\) be specified detection thresholds.

Define:

\\[ \mathcal S_K^{(\varepsilon_K)} = \\{(x,y)\in\Omega: |K\_\omega(x,y)|>\varepsilon_K\\}, \\]

and:

\\[ \mathcal S_R^{(\varepsilon_R)} = \\{(x,y)\in\Omega: |R\_\omega(x,y)|>\varepsilon_R\\}. \\]

These are operationally resolvable supports.

The threshold must be calibrated relative to measurement noise, systematic error, and the statistical estimator used.

A more robust definition uses confidence bounds. For an estimator \\(\widehat K\\) with uncertainty \\(\sigma_K\\), define a detection region through:

\\[ |\widehat K(x,y)| > z\_\alpha\sigma_K(x,y), \\]

where \\(z\_\alpha\\) is a prespecified confidence multiplier.

An analogous definition applies to response.

The two thresholds need not be numerically equal because the correlation and response estimators may have different units, variances, and calibration uncertainties.

### 6.3 Resolution-dependent disparity

The finite-resolution discrepancy is:

\\[ \boxed{ \mathfrak D\_{\mathrm{CCCD}} (\varepsilon_K,\varepsilon_R;\Omega) = \frac{ \mu\_\Omega[ \mathcal S_K^{(\varepsilon_K)} \triangle \mathcal S_R^{(\varepsilon_R)} ] }{ \mu\_\Omega(\Omega) }. } \\]

The dependence on thresholds is part of the definition, not a nuisance to be hidden.

A stronger result would establish a stable plateau:

\\[ \mathfrak D\_{\mathrm{CCCD}} (\varepsilon_K,\varepsilon_R) \approx D\_\* \\]

over a finite range of reasonable thresholds.

Such a plateau would indicate that the measured disparity is not an artifact of a particular detection convention.

### 6.4 Smooth support weights

Instead of a binary threshold, define continuous detection weights:

\\[ q_K(x,y) = F_K\left( \frac{|K\_\omega(x,y)|}{\varepsilon_K} \right), \\]

\\[ q_R(x,y) = F_R\left( \frac{|R\_\omega(x,y)|}{\varepsilon_R} \right), \\]

where \\(F_K,F_R\\) are bounded monotonic functions satisfying:

\\[ F(0)=0, \qquad F(z)\rightarrow1 \quad(z\rightarrow\infty). \\]

One possible choice is:

\\[ F(z)=\frac{z^2}{1+z^2}. \\]

Then define:

\\[ \boxed{ \mathfrak D\_{\mathrm{soft}} = \frac1{\mu\_\Omega(\Omega)} \int\_\Omega |q_K(x,y)-q_R(x,y)| \\,d\mu\_\Omega. } \\]

This functional is continuous in the measured amplitudes and less sensitive to threshold crossings.

It is not a replacement for the exact support definition. It is an operationally regularized counterpart.

### 6.5 Amplitude-weighted disparity

To retain information about the magnitudes of correlation and response, define normalized amplitudes:

\\[ \widetilde K = \frac{|K\_\omega|}{K\_\*}, \qquad \widetilde R = \frac{|R\_\omega|}{R\_\*}, \\]

where \\(K\_\*,R\_\*>0\\) are declared reference scales.

Then:

\\[ \boxed{ \mathfrak D\_{\mathrm{amp}} = \frac1{\mu\_\Omega(\Omega)} \int\_\Omega \left| \widetilde K(x,y)-\widetilde R(x,y) \right| d\mu\_\Omega. } \\]

This expression is meaningful only after the normalization scales have been justified. Correlation and response generally have different physical dimensions, so subtracting their unnormalized amplitudes would be invalid.

The amplitude-weighted measure complements rather than replaces support disparity.

## 7. The correlation–response spectral relationship

The most promising route toward a universal CCCD law is spectral theory.

### 7.1 Commutator and anticommutator sectors

For a Hermitian bosonic observable \\(\mathcal O\\), define:

\\[ C\_\omega(x,y) = \omega([\mathcal O(x),\mathcal O(y)]) \\]

and:

\\[ N\_\omega(x,y) = \frac12\omega(\\{\delta\mathcal O(x),\delta\mathcal O(y)\\}), \\]

where:

\\[ \delta\mathcal O = \mathcal O-\omega(\mathcal O). \\]

The first quantity determines the retarded response. The second determines the symmetrized connected correlation.

In this sense, the two functions encode different sectors of the same quantum operator algebra:

- the commutator sector encodes dynamical response and causal propagation;
- the anticommutator sector encodes fluctuations and statistical correlations.

They are not independent in every quantum state, but neither are they generally identical or mutually determined by microcausality alone.

### 7.2 Fourier representation in stationary states

In a stationary homogeneous state, write:

\\[ N(\omega,\mathbf k) \\]

for the Fourier transform of the symmetrized correlation, and:

\\[ \rho(\omega,\mathbf k) \\]

for the spectral function associated with the commutator.

The retarded Green function has a spectral representation of the form:

\\[ G_R(\omega,\mathbf k) = \int\_{-\infty}^{\infty} \frac{d\omega'}{2\pi} \frac{\rho(\omega',\mathbf k)} {\omega-\omega'+i0}, \\]

up to convention-dependent factors.

The correlation spectrum and spectral density are distinct objects.

A state-dependent occupation factor may relate them in equilibrium.

### 7.3 Thermal equilibrium and fluctuation–dissipation

For a system in thermal equilibrium at inverse temperature \\(\beta\\), the Kubo–Martin–Schwinger condition implies a fluctuation–dissipation relation.

With a conventional spectral normalization:

\\[ \boxed{ N(\omega,\mathbf k) = \frac12 \coth\left(\frac{\beta\omega}{2}\right) \rho(\omega,\mathbf k). } \\]

Equivalently, the symmetrized correlation spectrum is related to the imaginary part of the retarded response.

The precise factors depend on Fourier and spectral-function conventions.

This relation is important for CCCD because it constrains the amplitude relationship between correlation and response in equilibrium.

It does not make their spacetime supports identical.

Indeed, a multiplicative frequency-domain relation can preserve a shared spectral support while the inverse Fourier transforms have different spacetime support properties due to the distinction between symmetric and retarded temporal structures.

### 7.4 Nonequilibrium states

Away from equilibrium, a universal fluctuation–dissipation relation generally fails.

The correlation and response functions may contain independent state-dependent information.

A possible CCCD research target is therefore to identify a generalized relation:

\\[ N\_\omega(\omega,\mathbf k) = \mathcal F\_\omega[ G_R(\omega,\mathbf k) ], \\]

where \\(\mathcal F\_\omega\\) is constrained by a measurable state descriptor.

Such a relation would need to be derived, not postulated.

The relevant state descriptors may include:

- occupation distributions;
- spectral densities;
- conserved charges;
- temperature where meaningful;
- chemical potentials;
- nonequilibrium distribution functions;
- entanglement structure;
- and local geometric data.

No universal form is assumed here.

### 7.5 The Källén–Lehmann representation

For a Lorentz-invariant vacuum state in a suitable scalar theory, the two-point function admits the representation:

\\[ \boxed{ W(x-y) = \int_0^\infty d\mu^2\\, \rho\_{\mathrm{KL}}(\mu^2) \Delta\_+(x-y;\mu^2), } \\]

where \\(\rho\_{\mathrm{KL}}\\) is a nonnegative spectral measure and \\(\Delta\_+\\) is the positive-frequency two-point function for mass \\(\mu\\).

The corresponding commutator function is:

\\[ \boxed{ \Delta(x-y) = \int_0^\infty d\mu^2\\, \rho\_{\mathrm{KL}}(\mu^2) \Delta\_\mu(x-y). } \\]

For a local relativistic theory, each Pauli–Jordan commutator function \\(\Delta\_\mu\\) vanishes at spacelike separation. Their spectral superposition does also.

But the positive-frequency functions \\(\Delta\_+\\) are generally nonzero there.

This yields a broad result:

Within the stated assumptions, spectral superposition preserves causal commutator support while allowing nonzero spacelike correlation support.

This is stronger than the single free-field example, but it is still a consequence of established spectral and locality structure rather than a new CCCD law.

## 8. Candidate universal CCCD laws

The central question is no longer whether correlation and response supports can differ. That is established. The question is whether their difference obeys a quantitative law that is stable across a meaningful class of states and theories.

A universal law must do more than restate microcausality. It must constrain the magnitude, spatial extent, scaling, or state dependence of the disparity.

### 8.1 The correlation-range function

A support measure over an arbitrary finite domain depends on the experimenter's chosen domain. A more physically interpretable quantity is a correlation-range profile.

In a stationary, spatially homogeneous system, let:

\\[ K\_\omega(t,\mathbf r) \\]

be the connected correlation function, with \\(\mathbf r=\mathbf x-\mathbf y\\).

For a fixed temporal separation \\(t\\), define the threshold correlation range:

\\[ \boxed{ L_K(\varepsilon;t) = \sup\left\\{ |\mathbf r|: |K\_\omega(t,\mathbf r)|>\varepsilon \right\\}. } \\]

If the set is empty, define \\(L_K=0\\). If it is unbounded, the range is infinite.

Similarly, define the response range:

\\[ \boxed{ L_R(\varepsilon;t) = \sup\left\\{ |\mathbf r|: |R\_\omega(t,\mathbf r)|>\varepsilon \right\\}. } \\]

These definitions require a common coordinate frame and an explicit normalization of the two amplitudes. Their thresholds are operational rather than intrinsically equal.

For an ideal microcausal relativistic theory:

\\[ R\_\omega(t,\mathbf r)=0 \qquad \text{whenever }|\mathbf r|>|t| \\]

in units \\(c=1\\). Hence:

\\[ L_R(\varepsilon;t)\leq |t| \\]

for a thresholded response support, provided the response is measured in the corresponding retarded orientation.

The correlation range need not obey this bound.

A candidate disparity range is:

\\[ \boxed{ \Delta L\_{\mathrm{CCCD}}(\varepsilon;t) = L_K(\varepsilon;t)-L_R(\varepsilon;t). } \\]

This is a useful diagnostic, but it is not yet a universal invariant. It depends on the observable, threshold, state, temporal separation, and detector resolution.

### 8.2 Spacelike correlation range

A more direct measure isolates the spacelike region.

For fixed \\(t\\), define:

\\[ \boxed{ L_K^{\mathrm{SL}}(\varepsilon;t) = \sup\left\\{ r>|t|: |K\_\omega(t,r)|>\varepsilon \right\\}. } \\]

This measures how far the resolvable correlation extends beyond the light-cone boundary.

For a microcausal theory, the corresponding retarded response vanishes throughout this region.

A natural research quantity is therefore:

\\[ \Delta L\_{\mathrm{SL}}(\varepsilon;t) = L_K^{\mathrm{SL}}(\varepsilon;t)-|t|. \\]

This measures the resolvable correlation extension beyond the causal cone. It should not be confused with a propagation speed: it describes a statistical correlation range, not a signal trajectory.

### 8.3 A proposed spectral correlation length

Suppose a connected equal-time correlation decays asymptotically as:

\\[ K\_\omega(0,r) \sim A\_\omega r^{-\alpha\_\omega} e^{-r/\xi_K}. \\]

Then \\(\xi_K\\) is a correlation length, assuming the exponential asymptotic regime exists.

The response may possess a separate characteristic scale, for example through its spectral poles, damping rates, or dispersion relation.

One can define:

\\[ \xi_R \\]

from the appropriate response decay or spectral structure, but the definition is model-dependent. In particular, the support of a retarded Green function may extend throughout the causal cone even when its amplitude decays rapidly.

Thus a response correlation length is not generally the same thing as a causal propagation range.

The candidate dimensionless ratio is:

\\[ \boxed{ \mathcal Q\_{\mathrm{CCCD}} = \frac{\xi_K}{\xi_R} } \\]

where both lengths are well-defined under the chosen operational prescription.

A possible universality claim would be:

\\[ \mathcal Q\_{\mathrm{CCCD}} \longrightarrow \mathcal Q\_\* \\]

near a critical point, within a universality class, or under a specified scaling limit.

This would be a meaningful research result only if \\(\mathcal Q\_\*\\) is independent of microscopic details that are irrelevant under the corresponding renormalization-group flow.

No such universal constant is asserted here.

### 8.4 A state-dependent disparity law

The strongest version of the CCCD programme would identify a functional relationship:

\\[ \boxed{ \mathfrak D\_{\mathrm{CCCD}} = \mathcal F[ \mathfrak S\_\omega, \mathfrak G, \mathfrak O, \mathfrak P ] } \\]

where:

- \\(\mathfrak S\_\omega\\) denotes state-dependent spectral information;
- \\(\mathfrak G\\) denotes spacetime geometry;
- \\(\mathfrak O\\) denotes the observable pair;
- \\(\mathfrak P\\) denotes the intervention and measurement protocol.

The inclusion of \\(\mathfrak O\\) and \\(\mathfrak P\\) is essential. There is no reason to expect a universal numerical disparity independent of which observables are measured or which interventions are permitted.

A more ambitious result would establish a restricted universality class:

\\[ \mathfrak D\_{\mathrm{CCCD}} = \mathcal F\_{\mathcal U} [ \mathfrak S\_\omega,\mathfrak G ] \\]

for a specified family \\(\mathcal U\\) of theories, states, observables, and protocols.

Such a relation would have to be proved under explicit assumptions.

### 8.5 Candidate inequality from causal support

For a microcausal theory, the response support lies within the causal region. Decompose the observational domain:

\\[ \Omega = \Omega\_{\mathrm{SL}} \cup \Omega\_{\mathrm{C}}, \\]

where \\(\Omega\_{\mathrm{SL}}\\) is spacelike and \\(\Omega\_{\mathrm C}\\) contains timelike and null-related pairs.

Then:

\\[ \mathfrak D\_{\mathrm{SL}} = \frac{ \mu\_\Omega(\mathcal S_K\cap\Omega\_{\mathrm{SL}}) }{ \mu\_\Omega(\Omega) }. \\]

Since the spacelike response support vanishes, this is exactly the correlation-only spacelike support fraction.

The elementary bound is:

\\[ 0\leq\mathfrak D\_{\mathrm{SL}} \leq \frac{\mu\_\Omega(\Omega\_{\mathrm{SL}})} {\mu\_\Omega(\Omega)} \leq1. \\]

This bound is mathematically correct but not physically deep. It follows immediately from measure inclusion.

A nontrivial CCCD theorem would need a stronger bound, for example:

\\[ \mathfrak D\_{\mathrm{SL}} \leq \mathcal B( m,\beta,\rho\_{\mathrm{KL}},\xi,\text{geometry} ), \\]

where \\(\mathcal B\\) is determined by independently measurable physical quantities and is strictly more informative than the trivial measure bound.

Such an inequality is a research target, not an established result.

## 9. Covariance and the geometry of disparity

A quantitative measure of correlation–response disparity should not depend spuriously on coordinate choices.

### 9.1 Covariant domain specification

Let \\(\Omega\subset M\times M\\) be a compact observational domain. A covariant measure should be constructed from the spacetime metric and explicitly specified scalar weights.

For example:

\\[ d\mu\_\Omega = w(x,y) \sqrt{|g(x)|}\sqrt{|g(y)|} \\,d^dx\\,d^dy, \\]

where \\(w(x,y)\\) is a scalar under simultaneous coordinate transformations.

The resulting measure is invariant under coordinate changes when the domain and weight are transformed consistently.

However, this does not automatically make the physical measurement protocol observer-independent.

A detector network introduces preferred worldlines, four-velocities, and time-ordering conventions. These must be represented geometrically.

### 9.2 Detector-frame variables

Let \\(u^\mu(x)\\) be the unit timelike four-velocity field of an observer congruence. The proper time measured along the observer worldline is:

\\[ d\tau^2=-g\_{\mu\nu}dx^\mu dx^\nu \\]

for signature \\((-+++)\\).

For two events assigned to a common detector frame, the experiment may characterize:

- proper temporal separation;
- spatial separation on a specified hypersurface;
- invariant interval;
- geodesic distance where defined;
- and the causal relation between localization regions.

A CCCD result should state which of these quantities defines the separation coordinate.

Coordinate distance alone is not a covariant measure of correlation range.

### 9.3 Region-based formulation

Pointwise support is not always the most operationally meaningful formulation.

Let \\(\mathcal O_A\\) and \\(\mathcal O_B\\) be bounded spacetime regions, and let \\(A\in\mathcal A(\mathcal O_A)\\), \\(B\in\mathcal A(\mathcal O_B)\\).

Define:

\\[ K\_\omega(\mathcal O_A,\mathcal O_B) = \omega(AB)-\omega(A)\omega(B). \\]

Define the response of \\(B\\) to a perturbation generated by \\(A\\) as:

\\[ R\_\omega(\mathcal O_B,\mathcal O_A) = \left. \frac{\delta\omega(B)} {\delta j_A} \right|\_{j_A=0}. \\]

For spacelike-separated regions, local commutativity implies zero retarded response under the corresponding local coupling.

This formulation is better suited to actual detector experiments because finite instruments never sample mathematical points.

### 9.4 Localization uncertainty

Suppose detector \\(A\\) has a compact spatial profile \\(f_A\\) and detector \\(B\\) has profile \\(f_B\\). Their effective supports are:

\\[ \operatorname{supp}f_A, \qquad \operatorname{supp}f_B. \\]

The relevant causal relation is between these regions, not merely their centers.

Two detector centers may be spacelike-separated while their extended supports overlap a causal region. In that case, an apparent response outside the center-to-center light cone need not violate microcausality.

The experimental definition of CCCD must therefore include detector localization widths and temporal switching profiles.

### 9.5 Curved spacetime

On a globally hyperbolic curved spacetime, the retarded Green function for a normally hyperbolic operator has support in the causal future:

\\[ \operatorname{supp}G_R \subseteq J^+. \\]

In four-dimensional curved spacetimes, propagation may exhibit tails inside the light cone, depending on the field equation and curvature. Such tails are causal: they do not imply support outside \\(J^+\\).

Meanwhile, the state-dependent two-point function can be nonzero for spacelike-separated points.

The CCCD distinction therefore survives curvature, provided the field theory is locally covariant and microcausal.

Curvature may, however, alter the amplitude, decay, and geometry of correlation support. A possible CCCD extension would investigate how curvature-dependent spectral structure affects the resolvable spacelike correlation range.

## 10. The role of quantum state

The support of the retarded commutator and the support of the correlation function have different state dependencies.

### 10.1 State independence of the causal constraint

For a local bosonic field in a microcausal theory:

\\[ [\mathcal O(x),\mathcal O(y)]=0 \\]

at spacelike separation as an operator identity.

Consequently:

\\[ \omega([\mathcal O(x),\mathcal O(y)])=0 \\]

for every admissible state \\(\omega\\).

Thus the spacelike vanishing of the retarded response is not a special property of the vacuum.

It follows from the local operator algebra.

### 10.2 State dependence of correlation

The correlation function:

\\[ K\_\omega(x,y) = \omega(\mathcal O(x)\mathcal O(y)) - \omega(\mathcal O(x))\omega(\mathcal O(y)) \\]

depends explicitly on the state.

Two states of the same theory may have different:

- correlation amplitudes;
- correlation lengths;
- asymptotic decay exponents;
- correlation spectra;
- entanglement structure;
- and finite-resolution support.

Therefore the CCCD disparity is potentially a sensitive probe of state preparation.

### 10.3 Vacuum, thermal, and excited states

Consider three classes of states:

1. Vacuum states.
2. Thermal equilibrium states.
3. Nonequilibrium excited states.

In all three, microcausality constrains the retarded response outside the light cone.

But their correlation structures can differ substantially.

The vacuum may exhibit correlations associated with quantum fluctuations. A thermal state introduces occupation-dependent correlations. An excited state may contain localized wave packets, long-range coherence, or additional correlation scales.

The comparison is particularly useful because the causal support constraint remains fixed while the state-dependent correlation support changes.

This gives a natural experimental strategy: hold the field theory and detector geometry fixed while varying the state.

### 10.4 Purity and mixedness

It would be incorrect to identify a large CCCD disparity with a large degree of entanglement or state purity.

A mixed thermal state can possess substantial correlations. A pure state can have weak correlations for a particular observable pair. Classical mixtures can also exhibit nonzero connected correlations.

A universal CCCD law must therefore identify which state properties actually determine the disparity.

Purity alone is unlikely to suffice.

### 10.5 Entanglement-sensitive extensions

For separated subsystems, one may compare CCCD measures with entanglement measures such as:

- negativity;
- logarithmic negativity;
- mutual information;
- entanglement entropy;
- relative entropy of entanglement.

For spacelike-separated regions, mutual information may be nonzero even when no causal response is possible.

A potential research question is whether any bound of the form

\\[ \mathfrak D\_{\mathrm{SL}} \leq \mathcal B(I(A:B),\mathcal G) \\]

exists, where \\(I(A:B)\\) is mutual information and \\(\mathcal G\\) specifies geometry and detector resolution.

Such a relation would need to distinguish quantum entanglement from classical correlation. Mutual information alone does not make that distinction.

No general inequality of this exact form is claimed in this paper.

## 11. Relationship to established theories

CCCD is best understood as a proposed organizing framework situated among several established results.

### 11.1 Microcausality

Microcausality provides the causal-support restriction:

\\[ \mathcal S_R\cap\mathcal D\_{\mathrm{SL}} = \varnothing. \\]

It does not determine the full correlation support.

CCCD takes this established result as a starting point rather than a discovery.

### 11.2 Bell nonlocality

Bell inequalities constrain the correlations predicted by local hidden-variable models.

A Bell-inequality violation demonstrates that quantum correlations cannot be represented by a model satisfying the relevant Bell-local factorization assumptions.

It does not imply controllable superluminal signaling.

CCCD is not a replacement for Bell nonlocality. Its primary object is the support mismatch between correlation and response functions, including in systems that need not violate a Bell inequality.

### 11.3 Reeh–Schlieder theorem

In relativistic quantum field theory, the vacuum is highly entangled across local regions. The Reeh–Schlieder theorem establishes a strong cyclicity property of the vacuum for local operator algebras under standard assumptions.

It helps explain why local regions can encode nontrivial global information.

However, it does not imply that a local operation can send a controllable signal to a spacelike-separated region.

CCCD does not derive the Reeh–Schlieder theorem. It identifies one operationally relevant aspect of the broader distinction between vacuum correlations and local causal influence.

### 11.4 Cluster decomposition

For suitable states and theories, connected correlations decay at large spacelike separation:

\\[ K\_\omega(x,y)\rightarrow0 \qquad \text{as spatial separation}\rightarrow\infty. \\]

In massive theories, the decay may be exponential. In massless theories or critical systems, it may be algebraic.

Cluster decomposition constrains the asymptotic behavior of correlation functions. It does not generally make their support identical to the causal-response support.

A finite-resolution CCCD range may be closely related to the correlation length appearing in cluster behavior.

### 11.5 Fluctuation–dissipation relations

Equilibrium fluctuation–dissipation relations connect correlation spectra with the dissipative part of linear response.

They are important candidate ingredients for quantitative CCCD laws.

But they do not identify the spacetime supports of the corresponding functions. Frequency-domain relations and spacetime support properties must not be conflated.

### 11.6 Algebraic quantum field theory

Algebraic quantum field theory provides a natural language for local observable algebras, spacelike commutativity, and state-dependent correlations.

It may be the most suitable mathematical setting for a rigorous extension of CCCD beyond elementary field models.

The region-based formulation in Section 9.3 is particularly compatible with this approach.

## 12. A proposed theorem programme

The most valuable contribution would be a theorem that goes beyond the known support distinction.

The following propositions define a research programme. They are not all established results.

### 12.1 Theorem A: causal-response support containment

Statement. Let a quantum field theory on a globally hyperbolic spacetime satisfy local commutativity for the relevant bosonic observables. Let the response be generated by a local perturbation coupled to an observable in a bounded region \\(\mathcal O_A\\). Then:

\\[ \boxed{ \operatorname{supp}R^{BA} \subseteq J^+(\mathcal O_A)\times\mathcal O_A } \\]

with the precise product ordering adjusted to the source and response arguments.

Status: Established consequence of microcausality and retarded response theory.

Assumptions: Local observables, local perturbation, appropriate well-defined linear response, and relativistic microcausality.

This result is the causal foundation of CCCD.

### 12.2 Theorem B: correlation support is not fixed by causal support

Proposition. There exist microcausal relativistic quantum field theories and admissible states for which:

\\[ \operatorname{supp}K\_\omega \not\subseteq \operatorname{supp}R\_\omega. \\]

Demonstration: The massive free scalar vacuum provides an explicit example, as shown in Section 4.

Status: Established by the example.

The result is an existence statement. It does not imply that every state and observable pair has nonzero spacelike correlation.

### 12.3 Theorem C: finite-domain support-discrepancy bound

For any measurable finite domain \\(\Omega\\) with finite nonzero measure:

\\[ 0\leq \mathfrak D\_{\mathrm{CCCD}} \leq1. \\]

Proof. The symmetric difference is a measurable subset of \\(\Omega\\). Therefore:

\\[ 0\leq \mu\_\Omega[ (\mathcal S_K\triangle\mathcal S_R)\cap\Omega ] \leq \mu\_\Omega(\Omega). \\]

Dividing by the positive total measure yields the bound.

Status: Proven elementary measure-theoretic result.

Limitation: The bound is not a nontrivial physical law. It does not constrain the disparity in terms of the state or field dynamics.

### 12.4 Theorem D: spacelike disparity in a microcausal theory

If:

\\[ \mathcal S_R\cap\Omega\_{\mathrm{SL}}=\varnothing, \\]

then:

\\[ \boxed{ \mathfrak D\_{\mathrm{SL}} = \frac{ \mu\_\Omega(\mathcal S_K\cap\Omega\_{\mathrm{SL}}) }{ \mu\_\Omega(\Omega) }. } \\]

Proof. On the spacelike domain, the response support is empty. Therefore the symmetric difference restricted to that domain reduces to the correlation support. The equality follows directly from the definition.

Status: Proven under the stated assumptions.

### 12.5 Conjecture E: spectral control of finite-resolution disparity

For a restricted class of stationary, homogeneous, clustering states, the large-distance behavior of finite-resolution spacelike CCCD may be controlled by the lowest relevant spectral threshold:

\\[ \boxed{ L_K(\varepsilon) \sim \frac{1}{\mu\_{\mathrm{eff}}} \left[ \log\frac{A}{\varepsilon} - \alpha\log L_K +\cdots \right]. } \\]

Here \\(\mu\_{\mathrm{eff}}\\) is a spectral scale, not necessarily a particle mass, and \\(A,\alpha\\) depend on the observable and asymptotic spectral density.

Status: Research conjecture.

Motivation: In massive theories, spacelike correlations commonly exhibit exponential decay multiplied by a power-law prefactor. Solving the threshold condition yields logarithmic dependence of the resolvable range on the detector threshold.

Required work: Derive the asymptotic relation for interacting theories and determine the role of multiparticle thresholds, bound states, and anomalous dimensions.

### 12.6 Conjecture F: critical scaling of CCCD

Near a continuous critical point, the correlation length may diverge while causal propagation remains constrained by the relativistic light cone.

A candidate scaling law is:

\\[ \boxed{ L_K(\varepsilon;\delta) = \xi(\delta)\\, \mathcal G\left( \varepsilon\\,\xi(\delta)^{\Delta_K}, \frac{t}{\xi(\delta)^z} \right), } \\]

where:

- \\(\delta\\) measures distance from criticality;
- \\(\xi(\delta)\\) is the correlation length;
- \\(z\\) is the dynamical critical exponent;
- \\(\Delta_K\\) is the scaling dimension relevant to the chosen correlation observable;
- \\(\mathcal G\\) is a scaling function.

A universal scaling form of this kind could produce a nontrivial CCCD signature.

Status: Conjectural extension of established critical scaling ideas.

It would need to be shown that the response range or response amplitude contributes a genuinely independent universal structure, rather than merely reproducing known dynamical critical scaling.

### 12.7 Conjecture G: curvature-sensitive CCCD

For a family of states on slowly varying curved backgrounds, the spacelike correlation profile may admit a local expansion:

\\[ K\_\omega(x,y) = K_0(\sigma) + R(x)\\,K_1(\sigma) + R\_{\mu\nu}(x)\\, \mathcal T^{\mu\nu}\_2(x,y) +\cdots, \\]

where \\(\sigma\\) denotes an appropriate geodesic separation variable and \\(R\\), \\(R\_{\mu\nu}\\) are curvature tensors.

A corresponding expansion of the finite-resolution disparity might reveal curvature-dependent corrections.

Status: Research conjecture.

Obstacle: Curved-spacetime two-point functions are sensitive to the quantum state and global geometry. A universal local curvature correction cannot be assumed without specifying the state class and field equation.

### 12.8 Conjecture H: an equilibrium disparity constraint

In thermal equilibrium, the fluctuation–dissipation theorem constrains the frequency-domain relationship between correlation and response.

A possible CCCD result would establish bounds on the spacelike correlation profile in terms of the retarded spectral density and temperature:

\\[ \boxed{ \mathfrak D\_{\mathrm{SL}} \leq \mathcal B\_\beta[ \rho\_{\mathrm{spec}}, \Omega, \varepsilon_K ]. } \\]

Status: Open research problem.

Obstacle: The inverse Fourier transform, thresholding, detector smearing, and finite-domain measure all enter the support functional. A simple pointwise spectral inequality does not automatically yield a support-measure bound.

## 13. Operational experimental programme

The central empirical principle is that correlation and response must be measured independently.

A nonzero correlation measurement alone cannot establish a causal response. Conversely, the absence of an observed response does not establish exact mathematical vanishing without a sufficiently sensitive intervention protocol.

### 13.1 Experimental architecture

[Entanglement harvesting of three Unruh-DeWitt detectors · Issue #2902 · github-nakasho/quantph · GitHub](https://images.openai.com/static-rsc-4/v1ENb38ymfdBUTvj5_3Efdc8KyazY76t1KINk0P1JW2NjbdOz2VP_1PNEZUh581XlqC1UuRgAy-eRspGAQ-KlVBYHDirzt0yu6edsyoW-8NDYyYH6o8lOcV6ni8lnLRfHqufQGQqB_XsDhz4drx_axf2cbAyzwjR20ae8mt6A1o?purpose=inline)

Consider two localized detectors, \\(A\\) and \\(B\\), coupled to a common quantum field.

The detectors are positioned so that their interaction regions can be varied between:

- timelike separation;
- null separation;
- spacelike separation.

Each detector has a controllable switching function:

\\[ \chi_A(t),\qquad \chi_B(t), \\]

and a localized spatial profile:

\\[ f_A(\mathbf x),\qquad f_B(\mathbf x). \\]

The coupling strengths are:

\\[ \lambda_A,\qquad\lambda_B. \\]

The detector geometry and switching functions must be chosen so that the entire interaction supports, not merely the detector centers, are spacelike-separated in the spacelike trials.

### 13.2 Correlation measurement

The experiment first estimates a connected correlation observable.

For detector readouts \\(X_A,X_B\\):

\\[ \widehat K\_{AB} = \langle X_AX_B\rangle - \langle X_A\rangle\langle X_B\rangle. \\]

The estimator should be evaluated across controlled separations and repeated for multiple detector profiles.

Possible implementations include:

- entangled photonic systems;
- superconducting qubit arrays;
- trapped-ion systems;
- quantum simulators;
- detector models coupled to engineered bosonic fields.

The interpretation depends on whether the measured correlation is a field correlation, detector correlation, or a correlation induced by their interaction history.

These should not be conflated.

### 13.3 Response measurement

A separate intervention is applied at detector \\(A\\).

Let \\(\lambda_A\\) be varied by a small amount. Measure the change in the expectation of detector \\(B\\):

\\[ R\_{B\leftarrow A} = \left. \frac{\partial\langle X_B\rangle} {\partial\lambda_A} \right|\_{\lambda_A=0}. \\]

For a time-dependent source:

\\[ R\_{B\leftarrow A}(t_B,t_A) = \left. \frac{\delta\langle X_B(t_B)\rangle} {\delta j_A(t_A)} \right|\_{j_A=0}. \\]

The measurement must use unconditional statistics at \\(B\\). Conditioning on the recorded outcome at \\(A\\) can reveal correlations without demonstrating a causal response.

### 13.4 Controlled separation sweep

The detector separation is varied over a range of spacetime intervals.

Define the invariant interval:

\\[ s^2 = c^2\Delta t^2-\Delta r^2. \\]

The experiment should sample:

\\[ s^2>0, \qquad s^2=0, \qquad s^2<0. \\]

For each separation, record:

\\[ \widehat K(s^2), \qquad \widehat R(s^2). \\]

A controlled sweep across the light-cone boundary allows the support structures to be compared directly.

### 13.5 Reconstructing finite-resolution supports

Given estimators and uncertainty bounds, construct:

\\[ \widehat{\mathcal S}\_K^{(\varepsilon_K)} = \left\\{ (x,y): |\widehat K(x,y)| > \varepsilon_K(x,y) \right\\}, \\]

and:

\\[ \widehat{\mathcal S}\_R^{(\varepsilon_R)} = \left\\{ (x,y): |\widehat R(x,y)| > \varepsilon_R(x,y) \right\\}. \\]

The thresholds should be established before the main analysis.

The measured CCCD discrepancy is:

\\[ \widehat{\mathfrak D}\_{\mathrm{CCCD}} = \frac{ \widehat\mu\_\Omega[ \widehat{\mathcal S}\_K^{(\varepsilon_K)} \triangle \widehat{\mathcal S}\_R^{(\varepsilon_R)} ] }{ \widehat\mu\_\Omega(\Omega) }. \\]

Uncertainty in this quantity should be estimated using an appropriate resampling or likelihood procedure that accounts for correlations between sampled spacetime points.

### 13.6 Essential controls

The experimental design must address:

1. Detector cross-talk.
2. Classical communication leakage.
3. Common environmental noise.
4. Timing synchronization.
5. Imperfect spacetime localization.
6. Switching-function tails.
7. State-preparation errors.
8. Calibration drift.
9. Finite sample size.
10. Conditional-versus-unconditional statistical analysis.

A particularly important issue is that switching functions with noncompact temporal tails can create effective interaction overlap even when nominal switching centers are spacelike-separated.

Compact support or quantitatively bounded tails are needed for a defensible causal analysis.

### 13.7 Statistical rejection criteria

The null hypothesis for spacelike causal response is:

\\[ H_0: R\_\omega(x,y)=0 \quad \text{for spacelike-separated interaction regions}. \\]

A detected nonzero response would not immediately falsify relativistic microcausality. The first task would be to eliminate:

- residual causal overlap;
- detector cross-talk;
- postselection artifacts;
- nonlocal control circuitry;
- and errors in the intervention definition.

Only after those possibilities are excluded would a genuine violation of the assumed local causal model be implicated.

The correlation hypothesis is different:

\\[ H_K: K\_\omega(x,y)\neq0 \\]

for at least some spacelike-separated pairs.

This should be tested against a state-specific theoretical prediction, rather than treated as universally true for every observable pair.

### 13.8 What would count as a discovery?

A measurement of nonzero spacelike correlation with zero spacelike response would reproduce established quantum field theory.

A potentially new result would require at least one of the following:

- a universal scaling law for the spacelike correlation range;
- a state-dependent disparity invariant;
- a sharp bound relating disparity to spectral data;
- a new critical exponent or universal scaling function;
- a curvature-dependent CCCD correction;
- or an operational theorem identifying a minimal set of measurements sufficient to reconstruct the disparity.

The experiment must distinguish such a result from known fluctuation–dissipation, clustering, and spectral relations.

## 14. Computational reconstruction and numerical programme

### 14.1 Model hierarchy

A useful numerical programme should proceed from analytically controlled models to more complex interacting systems.

| Model                        | Principal CCCD role        | Main issue                               |
| ---------------------------- | -------------------------- | ---------------------------------------- |
| Free massive scalar field    | Exact baseline             | Bessel-function decay                    |
| Free massless scalar field   | Long-range baseline        | Infrared and dimensional dependence      |
| Harmonic oscillator chain    | Discrete controlled system | Lattice propagation                      |
| Transverse-field Ising model | Critical scaling           | Finite-size effects                      |
| Interacting scalar field     | Spectral broadening        | Nonperturbative dynamics                 |
| Curved-spacetime field       | Geometry dependence        | State selection                          |
| Thermal field theory         | Equilibrium constraints    | KMS structure                            |
| Nonequilibrium field theory  | State dependence           | No universal fluctuation–dissipation law |

### 14.2 Numerical observables

For each model, compute:

\\[ K\_\omega(t,r), \qquad R\_\omega(t,r), \\]

over a finite spacetime grid.

Then calculate:

\\[ \mathfrak D\_{\mathrm{CCCD}}(\varepsilon_K,\varepsilon_R), \\]

\\[ \widehat{\mathfrak D}\_{\mathrm{SL}}, \\]

\\[ \mathcal O\_{KR}, \\]

and:

\\[ \Delta L\_{\mathrm{CCCD}}. \\]

The output should include uncertainty or numerical error estimates.

### 14.3 Finite-size scaling

For a lattice model with linear system size \\(L\\), calculate the disparity at several values of \\(L\\).

A finite-size scaling ansatz might be:

\\[ \mathfrak D\_{\mathrm{CCCD}}(L,\delta) = L^{-\kappa} \mathcal F(\delta L^{1/\nu}) + D\_{\mathrm{reg}}, \\]

where:

- \\(\delta\\) measures distance from criticality;
- \\(\nu\\) is a correlation-length exponent;
- \\(\kappa\\) is an exponent to be determined;
- \\(D\_{\mathrm{reg}}\\) is a regular background term.

This is a proposed fitting form, not a universal identity.

The exponent \\(\kappa\\) should not be assumed to be independent of observable choice or threshold prescription.

### 14.4 Numerical stability

The exact-support functional is particularly vulnerable to numerical noise. A single floating-point residue can change whether a grid point is classified as part of the support.

Consequently, numerical work should prioritize:

- threshold sweeps;
- smooth-support measures;
- convergence under grid refinement;
- comparison between independent numerical methods;
- and error propagation from the correlator and response estimators.

A claimed CCCD invariant should remain stable under these changes within a declared regime.

## 15. Potential applications

The immediate scientific value of CCCD is diagnostic rather than technological. It provides a common language for comparing correlation structure and causal response.

### 15.1 Quantum communication

CCCD may help distinguish:

- correlation available for distributed quantum protocols;
- controllable communication channels;
- operationally accessible information;
- and causal response to local interventions.

It could be useful in characterizing networks where strong correlations coexist with strict no-signaling constraints.

### 15.2 Quantum sensing

A sensor array may detect correlations between separated probes even when local perturbations do not propagate between them.

The distinction could help characterize:

- correlated noise;
- vacuum fluctuations;
- common quantum environments;
- and the limits of distributed sensing.

The presence of a correlation does not by itself establish a useful sensing resource. Its operational utility must be demonstrated.

### 15.3 Quantum many-body systems

In extended quantum systems, correlations may develop long-range structure near criticality while response functions display distinct dynamical behavior.

CCCD could provide a comparative diagnostic for:

- correlation length;
- dynamical critical scaling;
- collective excitations;
- transport;
- and relaxation.

### 15.4 Relativistic quantum information

The framework may assist in quantifying the difference between information shared across spacelike-separated regions and information that can be transmitted through causal channels.

The most useful formulation would likely employ local algebras, detector models, and operational channel distinguishability.

### 15.5 Curved-spacetime quantum fields

A state-dependent correlation profile may encode information about horizon structure, curvature, and global field modes.

CCCD could provide a way to compare those correlations with local causal response.

However, no claim is made that support disparity alone detects horizons or measures spacetime curvature. Such applications would require an independently derived relationship.

### 15.6 Analogue gravity

Condensed-matter systems with effective causal cones can provide controlled environments in which correlation and response profiles are reconstructed.

Examples include:

- acoustic horizons;
- polariton systems;
- driven optical media;
- superconducting circuits;
- and engineered lattice systems.

These systems do not reproduce every feature of fundamental relativistic quantum field theory. Their effective metrics, dispersion relations, and ultraviolet behavior must be included in the model.

## 16. Limitations and unresolved mathematical problems

A rigorous CCCD theory must confront several obstacles before any universal claim can be justified.

### 16.1 Dependence on observable choice

The correlation support is not a property of the state alone.

For example, two observables may have vanishing connected correlation in a state even though other observable pairs are correlated.

Thus:

\\[ \mathcal S_K = \mathcal S_K[\omega,A,B]. \\]

Likewise:

\\[ \mathcal S_R = \mathcal S_R[\omega,A,B,\mathfrak I], \\]

where \\(\mathfrak I\\) specifies the intervention.

Any state-only CCCD invariant would need to aggregate over a declared complete observable family.

### 16.2 Exact support is unstable

A function can be arbitrarily small yet nonzero. Exact support therefore does not correspond directly to finite experimental detectability.

Thresholded support introduces dependence on calibration and statistical confidence.

The framework must report threshold dependence rather than conceal it.

### 16.3 Distributional subtleties

Quantum field correlation functions can be singular on the light cone and at coincident points.

A support measure over these singular sets may be mathematically ill-defined or physically uninformative without regularization.

Smeared observables, wavefront-set analysis, or carefully defined distributional measures may be necessary.

### 16.4 Correlation is not entanglement

A nonzero connected correlation may be classical.

A CCCD analysis that interprets every nonzero correlation as entanglement would be incorrect.

Quantum-specific extensions must include entanglement witnesses or operational tests that distinguish entangled from separable states.

### 16.5 Response depends on intervention

Different interventions can produce different response functions.

The linear response function is determined by the coupling operator, source profile, and state.

A universal comparison therefore requires a standardized intervention class.

### 16.6 Equilibrium relations do not automatically generalize

The fluctuation–dissipation theorem imposes a powerful equilibrium constraint, but generic nonequilibrium states need not obey it.

One cannot infer a universal CCCD law by extending the equilibrium relation without proof.

### 16.7 Finite-domain dependence

The support-discrepancy measure depends on the observational domain and its measure.

Two experiments sampling different spacetime regions can report different disparity values for the same underlying field state.

This is not a mathematical defect if the domain is part of the observable definition, but it prevents the raw measure from being an intrinsic universal constant.

### 16.8 Causal support does not specify amplitude

The retarded response may be nonzero throughout a causal region, but its amplitude can decay, oscillate, or vanish on submanifolds.

Support geometry and response strength must be studied separately.

### 16.9 No automatic ontological conclusion

The mismatch does not establish that correlations are literally timeless, that no underlying mediator exists, or that the universe contains a separate noncausal correlation mechanism.

CCCD is initially an operational and mathematical framework.

Any ontological interpretation would require independent evidence.

## 17. Novelty assessment

### 17.1 What is already established

The following components are part of established physics:

1. Relativistic microcausality.
2. Vanishing of local commutator response at spacelike separation.
3. Nonzero spacelike vacuum correlations in relativistic quantum field theory.
4. The distinction between Wightman and retarded functions.
5. The Källén–Lehmann spectral representation.
6. The fluctuation–dissipation theorem in equilibrium.
7. Exponential clustering in suitable massive theories.
8. State dependence of correlation functions.
9. The distinction between quantum correlations and controllable signaling.

None of these should be claimed as a discovery of CCCD.

### 17.2 What is potentially new

The framework could produce a contribution through:

- a covariant finite-domain support-discrepancy invariant;
- a threshold-stable operational disparity functional;
- a universal spectral bound;
- a critical scaling law for correlation–response support mismatch;
- a curvature-sensitive disparity relation;
- or a complete classification of disparity by state, observable, and intervention equivalence classes.

The strongest result would be a theorem linking a nontrivial CCCD functional to independently measurable state parameters.

### 17.3 What would not count as novelty

The following would be insufficient:

- demonstrating nonzero spacelike vacuum correlations;
- restating microcausality;
- defining the symmetric difference of two supports without further results;
- reporting a detector correlation without a separate intervention experiment;
- assigning a universal numerical value to a domain-dependent support ratio;
- or treating correlation as evidence of superluminal causal influence.

### 17.4 The principal obstacle

The major mathematical obstacle is that correlation and response are different functions with different physical dimensions and different operational definitions.

Their supports can be compared geometrically, but a universal relationship between them is not guaranteed.

Even in equilibrium, where their spectra are related, the conversion between spectral information and spacetime support is nontrivial.

A genuinely new CCCD theory must solve this problem rather than merely describe it.

### 17.5 A decisive novelty criterion

A successful CCCD result should satisfy the following test:

There must exist a specified family of theories \\(\mathcal U\\), states \\(\omega\\), observables \\(A,B\\), and protocols \\(\mathfrak I\\) for which a proposed relation

\\[ \boxed{ \mathfrak D\_{\mathrm{CCCD}} = \mathcal F(\text{independent physical data}) } \\]

is:

1. mathematically derived;
2. independent of arbitrary coordinate choices;
3. stable under a declared range of detector resolutions;
4. nontrivial beyond microcausality and known spectral identities;
5. falsifiable by a controlled experiment;
6. and reproducible across independent models in the stated universality class.

That is the threshold separating a useful relabeling of known physics from a substantive new result.

## 18. Research roadmap: from support disparity to a predictive theory

The next phase of CCCD should not begin by expanding its terminology. It should begin by identifying the smallest mathematical result that would establish predictive content.

I propose the following sequence.

### Stage I — Establish the operational definition

Fix a reference model, preferably a massive free scalar field, and specify:

\\[ \mathfrak C = (M,g,\omega,\mathcal O_A,\mathcal O_B,\Omega, \varepsilon_K,\varepsilon_R,\mathfrak I). \\]

Here \\(\mathfrak C\\) is the complete CCCD experimental configuration.

Calculate the exact correlation and response functions, their smeared versions, and their finite-resolution support measures.

The result is a reproducible baseline rather than a new physical law.

### Stage II — Establish stability

Prove or numerically verify that the proposed soft disparity functional converges under:

- detector-profile refinement;
- spacetime-grid refinement;
- changes in the sampling measure;
- reasonable threshold variation;
- and perturbations of the state.

The objective is to determine which parts of CCCD are robust observables and which are artifacts of measurement conventions.

### Stage III — Establish state sensitivity

Compare states of the same field theory:

\\[ \omega_1,\omega_2,\ldots,\omega_n. \\]

Determine whether their disparity profiles can be predicted from independently measured quantities such as:

\\[ \\{\rho\_{\mathrm{spec}},\beta,\xi,\Delta\_{\mathcal O}, \text{occupation data}\\}. \\]

This is the first stage at which CCCD might reveal a new quantitative regularity.

### Stage IV — Establish universality

Compare physically distinct models near corresponding scaling regimes.

A genuine universal result should survive changes in microscopic details while retaining a common scaling law or invariant.

The relevant comparison is not simply whether two models have nonzero spacelike correlations. It is whether their normalized disparity profiles converge to the same function or critical parameter.

### Stage V — Establish a falsifiable theorem

The final objective is a result of the form:

\\[ \boxed{ \mathfrak D\_{\mathrm{CCCD}} \leq \mathcal B( \text{spectral data}, \text{state parameters}, \text{geometry}, \text{resolution} ) } \\]

or:

\\[ \boxed{ \lim\_{\delta\rightarrow0} \mathfrak D\_{\mathrm{CCCD}}(\delta) = D\_\* } \\]

within a specified universality class.

The first would be a quantitative bound. The second would be a universal critical limit.

Either could establish a substantial contribution, provided the relation is nontrivial, rigorously derived, and experimentally falsifiable.

## 19. Conclusion

Correlation and causal response are distinct structures in relativistic quantum theory.

The connected correlation function describes statistical dependence between observables in a specified state. The retarded response function describes the change in an observable produced by a specified perturbation. Their mathematical definitions differ, their physical interpretations differ, and their spacetime supports need not coincide.

Microcausality imposes a strict constraint on the latter:

\\[ R\_\omega(x,y)=0 \\]

for spacelike-separated localized observables in a local relativistic quantum field theory.

It does not impose the corresponding condition:

\\[ K\_\omega(x,y)=0. \\]

The vacuum of the massive free scalar field provides an explicit demonstration. Its connected two-point function is nonzero at spacelike separation, while its retarded response vanishes there. The phenomenon persists in broader classes of local relativistic theories and is compatible with the spectral structure of quantum fields.

The present work introduces Correlation–Causal Cone Disparity as a framework for studying this difference quantitatively. It defines exact and finite-resolution supports, constructs normalized symmetric-difference measures, distinguishes correlation-only from response-only support, and introduces spacelike disparity, overlap, amplitude-weighted discrepancy, and correlation-range profiles.

The mathematical framework also identifies an important distinction between three levels of analysis:

\\[ \boxed{ \begin{aligned} \text{Level I:}&\quad \text{Support geometry},\\\\[2mm] \text{Level II:}&\quad \text{Correlation and response amplitudes},\\\\[2mm] \text{Level III:}&\quad \text{State-dependent universal relations}. \end{aligned} } \\]

The first level is straightforward to formulate and is already grounded in established physics. The second requires operational normalization and finite-resolution analysis. The third remains the central research challenge.

The decisive question is whether the support disparity contains information that can be predicted from spectral structure, state parameters, critical behavior, or spacetime geometry through a relation stronger than existing microcausality and fluctuation–dissipation results.

The framework does not establish a new causal mechanism, a superluminal process, or a timeless ontology. Nor does it claim that every nonzero correlation is an entanglement witness. Its purpose is more precise: to make the difference between statistical dependence and causal influence measurable, mathematically organized, and open to quantitative classification.

The central research proposition may therefore be stated as follows:

\\[ \boxed{ \textit{ The spacetime support of quantum correlation and the spacetime support of causal response are independently structured, but may be quantitatively constrained by the spectral and geometric organization of the underlying physical state. } } \\]

The first clause is established. The second is the conjectural research programme.

If CCCD is to become a predictive theory rather than a descriptive framework, its defining achievement must be a universal disparity law: a relation that determines how much correlation can exist beyond causal-response support, how that extension depends on the quantum state, and how it changes under controlled variations of geometry, temperature, spectral structure, and observational resolution.

That is the mathematical problem left open.

## Appendix A. Consolidated mathematical definitions

For reference, the principal quantities are collected below.

| Object                | Definition                                                                                 | Interpretation                                              |
| --------------------- | ------------------------------------------------------------------------------------------ | ----------------------------------------------------------- |
| Connected correlation | \\(K\_\omega(x,y)=\omega(AB)-\omega(A)\omega(B)\\)                                         | Statistical dependence                                      |
| Retarded response     | \\(R\_\omega(x,y)=i\theta(x\succ y)\omega([A,B])\\)                                        | Linear causal response                                      |
| Correlation support   | \\(\mathcal S_K=\operatorname{supp}K\_\omega\\)                                            | Region of nonzero correlation distribution                  |
| Response support      | \\(\mathcal S_R=\operatorname{supp}R\_\omega\\)                                            | Region of nonzero response distribution                     |
| Symmetric discrepancy | \\(\mathfrak D\_{\mathrm{CCCD}}=\mu(\mathcal S_K\triangle\mathcal S_R)/\mu(\Omega)\\)      | Total support mismatch                                      |
| Spacelike discrepancy | \\(\mathfrak D\_{\mathrm{SL}}=\mu(\mathcal S_K\cap\Omega\_{\mathrm{SL}})/\mu(\Omega)\\)    | Spacelike correlation-only fraction in a microcausal theory |
| Support overlap       | \\(\mathcal O\_{KR}=\mu(\mathcal S_K\cap\mathcal S_R)/\mu(\mathcal S_K\cup\mathcal S_R)\\) | Relative support coincidence                                |
| Soft discrepancy      | \\(\int\_\Omega\|q_K-q_R\|d\mu/\mu(\Omega)\\)                                              | Resolution-regularized mismatch                             |
| Correlation range     | \\(L_K(\varepsilon;t)\\)                                                                   | Threshold-dependent spatial correlation extent              |
| Response range        | \\(L_R(\varepsilon;t)\\)                                                                   | Threshold-dependent response extent                         |
| Range disparity       | \\(\Delta L=L_K-L_R\\)                                                                     | Difference between operational ranges                       |

These definitions are not interchangeable. A study must identify which measure is being used and why it is appropriate for the physical question.

## Appendix B. Core assumptions and their consequences

| Assumption                        | Consequence                                              | Status                                |
| --------------------------------- | -------------------------------------------------------- | ------------------------------------- |
| Globally hyperbolic spacetime     | Well-posed causal evolution for suitable field equations | Established framework                 |
| Locality of observable algebras   | Spacelike commutativity                                  | Established assumption of local QFT   |
| Local perturbative coupling       | Response represented by retarded commutator              | Established linear-response framework |
| Specified quantum state           | State-dependent correlation function                     | Definition                            |
| Finite observational domain       | Finite normalized support measure can be constructed     | Mathematical requirement              |
| Measurable thresholds             | Operationally resolvable support                         | Experimental convention               |
| Equilibrium KMS condition         | Fluctuation–dissipation relation                         | Established result                    |
| Spectral control of CCCD scaling  | Potential universal disparity law                        | Open problem                          |
| Curvature dependence of disparity | Geometric CCCD correction                                | Open problem                          |

## Appendix C. Recommended foundational literature

The following works establish the principal mathematical and physical background. They are not evidence that the CCCD framework itself has already been established as a distinct theory.

1\. Wightman, A. S. (1956). Quantum Field Theory in Terms of Vacuum Expectation Values. Physical Review, 101, 860–866. Foundational formulation of relativistic field theory through vacuum expectation values.

2\. Källén, G. (1952). On the Definition of the Renormalization Constants in Quantum Electrodynamics. Helvetica Physica Acta, 25, 417–434. Early spectral representation results.

3\. Lehmann, H. (1954). On the Properties of Propagation Functions and Renormalization Constants of Quantized Fields. Il Nuovo Cimento, 11, 342–357. Spectral structure of quantum-field propagators.

4\. Reeh, H., and Schlieder, S. (1961). Bemerkungen zur Unitäräquivalenz von Lorentzinvarianten Feldern. Il Nuovo Cimento, 22, 1051–1068. Local algebraic properties of relativistic quantum fields.

5\. Kubo, R. (1957). Statistical-Mechanical Theory of Irreversible Processes. I. General Theory and Simple Applications to Magnetic and Conduction Problems. Journal of the Physical Society of Japan, 12, 570–586. Linear response and the foundations of response theory.

6\. Martin, P. C., and Schwinger, J. (1959). Theory of Many-Particle Systems. I. Physical Review, 115, 1342–1373. Correlation functions and nonequilibrium many-body theory.

7\. Haag, R. (1996). Local Quantum Physics: Fields, Particles, Algebras. Springer. Algebraic quantum field theory and local observables.

8\. Birrell, N. D., and Davies, P. C. W. (1982). Quantum Fields in Curved Space. Cambridge University Press. Quantum fields, causal propagation, and state-dependent correlations in curved spacetime.

9\. Bratteli, O., and Robinson, D. W. (1987). Operator Algebras and Quantum Statistical Mechanics 2. Springer. KMS states and operator-algebraic statistical mechanics.

10\. Peskin, M. E., and Schroeder, D. V. (1995). An Introduction to Quantum Field Theory. Westview Press. Relativistic field theory, propagators, and commutator structure.
